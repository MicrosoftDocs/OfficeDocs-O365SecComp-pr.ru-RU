---
title: Общие сведения о диспетчере плана файлов
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 9/25/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Диспетчер плана файлов обеспечивает расширенные функции управления для политик и меток хранения, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.
ms.openlocfilehash: 4feacf20444591f6da2d55a928a81e86b56c5d9a
ms.sourcegitcommit: 9f34ace6bbe3d5e07e24ebaae96613750869cddf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2018
ms.locfileid: "25019280"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="38345-103">Общие сведения о диспетчере плана файлов</span><span class="sxs-lookup"><span data-stu-id="38345-103">Overview of file plan manager</span></span>

<span data-ttu-id="38345-104">Диспетчер плана файлов обеспечивает расширенные функции управления для политик и меток хранения, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.</span><span class="sxs-lookup"><span data-stu-id="38345-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Страница плана файлов](media/file-plan-page.png)

## <a name="important-this-feature-is-currently-available-only-as-part-of-the-office-365-preview-program"></a><span data-ttu-id="38345-106">Важно: эта функция в настоящее время доступна только в рамках программы Office 365 Preview</span><span class="sxs-lookup"><span data-stu-id="38345-106">Important: This feature is currently available only as part of the Office 365 Preview program</span></span>

<span data-ttu-id="38345-107">Эта функция будет доступна в вашем клиенте только в том случае, если ваша организация зарегистрирована в программе Office 365 Preview.</span><span class="sxs-lookup"><span data-stu-id="38345-107">You will see this feature in your tenant only if your organization has enrolled in the Office 365 Preview program.</span></span>

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="38345-108">Доступ к диспетчеру плана файлов</span><span class="sxs-lookup"><span data-stu-id="38345-108">Accessing file plan manager</span></span>

<span data-ttu-id="38345-109">Существуют два требования для доступа к диспетчеру плана файлов. Эти требования приводятся ниже.</span><span class="sxs-lookup"><span data-stu-id="38345-109">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="38345-110">Подписка на Office 365 корпоративный E5.</span><span class="sxs-lookup"><span data-stu-id="38345-110">An Office 365 Enterprise E5 subscription with user licenses.</span></span>
- <span data-ttu-id="38345-111">Пользователю назначена одна из следующих ролей &amp;Центра безопасности и соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="38345-111">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span> 
    - <span data-ttu-id="38345-112">диспетчер хранения;</span><span class="sxs-lookup"><span data-stu-id="38345-112">Retention Manager</span></span>
    - <span data-ttu-id="38345-113">диспетчер хранения только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="38345-113">View-only Retention Manager</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="38345-114">Навигация в плане файлов</span><span class="sxs-lookup"><span data-stu-id="38345-114">Navigating your file plan</span></span>

<span data-ttu-id="38345-115">Диспетчер плана файлов упрощает просмотр и изучение параметров всех ваших политик и меток хранения в одном представлении.</span><span class="sxs-lookup"><span data-stu-id="38345-115">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="38345-116">Обратите внимание на то, что метки хранения, созданные вне плана файлов, будут доступны в плане файлов и наоборот.</span><span class="sxs-lookup"><span data-stu-id="38345-116">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="38345-117">На вкладке **Метки плана файлов** доступна приведенная ниже дополнительная информация и возможности.</span><span class="sxs-lookup"><span data-stu-id="38345-117">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="38345-118">Столбцы параметров меток</span><span class="sxs-lookup"><span data-stu-id="38345-118">Label settings columns</span></span>
 
- <span data-ttu-id="38345-p101">**На основе** определяет тип триггера, который устанавливает начало периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="38345-p101">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="38345-121">Событие</span><span class="sxs-lookup"><span data-stu-id="38345-121">Event</span></span>
    - <span data-ttu-id="38345-122">Дата создания</span><span class="sxs-lookup"><span data-stu-id="38345-122">When created</span></span>
    - <span data-ttu-id="38345-123">Дата последнего изменения</span><span class="sxs-lookup"><span data-stu-id="38345-123">When last modified</span></span>
    - <span data-ttu-id="38345-124">Дата метки</span><span class="sxs-lookup"><span data-stu-id="38345-124">When labeled</span></span>
- <span data-ttu-id="38345-p102">**Запись** определяет, станет ли элемент объявленной записью после присвоения метки. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="38345-p102">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="38345-127">Нет</span><span class="sxs-lookup"><span data-stu-id="38345-127">No</span></span>
    - <span data-ttu-id="38345-128">Да</span><span class="sxs-lookup"><span data-stu-id="38345-128">Yes</span></span>
    - <span data-ttu-id="38345-129">Да (норматив)</span><span class="sxs-lookup"><span data-stu-id="38345-129">Yes(Regulatory)</span></span>
- <span data-ttu-id="38345-p103">**Хранение** определяет тип хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="38345-p103">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="38345-132">Оставить</span><span class="sxs-lookup"><span data-stu-id="38345-132">Keep</span></span>
    - <span data-ttu-id="38345-133">Оставить и удалить</span><span class="sxs-lookup"><span data-stu-id="38345-133">Keep and delete</span></span>
    - <span data-ttu-id="38345-134">Удалить</span><span class="sxs-lookup"><span data-stu-id="38345-134">Delete</span></span>
