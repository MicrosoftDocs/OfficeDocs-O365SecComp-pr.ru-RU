---
title: Ограничения ресурсов для Office 365
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
description: 'Сводка: Сведения о ресурсе ограничения для различных приложений в Office 365.'
ms.openlocfilehash: a2e7ef42f9bf224363f3b10a5e450d6127f11585
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535512"
---
# <a name="resource-limits"></a><span data-ttu-id="19dcb-103">Ограничения ресурсов</span><span class="sxs-lookup"><span data-stu-id="19dcb-103">Resource Limits</span></span>

<span data-ttu-id="19dcb-p101">С помощью квот (ограничения) и регулирования принудительно применяются ограничения ресурсов. Отдельные службы Office 365 и Azure Active Directory используйте их вместе. Ограничения для конкретной службы и измените по времени по мере добавления новых возможностей. Сведения о текущем ограничения для различных служб содержатся в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="19dcb-p101">Resource limits are enforced using quotas (limits) and throttling. Azure Active Directory and the individual Office 365 services use both. Limits are service-specific and change over time as new capabilities are added. For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="19dcb-108">Ограничения для службы Active Directory и ограничения для Azure</span><span class="sxs-lookup"><span data-stu-id="19dcb-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="19dcb-109">Ограничения Exchange Online</span><span class="sxs-lookup"><span data-stu-id="19dcb-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="19dcb-110">Ограничения Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="19dcb-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="19dcb-111">SharePoint Online программные ограничения и лимиты</span><span class="sxs-lookup"><span data-stu-id="19dcb-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="19dcb-112">Скайп для ограничения для бизнеса</span><span class="sxs-lookup"><span data-stu-id="19dcb-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="19dcb-113">Ограничения скорости и API-Интерфейс REST Yammer</span><span class="sxs-lookup"><span data-stu-id="19dcb-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="19dcb-114">Ограничения на размер файла в Sway</span><span class="sxs-lookup"><span data-stu-id="19dcb-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="19dcb-p102">В дополнение к эти ограничения несколько механизмы регулирования используются в Office 365 и Azure Active Directory. Регулирование службы особенно важно, учитывая, что сетевых ресурсов в центрах обработки данных Майкрософт, оптимизированные для широкий набор клиентов, использующих службы. Механизмы регулирования, относятся:</span><span class="sxs-lookup"><span data-stu-id="19dcb-p102">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365. Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services. Throttling mechanisms include:</span></span>
- <span data-ttu-id="19dcb-118">Azure Active Directory и регулирования уровня пользователя компонентов Office 365, которые ограничить число транзакций или одновременных звонков (по сценарий или код), которые могут выполняться с одним пользователем.</span><span class="sxs-lookup"><span data-stu-id="19dcb-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="19dcb-p103">По умолчанию политики регулирования PowerShell назначается для каждого клиента при создании клиента. Эти параметры влияют на других элементов, таких как максимальное количество одновременных сеансов PowerShell, которые можно открыть в одной администратор.</span><span class="sxs-lookup"><span data-stu-id="19dcb-p103">A default PowerShell throttling policy is assigned to each tenant at tenant creation. These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="19dcb-121">Каждый клиент Exchange Online имеет политику по умолчанию веб-служб Exchange (EWS), который настроен для операций клиента веб-служб Exchange и регулирования, который применяется для всех клиентов Outlook.</span><span class="sxs-lookup"><span data-stu-id="19dcb-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
