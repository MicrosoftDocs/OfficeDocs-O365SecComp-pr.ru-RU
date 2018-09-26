---
title: Клонирование поиска контента безопасности Office 365 &amp; центре соответствия требованиям
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Быстро клонирование существующего контента поиска в системы с помощью сценария Windows PowerShell в данной статье &amp; Compliane центр поиска. При клонировании поиска, создается новый поиск (с новым именем), содержащий те же свойства, как исходного поиска. Затем можно изменить нового поиска (с помощью изменения запроса ключевого слова или диапазон дат) и запустите его.
ms.openlocfilehash: fd2ea0d8fa812d23e7479b664b13c786a62d5a38
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038052"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="30329-105">Клонирование поиска контента безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="30329-105">Clone a Content Search in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="30329-p102">Создание контента поиска в Office 365 безопасность &amp; центре соответствия требованиям, которая выполняет поиск много почтовых ящиков или на сервере SharePoint и OneDrive для бизнеса сайтов может занять некоторое время. Определение сайтов для поиска также может быть может привести к ошибкам при вводе URL-адреса. Чтобы избежать этих проблем, можно использовать сценарий Windows PowerShell в данной статье следует быстро скопировать существующий поиск контента. При клонировании поиска, создается новый поиск (с другим именем), содержащий те же свойства (например, расположения контента и запросов поиска), как исходного поиска. Затем можно редактировать новый поиск (с помощью изменения запроса ключевого слова или диапазон дат) и запустите его.</span><span class="sxs-lookup"><span data-stu-id="30329-p102">Creating a Content Search in Office 365 Security &amp; Compliance Center that searches a lot of mailboxes or SharePoint and OneDrive for Business sites can take awhile. Specifying the sites to search can also be prone to errors if you mistype a URL. To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search. When a you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search. Then you can edit the new search (by changing the keyword query or the date range) and run it.</span></span>
  
<span data-ttu-id="30329-111">Почему клонирование контента поиска?</span><span class="sxs-lookup"><span data-stu-id="30329-111">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="30329-112">Сравнение полученных результатов различных ключевых слов запросов поиска выполните на одном размещения содержимого.</span><span class="sxs-lookup"><span data-stu-id="30329-112">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="30329-113">Чтобы избежать повторного ввода большое число размещения содержимого при создании нового поиска.</span><span class="sxs-lookup"><span data-stu-id="30329-113">To save you from having to re-enter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="30329-114">Уменьшение размера результатов поиска; Например при наличии поиска, которое возвращает слишком много результатов для экспорта, можно клонирование поиска и добавить условие поиска, на основе диапазона дат, чтобы уменьшить количество результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="30329-114">To decrease the size of the search results; for example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="30329-115">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="30329-115">Before you begin</span></span>

- <span data-ttu-id="30329-116">Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям для запуска сценария, описанного в данном разделе.</span><span class="sxs-lookup"><span data-stu-id="30329-116">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="30329-p103">Сценарий включает в себя обработка минимальной ошибок. Основным назначением сценарий — это быстро клонирование поиска контента.</span><span class="sxs-lookup"><span data-stu-id="30329-p103">The script includes minimal error handling. The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="30329-119">Сценарий создает новый поиск контента, но не запустите ее.</span><span class="sxs-lookup"><span data-stu-id="30329-119">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="30329-p104">Этот сценарий учитывает ли поиск контента копируемого связан с вариантом eDiscovery. Если поиск связан с дела, новый поиск также будет связан с того же регистра. Если существующий поиск, не сопоставленный с дела, новый поиск отображаются на странице **поиска контента** в безопасности &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="30329-p104">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case. If the search is associated with a case, the new search will also be associated with the same case. If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="30329-p105">Пример сценария, представленные в этом разделе не поддерживается в любой программе стандартной поддержки корпорации Майкрософт и службы. Образец сценария предоставляются как есть без какой-либо. Дополнительно корпорация Майкрософт не все подразумеваемых гарантий, включая, без ограничения, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности образец сценария и документация остается с вами. Событие не корпорации Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценариев несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать примеры сценариев или документации, даже если Microsoft поступали предупреждения о возможности такого ущерба.</span><span class="sxs-lookup"><span data-stu-id="30329-p105">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="30329-128">Шаг 1: Выполните скрипт, чтобы скопировать поиска</span><span class="sxs-lookup"><span data-stu-id="30329-128">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="30329-p106">Скрипт на этом этапе будет создан новый поиск контента путем копирования существующей. При выполнении этого скрипта появится следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="30329-p106">The script in this step will create a new Content Search by cloning an existing one. When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="30329-p107">**Учетные данные пользователя** - скрипт будет использовать свои учетные данные для подключения к безопасности &amp; центре соответствия требованиям для своей организации Office 365 с помощью Windows PowerShell. Как уже указано, необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям для выполнения скрипта.</span><span class="sxs-lookup"><span data-stu-id="30329-p107">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center for your Office 365 organization with Windows PowerShell. As previously stated, you have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script.</span></span> 
    
