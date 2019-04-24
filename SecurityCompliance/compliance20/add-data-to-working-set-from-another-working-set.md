---
title: Добавление данных из одного рабочего набора в другой рабочий набор
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
ms.openlocfilehash: e9e34d112cb84c27fec35e752eb2bfcbfe3136a3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243445"
---
# <a name="add-data-to-a-working-set-from-another-working-set"></a><span data-ttu-id="d305b-102">Добавление данных в рабочий набор из другого рабочего набора</span><span class="sxs-lookup"><span data-stu-id="d305b-102">Add data to a working set from another working set</span></span>
<span data-ttu-id="d305b-103">В некоторых случаях может потребоваться создавайте часть документов из одного рабочего набора и работать с ними по отдельности в другом рабочем наборе.</span><span class="sxs-lookup"><span data-stu-id="d305b-103">In some cases, it may be necessary to carve out a portion of documents from one working set and work with them individually in another working set.</span></span>  <span data-ttu-id="d305b-104">Это особенно полезно, если вы использи контент из рабочего множества и хотите запустить аналитику для подмножества данных.</span><span class="sxs-lookup"><span data-stu-id="d305b-104">This is especially useful if you've culled content in a working set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="d305b-105">Используйте следующий рабочий процесс для добавления контента из одного рабочего набора в другой.</span><span class="sxs-lookup"><span data-stu-id="d305b-105">Use the following workflow to add content from one working set to another.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="d305b-106">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="d305b-106">Before you start</span></span>
<span data-ttu-id="d305b-107">Прежде чем начать, вам потребуется создать новый рабочий набор.</span><span class="sxs-lookup"><span data-stu-id="d305b-107">Before you start, you'll need to create a new working set.</span></span>  <span data-ttu-id="d305b-108">Новый рабочий набор можно добавить на вкладке *рабочие* группы, чтобы [узнать больше](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-working-sets).</span><span class="sxs-lookup"><span data-stu-id="d305b-108">A new working set can be added through the *Working sets* tab [Learn more](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-working-sets).</span></span>

## <a name="step-1-identify-content-to-add-to-another-working-set"></a><span data-ttu-id="d305b-109">Шаг 1: Определение контента для добавления в другой рабочий набор</span><span class="sxs-lookup"><span data-stu-id="d305b-109">Step 1: Identify content to add to another working set</span></span>
<span data-ttu-id="d305b-110">Вы можете добавить содержимое в рабочий набор, выбрав сообщения электронной почты и документы в сетке документа или все элементы в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="d305b-110">You can add content to a working set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="d305b-111">Если вы добавите выбранные элементы, выберите их и щелкните раскрывающийся список *действий* , а затем *добавьте к другому рабочему набору*.</span><span class="sxs-lookup"><span data-stu-id="d305b-111">If choosing to add selected items, select the items and click the *Action* drop down then *Add to another working set*.</span></span>

![Добавить в другой рабочий набор](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-workings-set"></a><span data-ttu-id="d305b-113">Шаг 2: Указание параметров для добавления в другие наборы для рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="d305b-113">Step 2: Specify options for adding to another workings set</span></span>
<span data-ttu-id="d305b-114">В меню *Добавить в другой рабочий набор параметры* выберите рабочий набор, в который вы хотите добавить элементы.</span><span class="sxs-lookup"><span data-stu-id="d305b-114">In the *Add to another working set options* flyout, first choose the working set you want to add the items to.</span></span>  <span data-ttu-id="d305b-115">Выберите, нужно ли добавить все результаты поиска или выбранные элементы.</span><span class="sxs-lookup"><span data-stu-id="d305b-115">Choose whether to add All search results or Selected items.</span></span>  <span data-ttu-id="d305b-116">Дополнительные сведения предоставляют параметры для включения всех метаданных из элементов и, наконец, следует ли включать Теги документа в новый рабочий набор.</span><span class="sxs-lookup"><span data-stu-id="d305b-116">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new working set.</span></span>  <span data-ttu-id="d305b-117">После нажатия кнопки *ОК* будет создано новое задание для добавления контента в рабочий набор, вы можете отслеживать ход выполнения этого задания на вкладке [задания](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-jobs-ediscovery20) . ![добавить к другому рабочему набору](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)</span><span class="sxs-lookup"><span data-stu-id="d305b-117">After clicking *OK* a new job will be created to add the content to a working set, you can monitor the progress of that job in the [Jobs](https://docs.microsoft.com/en-us/office365/securitycompliance/compliance20/managing-jobs-ediscovery20) tab. ![Add to another working set](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)</span></span>
