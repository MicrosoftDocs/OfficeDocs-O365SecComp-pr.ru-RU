---
title: Аналитика поток почты в Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/27/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: 'Как правило, используется соединитель для маршрутизации сообщений из вашей организации Office 365 в своей локальной среде обмена сообщениями. Можно также использовать соединитель для маршрутизации сообщений из Office 365 в партнерской организации. Когда Office 365 не удается доставить эти сообщения через соединитель, они в случае в очередь в Office 365. '
ms.openlocfilehash: 4effbb783d6ba8f3b33d0aed446e031193d2f2a3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002731"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="f6dce-105">Аналитика поток почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="f6dce-105">Mail flow intelligence in Office 365</span></span>
  
<span data-ttu-id="f6dce-p102">Обычно для маршрутизации сообщений из организации Office 365 в локальную среду обмена сообщениями используется соединитель. Соединитель также можно использовать для маршрутизации сообщений из Office 365 в партнерскую организацию. Когда Office 365 не удается доставить сообщение через соединитель, оно помещается в очередь. Office 365 продолжает попытки доставить его в течение 48 часов. После этого сообщение возвращается исходному отправителю в отчете о недоставке.</span><span class="sxs-lookup"><span data-stu-id="f6dce-p102">Typically, you use a connector to route messages from your Office 365 organization to your on-premises messaging environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>
  
<span data-ttu-id="f6dce-p103">Office 365 генерирует ошибку, когда сообщение не удается доставить с помощью соединителя. Наиболее распространенные ошибки и их решения описаны в этом разделе. Помещение в очередь недоставленных сообщений, отправленных через соединители, и ошибки уведомлений о них называют логикой потока обработки почты.</span><span class="sxs-lookup"><span data-stu-id="f6dce-p103">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as mailflow intelligence.</span></span>
  
 <span data-ttu-id="f6dce-114">**Содержание**</span><span class="sxs-lookup"><span data-stu-id="f6dce-114">**Contents**</span></span>
  
- [<span data-ttu-id="f6dce-115">Код ошибки: 450 4.4.312 Сбой запроса DNS</span><span class="sxs-lookup"><span data-stu-id="f6dce-115">Error code: 450 4.4.312 DNS query failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44312)
    
- [<span data-ttu-id="f6dce-116">Код ошибки: 450 4.4.315 Время ожидания подключения истекло</span><span class="sxs-lookup"><span data-stu-id="f6dce-116">Error code: 450 4.4.315 Connection timed out</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44315)
    
- [<span data-ttu-id="f6dce-117">Код ошибки: 450 4.4.316 В подключении отказано</span><span class="sxs-lookup"><span data-stu-id="f6dce-117">Error code: 450 4.4.316 Connection refused</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44316)
    
- [<span data-ttu-id="f6dce-118">Код ошибки: 450 4.4.317 Не удается подключиться к удаленному серверу</span><span class="sxs-lookup"><span data-stu-id="f6dce-118">Error code: 450 4.4.317 Cannot connect to remote server</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44317)
    
- [<span data-ttu-id="f6dce-119">Код ошибки: 450 4.4.318 Соединение было внезапно прервано</span><span class="sxs-lookup"><span data-stu-id="f6dce-119">Error code: 450 4.4.318 Connection was closed abruptly</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode44318)
    
