---
title: Просмотр результатов модуля обработки в Office 365 Advanced eDiscovery
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
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Сведения о том, как найти результаты модуля процесса выполните в Office 365 расширенного обнаружения электронных данных, включая состояние задачи и процесс сводки.  '
ms.openlocfilehash: 01093b0230aaf78ab7ccf1235f0874a0b69aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534262"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="262ce-103">Просмотр результатов модуля обработки в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="262ce-103">View Process module results in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="262ce-104">После **подготовки** \> инициировал **процесс** , можно просмотреть ход выполнения и результаты.</span><span class="sxs-lookup"><span data-stu-id="262ce-104">After **Prepare** \> **Process** is initiated, you can view progress and results.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="262ce-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="262ce-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="process-task-status"></a><span data-ttu-id="262ce-107">Состояние процесса задачи</span><span class="sxs-lookup"><span data-stu-id="262ce-107">Process task status</span></span>

<span data-ttu-id="262ce-108">В статье **Prepare** \> **процесс** \> **результатов**на странице отображается текущее состояние (если процесс выполняется в данный момент) или последнего состояния задачи состояние процесса как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="262ce-108">In **Prepare** \> **Process** \> **Results**, the page shows the current status (if Process is currently running) or the last Process status task status as shown in the following example.</span></span>
  
