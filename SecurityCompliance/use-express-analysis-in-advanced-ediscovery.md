---
title: Использование экспресс-анализа в Office 365 Advanced eDiscovery
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Узнайте, как запустить режим Экспресс Analysis в Office 365 Advanced eDiscovery
ms.openlocfilehash: e306aa03962c646ce4083b7385e527b523e86fd6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217629"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="6e5f5-103">Использование экспресс-анализа в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6e5f5-103">Use Express Analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="6e5f5-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="6e5f5-106">С помощью **Express Analysis** можно быстро проанализировать обращение и экспортировать результаты.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-106">You can use **Express analysis** to quickly analyze a case and export the results.</span></span> 
  
<span data-ttu-id="6e5f5-p102">С помощью Express Analysis можно рассчитать почти повторяющиеся и почтовые потоки и вычислить темы. Вы также можете задать определенные параметры для тем, подобия документа и файлов экспорта в [дополнительных параметрАх Express Analysis](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p102">You can use express analysis to calculate near-duplicates and email threads and calculate themes. You can also set certain parameters for themes, document similarity and the export files in the [Advanced settings for Express analysis](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span></span>
  
## <a name="run-express-analysis"></a><span data-ttu-id="6e5f5-109">Выполнение экспресс – анализа</span><span class="sxs-lookup"><span data-stu-id="6e5f5-109">Run Express analysis</span></span>

1. <span data-ttu-id="6e5f5-110">На вкладке **Экспресс-анализ** (1) выберите контейнер, чтобы включить кнопки \* \* Express Analysis \* \* (2) и **Advanced Settings (дополнительные параметры** ).</span><span class="sxs-lookup"><span data-stu-id="6e5f5-110">In the **Express analysis** (1) tab, select a container to enable the \*\* Express analysis \*\* (2), and **Advanced settings** buttons.</span></span> 
    
    ![Снимок экрана: страница "Экспресс-анализ"](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. <span data-ttu-id="6e5f5-112">В разделе **Анализ параметров**:</span><span class="sxs-lookup"><span data-stu-id="6e5f5-112">Under **Analyze parameters**:</span></span>
    
  - <span data-ttu-id="6e5f5-p103">Установите флажок **рассчитать почти повторяющиеся и почтовые потоки** , если вы хотите запустить анализ. Он установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p103">Check **Calculate near-duplicates and email threads** if you want to run the analysis. It is selected by default.</span></span> 
    
  - <span data-ttu-id="6e5f5-p104">Проверьте **темы** , чтобы обработать все файлы и назначить им темы. Он установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p104">Check **Calculate Themes** to process all files and assign themes to them. It is selected by default.</span></span> 
    
3. <span data-ttu-id="6e5f5-117">В разделе **назначение экспорта**:</span><span class="sxs-lookup"><span data-stu-id="6e5f5-117">Under **Export destination**:</span></span>
    
  - <span data-ttu-id="6e5f5-118">Проверьте **загрузку на локальный** компьютер, чтобы скачать его на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-118">Check **Download to local machine** to download to your local computer.</span></span> 
    
  - <span data-ttu-id="6e5f5-119">Если вы установите флажок **экспортировать в Пользовательский BLOB-объект Azure** , вы также можете указать URL-адрес контейнера и маркер SAS.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-119">If you check **Export to user-defined Azure blob** then you can also specify a container URL and SAS token.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6e5f5-p105">После того как пакет экспорта будет сохранен в определенном пользователем большом двоичном объекте Azure, данные не будут больше управляться с помощью расширенного обнаружения электронных данных. Он управляется BLOB-объектом Azure. Это означает, что при удалении такого случая экспортированные файлы останутся в большом двоичном объекте Azure.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p105">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery. it is managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="6e5f5-123">**Сохранить маркер SAS для следующего сеанса экспорта**: Если этот флажок установлен, маркер SAS будет зашифрован в дополнительной базе данных расширенного обнаружения электронных данных для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-123">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6e5f5-p106">В настоящее время срок действия маркера SAS истечет через месяц. Если вы попытаетесь скачать его через несколько месяцев, необходимо отменить последний сеанс, а затем снова выполнить экспорт.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p106">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
4. <span data-ttu-id="6e5f5-126">Чтобы запустить Экспресс-анализ с параметрами по умолчанию, нажмите **Экспресс-анализ**, а на странице " **состояние задачи** " отображается</span><span class="sxs-lookup"><span data-stu-id="6e5f5-126">To start the express analysis with default settings, choose **Express analysis**, and the **Task status** page will display</span></span> 
    
    <span data-ttu-id="6e5f5-127">На странице " **состояние задачи** " можно развернуть вкладки **процесс**, **анализ** и **Экспорт** , чтобы отобразить подробные сведения о запуске Express.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-127">On the **Task status** page you can expand the **Process**, **Analyze** and **Export** tabs to display details about the express run.</span></span> 
    
    ![Снимок экрана с расширенной страницей состояния задач анализа обнаружения электронных данных Express](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. <span data-ttu-id="6e5f5-129">Чтобы получить подробные сведения о запуске, выберите страницу **сводный отчет Express Analysis** .</span><span class="sxs-lookup"><span data-stu-id="6e5f5-129">Choose the **Express analysis summary** page to list detailed information about the run.</span></span> 
    
    <span data-ttu-id="6e5f5-p107">В нижней части страницы **сводный анализ для анализа** выберите **загрузить последний сеанс** , чтобы скачать файлы анализа TP локального компьютера. Сначала необходимо скачать средство экспорта обнаружения электронных данных и вставить ключ экспорта в средство экспорта eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p107">On the bottom of the **Express analysis summary** page, choose **Download last session** to download the analysis files tp your local computer. You will first have to download eDiscovery Export tool and paste the Export key to the eDiscovery Export tool.</span></span> 
    
## <a name="advanced-settings-for-express-analysis"></a><span data-ttu-id="6e5f5-132">Дополнительные параметры для экспресс – анализа</span><span class="sxs-lookup"><span data-stu-id="6e5f5-132">Advanced settings for Express analysis</span></span>
<span data-ttu-id="6e5f5-133"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="6e5f5-133"></span></span>

<span data-ttu-id="6e5f5-134">При необходимости можно задать **Дополнительные параметры** , чтобы изменить параметры по умолчанию Express Analysis.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-134">You can optionally set **Advanced settings** to change the default Express analysis parameters.</span></span> 
  
1. <span data-ttu-id="6e5f5-135">В разделе **анализ** :</span><span class="sxs-lookup"><span data-stu-id="6e5f5-135">In the **Analyze** section:</span></span> 
    
  - <span data-ttu-id="6e5f5-136">В **ближайшем дубликатах и потоках электронной почты**введите значение **подобия документа** или примите значение по умолчанию 65%.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-136">In the **Near duplicates and email threads**, enter the **Document similarity** value, or accept the default of 65%.</span></span> 
    
  - <span data-ttu-id="6e5f5-p108">В поле **Максимальное число тем** введите или выберите значение для количества создаваемых тем. Значение по умолчанию — 200.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p108">In the **Max number of themes** enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6e5f5-p109">Увеличение числа тем влияет на производительность, а также на возможность обобщения темы. Чем больше количество тем, тем больше их детализация. Например, если в наборе 50 тем есть тема, например "Баскетбалл, Спурс, обтравочные части, Лакерс"; 300 темы могут включать в себя отдельные темы: "Спурс", "обтравочные отделы", "Лакерс". Если у вас нет сведений о теме "Баскетбалл" и эта функция не используется для ЕКА, то, возможно, будет полезна тема "Баскетбалл". Но если в обработке слишком много тем, слово "Баскетбалл" может оказаться недоступным, и оно может не знать о том, что Спурс и отРезки хорошо подходят Баскетбалл темы для проверки, а не элементы, которые переходят на загрузку и используют для перекрестия.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p109">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
  - <span data-ttu-id="6e5f5-p110">В **предложенных темах** выберите **изменить** , чтобы предложить слова темы для управления обработкой тем. Расширенное обнаружение электронных данных позволяет сосредоточиться на этих предложенных словах и попытаться создать одну или несколько релевантных тем на основе параметров "максимальное количество тем".</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p110">In the **Suggested themes** choose **Modify** to suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="6e5f5-p111">Например, если предлагаемое слово "Computer" и вы указали "2" как "максимальное количество тем", Расширенное обнаружение электронных данных попытается создать две темы, которые относятся к слову "Computer". Эти две темы могут быть "программным обеспечением компьютера" и "компьютерным аппаратным обеспечением", например.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p111">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span>
    
    ![Добавление предложенной темы](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - <span data-ttu-id="6e5f5-149">**Режим** В раскрывающемся списке выберите **темы** :</span><span class="sxs-lookup"><span data-stu-id="6e5f5-149">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="6e5f5-150">**Create and Apply Model**: вычисляет темы по моделям из сегмента файлов, а затем распространяет файлы между ними.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-150">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="6e5f5-p112">**CREATE Model**: вычисляет модель тем из сегмента файлов. Процесс применения разделения файлов выполняется отдельно в другое время.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p112">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="6e5f5-p113">**Apply Model**: этот параметр отображается только в том случае, если модель была создана ранее и еще не применена. Это позволит разделить файлы на основе тем.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p113">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
2. <span data-ttu-id="6e5f5-155">В разделе **Export (экспорт** ):</span><span class="sxs-lookup"><span data-stu-id="6e5f5-155">In the **Export** section:</span></span> 
    
1. <span data-ttu-id="6e5f5-156">В **разделе Выбор экспорта**выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6e5f5-156">In the **Select export batch**:</span></span>
    
  - <span data-ttu-id="6e5f5-157">В списке **Экспорт пакета** выберите имя пакета или результаты экспорта для экспорта пакет 01 (пакет по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="6e5f5-157">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="6e5f5-p114">Чтобы экспортировать результаты для новых файлов, добавленных к существующему случаю, перейдите к текущему пакету. Чтобы создать сеанс в пакете, выберите один и тот же номер пакета и нажмите кнопку **создать сеанс экспорта** . Этот параметр позволяет экспортировать те же параметры, что и в предыдущем пакете, в добавочном режиме.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p114">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="6e5f5-p115">Чтобы экспортировать в новый пакет, нажмите **Добавить**![значок](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) добавить и введите новое имя в поле **имя раздела** (или оставьте значение по умолчанию) и описание в поле **Описание пакета**. Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p115">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="6e5f5-162">Чтобы изменить имя или описание раздела, выберите имя в **разделе Export Batch**, нажмите **изменить** ![значок](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png)редактирования, а затем измените поля.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-162">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6e5f5-p116">После выполнения сеансов для пакета экспорта их невозможно удалить. Кроме того, после запуска первого сеанса можно изменить только некоторые параметры.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p116">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="6e5f5-165">Чтобы создать дубликат пакета экспорта, выберите команду **дублировать экспортируемый пакет**![создать дублирующийся значок](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) пакета экспорта и введите имя и описание для повторяющегося пакета в панели.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-165">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="6e5f5-166">Чтобы удалить пакет экспорта, нажмите кнопку **Удалить**![, чтобы удалить значок](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)экспорта пакета.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-166">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="6e5f5-167">Чтобы просмотреть историю пакета, щелкните значок![](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)истории просмотра **журнала пакетов**.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-167">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="6e5f5-p117">В разделе define p **опулатион:** установите флажок **включать только те файлы** , которые выводятся по сравнению с нерелевантностью и/или **уточнение экспортируемого пакета** , если необходимо настроить параметры для пакета экспорта. Если выбран параметр **включить только те файлы**, которые находятся в выпадающем списке со значением релевантности, то эта **Ошибка** включена, и если показатель релевантности файла выше, чем значение вырезкие для выбранного вопроса, то файл экспортируется. Файл будет экспортирован, если он не исключен фильтром " **для проверки** ". Если выбран параметр "подБирать **пакет экспорта**", то переключатели переключателя " **de – копия** " и "Фильтрация" будут включены для переключателей **"для проверки"** . Если выбрано значение **de-копия**, то дубликаты файлов будут фильтроваться в соответствии с заданной политикой: [уровень вариантов (по умолчанию): из каждого набора дубликатов файлов во всем случае все файлы, кроме одного, будут передаваться в дупед. Уровень хранитель: из каждого набора повторяющихся файлов одного и того же Хранитель все файлы, кроме одного, будут находиться в дупед. Запись всех повторяющихся файлов доступна в выходных данных экспорта. Если выбрано поле **Filter by to Review** , выберите **изменить в разделе Метаданные** , чтобы ввести параметры поля **"для просмотра"**. Выберите **включить входные файлы**, чтобы включить исходные файлы в содержимое пакета. Вы можете снять этот флажок, чтобы ускорить процесс экспорта. Обратите внимание на то, что собственные файлы будут экспортированы в любом случае.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p117">Under Define p **opulation:** Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch. If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled, and if the file's relevance score is higher than the cut-off score for the selected issue, then the file is exported. The file will be exported unless it's excluded by the ' **For review** filter. If you select **Refine export batch**, then the **De-dupe** and **Filter by 'For review' field** radio buttons are enabled. If you choose **De-dupe**, then duplicates files will be filtered-out according to the policy defined: [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped. A record of all duplicate files is available in export output. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files**to include source files in the package content. You can clear this option to speed up the export process. Note that the Native files will be exported in any case.</span></span>
    
3. <span data-ttu-id="6e5f5-179">В разделе **Определение метаданных**выберите один из следующих вариантов в списке **Экспорт шаблона** (один раз для каждого сеанса).</span><span class="sxs-lookup"><span data-stu-id="6e5f5-179">Under **Define metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="6e5f5-p118">**Стандартный**: базовый набор элементов данных, метаданных и свойств. Используйте этот параметр, если импорт данных уже был обработан во время расширенного обнаружения электронных данных, а экспорт данных отправлен в систему, которая уже содержит эти файлы. По умолчанию создаются и заполняются столбцы экспорта шаблонов.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p118">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="6e5f5-p119">**ALL**: полный набор стандартных метаданных, включая все обрабатываемые данные, а также результаты анализа и релевантности. Этот шаблон необходим, когда Расширенное обнаружение электронных данных выполняет обработку и передачу данных файлов во внешнюю систему в первый раз.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-p119">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="6e5f5-185">**Проблемы**: выберите **все проблемы** или выберите созданную вами задачу.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-185">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
<span data-ttu-id="6e5f5-186">Нажмите кнопку **ОК**, чтобы сохранить дополнительные параметры, **восстановить** значения по умолчанию, чтобы использовать значения по умолчанию, или **Отмена** , чтобы отменить установку дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="6e5f5-186">Choose **OK**to save the advanced settings, **Restore defaults** to use default values, or **Cancel** to cancel setting the advanced settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e5f5-187">См. также</span><span class="sxs-lookup"><span data-stu-id="6e5f5-187">See also</span></span>
<span data-ttu-id="6e5f5-188"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="6e5f5-188"></span></span>

[<span data-ttu-id="6e5f5-189">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6e5f5-189">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)

