---
title: Фильтрация данных при импорте PST-файлов в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Используйте новую интеллектуальную функцию импорта в службе импорта Office 365, чтобы отфильтровать элементы, которые фактически импортируются в целевые почтовые ящики. Интеллектуальный импорт позволяет определять, какие данные импортировать и что следует оставить позади. С помощью интеллектуального импорта также можно получить подробные сведения о данных, импортируемых в Office 365. '
ms.openlocfilehash: 6091f6cca75bffbb05bcd59f70cfae0dbdcb9040
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30297072"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a><span data-ttu-id="d0c09-105">Фильтрация данных при импорте PST-файлов в Office 365</span><span class="sxs-lookup"><span data-stu-id="d0c09-105">Filter data when importing PST files to Office 365</span></span>

<span data-ttu-id="d0c09-p102">Используйте новый компонент интеллектуального импорта в службе импорта Office 365, чтобы отфильтровать элементы в PST-файлах, которые фактически импортируются в целевые почтовые ящики. Вот как это работает:</span><span class="sxs-lookup"><span data-stu-id="d0c09-p102">Use the new Intelligent Import feature in the Office 365 Import service to filter the items in PST files that actually get imported to the target mailboxes. Here's how it works:</span></span>
  
- <span data-ttu-id="d0c09-108">После создания и отправки задания импорта PST-файлов в область хранилища Azure в облаке Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d0c09-108">After you create and submit a PST import job, PST files are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
    
- <span data-ttu-id="d0c09-109">Office 365 анализирует данные в PST-файлах безопасным и безопасным способом, определяя возраст элементов почтового ящика и различные типы сообщений, включенные в PST-файлы.</span><span class="sxs-lookup"><span data-stu-id="d0c09-109">Office 365 analyzes the data in the PST files, in a safe and secure manner, by identifying the age of the mailbox items and the different message types included in the PST files.</span></span>
    
- <span data-ttu-id="d0c09-p103">После завершения анализа и данных, готовых к импорту, можно импортировать все данные в PST-файлах как есть или обрезать импортируемые данные, задав фильтры, которые контролируют, какие данные следует импортировать. Например, можно выбрать один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="d0c09-p103">When the analysis is complete and the data is ready to import, you have the option to import all data in the PST files as is or trim the data that's imported by setting filters that control what data gets imported. For example, you can choose to:</span></span>
    
  - <span data-ttu-id="d0c09-112">Импортировать только элементы определенного возраста.</span><span class="sxs-lookup"><span data-stu-id="d0c09-112">Import only items of a certain age.</span></span>
    
  - <span data-ttu-id="d0c09-113">Импорт выбранных типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="d0c09-113">Import selected message types.</span></span>
    
  - <span data-ttu-id="d0c09-114">Исключение сообщений, отправленных или полученных определенными пользователями.</span><span class="sxs-lookup"><span data-stu-id="d0c09-114">Exclude messages sent or received by specific people.</span></span>
    
- <span data-ttu-id="d0c09-115">После настройки параметров фильтра Office 365 импортирует только те данные, которые соответствуют критериям фильтрации, с целевыми почтовыми ящиками, указанными в задании импорта.</span><span class="sxs-lookup"><span data-stu-id="d0c09-115">After you configure the filter settings, Office 365 imports only the data that meets the filtering criteria to the target mailboxes specified in the import job.</span></span>
    
<span data-ttu-id="d0c09-116">На приведенном ниже рисунке показан процесс интеллектуального импорта, в котором выделены выполняемые задачи и задачи, выполняемые в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d0c09-116">The following graphic shows the Intelligent Import process, and highlights the tasks you perform and the tasks performed by Office 365.</span></span>
  
