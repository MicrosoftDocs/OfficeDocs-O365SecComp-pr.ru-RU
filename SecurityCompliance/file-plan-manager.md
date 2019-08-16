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
ms.openlocfilehash: 38bfb1e6a6cde931804e518660ddf6c2b45205b0
ms.sourcegitcommit: f443de08971da2fe200a159b8efbed40effba125
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2019
ms.locfileid: "36430016"
---
# <a name="overview-of-file-plan-manager"></a><span data-ttu-id="cfbc0-103">Общие сведения о диспетчере плана файлов</span><span class="sxs-lookup"><span data-stu-id="cfbc0-103">Overview of file plan manager</span></span>

<span data-ttu-id="cfbc0-104">Диспетчер плана хранения предоставляет расширенные функции управления для меток хранения и связанных с ними политик, а также встроенные возможности просмотра меток и действий от меток до содержимого для всего жизненного цикла содержимого — создания, совместной работы, объявления записей, хранения и окончательного удаления.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-104">File plan manager provides advanced management capabilities for retention labels and policies, and provides an integrated way to traverse label and label-to-content activity for your entire content lifecycle – from creation, through collaboration, record declaration, retention, and finally disposition.</span></span>

![Страница плана файлов](media/file-plan-page.png)

## <a name="accessing-file-plan-manager"></a><span data-ttu-id="cfbc0-106">Доступ к диспетчеру плана файлов</span><span class="sxs-lookup"><span data-stu-id="cfbc0-106">Accessing file plan manager</span></span>

<span data-ttu-id="cfbc0-107">Существуют два требования для доступа к диспетчеру плана файлов. Эти требования приводятся ниже.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-107">There are two requirements to access file plan manager, they are:</span></span>
- <span data-ttu-id="cfbc0-108">Подписка на Office 365 корпоративный E5.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-108">An Office 365 Enterprise E5 subscription.</span></span>
- <span data-ttu-id="cfbc0-109">Пользователю назначена одна из следующих ролей &amp;Центра безопасности и соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-109">The user has been in assigned one of the following roles of the Security &amp; Compliance Center:</span></span>
    - <span data-ttu-id="cfbc0-110">диспетчер хранения;</span><span class="sxs-lookup"><span data-stu-id="cfbc0-110">Retention Manager</span></span>
    - <span data-ttu-id="cfbc0-111">диспетчер хранения только для просмотра.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-111">View-only Retention Manager</span></span>

## <a name="default-retention-labels-and-label-policy"></a><span data-ttu-id="cfbc0-112">Метки хранения и политика меток по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cfbc0-112">Default retention labels and label policy</span></span>

<span data-ttu-id="cfbc0-113">Если в Центре безопасности и соответствия требованиям отсутствуют метки хранения, при первом выборе в левой области навигации пункта **План файлов** создается политика меток под названием **Политика публикации управления данными по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-113">If there are no retention labels in the Security & Compliance Center, the first time you choose **File plan** in the left nav, this creates a label policy called **Default Data Governance Publishing Policy**.</span></span> 

<span data-ttu-id="cfbc0-114">Эта политика меток содержит три метки хранения:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-114">This label policy contains three retention labels:</span></span>

- <span data-ttu-id="cfbc0-115">**Рабочая процедура**</span><span class="sxs-lookup"><span data-stu-id="cfbc0-115">**Operational procedure**</span></span>
- <span data-ttu-id="cfbc0-116">**Общие для предприятия**</span><span class="sxs-lookup"><span data-stu-id="cfbc0-116">**Business general**</span></span>
- <span data-ttu-id="cfbc0-117">**Контрактное соглашение**</span><span class="sxs-lookup"><span data-stu-id="cfbc0-117">**Contract agreement**</span></span>

<span data-ttu-id="cfbc0-118">Эти метки хранения настроены только для хранения содержимого, а не его удаления.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-118">These retention labels are configured only to retain content, not delete content.</span></span> <span data-ttu-id="cfbc0-119">Эта политика меток публикуется для всей организации и может быть отключена или удалена.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-119">This label policy will be published to the entire organization and can be disabled or removed.</span></span> 

<span data-ttu-id="cfbc0-120">Вы можете определить, кто открывал диспетчер плана файлов и выполнил взаимодействие при первом запуске, просмотрев журнал аудита для действий **Созданная политика хранения** и **Созданная конфигурация хранения для политики хранения**.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-120">You can determine who opened file plan manager and kicked off the first-run experience by reviewing the audit log for the activities **Created retention policy** and **Created retention configuration for a retention policy**.</span></span>

