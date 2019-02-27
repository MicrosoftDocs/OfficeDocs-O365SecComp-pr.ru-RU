---
title: Незарегистрированный адрес электронной почты домена
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Если вы отправите большой объем незарегистрированного почтового домена, вы получаете риск блокирования электронной почты. Ознакомьтесь с этой статьей, чтобы узнать больше.
ms.openlocfilehash: 8120bd147da2a7aab41ae14c444d2fe57242199e
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276229"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="1f459-104">Незарегистрированный адрес электронной почты домена: что нужно знать</span><span class="sxs-lookup"><span data-stu-id="1f459-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="1f459-p102">Office 365 позволяет клиентам ретранслировать некоторые сообщения через Exchange Online Protection (EOP). Одним из поддерживаемых примеров является то, что пользователи имеют почтовый ящик Office 365, а внешний отправляет сообщения электронной почты, но пересылка электронной почты настроена таким образом, что они передаются обратно во внешний почтовый ящик пользователя. Это наиболее распространенная среда для образования, в которой студенты хотят использовать свой личный интерфейс электронной почты, но по-прежнему получают электронную почту, относящуюся к учебному заведению. Другой пример — когда клиенты находятся в гибридном сценарии и имеют локальные серверы, которые отправляют электронную почту из EOP.</span><span class="sxs-lookup"><span data-stu-id="1f459-p102">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP). One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox. This is most common in education environments where students want to leverage their personal email interface but still get emails related to school. Another example is when customers are in a hybrid scenario and have on-premises servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="1f459-109">Проблемы с незарегистрированными доменами</span><span class="sxs-lookup"><span data-stu-id="1f459-109">Problems with unregistered domains</span></span>

<span data-ttu-id="1f459-p103">Проблема заключается в том, что локальные серверы подвергнуть риску и приступить к ретрансляции большого объема нежелательной почты из EOP. Почти во всех случаях настройка правых соединителей выполняется, но электронная почта отправляется из незарегистрированных, также называемых неподготовленными доменами. Office 365 обеспечивает возможность разумного объема почты от незарегистрированных доменов, но обслуживаемый домен должен быть настроен в центре администрирования для каждого домена, для которого вы планируете отправку.</span><span class="sxs-lookup"><span data-stu-id="1f459-p103">The problem is when on-premises servers get compromised and end up relaying a large volume of spam out of EOP. In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains. Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="1f459-p104">После компрометации клиенты не смогут отправлять исходящую почту для незарегистрированных доменов. Пользователи получат отчет о недоСтавке (NDR), в котором указаны следующие условия.</span><span class="sxs-lookup"><span data-stu-id="1f459-p104">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains. Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="1f459-p105">550 служба 5.7.750 недоступна. Клиент блокировал отправку с незарегистрированных доменов</span><span class="sxs-lookup"><span data-stu-id="1f459-p105">550 5.7.750 Service unavailable. Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="1f459-117">Разблокировка клиента для повторной отправки</span><span class="sxs-lookup"><span data-stu-id="1f459-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="1f459-118">Существует несколько действий, которые необходимо выполнить, если вы блокируете отправку из незарегистрированных доменов:</span><span class="sxs-lookup"><span data-stu-id="1f459-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="1f459-p106">Убедитесь, что зарегистрированы все домены в центре администрирования Office 365. Дополнительные сведения можно найти [здесь](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="1f459-p106">Make sure that you register all of your domains in Office 365 admin center. More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="1f459-p107">Ищите необычные соединители. Вредоносные субъекты часто создают новые входящие соединители в клиенте Office 365 для отправки спама. Дополнительные сведения о проверке соединителей можно найти [здесь](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="1f459-p107">Look for unusual connectors. Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam. More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="1f459-124">ЗаБлокируйте локальные серверы и убедитесь, что они не скомпрометированы.</span><span class="sxs-lookup"><span data-stu-id="1f459-124">Lock down your on-premises servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="1f459-p108">Здесь приводятся многие факторы, особенно если это серверы сторонних производителей. Несмотря на то, что вам потребуется подтвердить, что вся почта, покидает серверы, будет незаконной.</span><span class="sxs-lookup"><span data-stu-id="1f459-p108">There are many factors involved here, especially if these are third-party servers. Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="1f459-p109">После этого вам потребуется позвонить в службу поддержки Майкрософт и попросить предоставить свой клиент незаблокированным для отправки от незарегистрированных доменов.  Указание кода ошибки полезно, но вам необходимо убедиться, что ваша среда защищена, а нежелательная почта не будет отправлена повторно. Дополнительные сведения о том, как открыть обращение в службу поддержки, можно найти [здесь](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="1f459-p109">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.  Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again. More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="1f459-130">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="1f459-130">For more information</span></span>

[<span data-ttu-id="1f459-131">Защита от нежелательной почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="1f459-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="1f459-132">Отчеты о недоставке сообщений электронной почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="1f459-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="1f459-133">Настройка переадресации электронной почты для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="1f459-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="1f459-134">Как настроить отправку электронной почты с помощью Office 365 на многофункциональном устройстве или в приложении</span><span class="sxs-lookup"><span data-stu-id="1f459-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="1f459-135">[Управление обслуживаемыми доменами в Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="1f459-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
