---
title: Отображение аналитики правил потока обработки почты
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 5/3/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 37125cdb-715d-42d0-b669-1a8efa140813
description: Администраторы могут узнать о медленных правилах почтовых ящиков в панели мониторинга почтовых ящиков в центре безопасности Office 365 Security _Амп_.
ms.openlocfilehash: 8188ee0da15ac337499866783ca4f2d893062d5b
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454881"
---
# <a name="slow-mail-flow-rules-insight"></a><span data-ttu-id="0c509-103">Отображение аналитики правил потока обработки почты</span><span class="sxs-lookup"><span data-stu-id="0c509-103">Slow mail flow rules insight</span></span>

<span data-ttu-id="0c509-104">Неэффективные правила для поток обработки почты (также называемые правилами транспорта) могут приводить к задержкам обработки почты для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0c509-104">Inefficient mail flow rules (also known as transport rules) can lead to mail flow delays for your organization.</span></span> <span data-ttu-id="0c509-105">Этот отчет содержит правила обработки почты, которые влияют на процесс обработки почты в Организации.</span><span class="sxs-lookup"><span data-stu-id="0c509-105">This insight reports mail flow rules that have an impact on your organization's mail flow.</span></span> <span data-ttu-id="0c509-106">Ниже приведены примеры этих типов правил.</span><span class="sxs-lookup"><span data-stu-id="0c509-106">Examples of these types of rules are:</span></span>

- <span data-ttu-id="0c509-107">Условия использования **— членство** в группах больших групп.</span><span class="sxs-lookup"><span data-stu-id="0c509-107">Conditions that use **Is member of** for large groups.</span></span>

- <span data-ttu-id="0c509-108">Условия, в которых используется сложное совпадение с шаблонами регулярных выражений (Regex).</span><span class="sxs-lookup"><span data-stu-id="0c509-108">Conditions that use complex regular expression (regex) pattern matching.</span></span>

- <span data-ttu-id="0c509-109">Условия, в которых используется проверка содержимого во вложениях.</span><span class="sxs-lookup"><span data-stu-id="0c509-109">Conditions that use content checking in attachments.</span></span>

<span data-ttu-id="0c509-110">Сведения, содержащиеся в этой справке, помогут вам определить и настроить правила обработки почтового ящика, чтобы снизить задержку обработки почты.</span><span class="sxs-lookup"><span data-stu-id="0c509-110">The insight will help you to identify and fine-tune mail flow rules to help reduce mail flow delays.</span></span>

![Медленные правила почтовых ящиков в панели мониторинга почтовых ящиков в центре безопасности _Амп_ соответствия требованиям Office 365](media/1dd90faa-f065-4b10-8b47-d35dc127fc26.png)

<span data-ttu-id="0c509-112">При нажатии кнопки **Просмотреть сведения**отображается раскрывающаяся панель, в которой можно просмотреть правило.</span><span class="sxs-lookup"><span data-stu-id="0c509-112">When you click **View details**, a flyout pane appears where you can review the rule.</span></span> <span data-ttu-id="0c509-113">В раскрывающейся области можно также щелкнуть **Просмотр образцов сообщений** , чтобы узнать, какие типы сообщений влияют на это правило.</span><span class="sxs-lookup"><span data-stu-id="0c509-113">In the flyout pane, can also click **view sample messages** to see what kind of messages are impacted by the rule.</span></span>

![РасКрывающаяся панель после нажатия кнопки Просмотреть сведения в разделе медленные почтовые ящики анализ правил в панели мониторинга почтового процесса](media/2cbd43b7-1f21-4338-a70c-7b50de5c69cd.png)
