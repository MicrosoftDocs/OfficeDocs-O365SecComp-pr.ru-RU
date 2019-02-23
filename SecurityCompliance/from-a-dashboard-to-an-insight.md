---
title: Пошаговое руководство. Из панели мониторинга к аналитике
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 703c41df-b3e2-4e7e-9eeb-1a0b8d60fb56
description: Сведения о том, как можно переходить с панели мониторинга в представление о рекомендуемых действиях &amp; в центре безопасности и соответствия требованиям.
ms.openlocfilehash: 1c43d529d02872563bf6e1c9643b542ab6b8db9a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220529"
---
# <a name="walkthrough---from-a-dashboard-to-an-insight"></a><span data-ttu-id="cb77a-103">Пошаговое руководство. Из панели мониторинга к аналитике</span><span class="sxs-lookup"><span data-stu-id="cb77a-103">Walkthrough - From a dashboard to an insight</span></span>

<span data-ttu-id="cb77a-104">Если вы не знакомы с [отчетами и аналитическими сведениями в центре безопасности &amp; и соответствия требованиям Office 365](reports-and-insights-in-security-and-compliance.md), то можете понять, как легко переходить с панели мониторинга на подробные и рекомендуемые действия.</span><span class="sxs-lookup"><span data-stu-id="cb77a-104">If you're new to [reports and insights in the Office 365 Security &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md), it might help to see how you can easily navigate from a dashboard to an insight and recommended actions.</span></span> 
  
