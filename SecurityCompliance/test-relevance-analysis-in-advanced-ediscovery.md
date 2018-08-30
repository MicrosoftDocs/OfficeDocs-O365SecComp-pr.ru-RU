---
title: Проверка анализа релевантности в Office 365 Advanced eDiscovery
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Сведения об использовании вкладке тест после пакета вычислений в Office 365 расширенного обнаружения электронных данных для тестирования, сравнения и проверки общее качество обработки.  '
ms.openlocfilehash: 782859fe3b6bb3d00945c477928131cd1154446d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534866"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="07b16-103">Проверка анализа релевантности в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="07b16-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="07b16-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="07b16-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="07b16-p102">Вкладке теста в расширенной обнаружения электронных данных позволяет проверить, сравнения и проверки общее качество обработки. Эти тесты выполняются после расчета пакета. Теги файлов в коллекции, эксперт делает принятие окончательного решения о ли каждый файл с тегами уместно, фактически в рамках данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="07b16-p102">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing. These tests are performed after Batch calculation. By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="07b16-p103">В сценарии одной и несколькими проблему тесты обычно выполняются на проблему. Результаты можно просмотреть после каждого теста и результаты теста можно доработаны с указанного примеры тестирования файлов.</span><span class="sxs-lookup"><span data-stu-id="07b16-p103">In single and multiple-issue scenarios, tests are typically performed per issue. Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="07b16-111">Тестирование rest</span><span class="sxs-lookup"><span data-stu-id="07b16-111">Testing the rest</span></span>

