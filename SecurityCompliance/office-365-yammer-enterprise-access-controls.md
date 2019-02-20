---
title: Элементы управления доступом к Office 365 Yammer корпоративный
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
description: Сводка. Краткие сведения об элементах управления корпоративным доступом в Yammer в рабочей среде.
ms.openlocfilehash: 33126ee6acf42a97148c12917855535a8578e8cf
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090731"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="31ac1-103">Элементы управления доступом к Yammer корпоративный</span><span class="sxs-lookup"><span data-stu-id="31ac1-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="31ac1-p101">Физический и логический доступ к рабочей среде Yammer ограничены очень небольшим набором людей (инфраструктурой и операциями). Как и в случае с другими инженерами Office 365, инженеры Yammer имеют нулевой доступ к данным клиента. Доступ должен запрашиваться с помощью системы управления доступом на основе утверждений, аналогичной системе управления защищенным доступом, и ограниченным количеством утверждающих. Утверждающие проверяют запрос (например, проверяет, является ли запрос действительным на основании потребностей, Бизнес-дел, времени и т. д.), а затем Утвердите или отклоните запрос. Если запрос утвержден, JIT-доступ предоставляется для определенного и ограниченного времени, после которого срок действия автоматически истечет.</span><span class="sxs-lookup"><span data-stu-id="31ac1-p101">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations). As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data. Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers. Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request. If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="31ac1-p102">Как и в случае с другими службами Office 365, при доступе к рабочей среде Yammer используется многофакторная проверка подлинности. Все пользователи получают доступ к журналу команд и записываются в журнал и регулярно проверяются группой безопасности Yammer.</span><span class="sxs-lookup"><span data-stu-id="31ac1-p102">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication. All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="31ac1-111">Для получения дополнительных сведений об администрировании и управлении Yammer обратитесь к справочной статье [администратора Yammer](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="31ac1-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>