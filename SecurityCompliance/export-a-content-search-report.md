---
title: Экспорт отчета о поиске контента
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/25/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Вместо Экспорт фактические результаты поиска контента в Office 365 безопасность &amp; центре соответствия требованиям, можно просто экспортировать отчет о результатах поиска. Отчет содержит сводку результатов поиска и документа с подробными сведениями об каждого элемента, который будет экспортирован.
ms.openlocfilehash: 45415f25754b4549a919e4ce56853a6ae09a9bdc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534254"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="8e9b1-104">Экспорт отчета о поиске контента</span><span class="sxs-lookup"><span data-stu-id="8e9b1-104">Export a Content Search report</span></span>

<span data-ttu-id="8e9b1-105">Вместо Экспорт полного набора поиска результаты из поиска контента в Office 365 безопасность &amp; центре соответствия требованиям (и из поиска контента, связанной с вариантом eDiscovery), можно экспортировать только что же отчеты, которые можно, возникающие при вы Экспорт результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-105">Instead of exporting the full set of search results from a Content Search in the Office 365 Security &amp; Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can just export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="8e9b1-p102">При экспорте отчета, его загружается в папку, которая имеет то же имя, как поиск контента, но, который используется в качестве с *_ReportsOnly* . Например если поиск содержимого с именем *ContosoCase0815* , отчет будет загружен в папку с именем *ContosoCase0815_ReportsOnly* . Список документов, которые включены в отчет в разделе [возможностей, включенных в отчет](#whats-included-in-the-report).</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p102">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with  *_ReportsOnly*  . For example, if the Content Search is named  *ContosoCase0815*  , then the report is downloaded to a folder named  *ContosoCase0815_ReportsOnly*  . For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="8e9b1-109">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="8e9b1-109">Before you begin</span></span>

