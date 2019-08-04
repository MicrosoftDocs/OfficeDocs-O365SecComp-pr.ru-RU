---
title: Анализ релевантности тестирования в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 09/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Узнайте, как использовать вкладку тест после вычисления пакетов в Office 365 Advanced eDiscovery для тестирования, сравнения и проверки общего качества обработки.  '
ms.openlocfilehash: 7d150b9f68cdcd3246fbd4d8f79e0972a81a4703
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35601396"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="19c29-103">Анализ релевантности тестирования в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="19c29-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="19c29-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="19c29-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="19c29-106">Вкладка тест в Advanced eDiscovery позволяет тестировать, сравнивать и проверять общее качество обработки.</span><span class="sxs-lookup"><span data-stu-id="19c29-106">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing.</span></span> <span data-ttu-id="19c29-107">Эти тесты выполняются после пакетного вычисления.</span><span class="sxs-lookup"><span data-stu-id="19c29-107">These tests are performed after Batch calculation.</span></span> <span data-ttu-id="19c29-108">Размечая файлы в коллекции, эксперт делает последние сведения о том, действительно ли каждый из них имеет отношение к регистру.</span><span class="sxs-lookup"><span data-stu-id="19c29-108">By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="19c29-109">В сценариях с одним и несколькими проблемами тесты обычно выполняются для каждой проблемы.</span><span class="sxs-lookup"><span data-stu-id="19c29-109">In single and multiple-issue scenarios, tests are typically performed per issue.</span></span> <span data-ttu-id="19c29-110">Результаты можно просматривать после каждого теста, а результаты тестирования можно переработать с указанным образцом тестовых файлов.</span><span class="sxs-lookup"><span data-stu-id="19c29-110">Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="19c29-111">Тестирование REST</span><span class="sxs-lookup"><span data-stu-id="19c29-111">Testing the rest</span></span>

