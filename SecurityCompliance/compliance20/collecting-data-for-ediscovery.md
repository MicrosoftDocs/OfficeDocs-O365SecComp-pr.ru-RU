---
title: Сбор данных для обращения в Advanced eDiscovery (Предварительная версия)
ms.author: esclee
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: fb4b36841394576c44667f9677507c5655179e45
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242557"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="7e9ff-102">Сбор данных для обращения в Advanced eDiscovery (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="7e9ff-102">Collect data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="7e9ff-103">Определив custodians и источники данных, представляющие интерес для вашего случая, можно определить набор документов для delve.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-103">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="7e9ff-104">Вы можете использовать средство поиска в Advanced eDiscovery (Предварительная версия), чтобы определить их из расположений кустодиал и кустодиал в Office 365.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-104">You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="7e9ff-105">После выполнения поиска вы сможете просматривать статистику извлеченных элементов, таких как расположения, в которых большинство элементов содержали поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-105">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="7e9ff-106">Кроме того, можно выполнить предварительный просмотр подмножества результатов.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-106">You can also preview a subset of the results.</span></span> <span data-ttu-id="7e9ff-107">После определения набора документов, которые необходимо проанализировать, можно добавить результаты поиска в рабочий набор для сбора и обработки.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-107">When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="7e9ff-108">Create a search</span><span class="sxs-lookup"><span data-stu-id="7e9ff-108">Create a search</span></span>

<span data-ttu-id="7e9ff-109">При нажатии кнопки **Новый поиск** на вкладке **поиски** запустится мастер, который поможет создать поиск.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-109">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="7e9ff-110">Подробную информацию о том, как создать поиск, можно узнать в статье [Создание поиска для сбора данных](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="7e9ff-110">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="7e9ff-111">После создания поиска отображается раскрывающаяся страница со сведениями.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-111">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="7e9ff-112">Обратите внимание, что кнопки **Статистика** и **Предварительный просмотр** изначально отображаются серым цветом, так как поиск еще не завершен.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-112">Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet.</span></span> <span data-ttu-id="7e9ff-113">Вы можете следить за ходом выполнения поиска на вкладке поиски. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7e9ff-113">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="7e9ff-114">Просмотр результатов поиска и статистики</span><span class="sxs-lookup"><span data-stu-id="7e9ff-114">View search results and statistics</span></span>
<span data-ttu-id="7e9ff-115">Поиск контента состоит из двух компонентов: статистики (оценок) и предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-115">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="7e9ff-116">По мере завершения каждого из этих компонентов отображается состояние, отображаемое в соответствующих столбцах вкладки поисковые **запросы** изменяЮтся с **отправленного** на **в состояние** **завершено**.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-116">As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="7e9ff-117">После завершения оценки нажмите кнопку поиска, чтобы отобразить раскрывающуюся страницу, в которой будет отображена определенная высокоуровневая статистика о результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-117">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="7e9ff-118">На этом шаге кнопка **Статистика** будет активна.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-118">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="7e9ff-119">Вы можете щелкнуть его, чтобы просмотреть статистику поиска, например:</span><span class="sxs-lookup"><span data-stu-id="7e9ff-119">You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="7e9ff-120">Сводка</span><span class="sxs-lookup"><span data-stu-id="7e9ff-120">Summary</span></span>
- <span data-ttu-id="7e9ff-121">Основные расположения</span><span class="sxs-lookup"><span data-stu-id="7e9ff-121">Top locations</span></span>
- <span data-ttu-id="7e9ff-122">Запросы</span><span class="sxs-lookup"><span data-stu-id="7e9ff-122">Queries</span></span>

<span data-ttu-id="7e9ff-123">Дополнительные сведения о статистике поиска можно найти в статье [Статистика поиска](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="7e9ff-123">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="7e9ff-124">После завершения предварительного просмотра кнопка **предварительНый Просмотр** будет активна.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-124">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="7e9ff-125">Щелкните его, чтобы просмотреть образец подмножества результатов.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-125">Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="7e9ff-126">Добавление результатов поиска в рабочий набор</span><span class="sxs-lookup"><span data-stu-id="7e9ff-126">Adding search results to a working set</span></span>

<span data-ttu-id="7e9ff-127">Когда вы будете готовы собирать и обрабатывать результаты поиска, вы можете сделать это, добавив его в рабочий набор.</span><span class="sxs-lookup"><span data-stu-id="7e9ff-127">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set.</span></span> <span data-ttu-id="7e9ff-128">Дополнительные сведения см. в статье [Добавление данных в рабочий набор](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="7e9ff-128">For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 