---
title: Поддержка проверки сообщений, подписанных с помощью DKIM
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
description: Службы Exchange Online Protection (EOP) и Exchange Online поддерживают проверку входящей почты сообщений, подписанных с помощью Domain Keys Identified Mail (DKIM). DKIM позволяет проверить, отправлено ли сообщение из заявленного домена и не подделали ли его. Сообщение электронной почты связывается с организацией, ответственной за его отправку. Проверка DKIM используется автоматически для всех сообщений, отправленных через подключения по протоколу IPv6. (Дополнительные сведения о поддержке IPv6 см. в разделе Поддержка анонимных входящих сообщений электронной почты по протоколу IPv6.)
ms.openlocfilehash: d2fab69847732bb7ed54f943d2c7845e06084936
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002277"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a>Поддержка проверки сообщений, подписанных с помощью DKIM

Службы Exchange Online Protection (EOP) и Exchange Online поддерживают проверку входящей почты сообщений, подписанных с помощью Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)). DKIM позволяет проверить, отправлено ли сообщение из заявленного домена и не подделали ли его. Сообщение электронной почты связывается с организацией, ответственной за его отправку. Проверка DKIM используется автоматически для всех сообщений, отправленных через подключения по протоколу IPv6. (Дополнительные сведения о поддержке IPv6 см. в разделе [Поддержка анонимных входящих сообщений электронной почты по протоколу IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)
  
DKIM проверяет сообщение с цифровой подписью, которое отображается в заголовке DKIM-Signature в заголовках сообщения. Результаты проверки заголовка DKIM-Signature помечаются в заголовке Authentication-Results, который соответствует спецификации RFC 7001 ([Поле заголовка сообщения для указания состояния проверки подлинности сообщения](https://www.rfc-editor.org/rfc/rfc7001.txt)). Текст заголовка сообщения имеет указанные ниже формат (где contoso.com  отправитель).
  
 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`
  
Администраторы могут создавать [Transport Rules](http://technet.microsoft.com/library/743bd525-0ca2-426d-b76c-b4a052bc8886.aspx) по результатам проверки DKIM, чтобы при необходимости фильтровать или направлять сообщения. 
  

