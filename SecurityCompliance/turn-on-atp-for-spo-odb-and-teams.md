---
title: Включение Office 365 ATP для SharePoint, OneDrive и Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection:
- M365-security-compliance
description: Узнайте, как включить ATP для SharePoint, OneDrive и Teams, включая настройку оповещений для обнаруженных файлов.
ms.openlocfilehash: 30eb28bfc5156664656ca1c200f9e999661b3b0c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264309"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="191c8-103">Включение Office 365 ATP для SharePoint, OneDrive и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="191c8-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="191c8-104">[Office 365 ATP для SharePoint, OneDrive и Microsoft Teams](atp-for-spo-odb-and-teams.md) защищает организацию от случайного предоставления вредоносных файлов.</span><span class="sxs-lookup"><span data-stu-id="191c8-104">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files.</span></span> <span data-ttu-id="191c8-105">При обнаружении вредоносного файла этот файл блокируется, чтобы никто не мог открыть, скопировать, переместить или предоставить к нему общий доступ до тех пор, пока не будут предприняты дальнейшие действия группы безопасности Организации.</span><span class="sxs-lookup"><span data-stu-id="191c8-105">When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team.</span></span> <span data-ttu-id="191c8-106">В этой статье описано, как включить ATP для SharePoint, OneDrive и Teams, настроить оповещения о обнаруженных файлах и выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="191c8-106">Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
<span data-ttu-id="191c8-107">Для определения (или изменения) политик ATP необходимо назначить соответствующую роль.</span><span class="sxs-lookup"><span data-stu-id="191c8-107">To define (or edit) ATP policies, you must be assigned an appropriate role.</span></span> <span data-ttu-id="191c8-108">Некоторые примеры описаны в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="191c8-108">Some examples are described in the following table:</span></span>

