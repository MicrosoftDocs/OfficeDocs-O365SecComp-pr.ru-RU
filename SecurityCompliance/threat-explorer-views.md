---
title: Представления в обозревателе угроз и обнаружения в режиме реального времени
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 03/18/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.collection:
- M365-security-compliance
description: Узнайте о различных видах представлений, доступных в обозревателе угроз и обнаружения в режиме реального времени.
ms.openlocfilehash: 71ec20daae45bee8385f24091850ea6223399eae
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600822"
---
# <a name="views-in-threat-explorer-and-real-time-detections"></a><span data-ttu-id="62bfa-103">Представления в обозревателе угроз и обнаружения в режиме реального времени</span><span class="sxs-lookup"><span data-stu-id="62bfa-103">Views in Threat Explorer and real-time detections</span></span>

![Обозреватель угроз](media/ThreatExplorerFirstOpened.png)

<span data-ttu-id="62bfa-105">[Обозреватель угроз](use-explorer-in-security-and-compliance.md) (и отчет об обнаружении в режиме реального времени) — это мощное средство в режиме реального времени, которое помогает системам безопасности Teams исследовать и отвечать на &amp; угрозы в центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="62bfa-105">[Threat Explorer](use-explorer-in-security-and-compliance.md) (and the real-time detections report) is a powerful, near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="62bfa-106">В проводнике (и отчете об обнаружении в режиме реального времени) отображаются сведения о потенциальных вредоносных и мошеннических программах в электронной почте и файлах в Office 365, а также о других угрозах безопасности и рисках для Организации.</span><span class="sxs-lookup"><span data-stu-id="62bfa-106">Explorer (and the real-time detections report) displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span> 

- <span data-ttu-id="62bfa-107">Если у вас есть [Office 365 Advanced Threat protection](office-365-atp.md) (ATP), то у вас есть проводник.</span><span class="sxs-lookup"><span data-stu-id="62bfa-107">If you have [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) Plan 2, then you have Explorer.</span></span>
- <span data-ttu-id="62bfa-108">Если у вас есть Office 365 ATP 1 (план 1), то у вас есть обнаружение в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="62bfa-108">If you have Office 365 ATP Plan 1, then you have real-time detections.</span></span>

