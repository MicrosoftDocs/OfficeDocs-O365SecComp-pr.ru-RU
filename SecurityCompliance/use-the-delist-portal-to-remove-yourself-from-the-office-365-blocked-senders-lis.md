---
title: Удаление себя из списка заблокированных отправителей Office 365 с помощью портала удаления из списка
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/18/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
description: Вы получаете сообщение об ошибке каждый раз, когда пытаетесь отправить сообщение получателю, адрес электронной почты которого зарегистрирован в Office 365? Если вы считаете, что это недоразумение, воспользуйтесь порталом удаления из списка, чтобы удалить себя из списка заблокированных отправителей Office 365.
ms.openlocfilehash: 4964429f4d3aa1a585b1b543929f83c2cebfb9a4
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003258"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a><span data-ttu-id="bf9f4-104">Удаление себя из списка заблокированных отправителей Office 365 с помощью портала удаления из списка</span><span class="sxs-lookup"><span data-stu-id="bf9f4-104">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>

<span data-ttu-id="bf9f4-p102">Вы получаете сообщение об ошибке каждый раз, когда пытаетесь отправить сообщение получателю, адрес электронной почты которого зарегистрирован в Office 365? Если вы считаете, что это недоразумение, воспользуйтесь порталом удаления из списка, чтобы удалить себя из списка заблокированных отправителей Office 365.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p102">Are you getting an error message when you try to send an email to a recipient whose email address is in Office 365? If you think you should not be receiving the error message, you can use the delist portal to remove yourself from the Office 365 blocked senders list.</span></span>
  
## <a name="what-is-the-office-365-blocked-senders-list"></a><span data-ttu-id="bf9f4-107">Что такое список заблокированных отправителей Office 365?</span><span class="sxs-lookup"><span data-stu-id="bf9f4-107">What is the Office 365 blocked senders list?</span></span>

<span data-ttu-id="bf9f4-p103">Майкрософт использует этот список, чтобы защитить своих клиентов от спама, спуфинга и фишинг-атак. По какой-то причине IP-адрес вашего почтового сервера помечен в Office 365 как представляющий потенциальную угрозу. Добавление IP-адреса в список заблокированных отправителей Office 365 позволяет предотвратить обмен данными между этим IP-адресом и нашими пользователями через наши центры данных.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p103">Microsoft uses the blocked senders list to protect its customers from spam, spoofing, and phishing attacks. Your mail server's IP address, that is, the address your mail server uses to identify itself on the Internet, was tagged as a potential threat to Office 365 for one of a variety of reasons. When Office 365 adds the IP address to the list, it prevents all further communication between the IP address and any of our customers through our datacenters.</span></span>
  
<span data-ttu-id="bf9f4-111">Если ваш адрес внесен в список заблокированных отправителей, то в ответ на отправленное письмо вы получаете сообщение об ошибке примерно следующего вида:</span><span class="sxs-lookup"><span data-stu-id="bf9f4-111">You will know you have been added to the list when you receive a response to a mail message that includes an error that looks something like this:</span></span>
  
<span data-ttu-id="bf9f4-p104">550 5.7.606-649, отказано в доступе, запрещенный отправки IP-адресов [_IP-адрес_]; Чтобы запросить удаления из этого списка посетите веб- https://sender.office.com/ и следуйте инструкциям. Дополнительные сведения можно найти в [отчеты о недоставке электронной почты в Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p104">550 5.7.606-649 Access denied, banned sending IP [_IP address_]; To request removal from this list please visit https://sender.office.com/ and follow the directions. For more information please see [Email non-delivery reports in Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span></span>
  
<span data-ttu-id="bf9f4-114">где  _IP address_  IP-адрес компьютера, на котором запущен почтовый сервер.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-114">where  _IP address_ is the IP address of the computer on which the mail server runs.</span></span> 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="bf9f4-115">Использование портала удаления из списка в Office 365 для удаления себя из списка заблокированных отправителей</span><span class="sxs-lookup"><span data-stu-id="bf9f4-115">To use the Office 365 delist portal to remove yourself from the blocked senders list</span></span>

1. <span data-ttu-id="bf9f4-116">В веб-браузере перейдите по адресу [https://sender.office.com](https://sender.office.com)</span><span class="sxs-lookup"><span data-stu-id="bf9f4-116">In a web browser, go to [https://sender.office.com](https://sender.office.com).</span></span>
    
2. <span data-ttu-id="bf9f4-p105">и следуйте инструкциям на странице. Убедитесь, что указали тот адрес электронной почты, на который пришло сообщение об ошибке, и введите указанный в нем IP-адрес. За одно посещение можно указать только один адрес электронной почты и IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p105">Follow the instructions on the page. Ensure that you use the email address to which the error message was sent, and the IP address that is specified in the error message. You can only enter one email address and one IP address per visit.</span></span>
    
3. <span data-ttu-id="bf9f4-120">Нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-120">Click **Submit**.</span></span>
    
    <span data-ttu-id="bf9f4-p106">Портал отправляет сообщение электронной почты на адрес электронной почты, который необходимо предоставить. Сообщение электронной почты будет выглядеть примерно следующим образом: ![снимок экрана электронной почты, полученных при отправке запроса через портал delist](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p106">The portal sends an email to the email address that you supply. The email will look something like the following:  ![Screenshot of email received when you submit a request through the delist portal](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span></span>
  
4. <span data-ttu-id="bf9f4-123">В полученном письме нажмите ссылку подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-123">Click the confirmation link in the email sent to you by the delisting portal.</span></span>
    
    <span data-ttu-id="bf9f4-124">Вы вернетесь на портал удаления из списка.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-124">This brings you back to the delist portal.</span></span>
    
5. <span data-ttu-id="bf9f4-125">Здесь выберите **Удалить IP-адрес из списка**.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-125">In the delist portal, click **Delist IP**.</span></span>
    
    <span data-ttu-id="bf9f4-p107">После удаления IP-адреса из списка заблокированных отправителей сообщения с этого IP-адреса будут доставляться получателям, которые используют Office 365. Убедитесь, что с этого IP-адреса не будут отправляться оскорбительные или вредоносные сообщения. В противном случае IP-адрес может быть заблокирован снова.</span><span class="sxs-lookup"><span data-stu-id="bf9f4-p107">After the IP address is removed from the blocked senders list, email messages from that IP address will be delivered to recipients who use Office 365. So, make sure you're confident that email sent from that IP address won't be abusive or malicious; otherwise, the IP address might be blocked again.</span></span>
    

