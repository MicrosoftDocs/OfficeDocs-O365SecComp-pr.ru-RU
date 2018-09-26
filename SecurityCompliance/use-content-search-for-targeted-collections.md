---
title: Использование поиска контента в Office 365 для целевого семейства сайтов
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Использование поиска контента в Office 365 безопасность &amp; центре соответствия требованиям для выполнения целевого семейства сайтов. Целевой коллекции означает, что уверенности, реагировать на случай или привилегированной элементов, находятся в определенной папке почтового ящика или сайта. Получение идентификатор папки или путь для определенного почтового ящика или сайта папок, которые требуется выполнить поиск с помощью сценария в этой статье.
ms.openlocfilehash: bb808e38f24ebf09a975b3082ef1dc61bc6344c4
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038302"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a>Использование поиска контента в Office 365 для целевого семейства сайтов

Компонент поиска контента в Office 365 безопасность &amp; центре соответствия требованиям не дает прямое возможности в пользовательском Интерфейсе для конкретных папки поиска в почтовых ящиках Exchange или SharePoint и OneDrive для бизнеса сайтов. Тем не менее можно выполнить поиск определенных папок (называемых целевой коллекции), указав идентификатор папки или пути в синтаксисе запроса фактического поиска. С помощью поиска контента для выполнения целевой коллекции полезен в том случае, когда вы будете уверенно реагировать на случай или привилегированной элементов, находятся в определенной папке почтового ящика или сайта. Чтобы получить идентификатор папки для папок почтовых ящиков или путь для папок на сервере SharePoint и OneDrive для бизнеса сайта можно использовать сценарий в этой статье. Затем можно использовать идентификатор папки или путь в поисковый запрос возвращает элементы, расположенные в папке.
  
## <a name="before-you-begin"></a>Перед началом работы

- Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям для запуска сценария на шаге 1. Дополнительные сведения можно [назначать разрешения обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям](assign-ediscovery-permissions.md).
    
    Кроме того необходимо назначить роль получателей почты в организации Exchange Online. Это необходимо, чтобы запустить командлет **Get-MailboxFolderStatistics** , который включен в скрипт на шаге 1. По умолчанию роли получателей почты назначается группы ролей управления организацией и Recipient Management в Exchange Online. Дополнительные сведения о назначении разрешений в Exchange Online содержатся в разделе [Управление членов группы ролей](https://go.microsoft.com/fwlink/p/?linkid=692102). Может также создать пользовательскую группу ролей, назначить роли получателей почты и затем добавить участников, которым требуется для запуска сценария на шаге 1. Для получения дополнительных сведений см [роли](https://go.microsoft.com/fwlink/p/?linkid=730688).
    
- Каждый раз при запуске сценария на шаге 1, создается новый удаленный сеанс PowerShell. Таким образом можно использовать все удаленные PowerShell сеансы доступны. Чтобы предотвратить это, можно выполнить следующую команду для отключения активной удаленные сеансы PowerShell.
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    Дополнительные сведения можно [Подключить к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Сценарий включает в себя обработка минимальной ошибок. Основным назначением скрипт заключается в быстро Отображение списка папки почтового ящика идентификаторы или путей, которые можно использовать в синтаксисе запроса поиска контента поиска для выполнения целевого семейства веб-сайтов.
    
- Пример сценария, представленные в этом разделе не поддерживается в любой программе стандартной поддержки корпорации Майкрософт и службы. Образец сценария предоставляются как есть без какой-либо. Дополнительно корпорация Майкрософт не все подразумеваемых гарантий, включая, без ограничения, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности образец сценария и документация остается с вами. Событие не корпорации Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценариев несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать примеры сценариев или документации, даже если Microsoft поступали предупреждения о возможности такого ущерба.
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a>Шаг 1: Выполните скрипт, чтобы получить список папок для почтового ящика или сайта

Скрипт, которые выполняются на первом этапе возвращает список папок почтового ящика или SharePoint или OneDrive для бизнеса папок и соответствующий идентификатор папки или путь для каждой папки. При выполнении этого скрипта его запросит со следующими сведениями.
  
- **URL-адрес сайта или адрес электронной почты** Введите адрес электронной почты custodian, чтобы возвратить список папок почтовых ящиков Exchange и сложить идентификаторы. Или введите URL-адрес для сайта SharePoint или OneDrive для бизнеса сайта, чтобы возвратить список путей для указанного сайта. Вот несколько примеров: 
    
  - **Exchange** - stacig@contoso.onmicrosoft.com 
    
  - **SharePoint** - https://contoso.sharepoint.com/sites/marketing 
    
  - **OneDrive для бизнеса** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com 
    
- **Учетные данные пользователя** - скрипт будет использовать свои учетные данные для подключения к Exchange Online и безопасность &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell. Как объяснялось ранее необходимо назначить соответствующие разрешения для успешного запуска этого сценария.
    
В список папок почтового ящика и веб-сайтов путей:
  
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `GetFolderSearchParameters.ps1`.
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security &amp; Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the folder paths for the site. #
  #    * In both cases, the script supplies the correct search properties (folderid: or path:)      #
  #      appeneded to the folder ID or path ID to use in a Content Search.              #
  # Notes:                                              #
  #    * For SharePoint and OneDrive for Business, the paths are searched recursively; this means the   #
  #      the current folder and all sub-folders are searched.                       #
  #    * For Exchange, only the specified folder will be searched; this means sub-folders in the folder #
  #      will not be searched.  To search sub-folders, you need to use the specify the folder ID for    #
  #      each sub-folder that you want to search.                               #
  #    * For Exchange, only folders in the user's primary mailbox will be returned by the script.       #
  #########################################################################################################
  # Collect the target email address or SharePoint Url
  $addressOrSite = Read-Host "Enter an email address or a URL for a SharePoint or OneDrive for Business site"
  # Authenticate with Exchange Online and the Security &amp; Complaince Center (Exchange Online Protection - EOP)
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  if ($addressOrSite.IndexOf("@") -ige 0)
  {
      # List the folder Ids for the target mailbox
      $emailAddress = $addressOrSite
      # Authenticate with Exchange Online
      if (!$ExoSession)
      {
          $ExoSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid/ -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $ExoSession -AllowClobber -DisableNameChecking
      }
      $folderQueries = @()
      $folderStatistics = Get-MailboxFolderStatistics $emailAddress
      foreach ($folderStatistic in $folderStatistics)
      {
          $folderId = $folderStatistic.FolderId;
          $folderPath = $folderStatistic.FolderPath;
          $encoding= [System.Text.Encoding]::GetEncoding("us-ascii")
          $nibbler= $encoding.GetBytes("0123456789ABCDEF");
          $folderIdBytes = [Convert]::FromBase64String($folderId);
          $indexIdBytes = New-Object byte[] 48;
          $indexIdIdx=0;
          $folderIdBytes | select -skip 23 -First 24 | %{$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -shr 4];$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -band 0xF]}
          $folderQuery = "folderid:$($encoding.GetString($indexIdBytes))";
          $folderStat = New-Object PSObject
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderPath -Value $folderPath
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderQuery -Value $folderQuery
          $folderQueries += $folderStat
      }
      Write-Host "-----Exchange Folders-----"
      $folderQueries |ft
  }
  elseif ($addressOrSite.IndexOf("http") -ige 0)
  {
      $searchName = "SPFoldersSearch"
      $searchActionName = "SPFoldersSearch_Preview"
      # List the folders for the SharePoint or OneDrive for Business Site
      $siteUrl = $addressOrSite
      # Authenticate with the Security &amp; Complaince Center
      if (!$SccSession)
      {
          $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $SccSession -AllowClobber -DisableNameChecking
      }
      # Clean-up, if the the script was aborted, the search we created might not have been deleted.  Try to do so now.
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
      # Create a Content Search against the SharePoint Site or OneDrive for Business site and only search for folders; wait for the search to complete
      $complianceSearch = New-ComplianceSearch -Name $searchName -ContentMatchQuery "contenttype:folder" -SharePointLocation $siteUrl
      Start-ComplianceSearch $searchName
      do{
          Write-host "Waiting for search to complete..."
          Start-Sleep -s 5
          $complianceSearch = Get-ComplianceSearch $searchName
      }while ($complianceSearch.Status -ne 'Completed')
      if ($complianceSearch.Items -gt 0)
      {
          # Create a Complinace Search Action and wait for it to complete. The folders will be listed in the .Results parameter
          $complianceSearchAction = New-ComplianceSearchAction -SearchName $searchName -Preview
          do
          {
              Write-host "Waiting for search action to complete..."
              Start-Sleep -s 5
              $complianceSearchAction = Get-ComplianceSearchAction $searchActionName
          }while ($complianceSearchAction.Status -ne 'Completed')
          # Get the results and print out the folders
          $results = $complianceSearchAction.Results
          $matches = Select-String "Data Link:.+[,}]" -Input $results -AllMatches
          foreach ($match in $matches.Matches)
          {
              $rawUrl = $match.Value
              $rawUrl = $rawUrl -replace "Data Link: " -replace "," -replace "}"
              Write-Host "path:""$rawUrl"""
          }
      }
      else
      {
          Write-Host "No folders were found for $siteUrl"
      }
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
  }
  else
  {
      Write-Error "Couldn't recognize $addressOrSite as an email address or a site URL"
  }
  ```

2. На локальном компьютере откройте Windows PowerShell и перейдите к папке, в которой вы сохранили скрипт.
    
3. Выполнение скрипта; Например:
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. Введите сведения, будет предложено для.
    
    Сценарий отображает список папок почтового ящика или папки сайт для указанного пользователя. Сообщите это окно Открыть, чтобы скопировать имя идентификатора или пути папки и вставьте его в запрос поиска в шаге 2.
    
    > [!TIP]
    > Вместо отображения список папок, на экране компьютера, можно повторно прямой вывода скрипта в текстовый файл. Этот файл сохраняется в папку, где находится скрипта. Например, чтобы перенаправить вывод в текстовом файле сценарий, выполните следующую команду на шаге 3: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` затем можно скопировать идентификатор папки или путь из файла для использования в запросе поиска.
  
