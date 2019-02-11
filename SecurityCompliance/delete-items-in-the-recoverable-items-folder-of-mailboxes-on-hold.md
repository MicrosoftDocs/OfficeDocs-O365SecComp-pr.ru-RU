---
title: Удаление элементов в папке элементов для восстановления облачные почтовые ящики на удержание - Admin справки
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Для администраторов: удаление элементов в папке элементов для восстановления пользователя почтовый ящик Exchange Online, даже в том случае, если этот почтовый ящик размещен на удержания по юридическим причинам. Это эффективный способ удаления данных, который является был случайно распределяются в Office 365.'
ms.openlocfilehash: e80f5182bc425d71c6219decd48d41cf3dce6bba
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "28009645"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a><span data-ttu-id="356a1-104">Удаление элементов в папке элементов для восстановления облачные почтовые ящики на удержание - Admin справки</span><span class="sxs-lookup"><span data-stu-id="356a1-104">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold - Admin Help</span></span>

<span data-ttu-id="356a1-p102">Для защиты от случайного или намеренного удаления существует папка элементов для восстановления для почтовый ящик Exchange Online. Он также используется для хранения элементов, которые сохраняются и доступна для функции контроля соответствия требованиям Office 365, такие как удержания и eDiscovery операций поиска. Тем не менее в некоторых случаях организации могут иметь данные, которые были случайно сохраняется в папке элементов для восстановления, их необходимо удалить. К примеру пользователь может непреднамеренно отправить или пересылать сообщения электронной почты, который содержит конфиденциальные сведения или сведения, которые могут иметь business серьезные последствия. Даже в том случае, если сообщение будет удалено без возможности восстановления, его может храниться неограниченное время так как удержания по юридическим причинам было помещено в почтовый ящик. Этот сценарий называется spillage данных, так как данные были случайно распределяются в Office 365. В таких случаях можно удалить элементы в папке элементов для восстановления пользователя почтовый ящик Exchange Online даже в том случае, если этот почтовый ящик ставится на удержание с одним из разных удержания функции в Office 365. Эти типы удержаний включают Судебное удержание, удержание на месте, удержание электронных данных и политики хранения Office 365, созданные в Office 365 безопасность &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="356a1-p102">The Recoverable Items folder for an Exchange Online mailbox exists to protect from accidental or malicious deletions. It's also used to store items that are retained and accessed by Office 365 compliance features, such as holds and eDiscovery searches. However, in some situations organizations might have data that's been unintentionally retained in the Recoverable Items folder that they must delete. For example, a user might unknowingly send or forward an email message that contains sensitive information or information that may have serious business consequences. Even if the message is permanently deleted, it might be retained indefinitely because a legal hold has been placed on the mailbox. This scenario is known as data spillage because data has been unintentionally spilled into Office 365. In these situations, you can delete items in a user's Recoverable Items folder for an Exchange Online mailbox, even if that mailbox is placed on hold with one of the different hold features in Office 365. These types of holds include Litigation Holds, In-Place Holds, eDiscovery holds, and Office 365 retention policies created in the Office 365 Security &amp; Compliance Center.</span></span> 
  
 <span data-ttu-id="356a1-p103">В этой статье объясняется, как удалить элементы из папки элементов для восстановления для облачные почтовые ящики, которые находятся на удержании. Эта процедура состоит из отключение доступа к почтовому ящику и отключить функцию восстановления отдельных элементов, отключение помощника для управляемых папок из обработки почтового ящика, временное удаление удержания, удаление элементов из папки элементов для восстановления и затем возврат почтовый ящик, чтобы его предыдущую конфигурацию. Вот как это делается:</span><span class="sxs-lookup"><span data-stu-id="356a1-p103">This article explains how to delete items from the Recoverable Items folder for cloud-based mailboxes that are on hold. This procedure involves disabling access to the mailbox and disabling single item recovery, disabling the Managed Folder Assistant from processing the mailbox, temporarily removing the hold, deleting items from the Recoverable Items folder, and then reverting the mailbox to its previous configuration. Here's the process:</span></span> 
  
