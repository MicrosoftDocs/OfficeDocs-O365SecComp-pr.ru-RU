---
title: Управление почтовыми пользователями в EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 4bfaf2ab-e633-4227-8bde-effefb41a3db
description: "Определение почтовых пользователей \x97 важный этап управления службой Exchange Online Protection (EOP)."
ms.openlocfilehash: b0093c64a0fcb5997b474e7bd491c0915164b77e
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341030"
---
# <a name="manage-mail-users-in-eop"></a><span data-ttu-id="223df-103">Управление почтовыми пользователями в EOP</span><span class="sxs-lookup"><span data-stu-id="223df-103">Manage mail users in EOP</span></span>

<span data-ttu-id="223df-p101">Определение почтовых пользователей  важный этап управления службой Exchange Online Protection (EOP). Существует несколько способов управления получателями в EOP.</span><span class="sxs-lookup"><span data-stu-id="223df-p101">Defining mail users is an important part of managing the Exchange Online Protection (EOP) service. There are several ways that you can manage users in EOP:</span></span>
  
- <span data-ttu-id="223df-p102">Используйте синхронизацию службы каталогов для управления почтовыми пользователями: Если ваша компания имеет существующие учетные записи пользователей в локальной среде Active Directory, вы можете синхронизировать эти учетные записи с Azure Active Directory (AD), где копия учетных записей хранится в облаке. При синхронизации существующих учетных записей пользователей с Azure Active Directory вы можете просмотреть этих пользователей в области **получателей** центра администрирования Exchange. Рекомендуется использовать синхронизацию службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="223df-p102">Use directory synchronization to manage mail users: If your company has existing user accounts in an on-premises Active Directory environment, you can synchronize those accounts to Azure Active Directory (AD), where a copy of the accounts is stored in the cloud. When you synchronize your existing user accounts to Azure Active Directory, you can view those users in the **Recipients** pane of the Exchange admin center (EAC). Using directory synchronization is recommended.</span></span> 
    
- <span data-ttu-id="223df-p103">Управление почтовыми пользователями с помощью Центра администрирования Exchange: добавление почтовых пользователей и управление ими непосредственно в Центре администрирования Exchange. Это самый простой и удобный способ добавить почтовых пользователей по одному.</span><span class="sxs-lookup"><span data-stu-id="223df-p103">Use the EAC to manage mail users: Add and manage mail users directly in the EAC. This is the easiest way to add mail users and is useful for adding one user at a time.</span></span>
    
- <span data-ttu-id="223df-p104">Использование удаленной консоли Windows PowerShell для управления почтовыми пользователями: добавление почтовых пользователей и управление ими с помощью удаленной консоли Windows PowerShell. Этот способ удобен для добавления нескольких записей и создания сценариев.</span><span class="sxs-lookup"><span data-stu-id="223df-p104">Use remote Windows PowerShell to manage mail users: Add and manage mail users by running remote Windows PowerShell. This method is useful for adding multiple records and creating scripts.</span></span>
    
> [!NOTE]
> <span data-ttu-id="223df-113">Пользователей можно добавлять в Центре администрирования Office 365, однако таких пользователей невозможно использовать в качестве получателей электронной почты.</span><span class="sxs-lookup"><span data-stu-id="223df-113">You can add users in the Office 365 admin center, however these users can't be used as mail recipients.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="223df-114">Приступая к работе</span><span class="sxs-lookup"><span data-stu-id="223df-114">Before you begin</span></span>

- <span data-ttu-id="223df-p105">Для процедур в этом разделе требуются особые разрешения. См. информацию о разрешениях по каждой процедуре.</span><span class="sxs-lookup"><span data-stu-id="223df-p105">Procedures in this topic require specific permissions. See each procedure for its permissions information.</span></span>
    
