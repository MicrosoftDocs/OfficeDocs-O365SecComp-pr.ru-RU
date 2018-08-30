---
title: Настройка загрузок для добавления импортированных файлов в Office 365 Advanced eDiscovery
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Просмотрите действия, чтобы добавить импортируемые файлы последнего нагрузки или пакетного файлов перед выполнением учебный курс по релевантности в Office 365 расширенного обнаружения электронных данных.  '
ms.openlocfilehash: 2c986578b969b671351930fd6939a90e3a821dc2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535370"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a><span data-ttu-id="06a8a-103">Настройка загрузок для добавления импортированных файлов в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="06a8a-103">Set up loads to add imported files in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="06a8a-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="06a8a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="06a8a-p102">В расширенной eDiscovery нагрузки — это новый пакет файлы, добавленные в случае. По умолчанию определенные один нагрузки и всех импортированных файлов добавляются к нему. Перед выполнением учебный курс по релевантности, необходимо добавить импортируемые файлы для загрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p102">In Advanced eDiscovery, a load is a new batch of files added to a case. By default, one load is defined and all imported files are added to it. Before performing Relevance training, imported files must be added to the load.</span></span> 
  
<span data-ttu-id="06a8a-109">Рассмотрим следующие сценарии:</span><span class="sxs-lookup"><span data-stu-id="06a8a-109">Consider the following scenarios:</span></span>
  
- <span data-ttu-id="06a8a-p103">Новые файлы называют похоже на предыдущих файлов, загруженных в базу данных case или предыдущей загрузки файлов был в случайном порядке набор из коллекции файлов. В этом экземпляре добавьте импортируемые файлы текущего файла нагрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p103">New files are known to be similar to the previous files loaded to the case database, or the previous load of files was a random set from the file collection. In this instance, add the imported files to the current file load.</span></span>
    
- <span data-ttu-id="06a8a-p104">Новые файлы отличаются от предыдущих (например, из другого источника) или нет предыдущего сведений, если они аналогичные или другой предыдущей нагрузок. В этом случае добавьте новый файл нагрузки импортируемые файлы. Расширенные eDiscovery распознает его как сценарий загружает последовательные, вызывает дополнительной процесс, блокирует релевантности обучения и вычисления пакета до завершения захват и новые нагрузки интегрированное и обучение.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p104">New files are different from previous ones (for example, from a different source), or you have no prior knowledge that they're similar or different to the previous loads. In this scenario, add the imported files to a new file load. Advanced eDiscovery recognizes this as a Rolling loads scenario, invokes a Catch-up process, locks Relevance training and Batch calculations until Catch-up is completed, and the new load is integrated and trained.</span></span> 
    
## <a name="adding-imported-files-to-the-current-load"></a><span data-ttu-id="06a8a-115">Добавление импортированных файлов на текущем нагрузки</span><span class="sxs-lookup"><span data-stu-id="06a8a-115">Adding imported files to the current load</span></span>

<span data-ttu-id="06a8a-p105">Все импортированные файлы необходимо добавить нагрузки для обработки в расширенной обнаружения электронных данных. Импортируемые файлы добавляются последнего нагрузки. Если позднее импортировать дополнительные файлы, они также необходимо добавить загрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p105">All imported files must be added to a load to be processed in Advanced eDiscovery. Imported files are added to the last defined load. If you import additional files later, they also must be added to the load.</span></span>
  
