---
title: Руководство по безопасности (Майкрософт) для политических кампаний, некоммерческих и других динамических организаций
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.custom: Strat_O365_Enterprise
ms.assetid: 10d1004b-42b6-4e2b-aaa2-18ddd9118f64
description: Сводка. Руководство по планированию и реализации для быстроразвивающихся организаций с высокой вероятностью возникновения угроз безопасности.
ms.openlocfilehash: df2b259f992c781bfa86acfaff0bb0a378994a6b
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272094"
---
# <a name="microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-organizations"></a><span data-ttu-id="5489c-103">Руководство по безопасности (Майкрософт) для политических кампаний, некоммерческих и других динамических организаций</span><span class="sxs-lookup"><span data-stu-id="5489c-103">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>

 <span data-ttu-id="5489c-104">**Сводка.** Руководство по планированию и реализации для быстроразвивающихся организаций с высокой вероятностью возникновения угроз безопасности.</span><span class="sxs-lookup"><span data-stu-id="5489c-104">**Summary:** Planning and implementation guidance for fast-moving organizations that have an increased threat profile.</span></span>
  
<span data-ttu-id="5489c-p101">Если у вас динамичная организация, небольшая команда ИТ-специалистов, а профиль угроз выше среднего, это руководство — именно то, что вам нужно. Здесь вы узнаете, как быстро создать среду с основными облачным службами, куда изначально входят и элементы управления безопасностью. В этом руководстве приводятся рекомендации по защите данных, электронной почты и удостоверений, а также по организации безопасного доступа с мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="5489c-p101">If your organization is agile, you have a small IT team, and your threat profile is higher than average, this guidance is designed for you. This solution demonstrates how to quickly build an environment with essential cloud services that include secure controls from the start. This guidance includes prescriptive security recommendations for protecting data, identities, email, and access from mobile devices.</span></span>
  
## <a name="security-solution-guidance"></a><span data-ttu-id="5489c-108">Руководство по безопасности</span><span class="sxs-lookup"><span data-stu-id="5489c-108">Security solution guidance</span></span>

