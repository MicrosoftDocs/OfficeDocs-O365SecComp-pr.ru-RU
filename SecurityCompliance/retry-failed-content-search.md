---
title: Повторить поиск содержимого, чтобы устранить ошибку расположение содержимого
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Используйте кнопку "Повторить" для разрешения поиск содержимого, для которого настроено расположение содержимого ошибки.
ms.openlocfilehash: 0fdc11593fec42e1f9f9b76fbbb408d9c16fd183
ms.sourcegitcommit: d5f841744b716fcf368c670009b61441f5a5eed2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210198"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="7e671-103">Повторить поиск содержимого, чтобы устранить ошибку расположение содержимого</span><span class="sxs-lookup"><span data-stu-id="7e671-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="7e671-104">При использовании поиска контента в Office 365 безопасности & центре соответствия требованиям для поиска очень большое количество почтовых ящиков (например, поиск в 100 000 почтовых ящиков и многого другого в одном поиска контента) могут возникнуть ошибки поиска, похожие на следующие:</span><span class="sxs-lookup"><span data-stu-id="7e671-104">When you use Content Search in the Office 365 Security & Compliance Center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="7e671-p101">Эти ошибки (с коды ошибок CS008 009 и CS012-002) сообщение, что поиск содержимого для поиска конкретных размещения содержимого; в этом примере два почтовые ящики не были поиск. Эти ошибки отображаются на странице всплывающего сведения о состоянии поиска содержимого.</span><span class="sxs-lookup"><span data-stu-id="7e671-p101">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched. These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="7e671-107">Причиной ошибок расположение содержимого</span><span class="sxs-lookup"><span data-stu-id="7e671-107">Cause of content location errors</span></span>

<span data-ttu-id="7e671-p102">При поиске большое число почтовых ящиков, поиск распределены по тысячи серверов в центре обработки данных Майкрософт. В любой момент времени конкретных серверов может быть в состоянии перезагрузки или в процессе отработка отказа для резервных копий. В любом из этих случаев запрос поиска контента для извлечения данных будет времени ожидания. В предыдущем примере ошибки для почтовых ящиков, которые не удалось были результатов поиска времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="7e671-p102">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter. At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies. In either of these cases, the Content Search's request to retrieve data will timeout. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="7e671-112">Устранение ошибок расположение содержимого</span><span class="sxs-lookup"><span data-stu-id="7e671-112">Resolving content location errors</span></span>

<span data-ttu-id="7e671-p103">Перезапуск поиска часто приведет к похожие ошибки на разных серверах. Вместо перезапуска поиска, нажмите кнопку **Повторить** , который отображается в верхней части страницы результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="7e671-p103">Restarting the search will often result in similar errors on different servers. Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Нажмите кнопку "Повторить" для устранения ошибок расположение содержимого](media/retrycontentsearch3.png)

<span data-ttu-id="7e671-p104">В результате поиска только для почтовых ящиков, которые не удалось повтор. Если повторить поиск, другие результаты, которые были успешно возвращены, сохраняются.</span><span class="sxs-lookup"><span data-stu-id="7e671-p104">This will result in the retrying the search only for the mailboxes that failed. When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="7e671-118">Советы по предотвращению ошибки расположение содержимого</span><span class="sxs-lookup"><span data-stu-id="7e671-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="7e671-119">Ниже приведены некоторые причины сложения ошибок расположение содержимого и несколько советов, чтобы избежать их при поиске большого числа почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="7e671-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="7e671-p105">Почтовый ящик поиска может быть загружен из-за активности пользователя. В этом случае служба поиска может регулировать так, чтобы предотвратить почтового ящика становится недоступным. Чтобы избежать этого, попробуйте выполнить поиск во время часы.</span><span class="sxs-lookup"><span data-stu-id="7e671-p105">The mailbox being searched might be busy due to user activity. In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable. To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="7e671-p106">Поисковые запросы могут извлечение слишком много содержимого из почтового ящика. Если это возможно попробуйте сузить область поиска с помощью ключевых слов, диапазона дат и условия поиска.</span><span class="sxs-lookup"><span data-stu-id="7e671-p106">The search query might be retrieving too much content from the mailbox. If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="7e671-p107">Слишком много ключевые слова или фразы ключевое слово при создании поискового запроса с помощью [списка ключевых слов](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). При выполнении запроса поиска, который использует список ключевых слов, по сути запущена служба отдельные поиска для каждой строки в списке ключевое слово, чтобы статистики могут быть созданы. Если вы используете список ключевых слов в поисковых запросов, сократить число строк в списке ключевое слово или деления номеров ключевых слов в списки меньшего размера и создание различных поиска для каждого списка ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="7e671-p107">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated. If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="7e671-128">Чтобы уменьшить проблемы, связанные с ключевое слово больших списков, теперь вы ограничивается не более 20 строк в списке ключевого слова поискового запроса.</span><span class="sxs-lookup"><span data-stu-id="7e671-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="7e671-p108">Слишком много операций поиска при выполнении этого почтового ящика в то же время. Если это возможно попробуйте для выполнения поиска по одному на любой один почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="7e671-p108">Too many searches are being performed on the same mailbox at the same time. If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="7e671-p109">Поиск слишком большого числа почтовых ящиков в одной. Вероятность ошибки расположение содержимого увеличивается при поиске очень большое количество почтовых ящиков. Если это возможно попробуйте выполнить несколько поисков, чтобы каждый поиска включает в себя набор почтовых ящиков в организации.</span><span class="sxs-lookup"><span data-stu-id="7e671-p109">Searching too many mailboxes in a single search. The probability of content location errors increases when searching a very large number of mailboxes. If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="7e671-p110">Требуется обслуживание выполняется на почтовый ящик. Хотя в этом причина, вероятно, возникает редко, подождите немного времени после сообщение об ошибке расположение содержимого и повторите попытку поиска.</span><span class="sxs-lookup"><span data-stu-id="7e671-p110">Required maintenance is being performed on the mailbox. Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
