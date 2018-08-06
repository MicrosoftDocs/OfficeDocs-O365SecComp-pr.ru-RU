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
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
description: Чтобы пересылаемые через службу сообщения не помечались как спам, администратор Exchange Online или Exchange Online Protection (EOP) может создать списки надежных и заблокированных отправителей для пользователей в вашей организации.
ms.openlocfilehash: fcb43f990750782788dc6f459dd5c7d296146a38
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22028086"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a>Списки надежных и заблокированных отправителей в Exchange Online

Чтобы пересылаемые через службу сообщения не помечались как спам, администратор Exchange Online или Exchange Online Protection (EOP) может создать списки надежных и заблокированных отправителей для пользователей в вашей организации. 
  
 *Обновленные подсказки и процедуры по работе с этими списками от имени администратора приведены в статье* [Предотвращение попадания электронной почты в спам в EOP и Office 365](https://go.microsoft.com/fwlink/p/?LinkID=534224). 
  
Если вы не администратор и просто хотите управлять нежелательной почтой в Outlook с помощью списка надежных отправителей, просмотрите общие сведения о [фильтре нежелательной почты](https://go.microsoft.com/fwlink/?LinkId=817222). 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a>Сколько надежных и заблокированных отправителей можно добавить в Exchange Online?

Ограничения на количество надежных и заблокированных отправителей в Exchange Online, Active Directory и Outlook отличаются. Они представлены ниже.
  
- Ограничение надежных отправителей: 1 024
    
- Ограничение заблокированных отправителей: 500
    
Примечание.
  
Могут возникать ошибки, описанные в КБ 2590466 («ошибка «Ошибка проверки нежелательной электронной почты» в Outlook Web App для Exchange Server 2010»). Чтобы устранить эту проблему, снимите флажок «Доверять от личных контактов по электронной почте». Кроме того сократить адресов электронной почты, которые являются в папке контактов по умолчанию для переноса в максимально допустимое не более 1 024 в Exchange Online, задайте для атрибута «MaxSafeSenders». Дополнительные сведения о этот атрибут и командлет Set-Mailbox seethe следующий раздел:
  
[Set-Mailbox](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a>See also

[Sender filtering in Exchange 2016](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

