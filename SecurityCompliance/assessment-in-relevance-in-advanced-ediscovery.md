---
title: Сведения об оценке в модуле релевантности в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: Ознакомьтесь с обзором этапа оценки и его роли в определении богатости проблем во время обучения по релевантности в Office 365 Advanced eDiscovery.
ms.openlocfilehash: 1ddaa7ef37f762d7b63bb6c0c51193ff382b8d6b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212979"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a><span data-ttu-id="55fbb-103">Сведения об оценке в модуле релевантности в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="55fbb-103">Understand Assessment in Relevance in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="55fbb-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="55fbb-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="55fbb-p102">Расширенные функции обнаружения электронных данных обеспечивают более раннюю оценку, например, для определенных проблем и данных, импортированных для случая. Расширенное обнаружение электронных данных позволяет эксперту принимать решения, относящихся к принятому подходу, и применять их к проекту рецензирования документов.</span><span class="sxs-lookup"><span data-stu-id="55fbb-p102">Advanced eDiscovery enables early assessment, for example, for the defined issues and the data imported for a case. Advanced eDiscovery enables the expert to make decisions pertaining to an adopted approach and to apply them to the document review project.</span></span>
  
## <a name="understanding-assessment"></a><span data-ttu-id="55fbb-108">Общие сведения о оценке</span><span class="sxs-lookup"><span data-stu-id="55fbb-108">Understanding assessment</span></span>

<span data-ttu-id="55fbb-p103">В ходе оценки эксперт просматривает случайный набор по крайней мере 500 файлов, который используется для определения полноты проблем и получения статистики, отражающей обучающие результаты. Оценка считается успешной, если найдено достаточное количество релевантных файлов для достижения статистического уровня, который обеспечивает расширенную степень соответствия eDiscovery для обеспечения точной статистики и эффективного определения точки стабилизатион в процессе обучения.</span><span class="sxs-lookup"><span data-stu-id="55fbb-p103">In Assessment, the expert reviews a random set of at least 500 files, which are used to determine the richness of the issues and to produce statistics that reflect the training results. Assessment is successful when enough relevant files are found to reach a statistical level that will help Advanced eDiscovery Relevance to provide accurate statistics and to effectively determine the stabilization point in the training process.</span></span> 
  
<span data-ttu-id="55fbb-p104">Чем больше количество релевантных файлов в наборе оценки, тем точнее статистика и эффективность алгоритма стабильности. Количество релевантных файлов в оценочных файлах зависит от полноты проблемы. Насыщенность — это предполагаемый процент релевантных файлов в наборе, который относится к возникшей ошибке. Проблемы, связанные с более высокой степенью насыщенности, быстрее, чем проблемы с более высокой степенью насыщенности. Проблемы с чрезвычайно низким уровнем насыщенности (например, 2% или менее) требуют очень большого набора оценок для достижения значительного количества релевантных файлов.</span><span class="sxs-lookup"><span data-stu-id="55fbb-p104">The higher the number of relevant files in the assessment set, the more accurate the statistics and the effectiveness of the stability algorithm. The number of relevant files within the assessment files depends on the richness of the issue. Richness is the estimated percent of relevant files in the set relevant to an issue. Issues with higher richness will reach a higher number of relevant files more quickly than issues with lower richness. Issues with extremely low richness (for example, 2% or less) will require a very large assessment set to reach a significant number of Relevant files.</span></span>
  
<span data-ttu-id="55fbb-p105">Статистика, которая представлена в разделе Отслеживание и принятие вкладок во время обучения и после выполнения пакетного вычисления, включает оценки отзывов для разных наборов проверки. В статистике оценки, основанные на образце набора (в данном случае, файлы оценки) включают маржу ошибки и уровень вероятности этого поля ошибки. Например, оценочный отзыв 80% может иметь маржу ошибки плюс или минус 5% с уровнем вероятности 95%. Это означает, что предполагаемый отзыв фактически составляет 75%-85%, и эта оценка имеет значение 95%. Чем больше уровень оценки, тем меньше размер поля ошибки, а статистика будет более точной.</span><span class="sxs-lookup"><span data-stu-id="55fbb-p105">The statistics, which are presented in the Track and Decide tabs during training and after Batch calculation, include estimations of recall for different review sets. In statistics, estimations that are based on a sample set (in this case, the assessment files) include the margin of error and the confidence level of that error margin. For example, estimated recall of 80% might have a margin of error of plus or minus 5% with a confidence level of 95%. This means that the estimated recall is actually 75%-85% and this estimation has 95% confidence. The larger the assessment set, the margin of error becomes smaller and the statistics are more accurate.</span></span> 
  
