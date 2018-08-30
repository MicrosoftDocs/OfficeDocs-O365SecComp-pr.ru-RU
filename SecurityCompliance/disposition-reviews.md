---
title: Общие сведения о проверках перед ликвидацией
ms.author: stephow
author: stephow-MSFT
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
ms.assetid: d0c6095b-bfee-4906-a2c7-89c2d7f411c1
description: При создании метки, который сохраняет контента в Office 365, вы можете запуск проверки ликвидации в конце периода хранения.
ms.openlocfilehash: c0a2933f597c9b314ac4ce2e72de9619fac90082
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013723"
---
# <a name="overview-of-disposition-reviews"></a><span data-ttu-id="c991b-103">Общие сведения о проверках перед ликвидацией</span><span class="sxs-lookup"><span data-stu-id="c991b-103">Overview of disposition reviews</span></span>

<span data-ttu-id="c991b-p101">По достижении конца периода хранения содержимого существует несколько причин, по которым проверка, что содержимое, чтобы решить, будет ли она может быть удалена («удален»). Например может потребоваться:</span><span class="sxs-lookup"><span data-stu-id="c991b-p101">When content reaches the end of its retention period, there are several reasons why you might want to review that content to decide whether it can be safely deleted ("disposed"). For example, you might need to:</span></span>
  
- <span data-ttu-id="c991b-106">Приостановить удаление («расположение») требуемого содержимого в случае судебного разбирательства или аудита.</span><span class="sxs-lookup"><span data-stu-id="c991b-106">Suspend the deletion ("disposition") of relevant content in the event of litigation or an audit.</span></span>
    
- <span data-ttu-id="c991b-107">Удалите содержимое из списка размещение документов для хранения в архиве, если, что содержимое справочных материалов или предыдущие значения.</span><span class="sxs-lookup"><span data-stu-id="c991b-107">Remove content from the disposition list to store in an archive, if that content has research or historical value.</span></span>
    
- <span data-ttu-id="c991b-108">Назначьте период различных хранения содержимого, если исходный политики был временной или промежуточная решения.</span><span class="sxs-lookup"><span data-stu-id="c991b-108">Assign a different retention period to the content, if the original policy was a temporary or provisional solution.</span></span>
    
- <span data-ttu-id="c991b-109">Возвратите содержимое клиентам или переместить его в другой организации.</span><span class="sxs-lookup"><span data-stu-id="c991b-109">Return the content to clients or transfer it to another organization.</span></span>
    
<span data-ttu-id="c991b-p102">При создании метки, который сохраняет контента в Office 365, вы можете запуск проверки ликвидации в конце периода хранения. В разделе review ликвидации:</span><span class="sxs-lookup"><span data-stu-id="c991b-p102">When you create a label that retains content in Office 365, you can choose to trigger a disposition review at the end of the retention period. In a disposition review:</span></span>
  
- <span data-ttu-id="c991b-p103">Определенные пользователи получают уведомление по электронной почте, что у них контент для просмотра. Эти проверяющие могут быть отдельных пользователей, рассылки или групп безопасности или группы Office 365. Обратите внимание на то, что уведомления отправляются неделю.</span><span class="sxs-lookup"><span data-stu-id="c991b-p103">The people you choose receive an email notification that they have content to review. These reviewers can be individual users, distribution or security groups, or Office 365 groups. Note that notifications are sent on a weekly basis.</span></span>
    
- <span data-ttu-id="c991b-115">Рецензенты перейдите на страницу **ликвидации** в системы &amp; центре соответствия требованиям для просмотра содержимого.</span><span class="sxs-lookup"><span data-stu-id="c991b-115">The reviewers go to the **Disposition** page in the Security &amp; Compliance Center to review the content.</span></span> 
    
- <span data-ttu-id="c991b-116">Для каждого документа проверяющий выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c991b-116">For each document, the reviewer can:</span></span>
    
  - <span data-ttu-id="c991b-117">Применить другую метку.</span><span class="sxs-lookup"><span data-stu-id="c991b-117">Apply a different label.</span></span>
    
  - <span data-ttu-id="c991b-118">Расширение срок его хранения.</span><span class="sxs-lookup"><span data-stu-id="c991b-118">Extend its retention period.</span></span>
    
  - <span data-ttu-id="c991b-119">Окончательно удалите его.</span><span class="sxs-lookup"><span data-stu-id="c991b-119">Permanently delete it.</span></span>
    
