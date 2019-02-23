---
title: Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection: M365-security-compliance
description: Узнайте, как функции интеллектуального анализа угроз в Advanced Threat protection помогают находить угрозы в Организации, отвечать на вредоносные программы, фишингы и другие атаки, обнаруженные в Office 365 от вашего имени, и искать индикаторы угроз.
ms.openlocfilehash: a55a17bae141c394ba01e1526615c5c1687340a2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216559"
---
# <a name="office-365-threat-intelligence"></a><span data-ttu-id="e5024-103">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="e5024-103">Office 365 Threat Intelligence</span></span>

<span data-ttu-id="e5024-104">Возможности системы анализа угроз в Office 365 Advanced Threat protection помогают аналитикам и администраторам защищать пользователей Office 365, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e5024-104">Threat intelligence capabilities in Office 365 Advanced Threat Protection help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="e5024-105">Упрощение распознавания, отслеживания и анализа атак</span><span class="sxs-lookup"><span data-stu-id="e5024-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="e5024-106">Помощь в быстром устранении угроз в Exchange Online и SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="e5024-106">Helping to quickly address threats in Exchange Online and SharePoint Online</span></span>
    
3. <span data-ttu-id="e5024-107">Предоставление ценных сведений и знаний для защиты от атак в Организации</span><span class="sxs-lookup"><span data-stu-id="e5024-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="e5024-p101">**В office 365 Advanced Threat protection (план 2**), включенный в некоторые подписки, такие как [Microsoft 365 корпоративный](https://www.microsoft.com/microsoft-365/enterprise/home), [microsoft 365 бизнес](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise, Office 365 Образование A5 и т. д. Если в вашей организации есть подписка, не включающая в себя Office 365 ATP, вы можете приобрести ATP как надстройку. Дополнительные сведения см. в статье [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="e5024-p101">**Threat Intelligence is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="e5024-110">Что изменилось?</span><span class="sxs-lookup"><span data-stu-id="e5024-110">What's changing?</span></span>

<span data-ttu-id="e5024-p102">Ранее в подписках на Office 365 включена логика защиты от угроз, например Office 365 корпоративный. Это по-прежнему относится, несмотря на то что функции системы анализа угроз включены в Office 365 Advanced Threat protection (план 2) (а также включены в Office 365 корпоративный ~).</span><span class="sxs-lookup"><span data-stu-id="e5024-p102">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5. This is still the case, although Threat Intelligence features are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="e5024-p103">Кроме того, в качестве надстройки для клиентов Office 365 для бизнеса вы ранее приобрели систему анализа угроз для Office 365. Теперь логика угроз включена в Office 365 Advanced Threat Protection Plan 2. Чтобы узнать больше, ознакомьтесь со статьями [Office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="e5024-p103">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers. Now, Threat Intelligence is included in Office 365 Advanced Threat Protection Plan 2. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="e5024-116">Вот что это означает:</span><span class="sxs-lookup"><span data-stu-id="e5024-116">Here's what all this means:</span></span>

- <span data-ttu-id="e5024-117">**Если в вашей организации уже есть Office 365 корпоративный**, то у вас уже есть Advanced Threat protection (план 2), и это включает возможности системы анализа угроз.</span><span class="sxs-lookup"><span data-stu-id="e5024-117">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes Threat Intelligence capabilities.</span></span>

- <span data-ttu-id="e5024-p104">**Если в Организации ранее имела значение office 365 Threat Intelligence (но не office 365 Advanced Threat protection) в качестве надстройки** к другой подписке на Office 365, вы получите Office 365 Advanced Threat Protection Plan 2. Это включает в себя расширенные возможности защиты от угроз и системы анализа угроз.</span><span class="sxs-lookup"><span data-stu-id="e5024-p104">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 2. This includes Advanced Threat Protection and Threat Intelligence capabilities.</span></span> 

- <span data-ttu-id="e5024-p105">**Если в Организации ранее было установлено приложение office 365 Advanced Threat protection (но не office 365 Threat Intelligence) в качестве надстройки** к другой подписке на Office 365, вы получите Office 365 Advanced Threat Protection Plan 1. Это включает в себя расширенные возможности защиты от угроз (но не возможности системы аналитики).</span><span class="sxs-lookup"><span data-stu-id="e5024-p105">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1. This includes Advanced Threat Protection (but not Threat Intelligence capabilities).</span></span>

<span data-ttu-id="e5024-122">Дополнительные сведения см. в статье [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat protection Description Service](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span><span class="sxs-lookup"><span data-stu-id="e5024-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-intelligence-capabilities"></a><span data-ttu-id="e5024-123">Начало работы с возможностями аналитики угроз</span><span class="sxs-lookup"><span data-stu-id="e5024-123">Get started with threat intelligence capabilities</span></span>

<span data-ttu-id="e5024-124">Используйте указанные ниже ресурсы, чтобы узнать больше об управлении угрозами, а также о том, как использовать его для более безопасного хранения людей в Организации.</span><span class="sxs-lookup"><span data-stu-id="e5024-124">Use the following resources to learn more about threat intelligence, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="e5024-125">[Начало работы с логикой операций с угрозами](get-started-with-ti.md) (сюда входят сведения о необходимых ролях)</span><span class="sxs-lookup"><span data-stu-id="e5024-125">[Get started with Threat Intelligence](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="e5024-126">Сведения о средствах отслеживания угроз — новые и полезные</span><span class="sxs-lookup"><span data-stu-id="e5024-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="e5024-127">Поиск и исследование вредоносных сообщений электронной почты, которые были доставлены</span><span class="sxs-lookup"><span data-stu-id="e5024-127">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="e5024-128">Использование симулятора атак</span><span class="sxs-lookup"><span data-stu-id="e5024-128">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="e5024-129">Интеграция Threat Intelligence с Advanced Threat Protection в Защитнике Windows</span><span class="sxs-lookup"><span data-stu-id="e5024-129">Integrate Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="e5024-130">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="e5024-130">Related topics</span></span>

[<span data-ttu-id="e5024-131">Защита от угроз в Office 365</span><span class="sxs-lookup"><span data-stu-id="e5024-131">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="e5024-132">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e5024-132">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="e5024-133">Разрешения в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="e5024-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

