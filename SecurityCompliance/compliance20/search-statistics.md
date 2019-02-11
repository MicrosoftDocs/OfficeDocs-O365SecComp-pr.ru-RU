---
title: Статистика поиска
ms.author: markjjo
author: esclee
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
ms.openlocfilehash: 0cfc1e5f04887cbdbcc0be8854fc50d6f9b5f1f2
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706010"
---
# <a name="search-statistics"></a><span data-ttu-id="11b12-102">Статистика поиска</span><span class="sxs-lookup"><span data-stu-id="11b12-102">Search statistics</span></span>

<span data-ttu-id="11b12-p101">Одним из способов можно проверить результаты поиска — это рассмотрение статистики вокруг результаты убедитесь, что они выровнять с этим рекомендациям. После завершения поиска высокого уровня статистики отображаются на всплывающих поиска сведений:</span><span class="sxs-lookup"><span data-stu-id="11b12-p101">One way you can validate your search results is to look at the statistics around your results to make sure they align with your expectations. When a search completes, high-level statistics are shown on the search details flyout:</span></span>
- <span data-ttu-id="11b12-105">Количество и размер элементов, извлеченные при поиске</span><span class="sxs-lookup"><span data-stu-id="11b12-105">Number and volume of items retrieved by the search</span></span>
- <span data-ttu-id="11b12-106">Количество и объем частично индексируются/неиндексированные элементы, обнаруженные в папках поиска</span><span class="sxs-lookup"><span data-stu-id="11b12-106">Number and volume of partially indexed/unindexed items that were found in the search locations</span></span>
- <span data-ttu-id="11b12-p102">Поиск числа почтовых ящиков и расположений. Чтобы просмотреть более подробную статистику, щелкните «Статистика» из всплывающего поиска сведений.</span><span class="sxs-lookup"><span data-stu-id="11b12-p102">Number of mailboxes and locations searched. In order to view more detailed statistics, click on "Statistics" from the search details flyout.</span></span>

## <a name="summary"></a><span data-ttu-id="11b12-109">Сводка</span><span class="sxs-lookup"><span data-stu-id="11b12-109">Summary</span></span>

<span data-ttu-id="11b12-p103">В представление сводки можно видеть результаты поиска, разбитые по тип расположения (например Exchange). Для каждого типа расположения можно увидеть:</span><span class="sxs-lookup"><span data-stu-id="11b12-p103">In Summary view, you can see the search results broken down by location type (e.g. Exchange). For each location type, you can see:</span></span>
- <span data-ttu-id="11b12-112">Число расположений, которым пришлось элементов, которые соответствуют условиям поиска</span><span class="sxs-lookup"><span data-stu-id="11b12-112">Number of locations that had items that matched the search conditions</span></span>
- <span data-ttu-id="11b12-113">Количество элементов из этих расположений, которые соответствуют условиям поиска</span><span class="sxs-lookup"><span data-stu-id="11b12-113">Number of items from these locations that matched the search conditions</span></span>
- <span data-ttu-id="11b12-114">Общий объем элементов, которые соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="11b12-114">Total volume of items that matched the search conditions.</span></span>

## <a name="top-locations"></a><span data-ttu-id="11b12-115">Основные расположения</span><span class="sxs-lookup"><span data-stu-id="11b12-115">Top locations</span></span>

<span data-ttu-id="11b12-p104">В представлении верхней расположения показаны отдельные расположения с наиболее совпадений. Для каждого места вы увидите:</span><span class="sxs-lookup"><span data-stu-id="11b12-p104">In Top locations view, you see the individual locations with the most matches. For each location, you will see:</span></span>
- <span data-ttu-id="11b12-118">Имя расположения (например URL-адрес SharePoint)</span><span class="sxs-lookup"><span data-stu-id="11b12-118">Location name (e.g. SharePoint URL)</span></span>
- <span data-ttu-id="11b12-119">тип расположения;</span><span class="sxs-lookup"><span data-stu-id="11b12-119">Location type</span></span>
- <span data-ttu-id="11b12-120">Число элементов, которые соответствуют условиям поиска</span><span class="sxs-lookup"><span data-stu-id="11b12-120">Number of items that matched the search conditions</span></span>
- <span data-ttu-id="11b12-121">Общий объем элементов, которые соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="11b12-121">Total volume of items that matched the search conditions.</span></span>

