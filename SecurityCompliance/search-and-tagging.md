---
title: Поиск и тегов
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: Модуль поиска и тегов в расширенной eDiscovery позволяет поиск, предварительный просмотр и организации документов в случае. На данный момент в бета-версии — в этом модуле.
ms.openlocfilehash: fde887e496e9a40aa88d841053a0c66e48f04200
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534927"
---
# <a name="search-and-tagging"></a><span data-ttu-id="ba308-104">Поиск и тегов</span><span class="sxs-lookup"><span data-stu-id="ba308-104">Search and Tagging</span></span>

<span data-ttu-id="ba308-p102">Модуль поиска и тегов в расширенной eDiscovery позволяет поиск, предварительный просмотр и организации документов в случае. На данный момент в бета-версии — в этом модуле.</span><span class="sxs-lookup"><span data-stu-id="ba308-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta.</span></span>

> [!NOTE]
> <span data-ttu-id="ba308-p103">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="ba308-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="ba308-109">Поиск документов в случае</span><span class="sxs-lookup"><span data-stu-id="ba308-109">Search the documents in your case</span></span>

<span data-ttu-id="ba308-p104">После обработки документов в расширенных обнаружения электронных данных и при необходимости выполните анализ модуль или модуль релевантности, можно выполнить поиск и тегов для поиска документов в случае и разместите их использование тегов конкретного примера. Можно определить запросы с использованием карт отмеченными условие, или через язык KQL как запрос в ключевые слова условие карточки. Общий синтаксис KQL, например и, или нет, и NEAR(n), поддерживаемые, а также конечные составные подстановочные знаки (\*). В имени свойства языка запросов поддерживаются следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="ba308-p104">Once you have processed documents in Advanced eDiscovery and optionally run the Analyze module or the Relevance module, you can use Search and Tagging to search through the documents in the case and organize them using case-specific tags. You can define your queries using the provided condition cards, or through a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*). These properties are supported in the query language property name:</span></span>

