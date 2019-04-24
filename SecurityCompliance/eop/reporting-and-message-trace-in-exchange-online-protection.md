---
title: Отчеты и трассировка сообщений в Exchange Online Protection
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 12/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f40253f2-50a1-426e-9979-be74ba74cb61
description: В Microsoft Exchange Online Protection (EOP) доступно множество различных отчетов, с помощью которых вы сможете определить общее состояние и работоспособность вашей организации. Существуют также средства, позволяющие устранять неполадки с определенными событиями (например, если сообщение не приходит указанным получателям), а также отчеты аудита для целей соответствия требованиями. В следующей таблице описаны отчеты и средства устранения неполадок, доступные администраторам EOP.
ms.openlocfilehash: fcefa14991d074f1f4459007c16dd7f4df1cedd1
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256277"
---
# <a name="reporting-and-message-trace-in-exchange-online-protection"></a><span data-ttu-id="0552f-105">Отчеты и трассировка сообщений в Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="0552f-105">Reporting and message trace in Exchange Online Protection</span></span>

<span data-ttu-id="0552f-106">В Microsoft Exchange Online Protection (EOP) доступно множество различных отчетов, с помощью которых вы сможете определить общее состояние и работоспособность вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0552f-106">Microsoft Exchange Online Protection (EOP) offers many different reports that can help you determine the overall status and health of your organization.</span></span> <span data-ttu-id="0552f-107">Существуют также средства, позволяющие устранять неполадки с определенными событиями (например, если сообщение не приходит указанным получателям), а также отчеты аудита для целей соответствия требованиями.</span><span class="sxs-lookup"><span data-stu-id="0552f-107">There are also tools to help you troubleshoot specific events (such as a message not arriving to its intended recipients), and auditing reports to aid with compliance requirements.</span></span> 

## <a name="usage-reports"></a><span data-ttu-id="0552f-108">Отчеты об использовании</span><span class="sxs-lookup"><span data-stu-id="0552f-108">Usage reports</span></span>

<span data-ttu-id="0552f-109">**Действия с группами Office 365** Просмотр сведений о количестве созданных и используемых групп Office 365.</span><span class="sxs-lookup"><span data-stu-id="0552f-109">**Office 365 groups activity** View information about the number of Office 365 groups that are created and used.</span></span>  

<span data-ttu-id="0552f-110">**Действия с электронной почтой** Просмотр сведений о количестве отправленных, получаемых и прочтенных сообщений в Организации и определенных пользователях.</span><span class="sxs-lookup"><span data-stu-id="0552f-110">**Email activity** View information about the number of messages sent, received and read in your whole organization, and by specific users.</span></span>  

<span data-ttu-id="0552f-111">**Использование почтовых приложений** Просмотр сведений о почтовых приложениях, которые используются.</span><span class="sxs-lookup"><span data-stu-id="0552f-111">**Email app usage** View information about the email apps that are used.</span></span> <span data-ttu-id="0552f-112">Сюда входят общее число подключений для каждого приложения и версии Outlook, которые подключаются.</span><span class="sxs-lookup"><span data-stu-id="0552f-112">This include the total number of connections for each app, and the versions of Outlook that are connecting.</span></span>  

<span data-ttu-id="0552f-113">**Использование почтовоГо ящика** Просмотр сведений об используемом хранилище, потреблении квот, количестве элементов и последних действиях для почтовых ящиков ("Отправка" и "чтение").</span><span class="sxs-lookup"><span data-stu-id="0552f-113">**Mailbox usage** View information about storage used, quota consumption, item count, and last activity (send or read activity) for mailboxes.</span></span>

<span data-ttu-id="0552f-114">Дополнительные сведения можно найти в следующих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="0552f-114">See the following resources for more information:</span></span>

