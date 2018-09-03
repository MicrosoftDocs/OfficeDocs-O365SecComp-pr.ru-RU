---
title: Общие сведения о неограниченном архивировании в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Узнайте о развертываемым архивации в Office 365, которая позволяет неограниченное архивного хранилища для почтовых ящиков Exchange Online.
ms.openlocfilehash: a762a0fb8295a645957404c1c88881f40329f7a1
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782126"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a><span data-ttu-id="ffb56-103">Общие сведения о неограниченном архивировании в Office 365</span><span class="sxs-lookup"><span data-stu-id="ffb56-103">Overview of unlimited archiving in Office 365</span></span>

<span data-ttu-id="ffb56-p101">В Office 365 архивные почтовые ящики предоставляют пользователям дополнительного почтового ящика дискового пространства. После включения архивного почтового ящика пользователя до 100 ГБ дополнительного хранилища доступен. При достижении квота хранилища 100 ГБ организаций были вынуждены обратитесь в Майкрософт для запроса дополнительной дискового пространства для архивного почтового ящика. Это больше не так. Новая функция неограниченное архивации в Office 365 (называемые *развертываемым архивации*) предоставляет не ограничен объем хранилища в архивных почтовых ящиков. Теперь при достижении квота хранилища в архивный почтовый ящик Office 365 автоматически увеличивается размер архива, что означает, что пользователи не будут выполняться недостаточно дискового пространства для сохранения почтовых ящиков, и администраторы не потребуется запросить дополнительное хранилище для архивных почтовых ящиков .</span><span class="sxs-lookup"><span data-stu-id="ffb56-p101">In Office 365, archive mailboxes provide users with additional mailbox storage space. After a user's archive mailbox is enabled, up to 100 GB of additional storage is available. When the 100 GB storage quota is reached, organizations had to contact Microsoft to request additional storage space for an archive mailbox. That's no longer the case. The new unlimited archiving feature in Office 365 (called *auto-expanding archiving*) provides an unlimited amount of storage in archive mailboxes. Now, when the storage quota in the archive mailbox is reached, Office 365 automatically increases the size of the archive, which means that users won't run out of mailbox storage space and administrators won't have to request additional storage for archive mailboxes.</span></span>
  
