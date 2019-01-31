---
title: Поиск и тегов
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: Модуль поиска и тегов в расширенной eDiscovery позволяет поиск, предварительный просмотр и организации документов в случае. На данный момент в бета-версии — в этом модуле.
ms.openlocfilehash: 013e559ca55e9a877dfb2f8747c4696f81e1e095
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666149"
---
# <a name="search-and-tagging"></a><span data-ttu-id="24d78-104">Поиск и тегов</span><span class="sxs-lookup"><span data-stu-id="24d78-104">Search and Tagging</span></span>

<span data-ttu-id="24d78-p102">Модуль поиска и тегов в расширенной eDiscovery позволяет поиск, предварительный просмотр и организации документов в случае. На данный момент в бета-версии — в этом модуле. Краткое Демонстрация поиска и тегов в разделе [Управление данных с помощью расширенных eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) видео.</span><span class="sxs-lookup"><span data-stu-id="24d78-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta. For a brief demonstration of searching and tagging, see the [Manage your data with Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) video.</span></span>

> [!NOTE]
> <span data-ttu-id="24d78-p103">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="24d78-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="24d78-110">Поиск документов в случае</span><span class="sxs-lookup"><span data-stu-id="24d78-110">Search the documents in your case</span></span>

<span data-ttu-id="24d78-p104">После обработки документов в случае расширенные обнаружения электронных данных (и при необходимости выполните анализ или релевантности модуль), можно использовать для поиска документов и разместите их применение тегов конкретного case (также называемая меток) поиска и тегов. Можно определить поисковый запрос с использованием карт отмеченными условие или с помощью языка KQL как запрос в ключевые слова условие карточки. Общий синтаксис KQL, например и, или нет, и NEAR(n), поддерживаемые, а также конечные составные подстановочные знаки (\*).</span><span class="sxs-lookup"><span data-stu-id="24d78-p104">After you have processed documents in an Advanced eDiscovery case (and optionally run the Analyze or Relevance module), you can use the Search and Tagging to search documents and then organize them by applying case-specific tags (also called labels). You can define a search query using the provided condition cards or by using a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*).</span></span> 

<span data-ttu-id="24d78-p105">В следующей таблице приведены свойства, которые можно выполнить поиск с помощью запроса ключевого слова KQL. Кроме того можно использовать карточку условие для возможности дополнительные средства поиска обнаружения электронных данных добавить условие (для выбранных свойств) поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="24d78-p105">The following table lists the properties that you can search for using a KQL keyword query. Alternatively, you can use a condition card for in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query.</span></span>

