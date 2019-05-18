---
title: Сбор данных для обращения в Advanced eDiscovery
ms.author: esclee
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
ms.openlocfilehash: 8e67c3c8a693e627bade9e581f0f1e246bf6802a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151892"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery"></a><span data-ttu-id="1d0d9-102">Сбор данных для обращения в Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1d0d9-102">Collect data for a case in Advanced eDiscovery</span></span>

<span data-ttu-id="1d0d9-103">Определив custodians и источники данных, представляющие интерес для вашего случая, можно определить набор документов для delve.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-103">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="1d0d9-104">Вы можете использовать средство поиска в Advanced eDiscovery для идентификации этих кустодиал и расположений, не являющихся кустодиал в Office 365.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-104">You can use the Search tool in Advanced eDiscovery to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="1d0d9-105">После выполнения поиска вы сможете просматривать статистику извлеченных элементов, таких как расположения, в которых большинство элементов содержали поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-105">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="1d0d9-106">Кроме того, можно выполнить предварительный просмотр подмножества результатов.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-106">You can also preview a subset of the results.</span></span> <span data-ttu-id="1d0d9-107">После определения набора документов, которые необходимо проанализировать, можно добавить результаты поиска в набор проверки для сбора и обработки.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-107">When you've identified the set of documents that want to further examine, you can add the search results to a review set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="1d0d9-108">Create a search</span><span class="sxs-lookup"><span data-stu-id="1d0d9-108">Create a search</span></span>

<span data-ttu-id="1d0d9-109">При нажатии кнопки **Новый поиск** на вкладке **поиски** запустится мастер, который поможет создать поиск.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-109">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="1d0d9-110">Подробную информацию о том, как создать поиск, можно узнать в статье [Создание поиска для сбора данных](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="1d0d9-110">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="1d0d9-111">После создания поиска отображается раскрывающаяся страница со сведениями.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-111">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="1d0d9-112">Обратите внимание, что кнопки **Статистика** и **Предварительный просмотр** изначально отображаются серым цветом, так как поиск еще не завершен.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-112">Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet.</span></span> <span data-ttu-id="1d0d9-113">Вы можете следить за ходом выполнения поиска на вкладке поиски. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1d0d9-113">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="1d0d9-114">Просмотр результатов поиска и статистики</span><span class="sxs-lookup"><span data-stu-id="1d0d9-114">View search results and statistics</span></span>
<span data-ttu-id="1d0d9-115">Поиск контента состоит из двух компонентов: статистики (оценок) и предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-115">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="1d0d9-116">По мере завершения каждого из этих компонентов отображается состояние, отображаемое в соответствующих столбцах вкладки поисковые **запросы** изменяются с **отправленного** на **в состояние** **завершено**.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-116">As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="1d0d9-117">После завершения оценки нажмите кнопку поиска, чтобы отобразить раскрывающуюся страницу, в которой будет отображена определенная высокоуровневая статистика о результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-117">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="1d0d9-118">На этом шаге кнопка **Статистика** будет активна.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-118">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="1d0d9-119">Вы можете щелкнуть его, чтобы просмотреть статистику поиска, например:</span><span class="sxs-lookup"><span data-stu-id="1d0d9-119">You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="1d0d9-120">Сводка</span><span class="sxs-lookup"><span data-stu-id="1d0d9-120">Summary</span></span>
- <span data-ttu-id="1d0d9-121">Основные расположения</span><span class="sxs-lookup"><span data-stu-id="1d0d9-121">Top locations</span></span>
- <span data-ttu-id="1d0d9-122">Запросы</span><span class="sxs-lookup"><span data-stu-id="1d0d9-122">Queries</span></span>

<span data-ttu-id="1d0d9-123">Дополнительные сведения о статистике поиска можно найти в статье [Статистика поиска](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="1d0d9-123">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="1d0d9-124">После завершения предварительного просмотра кнопка **Предварительный просмотр** будет активна.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-124">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="1d0d9-125">Щелкните его, чтобы просмотреть образец подмножества результатов.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-125">Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-review-set"></a><span data-ttu-id="1d0d9-126">Добавление результатов поиска в набор проверки</span><span class="sxs-lookup"><span data-stu-id="1d0d9-126">Adding search results to a review set</span></span>

<span data-ttu-id="1d0d9-127">Когда вы будете готовы собирать и обрабатывать результаты поиска, вы можете сделать это, добавив его в набор рецензирования.</span><span class="sxs-lookup"><span data-stu-id="1d0d9-127">When you are ready to collect and process the entire results of a search, you can do so by adding it to a review set.</span></span> <span data-ttu-id="1d0d9-128">Дополнительные сведения см. в статье [Добавление данных в набор рецензирования](add-data-to-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="1d0d9-128">For details, see [Add data to a review set](add-data-to-review-set.md).</span></span> 