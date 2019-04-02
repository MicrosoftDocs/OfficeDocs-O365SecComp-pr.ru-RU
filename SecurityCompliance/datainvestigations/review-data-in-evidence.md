---
title: Просмотр данных в свидетельстве
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
ms.openlocfilehash: 279d2117a69e889f9e605e0ab211c03c5842a59d
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030452"
---
# <a name="review-data-in-evidence"></a><span data-ttu-id="5970c-102">Просмотр данных в свидетельстве</span><span class="sxs-lookup"><span data-stu-id="5970c-102">Review data in evidence</span></span>

<span data-ttu-id="5970c-103">**Свидетельство** — это снимок полученных результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="5970c-103">**Evidence** is a snapshot of search results that you collected.</span></span> <span data-ttu-id="5970c-104">При добавлении результатов поиска в свидетельство процесс запускается для извлечения файлов, метаданных и текста.</span><span class="sxs-lookup"><span data-stu-id="5970c-104">When you add search results to evidence, a process is triggered to extract files, metadata, and text.</span></span> <span data-ttu-id="5970c-105">Затем система создает новый индекс всех данных и добавляется в **свидетельство**.</span><span class="sxs-lookup"><span data-stu-id="5970c-105">Then, the system builds a new index of all the data and adds to **Evidence**.</span></span> 

<span data-ttu-id="5970c-106">Для любых инцидентов с учетом времени это позволяет быстро содержать среду, удаляя данные в исходных расположениях при исследовании повторно созданных доказательств в среде с карантином.</span><span class="sxs-lookup"><span data-stu-id="5970c-106">For any time-sensitive incidents, this allows you to quickly contain the environment by deleting data at original locations while investigating re-created evidence in a quarantined environment.</span></span> <span data-ttu-id="5970c-107">После сбора доказательств можно просматривать отдельные документы в собственном формате, в текстовом формате или в близком формате.</span><span class="sxs-lookup"><span data-stu-id="5970c-107">Once evidence is collected, you can review individual documents in their native format, text format, or a near-native format.</span></span> <span data-ttu-id="5970c-108">Кроме того, вы можете выполнять запросы для сужения данных по диапазону времени, типам файлов, владельцам данных и многим другим условиям.</span><span class="sxs-lookup"><span data-stu-id="5970c-108">Additionally, you can run queries to narrow the data by time range, file types, data owners, and many other condition cards.</span></span> <span data-ttu-id="5970c-109">Используя карточки условия автора/отПравителя или получателя, вы можете быстро проанализировать, кто участвует в Spill, а какие внешние общие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5970c-109">Using Author/Sender/Recipient condition cards, you can quickly examine who are involved in the spill and if there have been any external shares.</span></span> <span data-ttu-id="5970c-110">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="5970c-110">For more information, see:</span></span>

  - [<span data-ttu-id="5970c-111">Запрос данных в доказательстве</span><span class="sxs-lookup"><span data-stu-id="5970c-111">Query the data in evidence</span></span>](evidence-query.md)

<span data-ttu-id="5970c-112">Для группировки документов и получения дополнительной помощи по проверке нажмите кнопку **Управление доказательствами**.</span><span class="sxs-lookup"><span data-stu-id="5970c-112">To group documents and get more assistance for your review, click **Manage evidence**.</span></span> <span data-ttu-id="5970c-113">В плитке **аналитика** щелкните **анализ**.</span><span class="sxs-lookup"><span data-stu-id="5970c-113">In the **Analytics** tile, click **Analyze**.</span></span> <span data-ttu-id="5970c-114">При этом будет выполняться Расширенная аналитика, например поиск повторяющихся данных, почтовые потоки и анализ темы.</span><span class="sxs-lookup"><span data-stu-id="5970c-114">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="5970c-115">После этого вы увидите общие темы данных, а также упорядочивайте документы по потокам электронной почты, точным повторам и близким дубликатам для улучшения расследования.</span><span class="sxs-lookup"><span data-stu-id="5970c-115">Afterwards, you can see the general themes of the data and also organize documents by email threads, exact duplicates and near duplicates to facilitate your investigation.</span></span> <span data-ttu-id="5970c-116">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="5970c-116">For more information, see:</span></span>

  - [<span data-ttu-id="5970c-117">Запуск аналитики для более быстрого исследования</span><span class="sxs-lookup"><span data-stu-id="5970c-117">Run analytics to investigate faster</span></span>](run-analytics-to-investigate-faster.md)

