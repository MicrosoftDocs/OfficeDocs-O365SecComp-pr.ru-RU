---
title: Отчеты и трассировка сообщений в Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: В Microsoft Exchange Online Protection (EOP) доступно множество различных отчетов, с помощью которых вы сможете определить общее состояние и работоспособность вашей организации. Существуют также средства, позволяющие устранять неполадки с определенными событиями (например, если сообщение не приходит указанным получателям), а также отчеты аудита для целей соответствия требованиями. В следующей таблице описаны отчеты и средства устранения неполадок, доступные администраторам EOP.
ms.openlocfilehash: 01a09b2b4b72161352af3793686c6cc888e44e29
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027146"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a><span data-ttu-id="8aab6-105">Отчеты и трассировка сообщений в Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8aab6-105">Reporting and message trace in Exchange Online Protection</span></span>

<span data-ttu-id="8aab6-p102">Microsoft Exchange Online Protection (EOP) предлагает различные отчеты, которые помогут вам определить общее состояние и работоспособность организации. Существует также средства, помогающие устранять определенные события (например, сообщения, поступающие не для его указанным получателям) и аудит отчетов для обеспечения соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="8aab6-p102">Microsoft Exchange Online Protection (EOP) offers many different reports that can help you determine the overall status and health of your organization. There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span> 

## <a name="usage-reports"></a><span data-ttu-id="8aab6-108">Отчеты об использовании</span><span class="sxs-lookup"><span data-stu-id="8aab6-108">Usage reports</span></span>

<span data-ttu-id="8aab6-109">**Активность группы Office 365** Просмотр сведений о число групп Office 365, которые создаются и используются.</span><span class="sxs-lookup"><span data-stu-id="8aab6-109">**Office 365 groups activity** View information about the number of Office 365 groups that are created and used.</span></span>  

<span data-ttu-id="8aab6-110">**Действие электронной почты** Просмотр сведений о количестве сообщений, отправляемых, полученных и чтение в рамках всей организации, а также с определенным пользователям.</span><span class="sxs-lookup"><span data-stu-id="8aab6-110">**Email activity** View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>  

<span data-ttu-id="8aab6-p103">**Использование приложения электронной почты** Просмотр сведений о приложения электронной почты, которые используются. Это быть общее число подключений для каждого приложения и версии Outlook, на которых выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="8aab6-p103">**Email app usage** View information about the email apps that are used. This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>  

<span data-ttu-id="8aab6-113">**Использование почтового ящика** Просмотр сведений о хранения, используемый, потребление квот, число элементов и последнего действия (отправки или операции чтения) для почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="8aab6-113">**Mailbox usage** View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="8aab6-114">Воспользуйтесь следующими ресурсами для получения дополнительных сведений:</span><span class="sxs-lookup"><span data-stu-id="8aab6-114">See the following resources for more information:</span></span>

