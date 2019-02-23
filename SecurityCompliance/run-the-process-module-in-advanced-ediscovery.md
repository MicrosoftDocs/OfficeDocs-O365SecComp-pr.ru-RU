---
title: Запуск модуля обработки в Office 365 Advanced eDiscovery
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'ИзУчите рекомендации по подготовке файлов Office 365 для анализа с помощью Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: 19d50bda21f752ec7c22fe52b6fa7272592de128
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216119"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="0321c-103">Запуск модуля обработки в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0321c-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="0321c-104">Файлы Case загружаются в Расширенное обнаружение электронных данных при **подготовке** \> **процесса**подготовки.</span><span class="sxs-lookup"><span data-stu-id="0321c-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0321c-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="0321c-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="0321c-107">Рекомендации: подготовка данных для расширенного обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="0321c-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="0321c-108">**Качество**: ясно определите заполнение файла Case, которое требуется для случая.</span><span class="sxs-lookup"><span data-stu-id="0321c-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="0321c-109">**Загрузка**: Загрузка файлов в расположение, доступное для расширенного обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="0321c-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="0321c-p102">**Идентификатор файла**: уникальный идентификатор файла в Advanced eDiscovery. Если идентификатор файла не импортируется, Advanced eDiscovery автоматически создает идентификатор. Если вы созначите идентификатор в ходе последующей загрузки процесса и сопоставьте другой путь, отличный от пути в начальной нагрузке процесса, Расширенное обнаружение электронных данных заменит путь (вместо добавления новой записи файла). Идентификатор можно использовать в качестве ссылки в процессе экспорта. Значение ID не должно быть равно "– 1".</span><span class="sxs-lookup"><span data-stu-id="0321c-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="0321c-p103">**MD5**: Эта подпись используется для различения файлов (два файла не считаются точными копиями, если они не имеют одинаковых MD5). По умолчанию Расширенное обнаружение электронных данных вычисляет MD5 для файлов. Если загруженные файлы представляют собой текстовые файлы, рекомендуется загружать и сопоставлять исходное значение MD5, а не подсчитывать их в Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="0321c-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="0321c-118">**Тип и имя файла**:</span><span class="sxs-lookup"><span data-stu-id="0321c-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="0321c-p104">Расширенные функции обнаружения электронных данных могут обрабатывать файлы различных форматов и извлекать файлы, загруженные из машинного \*кода, в стандартный формат, например. TXT, HTML или. XML. обработка текстовых файлов выполняется быстрее, чем у собственных файлов. Извлеченные текстовые файлы хранятся в папке "Case".</span><span class="sxs-lookup"><span data-stu-id="0321c-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="0321c-p105">Не загружайте файлы, которые не удается извлечь, например системные файлы или графические изображения. Эти файлы могут отложить обработку.</span><span class="sxs-lookup"><span data-stu-id="0321c-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="0321c-124">Убедитесь, что имена файлов имеют строгое имя, а пути указаны правильно.</span><span class="sxs-lookup"><span data-stu-id="0321c-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="0321c-125">**Путь к файлу**: Advanced eDiscovery может загружать файлы, длина пути к которым не может превышать 400 символов.</span><span class="sxs-lookup"><span data-stu-id="0321c-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="0321c-p106">**Извлечение текста**: при извлечении текста из собственных файлов помимо обычного текста также извлекаются следующие сведения: скрытый текст (Excel и. doc), скрытые столбцы (Excel), отслеживание изменений (doc), заметки докладчика (PPT), внедренные объекты (например, Объекты Excel в PPT-файле). Их можно просмотреть в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="0321c-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="0321c-p107">**Игнорировать текст**: Эта дополнительная функция задается после выполнения процесса и до анализа. Пропуск текста следует использовать с осторожностью, так как его использование может снизить производительность анализа файлов.</span><span class="sxs-lookup"><span data-stu-id="0321c-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="0321c-130">**Многоязычный текст**: расширенные функции обнаружения электронных данных в настоящее время не поддерживают многоязычные имена для тегов, хранитель и проблем.</span><span class="sxs-lookup"><span data-stu-id="0321c-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="0321c-p108">**Метаданные**: Определите, имеются ли метаданные, которые необходимо сохранить в базе данных вариантов для будущего использования, например диапазон дат, размер файла, тип файла, хранитель и тема. Метаданные можно загружать после того, как файлы уже были загружены без повторного запуска инвентаризации или добавления дополнительных затрат на обработку.</span><span class="sxs-lookup"><span data-stu-id="0321c-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="0321c-p109">Если файлы изначально загружались по пути, сопоставьте столбец Path при дальнейшем импорте метаданных. Можно сослаться на файл по ИДЕНТИФИКАТОРу и сопоставить другой путь. Этот сценарий полезен при изменении путей к файлам.</span><span class="sxs-lookup"><span data-stu-id="0321c-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="0321c-p110">Если файлы были первоначально загружены по ИДЕНТИФИКАТОРу файла, сопоставьте столбец ИДЕНТИФИКАТОРов при загрузке метаданных. Ссылка на файл по пути (а не по ИДЕНТИФИКАТОРу) приведет к повторной загрузке файлов с другим ИДЕНТИФИКАТОРом. Расширенное обнаружение электронных данных создает копии файлов, а не загружает метаданные существующих файлов.</span><span class="sxs-lookup"><span data-stu-id="0321c-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="0321c-139">**Семейства**: невозможно загрузить семейство без родительского (головного офиса).</span><span class="sxs-lookup"><span data-stu-id="0321c-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="0321c-p111">**Размер файла**: ограничение размера файлов, загруженных в Расширенное обнаружение электронных данных, не ограничено. Для анализа (анализ, релевантность и т. д.) — 5 242 880 символов извлеченного текста. Большие файлы игнорируются (например, файлы не участвуют в процессе обучения релевантности и не получают показатель релевантности после вычисления партии).</span><span class="sxs-lookup"><span data-stu-id="0321c-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="0321c-p112">**Количество файлов**: не предусмотрено максимальное количество файлов, которые можно обработать в едином случае. Производительность зависит от ресурсов системы.</span><span class="sxs-lookup"><span data-stu-id="0321c-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="0321c-145">Фильтрация файлов</span><span class="sxs-lookup"><span data-stu-id="0321c-145">Filtering files</span></span>

<span data-ttu-id="0321c-p113">Пользовательская метка может быть связана с набором файлов, чтобы исключить их из процесса или из других задач. Каждый сеанс процесса связан с ИДЕНТИФИКАТОРом пакета. Несмотря на то, что идентификатор пакета не виден эксперту по релевантности, это можно сделать с помощью средства поиска, добавив фильтр для текущего пакета и размечая все соответствующие файлы с помощью пользовательской метки.</span><span class="sxs-lookup"><span data-stu-id="0321c-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0321c-149">См. также</span><span class="sxs-lookup"><span data-stu-id="0321c-149">See also</span></span>

[<span data-ttu-id="0321c-150">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0321c-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="0321c-151">Запуск модуля Process и загрузка данных</span><span class="sxs-lookup"><span data-stu-id="0321c-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0321c-152">Просмотр результатов модуля процесса</span><span class="sxs-lookup"><span data-stu-id="0321c-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

