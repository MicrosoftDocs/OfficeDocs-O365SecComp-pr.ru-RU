---
title: Взаимодействие DLP между центром безопасности _Амп_ и центром администрирования Exchange
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
description: Узнайте, как система защиты от потери данных в центре безопасности _Амп_ соответствует правилам защиты от потери данных и почтовых ящиков (правила транспорта) в центре администрирования Exchange.
ms.openlocfilehash: c20cf5d4e7b83a726b104a57b89f2d8f765d7f16
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341490"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a><span data-ttu-id="f00ff-103">Взаимодействие DLP между центром безопасности _Амп_ и центром администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="f00ff-103">How DLP works between the Security & Compliance Center and Exchange admin center</span></span>

<span data-ttu-id="f00ff-104">В Office 365 вы можете создать политику защиты от потери данных (DLP) в двух разных центрах администрирования:</span><span class="sxs-lookup"><span data-stu-id="f00ff-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="f00ff-p101">В **центре безопасности _Амп_ соответствие требованиям**можно создать единую политику защиты от потери данных, которая поможет защитить контент в SharePoint, OneDrive и Exchange. По возможности рекомендуется создать политику защиты от потери данных здесь. Для получения дополнительных сведений обратитесь [к разделу защита от потери данных в центре безопасности _амп_](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="f00ff-p101">In the **Security & Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security & Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="f00ff-p102">В **центре администрирования Exchange**можно создать политику защиты от потери данных, которая поможет защитить контент только в Exchange. Эта политика может использовать правила для обработки почтового ящика Exchange (также называемые правилами транспорта), поэтому у нее есть дополнительные параметры обработки электронной почты. Для получения дополнительных сведений обратитесь к разделу защита [от потери данных в центре администрирования Exchange](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="f00ff-p102">In the **Exchange admin center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange mail flow rules (also known as transport rules), so it has more options specific to handling email. For more information, see [DLP in the Exchange admin center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="f00ff-111">Политики DLP, созданные в этих центрах администрирования, работают параллельно — в этом разделе описывается, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="f00ff-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![Страницы защиты от потери данных в центре безопасности и соответствия требованиям и центре администрирования Exchange](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a><span data-ttu-id="f00ff-113">Принцип работы защиты от потери данных в центре безопасности _Амп_ соответствует правилам защиты от потери данных и почтовых ящиков в центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="f00ff-113">How DLP in the Security & Compliance Center works with DLP and mail flow rules in the Exchange admin center</span></span>

<span data-ttu-id="f00ff-p103">После создания политики защиты от потери данных в центре безопасности _Амп_ соответствие политике разворачивается во всех расположениях, включенных в политику. Если политика включает Exchange Online, политика синхронизируется и применяется точно так же, как и политика защиты от потери данных, созданная в центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="f00ff-p103">After you create a DLP policy in the Security & Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="f00ff-p104">Если вы создали политики защиты от потери данных в центре администрирования Exchange, эти политики продолжат работать параллельно с любыми политиками для электронной почты, создаваемой в центре безопасности _Амп_ соответствия требованиям. Но обратите внимание, что правила, созданные в центре администрирования Exchange, имеют приоритет. Все правила для почтовых ящиков Exchange обрабатываются первыми, а затем обрабатываются правила защиты от потери данных из центра обеспечения безопасности _Амп_.</span><span class="sxs-lookup"><span data-stu-id="f00ff-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security & Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange mail flow rules are processed first, and then the DLP rules from the Security & Compliance Center are processed.</span></span>
  
<span data-ttu-id="f00ff-119">Это означает, что:</span><span class="sxs-lookup"><span data-stu-id="f00ff-119">This means that:</span></span>
  
- <span data-ttu-id="f00ff-120">Сообщения, заблокированные правилами для почтовых ящиков Exchange, не отсканированы правилами DLP, созданными в центре безопасности _Амп_ соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="f00ff-120">Messages that are blocked by Exchange mail flow rules won't get scanned by DLP rules created in the Security & Compliance Center.</span></span>
    
- <span data-ttu-id="f00ff-121">Если правило обработки почты Exchange изменяет сообщение таким образом, что оно соответствует политике DLP в центре безопасности _Амп_ соответствия требованиям (например, Добавление внешних пользователей), то правила защиты от потери данных будут обнаруживать эту политику и применять ее при необходимости.</span><span class="sxs-lookup"><span data-stu-id="f00ff-121">If an Exchange mail flow rule modifies a message in a way that causes it to match a DLP policy in the Security & Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="f00ff-122">Кроме того, обратите внимание, что правила для почтовых ящиков Exchange, использующие действие "остановить обработку", не влияют на обработку правил DLP в центре безопасности _Амп_ соответствия требованиям — они по-прежнему будут обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="f00ff-122">Also note that Exchange mail flow rules that use the "stop processing" action don't affect the processing of DLP rules in the Security & Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="f00ff-123">Подсказки политики в центре безопасности _Амп_ соответствие требованиям и в центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="f00ff-123">Policy tips in the Security & Compliance Center vs. the Exchange admin center</span></span>

<span data-ttu-id="f00ff-p105">Подсказки политики могут работать с политиками защиты от потери данных и правилами, созданными в центре администрирования Exchange, или с политиками защиты от потери данных, созданными в центре безопасности _Амп_ соответствие требованиям. Это связано с тем, что эти политики хранятся в разных расположениях, но подсказки политики можно изобразить только из одного места.</span><span class="sxs-lookup"><span data-stu-id="f00ff-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange admin center, or with DLP policies created in the Security & Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="f00ff-p106">Если вы настроили подсказки политики в центре администрирования Exchange, любые подсказки политики, которые вы настроили в центре обеспечения безопасности _Амп_, не будут отображаться для пользователей в Outlook в Интернете и Outlook 2013 и более поздних версий, пока вы не отключите советы в центре администрирования Exchange. Это гарантирует, что текущие правила для почтовых ящиков Exchange продолжат работать, пока не будет выбрано переключиться на центр обеспечения безопасности _Амп_.</span><span class="sxs-lookup"><span data-stu-id="f00ff-p106">If you've configured policy tips in the Exchange admin center, any policy tips that you configure in the Security & Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange admin center. This ensures that your current Exchange mail flow rules will continue to work until you choose to switch over to the Security & Compliance Center.</span></span>
  
<span data-ttu-id="f00ff-128">Обратите внимание, что хотя подсказки политики могут рисовать только из одного места, уведомления по электронной почте всегда отправляются, даже если вы используете политики защиты от потери данных в центре безопасности _Амп_ соответствие требованиям и в центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="f00ff-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security & Compliance Center and the Exchange admin center.</span></span>
  

