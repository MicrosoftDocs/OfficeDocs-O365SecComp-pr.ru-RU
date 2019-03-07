---
title: Добавление тегов к документам в рабочем наборе
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
ms.openlocfilehash: 1183264f64a74e50f750ee13618f7532ffe04eb7
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455161"
---
# <a name="tag-documents-in-a-working-set"></a><span data-ttu-id="82e5f-102">Добавление тегов к документам в рабочем наборе</span><span class="sxs-lookup"><span data-stu-id="82e5f-102">Tag documents in a working set</span></span>

<span data-ttu-id="82e5f-103">Организация контента в рабочем наборе важна для выполнения различных рабочих процессов в процессе обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="82e5f-103">Organizing content in a working set is important to complete various workflows in the eDiscovery process.</span></span> <span data-ttu-id="82e5f-104">Это достигается за счет следующего:</span><span class="sxs-lookup"><span data-stu-id="82e5f-104">This includes:</span></span>

-  <span data-ttu-id="82e5f-105">Отбор ненужного контента.</span><span class="sxs-lookup"><span data-stu-id="82e5f-105">Culling unnecessary content.</span></span>

- <span data-ttu-id="82e5f-106">Определение релевантного контента.</span><span class="sxs-lookup"><span data-stu-id="82e5f-106">Identifying relevant content.</span></span>
 
-  <span data-ttu-id="82e5f-107">Определение контента, который должен быть проверен экспертом или юристом.</span><span class="sxs-lookup"><span data-stu-id="82e5f-107">Identifying content that must be reviewed by an expert or an attorney.</span></span>

<span data-ttu-id="82e5f-108">Когда эксперты, юристы или другие пользователи просматривают контент в рабочем наборе, их мнения, связанные с содержимым, можно записать с помощью тегов.</span><span class="sxs-lookup"><span data-stu-id="82e5f-108">When experts, attorneys, or other users review content in a working set, their opinions related to the content can be captured by using tags.</span></span> <span data-ttu-id="82e5f-109">Например, если предполагалось исключать ненужное содержимое, пользователь может отмечать документы тегами, например "не отвечает".</span><span class="sxs-lookup"><span data-stu-id="82e5f-109">For example, if the intent is to cull unnecessary content, a user can tag documents with a tag such as “non-responsive”.</span></span> <span data-ttu-id="82e5f-110">После рассмотрения и пометки контента можно создать поисковый набор, который будет использоваться для исключения любого содержимого, помеченного как "не отвечает", что исключает из следующих этапов рабочего процесса обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="82e5f-110">After content has been reviewed and tagged, a working set search can be created to exclude any content tagged as “non-responsive”, which eliminates this content from the next steps in the eDiscovery workflow.</span></span> <span data-ttu-id="82e5f-111">Область тегов можно изменить для каждого случая, чтобы теги могли поддерживать рабочий процесс, предназначенный для рецензирования.</span><span class="sxs-lookup"><span data-stu-id="82e5f-111">The tag panel can be customized for every case so that the tags can support the intended review workflow.</span></span>

## <a name="tag-types"></a><span data-ttu-id="82e5f-112">Типы тегов</span><span class="sxs-lookup"><span data-stu-id="82e5f-112">Tag types</span></span>

<span data-ttu-id="82e5f-113">Расширенное обнаружение электронных данных (Предварительная версия) предоставляет два типа тегов:</span><span class="sxs-lookup"><span data-stu-id="82e5f-113">Advanced eDiscovery (Preview) provides two types of tags:</span></span>

- <span data-ttu-id="82e5f-114">**Один тег выбора** — запрещает пользователям выбирать один тег в группе.</span><span class="sxs-lookup"><span data-stu-id="82e5f-114">**Single choice tags** - Restricts users to select a single tag within a group.</span></span> <span data-ttu-id="82e5f-115">Это может быть удобно, чтобы пользователи не могли выбирать конфликтующие теги, такие как "реагирующий" и "не отвечает".</span><span class="sxs-lookup"><span data-stu-id="82e5f-115">This can be useful to ensure users don’t select conflicting tags such as “responsive” and “non-responsive”.</span></span> 

