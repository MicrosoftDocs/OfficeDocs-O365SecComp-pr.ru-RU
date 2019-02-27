---
title: Подложные уведомления о недоставленном сообщении и EOP
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
description: Почтовые сообщения — это автоматизированные сообщения, которые отправляются почтовыми серверами, как правило, в результате входящих нежелательных сообщений. DNSBL с рассеиванием — это список IP-адресов, которые отправляют сообщения с нерасположенной рассеиванием. Он не является списком нежелательной почты и не пытается удалить наши серверы из DNSBL.
ms.openlocfilehash: 73f8631c50bcfb8a023b2b6007b7ccf48038e16e
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275299"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="3aa93-105">Подложные уведомления о недоставленном сообщении и EOP</span><span class="sxs-lookup"><span data-stu-id="3aa93-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="3aa93-p102">Почтовые сообщения — это автоматизированные сообщения, которые отправляются почтовыми серверами, как правило, в результате входящих нежелательных сообщений. Так как служба фильтрации нежелательной почты Exchange Online Protection (EOP) является службой фильтрации нежелательной почты, сообщения электронной почты, отправленные несуществующим получателям и другим подозрительным адресатам, отклоняются нашей службой. В этом случае EOP создает сообщение о недоставке и доставляет его обратно в "отправитель". Так как нежелательные сообщения часто используют подложный или недопустимый адрес из сообщения, адрес отправителя, на который отправляется отчет о недоСТАВКЕ, может привести к появлению сообщения о недоСТАВКЕ. В этом случае исходящие серверы, связанные с сетью EOP, могут быть указаны в черном списке DNS (DNSBL). DNSBL с рассеиванием — это список IP-адресов, которые отправляют сообщения с нерасположенной рассеиванием. Он не является списком нежелательной почты и не пытается удалить наши серверы из DNSBL.</span><span class="sxs-lookup"><span data-stu-id="3aa93-p102">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam. Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service. When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender." Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message. When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL). The Backscatterer DNSBL is a list of IP addresses that send backscatter messages. It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="3aa93-p103">Согласно инструкциям на веб-сайте Backscatterer использование режима отклонения для всех входящих сообщений не является рекомендуемой конфигурацией этой службы. Ее необходимо использовать в безопасном режиме. Дополнительные сведения о реализации правильной конфигурации Backscatterer см. на [веб-сайте Backscatterer.org](http://www.backscatterer.org/?target=usage).</span><span class="sxs-lookup"><span data-stu-id="3aa93-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="3aa93-116">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3aa93-116">For more information</span></span>

[<span data-ttu-id="3aa93-117">Список IP-адресов на сайте The Backscatterer.org</span><span class="sxs-lookup"><span data-stu-id="3aa93-117">The Backscatterer.org IP list</span></span>](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
<span data-ttu-id="3aa93-118">Просмотр записи "Нежелательная почта" в разделе [Advanced Filtering Options Filtering](advanced-spam-filtering-asf-options.md)</span><span class="sxs-lookup"><span data-stu-id="3aa93-118">See the "NDR backscatter" entry in [Advanced spam filtering  options](advanced-spam-filtering-asf-options.md)</span></span>
  