![Интеллектуальный процесс импорта в Office 365](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a><span data-ttu-id="d0c09-118">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="d0c09-118">Before you begin</span></span>

- <span data-ttu-id="d0c09-p104">Действия, описанные в этом разделе, предполагают, что вы создали задание импорта PST в службе импорта Office 365, используя отправку по сети или доставку дисков. Пошаговые инструкции представлены в одном из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="d0c09-p104">The steps in this topic assume that you've created a PST import job in the Office 365 Import service by using network upload or drive shipping. For step-by-step instructions, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="d0c09-121">Импорт PST-файлов в Office 365 с помощью отправки по сети</span><span class="sxs-lookup"><span data-stu-id="d0c09-121">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
    
  - [<span data-ttu-id="d0c09-122">Импорт PST-файлов в Office 365 с помощью отправки дисков</span><span class="sxs-lookup"><span data-stu-id="d0c09-122">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- <span data-ttu-id="d0c09-p105">После создания задания импорта с помощью команды "Отправка по сети" состояние задания импорта на странице "Импорт" в центре соответствия требованиям безопасности &amp; Office 365 — " **выполняется анализ**", что означает, что Office 365 анализирует данные в PST-файлах, которые вы отправляет. Нажмите \*\*\*\*![кнопку обновить](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) обновление, чтобы обновить состояние задания импорта.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p105">After you create an import job by using network upload, the status for the import job on the Import page in Office 365 Security &amp; Compliance Center is set to **Analysis in progress**, which means that Office 365 is analyzing the data in the PST files that you uploaded. Click **Refresh**![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) to update the status for the import job.</span></span> 
    
- <span data-ttu-id="d0c09-125">Для заданий импорта доставки дисков данные анализируются в Office 365 после того, как сотрудники центра обработки данных Майкрософт получат жесткий диск и отправит PST-файлы в область хранилища Azure для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="d0c09-125">For drive shipping import jobs, the data will be analyzed by Office 365 after Microsoft data center personnel receive your hard drive and upload the PST files to the Azure storage area for your organization.</span></span>
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a><span data-ttu-id="d0c09-126">Фильтрация данных, которые импортируются в почтовые ящики</span><span class="sxs-lookup"><span data-stu-id="d0c09-126">Filter data that gets imported to mailboxes</span></span>

<span data-ttu-id="d0c09-127">После создания задания импорта PST-файла выполните следующие действия, чтобы отфильтровать данные перед их импортом в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d0c09-127">After you've created a PST import job, follow these steps to filter the data before you import it to Office 365.</span></span>
  
1. <span data-ttu-id="d0c09-128">Перейдите к [https://protection.office.com/](https://protection.office.com/) учетной записи администратора в организации Office 365 и войдите в нее, используя учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="d0c09-128">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="d0c09-129">в левой области &amp; центра безопасности Office 365 щелкните **импорт** **данных** \> .</span><span class="sxs-lookup"><span data-stu-id="d0c09-129">In the left pane of the Office 365 Security &amp; Compliance Center, click **Data governance** \> **Import**.</span></span>
    
    <span data-ttu-id="d0c09-p106">Задания импорта для Организации перечислены на странице " **Импорт** ". Обратите внимание, что в столбце **состояние** завершено значение **анализ** указывает, что задания импорта были проанализированы в Office 365 и готовы к импорту.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p106">The import jobs for your organization are listed on the **Import** page. Note that the **Analysis completed** value in the **Status** column indicates the import jobs that have been analyzed by Office 365 and are ready for you to import.</span></span> 
    
    ![Состояние завершения анализа указывает, что Office 365 проанализировал данные в PST-файлах](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. <span data-ttu-id="d0c09-133">Нажмите кнопку **Готово, чтобы импортировать в Office 365** для задания импорта, которое требуется выполнить.</span><span class="sxs-lookup"><span data-stu-id="d0c09-133">Click **Ready to import to Office 365** for the import job that you want to complete.</span></span> 
    
    <span data-ttu-id="d0c09-134">Отобразится страница вылет со сведениями о PST-файлах и других сведениях о задании импорта.</span><span class="sxs-lookup"><span data-stu-id="d0c09-134">A fly out page is displayed with information about the PST files and other information about the import job.</span></span>
    
4. <span data-ttu-id="d0c09-135">Нажмите кнопку **Импорт в Office 365**.</span><span class="sxs-lookup"><span data-stu-id="d0c09-135">Click **Import to Office 365**.</span></span>
    
    <span data-ttu-id="d0c09-p107">Отобразится страница " **Фильтрация данных** ". Он содержит сведения о данных в PST-файлах для задания импорта, в том числе сведения о сроке хранения данных.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p107">The **Filter your data** page is displayed. It contains data insights about the data in the PST files for the import job, including information about the age of the data.</span></span> 
    
    ![На странице фильтра данных отображается информация о PST-файлах для задания импорта](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. <span data-ttu-id="d0c09-139">В зависимости от того, хотите ли вы обрезать данные, импортированные в Office 365, в разделе **для фильтрации данных**выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="d0c09-139">Based on whether or not you want to trim the data that's imported to Office 365, under **Do you want to filter your data?**, do one of the following:</span></span>
    
    <span data-ttu-id="d0c09-p108">о. Щелкните **Да, я хочу отфильтровать его перед импортом** , чтобы обрезать импортируемые данные, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p108">a. Click **Yes, I want to filter it before importing** to trim the data that you import, and then click **Next**.</span></span>
    
    <span data-ttu-id="d0c09-142">На странице **Импорт данных в office 365** отображается подробная информация об анализе данных, выполненном при анализе, выполненНом в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d0c09-142">The **Import data to Office 365 page** page is displayed with detailed data insights from the analysis that Office 365 performed.</span></span> 
    
    ![Office 365 отображает подробные сведения об анализе PST-файлов.](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    <span data-ttu-id="d0c09-p109">На диаграмме на этой странице отображается объем данных, которые будут импортированы. Сведения о каждом типе сообщений, обнаруженном в PST-файлах, отображаются на диаграмме. Вы можете навести курсор на каждую панель, чтобы отобразить конкретные сведения об этом типе сообщения. Кроме того, существует раскрывающийся список с разными значениями возраста на основе анализа PST-файлов. При выборе возраста в раскрывающемся списке диаграмма обновляется, чтобы показать, сколько данных будет импортировано для выбранного возраста.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p109">The graph on this page shows the amount of data that will be imported. Information about each message type found in the PST files is displayed in the graph. You can hover the cursor over each bar to display specific information about that message type. There is also a drop-down list with different age values based on the analysis of the PST files. When you select an age in the drop-down list, the graph is updated to show how much data will be imported for the selected age.</span></span> 
    
    <span data-ttu-id="d0c09-p110">б. Чтобы настроить дополнительные фильтры для уменьшения объема импортируемых данных, щелкните **Дополнительные параметры фильтрации**.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p110">b. To configure addition filters to reduce the amount of data that's imported, click **More filtering options**.</span></span>
    
    ![Настройка фильтров на странице "Дополнительные параметры" для обрезки импортированных данных](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    <span data-ttu-id="d0c09-152">Вы можете настроить эти фильтры:</span><span class="sxs-lookup"><span data-stu-id="d0c09-152">You can configure these filters:</span></span>
    
      - <span data-ttu-id="d0c09-p111">**Age** — Выберите возраст, чтобы импортироваться только элементы новее указанного возраста. В разделе [More Information (Дополнительные сведения](filter-data-when-importing-pst-files.md#moreinfo) ) представлено описание того, как Office 365 определяет периоды хранения для фильтра **возраста** .</span><span class="sxs-lookup"><span data-stu-id="d0c09-p111">**Age** - Select an age so only items that are newer than the specified age will be imported. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a description about how Office 365 determines the age buckets for the **Age** filter.</span></span> 
    
      - <span data-ttu-id="d0c09-p112">**Type** — в этом разделе показаны все типы сообщений, обнаруженные в PST-файлах для задания импорта. Вы можете снять флажок рядом с типом сообщения, которое нужно исключить. Обратите внимание, что вы не можете исключить другой тип сообщения. Список элементов почтовых ящиков, включенных в другую категорию, представлен в разделе [Дополнительные сведения](filter-data-when-importing-pst-files.md#moreinfo) .</span><span class="sxs-lookup"><span data-stu-id="d0c09-p112">**Type** - This section shows all the message types that were found in the PST files for the import job. You can uncheck a box next to a message type that you want to exclude. Note that you can't exclude the Other message type. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a list of mailbox items that are included in the Other category.</span></span> 
    
      - <span data-ttu-id="d0c09-p113">**Пользователи** — вы можете исключить сообщения, отправленные или полученные определенными пользователями. Чтобы исключить пользователей, которые отображаются в поле "от:", "Кому:" или "копия: сообщения", нажмите кнопку **исключить пользователей** рядом с этим типом получателя. Введите адрес электронной почты (SMTP-адрес) пользователя, щелкните **Добавить**![значок](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) , чтобы добавить его в список исключенных пользователей для этого типа получателя, а затем нажмите кнопку **сохранить** , чтобы сохранить список исключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p113">**Users** - You can exclude messages that are sent or received by specific people. To exclude people who appear in the From: field, To: field, or the Cc: field of messages, click **Exclude users** next to that recipient type. Type the email address (SMTP address) of the person, click **Add**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) to add them to the list of excluded users for that recipient type, and then click **Save** to save the list of excluded users.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="d0c09-p114">В Office 365 не отображается информация о том, что в результате настройки фильтра **людей** не отображается. Тем не менее, если вы настроили этот фильтр, чтобы исключить сообщения, отправленные или полученные определенными пользователями, эти сообщения будут исключены во время фактического процесса импорта.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p114">Office 365 doesn't show data insights that result from setting the **People** filter. However, if you set this filter to exclude messages sent or received by specific people, those messages will be excluded during the actual import process.</span></span> 
  
    <span data-ttu-id="d0c09-p115">c. Нажмите кнопку **Применить** на странице **Дополнительные параметры фильтрации** , чтобы сохранить параметры фильтра.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p115">c. Click **Apply** in the **More filtering options** fly out page to save your filter settings.</span></span> 
    
    <span data-ttu-id="d0c09-p116">Сведения, содержащиеся на странице **Импорт данных в Office 365** , обновляются на основе параметров фильтра, в том числе общий объем данных, которые будут импортированы на основе параметров фильтра. Обратите внимание, что также отображается сводка по параметрам фильтра. При необходимости можно нажать кнопку **изменить** рядом с фильтром, чтобы изменить значение.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p116">The data insights on the **Import data to Office 365** page are updated based on your filter settings, including the total amount of data that will be imported based on the filter settings. Note that a summary of the filter settings is also shown. You can click **Edit** next to a filter to change the setting if necessary.</span></span> 
    
    ![Сведения об аналитике обновляются в соответствии с параметрами фильтров](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    <span data-ttu-id="d0c09-p117">г. Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p117">d. Click **Next**.</span></span>
    
    <span data-ttu-id="d0c09-p118">Отображается страница состояния, на которой показаны параметры фильтра. Опять же, вы можете изменить любой из параметров фильтра.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p118">A status page is displayed showing your filter settings. Again, you can edit any of the filter settings.</span></span>
    
    <span data-ttu-id="d0c09-p119">д Нажмите кнопку **Импорт данных** , чтобы начать импорт. Обратите внимание, что отображается общий объем данных, которые будут импортированы.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p119">e. Click **Import data** to start the import . Note that the total amount of data that will be imported is displayed.</span></span> 
    
    <span data-ttu-id="d0c09-177">Или</span><span class="sxs-lookup"><span data-stu-id="d0c09-177">Or</span></span>
    
    <span data-ttu-id="d0c09-p120">a. Нажмите кнопку **нет, импортировать** все данные из PST-файлов в Office 365, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p120">a. Click **No, I want to import everything** to import all data in the PST files to Office 365, and then click **Next**.</span></span>
    
    <span data-ttu-id="d0c09-p121">б. на странице **Импорт данных в Office 365** щелкните **Импорт данных** , чтобы начать импорт. Обратите внимание, что отображается общий объем данных, которые будут импортированы.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p121">b. On the **Import data to Office 365** page, click **Import data** to start the import. Note that the total amount of data that will be imported is displayed.</span></span> 
    
6. <span data-ttu-id="d0c09-p122">На странице **Импорт** нажмите кнопку **Обновить** ![обновление](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). Состояние задания импорта отображается в столбце **состояние** .</span><span class="sxs-lookup"><span data-stu-id="d0c09-p122">On the **Import** page, click **Refresh** ![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). The status for the import job is displayed in the **Status** column.</span></span> 
    
7. <span data-ttu-id="d0c09-185">Щелкните Импорт задания, чтобы отобразить более подробные сведения, такие как состояние каждого PST-файла и параметры фильтра, которые вы настроили.</span><span class="sxs-lookup"><span data-stu-id="d0c09-185">Click the import the job to display more detailed information, such as the status for each PST file and the filter settings that you configured.</span></span>

  
## <a name="more-information"></a><span data-ttu-id="d0c09-186">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d0c09-186">More information</span></span>

- <span data-ttu-id="d0c09-p123">Как Office 365 определяет приращения для фильтра возраста? Когда Office 365 анализирует PST-файл, он анализирует отметку времени отправки или получения каждого элемента (если для элемента задана отметка времени отправки и получения, выбирается самая старая Дата). После этого Office 365 просматривает значение года для этой временной метки и сравнивает его с текущей датой для определения возраста элемента. Эти простои используются в качестве значений в раскрывающемся списке для фильтра **возраста** . Например, если PST-файл содержит сообщения от 2016, 2015 и 2014, то значения в фильтре **возраста** будут составлять **1 год**, **2 года**и **3 года**.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p123">How does Office 365 determine the increments for the age filter? When Office 365 analyzes a PST file, it looks at the sent or received time stamp of each item (if an item has both a sent and received timestamp, the oldest date is selected). Then Office 365 looks at the year value for that timestamp and compares it to the current date to determine the age of the item. These ages are then used as the values in the drop-down list for the **Age** filter. For example, if a PST file has messages from 2016, 2015, and 2014, then values in the **Age** filter would be **1 year**, **2 years**, and **3 years**.</span></span>
    
- <span data-ttu-id="d0c09-p124">В следующей таблице приведены типы сообщений, которые включены в категорию " **другие** " в поле " **тип** фильтра" на странице " **Дополнительные параметры** " на лету (см. шаг 5b в предыдущей процедуре). В настоящее время вы не можете исключить элементы из категории "другие" при импорте PST в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d0c09-p124">The following table lists the message types that are included in the **Other** category in the **Type** filter on the **More options** fly out page (see Step 5b in the previous procedure). Currently, you can't exclude items in the "Other" category when you import PSTs to Office 365.</span></span> 
    
    |<span data-ttu-id="d0c09-194">**Идентификатор класса сообщения**</span><span class="sxs-lookup"><span data-stu-id="d0c09-194">**Message class ID**</span></span>|<span data-ttu-id="d0c09-195">**Элементы почтового ящика, которые используют этот класс сообщений**</span><span class="sxs-lookup"><span data-stu-id="d0c09-195">**Mailbox items that use this message class**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="d0c09-196">Класс. Лент</span><span class="sxs-lookup"><span data-stu-id="d0c09-196">IPM.Activity</span></span>  <br/> |<span data-ttu-id="d0c09-197">Записи дневника</span><span class="sxs-lookup"><span data-stu-id="d0c09-197">Journal entries</span></span>  <br/> |
    |<span data-ttu-id="d0c09-198">Класс. Документов</span><span class="sxs-lookup"><span data-stu-id="d0c09-198">IPM.Document</span></span>  <br/> |<span data-ttu-id="d0c09-199">Документы и файлы (не вложенные в сообщение электронной почты)</span><span class="sxs-lookup"><span data-stu-id="d0c09-199">Documents and files (not attached to an email message)</span></span>  <br/> |
    |<span data-ttu-id="d0c09-200">Класс. Файлу</span><span class="sxs-lookup"><span data-stu-id="d0c09-200">IPM.File</span></span>  <br/> |<span data-ttu-id="d0c09-201">(то же, что и IPM. Документов</span><span class="sxs-lookup"><span data-stu-id="d0c09-201">(same as IPM.Document)</span></span>  <br/> |
    |<span data-ttu-id="d0c09-202">Класс. Note. ИМК. Notification</span><span class="sxs-lookup"><span data-stu-id="d0c09-202">IPM.Note.IMC.Notification</span></span>  <br/> |<span data-ttu-id="d0c09-203">Отчеты, отправляемые службой почты Интернета, которая является шлюзом Exchange Server в Интернет</span><span class="sxs-lookup"><span data-stu-id="d0c09-203">Reports sent by Internet Mail Connect, which is the Exchange Server gateway to the Internet</span></span>  <br/> |
    |<span data-ttu-id="d0c09-204">Класс. Note. Microsoft. Fax</span><span class="sxs-lookup"><span data-stu-id="d0c09-204">IPM.Note.Microsoft.Fax</span></span>  <br/> |<span data-ttu-id="d0c09-205">Факсимильные сообщения</span><span class="sxs-lookup"><span data-stu-id="d0c09-205">Fax messages</span></span>  <br/> |
    |<span data-ttu-id="d0c09-206">Класс. Note. rules. отсутствие на работе. Template. Microsoft</span><span class="sxs-lookup"><span data-stu-id="d0c09-206">IPM.Note.Rules.Oof.Template.Microsoft</span></span>  <br/> |<span data-ttu-id="d0c09-207">Сообщения автоответа об отсутствии на месте</span><span class="sxs-lookup"><span data-stu-id="d0c09-207">Out-of-office auto-reply messages</span></span>  <br/> |
    |<span data-ttu-id="d0c09-208">Класс. Note. rules. Реплитемплате. Microsoft</span><span class="sxs-lookup"><span data-stu-id="d0c09-208">IPM.Note.Rules.ReplyTemplate.Microsoft</span></span>  <br/> |<span data-ttu-id="d0c09-209">Ответы, отправленные правилом папки "Входящие"</span><span class="sxs-lookup"><span data-stu-id="d0c09-209">Replies sent by an inbox rule</span></span>  <br/> |
    |<span data-ttu-id="d0c09-210">Класс. OLE. Классе</span><span class="sxs-lookup"><span data-stu-id="d0c09-210">IPM.OLE.Class</span></span>  <br/> |<span data-ttu-id="d0c09-211">Исключения для повторяющихся рядов</span><span class="sxs-lookup"><span data-stu-id="d0c09-211">Exceptions for a recurring series</span></span>  <br/> |
    |<span data-ttu-id="d0c09-212">Класс. Отозвать. Report</span><span class="sxs-lookup"><span data-stu-id="d0c09-212">IPM.Recall.Report</span></span>  <br/> |<span data-ttu-id="d0c09-213">Отчеты об отзыве сообщений</span><span class="sxs-lookup"><span data-stu-id="d0c09-213">Message recall reports</span></span>  <br/> |
    |<span data-ttu-id="d0c09-214">Класс. Удаленного</span><span class="sxs-lookup"><span data-stu-id="d0c09-214">IPM.Remote</span></span>  <br/> |<span data-ttu-id="d0c09-215">Удаленные сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="d0c09-215">Remote mail messages</span></span>  <br/> |
    |<span data-ttu-id="d0c09-216">Класс. Вложен</span><span class="sxs-lookup"><span data-stu-id="d0c09-216">IPM.Report</span></span>  <br/> |<span data-ttu-id="d0c09-217">Отчеты о состоянии элементов</span><span class="sxs-lookup"><span data-stu-id="d0c09-217">Item status reports</span></span>  <br/> |
