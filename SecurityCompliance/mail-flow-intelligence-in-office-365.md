---
title: Аналитика поток почты в Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c29f75e5-c16e-409e-a123-430691e38276
description: Администраторы могут узнать о коды ошибок, связанных с доставка сообщений с помощью соединителей в Office 365 (также известной как аналитики поток почты).
ms.openlocfilehash: 9f27dfd4c265eb62028d68c27764183202692ef4
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327091"
---
# <a name="mail-flow-intelligence-in-office-365"></a><span data-ttu-id="2be84-103">Аналитика поток почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="2be84-103">Mail flow intelligence in Office 365</span></span>

<span data-ttu-id="2be84-p101">Как правило используйте соединитель для маршрутизации сообщений электронной почты из организации Office 365 на локальную среду электронной почты. Можно также использовать соединитель для маршрутизации сообщений из Office 365 в партнерской организации. Когда Office 365 не удается доставить эти сообщения через соединитель, они в случае в очередь в Office 365. Office 365 будет предоставляться попыток доставки для каждого сообщения в течение 48 часов. После 48 часов истечения срока действия сообщение из очереди и сообщение будет возвращено отправителю в отчет о недоставке (также известной как сообщение о Недоставке или недоставки).</span><span class="sxs-lookup"><span data-stu-id="2be84-p101">Typically, you use a connector to route email messages from your Office 365 organization to your on-premises email environment. You might also use a connector to route messages from Office 365 to a partner organization. When Office 365 can't deliver these messages via the connector, they're queued in Office 365. Office 365 will continue to retry delivery for each message for 48 hours. After 48 hours, the queued message will expire, and the message will be returned to the original sender in a non-delivery report (also known as an NDR or bounce message).</span></span>

<span data-ttu-id="2be84-p102">Office 365 приводит к ошибке, если сообщение не удается доставить с помощью соединитель. В этом разделе описаны наиболее распространенные ошибки и способы их решения. В совокупности ошибки очереди и уведомления для недоставленных сообщений, отправленных с помощью соединителей называется _аналитики поток почты_.</span><span class="sxs-lookup"><span data-stu-id="2be84-p102">Office 365 generates an error when a message can't be delivered by using a connector. The most common errors and their solutions are described in this topic. Collectively, queuing and notification errors for undeliverable messages sent via connectors is known as _mail flow intelligence_.</span></span>

## <a name="error-code-450-44312-dns-query-failed"></a><span data-ttu-id="2be84-112">Код ошибки: 450 4.4.312 Сбой запроса DNS</span><span class="sxs-lookup"><span data-stu-id="2be84-112">Error code: 450 4.4.312 DNS query failed</span></span>

<span data-ttu-id="2be84-p103">Как правило Эта ошибка означает, что Office 365 пытался подключиться к промежуточный узел, который указан в соединитель, но DNS-запрос, чтобы найти не удалось промежуточный узел IP-адресов. Ниже приведены возможные причины сообщения об ошибке:</span><span class="sxs-lookup"><span data-stu-id="2be84-p103">Typically, this error means Office 365 tried to connect to the smart host that's specified in the connector, but the DNS query to find the smart host's IP addresses failed. The possible causes for this error are:</span></span>

- <span data-ttu-id="2be84-115">Проблема со службой размещения DNS домена (компанией, которая обслуживает полномочные серверы доменных имен для вашего домена).</span><span class="sxs-lookup"><span data-stu-id="2be84-115">There's an issue with your domain's DNS hosting service (the party that maintains the authoritative name servers for your domain).</span></span>

- <span data-ttu-id="2be84-116">Срок действия домена недавно истек, поэтому запись MX невозможно восстановить.</span><span class="sxs-lookup"><span data-stu-id="2be84-116">Your domain has recently expired, so the MX record can't be retrieved.</span></span>

- <span data-ttu-id="2be84-117">Запись MX домена была недавно изменена, а информация о нем на DNS-серверах Office 365 остается прежней.</span><span class="sxs-lookup"><span data-stu-id="2be84-117">Your domain's MX record has recently changed, and the Office 365 DNS servers still have previously cached DNS information for your domain.</span></span>

