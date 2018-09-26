---
title: Создание, составление отчета и удаление нескольких поисков контента
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: Узнайте, как для автоматизации задач поиска контента, таких как создание запросов на поиск и выполнения отчетов с помощью скриптов PowerShell в Office 365 безопасность &amp; центре соответствия требованиям.
ms.openlocfilehash: a32c003dfd9a27ea8c38b29b31001b612368bc4a
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038142"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a><span data-ttu-id="d160e-103">Создание, составление отчета и удаление нескольких поисков контента</span><span class="sxs-lookup"><span data-stu-id="d160e-103">Create, report on, and delete multiple Content Searches</span></span>

 <span data-ttu-id="d160e-p101">Быстрое создание и отчетности операций поиска обнаружения часто играет важную роль в обнаружении электронных данных и расследований при сведения о базовых данных и расширение и качество поиска. Для этого введите безопасности &amp; центре соответствия требованиям предоставляет набор командлетов Windows PowerShell для автоматизации задач занимать много времени поиска контента. Эти сценарии предоставляют быстрый и простой способ создания число операций поиска и затем запустите отчеты оценке результатов поиска, которые могут помочь вам определить количество обрабатываемых данных. Можно также использовать сценарии для создания разных версий выполняет сравнение полученных результатов, каждый из них создает. Эти сценарии может помочь быстро и эффективно определение и исключает, направленными ваши данные.</span><span class="sxs-lookup"><span data-stu-id="d160e-p101">Quickly creating and reporting discovery searches is often an important step in eDiscovery and investigations when you're trying to learn about the underlying data, and the richness and quality of your searches. To help you do this, the Security &amp; Compliance Center offers a set of Windows PowerShell cmdlets to automate time-consuming Content Search tasks. These scripts provide a quick and easy way to create a number of searches, and then run reports of the estimated search results that can help you determine the quantity of data in question. You can also use the scripts to create different versions of searches to compare the results each one produces. These scripts can help you to quickly and efficiently identify and cull your data.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="d160e-109">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="d160e-109">Before you begin</span></span>

- <span data-ttu-id="d160e-110">Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям для запуска сценариев, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="d160e-110">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the scripts that are described in this topic.</span></span> 
    
- <span data-ttu-id="d160e-111">Необходимо собрать список URL-адресов для OneDrive для бизнеса сайтов в вашей организации, которые можно добавлять в CSV-файл на шаге 1, перейдите в раздел [Create список всех расположений OneDrive в вашей организации](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span><span class="sxs-lookup"><span data-stu-id="d160e-111">To collect a list of the URLs for the OneDrive for Business sites in your organization that you can add to the CSV file in Step 1, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span></span> 
    
- <span data-ttu-id="d160e-p102">Не забудьте сохранить все файлы, созданные в этом разделе, чтобы ту же папку. Который будет упростить выполнение скриптов.</span><span class="sxs-lookup"><span data-stu-id="d160e-p102">Be sure to save all the files that you create in this topic to the same folder. That will make it easier to run the scripts.</span></span>
    
- <span data-ttu-id="d160e-p103">Сценарии содержат обработка минимальной ошибок. Их основной целью является быстро создавать, создание отчетов по и удаление несколько поисков содержимого.</span><span class="sxs-lookup"><span data-stu-id="d160e-p103">The scripts include minimal error handling. Their primary purpose is to quickly create, report on, and delete multiple Content Searches.</span></span>
    
- <span data-ttu-id="d160e-p104">Примеры скриптов, представленные в этой статье, не поддерживаются ни одной из стандартных программ поддержки или служб Майкрософт. Примеры скриптов предоставляются КАК ЕСТЬ и без каких-либо гарантий. Кроме того, корпорация Майкрософт не дает никаких обязательств в отношении подразумеваемых гарантий, в том числе гарантий товарного качества и пригодности для использования по назначению. Ответственность за риск, возникающий в результате выполнения примеров скриптов и использования документации, полностью возлагается на вас. Корпорация Майкрософт, ее авторы и все, кто принимает участие в создании, подготовке и публикации скриптов, не несут ответственности за какой-либо ущерб (в том числе потерю прибыли предприятия, приостановку его деятельности, потерю бизнес-данных и другой денежный ущерб), вызванный использованием или неспособностью использования примеров скриптов или документации, даже если корпорации Майкрософт было известно о возможности такого ущерба.</span><span class="sxs-lookup"><span data-stu-id="d160e-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a><span data-ttu-id="d160e-121">Шаг 1: Создание CSV-файл, содержащий сведения о поисковые запросы, чтобы запустить</span><span class="sxs-lookup"><span data-stu-id="d160e-121">Step 1: Create a CSV file that contains information about the searches you want to run</span></span>

<span data-ttu-id="d160e-p105">Файл значений, разделенных запятыми (CSV) запятыми, создаваемого на этом этапе содержит строку для каждого пользователя, который нужно найти. Можно выполнить поиск Exchange Online почтового ящика пользователя (к которым относятся архивного почтового ящика, если он включен) и их OneDrive для бизнеса сайта. Или можно выполнить поиск только что почтовый ящик или OneDrive для бизнеса сайта. Также можно выполнить поиск любого сайта в SharePoint Online организации. Скрипт, на котором запущен на шаге 3 будет создавать отдельные поиска для каждой строки в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="d160e-p105">The comma separated value (CSV) file that you create in this step contains a row for each user that want to search. You can search the user's Exchange Online mailbox (which includes the archive mailbox, if it's enabled) and their OneDrive for Business site. Or you can search just the mailbox or the OneDrive for Business site. You can also search any site in your SharePoint Online organization. The script that you run in Step 3 will create a separate search for each row in the CSV file.</span></span> 
  
