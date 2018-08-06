---
title: Обзор Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 1270a65f-ddc3-4430-b500-4d3a481efb1e
description: Microsoft Exchange Online Protection (EOP) — это облачная службу фильтрации электронной почты, которое помогает защитить организацию от нежелательной почты и вредоносных программ и включает в себя компоненты по защите от нарушения политики обмена сообщениями вашей организации.
ms.openlocfilehash: 89852c7ba211ccb266c8b231b00d3d83987a5f20
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026696"
---
# <a name="exchange-online-protection-overview"></a><span data-ttu-id="4f3c1-103">Обзор Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="4f3c1-103">Exchange Online Protection overview</span></span>

<span data-ttu-id="4f3c1-p101">Microsoft Exchange Online Protection (EOP)  это облачная служба фильтрации электронной почты, которая помогает защитить организацию от нежелательной почты и вредоносных программ, передаваемых через электронную почту. К тому же, эта служба обладает функциями для защиты организации от нарушений политик обмена сообщениями. EOP может упростить управление вашей среды обмена сообщениями и облегчить многие тяготы, которые приходят с поддержкой локального аппаратного и программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-p101">Microsoft Exchange Online Protection (EOP) is a cloud-based email filtering service that helps protect your organization against spam and malware, and includes features to safeguard your organization from messaging-policy violations. EOP can simplify the management of your messaging environment and alleviate many of the burdens that come with maintaining on-premises hardware and software.</span></span>
  
<span data-ttu-id="4f3c1-106">Ниже приведены основные способы, с помощью которых можно использовать EOP для защиты сообщений.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-106">The following are the primary ways you can use EOP for messaging protection:</span></span>
  
- <span data-ttu-id="4f3c1-107">**В случае автономного** EOP обеспечивает защиту электронной почты на основе облака для Microsoft Exchange Server 2013 в локальной среде, прежних версий Exchange Server, или любые другие локального решения электронной почты SMTP.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-107">**In a standalone scenario** EOP provides cloud-based email protection for your on-premises Microsoft Exchange Server 2013 environment, legacy Exchange Server versions, or for any other on-premises SMTP email solution.</span></span> 
    
- <span data-ttu-id="4f3c1-108">**Как часть Microsoft Exchange Online** По умолчанию EOP защищает облачные почтовые ящики Microsoft Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-108">**As a part of Microsoft Exchange Online** By default, EOP protects Microsoft Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="4f3c1-109">**В гибридном развертывании** EOP можно настроить для защиты среды обмена сообщениями и управления маршрутизацией почты, когда имеется набор локальных и облачных почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-109">**In a hybrid deployment** EOP can be configured to protect your messaging environment and control mail routing when you have a mix of on-premises and cloud mailboxes.</span></span> 
    
## <a name="how-eop-works"></a><span data-ttu-id="4f3c1-110">Как работает EOP</span><span class="sxs-lookup"><span data-stu-id="4f3c1-110">How EOP works</span></span>

<span data-ttu-id="4f3c1-111">Чтобы понять, как работает EOP, будет полезным взглянуть, как эта служба обрабатывает входящую электронную почту.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-111">To understand how EOP works, it helps to see how it processes incoming email:</span></span>
  
![EOP электронной почты обработки](../media/EOP-email-processing.png)
  
