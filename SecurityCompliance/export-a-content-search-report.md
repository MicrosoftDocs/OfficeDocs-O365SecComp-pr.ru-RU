---
title: Экспорт отчета о поиске контента
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Вместо того чтобы экспортировать фактические результаты поиска контента в центре безопасности &amp; и соответствия требованиям Office 365, можно просто экспортировать отчет о результатах поиска. Отчет содержит сводку результатов поиска и документ с подробными сведениями о каждом экспортируемом элементе.
ms.openlocfilehash: d98f70d4f38f524de8751aecb197d0f85ee7f088
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295982"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="711d4-104">Экспорт отчета о поиске контента</span><span class="sxs-lookup"><span data-stu-id="711d4-104">Export a Content Search report</span></span>

<span data-ttu-id="711d4-105">Вместо того чтобы экспортировать полный набор результатов поиска из поиска контента в центре безопасности &amp; и соответствия требованиям Office 365 (и из поиска контента, связанного с вариантом обнаружения электронных данных), можно просто экспортировать те же отчеты, которые создаются при Экспорт результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="711d4-105">Instead of exporting the full set of search results from a Content Search in the Office 365 Security &amp; Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can just export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="711d4-p102">При экспорте отчета он загружается в папку с таким же именем, что и для поиска контента, но добавляется с помощью *_репортсонли* . Например, если поиск контента имеет имя *ContosoCase0815* , то отчет загружается в папку с именем *ContosoCase0815_ReportsOnly* . Список документов, включенных в отчет, приведен в разделе сведения, [включенные в отчет](#whats-included-in-the-report).</span><span class="sxs-lookup"><span data-stu-id="711d4-p102">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with  *_ReportsOnly*  . For example, if the Content Search is named  *ContosoCase0815*  , then the report is downloaded to a folder named  *ContosoCase0815_ReportsOnly*  . For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="711d4-109">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="711d4-109">Before you begin</span></span>

- <span data-ttu-id="711d4-p103">Для экспорта отчета по поиску контента необходимо назначить роль управления поиском соответствия требованиям в центре безопасности &amp; и соответствия требованиям Office 365. Эта роль назначена встроенному Диспетчеру обнаружения электронных данных и группам ролей управления Организацией. По умолчанию она не назначается группе ролей Управление организацией. Дополнительные сведения см в разделе [Назначение разрешений обнаружения электронных данных в центре безопасности &amp; Office 365](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="711d4-p103">To export a Content Search report, you have to be assigned the Compliance Search management role in the Office 365 Security &amp; Compliance Center. This role is assigned to the built-in eDiscovery Manager and Organization Management role groups. It isn't assigned by default to the Organization Management role group. For more information, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="711d4-p104">При экспорте отчета данные временно хранятся в уникальной области хранения Windows Azure в облаке Майкрософт, прежде чем она будет загружена на локальный компьютер. убедитесь, что ваша организация может подключаться к конечной точке в Azure, т \*\* \*. е. blob.core.windows.net\*\* (подстановочный знак представляет уникальный идентификатор для экспорта). Данные результатов поиска удаляются из области хранилища Azure две недели после ее создания.</span><span class="sxs-lookup"><span data-stu-id="711d4-p104">When you export a report, the data is temporarily stored in a unique Windows Azure storage area in the Microsoft cloud before it's downloaded to your local computer. Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export). The search results data is deleted from the Azure storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="711d4-117">Компьютер, который вы используете для экспорта результатов поиска, должен соответствовать указанным ниже требованиям к системе.</span><span class="sxs-lookup"><span data-stu-id="711d4-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="711d4-118">32- или 64-разрядный выпуск Windows 7 и более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="711d4-118">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="711d4-119">Microsoft .NET Framework 4,7</span><span class="sxs-lookup"><span data-stu-id="711d4-119">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="711d4-120">Поддерживаемый браузер:</span><span class="sxs-lookup"><span data-stu-id="711d4-120">A supported browser:</span></span>
    
    - <span data-ttu-id="711d4-121">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="711d4-121">Microsoft Edge</span></span>
    
      <span data-ttu-id="711d4-122">или</span><span class="sxs-lookup"><span data-stu-id="711d4-122">or</span></span>
    
    - <span data-ttu-id="711d4-123">Microsoft Internet Explorer 10 и более поздние версии</span><span class="sxs-lookup"><span data-stu-id="711d4-123">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="711d4-p105">**Примечание:** Корпорация Майкрософт не производит сторонние расширения или надстройки для приложений ClickOnce. Экспорт результатов поиска с использованием неподдерживаемого браузера со сторонними расширениями или надстройками не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="711d4-p105">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 

- <span data-ttu-id="711d4-p106">Если предполагаемый общий размер результатов, возвращаемых службой поиска контента, превышает 20&nbsp;ТБ, экспорт отчета завершается с ошибками. Чтобы успешно экспортировать отчет, попытайтесь сузить область и повторно запустите поиск, чтобы предполагаемый размер результатов не превышал 20&nbsp;ТБ.</span><span class="sxs-lookup"><span data-stu-id="711d4-p106">If the estimated total size of the results returned by a Content Search exceeds 20&nbsp;TB, exporting the report will fail. To successfully export the report, try to narrow the scope and re-run the search so the estimated size of the results is less than 20&nbsp;TB.</span></span>

- <span data-ttu-id="711d4-p107">При экспорте отчетов поиска контента учитываются максимальное число одновременно выполняемых операций экспорта и максимальное количество экспортируемых элементов, которое может выполнить один пользователь. Более подробную информацию об ограничениях экспорта можно узнать в статье [Экспорт результатов поиска содержимого из центра безопасности Office 365 Security _амп_ в центре соответствия требованиям](export-search-results.md#export-limits).</span><span class="sxs-lookup"><span data-stu-id="711d4-p107">Exporting Content Search reports counts against the maximum number of exports running at the same time and the maximum number of exports that a single user can run. For more information about export limits, see [Export Content Search results from the Office 365 Security & Compliance Center](export-search-results.md#export-limits).</span></span>

## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="711d4-130">Создание и скачивание отчета о поиске контента</span><span class="sxs-lookup"><span data-stu-id="711d4-130">Generate and download a Content Search report</span></span>

<span data-ttu-id="711d4-131">Действия по созданию и загрузке отчета о поиске контента очень похожи на фактическое Экспортирование результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="711d4-131">The steps to generate and download a Content Search report are very similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="711d4-132">Шаг 1: создание отчета для экспорта</span><span class="sxs-lookup"><span data-stu-id="711d4-132">Step 1: Generate the report for export</span></span>

<span data-ttu-id="711d4-p108">Первым этапом является подготовка отчета для загрузки на компьютер экспорта. При отправке отчета документы отчетов отправляются в область хранилища Azure в облаке Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="711d4-p108">The first step is to prepare the report for downloading to your computer exporting. When you the report, the report documents are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="711d4-135">Перейдите по ссылке [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="711d4-135">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="711d4-136">Войдите в Office 365 с помощью своей рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="711d4-136">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="711d4-137">В расположенной слева области Центра безопасности и соответствия требованиям щелкните **Поиск и исследования** \> **Поиск контента**.</span><span class="sxs-lookup"><span data-stu-id="711d4-137">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="711d4-138">На странице **Поиск контента** выберите Поиск.</span><span class="sxs-lookup"><span data-stu-id="711d4-138">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="711d4-139">В области сведений в разделе **Экспорт отчета на компьютер**нажмите **создать отчет**.</span><span class="sxs-lookup"><span data-stu-id="711d4-139">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="711d4-p109">Если результаты поиска старше 7 дней, вам будет предложено обновить результаты поиска. В этом случае отмените экспорт, щелкните **Обновить результаты поиска** в области сведений для выбранного поиска, а затем снова запустите экспорт отчета после обновления результатов.</span><span class="sxs-lookup"><span data-stu-id="711d4-p109">If the results for a search are older than 7 days, you are prompted to update the search results. If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="711d4-142">На странице " **Экспорт отчета** " в разделе **включить эти элементы из поиска**выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="711d4-142">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="711d4-143">Экспортировать только индексированные элементы.</span><span class="sxs-lookup"><span data-stu-id="711d4-143">Export only indexed items</span></span>
    
    - <span data-ttu-id="711d4-144">Экспортировать индексированные и неиндексированные элементы.</span><span class="sxs-lookup"><span data-stu-id="711d4-144">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="711d4-145">Экспортировать только неиндексированные элементы.</span><span class="sxs-lookup"><span data-stu-id="711d4-145">Export only unindexed items</span></span>
    
    <span data-ttu-id="711d4-146">Для получения дополнительных сведений об неиндексированных элементах просмотрите раздел " [частично индексированные элементы" в поиске контента](partially-indexed-items-in-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="711d4-146">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="711d4-p110">Выберите, чтобы включить статистику поиска для всех версий документов SharePoint. Этот параметр отображается только в том случае, если источники контента поиска содержат сайты SharePoint или OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="711d4-p110">Choose to include search statistics for all versions of SharePoint documents. This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="711d4-149">Нажмите **создать отчет**.</span><span class="sxs-lookup"><span data-stu-id="711d4-149">Click **Generate report**.</span></span>
    
    <span data-ttu-id="711d4-p111">Отчет по результатам поиска готов к скачиванию, что означает, что документы отчета будут отправлены в область хранилища Azure в Microsoft Cloud. Когда отчет будет готов к скачиванию, ссылка **загрузить отчет** будет отображаться в разделе **Экспорт отчета на компьютер** в области сведений.</span><span class="sxs-lookup"><span data-stu-id="711d4-p111">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure storage area in the Microsoft cloud. When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="711d4-p112">Вы также можете экспортировать отчет для поиска контента, связанного с вариантом обнаружения электронных данных. Для этого перейдите к разделу \*\*Поиск &amp; \*\* \> **обнаружения электронных**данных, выберите обращение и щелкните **изменить** ![значок](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)редактирования. На странице **поиски** выберите Поиск, а затем нажмите кнопку **Экспорт** ![экспорта](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> результатов поиска **Экспорт отчета**.</span><span class="sxs-lookup"><span data-stu-id="711d4-p112">You can also export a report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Searches** page, select a search, and then click **Export** ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="711d4-155">Шаг 2: Скачайте отчет</span><span class="sxs-lookup"><span data-stu-id="711d4-155">Step 2: Download the report</span></span>

<span data-ttu-id="711d4-156">Следующий шаг — скачать отчет из области хранилища Azure на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="711d4-156">The next step is to download the report from the Azure storage area to your local computer.</span></span>
  
1. <span data-ttu-id="711d4-157">В области сведений для поиска, для которого был создан отчет, в разделе **Экспорт отчета на компьютер**нажмите кнопку **скачать отчет**.</span><span class="sxs-lookup"><span data-stu-id="711d4-157">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="711d4-158">Откроется страница " **Загрузка отчета** " со следующими сведениями о отчете, который был загружен на компьютер.</span><span class="sxs-lookup"><span data-stu-id="711d4-158">The **Download report** page is displayed and contains the following information about the report till be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="711d4-159">Количество скачиваемых элементов.</span><span class="sxs-lookup"><span data-stu-id="711d4-159">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="711d4-160">Предполагаемый общий размер скачиваемых элементов.</span><span class="sxs-lookup"><span data-stu-id="711d4-160">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="711d4-p113">Указывает, будет ли экспортироваться индексированный или неиндексированный. Неиндексированные элементы — это элементы, которые имеют распознаваемый формат, шифруются или не индексируются по другим причинам.</span><span class="sxs-lookup"><span data-stu-id="711d4-p113">Whether indexed or unindexed will be exported. Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="711d4-163">Сведения о том, будут ли скачаны версии документов SharePoint.</span><span class="sxs-lookup"><span data-stu-id="711d4-163">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="711d4-p114">Состояние процесса экспорта отчета. Вы можете начать загрузку отчета, даже если подготовка отчета не завершена.</span><span class="sxs-lookup"><span data-stu-id="711d4-p114">The status of the report export process. You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="711d4-p115">В разделе **Экспорт ключа**нажмите кнопку **Копировать в буфер обмена**. Этот ключ будет использоваться на шаге 5, чтобы скачать отчет.</span><span class="sxs-lookup"><span data-stu-id="711d4-p115">Under **Export key**, click **Copy to clipboard**. You will use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="711d4-168">Так как любой пользователь может установить и запустить средство экспорта обнаружения электронных данных, а затем использовать этот ключ для загрузки отчета о поиске, обязательно примите меры предосторожности, чтобы защитить этот ключ так же, как и при защите паролей или других данных, связанных с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="711d4-168">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="711d4-169">Нажмите кнопку **загрузить отчет**.</span><span class="sxs-lookup"><span data-stu-id="711d4-169">Click **Download report**.</span></span>
    
4. <span data-ttu-id="711d4-170">Если вам будет предложено установить **средство экспорта майкрософтoffice 365 для обнаружения электронных**данных, нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="711d4-170">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="711d4-171">В **средстве экспорта службы обнаружения электронных данных** в соответствующее поле вставьте ключ экспорта, который вы скопировали в действии 2. </span><span class="sxs-lookup"><span data-stu-id="711d4-171">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="711d4-172">Нажмите кнопку **Обзор** , чтобы указать папку, в которую вы хотите скачать отчет.</span><span class="sxs-lookup"><span data-stu-id="711d4-172">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="711d4-173">Нажмите кнопку **Запустить**, чтобы скачать результаты поиска на свой компьютер.</span><span class="sxs-lookup"><span data-stu-id="711d4-173">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="711d4-p116">**Средство экспорта eDiscovery** отображает сведения о состоянии процесса экспорта, в том числе оценку числа и размера остальных загружаемых элементов. По завершении процесса экспорта можно получить доступ к файлам в том расположении, в котором они были скачаны.</span><span class="sxs-lookup"><span data-stu-id="711d4-p116">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="711d4-p117">Вы можете скачать отчет для поиска контента, связанного с вариантом обнаружения электронных данных. Для этого перейдите к разделу \*\*Поиск &amp; \*\* \> **обнаружения электронных**данных, выберите обращение и щелкните **изменить** ![значок](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)редактирования. На странице " **Экспорт** " выберите Экспорт отчета, а затем нажмите кнопку **скачать отчет** в области сведений.</span><span class="sxs-lookup"><span data-stu-id="711d4-p117">You can download the report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="711d4-179">Что входит в отчет</span><span class="sxs-lookup"><span data-stu-id="711d4-179">What's included in the report</span></span>

<span data-ttu-id="711d4-180">При создании и экспорте отчета о результатах поиска контента загружаются следующие документы:</span><span class="sxs-lookup"><span data-stu-id="711d4-180">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="711d4-p118">**Сводка по экспорту** — документ Excel, который содержит сводку по экспорту. Сюда входят такие сведения, как количество искомых источников контента, количество результатов поиска из каждого расположения контента, предполагаемое количество элементов, фактическое количество элементов, которые будут экспортированы, а также предполагаемый и фактический размер элементов. экспортируемый.</span><span class="sxs-lookup"><span data-stu-id="711d4-p118">**Export Summary** - An Excel document that contains a summary of the export. This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="711d4-p119">Если вы включили неиндексированные элементы при экспорте отчета, число неиндексированных элементов будет включено в общее число оценочных результатов поиска и в общее число загруженных результатов поиска (если вы намерены экспортировать результаты поиска), перечисленные в разделе Сводный отчет по экспорту. Другими словами, общее количество загружаемых элементов равно общему количеству предполагаемых результатов и общему количеству неиндексированных элементов.</span><span class="sxs-lookup"><span data-stu-id="711d4-p119">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report. In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="711d4-185">**Manifest** — файл манифеста (в формате XML), который содержит сведения о каждом элементе, включенном в результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="711d4-185">**Manifest** - A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="711d4-p120">**Results** — документ Excel, содержащий строку со сведениями о каждом индексируемом элементе, который будет экспортирован в результаты поиска. Для электронной почты журнал результатов содержит сведения о каждом сообщении, в том числе:</span><span class="sxs-lookup"><span data-stu-id="711d4-p120">**Results** - An Excel document that contains a row with information about each indexed item that would be exported with the search results. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="711d4-188">Расположение сообщения в исходном почтовом ящике (включая сведения о том, в каком почтовом ящике находится сообщение, в основном или в архивном).</span><span class="sxs-lookup"><span data-stu-id="711d4-188">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="711d4-189">Дата отправки или получения сообщения.</span><span class="sxs-lookup"><span data-stu-id="711d4-189">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="711d4-190">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="711d4-190">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="711d4-191">Отправитель и получатели сообщения.</span><span class="sxs-lookup"><span data-stu-id="711d4-191">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="711d4-192">Для документов из сайтов SharePoint и OneDrive для бизнеса журнал результатов содержит сведения о каждом документе, в том числе:</span><span class="sxs-lookup"><span data-stu-id="711d4-192">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="711d4-193">URL-адрес документа.</span><span class="sxs-lookup"><span data-stu-id="711d4-193">The URL for the document.</span></span>
    
  - <span data-ttu-id="711d4-194">URL-адрес семейства веб-сайтов, в котором расположен документ.</span><span class="sxs-lookup"><span data-stu-id="711d4-194">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="711d4-195">Дата последнего изменения документа.</span><span class="sxs-lookup"><span data-stu-id="711d4-195">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="711d4-196">Имя документа (которое указано в столбце "Тема" журнала результатов).</span><span class="sxs-lookup"><span data-stu-id="711d4-196">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="711d4-197">Количество строк в отчете о **результатах** должно равняться общему количеству загружаемых результатов поиска за вычетом общего числа элементов, указанных в отчете неиндексированные **элементы** .</span><span class="sxs-lookup"><span data-stu-id="711d4-197">The number of rows in the **Results** report should be equal to the total number of search results that would be downloaded minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="711d4-p121">**НеиндексированНые элементы** — документ Excel, содержащий сведения обо всех неиндексированных элементах, которые будут включены в результаты поиска. Если вы не включаете неиндексированные элементы при создании отчета по результатам поиска, этот отчет по-прежнему будет скачан, но будет пустым.</span><span class="sxs-lookup"><span data-stu-id="711d4-p121">**Unindexed Items** - An Excel document that contains information about any unindexed items that would be included in the search results. If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
