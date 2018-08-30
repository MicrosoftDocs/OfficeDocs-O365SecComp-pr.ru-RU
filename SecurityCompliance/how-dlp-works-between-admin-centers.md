---
title: Как работает защиты от потери данных между безопасности &amp; центре соответствия требованиям и Центр администрирования Exchange
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Узнайте, как защиты от потери данных в системы &amp; центре соответствия требованиям для работы с защиты от потери данных и правила транспорта в центре администрирования Exchange.
ms.openlocfilehash: bc7494f504c2c0ffa668562d6e64b9f29992e24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535124"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="8acbc-103">Как работает защиты от потери данных между безопасности &amp; центре соответствия требованиям и Центр администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="8acbc-103">How DLP works between the Security &amp; Compliance Center and Exchange Admin Center</span></span>

<span data-ttu-id="8acbc-104">В Office 365 можно создать политику предотвращения (DLP) потери данных в двух центров обработки различных администрирования:</span><span class="sxs-lookup"><span data-stu-id="8acbc-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="8acbc-p101">В **безопасности &amp; центре соответствия требованиям**, можно создать одну политику защиты от потери данных для защиты контента в SharePoint, OneDrive и Exchange. Если возможно, рекомендуется создать политику предотвращения потери данных. Дополнительные сведения можно [защиты от потери данных в системы &amp; центре соответствия требованиям](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8acbc-p101">In the **Security &amp; Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security &amp; Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="8acbc-p102">В **Центре администрирования Exchange**можно создать политику защиты от потери данных для защиты содержимого только в Exchange. Эту политику можно использовать правила транспорта Exchange, поэтому имеет несколько параметров для обработки электронной почты. Для получения дополнительных сведений см [защиты от потери данных в центре администрирования Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="8acbc-p102">In the **Exchange Admin Center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange transport rules, so it has more options specific to handling email. For more information, see [DLP in the Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="8acbc-111">Политики защиты от потери данных создан в этих администрирования центры работают рядом - в этом разделе описывается, как.</span><span class="sxs-lookup"><span data-stu-id="8acbc-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Страницы защиты от потери данных в центре администрирования Exchange и центре соответствия требованиям безопасности](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a><span data-ttu-id="8acbc-113">Способ защиты от потери данных в системы &amp; центре соответствия требованиям для работы с защиты от потери данных и правила транспорта в центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="8acbc-113">How DLP in the Security &amp; Compliance Center works with DLP and transport rules in the Exchange Admin Center</span></span>

<span data-ttu-id="8acbc-p103">После создания политики защиты от потери данных в системы &amp; центре соответствия требованиям, политика развертывается для всех узлов, включенных в политике. Если политика включает Exchange Online, политика синхронизирован существует и применения в точно так же, как политики защиты от потери данных, созданных в центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="8acbc-p103">After you create a DLP policy in the Security &amp; Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="8acbc-p104">При создании политики защиты от потери данных в центре администрирования Exchange этих политик будут продолжать работать рядом с любые политики для электронной почты, создаваемого в системы &amp; центре соответствия требованиям. Но Обратите внимание на то, что правила, созданные в центре администрирования Exchange, имеют приоритет. Сначала обрабатываются все правила транспорта Exchange, а затем правил защиты от потери данных из системы &amp; обрабатываются центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="8acbc-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security &amp; Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange transport rules are processed first, and then the DLP rules from the Security &amp; Compliance Center are processed.</span></span>
  
<span data-ttu-id="8acbc-119">Это означает, что:</span><span class="sxs-lookup"><span data-stu-id="8acbc-119">This means that:</span></span>
  
- <span data-ttu-id="8acbc-120">Сообщения, которые блокируются правила транспорта Exchange не получите проверены правила защиты от потери данных, созданные в безопасности &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="8acbc-120">Messages that are blocked by Exchange transport rules won't get scanned by DLP rules created in the Security &amp; Compliance Center.</span></span>
    
- <span data-ttu-id="8acbc-121">Если правило транспорта Exchange изменяет сообщение в виде, который вызывает их в соответствии с политики защиты от потери данных в системы &amp; центр соответствия — например, добавление внешние пользователи - затем правила защиты от потери данных будет обнаруживать это и принудительное применение политики при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8acbc-121">If an Exchange transport rule modifies a message in a way that causes it to match a DLP policy in the Security &amp; Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="8acbc-122">Также Обратите внимание, что правила транспорта Exchange, использующих действие «остановить обработку» не влияет на функции обработки для защиты от потери данных правил ценные &amp; центр соответствия — они по-прежнему будут обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="8acbc-122">Also note that Exchange transport rules that use the "stop processing" action don't affect the processing of DLP rules in the Security &amp; Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="8acbc-123">Советы политики безопасности &amp; центре соответствия требованиям и Центр администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="8acbc-123">Policy tips in the Security &amp; Compliance Center vs. the Exchange Admin Center</span></span>

<span data-ttu-id="8acbc-p105">Советы по политикам можно работать с помощью политик защиты от потери данных и почтовые поток правила, созданные в центре администрирования Exchange или с помощью политик DLP, созданных в системы &amp; центре соответствия требованиям, но не оба. Это, так как эти политики хранятся в различных местах, но советы по политикам можно создать только из одного расположения.</span><span class="sxs-lookup"><span data-stu-id="8acbc-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange Admin Center, or with DLP policies created in the Security &amp; Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="8acbc-p106">Если вы настроили подсказок политики в центре администрирования Exchange, советы политики для настройки безопасности &amp; центре соответствия требованиям не будет отображаться для пользователей в Outlook в Интернете и Outlook 2013 и более поздних версий, пока не отключить советы, приведенные в центре администрирования Exchange. Это гарантирует, что текущие правила транспорта Exchange будет продолжать работать, пока пользователь не для переключения на безопасность &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="8acbc-p106">If you've configured policy tips in the Exchange Admin Center, any policy tips that you configure in the Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange Admin Center. This ensures that your current Exchange transport rules will continue to work until you choose to switch over to the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="8acbc-128">Обратите внимание, что во время советы по политикам можно создать только из одного расположения уведомлений по электронной почте отправляются всегда, даже в том случае, если вы используете политик защиты от потери данных в обоих системы &amp; центре соответствия требованиям и Центр администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="8acbc-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>
  

