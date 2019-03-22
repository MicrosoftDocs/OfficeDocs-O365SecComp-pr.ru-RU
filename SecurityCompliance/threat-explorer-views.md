---
title: Представления обозревателя угроз
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/18/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.collection:
- M365-security-compliance
description: Узнайте о различных видах представлений, доступных в проводнике (также называемом обозревателем угроз) в составе Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: bcfa044db6844d9459b3dd62d9ced1cd37a999ec
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/21/2019
ms.locfileid: "30736469"
---
# <a name="threat-explorer-views"></a><span data-ttu-id="ecdbb-103">Представления обозревателя угроз</span><span class="sxs-lookup"><span data-stu-id="ecdbb-103">Threat Explorer views</span></span>

<span data-ttu-id="ecdbb-104">[Обозреватель угроз](use-explorer-in-security-and-compliance.md) — это мощное почти и почти безвозвратное средство, помогающее системам безопасности Teams исследовать и отвечать &amp; на угрозы в центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-104">[Threat Explorer](use-explorer-in-security-and-compliance.md) is a powerful, near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="ecdbb-105">В проводнике отображаются сведения об обнаруженных вредоносных программах и фишинге в Office 365, а также о других угрозах безопасности и рисках для Организации.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-105">Explorer displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span> 

<span data-ttu-id="ecdbb-106">При первом открытии проводника представление по умолчанию показывает обнаружение вредоносных программ электронной почты за прошедшие 7 дней.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-106">When you first open Explorer, the default view shows email malware detections for the past 7 days.</span></span> 

![Обозреватель угроз](media/ThreatExplorerFirstOpened.png)

<span data-ttu-id="ecdbb-108">В проводнике также могут отображаться функции защиты системы безопасности в Office 365, в том числе [безопасные ссылки](atp-safe-links.md) и [безопасные вложения](atp-safe-attachments.md) , которые можно изменить для отображения данных за прошедшие 30 дней.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-108">Explorer can also show security protection features in Office 365, including [Safe Links](atp-safe-links.md) and [Safe Attachments](atp-safe-attachments.md) and can be modified to show data for the past 30 days.</span></span> 

> [!NOTE]
> <span data-ttu-id="ecdbb-109">Если вы используете пробную подписку на Office 365 Advanced Threat protection (план 2) или Office 365 в ~, вы увидите только обнаружение и данные электронной почты за прошедшие 7 дней.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-109">If you have a trial subscription for Office 365 Advanced Threat Protection Plan 2 or Office 365 E5, you will only see detections and email data for the past 7 days.</span></span>
  
<span data-ttu-id="ecdbb-110">Используйте меню **вид** для изменения отображаемых сведений.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-110">Use the **View** menu to change what information is displayed.</span></span> <span data-ttu-id="ecdbb-111">Подсказки помогут определить, какое представление использовать.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-111">Tooltips help you determine which view to use.</span></span>
  
![Меню "вид" обозревателя угроз](media/ThreatExplorerViewMenu.png)

<span data-ttu-id="ecdbb-113">После выбора представления можно применить фильтры и настроить запросы для дальнейшего анализа.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-113">Once you have selected a view, you can apply filters and set up queries to conduct further analysis.</span></span> <span data-ttu-id="ecdbb-114">В следующих разделах представлен краткий обзор различных представлений, доступных в проводнике.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-114">The following sections provide a brief overview of the various views available in Explorer.</span></span>  

## <a name="email--malware"></a><span data-ttu-id="ecdbb-115">Вредоносная программа электронной почты _Гт_</span><span class="sxs-lookup"><span data-stu-id="ecdbb-115">Email > Malware</span></span>

<span data-ttu-id="ecdbb-116">Чтобы просмотреть этот отчет, в проводнике выберите пункт **Просмотр** > **вредоносных программ\*\*\*\*электронной почты** > .</span><span class="sxs-lookup"><span data-stu-id="ecdbb-116">To view this report, in Explorer, choose **View** > **Email** > **Malware**.</span></span> <span data-ttu-id="ecdbb-117">В этом представлении отображаются сведения о сообщениях электронной почты, которые были идентифицированы как содержащие вредоносные программы.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-117">This view shows information about email messages that were identified as containing malware.</span></span>  

![Просмотр данных о сообщении электронной почты, которое определено как вредоносное](media/ExplorerEmailMalwareMenu.png) 

