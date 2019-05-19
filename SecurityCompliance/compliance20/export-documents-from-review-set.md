---
title: Экспорт документов из набора для проверки
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 14efa58305e1963aa43c0c94fb208e5391c87119
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155071"
---
# <a name="export-documents-from-a-review-set"></a><span data-ttu-id="e0555-102">Экспорт документов из набора для проверки</span><span class="sxs-lookup"><span data-stu-id="e0555-102">Export documents from a review set</span></span>

<span data-ttu-id="e0555-103">Экспорт контента из набора проверки можно выполнить с помощью трех различных способов:</span><span class="sxs-lookup"><span data-stu-id="e0555-103">Exporting content from a review set can be accomplished via 3 different methods:</span></span>

## <a name="download"></a><span data-ttu-id="e0555-104">Скачать</span><span class="sxs-lookup"><span data-stu-id="e0555-104">Download</span></span>

<span data-ttu-id="e0555-105">Загрузка предлагает простой способ загрузки контента из набора проверки в собственном формате.</span><span class="sxs-lookup"><span data-stu-id="e0555-105">Download offers a simple way to download content from a review set in Native format.</span></span> <span data-ttu-id="e0555-106">Он использует функции передачи данных в браузере, поэтому приглашение браузера появится после того, как загрузка будет завершена.</span><span class="sxs-lookup"><span data-stu-id="e0555-106">It leverages the browser’s data transfer features so a browser prompt will appear once a download is ready.</span></span> <span data-ttu-id="e0555-107">Файлы, загруженные с помощью этого метода, будут архивированы в файл контейнера и будут файлами уровня элемента.</span><span class="sxs-lookup"><span data-stu-id="e0555-107">Files downloaded using this method will be zipped into a container file and will be item level files.</span></span> <span data-ttu-id="e0555-108">Это означает, что если вы выбрали вложение, вы автоматически получите сообщение электронной почты с включенным вложением.</span><span class="sxs-lookup"><span data-stu-id="e0555-108">This means that if you select an attachment, you will automatically receive the email with the attachment included.</span></span> <span data-ttu-id="e0555-109">Аналогично, если выбрать электронную таблицу Excel, внедренную в документ Word, вы получите документ Word с внедренной таблицей Excel.</span><span class="sxs-lookup"><span data-stu-id="e0555-109">Similarly, if you select an excel spreadsheet that was embedded in a word document, you will receive the word document with the excel spreadsheet embedded.</span></span> <span data-ttu-id="e0555-110">Скачанные элементы сохраняют дату последнего изменения, которую можно просмотреть в виде свойства файла.</span><span class="sxs-lookup"><span data-stu-id="e0555-110">Downloaded items will preserve the last modified date which can be viewed as a file property.</span></span>

<span data-ttu-id="e0555-111">Чтобы скачать контент из набора рецензирования, сначала выберите файлы, которые нужно скачать, а затем в меню действия выберите команду "Загрузить".</span><span class="sxs-lookup"><span data-stu-id="e0555-111">To download content from a review set, start by selecting the files you want to download then select “Download” under the Actions menu.</span></span>

![Снимок экрана с автоматически созданным описанием компьютера](../media/eDiscoDownload.png)

## <a name="export"></a><span data-ttu-id="e0555-113">Экспорт</span><span class="sxs-lookup"><span data-stu-id="e0555-113">Export</span></span>

<span data-ttu-id="e0555-114">Экспорт позволяет пользователям настраивать контент, включенный в загружаемый пакет.</span><span class="sxs-lookup"><span data-stu-id="e0555-114">Export allows users to customize the content that is included in the download package.</span></span> <span data-ttu-id="e0555-115">Она предоставляет страницу конфигурации со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="e0555-115">It provides a configuration page with the following settings:</span></span>

### <a name="metadata-file"></a><span data-ttu-id="e0555-116">Файл метаданных</span><span class="sxs-lookup"><span data-stu-id="e0555-116">Metadata file</span></span>

> <span data-ttu-id="e0555-117">Это можно считать "Загрузка файла", которая содержит метаданные, связанные с экспортированными файлами.</span><span class="sxs-lookup"><span data-stu-id="e0555-117">This can be considered your “load file” that contains metadata associated with the files you exported.</span></span> <span data-ttu-id="e0555-118">Список полей, доступных в файле метаданных, приведен в разделе \[Link.\]</span><span class="sxs-lookup"><span data-stu-id="e0555-118">For a list of fields available in the metadata file, see \[link\].</span></span> <span data-ttu-id="e0555-119">Этот файл, как правило, может быть вызван тремя средствами субъектов<sup>удаленных рабочих столов</sup> .</span><span class="sxs-lookup"><span data-stu-id="e0555-119">This file can typically be ingested by 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="tag-data"></a><span data-ttu-id="e0555-120">Данные тегов</span><span class="sxs-lookup"><span data-stu-id="e0555-120">Tag data</span></span>

> <span data-ttu-id="e0555-121">Этот контент будет добавлен в виде полей в файле метаданных.</span><span class="sxs-lookup"><span data-stu-id="e0555-121">This content would be added as fields in the metadata file.</span></span> <span data-ttu-id="e0555-122">Он содержит все сведения о тегах, применяемые в наборах рецензирования.</span><span class="sxs-lookup"><span data-stu-id="e0555-122">It contains all of the tag information applied in review sets.</span></span>