<span data-ttu-id="62bfa-109">При первом открытии проводника (или отчета по обнаружениям в режиме реального времени) представление по умолчанию показывает обнаружение вредоносных программ по электронной почте за прошедшие 7 дней.</span><span class="sxs-lookup"><span data-stu-id="62bfa-109">When you first open Explorer (or the real-time detections report), the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="62bfa-110">В этом отчете также могут отображаться определения ATP, такие как вредоносные [ссылки](atp-safe-links.md), обнаруженные безопасными ссылками, а также вредоносные файлы, обнаруженные [безопасными вложениями](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="62bfa-110">This report can also show ATP detections, such as malicious URLs detected by [Safe Links](atp-safe-links.md), and malicious files detected by [Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="62bfa-111">Этот отчет можно изменить для отображения данных за прошедшие 30 дней (если вы не используете пробную подписку).</span><span class="sxs-lookup"><span data-stu-id="62bfa-111">This report can be modified to show data for the past 30 days (unless you are using a trial subscription).</span></span> <span data-ttu-id="62bfa-112">Пробные подписки будут включать данные только за прошедшие семь дней.</span><span class="sxs-lookup"><span data-stu-id="62bfa-112">Trial subscriptions will include data for the past seven days only.</span></span>

<span data-ttu-id="62bfa-113">Используйте меню **вид** для изменения отображаемых сведений.</span><span class="sxs-lookup"><span data-stu-id="62bfa-113">Use the **View** menu to change what information is displayed.</span></span> <span data-ttu-id="62bfa-114">Подсказки помогут определить, какое представление использовать.</span><span class="sxs-lookup"><span data-stu-id="62bfa-114">Tooltips help you determine which view to use.</span></span>
  
![Меню "вид" обозревателя угроз](media/ThreatExplorerViewMenu.png)

<span data-ttu-id="62bfa-116">После выбора представления можно применить фильтры и настроить запросы для дальнейшего анализа.</span><span class="sxs-lookup"><span data-stu-id="62bfa-116">Once you have selected a view, you can apply filters and set up queries to conduct further analysis.</span></span> <span data-ttu-id="62bfa-117">В следующих разделах представлен краткий обзор различных представлений, доступных в проводнике (или обнаружения в режиме реального времени).</span><span class="sxs-lookup"><span data-stu-id="62bfa-117">The following sections provide a brief overview of the various views available in Explorer (or real-time detections).</span></span>  

## <a name="email--malware"></a><span data-ttu-id="62bfa-118">Вредоносная > по электронной почте</span><span class="sxs-lookup"><span data-stu-id="62bfa-118">Email > Malware</span></span>

<span data-ttu-id="62bfa-119">Чтобы просмотреть этот отчет, в проводнике (или обнаружения в режиме реального времени) выберите **Просмотр** > **вредоносных программ\*\*\*\*электронной почты** > .</span><span class="sxs-lookup"><span data-stu-id="62bfa-119">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Malware**.</span></span> <span data-ttu-id="62bfa-120">В этом представлении отображаются сведения о сообщениях электронной почты, которые были идентифицированы как содержащие вредоносные программы.</span><span class="sxs-lookup"><span data-stu-id="62bfa-120">This view shows information about email messages that were identified as containing malware.</span></span>  

![Просмотр данных о сообщении электронной почты, которое определено как вредоносное](media/ExplorerEmailMalwareMenu.png) 

<span data-ttu-id="62bfa-122">Нажмите \*\*\*\* кнопку отправитель, чтобы открыть список параметров просмотра.</span><span class="sxs-lookup"><span data-stu-id="62bfa-122">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="62bfa-123">Этот список используется для просмотра данных по отправителям, получателям, доменам отправителей, темам, технологиям обнаружения, состояниям защиты и т. д.</span><span class="sxs-lookup"><span data-stu-id="62bfa-123">Use this list to view data by sender, recipients, sender domain, subject, detection technology, protection status, and more.</span></span> 

<span data-ttu-id="62bfa-124">Например, чтобы узнать, какие действия были выполнены с обнаруженными сообщениями электронной почты, выберите **состояние защиты** в списке.</span><span class="sxs-lookup"><span data-stu-id="62bfa-124">For example, to see what actions were taken on detected email messages, choose **Protection status** in the list.</span></span> <span data-ttu-id="62bfa-125">Выберите параметр, а затем нажмите кнопку обновить, чтобы применить этот фильтр к отчету.</span><span class="sxs-lookup"><span data-stu-id="62bfa-125">Select an option, and then click the Refresh button to apply that filter to your report.</span></span>

![Параметры состояния защиты от угроз для обозревателя угроз](media/ThreatExplorerProtectionStatusOptions.png)

<span data-ttu-id="62bfa-127">Под диаграммой просмотрите дополнительные сведения о конкретных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="62bfa-127">Below the chart, view more details about specific messages.</span></span> <span data-ttu-id="62bfa-128">При выборе элемента в списке открывается область "вылет", в которой можно узнать больше о выбранном элементе.</span><span class="sxs-lookup"><span data-stu-id="62bfa-128">When you select an item in the list, a fly-out pane opens, where you can learn more about the item you selected.</span></span> 

![Обозреватель угроз с открытым всплывающим окном](media/ThreatExplorerMalwareItemSelectedFlyout.png)

## <a name="email--phish"></a><span data-ttu-id="62bfa-130">Электронная почта > фишинга</span><span class="sxs-lookup"><span data-stu-id="62bfa-130">Email > Phish</span></span>

<span data-ttu-id="62bfa-131">Чтобы просмотреть этот отчет, в проводнике (или обнаружения в режиме реального времени) выберите **Просмотр** > фишинга**электронной почты** > \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="62bfa-131">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Phish**.</span></span> <span data-ttu-id="62bfa-132">В этом представлении отображаются сообщения электронной почты, которые определены как попытки фишинга.</span><span class="sxs-lookup"><span data-stu-id="62bfa-132">This view shows email messages identified as phishing attempts.</span></span>  

![Просмотр данных о почтовых сообщениях, определенных как попытки фишинга](media/ThreatExplorerEmailPhish.png) 

<span data-ttu-id="62bfa-134">Нажмите \*\*\*\* кнопку отправитель, чтобы открыть список параметров просмотра.</span><span class="sxs-lookup"><span data-stu-id="62bfa-134">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="62bfa-135">Используйте этот список для просмотра данных по отправителям, получателям, доменам отправителей, IP-адресу отправителя, домену URL-адресов, нажмите вредоносности и дополнительно.</span><span class="sxs-lookup"><span data-stu-id="62bfa-135">Use this list to view data by sender, recipients, sender domain, sender IP, URL domain, click verdict, and more.</span></span> 

<span data-ttu-id="62bfa-136">Например, чтобы узнать, какие действия были предприняты при нажатии на URL-адреса, идентифицированные как попытки фишинга, выберите **пункт вредоносности** в списке, выберите один или несколько параметров, а затем нажмите кнопку Обновить.</span><span class="sxs-lookup"><span data-stu-id="62bfa-136">For example, to see what actions were taken when people clicked on URLs that were identified as phishing attempts, choose **Click verdict** in the list, select one or more options, and then click the Refresh button.</span></span>

![Нажмите кнопку вредоносности Options (параметры) для отчета по фишингу](media/ThreatExplorerEmailPhishClickVerdictOptions.png)

<span data-ttu-id="62bfa-138">Под диаграммой просмотрите дополнительные сведения о конкретных сообщениях, нажатии URL-адресов, URL-адреса и источник электронной почты.</span><span class="sxs-lookup"><span data-stu-id="62bfa-138">Below the chart, view more details about specific messages, URL clicks, URLs, and email origin.</span></span> 

![URL-адреса, обнаруженные в сообщениях электронной почты как фишинг](media/ThreatExplorerEmailPhishURLs.png)

<span data-ttu-id="62bfa-140">При выборе элемента в списке, например обнаруженного URL-адреса, открывается область "вылет", в которой можно узнать больше о выбранном элементе.</span><span class="sxs-lookup"><span data-stu-id="62bfa-140">When you select an item in the list, such as a URL that was detected, a fly-out pane opens, where you can learn more about the item you selected.</span></span> 

![Сведения об обнаруженном URL-адресе](media/ThreatExplorerEmailPhishURLDetails.png)

## <a name="email--user-reported"></a><span data-ttu-id="62bfa-142">Электронная почта > о пользователях</span><span class="sxs-lookup"><span data-stu-id="62bfa-142">Email > User-reported</span></span>

<span data-ttu-id="62bfa-143">Чтобы просмотреть этот отчет, в проводнике (или обнаружения в режиме реального времени) выберите **Просмотр** > **электронной почты** > ,**отчет о пользователях**.</span><span class="sxs-lookup"><span data-stu-id="62bfa-143">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **User-reported**.</span></span> <span data-ttu-id="62bfa-144">В этом представлении отображаются сообщения электронной почты о том, что пользователи сообщили о нежелательной почте, нежелательной почте или фишинге.</span><span class="sxs-lookup"><span data-stu-id="62bfa-144">This view shows email that users have reported as junk, not junk, or phishing email.</span></span> 

![Сообщения электронной почты, сообщаемые пользователями](media/ThreatExplorerEmailUserReportedViewOptions.png) 

<span data-ttu-id="62bfa-146">Нажмите \*\*\*\* кнопку отправитель, чтобы открыть список параметров просмотра.</span><span class="sxs-lookup"><span data-stu-id="62bfa-146">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="62bfa-147">Этот список используется для просмотра сведений по отправителям, получателям, типам отчетов (определение пользователя на нежелательное, не спаме или фишинге) и многое другое.</span><span class="sxs-lookup"><span data-stu-id="62bfa-147">Use this list to view information by sender, recipients, report type (the user's determination that the email was junk, not junk, or phish), and more.</span></span> 

<span data-ttu-id="62bfa-148">Например, чтобы просмотреть сведения о сообщениях электронной почты, которые были зарегистрированы как попытки фишинга, щелкните**тип отчета**по отправителю \*\*\*\* > , выберите пункт **Фишинг**, а затем нажмите кнопку Обновить.</span><span class="sxs-lookup"><span data-stu-id="62bfa-148">For example, to view information about email messages that were reported as phishing attempts, click **Sender** > **Report type**, select **Phish**, and then click the Refresh button.</span></span>

![Фишинг, выбранный для фильтра типа отчета](media/ThreatExplorerEmailUserReportedPhishSelected.png)

<span data-ttu-id="62bfa-150">Под диаграммой просмотрите дополнительные сведения об определенных сообщениях электронной почты, таких как строка темы, IP-адрес отправителя, пользователь, который сообщил сообщение как нежелательное, нежелательное или фишинг, а также другие сведения.</span><span class="sxs-lookup"><span data-stu-id="62bfa-150">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

![Сообщения, которые были зарегистрированы как попытки фишинга](media/ThreatExplorerEmailPhishUserReportedPhishDetails.png)

<span data-ttu-id="62bfa-152">Выберите элемент в списке, чтобы просмотреть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="62bfa-152">Select an item in the list to view additional details.</span></span>

## <a name="email--all-email"></a><span data-ttu-id="62bfa-153">Электронная почта > всю почту</span><span class="sxs-lookup"><span data-stu-id="62bfa-153">Email > All email</span></span>

<span data-ttu-id="62bfa-154">Чтобы просмотреть этот отчет, в проводнике\*\*\*\* выберите **Просмотр** > **электронной почты по электронной почте** > .</span><span class="sxs-lookup"><span data-stu-id="62bfa-154">To view this report, in Explorer, choose **View** > **Email** > **All mail**.</span></span> <span data-ttu-id="62bfa-155">В этом представлении отображается представление действий с электронной почтой, в том числе сообщение электронной почты, которое определено как вредоносное по причине фишинга или вредоносных программ, а также для всех невредоносных сообщений (обычной электронной почты, спама и массовой почты).</span><span class="sxs-lookup"><span data-stu-id="62bfa-155">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="62bfa-156">Если вы получаете сообщение об ошибке, которое считывает **слишком много данных**, добавьте фильтр и при необходимости Сократите диапазон дат, который вы просматриваете.</span><span class="sxs-lookup"><span data-stu-id="62bfa-156">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="62bfa-157">Чтобы применить фильтр, выберите **отправитель**, выберите элемент в списке, а затем нажмите кнопку Обновить.</span><span class="sxs-lookup"><span data-stu-id="62bfa-157">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="62bfa-158">В нашем примере мы использовали **технологию обнаружения** в качестве фильтра (доступно несколько вариантов).</span><span class="sxs-lookup"><span data-stu-id="62bfa-158">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="62bfa-159">Просмотр сведений по отправителям, доменам отправителя, получателям, темам, вложениям filename, семействам вредоносных программ, состоянию защиты (действия, выполняемые функциями и политиками защиты от угроз в Office 365), технология обнаружения (способ обнаружения вредоносных программ) и превышает.</span><span class="sxs-lookup"><span data-stu-id="62bfa-159">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Просмотр данных об обнаруженных сообщениях электронной почты с помощью технологии обнаружения](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="62bfa-161">Под диаграммой просмотрите дополнительные сведения об определенных сообщениях электронной почты, таких как строка темы, получатель, отправитель, состояние и т. д.</span><span class="sxs-lookup"><span data-stu-id="62bfa-161">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="62bfa-162">Контент > вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="62bfa-162">Content > Malware</span></span>

<span data-ttu-id="62bfa-163">Чтобы просмотреть этот отчет, в проводнике (или обнаружения в режиме реального времени) выберите **Просмотр** > \*\*\*\* > **вредоносных программ**.</span><span class="sxs-lookup"><span data-stu-id="62bfa-163">To view this report, in Explorer (or real-time detections), choose **View** > **Content** > **Malware**.</span></span> <span data-ttu-id="62bfa-164">В этом представлении показаны файлы, которые были определены как вредоносные [в Office 365 Advanced Threat Protection в SharePoint Online, OneDrive для бизнеса и Microsoft Teams](atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="62bfa-164">This view shows files that were identified as malicious by [Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="62bfa-165">Просмотр сведений о семействе вредоносных программ, технологии обнаружения (способе обнаружения вредоносных программ) и рабочей нагрузке (OneDrive, SharePoint или Teams).</span><span class="sxs-lookup"><span data-stu-id="62bfa-165">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Просмотр данных об обнаруженных вредоносных программах](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="62bfa-167">Под диаграммой просмотрите дополнительные сведения о конкретных файлах, таких как имя файла вложения, Рабочая нагрузка, размер файла, Последнее изменение файла и т. д.</span><span class="sxs-lookup"><span data-stu-id="62bfa-167">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="click-to-filter-capabilities"></a><span data-ttu-id="62bfa-168">Возможности "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="62bfa-168">Click-to-filter capabilities</span></span>

<span data-ttu-id="62bfa-169">С помощью проводника (и обнаружения в режиме реального времени) можно применить фильтр по щелчку.</span><span class="sxs-lookup"><span data-stu-id="62bfa-169">With Explorer (and real-time detections), you can apply a filter in a click.</span></span> <span data-ttu-id="62bfa-170">Щелкните элемент в условных обозначениях, и этот элемент становится фильтром для отчета.</span><span class="sxs-lookup"><span data-stu-id="62bfa-170">Click an item in the legend, and that item becomes a filter for the report.</span></span> <span data-ttu-id="62bfa-171">Например, предположим, что вы ищете представление вредоносных программ в проводнике:</span><span class="sxs-lookup"><span data-stu-id="62bfa-171">For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Перейти к обозревателю \> управления угрозами](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="62bfa-173">Выбор **ATP детонации** в этой диаграмме приводит к представлению следующего вида:</span><span class="sxs-lookup"><span data-stu-id="62bfa-173">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorer фильтрует, чтобы отображались только результаты детонации ATP.](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="62bfa-175">В этом представлении теперь вы ищете данные для файлов, которые были обезвреженои [безопасными вложениями Office 365 ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="62bfa-175">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="62bfa-176">Под диаграммой можно просмотреть подробные сведения об определенных сообщениях электронной почты, для которых были обнаружены вложения, обнаруженные безопасными вложениями ATP.</span><span class="sxs-lookup"><span data-stu-id="62bfa-176">Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Конкретные сведения о сообщениях электронной почты с обнаруженными вложениями](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="62bfa-178">При выборе одного или нескольких элементов активируется меню **действия** , в котором предлагается несколько вариантов выбора для выбранных элементов.</span><span class="sxs-lookup"><span data-stu-id="62bfa-178">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![Выбор элемента активирует меню "действия"](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="62bfa-180">Возможность фильтрации в нажатии и переходе к определенным сведениям может значительно сэкономить время при изучении угроз.</span><span class="sxs-lookup"><span data-stu-id="62bfa-180">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>

## <a name="queries-and-filters"></a><span data-ttu-id="62bfa-181">Запросы и фильтры</span><span class="sxs-lookup"><span data-stu-id="62bfa-181">Queries and filters</span></span>

<span data-ttu-id="62bfa-182">В проводнике (и отчете об обнаружении в режиме реального времени) предусмотрено несколько мощных фильтров и запросов, позволяющих переходить к детальным сведениям, таким как самые популярные конечные пользователи, основные семейства вредоносных программ, технологию обнаружения и многое другое.</span><span class="sxs-lookup"><span data-stu-id="62bfa-182">Explorer (and the real-time detections report) has several powerful filters and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="62bfa-183">Каждый вид отчета предлагает различные способы просмотра и изучения данных.</span><span class="sxs-lookup"><span data-stu-id="62bfa-183">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62bfa-184">Не используйте подстановочные знаки, такие как звездочка (\*) или вопросительный знак (?), на панели запросов проводника (или обнаружения в режиме реального времени).</span><span class="sxs-lookup"><span data-stu-id="62bfa-184">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), in the query bar for Explorer (or real-time detections).</span></span> <span data-ttu-id="62bfa-185">При поиске в поле subject для сообщений электронной почты проводник (или обнаружение в режиме реального времени) выполняет частичные совпадения и дают результаты, аналогичные условиям поиска по шаблону.</span><span class="sxs-lookup"><span data-stu-id="62bfa-185">When you search on the Subject field for email messages, Explorer (or real-time detections) will perform partial matching and yield results similar to a wildcard search.</span></span>
