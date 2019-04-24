---
title: Управление custodians в расширенном варианте обнаружения электронных данных (Предварительная версия)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 6a21240f71c64f244ee42c3d3a2ed9d75381edaa
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241868"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="b02b3-102">Управление custodians в расширенном варианте обнаружения электронных данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="b02b3-102">Manage custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="b02b3-103">На вкладке custodians содержится список, поддерживающий сортировку всех custodians в случае.</span><span class="sxs-lookup"><span data-stu-id="b02b3-103">The Custodians tab contains a sortable list of all the custodians in the case.</span></span> <span data-ttu-id="b02b3-104">После добавления custodians в случае, сведения о каждом хранитель будут автоматически собраны из Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b02b3-104">After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

![Управление custodians](../media/CustodianDetails.PNG)

## <a name="viewing-custodian-details"></a><span data-ttu-id="b02b3-106">Просмотр сведений о хранитель</span><span class="sxs-lookup"><span data-stu-id="b02b3-106">Viewing custodian details</span></span>

<span data-ttu-id="b02b3-107">Всплывающая страница, содержащая сведения о хранитель, появляется после добавления хранитель к обращению и выбора их из списка на вкладке **custodians** . Отсюда вы можете просмотреть все сведения, относящиеся к этой хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-107">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian.</span></span> <span data-ttu-id="b02b3-108">Всплывающая страница содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="b02b3-108">The flyout page contains the following fields:</span></span>

- <span data-ttu-id="b02b3-109">Контактные данные</span><span class="sxs-lookup"><span data-stu-id="b02b3-109">Contact information</span></span>

  - <span data-ttu-id="b02b3-110">**ОтображаемОе имя**: имя, отображаемое в адресной книге для хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-110">**Display Name**: The name displayed in the address book for the custodian.</span></span> <span data-ttu-id="b02b3-111">Обычно это сочетание имени, инициала и фамилии хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-111">This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="b02b3-112">**Mail/SMTP**: SMTP-адрес для хранитель, например Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="b02b3-112">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="b02b3-113">**Название**: название задания хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-113">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="b02b3-114">**Отдел**: имя отдела, в котором работает хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-114">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="b02b3-115">**Руководитель**: менеджер хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-115">**Manager**: The custodian’s manager.</span></span> <span data-ttu-id="b02b3-116">Указанный руководитель получит все сообщения о эскалации для этого хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-116">The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="b02b3-117">Сведения о расположении</span><span class="sxs-lookup"><span data-stu-id="b02b3-117">Location information</span></span>

  - <span data-ttu-id="b02b3-118">**City**: город, в котором располагается хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-118">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="b02b3-119">**Состояние**: область или край в адресе хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-119">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="b02b3-120">**Страна или регион**: страна или регион, в котором размещается хранитель; Например, "US" или "Великобритания".</span><span class="sxs-lookup"><span data-stu-id="b02b3-120">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="b02b3-121">**Office**: расположение офиса в Организации хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-121">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="b02b3-122">Сведения о делах</span><span class="sxs-lookup"><span data-stu-id="b02b3-122">Case information</span></span>

  - <span data-ttu-id="b02b3-123">**Состояние удержания**: указывает, был ли хранитель включен в удержание.</span><span class="sxs-lookup"><span data-stu-id="b02b3-123">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="b02b3-124">**Состояние связи**: указывает, было ли хранитель было создано уведомление об удержании.</span><span class="sxs-lookup"><span data-stu-id="b02b3-124">**Communication status**: Indicates if the custodian has been issued a hold notice.</span></span> <span data-ttu-id="b02b3-125">Если для хранитель было создано уведомление, оно будет помечено как опубликованное. \*\*</span><span class="sxs-lookup"><span data-stu-id="b02b3-125">If the custodian has been issued a notice, then this will be marked as *Published*.</span></span> <span data-ttu-id="b02b3-126">Если уведомление о хранитель еще не выдано, то этот статус будет *отменен*.</span><span class="sxs-lookup"><span data-stu-id="b02b3-126">If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="b02b3-127">**Состояние**: состояние хранитель в случае.</span><span class="sxs-lookup"><span data-stu-id="b02b3-127">**Status**: The status of the custodian within the case.</span></span> <span data-ttu-id="b02b3-128">Она будет *активна* , если Хранитель по-прежнему находится на удержании для обращения.</span><span class="sxs-lookup"><span data-stu-id="b02b3-128">This will be *Active* if the custodian is still on hold for the case.</span></span> <span data-ttu-id="b02b3-129">Если хранитель удаляется из случая, его состояние изменится на " *выпущено*".</span><span class="sxs-lookup"><span data-stu-id="b02b3-129">If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="b02b3-130">Состояние обработки</span><span class="sxs-lookup"><span data-stu-id="b02b3-130">Processing status</span></span>

  - <span data-ttu-id="b02b3-131">**Состояние индексирования**: указывает состояние задания глубокого индексирования.</span><span class="sxs-lookup"><span data-stu-id="b02b3-131">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="b02b3-132">**Время последнего обновления индексации**: указывает Дата при последнем запуске задания глубокого индексирования.</span><span class="sxs-lookup"><span data-stu-id="b02b3-132">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="b02b3-133">**Источники данных**: показывает количество почтовых ящиков, сайтов и команд, выбранных для хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-133">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="editing-a-custodian"></a><span data-ttu-id="b02b3-134">Изменение хранитель</span><span class="sxs-lookup"><span data-stu-id="b02b3-134">Editing a custodian</span></span>

