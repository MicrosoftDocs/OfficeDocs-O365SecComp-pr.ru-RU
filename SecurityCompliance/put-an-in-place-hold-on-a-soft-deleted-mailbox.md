---
title: Назначение удержания на месте для обратимо удаленного почтового ящика в Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Узнайте, как создать запрос удержания на месте для обратимо удаленного почтового ящика, чтобы сделать последний неактивным и сохранить его содержимое. После этого вы сможете использовать средства обнаружения электронных данных для поиска в неактивном почтовом ящике.
ms.openlocfilehash: f5ac31b4bfd993bf384aa17ba5f71de937cec720
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999512"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a>Назначение удержания на месте для обратимо удаленного почтового ящика в Exchange Online

Узнайте, как создать запрос удержания на месте для обратимо удаленного почтового ящика, чтобы сделать последний неактивным и сохранить его содержимое. После этого вы сможете использовать средства обнаружения электронных данных для поиска в неактивном почтовом ящике.
  
> [!NOTE]
> Мы отложили крайний срок создания новых удержаний на месте в Exchange Online (в автономных планах Office 365 и Exchange Online). But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. В качестве альтернативы удержанию на месте можно использовать [случаи обнаружения электронных](https://go.microsoft.com/fwlink/?linkid=780738) данных или [политики хранения](https://go.microsoft.com/fwlink/?linkid=827811) в центре безопасности _амп_ соответствия требованиям. After we decommission new In-Place Holds, you'll still be able to modify existing In-Place Holds, and creating new In-Place Holds in Exchange Server 2013 and Exchange hybrid deployments will still be supported. And, you'll still be able to place mailboxes on Litigation Hold. 
  
You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted. Afterwards, you realize there's information in the mailbox that needs to be preserved. What can you do? If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox. An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization. The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive. После неактивного почтового ящика можно выполнить поиск в почтовом ящике, используя обнаружение электронных данных на месте в Exchange Online, поиск контента в центре безопасности _Амп_ соответствия требованиям или в центре обнаружения электронных данных в SharePoint Online. 
  
> [!NOTE]
> В Exchange Online обратимо удаленный почтовый ящик  почтовый ящик, который был удален, но может быть восстановлен в течение определенного срока хранения (в Exchange Online он составляет 30 дней). Это значит, что такой почтовый ящик можно восстановить или сделать неактивным в течение 30 дней после удаления. По истечении этого периода обратимо удаленный почтовый ящик помечается для окончательного удаления, и в этом случае его уже невозможно восстановить или сделать неактивным. 
  
## <a name="before-you-begin"></a>Перед началом работы

- Примените командлет **New-MailboxSearch** в Оболочка Windows PowerShell, чтобы назначить удержание на месте для обратимо удаленного почтового ящика. В SharePoint Online вы не можете использовать Центр администрирования Exchange (EAC) или центр обнаружения электронных данных. 
    
- Сведения о том, как с помощью Оболочка Windows PowerShell подключаться к Exchange Online, см. в статье [Подключение к PowerShell для Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Выполните указанную ниже команду, чтобы отобразить удостоверения обратимо удаленных почтовых ящиков в организации. 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- Дополнительные сведения о неактивных почтовых ящиках можно найти [в статье Обзор неактивных почтовых ящиков в Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a>Назначение удержания на месте для обратимо удаленного почтового ящика, чтобы сделать последний неактивным

С помощью командлета **New-MailboxSearch** сделайте обратимо удаленный почтовый ящик неактивным. Дополнительные сведения см. в статье [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).
  
1. Создайте переменную, содержащую свойства обратимо удаленного почтового ящика. 
    
   ```
   $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
   ```

    > [!IMPORTANT]
    > В указанной выше команде используйте значение свойства **DistinguishedName** или **ExchangeGuid** для определения обратимо удаленного почтового ящика. Эти свойства уникальны для каждого почтового ящика в организации, тогда как у активного и обратимо удаленного почтовых ящиков может быть один и тот же основной SMTP-адрес. 
  
2. Создайте запрос удержания на месте и назначьте его для обратимо удаленного почтового ящика. В этом примере не указан период удержания. Это означает, что элементы будут храниться в течение неограниченного срока или до тех пор, пока для неактивного почтового ящика не будет отменено удержание.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
    ```
   Кроме того, вы можете указать длительность удержания при создании запроса удержания на месте. В этом примере элементы в неактивном почтовом ящике удерживаются около 7 лет.
    
   ```
   New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
   ```

3. Через пару минут запустите одну из указанных ниже команд, чтобы убедиться в неактивности этого обратимо удаленного почтового ящика.
    
   ```
   Get-Mailbox -InactiveMailboxOnly
   ```

    Еще вариант:
    
   ```
   Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
   ```

## <a name="more-information"></a>Дополнительные сведения

Сделав обратимо удаленный почтовый ящик неактивным, вы сможете управлять им несколькими способами. Дополнительные сведения см. в таких статьях:
  
- [Изменение срока хранения неактивного почтового ящика](change-the-hold-duration-for-an-inactive-mailbox.md)
    
- [Возврат неактивного почтового ящика](recover-an-inactive-mailbox.md)
    
- [Восстановление неактивного почтового ящика](restore-an-inactive-mailbox.md)
    
- [Удаление](delete-an-inactive-mailbox.md) неактивного почтового ящика (за исключением удержания)
