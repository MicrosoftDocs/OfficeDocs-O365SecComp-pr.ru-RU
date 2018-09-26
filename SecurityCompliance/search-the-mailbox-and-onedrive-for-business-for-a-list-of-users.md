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
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a>Поиск списка пользователей в почтовом ящике и на сайте OneDrive для бизнеса с помощью поиска контента

Безопасность Office 365 &amp; центре соответствия требованиям предоставляет ряд командлетов Windows PowerShell, позволяющие автоматизировать занимать много времени задачи, связанные с обнаружения электронных данных. На данный момент создания поиска содержимого в системы &amp; центре соответствия требованиям для поиска большое число размещения содержимого custodian затраты времени и подготовки. Перед созданием поиска необходимо собрать URL-адрес для каждого OneDrive для бизнеса сайта, а затем добавьте каждого почтового ящика и neDrive O для сайта бизнес поиск в. В будущих выпусках, это будет проще безопасности &amp; центре соответствия требованиям. До тех пор можно использовать сценарий в этой статье для автоматизации этого процесса. Этого сценария необходимо будет ввести имя домена вашей организации MySite (например, **contoso** в URL-адрес https://contoso-my.sharepoint.com), решает списка сообщений электронной почты пользователя, имя нового поиска контента и запросов поиска для использования. Скрипт получает OneDrive для бизнеса URL-адреса для каждого пользователя в списке и затем создает и запускает поиска контента, которая выполняет поиск почтового ящика и OneDrive для бизнеса узла для каждого пользователя в списке, с помощью запросов поиска, который вы предоставлять. 
  
## <a name="before-you-begin"></a>Перед началом работы

- Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям и SharePoint Online глобального администратора для запуска сценария в шаге 3.
    
- Не забудьте сохранить список пользователей, созданные вами в шаге 2 и скрипт в шаге 3 в ту же папку. Который будет упростить выполнение скрипта.
    
- Сценарий включает в себя обработка минимальной ошибок. Основным назначением является быстро и легко поиска почтовых ящиков и OneDrive для бизнеса сайта каждого из пользователей.
    
- Примеры сценариев, представленные в этом разделе не поддерживаются в разделе службы или любой другой программы стандартной поддержки корпорации Майкрософт. Примеры сценариев, предоставляются как есть без никаких гарантий. Дополнительно корпорация Майкрософт не все я[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied никаких гарантий, включая, без ограничений, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности примеры скриптов и документация остается с вами. Событие не корпорации Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценариев несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать примеры сценариев или документации, даже если Microsoft поступали предупреждения о возможности такого ущерба.
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Шаг 1. Установка командной консоли SharePoint Online
<a name="step1"> </a>

Первым шагом является установка консоли SharePoint Online. Использование командной консоли в эту процедуру не требуется, но необходимо установить, так как он содержит необходимые условия, необходимые для сценария, на котором запущен на шаге 3. Эти компоненты позволяют скрипта для взаимодействия с SharePoint Online, чтобы получить URL-адреса для OneDrive для бизнеса сайтов.
  
Перейдите к [настройке среды SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) и выполните шаг 1 и шаг 2 для установки консоли SharePoint Online.
  
## <a name="step-2-generate-a-list-of-users"></a>Шаг 2: Создание списка пользователей
<a name="step2"> </a>

Скрипт в шаге 3 создадим контента поиска для поиска почтовых ящиков и учетных записей службы OneDrive для списка пользователей. Можно просто введите адреса электронной почты в текстовом файле или выполнении команды Windows PowerShell, чтобы получить список адресов электронной почты и сохраните их в файл (находится в одной папке, где будут сохранены скрипт, чтобы в шаге 3).
  
Вот команда [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) , что вы можете runt ознакомьтесь со списком адресов электронной почты для всех пользователей в вашей организации и сохранение его в текстовый файл с именем `Users.txt`. 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

После выполнения этой команды необходимо открыть файл и удалить заголовок, содержащий имя свойства `PrimarySmtpAddress`. В текстовом файле только что должны содержать список адресов электронной почты и ничего. Убедитесь, что нет ни одной пустой строки до или после список адресов электронной почты.
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a>Шаг 3: Выполните скрипт, чтобы создавать и запускать поиск

При запуске сценария на этом этапе его запросит со следующими сведениями. Убедитесь, что для получения этой информации готов, перед запуском сценария.
  
- **Учетные данные пользователя** - скрипт будет использовать свои учетные данные для доступа к SharePoint Online, чтобы получить OneDrive для бизнеса URL-адресов и для подключения к безопасности &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell. 
    
- **Имя вашего домена MySite** - MySite домена является домен, который содержит все OneDrive для бизнеса сайтов в вашей организации. Например, если URL-адрес для своего домена MySite — **https://contoso-my.sharepoint.com**, а затем введите `contoso` когда будет предложено для имени домена MySite. 
    
- **Путь к файлу текст из действия 2** - pathname текстовый файл, созданный на шаге 2. Если в текстовом файле и скрипт, находятся в той же папке, введите имя в текстовом файле. В противном случае укажите полный путь для текстового файла. 
    
- **Имя поиска контента** - имя поиска контента, который будет создан с помощью сценария. 
    
- Создан и запустите **поисковых запросов** - запросов поиска, который будет использоваться с поиска контента. Дополнительные сведения о запросах поиска можно [запросах по ключевым словам и условия поиска для поиска контента](keyword-queries-and-search-conditions.md).


**Чтобы запустить сценарий, сделайте следующее:**
    
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `SearchEXOOD4B.ps1`. Сохраните файл на ту же папку, где был сохранен в списке пользователей на шаге 2.
    
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

2. Откройте Windows PowerShell и перейдите к папке, в которой был сохранен сценарий и список пользователей в шаге 2.
    
3. Запустите сценарий; Например:
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. Когда требуется ввести учетные данные, введите адрес электронной почты и пароль и нажмите кнопку **ОК**. 
    
5. Введите следующую информацию в ответ на запрос с помощью сценария. Введите каждый блок данных и нажмите клавишу **Ввод**.
    
    - Имя вашего домена MySite. 
    
    - Путь к текстовый файл, содержащий список пользователей.
    
    - Имя для поиска контента.
    
    - Запрос поиска (оставьте этом пустой для возвращения всех элементов в размещения содержимого).
    
    Скрипт возвращает URL-адреса для каждого OneDrive для бизнеса сайта и создает и запускает поиска. Либо можно запустить командлет **Get-ComplianceSearch** в безопасности & PowerShell центр соответствия требованиям для отображения статистика поиска и результатов, или можно перейти к странице **поиска контента** в системы &amp; центре соответствия требованиям для просмотра сведения о поиске. 
