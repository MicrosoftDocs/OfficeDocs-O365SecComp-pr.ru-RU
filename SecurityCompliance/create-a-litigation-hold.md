---
title: Создание хранение для судебного разбирательства в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 39db1659-0b12-4243-a21c-2614512dcb44
ms.openlocfilehash: aa78d12046108aa1f1b974f01c02ff923b99b97b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25037962"
---
# <a name="create-a-litigation-hold-in-office-365"></a><span data-ttu-id="d096f-102">Создание хранение для судебного разбирательства в Office 365</span><span class="sxs-lookup"><span data-stu-id="d096f-102">Create a Litigation Hold in Office 365</span></span>

<span data-ttu-id="d096f-p101">Можно поместить почтовый ящик на хранение для судебного разбирательства для сохранения все содержимое почтового ящика, включая удаленных элементов и оригинальных версий измененных элементов. При выполнении почтового ящика пользователя на хранение для судебного разбирательства контента в архивный почтовый ящик пользователя (если он включен) также сохраняется. При создании удержания можно указать продолжительность удержания (также называемая *Удержание по времени*), чтобы удалить и измененные элементы сохраняются в течение заданного периода и окончательно удаляется из почтового ящика. Или можно просто сохранить содержимое неопределенное время (называемые *неограниченное удержание*) или пока не будет снято хранение для судебного разбирательства. Если указать продолжительность периода удержания, рассчитывается от даты выдается сообщение или создания элемента почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="d096f-p101">You can place a mailbox on Litigation Hold to retain all mailbox content, including deleted items and the original versions of modified items. When you place a user mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also retained. When you create a hold, you can specify a hold duration (also called a *time-based hold*) so that deleted and modified items are retained for a specified period and then permanently deleted from the mailbox. Or you can just retain content indefinitely (called an *infinite hold*) or until the Litigation Hold is removed. If you do specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> 
  
<span data-ttu-id="d096f-108">Вот что происходит при создании хранение для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="d096f-108">Here's what happens when you create a Litigation Hold.</span></span>
  
- <span data-ttu-id="d096f-109">Элементы, которые будут удалены пользователем, сохраняются в папке папки в почтовом ящике пользователя во время выполнения удержания.</span><span class="sxs-lookup"><span data-stu-id="d096f-109">Items that are permanently deleted by the user are retained in the Recoverable Items folder in the user's mailbox for the duration of the hold.</span></span>
    
- <span data-ttu-id="d096f-110">Элементы, удаленные из папки элементов для восстановления пользователем, сохраняются в течение удержания.</span><span class="sxs-lookup"><span data-stu-id="d096f-110">Items that are purged from the Recoverable Items folder by the user are retained for the duration of the hold.</span></span>
    
- <span data-ttu-id="d096f-111">Квота хранилища для папки элементов для восстановления увеличено с 30 ГБ до 110 ГБ.</span><span class="sxs-lookup"><span data-stu-id="d096f-111">The storage quota for the Recoverable Items folder is increased from 30 GB to 110 GB.</span></span>
    
- <span data-ttu-id="d096f-112">Сохраняются элементы в главный пользователя и архивные почтовые ящики</span><span class="sxs-lookup"><span data-stu-id="d096f-112">Items in the user's primary and the archive mailboxes are retained</span></span>
    
## <a name="before-you-begin"></a><span data-ttu-id="d096f-113">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="d096f-113">Before you begin</span></span>

- <span data-ttu-id="d096f-p102">Чтобы поставить почтовый ящик Exchange Online на хранение для судебного разбирательства, она должна быть назначена лицензия на Exchange Online (план 2). Если почтовый ящик назначена лицензия на Exchange Online план 1, необходимо назначить его отдельная лицензия архивации Exchange Online чтобы поставить на удержание.</span><span class="sxs-lookup"><span data-stu-id="d096f-p102">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online Plan 2 license. If a mailbox is assigned an Exchange Online Plan 1 license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    

## <a name="place-a-mailbox-on-litigation-hold-in-the-office-365-admin-center"></a><span data-ttu-id="d096f-116">Постановка почтового ящика на хранение для судебного разбирательства в центре администрирования Office 365</span><span class="sxs-lookup"><span data-stu-id="d096f-116">Place a mailbox on Litigation Hold in the Office 365 admin center</span></span>

<span data-ttu-id="d096f-117">Далее приведены шаги для помещения maibox на хранение для судебного разбирательства с помощью центра администрирования Office 365.</span><span class="sxs-lookup"><span data-stu-id="d096f-117">Here are the steps to place a maibox on Litigation Hold using the Office 365 admin center.</span></span>

