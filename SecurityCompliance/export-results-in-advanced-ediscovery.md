---
title: Экспорт результатов в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Узнайте, как определить параметры для экспорта результатов из Office 365 расширенного обнаружения электронных данных, включая процедуры для указания параметров для экспорта пакета. '
ms.openlocfilehash: 92ee107ad096393fbccbc9a3dbe81d8e7dd28da9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535439"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="bcfbf-103">Экспорт результатов в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="bcfbf-103">Export results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="bcfbf-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="bcfbf-106">В этом разделе описаны параметры экспорта установки расширенных обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-106">This topic describes the Advanced eDiscovery Export Setup options.</span></span>
  
 <span data-ttu-id="bcfbf-107">**В этом разделе:**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-107">**In this topic:**</span></span>
  
- [<span data-ttu-id="bcfbf-108">Определение экспорта пакетов и сеансов</span><span class="sxs-lookup"><span data-stu-id="bcfbf-108">Defining export batches and sessions</span></span>](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [<span data-ttu-id="bcfbf-109">Экспортирует добавочного и Дополнительные</span><span class="sxs-lookup"><span data-stu-id="bcfbf-109">Incremental and additional exports</span></span>](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [<span data-ttu-id="bcfbf-110">Настройка параметров экспорта пакета</span><span class="sxs-lookup"><span data-stu-id="bcfbf-110">Set up batch export parameters</span></span>](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [<span data-ttu-id="bcfbf-111">Экспортируйте файлы отчетов</span><span class="sxs-lookup"><span data-stu-id="bcfbf-111">Export report output files</span></span>](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a><span data-ttu-id="bcfbf-112">Определение экспорта пакетов и сеансов</span><span class="sxs-lookup"><span data-stu-id="bcfbf-112">Defining export batches and sessions</span></span>
<span data-ttu-id="bcfbf-113"><a name="BK_Define"> </a></span><span class="sxs-lookup"><span data-stu-id="bcfbf-113"></span></span>

<span data-ttu-id="bcfbf-p102">Пакет экспорта позволяет обработка экспорта с использованием набора для определенных параметров. Расширенные обнаружения электронных данных позволяет определить пакетов для настройки каждого экспорта.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p102">An export batch allows export processing using a set of defined parameters. Advanced eDiscovery enables you to define batches to customize each export.</span></span>
  
<span data-ttu-id="bcfbf-p103">Параметры определяются в пакете экспорта. Пакет с именем «Экспорт пакета 01» создается по умолчанию для первого пакета дела. Можно также изменить имя пакета и описание.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p103">Parameters are defined per export batch. A batch named "Export batch 01" is created by default for the first batch of a case. You can also edit the batch name and description.</span></span>
  
<span data-ttu-id="bcfbf-119">Сеанс обмена экспорта является выполнение расширенной eDiscovery экспорта в пакет экспорта.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-119">An export session is an execution of Advanced eDiscovery Export within an export batch.</span></span>
  
## <a name="incremental-and-additional-exports"></a><span data-ttu-id="bcfbf-120">Экспортирует добавочного и Дополнительные</span><span class="sxs-lookup"><span data-stu-id="bcfbf-120">Incremental and additional exports</span></span>
<span data-ttu-id="bcfbf-121"><a name="BK_IncrementalReports"> </a></span><span class="sxs-lookup"><span data-stu-id="bcfbf-121"></span></span>

<span data-ttu-id="bcfbf-p104">Можно запустить несколько сеансов экспорта в пакет экспорта, чтобы обеспечить согласованность результатов на основе одного шаблона экспорта и параметры. Для каждого сеанса в пакете можно экспортировать аналитики для вновь обработать данные вариантов и обработке каждого «последовательно».</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p104">You can run multiple export sessions within an export batch, to ensure consistent results based on the same export template and parameters. For each session within a batch, you can export analytics for newly processed case data and process each "incrementally."</span></span>
  
<span data-ttu-id="bcfbf-p105">Чтобы экспортировать с помощью на другой набор параметров, необходимо сначала создать новый раздел. Первый сеанс в новый пакет даст результатов для обработки в случае на данный момент ли эти файлы были импортированы и обрабатываются через один или несколько Импорт файлов. Каждый пакет пересчитывает сводные таблицы, подобия, inclusives, и т.д. Сеансы используйте параметры, определенные для пакета и не пересчитывать сводные таблицы, подобия, inclusives, и т.д. для каждого сеанса выполнения.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p105">In order to export using a different set of parameters, you first need to create a new batch. The first session in the new batch will produce results for files processed in the case so far, whether or not these files were imported and processed over one or multiple Imports. Each batch recalculates pivots, similarity, inclusives, etc. Sessions use the parameters defined for the batch and do not recalculate pivots, similarity, inclusives, etc. for each session execution.</span></span>
  
<span data-ttu-id="bcfbf-p106">Например предположим, импортированные дела и анализ данных. Чтобы восстановить рядом с дубликаты и электронной почты Threading результаты для добавочных данных, нажмите кнопку **Создать Экспорт сеанса** в одном пакете, который использовался ранее для экспорта данных.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p106">For example, assume a case was imported and its data analyzed. In order to retrieve Near-duplicates and Email Threading results for the incremental data, click **Create export session** in the same batch that was previously used to export data.</span></span> 
  
## <a name="set-up-batch-export-parameters"></a><span data-ttu-id="bcfbf-129">Настройка параметров экспорта пакета</span><span class="sxs-lookup"><span data-stu-id="bcfbf-129">Set up batch export parameters</span></span>
<span data-ttu-id="bcfbf-130"><a name="BK_SetUpExport"> </a></span><span class="sxs-lookup"><span data-stu-id="bcfbf-130"></span></span>

<span data-ttu-id="bcfbf-p107">Средство экспорта eDiscovery используется для экспорта результатов поиска из расширенных обнаружения электронных данных на локальном компьютере. Чтобы повысить пропускную способность передачи данных и ускорить процесс экспорта, можно настроить параметр реестра Windows на компьютере, которая используется для экспорта результатов поиска. Если вы хотите увеличить скорость загрузки, настройте параметр реестра, прежде чем настраивать параметры экспорта. Дополнительные сведения можно [повысить скорость загрузки при экспорте результаты поиска обнаружения электронных данных в Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p107">The eDiscovery Export Tool is used to export search results from Advanced eDiscovery to your local computer. To increase the data transfer throughput and speed-up the export process, you can configure a Windows Registry setting on the computer that you use to export the search results. If you'd like to increase the download speed, configure the registry setting before you set up the export parameters. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
  
1. <span data-ttu-id="bcfbf-135">В расширенной eDiscovery select Case и нажмите кнопку **Экспорт** \> **программы установки**.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-135">In Advanced eDiscovery, select a Case and click **Export** \> **Setup**.</span></span>
    
  - <span data-ttu-id="bcfbf-136">В списке **Экспорт пакета** выберите имя пакета или экспортировать результаты в пакет экспорта 01 (пакет по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="bcfbf-136">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="bcfbf-p108">Чтобы экспортировать результаты для новых файлов, которые добавлены в существующий случай, продолжите текущего пакета. Для создания сеанса в пакете, выберите один и тот же номер пакета и нажмите кнопку **Создать Экспорт сеанса** этот параметр можно использовать для экспорта те же параметры предыдущей пакетного добавочного образом.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p108">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="bcfbf-p109">Чтобы экспортировать в новый раздел, нажмите кнопку **Добавить**![добавить значок](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)и введите новое имя в поле **имя пакета** (или примите значение по умолчанию) и описание в **поле Описание пакета**. Нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p109">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="bcfbf-141">Чтобы изменить имя пакета или описание, выберите имя в **пакет экспорта**, нажмите кнопку **Изменить** ![значок Правка](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)и затем изменить поля.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-141">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="bcfbf-p110">При запуске сеансов для экспорта партии их невозможно удалить. Кроме того можно изменять только некоторые параметры, после запуска первого сеанса.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p110">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="bcfbf-144">Создание пакета повторяющихся экспорта, выберите **пакет экспорта повторяющихся**![создать значок пакета повторяющихся экспорта](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) и введите имя и описание для повторяющихся пакета на панели.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-144">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="bcfbf-145">Чтобы удалить пакет экспорта, выберите команду **Удалить**![удалить значок пакета экспорта](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span><span class="sxs-lookup"><span data-stu-id="bcfbf-145">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="bcfbf-146">Чтобы просмотреть журнал пакет, выберите **Журнал пакетов**![значок представления журнала](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span><span class="sxs-lookup"><span data-stu-id="bcfbf-146">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="bcfbf-147">В разделе **совокупности**Чтобы настроить параметры для вашего пакета экспорта выберите **включать только файлы, над показатель релевантности срока** и/или **Уточнение Экспорт пакета** .</span><span class="sxs-lookup"><span data-stu-id="bcfbf-147">Under **Population**,Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch.</span></span> 
    
3. <span data-ttu-id="bcfbf-p111">Если выбран параметр **Включить только файлы над прекращения показатель релевантности**, **проблема** включена. Если показатель релевантности файла больше, чем показатель прекращения для выбранного проблемы, файл будет экспортироваться пока исключен фильтром «для просмотра».</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p111">If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled. If the file's relevance score is higher than the cut-off score for the selected issue, the file will be exported unless it's excluded by the 'For review' filter.</span></span> 
  
<span data-ttu-id="bcfbf-p112">При выборе **пакета экспорта уточнение** **отзыва Копировать** и фильтрация по «К рассмотрению» включено поле переключателей. Если выбрано **отзыва Копировать**, а затем повторяющиеся файлы не будут отображаться в соответствии с определена политика [случае уровень (по умолчанию): из каждого набора повторяющихся файлов в случае всего лишь один файл будет отзыва duped. Уровень custodian: из каждого набора повторяющихся файлов же custodian только один файл будет отзыва duped.] Выходные данные экспорта содержит записи всех повторяющихся файлов. Если выбрано поле **Filter by «для просмотра»** , выберите **изменить в разделе метаданные** , чтобы ввести настройки поля **«для просмотра»** . Выберите **Включить входных файлов** для включения исходных файлов в содержимое пакета. Снимите этот параметр, чтобы ускорить процесс экспорта. Обратите внимание, что собственные файлы будут экспортироваться в любом случае.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p112">If you select **Refine export batch**, the **De-dupe** and Filter by 'For review' field radio buttons are enabled. If you choose **De-dupe**, then duplicate files will be filtered out according to the policy defined [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped.] The export output contains a record of all duplicate files. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files** to include source files in the package content. You can clear this setting to speed up the export process. Note that the Native files will be exported in any case.</span></span> 
    
4. <span data-ttu-id="bcfbf-157">В разделе **метаданные**выберите из следующих вариантов в списке **Экспорт шаблона** (одно на сеанс).</span><span class="sxs-lookup"><span data-stu-id="bcfbf-157">Under **Metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="bcfbf-p113">**Стандартный**: базовый набор элементов данных, метаданных и свойств. Используйте этот вариант, когда импорт данных уже было обработано в расширенной обнаружения электронных данных и загрузил Экспорт данных в системе, которая уже содержит файлы. По умолчанию Экспорт шаблона столбцы созданы и заполнены.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p113">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="bcfbf-p114">**Все**: полный набор стандартных метаданных, включая все обработки данных, а также анализировать и релевантности показателям. Этот шаблон является обязательным при расширенной eDiscovery выполняет обработку и загрузке файлов данных для внешней системы в первый раз.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p114">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="bcfbf-163">**Проблемы**: выберите **Все проблемы** или выберите конкретную проблему создания.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-163">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
5. <span data-ttu-id="bcfbf-164">В разделе **назначения**:</span><span class="sxs-lookup"><span data-stu-id="bcfbf-164">Under **Destination**:</span></span>
    
  - <span data-ttu-id="bcfbf-165">**Загрузите файл на локальном компьютере**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-165">**Download to local machine**</span></span>
    
  - <span data-ttu-id="bcfbf-166">**Экспорт в пользовательских Azure blob**: Если этот параметр выбран, можно указать контейнер URL-адрес и SAS маркер.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-166">**Export to user-defined Azure blob**: If this is checked, you can specify a container URL and SAS token.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="bcfbf-p115">После пакета экспорта сохраняется, чтобы пользователем Azure больших двоичных объектов, данные больше не управляется расширенной обнаружения электронных данных; управляется Azure больших двоичных объектов. Это означает, что при удалении регистр, экспортированные файлы по-прежнему останется на Azure больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p115">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery; it's managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="bcfbf-169">**Сохраните SAS маркер для будущего экспорта сеанса**: Если этот флажок установлен, маркер SAS шифруются в расширенной eDiscovery внутренней базы данных для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-169">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="bcfbf-p116">В настоящее время SAS истечения срока действия маркера после месяца. При попытке загрузки после более чем месяца необходимо отменить последнего сеанса, затем экспортируйте еще раз.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p116">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
6. <span data-ttu-id="bcfbf-172">Нажмите кнопку **Изменить** , чтобы задать «для просмотра "Параметры полей.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-172">Click **Modify** to set the "for review' field settings.</span></span> 
    
> ![Настройка для проверки seetings поля для экспорта партии](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
    In **For review field settings** panel, in **Select scenario**, select the scenario and scope of the review. The settings are displayed based on your selection.
    
    **Review all** (default): All emails, attachments, and documents are selected by default. 
    
    **Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.
    
    **Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. 
    
    If you select custom, you can then customize the settings for emails, documents, attachments and miscellaneous.
    
> <span data-ttu-id="bcfbf-174">В **сообщения электронной почты** выберите сообщения электронной почты, которые необходимо экспортировать.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-174">In **Emails** select the emails you want to export:</span></span> 
    
    **All emails**: (default) All emails are selected.
    
    **Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.
    
    **Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .
    
> <span data-ttu-id="bcfbf-175">В **документах** выберите документы, которые требуется экспортировать:</span><span class="sxs-lookup"><span data-stu-id="bcfbf-175">In **Documents** select the documents you want to export:</span></span> 
    
    **All documents**: (default) All documents are selected.
    
    **Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.
    
    **Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).
    
> <span data-ttu-id="bcfbf-176">Выберите вложения, которые требуется экспортировать в **вложения**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-176">In **Attachments** select the attachments you want to export</span></span> 
    
    **All attachments**: (default) All attachments are selected.
    
    **Unique attachment in case level**: Unique attachment files within the specified case.
    
    **Unique attachment in email set level**: Unique attachment files within the specified email case.
    
> <span data-ttu-id="bcfbf-p117">В **Micellaneous** можно **рассматривать вложения как документы**, **рассматривать как документы по электронной почте**или **Развернуть для включения семейства файлов**. При выборе **развертывания для включения семейства файлы**для каждого файла, помеченная для ознакомления также отмечаемых все файлы из того же семейства.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p117">In **Micellaneous** you can choose to **Treat attachments as documents**, **Treat emails as documents**, or **Expand to include family files**. When you choose **Expand to include family files**, for each file that is flagged for review, all files of the same family will also be flagged.</span></span>
    
    Choose **Save** to save the settings. 
    
7. <span data-ttu-id="bcfbf-179">Указав параметры экспорта, чтобы запустить пакет экспорта, щелкните **Создать Экспорт сеанса**.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-179">After you specify export parameters, to start export batch, click **Create export session**.</span></span>
    
    <span data-ttu-id="bcfbf-p118">Во время экспорта состояние отображается в **состояние задачи**. Результаты отображаются в **экспортируемом сводки**.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p118">During export, the status is displayed in **Task status**. The results are displayed in **Export summary**.</span></span>
    
8. <span data-ttu-id="bcfbf-182">В окне **загрузки файлов** нажмите кнопку **Копировать в буфер обмена** для копирования ключа экспорта.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-182">In the **Download files** window, click **Copy to clipboard** to copy the Export key.</span></span> 
    
    ![Загрузка файлов](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
9. <span data-ttu-id="bcfbf-184">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-184">Click **Close**.</span></span> 
    
    <span data-ttu-id="bcfbf-185">Запускается средство экспорта обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-185">The eDiscovery Export Tool is started.</span></span>
    
    ![Средство экспорта обнаруженных электронных данных](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
10. <span data-ttu-id="bcfbf-187">В **eDiscovery средство экспорта**:</span><span class="sxs-lookup"><span data-stu-id="bcfbf-187">In the **eDiscovery Export Tool**:</span></span>
    
1. <span data-ttu-id="bcfbf-188">**Вставьте подпись общих доступа, который будет использоваться для подключения к источнику**вставьте в экспорт ключа, youcopied в буфер обмена на шаге 7.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-188">In **Paste the Shared Access Signature that will be used to connect to the source**, paste the Export key that youcopied to the clipboard in step 7.</span></span>
    
2. <span data-ttu-id="bcfbf-189">Нажмите кнопку **Обзор** , чтобы выбрать целевое расположение для хранения файлов экспорта загруженного на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-189">Click **Browse** to select the target location for storing the downloaded export files on the local machine.</span></span> 
    
11. <span data-ttu-id="bcfbf-p119">Нажмите кнопку **Пуск**. Экспорт файлы загружаются на локальном компьютере. Если Вы разрешили **экспорта для пользовательских Azure больших двоичных объектов** на шаге 4, сеанс экспортируется в URL-адрес хранилища больших двоичных объектов на выбор.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p119">Click **Start**.The export files are downloaded to the local machine. If you chose **Export to user-defined Azure blob** in step 4, the session is exported to a Blob storage URL destination of your choosing.</span></span> 
    
<span data-ttu-id="bcfbf-192">Полное описание поля в отчет экспорта в разделе [Экспорт полей отчета](export-report-fields-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="bcfbf-192">For a full description of the fields in the export report, see [Export report fields](export-report-fields-in-advanced-ediscovery.md).</span></span>
  
## <a name="export-report-output-files"></a><span data-ttu-id="bcfbf-193">Экспортируйте файлы отчетов</span><span class="sxs-lookup"><span data-stu-id="bcfbf-193">Export report output files</span></span>
<span data-ttu-id="bcfbf-194"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="bcfbf-194"></span></span>

<span data-ttu-id="bcfbf-195">В следующей таблице приведены выходные файлы, которые создаются при выполнении пакет экспорта.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-195">The following table lists the output files that are generated when you run an Export batch.</span></span>
  
|<span data-ttu-id="bcfbf-196">**Имя файла**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-196">**File name**</span></span>|<span data-ttu-id="bcfbf-197">**Тип файла**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-197">**File type**</span></span>|<span data-ttu-id="bcfbf-198">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bcfbf-198">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bcfbf-199">Сводка экспорта</span><span class="sxs-lookup"><span data-stu-id="bcfbf-199">Export summary</span></span>  <br/> |<span data-ttu-id="bcfbf-200">CSV</span><span class="sxs-lookup"><span data-stu-id="bcfbf-200">csv</span></span>  <br/> |<span data-ttu-id="bcfbf-201">Файл журнала, созданных функцией обнаружения электронных данных средство экспорта.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-201">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="bcfbf-202">Трассировки</span><span class="sxs-lookup"><span data-stu-id="bcfbf-202">Trace</span></span>  <br/> |<span data-ttu-id="bcfbf-203">TXT</span><span class="sxs-lookup"><span data-stu-id="bcfbf-203">txt</span></span>  <br/> |<span data-ttu-id="bcfbf-204">Файл журнала, созданных функцией обнаружения электронных данных средство экспорта.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-204">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="bcfbf-205">Извлеченные текстовые файлы</span><span class="sxs-lookup"><span data-stu-id="bcfbf-205">Extracted text files</span></span>  <br/> |<span data-ttu-id="bcfbf-206">Папки с файлом</span><span class="sxs-lookup"><span data-stu-id="bcfbf-206">File folder</span></span>  <br/> |<span data-ttu-id="bcfbf-207">Папка, содержащая Извлеченные текстовые файлы экспортированных файлов.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-207">Folder that contains the extracted text files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="bcfbf-208">Входные данные или собственные файлы</span><span class="sxs-lookup"><span data-stu-id="bcfbf-208">Input or native files</span></span>  <br/> |<span data-ttu-id="bcfbf-209">Папки с файлом</span><span class="sxs-lookup"><span data-stu-id="bcfbf-209">File folder</span></span>  <br/> |<span data-ttu-id="bcfbf-210">Папка, содержащая файлы собственный и ввода экспортированные файлы.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-210">Folder that contains the native and input files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="bcfbf-211">Экспорт списка</span><span class="sxs-lookup"><span data-stu-id="bcfbf-211">Export list</span></span>  <br/> |<span data-ttu-id="bcfbf-212">XLSX</span><span class="sxs-lookup"><span data-stu-id="bcfbf-212">xlsx</span></span>  <br/> |<span data-ttu-id="bcfbf-p120">Метаданные экспортированные файлы в формате xlsx. Поля в файлах в соответствии с шаблона пользователь выбирает для экспорта. При необходимости, создается несколько файлов, каждый содержит строк 100-150 КБ. Если определенное значение содержит больше символов, чем может содержать ячейки Excel (в настоящее время ограничение составляет 32 767 символов), а затем будет Обрезка значения для Максимальная длина. Если значение обрезается, цвет фона ячейки красный цвет, чтобы указать для пользователя.» Участники электронной почты» является примером поле, которое может превышать ограничение на длину, если сообщение электронной почты отправлено в крупных рассылки. Для получения дополнительных сведений о полях выходные данные в разделе [Экспорт полей отчета](export-report-fields-in-advanced-ediscovery.md) .</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p120">Exported files metadata in xlsx format. Fields in files are according to template user selects to export. If needed, several files are created, each contains 100-150K rows. If a certain value contains more characters than an Excel cell can contain (currently the limit is 32,767 characters), then the value will be trimmed to the maximum length allowed. If a value is trimmed, the cell's background color is red to indicate this to the user."Email participants" is an example of a field that can exceed the length limit, if the email was sent to a large distribution. See [Export report fields](export-report-fields-in-advanced-ediscovery.md) for details about the output fields.  </span></span><br/> |
|<span data-ttu-id="bcfbf-219">Загрузить файл</span><span class="sxs-lookup"><span data-stu-id="bcfbf-219">Load file</span></span>  <br/> |<span data-ttu-id="bcfbf-220">CSV</span><span class="sxs-lookup"><span data-stu-id="bcfbf-220">csv</span></span>  <br/> |<span data-ttu-id="bcfbf-p121">Метаданные экспортированных файлов в формат csv для загрузки в другом приложении. Поля в файлах в соответствии с шаблона пользователь выбирает для экспорта.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p121">Exported files metadata in csv format for loading into a different application. Fields in files are according to template user selects to export.</span></span>  <br/> |
|<span data-ttu-id="bcfbf-223">Индикатор успеха</span><span class="sxs-lookup"><span data-stu-id="bcfbf-223">Success indicator</span></span>  <br/> |<span data-ttu-id="bcfbf-224">TXT</span><span class="sxs-lookup"><span data-stu-id="bcfbf-224">txt</span></span>  <br/> |<span data-ttu-id="bcfbf-p122">Только созданные при экспорте третьей стороне Azure больших двоичных объектов. При экспорте полностью успешно, файл будет создан. В случае отказа или частичный успех файл не создаются. Файл создается в корневом каталоге, позволяя автоматического отслеживания на различных статусов экспорт пакетов/сеансов. Это пустой файл. — Это имя: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span><span class="sxs-lookup"><span data-stu-id="bcfbf-p122">Only created when exporting to a 3rd party Azure blob. If export succeed completely, the file will be created. In case of failure, or partial success the file will not be created. File will be created in the root folder, allowing automated tracking on different Export batches/sessions statuses. This is an empty file. Its name is: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bcfbf-231">См. также</span><span class="sxs-lookup"><span data-stu-id="bcfbf-231">See also</span></span>
<span data-ttu-id="bcfbf-232"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="bcfbf-232"></span></span>

[<span data-ttu-id="bcfbf-233">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="bcfbf-233">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="bcfbf-234">Просмотр журнала пакета и экспорт предыдущих результатов</span><span class="sxs-lookup"><span data-stu-id="bcfbf-234">Viewing batch history and exporting past results</span></span>](view-batch-history-and-export-past-results.md)
  
[<span data-ttu-id="bcfbf-235">Быстрая настройка Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="bcfbf-235">Quick setup for Office 365 Advanced eDiscovery</span></span>](quick-setup-for-advanced-ediscovery.md)

[<span data-ttu-id="bcfbf-236">Экспорт отчета полей</span><span class="sxs-lookup"><span data-stu-id="bcfbf-236">Export report fields</span></span>](export-report-fields-in-advanced-ediscovery.md)
  
[<span data-ttu-id="bcfbf-237">Увеличение скорости при экспорте результаты поиска обнаружения электронных данных из Office 365</span><span class="sxs-lookup"><span data-stu-id="bcfbf-237">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>](increase-download-speeds-when-exporting-ediscovery-results.md)

