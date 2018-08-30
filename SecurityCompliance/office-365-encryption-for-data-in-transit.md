---
title: Шифрование Office 365 при передаче данных
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Сводка: Краткое описание как Microsoft шифрует данные в ходе доставки.'
ms.openlocfilehash: 8f4781cf1127fb1b6bf742c267c76e3df39b8209
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534301"
---
# <a name="office-365-encryption-for-data-in-transit"></a>Шифрование Office 365 при передаче данных

В дополнение к защите статических данных клиента, корпорация Майкрософт использует технологии шифрования для защиты данных клиента Office 365 в пути. 

Данные находятся в пути:
- Когда клиентский компьютер взаимодействует с сервером Office 365;
- Когда сервер Office 365 взаимодействует с другим сервером Office 365; и
- Когда сервер Office 365 взаимодействует с сервером Office 365 (например, Exchange Online выполнению электронной почты внешнего почтовый сервер).

Взаимодействия между каналами центра обработки данных связи между серверами Office 365 осуществляется через TLS или IPsec, а все серверы заказчика согласование безопасного сеанса с использованием TLS с клиентскими компьютерами (например, Exchange Online использует TLS 1.2 с 256-разрядного шифрования силы используется (FIPS 140-2 уровень проверки 2). (Просмотреть [Справочные сведения о шифровании в Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) список наборов шифрования TLS, поддерживаются в Office 365). Это относится к протоколов, используемых клиентами, например Outlook, Скайп для бизнеса и Outlook в Интернете (например, HTTP, POP3, и т.д.).

Сертификаты открытого выдаются Microsoft IT SSL с помощью SSLAdmin, внутренний средство Майкрософт для защиты конфиденциальности передаваемых данных. Все сертификаты, выданные ИТ-отдела Майкрософт не менее 2048 бит в длину и соответствия [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) требуется SSLAdmin, чтобы убедиться в том, что сертификаты выдаются только общие IP-адреса, принадлежащие Майкрософт. IP-адресов, не этот критерий направляются через процесс исключение.

Все сведения о реализации как версия используется протокол TLS, включена ли переадресовывать безопасной пересылки (FS), порядок наборы шифрования, и др., доступны публично. — Это один из способов видеть эти сведения для использования веб-сайта сторонних производителей, такие как руководства Компанию Qualys SSL (www.ssllabs.com). Ниже приведены ссылки на страницы, автоматического теста из Компанию Qualys, отображать сведения для следующих служб:
- [Портал Office 365](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Скайп для бизнеса (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Скайп для бизнеса (Интернет)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Для Exchange Online Protection URL-адреса в зависимости от имен клиента; Тем не менее все клиенты можно проверить с помощью **microsoft com.mail.protection.outlook.com**Office 365.
