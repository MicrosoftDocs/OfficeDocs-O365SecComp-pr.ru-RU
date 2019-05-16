---
title: Просмотр отчетов для Office 365 Advanced Threat protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 04/01/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection:
- M365-security-compliance
description: Узнайте, как найти и использовать отчеты для Office 365 Advanced Threat Protection в центре безопасности &amp; и соответствия требованиям.
ms.openlocfilehash: 3525c71f8a627d930afbf94f5f0d12e55f19a0b6
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077325"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="d8863-103">Просмотр отчетов для Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="d8863-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="d8863-104">Если в Организации имеется [Office 365 Advanced Threat protection](office-365-atp.md) (ATP), и у вас есть [необходимые разрешения](#what-permissions-are-needed-to-view-the-atp-reports), вы можете использовать несколько отчетов ATP в центре &amp; безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d8863-104">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-the-atp-reports), you can use several ATP reports in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="d8863-105">(Перейдите в \*\*\*\* \> **панель мониторинга**отчетов.)</span><span class="sxs-lookup"><span data-stu-id="d8863-105">(Go to **Reports** \> **Dashboard**.)</span></span>
  
![Информационная &amp; панель центра соответствия требованиям безопасности поможет вам узнать, где работает Расширенная защита от угроз](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="d8863-107">Отчеты ATP включают в себя [отчет о состоянии защиты от угроз](#threat-protection-status-report), [отчет о типах файлов ATP](#atp-file-types-report)и [отчет об ликвидации сообщений ATP](#atp-message-disposition-report).</span><span class="sxs-lookup"><span data-stu-id="d8863-107">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report).</span></span> <span data-ttu-id="d8863-108">В этой статье описываются отчеты ATP и приводятся ссылки на [Дополнительные отчеты для просмотра](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="d8863-108">This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="d8863-109">Отчет о состоянии защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="d8863-109">Threat Protection Status report</span></span>

<span data-ttu-id="d8863-110">Отчет **о состоянии защиты от угроз** — это единое представление, объединяющее сведения о вредоносном содержимом и вредоносных сообщениях, обнаруженных и заблокированных службой [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) и [Office 365 ATP](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="d8863-110">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md).</span></span> <span data-ttu-id="d8863-111">В отчете представлено общее количество уникальных сообщений электронной почты с вредоносным содержимым (файлы или адреса веб-сайтов (URL-адреса)), заблокированных ядром защиты от вредоносных программ, функции [автоматического очистки (ZAP)](zero-hour-auto-purge.md)и ATP, такие как [безопасные ссылки ATP](atp-safe-links.md), [безопасно ](atp-safe-attachments.md)И [функции защиты от фишинга ATP](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="d8863-111">The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d8863-112">Отчет о состоянии защиты от угроз доступен клиентам, у которых есть [Office 365 ATP](office-365-atp.md) или [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); Однако сведения, отображаемые в отчете о состоянии защиты от угроз для клиентов ATP, скорее всего, будут содержать данные, отличные от данных, которые могут видеть пользователи EOP.</span><span class="sxs-lookup"><span data-stu-id="d8863-112">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see.</span></span> <span data-ttu-id="d8863-113">Например, отчет о состоянии защиты от угроз для клиентов ATP будет содержать сведения о [вредоносных файлах, обнаруженных в SharePoint Online, OneDrive или Microsoft Teams](atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="d8863-113">For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span> <span data-ttu-id="d8863-114">Такие сведения относятся к ATP, поэтому клиенты, у которых есть EOP, но не ATP, не увидят эти сведения в отчете о состоянии защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="d8863-114">Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="d8863-115">Чтобы просмотреть отчет о состоянии защиты от угроз, в [центре &amp; безопасности и соответствия требованиям](https://protection.office.com)выберите \*\*\*\* \> \*\*\*\* \> **состояние защиты от угроз**для отчетов.</span><span class="sxs-lookup"><span data-stu-id="d8863-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Отчет о состоянии защиты от угроз для ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="d8863-117">Чтобы получить подробные сведения о состоянии дня, наведите указатель на диаграмму.</span><span class="sxs-lookup"><span data-stu-id="d8863-117">To get detailed status for a day, hover over the graph.</span></span>
  
![Данные о состоянии ATP Threat protection за день](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="d8863-119">По умолчанию в отчете о состоянии защиты от угроз отображаются данные за прошедшие семь дней.</span><span class="sxs-lookup"><span data-stu-id="d8863-119">By default, the Threat Protection Status report shows data for the past seven days.</span></span> <span data-ttu-id="d8863-120">Тем не менее, вы можете выбрать **фильтры** и изменить диапазон дат для просмотра данных в течение до 90 дней.</span><span class="sxs-lookup"><span data-stu-id="d8863-120">However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Фильтры состояния защиты от угроз ATP](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="d8863-122">Вы также можете использовать меню **Просмотр данных,** чтобы изменить сведения, отображаемые в отчете.</span><span class="sxs-lookup"><span data-stu-id="d8863-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Параметры просмотра для отчета о состоянии защиты от угроз для ATP](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="d8863-124">Отчет о типах файлов ATP</span><span class="sxs-lookup"><span data-stu-id="d8863-124">ATP File Types report</span></span>

<span data-ttu-id="d8863-125">В отчете " **типы файлов ATP** " отображаются типы файлов, обнаруженных в качестве вредоносных при [безопасном вложении ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="d8863-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="d8863-126">Чтобы просмотреть этот отчет, в [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)перейдите к **типам файлов** **панели мониторинга** \> **отчетов** \> ATP.</span><span class="sxs-lookup"><span data-stu-id="d8863-126">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Отчет о типах файлов ATP](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="d8863-128">Если навести указатель мыши на определенный день, можно увидеть разбивку типов вредоносных файлов, обнаруженных безопасными [вложениями ATP](atp-safe-attachments.md) и защитой от нежелательной [почты &amp; в Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="d8863-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![Данные о типах файлов ATP в день](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="d8863-130">Отчет об ликвидации сообщений ATP</span><span class="sxs-lookup"><span data-stu-id="d8863-130">ATP Message Disposition report</span></span>

<span data-ttu-id="d8863-131">В отчете об **ликвидации сообщений ATP** отображаются действия, предпринятые для сообщений электронной почты, которые были обнаружены как вредоносный контент.</span><span class="sxs-lookup"><span data-stu-id="d8863-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="d8863-132">Чтобы просмотреть этот отчет, в [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)перейдите к разделу **панель мониторинга** \> **отчетов** \> **ATP Message Disposition**.</span><span class="sxs-lookup"><span data-stu-id="d8863-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Отчет об ликвидации сообщений ATP](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="d8863-134">При наведении указателя мыши на полоску на диаграмме можно просмотреть, какие действия были предприняты для обнаруженных сообщений электронной почты в этот день.</span><span class="sxs-lookup"><span data-stu-id="d8863-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![Данные отчета об ликвидации сообщений ATP за день](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="d8863-136">Дополнительные отчеты для просмотра</span><span class="sxs-lookup"><span data-stu-id="d8863-136">Additional reports to view</span></span>

<span data-ttu-id="d8863-137">Помимо отчетов ATP, описанных в этой статье, доступны некоторые другие отчеты, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d8863-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>

|<span data-ttu-id="d8863-138">Отчет (ы)</span><span class="sxs-lookup"><span data-stu-id="d8863-138">Report(s)</span></span>  |<span data-ttu-id="d8863-139">Сведения</span><span class="sxs-lookup"><span data-stu-id="d8863-139">Details</span></span>  |
|---------|---------|
|<span data-ttu-id="d8863-140">**Трассировка URL-адресов для безопасных ссылок ATP** (Это отчет, созданный с помощью PowerShell.) В этом отчете представлены результаты действий безопасных ссылок ATP за прошедшие семь (7) дней.</span><span class="sxs-lookup"><span data-stu-id="d8863-140">**ATP Safe Links URL trace** (This is a report you generate by using PowerShell.) This report shows the results of ATP Safe Links actions over the past seven (7) days.</span></span> |[<span data-ttu-id="d8863-141">Справочные материалы по командлету Get – Урлтраце</span><span class="sxs-lookup"><span data-stu-id="d8863-141">Get-UrlTrace cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-urltrace?view=exchange-ps) |
|<span data-ttu-id="d8863-142">**Отчеты о безопасности электронной почты**, например отчет о самых отправителях и получателях, отчет о поддельной почте и отчет об обнаружении нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="d8863-142">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="d8863-143">Просмотр отчетов о безопасности электронной почты в &amp; центре безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d8863-143">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="d8863-144">**Explorer** (также называется проводником по угрозам, это включено в [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md))</span><span class="sxs-lookup"><span data-stu-id="d8863-144">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md))</span></span>     | [<span data-ttu-id="d8863-145">Использование проводника в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d8863-145">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="d8863-146">**Результаты EOP и ATP** (Это настраиваемый отчет, созданный с помощью PowerShell).</span><span class="sxs-lookup"><span data-stu-id="d8863-146">**EOP and ATP results** (This is a custom report you generate by using PowerShell).</span></span> <span data-ttu-id="d8863-147">Этот отчет содержит такие сведения, как домен, Дата, тип события, направление, действие и количество сообщений.</span><span class="sxs-lookup"><span data-stu-id="d8863-147">This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="d8863-148">Справочные материалы по командлету Get – Маилтраффикатпрепорт</span><span class="sxs-lookup"><span data-stu-id="d8863-148">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="d8863-149">**Обнаружения EOP и ATP** (Это настраиваемый отчет, созданный с помощью PowerShell).</span><span class="sxs-lookup"><span data-stu-id="d8863-149">**EOP and ATP detections** (This is a custom report you generate by using PowerShell).</span></span> <span data-ttu-id="d8863-150">Этот отчет содержит сведения о вредоносных файлах или URL-адресах, фишинговых попытках, олицетворении и других потенциальных угрозах в электронной почте или файлах.</span><span class="sxs-lookup"><span data-stu-id="d8863-150">This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="d8863-151">Справочные материалы по командлету Get – Маилдетаилатпрепорт</span><span class="sxs-lookup"><span data-stu-id="d8863-151">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="d8863-152">Какие разрешения необходимы для просмотра отчетов ATP?</span><span class="sxs-lookup"><span data-stu-id="d8863-152">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="d8863-153">Для просмотра и использования отчетов, описанных в этой статье, **необходимо назначить соответствующую роль для центра безопасности &amp; и центра администрирования Exchange**.</span><span class="sxs-lookup"><span data-stu-id="d8863-153">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange admin center**.</span></span>

- <span data-ttu-id="d8863-154">Для центра соответствия &amp; требованиям безопасности необходимо назначить одну из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="d8863-154">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="d8863-155">Управление организацией</span><span class="sxs-lookup"><span data-stu-id="d8863-155">Organization Management</span></span>
    - <span data-ttu-id="d8863-156">Администратор безопасности (это можно назначить в центре администрирования Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))).</span><span class="sxs-lookup"><span data-stu-id="d8863-156">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
    - <span data-ttu-id="d8863-157">Средство чтения безопасности</span><span class="sxs-lookup"><span data-stu-id="d8863-157">Security Reader</span></span>

- <span data-ttu-id="d8863-158">Для Exchange Online необходимо назначить одну из следующих ролей в центре администрирования Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) или с помощью командлетов PowerShell (см. [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span><span class="sxs-lookup"><span data-stu-id="d8863-158">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="d8863-159">Управление организацией</span><span class="sxs-lookup"><span data-stu-id="d8863-159">Organization Management</span></span>
    - <span data-ttu-id="d8863-160">Управление организацией с правами только на просмотр</span><span class="sxs-lookup"><span data-stu-id="d8863-160">View-only Organization Management</span></span>
    - <span data-ttu-id="d8863-161">Роль получателей с правами только на просмотр</span><span class="sxs-lookup"><span data-stu-id="d8863-161">View-Only Recipients role</span></span>
    - <span data-ttu-id="d8863-162">Управление соответствием требованиям</span><span class="sxs-lookup"><span data-stu-id="d8863-162">Compliance Management</span></span>

<span data-ttu-id="d8863-163">Чтобы узнать больше, ознакомьтесь со следующими материалами:</span><span class="sxs-lookup"><span data-stu-id="d8863-163">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="d8863-164">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="d8863-164">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="d8863-165">Разрешения компонентов в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="d8863-165">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="d8863-166">Что делать, если в отчетах данные не отображаются?</span><span class="sxs-lookup"><span data-stu-id="d8863-166">What if the reports aren't showing data?</span></span>

<span data-ttu-id="d8863-167">Если вы не видите данные в отчетах ATP, дважды проверьте правильность настройки политик.</span><span class="sxs-lookup"><span data-stu-id="d8863-167">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly.</span></span> <span data-ttu-id="d8863-168">Для вашей организации должны быть определены политики [безопасных ссылок ATP](set-up-atp-safe-links-policies.md) и [политики безопасных вложений ATP](set-up-atp-safe-attachments-policies.md) для обеспечения безопасности ATP.</span><span class="sxs-lookup"><span data-stu-id="d8863-168">Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place.</span></span> <span data-ttu-id="d8863-169">Кроме того, вы можете увидеть защиту от нежелательной [почты и вредоносных программ в Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="d8863-169">Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="d8863-170">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d8863-170">Related topics</span></span>

[<span data-ttu-id="d8863-171">Отчеты и аналитика в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="d8863-171">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="d8863-172">Создание расписания для отчета в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d8863-172">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="d8863-173">Настройка и загрузка настраиваемого отчета в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d8863-173">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

