---
title: Общие сведения о диспетчере плана файлов
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: af398293-c69d-465e-a249-d74561552d30
description: Диспетчер плана хранения предоставляет расширенные функции управления для меток хранения и связанных с ними политик, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.
ms.openlocfilehash: b7d80ff6a7f78e592462fe2723a87383e046015f
ms.sourcegitcommit: 6eb51931242d07abde2e37f1bd57d13bc724f0de
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34547974"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="15905-103">Общие сведения о диспетчере плана файлов</span><span class="sxs-lookup"><span data-stu-id="15905-103">Overview of file plan manager</span></span>

<span data-ttu-id="15905-104">Диспетчер плана хранения предоставляет расширенные функции управления для меток хранения и связанных с ними политик, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.</span><span class="sxs-lookup"><span data-stu-id="15905-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Страница плана файлов](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="15905-106">Доступ к диспетчеру плана файлов</span><span class="sxs-lookup"><span data-stu-id="15905-106">Accessing file plan manager</span></span>

<span data-ttu-id="15905-107">Существуют два требования для доступа к диспетчеру плана файлов. Эти требования приводятся ниже.</span><span class="sxs-lookup"><span data-stu-id="15905-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="15905-108">Подписка на Office 365 корпоративный E5.</span><span class="sxs-lookup"><span data-stu-id="15905-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="15905-109">Пользователю назначена одна из следующих ролей &amp;Центра безопасности и соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="15905-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span>
    - <span data-ttu-id="15905-110">диспетчер хранения;</span><span class="sxs-lookup"><span data-stu-id="15905-110">Retention Manager</span></span>
    - <span data-ttu-id="15905-111">диспетчер хранения только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="15905-111">View-only Retention Manager</span></span>

## <a name="default-retention-labels-and-label-policy"></a><span data-ttu-id="15905-112">Метки хранения и политика меток по умолчанию</span><span class="sxs-lookup"><span data-stu-id="15905-112">Default retention labels and label policy</span></span>

<span data-ttu-id="15905-113">Если в Центре безопасности и соответствия требованиям отсутствуют метки хранения, при первом выборе в левой области навигации пункта **План файлов** создается политика меток под названием **Политика публикации управления данными по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="15905-113">If there are no retention labels in the Security & Compliance Center, the first time you choose **File plan** in the left nav, this creates a label policy called **Default Data Governance Publishing Policy**.</span></span> 

<span data-ttu-id="15905-114">Эта политика меток содержит три метки хранения:</span><span class="sxs-lookup"><span data-stu-id="15905-114">This label policy contains three retention labels:</span></span>

- <span data-ttu-id="15905-115">**Рабочая процедура**</span><span class="sxs-lookup"><span data-stu-id="15905-115">**Operational procedure**</span></span>
- <span data-ttu-id="15905-116">**Общие для предприятия**</span><span class="sxs-lookup"><span data-stu-id="15905-116">**Business general**</span></span>
- <span data-ttu-id="15905-117">**Контрактное соглашение**</span><span class="sxs-lookup"><span data-stu-id="15905-117">**Contract agreement**</span></span>

<span data-ttu-id="15905-118">Эти метки хранения настроены только для хранения содержимого, а не его удаления.</span><span class="sxs-lookup"><span data-stu-id="15905-118">These retention labels are configured only to retain content, not delete content.</span></span> <span data-ttu-id="15905-119">Эта политика меток публикуется для всей организации и может быть отключена или удалена.</span><span class="sxs-lookup"><span data-stu-id="15905-119">This label policy will be published to the entire organization and can be disabled or removed.</span></span> 

<span data-ttu-id="15905-120">Вы можете определить, кто открывал диспетчер плана файлов и выполнил взаимодействие при первом запуске, просмотрев журнал аудита для действий **Созданная политика хранения** и **Созданная конфигурация хранения для политики хранения**.</span><span class="sxs-lookup"><span data-stu-id="15905-120">You can determine who opened file plan manager and kicked off the first-run experience by reviewing the audit log for the activities **Created retention policy** and **Created retention configuration for a retention policy**.</span></span>

> [!NOTE]
> <span data-ttu-id="15905-121">По просьбам пользователей мы убрали эту функцию, создающую приведенные выше метки хранения и политику меток хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15905-121">Due to customer feedback, we have removed this feature that creates the default retention labels and label policy mentioned above.</span></span> <span data-ttu-id="15905-122">Эти метки хранения и политика отображаются, только если вы открыли диспетчер плана хранения до 11 апреля 2019 г.</span><span class="sxs-lookup"><span data-stu-id="15905-122">You will only see this policy and labels if you used file plan manager before April 11, 2019.</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="15905-123">Навигация в плане файлов</span><span class="sxs-lookup"><span data-stu-id="15905-123">Navigating your file plan</span></span>

