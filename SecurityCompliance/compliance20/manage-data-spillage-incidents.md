---
title: Управление происшествиями spillage данных в Microsoft 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: В этой статье описываются с помощью новое средство расследований (Просмотр) данных в центре соответствия требованиям & безопасности Office 365 для управления происшествиями spillage данных.
ms.openlocfilehash: d7adc17d01a0ae2ad6b7bfb7052862a5a6419882
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706181"
---
# <a name="manage-a-data-spillage-incident-in-microsoft-365"></a><span data-ttu-id="f6ff4-103">Управление происшествиями spillage данных в Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f6ff4-103">Manage a data spillage incident in Microsoft 365</span></span> 

<span data-ttu-id="f6ff4-p101">Spillage данных при выпуске confidential документа в ненадежной среде. При обнаружении запроса технической spillage данных, важно быстро оценки размера и расположения spillage и проверить работу пользователей вокруг него окончательно удалить сброшенные данных из системы.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p101">Data spillage is when a confidential document is released into an untrusted environment. When a data spillage incident is detected, it's important to quickly assess the size and locations of the spillage, examine user activities around it, and then permanently purge the spilled data from the system.</span></span>

## <a name="scope-of-this-article"></a><span data-ttu-id="f6ff4-106">Области применения этой статьи</span><span class="sxs-lookup"><span data-stu-id="f6ff4-106">Scope of this article</span></span>

<span data-ttu-id="f6ff4-107">В этой статье представлен список инструкций по окончательное удаление элементов из почтовых ящиков Office 365, поэтому они больше не доступен или восстановить с помощью пользователей и администраторов.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-107">This article provides a list of instructions on how to permanently remove items from Office 365 mailboxes so they are no longer accessible or recoverable by users or admins.</span></span> 

> [!NOTE]
> <span data-ttu-id="f6ff4-108">При удалении элементов, размещенных в SharePoint или OneDrive для бизнеса сайта, их можно сохранить для 93 дней с момента удаления их из исходного расположения.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-108">When you delete items located in a SharePoint or OneDrive for Business site, they are retained for 93 days from the time you delete them from their original location.</span></span>

## <a name="scenario"></a><span data-ttu-id="f6ff4-109">Сценарий</span><span class="sxs-lookup"><span data-stu-id="f6ff4-109">Scenario</span></span>

<span data-ttu-id="f6ff4-p102">В случае проинформировать о происшествии spillage данных, где сотрудник непреднамеренно общих повышенной конфиденциальности документа с несколькими людьми по электронной почте. Вы хотите быстро оценить, полученных в этом документе, как внутри, так и вне организации. После после изучения происшествия, планируется совместное использование полученных результатов с другими следствие просмотрите и затем удалить без возможности восстановления сброшенные данных из Office 365. После завершения исследования, стоит ли удалить все свидетельства.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p102">You're informed of a data spillage incident where an employee unknowingly shared a highly-confidential document with multiple people through email. You want to quickly assess who received this document, both inside and outside of your organization. After you've investigate the incident, you plan to share your findings with other investigators to review, and then permanently remove the spilled data from Office 365. After the investigation is complete, you want to remove all evidence.</span></span> 

## <a name="workflow"></a><span data-ttu-id="f6ff4-114">Рабочий процесс</span><span class="sxs-lookup"><span data-stu-id="f6ff4-114">Workflow</span></span>

<span data-ttu-id="f6ff4-115">Ниже приведен рабочего процесса по управлению запроса технической spillage данных с помощью исследования данных (Просмотр).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-115">Here's the workflow for using Data Investigations (Preview) to manage a data spillage incident:</span></span>

1.  <span data-ttu-id="f6ff4-116">Создайте исследования данных.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-116">Create a data investigation.</span></span>

2.  <span data-ttu-id="f6ff4-117">Поиск сброшенные данных.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-117">Search for the spilled data.</span></span>

3.  <span data-ttu-id="f6ff4-118">Просмотрите и проверьте происшествия.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-118">Review and investigate the incident.</span></span>

4.  <span data-ttu-id="f6ff4-119">Окончательно удалите сброшенные данных.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-119">Permanently delete the spilled data.</span></span>

5.  <span data-ttu-id="f6ff4-120">Закрытие и удаление расследования.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-120">Close or delete the investigation.</span></span>


## <a name="before-you-begin"></a><span data-ttu-id="f6ff4-121">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="f6ff4-121">Before you begin</span></span>

