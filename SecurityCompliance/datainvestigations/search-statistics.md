---
title: Статистика поиска
ms.author: markjjo
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
ms.openlocfilehash: 986c3f3cbb19cd0f66b18db274e68a3bf8414952
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258115"
---
# <a name="search-statistics"></a><span data-ttu-id="25e67-102">Статистика поиска</span><span class="sxs-lookup"><span data-stu-id="25e67-102">Search statistics</span></span>

<span data-ttu-id="25e67-103">Эффективный способ проверки результатов поиска при изучении инцидента данных — просмотреть статистику результатов поиска, чтобы убедиться в их соответствии ожиданиям.</span><span class="sxs-lookup"><span data-stu-id="25e67-103">An effective way to validate your search results when investigation a data incident is to view the statistics about your search results to make sure they align with your expectations.</span></span> <span data-ttu-id="25e67-104">При завершении поиска в разделе **Status (состояние** ) на всплывающей странице сведения о поиске отображается следующая высокоуровневая Статистика:</span><span class="sxs-lookup"><span data-stu-id="25e67-104">When a search as finished running, the following high-level statistics are displayed under **Status** on the search details flyout page:</span></span>

![Всплывающая страница "Поиск сведений о поиске" статисикс](../media/SearchDetailsFlyout.png)

- <span data-ttu-id="25e67-106">Предполагаемое количество и размер элементов, которые удовлетворяют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="25e67-106">The estimated number and size of items that matched the search criteria.</span></span>

- <span data-ttu-id="25e67-107">Число и размер частично индексированных элементов (также называемых неиндексированными *элементами*), которые не поддерживаются для поиска, но обнаружены в расположениях контента, включенных в поиск.</span><span class="sxs-lookup"><span data-stu-id="25e67-107">The number and size of partially indexed items (also called *unindexed items*) that aren't searchable but that were found in the content locations that were included in the search.</span></span>

- <span data-ttu-id="25e67-108">Количество выполненных почтовых ящиков и сайтов.</span><span class="sxs-lookup"><span data-stu-id="25e67-108">The number of mailboxes and sites that were searched.</span></span>

<span data-ttu-id="25e67-109">Чтобы просмотреть более подробную статистику, нажмите кнопку **Статистика** на всплывающей странице сведений о поиске.</span><span class="sxs-lookup"><span data-stu-id="25e67-109">To view more detailed statistics, click **Statistics** on the search details flyout page.</span></span> <span data-ttu-id="25e67-110">На странице **Статистика поиска** вы можете просмотреть сводку поиска, верхнюю область, содержащую элементы, которые совпадают с результатами поиска, и подробную статистику поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="25e67-110">On the **Search statistics** page, you can view the search summary, the top location that contained items that matched the search results, and detailed statistics about the search query.</span></span>

![Раскрывающийся список статистики поиска](../media/SearchStatisticsDropDownList.png)

## <a name="summary"></a><span data-ttu-id="25e67-112">Сводка</span><span class="sxs-lookup"><span data-stu-id="25e67-112">Summary</span></span>

<span data-ttu-id="25e67-113">В представлении **сводки** можно просмотреть результаты поиска, разбитые по типу расположения (например, расположения включают почтовые ящики Exchange и сайты SharePoint).</span><span class="sxs-lookup"><span data-stu-id="25e67-113">In the **Summary** view, you can see the search results broken down by location type (for example, locations include Exchange mailboxes and SharePoint sites).</span></span> <span data-ttu-id="25e67-114">Для каждого типа местоположения отображается следующая информация:</span><span class="sxs-lookup"><span data-stu-id="25e67-114">The following information is displayed for each location type:</span></span>

- <span data-ttu-id="25e67-115">Количество местоположений, в которых были элементы, соответствующие условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="25e67-115">The number of locations that had items that matched the search criteria.</span></span>