<span data-ttu-id="15905-124">Диспетчер плана файлов упрощает просмотр и изучение параметров всех ваших политик и меток хранения в одном представлении.</span><span class="sxs-lookup"><span data-stu-id="15905-124">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="15905-125">Обратите внимание на то, что метки хранения, созданные вне плана файлов, будут доступны в плане файлов и наоборот.</span><span class="sxs-lookup"><span data-stu-id="15905-125">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="15905-126">На вкладке **Метки плана файлов** доступна приведенная ниже дополнительная информация и возможности.</span><span class="sxs-lookup"><span data-stu-id="15905-126">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="15905-127">Столбцы параметров меток</span><span class="sxs-lookup"><span data-stu-id="15905-127">Label settings columns</span></span>

- <span data-ttu-id="15905-p103">**На основе** определяет тип триггера, который устанавливает начало периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="15905-p103">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span>
    - <span data-ttu-id="15905-130">Событие</span><span class="sxs-lookup"><span data-stu-id="15905-130">Event</span></span>
    - <span data-ttu-id="15905-131">Дата создания</span><span class="sxs-lookup"><span data-stu-id="15905-131">When created</span></span>
    - <span data-ttu-id="15905-132">Дата последнего изменения</span><span class="sxs-lookup"><span data-stu-id="15905-132">When last modified</span></span>
    - <span data-ttu-id="15905-133">Дата метки</span><span class="sxs-lookup"><span data-stu-id="15905-133">When labeled</span></span>
- <span data-ttu-id="15905-p104">**Запись** определяет, станет ли элемент объявленной записью после присвоения метки. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="15905-p104">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="15905-136">Нет</span><span class="sxs-lookup"><span data-stu-id="15905-136">No</span></span>
    - <span data-ttu-id="15905-137">Да</span><span class="sxs-lookup"><span data-stu-id="15905-137">Yes</span></span>
    - <span data-ttu-id="15905-138">Да (норматив)</span><span class="sxs-lookup"><span data-stu-id="15905-138">Yes(Regulatory)</span></span>
- <span data-ttu-id="15905-p105">**Хранение** определяет тип хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="15905-p105">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="15905-141">Оставить</span><span class="sxs-lookup"><span data-stu-id="15905-141">Keep</span></span>
    - <span data-ttu-id="15905-142">Оставить и удалить</span><span class="sxs-lookup"><span data-stu-id="15905-142">Keep and delete</span></span>
    - <span data-ttu-id="15905-143">Удалить</span><span class="sxs-lookup"><span data-stu-id="15905-143">Delete</span></span>
- <span data-ttu-id="15905-p106">**Ликвидация** определяет, что произойдет с содержимым в конце периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="15905-p106">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span>
    - <span data-ttu-id="15905-146">пусто</span><span class="sxs-lookup"><span data-stu-id="15905-146">null</span></span>
    - <span data-ttu-id="15905-147">Нет действий</span><span class="sxs-lookup"><span data-stu-id="15905-147">No action</span></span>
    - <span data-ttu-id="15905-148">Автоматическое удаление</span><span class="sxs-lookup"><span data-stu-id="15905-148">Auto-delete</span></span>
    - <span data-ttu-id="15905-149">Требуется проверка (т. е. проверка перед ликвидацией)</span><span class="sxs-lookup"><span data-stu-id="15905-149">Review required (aka Disposition review)</span></span>

![Параметры метки в плане файлов](media/file-plan-label-columns.png)

### <a name="retention-label-file-plan-descriptors-columns"></a><span data-ttu-id="15905-151">Столбцы дескрипторов плана хранения для меток</span><span class="sxs-lookup"><span data-stu-id="15905-151">Label file plan descriptors columns</span></span>

<span data-ttu-id="15905-p107">Теперь вы можете включать больше информации в конфигурацию ваших меток хранения. Вставка дескрипторов плана хранения в метки повышает управляемость и организованность плана хранения.</span><span class="sxs-lookup"><span data-stu-id="15905-p107">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="15905-p108">Для быстрого начала работы диспетчер плана файлов содержит некоторые встроенные значения для: функции/отдела, категории, типа сертификации и подготовки/ссылки. Вы можете добавлять новые значения дескриптора плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="15905-p108">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="15905-156">Вот представление этапа дескрипторов плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="15905-156">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Дескрипторы плана файлов](media/file-plan-descriptors.png)