- <span data-ttu-id="82e5f-116">**Несколько тегов выбора** — позволяет пользователям выбирать несколько тегов в группе.</span><span class="sxs-lookup"><span data-stu-id="82e5f-116">**Multiple choice tags** - Allow users to select multiple tags within a group.</span></span>

## <a name="tag-structure"></a><span data-ttu-id="82e5f-117">Структура тегов</span><span class="sxs-lookup"><span data-stu-id="82e5f-117">Tag structure</span></span>

<span data-ttu-id="82e5f-118">В дополнение к типам тегов, структура того, как теги являются организациями в панели тегов, может использоваться для упрощения интуитивной маркировки документов.</span><span class="sxs-lookup"><span data-stu-id="82e5f-118">In addition to the tag types, the structure of how tags are organization in the tag panel can be used to make tagging documents more intuitive.</span></span> <span data-ttu-id="82e5f-119">Теги группируются по разделам.</span><span class="sxs-lookup"><span data-stu-id="82e5f-119">Tags are grouped by sections.</span></span> <span data-ttu-id="82e5f-120">Working Set Search поддерживает поиск по разделу "возможность поиска по тегам" и "по тегу".</span><span class="sxs-lookup"><span data-stu-id="82e5f-120">Working set search supports the ability to search by tag and by tag section.</span></span> <span data-ttu-id="82e5f-121">Это означает, что вы можете создать Поиск рабочего набора, чтобы получить документы с тегами в разделе.</span><span class="sxs-lookup"><span data-stu-id="82e5f-121">This means you can create a working set search to retrieve documents tagged with any tag in a section.</span></span>

![Разделы с тегами в панели тегов](../media/Tagtypes.png)

<span data-ttu-id="82e5f-123">Теги можно упорядочить, дополнив их вложение в раздел.</span><span class="sxs-lookup"><span data-stu-id="82e5f-123">Tags can be further organized by nesting them within a section.</span></span> <span data-ttu-id="82e5f-124">Например, если предполагается определить и пометить привилегированный контент, можно использовать вложение, чтобы сделать так, чтобы пользователь мог пометить документ как "Привилегированный" и выбрать тип привилегий, проверив соответствующий вложенный тег.</span><span class="sxs-lookup"><span data-stu-id="82e5f-124">For example, if the intent is to identify and tag privileged content, nesting can be used to make it clear that a user can tag a document as “Privileged” and select the type of privilege by checking the appropriate nested tag.</span></span>

![Вложенные теги в разделе тегов](../media/Nestingtags.png)

## <a name="applying-tags"></a><span data-ttu-id="82e5f-126">Применение тегов</span><span class="sxs-lookup"><span data-stu-id="82e5f-126">Applying tags</span></span>

<span data-ttu-id="82e5f-127">Существует несколько способов применения тега к контенту.</span><span class="sxs-lookup"><span data-stu-id="82e5f-127">There are several ways to apply a tag to content.</span></span>

### <a name="tagging-a-single-document"></a><span data-ttu-id="82e5f-128">Добавление тегов для одного документа</span><span class="sxs-lookup"><span data-stu-id="82e5f-128">Tagging a single document</span></span>

<span data-ttu-id="82e5f-129">При просмотре документа в рабочем наборе можно отобразить теги, которые может использовать проверка, щелкнув **Панель кода**.</span><span class="sxs-lookup"><span data-stu-id="82e5f-129">When viewing a document in a working set, you can display the tags that a review can use by clicking **Coding panel**.</span></span>

![Щелкните панель тегов, чтобы отобразить панель тегов](../media/Singledoctag.png)

<span data-ttu-id="82e5f-131">Это позволит применить теги к документу, отображаемому в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="82e5f-131">This will enable you to apply tags to the document displayed in the viewer.</span></span>

### <a name="bulk-tagging"></a><span data-ttu-id="82e5f-132">Массовая маркировка</span><span class="sxs-lookup"><span data-stu-id="82e5f-132">Bulk tagging</span></span>