### <a name="how-do-i-fix-error-code-450-44312"></a><span data-ttu-id="2be84-118">Как исправить код ошибки 450 4.4.312?</span><span class="sxs-lookup"><span data-stu-id="2be84-118">How do I fix error code 450 4.4.312?</span></span>

- <span data-ttu-id="2be84-119">Работа с службе размещения DNS для определения и устранения проблем с вашего домена.</span><span class="sxs-lookup"><span data-stu-id="2be84-119">Work with your DNS hosting service to identify and fix the problem with your domain.</span></span>

- <span data-ttu-id="2be84-120">Если ошибку из вашей партнерской организации (например, стороннего облачной службы поставщика), обратитесь к своему партнеру для решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="2be84-120">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44315-connection-timed-out"></a><span data-ttu-id="2be84-121">Код ошибки: 450 4.4.315 Время ожидания подключения истекло</span><span class="sxs-lookup"><span data-stu-id="2be84-121">Error code: 450 4.4.315 Connection timed out</span></span>

<span data-ttu-id="2be84-p104">Как правило это означает, что Office 365 не удается подключиться к конечному серверу электронной почты. Дополнительные сведения об ошибке будут рассмотрены следующие вопросы проблемы. Например:</span><span class="sxs-lookup"><span data-stu-id="2be84-p104">Typically, this means Office 365 can't connect to the destination email server. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="2be84-125">Электронной почты на локальный сервер не работает.</span><span class="sxs-lookup"><span data-stu-id="2be84-125">Your on-premises email server is down.</span></span>

- <span data-ttu-id="2be84-126">Ошибка в настройках промежуточного узла соединителя, поэтому Office 365 пытается подключиться к неправильному IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="2be84-126">There's an error in the connector's smart host settings, so Office 365 is trying to connect to the wrong IP address.</span></span>

### <a name="how-do-i-fix-error-code-450-44315"></a><span data-ttu-id="2be84-127">Как исправить код ошибки 450 4.4.315?</span><span class="sxs-lookup"><span data-stu-id="2be84-127">How do I fix error code 450 4.4.315?</span></span>

- <span data-ttu-id="2be84-p105">Узнайте, какие сценарии относится к вам и внесите необходимые изменения. Например если правильность работы потока почты и не были изменены параметры соединителя, необходимо проверить среду электронной почты на локальный сервер не работает или были любые изменения инфраструктуры сети (например, изменены поставщикам услуг Интернета, теперь у вас есть различные IP-адреса).</span><span class="sxs-lookup"><span data-stu-id="2be84-p105">Find out which scenario applies to you, and make the necessary corrections. For example, if mail flow has been working correctly, and you haven't changed the connector settings, you need to check your on-premises email environment to see if the server is down, or if there have been any changes to your network infrastructure (for example, you've changed internet service providers, so you now have different IP addresses).</span></span>

- <span data-ttu-id="2be84-130">Если ошибку из вашей партнерской организации (например, стороннего облачной службы поставщика), обратитесь к своему партнеру для решения проблемы.</span><span class="sxs-lookup"><span data-stu-id="2be84-130">If the error is from your partner organization (for example, a 3rd party cloud service provider), contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44316-connection-refused"></a><span data-ttu-id="2be84-131">Код ошибки: 450 4.4.316 В подключении отказано</span><span class="sxs-lookup"><span data-stu-id="2be84-131">Error code: 450 4.4.316 Connection refused</span></span>

<span data-ttu-id="2be84-p106">Как правило Эта ошибка означает, что Office 365 произошла ошибка подключения при попытке подключения к электронной почты на целевой сервер. Скорее всего причина этой ошибки — брандмауэр блокирует подключения с Office 365 IP-адресов. Также эта ошибка может быть предусмотрено при проектировании если полностью перенесены на локальную электронной почты системы в Office 365 и завершите работу электронной почты в локальной среде.</span><span class="sxs-lookup"><span data-stu-id="2be84-p106">Typically, this error means Office 365 encountered a connection error when it tried to connect to the destination email server. A likely cause for this error is your firewall is blocking connections from Office 365 IP addresses. Or, this error might be by design if you've completely migrated your on-premises email system to Office 365 and shut down your on-premises email environment.</span></span>