<span data-ttu-id="15905-158">Вот представление столбцов дескрипторов плана файлов на вкладке меток диспетчера плана файлов.</span><span class="sxs-lookup"><span data-stu-id="15905-158">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews"></a><span data-ttu-id="15905-160">Экспорт всех имеющихся меток хранения для анализа и/или проведения автономных проверок</span><span class="sxs-lookup"><span data-stu-id="15905-160">Export all existing retention labels to analyze and/or perform offline reviews</span></span>

<span data-ttu-id="15905-161">Из диспетчера плана файлов можно экспортировать сведения о всех метках хранения в файл .csv, что упростит проведение периодических проверок соответствия требованиям с заинтересованными лицами в сфере управления данными в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="15905-161">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="15905-162">Чтобы экспортировать все метки хранения, выполните переход: **диспетчер плана файлов** \> **действия плана файлов** \> **экспорт меток**.</span><span class="sxs-lookup"><span data-stu-id="15905-162">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Возможность экспортировать план файлов](media/file-plan-export-labels-option.png)

<span data-ttu-id="15905-164">Откроется файл с расширением \*.csv, содержащий все существующие метки хранения.</span><span class="sxs-lookup"><span data-stu-id="15905-164">A \*.csv file containing all existing retention labels will open.</span></span>

![Файл CSV с отображением всех меток хранения](media/file-plan-csv-file.png)

## <a name="import-retention-labels-into-your-file-plan"></a><span data-ttu-id="15905-166">Импорт меток в план хранения</span><span class="sxs-lookup"><span data-stu-id="15905-166">Import labels into your file plan</span></span>

<span data-ttu-id="15905-167">В диспетчере плана хранения можно выполнить массовый импорт новых меток, а также изменять существующие.</span><span class="sxs-lookup"><span data-stu-id="15905-167">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="15905-168">Чтобы импортировать новые метки хранения или изменить существующие, выберите **Диспетчер плана хранения** \> **Действия плана хранения** \> **Импорт меток**.</span><span class="sxs-lookup"><span data-stu-id="15905-168">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Возможность импортировать план файлов](media/file-plan-import-labels-option.png)

![Возможность скачать пустой шаблон плана файлов](media/file-plan-blank-template-option.png)

<span data-ttu-id="15905-171">Скачайте пустой шаблон (или начните с экспорта вашего текущего плана файлов).</span><span class="sxs-lookup"><span data-stu-id="15905-171">Download a blank template (or start from an export of your current file plan).</span></span>

![Пустой шаблон плана файлов, открытый в Excel](media/file-plan-blank-template.png)

<span data-ttu-id="15905-173">Заполните шаблон (в скором времени появятся сведения о допустимых сочетаниях значений для одной метки хранения).</span><span class="sxs-lookup"><span data-stu-id="15905-173">Fill-out the template (coming soon: reference information about valid value combinations for a single retention label).</span></span>

![Шаблон плана файлов с заполненной информацией](media/file-plan-filled-out-template.png)

<span data-ttu-id="15905-175">Отправьте заполненный шаблон — диспетчер плана файлов проверит записи и отобразит статистику импорта.</span><span class="sxs-lookup"><span data-stu-id="15905-175">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Статистика импорта плана файлов](media/file-plan-import-statistics.png)

<span data-ttu-id="15905-177">В случае ошибки проверки в импортированном плане хранения по-прежнему будет проверяться каждая запись в импортированном файле и будут отображаться все ошибки, ссылающиеся на номера строк в импортированном файле. Копируйте отображаемые результаты ошибок, чтобы легко возвращаться к импортированному файлу и исправить ошибки.</span><span class="sxs-lookup"><span data-stu-id="15905-177">In the event there is a validation error, file plan import will continue to validate every entry in the import file and display all errors referencing line/row numbers in the import file, copy the displayed error results so that you can easilly return to the import file and correct the errors.</span></span> 

<span data-ttu-id="15905-178">По завершении импорта вернитесь к диспетчеру плана хранения, чтобы связать новые метки хранения с новыми или существующими политиками.</span><span class="sxs-lookup"><span data-stu-id="15905-178">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Возможность публикации меток](media/file-plan-publish-labels-option.png)

