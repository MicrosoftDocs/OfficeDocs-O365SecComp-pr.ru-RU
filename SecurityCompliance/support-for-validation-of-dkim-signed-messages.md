---
title: Поддержка проверки сообщений, подписанных с помощью DKIM
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
ms.collection:
- M365-security-compliance
description: Сведения о проверке подлинности подписанных сообщений DKIM в Exchange Online Protection и Exchange Online
ms.openlocfilehash: 75c104af4b3e6126bac37024de2c7f6ab337a028
ms.sourcegitcommit: 1947ad3c0dde9163ba9b6834d8b38bd04b4264a5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2019
ms.locfileid: "36643271"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>Поддержка проверки сообщений, подписанных с помощью DKIM

Exchange Online Protection (EOP) и Exchange Online поддерживают входящую проверку входящих сообщений электронной почты ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)) в ключах домена. DKIM позволяет проверить, отправлено ли сообщение из заявленного домена и не подделали ли его. Сообщение электронной почты связывается с организацией, ответственной за его отправку. Проверка DKIM используется автоматически для всех сообщений, отправленных через подключения по протоколу IPv6. Кроме того, Office 365 поддерживает DKIM при отправке почты по протоколу IPv4. (Дополнительные сведения о поддержке протокола IPv6 см. в разделе [Поддержка анонимных входящих сообщений электронной почты по протоколу IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)
  
DKIM проверяет сообщение с цифровой подписью, которое отображается в заголовке DKIM-Signature в заголовках сообщения. Результаты проверки заголовка DKIM-Signature помечаются в заголовке Authentication-Results, который соответствует спецификации RFC 7001 ([Поле заголовка сообщения для указания состояния проверки подлинности сообщения](https://www.rfc-editor.org/rfc/rfc7001.txt)). Текст заголовка сообщения имеет указанные ниже формат (где contoso.com  отправитель).
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
Администраторы могут создавать [правила](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) для почтовых ящиков Exchange (которые также называются правилами транспорта) на результаты проверки DKIM для фильтрации и маршрутизации сообщений по мере необходимости. 
  

