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
ms.openlocfilehash: 8dcd6c8f55d867e1c2e249ec71a3a5c6b78ac76a
ms.sourcegitcommit: d89c24258123a3ffde574a391d59afd3aea8470d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2018
ms.locfileid: "23955441"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="c516c-103">Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений</span><span class="sxs-lookup"><span data-stu-id="c516c-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="c516c-p101">Если пользователь постоянно отправляет сообщения электронной почты из Office 365, классифицировано как нежелательная почта, они будут блокироваться может отправлять сообщения. Пользователя отображается в службы, как недопустимый исходящих отправителя и будет получать отчет о недоставке (NDR или не удается отправить сообщение электронной почты), которая предоставляет конкретные сведения о действиях, которые необходимо предпринять для разблокирования сами.</span><span class="sxs-lookup"><span data-stu-id="c516c-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>

<span data-ttu-id="c516c-p102">Можно настроить параметры политики исходящей нежелательной почты, чтобы получить уведомление о блокировании пользователь Office 365 отправляет сообщения электронной почты. После разрешения проблемы с почтовым ящиком пользователя можно удалить блок на этого отправителя.</span><span class="sxs-lookup"><span data-stu-id="c516c-p102">You can configure your outbound spam policy settings so that you get a notification when an Office 365 user is blocked from sending email. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="c516c-108">Отмена блокировки заблокированной учетной записи электронной почты Office 365</span><span class="sxs-lookup"><span data-stu-id="c516c-108">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="c516c-p103">Выполните эту задачу в Office 365 безопасности & соответствия центр единым Хранилищем. [Последовательно выберите пункты безопасность Office 365 и центре соответствия требованиям](go-to-the-securitycompliance-center.md) для получения дополнительных сведений о SCC.</span><span class="sxs-lookup"><span data-stu-id="c516c-p103">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="c516c-111">С помощью рабочих или школы учетной записи, имеющей права глобального администратора Office 365, войти в центре соответствия требованиям и безопасности Office 365 и в списке слева разверните **Threat Management**, нажмите кнопку **Обзор**и выберите **Restricted Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="c516c-111">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="c516c-112">Чтобы перейти непосредственно к странице **Пользователи с ограниченным доступом** в безопасности &amp; центре соответствия требованиям, используйте этот URL-адрес: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="c516c-112">To go directly to the **Restricted Users** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="c516c-p104">На этой странице будет содержать список пользователей, которые были заблокированы может отправлять почту за пределами вашей организации.  Найти пользователя, которого необходимо удалить ограничения на и нажмите кнопку **разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="c516c-p104">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="c516c-115">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c516c-115">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c516c-p105">Существует ограничение на количество совпадений для учетной записи можно разблокировать администратором клиента При превышении ограничений для пользователя отображается сообщение об ошибке. Затем необходимо обратиться в службу поддержки разблокирование пользователя.</span><span class="sxs-lookup"><span data-stu-id="c516c-p105">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="c516c-118">Сторонние списки блокировок</span><span class="sxs-lookup"><span data-stu-id="c516c-118">Third-party block lists</span></span>

<span data-ttu-id="c516c-p106">Exchange Online Protection также использует списки блокировки сторонних производителей для принятия решений в фильтрации нежелательной почты. Пользователи, веб-сайтов, доменов и IP-адреса можно добавить в черные списки только для отображения в сообщении нежелательной почты. В качестве администратора Office 365 попробуйте для получения этих объектов, удаляется из списка сторонних поставщиков, если они относятся к вам. Используйте ссылки в приведенной ниже таблице связаться с каждой сторонних производителей и затем следуйте инструкциям.</span><span class="sxs-lookup"><span data-stu-id="c516c-p106">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you. Use the links in the below table to contact each third party and then follow their instructions.</span></span>

|<span data-ttu-id="c516c-123">**Имя списка**</span><span class="sxs-lookup"><span data-stu-id="c516c-123">**List Name**</span></span>|<span data-ttu-id="c516c-124">**Портал исключений**</span><span class="sxs-lookup"><span data-stu-id="c516c-124">**Delisting Portal**</span></span>|<span data-ttu-id="c516c-125">**Дополнительные сведения**</span><span class="sxs-lookup"><span data-stu-id="c516c-125">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c516c-126">URIBL</span><span class="sxs-lookup"><span data-stu-id="c516c-126">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="c516c-127">URIBL веб-сайта</span><span class="sxs-lookup"><span data-stu-id="c516c-127">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="c516c-128">SURBL</span><span class="sxs-lookup"><span data-stu-id="c516c-128">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="c516c-129">Краткие сведения о репутации SURBL URI данных</span><span class="sxs-lookup"><span data-stu-id="c516c-129">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="c516c-130">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="c516c-130">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="c516c-131">Общие сведения о фильтрации фильтрации</span><span class="sxs-lookup"><span data-stu-id="c516c-131">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="c516c-132">invaluement</span><span class="sxs-lookup"><span data-stu-id="c516c-132">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="c516c-133">Список список защиты от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="c516c-133">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="c516c-134">Phishtank</span><span class="sxs-lookup"><span data-stu-id="c516c-134">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="c516c-135">Вопросы и ответы по PhishTank</span><span class="sxs-lookup"><span data-stu-id="c516c-135">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |

> [!NOTE]
> <span data-ttu-id="c516c-p107">Если кто-то за пределами Office 365 не могут отправлять сообщения в учетную запись Office 365, может быть своей учетной записи в списке внешние заблокированных отправителей. Для удаления сами через [портал самостоятельного исключений](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)можно попробовать пользователей за пределами Office 365.</span><span class="sxs-lookup"><span data-stu-id="c516c-p107">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="c516c-138">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="c516c-138">For more information</span></span>

[<span data-ttu-id="c516c-139">Реагирование на запись атаке электронной почты</span><span class="sxs-lookup"><span data-stu-id="c516c-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="c516c-140">Настройка политики защиты от нежелательной почты для исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="c516c-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="c516c-141">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="c516c-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

  

  

