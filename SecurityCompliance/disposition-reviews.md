---
title: Обзор проверок ликвидации
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: При создании метки, в которой хранится контент в Office 365, вы можете запустить проверку ликвидации в конце периода хранения.
ms.openlocfilehash: 5dac91368ff2aff6ca7e1a2c3591b50466b869ac
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455041"
---
# <a name="overview-of-disposition-reviews"></a><span data-ttu-id="9fb18-103">Обзор проверок ликвидации</span><span class="sxs-lookup"><span data-stu-id="9fb18-103">Overview of disposition reviews</span></span>

<span data-ttu-id="9fb18-104">Когда содержимое достигает окончания срока хранения, существует несколько причин, по которым может потребоваться проверить, можно ли его удалить ("удалено").</span><span class="sxs-lookup"><span data-stu-id="9fb18-104">When content reaches the end of its retention period, there are several reasons why you might want to review that content to decide whether it can be safely deleted ("disposed").</span></span> <span data-ttu-id="9fb18-105">Например, может потребоваться выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9fb18-105">For example, you might need to:</span></span>
  
- <span data-ttu-id="9fb18-106">ПриОстановка удаления ("расположения") релевантного контента в случае судебного разбирательства или аудита.</span><span class="sxs-lookup"><span data-stu-id="9fb18-106">Suspend the deletion ("disposition") of relevant content in the event of litigation or an audit.</span></span>
    
- <span data-ttu-id="9fb18-107">Удаление контента из списка расстановки для хранения в архиве, если это содержимое содержит исследование или историческое значение.</span><span class="sxs-lookup"><span data-stu-id="9fb18-107">Remove content from the disposition list to store in an archive, if that content has research or historical value.</span></span>
    
- <span data-ttu-id="9fb18-108">Назначьте другой срок хранения содержимому, если исходная политика была временным или предустановленным решением.</span><span class="sxs-lookup"><span data-stu-id="9fb18-108">Assign a different retention period to the content, if the original policy was a temporary or provisional solution.</span></span>
    
- <span data-ttu-id="9fb18-109">Возврат контента клиентам или их передача в другую организацию.</span><span class="sxs-lookup"><span data-stu-id="9fb18-109">Return the content to clients or transfer it to another organization.</span></span>
    
<span data-ttu-id="9fb18-110">При создании метки, в которой хранится контент в Office 365, вы можете запустить проверку ликвидации в конце периода хранения.</span><span class="sxs-lookup"><span data-stu-id="9fb18-110">When you create a label that retains content in Office 365, you can choose to trigger a disposition review at the end of the retention period.</span></span> <span data-ttu-id="9fb18-111">При проверке ликвидации:</span><span class="sxs-lookup"><span data-stu-id="9fb18-111">In a disposition review:</span></span>
  
- <span data-ttu-id="9fb18-112">Выбранные пользователи получат уведомление по электронной почте о том, что у них есть контент для просмотра.</span><span class="sxs-lookup"><span data-stu-id="9fb18-112">The people you choose receive an email notification that they have content to review.</span></span> <span data-ttu-id="9fb18-113">Этими рецензентами могут быть отдельные пользователи, группы рассылки или группы безопасности или группы Office 365.</span><span class="sxs-lookup"><span data-stu-id="9fb18-113">These reviewers can be individual users, distribution or security groups, or Office 365 groups.</span></span> <span data-ttu-id="9fb18-114">Обратите внимание, что уведомления отправляются еженедельно.</span><span class="sxs-lookup"><span data-stu-id="9fb18-114">Note that notifications are sent on a weekly basis.</span></span>
    
- <span data-ttu-id="9fb18-115">Рецензенты отправляются на страницу **размещения** в центре соответствия &amp; требованиям безопасности для просмотра контента.</span><span class="sxs-lookup"><span data-stu-id="9fb18-115">The reviewers go to the **Disposition** page in the Security &amp; Compliance Center to review the content.</span></span> 
    
- <span data-ttu-id="9fb18-116">Для каждого документа проверяющий может выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9fb18-116">For each document, the reviewer can:</span></span>
    
  - <span data-ttu-id="9fb18-117">Примените другую метку.</span><span class="sxs-lookup"><span data-stu-id="9fb18-117">Apply a different label.</span></span>
    
  - <span data-ttu-id="9fb18-118">Расширьте срок хранения.</span><span class="sxs-lookup"><span data-stu-id="9fb18-118">Extend its retention period.</span></span>
    
  - <span data-ttu-id="9fb18-119">Окончательно удалить.</span><span class="sxs-lookup"><span data-stu-id="9fb18-119">Permanently delete it.</span></span>
    
