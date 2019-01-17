---
title: Оповещения очереди и очередей
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 37640c80-ce6f-47e2-afd1-bc1d3c50e637
description: Администраторы могут узнать о оповещения очереди и очереди на панели мониторинга поток почты в центре соответствия требованиям & безопасности Office 365.
ms.openlocfilehash: fe750e32136af095bb0ccff8544306db76a7a667
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685615"
---
# <a name="queue-alerts-and-queues"></a><span data-ttu-id="55fb5-103">Оповещения очереди и очередей</span><span class="sxs-lookup"><span data-stu-id="55fb5-103">Queue alerts and Queues</span></span>

## <a name="queue-alerts"></a><span data-ttu-id="55fb5-104">Очередь оповещений</span><span class="sxs-lookup"><span data-stu-id="55fb5-104">Queue alerts</span></span>

<span data-ttu-id="55fb5-p101">Когда сообщения не могут отправлять из вашей организации Office 365 в своей локальной или партнерских почтовых серверов с помощью соединителей, сообщения поставлены в очередь в Office 365. Наиболее распространенные, которые вызывают это условие являются:</span><span class="sxs-lookup"><span data-stu-id="55fb5-p101">When messages can't be sent from your Office 365 organization to your on-premises or partner email servers using connectors, the messages are queued in Office 365. Common examples that cause this condition are:</span></span>

- <span data-ttu-id="55fb5-107">Соединитель настроен неправильно.</span><span class="sxs-lookup"><span data-stu-id="55fb5-107">The connector is incorrectly configured.</span></span>

- <span data-ttu-id="55fb5-108">Изменилось сети или брандмауэра в локальной среде.</span><span class="sxs-lookup"><span data-stu-id="55fb5-108">There have been networking or firewall changes in your on-premises environment.</span></span>

<span data-ttu-id="55fb5-p102">Office 365 будет продолжать попытки доставки для 48 часов. После 48 часов истечения срока действия сообщения и будут возвращаться отправителям в отчеты о недоставке (также известной как отчеты о недоставке или переходить сообщения).</span><span class="sxs-lookup"><span data-stu-id="55fb5-p102">Office 365 will continue to retry to delivery for 48 hours. After 48 hours, the messages will expire and will be returned to the senders in non-delivery reports (also known as a NDRs or bounce messages).</span></span>

<span data-ttu-id="55fb5-p103">Если том электронной почты в очереди превышает предварительно заданные пороговое значение (по умолчанию значение равно 2000 сообщений), оповещения будут доступны в панели мониторинга поток почты в **оповещений**и "Администраторы" будет получать уведомления по электронной почте (на свой адрес электронной почты альтернативный) . Чтобы настроить оповещения порогового значения, ежедневно ограничение уведомлений и/или получателей оповещения, в разделе **Настройка очереди оповещений** ниже.</span><span class="sxs-lookup"><span data-stu-id="55fb5-p103">If the queued email volume exceeds the pre-defined threshold (the default value is 2000 messages), the alerts will be available in the mail flow dashboard at **Recent alerts**, and admins will receive an email notification (to their alternative email address). To configure the alert threshold, daily notification limit, and/or recipients of the alert, see the **Customize queue alerts** section below.</span></span>

![Очередь оповещений в области последние оповещения панели мониторинга поток почты в центре соответствия требованиям & безопасности Office 365](media/5fc4a51c-6118-4270-960b-c6b176ef94ae.png)

## <a name="customize-queue-alerts"></a><span data-ttu-id="55fb5-114">Настройка оповещений очереди</span><span class="sxs-lookup"><span data-stu-id="55fb5-114">Customize queue alerts</span></span>

<span data-ttu-id="55fb5-p104">Полезные сведения о поток почты Создание оповещения политики именованные **отложенных сообщений** ( **отправки уведомлений по электронной почте** флажок в приведенном ниже снимке экрана примере) найден в **оповещения** \> **Политик оповещение**. Получатели порогового значения и предупреждения можно изменить, щелкнув в политике.</span><span class="sxs-lookup"><span data-stu-id="55fb5-p104">Mail flow insights create an alert policy named **Messages have been delayed** (the **Send email notifications** check box in the example screen shot below) found in **Alerts** \> **Alert Policies**. You can modify the threshold and alert recipients by clicking on the policy.</span></span>

![Оповещения о навигации](media/efb95976-9e0b-484e-a2fd-093c5bc7a40f.png)

