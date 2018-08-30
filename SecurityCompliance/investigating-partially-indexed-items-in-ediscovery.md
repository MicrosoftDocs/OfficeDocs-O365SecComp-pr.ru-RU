---
title: Исследование частично индексированных элементов в функции обнаружения электронных данных в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: Частично индексированных элементов (также вызов неиндексированные элементов) являются элементы почтовых ящиков Exchange и документами в SharePoint и OneDrive сайтов, для какой-либо причине не были полностью индексироваться для поиска контента. В этой статье можно Узнайте, почему элементы не могут быть индексированы для поиска и возвращаются в виде частично индексированных элементов, обнаружения ошибок поиска для частично индексированных элементов и использовать сценарий PowerShell для определения наличия вашей организации в частично индексированных электронной почты элементы.
ms.openlocfilehash: 4e8e8c31e6c5450a9b84a1240c2ae8d891c1bd6f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535394"
---
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a><span data-ttu-id="fa3e1-104">Исследование частично индексированных элементов в функции обнаружения электронных данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="fa3e1-104">Investigating partially indexed items in Office 365 eDiscovery</span></span>

<span data-ttu-id="fa3e1-p102">Поиск контента, которую можно запускать из безопасности Office 365 &amp; центре соответствия требованиям автоматически включает в себя частично индексированных элементов в оценке результатов поиска при выполнении поиска. Частично индексированных элементов, элементы почтовых ящиков Exchange и документов на сервере SharePoint и OneDrive для бизнеса сайтов, для какой-либо причине не были полностью индексироваться для поиска. Большинство сообщений электронной почты и документы сайта успешно индексируются, так как они попадают в [индексирования ограничения для сообщений электронной почты](limits-for-content-search.md#indexinglimits). Тем не менее некоторые элементы может превысить эти ограничения для индексирования и частично индекс. Ниже перечислены другие и по следующим причинам элементов не могут быть индексированы для поиска возвращаются в виде частично индексированных элементов при выполнении поиска контента:</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p102">A Content Search that you run from the Office 365 Security &amp; Compliance Center automatically includes partially indexed items in the estimated search results when you run a search. Partially indexed items are Exchange mailbox items and documents on SharePoint and OneDrive for Business sites that for some reason weren't completely indexed for search. Most email messages and site documents are successfully indexed because they fall within the [Indexing limits for email messages](limits-for-content-search.md#indexinglimits). However, some items may exceed these indexing limits, and will be partially indexed. Here are other reasons why items can't be indexed for search and are returned as partially indexed items when you run a Content Search:</span></span>
  
- <span data-ttu-id="fa3e1-110">Сообщения электронной почты у вложенного файла типа файлов, не могут быть индексированы; в большинстве случаев тип файла имеет значение [нераспознанный или не поддерживается для индексации](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span><span class="sxs-lookup"><span data-stu-id="fa3e1-110">Email messages have an attached file of a file type that can't be indexed; in most cases, the file type is [unrecognized or unsupported for indexing](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span></span>
    
- <span data-ttu-id="fa3e1-111">Сообщения электронной почты имеют вложенный файл без допустимого обработчика, такие как файлы изображений; Это является самой распространенной причиной частично индексированных электронной почты</span><span class="sxs-lookup"><span data-stu-id="fa3e1-111">Email messages have an attached file without a valid handler, such as image files; this is the most common cause of partially indexed email items</span></span>
    
- <span data-ttu-id="fa3e1-112">Слишком много файлов, вложенных в сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="fa3e1-112">Too many files attached to an email message</span></span>
    
- <span data-ttu-id="fa3e1-113">Файл, вложенный в сообщение электронной почты слишком велико</span><span class="sxs-lookup"><span data-stu-id="fa3e1-113">A file attached to an email message is too large</span></span>
    
- <span data-ttu-id="fa3e1-114">Тип файла поддерживает индексирование, но произошла ошибка индексирования определенного файла</span><span class="sxs-lookup"><span data-stu-id="fa3e1-114">The file type is supported for indexing but an indexing error occurred for a specific file</span></span>
    
<span data-ttu-id="fa3e1-p103">Несмотря на то, что она может изменяться большинство организаций клиентов Office 365 иметь не более 1% контента меньше, чем 12% контента и его по размеру, частично индексируются. Причина различие между тома и размер является то, что большие файлы выше вероятность содержащий данные, которые не могут быть индексированы полностью.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p103">Although it varies, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed. The reason for the difference between the volume versus size is that larger files have a higher probability of containing content that can't be completely indexed.</span></span>
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a><span data-ttu-id="fa3e1-117">Почему изменить число частично индексированных элементов для поиска</span><span class="sxs-lookup"><span data-stu-id="fa3e1-117">Why does the partially indexed item count change for a search?</span></span>

<span data-ttu-id="fa3e1-p104">После выполнения поиска контента в Office 365 безопасность &amp; в статистику результатов поиска, которая отображается в подробную статистику по перечислены центре соответствия требованиям, общее число и размер частично индексированных элементов в папках поиска поиск. Обратите внимание, что они называются *неиндексированные элементов* в Статистика поиска. Вот несколько вещей, которые влияют на количество частично индексированных элементов, возвращаемых в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p104">After you run a Content Search in the Office 365 Security &amp; Compliance Center, the total number and size of partially indexed items in the locations that were searched are listed in the search result statistics that are displayed in the detailed statistics for the search. Note these are called  *unindexed items*  in the search statistics. Here are a few things that will affect the number of partially indexed items that are returned in the search results:</span></span> 
  
- <span data-ttu-id="fa3e1-p105">Если элемент частично индексируются и отвечающей поисковому запросу, он включен в count (и размер) элементов результатов поиска и частично индексированных элементов. Тем не менее при экспорте результатов, что же поиск элемент включен только с набором результатов поиска; он не включен как частично индексированных элементов.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p105">If an item is partially indexed and matches the search query, it's included in both the count (and size) of search result items and partially indexed items. However, when the results of that same search are exported, the item is included only with set of search results; it's not included as a partially indexed item.</span></span>
    
- <span data-ttu-id="fa3e1-p106">Если указать диапазон дат для поискового запроса (в том числе его в запрос) или используя условия, любой частично индексированный элемент, который не совпадает с диапазон дат не включена в подсчет частично индексированных элементов. В число частично индексированных элементов включены только частично индексированных элементов, попадающих в интервал дат.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p106">If you specify a date range for a search query (by including it in the keyword query or by using a condition), any partially indexed item that doesn't match the date range isn't included in the count of partially indexed items. Only the partially indexed items that fall within date range are included in the count of partially indexed items.</span></span>
    
 <span data-ttu-id="fa3e1-p107">**Примечание:** Частично индексированных элементов, размещенных в SharePoint и OneDrive сайты *, не* включены в оценку частично индексированных элементов, отображаемых в статистика для поиска. Тем не менее частично индексированных элементов можно экспортировать, если экспортировать результаты поиска контента. Например если можно только поиск сайтов в поиск контента, расчетное частично индексированных элементов будет равен нулю.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p107">**Note:** Partially indexed items located in SharePoint and OneDrive sites  *are not*  included in the estimate of partially indexed items that's displayed in the detailed statistics for the search. However, partially indexed items can be exported when you export the results of a Content Search. For example, if you only search sites in a Content Search, the estimated number partially indexed items will be zero.</span></span> 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a><span data-ttu-id="fa3e1-128">Вычисление соотношение частично индексированных элементов в вашей организации</span><span class="sxs-lookup"><span data-stu-id="fa3e1-128">Calculating the ratio of partially indexed items in your organization</span></span>

<span data-ttu-id="fa3e1-p108">Понять воздействие частично индексированных элементов вашей организации, можно запустить поиска для всего контента в всех почтовых ящиков (с помощью запроса ключевого слова пустым). В следующем примере существует 56,208 (4,830 МБ) полностью индексированных элементов и 470 (316 МБ) частично индексированных элементов.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p108">To understand your organization's exposure to partially indexed items, you can run a search for all content in all mailboxes (by using a blank keyword query). In the following example below, there are 56,208 (4,830 MB) fully indexed items and 470 (316 MB) partially indexed items.</span></span>
  
![Пример поиска отображение статистики частично индексированных элементов](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
<span data-ttu-id="fa3e1-132">Можно определить процент частично индексированных элементов с помощью следующих методов вычисления.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-132">You can determine the percentage of partially indexed items by using the following calculations.</span></span>
  
 <span data-ttu-id="fa3e1-133">**Для расчета коэффициента частично индексированных элементов в вашей организации:**</span><span class="sxs-lookup"><span data-stu-id="fa3e1-133">**To calculate the ratio of partially indexed items in your organization:**</span></span>

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
<span data-ttu-id="fa3e1-134">С помощью результаты поиска из предыдущего примера. 84% всех элементов почтовых ящиков, частично индексируются.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-134">By using the search results from the previous example, .84% of all mailboxes items are partially indexed.</span></span>
  
 <span data-ttu-id="fa3e1-135">**Чтобы вычислить процент размер частично индексированных элементов в вашей организации:**</span><span class="sxs-lookup"><span data-stu-id="fa3e1-135">**To calculate the percentage of the size of partially indexed items in your organization:**</span></span>

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

<span data-ttu-id="fa3e1-p109">Так что в предыдущем примере 6.54% от общего объема элементов почтового ящика являются из частично индексированных элементов. Как уже указано, большинство организаций Office 365, клиенты могут не более 1% контента и меньше, чем 12% содержимого по размеру, частично индексированы.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p109">So in the previous example, 6.54% of the total size of mailbox items are from partially indexed items. As previously stated, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span>

## <a name="working-with-partially-indexed-items"></a><span data-ttu-id="fa3e1-138">Работа с частично индексированных элементов</span><span class="sxs-lookup"><span data-stu-id="fa3e1-138">Working with partially indexed items</span></span>

<span data-ttu-id="fa3e1-p110">В тех случаях, когда следует просмотреть частично элементов, чтобы убедиться, что они не содержат информацию, можно [экспортировать отчет поиска контента](export-a-content-search-report.md) , который содержит сведения о частично индексированных элементов. При экспорте отчета поиска контента, обязательно выберите один из параметров экспорта, включает в себя частично индексированных элементов.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p110">In cases when you need to examine partially items to validate that they don't contain relevant information, you can [export a content search report](export-a-content-search-report.md) that contains information about partially indexed items. When you export a content search report, be sure to choose one of the export options that includes partially indexed items.</span></span> 
  
![Выберите параметр 2 или 3 для экспорта частично индексированных элементов](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
<span data-ttu-id="fa3e1-p111">При экспорте результаты поиска контента или отчет поиска контента, с помощью одного из этих параметров экспорта включает в себя отчет с именем неиндексированные Items.csv. В этом отчете включает большинство те же данные, где находится файл ResultsLog.csv; Тем не менее, файл неиндексированные Items.csv также включает в себя два поля, связанные с частично индексированных элементов: **Ошибка теги** и **Свойства об ошибках**. Эти поля содержат информацию о ошибка индексирования для каждого частично индексированных элементов. С помощью сведений, эти два поля, которые помогут определить ли ошибка индексирования для определенного влияет на изучение. Если это так, можно выполнить поиск целевого контента и извлечение и экспорта определенных сообщений и документы SharePoint и OneDrive, чтобы вы их можно проверить, чтобы определить, если они важны для расследования. Для получения пошаговых инструкций см. [Подготовка CSV-файл для целевого контента поиска в Office 365](csv-file-for-an-id-list-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p111">When you export content search results or a content search report using one of these options, the export includes a report named Unindexed Items.csv. This report includes most of the same information as the ResultsLog.csv file; however, the Unindexed Items.csv file also includes two fields related to partially indexed items: **Error Tags** and **Error Properties**. These fields contain information about the indexing error for each partially indexed item. Using the information in these two fields can help you determine whether or not the indexing error for a particular impacts your investigation. If it does, you can perform a targeted content search and retrieve and export specific email messages and SharePoint or OneDrive documents so that you can examine them to determine if they're relevant to your investigation. For step-by-step instructions, see [Prepare a CSV file for a targeted Content Search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>
  
 <span data-ttu-id="fa3e1-p112">**Примечание:** Файл неиндексированные Items.csv также содержит поля с именем **Тип ошибки** и **Сообщение об ошибке**. Это прежних версий полей, которые содержат данные, похожие на сведения в полях **Ошибка теги** и **Свойства об ошибке** , но с более подробными сведениями. Эти устаревшие поля можно игнорировать.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p112">**Note:** The Unindexed Items.csv file also contains fields named **Error Type** and **Error Message**. These are legacy fields that contain information that is similar to the information in the **Error Tags** and **Error Properties** fields, but with less detailed information. You can safely ignore these legacy fields.</span></span> 
  
## <a name="errors-related-to-partially-indexed-items"></a><span data-ttu-id="fa3e1-151">Ошибки, связанные с частично индексированных элементов</span><span class="sxs-lookup"><span data-stu-id="fa3e1-151">Errors related to partially indexed items</span></span>

<span data-ttu-id="fa3e1-p113">Ошибка тегов состоят из двух частей данных, ошибки и тип файла. Например в данной паре ошибка/filetype:</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p113">Error tags are made up of two pieces of information, the error and the file type. For example, in this error/filetype pair:</span></span>

```
 parseroutputsize_xls
```

   
 <span data-ttu-id="fa3e1-p114">`parseroutputsize`— Это ошибки и `xls` — это тип файла, возникла ошибка. В тех случаях, которые были тип файла не был распознан или тип файла был не применяется к ошибке появится значение `noformat` вместо типа файла.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p114">`parseroutputsize` is the error and  `xls` is the file type of the file the error occurred on. In cases were the file type wasn't recognized or the file type was doesn't apply to the error, you will see the value  `noformat` in place of the file type.</span></span> 
  
<span data-ttu-id="fa3e1-156">Ниже приведен список индексирования ошибки и описание возможных причин ошибки.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-156">The following is a list of indexing errors and a description of the possible cause of the error.</span></span>
  
|<span data-ttu-id="fa3e1-157">**Ошибка тега**</span><span class="sxs-lookup"><span data-stu-id="fa3e1-157">**Error tag**</span></span>|<span data-ttu-id="fa3e1-158">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fa3e1-158">**Description**</span></span>|
|:-----|:-----|
| `attachmentcount` <br/> |<span data-ttu-id="fa3e1-159">Сообщение электронной почты было слишком много вложений, а некоторые из этих вложений не были обработаны.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-159">An email message had too many attachments, and some of these attachments weren't processed.</span></span>  <br/> |
| `attachmentdepth` <br/> |<span data-ttu-id="fa3e1-p115">Контента синтаксического анализа об изменениях и документа найдено слишком много уровней вложения, вложенных в другие вложения. Некоторые из этих вложений не были обработаны.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p115">The content retriever and document parser found too many levels of attachments nested inside other attachments. Some of these attachments were not processed.</span></span>  <br/> |
| `attachmentrms` <br/> |<span data-ttu-id="fa3e1-162">Вложение не удается декодировать за защитой службы управления правами.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-162">An attachment failed decoding because it was RMS-protected.</span></span>  <br/> |
| `attachmentsize` <br/> |<span data-ttu-id="fa3e1-163">Файл, вложенный в сообщение электронной почты слишком велико и не удается обработать.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-163">A file attached to an email message was too large and couldn't be processed.</span></span>  <br/> |
| `indexingtruncated` <br/> |<span data-ttu-id="fa3e1-p116">При составлении сообщения электронной почты обработанные в индекс, одного из индексируемых свойств слишком велико и усечено. Усеченных свойства перечислены в поле свойства об ошибках.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p116">When writing the processed email message to the index, one of the indexable properties was too large and was truncated. The truncated properties are listed in Error Properties field.</span></span>  <br/> |
| `invalidunicode` <br/> |<span data-ttu-id="fa3e1-p117">Сообщение электронной почты содержит текст, который не удалось обработать как Юникода. Индексирование для этого элемента может быть неполным.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p117">An email message contained text that couldn't be processed as valid Unicode. Indexing for this item may be incomplete.</span></span>  <br/> |
| `parserencrypted` <br/> |<span data-ttu-id="fa3e1-168">Шифрования содержимого вложения или сообщение электронной почты и Office 365 не удалось расшифровать содержимое.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-168">The content of attachment or email message is encrypted, and Office 365 couldn't decode the content.</span></span>  <br/> |
| `parsererror` <br/> |<span data-ttu-id="fa3e1-p118">Неизвестная ошибка во время синтаксического анализа. Обычно это происходит при программного обеспечения ошибки или сбоя службы.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p118">An unknown error occurred during parsing. This typically results from a software bug or a service crash.</span></span>  <br/> |
| `parserinputsize` <br/> |<span data-ttu-id="fa3e1-171">Вложение слишком велик для синтаксического анализа для обработки и синтаксического анализа вложение не произойти или не был завершен.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-171">An attachment was too large for the parser to handle, and the parsing of that attachment didn't happen or wasn't completed.</span></span>  <br/> |
| `parsermalformed` <br/> |<span data-ttu-id="fa3e1-p119">Вложение сформирован и не может обрабатываться средство синтаксического анализа. В этом результатов из старого файла могут получать форматов, файлы, созданные несовместимое программное обеспечение или вирусов, изображающий командлет что-то отличное от собственностью.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p119">An attachment was malformed and couldn't be handled by the parser. This result from can old file formats, files created by incompatible software, or viruses pretending to be something other than claimed.</span></span>  <br/> |
| `parseroutputsize` <br/> |<span data-ttu-id="fa3e1-174">Выходные данные анализа вложения слишком велико и были вынуждены усечено.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-174">The output from the parsing of an attachment was too large and had to be truncated.</span></span>  <br/> |
| `parserunknowntype` <br/> |<span data-ttu-id="fa3e1-175">Вложение имеет тип файла, который не удалось обнаружить Office 365.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-175">An attachment had a file type that Office 365 couldn't detect.</span></span>  <br/> |
| `parserunsupportedtype` <br/> |<span data-ttu-id="fa3e1-176">Вложение имеет тип файла, обнаруживать Office 365could, но синтаксический анализ данного типа файлов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-176">An attachment had a file type that Office 365could detect, but parsing that file type isn't supported.</span></span>  <br/> |
| `propertytoobig` <br/> |<span data-ttu-id="fa3e1-p120">Значение свойства электронной почты в Exchange Store слишком велик нужно вернуть и не удается обработать сообщение. Это обычно происходит только свойства текста сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p120">The value of an email property in Exchange Store was too large to be retrieved and the message couldn't be processed. This typically only happens to the body property of an email message.</span></span>  <br/> |
| `retrieverrms` <br/> |<span data-ttu-id="fa3e1-179">Не удалось расшифровать сообщение защищенных контента об изменениях.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-179">The content retriever failed to decode an RMS-protected message.</span></span>  <br/> |
| `wordbreakertruncated` <br/> |<span data-ttu-id="fa3e1-p121">Слишком много слова обнаружены в документе во время индексирования. После достижения предела прекращена обработка свойства и свойства урезается.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p121">Too many words were identified in the document during indexing. Processing of the property stopped when reaching the limit, and the property is truncated.</span></span>  <br/> |
   
<span data-ttu-id="fa3e1-p122">Ошибка поля описываются поля, которые затрагиваются указанной в поле метки ошибки обработки ошибки. При поиске свойства, такие как `subject` или `participants`, ошибки в тексте сообщения не будут влиять на результаты поиска. Это может быть полезен при определении точно какие частично индексированных элементов, может потребоваться дальнейшего изучения.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p122">Error fields describe which fields are affected by the processing error listed in the Error Tags field. If you're searching a property such as  `subject` or  `participants`, errors in the body of the message won't impact the results of your search. This can be useful when determining exactly which partially indexed items you might need to further investigate.</span></span>
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a><span data-ttu-id="fa3e1-185">С помощью скрипта PowerShell для определения наличия вашей организации в электронной почты частично индексированных элементов</span><span class="sxs-lookup"><span data-stu-id="fa3e1-185">Using a PowerShell script to determine your organization's exposure to partially indexed email items</span></span>

<span data-ttu-id="fa3e1-p123">Далее показано, как запустить сценарий PowerShell, который выполняет поиск всех элементов в всех почтовых ящиков Exchange и создает отчет о вашей организации соотношение частично индексированных электронной почты (число и размер) и отображает число элементов (и их типа) для каждого индексирования Ошибка выполнения. Используйте тег описания ошибок в предыдущем разделе для идентификации ошибка индексирования.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-p123">The following steps show you how to run a PowerShell script that searches for all items in all Exchange mailboxes, and then generates a report about your organization's ratio of partially indexed email items (by count and by size) and displays the number of items (and their file type) for each indexing error that occurs. Use the error tag descriptions in the previous section to identify the indexing error.</span></span>
  
1. <span data-ttu-id="fa3e1-188">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `PartiallyIndexedItems.ps1`.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-188">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `PartiallyIndexedItems.ps1`.</span></span>

```
  write-host "**************************************************"
  write-host "     Office 365 Security &amp; Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery Partially Indexed Item Statistics   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "**************************************************"
  " " 
  # Create a search with Error Tags Refinders enabled
  Remove-ComplianceSearch "RefinerTest" -Confirm:$false -ErrorAction 'SilentlyContinue'
  New-ComplianceSearch -Name "RefinerTest" -ContentMatchQuery "size>0" -RefinerNames ErrorTags -ExchangeLocation ALL
  Start-ComplianceSearch "RefinerTest"
  # Loop while search is in progress
  do{
      Write-host "Waiting for search to complete..."
      Start-Sleep -s 5
      $complianceSearch = Get-ComplianceSearch "RefinerTest"
  }while ($complianceSearch.Status -ne 'Completed')
  $refiners = $complianceSearch.Refiners | ConvertFrom-Json
  $errorTagProperties = $refiners.Entries | Get-Member -MemberType NoteProperty
  $partiallyIndexedRatio = $complianceSearch.UnindexedItems / $complianceSearch.Items
  $partiallyIndexedSizeRatio = $complianceSearch.UnindexedSize / $complianceSearch.Size
  " "
  "===== Partially indexed items ====="
  "         Total          Ratio"
  "Count    {0:N0}{1:P2}" -f $complianceSearch.Items.ToString("N0").PadRight(15, " "), $partiallyIndexedRatio
  "Size(GB) {0:N2}{1:P2}" -f ($complianceSearch.Size / 1GB).ToString("N2").PadRight(15, " "), $partiallyIndexedSizeRatio
  " "
  Write-Host ===== Reasons for partially indexed items =====
  foreach($errorTagProperty in $errorTagProperties)
  {
      $name = $refiners.Entries.($errorTagProperty.Name).Name
      $count = $refiners.Entries.($errorTagProperty.Name).TotalCount
      $frag = $name.Split("{_}")
      $errorTag = $frag[0]
      $fileType = $frag[1]
      if ($errorTag -ne $lastErrorTag)
      {
          $errorTag
      }
      "    " + $fileType + " => " + $count
      $lastErrorTag = $errorTag
  }
  
```
   
2. <span data-ttu-id="fa3e1-189">[Подключение к Office 365: безопасность &amp; PowerShell центре соответствия требованиям](https://go.microsoft.com/fwlink/p/?linkid=627084).</span><span class="sxs-lookup"><span data-stu-id="fa3e1-189">[Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span></span>
    
3. <span data-ttu-id="fa3e1-190">В разделе Безопасность &amp; PowerShell центр соответствия требованиям, перейдите к папке, где был сохранен сценарий на шаге 1, а затем запустите сценарий; Например:</span><span class="sxs-lookup"><span data-stu-id="fa3e1-190">In Security &amp; Compliance Center PowerShell, go to the folder where you saved the script in step 1, and then run the script; for example:</span></span>

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
<span data-ttu-id="fa3e1-191">Ниже приведен пример опубликованные выходных данных, возвращаемое скриптом.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-191">Here's an example fo the output returned by the script.</span></span>
  
![Пример выходных данных из скрипта, который создает отчет в вашей организации доступом частично индексированных элементов электронной почты](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
<span data-ttu-id="fa3e1-193">Обратите внимание на следующее:</span><span class="sxs-lookup"><span data-stu-id="fa3e1-193">Note the following:</span></span>
  
1. <span data-ttu-id="fa3e1-194">Общее число и размер элементов электронной почты и отношение вашей организации электронной почты частично индексированных элементов (число и размер)</span><span class="sxs-lookup"><span data-stu-id="fa3e1-194">The total number and size of email items, and your organization's ratio of partially indexed email items (by count and by size)</span></span>
    
2. <span data-ttu-id="fa3e1-195">Теги ошибка списков и соответствующие типы файлов, для которых произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="fa3e1-195">A list error tags and the corresponding file types for which the error occurred.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fa3e1-196">См. также</span><span class="sxs-lookup"><span data-stu-id="fa3e1-196">See also</span></span>

[<span data-ttu-id="fa3e1-197">Частично индексированные элементы в Поиске содержимого в Office 365</span><span class="sxs-lookup"><span data-stu-id="fa3e1-197">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)
