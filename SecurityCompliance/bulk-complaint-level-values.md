---
title: Уровни жалоб на массовые сообщения
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 3/5/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
description: Разные системы массовой рассылки используют различные шаблоны, средства создания контента и списки адресатов. Некоторые из них отправляют подписчикам полезные сообщения с соответствующим содержимым. Такие сообщения вызывают очень мало жалоб со стороны получателей. Другие же системы массовой рассылки распространяют нежелательные сообщения, похожие на спам, и тем самым вызывают множество жалоб от получателей. Для распознавания таких систем рассылок групповым сообщениям присваивается оценка BCL (уровень жалоб на массовые сообщения). Оценка BCL может варьироваться от 1 до 9 в зависимости от того, насколько высока вероятность получения жалоб на сообщения, рассылаемые системой. Система массовой рассылки с оценкой BCL 9 вызовет намного больше жалоб со стороны получателей, чем система с оценкой BCL 3. Майкрософт использует внутренние и сторонние источники для идентификации массовых рассылок и присвоения соответствующей оценки BCL. Эта оценка приводится в заголовке каждого сообщения X-Microsoft-Antispam. Дополнительные сведения об этом заголовке см. в статье Заголовки сообщений по защите от нежелательной почты.
ms.openlocfilehash: adf179ba4a309f2ed22275179013b576888960c6
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026266"
---
# <a name="bulk-complaint-level-values"></a><span data-ttu-id="351be-112">Уровни жалоб на массовые сообщения</span><span class="sxs-lookup"><span data-stu-id="351be-112">Bulk Complaint Level values</span></span>

<span data-ttu-id="351be-p102">Разные системы массовой рассылки используют различные шаблоны, средства создания контента и списки адресатов. Некоторые из них отправляют подписчикам полезные сообщения с соответствующим содержимым. Такие сообщения вызывают очень мало жалоб со стороны получателей. Другие же системы массовой рассылки распространяют нежелательные сообщения, похожие на спам, и тем самым вызывают множество жалоб от получателей. Для распознавания таких систем рассылок групповым сообщениям присваивается оценка BCL (уровень жалоб на массовые сообщения). Оценка BCL может варьироваться от 1 до 9 в зависимости от того, насколько высока вероятность получения жалоб на сообщения, рассылаемые системой. Система массовой рассылки с оценкой BCL 9 вызовет намного больше жалоб со стороны получателей, чем система с оценкой BCL 3. Майкрософт использует внутренние и сторонние источники для идентификации массовых рассылок и присвоения соответствующей оценки BCL. Эта оценка приводится в заголовке каждого сообщения **X-Microsoft-Antispam**. Дополнительные сведения об этом заголовке см. в статье [Заголовки сообщений по защите от нежелательной почты](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="351be-p102">Bulk mailers vary in their sending patterns, content creation, and list acquisition practices. Some are good bulk mailers that send wanted messages with relevant content to their subscribers. These messages generate few complaints from recipients. Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients. To distinguish these types of bulk mailers, messages from bulk mailers are assigned a Bulk Complaint Level (BCL) rating. BCL ratings range from 1 to 9 depending on how likely the bulk mailer is to generate complaints. A sender that has a rating of BCL 9 is likely to generate many complaints from recipients, whereas a rating of BCL 3 is unlikely to generate many complaints. Microsoft uses both internal and third-party sources to identify bulk mail and determine the appropriate BCL. This rating is exposed in the **X-Microsoft-Antispam** header of every message. For more information about this message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span> 
  
<span data-ttu-id="351be-123">Вы можете использовать значения BCL, чтобы установить уровень фильтрации массовых рассылок, соответствующий требованиям вашей организации. Для этого нужно выполнить действия, приведенные в статье [Настройте политики защиты от спама](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="351be-123">You can use BCL values to set the desired level of bulk filtering your organization requires by following the steps in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
<span data-ttu-id="351be-p103">Добавляются новые значения BCL, которые будут указаны здесь в будущем. В таблице ниже приведены и описаны значения BCL, которые используются в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="351be-p103">More BCL values are being added and will be included here in the future. The following table lists and describes the BCL values that are currently in use.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="351be-126">**Значение BCL**</span><span class="sxs-lookup"><span data-stu-id="351be-126">**BCL Value**</span></span> <br/> |<span data-ttu-id="351be-127">**Описание**</span><span class="sxs-lookup"><span data-stu-id="351be-127">**Description**</span></span> <br/> |
|<span data-ttu-id="351be-128">0</span><span class="sxs-lookup"><span data-stu-id="351be-128">0</span></span>  <br/> |<span data-ttu-id="351be-129">Сообщение отправлено без использования систем массовой рассылки.</span><span class="sxs-lookup"><span data-stu-id="351be-129">The message isn't from a bulk sender.</span></span>  <br/> |
|<span data-ttu-id="351be-130">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="351be-130">1, 2, 3</span></span>  <br/> |<span data-ttu-id="351be-131">Сообщение от системы массовой рассылки, которое вызывает малое количество жалоб.</span><span class="sxs-lookup"><span data-stu-id="351be-131">The message is from a bulk sender that generates few complaints.</span></span>  <br/> |
|<span data-ttu-id="351be-132">4, 5, 6, 7</span><span class="sxs-lookup"><span data-stu-id="351be-132">4, 5, 6, 7</span></span>  <br/> |<span data-ttu-id="351be-133">Сообщение от системы массовой рассылки, которое может вызвать как малое, так и большое количество жалоб.</span><span class="sxs-lookup"><span data-stu-id="351be-133">The message is from a bulk sender that generates a mixed number of complaints.</span></span>  <br/> |
|<span data-ttu-id="351be-134">8, 9</span><span class="sxs-lookup"><span data-stu-id="351be-134">8, 9</span></span>  <br/> |<span data-ttu-id="351be-135">Сообщение от системы массовой рассылки, которое вызывает большое количество жалоб</span><span class="sxs-lookup"><span data-stu-id="351be-135">The message is from a bulk sender that generates a high number of complaints</span></span>  <br/> |
   
