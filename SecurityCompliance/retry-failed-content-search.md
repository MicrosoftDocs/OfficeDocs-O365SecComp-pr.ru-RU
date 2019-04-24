---
title: Повторный поиск контента для устранения ошибки размещения контента
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Используйте кнопку Retry (повторить) для разрешения поиска контента с ошибками расположения контента.
ms.openlocfilehash: 8334ec053e86e48f99955af2d56e511a2df5c25a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261506"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="c7e38-103">Повторный поиск контента для устранения ошибки размещения контента</span><span class="sxs-lookup"><span data-stu-id="c7e38-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="c7e38-104">При использовании поиска контента в центре безопасности и соответствия требованиям для поиска очень большого количества почтовых ящиков (например, при поиске 100 000 почтовых ящиков в одной системе поиска контента) могут возникать ошибки поиска, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="c7e38-104">When you use Content Search in the security and compliance center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="c7e38-105">Эти ошибки (коды ошибок CS008-009 и CS012-002) указывают на то, что при поиске контента не удалось выполнить поиск определенных расположений содержимого; в этом примере не выполнялся поиск двух почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="c7e38-105">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched.</span></span> <span data-ttu-id="c7e38-106">Эти ошибки отображаются на всплывающей странице "сведения о состоянии" для поиска контента.</span><span class="sxs-lookup"><span data-stu-id="c7e38-106">These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="c7e38-107">Причина ошибок расположения контента</span><span class="sxs-lookup"><span data-stu-id="c7e38-107">Cause of content location errors</span></span>

<span data-ttu-id="c7e38-108">При поиске большого количества почтовых ящиков Поиск распространяется между тысячами серверов в центре обработки данных Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="c7e38-108">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter.</span></span> <span data-ttu-id="c7e38-109">В любой момент некоторые серверы могут находиться в состоянии перезагрузки или в процессе отработки отказа для избыточных копий.</span><span class="sxs-lookup"><span data-stu-id="c7e38-109">At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies.</span></span> <span data-ttu-id="c7e38-110">В любом из этих случаев запрос поиска контента для получения данных будет иметь время ожидания.</span><span class="sxs-lookup"><span data-stu-id="c7e38-110">In either of these cases, the Content Search's request to retrieve data will timeout.</span></span> <span data-ttu-id="c7e38-111">В предыдущем примере ошибки для почтовых ящиков, для которых не удалось выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="c7e38-111">In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="c7e38-112">Устранение ошибок в расположении контента</span><span class="sxs-lookup"><span data-stu-id="c7e38-112">Resolving content location errors</span></span>

<span data-ttu-id="c7e38-113">Перезапуск поиска часто приводит к возникновению подобных ошибок на разных серверах.</span><span class="sxs-lookup"><span data-stu-id="c7e38-113">Restarting the search will often result in similar errors on different servers.</span></span> <span data-ttu-id="c7e38-114">Вместо перезапуска поиска нажмите кнопку **Retry (повторить** ), которая отображается в верхней части страницы результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="c7e38-114">Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Нажмите кнопку "повторить", чтобы устранить ошибки расположения контента](media/retrycontentsearch3.png)

<span data-ttu-id="c7e38-116">Это приведет к повторной попытке поиска только для почтовых ящиков, для которых произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="c7e38-116">This will result in the retrying the search only for the mailboxes that failed.</span></span> <span data-ttu-id="c7e38-117">При повторном выполнении поиска остальные возвращенные результаты сохраняются.</span><span class="sxs-lookup"><span data-stu-id="c7e38-117">When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="c7e38-118">Советы по предотвращению ошибок расположения контента</span><span class="sxs-lookup"><span data-stu-id="c7e38-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="c7e38-119">Ниже приведено несколько дополнительных причин ошибок в расположении контента, а также некоторые советы, которые помогут избежать их при поиске в большом количество почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="c7e38-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="c7e38-120">Почтовые ящики, в которых выполняется поиск, могут быть заняты из-за активности пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7e38-120">The mailbox being searched might be busy due to user activity.</span></span> <span data-ttu-id="c7e38-121">В этом случае служба поиска может перерегулироваться, чтобы предотвратить недоступность почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="c7e38-121">In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable.</span></span> <span data-ttu-id="c7e38-122">Чтобы избежать этого, попробуйте выполнить поиск в нерабочие часы.</span><span class="sxs-lookup"><span data-stu-id="c7e38-122">To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="c7e38-123">Поисковый запрос может получать слишком много контента из почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="c7e38-123">The search query might be retrieving too much content from the mailbox.</span></span> <span data-ttu-id="c7e38-124">Если это возможно, попробуйте сузить область поиска с помощью ключевых слов, диапазонов дат и условий поиска.</span><span class="sxs-lookup"><span data-stu-id="c7e38-124">If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="c7e38-125">Слишком много ключевых слов или ключевых слов при создании поискового запроса с помощью [списка ключевых слов](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches).</span><span class="sxs-lookup"><span data-stu-id="c7e38-125">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches).</span></span> <span data-ttu-id="c7e38-126">При запуске поискового запроса, использующего список ключевых слов, служба по сути выполняет отдельный поиск для каждой строки в списке ключевых слов, чтобы можно было создать статистику.</span><span class="sxs-lookup"><span data-stu-id="c7e38-126">When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated.</span></span> <span data-ttu-id="c7e38-127">Если вы используете список ключевых слов в поисковых запросах, сократите количество строк в списке ключевых слов или разделите их на более мелкие списки и создайте различные поисковые значения для каждого списка ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="c7e38-127">If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="c7e38-128">Для сокращения проблем, вызванных списками с большими ключевыми словами, вы можете ограничить до 20 строк в списке ключевых слов поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="c7e38-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="c7e38-129">Одновременно выполняется слишком много операций поиска для одного и того же почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="c7e38-129">Too many searches are being performed on the same mailbox at the same time.</span></span> <span data-ttu-id="c7e38-130">Если это возможно, попробуйте запустить один поиск одновременно по одному почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="c7e38-130">If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="c7e38-131">Поиск слишком большого количества почтовых ящиков за один поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="c7e38-131">Searching too many mailboxes in a single search.</span></span> <span data-ttu-id="c7e38-132">Вероятность ошибок расположения содержимого возрастает при поиске большого количества почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="c7e38-132">The probability of content location errors increases when searching a very large number of mailboxes.</span></span> <span data-ttu-id="c7e38-133">Если это возможно, попробуйте выполнить несколько операций поиска, чтобы каждый из них включал в себя подмножество почтовых ящиков в Организации.</span><span class="sxs-lookup"><span data-stu-id="c7e38-133">If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="c7e38-134">В почтовом ящике должно выполняться обслуживание.</span><span class="sxs-lookup"><span data-stu-id="c7e38-134">Required maintenance is being performed on the mailbox.</span></span> <span data-ttu-id="c7e38-135">Несмотря на то что это может произойти нечасто, подождите немного, пока не будет получено сообщение об ошибке расположения контента, а затем повторите поиск.</span><span class="sxs-lookup"><span data-stu-id="c7e38-135">Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
