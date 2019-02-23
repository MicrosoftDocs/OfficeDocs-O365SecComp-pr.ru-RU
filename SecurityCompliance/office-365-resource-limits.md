---
title: Пределы ресурсов для Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Сводка. сведения об ограничении ресурсов для различных приложений в Office 365.
ms.openlocfilehash: ee44bde8bd93d3628ed3f31f5bbbce024a3056b5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220219"
---
# <a name="resource-limits"></a><span data-ttu-id="0b4d4-103">Ограничения ресурсов</span><span class="sxs-lookup"><span data-stu-id="0b4d4-103">Resource Limits</span></span>

<span data-ttu-id="0b4d4-p101">Ограничения ресурсов применяются с помощью квот (ограничений) и регулирования. Azure Active Directory и отдельные службы Office 365 используют оба. При добавлении новых возможностей преДельные значения задаются для конкретных служб и изменяются с течением времени. Сведения о текущих пределах для различных служб представлены в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="0b4d4-p101">Resource limits are enforced using quotas (limits) and throttling. Azure Active Directory and the individual Office 365 services use both. Limits are service-specific and change over time as new capabilities are added. For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="0b4d4-108">Ограничения и ограничения для службы Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="0b4d4-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="0b4d4-109">Ограничения Exchange Online</span><span class="sxs-lookup"><span data-stu-id="0b4d4-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="0b4d4-110">Ограничения Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="0b4d4-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="0b4d4-111">Границы и ограничения программного обеспечения SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="0b4d4-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="0b4d4-112">Пределы Skype для бизнеса</span><span class="sxs-lookup"><span data-stu-id="0b4d4-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="0b4d4-113">API REST для REST и пределы скорости</span><span class="sxs-lookup"><span data-stu-id="0b4d4-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="0b4d4-114">ПреДельные значения для размера файлов в Sway</span><span class="sxs-lookup"><span data-stu-id="0b4d4-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="0b4d4-p102">В дополнение к этим ограничениям в Azure Active Directory и Office 365 используются несколько механизмов регулирования. Регулирование в службе особенно важно, так как сетевые ресурсы в центрах обработки данных корпорации Майкрософт оптимизированы для широкого набора клиентов, использующих эти службы. Механизмы регулирования включают:</span><span class="sxs-lookup"><span data-stu-id="0b4d4-p102">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365. Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services. Throttling mechanisms include:</span></span>
- <span data-ttu-id="0b4d4-118">Функция регулирования на уровне пользователей Azure Active Directory и Office 365, которая ограничивает количество транзакций или одновременных вызовов (в соответствии со сценарием или кодом), которые могут выполняться одним пользователем.</span><span class="sxs-lookup"><span data-stu-id="0b4d4-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="0b4d4-p103">Политика регулирования PowerShell по умолчанию назначается каждому клиенту при создании клиента. Эти параметры влияют на другие элементы, например максимальное количество одновременных сеансов PowerShell, которые могут быть открыты одним администратором.</span><span class="sxs-lookup"><span data-stu-id="0b4d4-p103">A default PowerShell throttling policy is assigned to each tenant at tenant creation. These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="0b4d4-121">У каждого клиента Exchange Online есть политика веб-служб Exchange по умолчанию (EWS), которая настроена на выполнение клиентских операций EWS, и регулирование, которое применяется ко всем клиентам Outlook.</span><span class="sxs-lookup"><span data-stu-id="0b4d4-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