1. <span data-ttu-id="d160e-p106">Скопируйте и вставьте следующий текст в txt-файл с помощью блокнота. Сохраните этот файл в папку на локальном компьютере. В эту папку, а также будет сохранять других сценариев.</span><span class="sxs-lookup"><span data-stu-id="d160e-p106">Copy and paste the following text into a .txt file using NotePad. Save this file to a folder on your local computer. You'll save the other scripts to this folder as well.</span></span>
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    <span data-ttu-id="d160e-p107">Первая строка или строка заголовка в файле перечислены параметры, которые будут использоваться для создания нового контента поисков командлетом **New-ComplianceSearch** (с помощью скрипта на шаге 3). Имя каждого параметра разделенных запятыми. Убедитесь в том, что все пробелы в строке заголовков. Каждая строка в строке заголовков представляет значения параметров для каждой операции поиска. Обязательно замените местозаполнители в CSV-файл с данными.</span><span class="sxs-lookup"><span data-stu-id="d160e-p107">The first row, or header row, of the file lists the parameters that will be used by **New-ComplianceSearch** cmdlet (in the script in Step 3) to create a new Content Searches. Each parameter name is separated by a comma. Make sure there aren't any spaces in the header row. Each row under the header row represents the parameter values for each search. Be sure to replace the placeholder data in the CSV file with your actual data.</span></span> 
    
