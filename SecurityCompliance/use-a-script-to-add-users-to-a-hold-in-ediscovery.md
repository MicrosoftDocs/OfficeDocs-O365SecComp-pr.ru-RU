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
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: Выполните скрипт, чтобы быстро добавить почтовые ящики и OneDrive для бизнеса-сайтов в новое удержание, связанной с вариантом eDiscovery безопасности Office 365 &amp; центре соответствия требованиям.
ms.openlocfilehash: 2c93deb14bc8c1f89dab7bb054d2e94db06cfbd5
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038262"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a>Использование сценария для добавления пользователей в удержание в случае обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям

Безопасность Office 365 &amp; центре соответствия требованиям содержит большое количество командлетов Windows PowerShell, позволяющие автоматизировать занимать много времени задачи, связанные с создания и управления ими вариантах eDiscovery. В настоящее время с помощью вариантов средство обнаружения электронных данных в системы &amp; центре соответствия требованиям, чтобы поставить на удержание большое число размещения содержимого custodian затраты времени и подготовки. К примеру перед созданием удержания необходимо собрать URL-адрес для каждого OneDrive для бизнеса сайта, который необходимо поставить на удержание. Затем для каждого пользователя, которые необходимо поставить на удержание, необходимо добавить к удержанию их почтовых ящиков и их OneDrive для бизнеса сайта. В будущих выпусках безопасности &amp; центре соответствия требованиям, будет проще. До тех пор можно использовать сценарий в этой статье для автоматизации этого процесса.
  
