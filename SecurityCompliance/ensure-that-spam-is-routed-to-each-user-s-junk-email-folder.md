---
title: Настройка гарантированной отправки нежелательной почты в соответствующую папку каждого пользователя
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
description: Для пользователей EOP нежелательная почта по умолчанию перемещается в соответствующую папку получателя. Чтобы применить это действие к локальным почтовым ящикам, необходимо настроить правила транспорта Exchange на локальных серверах (сервере-концентраторе или пограничном сервере) для обнаружения заголовков нежелательной почты, добавляемых службой EOP. Эти правила транспорта настроят вероятность нежелательной почты, используемую свойством SclJunkThreshold командлета Set-OrganizationConfig, на перемещение спама в соответствующую папку каждого почтового ящика.
ms.openlocfilehash: 290a3cc6aed07cd4d91df65350fd49c9226a0d64
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026636"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Настройка гарантированной отправки нежелательной почты в соответствующую папку каждого пользователя

> [!IMPORTANT]
> Сведения, представленные в этом разделе, касаются только пользователей Exchange Online Protection (EOP), чьи почтовые ящики размещаются локально в гибридном развертывании. Пользователям Exchange Online, чьи почтовые ящики размещаются в Office 365, не нужно выполнять эти команды. 
  
Для пользователей EOP нежелательная почта по умолчанию перемещается в соответствующую папку получателя. Чтобы применить это действие к локальным почтовым ящикам, необходимо настроить правила транспорта Exchange на локальных серверах (сервере-концентраторе или пограничном сервере) для обнаружения заголовков нежелательной почты, добавляемых службой EOP. Эти правила транспорта настроят вероятность нежелательной почты, используемую свойством SclJunkThreshold командлета Set-OrganizationConfig, на перемещение спама в соответствующую папку каждого почтового ящика. 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a>Как добавить правила транспорта для перемещения спама в папку нежелательной почты с помощью Windows PowerShell

1. Откройте командную консоль Exchange для локального сервера Exchange Server. Сведения о том, как открыть командную консоль Exchange в локальной организации Exchange, см. в статье **Open the Shell**.
    
2. Выполните следующую команду, чтобы перенаправлять отфильтрованную по содержимому нежелательную почту в папку "Нежелательная почта":
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    Где  _NameForRule_  имя нового правила, например JunkContentFilteredMail. 
    
3. Выполните следующую команду, чтобы перенаправлять сообщения, отмеченные как нежелательные, перед их попаданием в фильтр содержимого и папку нежелательной почты:
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    Где  _NameForRule_  это имя нового правила, например JunkMailBeforeReachingContentFilter. 
    
4. Выполните следующую команду, чтобы направлять сообщения от заблокированных отправителей, например в списке **блокировок отправителя**, в папку нежелательной почты: 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    Где  _NameForRule_  это имя нового правила, например JunkMailInSenderBlockList. 
    
Если вы не хотите использовать действие **Переместить сообщение в папку нежелательной почты**, можно выбрать другое действие с помощью политик фильтрации содержимого в Центре администрирования Exchange. Дополнительные сведения см. в статье [Настройте политики защиты от спама](configure-your-spam-filter-policies.md). Дополнительные сведения об этих полях в заголовке сообщения см. в статье [Заголовки сообщений по защите от нежелательной почты](anti-spam-message-headers.md).
  
## <a name="see-also"></a>See also

[Командлет New-TransportRule](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