2. <span data-ttu-id="d160e-135">Откройте файл .txt в Excel и затем использовать сведения в следующей таблице для редактирования файла с данными для каждой операции поиска.</span><span class="sxs-lookup"><span data-stu-id="d160e-135">Open the .txt file in Excel, and then use the information in the following table to edit the file with information for each search.</span></span> 
    
    |<span data-ttu-id="d160e-136">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="d160e-136">**Parameter**</span></span>|<span data-ttu-id="d160e-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d160e-137">**Description**</span></span>|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |<span data-ttu-id="d160e-138">SMTP-адрес почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="d160e-138">The SMTP address of the user's mailbox.</span></span>  <br/> |
    | `SharePointLocation` <br/> |<span data-ttu-id="d160e-p108">URL-адрес для пользователя OneDrive для бизнеса сайта или URL-адрес для любого сайта в вашей организации. Для URL-адреса для OneDrive для бизнеса сайтов, используйте следующий формат: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. Например `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span><span class="sxs-lookup"><span data-stu-id="d160e-p108">The URL for the user's OneDrive for Business site or the URL for any site in your organization. For the URL for OneDrive for Business sites, use this format: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. For example,  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.  </span></span><br/> |
    | `ContentMatchQuery` <br/> |<span data-ttu-id="d160e-p109">Запрос поиска для поиска. Дополнительные сведения о создании поискового запроса можно [запросах по ключевым словам и условия поиска для поиска контента](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="d160e-p109">The search query for the search. For more information about creating a search query, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).  </span></span><br/> |
    | `StartDate` <br/> |<span data-ttu-id="d160e-p110">Для электронной почты Дата, или после сообщения, получаемые получателя или отправленные отправителем. Для документов в SharePoint или OneDrive для бизнеса сайтов после документа или даты последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="d160e-p110">For email, the date on or after a message was received by a recipient or sent by the sender. For documents on SharePoint or OneDrive for Business sites, the date on or after a document was last modified.</span></span>  <br/> |
    | `EndDate` <br/> |<span data-ttu-id="d160e-p111">Для электронной почты, дату или до сообщение было отправлено отправленных пользователем. Для документов в SharePoint или OneDrive для бизнеса сайтов до документа или даты последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="d160e-p111">For email, the date on or before a message was sent by a sent by the user. For documents on SharePoint or OneDrive for Business sites, the date on or before a document was last modified.</span></span>  <br/> |
   
3. <span data-ttu-id="d160e-p112">Сохраните файл Excel как CSV-файл в папку на локальном компьютере. Сценарий, созданный на шаге 3 будет использовать сведения в этом CSV-файла для создания поисковые запросы.</span><span class="sxs-lookup"><span data-stu-id="d160e-p112">Save the Excel file as a CSV file to a folder on your local computer. The script that you create in Step 3 will use the information in this CSV file to create the searches.</span></span> 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a><span data-ttu-id="d160e-150">Шаг 2: Подключение к безопасности & PowerShell центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d160e-150">Step 2: Connect to Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="d160e-151">Следующим шагом является подключение Windows PowerShell для защиты &amp; центре соответствия требованиям для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="d160e-151">The next step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="d160e-p113">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `ConnectSCC.ps1`. Сохраните файл на ту же папку, который был сохранен CSV-файла для на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="d160e-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`. Save the file to the same folder that you saved the CSV file to in Step 1.</span></span>
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="d160e-154">На локальном компьютере откройте Windows PowerShell, перейдите к папке, где находится сценарий, созданный на предыдущем шаге и затем запустите сценарий; Например:</span><span class="sxs-lookup"><span data-stu-id="d160e-154">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a><span data-ttu-id="d160e-155">Шаг 3: Выполните скрипт, чтобы создавать и запускать поиск</span><span class="sxs-lookup"><span data-stu-id="d160e-155">Step 3: Run the script to create and start the searches</span></span>

<span data-ttu-id="d160e-p114">Скрипт на этом этапе создается отдельный поиска контента для каждой строки в CSV-файл, созданный на шаге 1. При выполнении этого скрипта будет выведен для двух значений:</span><span class="sxs-lookup"><span data-stu-id="d160e-p114">The script in this step will create a separate Content Search for each row in the CSV file that you created in Step 1. When you run this script, you'll be prompted for two values:</span></span>
  
- <span data-ttu-id="d160e-p115">**Идентификатор группы поиска** — это имя предоставляет простой способ организации поисковые запросы, создаваемые из CSV-файла. Каждой операции поиска, которая создается называется с Идентификатором группы поиска, а затем номер используется в качестве имени пользователя. Например при вводе **ContosoCase** идентификатор группы поиска нажмите поисковые запросы называются **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**и т. д. Обратите внимание на то, что имя, которое вводится с учетом регистра. При использовании идентификатор группы поиска в шаге 4 и 5 действие, необходимо использовать так же, как это делалось во время создания.</span><span class="sxs-lookup"><span data-stu-id="d160e-p115">**Search Group ID** - This name provides an easy way to organize the searches that are created from the CSV file. Each search that's created is named with the Search Group ID, and then a number is appended to the search name. For example, if you enter **ContosoCase** for the Search Group ID, then the searches are named **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**, and so on. Note that the name you type is case sensitive. When you use the Search Group ID in Step 4 and Step 5, you have to use the same case as you did when you created it.</span></span> 
    
