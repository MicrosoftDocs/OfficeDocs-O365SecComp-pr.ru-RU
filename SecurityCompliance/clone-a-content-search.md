---
title: Клонирование поиска контента в центре безопасности &amp; и соответствия требованиям Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: С помощью скрипта Windows PowerShell в этой статье можно быстро клонировать существующий поиск контента в Поиск центра &amp; безопасности комплиане Center. При клонировании поиска создается новый поиск (с новым именем), содержащий те же свойства, что и исходный Поиск. Затем можно изменить новый поиск (изменив запрос ключевых слов или диапазон дат), а затем запустить его.
ms.openlocfilehash: 15f1ca5d00f03f510745fef7ae8418192a9eb448
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213549"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="e3067-105">Клонирование поиска контента в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="e3067-105">Clone a Content Search in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="e3067-p102">Создание поиска контента в центре безопасности &amp; и соответствия требованиям Office 365, который ищет большое количество почтовых ящиков или сайтов SharePoint и OneDrive для бизнеса, может занять некоторое время. Указание сайтов для поиска также может привести к ошибкам при ошибочном вводе URL-адреса. Чтобы избежать этих проблем, можно использовать сценарий Windows PowerShell, описанный в этой статье, для быстрой клонирования существующего поиска контента. При клонировании поиска создается новый поиск (с другим именем), содержащий те же свойства (такие как расположения контента и поисковый запрос), что и в исходном поиске. После этого вы можете изменить новый поиск (изменив запрос ключевых слов или диапазон дат) и запуская его.</span><span class="sxs-lookup"><span data-stu-id="e3067-p102">Creating a Content Search in Office 365 Security &amp; Compliance Center that searches a lot of mailboxes or SharePoint and OneDrive for Business sites can take awhile. Specifying the sites to search can also be prone to errors if you mistype a URL. To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search. When a you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search. Then you can edit the new search (by changing the keyword query or the date range) and run it.</span></span>
  
<span data-ttu-id="e3067-111">Зачем выполнять поиск по клону контента?</span><span class="sxs-lookup"><span data-stu-id="e3067-111">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="e3067-112">Чтобы сравнить результаты разных запросов поиска ключевых слов, выполните одно и то же расположение контента.</span><span class="sxs-lookup"><span data-stu-id="e3067-112">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="e3067-113">Для сохранения необходимости повторного ввода большого количества расположений контента при создании нового поиска.</span><span class="sxs-lookup"><span data-stu-id="e3067-113">To save you from having to re-enter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="e3067-114">Для уменьшения размера результатов поиска; Например, если у вас есть поиск, возвращающий слишком много результатов для экспорта, можно клонировать Поиск, а затем добавить условие поиска на основе диапазона дат, чтобы уменьшить количество результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="e3067-114">To decrease the size of the search results; for example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="e3067-115">Подготовка</span><span class="sxs-lookup"><span data-stu-id="e3067-115">Before you begin</span></span>

