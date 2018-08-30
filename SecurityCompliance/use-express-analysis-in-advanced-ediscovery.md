---
title: Использование экспресс-анализа в Office 365 Advanced eDiscovery
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Узнайте, как запустить режим анализа, экспресс-выпуск Microsoft Office 365 Advanced электронного обнаружения
ms.openlocfilehash: a71e6775b1116e805e455815dca53a727d887809
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534711"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="8ed18-103">Использование экспресс-анализа в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8ed18-103">Use Express Analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="8ed18-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="8ed18-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="8ed18-106">**Express анализа** можно использовать для быстрого анализа дела и экспортировать результаты.</span><span class="sxs-lookup"><span data-stu-id="8ed18-106">You can use **Express analysis** to quickly analyze a case and export the results.</span></span> 
  
<span data-ttu-id="8ed18-p102">Express анализа можно использовать для расчета рядом с дубликаты и отправьте потоков и вычисление тем. В диалоговом окне [Дополнительные параметры для анализа, экспресс-выпуск](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings)также можно задать определенные параметры для темы, подобия документов и файлов экспорта.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p102">You can use express analysis to calculate near-duplicates and email threads and calculate themes. You can also set certain parameters for themes, document similarity and the export files in the [Advanced settings for Express analysis](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span></span>
  
## <a name="run-express-analysis"></a><span data-ttu-id="8ed18-109">Выполните анализ, экспресс-выпуск</span><span class="sxs-lookup"><span data-stu-id="8ed18-109">Run Express analysis</span></span>

