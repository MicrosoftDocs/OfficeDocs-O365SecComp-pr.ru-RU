---
title: Сбор данных для обращения в расширенной обнаружения электронных данных (Предварительная версия)
ms.author: esclee
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
ms.openlocfilehash: 6964cc00d7ae78078aa0729bd5408abd5ed9542a
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608264"
---
# <a name="collecting-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="1cd89-102">Сбор данных для обращения в расширенной обнаружения электронных данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="1cd89-102">Collecting data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="1cd89-p101">После определения custodians и источники данных, которые могут представлять интерес для вашей случая, настало время для идентификации набор документов для изучения. Можно использовать средство поиска в расширенной обнаружения электронных данных (Просмотр) для определения их из наказание и не являющиеся наказание расположений в Office 365.</span><span class="sxs-lookup"><span data-stu-id="1cd89-p101">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into. You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="1cd89-p102">После выполнения поиска можно просматривать статистику извлеченных элементов, таких как расположений, которым пришлось большинство элементов, которые соответствуют поисковый запрос. Также можно выполнить предварительный просмотр набор результатов. Если вы определили набор документов, которые хотите дальнейшего изучения, позволяет проводить рабочее множество для сбора и обработки результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="1cd89-p102">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query. You can also preview a subset of the results. When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="1cd89-108">Создать поиск</span><span class="sxs-lookup"><span data-stu-id="1cd89-108">Create a search</span></span>

<span data-ttu-id="1cd89-p103">После нажатия кнопки **нового поиска** на вкладке **Поиск** будет запущен мастер, руководство по созданию поиска. Подробные сведения о том, как создать поиск перейдите в раздел [Create поиска можно собирать данные](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="1cd89-p103">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search. For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="1cd89-p104">После создания поиска отображается страница всплывающее окно с подробными сведениями. Обратите внимание на то, что кнопки **статистики** и **предварительного просмотра** изначально серым, так как поиска еще не завершено. Вы можете отслеживания хода выполнения поиска на вкладке **поиска** .</span><span class="sxs-lookup"><span data-stu-id="1cd89-p104">After a search is created, a flyout page with details is displayed. Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet. You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="1cd89-114">Просмотр результатов поиска и статистики</span><span class="sxs-lookup"><span data-stu-id="1cd89-114">View search results and statistics</span></span>
<span data-ttu-id="1cd89-p105">Существует два компонента поиска контента: Статистика (оценки) и предварительного просмотра. Как каждый из этих компонентов завершена вы увидите состояние, отображаемое в соответствующие столбцы на вкладке **Поиск** и переход от с **Отправлено** для **выполняется** значение **завершено**.</span><span class="sxs-lookup"><span data-stu-id="1cd89-p105">There are two components of a content search: Statistics (Estimates) and Preview. As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="1cd89-p106">После завершения оценки поиска щелкните Поиск, чтобы отображать всплывающее окно страницы, который будет отображаться высокого уровня статистику о результатах поиска. На этом этапе кнопку **Статистика** станет активным. Можно щелкнуть его для просмотра статистики поиска, такие как:</span><span class="sxs-lookup"><span data-stu-id="1cd89-p106">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search. At this point, the **Statistics** button will be active. You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="1cd89-120">Сводка</span><span class="sxs-lookup"><span data-stu-id="1cd89-120">Summary</span></span>
- <span data-ttu-id="1cd89-121">Основные расположения</span><span class="sxs-lookup"><span data-stu-id="1cd89-121">Top locations</span></span>
- <span data-ttu-id="1cd89-122">Запросы</span><span class="sxs-lookup"><span data-stu-id="1cd89-122">Queries</span></span>
- <span data-ttu-id="1cd89-123">Уточнители</span><span class="sxs-lookup"><span data-stu-id="1cd89-123">Refiners</span></span>

<span data-ttu-id="1cd89-124">Дополнительные сведения о статистике поиска можно [Статистика поиска](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="1cd89-124">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="1cd89-p107">После завершения предварительной версии **Предварительный** Просмотр станет активным. Установите его для предварительного просмотра выборки набор результатов.</span><span class="sxs-lookup"><span data-stu-id="1cd89-p107">Once preview is completed, the **Preview** button will be active. Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="1cd89-127">Добавление результатов поиска в рабочий набор</span><span class="sxs-lookup"><span data-stu-id="1cd89-127">Adding search results to a working set</span></span>

<span data-ttu-id="1cd89-p108">Когда вы готовы для сбора и обработки всей результаты поиска, это можно сделать, добавив его рабочее множество. Дополнительные сведения см [Добавить данные в рабочий набор](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="1cd89-p108">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set. For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 