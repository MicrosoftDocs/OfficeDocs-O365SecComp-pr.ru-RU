---
title: Использование общего доступа к аудит в журнале аудита Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Совместное использование — это ключевые действия в SharePoint Online и OneDrive для бизнеса. Администраторы могут теперь использовать общий доступ к аудит в журнале аудита Office 365 для определения, как общий доступ к используется в своей организации. '
ms.openlocfilehash: 511f8b0e61d450659d78177d5b87fac9ee636cd4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534957"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="ebf65-104">Использование общего доступа к аудит в журнале аудита Office 365</span><span class="sxs-lookup"><span data-stu-id="ebf65-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="ebf65-p102">Совместное использование — это ключевые действия в SharePoint Online и OneDrive для бизнеса и его широко используются в организациях Office 365. Администраторы могут теперь использовать общий доступ к аудит в журнале аудита Office 365 для определения, как общий доступ к используется в своей организации.</span><span class="sxs-lookup"><span data-stu-id="ebf65-p102">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations. Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="ebf65-107">Схема общего доступа к SharePoint</span><span class="sxs-lookup"><span data-stu-id="ebf65-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="ebf65-p103">Общего доступа (за исключением политики общего доступа и общего доступа к ссылки на события) событий, отличаются от события, связанные с файлов и папок в одной основной способ: один пользователь занимает действие, которое некоторые влияет на другого пользователя. Например пользователь A предоставляет доступ пользователю В в файл. В этом примере пользователь A *будет действовать пользователя* и пользователь B — *конечного пользователя*. В этой схеме файла SharePoint действие действующего пользователя влияет только на сам файл. Когда пользователь открывает файл, только информацию, необходимую для события **FileAccessed** является действующего пользователя. С учетом разницы, существует отдельный файл схемы, называется *схемы общего доступа к SharePoint*, собирает Дополнительные сведения об общем доступе к событиям. Это гарантирует, что администраторы имеют несколько понять, общих ресурсов и предоставлен пользовательского ресурса.</span><span class="sxs-lookup"><span data-stu-id="ebf65-p103">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user. For example, User A gives User B access to a file. In this example, User A is the  *acting user*  and User B is the  *target user*. In the SharePoint File schema, the acting user's action only affects the file itself. When User A opens a file, the only information needed in the **FileAccessed** event is the acting user. To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events. This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="ebf65-115">Схема общий доступ предоставляет два дополнительных полей в журнале аудита, относящиеся к совместному использованию событий:</span><span class="sxs-lookup"><span data-stu-id="ebf65-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="ebf65-116">**TargetUserOrGroupName** - Сохранение имени участника-пользователя или имя конечного пользователя или группы, что ресурс был предоставлен (пользователь В в предыдущем примере).</span><span class="sxs-lookup"><span data-stu-id="ebf65-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="ebf65-117">**TargetUserOrGroupType** - определяет, является ли конечного пользователя или группы члена, гостя, группы или партнера.</span><span class="sxs-lookup"><span data-stu-id="ebf65-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="ebf65-118">Эти два поля, в дополнение к другим свойства из Office 365 аудита схема журнала, например, пользователь, операция и Дата сообщить чтение о *какой* пользователь выделил *какие* ресурсов с помощью *которого* , а *Когда*.</span><span class="sxs-lookup"><span data-stu-id="ebf65-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="ebf65-p104">Есть другой свойства схемы, важных для общего доступа сценариев. Свойство **того** хранит дополнительную информацию об общем доступе к событиям. Например когда пользователь использует совместно сайта с другим пользователем, для этого, добавив конечного пользователя в группу SharePoint. Свойство **того** позволяет получить дополнительные сведения для предоставления контекста для администраторов.</span><span class="sxs-lookup"><span data-stu-id="ebf65-p104">There's another schema property that's important to the sharing story. The **EventData** property stores additional information about sharing events. For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group. The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="ebf65-123">Общий доступ к модели и общий доступ к событий SharePoint</span><span class="sxs-lookup"><span data-stu-id="ebf65-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="ebf65-p105">Общий доступ к фактически определенного три разных событий: **SharingSet**, **SharingInvitationCreated**и **SharingInvitaitonAccepted**. Ниже рабочий процесс для общего доступа как событий записываются в журнал аудита Office 365.</span><span class="sxs-lookup"><span data-stu-id="ebf65-p105">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**. Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Блок-схема работы общего доступа к аудит](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="ebf65-p106">Когда пользователь (действующего пользователя), где требуется реализовать общего ресурса с другим пользователем (конечного пользователя), SharePoint (или OneDrive для бизнеса) сначала проверяет, если адрес электронной почты пользователя, конечного уже связан с учетной записи пользователя в каталоге организации. Если конечный пользователь находится в каталоге организации, SharePoint делает следующее:</span><span class="sxs-lookup"><span data-stu-id="ebf65-p106">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory. If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="ebf65-129">Сразу же назначает разрешения конечного пользователя для доступа к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="ebf65-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="ebf65-130">Отправляет уведомление общего доступа на адрес электронной почты конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="ebf65-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="ebf65-131">Журналы событий **SharingSet** .</span><span class="sxs-lookup"><span data-stu-id="ebf65-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="ebf65-132">Если учетная запись пользователя для конечного пользователя не находится в каталоге организации, SharePoint делает следующее:</span><span class="sxs-lookup"><span data-stu-id="ebf65-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="ebf65-133">Создает приглашения на общий доступ и отправляет его на адрес электронной почты конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="ebf65-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="ebf65-134">Журналы событий **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="ebf65-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="ebf65-135">Событие **SharingInvitationCreated** наиболее всегда связан с внешним или гостя общего доступа к при конечного пользователя нет доступа к ресурс, к которому предоставлен общий доступ.</span><span class="sxs-lookup"><span data-stu-id="ebf65-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="ebf65-p107">Когда целевой пользователь принимает приглашение к совместному использованию, который отправил их (, щелкнув ссылку в приглашении, полученном), SharePoint журналы событий **SharingInvitationAccepted** и назначает разрешения конечного пользователя для доступа к ресурсу. Дополнительные сведения о пользователе конечного регистрируется, такие как идентификатор пользователя, которое было отправлено приглашение и пользователя, который фактически принял приглашение. В некоторых случаях может отличаться этих пользователей (или адреса электронной почты).</span><span class="sxs-lookup"><span data-stu-id="ebf65-p107">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource. Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation. In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="ebf65-139">Как определить ресурсы совместно с внешними пользователями</span><span class="sxs-lookup"><span data-stu-id="ebf65-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="ebf65-p108">Общие требования для администраторов создает список всех ресурсов, которые предоставлен пользователей за пределами организации. С помощью общего доступа к аудита в Office 365, администраторы могут приступить к созданию этого списка. Вот как.</span><span class="sxs-lookup"><span data-stu-id="ebf65-p108">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization. By using sharing auditing in Office 365, administrators can now generate this list. Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="ebf65-143">Шаг 1: Поиск общий доступ к событиям и экспортировать результаты в CSV-файл</span><span class="sxs-lookup"><span data-stu-id="ebf65-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="ebf65-p109">Первый шаг — это поиск в журнале аудита Office 365 для общего доступа к событиям. Дополнительные сведения (включая соответствующие разрешения) о поиске в журнал аудита, [Поиск в журнале аудита безопасности Office 365 &amp; центре соответствия требованиям](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="ebf65-p109">The first step is to search the Office 365 audit log for sharing events. For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="ebf65-146">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="ebf65-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="ebf65-147">Войдите в Office 365 с помощью учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="ebf65-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="ebf65-148">В левой области безопасности &amp; центре соответствия требованиям, нажмите кнопку **поиска &amp; расследования**и нажмите кнопку **Поиск журнала аудита**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-148">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation**, and then click **Audit log search**.</span></span>
    
    <span data-ttu-id="ebf65-149">Отображается страница **поиска журнала аудита** .</span><span class="sxs-lookup"><span data-stu-id="ebf65-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="ebf65-150">В области **действий**щелкните **действия общий доступ** для поиска только общий доступ к событиям.</span><span class="sxs-lookup"><span data-stu-id="ebf65-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![В разделе действия выберите действия общий доступ](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="ebf65-152">Выберите дату и время диапазона поиска общего доступа событий, которые произошли в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="ebf65-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="ebf65-153">Нажмите кнопку **поиска** , чтобы выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="ebf65-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="ebf65-154">После завершения поиска выполнение и результаты отображаются, нажмите кнопку **экспортировать результаты** \> **Загрузите все результаты**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="ebf65-155">Когда вы выберете параметр экспорта, в нижней части окна, предлагающее открыть или сохранить CSV-файла отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="ebf65-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="ebf65-156">Нажмите кнопку **Сохранить** \> **Сохранить как** и сохраните CSV-файл в папку на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ebf65-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="ebf65-157">Шаг 2: Фильтр в CSV-файле ресурсы совместно с внешними пользователями</span><span class="sxs-lookup"><span data-stu-id="ebf65-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="ebf65-p110">Следующим шагом является для фильтрации CSV для событий **SharingSet** и **SharingInvitationCreated** и для отображения событий, где свойство **TargetUserOrGroupType** — **гостя**. Для этого будет использовать функцию Power запроса в Excel. Следующая процедура выполняется в Excel 2016.</span><span class="sxs-lookup"><span data-stu-id="ebf65-p110">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**. You'll use the Power Query feature in Excel to do this. The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="ebf65-161">Откройте пустую книгу в Excel 2016.</span><span class="sxs-lookup"><span data-stu-id="ebf65-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="ebf65-162">Перейдите на вкладку **Данные**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="ebf65-163">Нажмите кнопку **Создать запрос** \> **из файла** \> **Из CSV**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![На вкладке Данные выберите создать запрос, выберите файл и затем выберите из CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="ebf65-165">Откройте CSV-файла, который был загружен на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="ebf65-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="ebf65-p111">CSV-файл открыт в редакторе запросов. Обратите внимание на то, что существует четыре столбца: **время**, **пользователь**, **Действие**и **сведений**. Столбец **данных** — это поле многозначного свойства. Следующим шагом является создание нового столбца для каждого свойства в столбце **подробностями** .</span><span class="sxs-lookup"><span data-stu-id="ebf65-p111">The CSV file is opened in the Query Editor. Note that there are four columns: **Time**, **User**, **Action**, and **Detail**. The **Detail** column is a multi-property field. The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="ebf65-170">Выберите в столбце **сведений о** и затем на вкладке **Главная** щелкните **Столбец с разделением** \> **С разделителем**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![На вкладке Главная щелкните столбец с разделением и нажмите кнопку с разделителем](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="ebf65-172">В окне **Столбец с разделением разделителем** выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ebf65-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="ebf65-173">В разделе **Выберите или введите разделитель**выберите **их запятыми**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="ebf65-174">В разделе **Split**выберите **при каждом возникновении разделителя**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="ebf65-175">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-175">Click **OK**.</span></span>
    
    <span data-ttu-id="ebf65-p112">В столбце **сведений о** делится на несколько столбцов. Каждый новый столбец называется **Detail.1**, **Detail.2**, **Detail.3**и т. д. Можно заметить, что значения в каждой ячейки в столбцах **Detail.n** начинаются с именем свойства; например **Операция: SharingSet**, **Операции: SharingInvitationAccepted**и **Операции: SharingInvitationCreated**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-p112">The **Detail** column is split into multiple columns. Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on. You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![В столбце сведений о разбивается на несколько столбцов, другая — для каждого свойства](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="ebf65-180">На вкладке **файл** нажмите кнопку **Закрыть &amp; нагрузки** чтобы закрыть редактор запросов и откройте файл в книге Excel.</span><span class="sxs-lookup"><span data-stu-id="ebf65-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="ebf65-181">Следующим шагом является для фильтрации файлов для отображения только события **SharingSet** и **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="ebf65-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="ebf65-182">Перейдите на вкладку **Главная** и выберите в столбце **Действие** .</span><span class="sxs-lookup"><span data-stu-id="ebf65-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="ebf65-183">В **сортировки &amp; фильтра** раскрывающегося списка, снимите все флажки, затем выберите **SharingSet** и **SharingInvitationCreated**и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="ebf65-184">Excel отображает строки для событий **SharingSet** и **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="ebf65-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="ebf65-185">Перейдите к столбцу с именем **Detail.17** (или независимо от выбранного столбца содержит свойство **TargetUserOrGroupType** ), а затем выберите ее.</span><span class="sxs-lookup"><span data-stu-id="ebf65-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="ebf65-186">В **сортировки &amp; фильтра** раскрывающегося списка, снимите все флажки, затем выберите **TargetUserOrGroupType:Guest**и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="ebf65-187">Теперь Excel отображает строк для события **SharingInvitationCreated** и **SharingSet** и где конечного пользователя не из вашей организации, так как внешние пользователи идентифицируются по значению **TargetUserOrGroupType:Guest**.</span><span class="sxs-lookup"><span data-stu-id="ebf65-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="ebf65-188">В следующей таблице показаны все пользователи в организации, который общих ресурсов с Гость в указанный диапазон дат.</span><span class="sxs-lookup"><span data-stu-id="ebf65-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Журнал аудита событий общего доступа в Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="ebf65-190">Несмотря на то, что не входит в предыдущей таблице, в столбце **Detail.10** (или независимо от выбранного столбца содержит свойство **ObjectId** ) идентифицирует ресурс, который был открыт для конечного пользователя. например `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="ebf65-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="ebf65-191">Если вы хотите определить при гостевой фактически назначения пользователю разрешения на доступ к ресурсу (а не только к ресурсам, которые совместно с ними), повторите шаги 10, 11 и 12 и фильтрации на **SharingInvitationAccepted** и **SharingSet **события в шаге 10.</span><span class="sxs-lookup"><span data-stu-id="ebf65-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
