---
title: Просмотр отчетов для Office 365 Advanced Threat protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection: M365-security-compliance
description: Узнайте, как найти и использовать отчеты для Office 365 Advanced Threat Protection в центре безопасности &amp; и соответствия требованиям.
ms.openlocfilehash: c45224155d2e72edda1e0f0eced879e152b49629
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2019
ms.locfileid: "30062617"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="08a96-103">Просмотр отчетов для Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="08a96-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="08a96-p101">Если в Организации имеется [Office 365 Advanced Threat protection](office-365-atp.md) (ATP), и у вас есть [необходимые разрешения](#what-permissions-are-needed-to-view-these-reports), вы можете использовать несколько отчетов ATP в центре &amp; безопасности и соответствия требованиям. (Перейдите в \*\*\*\* \> **панель мониторинга**отчетов.)</span><span class="sxs-lookup"><span data-stu-id="08a96-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![Информационная &amp; панель центра соответствия требованиям безопасности поможет вам узнать, где работает Расширенная защита от угроз](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="08a96-p102">Отчеты ATP включают в себя [отчет о состоянии защиты от угроз](#threat-protection-status-report), [отчет о типах файлов ATP](#atp-file-types-report)и [отчет об ликвидации сообщений ATP](#atp-message-disposition-report). В этой статье описываются отчеты ATP и приводятся ссылки на [Дополнительные отчеты для просмотра](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="08a96-p102">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="08a96-109">Отчет о состоянии защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="08a96-109">Threat Protection Status report</span></span>

<span data-ttu-id="08a96-p103">Отчет **о состоянии защиты от угроз** — это единое представление, объединяющее сведения о вредоносном содержимом и вредоносных сообщениях, обнаруженных и заблокированных службой [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) и [Office 365 ATP](office-365-atp.md). В отчете представлено общее количество уникальных сообщений электронной почты с вредоносным содержимым (файлы или адреса веб-сайтов (URL-адреса)), заблокированных ядром защиты от вредоносных программ, функции [автоматического очистки (ZAP)](zero-hour-auto-purge.md)и ATP, такие как [безопасные ссылки ATP](atp-safe-links.md), [безопасно ](atp-safe-attachments.md)И [функции защиты от фишинга ATP](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="08a96-p103">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md). The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="08a96-p104">Отчет о состоянии защиты от угроз доступен клиентам, у которых есть [Office 365 ATP](office-365-atp.md) или [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); Однако сведения, отображаемые в отчете о состоянии защиты от угроз для клиентов ATP, скорее всего, будут содержать данные, отличные от данных, которые могут видеть пользователи EOP. Например, отчет о состоянии защиты от угроз для клиентов ATP будет содержать сведения о [вредоносных файлах, обнаруженных в SharePoint Online, OneDrive или Microsoft Teams](atp-for-spo-odb-and-teams.md). Такие сведения относятся к ATP, поэтому клиенты, у которых есть EOP, но не ATP, не увидят эти сведения в отчете о состоянии защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="08a96-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md). Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="08a96-115">Чтобы просмотреть отчет о состоянии защиты от угроз, в [центре &amp; безопасности и соответствия требованиям](https://protection.office.com)выберите \*\*\*\* \> \*\*\*\* \> **состояние защиты от угроз**для отчетов.</span><span class="sxs-lookup"><span data-stu-id="08a96-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Отчет о состоянии защиты от угроз для ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="08a96-117">Чтобы получить подробные сведения о состоянии дня, наведите указатель на диаграмму.</span><span class="sxs-lookup"><span data-stu-id="08a96-117">To get detailed status for a day, hover over the graph.</span></span>
  
![Данные о состоянии ATP Threat protection за день](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="08a96-p105">По умолчанию в отчете о состоянии защиты от угроз отображаются данные за прошедшие семь дней. Тем не менее, вы можете выбрать **фильтры** и изменить диапазон дат для просмотра данных в течение до 90 дней.</span><span class="sxs-lookup"><span data-stu-id="08a96-p105">By default, the Threat Protection Status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Фильтры состояния защиты от угроз ATP](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="08a96-122">Вы также можете использовать меню **Просмотр данных,** чтобы изменить сведения, отображаемые в отчете.</span><span class="sxs-lookup"><span data-stu-id="08a96-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Параметры просмотра для отчета о состоянии защиты от угроз для ATP](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="08a96-124">Отчет о типах файлов ATP</span><span class="sxs-lookup"><span data-stu-id="08a96-124">ATP File Types report</span></span>

<span data-ttu-id="08a96-125">В отчете " **типы файлов ATP** " отображаются типы файлов, обнаруженных в качестве вредоносНых при [безопасном вложении ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="08a96-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="08a96-126">Чтобы просмотреть этот отчет, в [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)перейдите к **типам файлов** **панели мониторинга** \> **отчетов** \> ATP.</span><span class="sxs-lookup"><span data-stu-id="08a96-126">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Отчет о типах файлов ATP](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="08a96-128">Если навести указатель мыши на определенный день, можно увидеть разбивку типов вредоносных файлов, обнаруженных безопасными [вложенияМи ATP](atp-safe-attachments.md) и защитой от нежелательной [почты &amp; в Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="08a96-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![Данные о типах файлов ATP в день](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="08a96-130">Отчет об ликвидации сообщений ATP</span><span class="sxs-lookup"><span data-stu-id="08a96-130">ATP Message Disposition report</span></span>

<span data-ttu-id="08a96-131">В отчете об **ликвидации сообщений ATP** отображаются действия, предпринятые для сообщений электронной почты, которые были обнаружены как вредоносный контент.</span><span class="sxs-lookup"><span data-stu-id="08a96-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="08a96-132">Чтобы просмотреть этот отчет, в [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)перейдите к разделу **панель мониторинга** \> **отчетов** \> **ATP Message Disposition**.</span><span class="sxs-lookup"><span data-stu-id="08a96-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Отчет об ликвидации сообщений ATP](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="08a96-134">При наведении указателя мыши на полоску на диаграмме можно просмотреть, какие действия были предприняты для обнаруженных сообщений электронной почты в этот день.</span><span class="sxs-lookup"><span data-stu-id="08a96-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![Данные отчета об ликвидации сообщений ATP за день](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="08a96-136">Дополнительные отчеты для просмотра</span><span class="sxs-lookup"><span data-stu-id="08a96-136">Additional reports to view</span></span>

<span data-ttu-id="08a96-137">Помимо отчетов ATP, описанных в этой статье, доступны некоторые другие отчеты, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="08a96-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>

|<span data-ttu-id="08a96-138">Тип отчета</span><span class="sxs-lookup"><span data-stu-id="08a96-138">Report type</span></span>  |<span data-ttu-id="08a96-139">Подробнее</span><span class="sxs-lookup"><span data-stu-id="08a96-139">Learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="08a96-140">**Отчеты о безопасности электронной почты**, например отчет о самых отправителях и получателях, отчет о поддельной почте и отчет об обнаруженИи нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="08a96-140">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="08a96-141">Просмотр отчетов о безопасности электронной почты в &amp; центре безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="08a96-141">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="08a96-142">**Explorer** (также называется обозревателем угроз, это включено в [Office 365 Threat Intelligence](office-365-ti.md)).</span><span class="sxs-lookup"><span data-stu-id="08a96-142">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Threat Intelligence](office-365-ti.md))</span></span>     | [<span data-ttu-id="08a96-143">Использование проводника в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="08a96-143">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="08a96-p106">**Результаты EOP и ATP** (Это настраиваемый отчет, созданный с помощью PowerShell). Этот отчет содержит такие сведения, как домен, Дата, тип события, направление, действие и количество сообщений.</span><span class="sxs-lookup"><span data-stu-id="08a96-p106">**EOP and ATP results** (This is a custom report you generate by using PowerShell). This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="08a96-146">Справочные материалы по командлету Get – Маилтраффикатпрепорт</span><span class="sxs-lookup"><span data-stu-id="08a96-146">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="08a96-p107">**Обнаружения EOP и ATP** (Это настраиваемый отчет, созданный с помощью PowerShell). Этот отчет содержит сведения о вредоносных файлах или URL-адресах, фишинговых попытках, олицетворении и других потенциальных угрозах в электронной почте или файлах.</span><span class="sxs-lookup"><span data-stu-id="08a96-p107">**EOP and ATP detections** (This is a custom report you generate by using PowerShell). This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="08a96-149">Справочные материалы по командлету Get – Маилдетаилатпрепорт</span><span class="sxs-lookup"><span data-stu-id="08a96-149">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="08a96-150">Какие разрешения необходимы для просмотра отчетов ATP?</span><span class="sxs-lookup"><span data-stu-id="08a96-150">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="08a96-151">Для просмотра и использования отчетов, описанных в этой статье, **необходимо назначить соответствующую роль для центра безопасности &amp; и центра администрирования Exchange**.</span><span class="sxs-lookup"><span data-stu-id="08a96-151">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="08a96-152">Для центра соответствия &amp; требованиям безопасности необходимо назначить одну из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="08a96-152">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="08a96-153">Управление организацией</span><span class="sxs-lookup"><span data-stu-id="08a96-153">Organization Management</span></span>
    - <span data-ttu-id="08a96-154">Администратор безопасности (это можно назначить в центре администрирования Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))).</span><span class="sxs-lookup"><span data-stu-id="08a96-154">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
    - <span data-ttu-id="08a96-155">Средство чтения безопасности</span><span class="sxs-lookup"><span data-stu-id="08a96-155">Security Reader</span></span>

- <span data-ttu-id="08a96-156">Для Exchange Online необходимо назначить одну из следующих ролей в центре администрирования Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) или с помощью командлетов PowerShell (см. [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span><span class="sxs-lookup"><span data-stu-id="08a96-156">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="08a96-157">Управление организацией</span><span class="sxs-lookup"><span data-stu-id="08a96-157">Organization Management</span></span>
    - <span data-ttu-id="08a96-158">Управление организацией с правами только на просмотр</span><span class="sxs-lookup"><span data-stu-id="08a96-158">View-only Organization Management</span></span>
    - <span data-ttu-id="08a96-159">Роль получателей с правами только на просмотр</span><span class="sxs-lookup"><span data-stu-id="08a96-159">View-Only Recipients role</span></span>
    - <span data-ttu-id="08a96-160">Управление соответствием требованиям</span><span class="sxs-lookup"><span data-stu-id="08a96-160">Compliance Management</span></span>

<span data-ttu-id="08a96-161">Чтобы узнать больше, ознакомьтесь со следующими материалами:</span><span class="sxs-lookup"><span data-stu-id="08a96-161">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="08a96-162">Разрешения в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="08a96-162">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="08a96-163">Разрешения компонентов в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="08a96-163">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="08a96-164">Что делать, если в отчетах данные не отображаются?</span><span class="sxs-lookup"><span data-stu-id="08a96-164">What if the reports aren't showing data?</span></span>

<span data-ttu-id="08a96-p108">Если вы не видите данные в отчетах ATP, дважды проверьте правильность настройки политик. Для вашей организации должны быть определены политики [безопасных ссылок ATP](set-up-atp-safe-links-policies.md) и [политики безОпасных вложений ATP](set-up-atp-safe-attachments-policies.md) для обеспечения безопасности ATP. Кроме того, вы можете увидеть защиту от нежелательной [почты и вредоносных программ в Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="08a96-p108">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="08a96-168">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="08a96-168">Related topics</span></span>

[<span data-ttu-id="08a96-169">Отчеты и аналитика в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="08a96-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="08a96-170">Создание расписания для отчета в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="08a96-170">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="08a96-171">Настройка и загрузка настраиваемого отчета в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="08a96-171">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