<span data-ttu-id="b02b3-135">Как и в случае с ходом выполнения, может возникнуть необходимость в наличии дополнительных источников данных, относящихся к определенному хранитель _Амп_ вашем случае.</span><span class="sxs-lookup"><span data-stu-id="b02b3-135">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case.</span></span> <span data-ttu-id="b02b3-136">В других сценариях может потребоваться удалить некоторые источники данных, которые были проверены и были признаны несвязанными.</span><span class="sxs-lookup"><span data-stu-id="b02b3-136">In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="b02b3-137">Чтобы обновить хранитель и выбранные источники данных, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b02b3-137">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="b02b3-138">Выберите существующее обращение из расширенного **обнаружения электронных данных _гт_ (предварительНая версия)**.</span><span class="sxs-lookup"><span data-stu-id="b02b3-138">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="b02b3-139">В случае откройте вкладку **custodians** .</span><span class="sxs-lookup"><span data-stu-id="b02b3-139">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="b02b3-140">Выберите хранитель в списке и нажмите кнопку **изменить источники**.</span><span class="sxs-lookup"><span data-stu-id="b02b3-140">Select the custodian(s) from the list and click **Edit sources**.</span></span>

    ![Изменение источников данных](../media/EditCustodianDataSource.PNG)
  
4. <span data-ttu-id="b02b3-142">Обновите параметры для расположений Exchange и OneDrive, нажав кнопку **Выбор источников данных**.</span><span class="sxs-lookup"><span data-stu-id="b02b3-142">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="b02b3-143">Добавление или удаление командных почтовых ящиков, SharePoint или Exchange, сопоставленных пользователю, путем **выбора дополнительных источников данных**.</span><span class="sxs-lookup"><span data-stu-id="b02b3-143">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**.</span></span> <span data-ttu-id="b02b3-144">Дополнительные сведения о том, как сопоставить источники данных с хранитель, можно узнать в статье [Add custodians to a](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="b02b3-144">For more information about how you to map data sources to a custodian, see [Add custodians to a case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="b02b3-145">Чтобы обновить состояние удержания хранитель, нажмите кнопку **поместить кустодиал**, а затем включите или отключите удержание для custodians.</span><span class="sxs-lookup"><span data-stu-id="b02b3-145">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="b02b3-146">Можно выбрать несколько custodians для выполнения пакетных действий, например переиндексации, освобождения или редактирования набора custodians.</span><span class="sxs-lookup"><span data-stu-id="b02b3-146">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="b02b3-147">Устранение ошибок обработки хранитель</span><span class="sxs-lookup"><span data-stu-id="b02b3-147">Resolving custodian processing errors</span></span>

<span data-ttu-id="b02b3-148">В большинстве юридических бизнес-процессов после добавления custodians для определенного исследования будет выполнен поиск подмножества данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="b02b3-148">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched.</span></span> <span data-ttu-id="b02b3-149">Из-за больших размеров файлов или возможных повреждений некоторые элементы в источниках данных custodians могут быть частично индексированы.</span><span class="sxs-lookup"><span data-stu-id="b02b3-149">Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed.</span></span> <span data-ttu-id="b02b3-150">С помощью расширенной функции индексирования (расширенного режима обнаружения электронных данных) эти частично индексированные элементы можно автоматически исправить путем повторного обхода и повторного индексирования этих элементов по запросу.</span><span class="sxs-lookup"><span data-stu-id="b02b3-150">Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="b02b3-151">Когда хранитель добавляется к случаю, их данные автоматически будут иметь глубокий индекс, что позволит пользователям оставить эти элементы с частичным индексированием, а не загружать, исправить и повторно выполнять поиск вне Office 365.</span><span class="sxs-lookup"><span data-stu-id="b02b3-151">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365.</span></span> <span data-ttu-id="b02b3-152">Во время жизненного цикла пользователь может исправить элементы или добавить новые источники данных для конкретного хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-152">During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian.</span></span> <span data-ttu-id="b02b3-153">Для этого может потребоваться обновление индекса хранитель.</span><span class="sxs-lookup"><span data-stu-id="b02b3-153">This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="b02b3-154">Чтобы запустить процесс повторного индексирования для частично индексированных элементов:</span><span class="sxs-lookup"><span data-stu-id="b02b3-154">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="b02b3-155">Перейдите на **Обнаружение электронных данных _Гт_ Advanced eDiscovery (предварительНая версия)** и выберите существующее обращение.</span><span class="sxs-lookup"><span data-stu-id="b02b3-155">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="b02b3-156">В случае откройте **вкладку custodians**.</span><span class="sxs-lookup"><span data-stu-id="b02b3-156">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="b02b3-157">Выберите хранитель, для которых необходимо выполнить повторное индексирование, а затем нажмите кнопку</span><span class="sxs-lookup"><span data-stu-id="b02b3-157">Select the custodian(s) that needs to be re-indexed, and then click</span></span> ![Обновление индекса](../media/UpdateIndex.PNG) <span data-ttu-id="b02b3-159">на всплывающей странице.</span><span class="sxs-lookup"><span data-stu-id="b02b3-159">on the flyout page.</span></span>

4. <span data-ttu-id="b02b3-160">Проверьте состояние индекса хранитель, щелкнув ссылку в столбце " **состояние задания индексирования** " на вкладке " **custodians** ".</span><span class="sxs-lookup"><span data-stu-id="b02b3-160">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="b02b3-161">Состояние процесса повторной индексации также можно отслеживать на вкладке **задания** .</span><span class="sxs-lookup"><span data-stu-id="b02b3-161">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="b02b3-162">Дополнительные сведения о возможностях повторного индексирования и устранение частичных индексированных элементов приведены в разделе [Устранение ошибок обработки](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="b02b3-162">For more information about re-indexing and remediating partially indexed items, see [Fix processing errors](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="b02b3-163">Выпуск хранитель из обращения</span><span class="sxs-lookup"><span data-stu-id="b02b3-163">Releasing a custodian from a case</span></span>

<span data-ttu-id="b02b3-164">Хранитель размещается в ситуациях, когда обращение закрывается, хранитель не находится в обязательстве по сохранению содержимого для случая или когда хранитель считается нерелевантным для конкретного случая.</span><span class="sxs-lookup"><span data-stu-id="b02b3-164">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="b02b3-165">Если вы выпустите хранитель после публикации уведомления об удержании, в Хранитель будет отправлено уведомление о выпуске.</span><span class="sxs-lookup"><span data-stu-id="b02b3-165">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian.</span></span> <span data-ttu-id="b02b3-166">Кроме того, все кустодиал, содержащие атрибуты для выпущенных custodians, также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="b02b3-166">In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="b02b3-167">Если хранитель было размещено в автоматическом удержании, где оно не выдавало уведомлений о юридическом удержании, то любые кустодиал, помеченные для выпущенного custodians, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="b02b3-167">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="b02b3-168">Чтобы освободить хранитель, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b02b3-168">To release a custodian:</span></span> 

1.  <span data-ttu-id="b02b3-169">Перейдите на вкладку **custodians** .</span><span class="sxs-lookup"><span data-stu-id="b02b3-169">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="b02b3-170">Выберите хранитель в списке и нажмите кнопку</span><span class="sxs-lookup"><span data-stu-id="b02b3-170">Select the custodian from the list and click</span></span> ![Выпуск хранитель](../media/ReleaseCustodian.PNG) <span data-ttu-id="b02b3-172">на всплывающей странице.</span><span class="sxs-lookup"><span data-stu-id="b02b3-172">on the flyout page.</span></span>

    <span data-ttu-id="b02b3-173">Состояние хранитель на вкладке **custodians** установлено на "отключено", \*\*\*\* а **состояние хранения** на всплывающей странице изменяется на неактивное \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="b02b3-173">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="b02b3-174">Хранитель может быть одновременно задействована в нескольких юридических удержаниях.</span><span class="sxs-lookup"><span data-stu-id="b02b3-174">A custodian might be simultaneously be involved in several legal hold matters.</span></span> <span data-ttu-id="b02b3-175">Когда хранитель выпускается из случая, не будут затронуты удержания и уведомления по другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="b02b3-175">When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="b02b3-176">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="b02b3-176">Related information</span></span>

 - [<span data-ttu-id="b02b3-177">Исправление ошибок при обработке данных</span><span class="sxs-lookup"><span data-stu-id="b02b3-177">Error remediation when processing data</span></span>](error-remediation.md) 
- [<span data-ttu-id="b02b3-178">Работа с взаимодействием</span><span class="sxs-lookup"><span data-stu-id="b02b3-178">Work with communications</span></span>](managing-custodian-communications.md)