- [<span data-ttu-id="f6dce-120">Код ошибки: 450 4.7.320 Не удалось проверить сертификат</span><span class="sxs-lookup"><span data-stu-id="f6dce-120">Error code: 450 4.7.320 Certificate validation failed</span></span>](mail-flow-intelligence-in-office-365.md#ErrorCode47320)
    
## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="f6dce-121">Код ошибки: 450 4.4.312 Сбой запроса DNS</span><span class="sxs-lookup"><span data-stu-id="f6dce-121">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="f6dce-p104">Как правило, эта ошибка означает, что Office 365 пытался подключиться к промежуточному узлу, указанному в соединителе, но поиск IP-адресов промежуточного узла выполнить не удалось. Возможные причины этой ошибки:</span><span class="sxs-lookup"><span data-stu-id="f6dce-p104">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host IP addresses failed. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="f6dce-124">Проблема со службой размещения DNS домена (компанией, которая обслуживает полномочные серверы доменных имен для вашего домена).</span><span class="sxs-lookup"><span data-stu-id="f6dce-124">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>
    
- <span data-ttu-id="f6dce-125">Срок действия домена недавно истек, поэтому запись MX невозможно восстановить.</span><span class="sxs-lookup"><span data-stu-id="f6dce-125">Your domain has recently expired, so the MX record can't be retrieved.</span></span>
    
- <span data-ttu-id="f6dce-126">Запись MX домена была недавно изменена, а информация о нем на DNS-серверах Office 365 остается прежней.</span><span class="sxs-lookup"><span data-stu-id="f6dce-126">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>
    
<span data-ttu-id="f6dce-127">Чтобы решить эту проблему, обратитесь в службу размещения DNS.</span><span class="sxs-lookup"><span data-stu-id="f6dce-127">You need to fix the DNS issue by working with your DNS hosting service.</span></span>
  
<span data-ttu-id="f6dce-128">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="f6dce-128">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="f6dce-129">Код ошибки: 450 4.4.315 Время ожидания подключения истекло</span><span class="sxs-lookup"><span data-stu-id="f6dce-129">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="f6dce-p105">Как правило, это означает, что Office 365 не может подключиться к целевому серверу обмена сообщениями. Описание проблемы см. в сведениях об ошибке. Например:</span><span class="sxs-lookup"><span data-stu-id="f6dce-p105">Typically, this means Office 365 can't connect to the destination messaging server. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="f6dce-133">Локальный сервер обмена сообщениями отключен.</span><span class="sxs-lookup"><span data-stu-id="f6dce-133">Your on-premises messaging server is down.</span></span>
    
- <span data-ttu-id="f6dce-134">Ошибка в настройках промежуточного узла соединителя, поэтому Office 365 пытается подключиться к неправильному IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="f6dce-134">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>
    
<span data-ttu-id="f6dce-p106">Выясните, какой из этих пунктов относится к вам, и внесите необходимые изменения. Например, если поток обработки почты работал правильно и вы не изменяли настройки соединителя, проверьте локальную среду обмена сообщениями, чтобы узнать, не отключен ли сервер и не было ли изменений в сетевой инфраструктуре (например, изменился интернет-провайдер, поэтому теперь у вас другие IP-адреса).</span><span class="sxs-lookup"><span data-stu-id="f6dce-p106">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises messaging environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed Internet service providers, so you now have different IP addresses).</span></span>
  
<span data-ttu-id="f6dce-137">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="f6dce-137">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="f6dce-138">Код ошибки: 450 4.4.316 В подключении отказано</span><span class="sxs-lookup"><span data-stu-id="f6dce-138">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="f6dce-p107">Как правило, эта ошибка означает, что при попытке подключения к целевому серверу обмена сообщениями произошла ошибка. Вероятно, эта ошибка произошла из-за того, что ваш брандмауэр блокирует подключения с IP-адресов Office 365. Если вы отказались от локальной среды обмена сообщениями, полностью перенеся локальную систему обмена сообщениями в Office 365, возникновение этой ошибки  нормальное поведение.</span><span class="sxs-lookup"><span data-stu-id="f6dce-p107">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination messaging server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises messaging system to Office 365 and shut down your on-premises messaging environment..</span></span>
  
