---
title: Запуск модуля обработки в Office 365 Advanced eDiscovery
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Изучите рекомендации по подготовке делами файлов данных Office 365 для анализа с Office 365 Advanced электронного обнаружения.  '
ms.openlocfilehash: 52b1dce9fb778c6628d90c39135f0c93f08134d7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535398"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="c4ce6-103">Запуск модуля обработки в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="c4ce6-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="c4ce6-104">Case файлов, загруженных в расширенной обнаружения электронных данных во время **подготовки** \> **процесса**.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c4ce6-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="c4ce6-107">Инструкции по: Подготовка данных для расширенной обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="c4ce6-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="c4ce6-108">**Качество**: четко определить заполнения вариантов файла, относящихся к регистр.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="c4ce6-109">**Загружает**: Загрузите файлы в папке, где доступны дополнительные обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="c4ce6-p102">**Идентификатор файла**: идентификатор уникальных файла в расширенной обнаружения электронных данных. Если идентификатор отсутствует файл импортировано, расширенные обнаружения электронных данных автоматически создает идентификатор. Если сопоставить идентификатор в последующих процесс загрузки и сопоставить путь отличается от начальной загрузки процесс, расширенные обнаружения электронных данных будет заменить путь (а не добавьте новую запись файлов). Идентификатор можно использовать в качестве ссылки в процесс экспорта. Значение идентификатора не должно быть значение-1».</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="c4ce6-p103">**MD5**: подписи используется для различения файлов (два файла не считаются точное дубликатами отсутствии же MD5). По умолчанию Дополнительно eDiscovery вычисляет MD5 файлы. После загрузки файлов текстовые файлы, рекомендуется для загрузки и сопоставить исходное значение MD5 вместо вычисления в расширенной обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="c4ce6-118">**Имя и тип файла**:</span><span class="sxs-lookup"><span data-stu-id="c4ce6-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="c4ce6-p104">Расширенные обнаружения электронных данных можно обработать файлы различных форматов и извлечение загружен собственный файлов в стандартный формат, таких как \*. TXT, HTML, или. Происходит быстрее, чем файлы в формате XML. обработки текстовых файлов. Извлеченные текстовые файлы хранятся в папке вариантов.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="c4ce6-p105">Не загружать файлы, которые не удается извлечь, например системные файлы или графические изображения. Эти файлы могут задержка обработки.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="c4ce6-124">Убедитесь, что имена файлов значительно с именем и путей.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="c4ce6-125">**Путь к файлу**: расширенные обнаружения электронных данных можно загружать файлы с длины пути до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="c4ce6-p106">**Извлечение текста**: извлечение текста из собственных файлов, кроме обычного текста следующие также извлекаются, когда: скрытый текст (Excel и DOC-файл), скрытые столбцы (Excel), отслеживание изменений (DOC-файл), динамик notes (.ppt), внедренные объекты (например, Объектов Excel в .ppt). Их можно просматривать в любом текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="c4ce6-p107">**Пропуск текста**: этот дополнительный компонент определяется после запуска процесса и перед анализ. Пропуск текста следует использовать с осторожностью, так как его использование может снизить производительность анализа файла.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="c4ce6-130">**Многоязычный текст**: расширенные обнаружения электронных данных в настоящее время не обрабатывает многоязычных имена тегов, custodian и проблемы.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="c4ce6-p108">**Метаданные**: определение метаданных, которую требуется сохранить социальной базы данных для последующего использования, таких как диапазон дат, размер файла, тип файла, custodian и субъектов. Метаданные могут быть загружены после уже загруженных файлов без перезапуска запасов или добавление повторной обработки дополнительную нагрузку.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="c4ce6-p109">Если файлы изначально были загружены по пути, сопоставление столбца "путь" во время импорта метаданных более поздней версии. Можно ссылаться на файл по Идентификатору и сопоставить другой путь. Это полезно сценарий при изменении пути к файлам.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="c4ce6-p110">Если файлы изначально были загружены по Идентификатору файла, сопоставьте столбец идентификатора при загрузке метаданных. Ссылка на файл по пути (а не идентификатор) будет отображено файлов необходимо повторно загрузить с другой идентификатор. Расширенные eDiscovery создает копии файлов вместо этого загрузки метаданных существующие файлы.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="c4ce6-139">**Семейства операционных систем**: невозможно загрузить семейства без его родителя (head семейства).</span><span class="sxs-lookup"><span data-stu-id="c4ce6-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="c4ce6-p111">**Размер файла**: нет отсутствие ограничения на размер файлов, загруженных в расширенной обнаружения электронных данных. Для analysis (анализ, релевантности, и т.д.) ограничение составляет 5,242,880 символов извлеченный текст. Большие файлы игнорируются (, например в релевантности, файлы не участвует в процессе учебный курс по релевантности и не получают показатель релевантности после расчета пакета).</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="c4ce6-p112">**Количество файлов**: нет рекомендуемые ограничения на количество файлов, которые могут быть обработаны в одном случае. Производительность зависит от ресурсов в системе.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="c4ce6-145">Фильтрация файлов</span><span class="sxs-lookup"><span data-stu-id="c4ce6-145">Filtering files</span></span>

<span data-ttu-id="c4ce6-p113">Пользовательские метки могут быть связаны с набор файлов, чтобы исключить их из процесса или другие задачи. Каждого сеанса процесс связан с идентификатором пакета. Несмотря на то, что идентификатор пакета не отображается для экспертов по релевантности, это можно сделать с помощью служебной программы поиска, путем добавления фильтра для текущего пакета и все соответствующие файлы с пользовательской меткой тегирования.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4ce6-149">См. также</span><span class="sxs-lookup"><span data-stu-id="c4ce6-149">See also</span></span>

[<span data-ttu-id="c4ce6-150">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="c4ce6-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="c4ce6-151">Под управлением модуля процесса и загрузка данных</span><span class="sxs-lookup"><span data-stu-id="c4ce6-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="c4ce6-152">Просмотр результатов процесса модуля</span><span class="sxs-lookup"><span data-stu-id="c4ce6-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

