---
title: Сведения о схожести документов в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Просмотрите, как документ значение подобия, минимальный уровень сходство для двух файлов следует учитывать рядом с дубликаты работает в Office 365 расширенного обнаружения электронных данных. '
ms.openlocfilehash: 39cd8c31204f0164f6b52c71fa707253cb22758a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534677"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a><span data-ttu-id="ed25c-103">Сведения о схожести документов в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ed25c-103">Understand document similarity in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="ed25c-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="ed25c-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="ed25c-106">В расширенной eDiscovery подобия документов — это минимальный уровень сходство, необходимые для двух документов рассматриваться как рядом с дубликатов.</span><span class="sxs-lookup"><span data-stu-id="ed25c-106">In Advanced eDiscovery, Document Similarity is the minimal level of resemblance required for two documents to be considered as near-duplicates.</span></span>
  
> [!TIP]
> <span data-ttu-id="ed25c-p102">Для большинства бизнес-приложений рекомендуется использовать значение подобия из 60% - 75%. Для очень плохого качества материалов оптического распознавания символов (OCR) можно применить меньше значения подобия.</span><span class="sxs-lookup"><span data-stu-id="ed25c-p102">For most business applications, it is recommended to use a Similarity value of 60%-75%. For very poor quality optical character recognition (OCR) material, lower Similarity values can be applied.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ed25c-109">После того как она включена и запустить для заданного варианта, нельзя изменить значение подобия.</span><span class="sxs-lookup"><span data-stu-id="ed25c-109">After it's set and run for a given case, the Similarity value cannot be changed.</span></span> 
  
<span data-ttu-id="ed25c-p103">В наборе Near повторяющиеся (ОЕ) может быть документы с уровнем сходство ниже порога подобия. Для документа для присоединения к набор и должен быть по крайней мере один документ в и задайте уровень сходство превышение сходства.</span><span class="sxs-lookup"><span data-stu-id="ed25c-p103">Within a Near-duplicate (ND) set, there may be documents with a level of resemblance below the Similarity threshold. For a document to join an ND set, there must be at least one document in the ND set with a level of resemblance exceeding the Similarity.</span></span> 
  
<span data-ttu-id="ed25c-112">Например предположим, сходства задано значение 80%, документ F1 имеет следующий вид: F2 документов на уровне 85% и документов F2 имеет следующий вид: документов F3 на уровне 90%.</span><span class="sxs-lookup"><span data-stu-id="ed25c-112">For example, assume the Similarity is set to 80%, document F1 resembles document F2 at a level of 85%, and document F2 resembles document F3 at a level of 90%.</span></span> 
  
<span data-ttu-id="ed25c-p104">Тем не менее документ F1 может иметь вид документов F3 на уровне только 70%, что находится ниже порогового значения. Тем не менее в этом примере документы F1, F2 и F3 все отображаются в одной и задать. Аналогично используя значение подобия 80%, мы может создавать два набора EquiSet-1 и EquiSet 2. EquiSet 1 содержит документы E1 и E2. Equiset-2 содержит документы F1, F2 и F3.</span><span class="sxs-lookup"><span data-stu-id="ed25c-p104">However, document F1 may resemble document F3 at a level of only 70%, which is below the threshold. Nonetheless, in this example, documents F1, F2, and F3 all appear in the one ND set. Similarly, using a Similarity value of 80%, we may have created two sets, EquiSet-1 and EquiSet-2. EquiSet-1 contains documents E1 and E2. Equiset-2 contains documents F1, F2, and F3.</span></span> 
  
<span data-ttu-id="ed25c-118">Уровни сходство проиллюстрированы следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ed25c-118">The levels of resemblance are illustrated as follows:</span></span>
  
![Схожесть документов](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
<span data-ttu-id="ed25c-p105">Предположим, что теперь вставляется в другой документ, X1. Сходство между X1 и E3 — 87%. Аналогично сходство между X1 и F1 — 92%. В результате EquiSet -1, EquiSet -2 и X1 теперь объединены в одну и установить.</span><span class="sxs-lookup"><span data-stu-id="ed25c-p105">Assume that another document, X1, is now inserted. The resemblance between X1 and E3 is 87%. Similarly, the resemblance between X1 and F1 is 92%. As a result, EquiSet -1, EquiSet -2, and X1 are now combined into one ND set.</span></span>
  
![Похожесть документов](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> <span data-ttu-id="ed25c-125">Если любой двух документов назначается один набор ОЕ, они останутся вместе в один и тот же набор ОЕ, даже если дополнительные документы добавляются в набор или если наборы объединяются.</span><span class="sxs-lookup"><span data-stu-id="ed25c-125">If any two documents are assigned to one ND set, they will remain together in the same ND set, even if additional documents are added to the set or if the sets are merged.</span></span> 
  
<span data-ttu-id="ed25c-126">После объединения наборов документов Pivot можно изменить при добавлении новых документов в набор.</span><span class="sxs-lookup"><span data-stu-id="ed25c-126">After sets are merged, the Pivot document can change when new documents are added to a set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed25c-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ed25c-127">See also</span></span>

[<span data-ttu-id="ed25c-128">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ed25c-128">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ed25c-129">Настройка параметров анализа</span><span class="sxs-lookup"><span data-stu-id="ed25c-129">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ed25c-130">Параметр Игнорировать текста</span><span class="sxs-lookup"><span data-stu-id="ed25c-130">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ed25c-131">Анализ параметр Дополнительные параметры</span><span class="sxs-lookup"><span data-stu-id="ed25c-131">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ed25c-132">Просмотр результатов анализа</span><span class="sxs-lookup"><span data-stu-id="ed25c-132">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

