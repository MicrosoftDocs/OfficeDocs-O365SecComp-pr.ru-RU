---
title: Непроверенный отправитель
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Чтобы предотвратить доступ к почтовому ящику с помощью фишинговых сообщений, Outlook.com и Outlook в Интернете убедитесь, что отправитель говорят, что они говорят о них и помечают подозрительные сообщения как нежелательная почта.
ms.openlocfilehash: 92458a93a4da3e449061e4d2a4ba312d635c42cc
ms.sourcegitcommit: 7f00f765e8fa674ce1c8c66f5b89b6bea45e13ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2019
ms.locfileid: "34341627"
---
# <a name="unverified-sender"></a><span data-ttu-id="0fbdd-103">Непроверенный отправитель</span><span class="sxs-lookup"><span data-stu-id="0fbdd-103">Unverified Sender</span></span>

<span data-ttu-id="0fbdd-104">Чтобы предотвратить доступ к почтовому ящику с помощью фишинговых сообщений, Outlook.com и Outlook в Интернете убедитесь, что отправитель говорят, что они говорят о них и помечают подозрительные сообщения как нежелательная почта.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-104">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0fbdd-105">Если сообщение помечено как фишинг, в Outlook.com и Outlook в Интернете отображается предупреждение в верхней части страницы, но все ссылки в сообщении все равно могут быть открыты.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-105">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="0fbdd-106">Как определить подозрительные сообщения в папке "Входящие"?</span><span class="sxs-lookup"><span data-stu-id="0fbdd-106">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="0fbdd-107">Outlook.com и Outlook в Интернете показывают индикаторы, когда отправитель сообщения не может быть идентифицирован или его удостоверение отличается от того, что отображается в адресе отправителя.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-107">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a><span data-ttu-id="0fbdd-108">Как управлять сообщениями, принимающими непроверенные отправители</span><span class="sxs-lookup"><span data-stu-id="0fbdd-108">How to manage which messages receive the unverified sender treatment</span></span> 

<span data-ttu-id="0fbdd-109">Если вы являетесь клиентом Office 365, вы можете управлять этим компонентом с помощью центра безопасности _Амп_ соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-109">If you are an Office 365 customer you can manage this feature through the Security & Compliance Center.</span></span> 