1. <span data-ttu-id="d096f-118">Последовательно выберите пункты https://portal.office.com/adminportal/home и выполнить вход с помощью учетной записи глобального администратора.</span><span class="sxs-lookup"><span data-stu-id="d096f-118">Go to https://portal.office.com/adminportal/home and sign in using your global administrator account.</span></span>
2. <span data-ttu-id="d096f-119">Щелкните элемент **Пользователи** > **активных пользователей** в левой области навигации.</span><span class="sxs-lookup"><span data-stu-id="d096f-119">Click **Users** > **Active users** in the left navigation pane.</span></span>
3. <span data-ttu-id="d096f-120">Выберите пользователя, почтовый ящик, для которого требуется поместить на хранение для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="d096f-120">Select the user whose mailbox you want to place on Litigation Hold.</span></span>
4. <span data-ttu-id="d096f-121">На странице "плавающее" нажмите кнопку **Параметры электронной почты**и нажмите кнопку **Изменить** рядом с пунктом **хранение для судебного разбирательства**.</span><span class="sxs-lookup"><span data-stu-id="d096f-121">On the fly-out page, click **Mail settings**, and then click **Edit** next to **Litigation hold**.</span></span>
5. <span data-ttu-id="d096f-122">На странице **хранение для судебного разбирательства** выберите переключатель, чтобы включить хранение для судебного разбирательства и выполните следующие необязательные параметры, которые отображаются:</span><span class="sxs-lookup"><span data-stu-id="d096f-122">On the **Litigation hold** page, click the toggle to turn on Litigation Hold and complete the following optional settings that are displayed:</span></span>
 
    ![O365_LitigationHold1.PNG](media/O365-LitigationHold1.png)

    <span data-ttu-id="d096f-p103">a. **ареста (дней)** — это поле используется для создания удержания на основе времени и укажите, как долго сохраняются элементы почтового ящика при размещении почтовый ящик на хранение для судебного разбирательства. Во время выполнения рассчитывается из даты, полученного или созданного элемента почтового ящика. Если оставить это поле пустым, элементы хранятся неограниченное время или пока не будет снято удержание. Используйте дней, чтобы указать во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d096f-p103">a. **Hold duration (days)** - Use this box to create a time-based hold and specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span>
    
    <span data-ttu-id="d096f-p104">б. **Примечание** — это поле используется для оповещения пользователя, почтовый ящик находится на хранение для судебного разбирательства. Если при использовании Outlook 2010 или более поздняя версия Примечание будет отображаться на странице сведения об учетной записи в почтовом ящике пользователя. Для доступа к этой странице, пользователи могут щелкнуть **файл** в Outlook.</span><span class="sxs-lookup"><span data-stu-id="d096f-p104">b. **Note** - Use this box to inform the user their mailbox is on Litigation Hold. The note will appear on the Account Information page in the user's mailbox if they're using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
     
    <span data-ttu-id="d096f-p105">c. **веб-страницы** — это поле используется для направления пользователя веб-сайта, Дополнительные сведения о хранение для судебного разбирательства. Этот URL-адрес отображается на странице сведения об учетной записи в почтовом ящике пользователя, если они используют Outlook 2010 или более поздней версии. Для доступа к этой странице, пользователи могут щелкнуть **файл** в Outlook.</span><span class="sxs-lookup"><span data-stu-id="d096f-p105">c. **Web page** - Use this box to direct the user to a website for more information about Litigation Hold. This URL appears on the Account Information page in the user's mailbox if they are using Outlook 2010 or later. To access this page, users can click **File** in Outlook.</span></span>
 
6. <span data-ttu-id="d096f-137">Нажмите кнопку **Сохранить** , чтобы создать хранение для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="d096f-137">Click **Save** to create the Litigation Hold.</span></span>

<span data-ttu-id="d096f-138">После создания удержания, параметры электронной почты на странице раскрывающимися показывает, что хранение для судебного разбирательства включена для выбранного пользователя.</span><span class="sxs-lookup"><span data-stu-id="d096f-138">After you create the hold, the mail settings on the fly-out page shows that Litigation Hold is turned on for the selected user.</span></span>

![O365_LitigationHold2.PNG](media/O365-LitigationHold2.png)

<span data-ttu-id="d096f-140">Дополнительные сведения о создании и управлении Судебное удержание и Массовое создание Судебное удержание с помощью Exchange Online PowerShell просмотра [позиции почтовых ящиков на хранение для судебного разбирательства](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span><span class="sxs-lookup"><span data-stu-id="d096f-140">For more information about creating and managing Litigation Holds and using Exchange Online PowerShell to bulk-create Litigation Holds, see [Place a mailbox on Litigation Hold](https://docs.microsoft.com/office365/SecurityCompliance/place-a-mailbox-on-litigation-hold).</span></span>
