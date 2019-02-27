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
ms.openlocfilehash: 95a1bcbbc279ad4e476fc479e701b0f8a921c83b
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295682"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="566e4-102">Управление custodians в расширенном варианте обнаружения электронных данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="566e4-102">Manage custodians in an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="566e4-p101">На вкладке custodians содержится список, поддерживающий сортировку всех custodians в случае. После добавления custodians в случае, сведения о каждом хранитель будут автоматически собраны из Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="566e4-p101">The Custodians tab contains a sortable list of all the custodians in the case. After you add custodians to a case, details about each custodian will automatically be collected from Azure Active Directory.</span></span>

## <a name="viewing-custodian-details"></a><span data-ttu-id="566e4-105">Просмотр сведений о хранитель</span><span class="sxs-lookup"><span data-stu-id="566e4-105">Viewing custodian details</span></span>

<span data-ttu-id="566e4-p102">Всплывающая страница, содержащая сведения о хранитель, появляется после добавления хранитель к обращению и выбора их из списка на вкладке **custodians** . Отсюда вы можете просмотреть все сведения, относящиеся к этой хранитель. Всплывающая страница содержит следующие поля:</span><span class="sxs-lookup"><span data-stu-id="566e4-p102">The flyout page that contains custodian details appears after you add a custodian to a case and select them from the list on the **Custodians** tab. From here, you can view all the details related to that custodian. The flyout page contains the following fields:</span></span>

- <span data-ttu-id="566e4-108">Контактные данные</span><span class="sxs-lookup"><span data-stu-id="566e4-108">Contact information</span></span>

  - <span data-ttu-id="566e4-p103">**ОтображаемОе имя**: имя, отображаемое в адресной книге для хранитель. Обычно это сочетание имени, инициала и фамилии хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-p103">**Display Name**: The name displayed in the address book for the custodian. This is usually the combination of the custodian’s first name, middle initial and last name.</span></span>
  - <span data-ttu-id="566e4-111">**Mail/SMTP**: SMTP-адрес для хранитель, например Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="566e4-111">**Mail/SMTP**: The SMTP address for the custodian, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="566e4-112">**Название**: название задания хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-112">**Title**: The custodian’s job title.</span></span>
  - <span data-ttu-id="566e4-113">**Отдел**: имя отдела, в котором работает хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-113">**Department**: The name for the department in which the custodian works.</span></span>
  - <span data-ttu-id="566e4-p104">**Руководитель**: менеджер хранитель. Указанный руководитель получит все сообщения о эскалации для этого хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-p104">**Manager**: The custodian’s manager. The designated manager will receive any Escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="566e4-116">Сведения о расположении</span><span class="sxs-lookup"><span data-stu-id="566e4-116">Location information</span></span>

  - <span data-ttu-id="566e4-117">**City**: город, в котором располагается хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-117">**City**: The city in which the custodian is located.</span></span>
  - <span data-ttu-id="566e4-118">**Состояние**: область или край в адресе хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-118">**State**: The state or province in the custodian’s address.</span></span>
  - <span data-ttu-id="566e4-119">**Страна или регион**: страна или регион, в котором размещается хранитель; Например, "US" или "Великобритания".</span><span class="sxs-lookup"><span data-stu-id="566e4-119">**Country/Region**: The country/region in which the custodian’s is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="566e4-120">**Office**: расположение офиса в Организации хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-120">**Office**: The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="566e4-121">Сведения о делах</span><span class="sxs-lookup"><span data-stu-id="566e4-121">Case information</span></span>

  - <span data-ttu-id="566e4-122">**Состояние удержания**: указывает, был ли хранитель включен в удержание.</span><span class="sxs-lookup"><span data-stu-id="566e4-122">**Hold status**: Indicates if the custodian has been placed on hold.</span></span> 
  - <span data-ttu-id="566e4-p105">**Состояние связи**: указывает, было ли хранитель было создано уведомление об удержании. Если для хранитель было создано уведомление, оно будет помечено как опубликованное. \*\* Если уведомление о хранитель еще не выдано, то этот статус будет *отменен*.</span><span class="sxs-lookup"><span data-stu-id="566e4-p105">**Communication status**: Indicates if the custodian has been issued a hold notice. If the custodian has been issued a notice, then this will be marked as *Published*. If the custodian has not been issued a notice, then this status will be *Un-Published*.</span></span> 
  - <span data-ttu-id="566e4-p106">**Состояние**: состояние хранитель в случае. Она будет *активна* , если Хранитель по-прежнему находится на удержании для обращения. Если хранитель удаляется из случая, его состояние изменится на " *выпущено*".</span><span class="sxs-lookup"><span data-stu-id="566e4-p106">**Status**: The status of the custodian within the case. This will be *Active* if the custodian is still on hold for the case. If a custodian is removed from a case, their status will change to *Released*.</span></span> 

