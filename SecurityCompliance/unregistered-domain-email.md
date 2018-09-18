---
title: Незарегистрированных домен электронной почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: При отправке большой объем незарегистрированных домен электронной почты, риск блокирования электронной почты. В этой статье, чтобы получить дополнительные сведения.
ms.openlocfilehash: f2b60f492197bf0dadb702a1c3f184c2d7e56bf1
ms.sourcegitcommit: 7b85c22fc85ec19e4b44a07e91bfa9ade768185a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2018
ms.locfileid: "23998603"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="e79db-104">Незарегистрированных домен электронной почты: Что нужно знать</span><span class="sxs-lookup"><span data-stu-id="e79db-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="e79db-p102">Office 365 позволяет клиентам для ретрансляции некоторых сообщений через Exchange Online Protection (EOP). Поддерживаемые примером это может быть, если у пользователей есть почтовый ящик Office 365 и внешних кто-то отправляет сообщение электронной почты их переадресация почты настроена таким образом, чтобы его возврат в работе внешнего почтового ящика пользователя. Это наиболее распространенные в образовательных учреждений средах, где студентов необходимо использовать свои личные электронной почты интерфейса, но по-прежнему получить сообщения электронной почты, связанные с school. Другой пример заключается в гибридном сценарии клиентов, и локальных серверов, адрес электронной почты из него EOP.</span><span class="sxs-lookup"><span data-stu-id="e79db-p102">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP). One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox. This is most common in education environments where students want to leverage their personal email interface but still get emails related to school. Another example is when customers are in a hybrid scenario and have on-premise servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="e79db-109">Проблемы с незарегистрированных доменов</span><span class="sxs-lookup"><span data-stu-id="e79db-109">Problems with unregistered domains</span></span>

<span data-ttu-id="e79db-p103">Проблема возникает, когда локальных серверов компрометации и приходится ретрансляцию большой объем нежелательной почты из него EOP. Почти во всех случаях зависят от выбора справа соединители, но электронной почты отправляется из незарегистрированных, также известной как подготовлено доменов. Office 365 разрешить разумный объем почты из незарегистрированных доменов, но обслуживаемых доменов, необходимо настроить в центре администрирования для каждого домена, на которых планируется отправка об отсутствии на работе.</span><span class="sxs-lookup"><span data-stu-id="e79db-p103">The problem is when on-premise servers get compromised and end up relaying a large volume of spam out of EOP. In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains. Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="e79db-p104">После атаке, клиенты не сможет отправки исходящей почты для незарегистрированных доменов. Пользователи будут получать Non-недоставке (NDR) о том:</span><span class="sxs-lookup"><span data-stu-id="e79db-p104">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains. Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="e79db-p105">550 5.7.750 служба недоступна. Клиент запретом Отправка из незарегистрированных доменов</span><span class="sxs-lookup"><span data-stu-id="e79db-p105">550 5.7.750 Service unavailable. Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="e79db-117">Разблокировка клиента для отправки еще раз</span><span class="sxs-lookup"><span data-stu-id="e79db-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="e79db-118">Существует несколько моментов, которые необходимо выполнить при блокируются для отправки из незарегистрированных доменов.</span><span class="sxs-lookup"><span data-stu-id="e79db-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="e79db-p106">Убедитесь в том, что все домены регистрация в центре администрирования Office 365. Дополнительные сведения можно найти [здесь](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="e79db-p106">Make sure that you register all of your domains in Office 365 admin center. More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="e79db-p107">Заблокировать локальных серверов и убедитесь в том, что они не скомпрометированы. Существует множество факторов участвующие здесь, особенно если серверы сторонних производителей, но необходимо иметь возможность убедитесь в том, что все почтовые сообщения, отправляемых из этого сервера является допустимым.</span><span class="sxs-lookup"><span data-stu-id="e79db-p107">Lock down your on-premise servers and ensure that they are not compromised. There are many factors involved here, especially if these are third-party servers, but you will need to be able to make sure all mail leaving that server is legitimate.</span></span>

<span data-ttu-id="e79db-p108">После этого необходимо будет вызовов службы поддержки Майкрософт и попросите для получения клиенту разблокировать для отправки из незарегистрированных доменов еще раз.  Предоставление код ошибки будет полезно, но необходимо подтвердить, что обеспечивается безопасность среды и что нежелательной почты не будут отправляться еще раз. Дополнительные сведения можно найти [здесь](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="e79db-p108">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.  Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again. More information can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="e79db-126">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="e79db-126">For more information</span></span>

[<span data-ttu-id="e79db-127">Защита от нежелательной почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="e79db-127">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="e79db-128">Отчеты о недоставке электронной почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="e79db-128">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="e79db-129">Настройка переадресации электронной почты для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="e79db-129">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="e79db-130">Как настроить отправку электронной почты с помощью Office 365 на многофункциональном устройстве или в приложении</span><span class="sxs-lookup"><span data-stu-id="e79db-130">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="e79db-131">[Управление обслуживаемые домены и в Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="e79db-131">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