> [!NOTE]
> <span data-ttu-id="cfbc0-121">По просьбам пользователей мы убрали эту функцию, создающую приведенные выше метки хранения и политику меток хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-121">Due to customer feedback, we have removed this feature that creates the default retention labels and label policy mentioned above.</span></span> <span data-ttu-id="cfbc0-122">Эти метки хранения и политика отображаются, только если вы открыли диспетчер плана хранения до 11 апреля 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-122">You will only see this policy and labels if you used file plan manager before April 11, 2019.</span></span>

## <a name="navigating-your-file-plan"></a><span data-ttu-id="cfbc0-123">Навигация в плане файлов</span><span class="sxs-lookup"><span data-stu-id="cfbc0-123">Navigating your file plan</span></span>

<span data-ttu-id="cfbc0-124">Диспетчер плана файлов упрощает просмотр и изучение параметров всех ваших политик и меток хранения в одном представлении.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-124">File plan manager makes it easier see into and across the settings of all your retention labels and policies from one view.</span></span>

<span data-ttu-id="cfbc0-125">Обратите внимание на то, что метки хранения, созданные вне плана файлов, будут доступны в плане файлов и наоборот.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-125">Note that retention labels created outside of the file plan will be available in the file plan and vice versa.</span></span>

<span data-ttu-id="cfbc0-126">На вкладке **Метки плана файлов** доступна приведенная ниже дополнительная информация и возможности.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-126">On the **file plan labels** tab, the following additional information and capabilities are available:</span></span>

### <a name="label-settings-columns"></a><span data-ttu-id="cfbc0-127">Столбцы параметров меток</span><span class="sxs-lookup"><span data-stu-id="cfbc0-127">Label settings columns</span></span>

- <span data-ttu-id="cfbc0-p103">**На основе** определяет тип триггера, который устанавливает начало периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-p103">**Based on** identifies the type of trigger that will start the retention period. Valid values are:</span></span>
    - <span data-ttu-id="cfbc0-130">Событие</span><span class="sxs-lookup"><span data-stu-id="cfbc0-130">Event</span></span>
    - <span data-ttu-id="cfbc0-131">Дата создания</span><span class="sxs-lookup"><span data-stu-id="cfbc0-131">When created</span></span>
    - <span data-ttu-id="cfbc0-132">Дата последнего изменения</span><span class="sxs-lookup"><span data-stu-id="cfbc0-132">When last modified</span></span>
    - <span data-ttu-id="cfbc0-133">Дата метки</span><span class="sxs-lookup"><span data-stu-id="cfbc0-133">When labeled</span></span>
- <span data-ttu-id="cfbc0-p104">**Запись** определяет, станет ли элемент объявленной записью после присвоения метки. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-p104">**Record** identifies if the item will become a declared record when the label is applied. Valid values are:</span></span>
    - <span data-ttu-id="cfbc0-136">Нет</span><span class="sxs-lookup"><span data-stu-id="cfbc0-136">No</span></span>
    - <span data-ttu-id="cfbc0-137">Да</span><span class="sxs-lookup"><span data-stu-id="cfbc0-137">Yes</span></span>
    - <span data-ttu-id="cfbc0-138">Да (норматив)</span><span class="sxs-lookup"><span data-stu-id="cfbc0-138">Yes(Regulatory)</span></span>
- <span data-ttu-id="cfbc0-p105">**Хранение** определяет тип хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-p105">**Retention** identifies the retention type. Valid values are:</span></span>
    - <span data-ttu-id="cfbc0-141">Оставить</span><span class="sxs-lookup"><span data-stu-id="cfbc0-141">Keep</span></span>
    - <span data-ttu-id="cfbc0-142">Оставить и удалить</span><span class="sxs-lookup"><span data-stu-id="cfbc0-142">Keep and delete</span></span>
    - <span data-ttu-id="cfbc0-143">Удалить</span><span class="sxs-lookup"><span data-stu-id="cfbc0-143">Delete</span></span>
