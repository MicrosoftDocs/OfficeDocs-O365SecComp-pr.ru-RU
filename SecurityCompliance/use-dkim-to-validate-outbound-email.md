---
title: Проверка исходящей электронной почты, отправляемой с личного домена в Office 365, с помощью DKIM
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.custom: TN2DMC
search.appverid:
- MET150
ms.assetid: 56fee1c7-dc37-470e-9b09-33fff6d94617
description: Сводка. В этой статье описано, как обеспечить доверие целевых почтовых систем к сообщениям, отправляемым из личного домена, с помощью технологии DKIM (DomainKeys Identified Mail) в Office 365.
ms.openlocfilehash: 1bafae2a1e1e5de390fd0b8d81c1cf2513092d8e
ms.sourcegitcommit: 4f776e1cf8872ce90e632d4305cb727d31754767
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/13/2018
ms.locfileid: "27263918"
---
# <a name="use-dkim-to-validate-outbound-email-sent-from-your-custom-domain-in-office-365"></a><span data-ttu-id="83abd-103">Проверка исходящей электронной почты, отправляемой с личного домена в Office 365, с помощью DKIM</span><span class="sxs-lookup"><span data-stu-id="83abd-103">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>

 <span data-ttu-id="83abd-104">**Сводка.** В этой статье описано, как обеспечить доверие целевых почтовых систем к сообщениям, отправляемым из личного домена, с помощью технологии DKIM (DomainKeys Identified Mail) в Office 365.</span><span class="sxs-lookup"><span data-stu-id="83abd-104">**Summary:** This article describes how you use DomainKeys Identified Mail (DKIM) with Office 365 to ensure that destination email systems trust messages sent from your custom domain.</span></span> 
  
<span data-ttu-id="83abd-p101">Используйте DKIM вместе с инфраструктурой политики отправителей и DMARC, чтобы злоумышленники не могли отправлять сообщения якобы из вашего домена. DKIM позволяет добавлять цифровую подпись в заголовки сообщений электронной почты. Может показаться, что это сложно, но на самом деле все просто. При настройке DKIM вы авторизуете домен, чтобы сопоставить его имя с сообщением электронной почты с помощью криптографической проверки подлинности. С помощью этой цифровой подписи системы электронной почты могут определить, действительно ли входящее сообщение отправлено из вашего домена.</span><span class="sxs-lookup"><span data-stu-id="83abd-p101">You should use DKIM in addition to SPF and DMARC to help prevent spoofers from sending messages that look like they are coming from your domain. DKIM lets you add a digital signature to email messages in the message header. Sounds complicated, but it's really not. When you configure DKIM, you authorize your domain to associate, or sign, its name to an email message by using cryptographic authentication. Email systems that receive email from your domain can use this digital signature to help determine if incoming email that they receive is legitimate.</span></span>
  
<span data-ttu-id="83abd-p102">По сути, вы используете закрытый ключ для шифрования заголовков сообщений, отправляемых из домена. В записях DNS домена вы публикуете открытый ключ, с помощью которого принимающие серверы расшифровывают подпись. С помощью открытого ключа они проверяют, действительно ли сообщения отправлены вами, а не злоумышленниками, подделавшими ваш домен.</span><span class="sxs-lookup"><span data-stu-id="83abd-p102">Basically, you use a private key to encrypt the header in your domain's outgoing email. You publish a public key to your domain's DNS records that receiving servers can then use to decode the signature. They use the public key to verify that the messages are really coming from you and not coming from someone spoofing your domain.</span></span>
  