### <a name="how-do-i-fix-error-code-450-44316"></a><span data-ttu-id="2be84-135">Как исправить код ошибки 450 4.4.316?</span><span class="sxs-lookup"><span data-stu-id="2be84-135">How do I fix error code 450 4.4.316?</span></span>

- <span data-ttu-id="2be84-p107">Если почтовые ящики в локальную среду, необходимо изменить параметры брандмауэра, чтобы разрешить подключение с Office 365 IP-адреса на TCP-порт 25 на локальных серверах электронной почты. Список в Office 365 IP-адреса в разделе [URL-адреса Office 365 и диапазоны IP-адресов](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span><span class="sxs-lookup"><span data-stu-id="2be84-p107">If you have mailboxes in your on-premises environment, you need to modify your firewall settings to allow connections from Office 365 IP addresses on TCP port 25 to your on-premises email servers. For a list of the Office 365 IP addresses, see [Office 365 URLs and IP address ranges](https://support.office.com/article/8548a211-3fe7-47cb-abb1-355ea5aa88a2.aspx).</span></span>

- <span data-ttu-id="2be84-p108">Если больше не нужна доставка сообщений в локальную среду, нажмите кнопку **Исправить** в оповещении, чтобы служба Office 365 могла немедленно отклонять сообщения, для которых указаны недействительные получатели. Это уменьшит риск превышения квоты организации относительно недействительных получателей. Такое превышение влияет на нормальную доставку сообщений. Вы также можете вручную устранить проблему, следуя приведенными ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="2be84-p108">If no more messages should be delivered to your on-premises environment, click **Fix now** in the alert so Office 365 can immediately reject the messages with invalid recipients. This will reduce the risk of exceeding your organization's quota for invalid recipients, which could impact normal message delivery. Or, you can use the following instructions to manually fix the issue:</span></span>

  - <span data-ttu-id="2be84-141">В [центре администрирования Exchange (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) в Office 365 отключение или удаление соединителя, доставка электронной почты из Office 365 на локальную среду электронной почты:</span><span class="sxs-lookup"><span data-stu-id="2be84-141">In the [Exchange admin center (EAC)](https://docs.microsoft.com/Exchange/exchange-admin-center) in Office 365, disable or delete the connector that delivers email from Office 365 to your on-premises email environment:</span></span>

    1. <span data-ttu-id="2be84-142">В центре администрирования Exchange последовательно выберите пункты **поток обработки почты** \> **соединители**.</span><span class="sxs-lookup"><span data-stu-id="2be84-142">In the EAC, go to **Mail flow** \> **Connectors**.</span></span>

    2. <span data-ttu-id="2be84-143">Выберите значение **для** **сервера электронной почты вашей организации** и соединителя со значением **из** **Office 365** и выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="2be84-143">Select the connector with the **From** value **Office 365** and the **To** value **Your organization's email server** and do one of the following steps:</span></span>

       - <span data-ttu-id="2be84-144">Удаление соединителя, нажав кнопку **Удалить** ![значок "Удалить"](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span><span class="sxs-lookup"><span data-stu-id="2be84-144">Delete the connector by clicking **Delete** ![Remove icon](media/adf01106-cc79-475c-8673-065371c1897b.gif)</span></span>

       - <span data-ttu-id="2be84-145">Отключение соединитель, нажав кнопку **Изменить** ![значок Правка](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) unchecking **Включить эту возможность**.</span><span class="sxs-lookup"><span data-stu-id="2be84-145">Disable the connector by clicking **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) and unchecking **Turn it on**.</span></span>

  - <span data-ttu-id="2be84-p109">Измените обслуживаемого домена в Office 365, связанную с вашей электронной почты в локальную среду из **Внутренней ретрансляции** **Уполномоченный**. Сведения содержатся в разделе [Управление обслуживаемые домены и в Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span><span class="sxs-lookup"><span data-stu-id="2be84-p109">Change the accepted domain in Office 365 that's associated with your on-premises email environment from **Internal Relay** to **Authoritative**. For instructions, see [Manage accepted domains in Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=785428).</span></span>

  <span data-ttu-id="2be84-p110">**Примечание**: как правило, эти изменения вступили между 30 минут и один час вступили в силу. Через 1 час проверьте больше не сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2be84-p110">**Note**: Typically, these changes take between 30 minutes and one hour to take effect. After one hour, verify that you no longer receive the error.</span></span>

- <span data-ttu-id="2be84-150">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="2be84-150">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44317-cannot-connect-to-remote-server"></a><span data-ttu-id="2be84-151">Код ошибки: 450 4.4.317 Не удается подключиться к удаленному серверу</span><span class="sxs-lookup"><span data-stu-id="2be84-151">Error code: 450 4.4.317 Cannot connect to remote server</span></span>

<span data-ttu-id="2be84-p111">Как правило Эта ошибка означает, что Office 365, подключенных к на целевой сервер электронной почты, но сервер в ответе интерпретации ошибка или не соответствует требованиям подключения. Дополнительные сведения об ошибке будут рассмотрены следующие вопросы проблемы. Например:</span><span class="sxs-lookup"><span data-stu-id="2be84-p111">Typically, this error means Office 365 connected to the destination email server, but the server responded with an immediate error, or doesn't meet the connection requirements. The error details will explain the problem. For example:</span></span>

- <span data-ttu-id="2be84-155">На целевой сервер электронной почты в ответе на ошибку «Служба недоступна», которая указывает сервер, не удается поддержание связи с Office 365.</span><span class="sxs-lookup"><span data-stu-id="2be84-155">The destination email server responded with a "Service not available" error, which indicates the server is unable to maintain communication with Office 365.</span></span>

- <span data-ttu-id="2be84-156">Соединитель настроен для использования TLS, но на целевой сервер электронной почты не поддерживает TLS.</span><span class="sxs-lookup"><span data-stu-id="2be84-156">The connector is configured to require TLS, but the destination email server doesn't support TLS.</span></span>

### <a name="how-do-i-fix-error-code-450-44317"></a><span data-ttu-id="2be84-157">Как исправить код ошибки 450 4.4.317?</span><span class="sxs-lookup"><span data-stu-id="2be84-157">How do I fix error code 450 4.4.317?</span></span>

- <span data-ttu-id="2be84-158">Проверьте настройки TLS и сертификаты на локальных серверах электронной почты и параметров TLS на соединителе.</span><span class="sxs-lookup"><span data-stu-id="2be84-158">Verify the TLS settings and certificates on your on-premises email servers, and the TLS settings on the connector.</span></span>

- <span data-ttu-id="2be84-159">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="2be84-159">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-44318-connection-was-closed-abruptly"></a><span data-ttu-id="2be84-160">Код ошибки: 450 4.4.318 Соединение было внезапно прервано</span><span class="sxs-lookup"><span data-stu-id="2be84-160">Error code: 450 4.4.318 Connection was closed abruptly</span></span>

<span data-ttu-id="2be84-p112">Как правило Эта ошибка означает, что Office 365 возникли ошибки, в связи с электронной почты в локальной среде, поэтому сброс подключения. Ниже приведены возможные причины сообщения об ошибке:</span><span class="sxs-lookup"><span data-stu-id="2be84-p112">Typically, this error means Office 365 is having difficulty communicating with your on-premises email environment, so the connection was dropped. The possible causes for this error are:</span></span>

- <span data-ttu-id="2be84-163">Брандмауэр использует правила проверки пакетов SMTP, и эти правила работают неправильно.</span><span class="sxs-lookup"><span data-stu-id="2be84-163">Your firewall uses SMTP packet examination rules, and those rules aren't working correctly.</span></span>

- <span data-ttu-id="2be84-164">На локальный сервер электронной почты не будет работать правильно (например, службы зависает, сбои или нехватка системных ресурсов), которой — это приведет к времени ожидания и закройте подключение к Office 365.</span><span class="sxs-lookup"><span data-stu-id="2be84-164">Your on-premises email server isn't working correctly (for example, service hangs, crashes, or low system resources), which is causing the server to time out and close the connection to Office 365.</span></span>

- <span data-ttu-id="2be84-165">Проблемы с сетью между локальной средой и Office 365.</span><span class="sxs-lookup"><span data-stu-id="2be84-165">There are network issues between your on-premises environment and Office 365.</span></span>

### <a name="how-do-i-fix-error-code-450-44318"></a><span data-ttu-id="2be84-166">Как исправить код ошибки 450 4.4.318?</span><span class="sxs-lookup"><span data-stu-id="2be84-166">How do I fix error code 450 4.4.318?</span></span>

- <span data-ttu-id="2be84-167">Выясните, какой из этих пунктов относится к вам, и внесите необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="2be84-167">Find out which scenario applies to you, and make the necessary corrections.</span></span>

- <span data-ttu-id="2be84-168">Если проблема вызвана неполадки в сети между локальной средой и Office 365, обратитесь к своему сети группу для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="2be84-168">If the problem is caused by network issues between your on-premises environment and Office 365, contact your network team to troubleshoot the issue.</span></span>

- <span data-ttu-id="2be84-169">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="2be84-169">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="error-code-450-47320-certificate-validation-failed"></a><span data-ttu-id="2be84-170">Код ошибки: 450 4.7.320 Не удалось проверить сертификат</span><span class="sxs-lookup"><span data-stu-id="2be84-170">Error code: 450 4.7.320 Certificate validation failed</span></span>

<span data-ttu-id="2be84-p113">Как правило Эта ошибка означает, что Office 365 произошла ошибка при попытке проверить сертификат на целевой сервер электронной почты. Дополнительные сведения об ошибке будут рассмотрены следующие вопросы об ошибке. Например:</span><span class="sxs-lookup"><span data-stu-id="2be84-p113">Typically, this error means Office 365 encountered an error while trying to validate the certificate of the destination email server. The error details will explain the error. For example:</span></span>

- <span data-ttu-id="2be84-174">Срок действия сертификата истек</span><span class="sxs-lookup"><span data-stu-id="2be84-174">Certificate expired</span></span>

- <span data-ttu-id="2be84-175">Субъект сертификата не совпадает с именем узла</span><span class="sxs-lookup"><span data-stu-id="2be84-175">Certificate subject mismatch</span></span>

- <span data-ttu-id="2be84-176">Сертификат больше не действителен</span><span class="sxs-lookup"><span data-stu-id="2be84-176">Certificate is no longer valid</span></span>

### <a name="how-do-i-fix-error-code-450-47320"></a><span data-ttu-id="2be84-177">Как исправить код ошибки 450 4.7.320?</span><span class="sxs-lookup"><span data-stu-id="2be84-177">How do I fix error code 450 4.7.320?</span></span>

- <span data-ttu-id="2be84-178">Исправление сертификата или параметров на соединитель, чтобы сообщения из очереди в Office 365 могут доставляться.</span><span class="sxs-lookup"><span data-stu-id="2be84-178">Fix the certificate or the settings on the connector so that queued messages in Office 365 can be delivered.</span></span>

- <span data-ttu-id="2be84-179">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных служб), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="2be84-179">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>

## <a name="other-error-codes"></a><span data-ttu-id="2be84-180">Коды других ошибок</span><span class="sxs-lookup"><span data-stu-id="2be84-180">Other error codes</span></span>

<span data-ttu-id="2be84-p114">Office 365 возникли ошибки, доставка сообщений в своей локальной или партнерские сервер электронной почты. Процесс выдачи в вашей среде с помощью сведений **конечного сервера** при возникновении ошибки или изменения соединителя, если ошибка конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2be84-p114">Office 365 is having difficulty delivering messages to your on-premises or partner email server. Use the **Destination server** information in the error to examine the issue in your environment, or modify the connector if there's a configuration error.</span></span> 

<span data-ttu-id="2be84-183">Если ошибка связана с партнерской организацией (например, сторонним поставщиком облачных услуг), свяжитесь с ней, чтобы решить проблему.</span><span class="sxs-lookup"><span data-stu-id="2be84-183">If the error is from your partner organization (for example, a 3rd party cloud service provider), you need to contact your partner to fix the issue.</span></span>
