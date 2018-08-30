---
title: Фильтрация данных при импорте PST-файлов в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/24/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 26af16df-34cd-4f4a-b893-bc1d2e74039e
description: 'Используйте новые функции Intelligent импорта в службе Office 365 импорта для фильтрации элементов, которые фактически импортируются в почтовые ящики конечного. Интеллектуальный Import позволяет заранее решить, какие данные для импорта и что следует оставить. Интеллектуальный импорта также предоставляет полезные сведения о на данные, импортируемые в Office 365. '
ms.openlocfilehash: 723a2e05a1f5d256e99bcf8497643435d0c98a23
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534258"
---
# <a name="filter-data-when-importing-pst-files-to-office-365"></a><span data-ttu-id="863d1-105">Фильтрация данных при импорте PST-файлов в Office 365</span><span class="sxs-lookup"><span data-stu-id="863d1-105">Filter data when importing PST files to Office 365</span></span>

<span data-ttu-id="863d1-p102">Используйте новые функции Intelligent импорта в службе Office 365 импорта для фильтрации элементов в PST-файлов, которые фактически импортируются в почтовые ящики конечного. Вот как это работает:</span><span class="sxs-lookup"><span data-stu-id="863d1-p102">Use the new Intelligent Import feature in the Office 365 Import service to filter the items in PST files that actually get imported to the target mailboxes. Here's how it works:</span></span>
  
- <span data-ttu-id="863d1-108">После создания и отправки задания импорта PST-файлов PST-файлов, передаются в область хранилища Azure в облаке Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="863d1-108">After you create and submit a PST import job, PST files are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
    
- <span data-ttu-id="863d1-109">Office 365 служит для анализа данных в PST-файлов в надежным и безопасным способом с учетом срока хранения типов другое сообщение, включенные в PST-файлов и элементов почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="863d1-109">Office 365 analyzes the data in the PST files, in a safe and secure manner, by identifying the age of the mailbox items and the different message types included in the PST files.</span></span>
    
- <span data-ttu-id="863d1-p103">После завершения анализа и можно импортировать данные, у вас есть параметр, чтобы импортировать все данные в PST-файлов или обрезать данные, который импортируется, установив фильтры, которые управляют получает импортированных данных. Например вы можете:</span><span class="sxs-lookup"><span data-stu-id="863d1-p103">When the analysis is complete and the data is ready to import, you have the option to import all data in the PST files as is or trim the data that's imported by setting filters that control what data gets imported. For example, you can choose to:</span></span>
    
  - <span data-ttu-id="863d1-112">Импортируйте только элементы определенного срока.</span><span class="sxs-lookup"><span data-stu-id="863d1-112">Import only items of a certain age.</span></span>
    
  - <span data-ttu-id="863d1-113">Импорт типов выбранного сообщения.</span><span class="sxs-lookup"><span data-stu-id="863d1-113">Import selected message types.</span></span>
    
  - <span data-ttu-id="863d1-114">Исключение сообщения, отправленные или определенные пользователи.</span><span class="sxs-lookup"><span data-stu-id="863d1-114">Exclude messages sent or received by specific people.</span></span>
    
- <span data-ttu-id="863d1-115">После настройки параметров фильтрации Office 365 импортирует данные, отвечающую критериев фильтрации для целевого почтовые ящики, указанные в задание импорта.</span><span class="sxs-lookup"><span data-stu-id="863d1-115">After you configure the filter settings, Office 365 imports only the data that meets the filtering criteria to the target mailboxes specified in the import job.</span></span>
    
<span data-ttu-id="863d1-116">Приведенный ниже рисунок показывает процесс импорта Intelligent и приводится описание задач, которые можно выполнить и задачи, выполняемые с Office 365.</span><span class="sxs-lookup"><span data-stu-id="863d1-116">The following graphic shows the Intelligent Import process, and highlights the tasks you perform and the tasks performed by Office 365.</span></span>
  
![Процесс импорта Intelligent в Office 365](media/f2ec309b-11f5-48f2-939c-a6ff72152d14.png)
  
## <a name="before-you-begin"></a><span data-ttu-id="863d1-118">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="863d1-118">Before you begin</span></span>

