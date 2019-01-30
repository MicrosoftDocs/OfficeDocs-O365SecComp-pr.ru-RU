---
title: Обнаружение схожих документов (почти дубликатов)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: a3f5945ee4ba0a1bc78ab6c8ccc9af934d392232
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608236"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="33670-102">Обнаружение схожих документов (почти дубликатов)</span><span class="sxs-lookup"><span data-stu-id="33670-102">Near duplicate detection</span></span>

<span data-ttu-id="33670-p101">Рассмотрите возможность набор документов для изучить, в которых подмножества основано на тот же шаблон и имеет большей части же стандартного языка с, что некоторые отличия. Если проверяющий может определить приведенного ниже подмножества, тщательной просмотрите один из них и просмотрите различия для остальных, они будут не пропущенные любые уникальные данные во время с удалением только часть из времени, который будет перевода их для просмотра всех документов обложка для заставки. NEAR повторяющихся групп текстового документам вместе, чтобы сведения, которые помогут вашей процесс просмотра более эффективно.</span><span class="sxs-lookup"><span data-stu-id="33670-p101">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there. If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover. Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="33670-106">Как это работает?</span><span class="sxs-lookup"><span data-stu-id="33670-106">How does it work?</span></span>

<span data-ttu-id="33670-p102">При запуске рядом повторяющихся система выполняет синтаксический анализ каждого документа с текстом. Затем он сравнивает все документы с друг от друга, чтобы определить, является ли их подобия больше, чем установленное пороговое значение. Если он установлен, документы сгруппированы. После всех документов по сравнению и сгруппированные, документов из каждой группе отмечен как «pivot»; в анализ документов, можно просматривать сводки сначала и просмотреть другие документы в то же самое, рядом с дубликат набора повышения различие между pivot и документ, который находится на рассмотрении.</span><span class="sxs-lookup"><span data-stu-id="33670-p102">When near duplicate detection is run, the system parses every document with text. Then, it compares every document against each other to determine whether their similarity is greater than the set threshold. If it is, the documents are grouped together. Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>