---
title: Определение подозрительных сообщений в Outlook.com и Outlook в Интернете
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Чтобы предотвратить доступ к почтовому ящику с помощью фишинговых сообщений, Outlook.com и Outlook в Интернете убедитесь, что отправитель говорят, что они говорят о них и помечают подозрительные сообщения как нежелательная почта.
ms.openlocfilehash: edba30bb2ac0f9dc6ebc12db957a518de0c1b543
ms.sourcegitcommit: 9907bebc5f225032f681c4952de0b0be2df278ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345924"
---
# <a name="identify-suspicious-messages-in-outlookcom-and-outlook-on-the-web"></a><span data-ttu-id="81558-103">Определение подозрительных сообщений в Outlook.com и Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="81558-103">Identify suspicious messages in Outlook.com and Outlook on the web</span></span>

<span data-ttu-id="81558-104">Чтобы предотвратить доступ к почтовому ящику с помощью фишинговых сообщений, Outlook.com и Outlook в Интернете убедитесь, что отправитель говорят, что они говорят о них и помечают подозрительные сообщения как нежелательная почта.</span><span class="sxs-lookup"><span data-stu-id="81558-104">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81558-105">Если сообщение помечено как фишинг, в Outlook.com и Outlook в Интернете отображается предупреждение в верхней части страницы, но все ссылки в сообщении все равно могут быть открыты.</span><span class="sxs-lookup"><span data-stu-id="81558-105">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="81558-106">Как определить подозрительные сообщения в папке "Входящие"?</span><span class="sxs-lookup"><span data-stu-id="81558-106">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="81558-107">Outlook.com и Outlook в Интернете показывают индикаторы, когда отправитель сообщения не может быть идентифицирован или его удостоверение отличается от того, что отображается в адресе отправителя.</span><span class="sxs-lookup"><span data-stu-id="81558-107">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="81558-108">Отображается значок "?" в изображении отправителя</span><span class="sxs-lookup"><span data-stu-id="81558-108">You see a '?' in the sender image</span></span>

<span data-ttu-id="81558-109">Когда Outlook.com и Outlook в Интернете не могут проверить подлинность отправителя с помощью методов проверки подлинности электронной почты, в фотографии отправителя отображается "?".</span><span class="sxs-lookup"><span data-stu-id="81558-109">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span>

