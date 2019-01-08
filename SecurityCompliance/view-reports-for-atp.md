---
title: Просмотр отчетов для защиты расширенного Threat Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/07/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
description: Узнайте, как найти и использовать отчеты для Office 365 расширенного защиту от угроз безопасности &amp; центре соответствия требованиям.
ms.openlocfilehash: d387e020e5834d4961e7bda50b418ea11b9f0f4d
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749353"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="3d4f3-103">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="3d4f3-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="3d4f3-p101">Если ваша организация имеет [Защиту от угроз для Office 365 Advanced](office-365-atp.md) (ATP) и у вас есть [соответствующие разрешения](#what-permissions-are-needed-to-view-these-reports), можно использовать несколько отчетов анализа в системы &amp; центре соответствия требованиям. (Перейдите к **отчетам** \> **панели мониторинга**.)</span><span class="sxs-lookup"><span data-stu-id="3d4f3-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![Безопасность &amp; панели мониторинга в центре соответствия требованиям, которые помогут посмотреть, где работает расширенного защиту от угроз](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="3d4f3-p102">Отчеты анализа включают [отчет о состоянии защиты от угроз](#threat-protection-status-report), [типы файлов ATP отчета](#atp-file-types-report)и [отчет о ликвидации ATP сообщения](#atp-message-disposition-report). В этой статье описываются отчетов анализа и приведены ссылки на [Дополнительные отчеты для просмотра](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="3d4f3-p102">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="3d4f3-109">Отчет о состоянии защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="3d4f3-109">Threat Protection Status report</span></span>

<span data-ttu-id="3d4f3-p103">Отчет о **Состоянии защиты от угроз** — это один представление, который объединяет сведения о нежелательном содержимое и вредоносное электронной почты обнаруженных и блокирует [Office 365 ATP](office-365-atp.md)и [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP). Отчет предоставляет сводный число сообщений уникальные электронной почты с вредоносным содержимым (файлы или адреса веб-сайта (URL-адреса)), блокирует модуль защиты от вредоносных программ, [критическую автоматической очистки (ZAP)](zero-hour-auto-purge.md)и функции анализа, такие как [Безопасных ссылок анализа](atp-safe-links.md), [ATP Safe Вложения](atp-safe-attachments.md)и [возможности фишинга анализа](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="3d4f3-p103">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md). The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="3d4f3-p104">Отчет о состоянии защиты от угроз доступна для пользователей, которые имеют [Office 365 ATP](office-365-atp.md) и [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); Тем не менее сведения, отображаемые в отчет о состоянии защиты от угроз для клиентов ATP скорее всего будет содержать данных клиенты EOP могут видеть. Например отчет о состоянии защиты от угроз для анализа клиентов будет содержать сведения об [обнаруженных вредоносных файлов в SharePoint Online, OneDrive или группами Майкрософт](atp-for-spo-odb-and-teams.md). Такие данные, специально для анализа, чтобы пользователям EOP, но не ATP не будет видеть эти сведения в своих отчет о состоянии защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md). Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="3d4f3-115">Чтобы просмотреть отчет о состоянии защиты от угроз, в [безопасности &amp; центре соответствия требованиям](https://security.microsoft.com), перейдите к **отчетам** \> **панели мониторинга** \> **Состояние защиты от угроз**.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Отчет о состоянии защиты от угроз ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="3d4f3-117">Чтобы получить подробные сведения о состоянии в течение дня, наведите указатель мыши на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-117">To get detailed status for a day, hover over the graph.</span></span>
  
![Состояние защиты от угроз анализа данных в течение дня](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="3d4f3-p105">По умолчанию отчет о состоянии защиты от угроз отображаются данные за последние семь дней. Тем не менее можно выбрать **фильтры** и изменить диапазон дат для просмотра данных в течение 90 дней.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-p105">By default, the Threat Protection Status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Фильтры состояния защиты от угроз ATP](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="3d4f3-122">В меню **Просмотр данных с** также можно использовать для изменения сведениях, отображаемых в отчете.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Параметры просмотра для отчета о состоянии защиты от угроз ATP](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="3d4f3-124">Типы файлов ATP отчета</span><span class="sxs-lookup"><span data-stu-id="3d4f3-124">ATP File Types report</span></span>

<span data-ttu-id="3d4f3-125">**Типы файлов ATP** отчет отображает тип файлов, обнаруженных вредоносных как [Безопасные вложения ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="3d4f3-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="3d4f3-126">Чтобы просмотреть этот отчет в [безопасности &amp; центре соответствия требованиям](https://security.microsoft.com), перейдите к **отчетам** \> **панели мониторинга** \> **ATP типов файлов**.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-126">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Типы файлов ATP отчета](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="3d4f3-128">При наведении указателя на конкретный день, могут видеть декомпозиции типы вредоносных файлов, обнаруженных с [ATP безопасные вложения](atp-safe-attachments.md) и [защиты от нежелательной почты &amp; защита от вредоносных программ в Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="3d4f3-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![Типы файлов анализа данных отчетов в течение дня](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="3d4f3-130">Отчет о ликвидации ATP сообщения</span><span class="sxs-lookup"><span data-stu-id="3d4f3-130">ATP Message Disposition report</span></span>

<span data-ttu-id="3d4f3-131">Отчет о **Ликвидации ATP сообщение** показывает действия, предпринятые для сообщений электронной почты, обнаруженные как имеющий вредоносного содержимого.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="3d4f3-132">Чтобы просмотреть этот отчет в [безопасности &amp; центре соответствия требованиям](https://security.microsoft.com), перейдите к **отчетам** \> **панели мониторинга** \> **Ликвидации ATP сообщения**.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-132">To view this report, in the [Security &amp; Compliance Center](https://security.microsoft.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Отчет о ликвидации ATP сообщения](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="3d4f3-134">При наведении указателя на панели диаграммы, можно просмотреть действия, которые были созданы для вредоносным электронной почты для этого дня.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![Данные отчета о ликвидации ATP сообщений в течение дня](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="3d4f3-136">Дополнительные отчеты для просмотра</span><span class="sxs-lookup"><span data-stu-id="3d4f3-136">Additional reports to view</span></span>

<span data-ttu-id="3d4f3-137">Помимо анализа отчета, описанные в этой статье другие отчеты, которые описаны в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="3d4f3-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>


|<span data-ttu-id="3d4f3-138">Тип отчета</span><span class="sxs-lookup"><span data-stu-id="3d4f3-138">Report type</span></span>  |<span data-ttu-id="3d4f3-139">Подробнее</span><span class="sxs-lookup"><span data-stu-id="3d4f3-139">Learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="3d4f3-140">**Отчеты о безопасности электронной почты**, например отправителей в начало и получатели отчета, отчет подделка почты и отчет об обнаружениях нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-140">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="3d4f3-141">Просмотр отчетов по безопасности электронной почты в безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="3d4f3-141">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="3d4f3-142">**Обозреватель** (также называются Explorer угроз, входит в [Анализ угроз Office 365](office-365-ti.md))</span><span class="sxs-lookup"><span data-stu-id="3d4f3-142">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Threat Intelligence](office-365-ti.md))</span></span>     | [<span data-ttu-id="3d4f3-143">Используйте проводник в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="3d4f3-143">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="3d4f3-p106">**Результаты анализа и EOP** (Это настраиваемый отчет, создаваемые с помощью PowerShell). В этом отчете содержатся сведения, такие как домена, дата, тип события, направление, действие и количество сообщений.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-p106">**EOP and ATP results** (This is a custom report you generate by using PowerShell). This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="3d4f3-146">Справочник командлетов Get-MailTrafficATPReport</span><span class="sxs-lookup"><span data-stu-id="3d4f3-146">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="3d4f3-p107">**Обнаружение программ EOP и анализа** (Это настраиваемый отчет, создаваемые с помощью PowerShell). Этот отчет содержит подробные сведения о вредоносных файлов или URL-адреса, попытки, олицетворения и других потенциальных угроз в электронной почте или файлы.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-p107">**EOP and ATP detections** (This is a custom report you generate by using PowerShell). This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="3d4f3-149">Справочник командлетов Get-MailDetailATPReport</span><span class="sxs-lookup"><span data-stu-id="3d4f3-149">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="3d4f3-150">Какие разрешения необходимы для просмотра отчетов анализа?</span><span class="sxs-lookup"><span data-stu-id="3d4f3-150">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="3d4f3-151">Для просмотра и использования отчетов, описанного в данной статье **необходимо иметь соответствующие роли, назначенные в обоих системы &amp; центре соответствия требованиям и Центр администрирования Exchange**.</span><span class="sxs-lookup"><span data-stu-id="3d4f3-151">In order to view and use the reports described in this article, **you must have an appropriate role assigned in both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="3d4f3-152">Для системы безопасности &amp; центре соответствия требованиям, вы должны использовать одну из следующих роли, назначенные:</span><span class="sxs-lookup"><span data-stu-id="3d4f3-152">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="3d4f3-153">Управление организацией</span><span class="sxs-lookup"><span data-stu-id="3d4f3-153">Organization Management</span></span>
    - <span data-ttu-id="3d4f3-154">администратор безопасности (Security Administrator).</span><span class="sxs-lookup"><span data-stu-id="3d4f3-154">Security Administrator</span></span>
    - <span data-ttu-id="3d4f3-155">Средство чтения безопасности</span><span class="sxs-lookup"><span data-stu-id="3d4f3-155">Security Reader</span></span>

- <span data-ttu-id="3d4f3-156">Для Exchange Online должны использовать одну из следующих роли, назначенные:</span><span class="sxs-lookup"><span data-stu-id="3d4f3-156">For Exchange Online, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="3d4f3-157">Управление организацией</span><span class="sxs-lookup"><span data-stu-id="3d4f3-157">Organization Management</span></span>
    - <span data-ttu-id="3d4f3-158">Управление организацией с правами только на просмотр</span><span class="sxs-lookup"><span data-stu-id="3d4f3-158">View-only Organization Management</span></span>
    - <span data-ttu-id="3d4f3-159">Роль получателей с правами только на просмотр</span><span class="sxs-lookup"><span data-stu-id="3d4f3-159">View-Only Recipients role</span></span>
    - <span data-ttu-id="3d4f3-160">Управление соответствием требованиям</span><span class="sxs-lookup"><span data-stu-id="3d4f3-160">Compliance Management</span></span>

<span data-ttu-id="3d4f3-161">Дополнительные сведения, можно найти в следующих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="3d4f3-161">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="3d4f3-162">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="3d4f3-162">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="3d4f3-163">Разрешения компонентов в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3d4f3-163">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="3d4f3-164">Что делать, если отчеты не отображаются данные?</span><span class="sxs-lookup"><span data-stu-id="3d4f3-164">What if the reports aren't showing data?</span></span>

<span data-ttu-id="3d4f3-p108">Если вы не видите данных в отчетах анализа, проверьте, что политиках правильность установки. Вашей организации должны иметь [безопасных ссылок анализа политик](set-up-atp-safe-links-policies.md) и [политик ATP безопасные вложения](set-up-atp-safe-attachments-policies.md) , определенные в порядке для защиты ATP, чтобы обеспечить выполнение. Также обратиться к разделу [Защита от нежелательной почты и вредоносных программ в Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="3d4f3-p108">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="3d4f3-168">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3d4f3-168">Related topics</span></span>

[<span data-ttu-id="3d4f3-169">Отчеты и полезные сведения о безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="3d4f3-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="3d4f3-170">Создать расписание для отчета в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="3d4f3-170">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="3d4f3-171">Установка и загрузка пользовательского отчета в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="3d4f3-171">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

