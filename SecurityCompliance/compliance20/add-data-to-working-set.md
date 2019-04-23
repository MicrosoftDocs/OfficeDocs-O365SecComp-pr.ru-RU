---
title: Добавление результатов поиска в рабочий набор
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
ms.openlocfilehash: 7830b483190a69e6055fae369580064c5df42f49
ms.sourcegitcommit: f0e3c9de0b545081a4d264f74559b941f6c71410
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2019
ms.locfileid: "31958290"
---
# <a name="add-search-results-to-a-working-set"></a><span data-ttu-id="ff952-102">Добавление результатов поиска в рабочий набор</span><span class="sxs-lookup"><span data-stu-id="ff952-102">Add search results to a working set</span></span>

<span data-ttu-id="ff952-103">После определения и отбора при поиске в Exchange, SharePoint и OneDrive для бизнеса можно добавить результаты в рабочий набор.</span><span class="sxs-lookup"><span data-stu-id="ff952-103">After you've identified and culled with searches against Exchange, SharePoint and OneDrive for business, you can add the results to a working set.</span></span> <span data-ttu-id="ff952-104">Рабочие наборы представляют собой статический набор документов, которые будут индексироваться для быстрого поиска, проанализируйте идентификацию потока электронной почты, чтобы обнаружить дублирование и темы.</span><span class="sxs-lookup"><span data-stu-id="ff952-104">Working sets represent a static set of documents that we will index for lightning fast search results, analyze for email thread identification, near duplicate detection and themes.</span></span>  <span data-ttu-id="ff952-105">Вы также можете добавлять данные из источников данных, отЛичных от Office 365, в параллельный режим с данными, собранными из Office 365.</span><span class="sxs-lookup"><span data-stu-id="ff952-105">You can also add data from Non-Office 365 data sources to live side by side with the data you collect from Office 365.</span></span>

<span data-ttu-id="ff952-106">Чтобы добавить данные в рабочий набор, сначала выберите Поиск, а затем в результатах поиска нажмите кнопку *+ Добавить результаты в рабочий набор* .</span><span class="sxs-lookup"><span data-stu-id="ff952-106">To add data to a working set, start by selecting a search, in the search results fly out, click the *+ Add results to working set* button.</span></span>

![Добавление данных в рабочий набор](../media/c1b4fc00-7a15-4587-b9b0-ce594bb02e4d.png)

<span data-ttu-id="ff952-108">Затем можно добавить существующий рабочий набор или *новый рабочий набор*.</span><span class="sxs-lookup"><span data-stu-id="ff952-108">You can then choose to add to an existing working set or a *New working set*.</span></span>  <span data-ttu-id="ff952-109">Если добавляется к новому рабочему набору, укажите имя, а затем нажмите кнопку *Добавить* .</span><span class="sxs-lookup"><span data-stu-id="ff952-109">If adding to a new working set, specify the name and finally click the *Add* button.</span></span>

![Выбор рабочего набора](../media/e8c6ab51-da8d-4c39-9b21-26bfdf453fb9.png)

<span data-ttu-id="ff952-111">Добавление данных в рабочий набор — это длительный процесс, который можно отслеживать на вкладке "задания" или в столбце " *состояние рабочего задания* " на вкладке " *поиски* ".  Процесс включает сбор элементов из Office 365 и, наконец, _Амп_ индексирование.</span><span class="sxs-lookup"><span data-stu-id="ff952-111">Adding data to a working set is a long running process, you can either track the progress in the Jobs tab or in the *Working set status* column in the *Searches* tab.  The process includes gathering items from Office 365 and finally Ingestion & Indexing.</span></span>  <span data-ttu-id="ff952-112">После завершения обработки рабочего набора можно перейти к рабочему набору, щелкнув вкладку *рабочие наборы* , а затем выбрав рабочий набор.</span><span class="sxs-lookup"><span data-stu-id="ff952-112">Once working set processing is completed, you can navigate to the working set by clicking on the *Working Sets* tab and then clicking on the working set.</span></span>  <span data-ttu-id="ff952-113">Затем вы можете перейти к поиску, просмотру, маркировке и экспорту всех релевантных данных.</span><span class="sxs-lookup"><span data-stu-id="ff952-113">You can then move on to searching, reviewing, tagging and exporting any relevant data.</span></span>

## <a name="adding-a-sample-to-a-working-set"></a><span data-ttu-id="ff952-114">Добавление примера в рабочий набор</span><span class="sxs-lookup"><span data-stu-id="ff952-114">Adding a sample to a working set</span></span>

<span data-ttu-id="ff952-115">Если вы хотите проверить результаты поиска более сораугли, прежде чем собирать все документы, которые были получены при поиске, можно добавить случайный образец результатов поиска в рабочий набор, а не добавлять все.</span><span class="sxs-lookup"><span data-stu-id="ff952-115">If you would like to validate your search results more thorougly before collecting all documents that were retrieved by your search, you can add a random sample of the search results to a working set instead of adding everything.</span></span>

<span data-ttu-id="ff952-116">Чтобы добавить пример в рабочий набор, начните с выбора поиска в меню результаты поиска, нажмите кнопку *образец* .</span><span class="sxs-lookup"><span data-stu-id="ff952-116">To add a sample to a working set, start by selecting a search, in the search results flyout, click *Sample* button.</span></span>

<span data-ttu-id="ff952-117">Затем вы можете выбрать параметр выборки.</span><span class="sxs-lookup"><span data-stu-id="ff952-117">You can then choose the parameter of your sampling.</span></span> <span data-ttu-id="ff952-118">Возможны два указанных ниже значения параметра.</span><span class="sxs-lookup"><span data-stu-id="ff952-118">There are two options:</span></span>
- <span data-ttu-id="ff952-119">Уровень достоверности и интервал: выбор размера образца будет выбран для удовлетворения указанных статистических параметров.</span><span class="sxs-lookup"><span data-stu-id="ff952-119">Confidence level and interval: sample size will be chosen to satisfy the given statistical parameters.</span></span>
- <span data-ttu-id="ff952-120">Процент: размер выборки определяется на основе количества элементов, возвращенных при поиске, и выбранного параметра.</span><span class="sxs-lookup"><span data-stu-id="ff952-120">Percentage: sample size will be determined based on the number of items that was returned by the search, and the chosen parameter.</span></span>

<span data-ttu-id="ff952-121">Наконец, выберите рабочий набор, в который добавляется пример.</span><span class="sxs-lookup"><span data-stu-id="ff952-121">Finally, choose the working set to add the sample to.</span></span> <span data-ttu-id="ff952-122">В нем можно проверить состояние процесса так же, как при добавлении всего поиска в рабочий набор.</span><span class="sxs-lookup"><span data-stu-id="ff952-122">From there, you can check the status of the process just as you would for adding a whole search into a working set.</span></span> 