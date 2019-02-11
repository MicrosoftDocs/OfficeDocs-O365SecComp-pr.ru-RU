---
title: Использование модуля релевантности для анализа данных в расширенной обнаружения электронных данных (Предварительная версия)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 56e83a1f8a951fd6e14172122a5e86447c6f2ccf
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695175"
---
# <a name="use-the-relevance-module-to-analyze-data-in-advanced-ediscovery-preview"></a><span data-ttu-id="2fe83-102">Использование модуля релевантности для анализа данных в расширенной обнаружения электронных данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="2fe83-102">Use the Relevance module to analyze data in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="2fe83-p101">В расширенной обнаружения электронных данных (Предварительная версия) модуль релевантности содержит обзор файлы, относящиеся к обращению и учебный курс по релевантности. Рабочий процесс релевантности показано и описано, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="2fe83-p101">In Advanced eDiscovery (Preview), the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![Рабочий процесс определения релевантности](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="2fe83-106">**Циклы оценки и отслеживания**:</span><span class="sxs-lookup"><span data-stu-id="2fe83-106">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="2fe83-107">**Оценка**: включает первых оценки в случайном порядке примере файлов и применения решений для определения производительности упреждающий процесс написания кода с помощью этой оценки.</span><span class="sxs-lookup"><span data-stu-id="2fe83-107">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="2fe83-108">**Отслеживание**: вычисление и отображение промежуточных результатов оценки при отслеживании статистические действия в процессе.</span><span class="sxs-lookup"><span data-stu-id="2fe83-108">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="2fe83-109">**Циклы обучения и отслеживания**</span><span class="sxs-lookup"><span data-stu-id="2fe83-109">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="2fe83-110">**Тег**: расширенные обнаружения электронных данных (Просмотр) запоминает релевантности критерии для каждой проблемы на основании expert последовательной проверки и тегов отдельных файлов.</span><span class="sxs-lookup"><span data-stu-id="2fe83-110">**Tag**: Advanced eDiscovery (Preview) learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="2fe83-111">**Отслеживание**: вычисление и отображение промежуточных результатов учебный курс по релевантности при отслеживании статистические действия в процессе.</span><span class="sxs-lookup"><span data-stu-id="2fe83-111">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="2fe83-112">**Расчет пакета**: критерии релевантности накопленной и известных применяется к коллекции весь файл, а показатель релевантности, создается для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="2fe83-112">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="2fe83-113">**Решите**: результаты анализа, применяется для всего примера отображается после расчета пакета и отображаются данные, используемые для принятия решений рецензирования документов.</span><span class="sxs-lookup"><span data-stu-id="2fe83-113">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="2fe83-114">**Test**: проверка допустимости и эффективность обработки расширенных обнаружения электронных данных (Предварительная версия), можно проверить результаты.</span><span class="sxs-lookup"><span data-stu-id="2fe83-114">**Test**: Results can be tested to verify the validity and effectiveness of the Advanced eDiscovery (Preview) processing.</span></span>

