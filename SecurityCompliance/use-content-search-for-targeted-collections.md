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
search.appverid:
- MOE150
- MET150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Использование поиска контента в Office 365 безопасность &amp; центре соответствия требованиям для выполнения целевого семейства сайтов. Целевой коллекции означает, что уверенности, реагировать на случай или привилегированной элементов, находятся в определенной папке почтового ящика или сайта. Получение идентификатор папки или путь для определенного почтового ящика или сайта папок, которые требуется выполнить поиск с помощью сценария в этой статье.
ms.openlocfilehash: 3ff0ca00915bce53e9e932316c5ab47884f346b2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534370"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a><span data-ttu-id="9cb3a-105">Использование поиска контента в Office 365 для целевого семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="9cb3a-105">Use Content Search in Office 365 for targeted collections</span></span>

<span data-ttu-id="9cb3a-p102">Компонент поиска контента в Office 365 безопасность &amp; центре соответствия требованиям не дает прямое возможности в пользовательском Интерфейсе для конкретных папки поиска в почтовых ящиках Exchange или SharePoint и OneDrive для бизнеса сайтов. Тем не менее можно выполнить поиск определенных папок (называемых целевой коллекции), указав идентификатор папки или пути в синтаксисе запроса фактического поиска. С помощью поиска контента для выполнения целевой коллекции полезен в том случае, когда вы будете уверенно реагировать на случай или привилегированной элементов, находятся в определенной папке почтового ящика или сайта. Чтобы получить идентификатор папки для папок почтовых ящиков или путь для папок на сервере SharePoint и OneDrive для бизнеса сайта можно использовать сценарий в этой статье. Затем можно использовать идентификатор папки или путь в поисковый запрос возвращает элементы, расположенные в папке.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p102">The Content Search feature in the Office 365 Security &amp; Compliance Center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites. However, it is possible to search specific folders (called a targeted collection) by specifying the folder ID or path in the actual search query syntax. Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder. You can use the script in this article to obtain the folder ID for mailbox folders or the path for folders on a SharePoint and OneDrive for Business site. Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="9cb3a-111">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="9cb3a-111">Before you begin</span></span>