1. <span data-ttu-id="8ed18-110">На вкладке **Анализ, экспресс-выпуск** (1) выберите контейнер для включения ** Express анализа ** (2) и кнопки **Дополнительные параметры** .</span><span class="sxs-lookup"><span data-stu-id="8ed18-110">In the **Express analysis** (1) tab, select a container to enable the ** Express analysis ** (2), and **Advanced settings** buttons.</span></span> 
    
    ![Снимок экрана страницы анализа, экспресс-выпуск](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. <span data-ttu-id="8ed18-112">В разделе **Параметры анализа**:</span><span class="sxs-lookup"><span data-stu-id="8ed18-112">Under **Analyze parameters**:</span></span>
    
  - <span data-ttu-id="8ed18-p103">Если флажок установлен, **Вычисление рядом с дубликаты и электронной почты потоков** для выполнения анализа. Установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p103">Check **Calculate near-duplicates and email threads** if you want to run the analysis. It is selected by default.</span></span> 
    
  - <span data-ttu-id="8ed18-p104">Установите флажок **Вычисление тем** обработать все файлы и назначить их тем. Установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p104">Check **Calculate Themes** to process all files and assign themes to them. It is selected by default.</span></span> 
    
3. <span data-ttu-id="8ed18-117">В разделе **Место экспорта**:</span><span class="sxs-lookup"><span data-stu-id="8ed18-117">Under **Export destination**:</span></span>
    
  - <span data-ttu-id="8ed18-118">Проверьте, **Загрузите файл на локальном компьютере** можно загрузить на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="8ed18-118">Check **Download to local machine** to download to your local computer.</span></span> 
    
  - <span data-ttu-id="8ed18-119">Если проверьте **экспорта для пользовательских Azure больших двоичных объектов** можно также указать контейнер URL-адрес и SAS маркер.</span><span class="sxs-lookup"><span data-stu-id="8ed18-119">If you check **Export to user-defined Azure blob** then you can also specify a container URL and SAS token.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8ed18-p105">После пакета экспорта сохраняется, чтобы пользователем Azure больших двоичных объектов, данные больше не управляется расширенной обнаружения электронных данных. управляется Azure больших двоичных объектов. Это означает, что при удалении регистр, экспортированные файлы по-прежнему останется на Azure больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p105">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery. it is managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="8ed18-123">**Сохраните SAS маркер для будущего экспорта сеанса**: Если этот флажок установлен, маркер SAS шифруются в расширенной eDiscovery внутренней базы данных для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="8ed18-123">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8ed18-p106">В настоящее время SAS истечения срока действия маркера после месяца. При попытке загрузки после более чем месяца необходимо отменить последнего сеанса, затем экспортируйте еще раз.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p106">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
4. <span data-ttu-id="8ed18-126">Для запуска анализа express с по умолчанию параметры выберите **Express анализа**и будет отображаться на странице **состояния задач**</span><span class="sxs-lookup"><span data-stu-id="8ed18-126">To start the express analysis with default settings, choose **Express analysis**, and the **Task status** page will display</span></span> 
    
    <span data-ttu-id="8ed18-127">На странице " **состояние задачи** " можно развернуть **процесс**, **анализировать** и **Экспорт** вкладки для отображения сведений о выполнении, express.</span><span class="sxs-lookup"><span data-stu-id="8ed18-127">On the **Task status** page you can expand the **Process**, **Analyze** and **Export** tabs to display details about the express run.</span></span> 
    
    ![Снимок экрана расширенного eDiscovery, экспресс-выпуск анализа задач "состояние"](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. <span data-ttu-id="8ed18-129">Выбор страницы **Express анализа сводный** список подробные сведения о выполнении.</span><span class="sxs-lookup"><span data-stu-id="8ed18-129">Choose the **Express analysis summary** page to list detailed information about the run.</span></span> 
    
    <span data-ttu-id="8ed18-p107">В нижней части страницы **Express анализа сводки** нажмите кнопку **загрузить последнего сеанса** для загрузки tp анализа файлов локального компьютера. Сначала необходимо загрузить средство экспорта обнаружения электронных данных и вставьте ключ экспорта на средство экспорта обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p107">On the bottom of the **Express analysis summary** page, choose **Download last session** to download the analysis files tp your local computer. You will first have to download eDiscovery Export tool and paste the Export key to the eDiscovery Export tool.</span></span> 
    
## <a name="advanced-settings-for-express-analysis"></a><span data-ttu-id="8ed18-132">Дополнительные параметры для анализа, экспресс-выпуск</span><span class="sxs-lookup"><span data-stu-id="8ed18-132">Advanced settings for Express analysis</span></span>
<span data-ttu-id="8ed18-133"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="8ed18-133"></span></span>

<span data-ttu-id="8ed18-134">При необходимости можно настроить **Дополнительные параметры** для изменения параметров по умолчанию, экспресс-выпуск анализа.</span><span class="sxs-lookup"><span data-stu-id="8ed18-134">You can optionally set **Advanced settings** to change the default Express analysis parameters.</span></span> 
  
1. <span data-ttu-id="8ed18-135">В разделе **Анализ** :</span><span class="sxs-lookup"><span data-stu-id="8ed18-135">In the **Analyze** section:</span></span> 
    
  - <span data-ttu-id="8ed18-136">В **рядом с дубликаты и потоков электронной почты**введите значение **подобия документа** или примите значение по умолчанию 65%.</span><span class="sxs-lookup"><span data-stu-id="8ed18-136">In the **Near duplicates and email threads**, enter the **Document similarity** value, or accept the default of 65%.</span></span> 
    
  - <span data-ttu-id="8ed18-p108">В поле **Максимальное количество тем** введите или выберите значение для количества тем для создания. Значение по умолчанию равно 200.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p108">In the **Max number of themes** enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8ed18-p109">Увеличение числа тем влияет на производительность, а также возможность темы Подготовка к использованию. Чем больше число тем, большую детализацию эти атрибуты. Например, если набор 50 темы включают темы, такие как «Баскетбольная, данных стимулирует, Ножницы, Lakers»; 300 тем может включать отдельные тем: «Подстегивает», «Ножницы», «Lakers». Если бы не знают темы «Баскетбольная» и использовать эту функцию для ECA видеть темы «Баскетбольная» может быть полезна. Однако если обработки слишком много тем, никогда не может отображаться слово «Баскетбольная» и могут не знать данных стимулирует и Ножницы, хороший Баскетбольная тем для просмотра, а не загружается и используются для Сверхтонкая элементов, которые будут входить на.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p109">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
  - <span data-ttu-id="8ed18-p110">В **темах предлагаемые** выберите **Изменить** , чтобы предложить темы слова для управления тем обработки. Расширенные обнаружения электронных данных будет сосредоточиться на этих предложенного слов и попытаться создать один или несколько соответствующих темы на основе параметров «Максимальное количество темы».</span><span class="sxs-lookup"><span data-stu-id="8ed18-p110">In the **Suggested themes** choose **Modify** to suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="8ed18-p111">Например если предложенного слово «computer» и указанного «2» в качестве «максимальное количество темы», расширенные обнаружения электронных данных будет пытаться создать две темы, влияющие на слово «computer». Две темы может быть «компьютерного программного обеспечения» и «hardware компьютер», например.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p111">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span>
    
    ![Добавление предложенной темы](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - <span data-ttu-id="8ed18-149">**Режим** В раскрывающемся списке выберите вариант **темы** :</span><span class="sxs-lookup"><span data-stu-id="8ed18-149">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="8ed18-150">**Создание и применение модели**: вычисляет тем с моделями из сегмента файлов и затем распределяет файлы между ними.</span><span class="sxs-lookup"><span data-stu-id="8ed18-150">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="8ed18-p112">**Создать модель**: вычисляет модель тем для сегмента файлов. Применить процесс разделения файлов выполняется отдельно в другое время.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p112">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="8ed18-p113">**Применить модель**: этот параметр доступен только в том случае, если модель была создана ранее и еще не были применены. Это будет разделить файлы на основании тем.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p113">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
2. <span data-ttu-id="8ed18-155">В разделе **экспорта** :</span><span class="sxs-lookup"><span data-stu-id="8ed18-155">In the **Export** section:</span></span> 
    
1. <span data-ttu-id="8ed18-156">В **пакет экспортировать**:</span><span class="sxs-lookup"><span data-stu-id="8ed18-156">In the **Select export batch**:</span></span>
    
  - <span data-ttu-id="8ed18-157">В списке **Экспорт пакета** выберите имя пакета или экспортировать результаты в пакет экспорта 01 (пакет по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="8ed18-157">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="8ed18-p114">Чтобы экспортировать результаты для новых файлов, которые добавлены в существующий случай, продолжите текущего пакета. Для создания сеанса в пакете, выберите один и тот же номер пакета и нажмите кнопку **Создать Экспорт сеанса** этот параметр можно использовать для экспорта те же параметры предыдущей пакетного добавочного образом.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p114">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="8ed18-p115">Чтобы экспортировать в новый раздел, нажмите кнопку **Добавить**![добавить значок](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) и введите новое имя в поле **имя пакета** (или примите значение по умолчанию) и описание в **поле Описание пакета**. Нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p115">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="8ed18-162">Чтобы изменить имя пакета или описание, выберите имя в **пакет экспорта**, нажмите кнопку **Изменить** ![значок Правка](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)и затем изменить поля.</span><span class="sxs-lookup"><span data-stu-id="8ed18-162">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8ed18-p116">При запуске сеансов для экспорта партии их невозможно удалить. Кроме того можно изменять только некоторые параметры, после запуска первого сеанса.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p116">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="8ed18-165">Создание пакета повторяющихся экспорта, выберите **пакет экспорта повторяющихся**![создать значок пакета повторяющихся экспорта](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) и введите имя и описание для повторяющихся пакета на панели.</span><span class="sxs-lookup"><span data-stu-id="8ed18-165">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="8ed18-166">Чтобы удалить пакет экспорта, выберите команду **Удалить**![удалить значок пакета экспорта](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span><span class="sxs-lookup"><span data-stu-id="8ed18-166">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="8ed18-167">Чтобы просмотреть журнал пакет, выберите **Журнал пакетов**![значок представления журнала](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span><span class="sxs-lookup"><span data-stu-id="8ed18-167">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="8ed18-p117">В разделе Определение p **opulation:** выберите **включать только файлы, над показатель релевантности срока** и/или **Уточнение Экспорт пакета** , чтобы настроить параметры для вашего пакета экспорта. Если выбран параметр **Включить только файлы над прекращения показатель релевантности**, включено **проблему** , если показатель релевантности файла больше, чем показатель прекращения для выбранного проблемы, экспортируется файл. Файл будет экспортироваться, если не исключен по "Фильтр **для проверки** . При выборе **Уточнение Экспорт пакета**, а затем **отзыва Копировать** и **Filter by «К рассмотрению» поля** включены переключателей. При выборе **отзыва Копировать**, а затем дубликаты файлов будет иметь отфильтровано масштабированием согласно определена политика: [случае уровень (по умолчанию): из каждого набора повторяющихся файлов в случае всего лишь один файл будет отзыва duped. Уровень custodian: из каждого набора повторяющихся файлов же custodian только один файл будет отзыва duped. Запись всех повторяющихся файлов недоступна в выходных данных экспорта. Если выбрано поле **Filter by «для просмотра»** , выберите **изменить в разделе метаданные** , чтобы ввести настройки поля **«для просмотра»**. Выберите **Включить входных файлов**для включения исходных файлов в содержимое пакета. Может снять этот флажок, чтобы ускорить процесс экспорта. Обратите внимание, что собственные файлы будут экспортироваться в любом случае.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p117">Under Define p **opulation:** Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch. If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled, and if the file's relevance score is higher than the cut-off score for the selected issue, then the file is exported. The file will be exported unless it's excluded by the ' **For review** filter. If you select **Refine export batch**, then the **De-dupe** and **Filter by 'For review' field** radio buttons are enabled. If you choose **De-dupe**, then duplicates files will be filtered-out according to the policy defined: [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped. A record of all duplicate files is available in export output. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files**to include source files in the package content. You can clear this option to speed up the export process. Note that the Native files will be exported in any case.</span></span>
    
3. <span data-ttu-id="8ed18-179">В разделе **Определение метаданных**выберите из следующих вариантов в списке **Экспорт шаблона** (одно на сеанс).</span><span class="sxs-lookup"><span data-stu-id="8ed18-179">Under **Define metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="8ed18-p118">**Стандартный**: базовый набор элементов данных, метаданных и свойств. Используйте этот вариант, когда импорт данных уже было обработано в расширенной обнаружения электронных данных и загрузил Экспорт данных в системе, которая уже содержит файлы. По умолчанию Экспорт шаблона столбцы созданы и заполнены.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p118">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="8ed18-p119">**Все**: полный набор стандартных метаданных, включая все обработки данных, а также анализировать и релевантности показателям. Этот шаблон является обязательным при расширенной eDiscovery выполняет обработку и загрузке файлов данных для внешней системы в первый раз.</span><span class="sxs-lookup"><span data-stu-id="8ed18-p119">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="8ed18-185">**Проблемы**: выберите **Все проблемы** или выберите конкретную проблему создания.</span><span class="sxs-lookup"><span data-stu-id="8ed18-185">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
<span data-ttu-id="8ed18-186">Нажмите **кнопку ОК**, чтобы сохранить параметры, **Восстановить значения по умолчанию** для использования значения по умолчанию, или **Отмена** , чтобы отменить задание Дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="8ed18-186">Choose **OK**to save the advanced settings, **Restore defaults** to use default values, or **Cancel** to cancel setting the advanced settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ed18-187">См. также</span><span class="sxs-lookup"><span data-stu-id="8ed18-187">See also</span></span>
<span data-ttu-id="8ed18-188"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="8ed18-188"></span></span>

[<span data-ttu-id="8ed18-189">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8ed18-189">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)

