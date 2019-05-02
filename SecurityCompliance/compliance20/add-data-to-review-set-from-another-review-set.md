---
title: Добавление данных из одного набора проверки в другой
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
ms.openlocfilehash: 025fd90373313f762ce1d1dab8d48286e32e3cbb
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527267"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a><span data-ttu-id="d5b5f-102">Добавление данных в набор проверки из другого набора проверки</span><span class="sxs-lookup"><span data-stu-id="d5b5f-102">Add data to a review set from another review set</span></span>

<span data-ttu-id="d5b5f-103">В некоторых случаях может потребоваться создавайте часть документов из одного набора проверки и работать с ними по отдельности в другом наборе рецензирования.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-103">In some cases, it may be necessary to carve out a portion of documents from one review set and work with them individually in another review set.</span></span>  <span data-ttu-id="d5b5f-104">Это особенно полезно, если вы использи контент из набора проверки и хотите запустить аналитику для подмножества данных.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-104">This is especially useful if you've culled content in a review set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="d5b5f-105">Используйте следующий рабочий процесс, чтобы добавить контент из одного набора проверки в другой.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-105">Use the following workflow to add content from one review set to another.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="d5b5f-106">Подготовка к работе</span><span class="sxs-lookup"><span data-stu-id="d5b5f-106">Before you begin</span></span>

<span data-ttu-id="d5b5f-107">Прежде чем начать, вам потребуется создать новый набор рецензирования, чтобы добавить данные в.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-107">Before you start, you'll need to create a new review set to add the data to.</span></span>  <span data-ttu-id="d5b5f-108">Новый набор проверки можно добавить на вкладке " **наборы проверки** ".</span><span class="sxs-lookup"><span data-stu-id="d5b5f-108">A new review set can be added on the **Review sets** tab of the case.</span></span> <span data-ttu-id="d5b5f-109">Дополнительные сведения можно найти в разделе [Manage reviewing Sets](managing-review-sets.md).</span><span class="sxs-lookup"><span data-stu-id="d5b5f-109">For more information, see [Manage review sets](managing-review-sets.md).</span></span>

## <a name="step-1-identify-content-to-add-to-another-review-set"></a><span data-ttu-id="d5b5f-110">Шаг 1: Определение контента для добавления в другой набор проверки</span><span class="sxs-lookup"><span data-stu-id="d5b5f-110">Step 1: Identify content to add to another review set</span></span>

<span data-ttu-id="d5b5f-111">Вы можете добавить контент в набор проверки, выбрав сообщения электронной почты и документы в сетке документа или все элементы в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-111">You can add content to a review set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="d5b5f-112">Если выбрано добавление выбранных элементов, выберите элементы, щелкните **действие**, а затем нажмите кнопку **Добавить в другой набор рецензирования**.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-112">If choosing to add selected items, select the items, click **Action**, and then click **Add to another review set**.</span></span>

![Добавить в другой набор проверки](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a><span data-ttu-id="d5b5f-114">Шаг 2: Указание параметров для добавления в другой набор рецензирования</span><span class="sxs-lookup"><span data-stu-id="d5b5f-114">Step 2: Specify options for adding to another review set</span></span>

<span data-ttu-id="d5b5f-115">На всплывающей странице **Добавление на другой набор проверки** выберите набор проверок, в который нужно добавить элементы.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-115">In the **Add to another review set** flyout page, choose the review set you want to add the items to.</span></span> <span data-ttu-id="d5b5f-116">Выберите, нужно ли добавить **все результаты поиска** или **Выбранные элементы**.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-116">Choose whether to add **All search results** or **Selected items**.</span></span>  <span data-ttu-id="d5b5f-117">Дополнительные сведения предоставляют параметры для включения всех метаданных из элементов и, наконец, следует ли включать Теги документа в новый набор рецензирования.</span><span class="sxs-lookup"><span data-stu-id="d5b5f-117">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new review set.</span></span>  <span data-ttu-id="d5b5f-118">После нажатия кнопки **ОК** будет создано новое задание для добавления контента в набор проверки; ход выполнения этого задания можно отслеживать на вкладке " **Задание** ". Более подробную информацию можно узнать в статье [Управление заданиями](managing-jobs-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="d5b5f-118">After clicking **Ok** a new job will be created to add the content to a review set; you can monitor the progress of that job on the **Job** tab. For more information, see [Manage jobs](managing-jobs-ediscovery20.md).</span></span>

![Добавить в другой набор проверки](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)