<span data-ttu-id="ecdbb-119">Нажмите \*\*\*\* кнопку отправитель, чтобы открыть список параметров просмотра.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-119">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="ecdbb-120">Этот список используется для просмотра данных по отправителям, получателям, доменам отправителей, темам, технологиям обнаружения, состояниям защиты и т. д.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-120">Use this list to view data by sender, recipients, sender domain, subject, detection technology, protection status, and more.</span></span> 

<span data-ttu-id="ecdbb-121">Например, чтобы узнать, какие действия были выполнены с обнаруженными сообщениями электронной почты, выберите **состояние защиты** в списке.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-121">For example, to see what actions were taken on detected email messages, choose **Protection status** in the list.</span></span> <span data-ttu-id="ecdbb-122">Выберите параметр, а затем нажмите кнопку обновить, чтобы применить этот фильтр к отчету.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-122">Select an option, and then click the Refresh button to apply that filter to your report.</span></span>

![Параметры состояния защиты от угроз для обозревателя угроз](media/ThreatExplorerProtectionStatusOptions.png)

<span data-ttu-id="ecdbb-124">Под диаграммой просмотрите дополнительные сведения о конкретных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-124">Below the chart, view more details about specific messages.</span></span> <span data-ttu-id="ecdbb-125">При выборе элемента в списке открывается область "вылет", в которой можно узнать больше о выбранном элементе.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-125">When you select an item in the list, a fly-out pane opens, where you can learn more about the item you selected.</span></span> 

![Обозреватель угроз с открытым всплывающим окном](media/ThreatExplorerMalwareItemSelectedFlyout.png)

## <a name="email--phish"></a><span data-ttu-id="ecdbb-127">_Гт_ фишинга электронной почты</span><span class="sxs-lookup"><span data-stu-id="ecdbb-127">Email > Phish</span></span>

<span data-ttu-id="ecdbb-128">Чтобы просмотреть этот отчет, в проводнике выберите **Просмотр** > фишинга**электронной почты** > \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-128">To view this report, in Explorer, choose **View** > **Email** > **Phish**.</span></span> <span data-ttu-id="ecdbb-129">В этом представлении отображаются сообщения электронной почты, которые определены как попытки фишинга.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-129">This view shows email messages identified as phishing attempts.</span></span>  

![Просмотр данных о почтовых сообщениях, определенных как попытки фишинга](media/ThreatExplorerEmailPhish.png) 

<span data-ttu-id="ecdbb-131">Нажмите \*\*\*\* кнопку отправитель, чтобы открыть список параметров просмотра.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-131">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="ecdbb-132">Используйте этот список для просмотра данных по отправителям, получателям, доменам отправителей, IP-АДРЕСу отправителя, домену URL-адресов, нажмите вредоносности и дополнительно.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-132">Use this list to view data by sender, recipients, sender domain, sender IP, URL domain, click verdict, and more.</span></span> 

<span data-ttu-id="ecdbb-133">Например, чтобы узнать, какие действия были предприняты при нажатии на URL-адреса, идентифицированные как попытки фишинга, выберите **пункт вредоносности** в списке, выберите один или несколько параметров, а затем нажмите кнопку Обновить.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-133">For example, to see what actions were taken when people clicked on URLs that were identified as phishing attempts, choose **Click verdict** in the list, select one or more options, and then click the Refresh button.</span></span>

![Нажмите кнопку вредоносности Options (параметры) для отчета по фишингу](media/ThreatExplorerEmailPhishClickVerdictOptions.png)

<span data-ttu-id="ecdbb-135">Под диаграммой просмотрите дополнительные сведения о конкретных сообщениях, нажатии URL-адресов, URL-адреса и источник электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-135">Below the chart, view more details about specific messages, URL clicks, URLs, and email origin.</span></span> 

![URL-адреса, обнаруженные в сообщениях электронной почты как фишинг](media/ThreatExplorerEmailPhishURLs.png)

<span data-ttu-id="ecdbb-137">При выборе элемента в списке, например обнаруженного URL-адреса, открывается область "вылет", в которой можно узнать больше о выбранном элементе.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-137">When you select an item in the list, such as a URL that was detected, a fly-out pane opens, where you can learn more about the item you selected.</span></span> 

![Сведения об обнаруженном URL-АДРЕСе](media/ThreatExplorerEmailPhishURLDetails.png)

## <a name="email--user-reported"></a><span data-ttu-id="ecdbb-139">Сообщение электронной почты _Гт_ пользователя</span><span class="sxs-lookup"><span data-stu-id="ecdbb-139">Email > User-reported</span></span>

