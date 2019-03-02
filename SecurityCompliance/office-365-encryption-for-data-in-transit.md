---
title: Шифрование в Office 365 для переСылки данных
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: Сводка. краткое объяснение того, как корпорация Майкрософт шифрует данные при передаче.
ms.openlocfilehash: ba1317a0a2a685d0f3ac2216939d04e402503e49
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357610"
---
# <a name="office-365-encryption-for-data-in-transit"></a>Шифрование в Office 365 для пересылки данных

Помимо защиты данных клиентов, корпорация Майкрософт использует технологии шифрования для защиты данных клиентов Office 365 в транзитном офисе. 

Данные находятся в пути:

- Когда клиентский компьютер обменивается данными с сервером Office 365;
- Когда сервер Office 365 обменивается данными с другим сервером Office 365; с
- Когда сервер Office 365 обменивается данными с сервером, отличным от Office 365 (например, Exchange Online доставляет электронную почту на инородный сервер электронной почты).

Обмен данными между центрами обработки данных между серверами Office 365 выполняется по протоколу TLS или IPsec, а все серверы, подключенные к клиентам, согласовывают безопасный сеанс с помощью протокола TLS с клиентскими компьютерами (например, Exchange Online использует TLS 1,2 с 256-разрядным шифром (FIPS). 140-2 — проверенный уровень 2). (Просмотрите [технические справочные сведения о шифровании в office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) , чтобы получить список комплектов шифров TLS, поддерживаемых в Office 365.) Это относится к протоколам, используемым клиентами, таким как Outlook, Skype для бизнеса и Outlook в Интернете (например, HTTP, POP3 и т. д.).

Общедоступные сертификаты выдаются по ПРОТОКОЛу Microsoft IT SSL с помощью Ссладмин, внутреннего средства Майкрософт для защиты конфиденциальности передаваемых данных. Все сертификаты, выданные корпорацией Майкрософт, имеют значение не менее 2048 бит, а для обеспечения соответствия требованиям [вебтруст](http://www.webtrust.org/homepage-documents/item70372.pdf) требуется ссладмин, чтобы сертификаты выдавались только общеДОСТУПНЫМ IP-адресам, принадлежащим корпорации Майкрософт. Все IP-адреса, которые не удовлетворяют этому критерию, направляются через процесс исключения.

Все детали реализации, такие как используемая версия протокола TLS, включена ли функция переСылки безопасной (Федерации), порядок комплектов шифров и т. д. доступно в открытых источниках. Один из способов просмотреть эти сведения — использовать сторонний веб-сайт, такой как Куалис SSL (www.ssllabs.com). Ниже приведены ссылки на страницы автоматизированного теста из Куалис, отображающие сведения о следующих службах:

- [Портал Office 365](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype для бизнеса (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype для бизнеса (Интернет)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Для Exchange Online Protection URL-адреса различаются в зависимости от имен клиентов; Тем не менее, все клиенты могут тестировать Office 365 с помощью **Microsoft-COM.mail.Protection.Outlook.com**.