- <span data-ttu-id="d160e-p116">**CSV-файла** — имя CSV-файл, созданный на шаге 1. Не забудьте включить использование полного имени файла, включают расширение файла .csv; например `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="d160e-p116">**CSV file** - The name of the CSV file that you created in Step 1. Be sure to include the use the full filename, include the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
<span data-ttu-id="d160e-165">Чтобы запустить сценарий, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="d160e-165">To run the script:</span></span>

1. <span data-ttu-id="d160e-p117">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `CreateSearches.ps1`. Сохраните файл на ту же папку, где был сохранен другие файлы.</span><span class="sxs-lookup"><span data-stu-id="d160e-p117">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CreateSearches.ps1`. Save the file to the same folder where you saved the other files.</span></span>
    
  ```
  # Get the Search Group ID and the location of the CSV input file
  $searchGroup = Read-Host 'Search Group ID'
  $csvFile = Read-Host 'Source CSV file'
    
  # Do a quick check to make sure our group name will not collide with other searches
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    $searchName = $searchGroup +'_' + $searchCounter
    $search = Get-ComplianceSearch $searchName -EA SilentlyContinue
    if ($search)
    {
        Write-Error "The Search Group ID conflicts with existing searches.  Please choose a search group name and restart the script."
        return
    }
    $searchCounter++
  }
    
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    # Create the query
    $query = $_.ContentMatchQuery
    if(($_.StartDate -or $_.EndDate))
    {
          # Add the appropriate date restrictions.  NOTE: Using the Date condition property here because it works across Exchange, SharePoint, and OneDrive for Business.
          # For Exchange, the Date condition property maps to the Sent and Received dates; for SharePoint and OneDrive for Business, it maps to Created and Modified dates.
          if($query)
          {
              $query += " AND"
          }
          $query += " ("
          if($_.StartDate)
          {
              $query += "Date >= " + $_.StartDate
          }
          if($_.EndDate)
          {
              if($_.StartDate)
              {
                  $query += " AND "
              }
              $query += "Date <= " + $_.EndDate
          }
          $query += ")"
    }
      
      # -ExchangeLocation can't be set to an empty string, set to null if there's no location.
      $exchangeLocation = $null
      if ( $_.ExchangeLocation)
      {
           $exchangeLocation = $_.ExchangeLocation
      }
    
    # Create and run the search        
    $searchName = $searchGroup +'_' + $searchCounter
    Write-Host "Creating and running search: " $searchName -NoNewline
    $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $exchangeLocation -SharePointLocation $_.SharePointLocation -ContentMatchQuery $query
    
    # Start and wait for each search to complete
    Start-ComplianceSearch $search.Name
    while ((Get-ComplianceSearch $search.Name).Status -ne "Completed")
    {
        Write-Host " ." -NoNewline
        Start-Sleep -s 3
    }
    Write-Host ""
    
    $searchCounter++
  }
  ```

2. <span data-ttu-id="d160e-168">В Windows PowerShell перейдите к папке, где скрипт сохранен в предыдущем шаге и запустите сценарии; Например:</span><span class="sxs-lookup"><span data-stu-id="d160e-168">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```
    .\CreateSearches.ps1
    ```

3. <span data-ttu-id="d160e-p118">В командной строке **Идентификатор группы поиска** введите имя группы поиска и затем нажмите клавишу **Ввод**. например `ContosoCase`. Имейте в виду, что это имя с учетом регистра, поэтому необходимо будет ввести его так же, как в последующих шагах.</span><span class="sxs-lookup"><span data-stu-id="d160e-p118">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example,  `ContosoCase`. Remember that this name is case sensitive, so you'll have to type it the same way in the subsequent steps.</span></span>
    
