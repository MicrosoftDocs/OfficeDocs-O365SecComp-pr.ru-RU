---
title: Удаление пользователя из портала "ограниченные пользователи" после отправки нежелательной почты
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/12/2019
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter.Restricted.Users.RestrictedUsers
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
ms.collection:
- M365-security-compliance
description: Если пользователь постоянно отправляет электронные письма от Office 365, которые классифицируются как спам, они не смогут отправлять сообщения.
ms.openlocfilehash: c775887ecfa136bd638d0b76050c7882a6219ae4
ms.sourcegitcommit: f86383dcb9c52352661d51b22617f1809445beaa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/14/2019
ms.locfileid: "30573523"
---
# <a name="removing-a-user-from-the-restricted-users-portal-after-sending-spam-email"></a><span data-ttu-id="d2a89-103">Удаление пользователя из портала "ограниченные пользователи" после отправки нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="d2a89-103">Removing a user from the restricted users portal after sending spam email</span></span>

<span data-ttu-id="d2a89-104">Если пользователь непрерывно отправляет электронные письма от Office 365, которые классифицируются как спам, они не смогут отправлять исходящие сообщения.</span><span class="sxs-lookup"><span data-stu-id="d2a89-104">If a user continuously sends emails from Office 365 that are classified as spam, they will be restricted from sending any more messages outbound.</span></span> <span data-ttu-id="d2a89-105">Пользователь будет указан в службе как недопустимый исходящий отправитель и будет получать отчет о недоСтавке (NDR), в котором говорится о том, что:</span><span class="sxs-lookup"><span data-stu-id="d2a89-105">The user will be listed in the service as a bad outbound sender and will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="d2a89-106">Не удалось доставить сообщение, так как вы не распознаны как допустимый отправитель.</span><span class="sxs-lookup"><span data-stu-id="d2a89-106">Your message couldn't be delivered because you weren't recognized as a valid sender.</span></span> <span data-ttu-id="d2a89-107">Наиболее распространенной причиной этого является то, что ваш адрес электронной почты может отсылать нежелательную почту и больше не может отправлять сообщения за пределом вашей организации.</span><span class="sxs-lookup"><span data-stu-id="d2a89-107">The most common reason for this is that your email address is suspected of sending spam and it's no longer allowed to send messages outside of your organization.</span></span> <span data-ttu-id="d2a89-108">Обратитесь за помощью к администратору электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d2a89-108">Contact your email admin for assistance.</span></span> <span data-ttu-id="d2a89-109">Удаленному серверу возвращено "550 5.1.8 доступ запрещен, недопустимый исходящий отправитель"</span><span class="sxs-lookup"><span data-stu-id="d2a89-109">Remote Server returned '550 5.1.8 Access denied, bad outbound sender'</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d2a89-110">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="d2a89-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="d2a89-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="d2a89-111"></span></span>

<span data-ttu-id="d2a89-112">Предполагаемое время для завершения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="d2a89-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="d2a89-113">Для выполнения этих процедур необходимы соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="d2a89-113">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="d2a89-114">Чтобы просмотреть необходимые разрешения, обратитесь к разделу "Защита от нежелательной почты" в разделе [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d2a89-114">To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span>

<span data-ttu-id="d2a89-115">Следующую процедуру также можно выполнить в удаленном сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d2a89-115">The following procedure can also be performed via remote PowerShell.</span></span> <span data-ttu-id="d2a89-116">Используйте командлет Get – Блоккедсендераддресс, чтобы получить список пользователей с ограниченным доступом и reMove — Блоккедсендераддресс для удаления ограничения.</span><span class="sxs-lookup"><span data-stu-id="d2a89-116">Use the Get-BlockedSenderAddress cmdlet to get the list of restricted users and Remove-BlockedSenderAddress to remove the restriction.</span></span> <span data-ttu-id="d2a89-117">Сведения о том, как с помощью Оболочка Windows PowerShell подключаться к Exchange Online, см. в статье [Подключение к PowerShell для Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="d2a89-117">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

## <a name="remove-restrictions-for-a-blocked-office-365-email-account"></a><span data-ttu-id="d2a89-118">Удаление ограничений для заблокированной учетной записи электронной почты Office 365</span><span class="sxs-lookup"><span data-stu-id="d2a89-118">Remove restrictions for a blocked Office 365 email account</span></span>