- <span data-ttu-id="9cb3a-p103">Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям для запуска сценария на шаге 1. Дополнительные сведения можно [назначать разрешения обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script in Step 1. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
    <span data-ttu-id="9cb3a-p104">Кроме того необходимо назначить роль получателей почты в организации Exchange Online. Это необходимо, чтобы запустить командлет **Get-MailboxFolderStatistics** , который включен в скрипт на шаге 1. По умолчанию роли получателей почты назначается группы ролей управления организацией и Recipient Management в Exchange Online. Дополнительные сведения о назначении разрешений в Exchange Online содержатся в разделе [Управление членов группы ролей](https://go.microsoft.com/fwlink/p/?linkid=692102). Может также создать пользовательскую группу ролей, назначить роли получателей почты и затем добавить участников, которым требуется для запуска сценария на шаге 1. Для получения дополнительных сведений см [роли](https://go.microsoft.com/fwlink/p/?linkid=730688).</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p104">Additionally, you have to be assigned the Mail Recipients role in your Exchange Online organization. This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script in Step 1. By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online. For more information about assigning permissions in Exchange Online, see [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102). You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1. For more information, see [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span></span>
    
- <span data-ttu-id="9cb3a-p105">Каждый раз при запуске сценария на шаге 1, создается новый удаленный сеанс PowerShell. Таким образом можно использовать все удаленные PowerShell сеансы доступны. Чтобы предотвратить это, можно выполнить следующую команду для отключения активной удаленные сеансы PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p105">Each time you run the script in Step 1, a new remote PowerShell session is created. So you could use up all the remote PowerShell sessions available to you. To prevent this from happening, you can run the following command to disconnect your active remote PowerShell sessions.</span></span>
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="9cb3a-123">Дополнительные сведения можно [Подключить к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="9cb3a-123">For more information, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="9cb3a-p106">Сценарий включает в себя обработка минимальной ошибок. Основным назначением скрипт заключается в быстро Отображение списка папки почтового ящика идентификаторы или путей, которые можно использовать в синтаксисе запроса поиска контента поиска для выполнения целевого семейства веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p106">The script includes minimal error handling. The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>
    
- <span data-ttu-id="9cb3a-p107">Пример сценария, представленные в этом разделе не поддерживается в любой программе стандартной поддержки корпорации Майкрософт и службы. Образец сценария предоставляются как есть без какой-либо. Дополнительно корпорация Майкрософт не все подразумеваемых гарантий, включая, без ограничения, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности образец сценария и документация остается с вами. Событие не корпорации Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценариев несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать примеры сценариев или документации, даже если Microsoft поступали предупреждения о возможности такого ущерба.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p107">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="9cb3a-131">Шаг 1: Выполните скрипт, чтобы получить список папок для почтового ящика или сайта</span><span class="sxs-lookup"><span data-stu-id="9cb3a-131">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="9cb3a-p108">Скрипт, которые выполняются на первом этапе возвращает список папок почтового ящика или SharePoint или OneDrive для бизнеса папок и соответствующий идентификатор папки или путь для каждой папки. При выполнении этого скрипта его запросит со следующими сведениями.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p108">The script that you run in this first step will return a list of mailbox folders or SharePoint or OneDrive for Business folders, and the corresponding folder ID or path for each folder. When you run this script, it will prompt you for the following information.</span></span>
  
- <span data-ttu-id="9cb3a-p109">**URL-адрес сайта или адрес электронной почты** Введите адрес электронной почты custodian, чтобы возвратить список папок почтовых ящиков Exchange и сложить идентификаторы. Или введите URL-адрес для сайта SharePoint или OneDrive для бизнеса сайта, чтобы возвратить список путей для указанного сайта. Вот несколько примеров:</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p109">**Email address or site URL** Type an email address of the custodian to return a list of Exchange mailbox folders and fold IDs. Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site. Here are some examples:</span></span> 
    
  - <span data-ttu-id="9cb3a-137">**Exchange** - stacig@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="9cb3a-137">**Exchange** - stacig@contoso.onmicrosoft.com</span></span> 
    
  - <span data-ttu-id="9cb3a-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="9cb3a-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span></span> 
    
  - <span data-ttu-id="9cb3a-139">**OneDrive для бизнеса** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="9cb3a-139">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span> 
    
- <span data-ttu-id="9cb3a-p110">**Учетные данные пользователя** - скрипт будет использовать свои учетные данные для подключения к Exchange Online и безопасность &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell. Как объяснялось ранее необходимо назначить соответствующие разрешения для успешного запуска этого сценария.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p110">**Your user credentials** - The script will use your credentials to connect to Exchange Online and the Security &amp; Compliance Center with remote PowerShell. As previously explained, you have to assigned the appropriate permissions to successfully run this script.</span></span>
    
<span data-ttu-id="9cb3a-142">В список папок почтового ящика и веб-сайтов путей:</span><span class="sxs-lookup"><span data-stu-id="9cb3a-142">To display a list of mailbox folders or site path names:</span></span>
  
1. <span data-ttu-id="9cb3a-143">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `GetFolderSearchParameters.ps1`.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-143">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>
    
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

2. <span data-ttu-id="9cb3a-144">На локальном компьютере откройте Windows PowerShell и перейдите к папке, в которой вы сохранили скрипт.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-144">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="9cb3a-145">Выполнение скрипта; Например:</span><span class="sxs-lookup"><span data-stu-id="9cb3a-145">Run the script; for example:</span></span>
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. <span data-ttu-id="9cb3a-146">Введите сведения, будет предложено для.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-146">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="9cb3a-p111">Сценарий отображает список папок почтового ящика или папки сайт для указанного пользователя. Сообщите это окно Открыть, чтобы скопировать имя идентификатора или пути папки и вставьте его в запрос поиска в шаге 2.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p111">The script displays a list of mailbox folders or site folder for the specified user. Let this window open so that you can copy a folder ID or path name and paste it in to a search query in Step 2.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="9cb3a-p112">Вместо отображения список папок, на экране компьютера, можно повторно прямой вывода скрипта в текстовый файл. Этот файл сохраняется в папку, где находится скрипта. Например, чтобы перенаправить вывод в текстовом файле сценарий, выполните следующую команду на шаге 3: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` затем можно скопировать идентификатор папки или путь из файла для использования в запросе поиска.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p112">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file. This file will be saved to the folder where the script is located. For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or path from the file to use in a search query.</span></span>
  
### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="9cb3a-152">Выходные данные сценария для папок почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="9cb3a-152">Script output for mailbox folders</span></span>

<span data-ttu-id="9cb3a-p113">Если они будут папки почтового ящика идентификаторы, сценарий подключается к Exchange Online с помощью удаленной оболочки PowerShell, запустивший командлет **Get-MailboxFolderStatisics** и затем отображает список папок, из указанного почтового ящика. Для каждой папки в почтовом ящике сценарий отображает имя папки в столбце **FolderPath** и идентификатор папки в столбце **FolderQuery** . Кроме того сценарий добавляет префикс **folderId** (по имени свойства почтового ящика) с идентификатором папки. Так как свойство **folderid** является свойством с возможностью поиска, используется `folderid:<folderid>` в поисковый запрос на шаге 2, чтобы найти эту папку.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p113">If you're getting mailbox folder IDs, the script connects to Exchange Online by using remote PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox. For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column. Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID. Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="9cb3a-157">Ниже приведен пример выходных данных, возвращаемое скриптом для папок почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-157">Here's an example of the output returned by the script for mailbox folders.</span></span>
  
![Пример списка папок почтового ящика и папок идентификаторы, возвращаемое скриптом](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
<span data-ttu-id="9cb3a-159">В примере на шаге 2 показано запрос, используемый для поиска удаляет подпапку папки элементов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-159">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>
  
### <a name="script-output-for-site-folders"></a><span data-ttu-id="9cb3a-160">Выходные данные сценария для папки сайта</span><span class="sxs-lookup"><span data-stu-id="9cb3a-160">Script output for site folders</span></span>

<span data-ttu-id="9cb3a-p114">Если они будут пути из SharePoint или OneDrive для бизнеса сайтов, сценарий подключается к безопасности &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell создает новый поиск контента, который выполняет поиск сайтов для папок, а затем отображает список папок находится в указанном узле. Сценарий отображается имя каждой папки и добавляет префикс **пути** (по имени свойства сайта) в URL-адрес папки. Так как свойство **path** является свойством с возможностью поиска, используется `path:<path>` в поисковый запрос на шаге 2, чтобы найти эту папку.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p114">If you're getting paths from SharePoint or OneDrive for Business sites, the script connects to the Security &amp; Compliance Center using remote PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site. The script displays the name of each folder and adds the prefix of **path** (which is the name of the site property) to the folder URL. Because the **path** property is a searchable property, you'll use  `path:<path>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="9cb3a-164">Ниже приведен пример выходных данных, возвращаемое скриптом для папок сайта.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-164">Here's an example of the output returned by the script for site folders.</span></span>
  
![Пример списка путей для сайтов папок, возвращаемое скриптом](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a><span data-ttu-id="9cb3a-166">Шаг 2: Используйте идентификатор папки или путь для выполнения целевой коллекции</span><span class="sxs-lookup"><span data-stu-id="9cb3a-166">Step 2: Use a folder ID or path to perform a targeted collection</span></span>

<span data-ttu-id="9cb3a-p115">После выполнении сценария необходимо собрать список идентификаторов папок или пути для определенного пользователя, то вы переходите переход на безопасность &amp; центре соответствия требованиям и создать новый поиск контента для поиска указанной папки. Вы будете использовать `folderid:<folderid>` или `path:<path>` свойства в поисковый запрос, который настроен в поле ключевых слов поиска контента (или в качестве значения для параметра *ContentMatchQuery* , если использовать командлет **New-ComplianceSearch** ). Вы можете сочетать `folderid` или `path` свойство с другими параметрами поиска или условия поиска. Если указан только `folderid` или `path` свойство в запрос поиска будет возвращать все элементы, расположенные в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p115">After you've run the script to collect a list of folder IDs or paths for a specific user, the next step to go to the Security &amp; Compliance Center and create a new Content Search to search a specific folder. You'll use the  `folderid:<folderid>` or  `path:<path>` property in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet). You can combine the  `folderid` or  `path` property with other search parameters or search conditions. If you only include the  `folderid` or  `path` property in the query, the search will return all items located in the specified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9cb3a-171">С помощью `path` свойство для поиска OneDrive расположения не возвращают файлы мультимедиа, такие как файлы PNG, TIFF. или .wav, в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-171">Using the  `path` property to search OneDrive locations won't return media files, such as .png, .tiff, or .wav files, in the search results.</span></span> 
  
1. <span data-ttu-id="9cb3a-172">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="9cb3a-172">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="9cb3a-173">Войдите в Office 365 с помощью учетной записи и учетные данные, используемые для выполнения скрипта на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-173">Sign in to Office 365 using the account and credentials that you used to run the script in Step 1.</span></span>
    
3. <span data-ttu-id="9cb3a-174">В левой области безопасности &amp; центре соответствия требованиям, нажмите кнопку **поиска &amp; расследования** \> **поиска контента**и нажмите кнопку **Создать** ![значком Добавить](media/O365-MDM-CreatePolicy-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="9cb3a-174">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="9cb3a-p116">На странице **Новый поиск** введите имя поиска контента. Это имя должно быть уникальным в пределах организации.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p116">On the **New search** page, type a name for the Content Search. This name has to be unique in your organization.</span></span> 
    
5. <span data-ttu-id="9cb3a-177">В разделе, **выберите раздел "мне нравится" для поиска**, выполните одно из следующих значений, в зависимости от поиска почтовых ящиков или папка сайта:</span><span class="sxs-lookup"><span data-stu-id="9cb3a-177">Under **Where do you want us to look**, do one of the following, based on whether your searching a mailbox folder or a site folder:</span></span>
    
    - <span data-ttu-id="9cb3a-178">Нажмите кнопку **выбрать определенных почтовых ящиков для поиска** , а затем добавьте этого почтового ящика, который указан при выполнении скрипта на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-178">Click **Choose specific mailboxes to search** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span> 
    
      <span data-ttu-id="9cb3a-179">Второй вариант:</span><span class="sxs-lookup"><span data-stu-id="9cb3a-179">Or</span></span>
    
    - <span data-ttu-id="9cb3a-180">Нажмите кнопку **выбрать определенных сайтов для поиска** для поиска и затем добавьте же URL-адрес сайта, который указан при выполнении скрипта на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-180">Click **Choose specific sites to search** to search and then add the same site URL that you specified when you ran the script in Step 1.</span></span> 
    
6. <span data-ttu-id="9cb3a-181">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-181">Click **Next**.</span></span>
    
7. <span data-ttu-id="9cb3a-182">На странице **выберите "мне нравится" для поиска** в поле ключевое слово вставьте `folderid:<folderid>` или `path:<path>` значение, возвращенное сценарием на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-182">In the keyword box on the **What do you want us to look for** page, paste the  `folderid:<folderid>` or  `path:<path>` value that was returned by the script in Step 1.</span></span> 
    
    <span data-ttu-id="9cb3a-183">Например, запрос на следующем снимке экрана выполняет поиск любого элемента во вложенной папке удаляет в папки элементов для восстановления (значение `folderid` свойства для вложенной папке удаляет — это показано на снимке экрана на шаге 1):</span><span class="sxs-lookup"><span data-stu-id="9cb3a-183">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>
    
    ![Вставьте folderid или путь в поле ключевого слова поискового запроса](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. <span data-ttu-id="9cb3a-185">Нажмите кнопку **поиска** , чтобы начать поиск целевой коллекции.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-185">Click **Search** to start the targeted collection search.</span></span> 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="9cb3a-186">Примеры запросов поиска для целевого семейства сайтов</span><span class="sxs-lookup"><span data-stu-id="9cb3a-186">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="9cb3a-p117">Вот несколько примеров использования `folderid` и `path` свойства в поисковый запрос для выполнения целевой коллекции. Обратите внимание на то, что заполнители используются для `folderid:<folderid>` и `path:<path>` для экономии места.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p117">Here are some examples of using the  `folderid` and  `path` properties in a search query to perform a targeted collection. Note that placeholders are used for  `folderid:<folderid>` and  `path:<path>` to save space.</span></span> 
  
- <span data-ttu-id="9cb3a-p118">В этом примере выполняется поиск папки три разных почтовых ящиков. Можно использовать следующий синтаксис запроса для поиска скрытых папок в папки элементов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p118">This example searches three different mailbox folders. You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="9cb3a-191">В этом примере производится поиск в папке почтового ящика для элементов, которые содержат точную фразу.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-191">This example searches a mailbox folder for items that contain an exact phrase.</span></span>
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="9cb3a-192">В этом примере выполняется поиск папки сайта (и все вложенные папки) документов, содержащих только буквы «Соглашение о неразглашении МЕЖДУ» в поле название.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-192">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>
    
  ```
  path:<path> AND filename:nda
  ```

- <span data-ttu-id="9cb3a-193">В этом примере выполняется поиск папки сайта (и все подпапки) для документов были изменены в интервал дат.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-193">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a><span data-ttu-id="9cb3a-194">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="9cb3a-194">More information</span></span>

<span data-ttu-id="9cb3a-195">Имейте в виду следующее при семейств сайтов с помощью скрипта в этой статье и для выполнения.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-195">Keep the following things in mind when using the script in this article and performing targeted collections.</span></span>
  
- <span data-ttu-id="9cb3a-p119">Сценарий не удалять какие-либо папки из результатов. Указанные некоторые папки в результаты могут быть не включаемые (или возврата ноль элементов), так как они содержат сгенерированное системой содержимого.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p119">The script doesn't remove any folders from the results. So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content.</span></span>
    
- <span data-ttu-id="9cb3a-p120">Этот сценарий возвращает только сведений о папке для основного почтового ящика пользователя. Он не возвращает сведения о папках в архивный почтовый ящик пользователя.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p120">This script only returns folder information for the user's primary mailbox. It doesn't return information about folders in the user's archive mailbox.</span></span>
    
- <span data-ttu-id="9cb3a-p121">При поиске папки почтовых ящиков, только в указанной папке (обозначенный его `folderid` свойство) будет осуществляться. Вложенные папки не будет искать. Чтобы выполнить поиск вложенных папок, которые необходимы для использования `folderid` для вложенных папок, который нужно найти.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p121">When searching mailbox folders, only the specified folder (identified by its  `folderid` property) will be searched. Subfolders won't be searched. To search sub-folders, you need to use the  `folderid` for the sub-folder that you want to search.</span></span> 
    
- <span data-ttu-id="9cb3a-203">При поиске папки сайта, папка (обозначенный его `path` свойство) и всех вложенных папок поиска.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-203">When searching site folders, the folder (identified by its  `path` property) and all sub-folders will be searched.</span></span> 
    
- <span data-ttu-id="9cb3a-p122">Как было сказано ранее, нельзя использовать `path` свойство для поиска файлов мультимедиа, таких как PNG, TIFF. или WAV-файл, расположенный в OneDrive расположения. Используйте различные [Свойства сайта](keyword-queries-and-search-conditions.md#searchable-site-properties) для поиска файлов мультимедиа в папках OneDrive.</span><span class="sxs-lookup"><span data-stu-id="9cb3a-p122">As previously stated, you can't use  `path` property to search for media files, such as .png, .tiff, or .wav files, located in OneDrive locations. Use a different [site property](keyword-queries-and-search-conditions.md#searchable-site-properties) to search for media files in OneDrive folders.</span></span> 
