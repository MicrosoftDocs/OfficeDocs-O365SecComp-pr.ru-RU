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
# <a name="office-365-mailbox-migrations"></a><span data-ttu-id="dc673-103">Перенос почтовых ящиков Office 365</span><span class="sxs-lookup"><span data-stu-id="dc673-103">Office 365 Mailbox Migrations</span></span>
<span data-ttu-id="dc673-p101">На основе Exchange гибридного развертывания клиенты можно выбрать для перемещения почтовых ящиков Exchange в локальной организации [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) или перемещение почтовых ящиков Exchange Online в [локальную систему Exchange](https://docs.microsoft.com/Exchange/exchange-server) организации. Пакеты миграции используются при перемещении почтовых ящиков между локальной организацией и организацией Exchange Online. Клиенты можно просмотреть статистику и другие сведения о миграции почтовых ящиков с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="dc673-p101">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization. Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations. Customers can review statistics and other information about mailbox migrations using the following cmdlets:</span></span>

- <span data-ttu-id="dc673-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - предоставляет статистику по умолчанию для почтового ящика пользователя, который включает в себя состояние, размер почтового ящика, архивация размер почтового ящика и процент выполнения.</span><span class="sxs-lookup"><span data-stu-id="dc673-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size and percentage complete.</span></span>
- <span data-ttu-id="dc673-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - предоставляет сводный список почтовых ящиков объекты и атрибуты в организации.</span><span class="sxs-lookup"><span data-stu-id="dc673-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="dc673-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - список существующих объектов с включенной поддержкой почты как почтовые ящики, пользователей почты, контакты и группы рассылки.</span><span class="sxs-lookup"><span data-stu-id="dc673-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts and distribution groups.</span></span>
- <span data-ttu-id="dc673-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - предоставляет подробного состояния текущего почтовые ящики, миграция.</span><span class="sxs-lookup"><span data-stu-id="dc673-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="dc673-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - сведения о почтовом ящике перемещения и миграции пользователей.</span><span class="sxs-lookup"><span data-stu-id="dc673-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="dc673-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - предоставляются сведения о состоянии текущего пакета миграции.</span><span class="sxs-lookup"><span data-stu-id="dc673-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="dc673-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - предоставляет подробные сведения о состоянии миграции для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc673-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="dc673-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - предоставляет сведения о почтовых ящиках, такие как размер, количество сообщений и время последнего доступа.</span><span class="sxs-lookup"><span data-stu-id="dc673-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="dc673-115">Дополнительные сведения о дополнительных командлеты видеть [командлеты перемещения и миграции в Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="dc673-115">For more information on additional cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
