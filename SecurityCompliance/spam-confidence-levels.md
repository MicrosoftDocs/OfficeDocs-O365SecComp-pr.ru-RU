---
title: Вероятность нежелательной почты
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
description: Когда электронное сообщение проходит процесс фильтрации нежелательной почты, ему назначается область нежелательных сообщений. Эта область соотносится с оценкой вероятности нежелательной почты и отмечается в Х-заголовке. Служба предпринимает действия к сообщениям в зависимости от интерпретации оценки вероятности нежелательной почты. В таблице ниже показано, как разные оценки вероятности нежелательной почты интерпретируются фильтрами, а также действия по умолчанию, которые применяются к входящим сообщениям в зависимости от оценки.
ms.openlocfilehash: 1822fa50f9815397513fddf7a2024a99277cbb28
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275649"
---
# <a name="spam-confidence-levels"></a><span data-ttu-id="cd936-106">Вероятность нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="cd936-106">Spam confidence levels</span></span>

<span data-ttu-id="cd936-p102">Когда электронное сообщение проходит процесс фильтрации нежелательной почты, ему назначается область нежелательных сообщений. Эта область соотносится с оценкой вероятности нежелательной почты и отмечается в Х-заголовке. Служба предпринимает действия к сообщениям в зависимости от интерпретации оценки вероятности нежелательной почты. В таблице ниже показано, как разные оценки вероятности нежелательной почты интерпретируются фильтрами, а также действия по умолчанию, которые применяются к входящим сообщениям в зависимости от оценки.</span><span class="sxs-lookup"><span data-stu-id="cd936-p102">When an email message goes through spam filtering it is assigned a spam score. That score is mapped to an individual Spam Confidence Level (SCL) rating and stamped in an X-header. The service takes actions upon the messages depending upon the spam confidence interpretation of the SCL rating. The following table shows how the different SCL ratings are interpreted by the filters and the default action that is taken on inbound messages for each rating.</span></span>
  
|<span data-ttu-id="cd936-111">**Оценка вероятности нежелательной почты**</span><span class="sxs-lookup"><span data-stu-id="cd936-111">**SCL Rating**</span></span>|<span data-ttu-id="cd936-112">**Интерпретации оценки вероятности нежелательной почты**</span><span class="sxs-lookup"><span data-stu-id="cd936-112">**Spam Confidence Interpretation**</span></span>|<span data-ttu-id="cd936-113">**Действие по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="cd936-113">**Default Action**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cd936-114">-1</span><span class="sxs-lookup"><span data-stu-id="cd936-114">-1</span></span>  <br/> |<span data-ttu-id="cd936-115">Сообщение, не относящееся к нежелательным, от надежного отправителя, надежного получателя или надежного IP-адреса (доверенный партнер)</span><span class="sxs-lookup"><span data-stu-id="cd936-115">Non-spam coming from a safe sender, safe recipient, or safe listed IP address (trusted partner)</span></span>  <br/> |<span data-ttu-id="cd936-116">Доставка сообщения в папку входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="cd936-116">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="cd936-117">0, 1</span><span class="sxs-lookup"><span data-stu-id="cd936-117">0, 1</span></span>  <br/> |<span data-ttu-id="cd936-118">Сообщение не относится к нежелательным, так как оно было проверено и определено как чистое</span><span class="sxs-lookup"><span data-stu-id="cd936-118">Non-spam because the message was scanned and determined to be clean</span></span>  <br/> |<span data-ttu-id="cd936-119">Доставка сообщения в папку входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="cd936-119">Deliver the message to the recipients' inbox.</span></span>  <br/> |
|<span data-ttu-id="cd936-120">5, 6</span><span class="sxs-lookup"><span data-stu-id="cd936-120">5, 6</span></span>  <br/> | <span data-ttu-id="cd936-121">Нежелательное сообщение</span><span class="sxs-lookup"><span data-stu-id="cd936-121">Spam</span></span>  <br/> |<span data-ttu-id="cd936-122">Доставка сообщения в папку нежелательной почты получателя.</span><span class="sxs-lookup"><span data-stu-id="cd936-122">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
|<span data-ttu-id="cd936-123">7, 8, 9</span><span class="sxs-lookup"><span data-stu-id="cd936-123">7, 8, 9</span></span>  <br/> |<span data-ttu-id="cd936-124">Нежелательное сообщение высокого уровня</span><span class="sxs-lookup"><span data-stu-id="cd936-124">High confidence spam</span></span>  <br/> |<span data-ttu-id="cd936-125">Доставка сообщения в папку нежелательной почты получателя.</span><span class="sxs-lookup"><span data-stu-id="cd936-125">Deliver the message to the recipients' Junk Email folder.</span></span>  <br/> |
   
> [!TIP]
> <span data-ttu-id="cd936-p103">Оценки SCL, равные 2, 3, 4, 7 и 8, не устанавливаются службой. Оценка ВЕРОЯТНОсти неЖЕЛАТЕЛЬНОй почты 5 или 6 считается потенциальной нежелательной почтой, которая меньше, чем уровень ВЕРОЯТНОсти неЖЕЛАТЕЛЬНОй почты, равный 9, что считается определенной нежелательной почтой. Различные действия по нежелательной почте и высокой вероятности нежелательной почты можно настроить с помощью политик фильтрации содержимого в центре администрирования Exchange. Дополнительные сведения можно найти [в статье Настройка политик фильтрации нежелательной почты](configure-your-spam-filter-policies.md). Вы также можете задать рейтинг ВЕРОЯТНОсти неЖЕЛАТЕЛЬНОй почты для сообщений, которые отвечают определенным условиям, с помощью правил транспорта, как описано в статье Использование правил обработки почты для установки вероятности нежелательной [почты (SCL) в сообщениях](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). Если вы используете правило транспорта, чтобы задать значение ВЕРОЯТНОсти неЖЕЛАТЕЛЬНОй почты 7, 8 или 9, сообщение будет обрабатываться как нежелательная почта высокой достоверности.</span><span class="sxs-lookup"><span data-stu-id="cd936-p103">SCL ratings of 2, 3, 4, 7, and 8 are not set by the service. An SCL rating of 5 or 6 is considered suspected spam, which is less certain to be spam than an SCL rating of 9, which is considered certain spam. Different actions for spam and high confidence spam can be configured via your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). You can also set the SCL rating for messages that match specific conditions by using Transport rules, as described in [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md). If you use a transport rule to set SCL of 7, 8, or 9 the message will be treated as high confidence spam.</span></span> 
  
||
|:-----|
|<span data-ttu-id="cd936-p104">![Небольшой значок LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **Никогда не работали с Office 365?**         Вам помогут бесплатные видеокурсы по **Office 365 admins and IT pros**, предоставленные платформой LinkedIn Learning.</span><span class="sxs-lookup"><span data-stu-id="cd936-p104">![The short icon for LinkedIn Learning](media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Office 365?**         Discover free video courses for **Office 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span> |
   

