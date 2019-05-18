---
title: Добавление результатов поиска в набор для проверки
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 4de390972672509422e055cd3fd6a9f65d54a7ba
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155241"
---
# <a name="add-search-results-to-a-review-set"></a><span data-ttu-id="6467a-102">Добавление результатов поиска в набор для проверки</span><span class="sxs-lookup"><span data-stu-id="6467a-102">Add search results to a review set</span></span>

<span data-ttu-id="6467a-103">При удовлетворении результатов поиска и готовности к просмотру и анализу этих результатов поиска их можно добавить в набор проверки в случае.</span><span class="sxs-lookup"><span data-stu-id="6467a-103">When you're satisfied with the results of a search and you're ready to review and analyze those search results, you can add them to a review set in the case.</span></span> <span data-ttu-id="6467a-104">Копирование исходных данных в набор рецензирования также упрощает процесс анализа и анализа, предоставляя расширенные средства анализа, такие как обнаружение тем, обнаружение близких копий и идентификация цепочки сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6467a-104">Copying the original data to the review set also facilitates the review and analysis process by providing you with advanced analytics tools such as themes detection, near-duplicate detection, and email thread identification.</span></span> <span data-ttu-id="6467a-105">Вы также можете добавлять данные из источников данных, отличных от Office 365, в набор проверки, чтобы вы могли просматривать эти данные в дополнение к данным, собранным из Office 365.</span><span class="sxs-lookup"><span data-stu-id="6467a-105">You can also add data from non-Office 365 data sources to a review set so that you can review that data in addition to the data you collect from Office 365.</span></span>

<span data-ttu-id="6467a-106">При добавлении результатов поиска в набор рецензирования (наборы рецензирования размещаются на вкладке "контрольные **наборы** ") выполняются следующие два действия:</span><span class="sxs-lookup"><span data-stu-id="6467a-106">When you add the results of a search to a review set (review sets are located on the **Review sets** tab of the case), the following two things occur:</span></span>

- <span data-ttu-id="6467a-107">Все элементы в результатах поиска копируются из исходного источника данных в службы Live Office 365 и копируются в безопасное место хранения Azure в облаке Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6467a-107">All items in the search results are copied from the original data source in the live Office 365 services, and copied to a secure Azure storage location in the Microsoft cloud.</span></span>

- <span data-ttu-id="6467a-108">Все элементы (включая содержимое и метаданные) переиндексируются таким образом, чтобы все данные в наборе проверки были полностью доступны для поиска во время проверки данных регистра.</span><span class="sxs-lookup"><span data-stu-id="6467a-108">All items (including the content and metadata) are re-indexed so that all data in the review set is fully searchable during the review of the case data.</span></span> <span data-ttu-id="6467a-109">Повторное индексирование результатов данных выполняется при поиске в наборе проверки в ходе анализа.</span><span class="sxs-lookup"><span data-stu-id="6467a-109">Re-indexing the data results in thorough and very fast searches when you search the data in the review set during the case investigation.</span></span>

<span data-ttu-id="6467a-110">Чтобы добавить данные в набор рецензирования, щелкните Поиск на вкладке **поиски** , а затем щелкните **Добавить результаты для проверки набора** на всплывающей странице.</span><span class="sxs-lookup"><span data-stu-id="6467a-110">To add data to a review set, click a search on the **Searches** tab and then click **Add results to review set** on the flyout page.</span></span>