<span data-ttu-id="83abd-p103">Office 365 автоматически настраивает DKIM для исходных доменов. Исходный домен  это домен, созданный при регистрации в службе Office 365, например contoso.onmicrosoft.com. Вам не нужно ничего делать, чтобы настроить DKIM для исходного домена. Дополнительные сведения о доменах см. в разделе [часто задаваемых вопросов](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span><span class="sxs-lookup"><span data-stu-id="83abd-p103">Office 365 automatically sets up DKIM for initial domains. The initial domain is the domain that Office 365 created for you when you signed up with the service, for example, contoso.onmicrosoft.com. You don't need to do anything to set up DKIM for your initial domain. For more information about domains, see [Domains FAQ](https://support.office.com/article/Domains-FAQ-1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
<span data-ttu-id="83abd-p104">Вы также можете не настраивать DKIM для личного домена. В этом случае Office 365 создаст пару ключей — закрытый и открытый, включит подпись с помощью DKIM и настроит политику по умолчанию для личного домена. Этого вполне достаточно для защиты большинства пользователей Office 365. Настраивать DKIM для личного домена вручную следует в таких случаях:</span><span class="sxs-lookup"><span data-stu-id="83abd-p104">You can choose to do nothing about DKIM for your custom domain too. If you do not set up DKIM for your custom domain, Office 365 creates a private and public key pair, enables DKIM signing, and then configures the Office 365 default policy for your custom domain. While this is sufficient coverage for most Office 365 customers, you should manually configure DKIM for your custom domain in the following circumstances:</span></span>
  
- <span data-ttu-id="83abd-120">у вас есть несколько личных доменов в Office 365;</span><span class="sxs-lookup"><span data-stu-id="83abd-120">You have more than one custom domain in Office 365</span></span>
    
- <span data-ttu-id="83abd-121">вы также собираетесь настроить DMARC (рекомендуется);</span><span class="sxs-lookup"><span data-stu-id="83abd-121">You're going to set up DMARC too (recommended)</span></span>
    
- <span data-ttu-id="83abd-122">вам необходим контроль над закрытым ключом;</span><span class="sxs-lookup"><span data-stu-id="83abd-122">You want control over your private key</span></span>
    
- <span data-ttu-id="83abd-123">вам необходимо настроить записи CNAME.</span><span class="sxs-lookup"><span data-stu-id="83abd-123">You want to customize your CNAME records</span></span>
    
- <span data-ttu-id="83abd-124">вам нужно настроить ключи DKIM для сообщений электронной почты со стороннего домена, например при использовании стороннего средства для массовых рассылок.</span><span class="sxs-lookup"><span data-stu-id="83abd-124">You want to set up DKIM keys for email originating out of a third-party domain, for example, if you use a third-party bulk mailer.</span></span>
    
<span data-ttu-id="83abd-125">Содержание</span><span class="sxs-lookup"><span data-stu-id="83abd-125">In this article:</span></span>
  
- [<span data-ttu-id="83abd-126">Преимущества технологии DKIM над инфраструктурой политики отправителей для предотвращения спуфинга в Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-126">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#HowDKIMWorks)
    
- [<span data-ttu-id="83abd-127">Как настроить DKIM в Office 365 вручную</span><span class="sxs-lookup"><span data-stu-id="83abd-127">What you need to do to manually set up DKIM in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365)
    
- [<span data-ttu-id="83abd-128">Настройка DKIM для нескольких личных доменов в Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-128">To configure DKIM for more than one custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMMultiDomain)
    
- [<span data-ttu-id="83abd-129">Как отключить политику подписывания DKIM для личного домена в Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-129">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DisableDKIMSigningPolicy)
    
- [<span data-ttu-id="83abd-130">Настройка по умолчанию для DKIM и Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-130">Default behavior for DKIM and Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior)
    
- [<span data-ttu-id="83abd-131">Как настроить DKIM так, чтобы сторонняя служба могла отправлять сообщения электронной почты от имени вашего личного домена</span><span class="sxs-lookup"><span data-stu-id="83abd-131">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>](use-dkim-to-validate-outbound-email.md#SetUp3rdPartyspoof)
    
- [<span data-ttu-id="83abd-132">Дальнейшие действия: после настройки инфраструктуры политики отправителей для Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-132">Next steps: After you set up DKIM for Office 365</span></span>](use-dkim-to-validate-outbound-email.md#DKIMNextSteps)
    
## <a name="how-dkim-works-better-than-spf-alone-to-prevent-malicious-spoofing-in-office-365"></a><span data-ttu-id="83abd-133">Преимущества технологии DKIM над инфраструктурой политики отправителей для предотвращения спуфинга в Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-133">How DKIM works better than SPF alone to prevent malicious spoofing in Office 365</span></span>
<span data-ttu-id="83abd-134"><a name="HowDKIMWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-134"></span></span>

<span data-ttu-id="83abd-p105">Инфраструктура политики отправителей добавляет сведения в конверт сообщения, а технология DKIM шифрует подпись в заголовке сообщения. При пересылке фрагменты конверта этого сообщения могут быть удалены сервером пересылки. Поскольку цифровая подпись остается в заголовке сообщения, технология DKIM работает даже при пересылке, как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="83abd-p105">SPF adds information to a message envelope but DKIM actually encrypts a signature within the message header. When you forward a message, portions of that message's envelope can be stripped away by the forwarding server. Since the digital signature stays with the email message because it's part of the email header, DKIM works even when a message has been forwarded as shown in the following example.</span></span>
  
![Схема, на которой показана проверка подлинности DKIM: пересланное сообщение не прошло проверку инфраструктурой политики отправителей](media/28f93b4c-97e7-4309-acc4-fd0d2e0e3377.jpg)
  
<span data-ttu-id="83abd-p106">Если бы в этом примере вы опубликовали только запись типа TXT инфраструктуры политики отправителей для домена, почтовый сервер получателя мог бы пометить ваше сообщение как спам, что привело бы к ложному срабатыванию. Добавление DKIM в этом сценарии позволяет снизить количество ложных срабатываний. Так как в технологии DKIM для проверки подлинности используется шифрование с помощью открытого ключа, а не только IP-адресов, она считается более надежным способом проверки подлинности, чем инфраструктура политики отправителей. Рекомендуем использовать обе эти технологии, а также DMARC в вашем развертывании.</span><span class="sxs-lookup"><span data-stu-id="83abd-p106">In this example, if you had only published an SPF TXT record for your domain, the recipient's mail server could have marked your email as spam and generated a false positive result. The addition of DKIM in this scenario reduces false positive spam reporting. Because DKIM relies on public key cryptography to authenticate and not just IP addresses, DKIM is considered a much stronger form of authentication than SPF. We recommend using both SPF and DKIM, as well as DMARC in your deployment.</span></span>
  
<span data-ttu-id="83abd-p107">Подробности: DKIM использует закрытый ключ для вставки зашифрованной подписи в заголовки сообщений. Имя подписывающего домена (или домена исходящей почты) вставляется в заголовок в качестве значения поля **d=**. Проверяющий домен (или домен получателя) затем использует поле **d=** для поиска открытого ключа в DNS и проверки подлинности сообщения. Так сообщение проходит проверку DKIM.</span><span class="sxs-lookup"><span data-stu-id="83abd-p107">The nitty gritty: DKIM uses a private key to insert an encrypted signature into the message headers. The signing domain, or outbound domain, is inserted as the value of the **d=** field in the header. The verifying domain, or recipient's domain, then use the **d=** field to look up the public key from DNS and authenticate the message. If the message is verified, the DKIM check passes.</span></span> 
  
## <a name="what-you-need-to-do-to-manually-set-up-dkim-in-office-365"></a><span data-ttu-id="83abd-147">Как настроить DKIM в Office 365 вручную</span><span class="sxs-lookup"><span data-stu-id="83abd-147">What you need to do to manually set up DKIM in Office 365</span></span>
<span data-ttu-id="83abd-148"><a name="SetUpDKIMO365"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-148"></span></span>

<span data-ttu-id="83abd-149">Настройка DKIM состоит из двух этапов:</span><span class="sxs-lookup"><span data-stu-id="83abd-149">To configure DKIM, you will complete these steps:</span></span>
  
- [<span data-ttu-id="83abd-150">Публикация двух записей CNAME для личного домена в DNS</span><span class="sxs-lookup"><span data-stu-id="83abd-150">Publish two CNAME records for your custom domain in DNS</span></span>](use-dkim-to-validate-outbound-email.md#Publish2CNAME)
    
- [<span data-ttu-id="83abd-151">Включение подписи с помощью DKIM для личного домена в Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-151">Enable DKIM signing for your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md#EnableDKIMinO365)
    
### <a name="publish-two-cname-records-for-your-custom-domain-in-dns"></a><span data-ttu-id="83abd-152">Публикация двух записей CNAME для личного домена в DNS</span><span class="sxs-lookup"><span data-stu-id="83abd-152">Publish two CNAME records for your custom domain in DNS</span></span>
<span data-ttu-id="83abd-153"><a name="Publish2CNAME"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-153"></span></span>

<span data-ttu-id="83abd-p108">Для каждого домена, для которого требуется добавить подпись DKIM в DNS, необходимо опубликовать две записи CNAME. Запись CNAME указывает, что каноническое имя домена является псевдонимом другого доменного имени.</span><span class="sxs-lookup"><span data-stu-id="83abd-p108">For each domain for which you want to add a DKIM signature in DNS, you need to publish two CNAME records. A CNAME record is used by DNS to specify that the canonical name of a domain is an alias for another domain name.</span></span> 
  
 <span data-ttu-id="83abd-p109">Office 365 выполняет автоматическую ротацию ключей, используя две заданные записи. Для каждого дополнительного домена в Office 365 необходимо опубликовать две записи CNAME. Таким образом, если у вас есть два домена, необходимо опубликовать две дополнительные записи CNAME и так далее.</span><span class="sxs-lookup"><span data-stu-id="83abd-p109">Office 365 performs automatic key rotation using the two records that you establish. If you have provisioned custom domains in addition to the initial domain in Office 365, you must publish two CNAME records for each additional domain. So, if you have two domains, you must publish two additional CNAME records, and so on.</span></span>
  
<span data-ttu-id="83abd-159">Используйте следующий формат для записи CNAME.</span><span class="sxs-lookup"><span data-stu-id="83abd-159">Use the following format for the CNAME records.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="83abd-p110">Если вы являетесь одним из наших клиентов GCC, метод domainGUID не будут работать для вас! Убедитесь, что используется правильное значение MX для вашего домена. Использование: `selector2-<domain-key>._domainkey.<initialDomain>` в примере ниже. Используйте [эту статью](https://docs.microsoft.com/en-us/office365/admin/get-help-with-domains/information-for-dns-records?view=o365-worldwide) для поиска MX-записи, необходимые для вашего *домена ключ* значение.</span><span class="sxs-lookup"><span data-stu-id="83abd-p110">If you are one of our GCC customers, the domainGUID method will not work for you! Be sure to use the proper MX value for your domain. Use: `selector2-<domain-key>._domainkey.<initialDomain>` for the examples below. Use [this article](https://docs.microsoft.com/en-us/office365/admin/get-help-with-domains/information-for-dns-records?view=o365-worldwide) to find the MX record needed for your *domain-key* value.</span></span>
  
```
Host name:          selector1._domainkey
Points to address or value: selector1-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: selector2-<domainGUID>._domainkey.<initialDomain> 
TTL:                3600
```

<span data-ttu-id="83abd-164">Где:</span><span class="sxs-lookup"><span data-stu-id="83abd-164">Where:</span></span>
  
- <span data-ttu-id="83abd-165">selector1 и selector2  это селекторы для Office 365.</span><span class="sxs-lookup"><span data-stu-id="83abd-165">For Office 365, the selectors will always be "selector1" or "selector2".</span></span> 
    
- <span data-ttu-id="83abd-p111">_domainGUID_ — это то же, что _domainGUID_ в настраиваемой записи MX для настраиваемого домена, который отображается перед mail.protection.outlook.com. Например в следующую запись MX для домена contoso.com, _domainGUID_ является contoso-com:</span><span class="sxs-lookup"><span data-stu-id="83abd-p111">_domainGUID_ is the same as the _domainGUID_ in the customized MX record for your custom domain that appears before mail.protection.outlook.com. For example, in the following MX record for the domain contoso.com, the _domainGUID_ is contoso-com:</span></span> 
    
    ```
    contoso.com.  3600  IN  MX   5 contoso-com.mail.protection.outlook.com
    ```

- <span data-ttu-id="83abd-p112">_initialDomain_ является домен, который использовался во время регистрации для Office 365. Начальное доменов всегда заканчиваться onmicrosoft.com. Сведения об определении начальной домена видеть [Домены вопросы и ответы](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span><span class="sxs-lookup"><span data-stu-id="83abd-p112">_initialDomain_ is the domain that you used when you signed up for Office 365. Initial domains always end in onmicrosoft.com. For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
    
<span data-ttu-id="83abd-171">Например, если у вас есть исходный домен cohovineyardandwinery.onmicrosoft.com и два личных домена cohovineyard.com и cohowinery.com, вам необходимо настроить две записи CNAME для каждого дополнительного домена (всего четыре записи CNAME).</span><span class="sxs-lookup"><span data-stu-id="83abd-171">For example, if you have an initial domain of cohovineyardandwinery.onmicrosoft.com, and two custom domains cohovineyard.com and cohowinery.com, you would need to set up two CNAME records for each additional domain, for a total of four CNAME records.</span></span>
  
```
Host name:          selector1._domainkey
Points to address or value: **selector1-cohovineyard-com**._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector2._domainkey
Points to address or value: **selector2-cohovineyard-com**._domainkey.cohovineyardandwinery.onmicrosoft.com
TTL:                3600

Host name:          selector1._domainkey
Points to address or value: **selector1-cohowinery-com**._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
 
Host name:          selector2._domainkey
Points to address or value: **selector2-cohowinery-com**._domainkey.cohovineyardandwinery.onmicrosoft.com 
TTL:                3600
```

### <a name="enable-dkim-signing-for-your-custom-domain-in-office-365"></a><span data-ttu-id="83abd-172">Включение подписи с помощью DKIM для личного домена в Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-172">Enable DKIM signing for your custom domain in Office 365</span></span>
<span data-ttu-id="83abd-173"><a name="EnableDKIMinO365"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-173"></span></span>

<span data-ttu-id="83abd-p113">После публикации записей CNAME в DNS включите подпись с помощью DKIM в Office 365. Это можно сделать в Центре администрирования Office 365 или с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83abd-p113">Once you have published the CNAME records in DNS, you are ready to enable DKIM signing through Office 365. You can do this either through the Office 365 admin center or by using PowerShell.</span></span>
  
#### <a name="to-enable-dkim-signing-for-your-custom-domain-through-the-office-365-admin-center"></a><span data-ttu-id="83abd-176">Как включить подпись с помощью DKIM для личного домена в Центре администрирования Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-176">To enable DKIM signing for your custom domain through the Office 365 admin center</span></span>

1. <span data-ttu-id="83abd-177">[Войдите в Office 365](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) с помощью рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="83abd-177">[Sign in to Office 365](https://support.office.microsoft.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) with your work or school account.</span></span> 
    
2. <span data-ttu-id="83abd-178">В левом верхнем углу выберите значок запуска приложений и выберите элемент **Администратор**.</span><span class="sxs-lookup"><span data-stu-id="83abd-178">Select the app launcher icon in the upper-left and choose **Admin**.</span></span>
    
3. <span data-ttu-id="83abd-179">В области навигации слева внизу разверните узел **Администратор** и выберите элемент **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="83abd-179">In the lower-left navigation, expand **Admin** and choose **Exchange**.</span></span>
    
4. <span data-ttu-id="83abd-180">Перейдите в раздел **Защита** \> **dkim**.</span><span class="sxs-lookup"><span data-stu-id="83abd-180">Go to **Protection** \> **dkim**.</span></span>
    
5. <span data-ttu-id="83abd-p114">Выберите домен, для которого требуется включить DKIM, а затем в разделе **Добавлять подписи DKIM в сообщения для этого домена** нажмите **Включить**. Повторите этот шаг для каждого личного домена.</span><span class="sxs-lookup"><span data-stu-id="83abd-p114">Select the domain for which you want to enable DKIM and then, for **Sign messages for this domain with DKIM signatures**, choose **Enable**. Repeat this step for each custom domain.</span></span>
    
#### <a name="to-enable-dkim-signing-for-your-custom-domain-by-using-powershell"></a><span data-ttu-id="83abd-183">Как включить подпись с помощью DKIM для личного домена, используя PowerShell</span><span class="sxs-lookup"><span data-stu-id="83abd-183">To enable DKIM signing for your custom domain by using PowerShell</span></span>

1. <span data-ttu-id="83abd-184">[Подключение к Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="83abd-184">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>
    
2. <span data-ttu-id="83abd-185">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="83abd-185">Run the following command:</span></span>
    
    ```
    New-DkimSigningConfig -DomainName <domain> -Enabled $true
    ```

   <span data-ttu-id="83abd-186">Где _домен_ — это имя настраиваемого домена, который вы хотите включить ПРОВЕРКУ подписи для.</span><span class="sxs-lookup"><span data-stu-id="83abd-186">Where _domain_ is the name of the custom domain that you want to enable DKIM signing for.</span></span> 
    
   <span data-ttu-id="83abd-187">Например, для домена contoso.com:</span><span class="sxs-lookup"><span data-stu-id="83abd-187">For example, for the domain contoso.com:</span></span>
    
    ```
    New-DkimSigningConfig -DomainName contoso.com -Enabled $true
    ```

#### <a name="to-confirm-dkim-signing-is-configured-properly-for-office-365"></a><span data-ttu-id="83abd-188">Как проверить настройку подписи с помощью DKIM для Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-188">To Confirm DKIM signing is configured properly for Office 365</span></span>

<span data-ttu-id="83abd-p115">Прежде чем выполнять указанные ниже действия для проверки настройки DKIM, подождите несколько минут. Для распространения информации DKIM о домене по сети требуется время.</span><span class="sxs-lookup"><span data-stu-id="83abd-p115">Wait a few minutes before you follow these steps to confirm that you have properly configured DKIM. This allows time for the DKIM information about the domain to be spread throughout the network.</span></span>
  
- <span data-ttu-id="83abd-191">Отправьте сообщение из учетной записи в вашем домене Office 365 с включенной проверкой DKIM в другую учетную запись электронной почты, например outlook.com или Hotmail.com.</span><span class="sxs-lookup"><span data-stu-id="83abd-191">Send a message from an account within your Office 365 DKIM-enabled domain to another email account such as outlook.com or Hotmail.com.</span></span>
    
- <span data-ttu-id="83abd-p116">Не используйте для проверки учетную запись aol.com. AOL может пропустить проверку DKIM в случае успешной проверки SPF. Такая проверка будет недействительной.</span><span class="sxs-lookup"><span data-stu-id="83abd-p116">Do not use an aol.com account for testing purposes. AOL may skip the DKIM check if the SPF check passes. This will nullify your test.</span></span>
    
- <span data-ttu-id="83abd-p117">Откройте сообщение и посмотрите на заголовок. Инструкции по просмотру заголовка сообщения зависят от вашего почтового клиента. Инструкции по просмотру заголовков сообщений в Outlook см. в статье [Просмотр заголовков сообщений электронной почты](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C).</span><span class="sxs-lookup"><span data-stu-id="83abd-p117">Open the message and look at the header. Instructions for viewing the header for the message will vary depending on your messaging client. For instructions on viewing message headers in Outlook, see [View e-mail message headers](https://support.office.com/article/CD039382-DC6E-4264-AC74-C048563D212C).</span></span>

  <span data-ttu-id="83abd-p118">Сообщение, подписанное с помощью DKIM, будет содержать имя узла и доменное имя, указанные вами при публикации записей CNAME. Сообщение будет выглядеть примерно так:</span><span class="sxs-lookup"><span data-stu-id="83abd-p118">The DKIM-signed message will contain the host name and domain you defined when you published the CNAME entries. The message will look something like this example:</span></span> 
    
    ```
    From: Example User <example@contoso.com> 
    DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
        s=selector1; d=contoso.com; t=1429912795; 
        h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
        bh=<body hash>; 
        b=<signed field>;
    ```

- <span data-ttu-id="83abd-p119">Найдите заголовок Authentication-Results. Принимающие службы помечают входящую почту по-разному, но результат должен содержать элемент, подобный **DKIM=pass** или **DKIM=OK**.</span><span class="sxs-lookup"><span data-stu-id="83abd-p119">Look for the Authentication-Results header. While each receiving service uses a slightly different format to stamp the incoming mail, the result should include something like **DKIM=pass** or **DKIM=OK**.</span></span> 
    
## <a name="to-configure-dkim-for-more-than-one-custom-domain-in-office-365"></a><span data-ttu-id="83abd-202">Настройка DKIM для нескольких личных доменов в Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-202">To configure DKIM for more than one custom domain in Office 365</span></span>
<span data-ttu-id="83abd-203"><a name="DKIMMultiDomain"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-203"></span></span>

<span data-ttu-id="83abd-p120">Действия, описанные в этой статье, необходимо выполнить для каждого дополнительного личного домена, для которого требуется включить DKIM. В частности, выполните все действия, описанные в разделе [Как настроить DKIM в Office 365 вручную](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span><span class="sxs-lookup"><span data-stu-id="83abd-p120">If at some point in the future you decide to add another custom domain and you want to enable DKIM for the new domain, you must complete the steps in this article for each domain. Specifically, complete all steps in [What you need to do to manually set up DKIM in Office 365](use-dkim-to-validate-outbound-email.md#SetUpDKIMO365).</span></span>
  
## <a name="disabling-the-dkim-signing-policy-for-a-custom-domain-in-office-365"></a><span data-ttu-id="83abd-206">Как отключить политику подписывания DKIM для личного домена в Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-206">Disabling the DKIM signing policy for a custom domain in Office 365</span></span>
<span data-ttu-id="83abd-207"><a name="DisableDKIMSigningPolicy"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-207"></span></span>

<span data-ttu-id="83abd-p121">Отключение политики подписывания полностью не отключает DKIM. Через некоторое время служба Office 365 автоматически применит политику Office 365 по умолчанию для вашего домена. Дополнительные сведения см. в разделе [Настройка по умолчанию для DKIM и Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span><span class="sxs-lookup"><span data-stu-id="83abd-p121">Disabling the signing policy does not completely disable DKIM. After a period of time, Office 365 will automatically apply the default Office 365 policy for your domain. For more information, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
### <a name="to-disable-the-dkim-signing-policy-by-using-windows-powershell"></a><span data-ttu-id="83abd-211">Отключение политики подписывания DKIM с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="83abd-211">To disable the DKIM signing policy by using Windows PowerShell</span></span>

1. <span data-ttu-id="83abd-212">[Подключение к Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span><span class="sxs-lookup"><span data-stu-id="83abd-212">[Connect to Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289.aspx).</span></span>
    
2. <span data-ttu-id="83abd-213">Выполните одну из указанных ниже команд для каждого домена, для которого требуется отключить подпись с помощью DKIM.</span><span class="sxs-lookup"><span data-stu-id="83abd-213">Run one of the following commands for each domain for which you want to disable DKIM signing.</span></span>
    
    ```
    $p=Get-DkimSigningConfig -identity <domain>
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   <span data-ttu-id="83abd-214">Пример:</span><span class="sxs-lookup"><span data-stu-id="83abd-214">For example:</span></span>
    
    ```
    $p=Get-DkimSigningConfig -identity contoso.com
    $p[0] | set-DkimSigningConfig -enabled $false
    ```

   <span data-ttu-id="83abd-215">или</span><span class="sxs-lookup"><span data-stu-id="83abd-215">Or</span></span>
    
    ```
    Set-DkimSigningConfig -identity $p[<number>].identity -enabled $false
    ```

    <span data-ttu-id="83abd-p122">Где _number_ — это индекс политики. Например:</span><span class="sxs-lookup"><span data-stu-id="83abd-p122">Where _number_ is the index of the policy. For example:</span></span> 
    
    ```
    Set-DkimSigningConfig -identity $p[0].identity -enabled $false
    ```

## <a name="default-behavior-for-dkim-and-office-365"></a><span data-ttu-id="83abd-218">Настройка по умолчанию для DKIM и Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-218">Default behavior for DKIM and Office 365</span></span>
<span data-ttu-id="83abd-219"><a name="DefaultDKIMbehavior"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-219"></span></span>

<span data-ttu-id="83abd-p123">Если вы не включите DKIM, Office 365 автоматически создаст 1024-разрядный открытый ключ DKIM для вашего личного домена и соответствующий закрытый ключ, которые хранятся в нашем центре обработки данных. Для доменов без действующей политики Office 365 использует конфигурацию подписывания по умолчанию. Это означает, что если вы не настроите DKIM самостоятельно, Office 365 включит DKIM для вашего домена, используя политику по умолчанию и созданные ключи.</span><span class="sxs-lookup"><span data-stu-id="83abd-p123">If you do not enable DKIM, Office 365 automatically creates a 1024-bit DKIM public key for your custom domain and the associated private key which we store internally in our datacenter. By default, Office 365 uses a default signing configuration for domains that do not have a policy in place. This means that if you do not set up DKIM yourself, Office 365 will use its default policy and keys it creates in order to enable DKIM for your domain.</span></span>
  
<span data-ttu-id="83abd-223">Кроме того, если вы отключите подпись с помощью DKIM, то через некоторое время Office 365 автоматически включит для вашего домена политику по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83abd-223">Also, if you disable DKIM signing after enabling it, after a period of time, Office 365 will automatically apply the Office 365 default policy for your domain.</span></span>
  
<span data-ttu-id="83abd-p124">Предположим, что в примере ниже подпись DKIM для домена fabrikam.com включил Office 365, а не администратор домена. Это означает, что в службе DNS нет требуемых записей CNAME. Подписи DKIM для электронной почты из этого домена будут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="83abd-p124">In the following example, suppose that DKIM for fabrikam.com was enabled by Office 365, not by the administrator of the domain. This means that the required CNAMEs do not exist in DNS. DKIM signatures for email from this domain will look something like this:</span></span>
  
```
From: Second Example <second.example@fabrikam.com> 
DKIM-Signature: v=1; a=rsa-sha256; q=dns/txt; c=relaxed/relaxed; 
    s=selector1-fabrikam-com; d=contoso.onmicrosoft.com; t=1429912795; 
    h=From:To:Message-ID:Subject:MIME-Version:Content-Type; 
    bh=<body hash>; 
    b=<signed field>;
```

<span data-ttu-id="83abd-p125">В этом примере имя узла и доменное имя содержат значения, на которые указывала бы запись CNAME, если бы администратор домена настроил подпись DKIM для домена fabrikam.com. Каждое сообщение, отправленное из Office 365, будет подписано с помощью DKIM. Если вы включили DKIM самостоятельно, то домен будет совпадать с доменом, указанным в адресе отправителя (в этом случае  fabrikam.com). В противном случае будет использоваться исходный домен организации. О том, как узнать свой исходный домен, читайте в разделе [часто задаваемых вопросов](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span><span class="sxs-lookup"><span data-stu-id="83abd-p125">In this example, the host name and domain contain the values to which the CNAME would point if DKIM-signing for fabrikam.com had been enabled by the domain administrator. Eventually, every single message sent from Office 365 will be DKIM-signed. If you enable DKIM yourself, the domain will be the same as the domain in the From: address, in this case fabrikam.com. If you don't, it will not align and instead will use your organization's initial domain. For information about determining your initial domain, see [Domains FAQ](https://support.office.com/article/1272bad0-4bd4-4796-8005-67d6fb3afc5a#bkmk_whydoihaveanonmicrosoft.comdomain).</span></span>
  
## <a name="set-up-dkim-so-that-a-third-party-service-can-send-or-spoof-email-on-behalf-of-your-custom-domain"></a><span data-ttu-id="83abd-232">Как настроить DKIM так, чтобы сторонняя служба могла отправлять сообщения электронной почты от имени вашего личного домена</span><span class="sxs-lookup"><span data-stu-id="83abd-232">Set up DKIM so that a third-party service can send, or spoof, email on behalf of your custom domain</span></span>
<span data-ttu-id="83abd-233"><a name="SetUp3rdPartyspoof"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-233"></span></span>

<span data-ttu-id="83abd-p126">Некоторые поставщика услуг электронной почты, или поставщики программного обеспечения как службы, позволяют настраивать ключи DKIM для сообщений электронной почты, отправляемых из их службы. Для этого вам необходимо координировать свои действия с третьей стороной, чтобы настроить необходимые записи DNS. В каждой организации это делают по-своему. Процесс полностью зависит от конкретного предприятия.</span><span class="sxs-lookup"><span data-stu-id="83abd-p126">Some bulk email service providers, or software-as-a-service providers, let you set up DKIM keys for email that originates from their service. This requires coordination between yourself and the third-party in order to set up the necessary DNS records. No two organizations do it exactly the same way. Instead, the process depends entirely on the organization.</span></span>
  
<span data-ttu-id="83abd-238">Пример сообщения с правильно настроенными ключами DKIM для доменов contoso.com и bulkemailprovider.com:</span><span class="sxs-lookup"><span data-stu-id="83abd-238">An example message showing a properly configured DKIM for contoso.com and bulkemailprovider.com might look like this:</span></span>
  
```
Return-Path: <communication@bulkemailprovider.com>
 From: <sender@contoso.com>
 DKIM-Signature: s=s1024; d=contoso.com
 Subject: Here is a message from Bulk Email Provider's infrastructure, but with a DKIM signature authorized by contoso.com
```

<span data-ttu-id="83abd-239">В этом примере для достижения представленного результата:</span><span class="sxs-lookup"><span data-stu-id="83abd-239">In this example, in order to achieve this result:</span></span>
  
1. <span data-ttu-id="83abd-240">Поставщик услуг массовой рассылки предоставил компании Contoso открытый ключ DKIM.</span><span class="sxs-lookup"><span data-stu-id="83abd-240">Bulk Email Provider gave Contoso a public DKIM key.</span></span>
    
2. <span data-ttu-id="83abd-241">Компания Contoso опубликовала ключ DKIM в своей записи DNS.</span><span class="sxs-lookup"><span data-stu-id="83abd-241">Contoso published the DKIM key to its DNS record.</span></span>
    
3. <span data-ttu-id="83abd-p127">При отправке сообщения поставщик услуг массовой рассылки подписывает ключ соответствующим закрытым ключом. Таким образом он добавляет подпись DKIM в заголовок сообщения.</span><span class="sxs-lookup"><span data-stu-id="83abd-p127">When sending email, Bulk Email Provider signs the key with the corresponding private key. By doing so, Bulk Email Provider attached the DKIM signature to the message header.</span></span>
    
4. <span data-ttu-id="83abd-p128">Почтовые системы получателей выполняют проверку DKIM путем сравнения значения DKIM-Signature d=\<domain\> с доменом в поле "От" (5322.From) сообщения. В этом примере значения совпадают:</span><span class="sxs-lookup"><span data-stu-id="83abd-p128">Receiving email systems perform a DKIM check by authenticating the DKIM-Signature d=\<domain\> value against the domain in the From: (5322.From) address of the message. In this example, the values match:</span></span>
    
    <span data-ttu-id="83abd-246">Отправитель @**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="83abd-246">sender@**contoso.com**</span></span>
    
    <span data-ttu-id="83abd-247">d =**contoso.com**</span><span class="sxs-lookup"><span data-stu-id="83abd-247">d=**contoso.com**</span></span>
    
## <a name="next-steps-after-you-set-up-dkim-for-office-365"></a><span data-ttu-id="83abd-248">Дальнейшие действия: после настройки инфраструктуры политики отправителей для Office 365</span><span class="sxs-lookup"><span data-stu-id="83abd-248">Next steps: After you set up DKIM for Office 365</span></span>
<span data-ttu-id="83abd-249"><a name="DKIMNextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="83abd-249"></span></span>

<span data-ttu-id="83abd-p129">Хотя ПРОВЕРКУ предназначена для предотвращения спуфинг, ПРОВЕРКУ лучше работает с SPF и DMARC. После настройки ПРОВЕРКУ, если вы еще не настроили копирование SPF это следует сделать. Краткое введение SPF и настройки быстро [Настройка инфраструктуры политики Отправителей в Office 365 для предотвращения спуфинг](set-up-spf-in-office-365-to-help-prevent-spoofing.md)см. Более подробное представление о, как Office 365 использует SPF или устранения неисправностей или нестандартную развертывания, такие как гибридные развертывания начните с [Framework политики отправителя (SPF) для предотвращения спуфинг используется как Office 365](how-office-365-uses-spf-to-prevent-spoofing.md). Рассмотрим процедуру в разделе [DMARC используется для проверки электронной почты в Office 365](use-dmarc-to-validate-email.md). [Заголовки сообщения защиты от нежелательной почты](anti-spam-message-headers.md) включает в себя синтаксис и заголовок поля, используемые в Office 365 для проверки ПРОВЕРКУ.</span><span class="sxs-lookup"><span data-stu-id="83abd-p129">Although DKIM is designed to help prevent spoofing, DKIM works better with SPF and DMARC. Once you have set up DKIM, if you have not already set up SPF you should do so. For a quick introduction to SPF and to get it configured quickly, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md). For a more in-depth understanding of how Office 365 uses SPF, or for troubleshooting or non-standard deployments such as hybrid deployments, start with [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](how-office-365-uses-spf-to-prevent-spoofing.md). Next, see [Use DMARC to validate email in Office 365](use-dmarc-to-validate-email.md). [Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DKIM checks.</span></span> 
  

