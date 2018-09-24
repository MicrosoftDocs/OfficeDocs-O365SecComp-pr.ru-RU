---
title: Включить ATP Office 365 для SharePoint, OneDrive и группами Майкрософт
ms.author: derng
author: derng
manager: laurawi
ms.date: 5/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
description: Узнайте, как включить ATP для SharePoint, OneDrive и групп, включая способ настройки оповещения об обнаруженных файлах.
ms.openlocfilehash: bb99aee0887f15f065a47d691c59ce47639bdc32
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972241"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="bb0cb-103">Включить ATP Office 365 для SharePoint, OneDrive и группами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="bb0cb-103">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="bb0cb-p101">[Office 365 ATP для SharePoint, OneDrive и группами Майкрософт](atp-for-spo-odb-and-teams.md) защищает вашей организации от случайно совместное использование вредоносных файлов. При обнаружении вредоносных файлов, этот файл блокируется, чтобы никто можно открыть, скопируйте, перемещение или совместно использовать до дополнительных действий группой безопасности в организации. Ознакомьтесь с этой статьей, чтобы включить ATP для SharePoint, OneDrive и рабочих групп, настроить оповещения для уведомления об обнаруженных файлов и выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from inadvertently sharing malicious files. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to turn on ATP for SharePoint, OneDrive, and Teams, set up alerts to be notified about detected files, and take your next steps.</span></span> 
  