- <span data-ttu-id="2fe83-115">**Поиск**: после завершения рабочего процесса релевантности выходные данные, например чтение процентиль документа можно использовать для своей проблеме при выполнении запроса в рабочее множество.</span><span class="sxs-lookup"><span data-stu-id="2fe83-115">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your working set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="2fe83-116">Рекомендации по релевантности обучения и рецензирование</span><span class="sxs-lookup"><span data-stu-id="2fe83-116">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="2fe83-117">Ниже приведен обзор рекомендаций по релевантности обучения и Повторение пройденного:</span><span class="sxs-lookup"><span data-stu-id="2fe83-117">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="2fe83-p102">**Ошибки и несоответствия**: Если тегов ошибки выполняются во время обучения, вернуться в предыдущих примерах по их устранению. Если существует слишком много ошибок или в новой точки зрения case или проблема, релевантности критерии следует переопределить администратором и перезапустить учебный курс по релевантности.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p102">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="2fe83-120">**Тегов и обучающие материалы**:</span><span class="sxs-lookup"><span data-stu-id="2fe83-120">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="2fe83-p103">Файлы следует тегами на основе только содержимого. Необходимо учитывать метаданных, например custodian, даты или путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p103">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="2fe83-123">Не следует учитывать даты показания индикатора диапазон текста при тегов файлы.</span><span class="sxs-lookup"><span data-stu-id="2fe83-123">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="2fe83-124">Не следует учитывать встроенные графические изображения при тегов файлы.</span><span class="sxs-lookup"><span data-stu-id="2fe83-124">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="2fe83-p104">Пропуск текста, применяемые к релевантности будут удалены в содержимое файла отображаемых в представлении текста в релевантности. Если значения для текста игнорировать определены после релевантности, уже обучение приступить к работе, новый игнорируемыми текст будет применяться к примеры файлов, созданных из точки, в которой он был определен. Функцию игнорировать текст должен использоваться с осторожностью, как его использование может снизить производительность анализ файла</span><span class="sxs-lookup"><span data-stu-id="2fe83-p104">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="2fe83-p105">Параметр **Пропустить тегов** только при необходимости. Расширенные обнаружения электронных данных (Просмотр) не обучение пользователей на основе на пропущенных файлов. В оценки, если это трудно определить, является ли файл относится лучше тег как Relevant (R) или нет соответствующих (NR) каждый раз, когда это возможно, вместо выбора **Пропустить**. При расширенной обнаружения электронных данных (Просмотр) оценивает обучения, его будут видны насколько обработки этих типов файлов.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p105">Use the **Skip tagging** option only when necessary. Advanced eDiscovery (Preview) does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery (Preview) evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="2fe83-132">Даже файлы с очень небольшое количество извлеченный текст должен тегами в учебный курс по как R/NR, а не как «Пропустить», когда это возможно.</span><span class="sxs-lookup"><span data-stu-id="2fe83-132">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="2fe83-133">Тегов могут влиять классификатор, поскольку файл доступен для чтения и может быть помечена как R/NR.</span><span class="sxs-lookup"><span data-stu-id="2fe83-133">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="2fe83-134">Порядковый номер файла на отображаемой образца списка файлов на вкладке **тег** пользователь может вернуться к исходной отображаемой порядок файлов.</span><span class="sxs-lookup"><span data-stu-id="2fe83-134">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="2fe83-p106">Можно вернуться к любой образца и изменить тегов оценки и обучающего набора файлов. Изменения будут применяться при создании в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p106">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="2fe83-137">Поиска Excel, файлы в формате PDF следует обрабатывается так же, как файлы в формате Excel при тегов файлы.</span><span class="sxs-lookup"><span data-stu-id="2fe83-137">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="2fe83-p107">При работе в сомнения по релевантности тегов файла, обратитесь к специалисту. Неправильные маркировки во время обучения релевантности может привести к потере времени позднее в процессе и также может содержать отрицательное влияние на качество общие результаты.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p107">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="2fe83-140">Ключевые слова, которые были определены в ключевое слово списков будет отображаться в цвета и позволяющая пользователю определить необходимые файлы во время добавления тегов.</span><span class="sxs-lookup"><span data-stu-id="2fe83-140">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="2fe83-p108">**Расчет пакета**: файлы, которые были добавлены как R/NR с эксперт будет получать балл 0 или 100. Это относится к тегов до пакета вычислений. Если эксперт переключение проблему Idle после расчета пакета и продолжение тегов эту проблему, недавно с тегами показатели не будут 100/0, но вместо исходного счета.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p108">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="2fe83-144">**Проблемы и выборки режим**: проблемы отключены как правило, после завершения работы над ними (стабилизироваться релевантности обучение и выполнить расчет пакета), при отмене проблем, или когда другой пользователь работает вопросы.</span><span class="sxs-lookup"><span data-stu-id="2fe83-144">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="2fe83-145">Действия, описанные в учебный курс по релевантности</span><span class="sxs-lookup"><span data-stu-id="2fe83-145">Steps in Relevance training</span></span>

