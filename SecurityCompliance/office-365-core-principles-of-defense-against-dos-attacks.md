---
title: Office 365 основных принципов защиты от атак типа "отказ в обслуживании"
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Как корпорация Майкрософт использует основные принципы интеграцию, обнаружение и Устранение риска в его защиту от атак типа "отказ в обслуживании" (DoS).
ms.openlocfilehash: e313d5514e9bc493db78bebffca24a0fae4cbca7
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741102"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="c6c85-103">Основные принципы защиты от атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="c6c85-103">Core Principles of Defense Against Denial-of-Service Attacks</span></span>

<span data-ttu-id="c6c85-p101">Защита от DoS-атак сети территориально интеграцию, обнаружение и Устранение риска три основные принципы. Интеграцию происходит перед обнаружение и обнаружение происходит перед его устранение. Интеграцию — это лучший защиту от DoS-атак. Атака не может быть обнаружена, не могут быть уменьшены. Однако если не удается соль даже наименьшее DoS-атаки, служб не будем выдержать достаточным, атаки для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c6c85-p101">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation. Absorption happens before detection, and detection happens before mitigation. Absorption is the best defense against a DoS attacks. If the attack can't be detected, it can't be mitigated. But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="c6c85-p102">Конечно обычно это не экономически оправданным для большинства организаций на покупку лишние емкости необходимо выделить DoS-атак, как для этого необходимо значительные инвестиции в технологии и технические навыки. Это выделяет одним из преимуществ безопасности с помощью служб Microsoft cloud; оперировать масштаба наших услуг позволяет обеспечить защиту строгое сети клиентам облачных экономичным способом. Однако даже в нашем масштабе, должен существовать баланс между интеграцию, обнаружение и Устранение риска. Чтобы найти баланса, мы изучите атаки прирост чтобы оценить, насколько нам нужно выделить.</span><span class="sxs-lookup"><span data-stu-id="c6c85-p102">Of course, it is generally not economically feasible for most organizations to purchase the excess capacity necessary to absorb DoS attacks, as this requires a considerable investment in technology and technical skills. This highlights one of the security benefits of using Microsoft cloud services; the sheer scale of our services enables us to provide strong network protection to our cloud customers in a cost-effective manner. But even at our scale, though, there must still be a balance between absorption, detection, and mitigation. To find that balance, we study an attack's growth rate to estimate how much we need to absorb.</span></span>

<span data-ttu-id="c6c85-p103">Это является cat-and-mouse игру. Необходимо постоянно выглядеть для новых способов людей атаки вы или попытка обойти систем. Обнаружение - устранять > - обнаруживать > - > Mitigate, и др., представляет собой Бессрочная, сохраняемых состояние, продолжат неопределенное время.</span><span class="sxs-lookup"><span data-stu-id="c6c85-p103">Detection is a cat-and-mouse game. You must constantly look for the new ways people are attacking you or trying to defeat your systems. Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that will continue indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="c6c85-116">Защита от DoS-атак</span><span class="sxs-lookup"><span data-stu-id="c6c85-116">Defending Against DoS Attacks</span></span>

<span data-ttu-id="c6c85-p104">Для успешного защиты от DoS-атаки, важно раннего обнаружения. Перед перегружен система обнаруживает атака, защитники может выполнять плана действий.</span><span class="sxs-lookup"><span data-stu-id="c6c85-p104">To successfully defend against a DoS attack, early detection is essential. By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="c6c85-119">Следующая формула помогут приблизительное время влиять DoS-атаки:</span><span class="sxs-lookup"><span data-stu-id="c6c85-119">The following formula will help approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="c6c85-120">**Максимальной мощности (в байт/сек) аудио- и роста оценка (в байт/сек) = время воздействия (байт/сек)**</span><span class="sxs-lookup"><span data-stu-id="c6c85-120">**Maximum Capacity (in bytes/sec) / Growth Rate (in bytes/sec) = Time to Impact (in bytes/sec)**</span></span>

<span data-ttu-id="c6c85-p105">Если время к обнаружение возникает после времени для последствия, вероятно будет успешной DoS-атаки. Если время к обнаружение предшествует времени для воздействия, атаки служб должны оставаться online и доступны при использовании стратегии устранения. Таким образом существует только два следующих аспекта, которые можно выполнить для защиты от DoS-атак.</span><span class="sxs-lookup"><span data-stu-id="c6c85-p105">If the time-to-detection occurs after time-to-impact, then it is likely the DoS attack will be successful. If the time-to-detection occurs before time-to-impact, then the services being attacked should remain online and accessible, if mitigation strategies are used. Thus, there are only two things that can be done to defend against DoS attacks:</span></span>
- <span data-ttu-id="c6c85-124">Увеличение емкости для возведения потолок максимальной мощности (который в свою очередь, предоставляет больше времени для обнаружения атаки); или</span><span class="sxs-lookup"><span data-stu-id="c6c85-124">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="c6c85-125">Уменьшение времени для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c6c85-125">Decrease the time to detect.</span></span>

<span data-ttu-id="c6c85-p106">Увеличение емкости имеет непосредственно влияют финансовые. Корпорация Майкрософт рекомендует, что пользователи разрабатывать по крайней мере основные интеграцию емкость, чтобы убедиться, что они способное некоторые уровень DoS-атаки. Фактические интеграцию емкости зависит от клиента к другому, как каждый клиент имеет свои собственные пороговые значения для риск, риски и финансовые расходы. В конечном счете в целях экономии вклад в развитие справочных материалов и времени, в том, чтобы уменьшить время для обнаружения, как правило, наиболее экономичную защиту.</span><span class="sxs-lookup"><span data-stu-id="c6c85-p106">Increasing capacity has a direct fiscal impact. Microsoft recommends that customers develop at least basic absorption capacity, to ensure that they can survive some level of DoS attack. The actual absorption capacity will vary from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay. Ultimately, for economic reasons, investments of research and time in ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>