- <span data-ttu-id="c991b-120">Проверяющие можно просмотреть ожидающие или журналу расположения и экспортировать этот список в виде CSV-файла.</span><span class="sxs-lookup"><span data-stu-id="c991b-120">Reviewers can view either pending or historical dispositions, and export that list as a .csv file.</span></span>
    
<span data-ttu-id="c991b-121">Обратите внимание, что ликвидации обзоры требуется подписка на Office 365 корпоративный E5.</span><span class="sxs-lookup"><span data-stu-id="c991b-121">Note that disposition reviews require an Office 365 Enterprise E5 subscription.</span></span>
  
<span data-ttu-id="c991b-p104">Обзор ликвидации можно включить в почтовые ящики Exchange, сайты SharePoint, OneDrive учетные записи и группы Office 365. Контент, ожидающие review ликвидации в тех местах удаляется только в том случае, после проверяющий выбирает для окончательного удаления содержимого.</span><span class="sxs-lookup"><span data-stu-id="c991b-p104">A disposition review can include content in Exchange mailboxes, SharePoint sites, OneDrive accounts, and Office 365 groups. Content awaiting a disposition review in those locations is deleted only after a reviewer chooses to permanently delete the content.</span></span>
  
![Страница ликвидации](media/b7436fb2-1f35-4146-8ca2-32c9d10f7e09.png)
  
## <a name="setting-up-the-disposition-review-by-creating-a-label"></a><span data-ttu-id="c991b-125">Настройка проверки ликвидации путем создания метки</span><span class="sxs-lookup"><span data-stu-id="c991b-125">Setting up the disposition review by creating a label</span></span>

<span data-ttu-id="c991b-p105">Это базовый рабочий процесс по настройке проверки ликвидации. Обратите внимание, что этот поток показано, как label, опубликованный и затем вручную применить пользователем; Кроме того метки, по которому формируются review ликвидации может быть автоматически применяется к контенту.</span><span class="sxs-lookup"><span data-stu-id="c991b-p105">This is the basic workflow for setting up a disposition review. Note that this flow shows a label being published and then manually applied by a user; alternatively, a label that triggers a disposition review can be auto-applied to content.</span></span>
  
