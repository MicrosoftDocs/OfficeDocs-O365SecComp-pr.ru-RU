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
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a><span data-ttu-id="902e6-103">Получение сведений об устройствах, управляемых Mobile Device Management (MDM) для Office 365</span><span class="sxs-lookup"><span data-stu-id="902e6-103">Get details about devices managed by Mobile Device Management (MDM) for Office 365</span></span>

<span data-ttu-id="902e6-104">В этой статье показано, как использовать Windows PowerShell для получения сведений об устройствах в вашей организации, которые можно настроить для мобильного устройства управления для Office 365.</span><span class="sxs-lookup"><span data-stu-id="902e6-104">This article shows you how to use Windows PowerShell to get details about the devices in your organization that you set up for Mobile Device Management for Office 365.</span></span> 
  
## <a name="what-device-details-can-i-get"></a><span data-ttu-id="902e6-105">Какие сведений об устройстве можно получить?</span><span class="sxs-lookup"><span data-stu-id="902e6-105">What device details can I get?</span></span>

<span data-ttu-id="902e6-106">Ниже представлена классификация.</span><span class="sxs-lookup"><span data-stu-id="902e6-106">Here's a breakdown.</span></span>
  
|<span data-ttu-id="902e6-107">**Подробности**</span><span class="sxs-lookup"><span data-stu-id="902e6-107">**Detail**</span></span>|<span data-ttu-id="902e6-108">**Что следует искать в PowerShell**</span><span class="sxs-lookup"><span data-stu-id="902e6-108">**What to look for in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="902e6-109">Устройство является [участвуют в MDM для Office 365](enroll-your-mobile-device.md)</span><span class="sxs-lookup"><span data-stu-id="902e6-109">Device is [enrolled in MDM for Office 365](enroll-your-mobile-device.md)</span></span> <br/> |<span data-ttu-id="902e6-110">Значение параметра *isManaged* — это:</span><span class="sxs-lookup"><span data-stu-id="902e6-110">The value of the  *isManaged*  parameter is:</span></span>  <br/> <span data-ttu-id="902e6-111">**Значение true,** = регистрации устройство.</span><span class="sxs-lookup"><span data-stu-id="902e6-111">**True** = device is enrolled.</span></span>  <br/> <span data-ttu-id="902e6-112">**False** = не участвуют устройства.</span><span class="sxs-lookup"><span data-stu-id="902e6-112">**False** = device is not enrolled.</span></span>  <br/> |
|<span data-ttu-id="902e6-113">Устройства совместим с вашей [политики безопасности устройств](https://go.microsoft.com/fwlink/?linkid=615144)</span><span class="sxs-lookup"><span data-stu-id="902e6-113">Device is compliant with your [device security policies](https://go.microsoft.com/fwlink/?linkid=615144)</span></span> <br/> |<span data-ttu-id="902e6-114">Значение параметра *isCompliant* — это:</span><span class="sxs-lookup"><span data-stu-id="902e6-114">The value of the  *isCompliant*  parameter is:</span></span>  <br/> <span data-ttu-id="902e6-115">**Значение true,** = устройства политикам.</span><span class="sxs-lookup"><span data-stu-id="902e6-115">**True** = device is compliant with policies.</span></span>  <br/> <span data-ttu-id="902e6-116">**False** = устройства несовместим с политиками.</span><span class="sxs-lookup"><span data-stu-id="902e6-116">**False** = device is not compliant with policies.</span></span>  <br/> |
   
![Отображение значения параметров командной консоли AAD ли участвуют устройств и жалоб потока](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> <span data-ttu-id="902e6-118">Команды и сценарии в этой статье также возвращает подробные сведения о всех устройств, которые управляют [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune).</span><span class="sxs-lookup"><span data-stu-id="902e6-118">The commands and scripts in this article will also return details about any devices that are managed by [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="902e6-119">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="902e6-119">Before you begin</span></span>

<span data-ttu-id="902e6-120">Существует несколько вещей, которые необходимо настроить для выполнения команд и сценарии, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="902e6-120">There are a few things you'll need to set up to run the commands and scripts described in this article.</span></span>
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="902e6-121">Шаг 1: Загрузите и установите Azure модуль Active Directory для Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="902e6-121">Step 1: Download and install the Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="902e6-122">Дополнительные сведения о эти действия в разделе [подключение к Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="902e6-122">For more info on these steps, see [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span></span>
  
1. <span data-ttu-id="902e6-123">Перейдите к [Microsoft Online Services помощника по входу для ИТ профессионалов RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) и нажмите кнопку **загрузки** для Microsoft Online Services помощник по входу.</span><span class="sxs-lookup"><span data-stu-id="902e6-123">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) and click **Download** for Microsoft Online Services Sign-in Assistant.</span></span> 
    
2. <span data-ttu-id="902e6-124">Чтобы установить модуль Microsoft Azure Active Directory для Windows PowerShell, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="902e6-124">Install the Microsoft Azure Active Directory Module for Windows PowerShell with these steps:</span></span>
    
    1. <span data-ttu-id="902e6-125">Откройте командную строку для уровня администратора PowerShell.</span><span class="sxs-lookup"><span data-stu-id="902e6-125">Open an administrator-level PowerShell command prompt.</span></span>
        
    2. <span data-ttu-id="902e6-126">Запустите `Install-Module MSOnline` команды.</span><span class="sxs-lookup"><span data-stu-id="902e6-126">Run the `Install-Module MSOnline` command.</span></span>
        
    3. <span data-ttu-id="902e6-127">Если запрос на установку поставщика NuGet введите `Y` и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="902e6-127">If prompted to install the NuGet provider, type `Y` and press ENTER.</span></span>
        
    4. <span data-ttu-id="902e6-128">Если запрос на установку модуля из PSGallery, введите `Y` и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="902e6-128">If prompted to install the module from PSGallery, type `Y` and press ENTER.</span></span>
        
    5. <span data-ttu-id="902e6-129">После установки закройте командное окно PowerShell.</span><span class="sxs-lookup"><span data-stu-id="902e6-129">After installation, close the PowerShell command window.</span></span>
    
### <a name="step-2-connect-to-your-office-365-subscription"></a><span data-ttu-id="902e6-130">Шаг 2. Подключитесь к своей подписке Office 365</span><span class="sxs-lookup"><span data-stu-id="902e6-130">Step 2: Connect to your Office 365 subscription</span></span>

1. <span data-ttu-id="902e6-131">В Windows Azure модуль Active Directory для Windows PowerShell выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="902e6-131">In the Windows Azure Active Directory Module for Windows PowerShell, run the following command.</span></span><br/>  
  `$UserCredential = Get-Credential`

2. <span data-ttu-id="902e6-132">В диалоговом окне **Запрос учетных данных Windows PowerShell** введите имя пользователя и пароль для учетной записи глобального администратора Office 365 и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="902e6-132">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global admin account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="902e6-133">Выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="902e6-133">Run the following command.</span></span><br/>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a><span data-ttu-id="902e6-134">Шаг 3: Убедитесь, что вы сможете продолжить выполнение скриптов PowerShell</span><span class="sxs-lookup"><span data-stu-id="902e6-134">Step 3: Make sure you're able to run PowerShell scripts</span></span>

> [!NOTE]
> <span data-ttu-id="902e6-135">Этот шаг можно пропустить, если вы будете уже настроен для запуска скриптов PowerShell.</span><span class="sxs-lookup"><span data-stu-id="902e6-135">You can skip this step if you're already set up to run PowerShell scripts.</span></span> 
  
<span data-ttu-id="902e6-136">Чтобы запустить сценарий **Get-MsolUserDeviceComplianceStatus.ps1** , необходимо разрешить выполнение сценариев PowerShell.</span><span class="sxs-lookup"><span data-stu-id="902e6-136">To run the **Get-MsolUserDeviceComplianceStatus.ps1** script, you need to enable the running of PowerShell scripts.</span></span> 
  
1. <span data-ttu-id="902e6-p101">На рабочем столе Windows нажмите кнопку **Пуск**и затем введите Windows PowerShell. Щелкните правой кнопкой мыши **Windows PowerShell**и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="902e6-p101">From your Windows Desktop, click **Start**, and then type Windows PowerShell. Right click **Windows PowerShell**, and then click **Run as administrator**.</span></span>
    
2. <span data-ttu-id="902e6-139">Выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="902e6-139">Run the following command.</span></span><br/>
  `Set-ExecutionPolicy RemoteSigned`

3. <span data-ttu-id="902e6-140">При появлении запроса введите `Y` и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="902e6-140">When prompted, type `Y` and then press Enter.</span></span> 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a><span data-ttu-id="902e6-141">Выполните командлет Get-MsolDevice, чтобы отобразить подробные сведения для всех устройств в вашей организации</span><span class="sxs-lookup"><span data-stu-id="902e6-141">Run the Get-MsolDevice cmdlet to display details for all devices in your organization</span></span>

1. <span data-ttu-id="902e6-142">Откройте модуль Microsoft Azure Active Directory для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="902e6-142">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="902e6-143">Выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="902e6-143">Run the following command.</span></span><br/>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

<span data-ttu-id="902e6-144">Дополнительные примеры [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)см.</span><span class="sxs-lookup"><span data-stu-id="902e6-144">For more examples, see [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).</span></span>
  
## <a name="run-a-script-to-get-device-details"></a><span data-ttu-id="902e6-145">Выполнение скрипта для получения сведений об устройстве</span><span class="sxs-lookup"><span data-stu-id="902e6-145">Run a script to get device details</span></span>

### <a name="first-save-the-script-to-your-computer"></a><span data-ttu-id="902e6-146">Во-первых Сохраните скрипт на своем компьютере</span><span class="sxs-lookup"><span data-stu-id="902e6-146">First, save the script to your computer</span></span>

1. <span data-ttu-id="902e6-147">Скопируйте и вставьте следующий текст в "Блокнот".</span><span class="sxs-lookup"><span data-stu-id="902e6-147">Copy and paste the following text into Notepad.</span></span><br/> 
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

2. <span data-ttu-id="902e6-148">Сохраните его как файл сценария Windows PowerShell с помощью файла расширением **.ps1**.</span><span class="sxs-lookup"><span data-stu-id="902e6-148">Save it as a Windows PowerShell script file by using the file extension **.ps1**.</span></span> <br/><span data-ttu-id="902e6-149">Пример.</span><span class="sxs-lookup"><span data-stu-id="902e6-149">Example:</span></span><br/> <span data-ttu-id="902e6-150">`Get-MsolUserDeviceComplianceStatus.ps1`.</span><span class="sxs-lookup"><span data-stu-id="902e6-150"></span></span>
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a><span data-ttu-id="902e6-151">Выполните скрипт, чтобы получить сведения об устройстве для одной учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="902e6-151">Run the script to get device information for a single user account</span></span>

1. <span data-ttu-id="902e6-152">Откройте модуль Microsoft Azure Active Directory для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="902e6-152">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="902e6-p102">Перейдите к папке, в которой вы сохранили скрипт. Например если он был сохранен на C:\PS-Scripts, будет выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="902e6-p102">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span><br/>
    `cd C:\PS-Scripts`

3. <span data-ttu-id="902e6-p103">Выполните следующую команду для идентификации пользователя, для получения сведений об устройстве для. В этом примере выводятся сведения для bar@example.com.</span><span class="sxs-lookup"><span data-stu-id="902e6-p103">Run the following command to identify the user you want to get device details for. This example gets details for bar@example.com.</span></span><br/>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. <span data-ttu-id="902e6-157">Выполните следующую команду, чтобы запустить сценарий.</span><span class="sxs-lookup"><span data-stu-id="902e6-157">Run the following command to initiate the script.</span></span><br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="902e6-p104">Сведения экспортируется в CSV-файл на рабочем столе Windows. Чтобы указать имя файла и путь к CSV можно использовать дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="902e6-p104">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a><span data-ttu-id="902e6-160">Выполните скрипт, чтобы получить сведения об устройстве для группы пользователей</span><span class="sxs-lookup"><span data-stu-id="902e6-160">Run the script to get device information for a group of users</span></span>

1. <span data-ttu-id="902e6-161">Откройте модуль Microsoft Azure Active Directory для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="902e6-161">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="902e6-p105">Перейдите к папке, в которой вы сохранили скрипт. Например если он был сохранен на C:\PS-Scripts, будет выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="902e6-p105">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span><br/>
  `cd C:\PS-Scripts`

3. <span data-ttu-id="902e6-p106">Выполните следующую команду, чтобы указать группу, для получения сведений об устройстве для. В этом примере выводятся сведения для пользователей в группу FinanceStaff.</span><span class="sxs-lookup"><span data-stu-id="902e6-p106">Run the following command to identify the group you want to get device details for. This example gets details for users in the FinanceStaff group.</span></span><br/>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. <span data-ttu-id="902e6-166">Выполните следующую команду, чтобы запустить сценарий.</span><span class="sxs-lookup"><span data-stu-id="902e6-166">Run the following command to initiate the script.</span></span><br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="902e6-p107">Сведения экспортируется в CSV-файл на рабочем столе Windows. Чтобы указать имя файла и путь к CSV можно использовать дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="902e6-p107">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
## <a name="more-info"></a><span data-ttu-id="902e6-169">Больше информации</span><span class="sxs-lookup"><span data-stu-id="902e6-169">More info</span></span>

[<span data-ttu-id="902e6-170">Общие сведения о MDM для Office 365</span><span class="sxs-lookup"><span data-stu-id="902e6-170">Overview of MDM for Office 365</span></span>](overview-of-mdm.md)
  
[<span data-ttu-id="902e6-171">Get-MsolDevice</span><span class="sxs-lookup"><span data-stu-id="902e6-171">Get-MsolDevice</span></span>](https://go.microsoft.com/fwlink/?linkid=841721)
  