<span data-ttu-id="2fe83-p109">В **релевантности \> отслеживание** вкладки, расширенные eDiscovery рекомендации о том, как перейти в обработку с следующие шаги. Ниже описаны последствия, при каждой из следующих действий рекомендуется в процессе учебный курс по релевантности.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p109">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="2fe83-148">Маркировки / Continue тегов: Обзор файлов и релевантности тегов, выполняемой expert для каждого файла и выдача внутри примера.</span><span class="sxs-lookup"><span data-stu-id="2fe83-148">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="2fe83-149">Импликации: Существующий пример должен помечен.</span><span class="sxs-lookup"><span data-stu-id="2fe83-149">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="2fe83-150">Оценка / Continue оценки: включает первых проверки релевантности делами проблемы и предварительный просмотр релевантности заполнения файла импорта для текущего варианта.</span><span class="sxs-lookup"><span data-stu-id="2fe83-150">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="2fe83-151">Импликации: Дополнительные оценки — это требуется и не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2fe83-151">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="2fe83-152">Учебный курс / Continue обучение: процесс, во время которых дополнительно eDiscovery запоминает из expert кто тегов файл образцы и получает возможность определения критериев релевантности, относящихся к каждой проблемы в контексте каждого варианта.</span><span class="sxs-lookup"><span data-stu-id="2fe83-152">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="2fe83-153">Импликации: Проблему должно Дополнительные обучающие материалы; в следующем примере должен быть создан и с меткой.</span><span class="sxs-lookup"><span data-stu-id="2fe83-153">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="2fe83-p110">Пакетная вычислений: процесс релевантности в какой Дополнительно eDiscovery принимает базы знаний, полученные на этапе обучения и применяется для заполнения весь файл. Все файлы в группе соответствующие файл оценки соответствия и назначен показатель релевантности.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p110">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="2fe83-156">Импликации: Стабилизироваться проблему, а можно выполнить расчет пакета.</span><span class="sxs-lookup"><span data-stu-id="2fe83-156">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="2fe83-157">Захват: Релевантности указывает, когда эксперт дается обзор и теги пример файлов, выбранных с нагрузки дополнительных файлов во время развертывания загружает сценарий.</span><span class="sxs-lookup"><span data-stu-id="2fe83-157">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="2fe83-158">Импликации: Добавлен новый нагрузки и захват является обязательным для продолжения работы.</span><span class="sxs-lookup"><span data-stu-id="2fe83-158">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="2fe83-159">Установка метки несоответствия: процесс идентифицирует через алгоритм расширенной eDiscovery несоответствий в файле тегов процесс, который может отрицательно сказаться на анализа.</span><span class="sxs-lookup"><span data-stu-id="2fe83-159">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="2fe83-160">Импликации: В следующем примере будет содержать файлы, которые были с тегами в предыдущих примерах, и их тегов должны быть выполнены повторно.</span><span class="sxs-lookup"><span data-stu-id="2fe83-160">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="2fe83-161">Обновление классификатора: пользователь может применить тегов или заполнения изменения.</span><span class="sxs-lookup"><span data-stu-id="2fe83-161">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="2fe83-162">Импликации: Тегов и заполнения изменения могут применяться без необходимости вручную запустите другой пример релевантности.</span><span class="sxs-lookup"><span data-stu-id="2fe83-162">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="2fe83-163">При удержании: завершения процесса учебный курс по релевантности.</span><span class="sxs-lookup"><span data-stu-id="2fe83-163">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="2fe83-164">Импликации: Нет учебный курс по релевантности необходим на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="2fe83-164">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="2fe83-165">Несмотря на то, что расширенные обнаружения электронных данных помогает выполнить процесс, с рекомендуется дальнейшие действия на разных этапах, также можно переходить между вкладок и страницы и задавать параметры для устранения проблемы, которые, возможно, относящихся к отдельным случая, проблема, или процесс проверки документа.</span><span class="sxs-lookup"><span data-stu-id="2fe83-165">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="2fe83-p111">Можно принять или override следующим шагом расширенной eDiscovery обработки вариантов. Если вы хотите выполните действие, отличный от действия, нажмите кнопку **Следующий шаг** списка отображения расширенной проблема в диалоговом окне, нажмите кнопку **Изменить** , рядом с полем следующим шагом и выберите другой параметр Следующий шаг.</span><span class="sxs-lookup"><span data-stu-id="2fe83-p111">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2fe83-168">Некоторые параметры могут оставаться отключенных после разблокирования как они не поддерживаются для использования на этом этапе процесса.</span><span class="sxs-lookup"><span data-stu-id="2fe83-168">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="2fe83-169">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="2fe83-169">More information</span></span>

[<span data-ttu-id="2fe83-170">Общие сведения об оценке в релевантности</span><span class="sxs-lookup"><span data-stu-id="2fe83-170">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2fe83-171">Теги и оценки</span><span class="sxs-lookup"><span data-stu-id="2fe83-171">Tagging and Assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2fe83-172">Теги и учебный курс по релевантности</span><span class="sxs-lookup"><span data-stu-id="2fe83-172">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2fe83-173">Отслеживание анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="2fe83-173">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2fe83-174">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="2fe83-174">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="2fe83-175">Тестирование анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="2fe83-175">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="2fe83-176">Запросов в рабочий набор</span><span class="sxs-lookup"><span data-stu-id="2fe83-176">Query within working set</span></span>](working-set-search.md)
