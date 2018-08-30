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
ms.collection: Strat_O365_Enterprise
description: Краткий обзор командлетов для миграции почтовых ящиков в Office 365.
ms.openlocfilehash: 86896d956072b5c11e3b3292363bb32312ff1187
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535101"
---
# <a name="office-365-mailbox-migrations"></a>Перенос почтовых ящиков Office 365
На основе Exchange гибридного развертывания клиенты можно выбрать для перемещения почтовых ящиков Exchange в локальной организации [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) или перемещение почтовых ящиков Exchange Online в [локальную систему Exchange](https://docs.microsoft.com/Exchange/exchange-server) организации. Пакеты миграции используются при перемещении почтовых ящиков между локальной организацией и организацией Exchange Online. Клиенты можно просмотреть статистику и другие сведения о миграции почтовых ящиков с помощью следующих командлетов:

- [Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - предоставляет статистику по умолчанию для почтового ящика пользователя, который включает в себя состояние, размер почтового ящика, архивация размер почтового ящика и процент выполнения.
- [Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - предоставляет сводный список почтовых ящиков объекты и атрибуты в организации.
- [Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - список существующих объектов с включенной поддержкой почты как почтовые ящики, пользователей почты, контакты и группы рассылки.
- [Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - предоставляет подробного состояния текущего почтовые ящики, миграция.
- [Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - сведения о почтовом ящике перемещения и миграции пользователей.
- [Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - предоставляются сведения о состоянии текущего пакета миграции.
- [Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - предоставляет подробные сведения о состоянии миграции для определенного пользователя.
- [Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - предоставляет сведения о почтовых ящиках, такие как размер, количество сообщений и время последнего доступа.

Дополнительные сведения о дополнительных командлеты видеть [командлеты перемещения и миграции в Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
