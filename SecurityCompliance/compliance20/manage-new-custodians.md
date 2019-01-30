---
title: Управление custodians в случае расширенные обнаружения электронных данных (Предварительная версия)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 742f6bc35b67071fba528e6a0ce543ecc6915762
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608287"
---
# <a name="managing-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="fb1df-102">Управление custodians в случае расширенные обнаружения электронных данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="fb1df-102">Managing custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="fb1df-p101">На вкладке Custodians со списком возможность сортировки всех custodians в случае. После добавления custodians дела подробные сведения о каждом custodian будет автоматически собираются из Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p101">The Custodians tab contains a sortable list of all the custodians in the case. After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

## <a name="viewing-custodian-details"></a><span data-ttu-id="fb1df-105">Просмотр подробных сведений о custodian</span><span class="sxs-lookup"><span data-stu-id="fb1df-105">Viewing custodian details</span></span>

<span data-ttu-id="fb1df-p102">После добавления custodian дела и выберите их в списке на вкладке **Custodians** , откроется страница "всплывающее окно", который содержит сведения о custodian. Здесь можно просмотреть все сведения, связанные с этой custodian. Всплывающее окно страница содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="fb1df-p102">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian. The flyout page contains the following fields:</span></span>

- <span data-ttu-id="fb1df-108">Контактные данные</span><span class="sxs-lookup"><span data-stu-id="fb1df-108">Contact information</span></span>

  - <span data-ttu-id="fb1df-p103">**Отображаемое имя**: имя, отображаемое в адресной книге для custodian. Обычно это сочетание custodian имя, средней имя и Фамилия.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p103">**Display Name**: The name displayed in the address book for the custodian. This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="fb1df-111">**Mail/SMTP**: SMTP-адреса для custodian, например, jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="fb1df-111">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="fb1df-112">**Название**: название задания custodian.</span><span class="sxs-lookup"><span data-stu-id="fb1df-112">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="fb1df-113">**Подразделение**: имя для отдела, в котором работает custodian.</span><span class="sxs-lookup"><span data-stu-id="fb1df-113">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="fb1df-p104">**Manager**: руководитель custodian. Назначенный диспетчера будут иметь любое эскалации коммуникаций для этой custodian.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p104">**Manager**: The custodian’s manager. The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="fb1df-116">Сведения о расположении</span><span class="sxs-lookup"><span data-stu-id="fb1df-116">Location information</span></span>

  - <span data-ttu-id="fb1df-117">**Город**: город, в котором находится custodian.</span><span class="sxs-lookup"><span data-stu-id="fb1df-117">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="fb1df-118">**Состояние**: область или край в адресе custodian.</span><span class="sxs-lookup"><span data-stu-id="fb1df-118">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="fb1df-119">**Страна или регион**: Страна или регион, в которой находится custodian; Например, «US» или «(Великобритания)».</span><span class="sxs-lookup"><span data-stu-id="fb1df-119">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="fb1df-120">**Office**: расположение комнаты на месте custodian бизнеса.</span><span class="sxs-lookup"><span data-stu-id="fb1df-120">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="fb1df-121">Сведения об обращении</span><span class="sxs-lookup"><span data-stu-id="fb1df-121">Case information</span></span>

  - <span data-ttu-id="fb1df-122">**Состояние удержания**: Указывает, если custodian переведен на удержание.</span><span class="sxs-lookup"><span data-stu-id="fb1df-122">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="fb1df-p105">**Состояние связи**: Указывает, если custodian выдано уведомление удержания. Если custodian выдано уведомление, это будут помечены как *опубликованные*. Если custodian не была выдана уведомление, то это состояние будет *без опубликованные*.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p105">**Communication status**: Indicates if the custodian has been issued a hold notice. If the custodian has been issued a notice, then this will be marked as *Published*. If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="fb1df-p106">**Состояние**: состояние custodian в случае. Это станет *активным* , если custodian — это по-прежнему на удержание для случая. Если custodian удален из дела, их состояние изменится на *запущен*.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p106">**Status**: The status of the custodian within the case. This will be *Active* if the custodian is still on hold for the case. If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="fb1df-129">Состояние обработки</span><span class="sxs-lookup"><span data-stu-id="fb1df-129">Processing status</span></span>

  - <span data-ttu-id="fb1df-130">**Состояние индексирования**: Указывает состояние глубокой индексирования задания.</span><span class="sxs-lookup"><span data-stu-id="fb1df-130">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="fb1df-131">**Индексирование времени последнего обновления**: Указывает, метки даты из при последнего было включено глубокое заданий индексирования.</span><span class="sxs-lookup"><span data-stu-id="fb1df-131">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="fb1df-132">**Источники данных**: отображается количество почтовых ящиков, сайты и групп, которые были выбраны для custodian.</span><span class="sxs-lookup"><span data-stu-id="fb1df-132">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="updating-a-custodian"></a><span data-ttu-id="fb1df-133">Обновление custodian</span><span class="sxs-lookup"><span data-stu-id="fb1df-133">Updating a custodian</span></span>

