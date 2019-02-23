---
title: Анализ данных в рабочем наборе в Advanced eDiscovery (Предварительная версия)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: ae024f423ac9b4ab9210ddfab519093a9fee3e42
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216799"
---
# <a name="analyze-data-in-a-working-set-in-advanced-ediscovery-preview"></a><span data-ttu-id="07687-102">Анализ данных в рабочем наборе в Advanced eDiscovery (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="07687-102">Analyze data in a working set in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="07687-p101">При большом количестве собранных документов может быть довольно сложно просмотреть все. Расширенное обнаружение электронных данных (Предварительная версия) предоставляет ряд средств для анализа документов, чтобы сократить объем документов, проверяемых без потери данных, и помочь организовать документы единообразно. Чтобы узнать больше об этих возможностях, ознакомьтесь со статьей:</span><span class="sxs-lookup"><span data-stu-id="07687-p101">When the number of collected documents is large, it can be quite difficult to review them all. Advanced eDiscovery (Preview) provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner. To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="07687-106">Обнаружение схожих документов (почти дубликатов)</span><span class="sxs-lookup"><span data-stu-id="07687-106">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="07687-107">Потоки почты</span><span class="sxs-lookup"><span data-stu-id="07687-107">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="07687-108">Темы</span><span class="sxs-lookup"><span data-stu-id="07687-108">Themes</span></span>](themes.md)

<span data-ttu-id="07687-109">Для анализа данных в рабочем наборе:</span><span class="sxs-lookup"><span data-stu-id="07687-109">To analyze data in a working set:</span></span>

1. <span data-ttu-id="07687-p102">Настройте параметры аналитики для своего случая. Дополнительную информацию можно узнать в статье [Настройка параметров поиска и аналитики](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="07687-p102">Configure analytics settings for your case. For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>
2. <span data-ttu-id="07687-112">Откройте рабочий набор, который вы хотите проанализировать.</span><span class="sxs-lookup"><span data-stu-id="07687-112">Open the working set you wish to analyze.</span></span>
3. <span data-ttu-id="07687-113">Перейдите к разделу "Управление рабочим набором".</span><span class="sxs-lookup"><span data-stu-id="07687-113">Go to "Manage working set".</span></span>
4. <span data-ttu-id="07687-114">Нажмите кнопку "анализ".</span><span class="sxs-lookup"><span data-stu-id="07687-114">Click "Analyze".</span></span>

<span data-ttu-id="07687-115">В этом случае можно проверить ход выполнения анализа на вкладке задания.</span><span class="sxs-lookup"><span data-stu-id="07687-115">You can check the progress of analysis in the Jobs tab in your case.</span></span>

 <span data-ttu-id="07687-116">После завершения анализа вы можете просмотреть аналитический отчет, запускать запросы в рабочем наборе на выходных данных анализа (Дополнительные сведения см. в разделе " [запрос в рабочем наборе](working-set-search.md)"), а также о связанных документах данного документа (Дополнительные сведения см [. Просмотр данных в рабочем наборе](reviewing-data-in-working-set.md)).</span><span class="sxs-lookup"><span data-stu-id="07687-116">Once analysis is completed, you can view analytics report, run queries within your working set on outputs of the analysis (for more information see [Query within your working set](working-set-search.md)), and see related documents of a given document (for more information see [Reviewing data in working set](reviewing-data-in-working-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="07687-117">Аналитический отчет</span><span class="sxs-lookup"><span data-stu-id="07687-117">Analytics report</span></span>

<span data-ttu-id="07687-118">Чтобы просмотреть аналитический отчет для рабочего набора, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="07687-118">To view a analytics report for your working set:</span></span>

1. <span data-ttu-id="07687-119">Откройте рабочий набор.</span><span class="sxs-lookup"><span data-stu-id="07687-119">Open your working set.</span></span>
2. <span data-ttu-id="07687-120">Перейдите к разделу "Управление рабочим набором".</span><span class="sxs-lookup"><span data-stu-id="07687-120">Go to "Manage working set".</span></span>
3. <span data-ttu-id="07687-121">Нажмите кнопку "отчет".</span><span class="sxs-lookup"><span data-stu-id="07687-121">Click "Report".</span></span>

<span data-ttu-id="07687-122">Отчет содержит четыре компонента из анализа:</span><span class="sxs-lookup"><span data-stu-id="07687-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="07687-123">**Подразделение** — количество обнаруженных в рабочем множестве сообщений электронной почты, вложений и свободных документов.</span><span class="sxs-lookup"><span data-stu-id="07687-123">**Breakdown** - How many emails, attachments, and loose documents were found in the working set.</span></span>

- <span data-ttu-id="07687-124">**Документы (за исключением вложений)** — сколько свободных документов было сведено, уникально возле дубликатов сводной таблицы или точной копии другого документа.</span><span class="sxs-lookup"><span data-stu-id="07687-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="07687-125">**Сообщения электронной почты** — сколько электронных писем было инклюзивно, включительно — включительно или ни один из вышеперечисленных вариантов.</span><span class="sxs-lookup"><span data-stu-id="07687-125">**Emails** - How many emails were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="07687-126">**Вложения** . Сколько вложений электронной почты было уникальным или дублировать другое вложение в рабочем наборе.</span><span class="sxs-lookup"><span data-stu-id="07687-126">**Attachments** - How many email attachments were unique or duplicates of a different email attachment within the working set.</span></span>