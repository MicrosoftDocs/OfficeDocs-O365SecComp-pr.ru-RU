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
ms.openlocfilehash: a7e67fcc87867190f345c5dad14e38a473420eab
ms.sourcegitcommit: 1261a37c414111f869df5791548a768d853fda60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/30/2019
ms.locfileid: "31004076"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="3375c-103">Защита от атак типа "отказ в обслуживании" в Office 365</span><span class="sxs-lookup"><span data-stu-id="3375c-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="3375c-104">Введение</span><span class="sxs-lookup"><span data-stu-id="3375c-104">Introduction</span></span>
<span data-ttu-id="3375c-105">Корпорация Майкрософт предоставляет надежную инфраструктуру для более чем 200 облачных служб, в том числе Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype и Xbox Live, размещенных в нашем глобальном облаке. инфраструктура с более чем 100 центрами обработки данных.</span><span class="sxs-lookup"><span data-stu-id="3375c-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="3375c-106">Как глобальная организация со значительным присутствием в Интернете и многими выразительноми свойствами Интернета, предоставляющими облачные службы, корпорация Майкрософт представляет собой большой общий целевой объект для хакеров и других вредоносных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3375c-106">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals.</span></span> <span data-ttu-id="3375c-107">Сеть — уровень взаимодействия между клиентами и Microsoft Cloud — одна из крупнейших целевых объектов вредоносных атак.</span><span class="sxs-lookup"><span data-stu-id="3375c-107">The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks.</span></span> <span data-ttu-id="3375c-108">На самом деле, в течение многих лет корпорация Майкрософт непрерывно и постоянна в некоторых формах сетевых цибераттакк.</span><span class="sxs-lookup"><span data-stu-id="3375c-108">In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack.</span></span> <span data-ttu-id="3375c-109">Практически все время, по крайней мере, одно из Интернет-свойств корпорации Майкрософт имеет некоторый вид атаки.</span><span class="sxs-lookup"><span data-stu-id="3375c-109">At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack.</span></span> <span data-ttu-id="3375c-110">Без надежных и постоянных систем защиты, которые могут защититься от этих атак, облачные службы Майкрософт будут отключены от сети и недоступны для пользователей.</span><span class="sxs-lookup"><span data-stu-id="3375c-110">Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="3375c-111">Корпорация Майкрософт использует принципы защиты от глубокой защиты для защиты облачных служб и сетей.</span><span class="sxs-lookup"><span data-stu-id="3375c-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="3375c-112">Определение и признаки атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="3375c-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="3375c-113">Один из способов атаки на сетевые службы состоит в том, чтобы создать большое количество запросов к узлам службы, чтобы перегрузить сеть и серверы для отказа от обслуживания легальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="3375c-113">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users.</span></span> <span data-ttu-id="3375c-114">Это называется атакой типа "отказ в обслуживании" (DoS).</span><span class="sxs-lookup"><span data-stu-id="3375c-114">This is referred to as a denial-of-service (DoS) attack.</span></span> <span data-ttu-id="3375c-115">Когда атака выполняется несколькими субъектами, конечными точками и/или векторами, она называется атакой с распределенным отказом в обслуживании (DDoS).</span><span class="sxs-lookup"><span data-stu-id="3375c-115">When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack.</span></span> <span data-ttu-id="3375c-116">Несмотря на то, что средства, мотивес и целевые объекты различаются, атаки DoS и DDoS обычно состоят из действий человека или пользователей, которые могут помешать нормальной или неопределенной работе Интернет-сайта или службы.</span><span class="sxs-lookup"><span data-stu-id="3375c-116">Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="3375c-117">[Группа "экстреннАя готовность компьютера" США](https://www.us-cert.gov/) (США-CERT) определяет признаки атак DOS:</span><span class="sxs-lookup"><span data-stu-id="3375c-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="3375c-118">Необычно низкая производительность сети (при открытии файлов или доступе к Интернет-сайтам)</span><span class="sxs-lookup"><span data-stu-id="3375c-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="3375c-119">Недоступность веб-сайта</span><span class="sxs-lookup"><span data-stu-id="3375c-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="3375c-120">Невозможность доступа к веб-сайту</span><span class="sxs-lookup"><span data-stu-id="3375c-120">Inability to access a Web site</span></span>
- <span data-ttu-id="3375c-121">Значительное увеличение получаемых нежелательных сообщений</span><span class="sxs-lookup"><span data-stu-id="3375c-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="3375c-122">Отключение беспроводного или беспроводного подключения к Интернету</span><span class="sxs-lookup"><span data-stu-id="3375c-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="3375c-123">Долгосрочный отказ в доступе к Интернету или Интернет-службам</span><span class="sxs-lookup"><span data-stu-id="3375c-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="3375c-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3375c-124">Related Topics</span></span>
- [<span data-ttu-id="3375c-125">Основные принципы защиты от атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="3375c-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="3375c-126">Стратегия защиты от атак типа "отказ в обслуживании" корпорации Майкрософт</span><span class="sxs-lookup"><span data-stu-id="3375c-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="3375c-127">Защита облачных служб Майкрософт от атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="3375c-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
