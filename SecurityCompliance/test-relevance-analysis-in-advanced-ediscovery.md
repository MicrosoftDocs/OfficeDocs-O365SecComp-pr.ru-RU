---
title: Проверка анализа релевантности в Office 365 Advanced eDiscovery
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Узнайте, как использовать вкладку тест после вычисления пакетов в Office 365 Advanced eDiscovery для тестирования, сравнения и проверки общего качества обработки.  '
ms.openlocfilehash: 735a6d8088b4696e2ebc348db435a11914bd0b10
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215839"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="d19f4-103">Проверка анализа релевантности в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d19f4-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="d19f4-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="d19f4-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="d19f4-p102">Вкладка тест в Advanced eDiscovery позволяет тестировать, сравнивать и проверять общее качество обработки. Эти тесты выполняются после пакетного вычисления. Размечая файлы в коллекции, эксперт делает последние сведения о том, действительно ли каждый из них имеет отношение к регистру.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p102">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing. These tests are performed after Batch calculation. By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="d19f4-p103">В сценариях с одним и несколькими проблемами тесты обычно выполняются для каждой проблемы. Результаты можно просматривать после каждого теста, а результаты тестирования можно переработать с указанным образцом тестовых файлов.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p103">In single and multiple-issue scenarios, tests are typically performed per issue. Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="d19f4-111">Тестирование REST</span><span class="sxs-lookup"><span data-stu-id="d19f4-111">Testing the rest</span></span>