- <span data-ttu-id="f6ff4-p103">Используется средство исследования данных (Предварительная версия) в центре соответствия требованиям & безопасности Office 365 для создания расследования, поиск сброшенные данных и просмотрите и их анализа. Затем используется & безопасности PowerShell центр соответствия удалить сброшенные данных с Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p103">You'll use the Data Investigations (Preview) tool in the Office 365 Security & Compliance Center to create an investigation, search for the spilled data, and review and analyze it. Then you'll use Security & Compliance Center PowerShell to permanently delete the spilled data from Office 365.</span></span> 

- <span data-ttu-id="f6ff4-124">Чтобы создать расследование, необходимо быть участником группы ролей администратора соответствия требованиям в центре соответствия требованиям & безопасности.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-124">To create an investigation, you have to be a member of the Compliance Administrator role group in the Security & Compliance Center.</span></span>

- <span data-ttu-id="f6ff4-p104">Чтобы удалить сообщения, необходимо быть участником группы ролей управления организацией в центре соответствия требованиям & безопасности или назначить роль поиска и очистки. Сведения о добавлении пользователей в группу ролей [Предоставьте пользователям доступ к безопасности & центре соответствия требованиям](../grant-access-to-the-security-and-compliance-center.md)см.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p104">To delete messages, you have to be a member of the Organization Management role group in the Security & Compliance Center or be assigned the Search and Purge role. For information about adding users to a role group, see [Give users access to the Security & Compliance Center](../grant-access-to-the-security-and-compliance-center.md).</span></span> 

- <span data-ttu-id="f6ff4-p105">Чтобы контролировать, какие почтовые ящики пользователей и учетных записей OneDrive человек может выполнять поиск, вашей организации можно задать границы соответствия требованиям. Дополнительные сведения, [установке границ соответствия требованиям для исследования обнаружения электронных данных](../set-up-compliance-boundaries.md).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p105">To control which user mailboxes and OneDrive accounts an investigator can search, your organization can set up compliance boundaries. For more information, [Set up compliance boundaries for eDiscovery investigations](../set-up-compliance-boundaries.md).</span></span> 

## <a name="step-1-create-a-data-investigation"></a><span data-ttu-id="f6ff4-129">Шаг 1: Создание исследования данных</span><span class="sxs-lookup"><span data-stu-id="f6ff4-129">Step 1: Create a data investigation</span></span>

<span data-ttu-id="f6ff4-130">Чтобы создать исследования данных:</span><span class="sxs-lookup"><span data-stu-id="f6ff4-130">To create a data investigation:</span></span>

