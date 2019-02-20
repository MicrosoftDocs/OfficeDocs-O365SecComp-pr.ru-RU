---
title: Перенос почтовых ящиков Office 365
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Краткое описание командлетов, используемых для миграции почтовых ящиков Office 365.
ms.openlocfilehash: 195497d94ab434c66a176e37fb84f6cd1da48baa
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090781"
---
# <a name="office-365-mailbox-migrations"></a>Перенос почтовых ящиков Office 365
С помощью гибридного развертывания на основе Exchange клиенты могут выбрать, как переместить локальные почтовые ящики Exchange в организацию [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) или переместить почтовые ящики Exchange Online в локальную организацию [Exchange](https://docs.microsoft.com/Exchange/exchange-server) . Пакеты миграции используются при перемещении почтовых ящиков между локальной организацией и организацией Exchange Online. Пользователи могут просматривать статистику и другие сведения о миграции почтовых ящиков с помощью следующих командлетов:

- [Get – MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) — предоставляет статистические данные по умолчанию для почтового ящика пользователя, включая состояние, размер почтового ящика, размер архивного почтового ящика и процент завершения.
- [Get/Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) — содержит сводный список объектов и атрибутов почтовых ящиков в Организации.
- [Get – Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) — предоставляет список существующих объектов с включенной поддержкой почты, таких как почтовые ящики, почтовые пользователи, контакты и группы рассылки.
- [Get – MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) — предоставляет подробные сведения о состоянии текущей миграции почтовых ящиков.
- [Get – MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) — предоставляет сведения о пользователях перемещения и переноса почтовых ящиков.
- [Get – MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) — предоставляет сведения о состоянии текущего пакета миграции.
- [Get – мигратионусерстатистикс](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) — предоставляет подробные сведения о состоянии миграции для определенного пользователя.
- [Get – MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) — предоставляет сведения о почтовых ящиках, такие как размер, количество сообщений и время последнего обращения.

Дополнительные сведения о дополнительных командлетах приведены [в статье Move and Migration командлеты в Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
