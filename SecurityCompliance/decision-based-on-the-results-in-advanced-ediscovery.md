---
title: Решение на основе результатов в Office 365 Advanced eDiscovery
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
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Узнайте, как определить вкладки в Office 365 Advanced электронного обнаружения включает сведения о данных, которые помогут вам определить правильное размер review набор вариантов файлов. '
ms.openlocfilehash: 58a181e00ad5843ccbbde4dcb47050eccf199225
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534562"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="ee36e-103">Решение на основе результатов в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ee36e-103">Decision based on the results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="ee36e-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="ee36e-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="ee36e-106">В расширенной eDiscovery на вкладке определить дополнительные сведения для просмотра и использования поддержки решений статистику по определению размера набора Обзор вариантов файлов.</span><span class="sxs-lookup"><span data-stu-id="ee36e-106">In Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span> 
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="ee36e-107">С помощью определения вкладки</span><span class="sxs-lookup"><span data-stu-id="ee36e-107">Using the Decide tab</span></span>

!["Релевантность" > "Решение"](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="ee36e-109">На этой вкладке включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="ee36e-109">This tab includes the following:</span></span>
  
- <span data-ttu-id="ee36e-110">**Проблема**: Здесь можно выбрать проблему процент из списка.</span><span class="sxs-lookup"><span data-stu-id="ee36e-110">**Issue**: From here, you can select the issue of interest from the list.</span></span> 
    
- <span data-ttu-id="ee36e-p102">**Соотношение проверки отзыва**: сравнение Расширенный обзор обнаружения электронных данных по степени соответствия. Точка сканирования на диаграмме представляет собой процентную долю файлы для просмотра, сопоставленные с показатель релевантности. Используется на этапе тестирования релевантности и как экспорта пороговое значение для отбора. В точке, в которой баланс между точности и эффективности поиска является оптимальным — точку максимально допустимое значение по умолчанию, число файлов для просмотра. Фактические прекращения точки должны определяться пользователя в зависимости от целей и стоимость компромисс (% ознакомления) и риска (% отзыва). С помощью ползунок, можно настроить ограничения точка и увидеть влияние на графике и параметры, при настройке % соответствующие файлы нужно вернуть и перед проверкой решение.</span><span class="sxs-lookup"><span data-stu-id="ee36e-p102">**Review-recall ratio**: Comparison of Advanced eDiscovery review according to Relevance scores. The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score. This is used in the Relevance Test phase and as an Export threshold for culling. The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal. The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>
    
- <span data-ttu-id="ee36e-p103">**Параметры**: просмотрите, помните, что параметры следующей соответствующих и общая стоимость являются накопительных статистику, относящиеся к просмотру, задайте по отношению к коллекции для всего примера. Определений для этих параметров, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="ee36e-p103">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case. Definitions for these parameters are as follows:</span></span>
    
    <span data-ttu-id="ee36e-118">**Просмотрите**: процент файлы для просмотра на основании этого сканирования.</span><span class="sxs-lookup"><span data-stu-id="ee36e-118">**Review**: Percentage of files to review based on this cutoff.</span></span> 
    
    <span data-ttu-id="ee36e-119">**Отзыв**: процент соответствующие файлы в наборе проверки.</span><span class="sxs-lookup"><span data-stu-id="ee36e-119">**Recall**: Percentage of relevant files in the review set.</span></span> 
    
    <span data-ttu-id="ee36e-120">**Далее соответствующих**: расходов на просмотр и определение соответствующего файла, который в данный момент в просмотре установлено.</span><span class="sxs-lookup"><span data-stu-id="ee36e-120">**Next relevant**: Cost to review and identify an additional relevant file that is not currently in the review set.</span></span> 
    
    <span data-ttu-id="ee36e-p104">**Общие расходы**: затраты на рецензирование этот процент вариантов файлы. Затратные значений параметров можно задать руководителем вариантов.</span><span class="sxs-lookup"><span data-stu-id="ee36e-p104">**Total cost**: Cost for reviewing this percentage of the case files. Cost parameter settings can be set by the Case manager.</span></span>
    
- <span data-ttu-id="ee36e-p105">**Распределение по релевантности показателю**: файлы темный экран серый слева, ниже ограничения оценки. Подсказки отображает показатель релевантности и связанных с ними процент файлы в файле проверки, задайте по отношению к всего файлов.</span><span class="sxs-lookup"><span data-stu-id="ee36e-p105">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
<span data-ttu-id="ee36e-p106">Расширенная область сведений отображает дополнительные сведения. Файлы в коллекции фигур исключение пустой или nebulous файлов. Семьи файлы рисунков представляют файлы, которые являются не загружается в релевантности, но по-прежнему учитываются как часть семейства.</span><span class="sxs-lookup"><span data-stu-id="ee36e-p106">The expanded Details pane displays additional details. Files in collection figures do not include empty or nebulous files. Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee36e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ee36e-128">See also</span></span>

[<span data-ttu-id="ee36e-129">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ee36e-129">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ee36e-130">Общие сведения об оценке в релевантности</span><span class="sxs-lookup"><span data-stu-id="ee36e-130">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ee36e-131">Теги и оценки</span><span class="sxs-lookup"><span data-stu-id="ee36e-131">Tagging and Assessment</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ee36e-132">Учебный курс по релевантности для выполнения</span><span class="sxs-lookup"><span data-stu-id="ee36e-132">Performing Relevance training</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ee36e-133">Отслеживание анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="ee36e-133">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ee36e-134">Тестирование анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="ee36e-134">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