- <span data-ttu-id="223df-117">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Сочетания клавиш в Центре администрирования Exchange**.</span><span class="sxs-lookup"><span data-stu-id="223df-117">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="223df-p106">Возникли проблемы? Обратитесь за помощью к участникам форумов, посвященных Exchange. Посетите форумы по таким продуктам: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) или [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="223df-p106">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-directory-synchronization-to-manage-mail-users"></a><span data-ttu-id="223df-121">Управление почтовыми пользователями с помощью синхронизации службы каталогов</span><span class="sxs-lookup"><span data-stu-id="223df-121">Use directory synchronization to manage mail users</span></span>

<span data-ttu-id="223df-122">В этом разделе представлены сведения об управлении пользователями электронной почты с помощью синхронизации службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="223df-122">This section provides information about managing email users by using directory synchronization.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="223df-p107">Если для управления получателями используется синхронизация службы каталогов, пользователей можно добавлять и управлять ими в Центр администрирования Office 365, однако они не будут синхронизироваться с локальной службой Active Directory. Это объясняется тем, что получатели синхронизируются только в одном направлении: из локальной службы каталогов Active Directory в облако.</span><span class="sxs-lookup"><span data-stu-id="223df-p107">If you use directory synchronization to manage your recipients, you can still add and manage users in the Office 365 admin center, but they will not be synchronized with your on-premises Active Directory. This is because directory synchronization only syncs recipients from your on-premises Active Directory to the cloud.</span></span> 
  
> [!TIP]
>  <span data-ttu-id="223df-p108">Использовать синхронизацию службы каталогов рекомендуется для следующих компонентов: _Гт_ **Outlook Safe Senders and Blocked Sender Lists** — при синхронизации со службой эти списки будут иметь приоритет над фильтрацией нежелательной почты в службе. Это позволяет пользователям управлять своими списками надежных отправителей и заблокированных отправителей для отдельных пользователей или для отдельных доменов. **пограничная блокировка на основе каталога _гт_ (DBEB)** — дополнительные сведения об DBEB см. [в статье Использование пограничной блокировки на основе каталогов для отклонения сообщений, отправляемых](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx)недопустимым получателям. **Карантин пользователя _Гт_ конечного пользователя** — для доступа к карантину нежелательной почты конечного пользователя, конечные пользователи должны иметь действительный идентификатор пользователя Office 365 и пароль. EOP клиенты, защищающие локальные почтовые ящики, должны быть действительными пользователями электронной почты. **правила обработки почты** _гт_ — при использовании синхронизации службы каталогов существующие пользователи и группы Active Directory автоматически отправляются в облако, а затем можно создавать правила для поток обработки почты (также называемые правилами транспорта), предназначенные для определенных пользователей и/или или группы без необходимости вручную добавлять их через центр администрирования Exchange или Exchange Online Protection PowerShell. Обратите внимание на то, что [динамические группы рассылки](https://go.microsoft.com/fwlink/?LinkId=507569) невозможно синхронизировать через синхронизацию службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="223df-p108">Using directory synchronization is recommended for use with the following features: > **Outlook safe sender and blocked sender lists** - When synchronized to the service, these lists will take precedence over spam filtering in the service. This lets users manage their own safe sender and blocked sender lists on a per-user or per-domain basis. > **Directory Based Edge Blocking (DBEB)** - For more information about DBEB, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx). > **End user spam quarantine** - In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password. EOP customers protecting on-premises mailboxes must be valid email users. > **Mail flow rules** - When you use directory synchronization, your existing Active Directory users and groups are automatically uploaded to the cloud, and you can then create mail flow rules (also known as transport rules) that target specific users and/or groups without having to manually add them via the the EAC or Exchange Online Protection PowerShell. Note that [dynamic distribution groups](https://go.microsoft.com/fwlink/?LinkId=507569) can't be synchronized via directory synchronization.</span></span> 
  
 <span data-ttu-id="223df-132">**Приступая к работе**</span><span class="sxs-lookup"><span data-stu-id="223df-132">**Before you begin**</span></span>
  
<span data-ttu-id="223df-133">Получите необходимые разрешения и подготовьтесь к синхронизации службы каталогов, как описано в статье [Подготовка к синхронизации службы каталогов](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span><span class="sxs-lookup"><span data-stu-id="223df-133">Get the necessary permissions and prepare for directory synchronization, as described in [Prepare for directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308908).</span></span>
  
### <a name="to-synchronize-user-directories"></a><span data-ttu-id="223df-134">Синхронизация каталогов пользователей</span><span class="sxs-lookup"><span data-stu-id="223df-134">To synchronize user directories</span></span>

1. <span data-ttu-id="223df-135">Активируйте синхронизацию службы каталогов, как описано в статье, посвященной [активации синхронизации службы каталогов](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span><span class="sxs-lookup"><span data-stu-id="223df-135">Activate directory synchronization, as described in [Activate directory synchronization](https://go.microsoft.com/fwlink/p/?LinkId=308909).</span></span>
    
2. <span data-ttu-id="223df-136">Настройте свой компьютер для синхронизации службы каталогов, как описано в статье о [настройке компьютера для синхронизации службы каталогов](http://go.microsoft.com/fwlink/p/?LinkId=308911).</span><span class="sxs-lookup"><span data-stu-id="223df-136">Set up your directory synchronization computer, as described in [Set up your directory sync computer](http://go.microsoft.com/fwlink/p/?LinkId=308911).</span></span>
    
3. <span data-ttu-id="223df-137">Синхронизируйте каталоги, как описано в статье, посвященной [синхронизации каталогов с помощью мастера настройки](http://go.microsoft.com/fwlink/?LinkId=308912).</span><span class="sxs-lookup"><span data-stu-id="223df-137">Synchronize your directories, as described in [Use the Configuration Wizard to sync your directories](http://go.microsoft.com/fwlink/?LinkId=308912).</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="223df-p109">Когда Мастер настройки средства синхронизации Azure Active Directory завершит работу, учетная запись **MSOL_AD_SYNC** будет создана в вашем лесу Active Directory. Она используется для чтения и синхронизации локальных данных Active Directory. Чтобы каталоги синхронизировались правильно, убедитесь, что порт TCP 443 на локальном сервере синхронизации службы каталогов открыт.</span><span class="sxs-lookup"><span data-stu-id="223df-p109">When you finish the Azure Active Directory Sync Tool Configuration Wizard, the **MSOL_AD_SYNC** account is created in your Active Directory forest. This account is used to read and synchronize your on-premises Active Directory information. In order for directory synchronization to work correctly, make sure that TCP 443 on your local directory synchronization server is open.</span></span> 
  
4. <span data-ttu-id="223df-141">Активируйте синхронизированных пользователей, как описано в статье [Активация синхронизированных пользователей](http://go.microsoft.com/fwlink/p/?LinkId=308913).</span><span class="sxs-lookup"><span data-stu-id="223df-141">Activate synced users, as described in [Activate synced users](http://go.microsoft.com/fwlink/p/?LinkId=308913).</span></span>
    
5. <span data-ttu-id="223df-142">Управляйте синхронизацией службы каталогов, как описано в статье [Управление синхронизацией службы каталогов](http://go.microsoft.com/fwlink/p/?LinkId=308915).</span><span class="sxs-lookup"><span data-stu-id="223df-142">Manage directory synchronization, as described in [Manage directory synchronization](http://go.microsoft.com/fwlink/p/?LinkId=308915).</span></span>
    
6. <span data-ttu-id="223df-p110">Убедитесь, что синхронизация в службе EOP выполняется правильно. В Центре администрирования Exchange перейдите в раздел **Получатели** \> **Контакты** и убедитесь, что список пользователей с локальной среды должным образом синхронизирован.</span><span class="sxs-lookup"><span data-stu-id="223df-p110">Verify that EOP is synchronizing correctly. In the EAC, go to **Recipients** \> **Contacts** and view that the list of users was correctly synchronized from your on-premises environment.</span></span> 
    
## <a name="use-the-eac-to-manage-mail-users"></a><span data-ttu-id="223df-145">Управление почтовыми пользователями с помощью Центра администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="223df-145">Use the EAC to manage mail users</span></span>

<span data-ttu-id="223df-146">В этом разделе предоставлены сведения о добавлении пользователей электронной почты непосредственно в Центр администрирования Exchange и управлении ими.</span><span class="sxs-lookup"><span data-stu-id="223df-146">This section provides information about adding and managing email users directly in the EAC.</span></span>
  
 <span data-ttu-id="223df-147">**Приступая к работе**</span><span class="sxs-lookup"><span data-stu-id="223df-147">**Before you begin**</span></span>
  
<span data-ttu-id="223df-p111">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье Запись "Пользователи, контакты и группы ролей" в разделе [Разрешения на функции в службе EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="223df-p111">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
  
### <a name="to-add-a-mail-user-in-the-eac"></a><span data-ttu-id="223df-150">Добавление почтового пользователя в Центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="223df-150">To add a mail user in the EAC</span></span>

1. <span data-ttu-id="223df-151">Создайте пользователя электронной почты. Для этого перейдите в раздел **Получатели** \> **Контакты** в Центре администрирования Exchange, а затем нажмите кнопку **Создать +**.</span><span class="sxs-lookup"><span data-stu-id="223df-151">Create an email user by going to go to **Recipients** \> **Contacts** in the EAC, and then clicking **New +**.</span></span>
    
2. <span data-ttu-id="223df-152">На странице **Создание почтового пользователя** введите сведения о пользователе, в том числе приведенные ниже.</span><span class="sxs-lookup"><span data-stu-id="223df-152">On the **New mail user** page, enter the user's information, including the following:</span></span> 
    
   ****

|<span data-ttu-id="223df-153">**Свойство почтового пользователя**</span><span class="sxs-lookup"><span data-stu-id="223df-153">**Mail user property**</span></span>|<span data-ttu-id="223df-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="223df-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="223df-155">**Имя**, **Отчество** и **Фамилия**</span><span class="sxs-lookup"><span data-stu-id="223df-155">**First name**, **Initials**, and **Last name**</span></span> <br/> |<span data-ttu-id="223df-156">Введите полное имя пользователя в соответствующие поля.</span><span class="sxs-lookup"><span data-stu-id="223df-156">Type the user's full name in the appropriate boxes.</span></span>  <br/> |
|<span data-ttu-id="223df-157">**Отображаемое имя**</span><span class="sxs-lookup"><span data-stu-id="223df-157">**Display name**</span></span> <br/> |<span data-ttu-id="223df-p112">Введите имя до 64 символов в длину. По умолчанию в этом поле отображаются имена, введенные в поля **Имя**, **Инициалы** и **Фамилия** (при наличии). Отображаемое имя является обязательным параметром.  </span><span class="sxs-lookup"><span data-stu-id="223df-p112">Type a name, using up to 64 characters. By default, this box shows the names in the **First name**, **Initials**, and **Last name** boxes if any. The display name is required.  </span></span><br/> |
|<span data-ttu-id="223df-161">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="223df-161">**Alias**</span></span> <br/> |<span data-ttu-id="223df-p113">Введите уникальный псевдоним пользователя, содержащий до 64 символов. Псевдоним является обязательным параметром.</span><span class="sxs-lookup"><span data-stu-id="223df-p113">Type a unique alias, using up to 64 characters, for the user. The alias is required.</span></span>  <br/> |
|<span data-ttu-id="223df-164">**Внешний адрес электронной почты**</span><span class="sxs-lookup"><span data-stu-id="223df-164">**External email address**</span></span> <br/> |<span data-ttu-id="223df-165">Введите внешний адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="223df-165">Type the external email address of the user.</span></span>  <br/> |
|<span data-ttu-id="223df-166">**Идентификатор пользователя**</span><span class="sxs-lookup"><span data-stu-id="223df-166">**User id**</span></span> <br/> |<span data-ttu-id="223df-p114">Введите имя, с помощью которого почтовый пользователь будет входить в службу. Учетное имя пользователя состоит из имени пользователя, который находится слева от символа @, и суффикса справа от этого символа. Обычно в качестве суффикса выступает имя домена, в котором размещается учетная запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="223df-p114">Type the name that the mail user will use to sign in to the service. The user sign-in name consists of a user name on the left side of the at (@) symbol and a suffix on the right side. Typically, the suffix is the domain name in which the user account resides.</span></span>  <br/> |
|<span data-ttu-id="223df-170">**Новый пароль**</span><span class="sxs-lookup"><span data-stu-id="223df-170">**New password**</span></span> <br/> |<span data-ttu-id="223df-p115">Введите пароль, с помощью которого почтовый пользователь будет входить в службу. Убедитесь, что введенный пароль соответствует требованиям к длине, сложности и истории паролей, предъявляемым для домена, в котором создается учетная запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="223df-p115">Type the password that the mail user will use to sign in to the service. Make sure that the password you supply complies with the password length, complexity, and history requirements of the domain in which you're creating the user account.</span></span>  <br/> |
|<span data-ttu-id="223df-173">**Подтверждение пароля**</span><span class="sxs-lookup"><span data-stu-id="223df-173">**Confirm password**</span></span> <br/> |<span data-ttu-id="223df-174">Повторно введите пароль, чтобы подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="223df-174">Retype the password to confirm it.</span></span>  <br/> |
   
3. <span data-ttu-id="223df-p116">Нажмите кнопку **Сохранить**, чтобы создать нового пользователя электронной почты. Новый пользователь должен отобразиться в списке пользователей.</span><span class="sxs-lookup"><span data-stu-id="223df-p116">Click **Save** to create the new email user. The new user should appear in the list of users.</span></span> 
    
### <a name="to-edit-or-remove-a-mail-user-in-the-eac"></a><span data-ttu-id="223df-177">Изменение или удаление почтового пользователя в Центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="223df-177">To edit or remove a mail user in the EAC</span></span>

- <span data-ttu-id="223df-p117">В центре администрирования Exchange перейдите к разделу **получатели** \> **контактов**. В списке пользователей выберите пользователя, которого нужно просмотреть или изменить, а затем нажмите кнопку **изменить** ![значок](../media/ITPro-EAC-EditIcon.gif) редактирования, чтобы обновить параметры пользователя по мере необходимости. Вы можете изменить имя пользователя, псевдоним или контактные данные, а также указать подробные сведения о роли пользователя в Организации. Вы также можете выбрать пользователя и нажать кнопку **Удалить**![значок](../media/ITPro-EAC-RemoveIcon.gif) удалить, чтобы удалить его.</span><span class="sxs-lookup"><span data-stu-id="223df-p117">In the EAC, go to **Recipients** \> **Contacts**. In the list of users, click the user that you want to view or change, and then select **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif) to update the user settings as needed. You can change the user's name, alias, or contact information, and you can record detailed information about the user's role in the organization. You can also select a user and then choose **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif) to delete it.</span></span> 
    
## <a name="use-remote-windows-powershell-to-manage-mail-users"></a><span data-ttu-id="223df-182">Использование удаленной консоли Windows PowerShell для управления почтовыми пользователями</span><span class="sxs-lookup"><span data-stu-id="223df-182">Use remote Windows PowerShell to manage mail users</span></span>

<span data-ttu-id="223df-183">В этом разделе приведены сведения о добавлении почтовых пользователей и управлении ими с помощью удаленной консоли Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="223df-183">This section provides information about adding and managing mail users by using remote Windows PowerShell.</span></span>
  
 <span data-ttu-id="223df-184">**Приступая к работе**</span><span class="sxs-lookup"><span data-stu-id="223df-184">**Before you begin**</span></span>
  
- <span data-ttu-id="223df-p118">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье Запись "Пользователи, контакты и группы ролей" в разделе [Разрешения на функции в службе EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="223df-p118">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in [Feature permissions in EOP](feature-permissions-in-eop.md).</span></span>
    
- <span data-ttu-id="223df-187">Обратите внимание, что при создании почтовых пользователей с помощью командлетов удаленной консоли PowerShell вы можете столкнуться с регулированием.</span><span class="sxs-lookup"><span data-stu-id="223df-187">Be aware that when creating mail users by using remote PowerShell cmdlets, you may encounter throttling.</span></span>
    
- <span data-ttu-id="223df-188">Этот командлет использует метод пакетной обработки, из-за чего результаты его выполнения становятся видны через несколько минут.</span><span class="sxs-lookup"><span data-stu-id="223df-188">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span>
    
- <span data-ttu-id="223df-189">Сведения об использовании Windows PowerShell для подключения к службе Exchange Online Protection см. в статье [Подключение к Exchange Online Protection с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span><span class="sxs-lookup"><span data-stu-id="223df-189">To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection Using Remote PowerShell](http://technet.microsoft.com/library/054e0fd7-d465-4572-93f8-a00a9136e4d1.aspx).</span></span>
    
 <span data-ttu-id="223df-190">**Добавление почтового пользователя с помощью удаленной консоли PowerShell**</span><span class="sxs-lookup"><span data-stu-id="223df-190">**To add a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="223df-191">В этом примере с помощью командлета [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) создается учетная запись пользователя с включенной поддержкой почты в EOP для Григория Иванова с такими сведениями:</span><span class="sxs-lookup"><span data-stu-id="223df-191">This example uses the [New-EOPMailUser](http://technet.microsoft.com/library/0520cf33-4ad0-44e4-99a3-1b485739fc05.aspx) cmdlet to create a mail-enabled user account for Jeffrey Zeng in EOP with the following details:</span></span> 
  
- <span data-ttu-id="223df-192">Имя  Григорий, фамилия  Иванов.</span><span class="sxs-lookup"><span data-stu-id="223df-192">The first name is Jeffrey and the last name is Zeng.</span></span>
    
- <span data-ttu-id="223df-193">Имя  Григорий, отображаемое имя  Григорий Иванов.</span><span class="sxs-lookup"><span data-stu-id="223df-193">The name is Jeffrey and the display name is Jeffrey Zeng.</span></span>
    
- <span data-ttu-id="223df-194">Псевдоним  gregoryiv.</span><span class="sxs-lookup"><span data-stu-id="223df-194">The alias is jeffreyz.</span></span>
    
- <span data-ttu-id="223df-195">Внешний адрес электронной почты  givanov@tailspintoys.com.</span><span class="sxs-lookup"><span data-stu-id="223df-195">The external email address is jzeng@tailspintoys.com.</span></span>
    
- <span data-ttu-id="223df-196">Имя входа в Office 365  gregoryiv@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="223df-196">The Office 365 sign in name is jeffreyz@contoso.onmicrosoft.com.</span></span>
    
- <span data-ttu-id="223df-197">Пароль  Pa$$word1.</span><span class="sxs-lookup"><span data-stu-id="223df-197">The password is Pa$$word1.</span></span>
    
```
New-EOPMailUser -LastName Zeng -FirstName Jeffrey -DisplayName "Jeffrey Zeng" -Name Jeffrey -Alias jeffreyz -MicrosoftOnlineServicesID jeffreyz@contoso.onmicrosoft.com -ExternalEmailAddress jeffreyz@tailspintoys.com -Password (ConvertTo-SecureString -String 'Pa$$word1' -AsPlainText -Force)
```

 <span data-ttu-id="223df-198">**Проверка функционирования**</span><span class="sxs-lookup"><span data-stu-id="223df-198">**To verify that this worked**</span></span>
  
<span data-ttu-id="223df-199">Чтобы отобразить сведения о новом почтовом пользователе Григории Иванове, запустите командлет [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx):</span><span class="sxs-lookup"><span data-stu-id="223df-199">Run the [Get-User](http://technet.microsoft.com/library/2a33c9e6-33da-438c-912d-28ce3f4c9afb.aspx) cmdlet as follows to display information about new mail user Jeffrey Zeng:</span></span> 
  
```
Get-User "Jeffrey Zeng"

```

 <span data-ttu-id="223df-200">**Изменение свойств почтового пользователя с помощью удаленной консоли PowerShell**</span><span class="sxs-lookup"><span data-stu-id="223df-200">**To edit the properties of a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="223df-201">Просматривайте и изменяйте свойства почтовых пользователей с помощью командлетов [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) и [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx).</span><span class="sxs-lookup"><span data-stu-id="223df-201">Use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) and [Set-EOPMailUser](http://technet.microsoft.com/library/834c3de6-1485-4d50-bb96-262a2c0c8619.aspx) cmdlets to view or change properties for mail users.</span></span> 
  
<span data-ttu-id="223df-202">В этом примере настраивается внешний адрес электронной почты для пользователя Марты Артемьевой.</span><span class="sxs-lookup"><span data-stu-id="223df-202">This example sets the external email address for Pilar Pinilla.</span></span>
  
```
Set-EOPMailUser -Identity "Pilar Pinilla" -EmailAddresses pilarp@tailspintoys.com
```

<span data-ttu-id="223df-203">В этом примере значение "Компания" задано как Contoso для всех почтовых пользователей.</span><span class="sxs-lookup"><span data-stu-id="223df-203">This example sets the Company property for all mail users to Contoso.</span></span>
  
```
$Recip = Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')}
$Recip | foreach {Set-EOPUser -Identity $_.Alias -Company Contoso}

```

 <span data-ttu-id="223df-204">**Проверка функционирования**</span><span class="sxs-lookup"><span data-stu-id="223df-204">**To verify that this worked**</span></span>
  
<span data-ttu-id="223df-p119">В предыдущем примере мы изменили свойства почтового пользователя Марты Артемьевой. Проверьте изменения с помощью командлета [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx). (Обратите внимание, что можно просматривать несколько свойств нескольких почтовых контактов.)</span><span class="sxs-lookup"><span data-stu-id="223df-p119">In the previous example where we changed the properties for mail user Pilar Pinella, use the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet to verify the changes. (Note that you can view multiple properties for multiple mail contacts.)</span></span> 
  
```
Get-Recipient -Identity "Pilar Pinilla" | Format-List 

```

<span data-ttu-id="223df-207">Проверьте изменения из предыдущего примера, в котором для свойства "Компания" было задано значение Contoso для всех пользователей почты. Для этого выполните такую команду:</span><span class="sxs-lookup"><span data-stu-id="223df-207">In the previous example where the Company property was set to Contoso for all mail users, run the following command to verify the changes:</span></span>
  
```
Get-Recipient -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'mailuser')} | Format-List Name,Company
```

> [!IMPORTANT]
> <span data-ttu-id="223df-208">Этот командлет использует метод пакетной обработки, из-за чего результаты его выполнения становятся видны через несколько минут.</span><span class="sxs-lookup"><span data-stu-id="223df-208">This cmdlet uses a batch processing method that results in a propagation delay of a few minutes before the results of the cmdlet are visible.</span></span> 
  
 <span data-ttu-id="223df-209">**Удаление почтового пользователя с помощью удаленной консоли PowerShell**</span><span class="sxs-lookup"><span data-stu-id="223df-209">**To remove a mail user using remote PowerShell**</span></span>
  
<span data-ttu-id="223df-210">В этом примере командлет [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) используется для удаления пользователя Григория Иванова:</span><span class="sxs-lookup"><span data-stu-id="223df-210">This example uses the [Remove-EOPMailUser](http://technet.microsoft.com/library/cb91dc26-ed22-4d3c-9f64-df9df1754edb.aspx) cmdlet to delete user Jeffrey Zeng:</span></span> 
  
```
Remove-EOPMailUser -Identity Jeffrey
```

 <span data-ttu-id="223df-211">**Проверка функционирования**</span><span class="sxs-lookup"><span data-stu-id="223df-211">**To verify that this worked**</span></span>
  
<span data-ttu-id="223df-p120">Запустите командлет [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx), как описано далее. Должно отобразиться сообщение об ошибке, так как этот пользователь больше не существует.</span><span class="sxs-lookup"><span data-stu-id="223df-p120">Run the [Get-Recipient](http://technet.microsoft.com/library/2ce6250f-0ad3-4b29-870c-e1d6e1e154bc.aspx) cmdlet as follows. You should get an error message since the user no longer exists.</span></span> 
  
```
Get-Recipient Jeffrey | fl
```


