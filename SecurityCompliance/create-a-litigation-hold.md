---
title: Создание удержания для судебного разбирательства в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: f2d3793eac84e8f80158842c833c30986b0549c5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218659"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="79a65-102">Создание удержания для судебного разбирательства в Office 365</span><span class="sxs-lookup"><span data-stu-id="79a65-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="79a65-p101">Вы можете поместить почтовый ящик на хранение для судебного разбирательства, чтобы сохранить все содержимое почтового ящика, включая удаленные элементы и исходные версии измененных элементов. При помещении почтового ящика пользователя на хранение для судебного разбирательства также сохраняется содержимое архивного почтового ящика пользователя (если он включен). При создании удержания можно указать продолжительность удержания (также называемую *удержанием на основе времени*), чтобы удаленные и измененные элементы сохранялись в течение указанного периода, а затем окончательно удалены из почтового ящика. Или вы можете просто хранить контент в неопределенном состоянии (называемом бесконечное *удержание*) или пока не будет удалено удержание для судебного разбирательства. Если указать период хранения, он вычисляется с момента получения сообщения или создания элемента почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="79a65-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="79a65-108">Ниже показано, что происходит при создании удержания для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="79a65-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="79a65-109">Элементы, которые пользователь навсегда удаляет, сохраняются в папке "элементы с возможностью восстановления" в почтовом ящике пользователя в течение периода удержания.</span><span class="sxs-lookup"><span data-stu-id="79a65-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="79a65-110">Элементы, которые удаляются из папки "элементы с возможностью восстановления", сохраняются в течение срока хранения.</span><span class="sxs-lookup"><span data-stu-id="79a65-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="79a65-111">Квота хранилища для папки "элементы с возможностью восстановления" увеличивается с 30 ГБ до 110 ГБ.</span><span class="sxs-lookup"><span data-stu-id="79a65-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="79a65-112">Элементы в основном пользователе и архивные почтовые ящики сохраняются</span><span class="sxs-lookup"><span data-stu-id="79a65-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="79a65-113">Подготовка</span><span class="sxs-lookup"><span data-stu-id="79a65-113">Before you begin</span></span>

- <span data-ttu-id="79a65-p102">Чтобы поместить почтовый ящик Exchange Online на удержание для судебного разбирательства, ему необходимо назначить лицензию на Exchange Online (план 2). Если почтовому ящику назначена лицензия на Exchange Online (план 1), необходимо назначить ему отдельную лицензию на архивацию на базе Exchange Online, чтобы разместить ее на удержании.</span><span class="sxs-lookup"><span data-stu-id="79a65-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="79a65-116">Помещение почтового ящика на удержание для судебного разбирательства в центре администрирования Office 365</span><span class="sxs-lookup"><span data-stu-id="79a65-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="79a65-117">Ниже описаны действия, которые необходимо выполнить, чтобы поместить маибокс на удержание для судебного разбирательства с помощью центра администрирования Office 365.</span><span class="sxs-lookup"><span data-stu-id="79a65-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="79a65-118">Войдите в https://portal.office.com/adminportal/home систему, используя свою учетную запись глобального администратора.</span><span class="sxs-lookup"><span data-stu-id="79a65-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="79a65-119">Щелкните **Пользователи** > **Активные пользователи** в левой области навигации.</span><span class="sxs-lookup"><span data-stu-id="79a65-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="79a65-120">Выберите пользователя, чей почтовый ящик вы хотите поместить на удержание для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="79a65-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="79a65-121">На странице "выпадающее сообщение" щелкните **Параметры почты**, а затем нажмите кнопку **изменить** рядом с пунктом **удержание для судебного разбирательства**.</span><span class="sxs-lookup"><span data-stu-id="79a65-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="79a65-122">На странице " **удержание** для судебного разбирательства" щелкните переключатель, чтобы включить удержание для судебного разбирательства и заполните следующие необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="79a65-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1. png](media/O365-LitigationHold1.png)

    <span data-ttu-id="79a65-p103">**срок хранения (дни)** — это поле используется для создания удержаний на основе времени и определения продолжительности хранения элементов почтовых ящиков при включении почтового ящика на хранение для судебного разбирательства. Продолжительность рассчитывается от даты получения или создания элемента почтового ящика. Если оставить это поле пустым, элементы будут храниться в течение неограниченного времени или до удаления удержания. Используйте дни, чтобы указать длительность.</span><span class="sxs-lookup"><span data-stu-id="79a65-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="79a65-p104">b. **Примечание** . это поле используется для информирования пользователя о своем почтовом ящике на удержание для судебного разбирательства. Примечание появится на странице сведения об учетной записи в почтовом ящике пользователя, если они используют Outlook 2010 или более поздней версии. Для доступа к этой странице пользователи могут щелкнуть **файл** в Outlook.</span><span class="sxs-lookup"><span data-stu-id="79a65-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="79a65-p105">c. **Web Page** — это поле используется для направления пользователя на веб-сайт для получения дополнительных сведений о удержании судебного разбирательства. Этот URL-адрес отображается на странице "сведения об учетной записи" в почтовом ящике пользователя, если они используют Outlook 2010 или более поздней версии. Для доступа к этой странице пользователи могут щелкнуть **файл** в Outlook.</span><span class="sxs-lookup"><span data-stu-id="79a65-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="79a65-137">Нажмите кнопку **сохранить** , чтобы создать удержание для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="79a65-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="79a65-138">После создания удержания параметры почты на выпадающем окне показывают, что для выбранного пользователя включено удержание для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="79a65-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2. png](media/O365-LitigationHold2.png)

<span data-ttu-id="79a65-140">Дополнительные сведения о создании и управлении судебным удержанием и использовании Exchange Online PowerShell для массового создания судебного удержания см. в разделе [Помещение почтового ящика на удержание для судебНого разбирательства](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span><span class="sxs-lookup"><span data-stu-id="79a65-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>