- <span data-ttu-id="f6dce-p108">Если в локальной среде есть почтовые ящики, измените настройки брандмауэра, чтобы разрешать подключения к локальным серверам обмена сообщениями с IP-адресов Office 365 на TCP-порту 25. Список IP-адресов Office 365 см. в статье [URL-адреса и диапазоны IP-адресов Office 365](https://go.microsoft.com/fwlink/p/?linkid=228887).</span><span class="sxs-lookup"><span data-stu-id="f6dce-p108">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises messaging servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://go.microsoft.com/fwlink/p/?linkid=228887).</span></span>
    
- <span data-ttu-id="f6dce-p109">Если больше не нужна доставка сообщений в локальную среду, нажмите кнопку **Исправить** в оповещении, чтобы служба Office 365 могла немедленно отклонять сообщения, для которых указаны недействительные получатели. Это уменьшит риск превышения квоты организации относительно недействительных получателей. Такое превышение влияет на нормальную доставку сообщений. Вы также можете вручную устранить проблему, следуя приведенными ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="f6dce-p109">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span> 
    
  - <span data-ttu-id="f6dce-p110">Отключение или удаление соединителя с Office 365 в локальную среду: центр администрирования Office 365 \> **центры администрирования** \> **Exchange** \> **поток обработки почты** \> **соединители** \> выберите соединитель со значением **из** **Office 365** и **для** значения **сервер электронной почты вашей организации**. Удаление соединителя, нажав кнопку **Удалить**![значок удаления](media/ITPro-EAC-DeleteIcon.gif), или отключить соединитель, нажав кнопку **Изменить** ![значок Правка](media/ITPro-EAC-EditIcon.gif) unchecking **Включить эту возможность**.</span><span class="sxs-lookup"><span data-stu-id="f6dce-p110">Disable or delete the connector from Office 365 to your on-premises environment: Office 365 admin center \> **Admin centers** \> **Exchange** \> **Mail flow** \> **Connectors** \> select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server**. Delete the connector by clicking **Delete**![Delete icon](media/ITPro-EAC-DeleteIcon.gif), or disable the connector by clicking **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif) and unchecking **Turn it on**.</span></span>
    
  - <span data-ttu-id="f6dce-p111">Измените обслуживаемый домен в Office 365, который связан с локальной средой обмена сообщениями, задав вместо параметра **Внутренняя ретрансляция** параметр **Заслуживающий доверия**. Инструкции см. в статье [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span><span class="sxs-lookup"><span data-stu-id="f6dce-p111">Change the accepted domain in Office 365 that's associated with your on-premises messaging environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage Accepted Domains in Exchange Online](http://technet.microsoft.com/library/0fc0ecc0-e133-48fa-9d72-cb4793a73960.aspx).</span></span>
    
    <span data-ttu-id="f6dce-p112">**Примечание**: как правило, эти изменения вступили между 30 минут и один час вступили в силу. Через 1 час проверьте больше не сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f6dce-p112">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>
    
<span data-ttu-id="f6dce-153">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="f6dce-153">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="f6dce-154">Код ошибки: 450 4.4.317 Не удается подключиться к удаленному серверу</span><span class="sxs-lookup"><span data-stu-id="f6dce-154">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="f6dce-p113">Как правило, эта ошибка означает, что Office 365 подключился к целевому серверу обмена сообщениями, но ответ сервера содержит ошибку или он не соответствует требованиям для подключения. Описание проблемы см. в сведениях об ошибке. Например:</span><span class="sxs-lookup"><span data-stu-id="f6dce-p113">Typically, this error means Office 365 connected to the destination messaging server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>
  
- <span data-ttu-id="f6dce-158">Ответ целевого сервера обмена сообщений содержит ошибку "Служба недоступна", что означает, что сервер не может поддерживать связь с Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6dce-158">The destination messaging server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>
    
- <span data-ttu-id="f6dce-159">Настройки соединителя требуют использовать TLS, но целевой сервер обмена сообщениями не поддерживает TLS.</span><span class="sxs-lookup"><span data-stu-id="f6dce-159">The connector is configured to require TLS, but the destination messaging server doesn't support TLS.</span></span>
    
<span data-ttu-id="f6dce-160">Проверьте настройки TLS и сертификаты на локальных серверах обмена сообщениями и настройки TLS на соединителе.</span><span class="sxs-lookup"><span data-stu-id="f6dce-160">Verify the TLS settings and certificates on your on-premises messaging servers, and the TLS settings on the connector.</span></span>
  
<span data-ttu-id="f6dce-161">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="f6dce-161">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="f6dce-162">Код ошибки: 450 4.4.318 Соединение было внезапно прервано</span><span class="sxs-lookup"><span data-stu-id="f6dce-162">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="f6dce-p114">Как правило, эта ошибка означает, что возникла проблема со связью с локальной средой обмена сообщениями, поэтому соединение было прервано. Возможные причины этой ошибки:</span><span class="sxs-lookup"><span data-stu-id="f6dce-p114">Typically, this error means Office 365 is having difficulty communicating with your on-premises messaging environment, so the connection was dropped. The possible causes for this error are:</span></span>
  
- <span data-ttu-id="f6dce-165">Брандмауэр использует правила проверки пакетов SMTP, и эти правила работают неправильно.</span><span class="sxs-lookup"><span data-stu-id="f6dce-165">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>
    
- <span data-ttu-id="f6dce-166">Локальный сервер обмена сообщениями работает неправильно (например, зависания служб, сбои или низкие системные ресурсы), из-за чего время ожидания истекает и сервер прерывает подключение к Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6dce-166">Your on-premises messaging server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>
    
- <span data-ttu-id="f6dce-p115">Проблемы с сетью между локальной средой и Office 365. Если проблема не исчезает, обратитесь к специалисту по сетям для ее устранения.</span><span class="sxs-lookup"><span data-stu-id="f6dce-p115">There are network issues between your on-premises environment and Office 365. If the problem persists, contact your network team to troubleshoot the issue.</span></span>
    
<span data-ttu-id="f6dce-169">Выясните, какой из этих пунктов относится к вам, и внесите необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="f6dce-169">Find out which scenario applies to you, and make the necessary corrections.</span></span>
  
<span data-ttu-id="f6dce-170">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="f6dce-170">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="f6dce-171">Код ошибки: 450 4.7.320 Не удалось проверить сертификат</span><span class="sxs-lookup"><span data-stu-id="f6dce-171">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="f6dce-p116">Как правило, эта ошибка означает, что при попытке проверить сертификат целевого сервера обмена сообщениями произошла ошибка. Описание см. в сведениях об ошибке. Например:</span><span class="sxs-lookup"><span data-stu-id="f6dce-p116">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination messaging server. The error details will explain the error. For example:</span></span>
  
- <span data-ttu-id="f6dce-175">Срок действия сертификата истек</span><span class="sxs-lookup"><span data-stu-id="f6dce-175">Certificate expired</span></span>
    
- <span data-ttu-id="f6dce-176">Субъект сертификата не совпадает с именем узла</span><span class="sxs-lookup"><span data-stu-id="f6dce-176">Certificate subject mismatch</span></span>
    
- <span data-ttu-id="f6dce-177">Сертификат больше не действителен</span><span class="sxs-lookup"><span data-stu-id="f6dce-177">Certificate is no longer valid</span></span>
    
<span data-ttu-id="f6dce-178">Исправьте сертификат или соединитель, чтобы можно было доставить сообщения в очереди Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6dce-178">Please fix the certificate or the connector so that queued messages in Office 365can be delivered.</span></span>
  
<span data-ttu-id="f6dce-179">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных служб), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="f6dce-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  
## <a name="other-error-codes"></a><span data-ttu-id="f6dce-180">Коды других ошибок</span><span class="sxs-lookup"><span data-stu-id="f6dce-180">Other error codes</span></span>

<span data-ttu-id="f6dce-p117">Office 365 не удается доставить сообщения на локальный или партнерский сервер обмена сообщениями. Используйте информацию **Конечный сервер** в сообщении об ошибке, чтобы устранить проблему в своей среде, или измените соединитель, если ошибка связана с конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="f6dce-p117">Office 365 is having difficulty delivering messages to your on-premises or partner messaging server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 
  
<span data-ttu-id="f6dce-183">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="f6dce-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
  

