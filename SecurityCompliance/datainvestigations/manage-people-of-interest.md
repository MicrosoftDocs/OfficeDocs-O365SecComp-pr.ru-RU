---
title: Управление интересными людьми при расследовании данных (Предварительная версия)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: e374509dccd235ef689609acc1c4f99db6594d4c
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150711"
---
# <a name="manage-people-of-interest-in-data-investigations-preview"></a><span data-ttu-id="03d52-102">Управление интересными людьми при расследовании данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="03d52-102">Manage people of interest in Data Investigations (Preview)</span></span>

<span data-ttu-id="03d52-103">При расследовании данных часто используются люди, представляющие интерес.</span><span class="sxs-lookup"><span data-stu-id="03d52-103">Data investigations often involve people of interest.</span></span> <span data-ttu-id="03d52-104">Обычно это люди, которые владеют неправильной, конфиденциальными или вредоносными данными, которые вы изучаете или ищете.</span><span class="sxs-lookup"><span data-stu-id="03d52-104">Usually they are people who own the misplaced, sensitive or malicious data that you're investigating or looking to remediate.</span></span> <span data-ttu-id="03d52-105">При **расследовании данных (Предварительная версия)** можно добавить их для обнаружения источников данных, чтобы использовать их в области поиска, или просмотреть дополнительные сведения, такие как контакты, расположение и журналы действий.</span><span class="sxs-lookup"><span data-stu-id="03d52-105">In **Data Investigations (Preview)**, you can add them to discover their data sources to use in scoping your search or view additional information such as contact, location and activity logs.</span></span> 


## <a name="add-people-of-interest"></a><span data-ttu-id="03d52-106">Добавление интересующих людей</span><span class="sxs-lookup"><span data-stu-id="03d52-106">Add people of interest</span></span>

<span data-ttu-id="03d52-107">На вкладке **люди по процентам** вы можете добавлять людей и находить свои источники данных, такие как почтовые ящики Exchange или сайт OneDrive для бизнеса, которые можно использовать для определения области поиска.</span><span class="sxs-lookup"><span data-stu-id="03d52-107">In **People of interest** tab, you can add people of interest and discover their data sources such as Exchange mailboxes or OneDrive for Business site that you can use to scope your search.</span></span> <span data-ttu-id="03d52-108">Если область ограничена интересующими пользователями, поиск является более производительным и точным, так как средство повторно обрабатывает любые неиндексированные данные, такие как изображения или неподдерживаемые типы файлов.</span><span class="sxs-lookup"><span data-stu-id="03d52-108">When scoped down by people of interest, searches are more performant and accurate because the tool re-processes any unindexed data such as images or unsupported file types.</span></span> <span data-ttu-id="03d52-109">Вы также можете просмотреть сведения о контакте, сведения о расположении и журналах активности, которые можно использовать для инициации связи или дальнейшего изучения их действий.</span><span class="sxs-lookup"><span data-stu-id="03d52-109">You can also see their contact information, location information and activity logs that you can use to initiate communications or further investigate their activities.</span></span> 

<span data-ttu-id="03d52-110">Чтобы добавить людей для расследования, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="03d52-110">To add people of interest to an investigation:</span></span>

1. <span data-ttu-id="03d52-111">На странице **расследования данных (Предварительная версия)** перейдите к вашему исследованию.</span><span class="sxs-lookup"><span data-stu-id="03d52-111">From the **Data Investigations (Preview)** page, go to your investigation.</span></span>
 
2. <span data-ttu-id="03d52-112">Выбрав нужное исследование, перейдите на вкладку **люди, представляющие интерес** , и нажмите кнопку **+ Добавить интересующих людей**.</span><span class="sxs-lookup"><span data-stu-id="03d52-112">After you have selected a investigation, go to the **People of interest** tab and click **+ Add people of interest**.</span></span> 
 