<span data-ttu-id="ffb56-110">Пошаговые инструкции для включения развертываемым архивации, см [неограниченном архивировании в Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="ffb56-110">For step-by-step instructions for turning on auto-expanding archiving, see [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="ffb56-p102">Автоматическое развертывание архивации также поддерживает общие почтовые ящики. Чтобы включить в архив для общего почтового ящика, лицензии Exchange Online (план 2) или лицензии Exchange Online план 1 с лицензией архивации Exchange Online является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ffb56-p102">Auto-expanding archiving also supports shared mailboxes. To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span> 
  
## <a name="how-auto-expanding-archiving-works"></a><span data-ttu-id="ffb56-113">Как развертываемым работы архивации</span><span class="sxs-lookup"><span data-stu-id="ffb56-113">How auto-expanding archiving works</span></span>

<span data-ttu-id="ffb56-p103">Как объяснялось ранее, дополнительные почтовый ящик дискового пространства для сохранения создается при включении архивного почтового ящика пользователя. При включении развертываемым архивации Office 365 периодически проверяет размер архивного почтового ящика. При архивного почтового ящика приближается к ограничению для хранилища, Office 365 автоматически создает дополнительные дискового пространства для архива. Если пользователь запускает из этого пространства дополнительное хранилище, Office 365 добавляет больше места для хранения архива пользователя. Это происходит автоматически, что означает, что администраторы не имеют для запроса дополнительной архивного хранилища или управление развертываемым архивации.</span><span class="sxs-lookup"><span data-stu-id="ffb56-p103">As previously explained, additional mailbox storage space is created when a user's archive mailbox is enabled. When auto-expanding archiving is enabled, Office 365 periodically checks the size of the archive mailbox. When an archive mailbox gets close to its storage limit, Office 365 automatically creates additional storage space for the archive. If the user runs out of this additional storage space, Office 365 adds more storage space to the user's archive. This process happens automatically, which means administrators don't have to request additional archive storage or manage auto-expanding archiving.</span></span> 
  
<span data-ttu-id="ffb56-119">Ниже приведен краткий обзор процесса.</span><span class="sxs-lookup"><span data-stu-id="ffb56-119">Here's a quick overview of the process.</span></span>
  
![Обзор процесса развертываемым архивации](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. <span data-ttu-id="ffb56-p104">Архивация включена для почтового ящика пользователя или общего почтового ящика. Создать архивный почтовый ящик с 100 ГБ дискового пространства, квота предупреждений для архивного почтового ящика задано значение 90 ГБ.</span><span class="sxs-lookup"><span data-stu-id="ffb56-p104">Archiving is enabled for a user mailbox or a shared mailbox. An archive mailbox with 100 GB of storage space is created, and the warning quota for the archive mailbox is set to 90 GB.</span></span>
    
2. <span data-ttu-id="ffb56-p105">Администратор включает развертываемым архивацию для почтового ящика. Затем по достижении 90 ГБ (включая папки элементов для восстановления) архивный почтовый ящик преобразуется в архиве развертываемым и Office 365 добавляет дискового пространства для сохранения в архив. Обратите внимание на то, что может потребоваться до 30 дней дополнительные дискового пространства для подготовить к работе.</span><span class="sxs-lookup"><span data-stu-id="ffb56-p105">An administrator enables auto-expanding archiving for the mailbox. Then, when the archive mailbox (including the Recoverable Items folder) reaches 90 GB, it's converted to an auto-expanding archive, and Office 365 adds storage space to the archive. Note that it can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
3. <span data-ttu-id="ffb56-126">Office 365 автоматически добавляет больше места для хранения в архив при необходимости.</span><span class="sxs-lookup"><span data-stu-id="ffb56-126">Office 365 automatically adds more storage space to the archive when necessary.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ffb56-p106">Если почтовый ящик в режим ожидания или назначенные политики хранения к Office 365, квоту хранилища для архива maibox увеличивается до 110 ГБ при включенном развертываемым архивации. Аналогично Квота предупреждений для архива увеличивается до 100 ГБ.</span><span class="sxs-lookup"><span data-stu-id="ffb56-p106">If a mailbox is placed on hold or assigned to an Office 365 retention policy, the storage quota for the archive maibox is increased to 110 GB when auto-expanding archiving is enabled. Similarly, the archive warning quota is increased to 100 GB.</span></span>

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a><span data-ttu-id="ffb56-129">Что получает перемещено в пространстве для хранения дополнительных архив?</span><span class="sxs-lookup"><span data-stu-id="ffb56-129">What gets moved to the additional archive storage space?</span></span>

<span data-ttu-id="ffb56-p107">Чтобы эффективно использовать развертываемым архивного хранилища, может получить перемещены папок. Office 365 определяет, какие папки могут перемещаться дополнительное хранилище добавляется в архив. При перемещении папки вложенной папке создается автоматически в исходной папке в архив часть к списку папок в Outlook. В этой новой папке указывает на элементы, которые были перемещены. Соглашение об именовании, назовите эту папку с помощью Office 365 — это ** \<имя папки\>_yyyy (созданной на ммм дд, гггг h_mm)**, где:</span><span class="sxs-lookup"><span data-stu-id="ffb56-p107">To make efficient use of auto-expanding archive storage, folders might get moved. Office 365 determines which folders get moved when additional storage is added to the archive. When a folder is moved, a subfolder is automatically created under the original folder in the archive portion of the folder list in Outlook. This new subfolder points to the items that were moved. The naming convention that Office 365 uses to name this folder is **\<folder name\>_yyyy (Created on mmm dd, yyyy h_mm)**, where:</span></span> 
  
- <span data-ttu-id="ffb56-135">**гггг** — год, в котором были получены сообщения в папке.</span><span class="sxs-lookup"><span data-stu-id="ffb56-135">**yyyy** is the year the messages in the folder were received.</span></span> 
    
- <span data-ttu-id="ffb56-136">**мммм дд, гггг h_m** — это дата и время создания вложенной папке с Office 365, в формате UTC, на основе часовой пояс пользователя и региональных параметров в Outlook.</span><span class="sxs-lookup"><span data-stu-id="ffb56-136">**mmm dd, yyyy h_m** is the date and time that the subfolder was created by Office 365, in UTC format, based on the user's time zone and regional settings in Outlook.</span></span> 
    
<span data-ttu-id="ffb56-137">На следующих снимках экрана в списке папок до и после перемещения сообщений в архиве автоматически расширяется.</span><span class="sxs-lookup"><span data-stu-id="ffb56-137">The following screen shots show a folder list before and after messages are moved in an auto-expanded archive.</span></span>
  
 <span data-ttu-id="ffb56-138">**Перед добавлением дополнительное хранилище**</span><span class="sxs-lookup"><span data-stu-id="ffb56-138">**Before additional storage is added**</span></span>
  
![Список папок из архивного почтового ящика перед развертываемым архив подготовить к работе](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 <span data-ttu-id="ffb56-140">**После добавления дополнительное хранилище**</span><span class="sxs-lookup"><span data-stu-id="ffb56-140">**After additional storage is added**</span></span>
  
![Список папок из архивного почтового ящика после подготовки развертываемым архива](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a><span data-ttu-id="ffb56-142">Требования к Outlook для доступа к элементам в архиве автоматически расширяется</span><span class="sxs-lookup"><span data-stu-id="ffb56-142">Outlook requirements for accessing items in an auto-expanded archive</span></span>

<span data-ttu-id="ffb56-143">Для доступа к сообщениям, которые хранятся в архиве автоматически расширяется, пользователям нужно использовать один из следующих клиентах Outlook:</span><span class="sxs-lookup"><span data-stu-id="ffb56-143">To access messages that are stored in an auto-expanded archive, users have to use one of the following Outlook clients:</span></span>
  
- <span data-ttu-id="ffb56-144">Outlook 2016 для Windows</span><span class="sxs-lookup"><span data-stu-id="ffb56-144">Outlook 2016 for Windows</span></span>
    
- <span data-ttu-id="ffb56-145">Outlook в Интернете;</span><span class="sxs-lookup"><span data-stu-id="ffb56-145">Outlook on the web</span></span> 
    
- <span data-ttu-id="ffb56-146">Outlook 2016 для Mac;</span><span class="sxs-lookup"><span data-stu-id="ffb56-146">Outlook 2016 for Mac</span></span> 
    
> [!NOTE]
> <span data-ttu-id="ffb56-p108">Outlook 2013 пользователи могут только доступа к элементам, которые были сохранены в их архивного почтового ящика. Они не сможет для доступа к элементам, которые перемещаются в дополнительных архивного хранилища.</span><span class="sxs-lookup"><span data-stu-id="ffb56-p108">Outlook 2013 users can only access items that were originally stored in their archive mailbox. They won't be able to access items that are moved to additional archive storage.</span></span> 
  
<span data-ttu-id="ffb56-149">Ниже приведены некоторые факторы, которые следует учитывать при использовании Outlook или Outlook в Интернете на получение доступа к сообщениям, которые хранятся в архиве автоматически расширяется.</span><span class="sxs-lookup"><span data-stu-id="ffb56-149">Here are some things to consider when using Outlook or Outlook on the web to access messages stored in an auto-expanded archive.</span></span>
  
- <span data-ttu-id="ffb56-150">Можно получить доступ к любой папки в почтовом ящике пользователя архива, включая объекты, которые были перемещены в область хранения автоматически расширяется.</span><span class="sxs-lookup"><span data-stu-id="ffb56-150">You can access any folder in your archive mailbox, including ones that were moved to the auto-expanded storage area.</span></span>
    
- <span data-ttu-id="ffb56-p109">Можно выполнить поиск для элементов, которые были перемещены в области дополнительное хранилище только по словам к самой папке. Это означает, что необходимо выбрать папку архива в списке папок, выберите вариант **Текущую папку** в качестве области поиска. Аналогично Если папки в области хранения автоматически расширяется содержит вложенные папки, необходимо выполните поиск каждой вложенной папке отдельно.</span><span class="sxs-lookup"><span data-stu-id="ffb56-p109">You can search for items that were moved to an additional storage area only by searching the folder itself. This means you have to select the archive folder in the folder list to select the **Current Folder** option as the search scope. Similarly, if a folder in an auto-expanded storage area contains subfolders, you have to search each subfolder separately.</span></span> 
    
- <span data-ttu-id="ffb56-154">Число элементов в Outlook и счетчики чтения/непрочитанные (в Outlook и Outlook в Интернете) в архиве автоматически расширяется не может быть точным.</span><span class="sxs-lookup"><span data-stu-id="ffb56-154">Item counts in Outlook and Read/Unread counts (in Outlook and Outlook on the web ) in an auto-expanded archive might not be accurate.</span></span>
    
- <span data-ttu-id="ffb56-155">Можно удалить элементы во вложенной папке, указывающий на область автоматически расширяется хранилища, но не может быть удален к самой папке.</span><span class="sxs-lookup"><span data-stu-id="ffb56-155">You can delete items in a subfolder that points to an auto-expanded storage area, but the folder itself can't be deleted.</span></span>
    
- <span data-ttu-id="ffb56-156">Восстановление удаленных элементов компонента нельзя использовать для восстановления элемента, который был удален из области автоматически расширяется хранилища.</span><span class="sxs-lookup"><span data-stu-id="ffb56-156">You can't use the Recover Deleted Items feature to recover an item that was deleted from an auto-expanded storage area.</span></span>
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a><span data-ttu-id="ffb56-157">Автоматическое развертывание архивации и другие функции контроля соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="ffb56-157">Auto-expanding archiving and other Office 365 compliance features</span></span>

<span data-ttu-id="ffb56-158">В этом разделе объясняется принцип взаимодействия развертываемым архивации и другие соответствия требованиям Office 365 и компоненты управления данными.</span><span class="sxs-lookup"><span data-stu-id="ffb56-158">This section explains the functionality between auto-expanding archiving and other Office 365 compliance and data governance features.</span></span>
  
- <span data-ttu-id="ffb56-159">**Обнаружение электронных данных** — при использовании средство обнаружения электронных данных для Office 365, например поиска контента или In-Place eDiscovery, области дополнительное хранилище в архиве автоматически расширяется также поиск.</span><span class="sxs-lookup"><span data-stu-id="ffb56-159">**eDiscovery** - When you use an Office 365 eDiscovery tool, such as Content Search or In-Place eDiscovery, the additional storage areas in an auto-expanded archive are also searched.</span></span>
    
- <span data-ttu-id="ffb56-160">**Хранение** - при переходе почтового ящика на удержание с помощью средства, такие как хранение для судебного разбирательства в Exchange Online или содержит случая обнаружения электронных данных и политики хранения безопасности Office 365 &amp; центре соответствия требованиям, содержимого, расположенного в архиве автоматически расширяется является также помещенные на удержание.</span><span class="sxs-lookup"><span data-stu-id="ffb56-160">**Retention** - When you put a mailbox on hold by using tools such as Litigation Hold in Exchange Online or eDiscovery case holds and retention policies in the Office 365 Security &amp; Compliance Center, content located in an auto-expanded archive is also placed on hold.</span></span>
    
- <span data-ttu-id="ffb56-161">**Управление Записями записями системы обмена сообщениями** - при использовании политики удаления управления записями сообщений в Exchange Online для окончательно удалить элементы просроченных почтовых ящиков, просроченных элементов, расположенных в архив автоматически расширяется также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="ffb56-161">**Messaging records management (MRM)** - If you use MRM deletion policies in Exchange Online to permanently delete expired mailbox items, expired items located in the auto-expanded archive will also be deleted.</span></span>
    
- <span data-ttu-id="ffb56-p110">**Импорт службы** - службы Office 365 импортировать можно использовать для импорта PST-файлов были развернуты auto архив пользователя. До 100 ГБ данных можно импортировать из PST-файлов для архивного почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="ffb56-p110">**Import service** - You can use the Office 365 Import service to import PST files to a user's auto-expanded archive. You can import up to 100 GB of data from PST files to the user's archive mailbox.</span></span> 

## <a name="more-information"></a><span data-ttu-id="ffb56-164">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="ffb56-164">More information</span></span>

<span data-ttu-id="ffb56-165">Более подробные технические сведения об архивации, см. развертываемым [Office 365: вопросы и ответы архивы развертываемым](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span><span class="sxs-lookup"><span data-stu-id="ffb56-165">For more technical details about auto-expanding archiving, see [Office 365: Auto-Expanding Archives FAQ](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span></span>