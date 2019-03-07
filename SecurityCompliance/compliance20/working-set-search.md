---
title: Запрос данных в рабочем наборе
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
ms.openlocfilehash: 2523072181307cce510f0f318834329b2c70b376
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454991"
---
# <a name="query-the-data-in-a-working-set"></a><span data-ttu-id="5e8a0-102">Запрос данных в рабочем наборе</span><span class="sxs-lookup"><span data-stu-id="5e8a0-102">Query the data in a working set</span></span>

<span data-ttu-id="5e8a0-103">В большинстве случаев полезно иметь возможность глубже проанализировать то, что находится в рабочем наборе, и упорядочить их для более эффективного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-103">In most cases, it will be useful to be able to dig deeper into what is there in a working set and organize them to review more efficiently.</span></span> <span data-ttu-id="5e8a0-104">Запросы в рабочем наборе позволяют сделать это, позволяя сосредоточиться на подмножестве документов, которые удовлетворяют критериям, определенным вами одновременно.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-104">Queries within a working set enables you to do so by letting you focus on a subset of documents that meet the criteria defined by you at once.</span></span>

## <a name="creating-and-running-a-query-within-a-working-set"></a><span data-ttu-id="5e8a0-105">Создание и выполнение запроса в рабочем наборе</span><span class="sxs-lookup"><span data-stu-id="5e8a0-105">Creating and running a query within a working set</span></span>

<span data-ttu-id="5e8a0-106">Чтобы создать и запустить запрос в рабочем наборе, щелкните "новый запрос" в рабочем наборе.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-106">In order to create and run a query within your working set, click on "New Query" in your working set.</span></span> <span data-ttu-id="5e8a0-107">После задания имени запроса и определения условий нажмите кнопку Save (сохранить), чтобы выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-107">After you name your query and define the conditions, click "Save" to run the query.</span></span> <span data-ttu-id="5e8a0-108">Чтобы выполнить сохраненный ранее запрос, просто щелкните сохраненный запрос.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-108">To run a query that has been previously saved, simply click on the saved query.</span></span> <span data-ttu-id="5e8a0-109">Ссылки на [поля метаданных документа](document-metadata-fields.md) для списка метаданных, по которым можно выполнять поиск.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-109">Refer to [Document metadata fields](document-metadata-fields.md) for a list of metadata you can search by.</span></span>

## <a name="building-your-query"></a><span data-ttu-id="5e8a0-110">Создание запроса</span><span class="sxs-lookup"><span data-stu-id="5e8a0-110">Building your query</span></span>

<span data-ttu-id="5e8a0-111">Вы можете создать запрос, используя сочетание карточек условий и языка запросов в карточке условия ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-111">You can build your query using a combination of condition cards and query language in the Keywords condition card.</span></span>

### <a name="condition-card"></a><span data-ttu-id="5e8a0-112">Карточка условия</span><span class="sxs-lookup"><span data-stu-id="5e8a0-112">Condition card</span></span>

<span data-ttu-id="5e8a0-113">Каждое поле для поиска в рабочем наборе имеет соответствующую карточку условия, которую можно использовать для создания запроса.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-113">Every searchable field in a working set has a corresponding condition card that you can use to build your query.</span></span>

<span data-ttu-id="5e8a0-114">Существует несколько типов карточек условий:</span><span class="sxs-lookup"><span data-stu-id="5e8a0-114">There are multiple types of condition cards:</span></span>
- <span data-ttu-id="5e8a0-115">FREETEXT: карточка условия FREETEXT используется для текстовых полей, таких как тема.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-115">Freetext: freetext condition card is used for text fields such as subject.</span></span> <span data-ttu-id="5e8a0-116">Вы можете перечислить несколько терминов поиска, разделяя их запятыми.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-116">You can list multiple search terms by separating them out with a comma.</span></span>
- <span data-ttu-id="5e8a0-117">Дата: Дата условия используется для полей даты, таких как Дата последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-117">Date: date condition card is used for date fields such as last modified date.</span></span>
- <span data-ttu-id="5e8a0-118">Параметры поиска: в карточке с параметрами поиска в карточке будет представлен список возможных значений для определенного поля в рабочем наборе.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-118">Search options: search options condition card will provide a list of possible values for the particular field in your working set.</span></span> <span data-ttu-id="5e8a0-119">Используется для таких полей, как отправитель, где в рабочем наборе есть конечное число возможных значений.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-119">This is used for fields such as sender, where there is a finite number of possible values in your working set.</span></span>
- <span data-ttu-id="5e8a0-120">Ключевое слово: карточка условия для ключевых слов — это определенный экземпляр карточки условия FREETEXT, который можно использовать для поиска терминов или использовать KQL на языке запросов, аналогичный языку запросов в.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-120">Keyword: keyword condition card is a specific instance of freetext condition card that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="5e8a0-121">Более подробную информацию можно найти ниже.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-121">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="5e8a0-122">Язык запросов</span><span class="sxs-lookup"><span data-stu-id="5e8a0-122">Query language</span></span>

<span data-ttu-id="5e8a0-123">В дополнение к карточкам условий для создания запроса можно использовать язык запросов KQL в карточке ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="5e8a0-123">In addition to condition cards, you can use a KQL-like query language in the Keywords card to craft your query.</span></span> <span data-ttu-id="5e8a0-124">Язык запросов поддерживает стандартный синтаксис KQL, такой как AND, OR, NOT и NEAR (n).</span><span class="sxs-lookup"><span data-stu-id="5e8a0-124">The query language supports standard KQL syntax like AND, OR, NOT, and NEAR(n).</span></span> <span data-ttu-id="5e8a0-125">Он также поддерживает односимвольный подстановочный знак (?) и многозначный подстановочный знак (\*).</span><span class="sxs-lookup"><span data-stu-id="5e8a0-125">It also supports single-character wildcard (?) and multi-character wildcard (\*).</span></span>