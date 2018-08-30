---
title: Просмотр результатов анализа в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Понимаете, где можно просмотреть результаты анализа процесса в Office 365 расширенного обнаружения электронных данных, включая определения параметров отображаемых задач.  '
ms.openlocfilehash: 8f1de53e5548c8721f8fbfdb83374edb18379114
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535233"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="4e597-103">Просмотр результатов анализа в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4e597-103">View Analyze results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="4e597-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="4e597-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="4e597-106">В расширенной eDiscovery хода выполнения и результатов для процесса анализа можно просматривать в различных отображается как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="4e597-106">In Advanced eDiscovery, progress and results for the Analyze process can be viewed in a variety of displays as described below.</span></span>
  
## <a name="view-analyze-task-status"></a><span data-ttu-id="4e597-107">Просмотр состояния задачи анализ</span><span class="sxs-lookup"><span data-stu-id="4e597-107">View Analyze task status</span></span>

<span data-ttu-id="4e597-108">В **Prepare \> анализ \> результатов \> состояние задачи**, состояние во время и после выполнения процесса анализа.</span><span class="sxs-lookup"><span data-stu-id="4e597-108">In **Prepare \> Analyze \> Results \> Task status**, the status is displayed during and after Analyze process execution.</span></span> 
  
![Состояние задачи анализа](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
<span data-ttu-id="4e597-110">Отображаемых задач может различаться в зависимости от выбранных параметров.</span><span class="sxs-lookup"><span data-stu-id="4e597-110">The tasks displayed may vary depending on the options selected.</span></span> 
  
- <span data-ttu-id="4e597-111">**ОЕ/ET: программа установки**: подготавливает для выполнения, например, задаются параметры выполнения и вариантов.</span><span class="sxs-lookup"><span data-stu-id="4e597-111">**ND/ET: setup**: Prepares for the run, for example, sets run and case parameters.</span></span>
    
- <span data-ttu-id="4e597-112">**ОЕ/ET: вычисления и**: анализ процессов почти повторяющиеся файлы.</span><span class="sxs-lookup"><span data-stu-id="4e597-112">**ND/ET: ND calculation**: Processes Near-duplicate analysis of files.</span></span>
    
- <span data-ttu-id="4e597-113">**ОЕ/ET: ET вычислений**: потока электронной почты выполняет анализ в наборе всей электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4e597-113">**ND/ET: ET calculation**: Performs Email Thread analysis on the entire email set.</span></span>
    
- <span data-ttu-id="4e597-114">**ОЕ/ET: сводные таблицы и сходства**: выполняет pivot и обработка подобия файла.</span><span class="sxs-lookup"><span data-stu-id="4e597-114">**ND/ET: pivots and similarities**: Performs pivot and file similarity processing.</span></span>
    
- <span data-ttu-id="4e597-115">**ОЕ/ET: обновление метаданных**: завершает новых данных, собранных на файлы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="4e597-115">**ND/ET: metadata update**: Finalizes the new data collected on the files in the database.</span></span>
    
- <span data-ttu-id="4e597-p102">**Тем: тем вычислений**: выполняется анализ тем. (Отображается только в том случае, если выбран).</span><span class="sxs-lookup"><span data-stu-id="4e597-p102">**Themes: themes calculation**: Runs themes analysis. (Displayed only if selected.)</span></span>
    
- <span data-ttu-id="4e597-p103">**Состояние задачи**: Эта строка отображается после завершения задачи. Во время выполнения задачи, отображается длительность.</span><span class="sxs-lookup"><span data-stu-id="4e597-p103">**Task status**: This line is displayed after task completion. While tasks are running, run duration is displayed.</span></span>
    
> [!NOTE]
> <span data-ttu-id="4e597-p104">Анализ результатов рядом с дубликаты и потоков электронной почты (ОЕ и ED) применяется к число документов для обработки. Он не включает точное повторяющиеся файлы.</span><span class="sxs-lookup"><span data-stu-id="4e597-p104">The Analyze results of Near-duplicates and Email Threads (ND and ED) applies to the number of documents to be processed. It does not include Exact duplicate files.</span></span> 
  
## <a name="view-near-duplicates-and-email-threads-status"></a><span data-ttu-id="4e597-122">Просмотр состояния рядом с дубликаты и потоков электронной почты</span><span class="sxs-lookup"><span data-stu-id="4e597-122">View Near-duplicates and Email Threads status</span></span>

<span data-ttu-id="4e597-123">Результаты совокупности **конечного** отображения число документов, по электронной почте, вложения и ошибки в целевого заполнения.</span><span class="sxs-lookup"><span data-stu-id="4e597-123">The **Target** population results display the number of documents, emails, attachments, and errors in the target population.</span></span> 
  
<span data-ttu-id="4e597-124">Результаты **документы** Отображение числа сводные таблицы, уникальные рядом с дубликаты и точное повторяющиеся файлы.</span><span class="sxs-lookup"><span data-stu-id="4e597-124">The **Documents** results display the number of pivots, unique near-duplicates, and exact duplicate files.</span></span> 
  
<span data-ttu-id="4e597-p105">Результаты **по электронной почте** показывать число включительно, включительно минус уникальные включительно копии и остальную часть сообщения электронной почты. Различные типы результатов электронной почты являются:</span><span class="sxs-lookup"><span data-stu-id="4e597-p105">The **Emails** results display the number of inclusive, inclusive minus, unique inclusive copies, and the rest of the email messages. The different types of email results are:</span></span> 
  
- <span data-ttu-id="4e597-p106">**Включающий**: включительно электронной почты — это прерывающие узел в поток электронной почты и содержит все предыдущие журнал данного потока. В результате проверяющий безопасно можно сосредоточиться на включительно электронной почты без необходимости читать предыдущие сообщения в потоке.</span><span class="sxs-lookup"><span data-stu-id="4e597-p106">**Inclusive**: An inclusive email is the terminating node in an email thread and contains all the previous history of that thread. As a result, the reviewer can safely focus on the inclusive email, without the need to read the previous messages in the thread.</span></span> 
    
- <span data-ttu-id="4e597-p107">**Включающий минус**: включительно электронной почты используется в качестве включительно минус при наличии одного или нескольких различных вложений, связанных с родительские включительно сообщения. В этом контекста, термин Parent используется для сообщения, находящиеся в потоке электронной почты или бесед не менее включены в сообщение электронной почты конкретного включительно. Проверяющий можно использовать включительно минус сигнал о том как сигнал, что несмотря на то, что может оказаться необходимые для просмотра содержимого родительские включительно электронной почты, ее можно использовать для просмотра вложений, связанных с родительские путь включительно.</span><span class="sxs-lookup"><span data-stu-id="4e597-p107">**Inclusive minus**: An inclusive email is designated as inclusive minus if there are one or more different attachments associated with the parents of the inclusive message. In this context, the term Parent is used for messages located upwards on the email thread or conversations included in that specific inclusive email. A reviewer can use the inclusive minus indication as a signal that although it might not be necessary to review the content of the inclusive email parents, it may be useful to review the attachments associated with the inclusive path parents.</span></span> 
    
- <span data-ttu-id="4e597-p108">**Включительно копии**: включительно копии, если это копии другое сообщение отмечен как включительно или включительно минус назначенные включительно электронной почты. Другими словами это сообщение имеет же темы и текста как другой включительно сообщение и, таким образом, совместное находится в том же узле. Так как же содержимым включительно копии сообщения, можно обычно пропущена в процессе проверки.</span><span class="sxs-lookup"><span data-stu-id="4e597-p108">**Inclusive copy**: An inclusive email is designated as inclusive copy if it's the copy of another message marked as inclusive or inclusive minus. In other words, this message has the same subject and body as another inclusive message and, as such, co-resides in the same node. Because inclusive copy messages contain the same content, they can usually be skipped in the review process.</span></span> 
    
- <span data-ttu-id="4e597-p109">**Остальные**: указывает электронной почты, которая не содержит уникальный содержимого и поэтому не попадают в любой из предыдущих три категории. Эти сообщения электронной почты не нужно просмотреть. Если сообщение содержит вложение, которая не отображается на более поздней версии включительно электронной почты, вложение может потребоваться для анализа. Это указано при наличии включительно минус электронной почты в рамках потока.</span><span class="sxs-lookup"><span data-stu-id="4e597-p109">**The rest**: This indicates email that doesn't contain any unique content, and therefore doesn't fall into any of the previous three categories. These email messages don't need to be reviewed. If a message contains an attachment that isn't on a later inclusive email, then the attachment might need to be reviewed. This is indicated by the existence of an inclusive minus email within the thread.</span></span>
    
<span data-ttu-id="4e597-139">В результатах **вложения** отображается число вложений от такого типа как уникальный и повторяющиеся значения.</span><span class="sxs-lookup"><span data-stu-id="4e597-139">The **Attachments** results display the number of attachments, according to such type as unique and duplicates.</span></span> 
  
![Почти повторяющиеся результаты и цепочки сообщений](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a><span data-ttu-id="4e597-141">См. также</span><span class="sxs-lookup"><span data-stu-id="4e597-141">See also</span></span>

[<span data-ttu-id="4e597-142">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4e597-142">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="4e597-143">Общие сведения о документе подобия</span><span class="sxs-lookup"><span data-stu-id="4e597-143">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4e597-144">Настройка параметров анализа</span><span class="sxs-lookup"><span data-stu-id="4e597-144">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4e597-145">Параметр Игнорировать текста</span><span class="sxs-lookup"><span data-stu-id="4e597-145">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4e597-146">Анализ параметр Дополнительные параметры</span><span class="sxs-lookup"><span data-stu-id="4e597-146">Setting Analyze advanced settings</span></span>](view-analyze-results-in-advanced-ediscovery.md)