4. <span data-ttu-id="d160e-171">В командной строке **исходного CSV-файла** введите имя CSV-файла, включая расширение файла .csv; например `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="d160e-171">At the **Source CSV file** prompt, type the name of the CSV file, including the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
5. <span data-ttu-id="d160e-172">Нажмите клавишу **Ввод** , чтобы продолжить выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="d160e-172">Press **Enter** to continue running the script.</span></span> 
    
    <span data-ttu-id="d160e-p119">Сценарий отображается ход выполнения создания и выполнения операций поиска. По завершении сценария возвращается в командной строке.</span><span class="sxs-lookup"><span data-stu-id="d160e-p119">The script displays the progress of creating and running the searches. When the script is complete, it returns to the prompt.</span></span> 
    
    ![Пример результата выполнения сценария для создания нескольких запросов на поиск соответствий требованиям](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a><span data-ttu-id="d160e-176">Шаг 4: Запустите скрипт, чтобы сообщить о поиска оценки</span><span class="sxs-lookup"><span data-stu-id="d160e-176">Step 4: Run the script to report the search estimates</span></span>

<span data-ttu-id="d160e-p120">После создания поисковые запросы, следующим шагом является выполнение скрипта, который отображает простой отчет, содержащий число найденных элементов для каждой операции поиска, созданного на шаге 3. Отчет также включает в себя размера результатов для каждой операции поиска, а также общее число обращений и общий размер всех запросов поиска. При выполнении работы с отчетами сценарий, вы будете предложит идентификатор группы поиска и имя файла CSV Если вы хотите сохранить отчет в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="d160e-p120">After you create the searches, the next step is to run a script that displays a simple report of the number of search hits for each search that was created in Step 3. The report also includes the size of results for each search, and the total number of hits and total size of all searches. When you run the reporting script, you'll be prompted for the Search Group ID, and a CSV filename if you want to save the report to a CSV file.</span></span>
  
1. <span data-ttu-id="d160e-p121">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `SearchReport.ps1`. Сохраните файл на ту же папку, где был сохранен другие файлы.</span><span class="sxs-lookup"><span data-stu-id="d160e-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchReport.ps1`. Save the file to the same folder where you saved the other files.</span></span>
    
  ```
  $searchGroup = Read-Host 'Search Group ID'
  $outputFile = Read-Host 'Enter a file name or file path to save the report to a .csv file. Leave blank to only display the report'
  $searches = Get-ComplianceSearch | ?{$_.Name -clike $searchGroup + "_*"}
  $allSearchStats = @()
  foreach ($partialObj in $searches)
  {
      $search = Get-ComplianceSearch $partialObj.Name
      $sizeMB = [System.Math]::Round($search.Size / 1MB, 2)
      $searchStatus = $search.Status
      if($search.Errors)
      {
          $searchStatus = "Failed"
      }elseif($search.NumFailedSources -gt 0)
      {
          $searchStatus = "Failed Sources"
      }
      $searchStats = New-Object PSObject
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Name -Value $search.Name
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name ContentMatchQuery -Value $search.ContentMatchQuery
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Status -Value $searchStatus
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Items -Value $search.Items
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size" -Value $search.Size
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size(MB)" -Value $sizeMB
      $allSearchStats += $searchStats
  }
  # Calculate the totals
  $allItems = ($allSearchStats | Measure-Object Items -Sum).Sum
  # Convert the total size to MB and round to the nearst 100th
  $allSize = ($allSearchStats | Measure-Object 'Size' -Sum).Sum
  $allSizeMB = [System.Math]::Round($allSize  / 1MB, 2)
  # Get the total successful searches and total of all searches
  $allSuccessCount = ($allSearchStats |?{$_.Status -eq "Completed"}).Count
  $allCount = $allSearchStats.Count
  $allStatus = [string]$allSuccessCount + " of " + [string]$allCount
  # Totals Row
  $totalSearchStats = New-Object PSObject
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Name -Value "Total"
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Status -Value $allStatus
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Items -Value $allItems
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name "Size(MB)" -Value $allSizeMB
  $allSearchStats += $totalSearchStats
  # Just get the columns we're interested in showing
  $allSearchStatsPrime = $allSearchStats | Select-Object Name, Status, Items, "Size(MB)", ContentMatchQuery
  # Print the results to the screen
  $allSearchStatsPrime |ft -AutoSize -Wrap
  # Save the results to a CSV file
  if ($outputFile)
  {
      $allSearchStatsPrime | Export-Csv -Path $outputFile -NoTypeInformation
  }
  ```

2. <span data-ttu-id="d160e-182">В Windows PowerShell перейдите к папке, где скрипт сохранен в предыдущем шаге и запустите сценарии; Например:</span><span class="sxs-lookup"><span data-stu-id="d160e-182">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```
    .\SearchReport.ps1
    ```

3. <span data-ttu-id="d160e-p122">В командной строке **Идентификатор группы поиска** введите имя группы поиска и затем нажмите клавишу **Ввод**. например `ContosoCase`. Помните, что в этом имени учитывается регистр, поэтому необходимо будет ввести его так же, как это делалось при выполнении скрипта в шаге 3.</span><span class="sxs-lookup"><span data-stu-id="d160e-p122">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example  `ContosoCase`. Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
4. <span data-ttu-id="d160e-p123">В командной строке **путь к файлу для сохранения отчета в CSV-файл (не заполнять для только что отображения отчета)** введите имя файла (включая расширение файла .csv) пути полного имени файла, если вы хотите сохранить отчет в CSV-файл. Имя CSV-файла, включая расширение файла .csv. Например, можно ввести `ContosoCaseReport.csv` для сохранения в текущем каталоге или можно ввести `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` для сохранения в другую папку. Командной строке можно также оставить пустым, чтобы отобразить отчет, но не сохраните его в файл.</span><span class="sxs-lookup"><span data-stu-id="d160e-p123">At the **File path to save the report to a CSV file (leave blank to just display the report)** prompt, type a file name of complete filename path (including the .csv file extension) if you want to save the report to a CSV file. name of the CSV file, including the .csv file extension. For example, you could type  `ContosoCaseReport.csv` to save it to the current directory or you could type  `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` to save it to a different folder. You can also leave the prompt blank to display the report but not save it to a file.</span></span> 
    
