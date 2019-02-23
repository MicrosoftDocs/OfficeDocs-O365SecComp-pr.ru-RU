---
title: Обеспечение безопасности пользователей Office 365 с помощью Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3387bfc3-028a-42f4-8133-4cbecfaab812
ms.collection: M365-security-compliance
description: Узнайте, как Office 365 Threat Intelligence помогает вашей организации обнаруживать проникновения и угрозы, а также быстро устранять угрозы и восстанавливать их.
ms.openlocfilehash: c2c601c7828e947c6cfa1c91723a19acee9e09ee
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213699"
---
# <a name="keep-your-office-365-users-safe-with-office-365-threat-intelligence"></a><span data-ttu-id="763dd-103">Обеспечение безопасности пользователей Office 365 с помощью Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="763dd-103">Keep your Office 365 users safe with Office 365 Threat Intelligence</span></span>

## <a name="overview"></a><span data-ttu-id="763dd-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="763dd-104">Overview</span></span>

<span data-ttu-id="763dd-p101">Знаете ли вы, какие пользователи Office 365 подвержены атакам или хуже их безопасности? Знаете, как устранять и устранять атаки, предназначенные для пользователей? Знаете ли вы, что именно это можно сделать с возможностями безопасности, которые уже доступны в Office 365?</span><span class="sxs-lookup"><span data-stu-id="763dd-p101">Do you know which of your Office 365 users are under attack, or worse - compromised? Do know how to mitigate and recover from attacks that are targeting your users? Did you know you can do exactly this with security capabilities that are already available to you in Office 365?</span></span> 
  
