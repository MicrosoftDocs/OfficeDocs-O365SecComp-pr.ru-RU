---
title: Подготовка CSV-файла для списка идентификатор поиска контента в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Используйте файл Results.csv или неиндексированные Items.csv из существующего контента поиска для создания поискового идентификатор списка, возвращающий определенного сообщения. Поиска списка Идентификаторов обычно используется для возврата элементов частично индексированных почтового ящика.
ms.openlocfilehash: 28e4a66e5c9be1817881004b1e4b3a3e6d4bfdb9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535242"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a><span data-ttu-id="99969-104">Подготовка CSV-файла для списка идентификатор поиска контента в Office 365</span><span class="sxs-lookup"><span data-stu-id="99969-104">Prepare a CSV file for an ID list Content Search in Office 365</span></span>

<span data-ttu-id="99969-p102">Можно выполнить поиск определенного почтового ящика сообщения электронной почты и другие элементы почтового ящика с помощью списка идентификаторов Exchange. Для создания поискового списка ID (официально называется целевого поиска), отправка значений, разделенных запятыми (CSV) файл, определяющий элементы определенного почтового ящика для поиска. Для этой CSV-файл с помощью **Results.csv** файл или файл **Неиндексированные Items.csv** , включаемых при экспортировать результаты поиска контента или экспортировать отчет о поиске содержимого из и поиска существующего контента. Затем изменить один из этих файлов, чтобы указать определенные элементы для поиска и затем создать новый поиск списка идентификатор и отправки CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="99969-p102">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For this CSV file you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content Search results or export a Content Search report from and existing Content Search. Then you edit one of these files to indicate the specific items to search for, and then create a new ID list search and submit the CSV file.</span></span> 
  
<span data-ttu-id="99969-109">Ниже приведен краткий обзор процедуры создания поискового запроса идентификатор списка.</span><span class="sxs-lookup"><span data-stu-id="99969-109">Here's a quick overview of the process for creating an ID list search.</span></span>
  
1. <span data-ttu-id="99969-110">Создание и выполнение новых или под руководством инструктора поиска контента в системы &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="99969-110">Create and run a new or guided Content Search in the Security &amp; Compliance Center.</span></span>
    