- <span data-ttu-id="566e4-129">Состояние обработки</span><span class="sxs-lookup"><span data-stu-id="566e4-129">Processing status</span></span>

  - <span data-ttu-id="566e4-130">**Состояние индексирования**: указывает состояние задания глубокого индексирования.</span><span class="sxs-lookup"><span data-stu-id="566e4-130">**Indexing status**: Indicates the status of the deep indexing job.</span></span>  
  - <span data-ttu-id="566e4-131">**Время последнего обновления индексации**: указывает Дата при последнем запуске задания глубокого индексирования.</span><span class="sxs-lookup"><span data-stu-id="566e4-131">**Indexing Last Updated Time**: Indicates the datestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="566e4-132">**Источники данных**: показывает количество почтовых ящиков, сайтов и команд, выбранных для хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-132">**Data sources**: Shows the count of mailboxes, sites, and Teams that have been selected for the custodian.</span></span>

## <a name="updating-a-custodian"></a><span data-ttu-id="566e4-133">Обновление хранитель</span><span class="sxs-lookup"><span data-stu-id="566e4-133">Updating a custodian</span></span>

<span data-ttu-id="566e4-p107">Как и в случае с ходом выполнения, может возникнуть необходимость в наличии дополнительных источников данных, относящихся к определенному хранитель _Амп_ вашем случае. В других сценариях может потребоваться удалить некоторые источники данных, которые были проверены и были признаны несвязанными.</span><span class="sxs-lookup"><span data-stu-id="566e4-p107">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case. In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="566e4-136">Чтобы обновить хранитель и выбранные источники данных, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="566e4-136">To update a custodian and the selected data sources:</span></span>

1. <span data-ttu-id="566e4-137">Выберите существующее обращение из расширенного **обнаружения электронных данных _гт_ (предварительНая версия)**.</span><span class="sxs-lookup"><span data-stu-id="566e4-137">Select an existing case from the **eDiscovery > Advanced eDiscovery (Preview)**.</span></span>
  
2. <span data-ttu-id="566e4-138">В случае откройте вкладку **custodians** .</span><span class="sxs-lookup"><span data-stu-id="566e4-138">In the case, click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="566e4-139">Выберите хранитель в списке и нажмите кнопку **изменить источники**.</span><span class="sxs-lookup"><span data-stu-id="566e4-139">Select the custodian(s) from the list and click **Edit sources**.</span></span>
  
4. <span data-ttu-id="566e4-140">Обновите параметры для расположений Exchange и OneDrive, нажав кнопку **Выбор источников данных**.</span><span class="sxs-lookup"><span data-stu-id="566e4-140">Update selections for Exchange and OneDrive locations by clicking **Choose data sources**.</span></span>
  
5. <span data-ttu-id="566e4-p108">Добавление или удаление командных почтовых ящиков, SharePoint или Exchange, сопоставленных пользователю, путем **выбора дополнительных источников данных**. Дополнительные сведения о том, как сопоставить источники данных с хранитель, можно узнать в статье [Add custodians to a](add-custodians-to-case.md).</span><span class="sxs-lookup"><span data-stu-id="566e4-p108">Add or remove Teams, SharePoint, or Exchange mailboxes mapped the user by clicking to **Select additional data sources**. For more information about how you to map data sources to a custodian, see [Add custodians to a case](add-custodians-to-case.md).</span></span>
  