- <span data-ttu-id="38345-p104">**Ликвидация** определяет, что произойдет с содержимым в конце периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="38345-p104">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span> 
    - <span data-ttu-id="38345-137">пусто</span><span class="sxs-lookup"><span data-stu-id="38345-137">Null</span></span>
    - <span data-ttu-id="38345-138">Нет действий</span><span class="sxs-lookup"><span data-stu-id="38345-138">No action necessary.</span></span>
    - <span data-ttu-id="38345-139">Автоматическое удаление</span><span class="sxs-lookup"><span data-stu-id="38345-139">Auto-delete</span></span>
    - <span data-ttu-id="38345-140">Требуется проверка (т. е. проверка перед ликвидацией)</span><span class="sxs-lookup"><span data-stu-id="38345-140">Review required (aka Disposition review)</span></span>

![Параметры метки в плане файлов](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="38345-142">Столбцы дескрипторов плана файлов метки</span><span class="sxs-lookup"><span data-stu-id="38345-142">Label file plan descriptors columns</span></span>

<span data-ttu-id="38345-p105">Теперь вы можете включать больше информации в конфигурацию ваших меток хранения. Вставка дескрипторов плана файлов в метки повышает управляемость и организацию плана файлов.</span><span class="sxs-lookup"><span data-stu-id="38345-p105">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="38345-p106">Для быстрого начала работы диспетчер плана файлов содержит некоторые встроенные значения для: функции/отдела, категории, типа сертификации и подготовки/ссылки. Вы можете добавлять новые значения дескриптора плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="38345-p106">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="38345-147">Вот представление этапа дескрипторов плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="38345-147">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Дескрипторы плана файлов](media/file-plan-descriptors.png)

<span data-ttu-id="38345-149">Вот представление столбцов дескрипторов плана файлов на вкладке меток диспетчера плана файлов.</span><span class="sxs-lookup"><span data-stu-id="38345-149">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="38345-151">Экспорт меток из плана файлов</span><span class="sxs-lookup"><span data-stu-id="38345-151">Export labels out of your file plan</span></span>

<span data-ttu-id="38345-152">Из диспетчера плана файлов можно экспортировать сведения о всех метках хранения в файл .csv, что упростит проведение периодических проверок соответствия требованиям с заинтересованными лицами в сфере управления данными в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="38345-152">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="38345-153">Чтобы экспортировать все метки хранения, выполните переход: **диспетчер плана файлов** \> **действия плана файлов** \> **экспорт меток**.</span><span class="sxs-lookup"><span data-stu-id="38345-153">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Возможность экспортировать план файлов](media/file-plan-export-labels-option.png)

<span data-ttu-id="38345-155">Откроется файл с расширением \*.csv, содержащий все существующие метки хранения.</span><span class="sxs-lookup"><span data-stu-id="38345-155">A \*.csv file containing all existing retention labels will open.</span></span>

![Файл CSV с отображением всех меток хранения](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="38345-157">Импорт меток в план файлов</span><span class="sxs-lookup"><span data-stu-id="38345-157">Import labels into your file plan</span></span>

<span data-ttu-id="38345-158">Из диспетчера плана файлов можно выполнить массовый импорт новых меток, а также изменять существующие метки хранения.</span><span class="sxs-lookup"><span data-stu-id="38345-158">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="38345-159">Чтобы импортировать новые метки хранения и внести изменения в существующие метки хранения, выполните переход: **диспетчер плана файлов** \> **действия плана файлов** \> **импорт меток**.</span><span class="sxs-lookup"><span data-stu-id="38345-159">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Возможность импортировать план файлов](media/file-plan-import-labels-option.png)

![Возможность скачать пустой шаблон плана файлов](media/file-plan-blank-template-option.png)

<span data-ttu-id="38345-162">Скачайте пустой шаблон (или начните с экспорта вашего текущего плана файлов).</span><span class="sxs-lookup"><span data-stu-id="38345-162">Download a blank template (or start from an export of your current file plan).</span></span>

![Пустой шаблон плана файлов, открытый в Excel](media/file-plan-blank-template.png)

<span data-ttu-id="38345-164">Заполните шаблон (в ближайшее время ожидается справочная информация о допустимых значениях для записей).</span><span class="sxs-lookup"><span data-stu-id="38345-164">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![Шаблон плана файлов с заполненной информацией](media/file-plan-filled-out-template.png)

<span data-ttu-id="38345-166">Отправьте заполненный шаблон — диспетчер плана файлов проверит записи и отобразит статистику импорта.</span><span class="sxs-lookup"><span data-stu-id="38345-166">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Статистика импорта плана файлов](media/file-plan-import-statistics.png)

<span data-ttu-id="38345-168">Когда импорт завершится, вернитесь к диспетчеру плана файлов, чтобы назначить новые метки новым или существующим политикам.</span><span class="sxs-lookup"><span data-stu-id="38345-168">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Возможность публикации меток](media/file-plan-publish-labels-option.png)