- [<span data-ttu-id="0552f-115">Отчеты об Office 365 в центре администрирования — группы Office 365</span><span class="sxs-lookup"><span data-stu-id="0552f-115">Office 365 Reports in the admin center - Office 365 groups</span></span>](https://go.microsoft.com/fwlink/p/?linkid=861610) 
- [<span data-ttu-id="0552f-116">Отчеты об Office 365 в центре администрирования — действие электронной почты</span><span class="sxs-lookup"><span data-stu-id="0552f-116">Office 365 Reports in the Admin Center - Email activity</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859706) 
- [<span data-ttu-id="0552f-117">Отчеты Office 365 в центре администрирования — использование поЧтовых приложений</span><span class="sxs-lookup"><span data-stu-id="0552f-117">Office 365 Reports in the Admin Center - Email apps usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859707)
- [<span data-ttu-id="0552f-118">Отчеты Office 365 в центре администрирования — использование поЧтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="0552f-118">Office 365 Reports in the Admin Center - Mailbox usage</span></span>](https://go.microsoft.com/fwlink/p/?linkid=859708)

## <a name="security-amp-compliance-reports-in-the-microsoft-365-admin-center"></a><span data-ttu-id="0552f-119">Отчеты &amp; о соответствии безопасности в центре администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0552f-119">Security &amp; compliance reports in the Microsoft 365 admin center</span></span>

<span data-ttu-id="0552f-120">Эти расширенные отчеты предоставляют Интерактивные отчеты для администраторов EOP, включающие сводную информацию и возможность детализации для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="0552f-120">These enhanced reports provide an interactive reporting experience for EOP admins, which includes summary information, and the ability to drill down for more details.</span></span>  

<span data-ttu-id="0552f-121">**Advanced Threat protection (ATP)** Просмотр сведений о безопасных ссылках и безопасных вложениях, которые входят в состав ATP.</span><span class="sxs-lookup"><span data-stu-id="0552f-121">**Advanced Threat Protection (ATP)** View information about safe links and safe attachments that are part of ATP.</span></span>  

<span data-ttu-id="0552f-122">**EOP** Просмотр сведений об обнаружении вредоносных программ, поддельной почте, обнаружении нежелательной почты и почтовых почтовых ящиков в Организации.</span><span class="sxs-lookup"><span data-stu-id="0552f-122">**EOP** View information about malware detections, spoofed mail, spam detections, and mail flow to and from your organization.</span></span>  

[<span data-ttu-id="0552f-123">Просмотр отчетов по расширенной защите от угроз и Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="0552f-123">View reports for Advanced Threat Protection and Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/p/?linkid=852409) 

##<a name="custom-reports-using-microsoft-graph"></a><span data-ttu-id="0552f-124">Настраиваемые отчеты с помощью Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="0552f-124">Custom reports using Microsoft Graph</span></span>

<span data-ttu-id="0552f-125">Программное создание отчетов, доступных в центре администрирования Майкрософт 365, с помощью Microsoft Graph Просмотр подразделов [о работе с отчетами об использовании Office 365 в Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span><span class="sxs-lookup"><span data-stu-id="0552f-125">Programmatically create reports that are available in the Microsoft 365 admin center by using Microsoft Graph  See the subtopics of [Working with Office 365 usage reports in Microsoft Graph](https://go.microsoft.com/fwlink/p/?linkid=865135)</span></span> 

##<a name="custom-reports-using-reporting-web-services"></a><span data-ttu-id="0552f-126">Настраиваемые отчеты с помощью веб-служб отчетов</span><span class="sxs-lookup"><span data-stu-id="0552f-126">Custom reports using reporting web services</span></span>

<span data-ttu-id="0552f-127">Программное создание отчетов из доступных командлетов отчетов Exchange Online Protection PowerShell с помощью фильтрации запросов REST/ODATA2.</span><span class="sxs-lookup"><span data-stu-id="0552f-127">Programmatically create reports from the available Exchange Online Protection PowerShell reporting cmdlets by using REST/ODATA2 query filtering.</span></span>

<span data-ttu-id="0552f-128">Просмотр [веб-служб отчетов Office 365](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span><span class="sxs-lookup"><span data-stu-id="0552f-128">See [Office 365 Reporting Web Services](https://go.microsoft.com/fwlink/p/?LinkId=279926)</span></span> 

##<a name="message-trace"></a><span data-ttu-id="0552f-129">Трассировка сообщений</span><span class="sxs-lookup"><span data-stu-id="0552f-129">Message trace</span></span>

<span data-ttu-id="0552f-130">Отслеживает сообщения электронной почты, проходящие через EOP.</span><span class="sxs-lookup"><span data-stu-id="0552f-130">Follows email messages as they travel through EOP.</span></span> <span data-ttu-id="0552f-131">Можно определить, было ли сообщение получено, отклонено, задержано или доставлено службой.</span><span class="sxs-lookup"><span data-stu-id="0552f-131">You can determine if an email message was received, rejected, deferred, or delivered by the service.</span></span> <span data-ttu-id="0552f-132">Кроме того, здесь показано, какие действия были выполнены над сообщением до достижения его последнего состояния.</span><span class="sxs-lookup"><span data-stu-id="0552f-132">It also shows what actions were taken on the message before it reached its final status.</span></span>  

<span data-ttu-id="0552f-133">Вы можете использовать эти сведения для эффективного ответа на вопросы пользователя, устранения проблем с потоками обработки почты, проверки изменений политик и устранения необходимости обращения в службу технической поддержки за помощью.</span><span class="sxs-lookup"><span data-stu-id="0552f-133">You can use this information to efficiently answer your user's questions, troubleshoot mail flow issues, validate policy changes, and alleviates the need to contact technical support for assistance.</span></span>  

<span data-ttu-id="0552f-134">Просмотр [трассировки сообщения электронной почты](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span><span class="sxs-lookup"><span data-stu-id="0552f-134">See [Trace an Email Message](http://technet.microsoft.com/library/0c83cde6-5b09-4106-8587-c200cdc59094.aspx)</span></span> 

## <a name="audit-logging"></a><span data-ttu-id="0552f-135">Ведение журнала аудита</span><span class="sxs-lookup"><span data-stu-id="0552f-135">Audit logging</span></span>

<span data-ttu-id="0552f-136">Отслеживает определенные изменения, выполненные администраторами в организации.</span><span class="sxs-lookup"><span data-stu-id="0552f-136">Tracks specific changes made by admins to your organization.</span></span> <span data-ttu-id="0552f-137">Эти отчеты позволяют устранять неполадки конфигурации и определять причины проблем безопасности или соблюдения требований.</span><span class="sxs-lookup"><span data-stu-id="0552f-137">These reports can help you troubleshoot configuration issues or find the cause of security or compliance-related problems.</span></span>  <span data-ttu-id="0552f-138">Просмотр [отчетов об аудите в EOP](auditing-reports-in-eop.md)</span><span class="sxs-lookup"><span data-stu-id="0552f-138">see [Auditing reports in EOP](auditing-reports-in-eop.md)</span></span> 


## <a name="reporting-and-message-trace-data-availability-and-latency"></a><span data-ttu-id="0552f-139">Отчеты и трассировка сообщений: доступность данных и задержка</span><span class="sxs-lookup"><span data-stu-id="0552f-139">Reporting and message trace data availability and latency</span></span>

<span data-ttu-id="0552f-140">В таблице ниже описано, когда и в течение какого времени доступны данные отчетов и трассировки сообщений EOP.</span><span class="sxs-lookup"><span data-stu-id="0552f-140">The following table describes when EOP reporting and message trace data is available and for how long.</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="0552f-141">**Тип отчета**</span><span class="sxs-lookup"><span data-stu-id="0552f-141">**Report type**</span></span> <br/> |<span data-ttu-id="0552f-142">**Доступные данные (период просмотра)**</span><span class="sxs-lookup"><span data-stu-id="0552f-142">**Data available for (look back period)**</span></span> <br/> |<span data-ttu-id="0552f-143">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="0552f-143">**Latency**</span></span> <br/> |
|<span data-ttu-id="0552f-144">Сводные отчеты о защите почты</span><span class="sxs-lookup"><span data-stu-id="0552f-144">Mail protection summary reports</span></span>  <br/> |<span data-ttu-id="0552f-145">90 дней</span><span class="sxs-lookup"><span data-stu-id="0552f-145">90 days</span></span>  <br/> |<span data-ttu-id="0552f-p106">Агрегирование данных сообщений в основном выполняется в течение 24-48 часов. Постепенное внесение незначительных изменений при агрегировании может занять до 5 дней.</span><span class="sxs-lookup"><span data-stu-id="0552f-p106">Message data aggregation is mostly complete within 24-48 hours. Some minor incremental aggregated changes may occur for up to 5 days.</span></span>  <br/> |
|<span data-ttu-id="0552f-148">Подробные отчеты о защите почты</span><span class="sxs-lookup"><span data-stu-id="0552f-148">Mail protection detail reports</span></span>  <br/> |<span data-ttu-id="0552f-149">90 дней</span><span class="sxs-lookup"><span data-stu-id="0552f-149">90 days</span></span>  <br/> |<span data-ttu-id="0552f-p107">Более подробные данные с давностью не более 7 дней появятся в течение 24 часов, но могут быть неполными в течение 48 часов. Постепенное внесение незначительных изменений может занять до 5 дней.</span><span class="sxs-lookup"><span data-stu-id="0552f-p107">For detail data that's less than 7 days old, data should appear within 24 hours but may not be complete until 48 hours. Some minor incremental changes may occur for up to 5 days.</span></span>  <br/> <span data-ttu-id="0552f-152">Для отображения подробных отчетов о сообщениях с давностью более 7 дней может понадобиться несколько часов.</span><span class="sxs-lookup"><span data-stu-id="0552f-152">To view detail reports for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
|<span data-ttu-id="0552f-153">Данные трассировки сообщений</span><span class="sxs-lookup"><span data-stu-id="0552f-153">Message trace data</span></span>  <br/> |<span data-ttu-id="0552f-154">90 дней</span><span class="sxs-lookup"><span data-stu-id="0552f-154">90 days</span></span>  <br/> |<span data-ttu-id="0552f-155">Трассировка сообщений с давностью менее 7 дней может занять от 5 до 30 минут.</span><span class="sxs-lookup"><span data-stu-id="0552f-155">When you run a message trace for messages that are less than 7 days old, the messages should appear within 5-30 minutes.</span></span>  <br/> <span data-ttu-id="0552f-156">Трассировка сообщений с давностью более 7 дней может занять несколько часов.</span><span class="sxs-lookup"><span data-stu-id="0552f-156">When you run a message trace for messages that are greater than 7 days old, results may take up to a few hours.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="0552f-157">Доступность данных и задержка это то же самое, что и при запросе через центр администрирования Microsoft 365 или удаленную среду PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0552f-157">Data availability and latency is the same whether requested via the Microsoft 365 admin center or remote PowerShell.</span></span> 
  

