---
title: Поставленные в очередь, отложенные и возвращенные сообщения EOP вопросы и ответы
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: В этом разделе приводятся ответы на часто задаваемые вопросы о сообщениях, добавленных в очередь, отложенных или возвращенных в ходе процесса фильтрации Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: e8fdb07d11a1f540e94b82730eb848a97f51523a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256267"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="e13c0-103">Поставленные в очередь, отложенные и возвращенные сообщения EOP: вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="e13c0-103">EOP queued, deferred, and bounced messages FAQ</span></span>

<span data-ttu-id="e13c0-104">В этом разделе приводятся ответы на часто задаваемые вопросы о сообщениях, добавленных в очередь, отложенных или возвращенных в ходе процесса фильтрации Microsoft Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="e13c0-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Microsoft Exchange Online Protection (EOP) filtering process.</span></span>
  
 <span data-ttu-id="e13c0-105">**В. Почему сообщения добавляются в очередь?**</span><span class="sxs-lookup"><span data-stu-id="e13c0-105">**Q. Why is mail queuing?**</span></span>
  
<span data-ttu-id="e13c0-p101">О. Сообщения добавляются в очередь или откладываются, если службе не удается установить соединение с сервером получателя для доставки. Сообщения не откладываются, если сеть получателя возвращает ошибку серии 500.</span><span class="sxs-lookup"><span data-stu-id="e13c0-p101">A. Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery. It will not defer messages if a 500-series error is returned from the recipient network.</span></span>
  
 <span data-ttu-id="e13c0-109">**В. Как откладываются сообщения?**</span><span class="sxs-lookup"><span data-stu-id="e13c0-109">**Q. How does a message become deferred?**</span></span>
  
<span data-ttu-id="e13c0-p102">О. Сообщения будут удерживаться, когда не удается установить соединение с сервером получателя, или сервер возвращает временную ошибку, например истечение времени ожидания подключения, отказ в соединении или ошибку серии 400. В случае постоянной ошибки, например ошибки серии 500, сообщение будет возвращено отправителю.</span><span class="sxs-lookup"><span data-stu-id="e13c0-p102">A. Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error. If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>
  
 <span data-ttu-id="e13c0-113">**В. Как долго сообщение остается отложенным, и чему равен интервал между повторными попытками?**</span><span class="sxs-lookup"><span data-stu-id="e13c0-113">**Q. How long does a message remain in deferral and what is the retry interval?**</span></span>
  
<span data-ttu-id="e13c0-114">О.</span><span class="sxs-lookup"><span data-stu-id="e13c0-114">A.</span></span> <span data-ttu-id="e13c0-115">Отложенные сообщения будут оставаться в очереди в течение 2 дней.</span><span class="sxs-lookup"><span data-stu-id="e13c0-115">Messages in deferral will remain in our queues for 2 days.</span></span> <span data-ttu-id="e13c0-116">Попытки повторной отправки сообщений зависят от ошибки, полученной от почтовой системы получателя.</span><span class="sxs-lookup"><span data-stu-id="e13c0-116">Message retry attempts are based on the error we get back from the recipient's mail system.</span></span> <span data-ttu-id="e13c0-117">Первые несколько РБП выводятся 15 минут или меньше, при последующих повторах (на ближайшие половины десятков) увеличивается интервал до нескольких повторов в течение 60 минут.</span><span class="sxs-lookup"><span data-stu-id="e13c0-117">The first few deferrals are 15 minutes or less, with subsequent retries (over the next half dozen or so) increasing the interval over multiple retries to a max of 60 minutes.</span></span> <span data-ttu-id="e13c0-118">Расширение длительности интервала является динамическим, учитывая несколько переменных, таких как размер очереди и внутренний приоритет сообщений.</span><span class="sxs-lookup"><span data-stu-id="e13c0-118">The interval duration expansion is dynamic, taking into consideration multiple variables like queue sizes and internal message priority.</span></span> <span data-ttu-id="e13c0-119">В основном это 15 минут (или меньше) для запуска, а затем развертывание в течение следующих нескольких часов до 60 мин.</span><span class="sxs-lookup"><span data-stu-id="e13c0-119">In basic, it's 15 minutes (or less) to start, then expanding from there over the next few hours to 60 mins max.</span></span>
  
 <span data-ttu-id="e13c0-120">**В. Как сообщения распределяются из очередь после восстановления почтового сервера?**</span><span class="sxs-lookup"><span data-stu-id="e13c0-120">**Q. After your email server is restored, how are queued messages distributed?**</span></span>
  
<span data-ttu-id="e13c0-p104">О. После восстановления почтового сервера все сообщения из очереди автоматически обрабатываются в то же порядке, в котором они были получены и добавлены в очередь, когда сервер стал недоступен.</span><span class="sxs-lookup"><span data-stu-id="e13c0-p104">A. After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span> 
  