<span data-ttu-id="cb77a-p101">Это одно из нескольких пошаговых руководств для центра &amp; безопасности и соответствия требованиям. Дополнительные пошаговые руководства можно найти в разделе [связанные темы](#related-topics) .</span><span class="sxs-lookup"><span data-stu-id="cb77a-p101">This is one of several walkthroughs for the Security &amp; Compliance Center. To see additional walkthroughs, see the [Related topics](#related-topics) section.</span></span> 
  
## <a name="walkthrough-from-a-dashboard-to-an-insight"></a><span data-ttu-id="cb77a-107">ПоШаговое руководство: из панели мониторинга в представление</span><span class="sxs-lookup"><span data-stu-id="cb77a-107">Walkthrough: From a dashboard to an insight</span></span>

<span data-ttu-id="cb77a-p102">Давайте рассмотрим процесс передачи данных из панели мониторинга в отчет для анализа и действия. (Это краткий пример [](learn-about-spoof-intelligence.md) службы подделки.)</span><span class="sxs-lookup"><span data-stu-id="cb77a-p102">Let's walk through the flow from a dashboard to a report to an insight and action. (This is a brief [spoof intelligence](learn-about-spoof-intelligence.md) example.)</span></span> 
  
1. <span data-ttu-id="cb77a-p103">Мы начнем с панели мониторинга безопасности в [центре безопасности &amp; и соответствия требованиям](https://protection.office.com). (Перейдите на **панель мониторинга** **управления** \> угрозами.)</span><span class="sxs-lookup"><span data-stu-id="cb77a-p103">We begin with the Security dashboard in the [Security &amp; Compliance Center](https://protection.office.com). (Go to **Threat management** \> **Dashboard**.)</span></span><br><span data-ttu-id="cb77a-112">![В центре безопасности &amp; и соответствия требованиям выберите панель мониторинга \> управления угрозами](media/05a38660-eb13-4960-a266-11809c453d95.png)</span><span class="sxs-lookup"><span data-stu-id="cb77a-112">![In the Security &amp; Compliance Center, choose Threat management \> Dashboard](media/05a38660-eb13-4960-a266-11809c453d95.png)</span></span><br>
  
2. <span data-ttu-id="cb77a-p104">В строке **Insights** мы рассмотрели информацию о том, что нам нужно проверить некоторые домены, которые могут быть подозрительными. В строке **Insights** (сведения о домене) выберите пункт **пары доменов**.</span><span class="sxs-lookup"><span data-stu-id="cb77a-p104">In the **Insights** row, we notice an insight indicating we need to review some domains that might be suspicious. (In the **Insights** row, click **Domain pairs**.)</span></span><br><span data-ttu-id="cb77a-115">![В строке Insights упоминаются потенциальные проблемы подмены](media/dd1d0cb3-3201-45d7-b41d-18a0944fe85d.png)</span><span class="sxs-lookup"><span data-stu-id="cb77a-115">![The Insights row mentions potential spoofing concerns](media/dd1d0cb3-3201-45d7-b41d-18a0944fe85d.png)</span></span><br>
  
3. <span data-ttu-id="cb77a-p105">Мы получаем список действий, связанных с логикой подделки. Это экземпляры, в которых сообщения электронной почты отправляются так, как они поступили из нашей Организации, но на самом деле были отправлены из другой организации. Цель состоит в том, чтобы определить, авторизованы ли подложные сообщения.</span><span class="sxs-lookup"><span data-stu-id="cb77a-p105">We get a list of activities related to spoof intelligence. These are instances where email messages were sent that look like they came from our organization but were, in fact, sent from another organization. The goal is to determine whether the spoofed messages are authorized or not.</span></span><br><span data-ttu-id="cb77a-119">![Советы по подДелке](media/a2e2b4fd-0c1e-499f-8401-cf3089da82fa.png)</span><span class="sxs-lookup"><span data-stu-id="cb77a-119">![Spoof intelligence insights](media/a2e2b4fd-0c1e-499f-8401-cf3089da82fa.png)</span></span><br><span data-ttu-id="cb77a-p106">В этом списке можно отсортировать информацию по количеству сообщений, дате и времени последнего обнаружения поддельных сообщений. (Щелкните заголовки столбцов, например, **количество сообщений** или **Последнее** отображение, чтобы увидеть, как работает сортировка.)</span><span class="sxs-lookup"><span data-stu-id="cb77a-p106">In this list, we can sort the information by message count, date the spoofing was last detected, and more. (Click column headings, such as **Message count** or **Last seen** to see how sorting works.)</span></span> 
    
4. <span data-ttu-id="cb77a-p107">При выборе элемента в списке открывается область сведений, в которой можно увидеть дополнительные сведения, в том числе Похожие сообщения электронной почты, которые были обнаружены. (Щелкните элемент в списке и ознакомьтесь со сведениями и рекомендациями.)</span><span class="sxs-lookup"><span data-stu-id="cb77a-p107">Selecting an item in the list opens a details pane where we can see additional information, including similar email messages that were detected. (Click an item in the list, and review the information and recommendations.)</span></span><br>![При выборе элемента открывается область сведений](media/7ad1faa5-6ca2-474e-a609-eb275e0a8e59.png)<br>
  
5. <span data-ttu-id="cb77a-p108">Обратите внимание, что в верхней части области можно добавить отправителя в список разрешенных отправителей организации. (Не выбирайте **Добавить в список "алловедтоспуф" отправителя** , пока вы не подтвердите это. [Узнайте больше о логике подделки](learn-about-spoof-intelligence.md).)</span><span class="sxs-lookup"><span data-stu-id="cb77a-p108">Notice that at the top of the pane, we have the option to add the sender to our organization's allowed senders list. (Do not select **Add to 'AllowedtoSpoof' sender allow list** until you are sure you want to do this. [Learn more about spoof intelligence](learn-about-spoof-intelligence.md).)</span></span><br><span data-ttu-id="cb77a-128">![Вы можете авторизовать отправителя](media/caf0c20a-6047-486d-8060-5a229a3de49f.png)</span><span class="sxs-lookup"><span data-stu-id="cb77a-128">![You can authorize a sender](media/caf0c20a-6047-486d-8060-5a229a3de49f.png)</span></span>
  
<span data-ttu-id="cb77a-129">Таким образом, мы можем перейти с панели мониторинга к ценным и рекомендуемым действиям.</span><span class="sxs-lookup"><span data-stu-id="cb77a-129">In this way, we can move from a dashboard to insights and recommended actions.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="cb77a-130">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="cb77a-130">Related topics</span></span>

[<span data-ttu-id="cb77a-131">ПоШаговое руководство: из подробного отчета</span><span class="sxs-lookup"><span data-stu-id="cb77a-131">Walkthrough: From an insight to a detailed report</span></span>](from-an-insight-to-a-detailed-report.md)
  
[<span data-ttu-id="cb77a-132">ПоШаговое руководство: из подробного отчета в представление</span><span class="sxs-lookup"><span data-stu-id="cb77a-132">Walkthrough: From a detailed report to an insight</span></span>](from-a-detailed-report-to-an-insight.md)
  