- [<span data-ttu-id="8aab6-115">Office 365 отчетов в центре администрирования — Office 365 групп</span><span class="sxs-lookup"><span data-stu-id="8aab6-115">Office 365 Reports in the admin center - Office 365 groups</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [<span data-ttu-id="8aab6-116">Office 365 отчеты в центре администрирования — действие электронной почты</span><span class="sxs-lookup"><span data-stu-id="8aab6-116">Office 365 Reports in the Admin Center - Email activity</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [<span data-ttu-id="8aab6-117">Office 365 отчеты в центре администрирования — использование приложений электронной почты</span><span class="sxs-lookup"><span data-stu-id="8aab6-117">Office 365 Reports in the Admin Center - Email apps usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [<span data-ttu-id="8aab6-118">Office 365 отчеты в центре администрирования — использование почтового ящика</span><span class="sxs-lookup"><span data-stu-id="8aab6-118">Office 365 Reports in the Admin Center - Mailbox usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-office-365-admin-center"></a><span data-ttu-id="8aab6-119">Безопасность &amp; создания отчетов в центре администрирования Office 365</span><span class="sxs-lookup"><span data-stu-id="8aab6-119">Security &amp; compliance reports in the Office 365 admin center</span></span>

<span data-ttu-id="8aab6-120">Эти расширенные отчеты предоставляют интерактивный интерфейс отчетов администраторам EOP, в том числе сводную информацию и возможность детального для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="8aab6-120">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>  

<span data-ttu-id="8aab6-121">**Дополнительные защиту от угроз (ATP)** Просмотр сведений о ссылок надежных и безопасных вложений, которые входят в состав пакета анализа.</span><span class="sxs-lookup"><span data-stu-id="8aab6-121">**Advanced Threat Protection (ATP)** View information about safe links and safe attachments that are part of ATP.</span></span>  

<span data-ttu-id="8aab6-122">**EOP** Просмотр сведений о обнаружения вредоносных программ, подложный почты, числом обнаруженных нежелательных сообщений и поток обработки почты в вашу организацию и из.</span><span class="sxs-lookup"><span data-stu-id="8aab6-122">**EOP** View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>  

[<span data-ttu-id="8aab6-123">Просмотр отчетов для расширенного защиту от угроз и Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8aab6-123">View reports for Advanced Threat Protection and Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="8aab6-124">Настраиваемые отчеты с помощью Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8aab6-124">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="8aab6-125">Программное создание отчетов, доступных в центре администрирования Office 365 с помощью Microsoft Graph видеть подразделов работы [с Office 365 отчеты об использовании в Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span><span class="sxs-lookup"><span data-stu-id="8aab6-125">Programmatically create reports that are available in the Office 365 admin center by using Microsoft Graph  See the subtopics of [Working with Office 365 usage reports in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span></span> 

##<a name="custom-reports-using-reporting-web-services"></a><span data-ttu-id="8aab6-126">Создание пользовательских отчетов с помощью веб-служб отчетов</span><span class="sxs-lookup"><span data-stu-id="8aab6-126">Custom reports using reporting web services</span></span>

<span data-ttu-id="8aab6-127">Программное создание отчетов из доступных Exchange Online Protection PowerShell командлеты отчетов с помощью фильтрации запросов REST/ODATA2.</span><span class="sxs-lookup"><span data-stu-id="8aab6-127">Programmatically create reports from the available Exchange Online Protection PowerShell reporting cmdlets by using REST/ODATA2 query filtering.</span></span>

<span data-ttu-id="8aab6-128">Просмотреть [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span><span class="sxs-lookup"><span data-stu-id="8aab6-128">See [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span></span> 

##<a name="message-trace"></a><span data-ttu-id="8aab6-129">Трассировка сообщений</span><span class="sxs-lookup"><span data-stu-id="8aab6-129">Message trace</span></span>

<span data-ttu-id="8aab6-p104">Следующие сообщения электронной почты, проходящих через службу EOP. Можно определить, если сообщение электронной почты было получено, отклонено, отложенной или доставлено службой. Также показаны действия, которые были сделаны в сообщении перед его связаться с вами его конечное состояние.</span><span class="sxs-lookup"><span data-stu-id="8aab6-p104">Follows email messages as they travel through EOP. You can determine if an email message was received, rejected, deferred, or delivered by the service. It also shows what actions were taken on the message before it reached its final status.</span></span>  

<span data-ttu-id="8aab6-133">Эти сведения помогут вам оперативно отвечать на вопросы пользователей, устранять проблемы с потоком обработки почты и проверять изменения политик, а также избавляет от необходимости обращаться за помощью в службу технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="8aab6-133">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>  

<span data-ttu-id="8aab6-134">Просмотреть [Отслеживание сообщений электронной почты](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span><span class="sxs-lookup"><span data-stu-id="8aab6-134">See [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span></span> 

## <a name="audit-logging"></a><span data-ttu-id="8aab6-135">Ведение журнала аудита</span><span class="sxs-lookup"><span data-stu-id="8aab6-135">Audit logging</span></span>

<span data-ttu-id="8aab6-p105">Отслеживает определенные изменения, внесенные администраторами с вашей организации. Эти отчеты, которые помогут Устранение проблем настройки или найти причину безопасности или проблем, связанных с соответствием требованиям.  Просмотр [отчетов о аудит в EOP](auditing-reports-in-eop.md)</span><span class="sxs-lookup"><span data-stu-id="8aab6-p105">Tracks specific changes made by admins to your organization. These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.  see [Auditing reports in EOP](auditing-reports-in-eop.md)</span></span> 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="8aab6-139">Отчеты и трассировка сообщений: доступность данных и задержка</span><span class="sxs-lookup"><span data-stu-id="8aab6-139">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="8aab6-140">В таблице ниже описано, когда и в течение какого времени доступны данные отчетов и трассировки сообщений EOP.</span><span class="sxs-lookup"><span data-stu-id="8aab6-140">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="8aab6-141">**Тип отчета**</span><span class="sxs-lookup"><span data-stu-id="8aab6-141">**Report type**</span></span> <br/> |<span data-ttu-id="8aab6-142">**Доступные данные (период просмотра)**</span><span class="sxs-lookup"><span data-stu-id="8aab6-142">**Data available for (look back period)**</span></span> <br/> |<span data-ttu-id="8aab6-143">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="8aab6-143">**Latency**</span></span> <br/> |
|<span data-ttu-id="8aab6-144">Сводные отчеты о защите почты</span><span class="sxs-lookup"><span data-stu-id="8aab6-144">Mail protection summary reports</span></span>  <br/> |<span data-ttu-id="8aab6-145">90 дней</span><span class="sxs-lookup"><span data-stu-id="8aab6-145">90 days</span></span>  <br/> |<span data-ttu-id="8aab6-p106">Агрегирование данных сообщений в основном выполняется в течение 24-48 часов. Постепенное внесение незначительных изменений при агрегировании может занять до 5 дней.</span><span class="sxs-lookup"><span data-stu-id="8aab6-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>  <br/> |
|<span data-ttu-id="8aab6-148">Подробные отчеты о защите почты</span><span class="sxs-lookup"><span data-stu-id="8aab6-148">Mail protection detail reports</span></span>  <br/> |<span data-ttu-id="8aab6-149">90 дней</span><span class="sxs-lookup"><span data-stu-id="8aab6-149">90 days</span></span>  <br/> |<span data-ttu-id="8aab6-p107">Более подробные данные с давностью не более 7 дней появятся в течение 24 часов, но могут быть неполными в течение 48 часов. Постепенное внесение незначительных изменений может занять до 5 дней.</span><span class="sxs-lookup"><span data-stu-id="8aab6-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span>  <br/> <span data-ttu-id="8aab6-152">Для отображения подробных отчетов о сообщениях с давностью более 7 дней может понадобиться несколько часов.</span><span class="sxs-lookup"><span data-stu-id="8aab6-152">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
|<span data-ttu-id="8aab6-153">Данные о трассировке сообщений</span><span class="sxs-lookup"><span data-stu-id="8aab6-153">Message trace data</span></span>  <br/> |<span data-ttu-id="8aab6-154">90 дней</span><span class="sxs-lookup"><span data-stu-id="8aab6-154">90 days</span></span>  <br/> |<span data-ttu-id="8aab6-155">Трассировка сообщений с давностью менее 7 дней может занять от 5 до 30 минут.</span><span class="sxs-lookup"><span data-stu-id="8aab6-155">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span>  <br/> <span data-ttu-id="8aab6-156">Трассировка сообщений с давностью более 7 дней может занять несколько часов.</span><span class="sxs-lookup"><span data-stu-id="8aab6-156">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8aab6-157">Доступность и задержка данных аналогична запросам с помощью центра администрирования Office 365 или удаленной оболочки PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8aab6-157">Data availability and latency is the same whether requested via the Office 365 admin center or remote PowerShell.</span></span> 
  

