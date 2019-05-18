---
title: Управление custodians в расширенном случае обнаружения электронных данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d9806ecbc23f46ee2d39f8d7e6be07af0d6a83e8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151621"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-case"></a><span data-ttu-id="dd6b5-102">Управление custodians в расширенном случае обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="dd6b5-102">Manage custodians in an Advanced eDiscovery case</span></span>

<span data-ttu-id="dd6b5-103">На вкладке custodians (Расширенное обнаружение электронных данных) содержится список всех custodians, которые были добавлены в обращение.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-103">The Custodians tab in Advanced eDiscovery contains a list of all custodians that have been added to the case.</span></span> <span data-ttu-id="dd6b5-104">Когда вы добавите custodians в дело, сведения о каждом из них автоматически собираются из Azure Active Directory и доступны для просмотра в Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-104">After you add custodians to a case, details about each custodian are automatically collected from Azure Active Directory and are viewable in Advanced eDiscovery.</span></span>

![Управление custodians](../media/CustodianDetails.PNG)

## <a name="view-custodian-details"></a><span data-ttu-id="dd6b5-106">Просмотр сведений о хранитель</span><span class="sxs-lookup"><span data-stu-id="dd6b5-106">View custodian details</span></span>

<span data-ttu-id="dd6b5-107">Чтобы просмотреть сведения о хранитель, щелкните хранитель в списке на вкладке **custodians** . Откроется всплывающая страница со следующими сведениями о хранитель:</span><span class="sxs-lookup"><span data-stu-id="dd6b5-107">To view the details about a custodian, click the custodian from the list on the **Custodians** tab. A flyout page is displayed and contains the following information about the custodian:</span></span>

- <span data-ttu-id="dd6b5-108">Контактные данные</span><span class="sxs-lookup"><span data-stu-id="dd6b5-108">Contact information</span></span>

  - <span data-ttu-id="dd6b5-109">**Display Name** — имя, отображаемое в адресной книге для хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-109">**Display Name** - The name displayed in the address book for the custodian.</span></span> <span data-ttu-id="dd6b5-110">Обычно это сочетание имени, инициала и фамилии хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-110">This is usually the combination of the custodian’s first name, middle initial, and last name.</span></span>
  
   - <span data-ttu-id="dd6b5-111">**Mail/SMTP** — основной SMTP-адрес для хранитель, например brianj@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-111">**Mail/SMTP** - The primary SMTP address for the custodian, for example, brianj@contoso.onmicrosoft.com.</span></span> <span data-ttu-id="dd6b5-112">Обратите внимание, что также указано имя участника-пользователя хранитель (UPN).</span><span class="sxs-lookup"><span data-stu-id="dd6b5-112">Note that the custodian's user principal name (UPN) is also listed.</span></span>

  - <span data-ttu-id="dd6b5-113">**Title** — название задания хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-113">**Title** - The custodian’s job title.</span></span>

  - <span data-ttu-id="dd6b5-114">**Department** — имя отдела, в котором работает хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-114">**Department** - The name for the department in which the custodian works.</span></span>

  - <span data-ttu-id="dd6b5-115">**Руководитель** — менеджер хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-115">**Manager** - The custodian’s manager.</span></span> <span data-ttu-id="dd6b5-116">Указанный руководитель получит все сообщения о эскалации для этого хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-116">The designated manager will receive any escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="dd6b5-117">Сведения о расположении</span><span class="sxs-lookup"><span data-stu-id="dd6b5-117">Location information</span></span>

  - <span data-ttu-id="dd6b5-118">**City** — город, в котором располагается хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-118">**City** - The city in which the custodian is located.</span></span>

  - <span data-ttu-id="dd6b5-119">**State** — область или край в адресе хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-119">**State** - The state or province in the custodian’s address.</span></span>

  - <span data-ttu-id="dd6b5-120">**Страна** или регион — страна или регион, где находится хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-120">**Country/Region** - The country/region where the custodian’s is located.</span></span>

  - <span data-ttu-id="dd6b5-121">**Office** — расположение комнаты бизнеса в хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-121">**Office** - The office location in the custodian’s place of business.</span></span>

