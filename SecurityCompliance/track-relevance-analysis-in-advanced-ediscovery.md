---
title: Отслеживание анализа релевантности в Office 365 Advanced eDiscovery
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
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: 'Узнайте, как просматривать и интерпретации состояние учебный курс по релевантности и результаты для вариантов проблем в Office 365 расширенного обнаружения электронных данных.  '
ms.openlocfilehash: a19f7eaabf5dc15eefaa7209ded8261020d0d557
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535502"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="b0392-103">Отслеживание анализа релевантности в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b0392-103">Track Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="b0392-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="b0392-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="b0392-106">В расширенной eDiscovery на вкладку Отслеживание релевантности отображает вычисляемые допустимость учебный курс по релевантности, выполняется в тег вкладки и указывает следующий этап для использования в процессе последовательной обучение более релевантности.</span><span class="sxs-lookup"><span data-stu-id="b0392-106">In Advanced eDiscovery, the Relevance Track tab displays the calculated validity of the Relevance training performed in the Tag tab and indicates the next step to take in the iterative training process in Relevance.</span></span> 
  
## <a name="tracking-relevance-training-status"></a><span data-ttu-id="b0392-107">Отслеживание состояния учебный курс по релевантности</span><span class="sxs-lookup"><span data-stu-id="b0392-107">Tracking Relevance training status</span></span>

