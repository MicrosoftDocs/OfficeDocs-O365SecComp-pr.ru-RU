---
title: Отображение аналитики правил потока обработки почты
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: 5/3/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
description: Администраторы могут узнать о медленных почтовых правилах в панели мониторинга "почтовые потоки" в центре безопасности & соответствия требованиям.
ms.openlocfilehash: 4477b388df321ee774ec7916a695cbfc69fc8e87
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598075"
---
# <a name="slow-mail-flow-rules-insight"></a><span data-ttu-id="e45b6-103">Отображение аналитики правил потока обработки почты</span><span class="sxs-lookup"><span data-stu-id="e45b6-103">Slow mail flow rules insight</span></span>

<span data-ttu-id="e45b6-104">Неэффективные правила для поток обработки почты (также называемые правилами транспорта) могут приводить к задержкам обработки почты для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e45b6-104">Inefficient mail flow rules (also known as transport rules) can lead to mail flow delays for your organization.</span></span> <span data-ttu-id="e45b6-105">Этот отчет содержит правила обработки почты, которые влияют на процесс обработки почты в Организации.</span><span class="sxs-lookup"><span data-stu-id="e45b6-105">This insight reports mail flow rules that have an impact on your organization's mail flow.</span></span> <span data-ttu-id="e45b6-106">Ниже приведены примеры этих типов правил.</span><span class="sxs-lookup"><span data-stu-id="e45b6-106">Examples of these types of rules are:</span></span>

- <span data-ttu-id="e45b6-107">Условия использования **— членство** в группах больших групп.</span><span class="sxs-lookup"><span data-stu-id="e45b6-107">Conditions that use **Is member of** for large groups.</span></span>

- <span data-ttu-id="e45b6-108">Условия, в которых используется сложное совпадение с шаблонами регулярных выражений (Regex).</span><span class="sxs-lookup"><span data-stu-id="e45b6-108">Conditions that use complex regular expression (regex) pattern matching.</span></span>

- <span data-ttu-id="e45b6-109">Условия, в которых используется проверка содержимого во вложениях.</span><span class="sxs-lookup"><span data-stu-id="e45b6-109">Conditions that use content checking in attachments.</span></span>

<span data-ttu-id="e45b6-110">Сведения, содержащиеся в этой справке, помогут вам определить и настроить правила обработки почтового ящика, чтобы снизить задержку обработки почты.</span><span class="sxs-lookup"><span data-stu-id="e45b6-110">The insight will help you to identify and fine-tune mail flow rules to help reduce mail flow delays.</span></span>

![Медленные правила почтовых ящиков в панели мониторинга почтовых ящиков в центре безопасности & соответствия требованиям](media/1dd90faa-f065-4b10-8b47-d35dc127fc26.png)

<span data-ttu-id="e45b6-112">При нажатии кнопки **Просмотреть сведения**отображается раскрывающаяся панель, в которой можно просмотреть правило.</span><span class="sxs-lookup"><span data-stu-id="e45b6-112">When you click **View details**, a flyout pane appears where you can review the rule.</span></span> <span data-ttu-id="e45b6-113">В раскрывающейся области можно также щелкнуть **Просмотр образцов сообщений** , чтобы узнать, какие типы сообщений влияют на это правило.</span><span class="sxs-lookup"><span data-stu-id="e45b6-113">In the flyout pane, can also click **view sample messages** to see what kind of messages are impacted by the rule.</span></span>

![Раскрывающаяся панель после нажатия кнопки Просмотреть сведения в разделе медленные почтовые ящики анализ правил в панели мониторинга почтового процесса](media/2cbd43b7-1f21-4338-a70c-7b50de5c69cd.png)

## <a name="see-also"></a><span data-ttu-id="e45b6-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e45b6-115">See also</span></span>

<span data-ttu-id="e45b6-116">Для получения дополнительных сведений о других аналитиках почтовых ящиков в панели мониторинга обработки почты ознакомьтесь с разрешениями почтовых ящиков [в центре безопасности & соответствия требованиям](mail-flow-insights.md).</span><span class="sxs-lookup"><span data-stu-id="e45b6-116">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights.md).</span></span>
