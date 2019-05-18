---
title: Диспетчер соответствия требованиям (Майкрософт) и GDPR
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Диспетчер соответствия требованиям Майкрософт — бесплатное средство оценки рисков на основе рабочих процессов на портале доверия службы Майкрософт. Диспетчер соответствия требованиям позволяет отслеживать, назначать и проверять нормативные действия, связанные с облачными службами Майкрософт.
ms.openlocfilehash: a082d069aced13aa9260a1a856d942c4feb7dd4b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152101"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a><span data-ttu-id="d6c91-104">Диспетчер соответствия требованиям (Майкрософт) и GDPR</span><span class="sxs-lookup"><span data-stu-id="d6c91-104">Microsoft Compliance Manager and the GDPR</span></span>

<span data-ttu-id="d6c91-105">Общие требования к защите данных (GDPR), включенные в Европейский союз, могут повлиять на стратегию соответствия требованиям и выполнять действия, необходимые для управления сведениями о пользователях и клиентах, используемых в диспетчере соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d6c91-105">The General Data Protection Regulation (GDPR) enacted by the European Union can impact your compliance strategy and mandate actions needed to manage user and customer information used in Compliance Manager.</span></span>

## <a name="user-privacy-settings"></a><span data-ttu-id="d6c91-106">Параметры конфиденциальности пользователей</span><span class="sxs-lookup"><span data-stu-id="d6c91-106">User Privacy settings</span></span>

<span data-ttu-id="d6c91-107">Для определенных нормативных требований необходимо, чтобы Организация могла удалять данные журнала пользователей.</span><span class="sxs-lookup"><span data-stu-id="d6c91-107">Certain regulations require that an organization must be able to delete user history data.</span></span> <span data-ttu-id="d6c91-108">Диспетчер соответствия требованиям предоставляет функции **параметров конфиденциальности пользователей** , позволяющие администраторам выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d6c91-108">Compliance Manager provides **User Privacy Settings** functions that allow administrators to:</span></span>
  