5. <span data-ttu-id="d160e-189">Нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="d160e-189">Press **Enter**.</span></span>
    
    <span data-ttu-id="d160e-p124">Сценарий отображается ход выполнения создания и выполнения операций поиска. По завершении сценария отображается отчет.</span><span class="sxs-lookup"><span data-stu-id="d160e-p124">The script displays the progress of creating and running the searches. When the script is complete, the report is displayed.</span></span> 
    
    ![Выполнение отчета о поиске для просмотра результатов для группы поиска](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> <span data-ttu-id="d160e-p125">Если же почтового ящика или сайта указан как расположение содержимого в более одного поиска в группу поиска, общее результаты оценки в отчет (число элементов и общий размер) могут содержать результаты тех же элементов. Вот так как же сообщение электронной почты или документ будет учитываться более одного раза при совпадении запросов для разных операций поиска в группу поиска.</span><span class="sxs-lookup"><span data-stu-id="d160e-p125">If the same mailbox or site is specified as a content location in more than one search in a search group, the total results estimate in the report (for both the number of items and the total size) might include results for the same items. That's because the same email message or document will be counted more than once if it matches the query for different searches in the search group.</span></span> 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a><span data-ttu-id="d160e-195">Шаг 5: Выполните скрипт, чтобы удалить поисковые запросы</span><span class="sxs-lookup"><span data-stu-id="d160e-195">Step 5: Run the script to delete the searches</span></span>

<span data-ttu-id="d160e-p126">Так как они могут вызывать много операций поиска, этот сценарий только что упрощает Быстрое удаление поисковые запросы, созданной на шаге 3. Как и другие сценарии такой также необходимо будет ввести идентификатор группы поиска При выполнении этого скрипта все операции поиска с Идентификатором группы поиска в поле поиска имя будет удалена.</span><span class="sxs-lookup"><span data-stu-id="d160e-p126">Because you might be creating a lot of searches, this last script just makes it easy to quickly delete the searches you created in Step 3. Like the other scripts, this one also prompts you for the Search Group ID. All searches with the Search Group ID in the search name will be deleted when you run this script.</span></span> 
  
1. <span data-ttu-id="d160e-p127">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `DeleteSearches.ps1`. Сохраните файл на ту же папку, где был сохранен другие файлы.</span><span class="sxs-lookup"><span data-stu-id="d160e-p127">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `DeleteSearches.ps1`. Save the file to the same folder where you saved the other files.</span></span>
    
  ```
  # Delete all searches in a search group
  $searchGroup = Read-Host 'Search Group ID'
  Get-ComplianceSearch |
      ForEach-Object{
      # If the name matches the search group name pattern (case sensitive), delete the search
      if ($_.Name -cmatch $searchGroup + "_\d+")
      {
          Write-Host "Deleting search: " $_.Name
          Remove-ComplianceSearch $_.Name -Confirm:$false
      }
  }
  ```

2. <span data-ttu-id="d160e-201">В Windows PowerShell перейдите к папке, где скрипт сохранен в предыдущем шаге и запустите сценарии; Например:</span><span class="sxs-lookup"><span data-stu-id="d160e-201">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```
    .\DeleteSearches.ps1
    ```

3. <span data-ttu-id="d160e-p128">В командной строке **Идентификатор группы поиска** введите имя группы поиска для поиска, которые вы хотите удалить и затем нажмите клавишу **Ввод**. например `ContosoCase`. Помните, что в этом имени учитывается регистр, поэтому необходимо будет ввести его так же, как это делалось при выполнении скрипта в шаге 3.</span><span class="sxs-lookup"><span data-stu-id="d160e-p128">At the **Search Group ID** prompt, type a search group name for the searches that you want to delete, and then press **Enter**; for example,  `ContosoCase`. Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
    <span data-ttu-id="d160e-204">Сценарий отображает имя каждого поиска, который будет удален.</span><span class="sxs-lookup"><span data-stu-id="d160e-204">The script displays the name of each search that's deleted.</span></span>
    
    ![Выполните сценарий для удаления поисковых запросов в группе поиска](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