- <span data-ttu-id="863d1-p104">Действия, описанные в этом разделе предполагается, что создан задание импорта PST-файлов в службу Office 365 импортировать с помощью загрузки сети или доставку диск. Пошаговые инструкции см.</span><span class="sxs-lookup"><span data-stu-id="863d1-p104">The steps in this topic assume that you've created a PST import job in the Office 365 Import service by using network upload or drive shipping. For step-by-step instructions, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="863d1-121">Импорт PST-файлов в Office 365 с помощью отправки по сети</span><span class="sxs-lookup"><span data-stu-id="863d1-121">Use network upload to import PST files to Office 365</span></span>](use-network-upload-to-import-pst-files.md)
    
  - [<span data-ttu-id="863d1-122">Импорт PST-файлов в Office 365 с помощью отправки дисков</span><span class="sxs-lookup"><span data-stu-id="863d1-122">Use drive shipping to import PST files to Office 365</span></span>](use-drive-shipping-to-import-pst-files-to-office-365.md)
    
- <span data-ttu-id="863d1-p105">После создания задания импорта с помощью сетевой загрузки, сведения о состоянии задания импорта при импорте страницы в Office 365 безопасность &amp; центре соответствия требованиям задано значение **анализа в процессе выполнения**, что означает, что Office 365 анализ данных в PST-файлов, которые вы Отправить. Нажмите кнопку **Обновить**![обновить](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) для обновления состояния задания импорта.</span><span class="sxs-lookup"><span data-stu-id="863d1-p105">After you create an import job by using network upload, the status for the import job on the Import page in Office 365 Security &amp; Compliance Center is set to **Analysis in progress**, which means that Office 365 is analyzing the data in the PST files that you uploaded. Click **Refresh**![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) to update the status for the import job.</span></span> 
    
- <span data-ttu-id="863d1-125">Для импорта заданий доставки диска данные будут анализироваться с Office 365 после персонал центр данных Microsoft получать жесткого диска и загрузки файлов PST-файлов в область Azure хранения для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="863d1-125">For drive shipping import jobs, the data will be analyzed by Office 365 after Microsoft data center personnel receive your hard drive and upload the PST files to the Azure storage area for your organization.</span></span>
  
## <a name="filter-data-that-gets-imported-to-mailboxes"></a><span data-ttu-id="863d1-126">Фильтрация данных, который получает импортирован в почтовые ящики</span><span class="sxs-lookup"><span data-stu-id="863d1-126">Filter data that gets imported to mailboxes</span></span>

<span data-ttu-id="863d1-127">После создания PST задание импорта, выполните следующие действия для фильтрации данных до его импорта в Office 365.</span><span class="sxs-lookup"><span data-stu-id="863d1-127">After you've created a PST import job, follow these steps to filter the data before you import it to Office 365.</span></span>
  
