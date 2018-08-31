---
title: Сведения об оценке в модуле релевантности в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: 'Узнайте о стадии оценки и ее роль в определение набора ошибок во время учебный курс по релевантности в Office 365 расширенного обнаружения электронных данных.  '
ms.openlocfilehash: a54a4134609b16568586f3cb6b60ebdeba860bac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534857"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a><span data-ttu-id="58e5c-103">Сведения об оценке в модуле релевантности в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="58e5c-103">Understand Assessment in Relevance in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="58e5c-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="58e5c-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="58e5c-p102">Расширенные обнаружения электронных данных, как включить первых оценки, например для определенные проблемы и данные, импортированные для обращения. Расширенные eDiscovery позволяет expert для принятия решений, относящихся к принятый подход и применить их в проект проверки документа.</span><span class="sxs-lookup"><span data-stu-id="58e5c-p102">Advanced eDiscovery enables early assessment, for example, for the defined issues and the data imported for a case. Advanced eDiscovery enables the expert to make decisions pertaining to an adopted approach and to apply them to the document review project.</span></span>
  
## <a name="understanding-assessment"></a><span data-ttu-id="58e5c-108">Общее представление о оценки</span><span class="sxs-lookup"><span data-stu-id="58e5c-108">Understanding assessment</span></span>

<span data-ttu-id="58e5c-p103">В оценки эксперт дается обзор случайный набор по крайней мере 500 файлы, которые используются для определения набора проблем и для получения статистика, которая отражает результаты обучения. Оценка успешно обнаружении достаточно необходимые файлы для достижения статистические уровня, с помощью расширенных eDiscovery релевантности для обеспечения точной статистики и эффективно определить точку стабилизацией в процесс обучения.</span><span class="sxs-lookup"><span data-stu-id="58e5c-p103">In Assessment, the expert reviews a random set of at least 500 files, which are used to determine the richness of the issues and to produce statistics that reflect the training results. Assessment is successful when enough relevant files are found to reach a statistical level that will help Advanced eDiscovery Relevance to provide accurate statistics and to effectively determine the stabilization point in the training process.</span></span> 
  
<span data-ttu-id="58e5c-p104">Чем больше число соответствующие файлы в наборе оценки, более правильным Статистика и эффективность алгоритм стабильность. Число соответствующие файлы в файлах оценки зависит от полноты проблемы. Расширение является предполагаемый процент соответствующие файлы в наборе, относящиеся к проблеме. Проблемы, связанные с выше расширение будет связи с чем больше число соответствующие файлы быстрее, чем проблемы с нижней набора операторов. Проблемы, связанные с очень низкой расширение (например, % 2 или меньше) потребует очень большой оценки, задайте для доступа к значительному количеству необходимые файлы.</span><span class="sxs-lookup"><span data-stu-id="58e5c-p104">The higher the number of relevant files in the assessment set, the more accurate the statistics and the effectiveness of the stability algorithm. The number of relevant files within the assessment files depends on the richness of the issue. Richness is the estimated percent of relevant files in the set relevant to an issue. Issues with higher richness will reach a higher number of relevant files more quickly than issues with lower richness. Issues with extremely low richness (for example, 2% or less) will require a very large assessment set to reach a significant number of Relevant files.</span></span>
  
<span data-ttu-id="58e5c-p105">Статистика, указанные на вкладках отслеживание и определить во время обучения и после расчет пакета, включает оценок отзыва для проверки различных наборов. В статистические данные оценки, основанных на примере задайте (в данном случае файлы оценки) включают в себя поля ошибки и уровень вероятности, ошибка поля. К примеру примерный отзыва 80% может иметь поля ошибки плюс-минус 5% с уровень вероятности 95%. Это означает, что примерно отзыва фактически 75% - 85% и эта оценка имеет 95% вероятности. Большого набора оценки, уменьшается поля ошибки и статистики являются более правильным.</span><span class="sxs-lookup"><span data-stu-id="58e5c-p105">The statistics, which are presented in the Track and Decide tabs during training and after Batch calculation, include estimations of recall for different review sets. In statistics, estimations that are based on a sample set (in this case, the assessment files) include the margin of error and the confidence level of that error margin. For example, estimated recall of 80% might have a margin of error of plus or minus 5% with a confidence level of 95%. This means that the estimated recall is actually 75%-85% and this estimation has 95% confidence. The larger the assessment set, the margin of error becomes smaller and the statistics are more accurate.</span></span> 
  