|<span data-ttu-id="24d78-116">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="24d78-116">**Property**</span></span>|<span data-ttu-id="24d78-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="24d78-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24d78-118">**caselabel**</span><span class="sxs-lookup"><span data-stu-id="24d78-118">**caselabel**</span></span> <br/> | <span data-ttu-id="24d78-119">Имя тега создан/применяется, если документ имеет теги.</span><span class="sxs-lookup"><span data-stu-id="24d78-119">The name of the tag created/applied when a document is tagged.</span></span> <br/> |
|<span data-ttu-id="24d78-120">**custodian**</span><span class="sxs-lookup"><span data-stu-id="24d78-120">**custodian**</span></span> <br/> | <span data-ttu-id="24d78-121">Custodian, связанной с документом; может быть ограничений.</span><span class="sxs-lookup"><span data-stu-id="24d78-121">The custodian associated with a document; subject to limitations.</span></span> <br/> |
|<span data-ttu-id="24d78-122">**Дата**</span><span class="sxs-lookup"><span data-stu-id="24d78-122">**date**</span></span> <br/> | <span data-ttu-id="24d78-123">Отправлено даты для электронной почты; Дата изменения документов с сайта.</span><span class="sxs-lookup"><span data-stu-id="24d78-123">Sent date for email; the modified date for site documents.</span></span> <br/> |
|<span data-ttu-id="24d78-124">**Идентификатор файла**</span><span class="sxs-lookup"><span data-stu-id="24d78-124">**fileid**</span></span> <br/> | <span data-ttu-id="24d78-125">Идентификатор файла в случае.</span><span class="sxs-lookup"><span data-stu-id="24d78-125">The File ID within the case.</span></span> <br/> |
|<span data-ttu-id="24d78-126">**Тип файла**</span><span class="sxs-lookup"><span data-stu-id="24d78-126">**filetype**</span></span> <br/> | <span data-ttu-id="24d78-127">Расширение собственный файл.</span><span class="sxs-lookup"><span data-stu-id="24d78-127">The native file extension.</span></span> <br/> |
|<span data-ttu-id="24d78-128">**fileclass**</span><span class="sxs-lookup"><span data-stu-id="24d78-128">**fileclass**</span></span> <br/> | <span data-ttu-id="24d78-129">Электронной почты, документа или вложения.</span><span class="sxs-lookup"><span data-stu-id="24d78-129">Email, document, or attachment.</span></span> <br/> |
|<span data-ttu-id="24d78-130">**senderauthor**</span><span class="sxs-lookup"><span data-stu-id="24d78-130">**senderauthor**</span></span> <br/> | <span data-ttu-id="24d78-131">Отправитель для электронной почты; Автор документов с сайта.</span><span class="sxs-lookup"><span data-stu-id="24d78-131">The sender for email; the author for site documents.</span></span> <br/> |
|<span data-ttu-id="24d78-132">**размер**</span><span class="sxs-lookup"><span data-stu-id="24d78-132">**size**</span></span> <br/> | <span data-ttu-id="24d78-133">Размер файла в КБ.</span><span class="sxs-lookup"><span data-stu-id="24d78-133">The size of the file in KB.</span></span> <br/> |
|<span data-ttu-id="24d78-134">**subjecttitle**</span><span class="sxs-lookup"><span data-stu-id="24d78-134">**subjecttitle**</span></span> <br/> | <span data-ttu-id="24d78-135">Тема для электронной почты; заголовок узла документов.</span><span class="sxs-lookup"><span data-stu-id="24d78-135">The subject for email; the title for site documents.</span></span> <br/> |
|<span data-ttu-id="24d78-136">**СК.**</span><span class="sxs-lookup"><span data-stu-id="24d78-136">**bcc**</span></span> <br/> | <span data-ttu-id="24d78-137">Поля Скрытая копия сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="24d78-137">The Bcc field of an email.</span></span> <br/> |
|<span data-ttu-id="24d78-138">**копия;**</span><span class="sxs-lookup"><span data-stu-id="24d78-138">**cc**</span></span> <br/> | <span data-ttu-id="24d78-139">В поле копия сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="24d78-139">The Cc field of an email.</span></span> <br/> |
|<span data-ttu-id="24d78-140">**Участники**</span><span class="sxs-lookup"><span data-stu-id="24d78-140">**participants**</span></span> <br/> | <span data-ttu-id="24d78-141">Адрес электронной почты в потоке электронной почты, включая отсутствующих связей всех участников конференции.</span><span class="sxs-lookup"><span data-stu-id="24d78-141">The email address of all participants in an email thread, including for missing links.</span></span> <br/> |
|<span data-ttu-id="24d78-142">**Получено**</span><span class="sxs-lookup"><span data-stu-id="24d78-142">**received**</span></span> <br/> | <span data-ttu-id="24d78-143">Дата получения сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="24d78-143">The date an email was received.</span></span> <br/> |
|<span data-ttu-id="24d78-144">**Получатели**</span><span class="sxs-lookup"><span data-stu-id="24d78-144">**recipients**</span></span> <br/> | <span data-ttu-id="24d78-145">Получателей копии сообщения электронной почты, включенных на Кому, копия или Скрытая копия поля.</span><span class="sxs-lookup"><span data-stu-id="24d78-145">Recipients of an email, included on the To, Cc, or Bcc fields.</span></span> <br/> |
|<span data-ttu-id="24d78-146">**отправитель;**</span><span class="sxs-lookup"><span data-stu-id="24d78-146">**sender**</span></span> <br/> | <span data-ttu-id="24d78-147">Отправитель сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="24d78-147">The sender of an email.</span></span> <br/> |
|<span data-ttu-id="24d78-148">**Дата последнего изменения**</span><span class="sxs-lookup"><span data-stu-id="24d78-148">**lastmodifieddate**</span></span> <br/> | <span data-ttu-id="24d78-149">Дата документа сайта последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="24d78-149">The last modified date of a site document.</span></span> <br/> |
|<span data-ttu-id="24d78-150">**Отправленные**</span><span class="sxs-lookup"><span data-stu-id="24d78-150">**sent**</span></span> <br/> | <span data-ttu-id="24d78-151">Дата отправки сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="24d78-151">The sent date of an email.</span></span> <br/> |
|<span data-ttu-id="24d78-152">**Кому**</span><span class="sxs-lookup"><span data-stu-id="24d78-152">**to**</span></span> <br/> | <span data-ttu-id="24d78-153">Получателя, указанного в поле в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="24d78-153">The recipient listed in the To field of an email.</span></span> <br/> |
|<span data-ttu-id="24d78-154">**Автор**</span><span class="sxs-lookup"><span data-stu-id="24d78-154">**author**</span></span> <br/> | <span data-ttu-id="24d78-155">Автор документа сайта.</span><span class="sxs-lookup"><span data-stu-id="24d78-155">The author of a site document.</span></span> <br/> |
|<span data-ttu-id="24d78-156">**title**</span><span class="sxs-lookup"><span data-stu-id="24d78-156">**title**</span></span> <br/> | <span data-ttu-id="24d78-157">Заголовок узла документа.</span><span class="sxs-lookup"><span data-stu-id="24d78-157">The title of a site document.</span></span> <br/> |
|<span data-ttu-id="24d78-158">**dominanttheme**\*</span><span class="sxs-lookup"><span data-stu-id="24d78-158">**dominanttheme**\*</span></span> <br/> | <span data-ttu-id="24d78-159">Главный Тема элемента.</span><span class="sxs-lookup"><span data-stu-id="24d78-159">The dominant theme of an item.</span></span> <br/> |
|<span data-ttu-id="24d78-160">**themeslist**\*</span><span class="sxs-lookup"><span data-stu-id="24d78-160">**themeslist**\*</span></span> <br/> | <span data-ttu-id="24d78-161">Темы, связанные с элементом.</span><span class="sxs-lookup"><span data-stu-id="24d78-161">Themes that are associated with an item.</span></span> <br/> |
|<span data-ttu-id="24d78-162">**readpercentile_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="24d78-162">**readpercentile_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="24d78-163">Чтение процентиль элемента, проблемы, определенные в [issuenum].</span><span class="sxs-lookup"><span data-stu-id="24d78-163">The read percentile of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="24d78-164">**relevancescore_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="24d78-164">**relevancescore_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="24d78-165">Показатель релевантности для элемента, проблемы, определенные в [issuenum].</span><span class="sxs-lookup"><span data-stu-id="24d78-165">The relevance score of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="24d78-166">**relevancetag_ [tagname]**\*\*</span><span class="sxs-lookup"><span data-stu-id="24d78-166">**relevancetag_[tagname]**\*\*</span></span> <br/> | <span data-ttu-id="24d78-167">Если у элемента есть вручную помечен для релевантности, тег, определенные в [tagname].</span><span class="sxs-lookup"><span data-stu-id="24d78-167">If an item has been manually tagged for relevance, the tag defined by  [tagname].</span></span> <br/> |
|||