- <span data-ttu-id="dd6b5-122">Сведения о делах</span><span class="sxs-lookup"><span data-stu-id="dd6b5-122">Case information</span></span>

  - <span data-ttu-id="dd6b5-123">**Состояние удержания** — указывает, был ли хранитель включен в удержание.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-123">**Hold status** - Indicates if the custodian has been placed on hold.</span></span> 

  - <span data-ttu-id="dd6b5-124">**Состояние связи**: указывает, было ли хранитель было создано уведомление об удержании.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-124">**Communication status**: Indicates if the custodian has been issued a hold notice.</span></span> <span data-ttu-id="dd6b5-125">Если хранитель было создано уведомление, это значение этого свойства **публикуется**.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-125">If the custodian has been issued a notice, this value of this property is **Published**.</span></span> <span data-ttu-id="dd6b5-126">Если хранитель не выдал уведомление, состояние отменяется. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd6b5-126">If the custodian has not been issued a notice, the status is **Un-published**.</span></span> 

  - <span data-ttu-id="dd6b5-127">**Status (состояние** ) — состояние хранитель в случае.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-127">**Status** - The status of the custodian within the case.</span></span> <span data-ttu-id="dd6b5-128">Состояние **Active** указывает на то, что хранитель является частью дела.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-128">A status of **Active** indicates that the custodian is part of the case.</span></span> <span data-ttu-id="dd6b5-129">Если хранитель выпускается из случая, состояние изменится на " **выпущен**".</span><span class="sxs-lookup"><span data-stu-id="dd6b5-129">If a custodian is released from a case, the status is changed to **Released**.</span></span> 

- <span data-ttu-id="dd6b5-130">Источники данных и сведения об индексировании</span><span class="sxs-lookup"><span data-stu-id="dd6b5-130">Data sources and indexing information</span></span>

    - <span data-ttu-id="dd6b5-131">**Источники данных** — отображает количество и тип источников данных (почтовые ящики, сайты и команды), которые связаны с хранитель и являются частью этого случая.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-131">**Data sources** - Shows the count and type of data sources (mailboxes, sites, and Teams) that are associated with the custodian and are part of the case.</span></span>

    - <span data-ttu-id="dd6b5-132">**Обновлять время индексирования** — указывает время и дату последнего запуска задания расширенного индексирования.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-132">**Index updated time** - Indicates the time and date for when the advanced indexing job was last triggered.</span></span> <span data-ttu-id="dd6b5-133">Это свойство также указывает, когда в данный момент выполняется расширенный процесс индексирования.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-133">This property will also indicate when the advanced indexing process is currently in progress.</span></span>


## <a name="edit-a-custodian"></a><span data-ttu-id="dd6b5-134">Изменение хранитель</span><span class="sxs-lookup"><span data-stu-id="dd6b5-134">Edit a custodian</span></span>

<span data-ttu-id="dd6b5-135">Как и в случае с ходом выполнения, может возникнуть необходимость в наличии дополнительных источников данных, относящихся к определенному хранитель _Амп_ вашем случае.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-135">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case.</span></span> <span data-ttu-id="dd6b5-136">В других сценариях может потребоваться удалить некоторые источники данных, которые были проверены и были признаны несвязанными.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-136">In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="dd6b5-137">Обновление источников данных, связанных с хранитель:</span><span class="sxs-lookup"><span data-stu-id="dd6b5-137">To update the data sources that are associated with a custodian:</span></span>

1. <span data-ttu-id="dd6b5-138">Перейдите на **Обнаружение электронных данных _Гт_ Advanced eDiscovery** и откройте обращение.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-138">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>
  
2. <span data-ttu-id="dd6b5-139">Перейдите на вкладку **custodians** .</span><span class="sxs-lookup"><span data-stu-id="dd6b5-139">Click the **Custodians** tab.</span></span>
  