- [<span data-ttu-id="d6c91-109">искать пользователей;</span><span class="sxs-lookup"><span data-stu-id="d6c91-109">Search for a user</span></span>](#search-for-a-user)
- [<span data-ttu-id="d6c91-110">экспортировать отчет о журнале данных учетных записей;</span><span class="sxs-lookup"><span data-stu-id="d6c91-110">Export a report of account data history</span></span>](#export-a-report-of-account-data-history)
- [<span data-ttu-id="d6c91-111">удалять журналы данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="d6c91-111">Delete user data history</span></span>](#delete-user-data-history)
  
## <a name="search-for-a-user"></a><span data-ttu-id="d6c91-112">Поиск пользователя</span><span class="sxs-lookup"><span data-stu-id="d6c91-112">Search for a user</span></span>

<span data-ttu-id="d6c91-113">Чтобы найти учетную запись, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d6c91-113">To search for a user account:</span></span>
  
1. <span data-ttu-id="d6c91-114">Введите псевдоним электронной почты пользователя (сведения слева от символа @) и выберите имя домена в списке суффикс домена справа.</span><span class="sxs-lookup"><span data-stu-id="d6c91-114">Enter the user email alias (the information to the left of the @ symbol) and choose the domain name from the  domain suffix list on the right.</span></span> <span data-ttu-id="d6c91-115">Для организаций с несколькими зарегистрированными доменами дважды проверьте суффикс доменных имен, чтобы убедиться в их правильности.</span><span class="sxs-lookup"><span data-stu-id="d6c91-115">For organizations with multiple registered domains, double check the domain name suffix to ensure that it is correct.</span></span>

2. <span data-ttu-id="d6c91-116">Когда введено правильное имя пользователя, выберите **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="d6c91-116">When you have the username correctly entered, select **Search**.</span></span>

3. <span data-ttu-id="d6c91-117">Для того чтобы учетные записи пользователей не возвращались, на странице отображается элемент "пользователь не найден".</span><span class="sxs-lookup"><span data-stu-id="d6c91-117">For user accounts not returned, 'User not found' is displayed on the page.</span></span> <span data-ttu-id="d6c91-118">Проверьте сведения об адресе электронной почты пользователя и внесите необходимые исправления.</span><span class="sxs-lookup"><span data-stu-id="d6c91-118">Check the user's email address information and make corrections as necessary.</span></span> <span data-ttu-id="d6c91-119">Чтобы повторить попытку, нажмите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="d6c91-119">To retry, select **Search**.</span></span>

4. <span data-ttu-id="d6c91-120">Для возвращенных учетных записей пользователей текст кнопки меняется с " **Поиск** " на " **очистить**".</span><span class="sxs-lookup"><span data-stu-id="d6c91-120">For user accounts returned, the text of the button changes from **Search** to **Clear**.</span></span> <span data-ttu-id="d6c91-121">Это означает, что Возвращенная учетная запись пользователя является рабочим контекстом для дополнительных функций, и эти функции применяются к этой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="d6c91-121">This indicates that the returned user account is the operating context for the additional functions and that these functions apply to this user account.</span></span>

5. <span data-ttu-id="d6c91-122">Чтобы очистить результаты поиска и выполнить поиск другого пользователя, нажмите кнопку **очистить**.</span><span class="sxs-lookup"><span data-stu-id="d6c91-122">To clear search results and search for a different user, select **Clear**.</span></span>

## <a name="export-a-report-of-account-data-history"></a><span data-ttu-id="d6c91-123">Экспорт отчета о журнале данных учетной записи</span><span class="sxs-lookup"><span data-stu-id="d6c91-123">Export a report of account data history</span></span>

<span data-ttu-id="d6c91-124">Для каждой определенной учетной записи пользователя можно создать отчет о зависимостях, связанных с этой учетной записью.</span><span class="sxs-lookup"><span data-stu-id="d6c91-124">For each user account identified, you can generate a report of dependencies linked to this account.</span></span> <span data-ttu-id="d6c91-125">Эта информация позволяет переназначить открытые элементы действий или обеспечить доступ к ранее загруженным доказательствам.</span><span class="sxs-lookup"><span data-stu-id="d6c91-125">This information allows you to reassign open Action Items or ensure access to previously uploaded evidence.</span></span>
  
 <span data-ttu-id="d6c91-126">Чтобы создать и экспортировать отчет, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d6c91-126">To generate and export a report:</span></span>
  
1. <span data-ttu-id="d6c91-127">Выберите пункт **Экспорт** , чтобы создать и скачать отчет о элементах действий управления диспетчера соответствия требованиям, назначенных для возвращенной учетной записи пользователя, и список документов, отправленных этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="d6c91-127">Select **Export** to generate and download a report of the Compliance Manager control Action Items currently assigned to the returned user account, and the list of documents uploaded by that user.</span></span> <span data-ttu-id="d6c91-128">Если нет назначенных действий или отправленных документов, в сообщении об ошибке указывается "нет данных для этого пользователя".</span><span class="sxs-lookup"><span data-stu-id="d6c91-128">If there are no assigned actions or uploaded documents, an error message states "No data for this user".</span></span>

2. <span data-ttu-id="d6c91-129">Отчет загружается в фоновом окне активного браузера, если вы не видите всплывающее окно загрузки, которое вы хотите проверить в журнале скачивания браузера.</span><span class="sxs-lookup"><span data-stu-id="d6c91-129">The report downloads in the background of the active browser window — if you don't see a download popup that you want to check your browser download history.</span></span>

3. <span data-ttu-id="d6c91-130">Откройте документ, чтобы просмотреть данные отчета.</span><span class="sxs-lookup"><span data-stu-id="d6c91-130">Open the document to review the report data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6c91-131">Это не исторический отчет, который сохраняет и отображает изменения состояния журнала назначения элементов действий.</span><span class="sxs-lookup"><span data-stu-id="d6c91-131">This is not a historical report that retains and displays state changes to Action Item assignment history.</span></span> <span data-ttu-id="d6c91-132">Созданный отчет — это снимок элементов управления, назначенных во время запуска отчета (Дата и отметка времени, записанные в отчет).</span><span class="sxs-lookup"><span data-stu-id="d6c91-132">The generated report is a snapshot of the control Action Items assigned at the time that the report is run (date and time stamp written into the report).</span></span> <span data-ttu-id="d6c91-133">Например, при повторном создании этого отчета для того же пользователя все последующие Переназначенные элементы действия приводят к различным данным отчета о моментальных снимках.</span><span class="sxs-lookup"><span data-stu-id="d6c91-133">For example, any subsequent reassignment of Action Items result in different snapshot report data if this report is generated again for the same user.</span></span>
  
## <a name="delete-user-data-history"></a><span data-ttu-id="d6c91-134">Удаление журнала данных пользователя</span><span class="sxs-lookup"><span data-stu-id="d6c91-134">Delete user data history</span></span>

<span data-ttu-id="d6c91-135">Задает для всех элементов управления, назначенных для возвращенного пользователя, значение "не назначено".</span><span class="sxs-lookup"><span data-stu-id="d6c91-135">Sets all control Action Items assigned to the returned user to 'unassigned'.</span></span> <span data-ttu-id="d6c91-136">Задает значение, переданное **по** значению для всех документов, отправленных возвращенным пользователем, в папку "пользователь удален".</span><span class="sxs-lookup"><span data-stu-id="d6c91-136">Sets the **uploaded by** value for any documents uploaded by the returned user to 'user removed'.</span></span>
  
<span data-ttu-id="d6c91-137">Удаление элемента действия учетной записи пользователя и журнала отправки документов:</span><span class="sxs-lookup"><span data-stu-id="d6c91-137">To delete the user account Action Item and document upload history:</span></span>
  
1. <span data-ttu-id="d6c91-138">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="d6c91-138">Select **Delete**.</span></span>

    <span data-ttu-id="d6c91-139">Откроется диалоговое окно подтверждения "*это приведет к удалению всех назначенных элементов действий управления и журнала отправки документов для выбранного пользователя. Это действие необратимо. Вы действительно хотите продолжить?*"</span><span class="sxs-lookup"><span data-stu-id="d6c91-139">A confirmation dialog is displayed, "*This removes all control Action Item assignments and the document upload history for the selected user. This action is permanent. Are you sure you want to continue?*"</span></span>

2. <span data-ttu-id="d6c91-140">Чтобы продолжить, нажмите кнопку **ОК**, в противном случае нажмите **кнопку Отмена**.</span><span class="sxs-lookup"><span data-stu-id="d6c91-140">To continue select **OK**, otherwise select **Cancel**.</span></span>