### <a name="script-output-for-mailbox-folders"></a>Выходные данные сценария для папок почтовых ящиков

Если они будут папки почтового ящика идентификаторы, сценарий подключается к Exchange Online с помощью удаленной оболочки PowerShell, запустивший командлет **Get-MailboxFolderStatisics** и затем отображает список папок, из указанного почтового ящика. Для каждой папки в почтовом ящике сценарий отображает имя папки в столбце **FolderPath** и идентификатор папки в столбце **FolderQuery** . Кроме того сценарий добавляет префикс **folderId** (по имени свойства почтового ящика) с идентификатором папки. Так как свойство **folderid** является свойством с возможностью поиска, используется `folderid:<folderid>` в поисковый запрос на шаге 2, чтобы найти эту папку. 
  
Ниже приведен пример выходных данных, возвращаемое скриптом для папок почтовых ящиков.
  
![Пример списка папок почтового ящика и папок идентификаторы, возвращаемое скриптом](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
В примере на шаге 2 показано запрос, используемый для поиска удаляет подпапку папки элементов для восстановления.
  
### <a name="script-output-for-site-folders"></a>Выходные данные сценария для папки сайта

Если они будут пути из SharePoint или OneDrive для бизнеса сайтов, сценарий подключается к безопасности &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell создает новый поиск контента, который выполняет поиск сайтов для папок, а затем отображает список папок находится в указанном узле. Сценарий отображается имя каждой папки и добавляет префикс **пути** (по имени свойства сайта) в URL-адрес папки. Так как свойство **path** является свойством с возможностью поиска, используется `path:<path>` в поисковый запрос на шаге 2, чтобы найти эту папку. 
  
Ниже приведен пример выходных данных, возвращаемое скриптом для папок сайта.
  
![Пример списка путей для сайтов папок, возвращаемое скриптом](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a>Шаг 2: Используйте идентификатор папки или путь для выполнения целевой коллекции

После выполнении сценария необходимо собрать список идентификаторов папок или пути для определенного пользователя, то вы переходите переход на безопасность &amp; центре соответствия требованиям и создать новый поиск контента для поиска указанной папки. Вы будете использовать `folderid:<folderid>` или `path:<path>` свойства в поисковый запрос, который настроен в поле ключевых слов поиска контента (или в качестве значения для параметра *ContentMatchQuery* , если использовать командлет **New-ComplianceSearch** ). Вы можете сочетать `folderid` или `path` свойство с другими параметрами поиска или условия поиска. Если указан только `folderid` или `path` свойство в запрос поиска будет возвращать все элементы, расположенные в указанной папке. 
  
> [!NOTE]
> С помощью `path` свойство для поиска OneDrive расположения не возвращают файлы мультимедиа, такие как файлы PNG, TIFF. или .wav, в результатах поиска. 
  
1. Перейдите по ссылке [https://protection.office.com](https://protection.office.com).
    
2. Войдите в Office 365 с помощью учетной записи и учетные данные, используемые для выполнения скрипта на шаге 1.
    
3. В левой области безопасности &amp; центре соответствия требованиям, нажмите кнопку **поиска &amp; расследования** \> **поиска контента**и нажмите кнопку **Создать** ![значком Добавить](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
4. На странице **Новый поиск** введите имя поиска контента. Это имя должно быть уникальным в пределах организации. 
    
5. В разделе, **выберите раздел "мне нравится" для поиска**, выполните одно из следующих значений, в зависимости от поиска почтовых ящиков или папка сайта:
    
    - Нажмите кнопку **выбрать определенных почтовых ящиков для поиска** , а затем добавьте этого почтового ящика, который указан при выполнении скрипта на шаге 1. 
    
      Или
    
    - Нажмите кнопку **выбрать определенных сайтов для поиска** для поиска и затем добавьте же URL-адрес сайта, который указан при выполнении скрипта на шаге 1. 
    
6. Нажмите кнопку **Далее**.
    
7. На странице **выберите "мне нравится" для поиска** в поле ключевое слово вставьте `folderid:<folderid>` или `path:<path>` значение, возвращенное сценарием на шаге 1. 
    
    Например, запрос на следующем снимке экрана выполняет поиск любого элемента во вложенной папке удаляет в папки элементов для восстановления (значение `folderid` свойства для вложенной папке удаляет — это показано на снимке экрана на шаге 1):
    
    ![Вставьте folderid или путь в поле ключевого слова поискового запроса](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. Нажмите кнопку **поиска** , чтобы начать поиск целевой коллекции. 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a>Примеры запросов поиска для целевого семейства сайтов

Вот несколько примеров использования `folderid` и `path` свойства в поисковый запрос для выполнения целевой коллекции. Обратите внимание на то, что заполнители используются для `folderid:<folderid>` и `path:<path>` для экономии места. 
  
- В этом примере выполняется поиск папки три разных почтовых ящиков. Можно использовать следующий синтаксис запроса для поиска скрытых папок в папки элементов для восстановления.
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- В этом примере производится поиск в папке почтового ящика для элементов, которые содержат точную фразу.
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- В этом примере выполняется поиск папки сайта (и все вложенные папки) документов, содержащих только буквы «Соглашение о неразглашении МЕЖДУ» в поле название.
    
  ```
  path:<path> AND filename:nda
  ```

- В этом примере выполняется поиск папки сайта (и все подпапки) для документов были изменены в интервал дат.
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a>Дополнительные сведения

Имейте в виду следующее при семейств сайтов с помощью скрипта в этой статье и для выполнения.
  
- Сценарий не удалять какие-либо папки из результатов. Указанные некоторые папки в результаты могут быть не включаемые (или возврата ноль элементов), так как они содержат сгенерированное системой содержимого.
    
- Этот сценарий возвращает только сведений о папке для основного почтового ящика пользователя. Он не возвращает сведения о папках в архивный почтовый ящик пользователя.
    
- При поиске папки почтовых ящиков, только в указанной папке (обозначенный его `folderid` свойство) будет осуществляться. Вложенные папки не будет искать. Чтобы выполнить поиск вложенных папок, которые необходимы для использования `folderid` для вложенных папок, который нужно найти. 
    
- При поиске папки сайта, папка (обозначенный его `path` свойство) и всех вложенных папок поиска. 
    
- Как было сказано ранее, нельзя использовать `path` свойство для поиска файлов мультимедиа, таких как PNG, TIFF. или WAV-файл, расположенный в OneDrive расположения. Используйте различные [Свойства сайта](keyword-queries-and-search-conditions.md#searchable-site-properties) для поиска файлов мультимедиа в папках OneDrive. 
