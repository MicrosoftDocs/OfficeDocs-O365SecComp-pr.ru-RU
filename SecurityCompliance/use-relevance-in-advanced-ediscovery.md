---
title: Использование модуля релевантности в Office 365 Advanced eDiscovery
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Узнайте о модуле релевантности в Office 365 Advanced eDiscovery, в том числе о рабочем процессе и рекомендациях по обучению и проверке файлов.  '
ms.openlocfilehash: ad44066c8b00bccacf1f4fe2088aa84096c4db84
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217459"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="8f364-103">Использование модуля релевантности в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8f364-103">Use the Relevance module in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="8f364-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="8f364-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="8f364-p102">В Advanced eDiscovery модуль релевантности включает обучение релевантности и обзор файлов, связанных с обращением. Рабочий процесс релевантности отображается и описывается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8f364-p102">In Advanced eDiscovery, the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![Рабочий процесс определения релевантности](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="8f364-109">**Циклы оценки и отслеживания**:</span><span class="sxs-lookup"><span data-stu-id="8f364-109">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="8f364-110">**Оценка**: Advanced eDiscovery позволяет проводить раннее оценивание на основе случайного примера файлов и использовать эту оценку для определения производительности процесса прогнозирующих кодов.</span><span class="sxs-lookup"><span data-stu-id="8f364-110">**Assessment**: Advanced eDiscovery enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="8f364-111">**Track**: Advanced eDiscovery вычисляет и отображает промежуточные результаты оценки при наблюдении за статистическим действием процесса.</span><span class="sxs-lookup"><span data-stu-id="8f364-111">**Track**: Advanced eDiscovery calculates and displays interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="8f364-112">**Циклы обучения и отслеживания**:</span><span class="sxs-lookup"><span data-stu-id="8f364-112">**Cycles of training and tracking**:</span></span>
    
  - <span data-ttu-id="8f364-113">**Тег**: Advanced eDiscovery сведения об условиях релевантности для каждой из них, основанных на итеративной проверке и разметке отдельных файлов экспертом.</span><span class="sxs-lookup"><span data-stu-id="8f364-113">**Tag**: Advanced eDiscovery learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="8f364-114">**Track**: Advanced eDiscovery вычисляет и отображает промежуточные результаты обучения релевантности при наблюдении за статистическим действием процесса.</span><span class="sxs-lookup"><span data-stu-id="8f364-114">**Track**: Advanced eDiscovery calculates and displays interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="8f364-115">**ВычисленИе пакетов**: расширенные функции обнаружения электронных данных принимают условия с накоплением и накоплением соответствия, применяют их ко всей коллекции файлов и создают для каждого файла показатели релевантности.</span><span class="sxs-lookup"><span data-stu-id="8f364-115">**Batch calculation**: Advanced eDiscovery takes the accumulated and learned Relevance criteria, applies it to the entire file collection, and generates Relevance scores for each file.</span></span>
    
- <span data-ttu-id="8f364-116">**Выбор**: Advanced eDiscovery отображает результаты анализа, примененного ко всему случаю после выполнения пакетного вычисления, и отображает данные для принятия решений по рецензированию документов.</span><span class="sxs-lookup"><span data-stu-id="8f364-116">**Decide**: Advanced eDiscovery displays the results of the analysis applied to the entire case after Batch calculation and displays data for making document review decisions.</span></span>
    
