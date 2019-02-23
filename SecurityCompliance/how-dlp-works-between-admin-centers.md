---
title: Как работает DLP между центром безопасности &amp; и соответствием центром администрирования Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Узнайте, как защита от потери &amp; данных в центре обеспечения безопасности работает с помощью правил защиты от потери данных и транспорта в центре администрирования Exchange.
ms.openlocfilehash: 531a45308594d03dc219f50d989a08236b8b5e20
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215649"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="97ad7-103">Как работает DLP между центром безопасности &amp; и соответствием центром администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="97ad7-103">How DLP works between the Security &amp; Compliance Center and Exchange Admin Center</span></span>

<span data-ttu-id="97ad7-104">В Office 365 вы можете создать политику защиты от потери данных (DLP) в двух разных центрах администрирования:</span><span class="sxs-lookup"><span data-stu-id="97ad7-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="97ad7-p101">В **центре безопасности &amp; и соответствия требованиям**можно создать единую политику DLP для защиты контента в SharePoint, OneDrive и Exchange. По возможности рекомендуется создать политику защиты от потери данных здесь. Для получения дополнительных сведений обратитесь [к разделу защита &amp; от потери данных в центре безопасности и соответствия требованиям](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="97ad7-p101">In the **Security &amp; Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security &amp; Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="97ad7-p102">В **центре администрирования Exchange**можно создать политику защиты от потери данных, которая поможет защитить контент только в Exchange. Эта политика может использовать правила транспорта Exchange, поэтому у нее есть дополнительные параметры обработки электронной почты. Для получения дополнительных сведений обратитесь к разделу защита [от потери данных в центре администрирования Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="97ad7-p102">In the **Exchange Admin Center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange transport rules, so it has more options specific to handling email. For more information, see [DLP in the Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="97ad7-111">Политики DLP, созданные в этих центрах администрирования, работают параллельно — в этом разделе описывается, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="97ad7-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Страницы защиты от потери данных в центре безопасности и соответствия требованиям и центре администрирования Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a><span data-ttu-id="97ad7-113">Принципы работы защиты от потери &amp; данных в центре безопасности и правилах транспорта в центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="97ad7-113">How DLP in the Security &amp; Compliance Center works with DLP and transport rules in the Exchange Admin Center</span></span>

<span data-ttu-id="97ad7-p103">После создания политики защиты от потери данных в центре &amp; безопасности и соответствия политике она будет развернута во всех расположениях, включенных в политику. Если политика включает Exchange Online, политика синхронизируется и применяется точно так же, как и политика защиты от потери данных, созданная в центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="97ad7-p103">After you create a DLP policy in the Security &amp; Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="97ad7-p104">Если вы создали политики защиты от потери данных в центре администрирования Exchange, эти политики продолжат работать параллельно с любыми политиками для электронной почты, созданной в центре &amp; соответствия требованиям безопасности. Но обратите внимание, что правила, созданные в центре администрирования Exchange, имеют приоритет. Все правила транспорта Exchange обрабатываются первыми, а затем обрабатываются правила защиты &amp; от потери данных из центра соответствия требованиям безопасности.</span><span class="sxs-lookup"><span data-stu-id="97ad7-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security &amp; Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange transport rules are processed first, and then the DLP rules from the Security &amp; Compliance Center are processed.</span></span>
  
<span data-ttu-id="97ad7-119">Это означает, что:</span><span class="sxs-lookup"><span data-stu-id="97ad7-119">This means that:</span></span>
  
- <span data-ttu-id="97ad7-120">Сообщения, заблокированные правилами транспорта Exchange, не будут сканироваться правилами защиты от потери данных, &amp; созданными в центре соответствия требованиям безопасности.</span><span class="sxs-lookup"><span data-stu-id="97ad7-120">Messages that are blocked by Exchange transport rules won't get scanned by DLP rules created in the Security &amp; Compliance Center.</span></span>
    
- <span data-ttu-id="97ad7-121">Если правило транспорта Exchange изменяет сообщение таким образом, что оно соответствует политике защиты от потери данных в центре соответствия требованиям безопасности &amp; (например, Добавление внешних пользователей), то правила защиты от потери данных будут обнаруживать эту политику и применять ее при необходимости.</span><span class="sxs-lookup"><span data-stu-id="97ad7-121">If an Exchange transport rule modifies a message in a way that causes it to match a DLP policy in the Security &amp; Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="97ad7-122">Кроме того, обратите внимание на то, что правила транспорта Exchange, использующие действие "остановить обработку", не влияют на &amp; обработку правил DLP в центре безопасности и соответствия требованиям: они по-прежнему будут обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="97ad7-122">Also note that Exchange transport rules that use the "stop processing" action don't affect the processing of DLP rules in the Security &amp; Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="97ad7-123">Подсказки политики в центре обеспечения &amp; безопасности и центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="97ad7-123">Policy tips in the Security &amp; Compliance Center vs. the Exchange Admin Center</span></span>

<span data-ttu-id="97ad7-p105">Подсказки политики могут работать с политиками защиты от потери данных и почтовыми политиками, созданными в центре администрирования Exchange, или с &amp; ПОЛИТИКАми защиты от потери данных, созданными в центре безопасности соответствия требованиям. Это связано с тем, что эти политики хранятся в разных расположениях, но подсказки политики можно изобразить только из одного места.</span><span class="sxs-lookup"><span data-stu-id="97ad7-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange Admin Center, or with DLP policies created in the Security &amp; Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="97ad7-p106">Если вы настроили подсказки политики в центре администрирования Exchange, любые подсказки политики, которые вы настроили &amp; в центре соответствия требованиям безопасности, не будут отображаться для пользователей в Outlook в Интернете и Outlook 2013 и более поздних версий до тех пор, пока вы не отключите советы в центре администрирования Exchange. Это гарантирует, что текущие правила транспорта Exchange будут работать, пока не переключились на центр соответствия требованиям безопасности &amp; .</span><span class="sxs-lookup"><span data-stu-id="97ad7-p106">If you've configured policy tips in the Exchange Admin Center, any policy tips that you configure in the Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange Admin Center. This ensures that your current Exchange transport rules will continue to work until you choose to switch over to the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="97ad7-128">Обратите внимание, что хотя подсказки политики могут рисовать только из одного места, уведомления по электронной почте всегда отправляются, даже если вы используете политики защиты &amp; от потери данных в центре безопасности и безопасности центра администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="97ad7-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>
  

