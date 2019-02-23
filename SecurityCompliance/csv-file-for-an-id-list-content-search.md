---
title: Подготовка CSV-файла для поиска контента списка ИДЕНТИФИКАТОРов в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Используйте CSV-файл Results. CSV или неиндексированные элементы из существующего поиска контента, чтобы создать поиск списка ИДЕНТИФИКАТОРов, который возвращает определенные сообщения электронной почты. Поиск в списке ИДЕНТИФИКАТОРов обычно используется для возврата частично индексированных элементов почтового ящика.
ms.openlocfilehash: 940656fda58e37772471ba9d72d6bc3932bb8c48
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220239"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a><span data-ttu-id="d83fe-104">Подготовка CSV-файла для поиска контента списка ИДЕНТИФИКАТОРов в Office 365</span><span class="sxs-lookup"><span data-stu-id="d83fe-104">Prepare a CSV file for an ID list Content Search in Office 365</span></span>

<span data-ttu-id="d83fe-p102">Вы можете выполнять поиск определенных сообщений электронной почты и других элементов почтовых ящиков с помощью списка идентификаторов Exchange. Чтобы создать запрос на поиск списка ИДЕНТИФИКАТОРов (формально называется целевой поиском), необходимо предоставить файл данных с разделителями-запятыми (CSV), который определяет конкретные элементы почтового ящика для поиска. Для этого CSV-файла используется **CSV** -файл Results или неиндексированный **CSV** -файл, который включается при экспорте результатов поиска контента или экспорте отчета о поиске контента из и существующего поиска контента. Затем вы редактируете один из этих файлов, чтобы указать конкретные искомые элементы, а затем создайте новый список ИДЕНТИФИКАТОРов и отправит CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p102">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For this CSV file you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content Search results or export a Content Search report from and existing Content Search. Then you edit one of these files to indicate the specific items to search for, and then create a new ID list search and submit the CSV file.</span></span> 
  
<span data-ttu-id="d83fe-109">Ниже приведен краткий обзор процесса создания поиска списка ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-109">Here's a quick overview of the process for creating an ID list search.</span></span>
  
1. <span data-ttu-id="d83fe-110">Создание и запуск нового или интерактивного поиска контента в центре безопасности &amp; и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d83fe-110">Create and run a new or guided Content Search in the Security &amp; Compliance Center.</span></span>
    