Сценарий выдает запрос на имя домена вашей организации MySite (например, **contoso** в URL-адрес https://contoso-my.sharepoint.com), имя существующего случая обнаружения электронных данных, имя нового удержания, связанные с вариантом, список адресов электронной почты пользователей, необходимо Чтобы поместить на удержание и запросов поиска для использования, если вы хотите создать удержание на основе запроса. Сценарий затем возвращает URL-адрес для OneDrive для бизнеса сайтов для каждого пользователя в списке, создает новый удержания и затем добавляет почтовых ящиков и OneDrive для бизнеса узла для каждого пользователя в списке удержания. Скрипт также создает файлы журнала, содержащие сведения о новых удержания. 
  
Далее приведены шаги для этого введите:
  
[Шаг 1. Установка командной консоли SharePoint Online](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[Шаг 2: Создание списка пользователей](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[Шаг 3: Выполните скрипт, чтобы создать удержание и добавление пользователей](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a>Перед началом работы

- Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям и SharePoint Online глобального администратора для запуска сценария в шаге 3. Дополнительные сведения можно [назначать разрешения обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям](assign-ediscovery-permissions.md).
    
- Не более 1 000 почтовых ящиков и 100 сайтов можно добавить к удержанию, связанной с вариантом eDiscovery в системы &amp; центре соответствия требованиям. Если предполагается, что каждый пользователь, который необходимо поставить на удержание имеет OneDrive для бизнеса сайта, не более 100 пользователей можно добавить к удержанию, с помощью скрипта в этой статье. 
    
- Не забудьте сохранить список пользователей, созданные вами в шаге 2 и скрипт в шаге 3 в ту же папку. Который будет упростить выполнение скрипта.
    
- Сценарий добавляет список пользователей в новое удержание, связанный с существующей case. Убедитесь, что, которую требуется связать удержания с создания перед запуском сценария.
    
- Сценарий включает в себя обработка минимальной ошибок. Атрибут предназначен для быстрого и простого помещения почтового ящика и удерживайте OneDrive для бизнеса узла для каждого пользователя.
    
- Примеры скриптов, представленные в этой статье, не поддерживаются ни одной из стандартных программ поддержки или служб Майкрософт. Примеры скриптов предоставляются КАК ЕСТЬ и без каких-либо гарантий. Кроме того, корпорация Майкрософт не дает никаких обязательств в отношении подразумеваемых гарантий, в том числе гарантий товарного качества и пригодности для использования по назначению. Ответственность за риск, возникающий в результате выполнения примеров скриптов и использования документации, полностью возлагается на вас. Корпорация Майкрософт, ее авторы и все, кто принимает участие в создании, подготовке и публикации скриптов, не несут ответственности за какой-либо ущерб (в том числе потерю прибыли предприятия, приостановку его деятельности, потерю бизнес-данных и другой денежный ущерб), вызванный использованием или неспособностью использования примеров скриптов или документации, даже если корпорации Майкрософт было известно о возможности такого ущерба.

## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Шаг 1. Установка командной консоли SharePoint Online

Первым шагом является установка консоли SharePoint Online, если он еще не установлены на локальном компьютере. Использование командной консоли в эту процедуру не требуется, но необходимо установить, так как он содержит необходимые условия, необходимые для сценария, на котором запущен на шаге 3. Эти компоненты позволяют скрипта для взаимодействия с SharePoint Online, чтобы получить URL-адреса для OneDrive для бизнеса сайтов.
  
Перейдите к [настройке среды SharePoint Online Management Shell Windows PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=286318) и выполните шаг 1 и шаг 2 для установки консоли SharePoint Online на локальном компьютере. 

## <a name="step-2-generate-a-list-of-users"></a>Шаг 2: Создание списка пользователей
<a name="step2"> </a>

Скрипт в шаге 3 будет создать удержание, связанной с вариантом eDiscovery и добавить почтовых ящиков и OneDrive для бизнеса сайтов из списка пользователей к удержанию. Можно просто введите адреса электронной почты в текстовом файле или выполнении команды Windows PowerShell, чтобы получить список адресов электронной почты и сохраните их в файл (находится в одной папке, где будут сохранены скрипт, чтобы в шаге 3).
  
Вот команда PowerShell (которую можно запускать с помощью удаленной оболочки PowerShell, подключенных к организации Exchange Online) ознакомьтесь со списком адресов электронной почты для всех пользователей в вашей организации и сохранение его в текстовый файл с именем HoldUsers.txt.
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

После того как, выполните следующую команду, откройте текстовый файл и удалить заголовок, содержащий имя свойства `PrimarySmtpAddress`. Удалите все адреса электронной почты, за исключением из них для пользователей, которые вы хотите добавить к удержанию, которое вы создадите в шаге 3. Убедитесь, что нет ни одной пустой строки до или после список адресов электронной почты.
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a>Шаг 3: Выполните скрипт, чтобы создать удержание и добавление пользователей
<a name="step3"> </a>

При запуске сценария на этом этапе его запросит со следующими сведениями. Убедитесь, что для получения этой информации готов, перед запуском сценария.
  
- **Учетные данные пользователя** - скрипт будет использовать свои учетные данные для подключения к безопасности &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell. Он также будет использовать эти учетные данные для доступа к SharePoint Online, чтобы получить OneDrive для бизнеса URL-адресов для списка пользователей.
    
- **Имя вашего домена MySite** - MySite домена является домен, который содержит все OneDrive для бизнеса сайтов в вашей организации. Например, если URL-адрес для своего домена MySite — **https://contoso-my.sharepoint.com**, а затем введите `contoso` когда будет предложено для имени домена MySite. 
    
- **Имя случая** — имя существующего случая. Скрипт будет создан новый удержания, связанный с этим обращением.
    
- **Имя удержания** - имени удержания скрипт будет создавать и связать с указанным регистр.
    
- **Запрос поиска для запроса на удержание** - можно создать удержание на основе запроса, чтобы только содержимое, удовлетворяющие заданным критериям поиска ставится на удержание. Чтобы поместить все содержимое на удержание, нажмите клавишу **Ввод** , при появлении запроса поиска. 
    
- **Включить удержание или не** - у вас есть сценарий включить удержание после его создания или у вас есть сценарий создания удержания без включения его. Если у вас нет скрипта включить удержание, можно включить его позже в системы &amp; центре соответствия требованиям или, выполнив следующие команды PowerShell: 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- **Имя текстового файла со списком пользователей** — имя текстового файла в шаге 2, который содержит список пользователей для добавления в удержание. Если этот файл находится в той же папке, что и сценарий, просто введите имя файла (например, HoldUsers.txt). Если текстовый файл в другую папку, введите полный путь к файлу.
    
После собранные данные, скрипт будет предложено ввести, последний этап является выполните скрипт, чтобы создать новое удержание и добавление пользователей.
  
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `AddUsersToHold.ps1`.
    
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

2. На локальном компьютере откройте Windows PowerShell и перейдите к папке, в которой вы сохранили скрипт.
    
3. Выполнение скрипта; Например:
    
      ```
    .\AddUsersToHold.ps1
      ```

4. Введите сведения, будет предложено для.
    
    Сценарий подключается к безопасности и соответствия требованиям центр PowerShell и создает новое удержание в случае обнаружения электронных данных и добавляет почтовых ящиков и OneDrive для бизнеса для пользователей в списке. Можно перейти в рамках данного экземпляра на странице **электронных данных** в безопасности &amp; центре соответствия требованиям для просмотра новое удержание. 
    
После завершения скрипта под управлением, он создает следующие файлы журналов и сохраняет их в папку, где находится скрипта.
  
- **LocationsOnHold.txt** - содержит список почтовых ящиков и OneDrive для бизнеса сайтов, сценарий успешно помещенных на удержание.
    
- **LocationsNotOnHold.txt** - содержит список почтовых ящиков и OneDrive для бизнеса сайтов, сценарий не было поставить на удержание. Если пользователь имеет почтовый ящик, но не OneDrive для бизнеса сайта, пользователь будет включены в список OneDrive для бизнеса сайты, которые не были помещенные на удержание.
    
- **GetCaseHoldPolicy.txt** - содержит выходные данные командлета **Get-CaseHoldPolicy** для новых удержания сценарий выполняется после создания нового удержания. Данные, возвращенные с помощью этого командлета содержит список пользователей, чьи почтовые ящики и OneDrive для бизнеса сайтов находятся на удержании и включение или отключение удержания. 
    
- **GetCaseHoldRule.txt** - содержит выходные данные командлета **Get-CaseHoldRule** для новых удержания сценарий выполняется после создания нового удержания. Сведения, возвращаемые этот командлет включает поисковый запрос, если скрипт используется для создания запроса на удержание. 
