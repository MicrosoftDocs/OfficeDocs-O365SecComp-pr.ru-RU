---
title: Поддержка анонимных входящих сообщений электронной почты по протоколу IPv6
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/4/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
description: Exchange Online Protection (EOP) и Exchange Online поддерживает получение анонимных входящих сообщений электронной почты через IPv6 сообщения, которые не следует отправлять сообщения через безопасности TLS (Transport Layer). Вы можете явного согласия пользователя для получения сообщений по протоколу IPv6, направляемого UNRESOLVED_TOKEN_VAL(exMCSS) эту функцию, откройте Центр администрирования Office 365 в https://portal.office.com/adminportal/home, нажав кнопку поддержки и выбрав команду Создать запрос на обслуживание). Если вы не явного согласия пользователя для IPv6 будет продолжать получать сообщения через IPv4.
ms.openlocfilehash: a07e79732e9027d5848b787101be11066b5f0cb5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026296"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a>Поддержка анонимных входящих сообщений электронной почты по протоколу IPv6

Exchange Online Protection (EOP) и Exchange Online поддерживают получение анонимных входящих сообщений электронной почты по протоколу IPv6 от отправителей, которые не отправляют сообщения по протоколу TLS. Вы можете согласиться на получение сообщений по протоколу IPv6, запросив эти функции из UNRESOLVED_TOKEN_VAL(exMCSS) (для этого откройте Центр администрирования Office 365 по адресу [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), перейдите в раздел **Поддержка** и выберите **Создание запроса на обслуживание**). Если вы не согласитесь на использование протокола IPv6, вы по-прежнему будете получать сообщения по протоколу IPv4.
  
Отправители, передающие сообщения в службу по протоколу IPv6, должны выполнить два приведенных ниже требования.
  
1. У IPv6-адреса, с которого отправляются сообщения, должна быть допустимая запись PTR ([обратная запись DNS](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) IPv6-адреса, с которого отправляются сообщения). 
    
2. Отправитель должен пройти проверку инфраструктуры политики отправителей (определенную в документе [RFC 7208](https://tools.ietf.org/html/rfc7208)) или [проверку DKIM](http://dkim.org/) (которая описана в документе [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).
    
Перед переходом на IPv6 обязательно выполнить эти требования независимо от конфигурации. При выполнении обоих требований сообщение пройдет обычную фильтрацию электронных сообщений, которая предоставляется службой. Если какое-либо из этих требований не выполнено, сообщение будет отклонено с одним из следующих ответов 450:
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
Если вы не согласились на получение сообщений по протоколу IPv6, а отправитель пытается принудительно отправить сообщение по этому протоколу, вручную подключившись к почтовому серверу, то сообщение будет отклонено. При этом будет получен ответ 550, похожий на следующий:
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a>Дополнительные сведения

[Поддержка проверки сообщений, подписанных с помощью DKIM](support-for-validation-of-dkim-signed-messages.md)
  

