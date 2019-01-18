---
title: Поток обработки исходящих и входящих сообщений
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: 8/7/2018
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Администраторы могут узнать о исходящего соединителя и мини-приложения поток обработки входящей почты в панели мониторинга поток почты в центре соответствия требованиям & безопасности Office 365.
ms.openlocfilehash: 57792c0347490b40f97a8b92945a9c809484ba4f
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685614"
---
# <a name="outbound-and-inbound-mail-flow"></a><span data-ttu-id="8bfba-103">Поток обработки исходящих и входящих сообщений</span><span class="sxs-lookup"><span data-stu-id="8bfba-103">Outbound and inbound mail flow</span></span>

<span data-ttu-id="8bfba-104">Мини-приложения **исходящего соединителя и поток обработки входящей почты** объединяет сведения из **Отчета соединителя** и предыдущих версий **TLS Обзор отчетов** в одном месте.</span><span class="sxs-lookup"><span data-stu-id="8bfba-104">The **Outbound and inbound mail flow** widget combines the information from the **Connector Report** and the former **TLS Overview Report** in one place.</span></span>

![Входящие и исходящие отчета поток почты в панели мониторинга поток почты в центре соответствия требованиям & безопасности Office 365](media/2c591d1c-bad6-4b72-890e-f8fdfd4f447a.png)

<span data-ttu-id="8bfba-p101">Сведения, приведенные в мини-приложения связана с соединители и защита сообщений TLS в Office 365. Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="8bfba-p101">The information in the widget is related to connectors and TLS message protection in Office 365. For more information, see these topics:</span></span>

- [<span data-ttu-id="8bfba-108">Configure mail flow using connectors in Office 365</span><span class="sxs-lookup"><span data-stu-id="8bfba-108">Configure mail flow using connectors in Office 365</span></span>](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx)

