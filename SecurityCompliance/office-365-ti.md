---
title: Исследование угроз для Office 365 и ответ на них
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/09/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: Узнайте, как функции интеллектуального анализа в Office 365 Advanced Threat protection помогают находить угрозы в Организации, отвечать на вредоносные программы, фишингы и другие атаки, обнаруженные в Office 365 от вашего имени, и искать угрозу показател.
ms.openlocfilehash: 3d7bc40c4d5bec0c218adf093655cbbccde07ff9
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693508"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="5c0b0-103">Исследование угроз для Office 365 и ответ на них</span><span class="sxs-lookup"><span data-stu-id="5c0b0-103">Office 365 Threat Investigation and Response</span></span>

<span data-ttu-id="5c0b0-104">Исследование угроз и возможности реагирования в [Office 365 Advanced Threat protection](office-365-atp.md) помогают аналитикам безопасности и администраторам защищать пользователей Office 365 в Организации, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5c0b0-104">Threat investigation and response capabilities in [Office 365 Advanced Threat Protection](office-365-atp.md) help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="5c0b0-105">Упрощение распознавания, отслеживания и анализа атак</span><span class="sxs-lookup"><span data-stu-id="5c0b0-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="5c0b0-106">Помощь в быстром устранении угроз в Exchange Online, SharePoint Online, OneDrive для бизнеса и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5c0b0-106">Helping to quickly address threats in Exchange Online, SharePoint Online, OneDrive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="5c0b0-107">Предоставление ценных сведений и знаний для защиты от атак в Организации</span><span class="sxs-lookup"><span data-stu-id="5c0b0-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="5c0b0-108">Автоматическое исследование и ответ на критические угрозы электронной почты</span><span class="sxs-lookup"><span data-stu-id="5c0b0-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="5c0b0-109">**Office 365 Advanced Threat Protection и Threat расследования и ответ (ранее известного как office 365 Threat Intelligence) теперь являются office 365 Advanced Threat Protection Plan 2**, а также дополнительные возможности защиты от угроз, включенные в Некоторые подписки, такие как [microsoft 365 корпоративный](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 бизнес](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise и Office 365, образование A5 и т. д. Если в вашей организации есть подписка, не включающая в себя Office 365 ATP, вы можете приобрести ATP как надстройку.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-109">**Office 365 Advanced Threat Protection and Threat Investigation and Response (previously known as Office 365 Threat Intelligence) are now Office 365 Advanced Threat Protection Plan 2**, along with additional threat protection capabilities included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="5c0b0-110">Дополнительные сведения см. в статье [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="5c0b0-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="5c0b0-111">Что изменилось?</span><span class="sxs-lookup"><span data-stu-id="5c0b0-111">What's changing?</span></span>

<span data-ttu-id="5c0b0-112">Ранее в подписках на Office 365 включена логика защиты от угроз, например Office 365 корпоративный.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-112">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5.</span></span> <span data-ttu-id="5c0b0-113">По-прежнему существует ситуация, когда исследование угроз и возможности реагирования теперь входят в план 2 Office 365 Advanced Threat protection (план 2) (а также в Office 365 Enterprise ~).</span><span class="sxs-lookup"><span data-stu-id="5c0b0-113">This is still the case, as threat investigation and response capabilities are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="5c0b0-114">Кроме того, в качестве надстройки для клиентов Office 365 для бизнеса вы ранее приобрели систему анализа угроз для Office 365.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-114">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="5c0b0-115">Теперь эти возможности включены в Office 365 Advanced Threat Protection Plan 2 (вместе со всеми функциями в Office 365 Advanced Threat Protection Plan 1).</span><span class="sxs-lookup"><span data-stu-id="5c0b0-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (along with all the features in Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="5c0b0-116">Чтобы узнать больше, ознакомьтесь со статьями [Office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="5c0b0-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="5c0b0-117">Вот что это означает:</span><span class="sxs-lookup"><span data-stu-id="5c0b0-117">Here's what all this means:</span></span>

- <span data-ttu-id="5c0b0-118">**Если в вашей организации уже есть Office 365 корпоративный**, то у вас уже есть Advanced Threat protection (план 2), и это относится к расследованию угроз и возможностям реагирования.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-118">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span>

- <span data-ttu-id="5c0b0-119">**Если в вашей организации ранее имела значение office 365 Threat Intelligence (но не office 365 Advanced Threat protection) в качестве надстройки** к другой подписке на Office 365, теперь у вас будет Office 365 Advanced Threat Protection Plan 2, который включает Исследование угроз и возможности реагирования.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="5c0b0-120">**Если в Организации ранее было установлено приложение office 365 Advanced Threat protection (но не office 365 Threat Intelligence) в качестве надстройки** к другой подписке на Office 365, вы получите Office 365 Advanced Threat Protection Plan 1.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-120">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="5c0b0-121">В том числе Office 365 Advanced Threat protection (план 1) (но не для расследования угроз и возможностей реагирования).</span><span class="sxs-lookup"><span data-stu-id="5c0b0-121">This includes Office 365 Advanced Threat Protection Plan 1, (but not threat investigation and response capabilities).</span></span>

<span data-ttu-id="5c0b0-122">Дополнительные сведения см. в статье [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat protection Description Service](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span><span class="sxs-lookup"><span data-stu-id="5c0b0-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigation-and-response-capabilities"></a><span data-ttu-id="5c0b0-123">Начало работы с расследованиям угроз и возможностями реагирования</span><span class="sxs-lookup"><span data-stu-id="5c0b0-123">Get started with threat investigation and response capabilities</span></span>

<span data-ttu-id="5c0b0-124">Используйте следующие ресурсы для получения дополнительных сведений об расследовании угроз и возможностях реагирования в Office 365, а также о том, как использовать его для более безопасного хранения людей в Организации.</span><span class="sxs-lookup"><span data-stu-id="5c0b0-124">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="5c0b0-125">[Начало работы с расследованиям угроз и ответом](get-started-with-ti.md) (сюда входят сведения о необходимых ролях)</span><span class="sxs-lookup"><span data-stu-id="5c0b0-125">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="5c0b0-126">Сведения о средствах отслеживания угроз — новые и полезные</span><span class="sxs-lookup"><span data-stu-id="5c0b0-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="5c0b0-127">Поиск и исследование вредоносных сообщений электронной почты, которые были доставлены</span><span class="sxs-lookup"><span data-stu-id="5c0b0-127">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="5c0b0-128">Использование симулятора атак</span><span class="sxs-lookup"><span data-stu-id="5c0b0-128">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="5c0b0-129">Интеграция расследования угроз и ответа с помощью Advanced Threat Protection в Защитнике Windows</span><span class="sxs-lookup"><span data-stu-id="5c0b0-129">Integrate Threat Investigation and Response with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="5c0b0-130">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="5c0b0-130">Related topics</span></span>

[<span data-ttu-id="5c0b0-131">Защита от угроз в Office 365</span><span class="sxs-lookup"><span data-stu-id="5c0b0-131">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="5c0b0-132">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="5c0b0-132">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="5c0b0-133">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="5c0b0-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 