<span data-ttu-id="19c29-112">Тест "тестирование REST" используется для проверки решений, связанных с отбором, например, для просмотра только файлов, относящихся к определенному показателю порогового значения релевантности, на основе итоговых дополнительных результатов обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="19c29-112">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results.</span></span> <span data-ttu-id="19c29-113">Эксперт просматривает пример файлов в выбранном показателе отсечки для оценки количества соответствующих файлов в этом наборе.</span><span class="sxs-lookup"><span data-stu-id="19c29-113">The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="19c29-114">В этом тесте предоставляется статистика и сравнивается набор проверки и проверяется заполнение REST.</span><span class="sxs-lookup"><span data-stu-id="19c29-114">This test provides statistics and a comparison between the Review set and the Test the Rest population.</span></span> <span data-ttu-id="19c29-115">Результаты набора проверки рассчитываются по релевантности во время обучения.</span><span class="sxs-lookup"><span data-stu-id="19c29-115">The results of the review set are those calculated by Relevance during Training.</span></span> <span data-ttu-id="19c29-116">Результаты включают вычисления на основе параметров и входных параметров, таких как:</span><span class="sxs-lookup"><span data-stu-id="19c29-116">The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="19c29-117">Протестируйте пример статистики количества файлов в примере и определенных релевантных файлов.</span><span class="sxs-lookup"><span data-stu-id="19c29-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="19c29-118">Табличное сравнение параметров заполнения для набора проверки и REST, например, количества файлов, оценочного количества релевантных файлов, оценки полноты и средней стоимости поиска дополнительного релевантного файла.</span><span class="sxs-lookup"><span data-stu-id="19c29-118">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file.</span></span> <span data-ttu-id="19c29-119">Настройка параметров затрат может быть задана администратором.</span><span class="sxs-lookup"><span data-stu-id="19c29-119">Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="19c29-120">Откройте вкладку **Проверка \> релевантности** .</span><span class="sxs-lookup"><span data-stu-id="19c29-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="19c29-121">На вкладке **тест** нажмите кнопку **создать тест**.</span><span class="sxs-lookup"><span data-stu-id="19c29-121">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="19c29-122">Откроется диалоговое окно **Создание теста** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="19c29-122">The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Результаты теста "Тестирование остальных элементов" при определении релевантности](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="19c29-124">В поле **имя теста**и **Описание**введите имя и описание.</span><span class="sxs-lookup"><span data-stu-id="19c29-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="19c29-125">В списке **тип теста** выберите пункт **Проверка оставшейся части**</span><span class="sxs-lookup"><span data-stu-id="19c29-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="19c29-126">В списке " **выдача и Категория** " выберите имя вопроса.</span><span class="sxs-lookup"><span data-stu-id="19c29-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="19c29-127">В списке **Загрузка** выберите Load (загрузить).</span><span class="sxs-lookup"><span data-stu-id="19c29-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="19c29-128">В разделе **Read% (чтение%**) примите значение по умолчанию или выберите значение для оценки релевантности.</span><span class="sxs-lookup"><span data-stu-id="19c29-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="19c29-129">В поле **задать размер**или примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19c29-129">In **Set size**, or accept the default value.</span></span> <span data-ttu-id="19c29-130">Обратите внимание на то, что значки восстановления восстанавливают значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19c29-130">Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="19c29-131">Нажмите кнопку **начать маркировку**.</span><span class="sxs-lookup"><span data-stu-id="19c29-131">Click **Start tagging**.</span></span> <span data-ttu-id="19c29-132">Создается пример теста.</span><span class="sxs-lookup"><span data-stu-id="19c29-132">A test sample is generated.</span></span>
    
10. <span data-ttu-id="19c29-133">Просмотрите и пометьте все файлы на вкладке \*\* \> тег релевантности\*\* и по завершении нажмите кнопку вычислить. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="19c29-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="19c29-134">На вкладке тест можно щелкнуть **Просмотреть результаты** , чтобы просмотреть результаты теста.</span><span class="sxs-lookup"><span data-stu-id="19c29-134">In the Test tab, you can click **View results** to see the test results.</span></span> <span data-ttu-id="19c29-135">Пример показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="19c29-135">An example is shown in the following figure.</span></span> 
    
    ![Тестирование остальных элементов](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="19c29-137">На приведенном выше рисунке в разделе **примеры параметров** таблицы содержатся сведения о количестве файлов в образце, помеченном экспертом, и количестве соответствующих файлов, найденных в этом примере.</span><span class="sxs-lookup"><span data-stu-id="19c29-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="19c29-138">Раздел " **параметры заполнения** " таблицы содержит результаты тестирования, в том числе набор проверки заполнения файлов с оценкой ниже выбранной отсечки и "оставшиеся" файлы с оценкой, превышающим выбранную отсечение.</span><span class="sxs-lookup"><span data-stu-id="19c29-138">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff.</span></span> <span data-ttu-id="19c29-139">Для каждого заполнения отображаются следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="19c29-139">For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="19c29-140">Включает файлы с пороговой прочтением%</span><span class="sxs-lookup"><span data-stu-id="19c29-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="19c29-141">Общее число файлов</span><span class="sxs-lookup"><span data-stu-id="19c29-141">The total number of files</span></span> 
    
- <span data-ttu-id="19c29-142">Предполагаемое количество релевантных файлов</span><span class="sxs-lookup"><span data-stu-id="19c29-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="19c29-143">Оценка возможностей</span><span class="sxs-lookup"><span data-stu-id="19c29-143">The estimated richness</span></span> 
    
- <span data-ttu-id="19c29-144">Средняя стоимость проверки поиска другого соответствующего файла</span><span class="sxs-lookup"><span data-stu-id="19c29-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="19c29-145">Тестирование фрагмента</span><span class="sxs-lookup"><span data-stu-id="19c29-145">Testing the slice</span></span>

<span data-ttu-id="19c29-146">Тест выполняет тестирование, аналогичный тесту "тестирование REST", но к сегменту набора файлов, указанному в релевантности Read%.</span><span class="sxs-lookup"><span data-stu-id="19c29-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="19c29-147">Откройте вкладку **Проверка \> релевантности** .</span><span class="sxs-lookup"><span data-stu-id="19c29-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="19c29-148">На вкладке **тест** нажмите кнопку **создать тест**.</span><span class="sxs-lookup"><span data-stu-id="19c29-148">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="19c29-149">Откроется диалоговое окно **Создание теста** .</span><span class="sxs-lookup"><span data-stu-id="19c29-149">The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="19c29-150">В поле имя и **Описание** **теста** введите данные.</span><span class="sxs-lookup"><span data-stu-id="19c29-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="19c29-151">В списке **тип теста** выберите пункт **Проверка среза**.</span><span class="sxs-lookup"><span data-stu-id="19c29-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="19c29-152">В списке " **Ошибка** " выберите имя вопроса.</span><span class="sxs-lookup"><span data-stu-id="19c29-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="19c29-153">В списке **Загрузка** выберите Load (загрузить).</span><span class="sxs-lookup"><span data-stu-id="19c29-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="19c29-154">В разделе **Чтение% между**примите значения по умолчанию: минимальное и большое значения диапазона или выберите значения для показателей релевантности.</span><span class="sxs-lookup"><span data-stu-id="19c29-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="19c29-155">В поле Выбор **размера**выберите значение или примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19c29-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="19c29-156">Значки восстановления восстанавливают значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19c29-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="19c29-157">Нажмите кнопку **начать маркировку**.</span><span class="sxs-lookup"><span data-stu-id="19c29-157">Click **Start tagging**.</span></span> <span data-ttu-id="19c29-158">Создается пример теста.</span><span class="sxs-lookup"><span data-stu-id="19c29-158">A test sample is generated.</span></span>
    
10. <span data-ttu-id="19c29-159">Просмотрите и пометьте все файлы на вкладке \*\* \> тег релевантности\*\* и по завершении нажмите кнопку вычислить. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="19c29-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="19c29-160">На вкладке тест можно щелкнуть **Просмотреть результаты** , чтобы просмотреть результаты теста.</span><span class="sxs-lookup"><span data-stu-id="19c29-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="19c29-161">См. также</span><span class="sxs-lookup"><span data-stu-id="19c29-161">See also</span></span>

[<span data-ttu-id="19c29-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="19c29-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="19c29-163">Понимание оценки релевантности</span><span class="sxs-lookup"><span data-stu-id="19c29-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="19c29-164">Маркировка и оценка</span><span class="sxs-lookup"><span data-stu-id="19c29-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="19c29-165">Расстановка тегов и релевантности</span><span class="sxs-lookup"><span data-stu-id="19c29-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="19c29-166">Анализ релевантности отслеживания</span><span class="sxs-lookup"><span data-stu-id="19c29-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="19c29-167">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="19c29-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