- <span data-ttu-id="9fb18-120">Проверяющие могут просматривать как ожидающие, так и исторические расстановки, а также экспортировать этот список в виде CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="9fb18-120">Reviewers can view either pending or historical dispositions, and export that list as a .csv file.</span></span>
    
<span data-ttu-id="9fb18-121">Обратите внимание, что для рецензирования расстановки требуется подписка на Office 365 корпоративный для Office.</span><span class="sxs-lookup"><span data-stu-id="9fb18-121">Note that disposition reviews require an Office 365 Enterprise E5 subscription.</span></span>
  
<span data-ttu-id="9fb18-122">Обзор ликвидации может включать контент в почтовые ящики Exchange, сайты SharePoint, учетные записи OneDrive и группы Office 365.</span><span class="sxs-lookup"><span data-stu-id="9fb18-122">A disposition review can include content in Exchange mailboxes, SharePoint sites, OneDrive accounts, and Office 365 groups.</span></span> <span data-ttu-id="9fb18-123">Содержимое, ожидающее проверки ликвидации в этих расположениях, удаляется только после того, как рецензент выберет окончательное удаление контента.</span><span class="sxs-lookup"><span data-stu-id="9fb18-123">Content awaiting a disposition review in those locations is deleted only after a reviewer chooses to permanently delete the content.</span></span>
  