- [<span data-ttu-id="8bfba-109">Использование протокола TLS службой Exchange Online для защиты электронной почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="8bfba-109">How Exchange Online uses TLS to secure email connections in Office 365</span></span>](https://support.office.com/article/4CDE0CDA-3430-4DC0-B489-F2C0736C929F)

## <a name="message-protected-in-transit-by-tls"></a><span data-ttu-id="8bfba-110">Сообщения, для защиты во время передачи (TLS)</span><span class="sxs-lookup"><span data-stu-id="8bfba-110">Message protected in transit (by TLS)</span></span>

<span data-ttu-id="8bfba-p102">**Исходящие и поток обработки входящей почты** мини-приложение отображает шифрование TLS, которое используется для подключения к при сообщения будут доставляться в вашу организацию и из Office 365. Подключений, установленных с другими службами электронной почты шифруются с TLS при TLS предлагается в обе стороны. Мини-приложения предоставляет моментальный снимок за прошлую неделю поток почты. При щелчке **Просмотр подробных сведений о**всплывающих **защищенного сообщения во время передачи (Дон Джонс (TLS)** показано защиты TLS для сообщений, ввод и пределами организации.</span><span class="sxs-lookup"><span data-stu-id="8bfba-p102">The **Outbound and inbound mail flow** widget displays the TLS encryption that's used for the connection when messages are delivered to and from your Office 365 organization. The connections that are established with other email services are encrypted by TLS when TLS is offered by both sides. The widget offers a snapshot of the last week of mail flow. When you click **View Details**, the **Message protected in transit (by TLS)** flyout shows you the TLS protection for messages entering and leaving your organization.</span></span>

![Сообщения, защищенные в всплывающего пути (Дон Джонс (TLS) в центре соответствия требованиям & безопасности Office 365](media/825aa74c-413d-4141-8e3c-dfe68ae78eed.png)

<span data-ttu-id="8bfba-p103">На данный момент TLS 1.2 — это самый безопасный версия TLS, предоставляемые Office 365. Часто бывает нужно знать шифрование TLS, который используется для проверки соответствия требованиям. Возможно, у вас нет прямого отношения с большая часть исходной и целевой серверами электронной почты (вы не являетесь их и ни один из ли корпорация Майкрософт), поэтому у вас нет множество возможностей для повышения шифрование TLS, используемый этих серверов.</span><span class="sxs-lookup"><span data-stu-id="8bfba-p103">Currently, TLS 1.2 is the most secure version of TLS that's offered by Office 365. Often, you'll need to know the TLS encryption that's being used for compliance audits. You probably don't have a direct relationship with most of the source and destination email servers (you don't own them, and neither does Microsoft), so you don't have many options to improve the TLS encryption that's used by those servers.</span></span>

<span data-ttu-id="8bfba-p104">Однако можно использовать [соединители](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) для обеспечения наиболее доступные TLS защиту для сообщения, отправленные между серверами электронной почты и Office 365. Поток почты между Office 365 и собственных почтовых серверов или серверов, относящихся к партнеров чаще всего несколько важных и важен, чем обычные сообщения, поэтому может потребоваться применение дополнительной безопасности и бдительность этих сообщений. Можно обновить или исправить серверов электронной почты для улучшения шифрование TLS, который используется или доступ к партнеров на это. **Соединитель отчет** отображает тома поток почты и шифрование TLS для сообщения, использующие ваше соединители Office 365.</span><span class="sxs-lookup"><span data-stu-id="8bfba-p104">But, you can use [connectors](https://technet.microsoft.com/library/ms.exch.eac.connectorselection.aspx) to ensure the best available TLS protection for messages that are sent between your email servers and Office 365. Mail flow between Office 365 and your own email servers or servers that belong to your partners is often more important and sensitive than regular messages, so you'll want to apply extra security and vigilance to those messages. You can upgrade or fix your own email servers to improve the TLS encryption that's being used, or reach out to your partners to do the same. The **Connector Report** displays both mail flow volume and TLS encryption for messages that use your Office 365 connectors.</span></span>

## <a name="connector-report"></a><span data-ttu-id="8bfba-123">Отчет о соединителя</span><span class="sxs-lookup"><span data-stu-id="8bfba-123">Connector report</span></span>

<span data-ttu-id="8bfba-p105">Если щелкнуть ссылку **Отчет о соединителя** из всплывающего **защищенного сообщения во время передачи (Дон Джонс (TLS)** в отчете отображаются сведения о сообщениях, которые будут доставляться в вашу организацию и из Office 365 с помощью соединителей. Использовать соединители между серверов электронной почты и Office 365 или ваш партнер серверов и Office 365. Объем сообщений для каждого соединителя и шифрование TLS для подключения к доступен. Кроме того можно также просмотреть данные для сообщений, отправленных или полученных в Office 365 без использования соединитель.</span><span class="sxs-lookup"><span data-stu-id="8bfba-p105">When you click on the **Connector Report** link from the **Message protected in transit (by TLS)** flyout, the report displays information about messages that are delivered to and from your Office 365 organization using connectors. You use connectors between your own email servers and Office 365 or your partner's servers and Office 365. The message volume for each connector and the TLS encryption for the connection is available. In addition, you can also view data for messages that were sent or received in Office 365 without using a connector.</span></span>

<span data-ttu-id="8bfba-p106">Представление **Поток обработки почты** отображает объем сообщений через соединитель за прошлую неделю. Можно изменить диапазон дат, выбрав **фильтра** , где можно увеличить диапазон для не более 30 дней. Представление **Всех поток обработки почты** содержит весь поток сообщений в вашу организацию и из Office 365 через все соединители. Вы можете выбрать отдельного соединения по имени в раскрывающемся меню.</span><span class="sxs-lookup"><span data-stu-id="8bfba-p106">The **Mail Flow** view shows the volume of messages through the connector for the past week. You can change the date range by selecting **Filter** where you can increase the range to a maximum of 30 days. The **All Mail Flow** view shows all mail flow to and from your Office 365 organization through all connectors. You can select a specific connector by name in the drop down menu.</span></span>

<span data-ttu-id="8bfba-p107">Представление **использования TLS** можно выберите из раскрывающегося просмотреть декомпозиции TLS защиту сообщений через соединитель. Как в отчете по **TLS обзор отчета** , это представление отображает процент в разных версиях TLS. Для подключений TLS 1.0 вы должны получить почтовый сервер или сервер партнера обновлена или фиксированной во избежание проблем при поддержке TLS 1.0 со временем не поддерживаются в Office 365. Для получения дополнительных сведений см [Справочные сведения о шифровании в Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).</span><span class="sxs-lookup"><span data-stu-id="8bfba-p107">You can select the **TLS usage** view from the drop down to see the breakdown of TLS protection for messages through the connector. As with the **TLS Overview Report** report, this view shows the percentage of the different TLS versions. For TLS 1.0 connections, you really need to get your email server or your partner's server upgraded or fixed to avoid any issues when TLS 1.0 support is eventually deprecated in Office 365. For more information, see [Technical reference details about encryption in Office 365](https://support.office.com/article/862cbe93-4268-4ef9-ba79-277545ecf221).</span></span>

<span data-ttu-id="8bfba-p108">Полезные сведения о пункт соединители, помогающие Обратите внимание на потенциальные проблемы шифрование TLS для соединителя. Полезные сведения о являются: **No TLS является более 25%** или **TLS 1.0 превышает 50%**. Если эти исследования, необходимо изучить серверов электронной почты, которые связаны с соединителем или доступ к партнерской организации.</span><span class="sxs-lookup"><span data-stu-id="8bfba-p108">Insights point to connectors to help draw your attention to potential TLS encryption problems for the connector. The insights are: **No TLS is over 25%** or **TLS 1.0 is above 50%**. If you see these insights, you need to investigate your email servers that are associated with the connector, or reach out to your partner organization.</span></span>