### <a name="text-files"></a><span data-ttu-id="e0555-123">Текстовые файлы</span><span class="sxs-lookup"><span data-stu-id="e0555-123">Text files</span></span>

> <span data-ttu-id="e0555-124">Для каждого файла, экспортированного из набора проверки, можно создать текстовые файлы.</span><span class="sxs-lookup"><span data-stu-id="e0555-124">Text files can be generated for each file exported from a review set.</span></span> <span data-ttu-id="e0555-125">Часто эти файлы необходимы партнерам по службам в процессе приема данных в 3 средства субъектов<sup>удаленных рабочих столов</sup> .</span><span class="sxs-lookup"><span data-stu-id="e0555-125">Often times these files are required by service partners as part of ingesting data into 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="redacted-files"></a><span data-ttu-id="e0555-126">Файлы отредактировал</span><span class="sxs-lookup"><span data-stu-id="e0555-126">Redacted files</span></span>

> <span data-ttu-id="e0555-127">Если во время проверки создаются отредактировал PDF, эти файлы доступны во время экспорта.</span><span class="sxs-lookup"><span data-stu-id="e0555-127">If redacted PDFs are generated during review, these files are available during export.</span></span> <span data-ttu-id="e0555-128">Пользователи могут выбрать, следует ли экспортировать только собственные файлы или заменить собственные файлы с исправлениями, записанными в PDF-файлах.</span><span class="sxs-lookup"><span data-stu-id="e0555-128">Users can decide whether to export native files only or to replace natives that have redactions with the burned in PDFs.</span></span>

### <a name="export-location"></a><span data-ttu-id="e0555-129">Папка для экспорта</span><span class="sxs-lookup"><span data-stu-id="e0555-129">Export Location</span></span>

> <span data-ttu-id="e0555-130">Экспортированное содержимое доставляется либо в предоставленный Майкрософт большой двоичный объект Azure, либо на большой двоичный объект клиента, если сведения предоставлены при экспорте.</span><span class="sxs-lookup"><span data-stu-id="e0555-130">Exported content is delivered to either a Microsoft provided Azure blob or a customer’s blob can be used if the details are provided at export.</span></span>

## <a name="export-structure"></a><span data-ttu-id="e0555-131">Экспорт структуры</span><span class="sxs-lookup"><span data-stu-id="e0555-131">Export Structure</span></span>

<span data-ttu-id="e0555-132">При экспорте контента из набора проверки его содержимое организуется в следующей структуре.</span><span class="sxs-lookup"><span data-stu-id="e0555-132">When content is exported from a review set, the content is organized in the following structure.</span></span>

  - <span data-ttu-id="e0555-133">Корневая папка — код скачивания</span><span class="sxs-lookup"><span data-stu-id="e0555-133">Root folder – Download ID</span></span>
    
      - <span data-ttu-id="e0555-134">Export\_файл\_Load. CSV = файл метаданных</span><span class="sxs-lookup"><span data-stu-id="e0555-134">Export\_load\_file.csv = metadata file</span></span>
    
      - <span data-ttu-id="e0555-135">Summary. txt = файл сводки со статистикой по экспорту</span><span class="sxs-lookup"><span data-stu-id="e0555-135">Summary.txt = a summary file with export statistics</span></span>
    
      - <span data-ttu-id="e0555-136">Входные\_или\_собственные файлы = содержит все собственные файлы</span><span class="sxs-lookup"><span data-stu-id="e0555-136">Input\_or native\_files = contains all native files</span></span>
    
      - <span data-ttu-id="e0555-137">Файлы\_ошибок = содержит все файлы ошибок, включенные в экспорт</span><span class="sxs-lookup"><span data-stu-id="e0555-137">Error\_files = contains any error files included in the export</span></span>
        
          - <span data-ttu-id="e0555-138">Екстрактионеррор — CSV-файл, который содержит все доступные метаданные файлов, которые не были должным образом извлечены из родительских файлов</span><span class="sxs-lookup"><span data-stu-id="e0555-138">ExtractionError – a csv that contains any available metadata of files that were not properly extracted from parent files</span></span>
        
          - <span data-ttu-id="e0555-139">Процессинжеррор — контент с ошибками обработки.</span><span class="sxs-lookup"><span data-stu-id="e0555-139">ProcessingError – content with processing errors.</span></span> <span data-ttu-id="e0555-140">Это содержимое имеет уровень элемента. Если во вложении возникла ошибка обработки, в эту папку будут включены сообщения электронной почты, содержащие вложение.</span><span class="sxs-lookup"><span data-stu-id="e0555-140">This content is item level meaning if an attachment experienced a processing error, the email that contains the attachment will be included in this folder.</span></span>
    
      - <span data-ttu-id="e0555-141">\_Извлеченные\_текстовые файлы = содержит все извлеченные текстовые файлы, созданные при обработке.</span><span class="sxs-lookup"><span data-stu-id="e0555-141">Extracted\_text\_files = contains all of the extracted text files generated at processing.</span></span>

## <a name="review-set"></a><span data-ttu-id="e0555-142">Обзор набора</span><span class="sxs-lookup"><span data-stu-id="e0555-142">review set</span></span>

<span data-ttu-id="e0555-143">Контент можно добавить в другой набор рецензирования.</span><span class="sxs-lookup"><span data-stu-id="e0555-143">Content can be added to another review set.</span></span>