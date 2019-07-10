---
title: Анализ угроз и реагирование на них в Office 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 03/18/2019
audience: Admin
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
ms.openlocfilehash: 7e0ce37b33ea2c019005585fd70107145fbfc8aa
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598085"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="955cb-103">Анализ угроз и реагирование на них в Office 365</span><span class="sxs-lookup"><span data-stu-id="955cb-103">Office 365 threat investigation and response</span></span>

<span data-ttu-id="955cb-104">Исследование угроз и возможности реагирования в [Office 365 Advanced Threat protection](office-365-atp.md) помогают аналитикам безопасности и администраторам защищать пользователей Office 365 в Организации, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="955cb-104">Threat investigation and response capabilities in [Office 365 Advanced Threat Protection](office-365-atp.md) help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="955cb-105">Упрощение распознавания, отслеживания и анализа атак</span><span class="sxs-lookup"><span data-stu-id="955cb-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="955cb-106">Помощь в быстром устранении угроз в Exchange Online, SharePoint Online, OneDrive для бизнеса и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="955cb-106">Helping to quickly address threats in Exchange Online, SharePoint Online, OneDrive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="955cb-107">Предоставление ценных сведений и знаний для защиты от атак в Организации</span><span class="sxs-lookup"><span data-stu-id="955cb-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="955cb-108">Автоматическое исследование и ответ на критические угрозы электронной почты</span><span class="sxs-lookup"><span data-stu-id="955cb-108">Automated investigation and response for critical email based threats</span></span>
    
 
## <a name="whats-changing"></a><span data-ttu-id="955cb-109">Что изменилось?</span><span class="sxs-lookup"><span data-stu-id="955cb-109">What's changing?</span></span>

<span data-ttu-id="955cb-110">Ранее в подписках на Office 365 включена логика угроз Office, например Office 365 в.</span><span class="sxs-lookup"><span data-stu-id="955cb-110">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 E5.</span></span> <span data-ttu-id="955cb-111">По-прежнему существует ситуация, когда исследование угроз и возможности реагирования теперь входят в план 2 Office 365 Advanced Threat protection (план 2) (и это относится к Office 365 "+ 1").</span><span class="sxs-lookup"><span data-stu-id="955cb-111">This is still the case, as threat investigation and response capabilities are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 E5).</span></span> 

<span data-ttu-id="955cb-112">Кроме того, в качестве надстройки для клиентов Office 365 для бизнеса вы ранее приобрели систему анализа угроз для Office 365.</span><span class="sxs-lookup"><span data-stu-id="955cb-112">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="955cb-113">Теперь эти возможности включены в Office 365 Advanced Threat Protection Plan 2 (вместе со всеми функциями в Office 365 Advanced Threat Protection Plan 1).</span><span class="sxs-lookup"><span data-stu-id="955cb-113">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (along with all the features in Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="955cb-114">Чтобы узнать больше, ознакомьтесь со статьями [Office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="955cb-114">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="955cb-115">Вот что это означает:</span><span class="sxs-lookup"><span data-stu-id="955cb-115">Here's what all this means:</span></span>

- <span data-ttu-id="955cb-116">**Если в вашей организации уже есть Office 365**, то у вас уже есть Advanced Threat protection (план 2), и это относится к расследованию угроз и возможностям реагирования.</span><span class="sxs-lookup"><span data-stu-id="955cb-116">**If your organization already has Office 365 E5**, then you already have Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span>

- <span data-ttu-id="955cb-117">**Если в вашей организации ранее имела значение office 365 Threat Intelligence (но не office 365 Advanced Threat protection) в качестве надстройки** к другой подписке на Office 365, теперь у вас будет Office 365 Advanced Threat Protection Plan 2, который включает Исследование угроз и возможности реагирования.</span><span class="sxs-lookup"><span data-stu-id="955cb-117">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="955cb-118">**Если в Организации ранее было установлено приложение office 365 Advanced Threat protection (но не office 365 Threat Intelligence) в качестве надстройки** к другой подписке на Office 365, теперь у вас будет Office 365 Advanced Threat Protection Plan (план 1).</span><span class="sxs-lookup"><span data-stu-id="955cb-118">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="955cb-119">В том числе Office 365 Advanced Threat protection (план 1) (но не для расследования угроз и возможностей реагирования).</span><span class="sxs-lookup"><span data-stu-id="955cb-119">This includes Office 365 Advanced Threat Protection Plan 1, (but not threat investigation and response capabilities).</span></span>

<span data-ttu-id="955cb-120">Дополнительные сведения см. в статье [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat protection Description Service](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span><span class="sxs-lookup"><span data-stu-id="955cb-120">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigation-and-response-capabilities"></a><span data-ttu-id="955cb-121">Начало работы с расследованиям угроз и возможностями реагирования</span><span class="sxs-lookup"><span data-stu-id="955cb-121">Get started with threat investigation and response capabilities</span></span>

<span data-ttu-id="955cb-122">Используйте следующие ресурсы для получения дополнительных сведений об расследовании угроз и возможностях реагирования в Office 365, а также о том, как использовать его для более безопасного хранения людей в Организации.</span><span class="sxs-lookup"><span data-stu-id="955cb-122">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="955cb-123">[Начало работы с расследованиям угроз и ответом](get-started-with-ti.md) (сюда входят сведения о необходимых ролях)</span><span class="sxs-lookup"><span data-stu-id="955cb-123">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="955cb-124">Сведения о средствах отслеживания угроз — новые и полезные</span><span class="sxs-lookup"><span data-stu-id="955cb-124">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)

- [<span data-ttu-id="955cb-125">Экономия времени и усилий с помощью автоматизированного расследования и возможностей реагирования (AIR)</span><span class="sxs-lookup"><span data-stu-id="955cb-125">Save time and effort with Automated Investigation and Response (AIR) capabilities</span></span>](automated-investigation-response-office.md)

- [<span data-ttu-id="955cb-126">Использование обозревателя угроз (или обнаружения в режиме реального времени) для идентификации и исследования вредоносного содержимого в электронной почте и файлах</span><span class="sxs-lookup"><span data-stu-id="955cb-126">Use Threat Explorer (or real-time detections) to identify and investigate malicious content in email and files</span></span>](threat-explorer.md)
    
- [<span data-ttu-id="955cb-127">Ищите и изучайте нежелательную почту, которая былы доставлена</span><span class="sxs-lookup"><span data-stu-id="955cb-127">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="955cb-128">Использование симулятора атак для имитации атак и повышения осведомленности пользователей</span><span class="sxs-lookup"><span data-stu-id="955cb-128">Use Attack Simulator to simulate attacks and increase user awareness</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="955cb-129">Интеграция средств расследования и реагирования на угрозы с помощью Advanced Threat Protection в защитнике Майкрософт</span><span class="sxs-lookup"><span data-stu-id="955cb-129">Integrate Threat Investigation and Response capabilities with Microsoft Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="955cb-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="955cb-130">Related topics</span></span>

[<span data-ttu-id="955cb-131">Представления обозревателя угроз</span><span class="sxs-lookup"><span data-stu-id="955cb-131">Threat Explorer views</span></span>](threat-explorer-views.md)

[<span data-ttu-id="955cb-132">Защита от угроз в Office 365</span><span class="sxs-lookup"><span data-stu-id="955cb-132">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="955cb-133">Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="955cb-133">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="955cb-134">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="955cb-134">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 
