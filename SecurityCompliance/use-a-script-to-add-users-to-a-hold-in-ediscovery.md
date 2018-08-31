---
title: Использование сценария для добавления пользователей в удержание в случае обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: Выполните скрипт, чтобы быстро добавить почтовые ящики и OneDrive для бизнеса-сайтов в новое удержание, связанной с вариантом eDiscovery безопасности Office 365 &amp; центре соответствия требованиям.
ms.openlocfilehash: eb53f01b4f1b7245e1411ac470db629115eb1ef5
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534766"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="c6ccd-103">Использование сценария для добавления пользователей в удержание в случае обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="c6ccd-103">Use a script to add users to a hold in an eDiscovery case in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="c6ccd-p101">Безопасность Office 365 &amp; центре соответствия требованиям содержит большое количество командлетов Windows PowerShell, позволяющие автоматизировать занимать много времени задачи, связанные с создания и управления ими вариантах eDiscovery. В настоящее время с помощью вариантов средство обнаружения электронных данных в системы &amp; центре соответствия требованиям, чтобы поставить на удержание большое число размещения содержимого custodian затраты времени и подготовки. К примеру перед созданием удержания необходимо собрать URL-адрес для каждого OneDrive для бизнеса сайта, который необходимо поставить на удержание. Затем для каждого пользователя, которые необходимо поставить на удержание, необходимо добавить к удержанию их почтовых ящиков и их OneDrive для бизнеса сайта. В будущих выпусках безопасности &amp; центре соответствия требованиям, будет проще. До тех пор можно использовать сценарий в этой статье для автоматизации этого процесса.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p101">The Office 365 Security &amp; Compliance Center provides lots of Windows PowerShell cmdlets that let you automate time-consuming tasks related to creating and managing eDiscovery cases. Currently, using the eDiscovery case tool in the Security &amp; Compliance Center to place a large number of custodian content locations on hold takes time and preparation. For example, before you create a hold, you have to collect the URL for each OneDrive for Business site that you want to place on hold. Then for each user you want to place on hold, you have to add their mailbox and their OneDrive for Business site to the hold. In future releases of the Security &amp; Compliance Center, this will get easier to do. Until then, you can use the script in this article to automate this process.</span></span>
  