[<span data-ttu-id="356a1-116">Этап 1: Сбор информации о почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="356a1-116">Step 1: Collect information about the mailbox</span></span>](#step-1-collect-information-about-the-mailbox)

[<span data-ttu-id="356a1-117">Шаг 2: Подготовка почтового ящика</span><span class="sxs-lookup"><span data-stu-id="356a1-117">Step 2: Prepare the mailbox</span></span>](#step-2-prepare-the-mailbox)

[<span data-ttu-id="356a1-118">Шаг 3: Удаление всех удержаний из почтового ящика</span><span class="sxs-lookup"><span data-stu-id="356a1-118">Step 3: Remove all holds from the mailbox</span></span>](#step-3-remove-all-holds-from-the-mailbox)

[<span data-ttu-id="356a1-119">Шаг 4: Снимать хранение задержки из почтового ящика</span><span class="sxs-lookup"><span data-stu-id="356a1-119">Step 4: Remove the delay hold from the mailbox</span></span>](#step-4-remove-the-delay-hold-from-the-mailbox)

[<span data-ttu-id="356a1-120">Шаг 5: Удаление элементов в папке элементов для восстановления</span><span class="sxs-lookup"><span data-stu-id="356a1-120">Step 5: Delete items in the Recoverable Items folder</span></span>](#step-5-delete-items-in-the-recoverable-items-folder)

[<span data-ttu-id="356a1-121">Шаг 6: Возврат в предыдущее состояние почтового ящика</span><span class="sxs-lookup"><span data-stu-id="356a1-121">Step 6: Revert the mailbox to its previous state</span></span>](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> <span data-ttu-id="356a1-p104">Процедуры, приведенные в этой статье приведет к данных, окончательно удалены (очистка) из почтовый ящик Exchange Online. Это означает, что сообщения, удалите из папки элементов для восстановления нельзя восстановить и не будут доступны для законодательной проверки или других целях соответствия требованиям. Если вы хотите удалить сообщения из почтового ящика, помещенные на удержание как часть Судебное удержание, хранение на месте, удержание электронных данных или политики хранения Office 365, созданные в Office 365 безопасность &amp; центре соответствия требованиям, проверка с помощью управления записями или legal отделы перед удалением удержания. Ваша организация может иметь политики, которая определяет, будет ли почтовый ящик на хранение или приоритет запроса технической spillage данных.</span><span class="sxs-lookup"><span data-stu-id="356a1-p104">The procedures outlined in this article will result in data being permanently deleted (purged) from an Exchange Online mailbox. That means messages that you delete from the Recoverable Items folder can't be recovered and won't be available for legal discovery or other compliance purposes. If you want to delete messages from a mailbox that's placed on hold as part of a Litigation Hold, In-Place Hold, eDiscovery hold, or Office 365 retention policy created in the Office 365 Security &amp; Compliance Center, check with your records management or legal departments before removing the hold. Your organization might have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="356a1-126">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="356a1-126">Before you begin</span></span>

- <span data-ttu-id="356a1-127">Необходимо назначить обе следующие роли управления в Exchange Online для поиска и удаления сообщений из папки восстанавливаемых элементов на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="356a1-127">You have to be assigned both of the following management roles in Exchange Online to search for and delete messages from the Recoverable Items folder in Step 5.</span></span>
    
  - <span data-ttu-id="356a1-p105">**Поиск в почтовых ящиках** — эта роль позволяет выполнять поиск почтовых ящиков в организации. Администраторы Exchange не назначается эта роль по умолчанию. Чтобы назначить себя эта роль, добавьте себя в качестве должна быть членом группы ролей управления обнаружения в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="356a1-p105">**Mailbox Search** - This role lets you to search mailboxes in your organization. Exchange administrators aren't assigned this role by default. To assign yourself this role, add yourself as a member of the Discovery Management role group in Exchange Online.</span></span> 
    
  - <span data-ttu-id="356a1-p106">**Импорт и экспорт почтового ящика** — эта роль позволяет удалить сообщения из почтового ящика пользователя. По умолчанию эта роль не будет назначен группе ролей. Для удаления сообщений из почтовых ящиков пользователей, можно добавить роли почтового ящика Импорт и экспорт в группу ролей управления организацией в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="356a1-p106">**Mailbox Import Export** - This role lets you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> 
    
- <span data-ttu-id="356a1-p107">Процедуры, описанные в этой статье не поддерживается для неактивные почтовые ящики. Который является, поскольку не может повторно применить удержания (или политики хранения Office 365) для неактивного почтового ящика после его удаления. При удалении удержания из неактивного почтового ящика изменено на обычных почтовых ящиков, удаленные и будут окончательно удалены из вашей организации после обработки помощником для управляемых папок.</span><span class="sxs-lookup"><span data-stu-id="356a1-p107">The procedure described in this article isn't supported for inactive mailboxes. That's because you can't re-apply a hold (or Office 365 retention policy) to an inactive mailbox after you remove it. When you remove a hold from an inactive mailbox, it's changed to a normal soft-deleted mailbox and will be permanently deleted from your organization after it's processed by the Managed Folder Assistant.</span></span>
    
- <span data-ttu-id="356a1-p108">Невозможно выполнить эту процедуру для почтового ящика, которому назначена политика хранения Office 365, заблокирован с хранением блокировки. Это, поскольку сохранение блокировки не позволяет удалять или исключение почтового ящика из политики хранения Office 365 и отключение помощника для управляемых папок для почтового ящика. Дополнительные сведения о блокировке политики хранения в разделе [Блокировка политику хранения](retention-policies.md#locking-a-retention-policy).</span><span class="sxs-lookup"><span data-stu-id="356a1-p108">You can't perform this procedure for a mailbox that has been assigned to an Office 365 retention policy that's been locked with a Preservation Lock. That's because a Preservation Lock prevents you from removing or excluding the mailbox from the Office 365 retention policy and from disabling the Managed Folder Assistant on the mailbox. For more information about locking retention policies, see [Locking a retention policy](retention-policies.md#locking-a-retention-policy).</span></span>
    
- <span data-ttu-id="356a1-p109">Если почтовый ящик не помещенных на удержание (или не включена функция восстановления отдельных элементов), можно просто удалить элементы из папки элементов для восстановления. Дополнительные сведения содержатся в разделе [Поиск и удаление сообщений ](https://go.microsoft.com/fwlink/?linkid=852453).</span><span class="sxs-lookup"><span data-stu-id="356a1-p109">If a mailbox isn't placed on hold (or doesn't have single item recovery enabled), you can simply delete the items from the Recoverable Items folder. For more information about how to do this, see [Search for and delete messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span></span>
  
## <a name="step-1-collect-information-about-the-mailbox"></a><span data-ttu-id="356a1-142">Этап 1: Сбор информации о почтовом ящике</span><span class="sxs-lookup"><span data-stu-id="356a1-142">Step 1: Collect information about the mailbox</span></span>

<span data-ttu-id="356a1-p110">Это первый шаг состоит в сборе выбранных свойств из целевого почтового ящика, которые будут влиять на эту процедуру. Обязательно запишите эти параметры или сохранять их в текстовый файл, так как вы будете изменить некоторые из этих свойств и восстановить исходные значения на шаге 6, пока не будет удален из папки элементов для восстановления элементов. Ниже приведен список свойств почтового ящика, которые необходимо собрать.</span><span class="sxs-lookup"><span data-stu-id="356a1-p110">This first step is to collect selected properties from the target mailbox that will affect this procedure. Be sure to write down these settings or save them to a text file because you'll change some of these properties and then revert back to the original values in Step 6, after you delete items from the Recoverable Items folder. Here's a list of the mailbox properties you need to collect.</span></span>
  
-  <span data-ttu-id="356a1-146">*SingleItemRecoveryEnabled* и *RetainDeletedItemsFor* ; При необходимости можно отключить функцию восстановления одного и увеличить срок хранения удаленных элементов в шаге 3.</span><span class="sxs-lookup"><span data-stu-id="356a1-146">*SingleItemRecoveryEnabled*  and  *RetainDeletedItemsFor*  ; if necessary, you'll disable single recovery and increase the deleted items retention period in Step 3.</span></span> 
    
-  <span data-ttu-id="356a1-p111">*LitigationHoldEnabled* и *InPlaceHolds* ; необходимо определить всех удержаний, помещенные на почтовый ящик, чтобы временно удалить на шаге 3. Советы по идентификации удержания тип, который может располагаться на почтовый ящик в разделе [Дополнительные сведения](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) .</span><span class="sxs-lookup"><span data-stu-id="356a1-p111">*LitigationHoldEnabled*  and  *InPlaceHolds*  ; you need to identify all the holds placed on the mailbox so that you can temporarily remove them in Step 3. See the [More information](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
    
<span data-ttu-id="356a1-p112">Кроме того необходимо для получения параметров клиентского доступа почтового ящика, поэтому можно временно отключить их, владелец (или другим пользователям) во время этой процедуры нельзя доступ к почтовому ящику. И, наконец можно получить текущего размера и числа элементов в папке элементов для восстановления. После удаления элементов в папке элементов для восстановления в шаге 5, будет использовать эти сведения для убедитесь, что элементы были фактически удалены.</span><span class="sxs-lookup"><span data-stu-id="356a1-p112">Additionally, you need to get the mailbox client access settings so you can temporarily disable them so the owner (or other users) can't access the mailbox during this procedure. Finally, you can get the current size and number of items in the Recoverable Items folder. After you delete items in the Recoverable Items folder in Step 5, you'll use this information to verify that items were actually removed.</span></span>
  
1. <span data-ttu-id="356a1-p113">[Подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Необходимо использовать имя пользователя и пароль для учетной записи администратора, назначенную роли соответствующие управления в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="356a1-p113">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Be sure to use a user name and password for an administrator account that's been assigned the appropriate management roles in Exchange Online.</span></span> 
    
2. <span data-ttu-id="356a1-154">Выполните следующую команду для получения сведений о функцию восстановления отдельных элементов и срока хранения удаленного элемента.</span><span class="sxs-lookup"><span data-stu-id="356a1-154">Run the following command to get information about single item recovery and the deleted item retention period.</span></span>

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   <span data-ttu-id="356a1-p114">Если включить функцию восстановления отдельных элементов, вам придется отключить его в шаге 2. Если срок хранения удаленного элемента не задано в течение 30 дней (максимальное значение в Exchange Online), а затем может быть выше в шаге 2.</span><span class="sxs-lookup"><span data-stu-id="356a1-p114">If single item recovery is enabled, you'll have to disable it in Step 2. If the deleted item retention period isn't set for 30 days (the maximum value in Exchange Online), then you can increase it in Step 2.</span></span> 
    
3. <span data-ttu-id="356a1-157">Выполните следующую команду, чтобы получить параметры доступа для почтового ящика в почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="356a1-157">Run the following command to get the mailbox access settings for the mailbox.</span></span> 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   <span data-ttu-id="356a1-158">Будет отключить все эти методы доступа на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="356a1-158">You'll disable all of these access methods in Step 2.</span></span>
    
4. <span data-ttu-id="356a1-159">Выполните следующую команду для получения сведений об удержаниях и политик хранения Office 365, применяемых к почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="356a1-159">Run the following command to get information about the holds and Office 365 retention policies applied to the mailbox.</span></span>
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > <span data-ttu-id="356a1-160">Если в свойстве *InPlaceHolds* слишком много значений, и не все из них отображаются, можно выполнить `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` команду, чтобы отобразить каждое значение в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="356a1-160">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
5. <span data-ttu-id="356a1-161">Выполните следующую команду для получения сведений о любые политики хранения всей организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="356a1-161">Run the following command to get information about any organization-wide Office 365 retention policies.</span></span> 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   <span data-ttu-id="356a1-162">Если в организации имеются какие-либо политики хранения всей организации Office 365, необходимо исключить почтового ящика из этих политик на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="356a1-162">If your organization has any organization-wide Office 365 retention policies, you'll have to exclude the mailbox from these policies in Step 3.</span></span>

   > [!TIP]
    > <span data-ttu-id="356a1-163">Если в свойстве *InPlaceHolds* слишком много значений, и не все из них отображаются, можно выполнить `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` команду, чтобы отобразить каждое значение в отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="356a1-163">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
6. <span data-ttu-id="356a1-164">Выполните следующую команду для получения текущего размера и общее число элементов в папках и вложенных папок в папке элементов для восстановления в основной почтовый ящик пользователя.</span><span class="sxs-lookup"><span data-stu-id="356a1-164">Run the following command to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="356a1-165">Если включена архивный почтовый ящик пользователя, выполните следующую команду, чтобы получить размер и общее число элементов в папках и вложенных папок в папке папки в почтовом ящике архива.</span><span class="sxs-lookup"><span data-stu-id="356a1-165">If the user's archive mailbox is enabled, run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in their archive mailbox.</span></span> 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="356a1-p115">При удалении элементов на шаге 5, вы можете удалить или не удалять элементы в папке элементов для восстановления в основной архивного почтового ящика пользователя. Обратите внимание, что если для почтового ящика включена развертываемым архивации, элементы дополнительный архивного почтового ящика не будут удалены.</span><span class="sxs-lookup"><span data-stu-id="356a1-p115">When you delete items in Step 5, you can choose to delete or not delete items in the Recoverable Items folder in the user's primary archive mailbox. Note that if auto-expanding archiving is enabled for the mailbox, items in an auxiliary archive mailbox won't be deleted.</span></span>
  
## <a name="step-2-prepare-the-mailbox"></a><span data-ttu-id="356a1-168">Шаг 2: Подготовка почтового ящика</span><span class="sxs-lookup"><span data-stu-id="356a1-168">Step 2: Prepare the mailbox</span></span>

<span data-ttu-id="356a1-169">После сбора и сохранения сведений о почтовом ящике, следующий шаг состоит в подготовке почтового ящика, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="356a1-169">After collecting and saving information about the mailbox, the next step is to prepare the mailbox by performing the following tasks:</span></span> 
  
- <span data-ttu-id="356a1-170">**Отключение клиентского доступа к почтовому ящику** , чтобы владелец почтового ящика не может получить доступ к своему почтовому ящику и вносите никаких изменений в данных почтовых ящиков во время этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="356a1-170">**Disable client access to mailbox** so that the mailbox owner can't access their mailbox and make any changes to the mailbox data during this procedure.</span></span> 
    
- <span data-ttu-id="356a1-171">**Увеличить срок хранения удаленного элемента** до 30 дней (максимальное значение в Exchange Online), чтобы элементы не очищены из папки элементов для восстановления, прежде чем удалять их на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="356a1-171">**Increase the deleted item retention period** to 30 days (the maximum value in Exchange Online) so that items aren't purged from the Recoverable Items folder before you can delete them in Step 5.</span></span> 
    
- <span data-ttu-id="356a1-172">**Отключение восстановления одного элемента** , так что товаров не должны сохраняться (Длительность срока хранения удаленного элемента) пока не будет удален из папки восстанавливаемых элементов на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="356a1-172">**Disable single Item recovery** so that items won't be retained (for the duration of the deleted item retention period) after you delete them from the Recoverable Items folder in Step 5.</span></span> 
    
- <span data-ttu-id="356a1-173">**Отключение помощника для управляемых папок** , чтобы она не обработки почтового ящика и сохранение элементов, которые удаляют на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="356a1-173">**Disable the Managed Folder Assistant** so that it doesn't process the mailbox and retain the items that you delete in Step 5.</span></span> 
    
<span data-ttu-id="356a1-174">В Exchange Online PowerShell выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="356a1-174">Perform the following steps in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="356a1-p116">Выполните следующую команду, чтобы отключить все клиентского доступа к почтовому ящику. Синтаксис команды предполагается, что все методы доступа клиента были включены в почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="356a1-p116">Run the following command to disable all client access to the mailbox. The command syntax assumes that all client access methods were enabled on the mailbox.</span></span>

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > <span data-ttu-id="356a1-p117">Выполнение может занять до 60 минут, чтобы отключить все методы клиентского доступа к почтовому ящику. Обратите внимание на то, что отключение эти методы доступа к не будет отключаться владельца почтового ящика, которые в настоящее время входа в. Если владелец не будет выполнен, они будут иметь доступ к своему почтовому ящику после отключения эти методы доступа.</span><span class="sxs-lookup"><span data-stu-id="356a1-p117">It might take up to 60 minutes to disable all client access methods to the mailbox. Note that disabling these access methods won't disconnect the mailbox owner they're currently signed in. If the owner isn't signed in, then they won't be able to access their mailbox after these access methods are disabled.</span></span> 
  
2. <span data-ttu-id="356a1-p118">Выполните следующую команду, чтобы увеличить срок хранения удаленного элемента более 30 дней. Это предполагает, что текущее значение меньше, чем 30 дней.</span><span class="sxs-lookup"><span data-stu-id="356a1-p118">Run the following command to increase the deleted item retention period the maximum of 30 days. This assumes that the current setting is less than 30 days.</span></span> 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. <span data-ttu-id="356a1-182">Выполните следующую команду, чтобы отключить функцию восстановления отдельных элементов.</span><span class="sxs-lookup"><span data-stu-id="356a1-182">Run the following command to disable single item recovery.</span></span>
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > <span data-ttu-id="356a1-p119">Выполнение может занять более 60 минут, чтобы отключить функцию восстановления отдельных элементов. Не удаляйте элементов в папке элементов для восстановления, пока не истечет этого периода.</span><span class="sxs-lookup"><span data-stu-id="356a1-p119">It might take up to 60 minutes to disable single item recovery. Don't delete items in the Recoverable Items folder until this period has elapsed.</span></span> 
  
4. <span data-ttu-id="356a1-p120">Выполните следующую команду, чтобы предотвратить помощника для управляемых папок обработки почтового ящика. Как объяснялось ранее можно отключить помощника для управляемых папок только в том случае, если политика хранения Office 365 с хранением блокировки не применяются к почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="356a1-p120">Run the following command to prevent the Managed Folder Assistant from processing the mailbox. As previously explained, you can disable the Managed Folder Assistant only if an Office 365 retention policy with a Preservation Lock is not applied to the mailbox.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a><span data-ttu-id="356a1-187">Шаг 3: Удаление всех удержаний из почтового ящика</span><span class="sxs-lookup"><span data-stu-id="356a1-187">Step 3: Remove all holds from the mailbox</span></span>

<span data-ttu-id="356a1-p121">— Это последний этап, прежде чем удалять элементы из папки элементов для восстановления для удаления всех удержаний (, определенного на шаге 1) на почтовый ящик. Чтобы элементы не могут быть сохранены, пока не будет удален из папки элементов для восстановления, необходимо удалить всех удержаний. В следующих разделах содержатся сведения об удалении различных типов удержаний для почтового ящика. Советы по идентификации удержания тип, который может располагаться на почтовый ящик в разделе [Дополнительные сведения](#more-information) . Для получения дополнительных сведений см. [как определить тип удержания помещенных на почтовый ящик Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="356a1-p121">The last step before you can delete items from the Recoverable Items folder is to remove all holds (that you identified in Step 1) placed on the mailbox. All holds must be removed so that items won't be retained after you delete them from the Recoverable Items folder. The following sections contain information about removing different types of holds on a mailbox. See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox. For additional information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="356a1-193">Как было сказано ранее обратитесь к управлению записями или юридических отделов перед удалением удержания из почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="356a1-193">As previously stated, check with your records management or legal departments before removing a hold from a mailbox.</span></span> 
  
 ### <a name="litigation-hold"></a><span data-ttu-id="356a1-194">Хранение для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="356a1-194">Litigation Hold</span></span>
  
<span data-ttu-id="356a1-195">Выполните следующую команду в Exchange Online PowerShell для удаления хранение для судебного разбирательства из почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="356a1-195">Run the following command in Exchange Online PowerShell to remove a Litigation Hold from the mailbox.</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> <span data-ttu-id="356a1-p122">Как и отключение методы доступа клиентов и восстановления отдельных элементов, он может занять до 60 минут для удаления хранение для судебного разбирательства. Не удалять элементы из папки элементов для восстановления, до истечения этого периода.</span><span class="sxs-lookup"><span data-stu-id="356a1-p122">Similar to disabling the client access methods and single item recovery, it might take up to 60 minutes to remove the Litigation Hold. Don't delete items from the Recoverable Items folder until this period has elapsed.</span></span> 
  
 ### <a name="in-place-hold"></a><span data-ttu-id="356a1-198">Хранение на месте</span><span class="sxs-lookup"><span data-stu-id="356a1-198">In-Place Hold</span></span>
  
<span data-ttu-id="356a1-p123">Выполните следующую команду в Exchange Online PowerShell для идентификации хранение на месте, которое размещается на почтовый ящик. Используйте идентификатор GUID для хранения на месте, который был определен на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="356a1-p123">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's placed on the mailbox. Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
<span data-ttu-id="356a1-p124">После определения хранение на месте, можно использовать Центр администрирования Exchange (EAC) или Exchange Online PowerShell для удаления почтового ящика из удержания. Для получения дополнительных сведений см. [Создание и удаление хранение на месте](https://go.microsoft.com/fwlink/?linkid=852668).</span><span class="sxs-lookup"><span data-stu-id="356a1-p124">After you identify the In-Place Hold, you can use the Exchange admin center (EAC) or Exchange Online PowerShell to remove the mailbox from the hold. For more information, see [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span></span>
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a><span data-ttu-id="356a1-203">Office 365 хранения политик, применяемых к определенным почтовым ящикам</span><span class="sxs-lookup"><span data-stu-id="356a1-203">Office 365 retention policies applied to specific mailboxes</span></span>
  
<span data-ttu-id="356a1-p125">Выполните следующую команду [безопасности Office 365 &amp; PowerShell центр соответствия](https://go.microsoft.com/fwlink/?linkid=627084) определить политику хранения Office 365, которая применяется к почтовому ящику. Используйте идентификатор GUID (без учета `mbx` или `skp` префикс) для политики хранения, который был определен на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="356a1-p125">Run the following command in [Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the Office 365 retention policy that is applied to the mailbox. Use the GUID (not including the  `mbx` or  `skp` prefix) for the retention policy that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
<span data-ttu-id="356a1-206">После определения политики хранения, перейдите к **дате управления** \> **хранения** страницы в системы &amp; центре соответствия требованиям, изменить политику хранения, который был определен на предыдущем шаге и удалить почтовый ящик из списка получателей, включенных в политику хранения.</span><span class="sxs-lookup"><span data-stu-id="356a1-206">After you identify the retention policy, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy that you identified in the previous step, and remove the mailbox from the list of recipients that are included in the retention policy.</span></span> 
  
 ### <a name="organization-wide-office-365-retention-policies"></a><span data-ttu-id="356a1-207">Политики хранения всей организации Office 365</span><span class="sxs-lookup"><span data-stu-id="356a1-207">Organization-wide Office 365 retention policies</span></span>
  
<span data-ttu-id="356a1-p126">Всей организации и политики хранения Exchange всей Office 365, применяются для всех почтовых ящиков в организации. Они применяются на уровне организации (не на уровне почтового ящика) и возвращаются при запуске командлета **Get-OrganizationConfig** на шаге 1. Выполните следующую команду [безопасности &amp; PowerShell центр соответствия](https://go.microsoft.com/fwlink/?linkid=627084) для определения политик хранения всей организации Office 365. Используйте идентификатор GUID (без учета `mbx` префикс) для политики хранения всей организации, определенного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="356a1-p126">Organization-wide and Exchange-wide Office 365 retention policies are applied to every mailbox in the organization. They are applied at the organization level (not the mailbox level) and are returned when you run the **Get-OrganizationConfig** cmdlet in Step 1. Run the following command in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the organization-wide Office 365 retention policies. Use the GUID (not including the  `mbx` prefix) for the organization-wide retention policies that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

<span data-ttu-id="356a1-p127">После определения политик хранения всей организации Office 365 перейдите к **дате управления** \> **хранения** страницы в системы &amp; центре соответствия требованиям, изменение каждой политики хранения всей организации, который был определен предыдущий шаг и добавьте почтовый ящик в список исключенных получателей. Это приведет к удалению из политики хранения почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="356a1-p127">After you identify the organization-wide Office 365 retention policies, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit each organization-wide retention policy that you identified in the previous step, and add the mailbox to the list of excluded recipients. Doing this will remove the user's mailbox from the retention policy.</span></span> 

### <a name="office-365-retention-labels"></a><span data-ttu-id="356a1-214">Office 365 хранения меток</span><span class="sxs-lookup"><span data-stu-id="356a1-214">Office 365 retention labels</span></span>

<span data-ttu-id="356a1-p128">Каждый раз, когда пользователь применяет метки, который настроен на сохранение контента или сохранить, а затем удалите содержимое в любую папку или элемент в свой почтовый ящик, свойства почтового ящика *ComplianceTagHoldApplied* имеет значение **True**. В этом случае считается, что почтовый ящик будет отложен, как если он был помещенные на хранение для судебного разбирательства или назначенные политики хранения к Office 365.</span><span class="sxs-lookup"><span data-stu-id="356a1-p128">Whenever a user applies a label that's configured to retain content or retain and then delete content to any folder or item in their mailbox, the *ComplianceTagHoldApplied* mailbox property is set to **True**. When this happens, the mailbox is considered to be on hold, just as if it was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span>

<span data-ttu-id="356a1-217">Чтобы просмотреть значение свойства *ComplianceTagHoldApplied* , выполните следующую команду в Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="356a1-217">To view the value of the *ComplianceTagHoldApplied* property, run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

<span data-ttu-id="356a1-p129">Определив почтового ящика такое удержание, так как метка хранения применяется к папке или элемента, можно использовать средство поиска контента в центре соответствия требованиям & безопасности для поиска помеченных элементов с помощью условия поиска ComplianceTag. Для получения дополнительных сведений обратитесь к разделу «Условия поиска» в [запросах по ключевым словам и условия поиска для поиска контента](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span><span class="sxs-lookup"><span data-stu-id="356a1-p129">After you've identified that a mailbox is on hold because a retention label is applied to a folder or item, you can use the Content Search tool in the Security & Compliance Center to search for labeled items by using the ComplianceTag search condition. For more information, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span></span>

<span data-ttu-id="356a1-220">Дополнительные сведения о подписи можно [меток Обзор Office 365](labels.md).</span><span class="sxs-lookup"><span data-stu-id="356a1-220">For more information about labels, see [Overview of Office 365 labels](labels.md).</span></span>

 ### <a name="ediscovery-case-holds"></a><span data-ttu-id="356a1-221">содержит случая обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="356a1-221">eDiscovery case holds</span></span>
  
<span data-ttu-id="356a1-p130">Выполните следующие команды [безопасности &amp; PowerShell центр соответствия](https://go.microsoft.com/fwlink/?linkid=627084) для идентификации удержания, связанные с вариантом eDiscovery, которая применяется к почтовому ящику. Используйте идентификатор GUID (без учета `UniH` префикс) для обнаружения электронных данных удержания, определенным в шаге 1. Обратите внимание на то, что вторая команда отображает имя случая обнаружения электронных данных удержания с которым связан; Третья команда отображает имя удержания.</span><span class="sxs-lookup"><span data-stu-id="356a1-p130">Run the following commands in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the hold associated with an eDiscovery case that's applied to the mailbox. Use the GUID (not including the  `UniH` prefix) for the eDiscovery hold that you identified in Step 1. Note that the second command displays the name of the eDiscovery case the hold is associated with; the third command displays the name of the hold.</span></span> 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

<span data-ttu-id="356a1-p131">Определив имя случая обнаружения электронных данных и удержания, перейдите к **поиска &amp; расследования** \> страницы **обнаружения электронных данных** в системы &amp; центре соответствия требованиям, откройте регистр и удалить почтовый ящик из удержания. Дополнительные сведения можно [Управление вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям](manage-ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="356a1-p131">After you've identified the name of the eDiscovery case and the hold, go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and remove the mailbox from the hold. For more information, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md).</span></span>
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a><span data-ttu-id="356a1-227">Шаг 4: Снимать хранение задержки из почтового ящика</span><span class="sxs-lookup"><span data-stu-id="356a1-227">Step 4: Remove the delay hold from the mailbox</span></span>

<span data-ttu-id="356a1-p132">После любого типа удержания из почтового ящика, значение свойства почтового ящика *DelayHoldApplied* имеет значение **True**. Это возникает всякий раз помощника для управляемых папок обрабатывается почтовый ящик и обнаруживает, что удержания был удален. Это называется *Задержка удержания* и означает, что фактическое удаление удержания задерживается 30-дневная для предотвращения распространения данных за окончательно удаляется из почтового ящика. (Задержка удержания предназначен для предоставления возможности поиска или восстановить элементы почтовых ящиков, которые будут очищены после удаления удержания "Администраторы".)  Когда удержания задержки располагается на почтовый ящик, почтовый ящик по-прежнему считается при удержании в течение неограниченного периода времени, как было ли почтовый ящик на хранение для судебного разбирательства. Через 30 дней после истечения срока действия delay удержания и Office 365 автоматически попытаться удалить удержание delay (путем установки свойства *DelayHoldApplied* значение **False**), чтобы фактически будет снято удержание.</span><span class="sxs-lookup"><span data-stu-id="356a1-p132">After any type of hold is removed from a mailbox, the value of the *DelayHoldApplied* mailbox property is set to **True**. This occurs the next time the Managed Folder Assistant processes the mailbox and detects that a hold has been removed. This is called a *delay hold* and means the actual removal of the hold is delayed for 30 days to prevent data from being permanently deleted from the mailbox. (The purpose of a delay hold is to give admins an opportunity to search for or recover mailbox items that will be purged after a hold is removed.)  When a delay hold is placed on the mailbox, the mailbox is still considered to be on hold for an unlimited duration, as if the mailbox was on Litigation Hold. After 30 days, the delay hold expires, and Office 365 will automatically attempt to remove the delay hold (by setting the *DelayHoldApplied* property to **False**) so that the hold is actually removed.</span></span> 

<span data-ttu-id="356a1-p133">Прежде чем удалить элементы в шаге 5, необходимо удалить удержание задержки из почтового ящика. Во-первых определите, если задержка удержания будет применяться к почтовому ящику, выполнив следующую команду в Exchange Online PowerShell:</span><span class="sxs-lookup"><span data-stu-id="356a1-p133">Before you can delete items in Step 5, you have to remove the delay hold from the mailbox. First, determine if the delay hold is applied to the mailbox by running the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> | FL DelayHoldApplied
```

<span data-ttu-id="356a1-p134">Если значение свойства *DelayHoldApplied* задано значение **False**, удержание задержка не был включен в почтовом ящике. Можно перейти к шагу 5 и удаление элементов в папке элементов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="356a1-p134">If the value of the *DelayHoldApplied* property is set to **False**, a delay hold has not been placed on the mailbox. You can go to Step 5 and delete items in the Recoverable Items folder.</span></span>

<span data-ttu-id="356a1-237">Если значение свойства *DelayHoldApplied* задано значение **True**, выполните следующую команду, чтобы удалить удержание задержки.</span><span class="sxs-lookup"><span data-stu-id="356a1-237">If the value of the *DelayHoldApplied* property is set to **True**, run the following command to remove the delay hold:</span></span>

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
<span data-ttu-id="356a1-238">Обратите внимание на то, что вам должна быть назначена роль юридическое удержание в Exchange Online для использования параметра *RemoveDelayHoldApplied* .</span><span class="sxs-lookup"><span data-stu-id="356a1-238">Note that you must be assigned the Legal Hold role in Exchange Online to use the *RemoveDelayHoldApplied* parameter.</span></span>

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a><span data-ttu-id="356a1-239">Шаг 5: Удаление элементов в папке элементов для восстановления</span><span class="sxs-lookup"><span data-stu-id="356a1-239">Step 5: Delete items in the Recoverable Items folder</span></span>

<span data-ttu-id="356a1-p135">Теперь вы готовы к фактически удаление элементов в папке элементов для восстановления с помощью командлета [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) в Exchange Online PowerShell. У вас есть три варианта при запуске командлета **Search-Mailbox** .</span><span class="sxs-lookup"><span data-stu-id="356a1-p135">Now you're ready to actually delete items in the Recoverable Items folder by using the [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet in Exchange Online PowerShell. You have three options when running the **Search-Mailbox** cmdlet.</span></span> 
  
- <span data-ttu-id="356a1-242">Копирование элементов в целевой почтовый ящик, прежде чем удалять их, в котором можно просмотреть элементы, при необходимости, прежде чем удалять их.</span><span class="sxs-lookup"><span data-stu-id="356a1-242">Copy items to a target mailbox before you delete them so that you can review the items, if necessary, before you delete them.</span></span>
    
- <span data-ttu-id="356a1-243">Копирование элементов в целевой почтовый ящик и удалите их в одной команде.</span><span class="sxs-lookup"><span data-stu-id="356a1-243">Copy items to a target mailbox and delete them in the same command.</span></span>
    
- <span data-ttu-id="356a1-244">Удаление элементов без копирования их в целевой почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="356a1-244">Delete items without copying them to a target mailbox.</span></span> 
    
<span data-ttu-id="356a1-p136">Обратите внимание на то, что элементов в папке элементов для восстановления в основной архивного почтового ящика пользователя также будут удалены при запуске командлета **Search-Mailbox** . Чтобы предотвратить это, можно указывать параметр *DoNotIncludeArchive* . Как было сказано ранее, если развертываемым архивации включенном для почтового ящика и \*\* Search-Mailbox \*\* командлет не удаленные элементы в дополнительный архивного почтового ящика. Дополнительные сведения о развертываемым архивацию, просматривать [Общие сведения о неограниченном архивировании в Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="356a1-p136">Note that items in the Recoverable Items folder in the user's primary archive mailbox will also be deleted when you run the **Search-Mailbox** cmdlet. To prevent this, you can include the  *DoNotIncludeArchive*  switch. And as previously stated, if auto-expanding archiving is enabled for the mailbox, the \*\* Search-Mailbox \*\* cmdlet doesn't deleted items in an auxiliary archive mailbox. For more information about auto-expanding archive, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="356a1-p137">Если вы включите поисковый запрос (используя параметр  *SearchQuery*  ), командлет **Search-Mailbox** вернет максимум 10 000 элементов. Поэтому, чтобы удалить более 10 000 элементов, может потребоваться выполнить команду **Search-Mailbox** несколько раз.</span><span class="sxs-lookup"><span data-stu-id="356a1-p137">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
  
<span data-ttu-id="356a1-p138">В следующих примерах показано синтаксис команды для каждого из этих параметров. Используйте эти примеры, `-SearchQuery size>0` значение параметра, который удаляет все элементы из всех вложенных папок в папке элементов для восстановления. Если требуется удалить только элементы, которые соответствуют определенным условиям, можно также использовать параметр *SearchQuery* для указания других условий, такие как темы сообщения или диапазон дат. Просмотрите [другие примеры использования параметр SearchQuery](#other-examples-of-using-the-searchquery-parameter) ниже.</span><span class="sxs-lookup"><span data-stu-id="356a1-p138">The following examples show the command syntax for each of these options. These examples use the  `-SearchQuery size>0` parameter value, which deletes all items from all subfolders in the Recoverable Items folder. If you need to delete only items that match specific conditions, you can also use the  *SearchQuery*  parameter to specify other conditions, such as the subject of a message or a date range. See the [other examples of using the SearchQuery parameter](#other-examples-of-using-the-searchquery-parameter) below.</span></span> 
  
### <a name="example-1"></a><span data-ttu-id="356a1-255">Пример 1</span><span class="sxs-lookup"><span data-stu-id="356a1-255">Example 1</span></span>

<span data-ttu-id="356a1-p139">В этом примере копирует все элементы в папки восстанавливаемых элементов папки в почтовом ящике поиска обнаружения вашей организации. Это позволяет просматривать элементы перед их удалением без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="356a1-p139">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox. This lets you review the items before you permanently delete them.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

<span data-ttu-id="356a1-p140">В предыдущем примере он не требуется для копирования элементов в почтовый ящик поиска обнаружения. Можно скопировать сообщения любой целевой почтовый ящик. Тем не менее чтобы запретить доступ к данным потенциально конфиденциальных почтовых ящиков, рекомендуется копирование сообщений в почтовый ящик, который имеет доступ только авторизованный персонал. По умолчанию доступ к поиска почтового ящика обнаружения по умолчанию ограничен членов группы ролей управления обнаружения в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="356a1-p140">In the previous example, it isn't required to copy items to the Discovery Search Mailbox. You can copy messages to any target mailbox. However, to prevent access to potentially sensitive mailbox data, we recommend copying messages to a mailbox that has access restricted to authorized personnel. By default, access to the default Discovery Search Mailbox is restricted to members of the Discovery Management role group in Exchange Online.</span></span> 
  
### <a name="example-2"></a><span data-ttu-id="356a1-262">Пример 2</span><span class="sxs-lookup"><span data-stu-id="356a1-262">Example 2</span></span>

<span data-ttu-id="356a1-263">В этом примере копирует все элементы в папки восстанавливаемых элементов папки в почтовом ящике поиска обнаружения вашей организации, а затем удаляет элементы из папки элементов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="356a1-263">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox and then deletes the items from the user's Recoverable Items folder.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a><span data-ttu-id="356a1-264">Пример 3</span><span class="sxs-lookup"><span data-stu-id="356a1-264">Example 3</span></span>

<span data-ttu-id="356a1-265">В этом примере удаляется все элементы в папке элементов для восстановления пользователя, без необходимости копирования их в целевой почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="356a1-265">This example deletes all items in the user's Recoverable Items folder, without copying them to a target mailbox.</span></span> 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a><span data-ttu-id="356a1-266">Другие примеры использования параметр SearchQuery</span><span class="sxs-lookup"><span data-stu-id="356a1-266">Other examples of using the SearchQuery parameter</span></span>

<span data-ttu-id="356a1-p141">Вот несколько примеров использования параметр *SearchQuery* для поиска конкретных сообщений. Если параметр *SearchQuery* используется для поиска конкретных элементов, рассмотрите возможность копирования результатов поиска в целевой почтовый ящик, чтобы просмотреть результаты поиска и затем измените запрос при необходимости прежде чем удалять результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="356a1-p141">Here are a few examples of using the  *SearchQuery*  parameter to find specific messages. If you use the  *SearchQuery*  parameter to search for specific items, consider copying the search results to a target mailbox so that you can review the search results and then revise the query if necessary before you delete the results of a search.</span></span> 
  
<span data-ttu-id="356a1-269">Этот пример возвращает сообщения, которые содержат определенные фразу в поле Тема.</span><span class="sxs-lookup"><span data-stu-id="356a1-269">This example returns messages that contain a specific phrase in the Subject field.</span></span>
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

<span data-ttu-id="356a1-270">В этом примере возвращаются сообщений, отправленных в рамках за указанный диапазон дат.</span><span class="sxs-lookup"><span data-stu-id="356a1-270">This example returns messages that were sent within the specified date range.</span></span>
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
<span data-ttu-id="356a1-271">Этот пример возвращает сообщения, отправленные для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="356a1-271">This example returns messages that were sent to the specified person.</span></span>

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a><span data-ttu-id="356a1-272">Убедитесь, что элементы были удалены</span><span class="sxs-lookup"><span data-stu-id="356a1-272">Verify that items were deleted</span></span>

<span data-ttu-id="356a1-p142">Чтобы убедиться, что вы успешно удаленные элементы из папки элементов для восстановления почтового ящика, командлет **Get-MailboxFolderStatistics** в Exchange Online PowerShell Проверка размера и числа элементов в папке элементов для восстановления. Позволяет сравнивать статистику файлами, собранных на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="356a1-p142">To verify that you've successfully deleted items from the Recoverable Items folder of a mailbox, use **Get-MailboxFolderStatistics** cmdlet in Exchange Online PowerShell to check the size and number of items in Recoverable Items folder. You can compare these statistics with the ones you collected in Step 1.</span></span> 
  
<span data-ttu-id="356a1-275">Выполните следующую команду для получения текущего размера и общее число элементов в папках и вложенных папок в папке элементов для восстановления в основной почтовый ящик пользователя.</span><span class="sxs-lookup"><span data-stu-id="356a1-275">Run the following command in to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
<span data-ttu-id="356a1-276">Выполните следующую команду, чтобы получить размер и общее число элементов в папках и вложенных папок в папке элементов для восстановления в архивный почтовый ящик пользователя.</span><span class="sxs-lookup"><span data-stu-id="356a1-276">Run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in the user's archive mailbox.</span></span> 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a><span data-ttu-id="356a1-277">Шаг 6: Возврат в предыдущее состояние почтового ящика</span><span class="sxs-lookup"><span data-stu-id="356a1-277">Step 6: Revert the mailbox to its previous state</span></span>

<span data-ttu-id="356a1-p143">Последний этап заключается в возврат почтовых ящиков обратно в его предыдущую конфигурацию. Это означает, что сброс свойств, которые были изменены в шаге 2 и повторного применения удержаний, которые удалены в шаге 3. В том числе:</span><span class="sxs-lookup"><span data-stu-id="356a1-p143">The final step is to revert the mailbox back to its previous configuration. This means resetting the properties that you changed in Step 2 and re-applying the holds that you removed in Step 3. This includes:</span></span>
  
- <span data-ttu-id="356a1-p144">Изменение срока хранения удаленного элемента назад к предыдущему значению. Кроме того можно просто оставить это значение 30 дней, максимальное значение в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="356a1-p144">Changing the deleted item retention period back to its previous value. Alternatively, you can just leave this set to 30 days, the maximum value in Exchange Online.</span></span>
    
- <span data-ttu-id="356a1-283">Повторное включение восстановления одного элемента.</span><span class="sxs-lookup"><span data-stu-id="356a1-283">Re-enabling single Item recovery.</span></span>
    
- <span data-ttu-id="356a1-284">Повторное включение методы доступа клиентов, чтобы владелец может получить доступ к своему почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="356a1-284">Re-enabling the client access methods so that the owner can access their mailbox.</span></span>
    
- <span data-ttu-id="356a1-285">Повторное применение удержаний и политики хранения Office 365, которые вы удалили.</span><span class="sxs-lookup"><span data-stu-id="356a1-285">Re-applying the holds and Office 365 retention policies that you removed.</span></span>
    
- <span data-ttu-id="356a1-286">Повторное включение помощника для управляемых папок для обработки почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="356a1-286">Re-enabling the Managed Folder Assistant to process the mailbox.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="356a1-287">Мы рекомендуем отложить 24 часа после повторного применения удержание или Office 365 хранения политики (и, проверка, что оно будет готова) прежде чем повторно включить помощника для управляемых папок для обработки почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="356a1-287">We recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant to process the mailbox.</span></span> 
  
<span data-ttu-id="356a1-288">Выполните следующие действия (в указанной последовательности) в Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="356a1-288">Perform the following steps (in the specified sequence) in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="356a1-p145">Выполните следующую команду, чтобы изменить срок хранения удаленного элемента резервного исходное значение. Предполагается, что предыдущий параметр — меньше, чем 30 дней. Например, 14 дней.</span><span class="sxs-lookup"><span data-stu-id="356a1-p145">Run the following command to change the deleted item retention period back to its original value. This assumes that the previous setting is less than 30 days; for example 14 days.</span></span> 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. <span data-ttu-id="356a1-291">Выполните следующую команду, чтобы включить функцию восстановления отдельных элементов.</span><span class="sxs-lookup"><span data-stu-id="356a1-291">Run the following command to re-enable single item recovery.</span></span>
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. <span data-ttu-id="356a1-292">Выполните следующую команду, чтобы повторно включить все методы клиентского доступа к почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="356a1-292">Run the following command to re-enable all client access methods to the mailbox.</span></span>
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. <span data-ttu-id="356a1-p146">Повторное применение удержаний, которые удалены в шаге 3. В зависимости от типа удержания используйте одну из следующих процедур.</span><span class="sxs-lookup"><span data-stu-id="356a1-p146">Re-apply the holds that you removed in Step 3. Depending on the type of hold, use one of the following procedures.</span></span>
    
    <span data-ttu-id="356a1-295">**Хранение для судебного разбирательства**</span><span class="sxs-lookup"><span data-stu-id="356a1-295">**Litigation Hold**</span></span>
    
    <span data-ttu-id="356a1-296">Выполните следующую команду, чтобы повторно включить хранение для судебного разбирательства для почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="356a1-296">Run the following command to re-enable a Litigation Hold for the mailbox.</span></span>
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    <span data-ttu-id="356a1-297">**In-Place Hold**</span><span class="sxs-lookup"><span data-stu-id="356a1-297">**In-Place Hold**</span></span>
    
    <span data-ttu-id="356a1-298">Использование центра администрирования Exchange (или Exchange Online PowerShell), чтобы добавить почтовый ящик обратно в режим хранения на месте.</span><span class="sxs-lookup"><span data-stu-id="356a1-298">Use the EAC (or Exchange Online PowerShell) to add the mailbox back to the In-Place Hold.</span></span> 
    
    <span data-ttu-id="356a1-299">**Office 365 хранения политик, применяемых к определенным почтовым ящикам**</span><span class="sxs-lookup"><span data-stu-id="356a1-299">**Office 365 retention policies applied to specific mailboxes**</span></span>
    
    <span data-ttu-id="356a1-p147">Использование безопасности &amp; центре соответствия требованиям, чтобы добавить почтовый ящик Office 365 политики хранения. Последовательно выберите пункты **Управление даты** \> **хранения** страницы в системы &amp; центре соответствия требованиям, изменить политику хранения и добавьте почтовый ящик в список получателей, к которым применяется политика хранения.</span><span class="sxs-lookup"><span data-stu-id="356a1-p147">Use the Security &amp; Compliance Center to add the mailbox back to the Office 365 retention policy. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy, and add the mailbox back to the list of recipients that the retention policy is applied to.</span></span> 
    
    <span data-ttu-id="356a1-302">**Политики хранения всей организации Office 365**</span><span class="sxs-lookup"><span data-stu-id="356a1-302">**Organization-wide Office 365 retention policies**</span></span>
    
    <span data-ttu-id="356a1-p148">Если вы удалили всей организации или Exchange политики хранения, исключив из политики, используйте безопасности &amp; центре соответствия требованиям, чтобы удалить почтовый ящик из списка исключенных пользователей. Последовательно выберите пункты **Управление даты** \> **хранения** страницы в системы &amp; центре соответствия требованиям, изменить политику хранения всей организации и удалить почтовый ящик из списка исключенных получателей. При этом повторно применить политику хранения для почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="356a1-p148">If you removed an organization-wide or Exchange-wide retention policy by excluding it from the policy, then use the Security &amp; Compliance Center to remove the mailbox from the list of excluded users. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the organization-wide retention policy, and remove the mailbox from the list of excluded recipients. Doing this will re-apply the retention policy to the user's mailbox.</span></span> 
    
    <span data-ttu-id="356a1-306">**содержит случая обнаружения электронных данных**</span><span class="sxs-lookup"><span data-stu-id="356a1-306">**eDiscovery case holds**</span></span>
    
    <span data-ttu-id="356a1-p149">Использование безопасности &amp; центре соответствия требованиям, чтобы добавить почтовый ящик резервного удержания, связанной с вариантом eDiscovery. Последовательно выберите пункты **поиска &amp; расследования** \> страницы **обнаружения электронных данных** в системы &amp; центре соответствия требованиям, откройте регистр и добавить почтовый ящик в удержание.</span><span class="sxs-lookup"><span data-stu-id="356a1-p149">Use the Security &amp; Compliance Center to add the mailbox back the hold that's associated with an eDiscovery case. Go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and add the mailbox back to the hold.</span></span> 
    
5. <span data-ttu-id="356a1-p150">Выполните следующую команду, чтобы разрешить помощника для управляемых папок для обработки почтового ящика еще раз. Как уже упоминалось, рекомендуется отложить 24 часа после повторного применения удержание или Office 365 хранения политики (и, проверка, что оно будет готова) прежде чем повторно включить помощника для управляемых папок.</span><span class="sxs-lookup"><span data-stu-id="356a1-p150">Run the following command to allow the Managed Folder Assistant to process the mailbox again. As previously stated, we recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. <span data-ttu-id="356a1-311">Чтобы убедиться в том, что почтовый ящик восстановлен обратно в его предыдущую конфигурацию, можно выполните следующие команды и сравните параметры тем, которые собираются на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="356a1-311">To verify that the mailbox has been reverted back to its previous configuration, you can run the following commands and then compare the settings to the ones that you collected in Step 1.</span></span>

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a><span data-ttu-id="356a1-312">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="356a1-312">More information</span></span>

<span data-ttu-id="356a1-p151">Ниже приведена таблица, в которых описывается определение различных типов удержаний на основе значений в свойстве *InPlaceHolds* при запуске командлета **Get-Mailbox** или **Get-OrganizationConfig** . Для получения дополнительных сведений см. [как определить тип удержания помещенных на почтовый ящик Exchange Online](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="356a1-p151">Here's a table that describes how to identify different types of holds based on the values in the  *InPlaceHolds*  property when you run the **Get-Mailbox** or **Get-OrganizationConfig** cmdlets. For more detailed information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

<span data-ttu-id="356a1-315">Как уже описано, необходимо удалить всех удержаний и политик хранения Office 365 из почтового ящика, прежде чем вы успешно можно удалить элементы в папке элементов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="356a1-315">As previously explained, you have to remove all holds and Office 365 retention policies from a mailbox before you can successfully delete items in the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="356a1-316">**Тип удержания**</span><span class="sxs-lookup"><span data-stu-id="356a1-316">**Hold type**</span></span>|<span data-ttu-id="356a1-317">**Пример значения**</span><span class="sxs-lookup"><span data-stu-id="356a1-317">**Example value**</span></span>|<span data-ttu-id="356a1-318">**Как определить удержания**</span><span class="sxs-lookup"><span data-stu-id="356a1-318">**How to identify the hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="356a1-319">Хранение для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="356a1-319">Litigation Hold</span></span>  <br/> | `True` <br/> |<span data-ttu-id="356a1-320">Свойство  *LitigationHoldEnabled*  имеет значение  `True`.</span><span class="sxs-lookup"><span data-stu-id="356a1-320">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="356a1-321">Хранение на месте</span><span class="sxs-lookup"><span data-stu-id="356a1-321">In-Place Hold</span></span>  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |<span data-ttu-id="356a1-p152">Свойство *InPlaceHolds* содержит идентификатор GUID режима сохранения, помещенные на почтовый ящик. Чтобы узнать, что это хранение на месте, так как код GUID не начинается с префикса.</span><span class="sxs-lookup"><span data-stu-id="356a1-p152">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the mailbox. You can tell this is an In-Place Hold because the GUID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="356a1-324">Можно использовать `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` в Exchange Online PowerShell для получения сведений о хранение на месте в почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="356a1-324">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the mailbox.</span></span>  <br/> |
| <span data-ttu-id="356a1-325">Политики хранения Office 365 в безопасности &amp; центре соответствия требованиям применяется к определенным почтовым ящикам</span><span class="sxs-lookup"><span data-stu-id="356a1-325">Office 365 retention policies in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> <span data-ttu-id="356a1-326">или</span><span class="sxs-lookup"><span data-stu-id="356a1-326">or</span></span>  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |<span data-ttu-id="356a1-p153">При выполнении командлета **Get-Mailbox** , свойство *InPlaceHolds* также содержит политики хранения идентификаторов GUID Office 365, применяется к почтовому ящику. Можно определить политики хранения, так как код GUID начинается с `mbx` префикса. Обратите внимание, что если GUID политики хранения начинается с `skp` префикс, которое указывает, что политика хранения применяется к Скайп для бизнеса бесед.</span><span class="sxs-lookup"><span data-stu-id="356a1-p153">When you run the **Get-Mailbox** cmdlet, the  *InPlaceHolds*  property also contains GUIDs of Office 365 retention policies applied to the mailbox. You can identify retention policies because the GUID starts with the  `mbx` prefix. Note that if the GUID of the retention policy starts with the  `skp` prefix, that indicates that the retention policy is applied to Skype for Business conversations.  </span></span><br/> <span data-ttu-id="356a1-330">Политики хранения удостоверений Office 365, которая применяется к почтовому ящику, выполните следующую команду в безопасности &amp; PowerShell центр соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="356a1-330">To identity the Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="356a1-331">Удалите `mbx` или `skp` префиксов при выполнении этой команды.</span><span class="sxs-lookup"><span data-stu-id="356a1-331">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="356a1-332">Политики хранения всей организации Office 365 в безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="356a1-332">Organization-wide Office 365 retention policies in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="356a1-333">Нет значения</span><span class="sxs-lookup"><span data-stu-id="356a1-333">No value</span></span>  <br/> <span data-ttu-id="356a1-334">или</span><span class="sxs-lookup"><span data-stu-id="356a1-334">or</span></span>  <br/>  <span data-ttu-id="356a1-335">`-mbxe9b52bf7ab3b46a286308ecb29624696`(указывает на то, что почтовый ящик исключен из политики организации)</span><span class="sxs-lookup"><span data-stu-id="356a1-335">`-mbxe9b52bf7ab3b46a286308ecb29624696` (indicates that the mailbox is excluded from an organization-wide policy)</span></span>  <br/> |<span data-ttu-id="356a1-336">Даже в том случае, если свойство *InPlaceHolds* пуст, при запуске командлета **Get-Mailbox** , по-прежнему могут возникнуть один или несколько всей организации Office 365 политики хранения применяется к почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="356a1-336">Even if the  *InPlaceHolds*  property is empty when you run the **Get-Mailbox** cmdlet, there still might be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span>  <br/> <span data-ttu-id="356a1-p154">Чтобы проверить это, можно запустить `Get-OrganizationConfig | FL InPlaceHolds` в Exchange Online PowerShell, чтобы получить список идентификаторов GUID для политики хранения всей организации Office 365. Идентификатор GUID для политик хранения всей организации, применяемых Пуск почтовых ящиков Exchange с `mbx` префикс; например `mbxa3056bb15562480fadb46ce523ff7b02`.</span><span class="sxs-lookup"><span data-stu-id="356a1-p154">To verify this, you can run the  `Get-OrganizationConfig | FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  </span></span><br/> <span data-ttu-id="356a1-339">Удостоверение политики хранения Office 365 всей организации, которая применяется к почтовому ящику, выполните следующую команду в безопасности &amp; PowerShell центр соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="356a1-339">To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="356a1-340">Обратите внимание на то, что если почтовый ящик исключены из политики хранения всей организации Office 365, идентификатор GUID для политики хранения отображается в свойстве *InPlaceHolds* почтового ящика пользователя при запуске командлета **Get-Mailbox** ; определяется префикс `-mbx`; Например`-mbxe9b52bf7ab3b46a286308ecb29624696`</span><span class="sxs-lookup"><span data-stu-id="356a1-340">Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696`</span></span> <br/> |
|<span data-ttu-id="356a1-341">хранение случая обнаружения электронных данных в безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="356a1-341">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |<span data-ttu-id="356a1-p155">Свойство *InPlaceHolds* также содержит идентификатор GUID для любого удержания, связанные с вариантом eDiscovery в системы &amp; центре соответствия требованиям, который может располагаться на почтовый ящик. Можно указать это делами удержание электронных данных, так как код GUID начинается с `UniH` префикса.</span><span class="sxs-lookup"><span data-stu-id="356a1-p155">The  *InPlaceHolds*  property also contains the GUID of any hold associated with an eDiscovery case in the Security &amp; Compliance Center that might be placed on the mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="356a1-p156">Можно использовать `Get-CaseHoldPolicy` командлет в безопасности &amp; PowerShell центр соответствия требованиям для получения сведений о случая обнаружения электронных данных, с которым связана удержание для почтового ящика. Например, можно выполнить команду `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` для отображения имени делами удержания, который размещается на почтовый ящик. Удалите `UniH` префиксов при выполнении этой команды.</span><span class="sxs-lookup"><span data-stu-id="356a1-p156">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the mailbox is associated with. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  </span></span><br/><br/> <span data-ttu-id="356a1-347">Чтобы удостоверение случая обнаружения электронных данных, с которым связана удержание для почтового ящика выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="356a1-347">To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:</span></span><br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


