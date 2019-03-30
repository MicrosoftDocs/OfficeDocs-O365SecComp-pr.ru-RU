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
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: bd62d6d0b42edfd1eedf543d7d8bb68903c7c608
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000312"
---
# <a name="fix-sender-domain-insight"></a><span data-ttu-id="9b888-103">Исправление сведений о домене отправителя</span><span class="sxs-lookup"><span data-stu-id="9b888-103">Fix sender domain insight</span></span>

> [!NOTE]
> <span data-ttu-id="9b888-104">Функции, описанные в этом разделе, не были развернуты во всех организациях Office 365 и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="9b888-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="9b888-105">Office 365 требует, чтобы сообщения, отправляемые из внутренних локальных почтовых сред в Office 365, соответствовали определенным условиям безопасности:</span><span class="sxs-lookup"><span data-stu-id="9b888-105">Office 365 requires messages sending from internal on-premises email environments to Office 365 to meet certain security criteria:</span></span>

- <span data-ttu-id="9b888-106">Вы создали соединитель входящей почты в Office 365 для проверки подлинности SMTP-подключений с локального сервера электронной почты, используя исходный IP-адрес или сертификат.</span><span class="sxs-lookup"><span data-stu-id="9b888-106">You've created an inbound connector in Office 365 to authenticate SMTP connections from your on-premises email server by using the source IP address or a certificate.</span></span>

- <span data-ttu-id="9b888-107">Вы настроили локальный сервер электронной почты для ретрансляции электронной почты через Office 365 во внешний мир.</span><span class="sxs-lookup"><span data-stu-id="9b888-107">You've configured your on-premises email server to relay email via Office 365 to external world.</span></span>

- <span data-ttu-id="9b888-108">В конфигурации выполняется одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="9b888-108">In your configuration, one of the following statements is true:</span></span>

  - <span data-ttu-id="9b888-109">Домен электронной почты отправителя регистрируется в организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="9b888-109">The sender's email domain is registered in your Office 365 organization.</span></span> <span data-ttu-id="9b888-110">Дополнительные сведения см. в статье Добавление доменов в Office 365.</span><span class="sxs-lookup"><span data-stu-id="9b888-110">For more information, see Add Domains in Office 365.</span></span>

  - <span data-ttu-id="9b888-111">Локальный сервер электронной почты настроен на использование сертификата для отправки электронной почты в Office 365, сертификат содержит или точно соответствует доменному имени, зарегистрированному в Office 365, и создан соединитель на основе сертификата в Office 365 с этим поддомен.</span><span class="sxs-lookup"><span data-stu-id="9b888-111">Your on-premises email server is configured to use a certificate to send email to Office 365, the certificate contains or exactly matches a domain name that you've registered in Office 365, and you've created a certificate based connector in Office 365 with that domain.</span></span> 

<span data-ttu-id="9b888-112">Сообщения, которые не отвечают условиям, не будут применяться к Организации и могут быть отклонены.</span><span class="sxs-lookup"><span data-stu-id="9b888-112">Messages that don't meet the criteria will not be attributed to the organization and could be rejected.</span></span>

<span data-ttu-id="9b888-113">В \*\*\*\* этом примере показано, как определить потенциально скомпрометированные компьютеры и учетные записи пользователей в локальной среде электронной почты, которые не удовлетворяют критериям, и поможет вам выполнить действия по исправлению.</span><span class="sxs-lookup"><span data-stu-id="9b888-113">The **Fix sender domain** insight shows you email from your on-premises environment that doesn't meet the criteria, helps you to identify potentially compromised machines and user accounts in your on-premises email environment, and helps you to take remediation actions.</span></span>

![Исправление домена отправителя в информационной панели почтового процесса в центре безопасности _Амп_ соответствие требованиям](media/sender-domain-insight-selected.png)

<span data-ttu-id="9b888-115">При нажатии кнопки **Просмотреть сведения**вы перейдете на другой мини-приложение с дополнительными сведениями, как показано на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="9b888-115">When you click **View details**, you are taken to another widget with more details as shown in the following diagram:</span></span>

![Мини-приложение "сведения" в разделе Fix sender Domain Insight](media/sender-domain-view-details.png)

<span data-ttu-id="9b888-117">Вы увидите входящий соединитель, который использовался для доставки сообщений в Office 365.</span><span class="sxs-lookup"><span data-stu-id="9b888-117">You'll see the inbound connector that was used to deliver the messages to Office 365.</span></span> <span data-ttu-id="9b888-118">Вы также можете щелкнуть **Просмотреть примеры кодов сообщений** , чтобы просмотреть сведения о сообщениях, отправленных из локальной среды электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9b888-118">You can also click **view sample message IDs** to see details for the messages that were sent from your on-premises email environment.</span></span> <span data-ttu-id="9b888-119">Так как эти сообщения были отклонены в Office 365, вы не можете использовать трассировку сообщений, но вы можете использовать примеры идентификаторов сообщений для отслеживания сообщений в локальной почтовой среде.</span><span class="sxs-lookup"><span data-stu-id="9b888-119">Because these messages were rejected by Office 365, you can't use message trace, but you can use the sample message ids to track the messages in your on-premises email environment.</span></span>

![Просмотр образцов идентификаторов сообщений в исправлении домена отправителя](media/sender-domain-view-sample-message-ids.png)

## <a name="see-also"></a><span data-ttu-id="9b888-121">См. также</span><span class="sxs-lookup"><span data-stu-id="9b888-121">See also</span></span>

<span data-ttu-id="9b888-122">Для получения дополнительных сведений о других аналитиках почтовых ящиков в панели мониторинга для почтового процесса ознакомьтесь с разрешениями поЧтовых ящиков [в центре безопасности _Амп_ соответствия требованиям](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="9b888-122">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
