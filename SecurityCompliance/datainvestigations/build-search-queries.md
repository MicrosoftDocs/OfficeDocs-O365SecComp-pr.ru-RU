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
description: Использование ключевых слов и условий для сужения области поиска при использовании расследования данных в Microsoft 365.
ms.openlocfilehash: eeca1bf7ff89d1b7f79ceeed3334668e354f035a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262899"
---
# <a name="build-search-queries"></a><span data-ttu-id="bf912-103">Создание поисковых запросов</span><span class="sxs-lookup"><span data-stu-id="bf912-103">Build search queries</span></span>

<span data-ttu-id="bf912-104">При создании поисковых запросов можно использовать ключевые слова для поиска определенного содержимого и условий, чтобы сузить область поиска для возврата элементов, наиболее релевантных для вашего расследования.</span><span class="sxs-lookup"><span data-stu-id="bf912-104">When building search queries, you can use keywords to find specific content and conditions to narrow the scope of the search to return items that are most relevant to your investigation.</span></span>

![Использование ключевых слов и условий для сужения результатов поиска](../media/SearchQueryBox.png)

## <a name="keyword-searches"></a><span data-ttu-id="bf912-106">Поиск по ключевым словам</span><span class="sxs-lookup"><span data-stu-id="bf912-106">Keyword searches</span></span>

<span data-ttu-id="bf912-107">Введите запрос ключевого слова в поле **Ключевые слова** в запросе поиска.</span><span class="sxs-lookup"><span data-stu-id="bf912-107">Type a keyword query in the **Keywords** box in the search query.</span></span> <span data-ttu-id="bf912-108">Можно указать ключевые слова, свойства сообщений электронной почты (например, даты отправки и получения) или свойства документа (такие как имена файлов или Дата последнего изменения документа).</span><span class="sxs-lookup"><span data-stu-id="bf912-108">You can specify keywords, email message properties, (such as sent and received dates), or document properties (such as file names or the date that a document was last changed).</span></span> <span data-ttu-id="bf912-109">Можно использовать более сложные запросы, которые используют логический оператор, например **and**, **or**, **Not**и **NEAR**.</span><span class="sxs-lookup"><span data-stu-id="bf912-109">You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="bf912-110">Кроме того, можно искать конфиденциальные сведения (например, номера социального страхования) в документах SharePoint и OneDrive (не в сообщениях электронной почты) или искать документы, к которым предоставлен доступ извне.</span><span class="sxs-lookup"><span data-stu-id="bf912-110">You can also search for sensitive information (such as social security numbers) in documents in SharePoint and OneDrive (not in email messages), or search for documents that have been shared externally.</span></span> <span data-ttu-id="bf912-111">Если оставить поле **Ключевые слова** пустым, в результаты поиска будут включены все содержимое, расположенное в указанных расположениях контента.</span><span class="sxs-lookup"><span data-stu-id="bf912-111">If you leave the **Keywords** box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="bf912-112">Кроме того, можно щелкнуть флажок **Показать список ключевых слов** , а затем ввести ключевое слово или ключевое слово ключевое слово в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="bf912-112">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword or keyword phrase in each row.</span></span> <span data-ttu-id="bf912-113">В этом случае ключевые слова в каждой строке соединяются логическим оператором (представленным как *к:с*), который аналогичен оператору **or** в созданном запросе поиска.</span><span class="sxs-lookup"><span data-stu-id="bf912-113">If you do this, the keywords in each row are connected by a logical operator (which is represented as *c:s*) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> <span data-ttu-id="bf912-114">Это означает, что элементы, содержащие любое ключевое слово в любой строке, будут включены в результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="bf912-114">This means that items that contain any keyword in any row will be included in the search results.</span></span>

![Использование списка ключевых слов для получения статистики по всем ключевым словам в запросе](../media/KeywordListSearch.png)

<span data-ttu-id="bf912-116">Зачем использовать список ключевых слов?</span><span class="sxs-lookup"><span data-stu-id="bf912-116">Why use the keyword list?</span></span> <span data-ttu-id="bf912-117">Вы можете получить статистику по количеству элементов, которые совпадают с каждым ключевым словом в списке ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="bf912-117">You can get statistics that show how many items match each keyword in the keyword list.</span></span> <span data-ttu-id="bf912-118">Это поможет быстро определить наиболее эффективные (и наименее) Ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="bf912-118">This can help you quickly identify the keywords that are the most (and least) effective.</span></span> <span data-ttu-id="bf912-119">Кроме того, можно использовать ключевую фразу (заключенную в круглые скобки) в строке в списке ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="bf912-119">You can also use a keyword phrase (surrounded by parentheses) in a row in the keywords list.</span></span> <span data-ttu-id="bf912-120">Дополнительные сведения о статистике поиска можно найти в статье [Статистика поиска](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="bf912-120">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

> [!NOTE]
> <span data-ttu-id="bf912-121">Для сокращения проблем, вызванных списками с большими ключевыми словами, в списке ключевых слов можно ограничить до 20 строк.</span><span class="sxs-lookup"><span data-stu-id="bf912-121">To help reduce issues caused by large keyword lists, you're limited to a maximum of 20 rows in the keyword list.</span></span>

## <a name="conditions"></a><span data-ttu-id="bf912-122">Условия</span><span class="sxs-lookup"><span data-stu-id="bf912-122">Conditions</span></span>
    
<span data-ttu-id="bf912-123">Вы можете добавить условия поиска, чтобы сузить область поиска и возвратить более уточненный набор результатов.</span><span class="sxs-lookup"><span data-stu-id="bf912-123">You can add search conditions to narrow the scope of a search and return a more refined set of results.</span></span> <span data-ttu-id="bf912-124">Каждое условие добавляет в запрос поиска предложение, созданное и выполняемое при запуске поиска.</span><span class="sxs-lookup"><span data-stu-id="bf912-124">Each condition adds a clause to the search query that is created and run when you start the search.</span></span> <span data-ttu-id="bf912-125">Условие логически подключается к запросу ключевого слова (заданному в поле ключевое слово) логическим оператором (представленным как *к:к*), который аналогичен оператору **and** .</span><span class="sxs-lookup"><span data-stu-id="bf912-125">A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (which is represented as *c:c*) that is similar in functionality to the **AND** operator.</span></span> <span data-ttu-id="bf912-126">Это означает, что элементы должны удовлетворять как запрос ключевого слова, так и одно или несколько условий, включаемых в результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="bf912-126">That means that items have to satisfy both the keyword query and one or more conditions to be included in the search results.</span></span> <span data-ttu-id="bf912-127">Таким образом условия помогают сузить область результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="bf912-127">This is how conditions help to narrow your results.</span></span> <span data-ttu-id="bf912-128">Список и описание условий, которые можно использовать в поисковых запросах, представлены в разделе "условия поиска" в разделе [запросы и условия поиска ключевых слов](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="bf912-128">For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>