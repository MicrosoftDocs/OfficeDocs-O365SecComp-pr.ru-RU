---
title: Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/01/2018
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
ms.openlocfilehash: 6f6f4504a9c79463aadc21f2eaeadcd769e8b151
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614403"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="cf3fb-103">Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений</span><span class="sxs-lookup"><span data-stu-id="cf3fb-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="cf3fb-p101">Если пользователь постоянно отправляет сообщения электронной почты из Office 365, классифицировано как нежелательная почта, они будут блокироваться может отправлять сообщения. Пользователя отображается в службы, как недопустимый исходящих отправителя и получите Non-недоставке (NDR) о том:</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="cf3fb-p102">Не удалось доставить сообщение, так как не распознается как допустимое отправителя. Наиболее распространенные причина этого заключается в том, что свой адрес электронной почты — это вероятные рассылку нежелательной почты и его имеет больше не могут отправлять сообщения за пределами вашей организации. Обратитесь к администратору по электронной почте.  Удаленный сервер вернул "550 5.1.8 отказано в доступе, недопустимый исходящих отправителя»</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="cf3fb-110">Администраторы клиента также будет получать предупреждения о том, что пользователь был ограничен может отправлять любые дополнительные исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-110">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="cf3fb-111">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="cf3fb-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="cf3fb-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="cf3fb-112"></span></span>

<span data-ttu-id="cf3fb-113">Предполагаемое время для завершения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="cf3fb-p103">Вы должны быть назначены разрешения, перед выполнением этой процедуры или процедуры. Чтобы увидеть, какие нужны разрешения, см «защита от нежелательной почты в разделе [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="cf3fb-p104">Следующую процедуру можно также выполнить с помощью удаленной оболочки PowerShell. Командлет Get-BlockedSenderAddress для получения списка ограниченных пользователей и Remove-BlockedSenderAddress необходимость удаления ограничения. Чтобы узнать, как использовать Windows PowerShell для подключения к Exchange Online, обратитесь к разделу [подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p104">The following procedure can also be performed via remote PowerShell. Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="cf3fb-119">Удалить ограничения для блокировки учетной записи электронной почты Office 365</span><span class="sxs-lookup"><span data-stu-id="cf3fb-119">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="cf3fb-p105">Выполните эту задачу в Office 365 безопасность & соответствия центр единым Хранилищем. [Перейдите к Office 365 безопасность & центре соответствия требованиям](go-to-the-securitycompliance-center.md) для получения дополнительных сведений о SCC. Необходимо быть в **Управление организацией** или группу ролей **Безопасности администратора** для выполнения этих функций. [Перейдите к разрешения в Office 365 безопасность & центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md) для получения дополнительных сведений о группах ролей SCC.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p105">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC. You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions. [Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="cf3fb-124">С помощью рабочих или школы учетной записи, имеющей права глобального администратора Office 365, войти в центре соответствия требованиям и безопасности Office 365 и в списке слева разверните **Threat Management**, нажмите кнопку **Обзор**и выберите **Restricted Пользователи**.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-124">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="cf3fb-125">Чтобы перейти непосредственно к странице **Ограниченный доступ** (ранее называлась центр поддержки) безопасности &amp; центре соответствия требованиям, используйте этот URL-адрес: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="cf3fb-125">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="cf3fb-p106">На этой странице будет содержать список пользователей, которые были заблокированы может отправлять почту за пределами вашей организации.  Найти пользователя, которого необходимо удалить ограничения на и нажмите кнопку **разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p106">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="cf3fb-128">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-128">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="cf3fb-p107">Существует ограничение на количество совпадений для учетной записи можно разблокировать администратором клиента При превышении ограничений для пользователя отображается сообщение об ошибке. Затем необходимо обратиться в службу поддержки разблокирование пользователя.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p107">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span></br></br> <span data-ttu-id="cf3fb-131">Может потребоваться до 1 час, прежде чем пользователь не заблокирован.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-131">It may take up to 1 hour before the user is unblocked.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="cf3fb-132">Сторонние списки блокировок</span><span class="sxs-lookup"><span data-stu-id="cf3fb-132">Third-party block lists</span></span>

<span data-ttu-id="cf3fb-p108">Exchange Online Protection также использует списки блокировки сторонних производителей для принятия решений в фильтрации нежелательной почты. Пользователи, веб-сайтов, доменов и IP-адреса можно добавить в черные списки только для отображения в сообщении нежелательной почты. В качестве администратора Office 365 попробуйте для получения этих объектов, удаляется из списка сторонних поставщиков, если они относятся к вам.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p108">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="cf3fb-p109">Если кто-то за пределами Office 365 не могут отправлять сообщения в учетную запись Office 365, может быть своей учетной записи в списке внешние заблокированных отправителей. Для удаления сами через [портал самостоятельного исключений](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)можно попробовать пользователей за пределами Office 365.</span><span class="sxs-lookup"><span data-stu-id="cf3fb-p109">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="cf3fb-138">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="cf3fb-138">For more information</span></span>

[<span data-ttu-id="cf3fb-139">Реагирование на запись атаке электронной почты</span><span class="sxs-lookup"><span data-stu-id="cf3fb-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="cf3fb-140">Настройка политики защиты от нежелательной почты для исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="cf3fb-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="cf3fb-141">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="cf3fb-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="cf3fb-142">Разрешения в центре соответствия требованиям & безопасности Office 365</span><span class="sxs-lookup"><span data-stu-id="cf3fb-142">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

  

