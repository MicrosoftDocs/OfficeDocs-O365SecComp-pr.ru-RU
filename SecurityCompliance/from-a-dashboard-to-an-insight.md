---
title: Пошаговое руководство. Из панели мониторинга к аналитике
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 703c41df-b3e2-4e7e-9eeb-1a0b8d60fb56
description: Узнайте, как можно перейти из панели мониторинга знаниями с рекомендованные действия в системы &amp; центре соответствия требованиям.
ms.openlocfilehash: 933bf6e86bc1ddce9259d071b69654f68e4dd370
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706153"
---
# <a name="walkthrough---from-a-dashboard-to-an-insight"></a><span data-ttu-id="7ccfc-103">Пошаговое руководство. Из панели мониторинга к аналитике</span><span class="sxs-lookup"><span data-stu-id="7ccfc-103">Walkthrough - From a dashboard to an insight</span></span>

<span data-ttu-id="7ccfc-104">Если вы не знакомы с [отчетов и полезные сведения о безопасности Office 365 &amp; центре соответствия требованиям](reports-and-insights-in-security-and-compliance.md), он может помочь чтобы увидеть, как можно легко перейти из панели мониторинга к знаниями и рекомендуемые действия.</span><span class="sxs-lookup"><span data-stu-id="7ccfc-104">If you're new to [reports and insights in the Office 365 Security &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md), it might help to see how you can easily navigate from a dashboard to an insight and recommended actions.</span></span> 
  
