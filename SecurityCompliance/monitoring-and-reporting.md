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
ms.openlocfilehash: 2dcc82dd6eb64567ed944ff8fc876a029d82f74a
ms.sourcegitcommit: ef27da3ea5340d6e7a2eaa1288e2e005ef8e4788
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/23/2019
ms.locfileid: "30791870"
---
# <a name="monitor-and-report-security-status-in-microsoft-365-security-center"></a><span data-ttu-id="93923-104">Мониторинг и отчет о состоянии безопасности в центре безопасности Майкрософт 365</span><span class="sxs-lookup"><span data-stu-id="93923-104">Monitor and report security status in Microsoft 365 security center</span></span>

[!include[Prerelease�information](prerelease.md)]

<span data-ttu-id="93923-105">Центр безопасности Microsoft 365 предоставляет краткий обзор защиты и состояния безопасности в среде Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="93923-105">The Microsoft 365 security center provides at a glance summary of protection and security status across your Microsoft 365 environment.</span></span>

<span data-ttu-id="93923-106">Центр обеспечения безопасности включает раздел **_амп_ Reports (отчеты о мониторинге** ), в котором размещается узел карточек, охватывающий различные области, которые отслеживаются аналитиками и администраторами безопасности в рамках повседневных операций.</span><span class="sxs-lookup"><span data-stu-id="93923-106">The security center includes a **Monitoring & reports** section which features a host of cards covering a variety of areas that security analysts and administrators track as part of their day-to-day operations.</span></span> <span data-ttu-id="93923-107">При детализации карточки предоставляют подробные отчеты и, в некоторых случаях, параметры управления.</span><span class="sxs-lookup"><span data-stu-id="93923-107">On drill-down, cards provide detailed reports and, in some cases, management options.</span></span>

## <a name="customize-views"></a><span data-ttu-id="93923-108">Настройка представлений</span><span class="sxs-lookup"><span data-stu-id="93923-108">Customize views</span></span>

<span data-ttu-id="93923-109">По умолчанию карты мониторинга и отчетов сгруппированы по следующим категориям:</span><span class="sxs-lookup"><span data-stu-id="93923-109">By default, monitoring and report cards are grouped into these categories:</span></span>
  
* <span data-ttu-id="93923-110">[Удостоверения](monitor-and-report-identities.md) — учетные записи пользователей и учетные данные</span><span class="sxs-lookup"><span data-stu-id="93923-110">[Identities](monitor-and-report-identities.md) – user accounts and credentials</span></span>
* <span data-ttu-id="93923-111">[Данные](monitor-data.md) — электронная почта и содержимое документа</span><span class="sxs-lookup"><span data-stu-id="93923-111">[Data](monitor-data.md) – email and document contents</span></span>
* <span data-ttu-id="93923-112">[Устройства](monitor-devices.md) — компьютеры, мобильные телефоны и другие устройства</span><span class="sxs-lookup"><span data-stu-id="93923-112">[Devices](monitor-devices.md) – computers, mobile phones, and other devices</span></span>
* <span data-ttu-id="93923-113">[Приложения](monitor-apps.md) — программы и подключенные веб-службы</span><span class="sxs-lookup"><span data-stu-id="93923-113">[Apps](monitor-apps.md) – programs and attached online services</span></span>

<span data-ttu-id="93923-114">Переключитесь в **раздел группировать по разделу**, чтобы изменить порядок карточек и сгруппировать их в следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="93923-114">Switch to **Group by topic**, to rearrange the cards and group them into the following:</span></span>

* <span data-ttu-id="93923-115">**Риск** — карточки, на которых выделяются сущности, такие как учетные записи и устройства, которые могут быть подвержены риску.</span><span class="sxs-lookup"><span data-stu-id="93923-115">**Risk** – cards that highlight entities, such as accounts and devices, that might be at risk.</span></span> <span data-ttu-id="93923-116">Эти карточки также выделяют возможные источники риска, такие как новые кампании по угрозе и привилегированные облачные приложения</span><span class="sxs-lookup"><span data-stu-id="93923-116">These cards also highlight possible sources of risk, such as new threat campaigns and privileged cloud apps</span></span>  
* <span data-ttu-id="93923-117">**Тенденции обнаружения** — карты, которые выделяют новые средства обнаружения угроз, аномалий и нарушения политики</span><span class="sxs-lookup"><span data-stu-id="93923-117">**Detection trends** – cards that highlight new threat detections, anomalies, and policy violations</span></span>
* <span data-ttu-id="93923-118">**Конфигурация и работоспособность** — карты, охватывающие конфигурацию и развертывание элементов управления безопасностью, в том числе состояния подключения устройств к службам управления.</span><span class="sxs-lookup"><span data-stu-id="93923-118">**Configuration and health** – cards that cover the configuration and deployment of security controls, including device onboarding states to management services</span></span>
* <span data-ttu-id="93923-119">**Другие** — все остальные карточки, не отнесенные к другим разделам</span><span class="sxs-lookup"><span data-stu-id="93923-119">**Other** – all other cards not categorized under other topics</span></span>