- <span data-ttu-id="0fbdd-110">В центре безопасности _Амп_ по безопасности Office 365 Администраторы клиентов могут включать или отключать функцию с помощью защиты от спуфинга в политике защиты от фишинга.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-110">In the Office 365 Security & Compliance Center, tenant admins can turn the feature on, or off, through the Anti-spoofing protection under the Anti-Phish policy.</span></span> <span data-ttu-id="0fbdd-111">Кроме того, управлять ими можно с помощью командлета "Set – AntiPhishPolicy".</span><span class="sxs-lookup"><span data-stu-id="0fbdd-111">Additionally, it can be managed through the ‘Set-AntiPhishPolicy’ cmdlet.</span></span> <span data-ttu-id="0fbdd-112">Более подробную информацию можно узнать в статье Защита от фишинга в Office 365 и Set-AntiPhishPolicy.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-112">For more details, see Anti-phishing protection in Office 365 and Set-AntiPhishPolicy.</span></span>

    ![Изменение отправителя, не прошедшего проверку подлинности, в графическом интерфейсе.](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- <span data-ttu-id="0fbdd-114">Если администратор определил ложное срабатывание, а отправитель не может получить непроверенный отправитель, он может выполнить одно из следующих действий, чтобы добавить отправителя в список разрешенных поддельных поддельных поддельных поддельных поддельных подделки:</span><span class="sxs-lookup"><span data-stu-id="0fbdd-114">If an admin has identified a false positive, and a sender should not be receiving the unverified sender treatment they can take one of the following actions to add the sender to the Spoof Intelligence spoof allow list:</span></span>
        
    - <span data-ttu-id="0fbdd-115">Добавьте доменную связь с помощью анализа сведений о подделких.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-115">Add the domain pair through the Spoof Intelligence Insight.</span></span> <span data-ttu-id="0fbdd-116">Для получения дополнительных сведений см. Пошаговое руководство по подделке анализа</span><span class="sxs-lookup"><span data-stu-id="0fbdd-116">For more details, see Walkthrough: spoof intelligence insight</span></span>
                
    - <span data-ttu-id="0fbdd-117">Добавьте доменную комбинацию с помощью командлета PhishFilterPolicy.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-117">Add the domain pair through the PhishFilterPolicy cmdlet.</span></span> <span data-ttu-id="0fbdd-118">Дополнительные сведения: Set – PhishFilterPolicy и защита от спуфинга в Office 365</span><span class="sxs-lookup"><span data-stu-id="0fbdd-118">For more details, see Set-PhishFilterPolicy and Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="0fbdd-119">Кроме того, мы не применяем непроверенный отправитель, если он был доставлен в папку "Входящие" с помощью списка разрешений администратора, включая правила транспорта электронной почты (ETR), список надежных доменов (политика защиты от нежелательной почты), список надежных отправителей или пользователь установил в качестве этого пользователя "надежный отправитель". папке Входящие ".</span><span class="sxs-lookup"><span data-stu-id="0fbdd-119">Additionally, we do not apply the unverified sender treatment if it was delivered to the inbox via an admin allow list, including Email Transport Rules (ETRs), Safe Domain List (Anti-Spam Policy), Safe Sender List or a user has set this user as a “Safe Sender” in their inbox.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="0fbdd-120">Отображается значок "?" в изображении отправителя</span><span class="sxs-lookup"><span data-stu-id="0fbdd-120">You see a '?' in the sender image</span></span>

<span data-ttu-id="0fbdd-121">Когда Outlook.com и Outlook в Интернете не могут проверить подлинность отправителя с помощью методов проверки подлинности электронной почты, в фотографии отправителя отображается "?".</span><span class="sxs-lookup"><span data-stu-id="0fbdd-121">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span> 

![Сообщение не прошел проверку](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="0fbdd-123">Не все сообщения, которые не прошли проверку подлинности, являются вредоносными.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-123">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="0fbdd-124">Однако следует быть внимательным при взаимодействии с сообщениями, которые не прошли проверку подлинности, если вы не распознаете отправителя.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-124">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="0fbdd-125">Или, если вы распознаете отправителя, который обычно не содержит "?" в изображении отправителя, но вы неожиданно видите его, это может быть подписание отправителя.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-125">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="0fbdd-126">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="0fbdd-126">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="0fbdd-127">Какие условия Outlook.com и Outlook в Интернете используют для добавления свойств "?" и "Via"?</span><span class="sxs-lookup"><span data-stu-id="0fbdd-127">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="0fbdd-128">Для "?" в образе отправителя: Outlook.com требует, чтобы сообщение передавало либо проверку подлинности SPF, либо проверку подлинности DKIM.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-128">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="0fbdd-129">Дополнительные сведения см. в статье [Set up SPF in Office 365, чтобы предотвратить спуфинг](set-up-spf-in-office-365-to-help-prevent-spoofing.md) и [использовать DKIM для проверки исходящей электронной почты, отправленной из личного домена в Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="0fbdd-129">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="0fbdd-130">Для тега Via: Если домен, указанный в адресе отправителя, отличается от домена в подписи DKIM или в SMTP-почте FROM, Outlook.com отображает домен в одном из этих двух полей (предложив подпись DKIM).</span><span class="sxs-lookup"><span data-stu-id="0fbdd-130">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="how-do-i-remove-the-"></a><span data-ttu-id="0fbdd-131">Как удалить "?"</span><span class="sxs-lookup"><span data-stu-id="0fbdd-131">How do I remove the '?'</span></span>

<span data-ttu-id="0fbdd-132">Для "?" в изображении отправителя: в качестве отправителя необходимо проверить подлинность сообщения с помощью SPF или DKIM.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-132">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="0fbdd-133">Для тега Via: в качестве отправителя необходимо убедиться, что домен в подписи DKIM или SMTP-почте — то же, что и, или является поддоменом домена, в адресе отправителя.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-133">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="0fbdd-134">Выполняет ли Outlook.com и Outlook в Интернете показывать это значение для каждого сообщения, которое не проходит проверку подлинности?</span><span class="sxs-lookup"><span data-stu-id="0fbdd-134">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="0fbdd-135">Не обязательно.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-135">Not necessarily.</span></span> <span data-ttu-id="0fbdd-136">Outlook.com и Outlook в Интернете могут иметь другие свойства в сообщении для проверки подлинности отправителя.</span><span class="sxs-lookup"><span data-stu-id="0fbdd-136">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fbdd-137">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0fbdd-137">Related topics</span></span>

[<span data-ttu-id="0fbdd-138">Защитите свою учетную запись электронной почты Outlook.com</span><span class="sxs-lookup"><span data-stu-id="0fbdd-138">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="0fbdd-139">Работа с нарушениями, фишингом и подменой в Outlook.com</span><span class="sxs-lookup"><span data-stu-id="0fbdd-139">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="0fbdd-140">Фильтрация нежелательной почты и спама в Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="0fbdd-140">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
