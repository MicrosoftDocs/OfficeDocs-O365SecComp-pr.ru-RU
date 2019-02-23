---
title: Расширенная индексация данных хранителя
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218669"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="58cba-102">Расширенная индексация данных хранителя</span><span class="sxs-lookup"><span data-stu-id="58cba-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="58cba-p101">Когда хранитель добавляется к расширенному варианту обнаружения электронных данных (Preview), любое содержимое в Office 365, которое было признано частичным индексированием, повторно обрабатывается, чтобы сделать его полным поиском.  Этот процесс называется *расширенной индексацией*. Контент может частично индексироваться по ряду причин, в том числе наличия изображений, неподдерживаемых типов файлов или при обнаружении ограничения на размер файлов индексирования.  Чтобы узнать больше об частично индексированных элементах, просмотрите раздел [частично индексированные элементы в поиске контента в Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span><span class="sxs-lookup"><span data-stu-id="58cba-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="58cba-107">Просмотр результатов расширенного индексирования</span><span class="sxs-lookup"><span data-stu-id="58cba-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="58cba-p102">После выполнения расширенного процесса индексирования можно получить сведения о эффективности повторной обработки.  В представлении индексирования хранитель на диаграмме перечислены все элементы, добавленные в *гибридный индекс*.  Гибридный индекс там, где Advanced eDiscovery (Предварительная версия) сохраняет повторно обработанное содержимое.</span><span class="sxs-lookup"><span data-stu-id="58cba-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="58cba-p103">На диаграмме также представлено количество элементов, для которых требуется исправление, и еще один график ошибок по типам файлов. Дополнительные сведения см. в разделе [устраненИе ошибок при обработке данных](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="58cba-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="58cba-113">Обновление расширенных индексов для custodians</span><span class="sxs-lookup"><span data-stu-id="58cba-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="58cba-p104">Когда хранитель добавляется к расширенному варианту обнаружения электронных данных (Preview), все частично индексированные элементы обрабатываются повторно. Однако с течением времени в почтовый ящик пользователя или в учетную запись OneDrive можно добавить более частично индексированные элементы.  При необходимости вы можете обновить индексы.</span><span class="sxs-lookup"><span data-stu-id="58cba-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="58cba-p105">Обновление индексов хранитель выполняется длительным процессом. Рекомендуется не обновлять индексы более одного раза в день.</span><span class="sxs-lookup"><span data-stu-id="58cba-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
