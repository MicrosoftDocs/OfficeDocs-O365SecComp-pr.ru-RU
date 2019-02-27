---
title: Удаление элементов из папки "элементы с возможностью восстановления" в облачных почтовых ящиках в справке для удержания
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Для администраторов: удаление элементов из папки "элементы с возможностью восстановления" для почтового ящика Exchange Online, даже если этот почтовый ящик размещен на удержании по юридическим причинам. Это эффективный способ удаления данных, которые были случайно перенесены в Office 365.'
ms.openlocfilehash: 4b7b12b33a2364d76b5d7dab6c7e94dc8f00d151
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296182"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a><span data-ttu-id="830db-104">Удаление элементов из папки "элементы с возможностью восстановления" в облачных почтовых ящиках в справке для удержания</span><span class="sxs-lookup"><span data-stu-id="830db-104">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold - Admin Help</span></span>

<span data-ttu-id="830db-p102">Папка "элементы с возможностью восстановления" для почтового ящика Exchange Online существует для защиты от случайных или вредоносных удалений. Он также используется для хранения элементов, которые поддерживаются и доступны в Office 365, например для поиска удержаний и обнаружения электронных данных. Однако в некоторых ситуациях некоторые организации могут иметь непреднамеренно сохраненные данные в папке "элементы с возможностью восстановления", которые необходимо удалить. Например, пользователь может непреднамеренно отправить или переслать сообщение электронной почты, содержащее конфиденциальную информацию или информацию, которая может иметь серьезные последствия для бизнеса. Даже если сообщение окончательно удаляется, оно может храниться в течение неограниченного времени, так как для почтового ящика было включено юридическое удержание. Этот сценарий называется выпустка данных, так как данные были случайно перенесены в Office 365. В этом случае можно удалить элементы из папки "элементы с возможностью восстановления" для почтового ящика Exchange Online, даже если этот почтовый ящик включен в удержание с одной из различных функций хранения в Office 365. Эти типы удержаний включают судебные удержания, удержания на месте, удержания электронных данных и политики хранения Office 365, созданные в центре безопасности &amp; и соответствия требованиям Office 365.</span><span class="sxs-lookup"><span data-stu-id="830db-p102">The Recoverable Items folder for an Exchange Online mailbox exists to protect from accidental or malicious deletions. It's also used to store items that are retained and accessed by Office 365 compliance features, such as holds and eDiscovery searches. However, in some situations organizations might have data that's been unintentionally retained in the Recoverable Items folder that they must delete. For example, a user might unknowingly send or forward an email message that contains sensitive information or information that may have serious business consequences. Even if the message is permanently deleted, it might be retained indefinitely because a legal hold has been placed on the mailbox. This scenario is known as data spillage because data has been unintentionally spilled into Office 365. In these situations, you can delete items in a user's Recoverable Items folder for an Exchange Online mailbox, even if that mailbox is placed on hold with one of the different hold features in Office 365. These types of holds include Litigation Holds, In-Place Holds, eDiscovery holds, and Office 365 retention policies created in the Office 365 Security &amp; Compliance Center.</span></span> 
  
 <span data-ttu-id="830db-p103">В этой статье объясняется, как удалять элементы из папки "элементы с возможностью восстановления" для почтовых ящиков в облаке, находящихся на удержании. Эта процедура включает в себя отключение доступа к почтовому ящику и отключение восстановления отдельных элементов, отключение помощника по работе с управляемыми папками от обработки почтового ящика, временное удаление удержания, удаление элементов из папки "элементы с возможностью восстановления", а затем возврат почтового ящика в предыдущую конфигурацию. Вот процесс:</span><span class="sxs-lookup"><span data-stu-id="830db-p103">This article explains how to delete items from the Recoverable Items folder for cloud-based mailboxes that are on hold. This procedure involves disabling access to the mailbox and disabling single item recovery, disabling the Managed Folder Assistant from processing the mailbox, temporarily removing the hold, deleting items from the Recoverable Items folder, and then reverting the mailbox to its previous configuration. Here's the process:</span></span> 
  
