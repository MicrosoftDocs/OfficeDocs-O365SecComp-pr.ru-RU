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
ms.openlocfilehash: e84f05fa1a7356952b62f2f4adc3b7d0f1ddc94e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258047"
---
# <a name="review-the-data-in-evidence"></a><span data-ttu-id="552c5-102">Просмотр данных в свидетельстве</span><span class="sxs-lookup"><span data-stu-id="552c5-102">Review the data in evidence</span></span>

<span data-ttu-id="552c5-103">Данные в наборе свидетельств во время расследования данных — это моментальный снимок результатов поиска, которые вы собрали и добавляете в набор свидетельств.</span><span class="sxs-lookup"><span data-stu-id="552c5-103">The data in an evidence set in a data investigation is a snapshot of the search results that you collected and added to the evidence set.</span></span> <span data-ttu-id="552c5-104">Когда вы добавляете результаты поиска в свидетельство, процесс запускается для извлечения файлов, метаданных и текста из элементов, возвращенных при поиске.</span><span class="sxs-lookup"><span data-stu-id="552c5-104">When you add search results to evidence, a process is triggered to extract files, metadata, and text from the items returned by the search.</span></span> <span data-ttu-id="552c5-105">Затем средство расследования данных (Предварительная версия) создает новый индекс (процесс с *расширенной индексацией*) всех данных и добавляет к набору свидетельств на вкладке **свидетельство** .</span><span class="sxs-lookup"><span data-stu-id="552c5-105">Then the Data Investigations (Preview) tool then builds a new index (by a process called *Advanced indexing*) of all the data and adds to an evidence set on the **Evidence** tab.</span></span> 

<span data-ttu-id="552c5-106">При расследовании с учетом времени это позволяет быстро включить среду, удалив фактические перенесенные или вредоносные данные, расположенные в исходном источнике данных, в то же время, что позволяет исследовать повторно создаваемые доказательства в Среда, помещенная в карантин, в которой в данном случае данные копируются в набор свидетельства.</span><span class="sxs-lookup"><span data-stu-id="552c5-106">For time-sensitive investigations, this allows you to quickly contain the environment by deleting the actual spilled or malicious data located in the at original data source, while at the same time allowing you to investigate the re-created evidence in a quarantined environment, which in this case is the data copied to the evidence set).</span></span> <span data-ttu-id="552c5-107">После того как свидетельство будет собрано и Добавлено в набор свидетельств, можно просмотреть отдельные документы в собственном формате, в текстовом формате или в близком формате, который можно использовать для аннотирования и исправления документов.</span><span class="sxs-lookup"><span data-stu-id="552c5-107">After the evidence is collected and added to the evidence set, you can review individual documents in their native format, text format, or a near-native format that you can use to annotate and redact documents.</span></span> <span data-ttu-id="552c5-108">Кроме того, вы можете выполнять запросы для сужения набора данных по диапазону времени, типам файлов, владельцам данных и многим другим свойствам и условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="552c5-108">Additionally, you can run queries to narrow the data set by time range, file types, data owners, and many other properties and search conditions.</span></span> <span data-ttu-id="552c5-109">Например, с помощью условий "Автор", "отПравитель" или "получатель" можно быстро определить людей, участвующих в инциденте, а также предоставить доступ к данным из вашей организации к внешним пользователям.</span><span class="sxs-lookup"><span data-stu-id="552c5-109">For example, by using the Author, Sender, or Recipient conditions, you can quickly identify the people are involved in the incident and if any data from your organization has been shared with external users.</span></span> <span data-ttu-id="552c5-110">Дополнительные сведения о поиске в наборе свидетельств можно найти [в статье запрос данных в доказательстве](evidence-query.md).</span><span class="sxs-lookup"><span data-stu-id="552c5-110">For more information about searching through data in an evidence set, see [Query the data in evidence](evidence-query.md).</span></span>

