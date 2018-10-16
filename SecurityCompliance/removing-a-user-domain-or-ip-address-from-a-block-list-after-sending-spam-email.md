---
title: Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/16/2018
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
ms.openlocfilehash: 295d92fc6a1cd26783b18304a2d119d2ea0d7f1f
ms.sourcegitcommit: b164d4af65709133e0b512a4327a70fae13a974d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/16/2018
ms.locfileid: "25577068"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="393e3-103">Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений</span><span class="sxs-lookup"><span data-stu-id="393e3-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="393e3-p101">Если пользователь постоянно отправляет сообщения электронной почты из Office 365, классифицировано как нежелательная почта, они будут блокироваться может отправлять сообщения. Пользователя отображается в службы, как недопустимый исходящих отправителя и получите Non-недоставке (NDR) о том:</span><span class="sxs-lookup"><span data-stu-id="393e3-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="393e3-p102">Не удалось доставить сообщение, так как не распознается как допустимое отправителя. Наиболее распространенные причина этого заключается в том, что свой адрес электронной почты — это вероятные рассылку нежелательной почты и его имеет больше не могут отправлять сообщения за пределами вашей организации. Обратитесь к администратору по электронной почте.  Удаленный сервер вернул "550 5.1.8 отказано в доступе, недопустимый исходящих отправителя»</span><span class="sxs-lookup"><span data-stu-id="393e3-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="393e3-p103">Можно настроить параметры политики исходящей нежелательной почты, чтобы получить уведомление о блокировании пользователь Office 365 отправляет сообщения электронной почты. После разрешения проблемы с почтовым ящиком пользователя можно удалить блок на этого отправителя.</span><span class="sxs-lookup"><span data-stu-id="393e3-p103">You can configure your outbound spam policy settings so that you get a notification when an Office 365 user is blocked from sending email. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="393e3-112">Отмена блокировки заблокированной учетной записи электронной почты Office 365</span><span class="sxs-lookup"><span data-stu-id="393e3-112">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="393e3-p104">Выполните эту задачу в Office 365 безопасности & соответствия центр единым Хранилищем. [Последовательно выберите пункты безопасность Office 365 и центре соответствия требованиям](go-to-the-securitycompliance-center.md) для получения дополнительных сведений о SCC.</span><span class="sxs-lookup"><span data-stu-id="393e3-p104">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="393e3-115">С помощью рабочих или школы учетной записи, имеющей права глобального администратора Office 365, войти в центре соответствия требованиям и безопасности Office 365 и в списке слева разверните **Threat Management**, нажмите кнопку **Обзор**и выберите **Restricted Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="393e3-115">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="393e3-116">Чтобы перейти непосредственно к странице **Ограниченный доступ** (ранее называлась центр поддержки) безопасности &amp; центре соответствия требованиям, используйте этот URL-адрес: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="393e3-116">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="393e3-p105">На этой странице будет содержать список пользователей, которые были заблокированы может отправлять почту за пределами вашей организации.  Найти пользователя, которого необходимо удалить ограничения на и нажмите кнопку **разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="393e3-p105">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="393e3-119">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="393e3-119">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="393e3-p106">Существует ограничение на количество совпадений для учетной записи можно разблокировать администратором клиента При превышении ограничений для пользователя отображается сообщение об ошибке. Затем необходимо обратиться в службу поддержки разблокирование пользователя.</span><span class="sxs-lookup"><span data-stu-id="393e3-p106">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="393e3-122">Сторонние списки блокировок</span><span class="sxs-lookup"><span data-stu-id="393e3-122">Third-party block lists</span></span>

<span data-ttu-id="393e3-p107">Exchange Online Protection также использует списки блокировки сторонних производителей для принятия решений в фильтрации нежелательной почты. Пользователи, веб-сайтов, доменов и IP-адреса можно добавить в черные списки только для отображения в сообщении нежелательной почты. В качестве администратора Office 365 попробуйте для получения этих объектов, удаляется из списка сторонних поставщиков, если они относятся к вам.</span><span class="sxs-lookup"><span data-stu-id="393e3-p107">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="393e3-p108">Если кто-то за пределами Office 365 не могут отправлять сообщения в учетную запись Office 365, может быть своей учетной записи в списке внешние заблокированных отправителей. Для удаления сами через [портал самостоятельного исключений](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)можно попробовать пользователей за пределами Office 365.</span><span class="sxs-lookup"><span data-stu-id="393e3-p108">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="393e3-128">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="393e3-128">For more information</span></span>

[<span data-ttu-id="393e3-129">Реагирование на запись атаке электронной почты</span><span class="sxs-lookup"><span data-stu-id="393e3-129">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="393e3-130">Настройка политики защиты от нежелательной почты для исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="393e3-130">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="393e3-131">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="393e3-131">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

  

  