- <span data-ttu-id="30329-133">**Имя существующего поиска** — это поиска контента, которую требуется скопировать.</span><span class="sxs-lookup"><span data-stu-id="30329-133">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="30329-134">**Имя нового поиска, который будет создан** - Если оставить это значение пустым, скрипт будет Создайте имя для нового поиска, который создается на основе имени поиска копируемого.</span><span class="sxs-lookup"><span data-stu-id="30329-134">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="30329-135">Следует скопировать поиска:</span><span class="sxs-lookup"><span data-stu-id="30329-135">To clone a search:</span></span>
  
1. <span data-ttu-id="30329-136">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `CloneSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="30329-136">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="30329-137">Откройте Windows PowerShell и перейдите к папке, в которой вы сохранили скрипт.</span><span class="sxs-lookup"><span data-stu-id="30329-137">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="30329-138">Выполнение скрипта; Например:</span><span class="sxs-lookup"><span data-stu-id="30329-138">Run the script; for example:</span></span>
    
    ```
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="30329-139">Когда требуется ввести учетные данные, введите адрес электронной почты и пароль и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="30329-139">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="30329-p108">Введите следующую информацию в ответ на запрос с помощью сценария. Введите каждый блок данных и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="30329-p108">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="30329-142">Имя существующего поиска.</span><span class="sxs-lookup"><span data-stu-id="30329-142">The name of the existing search.</span></span>
    
    - <span data-ttu-id="30329-143">Имя нового поиска.</span><span class="sxs-lookup"><span data-stu-id="30329-143">The name of the new search.</span></span>
    
    <span data-ttu-id="30329-p109">Сценарий создает новый поиск контента, но не запустите ее. Это дает возможность изменить и выполните поиск на следующем шаге. Свойства нового поиска можно просмотреть с помощью командлета **Get-ComplianceSearch** или, перейдя на страницу **контента поиска** или **обнаружения электронных данных** в системы &amp; центре соответствия требованиям, в зависимости от того, является ли новый поиск связанные с дела.</span><span class="sxs-lookup"><span data-stu-id="30329-p109">The script creates the new Content Search, but doesn't start it. This gives you a chance to edit and run the search in the next step. You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the Security &amp; Compliance Center, depending on whether or not the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a><span data-ttu-id="30329-147">Шаг 2: Изменение и выполнение клонирования поиска в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="30329-147">Step 2: Edit and run the cloned search in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="30329-p110">После запуска сценария следует скопировать существующего контента поиска вы следующим шагом является переход на безопасность &amp; центре соответствия требованиям для редактирования и запустите новый поиск. Как уже указано, можно изменить поиска, изменив запрос поиска ключевого слова и добавление или удаление условия поиска. Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="30329-p110">After the you've run the script to clone an existing Content Search, the next step is to go to the Security &amp; Compliance Center to edit and run the new search. As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions. For more information, see:</span></span>
  
- [<span data-ttu-id="30329-151">Поиск контента в Office 365</span><span class="sxs-lookup"><span data-stu-id="30329-151">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="30329-152">Запросы ключевых слов и условия поиска контента</span><span class="sxs-lookup"><span data-stu-id="30329-152">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="30329-153">вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="30329-153">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>](ediscovery-cases.md)
