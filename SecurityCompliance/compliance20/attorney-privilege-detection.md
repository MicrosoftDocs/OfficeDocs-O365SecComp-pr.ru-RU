---
title: Настройка обнаружения доверенных прав клиентов в Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 6838203a500a4fe600d8186a4b848beed0730665
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/09/2019
ms.locfileid: "33835069"
---
# <a name="set-up-attorney-client-privilege-detection-preview-in-advanced-ediscovery"></a><span data-ttu-id="e25b2-102">Настройка юриста — обнаружение прав клиента (Предварительная версия) в Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="e25b2-102">Set up attorney-client privilege detection (preview) in Advanced eDiscovery</span></span>

<span data-ttu-id="e25b2-103">Основной и дорогостоящий аспект проверки любого процесса обнаружения — обзор защищенного контента.</span><span class="sxs-lookup"><span data-stu-id="e25b2-103">A major and costly aspect of the review portion of any discovery process is reviewing for privileged content.</span></span> <span data-ttu-id="e25b2-104">Расширенное обнаружение электронных данных обеспечивает обнаружение привилегированного контента на основе AI, что позволяет повысить эффективность этого процесса.</span><span class="sxs-lookup"><span data-stu-id="e25b2-104">Advanced eDiscovery provides an AI-based detection of privileged content in your case so that you can make this process more efficient.</span></span> <span data-ttu-id="e25b2-105">Так как эта функция в настоящее время находится в бета-версии, администратор eDiscovery должен принять участие в функции.</span><span class="sxs-lookup"><span data-stu-id="e25b2-105">As this feature is currently in beta, an eDiscovery Administrator has to opt into the feature to use it.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="e25b2-106">Как это работает?</span><span class="sxs-lookup"><span data-stu-id="e25b2-106">How does it work?</span></span>

<span data-ttu-id="e25b2-107">Если функция включена, при анализе набора проверки в случае всех документов выполняется через модель обнаружения доверенных прав клиентов.</span><span class="sxs-lookup"><span data-stu-id="e25b2-107">With the feature turned on, when you analyze a review set within a case, all documents run through the attorney-client privilege detection model.</span></span> <span data-ttu-id="e25b2-108">Модель рассматривает две вещи:</span><span class="sxs-lookup"><span data-stu-id="e25b2-108">The model looks at two things:</span></span>

- <span data-ttu-id="e25b2-109">Контент: Модель ML определяет вероятность того, что контент документа является юридическим в природе.</span><span class="sxs-lookup"><span data-stu-id="e25b2-109">Content: the ML model determines the likelihood of the document's content being legal in nature.</span></span>

- <span data-ttu-id="e25b2-110">Участники: Если в клиенте есть список доверенных пользователей, модель сравнивает участников документа со списком, чтобы определить, имеет ли документ по крайней мере один участник юриста.</span><span class="sxs-lookup"><span data-stu-id="e25b2-110">Participants: if there is a user-uploaded list of attorneys for the tenant, the model compares the participants of the document against the list to determine whether the document has at least one attorney participant.</span></span>
<span data-ttu-id="e25b2-111">Модель выводит три значения для каждого документа, для каждого из которых будет выполняться поиск в наборе проверки:</span><span class="sxs-lookup"><span data-stu-id="e25b2-111">The model outputs three values for every document, all of which will be searchable within a review set:</span></span>

- <span data-ttu-id="e25b2-112">Оценка контента: вероятность того, что документ является юридическим в природе (число от 0 до 1).</span><span class="sxs-lookup"><span data-stu-id="e25b2-112">Content score: the likelihood of the document being legal in nature (score between 0 and 1)</span></span>

- <span data-ttu-id="e25b2-113">Имеет юрист: true, если один из участников находится в переданном списке судебного юриста, или false в противном случае, или если список доверенных элементов отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e25b2-113">Has Attorney: True if one of the participants is found in the uploaded attorney list, false otherwise, or if there is no attorney list.</span></span>

