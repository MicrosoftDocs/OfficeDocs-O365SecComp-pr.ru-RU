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
description: Диспетчер плана файлов обеспечивает расширенные функции управления для политик и меток хранения, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.
ms.openlocfilehash: 377589ab0a8fd2f4c5e73a21eac3988091fa3ed3
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152901"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="786c9-103">Общие сведения о диспетчере плана файлов</span><span class="sxs-lookup"><span data-stu-id="786c9-103">Overview of file plan manager</span></span>

<span data-ttu-id="786c9-104">Диспетчер плана файлов обеспечивает расширенные функции управления для политик и меток хранения, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.</span><span class="sxs-lookup"><span data-stu-id="786c9-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Страница плана файлов](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="786c9-106">Доступ к диспетчеру плана файлов</span><span class="sxs-lookup"><span data-stu-id="786c9-106">Accessing file plan manager</span></span>

<span data-ttu-id="786c9-107">Существуют два требования для доступа к диспетчеру плана файлов. Эти требования приводятся ниже.</span><span class="sxs-lookup"><span data-stu-id="786c9-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="786c9-108">Подписка на Office 365 корпоративный E5.</span><span class="sxs-lookup"><span data-stu-id="786c9-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="786c9-109">Пользователю назначена одна из следующих ролей &amp;Центра безопасности и соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="786c9-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span>
    - <span data-ttu-id="786c9-110">диспетчер хранения;</span><span class="sxs-lookup"><span data-stu-id="786c9-110">Retention Manager</span></span>
    - <span data-ttu-id="786c9-111">диспетчер хранения только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="786c9-111">View-only Retention Manager</span></span>

## <a name="default-retention-labels-and-label-policy"></a><span data-ttu-id="786c9-112">Метки хранения и политика меток по умолчанию</span><span class="sxs-lookup"><span data-stu-id="786c9-112">Default retention labels and label policy</span></span>

<span data-ttu-id="786c9-113">Если в Центре безопасности и соответствия требованиям отсутствуют метки хранения, при первом выборе в левой области навигации пункта **План файлов** создается политика меток под названием **Политика публикации управления данными по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="786c9-113">If there are no retention labels in the Security & Compliance Center, the first time you choose **File plan** in the left nav, this creates a label policy called **Default Data Governance Publishing Policy**.</span></span> 

<span data-ttu-id="786c9-114">Эта политика меток содержит три метки хранения:</span><span class="sxs-lookup"><span data-stu-id="786c9-114">This label policy contains three retention labels:</span></span>

- <span data-ttu-id="786c9-115">**Рабочая процедура**</span><span class="sxs-lookup"><span data-stu-id="786c9-115">**Operational procedure**</span></span>
- <span data-ttu-id="786c9-116">**Общие для предприятия**</span><span class="sxs-lookup"><span data-stu-id="786c9-116">**Business general**</span></span>
- <span data-ttu-id="786c9-117">**Контрактное соглашение**</span><span class="sxs-lookup"><span data-stu-id="786c9-117">**Contract agreement**</span></span>

<span data-ttu-id="786c9-118">Эти метки хранения настроены только для хранения содержимого, а не его удаления.</span><span class="sxs-lookup"><span data-stu-id="786c9-118">These retention labels are configured only to retain content, not delete content.</span></span> <span data-ttu-id="786c9-119">Эта политика меток публикуется для всей организации и может быть отключена или удалена.</span><span class="sxs-lookup"><span data-stu-id="786c9-119">This label policy will be published to the entire organization and can be disabled or removed.</span></span> 

<span data-ttu-id="786c9-120">Вы можете определить, кто открывал диспетчер плана файлов и выполнил взаимодействие при первом запуске, просмотрев журнал аудита для действий **Созданная политика хранения** и **Созданная конфигурация хранения для политики хранения**.</span><span class="sxs-lookup"><span data-stu-id="786c9-120">You can determine who opened file plan manager and kicked off the first-run experience by reviewing the audit log for the activities **Created retention policy** and **Created retention configuration for a retention policy**.</span></span>

