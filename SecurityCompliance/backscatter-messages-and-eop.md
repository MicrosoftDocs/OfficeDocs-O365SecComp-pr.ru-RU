---
title: Подложные уведомления о недоставленном сообщении и EOP
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
description: "Почтовые сообщения — это автоматизированные сообщения, которые отправляются почтовыми серверами, как правило, в результате входящих нежелательных сообщений. Список Backscatterer DNSBL \x97 это список IP-адресов, отправляющих подложные уведомления о недоставленном сообщении. Это не список злоумышленников, рассылающих нежелательную почту, и мы не пытаемся удалить наши серверы из него."
ms.openlocfilehash: 7581255ce4e68f6eb661df280ecb0cb94b7515ef
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693368"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="66fd3-105">Подложные уведомления о недоставленном сообщении и EOP</span><span class="sxs-lookup"><span data-stu-id="66fd3-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="66fd3-106">Почтовые сообщения — это автоматизированные сообщения, которые отправляются почтовыми серверами, как правило, в результате входящих нежелательных сообщений.</span><span class="sxs-lookup"><span data-stu-id="66fd3-106">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam.</span></span> <span data-ttu-id="66fd3-107">Так как Exchange Online Protection (EOP)  это служба фильтрации нежелательной почты, сообщения электронной почты, отправленные несуществующим получателям и на другие подозрительные адреса, отклоняются нашей службой.</span><span class="sxs-lookup"><span data-stu-id="66fd3-107">Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service.</span></span> <span data-ttu-id="66fd3-108">В этом случае EOP создает сообщение отчета о недоставке (NDR) и направляет его "отправителю".</span><span class="sxs-lookup"><span data-stu-id="66fd3-108">When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender."</span></span> <span data-ttu-id="66fd3-109">Так как злоумышленники, рассылающие нежелательную почту, часто используют поддельный или недопустимый адрес отправителя в своих сообщениях, то после отправки отчета о недоставки может быть отправлено подложное уведомление о недоставленном сообщении.</span><span class="sxs-lookup"><span data-stu-id="66fd3-109">Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message.</span></span> <span data-ttu-id="66fd3-110">В этом случае серверы исходящей почты, связанные с сетью EOP, могут попасть в список блокировки DNS отправителей подложных сообщений Backscatterer (DNSBL).</span><span class="sxs-lookup"><span data-stu-id="66fd3-110">When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL).</span></span> <span data-ttu-id="66fd3-111">Список Backscatterer DNSBL  это список IP-адресов, отправляющих подложные уведомления о недоставленном сообщении.</span><span class="sxs-lookup"><span data-stu-id="66fd3-111">The Backscatterer DNSBL is a list of IP addresses that send backscatter messages.</span></span> <span data-ttu-id="66fd3-112">Это не список злоумышленников, рассылающих нежелательную почту, и мы не пытаемся удалить наши серверы из него.</span><span class="sxs-lookup"><span data-stu-id="66fd3-112">It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="66fd3-p103">Согласно инструкциям на веб-сайте Backscatterer использование режима отклонения для всех входящих сообщений не является рекомендуемой конфигурацией этой службы. Ее необходимо использовать в безопасном режиме. Дополнительные сведения о реализации правильной конфигурации Backscatterer см. на [веб-сайте Backscatterer.org](http://www.backscatterer.org/?target=usage).</span><span class="sxs-lookup"><span data-stu-id="66fd3-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="66fd3-116">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="66fd3-116">For more information</span></span>

[<span data-ttu-id="66fd3-117">Список IP-адресов на сайте The Backscatterer.org</span><span class="sxs-lookup"><span data-stu-id="66fd3-117">The Backscatterer.org IP list</span></span>](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
<span data-ttu-id="66fd3-118">Просмотр записи "Нежелательная почта" в разделе [Advanced Filtering Options Filtering](advanced-spam-filtering-asf-options.md)</span><span class="sxs-lookup"><span data-stu-id="66fd3-118">See the "NDR backscatter" entry in [Advanced spam filtering  options](advanced-spam-filtering-asf-options.md)</span></span>
  