- <span data-ttu-id="8f364-117">**Test**: расширенные результаты обнаружения электронных данных можно протестировать, чтобы проверить допустимость и эффективность работы расширенной обработки обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="8f364-117">**Test**: Advanced eDiscovery results can be tested to verify the validity and effectiveness of the Advanced eDiscovery processing.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="8f364-118">Рекомендации по изучению и обзору релевантности</span><span class="sxs-lookup"><span data-stu-id="8f364-118">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="8f364-119">Ниже представлен обзор рекомендаций по изучению и проверке релевантности.</span><span class="sxs-lookup"><span data-stu-id="8f364-119">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="8f364-p103">**Ошибки и несоответствия**. при возникновении ошибок тегирования в ходе обучения вернитесь к предыдущим примерам файлов, чтобы исправить их. Если вы намерены слишком много ошибок или если у вас есть новая перспектива или ситуация, условия релевантности должны быть переопределены администратором и перезапущено обучение по релевантности.</span><span class="sxs-lookup"><span data-stu-id="8f364-p103">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="8f364-122">**Маркировка и обучение**:</span><span class="sxs-lookup"><span data-stu-id="8f364-122">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="8f364-p104">Файлы следует размечать только на основе контента. Не учитывайте метаданные, такие как хранитель, дата или путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="8f364-p104">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="8f364-125">Не учитывайте указания диапазона дат в тексте при разметке тегами файлов.</span><span class="sxs-lookup"><span data-stu-id="8f364-125">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="8f364-126">Не учитывайте внедренные графические изображения при разметке тегами файлов.</span><span class="sxs-lookup"><span data-stu-id="8f364-126">Do not consider embedded graphical images when tagging files.</span></span>
    
  - <span data-ttu-id="8f364-p105">При просмотре файла с помощью значка **форматированного текста** во время тегирования не следует расдумать форматирование текста. Например, слово, отображаемое с зачеркиванием (горизонтальная линия через его центр, указывающее на удаление), по-прежнему считается релевантностью в составе анализируемого текста.</span><span class="sxs-lookup"><span data-stu-id="8f364-p105">If viewing a file using the **formatted text view** icon while tagging, do not consider the formatting of text. For example, a word displayed with a strikethrough (a horizontal line through its center indicating deletion) is still considered by Relevance as part of the analyzed text.</span></span> 
    
  - <span data-ttu-id="8f364-p106">Игнорировать текст, примененный к релевантности (как задано управляющим обращениями или администратором), будет удален в отображаемом содержимом файла в текстовом представлении релевантность. Если значения для параметра Ignore Text были определены после начала обучения соответствия, новый пропущенный текст будет применен к образцам файлов, созданным на основе точки, в которой он был определен. Функция ignore Text должна использоваться с осторожностью, так как ее использование может привести к снижению производительности анализа файлов.</span><span class="sxs-lookup"><span data-stu-id="8f364-p106">Ignore text applied to Relevance (as set by the Case Manager or Administrator) will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="8f364-p107">Используйте параметр **пропускать маркировку** , только если это необходимо. Расширенные функции обнаружения электронных данных не обучены на основе пропущенных файлов. В процессе оценки, если трудно определить, является ли файл релевантным, лучше помечаться как соответствующий (R) или нет (НР), если это возможно, а не выбирать **пропустить**. Когда Расширенное обнаружение электронных данных оценивает обучение, можно увидеть, насколько хорошо обрабатывались эти типы файлов.</span><span class="sxs-lookup"><span data-stu-id="8f364-p107">Use the **Skip tagging** option only when necessary. Advanced eDiscovery does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="8f364-136">Даже файлы с очень небольшим объемом извлеченного текста должны быть помечены как R/НР, а не как "Skip", когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="8f364-136">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="8f364-137">РасСтановка тегов может повлиять на классификатор до тех пор, пока файл доступен для чтения и его можно пометить как R/НР.</span><span class="sxs-lookup"><span data-stu-id="8f364-137">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="8f364-138">Порядковый номер файла в списке отображаемых файлов на вкладке **тег** позволяет пользователю вернуться к исходному отображаемому порядку файлов.</span><span class="sxs-lookup"><span data-stu-id="8f364-138">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="8f364-p108">Вы можете вернуться к любому примеру и изменить маркировку файлов оценки и учебного набора. Изменения будут применены при создании следующего примера.</span><span class="sxs-lookup"><span data-stu-id="8f364-p108">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="8f364-141">ОтСканированные файлы Excel в формате PDF должны рассматриваться как собственные файлы Excel при разметке тегами файлов.</span><span class="sxs-lookup"><span data-stu-id="8f364-141">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="8f364-p109">Если у вас есть сомнения относительно тегов релевантности файла, ознакомьтесь со статьей эксперта. НеПравильное расстановка тегов во время обучения неСоответствия может привести к потере времени в процессе, а также может негативно повлиять на качество общих результатов.</span><span class="sxs-lookup"><span data-stu-id="8f364-p109">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="8f364-144">Ключевые слова, определенные в списках ключевых слов, будут отображаться в цветах, чтобы помочь пользователю определить релевантные файлы при разметке тегами.</span><span class="sxs-lookup"><span data-stu-id="8f364-144">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="8f364-p110">**ВычисленИе пакетов**: файлы, помеченные экспертом как R/НР, получат значение 0 или 100. Это относится к разметке, выполненным перед вычислением пакетов. Если эксперт переключился на неАктивное после выполнения пакетного вычисления и размечает маркировку этой ситуации, то новые баллы не будут 100/0ся, а исходнее.</span><span class="sxs-lookup"><span data-stu-id="8f364-p110">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="8f364-148">**Проблемы и режим выборки**: проблемы обычно отключаются при завершении работы над ними (проведено обучение по релевантности и выполнен пакетный пересчет), когда проблемы отменяются или когда другой пользователь работает над проблемами.</span><span class="sxs-lookup"><span data-stu-id="8f364-148">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="8f364-149">Этапы обучения</span><span class="sxs-lookup"><span data-stu-id="8f364-149">Steps in Relevance training</span></span>

