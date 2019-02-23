---
title: Экспорт результатов в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Узнайте, как определить параметры экспорта результатов из Office 365 Advanced eDiscovery, включая процедуру указания параметров для пакета экспорта. '
ms.openlocfilehash: 02314b0848d8e7bb37a7cb96fa4a721cf2622712
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218099"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="7eeed-103">Экспорт результатов в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7eeed-103">Export results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="7eeed-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="7eeed-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="7eeed-106">В этом разделе описываются расширенные параметры настройки экспорта eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7eeed-106">This topic describes the Advanced eDiscovery Export Setup options.</span></span>
  
 <span data-ttu-id="7eeed-107">**В этом разделе:**</span><span class="sxs-lookup"><span data-stu-id="7eeed-107">**In this topic:**</span></span>
  
- [<span data-ttu-id="7eeed-108">Определение пакетов и сеансов экспорта</span><span class="sxs-lookup"><span data-stu-id="7eeed-108">Defining export batches and sessions</span></span>](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [<span data-ttu-id="7eeed-109">Добавочные и дополнительные операции экспорта</span><span class="sxs-lookup"><span data-stu-id="7eeed-109">Incremental and additional exports</span></span>](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [<span data-ttu-id="7eeed-110">Настройка параметров пакетного экспорта</span><span class="sxs-lookup"><span data-stu-id="7eeed-110">Set up batch export parameters</span></span>](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [<span data-ttu-id="7eeed-111">Экспорт выходных файлов отчета</span><span class="sxs-lookup"><span data-stu-id="7eeed-111">Export report output files</span></span>](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a><span data-ttu-id="7eeed-112">Определение пакетов и сеансов экспорта</span><span class="sxs-lookup"><span data-stu-id="7eeed-112">Defining export batches and sessions</span></span>
<span data-ttu-id="7eeed-113"><a name="BK_Define"> </a></span><span class="sxs-lookup"><span data-stu-id="7eeed-113"></span></span>

<span data-ttu-id="7eeed-p102">Пакет экспорта обеспечивает обработку экспорта с помощью набора определенных параметров. Расширенное обнаружение электронных данных позволяет определять пакеты для настройки каждого экспорта.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p102">An export batch allows export processing using a set of defined parameters. Advanced eDiscovery enables you to define batches to customize each export.</span></span>
  
<span data-ttu-id="7eeed-p103">Параметры определяются для пакета экспорта. Пакет с именем "Export Batch 01" создается по умолчанию для первого пакета дела. Вы также можете изменить имя и описание пакета.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p103">Parameters are defined per export batch. A batch named "Export batch 01" is created by default for the first batch of a case. You can also edit the batch name and description.</span></span>
  
<span data-ttu-id="7eeed-119">Сеанс экспорта — это выполнение расширенного экспорта eDiscovery в пакете экспорта.</span><span class="sxs-lookup"><span data-stu-id="7eeed-119">An export session is an execution of Advanced eDiscovery Export within an export batch.</span></span>
  
## <a name="incremental-and-additional-exports"></a><span data-ttu-id="7eeed-120">Добавочные и дополнительные операции экспорта</span><span class="sxs-lookup"><span data-stu-id="7eeed-120">Incremental and additional exports</span></span>
<span data-ttu-id="7eeed-121"><a name="BK_IncrementalReports"> </a></span><span class="sxs-lookup"><span data-stu-id="7eeed-121"></span></span>

<span data-ttu-id="7eeed-p104">Можно выполнить несколько сеансов экспорта в пакете экспорта, чтобы обеспечить согласованность результатов на основе одного и того же шаблона и параметров экспорта. Для каждого сеанса в пакете можно экспортировать аналитику для новых обработанных данных и обрабатывать каждый из них последовательно.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p104">You can run multiple export sessions within an export batch, to ensure consistent results based on the same export template and parameters. For each session within a batch, you can export analytics for newly processed case data and process each "incrementally."</span></span>
  
<span data-ttu-id="7eeed-p105">Для экспорта с использованием другого набора параметров сначала необходимо создать новый пакет. Первый сеанс в новом пакете приводит к получению результатов для файлов, обработанных в случае, независимо от того, были ли эти файлы импортированы и обработаны по одному или нескольким импортам. Каждый пакет пересчитывает сводки, подобия, инклюзивные и т. д. Сеансы используют параметры, определенные для пакета, и не пересчитываются сводные данные, подобия, инклюзивные и т. д. для каждого выполнения сеанса.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p105">In order to export using a different set of parameters, you first need to create a new batch. The first session in the new batch will produce results for files processed in the case so far, whether or not these files were imported and processed over one or multiple Imports. Each batch recalculates pivots, similarity, inclusives, etc. Sessions use the parameters defined for the batch and do not recalculate pivots, similarity, inclusives, etc. for each session execution.</span></span>
  
<span data-ttu-id="7eeed-p106">Например, предположим, что было импортировано обращение и проанализировано его данные. Чтобы получить результаты последовательного и поЧтовых сообщений для добавочных данных, щелкните **создать сеанс экспорта** в том же пакете, который использовался ранее для экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p106">For example, assume a case was imported and its data analyzed. In order to retrieve Near-duplicates and Email Threading results for the incremental data, click **Create export session** in the same batch that was previously used to export data.</span></span> 
  
## <a name="set-up-batch-export-parameters"></a><span data-ttu-id="7eeed-129">Настройка параметров пакетного экспорта</span><span class="sxs-lookup"><span data-stu-id="7eeed-129">Set up batch export parameters</span></span>
<span data-ttu-id="7eeed-130"><a name="BK_SetUpExport"> </a></span><span class="sxs-lookup"><span data-stu-id="7eeed-130"></span></span>

<span data-ttu-id="7eeed-p107">Средство экспорта eDiscovery используется для экспорта результатов поиска с расширенного обнаружения электронных данных на локальный компьютер. Чтобы увеличить пропускную способность и скорость процесса экспорта, можно настроить параметр реестра Windows на компьютере, используемом для экспорта результатов поиска. Если вы хотите увеличить скорость загрузки, настройте параметры реестра перед настройкой параметров экспорта. Более подробную информацию можно узнать [в статье увеличение скорости скачивания при экспорте результатов поиска eDiscovery из Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span><span class="sxs-lookup"><span data-stu-id="7eeed-p107">The eDiscovery Export Tool is used to export search results from Advanced eDiscovery to your local computer. To increase the data transfer throughput and speed-up the export process, you can configure a Windows Registry setting on the computer that you use to export the search results. If you'd like to increase the download speed, configure the registry setting before you set up the export parameters. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
  
1. <span data-ttu-id="7eeed-135">В Advanced eDiscovery выберите обращение и нажмите кнопку **Экспорт** \> **настройки**.</span><span class="sxs-lookup"><span data-stu-id="7eeed-135">In Advanced eDiscovery, select a Case and click **Export** \> **Setup**.</span></span>
    
    - <span data-ttu-id="7eeed-136">В списке **Экспорт пакета** выберите имя пакета или результаты экспорта для экспорта пакет 01 (пакет по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7eeed-136">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
    - <span data-ttu-id="7eeed-p108">Чтобы экспортировать результаты для новых файлов, добавленных к существующему случаю, перейдите к текущему пакету. Чтобы создать сеанс в пакете, выберите один и тот же номер пакета и нажмите кнопку **создать сеанс экспорта** . Этот параметр позволяет экспортировать те же параметры, что и в предыдущем пакете, в добавочном режиме.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p108">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
    - <span data-ttu-id="7eeed-p109">Чтобы экспортировать в новый пакет, нажмите **Добавить** ![значок](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)добавить и введите новое имя в поле **имя раздела** (или оставьте значение по умолчанию) и описание в поле **Описание пакета**. Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p109">To export to a new batch, click **Add** ![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
    - <span data-ttu-id="7eeed-141">Чтобы изменить имя или описание раздела, выберите имя в **разделе Export Batch**, нажмите **изменить** ![значок](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)редактирования, а затем измените поля.</span><span class="sxs-lookup"><span data-stu-id="7eeed-141">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="7eeed-p110">После выполнения сеансов для пакета экспорта их невозможно удалить. Кроме того, после запуска первого сеанса можно изменить только некоторые параметры.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p110">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
    - <span data-ttu-id="7eeed-144">Чтобы создать дубликат пакета экспорта, выберите команду **дублировать экспортируемый пакет** ![создать дублирующийся значок](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) пакета экспорта и введите имя и описание для повторяющегося пакета в панели.</span><span class="sxs-lookup"><span data-stu-id="7eeed-144">To create a duplicate export batch, choose **Duplicate export batch** ![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
    - <span data-ttu-id="7eeed-145">Чтобы удалить пакет экспорта, нажмите кнопку **Удалить** ![, чтобы удалить значок](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)экспорта пакета.</span><span class="sxs-lookup"><span data-stu-id="7eeed-145">To delete an export batch, choose **Delete** ![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
    - <span data-ttu-id="7eeed-146">Чтобы просмотреть историю пакета, щелкните значок ![](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)истории просмотра **журнала пакетов** .</span><span class="sxs-lookup"><span data-stu-id="7eeed-146">To view the history of a batch, choose **Batch history** ![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="7eeed-147">В \*\*\*\* разделе Заполнение установите флажок **включать только те файлы** , которые были бы вышеуказанными вышеуказанными показателями и/или **уточненным пакетом экспорта** , если необходимо настроить параметры для пакета экспорта.</span><span class="sxs-lookup"><span data-stu-id="7eeed-147">Under **Population**, select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch.</span></span> 
    
3. <span data-ttu-id="7eeed-p111">Если выбран параметр **включить только файлы**, превышающие значение релевантности, то эта **Ошибка** включена. Если показатель релевантности файла выше, чем показатель вырезания для выбранного вопроса, файл будет экспортирован, если он не исключен фильтром "для проверки".</span><span class="sxs-lookup"><span data-stu-id="7eeed-p111">If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled. If the file's relevance score is higher than the cut-off score for the selected issue, the file will be exported unless it's excluded by the 'For review' filter.</span></span> 
  
    <span data-ttu-id="7eeed-p112">Если выбран параметр **реточная экспорт пакета**, переключатели переключателя **de – копия** и фильтр по полю "для проверки" включены. Если выбрано значение " **de-копия**", то дубликаты файлов будут отфильтровываться в соответствии с политикой, заданной по умолчанию [уровень дел (по умолчанию): из каждого набора дубликатов файлов во всем случае все файлы, кроме одного, будут передаваться в дупед. Уровень хранитель: из каждого набора повторяющихся файлов одного и того же хранитель, все файлы, кроме одного, будут находиться в дупед.] В выходных данных экспорта содержится запись всех повторяющихся файлов. Если выбрано поле **Filter by to Review** , выберите **изменить в разделе Метаданные** , чтобы ввести параметры поля **"для просмотра"** . Выберите **включить входные файлы** , чтобы включить исходные файлы в содержимое пакета. Этот параметр можно очистить, чтобы ускорить процесс экспорта. Обратите внимание на то, что собственные файлы будут экспортированы в любом случае.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p112">If you select **Refine export batch**, the **De-dupe** and Filter by 'For review' field radio buttons are enabled. If you choose **De-dupe**, then duplicate files will be filtered out according to the policy defined [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped.] The export output contains a record of all duplicate files. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files** to include source files in the package content. You can clear this setting to speed up the export process. Note that the Native files will be exported in any case.</span></span> 
    
4. <span data-ttu-id="7eeed-157">В разделе **метаданные**выберите один из следующих параметров в списке **Экспорт шаблона** (один раз для каждого сеанса).</span><span class="sxs-lookup"><span data-stu-id="7eeed-157">Under **Metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
    - <span data-ttu-id="7eeed-p113">**Стандартный**: базовый набор элементов данных, метаданных и свойств. Используйте этот параметр, если импорт данных уже был обработан во время расширенного обнаружения электронных данных, а экспорт данных отправлен в систему, которая уже содержит эти файлы. По умолчанию создаются и заполняются столбцы экспорта шаблонов.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p113">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
    - <span data-ttu-id="7eeed-p114">**ALL**: полный набор стандартных метаданных, включая все обрабатываемые данные, а также результаты анализа и релевантности. Этот шаблон необходим, когда Расширенное обнаружение электронных данных выполняет обработку и передачу данных файлов во внешнюю систему в первый раз.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p114">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
    - <span data-ttu-id="7eeed-163">**Проблемы**: выберите **все проблемы** или выберите созданную вами задачу.</span><span class="sxs-lookup"><span data-stu-id="7eeed-163">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
5. <span data-ttu-id="7eeed-164">В разделе **назначение**:</span><span class="sxs-lookup"><span data-stu-id="7eeed-164">Under **Destination**:</span></span>
    
    - <span data-ttu-id="7eeed-165">**Загрузка на локальный компьютер**</span><span class="sxs-lookup"><span data-stu-id="7eeed-165">**Download to local machine**</span></span>
    
    - <span data-ttu-id="7eeed-166">**Экспорт в определяемый пользователем BLOB-объект Azure**: Если этот флажок установлен, можно указать URL-адрес контейнера и маркер SAS.</span><span class="sxs-lookup"><span data-stu-id="7eeed-166">**Export to user-defined Azure blob**: If this is checked, you can specify a container URL and SAS token.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="7eeed-p115">После того как пакет экспорта будет сохранен в определенном пользователем большом двоичном объекте Azure, данные не будут больше управляться с помощью расширенного обнаружения электронных данных; Он управляется BLOB-объектом Azure. Это означает, что при удалении такого случая экспортированные файлы останутся в большом двоичном объекте Azure.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p115">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery; it's managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
    - <span data-ttu-id="7eeed-169">**Сохранить маркер SAS для следующего сеанса экспорта**: Если этот флажок установлен, маркер SAS будет зашифрован в дополнительной базе данных расширенного обнаружения электронных данных для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="7eeed-169">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="7eeed-p116">В настоящее время срок действия маркера SAS истечет через месяц. Если вы попытаетесь скачать его через несколько месяцев, необходимо отменить последний сеанс, а затем снова выполнить экспорт.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p116">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
6. <span data-ttu-id="7eeed-172">Нажмите кнопку **изменить** , чтобы задать параметры поля "для рецензирования".</span><span class="sxs-lookup"><span data-stu-id="7eeed-172">Click **Modify** to set the 'for review' field settings.</span></span> 
    
    ![Настройка параметров поля просмотра для пакета экспорта](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
   - <span data-ttu-id="7eeed-p117">В разделе " **Параметры поля просмотра**" в раскрывающемся списке **Выбор сценария** выберите сценарий и область проверки. Параметры отображаются на основе выбранных элементов.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p117">Under **For review field settings**, in **Select scenario** pull-down list, select the scenario and scope of the review. The settings are displayed based on your selection.</span></span>
    
      - <span data-ttu-id="7eeed-176">**Просмотр всех** (по умолчанию): все электронные письма, вложения и документы выбираются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7eeed-176">**Review all** (default): All emails, attachments, and documents are selected by default.</span></span> 
    
      - <span data-ttu-id="7eeed-177">**Просмотр всего уникального содержимого в наборе**: Инклюзивные и уникальные Инклюзивные копии, уникальные вложения в уровне электронной почты, характерные для каждого набора точных дубликатов.</span><span class="sxs-lookup"><span data-stu-id="7eeed-177">**Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.</span></span>
    
      - <span data-ttu-id="7eeed-178">**Просмотрите все уникальные данные в наборе — без инклюзивных копий**: включающие, уникальные вложения в уровне электронной почты, представитель из каждого набора точных дубликатов.</span><span class="sxs-lookup"><span data-stu-id="7eeed-178">**Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.</span></span>
    
      - <span data-ttu-id="7eeed-179">**Просмотрите все уникальные сведения и связанные с ними файлы семьи**: включительно, уникальные вложения в уровне электронной почты, представитель из каждого набора точных дубликатов, разместите файлы семьи.</span><span class="sxs-lookup"><span data-stu-id="7eeed-179">**Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.</span></span>
    
      - <span data-ttu-id="7eeed-p118">**НастраиваемАя Настройка** (позволяет определять параметры в диалоговом окне): значение по умолчанию — сохранить текущие параметры и включить все диалоговые параметры, чтобы разрешить выбор. Если выбран этот параметр, можно настроить параметры для сообщений электронной почты, документов, вложений и прочих.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p118">**Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. If you select this option, you can then customize the settings for emails, documents, attachments and miscellaneous.</span></span>
    
    - <span data-ttu-id="7eeed-182">В разделе **сообщения электронной почты**выберите сообщения электронной почты, которые требуется экспортировать.</span><span class="sxs-lookup"><span data-stu-id="7eeed-182">Under **Emails**, select the emails you want to export.</span></span>
    
      - <span data-ttu-id="7eeed-183">**Все сообщения электронной почты**: (по умолчанию) выбраны все сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7eeed-183">**All emails**: (default) All emails are selected.</span></span>
    
      - <span data-ttu-id="7eeed-184">**Включительно**: инклюзивная электронная почта — это последняя электронная почта потока, которая содержит все остальные сообщения из потока.</span><span class="sxs-lookup"><span data-stu-id="7eeed-184">**Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.</span></span>
    
      - <span data-ttu-id="7eeed-185">**Инклюзивные и уникальные Инклюзивные копии**: включающие копии и инклюзивные с теми же темой, основной текст и вложения; уникальные неисключительные копии — это уникальные копии этих сообщений.</span><span class="sxs-lookup"><span data-stu-id="7eeed-185">**Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .</span></span>
    
    - <span data-ttu-id="7eeed-186">В разделе **документы**выберите документы, которые требуется экспортировать.</span><span class="sxs-lookup"><span data-stu-id="7eeed-186">Under **Documents**, select the documents you want to export.</span></span> 
    
      - <span data-ttu-id="7eeed-187">**Все документы**: (по умолчанию) выбраны все документы.</span><span class="sxs-lookup"><span data-stu-id="7eeed-187">**All documents**: (default) All documents are selected.</span></span>
    
      - <span data-ttu-id="7eeed-188">**Сведение**: файл, выбранный в качестве представителя набора почти-дубликатов, который обычно используется в качестве базового при просмотре набора.</span><span class="sxs-lookup"><span data-stu-id="7eeed-188">**Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.</span></span>
    
      - <span data-ttu-id="7eeed-189">**Представитель из каждого набора точных копий**: уникальные почти-повторяющиеся файлы (включая сведение).</span><span class="sxs-lookup"><span data-stu-id="7eeed-189">**Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).</span></span>
    
    - <span data-ttu-id="7eeed-190">В разделе **вложения**выберите вложения, которые требуется экспортировать.</span><span class="sxs-lookup"><span data-stu-id="7eeed-190">Under **Attachments**, select the attachments you want to export.</span></span> 
    
      - <span data-ttu-id="7eeed-191">**Все вложения**: (по умолчанию) выбраны все вложения.</span><span class="sxs-lookup"><span data-stu-id="7eeed-191">**All attachments**: (default) All attachments are selected.</span></span>
    
      - <span data-ttu-id="7eeed-192">**Уникальное вложение на уровне вариантов**: уникальные файлы вложений в указанном случае.</span><span class="sxs-lookup"><span data-stu-id="7eeed-192">**Unique attachment in case level**: Unique attachment files within the specified case.</span></span>
    
      - <span data-ttu-id="7eeed-193">**Уникальное вложение в поле уровень почтового набора**: уникальные файлы вложений в заданном почтовом случае.</span><span class="sxs-lookup"><span data-stu-id="7eeed-193">**Unique attachment in email set level**: Unique attachment files within the specified email case.</span></span>
    
   - <span data-ttu-id="7eeed-p119">В разделе**мицелланеаус**можно **обрабатывать вложения как документы**, **обрабатывать сообщения электронной почты как документы**или разворачивать **для включения файлов семьи**. При выборе **расширения для включения файлов семьи**для каждого файла, помеченного для проверки, также будут помечаться все файлы того же семейства.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p119">Under**Micellaneous**, you can choose to **Treat attachments as documents**, **Treat emails as documents**, or **Expand to include family files**. When you choose **Expand to include family files**, for each file that is flagged for review, all files of the same family will also be flagged.</span></span>
    
7. <span data-ttu-id="7eeed-196">Нажмите кнопку **сохранить** , чтобы сохранить параметры.</span><span class="sxs-lookup"><span data-stu-id="7eeed-196">Choose **Save** to save the settings.</span></span> 
    
8. <span data-ttu-id="7eeed-197">Указав параметры экспорта, чтобы начать экспорт пакета, нажмите кнопку **создать сеанс экспорта**.</span><span class="sxs-lookup"><span data-stu-id="7eeed-197">After you specify export parameters, to start export batch, click **Create export session**.</span></span>
    
    <span data-ttu-id="7eeed-p120">Во время экспорта состояние отображается в поле **состояние задачи**. Результаты отображаются в **сводке по экспорту**.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p120">During export, the status is displayed in **Task status**. The results are displayed in **Export summary**.</span></span>
    
9. <span data-ttu-id="7eeed-200">В окне **скачать файлы** щелкните **Копировать в буфер обмена** , чтобы скопировать ключ экспорта.</span><span class="sxs-lookup"><span data-stu-id="7eeed-200">In the **Download files** window, click **Copy to clipboard** to copy the Export key.</span></span> 
    
    ![Загрузка файлов](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
10. <span data-ttu-id="7eeed-202">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="7eeed-202">Click **Close**.</span></span> 
    
    <span data-ttu-id="7eeed-203">Запускается средство экспорта eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7eeed-203">The eDiscovery Export Tool is started.</span></span>
    
    ![Средство экспорта обнаруженных электронных данных](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
11. <span data-ttu-id="7eeed-205">В **средстве экспорта обнаружения электронных**данных:</span><span class="sxs-lookup"><span data-stu-id="7eeed-205">In the **eDiscovery Export Tool**:</span></span>
    
    -  <span data-ttu-id="7eeed-206">При **вставке подписи общего доступа, которая будет использоваться для подключения**к источнику, вставьте ключ экспорта, который йоукопиед в буфер обмена, на шаге 7.</span><span class="sxs-lookup"><span data-stu-id="7eeed-206">In **Paste the Shared Access Signature that will be used to connect to the source**, paste the Export key that youcopied to the clipboard in step 7.</span></span>
    
    - <span data-ttu-id="7eeed-207">Нажмите кнопку **Обзор** , чтобы выбрать целевое расположение для хранения скачанных файлов экспорта на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7eeed-207">Click **Browse** to select the target location for storing the downloaded export files on the local machine.</span></span> 
    
    - <span data-ttu-id="7eeed-p121">Нажмите кнопку **Пуск**. Экспортируемые файлы загружаются на локальный компьютер. Если вы выбрали параметр **Экспорт в Пользовательский BLOB-объект Azure** на шаге 4, сеанс будет экспортирован в место назначения URL-адреса хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p121">Click **Start**.The export files are downloaded to the local machine. If you chose **Export to user-defined Azure blob** in step 4, the session is exported to a Blob storage URL destination of your choosing.</span></span>
    
<span data-ttu-id="7eeed-210">Полное описание полей в отчете экспорта приведено в разделе [экспорт полей отчета](export-report-fields-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="7eeed-210">For a full description of the fields in the export report, see [Export report fields](export-report-fields-in-advanced-ediscovery.md).</span></span>
  
## <a name="export-report-output-files"></a><span data-ttu-id="7eeed-211">Экспорт выходных файлов отчета</span><span class="sxs-lookup"><span data-stu-id="7eeed-211">Export report output files</span></span>
<span data-ttu-id="7eeed-212"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="7eeed-212"></span></span>

<span data-ttu-id="7eeed-213">В следующей таблице перечислены выходные файлы, создаваемые при запуске пакета экспорта.</span><span class="sxs-lookup"><span data-stu-id="7eeed-213">The following table lists the output files that are generated when you run an Export batch.</span></span>
  
|<span data-ttu-id="7eeed-214">**Имя файла**</span><span class="sxs-lookup"><span data-stu-id="7eeed-214">**File name**</span></span>|<span data-ttu-id="7eeed-215">**Тип файла**</span><span class="sxs-lookup"><span data-stu-id="7eeed-215">**File type**</span></span>|<span data-ttu-id="7eeed-216">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7eeed-216">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7eeed-217">Сводка по экспорту</span><span class="sxs-lookup"><span data-stu-id="7eeed-217">Export summary</span></span>  <br/> |<span data-ttu-id="7eeed-218">расширения</span><span class="sxs-lookup"><span data-stu-id="7eeed-218">csv</span></span>  <br/> |<span data-ttu-id="7eeed-219">Файл журнала, созданный средством экспорта eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7eeed-219">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="7eeed-220">Трассировки</span><span class="sxs-lookup"><span data-stu-id="7eeed-220">Trace</span></span>  <br/> |<span data-ttu-id="7eeed-221">TXT</span><span class="sxs-lookup"><span data-stu-id="7eeed-221">txt</span></span>  <br/> |<span data-ttu-id="7eeed-222">Файл журнала, созданный средством экспорта eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="7eeed-222">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="7eeed-223">Извлеченные текстовые файлы</span><span class="sxs-lookup"><span data-stu-id="7eeed-223">Extracted text files</span></span>  <br/> |<span data-ttu-id="7eeed-224">Папка "файл"</span><span class="sxs-lookup"><span data-stu-id="7eeed-224">File folder</span></span>  <br/> |<span data-ttu-id="7eeed-225">Папка, содержащая извлеченные текстовые файлы для экспортированных файлов.</span><span class="sxs-lookup"><span data-stu-id="7eeed-225">Folder that contains the extracted text files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="7eeed-226">Входные или собственные файлы</span><span class="sxs-lookup"><span data-stu-id="7eeed-226">Input or native files</span></span>  <br/> |<span data-ttu-id="7eeed-227">Папка "файл"</span><span class="sxs-lookup"><span data-stu-id="7eeed-227">File folder</span></span>  <br/> |<span data-ttu-id="7eeed-228">Папка, содержащая собственные и входные файлы экспортированных файлов.</span><span class="sxs-lookup"><span data-stu-id="7eeed-228">Folder that contains the native and input files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="7eeed-229">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="7eeed-229">Export list</span></span>  <br/> |<span data-ttu-id="7eeed-230">XLSX</span><span class="sxs-lookup"><span data-stu-id="7eeed-230">xlsx</span></span>  <br/> |<span data-ttu-id="7eeed-p122">Метаданные экспортированных файлов в формате xlsx. Поля в файлах в соответствии с шаблоном пользователь выбирает для экспорта. При необходимости создаются несколько файлов, каждая из которых содержит 100 150K строк. Если определенное значение содержит больше символов, чем может содержать ячейка Excel (в настоящее время это ограничение составляет 32 767 символов), то значение будет обрезано до максимально допустимой длины. Если значение обрезается, цвет фона ячейки будет красным для обозначения пользователя. " "Участники электронной почты" — это пример поля, длина которого может превышать лимит, если сообщение было отправлено в большое распределение. В разделе [Export Report](export-report-fields-in-advanced-ediscovery.md) содержатся сведения о выходных полях.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p122">Exported files metadata in xlsx format. Fields in files are according to template user selects to export. If needed, several files are created, each contains 100-150K rows. If a certain value contains more characters than an Excel cell can contain (currently the limit is 32,767 characters), then the value will be trimmed to the maximum length allowed. If a value is trimmed, the cell's background color is red to indicate this to the user."Email participants" is an example of a field that can exceed the length limit, if the email was sent to a large distribution. See [Export report fields](export-report-fields-in-advanced-ediscovery.md) for details about the output fields.  </span></span><br/> |
|<span data-ttu-id="7eeed-237">Загрузка файла</span><span class="sxs-lookup"><span data-stu-id="7eeed-237">Load file</span></span>  <br/> |<span data-ttu-id="7eeed-238">расширения</span><span class="sxs-lookup"><span data-stu-id="7eeed-238">csv</span></span>  <br/> |<span data-ttu-id="7eeed-p123">Метаданные экспортированных файлов в формате CSV для загрузки в другое приложение. Поля в файлах в соответствии с шаблоном пользователь выбирает для экспорта.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p123">Exported files metadata in csv format for loading into a different application. Fields in files are according to template user selects to export.</span></span>  <br/> |
|<span data-ttu-id="7eeed-241">Индикатор успеха</span><span class="sxs-lookup"><span data-stu-id="7eeed-241">Success indicator</span></span>  <br/> |<span data-ttu-id="7eeed-242">TXT</span><span class="sxs-lookup"><span data-stu-id="7eeed-242">txt</span></span>  <br/> |<span data-ttu-id="7eeed-p124">Создается только при экспорте в BLOB-объект стороннего производителя Azure. Если экспорт полностью выполнен успешно, файл будет создан. В случае сбоя или частичного успеха файл не будет создан. Файл будет создан в корневой папке, что позволит автоматически отслеживать различные состояния пакетов и сеансов экспорта. Это пустой файл. Его имя: Тенантид_касеид_екстерналкасеид_касенаме_експортбатчид_сессионид_датетиме. txt.</span><span class="sxs-lookup"><span data-stu-id="7eeed-p124">Only created when exporting to a 3rd party Azure blob. If export succeed completely, the file will be created. In case of failure, or partial success the file will not be created. File will be created in the root folder, allowing automated tracking on different Export batches/sessions statuses. This is an empty file. Its name is: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7eeed-249">См. также</span><span class="sxs-lookup"><span data-stu-id="7eeed-249">See also</span></span>

[<span data-ttu-id="7eeed-250">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7eeed-250">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="7eeed-251">Просмотр журнала пакетной обработки и экспорт прошлых результатов</span><span class="sxs-lookup"><span data-stu-id="7eeed-251">Viewing batch history and exporting past results</span></span>](view-batch-history-and-export-past-results.md)
  
[<span data-ttu-id="7eeed-252">Быстрая настройка Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7eeed-252">Quick setup for Office 365 Advanced eDiscovery</span></span>](quick-setup-for-advanced-ediscovery.md)

[<span data-ttu-id="7eeed-253">Экспорт полей отчетов</span><span class="sxs-lookup"><span data-stu-id="7eeed-253">Export report fields</span></span>](export-report-fields-in-advanced-ediscovery.md)
  
[<span data-ttu-id="7eeed-254">Увеличение скорости загрузки при экспорте результатов поиска обнаружения электронных данных из Office 365</span><span class="sxs-lookup"><span data-stu-id="7eeed-254">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>](increase-download-speeds-when-exporting-ediscovery-results.md)

