---
title: Заметки о выПуске Microsoft соответствие требованиям
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Диспетчер соответствия требованиям Майкрософт — бесплатное средство оценки рисков на основе рабочих процессов на портале доверия службы Майкрософт. Диспетчер соответствия требованиям позволяет отслеживать, назначать и проверять нормативные действия, связанные с облачными службами Майкрософт.
ms.openlocfilehash: 5e18445e3f9ad2848f18174788ec6dd40bc4a178
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473194"
---
# <a name="release-notes-for-compliance-manager-preview"></a><span data-ttu-id="3cf16-104">Заметки о выПуске для диспетчера соответствия требованиям (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="3cf16-104">Release Notes for Compliance Manager (Preview)</span></span>

<span data-ttu-id="3cf16-105">Общедоступная Предварительная версия диспетчера соответствия требованиям обеспечивает ранний доступ к предстоящим функциям и обновлениям.</span><span class="sxs-lookup"><span data-stu-id="3cf16-105">The public preview of Compliance Manager provides you with early access to upcoming functionality and updates.</span></span>

<span data-ttu-id="3cf16-106">С помощью обновленного средства " [Диспетчер соответствия требованиям](https://servicetrust.microsoft.com/ComplianceManager) " на [портале доверия службы](https://servicetrust.microsoft.com) можно отслеживать, назначать и проверять нормативные действия, связанные с облачными службами Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3cf16-106">You can use the updated [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) tool on the [Service Trust Portal](https://servicetrust.microsoft.com) to track, assign, and verify regulatory compliance activities related to Microsoft cloud services.</span></span>

## <a name="whats-new-in-compliance-manager-preview"></a><span data-ttu-id="3cf16-107">Новые возможности в диспетчере соответствия требованиям (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="3cf16-107">What’s new in Compliance Manager (Preview)</span></span>

- <span data-ttu-id="3cf16-108">**Интеграция с показателЕм безопасности Майкрософт:** Диспетчер соответствия требованиям поддерживает интеграцию с [рейтингОм безопасности Майкрософт](microsoft-secure-score.md) путем сопоставления действий, управляемых клиентами, с более чем 50 действиями по безопасному рейтингу.</span><span class="sxs-lookup"><span data-stu-id="3cf16-108">**Integration with Microsoft Secure Score:** Compliance Manager supports integration with [Microsoft Secure Score](microsoft-secure-score.md) by mapping customer-managed Actions to more than 50 Secure Score actions.</span></span> <span data-ttu-id="3cf16-109">После выполнения сопоставленного действия в показателе безопасности соответствующее действие диспетчера соответствия автоматически обновляется.</span><span class="sxs-lookup"><span data-stu-id="3cf16-109">When you complete a mapped action in Secure Score, the corresponding Compliance Manager Action is automatically updated.</span></span>

- <span data-ttu-id="3cf16-110">**Импорт настраиваемЫх оценок:** Помимо встроенных оценок, диспетчер соответствия требованиям теперь поддерживает импорт пользовательских шаблонов, позволяя создавать пользовательские оценки для любого продукта или службы, а также любые стандартные или нормативные требования.</span><span class="sxs-lookup"><span data-stu-id="3cf16-110">**Import custom Assessments:** In addition to built-in Assessments, Compliance Manager now supports importing custom Templates, enabling you to create custom Assessments for any product or service and any standard or regulation.</span></span>

- <span data-ttu-id="3cf16-111">**Элементы действий:** Элементы Action теперь являются отдельными элементами, и многие из них включают коллекцию телеметрии из API графа Microsoft Secure scores.</span><span class="sxs-lookup"><span data-stu-id="3cf16-111">**Actions Items:** Action Items are now individual items and many include telemetry collection from the Microsoft Secure Score Graph API.</span></span> <span data-ttu-id="3cf16-112">Там, где это возможно, в технических рекомендациях теперь есть ссылки на страницу "соответствующая конфигурация" в службе Office 365.</span><span class="sxs-lookup"><span data-stu-id="3cf16-112">Where possible, technical action recommendations now have links to the applicable configuration page in the Office 365 service.</span></span>

- <span data-ttu-id="3cf16-113">**Управление клиентами:** Новый интерфейс для управления новыми элементами данных в диспетчере соответствия требованиям (Предварительная версия):</span><span class="sxs-lookup"><span data-stu-id="3cf16-113">**Tenant Management:** New interface for managing new data elements in Compliance Manager (Preview):</span></span>
    - <span data-ttu-id="3cf16-114">**Измерения:** Просматривать, добавлять и настраивать метаданные для шаблонов, оценок и действий, которые позволяют создавать настраиваемые сводные элементы для фильтров.</span><span class="sxs-lookup"><span data-stu-id="3cf16-114">**Dimensions:** View, add and customize metadata for Templates, Assessments, and Action Items that allow you to create custom pivots for filters.</span></span>
    - <span data-ttu-id="3cf16-115">**Владельцы:** Укажите владельца для каждого элемента Action.</span><span class="sxs-lookup"><span data-stu-id="3cf16-115">**Owners:** Specify an owner for each Action Item.</span></span>
    - <span data-ttu-id="3cf16-116">**Действия клиента:** Управление полным списком элементов действий, включенных в Диспетчер соответствия требованиям (Предварительная версия), а также включение и отключение мониторинга безопасного индекса для элементов действий, интегрированных с показателем безопасности.</span><span class="sxs-lookup"><span data-stu-id="3cf16-116">**Customer Actions:** Manage the complete list of Actions Items included in Compliance Manager (Preview) and enable/disable Secure Score monitoring for Action Items that are integrated with Secure Score.</span></span>

- <span data-ttu-id="3cf16-117">**ОбновленНый показатель соответствия требованиям**: методология изменилась для поддержки синхронизации с показателем безопасности Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3cf16-117">**Updated Compliance Score**: The methodology has changed to support syncing with Microsoft Secure Score.</span></span> <span data-ttu-id="3cf16-118">Система оценки удаляет кредиты управления, управляемые Майкрософт, и фокусируется исключительно на выполнении элементов управления, управляемых заказчиком.</span><span class="sxs-lookup"><span data-stu-id="3cf16-118">The scoring system removes the Microsoft-managed control credits and focuses solely on the completion of customer-managed controls.</span></span>

## <a name="known-issues-in-compliance-manager-preview"></a><span data-ttu-id="3cf16-119">Известные проблемы в диспетчере соответствия требованиям (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="3cf16-119">Known issues in Compliance Manager (Preview)</span></span>

<span data-ttu-id="3cf16-120">В следующих разделах рассматриваются известные проблемы, которые необходимо устранить в будущих выпусках диспетчера соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="3cf16-120">The following sections cover known issues to be resolved in upcoming releases of Compliance Manager.</span></span>

### <a name="compliance-score"></a><span data-ttu-id="3cf16-121">Оценка соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="3cf16-121">Compliance Score</span></span>

- <span data-ttu-id="3cf16-122">Когда элементы Action помечаются как не включенные **в область**действия, баллы, назначенные для элемента Action, не исключаются из вычисления оценки соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="3cf16-122">When Action Items are marked as **Not in Scope**, the score assigned to the Action Item is not excluded from the Compliance Score calculation.</span></span> <span data-ttu-id="3cf16-123">Элементы действий, помеченные **не в области** , не должны повышать уровень соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="3cf16-123">Action Items marked **Not in Scope** should not increase your Compliance Score.</span></span>

### <a name="microsoft-managed-controls"></a><span data-ttu-id="3cf16-124">Элементы управления, управляемые корпорацией Майкрософт</span><span class="sxs-lookup"><span data-stu-id="3cf16-124">Microsoft-managed Controls</span></span>

- <span data-ttu-id="3cf16-125">Тестовая дата для элементов управления, управляемых Майкрософт, не отображается в ПОЛЬЗОВАТЕЛЬСКОМ ИНТЕРФЕЙСе, даже если она включена в оценку.</span><span class="sxs-lookup"><span data-stu-id="3cf16-125">The test date for Microsoft-managed controls is not appearing in the UI, even when included in the Assessment.</span></span> <span data-ttu-id="3cf16-126">Чтобы просмотреть сведения о дате тестирования, необходимо экспортировать оценку.</span><span class="sxs-lookup"><span data-stu-id="3cf16-126">To see test date information, you must export the Assessment.</span></span>

### <a name="customization"></a><span data-ttu-id="3cf16-127">Настройка</span><span class="sxs-lookup"><span data-stu-id="3cf16-127">Customization</span></span>

- <span data-ttu-id="3cf16-128">Добавление пользовательских элементов управления позволяет добавить новый элемент управления к существующему семейству элементов управления, но не позволяет добавить новое семейство элементов управления.</span><span class="sxs-lookup"><span data-stu-id="3cf16-128">Adding custom Controls enables adding a new control to an existing control family, but it does not allow you to add a new Control Family.</span></span>
- <span data-ttu-id="3cf16-129">Этот выпуск не поддерживает связывание элементов действий и добавление действий или элементов управления для оценки.</span><span class="sxs-lookup"><span data-stu-id="3cf16-129">This release does not support linking Action Items or adding Actions Items or Controls to an Assessment.</span></span>
- <span data-ttu-id="3cf16-130">Если вы создаете дополнительное действие, его невозможно изменить или удалить.</span><span class="sxs-lookup"><span data-stu-id="3cf16-130">If you create a custom Action, you cannot edit or delete it.</span></span>

### <a name="control-families-not-shown-in-assessments"></a><span data-ttu-id="3cf16-131">Семейства элементов управления, не показанные в ходе оценки</span><span class="sxs-lookup"><span data-stu-id="3cf16-131">Control Families Not Shown in Assessments</span></span>

- <span data-ttu-id="3cf16-132">При импорте шаблона все оценки, основанные на этом шаблоне, будут отражать все семейства элементов управления, которые входят в шаблон.</span><span class="sxs-lookup"><span data-stu-id="3cf16-132">When you import a Template, all Assessments based on that Template will reflect all Control Families that are part of the Template.</span></span> <span data-ttu-id="3cf16-133">Но если вы добавите в шаблон новые элементы управления, все существующие оценки не отразятся на изменениях.</span><span class="sxs-lookup"><span data-stu-id="3cf16-133">But if you add new Control Families to the Template, any existing Assessments will not reflect the changes.</span></span> <span data-ttu-id="3cf16-134">Изменения будут отражены только в новых оценках, созданных с помощью обновленного шаблона.</span><span class="sxs-lookup"><span data-stu-id="3cf16-134">Only new Assessments created off the updated Template will reflect the changes.</span></span>

### <a name="filters"></a><span data-ttu-id="3cf16-135">Фильтры</span><span class="sxs-lookup"><span data-stu-id="3cf16-135">Filters</span></span>

- <span data-ttu-id="3cf16-136">Фильтрация по элементам действий или элементам управления не приводит к согласованию правильных результатов.</span><span class="sxs-lookup"><span data-stu-id="3cf16-136">Filtering on Action Items or Controls does not consistently produce correct results.</span></span>

### <a name="templates"></a><span data-ttu-id="3cf16-137">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="3cf16-137">Templates</span></span>

- <span data-ttu-id="3cf16-138">Архивные шаблоны доступны для редактирования, и их нельзя редактировать.</span><span class="sxs-lookup"><span data-stu-id="3cf16-138">Archived templates are editable and they should not be editable.</span></span>
- <span data-ttu-id="3cf16-139">Заблокированные шаблоны допускают создание оценки, если это не так.</span><span class="sxs-lookup"><span data-stu-id="3cf16-139">Locked templates allow for Assessment creation when they should not.</span></span> <span data-ttu-id="3cf16-140">Блокировка шаблона заключается в том, чтобы он не использовался для создания оценок.</span><span class="sxs-lookup"><span data-stu-id="3cf16-140">Locking a Template is meant to prevent it from being used to create Assessments.</span></span>

### <a name="export"></a><span data-ttu-id="3cf16-141">Экспорт</span><span class="sxs-lookup"><span data-stu-id="3cf16-141">Export</span></span>

- <span data-ttu-id="3cf16-142">Экспорт шаблона в JSON завершается с ошибкой, если состояние шаблона \*\*\*\* — "импортировано" или " **ожидающее утверждение**".</span><span class="sxs-lookup"><span data-stu-id="3cf16-142">Template export to JSON fails when the template status is set to **Imported** or **Pending Approval**.</span></span>

### <a name="supported-browsers"></a><span data-ttu-id="3cf16-143">Поддерживаемые браузеры</span><span class="sxs-lookup"><span data-stu-id="3cf16-143">Supported browsers</span></span>

- <span data-ttu-id="3cf16-144">Поддерживаются последние версии Microsoft EDGE, Chrome и Safari.</span><span class="sxs-lookup"><span data-stu-id="3cf16-144">The latest versions of Microsoft Edge, Chrome, and Safari are supported.</span></span>
- <span data-ttu-id="3cf16-145">В некоторых случаях обновленные данные не отображаются, пока браузер не обновится.</span><span class="sxs-lookup"><span data-stu-id="3cf16-145">There may be instances where updated data does not appear until your browser is refreshed.</span></span>
- <span data-ttu-id="3cf16-146">Предварительная версия Microsoft EDGE не поддерживается, но не имеет известных проблем.</span><span class="sxs-lookup"><span data-stu-id="3cf16-146">The preview version of Microsoft Edge is not supported but has no known issues.</span></span>
- <span data-ttu-id="3cf16-147">Internet Explorer не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3cf16-147">Internet Explorer is not supported.</span></span>

### <a name="session-timeout"></a><span data-ttu-id="3cf16-148">Время ожидания сеанса</span><span class="sxs-lookup"><span data-stu-id="3cf16-148">Session timeout</span></span>

- <span data-ttu-id="3cf16-149">При истечении времени ожидания сеанса может появиться сообщение об ошибке "что-то пошло не так".</span><span class="sxs-lookup"><span data-stu-id="3cf16-149">When a session times out, a “Something went wrong” error may appear.</span></span> <span data-ttu-id="3cf16-150">Чтобы устранить проблему, перейдите к [диспетчеру соответствия требованиям](https://servicetrust.microsoft.com/ComplianceManager) и снова войдите в систему.</span><span class="sxs-lookup"><span data-stu-id="3cf16-150">To resolve, go to [Compliance Manager](https://servicetrust.microsoft.com/ComplianceManager) and log in again.</span></span>