-  <span data-ttu-id="e25b2-114">Потенциально привилегированные: true, если оценка контента выше порогового значения или участник юриста; в противном случае — false.</span><span class="sxs-lookup"><span data-stu-id="e25b2-114">Potentially Privileged: True if content score is above threshold or has an attorney participant, false otherwise.</span></span>

## <a name="opting-into-attorney-client-privilege-detection"></a><span data-ttu-id="e25b2-115">Разрешение конфликтов обнаружения доверенности клиентов</span><span class="sxs-lookup"><span data-stu-id="e25b2-115">Opting into Attorney-client privilege detection</span></span>

### <a name="step-1-opt-into-attorney-client-privilege-detection-ediscovery-admin"></a><span data-ttu-id="e25b2-116">Шаг 1: согласие с юристом — обнаружение прав клиента (администратор eDiscovery)</span><span class="sxs-lookup"><span data-stu-id="e25b2-116">Step 1: Opt into Attorney-client privilege detection (eDiscovery Admin)</span></span>

<span data-ttu-id="e25b2-117">Так как обнаружение доверенности клиента является функцией предварительного просмотра, администратор обнаружения электронных данных должен принять участие в функции, доступной в ваших случаях.</span><span class="sxs-lookup"><span data-stu-id="e25b2-117">Because Attorney-client privilege detection is a preview feature, your eDiscovery Administrator needs to opt in to make the feature available in your cases.</span></span>

- <span data-ttu-id="e25b2-118">Переход к разделу "Настройка экспериментальных функций с" расширенной страницы обнаружения электронных данных "</span><span class="sxs-lookup"><span data-stu-id="e25b2-118">Go to "Configure experimental features" from Advanced eDiscovery page</span></span>

- <span data-ttu-id="e25b2-119">Нажмите кнопку "Управление юристом — обнаружение прав клиента".</span><span class="sxs-lookup"><span data-stu-id="e25b2-119">Click on "Manage Attorney-Client Privilege detection".</span></span>

- <span data-ttu-id="e25b2-120">Щелкните переключатель, чтобы включить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e25b2-120">Click on the toggle to turn the feature on.</span></span>

### <a name="step-2-upload-a-list-of-attorneys-optional"></a><span data-ttu-id="e25b2-121">Шаг 2: Отправка списка юристов (необязательно)</span><span class="sxs-lookup"><span data-stu-id="e25b2-121">Step 2: Upload a list of attorneys (optional)</span></span>

<span data-ttu-id="e25b2-122">Чтобы воспользоваться всеми преимуществами обнаружения доверенности клиентов, мы рекомендуем предоставить список адресов электронной почты юристам или юридических лиц, работающих в компании.</span><span class="sxs-lookup"><span data-stu-id="e25b2-122">In order to take full advantage of attorney-client privilege detection we recommend providing a list of email addresses lawyers or legal personas who work for the company.</span></span> <span data-ttu-id="e25b2-123">Список должен быть в формате CSV без заголовков, по одному адресу электронной почты в строке.</span><span class="sxs-lookup"><span data-stu-id="e25b2-123">The list should be a header-less CSV, with one email address per line.</span></span>

## <a name="leveraging-attorney-client-privilege-detection"></a><span data-ttu-id="e25b2-124">Использование юриста — обнаружение прав клиента</span><span class="sxs-lookup"><span data-stu-id="e25b2-124">Leveraging attorney-client privilege detection</span></span> 

### <a name="step-1-analyze-a-review-set"></a><span data-ttu-id="e25b2-125">Шаг 1: анализ набора проверки</span><span class="sxs-lookup"><span data-stu-id="e25b2-125">Step 1: Analyze a review set</span></span>