> [!TIP]
> <span data-ttu-id="bb0cb-107">Для выполнения задач, описанных в этой статье, необходимо иметь все необходимые разрешения, назначенные в Office 365 и в системы &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-107">In order to perform the tasks described in this article, you must have the necessary permissions assigned in Office 365 and in the Security &amp; Compliance Center.</span></span>
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="bb0cb-108">Включение ATP для SharePoint, OneDrive и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="bb0cb-108">Turn on ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

 <span data-ttu-id="bb0cb-p102">**Перед началом этой процедуры убедитесь в том, что ведение журнала аудита уже включен для вашей среды Office 365**. Обычно это делается пользователем, обладающим журналы аудита роли, назначенные в Exchange Online. Дополнительные сведения можно [Включить Office 365 проводить аудит операций поиска журнала включено или отключено](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="bb0cb-p102">**Before you begin this procedure, make sure that audit logging is already turned on for your Office 365 environment**. This is typically done by someone who has the Audit Logs role assigned in Exchange Online. For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>
  
1. <span data-ttu-id="bb0cb-112">Как глобальный администратор или администратор безопасности, перейдите к [https://protection.office.com](https://protection.office.com)и войдите с учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-112">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com), and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="bb0cb-113">В Office 365 безопасность &amp; центре соответствия требованиям в левой области навигации, в разделе **Управление угроз**, выберите **политику** \> **Безопасные вложения**.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-113">In the Office 365 Security &amp; Compliance Center, in the left navigation pane, under **Threat management**, choose **Policy** \> **Safe Attachments**.</span></span>
    
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите Threat management \> политики](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. <span data-ttu-id="bb0cb-115">Выберите **Включить ATP для SharePoint, OneDrive и группами Майкрософт**.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-115">Select **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>
    
    ![Включение расширенной защитой для SharePoint Online, OneDrive для бизнеса и группами Майкрософт](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. <span data-ttu-id="bb0cb-117">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-117">Click **Save**.</span></span>
    
5. <span data-ttu-id="bb0cb-118">Просмотрите (и, отредактируйте) [политики безопасные вложения](set-up-atp-safe-attachments-policies.md) и [политики безопасных ссылки](set-up-atp-safe-links-policies.md)вашей организации.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-118">Review (and, as appropriate, edit) your organization's [Safe Attachments policies](set-up-atp-safe-attachments-policies.md) and [Safe Links policies](set-up-atp-safe-links-policies.md).</span></span>
    
6. <span data-ttu-id="bb0cb-119">(Рекомендуется) Как глобальный администратор или администратор SharePoint Online, выполните командлет **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** с параметром **DisallowInfectedFileDownload** установлено значение *true* .</span><span class="sxs-lookup"><span data-stu-id="bb0cb-119">(Recommended) As a global administrator or a SharePoint Online administrator, run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true*  .</span></span> <br/><br/><span data-ttu-id="bb0cb-p103">Установка для параметра в *значение true,* блокирует все действия (за исключением Delete) для обнаруженных файлы. Пользователи не могут открыть, перемещение, копирование или общего доступа к файлам вредоносным.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-p103">Setting the parameter to *true* blocks all actions (except Delete) for detected files. People cannot open, move, copy, or share detected files. </span></span><br/><br/><span data-ttu-id="bb0cb-p104">Установка для параметра значение *false* блокирует все действия, за исключением Delete и загрузки. Люди могут выбрать для принятия риск и загрузите файл вредоносным.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-p104">Setting the parameter to *false* blocks all actions except Delete and Download. People can choose to accept the risk and download a detected file. </span></span><br/><br/><span data-ttu-id="bb0cb-124">Рекомендуется для параметра *значение true*.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-124">We recommend setting the parameter to *true*.</span></span> 
   
7. <span data-ttu-id="bb0cb-125">Разрешить до 30 минут для применения изменений для распространения для всех центров обработки данных Office 365.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-125">Allow up to 30 minutes for your changes to spread to all Office 365 datacenters.</span></span>
    
8. <span data-ttu-id="bb0cb-126">(Рекомендуется) Перейдите к настройке оповещения об обнаруженных файлах.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-126">(Recommended) Proceed to set up alerts for detected files.</span></span>
    
> [!TIP]
> <span data-ttu-id="bb0cb-p105">Чтобы подробнее узнать об использовании PowerShell с помощью Office 365, обратитесь к разделу [Управление Office 365 с помощью PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). > Для получения дополнительных сведений о удобство работы пользователей, при обнаружении файл как вредоносных, видеть [что делать при обнаружении вредоносных файлов в SharePoint Online, OneDrive или группами Майкрософт](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span><span class="sxs-lookup"><span data-stu-id="bb0cb-p105">To learn more about using PowerShell with Office 365, see [Manage Office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). > To learn more about the user experience when a file has been detected as malicious, see [What to do when a malicious file is found in SharePoint Online, OneDrive, or Microsoft Teams](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2).</span></span> 
  
## <a name="set-up-alerts-for-detected-files"></a><span data-ttu-id="bb0cb-129">Настройка оповещений для обнаруженных файлов</span><span class="sxs-lookup"><span data-stu-id="bb0cb-129">Set up alerts for detected files</span></span>

<span data-ttu-id="bb0cb-130">Чтобы получать уведомления, когда файл в SharePoint Online, OneDrive для бизнеса, или группами Майкрософт было определено как вредоносных, можно настроить оповещения.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-130">To receive notification when a file in SharePoint Online, OneDrive for Business, or Microsoft Teams has been identified as malicious, you can set up an alert.</span></span>
  
1. <span data-ttu-id="bb0cb-131">В Office 365 безопасность &amp; центре соответствия требованиям, выберите **оповещения** \> **Управление оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-131">In the Office 365 Security &amp; Compliance Center, choose **Alerts** \> **Manage alerts**.</span></span>
    
2. <span data-ttu-id="bb0cb-132">Выберите **новую политику оповещения**.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-132">Choose **New alert policy**.</span></span>
    
3. <span data-ttu-id="bb0cb-p106">Укажите имя для оповещения. Например вы введите вредоносных файлов в библиотеках.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-p106">Specify a name for the alert. For example, you could type Malicious Files in Libraries.</span></span>
    
4. <span data-ttu-id="bb0cb-p107">Введите описание для оповещения. Например можно ввести уведомляет администраторов при обнаружении вредоносных файлов в SharePoint Online, OneDrive или группами Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-p107">Type a description for the alert. For example, you could type Notifies admins when malicious files are detected in SharePoint Online, OneDrive, or Microsoft Teams.</span></span>
    
5. <span data-ttu-id="bb0cb-137">В разделе **Отправить это уведомление, когда...** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-137">In the **Send this alert when...** section, do the following:</span></span> 
    
  - <span data-ttu-id="bb0cb-138">В списке **действий** выберите **вредоносные программы обнаружены в файл**.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-138">In the **Activities** list, choose **Detected malware in file**.</span></span>
    
  - <span data-ttu-id="bb0cb-139">Не заполняйте поле **Пользователи** .</span><span class="sxs-lookup"><span data-stu-id="bb0cb-139">Leave the **Users** field empty.</span></span> 
    
6. <span data-ttu-id="bb0cb-140">В разделе **Отправить это оповещение, чтобы...** выберите одного или нескольких глобальных администраторов, администраторов безопасности или читатели безопасности, которые будут получать уведомления при обнаружении вредоносных файлов.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-140">In the **Send this alert to...** section, select one or more global administrators, security administrators, or security readers who should receive notification when a malicious file is detected.</span></span> 
    
7. <span data-ttu-id="bb0cb-141">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="bb0cb-141">Click **Save**.</span></span>
    
> [!TIP]
> <span data-ttu-id="bb0cb-142">Чтобы узнать больше о оповещения, обратитесь к разделу [Создание оповещений активности безопасности Office 365 &amp; центре соответствия требованиям](create-activity-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="bb0cb-142">To learn more about alerts, see [Create activity alerts in the Office 365 Security &amp; Compliance Center](create-activity-alerts.md).</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="bb0cb-143">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="bb0cb-143">Next steps</span></span>

- [<span data-ttu-id="bb0cb-144">Просмотр сведений о вредоносных файлов, обнаруженных в SharePoint, OneDrive или группами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="bb0cb-144">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
- [<span data-ttu-id="bb0cb-145">Управление сообщений на карантине и файлы с правами администратора в Office 365</span><span class="sxs-lookup"><span data-stu-id="bb0cb-145">Manage quarantined messages and files as an administrator in Office 365</span></span>](manage-quarantined-messages-and-files.md)
    
## <a name="related-topics"></a><span data-ttu-id="bb0cb-146">Смежные темы</span><span class="sxs-lookup"><span data-stu-id="bb0cb-146">Related topics</span></span>

[<span data-ttu-id="bb0cb-147">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="bb0cb-147">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="bb0cb-148">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="bb0cb-148">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="bb0cb-149">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="bb0cb-149">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