- <span data-ttu-id="e3067-116">Для запуска сценария, описанного в этом разделе, необходимо быть членом группы &amp; ролей "Диспетчер обнаружения электронных данных" в центре соответствия требованиям безопасности.</span><span class="sxs-lookup"><span data-stu-id="e3067-116">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="e3067-p103">Сценарий включает в себя минимальную обработку ошибок. Основной целью сценария является быстрая клонирование поиска контента.</span><span class="sxs-lookup"><span data-stu-id="e3067-p103">The script includes minimal error handling. The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="e3067-119">Сценарий создает новый поиск контента, но не запускает его.</span><span class="sxs-lookup"><span data-stu-id="e3067-119">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="e3067-p104">В этом сценарии учитывается, связан ли составной контент, для которого выполняется клонирование, с вариантом обнаружения электронных данных. Если поиск связан с обращением, новый поиск также будет связан с тем же случаем. Если существующий Поиск не связан с обращением, новый поиск будет указан на странице " **Поиск контента** " в центре безопасности &amp; и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="e3067-p104">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case. If the search is associated with a case, the new search will also be associated with the same case. If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="e3067-p105">Пример сценария, представленный в этом разделе, не поддерживается ни в одной из стандартных программ или услуг поддержки Майкрософт. Пример сценария предоставляется без каких-либо гарантий. Кроме того, корпорация Майкрософт отказывается от подразумеваемых гарантий, в том числе без каких бы то ни было ограничений. Весь риск, возникающий из примера использования или производительности примера сценария и документации, остается без вас. В противном случае корпорация Майкрософт, ее авторы или другие пользователи, участвующие в создании, производстве или доставке сценариев, не несут никакого ущерба (в том числе без ограничений, ущерба для потери прибыли бизнеса, перерыва в работе, потери Бизнес-информация или другие потери пекуниари), которые применяют или не могут использовать примеры сценариев или документации, даже если корпорация Майкрософт приходила к возможности такого ущерба.</span><span class="sxs-lookup"><span data-stu-id="e3067-p105">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="e3067-128">Шаг 1: запуск скрипта для клонирования поиска</span><span class="sxs-lookup"><span data-stu-id="e3067-128">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="e3067-p106">Скрипт на этом шаге создаст новый поиск контента, выполнив клонирование существующего контента. При выполнении этого сценария будут выведены следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="e3067-p106">The script in this step will create a new Content Search by cloning an existing one. When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="e3067-p107">**Ваши учетные данные пользователя** : сценарий будет использовать ваши учетные данные для подключения &amp; к центру соответствия требованиям безопасности для вашей организации Office 365 с Windows PowerShell. Как было сказано ранее, для запуска скрипта необходимо быть членом группы ролей "Диспетчер обнаружения электронных &amp; данных" в центре соответствия требованиям безопасности.</span><span class="sxs-lookup"><span data-stu-id="e3067-p107">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center for your Office 365 organization with Windows PowerShell. As previously stated, you have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script.</span></span> 
    
- <span data-ttu-id="e3067-133">**Имя существующего поиска** — это поиск контента, который необходимо клонировать.</span><span class="sxs-lookup"><span data-stu-id="e3067-133">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="e3067-134">**Имя нового поиска, который будет создан** — если оставить это значение пустым, сценарий создаст имя для нового поиска, основанное на имени клонированного запроса.</span><span class="sxs-lookup"><span data-stu-id="e3067-134">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="e3067-135">Для клонирования поиска:</span><span class="sxs-lookup"><span data-stu-id="e3067-135">To clone a search:</span></span>
  
