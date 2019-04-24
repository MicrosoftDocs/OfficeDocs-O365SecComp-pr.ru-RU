---
title: Перенос почтовых ящиков Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Краткое описание командлетов, используемых для миграции почтовых ящиков Office 365.
ms.openlocfilehash: f21462b1f4a1838ee617e0d429ba73f01ca2db90
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262581"
---
# <a name="office-365-mailbox-migrations"></a><span data-ttu-id="73b95-103">Перенос почтовых ящиков Office 365</span><span class="sxs-lookup"><span data-stu-id="73b95-103">Office 365 Mailbox Migrations</span></span>
<span data-ttu-id="73b95-104">С помощью гибридного развертывания на основе Exchange клиенты могут выбрать, как переместить локальные почтовые ящики Exchange в организацию [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) или переместить почтовые ящики Exchange Online в локальную организацию [Exchange](https://docs.microsoft.com/Exchange/exchange-server) .</span><span class="sxs-lookup"><span data-stu-id="73b95-104">With an Exchange-based hybrid deployment, customers can choose to either move on-premises Exchange mailboxes to an [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online) organization or move Exchange Online mailboxes to an [Exchange on-premises](https://docs.microsoft.com/Exchange/exchange-server) organization.</span></span> <span data-ttu-id="73b95-105">Пакеты миграции используются при перемещении почтовых ящиков между локальной организацией и организацией Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="73b95-105">Migration batches are used when moving mailboxes between on-premises and Exchange Online organizations.</span></span> <span data-ttu-id="73b95-106">Пользователи могут просматривать статистику и другие сведения о миграции почтовых ящиков с помощью следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="73b95-106">Customers can review statistics and other information about mailbox migrations using the following cmdlets:</span></span>

- <span data-ttu-id="73b95-107">[Get – MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) — предоставляет статистические данные по умолчанию для почтового ящика пользователя, включая состояние, размер почтового ящика, размер архивного почтового ящика и процент завершения.</span><span class="sxs-lookup"><span data-stu-id="73b95-107">[Get-MoveRequestStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequestStatistics?view=exchange-ps) - Provides default statistics for a user mailbox, which includes the status, mailbox size, archive mailbox size and percentage complete.</span></span>
- <span data-ttu-id="73b95-108">[Get/Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) — содержит сводный список объектов и атрибутов почтовых ящиков в Организации.</span><span class="sxs-lookup"><span data-stu-id="73b95-108">[Get-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-Mailbox?view=exchange-ps
) - Provides a summary list of mailbox objects and attributes in the organization.</span></span>
- <span data-ttu-id="73b95-109">[Get – Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) — предоставляет список существующих объектов с включенной поддержкой почты, таких как почтовые ящики, почтовые пользователи, контакты и группы рассылки.</span><span class="sxs-lookup"><span data-stu-id="73b95-109">[Get-Recipient](https://docs.microsoft.com/powershell/module/exchange/users-and-groups/Get-Recipient?view=exchange-ps) - Provides a list of existing mail-enabled objects such as mailboxes, mail users, contacts and distribution groups.</span></span>
- <span data-ttu-id="73b95-110">[Get – MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) — предоставляет подробные сведения о состоянии текущей миграции почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="73b95-110">[Get-MoveRequest](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MoveRequest?view=exchange-ps) - Provides a detailed status of an ongoing mailbox migration.</span></span>
- <span data-ttu-id="73b95-111">[Get – MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) — предоставляет сведения о пользователях перемещения и переноса почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="73b95-111">[Get-MigrationUser](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUser?view=exchange-ps) - Provides information about the mailbox move and migration users.</span></span>
- <span data-ttu-id="73b95-112">[Get – MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) — предоставляет сведения о состоянии текущего пакета миграции.</span><span class="sxs-lookup"><span data-stu-id="73b95-112">[Get-MigrationBatch](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationBatch?view=exchange-ps) - Provides information on the status of current migration batch.</span></span>
- <span data-ttu-id="73b95-113">[Get – мигратионусерстатистикс](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) — предоставляет подробные сведения о состоянии миграции для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="73b95-113">[Get-MigrationUserStatistics](https://docs.microsoft.com/powershell/module/exchange/move-and-migration/Get-MigrationUserStatistics?view=exchange-ps) - Provides detailed information about the migration status for a specific user.</span></span>
- <span data-ttu-id="73b95-114">[Get – MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) — предоставляет сведения о почтовых ящиках, такие как размер, количество сообщений и время последнего обращения.</span><span class="sxs-lookup"><span data-stu-id="73b95-114">[Get-MailboxStatistics](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Get-MailboxStatistics?view=exchange-ps) - Provides information about mailboxes, such as size, the number of messages, and the last accessed time.</span></span>

<span data-ttu-id="73b95-115">Дополнительные сведения о дополнительных командлетах приведены [в статье Move and Migration командлеты в Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="73b95-115">For more information on additional cmdlets, see [Move and Migration cmdlets in Exchange Online](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