<span data-ttu-id="24d78-168">\*Доступно только если модуль тем уже была запущена.</span><span class="sxs-lookup"><span data-stu-id="24d78-168">\* Only available if the Themes module has been run.</span></span>

<span data-ttu-id="24d78-169">\*\*Доступно только если модуль релевантности уже была запущена.</span><span class="sxs-lookup"><span data-stu-id="24d78-169">\*\* Only available if the Relevance module has been run.</span></span>

<span data-ttu-id="24d78-p106">Кроме того можно использовать карточку условие в расширенной обнаружения электронных данных средства поиска добавить условие (для выбранных свойств) поисковый запрос. На следующем рисунке показан условия, которые можно добавить в запрос. Столбец **группы** указывает, является ли свойство применяется к электронной почте, документы сайта или оба (определяется значением, *Общие*). Этот столбец также определяет для поиска свойств, доступных после запуска модуля релевантности.</span><span class="sxs-lookup"><span data-stu-id="24d78-p106">Alternatively, you can use a condition card in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query. The following screenshot shows the conditions that can be added to a query. The **Group** column indicates whether the property applies to email, site documents, or both (indicated by the value *Common*). This column also identifies the searchable properties that are available after you run the Relevance module.</span></span>

![Условия поиска в средстве поиска расширенной обнаружения электронных данных](media/AeDSearchConditions.png)

<span data-ttu-id="24d78-175">Дополнительные сведения о свойствах для поиска можно [запросах по ключевым словам и условия поиска](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="24d78-175">For more information about searchable properties, see [Keyword queries and search conditions](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="24d78-176">См. также</span><span class="sxs-lookup"><span data-stu-id="24d78-176">See also</span></span>

[<span data-ttu-id="24d78-177">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="24d78-177">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="24d78-178">Общие сведения об оценке в релевантности</span><span class="sxs-lookup"><span data-stu-id="24d78-178">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="24d78-179">Теги и оценки</span><span class="sxs-lookup"><span data-stu-id="24d78-179">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="24d78-180">Теги и учебный курс по релевантности</span><span class="sxs-lookup"><span data-stu-id="24d78-180">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="24d78-181">Отслеживание анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="24d78-181">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="24d78-182">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="24d78-182">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="24d78-183">Тестирование анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="24d78-183">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

