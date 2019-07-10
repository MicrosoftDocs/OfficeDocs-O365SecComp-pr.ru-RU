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
ms.openlocfilehash: 88a01944dd215ff3b6f22a266a12145927f89e0a
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600712"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>Поддержка проверки сообщений, подписанных с помощью DKIM

Службы Exchange Online Protection (EOP) и Exchange Online поддерживают проверку входящей почты сообщений, подписанных с помощью Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)). DKIM позволяет проверить, отправлено ли сообщение из заявленного домена и не подделали ли его. Сообщение электронной почты связывается с организацией, ответственной за его отправку. Проверка DKIM используется автоматически для всех сообщений, отправленных через подключения по протоколу IPv6. (Дополнительные сведения о поддержке IPv6 см. в разделе [Поддержка анонимных входящих сообщений электронной почты по протоколу IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)
  
DKIM проверяет сообщение с цифровой подписью, которое отображается в заголовке DKIM-Signature в заголовках сообщения. Результаты проверки заголовка DKIM-Signature помечаются в заголовке Authentication-Results, который соответствует спецификации RFC 7001 ([Поле заголовка сообщения для указания состояния проверки подлинности сообщения](https://www.rfc-editor.org/rfc/rfc7001.txt)). Текст заголовка сообщения имеет указанные ниже формат (где contoso.com  отправитель).
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
Администраторы могут создавать [правила](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) для почтовых ящиков Exchange (которые также называются правилами транспорта) на результаты проверки DKIM для фильтрации и маршрутизации сообщений по мере необходимости. 
  

