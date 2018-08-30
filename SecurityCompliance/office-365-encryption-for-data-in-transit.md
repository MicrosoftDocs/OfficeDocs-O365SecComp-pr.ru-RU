---
title: Шифрование Office 365 при передаче данных
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Сводка: Краткое описание как Microsoft шифрует данные в ходе доставки.'
ms.openlocfilehash: 8f4781cf1127fb1b6bf742c267c76e3df39b8209
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534301"
---
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="f6b38-103">Шифрование Office 365 при передаче данных</span><span class="sxs-lookup"><span data-stu-id="f6b38-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="f6b38-104">В дополнение к защите статических данных клиента, корпорация Майкрософт использует технологии шифрования для защиты данных клиента Office 365 в пути.</span><span class="sxs-lookup"><span data-stu-id="f6b38-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="f6b38-105">Данные находятся в пути:</span><span class="sxs-lookup"><span data-stu-id="f6b38-105">Data is in transit:</span></span>
- <span data-ttu-id="f6b38-106">Когда клиентский компьютер взаимодействует с сервером Office 365;</span><span class="sxs-lookup"><span data-stu-id="f6b38-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="f6b38-107">Когда сервер Office 365 взаимодействует с другим сервером Office 365; и</span><span class="sxs-lookup"><span data-stu-id="f6b38-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="f6b38-108">Когда сервер Office 365 взаимодействует с сервером Office 365 (например, Exchange Online выполнению электронной почты внешнего почтовый сервер).</span><span class="sxs-lookup"><span data-stu-id="f6b38-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="f6b38-p101">Взаимодействия между каналами центра обработки данных связи между серверами Office 365 осуществляется через TLS или IPsec, а все серверы заказчика согласование безопасного сеанса с использованием TLS с клиентскими компьютерами (например, Exchange Online использует TLS 1.2 с 256-разрядного шифрования силы используется (FIPS 140-2 уровень проверки 2). (Просмотреть [Справочные сведения о шифровании в Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) список наборов шифрования TLS, поддерживаются в Office 365). Это относится к протоколов, используемых клиентами, например Outlook, Скайп для бизнеса и Outlook в Интернете (например, HTTP, POP3, и т.д.).</span><span class="sxs-lookup"><span data-stu-id="f6b38-p101">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated). (See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="f6b38-p102">Сертификаты открытого выдаются Microsoft IT SSL с помощью SSLAdmin, внутренний средство Майкрософт для защиты конфиденциальности передаваемых данных. Все сертификаты, выданные ИТ-отдела Майкрософт не менее 2048 бит в длину и соответствия [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) требуется SSLAdmin, чтобы убедиться в том, что сертификаты выдаются только общие IP-адреса, принадлежащие Майкрософт. IP-адресов, не этот критерий направляются через процесс исключение.</span><span class="sxs-lookup"><span data-stu-id="f6b38-p102">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information. All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft. Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="f6b38-p103">Все сведения о реализации как версия используется протокол TLS, включена ли переадресовывать безопасной пересылки (FS), порядок наборы шифрования, и др., доступны публично. — Это один из способов видеть эти сведения для использования веб-сайта сторонних производителей, такие как руководства Компанию Qualys SSL (www.ssllabs.com). Ниже приведены ссылки на страницы, автоматического теста из Компанию Qualys, отображать сведения для следующих служб:</span><span class="sxs-lookup"><span data-stu-id="f6b38-p103">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly. One way to see these details is to use a third-party website, such as Qualys SSL Labs (www.ssllabs.com). Below are the links to automated test pages from Qualys that display information for the following services:</span></span>
- [<span data-ttu-id="f6b38-117">Портал Office 365</span><span class="sxs-lookup"><span data-stu-id="f6b38-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="f6b38-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="f6b38-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="f6b38-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="f6b38-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="f6b38-120">Скайп для бизнеса (SIP)</span><span class="sxs-lookup"><span data-stu-id="f6b38-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="f6b38-121">Скайп для бизнеса (Интернет)</span><span class="sxs-lookup"><span data-stu-id="f6b38-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="f6b38-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="f6b38-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="f6b38-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f6b38-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="f6b38-124">Для Exchange Online Protection URL-адреса в зависимости от имен клиента; Тем не менее все клиенты можно проверить с помощью **microsoft com.mail.protection.outlook.com**Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6b38-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