3. <span data-ttu-id="03d52-113">Выберите пользователей, которых вы хотите добавить к расследованию.</span><span class="sxs-lookup"><span data-stu-id="03d52-113">Choose people that you want to add to the investigation.</span></span> <span data-ttu-id="03d52-114">Для начала введите Поиск и выберите пользователей из Azure Active Directory вашей организации.</span><span class="sxs-lookup"><span data-stu-id="03d52-114">You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="03d52-115">После завершения работы со списком интересующих людей нажмите кнопку **Далее** , чтобы сопоставить источники данных.</span><span class="sxs-lookup"><span data-stu-id="03d52-115">After you have finalized the list of people of interest, click **Next** to map their data sources.</span></span> 

5. <span data-ttu-id="03d52-116">Необязательно Для каждого пользователя выберите **Exchange** , чтобы добавить основной почтовый ящик Exchange пользователя, и **OneDrive** , чтобы добавить основной сайт onedrive для бизнеса пользователя.</span><span class="sxs-lookup"><span data-stu-id="03d52-116">[Optional] For each person, select **Exchange** to add person's primary Exchange mailbox, and **OneDrive** to add person's primary OneDrive for Business site.</span></span>

6. <span data-ttu-id="03d52-117">Необязательно Нажмите кнопку **Далее** , чтобы добавить дополнительные источники данных, которые нужно связать с интересующими людьми.</span><span class="sxs-lookup"><span data-stu-id="03d52-117">[Optional] Click **Next** to add any additional data sources that you want to associate with your people of interest.</span></span>

7. <span data-ttu-id="03d52-118">Необязательно Выберите **Update (обновить** ), чтобы назначить расположение контента, например почтовые ящики, сайты и команды, для человека.</span><span class="sxs-lookup"><span data-stu-id="03d52-118">[Optional] Select **Update** to assign content locations, like mailboxes, sites, and Teams to a person.</span></span> 