<span data-ttu-id="55fb5-118">Вы увидите новый blade информацию политика, то можно нажать кнопку **Изменение политики**.</span><span class="sxs-lookup"><span data-stu-id="55fb5-118">You'll see a new policy information blade, you can now click **Edit Policy**.</span></span>

![Политика изменений ](media/ed2aceae-3ee2-4849-a17e-87915987a7dd.png)

<span data-ttu-id="55fb5-p105">Сведения о blade изменится на **Изменение политики**. Теперь можно изменить получателей сообщения электронной почты, ограничение на количество уведомлений, отправленных в день, а минимальное пороговое значение для запуска оповещения (200 и более).</span><span class="sxs-lookup"><span data-stu-id="55fb5-p105">The information blade will change to the **Edit Policy**. You can now change the recipients for the alert email, the limit on the number of notifications sent per day, and the minimum threshold to trigger the alert (200 or more).</span></span>

![Изменение политики Blade](media/c657cc74-7867-474c-b2c9-dc478449f990.png)

## <a name="queue-alert-details"></a><span data-ttu-id="55fb5-123">Детали оповещения очереди</span><span class="sxs-lookup"><span data-stu-id="55fb5-123">Queue alert details</span></span>

<span data-ttu-id="55fb5-124">При щелчке уведомления детали оповещения отображаются в области всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="55fb5-124">When you click the alert, the alert details appear in a flyout pane.</span></span>

![Выберите оповещение в очередь в области последние оповещения панели мониторинга поток почты в центре соответствия требованиям & безопасности Office 365](media/1f6b0e96-5b2c-41ef-9684-9d813b3fabe6.png)

![Оповещения всплывающее окно сведений очереди в центре соответствия требованиям & безопасности Office 365](media/105c8fff-912f-4763-8806-2740ebdecd4b.png)

<span data-ttu-id="55fb5-127">Щелкните **Просмотр очереди** в оповещения сведения, чтобы просмотреть сведения о очереди, проблем и ссылки на доступные исправления в новой области всплывающего.</span><span class="sxs-lookup"><span data-stu-id="55fb5-127">You can click **View queue** in the alert details to see the queue details, problems, and links to the available fixes in a new flyout pane.</span></span>

![Оповещения всплывающее окно сведений очереди в центре соответствия требованиям & безопасности Office 365](media/8ff60955-55ef-4f32-a966-85e02cb608d1.png)

![Просмотр очереди оповещения Дополнительные сведения](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)

## <a name="queues"></a><span data-ttu-id="55fb5-130">Очереди</span><span class="sxs-lookup"><span data-stu-id="55fb5-130">Queues</span></span>

<span data-ttu-id="55fb5-p106">Даже в том случае, если объем сообщений в очереди не превышает пороговое значение, по-прежнему можно использовать **очереди** область панели мониторинга поток обработки почты для просмотра сообщений, которые были поставлены в очередь для более чем на один час. Область **очереди** можно использовать для мониторинга число помещенных в очередь сообщений (значение 0 указывает, что поток почты — ОК) и выполнение действий перед становится слишком большое количество сообщений, помещенных в очередь.</span><span class="sxs-lookup"><span data-stu-id="55fb5-p106">Even if the queued message volume hasn't exceeded the threshold, you can still use the **Queues** area of the mail flow dashboard to see messages that have been queued for more than one hour. You can use the **Queues** area to monitor the number of queued messages (the value 0 indicates mail flow is OK) and take action before the number of queued messages becomes too large.</span></span>

![Очереди на панели мониторинга поток почты в центре соответствия требованиям & безопасности Office 365](media/0ef6e2ef-dd22-4363-9d4a-b20a00babc9f.png)

<span data-ttu-id="55fb5-134">При выберите количество сообщений, находящихся в **очереди**, сведения о очереди и инструкции по устранению этой проблемы отображаются в области всплывающих (же всплывающее окно, которое отображается после нажатия кнопки **Просмотр очереди** в дополнительных сведениях оповещение в очередь).</span><span class="sxs-lookup"><span data-stu-id="55fb5-134">When you click the number of queued messages in **Queues**, the queue details and guidance for how to fix the issue will appear in a flyout pane (the same flyout that appears after you click **View queue** in the details of a queue alert).</span></span>

![Сведения о очереди](media/4eb088fe-5dd9-4bf4-b959-c1bb2545c515.png)