1. <span data-ttu-id="e3067-136">Сохраните приведенный ниже текст в файле скрипта Windows PowerShell, используя суффикс имени файла PS1; Пример: `CloneSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="e3067-136">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
  ```
  # This PowerShell script clones an existing Content Search in the Office 365 Security &amp; Compliance Center
  # Get login credentials from the user
  if(!$UserCredential)
  {
      $UserCredential = Get-Credential
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
      if (!$Session)
      {
          Write-Error "Couldn't create a remote PowerShell session."
          return
      }
      Import-PSSession $Session -AllowClobber -DisableNameChecking
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)"
  }
  # Ask for the name of the search you want to clone
  $searchName = Read-Host 'Enter the name of the search that you want to clone'
  # Ask for the name of the new search
  $newSearchName = Read-Host 'Enter a name for the new search [leave blank to automatically generate a name]'
  $originalSearch = Get-ComplianceSearch $searchName -EA SilentlyContinue
  # Make sure we have a valid search before continuing
  if(!$originalSearch)
  {
      Write-Error "Couldn't find search: $searchName"
      return
  }
  $searchNameCounter = 1
  # Find a suitable name for the new search
  while(!$newSearchName)
  {
      $newSearchName = $originalSearch.Name + "_" + $searchNameCounter
      $tempSearch = Get-ComplianceSearch $newSearchName -EA SilentlyContinue
      if ($tempSearch)
      {
          $newSearchName = $null
          $searchNameCounter++
      }
  }
  $caseName
  # Determine if the search is part of a case; if so get the case name
  if ($originalSearch.CaseId)
  {
      $searchCase = Get-ComplianceCase $originalSearch.CaseId
      $caseName = $searchCase.Name
  }
  # Need to cast this value as a Boolean the old fashion way
  $allowNotFoundExchangeLocationsEnabled = $false
  if ($originalSearch.AllowNotFoundExchangeLocationsEnabled)
  {
      $allowNotFoundExchangeLocationsEnabled = $true
  }
  $newSearch = New-ComplianceSearch -Name $newSearchName -AllowNotFoundExchangeLocationsEnabled $allowNotFoundExchangeLocationsEnabled -Case $caseName -ContentMatchQuery $originalSearch.ContentMatchQuery -Description $originalSearch.Description -ExchangeLocation $originalSearch.ExchangeLocation -ExchangeLocationExclusion $originalSearch.ExchangeLocationExclusion -Language $originalSearch.Language -SharePointLocation $originalSearch.SharePointLocation -SharePointLocationExclusion $originalSearch.SharePointLocationExclusion -PublicFolderLocation $originalSearch.PublicFolderLocation
  if ($newSearch)
  {
      Write-Host $newSearch.Name "was successfully created" -ForegroundColor Yellow
  }
  ```

2. <span data-ttu-id="e3067-137">Откройте Windows PowerShell и перейдите к папке, в которой вы сохранили сценарий.</span><span class="sxs-lookup"><span data-stu-id="e3067-137">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="e3067-138">Запуск скрипта; Например:</span><span class="sxs-lookup"><span data-stu-id="e3067-138">Run the script; for example:</span></span>
    
    ```
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="e3067-139">При запросе учетных данных введите свой адрес электронной почты и пароль, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e3067-139">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="e3067-p108">Введите следующие сведения, когда запрашивается сценарий. Введите все данные и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="e3067-p108">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="e3067-142">Имя существующего поиска.</span><span class="sxs-lookup"><span data-stu-id="e3067-142">The name of the existing search.</span></span>
    
    - <span data-ttu-id="e3067-143">Имя нового поиска.</span><span class="sxs-lookup"><span data-stu-id="e3067-143">The name of the new search.</span></span>
    
    <span data-ttu-id="e3067-p109">Сценарий создает новый поиск контента, но не запускает его. Это дает возможность изменить и запустить поиск на следующем этапе. Свойства нового поиска можно просмотреть, выполнив командлет **Get-ComplianceSearch** или перейдя на страницу **Поиск контента** или **Обнаружение электронных** данных в центре безопасности &amp; и соответствия требованиям в зависимости от того, является ли новый поиск связан с обращением.</span><span class="sxs-lookup"><span data-stu-id="e3067-p109">The script creates the new Content Search, but doesn't start it. This gives you a chance to edit and run the search in the next step. You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the Security &amp; Compliance Center, depending on whether or not the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a><span data-ttu-id="e3067-147">Шаг 2: изменение и выполнение клонированного поиска в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="e3067-147">Step 2: Edit and run the cloned search in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="e3067-p110">После выполнения сценария для клонирования существующего поиска контента необходимо перейти в центр соответствия требованиям безопасности &amp; для изменения и запуска нового поиска. Как было сказано ранее, вы можете изменить поиск, изменив запрос поиска ключевых слов и добавив или удалив условия поиска. Более подробную информацию можно узнать в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="e3067-p110">After the you've run the script to clone an existing Content Search, the next step is to go to the Security &amp; Compliance Center to edit and run the new search. As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions. For more information, see:</span></span>
  
- [<span data-ttu-id="e3067-151">Поиск контента в Office 365</span><span class="sxs-lookup"><span data-stu-id="e3067-151">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="e3067-152">Запросы ключевых слов и условия поиска контента</span><span class="sxs-lookup"><span data-stu-id="e3067-152">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="e3067-153">варианты обнаружения электронных данных в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="e3067-153">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>](ediscovery-cases.md)
