---
title: Создание отчета на удержаний в вариантах eDiscovery в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: Создать отчет, содержащий сведения о всех удержаний, связанных с вариантах eDiscovery безопасности Office 365 с помощью сценария в этой статье &amp; центре соответствия требованиям.
ms.openlocfilehash: b6cef2824002d7e45e4f500bc6c1e9bc880cbd41
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038212"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a>Создание отчета на удержаний в вариантах eDiscovery в Office 365
  
Скрипт в этой статье позволяет администраторам обнаружения электронных данных и диспетчеры обнаружения электронных данных создать отчет, содержащий сведения о всех удержаний, связанных с вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям. Отчет содержит сведения, такие как имя случая удержания связан с размещения содержимого, помещенные на удержание и удержания на основе запроса. Если случаев, которые не имеют все удержаний, скрипт будет создание отчета дополнительные со списком случаев без удержаний.

Подробное описание данных, включаемых в отчет в разделе [Дополнительные сведения](#more-information) . 
  
## <a name="before-you-begin"></a>Перед началом работы

- Чтобы создать отчет о всех случаев обнаружения в вашей организации, необходимо быть eDiscovery администратора в вашей организации. Если вы являетесь диспетчеру eDiscovery, отчет будет содержать только сведения о вариантах, которые могут получить доступ к. Дополнительные сведения о разрешениях обнаружения электронных данных можно [назначать разрешения обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям](assign-ediscovery-permissions.md).
    
- Скрипт в этой статье имеет обработка минимальной ошибок. Основной целью — для быстрого создания отчета об удержаниях, связанных с вариантах eDiscovery в вашей организации.
    
- Примеры скриптов, представленные в этой статье, не поддерживаются ни одной из стандартных программ поддержки или служб Майкрософт. Примеры скриптов предоставляются КАК ЕСТЬ и без каких-либо гарантий. Кроме того, корпорация Майкрософт не дает никаких обязательств в отношении подразумеваемых гарантий, в том числе гарантий товарного качества и пригодности для использования по назначению. Ответственность за риск, возникающий в результате выполнения примеров скриптов и использования документации, полностью возлагается на вас. Корпорация Майкрософт, ее авторы и все, кто принимает участие в создании, подготовке и публикации скриптов, не несут ответственности за какой-либо ущерб (в том числе потерю прибыли предприятия, приостановку его деятельности, потерю бизнес-данных и другой денежный ущерб), вызванный использованием или неспособностью использования примеров скриптов или документации, даже если корпорации Майкрософт было известно о возможности такого ущерба.
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a>Шаг 1: Подключение к безопасности &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell

Первым шагом является подключение Windows PowerShell для защиты &amp; центре соответствия требованиям для вашей организации.
  
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `ConnectSCC.ps1`. 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. На локальном компьютере откройте Windows PowerShell и перейдите к папке, в которой вы сохранили скрипт. 
    
3. Выполнение скрипта; Например:

    ```
    .\ConnectSCC.ps1
    ```
   
4. Когда требуется ввести учетные данные, введите адрес электронной почты и пароль и нажмите кнопку **ОК**. 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a>Шаг 2: Запустите сценарий для создания отчетов о содержит связанный с вариантах eDiscovery

После подключения к безопасности &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell, следующим шагом является создание и выполнение сценария, который собирает сведения о вариантах eDiscovery в вашей организации. 
  
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; Например CaseHoldsReport.ps1. 
    
  ```
#script begin
" " 
write-host "***********************************************"
write-host "   Office 365 Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
write-host "        eDiscovery cases - Holds report         " -foregroundColor yellow -backgroundcolor darkgreen 
write-host "***********************************************"
" " 
#prompt users to specify a path to store the output files
$time=get-date
$Path = Read-Host 'Enter a file path to save the report to a .csv file'
$outputpath=$Path+'\'+'CaseHoldsReport'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
$noholdsfilepath=$Path+'\'+'CaseswithNoHolds'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
#add case details to the csv file
function add-tocasereport{
Param([string]$casename,
[String]$casestatus,
[datetime]$casecreatedtime,
[string]$casemembers,
[datetime]$caseClosedDateTime,
[string]$caseclosedby,
[string]$holdname,
[String]$Holdenabled,
[string]$holdcreatedby,
[string]$holdlastmodifiedby,
[string]$ExchangeLocation,
[string]$sharePointlocation,
[string]$ContentMatchQuery,
[datetime]$holdcreatedtime,
[datetime]$holdchangedtime
)
$addRow = New-Object PSObject 
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case name" -Value $casename
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case status" -Value $casestatus
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case members" -Value $casemembers
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case created time" -Value $casecreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed time" -Value $caseClosedDateTime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed by" -Value $caseclosedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold name" -Value $holdname
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold enabled" -Value $Holdenabled
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created by" -Value $holdcreatedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold last changed by" -Value $holdlastmodifiedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Exchange locations" -Value  $ExchangeLocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "SharePoint locations" -Value $sharePointlocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold query" -Value $ContentMatchQuery
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created time (UTC)" -Value $holdcreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold changed time (UTC)" -Value $holdchangedtime
$allholdreport = $addRow | Select-Object "Case name","Case status","Hold name","Hold enabled","Case members", "Case created time","Case closed time","Case closed by","Exchange locations","SharePoint locations","Hold query","Hold created by","Hold created time (UTC)","Hold last changed by","Hold changed time (UTC)"
$allholdreport | export-csv -path $outputPath -notypeinfo -append -Encoding ascii 
}
#get information on the cases and pass values to the case report function
" "
write-host "Gathering a list of cases and holds..."
" "
$edc =Get-ComplianceCase -ErrorAction SilentlyContinue
foreach($cc in $edc)
{
write-host "Working on case :" $cc.name
if($cc.status -eq 'Closed')
{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
add-tocasereport -casename $cc.name -casestatus $cc.Status -caseclosedby $cc.closedby -caseClosedDateTime $cc.ClosedDateTime -casemembers $cmembers 
}
else{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
$policies = Get-CaseHoldPolicy -Case $cc.Name | %{ Get-CaseHoldPolicy $_.Name -Case $_.CaseId -DistributionDetail}
if ($policies -ne $NULL)
{
foreach ($policy in $policies)
{
$rule=Get-CaseHoldRule -Policy $policy.name
add-tocasereport -casename $cc.name -casemembers $cmembers -casestatus $cc.Status -casecreatedtime $cc.CreatedDateTime -holdname $policy.name -holdenabled $policy.enabled -holdcreatedby $policy.CreatedBy -holdlastmodifiedby $policy.LastModifiedBy -ExchangeLocation (($policy.exchangelocation.name)-join ';') -SharePointLocation (($policy.sharePointlocation.name)-join ';') -ContentMatchQuery $rule.ContentMatchQuery -holdcreatedtime $policy.WhenCreatedUTC -holdchangedtime $policy.WhenChangedUTC
}
}
else{
write-host "No hold policies found in case:" $cc.name -foregroundColor 'Yellow'
" "
[string]$cc.name | out-file -filepath $noholdsfilepath -append 
}
}
}

" "
Write-host "Script complete! Report files saved to this folder: '$Path'"
" "
#script end
  ```

2. Во время сеанса Windows PowerShell, которая открыта в шаге 1 Перейдите к папке, в которой вы сохранили скрипт. 
    
3. Выполнение скрипта; Например:

    ```
    .\CaseHoldsReport.ps1
    ```

    Сценарий выводит запрос, папку назначения для сохранения в отчете. 
    
4. Введите полный путь к папке для сохранения в отчете и нажмите клавишу **Ввод**.
    
    > [!TIP]
    > Чтобы сохранить отчет в той же папке, размещенной в скрипт, введите точку (".») при появлении запроса папку назначения. Для сохранения отчета во вложенной папке в папке, где расположена скрипт, просто введите имя вложенной папке. 
  
    Сценарий начинает сбор сведений о всех случаев обнаружения в вашей организации. Нет доступа к файлу отчета во время выполнения скрипта. После завершения скрипта сообщение с подтверждением отображается в сеанса Windows PowerShell. После данное сообщение, можно обращаться к отчет в папке, указанной на шаге 4. — Это имя файла для отчета `CaseHoldsReport<DateTimeStamp>.csv`.

    Addtionally, сценарий также создает отчет со списком случаев, которые не имеют все удержаний. — Это имя файла для этого отчета `CaseswithNoHolds<DateTimeStamp>.csv`.
    
    Ниже приведен пример выполнения скрипта CaseHoldsReport.ps1. 
    
    ![После запуска сценария CaseHoldsReport.ps1 выходных данных](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a>Дополнительные сведения

Регистр содержит отчета, который создается при запуске сценария в этой статье содержатся следующие сведения о каждом удержания. Как объяснялось ранее необходимо быть eDiscovery администратору, чтобы получить сведения обо всех удержаний в вашей организации. Содержит дополнительные сведения о case см [вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям](ediscovery-cases.md).
  
  - Имя удержания и имя случая обнаружения электронных данных, с которым связана удержания.
    
  - Ли случая обнаружения электронных данных является активным или закрытой.
    
  - Ли удержание включена или отключена.
    
  - Члены случая обнаружения электронных данных, с которым связана удержания. Case элементы можно просмотреть или изменить дела, в зависимости от разрешения обнаружения электронных данных, которые они были назначены.
    
  - Время и Дата создания обращения.
    
  - При закрытии обращения человека, который закрыть его и время и дата его было закрыто.
    
  - Почтовые ящики Exchange и SharePoint узлы расположения, которые находятся на удержании.
    
  - Если удержание на основе запроса, синтаксис запроса.
    
  - Время и Дата создания удержания и человека, создавшего его.
    
  - Время и Дата последнего изменения удержания и пользователя, который изменил его.