2. <span data-ttu-id="d83fe-p103">Экспорт результатов поиска контента или экспорт отчета о поиске контента. Более подробную информацию можно узнать в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="d83fe-p103">Export the content search results or export the content search report. For more information, see:</span></span>
    
    - [<span data-ttu-id="d83fe-113">Экспорт результатов поиска контента из центра безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="d83fe-113">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
    - [<span data-ttu-id="d83fe-114">Экспорт отчета о поиске контента</span><span class="sxs-lookup"><span data-stu-id="d83fe-114">Export a Content Search report</span></span>](export-a-content-search-report.md)
    
3. <span data-ttu-id="d83fe-p104">ОтРедактируйте файл **Results. csv** или **неиндексированные элементы. csv** и определите элементы почтового ящика, которые необходимо включить в поиск списка идентификаторов. В этой [статье приведены инструкции](#prepare-the-csv-file-for-an-id-list-search) по подготовке CSV-файла для поиска в списке идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p104">Edit the **Results.csv** file or the **Unindexed Items.csv** and identify the specific mailbox items that you want to include in the ID list search. See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span> 
    
4. <span data-ttu-id="d83fe-p105">Создайте новый поисковый список ИДЕНТИФИКАТОРов (ознакомьтесь [](#create-an-id-list-search)с инструкциями) и передайте подготовленный CSV-файл. Созданный запрос поиска будет искать только элементы, выбранные в CSV-файле.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p105">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared. The search query that's created will only search for the items selected in the CSV file.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d83fe-p106">Поиск в списке ИДЕНТИФИКАТОРов поддерживается только для элементов почтового ящика. Поиск документов SharePoint и OneDrive в поиске списка ИДЕНТИФИКАТОРов невозможен.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p106">ID list searches are only supported for mailbox items. You can't search for SharePoint and OneDrive documents in an ID list search.</span></span> 
  
 <span data-ttu-id="d83fe-p107">**Зачем создавать Поиск списка идентификаторов?** Если вы не можете определить, отвечает ли элемент на запрос обнаружения электронных данных на основе метаданных в CSV-файлах **Results. csv** или неиндексированных **элементов** , можно использовать поиск списка идентификаторов для поиска, просмотра и экспорта этого элемента, чтобы определить, является ли он реагирование на случай, когда вы изучаете. Поиск по списку ИДЕНТИФИКАТОРов обычно используется для поиска и возврата определенного набора неиндексированных элементов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p107">**Why create an ID list search?** If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating. ID list searches are typically used to search for and return a specific set of unindexed items.</span></span> 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="d83fe-124">Подготовка CSV-файла для поиска списка ИДЕНТИФИКАТОРов</span><span class="sxs-lookup"><span data-stu-id="d83fe-124">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="d83fe-p108">После экспорта результатов поиска или отчета по поиску контента можно выполнить следующие действия, чтобы подготовить CSV-файл для поиска в списке ИДЕНТИФИКАТОРов. Этот CSV-файл определяет каждый элемент в поиске списка ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p108">After you export the search results or report for a content search, you can perform the following steps to prepare the CSV file for an ID list search. This CSV file will identify every item in the ID list search.</span></span>
  
<span data-ttu-id="d83fe-p109">Обратите внимание, что вы можете использовать CSV-файл из поиска, включающего сайты SharePoint и учетные записи OneDrive, но вы можете выбрать *только* элементы почтового ящика для поиска в списке идентификаторов. При выборе документа в SharePoint или OneDrive при создании поиска списка ИДЕНТИФИКАТОРов CSV-файл пройдет проверку на наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p109">Note that you can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can select  *only*  mailbox items for an ID list search. If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span> 
  
1. <span data-ttu-id="d83fe-129">Откройте CSV-файл **Results. csv** или неиндексированные **элементы** в Excel.</span><span class="sxs-lookup"><span data-stu-id="d83fe-129">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span> 
    
2. <span data-ttu-id="d83fe-p110">Вставьте новый столбец и присвойте ему \*\*\*\* имя. При вставке столбца не имеет значения. Для удобства рекомендуется вставить его слева от первого столбца.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p110">Insert a new column and name it **Selected**. It doesn't matter where you insert the column. For convenience, consider inserting it to the left of the first column.</span></span>
    
3. <span data-ttu-id="d83fe-p111">В столбце **выбранный** столбец введите **Да** в ячейке, которая соответствует элементу, который требуется найти. Повторите этот шаг для каждого элемента, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p111">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for. Repeat this step for every item that you want to search for.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="d83fe-p112">При открытии CSV-файла в Excel формат данных для столбца " **идентификатор документа** " изменяется на " **Общий**". Это приводит к отображению идентификатора документа для элемента в экспоненциальной нотации. Например, идентификатор документа "481037338205" отображается как "4.81037 E + 11", поэтому необходимо выполнить следующие действия, чтобы изменить формат данных столбца **идентификаторОв документов** на **Number** для восстановления правильного формата идентификатора документа. Если этого не сделать, поиск в списке ИДЕНТИФИКАТОРов, использующий CSV-файл, завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p112">When you open the CSV file in Excel, the data format for the **Document ID** column is changed to **General**. This results in displaying the document ID for an item in scientific notation. For example, the document ID of "481037338205" is displayed as "4.81037E+11" You have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID. If you don't do this, the ID list search that uses the CSV file will fail.</span></span> 
  
4. <span data-ttu-id="d83fe-139">Щелкните правой кнопкой мыши весь столбец " **идентификатор документа** " и выберите пункт **Формат ячеек**.</span><span class="sxs-lookup"><span data-stu-id="d83fe-139">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>
    
5. <span data-ttu-id="d83fe-140">В поле **Категория** выберите **число**.</span><span class="sxs-lookup"><span data-stu-id="d83fe-140">In the **Category** box, click **Number**.</span></span>
    
6. <span data-ttu-id="d83fe-p113">Измените число десятичных разрядов на **0**и нажмите кнопку **ОК** , чтобы сохранить изменения. Обратите внимание, что значения в столбце Идентификатор документа изменяются на числа.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p113">Change the number of decimal places to **0**, and then click **OK** to save your changes. Notice that the values in the Document ID column are changed to numbers.</span></span> 
    
    <span data-ttu-id="d83fe-143">Ниже приведен пример CSV-файла, готового к отправке для поиска контента списка ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-143">Here's an example of the a CSV file that's ready to be submitted for a ID list content search.</span></span>
    
    ![Пример CSV-файла для целевого поиска контента](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. <span data-ttu-id="d83fe-p114">Сохраните CSV-файл или используйте параметр **Сохранить как** , чтобы сохранить файл с другим именем файла. В обоих случаях обязательно сохраните файл в формате CSV.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p114">Save the CSV file or use **Save As** to the save the file with different file name. In both cases, be sure to save the file with the CSV format.</span></span> 
  
## <a name="create-an-id-list-search"></a><span data-ttu-id="d83fe-147">Создание поискового списка ИДЕНТИФИКАТОРов</span><span class="sxs-lookup"><span data-stu-id="d83fe-147">Create an ID list search</span></span>

<span data-ttu-id="d83fe-148">Следующий шаг состоит в создании нового списка ИДЕНТИФИКАТОРов поиска контента и отсылке CSV-файла, подготовленного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="d83fe-148">The next step is to create a new ID list Content Search and submit the CSV file that you prepared in the previous step.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d83fe-p115">Вы должны создать список ИДЕНТИФИКАТОРов, не превышающий 2 дня после экспорта результатов или отчета из поиска контента. Если результаты поиска или отчет, где экспортируется более двух дней назад, необходимо повторно экспортировать результаты или отчет, чтобы создать обновленные CSV-файлы. Затем вы можете подготовить один из обновленных CSV-файлов и использовать его для создания поискового списка ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p115">You should create an ID list search no more than 2 days after exporting the results or report from a Content Search. If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files. Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span> 
  
1. <span data-ttu-id="d83fe-152">В центре безопасности &amp; и соответствия требованиям выберите Поиск \> **контента**для \*\* &amp; расследования\*\* .</span><span class="sxs-lookup"><span data-stu-id="d83fe-152">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**.</span></span>
    
2. <span data-ttu-id="d83fe-153">На странице **поиска** щелкните стрелку рядом с ![кнопкой Добавить значок](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **Поиск**, а затем выберите **Поиск по идентификатору**.</span><span class="sxs-lookup"><span data-stu-id="d83fe-153">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**, and then click **Search by ID List**.</span></span>
    
    ![В раскрывающемся списке создать Поиск выберите пункт Поиск по ИДЕНТИФИКАТОРу](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. <span data-ttu-id="d83fe-155">В всплывающем меню **Поиск по идентификатору** введите имя поиска (и при необходимости опишите его), а затем нажмите кнопку **Обзор** и выберите CSV-файл, подготовленный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="d83fe-155">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span> 
    
    <span data-ttu-id="d83fe-p116">Office 365 пытается проверить CSV-файл. Если проверка завершилась неудачно, отображается сообщение об ошибке, которое может помочь при устранении ошибок проверки. CSV-файл должен быть успешно проверен для создания запроса на поиск списка ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p116">Office 365 attempts to validate the CSV file. If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors. The CSV file has to be successfully validated to create an ID list search.</span></span>
    
4. <span data-ttu-id="d83fe-159">После успешной проверки CSV-файла нажмите кнопку **Поиск** , чтобы создать запрос на поиск списка идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-159">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span> 
    
    <span data-ttu-id="d83fe-160">Ниже приведен пример оценочных результатов поиска и запроса, созданного для поиска в списке ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-160">Here's an example of the estimated search results and the query that's generated for an ID list search.</span></span>
    
    ![Запрос поиска для целевого поиска контента в области сведений](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    <span data-ttu-id="d83fe-162">Обратите внимание, что количество оцененных элементов, отображаемых в статистике для поиска ИДЕНТИФИКАТОРов, должно быть равно количеству элементов, выбранных в CSV-файле.</span><span class="sxs-lookup"><span data-stu-id="d83fe-162">Note that the number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>
    
5. <span data-ttu-id="d83fe-163">Предварительный просмотр или экспорт элементов, возвращенных поиском списка ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-163">Preview or export the items returned by the ID list search.</span></span>
    
> [!NOTE]
> <span data-ttu-id="d83fe-p117">Если вы перемещаете почтовый ящик после создания поискового списка ИДЕНТИФИКАТОРов, запрос поиска не вернет указанные элементы. Это связано с тем, что свойство **DocumentID** для элементов почтового ящика изменяется при перемещении почтового ящика. В редких случаях при перемещении почтового ящика после создания поискового списка ИДЕНТИФИКАТОРов необходимо создать новый поиск контента (или обновить результаты поиска для существующего контента), а затем экспортировать результаты или отчет для создания обновленных CSV-файлов, которые можно использовать  для создания нового поиска списка ИДЕНТИФИКАТОРов.</span><span class="sxs-lookup"><span data-stu-id="d83fe-p117">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items. That's because the **DocumentId** property for mailbox items are changed when a mailbox is moved. In the rare instance when a mailbox is moved after you create an ID list search, you should create a new content search (or update the search results for the existing content search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span> 