<span data-ttu-id="552c5-111">Чтобы сгруппировать документы и получить дополнительную помощь по проверке, выберите набор свидетельств на вкладке **свидетельство** , а затем нажмите кнопку **Управление доказательством**.</span><span class="sxs-lookup"><span data-stu-id="552c5-111">To group documents and get more assistance for your review, select an evidence set on the **Evidence** tab, and then click **Manage evidence**.</span></span> <span data-ttu-id="552c5-112">В плитке аналитика щелкните **перестроить аналитику для всего набора**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="552c5-112">In the **Analytics** tile, click **Rebuild analytics for the whole set**.</span></span> <span data-ttu-id="552c5-113">При этом будет выполняться Расширенная аналитика, например поиск повторяющихся данных, почтовые потоки и анализ темы.</span><span class="sxs-lookup"><span data-stu-id="552c5-113">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="552c5-114">После этого вы увидите общие темы данных, а также упорядочивайте документы по потокам электронной почты, рядом с дубликатами, а также точные дубликаты, которые помогут провести расследование.</span><span class="sxs-lookup"><span data-stu-id="552c5-114">Afterwards, you can see the general themes of the data and also organize documents by email threads, near duplicates, and exact duplicates to help your investigation.</span></span> <span data-ttu-id="552c5-115">Дополнительные сведения см. [в статье Run Analytics для более быстрого исследования](run-analytics-to-investigate-faster.md).</span><span class="sxs-lookup"><span data-stu-id="552c5-115">For more information, see [Run analytics to investigate faster](run-analytics-to-investigate-faster.md).</span></span>

## <a name="view-documents-in-evidence"></a><span data-ttu-id="552c5-116">Просмотр документов в свидетельстве</span><span class="sxs-lookup"><span data-stu-id="552c5-116">View documents in evidence</span></span>

<span data-ttu-id="552c5-117">Расследования данных (Предварительная версия) позволяет отображать содержимое в нескольких различных средствах просмотра, при этом у каждого средства просмотра есть своя цель.</span><span class="sxs-lookup"><span data-stu-id="552c5-117">Data Investigations (Preview) allows you to display content in several different viewers, with each viewer having a different purpose.</span></span> <span data-ttu-id="552c5-118">Эти средства просмотра:</span><span class="sxs-lookup"><span data-stu-id="552c5-118">These viewers are:</span></span>

- <span data-ttu-id="552c5-119">Метаданные файла</span><span class="sxs-lookup"><span data-stu-id="552c5-119">File metadata</span></span>
- <span data-ttu-id="552c5-120">Собственное представление</span><span class="sxs-lookup"><span data-stu-id="552c5-120">Native view</span></span>
- <span data-ttu-id="552c5-121">Представление текста</span><span class="sxs-lookup"><span data-stu-id="552c5-121">Text view</span></span>
- <span data-ttu-id="552c5-122">Представление "Примечания"</span><span class="sxs-lookup"><span data-stu-id="552c5-122">Annotate view</span></span>

<span data-ttu-id="552c5-123">Чтобы получить доступ к любому из этих средств просмотра, просто выберите документ в наборе свидетельств.</span><span class="sxs-lookup"><span data-stu-id="552c5-123">To access any of these viewers, just select a document in an evidence set.</span></span>

## <a name="file-metadata"></a><span data-ttu-id="552c5-124">Метаданные файла</span><span class="sxs-lookup"><span data-stu-id="552c5-124">File metadata</span></span>

<span data-ttu-id="552c5-125">В этом представлении отображаются различные свойства метаданных, связанные с выбранным документом.</span><span class="sxs-lookup"><span data-stu-id="552c5-125">This view displays various metadata properties associated with the selected document.</span></span> <span data-ttu-id="552c5-126">Чтобы включить или отключить это представление, щелкните **метаданные файла**.</span><span class="sxs-lookup"><span data-stu-id="552c5-126">You can toggle this view on and off by clicking **File metadata**.</span></span> <span data-ttu-id="552c5-127">При просмотре документа можно просматривать метаданные файла и по-прежнему изменять их между различными средствами просмотра.</span><span class="sxs-lookup"><span data-stu-id="552c5-127">When reviewing a document, you can view the file metadata and still change between the different viewers.</span></span>

<span data-ttu-id="552c5-128">Ниже приведен пример метаданных файла для документа.</span><span class="sxs-lookup"><span data-stu-id="552c5-128">Here's an example of the file metadata for a document.</span></span> <span data-ttu-id="552c5-129">Дополнительные сведения о полях метаданных приведены [в статье Document Data расследования (предварительНая версия)](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="552c5-129">For more information about the metadata fields, see [Document metadata fields in Data Investigations (Preview)](document-metadata-fields.md).</span></span>