![Сообщение не прошел проверку](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="81558-111">Не все сообщения, которые не прошли проверку подлинности, являются вредоносными.</span><span class="sxs-lookup"><span data-stu-id="81558-111">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="81558-112">Однако следует быть внимательным при взаимодействии с сообщениями, которые не прошли проверку подлинности, если вы не распознаете отправителя.</span><span class="sxs-lookup"><span data-stu-id="81558-112">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="81558-113">Или, если вы распознаете отправителя, который обычно не содержит "?" в изображении отправителя, но вы неожиданно видите его, это может быть подписание отправителя.</span><span class="sxs-lookup"><span data-stu-id="81558-113">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a><span data-ttu-id="81558-114">Адрес отправителя отличается от того, который отображается в адресе отправителя</span><span class="sxs-lookup"><span data-stu-id="81558-114">The sender's address is different than what appears in the From address</span></span>

<span data-ttu-id="81558-115">Часто адрес электронной почты, который отображается в сообщении, отличается от того, что отображается в адресе отПравителя.</span><span class="sxs-lookup"><span data-stu-id="81558-115">Frequently, the email address you see in a message is different than what you see in the From address.</span></span> <span data-ttu-id="81558-116">Иногда фишингы пытаются подумать о том, что отправитель отличается от того, кто на самом деле.</span><span class="sxs-lookup"><span data-stu-id="81558-116">Sometimes phishers try to trick you into thinking that the sender is someone other than who they really are.</span></span>

<span data-ttu-id="81558-117">Когда Outlook.com и Outlook в Интернете обнаруживают различие между фактическим адресом отправителя и адресом, указанным на адресе отправителя, он показывает фактическое отправителя с помощью тега Via, который будет подчеркиванием.</span><span class="sxs-lookup"><span data-stu-id="81558-117">When Outlook.com and Outlook on the web detect a difference between the sender's actual address and the address on the From address, they show the actual sender using the via tag, which will be underlined.</span></span>

![непроверенный замещающий текст отправителя](media/unverified-sender-feature1.png)

<span data-ttu-id="81558-119">В этом примере отправляющий домен `suspicious.com` проходит проверку подлинности, но отправитель помещается `unknown@contoso.com` в адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="81558-119">In this example, the sending domain `suspicious.com` is authenticated, but the sender put `unknown@contoso.com` in the From address.</span></span>

<span data-ttu-id="81558-120">Не каждое сообщение с тегом Via является подозрительным.</span><span class="sxs-lookup"><span data-stu-id="81558-120">Not every message with a via tag is suspicious.</span></span> <span data-ttu-id="81558-121">Тем не менее, если сообщение с тегом Via не распознается, следует соблюдать осторожность при взаимодействии с ним.</span><span class="sxs-lookup"><span data-stu-id="81558-121">However, if you don't recognize a message with a via tag, you should be cautious about interacting with it.</span></span>

<span data-ttu-id="81558-122">В Outlook.com и новом Outlook в Интернете вы можете навести указатель мыши на имя или адрес отправителя в списке сообщений, чтобы просмотреть его адрес электронной почты без необходимости открывать сообщение.</span><span class="sxs-lookup"><span data-stu-id="81558-122">In Outlook.com and the new Outlook on the web, you can hover your cursor over a sender's name or address in the message list to see their email address, without needing to open the message.</span></span>

![Начало работы с OneDrive](media/get-started-with-onedrive-message.png)

<span data-ttu-id="81558-124">Как узнать, что вы используете новый Outlook в Интернете?</span><span class="sxs-lookup"><span data-stu-id="81558-124">How do you know if you're using the new Outlook on the web?</span></span> <span data-ttu-id="81558-125">Ознакомьтесь со следующими примерами:</span><span class="sxs-lookup"><span data-stu-id="81558-125">See the following examples:</span></span>

![Outlook и Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a><span data-ttu-id="81558-127">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="81558-127">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="81558-128">Какие условия Outlook.com и Outlook в Интернете используют для добавления свойств "?" и "Via"?</span><span class="sxs-lookup"><span data-stu-id="81558-128">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="81558-129">Для "?" в образе отправителя: Outlook.com требует, чтобы сообщение передавало либо проверку подлинности SPF, либо проверку подлинности DKIM.</span><span class="sxs-lookup"><span data-stu-id="81558-129">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="81558-130">Дополнительные сведения см. в статье [Set up SPF in Office 365, чтобы предотвратить спуфинг](set-up-spf-in-office-365-to-help-prevent-spoofing.md) и [использовать DKIM для проверки исходящей электронной почты, отправленной из личного домена в Office 365](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="81558-130">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="81558-131">Для тега Via: Если домен, указанный в адресе отПравителя, отличается от домена в подписи DKIM или в SMTP-почте FROM, Outlook.com отображает домен в одном из этих двух полей (предложив подпись DKIM).</span><span class="sxs-lookup"><span data-stu-id="81558-131">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a><span data-ttu-id="81558-132">Можно ли переопределить эти свойства с помощью IP-адреса, правила транспорта Exchange разрешить или только надежные отправители?</span><span class="sxs-lookup"><span data-stu-id="81558-132">Can I override these properties with IP Allows, Exchange Transport Rule Allows, or safe senders?</span></span>

<span data-ttu-id="81558-133">Вы не можете переопределить эти свойства.</span><span class="sxs-lookup"><span data-stu-id="81558-133">You can't override these properties.</span></span>

### <a name="how-do-i-remove-these-properties"></a><span data-ttu-id="81558-134">Как удалить эти свойства?</span><span class="sxs-lookup"><span data-stu-id="81558-134">How do I remove these properties?</span></span>

<span data-ttu-id="81558-135">Для "?" в изображении отправителя: в качестве отправителя необходимо проверить подлинность сообщения с помощью SPF или DKIM.</span><span class="sxs-lookup"><span data-stu-id="81558-135">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="81558-136">Для тега Via: в качестве отправителя необходимо убедиться, что домен в подписи DKIM или SMTP-почте — то же, что и, или является поддоменом домена, в адресе отправителя.</span><span class="sxs-lookup"><span data-stu-id="81558-136">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="81558-137">Выполняет ли Outlook.com и Outlook в Интернете показывать это значение для каждого сообщения, которое не проходит проверку подлинности?</span><span class="sxs-lookup"><span data-stu-id="81558-137">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="81558-138">Не обязательно.</span><span class="sxs-lookup"><span data-stu-id="81558-138">Not necessarily.</span></span> <span data-ttu-id="81558-139">Outlook.com и Outlook в Интернете могут иметь другие свойства в сообщении для проверки подлинности отправителя.</span><span class="sxs-lookup"><span data-stu-id="81558-139">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81558-140">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="81558-140">Related topics</span></span>

[<span data-ttu-id="81558-141">Защитите свою учетную запись электронной почты Outlook.com</span><span class="sxs-lookup"><span data-stu-id="81558-141">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="81558-142">Работа с нарушениями, фишингом и подменой в Outlook.com</span><span class="sxs-lookup"><span data-stu-id="81558-142">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="81558-143">Фильтрация нежелательной почты и спама в Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="81558-143">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
