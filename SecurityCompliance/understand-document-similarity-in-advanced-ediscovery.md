---
title: Сведения о сходстве документов в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Проверьте, как значение подобия документа — минимальный уровень сходства для двух файлов, которые должны рассматриваться как почти повторяющиеся, работает в Office 365 Advanced eDiscovery. '
ms.openlocfilehash: ce9c2e6ea1d40c82b7a124c9d4d64ce915d266b0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156381"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a><span data-ttu-id="8db50-103">Сведения о сходстве документов в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8db50-103">Understand document similarity in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="8db50-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="8db50-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="8db50-106">В Advanced eDiscovery сходство документов — это минимальный уровень сходства, необходимый для двух документов, которые должны рассматриваться как почти повторяющиеся.</span><span class="sxs-lookup"><span data-stu-id="8db50-106">In Advanced eDiscovery, Document Similarity is the minimal level of resemblance required for two documents to be considered as near-duplicates.</span></span>
  
> [!TIP]
> <span data-ttu-id="8db50-107">Для большинства бизнес-приложений рекомендуется использовать значение подобия 60%-75%.</span><span class="sxs-lookup"><span data-stu-id="8db50-107">For most business applications, it is recommended to use a Similarity value of 60%-75%.</span></span> <span data-ttu-id="8db50-108">Для очень низкого качества оптического распознавания символов (OCR) можно применить меньшее значение подобия.</span><span class="sxs-lookup"><span data-stu-id="8db50-108">For very poor quality optical character recognition (OCR) material, lower Similarity values can be applied.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8db50-109">После настройки и запуска в заданном случае значение сходства не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="8db50-109">After it's set and run for a given case, the Similarity value cannot be changed.</span></span> 
  
<span data-ttu-id="8db50-110">В наборе NEAR-дублировать (ND) могут находиться документы с уровнем сходства ниже порога подобия.</span><span class="sxs-lookup"><span data-stu-id="8db50-110">Within a Near-duplicate (ND) set, there may be documents with a level of resemblance below the Similarity threshold.</span></span> <span data-ttu-id="8db50-111">Чтобы документ присоединился к набору ND, в наборе ND должен быть по крайней мере один документ с уровнем сходства, превышающим подобную степень.</span><span class="sxs-lookup"><span data-stu-id="8db50-111">For a document to join an ND set, there must be at least one document in the ND set with a level of resemblance exceeding the Similarity.</span></span> 
  
<span data-ttu-id="8db50-112">Например, предположим, что для параметра подобие задано значение 80%, а в документе F1 похож документ F2 на уровне 85%, а документ F2 напоминает документ F3 на уровне 90%.</span><span class="sxs-lookup"><span data-stu-id="8db50-112">For example, assume the Similarity is set to 80%, document F1 resembles document F2 at a level of 85%, and document F2 resembles document F3 at a level of 90%.</span></span> 
  
<span data-ttu-id="8db50-113">Тем не менее, в документе F1 может напоминаться документ F3 на уровне 70%, который ниже порогового значения.</span><span class="sxs-lookup"><span data-stu-id="8db50-113">However, document F1 may resemble document F3 at a level of only 70%, which is below the threshold.</span></span> <span data-ttu-id="8db50-114">Тем не менее, в этом примере документы F1, F2 и F3 отображаются в наборе ND.</span><span class="sxs-lookup"><span data-stu-id="8db50-114">Nonetheless, in this example, documents F1, F2, and F3 all appear in the one ND set.</span></span> <span data-ttu-id="8db50-115">Аналогично, при использовании значения подобия 80% могли быть созданы два набора: Екуисет – 1 и Екуисет – 2.</span><span class="sxs-lookup"><span data-stu-id="8db50-115">Similarly, using a Similarity value of 80%, we may have created two sets, EquiSet-1 and EquiSet-2.</span></span> <span data-ttu-id="8db50-116">Екуисет – 1 содержит документы E1 и E2.</span><span class="sxs-lookup"><span data-stu-id="8db50-116">EquiSet-1 contains documents E1 and E2.</span></span> <span data-ttu-id="8db50-117">Екуисет – 2 содержит документы F1, F2 и F3.</span><span class="sxs-lookup"><span data-stu-id="8db50-117">Equiset-2 contains documents F1, F2, and F3.</span></span> 
  
<span data-ttu-id="8db50-118">Уровни сходства иллюстрируются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8db50-118">The levels of resemblance are illustrated as follows:</span></span>
  
![Схожесть документов](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
<span data-ttu-id="8db50-120">Предположим, что теперь вставлен другой документ, x1.</span><span class="sxs-lookup"><span data-stu-id="8db50-120">Assume that another document, X1, is now inserted.</span></span> <span data-ttu-id="8db50-121">Сходство между x1 и E3 составляет 87%.</span><span class="sxs-lookup"><span data-stu-id="8db50-121">The resemblance between X1 and E3 is 87%.</span></span> <span data-ttu-id="8db50-122">Аналогично, сходство между x1 и F1 составляет 92%.</span><span class="sxs-lookup"><span data-stu-id="8db50-122">Similarly, the resemblance between X1 and F1 is 92%.</span></span> <span data-ttu-id="8db50-123">В результате Екуисет – 1, Екуисет – 2 и x1 теперь объединены в один набор ND.</span><span class="sxs-lookup"><span data-stu-id="8db50-123">As a result, EquiSet -1, EquiSet -2, and X1 are now combined into one ND set.</span></span>
  
![Похожесть документов](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> <span data-ttu-id="8db50-125">Если для одного набора ND назначены два документа, они останутся в одном наборе ND, даже если в набор добавляются дополнительные документы, или же при объединении наборов.</span><span class="sxs-lookup"><span data-stu-id="8db50-125">If any two documents are assigned to one ND set, they will remain together in the same ND set, even if additional documents are added to the set or if the sets are merged.</span></span> 
  
<span data-ttu-id="8db50-126">После объединения наборов сводный документ может измениться при добавлении новых документов в набор.</span><span class="sxs-lookup"><span data-stu-id="8db50-126">After sets are merged, the Pivot document can change when new documents are added to a set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8db50-127">См. также</span><span class="sxs-lookup"><span data-stu-id="8db50-127">See also</span></span>

[<span data-ttu-id="8db50-128">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8db50-128">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="8db50-129">Настройка параметров анализа</span><span class="sxs-lookup"><span data-stu-id="8db50-129">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8db50-130">Настройка игнорируемого текста</span><span class="sxs-lookup"><span data-stu-id="8db50-130">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8db50-131">Настройка дополнительных параметров анализа</span><span class="sxs-lookup"><span data-stu-id="8db50-131">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8db50-132">Просмотр результатов анализа</span><span class="sxs-lookup"><span data-stu-id="8db50-132">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

