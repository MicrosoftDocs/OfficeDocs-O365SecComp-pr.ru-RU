---
title: Защита от атак типа "отказ в обслуживании" в Office 365
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
description: Обзор отказ в обслуживании (DoS).
ms.openlocfilehash: b5a51ae332b32142d9ab993a29763b2160c3ce97
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534240"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="d8249-103">Защита от атак типа "отказ в обслуживании" в Office 365</span><span class="sxs-lookup"><span data-stu-id="d8249-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="d8249-104">Введение</span><span class="sxs-lookup"><span data-stu-id="d8249-104">Introduction</span></span>
<span data-ttu-id="d8249-105">Корпорация Майкрософт предоставляет надежности инфраструктуры для более чем 200 облачные службы, включая Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Скайп и Xbox Live, размещенных в нашей глобального облака Инфраструктура более 100 центров обработки данных.</span><span class="sxs-lookup"><span data-stu-id="d8249-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="d8249-p101">Как международной организации с значительные представление в сети Интернет и множество наиболее важные свойства Интернета, которые обеспечивают облачных служб Microsoft — это целевой больших, общие для злоумышленников и других злоумышленников. Сеть — уровень взаимодействия между клиентами и в облаке Майкрософт--— это один из крупнейших целевых значений от злонамеренных атак. На самом деле в течение многих лет Microsoft была непрерывно и постоянно в разделе некоторые формы на основе сети cyberattack. Почти все время по крайней мере один из свойства Интернета корпорации Майкрософт возникают некоторые формы атаки. Без надежных и сохраняемого смягчение систем, обеспечить защиту от этих атак корпорации Майкрософт облачной службы будет становится недоступной для клиентов и в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="d8249-p101">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals. The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks. In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack. At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack. Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="d8249-111">Корпорация Майкрософт использует принципы безопасности в глубокой защиты его облачных служб и сетей.</span><span class="sxs-lookup"><span data-stu-id="d8249-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="d8249-112">Определение и признаки атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="d8249-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="d8249-p102">Одним из способов атак сетевые службы является создание много запросов от службы узлов в перегрузке сети и серверы для запрета службы законным пользователям. Это называется атака типа "отказ в обслуживании" (DoS). При выполнении атаки с несколькими субъектами, конечные точки и/или векторов она называется распределенных атак типа "отказ в обслуживании" (DDoS). Несмотря на то, что означает, что, motives и целевые значения отличаются, атаки DoS и DDoS обычно состоят из усилия контактного лица или лиц, чтобы предотвратить веб-сайтом или служба работает правильно, а все, временно или неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="d8249-p102">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users. This is referred to as a denial-of-service (DoS) attack. When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack. Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="d8249-117">[Группы подготовки аварийного компьютер США](https://www.us-cert.gov/) (US-CERT) определяет признаки DoS-атак для включения:</span><span class="sxs-lookup"><span data-stu-id="d8249-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="d8249-118">Слишком снижение производительности сети (при открытии файлов или получение доступа к веб-сайтов)</span><span class="sxs-lookup"><span data-stu-id="d8249-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="d8249-119">Недоступность веб-сайта</span><span class="sxs-lookup"><span data-stu-id="d8249-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="d8249-120">Не удается получить доступ к веб-сайта</span><span class="sxs-lookup"><span data-stu-id="d8249-120">Inability to access a Web site</span></span>
- <span data-ttu-id="d8249-121">Значительное увеличение полученная Нежелательная почта</span><span class="sxs-lookup"><span data-stu-id="d8249-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="d8249-122">Отключение беспроводной или проводной подключение к Интернету</span><span class="sxs-lookup"><span data-stu-id="d8249-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="d8249-123">Долгосрочные потери доступа к веб-сайта или служб Интернета</span><span class="sxs-lookup"><span data-stu-id="d8249-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8249-124">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d8249-124">Related Topics</span></span>
- [<span data-ttu-id="d8249-125">Основные принципы защиты от атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="d8249-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="d8249-126">Стратегия защиты типа "отказ в обслуживании" корпорации Майкрософт</span><span class="sxs-lookup"><span data-stu-id="d8249-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="d8249-127">Защита облачные службы Майкрософт от атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="d8249-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