|<span data-ttu-id="191c8-109">Role</span><span class="sxs-lookup"><span data-stu-id="191c8-109">Role</span></span>  |<span data-ttu-id="191c8-110">Где/как назначено</span><span class="sxs-lookup"><span data-stu-id="191c8-110">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="191c8-111">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="191c8-111">Office 365 Global Administrator</span></span> |<span data-ttu-id="191c8-112">Пользователь, который подписывается на приобретение Office 365, по умолчанию является глобальным администратором.</span><span class="sxs-lookup"><span data-stu-id="191c8-112">The person who signs up to buy Office 365 is a global admin by default.</span></span> <span data-ttu-id="191c8-113">(Чтобы узнать больше, ознакомьтесь со статьей [о ролях администратора Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)</span><span class="sxs-lookup"><span data-stu-id="191c8-113">(See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="191c8-114">администратор безопасности (Security Administrator).</span><span class="sxs-lookup"><span data-stu-id="191c8-114">Security Administrator</span></span> |<span data-ttu-id="191c8-115">Центр администрирования Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="191c8-115">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="191c8-116">Управление организацией Exchange Online</span><span class="sxs-lookup"><span data-stu-id="191c8-116">Exchange Online Organization Management</span></span> |<span data-ttu-id="191c8-117">Центр администрирования Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="191c8-117">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="191c8-118">Кроме того:</span><span class="sxs-lookup"><span data-stu-id="191c8-118">or</span></span> <br>  <span data-ttu-id="191c8-119">Командлеты PowerShell (см. [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="191c8-119">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="191c8-120">Включение ATP для SharePoint, OneDrive и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="191c8-120">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="191c8-121">**Прежде чем приступить к этой процедуре, убедитесь, что ведение журнала аудита для вашей среды Office 365 уже включено**.</span><span class="sxs-lookup"><span data-stu-id="191c8-121">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**.</span></span> <span data-ttu-id="191c8-122">Это обычно делается для пользователей, которым назначена роль "журналы аудита" в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="191c8-122">This is typically done by someone who has the Audit Logs role assigned in Exchange Online.</span></span> <span data-ttu-id="191c8-123">Дополнительную информацию можно узнать [в статье Включение и отключение поиска в журнале аудита Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="191c8-123">For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="191c8-124">Перейдите на [https://protection.office.com](https://protection.office.com)страницу и войдите с помощью рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="191c8-124">Go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="191c8-125">в центре &amp; безопасности и соответствия требованиям Office 365 в области навигации слева в разделе **управление угрозами**выберите пункт **безопасные вложения** **политики** \> .</span><span class="sxs-lookup"><span data-stu-id="191c8-125">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span> <br/><span data-ttu-id="191c8-126">![В центре безопасности &amp; и соответствия требованиям выберите Политика управления \> угрозами](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span><span class="sxs-lookup"><span data-stu-id="191c8-126">![In the Security &amp; Compliance Center, choose Threat management \> Policy](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)</span></span>
  
3. <span data-ttu-id="191c8-127">Выберите **включить ATP для SharePoint, OneDrive и Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="191c8-127">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span><br/><span data-ttu-id="191c8-128">![Включение расширенной защиты от угроз для SharePoint Online, OneDrive для бизнеса и Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span><span class="sxs-lookup"><span data-stu-id="191c8-128">![Turn on Advanced Threat Protection for SharePoint Online, OneDrive for Business, and Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)</span></span>
  
4. <span data-ttu-id="191c8-129">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="191c8-129">Click **Save**.</span></span>
    
5. <span data-ttu-id="191c8-130">Просмотрите (и, соответственно, измените) [политики безопасных вложений](set-up-atp-safe-attachments-policies.md) в Организации и [политики безопасных ссылок](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="191c8-130">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="191c8-131">Предложен В качестве глобального администратора или администратора SharePoint Online выполните командлет **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** с параметром **дисалловинфектедфиледовнлоад** , для которого задано *значение true*.</span><span class="sxs-lookup"><span data-stu-id="191c8-131">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*.</span></span> <br/>
      - <span data-ttu-id="191c8-132">При установке для параметра значения *true* блокируются все действия для обнаруженных файлов (кроме DELETE).</span><span class="sxs-lookup"><span data-stu-id="191c8-132">Setting the parameter to *true* blocks all actions (except Delete) for detected files.</span></span> <span data-ttu-id="191c8-133">Пользователи не могут открывать, перемещать и копировать обнаруженные файлы, а также предоставлять к ним общий доступ.</span><span class="sxs-lookup"><span data-stu-id="191c8-133">People cannot open, move, copy, or share detected files.</span></span>
      - <span data-ttu-id="191c8-134">Если задать для параметра *значение false* , все действия, кроме DELETE и download, блокируются.</span><span class="sxs-lookup"><span data-stu-id="191c8-134">Setting the parameter to *false* blocks all actions except Delete and Download.</span></span> <span data-ttu-id="191c8-135">Пользователи могут принять решение о риске и скачать обнаруженный файл.</span><span class="sxs-lookup"><span data-stu-id="191c8-135">People can choose to accept the risk and download a detected file.</span></span>  
   
7. <span data-ttu-id="191c8-136">РазРешите до 30 минут, пока ваши изменения распространяются на все центры обработки данных Office 365.</span><span class="sxs-lookup"><span data-stu-id="191c8-136">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="191c8-137">Предложен Перейдите к разделу Настройка оповещений для обнаруженных файлов.</span><span class="sxs-lookup"><span data-stu-id="191c8-137">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
<span data-ttu-id="191c8-138">Для получения дополнительных сведений об использовании PowerShell с Office 365, ознакомьтесь со статьей [Управление office 365 с помощью PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="191c8-138">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell).</span></span> 

<span data-ttu-id="191c8-139">Чтобы узнать больше о пользовательском интерфейсе, когда файл был определен как вредоносный, посмотрите, [что делать, когда вредоносный файл обнаружен в SharePoint Online, OneDrive или Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="191c8-139">To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="191c8-140">Настройка оповещений для обнаруженных файлов</span><span class="sxs-lookup"><span data-stu-id="191c8-140">Set up alerts for detected files</span></span>

<span data-ttu-id="191c8-141">Чтобы получать уведомления о том, что файл в SharePoint Online, OneDrive для бизнеса или Microsoft Teams определен как вредоносный, вы можете настроить оповещение.</span><span class="sxs-lookup"><span data-stu-id="191c8-141">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="191c8-142">в [центре &amp; безопасности и соответствия требованиям Office 365](https://protection.office.com)выберите **оповещения** \> **управление оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="191c8-142">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="191c8-143">Выберите **создать политику оповещений**.</span><span class="sxs-lookup"><span data-stu-id="191c8-143">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="191c8-144">Укажите имя оповещения.</span><span class="sxs-lookup"><span data-stu-id="191c8-144">Specify a name for the alert.</span></span> <span data-ttu-id="191c8-145">Например, можно ввести в библиотеки вредоносные файлы.</span><span class="sxs-lookup"><span data-stu-id="191c8-145">For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="191c8-146">Введите описание оповещения.</span><span class="sxs-lookup"><span data-stu-id="191c8-146">Type a description for the alert.</span></span> <span data-ttu-id="191c8-147">Например, вы можете ввести уведомление администраторов об обнаружении вредоносных файлов в SharePoint Online, OneDrive или Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="191c8-147">For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="191c8-148">В разделе **отправить это оповещение, когда...** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="191c8-148">In the **Send this alert when...** section, do the following:</span></span> 
    
    <span data-ttu-id="191c8-149">а.</span><span class="sxs-lookup"><span data-stu-id="191c8-149">a.</span></span> <span data-ttu-id="191c8-150">В списке **действия** выберите обнаруженная **вредоносная программа в файле**.</span><span class="sxs-lookup"><span data-stu-id="191c8-150">In the **Activities** list, choose **Detected malware in file**.</span></span>
    
    <span data-ttu-id="191c8-151">б.</span><span class="sxs-lookup"><span data-stu-id="191c8-151">b.</span></span> <span data-ttu-id="191c8-152">Оставьте поле **Пользователи** пустым.</span><span class="sxs-lookup"><span data-stu-id="191c8-152">Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="191c8-153">В разделе **отправить это оповещение по...** выберите одного или нескольких глобальных администраторов, администраторов безопасности или средств чтения безопасности, которые должны получать уведомление при обнаружении вредоносного файла.</span><span class="sxs-lookup"><span data-stu-id="191c8-153">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="191c8-154">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="191c8-154">Click **Save**.</span></span>
    
<span data-ttu-id="191c8-155">Чтобы узнать больше об оповещениях, ознакомьтесь со статьей [Создание оповещений о &amp; действиях в центре безопасности и соответствия требованиям Office 365](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="191c8-155">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="191c8-156">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="191c8-156">Next steps</span></span>

1. [<span data-ttu-id="191c8-157">Просмотр сведений о вредоносных файлах, обнаруженных в SharePoint, OneDrive или Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="191c8-157">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [<span data-ttu-id="191c8-158">Управление сообщениями, помещенными в карантин, и файлами в качестве администратора в Office 365</span><span class="sxs-lookup"><span data-stu-id="191c8-158">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    

  

