---
title: Незарегистрированных домен электронной почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: При отправке большой объем незарегистрированных домен электронной почты, риск блокирования электронной почты. В этой статье, чтобы получить дополнительные сведения.
ms.openlocfilehash: 30d7887be0429195380f2c4ae1a328904dffd69c
ms.sourcegitcommit: 6d72cdb882b93edf6dfddb5ff2e6d8a16e2fa0bc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25596732"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="94457-104">Незарегистрированных домен электронной почты: Что нужно знать</span><span class="sxs-lookup"><span data-stu-id="94457-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="94457-p102">Office 365 позволяет клиентам для ретрансляции некоторых сообщений через Exchange Online Protection (EOP). Поддерживаемые примером это может быть, если у пользователей есть почтовый ящик Office 365 и внешних кто-то отправляет сообщение электронной почты их переадресация почты настроена таким образом, чтобы его возврат в работе внешнего почтового ящика пользователя. Это наиболее распространенные в образовательных учреждений средах, где студентов необходимо использовать свои личные электронной почты интерфейса, но по-прежнему получить сообщения электронной почты, связанные с school. Другой пример заключается в гибридном сценарии клиентов, и локальных серверов, адрес электронной почты из него EOP.</span><span class="sxs-lookup"><span data-stu-id="94457-p102">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP). One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox. This is most common in education environments where students want to leverage their personal email interface but still get emails related to school. Another example is when customers are in a hybrid scenario and have on-premise servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="94457-109">Проблемы с незарегистрированных доменов</span><span class="sxs-lookup"><span data-stu-id="94457-109">Problems with unregistered domains</span></span>

<span data-ttu-id="94457-p103">Проблема возникает, когда локальных серверов компрометации и приходится ретрансляцию большой объем нежелательной почты из него EOP. Почти во всех случаях зависят от выбора справа соединители, но электронной почты отправляется из незарегистрированных, также известной как подготовлено доменов. Office 365 разрешить разумный объем почты из незарегистрированных доменов, но обслуживаемых доменов, необходимо настроить в центре администрирования для каждого домена, на которых планируется отправка об отсутствии на работе.</span><span class="sxs-lookup"><span data-stu-id="94457-p103">The problem is when on-premise servers get compromised and end up relaying a large volume of spam out of EOP. In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains. Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="94457-p104">После атаке, клиенты не сможет отправки исходящей почты для незарегистрированных доменов. Пользователи будут получать Non-недоставке (NDR) о том:</span><span class="sxs-lookup"><span data-stu-id="94457-p104">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains. Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="94457-p105">550 5.7.750 служба недоступна. Клиент запретом Отправка из незарегистрированных доменов</span><span class="sxs-lookup"><span data-stu-id="94457-p105">550 5.7.750 Service unavailable. Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="94457-117">Разблокировка клиента для отправки еще раз</span><span class="sxs-lookup"><span data-stu-id="94457-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="94457-118">Существует несколько моментов, которые необходимо выполнить при блокируются для отправки из незарегистрированных доменов.</span><span class="sxs-lookup"><span data-stu-id="94457-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="94457-p106">Убедитесь в том, что все домены регистрация в центре администрирования Office 365. Дополнительные сведения можно найти [здесь](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="94457-p106">Make sure that you register all of your domains in Office 365 admin center. More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="94457-p107">Найдите нестандартный соединители. Сообщение о нежелательном субъекты часто требуется создавать новые входящие соединители в клиент Office 365 для отправки нежелательных сообщений. Дополнительные сведения о проверке вашей соединителей можно найти [здесь](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="94457-p107">Look for unusual connectors. Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam. More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="94457-124">Заблокировать локальных серверов и убедитесь в том, что они не скомпрометированы.</span><span class="sxs-lookup"><span data-stu-id="94457-124">Lock down your on-premise servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="94457-p108">Существует множество факторов участвующие здесь, особенно если серверы сторонних производителей. Независимо от того, необходимо будет могли убедитесь, что указаны допустимых всех почтовых сообщений, отправляемых из серверов.</span><span class="sxs-lookup"><span data-stu-id="94457-p108">There are many factors involved here, especially if these are third-party servers. Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="94457-p109">После этого необходимо будет вызовов службы поддержки Майкрософт и попросите для получения клиенту разблокировать для отправки из незарегистрированных доменов еще раз.  Предоставление код ошибки будет полезно, но необходимо подтвердить, что обеспечивается безопасность среды и что нежелательной почты не будут отправляться еще раз. Дополнительные сведения об открытии дела поддержки можно найти [здесь](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="94457-p109">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.  Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again. More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="94457-130">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="94457-130">For more information</span></span>

[<span data-ttu-id="94457-131">Office 365 email anti-spam protection</span><span class="sxs-lookup"><span data-stu-id="94457-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="94457-132">Отчеты о недоставке сообщений электронной почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="94457-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="94457-133">Настройка переадресации электронной почты для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="94457-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="94457-134">Настройка многофункционального устройства или приложения для отправки электронной почты с помощью Office 365</span><span class="sxs-lookup"><span data-stu-id="94457-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="94457-135">[Управление обслуживаемые домены и в Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="94457-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
