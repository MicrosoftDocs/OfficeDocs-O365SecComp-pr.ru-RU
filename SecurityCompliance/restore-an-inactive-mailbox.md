---
title: Восстановление неактивного почтового ящика в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/28/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 97e06a7a-ef9a-4ce8-baea-18b9e20449a3
description: Если новый сотрудник или другому пользователю требуется доступ к содержимому неактивного почтового ящика в Office 365, можно восстанавливать (или объединения) содержимое неактивного почтового ящика для существующего почтового ящика.
ms.openlocfilehash: e0add2b63a48edc27795143324c83153b15dcf8c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534322"
---
# <a name="restore-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="08e61-103">Восстановление неактивного почтового ящика в Office 365</span><span class="sxs-lookup"><span data-stu-id="08e61-103">Restore an inactive mailbox in Office 365</span></span>

<span data-ttu-id="08e61-p101">Неактивного почтового ящика (который — это тип удаленный почтовый ящик) используется для сохранения бывший сотрудник электронной почты после он или она уволится из вашей организации. Если другой сотрудник принимает должностные обязанности сотрудника, departed или он возвращает для вашей организации, существует два способа, что вы можете предоставить содержимое неактивного почтового ящика пользователя:</span><span class="sxs-lookup"><span data-stu-id="08e61-p101">An inactive mailbox (which is a type of soft-deleted mailbox) is used to retain a former employee's email after he or she leaves your organization. If another employee takes on the job responsibilities of the departed employee or if that employee returns to your organization, there are two ways that you can make the contents of the inactive mailbox available to a user:</span></span> 
  
- <span data-ttu-id="08e61-p102">**Восстановление неактивного почтового ящика**. Если другой сотрудник берет на себя обязанности уволенного сотрудника или другому пользователю требуется доступ к содержимому неактивного почтового ящика, вы можете восстановить содержимое неактивного почтового в существующем почтовом ящике (этот процесс также называют слиянием). Можно также восстановить архив из неактивного почтового ящика. После восстановления неактивный почтовый ящик хранится как неактивный. В этом разделе описаны процедуры восстановления неактивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-p102">**Restore an inactive mailbox** If another employee takes on the job responsibilities of the departed employee, or if another user needs access to the contents of the inactive mailbox, you can restore (or merge) the contents of the inactive mailbox to an existing mailbox. You can also restore the archive from an inactive mailbox. After it's restored, the inactive mailbox is preserved and is retained as an inactive mailbox. This topic describes the procedures for restoring an inactive mailbox.</span></span> 
    