<span data-ttu-id="fb1df-p107">Мере делами может оказаться, что может быть дополнительные источники данных относится к определенным custodian & случае. В других случаях может потребоваться удалить некоторые источники данных, просмотра и подразумевается в качестве несущественно.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p107">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case. In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="fb1df-136">Чтобы обновить custodian и выбранные источники данных:</span><span class="sxs-lookup"><span data-stu-id="fb1df-136">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="fb1df-137">Выберите существующее обращение **eDiscovery > расширенной обнаружения электронных данных (Просмотр)**.</span><span class="sxs-lookup"><span data-stu-id="fb1df-137">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="fb1df-138">В случае перейдите на вкладку **Custodians** .</span><span class="sxs-lookup"><span data-stu-id="fb1df-138">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="fb1df-139">Выберите custodian(s) в списке и нажмите кнопку **Изменить источников**.</span><span class="sxs-lookup"><span data-stu-id="fb1df-139">Select the custodian(s) from the list and click **Edit sources**.</span></span>
  
4. <span data-ttu-id="fb1df-140">Обновление выбранных элементов для Exchange и OneDrive расположений, нажав кнопку **Выбор источников данных**.</span><span class="sxs-lookup"><span data-stu-id="fb1df-140">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="fb1df-p108">Добавление или удаление группы SharePoint и Exchange почтовые ящики сопоставленные пользователя, нажав кнопку, чтобы **выбрать дополнительные источники данных**. Дополнительные сведения о как для сопоставления данных источников custodian можно [Добавьте custodians расширенной eDiscovery (Просмотр) Case](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="fb1df-p108">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**. For more information about how you to map data sources to a custodian, see [Add custodians to an Advanced eDiscovery (Preview) Case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="fb1df-143">Чтобы обновить состояние удержания custodian, нажмите кнопку **наказание место хранения**и включить или отключить удержания для custodians.</span><span class="sxs-lookup"><span data-stu-id="fb1df-143">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="fb1df-144">Можно выбрать несколько custodians для выполнения действий массового, такой как повторное индексирование, выпуска или изменение набора custodians.</span><span class="sxs-lookup"><span data-stu-id="fb1df-144">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="fb1df-145">Разрешение custodian обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="fb1df-145">Resolving custodian processing errors</span></span>

<span data-ttu-id="fb1df-p109">В большинстве юридических рабочих процессов после добавления custodians для конкретного исследования, подмножество данных пользователей будет осуществляться. Из-за размеры больших файлов или поврежден некоторые элементы в источники данных custodians может частично индексированы. С помощью глубокой индексирование расширенной обнаружения электронных данных (Предварительная версия), эти частично индексированных элементов могут быть автоматически remediated повторный обход и повторное индексирование эти элементы по запросу.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p109">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched. Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed. Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="fb1df-p110">Добавленное custodian в случае их данных будет автоматически «глубоко индексироваться», позволяя пользователям оставьте это частично индексированных элементов на месте вместо того, чтобы загрузить, устранения и повторно запустить поиск за пределами Office 365. Во время жизненного цикла дела пользователь может Устранение элементов или добавление новых источников данных для указанного custodian. Может потребоваться Custodian индекс, который требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p110">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365. During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian. This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="fb1df-152">Запуск процесса повторного индексирования на адрес частично индексированных элементов:</span><span class="sxs-lookup"><span data-stu-id="fb1df-152">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="fb1df-153">Перейдите на **eDiscovery > расширенной обнаружения электронных данных (Предварительная версия)** и выберите существующее обращение.</span><span class="sxs-lookup"><span data-stu-id="fb1df-153">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="fb1df-154">В случае щелкните **вкладку Custodians**.</span><span class="sxs-lookup"><span data-stu-id="fb1df-154">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="fb1df-155">Выберите custodian(s), которую требуется необходимо повторное индексирование и нажмите кнопку **обновление индекса** на странице всплывающее меню.</span><span class="sxs-lookup"><span data-stu-id="fb1df-155">Select the custodian(s) that needs to be re-indexed, and then click **Update index** on the flyout page.</span></span>

4. <span data-ttu-id="fb1df-156">Проверьте состояние индексирования custodian, щелкнув ссылку в столбце **Служба индексирования задания состояния** на вкладке **Custodians** .</span><span class="sxs-lookup"><span data-stu-id="fb1df-156">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="fb1df-157">Также можно отслеживать состояние процесса повторного индексирования на вкладке **задания** .</span><span class="sxs-lookup"><span data-stu-id="fb1df-157">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="fb1df-158">Дополнительные сведения о повторно индексирования и устранение частично индексированных элементов можно [устранению обработки ошибок в расширенной обнаружения электронных данных (Просмотр)](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="fb1df-158">For more information about re-indexing and remediating partially indexed items, see [Fixing processing errors in Advanced eDiscovery (Preview)](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="fb1df-159">Освобождение custodian из дела</span><span class="sxs-lookup"><span data-stu-id="fb1df-159">Releasing a custodian from a case</span></span>

<span data-ttu-id="fb1df-160">Custodian высвобождается в ситуациях, где закрытии обращения, custodian больше не обязана сохранять содержимое для дела или при custodian считается не больше релевантным к конкретному случае.</span><span class="sxs-lookup"><span data-stu-id="fb1df-160">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="fb1df-p111">При отпускании custodian после публикации удержания уведомление о выпуске будет отправляться custodian. Кроме того также будут удалены все наказание удержаний атрибутами, выпущенного custodians.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p111">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian. In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="fb1df-163">Если custodian помещен на автоматическом удержание, где они не было выдано никаких уведомлений о удержания по юридическим причинам, будут удалены все наказание удержаний атрибутами, выпущенного custodians.</span><span class="sxs-lookup"><span data-stu-id="fb1df-163">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="fb1df-164">Для освобождения custodian:</span><span class="sxs-lookup"><span data-stu-id="fb1df-164">To release a custodian:</span></span> 

1.  <span data-ttu-id="fb1df-165">Перейдите на вкладку **Custodians** .</span><span class="sxs-lookup"><span data-stu-id="fb1df-165">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="fb1df-166">Выберите custodian из списка и нажмите кнопку **custodians версии** на странице всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="fb1df-166">Select the custodian from the list and click **Release custodians** on the flyout page.</span></span>

    <span data-ttu-id="fb1df-167">Состояние custodian на вкладке **Custodians** устанавливается на **запущен** и **состояние удержания** на странице всплывающего меняется на **неактивен**.</span><span class="sxs-lookup"><span data-stu-id="fb1df-167">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="fb1df-p112">Custodian может быть одновременно принимать участие в нескольких удержания по юридическим причинам: вопросы и ответы. После выпуска custodian из дела удержаний и уведомления на другие вопросы и ответы не повлияет.</span><span class="sxs-lookup"><span data-stu-id="fb1df-p112">A custodian might be simultaneously be involved in several legal hold matters. When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="fb1df-170">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="fb1df-170">Related information</span></span>

 - <span data-ttu-id="fb1df-171">Атрибуты пользователя в Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb1df-171">User Attributes in Active Directory</span></span> 
 - [<span data-ttu-id="fb1df-172">Исправление ошибок при обработке данных</span><span class="sxs-lookup"><span data-stu-id="fb1df-172">Error remediation when processing data</span></span>](error-remediation.md) 
 - [<span data-ttu-id="fb1df-173">Работа с взаимодействием</span><span class="sxs-lookup"><span data-stu-id="fb1df-173">Working with communications</span></span>](managing-custodian-communications.md)
