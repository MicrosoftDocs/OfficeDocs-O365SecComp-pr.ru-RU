---
title: Расширенная индексация данных для расследования
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
ms.openlocfilehash: 2e2077fa5ee5333a563470d5bcbb140364bc0ba2
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150781"
---
# <a name="advanced-indexing-of-data-for-an-investigation"></a><span data-ttu-id="54380-102">Расширенная индексация данных для расследования</span><span class="sxs-lookup"><span data-stu-id="54380-102">Advanced indexing of data for an investigation</span></span>

<span data-ttu-id="54380-103">Содержимое в действующей системе может частично индексироваться по ряду причин, в том числе наличия изображений, неподдерживаемых типов файлов или при обнаружении ограничения на размер файлов индексирования.</span><span class="sxs-lookup"><span data-stu-id="54380-103">Content in the live system can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.</span></span> <span data-ttu-id="54380-104">При использовании сброса данных с высоким уровнем риска необходимо убедиться, что поиск сохранил все данные, которые нужно исследовать.</span><span class="sxs-lookup"><span data-stu-id="54380-104">When you are dealing with high risk data spill, you want to make sure that your search captured all data that you want to investigate.</span></span> <span data-ttu-id="54380-105">Когда интересующий пользователь добавляется в анализ данных, любое содержимое в Office 365, которое было признано частичным индексированием, будет повторно обработано, чтобы сделать его полным поиском.</span><span class="sxs-lookup"><span data-stu-id="54380-105">When a person of interest is added to a Data investigation, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.</span></span> <span data-ttu-id="54380-106">Этот процесс называется *расширенной индексацией*.</span><span class="sxs-lookup"><span data-stu-id="54380-106">This process is called *Advanced indexing*.</span></span> 

<span data-ttu-id="54380-107">Дополнительные сведения о поддержке обработки в Office 365 и частично индексированных элементах приведены в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="54380-107">To learn more about processing support in Office 365 and partially indexed items, see:</span></span>

- [<span data-ttu-id="54380-108">Поддерживаемые типы файлов при расследовании данных</span><span class="sxs-lookup"><span data-stu-id="54380-108">Supported file types in Data Investigations</span></span>](supported-filetypes-datainvestigations.md)

- [<span data-ttu-id="54380-109">Частично индексированные элементы в средстве "Поиск контента" в Office 365</span><span class="sxs-lookup"><span data-stu-id="54380-109">Partially indexed items in Content Search in Office 365</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)

- [<span data-ttu-id="54380-110">Форматы файлов, индексируемые службой поиска Exchange</span><span class="sxs-lookup"><span data-stu-id="54380-110">File formats indexed by Exchange Search</span></span>](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [<span data-ttu-id="54380-111">Анализируемые типы файлов и расширения имен файлов для обхода по умолчанию в SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="54380-111">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="54380-112">Просмотр результатов расширенного индексирования</span><span class="sxs-lookup"><span data-stu-id="54380-112">Viewing Advanced indexing results</span></span>

<span data-ttu-id="54380-113">После выполнения расширенного процесса индексирования можно получить сведения о эффективности повторной обработки.</span><span class="sxs-lookup"><span data-stu-id="54380-113">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.</span></span>  <span data-ttu-id="54380-114">В представлении индексирование интересов на диаграмме представлены все элементы, добавленные в *гибридный индекс*.</span><span class="sxs-lookup"><span data-stu-id="54380-114">In the People of interest indexing view, the graph lists all items added to the *hybrid index*.</span></span>  <span data-ttu-id="54380-115">Гибридный индекс — это место, в котором расследования данных (Предварительная версия) сохраняет повторно обработанное содержимое.</span><span class="sxs-lookup"><span data-stu-id="54380-115">The hybrid index is where Data Investigations (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="54380-116">На диаграмме также представлено количество элементов, для которых требуется исправление, и еще один график ошибок по типам файлов.</span><span class="sxs-lookup"><span data-stu-id="54380-116">The graph also includes the number of items that require remediation and another graph of errors by file type.</span></span> <span data-ttu-id="54380-117">Дополнительные сведения см. в разделе [Устранение ошибок при обработке данных](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="54380-117">For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-people-of-interest"></a><span data-ttu-id="54380-118">Обновление расширенных индексов для интересующих людей</span><span class="sxs-lookup"><span data-stu-id="54380-118">Updating Advanced indexes for people of interest</span></span>

<span data-ttu-id="54380-119">Когда интересующий пользователь добавляется в анализ данных, все частично индексированные элементы обрабатываются повторно.</span><span class="sxs-lookup"><span data-stu-id="54380-119">When a person of interest is added to a data investigation, all partially indexed items are re-processed.</span></span> <span data-ttu-id="54380-120">Однако с течением времени в почтовый ящик пользователя или в учетную запись OneDrive можно добавить более частично индексированные элементы.</span><span class="sxs-lookup"><span data-stu-id="54380-120">However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.</span></span>  <span data-ttu-id="54380-121">При необходимости вы можете обновить индексы.</span><span class="sxs-lookup"><span data-stu-id="54380-121">When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="54380-122">Обновление индексов людей — длительный процесс.</span><span class="sxs-lookup"><span data-stu-id="54380-122">Updating people of interest indexes is a long running process.</span></span> <span data-ttu-id="54380-123">Рекомендуется не обновлять индексы более одного раза в течение одного дня при расследовании.</span><span class="sxs-lookup"><span data-stu-id="54380-123">It's recommended that you don't update indexes more than once per day in an investigation.</span></span>