![Диаграмма, отражающая поток работы ликвидации](media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
<span data-ttu-id="c991b-p106">Просмотр расположения может использоваться при создании метки в Office 365. Обратите внимание, что этот параметр недоступен в политику хранения, но только в элемент label с настроек хранения.</span><span class="sxs-lookup"><span data-stu-id="c991b-p106">A disposition review is an option when you create a label in Office 365. Note that this option is not available in a retention policy but only in a label with retention settings.</span></span>
  
<span data-ttu-id="c991b-131">Дополнительные сведения о меток [метки](labels.md)см.</span><span class="sxs-lookup"><span data-stu-id="c991b-131">For more information about labels, see [Overview of labels](labels.md).</span></span>
  
![Параметры хранения для элемента label](media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
  
## <a name="disposing-content"></a><span data-ttu-id="c991b-133">Удаление содержимого</span><span class="sxs-lookup"><span data-stu-id="c991b-133">Disposing content</span></span>

<span data-ttu-id="c991b-p107">Если проверяющий получает уведомление по электронной почте, что содержимое Готово для просмотра, их можно перейти к странице **ликвидации** в системы &amp; центре соответствия требованиям и выберите один или несколько элементов. Проверяющий нажмите выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="c991b-p107">When a reviewer is notified by email that content is ready to review, they can go to the **Disposition** page in the Security &amp; Compliance Center and select one or more items. The reviewer can then:</span></span> 
  
- <span data-ttu-id="c991b-136">Применить другую метку.</span><span class="sxs-lookup"><span data-stu-id="c991b-136">Apply a different label.</span></span>
    
- <span data-ttu-id="c991b-137">Увеличить срок хранения;</span><span class="sxs-lookup"><span data-stu-id="c991b-137">Extend the retention period.</span></span>
    
- <span data-ttu-id="c991b-138">Окончательно удалите элемент.</span><span class="sxs-lookup"><span data-stu-id="c991b-138">Permanently delete the item.</span></span>
    
<span data-ttu-id="c991b-p108">Проверяющий можно использовать ссылку для просмотра документа в его исходное расположение, если проверяющий есть разрешения для данного расположения. Во время проверки ликвидации контента никогда не перемещается из исходного расположения и никогда не удаляются, пока проверяющий выбирает это действие.</span><span class="sxs-lookup"><span data-stu-id="c991b-p108">A reviewer can use the link to view the document in its original location, if the reviewer has permissions for that location. During a disposition review, the content never moves from its original location, and it's never deleted until the reviewer chooses to do so.</span></span>
  
<span data-ttu-id="c991b-p109">Обратите внимание, что уведомления по электронной почте отправляются автоматически рецензентов неделю. Таким образом, по достижении конца периода хранения содержимого может потребоваться до семи дней рецензентов на получение уведомлений по электронной почте, что содержимое ожидает обработки.</span><span class="sxs-lookup"><span data-stu-id="c991b-p109">Note that the email notifications are sent automatically to reviewers on a weekly basis. Therefore, when content reaches the end of its retention period, it may take up to seven days for reviewers to receive the email notification that content is awaiting disposition.</span></span>
  
<span data-ttu-id="c991b-p110">Также Обратите внимание на то, что все ликвидации действия были проверены. Чтобы обеспечить это, необходимо включить аудит по крайней мере один день до первое действие ликвидации — для получения дополнительных сведений, см [Поиск в журнале аудита безопасности Office 365 &amp; центре соответствия требованиям](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="c991b-p110">Also note that all disposition actions are audited. To ensure this, you must turn on auditing at least one day prior to the first disposition action - for more information, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> 
  
![Параметры расположения для документа](media/771630fd-a9b0-47cf-983b-fe85eb4cdafd.png)
  
## <a name="permissions-for-disposition"></a><span data-ttu-id="c991b-146">Разрешения для ликвидации</span><span class="sxs-lookup"><span data-stu-id="c991b-146">Permissions for disposition</span></span>

<span data-ttu-id="c991b-p111">Чтобы получить доступ к странице **ликвидации** , проверяющие должны быть членами роль **Ликвидации управления** и роль **Только для просмотра журналов аудита** . Мы рекомендуем Создание новой группы ролей, называется ликвидации рецензентов, добавление эти две роли, группы ролей и затем добавлении членов в группу ролей.</span><span class="sxs-lookup"><span data-stu-id="c991b-p111">To get access to the **Disposition** page, reviewers must be members of the **Disposition Management** role and the **View-Only Audit Logs** role. We recommend creating a new role group called Disposition Reviewers, adding these two roles to that role group, and then adding members to the role group.</span></span> 
  
<span data-ttu-id="c991b-149">Дополнительные сведения можно [предоставления пользователям доступа к Office 365 безопасность &amp; центре соответствия требованиям](grant-access-to-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="c991b-149">For more information, see [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md)</span></span>
  
## <a name="how-long-until-disposed-content-is-permanently-deleted"></a><span data-ttu-id="c991b-150">Сколько времени до окончательного удаления удаленного содержимого</span><span class="sxs-lookup"><span data-stu-id="c991b-150">How long until disposed content is permanently deleted</span></span>

<span data-ttu-id="c991b-p112">Ожидает проверки ликвидации контента удаляется только после проверяющий выбирает для окончательного удаления содержимого. Если проверяющий выбирает этот параметр, содержимое в сайт SharePoint или учетной записи службы OneDrive становится доступным для процесса очистки standard, описанных в данном разделе: [как работает политика удержания с содержимым на месте](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span><span class="sxs-lookup"><span data-stu-id="c991b-p112">Content awaiting a disposition review is deleted only after a reviewer chooses to permanently delete the content. When the reviewer chooses this option, the content in the SharePoint site or OneDrive account becomes eligible for the standard cleanup process described in this section: [How a retention policy works with content in place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span></span>
  
<span data-ttu-id="c991b-153">Это означает, что:</span><span class="sxs-lookup"><span data-stu-id="c991b-153">This means that:</span></span>
  
- <span data-ttu-id="c991b-p113">Содержимое в библиотеке документов будет перемещено в первого корзины **в течение 7 дней** расстановки и окончательно удалены **93 дней** после этого. В корзину не индексируются службой поиска и таким образом его контент, недоступны в удержание электронных данных.</span><span class="sxs-lookup"><span data-stu-id="c991b-p113">Content in a document library will be moved to the first-stage Recycle Bin **within 7 days** of disposition, and then permanently deleted **93 days** after that. The Recycle Bin is not indexed by search and therefore its contents are not available to an eDiscovery hold.</span></span> 
    
- <span data-ttu-id="c991b-156">Содержимое библиотеки будет безвозвратно удержания хранения удаленных **в течение 7 дней** расстановки.</span><span class="sxs-lookup"><span data-stu-id="c991b-156">Content in the Preservation Hold library will be permanently deleted **within 7 days** of disposition.</span></span> 
    
## <a name="view-pending-and-completed-dispositions"></a><span data-ttu-id="c991b-157">Просмотр ожидающих и завершенных расположения</span><span class="sxs-lookup"><span data-stu-id="c991b-157">View pending and completed dispositions</span></span>

<span data-ttu-id="c991b-158">На странице **ликвидации** безопасности &amp; центре соответствия требованиям, можно просмотреть ожидающие и завершенные расположения:</span><span class="sxs-lookup"><span data-stu-id="c991b-158">On the **Disposition** page of the Security &amp; Compliance Center, you can view both pending and completed dispositions:</span></span> 
  
- <span data-ttu-id="c991b-p114">**Ожидающие** расположения закончили срок их хранения и требуют проверки ликвидации. После просмотра каждого элемента, решите, следует ли применить другую метку, расширение срок его хранения или окончательно удалить.</span><span class="sxs-lookup"><span data-stu-id="c991b-p114">**Pending** dispositions have reached the end of their retention period and require a disposition review. After reviewing each item, decide if you want to apply a different label to it, extend its retention period, or permanently delete it.</span></span> 
    
- <span data-ttu-id="c991b-p115">Расположения **завершено** были утверждены для удаления во время проверки ликвидации и теперь находятся в процессе окончательного удаления. Элементы, которые имели разные метки применяется или их период хранения для расширенного как часть анализа не будет отображаться, здесь.</span><span class="sxs-lookup"><span data-stu-id="c991b-p115">**Completed** dispositions were approved for deletion during a disposition review and are now in the process of being permanently deleted. Items that had a different label applied or their retention period extended as part of a review won't appear here.</span></span> 
    
### <a name="filter-the-disposition-views"></a><span data-ttu-id="c991b-163">Фильтрация представления ликвидации</span><span class="sxs-lookup"><span data-stu-id="c991b-163">Filter the disposition views</span></span>

<span data-ttu-id="c991b-p116">Эти представления можно фильтровать по диапазону метки или время. Для ожидающих расположения, интервала времени на основе даты окончания срока действия. Для журнала расположения интервала времени основано на Дата удаления.</span><span class="sxs-lookup"><span data-stu-id="c991b-p116">You can filter these views by label or time range. For pending dispositions, the time range is based on the expiry date. For historical dispositions, the time range is based on the deletion date.</span></span>
  
![Параметры фильтра на странице ликвидации](media/8682a9f5-a77d-45ae-b902-8418a3ebbea1.png)
  
### <a name="export-the-disposition-items"></a><span data-ttu-id="c991b-168">Экспорт элементов ликвидации</span><span class="sxs-lookup"><span data-stu-id="c991b-168">Export the disposition items</span></span>

<span data-ttu-id="c991b-169">Кроме того можно экспортировать элементов в любом представлении как CSV-файл, который можно открыть в Excel.</span><span class="sxs-lookup"><span data-stu-id="c991b-169">In addition, you can export the items in either view as a .csv file that you can open in Excel.</span></span>
  
![Экспортированные ликвидации данных в Excel](media/08e3bc09-b132-47b4-a051-a590b697e725.png)
  

