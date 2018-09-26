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
# <a name="create-report-on-and-delete-multiple-content-searches"></a>Создание, составление отчета и удаление нескольких поисков контента

 Быстрое создание и отчетности операций поиска обнаружения часто играет важную роль в обнаружении электронных данных и расследований при сведения о базовых данных и расширение и качество поиска. Для этого введите безопасности &amp; центре соответствия требованиям предоставляет набор командлетов Windows PowerShell для автоматизации задач занимать много времени поиска контента. Эти сценарии предоставляют быстрый и простой способ создания число операций поиска и затем запустите отчеты оценке результатов поиска, которые могут помочь вам определить количество обрабатываемых данных. Можно также использовать сценарии для создания разных версий выполняет сравнение полученных результатов, каждый из них создает. Эти сценарии может помочь быстро и эффективно определение и исключает, направленными ваши данные. 
  
## <a name="before-you-begin"></a>Перед началом работы

- Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям для запуска сценариев, описанных в этом разделе. 
    
- Необходимо собрать список URL-адресов для OneDrive для бизнеса сайтов в вашей организации, которые можно добавлять в CSV-файл на шаге 1, перейдите в раздел [Create список всех расположений OneDrive в вашей организации](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a). 
    
- Не забудьте сохранить все файлы, созданные в этом разделе, чтобы ту же папку. Который будет упростить выполнение скриптов.
    
- Сценарии содержат обработка минимальной ошибок. Их основной целью является быстро создавать, создание отчетов по и удаление несколько поисков содержимого.
    
- Примеры скриптов, представленные в этой статье, не поддерживаются ни одной из стандартных программ поддержки или служб Майкрософт. Примеры скриптов предоставляются КАК ЕСТЬ и без каких-либо гарантий. Кроме того, корпорация Майкрософт не дает никаких обязательств в отношении подразумеваемых гарантий, в том числе гарантий товарного качества и пригодности для использования по назначению. Ответственность за риск, возникающий в результате выполнения примеров скриптов и использования документации, полностью возлагается на вас. Корпорация Майкрософт, ее авторы и все, кто принимает участие в создании, подготовке и публикации скриптов, не несут ответственности за какой-либо ущерб (в том числе потерю прибыли предприятия, приостановку его деятельности, потерю бизнес-данных и другой денежный ущерб), вызванный использованием или неспособностью использования примеров скриптов или документации, даже если корпорации Майкрософт было известно о возможности такого ущерба.
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a>Шаг 1: Создание CSV-файл, содержащий сведения о поисковые запросы, чтобы запустить

Файл значений, разделенных запятыми (CSV) запятыми, создаваемого на этом этапе содержит строку для каждого пользователя, который нужно найти. Можно выполнить поиск Exchange Online почтового ящика пользователя (к которым относятся архивного почтового ящика, если он включен) и их OneDrive для бизнеса сайта. Или можно выполнить поиск только что почтовый ящик или OneDrive для бизнеса сайта. Также можно выполнить поиск любого сайта в SharePoint Online организации. Скрипт, на котором запущен на шаге 3 будет создавать отдельные поиска для каждой строки в CSV-файл. 
  
1. Скопируйте и вставьте следующий текст в txt-файл с помощью блокнота. Сохраните этот файл в папку на локальном компьютере. В эту папку, а также будет сохранять других сценариев.
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    Первая строка или строка заголовка в файле перечислены параметры, которые будут использоваться для создания нового контента поисков командлетом **New-ComplianceSearch** (с помощью скрипта на шаге 3). Имя каждого параметра разделенных запятыми. Убедитесь в том, что все пробелы в строке заголовков. Каждая строка в строке заголовков представляет значения параметров для каждой операции поиска. Обязательно замените местозаполнители в CSV-файл с данными. 
    
