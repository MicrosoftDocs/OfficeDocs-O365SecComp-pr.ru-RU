---
title: Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
description: Узнайте, как возможности аналитики угроз в расширенного защиту от угроз, которые помогут исследование угрозы, связанные с вашей организацией, реагировать на вредоносные программы, фишинга и других атак, обнаруженных в Office 365 от вашего имени и поиск индикаторы угроз.
ms.openlocfilehash: 5dfd0377c4cafe89c5f69ea080f07d04d892329e
ms.sourcegitcommit: c1c41744c2de89c9e172f817c8f73bb0ada81a58
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2019
ms.locfileid: "29792264"
---
# <a name="office-365-threat-intelligence"></a><span data-ttu-id="afc88-103">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="afc88-103">Office 365 Threat Intelligence</span></span>

<span data-ttu-id="afc88-104">Возможности аналитики угроз в защиту от угроз для Office 365 расширенного помочь аналитикам безопасности и Администраторы защитить пользователей Office 365 своей организации с:</span><span class="sxs-lookup"><span data-stu-id="afc88-104">Threat intelligence capabilities in Office 365 Advanced Threat Protection help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="afc88-105">Что позволяет легко определить, контроля и понять атаки</span><span class="sxs-lookup"><span data-stu-id="afc88-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="afc88-106">Как помочь быстро угрозы в Exchange Online и SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="afc88-106">Helping to quickly address threats in Exchange Online and SharePoint Online</span></span>
    
3. <span data-ttu-id="afc88-107">Предоставление обмена мнениями и знания для предотвращения атак на своей организации</span><span class="sxs-lookup"><span data-stu-id="afc88-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="afc88-p101">**Анализ угроз является частью теперь в Office 365 расширенного угроз защиты (план 2)**, который является включены в в определенных подписки, например [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [365 Microsoft Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, и т.д. Если в вашей организации есть подписка, которая не включает Office 365 ATP, вы можете приобрести ATP потенциально как дополнительный компонент. Для получения дополнительных сведений см [защиту от угроз для Office 365 Дополнительные планы и ценах](https://products.office.com/exchange/advance-threat-protection) и [Office 365 расширенного угроз защиты описание службы](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="afc88-p101">**Threat Intelligence is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="afc88-110">Что происходит изменение?</span><span class="sxs-lookup"><span data-stu-id="afc88-110">What's changing?</span></span>

<span data-ttu-id="afc88-p102">Ранее анализ угроз Office 365 была включена в подписки, такие как Office 365 корпоративный E5. Это по-прежнему так, несмотря на то, что анализ угроз функции теперь входят в состав Office 365 расширенного угроз защиты (план 2) (и оно будет указано в Office 365 корпоративный E5).</span><span class="sxs-lookup"><span data-stu-id="afc88-p102">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5. This is still the case, although Threat Intelligence features are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="afc88-p103">Кроме того анализ угроз Office 365 был ранее можно приобрести в качестве надстройки для Office 365 для предприятий. Теперь анализ угроз включен в Office 365 расширенного угроз защиты (план 2). Для получения дополнительных сведений см [защиту от угроз для Office 365 Дополнительные планы и ценах](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="afc88-p103">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers. Now, Threat Intelligence is included in Office 365 Advanced Threat Protection Plan 2. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="afc88-116">Вот, что все это означает, что:</span><span class="sxs-lookup"><span data-stu-id="afc88-116">Here's what all this means:</span></span>

- <span data-ttu-id="afc88-117">**Если в организации уже существует Office 365 Enterprise E5**, а затем вы уже есть дополнительные угроз защиты (план 2), а это включает возможности анализ угроз.</span><span class="sxs-lookup"><span data-stu-id="afc88-117">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes Threat Intelligence capabilities.</span></span>

- <span data-ttu-id="afc88-p104">**Если ваша организация ранее находилась анализ угроз Office 365 (но не Office 365 расширенного защиту от угроз) как дополнительный компонент** другой подписки Office 365, после чего вам будет иметь Office 365 расширенного угроз защиты (план 2). Этот компонент включает возможности расширенного защиту от угроз и анализ угроз.</span><span class="sxs-lookup"><span data-stu-id="afc88-p104">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 2. This includes Advanced Threat Protection and Threat Intelligence capabilities.</span></span> 

- <span data-ttu-id="afc88-p105">**Если ваша организация ранее находилась защиту от угроз для Office 365 Advanced (но не Office 365 Threat аналитики) как дополнительный компонент** другой подписки Office 365, после чего вам будет иметь Office 365 расширенного угроз защиты план 1. Это включает в себя дополнительные защиту от угроз (но не анализ угроз возможности).</span><span class="sxs-lookup"><span data-stu-id="afc88-p105">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1. This includes Advanced Threat Protection (but not Threat Intelligence capabilities).</span></span>

<span data-ttu-id="afc88-122">Для получения дополнительных сведений см [защиту от угроз для Office 365 Дополнительные планы и ценах](https://products.office.com/exchange/advance-threat-protection) и [Office 365 расширенного угроз защиты описание службы](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span><span class="sxs-lookup"><span data-stu-id="afc88-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-intelligence-capabilities"></a><span data-ttu-id="afc88-123">Начало работы с возможностями аналитики угроз</span><span class="sxs-lookup"><span data-stu-id="afc88-123">Get started with threat intelligence capabilities</span></span>

<span data-ttu-id="afc88-124">Используйте следующие ресурсы, чтобы узнать больше о анализ угроз и как его использовать для хранения людей в организации.</span><span class="sxs-lookup"><span data-stu-id="afc88-124">Use the following resources to learn more about threat intelligence, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="afc88-125">[Начало работы с анализ угроз](get-started-with-ti.md) (Это включает сведения о необходимых ролей)</span><span class="sxs-lookup"><span data-stu-id="afc88-125">[Get started with Threat Intelligence](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="afc88-126">Узнайте о системы отслеживания дефектов угроз - новости и полезные сведения</span><span class="sxs-lookup"><span data-stu-id="afc88-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="afc88-127">Поиск и исследовать вредоносных электронной почты, которое было доставлено</span><span class="sxs-lookup"><span data-stu-id="afc88-127">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="afc88-128">Используйте имитатора атаки</span><span class="sxs-lookup"><span data-stu-id="afc88-128">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="afc88-129">Интеграция с Защитник Windows Advanced защиту от угроз анализ угроз</span><span class="sxs-lookup"><span data-stu-id="afc88-129">Integrate Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="afc88-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="afc88-130">Related topics</span></span>

[<span data-ttu-id="afc88-131">Защита от угроз в Office 365</span><span class="sxs-lookup"><span data-stu-id="afc88-131">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="afc88-132">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="afc88-132">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="afc88-133">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="afc88-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

