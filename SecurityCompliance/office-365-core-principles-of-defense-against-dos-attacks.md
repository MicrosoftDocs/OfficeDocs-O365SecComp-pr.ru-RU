---
title: Основные принципы защиты от атак типа "отказ в обслуживании" для Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Сведения о том, как корпорация Майкрософт использует основные принципы абсорптион, обнаружения и смягчения защиты от атак типа "отказ в обслуживании" (DoS).
ms.openlocfilehash: dfe179924f7414b0120697023f3daf7e6b6661b6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216009"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a><span data-ttu-id="3ad31-103">Основные принципы защиты от атак типа "отказ в обслуживании"</span><span class="sxs-lookup"><span data-stu-id="3ad31-103">Core Principles of Defense Against Denial-of-Service Attacks</span></span>

<span data-ttu-id="3ad31-p101">Три основных принципа защиты от сетевых атак DoS: Абсорптион, обнаружение и устранение. Абсорптион происходит перед обнаружением, а обнаружение происходит перед устранением. Абсорптион — это лучшая защита от атак DoS. Если атака не удается обнаружить, она не может быть снижена. Но если не удается придерживаться самой минимальной атаки DoS, службы не будут работать достаточно долго для обнаружения атаки.</span><span class="sxs-lookup"><span data-stu-id="3ad31-p101">The three core principles when defending against network-based DoS attacks are Absorption, Detection, and Mitigation. Absorption happens before detection, and detection happens before mitigation. Absorption is the best defense against a DoS attacks. If the attack can't be detected, it can't be mitigated. But if even the smallest DoS attack can't be absorbed, then services aren't going to survive long enough for the attack to be detected.</span></span>

<span data-ttu-id="3ad31-p102">Конечно, он обычно не економикалли для большинства организаций по приобретению избыточной емкости, необходимой для проведения атак DoS, так как это требует значительных капиталовложений в технологии и технические навыки. Это является одним из преимуществ для обеспечения безопасности при использовании облачных служб Майкрософт; такой масштаб услуг позволяет нам эффективно обеспечивать надежную защиту сети для наших облачных клиентов. Но даже в нашем масштабе по-прежнему должны быть баланс между абсорптион, обнаружением и снижением. Чтобы найти это сальдо, мы изучен темп роста атак для оценки того, сколько нам нужно.</span><span class="sxs-lookup"><span data-stu-id="3ad31-p102">Of course, it is generally not economically feasible for most organizations to purchase the excess capacity necessary to absorb DoS attacks, as this requires a considerable investment in technology and technical skills. This highlights one of the security benefits of using Microsoft cloud services; the sheer scale of our services enables us to provide strong network protection to our cloud customers in a cost-effective manner. But even at our scale, though, there must still be a balance between absorption, detection, and mitigation. To find that balance, we study an attack's growth rate to estimate how much we need to absorb.</span></span>

<span data-ttu-id="3ad31-p103">Обнаружение — это игра Cat-and-Mouse. Необходимо постоянно искать новые способы, с помощью которых люди могут атаковать вас и пытаться отменять системы. Обнаружение-_Гт_ смягчение-_Гт_ обнаружение-_Гт_ снижение и т. д. — это бессрочное постоянное состояние, которое будет продолжаться неограниченно.</span><span class="sxs-lookup"><span data-stu-id="3ad31-p103">Detection is a cat-and-mouse game. You must constantly look for the new ways people are attacking you or trying to defeat your systems. Detect -> Mitigate -> Detect -> Mitigate, etc., is a perpetual, persistent state that will continue indefinitely.</span></span>

## <a name="defending-against-dos-attacks"></a><span data-ttu-id="3ad31-116">Защита от атак DoS</span><span class="sxs-lookup"><span data-stu-id="3ad31-116">Defending Against DoS Attacks</span></span>

<span data-ttu-id="3ad31-p104">Чтобы успешно защититься от атак DoS, необходимо раннее обнаружение. Обнаруживая атаку до того, как система перегружена, защитник может выполнить план ответа.</span><span class="sxs-lookup"><span data-stu-id="3ad31-p104">To successfully defend against a DoS attack, early detection is essential. By detecting an attack before the system is overwhelmed, defenders can execute a response plan.</span></span>

<span data-ttu-id="3ad31-119">Приведенная ниже формула позволяет оценить время, влияющее на воздействие атак DoS:</span><span class="sxs-lookup"><span data-stu-id="3ad31-119">The following formula will help approximate the time to impact of a DoS attack:</span></span>

   <span data-ttu-id="3ad31-120">**Максимальная мощность (в байтах/с)/скорость роста (байт/сек) = время, влияющее на воздействие (байт/с)**</span><span class="sxs-lookup"><span data-stu-id="3ad31-120">**Maximum Capacity (in bytes/sec) / Growth Rate (in bytes/sec) = Time to Impact (in bytes/sec)**</span></span>

<span data-ttu-id="3ad31-p105">Если время ожидания истекает, то, скорее всего, атака на DoS будет успешной. Если время ожидания исправляется до начала действия, то службы, которые необходимо атаковать, должны быть доступны в сети и доступны, если используются стратегии устранения. Таким образом, для защиты от атак DoS можно выполнить только два действия.</span><span class="sxs-lookup"><span data-stu-id="3ad31-p105">If the time-to-detection occurs after time-to-impact, then it is likely the DoS attack will be successful. If the time-to-detection occurs before time-to-impact, then the services being attacked should remain online and accessible, if mitigation strategies are used. Thus, there are only two things that can be done to defend against DoS attacks:</span></span>
- <span data-ttu-id="3ad31-124">Увеличьте емкость, чтобы увеличить максимальный объем максимальной мощности (что, в свою очередь, больше времени на обнаружение атак); также</span><span class="sxs-lookup"><span data-stu-id="3ad31-124">Increase capacity to raise the ceiling of maximum capacity (which in turn provides more time to detect an attack); or</span></span>
- <span data-ttu-id="3ad31-125">Сократите время для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="3ad31-125">Decrease the time to detect.</span></span>

<span data-ttu-id="3ad31-p106">Повышение емкости имеет прямой финансовый эффект. Корпорация Майкрософт рекомендует, чтобы клиенты разработали по крайней мере базовую емкость абсорптион, чтобы они могли отдерживаться некоторого уровня атак DoS. Реальная мощность абсорптион варьируется от клиента к клиенту, так как у каждого клиента есть собственные пороговые значения для экспозиции, риска и финансовых аутлай. В конечном итоге, в случае экономических причин, в целях экономии времени на обнаружение обычно важна самая экономичная защита.</span><span class="sxs-lookup"><span data-stu-id="3ad31-p106">Increasing capacity has a direct fiscal impact. Microsoft recommends that customers develop at least basic absorption capacity, to ensure that they can survive some level of DoS attack. The actual absorption capacity will vary from customer to customer, as each customer has their own thresholds for exposure, risk, and financial outlay. Ultimately, for economic reasons, investments of research and time in ways to decrease time-to-detection are usually the most cost-effective defense.</span></span>