> [!NOTE]
> <span data-ttu-id="786c9-121">По просьбам пользователей мы убрали эту функцию, создающую метки хранения и политику хранения по умолчанию, указанные выше.</span><span class="sxs-lookup"><span data-stu-id="786c9-121">Due to customer feedback, we have removed this feature that creates the default retention labels and label policy mentioned above.</span></span> <span data-ttu-id="786c9-122">Эта политика и метки отображались при использовании диспетчера плана только до 11 апреля 2019 г.</span><span class="sxs-lookup"><span data-stu-id="786c9-122">You will only see this policy and labels if you used file plan manager before April 11, 2019.</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="786c9-123">Навигация в плане файлов</span><span class="sxs-lookup"><span data-stu-id="786c9-123">Navigating your file plan</span></span>

<span data-ttu-id="786c9-124">Диспетчер плана файлов упрощает просмотр и изучение параметров всех ваших политик и меток хранения в одном представлении.</span><span class="sxs-lookup"><span data-stu-id="786c9-124">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="786c9-125">Обратите внимание на то, что метки хранения, созданные вне плана файлов, будут доступны в плане файлов и наоборот.</span><span class="sxs-lookup"><span data-stu-id="786c9-125">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="786c9-126">На вкладке **Метки плана файлов** доступна приведенная ниже дополнительная информация и возможности.</span><span class="sxs-lookup"><span data-stu-id="786c9-126">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="786c9-127">Столбцы параметров меток</span><span class="sxs-lookup"><span data-stu-id="786c9-127">Label settings columns</span></span>

- <span data-ttu-id="786c9-p103">**На основе** определяет тип триггера, который устанавливает начало периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="786c9-p103">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span>
    - <span data-ttu-id="786c9-130">Событие</span><span class="sxs-lookup"><span data-stu-id="786c9-130">Event</span></span>
    - <span data-ttu-id="786c9-131">Дата создания</span><span class="sxs-lookup"><span data-stu-id="786c9-131">When created</span></span>
    - <span data-ttu-id="786c9-132">Дата последнего изменения</span><span class="sxs-lookup"><span data-stu-id="786c9-132">When last modified</span></span>
    - <span data-ttu-id="786c9-133">Дата метки</span><span class="sxs-lookup"><span data-stu-id="786c9-133">When labeled</span></span>
- <span data-ttu-id="786c9-p104">**Запись** определяет, станет ли элемент объявленной записью после присвоения метки. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="786c9-p104">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="786c9-136">Нет</span><span class="sxs-lookup"><span data-stu-id="786c9-136">No</span></span>
    - <span data-ttu-id="786c9-137">Да</span><span class="sxs-lookup"><span data-stu-id="786c9-137">Yes</span></span>
    - <span data-ttu-id="786c9-138">Да (норматив)</span><span class="sxs-lookup"><span data-stu-id="786c9-138">Yes(Regulatory)</span></span>
- <span data-ttu-id="786c9-p105">**Хранение** определяет тип хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="786c9-p105">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="786c9-141">Оставить</span><span class="sxs-lookup"><span data-stu-id="786c9-141">Keep</span></span>
    - <span data-ttu-id="786c9-142">Оставить и удалить</span><span class="sxs-lookup"><span data-stu-id="786c9-142">Keep and delete</span></span>
    - <span data-ttu-id="786c9-143">Удалить</span><span class="sxs-lookup"><span data-stu-id="786c9-143">Delete</span></span>
- <span data-ttu-id="786c9-p106">**Ликвидация** определяет, что произойдет с содержимым в конце периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="786c9-p106">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span>
    - <span data-ttu-id="786c9-146">пусто</span><span class="sxs-lookup"><span data-stu-id="786c9-146">null</span></span>
    - <span data-ttu-id="786c9-147">Нет действий</span><span class="sxs-lookup"><span data-stu-id="786c9-147">No action</span></span>
    - <span data-ttu-id="786c9-148">Автоматическое удаление</span><span class="sxs-lookup"><span data-stu-id="786c9-148">Auto-delete</span></span>
    - <span data-ttu-id="786c9-149">Требуется проверка (т. е. проверка перед ликвидацией)</span><span class="sxs-lookup"><span data-stu-id="786c9-149">Review required (aka Disposition review)</span></span>

![Параметры метки в плане файлов](media/file-plan-label-columns.png)

### <a name="label-file-plan-descriptors-columns"></a><span data-ttu-id="786c9-151">Столбцы дескрипторов плана файлов метки</span><span class="sxs-lookup"><span data-stu-id="786c9-151">Label file plan descriptors columns</span></span>

