---
title: Поставленные в очередь, отложенные и возвращенные сообщения EOP вопросы и ответы
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: В этом разделе приводятся ответы на часто задаваемые вопросы о сообщениях, добавленных в очередь, отложенных или возвращенных в ходе процесса фильтрации Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 4b2c902adacd6e72e587aadaceecd22dd0084d85
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29686429"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="2706c-103">Поставленные в очередь, отложенные и возвращенные сообщения EOP: вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="2706c-103">EOP queued, deferred, and bounced messages FAQ</span></span>

<span data-ttu-id="2706c-104">В этом разделе приводятся ответы на часто задаваемые вопросы о сообщениях, добавленных в очередь, отложенных или возвращенных в ходе процесса фильтрации Microsoft Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="2706c-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Microsoft Exchange Online Protection (EOP) filtering process.</span></span>
  
 <span data-ttu-id="2706c-105">**В. Почему сообщения добавляются в очередь?**</span><span class="sxs-lookup"><span data-stu-id="2706c-105">**Q. Why is mail queuing?**</span></span>
  
<span data-ttu-id="2706c-p101">О. Сообщения добавляются в очередь или откладываются, если службе не удается установить соединение с сервером получателя для доставки. Сообщения не откладываются, если сеть получателя возвращает ошибку серии 500.</span><span class="sxs-lookup"><span data-stu-id="2706c-p101">A. Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery. It will not defer messages if a 500-series error is returned from the recipient network.</span></span>
  
 <span data-ttu-id="2706c-109">**В. Как откладываются сообщения?**</span><span class="sxs-lookup"><span data-stu-id="2706c-109">**Q. How does a message become deferred?**</span></span>
  
<span data-ttu-id="2706c-p102">О. Сообщения будут удерживаться, когда не удается установить соединение с сервером получателя, или сервер возвращает временную ошибку, например истечение времени ожидания подключения, отказ в соединении или ошибку серии 400. В случае постоянной ошибки, например ошибки серии 500, сообщение будет возвращено отправителю.</span><span class="sxs-lookup"><span data-stu-id="2706c-p102">A. Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error. If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>
  
 <span data-ttu-id="2706c-113">**В. Как долго сообщение остается отложенным, и чему равен интервал между повторными попытками?**</span><span class="sxs-lookup"><span data-stu-id="2706c-113">**Q. How long does a message remain in deferral and what is the retry interval?**</span></span>
  
<span data-ttu-id="2706c-p103">A. сообщений в об отсрочках будет храниться в нашем очередей 2 дня. Сообщение повторных попыток основаны на ошибки, которые мы получаем из системы почты получателя. Первый несколько расходов, 15 минут или меньше с последующих попыток (по следующей десятков наполовину или это) увеличение интервала через несколько повторы максимум 60 минут. Расширения продолжительность интервала динамических, принимая во внимание несколько переменных как размеры очереди и приоритет внутреннего сообщения. В basic, это 15 минут (или меньше) для запуска, развернув оттуда через Далее несколько часов для максимальной 60 минут.</span><span class="sxs-lookup"><span data-stu-id="2706c-p103">A. Messages in deferral will remain in our queues for 2 days. Message retry attempts are based on the error we get back from the recipient's mail system. The first few deferrals are 15 minutes or less, with subsequent retries (over the next half dozen or so) increasing the interval over multiple retries to a max of 60 minutes. The interval duration expansion is dynamic, taking into consideration multiple variables like queue sizes and internal message priority. In basic, it's 15 minutes (or less) to start, then expanding from there over the next few hours to 60 mins max.</span></span>
  
 <span data-ttu-id="2706c-120">**В. Как сообщения распределяются из очередь после восстановления почтового сервера?**</span><span class="sxs-lookup"><span data-stu-id="2706c-120">**Q. After your email server is restored, how are queued messages distributed?**</span></span>
  
<span data-ttu-id="2706c-p104">О. После восстановления почтового сервера все сообщения из очереди автоматически обрабатываются в то же порядке, в котором они были получены и добавлены в очередь, когда сервер стал недоступен.</span><span class="sxs-lookup"><span data-stu-id="2706c-p104">A. After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span> 
  

