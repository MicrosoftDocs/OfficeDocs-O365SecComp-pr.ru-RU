---
title: Управление списками надежных отправителей при массовой рассылке почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
description: При использовании списков надежных отправителей следует учитывать, что обработка в службе Exchange Online Protection (EOP) и программе Outlook несколько отличается. Служба рассматривает надежных отправителей и домены, проверяя RFC-адреса 5321.MailFrom и 5322.From, в то время как программа Outlook добавляет RFC-адрес 5322.From в список надежных отправителей пользователя. (Примечание. Для заблокированных пользователей и доменов служба проверяет адреса 5321.MailFrom и 5322.From.)
ms.openlocfilehash: 9442bb39e15b9db9a826472dd6110a8fa14130c6
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002998"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a><span data-ttu-id="a21ad-105">Управление списками надежных отправителей при массовой рассылке почты</span><span class="sxs-lookup"><span data-stu-id="a21ad-105">Manage safe sender lists for bulk mailers</span></span>

<span data-ttu-id="a21ad-p102">При использовании списков надежных отправителей следует учитывать, что обработка в службе Exchange Online Protection (EOP) и программе Outlook несколько отличается. Служба рассматривает надежных отправителей и домены, проверяя RFC-адреса 5321.MailFrom и 5322.From, в то время как программа Outlook добавляет RFC-адрес 5322.From в список надежных отправителей пользователя. (Примечание. Для заблокированных пользователей и доменов служба проверяет адреса 5321.MailFrom и 5322.From.)</span><span class="sxs-lookup"><span data-stu-id="a21ad-p102">If you want to use safe sender lists, you should know that Exchange Online Protection (EOP) and Outlook handle processing differently. The service respects safe senders and domains by inspecting the RFC 5321.MailFrom address and the RFC 5322.From address, while Outlook adds the RFC 5322.From address to a user's safe sender list. (Note: The service inspects both the 5321.MailFrom address and 5322.From address for blocked senders and domains.)</span></span>
  
<span data-ttu-id="a21ad-p103">SMTP-адрес MAIL FROM (он же  RFC-адрес 5321.MailFrom)  это адрес электронной почты, который используется для выполнения проверок инфраструктуры политики отправителей. Он также выступает в роли пути, по которому доставляется сообщение о недоставке, если не удается доставить почту. Этот адрес электронной почты вставляется в Return-Path в заголовках сообщений по умолчанию, хотя отправитель может указать другой адрес Return-Path.</span><span class="sxs-lookup"><span data-stu-id="a21ad-p103">The SMTP MAIL FROM address, otherwise known as the RFC 5321.MailFrom address, is the email address that's used to perform SPF checks, and if the mail can't be delivered, the path to which the bounced message is delivered. It's this email address that is placed into the Return-Path in the message headers by default, though it's possible for the sender to designate a different Return-Path address.</span></span>
  
<span data-ttu-id="a21ad-111">Адрес "От:" в заголовках сообщений (он же  RFC-адрес 5322.From)  это адрес электронной почты, который отображается в почтовом клиенте, например Outlook.</span><span class="sxs-lookup"><span data-stu-id="a21ad-111">The From: address in the message headers, otherwise known as the RFC 5322.From address, is the email address that is displayed in the mail client such as Outlook.</span></span>
  
<span data-ttu-id="a21ad-p104">Чаще всего адреса 5321.MailFrom и 5322.From совпадают, обычно в случае взаимодействия между пользователями. Но при отправке сообщений от чужого имени эти адреса чаще всего различаются. Это характерно для массовой рассылки сообщений.</span><span class="sxs-lookup"><span data-stu-id="a21ad-p104">Much of the time, the 5321.MailFrom and 5322.From addresses are the same. This is typical for person-to-person communication. However, when email is sent on behalf of someone else, the addresses are frequently different. This usually happens most often for bulk email messages.</span></span>
  
<span data-ttu-id="a21ad-p105">Например, предположим, что авиалиния Blue Yonder Airlines наняла компанию Margie's Travel для отправки рекламных сообщений по электронной почте. Затем в вашу папку "Входящие" приходит сообщение от отправителя blueyonder@news.blueyonderairlines.com. В таком случае адрес 5321.MailFrom  это blueyonder.airlines@margiestravel.com, а blueyonder@news.blueyonderairlines.com  это адрес 5322.From, и именно он отображается в Outlook. Поскольку служба рассматривает адрес RFC 5322.From, во избежание фильтрации этого сообщения вы можете просто добавить RFC-адрес 5322.From в качестве надежного отправителя в Outlook.</span><span class="sxs-lookup"><span data-stu-id="a21ad-p105">For example, suppose that the airline Blue Yonder Airlines has contracted out Margie's Travel to send out its email advertising. You then get a message in your inbox from sender blueyonder@news.blueyonderairlines.com. In this case, the 5321.MailFrom address is blueyonder.airlines@margiestravel.com, and blueyonder@news.blueyonderairlines.com is the 5322.From address which is the one you see in Outlook. Because the service respects the RFC 5322.From address, to prevent this message from getting filtered, you can simply add the RFC 5322.From address as a safe sender in Outlook.</span></span>
  

