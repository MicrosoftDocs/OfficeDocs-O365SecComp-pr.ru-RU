---
title: Поиск списка пользователей в почтовом ящике и на сайте OneDrive для бизнеса с помощью поиска контента
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Использование поиска контента и сценарий в этой статье для поиска почтовых ящиков и OneDrive для бизнеса сайтов для группы пользователей.
ms.openlocfilehash: e7f16ec0ca34d9f7f6155cab7e473119de3966cb
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038172"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a><span data-ttu-id="f8030-103">Поиск списка пользователей в почтовом ящике и на сайте OneDrive для бизнеса с помощью поиска контента</span><span class="sxs-lookup"><span data-stu-id="f8030-103">Use Content Search to search the mailbox and OneDrive for Business site for a list of users</span></span>

<span data-ttu-id="f8030-p101">Безопасность Office 365 &amp; центре соответствия требованиям предоставляет ряд командлетов Windows PowerShell, позволяющие автоматизировать занимать много времени задачи, связанные с обнаружения электронных данных. На данный момент создания поиска содержимого в системы &amp; центре соответствия требованиям для поиска большое число размещения содержимого custodian затраты времени и подготовки. Перед созданием поиска необходимо собрать URL-адрес для каждого OneDrive для бизнеса сайта, а затем добавьте каждого почтового ящика и neDrive O для сайта бизнес поиск в. В будущих выпусках, это будет проще безопасности &amp; центре соответствия требованиям. До тех пор можно использовать сценарий в этой статье для автоматизации этого процесса. Этого сценария необходимо будет ввести имя домена вашей организации MySite (например, **contoso** в URL-адрес https://contoso-my.sharepoint.com), решает списка сообщений электронной почты пользователя, имя нового поиска контента и запросов поиска для использования. Скрипт получает OneDrive для бизнеса URL-адреса для каждого пользователя в списке и затем создает и запускает поиска контента, которая выполняет поиск почтового ящика и OneDrive для бизнеса узла для каждого пользователя в списке, с помощью запросов поиска, который вы предоставлять.</span><span class="sxs-lookup"><span data-stu-id="f8030-p101">The Office 365 Security &amp; Compliance Center provides a number of Windows PowerShell cmdlets that let you automate time-consuming eDiscovery-related tasks. Currently, creating a Content Search in the Security &amp; Compliance Center to search a large number of custodian content locations takes time and preparation. Before you create a search, you have to collect the URL for each OneDrive for Business site and then add each mailbox and O neDrive for Business site to the search. In future releases, this will be easier to do in the Security &amp; Compliance Center. Until then, you can use the script in this article to automate this process. This script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), a list of user email addresses, the name of the new Content Search, and the search query to use. The script gets the OneDrive for Business URL for each user in the list, and then it creates and starts a Content Search that searches the mailbox and OneDrive for Business site for each user in the list, using the search query that you provide.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="f8030-111">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="f8030-111">Before you begin</span></span>

- <span data-ttu-id="f8030-112">Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям и SharePoint Online глобального администратора для запуска сценария в шаге 3.</span><span class="sxs-lookup"><span data-stu-id="f8030-112">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center and a SharePoint Online global administrator to run the script in Step 3.</span></span>
    
- <span data-ttu-id="f8030-p102">Не забудьте сохранить список пользователей, созданные вами в шаге 2 и скрипт в шаге 3 в ту же папку. Который будет упростить выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="f8030-p102">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder. That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="f8030-p103">Сценарий включает в себя обработка минимальной ошибок. Основным назначением является быстро и легко поиска почтовых ящиков и OneDrive для бизнеса сайта каждого из пользователей.</span><span class="sxs-lookup"><span data-stu-id="f8030-p103">The script includes minimal error handling. It's primary purpose is to quickly and easily search the mailbox and OneDrive for Business site of each user.</span></span>
    
- <span data-ttu-id="f8030-p104">Примеры сценариев, представленные в этом разделе не поддерживаются в разделе службы или любой другой программы стандартной поддержки корпорации Майкрософт. Примеры сценариев, предоставляются как есть без никаких гарантий. Дополнительно корпорация Майкрософт не все я[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied никаких гарантий, включая, без ограничений, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности примеры скриптов и документация остается с вами. Событие не корпорации Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценариев несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать примеры сценариев или документации, даже если Microsoft поступали предупреждения о возможности такого ущерба.</span><span class="sxs-lookup"><span data-stu-id="f8030-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="f8030-122">Шаг 1. Установка командной консоли SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="f8030-122">Step 1: Install the SharePoint Online Management Shell</span></span>
<span data-ttu-id="f8030-123"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="f8030-123"></span></span>

<span data-ttu-id="f8030-p105">Первым шагом является установка консоли SharePoint Online. Использование командной консоли в эту процедуру не требуется, но необходимо установить, так как он содержит необходимые условия, необходимые для сценария, на котором запущен на шаге 3. Эти компоненты позволяют скрипта для взаимодействия с SharePoint Online, чтобы получить URL-адреса для OneDrive для бизнеса сайтов.</span><span class="sxs-lookup"><span data-stu-id="f8030-p105">The first step is to install the SharePoint Online Management Shell. You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3. These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="f8030-127">Перейдите к [настройке среды SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) и выполните шаг 1 и шаг 2 для установки консоли SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="f8030-127">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell.</span></span>
  
## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="f8030-128">Шаг 2: Создание списка пользователей</span><span class="sxs-lookup"><span data-stu-id="f8030-128">Step 2: Generate a list of users</span></span>
<span data-ttu-id="f8030-129"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="f8030-129"></span></span>

<span data-ttu-id="f8030-p106">Скрипт в шаге 3 создадим контента поиска для поиска почтовых ящиков и учетных записей службы OneDrive для списка пользователей. Можно просто введите адреса электронной почты в текстовом файле или выполнении команды Windows PowerShell, чтобы получить список адресов электронной почты и сохраните их в файл (находится в одной папке, где будут сохранены скрипт, чтобы в шаге 3).</span><span class="sxs-lookup"><span data-stu-id="f8030-p106">The script in Step 3 will create a Content Search to search the mailboxes and OneDrive accounts for a list of users. You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="f8030-132">Вот команда [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) , что вы можете runt ознакомьтесь со списком адресов электронной почты для всех пользователей в вашей организации и сохранение его в текстовый файл с именем `Users.txt`.</span><span class="sxs-lookup"><span data-stu-id="f8030-132">Here's an [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) command that you can runt to get a list of email addresses for all users in your organization and save it to a text file named `Users.txt`.</span></span> 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

<span data-ttu-id="f8030-p107">После выполнения этой команды необходимо открыть файл и удалить заголовок, содержащий имя свойства `PrimarySmtpAddress`. В текстовом файле только что должны содержать список адресов электронной почты и ничего. Убедитесь, что нет ни одной пустой строки до или после список адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f8030-p107">After you run this command, be sure to open the file and remove the header that contains the property name,  `PrimarySmtpAddress`. The text file should just contain a list of email addresses, and nothing else. Make sure there are no blank rows before or after the list of email addresses.</span></span>
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a><span data-ttu-id="f8030-136">Шаг 3: Выполните скрипт, чтобы создавать и запускать поиск</span><span class="sxs-lookup"><span data-stu-id="f8030-136">Step 3: Run the script to create and start the search</span></span>

<span data-ttu-id="f8030-p108">При запуске сценария на этом этапе его запросит со следующими сведениями. Убедитесь, что для получения этой информации готов, перед запуском сценария.</span><span class="sxs-lookup"><span data-stu-id="f8030-p108">When you run the script in this step, it will prompt you for the following information. Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="f8030-139">**Учетные данные пользователя** - скрипт будет использовать свои учетные данные для доступа к SharePoint Online, чтобы получить OneDrive для бизнеса URL-адресов и для подключения к безопасности &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8030-139">**Your user credentials** - The script will use your credentials to access SharePoint Online to get the OneDrive for Business URLs and to connect to the Security &amp; Compliance Center with remote PowerShell.</span></span> 
    
- <span data-ttu-id="f8030-p109">**Имя вашего домена MySite** - MySite домена является домен, который содержит все OneDrive для бизнеса сайтов в вашей организации. Например, если URL-адрес для своего домена MySite — **https://contoso-my.sharepoint.com**, а затем введите `contoso` когда будет предложено для имени домена MySite.</span><span class="sxs-lookup"><span data-stu-id="f8030-p109">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization. For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="f8030-p110">**Путь к файлу текст из действия 2** - pathname текстовый файл, созданный на шаге 2. Если в текстовом файле и скрипт, находятся в той же папке, введите имя в текстовом файле. В противном случае укажите полный путь для текстового файла.</span><span class="sxs-lookup"><span data-stu-id="f8030-p110">**Pathname of the text file from Step 2** - The pathname of the text file that you created in Step 2. If the text file and the script are located in the same folder, then enter the name of the text file. Otherwise, enter the complete pathname for the text file.</span></span> 
    
- <span data-ttu-id="f8030-145">**Имя поиска контента** - имя поиска контента, который будет создан с помощью сценария.</span><span class="sxs-lookup"><span data-stu-id="f8030-145">**Name of the Content Search** - The name of the Content Search that will be created by the script.</span></span> 
    
- <span data-ttu-id="f8030-p111">Создан и запустите **поисковых запросов** - запросов поиска, который будет использоваться с поиска контента. Дополнительные сведения о запросах поиска можно [запросах по ключевым словам и условия поиска для поиска контента](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="f8030-p111">**Search query** - The search query that will be used with the Content Search is created and run. For more information about search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>


<span data-ttu-id="f8030-148">**Чтобы запустить сценарий, сделайте следующее:**</span><span class="sxs-lookup"><span data-stu-id="f8030-148">**To run the script:**</span></span>
    
1. <span data-ttu-id="f8030-p112">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `SearchEXOOD4B.ps1`. Сохраните файл на ту же папку, где был сохранен в списке пользователей на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="f8030-p112">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchEXOOD4B.ps1`. Save the file to the same folder where you saved the list of users in Step 2.</span></span>
    
  ```
  # This PowerShell script will prompt you for the following information:
  #    * Your user credentials 
  #    * The name of your organization's MySite domain                                              
  #    * The pathname for the text file that contains a list of user email addresses
  #    * The name of the Content Search that will be created
  #    * The search query string
  # The script will then:
  #    * Find the OneDrive for Business site for each user in the text file
  #    * Create and start a Content Search using the above information
  # Get user credentials
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  # Get the user's MySite domain name.  We use this to create the admin URL and root URL for OneDrive for Business
  $mySiteDomain = Read-Host "What is your organization's MySite domain?  For example,  'contoso' for 'https://contoso-my.sharepoint.com'"
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
  # Get other required information
  $inputfile = read-host "Enter the file name of the text file that contains the email addresses for the users you want to search"
  $searchName = Read-Host "Enter the name for the new search"
  $searchQuery = Read-Host "Enter the search query you want to use"
  $emailAddresses = Get-Content $inputfile | where {$_ -ne ""}  | foreach{ $_.Trim() }
  # Connect to Office 365
  if (!$s -or !$a)
  {
      $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
      $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Could not create PowerShell session."
          return;
      }
  }
  # Load the SharePoint assemblies from the SharePoint Online Management Shell
  # To install, go to http://go.microsoft.com/fwlink/p/?LinkId=255251
  if (!$SharePointClient -or !$SPRuntime -or !$SPUserProfile)
  {
      $SharePointClient = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client")
      $SPRuntime = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.Runtime")
      $SPUserProfile = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.UserProfiles")
      if (!$SharePointClient)
      {
          Write-Error "SharePoint Online Management Shell isn't installed, please install from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then run this script again"
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Add the path of the User Profile Service to the SPO admin URL, then create a new webservice proxy to access it
  $proxyaddr = "$AdminUrl/_vti_bin/UserProfileService.asmx?wsdl"
  $UserProfileService= New-WebServiceProxy -Uri $proxyaddr -UseDefaultCredential False
  $UserProfileService.Credentials = $credentials
  # Take care of auth cookies
  $strAuthCookie = $spCreds.GetAuthenticationCookie($AdminUrl)
  $uri = New-Object System.Uri($AdminUrl)
  $container = New-Object System.Net.CookieContainer
  $container.SetCookies($uri, $strAuthCookie)
  $UserProfileService.CookieContainer = $container
  Write-Host "Getting each user's OneDrive for Business URL"
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
      try
      {
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" } 
          $url = $prop.values[0].value
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "-$emailAddress => $furl"
      }
      catch
      {
          Write-Warning "Could not locate OneDrive for $emailAddress"
      }
  }
  Write-Host "Creating and starting the search"
  $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $emailAddresses -SharePointLocation $urls -ContentMatchQuery $searchQuery
  # Finally, start the search and then display the status
  if($search)
  {
      Start-ComplianceSearch $search.Name
      Get-ComplianceSearch $search.Name
  }
  
  ```

2. <span data-ttu-id="f8030-151">Откройте Windows PowerShell и перейдите к папке, в которой был сохранен сценарий и список пользователей в шаге 2.</span><span class="sxs-lookup"><span data-stu-id="f8030-151">Open Windows PowerShell and go to the folder where you saved the script and the list of users from Step 2.</span></span>
    
3. <span data-ttu-id="f8030-152">Запустите сценарий; Например:</span><span class="sxs-lookup"><span data-stu-id="f8030-152">Start the script; for example:</span></span>
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. <span data-ttu-id="f8030-153">Когда требуется ввести учетные данные, введите адрес электронной почты и пароль и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f8030-153">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="f8030-p113">Введите следующую информацию в ответ на запрос с помощью сценария. Введите каждый блок данных и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="f8030-p113">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="f8030-156">Имя вашего домена MySite.</span><span class="sxs-lookup"><span data-stu-id="f8030-156">The name of your MySite domain.</span></span> 
    
    - <span data-ttu-id="f8030-157">Путь к текстовый файл, содержащий список пользователей.</span><span class="sxs-lookup"><span data-stu-id="f8030-157">The pathname of the text file that contains the list of users.</span></span>
    
    - <span data-ttu-id="f8030-158">Имя для поиска контента.</span><span class="sxs-lookup"><span data-stu-id="f8030-158">A name for the Content Search.</span></span>
    
    - <span data-ttu-id="f8030-159">Запрос поиска (оставьте этом пустой для возвращения всех элементов в размещения содержимого).</span><span class="sxs-lookup"><span data-stu-id="f8030-159">The search query (leave this blank to return all items in the content locations).</span></span>
    
    <span data-ttu-id="f8030-p114">Скрипт возвращает URL-адреса для каждого OneDrive для бизнеса сайта и создает и запускает поиска. Либо можно запустить командлет **Get-ComplianceSearch** в безопасности & PowerShell центр соответствия требованиям для отображения статистика поиска и результатов, или можно перейти к странице **поиска контента** в системы &amp; центре соответствия требованиям для просмотра сведения о поиске.</span><span class="sxs-lookup"><span data-stu-id="f8030-p114">The script gets the URLs for each OneDrive for Business site and then creates and starts the search. You can either run the **Get-ComplianceSearch** cmdlet in Security & Compliance Center PowerShell to display the search statistics and results, or you can go to the **Content search** page in the Security &amp; Compliance Center to view information about the search.</span></span> 
