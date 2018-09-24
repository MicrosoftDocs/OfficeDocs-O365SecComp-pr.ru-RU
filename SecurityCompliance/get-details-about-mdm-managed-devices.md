---
title: Получение сведений об устройствах, управляемых Mobile Device Management (MDM) для Office 365
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MBS150
- MET150
ms.assetid: 5602963c-a1f2-4c21-afb9-f66cd7dca1f0
description: В этой статье показано, как использовать Windows PowerShell для получения сведений об устройствах в вашей организации, которые можно настроить для мобильного устройства управления для Office 365.
ms.openlocfilehash: 90ee59c5afed1cd260e13134299a7cb4f17dc5bc
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972321"
---
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a>Получение сведений об устройствах, управляемых Mobile Device Management (MDM) для Office 365

В этой статье показано, как использовать Windows PowerShell для получения сведений об устройствах в вашей организации, которые можно настроить для мобильного устройства управления для Office 365. 
  
## <a name="what-device-details-can-i-get"></a>Какие сведений об устройстве можно получить?

Ниже представлена классификация.
  
|**Подробности**|**Что следует искать в PowerShell**|
|:-----|:-----|
|Устройство является [участвуют в MDM для Office 365](enroll-your-mobile-device.md) <br/> |Значение параметра *isManaged* — это:  <br/> **Значение true,** = регистрации устройство.  <br/> **False** = не участвуют устройства.  <br/> |
|Устройства совместим с вашей [политики безопасности устройств](https://go.microsoft.com/fwlink/?linkid=615144) <br/> |Значение параметра *isCompliant* — это:  <br/> **Значение true,** = устройства политикам.  <br/> **False** = устройства несовместим с политиками.  <br/> |
   
![Отображение значения параметров командной консоли AAD ли участвуют устройств и жалоб потока](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> Команды и сценарии в этой статье также возвращает подробные сведения о всех устройств, которые управляют [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune). 
  
## <a name="before-you-begin"></a>Перед началом работы

Существует несколько вещей, которые необходимо настроить для выполнения команд и сценарии, описанные в этой статье.
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a>Шаг 1: Загрузите и установите Azure модуль Active Directory для Windows PowerShell

Дополнительные сведения о эти действия в разделе [подключение к Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).
  
1. Перейдите к [Microsoft Online Services помощника по входу для ИТ профессионалов RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) и нажмите кнопку **загрузки** для Microsoft Online Services помощник по входу. 
    
2. Чтобы установить модуль Microsoft Azure Active Directory для Windows PowerShell, сделайте следующее:
    
    1. Откройте командную строку для уровня администратора PowerShell.
        
    2. Запустите `Install-Module MSOnline` команды.
        
    3. Если запрос на установку поставщика NuGet введите `Y` и нажмите клавишу ВВОД.
        
    4. Если запрос на установку модуля из PSGallery, введите `Y` и нажмите клавишу ВВОД.
        
    5. После установки закройте командное окно PowerShell.
    
### <a name="step-2-connect-to-your-office-365-subscription"></a>Шаг 2. Подключитесь к своей подписке Office 365

1. В Windows Azure модуль Active Directory для Windows PowerShell выполните следующую команду.<br/>  
  `$UserCredential = Get-Credential`

2. В диалоговом окне **Запрос учетных данных Windows PowerShell** введите имя пользователя и пароль для учетной записи глобального администратора Office 365 и нажмите кнопку **ОК**.
    
3. Выполните следующую команду.<br/>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a>Шаг 3: Убедитесь, что вы сможете продолжить выполнение скриптов PowerShell

> [!NOTE]
> Этот шаг можно пропустить, если вы будете уже настроен для запуска скриптов PowerShell. 
  
Чтобы запустить сценарий **Get-MsolUserDeviceComplianceStatus.ps1** , необходимо разрешить выполнение сценариев PowerShell. 
  
1. На рабочем столе Windows нажмите кнопку **Пуск**и затем введите Windows PowerShell. Щелкните правой кнопкой мыши **Windows PowerShell**и выберите команду **Запуск от имени администратора**.
    
2. Выполните следующую команду.<br/>
  `Set-ExecutionPolicy RemoteSigned`

3. При появлении запроса введите `Y` и нажмите клавишу ВВОД. 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a>Выполните командлет Get-MsolDevice, чтобы отобразить подробные сведения для всех устройств в вашей организации

1. Откройте модуль Microsoft Azure Active Directory для Windows PowerShell.
    
2. Выполните следующую команду.<br/>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

Дополнительные примеры [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)см.
  
## <a name="run-a-script-to-get-device-details"></a>Выполнение скрипта для получения сведений об устройстве

### <a name="first-save-the-script-to-your-computer"></a>Во-первых Сохраните скрипт на своем компьютере

1. Скопируйте и вставьте следующий текст в "Блокнот".<br/> 
  ```
  param (
      [PSObject[]]$users = @(),
      [Switch]$export,
      [String]$exportFileName = "UserDeviceComplianceStatus_" + (Get-Date -Format "yyMMdd_HHMMss") + ".csv",
      [String]$exportPath = [Environment]::GetFolderPath("Desktop")
   )
  [System.Collections.IDictionary]$script:schema = @{
      
      DeviceId = ''
      DeviceOSType = ''
      DeviceOSVersion = ''
      DeviceTrustLevel = ''
      DisplayName = ''
      IsCompliant = ''
      IsManaged = ''
      ApproximateLastLogonTimestamp = ''
      DeviceObjectId = ''    
      RegisteredOwnerUpn = ''
      RegisteredOwnerObjectId = ''
      RegisteredOwnerDisplayName = ''
  }
  function createResultObject
  {
      [PSObject]$resultObject = New-Object -TypeName PSObject -Property $script:schema
      return $resultObject
  }
  If ($users.Count -eq 0)
  {
      $users = Get-MsolUser
  }
  [PSObject[]]$result = foreach ($u in $users)
  {
      
      [PSObject]$devices = get-msoldevice -RegisteredOwnerUpn $u.UserPrincipalName
      foreach ($d in $devices)
      {
          [PSObject]$deviceResult = createResultObject
          $deviceResult.DeviceId = $d.DeviceId 
          $deviceResult.DeviceOSType = $d.DeviceOSType 
          $deviceResult.DeviceOSVersion = $d.DeviceOSVersion 
          $deviceResult.DeviceTrustLevel = $d.DeviceTrustLevel
          $deviceResult.DisplayName = $d.DisplayName
          $deviceResult.IsCompliant = $d.GraphDeviceObject.IsCompliant
          $deviceResult.IsManaged = $d.GraphDeviceObject.IsManaged
          $deviceResult.DeviceObjectId = $d.ObjectId
          $deviceResult.RegisteredOwnerUpn = $u.UserPrincipalName
          $deviceResult.RegisteredOwnerObjectId = $u.ObjectId
          $deviceResult.RegisteredOwnerDisplayName = $u.DisplayName
          $deviceResult.ApproximateLastLogonTimestamp = $d.ApproximateLastLogonTimestamp
          $deviceResult
      }
  }
  If ($export)
  {
      $result | Export-Csv -path ($exportPath + "\" + $exportFileName) -NoTypeInformation
  }
  Else
  {
      $result
  }
  
  ```

2. Сохраните его как файл сценария Windows PowerShell с помощью файла расширением **.ps1**. <br/>Пример.<br/> `Get-MsolUserDeviceComplianceStatus.ps1`.
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a>Выполните скрипт, чтобы получить сведения об устройстве для одной учетной записи пользователя

1. Откройте модуль Microsoft Azure Active Directory для Windows PowerShell.
    
2. Перейдите к папке, в которой вы сохранили скрипт. Например если он был сохранен на C:\PS-Scripts, будет выполните следующую команду.<br/>
    `cd C:\PS-Scripts`

3. Выполните следующую команду для идентификации пользователя, для получения сведений об устройстве для. В этом примере выводятся сведения для bar@example.com.<br/>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. Выполните следующую команду, чтобы запустить сценарий.<br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

Сведения экспортируется в CSV-файл на рабочем столе Windows. Чтобы указать имя файла и путь к CSV можно использовать дополнительные параметры.
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a>Выполните скрипт, чтобы получить сведения об устройстве для группы пользователей

1. Откройте модуль Microsoft Azure Active Directory для Windows PowerShell.
    
2. Перейдите к папке, в которой вы сохранили скрипт. Например если он был сохранен на C:\PS-Scripts, будет выполните следующую команду.<br/>
  `cd C:\PS-Scripts`

3. Выполните следующую команду, чтобы указать группу, для получения сведений об устройстве для. В этом примере выводятся сведения для пользователей в группу FinanceStaff.<br/>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. Выполните следующую команду, чтобы запустить сценарий.<br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

Сведения экспортируется в CSV-файл на рабочем столе Windows. Чтобы указать имя файла и путь к CSV можно использовать дополнительные параметры.
  
## <a name="more-info"></a>Больше информации

[Общие сведения о MDM для Office 365](overview-of-mdm.md)
  
[Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)
  