3. <span data-ttu-id="dd6b5-140">Выберите хранитель в списке и нажмите кнопку **изменить** на всплывающей странице.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-140">Select a custodian from the list and click **Edit** on the flyout page.</span></span>

    ![Изменение источников данных](../media/EditCustodianDataSource.PNG)
  
4. <span data-ttu-id="dd6b5-142">Нажмите кнопку **Выбор источников данных** , чтобы изменить параметры почтового ящика Exchange и учетной записи OneDrive хранитель, и выберите пункт **выбрать источники данных**.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-142">Click **Choose data sources** tab to change the settings for the custodian's Exchange mailbox and OneDrive account, click **Choose data sources**.</span></span>
  
5. <span data-ttu-id="dd6b5-143">Перейдите на вкладку **выберите Дополнительные источники данных** , чтобы добавить или удалить Teams, SharePoint или почтовые ящики Exchange, связанные с хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-143">Click the **Select additional data sources** tab to add or remove Teams, SharePoint, or Exchange mailboxes associated with the custodian.</span></span> 

    <span data-ttu-id="dd6b5-144">Для получения дополнительных сведений об источниках данных, связанных с хранитель, обратитесь к разделу "шаг 3: связывание дополнительных источников данных с хранитель" в разделе [Add custodians to Case](add-custodians-to-case.md#step-3-associate-additional-data-sources-to-a-custodian).</span><span class="sxs-lookup"><span data-stu-id="dd6b5-144">For more information about data sources associated with a custodian, see "Step 3: Associate additional data sources to a custodian" in [Add custodians to a case](add-custodians-to-case.md#step-3-associate-additional-data-sources-to-a-custodian).</span></span> 
  
6. <span data-ttu-id="dd6b5-145">Нажмите кнопку **поместить кустодиал удержания** , чтобы включить или отключить удержание для хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-145">Click **Place custodial holds** to enable or disable the hold for the custodian.</span></span>

## <a name="resolve-custodian-processing-errors"></a><span data-ttu-id="dd6b5-146">Устранение ошибок обработки хранитель</span><span class="sxs-lookup"><span data-stu-id="dd6b5-146">Resolve custodian processing errors</span></span>

<span data-ttu-id="dd6b5-147">В большинстве рабочих процессов обнаружения электронных данных для юридического расследования подмножество данных хранитель ищется после добавления хранитель в юридическое обращение.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-147">In most eDiscovery workflows for legal investigations, a subset of a custodian's data is searched after the custodian is added to a legal case.</span></span> <span data-ttu-id="dd6b5-148">Из-за очень большого размера файлов или возможных повреждений данных некоторые элементы в источниках данных, связанных с хранитель, могут быть частично индексированы.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-148">Because of very large file sizes or possible data corruption, some items in the data sources associated with a custodian may be partially indexed.</span></span> <span data-ttu-id="dd6b5-149">С помощью [расширенной](indexing-custodian-data.md) функции индексирования расширенного обнаружения электронных данных большинство частично индексированных элементов можно автоматически исправить путем повторного индексирования этих элементов по запросу.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-149">Using the [advanced indexing](indexing-custodian-data.md) capability in the Advanced eDiscovery, most partially indexed items can be automatically remediated by re-indexing these items on demand.</span></span>

<span data-ttu-id="dd6b5-150">Когда хранитель добавляется к случаю, данные, расположенные в источниках данных, связанных с хранитель, автоматически переиндексируются автоматически (с помощью расширенного процесса индексирования).</span><span class="sxs-lookup"><span data-stu-id="dd6b5-150">When a custodian is added to a case, the data located in the data sources associated with the custodian is automatically re-indexed (by the advanced indexing process).</span></span> <span data-ttu-id="dd6b5-151">Это означает, что вы можете оставить данные на месте, а не загружать и исправлять их, а затем искать их в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-151">This means you can leave the data in-place instead of having to download and remediate it and then search it offline).</span></span> <span data-ttu-id="dd6b5-152">Однако во время жизненного цикла для юридического случая новые источники данных могут быть связаны с хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-152">However, during the lifecycle of a legal case new data sources might be associated to a custodian.</span></span> <span data-ttu-id="dd6b5-153">В этом случае выполняется повторное индексирование данных хранитель путем повторного выполнения расширенного процесса индексирования для исправления всех элементов с частичным индексированием и обновления индекса данных хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-153">In this case, you re-index the custodian's data by re-running the advanced indexing process to remediate any partially indexed items and update the index for the custodian's data.</span></span>

<span data-ttu-id="dd6b5-154">Чтобы запустить процесс повторного индексирования для частично индексированных элементов:</span><span class="sxs-lookup"><span data-stu-id="dd6b5-154">To trigger the re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="dd6b5-155">Перейдите на **Обнаружение электронных данных _Гт_ Advanced eDiscovery** и откройте обращение.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-155">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>

2. <span data-ttu-id="dd6b5-156">Перейдите на **вкладку custodians**, а затем выберите хранитель, данные которого необходимо переиндексировать.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-156">Click to **Custodians tab**, and then select a custodian whose data must be reindexed.</span></span> 

3. <span data-ttu-id="dd6b5-157">На всплывающей странице щелкните **обновить индекс**.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-157">On the flyout page, click **Update index**.</span></span>

   <span data-ttu-id="dd6b5-158">Отображается диалоговое окно с сообщением о том, что было создано задание индексирования.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-158">A dialog is displayed saying the index job has been created.</span></span>

<span data-ttu-id="dd6b5-159">Повторное индексирование данных хранитель — это длительный процесс; соответствующее созданное задание называется **повторная индексация данных хранитель**.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-159">Re-indexing custodian data is a long-running process; the corresponding job that's created is named **Re-indexing custodian data**.</span></span> <span data-ttu-id="dd6b5-160">Отслеживать ход выполнения можно на вкладке " **задания** " или на вкладке " **custodians** ", отслеживая состояние в столбце " **состояние задания индексирования** ".</span><span class="sxs-lookup"><span data-stu-id="dd6b5-160">You can track the progress on the **Jobs** tab or on the **Custodians** tab by monitoring the status in the **Indexing job status** column.</span></span>

<span data-ttu-id="dd6b5-161">Дополнительные сведения см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="dd6b5-161">For more information, see:</span></span>

- [<span data-ttu-id="dd6b5-162">Работа с ошибками обработки</span><span class="sxs-lookup"><span data-stu-id="dd6b5-162">Work with processing errors</span></span>](processing-data-for-case.md)

- [<span data-ttu-id="dd6b5-163">Управление заданиями</span><span class="sxs-lookup"><span data-stu-id="dd6b5-163">Manage jobs</span></span>](managing-jobs-ediscovery20.md)

## <a name="release-a-custodian-from-a-case"></a><span data-ttu-id="dd6b5-164">Выпуск хранитель из обращения</span><span class="sxs-lookup"><span data-stu-id="dd6b5-164">Release a custodian from a case</span></span>

<span data-ttu-id="dd6b5-165">Хранитель размещается в ситуациях, когда обращение закрывается, хранитель больше не считается обязательством по сохранению содержимого для случая или когда хранитель считается нерелевантным для случая.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-165">A custodian is released in situations where a case is closed, the custodian is no longer under obligation to preserve content for a case, or when the custodian is deemed to no longer be relevant to the case.</span></span> 

<span data-ttu-id="dd6b5-166">Если вы выпустите хранитель после публикации уведомления об удержании, в Хранитель будет отправлено уведомление о выпуске.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-166">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian.</span></span> <span data-ttu-id="dd6b5-167">Кроме того, удаляются все удержания, размещенные в источниках данных, связанных с хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-167">Additionally, any holds placed on data sources that were associated with the custodian are removed.</span></span> <span data-ttu-id="dd6b5-168">Если хранитель размещается на удержании в *автоматическом режиме*, где они не получали уведомления о юридическом удержании, уведомление о выпуске не будет отправлено, но все удержания, размещенные на источниках данных, связанных с этим хранитель, удаляются.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-168">If the custodian was placed on a *silent hold*, where they weren't issued any legal hold notifications, a release notice will not be sent but any holds placed on data sources that were associated with that custodian are removed.</span></span>

<span data-ttu-id="dd6b5-169">Чтобы освободить хранитель, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-169">To release a custodian:</span></span> 

1. <span data-ttu-id="dd6b5-170">Перейдите на **Обнаружение электронных данных _Гт_ Advanced eDiscovery** и откройте обращение.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-170">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>

2.  <span data-ttu-id="dd6b5-171">Перейдите на вкладку **custodians** .</span><span class="sxs-lookup"><span data-stu-id="dd6b5-171">Go to the **Custodians** tab.</span></span>

3.  <span data-ttu-id="dd6b5-172">Перейдите на **вкладку custodians**, а затем выберите хранитель, который выпускается из этого случая.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-172">Click to **Custodians tab**, and then select the custodian who is being released from the case.</span></span>

4. <span data-ttu-id="dd6b5-173">На всплывающей странице нажмите кнопку **Release хранитель**.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-173">On the flyout page, click **Release custodian**.</span></span>

   <span data-ttu-id="dd6b5-174">Будет выведена страница с предупреждением о том, что если удержание помещается в источник данных, связанный с хранитель, то удержание будет удалено и все остальные удержания, связанные с другими дополнительными случаями обнаружения электронных данных, будут по-прежнему применяться.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-174">A warning page is displayed explaining that if a hold is placed on a data source associated with the custodian, the hold will be removed, and that any other hold associated with a different Advanced eDiscovery case will still apply.</span></span> <span data-ttu-id="dd6b5-175">Включает другие типы сохранения и хранения в Office 365 (например, политика хранения Office 365).</span><span class="sxs-lookup"><span data-stu-id="dd6b5-175">That includes other types of preservation and retention features in Office 365 (such as an Office 365 retention policy).</span></span>

5. <span data-ttu-id="dd6b5-176">Нажмите кнопку **Да** , чтобы подтвердить, что вы хотите освободить хранитель.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-176">Click **Yes** to confirm that you want to release the custodian.</span></span> 

    <span data-ttu-id="dd6b5-177">Обратите внимание на то, что для этого пользователя на вкладке **custodians** задано значение "запущена", а **состояние удержания** для всплывающей страницы изменяется на " **false**". \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd6b5-177">Note that status for this user on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **False**.</span></span> 

> [!NOTE]
> <span data-ttu-id="dd6b5-178">Хранитель может быть одновременно задействована в нескольких юридических случаях.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-178">A custodian might be simultaneously involved in several legal cases.</span></span> <span data-ttu-id="dd6b5-179">При отпускании хранитель из случая удержания и уведомления на другие вопросы не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-179">When a custodian is released from a case, the holds and notifications across other matters won't be impacted.</span></span>

## <a name="bulk-edit-custodians"></a><span data-ttu-id="dd6b5-180">Массовое изменение custodians</span><span class="sxs-lookup"><span data-stu-id="dd6b5-180">Bulk-edit custodians</span></span>

<span data-ttu-id="dd6b5-181">Можно использовать пакетный редактор для одновременного редактирования нескольких custodians.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-181">You can use the bulk editor to edit multiple custodians as the same time.</span></span> <span data-ttu-id="dd6b5-182">Для этого достаточно выбрать два или более custodians на вкладке **custodians** , чтобы отобразить Пакетный редактор, а затем выбрать одну из задач.</span><span class="sxs-lookup"><span data-stu-id="dd6b5-182">To do this, just select two or more custodians on the **Custodians** tab to display the bulk editor and then click one of tasks.</span></span>

![Всплывающая страница для изменения параметров нескольких custodians](../media/AeDBulkEditCustodians.png)