<span data-ttu-id="82e5f-133">Массовое расстановку тегов можно выполнить, выбрав несколько файлов в таблице результатов, а затем используя теги в **панели кода** , например, размечая отдельные документы.</span><span class="sxs-lookup"><span data-stu-id="82e5f-133">Bulk tagging can be done by selecting multiple files in the results grid and then using the tags in the **Coding panel** similar to tagging single documents.</span></span> <span data-ttu-id="82e5f-134">Массовое снятие тегов можно выполнить, выбирая Теги дважды; При первом щелчке будет применен тег, а во втором выделенном фрагменте этот тег будет очищен для всех выбранных файлов.</span><span class="sxs-lookup"><span data-stu-id="82e5f-134">Bulk un-tagging can be done by selecting tags twice; the first click will apply the tag, and the second selection will ensure that tag is cleared for all selected files.</span></span>

![Снимок экрана с автоматическим созданием описания сотового телефона](../media/Bulktag.png)

> [!NOTE]
> <span data-ttu-id="82e5f-136">При массовом разметке на панели маркировки отображается количество файлов, помеченных для каждого тега в панели.</span><span class="sxs-lookup"><span data-stu-id="82e5f-136">When bulk tagging, the tagging panel will display a count of files that are tagged for each tag in the panel.</span></span>

### <a name="tagging-in-other-review-panels"></a><span data-ttu-id="82e5f-137">Добавление тегов в другие панели рецензирования</span><span class="sxs-lookup"><span data-stu-id="82e5f-137">Tagging in other review panels</span></span>

<span data-ttu-id="82e5f-138">При просмотре документов можно использовать другие панели рецензирования для просмотра других характеристик документов в таблице результатов.</span><span class="sxs-lookup"><span data-stu-id="82e5f-138">When reviewing documents, you can use the other review panels to review other characteristics of documents in the results grid.</span></span> <span data-ttu-id="82e5f-139">Это включает проверку других связанных документов, почтовых потоков, ближайших дубликатов и хэш-дубликатов.</span><span class="sxs-lookup"><span data-stu-id="82e5f-139">This includes reviewing other related documents, email threads, near duplicates, and hash duplicates.</span></span> <span data-ttu-id="82e5f-140">Например, если вы просматриваете документы (с помощью палитры "Обзор **семейства документов** "), вы можете значительно снизить время на проверку путем массового разметки связанных документов.</span><span class="sxs-lookup"><span data-stu-id="82e5f-140">For example, when your reviewing related documents (by using the **Document family** review panel), you can significantly reduce review time by bulk tagging related documents.</span></span> <span data-ttu-id="82e5f-141">Например, если сообщение электронной почты имеет несколько вложений и вы хотите обеспечить единообразное пометку всех семейств.</span><span class="sxs-lookup"><span data-stu-id="82e5f-141">For example, if an email message has several attachments and you want to ensure that the entire family is tagged consistently.</span></span>

<span data-ttu-id="82e5f-142">Например, вот как можно отобразить **Панель кода** при использовании панели "Обзор **семейства документов** ":</span><span class="sxs-lookup"><span data-stu-id="82e5f-142">For example, here's how to display the **Coding panel** when using the **Document family** review panel:</span></span>

1. <span data-ttu-id="82e5f-143">Откройте панель "Рецензирование" для выбранного документа (например, отобразите список связанных материалов на панели "Рецензирование **семейства документов** "), щелкнув **документы кода** в верхней части текущей панели рецензирования.</span><span class="sxs-lookup"><span data-stu-id="82e5f-143">With the review panel open for a selected document (for example, displaying the list of related content in the **Document family** review panel, click **Code documents** at the top of the current review panel.</span></span>

   <span data-ttu-id="82e5f-144">Отображается панель "кодирование" — всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="82e5f-144">The Coding panel is displayed is a pop-up window.</span></span>

2. <span data-ttu-id="82e5f-145">Выберите один или несколько тегов, которые необходимо применить к выбранному документу.</span><span class="sxs-lookup"><span data-stu-id="82e5f-145">Choose one or more tags to apply the selected document.</span></span> 

3. <span data-ttu-id="82e5f-146">Чтобы отметить все документы, выберите все документы в области **семейство документов** , щелкните **документы кода**, а затем выберите Теги для применения ко всему семейству документов.</span><span class="sxs-lookup"><span data-stu-id="82e5f-146">To tag all documents, select all documents in the **Document family** panel, click **Code documents**, and then choose the tags to apply to the entire family of documents.</span></span>

![Снимок экрана с автоматически созданным описанием записи социальных медиа](../media/Relatedtag.png)
