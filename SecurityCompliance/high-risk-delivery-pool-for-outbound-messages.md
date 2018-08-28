---
title: Пул доставки сообщений с высоким уровнем опасности
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/24/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: ac11edd9-2da3-462d-8ea3-bbf9dbc6f948
description: Если почтовая система клиента скомпрометирована вредоносной программой или спам-атакой и отправляет спам через размещенную службу фильтрации, IP-адреса серверов центра данных Office 365 могут быть занесены в сторонние списки блокировок.
ms.openlocfilehash: 856db53b105379ea3e606e39bf3c2612afa803c3
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026626"
---
# <a name="high-risk-delivery-pool-for-outbound-messages"></a><span data-ttu-id="bcc57-103">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="bcc57-103">High-risk delivery pool for outbound messages</span></span>

<span data-ttu-id="bcc57-p101">Если почтовая система клиента скомпрометирована вредоносной программой или спам-атакой и отправляет спам через размещенную службу фильтрации, IP-адреса серверов центра данных Office 365 могут быть занесены в сторонние списки блокировок. Конечные серверы, которые не используют размещенную службу фильтрации, но используют эти списки блокировок, будут отклонять всю почту, отправляемую с IP-адресов, добавленных в эти списки. Чтобы этого избежать, все исходящие сообщения, которые превышают порог спама, отправляются через пул доставки сообщений с высоким уровнем опасности. Этот дополнительный пул исходящей почты используется для отправки сообщений низкого качества. Это позволяет защитить остальную сеть от отправки сообщений, которые могут привести к блокировке IP-адреса отправки.</span><span class="sxs-lookup"><span data-stu-id="bcc57-p101">When a customer's email system has been compromised by malware or a malicious spam attack, and it's sending outbound spam through the hosted filtering service, this can result in the IP addresses of the Office 365 data center servers being listed on third-party block lists. Destination servers that do not use the hosted filtering service, but do use these block lists, reject all email sent from any of the hosted filtering IP addresses that have been added to those lists. To prevent this, all outbound messages that exceed the spam threshold are sent through a high-risk delivery pool. This secondary outbound email pool is only used to send messages that may be of low quality. This helps to protect the rest of the network from sending messages that are more likely to result in the sending IP address being blocked.</span></span>
  
<span data-ttu-id="bcc57-p102">Мы используем специальный пул доставки сообщений с высоким уровнем опасности, чтобы с нормального пула исходящей почты отправлялись только сообщения высокого качества. Этот дополнительный пул IP-адресов позволяет снизить вероятность добавления нормального пула исходящих IP-адресов в список блокировок. Пул доставки сообщений с высоким уровнем опасности по-прежнему может быть занесен в список блокировок.</span><span class="sxs-lookup"><span data-stu-id="bcc57-p102">The use of a dedicated high-risk delivery pool helps ensure that the normal outbound pool is only sending messages that are known to be of a high-quality. Using this secondary IP pool helps to reduce the probability of the normal outbound-IP pool being added to a blocked list. The possibility of the high-risk delivery pool being placed on a blocked list remains a risk. This is by design.</span></span>
  
<span data-ttu-id="bcc57-113">Сообщения без адресной записи (записи A), которая содержит IP-адрес домена, и записи MX, которая направляет почту на серверы, отвечающие домену в DNS, всегда направляются через пул доставки сообщений с высоким уровнем опасности независимо от вероятности спама.</span><span class="sxs-lookup"><span data-stu-id="bcc57-113">Messages where the sending domain has no address record (A record), which gives you the IP address of the domain, and no MX record, which helps direct mail to the servers that should receive the mail for a particular domain in the DNS, are always routed through the high-risk delivery pool regardless of their spam disposition.</span></span>
  
## <a name="understanding-delivery-status-notification-dsn-messages"></a><span data-ttu-id="bcc57-114">Уведомления о доставке</span><span class="sxs-lookup"><span data-stu-id="bcc57-114">Understanding Delivery Status Notification (DSN) messages</span></span>

<span data-ttu-id="bcc57-115">Пул доставки сообщений с высоким уровнем опасности управляет доставкой всех сообщений о недоставке.</span><span class="sxs-lookup"><span data-stu-id="bcc57-115">The outbound high-risk delivery pool manages the delivery for all "bounced" or "failed" (DSN) messages.</span></span>
  
<span data-ttu-id="bcc57-116">Ниже приведены возможные причины повышения количества сообщений DSN.</span><span class="sxs-lookup"><span data-stu-id="bcc57-116">Possible causes for a surge in DSN messages include the following:</span></span>
  
- <span data-ttu-id="bcc57-117">Спуфинг-атака, влияющая на одного из клиентов, использующих службу.</span><span class="sxs-lookup"><span data-stu-id="bcc57-117">A spoofing campaign affecting one of the customers using the service</span></span>
    
- <span data-ttu-id="bcc57-118">Атака с целью сбора действующих адресов</span><span class="sxs-lookup"><span data-stu-id="bcc57-118">A directory harvest attack</span></span>
    
- <span data-ttu-id="bcc57-119">Атака с использованием нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="bcc57-119">A spam attack</span></span>
    
- <span data-ttu-id="bcc57-120">Неавторизованный сервер SMTP</span><span class="sxs-lookup"><span data-stu-id="bcc57-120">A rogue SMTP server</span></span>
    
<span data-ttu-id="bcc57-p103">В результате всех этих проблем количество обрабатываемых службой сообщений о недоставке может резко увеличиться. Часто другие почтовых серверы и службы считают эти сообщения спамом.</span><span class="sxs-lookup"><span data-stu-id="bcc57-p103">All of these issues can result in a sudden increase in the number of DSN messages being processed by the service. Many times, these DSN messages appear to be spam to other email servers and services.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="bcc57-123">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="bcc57-123">For more information</span></span>

[<span data-ttu-id="bcc57-124">Настройка правил защиты от спама для исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="bcc57-124">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="bcc57-125">Защита от нежелательной почты вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="bcc57-125">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  
