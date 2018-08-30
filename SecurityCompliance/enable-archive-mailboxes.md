---
title: Включение архивных почтовых ящиков в Office 365 безопасность &amp; центре соответствия требованиям
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Использование безопасности Office 365 &amp; центре соответствия требованиям для включения архивных почтовых ящиков для поддержки хранения сообщений вашей организации, обнаружения электронных данных и удерживайте требования.
ms.openlocfilehash: 5ba578ba611f619194ac4f475121bd485b75f9e0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534938"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="66168-103">Включение архивных почтовых ящиков в Office 365 безопасность &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="66168-103">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>
  
<span data-ttu-id="66168-p101">Архивация в Office 365 (также называемая в архивирование на месте) предоставляет пользователям дополнительного почтового ящика дискового пространства. После включения архивные почтовые ящики, пользователи могут получить доступ к и хранение сообщений в их архивных почтовых ящиков с помощью Microsoft Outlook и Outlook Web App. пользователи могут также копирования или перемещения сообщений между их основной почтовый ящик и их архивного почтового ящика. Они также можно восстановить удаленные элементы из папки восстанавливаемых элементов в почтовом ящике архива с помощью средства восстановления удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="66168-p101">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space. After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook Web App. Users can also move or copy messages between their primary mailbox and their archive mailbox. They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="66168-p102">Office 365 предоставляет неограниченного архивного хранилища с помощью функции архивации развертываемым. При развертываемым архивации включается, и затем достигается Квота начальной хранилища в архивный почтовый ящик пользователя, Office 365 автоматически добавляет дополнительные дискового пространства. Это означает, что пользователи не будут выполняться недостаточно дискового пространства для сохранения почтовых ящиков и изначально управление что-либо после вам не придется Включение архивного почтового ящика и включение развертываемым архивации для вашей организации. Для получения дополнительных сведений см [неограниченном архивировании в Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="66168-p102">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature. When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space. This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization. For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="66168-112">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="66168-112">Before you begin</span></span>

<span data-ttu-id="66168-p103">Необходимо назначить роль получателей почты в Exchange Online для включения или отключения архивные почтовые ящики. По умолчанию эта роль назначается группы ролей управления получателя и управление организацией на странице " **разрешения** " в центре администрирования Exchange. Если не отображается страница **архива** в системы &amp; центру соответствия требованиям, обратитесь к администратору, чтобы назначить необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="66168-p103">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes. By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. If you don't see the **Archive** page in the Security &amp; Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="66168-116">Включение архивного почтового ящика</span><span class="sxs-lookup"><span data-stu-id="66168-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="66168-117">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="66168-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="66168-118">Войдите в Office 365 с помощью учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="66168-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="66168-119">В левой области безопасности &amp; центре соответствия требованиям, нажмите кнопку **управления данными** \> **архива**.</span><span class="sxs-lookup"><span data-stu-id="66168-119">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="66168-p104">Отобразится страница **Архив**. В столбце **Архивный почтовый ящик** указывается, включен ли архивный почтовый ящик для соответствующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="66168-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="66168-122">В списке почтовых ящиков выберите пользователя, для которого вы хотите включить архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="66168-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![Нажмите кнопку включить в области сведений выбранного пользователя с целью архивного почтового ящика](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="66168-124">В области сведений для выбранного пользователя нажмите кнопку **Включить**.</span><span class="sxs-lookup"><span data-stu-id="66168-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="66168-p105">Отображается предупреждение о том, что при включении архивного почтового ящика элементов в почтовом ящике пользователя, возраст которых превышает политики архивации, назначенные для будут перемещены в новый архивный почтовый ящик. Архив политики по умолчанию, который является частью политики хранения, назначенных для почтовых ящиков Exchange Online перемещает элементы в архивный почтовый ящик двух лет после даты доставлено в почтовый ящик или создаваемые пользователем элемента. Для получения дополнительных сведений обратитесь к разделу **Дополнительные сведения** в этой статье.</span><span class="sxs-lookup"><span data-stu-id="66168-p105">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox. The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="66168-128">Нажмите кнопку **Да**, чтобы включить архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="66168-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="66168-p106">Выполнение может занять некоторое время создание архивного почтового ящика. При создании, **архивный почтовый ящик: включено** отображается в области сведений для выбранного пользователя. Нажмите кнопку **Обновить,** может потребоваться ![значок обновления](media/O365-MDM-Policy-RefreshIcon.gif) для обновления данных в области сведений.</span><span class="sxs-lookup"><span data-stu-id="66168-p106">It might take a few moments to create the archive mailbox. When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="66168-p107">Вы также можете включить архивные почтовые ящики сразу для нескольких пользователей, выбрав их с помощью клавиши SHIFT или CTRL. Выбрав несколько почтовых ящиков, нажмите кнопку **Включить** в области сведений. </span><span class="sxs-lookup"><span data-stu-id="66168-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="66168-134">Отключение архивного почтового ящика</span><span class="sxs-lookup"><span data-stu-id="66168-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="66168-p108">Можно также использовать страницу **архива** в безопасности &amp; центре соответствия требованиям, чтобы отключить архивный почтовый ящик пользователя. Если вы отключили архивного почтового ящика можно подключиться к основной почтовый ящик пользователя в течение 30 дней после его отключение. В этом случае восстановить исходное содержимое архивного почтового ящика. Через 30 дней после их содержимое исходного архивного почтового ящика будут окончательно удалены и не могут быть восстановлены. Так что если вы повторно включить архив более 30 дней после его отключения, создается новый архивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="66168-p108">You can also use the **Archive** page in the Security &amp; Compliance Center to disable a user's archive mailbox. After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it. In this case, the original contents of the archive mailbox are restored. After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered. So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="66168-p109">Обратите внимание, что по умолчанию архив назначена политика почтовых ящиков пользователей перемещения элементов в архивный почтовый ящик двух лет после даты элемента доставки. Если отключить архивный почтовый ящик пользователя, не действие не выполняется на элементы почтового ящика и они будут оставаться в основной почтовый ящик пользователя.</span><span class="sxs-lookup"><span data-stu-id="66168-p109">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered. If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="66168-142">Чтобы отключить архивный почтовый ящик:</span><span class="sxs-lookup"><span data-stu-id="66168-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="66168-143">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="66168-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="66168-144">Войдите в Office 365 с помощью учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="66168-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="66168-145">В левой области безопасности &amp; центре соответствия требованиям, нажмите кнопку **управления данными** \> **архива**.</span><span class="sxs-lookup"><span data-stu-id="66168-145">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="66168-p110">Отобразится страница **Архив**. В столбце **Архивный почтовый ящик** указывается, включен ли архивный почтовый ящик для соответствующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="66168-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="66168-148">В списке почтовых ящиков выберите пользователя, для которого вы хотите выключить архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="66168-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="66168-149">В области сведений нажмите кнопку **Отключить**. </span><span class="sxs-lookup"><span data-stu-id="66168-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="66168-150">Отображается сообщение предупреждения о том, что вам придется 30 дней, чтобы повторно включить архивного почтового ящика и что через 30 дней после их все данные в архиве будут окончательно удалены.</span><span class="sxs-lookup"><span data-stu-id="66168-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="66168-151">Нажмите кнопку **Да**, чтобы отключить архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="66168-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="66168-p111">Выполнение может занять несколько минут, чтобы отключить архивный почтовый ящик. При отключении, **архивный почтовый ящик: этот параметр отключен** отображается в области сведений для выбранного пользователя. Нажмите кнопку **Обновить,** может потребоваться ![значок обновления](media/O365-MDM-Policy-RefreshIcon.gif) для обновления данных в области сведений.</span><span class="sxs-lookup"><span data-stu-id="66168-p111">It might take a few moments to disable the archive mailbox. When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="66168-p112">Вы также можете отключить архивные почтовые ящики сразу для нескольких пользователей, выбрав их с помощью клавиши SHIFT или CTRL. Выбрав несколько почтовых ящиков, нажмите кнопку **Отключить** в области сведений. </span><span class="sxs-lookup"><span data-stu-id="66168-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="66168-157">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="66168-157">More information</span></span>
  
- <span data-ttu-id="66168-p113">Архивные почтовые ящики помочь вам и вашим пользователям в соответствии с вашей организации хранения, обнаружения электронных данных и удерживайте требования. К примеру можно использовать политики хранения вашей организации Exchange для переноса содержимого почтовых ящиков на пользователей архивного почтового ящика. При использовании средства поиска содержимого в системы &amp; центре соответствия требованиям для поиска почтового ящика пользователя для определенного содержимого, архивный почтовый ящик пользователя также выполнить поиск. И, при помещении хранение для судебного разбирательства или применение политики хранения к Office 365 для почтового ящика пользователя, также сохраняются элементы в архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="66168-p113">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements. For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox. When you use the Content Search tool in the Security &amp; Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched. And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="66168-p114">Если архивного почтового ящика включена, пользователи могут хранить сообщения в почтовом ящике архива. Пользователи могут получить доступ к почтовым ящикам архива с помощью Microsoft Outlook и Outlook Web App. с помощью этих клиентских приложений, пользователи могут просматривать сообщения в почтовом ящике архива и копирования или перемещения сообщений между их основной почтовый ящик и их архивного почтового ящика. Пользователи также можно восстановить удаленных элементов из папки восстанавливаемых элементов в почтовом ящике архива с помощью средства восстановления удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="66168-p114">When an archive mailbox is enabled, users can store messages in their archive mailbox. Users can access their archive mailboxes by using Microsoft Outlook and Outlook Web App. Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox. Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="66168-p115">После архив включены почтовые ящики вашей организации могут воспользоваться преимуществами по умолчанию Exchange политику хранения (также называемая политики управления записями обмена сообщениями или управления записями сообщений), который автоматически назначается для каждого почтового ящика. При включении архивного почтового ящика, политика хранения по умолчанию Exchange автоматически выполняет следующее.</span><span class="sxs-lookup"><span data-stu-id="66168-p115">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox. When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="66168-168">Перемещает элементы, которые хранились два года или дольше, из основного почтового ящика пользователя в архивный.</span><span class="sxs-lookup"><span data-stu-id="66168-168">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="66168-169">Перемещает элементы, которые хранились 14 дней или дольше, из папки "Элементы для восстановления" в основном почтовом ящике пользователя в такую же папку архивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="66168-169">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="66168-170">Дополнительные сведения об архивных почтовых ящиков и политики хранения Exchange можно:</span><span class="sxs-lookup"><span data-stu-id="66168-170">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
  
  - [<span data-ttu-id="66168-171">Архивные почтовые ящики в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="66168-171">Archive mailboxes in Exchange Online</span></span>](https://go.microsoft.com/fwlink/?LinkId=404421)
    
  - [<span data-ttu-id="66168-172">Теги хранения и политики хранения</span><span class="sxs-lookup"><span data-stu-id="66168-172">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="66168-173">По умолчанию политика хранения в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="66168-173">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="66168-174">Настроить политику архивации и удаления для почтовых ящиков в организации Office 365</span><span class="sxs-lookup"><span data-stu-id="66168-174">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