![Состояние задач для модуля обработки](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
<span data-ttu-id="262ce-110">Отображаемые задачи зависит от выбранных параметров процесс.</span><span class="sxs-lookup"><span data-stu-id="262ce-110">The displayed tasks may vary depending on the Process options selected.</span></span> 
  
- <span data-ttu-id="262ce-111">**Перечень**: расширенные eDiscovery итерацию всех файлов, выбранных для процесса и выполняет сбора основных данных.</span><span class="sxs-lookup"><span data-stu-id="262ce-111">**Inventory**: Advanced eDiscovery iterates through all files selected for Process and performs basic data collection.</span></span>
    
- <span data-ttu-id="262ce-112">**Расчет подписей**: вычисляет MD5 цифровых подписей.</span><span class="sxs-lookup"><span data-stu-id="262ce-112">**Calculate signatures**: Calculates the MD5 digital signatures.</span></span>
    
- <span data-ttu-id="262ce-p102">**Извлечение соединения**: извлекает внутренние или автономные файлы рекурсивно из составных файлов (например, PST-файлов, ZIP, MSG). Извлеченные файлы хранятся в папке делами регистр.</span><span class="sxs-lookup"><span data-stu-id="262ce-p102">**Compounds extraction**: Extracts inner or contained files recursively from compound files (for example, PST, ZIP, MSG). Extracted files are stored in the case folder of the case.</span></span>
    
- <span data-ttu-id="262ce-115">**Синхронизация баз данных**: процесс внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="262ce-115">**Synchronizing database**: Internal database process.</span></span>
    
- <span data-ttu-id="262ce-p103">**Копирование файлов**: обработки копии файлов. Эта задача всегда отображается, даже в том случае, если выбран параметр Дополнительные файлы копии.</span><span class="sxs-lookup"><span data-stu-id="262ce-p103">**File copy**: Copies Process files. This task is always displayed, even when the advanced Copy files option is selected.</span></span>
    
- <span data-ttu-id="262ce-p104">**Извлечение текста**: при наличии файлы в формате, расширенные eDiscovery извлекает текст из этих файлов с помощью DTSearch. Извлеченный текст из этих файлов сохраняется как текстовые файлы в папке вариантов.</span><span class="sxs-lookup"><span data-stu-id="262ce-p104">**Text extraction**: When there are native files, Advanced eDiscovery extracts text from these files using DTSearch. The extracted text of these files is stored as text files in the case folder.</span></span>
    
- <span data-ttu-id="262ce-120">**Обновление метаданных**: обрабатывает загруженных метаданных.</span><span class="sxs-lookup"><span data-stu-id="262ce-120">**Updating metadata**: Processes the loaded metadata.</span></span> 
    
- <span data-ttu-id="262ce-121">**Finalizing**: Внутренняя обработка, завершающий данные загружены делами файлы (например, идентификации ошибки и успешности файлов).</span><span class="sxs-lookup"><span data-stu-id="262ce-121">**Finalizing**: Internal processing that finalizes data of loaded case files (for example, identify error and success files).</span></span> 
    
<span data-ttu-id="262ce-p105">Состояние задачи: отображается после завершения задачи. Во время выполнения задачи, отображается длительность.</span><span class="sxs-lookup"><span data-stu-id="262ce-p105">Task status: Displayed after task completion. While tasks are running, run duration is displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="262ce-124">Завершенные задачи могут также включать итоговые значения для файлов, которые завершения обработки и файлов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="262ce-124">Completed tasks may also include totals for files that completed processing or files with errors.</span></span> 
  
> [!TIP]
> <span data-ttu-id="262ce-p106">«Отмена» предоставляет параметр отката, чтобы остановить выполнение процесса и затем откат к предыдущей заполнения данных или сохранения обработанные данные. Откат очищает все обработанные данные. Если не хотите, чтобы обработанные данные к потере (например, при планировании для перезагрузки этих файлов), выберите «Отмена» параметр в это окно, чтобы отказаться от отката.</span><span class="sxs-lookup"><span data-stu-id="262ce-p106">"Cancel" provides a rollback option to stop Process execution and then roll back to the previous data population or saved processed data. Rollback clears all processed data. If you do not want the processed data to be lost (for example, you plan to reload these files), select the "Cancel" option in this window to choose not to roll back.</span></span> 
  
## <a name="process-summary"></a><span data-ttu-id="262ce-128">Сводка процесса</span><span class="sxs-lookup"><span data-stu-id="262ce-128">Process summary</span></span>

<span data-ttu-id="262ce-129">В статье Prepare \> процесс \> результатов \> процесса сводки, декомпозиции загруженный файл результатов — это отображаемые в зависимости от успешные файл результаты обработки и ошибки.</span><span class="sxs-lookup"><span data-stu-id="262ce-129">In Prepare \> Process \> Results \> Process summary, a breakdown of loaded file results is displayed according to successful file processing and error results.</span></span>
  
<span data-ttu-id="262ce-130">Области представить графического отображения статистики импортируемый файл следующим образом:</span><span class="sxs-lookup"><span data-stu-id="262ce-130">The panes present a graphical display of imported file statistics, as follows:</span></span>
  
- <span data-ttu-id="262ce-131">**Суммирование процесса сводки**d:, все файлы в случае.</span><span class="sxs-lookup"><span data-stu-id="262ce-131">**Process summary accumulate**d: All files in the case.</span></span>
    
- <span data-ttu-id="262ce-132">**Обработать Сводка последнего**: файлы загружаются из последнего сеанса или действие.</span><span class="sxs-lookup"><span data-stu-id="262ce-132">**Process summary last**: Files loaded from the last session or action.</span></span> 
    
- <span data-ttu-id="262ce-133">**Последние семейств**: сведения о семействе в случае (при его наличии).</span><span class="sxs-lookup"><span data-stu-id="262ce-133">**Families last**: Family information in the case (if any).</span></span>
    
- <span data-ttu-id="262ce-134">При **инициализации** файлы были добавлены, число файлов начального значения отображается на проблему, который был определен для файлов.</span><span class="sxs-lookup"><span data-stu-id="262ce-134">If **Seed** files were added, the number of seed files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="262ce-135">В случае сбоя маркировку **Начальное число** файлов, который также сказано.</span><span class="sxs-lookup"><span data-stu-id="262ce-135">If the marking of **Seed** files failed, that is also noted.</span></span> 
    
- <span data-ttu-id="262ce-136">При **предварительно с меткой** файлы были добавлены, количество предварительно с тегами файлов отображается на проблему, который был определен для файлов.</span><span class="sxs-lookup"><span data-stu-id="262ce-136">If **Pre-tagged** files were added, the number of pre-tagged files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="262ce-137">В случае сбоя маркировку **предварительно с меткой** файлов, который также сказано.</span><span class="sxs-lookup"><span data-stu-id="262ce-137">If the marking of **Pre-tagged** files failed, that is also noted.</span></span> 
    
![Сводка по модулю обработки](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a><span data-ttu-id="262ce-139">Сводка процесса возникшую, а затем диаграмм</span><span class="sxs-lookup"><span data-stu-id="262ce-139">Process summary accumulated and last charts</span></span>

<span data-ttu-id="262ce-140">Левая панель содержит источник + извлеченные файлы: которого является все файлы найден.</span><span class="sxs-lookup"><span data-stu-id="262ce-140">The left bar includes Source + extracted files: which is all files found.</span></span> 
  
<span data-ttu-id="262ce-141">Правой панели, обработанных, включает:</span><span class="sxs-lookup"><span data-stu-id="262ce-141">The right bar, Processed, includes:</span></span>
  
- <span data-ttu-id="262ce-142">Файлы с ошибками нагрузки</span><span class="sxs-lookup"><span data-stu-id="262ce-142">Files with load errors</span></span>
    
- <span data-ttu-id="262ce-143">Успешной загрузке файлов, которые могут включать:</span><span class="sxs-lookup"><span data-stu-id="262ce-143">Successfully loaded files, which may include:</span></span> 
    
  - <span data-ttu-id="262ce-144">**Существующие**: файлы, которые были загружены до и теперь загружается еще раз (в том числе дубликатов).</span><span class="sxs-lookup"><span data-stu-id="262ce-144">**Existing**: Files that were loaded before and are now loaded again (including duplicates).</span></span>
    
  - <span data-ttu-id="262ce-145">**Текст**: уникальный файлы с текстом.</span><span class="sxs-lookup"><span data-stu-id="262ce-145">**Text**: Unique files with text.</span></span>
    
  - <span data-ttu-id="262ce-146">**Текст не**: очистить текстовые файлы, пустой собственный текстовые файлы, файлы в формате нетекстовых.</span><span class="sxs-lookup"><span data-stu-id="262ce-146">**Non-text**: Empty text files, empty native text files, native non-text files.</span></span> 
    
  - <span data-ttu-id="262ce-147">**Дублирующиеся**s: повторяющихся файлов с текстом.</span><span class="sxs-lookup"><span data-stu-id="262ce-147">**Duplicate**s: Duplicate files with text.</span></span>
    
## <a name="last-process-errors"></a><span data-ttu-id="262ce-148">Последний обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="262ce-148">Last process errors</span></span>

<span data-ttu-id="262ce-149">В статье Prepare \> процесс \> результатов \> последней обработки ошибок, сведения о ошибок во время последнего сеанса или действие, выполняемое, отображаются.</span><span class="sxs-lookup"><span data-stu-id="262ce-149">In Prepare \> Process \> Results \> Last process errors, details of the errors in the last session or action performed are displayed.</span></span>
  
![Ошибки модуля обработки](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a><span data-ttu-id="262ce-151">См. также</span><span class="sxs-lookup"><span data-stu-id="262ce-151">See also</span></span>

[<span data-ttu-id="262ce-152">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="262ce-152">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="262ce-153">Под управлением модуля процесса и загрузка данных</span><span class="sxs-lookup"><span data-stu-id="262ce-153">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

