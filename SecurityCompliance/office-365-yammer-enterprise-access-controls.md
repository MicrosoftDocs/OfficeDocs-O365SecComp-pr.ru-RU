---
title: Элементы управления доступом к Office 365 Yammer корпоративный
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
description: Сводка. Краткие сведения об элементах управления корпоративным доступом в Yammer в рабочей среде.
ms.openlocfilehash: 61598235a010aaa1c578c449cb054073212a41f9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262351"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="8f44a-103">Элементы управления доступом к Yammer корпоративный</span><span class="sxs-lookup"><span data-stu-id="8f44a-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="8f44a-104">Физический и логический доступ к рабочей среде Yammer ограничены очень небольшим набором людей (инфраструктурой и операциями).</span><span class="sxs-lookup"><span data-stu-id="8f44a-104">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations).</span></span> <span data-ttu-id="8f44a-105">Как и в случае с другими инженерами Office 365, инженеры Yammer имеют нулевой доступ к данным клиента.</span><span class="sxs-lookup"><span data-stu-id="8f44a-105">As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data.</span></span> <span data-ttu-id="8f44a-106">Доступ должен запрашиваться с помощью системы управления доступом на основе утверждений, аналогичной системе управления защищенным доступом, и ограниченным количеством утверждающих.</span><span class="sxs-lookup"><span data-stu-id="8f44a-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers.</span></span> <span data-ttu-id="8f44a-107">Утверждающие проверяют запрос (например, проверяет, является ли запрос действительным на основании потребностей, Бизнес-дел, времени и т. д.), а затем Утвердите или отклоните запрос.</span><span class="sxs-lookup"><span data-stu-id="8f44a-107">Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="8f44a-108">Если запрос утвержден, JIT-доступ предоставляется для определенного и ограниченного времени, после которого срок действия автоматически истечет.</span><span class="sxs-lookup"><span data-stu-id="8f44a-108">If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="8f44a-109">Как и в случае с другими службами Office 365, при доступе к рабочей среде Yammer используется многофакторная проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="8f44a-109">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication.</span></span> <span data-ttu-id="8f44a-110">Все пользователи получают доступ к журналу команд и записываются в журнал и регулярно проверяются группой безопасности Yammer.</span><span class="sxs-lookup"><span data-stu-id="8f44a-110">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="8f44a-111">Для получения дополнительных сведений об администрировании и управлении Yammer обратитесь к справочной статье [администратора Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="8f44a-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>