6. <span data-ttu-id="566e4-143">Чтобы обновить состояние удержания хранитель, нажмите кнопку **поместить кустодиал**, а затем включите или отключите удержание для custodians.</span><span class="sxs-lookup"><span data-stu-id="566e4-143">To update the custodian hold status, click **Place custodial holds**, and enable or disable the hold for custodians.</span></span>

> [!TIP]
> <span data-ttu-id="566e4-144">Можно выбрать несколько custodians для выполнения пакетных действий, например переиндексации, освобождения или редактирования набора custodians.</span><span class="sxs-lookup"><span data-stu-id="566e4-144">You can select multiple custodians to perform bulk actions, like re-indexing, releasing, or editing a set of custodians.</span></span>

## <a name="resolving-custodian-processing-errors"></a><span data-ttu-id="566e4-145">Устранение ошибок обработки хранитель</span><span class="sxs-lookup"><span data-stu-id="566e4-145">Resolving custodian processing errors</span></span>

<span data-ttu-id="566e4-p109">В большинстве юридических бизнес-процессов после добавления custodians для определенного исследования будет выполнен поиск подмножества данных пользователей. Из-за больших размеров файлов или возможных повреждений некоторые элементы в источниках данных custodians могут быть частично индексированы. С помощью расширенной функции индексирования (расширенного режима обнаружения электронных данных) эти частично индексированные элементы можно автоматически исправить путем повторного обхода и повторного индексирования этих элементов по запросу.</span><span class="sxs-lookup"><span data-stu-id="566e4-p109">In most Legal workflows, after custodians are added for a specific investigation, a subset of the users’ data will be searched. Due to large file sizes or possible corruption, some items within the custodians’ data sources may be partially indexed. Using the Advanced eDiscovery (Preview) deep indexing capability, these partially indexed items can be automatically remediated by re-crawling and re-indexing these items on demand.</span></span> 

<span data-ttu-id="566e4-p110">Когда хранитель добавляется к случаю, их данные автоматически будут иметь глубокий индекс, что позволит пользователям оставить эти элементы с частичным индексированием, а не загружать, исправить и повторно выполнять поиск вне Office 365. Во время жизненного цикла пользователь может исправить элементы или добавить новые источники данных для конкретного хранитель. Для этого может потребоваться обновление индекса хранитель.</span><span class="sxs-lookup"><span data-stu-id="566e4-p110">When a custodian is added to a case, their data will automatically be "deep indexed”, allowing users to leave these partially indexed items in place instead of having to download, remediate and re-run searches outside of Office 365. During the lifecycle of a case, a user may remediate items or add new data sources for a given custodian. This may require the Custodian Index to be updated.</span></span> 

<span data-ttu-id="566e4-152">Чтобы запустить процесс повторного индексирования для частично индексированных элементов:</span><span class="sxs-lookup"><span data-stu-id="566e4-152">To trigger a re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="566e4-153">Перейдите на **Обнаружение электронных данных _Гт_ Advanced eDiscovery (предварительНая версия)** и выберите существующее обращение.</span><span class="sxs-lookup"><span data-stu-id="566e4-153">Go to **eDiscovery > Advanced eDiscovery (Preview)** and select an existing case.</span></span>

2. <span data-ttu-id="566e4-154">В случае откройте **вкладку custodians**.</span><span class="sxs-lookup"><span data-stu-id="566e4-154">In the case, click to **Custodians tab**.</span></span> 

3. <span data-ttu-id="566e4-155">Выберите хранитель, для которых необходимо выполнить повторное индексирование, а затем нажмите кнопку **обновить индекс** на всплывающей странице.</span><span class="sxs-lookup"><span data-stu-id="566e4-155">Select the custodian(s) that needs to be re-indexed, and then click **Update index** on the flyout page.</span></span>

4. <span data-ttu-id="566e4-156">Проверьте состояние индекса хранитель, щелкнув ссылку в столбце " **состояние задания индексирования** " на вкладке " **custodians** ".</span><span class="sxs-lookup"><span data-stu-id="566e4-156">Check the status of the custodian index by clicking the link in the **Indexing job Status** column on the **Custodians** tab.</span></span>  

