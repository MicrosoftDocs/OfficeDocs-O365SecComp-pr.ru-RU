---
title: Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
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
ms.openlocfilehash: ff5bb010f45b0c89e08239f0e37885bd7ae5c7cd
ms.sourcegitcommit: 234a22c61859133ed5e7988a9551a569781518a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2018
ms.locfileid: "23875791"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="f0713-103">Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений</span><span class="sxs-lookup"><span data-stu-id="f0713-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="f0713-104">Если пользователь постоянно рассылает из Office 365 нежелательную почту, он может лишиться возможности отправлять сообщения. </span><span class="sxs-lookup"><span data-stu-id="f0713-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="f0713-105">
В этом случае отправитель получает отчет о недоставке (письмо о невозможности отправки сообщения) с конкретными инструкциями для снятия блокировки.</span><span class="sxs-lookup"><span data-stu-id="f0713-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="f0713-p101">Не только можно заблокировать отдельные пользователи службы, но конкретных веб-сайтами, доменами и IP-адресов, также могут быть заблокированы. В некоторых случаях доменов или веб-сайтов можно добавить в список блокировки только то, что они отображаются в сообщении нежелательной почты. В качестве администратора Office 365 можно попробовать получить пользователей, веб-сайтов, доменов и IP-адресов удаляется из списков блокировки сторонних производителей. Используйте ссылки в таблице в нижней части этого раздела для связи каждого сторонних производителей и затем следуйте инструкциям. Если кто-то за пределами Office 365 не могут отправлять сообщения в учетную запись Office 365, своей учетной записи может дойти до список внешних блокированных отправителей. Для удаления себя из списка заблокированных отправителей с помощью [портала самообслуживания исключений](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)можно попробовать пользователей за пределами Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0713-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="f0713-p102">Вы можете настроить параметры исходящей нежелательной почты, чтобы получать уведомление, когда блокируется пользователь Office 365, отправляющий нежелательную почту. Как только проблема с почтовым ящиком пользователя будет решена, блокировку можно снять.</span><span class="sxs-lookup"><span data-stu-id="f0713-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="f0713-114">Отмена блокировки заблокированной учетной записи электронной почты Office 365</span><span class="sxs-lookup"><span data-stu-id="f0713-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="f0713-p103">Выполните эту задачу в Office 365 безопасности & соответствия центр единым Хранилищем. [Последовательно выберите пункты безопасность Office 365 и центре соответствия требованиям](go-to-the-securitycompliance-center.md) для получения дополнительных сведений о SCC.</span><span class="sxs-lookup"><span data-stu-id="f0713-p103">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="f0713-117">С помощью рабочих или школы учетной записи, имеющей права глобального администратора Office 365, войти в центре соответствия требованиям и безопасности Office 365 и в списке слева разверните **Threat Management**, нажмите кнопку **Обзор**и выберите **Restricted Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="f0713-117">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="f0713-118">Чтобы перейти непосредственно к странице **Пользователи с ограниченным доступом** в безопасности &amp; центре соответствия требованиям, используйте этот URL-адрес: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="f0713-118">To go directly to the **Restricted Users** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="f0713-p104">На этой странице будет содержать список пользователей, которые были заблокированы может отправлять почту за пределами вашей организации.  Найти пользователя, которого необходимо удалить ограничения на и нажмите кнопку **разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="f0713-p104">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="f0713-121">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f0713-121">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f0713-p105">Существует ограничение на количество совпадений для учетной записи можно разблокировать администратором клиента При превышении ограничений для пользователя отображается сообщение об ошибке. Затем необходимо обратиться в службу поддержки разблокирование пользователя.</span><span class="sxs-lookup"><span data-stu-id="f0713-p105">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="f0713-124">Сторонние списки блокировок</span><span class="sxs-lookup"><span data-stu-id="f0713-124">Third-party block lists</span></span>

|<span data-ttu-id="f0713-125">**Имя списка**</span><span class="sxs-lookup"><span data-stu-id="f0713-125">**List Name**</span></span>|<span data-ttu-id="f0713-126">**Портал исключений**</span><span class="sxs-lookup"><span data-stu-id="f0713-126">**Delisting Portal**</span></span>|<span data-ttu-id="f0713-127">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="f0713-127">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0713-128">URIBL</span><span class="sxs-lookup"><span data-stu-id="f0713-128">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="f0713-129">URIBL веб-сайта</span><span class="sxs-lookup"><span data-stu-id="f0713-129">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="f0713-130">SURBL</span><span class="sxs-lookup"><span data-stu-id="f0713-130">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="f0713-131">Краткие сведения о репутации SURBL URI данных</span><span class="sxs-lookup"><span data-stu-id="f0713-131">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="f0713-132">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="f0713-132">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="f0713-133">Общие сведения о фильтрации фильтрации</span><span class="sxs-lookup"><span data-stu-id="f0713-133">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="f0713-134">invaluement</span><span class="sxs-lookup"><span data-stu-id="f0713-134">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="f0713-135">Список список защиты от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="f0713-135">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="f0713-136">Phishtank</span><span class="sxs-lookup"><span data-stu-id="f0713-136">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="f0713-137">Вопросы и ответы по PhishTank</span><span class="sxs-lookup"><span data-stu-id="f0713-137">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="f0713-138">Exchange Online Protection также использует списки блокировки сторонних производителей для фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="f0713-138">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="f0713-139">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="f0713-139">For more information</span></span>

[<span data-ttu-id="f0713-140">Настройка правил защиты от спама для исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="f0713-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="f0713-141">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="f0713-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="f0713-142">Удаление себя из списка заблокированных отправителей Office 365 с помощью портала удаления из списка</span><span class="sxs-lookup"><span data-stu-id="f0713-142">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