8. <span data-ttu-id="03d52-119">Необязательно В всплывающем меню:</span><span class="sxs-lookup"><span data-stu-id="03d52-119">[Optional] In the flyout:</span></span>
   
    -  <span data-ttu-id="03d52-120">**Почтовые ящики Exchange** — выберите **Пользователи, группы или Teams** , а затем снова нажмите кнопку **выбрать пользователей, группы или Teams** .</span><span class="sxs-lookup"><span data-stu-id="03d52-120">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again.</span></span> <span data-ttu-id="03d52-121">Чтобы добавить дополнительные почтовые ящики, используйте поле поиска для поиска почтовых ящиков пользователей и групп рассылки.</span><span class="sxs-lookup"><span data-stu-id="03d52-121">To add more mailboxes, use the search box to find user mailboxes and distribution groups.</span></span> <span data-ttu-id="03d52-122">Вы также можете добавить почтовые ящики, используемые для хранения сведений о группе Office 365 или Microsoft Team.</span><span class="sxs-lookup"><span data-stu-id="03d52-122">You can also add mailboxes used to store an Office 365 Group or a Microsoft Team information.</span></span> <span data-ttu-id="03d52-123">Установите флажок Пользователь, группа, группа, нажмите кнопку **выбрать**, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="03d52-123">Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="03d52-124">При нажатии кнопки выбрать пользователей, группы или Teams для указания почтовых ящиков, отображается пустое средство выбора почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="03d52-124">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty.</span></span> <span data-ttu-id="03d52-125">Это вызвано мерами по повышению скорости работы.</span><span class="sxs-lookup"><span data-stu-id="03d52-125">This is by design to enhance performance.</span></span> <span data-ttu-id="03d52-126">Чтобы добавить пользователей в этот список, введите в поле поиска имя (не менее 3 символов).</span><span class="sxs-lookup"><span data-stu-id="03d52-126">To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
     - <span data-ttu-id="03d52-127">**Сайты SharePoint** — нажмите кнопку **выбрать сайты** , а затем нажмите кнопку **выбрать сайты** еще раз, чтобы указать сайты SharePoint и OneDrive для бизнеса, которые будут добавлены в подсети WWAN для пользователя.</span><span class="sxs-lookup"><span data-stu-id="03d52-127">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you wwant to add to a person.</span></span> <span data-ttu-id="03d52-128">Вы также можете добавить URL-адрес сайта SharePoint для группы Office 365 или группы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="03d52-128">You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="03d52-129">Введите URL-адрес для каждого сайта, который необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="03d52-129">Type the URL for each site that you want to assign.</span></span> <span data-ttu-id="03d52-130">Нажмите кнопку **выбрать**, а затем кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="03d52-130">Click **Choose**, and then click **Done**.</span></span>
     - <span data-ttu-id="03d52-131">**Microsoft** Teams — выберите команду **выбрать Teams** и снова нажмите кнопку **выбрать** Teams, чтобы просмотреть список групп Microsoft Teams, участником которых является данный сотрудник.</span><span class="sxs-lookup"><span data-stu-id="03d52-131">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the person is a member of today.</span></span> <span data-ttu-id="03d52-132">Выберите команды, которые вы хотите добавить для пользователя.</span><span class="sxs-lookup"><span data-stu-id="03d52-132">Select the Teams that you want to add to the person.</span></span> <span data-ttu-id="03d52-133">После выбора система автоматически определит _Амп_ выберите связанный сайт SharePoint и почтовые ящики групп, связанные с этой командой Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="03d52-133">Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team.</span></span> <span data-ttu-id="03d52-134">Нажмите кнопку **выбрать**, а затем кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="03d52-134">Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="03d52-135">Чтобы добавить дополнительные Microsoft Teams, вам потребуется отдельно добавить почтовый ящик и сайт SharePoint, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="03d52-135">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="03d52-136">После того как вы намерены сопоставление источников данных с интересующими пользователями, вы увидите сводку всех добавленных почтовых ящиков, сайтов и команд.</span><span class="sxs-lookup"><span data-stu-id="03d52-136">After you have finished mapping data sources to people of interest, you can see the summary of total mailboxes, sites, and Teams that you just added.</span></span> <span data-ttu-id="03d52-137">Если вы созначите какие-либо дополнительные источники данных для интересующих людей и выведете Поиск по интересующим людям, то сопоставление документа с интересующими пользователями не будет продолжено в течение расследования, что облегчит организацию доказательств или создание отчетов по интересующим людям. .</span><span class="sxs-lookup"><span data-stu-id="03d52-137">If you map any additional data sources to people of interest and scope your search by people of interest, the mapping of document to people of interest persist throughout the investigation, making it easier to organize evidence or generate report by people of interest.</span></span> 

## <a name="view-additional-people-of-interest-information"></a><span data-ttu-id="03d52-138">Просмотр дополнительных сведений о людях</span><span class="sxs-lookup"><span data-stu-id="03d52-138">View additional people of interest information</span></span>

<span data-ttu-id="03d52-139">На вкладке **люди процентов** щелкните человека, которого вы адиде.</span><span class="sxs-lookup"><span data-stu-id="03d52-139">In **People of interest** tab, click on a person that you adeed.</span></span> <span data-ttu-id="03d52-140">В всплывающем меню вы увидите следующее:</span><span class="sxs-lookup"><span data-stu-id="03d52-140">In a flyout, you'll see:</span></span>