<span data-ttu-id="7ccfc-p101">Это один из несколько пошаговых руководств для системы безопасности &amp; центре соответствия требованиям. Чтобы просмотреть Дополнительные пошаговые руководства, в разделе [связанные темы](#related-topics) .</span><span class="sxs-lookup"><span data-stu-id="7ccfc-p101">This is one of several walkthroughs for the Security &amp; Compliance Center. To see additional walkthroughs, see the [Related topics](#related-topics) section.</span></span> 
  
## <a name="walkthrough-from-a-dashboard-to-an-insight"></a><span data-ttu-id="7ccfc-107">Пошаговое руководство: из панели мониторинга для знаниями</span><span class="sxs-lookup"><span data-stu-id="7ccfc-107">Walkthrough: From a dashboard to an insight</span></span>

<span data-ttu-id="7ccfc-p102">Рассмотрим поток из панели мониторинга с отчетом, чтобы анализировать и действия. (Это пример краткое [Подделка аналитики](learn-about-spoof-intelligence.md) ).</span><span class="sxs-lookup"><span data-stu-id="7ccfc-p102">Let's walk through the flow from a dashboard to a report to an insight and action. (This is a brief [spoof intelligence](learn-about-spoof-intelligence.md) example.)</span></span> 
  
1. <span data-ttu-id="7ccfc-p103">Мы начнем с помощью панели мониторинга безопасности в [безопасности &amp; центре соответствия требованиям](https://security.microsoft.com). (Перейдите на страницу **управления угроз** \> **панели мониторинга**.)</span><span class="sxs-lookup"><span data-stu-id="7ccfc-p103">We begin with the Security dashboard in the [Security &amp; Compliance Center](https://security.microsoft.com). (Go to **Threat management** \> **Dashboard**.)</span></span>
    
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите Threat management \> панели мониторинга](media/05a38660-eb13-4960-a266-11809c453d95.png)
  
2. <span data-ttu-id="7ccfc-p104">В строке **полезные сведения о** мы Обратите внимание на то подробности о том, что нужно проверить несколько доменов, которые могут быть подозрительные. (В строке **полезные сведения о** щелкните **пары "домен"**).</span><span class="sxs-lookup"><span data-stu-id="7ccfc-p104">In the **Insights** row, we notice an insight indicating we need to review some domains that might be suspicious. (In the **Insights** row, click **Domain pairs**.)</span></span>
    
    ![Полезные сведения о строке упоминания потенциальных проблем спуфинга](media/dd1d0cb3-3201-45d7-b41d-18a0944fe85d.png)
  
3. <span data-ttu-id="7ccfc-p105">Мы получить список действий, связанных с подменить аналитики. Это экземпляры, где были отправлены сообщения электронной почты, выглядящие как поступил от организации, но на самом деле, отправленные из другой организации. Цель — определить, разрешено ли подложный сообщения или нет.</span><span class="sxs-lookup"><span data-stu-id="7ccfc-p105">We get a list of activities related to spoof intelligence. These are instances where email messages were sent that look like they came from our organization but were, in fact, sent from another organization. The goal is to determine whether the spoofed messages are authorized or not.</span></span>
    
    ![Полезные сведения о подделка аналитике](media/a2e2b4fd-0c1e-499f-8401-cf3089da82fa.png)
  
    <span data-ttu-id="7ccfc-p106">В этом списке мы сортировки информации, количество сообщений, спуфинг обнаружена последняя дата и др. (Щелкните заголовки столбцов, таких как **число сообщений** или **Последнее обнаружение** , чтобы узнать, как сортировки works).</span><span class="sxs-lookup"><span data-stu-id="7ccfc-p106">In this list, we can sort the information by message count, date the spoofing was last detected, and more. (Click column headings, such as **Message count** or **Last seen** to see how sorting works.)</span></span> 
    
4. <span data-ttu-id="7ccfc-p107">Выбор элемента в списке откроется область сведений, где можно увидеть дополнительные сведения, в том числе аналогичные сообщений электронной почты, обнаруженные. (Щелкните элемент в списке и просмотрите сведения и рекомендации).</span><span class="sxs-lookup"><span data-stu-id="7ccfc-p107">Selecting an item in the list opens a details pane where we can see additional information, including similar email messages that were detected. (Click an item in the list, and review the information and recommendations.)</span></span>
    
    ![При выборе элемента откроется область сведений](media/7ad1faa5-6ca2-474e-a609-eb275e0a8e59.png)
  
5. <span data-ttu-id="7ccfc-p108">Обратите внимание на то, что в верхней области, у нас есть параметр, чтобы добавить отправителя в список разрешенных отправителей вашей организации. (Не устанавливайте флажок **Добавить, чтобы отправителя «AllowedtoSpoof» белый список** до убедитесь, что вы хотите сделать это. [Дополнительные сведения о аналитики подделка](learn-about-spoof-intelligence.md).)</span><span class="sxs-lookup"><span data-stu-id="7ccfc-p108">Notice that at the top of the pane, we have the option to add the sender to our organization's allowed senders list. (Do not select **Add to 'AllowedtoSpoof' sender allow list** until you are sure you want to do this. [Learn more about spoof intelligence](learn-about-spoof-intelligence.md).)</span></span>
    
    ![Можно разрешить отправителя](media/caf0c20a-6047-486d-8060-5a229a3de49f.png)
  
<span data-ttu-id="7ccfc-129">Таким образом можно переместить из панели мониторинга в средствами и рекомендуемые действия.</span><span class="sxs-lookup"><span data-stu-id="7ccfc-129">In this way, we can move from a dashboard to insights and recommended actions.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="7ccfc-130">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="7ccfc-130">Related topics</span></span>

[<span data-ttu-id="7ccfc-131">Пошаговое руководство: из insight для подробного отчета</span><span class="sxs-lookup"><span data-stu-id="7ccfc-131">Walkthrough: From an insight to a detailed report</span></span>](from-an-insight-to-a-detailed-report.md)
  
[<span data-ttu-id="7ccfc-132">Пошаговое руководство: из подробного отчета для знаниями</span><span class="sxs-lookup"><span data-stu-id="7ccfc-132">Walkthrough: From a detailed report to an insight</span></span>](from-a-detailed-report-to-an-insight.md)
  

