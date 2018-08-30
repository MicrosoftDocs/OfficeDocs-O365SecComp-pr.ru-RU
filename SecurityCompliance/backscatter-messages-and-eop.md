---
title: Подложные уведомления о недоставленном сообщении и EOP
ms.author: krowley
author: kccross
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
description: Подложные сообщения, автоматических недоставки сообщения, отправляемые с почтовых серверов, обычно из-за входящей нежелательной почты. ФИЛЬТРАЦИИ Backscatterer — список IP-адресов, которые отправляют сообщения подложный. Файл не является списком рекламное, и мы не пытайтесь удалить наших серверов из фильтрации Backscatterer.
ms.openlocfilehash: 2ab5c6a3bec347446452acd3bdfd8c5d309994a9
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002691"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="e449b-105">Подложные уведомления о недоставленном сообщении и EOP</span><span class="sxs-lookup"><span data-stu-id="e449b-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="e449b-p102">Подложные сообщения, автоматических недоставки сообщения, отправляемые с почтовых серверов, обычно из-за входящей нежелательной почты. Поскольку службы фильтрации нежелательной почты Exchange Online Protection (EOP), сообщения электронной почты отправленных несуществующим получателям и другие подозрительные получателям, отклоняются нашей службой. В этом случае EOP создает отчет о недоставке (NDR) сообщение и посылает отправителю «.» Так как часто используются подложного или недопустимых «От» адрес в сообщения, адрес отправителя, на который отправляются отчет о Недоставке может привести к подложный сообщения. В этом случае исходящих серверов, связанные с сетью EOP могут отображаться на Backscatterer DNS черного списка (фильтрации). ФИЛЬТРАЦИИ Backscatterer — список IP-адресов, которые отправляют сообщения подложный. Файл не является списком рекламное, и мы не пытайтесь удалить наших серверов из фильтрации Backscatterer.</span><span class="sxs-lookup"><span data-stu-id="e449b-p102">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam. Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service. When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender." Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message. When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL). The Backscatterer DNSBL is a list of IP addresses that send backscatter messages. It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="e449b-p103">Согласно инструкциям на веб-сайте Backscatterer использование режима отклонения для всех входящих сообщений не является рекомендуемой конфигурацией этой службы. Ее необходимо использовать в безопасном режиме. Дополнительные сведения о реализации правильной конфигурации Backscatterer см. на [веб-сайте Backscatterer.org](http://www.backscatterer.org/?target=usage).</span><span class="sxs-lookup"><span data-stu-id="e449b-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="e449b-116">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="e449b-116">For more information</span></span>

[<span data-ttu-id="e449b-117">Список IP-адресов на сайте The Backscatterer.org</span><span class="sxs-lookup"><span data-stu-id="e449b-117">The Backscatterer.org IP list</span></span>](https://blogs.msdn.com/b/tzink/archive/2012/08/22/the-backscatterer-org-ip-list.aspx)
  
<span data-ttu-id="e449b-118">Запись «Подложный отчет о Недоставке» в [параметры фильтрации расширенной нежелательной почты](advanced-spam-filtering-asf-options.md)</span><span class="sxs-lookup"><span data-stu-id="e449b-118">See the "NDR backscatter" entry in [Advanced spam filtering  options](advanced-spam-filtering-asf-options.md)</span></span>
  