<span data-ttu-id="58e5c-p106">После опытный пользователь просматривает набор начальной оценки 500 файлов, релевантности для определения текущего поля ошибки значений отзыва. Релевантность будет также необходимо задать поля по умолчанию ошибки, в котором он рекомендуется сделать доступными для оптимизации set оценки. Ниже приведены некоторые примеры:</span><span class="sxs-lookup"><span data-stu-id="58e5c-p106">After the expert reviews an initial assessment set of 500 files, Relevance is able to determine the current margin of error of the recall values. Relevance will also set a default margin of error that it recommends to reach to optimize the assessment set. Following are some examples:</span></span>
  
- <span data-ttu-id="58e5c-124">Если оценки, уже настроено появилось поля ошибки плюс-минус 10%, релевантности будет рекомендуется для перемещения обучение (без проверки дополнительные оценки необходима).</span><span class="sxs-lookup"><span data-stu-id="58e5c-124">If the assessment set already yielded a margin of error of plus or minus 10%, Relevance will recommend to move on to training (no additional assessment review is needed).</span></span> 
    
- <span data-ttu-id="58e5c-125">Если набор оценки появилось поля ошибки плюс-минус 13%, релевантности может порекомендовать review другой набор файлов оценки для достижения меньшего размера поля.</span><span class="sxs-lookup"><span data-stu-id="58e5c-125">If the assessment set yielded a margin of error of plus or minus 13%, Relevance might recommend the review of another set of assessment files to reach a smaller margin.</span></span> 
    
- <span data-ttu-id="58e5c-126">Если расширение является очень низкий, релевантности может порекомендовать остановка оценки, несмотря на то, что поля ошибки больших (отображение статистики нецелесообразным), так как набор оценки необходимое для достижения полезные поля ошибки слишком велик.</span><span class="sxs-lookup"><span data-stu-id="58e5c-126">If richness is extremely low, Relevance might recommend stopping assessment even though the margin of error is large (making statistics impractical), because the assessment set needed to reach a useful margin of error is too large.</span></span>
    
<span data-ttu-id="58e5c-p107">Каждая проблема имеет свой собственный набор операторов, текущего поля ошибки и в результате предполагаемое количество файлов дополнительные оценки. Следующий набор оценки создается в соответствии с максимальное количество файлов (до 1000 в один набор).</span><span class="sxs-lookup"><span data-stu-id="58e5c-p107">Each issue has its own richness, current margin of error, and as a result, estimated number of additional assessment files. The next assessment set is created according to the maximum number of files (up to 1,000 in a single set).</span></span>
  
<span data-ttu-id="58e5c-p108">Можно принять рекомендации по релевантности или настроить текущего поля ошибки по мере необходимости. Текущий погрешность по умолчанию определяется для отзыва, равно или превышает 75%.</span><span class="sxs-lookup"><span data-stu-id="58e5c-p108">You can accept the Relevance recommendations or adjust the current margin of error according to your needs. The default current margin of error is determined for recall at equal or above 75%.</span></span>
  
> [!NOTE]
> <span data-ttu-id="58e5c-p109">Этап оценки можно обойти, в **релевантности \> отслеживание** на вкладке подробный проблемы, сняв флажок **оценки** на проблему, а затем проблем «все». Тем не менее в результате будет Нет статистики для этой проблемы. > Если снять флажок **оценки** может быть выполнено только до выполнения оценки. Если существует несколько проблем в случае, оценка будет выполняться обход только в том случае, если флажок установлен для каждой проблемы</span><span class="sxs-lookup"><span data-stu-id="58e5c-p109">The Assessment stage can be bypassed, in the **Relevance \> Track** tab in the expanded view for an issue, by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="58e5c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="58e5c-135">See also</span></span>

[<span data-ttu-id="58e5c-136">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="58e5c-136">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="58e5c-137">Теги и оценки</span><span class="sxs-lookup"><span data-stu-id="58e5c-137">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="58e5c-138">Теги и учебный курс по релевантности</span><span class="sxs-lookup"><span data-stu-id="58e5c-138">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="58e5c-139">Отслеживание анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="58e5c-139">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="58e5c-140">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="58e5c-140">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="58e5c-141">Тестирование анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="58e5c-141">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