## <a name="view-documents-in-evidence"></a><span data-ttu-id="5970c-118">Просмотр документов в свидетельстве</span><span class="sxs-lookup"><span data-stu-id="5970c-118">View documents in evidence</span></span>

<span data-ttu-id="5970c-119">Исследование данных (Предварительная версия) отображает содержимое по нескольким читателям с разными целями.</span><span class="sxs-lookup"><span data-stu-id="5970c-119">Data investigation (Preview) displays content via several viewers each with different purposes.</span></span> <span data-ttu-id="5970c-120">Можно использовать различные средства просмотра, щелкнув любой документ в доказательстве \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="5970c-120">The various viewers can be used by clicking on any document in **Evidence**.</span></span> <span data-ttu-id="5970c-121">В настоящее время доступны следующие средства просмотра:</span><span class="sxs-lookup"><span data-stu-id="5970c-121">The viewers currently provided are:</span></span>

- <span data-ttu-id="5970c-122">Метаданные файла</span><span class="sxs-lookup"><span data-stu-id="5970c-122">File metadata</span></span>
- <span data-ttu-id="5970c-123">Собственное представление</span><span class="sxs-lookup"><span data-stu-id="5970c-123">Native view</span></span>
- <span data-ttu-id="5970c-124">Представление текста</span><span class="sxs-lookup"><span data-stu-id="5970c-124">Text view</span></span>
- <span data-ttu-id="5970c-125">Представление "Примечания"</span><span class="sxs-lookup"><span data-stu-id="5970c-125">Annotate view</span></span>
- <span data-ttu-id="5970c-126">Преобразованное представление</span><span class="sxs-lookup"><span data-stu-id="5970c-126">Converted view</span></span>

## <a name="file-metadata"></a><span data-ttu-id="5970c-127">Метаданные файла</span><span class="sxs-lookup"><span data-stu-id="5970c-127">File metadata</span></span>

<span data-ttu-id="5970c-128">Эту панель можно включать и отключать для отображения различных метаданных, связанных с документом.</span><span class="sxs-lookup"><span data-stu-id="5970c-128">This panel can be toggled on/off to display various metadata associated with the document.</span></span> <span data-ttu-id="5970c-129">Несмотря на то, что сетка результатов поиска может быть настроена для отображения определенных метаданных, существуют экземпляры, в которых горизонтальная прокрутка может быть затруднительна во время проверки данных.</span><span class="sxs-lookup"><span data-stu-id="5970c-129">Although the search results grid can be customized to display specific metadata, there are instances where scrolling horizontally can be difficult while reviewing data.</span></span> <span data-ttu-id="5970c-130">Панель метаданных файлов позволяет пользователю переключаться между представлениями в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="5970c-130">The File metadata panel allows a user to toggle on a view within the viewer.</span></span>