1. <span data-ttu-id="06a8a-119">В **релевантности \> установки релевантности** выберите **нагрузок**.</span><span class="sxs-lookup"><span data-stu-id="06a8a-119">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
    ![Элемент "Операции загрузки" на вкладке "Настройка релевантности"](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. <span data-ttu-id="06a8a-p106">**Включаемых файлов**: выберите соответствующее значение параметра файлы для включения. По умолчанию Добавление файлов на текущем нагрузки основано на заполнение «Все файлы».</span><span class="sxs-lookup"><span data-stu-id="06a8a-p106">**Include files**: Select an option for files to include. By default, adding files to the current load is based on the "All files" population.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="06a8a-p107">Загрузите все доступные файлы culled в релевантности. Если планируется загрузить только подмножество доступных файлов, впервые, проконсультируйтесь с поддержки, как Загрузка подмножеств может отрицательно сказаться на учебный курс по релевантности.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p107">Load all available culled files into Relevance. If you plan to load only a subset of the available files, please first consult with Support, as loading subsets can adversely affect Relevance training.</span></span> 
  
3. <span data-ttu-id="06a8a-125">Возможности **управления нагрузками**выберите нагрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-125">In **Loads management**, select a load.</span></span>
    
4. <span data-ttu-id="06a8a-p108">Щелкните **Добавить файлы**. Добавить файлы для загрузки и отобразится сообщение с подтверждением.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p108">Click **Add files**. The files are added to the load and a confirmation message is displayed.</span></span> 
    
5. <span data-ttu-id="06a8a-128">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="06a8a-128">Click **OK**.</span></span>
    
<span data-ttu-id="06a8a-129">Файлы могут теперь обрабатываться в расширенной eDiscovery релевантности для обучения файлы.</span><span class="sxs-lookup"><span data-stu-id="06a8a-129">The files can now be processed in Advanced eDiscovery Relevance for training the files.</span></span>
  
## <a name="editing-a-load-name-within-a-case"></a><span data-ttu-id="06a8a-130">Изменение имени нагрузки в случае</span><span class="sxs-lookup"><span data-stu-id="06a8a-130">Editing a load name within a case</span></span>

<span data-ttu-id="06a8a-131">Если изменить имя нагрузки, рекомендуется использовать имя, которое имеет значение в рамках данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="06a8a-131">If changing the load name, it is recommended to use a name that is significant to the case.</span></span>
  
1. <span data-ttu-id="06a8a-132">В **релевантности \> установки релевантности** выберите **нагрузок**.</span><span class="sxs-lookup"><span data-stu-id="06a8a-132">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="06a8a-p109">В списке **управления нагрузками** выберите нагрузки и щелкните значок **Правка** . Откроется окно редактирования нагрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p109">From the **Loads management** list, select a load and click the **Edit** icon. The Edit load window is displayed.</span></span> 
    
3. <span data-ttu-id="06a8a-135">Внесите необходимые изменения и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="06a8a-135">Enter the changes, and then click **OK**.</span></span>
    
## <a name="adding-imported-files-to-a-new-load"></a><span data-ttu-id="06a8a-136">Добавление импортированных файлов в новый нагрузки</span><span class="sxs-lookup"><span data-stu-id="06a8a-136">Adding imported files to a new load</span></span>

<span data-ttu-id="06a8a-137">После запуска релевантности обучении и для выполнения вычислений пакета, можно импортировать и обрабатывать дополнительные набор файлов.</span><span class="sxs-lookup"><span data-stu-id="06a8a-137">After starting Relevance training or performing Batch calculation, you may want to import and process an additional set of files.</span></span> 
  
<span data-ttu-id="06a8a-p110">Во время захват можно создавать, тега и анализировать захват set. Расширенные eDiscovery сравнивает его оценки Relevant и не Relevant файлов в новый нагрузку так, чтобы в предыдущем нагрузок. На основе результатов, будет предложено принять решения захват Если eDiscovery необходимые и дополнительные рекомендации на основе сведений начисления релевантности.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p110">During Catch-up, you can create, tag, and analyze the Catch-up set. Advanced eDiscovery compares its assessment of Relevant and Non-Relevant files in the new load to those in previous loads. Based on the results, you are prompted to make Catch-up decisions, if necessary, and Advanced eDiscovery provides recommendations based on the accrued Relevance information.</span></span> 
  
<span data-ttu-id="06a8a-141">Ваши загружается и дополнительной функциональности изменяется в соответствии следующим образом:</span><span class="sxs-lookup"><span data-stu-id="06a8a-141">Rolling Loads and Catch-up functionality varies as follows:</span></span> 
  
- <span data-ttu-id="06a8a-142">При импорте нового файла нагрузки после пакета расчета расширенных обнаружения электронных данных определяет, насколько файлы попадают в одну из следующих категорий:</span><span class="sxs-lookup"><span data-stu-id="06a8a-142">When you import a new file load after Batch calculation, Advanced eDiscovery determines to what extent the files fall into one of the following categories:</span></span>
    
  - <span data-ttu-id="06a8a-143">Аналогично (однородных): новые настраиваемые круга учебный курс по релевантности не является обязательным и базы знаний, начисления из предыдущей нагрузки может применяться «как есть» для нового нагрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-143">Similar (homogeneous): A new, custom round of Relevance training is not required and the knowledge accrued from the previous load can be applied "as is" to the new load.</span></span> 
    
  - <span data-ttu-id="06a8a-144">DISTINCT (разнородных): нового настраиваемого круга учебный курс по релевантности является обязательным и не могут быть применены базы знаний, начисления из предыдущей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-144">Distinct (heterogeneous): A new, custom round of Relevance training is required, and the knowledge accrued from the previous load cannot be applied.</span></span> 
    
    <span data-ttu-id="06a8a-145">Эти термины относятся к уровень подобия файлов между нагрузок, а не в нагрузок.</span><span class="sxs-lookup"><span data-stu-id="06a8a-145">These terms refer to the level of similarity of files between loads and not within the loads.</span></span> 
    
- <span data-ttu-id="06a8a-p111">При импорте нового файла нагрузки во время учебный курс по релевантности (до расчет пакета), захват позволяет продолжить учебный курс по релевантности в наборе united файла. Расширенные eDiscovery не оценка ли новые нагрузки аналогичную или отличались от предыдущей нагрузки. Просто собирает сведения о новых нагрузки и позволяет релевантности учебный курс, чтобы продолжить на новые и предыдущие задает файлов.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p111">When importing a new file load during Relevance training (before Batch calculation), Catch-up enables you to continue Relevance training on the united file set. Advanced eDiscovery does not estimate whether the new load is similar to or distinct from the previous load. It simply collects information about the new load and enables Relevance training to continue on the new and previous sets of files.</span></span> 
    
- <span data-ttu-id="06a8a-149">При наличии нескольких проблем в учебный курс по релевантности, а также проблем после расчета пакета, захват процесс выполняется один раз для всех ошибок и результаты вычисляются и отображаются для каждой проблемы.</span><span class="sxs-lookup"><span data-stu-id="06a8a-149">When there are multiple issues in Relevance training as well as issues after Batch calculation, the Catch-up process is performed once for all issues, and the results are calculated and displayed for each issue.</span></span>
    
> [!NOTE]
> <span data-ttu-id="06a8a-p112">Размер образца захват могут отличаться от указанных. Его зависит от размера нового нагрузки относительно предыдущей нагрузок и число образцов завершения перед добавлением нового нагрузки. Пример захват обычно представляют собой набор 200 до 2 000 файлов из нового нагрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p112">The size of the Catch-up sample may vary. It depends on the size of the new load relative to the previous loads, and on the number of samples completed before adding the new load. The Catch-up sample is typically a set of 200 to 2,000 files from the new load.</span></span> 
  
> [!TIP]
> <span data-ttu-id="06a8a-p113">Захват останавливает другие задачи и требует отдельного файла тегов и Повторение пройденного. Таким образом чтобы уменьшить дополнительную нагрузку при добавлении новых файлов в большие пакеты.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p113">Catch-up stops any other tasks and requires individual file tagging and review. Therefore, you can reduce overhead when you add new files in large batches.</span></span> 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a><span data-ttu-id="06a8a-155">Добавление нового файла нагрузки, с помощью связанной с подключением и динамическое загружает</span><span class="sxs-lookup"><span data-stu-id="06a8a-155">Adding a new file load using Catch-up and Rolling loads</span></span>

1. <span data-ttu-id="06a8a-156">В **релевантности \> установки релевантности** выберите **нагрузок**.</span><span class="sxs-lookup"><span data-stu-id="06a8a-156">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="06a8a-p114">В разделе **Управление нагрузок**, нажмите кнопку **+** значок, чтобы добавить загрузки. Отображается сообщение с подтверждением.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p114">Under **Loads management**, click the **+** icon to add a load. A confirmation message is displayed.</span></span> 
    
3. <span data-ttu-id="06a8a-p115">Нажмите кнопку **Да,** чтобы продолжить. Отображается диалоговое окно **Добавить загрузки** .</span><span class="sxs-lookup"><span data-stu-id="06a8a-p115">Click **Yes** to continue. The **Add new load** dialog is displayed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="06a8a-161">Новые нагрузки можно добавить только в том случае, если действия были выполнены предыдущие нагрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-161">You can only add a new load if actions were performed to the previous load.</span></span> 
  
4. <span data-ttu-id="06a8a-p116">В диалоговом окне **Добавить загрузки** введите сведения в **загрузить имя** и **Описание** , а затем нажмите кнопку **ОК**. Расширенные eDiscovery добавляет новый нагрузки.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p116">In the **Add new load** dialog, type information in **Load name** and **Description** and then click **OK**. Advanced eDiscovery adds a new load.</span></span>
    
5. <span data-ttu-id="06a8a-p117">Чтобы импортировать новые загрузить файл, щелкните **Добавить файлы**. Все файлы, которые добавляются к этой нагрузки. После расширенной eDiscovery импортирует файлы, распознает сценарий загружает последовательные и указывает захват в качестве следующего шага.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p117">To import the new load file, click **Add files**. All new files are added to this load. After Advanced eDiscovery imports the files, it recognizes the Rolling loads scenario and indicates Catch-up as the next step.</span></span>
    
6. <span data-ttu-id="06a8a-167">Щелкните **захват** в нижней части диалогового окна для запуска сценария.</span><span class="sxs-lookup"><span data-stu-id="06a8a-167">Click **Catch-up** at the bottom of the dialog to run the scenario.</span></span> 
    
    <span data-ttu-id="06a8a-168">Один набор захват, обычно с файлами 200 до 2000 из нового нагрузки создается для всех ошибок разрешить параллельных файл тегов.</span><span class="sxs-lookup"><span data-stu-id="06a8a-168">A single Catch-up set, typically containing 200 to 2,000 files from the new load, is created for all issues to allow concurrent file tagging.</span></span>
    
    <span data-ttu-id="06a8a-169">Сведения об о нагрузок, являются ли аналогичные или четкие, ли дополнительные eDiscovery объединенные или разбитые нагрузок автоматически и сведения о обработки на следующем этапе.</span><span class="sxs-lookup"><span data-stu-id="06a8a-169">Details are provided about whether loads are similar or distinct, whether Advanced eDiscovery merged or split the loads automatically, and information regarding processing in the next step.</span></span>
    
    <span data-ttu-id="06a8a-p118">Можно отметить файлы и выполнить операцию calculate. Теги позволяет релевантности для определения аналогичные или отдельных нагрузок и позволяет продолжить работу на новый набор файлов.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p118">You can then tag files and run a calculate operation. The tagging enables Relevance to determine if loads are similar or distinct and enables you to continue working on the new set of files.</span></span>
    
7. <span data-ttu-id="06a8a-172">После оценку set захват просмотреть **релевантности \> отслеживание** захват результатов.</span><span class="sxs-lookup"><span data-stu-id="06a8a-172">After the Catch-up set is reviewed, view **Relevance \> Track** for the Catch-up results.</span></span> 
    
1. <span data-ttu-id="06a8a-173">Если был добавлен новый файл нагрузки во время учебный курс по релевантности (то есть, проблема не еще не прошла расчет пакета), **продолжить обучение** является следующим шагом, независимо от того, захват результатов.</span><span class="sxs-lookup"><span data-stu-id="06a8a-173">If the new file load was added during Relevance training (meaning, the issue has not yet gone through Batch calculation), **Continue training** is the next step, regardless of the Catch-up results.</span></span> 
    
    <span data-ttu-id="06a8a-p119">Загружает новые и предыдущие обрабатываются как один нагрузки и учебный курс по релевантности продолжается на united set. Закончена с помощью этой процедуры и по-прежнему учебный курс по релевантности.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p119">The new and previous loads are processed as one load and Relevance training continues on the united set. You are now finished with this procedure and can continue Relevance training.</span></span> 
    
2. <span data-ttu-id="06a8a-176">Если новые нагрузки был добавлен после расчет пакета, перейти к следующие действия.</span><span class="sxs-lookup"><span data-stu-id="06a8a-176">If the new load was added after Batch calculation, proceed to the following steps.</span></span>
    
8. <span data-ttu-id="06a8a-177">Для нового загружается после расчет пакета расширенные обнаружения электронных данных определяет, если новые нагрузки аналогичную или отличались от предыдущей нагрузками, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="06a8a-177">For new loads added after Batch calculation, Advanced eDiscovery determines if the new load is similar to or distinct from previous loads, as follows:</span></span>
    
1. <span data-ttu-id="06a8a-p120">Если найдено аналогичные загружает: без дополнительного обучения релевантности не требуется. Панель мониторинга показаны рекомендуемые следующим шагом является запуск ** Batch вычислений ** еще раз, чтобы вычисление показателей релевантности для нового нагрузки. Загружает найдено как, поэтому предыдущей анализа классификатора может выполняться на новые файлы.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p120">If loads were found to be similar: No additional Relevance training is necessary. The dashboard shows the recommended next step is to run ** Batch calculation ** again to calculate Relevance scores for the new load. Loads were found to be similar, so the previous classifier analysis can be run on the new files.</span></span> 
    
2. <span data-ttu-id="06a8a-p121">Если загружает найдены отличаться: обучение более релевантности не требуется и следующим шагом является захват принятия решений. Выберите решение захват следующим образом:</span><span class="sxs-lookup"><span data-stu-id="06a8a-p121">If loads were found to be distinct: More Relevance training is necessary and the next step is Catch-up decision. Select a Catch-up decision as follows:</span></span>
    
    <span data-ttu-id="06a8a-p122">При выборе **Объединение нагрузок**, расширенные eDiscovery объединяет предыдущей и новой нагрузок для набора обучающих. Хотя для первой загрузки проходит расчет пакета, необходимые дополнительные обучающие материалы. Продолжайте обучение новых и предыдущих нагрузок их между собой. Расчет пакета будет запускаться еще раз и предыдущих показателям вычислений пакета следует игнорировать. Выберите этот параметр после показателям релевантности для существующего нагрузок может быть пересчета, например при review загружает существующий файл не запущен.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p122">If you select **Merge loads**, Advanced eDiscovery merges previous and new loads for the training set. Although the first load went through Batch calculation, more training is needed. Continue training new and previous loads together. Batch calculation will then run again and the previous Batch calculation scores should be ignored. Choose this selection when Relevance scores for existing loads can be recalculated, for example, when review of existing file loads has not started.</span></span>
    
    <span data-ttu-id="06a8a-p123">При выборе **загружает Split**продолжайте обучение релевантности только на новые нагрузки. В этом экземпляре предыдущей показателям вычислений Batch останется без изменений. Выберите этот параметр при существующих показателям релевантности для существующего нагрузок не удалось обновить, к примеру, если просмотр существующих загружает уже запущена. Показатели релевантности можно управлять отдельно с этого момента и не могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="06a8a-p123">If you select **Split loads**, continue Relevance training only on the new load. In this instance, previous Batch calculation scores will remain as is. Choose this option when existing Relevance scores for existing loads cannot be recalculated, for example, if review of existing loads has already started. Relevance scores are managed separately from this point onward and cannot be merged.</span></span>
    
3. <span data-ttu-id="06a8a-192">Нажмите кнопку **продолжить обучение**.</span><span class="sxs-lookup"><span data-stu-id="06a8a-192">Click **Continue training**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="06a8a-193">См. также</span><span class="sxs-lookup"><span data-stu-id="06a8a-193">See also</span></span>

[<span data-ttu-id="06a8a-194">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="06a8a-194">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="06a8a-195">Определение проблемы и назначение пользователей</span><span class="sxs-lookup"><span data-stu-id="06a8a-195">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="06a8a-196">Определение ключевых слов с выделением и дополнительные параметры</span><span class="sxs-lookup"><span data-stu-id="06a8a-196">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

