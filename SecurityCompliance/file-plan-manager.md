---
title: Общие сведения о диспетчере плана файлов
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Диспетчер плана файлов обеспечивает расширенные функции управления для политик и меток хранения, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.
ms.openlocfilehash: a6086ce73f898d261af46a1f1493b624db10931d
ms.sourcegitcommit: 799a958fcac643f62dfac6fa04020f2f4758635c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "30997275"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="a9d48-103">Общие сведения о диспетчере плана файлов</span><span class="sxs-lookup"><span data-stu-id="a9d48-103">Overview of file plan manager</span></span>

<span data-ttu-id="a9d48-104">Диспетчер плана файлов обеспечивает расширенные функции управления для политик и меток хранения, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.</span><span class="sxs-lookup"><span data-stu-id="a9d48-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Страница плана файлов](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="a9d48-106">Доступ к диспетчеру плана файлов</span><span class="sxs-lookup"><span data-stu-id="a9d48-106">Accessing file plan manager</span></span>

<span data-ttu-id="a9d48-107">Существуют два требования для доступа к диспетчеру плана файлов. Эти требования приводятся ниже.</span><span class="sxs-lookup"><span data-stu-id="a9d48-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="a9d48-108">Подписка на Office 365 корпоративный E5.</span><span class="sxs-lookup"><span data-stu-id="a9d48-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="a9d48-109">Пользователю назначена одна из следующих ролей &amp;Центра безопасности и соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="a9d48-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span> 
    - <span data-ttu-id="a9d48-110">диспетчер хранения;</span><span class="sxs-lookup"><span data-stu-id="a9d48-110">Retention Manager</span></span>
    - <span data-ttu-id="a9d48-111">диспетчер хранения только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="a9d48-111">View-only Retention Manager</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="a9d48-112">Навигация в плане файлов</span><span class="sxs-lookup"><span data-stu-id="a9d48-112">Navigating your file plan</span></span>

<span data-ttu-id="a9d48-113">Диспетчер плана файлов упрощает просмотр и изучение параметров всех ваших политик и меток хранения в одном представлении.</span><span class="sxs-lookup"><span data-stu-id="a9d48-113">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="a9d48-114">Обратите внимание на то, что метки хранения, созданные вне плана файлов, будут доступны в плане файлов и наоборот.</span><span class="sxs-lookup"><span data-stu-id="a9d48-114">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="a9d48-115">На вкладке **Метки плана файлов** доступна приведенная ниже дополнительная информация и возможности.</span><span class="sxs-lookup"><span data-stu-id="a9d48-115">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="a9d48-116">Столбцы параметров меток</span><span class="sxs-lookup"><span data-stu-id="a9d48-116">Label settings columns</span></span>
 
- <span data-ttu-id="a9d48-p101">**На основе** определяет тип триггера, который устанавливает начало периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a9d48-p101">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="a9d48-119">Событие</span><span class="sxs-lookup"><span data-stu-id="a9d48-119">Event</span></span>
    - <span data-ttu-id="a9d48-120">Дата создания</span><span class="sxs-lookup"><span data-stu-id="a9d48-120">When created</span></span>
    - <span data-ttu-id="a9d48-121">Дата последнего изменения</span><span class="sxs-lookup"><span data-stu-id="a9d48-121">When last modified</span></span>
    - <span data-ttu-id="a9d48-122">Дата метки</span><span class="sxs-lookup"><span data-stu-id="a9d48-122">When labeled</span></span>
- <span data-ttu-id="a9d48-p102">**Запись** определяет, станет ли элемент объявленной записью после присвоения метки. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a9d48-p102">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="a9d48-125">Нет</span><span class="sxs-lookup"><span data-stu-id="a9d48-125">No</span></span>
    - <span data-ttu-id="a9d48-126">Да</span><span class="sxs-lookup"><span data-stu-id="a9d48-126">Yes</span></span>
    - <span data-ttu-id="a9d48-127">Да (норматив)</span><span class="sxs-lookup"><span data-stu-id="a9d48-127">Yes(Regulatory)</span></span>
- <span data-ttu-id="a9d48-p103">**Хранение** определяет тип хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a9d48-p103">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="a9d48-130">Оставить</span><span class="sxs-lookup"><span data-stu-id="a9d48-130">Keep</span></span>
    - <span data-ttu-id="a9d48-131">Оставить и удалить</span><span class="sxs-lookup"><span data-stu-id="a9d48-131">Keep and delete</span></span>
    - <span data-ttu-id="a9d48-132">Удалить</span><span class="sxs-lookup"><span data-stu-id="a9d48-132">Delete</span></span>
