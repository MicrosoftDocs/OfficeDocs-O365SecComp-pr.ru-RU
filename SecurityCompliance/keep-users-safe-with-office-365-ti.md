---
title: Обеспечение безопасности пользователей Office 365 с помощью Office 365 Threat Intelligence
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
ms.assetid: 3387bfc3-028a-42f4-8133-4cbecfaab812
ms.collection: M365-security-compliance
description: Узнайте, как анализ угроз Office 365 может помочь вашей организации обнаружение вторжений и угроз и быстро устранять и восстановиться угрозы.
ms.openlocfilehash: c049e6f811eec8a30eb2b94361f8cdcbdaa8ac49
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995370"
---
# <a name="keep-your-office-365-users-safe-with-office-365-threat-intelligence"></a><span data-ttu-id="2f9cf-103">Обеспечение безопасности пользователей Office 365 с помощью Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="2f9cf-103">Keep your Office 365 users safe with Office 365 Threat Intelligence</span></span>

## <a name="overview"></a><span data-ttu-id="2f9cf-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="2f9cf-104">Overview</span></span>

<span data-ttu-id="2f9cf-p101">Узнать, какой из пользователей Office 365 находятся под атаки или более - атаке? Знать, как устранять от и атак, которые нацелены пользователей? Вы знаете, что для этого точно с возможностями безопасности, которые уже доступны в Office 365?</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p101">Do you know which of your Office 365 users are under attack, or worse - compromised? Do know how to mitigate and recover from attacks that are targeting your users? Did you know you can do exactly this with security capabilities that are already available to you in Office 365?</span></span> 
  
<span data-ttu-id="2f9cf-p102">[Анализ угроз Office 365](office-365-ti.md) — это набор возможностей, включенных в Office 365 E5 подписки. Office 365 анализ угроз был призван ИТ-отдела Майкрософт сократить среднее время разрешение для социальная инженерия происшествия, 80% и увеличения пропускной способности делами, 37% в месяц, по сравнению с предыдущей 2 квартала!</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p102">[Office 365 Threat Intelligence](office-365-ti.md) is a suite of capabilities included in your Office 365 E5 subscription. Office 365 Threat Intelligence has helped Microsoft IT reduce average time to resolution for social engineering incidents by 80%, and increased case throughput by 37% per month compared to the previous 2 quarters!</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="2f9cf-p103">Приступая к работе в 2019 февраля и развертывания в течение следующего несколько месяцев, анализ угроз Office 365 становится все Office 365 расширенного угроз защиты план 2, с помощью возможностей защиты дополнительных угроз. Для получения дополнительных сведений см [защиту от угроз для Office 365 Дополнительные планы и ценах](https://products.office.com/exchange/advance-threat-protection) и [Office 365 расширенного угроз защиты описание службы](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
<span data-ttu-id="2f9cf-p104">Недавно мы добавили новые возможности для улучшения обнаружения и восстановления из угрозы, связанные с! Ниже приведен краткий подробное описание из как обновленную анализ угроз можно усовершенствовать еще более эффективным.</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p104">We've recently added new capabilities to help improve how you can detect and recover from threats! Here's a quick walk through of how the updated Threat Intelligence service can make you even more efficient.</span></span>
  
## <a name="detect-intrusions-and-threats"></a><span data-ttu-id="2f9cf-114">Обнаружение вторжений и угроз</span><span class="sxs-lookup"><span data-stu-id="2f9cf-114">Detect intrusions and threats</span></span>

<span data-ttu-id="2f9cf-p105">[Обозреватель](use-explorer-in-security-and-compliance.md) (также называется Explorer угроз) помогает аналитикам определить и понять угроз, активных на предприятии, так как даже самые сложные параметры безопасности можно обойти, внешне безвредным пользовательских конфигураций как безопасный и безопасности "Администраторы" whitelists отправителя. Explorer приводятся рекомендации по Office 365 глобального или безопасности "Администраторы" быстро определить нарушается ли пользователи с угроз, таких как ловят или вредоносных программ. Это позволяет определять приоритеты которого пользователи наиболее находятся под угрозой угрозы и надлежащие ответа.</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p105">[Explorer](use-explorer-in-security-and-compliance.md) (also referred to as Threat Explorer) helps security admins and analysts identify and understand threats that are active in your enterprise because even the most complex security settings can be circumvented by seemingly innocuous user configurations like safe sender whitelists. Explorer helps Office 365 global or security admins quickly determine whether users have been compromised by threats such as malware or phish. This helps prioritize which users are most at risk for a threat and the requisite response.</span></span> 
  