![Панель метаданных файлов](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="552c5-131">Собственное представление</span><span class="sxs-lookup"><span data-stu-id="552c5-131">Native view</span></span>

<span data-ttu-id="552c5-132">В собственном средстве просмотра отображается наиболее точное представление документа в собственном формате.</span><span class="sxs-lookup"><span data-stu-id="552c5-132">The Native viewer displays the most accurate view of a document in it's native format.</span></span> <span data-ttu-id="552c5-133">Собственное представление поддерживается для сотен типов файлов и предназначено для отображения документов в собственном интерфейсе труест.</span><span class="sxs-lookup"><span data-stu-id="552c5-133">Native view is supported for hundreds of file types and is meant to display documents in the truest native experience possible.</span></span> <span data-ttu-id="552c5-134">Для файлов Microsoft Office в собственном средстве просмотра используется Office Online.</span><span class="sxs-lookup"><span data-stu-id="552c5-134">For Microsoft Office files, the Native viewer uses Office Online.</span></span> <span data-ttu-id="552c5-135">Это позволяет просматривать содержимое, например комментарии в различных документах Office, формулах и скрытых строках и столбцах в Excel, а также представление заМеток в PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="552c5-135">This allows you to view content such as comments in different Office documents, formulas and hidden rows/columns in Excel, and the Notes view in PowerPoint.</span></span>

![<span data-ttu-id="552c5-136">Собственное представление</span><span class="sxs-lookup"><span data-stu-id="552c5-136">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="552c5-137">Представление текста</span><span class="sxs-lookup"><span data-stu-id="552c5-137">Text view</span></span>

<span data-ttu-id="552c5-138">Средство просмотра текста предоставляет представление извлеченного текста файла.</span><span class="sxs-lookup"><span data-stu-id="552c5-138">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="552c5-139">Он игнорирует все внедренные изображения и форматирование, но это представление очень полезно, если вы пытаетесь быстро просмотреть и изучить содержимое документа.</span><span class="sxs-lookup"><span data-stu-id="552c5-139">It ignores any embedded images and formatting, but this view is very useful if you're trying to quickly review and understand the content in a document.</span></span> <span data-ttu-id="552c5-140">Кроме того, в текстовое представление включены следующие функции:</span><span class="sxs-lookup"><span data-stu-id="552c5-140">Text view also includes these features:</span></span>

  - <span data-ttu-id="552c5-141">Счетчик линий, упрощающий ссылки на определенные части документа.</span><span class="sxs-lookup"><span data-stu-id="552c5-141">A line counter, which makes it easier to reference specific portions of a document.</span></span>

  - <span data-ttu-id="552c5-142">Выделение совпадений поиска, выделяющий термины в документе, а также на полосу прокрутки</span><span class="sxs-lookup"><span data-stu-id="552c5-142">Search hit highlighting that highlight terms in the document as well as on the scrollbar</span></span>

  - <span data-ttu-id="552c5-143">Представление diff предоставляет представление сравнения, которое выделяет текстовые различия при просмотре документов с помощью панели **близких дубликатов** .</span><span class="sxs-lookup"><span data-stu-id="552c5-143">A diff view provides a comparison view that highlights the text differences when viewing documents using the **Near duplicates** panel.</span></span>

<span data-ttu-id="552c5-144">**Пример счетчика линии и выделение совпадений поиска в тексте и полоса прокрутки**</span><span class="sxs-lookup"><span data-stu-id="552c5-144">**Example of line counter and search hit highlighting in text and scrollbar**</span></span>

![<span data-ttu-id="552c5-145">Представление текста</span><span class="sxs-lookup"><span data-stu-id="552c5-145">Text view</span></span>
](../media/Reviewimage4.png)

<span data-ttu-id="552c5-146">**Пример представления diff**</span><span class="sxs-lookup"><span data-stu-id="552c5-146">**Example of the diff view**</span></span>

![<span data-ttu-id="552c5-147">Представление diff</span><span class="sxs-lookup"><span data-stu-id="552c5-147">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="552c5-148">Представление "Примечания"</span><span class="sxs-lookup"><span data-stu-id="552c5-148">Annotate view</span></span>

<span data-ttu-id="552c5-149">Представление "Примечания" содержит функции, позволяющие применить разметку к документу во время рецензирования. к ним относятся следующие средства:</span><span class="sxs-lookup"><span data-stu-id="552c5-149">The Annotate view provides features that allow you to apply markup on a document during the review process; this  includes these tools:</span></span>

  - <span data-ttu-id="552c5-150">**Исправления областей** — вы можете нарисовать непрозрачное поле в документе, которое скрывает конфиденциальное содержимое.</span><span class="sxs-lookup"><span data-stu-id="552c5-150">**Area redactions** – You can draw an opaque box on the document that hides sensitive content.</span></span>

  - <span data-ttu-id="552c5-151">**Карандаш** — вы можете свободно рисовать в документе, чтобы привлечь внимание к определенным частям содержимого.</span><span class="sxs-lookup"><span data-stu-id="552c5-151">**Pencil** – You can free-hand draw on a document to bring attention to certain portions of the content</span></span>

  - <span data-ttu-id="552c5-152">**Выбор заметок** — вы можете выбирать и удалять примечания в документе.</span><span class="sxs-lookup"><span data-stu-id="552c5-152">**Select annotations** - You can select and delete annotations in a document.</span></span>

  - <span data-ttu-id="552c5-153">\*\*\*\* Переключать заметку прозрачность — можно переключать прозрачность заметок (между непрозрачным и полупрозрачным), чтобы можно было просматривать содержимое, находящихся за заметкой.</span><span class="sxs-lookup"><span data-stu-id="552c5-153">**Toggle annotation transparency** – You can toggle the transparency of annotations (between opaque and semi-transparent)so you can view the content behind the annotation.</span></span> <span data-ttu-id="552c5-154">Это включает в себя переключение прозрачности аннотаций и исправлений карандаша.</span><span class="sxs-lookup"><span data-stu-id="552c5-154">This includes toggling the transparency of pencil annotations and redactions.</span></span>

<span data-ttu-id="552c5-155">Кроме того, в представлении примечаний предусмотрены следующие функции навигации:</span><span class="sxs-lookup"><span data-stu-id="552c5-155">The Annotate view also provides the following navigation functionality:</span></span>

  - <span data-ttu-id="552c5-156">**Предыдущая страница**, **Следующая страница**и **перейдите к** элементам управления навигацией по страницам, чтобы использовать их для многостраничных документов.</span><span class="sxs-lookup"><span data-stu-id="552c5-156">**Previous page**, **Next page**, and **Go to page** - Navigation controls to use for multi-page documents.</span></span>

  - <span data-ttu-id="552c5-157">**Zoom (увеличить** ) — увеличивает или уменьшает размер документов в представлении "Примечания".</span><span class="sxs-lookup"><span data-stu-id="552c5-157">**Zoom** – Increases or decreases the size of documents in Annotate view.</span></span>

  - <span data-ttu-id="552c5-158">**Поворот** — поворот документов по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="552c5-158">**Rotate** – Rotate documents clockwise.</span></span>

  - <span data-ttu-id="552c5-159">**Поиск** — Поиск ключевых слов в документе, а затем используйте предыдущий и следующий элементы управления для просмотра совпадений (выделено) в документе.</span><span class="sxs-lookup"><span data-stu-id="552c5-159">**Search** – Search for keywords in a document, and then use Previous and Next controls to view the hits (which are highlighted) within the document.</span></span>

<span data-ttu-id="552c5-160">**Пример представления примечаний**</span><span class="sxs-lookup"><span data-stu-id="552c5-160">**Example of Annotate view**</span></span>

![Представление "Примечания"](../media/Reviewimage1.png)

> [!NOTE]
> <span data-ttu-id="552c5-162">Примечания применяются к копии документа, добавленного в набор свидетельств.</span><span class="sxs-lookup"><span data-stu-id="552c5-162">Annotations are applied to a copy of the document that was added to the evidence set.</span></span> <span data-ttu-id="552c5-163">Исходные документы в службе Live не заметок.</span><span class="sxs-lookup"><span data-stu-id="552c5-163">The original documents in the live service aren't annotated.</span></span>
