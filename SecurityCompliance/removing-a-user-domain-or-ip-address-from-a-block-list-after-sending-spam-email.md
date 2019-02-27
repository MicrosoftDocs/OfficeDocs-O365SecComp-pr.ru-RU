---
title: Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений
ms.author: tracyp
author: MSFTTracyP
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
ms.collection:
- M365-security-compliance
description: 'Если пользователь постоянно рассылает из Office 365 нежелательную почту, он может лишиться возможности отправлять сообщения. '
ms.openlocfilehash: 870e5eabca9e799dfca1e99846a5bfe845f65df4
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275940"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="38b20-103">Удаление пользователя, домена или IP-адреса из списка блокировок после отправки нежелательных сообщений</span><span class="sxs-lookup"><span data-stu-id="38b20-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="38b20-p101">Если пользователь постоянно отправляет сообщения электронной почты из Office 365, которое классифицируется как нежелательная почта, отправка сообщений будет заблокирована. Пользователь будет указан в службе как недопустимый исходящий отправитель и будет получать отчет о недоСтавке (NDR), в котором говорится о том, что:</span><span class="sxs-lookup"><span data-stu-id="38b20-p101">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages. The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="38b20-p102">Не удалось доставить сообщение, так как вы не распознаны как допустимый отправитель. Наиболее распространенной причиной этого является то, что ваш адрес электронной почты может отсылать нежелательную почту и больше не может отправлять сообщения за пределом вашей организации. Обратитесь за помощью к администратору электронной почты.  Удаленному серверу возвращено "550 5.1.8 доступ запрещен, недопустимый исходящий отправитель"</span><span class="sxs-lookup"><span data-stu-id="38b20-p102">Your message couldn't be delivered because you weren't recognized as a valid sender. The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization. Contact your email admin for assistance.  Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

<span data-ttu-id="38b20-110">Кроме того, администраторы клиента получат оповещение о том, что пользователю запрещено отправлять больше исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="38b20-110">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="38b20-111">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="38b20-111">What do you need to know before you begin?</span></span>
<span data-ttu-id="38b20-112"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="38b20-112"></span></span>

<span data-ttu-id="38b20-113">Предполагаемое время для завершения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="38b20-113">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="38b20-p103">Перед выполнением этой процедуры или процедур необходимо назначить разрешения. Чтобы просмотреть необходимые разрешения, обратитесь к разделу "Защита от нежелательной почты" в разделе [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="38b20-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="38b20-p104">Следующую процедуру также можно выполнить с помощью удаленной оболочки PowerShell. Используйте командлет Get – Блоккедсендераддресс, чтобы получить список пользователей с ограниченным доступом и reMove — Блоккедсендераддресс для удаления ограничения. Чтобы узнать, как использовать Windows PowerShell для подключения к Exchange Online, ознакомьтесь [со статьЕй подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="38b20-p104">The following procedure can also be performed via remote PowerShell. Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="38b20-119">Удаление ограничений для заблокированной учетной записи электронной почты Office 365</span><span class="sxs-lookup"><span data-stu-id="38b20-119">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="38b20-p105">Эту задачу можно выполнить в центре безопасности _Амп_ по безопасности Office 365 (SCC). Чтобы узнать больше об SCC [, перейдите в центр безопасности _амп_ по безопасности Office 365](go-to-the-securitycompliance-center.md) . Для выполнения этих функций необходимо находиться в группе " **Управление организацией** " или "роль **администратора безопасности** ". Чтобы получить дополнительные сведения о группах ролей SCC [, перейдите в раздел "разрешения" в центре безопасности _амп_ по безопасности Office 365](permissions-in-the-security-and-compliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="38b20-p105">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC. You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions. [Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="38b20-124">С помощью рабочей или учебной учетной записи, имеющей права глобального администратора Office 365, войдите в центр безопасности и соответствия требованиям Office 365, а затем в списке слева разверните узел **Управление угрозами**, выберите пункт **Просмотр**, а затем выберите пункт ограниченный доступ. \*\* Пользователи\*\*.</span><span class="sxs-lookup"><span data-stu-id="38b20-124">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="38b20-125">Чтобы перейти непосредственно к странице " **Пользователи с ограниченНым доступом** " (ранее известной как "центр &amp; уведомлений") в центре безопасности и соответствия требованиям, используйте следующий URL-адрес: _гт_[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="38b20-125">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="38b20-p106">На этой странице будет содержаться список пользователей, которым запрещено отправлять почту извне организации.  Найдите пользователя, для которого необходимо удалить ограничения, а затем нажмите кнопку **разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="38b20-p106">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="38b20-128">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="38b20-128">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="38b20-p107">Существует предельное количество случаев, когда администратор клиента разблокирует учетную запись. Если превышено ограничение для пользователя, отображается сообщение об ошибке. Затем необходимо обратиться в службу поддержки, чтобы разблокировать пользователя.</span><span class="sxs-lookup"><span data-stu-id="38b20-p107">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span><br/><br/> <span data-ttu-id="38b20-131">Для разблокировки пользователя может потребоваться до 1 часа.</span><span class="sxs-lookup"><span data-stu-id="38b20-131">It may take up to 1 hour before the user is unblocked.</span></span>
  
## <a name="third-party-block-lists"></a><span data-ttu-id="38b20-132">Сторонние списки блокировок</span><span class="sxs-lookup"><span data-stu-id="38b20-132">Third-party block lists</span></span>

<span data-ttu-id="38b20-p108">В Exchange Online Protection также используются сторонние списки блокировок, которые помогают принимать решения при фильтрации нежелательной почты. Пользователи, веб-сайты, домены и IP-адреса можно добавлять к заблокированным спискам только для появления нежелательных сообщений. Как администратор Office 365, вы должны попытаться удалить эти объекты из сторонних поставщиков списков, если они принадлежат вам.</span><span class="sxs-lookup"><span data-stu-id="38b20-p108">Exchange Online Protection also uses third-party block lists to help make decisions in spam filtering. Users, websites, domains, and IP addresses can be added to block lists just for appearing in a spam message. As the Office 365 admin, you should try to get these objects removed from the third-party list providers if they belong to you.</span></span>

> [!NOTE]
> <span data-ttu-id="38b20-p109">Если кто-то за пределами Office 365 не может отправлять сообщения в вашу учетную запись Office 365, их учетные записи могут находиться в списке внешние Заблокированные отправители. Пользователи, не входящие в Office 365, могут попытаться удалить себя с помощью [портала самостоятельного](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis)удаления из списка.</span><span class="sxs-lookup"><span data-stu-id="38b20-p109">If someone outside Office 365 cannot send messages to your Office 365 account, their account may be on the external blocked senders list. Users outside Office 365 can try to remove themselves by using the [self-service delisting portal](https://docs.microsoft.com/en-us/office365/SecurityCompliance/use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis).</span></span> 

## <a name="for-more-information"></a><span data-ttu-id="38b20-138">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="38b20-138">For more information</span></span>

[<span data-ttu-id="38b20-139">Реагирование на скомпрометированную учетную запись электронной почты</span><span class="sxs-lookup"><span data-stu-id="38b20-139">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="38b20-140">Настройка политики защиты от нежелательной почты для исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="38b20-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="38b20-141">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="38b20-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="38b20-142">Разрешения в центре безопасности Office 365 _Амп_ соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="38b20-142">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

  

