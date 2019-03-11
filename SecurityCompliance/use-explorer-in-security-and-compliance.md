---
title: Использование обозревателя угроз в центре безопасности &amp; и соответствия требованиям
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/10/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Сведения о проводнике (также называемом обозревателе угроз) в центре &amp; безопасности и соответствия требованиям.
ms.openlocfilehash: 626d827712760aa0b7b6faf75d94f525cfe38dc2
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2019
ms.locfileid: "30524013"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="8762a-103">Использование обозревателя угроз в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8762a-103">Use Threat Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="8762a-104">Если в вашей организации используется [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md), а у вас есть необходимые разрешения, вы можете использовать обозреватель угроз для определения и анализа угроз.</span><span class="sxs-lookup"><span data-stu-id="8762a-104">If your organization has [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md), and you have the necessary permissions, you can use Threat Explorer to identify and analyze threats.</span></span> <span data-ttu-id="8762a-105">Например, вы можете определить и удалить вредоносное сообщение электронной почты, которое было доставлено, или увидеть вредоносные программы, перехваченные функциями безопасности Office 365.</span><span class="sxs-lookup"><span data-stu-id="8762a-105">For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features.</span></span> <span data-ttu-id="8762a-106">Обозреватель угроз (также называемый проводником) — это мощное практические средство в режиме реального времени, помогающее Teams исследовать и отвечать на угрозы &amp; в центре безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="8762a-106">Threat Explorer (also referred to as Explorer) is a powerful near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span>
  
