---
title: Поддержка анонимных входящих сообщений электронной почты по протоколу IPv6
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
description: Узнайте, как настроить поддержку анонимных сообщений из источников IPv6 для Exchange Online Protection и Exchange Online.
ms.openlocfilehash: 0d324ce6e0ff0ff9104ef597176b09a5a319abc7
ms.sourcegitcommit: 75b985b2574f4be70cf352498ea300b3d99dd338
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2018
ms.locfileid: "26255814"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a><span data-ttu-id="53d4f-103">Поддержка анонимных входящих сообщений электронной почты по протоколу IPv6</span><span class="sxs-lookup"><span data-stu-id="53d4f-103">Support for anonymous inbound email messages over IPv6</span></span>

<span data-ttu-id="53d4f-p101">Exchange Online Protection (EOP) и Exchange Online поддерживает получение анонимных входящих сообщений электронной почты через IPv6 сообщения, которые не следует отправлять сообщения через безопасности TLS (Transport Layer). Вы можете явного согласия пользователя для получения сообщений по протоколу IPv6, запрашивая этой функциональности от службы поддержки Майкрософт, откройте Центр администрирования Office 365 в [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), нажав кнопку **поддержки**и выбрав команду **Создать запрос на обслуживание**). Если вы не явного согласия пользователя для IPv6 будет продолжать получать сообщения через IPv4.</span><span class="sxs-lookup"><span data-stu-id="53d4f-p101">Exchange Online Protection (EOP) and Exchange Online support receiving anonymous inbound email messages over IPv6 communications from senders who don't send messages over Transport Layer Security (TLS). You can opt-in to receive messages over IPv6 by requesting this functionality from Microsoft Support by opening the Office 365 admin center at [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), clicking **Support**, and then clicking **New service request**). If you don't opt-in to IPv6 you'll continue to receive messages over IPv4.</span></span>
  
<span data-ttu-id="53d4f-107">Отправители, передающие сообщения в службу по протоколу IPv6, должны выполнить два приведенных ниже требования.</span><span class="sxs-lookup"><span data-stu-id="53d4f-107">Senders who transmit messages to the service over IPv6 must comply with the following two requirements:</span></span>
  
1. <span data-ttu-id="53d4f-108">У IPv6-адреса, с которого отправляются сообщения, должна быть допустимая запись PTR ([обратная запись DNS](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) IPv6-адреса, с которого отправляются сообщения).</span><span class="sxs-lookup"><span data-stu-id="53d4f-108">The sending IPv6 address must have a valid PTR record ([reverse DNS record](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) of the sending IPv6 address).</span></span> 
    
2. <span data-ttu-id="53d4f-109">Отправитель должен пройти проверку инфраструктуры политики отправителей (определенную в документе [RFC 7208](https://tools.ietf.org/html/rfc7208)) или [проверку DKIM](http://dkim.org/) (которая описана в документе [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span><span class="sxs-lookup"><span data-stu-id="53d4f-109">The sender must pass either SPF verification (defined in [RFC 7208](https://tools.ietf.org/html/rfc7208)) or [DKIM verification](http://dkim.org/) (defined in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span></span>
    
<span data-ttu-id="53d4f-p102">Перед переходом на IPv6 обязательно выполнить эти требования независимо от конфигурации. При выполнении обоих требований сообщение пройдет обычную фильтрацию электронных сообщений, которая предоставляется службой. Если какое-либо из этих требований не выполнено, сообщение будет отклонено с одним из следующих ответов 450:</span><span class="sxs-lookup"><span data-stu-id="53d4f-p102">Meeting these requirements is mandatory regardless of your configuration prior to opting-in to IPv6. If both requirements are met, the message will go through normal email message filtering provided by the service. If one or the other isn't met, the message will be rejected with one of the following 450 responses:</span></span>
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
<span data-ttu-id="53d4f-113">Если вы не согласились на получение сообщений по протоколу IPv6, а отправитель пытается принудительно отправить сообщение по этому протоколу, вручную подключившись к почтовому серверу, то сообщение будет отклонено. При этом будет получен ответ 550, похожий на следующий:</span><span class="sxs-lookup"><span data-stu-id="53d4f-113">If you aren't opted in to receive messages over IPv6 and the sender tries to force a message over IPv6 by manually connecting to the mail server, the message will be rejected with a 550 response that looks similar to the following:</span></span>
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a><span data-ttu-id="53d4f-114">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="53d4f-114">For more information</span></span>

[<span data-ttu-id="53d4f-115">Поддержка проверки сообщений, подписанных с помощью DKIM</span><span class="sxs-lookup"><span data-stu-id="53d4f-115">Support for validation of DKIM signed messages</span></span>](support-for-validation-of-dkim-signed-messages.md)
  