## <a name="queries"></a><span data-ttu-id="11b12-122">Запросы</span><span class="sxs-lookup"><span data-stu-id="11b12-122">Queries</span></span>

<span data-ttu-id="11b12-p105">При использовании ключевого слова (c:s) или ключевое слово строк в запросе, можно увидеть декомпозиции запроса в представление запросы на тип расположения. Для каждого типа расположения вы увидите:</span><span class="sxs-lookup"><span data-stu-id="11b12-p105">If you have used (c:s) keyword or keyword rows in your query, then you can see the breakdown of your query in Queries view per location type. For each location type, you will see:</span></span>

- <span data-ttu-id="11b12-p106">Часть: этот столбец будет иметь word «Основной» или «Ключевое слово». «Основной» означает, что строка предоставляет статистику о весь запрос в то время как «Ключевое слово» означает, что один из компонентов запросов.</span><span class="sxs-lookup"><span data-stu-id="11b12-p106">Part: this column will either have the word "Primary" or "Keyword". "Primary" means that the row presents statistics on the entire query, whereas "Keyword" means one of the query components.</span></span>

- <span data-ttu-id="11b12-p107">Запрос: компонент запроса фактические строки относится к. Если часть «Основной», это будет весь запрос; Если часть «Ключевое слово», вы увидите один из компонентов запросов здесь.</span><span class="sxs-lookup"><span data-stu-id="11b12-p107">Query: the actual query component the row refers to. If Part is "Primary", this will be the entire query; if Part was "Keyword", you will see one of the query components here.</span></span>
  
  - <span data-ttu-id="11b12-129">При выполнении поиска все почтовые ящики содержимого (, не указывая все ключевые слова), фактический запрос — (размер > = 0), чтобы возвращаются все элементы</span><span class="sxs-lookup"><span data-stu-id="11b12-129">When you search all contentin mailboxes (by not specifying any keywords), the actual query is (size >= 0) so that all items are returned</span></span>
  
  - <span data-ttu-id="11b12-130">При выполнении поиска SharePoint Online и OneDrive для бизнеса сайтов добавляются две следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="11b12-130">When you search SharePoint Online and OneDrive for Business sites, the two following components are added:</span></span>
    
    - <span data-ttu-id="11b12-131">НЕ IsExternalContent:1 - исключает любое содержимое из SharePoint в локальной организации</span><span class="sxs-lookup"><span data-stu-id="11b12-131">NOT IsExternalContent:1 - excludes any content from an on-premises SharePoint organization</span></span>
    
    - <span data-ttu-id="11b12-132">НЕ isOneNotePage: 1 — исключает все файлы OneNote, так как они должны быть дубликатов любого документа, отвечающей поисковому запросу.</span><span class="sxs-lookup"><span data-stu-id="11b12-132">NOT isOneNotePage: 1 - excludes all OneNote files because these would be duplicates of any document that matches the search query.</span></span>

- <span data-ttu-id="11b12-133">Число расположений, которым пришлось элементов, которые соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="11b12-133">Number of locations that had items that matched the search conditions.</span></span>

- <span data-ttu-id="11b12-134">Количество элементов из этих расположений, которые соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="11b12-134">Number of items from these locations that matched the search conditions.</span></span>

- <span data-ttu-id="11b12-135">Общий объем элементов, которые соответствуют условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="11b12-135">Total volume of items that matched the search conditions.</span></span>

## <a name="refiners"></a><span data-ttu-id="11b12-136">Уточнители</span><span class="sxs-lookup"><span data-stu-id="11b12-136">Refiners</span></span>

<span data-ttu-id="11b12-p108">Для почтовых ящиков Exchange уточнений представление дает дополнительных подразделений, ItemClass, отправителя и получателя. Для каждого места и уточнение значения можно видеть, сколько документов возвращенных в результате поиска.</span><span class="sxs-lookup"><span data-stu-id="11b12-p108">For Exchange mailboxes, refiners view gives you additional breakdowns by ItemClass, Sender, and Recipient. For each location and refiner value, you can see how many documents were returned in the search.</span></span>