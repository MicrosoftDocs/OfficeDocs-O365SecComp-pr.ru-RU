---
title: Создание поисковых запросов
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
ms.openlocfilehash: e62d486b102fa035ae21b379d30bb0657b82acc9
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296222"
---
# <a name="build-search-queries"></a><span data-ttu-id="819af-102">Создание поисковых запросов</span><span class="sxs-lookup"><span data-stu-id="819af-102">Build search queries</span></span>

<span data-ttu-id="819af-103">При создании запроса можно использовать различные ключевые слова и условия для определения элементов, которые требуется найти.</span><span class="sxs-lookup"><span data-stu-id="819af-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="819af-104">Поиск по ключевым словам</span><span class="sxs-lookup"><span data-stu-id="819af-104">Keyword searches</span></span>

<span data-ttu-id="819af-p101">Введите поисковый запрос в поле **Ключевые слова** . Вы можете указать ключевые слова, свойства сообщений, такие как даты отправки и получения, или свойства документа, такие как имена файлов или Дата последнего изменения документа. Можно использовать более сложные запросы, которые используют логический оператор, например **and**, **or**, **Not**и **NEAR**. Кроме того, можно искать конфиденциальные сведения (например, номера социального страхования) в документах или искать документы, к которым предоставлен доступ извне. Если оставить поле ключевое слово пустым, в результаты поиска будут включены все содержимое, расположенное в указанных расположениях контента.</span><span class="sxs-lookup"><span data-stu-id="819af-p101">Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="819af-p102">Кроме того, можно щелкнуть флажок **Показать список ключевых слов** и ввести ключевое слово в каждой строке. В этом случае ключевые слова в каждой строке соединяются логическим оператором ( **к:с**), который аналогичен оператору **or** в созданном запросе поиска.</span><span class="sxs-lookup"><span data-stu-id="819af-p102">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="819af-p103">Зачем использовать список ключевых слов? Вы можете получить статистику по количеству элементов, которые совпадают с каждым ключевым словом. Это поможет быстро определить, какие ключевые слова являются самыми эффективными (и, как минимум) эффективными. Кроме того, в строке можно использовать ключевую фразу (заключенную в круглые скобки). Дополнительные сведения о статистике поиска можно найти в статье [Статистика поиска](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="819af-p103">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="819af-117">Условия</span><span class="sxs-lookup"><span data-stu-id="819af-117">Conditions</span></span>
    
<span data-ttu-id="819af-p104">Вы можете добавить условия поиска, чтобы сузить поиск и получить более уточненный набор результатов. Каждое условие добавляет в запрос поиска предложение, созданное и выполняемое при запуске поиска. Условие логически подключается к запросу ключевого слова (указанному в поле ключевое слово) логическим оператором (**к:к**), который аналогичен оператору **and** . Это означает, что элементы должны удовлетворять как запрос ключевого слова, так и одно или несколько условий, включаемых в результаты. Это то, как условия помогают сузить результаты. Список и описание условий, которые можно использовать в поисковых запросах, представлены в разделе "условия поиска" в разделе [запросы и условия поиска контента](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="819af-p104">You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