2. <span data-ttu-id="99969-p103">Экспорт результатов поиска контента или экспорт отчетов поиска контента. Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="99969-p103">Export the content search results or export the content search report. For more information, see:</span></span>
    
    - [<span data-ttu-id="99969-113">Экспорт результатов поиска контента из безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="99969-113">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
    - [<span data-ttu-id="99969-114">Экспорт отчета о поиске контента</span><span class="sxs-lookup"><span data-stu-id="99969-114">Export a Content Search report</span></span>](export-a-content-search-report.md)
    
3. <span data-ttu-id="99969-p104">Измените файл **Results.csv** или **Неиндексированные Items.csv** и определите, какие элементы определенного почтового ящика, которые необходимо включить в список поиск идентификатора. В разделе [инструкции](#prepare-the-csv-file-for-an-id-list-search) по подготовке CSV-файла для поиска идентификатор списка.</span><span class="sxs-lookup"><span data-stu-id="99969-p104">Edit the **Results.csv** file or the **Unindexed Items.csv** and identify the specific mailbox items that you want to include in the ID list search. See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span> 
    
4. <span data-ttu-id="99969-p105">Создание нового списка Идентификаторов поиска (см. [инструкции](#create-an-id-list-search)) и отправки CSV-файла, подготовленном. Запрос поиска, которая создается выполняет поиск только для элементов, выбранных в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="99969-p105">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared. The search query that's created will only search for the items selected in the CSV file.</span></span>
    
> [!NOTE]
> <span data-ttu-id="99969-p106">Идентификатор списка поиска, поддерживаются только для элементов почтового ящика. Не удается выполнить поиск SharePoint и документов OneDrive в идентификатор списка поиска.</span><span class="sxs-lookup"><span data-stu-id="99969-p106">ID list searches are only supported for mailbox items. You can't search for SharePoint and OneDrive documents in an ID list search.</span></span> 
  
 <span data-ttu-id="99969-p107">**Почему Создание списка поиска идентификатор?** Если вы не удается определить, если элемент реагирует на запрос обнаружения электронных данных на основе метаданных в файлах **Results.csv** или **Неиндексированные Items.csv** , поискового запроса идентификатор списка можно использовать для поиска, предварительный просмотр, а затем экспортировать данного элемента, чтобы определить, если он есть реагирует на случае вы исследование. Идентификатор списка поиска обычно используется для поиска и возврата определенного набора неиндексированные элементов.</span><span class="sxs-lookup"><span data-stu-id="99969-p107">**Why create an ID list search?** If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating. ID list searches are typically used to search for and return a specific set of unindexed items.</span></span> 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="99969-124">Подготовка CSV-файла для поиска идентификатор списка</span><span class="sxs-lookup"><span data-stu-id="99969-124">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="99969-p108">После экспорта результатов поиска или отчет для поиска контента, можно выполнить следующие действия, чтобы подготовить CSV-файла для поиска идентификатор списка. В этом CSV-файла определяет всех элементов в список Поиск кода.</span><span class="sxs-lookup"><span data-stu-id="99969-p108">After you export the search results or report for a content search, you can perform the following steps to prepare the CSV file for an ID list search. This CSV file will identify every item in the ID list search.</span></span>
  
<span data-ttu-id="99969-p109">Обратите внимание на то, что можно использовать в CSV-файл из поиска, который включен учетных записей OneDrive и сайты SharePoint, но можно выбрать *только* элементы почтового ящика для поиска идентификатор списка. При выборе документа в SharePoint или OneDrive CSV-файла завершится ошибкой проверки при создании поискового запроса идентификатор списка.</span><span class="sxs-lookup"><span data-stu-id="99969-p109">Note that you can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can select  *only*  mailbox items for an ID list search. If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span> 
  
1. <span data-ttu-id="99969-129">Откройте файл **Results.csv** или **Неиндексированные Items.csv** в Excel.</span><span class="sxs-lookup"><span data-stu-id="99969-129">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span> 
    
2. <span data-ttu-id="99969-p110">Вставка нового столбца и присвойте ему имя **Выбранные**. Не имеет значения, где вставить столбец. Для удобства рассмотрите возможность вставки слева от первого столбца.</span><span class="sxs-lookup"><span data-stu-id="99969-p110">Insert a new column and name it **Selected**. It doesn't matter where you insert the column. For convenience, consider inserting it to the left of the first column.</span></span>
    
3. <span data-ttu-id="99969-p111">В **столбце** введите **Да** в ячейку, которая соответствует элементу, который требуется найти. Повторите этот шаг для каждого элемента, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="99969-p111">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for. Repeat this step for every item that you want to search for.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="99969-p112">При открытии CSV-файла в Excel, формат данных для столбца **Идентификатора документа** изменяется на **Общие**. Это приводит к отображение идентификатор документа для элемента в научное обозначение. Например документ, который ID «481037338205» отображается в виде «4.81037E + 11"необходимо выполнить дальнейшие действия для изменения формат данных в столбце **Идентификатор документа** **номер** для восстановления правильный формат для идентификатора документа Если вы не сделать, поиск списка кода, который использует CSV-файла завершится с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="99969-p112">When you open the CSV file in Excel, the data format for the **Document ID** column is changed to **General**. This results in displaying the document ID for an item in scientific notation. For example, the document ID of "481037338205" is displayed as "4.81037E+11" You have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID. If you don't do this, the ID list search that uses the CSV file will fail.</span></span> 
  
4. <span data-ttu-id="99969-139">Щелкните правой кнопкой мыши целый столбец **Идентификатора документа** и выберите **Формат ячеек**.</span><span class="sxs-lookup"><span data-stu-id="99969-139">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>
    
5. <span data-ttu-id="99969-140">В поле **категории** выберите **номер**.</span><span class="sxs-lookup"><span data-stu-id="99969-140">In the **Category** box, click **Number**.</span></span>
    
6. <span data-ttu-id="99969-p113">Изменение количества знаков после запятой; **0**и нажмите кнопку **ОК** , чтобы сохранить изменения. Обратите внимание на то, что значения в столбце идентификатор документа изменяются на номера.</span><span class="sxs-lookup"><span data-stu-id="99969-p113">Change the number of decimal places to **0**, and then click **OK** to save your changes. Notice that the values in the Document ID column are changed to numbers.</span></span> 
    
    <span data-ttu-id="99969-143">Ниже приведен пример CSV-файла, который будет готов для отправки для поиска контента списка идентификатор.</span><span class="sxs-lookup"><span data-stu-id="99969-143">Here's an example of the a CSV file that's ready to be submitted for a ID list content search.</span></span>
    
    ![Пример CSV-файла для поиска целевого контента](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. <span data-ttu-id="99969-p114">Сохраните CSV-файла или использовать **Сохранить как** , чтобы сохранить файл с другим именем. В обоих случаях обязательно сохраните файл в формате CSV.</span><span class="sxs-lookup"><span data-stu-id="99969-p114">Save the CSV file or use **Save As** to the save the file with different file name. In both cases, be sure to save the file with the CSV format.</span></span> 
  
## <a name="create-an-id-list-search"></a><span data-ttu-id="99969-147">Создание списка поиска идентификатор</span><span class="sxs-lookup"><span data-stu-id="99969-147">Create an ID list search</span></span>

<span data-ttu-id="99969-148">Следующим шагом является создание нового списка Идентификаторов поиска контента и отправки CSV-файла, подготовленном на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="99969-148">The next step is to create a new ID list Content Search and submit the CSV file that you prepared in the previous step.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="99969-p115">Следует создать поискового запроса идентификатор списка не более 2 дней после экспорта результатов или отчет из поиска контента. Если поиск результаты или отчетов, где экспортированные более 2 дня, повторно следует экспортировать результаты поиска или отчет для создания обновленного CSV-файлов. Затем можно подготовить один из обновленного CSV-файлов и используйте его для создания поискового запроса идентификатор списка.</span><span class="sxs-lookup"><span data-stu-id="99969-p115">You should create an ID list search no more than 2 days after exporting the results or report from a Content Search. If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files. Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span> 
  
1. <span data-ttu-id="99969-152">В разделе Безопасность &amp; центре соответствия требованиям, чтобы перейти на **поиска &amp; расследования** \> **поиска контента**.</span><span class="sxs-lookup"><span data-stu-id="99969-152">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**.</span></span>
    
2. <span data-ttu-id="99969-153">На странице **поиска** щелкните стрелку рядом с элементом ![значком Добавить](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **новый поиск**и нажмите кнопку **поиска с идентификатором**.</span><span class="sxs-lookup"><span data-stu-id="99969-153">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**, and then click **Search by ID List**.</span></span>
    
    ![Нажмите кнопку поиска в списке идентификатор нового раскрывающемся списке поиска](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. <span data-ttu-id="99969-155">На всплывающее окно **поиска с идентификатором** имя поиска (и при необходимости описание его) и затем нажмите кнопку **Обзор** и выберите CSV-файла, подготовленном на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="99969-155">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span> 
    
    <span data-ttu-id="99969-p116">Office 365 пытается проверить CSV-файл. Если проверка завершается неудачно, отображается сообщение об ошибке, которое может помочь устранить ошибки проверки. CSV-файл должен быть успешной проверки для создания поискового идентификатор списка.</span><span class="sxs-lookup"><span data-stu-id="99969-p116">Office 365 attempts to validate the CSV file. If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors. The CSV file has to be successfully validated to create an ID list search.</span></span>
    
4. <span data-ttu-id="99969-159">После CSV успешной проверки файла, нажмите кнопку **поиска** , чтобы создать поиск списка идентификатор.</span><span class="sxs-lookup"><span data-stu-id="99969-159">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span> 
    
    <span data-ttu-id="99969-160">Ниже приведен пример запроса, созданного для поиска идентификатор списка и оценке результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="99969-160">Here's an example of the estimated search results and the query that's generated for an ID list search.</span></span>
    
    ![Запрос поиска для поиска целевого контента в области сведений](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    <span data-ttu-id="99969-162">Обратите внимание на то, соответствие число примерный элементов, отображаемых в статистики для поиска идентификатор число элементов, выбранных в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="99969-162">Note that the number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>
    
5. <span data-ttu-id="99969-163">Предварительный просмотр или экспорт элементы, возвращенные операцией поиска идентификатор списка.</span><span class="sxs-lookup"><span data-stu-id="99969-163">Preview or export the items returned by the ID list search.</span></span>
    
> [!NOTE]
> <span data-ttu-id="99969-p117">При перемещении почтового ящика после создания поискового запроса списка идентификатор запроса для поиска не возвращают выбранные элементы. Вот так как свойство **DocumentId** для элементов почтового ящика изменяются при перемещении почтового ящика. В редких случаях, при перемещении почтового ящика после создания поискового запроса идентификатор списка, необходимо создать новый поиск контента (или обновление результатов поиска для поиска существующего контента) и затем Экспорт поиска результаты или отчет для создания обновленного CSV-файлов, которые могут использоваться  Чтобы создать новый поиск идентификатор списка.</span><span class="sxs-lookup"><span data-stu-id="99969-p117">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items. That's because the **DocumentId** property for mailbox items are changed when a mailbox is moved. In the rare instance when a mailbox is moved after you create an ID list search, you should create a new content search (or update the search results for the existing content search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span> 