- <span data-ttu-id="cfbc0-p106">**Ликвидация** определяет, что произойдет с содержимым в конце периода хранения. Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-p106">**Disposition** identifies what will happen to the content at the end of the retention period. Valid values are:</span></span>
    - <span data-ttu-id="cfbc0-146">пусто</span><span class="sxs-lookup"><span data-stu-id="cfbc0-146">null</span></span>
    - <span data-ttu-id="cfbc0-147">Нет действий</span><span class="sxs-lookup"><span data-stu-id="cfbc0-147">No action</span></span>
    - <span data-ttu-id="cfbc0-148">Автоматическое удаление</span><span class="sxs-lookup"><span data-stu-id="cfbc0-148">Auto-delete</span></span>
    - <span data-ttu-id="cfbc0-149">Требуется проверка (т. е. проверка перед ликвидацией)</span><span class="sxs-lookup"><span data-stu-id="cfbc0-149">Review required (aka Disposition review)</span></span>

![Параметры метки в плане файлов](media/file-plan-label-columns.png)

### <a name="retention-label-file-plan-descriptors-columns"></a><span data-ttu-id="cfbc0-151">Столбцы дескрипторов плана хранения для меток</span><span class="sxs-lookup"><span data-stu-id="cfbc0-151">Label file plan descriptors columns</span></span>

<span data-ttu-id="cfbc0-p107">Теперь вы можете включать больше информации в конфигурацию ваших меток хранения. Вставка дескрипторов плана хранения в метки повышает управляемость и организованность плана хранения.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-p107">You can now include more information in the configuration of your retention labels. Inserting file plan descriptors into labels will improve the manageability and organization of your file plan.</span></span>

<span data-ttu-id="cfbc0-p108">Для быстрого начала работы диспетчер плана файлов содержит некоторые встроенные значения для: функции/отдела, категории, типа сертификации и подготовки/ссылки. Вы можете добавлять новые значения дескриптора плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-p108">To get you started, file plan manager provides some out-of-box values for: Function/department, Category, Authority type and Provision/citation. You can add new file plan descriptor values when creating or editing a retention label.</span></span>

<span data-ttu-id="cfbc0-156">Вот представление этапа дескрипторов плана файлов при создании или изменении метки хранения.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-156">Here's a view of the file plan descriptors step when creating or editing a retention label.</span></span>

![Дескрипторы плана файлов](media/file-plan-descriptors.png)

<span data-ttu-id="cfbc0-158">Вот представление столбцов дескрипторов плана файлов на вкладке меток диспетчера плана файлов.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-158">Here's a view of the file plan descriptors columns on the labels tab of file plan manager.</span></span>

![file-plan-descriptors-on-labels-tab.png](media/file-plan-descriptors-on-labels-tab.png)

## <a name="export-all-existing-retention-labels-to-analyze-andor-perform-offline-reviews"></a><span data-ttu-id="cfbc0-160">Экспорт всех имеющихся меток хранения для анализа и/или проведения автономных проверок</span><span class="sxs-lookup"><span data-stu-id="cfbc0-160">Export all existing retention labels to analyze and/or perform offline reviews</span></span>

<span data-ttu-id="cfbc0-161">Из диспетчера плана файлов можно экспортировать сведения о всех метках хранения в файл .csv, что упростит проведение периодических проверок соответствия требованиям с заинтересованными лицами в сфере управления данными в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-161">From file plan manager, you can export the details of all retention labels into a .csv file to assist you in facilitating periodic compliance reviews with data governance stakeholders in your organization.</span></span>

<span data-ttu-id="cfbc0-162">Чтобы экспортировать все метки хранения, выполните переход: **диспетчер плана файлов** \> **действия плана файлов** \> **экспорт меток**.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-162">To export all retention labels, go to **file plan manager** \> **file plan actions** \> **export labels**.</span></span>

![Возможность экспортировать план файлов](media/file-plan-export-labels-option.png)

<span data-ttu-id="cfbc0-164">Откроется файл с расширением \*.csv, содержащий все существующие метки хранения.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-164">A \*.csv file containing all existing retention labels will open.</span></span>

![Файл CSV с отображением всех меток хранения](media/file-plan-csv-file.png)

## <a name="import-retention-labels-into-your-file-plan"></a><span data-ttu-id="cfbc0-166">Импорт меток в план хранения</span><span class="sxs-lookup"><span data-stu-id="cfbc0-166">Import labels into your file plan</span></span>

<span data-ttu-id="cfbc0-167">В диспетчере плана хранения можно выполнить массовый импорт новых меток, а также изменять существующие.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-167">From file plan manager, you can bulk import new labels as well as modify existing retention labels.</span></span>