1. <span data-ttu-id="b0392-108">Просмотрите следующие сведения в отслеживание релевантности для типовые проблемы, как показано в следующем примере диалоговое окно с **именем проблему** .</span><span class="sxs-lookup"><span data-stu-id="b0392-108">View the following details in Relevance Track for the case issues, as shown in the following example of an **Issue name** dialog below.</span></span> 
    
  - <span data-ttu-id="b0392-p102">**Оценка**: этот индикатор хода выполнения показывает, в какой степени релевантности, обучение, выполняемых на данный момент проведены конечного оценки с точки зрения погрешность. Расширение типов результатов учебный курс по релевантности также отображается.</span><span class="sxs-lookup"><span data-stu-id="b0392-p102">**Assessment**: This progress indicator shows to what degree the Relevance training performed to this point has achieved the assessment target in terms of margin of error. The richness of the Relevance training results is also displayed.</span></span> 
    
  - <span data-ttu-id="b0392-p103">**Учебный курс**: этот цветовой кодировкой хода выполнения индикатор и подсказки отображения указывает учебный курс по релевантности результатов стабильность и масштаб, отражающая число образцов учебный курс по релевантности с меткой для каждой проблемы. Эксперт отслеживает ход выполнения процесса последовательной учебный курс по релевантности.</span><span class="sxs-lookup"><span data-stu-id="b0392-p103">**Training**: This color-coded progress indicator and tool-tip display indicates the Relevance training results stability and a numeric scale showing the number of Relevance training samples tagged for each issue. The expert monitors the progress of the iterative Relevance training process.</span></span> 
    
  - <span data-ttu-id="b0392-113">**Расчет пакета**: этот индикатор хода выполнения предоставляет сведения о завершении расчет пакета.</span><span class="sxs-lookup"><span data-stu-id="b0392-113">**Batch calculation**: This progress indicator provides information about the completion of Batch calculation.</span></span>
    
  - <span data-ttu-id="b0392-114">**Следующий шаг**: отображает рекомендации по следующим шагом нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="b0392-114">**Next step**: Displays the recommendation for the next step to be performed.</span></span> 
    
    <span data-ttu-id="b0392-p104">В примере отображается успешно завершенных оценки проблемы, указанный в параметре завершенных цвет индикатора хода выполнения и флажок. Теги выполняется, но по-прежнему мероприятия нестабильных (стабильность состояния также отображаются в подсказки). Следующий шаг рекомендация «обучение».</span><span class="sxs-lookup"><span data-stu-id="b0392-p104">In the example, a successfully completed Assessment for an issue is shown, indicated by the completed color progress indicator and the checkmark. Tagging is underway, but the case is still considered unstable (stability status also shown in a tool-tip). The next step recommendation is "Training".</span></span> 
    
    ![Данные об обучении на вкладке "Релевантность" > "Отслеживание" (этап 1)](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    <span data-ttu-id="b0392-p105">Расширенное представление отображает дополнительные сведения и параметры. Отображаемые текущих полей ошибок — это поле ошибка отзыва в текущем состоянии оценки, учитывая существующие файлы (с тегами) оценки.</span><span class="sxs-lookup"><span data-stu-id="b0392-p105">The expanded view displays additional information and options. The displayed current error margin is the error margin of the recall in the current state of assessment, given the existing (already tagged) assessment files.</span></span>
    
    > [!NOTE]
    >  <span data-ttu-id="b0392-p106">Этап оценки можно обойти, сняв флажок **оценки** на проблему, а затем проблем «все». Тем не менее в результате будет Нет статистики для этой проблемы. > Если снять флажок **оценки** может быть выполнено только до выполнения оценки. Если существует несколько проблем в случае, оценка будет выполняться обход только в том случае, если флажок установлен для каждой проблемы</span><span class="sxs-lookup"><span data-stu-id="b0392-p106">The Assessment stage can be bypassed by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
    <span data-ttu-id="b0392-125">По завершении оценки не с первого примера набор файлов, оценки можно следующим шагом для добавления тегов дополнительные файлы.</span><span class="sxs-lookup"><span data-stu-id="b0392-125">When assessment is not completed with the first sample set of files, assessment might be the next step for tagging more files.</span></span> 
    
    <span data-ttu-id="b0392-p107">В **релевантности** \> **Отслеживание**, индикатор хода выполнения обучения и подсказки указывают предполагаемое количество Дополнительные примеры, необходимое для достижения стабильности. Эта оценка рекомендации, необходимые дополнительные обучения.</span><span class="sxs-lookup"><span data-stu-id="b0392-p107">In **Relevance** \> **Track**, the training progress indicator and tool-tip indicate the estimated number of additional samples needed to reach stability. This estimate provides a guideline for the additional training needed.</span></span>
    
    ![Данные об обучении на вкладке "Релевантность" > "Отслеживание"](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. <span data-ttu-id="b0392-p108">Когда вы будете Готово тегов и при необходимости продолжить обучение, щелкните **обучения**. Другой пример набор файлов создается из загруженного файла задайте для дополнительного обучения. Затем возврат к вкладке тег для тега и обучение пользователей дополнительные файлы.</span><span class="sxs-lookup"><span data-stu-id="b0392-p108">When you're done tagging and if you need to continue training, click **Training**. Another sample set of files is generated from the loaded file set for additional training. You are then returned to the Tag tab to tag and train more files.</span></span>
    
### <a name="reaching-stable-training-levels"></a><span data-ttu-id="b0392-132">Достижение уровни стабильным обучения</span><span class="sxs-lookup"><span data-stu-id="b0392-132">Reaching stable training levels</span></span>

<span data-ttu-id="b0392-133">После оценки файлы предметом стабильным уровень обучения, расширенные eDiscovery готов к расчет пакета.</span><span class="sxs-lookup"><span data-stu-id="b0392-133">After the assessment files have attained a stable level of training, Advanced eDiscovery is ready for Batch calculation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b0392-p109">Как правило после трех стабильность учебные примеры, следующим шагом является «Расчет пакета». Возможны исключения, например, когда выполнялись изменения для маркировки файлы из предыдущих примеров или когда начального значения файлы были добавлены.</span><span class="sxs-lookup"><span data-stu-id="b0392-p109">Usually, after three stable training samples, the next step is "Batch calculation". There may be exceptions, for example, when there were changes to the tagging of files from earlier samples or when seed files were added.</span></span> 
  
### <a name="performing-batch-calculation"></a><span data-ttu-id="b0392-136">Для выполнения вычислений пакета</span><span class="sxs-lookup"><span data-stu-id="b0392-136">Performing Batch calculation</span></span>

<span data-ttu-id="b0392-137">Расчет пакета выполняется как следующим шагом после успешного завершения обучения (когда стабильным обучение состояние отображается, индикатор хода выполнения, меток и с достаточно постоянным состояние всплывающая подсказка.) Расчет пакета применяется базы знаний, полученные при обучении релевантности для заполнения ко всему файлу, для оценки релевантности файлы и назначить показатели релевантности.</span><span class="sxs-lookup"><span data-stu-id="b0392-137">Batch calculation is executed as the next step after training is successfully completed (when a stable training status is shown by the progress bar, a checkmark and stable status in the tool-tip.) Batch calculation applies the knowledge acquired during the Relevance training to the entire file population, to assess the files' relevance and to assign Relevance scores.</span></span>
  
<span data-ttu-id="b0392-p110">При наличии более одной проблемы, расчет пакета выполняется на проблему. При расчете пакета ход выполнения отслеживается при обработке все файлы.</span><span class="sxs-lookup"><span data-stu-id="b0392-p110">When there is more than one issue, Batch calculation is done per issue. During Batch calculation, progress is monitored while processing all of the files.</span></span> 
  
<span data-ttu-id="b0392-p111">Здесь рекомендуется следующим шагом является «None», это означает, что без дополнительного обучения релевантности последовательной необходим на этом этапе. Следующий этап является **релевантности \> решите** вкладки.</span><span class="sxs-lookup"><span data-stu-id="b0392-p111">Here, the recommended next step is "None", which indicates that no additional iterative Relevance training is required at this point. The next phase is the **Relevance \> Decide** tab.</span></span> 
  
<span data-ttu-id="b0392-142">Если вы хотите импортировать новые файлы после расчета пакета, администратор может добавить импортируемые файлы новых нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b0392-142">If you want to import new files after Batch calculation, the administrator can add the imported files to a new load.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b0392-p112">Если нажать кнопку **Отмена** во время расчет пакета сохраняет что уже был выполнен. При выполнении расчет пакета еще раз, процесс будет предоставляться из последнего выполненного точки.</span><span class="sxs-lookup"><span data-stu-id="b0392-p112">If you click **Cancel** during Batch calculation, the process saves what was already executed. If you run Batch calculation again, the process will continue from the last executed point.</span></span> 
  
### <a name="assessing-tagging-consistency"></a><span data-ttu-id="b0392-145">Оценка тегов согласованности</span><span class="sxs-lookup"><span data-stu-id="b0392-145">Assessing tagging consistency</span></span>

<span data-ttu-id="b0392-p113">При наличии несоответствий в файл тегов, могут повлиять на анализа. Расширенные eDiscovery тегов согласованность процесса можно использовать при результаты не оптимальную или согласованности сомнения. Возвращает список возможных несогласованно с тегами файлы и просмотреть и повторно с меткой, при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b0392-p113">If there are inconsistencies in file tagging, it can affect the analysis. The Advanced eDiscovery tagging consistency process can be used when results are not optimal or consistency is in doubt. A list of possible inconsistently tagged files is returned, and they can be reviewed and re-tagged, as necessary.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b0392-p114">После 7 или более округляет обучения, можно просмотреть следующие оценки, тегов согласованности в **релевантности** \> **Отслеживание** \> **проблему** \> **Подробные результаты** \> **о ходе обучения**. Этот анализ выполняется для одной проблемы за раз.</span><span class="sxs-lookup"><span data-stu-id="b0392-p114">After seven or more training rounds following assessment, tagging consistency can be viewed in **Relevance** \> **Track** \> **Issue** \> **Detailed results** \> **Training progress**. This review is done for one issue at a time.</span></span> 
  
1. <span data-ttu-id="b0392-151">В **релевантности \> отслеживание**, разверните строку проблему.</span><span class="sxs-lookup"><span data-stu-id="b0392-151">In **Relevance \> Track**, expand an issue's row.</span></span>
    
2. <span data-ttu-id="b0392-152">В правой части **следующим шагом**нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="b0392-152">To the right of **Next step**, click **Modify**.</span></span>
    
3. <span data-ttu-id="b0392-153">Выберите **тег несоответствия** в качестве параметра **следующим шагом** после семь учебные примеры и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="b0392-153">Select **Tag inconsistencies** as the **Next step** option, after seven training samples and click **OK**.</span></span>
    
4. <span data-ttu-id="b0392-p115">Выберите **тег несоответствия**. Вкладка " **тег** " открывает вывод списка несоответствия повторно Установка метки при необходимости.</span><span class="sxs-lookup"><span data-stu-id="b0392-p115">Select **Tag inconsistencies**. The **Tag** tab opens displaying a list of the inconsistencies to re-tag as necessary.</span></span> 
    
5. <span data-ttu-id="b0392-p116">Нажмите кнопку **Расчет** внесения изменений. Следующим шагом после добавления тегов несоответствия «обучение».</span><span class="sxs-lookup"><span data-stu-id="b0392-p116">Click **Calculate** to submit the changes. The next step after tagging inconsistencies is "Training".</span></span> 
    
## <a name="viewing-and-using-relevance-results"></a><span data-ttu-id="b0392-158">Просмотр и использование релевантности результатов</span><span class="sxs-lookup"><span data-stu-id="b0392-158">Viewing and using Relevance results</span></span>

<span data-ttu-id="b0392-p117">В **релевантности \> отслеживание** , разверните строку проблему, а рядом с пунктом **Подробные результаты**, щелкните **представление**. Подробные результаты областей, отображаемых, как показано и описанных ниже.</span><span class="sxs-lookup"><span data-stu-id="b0392-p117">In the **Relevance \> Track** tab, expand an issue's row, and next to **Detailed results**, click **View**. The Detailed results panes are displayed, as shown and described below.</span></span>
  
![Подробные результаты обучения для определения релевантности](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a><span data-ttu-id="b0392-162">Сводка тегов</span><span class="sxs-lookup"><span data-stu-id="b0392-162">Tagging summary</span></span>

 <span data-ttu-id="b0392-163">В приведенном ниже примере **сводки тегов** отображает итоговые значения для каждой из связанной с подключением файлов, тегов процессы, обучение и оценки.</span><span class="sxs-lookup"><span data-stu-id="b0392-163">In the example shown below, the **Tagging summary** displays totals for each of Assessment, Training, and Catch-up file tagging processes.</span></span> 
  
![Сводка по тегам на вкладке "Релевантность" > "Отслеживание"](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a><span data-ttu-id="b0392-165">Keywords</span><span class="sxs-lookup"><span data-stu-id="b0392-165">Keywords</span></span>

<span data-ttu-id="b0392-p118">Ключевое слово — это уникальная строка, word, фразу или последовательность слов в файле помечаются с расширенной обнаружения электронных данных как значительные индикатор ли файл является релевантным. Столбцы «Включить» списка ключевых слов и веса в файлах, помеченный как Relevant и столбцы «Исключить» перечислены ключевые слова и веса в файлах, помеченный как Not релевантным.</span><span class="sxs-lookup"><span data-stu-id="b0392-p118">A keyword is a unique string, word, phrase, or sequence of words in a file identified by Advanced eDiscovery as a significant indicator of whether a file is relevant. The "Include" columns list keyword and weights in files tagged as Relevant, and the "Exclude" columns lists keywords and weights in files tagged as Not relevant.</span></span>
  
<span data-ttu-id="b0392-p119">Расширенные eDiscovery назначает ключевое слово или отрицательное вес значения. Чем выше вес, чем выше вероятность, что файл, в котором отображается ключевое слово назначен высокий показатель релевантности во время расчет пакета.</span><span class="sxs-lookup"><span data-stu-id="b0392-p119">Advanced eDiscovery assigns negative or positive keyword weight values. The higher the weight, the higher the likelihood that a file in which the keyword appears is assigned a higher Relevance score during Batch calculation.</span></span> 
  
<span data-ttu-id="b0392-170">Расширенные eDiscovery список ключевых слов можно использовать в качестве дополнения к список созданных эксперт или как проверку работоспособности косвенных в любой момент в файле процесса проверки.</span><span class="sxs-lookup"><span data-stu-id="b0392-170">The Advanced eDiscovery list of keywords can be used to supplement a list built by an expert or as an indirect sanity check at any point in the file review process.</span></span>
  
### <a name="training-progress"></a><span data-ttu-id="b0392-171">Учебный курс по хода выполнения</span><span class="sxs-lookup"><span data-stu-id="b0392-171">Training progress</span></span>

<span data-ttu-id="b0392-172">В области **Обучения хода выполнения** включает в себя обучение хода выполнения графике и качество индикатор display, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b0392-172">The **Training Progress** pane includes a training progress graph and quality indicator display, as shown in the example below.</span></span> 
  
![Индикатор выполнения обучения на вкладке "Релевантность" > "Отслеживание"](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 <span data-ttu-id="b0392-174">**Обучение индикатора качества**: отображает оценки тегов согласованности следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b0392-174">**Training quality indicator**: Displays the rating of the tagging consistency as follows:</span></span>
  
- <span data-ttu-id="b0392-p120">**Хороший**: файлы помеченные постоянно. (Зеленый отображаются)</span><span class="sxs-lookup"><span data-stu-id="b0392-p120">**Good**: Files are tagged consistently. (Green light displayed)</span></span>
    
- <span data-ttu-id="b0392-p121">**Средний**: некоторые файлы могут быть меткой несогласованно. (Желтый индикатор отображается)</span><span class="sxs-lookup"><span data-stu-id="b0392-p121">**Medium**: Some files may be tagged inconsistently. (Yellow light displayed)</span></span>
    
- <span data-ttu-id="b0392-p122">**Предупреждение**: много файлов может использоваться несогласованно. (Отображаться красный индикатор)</span><span class="sxs-lookup"><span data-stu-id="b0392-p122">**Warning**: Many files may be tagged inconsistently. (Red light displayed)</span></span>
    
 <span data-ttu-id="b0392-p123">**Обучение графическое представление о ходе выполнения**: показывает степень релевантности обучение стабильность после числа циклов учебный курс по релевантности по сравнению с значение F меры. Как мы перемещения из слева направо график, сужает доверительный интервал и используется, а также меры F расширенной eDiscovery релевантности для определения стабильности оптимизированы при учебный курс по релевантности результатов.</span><span class="sxs-lookup"><span data-stu-id="b0392-p123">**Training progress graph**: Shows the degree of Relevance training stability after a number of Relevance training cycles in comparison to the F-measure value. As we move from the left to the right across the graph, the confidence interval narrows and is used, along with the F-measure, by Advanced eDiscovery Relevance to determine stability when the Relevance training results are optimized.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b0392-p124">Релевантность использует F2 показатель F мер, где отзыва получает вдвое больший вес точность. Обращений с высокой расширение (более 25%), использует релевантности F1 (соотношение 1:1). Соотношение F мер можно настроить в **программе установки релевантности** \> **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="b0392-p124">Relevance uses F2, an F-measure metric where Recall receives twice as much weight as Precision. For cases with high richness (over 25%), Relevance uses F1 (1:1 ratio). The F-measure ratio can be configured in **Relevance setup** \> **Advanced settings**.</span></span> 
  
### <a name="batch-calculation-results"></a><span data-ttu-id="b0392-186">Результаты расчета пакета</span><span class="sxs-lookup"><span data-stu-id="b0392-186">Batch calculation results</span></span>

<span data-ttu-id="b0392-187">В области **Результаты расчета пакета** включает в себя число файлов, которые были результат соответствия, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="b0392-187">The **Batch calculation results** pane includes the number of files that were scored for Relevance, as follows:</span></span> 
  
- <span data-ttu-id="b0392-188">**Success**</span><span class="sxs-lookup"><span data-stu-id="b0392-188">**Success**</span></span>
    
- <span data-ttu-id="b0392-189">**Пустой**: не содержит текста, например только пробелы/вкладок</span><span class="sxs-lookup"><span data-stu-id="b0392-189">**Empty**: Contains no text, for example, only spaces/tabs</span></span>
    
- <span data-ttu-id="b0392-190">**Не удалось выполнить**: из-за чрезмерной размера или не удалось прочитать</span><span class="sxs-lookup"><span data-stu-id="b0392-190">**Failed**: Due to excessive size or could not be read</span></span>
    
- <span data-ttu-id="b0392-191">**Игнорируется**: из-за чрезмерной размера</span><span class="sxs-lookup"><span data-stu-id="b0392-191">**Ignored**: Due to excessive size</span></span>
    
- <span data-ttu-id="b0392-192">**Nebulous**: содержит не имеет смысла текста или не относится к проблеме функции</span><span class="sxs-lookup"><span data-stu-id="b0392-192">**Nebulous**: Contains meaningless text or no features relevant to the issue</span></span>
    
> [!NOTE]
> <span data-ttu-id="b0392-193">Пустой, не удалось выполнить, игнорируется или Nebulous будет получать показатель релевантности-1.</span><span class="sxs-lookup"><span data-stu-id="b0392-193">Empty, Failed, Ignored, or Nebulous will receive a Relevance score of -1.</span></span> 
  
### <a name="training-statistics"></a><span data-ttu-id="b0392-194">Учебный курс по статистике</span><span class="sxs-lookup"><span data-stu-id="b0392-194">Training statistics</span></span>

<span data-ttu-id="b0392-195">В области **Статистика учебный курс по** отображается статистика и диаграмм на основе результатов обучающего по релевантности расширенной обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="b0392-195">The **Training statistics** pane displays statistics and graphs based on results from Advanced eDiscovery Relevance training.</span></span> 
  
![Статистика обучения на вкладке "Релевантность" > "Отслеживание"](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
<span data-ttu-id="b0392-197">Это представление отображает следующие:</span><span class="sxs-lookup"><span data-stu-id="b0392-197">This view shows the following:</span></span>
  
- <span data-ttu-id="b0392-p125">**Соотношение проверки отзыва**: сравнение результатов по релевантности набирает гипотетически линейная проверки. Отзыв — это рекомендованная набора размера набора проверки.</span><span class="sxs-lookup"><span data-stu-id="b0392-p125">**Review-recall ratio**: Comparison of results according to Relevance scores in a hypothetically linear review. Recall is estimated given the review set size set.</span></span>
    
- <span data-ttu-id="b0392-200">**Параметры**: накопительные пакеты вычисления статистики, относящиеся к просмотру, задайте по отношению к заполнения файла для всего примера.</span><span class="sxs-lookup"><span data-stu-id="b0392-200">**Parameters**: Cumulative calculated statistics pertaining to the review set in relation to the file population for the entire case.</span></span>
    
- <span data-ttu-id="b0392-201">**Просмотрите**: процент файлы для просмотра на основании этого сканирования.</span><span class="sxs-lookup"><span data-stu-id="b0392-201">**Review**: Percentage of files to review based on this cutoff.</span></span>
    
- <span data-ttu-id="b0392-202">**Отзыв**: процент Relevant файлы в наборе проверки.</span><span class="sxs-lookup"><span data-stu-id="b0392-202">**Recall**: Percentage of Relevant files in the review set.</span></span> 
    
- <span data-ttu-id="b0392-p126">**Распределение по релевантности показателю**: файлы темный экран серый слева, ниже ограничения оценки. Подсказки отображает показатель релевантности и связанных с ними процент файлы в файле проверки, задайте по отношению к всего файлов.</span><span class="sxs-lookup"><span data-stu-id="b0392-p126">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0392-205">См. также</span><span class="sxs-lookup"><span data-stu-id="b0392-205">See also</span></span>

[<span data-ttu-id="b0392-206">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b0392-206">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="b0392-207">Общие сведения об оценке в релевантности</span><span class="sxs-lookup"><span data-stu-id="b0392-207">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b0392-208">Для выполнения и проверки оценки</span><span class="sxs-lookup"><span data-stu-id="b0392-208">Performing and reviewing Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b0392-209">Учебный курс по релевантности для выполнения</span><span class="sxs-lookup"><span data-stu-id="b0392-209">Performing Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b0392-210">Принятия решений на основе результатов</span><span class="sxs-lookup"><span data-stu-id="b0392-210">Making decisions based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b0392-211">Тестирование анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="b0392-211">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

