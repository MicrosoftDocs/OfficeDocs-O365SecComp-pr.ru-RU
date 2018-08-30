---
title: Списки надежных и заблокированных отправителей в Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
description: Чтобы пересылаемые через службу сообщения не помечались как спам, администратор Exchange Online или Exchange Online Protection (EOP) может создать списки надежных и заблокированных отправителей для пользователей в вашей организации.
ms.openlocfilehash: cbf886bdcc40044a31b285b6806aecbc95f0f97c
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003108"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a><span data-ttu-id="42d62-104">Списки надежных и заблокированных отправителей в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="42d62-104">Safe sender and blocked sender lists in Exchange Online</span></span>

<span data-ttu-id="42d62-p102">Чтобы пересылаемые через службу сообщения не помечались как спам, администратор Exchange Online или Exchange Online Protection (EOP) может создать списки надежных и заблокированных отправителей для пользователей в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="42d62-p102">As an Exchange Online or Exchange Online Protection (EOP) administrator, you can help ensure that an email message traveling through the service isn't marked as spam. One way to do this is to create safe sender and blocked sender lists for the people in your organization.</span></span> 
  
 <span data-ttu-id="42d62-107">*Обновленные подсказки и процедуры по работе с этими списками от имени администратора приведены в статье* [Предотвращение попадания электронной почты в спам в EOP и Office 365](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span><span class="sxs-lookup"><span data-stu-id="42d62-107">*See the updated version of the tips and procedures for how to work with these lists as an admin in* [Prevent false positive email marked as spam with a safelist or other techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span></span> 
  
<span data-ttu-id="42d62-108">Если вы не администратор и просто хотите управлять нежелательной почтой в Outlook с помощью списка надежных отправителей, просмотрите общие сведения о [фильтре нежелательной почты](https://go.microsoft.com/fwlink/?LinkId=817222).</span><span class="sxs-lookup"><span data-stu-id="42d62-108">If you're not an admin, and you just want to manage your own junk email in Outlook by using a safe sender list, check out the steps in this overview of [the Junk Email Filter](https://go.microsoft.com/fwlink/?LinkId=817222).</span></span> 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a><span data-ttu-id="42d62-109">Сколько надежных и заблокированных отправителей можно добавить в Exchange Online?</span><span class="sxs-lookup"><span data-stu-id="42d62-109">What is the safe and blocked sender limits in Exchange Online?</span></span>

<span data-ttu-id="42d62-p103">Ограничения на количество надежных и заблокированных отправителей в Exchange Online, Active Directory и Outlook отличаются. Они представлены ниже.</span><span class="sxs-lookup"><span data-stu-id="42d62-p103">The safe and blocked sender limits in Exchange Online differ from the Active Directory and Outlook limits. They are:</span></span>
  
- <span data-ttu-id="42d62-112">Ограничение надежных отправителей: 1 024</span><span class="sxs-lookup"><span data-stu-id="42d62-112">Safe sender limit: 1,024</span></span>
    
- <span data-ttu-id="42d62-113">Ограничение заблокированных отправителей: 500</span><span class="sxs-lookup"><span data-stu-id="42d62-113">Blocked sender limit: 500</span></span>
    
<span data-ttu-id="42d62-114">Примечание.</span><span class="sxs-lookup"><span data-stu-id="42d62-114">Note:</span></span>
  
<span data-ttu-id="42d62-p104">Могут возникать ошибки, описанные в КБ 2590466 («ошибка «Ошибка проверки нежелательной электронной почты» в Outlook Web App для Exchange Server 2010»). Чтобы устранить эту проблему, снимите флажок «Доверять от личных контактов по электронной почте». Кроме того сократить адресов электронной почты, которые являются в папке контактов по умолчанию для переноса в максимально допустимое не более 1 024 в Exchange Online, задайте для атрибута «MaxSafeSenders». Дополнительные сведения о этот атрибут и командлет Set-Mailbox seethe следующий раздел:</span><span class="sxs-lookup"><span data-stu-id="42d62-p104">You may experience the error that is described in KB 2590466 ("You receive the error "Junk e-mail validation error" in Outlook Web App for Exchange Server 2010"). To resolve this issue, clear the "Trust emails from my contacts" check box. Alternatively, decrease the amount of email addresses that are in your default Contacts folder to bring it within the maximum allowed limit of 1,024 in Exchange Online that is set for "MaxSafeSenders" attribute. For more information about this attribute and the Set-Mailbox cmdlet, seethe following topic:</span></span>
  
[<span data-ttu-id="42d62-119">Set-Mailbox</span><span class="sxs-lookup"><span data-stu-id="42d62-119">Set-Mailbox</span></span>](https://docs.microsoft.com/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a><span data-ttu-id="42d62-120">See also</span><span class="sxs-lookup"><span data-stu-id="42d62-120">See also</span></span>

[<span data-ttu-id="42d62-121">Sender filtering in Exchange 2016</span><span class="sxs-lookup"><span data-stu-id="42d62-121">Sender filtering in Exchange 2016</span></span>](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