2. Откройте файл .txt в Excel и затем использовать сведения в следующей таблице для редактирования файла с данными для каждой операции поиска. 
    
    |**Параметр**|**Описание**|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |SMTP-адрес почтового ящика пользователя.  <br/> |
    | `SharePointLocation` <br/> |URL-адрес для пользователя OneDrive для бизнеса сайта или URL-адрес для любого сайта в вашей организации. Для URL-адреса для OneDrive для бизнеса сайтов, используйте следующий формат: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. Например `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.<br/> |
    | `ContentMatchQuery` <br/> |Запрос поиска для поиска. Дополнительные сведения о создании поискового запроса можно [запросах по ключевым словам и условия поиска для поиска контента](keyword-queries-and-search-conditions.md).<br/> |
    | `StartDate` <br/> |Для электронной почты Дата, или после сообщения, получаемые получателя или отправленные отправителем. Для документов в SharePoint или OneDrive для бизнеса сайтов после документа или даты последнего изменения.  <br/> |
    | `EndDate` <br/> |Для электронной почты, дату или до сообщение было отправлено отправленных пользователем. Для документов в SharePoint или OneDrive для бизнеса сайтов до документа или даты последнего изменения.  <br/> |
   
3. Сохраните файл Excel как CSV-файл в папку на локальном компьютере. Сценарий, созданный на шаге 3 будет использовать сведения в этом CSV-файла для создания поисковые запросы. 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Шаг 2: Подключение к безопасности & PowerShell центре соответствия требованиям

Следующим шагом является подключение Windows PowerShell для защиты &amp; центре соответствия требованиям для вашей организации.
  
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `ConnectSCC.ps1`. Сохраните файл на ту же папку, который был сохранен CSV-файла для на шаге 1.
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. На локальном компьютере откройте Windows PowerShell, перейдите к папке, где находится сценарий, созданный на предыдущем шаге и затем запустите сценарий; Например:
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a>Шаг 3: Выполните скрипт, чтобы создавать и запускать поиск

Скрипт на этом этапе создается отдельный поиска контента для каждой строки в CSV-файл, созданный на шаге 1. При выполнении этого скрипта будет выведен для двух значений:
  
- **Идентификатор группы поиска** — это имя предоставляет простой способ организации поисковые запросы, создаваемые из CSV-файла. Каждой операции поиска, которая создается называется с Идентификатором группы поиска, а затем номер используется в качестве имени пользователя. Например при вводе **ContosoCase** идентификатор группы поиска нажмите поисковые запросы называются **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**и т. д. Обратите внимание на то, что имя, которое вводится с учетом регистра. При использовании идентификатор группы поиска в шаге 4 и 5 действие, необходимо использовать так же, как это делалось во время создания. 
    
- **CSV-файла** — имя CSV-файл, созданный на шаге 1. Не забудьте включить использование полного имени файла, включают расширение файла .csv; например `ContosoCase.csv`.
    
Чтобы запустить сценарий, сделайте следующее:

1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `CreateSearches.ps1`. Сохраните файл на ту же папку, где был сохранен другие файлы.
    
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

2. В Windows PowerShell перейдите к папке, где скрипт сохранен в предыдущем шаге и запустите сценарии; Например:
    
    ```
    .\CreateSearches.ps1
    ```

3. В командной строке **Идентификатор группы поиска** введите имя группы поиска и затем нажмите клавишу **Ввод**. например `ContosoCase`. Имейте в виду, что это имя с учетом регистра, поэтому необходимо будет ввести его так же, как в последующих шагах.
    
4. В командной строке **исходного CSV-файла** введите имя CSV-файла, включая расширение файла .csv; например `ContosoCase.csv`.
    
5. Нажмите клавишу **Ввод** , чтобы продолжить выполнение сценария. 
    
    Сценарий отображается ход выполнения создания и выполнения операций поиска. По завершении сценария возвращается в командной строке. 
    
    ![Пример результата выполнения сценария для создания нескольких запросов на поиск соответствий требованиям](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a>Шаг 4: Запустите скрипт, чтобы сообщить о поиска оценки

После создания поисковые запросы, следующим шагом является выполнение скрипта, который отображает простой отчет, содержащий число найденных элементов для каждой операции поиска, созданного на шаге 3. Отчет также включает в себя размера результатов для каждой операции поиска, а также общее число обращений и общий размер всех запросов поиска. При выполнении работы с отчетами сценарий, вы будете предложит идентификатор группы поиска и имя файла CSV Если вы хотите сохранить отчет в CSV-файл.
  
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `SearchReport.ps1`. Сохраните файл на ту же папку, где был сохранен другие файлы.
    
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

2. В Windows PowerShell перейдите к папке, где скрипт сохранен в предыдущем шаге и запустите сценарии; Например:
    
    ```
    .\SearchReport.ps1
    ```

3. В командной строке **Идентификатор группы поиска** введите имя группы поиска и затем нажмите клавишу **Ввод**. например `ContosoCase`. Помните, что в этом имени учитывается регистр, поэтому необходимо будет ввести его так же, как это делалось при выполнении скрипта в шаге 3.
    
4. В командной строке **путь к файлу для сохранения отчета в CSV-файл (не заполнять для только что отображения отчета)** введите имя файла (включая расширение файла .csv) пути полного имени файла, если вы хотите сохранить отчет в CSV-файл. Имя CSV-файла, включая расширение файла .csv. Например, можно ввести `ContosoCaseReport.csv` для сохранения в текущем каталоге или можно ввести `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` для сохранения в другую папку. Командной строке можно также оставить пустым, чтобы отобразить отчет, но не сохраните его в файл. 
    
5. Нажмите клавишу **Ввод**.
    
    Сценарий отображается ход выполнения создания и выполнения операций поиска. По завершении сценария отображается отчет. 
    
    ![Выполнение отчета о поиске для просмотра результатов для группы поиска](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> Если же почтового ящика или сайта указан как расположение содержимого в более одного поиска в группу поиска, общее результаты оценки в отчет (число элементов и общий размер) могут содержать результаты тех же элементов. Вот так как же сообщение электронной почты или документ будет учитываться более одного раза при совпадении запросов для разных операций поиска в группу поиска. 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a>Шаг 5: Выполните скрипт, чтобы удалить поисковые запросы

Так как они могут вызывать много операций поиска, этот сценарий только что упрощает Быстрое удаление поисковые запросы, созданной на шаге 3. Как и другие сценарии такой также необходимо будет ввести идентификатор группы поиска При выполнении этого скрипта все операции поиска с Идентификатором группы поиска в поле поиска имя будет удалена. 
  
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `DeleteSearches.ps1`. Сохраните файл на ту же папку, где был сохранен другие файлы.
    
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

2. В Windows PowerShell перейдите к папке, где скрипт сохранен в предыдущем шаге и запустите сценарии; Например:
    
    ```
    .\DeleteSearches.ps1
    ```

3. В командной строке **Идентификатор группы поиска** введите имя группы поиска для поиска, которые вы хотите удалить и затем нажмите клавишу **Ввод**. например `ContosoCase`. Помните, что в этом имени учитывается регистр, поэтому необходимо будет ввести его так же, как это делалось при выполнении скрипта в шаге 3.
    
    Сценарий отображает имя каждого поиска, который будет удален.
    
    ![Выполните сценарий для удаления поисковых запросов в группе поиска](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
