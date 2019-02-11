---
title: Создание поисковых запросов
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
ms.openlocfilehash: c337b49491fca11e0ba5bc13d22ac3e54038c400
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695075"
---
# <a name="build-search-queries"></a><span data-ttu-id="5ad96-102">Создание поисковых запросов</span><span class="sxs-lookup"><span data-stu-id="5ad96-102">Build search queries</span></span>

<span data-ttu-id="5ad96-103">В построение запроса, можно использовать различные ключевые слова и условия для определения элементов, предназначенных для поиска.</span><span class="sxs-lookup"><span data-stu-id="5ad96-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="5ad96-104">Поиска по ключевым словам</span><span class="sxs-lookup"><span data-stu-id="5ad96-104">Keyword searches</span></span>

<span data-ttu-id="5ad96-p101">Введите поисковый запрос в поле **ключевые слова** . Можно указать ключевые слова, сообщение свойства, например, отправленных и полученных даты, или свойств документа, таких как имена файлов или Дата последнего изменения документа. Можно использовать более сложные запросы, использующие логический оператор, например **и**, **или**, **не**и **NEAR**. Можно также выполнить поиск конфиденциальной информации (например, номера социального страхования) в документы или поиск документов, которые совместно извне. Если ключевое слово поле оставлено пустым, весь контент, расположенный в указанном расположении контента будут включены в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="5ad96-p101">Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="5ad96-p102">Кроме того щелкните флажок **Показать список ключевых слов** и тип ключевого слова в каждой строке. После этого ключевых слов в каждой строке, соединенных с логический оператор ( **c:s**), аналогичную функциональность оператор **OR** в запрос поиска, которая создается.</span><span class="sxs-lookup"><span data-stu-id="5ad96-p102">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="5ad96-p103">Причины использования список ключевых слов? Можно получить статистику, показывающие количество элементов соответствуют каждого ключевого слова. Это может помочь быстро определять, какие ключевые слова эффективны наиболее (и бы). Можно также использовать ключевая фраза (заключаются в круглые скобки) в строке. Дополнительные сведения о статистике поиска можно [статистики поиска](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="5ad96-p103">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="5ad96-117">Условия</span><span class="sxs-lookup"><span data-stu-id="5ad96-117">Conditions</span></span>
    
<span data-ttu-id="5ad96-p104">Можно добавить условия поиска для сужения области поиска и возвращать более качественных набора результатов. Каждое условие добавляет предложение в поисковый запрос, который создается и при запуске поиска. Условие по логический оператор (**c: c**), аналогичную функциональность **и** оператор логически подключение для запроса ключевого слова (указанного в поле ключевых слов). Который означает, что элементы для удовлетворения запроса ключевого слова и одно или несколько условий, которые будут включены в результаты. Это, как помочь условий, чтобы сузить результаты. Список и описание условий, которые можно использовать в запросе поиска обратитесь к разделу «Условия поиска» в [запросах по ключевым словам и условия поиска для поиска контента](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="5ad96-p104">You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