<span data-ttu-id="d19f4-p104">Тест "тестирование REST" используется для проверки решений, связанных с отбором, например, для просмотра только файлов, относящихся к определенному показателю порогового значения релевантности, на основе итоговых дополнительных результатов обнаружения электронных данных. Эксперт просматривает пример файлов в выбранном показателе отсечки для оценки количества соответствующих файлов в этом наборе.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p104">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results. The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="d19f4-p105">В этом тесте предоставляется статистика и сравнивается набор проверки и проверяется заполнение REST. Результаты набора проверки рассчитываются по релевантности во время обучения. Результаты включают вычисления на основе параметров и входных параметров, таких как:</span><span class="sxs-lookup"><span data-stu-id="d19f4-p105">This test provides statistics and a comparison between the Review set and the Test the Rest population. The results of the review set are those calculated by Relevance during Training. The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="d19f4-117">ПроТестируйте пример статистики количества файлов в примере и определенных релевантных файлов.</span><span class="sxs-lookup"><span data-stu-id="d19f4-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="d19f4-p106">Табличное сравнение параметров заполнения для набора проверки и REST, например, количества файлов, оценочного количества релевантных файлов, оценки полноты и средней стоимости поиска дополнительного релевантного файла. Настройка параметров затрат может быть задана администратором.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p106">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file. Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="d19f4-120">Откройте вкладку **Проверка \> релевантности** .</span><span class="sxs-lookup"><span data-stu-id="d19f4-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="d19f4-p107">На вкладке **тест** нажмите кнопку **создать тест**. Откроется диалоговое окно **Создание теста** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p107">In the **Test** tab, click **New test**. The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Результаты теста "Тестирование остальных элементов" при определении релевантности](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="d19f4-124">В поле **имя теста**и **Описание**введите имя и описание.</span><span class="sxs-lookup"><span data-stu-id="d19f4-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="d19f4-125">В списке **тип теста** выберите пункт **Проверка оставшейся части**</span><span class="sxs-lookup"><span data-stu-id="d19f4-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="d19f4-126">В списке " **выдача и Категория** " выберите имя вопроса.</span><span class="sxs-lookup"><span data-stu-id="d19f4-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="d19f4-127">В списке **Загрузка** выберите Load (загрузить).</span><span class="sxs-lookup"><span data-stu-id="d19f4-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="d19f4-128">В разделе **Read% (чтение%**) примите значение по умолчанию или выберите значение для оценки релевантности.</span><span class="sxs-lookup"><span data-stu-id="d19f4-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="d19f4-p108">В поле **задать размер**или примите значение по умолчанию. Обратите внимание на то, что значки восстановления восстанавливают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p108">In **Set size**, or accept the default value. Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="d19f4-p109">Нажмите кнопку **начать маркировку**. Создается пример теста.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p109">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="d19f4-133">Просмотрите и пометьте все файлы на вкладке \*\* \> тег релевантности\*\* и по завершенИи нажмите кнопку вычислить. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d19f4-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="d19f4-p110">На вкладке тест можно щелкнуть **Просмотреть результаты** , чтобы просмотреть результаты теста. Пример показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p110">In the Test tab, you can click **View results** to see the test results. An example is shown in the following figure.</span></span> 
    
    ![Тестирование остальных элементов](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="d19f4-137">На приведенном выше рисунке в разделе **примеры параметров** таблицы содержатся сведения о количестве файлов в образце, помеченном экспертом, и количестве соответствующих файлов, найденных в этом примере.</span><span class="sxs-lookup"><span data-stu-id="d19f4-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="d19f4-p111">Раздел " **параметры заполнения** " таблицы содержит результаты тестирования, в том числе набор проверки заполнения файлов с оценкой ниже выбранной отсечки и "оставшиеся" файлы с оценкой, превышающим выбранную отсечение. Для каждого заполнения отображаются следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="d19f4-p111">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff. For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="d19f4-140">Включает файлы с пороговой прочтением%</span><span class="sxs-lookup"><span data-stu-id="d19f4-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="d19f4-141">Общее число файлов</span><span class="sxs-lookup"><span data-stu-id="d19f4-141">The total number of files</span></span> 
    
- <span data-ttu-id="d19f4-142">Предполагаемое количество релевантных файлов</span><span class="sxs-lookup"><span data-stu-id="d19f4-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="d19f4-143">Оценка возможностей</span><span class="sxs-lookup"><span data-stu-id="d19f4-143">The estimated richness</span></span> 
    
- <span data-ttu-id="d19f4-144">Средняя стоимость проверки поиска другого соответствующего файла</span><span class="sxs-lookup"><span data-stu-id="d19f4-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="d19f4-145">Тестирование фрагмента</span><span class="sxs-lookup"><span data-stu-id="d19f4-145">Testing the slice</span></span>

<span data-ttu-id="d19f4-146">Тест выполняет тестирование, аналогичный тесту "тестирование REST", но к сегменту набора файлов, указанному в релевантности Read%.</span><span class="sxs-lookup"><span data-stu-id="d19f4-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="d19f4-147">Откройте вкладку **Проверка \> релевантности** .</span><span class="sxs-lookup"><span data-stu-id="d19f4-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="d19f4-p112">На вкладке **тест** нажмите кнопку **создать тест**. Откроется диалоговое окно **Создание теста** .</span><span class="sxs-lookup"><span data-stu-id="d19f4-p112">In the **Test** tab, click **New test**. The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="d19f4-150">В поле имя и **Описание** **теста** введите данные.</span><span class="sxs-lookup"><span data-stu-id="d19f4-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="d19f4-151">В списке **тип теста** выберите пункт **Проверка среза**.</span><span class="sxs-lookup"><span data-stu-id="d19f4-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="d19f4-152">В списке " **Ошибка** " выберите имя вопроса.</span><span class="sxs-lookup"><span data-stu-id="d19f4-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="d19f4-153">В списке **Загрузка** выберите Load (загрузить).</span><span class="sxs-lookup"><span data-stu-id="d19f4-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="d19f4-154">В разделе **Чтение% между**примите значения по умолчанию: минимальное и большое значения диапазона или выберите значения для показателей релевантности.</span><span class="sxs-lookup"><span data-stu-id="d19f4-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="d19f4-155">В поле Выбор **размера**выберите значение или примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d19f4-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="d19f4-156">Значки восстановления восстанавливают значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d19f4-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="d19f4-p113">Нажмите кнопку **начать маркировку**. Создается пример теста.</span><span class="sxs-lookup"><span data-stu-id="d19f4-p113">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="d19f4-159">Просмотрите и пометьте все файлы на вкладке \*\* \> тег релевантности\*\* и по завершенИи нажмите кнопку вычислить. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d19f4-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="d19f4-160">На вкладке тест можно щелкнуть **Просмотреть результаты** , чтобы просмотреть результаты теста.</span><span class="sxs-lookup"><span data-stu-id="d19f4-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d19f4-161">См. также</span><span class="sxs-lookup"><span data-stu-id="d19f4-161">See also</span></span>

[<span data-ttu-id="d19f4-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d19f4-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="d19f4-163">Понимание оценки релевантности</span><span class="sxs-lookup"><span data-stu-id="d19f4-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d19f4-164">Маркировка и оценка</span><span class="sxs-lookup"><span data-stu-id="d19f4-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d19f4-165">РасСтановка тегов и релевантности</span><span class="sxs-lookup"><span data-stu-id="d19f4-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d19f4-166">Анализ релевантности отслеживания</span><span class="sxs-lookup"><span data-stu-id="d19f4-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d19f4-167">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="d19f4-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