- <span data-ttu-id="a9d48-p104">**Ликвидация** определяет, что произойдет с содержимым в конце периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a9d48-p104">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="a9d48-135">пусто</span><span class="sxs-lookup"><span data-stu-id="a9d48-135">null</span></span>
    - <span data-ttu-id="a9d48-136">Нет действий</span><span class="sxs-lookup"><span data-stu-id="a9d48-136">No action</span></span>
    - <span data-ttu-id="a9d48-137">Автоматическое удаление</span><span class="sxs-lookup"><span data-stu-id="a9d48-137">Auto-delete</span></span>
    - <span data-ttu-id="a9d48-138">Требуется проверка (т. е. проверка перед ликвидацией)</span><span class="sxs-lookup"><span data-stu-id="a9d48-138">Review required (aka Disposition review)</span></span>

![Параметры метки в плане файлов](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="a9d48-140">Столбцы дескрипторов плана файлов метки</span><span class="sxs-lookup"><span data-stu-id="a9d48-140">Label file plan descriptors columns</span></span>

<span data-ttu-id="a9d48-p105">Теперь вы можете включать больше информации в конфигурацию ваших меток хранения. Вставка дескрипторов плана файлов в метки повышает управляемость и организацию плана файлов.</span><span class="sxs-lookup"><span data-stu-id="a9d48-p105">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="a9d48-p106">Для быстрого начала работы диспетчер плана файлов содержит некоторые встроенные значения для: функции/отдела, категории, типа сертификации и подготовки/ссылки. Вы можете добавлять новые значения дескриптора плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="a9d48-p106">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="a9d48-145">Вот представление этапа дескрипторов плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="a9d48-145">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Дескрипторы плана файлов](media/file-plan-descriptors.png)

<span data-ttu-id="a9d48-147">Вот представление столбцов дескрипторов плана файлов на вкладке меток диспетчера плана файлов.</span><span class="sxs-lookup"><span data-stu-id="a9d48-147">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="a9d48-149">Экспорт меток из плана файлов</span><span class="sxs-lookup"><span data-stu-id="a9d48-149">Export labels out of your file plan</span></span>

<span data-ttu-id="a9d48-150">Из диспетчера плана файлов можно экспортировать сведения о всех метках хранения в файл .csv, что упростит проведение периодических проверок соответствия требованиям с заинтересованными лицами в сфере управления данными в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="a9d48-150">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="a9d48-151">Чтобы экспортировать все метки хранения, выполните переход: **диспетчер плана файлов** \> **действия плана файлов** \> **экспорт меток**.</span><span class="sxs-lookup"><span data-stu-id="a9d48-151">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Возможность экспортировать план файлов](media/file-plan-export-labels-option.png)

<span data-ttu-id="a9d48-153">Откроется файл с расширением \*.csv, содержащий все существующие метки хранения.</span><span class="sxs-lookup"><span data-stu-id="a9d48-153">A \*.csv file containing all existing retention labels will open.</span></span>

![Файл CSV с отображением всех меток хранения](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="a9d48-155">Импорт меток в план файлов</span><span class="sxs-lookup"><span data-stu-id="a9d48-155">Import labels into your file plan</span></span>

<span data-ttu-id="a9d48-156">Из диспетчера плана файлов можно выполнить массовый импорт новых меток, а также изменять существующие метки хранения.</span><span class="sxs-lookup"><span data-stu-id="a9d48-156">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="a9d48-157">Чтобы импортировать новые метки хранения и внести изменения в существующие метки хранения, выполните переход: **диспетчер плана файлов** \> **действия плана файлов** \> **импорт меток**.</span><span class="sxs-lookup"><span data-stu-id="a9d48-157">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Возможность импортировать план файлов](media/file-plan-import-labels-option.png)

![Возможность скачать пустой шаблон плана файлов](media/file-plan-blank-template-option.png)

<span data-ttu-id="a9d48-160">Скачайте пустой шаблон (или начните с экспорта вашего текущего плана файлов).</span><span class="sxs-lookup"><span data-stu-id="a9d48-160">Download a blank template (or start from an export of your current file plan).</span></span>

![Пустой шаблон плана файлов, открытый в Excel](media/file-plan-blank-template.png)

<span data-ttu-id="a9d48-162">Заполните шаблон (в ближайшее время ожидается справочная информация о допустимых значениях для записей).</span><span class="sxs-lookup"><span data-stu-id="a9d48-162">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![Шаблон плана файлов с заполненной информацией](media/file-plan-filled-out-template.png)

<span data-ttu-id="a9d48-164">Отправьте заполненный шаблон — диспетчер плана файлов проверит записи и отобразит статистику импорта.</span><span class="sxs-lookup"><span data-stu-id="a9d48-164">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Статистика импорта плана файлов](media/file-plan-import-statistics.png)

<span data-ttu-id="a9d48-166">Когда импорт завершится, вернитесь к диспетчеру плана файлов, чтобы назначить новые метки новым или существующим политикам.</span><span class="sxs-lookup"><span data-stu-id="a9d48-166">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Возможность публикации меток](media/file-plan-publish-labels-option.png)