<span data-ttu-id="763dd-p102">[Office 365 Threat Intelligence](office-365-ti.md) — это набор возможностей, включенных в вашу подПиску на Office 365. Служба анализа угроз Office 365 помогает ИТ-отделу сократить среднее время на решение проблем с социальным проектированием на 80%, а повышенную пропускную способность — 37% в месяц по сравнению с предыдущими 2 кварталами.</span><span class="sxs-lookup"><span data-stu-id="763dd-p102">[Office 365 Threat Intelligence](office-365-ti.md) is a suite of capabilities included in your Office 365 E5 subscription. Office 365 Threat Intelligence has helped Microsoft IT reduce average time to resolution for social engineering incidents by 80%, and increased case throughput by 37% per month compared to the previous 2 quarters!</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="763dd-p103">Начиная с 2019 февраля и заканчивая на ближайшие несколько месяцев, управление угрозами безопасности Office 365 становится Office 365 Advanced Threat Protection Plan 2 с дополнительными возможностями защиты от угроз. Чтобы узнать больше, ознакомьтесь со статьями [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="763dd-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
<span data-ttu-id="763dd-p104">Мы недавно добавили новые возможности для улучшения возможности обнаружения и восстановления угроз. Вот краткий обзор того, как обновленная служба системы защиты от угроз может сделать еще эффективнее.</span><span class="sxs-lookup"><span data-stu-id="763dd-p104">We've recently added new capabilities to help improve how you can detect and recover from threats! Here's a quick walk through of how the updated Threat Intelligence service can make you even more efficient.</span></span>
  
## <a name="detect-intrusions-and-threats"></a><span data-ttu-id="763dd-114">Обнаружение вторжений и угроз</span><span class="sxs-lookup"><span data-stu-id="763dd-114">Detect intrusions and threats</span></span>

<span data-ttu-id="763dd-p105">[Explorer](use-explorer-in-security-and-compliance.md) (также называемое обозревателем угроз) помогает администраторам и аналитикам определить и понять угрозы, активные в Организации, так как даже самые сложные параметры безопасности можно обойти, наподобие небезопасных пользовательских конфигураций, таких как Safe Отправитель вхителистс. С помощью проводника пользователи Office 365 Global or Security Admins быстро определяют, были ли пользователи скомпрометированы угрозами, такими как вредоносные программы и фишинг. Это помогает определить, какие пользователи наиболее подвержены риску для угроз и отклика.</span><span class="sxs-lookup"><span data-stu-id="763dd-p105">[Explorer](use-explorer-in-security-and-compliance.md) (also referred to as Threat Explorer) helps security admins and analysts identify and understand threats that are active in your enterprise because even the most complex security settings can be circumvented by seemingly innocuous user configurations like safe sender whitelists. Explorer helps Office 365 global or security admins quickly determine whether users have been compromised by threats such as malware or phish. This helps prioritize which users are most at risk for a threat and the requisite response.</span></span> 
  
<span data-ttu-id="763dd-p106">Кроме того, проводник позволяет администраторам перемещаться по связям между пользователями и почтой. Знаете ли вы какую бы то ни было неисправное сообщение? Найдите его, чтобы узнать, какие пользователи получали почту, а затем выполните ряд событий и посмотрите, что именно эти пользователи сделали.</span><span class="sxs-lookup"><span data-stu-id="763dd-p106">Explorer also helps admins navigate the relationships between users and mail. Know of a particular mail that was bad? Search for it to see what users received the mail, then follow the series of events and see what those users in turn have done.</span></span>

<span data-ttu-id="763dd-p107">Если у вас еще нет логики защиты от угроз, [попробуйте сейчас](https://aka.ms/tryo365threatintel3). И [Узнайте больше о Microsoft Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="763dd-p107">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![Снимок экрана: обозреватель угроз в Office 365, цветовая кодировка для семейства вредоносных программ](media/591338dd-252a-437d-b5f2-87aa42e74b0c.png)
  
## <a name="quickly-mitigate-and-recover-from-threats"></a><span data-ttu-id="763dd-124">Быстрое устранение угроз и восстановление от угроз</span><span class="sxs-lookup"><span data-stu-id="763dd-124">Quickly mitigate and recover from threats</span></span>

<span data-ttu-id="763dd-p108">После того как администраторы безопасности выявили подозрительные или вредоносные события, происходящие в своем клиенте, они могут быстро содержать эту угрозу и реагировать на нее с помощью **платформы инцидентов**. Группирование нежелательных сообщений одним щелчком мыши и быстрое удаление сообщений электронной почты из почтовых ящиков пользователя.</span><span class="sxs-lookup"><span data-stu-id="763dd-p108">Once security admins have identified something suspicious or malicious happening in their tenant, they can quickly contain and respond to that threat with the **Incident Framework**. Group unwanted messages with one-click and quickly remove the email messages from your user's mailboxes.</span></span> 
  
 <span data-ttu-id="763dd-p109">**Обновление:** Недавно мы добавили возможность удалять сообщения электронной почты (мягкое или жесткое удаление) непосредственно из платформы инцидентов. Ранее администраторы могли только перемещать сообщения в папку нежелательной почты пользователя, где пользователи могут восстановить элемент. После выпуска новых возможностей удаления вы можете убедиться, что вредоносная или Нежелательная почта удаляется без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="763dd-p109">**UPDATE:** We've recently added the ability to delete (soft or hard delete) emails directly from the Incident Framework. Previously administrators could only move mails to a user's junk folder, where users could recover the item. With the newly released Delete capabilities, you can now be sure that a malicious or unwanted mail is removed permanently.</span></span> 
  
<span data-ttu-id="763dd-p110">Если у вас еще нет логики защиты от угроз, [попробуйте сейчас](https://aka.ms/tryo365threatintel3). И [Узнайте больше о Microsoft Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span><span class="sxs-lookup"><span data-stu-id="763dd-p110">If you don't already have Threat Intelligence, [try it now](https://aka.ms/tryo365threatintel3)! And [learn more about Office 365 Threat Intelligence](https://aka.ms/readmoreabouto365threatintel).</span></span>
  
![Снимок экрана с перечнем сообщений электронной почты об исправлении инцидентов](media/9d8452d3-d8d2-4b26-81f9-76396e08dd17.png)
  
## <a name="leverage-the-threat-telemetry-of-microsoft"></a><span data-ttu-id="763dd-133">Использование дистанционного отслеживания угроз для Майкрософт</span><span class="sxs-lookup"><span data-stu-id="763dd-133">Leverage the threat telemetry of Microsoft</span></span>

<span data-ttu-id="763dd-p111">Система анализа угроз Office 365 работает с данными из графа интеллектуальной безопасности Майкрософт. Граф получает последний сигнал угрозы из более чем 1 000 000 000 устройств с Windows, 450 000 000 000 ежемесячных учетных записей Azure и 400 000 000 000 ежемесячных сообщений в Office 365. Этот незавершенный сигнал угрозы — это то, что дает возможность широкому просмотру клиентского клиента, который имеет решающее значение для администраторов и аналитик безопасности, для получения полного представления угроз, влияющих на их организацию.</span><span class="sxs-lookup"><span data-stu-id="763dd-p111">Office 365 Threat Intelligence is powered with data from the Microsoft Intelligent Security Graph. The graph acquires the latest threat signal from over 1 billion Windows devices, 450 billion monthly Azure logins, and 400 billion monthly email messages in Office 365. This unrivaled threat signal is what gives the broad visibility into a customer tenant that is crucial for admins and security analysts to have a complete view of the threats impacting their organization.</span></span> 
  
## <a name="more-to-come"></a><span data-ttu-id="763dd-137">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="763dd-137">More to come</span></span>

<span data-ttu-id="763dd-p112">Вот лишь некоторые примеры того, как Microsoft Office 365 Threat Intelligence помогает защитить корпоративный сервер. В ближайшие недели мы добавим существенные дополнения к продукту, в том числе:</span><span class="sxs-lookup"><span data-stu-id="763dd-p112">These are just some examples of how Office 365 Threat Intelligence helps you secure your enterprise! In the coming weeks we are adding significant enhancements to the product including:</span></span>
  
- <span data-ttu-id="763dd-140">Предоставление сведений о потенциально опасном действиях, выполняемых в электронной почте Exchange Online и документах SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="763dd-140">Providing insight into potentially risky actions taken on Exchange Online email and SharePoint Online documents</span></span>
    
- <span data-ttu-id="763dd-141">Предоставление сведений о вредоносных мошеннических сообщениях электронной почты, которые были отправлены пользователям, в том числе некоторые, которые могут быть получены и прочитаны пользователями до их веапонизед</span><span class="sxs-lookup"><span data-stu-id="763dd-141">Providing insight into malicious phishing email messages that have been sent to users, including some that have may have been received and read by users before they were weaponized</span></span>
    
- <span data-ttu-id="763dd-142">Увеличение набора действий, которые администраторы могут предпринять для реагирования на инциденты</span><span class="sxs-lookup"><span data-stu-id="763dd-142">Increasing the set of actions admins can take to respond to incidents</span></span>
    
## <a name="why-threat-intelligence"></a><span data-ttu-id="763dd-143">Зачем нужна логика операций с угрозами?</span><span class="sxs-lookup"><span data-stu-id="763dd-143">Why Threat Intelligence?</span></span>

<span data-ttu-id="763dd-p113">Оценки Gartner, которые проходили в 2017 отдельно от $90B, были потрачены на циберсекурити. SID Дешпанде, основной исследовательской аналитики в компании Gartner, заключен в кавычки, так как это говорит о том, что в отрасли выбрана функция обнаружения и ответа в отрасли... отправляет неясное сообщение о том, что функция предотвращения футиле, если она не связана с возможностью обнаружения и ответа. " Логика операций с угрозами является важной частью каждого портфеля служб предприятия и может использоваться как отдельная служба или как часть Office 365 в ~.</span><span class="sxs-lookup"><span data-stu-id="763dd-p113">Gartner estimates that in 2017 alone over $90B was spent on cybersecurity. Sid Deshpande, principal research analyst at Gartner, is quoted as saying that "the industry's shift to detection and response … sends a clear message that prevention is futile unless it is tied into a detection and response capability." Threat Intelligence is a critical part of every enterprise's portfolio of services, and can be consumed as standalone service or as part of Office 365 E5.</span></span>
  
## <a name="whats-next"></a><span data-ttu-id="763dd-148">Что дальше</span><span class="sxs-lookup"><span data-stu-id="763dd-148">What's Next</span></span>

- <span data-ttu-id="763dd-149">Дополнительные сведения о Microsoft Office 365 Threat Intelligence в этом записанном сеансе: [Будьте в курсе событий кибератаки with office 365 Threat Intelligence](https://myignite.microsoft.com/videos/53723)</span><span class="sxs-lookup"><span data-stu-id="763dd-149">Learn more about Office 365 Threat Intelligence in this recorded session: [Stay Ahead of the Cyberattacks with Office 365 Threat Intelligence](https://myignite.microsoft.com/videos/53723)</span></span>
    
- <span data-ttu-id="763dd-150">Ознакомьтесь с ознакомительной версией [office 365 Threat Intelligence](https://aka.ms/tryo365threatintel3) или начните ее сегодня!</span><span class="sxs-lookup"><span data-stu-id="763dd-150">[Try out Office 365 Threat Intelligence now](https://aka.ms/tryo365threatintel3) or begin your Office E5 trial today!</span></span> 
    

