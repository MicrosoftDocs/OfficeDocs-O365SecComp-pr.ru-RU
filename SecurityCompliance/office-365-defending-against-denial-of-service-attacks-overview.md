---
title: Защита от атак типа "отказ в обслуживании" в Office 365
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
description: Обзор атак типа "отказ в обслуживании" (DoS).
ms.openlocfilehash: 94f87a11f396cb8ef09fd6d670d73ba8d1e88eda
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/05/2019
ms.locfileid: "36761665"
---
# <a name="defend-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="5a7c0-103">Защита от атак типа "отказ в обслуживании" в Office 365</span><span class="sxs-lookup"><span data-stu-id="5a7c0-103">Defend Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="5a7c0-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="5a7c0-104">Introduction</span></span>

<span data-ttu-id="5a7c0-105">Корпорация Майкрософт предоставляет надежную инфраструктуру для более чем 200 облачных служб, размещенных в глобальной облачной инфраструктуре с более чем 100 центрами обработки данных.</span><span class="sxs-lookup"><span data-stu-id="5a7c0-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services hosted in a global cloud infrastructure of more than 100 datacenters.</span></span> <span data-ttu-id="5a7c0-106">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="5a7c0-106">These include:</span></span>

- <span data-ttu-id="5a7c0-107">Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="5a7c0-107">Microsoft Azure</span></span>
- <span data-ttu-id="5a7c0-108">Microsoft Bing</span><span class="sxs-lookup"><span data-stu-id="5a7c0-108">Microsoft Bing</span></span>
- <span data-ttu-id="5a7c0-109">Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="5a7c0-109">Microsoft Dynamics 365</span></span>
- <span data-ttu-id="5a7c0-110">Microsoft Office 365</span><span class="sxs-lookup"><span data-stu-id="5a7c0-110">Microsoft Office 365</span></span>
- <span data-ttu-id="5a7c0-111">Microsoft OneDrive</span><span class="sxs-lookup"><span data-stu-id="5a7c0-111">Microsoft OneDrive</span></span>
- <span data-ttu-id="5a7c0-112">Skype</span><span class="sxs-lookup"><span data-stu-id="5a7c0-112">Skype</span></span>
- <span data-ttu-id="5a7c0-113">Xbox LIVE</span><span class="sxs-lookup"><span data-stu-id="5a7c0-113">Xbox Live</span></span>

<span data-ttu-id="5a7c0-114">Как глобальная организация со значительным присутствием в Интернете и многими выразительноми свойствами Интернета, предоставляющими облачные службы, корпорация Майкрософт представляет собой большой общий целевой объект для хакеров и других вредоносных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5a7c0-114">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals.</span></span> <span data-ttu-id="5a7c0-115">Уровень сетевого взаимодействия между клиентами и облаком Майкрософт является одной из крупнейших целевых объектов вредоносных атак.</span><span class="sxs-lookup"><span data-stu-id="5a7c0-115">The network communication layer between clients and the Microsoft Cloud is one of the biggest targets of malicious attacks.</span></span> <span data-ttu-id="5a7c0-116">На самом деле, корпорация Майкрософт непрерывно и постоянно работает в некоторых формах сетевых цибераттакк.</span><span class="sxs-lookup"><span data-stu-id="5a7c0-116">In fact, Microsoft is continuously and persistently under some form of network-based cyberattack.</span></span> <span data-ttu-id="5a7c0-117">В этом случае корпорация Майкрософт использует принципы защиты от глубокой защиты для защиты облачных служб и сетей.</span><span class="sxs-lookup"><span data-stu-id="5a7c0-117">In line with this, Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> <span data-ttu-id="5a7c0-118">Без надежных и постоянных систем защиты, которые защищаются от этих атак, облачные службы Майкрософт будут отключены от сети и недоступны для пользователей.</span><span class="sxs-lookup"><span data-stu-id="5a7c0-118">Without reliable and persistent mitigation systems that defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="5a7c0-119">Определение и признаки атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="5a7c0-119">Definition and Symptoms of Denial-of-Service Attacks</span></span>

<span data-ttu-id="5a7c0-120">Один из способов атаки на сетевые службы состоит в том, чтобы создать большое количество запросов к узлам служб, чтобы перегрузить сеть и серверы для отказа от обслуживания легальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5a7c0-120">One way to attack network services is to create many requests against service hosts to overwhelm the network and servers to deny service to legitimate users.</span></span> <span data-ttu-id="5a7c0-121">Это называется атакой типа "отказ в обслуживании" (DoS).</span><span class="sxs-lookup"><span data-stu-id="5a7c0-121">This is referred to as a denial-of-service (DoS) attack.</span></span> <span data-ttu-id="5a7c0-122">Когда атака выполняется несколькими субъектами, конечными точками и/или векторами, она называется атакой с распределенным отказом в обслуживании (DDoS).</span><span class="sxs-lookup"><span data-stu-id="5a7c0-122">When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack.</span></span> <span data-ttu-id="5a7c0-123">Несмотря на то, что средства, мотивес и целевые объекты различаются, атаки DoS и DDoS обычно состоят из усилий по предотвращению нормальной или неправильной работы Интернет-сайта или службы.</span><span class="sxs-lookup"><span data-stu-id="5a7c0-123">Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of efforts to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="5a7c0-124">[Группа "экстренная готовность компьютера" США](https://www.us-cert.gov/) (США-CERT) определяет признаки атак DOS:</span><span class="sxs-lookup"><span data-stu-id="5a7c0-124">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>

- <span data-ttu-id="5a7c0-125">Необычно низкая производительность сети (при открытии файлов или доступе к Интернет-сайтам)</span><span class="sxs-lookup"><span data-stu-id="5a7c0-125">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="5a7c0-126">Недоступность веб-сайта</span><span class="sxs-lookup"><span data-stu-id="5a7c0-126">Unavailability of a Web site</span></span>
- <span data-ttu-id="5a7c0-127">Невозможность доступа к веб-сайту</span><span class="sxs-lookup"><span data-stu-id="5a7c0-127">Inability to access a Web site</span></span>
- <span data-ttu-id="5a7c0-128">Значительное увеличение получаемых нежелательных сообщений</span><span class="sxs-lookup"><span data-stu-id="5a7c0-128">Dramatic increase in received spam</span></span>
- <span data-ttu-id="5a7c0-129">Отключение беспроводного или беспроводного подключения к Интернету</span><span class="sxs-lookup"><span data-stu-id="5a7c0-129">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="5a7c0-130">Долгосрочный отказ в доступе к Интернету или Интернет-службам</span><span class="sxs-lookup"><span data-stu-id="5a7c0-130">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a7c0-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5a7c0-131">Related Topics</span></span>

- [<span data-ttu-id="5a7c0-132">Основные принципы защиты от атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="5a7c0-132">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="5a7c0-133">Стратегия защиты от атак типа "отказ в обслуживании" корпорации Майкрософт</span><span class="sxs-lookup"><span data-stu-id="5a7c0-133">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="5a7c0-134">Защита облачных служб Майкрософт от атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="5a7c0-134">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