<span data-ttu-id="ecdbb-140">Чтобы просмотреть этот отчет, в проводнике выберите **Просмотр** > **сообщения электронной почты** > ,**отправленного пользователю**.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-140">To view this report, in Explorer, choose **View** > **Email** > **User-reported**.</span></span> <span data-ttu-id="ecdbb-141">В этом представлении отображаются сообщения электронной почты о том, что пользователи сообщили о нежелательной почте, нежелательной почте или фишинге.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-141">This view shows email that users have reported as junk, not junk, or phishing email.</span></span> 

![Сообщения электронной почты, сообщаемые пользователями](media/ThreatExplorerEmailUserReportedViewOptions.png) 

<span data-ttu-id="ecdbb-143">Нажмите \*\*\*\* кнопку отправитель, чтобы открыть список параметров просмотра.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-143">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="ecdbb-144">Этот список используется для просмотра сведений по отправителям, получателям, типам отчетов (определение пользователя на нежелательное, не спаме или фишинге) и многое другое.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-144">Use this list to view information by sender, recipients, report type (the user's determination that the email was junk, not junk, or phish), and more.</span></span> 

<span data-ttu-id="ecdbb-145">Например, чтобы просмотреть сведения о сообщениях электронной почты, которые были зарегистрированы как попытки фишинга, щелкните**тип отчета**по отправителю \*\*\*\* > , выберите пункт **Фишинг**, а затем нажмите кнопку Обновить.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-145">For example, to view information about email messages that were reported as phishing attempts, click **Sender** > **Report type**, select **Phish**, and then click the Refresh button.</span></span>

![Фишинг, выбранный для фильтра типа отчета](media/ThreatExplorerEmailUserReportedPhishSelected.png)

<span data-ttu-id="ecdbb-147">Под диаграммой просмотрите дополнительные сведения об определенных сообщениях электронной почты, таких как строка темы, IP-адрес отправителя, пользователь, который сообщил сообщение как нежелательное, нежелательное или фишинг, а также другие сведения.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-147">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

![Сообщения, которые были зарегистрированы как попытки фишинга](media/ThreatExplorerEmailPhishUserReportedPhishDetails.png)

<span data-ttu-id="ecdbb-149">Выберите элемент в списке, чтобы просмотреть дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-149">Select an item in the list to view additional details.</span></span>

## <a name="email--all-email"></a><span data-ttu-id="ecdbb-150">Электронная почта _Гт_ всю электронную почту</span><span class="sxs-lookup"><span data-stu-id="ecdbb-150">Email > All email</span></span>

<span data-ttu-id="ecdbb-151">Чтобы просмотреть этот отчет, в проводнике\*\*\*\* выберите **Просмотр** > **электронной почты по электронной почте** > .</span><span class="sxs-lookup"><span data-stu-id="ecdbb-151">To view this report, in Explorer, choose **View** > **Email** > **All mail**.</span></span> <span data-ttu-id="ecdbb-152">В этом представлении отображается представление действий с электронной почтой, в том числе сообщение электронной почты, которое определено как вредоносное по причине фишинга или вредоносных программ, а также для всех невредоносных сообщений (обычной электронной почты, спама и массовой почты).</span><span class="sxs-lookup"><span data-stu-id="ecdbb-152">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="ecdbb-153">Если вы получаете сообщение об ошибке, которое считывает **слишком много данных**, добавьте фильтр и при необходимости Сократите диапазон дат, который вы просматриваете.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-153">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="ecdbb-154">Чтобы применить фильтр, выберите **отправитель**, выберите элемент в списке, а затем нажмите кнопку Обновить.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-154">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="ecdbb-155">В нашем примере мы использовали **технологию обнаружения** в качестве фильтра (доступно несколько вариантов).</span><span class="sxs-lookup"><span data-stu-id="ecdbb-155">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="ecdbb-156">Просмотр сведений по отправителям, доменам отправителя, получателям, темам, вложениям filename, семействам вредоносных программ, состоянию защиты (действия, выполняемые функциями и политиками защиты от угроз в Office 365), технология обнаружения (способ обнаружения вредоносных программ) и превышает.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-156">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Просмотр данных об обнаруженных сообщениях электронной почты с помощью технологии обнаружения](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="ecdbb-158">Под диаграммой просмотрите дополнительные сведения об определенных сообщениях электронной почты, таких как строка темы, получатель, отправитель, состояние и т. д.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-158">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="ecdbb-159">_Гт_ вредоносных программ для контента</span><span class="sxs-lookup"><span data-stu-id="ecdbb-159">Content > Malware</span></span>

<span data-ttu-id="ecdbb-160">Чтобы просмотреть этот отчет, в проводнике выберите **Просмотр** > \*\*\*\* > **вредоносных программ**.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-160">To view this report, in Explorer, choose **View** > **Content** > **Malware**.</span></span> <span data-ttu-id="ecdbb-161">В этом представлении показаны файлы, которые были определены как вредоносные [в Office 365 Advanced Threat Protection в SharePoint Online, OneDrive для бизнеса и Microsoft Teams](atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="ecdbb-161">This view shows files that were identified as malicious by [Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="ecdbb-162">Просмотр сведений о семействе вредоносных программ, технологии обнаружения (способе обнаружения вредоносных программ) и рабочей нагрузке (OneDrive, SharePoint или Teams).</span><span class="sxs-lookup"><span data-stu-id="ecdbb-162">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Просмотр данных об обнаруженных вредоносных программах](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="ecdbb-164">Под диаграммой просмотрите дополнительные сведения о конкретных файлах, таких как имя файла вложения, Рабочая нагрузка, размер файла, Последнее изменение файла и т. д.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-164">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="click-to-filter-capabilities"></a><span data-ttu-id="ecdbb-165">Возможности "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="ecdbb-165">Click-to-filter capabilities</span></span>

<span data-ttu-id="ecdbb-166">С помощью проводника можно применить фильтр по щелчку.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-166">With Explorer, you can apply a filter in a click.</span></span> <span data-ttu-id="ecdbb-167">Щелкните элемент в условных обозначениях, и этот элемент становится фильтром для отчета.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-167">Click an item in the legend, and that item becomes a filter for the report.</span></span> <span data-ttu-id="ecdbb-168">Например, предположим, что вы ищете представление вредоносных программ в проводнике:</span><span class="sxs-lookup"><span data-stu-id="ecdbb-168">For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Перейти к обозревателю \> управления угрозами](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="ecdbb-170">Выбор **ATP детонации** в этой диаграмме приводит к представлению следующего вида:</span><span class="sxs-lookup"><span data-stu-id="ecdbb-170">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorer фильтрует, чтобы отображались только результаты детонации ATP.](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="ecdbb-172">В этом представлении теперь вы ищете данные для файлов, которые были обезвреженои [безопасными вложенияМи Office 365 ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="ecdbb-172">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="ecdbb-173">Под диаграммой можно просмотреть подробные сведения об определенных сообщениях электронной почты, для которых были обнаружены вложения, обнаруженные безопасными вложениями ATP.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-173">Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Конкретные сведения о сообщениях электронной почты с обнаруженными вложениями](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="ecdbb-175">При выборе одного или нескольких элементов активируется меню **действия** , в котором предлагается несколько вариантов выбора для выбранных элементов.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-175">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![Выбор элемента активирует меню "действия"](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="ecdbb-177">Возможность фильтрации в нажатии и переходе к определенным сведениям может значительно сэкономить время при изучении угроз.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-177">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>

## <a name="queries-and-filters"></a><span data-ttu-id="ecdbb-178">Запросы и фильтры</span><span class="sxs-lookup"><span data-stu-id="ecdbb-178">Queries and filters</span></span>

<span data-ttu-id="ecdbb-179">В проводнике предусмотрено несколько мощных фильтров и запросов, которые позволяют переходить к детальным сведениям, таким как лучшие целевые пользователи, основные семейства вредоносных программ, технологию обнаружения и многое другое.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-179">Explorer has several powerful filters and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="ecdbb-180">Каждый вид отчета предлагает различные способы просмотра и изучения данных.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-180">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ecdbb-181">Не используйте подстановочные знаки, например звездочку (\*) или вопросительный знак (?), на панели запросов проводника.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-181">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), in the query bar for Explorer.</span></span> <span data-ttu-id="ecdbb-182">При поиске по полю Тема для сообщений электронной почты Explorer выполняет частичные совпадения и передает результаты, аналогичные условиям поиска с использованием подстановочных знаков.</span><span class="sxs-lookup"><span data-stu-id="ecdbb-182">When you search on the Subject field for email messages, Explorer will perform partial matching and yield results similar to a wildcard search.</span></span>