<span data-ttu-id="c6ccd-p102">Сценарий выдает запрос на имя домена вашей организации MySite (например, **contoso** в URL-адрес https://contoso-my.sharepoint.com), имя существующего случая обнаружения электронных данных, имя нового удержания, связанные с вариантом, список адресов электронной почты пользователей, необходимо Чтобы поместить на удержание и запросов поиска для использования, если вы хотите создать удержание на основе запроса. Сценарий затем возвращает URL-адрес для OneDrive для бизнеса сайтов для каждого пользователя в списке, создает новый удержания и затем добавляет почтовых ящиков и OneDrive для бизнеса узла для каждого пользователя в списке удержания. Скрипт также создает файлы журнала, содержащие сведения о новых удержания.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p102">The script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), the name of an existing eDiscovery case, the name of the new hold that associated with the case, a list of email addresses of the users you want to put on hold, and a search query to use if you want to create a query-based hold. The script then gets the URL for the OneDrive for Business site for each user in the list, creates the new hold, and then adds the mailbox and OneDrive for Business site for each user in the list to the hold. The script also generates log files that contain information about the new hold.</span></span> 
  
<span data-ttu-id="c6ccd-113">Далее приведены шаги для этого введите:</span><span class="sxs-lookup"><span data-stu-id="c6ccd-113">Here are the steps to make this happen:</span></span>
  
[<span data-ttu-id="c6ccd-114">Шаг 1. Установка командной консоли SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c6ccd-114">Step 1: Install the SharePoint Online Management Shell</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[<span data-ttu-id="c6ccd-115">Шаг 2: Создание списка пользователей</span><span class="sxs-lookup"><span data-stu-id="c6ccd-115">Step 2: Generate a list of users</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[<span data-ttu-id="c6ccd-116">Шаг 3: Выполните скрипт, чтобы создать удержание и добавление пользователей</span><span class="sxs-lookup"><span data-stu-id="c6ccd-116">Step 3: Run the script to create a hold and add users</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a><span data-ttu-id="c6ccd-117">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="c6ccd-117">Before you begin</span></span>

- <span data-ttu-id="c6ccd-p103">Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям и SharePoint Online глобального администратора для запуска сценария в шаге 3. Дополнительные сведения можно [назначать разрешения обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center and a SharePoint Online global administrator to run the script in Step 3. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="c6ccd-p104">Не более 1 000 почтовых ящиков и 100 сайтов можно добавить к удержанию, связанной с вариантом eDiscovery в системы &amp; центре соответствия требованиям. Если предполагается, что каждый пользователь, который необходимо поставить на удержание имеет OneDrive для бизнеса сайта, не более 100 пользователей можно добавить к удержанию, с помощью скрипта в этой статье.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p104">A maximum of 1,000 mailboxes and 100 sites can be added to a hold that's associated with an eDiscovery case in the Security &amp; Compliance Center. Assuming that every user that you want to place on hold has a OneDrive for Business site, you can add a maximum of 100 users to a hold using the script in this article.</span></span> 
    
- <span data-ttu-id="c6ccd-p105">Не забудьте сохранить список пользователей, созданные вами в шаге 2 и скрипт в шаге 3 в ту же папку. Который будет упростить выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p105">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder. That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="c6ccd-p106">Сценарий добавляет список пользователей в новое удержание, связанный с существующей case. Убедитесь, что, которую требуется связать удержания с создания перед запуском сценария.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p106">The script adds the list of users to a new hold that is associated with an existing case. Be sure the case that you want to associate the hold with is created before you run the script.</span></span>
    
- <span data-ttu-id="c6ccd-p107">Сценарий включает в себя обработка минимальной ошибок. Атрибут предназначен для быстрого и простого помещения почтового ящика и удерживайте OneDrive для бизнеса узла для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p107">The script includes minimal error handling. Its primary purpose is to quickly and easily place the mailbox and OneDrive for Business site of each user on hold.</span></span>
    
- <span data-ttu-id="c6ccd-p108">Примеры сценариев, представленные в этом разделе не поддерживаются в разделе службы или любой другой программы стандартной поддержки корпорации Майкрософт. Примеры сценариев, предоставляются как есть без никаких гарантий. Дополнительно корпорация Майкрософт не все подразумеваемых гарантий, включая, без ограничения, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности примеры скриптов и документация остается с вами. Событие не корпорации Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценариев несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать примеры сценариев или документации, даже если Microsoft поступали предупреждения о возможности такого ущерба.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p108">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="c6ccd-133">Шаг 1. Установка командной консоли SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c6ccd-133">Step 1: Install the SharePoint Online Management Shell</span></span>

<span data-ttu-id="c6ccd-p109">Первым шагом является установка консоли SharePoint Online, если он еще не установлены на локальном компьютере. Использование командной консоли в эту процедуру не требуется, но необходимо установить, так как он содержит необходимые условия, необходимые для сценария, на котором запущен на шаге 3. Эти компоненты позволяют скрипта для взаимодействия с SharePoint Online, чтобы получить URL-адреса для OneDrive для бизнеса сайтов.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p109">The first step is to install the SharePoint Online Management Shell if it's not already installed on your local computer. You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3. These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="c6ccd-137">Перейдите к [настройке среды SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) и выполните шаг 1 и шаг 2 для установки консоли SharePoint Online на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-137">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell on your local computer.</span></span> 

## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="c6ccd-138">Шаг 2: Создание списка пользователей</span><span class="sxs-lookup"><span data-stu-id="c6ccd-138">Step 2: Generate a list of users</span></span>
<span data-ttu-id="c6ccd-139"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="c6ccd-139"></span></span>

<span data-ttu-id="c6ccd-p110">Скрипт в шаге 3 будет создать удержание, связанной с вариантом eDiscovery и добавить почтовых ящиков и OneDrive для бизнеса сайтов из списка пользователей к удержанию. Можно просто введите адреса электронной почты в текстовом файле или выполнении команды Windows PowerShell, чтобы получить список адресов электронной почты и сохраните их в файл (находится в одной папке, где будут сохранены скрипт, чтобы в шаге 3).</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p110">The script in Step 3 will create a hold that's associated with an eDiscovery case, and the add the mailboxes and OneDrive for Business sites of a list of users to the hold. You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="c6ccd-142">Вот команда PowerShell (которую можно запускать с помощью удаленной оболочки PowerShell, подключенных к организации Exchange Online) ознакомьтесь со списком адресов электронной почты для всех пользователей в вашей организации и сохранение его в текстовый файл с именем HoldUsers.txt.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-142">Here's a PowerShell command (that you run by using remote PowerShell connected to your Exchange Online organization) to get a list of email addresses for all users in your organization and save it to a text file named HoldUsers.txt.</span></span>
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

<span data-ttu-id="c6ccd-p111">После того как, выполните следующую команду, откройте текстовый файл и удалить заголовок, содержащий имя свойства `PrimarySmtpAddress`. Удалите все адреса электронной почты, за исключением из них для пользователей, которые вы хотите добавить к удержанию, которое вы создадите в шаге 3. Убедитесь, что нет ни одной пустой строки до или после список адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p111">After you run this command, open the text file and remove the header that contains the property name,  `PrimarySmtpAddress`. Then remove all email addresses except the ones for the users that you want to add to the hold that you'll create in Step 3. Make sure there are no blank rows before or after the list of email addresses.</span></span>
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a><span data-ttu-id="c6ccd-146">Шаг 3: Выполните скрипт, чтобы создать удержание и добавление пользователей</span><span class="sxs-lookup"><span data-stu-id="c6ccd-146">Step 3: Run the script to create a hold and add users</span></span>
<span data-ttu-id="c6ccd-147"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="c6ccd-147"></span></span>

<span data-ttu-id="c6ccd-p112">При запуске сценария на этом этапе его запросит со следующими сведениями. Убедитесь, что для получения этой информации готов, перед запуском сценария.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p112">When you run the script in this step, it will prompt you for the following information. Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="c6ccd-p113">**Учетные данные пользователя** - скрипт будет использовать свои учетные данные для подключения к безопасности &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell. Он также будет использовать эти учетные данные для доступа к SharePoint Online, чтобы получить OneDrive для бизнеса URL-адресов для списка пользователей.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p113">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center with remote PowerShell. It will also use these credentials to access SharePoint Online to get the OneDrive for Business URLs for the list of users.</span></span>
    
- <span data-ttu-id="c6ccd-p114">**Имя вашего домена MySite** - MySite домена является домен, который содержит все OneDrive для бизнеса сайтов в вашей организации. Например, если URL-адрес для своего домена MySite — **https://contoso-my.sharepoint.com**, а затем введите `contoso` когда будет предложено для имени домена MySite.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p114">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization. For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="c6ccd-p115">**Имя случая** — имя существующего случая. Скрипт будет создан новый удержания, связанный с этим обращением.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p115">**Name of the case** - The name of an existing case. The script will create a new hold that is associated with this case.</span></span>
    
- <span data-ttu-id="c6ccd-156">**Имя удержания** - имени удержания скрипт будет создавать и связать с указанным регистр.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-156">**Name of the hold** - The name of the hold the script will create and associate with the specified case.</span></span>
    
- <span data-ttu-id="c6ccd-p116">**Запрос поиска для запроса на удержание** - можно создать удержание на основе запроса, чтобы только содержимое, удовлетворяющие заданным критериям поиска ставится на удержание. Чтобы поместить все содержимое на удержание, нажмите клавишу **Ввод** , при появлении запроса поиска.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p116">**Search query for a query-based hold** - You can create a query-based hold so that only the content that meets the specified search criteria is placed on hold. To place all content on hold, just press **Enter** when you're prompted for a search query.</span></span> 
    
- <span data-ttu-id="c6ccd-p117">**Включить удержание или не** - у вас есть сценарий включить удержание после его создания или у вас есть сценарий создания удержания без включения его. Если у вас нет скрипта включить удержание, можно включить его позже в системы &amp; центре соответствия требованиям или, выполнив следующие команды PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p117">**Whether or not to turn the hold on** - You can have the script turn the hold on after it's created or you can have the script create the hold without enabling it. If you don't have the script turn on the hold, you can turn it on later in the Security &amp; Compliance Center or by running the following PowerShell commands:</span></span> 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- <span data-ttu-id="c6ccd-p118">**Имя текстового файла со списком пользователей** — имя текстового файла в шаге 2, который содержит список пользователей для добавления в удержание. Если этот файл находится в той же папке, что и сценарий, просто введите имя файла (например, HoldUsers.txt). Если текстовый файл в другую папку, введите полный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p118">**Name of the text file with the list of users** - The name of the text file from Step 2 that contains the list of users to add to the hold. If this file is located in the same folder as the script, just type the name of the file (for example, HoldUsers.txt). If the text file is in another folder, type the full pathname of the file.</span></span>
    
<span data-ttu-id="c6ccd-164">После собранные данные, скрипт будет предложено ввести, последний этап является выполните скрипт, чтобы создать новое удержание и добавление пользователей.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-164">After you've collected the information that the script will prompt you for, the final step is to run the script to create the new hold and add users to it.</span></span>
  
1. <span data-ttu-id="c6ccd-165">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `AddUsersToHold.ps1`.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-165">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `AddUsersToHold.ps1`.</span></span>
    
  ```
  #script begin
  " " 
  write-host "***********************************************"
  write-host "   Office 365 Security &amp; Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery cases - Add users to a hold   " -foregroundColor yellow -backgroundcolor darkgreen 
  write-host "***********************************************"
  " " 
  # Get user credentials &amp; Connect to Office 365 SCC, SPO
  $credentials = Get-Credential -Message "Specify your credentials to connect to the Office 365 Security &amp; Compliance Center and SharePoint Online"
  $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
  $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Couldn't create PowerShell session."
          return;
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
          Write-Error "The SharePoint Online Management Shell isn't installed. Please install it from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then re-run this script."
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Get the user's MySite domain name. We use this to create the admin URL and root URL for OneDrive for Business
  ""
  $mySiteDomain = Read-Host "Enter the name of your organization's MySite domain. For example, 'contoso' for 'https://contoso-my.sharepoint.com'"
  ""
  # Get other required information
  do{
  $casename = Read-Host "Enter the name of the case"
  $caseexists = (get-compliancecase -identity "$casename" -erroraction SilentlyContinue).isvalid
  if($caseexists -ne 'True')
  {""
  write-host "A case named '$casename' doesn't exist. Please specify the name of an existing case, or create a new case and then re-run the script." -foregroundColor Yellow
  ""}
  }While($caseexists -ne 'True')
  ""
  do{
  $holdName = Read-Host "Enter the name of the new hold"
  $holdexists=(get-caseholdpolicy -identity "$holdname" -case "$casename" -erroraction SilentlyContinue).isvalid
  if($holdexists -eq 'True')
  {""
  write-host "A hold named '$holdname' already exists. Please specify a new hold name." -foregroundColor Yellow
  ""}
  }While($holdexists -eq 'True')
  ""
  $holdQuery = Read-Host "Enter a search query to create a query-based hold, or press Enter to hold all content"
  ""
  $holdstatus = read-host "Do you want the hold enabled after it's created? (Yes/No)"
  do{
  ""
  $inputfile = read-host "Enter the name of the text file that contains the email addresses of the users to add to the hold"
  ""
  $fileexists = test-path -path $inputfile
  if($fileexists -ne 'True'){write-host "$inputfile doesn't exist. Please enter a valid file name." -foregroundcolor Yellow}
  }while($fileexists -ne 'True')
  #Import the list of addresses from the txt file.  Trim any excess spaces and make sure all addresses 
      #in the list are unique.
    [array]$emailAddresses = Get-Content $inputfile -ErrorAction SilentlyContinue | where {$_.trim() -ne ""}  | foreach{ $_.Trim() }
    [int]$dupl = $emailAddresses.count
    [array]$emailAddresses = $emailAddresses | select-object -unique
    $dupl -= $emailAddresses.count
  #Validate email addresses so the hold creation does not run in to an error.
  if($emailaddresses.count -gt 0){
  write-host ($emailAddresses).count "addresses were found in the text file. There were $dupl duplicate entries in the file." -foregroundColor Yellow
  ""
  Write-host "Validating the email addresses. Please wait..." -foregroundColor Yellow
  ""
  $finallist =@()
  foreach($emailAddress in $emailAddresses)
  {
  if((get-recipient $emailaddress -erroraction SilentlyContinue).isvalid -eq 'True')
  {$finallist += $emailaddress}
  else {"Unable to find the user $emailaddress"
  [array]$excludedlist += $emailaddress}
  }
  ""
  #find user's OneDrive Site URL using email address
  Write-Host "Getting the URL for each user's OneDrive for Business site." -foregroundColor Yellow
  ""
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
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
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
        try{
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" }
          $url = $prop.values[0].value
        if($url -ne $null){
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "- $emailAddress => $furl"
        [array]$ODadded += $furl}
    else{    
          Write-Warning "Couldn't locate OneDrive for $emailAddress"
        [array]$ODExluded += $emailAddress
      }}
    catch { 
    Write-Warning "Could not locate OneDrive for $emailAddress"
    [array]$ODExluded += $emailAddress
    Continue }
  }
  if(($finallist.count -gt 0) -or ($urls.count -gt 0)){
  ""
  Write-Host "Creating the hold named $holdname. Please wait..." -foregroundColor Yellow
  if(($holdstatus -eq "Y") -or ($holdstatus -eq  "y") -or ($holdstatus -eq "yes") -or ($holdstatus -eq "YES")){
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $True | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery | out-null
  }
  else{
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $false | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery -disabled $true | out-null
  }
  ""
  }
  else {"No valid locations were identified. Therefore, the hold wasn't created."}
  #write log files (if needed)
  $newhold=Get-CaseHoldPolicy -Identity "$holdname" -Case "$casename" -erroraction SilentlyContinue
  $newholdrule=Get-CaseHoldRule -Identity "$holdName" -erroraction SilentlyContinue
  if(($ODAdded.count -gt 0) -or ($ODExluded.count -gt 0) -or ($finallist.count -gt 0) -or ($excludedlist.count -gt 0) -or ($newhold.isvalid -eq 'True') -or ($newholdrule.isvalid -eq 'True'))
  {
  Write-Host "Generating output files..." -foregroundColor Yellow
  if($ODAdded.count -gt 0){
  "OneDrive Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.SharePointLocation.name | add-content .\LocationsOnHold.txt}
  if($ODExluded.count -gt 0){ 
  "Users without OneDrive locations" | add-content .\LocationsNotOnHold.txt
  "================================" | add-content .\LocationsNotOnHold.txt
  $ODExluded | add-content .\LocationsNotOnHold.txt}
  if($finallist.count -gt 0){
  " " | add-content .\LocationsOnHold.txt
  "Exchange Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.ExchangeLocation.name | add-content .\LocationsOnHold.txt}
  if($excludedlist.count -gt 0){
  " "| add-content .\LocationsNotOnHold.txt
  "Mailboxes not added to the hold" | add-content .\LocationsNotOnHold.txt
  "===============================" | add-content .\LocationsNotOnHold.txt
  $excludedlist | add-content .\LocationsNotOnHold.txt}
  $FormatEnumerationLimit=-1
  if($newhold.isvalid -eq 'True'){$newhold|fl >.\GetCaseHoldPolicy.txt}
  if($newholdrule.isvalid -eq 'True'){$newholdrule|Fl >.\GetCaseHoldRule.txt}
  }
  }
  else {"The hold wasn't created because no valid entries were found in the text file."}
  ""
  Write-host "Script complete!" -foregroundColor Yellow
  ""
  #script end
  ```

2. <span data-ttu-id="c6ccd-166">На локальном компьютере откройте Windows PowerShell и перейдите к папке, в которой вы сохранили скрипт.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-166">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="c6ccd-167">Выполнение скрипта; Например:</span><span class="sxs-lookup"><span data-stu-id="c6ccd-167">Run the script; for example:</span></span>
    
      ```
    .\AddUsersToHold.ps1
      ```

4. <span data-ttu-id="c6ccd-168">Введите сведения, будет предложено для.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-168">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="c6ccd-p119">Сценарий подключается к безопасности и соответствия требованиям центр PowerShell и создает новое удержание в случае обнаружения электронных данных и добавляет почтовых ящиков и OneDrive для бизнеса для пользователей в списке. Можно перейти в рамках данного экземпляра на странице **электронных данных** в безопасности &amp; центре соответствия требованиям для просмотра новое удержание.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p119">The script connects to Security & Compliance Center PowerShell, and then creates the new hold in the eDiscovery case and adds the mailboxes and OneDrive for Business for the users in the list. You can go to the case on the **eDiscovery** page in the Security &amp; Compliance Center to view the new hold.</span></span> 
    
<span data-ttu-id="c6ccd-171">После завершения скрипта под управлением, он создает следующие файлы журналов и сохраняет их в папку, где находится скрипта.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-171">After the script is finished running, it creates the following log files, and saves them to the folder where the script is located.</span></span>
  
- <span data-ttu-id="c6ccd-172">**LocationsOnHold.txt** - содержит список почтовых ящиков и OneDrive для бизнеса сайтов, сценарий успешно помещенных на удержание.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-172">**LocationsOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script successfully placed on hold.</span></span>
    
- <span data-ttu-id="c6ccd-p120">**LocationsNotOnHold.txt** - содержит список почтовых ящиков и OneDrive для бизнеса сайтов, сценарий не было поставить на удержание. Если пользователь имеет почтовый ящик, но не OneDrive для бизнеса сайта, пользователь будет включены в список OneDrive для бизнеса сайты, которые не были помещенные на удержание.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p120">**LocationsNotOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script did not place on hold. If a user has a mailbox, but not a OneDrive for Business site, the user would be included in the list of OneDrive for Business sites that weren't placed on hold.</span></span>
    
- <span data-ttu-id="c6ccd-p121">**GetCaseHoldPolicy.txt** - содержит выходные данные командлета **Get-CaseHoldPolicy** для новых удержания сценарий выполняется после создания нового удержания. Данные, возвращенные с помощью этого командлета содержит список пользователей, чьи почтовые ящики и OneDrive для бизнеса сайтов находятся на удержании и включение или отключение удержания.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p121">**GetCaseHoldPolicy.txt** - Contains the output of the **Get-CaseHoldPolicy** cmdlet for the new hold, which the script ran after creating the new hold. The information returned by this cmdlet includes a list of users whose mailboxes and OneDrive for Business sites were placed on hold and whether the hold is enabled or disabled.</span></span> 
    
- <span data-ttu-id="c6ccd-p122">**GetCaseHoldRule.txt** - содержит выходные данные командлета **Get-CaseHoldRule** для новых удержания сценарий выполняется после создания нового удержания. Сведения, возвращаемые этот командлет включает поисковый запрос, если скрипт используется для создания запроса на удержание.</span><span class="sxs-lookup"><span data-stu-id="c6ccd-p122">**GetCaseHoldRule.txt** - Contains the output of the **Get-CaseHoldRule** cmdlet for the new hold, which the script ran after creating the new hold. The information returned by this cmdlet includes the search query if you used the script to create a query-based hold.</span></span> 
