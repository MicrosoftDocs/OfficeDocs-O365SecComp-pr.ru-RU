---
title: Элементы управления доступа к Office 365 Yammer Enterprise
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
description: 'Сводка: Краткие сведения об элементах управления доступа к Yammer Enterprise в рабочей среде.'
ms.openlocfilehash: 3f51e63c16022353e743b57d8e977f2ea2e6a835
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535368"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="91aa9-103">Элементы управления доступом к Yammer корпоративный</span><span class="sxs-lookup"><span data-stu-id="91aa9-103">Yammer Enterprise Access Controls</span></span> 

<span data-ttu-id="91aa9-p101">Физические и логические доступа в рабочей среде Yammer ограничивается очень небольшое количество людей (инфраструктуры и операции). Как и в других Office 365 инженеров, инженеров Yammer доступны ноль положение данных клиента. Access должен запрос с помощью следующего защищенного хранилища системы управления доступом на основе утверждения в времени, и имеется ограниченное количество утверждающих. Утверждающие проверьте запрос (например, они проверить, является ли запрос допустимым по необходимости, экономическое обоснование, время, и т.д.), а затем утвердить или отклонить запрос. Если запрос утвержден, Требованию доступа для определенного и ограниченного времени, после которого автоматически истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="91aa9-p101">Both physical and logical access to the Yammer production environment is restricted to a very small set of people (infrastructure and operations). As with other Office 365 engineers, Yammer engineers have zero standing access to Customer Data. Access must be requested using an approval-based just-in-time access control system similar to Lockbox, and there is a limited number of approvers. Approvers verify the request (e.g., they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request. If the request is approved, JIT access is granted for a defined and limited time, after which it automatically expires.</span></span> 

<span data-ttu-id="91aa9-p102">Как и в случае с другими службами Office 365 все доступа в рабочей среде Yammer использует многофакторной проверки подлинности. Все истории доступа и команду атрибутами пользователя и вход и регулярно контролировать группой безопасности сети Yammer.</span><span class="sxs-lookup"><span data-stu-id="91aa9-p102">As with other Office 365 services, all access to the Yammer production environment leverages multi-factor authentication. All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="91aa9-111">Дополнительные сведения о Yammer администрирования и управления к справке [Yammer администрирования](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="91aa9-111">For more information about Yammer administration and management, see [Yammer Admin Help](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US).</span></span>