---
title: Настройка смарт-тегов для обнаружения доверенных прав клиентов в Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 5310acad1aa1bc2e01cbabee69dd7bb38084bd9a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153971"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a><span data-ttu-id="fb773-102">Настройка смарт-тегов для экспертной проверки в Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="fb773-102">Set up smart tags for ML-assisted review in Advanced eDiscovery</span></span>

<span data-ttu-id="fb773-103">Функции машинного обучения в Advanced eDiscovery предназначены для повышения эффективности процесса принятия решений на документах.</span><span class="sxs-lookup"><span data-stu-id="fb773-103">Machine learning capabilities in Advanced eDiscovery are meant to help make decision process on documents more efficient.</span></span> <span data-ttu-id="fb773-104">Смарт-теги позволяют разбивать возможности машинного обучения на место записи решений: Теги и группы тегов.</span><span class="sxs-lookup"><span data-stu-id="fb773-104">Smart tags is a way to bring the machine learning capabilities into where the decisions are recorded: tags and tag groups.</span></span> <span data-ttu-id="fb773-105">При создании группы смарт-тегов решение модели ML, сопоставленной с группой, будет отображаться в виде тегов в группе, чтобы можно было видеть информацию в виде встроенной строки, в которой они имеют смысл.</span><span class="sxs-lookup"><span data-stu-id="fb773-105">When you create a smart tag group, then the decisions of the ML model mapped to the group will be shown in-line with the tags in the group to help you see the information in-line, where they contextually make most sense.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="fb773-106">Настройка группы смарт-тегов</span><span class="sxs-lookup"><span data-stu-id="fb773-106">How to set up a smart tag group</span></span>

1. <span data-ttu-id="fb773-107">В наборе рецензирования перейдите к разделу **Управление набором** -> проверок**Управление тегами**.</span><span class="sxs-lookup"><span data-stu-id="fb773-107">In a review set, go to **Manage review set** -> **Manage tags**.</span></span>

2. <span data-ttu-id="fb773-108">Щелкните раскрывающийся список **Добавить группу тегов** и выберите команду **Добавить группу смарт-тегов**.</span><span class="sxs-lookup"><span data-stu-id="fb773-108">Click on the drop-down next to **Add tag group** and select **Add smart tag group**.</span></span>

3. <span data-ttu-id="fb773-109">Выберите модель, которую нужно сопоставить с этой группой.</span><span class="sxs-lookup"><span data-stu-id="fb773-109">Select the model you want to map to this group.</span></span> <span data-ttu-id="fb773-110">При этом будет создан раздел тегов и дочерние теги N, где N — это количество возможных выходных данных модели.</span><span class="sxs-lookup"><span data-stu-id="fb773-110">This will create a tag section and N child tags, where N is the number of possible outputs of the model.</span></span> <span data-ttu-id="fb773-111">Например, для модели обнаружения прав клиентов с юристом существует два возможных выходных данных, привилегированных и непривилегированных. При выборе этой модели в наборе проверки создаются два дочерних тега, каждый из которых соответствует одному из возможных выходов.</span><span class="sxs-lookup"><span data-stu-id="fb773-111">For instance, attorney-client privilege detection model has two possible outputs - privileged and not privileged; selecting this model will create two child tags in the review set, each corresponding to one of the possible outputs.</span></span>

4. <span data-ttu-id="fb773-112">Переименуйте группу тегов и теги так, как они отображаются.</span><span class="sxs-lookup"><span data-stu-id="fb773-112">Rename the tag group and tags as you see fit.</span></span>

## <a name="how-to-use-a-smart-tag-group"></a><span data-ttu-id="fb773-113">Использование группы смарт-тегов</span><span class="sxs-lookup"><span data-stu-id="fb773-113">How to use a smart tag group</span></span>

<span data-ttu-id="fb773-114">При просмотре документа результаты модели отображаются рядом с соответствующим значением тега.</span><span class="sxs-lookup"><span data-stu-id="fb773-114">When reviewing a document, the model's results will be exposed next to the appropriate tag value.</span></span> <span data-ttu-id="fb773-115">Например, если у вас есть группа смарт-тегов для обнаружения доверенных прав клиентов и вы просматриваете документ, который решил, что эта модель является потенциально привилегированной, вы увидите ее причину рядом с соответствующим тегом.</span><span class="sxs-lookup"><span data-stu-id="fb773-115">For instance, if you have a smart tag group for attorney-client privilege detection and you review a document that the model has decided is potentially privileged, you will see the reason for that next to the appropriate tag.</span></span> <span data-ttu-id="fb773-116">Важно отметить, что тег не применяется автоматически; для всех целей и целей теги в группе смарт-тегов действуют точно так же, как и обычные теги, за исключением того, что они представляют результаты модели рядом с ними при необходимости.</span><span class="sxs-lookup"><span data-stu-id="fb773-116">It is important to note that the tag is not automatically applied; for all intents and purposes, tags within a smart tag group act just like normal tags, except that they expose the model results next to them when appropriate.</span></span>