<span data-ttu-id="cfbc0-168">Чтобы импортировать новые метки хранения или изменить существующие, выберите **Диспетчер плана хранения** \> **Действия плана хранения** \> **Импорт меток**.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-168">To import new retention labels and make updates existing retention labels, go to **file plan manager** \> **file plan actions** \> **import labels**.</span></span>

![Возможность импортировать план файлов](media/file-plan-import-labels-option.png)

![Возможность скачать пустой шаблон плана файлов](media/file-plan-blank-template-option.png)

<span data-ttu-id="cfbc0-171">Скачайте пустой шаблон (или начните с экспорта вашего текущего плана файлов).</span><span class="sxs-lookup"><span data-stu-id="cfbc0-171">Download a blank template (or start from an export of your current file plan).</span></span>

![Пустой шаблон плана файлов, открытый в Excel](media/file-plan-blank-template.png)

<span data-ttu-id="cfbc0-173">Заполните шаблон.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-173">Fill-out the template.</span></span> <span data-ttu-id="cfbc0-174">Эта таблица содержит допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-174">This table provides valid values.</span></span>

|<span data-ttu-id="cfbc0-175">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="cfbc0-175">**Property**</span></span>|<span data-ttu-id="cfbc0-176">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cfbc0-176">**Type**</span></span>|<span data-ttu-id="cfbc0-177">**Допустимые значения**</span><span class="sxs-lookup"><span data-stu-id="cfbc0-177">**Valid values**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cfbc0-178">LabelName</span><span class="sxs-lookup"><span data-stu-id="cfbc0-178">LabelName</span></span>|<span data-ttu-id="cfbc0-179">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-179">String</span></span>|<span data-ttu-id="cfbc0-180">Если значение содержит пробелы, заключите его в кавычки (").</span><span class="sxs-lookup"><span data-stu-id="cfbc0-180">If the value contains spaces, enclose the value in quotation marks (").</span></span>|
|<span data-ttu-id="cfbc0-181">Comment</span><span class="sxs-lookup"><span data-stu-id="cfbc0-181">Comment</span></span>|<span data-ttu-id="cfbc0-182">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-182">String</span></span>|<span data-ttu-id="cfbc0-183">Если значение содержит пробелы, заключите его в кавычки (").</span><span class="sxs-lookup"><span data-stu-id="cfbc0-183">If the value contains spaces, enclose the value in quotation marks (").</span></span> |
|<span data-ttu-id="cfbc0-184">Notes</span><span class="sxs-lookup"><span data-stu-id="cfbc0-184">Notes</span></span>|<span data-ttu-id="cfbc0-185">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-185">String</span></span>|<span data-ttu-id="cfbc0-186">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-186">Custom</span></span>|
|<span data-ttu-id="cfbc0-187">IsRecordLabel</span><span class="sxs-lookup"><span data-stu-id="cfbc0-187">IsRecordLabel</span></span>|<span data-ttu-id="cfbc0-188">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-188">String</span></span>|<span data-ttu-id="cfbc0-189">$true: метка является меткой записи.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-189">The label is a record label.</span></span></br><span data-ttu-id="cfbc0-190">$false: метка не является меткой записи.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-190">The label isn't a record label.</span></span> <span data-ttu-id="cfbc0-191">Это значение установлено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-191">This is the default value.</span></span>|
|<span data-ttu-id="cfbc0-192">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="cfbc0-192">RetentionAction</span></span>|<span data-ttu-id="cfbc0-193">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-193">String</span></span>|<span data-ttu-id="cfbc0-194">Delete</span><span class="sxs-lookup"><span data-stu-id="cfbc0-194">Delete</span></span></br><span data-ttu-id="cfbc0-195">Keep</span><span class="sxs-lookup"><span data-stu-id="cfbc0-195">Keep</span></span></br><span data-ttu-id="cfbc0-196">KeepAndDelete</span><span class="sxs-lookup"><span data-stu-id="cfbc0-196">KeepAndDelete</span></span> |
|<span data-ttu-id="cfbc0-197">RetentionDuration</span><span class="sxs-lookup"><span data-stu-id="cfbc0-197">RetentionDuration</span></span>|<span data-ttu-id="cfbc0-198">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-198">String</span></span>|<span data-ttu-id="cfbc0-199">Это свойство указывает срок хранения содержимого (в днях).</span><span class="sxs-lookup"><span data-stu-id="cfbc0-199">The RetentionDuration parameter specifies the number of days to retain the content.</span></span> <span data-ttu-id="cfbc0-200">Допускаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-200">Valid values are:</span></span></br><span data-ttu-id="cfbc0-201">Положительное целое число.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-201">A positive integer.</span></span></br><span data-ttu-id="cfbc0-202">Значение не ограничено.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-202">The default value is unlimited.</span></span>|
|<span data-ttu-id="cfbc0-203">RetentionType</span><span class="sxs-lookup"><span data-stu-id="cfbc0-203">RetentionType</span></span>|<span data-ttu-id="cfbc0-204">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-204">String</span></span>|<span data-ttu-id="cfbc0-205">Это свойство указывает, рассчитывается ли срок хранения с даты создания содержимого, даты пометки (присвоения тега) или даты последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-205">The RetentionType parameter specifies whether the retention duration is calculated  from the content creation date, tagged date, or last modification date.</span></span> <span data-ttu-id="cfbc0-206">Допускаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-206">Valid values are:</span></span></br><span data-ttu-id="cfbc0-207">CreationAgeInDays</span><span class="sxs-lookup"><span data-stu-id="cfbc0-207">CreationAgeInDays</span></span></br><span data-ttu-id="cfbc0-208">EventAgeInDays</span><span class="sxs-lookup"><span data-stu-id="cfbc0-208">EventAgeInDays</span></span></br><span data-ttu-id="cfbc0-209">ModificationAgeInDays</span><span class="sxs-lookup"><span data-stu-id="cfbc0-209">ModificationAgeInDays</span></span></br><span data-ttu-id="cfbc0-210">TaggedAgeInDays</span><span class="sxs-lookup"><span data-stu-id="cfbc0-210">TaggedAgeInDays</span></span> |
|<span data-ttu-id="cfbc0-211">ReviewerEmail</span><span class="sxs-lookup"><span data-stu-id="cfbc0-211">ReviewerEmail</span></span>|<span data-ttu-id="cfbc0-212">SmtpAddress[]</span><span class="sxs-lookup"><span data-stu-id="cfbc0-212">SmtpAddress</span></span>|<span data-ttu-id="cfbc0-213">Это свойство указывает адрес электронной почты проверяющего для действий хранения Delete и KeepAndDelete.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-213">The ReviewerEmail parameter specifies the email address of a reviewer for Delete and KeepAndDelete retention actions.</span></span> <span data-ttu-id="cfbc0-214">Можно указать несколько адресов электронной почты, разделив их запятыми.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-214">You can specify multiple email addresses separated by commas.</span></span>|
|<span data-ttu-id="cfbc0-215">ReferenceId</span><span class="sxs-lookup"><span data-stu-id="cfbc0-215">ReferenceId</span></span>|<span data-ttu-id="cfbc0-216">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-216">String</span></span>|<span data-ttu-id="cfbc0-217">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-217">Custom</span></span>|
|<span data-ttu-id="cfbc0-218">DepartmentName</span><span class="sxs-lookup"><span data-stu-id="cfbc0-218">Departmentname</span></span>|<span data-ttu-id="cfbc0-219">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-219">String</span></span>|<span data-ttu-id="cfbc0-220">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-220">Custom</span></span>|
|<span data-ttu-id="cfbc0-221">Category</span><span class="sxs-lookup"><span data-stu-id="cfbc0-221">Category</span></span>|<span data-ttu-id="cfbc0-222">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-222">String</span></span>|<span data-ttu-id="cfbc0-223">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-223">Custom</span></span>|
|<span data-ttu-id="cfbc0-224">SubCategory</span><span class="sxs-lookup"><span data-stu-id="cfbc0-224">SubCategory</span></span>|<span data-ttu-id="cfbc0-225">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-225">String</span></span>|<span data-ttu-id="cfbc0-226">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-226">Custom</span></span>|
|<span data-ttu-id="cfbc0-227">AuthorityType</span><span class="sxs-lookup"><span data-stu-id="cfbc0-227">AuthorityType</span></span>|<span data-ttu-id="cfbc0-228">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-228">String</span></span>|<span data-ttu-id="cfbc0-229">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-229">Custom</span></span>|
|<span data-ttu-id="cfbc0-230">CitationName</span><span class="sxs-lookup"><span data-stu-id="cfbc0-230">CitationName</span></span>|<span data-ttu-id="cfbc0-231">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-231">String</span></span>|<span data-ttu-id="cfbc0-232">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-232">Custom</span></span>|
|<span data-ttu-id="cfbc0-233">CitationUrl</span><span class="sxs-lookup"><span data-stu-id="cfbc0-233">CitationUrl</span></span>|<span data-ttu-id="cfbc0-234">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-234">String</span></span>|<span data-ttu-id="cfbc0-235">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-235">Custom</span></span>|
|<span data-ttu-id="cfbc0-236">CitationJurisdiction</span><span class="sxs-lookup"><span data-stu-id="cfbc0-236">CitationJurisdiction</span></span>|<span data-ttu-id="cfbc0-237">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-237">String</span></span>|<span data-ttu-id="cfbc0-238">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-238">Custom</span></span>|
|<span data-ttu-id="cfbc0-239">Regulatory</span><span class="sxs-lookup"><span data-stu-id="cfbc0-239">Regulatory</span></span>|<span data-ttu-id="cfbc0-240">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-240">String</span></span>|<span data-ttu-id="cfbc0-241">Настраиваемое</span><span class="sxs-lookup"><span data-stu-id="cfbc0-241">Custom</span></span>|
|<span data-ttu-id="cfbc0-242">EventType</span><span class="sxs-lookup"><span data-stu-id="cfbc0-242">EventType</span></span>|<span data-ttu-id="cfbc0-243">String</span><span class="sxs-lookup"><span data-stu-id="cfbc0-243">String</span></span>|<span data-ttu-id="cfbc0-244">Это свойство указывает правило хранения, связанное с меткой.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-244">This property specifies the retention rule that's associated with the label.</span></span> <span data-ttu-id="cfbc0-245">Можно использовать любое значение, уникальным образом идентифицирующее правило.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-245">You can use any value that uniquely identifies the rule.</span></span> <span data-ttu-id="cfbc0-246">Пример:</span><span class="sxs-lookup"><span data-stu-id="cfbc0-246">For example:</span></span></br><span data-ttu-id="cfbc0-247">имя;</span><span class="sxs-lookup"><span data-stu-id="cfbc0-247">Name</span></span></br><span data-ttu-id="cfbc0-248">различающееся имя (DN);</span><span class="sxs-lookup"><span data-stu-id="cfbc0-248">Distinguished name (DN)</span></span></br><span data-ttu-id="cfbc0-249">GUID.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-249">GUID</span></span> </br><span data-ttu-id="cfbc0-250">Чтобы просмотреть доступные правила хранения, можно использовать командлет [Get-RetentionComplianceRule](https://docs.microsoft.com/ru-RU/powershell/module/exchange/policy-and-compliance-retention/get-retentioncompliancerule?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="cfbc0-250">You can use the [Get-DataEncryptionPolicy](https://docs.microsoft.com/en-us/powershell/module/exchange/policy-and-compliance-retention/get-retentioncompliancerule?view=exchange-ps) cmdlet to view the available policies.</span></span>|

![Шаблон плана файлов с заполненной информацией](media/file-plan-filled-out-template.png)

<span data-ttu-id="cfbc0-252">Отправьте заполненный шаблон — диспетчер плана файлов проверит записи и отобразит статистику импорта.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-252">Upload the filled-out template, and file plan manager will validate the entries and display import statistics.</span></span>

![Статистика импорта плана файлов](media/file-plan-import-statistics.png)

<span data-ttu-id="cfbc0-254">В случае ошибки проверки в импортированном плане хранения по-прежнему будет проверяться каждая запись в импортированном файле и будут отображаться все ошибки, ссылающиеся на номера строк в импортированном файле. Копируйте отображаемые результаты ошибок, чтобы легко возвращаться к импортированному файлу и исправить ошибки.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-254">In the event there is a validation error, file plan import will continue to validate every entry in the import file and display all errors referencing line/row numbers in the import file, copy the displayed error results so that you can easilly return to the import file and correct the errors.</span></span> 

<span data-ttu-id="cfbc0-255">По завершении импорта вернитесь к диспетчеру плана хранения, чтобы связать новые метки хранения с новыми или существующими политиками.</span><span class="sxs-lookup"><span data-stu-id="cfbc0-255">When the import is complete, return to file plan manager to assign new labels to new or existing policies.</span></span>

![Возможность публикации меток](media/file-plan-publish-labels-option.png)

