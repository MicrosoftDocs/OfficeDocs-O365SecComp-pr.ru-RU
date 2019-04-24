---
title: Мониторинг и отчет о состоянии безопасности в центре безопасности Майкрософт 365
description: В этой статье описано, как центр безопасности Microsoft 365 предоставляет краткий обзор защиты и состояния безопасности.
keywords: безопасность, вредоносные программы, Microsoft 365, M365, центр безопасности, монитор, отчет, состояние
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 0a0bcbde7daa79aabda30013fca2560384545feb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263131"
---
# <a name="monitor-and-report-security-status-in-microsoft-365-security-center"></a><span data-ttu-id="3fe34-104">Мониторинг и отчет о состоянии безопасности в центре безопасности Майкрософт 365</span><span class="sxs-lookup"><span data-stu-id="3fe34-104">Monitor and report security status in Microsoft 365 security center</span></span>

<span data-ttu-id="3fe34-105">Центр безопасности Microsoft 365 предоставляет краткий обзор защиты и состояния безопасности в среде Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3fe34-105">The Microsoft 365 security center provides at a glance summary of protection and security status across your Microsoft 365 environment.</span></span>

<span data-ttu-id="3fe34-106">Центр обеспечения безопасности включает раздел **_амп_ Reports (отчеты о мониторинге** ), в котором размещается узел карточек, охватывающий различные области, которые отслеживаются аналитиками и администраторами безопасности в рамках повседневных операций.</span><span class="sxs-lookup"><span data-stu-id="3fe34-106">The security center includes a **Monitoring & reports** section which features a host of cards covering a variety of areas that security analysts and administrators track as part of their day-to-day operations.</span></span> <span data-ttu-id="3fe34-107">При детализации карточки предоставляют подробные отчеты и, в некоторых случаях, параметры управления.</span><span class="sxs-lookup"><span data-stu-id="3fe34-107">On drill-down, cards provide detailed reports and, in some cases, management options.</span></span>

## <a name="customize-views"></a><span data-ttu-id="3fe34-108">Настройка представлений</span><span class="sxs-lookup"><span data-stu-id="3fe34-108">Customize views</span></span>

<span data-ttu-id="3fe34-109">По умолчанию карты мониторинга и отчетов сгруппированы по следующим категориям:</span><span class="sxs-lookup"><span data-stu-id="3fe34-109">By default, monitoring and report cards are grouped into these categories:</span></span>
  
* <span data-ttu-id="3fe34-110">[Удостоверения](monitor-and-report-identities.md) — учетные записи пользователей и учетные данные</span><span class="sxs-lookup"><span data-stu-id="3fe34-110">[Identities](monitor-and-report-identities.md) – user accounts and credentials</span></span>
* <span data-ttu-id="3fe34-111">[Данные](monitor-data.md) — электронная почта и содержимое документа</span><span class="sxs-lookup"><span data-stu-id="3fe34-111">[Data](monitor-data.md) – email and document contents</span></span>
* <span data-ttu-id="3fe34-112">[Устройства](monitor-devices.md) — компьютеры, мобильные телефоны и другие устройства</span><span class="sxs-lookup"><span data-stu-id="3fe34-112">[Devices](monitor-devices.md) – computers, mobile phones, and other devices</span></span>
* <span data-ttu-id="3fe34-113">[Приложения](monitor-apps.md) — программы и подключенные веб-службы</span><span class="sxs-lookup"><span data-stu-id="3fe34-113">[Apps](monitor-apps.md) – programs and attached online services</span></span>

<span data-ttu-id="3fe34-114">Переключитесь в **раздел группировать по разделу**, чтобы изменить порядок карточек и сгруппировать их в следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="3fe34-114">Switch to **Group by topic**, to rearrange the cards and group them into the following:</span></span>

* <span data-ttu-id="3fe34-115">**Риск** — карточки, на которых выделяются сущности, такие как учетные записи и устройства, которые могут быть подвержены риску.</span><span class="sxs-lookup"><span data-stu-id="3fe34-115">**Risk** – cards that highlight entities, such as accounts and devices, that might be at risk.</span></span> <span data-ttu-id="3fe34-116">Эти карточки также выделяют возможные источники риска, такие как новые кампании по угрозе и привилегированные облачные приложения</span><span class="sxs-lookup"><span data-stu-id="3fe34-116">These cards also highlight possible sources of risk, such as new threat campaigns and privileged cloud apps</span></span>  
* <span data-ttu-id="3fe34-117">**Тенденции обнаружения** — карты, которые выделяют новые средства обнаружения угроз, аномалий и нарушения политики</span><span class="sxs-lookup"><span data-stu-id="3fe34-117">**Detection trends** – cards that highlight new threat detections, anomalies, and policy violations</span></span>
* <span data-ttu-id="3fe34-118">**Конфигурация и работоспособность** — карты, охватывающие конфигурацию и развертывание элементов управления безопасностью, в том числе состояния подключения устройств к службам управления.</span><span class="sxs-lookup"><span data-stu-id="3fe34-118">**Configuration and health** – cards that cover the configuration and deployment of security controls, including device onboarding states to management services</span></span>
* <span data-ttu-id="3fe34-119">**Другие** — все остальные карточки, не отнесенные к другим разделам</span><span class="sxs-lookup"><span data-stu-id="3fe34-119">**Other** – all other cards not categorized under other topics</span></span>
