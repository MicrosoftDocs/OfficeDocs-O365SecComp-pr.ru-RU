---
title: Office 365 основных принципов защиты от атак типа "отказ в обслуживании"
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
description: Как корпорация Майкрософт использует основные принципы интеграцию, обнаружение и Устранение риска в его защиту от атак типа "отказ в обслуживании" (DoS).
ms.openlocfilehash: 8355a7897c788241092363a23e198423e81c587a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534242"
---
# <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Основные принципы защиты от атак типа "отказ в обслуживании"
Защита от DoS-атак сети территориально интеграцию, обнаружение и Устранение риска три основные принципы. Интеграцию происходит перед обнаружение и обнаружение происходит перед его устранение. Интеграцию — это лучший защиту от DoS-атак. Атака не может быть обнаружена, не могут быть уменьшены. Однако если не удается соль даже наименьшее DoS-атаки, служб не будем выдержать достаточным, атаки для обнаружения.

Конечно обычно это не экономически оправданным для большинства организаций на покупку лишние емкости необходимо выделить DoS-атак, как для этого необходимо значительные инвестиции в технологии и технические навыки. Это выделяет одним из преимуществ безопасности с помощью служб Microsoft cloud; оперировать масштаба наших услуг позволяет обеспечить защиту строгое сети клиентам облачных экономичным способом. Однако даже в нашем масштабе, должен существовать баланс между интеграцию, обнаружение и Устранение риска. Чтобы найти баланса, мы изучите атаки прирост чтобы оценить, насколько нам нужно выделить.

Это является cat-and-mouse игру. Необходимо постоянно выглядеть для новых способов людей атаки вы или попытка обойти систем. Найти -> Mitigate -> найти -> Mitigate, и др., представляет собой Бессрочная сохраняемого состояние, которое будет предоставляться неопределенное время.

## <a name="defending-against-dos-attacks"></a>Защита от DoS-атак
Для успешного защиты от DoS-атаки, важно раннего обнаружения. Перед перегружен система обнаруживает атака, защитники может выполнять плана действий.

Следующая формула помогут приблизительное время влиять DoS-атаки:

   **Максимальной мощности аудио- и (получил роста максимальной мощности X) = время влияния**

Если время к обнаружение возникает после времени для последствия, вероятно будет успешной DoS-атаки. Если время к обнаружение предшествует времени для воздействия, атаки служб должны оставаться online и доступны при использовании стратегии устранения. Таким образом существует только два следующих аспекта, которые можно выполнить для защиты от DoS-атак.
- Увеличение емкости для возведения потолок максимальной мощности (который в свою очередь, предоставляет больше времени для обнаружения атаки); или
- Уменьшение времени для обнаружения.

Увеличение емкости имеет непосредственно влияют финансовые. Корпорация Майкрософт рекомендует, что пользователи разрабатывать по крайней мере основные интеграцию емкость, чтобы убедиться, что они способное некоторые уровень DoS-атаки. Фактические интеграцию емкости зависит от клиента к другому, как каждый клиент имеет свои собственные пороговые значения для риск, риски и финансовые расходы. В конечном счете в целях экономии вклад в развитие справочных материалов и времени, в том, чтобы уменьшить время для обнаружения, как правило, наиболее экономичную защиту.