<span data-ttu-id="786c9-p107">Теперь вы можете включать больше информации в конфигурацию ваших меток хранения. Вставка дескрипторов плана файлов в метки повышает управляемость и организацию плана файлов.</span><span class="sxs-lookup"><span data-stu-id="786c9-p107">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="786c9-p108">Для быстрого начала работы диспетчер плана файлов содержит некоторые встроенные значения для: функции/отдела, категории, типа сертификации и подготовки/ссылки. Вы можете добавлять новые значения дескриптора плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="786c9-p108">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="786c9-156">Вот представление этапа дескрипторов плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="786c9-156">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Дескрипторы плана файлов](media/file-plan-descriptors.png)

<span data-ttu-id="786c9-158">Вот представление столбцов дескрипторов плана файлов на вкладке меток диспетчера плана файлов.</span><span class="sxs-lookup"><span data-stu-id="786c9-158">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-labels-out-of-your-file-plan"></a><span data-ttu-id="786c9-160">Экспорт меток из плана файлов</span><span class="sxs-lookup"><span data-stu-id="786c9-160">Export labels out of your file plan</span></span>

<span data-ttu-id="786c9-161">Из диспетчера плана файлов можно экспортировать сведения о всех метках хранения в файл .csv, что упростит проведение периодических проверок соответствия требованиям с заинтересованными лицами в сфере управления данными в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="786c9-161">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="786c9-162">Чтобы экспортировать все метки хранения, выполните переход: **диспетчер плана файлов** \> **действия плана файлов** \> **экспорт меток**.</span><span class="sxs-lookup"><span data-stu-id="786c9-162">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Возможность экспортировать план файлов](media/file-plan-export-labels-option.png)

<span data-ttu-id="786c9-164">Откроется файл с расширением \*.csv, содержащий все существующие метки хранения.</span><span class="sxs-lookup"><span data-stu-id="786c9-164">A \*.csv file containing all existing retention labels will open.</span></span>

![Файл CSV с отображением всех меток хранения](media/file-plan-csv-file.png)

## <a name="import-labels-into-your-file-plan"></a><span data-ttu-id="786c9-166">Импорт меток в план файлов</span><span class="sxs-lookup"><span data-stu-id="786c9-166">Import labels into your file plan</span></span>

<span data-ttu-id="786c9-167">Из диспетчера плана файлов можно выполнить массовый импорт новых меток, а также изменять существующие метки хранения.</span><span class="sxs-lookup"><span data-stu-id="786c9-167">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="786c9-168">Чтобы импортировать новые метки хранения и внести изменения в существующие метки хранения, выполните переход: **диспетчер плана файлов** \> **действия плана файлов** \> **импорт меток**.</span><span class="sxs-lookup"><span data-stu-id="786c9-168">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Возможность импортировать план файлов](media/file-plan-import-labels-option.png)

![Возможность скачать пустой шаблон плана файлов](media/file-plan-blank-template-option.png)

<span data-ttu-id="786c9-171">Скачайте пустой шаблон (или начните с экспорта вашего текущего плана файлов).</span><span class="sxs-lookup"><span data-stu-id="786c9-171">Download a blank template (or start from an export of your current file plan).</span></span>

![Пустой шаблон плана файлов, открытый в Excel](media/file-plan-blank-template.png)

<span data-ttu-id="786c9-173">Заполните шаблон (в ближайшее время ожидается справочная информация о допустимых значениях для записей).</span><span class="sxs-lookup"><span data-stu-id="786c9-173">Fill-out the template (coming soon is reference information about valid values for entries).</span></span>

![Шаблон плана файлов с заполненной информацией](media/file-plan-filled-out-template.png)

<span data-ttu-id="786c9-175">Отправьте заполненный шаблон — диспетчер плана файлов проверит записи и отобразит статистику импорта.</span><span class="sxs-lookup"><span data-stu-id="786c9-175">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Статистика импорта плана файлов](media/file-plan-import-statistics.png)

<span data-ttu-id="786c9-177">Когда импорт завершится, вернитесь к диспетчеру плана файлов, чтобы назначить новые метки новым или существующим политикам.</span><span class="sxs-lookup"><span data-stu-id="786c9-177">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Возможность публикации меток](media/file-plan-publish-labels-option.png)