<span data-ttu-id="55fbb-p106">После того как эксперт просматривает исходный набор оценок 500 файлов, релевантность может определить текущее поле ошибки для отзыва значений. Релевантность также задает значение по умолчанию для ошибки, которое рекомендуется для оптимизации набора оценки. Ниже приведены некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="55fbb-p106">After the expert reviews an initial assessment set of 500 files, Relevance is able to determine the current margin of error of the recall values. Relevance will also set a default margin of error that it recommends to reach to optimize the assessment set. Following are some examples:</span></span>
  
- <span data-ttu-id="55fbb-124">Если набор оценки уже выдает маржу "сообщение об ошибке плюс или минус 10%", релевантность будет рекомендуем перейти к учебному курсу (дополнительные оценки не требуются).</span><span class="sxs-lookup"><span data-stu-id="55fbb-124">If the assessment set already yielded a margin of error of plus or minus 10%, Relevance will recommend to move on to training (no additional assessment review is needed).</span></span> 
    
- <span data-ttu-id="55fbb-125">Если набор оценки выдает маржу ошибки плюс или минус 13%, релевантность может рекомендовать проверку другого набора файлов оценки для достижения меньшего поля.</span><span class="sxs-lookup"><span data-stu-id="55fbb-125">If the assessment set yielded a margin of error of plus or minus 13%, Relevance might recommend the review of another set of assessment files to reach a smaller margin.</span></span> 
    
- <span data-ttu-id="55fbb-126">Если насыщенность очень мала, важно остановить оценку, несмотря на то, что размер поля ошибки велик (Статистика непрактична), так как набор оценки, необходимый для достижения полезного поля ошибки, слишком велик.</span><span class="sxs-lookup"><span data-stu-id="55fbb-126">If richness is extremely low, Relevance might recommend stopping assessment even though the margin of error is large (making statistics impractical), because the assessment set needed to reach a useful margin of error is too large.</span></span>
    
<span data-ttu-id="55fbb-p107">У каждой ошибки есть свои полноты, текущая Маржа ошибки и в результате предполагаемое количество дополнительных файлов оценки. Следующий набор оценок создается в соответствии с максимальным количеством файлов (до 1 000 в едином наборе).</span><span class="sxs-lookup"><span data-stu-id="55fbb-p107">Each issue has its own richness, current margin of error, and as a result, estimated number of additional assessment files. The next assessment set is created according to the maximum number of files (up to 1,000 in a single set).</span></span>
  
<span data-ttu-id="55fbb-p108">Вы можете принять рекомендации относительно релевантности или скорректировать текущее поле ошибки в соответствии с вашими потребностями. По умолчанию для отзыва устанавливается значение по умолчанию равное или выше 75%.</span><span class="sxs-lookup"><span data-stu-id="55fbb-p108">You can accept the Relevance recommendations or adjust the current margin of error according to your needs. The default current margin of error is determined for recall at equal or above 75%.</span></span>
  
> [!NOTE]
> <span data-ttu-id="55fbb-p109">Этап оценки можно пропустить, на вкладке \*\* \> отслеживание релевантности\*\* в расширенном представлении проблемы, сняв флажок **оценки** для каждой проблемы, а затем — "все проблемы". Тем не менее, в результате этой ситуации будет отсутствовать статистика. _Гт_ очистка флажка **оценки** можно выполнить только до выполнения оценки. Если в случае существует несколько проблем, оценка обходится только в том случае, если этот флажок снят для каждой проблемы</span><span class="sxs-lookup"><span data-stu-id="55fbb-p109">The Assessment stage can be bypassed, in the **Relevance \> Track** tab in the expanded view for an issue, by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55fbb-135">См. также</span><span class="sxs-lookup"><span data-stu-id="55fbb-135">See also</span></span>

[<span data-ttu-id="55fbb-136">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="55fbb-136">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="55fbb-137">Маркировка и оценка</span><span class="sxs-lookup"><span data-stu-id="55fbb-137">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="55fbb-138">РасСтановка тегов и релевантности</span><span class="sxs-lookup"><span data-stu-id="55fbb-138">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="55fbb-139">Анализ релевантности отслеживания</span><span class="sxs-lookup"><span data-stu-id="55fbb-139">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="55fbb-140">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="55fbb-140">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="55fbb-141">Анализ релевантности тестирования</span><span class="sxs-lookup"><span data-stu-id="55fbb-141">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

