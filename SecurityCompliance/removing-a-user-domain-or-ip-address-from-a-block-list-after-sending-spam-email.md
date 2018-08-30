---
title: Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 'Если пользователь постоянно рассылает из Office 365 нежелательную почту, он может лишиться возможности отправлять сообщения. '
ms.openlocfilehash: 87b7083fe1345a15ea582f12a5b0d417bbe6b568
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002609"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="9dc07-103">Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений</span><span class="sxs-lookup"><span data-stu-id="9dc07-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="9dc07-104">Если пользователь постоянно рассылает из Office 365 нежелательную почту, он может лишиться возможности отправлять сообщения. </span><span class="sxs-lookup"><span data-stu-id="9dc07-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="9dc07-105">
В этом случае отправитель получает отчет о недоставке (письмо о невозможности отправки сообщения) с конкретными инструкциями для снятия блокировки.</span><span class="sxs-lookup"><span data-stu-id="9dc07-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="9dc07-p101">Не только можно заблокировать отдельные пользователи службы, но конкретных веб-сайтами, доменами и IP-адресов, также могут быть заблокированы. В некоторых случаях доменов или веб-сайтов можно добавить в список блокировки только то, что они отображаются в сообщении нежелательной почты. В качестве администратора Office 365 можно попробовать получить пользователей, веб-сайтов, доменов и IP-адресов удаляется из списков блокировки сторонних производителей. Используйте ссылки в таблице в нижней части этого раздела для связи каждого сторонних производителей и затем следуйте инструкциям. Если кто-то за пределами Office 365 не могут отправлять сообщения в учетную запись Office 365, своей учетной записи может дойти до список внешних блокированных отправителей. Для удаления себя из списка заблокированных отправителей с помощью [портала самообслуживания исключений](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)можно попробовать пользователей за пределами Office 365.</span><span class="sxs-lookup"><span data-stu-id="9dc07-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="9dc07-p102">Вы можете настроить параметры исходящей нежелательной почты, чтобы получать уведомление, когда блокируется пользователь Office 365, отправляющий нежелательную почту. Как только проблема с почтовым ящиком пользователя будет решена, блокировку можно снять.</span><span class="sxs-lookup"><span data-stu-id="9dc07-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="9dc07-114">Отмена блокировки заблокированной учетной записи электронной почты Office 365</span><span class="sxs-lookup"><span data-stu-id="9dc07-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="9dc07-p103">Выполните эту задачу в центре администрирования Exchange (EAC). Извлечь [Центр администрирования Exchange в Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) для получения дополнительных сведений о центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="9dc07-p103">You complete this task in the Exchange admin center (EAC). Check out [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) for details about the EAC.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9dc07-117">Центр уведомлений отображается только в Центре администрирования Exchange для Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9dc07-117">You won't see the action center unless you're in the EAC for Exchange Online.</span></span> 
  
1. <span data-ttu-id="9dc07-118">В центре администрирования Exchange перейдите к разделу **Защита** \> **Центр поддержки**.</span><span class="sxs-lookup"><span data-stu-id="9dc07-118">In the EAC, navigate to **protection** \> **action center**.</span></span>
    
    ![Переход к центру уведомлений в Центре администрирования Exchange](media/9bbf0844-7b34-4a86-a2b7-8c7e9c8519a3.png)
  
2. <span data-ttu-id="9dc07-120">Нажмите значок **Поиск** и введите SMTP-адрес заблокированного пользователя.</span><span class="sxs-lookup"><span data-stu-id="9dc07-120">Select the **Search** icon, and then enter the SMTP address of the blocked user.</span></span> 
    
    ![Поиск заблокированного пользователя в центре уведомлений](media/f931b5a0-7115-4d95-9f6f-b403436031ba.png)
  
3. <span data-ttu-id="9dc07-122">Нажмите кнопку **Разблокировать учетную запись** на панели описания.</span><span class="sxs-lookup"><span data-stu-id="9dc07-122">Click **Unblock Account** in the description pane.</span></span> 
    
    ![Отмена блокировки пользователя в центре уведомлений](media/c5d5b1b9-8416-45aa-9631-881e94d1d056.png)
  
4. <span data-ttu-id="9dc07-124">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9dc07-124">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="9dc07-p104">Администратор клиента может разблокировать учетную запись ограниченное число раз. Если превысить это ограничение, появится сообщение с уведомлением об ошибке. Чтобы разблокировать пользователя, обратитесь в службу технической поддержки.</span><span class="sxs-lookup"><span data-stu-id="9dc07-p104">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. Contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="9dc07-127">Сторонние списки блокировок</span><span class="sxs-lookup"><span data-stu-id="9dc07-127">Third-party block lists</span></span>

|<span data-ttu-id="9dc07-128">**Имя списка**</span><span class="sxs-lookup"><span data-stu-id="9dc07-128">**List Name**</span></span>|<span data-ttu-id="9dc07-129">**Портал исключений**</span><span class="sxs-lookup"><span data-stu-id="9dc07-129">**Delisting Portal**</span></span>|<span data-ttu-id="9dc07-130">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="9dc07-130">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9dc07-131">URIBL</span><span class="sxs-lookup"><span data-stu-id="9dc07-131">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="9dc07-132">URIBL веб-сайта</span><span class="sxs-lookup"><span data-stu-id="9dc07-132">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="9dc07-133">SURBL</span><span class="sxs-lookup"><span data-stu-id="9dc07-133">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="9dc07-134">Краткие сведения о репутации SURBL URI данных</span><span class="sxs-lookup"><span data-stu-id="9dc07-134">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="9dc07-135">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="9dc07-135">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="9dc07-136">Общие сведения о фильтрации фильтрации</span><span class="sxs-lookup"><span data-stu-id="9dc07-136">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="9dc07-137">invaluement</span><span class="sxs-lookup"><span data-stu-id="9dc07-137">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="9dc07-138">Список список защиты от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="9dc07-138">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="9dc07-139">Phishtank</span><span class="sxs-lookup"><span data-stu-id="9dc07-139">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="9dc07-140">Вопросы и ответы по PhishTank</span><span class="sxs-lookup"><span data-stu-id="9dc07-140">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="9dc07-141">Exchange Online Protection также использует списки блокировки сторонних производителей для фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="9dc07-141">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="9dc07-142">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="9dc07-142">For more information</span></span>

[<span data-ttu-id="9dc07-143">Настройка правил защиты от спама для исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="9dc07-143">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="9dc07-144">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="9dc07-144">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="9dc07-145">Удаление себя из списка заблокированных отправителей Office 365 с помощью портала удаления из списка</span><span class="sxs-lookup"><span data-stu-id="9dc07-145">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