1. <span data-ttu-id="f6ff4-131">Перейдите по ссылке [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-131">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="f6ff4-132">Войдите в Office 365 с помощью своей рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-132">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="f6ff4-133">В центре соответствия требованиям & безопасности нажмите кнопку **Исследования данных**.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-133">In the Security & Compliance Center, click **Data Investigations**.</span></span>
 
4. <span data-ttu-id="f6ff4-134">На странице **Данные расследований (Предварительная версия)** нажмите кнопку **Создать новый расследования**.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-134">On the **Data Investigations (Preview)** page, click **Create a new investigation**.</span></span>
    
5. <span data-ttu-id="f6ff4-p106">На странице " **новый исследования данных** всплывающее окно" Предоставление расследования name (обязательный) и введите номер необязательно расследования и описание. Обратите внимание на то, что имя должно быть уникальным в пределах организации.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p106">On the **New data investigation** flyout page, give the investigation a name (required), and then type an optional investigation number and description. Note that the name must be unique in your organization.</span></span>

6. <span data-ttu-id="f6ff4-137">В разделе **вы хотите настроить дополнительные параметры после создания исследование?**, выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="f6ff4-137">Under **Do you want to configure additional settings after creating this investigation?**, do one of the following:</span></span>

    - <span data-ttu-id="f6ff4-p107">Нажмите кнопку **Да,** Чтобы создать расследования и отображение страницы " **Параметры** " в новое обращение. Это позволяет добавить элементы для расследования.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p107">Click **Yes** to create the investigation, and display the **Settings** page in the new case. This allows you to add members to the investigation.</span></span>
    
    - <span data-ttu-id="f6ff4-p108">Нажмите кнопку **Нет** , чтобы только что создание расследования и отображение их в список случаев на странице **Данные расследований (Просмотр)** . Если выбран этот параметр, как будут использоваться только члена расследования и параметры по умолчанию аналитические данные и поиска добавлена. Вы можете добавить элементы или изменить параметры в любое время после создания расследования.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p108">Click **No** to just create the investigation and display it in the list of cases on the **Data Investigations (Preview)** page. If you choose this option, you will be added as the only member of the investigation and the default search and analytics settings will be used. You can add members or change settings any time after the investigation is created.</span></span>

7. <span data-ttu-id="f6ff4-143">Нажмите кнопку **Сохранить** , чтобы создать расследования.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-143">Click **Save** to create the investigation.</span></span>

    <span data-ttu-id="f6ff4-144">Новые расследования отображается в списке на странице **Данные расследований (Просмотр)** .</span><span class="sxs-lookup"><span data-stu-id="f6ff4-144">The new investigation is displayed in the list on the **Data Investigations (Preview)** page.</span></span> 

8. <span data-ttu-id="f6ff4-145">Чтобы открыть расследования, щелкните имя расследования.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-145">To open an investigation, click the name of the investigation.</span></span> 

    <span data-ttu-id="f6ff4-146">Отображается вкладка **Домашняя страница** для расследования.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-146">The **Home** tab for the investigation is displayed.</span></span> 

> [!TIP]
> <span data-ttu-id="f6ff4-147">Рекомендуется составить схему именования для исследования и сведения, как и в полях имя и описание, чтобы найти и ссылки в будущем при необходимости.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-147">Consider establishing a naming convention for investigations and provide as much information as you can in the name and description so you can locate and refer to in the future if necessary.</span></span>
 
## <a name="step-2-search-for-the-spilled-data"></a><span data-ttu-id="f6ff4-148">Шаг 2: Поиск сброшенные данных</span><span class="sxs-lookup"><span data-stu-id="f6ff4-148">Step 2: Search for the spilled data</span></span> 
 
<span data-ttu-id="f6ff4-p109">Если вы знаете пользователей, которым требуется выполнить поиск сброшенные данных, их можно добавить как людей интересов сопоставить их источники данных для исследования и быстро найти их почтовых ящиков и OneDrive учетной записи. Чтобы добавить людей представлять интерес для расследования, нажмите кнопку **людей интересов**и нажмите кнопку **Добавить людей интересов**.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p109">If you know which users you want to search for spilled data, you can add them as people of interest to map their data sources to the investigation and quickly search their mailbox and OneDrive account. To add people of interest to the investigation, click **People of interest**, and then click **Add people of interest**.</span></span> 

<span data-ttu-id="f6ff4-p110">На вкладке « **Поиск** » можно создать поиска для поиска сброшенные данных. Необходимо использовать тот же запрос поиска, который используется для поиска сброшенные данных, чтобы удалить эти же сообщения на [шаге 4](##step-4:-permanently-delete-the-spilled-data). Дополнительные сведения о создании операций поиска перейдите в раздел [Create поиска можно собирать данные](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p110">On the **Searches** tab, you can create searches to find the spilled data. You will use the same search query that you used to find the spilled data to delete those same messages in [Step 4](##step-4:-permanently-delete-the-spilled-data). For more information about creating searches, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="f6ff4-p111">После выполнения поиска можно выполнить предварительный просмотр примеров из результатов поиска и Просмотр статистики поиска в оценке эффективности запроса поиска. После определения элементов, которые необходимо удалить из Office 365 можно перейдите на вкладку **Происшествия** и затем создайте происшествие и добавьте результаты поиска, которые содержат эти элементы.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p111">After you run the search, you can preview samples of search results and view search statistics to evaluate the effectiveness of your search query. Once you identify the items that you want to delete from Office 365, you can click the **Incidents** tab, and then create an incident and add search results that contain those items.</span></span> 

<span data-ttu-id="f6ff4-p112">Для этого нажмите кнопку поиска, который необходимо рассмотреть. На странице "всплывающее окно" щелкните **Добавить результаты происшествия** и следуйте инструкциям. Затем можно просмотрите отдельных документов в происшествие, исследовать, которые имели доступ к документам и экспорт документов. Чтобы просто удалить документы вместо просмотра, перейдите к [шагу 4](##step-4:-permanently-delete-the-spilled-data).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p112">To do this, click the search that you want to investigate. On the flyout page, click **Add results to incident** and follow the instructions. Then in the incident, you can review individual documents, investigate who had access to documents, and export the documents. To simply delete the documents instead of reviewing them, go to [Step 4](##step-4:-permanently-delete-the-spilled-data).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="f6ff4-p113">Ключевые слова, используйте в запросе поиска может содержать сброшенные фактические данные, выполняя поиск. К примеру его поиск документов, содержащих номера социального страхования и можно использовать как ключевого слова в поисковый запрос, необходимо удалить запрос, затем для дальнейшей избежать spillage. Можно удалить поиска или удаление всей расследования на [шаге 5](##step-5:-close-or-delete-investigation).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p113">The keywords that you use in the search query may contain the actual spilled data that you're searching for. For example, if you searching for documents containing a social security number and you use it as a keyword in the search query, you must delete the query afterwards to avoid further spillage. You can delete search or delete the entire investigation in [Step 5](##step-5:-close-or-delete-investigation).</span></span> 

## <a name="step-3-review-and-investigate"></a><span data-ttu-id="f6ff4-163">Шаг 3: Просмотр и анализ</span><span class="sxs-lookup"><span data-stu-id="f6ff4-163">Step 3: Review and investigate</span></span> 

<span data-ttu-id="f6ff4-p114">В отношении которых ведется расследование перейдите на вкладку **Происшествия** и щелкните происшествия, созданной на предыдущем шаге. После завершения задания обработки и добавлены происшествия результатов поиска, можно просмотреть отдельных документов в их собственном формате, формат текста или рядом с собственном формате. Можно создать дополнительные запросы, чтобы сузить список документов и помечать документы, чтобы показать результаты из изучение.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p114">In the investigation, go to **Incidents** tab and click on the incident that you created in the previous step. After the processing job is completed and the search results are added to the incident, you can review individual documents in their native format, text format, or a near-native format. You can create additional queries to further narrow the list of documents, and tag documents to indicate findings from your investigation.</span></span>

<span data-ttu-id="f6ff4-p115">Чтобы получить дополнительные помощь для просмотра группирования документов, нажмите кнопку **Управление происшествиями**. Плитка **аналитики** щелкните **Анализ**. Будет запущен расширенных аналитических повторяющихся, threading электронной почты и анализа темы. Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p115">To group documents and get more assistance for your review, click **Manage incident**. In the **Analytics** tile, click **Analyze**. This will run advanced analytics such as duplicate detection, email threading, and theme analysis. For more information, see:</span></span>

- [<span data-ttu-id="f6ff4-171">Обнаружение схожих документов (почти дубликатов)</span><span class="sxs-lookup"><span data-stu-id="f6ff4-171">Near duplicate detection</span></span>](near-duplicates.md)
- [<span data-ttu-id="f6ff4-172">Потоки почты</span><span class="sxs-lookup"><span data-stu-id="f6ff4-172">Email threading</span></span>](email-threading.md)
- [<span data-ttu-id="f6ff4-173">Темы</span><span class="sxs-lookup"><span data-stu-id="f6ff4-173">Themes</span></span>](themes.md)

<span data-ttu-id="f6ff4-p116">Для определения пользователей, которые участвуют в spillage данных, можно создать новый запрос в происшествия и затем использовать отправителя/Author и условия получателей. Это создаст список всех отправителей, получателей и авторов, обнаруженных в собранные данные, который был добавлен происшествия. Обязательно проверьте список, чтобы определить наличие повторных внешних пользователей в списке. Для получения дополнительных сведений см [условиям поиска](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p116">To determine which users are involved in the data spillage, you can create a new query in the incident and then use the Sender/Author and Recipients conditions. This will create a list of all senders, recipients and authors found in collected data that was added to the incident. Be sure to examine the list to determine if there are any external users in the list. For more information, see [Search conditions](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>

## <a name="step-4-permanently-delete-the-spilled-data"></a><span data-ttu-id="f6ff4-178">Шаг 4: Окончательно удалить сброшенные данных</span><span class="sxs-lookup"><span data-stu-id="f6ff4-178">Step 4: Permanently delete the spilled data</span></span>

### <a name="deleting-mailbox-items"></a><span data-ttu-id="f6ff4-179">Удаление элементов почтового ящика</span><span class="sxs-lookup"><span data-stu-id="f6ff4-179">Deleting mailbox items</span></span>

<span data-ttu-id="f6ff4-p117">После просмотра и убедиться, что результаты поиска будут содержать только сообщения электронной почты, которые нужно удалить, можно окончательно удалить их, выполнив **New ComplianceSearchAction-очистить - PurgeType HardDelete** в & безопасности соответствия требованиям Центр PowerShell. Сведения содержатся в разделе [Поиск и удаление сообщений электронной почты](../search-for-and-delete-messages-in-your-organization.md).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p117">After you review and validate that the search results contain only the email messages that must be deleted, you can permanently delete them by running the **New-ComplianceSearchAction -Purge -PurgeType HardDelete** command in Security & Compliance Center PowerShell. For instructions, see [Search for and delete email messages](../search-for-and-delete-messages-in-your-organization.md).</span></span> 

<span data-ttu-id="f6ff4-p118">Обратите внимание, что если функцию восстановления отдельных элементов включена для почтовых ящиков в вашей организации без возможности восстановления удаленных элементов будет удержания в папки элементов для восстановления (и доступны для администраторов) до окончания периода хранения удаленных элементов (значение по умолчанию — 14 дней). Кроме того Если какие-либо почтовые ящики, которые содержат сброшенные данных юридических заблокированы или назначается политика хранения, удаленные сообщения будут храниться в папке элементов для восстановления, пока не будет снято удержание или почтовый ящик исключается из политики хранения. Для окончательного удаления сообщений немедленно, требуется для выполнения задач по добавлению. Сведения содержатся в разделе [Удалить элементы из папки облачные почтовые ящики на хранение элементов для восстановления ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p118">Note that if single item recovery is enabled for mailboxes in your organization, permanently deleted items will be retained in the user's Recoverable items folder (and accessible by admins) until the deleted item retention period ends (default is 14 days). Additionally, if any of the mailboxes that contain spilled data are on a legal hold or assigned to a retention policy, purged message will be retained in Recoverable items folder until the hold is removed or the mailbox is excluded from retention policies. To hard delete messages immediately, you need to perform addition tasks. For instructions, see [Delete items in the Recoverable Items folder of cloud-based mailboxes on hold ](../delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f6ff4-p119">Обратитесь к управлению записями или юридических отделов перед удалением политики удержания или хранения. У организации могут быть политики, которая определяет, будет ли почтовый ящик на хранение или приоритет запроса технической spillage данных.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p119">Check with your records management or legal departments before removing a hold or retention policy. Your organization may have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 

### <a name="deleting-site-items"></a><span data-ttu-id="f6ff4-188">Удаление элементов сайта</span><span class="sxs-lookup"><span data-stu-id="f6ff4-188">Deleting site items</span></span>

<span data-ttu-id="f6ff4-p120">Чтобы окончательно удалить документ с сайта SharePoint или OneDrive для бизнеса учетной записи, необходимо удалить ее и после этого необходимо удалить с сайта и затем удалите его из корзины семейства сайтов. Сведения содержатся в разделе [Удаление документов в SharePoint и OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p120">To permanently delete a document from a SharePoint site or OneDrive for Business account, you have to delete it and then you have to delete from the site and then delete it from the site collection Recycle Bin. For instructions, see [Delete documents in SharePoint and OneDrive](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#deleting-documents-in-sharepoint-online-and-onedrive-for-business).</span></span>

<span data-ttu-id="f6ff4-p121">Кроме того можно удалить все семейство сайтов, где может сброшенные данных. Сведения содержатся в разделе [Удаление семейства веб-сайтов](https://docs.microsoft.com/sharepoint/delete-site-collection).</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p121">Alternatively, you can delete an entire site collection that might contained spilled data. For instructions, see [Delete a site collection](https://docs.microsoft.com/sharepoint/delete-site-collection).</span></span>

## <a name="step-5-close-or-delete-the-investigation"></a><span data-ttu-id="f6ff4-193">Шаг 5: Закрытия или удаления исследования</span><span class="sxs-lookup"><span data-stu-id="f6ff4-193">Step 5: Close or delete the investigation</span></span>

<span data-ttu-id="f6ff4-p122">После удаления документов в расположения контента источника (почтовых ящиков или сайты) по-прежнему будут иметь копии этих документов, которые вы добавили в составе изучение происшествия. Чтобы избежать дальнейшей spillage данных, следует удалить расследования.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p122">After you delete documents in the source content locations (mailboxes or sites), you will still have copies of these documents that you added to incidents as part of your investigation. To avoid further data spillage, you should consider deleting the investigation.</span></span>

<span data-ttu-id="f6ff4-196">Чтобы удалить расследования:</span><span class="sxs-lookup"><span data-stu-id="f6ff4-196">To delete an investigation:</span></span>

1. <span data-ttu-id="f6ff4-197">На вкладке **настройки** нажмите кнопку **сведения расследования**.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-197">On the **Settings** tab, click **Investigation information**.</span></span>

2. <span data-ttu-id="f6ff4-198">Нажмите кнопку **Удалить case**.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-198">Click  **Delete case**.</span></span> 

<span data-ttu-id="f6ff4-p123">Если вам не нужно удалять расследования или если вы хотите сохранить сведения, собранные во время расследования, щелкните **Закрыть обращение**. В нужный момент может повторно открыть закрытый расследований.</span><span class="sxs-lookup"><span data-stu-id="f6ff4-p123">If you don't need to delete the investigation or if you want to save the information that you collected during the investigation, you can click **Close case**. At a later date, you can re-open closed investigations.</span></span>