- <span data-ttu-id="25e67-116">Общее количество элементов из каждого типа расположения, которые удовлетворяют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="25e67-116">The total number of items from each location type that matched the search criteria.</span></span>

- <span data-ttu-id="25e67-117">Общий размер элементов из каждого типа, которые отвечают условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="25e67-117">The total size of items from each location type that matched the search criteria.</span></span>

## <a name="top-locations"></a><span data-ttu-id="25e67-118">Основные расположения</span><span class="sxs-lookup"><span data-stu-id="25e67-118">Top locations</span></span>

<span data-ttu-id="25e67-119">В представлении " **верхние места** " отображаются отдельные расположения контента с большинством элементов, которые удовлетворяют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="25e67-119">In the **Top locations** view, you see the individual content locations with the most items that matched the search criteria.</span></span> <span data-ttu-id="25e67-120">Для каждого расположения содержимого отображаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="25e67-120">For each content location, the following information is displayed:</span></span>

- <span data-ttu-id="25e67-121">Имя расположения; адрес электронной почты для почтовых ящиков и URL-адреса сайтов SharePoint</span><span class="sxs-lookup"><span data-stu-id="25e67-121">The name of the location; the email address for mailboxes and the URL for SharePoint sites</span></span>

- <span data-ttu-id="25e67-122">Тип расположения</span><span class="sxs-lookup"><span data-stu-id="25e67-122">The location type</span></span>

- <span data-ttu-id="25e67-123">Количество элементов, которые удовлетворяют условиям поиска</span><span class="sxs-lookup"><span data-stu-id="25e67-123">Number of items that matched the search criteria</span></span>

- <span data-ttu-id="25e67-124">Общий размер всех элементов, которые удовлетворяют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="25e67-124">The total size of all items that matched the search criteria.</span></span>

## <a name="queries"></a><span data-ttu-id="25e67-125">Запросы</span><span class="sxs-lookup"><span data-stu-id="25e67-125">Queries</span></span>

<span data-ttu-id="25e67-126">В представлении **запросы** можно просмотреть подробную статистику для каждого компонента поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="25e67-126">In the **Queries** view, you can see detailed statistics for each component of the search query.</span></span> <span data-ttu-id="25e67-127">Если вы использовали список ключевых слов в поисковом запросе, вы можете просматривать расширенные статистические данные в представлении **запросы** , которые показывают, сколько элементов совпадают с ключевыми словами или ключевыми словами.</span><span class="sxs-lookup"><span data-stu-id="25e67-127">If you used the keyword list in the search query, you can view enhanced statistics in the **Queries** view  that show how many items match each keyword or keyword phrase.</span></span> <span data-ttu-id="25e67-128">Это поможет быстро определить, какие части запроса являются самыми эффективными (и, как минимум).</span><span class="sxs-lookup"><span data-stu-id="25e67-128">This can help you quickly identify which parts of the query are the most (and least) effective.</span></span> 

<span data-ttu-id="25e67-129">В представлении **запросы** отображаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="25e67-129">The following information is displayed in the **Queries** view:</span></span>

 - <span data-ttu-id="25e67-130">**Тип расположения** — тип расположения содержимого для статистики, отображаемой в строке.</span><span class="sxs-lookup"><span data-stu-id="25e67-130">**Location type** - The type of content location for the statistics displayed in the row.</span></span>

- <span data-ttu-id="25e67-131">**Part** — в этом столбце отображается одно из следующих значений: **PRIMARY** или **ключевое слово**.</span><span class="sxs-lookup"><span data-stu-id="25e67-131">**Part** - This column will display one of the following values: **Primary** or **Keyword**.</span></span> <span data-ttu-id="25e67-132">**Основной** означает, что строка содержит статистику по всему запросу; **КлючевОе слово** означает, что статистика в строке соответствует одному из компонентов запроса.</span><span class="sxs-lookup"><span data-stu-id="25e67-132">**Primary** means the row presents statistics on the entire query; **Keyword** means the statistics in the row are for one of the query components.</span></span>