- <span data-ttu-id="08e61-p103">**Восстановление неактивного почтового ящика** Если возвращает departed сотрудников вашей организации или работу новых сотрудников будет выполняться для должностные обязанности departed сотрудника, вы можете восстанавливать контент неактивного почтового ящика. Этот метод преобразует неактивного почтового ящика в новый почтовый ящик, который содержит содержимое неактивного почтового ящика. После восстановления, неактивного почтового ящика больше не существует. Пошаговые процедуры в разделе [Восстановление неактивного почтового ящика в Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="08e61-p103">**Recover an inactive mailbox** If the departed employee returns to your organization, or if a new employee is hired to take on the job responsibilities of the departed employee, you can recover the contents of the inactive mailbox. This method converts the inactive mailbox to a new mailbox that contains the contents of the inactive mailbox. After it's recovered, the inactive mailbox no longer exists. For the step-by-step procedures, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
<span data-ttu-id="08e61-114">В разделе **Дополнительные сведения** в этой статье для получения дополнительных сведений о различиях между восстановление и восстановление неактивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-114">See the **More information** section in this article for more details about the differences between restoring and recovering an inactive mailbox.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="08e61-115">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="08e61-115">Before you begin</span></span>

- <span data-ttu-id="08e61-p104">Необходимо использовать Exchange Online PowerShell для восстановления неактивного почтового ящика. Нельзя использовать Центр администрирования Exchange (EAC). Пошаговые инструкции в разделе [подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="08e61-p104">You have to use Exchange Online PowerShell to restore an inactive mailbox. You can't use the Exchange admin center (EAC). For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span></span>
    
- <span data-ttu-id="08e61-119">Выполните следующую команду в Exchange Online PowerShell, чтобы получить сведения об идентификации для неактивных почтовых ящиков в организации.</span><span class="sxs-lookup"><span data-stu-id="08e61-119">Run the following command in Exchange Online PowerShell to get identity information for the inactive mailboxes in your organization.</span></span> 
    
    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

     <span data-ttu-id="08e61-120">Используйте полученную информацию для восстановления определенного неактивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-120">Use the information returned by this command to restore a specific inactive mailbox.</span></span>
    
- <span data-ttu-id="08e61-121">Дополнительные сведения о неактивные почтовые ящики можно [неактивные почтовые ящики в Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="08e61-121">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="restore-an-inactive-mailbox"></a><span data-ttu-id="08e61-122">Восстановление неактивного почтового ящика</span><span class="sxs-lookup"><span data-stu-id="08e61-122">Restore an inactive mailbox</span></span>

<span data-ttu-id="08e61-p105">Используйте командлет **New-MailboxRestoreRequest** с параметрами  _SourceMailbox_ и  _TargetMailbox_, чтобы восстановить содержимое неактивного почтового ящика в существующем ящике. Дополнительные сведения об использовании данного командлета см. в статье [New-MailboxRestoreRequest](https://go.microsoft.com/fwlink/?linkid=856298).</span><span class="sxs-lookup"><span data-stu-id="08e61-p105">Use the **New-MailboxRestoreRequest** cmdlet with the  _SourceMailbox_ and  _TargetMailbox_ parameters to restore the contents of an inactive mailbox to an existing mailbox. For more information about using this cmdlet, see [New-MailboxRestoreRequest](https://go.microsoft.com/fwlink/?linkid=856298).</span></span>
  
1. <span data-ttu-id="08e61-125">Создайте переменную, содержащую свойства неактивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-125">Create a variable that contains the properties of the inactive mailbox.</span></span> 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="08e61-p106">В предыдущей команде используйте значение свойства **DistinguishedName** или **ExchangeGUID** для определения неактивного почтового ящика. Эти свойства уникальны для каждого почтового ящика в организации, тогда как у активного и неактивного почтового ящика может быть один и тот же основной SMTP-адрес.</span><span class="sxs-lookup"><span data-stu-id="08e61-p106">In the previous command, use the value of the **DistinguishedName** or **ExchangeGUID** property to identify the inactive mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active and an inactive mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="08e61-p107">Восстановление содержимого неактивного почтового ящика в существующем ящике. Содержимое неактивного (исходного) почтового ящика будет добавлено в соответствующие папки существующего (целевого) почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-p107">Restore the contents of the inactive mailbox to an existing mailbox. The contents of the inactive mailbox (source mailbox) will be merged into the corresponding folders in the existing mailbox (target mailbox).</span></span>
    
    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -AllowLegacyDNMismatch
    ```
   
   <span data-ttu-id="08e61-p108">Кроме того, можно указать папку верхнего уровня в целевом почтовом ящике, в которую будет восстановлено содержимое неактивного почтового ящика. Если указанная целевая папка или структура папок еще не существует в целевом почтовом ящике, она будет создана во время процесса восстановления.</span><span class="sxs-lookup"><span data-stu-id="08e61-p108">Alternatively, you can specify a top-level folder in the target mailbox in which to restore the contents from the inactive mailbox. If the specified target folder or target folder structure doesn't already exist in the target mailbox, it is created during the restore process.</span></span> 
    
    <span data-ttu-id="08e61-132">Этот пример копирует элементы и вложенные папки из неактивного почтового ящика в папку "Inactive Mailbox" в структуре папок верхнего уровня в целевом почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="08e61-132">This example copies mailbox items and subfolders from an inactive mailbox to a folder named "Inactive Mailbox" in the top-level folder structure of the target mailbox.</span></span>
    
   ```
   New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
   ```
  
## <a name="restore-the-archive-from-an-inactive-mailbox"></a><span data-ttu-id="08e61-133">Восстановление архива из неактивного почтового ящика</span><span class="sxs-lookup"><span data-stu-id="08e61-133">Restore the archive from an inactive mailbox</span></span>

<span data-ttu-id="08e61-p109">Если неактивный почтовый ящик содержит архивный почтовый ящик, можно восстановить его в архивный почтовый ящик существующего ящика. Для этого необходимо добавить параметры  _SourceIsArchive_ и  _TargetIsAchive_ в команду, используемую для восстановления неактивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-p109">If an inactive mailbox has an archive mailbox, you can also restore it to the archive mailbox of an existing mailbox. To restore the archive from an inactive mailbox, you have to add the  _SourceIsArchive_ and  _TargetIsAchive_ switches to the command used to restore an inactive mailbox.</span></span> 
  
1. <span data-ttu-id="08e61-136">Создайте переменную, содержащую свойства неактивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-136">Create a variable that contains the properties of the inactive mailbox.</span></span> 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="08e61-p110">В предыдущей команде используйте значение свойства **DistinguishedName** или **ExchangeGUID** для определения неактивного почтового ящика. Эти свойства уникальны для каждого почтового ящика в организации, тогда как у активного и неактивного почтового ящика может быть один и тот же основной SMTP-адрес.</span><span class="sxs-lookup"><span data-stu-id="08e61-p110">In the previous command, use the value of the **DistinguishedName** or **ExchangeGUID** property to identify the inactive mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active and an inactive mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="08e61-p111">Восстановление содержимого архива из неактивного почтового ящика (исходного архива) в архив существующего почтового ящика (целевой архив). В этом примере содержимое из исходного архива копируется в папку с именем "Inactive Mailbox Archive" в архиве целевого почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-p111">Restore the contents of the archive from the inactive mailbox (source archive) to the archive of an existing mailbox (target archive). In this example, the contents from the source archive are copied to a folder named "Inactive Mailbox Archive" in the archive of the target mailbox.</span></span>

    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -SourceIsArchive -TargetMailbox newemployee@contoso.com -TargetIsArchive -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
    ```

  
## <a name="more-information"></a><span data-ttu-id="08e61-141">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="08e61-141">More information</span></span>

- <span data-ttu-id="08e61-p112">**Возможности основное различие между восстановлении и восстановлении неактивного почтового ящика?** При восстановлении неактивного почтового ящика, по сути почтовый ящик преобразуется в новый почтовый ящик, контент и структура папки неактивного почтового ящика, сохраняются и связанный почтовый ящик учетной записи пользователя. После того как будет восстановлена, неактивного почтового ящика больше не существует и всех изменений, внесенных в содержимое в новый почтовый ящик повлияет на контент, который изначально на хранение в неактивного почтового ящика. С другой стороны при восстановлении неактивного почтового ящика содержимое просто копируются другого почтового ящика. Неактивного почтового ящика сохраняется и остается неактивного почтового ящика. Любые изменения, внесенные контента в целевой почтовый ящик не влияет на исходное содержимое, которые проводятся в неактивного почтового ящика. Неактивного почтового ящика по-прежнему может быть выполнен с помощью [средства поиска контента](run-a-content-search-in-the-security-and-compliance-center.md) в Office 365 безопасность &amp; центре соответствия требованиям, другого почтового ящика можно было восстановить его содержимое или его можно восстанавливать или удалении позже.</span><span class="sxs-lookup"><span data-stu-id="08e61-p112">**What's the main difference between recovering and restoring an inactive mailbox?** When you recover an inactive mailbox, the mailbox is basically converted to a new mailbox, the contents and folder structure of the inactive mailbox are retained, and the mailbox is linked to a new user account. After it's recovered, the inactive mailbox no longer exists, and any changes made to the content in the new mailbox will affect the content that was originally on hold in the inactive mailbox. Conversely, when you restore an inactive mailbox, the contents are merely copied to another mailbox. The inactive mailbox is preserved and remains an inactive mailbox. Any changes made to the content in the target mailbox won't affect the original content held in the inactive mailbox. The inactive mailbox can still be searched by using the [Content Search tool](run-a-content-search-in-the-security-and-compliance-center.md) in the Office 365 Security &amp; Compliance Center, its contents can be restored to another mailbox, or it can be recovered or deleted at a later date.</span></span> 
    
- <span data-ttu-id="08e61-p113">**Как найти неактивные почтовые ящики?** Для получения списка неактивных почтовых ящиков в организации и информации, необходимой для восстановления неактивного почтового ящика, выполните эту команду.</span><span class="sxs-lookup"><span data-stu-id="08e61-p113">**How do you find inactive mailboxes?** To get a list of the inactive mailboxes in your organization and display information that is useful for restoring an inactive mailbox, you can run this command.</span></span> 

  ```
  Get-Mailbox -InactiveMailboxOnly | FL Name,PrimarySMTPAddress,DistinguishedName,ExchangeGUID,LegacyExchangeDN,ArchiveStatus
  ```

- <span data-ttu-id="08e61-p114">**Сохранение контента неактивного почтового ящика с помощью политики хранения хранение для судебного разбирательства или Office 365.** Если вы хотите сохранить состояние неактивного почтового ящика после его восстановления, можно поместить целевой почтовый ящик на [Хранение для судебного разбирательства](https://go.microsoft.com/fwlink/?linkid=856286) или применить [политику хранения Office 365](retention-policies.md) , прежде чем восстанавливать неактивного почтового ящика. Это предотвратит окончательного удаления любых элементов из неактивного почтового ящика после их в случае восстановить целевой почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="08e61-p114">**Use a Litigation Hold or Office 365 retention policy to retain inactive mailbox content.** If you want to retain the state of an inactive mailbox after it's restored, you can place the target mailbox on [Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286) or apply an [Office 365 retention policy](retention-policies.md) before you restore the inactive mailbox. This will prevent the permanent deletion of any items from the inactive mailbox after they're restored to the target mailbox.</span></span> 
    
- <span data-ttu-id="08e61-p115">**Включить удержание на целевой почтовый ящик перед восстановлением неактивного почтового ящика.** Так как может быть старые элементы почтового ящика из неактивного почтового ящика, может потребоваться включение удержания хранения на целевой почтовый ящик, прежде чем восстанавливать неактивного почтового ящика. При переводе удержание почтовых ящиков на хранение политика хранения, назначенные ему не будет обработан, пока не будет снято удержание хранения или пока удержание истечения срока. Это дает владельца почтового ящика целевое время на управление старыми сообщениями с неактивного почтового ящика. В противном случае политика хранения может удалять старые элементы (или перемещаются в архивный почтовый ящик, если он включен), срок действия на основе параметров хранения, настроенные для целевого почтового ящика. Дополнительные сведения см в [почтовый ящик на хранение хранение в Exchange Online](https://go.microsoft.com/fwlink/?linkid=856300).</span><span class="sxs-lookup"><span data-stu-id="08e61-p115">**Enable retention hold on the target mailbox before you restore an inactive mailbox.** Because mailbox items from an inactive mailbox could be old, you might consider enabling retention hold on the target mailbox before you restore an inactive mailbox. When you put a mailbox on retention hold, the retention policy that's assigned to it won't be processed until the retention hold is removed or until the retention hold period expires. This gives the owner of the target mailbox time to manage old messages from the inactive mailbox. Otherwise, the retention policy might delete old items (or move items to the archive mailbox, if it's enabled) that have expired based on the retention settings configured for the target mailbox. For more information, see [Place a mailbox on retention hold in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856300).</span></span>
    
- <span data-ttu-id="08e61-p116">**Что делает параметр AllowLegacyDNMismatch?** В предыдущих примерах для восстановления неактивного почтового ящика параметр **AllowLegacyDNMismatch** используется для разрешения восстановление неактивного почтового ящика в разных целевой почтовый ящик. В сценарий восстановления цель — Восстановление содержимого исходного и конечного почтовые ящики которых этого почтового ящика. Поэтому по умолчанию командлет **New-MailboxRestoreRequest** проверяет, убедитесь в том, что значение свойства **LegacyExchangeDN** на исходный и целевой почтовых ящиков, то же. Это помогает запрещает случайно восстановление исходного почтового ящика в неправильную целевой почтовый ящик. При попытке восстановления неактивного почтового ящика без использования переключатель **AllowLegacyDNMismatch** команда может оказаться неудачным, если исходный и целевой почтовых ящиков имеют различные значения для свойства **LegacyExchangeDN** .</span><span class="sxs-lookup"><span data-stu-id="08e61-p116">**What does the AllowLegacyDNMismatch switch do?** In the previous examples to restore an inactive mailbox, the **AllowLegacyDNMismatch** switch is used to allow restoring the inactive mailbox to a different target mailbox. In a typical restore scenario, the goal is to restore content where the source and target mailboxes are the same mailbox. So by default, the **New-MailboxRestoreRequest** cmdlet checks to make sure that the value of the **LegacyExchangeDN** property on the source and target mailboxes is the same. This helps prevents you from accidentally restoring a source mailbox into the wrong target mailbox. If you try to restore an inactive mailbox without using the **AllowLegacyDNMismatch** switch, the command might fail if the source and target mailboxes have different values for the **LegacyExchangeDN** property.</span></span> 
    
- <span data-ttu-id="08e61-p117">**Можно использовать другие параметры с командлетом New-MailboxRestoreRequest для реализации различных сценариев восстановления неактивных почтовых ящиков.** Например, можно выполнить эту команду, чтобы восстановить архив из неактивного почтового ящика в основном почтовом ящике целевого почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="08e61-p117">**You can use other parameters with the New-MailboxRestoreRequest cmdlet to implement different restore scenarios for inactive mailboxes.** For example, you can run this command to restore the archive from the inactive mailbox into the primary mailbox of the target mailbox.</span></span> 
    
  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -SourceIsArchive -TargetMailbox <target mailbox> -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
  ```

  <span data-ttu-id="08e61-168">Можно также восстановить неактивный основной почтовый ящик в архиве в целевом почтовом ящике, выполнив эту команду.</span><span class="sxs-lookup"><span data-stu-id="08e61-168">You can also restore the inactive primary mailbox into the archive of the target mailbox by running this command.</span></span>

  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -TargetMailbox <target mailbox> -TargetIsArchive -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
  ```

- <span data-ttu-id="08e61-p118">**Что делает параметр TargetRootFolder?** Как объяснялось ранее, параметр **TargetRootFolder** можно использовать, чтобы указать папку в верхней части структуры папок ( корневой папке) целевого почтового ящика, в котором требуется восстановить содержимое неактивного почтового ящика. Если этот параметр не используется, элементы неактивного почтового ящика добавляются в соответствующие папки целевого почтового ящика по умолчанию, а пользовательские папки создаются заново в корневой папке целевого ящика. На следующих рисунках показаны различия между использованием и неиспользованием параметра **TargetRootFolder**.</span><span class="sxs-lookup"><span data-stu-id="08e61-p118">**What does the TargetRootFolder parameter do?** As previously explained, you can use the **TargetRootFolder** parameter to specify a folder in the top of the folder structure (also called the root) in the target mailbox in which to restore the contents of the inactive mailbox. If you don't use this parameter, mailbox items from the inactive mailbox are merged into the corresponding default folders of the target mailbox, and custom folders are re-created in the root of the target mailbox. The following illustrations highlight these differences between not using and using the **TargetRootFolder** parameter.</span></span> 
    
    <span data-ttu-id="08e61-173">**Иерархия папок в целевом почтовом ящике, если параметр TargetRootFolder не используется**</span><span class="sxs-lookup"><span data-stu-id="08e61-173">**Folder hierarchy in the target mailbox when the TargetRootFolder parameter isn't used**</span></span>
    
    ![Снимок экрана: не используется параметр TargetRootFolder.](media/76a759af-f483-4d1c-8cc7-243435b5562e.png)
  
    <span data-ttu-id="08e61-175">**Иерархия папок в целевом почтовом ящике, если параметр TargetRootFolder используется**</span><span class="sxs-lookup"><span data-stu-id="08e61-175">**Folder hierarchy in the target mailbox when the TargetRootFolder parameter is used**</span></span>
    
    ![Снимок экрана: используется параметр TargetRootFolder.](media/300da592-7323-48db-b8a4-07012259d113.png)

  

