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
ms.openlocfilehash: 032d93ef0990ed1dd7c1ea7bf2ba16653b3a862f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218859"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="26cfe-103">Повторный поиск контента для устранения ошибки размещения контента</span><span class="sxs-lookup"><span data-stu-id="26cfe-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="26cfe-104">При использовании поиска контента в центре безопасности _Амп_ по безопасности Office 365 для поиска очень большого количества почтовых ящиков (например, при поиске 100 000 почтовых ящиков или нескольких в одной системе поиска контента) могут возникнуть ошибки поиска, аналогичные приведенным ниже.</span><span class="sxs-lookup"><span data-stu-id="26cfe-104">When you use Content Search in the Office 365 Security & Compliance Center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="26cfe-p101">Эти ошибки (коды ошибок CS008-009 и CS012-002) указывают на то, что при поиске контента не удалось выполнить поиск определенных расположений содержимого; в этом примере не выполнялся поиск двух почтовых ящиков. Эти ошибки отображаются на всплывающей странице "сведения о состоянии" для поиска контента.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p101">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched. These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="26cfe-107">Причина ошибок расположения контента</span><span class="sxs-lookup"><span data-stu-id="26cfe-107">Cause of content location errors</span></span>

<span data-ttu-id="26cfe-p102">При поиске большого количества почтовых ящиков Поиск распространяется между тысячами серверов в центре обработки данных Майкрософт. В любой момент некоторые серверы могут находиться в состоянии перезагрузки или в процессе отработки отказа для избыточных копий. В любом из этих случаев запрос поиска контента для получения данных будет иметь время ожидания. В предыдущем примере ошибки для почтовых ящиков, для которых не удалось выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p102">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter. At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies. In either of these cases, the Content Search's request to retrieve data will timeout. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="26cfe-112">Устранение ошибок в расположении контента</span><span class="sxs-lookup"><span data-stu-id="26cfe-112">Resolving content location errors</span></span>

<span data-ttu-id="26cfe-p103">Перезапуск поиска часто приводит к возникновению подобных ошибок на разных серверах. Вместо перезапуска поиска нажмите кнопку **Retry (повторить** ), которая отображается в верхней части страницы результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p103">Restarting the search will often result in similar errors on different servers. Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Нажмите кнопку "повторить", чтобы устранить ошибки расположения контента](media/retrycontentsearch3.png)

<span data-ttu-id="26cfe-p104">Это приведет к повторной попытке поиска только для почтовых ящиков, для которых произошел сбой. При повторном выполнении поиска остальные возвращенные результаты сохраняются.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p104">This will result in the retrying the search only for the mailboxes that failed. When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="26cfe-118">Советы по предотвращению ошибок расположения контента</span><span class="sxs-lookup"><span data-stu-id="26cfe-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="26cfe-119">Ниже приведено несколько дополнительных причин ошибок в расположении контента, а также некоторые советы, которые помогут избежать их при поиске в большом количество почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="26cfe-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="26cfe-p105">Почтовые ящики, в которых выполняется поиск, могут быть заняты из-за активности пользователя. В этом случае служба поиска может перерегулироваться, чтобы предотвратить недоступность почтового ящика. Чтобы избежать этого, попробуйте выполнить поиск в нерабочие часы.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p105">The mailbox being searched might be busy due to user activity. In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable. To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="26cfe-p106">Поисковый запрос может получать слишком много контента из почтового ящика. Если это возможно, попробуйте сузить область поиска с помощью ключевых слов, диапазонов дат и условий поиска.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p106">The search query might be retrieving too much content from the mailbox. If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="26cfe-p107">Слишком много ключевых слов или ключевых слов при создании поискового запроса с помощью [списка ключевых слов](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). При запуске поискового запроса, использующего список ключевых слов, служба по сути выполняет отдельный поиск для каждой строки в списке ключевых слов, чтобы можно было создать статистику. Если вы используете список ключевых слов в поисковых запросах, сократите количество строк в списке ключевых слов или разделите их на более мелкие списки и создайте различные поисковые значения для каждого списка ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p107">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated. If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="26cfe-128">Для сокращения проблем, вызванных списками с большими ключевыми словами, вы можете ограничить до 20 строк в списке ключевых слов поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="26cfe-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="26cfe-p108">Одновременно выполняется слишком много операций поиска для одного и того же почтового ящика. Если это возможно, попробуйте запустить один поиск одновременно по одному почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p108">Too many searches are being performed on the same mailbox at the same time. If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="26cfe-p109">Поиск слишком большого количества почтовых ящиков за один поисковый запрос. Вероятность ошибок расположения содержимого возрастает при поиске большого количества почтовых ящиков. Если это возможно, попробуйте выполнить несколько операций поиска, чтобы каждый из них включал в себя подмножество почтовых ящиков в Организации.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p109">Searching too many mailboxes in a single search. The probability of content location errors increases when searching a very large number of mailboxes. If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="26cfe-p110">В почтовом ящике должно выполняться обслуживание. Несмотря на то что это может произойти нечасто, подождите немного, пока не будет получено сообщение об ошибке расположения контента, а затем повторите поиск.</span><span class="sxs-lookup"><span data-stu-id="26cfe-p110">Required maintenance is being performed on the mailbox. Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