1. <span data-ttu-id="863d1-128">Последовательно выберите пункты [https://protection.office.com/](https://protection.office.com/) и выполнить вход с использованием учетных данных для учетной записи администратора в организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="863d1-128">Go to [https://protection.office.com/](https://protection.office.com/) and sign in using the credentials for an administrator account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="863d1-129">В левой области безопасности Office 365 &amp; центре соответствия требованиям, нажмите кнопку **управления данными** \> **импорта**.</span><span class="sxs-lookup"><span data-stu-id="863d1-129">In the left pane of the Office 365 Security &amp; Compliance Center, click **Data governance** \> **Import**.</span></span>
    
    <span data-ttu-id="863d1-p106">На странице " **Импорт** " перечислены задания импорта для вашей организации. Обратите внимание, что **при выполнении анализа** значение в столбце **состояние** указывает задания импорта, проанализированных с Office 365 и готовы для импорта.</span><span class="sxs-lookup"><span data-stu-id="863d1-p106">The import jobs for your organization are listed on the **Import** page. Note that the **Analysis completed** value in the **Status** column indicates the import jobs that have been analyzed by Office 365 and are ready for you to import.</span></span> 
    
    ![Состояние выполнения анализа указывает, что Office 365 анализ данных в PST-файлов](media/de5294f4-f0ba-4b92-a48a-a4b32b6da490.png)
  
3. <span data-ttu-id="863d1-133">Нажмите кнопку **можно импортировать в Office 365** для задания импорта, которую требуется выполнить.</span><span class="sxs-lookup"><span data-stu-id="863d1-133">Click **Ready to import to Office 365** for the import job that you want to complete.</span></span> 
    
    <span data-ttu-id="863d1-134">Во время работы страницы отображается с сведения о файлах PST-файлов и другие сведения о задание импорта.</span><span class="sxs-lookup"><span data-stu-id="863d1-134">A fly out page is displayed with information about the PST files and other information about the import job.</span></span>
    
4. <span data-ttu-id="863d1-135">Нажмите кнопку **Импорт в Office 365**.</span><span class="sxs-lookup"><span data-stu-id="863d1-135">Click **Import to Office 365**.</span></span>
    
    <span data-ttu-id="863d1-p107">Откроется страница **фильтрации данных** . Он содержит полезные сведения о данных о данных в PST-файлов для задания импорта, а также приведены сведения о срок хранения данных.</span><span class="sxs-lookup"><span data-stu-id="863d1-p107">The **Filter your data** page is displayed. It contains data insights about the data in the PST files for the import job, including information about the age of the data.</span></span> 
    
    ![Страница данных отображаются полезные сведения о данных из PST-файлов для задания импорта](media/3b537ec0-25a4-45a4-96d5-a429e2a33128.png)
  
5. <span data-ttu-id="863d1-139">На основании того, является ли вы хотите сбросить данные, импортированные в Office 365, в разделе **требуется отфильтровать данные?**, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="863d1-139">Based on whether or not you want to trim the data that's imported to Office 365, under **Do you want to filter your data?**, do one of the following:</span></span>
    
    <span data-ttu-id="863d1-p108">а. нажмите кнопку **Да, я хочу фильтр перед импортом** для удаления данных, который можно импортировать и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="863d1-p108">a. Click **Yes, I want to filter it before importing** to trim the data that you import, and then click **Next**.</span></span>
    
    <span data-ttu-id="863d1-142">Откроется страница **Импорт данных в Office 365 страницы** со средствами подробные данные анализа, выполнившего Office 365.</span><span class="sxs-lookup"><span data-stu-id="863d1-142">The **Import data to Office 365 page** page is displayed with detailed data insights from the analysis that Office 365 performed.</span></span> 
    
    ![Office 365 отображает подробные данные суть анализа PST-файлов](media/4881205f-0288-4c32-a440-37e2160295f2.png)
  
    <span data-ttu-id="863d1-p109">На графике на этой странице показано объем данных, который будет импортирован. На графике отображаются сведения о каждом типе сообщения в PST-файлов. Можно наведении курсора на каждой линии для отображения определенных сведений о этого типа сообщений. Имеется также раскрывающегося списка на срок хранения в разных значения на основании анализа PST-файлов. При выборе возраст в раскрывающемся списке диаграммы обновляется для отображения, какой объем данных будет импортирован для выбранного срока хранения.</span><span class="sxs-lookup"><span data-stu-id="863d1-p109">The graph on this page shows the amount of data that will be imported. Information about each message type found in the PST files is displayed in the graph. You can hover the cursor over each bar to display specific information about that message type. There is also a drop-down list with different age values based on the analysis of the PST files. When you select an age in the drop-down list, the graph is updated to show how much data will be imported for the selected age.</span></span> 
    
    <span data-ttu-id="863d1-p110">б. Чтобы настроить Добавление фильтров для сокращения объема данных, который импортируется, нажмите кнопку **Дополнительные параметры фильтрации**.</span><span class="sxs-lookup"><span data-stu-id="863d1-p110">b. To configure addition filters to reduce the amount of data that's imported, click **More filtering options**.</span></span>
    
    ![Настройте фильтры на странице "Дополнительные параметры" Удалить данные, импортируемые](media/3f8d68c3-3fe2-4b4e-9488-b368b98fa9fe.png)
  
    <span data-ttu-id="863d1-152">Можно настроить эти фильтры:</span><span class="sxs-lookup"><span data-stu-id="863d1-152">You can configure these filters:</span></span>
    
      - <span data-ttu-id="863d1-p111">**Срок хранения** - выберите, будет импортирован возраст, поэтому только элементы, которые новее указанного срока хранения. Описание того, как Office 365 определяет сегменты срок хранения для фильтрации **срока хранения** в разделе [Дополнительные сведения](filter-data-when-importing-pst-files.md#moreinfo) .</span><span class="sxs-lookup"><span data-stu-id="863d1-p111">**Age** - Select an age so only items that are newer than the specified age will be imported. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a description about how Office 365 determines the age buckets for the **Age** filter.</span></span> 
    
      - <span data-ttu-id="863d1-p112">**Тип** — в этом разделе представлены все типы сообщений, найденных в PST-файлов для задания импорта. Можно снимите флажок в поле рядом с кнопкой типам сообщений, которые требуется исключить. Обратите внимание, что нельзя исключить тип сообщения. В разделе [Дополнительные сведения](filter-data-when-importing-pst-files.md#moreinfo) для списка элементов почтовых ящиков, которые включены в другой категории.</span><span class="sxs-lookup"><span data-stu-id="863d1-p112">**Type** - This section shows all the message types that were found in the PST files for the import job. You can uncheck a box next to a message type that you want to exclude. Note that you can't exclude the Other message type. See the [More information](filter-data-when-importing-pst-files.md#moreinfo) section for a list of mailbox items that are included in the Other category.</span></span> 
    
      - <span data-ttu-id="863d1-p113">**Пользователи** — можно исключить сообщений, отправленных или полученных конкретные пользователи. Чтобы исключить пользователей, которые отображаются в поле от: поля, чтобы: поля или «копия»: поля сообщений, щелкните **исключение пользователей** рядом с элементом, тип получателя. Введите адрес электронной почты (SMTP-адрес) контакта, нажмите кнопку **Добавить**![новый значок](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) для добавления их в список исключенных пользователей для этого типа получателя и нажмите кнопку **Сохранить** для сохранения в список исключенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="863d1-p113">**Users** - You can exclude messages that are sent or received by specific people. To exclude people who appear in the From: field, To: field, or the Cc: field of messages, click **Exclude users** next to that recipient type. Type the email address (SMTP address) of the person, click **Add**![New icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) to add them to the list of excluded users for that recipient type, and then click **Save** to save the list of excluded users.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="863d1-p114">Office 365 не отображается полезные сведения о данных, к которым приводят Настройка фильтра **людей** . Тем не менее если задать этот фильтр для исключения сообщений, отправку и получение определенных пользователями, эти сообщения будут исключены во время фактического процесса импорта.</span><span class="sxs-lookup"><span data-stu-id="863d1-p114">Office 365 doesn't show data insights that result from setting the **People** filter. However, if you set this filter to exclude messages sent or received by specific people, those messages will be excluded during the actual import process.</span></span> 
  
    <span data-ttu-id="863d1-p115">c. нажмите кнопку **Применить** в **Параметры более фильтрации** во время работы страницы для сохранения параметров фильтра.</span><span class="sxs-lookup"><span data-stu-id="863d1-p115">c. Click **Apply** in the **More filtering options** fly out page to save your filter settings.</span></span> 
    
    <span data-ttu-id="863d1-p116">Данные, которые обновляются средствами на странице **Импорт данных в Office 365** на основе параметров фильтра, включая общий объем данных, который будет импортирован на основании параметров фильтра. Обратите внимание, что также показана сводка параметров фильтра. Щелкните **Изменить** фильтр изменение настройки, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="863d1-p116">The data insights on the **Import data to Office 365** page are updated based on your filter settings, including the total amount of data that will be imported based on the filter settings. Note that a summary of the filter settings is also shown. You can click **Edit** next to a filter to change the setting if necessary.</span></span> 
    
    ![Полезные сведения о данных обновляются на основе параметров фильтра](media/897e20fb-3b13-44c3-9d56-9f330750f2a3.png)
  
    <span data-ttu-id="863d1-p117">d. нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="863d1-p117">d. Click **Next**.</span></span>
    
    <span data-ttu-id="863d1-p118">Отображение параметров фильтра отображается страница состояние. Опять же можно изменить параметры фильтра.</span><span class="sxs-lookup"><span data-stu-id="863d1-p118">A status page is displayed showing your filter settings. Again, you can edit any of the filter settings.</span></span>
    
    <span data-ttu-id="863d1-p119">e. нажмите кнопку **Импорт данных** , чтобы начать импорт. Обратите внимание на то, что отображается общий объем данных, который будет импортирован.</span><span class="sxs-lookup"><span data-stu-id="863d1-p119">e. Click **Import data** to start the import . Note that the total amount of data that will be imported is displayed.</span></span> 
    
    <span data-ttu-id="863d1-177">Второй вариант:</span><span class="sxs-lookup"><span data-stu-id="863d1-177">Or</span></span>
    
    <span data-ttu-id="863d1-p120">а. нажмите кнопку **Нет, я хочу импортировать все,** Чтобы импортировать все данные в PST-файлов в Office 365 и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="863d1-p120">a. Click **No, I want to import everything** to import all data in the PST files to Office 365, and then click **Next**.</span></span>
    
    <span data-ttu-id="863d1-p121">б. на странице **Импорт данных в Office 365** нажмите кнопку **Импорт данных** , чтобы начать импорт. Обратите внимание на то, что отображается общий объем данных, который будет импортирован.</span><span class="sxs-lookup"><span data-stu-id="863d1-p121">b. On the **Import data to Office 365** page, click **Import data** to start the import. Note that the total amount of data that will be imported is displayed.</span></span> 
    
6. <span data-ttu-id="863d1-p122">На странице " **Импорт** ", нажмите кнопку **Обновить** ![обновить](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). Сведения о состоянии задания импорта отображается в столбце **состояние** .</span><span class="sxs-lookup"><span data-stu-id="863d1-p122">On the **Import** page, click **Refresh** ![refresh](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png). The status for the import job is displayed in the **Status** column.</span></span> 
    
7. <span data-ttu-id="863d1-185">Задание для отображения более подробные сведения, такие как сведения о состоянии каждого PST-файл и настроенные параметры фильтра нажмите кнопку Импорт.</span><span class="sxs-lookup"><span data-stu-id="863d1-185">Click the import the job to display more detailed information, such as the status for each PST file and the filter settings that you configured.</span></span>

  
## <a name="more-information"></a><span data-ttu-id="863d1-186">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="863d1-186">More information</span></span>

- <span data-ttu-id="863d1-p123">Как Office 365 определить шагом в фильтре срока хранения Когда Office 365 служит для анализа в PST-файл, просматривает отметкой времени отправки или получения каждого элемента (если элемент имеет оба отправленных и полученных отметку времени, даты наиболее старых будет установлен). Затем Office 365 рассматривается значение года для этого метки времени и сравниваются с текущей датой, чтобы определить срок хранения элемента. Эти возраста затем используется как значение в раскрывающемся списке для фильтр **времени хранения** . Например если в PST-файл содержит сообщения из 2016, 2015 и 2014 г., со значениями в фильтр **времени хранения** будет **1 год**, **через 2 года**и **3 года**.</span><span class="sxs-lookup"><span data-stu-id="863d1-p123">How does Office 365 determine the increments for the age filter? When Office 365 analyzes a PST file, it looks at the sent or received time stamp of each item (if an item has both a sent and received timestamp, the oldest date is selected). Then Office 365 looks at the year value for that timestamp and compares it to the current date to determine the age of the item. These ages are then used as the values in the drop-down list for the **Age** filter. For example, if a PST file has messages from 2016, 2015, and 2014, then values in the **Age** filter would be **1 year**, **2 years**, and **3 years**.</span></span>
    
- <span data-ttu-id="863d1-p124">В следующей таблице приведены типы сообщений, которые включены в **другие** категории фильтра **типа** во время выполнения **Дополнительные параметры** страницы (см. шаг 5b в предыдущей процедуре). В настоящее время не удается исключить элементы в разделе «Другие» категория при импорте PST-файлов в Office 365.</span><span class="sxs-lookup"><span data-stu-id="863d1-p124">The following table lists the message types that are included in the **Other** category in the **Type** filter on the **More options** fly out page (see Step 5b in the previous procedure). Currently, you can't exclude items in the "Other" category when you import PSTs to Office 365.</span></span> 
    
    |<span data-ttu-id="863d1-194">**КОД класса сообщений**</span><span class="sxs-lookup"><span data-stu-id="863d1-194">**Message class ID**</span></span>|<span data-ttu-id="863d1-195">**Элементы почтового ящика, использующих этот класс сообщения**</span><span class="sxs-lookup"><span data-stu-id="863d1-195">**Mailbox items that use this message class**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="863d1-196">IPM. Действие</span><span class="sxs-lookup"><span data-stu-id="863d1-196">IPM.Activity</span></span>  <br/> |<span data-ttu-id="863d1-197">Записи журнала</span><span class="sxs-lookup"><span data-stu-id="863d1-197">Journal entries</span></span>  <br/> |
    |<span data-ttu-id="863d1-198">IPM. Документ</span><span class="sxs-lookup"><span data-stu-id="863d1-198">IPM.Document</span></span>  <br/> |<span data-ttu-id="863d1-199">Документы и файлы (не присоединен к сообщению электронной почты)</span><span class="sxs-lookup"><span data-stu-id="863d1-199">Documents and files (not attached to an email message)</span></span>  <br/> |
    |<span data-ttu-id="863d1-200">IPM. Файл</span><span class="sxs-lookup"><span data-stu-id="863d1-200">IPM.File</span></span>  <br/> |<span data-ttu-id="863d1-201">(аналогично IPM. Документ)</span><span class="sxs-lookup"><span data-stu-id="863d1-201">(same as IPM.Document)</span></span>  <br/> |
    |<span data-ttu-id="863d1-202">IPM. Note.IMC.Notification</span><span class="sxs-lookup"><span data-stu-id="863d1-202">IPM.Note.IMC.Notification</span></span>  <br/> |<span data-ttu-id="863d1-203">Отчеты, отправленных пользователем почты подключение к Интернету, являющийся шлюза Exchange Server в Интернет</span><span class="sxs-lookup"><span data-stu-id="863d1-203">Reports sent by Internet Mail Connect, which is the Exchange Server gateway to the Internet</span></span>  <br/> |
    |<span data-ttu-id="863d1-204">IPM. Note.Microsoft.Fax</span><span class="sxs-lookup"><span data-stu-id="863d1-204">IPM.Note.Microsoft.Fax</span></span>  <br/> |<span data-ttu-id="863d1-205">Факсимильные сообщения</span><span class="sxs-lookup"><span data-stu-id="863d1-205">Fax messages</span></span>  <br/> |
    |<span data-ttu-id="863d1-206">IPM. Note.Rules.Oof.Template.Microsoft</span><span class="sxs-lookup"><span data-stu-id="863d1-206">IPM.Note.Rules.Oof.Template.Microsoft</span></span>  <br/> |<span data-ttu-id="863d1-207">Сообщения от отсутствии автоматического ответа</span><span class="sxs-lookup"><span data-stu-id="863d1-207">Out-of-office auto-reply messages</span></span>  <br/> |
    |<span data-ttu-id="863d1-208">IPM. Note.Rules.ReplyTemplate.Microsoft</span><span class="sxs-lookup"><span data-stu-id="863d1-208">IPM.Note.Rules.ReplyTemplate.Microsoft</span></span>  <br/> |<span data-ttu-id="863d1-209">Ответы по правила папки «Входящие»</span><span class="sxs-lookup"><span data-stu-id="863d1-209">Replies sent by an inbox rule</span></span>  <br/> |
    |<span data-ttu-id="863d1-210">IPM. OLE. Класс</span><span class="sxs-lookup"><span data-stu-id="863d1-210">IPM.OLE.Class</span></span>  <br/> |<span data-ttu-id="863d1-211">Исключения для серии повторяющихся</span><span class="sxs-lookup"><span data-stu-id="863d1-211">Exceptions for a recurring series</span></span>  <br/> |
    |<span data-ttu-id="863d1-212">IPM. Recall.Report</span><span class="sxs-lookup"><span data-stu-id="863d1-212">IPM.Recall.Report</span></span>  <br/> |<span data-ttu-id="863d1-213">Отчеты о отзыв сообщения</span><span class="sxs-lookup"><span data-stu-id="863d1-213">Message recall reports</span></span>  <br/> |
    |<span data-ttu-id="863d1-214">IPM. Удаленные</span><span class="sxs-lookup"><span data-stu-id="863d1-214">IPM.Remote</span></span>  <br/> |<span data-ttu-id="863d1-215">Удаленные почтовые сообщения</span><span class="sxs-lookup"><span data-stu-id="863d1-215">Remote mail messages</span></span>  <br/> |
    |<span data-ttu-id="863d1-216">IPM. Отчет</span><span class="sxs-lookup"><span data-stu-id="863d1-216">IPM.Report</span></span>  <br/> |<span data-ttu-id="863d1-217">Отчеты о состоянии элемента</span><span class="sxs-lookup"><span data-stu-id="863d1-217">Item status reports</span></span>  <br/> |
