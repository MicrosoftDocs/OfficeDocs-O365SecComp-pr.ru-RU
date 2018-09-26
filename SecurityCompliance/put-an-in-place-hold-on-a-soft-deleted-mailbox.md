---
title: Назначение удержания на месте для обратимо удаленного почтового ящика в Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Узнайте, как создать запрос удержания на месте для обратимо удаленного почтового ящика, чтобы сделать последний неактивным и сохранить его содержимое. После этого вы сможете использовать средства обнаружения электронных данных для поиска в неактивном почтовом ящике.
ms.openlocfilehash: b4ef4ee26e98c8234f64d0879391f8fec89ffd3c
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038252"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a><span data-ttu-id="e70d4-104">Назначение удержания на месте для обратимо удаленного почтового ящика в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="e70d4-104">Put an In-Place Hold on a soft-deleted mailbox in Exchange Online</span></span>

<span data-ttu-id="e70d4-p102">Узнайте, как создать запрос удержания на месте для обратимо удаленного почтового ящика, чтобы сделать последний неактивным и сохранить его содержимое. После этого вы сможете использовать средства обнаружения электронных данных для поиска в неактивном почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="e70d4-p102">Learn how to create an In-Place Hold for a soft-deleted mailbox to make it inactive and preserve its contents. Then you can use Microsoft eDiscovery tools to search the inactive mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e70d4-p103">Мы отложено крайний срок 1 июля 2017 по созданию новых удержание на месте в Exchange Online (в отдельных планах Office 365 и Exchange Online). Однако в этом году или первых следующего года, не сможет создать удержание на месте в Exchange Online. В качестве альтернативы, используя удержание на месте, можно использовать [вариантах eDiscovery](https://go.microsoft.com/fwlink/?linkid=780738) и [политики хранения](https://go.microsoft.com/fwlink/?linkid=827811) безопасности Office 365 &amp; центре соответствия требованиям. После мы выводить из эксплуатации создать удержание на месте, по-прежнему сможет изменение существующей удержание на месте и создание новых удержание на месте в Exchange Server 2013 и гибридных развертываний Exchange будет по-прежнему будут поддерживаться. И, по-прежнему смогут помещение почтовых ящиков на хранение для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="e70d4-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds in Exchange Online (in Office 365 and Exchange Online standalone plans). But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. As an alternative to using In-Place Holds, you can use [eDiscovery cases](https://go.microsoft.com/fwlink/?linkid=780738) or [retention policies](https://go.microsoft.com/fwlink/?linkid=827811) in the Office 365 Security &amp; Compliance Center. After we decommission new In-Place Holds, you'll still be able to modify existing In-Place Holds, and creating new In-Place Holds in Exchange Server 2013 and Exchange hybrid deployments will still be supported. And, you'll still be able to place mailboxes on Litigation Hold.</span></span> 
  
<span data-ttu-id="e70d4-p104">Возможно случаев, когда пользователь покинул вашей организации, и их соответствующая учетная запись пользователя и почтовый ящик были удалены. После этого вы понимаем, что сведения в почтовый ящик, который необходимо сохранить. Что можно сделать? Если еще не истек срок хранения удаленных почтовых ящиков, можно перевести хранение на месте на удаленный почтовый ящик, (называемые почтового ящика, удаленные) и сделать его неактивного почтового ящика. *Неактивного почтового ящика* используется для хранения электронной переписки бывший сотрудник, после он или она уволится из вашей организации. Содержимое неактивного почтового ящика, сохраняются для продолжительность удержания на месте, которое было помещается на удаленный почтовый ящик, когда было выполнено неактивных. После внесения в неактивного почтового ящика можно выполнить поиск почтового ящика с помощью электронного обнаружения на месте в Exchange Online поиска контента в Office 365 безопасность &amp; соответствия требованиям, или центра обнаружения электронных данных в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="e70d4-p104">You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted. Afterwards, you realize there's information in the mailbox that needs to be preserved. What can you do? If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox. An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization. The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive. After the mailbox is made inactive, you can search the mailbox by using In-Place eDiscovery in Exchange Online, Content Search in the Office 365 Security &amp; Compliance Center, or the eDiscovery Center in SharePoint Online.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e70d4-p105">В Exchange Online обратимо удаленный почтовый ящик  почтовый ящик, который был удален, но может быть восстановлен в течение определенного срока хранения (в Exchange Online он составляет 30 дней). Это значит, что такой почтовый ящик можно восстановить или сделать неактивным в течение 30 дней после удаления. По истечении этого периода обратимо удаленный почтовый ящик помечается для окончательного удаления, и в этом случае его уже невозможно восстановить или сделать неактивным.</span><span class="sxs-lookup"><span data-stu-id="e70d4-p105">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered (or made an inactive mailbox) within 30 days of being deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered or made inactive.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="e70d4-123">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="e70d4-123">Before you begin</span></span>
<span data-ttu-id="e70d4-124"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="e70d4-124"></span></span>

- <span data-ttu-id="e70d4-p106">Примените командлет **New-MailboxSearch** в Оболочка Windows PowerShell, чтобы назначить удержание на месте для обратимо удаленного почтового ящика. В SharePoint Online вы не можете использовать Центр администрирования Exchange (EAC) или центр обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="e70d4-p106">You have to use the **New-MailboxSearch** cmdlet in Windows PowerShell to put an In-Place Hold on a soft-deleted mailbox. You can't use the Exchange admin center (EAC) or the eDiscovery Center in SharePoint Online.</span></span> 
    
- <span data-ttu-id="e70d4-127">Сведения о том, как с помощью Оболочка Windows PowerShell подключаться к Exchange Online, см. в статье [Подключение к PowerShell для Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="e70d4-127">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="e70d4-128">Выполните указанную ниже команду, чтобы отобразить удостоверения обратимо удаленных почтовых ящиков в организации.</span><span class="sxs-lookup"><span data-stu-id="e70d4-128">Run the following command to get identity information about the soft-deleted mailboxes in your organization.</span></span> 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- <span data-ttu-id="e70d4-129">Дополнительные сведения о неактивных почтовых ящиках см. в статье [Неактивные почтовые ящики в Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).</span><span class="sxs-lookup"><span data-stu-id="e70d4-129">For more information about inactive mailboxes, see [Inactive mailboxes in Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).</span></span>
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a><span data-ttu-id="e70d4-130">Назначение удержания на месте для обратимо удаленного почтового ящика, чтобы сделать последний неактивным</span><span class="sxs-lookup"><span data-stu-id="e70d4-130">Put an In-Place Hold on a soft-deleted mailbox to make it an inactive mailbox</span></span>
<span data-ttu-id="e70d4-131"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="e70d4-131"></span></span>

<span data-ttu-id="e70d4-p107">С помощью командлета **New-MailboxSearch** сделайте обратимо удаленный почтовый ящик неактивным. Дополнительные сведения см. в статье [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span><span class="sxs-lookup"><span data-stu-id="e70d4-p107">Use the **New-MailboxSearch** cmdlet to make a soft-deleted mailbox an inactive mailbox. For more information, see [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span></span>
  
1. <span data-ttu-id="e70d4-134">Создайте переменную, содержащую свойства обратимо удаленного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="e70d4-134">Create a variable that contains the properties of the soft-deleted mailbox.</span></span> 
    
  ```
  $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
  ```

    > [!IMPORTANT]
    > <span data-ttu-id="e70d4-p108">В указанной выше команде используйте значение свойства **DistinguishedName** или **ExchangeGuid** для определения обратимо удаленного почтового ящика. Эти свойства уникальны для каждого почтового ящика в организации, тогда как у активного и обратимо удаленного почтовых ящиков может быть один и тот же основной SMTP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e70d4-p108">In the previous command, use the value of the **DistinguishedName** or **ExchangeGuid** property to identify the soft-deleted mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active mailbox and a soft-deleted mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="e70d4-p109">Создайте запрос удержания на месте и назначьте его для обратимо удаленного почтового ящика. В этом примере не указан период удержания. Это означает, что элементы будут храниться в течение неограниченного срока или до тех пор, пока для неактивного почтового ящика не будет отменено удержание.</span><span class="sxs-lookup"><span data-stu-id="e70d4-p109">Create an In-Place Hold and place it on the soft-deleted mailbox. In this example, no hold duration is specified. This means items will be held indefinitely or until the hold is removed from the inactive mailbox.</span></span>
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
  
  ```

    <span data-ttu-id="e70d4-p110">Кроме того, вы можете указать длительность удержания при создании запроса удержания на месте. В этом примере элементы в неактивном почтовом ящике удерживаются около 7 лет.</span><span class="sxs-lookup"><span data-stu-id="e70d4-p110">You can also specify a hold duration when you create the In-Place Hold. This example holds items in the inactive mailbox for approximately 7 years.</span></span>
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
  ```

3. <span data-ttu-id="e70d4-142">Через пару минут запустите одну из указанных ниже команд, чтобы убедиться в неактивности этого обратимо удаленного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="e70d4-142">After a few moments, run one of the following commands to verify that the soft-deleted mailbox is an inactive mailbox.</span></span>
    
  ```
  Get-Mailbox -InactiveMailboxOnly
  ```

    <span data-ttu-id="e70d4-143">Еще вариант:</span><span class="sxs-lookup"><span data-stu-id="e70d4-143">Or</span></span>
    
  ```
  Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
  ```

## <a name="more-information"></a><span data-ttu-id="e70d4-144">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="e70d4-144">More information</span></span>
<span data-ttu-id="e70d4-145"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="e70d4-145"></span></span>

<span data-ttu-id="e70d4-p111">Сделав обратимо удаленный почтовый ящик неактивным, вы сможете управлять им несколькими способами. Дополнительные сведения см. в таких статьях:</span><span class="sxs-lookup"><span data-stu-id="e70d4-p111">After you make a soft-deleted mailbox an inactive mailbox, there are a number of ways you can manage the mailbox. For more information, see:</span></span>
  
- <span data-ttu-id="e70d4-148">[Изменение срока хранения неактивного почтового ящика в Exchange Online](http://technet.microsoft.com/library/96eb634e-af2f-454e-8014-b698396811c4.aspx) ;</span><span class="sxs-lookup"><span data-stu-id="e70d4-148">[Change the hold duration for an inactive mailbox in Exchange Online](http://technet.microsoft.com/library/96eb634e-af2f-454e-8014-b698396811c4.aspx)</span></span>
    
- <span data-ttu-id="e70d4-149">[Восстановление неактивного почтового ящика в Exchange Online](http://technet.microsoft.com/library/283838b4-66ba-4c34-b221-e1a3875e1d29.aspx) ;</span><span class="sxs-lookup"><span data-stu-id="e70d4-149">[Recover an inactive mailbox in Exchange Online](http://technet.microsoft.com/library/283838b4-66ba-4c34-b221-e1a3875e1d29.aspx)</span></span>
    
- <span data-ttu-id="e70d4-150">[Возврат неактивного почтового ящика в Exchange Online](http://technet.microsoft.com/library/1fb02feb-49e5-4485-aec5-9f1537b772b6.aspx) ;</span><span class="sxs-lookup"><span data-stu-id="e70d4-150">[Restore an inactive mailbox in Exchange Online](http://technet.microsoft.com/library/1fb02feb-49e5-4485-aec5-9f1537b772b6.aspx)</span></span>
    
- <span data-ttu-id="e70d4-151">[Отключение удержания неактивного почтового ящика в Exchange Online](http://technet.microsoft.com/library/930a98c3-cd81-4aaa-8e22-19714cb2b731.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e70d4-151">[Remove a hold from an inactive mailbox in Exchange Online](http://technet.microsoft.com/library/930a98c3-cd81-4aaa-8e22-19714cb2b731.aspx)</span></span>
    