<span data-ttu-id="8f364-p111">На вкладке **Отслеживание \> релевантНости** Расширенное обнаружение электронных данных содержит рекомендации относительно того, как продолжить обработку, со следующими действиями. Эти следствия описаны ниже, когда рекомендуется выполнить каждое из следующих действий в процессе обучения релевантности.</span><span class="sxs-lookup"><span data-stu-id="8f364-p111">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="8f364-152">Маркировка и продолжение маркировки: Проверка файлов и маркировка релевантности, выполненные экспертом для каждого файла и выпуска в рамках примера.</span><span class="sxs-lookup"><span data-stu-id="8f364-152">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="8f364-153">Результат: существующий пример должен быть помечен.</span><span class="sxs-lookup"><span data-stu-id="8f364-153">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="8f364-154">Оценка/продолжение оценки: включает начальную проверку релевантности с учетом регистра и предварительное представление релевантности заполнения файла, импортированного для текущего случая.</span><span class="sxs-lookup"><span data-stu-id="8f364-154">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="8f364-155">Результат: необходима дополнительная оценка или рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8f364-155">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="8f364-156">Обучение и продолжение обучения: процесс, в ходе которого расширенные функции обнаружения электронных данных изучены от эксперта, который размечает образцы файлов и получает возможность определять условия релевантности, относящиеся к каждой из них в контексте каждого случая.</span><span class="sxs-lookup"><span data-stu-id="8f364-156">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="8f364-157">Результат: для этой задачи требуется дополнительное обучение; Следующий пример следует создать и пометить тегами.</span><span class="sxs-lookup"><span data-stu-id="8f364-157">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="8f364-p112">Вычисление пакетов: процесс релевантности, в котором расширенные функции обнаружения электронных данных принимаются на этапе обучения и применяют его ко всему заполнению файла. Все файлы в релевантной группе файлов оцениваются по релевантности и имеют показатель релевантности.</span><span class="sxs-lookup"><span data-stu-id="8f364-p112">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="8f364-160">Результат: Эта ошибка вызвана, и можно выполнить пакетный пересчет.</span><span class="sxs-lookup"><span data-stu-id="8f364-160">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="8f364-161">При сопоставлении: релевантность указывает, что экспертная проверка и теги поЛучит пример файлов, выбранных из дополнительной загрузки файлов во время поэтапной загрузки.</span><span class="sxs-lookup"><span data-stu-id="8f364-161">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="8f364-162">Результат: была добавлена новая нагрузка, и для продолжения работы требуется дополнительное обновление.</span><span class="sxs-lookup"><span data-stu-id="8f364-162">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="8f364-163">Несогласованности тегов: процесс идентифицирует, с помощью расширенного алгоритма обнаружения электронных данных, несогласованности в процессе тегирования файлов, которые могут негативно повлиять на анализ.</span><span class="sxs-lookup"><span data-stu-id="8f364-163">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="8f364-164">Результат: в следующем примере будут содержаться файлы, помеченные в предыдущих примерах, и их маркировку необходимо выполнить повторно.</span><span class="sxs-lookup"><span data-stu-id="8f364-164">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="8f364-165">Классификатор обновлений: позволяет пользователю применять теги и изменения заполнения.</span><span class="sxs-lookup"><span data-stu-id="8f364-165">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="8f364-166">Результат: изменения тегов и заполнения могут быть применены без необходимости вручную запускать еще один пример.</span><span class="sxs-lookup"><span data-stu-id="8f364-166">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="8f364-167">На удержании: процесс обучения соответствия завершен.</span><span class="sxs-lookup"><span data-stu-id="8f364-167">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="8f364-168">Результат: в этой точке не обязательно должно быть обучение по релевантности.</span><span class="sxs-lookup"><span data-stu-id="8f364-168">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="8f364-169">Несмотря на то, что Расширенное обнаружение электронных данных рассказывает о рекомендуемых дальнейших действиях на разных стадиях, она также позволяет переходить между вкладками и страницами, а также делать варианты для решения проблем, которые могут быть отделоны с конкретным обращением, выпуску или процесс рецензирования документа.</span><span class="sxs-lookup"><span data-stu-id="8f364-169">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="8f364-p113">Можно принимать или переопределять дополнительные параметры обработки следующего этапа обнаружения электронных данных. Если вы хотите выполнить шаг, отличный от рекомендуемого, щелкните **следующий шаг** , приведенный в разделе Расширенная ошибка в диалоговом окне, нажмите кнопку **изменить** рядом с следующим шагом, а затем выберите другой параметр следующего шага.</span><span class="sxs-lookup"><span data-stu-id="8f364-p113">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8f364-172">Некоторые параметры могут быть отключены после снятия блокировки, так как они не поддерживаются в этой точке процесса.</span><span class="sxs-lookup"><span data-stu-id="8f364-172">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f364-173">См. также</span><span class="sxs-lookup"><span data-stu-id="8f364-173">See also</span></span>

[<span data-ttu-id="8f364-174">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8f364-174">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="8f364-175">Понимание оценки релевантности</span><span class="sxs-lookup"><span data-stu-id="8f364-175">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8f364-176">Маркировка и оценка</span><span class="sxs-lookup"><span data-stu-id="8f364-176">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8f364-177">РасСтановка тегов и релевантности</span><span class="sxs-lookup"><span data-stu-id="8f364-177">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8f364-178">Анализ релевантности отслеживания</span><span class="sxs-lookup"><span data-stu-id="8f364-178">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8f364-179">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="8f364-179">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8f364-180">Анализ релевантности тестирования</span><span class="sxs-lookup"><span data-stu-id="8f364-180">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