![<span data-ttu-id="5970c-131">Панель метаданных файлов</span><span class="sxs-lookup"><span data-stu-id="5970c-131">File metadata panel</span></span>
](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="5970c-132">Собственное представление</span><span class="sxs-lookup"><span data-stu-id="5970c-132">Native view</span></span>

<span data-ttu-id="5970c-133">В собственном средстве просмотра отображается большое представление документа.</span><span class="sxs-lookup"><span data-stu-id="5970c-133">The Native viewer displays the richest view of a document.</span></span> <span data-ttu-id="5970c-134">Он поддерживает сотни типов файлов и предназначен для отображения труест в собственной возможности.</span><span class="sxs-lookup"><span data-stu-id="5970c-134">It supports hundreds of file types and is meant to display the truest to native experience possible.</span></span> <span data-ttu-id="5970c-135">Например, для файлов Microsoft Office средство просмотра использует Office Online для отображения содержимого, например комментариев к документам, формул Excel, скрытых строк и столбцов, примечаний PowerPoint и т. д. Для получения дополнительных сведений о средствах просмотра Office Online посетите \[ссылку\]</span><span class="sxs-lookup"><span data-stu-id="5970c-135">For Microsoft Office files, for example, the viewer leverages Office Online in order to display content such as document comments, Excel formulas, hidden rows/columns, PowerPoint notes, etc. For more information regarding the Office Online viewers, visit here \[need link\]</span></span>

![<span data-ttu-id="5970c-136">Собственное представление</span><span class="sxs-lookup"><span data-stu-id="5970c-136">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="5970c-137">Представление текста</span><span class="sxs-lookup"><span data-stu-id="5970c-137">Text view</span></span>

<span data-ttu-id="5970c-138">Средство просмотра текста предоставляет представление извлеченного текста файла.</span><span class="sxs-lookup"><span data-stu-id="5970c-138">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="5970c-139">Он игнорирует все внедренные изображения и форматирование, но это очень производительное представление, если пользователь пытается быстро ознакомиться с контентом.</span><span class="sxs-lookup"><span data-stu-id="5970c-139">It ignores any embedded images and formatting but will be a very performant view if a user is trying to understand the content quickly.</span></span> <span data-ttu-id="5970c-140">Кроме того, текстовое представление включает другие функции:</span><span class="sxs-lookup"><span data-stu-id="5970c-140">Text view also includes other features:</span></span>

  - <span data-ttu-id="5970c-141">Счетчик линии упрощает ссылку на определенные части документа</span><span class="sxs-lookup"><span data-stu-id="5970c-141">Line counter makes it easier to reference specific portions of a document</span></span>

  - <span data-ttu-id="5970c-142">Выделение совпадений поиска, которое выделит термины в документе, а также полосу прокрутки</span><span class="sxs-lookup"><span data-stu-id="5970c-142">Search hit highlighting that will highlight terms within the document as well as the scrollbar</span></span>

  - <span data-ttu-id="5970c-143">Представление diff предоставляет представление сравнения, которое выделяет текстовые различия при просмотре около повторяющихся документов</span><span class="sxs-lookup"><span data-stu-id="5970c-143">Diff view provides a comparison view that highlights textual differences when viewing Near Duplicate documents</span></span>

![<span data-ttu-id="5970c-144">Представление текста</span><span class="sxs-lookup"><span data-stu-id="5970c-144">Text view</span></span>
](../media/Reviewimage4.png)

![<span data-ttu-id="5970c-145">Представление diff</span><span class="sxs-lookup"><span data-stu-id="5970c-145">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="5970c-146">Представление "Примечания"</span><span class="sxs-lookup"><span data-stu-id="5970c-146">Annotate view</span></span>

<span data-ttu-id="5970c-147">Представление "Примечания" содержит функции, позволяющие пользователям применять разметку к документу во время расследования, в том числе:</span><span class="sxs-lookup"><span data-stu-id="5970c-147">The Annotate view provides features that allow users to apply markup on a document during investigation including:</span></span>

  - <span data-ttu-id="5970c-148">Исправления областей — пользователи могут нарисовать рамку в документе, чтобы скрыть конфиденциальный контент.</span><span class="sxs-lookup"><span data-stu-id="5970c-148">Area redactions – users can draw a box on the document in order to hide sensitive content</span></span>

  - <span data-ttu-id="5970c-149">Карандаш — пользователи могут свободно рисовать в документе, чтобы привлечь внимание к определенным частям документа.</span><span class="sxs-lookup"><span data-stu-id="5970c-149">Pencil – users can free-hand draw on a document in order to bring attention to certain portions of a document</span></span>

  - <span data-ttu-id="5970c-150">Выбор примечаний — пользователи могут выбирать примечания в документе для удаления</span><span class="sxs-lookup"><span data-stu-id="5970c-150">Select annotations - users can select annotations on a document in order to delete</span></span>

  - <span data-ttu-id="5970c-151">Включить или отключить заметку прозрачность — делает заметки полупрозрачными, чтобы просматривать содержимое, находящихся за заметкой</span><span class="sxs-lookup"><span data-stu-id="5970c-151">Toggle annotation transparency – makes annotations semi-transparent in order to view the content behind the annotation</span></span>

  - <span data-ttu-id="5970c-152">Предыдущая страница — переход к предыдущей странице</span><span class="sxs-lookup"><span data-stu-id="5970c-152">Previous page – navigates to previous page</span></span>

  - <span data-ttu-id="5970c-153">Следующая страница — переход к следующей странице</span><span class="sxs-lookup"><span data-stu-id="5970c-153">Next page – navigates to the next page</span></span>

  - <span data-ttu-id="5970c-154">Страница "перейти к странице" — пользователь может ввести номер конкретной страницы для перехода</span><span class="sxs-lookup"><span data-stu-id="5970c-154">Go to page – user can enter a specific page number to navigate to</span></span>

  - <span data-ttu-id="5970c-155">Zoom (увеличить) — Задать уровень масштабирования для представления "Заметки"</span><span class="sxs-lookup"><span data-stu-id="5970c-155">Zoom – set zoom level for annotate view</span></span>

  - <span data-ttu-id="5970c-156">Поворот — пользователь может повернуть документ по часовой стрелке</span><span class="sxs-lookup"><span data-stu-id="5970c-156">Rotate – user can rotate document clockwise</span></span>

  - <span data-ttu-id="5970c-157">Search — пользователь может выполнять поиск в документе и переходить к различным совпадениям в документе</span><span class="sxs-lookup"><span data-stu-id="5970c-157">Search – user can search within a document and navigate to the various hits within the document</span></span>
    
    ![<span data-ttu-id="5970c-158">Представление "Примечания"</span><span class="sxs-lookup"><span data-stu-id="5970c-158">Annotate view</span></span>
    ](../media/Reviewimage1.png)

<span data-ttu-id="5970c-159">Обратите внимание, что эти заметки собраны на основании данных, а не в исходном расположении в Live System.</span><span class="sxs-lookup"><span data-stu-id="5970c-159">Note that these annotations are on data collected as evidence, not at its original location in live system.</span></span> 

## <a name="more-information"></a><span data-ttu-id="5970c-160">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="5970c-160">More information</span></span>

<span data-ttu-id="5970c-161">В следующей таблице приведены сведения об ограничении для доказательств в расследовании данных (Предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="5970c-161">The following table lists the limits for evidence in Data Investigations (Preview).</span></span>  <span data-ttu-id="5970c-162">Все элементы, превышающие максимальное количество файлов, будут отображаться как ошибки обработки.</span><span class="sxs-lookup"><span data-stu-id="5970c-162">Any items that exceed the single file maximums will show up as processing errors.</span></span>
    
  |<span data-ttu-id="5970c-163">**Описание ограничения**</span><span class="sxs-lookup"><span data-stu-id="5970c-163">**Description of limit**</span></span>|<span data-ttu-id="5970c-164">**Ограничение**</span><span class="sxs-lookup"><span data-stu-id="5970c-164">**Limit**</span></span>|
  |:-----|:-----|
  |<span data-ttu-id="5970c-165">Максимальное число семейств свидетельств</span><span class="sxs-lookup"><span data-stu-id="5970c-165">Maximum number of evidence collections</span></span>  <br/> |<span data-ttu-id="5970c-166">50</span><span class="sxs-lookup"><span data-stu-id="5970c-166">50</span></span>  <br/> |
  |<span data-ttu-id="5970c-167">Общее количество документов, которые могут быть относиться к обращению (для всех коллекций свидетельств в расследовании)</span><span class="sxs-lookup"><span data-stu-id="5970c-167">Total number of documents that can be ingested into a case (for all evidence collections in the investigation)</span></span>  <br/> |<span data-ttu-id="5970c-168">1 миллион</span><span class="sxs-lookup"><span data-stu-id="5970c-168">1 million</span></span>  <br/> |
  |<span data-ttu-id="5970c-169">Общий размер файлов для каждой нагрузки</span><span class="sxs-lookup"><span data-stu-id="5970c-169">Total file size per load</span></span>  <br/> |<span data-ttu-id="5970c-170">100 ГБ</span><span class="sxs-lookup"><span data-stu-id="5970c-170">100 GB</span></span>  <br/> |
  |<span data-ttu-id="5970c-171">Максимальный размер одного файла</span><span class="sxs-lookup"><span data-stu-id="5970c-171">Maximum size of single file</span></span>   <br/> |<span data-ttu-id="5970c-172">100 МБ</span><span class="sxs-lookup"><span data-stu-id="5970c-172">100 MB</span></span>  <br/> |
  |<span data-ttu-id="5970c-173">Максимальное число символов, извлеченных из одного файла</span><span class="sxs-lookup"><span data-stu-id="5970c-173">Maximum number of characters extracted from a single file</span></span>  <br/> |<span data-ttu-id="5970c-174">10 000 000</span><span class="sxs-lookup"><span data-stu-id="5970c-174">10 million</span></span>  <br/> |
  |<span data-ttu-id="5970c-175">Глубина внедренных элементов в документе</span><span class="sxs-lookup"><span data-stu-id="5970c-175">Depth of embedded items in a document</span></span>  <br/> |<span data-ttu-id="5970c-176">25</span><span class="sxs-lookup"><span data-stu-id="5970c-176">25</span></span>  <br/> |
  