![Перейти к обозревателю \> управления угрозами](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="8762a-108">Чтобы использовать обозреватель, в центре безопасности &amp; и соответствия требованиям откройте обозреватель **управления** \> \*\*\*\* угрозами.</span><span class="sxs-lookup"><span data-stu-id="8762a-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8762a-109">Office 365 Threat Intelligence теперь входит в план 2 Office 365 Advanced Threat protection (план 2) с дополнительными возможностями защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="8762a-109">Office 365 Threat Intelligence is now part of Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities.</span></span> <span data-ttu-id="8762a-110">Чтобы узнать больше, ознакомьтесь со статьями [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="8762a-110">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="8762a-111">Обзор проводника</span><span class="sxs-lookup"><span data-stu-id="8762a-111">Explorer overview</span></span>

<span data-ttu-id="8762a-112">В проводнике отображаются сведения об обнаруженных вредоносных программах и фишинге в Office 365, а также о других угрозах безопасности и рисках для Организации.</span><span class="sxs-lookup"><span data-stu-id="8762a-112">Explorer displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span> <span data-ttu-id="8762a-113">При первом открытии проводника представление по умолчанию показывает обнаружение вредоносных программ электронной почты за прошедшие 7 дней.</span><span class="sxs-lookup"><span data-stu-id="8762a-113">When you first open Explorer, the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="8762a-114">В проводнике также могут отображаться функции защиты системы безопасности в Office 365, в том числе [безопасные ссылки](atp-safe-links.md) и [безопасные вложения](atp-safe-attachments.md) , которые можно изменить для отображения данных за прошедшие 30 дней.</span><span class="sxs-lookup"><span data-stu-id="8762a-114">Explorer can also show security protection features in Office 365, including [Safe Links](atp-safe-links.md) and [Safe Attachments](atp-safe-attachments.md) and can be modified to show data for the past 30 days.</span></span> <span data-ttu-id="8762a-115">Если вы используете пробную версию субкриптион для Office 365 Advanced Threat protection (план 2) или Office 365 в ~, вы увидите только обнаружение и данные электронной почты за прошедшие 7 дней.</span><span class="sxs-lookup"><span data-stu-id="8762a-115">If you have a trial subcription for Office 365 Advanced Threat Protection Plan 2 or Office 365 E5, you will only see detections and email data for the past 7 days.</span></span>
  
![В проводнике отображаются сведения о самых частых вредоносных и целевых пользователях.](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
<span data-ttu-id="8762a-117">Используйте меню Вид для изменения отображаемых сведений.</span><span class="sxs-lookup"><span data-stu-id="8762a-117">Use the View menu to change what information is displayed.</span></span>
  
![Меню "вид" проводника](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
<span data-ttu-id="8762a-119">В проводнике есть несколько возможностей фильтрации и запросов, которые позволяют переходить к детальным сведениям, таким как самые популярные конечные пользователи, основные семейства вредоносных программ, технологию обнаружения и многое другое.</span><span class="sxs-lookup"><span data-stu-id="8762a-119">Explorer has several filtering and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="8762a-120">Каждый вид отчета предлагает различные способы просмотра и изучения данных.</span><span class="sxs-lookup"><span data-stu-id="8762a-120">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8762a-121">В проводнике не следует использовать подстановочные знаки, такие как звездочка (\*) или вопросительный знак (?).</span><span class="sxs-lookup"><span data-stu-id="8762a-121">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), with Explorer.</span></span> <span data-ttu-id="8762a-122">При поиске по полю Тема для сообщений электронной почты Explorer выполняет частичные совпадения и передает результаты, аналогичные условиям поиска с использованием подстановочных знаков.</span><span class="sxs-lookup"><span data-stu-id="8762a-122">When you search on the Subject field for email messages, Explorer will perform partial matching and yield results similar to a wildcard search.</span></span>

## <a name="email--malware"></a><span data-ttu-id="8762a-123">Вредоносные программы электронной почты \></span><span class="sxs-lookup"><span data-stu-id="8762a-123">Email \> Malware</span></span>

<span data-ttu-id="8762a-124">В этом представлении отображаются сообщения электронной почты, идентифицированные как содержащие вредоносные программы.</span><span class="sxs-lookup"><span data-stu-id="8762a-124">This view shows email messages identified as containing malware.</span></span>  

<span data-ttu-id="8762a-125">Просмотр сведений на диаграмме с помощью семейства вредоносных программ, домена отправителя, IP-адреса отправителя, состояния защиты (действия, предпринимаемые функциями и политиками защиты от угроз в Office 365) и технологией обнаружения (способ обнаружения вредоносных программ).</span><span class="sxs-lookup"><span data-stu-id="8762a-125">View information in the chart by malware family, sender domain, sender IP, protection status (actions taken by your threat protection features and policies in Office 365), and detection technology (how the malware was detected).</span></span>  

![Просмотр данных об обнаруженных вредоносных программах](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

<span data-ttu-id="8762a-127">Под диаграммой просмотрите сведения о самых популярных семействах вредоносных программ, основных целевых пользователях и более подробные сведения об определенных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="8762a-127">Below the chart, view details about top malware families, top targeted users, and more details about specific messages.</span></span> 

## <a name="email--phish"></a><span data-ttu-id="8762a-128">Фишинг \> электронной почты</span><span class="sxs-lookup"><span data-stu-id="8762a-128">Email \> Phish</span></span>

<span data-ttu-id="8762a-129">В этом представлении отображаются сообщения электронной почты, которые определены как попытки фишинга.</span><span class="sxs-lookup"><span data-stu-id="8762a-129">This view shows email messages identified as phishing attempts.</span></span>  

<span data-ttu-id="8762a-130">Просмотр сведений по домену отправителя, IP-АДРЕСу отправителя и защите (действия, предпринимаемые функциями и политиками защиты от угроз в Office 365).</span><span class="sxs-lookup"><span data-stu-id="8762a-130">View information by sender domain, sender IP, and protection status (actions taken by your threat protection features and policies in Office 365).</span></span> 

![Просмотр данных о почтовых сообщениях, определенных как попытки фишинга](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

<span data-ttu-id="8762a-132">Под диаграммой просмотрите дополнительные сведения о конкретных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="8762a-132">Below the chart, view more details about specific messages.</span></span> 

## <a name="email--user-reported"></a><span data-ttu-id="8762a-133">Сообщения \> электронной почты, о которых сообщил пользователь</span><span class="sxs-lookup"><span data-stu-id="8762a-133">Email \> User-reported</span></span>

<span data-ttu-id="8762a-134">В этом представлении отображаются сообщения электронной почты о том, что пользователи сообщили о нежелательной почте, нежелательной почте или фишинге.</span><span class="sxs-lookup"><span data-stu-id="8762a-134">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>  

<span data-ttu-id="8762a-135">Просмотр сведений по типу отчета (определение пользователя о том, что сообщение было нежелательным, не является нежелательным или фишингом) и по причине доставки (причины, по которым электронная почта появлялась в определенном месте, например в политике фильтрации нежелательной почты, правиле обработки почты, списке заблокированных отправителей, списке надежных отправителей) и т. д.).</span><span class="sxs-lookup"><span data-stu-id="8762a-135">View information by report type (the user's determination that the email was junk, not junk, or phish), and by delivery reason (reasons why email went to a specific location, such as a spam filter policy, a mail flow rule, a blocked-senders list, a safe-senders list, etc.).</span></span>  

![Просмотр данных о пользователях электронной почты, о которых сообщается как нежелательная почта, а не спам или фишинг](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

<span data-ttu-id="8762a-137">Под диаграммой просмотрите дополнительные сведения об определенных сообщениях электронной почты, таких как строка темы, IP-адрес отправителя, пользователь, который сообщил сообщение как нежелательное, нежелательное или фишинг, а также другие сведения.</span><span class="sxs-lookup"><span data-stu-id="8762a-137">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

## <a name="email--all-mail"></a><span data-ttu-id="8762a-138">Отправить \> сообщение по электронной почте</span><span class="sxs-lookup"><span data-stu-id="8762a-138">Email \> All mail</span></span>

<span data-ttu-id="8762a-139">В этом представлении отображается представление действий с электронной почтой, в том числе сообщение электронной почты, которое определено как вредоносное по причине фишинга или вредоносных программ, а также для всех невредоносных сообщений (обычной электронной почты, спама и массовой почты).</span><span class="sxs-lookup"><span data-stu-id="8762a-139">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="8762a-140">Если вы получаете сообщение об ошибке, которое считывает **слишком много данных**, добавьте фильтр и при необходимости Сократите диапазон дат, который вы просматриваете.</span><span class="sxs-lookup"><span data-stu-id="8762a-140">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="8762a-141">Чтобы применить фильтр, выберите **отправитель**, выберите элемент в списке, а затем нажмите кнопку Обновить.</span><span class="sxs-lookup"><span data-stu-id="8762a-141">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="8762a-142">В нашем примере мы использовали **технологию обнаружения** в качестве фильтра (доступно несколько вариантов).</span><span class="sxs-lookup"><span data-stu-id="8762a-142">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="8762a-143">Просмотр сведений по отправителям, доменам отправителя, получателям, темам, вложениям filename, семействам вредоносных программ, состоянию защиты (действия, выполняемые функциями и политиками защиты от угроз в Office 365), технология обнаружения (способ обнаружения вредоносных программ) и превышает.</span><span class="sxs-lookup"><span data-stu-id="8762a-143">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Просмотр данных об обнаруженных сообщениях электронной почты с помощью технологии обнаружения](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="8762a-145">Под диаграммой просмотрите дополнительные сведения об определенных сообщениях электронной почты, таких как строка темы, получатель, отправитель, состояние и т. д.</span><span class="sxs-lookup"><span data-stu-id="8762a-145">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="8762a-146">Вредоносные программы для контента \></span><span class="sxs-lookup"><span data-stu-id="8762a-146">Content \> Malware</span></span>

<span data-ttu-id="8762a-147">В этом представлении показаны файлы, которые были определены как вредоносные в Office 365 Advanced Threat Protection в SharePoint Online, OneDrive для бизнеса и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8762a-147">This view shows files that were identified as malicious by Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="8762a-148">Просмотр сведений о семействе вредоносных программ, технологии обнаружения (способе обнаружения вредоносных программ) и рабочей нагрузке (OneDrive, SharePoint или Teams).</span><span class="sxs-lookup"><span data-stu-id="8762a-148">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Просмотр данных об обнаруженных вредоносных программах](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="8762a-150">Под диаграммой просмотрите дополнительные сведения о конкретных файлах, таких как имя файла вложения, Рабочая нагрузка, размер файла, Последнее изменение файла и т. д.</span><span class="sxs-lookup"><span data-stu-id="8762a-150">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="new-click-to-filter-capabilities"></a><span data-ttu-id="8762a-151">(New!) Возможности "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="8762a-151">(New!) Click-to-filter capabilities</span></span>

<span data-ttu-id="8762a-152">Вы можете нажать кнопку "добавить в Проводник", чтобы выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="8762a-152">New to Explorer is the ability to click to filter.</span></span> <span data-ttu-id="8762a-153">При выборе элемента в условных обозначениях этот элемент становится фильтром для отчета.</span><span class="sxs-lookup"><span data-stu-id="8762a-153">When you click an item in the legend, that item becomes a filter for the report.</span></span> <span data-ttu-id="8762a-154">Например, предположим, что вы ищете представление вредоносных программ в проводнике:</span><span class="sxs-lookup"><span data-stu-id="8762a-154">For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Перейти к обозревателю \> управления угрозами](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="8762a-156">Выбор **ATP детонации** в этой диаграмме приводит к представлению следующего вида:</span><span class="sxs-lookup"><span data-stu-id="8762a-156">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorer фильтруется, чтобы отображались только результаты детонации для ATO](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="8762a-158">В этом представлении теперь вы ищете данные для файлов, которые были обезвреженои [безопасными вложенияМи Office 365 ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="8762a-158">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="8762a-159">Под диаграммой можно просмотреть подробные сведения об определенных сообщениях электронной почты, для которых были обнаружены вложения, обнаруженные безопасными вложениями ATP.</span><span class="sxs-lookup"><span data-stu-id="8762a-159">Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Конкретные сведения о сообщениях электронной почты с обнаруженными вложениями](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="8762a-161">При выборе одного или нескольких элементов активируется меню **действия** , в котором предлагается несколько вариантов выбора для выбранных элементов.</span><span class="sxs-lookup"><span data-stu-id="8762a-161">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![Выбор элемента активирует меню "действия"](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="8762a-163">Возможность фильтрации в нажатии и переходе к определенным сведениям может значительно сэкономить время при изучении угроз.</span><span class="sxs-lookup"><span data-stu-id="8762a-163">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>
  
## <a name="how-do-i-get-explorer"></a><span data-ttu-id="8762a-164">Как получить проводник?</span><span class="sxs-lookup"><span data-stu-id="8762a-164">How do I get Explorer?</span></span>

<span data-ttu-id="8762a-165">Explorer включен в [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span><span class="sxs-lookup"><span data-stu-id="8762a-165">Explorer is included in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span></span> 

<span data-ttu-id="8762a-166">Для просмотра и использования проводника необходимо иметь соответствующие разрешения, такие как предоставленные администратору безопасности или средству чтения безопасности.</span><span class="sxs-lookup"><span data-stu-id="8762a-166">You must have appropriate permissions, such as those granted to a security administrator or security reader, in order to view and use Explorer.</span></span> <span data-ttu-id="8762a-167">Чтобы узнать больше, ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8762a-167">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="8762a-168">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8762a-168">Related topics</span></span>

[<span data-ttu-id="8762a-169">Отчеты и аналитика в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="8762a-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="8762a-170">Поиск и исследование вредоносных сообщений электронной почты, которые были доставлены (Office 365 Threat Инвеситгатион и ответ)</span><span class="sxs-lookup"><span data-stu-id="8762a-170">Find and investigate malicious email that was delivered (Office 365 Threat Invesitgation and Response)</span></span>](investigate-malicious-email-that-was-delivered.md)
  
[<span data-ttu-id="8762a-171">Защита от нежелательной почты и вредоносных программ в Office 365</span><span class="sxs-lookup"><span data-stu-id="8762a-171">Anti-spam and anti-malware protection in Office 365</span></span>](anti-spam-and-anti-malware-protection.md)
  

