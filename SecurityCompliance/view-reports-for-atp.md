---
title: Просмотр отчетов для защиты расширенного Threat Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
description: Узнайте, как найти и использовать отчеты для Office 365 расширенного защиту от угроз безопасности &amp; центре соответствия требованиям.
ms.openlocfilehash: 4a76c6a5b888142dc4c35af432fa61916145d648
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454306"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="57515-103">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="57515-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="57515-p101">Если ваша организация имеет [Защиту от угроз для Office 365 Advanced](office-365-atp.md) (ATP) и у вас есть [соответствующие разрешения](#what-permissions-are-needed-to-view-these-reports), можно использовать несколько отчетов анализа в системы &amp; центре соответствия требованиям. (Перейдите к **отчетам** \> **панели мониторинга**.)</span><span class="sxs-lookup"><span data-stu-id="57515-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![Безопасность &amp; панели мониторинга в центре соответствия требованиям, которые помогут посмотреть, где работает расширенного защиту от угроз](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="57515-p102">Отчеты анализа включают [отчет о состоянии защиты от угроз](#threat-protection-status-report), [типы файлов ATP отчета](#atp-file-types-report)и [отчет о ликвидации ATP сообщения](#atp-message-disposition-report). В этой статье описываются отчетов анализа и приведены ссылки на [Дополнительные отчеты для просмотра](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="57515-p102">ATP reports include the [Threat protection status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="57515-109">Отчет о состоянии защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="57515-109">Threat protection status report</span></span>

<span data-ttu-id="57515-p103">Отчет о **состоянии защиты от угроз** — это один представление, который объединяет сведения о нежелательном содержимое и вредоносное электронной почты обнаруженных и блокирует Exchange Online и расширенный защиту от угроз. Отчет предоставляет сводный число уникальных электронных сообщений с вредоносного содержимого (файлы или URL-адреса), блокирует модуль защиты от вредоносных программ, [критическую автоматической очистки (ZAP)](zero-hour-auto-purge.md)и расширенный защиту от угроз функции, такие как [Безопасные ссылок анализа](atp-safe-links.md), [ATP Безопасные вложения](atp-safe-attachments.md)и [анализа фишинга возможностей в Office 365](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="57515-p103">The **Threat protection status** report is a single view that brings together information about malicious content and malicious email detected and blocked by Exchange Online and Advanced Threat Protection. The report provides an aggregated count of unique email messages with malicious content (files or URLs) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and Advanced Threat Protection features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities in Office 365](atp-anti-phishing.md).</span></span>
  
<span data-ttu-id="57515-112">Чтобы просмотреть отчет о состоянии защиты от угроз безопасности &amp; центре соответствия требованиям, чтобы перейти к **отчетам** \> **панели мониторинга** \> **состояние защиты от угроз**.</span><span class="sxs-lookup"><span data-stu-id="57515-112">To view the Threat protection status report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **Threat protection status**.</span></span>
  
![Отчет о состоянии защиты от угроз ATP](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="57515-114">Чтобы получить подробные сведения о состоянии в течение дня, наведите указатель мыши на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="57515-114">To get detailed status for a day, hover over the graph.</span></span>
  
![Состояние защиты от угроз анализа данных в течение дня](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="57515-p104">По умолчанию отчет о состоянии защиты от угроз отображаются данные за последние семь дней. Тем не менее можно выбрать **фильтры** и изменить диапазон дат для просмотра данных в течение 90 дней.</span><span class="sxs-lookup"><span data-stu-id="57515-p104">By default, the Threat protection status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Фильтры состояния защиты от угроз ATP](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="57515-119">В меню **Просмотр данных с** также можно использовать для изменения сведениях, отображаемых в отчете.</span><span class="sxs-lookup"><span data-stu-id="57515-119">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Параметры просмотра для отчета о состоянии защиты от угроз ATP](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="57515-121">Типы файлов ATP отчета</span><span class="sxs-lookup"><span data-stu-id="57515-121">ATP File Types report</span></span>

<span data-ttu-id="57515-122">**Типы файлов ATP** отчет отображает тип файлов, обнаруженных вредоносных как [Безопасные вложения ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="57515-122">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="57515-123">Чтобы просмотреть этот отчет в системы &amp; центре соответствия требованиям, чтобы перейти к **отчетам** \> **панели мониторинга** \> **ATP типов файлов**.</span><span class="sxs-lookup"><span data-stu-id="57515-123">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Типы файлов ATP отчета](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="57515-125">При наведении указателя на конкретный день, могут видеть декомпозиции типы вредоносных файлов, обнаруженных с [ATP безопасные вложения](atp-safe-attachments.md) и [защиты от нежелательной почты &amp; защита от вредоносных программ в Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="57515-125">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![Типы файлов анализа данных отчетов в течение дня](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="57515-127">Отчет о ликвидации ATP сообщения</span><span class="sxs-lookup"><span data-stu-id="57515-127">ATP Message Disposition report</span></span>

<span data-ttu-id="57515-128">Отчет о **Ликвидации ATP сообщение** показывает действия, предпринятые для сообщений электронной почты, обнаруженные как имеющий вредоносного содержимого.</span><span class="sxs-lookup"><span data-stu-id="57515-128">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="57515-129">Чтобы просмотреть этот отчет в безопасности &amp; центре соответствия требованиям, чтобы перейти к **отчетам** \> **панели мониторинга** \> **Ликвидации ATP сообщения**.</span><span class="sxs-lookup"><span data-stu-id="57515-129">To view this report, in the Security &amp; Compliance Center, go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Отчет о ликвидации ATP сообщения](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="57515-131">При наведении указателя на панели диаграммы, можно просмотреть действия, которые были созданы для вредоносным электронной почты для этого дня.</span><span class="sxs-lookup"><span data-stu-id="57515-131">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![Данные отчета о ликвидации ATP сообщений в течение дня](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="57515-133">Дополнительные отчеты для просмотра</span><span class="sxs-lookup"><span data-stu-id="57515-133">Additional reports to view</span></span>

<span data-ttu-id="57515-p105">Помимо анализа отчета, описанные в этой статье, [отчеты о безопасности электронной почты](view-email-security-reports.md) , доступны в безопасности &amp; центре соответствия требованиям. Отчеты о безопасности электронной почты включают [в начало отправителей и получателей отчетов](view-email-security-reports.md#top-senders-and-recipients-report), [Подделка почты отчета](view-email-security-reports.md#spoof-mail-report), [отчет об обнаружениях нежелательной почты](view-email-security-reports.md#spam-detections-report)и др.</span><span class="sxs-lookup"><span data-stu-id="57515-p105">In addition to the ATP reports described in this article, [email security reports](view-email-security-reports.md) are available in the Security &amp; Compliance Center. Email security reports include a [Top Senders and Recipients report](view-email-security-reports.md#top-senders-and-recipients-report), a [Spoof Mail report](view-email-security-reports.md#spoof-mail-report), a [Spam Detections report](view-email-security-reports.md#spam-detections-report), and more.</span></span>
  
<span data-ttu-id="57515-136">И, если в вашей организации есть [Анализ угроз Office 365](office-365-ti.md), можно также [с помощью обозревателя в системы &amp; центре соответствия требованиям](use-explorer-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="57515-136">And, if your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can also [Use Explorer in the Security &amp; Compliance Center](use-explorer-in-security-and-compliance.md).</span></span>
  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="57515-137">Какие разрешения необходимы для просмотра отчетов анализа?</span><span class="sxs-lookup"><span data-stu-id="57515-137">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="57515-138">Для просмотра и использования отчетов, описанного в данной статье, необходимо иметь соответствующие роли, назначенные в системы &amp; центре соответствия требованиям и в центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="57515-138">In order to view and use the reports described in this article, you must have an appropriate role assigned in the Security &amp; Compliance Center and in the Exchange Admin Center.</span></span>
  
|<span data-ttu-id="57515-139">**Группа ролей**</span><span class="sxs-lookup"><span data-stu-id="57515-139">**Role group**</span></span>|<span data-ttu-id="57515-140">**Где назначен**</span><span class="sxs-lookup"><span data-stu-id="57515-140">**Where assigned**</span></span>|<span data-ttu-id="57515-141">Просто вставьте трехмерную модель и вращайте ее на 360 градусов, чтобы добиться нужного результата.**Подробнее**</span><span class="sxs-lookup"><span data-stu-id="57515-141">**Learn more**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="57515-142">Один из следующих продуктов:</span><span class="sxs-lookup"><span data-stu-id="57515-142">One of the following:</span></span>  <br/>  <span data-ttu-id="57515-143">Управление организацией</span><span class="sxs-lookup"><span data-stu-id="57515-143">Organization Management</span></span>  <br/>  <span data-ttu-id="57515-144">администратор безопасности (Security Administrator).</span><span class="sxs-lookup"><span data-stu-id="57515-144">Security Administrator</span></span>  <br/>  <span data-ttu-id="57515-145">Средство чтения безопасности</span><span class="sxs-lookup"><span data-stu-id="57515-145">Security Reader</span></span>  <br/> |<span data-ttu-id="57515-146">Безопасность &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="57515-146">Security &amp; Compliance Center</span></span>  <br/> |[<span data-ttu-id="57515-147">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="57515-147">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md) <br/> |
| <span data-ttu-id="57515-148">Один из следующих продуктов:</span><span class="sxs-lookup"><span data-stu-id="57515-148">One of the following:</span></span>  <br/>  <span data-ttu-id="57515-149">Управление организацией</span><span class="sxs-lookup"><span data-stu-id="57515-149">Organization Management</span></span>  <br/>  <span data-ttu-id="57515-150">Управление организацией только с правом на просмотр</span><span class="sxs-lookup"><span data-stu-id="57515-150">View-only Organization Management</span></span>  <br/>  <span data-ttu-id="57515-151">Роль получателей с правами только на просмотр</span><span class="sxs-lookup"><span data-stu-id="57515-151">View-Only Recipients role</span></span>  <br/>  <span data-ttu-id="57515-152">Управление соответствием требованиям</span><span class="sxs-lookup"><span data-stu-id="57515-152">Compliance Management</span></span>  <br/> |<span data-ttu-id="57515-153">Центр администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="57515-153">Exchange Admin Center</span></span>  <br/> |[<span data-ttu-id="57515-154">Разрешения компонентов в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="57515-154">Feature permissions in Exchange Online</span></span>](https://technet.microsoft.com/library/jj200673%28v=exchg.150%29.aspx) <br/> |
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="57515-155">Что делать, если отчеты не отображаются данные?</span><span class="sxs-lookup"><span data-stu-id="57515-155">What if the reports aren't showing data?</span></span>

<span data-ttu-id="57515-p106">Если вы не видите данных в отчетах, проверьте, что политиках правильность установки. Вашей организации должны иметь [безопасных ссылок анализа политик](set-up-atp-safe-links-policies.md) и [политик ATP безопасные вложения](set-up-atp-safe-attachments-policies.md) , определенные в порядке для защиты ATP, чтобы обеспечить выполнение. Также обратиться к разделу [Защита от нежелательной почты и вредоносных программ в Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="57515-p106">If you are not seeing data in your reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="57515-159">Смежные темы</span><span class="sxs-lookup"><span data-stu-id="57515-159">Related topics</span></span>

[<span data-ttu-id="57515-160">Отчеты и полезные сведения о безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="57515-160">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="57515-161">Создать расписание для отчета в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="57515-161">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="57515-162">Установка и загрузка пользовательского отчета в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="57515-162">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