[<span data-ttu-id="830db-116">Шаг 1: сбор сведений о почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="830db-116">Step 1: Collect information about the mailbox</span></span>](#step-1-collect-information-about-the-mailbox)

[<span data-ttu-id="830db-117">Шаг 2: подготовка почтового ящика</span><span class="sxs-lookup"><span data-stu-id="830db-117">Step 2: Prepare the mailbox</span></span>](#step-2-prepare-the-mailbox)

[<span data-ttu-id="830db-118">Шаг 3: удаление всех удержаний из почтового ящика</span><span class="sxs-lookup"><span data-stu-id="830db-118">Step 3: Remove all holds from the mailbox</span></span>](#step-3-remove-all-holds-from-the-mailbox)

[<span data-ttu-id="830db-119">Шаг 4: удаление задержки хранения из почтового ящика</span><span class="sxs-lookup"><span data-stu-id="830db-119">Step 4: Remove the delay hold from the mailbox</span></span>](#step-4-remove-the-delay-hold-from-the-mailbox)

[<span data-ttu-id="830db-120">Шаг 5: удаление элементов из папки "элементы с возможностью восстановления"</span><span class="sxs-lookup"><span data-stu-id="830db-120">Step 5: Delete items in the Recoverable Items folder</span></span>](#step-5-delete-items-in-the-recoverable-items-folder)

[<span data-ttu-id="830db-121">Шаг 6: возврат к предыдущему состоянию почтового ящика</span><span class="sxs-lookup"><span data-stu-id="830db-121">Step 6: Revert the mailbox to its previous state</span></span>](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> <span data-ttu-id="830db-p104">Процедуры, описанные в этой статье, будут приводить к окончательному удалению данных из почтового ящика Exchange Online. Это означает, что сообщения, которые вы удаляете из папки "элементы с возможностью восстановления", невозможно восстановить, и они не будут доступны для судебного обнаружения или других целей обеспечения соответствия требованиям. Если вы хотите удалить сообщения из почтового ящика, помещенного на хранение в рамках хранения для судебного разбирательства, хранения на месте, удержания электронных данных или политики хранения Office 365, созданной в &amp; центре безопасности Office 365, обратитесь к управлению записями или юридическим требованиям. отделы перед удалением удержания. У вашей организации может быть политика, определяющая, имеет ли почтовые ящики на удержании или при проведении на них приоритет.</span><span class="sxs-lookup"><span data-stu-id="830db-p104">The procedures outlined in this article will result in data being permanently deleted (purged) from an Exchange Online mailbox. That means messages that you delete from the Recoverable Items folder can't be recovered and won't be available for legal discovery or other compliance purposes. If you want to delete messages from a mailbox that's placed on hold as part of a Litigation Hold, In-Place Hold, eDiscovery hold, or Office 365 retention policy created in the Office 365 Security &amp; Compliance Center, check with your records management or legal departments before removing the hold. Your organization might have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="830db-126">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="830db-126">Before you begin</span></span>

- <span data-ttu-id="830db-127">Для поиска и удаления сообщений из папки "элементы с возможностью восстановления" в действии 5 необходимо назначить обе указанные ниже роли управления в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="830db-127">You have to be assigned both of the following management roles in Exchange Online to search for and delete messages from the Recoverable Items folder in Step 5.</span></span>
    
  - <span data-ttu-id="830db-p105">**Поиск** в почтовом ящике — эта роль позволяет выполнять поиск в почтовых ящиках в Организации. Администраторы Exchange не назначают эту роль по умолчанию. Чтобы назначить себе эту роль, добавьте себя в качестве члена группы ролей Управление обнаружением в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="830db-p105">**Mailbox Search** - This role lets you to search mailboxes in your organization. Exchange administrators aren't assigned this role by default. To assign yourself this role, add yourself as a member of the Discovery Management role group in Exchange Online.</span></span> 
    
  - <span data-ttu-id="830db-p106">**Экспорт импорта** поЧтовых ящиков — Эта роль позволяет удалять сообщения из почтового ящика пользователя. По умолчанию эта роль не назначена ни одной группе ролей. Чтобы удалить сообщения из почтовых ящиков пользователей, можно добавить роль импорта поЧтовых ящиков в группу ролей Управление организацией в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="830db-p106">**Mailbox Import Export** - This role lets you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> 
    
- <span data-ttu-id="830db-p107">Процедуры, описанные в этой статье, не поддерживаются для неактивных почтовых ящиков. Это связано с тем, что после удаления неактивного почтового ящика невозможно повторно применить удержание (или политику хранения Office 365) к неактивному почтовому ящику. При удалении удержания из неактивного почтового ящика он заменяется обычным обратимо удаленным почтовым ящиком и будет окончательно удален из Организации после его обработки помощником для управляемых папок.</span><span class="sxs-lookup"><span data-stu-id="830db-p107">The procedure described in this article isn't supported for inactive mailboxes. That's because you can't re-apply a hold (or Office 365 retention policy) to an inactive mailbox after you remove it. When you remove a hold from an inactive mailbox, it's changed to a normal soft-deleted mailbox and will be permanently deleted from your organization after it's processed by the Managed Folder Assistant.</span></span>
    
- <span data-ttu-id="830db-p108">Эту процедуру невозможно выполнить для почтового ящика, назначенного политике хранения Office 365, заблокированной с блокировкой сохранения. Это связано с тем, что блокировка сохранения предотвращает удаление или исключение почтового ящика из политики хранения Office 365 и отключение помощника для управляемых папок в почтовом ящике. Дополнительные сведения о блокировке политик хранения приведены в разделе [Блокировка политики хранения](retention-policies.md#locking-a-retention-policy).</span><span class="sxs-lookup"><span data-stu-id="830db-p108">You can't perform this procedure for a mailbox that has been assigned to an Office 365 retention policy that's been locked with a Preservation Lock. That's because a Preservation Lock prevents you from removing or excluding the mailbox from the Office 365 retention policy and from disabling the Managed Folder Assistant on the mailbox. For more information about locking retention policies, see [Locking a retention policy](retention-policies.md#locking-a-retention-policy).</span></span>
    
- <span data-ttu-id="830db-p109">Если почтовый ящик не полагается на удержание (или не включено восстановление отдельных элементов), можно просто удалить элементы из папки "элементы с возможностью восстановления". Дополнительные сведения о том, как это сделать, можно найти в статье [Поиск и удаление сообщений ](https://go.microsoft.com/fwlink/?linkid=852453).</span><span class="sxs-lookup"><span data-stu-id="830db-p109">If a mailbox isn't placed on hold (or doesn't have single item recovery enabled), you can simply delete the items from the Recoverable Items folder. For more information about how to do this, see [Search for and delete messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span></span>
  
## <a name="step-1-collect-information-about-the-mailbox"></a><span data-ttu-id="830db-142">Шаг 1: сбор сведений о почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="830db-142">Step 1: Collect information about the mailbox</span></span>

<span data-ttu-id="830db-p110">Сначала необходимо собрать выбранные свойства из целевого почтового ящика, которые будут влиять на эту процедуру. Обязательно запишите эти параметры или сохраните их в текстовом файле, так как вы измените некоторые из этих свойств, а затем вернитесь к исходным значениям на шаге 6, после того как вы удалите элементы из папки "элементы с возможностью восстановления". Ниже приведен список свойств почтовых ящиков, которые необходимо собрать.</span><span class="sxs-lookup"><span data-stu-id="830db-p110">This first step is to collect selected properties from the target mailbox that will affect this procedure. Be sure to write down these settings or save them to a text file because you'll change some of these properties and then revert back to the original values in Step 6, after you delete items from the Recoverable Items folder. Here's a list of the mailbox properties you need to collect.</span></span>
  
-  <span data-ttu-id="830db-146">*Синглеитемрековеренаблед* и *RetainDeletedItemsFor* ; При необходимости вы отключите одно восстановление и увеличьте срок хранения удаленных элементов на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="830db-146">*SingleItemRecoveryEnabled*  and  *RetainDeletedItemsFor*  ; if necessary, you'll disable single recovery and increase the deleted items retention period in Step 3.</span></span> 
    
-  <span data-ttu-id="830db-p111">*LitigationHoldEnabled* и *InPlaceHolds* ; необходимо определить все удержания, размещенные в почтовом ящике, чтобы их можно было временно удалить на шаге 3. В разделе [Дополнительные сведения](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) приведены советы по определению типа удержания, который может быть включен в почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="830db-p111">*LitigationHoldEnabled*  and  *InPlaceHolds*  ; you need to identify all the holds placed on the mailbox so that you can temporarily remove them in Step 3. See the [More information](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
    
<span data-ttu-id="830db-p112">Кроме того, необходимо получить параметры клиентского доступа почтовых ящиков, чтобы их можно было временно отключить, чтобы владелец (или другие пользователи) не мог получить доступ к этому почтовому ящику во время выполнения этой процедуры. Наконец, вы можете получить текущий размер и количество элементов в папке "элементы с возможностью восстановления". После удаления элементов из папки "элементы с возможностью восстановления" в действии 5 эти сведения будут использоваться для проверки фактического удаления элементов.</span><span class="sxs-lookup"><span data-stu-id="830db-p112">Additionally, you need to get the mailbox client access settings so you can temporarily disable them so the owner (or other users) can't access the mailbox during this procedure. Finally, you can get the current size and number of items in the Recoverable Items folder. After you delete items in the Recoverable Items folder in Step 5, you'll use this information to verify that items were actually removed.</span></span>
  
1. <span data-ttu-id="830db-p113">[Подключитесь к Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Обязательно используйте имя пользователя и пароль для учетной записи администратора, которой назначены соответствующие роли управления в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="830db-p113">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Be sure to use a user name and password for an administrator account that's been assigned the appropriate management roles in Exchange Online.</span></span> 
    
2. <span data-ttu-id="830db-154">Выполните следующую команду, чтобы получить сведения об использовании восстановления отдельных элементов и периода хранения удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="830db-154">Run the following command to get information about single item recovery and the deleted item retention period.</span></span>

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   <span data-ttu-id="830db-p114">Если включено восстановление отдельных элементов, необходимо отключить его на шаге 2. Если срок хранения удаленных элементов не задан в течение 30 дней (максимальное значение в Exchange Online), его можно увеличить на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="830db-p114">If single item recovery is enabled, you'll have to disable it in Step 2. If the deleted item retention period isn't set for 30 days (the maximum value in Exchange Online), then you can increase it in Step 2.</span></span> 
    
3. <span data-ttu-id="830db-157">Выполните следующую команду, чтобы получить параметры доступа к почтовому ящику для почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="830db-157">Run the following command to get the mailbox access settings for the mailbox.</span></span> 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   <span data-ttu-id="830db-158">Все эти способы доступа будут отключены на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="830db-158">You'll disable all of these access methods in Step 2.</span></span>
    
4. <span data-ttu-id="830db-159">Выполните следующую команду, чтобы получить сведения о удержаниях и политиках хранения Office 365, применяемых к почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="830db-159">Run the following command to get information about the holds and Office 365 retention policies applied to the mailbox.</span></span>
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > <span data-ttu-id="830db-160">Если в свойстве *InPlaceHolds* слишком много значений, а не все они отображаются, можно выполнить `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` команду, чтобы отобразить каждое значение в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="830db-160">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
5. <span data-ttu-id="830db-161">Выполните следующую команду, чтобы получить сведения о политиках хранения Office 365 для всей Организации.</span><span class="sxs-lookup"><span data-stu-id="830db-161">Run the following command to get information about any organization-wide Office 365 retention policies.</span></span> 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   <span data-ttu-id="830db-162">Если в Организации есть политики хранения Office 365 на уровне Организации, необходимо исключить почтовый ящик из этих политик на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="830db-162">If your organization has any organization-wide Office 365 retention policies, you'll have to exclude the mailbox from these policies in Step 3.</span></span>

   > [!TIP]
    > <span data-ttu-id="830db-163">Если в свойстве *InPlaceHolds* слишком много значений, а не все они отображаются, можно выполнить `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` команду, чтобы отобразить каждое значение в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="830db-163">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
6. <span data-ttu-id="830db-164">Выполните следующую команду, чтобы получить текущий размер и общее количество элементов в папках и вложенных папках в папке "элементы с возможностью восстановления" в основном почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="830db-164">Run the following command to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="830db-165">Если архивный почтовый ящик пользователя включен, выполните следующую команду, чтобы получить размер и общее количество элементов в папках и подпапках в папке "элементы с возможностью восстановления" в своем архивном почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="830db-165">If the user's archive mailbox is enabled, run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in their archive mailbox.</span></span> 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="830db-p115">При удалении элементов на шаге 5 можно удалить или не удалять элементы из папки "элементы с возможностью восстановления" в основном архивном почтовом ящике пользователя. Обратите внимание, что если включено автоматическое расширение архивации для почтового ящика, элементы в вспомогательном архивном почтовом ящике не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="830db-p115">When you delete items in Step 5, you can choose to delete or not delete items in the Recoverable Items folder in the user's primary archive mailbox. Note that if auto-expanding archiving is enabled for the mailbox, items in an auxiliary archive mailbox won't be deleted.</span></span>
  
## <a name="step-2-prepare-the-mailbox"></a><span data-ttu-id="830db-168">Шаг 2: подготовка почтового ящика</span><span class="sxs-lookup"><span data-stu-id="830db-168">Step 2: Prepare the mailbox</span></span>

<span data-ttu-id="830db-169">После сбора и сохранения сведений о почтовом ящике следующим шагом является подготовка почтового ящика путем выполнения следующих задач.</span><span class="sxs-lookup"><span data-stu-id="830db-169">After collecting and saving information about the mailbox, the next step is to prepare the mailbox by performing the following tasks:</span></span> 
  
- <span data-ttu-id="830db-170">**Отключить клиентский доступ к почтовому ящику** , чтобы владелец почтового ящика не получил доступ к своему почтовому ящику и вносить в него изменения данных почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="830db-170">**Disable client access to mailbox** so that the mailbox owner can't access their mailbox and make any changes to the mailbox data during this procedure.</span></span> 
    
- <span data-ttu-id="830db-171">**Увеличьте срок хранения удаленных элементов** до 30 дней (максимальное значение в Exchange Online), чтобы элементы не удалялись из папки "элементы с возможностью восстановления", прежде чем их можно будет удалить на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="830db-171">**Increase the deleted item retention period** to 30 days (the maximum value in Exchange Online) so that items aren't purged from the Recoverable Items folder before you can delete them in Step 5.</span></span> 
    
- <span data-ttu-id="830db-172">**Отключите восстановление отдельных элементов** , чтобы элементы не сохранялись (срок хранения удаленных элементов) после удаления их из папки "элементы с возможностью восстановления" на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="830db-172">**Disable single Item recovery** so that items won't be retained (for the duration of the deleted item retention period) after you delete them from the Recoverable Items folder in Step 5.</span></span> 
    
- <span data-ttu-id="830db-173">**Отключите помощник по работе с управляемЫми папками** , чтобы он не обпомнил почтовый ящик и сохранял элементы, которые вы удалили на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="830db-173">**Disable the Managed Folder Assistant** so that it doesn't process the mailbox and retain the items that you delete in Step 5.</span></span> 
    
<span data-ttu-id="830db-174">Выполните следующие действия в Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="830db-174">Perform the following steps in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="830db-p116">Выполните следующую команду, чтобы отключить все клиентские права на доступ к почтовому ящику. Синтаксис команды предполагает, что все методы клиентского доступа были включены для почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="830db-p116">Run the following command to disable all client access to the mailbox. The command syntax assumes that all client access methods were enabled on the mailbox.</span></span>

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > <span data-ttu-id="830db-p117">Отключение всех методов клиентского доступа к почтовому ящику может занять до 60 минут. Обратите внимание, что отключение этих методов доступа не отключит владельца почтового ящика, в котором они вошли в систему. Если владелец не вошел в систему, он не сможет получить доступ к своему почтовому ящику после отключения этих методов доступа.</span><span class="sxs-lookup"><span data-stu-id="830db-p117">It might take up to 60 minutes to disable all client access methods to the mailbox. Note that disabling these access methods won't disconnect the mailbox owner they're currently signed in. If the owner isn't signed in, then they won't be able to access their mailbox after these access methods are disabled.</span></span> 
  
2. <span data-ttu-id="830db-p118">Выполните следующую команду, чтобы увеличить срок хранения удаленных элементов максимум 30 дней. Предполагается, что текущее значение меньше 30 дней.</span><span class="sxs-lookup"><span data-stu-id="830db-p118">Run the following command to increase the deleted item retention period the maximum of 30 days. This assumes that the current setting is less than 30 days.</span></span> 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. <span data-ttu-id="830db-182">Выполните следующую команду, чтобы отключить восстановление отдельных элементов.</span><span class="sxs-lookup"><span data-stu-id="830db-182">Run the following command to disable single item recovery.</span></span>
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > <span data-ttu-id="830db-p119">Отключение восстановления отдельных элементов может занять до 60 минут. Не удаляйте элементы в папке "элементы с возможностью восстановления" до истечения этого периода.</span><span class="sxs-lookup"><span data-stu-id="830db-p119">It might take up to 60 minutes to disable single item recovery. Don't delete items in the Recoverable Items folder until this period has elapsed.</span></span> 
  
4. <span data-ttu-id="830db-p120">Выполните следующую команду, чтобы предотвратить обработку почтового ящика помощником для управляемых папок. Как было сказано ранее, помощник для управляемых папок можно отключить только в том случае, если к почтовому ящику не применяется политика хранения Office 365 с блокировкой сохранения.</span><span class="sxs-lookup"><span data-stu-id="830db-p120">Run the following command to prevent the Managed Folder Assistant from processing the mailbox. As previously explained, you can disable the Managed Folder Assistant only if an Office 365 retention policy with a Preservation Lock is not applied to the mailbox.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a><span data-ttu-id="830db-187">Шаг 3: удаление всех удержаний из почтового ящика</span><span class="sxs-lookup"><span data-stu-id="830db-187">Step 3: Remove all holds from the mailbox</span></span>

<span data-ttu-id="830db-p121">Последний шаг перед удалением элементов из папки "элементы с возможностью восстановления" состоит в том, чтобы удалить все удержания (определенные на шаге 1), размещенные в почтовом ящике. Все удержания необходимо удалить, чтобы элементы не сохранялись после удаления их из папки "элементы с возможностью восстановления". В следующих разделах содержатся сведения об удалении различных типов удержаний для почтового ящика. В разделе [Дополнительные сведения](#more-information) приведены советы по определению типа удержания, который может быть включен в почтовый ящик. Для получения дополнительных сведений Узнайте, [как определить тип удержания, размещенного в почтовом ящике Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="830db-p121">The last step before you can delete items from the Recoverable Items folder is to remove all holds (that you identified in Step 1) placed on the mailbox. All holds must be removed so that items won't be retained after you delete them from the Recoverable Items folder. The following sections contain information about removing different types of holds on a mailbox. See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox. For additional information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="830db-193">Как было сказано ранее, прежде чем удалять удержание из почтового ящика, проверяйте управление записями или юридическими отделами.</span><span class="sxs-lookup"><span data-stu-id="830db-193">As previously stated, check with your records management or legal departments before removing a hold from a mailbox.</span></span> 
  
 ### <a name="litigation-hold"></a><span data-ttu-id="830db-194">Хранение для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="830db-194">Litigation Hold</span></span>
  
<span data-ttu-id="830db-195">Выполните следующую команду в Exchange Online PowerShell, чтобы удалить удержание для судебного разбирательства из почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="830db-195">Run the following command in Exchange Online PowerShell to remove a Litigation Hold from the mailbox.</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> <span data-ttu-id="830db-p122">Аналогично отключению методов клиентского доступа и восстановления отдельных элементов может потребоваться до 60 минут, чтобы удалить удержание для судебного разбирательства. Не удаляйте элементы из папки "элементы с возможностью восстановления" до истечения этого периода.</span><span class="sxs-lookup"><span data-stu-id="830db-p122">Similar to disabling the client access methods and single item recovery, it might take up to 60 minutes to remove the Litigation Hold. Don't delete items from the Recoverable Items folder until this period has elapsed.</span></span> 
  
 ### <a name="in-place-hold"></a><span data-ttu-id="830db-198">Хранение на месте</span><span class="sxs-lookup"><span data-stu-id="830db-198">In-Place Hold</span></span>
  
<span data-ttu-id="830db-p123">Выполните следующую команду в Exchange Online PowerShell, чтобы определить удержание на месте, которое размещено в почтовом ящике. Используйте GUID для хранения на месте, определенного в действии 1.</span><span class="sxs-lookup"><span data-stu-id="830db-p123">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's placed on the mailbox. Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
<span data-ttu-id="830db-p124">Определив удержание на месте, вы можете удалить почтовый ящик из удержания с помощью центра администрирования Exchange или Exchange Online PowerShell. Дополнительные сведения см. [в статье Создание или удаление удержания на месте](https://go.microsoft.com/fwlink/?linkid=852668).</span><span class="sxs-lookup"><span data-stu-id="830db-p124">After you identify the In-Place Hold, you can use the Exchange admin center (EAC) or Exchange Online PowerShell to remove the mailbox from the hold. For more information, see [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span></span>
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a><span data-ttu-id="830db-203">Политики хранения Office 365, применяемые к определенным почтовым ящикам</span><span class="sxs-lookup"><span data-stu-id="830db-203">Office 365 retention policies applied to specific mailboxes</span></span>
  
<span data-ttu-id="830db-p125">Выполните следующую команду в [оболочке PowerShell центра &amp; безопасности Office 365](https://go.microsoft.com/fwlink/?linkid=627084) , чтобы определить политику хранения Office 365, применяемую к почтовому ящику. Используйте GUID (не включая `mbx` `skp` префикс) для политики хранения, определенной на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="830db-p125">Run the following command in [Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the Office 365 retention policy that is applied to the mailbox. Use the GUID (not including the  `mbx` or  `skp` prefix) for the retention policy that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
<span data-ttu-id="830db-206">Определив политику хранения, перейдите на страницу "хранение управления **датой** \> \*\*\*\* " в центре соответствия требованиям безопасности &amp; , измените политику хранения, определенную на предыдущем шаге, и удалите почтовый ящик из списка получателей, включенных в политику хранения.</span><span class="sxs-lookup"><span data-stu-id="830db-206">After you identify the retention policy, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy that you identified in the previous step, and remove the mailbox from the list of recipients that are included in the retention policy.</span></span> 
  
 ### <a name="organization-wide-office-365-retention-policies"></a><span data-ttu-id="830db-207">Политики хранения Office 365 на уровне Организации</span><span class="sxs-lookup"><span data-stu-id="830db-207">Organization-wide Office 365 retention policies</span></span>
  
<span data-ttu-id="830db-p126">Политики хранения Office 365 на уровне Организации и Exchange применяются ко всем почтовым ящикам в Организации. Они применяются на уровне Организации (не на уровне почтового ящика) и возвращаются при выполнении командлета **Get-OrganizationConfig** на этапе 1. Выполните приведенную ниже команду в командной консоли [PowerShell Security &amp; Center](https://go.microsoft.com/fwlink/?linkid=627084) , чтобы определить политики хранения Office 365 для всей Организации. Используйте идентификатор GUID (не включая `mbx` префикс) для политик хранения на уровне Организации, определенных на этапе 1.</span><span class="sxs-lookup"><span data-stu-id="830db-p126">Organization-wide and Exchange-wide Office 365 retention policies are applied to every mailbox in the organization. They are applied at the organization level (not the mailbox level) and are returned when you run the **Get-OrganizationConfig** cmdlet in Step 1. Run the following command in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the organization-wide Office 365 retention policies. Use the GUID (not including the  `mbx` prefix) for the organization-wide retention policies that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

<span data-ttu-id="830db-p127">определив политики хранения Office 365 в масштабах всей организации, перейдите на страницу " \*\*\*\* \> **хранение** управления датой" в центре соответствия &amp; требованиям безопасности, измените каждую политику хранения на уровне организации, определенную в разделе предыдущий шаг и добавьте почтовый ящик в список исключенных получателей. Это приведет к удалению почтового ящика пользователя из политики хранения.</span><span class="sxs-lookup"><span data-stu-id="830db-p127">After you identify the organization-wide Office 365 retention policies, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit each organization-wide retention policy that you identified in the previous step, and add the mailbox to the list of excluded recipients. Doing this will remove the user's mailbox from the retention policy.</span></span> 

### <a name="office-365-retention-labels"></a><span data-ttu-id="830db-214">Метки хранения Office 365</span><span class="sxs-lookup"><span data-stu-id="830db-214">Office 365 retention labels</span></span>

<span data-ttu-id="830db-p128">Когда пользователь применяет метку, настроенную для сохранения контента или сохранения и удаления контента в любой папке или элементе почтового ящика, свойство Mailbox *комплианцетагхолдапплиед* имеет значение **true**. В этом случае почтовый ящик считается заблокированным, как если бы он был включен в удержание для судебного разбирательства или назначено политике хранения Office 365.</span><span class="sxs-lookup"><span data-stu-id="830db-p128">Whenever a user applies a label that's configured to retain content or retain and then delete content to any folder or item in their mailbox, the *ComplianceTagHoldApplied* mailbox property is set to **True**. When this happens, the mailbox is considered to be on hold, just as if it was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span>

<span data-ttu-id="830db-217">Чтобы просмотреть значение свойства *комплианцетагхолдапплиед* , выполните следующую команду в Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="830db-217">To view the value of the *ComplianceTagHoldApplied* property, run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

<span data-ttu-id="830db-p129">После определения того, что почтовый ящик находится на удержании, так как метка хранения применяется к папке или элементу, можно использовать средство поиска контента в центре безопасности _Амп_ соответствия требованиям для поиска элементов с метками с помощью условия поиска ComplianceTag. Дополнительные сведения можно найти в разделе условия поиска в [запросАх ключевых слов и условиях поиска для поиска контента](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span><span class="sxs-lookup"><span data-stu-id="830db-p129">After you've identified that a mailbox is on hold because a retention label is applied to a folder or item, you can use the Content Search tool in the Security & Compliance Center to search for labeled items by using the ComplianceTag search condition. For more information, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span></span>

<span data-ttu-id="830db-220">Дополнительные сведения о метках можно найти в статье [Обзор меток Office 365](labels.md).</span><span class="sxs-lookup"><span data-stu-id="830db-220">For more information about labels, see [Overview of Office 365 labels](labels.md).</span></span>

 ### <a name="ediscovery-case-holds"></a><span data-ttu-id="830db-221">футляр для обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="830db-221">eDiscovery case holds</span></span>
  
<span data-ttu-id="830db-p130">Выполните следующие команды в [оболочке &amp; PowerShell Security Center](https://go.microsoft.com/fwlink/?linkid=627084) , чтобы определить удержание, связанНое с вариантом обнаружения электронных данных, который применяется к почтовому ящику. Используйте GUID (не включая `UniH` префикс) для удержания обнаружения электронных данных, определенного в действии 1. Обратите внимание, что во второй команде отображается имя случая обнаружения электронных данных, с которым связана удержание. Третья команда отображает имя удержания.</span><span class="sxs-lookup"><span data-stu-id="830db-p130">Run the following commands in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the hold associated with an eDiscovery case that's applied to the mailbox. Use the GUID (not including the  `UniH` prefix) for the eDiscovery hold that you identified in Step 1. Note that the second command displays the name of the eDiscovery case the hold is associated with; the third command displays the name of the hold.</span></span> 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

<span data-ttu-id="830db-p131">Определив имя варианта обнаружения электронных данных и удержания, перейдите на страницу **Обнаружение электронных** данных для &amp; \*\*поиска &amp; \*\* \> в центре безопасности, откройте обращение и удалите почтовый ящик из удержания. Дополнительные сведения: Управление делами [eDiscovery в центре безопасности &amp; и соответствия требованиям Office 365](manage-ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="830db-p131">After you've identified the name of the eDiscovery case and the hold, go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and remove the mailbox from the hold. For more information, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md).</span></span>
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a><span data-ttu-id="830db-227">Шаг 4: удаление задержки хранения из почтового ящика</span><span class="sxs-lookup"><span data-stu-id="830db-227">Step 4: Remove the delay hold from the mailbox</span></span>

<span data-ttu-id="830db-p132">После удаления любого типа удержания из почтового ящика значение свойства Mailbox *делайхолдапплиед* задается равным **true**. Это происходит в следующий раз, когда помощник для управляемых папок обрабатывает почтовый ящик и обнаруживает, что удержание было удалено. Это называется *Задержка хранения* и означает, что фактическое удаление удержания задерживается в течение 30 дней, чтобы предотвратить окончательное удаление данных из почтового ящика. (Цель задержки хранения заключается в предоставлении администраторам возможности поиска и восстановления элементов почтовых ящиков, которые удаляются после удаления удержания.)  Если задержка отложена, почтовый ящик по-прежнему считается на хранение неограниченной длительности, как если бы почтовый ящик находился на удержании судебного разбирательства. По истечении 30 дней задержка задержки и Office 365 автоматически попытаются удалить задержку (задав для свойства *Делайхолдапплиед* **значение false**), чтобы удержание фактически было удалено.</span><span class="sxs-lookup"><span data-stu-id="830db-p132">After any type of hold is removed from a mailbox, the value of the *DelayHoldApplied* mailbox property is set to **True**. This occurs the next time the Managed Folder Assistant processes the mailbox and detects that a hold has been removed. This is called a *delay hold* and means the actual removal of the hold is delayed for 30 days to prevent data from being permanently deleted from the mailbox. (The purpose of a delay hold is to give admins an opportunity to search for or recover mailbox items that will be purged after a hold is removed.)  When a delay hold is placed on the mailbox, the mailbox is still considered to be on hold for an unlimited duration, as if the mailbox was on Litigation Hold. After 30 days, the delay hold expires, and Office 365 will automatically attempt to remove the delay hold (by setting the *DelayHoldApplied* property to **False**) so that the hold is actually removed.</span></span> 

<span data-ttu-id="830db-p133">Прежде чем удалять элементы на шаге 5, необходимо удалить их из почтового ящика. Сначала определите, применяется ли задержка хранения к почтовому ящику, выполнив следующую команду в Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="830db-p133">Before you can delete items in Step 5, you have to remove the delay hold from the mailbox. First, determine if the delay hold is applied to the mailbox by running the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> | FL DelayHoldApplied
```

<span data-ttu-id="830db-p134">Если для свойства *делайхолдапплиед* задано значение **false**, для почтового ящика не было включено удержание задержки. Вы можете перейти к шагу 5 и удалять элементы в папке "элементы с возможностью восстановления".</span><span class="sxs-lookup"><span data-stu-id="830db-p134">If the value of the *DelayHoldApplied* property is set to **False**, a delay hold has not been placed on the mailbox. You can go to Step 5 and delete items in the Recoverable Items folder.</span></span>

<span data-ttu-id="830db-237">Если для свойства *делайхолдапплиед* задано значение **true**, выполните следующую команду, чтобы удалить отложенную блокировку:</span><span class="sxs-lookup"><span data-stu-id="830db-237">If the value of the *DelayHoldApplied* property is set to **True**, run the following command to remove the delay hold:</span></span>

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
<span data-ttu-id="830db-238">Обратите внимание, что для использования параметра *ремоведелайхолдапплиед* необходимо назначить роль юридического удержания в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="830db-238">Note that you must be assigned the Legal Hold role in Exchange Online to use the *RemoveDelayHoldApplied* parameter.</span></span>

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a><span data-ttu-id="830db-239">Шаг 5: удаление элементов из папки "элементы с возможностью восстановления"</span><span class="sxs-lookup"><span data-stu-id="830db-239">Step 5: Delete items in the Recoverable Items folder</span></span>

<span data-ttu-id="830db-p135">Теперь вы готовы удалить элементы в папке "элементы с возможностью восстановления" с помощью командлета [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) в Exchange Online PowerShell. При запуске командлета **Search — Mailbox** можно выбрать три варианта.</span><span class="sxs-lookup"><span data-stu-id="830db-p135">Now you're ready to actually delete items in the Recoverable Items folder by using the [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet in Exchange Online PowerShell. You have three options when running the **Search-Mailbox** cmdlet.</span></span> 
  
- <span data-ttu-id="830db-242">Скопируйте элементы в целевой почтовый ящик, прежде чем удалять их, чтобы при необходимости можно было просматривать элементы, прежде чем удалять их.</span><span class="sxs-lookup"><span data-stu-id="830db-242">Copy items to a target mailbox before you delete them so that you can review the items, if necessary, before you delete them.</span></span>
    
- <span data-ttu-id="830db-243">Скопируйте элементы в целевой почтовый ящик и удалите их в одной команде.</span><span class="sxs-lookup"><span data-stu-id="830db-243">Copy items to a target mailbox and delete them in the same command.</span></span>
    
- <span data-ttu-id="830db-244">Удаление элементов без их копирования в целевой почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="830db-244">Delete items without copying them to a target mailbox.</span></span> 
    
<span data-ttu-id="830db-p136">Обратите внимание, что элементы в папке "элементы с возможностью восстановления" в основном архивном почтовом ящике пользователя также будут удалены при запуске командлета **Search — Mailbox** . Чтобы избежать этого, можно включить параметр *донотинклудеарчиве* . Как было сказано ранее, если для почтового ящика включено автоматическое расширение архивации, командлет \* \* Search-Mailbox \* \* не удаляет элементы в вспомогательном архивном почтовом ящике. Дополнительные сведения об автоматическом развертывании архивов приведены [в статье Обзор неограниченного архивирования в Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="830db-p136">Note that items in the Recoverable Items folder in the user's primary archive mailbox will also be deleted when you run the **Search-Mailbox** cmdlet. To prevent this, you can include the  *DoNotIncludeArchive*  switch. And as previously stated, if auto-expanding archiving is enabled for the mailbox, the \*\* Search-Mailbox \*\* cmdlet doesn't deleted items in an auxiliary archive mailbox. For more information about auto-expanding archive, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="830db-p137">Если вы включите поисковый запрос (используя параметр  *SearchQuery*  ), командлет **Search-Mailbox** вернет максимум 10 000 элементов. Поэтому, чтобы удалить более 10 000 элементов, может потребоваться выполнить команду **Search-Mailbox** несколько раз.</span><span class="sxs-lookup"><span data-stu-id="830db-p137">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
  
<span data-ttu-id="830db-p138">В приведенных ниже примерах показан синтаксис команд для каждого из этих параметров. В этих примерах `-SearchQuery size>0` используется значение параметра, которое удаляет все элементы из всех вложенных папок в папке "элементы с возможностью восстановления". Если необходимо удалить только элементы, которые отвечают определенным условиям, можно также использовать параметр *SearchQuery* для указания других условий, например темы сообщения или диапазона дат. Ниже приведены [другие примеры использования параметра SearchQuery](#other-examples-of-using-the-searchquery-parameter) ниже.</span><span class="sxs-lookup"><span data-stu-id="830db-p138">The following examples show the command syntax for each of these options. These examples use the  `-SearchQuery size>0` parameter value, which deletes all items from all subfolders in the Recoverable Items folder. If you need to delete only items that match specific conditions, you can also use the  *SearchQuery*  parameter to specify other conditions, such as the subject of a message or a date range. See the [other examples of using the SearchQuery parameter](#other-examples-of-using-the-searchquery-parameter) below.</span></span> 
  
### <a name="example-1"></a><span data-ttu-id="830db-255">Пример 1</span><span class="sxs-lookup"><span data-stu-id="830db-255">Example 1</span></span>

<span data-ttu-id="830db-p139">В этом примере показано, как скопировать все элементы из папки "элементы с возможностью восстановления" пользователя в папку почтового ящика поиска обнаружения в Организации. Это позволяет просматривать элементы перед их окончательным удалением.</span><span class="sxs-lookup"><span data-stu-id="830db-p139">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox. This lets you review the items before you permanently delete them.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

<span data-ttu-id="830db-p140">В предыдущем примере не требуется копировать элементы в почтовый ящик поиска обнаружения. Вы можете копировать сообщения в любой целевой почтовый ящик. Тем не менее, чтобы запретить доступ к потенциально конфиденциальным данным почтовых ящиков, рекомендуется копировать сообщения в почтовый ящик, доступ к которому ограничен уполномоченным сотрудникам. По умолчанию доступ к почтовому ящику поиска обнаружения по умолчанию ограничен только членами группы ролей "Управление обнаружением" в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="830db-p140">In the previous example, it isn't required to copy items to the Discovery Search Mailbox. You can copy messages to any target mailbox. However, to prevent access to potentially sensitive mailbox data, we recommend copying messages to a mailbox that has access restricted to authorized personnel. By default, access to the default Discovery Search Mailbox is restricted to members of the Discovery Management role group in Exchange Online.</span></span> 
  
### <a name="example-2"></a><span data-ttu-id="830db-262">Пример 2</span><span class="sxs-lookup"><span data-stu-id="830db-262">Example 2</span></span>

<span data-ttu-id="830db-263">В этом примере показано, как скопировать все элементы из папки "элементы с возможностью восстановления" пользователя в папку почтового ящика поиска обнаружения и затем удалить их из папки "элементы с возможностью восстановления" пользователя.</span><span class="sxs-lookup"><span data-stu-id="830db-263">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox and then deletes the items from the user's Recoverable Items folder.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a><span data-ttu-id="830db-264">Пример 3</span><span class="sxs-lookup"><span data-stu-id="830db-264">Example 3</span></span>

<span data-ttu-id="830db-265">В этом примере удаляются все элементы в папке "элементы с возможностью восстановления", не копируя их в целевой почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="830db-265">This example deletes all items in the user's Recoverable Items folder, without copying them to a target mailbox.</span></span> 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a><span data-ttu-id="830db-266">Другие примеры использования параметра SearchQuery</span><span class="sxs-lookup"><span data-stu-id="830db-266">Other examples of using the SearchQuery parameter</span></span>

<span data-ttu-id="830db-p141">Ниже приведено несколько примеров использования параметра *SearchQuery* для поиска определенных сообщений. Если для поиска определенных элементов используется параметр *SearchQuery* , рассмотрите возможность копирования результатов поиска в целевой почтовый ящик, чтобы можно было просмотреть результаты поиска, а затем изменить запрос, если это необходимо, прежде чем удалять результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="830db-p141">Here are a few examples of using the  *SearchQuery*  parameter to find specific messages. If you use the  *SearchQuery*  parameter to search for specific items, consider copying the search results to a target mailbox so that you can review the search results and then revise the query if necessary before you delete the results of a search.</span></span> 
  
<span data-ttu-id="830db-269">В этом примере возвращаются сообщения, содержащие определенную фразу в поле Subject.</span><span class="sxs-lookup"><span data-stu-id="830db-269">This example returns messages that contain a specific phrase in the Subject field.</span></span>
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

<span data-ttu-id="830db-270">В этом примере возвращаются сообщения, отправленные в указанный диапазон дат.</span><span class="sxs-lookup"><span data-stu-id="830db-270">This example returns messages that were sent within the specified date range.</span></span>
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
<span data-ttu-id="830db-271">В этом примере возвращаются сообщения, отправленные указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="830db-271">This example returns messages that were sent to the specified person.</span></span>

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a><span data-ttu-id="830db-272">Проверка того, что элементы были удалены</span><span class="sxs-lookup"><span data-stu-id="830db-272">Verify that items were deleted</span></span>

<span data-ttu-id="830db-p142">Чтобы убедиться, что вы успешно удалили элементы из папки "элементы с возможностью восстановления" почтового ящика, используйте командлет **Get-MailboxFolderStatistics** в Exchange Online PowerShell, чтобы проверить размер и количество элементов в папке "элементы с возможностью восстановления". Вы можете сравнить статистику с теми, которые были собраны на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="830db-p142">To verify that you've successfully deleted items from the Recoverable Items folder of a mailbox, use **Get-MailboxFolderStatistics** cmdlet in Exchange Online PowerShell to check the size and number of items in Recoverable Items folder. You can compare these statistics with the ones you collected in Step 1.</span></span> 
  
<span data-ttu-id="830db-275">Выполните следующую команду, чтобы получить текущий размер и общее количество элементов в папках и вложенных папках в папке "элементы с возможностью восстановления" в основном почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="830db-275">Run the following command in to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
<span data-ttu-id="830db-276">Выполните следующую команду, чтобы получить размер и общее количество элементов в папках и вложенных папках в папке "элементы с возможностью восстановления" в архивном почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="830db-276">Run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in the user's archive mailbox.</span></span> 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a><span data-ttu-id="830db-277">Шаг 6: возврат к предыдущему состоянию почтового ящика</span><span class="sxs-lookup"><span data-stu-id="830db-277">Step 6: Revert the mailbox to its previous state</span></span>

<span data-ttu-id="830db-p143">Последним шагом будет возврат к предыдущей конфигурации почтового ящика. Это означает, что вы переопределяете свойства, измененные в шаге 2, и повторно примените удержания, которые вы удалили на шаге 3. В том числе:</span><span class="sxs-lookup"><span data-stu-id="830db-p143">The final step is to revert the mailbox back to its previous configuration. This means resetting the properties that you changed in Step 2 and re-applying the holds that you removed in Step 3. This includes:</span></span>
  
- <span data-ttu-id="830db-p144">Возврат к предыдущему значению срока хранения удаленного элемента. Кроме того, можно просто оставить это значение 30 дней, максимальное значение в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="830db-p144">Changing the deleted item retention period back to its previous value. Alternatively, you can just leave this set to 30 days, the maximum value in Exchange Online.</span></span>
    
- <span data-ttu-id="830db-283">Повторное включение восстановления отдельных элементов.</span><span class="sxs-lookup"><span data-stu-id="830db-283">Re-enabling single Item recovery.</span></span>
    
- <span data-ttu-id="830db-284">Повторное включение клиентских методов доступа, чтобы владелец мог получать доступ к своему почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="830db-284">Re-enabling the client access methods so that the owner can access their mailbox.</span></span>
    
- <span data-ttu-id="830db-285">Повторное применение удаленных политик хранения и Office 365.</span><span class="sxs-lookup"><span data-stu-id="830db-285">Re-applying the holds and Office 365 retention policies that you removed.</span></span>
    
- <span data-ttu-id="830db-286">Повторное включение помощника для управляемых папок для обработки почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="830db-286">Re-enabling the Managed Folder Assistant to process the mailbox.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="830db-287">Рекомендуем подождать 24 часа после повторного применения политики хранения или политики хранения Office 365 (и подтвердить, что она находится на месте) перед повторным включением обработки почтового ящика помощником для управляемых папок.</span><span class="sxs-lookup"><span data-stu-id="830db-287">We recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant to process the mailbox.</span></span> 
  
<span data-ttu-id="830db-288">Выполните следующие действия (в указанной последовательности) в Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="830db-288">Perform the following steps (in the specified sequence) in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="830db-p145">Выполните следующую команду, чтобы вернуться к исходному значению срока хранения удаленного элемента. Предполагается, что предыдущее значение меньше 30 дней; Например, 14 дней.</span><span class="sxs-lookup"><span data-stu-id="830db-p145">Run the following command to change the deleted item retention period back to its original value. This assumes that the previous setting is less than 30 days; for example 14 days.</span></span> 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. <span data-ttu-id="830db-291">Выполните следующую команду, чтобы снова включить восстановление отдельных элементов.</span><span class="sxs-lookup"><span data-stu-id="830db-291">Run the following command to re-enable single item recovery.</span></span>
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. <span data-ttu-id="830db-292">Выполните следующую команду, чтобы снова включить все методы клиентского доступа к почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="830db-292">Run the following command to re-enable all client access methods to the mailbox.</span></span>
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. <span data-ttu-id="830db-p146">Повторно примените удержания, которые вы удалили на шаге 3. В зависимости от типа удержания используйте одну из следующих процедур.</span><span class="sxs-lookup"><span data-stu-id="830db-p146">Re-apply the holds that you removed in Step 3. Depending on the type of hold, use one of the following procedures.</span></span>
    
    <span data-ttu-id="830db-295">**Хранение для судебного разбирательства**</span><span class="sxs-lookup"><span data-stu-id="830db-295">**Litigation Hold**</span></span>
    
    <span data-ttu-id="830db-296">Выполните следующую команду, чтобы снова включить удержание для судебного разбирательства для почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="830db-296">Run the following command to re-enable a Litigation Hold for the mailbox.</span></span>
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    <span data-ttu-id="830db-297">**In-Place Hold**</span><span class="sxs-lookup"><span data-stu-id="830db-297">**In-Place Hold**</span></span>
    
    <span data-ttu-id="830db-298">Используйте центр администрирования Exchange (или Exchange Online PowerShell), чтобы добавить почтовый ящик обратно в режим удержания на месте.</span><span class="sxs-lookup"><span data-stu-id="830db-298">Use the EAC (or Exchange Online PowerShell) to add the mailbox back to the In-Place Hold.</span></span> 
    
    <span data-ttu-id="830db-299">**Политики хранения Office 365, применяемые к определенным почтовым ящикам**</span><span class="sxs-lookup"><span data-stu-id="830db-299">**Office 365 retention policies applied to specific mailboxes**</span></span>
    
    <span data-ttu-id="830db-p147">Используйте центр соответствия &amp; требованиям безопасности, чтобы добавить почтовый ящик обратно в политику хранения Office 365. Перейдите на страницу " **Хранение** управления **датой** \> " в центре &amp; безопасности и соответствия требованиям, измените политику хранения и добавьте почтовый ящик обратно в список получателей, к которым применяется политика хранения.</span><span class="sxs-lookup"><span data-stu-id="830db-p147">Use the Security &amp; Compliance Center to add the mailbox back to the Office 365 retention policy. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy, and add the mailbox back to the list of recipients that the retention policy is applied to.</span></span> 
    
    <span data-ttu-id="830db-302">**Политики хранения Office 365 на уровне Организации**</span><span class="sxs-lookup"><span data-stu-id="830db-302">**Organization-wide Office 365 retention policies**</span></span>
    
    <span data-ttu-id="830db-p148">Если вы удалили политику хранения на уровне Организации или на уровне Exchange, исключив ее из политики, используйте центр соответствия требованиям &amp; безопасности для удаления почтового ящика из списка исключенных пользователей. Перейдите на страницу " **Хранение** управления **датой** \> " в центре &amp; безопасности и соответствия требованиям, измените политику хранения на уровне Организации и удалите почтовый ящик из списка исключенных получателей. Это приведет к повторному применению политики хранения к почтовому ящику пользователя.</span><span class="sxs-lookup"><span data-stu-id="830db-p148">If you removed an organization-wide or Exchange-wide retention policy by excluding it from the policy, then use the Security &amp; Compliance Center to remove the mailbox from the list of excluded users. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the organization-wide retention policy, and remove the mailbox from the list of excluded recipients. Doing this will re-apply the retention policy to the user's mailbox.</span></span> 
    
    <span data-ttu-id="830db-306">**футляр для обнаружения электронных данных**</span><span class="sxs-lookup"><span data-stu-id="830db-306">**eDiscovery case holds**</span></span>
    
    <span data-ttu-id="830db-p149">Используйте центр соответствия &amp; требованиям безопасности, чтобы добавить почтовый ящик обратное удержание, связанное с вариантом обнаружения электронных данных. Перейдите на страницу \> **Обнаружение электронных** данных \*\*поиска &amp; \*\* в центре безопасности &amp; и соответствия требованиям, откройте обращение и снова добавьте почтовый ящик в удержание.</span><span class="sxs-lookup"><span data-stu-id="830db-p149">Use the Security &amp; Compliance Center to add the mailbox back the hold that's associated with an eDiscovery case. Go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and add the mailbox back to the hold.</span></span> 
    
5. <span data-ttu-id="830db-p150">Выполните следующую команду, чтобы разрешить помощнику для управляемых папок повторно обработать почтовый ящик. Как было сказано ранее, мы рекомендуем подождать 24 часа после повторного применения политики хранения или политики хранения Office 365 (и проверить, что она находится на месте) до повторного включения помощника для управляемых папок.</span><span class="sxs-lookup"><span data-stu-id="830db-p150">Run the following command to allow the Managed Folder Assistant to process the mailbox again. As previously stated, we recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. <span data-ttu-id="830db-311">Чтобы убедиться, что почтовый ящик возвращен в предыдущую конфигурацию, можно выполнить следующие команды, а затем сравнить параметры с теми, которые были собраны на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="830db-311">To verify that the mailbox has been reverted back to its previous configuration, you can run the following commands and then compare the settings to the ones that you collected in Step 1.</span></span>

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a><span data-ttu-id="830db-312">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="830db-312">More information</span></span>

<span data-ttu-id="830db-p151">Ниже приведена таблица, в которой описывается, как определить различные типы удержаний на основе значений в свойстве *InPlaceHolds* при запуске командлетов **Get-Mailbox** или **Get-OrganizationConfig** . Более подробную информацию можно узнать в статье [как определить тип удержания, размещенного в почтовом ящике Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="830db-p151">Here's a table that describes how to identify different types of holds based on the values in the  *InPlaceHolds*  property when you run the **Get-Mailbox** or **Get-OrganizationConfig** cmdlets. For more detailed information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

<span data-ttu-id="830db-315">Как описывалось ранее, необходимо удалить все удержания и политики хранения Office 365 из почтового ящика, прежде чем вы сможете успешно удалить элементы из папки "элементы с возможностью восстановления".</span><span class="sxs-lookup"><span data-stu-id="830db-315">As previously explained, you have to remove all holds and Office 365 retention policies from a mailbox before you can successfully delete items in the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="830db-316">**Тип удержания**</span><span class="sxs-lookup"><span data-stu-id="830db-316">**Hold type**</span></span>|<span data-ttu-id="830db-317">**Пример значения**</span><span class="sxs-lookup"><span data-stu-id="830db-317">**Example value**</span></span>|<span data-ttu-id="830db-318">**Определение удержания**</span><span class="sxs-lookup"><span data-stu-id="830db-318">**How to identify the hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="830db-319">Хранение для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="830db-319">Litigation Hold</span></span>  <br/> | `True` <br/> |<span data-ttu-id="830db-320">Свойство  *LitigationHoldEnabled*  имеет значение  `True`.</span><span class="sxs-lookup"><span data-stu-id="830db-320">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="830db-321">Хранение на месте</span><span class="sxs-lookup"><span data-stu-id="830db-321">In-Place Hold</span></span>  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |<span data-ttu-id="830db-p152">Свойство *InPlaceHolds* содержит GUID хранения на месте, который размещается в почтовом ящике. Вы можете указать, что это удержание на месте, так как идентификатор GUID не начинается с префикса.</span><span class="sxs-lookup"><span data-stu-id="830db-p152">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the mailbox. You can tell this is an In-Place Hold because the GUID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="830db-324">Вы можете использовать `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` команду в Exchange Online PowerShell, чтобы получить сведения об удержанИи на месте для почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="830db-324">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the mailbox.</span></span>  <br/> |
| <span data-ttu-id="830db-325">Политики хранения Office 365 в центре соответствия &amp; требованиям безопасности, применяемые к определенным почтовым ящикам</span><span class="sxs-lookup"><span data-stu-id="830db-325">Office 365 retention policies in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> <span data-ttu-id="830db-326">или</span><span class="sxs-lookup"><span data-stu-id="830db-326">or</span></span>  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |<span data-ttu-id="830db-p153">При запуске командлета **Get – Mailbox** свойство *INPLACEHOLDS* также содержит идентификаторы GUID для политик хранения Office 365, применяемых к почтовому ящику. Вы можете определить политики хранения, так как идентификатор GUID начинается `mbx` с префикса. Обратите внимание, что если GUID политики хранения начинается с `skp` префикса, то это означает, что политика хранения применяется к беседам Skype для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="830db-p153">When you run the **Get-Mailbox** cmdlet, the  *InPlaceHolds*  property also contains GUIDs of Office 365 retention policies applied to the mailbox. You can identify retention policies because the GUID starts with the  `mbx` prefix. Note that if the GUID of the retention policy starts with the  `skp` prefix, that indicates that the retention policy is applied to Skype for Business conversations.  </span></span><br/> <span data-ttu-id="830db-330">Чтобы определить политику хранения Office 365, применяемую к почтовому ящику, выполните следующую команду в PowerShell &amp; центра соответствия требованиям безопасности:</span><span class="sxs-lookup"><span data-stu-id="830db-330">To identity the Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="830db-331">При выполнении этой команды обязательно `mbx` удалите `skp` префикс или префикс.</span><span class="sxs-lookup"><span data-stu-id="830db-331">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="830db-332">Политики хранения Office 365 для всей Организации в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="830db-332">Organization-wide Office 365 retention policies in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="830db-333">Нет значения</span><span class="sxs-lookup"><span data-stu-id="830db-333">No value</span></span>  <br/> <span data-ttu-id="830db-334">или</span><span class="sxs-lookup"><span data-stu-id="830db-334">or</span></span>  <br/>  <span data-ttu-id="830db-335">`-mbxe9b52bf7ab3b46a286308ecb29624696`(указывает, что почтовый ящик исключен из политики на уровне Организации)</span><span class="sxs-lookup"><span data-stu-id="830db-335">`-mbxe9b52bf7ab3b46a286308ecb29624696` (indicates that the mailbox is excluded from an organization-wide policy)</span></span>  <br/> |<span data-ttu-id="830db-336">Даже если при запуске командлета **Get-Mailbox** свойство *InPlaceHolds* не задано, в почтовом ящике могут применятся одна или несколько политик хранения Office 365 для всей Организации.</span><span class="sxs-lookup"><span data-stu-id="830db-336">Even if the  *InPlaceHolds*  property is empty when you run the **Get-Mailbox** cmdlet, there still might be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span>  <br/> <span data-ttu-id="830db-p154">Чтобы убедиться в этом, можно выполнить `Get-OrganizationConfig | FL InPlaceHolds` команду в Exchange Online PowerShell, чтобы получить список идентификаторов GUID для политик хранения Office 365 на уровне Организации. GUID политик хранения на уровне Организации, применяемых к почтовым ящикам Exchange, `mbx` начинаются с префикса; например `mbxa3056bb15562480fadb46ce523ff7b02`:.</span><span class="sxs-lookup"><span data-stu-id="830db-p154">To verify this, you can run the  `Get-OrganizationConfig | FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  </span></span><br/> <span data-ttu-id="830db-339">Чтобы определить политику хранения Office 365 в Организации, которая применяется к почтовому ящику, выполните следующую команду в PowerShell центра &amp; соответствия требованиям безопасности:</span><span class="sxs-lookup"><span data-stu-id="830db-339">To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="830db-340">Обратите внимание, что если почтовый ящик исключен из политики хранения Office 365 на уровне Организации, идентификатор GUID политики хранения отображается в свойстве *InPlaceHolds* почтового ящика пользователя при запуске командлета **Get-Mailbox** . Он определяется по префиксу `-mbx`; Например`-mbxe9b52bf7ab3b46a286308ecb29624696`</span><span class="sxs-lookup"><span data-stu-id="830db-340">Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696`</span></span> <br/> |
|<span data-ttu-id="830db-341">удержание дел eDiscovery в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="830db-341">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |<span data-ttu-id="830db-p155">Свойство *InPlaceHolds* также содержит GUID всех удержаний, связанных с вариантом обнаружения электронных данных в центре &amp; безопасности, который может быть размещен в почтовом ящике. Вы можете сказать, что это удержание в случае обнаружения электронных данных, так как `UniH` идентификатор GUID начинается с префикса.</span><span class="sxs-lookup"><span data-stu-id="830db-p155">The  *InPlaceHolds*  property also contains the GUID of any hold associated with an eDiscovery case in the Security &amp; Compliance Center that might be placed on the mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="830db-p156">Вы можете использовать `Get-CaseHoldPolicy` командлет в PowerShell центра &amp; соответствия требованиям безопасности, чтобы получить сведения о том случае обнаружения электронных данных, с которым связано удержание для почтового ящика. Например, вы можете выполнить команду `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` , чтобы отобразить имя удержания в почтовом ящике. При выполнении этой команды обязательно `UniH` удалите префикс.</span><span class="sxs-lookup"><span data-stu-id="830db-p156">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the mailbox is associated with. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  </span></span><br/><br/> <span data-ttu-id="830db-347">Для идентификации случая обнаружения электронных данных, с которым связано удержание, выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="830db-347">To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:</span></span><br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


