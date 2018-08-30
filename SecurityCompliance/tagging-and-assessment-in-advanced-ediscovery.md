---
title: Добавление тегов и оценка в Office 365 Advanced eDiscovery
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
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: 'Рассмотрим эти действия для выполнения оценки, включая обучение тегов файлы и просмотрев результаты оценки в Office 365 расширенного обнаружения электронных данных. '
ms.openlocfilehash: 0f67dd4780a29536888231f556c18fe887f230ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534716"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a><span data-ttu-id="4d741-103">Добавление тегов и оценка в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4d741-103">Tagging and Assessment in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="4d741-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="4d741-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="4d741-106">В этом разделе описывается процедура модуль оценки релевантности расширенной обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="4d741-106">This section describes the procedure for the Advanced eDiscovery Relevance Assessment module.</span></span> 
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="4d741-107">Для выполнения оценки обучения и анализ</span><span class="sxs-lookup"><span data-stu-id="4d741-107">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="4d741-108">В **релевантности \> отслеживание** щелкните **оценки** для запуска вариантов оценки.</span><span class="sxs-lookup"><span data-stu-id="4d741-108">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span> 
    
    <span data-ttu-id="4d741-109">Например целей в этой процедуре, пример оценки 500 файлов — это создать, и отображается вкладка **тег** , который содержит панель тегов, отображаемые файл содержимого и другие параметры тегов.</span><span class="sxs-lookup"><span data-stu-id="4d741-109">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 
    
    ![Вкладка "Релевантность" > "Добавление тегов" для оценки](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="4d741-111">Просмотрите каждый файл в образце, определите файл релевантности для каждого case проблемы и отметить файл с помощью Relevance (R), не соответствующие (NR) и пропустить кнопки в области **панели тегов** .</span><span class="sxs-lookup"><span data-stu-id="4d741-111">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="4d741-p102">Для оценки необходимо 500 файлы с тегами. Если файлы «пропускаются», вы получите дополнительные файлы для тега.</span><span class="sxs-lookup"><span data-stu-id="4d741-p102">Assessment requires 500 tagged files. If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="4d741-114">После теги все файлы в образце, нажмите кнопку **Calculate**.</span><span class="sxs-lookup"><span data-stu-id="4d741-114">After tagging all files in the sample, click **Calculate**.</span></span> 
    
    <span data-ttu-id="4d741-p103">Оценки текущих ошибка полей и расширение рассчитывается и отображается на вкладке **Отслеживание релевантности** с расширенной сведениями на проблему, как показано ниже. Дополнительные сведения об этом диалоговом окне, описаны далее в разделе «Результаты оценки рецензирование».</span><span class="sxs-lookup"><span data-stu-id="4d741-p103">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below. More details about this dialog are described in the later section "Reviewing Assessments results".</span></span> 
    
    ![Оценка на вкладке "Релевантность" > "Отслеживание"](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="4d741-p104">По умолчанию мы рекомендуем, что переходите к следующему шагу по умолчанию после завершения индикатор хода выполнения оценки вопросов, указывающего на то, что пример оценки прошел проверку и достаточно соответствующие файлы были добавлены. > В противном случае если вы хотите просмотреть результаты вкладку **Отслеживание** и элемента управления поля сообщений об ошибках и следующим шагом, нажмите кнопку **Изменить** , рядом с **Следующим шагом**выберите **Продолжить оценки**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4d741-p104">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged. > Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span> 
  
1. <span data-ttu-id="4d741-p105">Нажмите кнопку **Изменить** справа от флажок **оценки** для просмотра и указания параметров оценки на одну проблему. Отображается диалоговое окно с **уровень оценки** для каждой проблемы, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="4d741-p105">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue. An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 
    
    ![Уровень оценки: элемент для оценивания при выполнении задания](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="4d741-123">Следующие параметры для проблему вычисляются и отображаются в диалоговом окне **уровень оценки** :</span><span class="sxs-lookup"><span data-stu-id="4d741-123">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 
    
    <span data-ttu-id="4d741-p106">**Оценивает целевого поля ошибки для отзыва**: на основе этого значения, рассчитывается предполагаемое количество дополнительные файлы, необходимо просмотреть. Поля, используемые для отзыва больше, чем 75% и с уровень вероятности 95%.</span><span class="sxs-lookup"><span data-stu-id="4d741-p106">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated. The margin used for recall is greater than 75% and with a 95% confidence level.</span></span> 
    
    <span data-ttu-id="4d741-126">**Необходимые файлы дополнительные оценки**: Указывает, сколько дополнительные файлы необходимы, если текущее поле ошибки не требований.</span><span class="sxs-lookup"><span data-stu-id="4d741-126">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 
    
2. <span data-ttu-id="4d741-127">Настройка полей текущей ошибки и посмотрите, влияние различных ошибка полей (для каждого проблема):</span><span class="sxs-lookup"><span data-stu-id="4d741-127">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>
    
1. <span data-ttu-id="4d741-128">В списке **выберите проблемы** выберите проблему.</span><span class="sxs-lookup"><span data-stu-id="4d741-128">In the **Select issue** list, select an issue.</span></span> 
    
2. <span data-ttu-id="4d741-129">В **оценивает целевого поля ошибки для отзыва**введите новое значение.</span><span class="sxs-lookup"><span data-stu-id="4d741-129">In **Target error margin for recall estimates**, enter a new value.</span></span>
    
3. <span data-ttu-id="4d741-130">Щелкните **Обновить значения** , чтобы оценить влияние корректировки.</span><span class="sxs-lookup"><span data-stu-id="4d741-130">Click **Update values** to see the impact of the adjustments.</span></span> 
    
3. <span data-ttu-id="4d741-131">Нажмите кнопку **Дополнительно** в диалоговом окне **уровень оценки** следующие дополнительные параметры и сведения о:</span><span class="sxs-lookup"><span data-stu-id="4d741-131">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 
    
    ![Расширенное представление "Уровень оценки: элемент для оценивания при выполнении задания"](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    <span data-ttu-id="4d741-133">**Оценка набора операторов**: Предполагаемое расширение в соответствии с текущих результатов оценки</span><span class="sxs-lookup"><span data-stu-id="4d741-133">**Estimated richness**: Estimated richness according to the current assessment results</span></span>
    
    <span data-ttu-id="4d741-p107">**Для предполагаемой отзыва**: по умолчанию, задает поля Ошибка целевой для отзыва выше 75%. Если вы хотите изменить этот параметр и управления поля ошибки на разных диапазон значений отзыв, нажмите кнопку **Изменить** .</span><span class="sxs-lookup"><span data-stu-id="4d741-p107">**For assumed recall**: By default, the target error margin applies to recall above 75%. Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 
    
    <span data-ttu-id="4d741-p108">**Уровень вероятности**: по умолчанию, поле рекомендуемые об ошибках для вероятности не 95%. Если вы хотите изменить этот параметр, нажмите кнопку **Изменить** .</span><span class="sxs-lookup"><span data-stu-id="4d741-p108">**Confidence level**: By default, the recommended error margin for confidence is 95%. Click **Edit** if you want to change this parameter.</span></span> 
    
    <span data-ttu-id="4d741-138">**Поля Ошибка ожидаемого набора операторов**: учитывая обновленные значения, это ожидаемый погрешность из набора, после разделами все файлы дополнительные оценки.</span><span class="sxs-lookup"><span data-stu-id="4d741-138">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>
    
    <span data-ttu-id="4d741-139">**Необходимые файлы дополнительные оценки**: учитывая обновленные значения, число дополнительных оценки файлы эту задачу для связи с целевым для анализа.</span><span class="sxs-lookup"><span data-stu-id="4d741-139">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>
    
    <span data-ttu-id="4d741-140">**Необходимые файлы общее оценки**: учитывая обновленные значения, общее число файлов оценки, необходимых для просмотра.</span><span class="sxs-lookup"><span data-stu-id="4d741-140">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>
    
    <span data-ttu-id="4d741-141">**Ожидаемое число соответствующие файлы в оценки**: обновленные значения ожидаемое число соответствующие файлы в всей оценки после разделами все файлы дополнительные оценки.</span><span class="sxs-lookup"><span data-stu-id="4d741-141">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>
    
4. <span data-ttu-id="4d741-p109">Нажмите **Пересчитать значения**, при изменении параметров. Закончив, если имеется одна проблема, нажмите **кнопку ОК** , чтобы сохранить изменения (или **Далее** при наличии нескольких проблем для просмотра или изменения, а затем **Готово**).</span><span class="sxs-lookup"><span data-stu-id="4d741-p109">Click **Recalculate values**, if parameters are changed. When you are done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 
    
    <span data-ttu-id="4d741-144">При наличии нескольких проблем после все проблемы были просмотрены или изменить, **уровень оценки: сводки** отображается диалоговое окно, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="4d741-144">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Уровень оценки: сводка](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="4d741-146">После успешного выполнения оценки перейдите на следующий этап в учебный курс по релевантности.</span><span class="sxs-lookup"><span data-stu-id="4d741-146">Upon successful completion of assessment, proceed to the next stage in Relevance training.</span></span>
    
## <a name="reviewing-assessment-results"></a><span data-ttu-id="4d741-147">Просмотр результатов оценки</span><span class="sxs-lookup"><span data-stu-id="4d741-147">Reviewing assessment results</span></span>

<span data-ttu-id="4d741-148">После отмеченными пример оценки, результаты оценки вычисляются и отображаются на вкладке Отслеживание релевантности.</span><span class="sxs-lookup"><span data-stu-id="4d741-148">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="4d741-149">Следующие результаты отображаются в окне Расширенный отслеживание:</span><span class="sxs-lookup"><span data-stu-id="4d741-149">The following results are displayed in the expanded Track display:</span></span> 
  
- <span data-ttu-id="4d741-150">Оценка текущего поля Ошибка оценки для отзыва</span><span class="sxs-lookup"><span data-stu-id="4d741-150">Assessment current error margin for recall estimates</span></span>
    
- <span data-ttu-id="4d741-151">Оценка набора операторов</span><span class="sxs-lookup"><span data-stu-id="4d741-151">Estimated richness</span></span>
    
- <span data-ttu-id="4d741-152">Файлы дополнительные оценки, обязательно (для ознакомления)</span><span class="sxs-lookup"><span data-stu-id="4d741-152">Additional assessment files required (for review)</span></span>
    
<span data-ttu-id="4d741-p110">Ошибка поля текущей оценки — это поля ошибки, рекомендуется использовать с расширенной обнаружения электронных данных. Номер, отображаемый для файлов дополнительные оценки «требуется» соответствует этой рекомендации.</span><span class="sxs-lookup"><span data-stu-id="4d741-p110">The Assessment current error margin is the error margin recommended by Advanced eDiscovery. The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="4d741-p111">Индикатор хода выполнения оценки показывает уровень завершении оценки, присвоенное текущих полей ошибок. Когда выполняется оценки, пользователь будет тега другой пример оценки.</span><span class="sxs-lookup"><span data-stu-id="4d741-p111">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin. When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="4d741-157">Когда индикатор выполнения оценки показывает оценки как завершенные, который означает, что была выполнена проверка примера оценки и достаточно соответствующие файлы были добавлены.</span><span class="sxs-lookup"><span data-stu-id="4d741-157">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="4d741-158">Расширенное отслеживание отображает действия, Статистика оценки и доступ к подробные результаты.</span><span class="sxs-lookup"><span data-stu-id="4d741-158">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="4d741-p112">При очень низкой расширение номеру оценки дополнительные файлы, требуемые для достижения минимально необходимое количество необходимые файлы для создания полезных статистики очень высокий. Расширенные eDiscovery затем будет рекомендуем перейдет на обучение. Индикатор хода выполнения оценки будет применена и статистики не будет доступен.</span><span class="sxs-lookup"><span data-stu-id="4d741-p112">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high. Advanced eDiscovery will then recommend moving on to training. The assessment progress indicator will be shaded, and no statistics will be available.</span></span> 
  
<span data-ttu-id="4d741-p113">В случае отсутствия статистическое на основе стабилизацией будет результаты с низким уровнем уровень точности и надежности. Тем не менее можно использовать эти результаты найти необходимые файлы, если необходимо знать процент найдено соответствующих файлов. Аналогично это состояние можно использовать для обучения проблемы с низкой расширение где показателям релевантности ускорение доступа к файлам, предназначенных для конкретной проблемы.</span><span class="sxs-lookup"><span data-stu-id="4d741-p113">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level. However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found. Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="4d741-p114">В **релевантности \> отслеживание** tab, отображать расширенное проблему, доступны следующие параметры просмотра: > рекомендуемые далее шаг, таких как **Следующий шаг: тегов** можно обойти (на проблему), щелкнув кнопку **Изменить** , чтобы его вправо затем выберите другой шаг на **следующем этапе**. Когда индикатор хода выполнения оценки не завершится, оценки будут далее параметр рекомендуется использовать, чтобы отметить дополнительные файлы оценки и повышают точность статистики. > Можно изменить поля ошибки и оценить его влияние, нажав кнопку **Изменить**и в окне **оценки уровня диалоговое окно**изменение **оценивает целевого поля ошибки для отзыва**и нажав кнопку **Обновить**. Кроме того в этом диалоговом окне можно просмотреть дополнительные параметры, нажмите кнопку **Дополнительно**. > Можно просмотреть дополнительные оценки уровня статистики и их влияния, нажав кнопку **Просмотр**. В окне результаты отображаемых сведений о статистики доступны на проблему, а также, если есть по крайней мере 500 файлы с тегами оценки и по крайней мере 18 файлы помеченные как Relevant вопросов.</span><span class="sxs-lookup"><span data-stu-id="4d741-p114">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available: > The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**. When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy. > You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**. Also, in this dialog, you can view advanced options, by clicking **Advanced**. > You can view additional assessment level statistics and their impact by clicking **View**. In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d741-171">См. также</span><span class="sxs-lookup"><span data-stu-id="4d741-171">See also</span></span>

[<span data-ttu-id="4d741-172">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4d741-172">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="4d741-173">Общие сведения об оценке в релевантности</span><span class="sxs-lookup"><span data-stu-id="4d741-173">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4d741-174">Теги и учебный курс по релевантности</span><span class="sxs-lookup"><span data-stu-id="4d741-174">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4d741-175">Отслеживание анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="4d741-175">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4d741-176">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="4d741-176">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4d741-177">Тестирование анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="4d741-177">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

