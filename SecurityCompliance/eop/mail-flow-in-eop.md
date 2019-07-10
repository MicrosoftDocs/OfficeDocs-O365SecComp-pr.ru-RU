---
title: Поток обработки почты в службе EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 3/13/2015
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: e109077e-cc85-4c19-ae40-d218ac7d0548
description: Поскольку вы являетесь пользователем Exchange Online Protection (EOP), все сообщения, отправляемые в организацию, проходят через службу EOP перед доставкой сотрудникам. Если все ваши почтовые ящики находятся в облаке с Exchange Online или хранятся локально (т. е. используется изолированный сценарий), возможно, для дальнейшего использования текущей инфраструктуры у вас есть возможности направлять сообщения, проходящие через службу EOP, для обработки, прежде чем они будут доставлены в папки "Входящие" ваших сотрудников.
ms.openlocfilehash: 60ac643e70805de7937a12c9b8f08b593ecd8aab
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599655"
---
# <a name="mail-flow-in-eop"></a><span data-ttu-id="b4cf3-104">Поток обработки почты в службе EOP</span><span class="sxs-lookup"><span data-stu-id="b4cf3-104">Mail flow in EOP</span></span>

<span data-ttu-id="b4cf3-p102">Поскольку вы являетесь пользователем Exchange Online Protection (EOP), все сообщения, отправляемые в организацию, проходят через службу EOP перед доставкой сотрудникам. Если все ваши почтовые ящики находятся в облаке с Exchange Online или хранятся локально (т. е. используется изолированный сценарий), возможно, для дальнейшего использования текущей инфраструктуры у вас есть возможности направлять сообщения, проходящие через службу EOP, для обработки, прежде чем они будут доставлены в папки "Входящие" ваших сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-p102">As an Exchange Online Protection (EOP) customer, all messages sent to your organization pass through EOP before your workers see them. Whether you host all of your mailboxes in the cloud with Exchange Online, or you host your mailboxes on premises (called a standalone scenario), perhaps to continue taking advantage of your existing infrastructure, you have options about how to route messages that will pass through EOP for processing before they are routed to your worker inboxes.</span></span>
  
<span data-ttu-id="b4cf3-p103">Возможно, следует настроить пользовательскую маршрутизацию почты, чтобы привести обмен сообщениями в соответствие с вашими бизнес-требованиями. Например, вы можете задать прохождение всей исходящей почты через устройство фильтрации политики.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-p103">You may want to configure custom mail routing to conform your messaging to a business requirement. For instance, you can pass all of your outbound mail through a policy-filtering appliance.</span></span> 
  
## <a name="working-with-messages-and-message-access-options"></a><span data-ttu-id="b4cf3-109">Возможности для работы с сообщениями и доступа к ним</span><span class="sxs-lookup"><span data-stu-id="b4cf3-109">Working with messages and message access options</span></span>

<span data-ttu-id="b4cf3-p104">Служба EOP позволяет гибко маршрутизировать сообщения. В указанных ниже разделах описаны шаги процесса потока обработки почты.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-p104">EOP offers a lot of flexibility in how your messages are routed. The following topics explain steps in the mail flow process.</span></span>
  
<span data-ttu-id="b4cf3-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Описание функции "Пограничная блокировка на основе каталогов", которая позволяет отклонять сообщения для недопустимых получателей в периметре сервисной сети.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-112">[Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx) Describes the Directory Based Edge Blocking feature which lets you reject messages for invalid recipients at the service network perimeter.</span></span> 
  
<span data-ttu-id="b4cf3-113">В разделе [View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) описано, как управлять доменами, сопоставленными со службой EOP.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-113">[View or Edit Managed Domains in EOP](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains) describes how to manage domains that are associated with your EOP service.</span></span> 
  
<span data-ttu-id="b4cf3-p105">Если вы добавляете поддомены в организацию, служба EOP поможет вам управлять и ими. Дополнительные сведения о поддоменах см. в разделе [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span><span class="sxs-lookup"><span data-stu-id="b4cf3-p105">If you add subdomains to your organization, your EOP service can help you manage these too. Learn more about subdomains at [Enable Mail Flow for Subdomains in Exchange Online](http://technet.microsoft.com/library/4033a30a-f506-481c-8ef0-fd9a0508ae38.aspx).</span></span>
  
<span data-ttu-id="b4cf3-p106">В разделе [Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) описываются соединители и их использование для настройки маршрутизации почты. Среди сценариев обеспечение безопасной связи с партнерской организацией и настройка промежуточного узла.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-p106">[Configure mail flow using connectors in Office 365](http://technet.microsoft.com/library/854b5a50-4462-4836-a092-37e208d29624.aspx) introduces connectors and shows how you can use them to customize mail routing. Scenarios include ensuring secure communication with a partner organization and setting up a smart host.</span></span> 
  
<span data-ttu-id="b4cf3-118">Чтобы убедиться, что нежелательная почта правильно направляется в папку нежелательной почты каждого пользователя, необходимо выполнить несколько действий по настройке.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-118">To ensure that junk email is routed correctly to each user's junk-email folder, you must perform a couple configuration steps.</span></span> <span data-ttu-id="b4cf3-119">Это подробное описание [того, что спам направляется в папку нежелательной почты каждого пользователя](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span><span class="sxs-lookup"><span data-stu-id="b4cf3-119">These are detailed in [Ensure that spam is routed to each user's Junk Email folder](../ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md).</span></span> <span data-ttu-id="b4cf3-120">Если вы не хотите перемещать сообщения в папку нежелательной почты каждого пользователя, вы можете выбрать другое действие, отредактировав политики фильтрации содержимого в центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-120">If you do not want to move messages to each user's junk-email folder, you may choose another action by editing your content filter policies in the Exchange admin center.</span></span> <span data-ttu-id="b4cf3-121">Дополнительные сведения см. в статье [Configure your spam filter policies](../configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b4cf3-121">For more information, see [Configure your spam filter policies](../configure-your-spam-filter-policies.md).</span></span>
  
## <a name="verify-mail-flow"></a><span data-ttu-id="b4cf3-122">Проверка потока почты</span><span class="sxs-lookup"><span data-stu-id="b4cf3-122">Verify mail flow</span></span>

<span data-ttu-id="b4cf3-p108">Чтобы убедиться в правильности настройки EOP, включая конфигурацию соединителей, см. раздел "Проверка выполнения" в [Настройка службы EOP](set-up-your-eop-service.md).</span><span class="sxs-lookup"><span data-stu-id="b4cf3-p108">To verify that your EOP setup, including your connector configuration, is working correctly, see the "How do you know this task worked?" section in [Set up your EOP service](set-up-your-eop-service.md).</span></span> 
  
<span data-ttu-id="b4cf3-125">В разделе [Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) приводятся инструкции по проверке правильности настройки потока обработки почты.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-125">[Test Mail Flow with the Remote Connectivity Analyzer](http://technet.microsoft.com/library/6c8c2964-d553-4329-8166-6e508dd63fa0.aspx) provides instructions for testing that your mail flow is set up correctly.</span></span> 
  