5. <span data-ttu-id="566e4-157">Состояние процесса повторной индексации также можно отслеживать на вкладке **задания** .</span><span class="sxs-lookup"><span data-stu-id="566e4-157">The status for the re-indexing process can also be tracked on the **Jobs** tab.</span></span>

<span data-ttu-id="566e4-158">Дополнительные сведения о возможностях повторного индексирования и устранение частичных индексированных элементов приведены в разделе [Устранение ошибок обработки](processing-data-for-case.md).</span><span class="sxs-lookup"><span data-stu-id="566e4-158">For more information about re-indexing and remediating partially indexed items, see [Fix processing errors](processing-data-for-case.md).</span></span>

## <a name="releasing-a-custodian-from-a-case"></a><span data-ttu-id="566e4-159">Выпуск хранитель из обращения</span><span class="sxs-lookup"><span data-stu-id="566e4-159">Releasing a custodian from a case</span></span>

<span data-ttu-id="566e4-160">Хранитель размещается в ситуациях, когда обращение закрывается, хранитель не находится в обязательстве по сохранению содержимого для случая или когда хранитель считается нерелевантным для конкретного случая.</span><span class="sxs-lookup"><span data-stu-id="566e4-160">A custodian is released in situations where a case is closed, a custodian is no longer under obligation to preserve content for a case, or when a custodian is deemed to no longer be relevant to a particular case.</span></span> 

<span data-ttu-id="566e4-p111">Если вы выпустите хранитель после публикации уведомления об удержании, в Хранитель будет отправлено уведомление о выпуске. Кроме того, все кустодиал, содержащие атрибуты для выпущенных custodians, также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="566e4-p111">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian. In addition, any custodial holds attributed to the released custodians will also be removed.</span></span>

<span data-ttu-id="566e4-163">Если хранитель было размещено в автоматическом удержании, где оно не выдавало уведомлений о юридическом удержании, то любые кустодиал, помеченные для выпущенного custodians, будут удалены.</span><span class="sxs-lookup"><span data-stu-id="566e4-163">If the custodian was placed on a silent hold, where they were not issued any legal hold notifications, then any custodial holds attributed to the released custodians will be removed.</span></span>  

<span data-ttu-id="566e4-164">Чтобы освободить хранитель, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="566e4-164">To release a custodian:</span></span> 

1.  <span data-ttu-id="566e4-165">Перейдите на вкладку **custodians** .</span><span class="sxs-lookup"><span data-stu-id="566e4-165">Go to the **Custodians** tab.</span></span>

2.  <span data-ttu-id="566e4-166">Выберите хранитель в списке и нажмите кнопку **освободить custodians** на всплывающей странице.</span><span class="sxs-lookup"><span data-stu-id="566e4-166">Select the custodian from the list and click **Release custodians** on the flyout page.</span></span>

    <span data-ttu-id="566e4-167">Состояние хранитель на вкладке **custodians** установлено на "отключено", \*\*\*\* а **состояние хранения** на всплывающей странице изменяется на неактивное \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="566e4-167">The status of the custodian on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **Inactive**.</span></span> 

> [!TIP]
> <span data-ttu-id="566e4-p112">Хранитель может быть одновременно задействована в нескольких юридических удержаниях. Когда хранитель выпускается из случая, не будут затронуты удержания и уведомления по другим параметрам.</span><span class="sxs-lookup"><span data-stu-id="566e4-p112">A custodian might be simultaneously be involved in several legal hold matters. When a custodian is released from a case, the holds and notifications across other matters will not be impacted.</span></span>

## <a name="related-information"></a><span data-ttu-id="566e4-170">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="566e4-170">Related information</span></span>

 - [<span data-ttu-id="566e4-171">Исправление ошибок при обработке данных</span><span class="sxs-lookup"><span data-stu-id="566e4-171">Error remediation when processing data</span></span>](error-remediation.md) 
- [<span data-ttu-id="566e4-172">Работа с взаимодействием</span><span class="sxs-lookup"><span data-stu-id="566e4-172">Work with communications</span></span>](managing-custodian-communications.md)