- <span data-ttu-id="25e67-133">**Condition** — фактический компонент запроса запроса поиска, на который ссылается строка.</span><span class="sxs-lookup"><span data-stu-id="25e67-133">**Condition** - The actual query component of the search query the row refers to.</span></span> <span data-ttu-id="25e67-134">Если значение в столбце **части** является **основным**, отображаются статистические данные всего поискового запроса; Если задано **ключевОе слово**value, отображаются статистические данные для компонента запроса, отображаемого в столбце **запрос** .</span><span class="sxs-lookup"><span data-stu-id="25e67-134">If the value in the **Part** column is **Primary**, then the statistics for the entire search query are displayed; if the value is **Keyword**, then the statistics for the component of the query shown in the **Query** column are displayed.</span></span> <span data-ttu-id="25e67-135">Например, если использовался список ключевых слов, отображается один из ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="25e67-135">For example, if the keyword list was used, then the statistics one of the keywords are displayed.</span></span>

  <span data-ttu-id="25e67-136">Ниже приведены дополнительные сведения о статистике, отображаемой в столбце **запросы** .</span><span class="sxs-lookup"><span data-stu-id="25e67-136">Here are some other things to know about the statistics displayed in the **Queries** column:</span></span>
  
  - <span data-ttu-id="25e67-137">При поиске всего содержимого в почтовых ящиках (без указания ключевых слов) фактическим запросом является **(Size _гт_ = 0)** , чтобы возвращались все элементы</span><span class="sxs-lookup"><span data-stu-id="25e67-137">When you search for all content in mailboxes (by not specifying any keywords), the actual query is **(size >= 0)** so that all items are returned</span></span>
  
  - <span data-ttu-id="25e67-138">При поиске на сайтах SharePoint и OneDrive в поисковый запрос добавляются два следующих компонента:</span><span class="sxs-lookup"><span data-stu-id="25e67-138">When you search SharePoint and OneDrive sites, the two following components are added to the search query:</span></span>
    
    <span data-ttu-id="25e67-139">**Не IsExternalContent: 1** — исключает любой контент из локальной организации SharePoint</span><span class="sxs-lookup"><span data-stu-id="25e67-139">**NOT IsExternalContent:1** - This excludes any content from an on-premises SharePoint organization</span></span>
    
    <span data-ttu-id="25e67-140">**Не исоненотепаже: 1** — исключает все файлы OneNote, так как они будут дублировать любой документ, соответствующий поисковому запросу.</span><span class="sxs-lookup"><span data-stu-id="25e67-140">**NOT isOneNotePage:1** - This excludes all OneNote files because these would be duplicates of any document that matches the search query.</span></span>

- <span data-ttu-id="25e67-141">**Расположения в поиске** Количество расположений контента, в которых были элементы, соответствующие запросу поиска для части или условия, отображаемых в строке.</span><span class="sxs-lookup"><span data-stu-id="25e67-141">**Locations in search** The number of content locations that had items that matched the search query for the part/condition displayed in the row.</span></span> <span data-ttu-id="25e67-142">Обратите внимание, что архивные почтовые ящики подсчитываются как отдельное расположение, если они содержат элементы, которые отвечают условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="25e67-142">Note that archive mailboxes are counted as a separate location if they contain items that match the search criteria.</span></span>

- <span data-ttu-id="25e67-143">**Items** — общее количество элементов, которые удовлетворяют критериям поиска для части или условия, отображаемых в строке.</span><span class="sxs-lookup"><span data-stu-id="25e67-143">**Items** - The total number of items that matched the search criteria for the part/condition displayed in the row.</span></span>

- <span data-ttu-id="25e67-144">**Size** — общее количество элементов, которые удовлетворяют критериям поиска для части или условия, отображаемых в строке.</span><span class="sxs-lookup"><span data-stu-id="25e67-144">**Size** - The total number of items that matched the search criteria for the part/condition displayed in the row.</span></span>