<span data-ttu-id="07b16-p104">Тест «Тестирование Rest» используется для проверки исключения решения, например, чтобы просмотреть только файлы выше определенного показателя прекращения релевантности, на основе результатов окончательный расширенной обнаружения электронных данных. Эксперт дается обзор пример файлов в разделе выбранного прекращения показатель, чтобы оценить количество соответствующие файлы в этот набор.</span><span class="sxs-lookup"><span data-stu-id="07b16-p104">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results. The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="07b16-p105">Этот тест предоставляет статистику и сравнение set проверки и тестирования совокупности Rest. Результаты проверки набор — это списки вычисляется по релевантности во время обучения. Результаты содержат вычисления, на основе параметров и входные параметры, такие как:</span><span class="sxs-lookup"><span data-stu-id="07b16-p105">This test provides statistics and a comparison between the Review set and the Test the Rest population. The results of the review set are those calculated by Relevance during Training. The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="07b16-117">Проверить образец статистики числа файлов в образец и определенного необходимые файлы.</span><span class="sxs-lookup"><span data-stu-id="07b16-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="07b16-p106">Табличные сравнение параметров заполнения набора проверки и Rest, например, число файлов, предполагаемое количество соответствующие файлы, примерный набора операторов и средние затраты на поиск соответствующего файла. Затратные значений параметров можно задать администратором.</span><span class="sxs-lookup"><span data-stu-id="07b16-p106">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file. Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="07b16-120">Открыть **релевантности \> тестирования** вкладки.</span><span class="sxs-lookup"><span data-stu-id="07b16-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="07b16-p107">Вкладка **тестирования** нажмите кнопку **Создать тест**. Откроется диалоговое окно **Создать тестовый** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="07b16-p107">In the **Test** tab, click **New test**. The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Результаты теста "Тестирование остальных элементов" при определении релевантности](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="07b16-124">В **тестовых имя**и **Описание**введите имя и описание.</span><span class="sxs-lookup"><span data-stu-id="07b16-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="07b16-125">В списке **Тип теста** выберите **Тест Rest**</span><span class="sxs-lookup"><span data-stu-id="07b16-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="07b16-126">В **проблема или категории** выберите имя проблему.</span><span class="sxs-lookup"><span data-stu-id="07b16-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="07b16-127">В списке **загрузки** выберите нагрузки.</span><span class="sxs-lookup"><span data-stu-id="07b16-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="07b16-128">**% Чтение**примите значение по умолчанию, или выберите значение для прекращения показатель релевантности.</span><span class="sxs-lookup"><span data-stu-id="07b16-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="07b16-p108">В **размер**или оставьте значение по умолчанию. Обратите внимание на то, что значки восстановления будет восстановить значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07b16-p108">In **Set size**, or accept the default value. Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="07b16-p109">Нажмите кнопку **Пуск тегов**. Создается тестового примера.</span><span class="sxs-lookup"><span data-stu-id="07b16-p109">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="07b16-133">Просмотрите и всех файлов в тег **релевантности \> тега** вкладок и по завершении нажмите кнопку **Calculate**.</span><span class="sxs-lookup"><span data-stu-id="07b16-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="07b16-p110">На вкладке тест можно щелкните **Просмотр результатов** , чтобы увидеть результаты тестирования. На следующем рисунке показан пример.</span><span class="sxs-lookup"><span data-stu-id="07b16-p110">In the Test tab, you can click **View results** to see the test results. An example is shown in the following figure.</span></span> 
    
    ![Тестирование остальных элементов](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="07b16-137">На рисунке выше раздел **Параметры образец** таблицы содержит сведения о число файлов в образце с меткой, эксперт и количество соответствующих файлов, обнаруженных в этом примере.</span><span class="sxs-lookup"><span data-stu-id="07b16-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="07b16-p111">Раздел **Параметры заполнение** таблицы содержит результаты тестирования, включая заполнение набора проверки файлов с индексом ниже выбранного сканирования и заполнение «Rest» файлы с индексом выше выбранного сканирования. Для каждого совокупности отображаются следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="07b16-p111">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff. For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="07b16-140">Включает файлы с чтения % - сказано сканирования</span><span class="sxs-lookup"><span data-stu-id="07b16-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="07b16-141">Общее число файлов</span><span class="sxs-lookup"><span data-stu-id="07b16-141">The total number of files</span></span> 
    
- <span data-ttu-id="07b16-142">Ожидаемое число соответствующих файлов</span><span class="sxs-lookup"><span data-stu-id="07b16-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="07b16-143">Оценка набора операторов</span><span class="sxs-lookup"><span data-stu-id="07b16-143">The estimated richness</span></span> 
    
- <span data-ttu-id="07b16-144">Среднее значение review затраты на поиск другого соответствующего файла</span><span class="sxs-lookup"><span data-stu-id="07b16-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="07b16-145">Тестирование фрагмента</span><span class="sxs-lookup"><span data-stu-id="07b16-145">Testing the slice</span></span>

<span data-ttu-id="07b16-146">«Тестирование срез» test выполняет тестирование аналогичен «Тестирование Rest» тестирование, но с сегментом файла указанного значения на % чтение релевантности.</span><span class="sxs-lookup"><span data-stu-id="07b16-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="07b16-147">Открыть **релевантности \> тестирования** вкладки.</span><span class="sxs-lookup"><span data-stu-id="07b16-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="07b16-p112">Вкладка **тестирования** нажмите кнопку **Создать тест**. Отображается диалоговое окно **Создать тестовый** .</span><span class="sxs-lookup"><span data-stu-id="07b16-p112">In the **Test** tab, click **New test**. The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="07b16-150">В **тестовых имя** и **Описание**введите сведения.</span><span class="sxs-lookup"><span data-stu-id="07b16-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="07b16-151">В списке **Тип теста** выберите **Тест фрагмент**.</span><span class="sxs-lookup"><span data-stu-id="07b16-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="07b16-152">В список **вопросов** выберите имя проблему.</span><span class="sxs-lookup"><span data-stu-id="07b16-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="07b16-153">В списке **загрузки** выберите нагрузки.</span><span class="sxs-lookup"><span data-stu-id="07b16-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="07b16-154">В **% Чтение между**примите значения по умолчанию высокой и низкой диапазон или выберите значения для прекращения показателям релевантности.</span><span class="sxs-lookup"><span data-stu-id="07b16-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="07b16-155">В **задать размер**выберите значение или примите значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07b16-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="07b16-156">Значки восстановления будет восстановить значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07b16-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="07b16-p113">Нажмите кнопку **Пуск тегов**. Создается тестового примера.</span><span class="sxs-lookup"><span data-stu-id="07b16-p113">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="07b16-159">Просмотрите и всех файлов в тег **релевантности \> тега** вкладок и по завершении нажмите кнопку **Calculate**.</span><span class="sxs-lookup"><span data-stu-id="07b16-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="07b16-160">На вкладке тест можно щелкните **Просмотр результатов** , чтобы увидеть результаты тестирования.</span><span class="sxs-lookup"><span data-stu-id="07b16-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="07b16-161">См. также</span><span class="sxs-lookup"><span data-stu-id="07b16-161">See also</span></span>

[<span data-ttu-id="07b16-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="07b16-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="07b16-163">Общие сведения об оценке в релевантности</span><span class="sxs-lookup"><span data-stu-id="07b16-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="07b16-164">Теги и оценки</span><span class="sxs-lookup"><span data-stu-id="07b16-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="07b16-165">Теги и учебный курс по релевантности</span><span class="sxs-lookup"><span data-stu-id="07b16-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="07b16-166">Отслеживание анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="07b16-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="07b16-167">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="07b16-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