<span data-ttu-id="2f9cf-p106">Обозреватель также помогает администраторам перехода по связям между пользователями и почты. Проверить, что определенный почты, который был поврежден? Поиск, чтобы увидеть, какие пользователи получили сообщение, выполните последовательность событий и видеть то этих пользователей в свою очередь, было выполнено.</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p106">Explorer also helps admins navigate the relationships between users and mail. Know of a particular mail that was bad? Search for it to see what users received the mail, then follow the series of events and see what those users in turn have done.</span></span>

<span data-ttu-id="2f9cf-p107">Если у вас еще нет анализ угроз, [Попробуйте прямо сейчас](https://aka.ms/tryo365threatintel3)! И [больше узнать о анализ угроз Office 365](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p107">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![Снимок экрана обозревателя угроз в Office 365, цветной закодированные семейства вредоносных программ](media/591338dd-252a-437d-b5f2-87aa42e74b0c.png)
  
## <a name="quickly-mitigate-and-recover-from-threats"></a><span data-ttu-id="2f9cf-124">Быстро устранять и восстановиться угрозы, связанные с</span><span class="sxs-lookup"><span data-stu-id="2f9cf-124">Quickly mitigate and recover from threats</span></span>

<span data-ttu-id="2f9cf-p108">После определения безопасности "Администраторы" что-то подозрительные или вредоносных сведений о событиях в своих клиентов, они могут быстро содержат и реагировать на этой угрозы с помощью **Framework происшествия**. Группировка нежелательных сообщений с одним щелчком мыши и быстро удаления сообщений электронной почты из почтовых ящиков на пользователей.</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p108">Once security admins have identified something suspicious or malicious happening in their tenant, they can quickly contain and respond to that threat with the **Incident Framework**. Group unwanted messages with one-click and quickly remove the email messages from your user's mailboxes.</span></span> 
  
 <span data-ttu-id="2f9cf-p109">**Обновления:** Недавно была добавлена возможность удаления (delete программных или жестко) по электронной почте непосредственно из Framework происшествия. Ранее Администраторы только переместить сообщения в папку нежелательной пользователя, где пользователи могут восстановить элемент. Новые возможности удалить позволяют убедиться, что вредоносных или нежелательных почтовых удаляется без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p109">**UPDATE:** We've recently added the ability to delete (soft or hard delete) emails directly from the Incident Framework. Previously administrators could only move mails to a user's junk folder, where users could recover the item. With the newly released Delete capabilities, you can now be sure that a malicious or unwanted mail is removed permanently.</span></span> 
  
<span data-ttu-id="2f9cf-p110">Если у вас еще нет анализ угроз, [Попробуйте прямо сейчас](https://aka.ms/tryo365threatintel3)! И [больше узнать о анализ угроз Office 365](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p110">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![Снимок экрана список инцидентов обновлений по электронной почте](media/9d8452d3-d8d2-4b26-81f9-76396e08dd17.png)
  
## <a name="leverage-the-threat-telemetry-of-microsoft"></a><span data-ttu-id="2f9cf-133">Использовать телеметрии threat корпорации Майкрософт</span><span class="sxs-lookup"><span data-stu-id="2f9cf-133">Leverage the threat telemetry of Microsoft</span></span>

<span data-ttu-id="2f9cf-p111">Анализ угроз Office 365 выключен с данными из Intelligent Microsoft Graph безопасности. Графическое представление получает последние сигнал threat более 1 миллиард устройства Windows, 450 миллиардов ежемесячный Azure имена входа и 400 миллиардов ежемесячный сообщений электронной почты в Office 365. Этот сигнал непревзойденной угроз является то, что предоставляет широкие видения клиента клиента, который является важным условием для администраторов и безопасности аналитикам иметь получить полное представление об угрозах, влияющее своей организации.</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p111">Office 365 Threat Intelligence is powered with data from the Microsoft Intelligent Security Graph. The graph acquires the latest threat signal from over 1 billion Windows devices, 450 billion monthly Azure logins, and 400 billion monthly email messages in Office 365. This unrivaled threat signal is what gives the broad visibility into a customer tenant that is crucial for admins and security analysts to have a complete view of the threats impacting their organization.</span></span> 
  
## <a name="more-to-come"></a><span data-ttu-id="2f9cf-137">Дополнительные статьи</span><span class="sxs-lookup"><span data-stu-id="2f9cf-137">More to come</span></span>

<span data-ttu-id="2f9cf-p112">Это лишь некоторые примеры того, как анализ угроз Office 365 помогает защитить предприятия! В течение нескольких недель мы добавляем широкие возможности продукта, включая:</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p112">These are just some examples of how Office 365 Threat Intelligence helps you secure your enterprise! In the coming weeks we are adding significant enhancements to the product including:</span></span>
  
- <span data-ttu-id="2f9cf-140">Предоставление понять потенциально опасным действий, выполняемых с электронной почты Exchange Online и SharePoint Online документов</span><span class="sxs-lookup"><span data-stu-id="2f9cf-140">Providing insight into potentially risky actions taken on Exchange Online email and SharePoint Online documents</span></span>
    
- <span data-ttu-id="2f9cf-141">Предоставляет подробные сведения о нежелательном фишинга сообщений электронной почты, отправленных пользователями, включая некоторые, для которого может были получены и прочитаны пользователями, прежде чем они были weaponized</span><span class="sxs-lookup"><span data-stu-id="2f9cf-141">Providing insight into malicious phishing email messages that have been sent to users, including some that have may have been received and read by users before they were weaponized</span></span>
    
- <span data-ttu-id="2f9cf-142">Увеличение набор действия администраторов может занять угрозы</span><span class="sxs-lookup"><span data-stu-id="2f9cf-142">Increasing the set of actions admins can take to respond to incidents</span></span>
    
## <a name="why-threat-intelligence"></a><span data-ttu-id="2f9cf-143">Почему угроз аналитики?</span><span class="sxs-lookup"><span data-stu-id="2f9cf-143">Why Threat Intelligence?</span></span>

<span data-ttu-id="2f9cf-p113">Gartner оценки, что сам по себе он через $90B 2017 было затрачено на cybersecurity. ИД безопасности Deshpande, аналитика участника исследования компании Gartner, находится в кавычках как о том, что «shift в отрасли для обнаружения и ответа... отправляет очистить сообщение предотвращения бесполезно, если он связан в функцию обнаружения и ответ.» Анализ угроз является важной частью портфеля каждое предприятие служб и может быть использован как автономную службу или в составе Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="2f9cf-p113">Gartner estimates that in 2017 alone over $90B was spent on cybersecurity. Sid Deshpande, principal research analyst at Gartner, is quoted as saying that "the industry's shift to detection and response … sends a clear message that prevention is futile unless it is tied into a detection and response capability." Threat Intelligence is a critical part of every enterprise's portfolio of services, and can be consumed as standalone service or as part of Office 365 E5.</span></span>
  
## <a name="whats-next"></a><span data-ttu-id="2f9cf-148">Что дальше</span><span class="sxs-lookup"><span data-stu-id="2f9cf-148">What's Next</span></span>

- <span data-ttu-id="2f9cf-149">Дополнительные сведения о анализ угроз Office 365 в данном сеансе записанных: [Всегда оставаться издержек из Cyberattacks с анализ угроз Office 365](https://myignite.microsoft.com/videos/53723)</span><span class="sxs-lookup"><span data-stu-id="2f9cf-149">Learn more about Office 365 Threat Intelligence in this recorded session: [Stay Ahead of the Cyberattacks with Office 365 Threat Intelligence](https://myignite.microsoft.com/videos/53723)</span></span>
    
- <span data-ttu-id="2f9cf-150">[Испытайте анализ угроз 365 Office теперь](https://aka.ms/tryo365threatintel3) или начать пробную версию Office E5 сегодня!</span><span class="sxs-lookup"><span data-stu-id="2f9cf-150">[Try out Office 365 Threat Intelligence now](https://aka.ms/tryo365threatintel3) or begin your Office E5 trial today!</span></span> 
    