- <span data-ttu-id="8e9b1-p103">Чтобы экспортировать отчет поиска контента, необходимо назначить роль управления поиска соответствия требованиям безопасности Office 365 &amp; центре соответствия требованиям. Эта роль назначается встроенных eDiscovery Manager и управление организацией группы ролей. Он не будет назначен по умолчанию в группу ролей управления организацией. Дополнительные сведения можно [назначать разрешения обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p103">To export a Content Search report, you have to be assigned the Compliance Search management role in the Office 365 Security &amp; Compliance Center. This role is assigned to the built-in eDiscovery Manager and Organization Management role groups. It isn't assigned by default to the Organization Management role group. For more information, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="8e9b1-p104">При экспорте отчета временно хранятся данные в уникальные области хранения Windows Azure в облаке Майкрософт перед загрузкой на локальный компьютер. Убедитесь, что ваша организация может подключаться к конечной точке в Azure, который является \*\* \*. blob.core.windows.net\*\* (подстановочный знак представляет уникальный идентификатор для экспорта). Результаты поиска удален из области хранилища Azure две недели после его создания.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p104">When you export a report, the data is temporarily stored in a unique Windows Azure storage area in the Microsoft cloud before it's downloaded to your local computer. Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export). The search results data is deleted from the Azure storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="8e9b1-117">Компьютер, который вы используете для экспорта результатов поиска, должен соответствовать указанным ниже требованиям к системе.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="8e9b1-118">32- или 64-разрядный выпуск Windows 7 и более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-118">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="8e9b1-119">Microsoft .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="8e9b1-119">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="8e9b1-120">Поддерживаемый браузер:</span><span class="sxs-lookup"><span data-stu-id="8e9b1-120">A supported browser:</span></span>
    
    - <span data-ttu-id="8e9b1-121">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8e9b1-121">Microsoft Edge</span></span>
    
      <span data-ttu-id="8e9b1-122">или</span><span class="sxs-lookup"><span data-stu-id="8e9b1-122">or</span></span>
    
    - <span data-ttu-id="8e9b1-123">Microsoft Internet Explorer 10 и более поздних версий</span><span class="sxs-lookup"><span data-stu-id="8e9b1-123">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="8e9b1-p105">**Примечание:** Корпорация Майкрософт не производит расширения сторонних производителей или надстройки для приложения ClickOnce. Экспорт результатов поиска, используете неподдерживаемый браузер с расширениями сторонних производителей или надстройки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p105">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 
    
## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="8e9b1-126">Создание и загрузка отчетов поиска контента</span><span class="sxs-lookup"><span data-stu-id="8e9b1-126">Generate and download a Content Search report</span></span>

<span data-ttu-id="8e9b1-127">Действия для создания и загрузить отчет поиска контента очень похожи на самом деле Экспорт результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-127">The steps to generate and download a Content Search report are very similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="8e9b1-128">Шаг 1: Создание отчета для экспорта</span><span class="sxs-lookup"><span data-stu-id="8e9b1-128">Step 1: Generate the report for export</span></span>

<span data-ttu-id="8e9b1-p106">Первый шаг состоит в подготовке отчета по загрузке на экспорт вашего компьютера. Когда вы отчета, отчет, который документы можно было выгрузить в область хранилища Azure в корпорации Майкрософт в облаке.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p106">The first step is to prepare the report for downloading to your computer exporting. When you the report, the report documents are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="8e9b1-131">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="8e9b1-131">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="8e9b1-132">Войдите в Office 365 с помощью учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-132">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="8e9b1-133">В расположенной слева области Центра безопасности и соответствия требованиям щелкните **Поиск и исследования** \> **Поиск контента**.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-133">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="8e9b1-134">На странице " **Поиск контента** " выберите поиск.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-134">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="8e9b1-135">В области сведений в разделе **Экспорт отчета на компьютер**, нажмите кнопку **Создать отчет**.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-135">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8e9b1-p107">Если результаты поиска не старше 7 дней, вам будет предложено обновление результатов поиска. В этом случае отменить экспорт, нажмите кнопку **Update результатов поиска** в области сведений для выбранного поиска и затем снова запустите экспорта отчетов после обновления результаты.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p107">If the results for a search are older than 7 days, you are prompted to update the search results. If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="8e9b1-138">На странице " **Экспорт отчета** " в разделе **Включить эти элементы из поиска**выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="8e9b1-138">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="8e9b1-139">Экспортировать только индексированные элементы.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-139">Export only indexed items</span></span>
    
    - <span data-ttu-id="8e9b1-140">Экспортировать индексированные и неиндексированные элементы.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-140">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="8e9b1-141">Экспортировать только неиндексированные элементы.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-141">Export only unindexed items</span></span>
    
    <span data-ttu-id="8e9b1-142">Дополнительные сведения об элементах неиндексированные можно [частично индексированных элементов в поиска контента](partially-indexed-items-in-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="8e9b1-142">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="8e9b1-p108">Выбор для включения поиска статистики для всех версий документов SharePoint. Этот параметр доступен только в том случае, если источники контента поиска включает в себя SharePoint или OneDrive для бизнеса сайтов.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p108">Choose to include search statistics for all versions of SharePoint documents. This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="8e9b1-145">Нажмите кнопку **Создать отчет**.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-145">Click **Generate report**.</span></span>
    
    <span data-ttu-id="8e9b1-p109">Отчет о результатах поиска, подготовленного для загрузки, что означает, что документы отчетов будет отправлен в область хранилища Azure в облаке Майкрософт. Когда отчет будет готов для загрузки, ссылку **загрузить отчет** отображается в списке **экспортировать отчет на компьютер** в области сведений.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p109">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure storage area in the Microsoft cloud. When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8e9b1-p110">Также можно экспортировать отчет для поиска контента, связанной с вариантом eDiscovery. Для этого перейдите к **поиска &amp; расследования** \> выберите дела **обнаружения электронных данных**и нажмите кнопку **Изменить** ![значок Правка](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). На странице " **Поиск** " выберите Поиск и нажмите кнопку **Экспорт** ![результатов поиска в экспорта значок](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Экспорт отчета**.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p110">You can also export a report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Searches** page, select a search, and then click **Export** ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="8e9b1-151">Шаг 2: Загрузить отчет</span><span class="sxs-lookup"><span data-stu-id="8e9b1-151">Step 2: Download the report</span></span>

<span data-ttu-id="8e9b1-152">Следующим шагом является можно загрузить отчет из области Azure хранилища для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-152">The next step is to download the report from the Azure storage area to your local computer.</span></span>
  
1. <span data-ttu-id="8e9b1-153">В области сведений для поиска, что создан отчет, в разделе **Экспорт отчета на компьютер**нажмите кнопку **загрузить отчет**.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-153">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="8e9b1-154">Страница **загрузить отчет** отображается и содержит следующие сведения об отчете до загрузить на свой компьютер.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-154">The **Download report** page is displayed and contains the following information about the report till be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="8e9b1-155">Количество скачиваемых элементов.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-155">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="8e9b1-156">Предполагаемый общий размер скачиваемых элементов.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-156">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="8e9b1-p111">Как индексируются, так и неиндексированные будет экспортироваться. Неиндексированные перечислены элементы, которые имеют распознанный формат, шифруются или не были индексированы по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p111">Whether indexed or unindexed will be exported. Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="8e9b1-159">Сведения о том, будут ли скачаны версии документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-159">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="8e9b1-p112">Состояние процесса экспорта отчета. Можно начать загрузку отчета даже в том случае, если Подготовка отчета не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p112">The status of the report export process. You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="8e9b1-p113">В разделе **экспортировать ключ**нажмите кнопку **Копировать в буфер обмена**. Чтобы загрузить отчет будет использовать этот ключ на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p113">Under **Export key**, click **Copy to clipboard**. You will use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="8e9b1-164">Поскольку всем пользователям можно установить и запустить средство экспорта обнаружения электронных данных и затем использовать этот ключ можно загрузить отчет о поиске, необходимо принять меры предосторожности, чтобы защитить этот ключ, так же, как бы защиты паролей и другие сведения, связанные с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-164">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="8e9b1-165">Нажмите кнопку **загрузить отчет**.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-165">Click **Download report**.</span></span>
    
4. <span data-ttu-id="8e9b1-166">Если вам будет предложено установить **eDiscovery MicrosoftOffice 365 средство экспорта**, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-166">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="8e9b1-167">В **средстве экспорта службы обнаружения электронных данных** в соответствующее поле вставьте ключ экспорта, который вы скопировали в действии 2. </span><span class="sxs-lookup"><span data-stu-id="8e9b1-167">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="8e9b1-168">Нажмите кнопку **Обзор** , чтобы указать расположение, где нужно загрузить отчет.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-168">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="8e9b1-169">Нажмите кнопку **Запустить**, чтобы скачать результаты поиска на свой компьютер.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-169">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="8e9b1-p114">**Обнаружение электронных данных средство экспорта** сведения о состоянии процесса экспорта, включая оценку числа (и размера) оставшихся элементов веб-сайта. После завершения экспорта имели доступ к файлам в месте, где они были загружены.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p114">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8e9b1-p115">Вы можете загрузить отчет для поиска контента, связанной с вариантом eDiscovery. Для этого перейдите к **поиска &amp; расследования** \> выберите дела **обнаружения электронных данных**и нажмите кнопку **Изменить** ![значок Правка](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). На странице " **Экспорт** " выберите Экспорт отчета и нажмите кнопку **загрузить отчет** в области сведений.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p115">You can download the report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="8e9b1-175">Что входит в отчете</span><span class="sxs-lookup"><span data-stu-id="8e9b1-175">What's included in the report</span></span>

<span data-ttu-id="8e9b1-176">После создания и экспорта отчета о результатах поиска контента, загружаются следующие документы:</span><span class="sxs-lookup"><span data-stu-id="8e9b1-176">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="8e9b1-p116">**Экспорт сводки** - документ Microsoft Excel, который содержит сводку экспорта. Это включает данные, например число источников контента, поиска, количество результатов поиска из каждого расположение содержимого, предполагаемое количество элементов, фактическое число элементов, которые будут экспортироваться и фактические размер элементов который будет экспортироваться.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p116">**Export Summary** - An Excel document that contains a summary of the export. This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8e9b1-p117">При включении неиндексированные элементов при экспорте отчета, число элементов неиндексированные включены в общее число оценке результатов поиска и в общее число результатов поиска загруженного (если требуется экспортировать результаты поиска), которые перечислены в Экспорт сводного отчета. Другими словами общее число элементов, которые будут загружены равно общее число примерный результатов и общее число неиндексированные элементов.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p117">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report. In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="8e9b1-181">**Манифест** - файл манифеста (в формате XML), который содержит сведения о каждом элементе, включенные в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-181">**Manifest** - A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="8e9b1-p118">**Результаты** - документ Microsoft Excel, строка, содержащая сведения о каждом индексированному элементу, который будет экспортироваться с результатами поиска. Для электронной почты, журнал результатов содержит сведения о каждом сообщении, включая:</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p118">**Results** - An Excel document that contains a row with information about each indexed item that would be exported with the search results. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="8e9b1-184">Расположение сообщения в исходном почтовом ящике (включая сведения о том, в каком почтовом ящике находится сообщение, в основном или в архивном).</span><span class="sxs-lookup"><span data-stu-id="8e9b1-184">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="8e9b1-185">Дата отправки или получения сообщения.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-185">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="8e9b1-186">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-186">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="8e9b1-187">Отправитель и получатели сообщения.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-187">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="8e9b1-188">Для документов из SharePoint и OneDrive для бизнеса сайтов журнал результатов содержит сведения о каждого документа, включая:</span><span class="sxs-lookup"><span data-stu-id="8e9b1-188">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="8e9b1-189">URL-адрес документа.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-189">The URL for the document.</span></span>
    
  - <span data-ttu-id="8e9b1-190">URL-адрес семейства веб-сайтов, в котором расположен документ.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-190">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="8e9b1-191">Дата последнего изменения документа.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-191">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="8e9b1-192">Имя документа (которое указано в столбце "Тема" журнала результатов).</span><span class="sxs-lookup"><span data-stu-id="8e9b1-192">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8e9b1-193">Количество строк в отчете о **результатах** должны быть равно общее количество результатов поиска, которые будут загружены за вычетом общее число элементов, перечисленных в отчете **Неиндексированные элементов** .</span><span class="sxs-lookup"><span data-stu-id="8e9b1-193">The number of rows in the **Results** report should be equal to the total number of search results that would be downloaded minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="8e9b1-p119">**Неиндексированных элементов** - документ Microsoft Excel, который содержит сведения о все неиндексированные элементы, которые должны быть включены в результатах поиска. Если не включить неиндексированные элементов при создании отчета результаты поиска, в этом отчете будет загружен, но будет пустым.</span><span class="sxs-lookup"><span data-stu-id="8e9b1-p119">**Unindexed Items** - An Excel document that contains information about any unindexed items that would be included in the search results. If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
