---
title: Исправление сведений о домене отправителя
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Администраторы могут узнать об исправлении домена отправителя в панели мониторинга почтовых ящиков в центре безопасности _Амп_ соответствия требованиям.
ms.openlocfilehash: a285a1c744ca540cc58b9408b4ee31e768f89479
ms.sourcegitcommit: e05e83212e7ca4e84f2ddb0de0297895b995338d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2019
ms.locfileid: "33868567"
---
# <a name="fix-sender-domain-insight"></a><span data-ttu-id="8b986-103">Исправление сведений о домене отправителя</span><span class="sxs-lookup"><span data-stu-id="8b986-103">Fix sender domain insight</span></span>

<span data-ttu-id="8b986-104">Office 365 требует, чтобы сообщения, отправляемые из внутренних локальных почтовых сред в Office 365, соответствовали определенным условиям безопасности:</span><span class="sxs-lookup"><span data-stu-id="8b986-104">Office 365 requires messages sending from internal on-premises email environments to Office 365 to meet certain security criteria:</span></span>

- <span data-ttu-id="8b986-105">Вы создали соединитель входящей почты в Office 365 для проверки подлинности SMTP-подключений с локального сервера электронной почты, используя исходный IP-адрес или сертификат.</span><span class="sxs-lookup"><span data-stu-id="8b986-105">You've created an inbound connector in Office 365 to authenticate SMTP connections from your on-premises email server by using the source IP address or a certificate.</span></span>

- <span data-ttu-id="8b986-106">Вы настроили локальный сервер электронной почты для ретрансляции электронной почты через Office 365 во внешний мир.</span><span class="sxs-lookup"><span data-stu-id="8b986-106">You've configured your on-premises email server to relay email via Office 365 to external world.</span></span>

- <span data-ttu-id="8b986-107">В конфигурации выполняется одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="8b986-107">In your configuration, one of the following statements is true:</span></span>

  - <span data-ttu-id="8b986-108">Домен электронной почты отправителя регистрируется в организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="8b986-108">The sender's email domain is registered in your Office 365 organization.</span></span> <span data-ttu-id="8b986-109">Дополнительные сведения см. в статье Добавление доменов в Office 365.</span><span class="sxs-lookup"><span data-stu-id="8b986-109">For more information, see Add Domains in Office 365.</span></span>

  - <span data-ttu-id="8b986-110">Локальный сервер электронной почты настроен на использование сертификата для отправки электронной почты в Office 365, сертификат содержит или точно соответствует доменному имени, зарегистрированному в Office 365, и создан соединитель на основе сертификата в Office 365 с этим поддомен.</span><span class="sxs-lookup"><span data-stu-id="8b986-110">Your on-premises email server is configured to use a certificate to send email to Office 365, the certificate contains or exactly matches a domain name that you've registered in Office 365, and you've created a certificate based connector in Office 365 with that domain.</span></span> 

<span data-ttu-id="8b986-111">Сообщения, которые не отвечают условиям, не будут применяться к Организации и могут быть отклонены.</span><span class="sxs-lookup"><span data-stu-id="8b986-111">Messages that don't meet the criteria will not be attributed to the organization and could be rejected.</span></span>

<span data-ttu-id="8b986-112">В \*\*\*\* этом примере показано, как определить потенциально скомпрометированные компьютеры и учетные записи пользователей в локальной среде электронной почты, которые не удовлетворяют критериям, и поможет вам выполнить действия по исправлению.</span><span class="sxs-lookup"><span data-stu-id="8b986-112">The **Fix sender domain** insight shows you email from your on-premises environment that doesn't meet the criteria, helps you to identify potentially compromised machines and user accounts in your on-premises email environment, and helps you to take remediation actions.</span></span>

![Исправление домена отправителя в информационной панели почтового процесса в центре безопасности _Амп_ соответствие требованиям](media/sender-domain-insight-selected.png)

<span data-ttu-id="8b986-114">При нажатии кнопки **Просмотреть сведения**вы перейдете на другой мини-приложение с дополнительными сведениями, как показано на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="8b986-114">When you click **View details**, you are taken to another widget with more details as shown in the following diagram:</span></span>

![Мини-приложение "сведения" в разделе Fix sender Domain Insight](media/sender-domain-view-details.png)

<span data-ttu-id="8b986-116">Вы увидите входящий соединитель, который использовался для доставки сообщений в Office 365.</span><span class="sxs-lookup"><span data-stu-id="8b986-116">You'll see the inbound connector that was used to deliver the messages to Office 365.</span></span> <span data-ttu-id="8b986-117">Вы также можете щелкнуть **Просмотреть примеры кодов сообщений** , чтобы просмотреть сведения о сообщениях, отправленных из локальной среды электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8b986-117">You can also click **view sample message IDs** to see details for the messages that were sent from your on-premises email environment.</span></span> <span data-ttu-id="8b986-118">Так как эти сообщения были отклонены в Office 365, вы не можете использовать трассировку сообщений, но вы можете использовать примеры идентификаторов сообщений для отслеживания сообщений в локальной почтовой среде.</span><span class="sxs-lookup"><span data-stu-id="8b986-118">Because these messages were rejected by Office 365, you can't use message trace, but you can use the sample message ids to track the messages in your on-premises email environment.</span></span>

![Просмотр образцов идентификаторов сообщений в исправлении домена отправителя](media/sender-domain-view-sample-message-ids.png)

## <a name="see-also"></a><span data-ttu-id="8b986-120">См. также</span><span class="sxs-lookup"><span data-stu-id="8b986-120">See also</span></span>

<span data-ttu-id="8b986-121">Для получения дополнительных сведений о других аналитиках почтовых ящиков в панели мониторинга для почтового процесса ознакомьтесь с разрешениями почтовых ящиков [в центре безопасности _Амп_ соответствия требованиям](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="8b986-121">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
