---
title: Расширенная индексация данных хранителя
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 158af8acf4acdb8ad6650c377a23b44ed28c6f54
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608218"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="1b277-102">Расширенная индексация данных хранителя</span><span class="sxs-lookup"><span data-stu-id="1b277-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="1b277-p101">Когда custodian добавляется к обращению eDiscovery расширенные (Предварительная версия), все содержимое в Office 365, подразумевается в качестве частично индексируются обрабатывается повторно, чтобы сделать для поиска.  Этот процесс называется *расширенное индексирование*. Содержимого могут быть индексированы частично по ряду причин, включая существование изображения, файлами неподдерживаемых типов или при обнаружении индексирования ограничения на размер файла.  Чтобы узнать больше о частично индексированных элементов, обратитесь к разделу [частично индексированных элементов в поиска контента в Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span><span class="sxs-lookup"><span data-stu-id="1b277-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="1b277-107">Просмотр расширенных индексирования результатов</span><span class="sxs-lookup"><span data-stu-id="1b277-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="1b277-p102">После выполнения расширенных процесса индексирования можно получить сведения о эффективность обработки повторно.  В представлении Custodian индексирования график список всех элементов, добавленных *гибридного индекса*.  Гибридного индекс находится где расширенные обнаружения электронных данных (Просмотр) хранит обрабатывается повторно содержимого.</span><span class="sxs-lookup"><span data-stu-id="1b277-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="1b277-p103">Графическое представление также включает число элементов, которые требуют обновлений и другой график ошибки по типу файла. Для получения дополнительных сведений см [исправлению ошибок во время обработки данных](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="1b277-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="1b277-113">Обновление расширенной индексов для custodians</span><span class="sxs-lookup"><span data-stu-id="1b277-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="1b277-p104">Когда custodian добавляется к обращению eDiscovery расширенные (Предварительная версия), частично индексированных элементов будет установлен обрабатывается повторно. Тем не менее как время прохода, частично более индексированных элементов могут быть добавлены почтового ящика или OneDrive учетной записи пользователя.  При необходимости можно обновлять индексы.</span><span class="sxs-lookup"><span data-stu-id="1b277-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="1b277-p105">Обновления индексов custodian является долгосрочного процесса. Рекомендуется не обновлять индексы несколько раз в день в случае.</span><span class="sxs-lookup"><span data-stu-id="1b277-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