<span data-ttu-id="e25b2-126">При анализе набора проверок также выполняется обнаружение доверенности клиента.</span><span class="sxs-lookup"><span data-stu-id="e25b2-126">When you analyze your review set, attorney-client privilege detection will be run as well.</span></span> <span data-ttu-id="e25b2-127">Чтобы узнать больше об анализе данных в наборе рецензирования, ознакомьтесь со статьей [анализ данных в наборе проверки в Advanced eDiscovery](analyzing-data-in-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="e25b2-127">To learn more about analyzing data in review set, please refer to [Analyze data in a review set in Advanced eDiscovery](analyzing-data-in-review-set.md).</span></span>

### <a name="step-2-create-a-smart-tag-group-with-attorney-client-privilege-detection-model"></a><span data-ttu-id="e25b2-128">Шаг 2: создание группы смарт-тегов с использованием доверенности — модели обнаружения прав клиентов</span><span class="sxs-lookup"><span data-stu-id="e25b2-128">Step 2: Create a smart tag group with attorney-client privilege detection model</span></span>

<span data-ttu-id="e25b2-129">С помощью группы смарт-тегов один из основных способов использования результатов обнаружения доверенности клиента в процессе проверки заключается в использовании группы смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="e25b2-129">One of the main ways you can consume the results of attorney-client privilege detection in your review process is by using a smart tag group.</span></span> <span data-ttu-id="e25b2-130">Группы смарт-тегов получают результаты модели ML и отображают результаты модели в строке рядом с тегами, чтобы можно было легко использовать результаты модели, в том числе и теги в процессе проверки, так же, как и любые другие теги на панели маркировки.</span><span class="sxs-lookup"><span data-stu-id="e25b2-130">Smart tag groups take the results of an ML model and show the results of the model in-line next to the tags, so that you can easily consume the results of the model where relevant, and use the tags in your review process as you would any other tags in your tagging panel.</span></span>

- <span data-ttu-id="e25b2-131">В разделе "Управление тегами" щелкните ссылку "добавить раздел смарт-тега".</span><span class="sxs-lookup"><span data-stu-id="e25b2-131">In "Manage tags", click on "Add smart tag section".</span></span>

- <span data-ttu-id="e25b2-132">Выберите "юрист — определение прав клиента".</span><span class="sxs-lookup"><span data-stu-id="e25b2-132">Select "Attorney-client privilege detection".</span></span> <span data-ttu-id="e25b2-133">Вы увидите, что Группа тегов и два тега, соответствующие возможным результатам модели, были созданы.</span><span class="sxs-lookup"><span data-stu-id="e25b2-133">You will see that a tag group and two tags, corresponding to the possible results of the model, have been created.</span></span>

- <span data-ttu-id="e25b2-134">Переименуйте группу тегов и теги так, как они отображаются для проверки.</span><span class="sxs-lookup"><span data-stu-id="e25b2-134">Rename the tag group and tags as you see fit for your review.</span></span>

### <a name="step-3-use-the-smart-tag-group-for-privilege-review"></a><span data-ttu-id="e25b2-135">Шаг 3: использование группы смарт-тегов для проверки прав</span><span class="sxs-lookup"><span data-stu-id="e25b2-135">Step 3: Use the smart tag group for privilege review</span></span>

<span data-ttu-id="e25b2-136">Когда вы просматриваете документ, если модель определила, что документ является потенциально привилегированным, соответствующий смарт-тег будет предоставлять результат:</span><span class="sxs-lookup"><span data-stu-id="e25b2-136">When you review a document, if the model has determined that the document is potentially privileged, the corresponding smart tag will expose the result:</span></span>

- <span data-ttu-id="e25b2-137">Если в документе есть контент, который может быть юридическим, рядом с соответствующим смарт-тегом появится подпись "юридический контент".</span><span class="sxs-lookup"><span data-stu-id="e25b2-137">If the document has content that may be legal in nature, a "Legal content" label will appear next to the corresponding smart tag.</span></span>

- <span data-ttu-id="e25b2-138">Если в документе есть участник, найденный в переданном списке юристов, рядом с соответствующим смарт-тегом появится метка "юрист".</span><span class="sxs-lookup"><span data-stu-id="e25b2-138">If the document has a participant that is found in the uploaded attorney list, an "Attorney" label will appear next to the corresponding smart tag.</span></span>