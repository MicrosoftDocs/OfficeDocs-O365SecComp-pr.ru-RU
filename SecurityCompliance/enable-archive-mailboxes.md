---
title: Включение архивных почтовых ящиков в центре безопасности _Амп_ соответствия требованиям
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Используйте центр соответствия требованиям по безопасности _Амп_ в Office 365, чтобы включить архивные почтовые ящики, чтобы обеспечить поддержку хранения сообщений, обнаружения электронных данных и удержания электронных данных в Организации.
ms.openlocfilehash: f4f02e5107526f2f45b0a46579e0676b791f0dd1
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402927"
---
# <a name="enable-archive-mailboxes-in-the-security--compliance-center"></a><span data-ttu-id="32443-103">Включение архивных почтовых ящиков в центре безопасности _Амп_ соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="32443-103">Enable archive mailboxes in the Security & Compliance Center</span></span>
  
<span data-ttu-id="32443-104">Архивация в Office 365 (также называется Архивация на месте) предоставляет пользователям дополнительное место для хранения почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="32443-104">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space.</span></span> <span data-ttu-id="32443-105">После включения архивных почтовых ящиков пользователи могут получать доступ к почтовым ящикам в архивных почтовых ящиках с помощью Microsoft Outlook и Outlook в Интернете (прежнее название — Outlook Web App).</span><span class="sxs-lookup"><span data-stu-id="32443-105">After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook on the web (formerly known as Outlook Web App).</span></span> <span data-ttu-id="32443-106">Пользователи также могут перемещать или копировать сообщения между основным и архивным почтовым ящиком.</span><span class="sxs-lookup"><span data-stu-id="32443-106">Users can also move or copy messages between their primary mailbox and their archive mailbox.</span></span> <span data-ttu-id="32443-107">Кроме того, они могут восстанавливать удаленные элементы из папки "элементы с возможностью восстановления" в своем архивном почтовом ящике с помощью средства восстановления удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="32443-107">They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="32443-108">Office 365 предоставляет неограниченный объем архивного хранилища с автоматически развертываемой функцией архивации.</span><span class="sxs-lookup"><span data-stu-id="32443-108">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature.</span></span> <span data-ttu-id="32443-109">При включенном автоматическом развертывании архивации и последующем достижении первоначальной квоты хранилища в архивном почтовом ящике пользователя Office 365 автоматически добавляет дополнительное дисковое пространство.</span><span class="sxs-lookup"><span data-stu-id="32443-109">When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space.</span></span> <span data-ttu-id="32443-110">Это означает, что пользователи не смогут использовать место для хранения почтовых ящиков, и вам не придется управлять что-либо после первоначального включения архивного почтового ящика и включения автоматического расширения архивации для Организации.</span><span class="sxs-lookup"><span data-stu-id="32443-110">This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization.</span></span> <span data-ttu-id="32443-111">Дополнительные сведения см. в статье [Общие сведения о неограниченной архивации в Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="32443-111">For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="32443-112">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="32443-112">Before you begin</span></span>

<span data-ttu-id="32443-113">Для включения или отключения архивных почтовых ящиков необходимо назначить роль получателей почты в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="32443-113">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes.</span></span> <span data-ttu-id="32443-114">По умолчанию эта роль назначается группам ролей "Управление получателями" и "Управление организацией" на странице " **разрешения** " в центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="32443-114">By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="32443-115">Если страница **Архив** не отображается в центре безопасности _Амп_ соответствие требованиям, попросите администратора назначить вам необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="32443-115">If you don't see the **Archive** page in the Security & Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="32443-116">Включение архивного почтового ящика</span><span class="sxs-lookup"><span data-stu-id="32443-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="32443-117">Перейдите по ссылке [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="32443-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="32443-118">Войдите в Office 365 с помощью своей рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="32443-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="32443-119">В левой области центра безопасности _амп_ соответствие требованиям щелкните **Архив**управления **данными** \> .</span><span class="sxs-lookup"><span data-stu-id="32443-119">In the left pane of the Security & Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="32443-120">Отобразится страница **Архив**.</span><span class="sxs-lookup"><span data-stu-id="32443-120">The **Archive** page is displayed.</span></span> <span data-ttu-id="32443-121">В столбце **Архивный почтовый ящик** указывается, включен ли архивный почтовый ящик для соответствующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-121">The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="32443-122">В списке почтовых ящиков выберите пользователя, для которого вы хотите включить архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="32443-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![Выберите включить в области сведений выбранного пользователя, чтобы включить архивный почтовый ящик.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="32443-124">В области сведений для выбранного пользователя нажмите кнопку **включить**.</span><span class="sxs-lookup"><span data-stu-id="32443-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="32443-125">Отображается предупреждение о том, что при включении архивного почтового ящика элементы в почтовом ящике пользователя, которые старше политики архивации, назначенной для почтового ящика, будут перемещены в новый архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="32443-125">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox.</span></span> <span data-ttu-id="32443-126">Политика архивации по умолчанию, которая является частью политики хранения, назначенной для почтовых ящиков Exchange Online, перемещает элементы в архивный почтовый ящик через два года после того, как дата доставки элемента в почтовый ящик или создана пользователем.</span><span class="sxs-lookup"><span data-stu-id="32443-126">The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user.</span></span> <span data-ttu-id="32443-127">Для получения дополнительных сведений обратитесь к разделу **more info** этой статьи.</span><span class="sxs-lookup"><span data-stu-id="32443-127">For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="32443-128">Нажмите кнопку **Да**, чтобы включить архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="32443-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="32443-129">Создание архивного почтового ящика может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="32443-129">It might take a few moments to create the archive mailbox.</span></span> <span data-ttu-id="32443-130">Когда он будет создан, **архивный почтовый ящик: Enabled** отображается в области сведений для выбранного пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-130">When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user.</span></span> <span data-ttu-id="32443-131">Чтобы обновить сведения в области \*\*\*\* ![сведений, может](media/O365-MDM-Policy-RefreshIcon.gif) потребоваться нажать кнопку Обновить обновление.</span><span class="sxs-lookup"><span data-stu-id="32443-131">You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="32443-p107">Вы также можете включить архивные почтовые ящики сразу для нескольких пользователей, выбрав их с помощью клавиши SHIFT или CTRL. Выбрав несколько почтовых ящиков, нажмите кнопку **Включить** в области сведений. </span><span class="sxs-lookup"><span data-stu-id="32443-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="32443-134">Отключение архивного почтового ящика</span><span class="sxs-lookup"><span data-stu-id="32443-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="32443-135">Вы также можете отключить архивный почтовый ящик пользователя с помощью страницы " **Архив** " в центре обеспечения безопасности _амп_.</span><span class="sxs-lookup"><span data-stu-id="32443-135">You can also use the **Archive** page in the Security & Compliance Center to disable a user's archive mailbox.</span></span> <span data-ttu-id="32443-136">После этого архивный почтовый ящик можно повторно подключить к основному почтовому ящику пользователя в течение 30 дней после отключения.</span><span class="sxs-lookup"><span data-stu-id="32443-136">After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it.</span></span> <span data-ttu-id="32443-137">В этом случае восстанавливается исходное содержимое архивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="32443-137">In this case, the original contents of the archive mailbox are restored.</span></span> <span data-ttu-id="32443-138">Через 30 дней содержимое исходного архивного почтового ящика удаляется безвозвратно.</span><span class="sxs-lookup"><span data-stu-id="32443-138">After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered.</span></span> <span data-ttu-id="32443-139">Поэтому если после отключения архива прошло более 30 дней, при его повторном включении будет создан новый архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="32443-139">So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="32443-140">Обратите внимание, что политика архивации по умолчанию, назначенная почтовым ящикам пользователей, перемещает элементы в архивный почтовый ящик через два года после даты доставки элемента.</span><span class="sxs-lookup"><span data-stu-id="32443-140">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered.</span></span> <span data-ttu-id="32443-141">Если отключить архивный почтовый ящик пользователя, никакие действия для элементов почтовых ящиков не будут выполняться, и они останутся в основном почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-141">If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="32443-142">Чтобы отключить архивный почтовый ящик:</span><span class="sxs-lookup"><span data-stu-id="32443-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="32443-143">Перейдите по ссылке [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="32443-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="32443-144">Войдите в Office 365 с помощью своей рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="32443-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="32443-145">В левой области центра безопасности _амп_ соответствие требованиям щелкните **Архив**управления **данными** \> .</span><span class="sxs-lookup"><span data-stu-id="32443-145">In the left pane of the Security & Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="32443-p110">Отобразится страница **Архив**. В столбце **Архивный почтовый ящик** указывается, включен ли архивный почтовый ящик для соответствующего пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="32443-148">В списке почтовых ящиков выберите пользователя, для которого вы хотите выключить архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="32443-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="32443-149">В области сведений нажмите кнопку **Отключить**. </span><span class="sxs-lookup"><span data-stu-id="32443-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="32443-150">Отображается предупреждающее сообщение о том, что для повторного включения архивного почтового ящика потребуется 30 дней, а после 30 дней все данные в архиве будут окончательно удалены.</span><span class="sxs-lookup"><span data-stu-id="32443-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="32443-151">Нажмите кнопку **Да**, чтобы отключить архивный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="32443-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="32443-152">Отключение архивного почтового ящика может занять несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="32443-152">It might take a few moments to disable the archive mailbox.</span></span> <span data-ttu-id="32443-153">Если этот параметр отключен, **архивный почтовый ящик: отключено** отображается в области сведений для выбранного пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-153">When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user.</span></span> <span data-ttu-id="32443-154">Чтобы обновить сведения в области \*\*\*\* ![сведений, может](media/O365-MDM-Policy-RefreshIcon.gif) потребоваться нажать кнопку Обновить обновление.</span><span class="sxs-lookup"><span data-stu-id="32443-154">You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="32443-p112">Вы также можете отключить архивные почтовые ящики сразу для нескольких пользователей, выбрав их с помощью клавиши SHIFT или CTRL. Выбрав несколько почтовых ящиков, нажмите кнопку **Отключить** в области сведений. </span><span class="sxs-lookup"><span data-stu-id="32443-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="32443-157">Включение и отключение архивных почтовых ящиков с помощью Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="32443-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="32443-158">Вы также можете использовать Exchange Online PowerShell для включения архивных почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="32443-158">You can also use Exchange Online PowerShell to enable archive mailboxes.</span></span> <span data-ttu-id="32443-159">Основная причина использования PowerShell заключается в том, что вы можете быстро включить архивный почтовый ящик для всех пользователей в Организации.</span><span class="sxs-lookup"><span data-stu-id="32443-159">The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="32443-160">Первый шаг — подключение к Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="32443-160">The first step is to connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="32443-161">Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="32443-161">For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="32443-162">После подключения к Exchange Online можно выполнить команды, приведенные в следующих разделах, для включения или отключения архивных почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="32443-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="32443-163">Включение архивных почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="32443-163">Enable archive mailboxes</span></span>

<span data-ttu-id="32443-164">Выполните следующую команду, чтобы включить архивный почтовый ящик для одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="32443-165">Выполните следующую команду, чтобы включить архивный почтовый ящик для всех пользователей в Организации (чей архивный почтовый ящик в данный момент не включен).</span><span class="sxs-lookup"><span data-stu-id="32443-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="32443-166">Отключение архивных почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="32443-166">Disable archive mailboxes</span></span>

<span data-ttu-id="32443-167">Выполните следующую команду, чтобы отключить архивный почтовый ящик для отдельного пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="32443-168">Выполните следующую команду, чтобы отключить архивный почтовый ящик для всех пользователей в Организации (чей архивный почтовый ящик включен).</span><span class="sxs-lookup"><span data-stu-id="32443-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="32443-169">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="32443-169">More information</span></span>
  
- <span data-ttu-id="32443-170">Если архивный почтовый ящик включен, пользователи могут хранить сообщения в архивном почтовом ящике.</span><span class="sxs-lookup"><span data-stu-id="32443-170">When an archive mailbox is enabled, users can store messages in their archive mailbox.</span></span> <span data-ttu-id="32443-171">Пользователи могут получать доступ к архивным почтовым ящикам с помощью Microsoft Outlook и Outlook в Интернете.</span><span class="sxs-lookup"><span data-stu-id="32443-171">Users can access their archive mailboxes by using Microsoft Outlook and Outlook on the web.</span></span> <span data-ttu-id="32443-172">Используя одно из этих клиентских приложений, пользователи могут просматривать сообщения в архивных почтовых ящиках, а также перемещать и копировать их из архивного в основной и наоборот.</span><span class="sxs-lookup"><span data-stu-id="32443-172">Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox.</span></span> <span data-ttu-id="32443-173">Пользователи также могут восстанавливать удаленные элементы из папки "Элементы с возможностью восстановления" в архивном почтовом ящике с помощью средства восстановления удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="32443-173">Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span>

   <span data-ttu-id="32443-174">Список лицензий Outlook, поддерживающих архивацию на месте, приведен в статье [требования к лицензиям Outlook для функций Exchange](https://support.office.com/article/outlook-license-requirements-for-exchange-features-46b6b7c5-c3ca-43e5-8424-1e2807917c99).</span><span class="sxs-lookup"><span data-stu-id="32443-174">For a list of Outlook licenses that support In-Place Archiving, see [Outlook license requirements for Exchange features](https://support.office.com/article/outlook-license-requirements-for-exchange-features-46b6b7c5-c3ca-43e5-8424-1e2807917c99).</span></span>

- <span data-ttu-id="32443-175">Архивные почтовые ящики помогают вам и вашим пользователям обеспечить соответствие требованиям Организации относительно хранения, обнаружения электронных данных и удержания.</span><span class="sxs-lookup"><span data-stu-id="32443-175">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements.</span></span> <span data-ttu-id="32443-176">Например, вы можете использовать политику хранения Exchange вашей организации для перемещения содержимого почтовых ящиков в архивный почтовый ящик пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-176">For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox.</span></span> <span data-ttu-id="32443-177">При использовании средства "поиск контента" в центре безопасности _Амп_ соответствие требованиям для поиска определенного содержимого в почтовом ящике пользователя также будет выполняться поиск архивного почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="32443-177">When you use the Content Search tool in the Security & Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched.</span></span> <span data-ttu-id="32443-178">Кроме того, при помещении судебного удержания или применении политики хранения Office 365 к почтовому ящику пользователя, элементы в архивном почтовом ящике также сохраняются.</span><span class="sxs-lookup"><span data-stu-id="32443-178">And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="32443-179">После включения архивных почтовых ящиков Организация может использовать политику хранения Exchange по умолчанию (также называемую "Управление записями сообщений" или "политика управления ЗАПИСЯМИ сообщений"), которая автоматически назначается каждому почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="32443-179">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox.</span></span> <span data-ttu-id="32443-180">При включении архивного почтового ящика политика хранения Exchange по умолчанию автоматически выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="32443-180">When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="32443-181">Перемещает элементы, которые хранились два года или дольше, из основного почтового ящика пользователя в архивный.</span><span class="sxs-lookup"><span data-stu-id="32443-181">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="32443-182">Перемещает элементы, которые хранились 14 дней или дольше, из папки "Элементы для восстановления" в основном почтовом ящике пользователя в такую же папку архивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="32443-182">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="32443-183">Дополнительные сведения о архивных почтовых ящиках и политиках хранения Exchange приведены в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="32443-183">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
    
  - [<span data-ttu-id="32443-184">Теги хранения и политики хранения</span><span class="sxs-lookup"><span data-stu-id="32443-184">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="32443-185">Политика хранения по умолчанию в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="32443-185">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="32443-186">Настройка политики архивации и удаления для почтовых ящиков в организации Office 365</span><span class="sxs-lookup"><span data-stu-id="32443-186">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
