---
title: Пример уведомления, отправляемого в случае блокирования отправки спама для отправителя
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 11/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c33fd406-a4c8-4ac8-ad85-123996c5cded
ms.collection:
- M365-security-compliance
description: 'Когда в службе блокируется отправитель за рассылку спама, администратор домена (которого вы указали с помощью действий, описанных в статье Настройка правил защиты от спама для исходящих сообщений) получает по электронной почте уведомление, подобное следующему:'
ms.openlocfilehash: 04d8bde8e9cadd3525191a5bee7d368229e85056
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260977"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a><span data-ttu-id="5b3a2-103">Пример уведомления, отправляемого в случае блокирования отправки спама для отправителя</span><span class="sxs-lookup"><span data-stu-id="5b3a2-103">Sample notification when a sender is blocked sending outbound spam</span></span>

<span data-ttu-id="5b3a2-104">Когда в службе блокируется отправитель за рассылку спама, администратор домена (которого вы указали с помощью действий, описанных в статье [Настройка правил защиты от спама для исходящих сообщений](configure-the-outbound-spam-policy.md)) получает по электронной почте уведомление, подобное следующему:</span><span class="sxs-lookup"><span data-stu-id="5b3a2-104">When a sender is blocked from the service due to sending outbound spam, the domain admin specified when you [Configure the outbound spam policy](configure-the-outbound-spam-policy.md) will receive a notification email similar to the following:</span></span> 
  
 <span data-ttu-id="5b3a2-105">**Адрес отправителя:** spamalerts@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5b3a2-105">**Sender address:** spamalerts@microsoft.com</span></span> 
  
 <span data-ttu-id="5b3a2-106">**Тема:** Уведомление об исходящем спаме: заблокирована отправка почты из \<  *имя учетной записи*  \></span><span class="sxs-lookup"><span data-stu-id="5b3a2-106">**Subject:** Outbound spam notification - \<  *account name*  \> blocked from sending outbound mail</span></span> 
  
 <span data-ttu-id="5b3a2-107">**Текст сообщения:** Это автоматический ответ от системы анализа спама Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-107">**Body:** This is an automated reply from the Exchange Online Protection Spam Analysis System.</span></span> 
  
<span data-ttu-id="5b3a2-p101">Вы получили это сообщение, так как из вашей организации исходит много спама или мы заметили другие подозрительные действия. Мы заблокировали отправку почты из следующих учетных записей (они по-прежнему могут получать почту):</span><span class="sxs-lookup"><span data-stu-id="5b3a2-p101">You are being contacted because we have detected high volumes of email marked as spam, or other suspicious behavior, originating from your organization. The following email accounts have been blocked from sending email (they can still receive email):</span></span>
  
<span data-ttu-id="5b3a2-110">\< *имя учетной записи*  \></span><span class="sxs-lookup"><span data-stu-id="5b3a2-110">\< *account name*  \></span></span> 
  
<span data-ttu-id="5b3a2-p102">Возможно, эта учетная запись электронной почты была взломана. Выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5b3a2-p102">It is likely that this email account has been compromised. Please follow these steps:</span></span>
  
1. <span data-ttu-id="5b3a2-113">Прежде всего:</span><span class="sxs-lookup"><span data-stu-id="5b3a2-113">Resolve this issue on your side by:</span></span>
    
  - <span data-ttu-id="5b3a2-114">Измените пароль учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-114">Changing the password of the account.</span></span>
    
  - <span data-ttu-id="5b3a2-115">Определите способ взлома учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-115">Determining how the account was compromised.</span></span>
    
  - <span data-ttu-id="5b3a2-116">Примите меры, чтобы предотвратить повторное использование этой уязвимости.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-116">Taking precautions to ensure that this vulnerability will not be exploited again.</span></span>
    
  - <span data-ttu-id="5b3a2-117">Удалите из очереди исходящей почты все сообщения, которые нарушают наши правила.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-117">Confirming that your outbound mail queue has been cleared of all offending messages.</span></span>
    
2. <span data-ttu-id="5b3a2-118">Обратитесь в службу поддержки Майкрософт по своему обычному каналу связи.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-118">Contact Microsoft support by using your regular contact channel.</span></span>
    
3. <span data-ttu-id="5b3a2-119">Сообщите, что проблема, из-за которой была заблокирована отправка почты, устранена.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-119">Explain that you have a user that is blocked from sending mail and that the problem has been dealt with.</span></span>
    
4. <span data-ttu-id="5b3a2-120">Агент передаст предоставленную вами информацию в службу поддержки для разблокировки адреса электронной почты или домена.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-120">The agent will create a support ticket with the information that you provide and escalate it to have the email address or domain unblocked.</span></span>
    
5. <span data-ttu-id="5b3a2-121">После разблокировки (при отсутствии других проблем) вы получите соответствующее уведомление.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-121">After the address has been unblocked, and pending no other issues, you will be contacted and alerted to the unblocking.</span></span>
    
<span data-ttu-id="5b3a2-122">Спасибо, что помогаете нам бороться с нежелательной электронной почтой.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-122">Thank you for assisting us in controlling unwanted email.</span></span>
  
<span data-ttu-id="5b3a2-123">Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="5b3a2-123">Exchange Online Protection.</span></span>
  
<span data-ttu-id="5b3a2-124">\*\*ПРИМЕЧАНИЕ. Не отвечайте на это сообщение электронной почты, так как оно отправлено с адреса, который не отслеживается\*\*</span><span class="sxs-lookup"><span data-stu-id="5b3a2-124">\*\*NOTE - Please do not respond to this email as it is sent from an unmonitored address\*\*</span></span>
  
> [!TIP]
> <span data-ttu-id="5b3a2-125">Вы также можете обратиться в службу поддержки с помощью параметров, описанных в [справке и поддержке EOP](eop/help-and-support-for-eop.md).</span><span class="sxs-lookup"><span data-stu-id="5b3a2-125">You can also contact support via the options documented at [Help and support for EOP](eop/help-and-support-for-eop.md).</span></span> 
  