![Страница расположения](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a><span data-ttu-id="9fb18-125">Настройка проверки ликвидации путем создания метки</span><span class="sxs-lookup"><span data-stu-id="9fb18-125">Setting up the disposition review by creating a label</span></span>

<span data-ttu-id="9fb18-126">Это базовый рабочий процесс для настройки проверки ликвидации.</span><span class="sxs-lookup"><span data-stu-id="9fb18-126">This is the basic workflow for setting up a disposition review.</span></span> <span data-ttu-id="9fb18-127">Обратите внимание, что этот процесс показывает, что метка публикуется и затем вручную применяется пользователем; Кроме того, метка, инициирующая проверку ликвидации, может быть автоматически применена к содержимому.</span><span class="sxs-lookup"><span data-stu-id="9fb18-127">Note that this flow shows a label being published and then manually applied by a user; alternatively, a label that triggers a disposition review can be auto-applied to content.</span></span>
  
![Диаграмма, на которой показано, как работает процесс ликвидации](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
<span data-ttu-id="9fb18-129">Проверка ликвидации является возможностью при создании метки в Office 365.</span><span class="sxs-lookup"><span data-stu-id="9fb18-129">A disposition review is an option when you create a label in Office 365.</span></span> <span data-ttu-id="9fb18-130">Обратите внимание, что этот параметр недоступен в политике хранения, но только в метке с параметрами хранения.</span><span class="sxs-lookup"><span data-stu-id="9fb18-130">Note that this option is not available in a retention policy but only in a label with retention settings.</span></span>
  
<span data-ttu-id="9fb18-131">Дополнительные сведения о метках см. в статье [Общие сведения о метках](labels.md).</span><span class="sxs-lookup"><span data-stu-id="9fb18-131">For more information about labels, see [Overview of labels](labels.md).</span></span>
  
![Параметры хранения для метки](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a><span data-ttu-id="9fb18-133">Удаление контента</span><span class="sxs-lookup"><span data-stu-id="9fb18-133">Disposing content</span></span>

<span data-ttu-id="9fb18-134">Когда проверяющий получает уведомление по электронной почте о том, что контент готов к просмотру, он может перейти на страницу **размещения** в центре безопасности &amp; и выбрать один или несколько элементов.</span><span class="sxs-lookup"><span data-stu-id="9fb18-134">When a reviewer is notified by email that content is ready to review, they can go to the **Disposition** page in the Security &amp; Compliance Center and select one or more items.</span></span> <span data-ttu-id="9fb18-135">Затем проверяющий может:</span><span class="sxs-lookup"><span data-stu-id="9fb18-135">The reviewer can then:</span></span> 
  
- <span data-ttu-id="9fb18-136">Примените другую метку.</span><span class="sxs-lookup"><span data-stu-id="9fb18-136">Apply a different label.</span></span>
    
- <span data-ttu-id="9fb18-137">Продлить срок хранения.</span><span class="sxs-lookup"><span data-stu-id="9fb18-137">Extend the retention period.</span></span>
    
- <span data-ttu-id="9fb18-138">Окончательное удаление элемента.</span><span class="sxs-lookup"><span data-stu-id="9fb18-138">Permanently delete the item.</span></span>
    
<span data-ttu-id="9fb18-139">Проверяющий может использовать ссылку для просмотра документа в его исходном расположении, если проверяющий имеет разрешения для этого расположения.</span><span class="sxs-lookup"><span data-stu-id="9fb18-139">A reviewer can use the link to view the document in its original location, if the reviewer has permissions for that location.</span></span> <span data-ttu-id="9fb18-140">Во время проверки ликвидации содержимое никогда не перемещается из исходного расположения и никогда не удаляется до тех пор, пока проверяющий не решит это.</span><span class="sxs-lookup"><span data-stu-id="9fb18-140">During a disposition review, the content never moves from its original location, and it's never deleted until the reviewer chooses to do so.</span></span>
  
<span data-ttu-id="9fb18-141">Обратите внимание, что уведомления по электронной почте автоматически отправляются проверяющим.</span><span class="sxs-lookup"><span data-stu-id="9fb18-141">Note that the email notifications are sent automatically to reviewers on a weekly basis.</span></span> <span data-ttu-id="9fb18-142">Таким образом, когда содержимое достигает окончания срока хранения, рецензентам может потребоваться до семи дней для получения уведомления по электронной почте о том, что содержимое ожидает расстановки.</span><span class="sxs-lookup"><span data-stu-id="9fb18-142">Therefore, when content reaches the end of its retention period, it may take up to seven days for reviewers to receive the email notification that content is awaiting disposition.</span></span>
  
<span data-ttu-id="9fb18-143">Кроме того, обратите внимание на то, что все действия по размещению подлежат аудиту.</span><span class="sxs-lookup"><span data-stu-id="9fb18-143">Also note that all disposition actions are audited.</span></span> <span data-ttu-id="9fb18-144">Для этого необходимо включить аудит по крайней мере один день перед первым действием обработки — дополнительные сведения можно найти в статье [Поиск в журнале аудита в центре безопасности &amp; и соответствия требованиям Office 365](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="9fb18-144">To ensure this, you must turn on auditing at least one day prior to the first disposition action - for more information, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> 
  
![Параметры ликвидации для документа](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a><span data-ttu-id="9fb18-146">Разрешения для ликвидации</span><span class="sxs-lookup"><span data-stu-id="9fb18-146">Permissions for disposition</span></span>

<span data-ttu-id="9fb18-147">Чтобы получить доступ к странице \*\*\*\* расстановки, рецензенты должны быть членами роли **управления** РасстановкОй и **аудитом только для просмотра** .</span><span class="sxs-lookup"><span data-stu-id="9fb18-147">To get access to the **Disposition** page, reviewers must be members of the **Disposition Management** role and the **View-Only Audit Logs** role.</span></span> <span data-ttu-id="9fb18-148">Мы рекомендуем создать новую группу ролей с именем проверяющих, добавив эти две роли в эту группу ролей, а затем добавляя участников в группу ролей.</span><span class="sxs-lookup"><span data-stu-id="9fb18-148">We recommend creating a new role group called Disposition Reviewers, adding these two roles to that role group, and then adding members to the role group.</span></span> 
  
<span data-ttu-id="9fb18-149">Дополнительные сведения см в статье [предоставление пользователям доступа к центру безопасности &amp; и соответствия требованиям Office 365](grant-access-to-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="9fb18-149">For more information, see [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md)</span></span>
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a><span data-ttu-id="9fb18-150">Время до окончательного удаления ликвидации контента</span><span class="sxs-lookup"><span data-stu-id="9fb18-150">How long until disposed content is permanently deleted</span></span>

<span data-ttu-id="9fb18-151">Контент, ожидающий проверки ликвидации, удаляется только после того, как рецензент выберет окончательное удаление контента.</span><span class="sxs-lookup"><span data-stu-id="9fb18-151">Content awaiting a disposition review is deleted only after a reviewer chooses to permanently delete the content.</span></span> <span data-ttu-id="9fb18-152">Когда проверяющий выбирает этот параметр, контент на сайте SharePoint или в учетной записи OneDrive становится доступным для стандартного процесса очистки, описанного в этом разделе: [как политика хранения работает с контентом на месте](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span><span class="sxs-lookup"><span data-stu-id="9fb18-152">When the reviewer chooses this option, the content in the SharePoint site or OneDrive account becomes eligible for the standard cleanup process described in this section: [How a retention policy works with content in place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span></span>
  
<span data-ttu-id="9fb18-153">Это означает, что:</span><span class="sxs-lookup"><span data-stu-id="9fb18-153">This means that:</span></span>
  
- <span data-ttu-id="9fb18-154">Содержимое библиотеки документов будет перемещено в корзину первого уровня **в течение 7 дней** после завершения, а затем окончательно удалено через **93 дней** после этого.</span><span class="sxs-lookup"><span data-stu-id="9fb18-154">Content in a document library will be moved to the first-stage Recycle Bin **within 7 days** of disposition, and then permanently deleted **93 days** after that.</span></span> <span data-ttu-id="9fb18-155">Корзина не индексируется службой поиска, поэтому ее содержимое недоступно для удержания обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="9fb18-155">The Recycle Bin is not indexed by search and therefore its contents are not available to an eDiscovery hold.</span></span> 
    
- <span data-ttu-id="9fb18-156">Контент из библиотеки хранения хранения будет окончательно удален **в течение 7 дней с момента** расстановки.</span><span class="sxs-lookup"><span data-stu-id="9fb18-156">Content in the Preservation Hold library will be permanently deleted **within 7 days** of disposition.</span></span> 
    
## <a name="view-pending-and-completed-dispositions"></a><span data-ttu-id="9fb18-157">Просмотр ожидающих и завершенных расстановки</span><span class="sxs-lookup"><span data-stu-id="9fb18-157">View pending and completed dispositions</span></span>

<span data-ttu-id="9fb18-158">На странице **размещения** центра соответствия требованиям безопасности &amp; можно просматривать как отложенные, так и завершенные расположения:</span><span class="sxs-lookup"><span data-stu-id="9fb18-158">On the **Disposition** page of the Security &amp; Compliance Center, you can view both pending and completed dispositions:</span></span> 
  
- <span data-ttu-id="9fb18-159">**Ожидающие** ликвидации достигают завершения срока хранения и требуют проверки ликвидации.</span><span class="sxs-lookup"><span data-stu-id="9fb18-159">**Pending** dispositions have reached the end of their retention period and require a disposition review.</span></span> <span data-ttu-id="9fb18-160">После проверки каждого элемента решите, следует ли применить к нему другую метку, продлить срок хранения или окончательно удалить его.</span><span class="sxs-lookup"><span data-stu-id="9fb18-160">After reviewing each item, decide if you want to apply a different label to it, extend its retention period, or permanently delete it.</span></span> 
    
- <span data-ttu-id="9fb18-161">**Завершенные** ликвидации были утверждены для удаления во время проверки ликвидации и теперь находятся в процессе окончательного удаления.</span><span class="sxs-lookup"><span data-stu-id="9fb18-161">**Completed** dispositions were approved for deletion during a disposition review and are now in the process of being permanently deleted.</span></span> <span data-ttu-id="9fb18-162">Элементы, к которым применена другая метка, или срок хранения, продленный в рамках проверки, не отображаются здесь.</span><span class="sxs-lookup"><span data-stu-id="9fb18-162">Items that had a different label applied or their retention period extended as part of a review won't appear here.</span></span> 
    
### <a name="filter-the-disposition-views"></a><span data-ttu-id="9fb18-163">Фильтрация представлений расстановки</span><span class="sxs-lookup"><span data-stu-id="9fb18-163">Filter the disposition views</span></span>

<span data-ttu-id="9fb18-164">Вы можете отфильтровать эти представления по метке или диапазону времени.</span><span class="sxs-lookup"><span data-stu-id="9fb18-164">You can filter these views by label or time range.</span></span> <span data-ttu-id="9fb18-165">Для ожидающих расстановки диапазон времени зависит от даты истечения срока действия.</span><span class="sxs-lookup"><span data-stu-id="9fb18-165">For pending dispositions, the time range is based on the expiry date.</span></span> <span data-ttu-id="9fb18-166">Для исторических расстановки диапазон времени основан на дате удаления.</span><span class="sxs-lookup"><span data-stu-id="9fb18-166">For historical dispositions, the time range is based on the deletion date.</span></span>
  
![Параметры фильтра на странице расположения](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a><span data-ttu-id="9fb18-168">Экспорт элементов ликвидации</span><span class="sxs-lookup"><span data-stu-id="9fb18-168">Export the disposition items</span></span>

<span data-ttu-id="9fb18-169">Кроме того, вы можете экспортировать элементы из любого представления в виде CSV-файла, который можно открыть в Excel.</span><span class="sxs-lookup"><span data-stu-id="9fb18-169">In addition, you can export the items in either view as a .csv file that you can open in Excel.</span></span>
  
![Экспортированные данные о расположении в Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