- <span data-ttu-id="ba308-114">caselabel: теги, созданные/применяется в поиска и тегов для этого случая</span><span class="sxs-lookup"><span data-stu-id="ba308-114">caselabel: tags created/applied in Search and Tagging for this case</span></span> 
- <span data-ttu-id="ba308-115">custodians: custodians, назначенные в случае - может быть ограничения</span><span class="sxs-lookup"><span data-stu-id="ba308-115">custodians: custodians assigned in the case - subject to limitations</span></span>
- <span data-ttu-id="ba308-116">Дата: отправки даты для электронной почты, изменены даты для документов</span><span class="sxs-lookup"><span data-stu-id="ba308-116">date: sent date for email, modified date for documents</span></span>
- <span data-ttu-id="ba308-117">Идентификатор файла: идентификатор файла в случае</span><span class="sxs-lookup"><span data-stu-id="ba308-117">fileid: file ID within the case</span></span>
- <span data-ttu-id="ba308-118">filetype: расширение собственного файла</span><span class="sxs-lookup"><span data-stu-id="ba308-118">filetype: native file extension</span></span>
- <span data-ttu-id="ba308-119">fileclass: электронной почте, документа или вложения</span><span class="sxs-lookup"><span data-stu-id="ba308-119">fileclass: email, document, or attachment</span></span>
- <span data-ttu-id="ba308-120">senderauthor: отправитель сообщения электронной почты, автор для документов</span><span class="sxs-lookup"><span data-stu-id="ba308-120">senderauthor: sender for emails, author for documents</span></span>
- <span data-ttu-id="ba308-121">Размер: размер файла в КБ</span><span class="sxs-lookup"><span data-stu-id="ba308-121">size: size of the file in KB</span></span>
- <span data-ttu-id="ba308-122">subjecttitle: Тема для сообщения электронной почты, должность для документов</span><span class="sxs-lookup"><span data-stu-id="ba308-122">subjecttitle: subject for emails, title for documents</span></span>
- <span data-ttu-id="ba308-123">СК.</span><span class="sxs-lookup"><span data-stu-id="ba308-123">bcc</span></span>
- <span data-ttu-id="ba308-124">копия;</span><span class="sxs-lookup"><span data-stu-id="ba308-124">cc</span></span>
- <span data-ttu-id="ba308-125">Участники: адреса всех участников в поток электронной почты, включая отсутствующих связей электронной почты</span><span class="sxs-lookup"><span data-stu-id="ba308-125">participants: Email addresses of all participants in an email thread, including for missing links</span></span>
- <span data-ttu-id="ba308-126">Получено: дате получения</span><span class="sxs-lookup"><span data-stu-id="ba308-126">received: received date</span></span>
- <span data-ttu-id="ba308-127">Получатели: электронной почты получателя имена или адреса (, cc, скрытой копии)</span><span class="sxs-lookup"><span data-stu-id="ba308-127">recipients: email recipient names or addresses (to, cc, bcc)</span></span>
- <span data-ttu-id="ba308-128">отправитель;</span><span class="sxs-lookup"><span data-stu-id="ba308-128">sender</span></span>
- <span data-ttu-id="ba308-129">Дата последнего изменения: последнее изменение даты документа</span><span class="sxs-lookup"><span data-stu-id="ba308-129">lastmodifieddate: last modified date of a document</span></span>
- <span data-ttu-id="ba308-130">отправлено: отправленные дату сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="ba308-130">sent: sent date of an email</span></span>
- <span data-ttu-id="ba308-131">по</span><span class="sxs-lookup"><span data-stu-id="ba308-131">to</span></span>
- <span data-ttu-id="ba308-132">Автор: автор сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="ba308-132">author: author of an email</span></span>
- <span data-ttu-id="ba308-133">Заголовок: заголовок документа;</span><span class="sxs-lookup"><span data-stu-id="ba308-133">title: title of a document</span></span>
- <span data-ttu-id="ba308-134">dominanttheme: доминирующим элементом Тема элемента\*</span><span class="sxs-lookup"><span data-stu-id="ba308-134">dominanttheme: dominant theme of an item\*</span></span>
- <span data-ttu-id="ba308-135">themeslist: темы, связанные с элемента\*</span><span class="sxs-lookup"><span data-stu-id="ba308-135">themeslist: themes that are associated with an item\*</span></span>
- <span data-ttu-id="ba308-136">readpercentile_ [issuenum]: чтение процентиль элемента по вопросам [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="ba308-136">readpercentile_[issuenum]: read percentile of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="ba308-137">relevancescore_ [issuenum]: показатель релевантности для элемента по вопросам [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="ba308-137">relevancescore_[issuenum]: relevance score of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="ba308-138">relevancetag_ [issuenum]: Если элемент уже вручную помечен для релевантности, его тег для [issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="ba308-138">relevancetag_[issuenum]: if an item has been manually tagged for relevance, its tag for [issuenum]\*\*</span></span>

<span data-ttu-id="ba308-139">\*Доступно только если модуль тем \* \* доступны только если модуль релевантности</span><span class="sxs-lookup"><span data-stu-id="ba308-139">\* Only available if the Themes module has been run \*\* Only available if the Relevance module has been run</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ba308-140">См. также</span><span class="sxs-lookup"><span data-stu-id="ba308-140">See also</span></span>

[<span data-ttu-id="ba308-141">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ba308-141">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ba308-142">Общие сведения об оценке в релевантности</span><span class="sxs-lookup"><span data-stu-id="ba308-142">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ba308-143">Теги и оценки</span><span class="sxs-lookup"><span data-stu-id="ba308-143">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ba308-144">Теги и учебный курс по релевантности</span><span class="sxs-lookup"><span data-stu-id="ba308-144">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ba308-145">Отслеживание анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="ba308-145">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ba308-146">Выбор на основе результатов</span><span class="sxs-lookup"><span data-stu-id="ba308-146">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ba308-147">Тестирование анализа релевантности</span><span class="sxs-lookup"><span data-stu-id="ba308-147">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