<span data-ttu-id="4f3c1-p102">Входящее сообщение изначально проходит через фильтрации подключений, который проверяет репутации отправителя и проверяет сообщения на наличие вредоносных программ. Большая часть нежелательной почты остановлена на этом этапе и удалять EOP. Продолжите работу фильтрации политик, где будут оцениваться сообщений с помощью правил транспорта настраиваемых, создания и применения на основе шаблона сообщения. Например может иметь правило, которое отправляет уведомление руководителя при поступлении от определенного отправителя. (Проверки предотвращения потери данных также создаваться на этом этапе при наличии, в функциях, сведения о доступности функций, в разделе [Описание службы Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Рассмотрим процедуру сообщения передаются фильтрации контента, где содержимое проверяется на наличие терминология или общие свойства для защиты от нежелательной почты. Сообщение определены как нежелательная почта фильтром содержимого могут быть отправлены в папку нежелательной почты пользователя или в карантин, среди других параметров, на основе параметров. По истечении сообщение все эти слои защиты успешно доставлено получателю.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-p102">An incoming message initially passes through connection filtering, which checks the sender's reputation and inspects the message for malware. The majority of spam is stopped at this point and deleted by EOP. Messages continue through policy filtering, where messages are evaluated against custom transport rules that you create or enforce from a template. For example, you can have a rule that sends a notification to a manager when mail arrives from a specific sender. (Data loss prevention checks also occur at this point, if you have that feature; for information about feature availability, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).) Next, messages pass through content filtering, where content is checked for terminology or properties common to spam. A message determined to be spam by the content filter can be sent to a user's Junk Email folder or to the quarantine, among other options, based on your settings. After a message passes all of these protection layers successfully, it's delivered to the recipient.</span></span>
  
### <a name="eop-datacenters"></a><span data-ttu-id="4f3c1-120">Центры обработки данных службы EOP</span><span class="sxs-lookup"><span data-stu-id="4f3c1-120">EOP datacenters</span></span>

<span data-ttu-id="4f3c1-p103">Служба EOP работает во всемирной сети центров данных, которые предназначены для обеспечения лучшей доступности. Например, если центр данных недоступен, сообщения электронной почты автоматически направляются в другой центр данных без остановки работы службы. Серверы в каждом центре данных принимают сообщения от вашего имени, обеспечивая уровень разделения между вашей организацией и Интернетом, тем самым снижая нагрузку на серверы. Благодаря этой высокой доступности сети корпорация Майкрософт может гарантировать, что электронная почта достигнет вашей организации в установленные сроки.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-p103">EOP runs on a worldwide network of datacenters that are designed to provide the best availability. For example, if a datacenter becomes unavailable, email messages are automatically routed to another datacenter without any interruption in service. Servers in each datacenter accept messages on your behalf, providing a layer of separation between your organization and the Internet, thereby reducing load on your servers. Through this highly available network, Microsoft can ensure that email reaches your organization in a timely manner.</span></span> 
  
<span data-ttu-id="4f3c1-p104">Служба EOP выполняет балансировку нагрузки между центрами обработки данных, но только в пределах одного региона. Если ваша система настроена в одном регионе, все ваши сообщения будут обрабатываться с использованием маршрутизации для этого региона. В следующем списке показано, как региональная маршрутизация почты работает для центров обработки данных EOP:</span><span class="sxs-lookup"><span data-stu-id="4f3c1-p104">EOP performs load balancing between datacenters but only within a region. If you're provisioned in one region all your messages will be processed using the mail routing for that region. The following list shows the how regional mail routing works for the EOP datacenters:</span></span>
  
- <span data-ttu-id="4f3c1-p105">Отпечатано в абонента, все Exchange Online почтовые ящики которых располагаются в центрах обработки данных США, за исключением Южная Америка, где используется центров обработки данных в Бразилии и Чили и Канады, где используются центров обработки данных в Канада. Все сообщения электронной почты, включая сообщения для клиентов в Южная Америка и Канада, направляются через США центров обработки данных для фильтрации EOP; Тем не менее quaratined электронной почты хранится в центре обработки данных, где находится клиента.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-p105">In the America's, all Exchange Online mailboxes are located in U.S. datacenters, with the exception of South America where datacenters in Brazil and Chile are used and in Canada where datacenters in Canada are used. All email messages, including messages for customers in South America and Canada, are routed through U.S. datacenters for EOP filtering; however quaratined email is stored in the datacenter where the tenant is located..</span></span>
    
- <span data-ttu-id="4f3c1-130">В Европе, на Ближнем Востоке и в Африке (регион EMEA) все почтовые ящики Exchange Online находятся в центрах обработки данных региона EMEA, а все сообщения направляются через центры обработки данных EMEA для фильтрации с помощью EOP.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-130">In Europe, the Middle East, and Africa (EMEA), all Exchange Online mailboxes are located in EMEA datacenters, and all messages are routed through EMEA datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="4f3c1-p106">В Азиатско-Тихоокеанском регионе (APAC) все почтовые ящики Exchange Online расположены в центрах обработки данных в регионе APAC, но в текущий момент сообщения направляются через центры обработки данных EMEA для фильтрации с помощью EOP. В четвертом квартале 2014 г. все сообщения будут направляться через центры обработки данных региона APAC для фильтрации с помощью EOP.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-p106">In Asia-Pacific (APAC), all Exchange Online mailboxes are located in APAC datacenters, but messages are currently routed through EMEA datacenters for EOP filtering. This is targeted to be changing in the fourth quarter of 2014, when messages will be routed through APAC datacenters for EOP filtering.</span></span>
    
- <span data-ttu-id="4f3c1-133">Для облака сообщества государственных учреждений США (GCC) все почтовые ящики Exchange Online находятся в центрах обработки данных в США, а все сообщения направляются через центры обработки данных в США для фильтрации с помощью EOP.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-133">For the Government Community Cloud (GCC), all Exchange Online mailboxes are located in U.S. datacenters and all messages are routed through U.S. datacenters for EOP filtering.</span></span>
    
## <a name="eop-plans-and-features"></a><span data-ttu-id="4f3c1-134">Планы и возможности EOP</span><span class="sxs-lookup"><span data-stu-id="4f3c1-134">EOP plans and features</span></span>

<span data-ttu-id="4f3c1-135">Ниже приведены доступные планы подписки EOP:</span><span class="sxs-lookup"><span data-stu-id="4f3c1-135">The following are the available EOP subscription plans:</span></span>
  
- <span data-ttu-id="4f3c1-136">**Изолированная EOP** EOP защищает ваши локальные почтовые ящики.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-136">**EOP standalone** Where EOP protects your on-premises mailboxes.</span></span> 
    
- <span data-ttu-id="4f3c1-137">**Функциональность EOP в Exchange Online** EOP защищает ваши облачные почтовые ящики Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-137">**EOP features in Exchange Online** Where EOP protects your Exchange Online cloud-hosted mailboxes.</span></span> 
    
- <span data-ttu-id="4f3c1-138">**Лицензия Exchange Enterprise CAL со службами**. EOP защищает ваши локальные почтовые ящики как изолированная EOP и включает защиту от потери данных, а также возможности создания отчетов с помощью веб-служб.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-138">**Exchange Enterprise CAL with Services** Where EOP protects your on-premises mailboxes, like EOP standalone, and includes data loss prevention (DLP) and reporting using web services.</span></span> 
    
<span data-ttu-id="4f3c1-139">Сведения о требованиях, ограничениях и доступности функций во всех планах подписки EOP см. на странице [Описание службы Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span><span class="sxs-lookup"><span data-stu-id="4f3c1-139">For information about requirements, important limits, and feature availability across all EOP subscription plans, see the [Exchange Online Protection Service Description](https://go.microsoft.com/fwlink/p/?LinkId=320619).</span></span>
  
## <a name="setting-up-eop"></a><span data-ttu-id="4f3c1-140">Настройка EOP</span><span class="sxs-lookup"><span data-stu-id="4f3c1-140">Setting up EOP</span></span>

<span data-ttu-id="4f3c1-p107">Настройка EOP может быть простой процедурой, особенно в случае небольшой организации с немногочисленными правилами соответствия. Однако, в случае большой организации с несколькими доменами, настраиваемыми правилами соответствия или гибридным потоком обработки почты настройка может потребовать большего планирования и времени.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-p107">Setting up EOP can be simple, especially in the case of a small organization with a handful of compliance rules. However, if you have a large organization with multiple domains, custom compliance rules, or hybrid mail flow, set up can take more planning and time.</span></span>
  
<span data-ttu-id="4f3c1-143">При уже приобретенной EOP см. [Настройка службы EOP](set-up-your-eop-service.md), чтобы убедиться в выполнении всех действий, необходимых для настройки EOP с целью защиты вашей среды обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4f3c1-143">If you've already purchased EOP, see [Set up your EOP service](set-up-your-eop-service.md) to ensure that you complete all the steps necessary to configure EOP to protect your messaging environment.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="4f3c1-144">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="4f3c1-144">For more information</span></span>

[<span data-ttu-id="4f3c1-145">Функции EOP</span><span class="sxs-lookup"><span data-stu-id="4f3c1-145">EOP features</span></span>](eop-features.md)
  
[<span data-ttu-id="4f3c1-146">Видео о начале работы с EOP</span><span class="sxs-lookup"><span data-stu-id="4f3c1-146">Videos for getting started with EOP</span></span>](videos-for-getting-started-with-eop.md)
  
[<span data-ttu-id="4f3c1-147">Общие вопросы и ответы по EOP</span><span class="sxs-lookup"><span data-stu-id="4f3c1-147">EOP general FAQ</span></span>](eop-general-faq.md)
  
[<span data-ttu-id="4f3c1-148">Поставленные в очередь, отложенные и возвращенные сообщения EOP: вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="4f3c1-148">EOP queued, deferred, and bounced messages FAQ</span></span>](eop-queued-deferred-and-bounced-messages-faq.md)
  
[<span data-ttu-id="4f3c1-149">Вопросы и ответы по делегированному администрированию</span><span class="sxs-lookup"><span data-stu-id="4f3c1-149">Delegated administration FAQ</span></span>](delegated-administration-faq.md)
  
[<span data-ttu-id="4f3c1-150">Перемещение доменов и настроек из одной организации EOP в другую</span><span class="sxs-lookup"><span data-stu-id="4f3c1-150">Move domains and settings from one EOP organization to another EOP organization</span></span>](move-domains-and-settings-from-one-eop-organization-to-another-eop-organization.md)
  