![Добавление данных в набор проверки](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

<span data-ttu-id="6467a-112">Обратите внимание, что вы можете добавить существующий набор рецензирования или создать новый.</span><span class="sxs-lookup"><span data-stu-id="6467a-112">Note that you can add to an existing review set or create a new review set.</span></span>  <span data-ttu-id="6467a-113">При добавлении в новый набор проверки укажите имя и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="6467a-113">If adding to a new review set, specify the name and then click **Add**.</span></span>

![Выбор набора проверок](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

<span data-ttu-id="6467a-115">Добавление данных в набор проверки — длительный процесс.</span><span class="sxs-lookup"><span data-stu-id="6467a-115">Adding data to a review set is a long-running process.</span></span> <span data-ttu-id="6467a-116">Этот процесс включает сбор элементов из исходных источников данных в Office 365 (например, из почтовых ящиков и сайтов), копируя их в место хранения Azure (этот процесс копирования также называется \*\* приемом), а затем повторной индексации элементов.</span><span class="sxs-lookup"><span data-stu-id="6467a-116">This process includes gathering items from the original data sources in Office 365 (for example, from mailboxes and sites), copying them to the Azure storage location (this copying process is also called *ingestion*), and then re-indexing the items.</span></span> <span data-ttu-id="6467a-117">Отслеживать ход выполнения можно на вкладке " **задания** " или на вкладке \*\*\*\* "поиски", отслеживая состояние **добавленных данных в столбце "просмотреть набор** ".</span><span class="sxs-lookup"><span data-stu-id="6467a-117">You can track the progress on the **Jobs** tab or on the **Searches** tab by monitoring the status in the **Added data to review set** column.</span></span> <span data-ttu-id="6467a-118">После завершения обработки набора проверки перейдите на вкладку **Просмотр наборов** , а затем щелкните набор проверки, чтобы начать фильтрацию, проверку, маркировку и экспорт данных в набор проверки.</span><span class="sxs-lookup"><span data-stu-id="6467a-118">After the review set processing is completed, click the **Review sets** tab in the case, and then click the review set to start the process filtering, reviewing, tagging, and exporting data in the review set.</span></span>

## <a name="add-a-sample-to-a-review-set"></a><span data-ttu-id="6467a-119">Добавление примера в набор проверки</span><span class="sxs-lookup"><span data-stu-id="6467a-119">Add a sample to a review set</span></span>

<span data-ttu-id="6467a-120">Если требуется более тщательный поиск результатов поиска перед добавлением их в набор рецензирования, можно добавить образец результатов поиска в набор проверки, а не добавлять все.</span><span class="sxs-lookup"><span data-stu-id="6467a-120">If you want to validate the results of a search more thoroughly before adding all of them to a review set, you can add a sample of the search results to a review set instead of adding everything.</span></span>

<span data-ttu-id="6467a-121">Чтобы добавить пример в набор рецензирования, щелкните Поиск на вкладке поиски \*\*\*\* и выберите пункт **Пример** на всплывающей странице.</span><span class="sxs-lookup"><span data-stu-id="6467a-121">To add a sample to a review set, click a search on the **Searches** tab and click **Sample** on the flyout page.</span></span> <span data-ttu-id="6467a-122">На странице " **Параметры выборки** " выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="6467a-122">On the **Sampling parameters** page, choose one of the following options:</span></span>

- <span data-ttu-id="6467a-123">**Уровень вероятности%** и **доверительный интервал%** — элементы, добавляемые в набор проверки, будут определяться заданными статистическими параметрами.</span><span class="sxs-lookup"><span data-stu-id="6467a-123">**Confidence level %** and **Confidence interval %** - The items added to the review set will be determined by the statistical parameters that you set.</span></span> <span data-ttu-id="6467a-124">Если обычно используется уровень вероятности и интервал при выборке результатов, укажите их в раскрывающихся списках.</span><span class="sxs-lookup"><span data-stu-id="6467a-124">If you typically use a confidence level and interval when sampling results, specify them in the drop-down boxes.</span></span> <span data-ttu-id="6467a-125">В противном случае просто используйте параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6467a-125">Otherwise, just use the default settings.</span></span>

- <span data-ttu-id="6467a-126">**Случайная выборка%** — элементы, добавленные в набор проверки, основываются на случайном выборе указанного процента от общего числа элементов, возвращенных при поиске.</span><span class="sxs-lookup"><span data-stu-id="6467a-126">**Random sample %** - The items added to the review set is based on a random selection of the specified percentage of the total number of items returned by the search.</span></span>

<span data-ttu-id="6467a-127">Выбрав и настроив один из предыдущих параметров, выберите существующий набор рецензирования, чтобы добавить пример, а затем нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="6467a-127">After selecting and configuring one of the previous options, choose an existing review set to add the sample to and then click **Send**.</span></span> <span data-ttu-id="6467a-128">Кроме того, вы можете отслеживать ход выполнения на вкладке **задания** или **поиска** , отслеживая состояние в добавленных данных в столбце " **просмотреть набор** ".</span><span class="sxs-lookup"><span data-stu-id="6467a-128">Again, you can track the progress on the **Jobs** tab or on the **Searches** tab by monitoring the status in the **Added data to review set** column.</span></span>