- <span data-ttu-id="03d52-141">Контактные данные</span><span class="sxs-lookup"><span data-stu-id="03d52-141">Contact information</span></span>

  - <span data-ttu-id="03d52-142">**Отображаемое имя**: имя Перон, отображаемое в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="03d52-142">**Display Name**: The peron's name displayed in the address book.</span></span> <span data-ttu-id="03d52-143">Обычно это сочетание имени, инициала и фамилии.</span><span class="sxs-lookup"><span data-stu-id="03d52-143">This is usually the combination of first name, middle initial and last name.</span></span>
  - <span data-ttu-id="03d52-144">**Mail/SMTP**: SMTP-адрес пользователя, например Jeff@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="03d52-144">**Mail/SMTP**: The SMTP address of the person, for example, jeff@contoso.onmicrosoft.com.</span></span>  
  - <span data-ttu-id="03d52-145">**Заголовок**: должность.</span><span class="sxs-lookup"><span data-stu-id="03d52-145">**Title**: Job title.</span></span>
  - <span data-ttu-id="03d52-146">**Отдел**: имя отдела, в котором работает пользователь.</span><span class="sxs-lookup"><span data-stu-id="03d52-146">**Department**: The name of the department in which the person works.</span></span>
  - <span data-ttu-id="03d52-147">**Руководитель**: руководитель сотрудника.</span><span class="sxs-lookup"><span data-stu-id="03d52-147">**Manager**: The person's manager.</span></span> <span data-ttu-id="03d52-148">Manager получает сведения о эскалации для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="03d52-148">Manager receives any escalation communications for this person.</span></span>
  
- <span data-ttu-id="03d52-149">Сведения о расположении</span><span class="sxs-lookup"><span data-stu-id="03d52-149">Location information</span></span>

  - <span data-ttu-id="03d52-150">**City**: город, в котором находится пользователь.</span><span class="sxs-lookup"><span data-stu-id="03d52-150">**City**: The city in which the person is located.</span></span>
  - <span data-ttu-id="03d52-151">**State**: область или край, где находится пользователь.</span><span class="sxs-lookup"><span data-stu-id="03d52-151">**State**: The state or province in which the person is located.</span></span>
  - <span data-ttu-id="03d52-152">**Страна или регион**: страна или регион, где находится пользователь; Например, "US" или "Великобритания".</span><span class="sxs-lookup"><span data-stu-id="03d52-152">**Country/Region**: The country/region in which the person is located; for example, “US” or “UK”.</span></span>
  - <span data-ttu-id="03d52-153">**Office**: расположение офиса пользователя.</span><span class="sxs-lookup"><span data-stu-id="03d52-153">**Office**: The office location of the person.</span></span>

- <span data-ttu-id="03d52-154">Состояние обработки</span><span class="sxs-lookup"><span data-stu-id="03d52-154">Processing status</span></span>

  - <span data-ttu-id="03d52-155">**Состояние индексирования**: состояние глубокого индексирования источников данных</span><span class="sxs-lookup"><span data-stu-id="03d52-155">**Indexing status**: Status of deep indexing the data sources</span></span>
  - <span data-ttu-id="03d52-156">**Время последнего обновления индексации**: метка времени последнего запуска задания глубокого индексирования.</span><span class="sxs-lookup"><span data-stu-id="03d52-156">**Indexing Last Updated Time**: Timestamp of when the deep indexing job was last triggered.</span></span>
  - <span data-ttu-id="03d52-157">**Источники данных**: показывает количество почтовых ящиков, сайтов и команд, сопоставленных с пользователем.</span><span class="sxs-lookup"><span data-stu-id="03d52-157">**Data sources**: Shows the count of mailboxes, sites, and Teams mapped to the person</span></span>

- <span data-ttu-id="03d52-158">Обновление индекса</span><span class="sxs-lookup"><span data-stu-id="03d52-158">Update index</span></span>
    - <span data-ttu-id="03d52-159">Вы можете повторно индексировать источники данных этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="03d52-159">You can re-index this person's data sources.</span></span> 

- <span data-ttu-id="03d52-160">Просмотр действий</span><span class="sxs-lookup"><span data-stu-id="03d52-160">View activity</span></span> 

    - <span data-ttu-id="03d52-161">Вы можете просматривать журналы активности пользователя и искать их.</span><span class="sxs-lookup"><span data-stu-id="03d52-161">You can view and search user's activity logs.</span></span> <span data-ttu-id="03d52-162">Дополнительную информацию можно узнать в статье [Просмотр сведений о действиях](view-people-of-interest-activity.md) по интересам</span><span class="sxs-lookup"><span data-stu-id="03d52-162">For more information, see [View people of interest activity](view-people-of-interest-activity.md)</span></span> 