<span data-ttu-id="d2a89-119">Эту задачу можно выполнить в центре безопасности _Амп_ по безопасности Office 365 (SCC).</span><span class="sxs-lookup"><span data-stu-id="d2a89-119">You complete this task in the Office 365 Security & Compliance Center (SCC).</span></span> <span data-ttu-id="d2a89-120">Чтобы узнать больше об SCC [, перейдите в центр безопасности _амп_ по безопасности Office 365](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a89-120">[Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span> <span data-ttu-id="d2a89-121">Для выполнения этих функций необходимо находиться в группе " **Управление организацией** " или "роль **администратора безопасности** ".</span><span class="sxs-lookup"><span data-stu-id="d2a89-121">You need to be in the **Organization Management** or the **Security Administrator** role group in order to perform these functions.</span></span> <span data-ttu-id="d2a89-122">Чтобы получить дополнительные сведения о группах ролей SCC [, перейдите в раздел "разрешения" в центре безопасности _амп_ по безопасности Office 365](permissions-in-the-security-and-compliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a89-122">[Go to Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) for more details about SCC role groups.</span></span>

1. <span data-ttu-id="d2a89-123">С помощью рабочей или учебной учетной записи, имеющей права глобального администратора Office 365, войдите в центр безопасности и соответствия требованиям Office 365, а затем в списке слева разверните узел **Управление угрозами**, выберите пункт **Просмотр**, а затем выберите пункт ограниченный доступ. \*\* Пользователи\*\*.</span><span class="sxs-lookup"><span data-stu-id="d2a89-123">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="d2a89-124">Чтобы перейти непосредственно к странице " **Пользователи с ограниченНым доступом** " (ранее известной как "центр &amp; уведомлений") в центре безопасности и соответствия требованиям, используйте следующий URL-адрес: _гт_[https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="d2a89-124">To go directly to the **Restricted Users** page (formerly known as the Action Center) in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/#/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="d2a89-125">На этой странице будет содержаться список пользователей, которым запрещено отправлять почту извне организации.</span><span class="sxs-lookup"><span data-stu-id="d2a89-125">This page will contain the list of users that have been blocked from sending mail to outside of your organization.</span></span>  <span data-ttu-id="d2a89-126">Найдите пользователя, для которого необходимо удалить ограничения, а затем нажмите кнопку **разблокировать**.</span><span class="sxs-lookup"><span data-stu-id="d2a89-126">Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="d2a89-127">При выпадающем списке будут извлекаться сведения о учетной записи, для которой запрещено отправку.</span><span class="sxs-lookup"><span data-stu-id="d2a89-127">A fly-out will go into the details about the account whose sending is restricted.</span></span> <span data-ttu-id="d2a89-128">Пройдите по рекомендациям, чтобы убедиться в том, что вы выполняете необходимые действия в случае, если учетная запись на самом деле скомпрометирована.</span><span class="sxs-lookup"><span data-stu-id="d2a89-128">You should go through the recommendations to ensure you're taking the proper actions in case the account is actually compromised.</span></span> <span data-ttu-id="d2a89-129">По завершении нажмите кнопку **Далее** .</span><span class="sxs-lookup"><span data-stu-id="d2a89-129">Click **Next** when done.</span></span>

4. <span data-ttu-id="d2a89-130">Следующий экран содержит рекомендации по предотвращению снижения безопасности в будущем.</span><span class="sxs-lookup"><span data-stu-id="d2a89-130">The next screen has recommendations to help prevent future compromise.</span></span> <span data-ttu-id="d2a89-131">Включение многофакторной проверки подлинности (MFA) и изменение паролей — это хорошая защита.</span><span class="sxs-lookup"><span data-stu-id="d2a89-131">Enabling multi-factor authentication (MFA) and changing the passwords are a good defense.</span></span> <span data-ttu-id="d2a89-132">Щелкните **разблокировать пользователя** по завершении.</span><span class="sxs-lookup"><span data-stu-id="d2a89-132">Click **Unblock user** when done.</span></span>

5. <span data-ttu-id="d2a89-133">Нажмите кнопку **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d2a89-133">Click **Yes** to confirm the change.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2a89-134">Удаление ограничений может занять до 30 минут.</span><span class="sxs-lookup"><span data-stu-id="d2a89-134">It may take up to 30 minutes before restrictions are removed.</span></span> 

## <a name="making-sure-admins-are-alerted-when-this-happens"></a><span data-ttu-id="d2a89-135">Как убедиться, что администраторы уведомляются, когда это произойдет</span><span class="sxs-lookup"><span data-stu-id="d2a89-135">Making sure admins are alerted when this happens</span></span>

<span data-ttu-id="d2a89-136">Кроме того, администраторы клиента получат оповещение о том, что пользователю запрещено отправлять больше исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="d2a89-136">The tenant admins will also receive an alert stating that the user has been restricted from sending any more outbound messages.</span></span> <span data-ttu-id="d2a89-137">Это оповещение по умолчанию, которое предоставляется для всех клиентов и отображается на странице политики оповещений SCC с названием "пользователь не может отправлять электронную почту".</span><span class="sxs-lookup"><span data-stu-id="d2a89-137">It is a default alert that is provided for all tenants and is listed in the SCC Alert policies page, titled "User restricted from sending email".</span></span> <span data-ttu-id="d2a89-138">Перейдите в раздел [политики оповещений в центре безопасности _амп_ по безопасности Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) , чтобы получить дополнительную информацию по оповещению.</span><span class="sxs-lookup"><span data-stu-id="d2a89-138">Go to [Alert policies in the Office 365 Security & Compliance Center](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies) for more information on the alert.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="d2a89-139">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d2a89-139">For more information</span></span>

[<span data-ttu-id="d2a89-140">Реагирование на скомпрометированную учетную запись электронной почты</span><span class="sxs-lookup"><span data-stu-id="d2a89-140">Responding to a compromised email account</span></span>](responding-to-a-compromised-email-account.md)

[<span data-ttu-id="d2a89-141">Общие сведения о пользователе, для которого запрещено отправлять оповещение по электронной почте</span><span class="sxs-lookup"><span data-stu-id="d2a89-141">Understanding the User restricted from sending email alert</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/alert-policies)

[<span data-ttu-id="d2a89-142">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="d2a89-142">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="d2a89-143">Разрешения в центре безопасности Office 365 _Амп_ соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="d2a89-143">Permissions in the Office 365 Security & Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