<span data-ttu-id="5489c-p102">В этом руководстве описано, как реализовать безопасную облачную среду. Это руководство может использовать любая организация. В него входят дополнительные справочные сведения для организации с гибкими возможностями работы с доступом BYOD и учетными записями гостей. Его можно взять за основу при разработке собственной среды. Отзывы можно отправлять по адресу [CloudAdopt@microsoft.com](mailto:CloudAdopt@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="5489c-p102">This guidance describes how to implement a secure cloud environment. The solution guidance can be used by any organization. It includes extra help for agile organizations with BYOD access and guest accounts. You can use this guidance as a starting-point for designing your own environment. We welcome your feedback at [CloudAdopt@microsoft.com](mailto:CloudAdopt@microsoft.com).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5489c-114">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5489c-114">**Item**</span></span> <br/> |<span data-ttu-id="5489c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5489c-115">**Description**</span></span> <br/> |
|<span data-ttu-id="5489c-116">**Руководство по безопасности (Майкрософт) для политических кампаний**</span><span class="sxs-lookup"><span data-stu-id="5489c-116">**Microsoft Security Guidance for Political Campaigns**</span></span> <br/> <span data-ttu-id="5489c-117">[![Эскиз для набора мини-постеров.](media/d370ce28-ca40-4930-9a2c-907312aa06c8.png)          ](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)</span><span class="sxs-lookup"><span data-stu-id="5489c-117">[![Thumb nail for mini poster set.](media/d370ce28-ca40-4930-9a2c-907312aa06c8.png)          ](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)</span></span> <br/> <span data-ttu-id="5489c-118">[PDF](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)  \| [Visio](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.vsdx)</span><span class="sxs-lookup"><span data-stu-id="5489c-118">[PDF](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.pdf)  \| [Visio](http://download.microsoft.com/download/B/4/D/B4D520C3-4D0C-4B4D-BFB9-09F0651C2775/MSFT_Cloud_architecture_security%20for%20political%20campaigns.vsdx)</span></span> <br/> |<span data-ttu-id="5489c-p103">В этом руководстве в качестве примера приведена организация, проводящая политические кампании. Используйте это руководство в качестве отправной точки для любой среды.</span><span class="sxs-lookup"><span data-stu-id="5489c-p103">This guidance uses a political campaign organization as an example. Use this guidance as a starting point for any environment.</span></span>  <br/> |
|<span data-ttu-id="5489c-121">**Руководство по безопасности (Майкрософт) для некоммерческих организаций**</span><span class="sxs-lookup"><span data-stu-id="5489c-121">**Microsoft Security Guidance for Nonprofits**</span></span> <br/> <span data-ttu-id="5489c-122">[![Эскиз для скачиваемого файла](media/e4784889-1c69-4067-9a8f-31d31d1eceea.png)          ](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)</span><span class="sxs-lookup"><span data-stu-id="5489c-122">[![Thumnail image for downloadable file](media/e4784889-1c69-4067-9a8f-31d31d1eceea.png)          ](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)</span></span> <br/> <span data-ttu-id="5489c-123">[PDF](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)  \| [Visio](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.vsdx)</span><span class="sxs-lookup"><span data-stu-id="5489c-123">[PDF](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.pdf)  \| [Visio](http://download.microsoft.com/download/9/4/3/94389612-C679-4061-8DF2-D9A15D72B65F/Microsoft_Cloud%20Architecture_Security%20for%20Nonprofits.vsdx)</span></span> <br/> |<span data-ttu-id="5489c-p104">В это руководство внесены незначительные изменения, благодаря которым оно подходит некоммерческим организациям. Например, рассмотрены планы Office 365 для некоммерческих организаций. Техническое руководство ничем не отличается от такового для организаций, проводящих политические кампании.</span><span class="sxs-lookup"><span data-stu-id="5489c-p104">This guide is slightly revised for nonprofit organizations. For example, it references Office 365 Nonprofit plans. The technical guidance is the same as the political campaign solution guide.</span></span>  <br/> |
   
## <a name="test-lab-guides"></a><span data-ttu-id="5489c-127">Руководства по лаборатории тестирования</span><span class="sxs-lookup"><span data-stu-id="5489c-127">Test Lab Guides</span></span>

<span data-ttu-id="5489c-128">Чтобы создать среду разработки и тестирования для этого решения, используйте следующие руководства:</span><span class="sxs-lookup"><span data-stu-id="5489c-128">To create a dev/test environment for this solution, use the following test lab guides:</span></span> 
  
- [<span data-ttu-id="5489c-129">Настройка групп и пользователей в случае среды разработки и тестирования для политической кампании</span><span class="sxs-lookup"><span data-stu-id="5489c-129">Configure groups and users for a political campaign dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/configure-groups-and-users-for-a-political-campaign-dev-test-environment)
    
     <span data-ttu-id="5489c-130">Создайте пробные подписки на Office 365 и EMS, а затем создайте группы и пользователей для типичной политической кампании.</span><span class="sxs-lookup"><span data-stu-id="5489c-130">Create trial subscriptions for Office 365 and EMS and then create groups and users for a representative political campaign.</span></span>
    
- [<span data-ttu-id="5489c-131">Создание сайтов групп в среде разработки и тестирования для политической кампании</span><span class="sxs-lookup"><span data-stu-id="5489c-131">Create team sites in a political campaign dev/test environment</span></span>](https://docs.microsoft.com/office365/enterprise/create-team-sites-in-a-political-campaign-dev-test-environment)
    
    <span data-ttu-id="5489c-132">Создайте четыре сайта группы SharePoint Online с уровнями безопасности "Для внутреннего пользования", "Для личного пользования", "Конфиденциально" и "Строго конфиденциально".</span><span class="sxs-lookup"><span data-stu-id="5489c-132">Create four SharePoint Online team sites with Internal, Private, Sensitive, and Highly Confidential levels of security.</span></span>
    
<span data-ttu-id="5489c-133">Дополнительные функции безопасности для демонстрации или доказательства правильности концепции см. в статье [Руководства по лаборатории тестирования Office 365](http://aka.ms/o365tlgs).</span><span class="sxs-lookup"><span data-stu-id="5489c-133">For additional security features for demonstration or proof of concept, see [Office 365 Test Lab Guides](http://aka.ms/o365tlgs).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5489c-134">См. также</span><span class="sxs-lookup"><span data-stu-id="5489c-134">See Also</span></span>

[<span data-ttu-id="5489c-135">Руководства по лаборатории тестирования для облачных решений</span><span class="sxs-lookup"><span data-stu-id="5489c-135">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[<span data-ttu-id="5489c-136">Ресурсы, посвященные ИТ-архитектуре Microsoft Cloud</span><span class="sxs-lookup"><span data-stu-id="5489c-136">Microsoft Cloud IT architecture resources</span></span>](https://docs.microsoft.com/office365/enterprise/microsoft-cloud-it-architecture-resources)



