---
title: Аудит общего доступа с помощью журнала аудита Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Общий доступ является ключевым действием в SharePoint Online и OneDrive для бизнеса. Теперь администраторы могут использовать аудит общего доступа в журнале аудита Office 365, чтобы определить, как общий доступ используется в Организации. '
ms.openlocfilehash: 919592bff43379b552b83258c7b22b7eddb14e7a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219889"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="74e40-104">Аудит общего доступа с помощью журнала аудита Office 365</span><span class="sxs-lookup"><span data-stu-id="74e40-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="74e40-p102">Общий доступ является ключевым действием в SharePoint Online и OneDrive для бизнеса, который широко используется в организациях Office 365. Теперь администраторы могут использовать аудит общего доступа в журнале аудита Office 365, чтобы определить, как общий доступ используется в Организации.</span><span class="sxs-lookup"><span data-stu-id="74e40-p102">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations. Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="74e40-107">Схема общего доступа SharePoint</span><span class="sxs-lookup"><span data-stu-id="74e40-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="74e40-p103">События общего доступа (за исключением событий общего доступа и общего доступа к ним) отличаются от событий, связанных с файлами и папками, одним из основных способов: один пользователь предпринимает действия, которые влияют на другого пользователя. Например, пользователь А предоставляет пользователю Б доступ к файлу. В этом примере пользователь А является *действующим пользователем* , А пользователь б — конечным *пользователем*. В схеме файлов SharePoint действие действующего пользователя влияет только на сам файл. Когда пользователь А открывает файл, в событии **филеакцессед** требуются только сведения о действующем пользователе. Чтобы устранить это различие, существует отдельная схема, называемая схемой *общего доступа SharePoint*, которая захватывает дополнительные сведения о событиях общего доступа. Это позволяет администраторам получить более подробные сведения о том, кто предоставил общий доступ к ресурсу, а также к пользователю, к которому предоставлен общий доступ к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="74e40-p103">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user. For example, User A gives User B access to a file. In this example, User A is the  *acting user*  and User B is the  *target user*. In the SharePoint File schema, the acting user's action only affects the file itself. When User A opens a file, the only information needed in the **FileAccessed** event is the acting user. To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events. This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="74e40-115">Схема общего доступа предоставляет два дополнительных поля в журнале аудита, связанные с событиями общего доступа:</span><span class="sxs-lookup"><span data-stu-id="74e40-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="74e40-116">**Таржетусерорграупнаме** — хранит UPN или имя конечного пользователя или группы, к которым предоставлен общий доступ к ресурсу (пользователь б в предыдущем примере).</span><span class="sxs-lookup"><span data-stu-id="74e40-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="74e40-117">**Таржетусерорграуптипе** — указывает, является ли целевой пользователь или группа участником, гостем, группой или партнером.</span><span class="sxs-lookup"><span data-stu-id="74e40-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="74e40-118">Эти два поля в дополнение к другим свойствам схемы журнала аудита Office 365, например user, Operation и Date, могут сообщить полное описание *того* *, какой* пользователь предоставил ресурс, с *которым* и *когда*.</span><span class="sxs-lookup"><span data-stu-id="74e40-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="74e40-p104">Существует еще одно свойство схемы, которое важно для общего описания. Свойство **EVENTDATA** хранит дополнительные сведения о событиях общего доступа. Например, если пользователь предоставляет доступ к сайту другому пользователю, это достигается путем добавления конечного пользователя в группу SharePoint. Свойство **EVENTDATA** записывает эти дополнительные сведения для предоставления контекста администраторам.</span><span class="sxs-lookup"><span data-stu-id="74e40-p104">There's another schema property that's important to the sharing story. The **EventData** property stores additional information about sharing events. For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group. The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="74e40-123">Модель общего доступа и события общего доступа SharePoint</span><span class="sxs-lookup"><span data-stu-id="74e40-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="74e40-p105">В действительности общий доступ определяется тремя отдельными событиями \*\*\*\*: Sharing, **шарингинвитатионкреатед**и **шарингинвитаитонакцептед**. Ниже показан рабочий процесс, в котором регистрируются события общего доступа в журнале аудита Office 365.</span><span class="sxs-lookup"><span data-stu-id="74e40-p105">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**. Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Схема, в которой работает общий аудит](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="74e40-p106">Когда пользователь (действующий пользователь) хочет предоставить доступ к ресурсу другому пользователю (конечному пользователю), SharePoint (или OneDrive для бизнеса), сначала проверяется, связан ли адрес электронной почты конечного пользователя с учетной записью пользователя в каталоге Организации. Если целевой пользователь находится в каталоге Организации, SharePoint выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="74e40-p106">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory. If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="74e40-129">Немедленно назначает разрешения конечного пользователя на доступ к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="74e40-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="74e40-130">Отправляет уведомление о совместном доступе на адрес электронной почты целевого пользователя.</span><span class="sxs-lookup"><span data-stu-id="74e40-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="74e40-131">ЗаНосит в журнал событие **общего доступа** .</span><span class="sxs-lookup"><span data-stu-id="74e40-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="74e40-132">Если учетная запись пользователя конечного пользователя не находится в каталоге Организации, SharePoint выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="74e40-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="74e40-133">Создает приглашение для совместного доступа и отправляет его на адрес электронной почты конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="74e40-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="74e40-134">ЗаНосит в журнал событие **шарингинвитатионкреатед** .</span><span class="sxs-lookup"><span data-stu-id="74e40-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="74e40-135">Событие **шарингинвитатионкреатед** чаще всего связано с внешним или гостевым общим доступом, если целевой пользователь не имеет доступа к общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="74e40-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="74e40-p107">Когда целевой пользователь принимает приглашение к совместному использованию, отправленное им (щелкнув ссылку в приглашении), SharePoint заносит в журнал событие **шарингинвитатионакцептед** и назначает целевому пользователю разрешения на доступ к ресурсу. Кроме того, регистрируется дополнительная информация о целевом пользователе, например идентификатор пользователя, которому было отправлено приглашение, и пользователя, который действительно принял приглашение. В некоторых случаях эти пользователи (или адреса электронной почты) могут различаться.</span><span class="sxs-lookup"><span data-stu-id="74e40-p107">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource. Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation. In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="74e40-139">Как определить ресурсы, к которым предоставлен доступ внешним пользователям</span><span class="sxs-lookup"><span data-stu-id="74e40-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="74e40-p108">Для администраторов распространенным требованием является создание списка всех ресурсов, к которым предоставлен доступ пользователям за преданной Организацией. С помощью аудита общего доступа в Office 365 администраторы теперь могут создать этот список. Вот как это делать.</span><span class="sxs-lookup"><span data-stu-id="74e40-p108">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization. By using sharing auditing in Office 365, administrators can now generate this list. Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="74e40-143">Шаг 1: Поиск событий общего доступа и экспорт результатов в CSV-файл</span><span class="sxs-lookup"><span data-stu-id="74e40-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="74e40-p109">Первым шагом является поиск событий общего доступа в журнале аудита Office 365. Дополнительные сведения (в том числе необходимые разрешения), связанные с поиском в журнале аудита, можно найти в статье [Поиск в журнале &amp; аудита в центре безопасности и соответствия требованиям Office 365](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="74e40-p109">The first step is to search the Office 365 audit log for sharing events. For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="74e40-146">Перейдите по ссылке [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="74e40-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="74e40-147">Войдите в Office 365 с помощью своей рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="74e40-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="74e40-148">В левой области центра безопасности &amp; и соответствия требованиям выберите Поиск \*\* &amp; в расследовании\*\*, а затем щелкните **Поиск в журнале аудита**.</span><span class="sxs-lookup"><span data-stu-id="74e40-148">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation**, and then click **Audit log search**.</span></span>
    
    <span data-ttu-id="74e40-149">Отображается страница " **Поиск журнала аудита** ".</span><span class="sxs-lookup"><span data-stu-id="74e40-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="74e40-150">В разделе **действия**щелкните **действия общего доступа** , чтобы выполнить поиск только для событий общего доступа.</span><span class="sxs-lookup"><span data-stu-id="74e40-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![В разделе действия выберите действия общего доступа](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="74e40-152">Выберите диапазон дат и времени, чтобы найти события общего доступа, произошедшие в течение этого периода.</span><span class="sxs-lookup"><span data-stu-id="74e40-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="74e40-153">Нажмите кнопку **Поиск** , чтобы выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="74e40-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="74e40-154">После завершения поиска и отображения результатов нажмите кнопку **Экспорт результатов** \> **скачать все результаты**.</span><span class="sxs-lookup"><span data-stu-id="74e40-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="74e40-155">После выбора варианта экспорта в нижней части окна отобразится сообщение с предложением открыть или сохранить CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="74e40-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="74e40-156">Нажмите кнопку **сохранить** \> **Сохранить как** и сохраните CSV-файл в папке на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="74e40-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="74e40-157">Шаг 2: Фильтрация CSV-файла для ресурсов, к которым предоставлен доступ внешним пользователям</span><span class="sxs-lookup"><span data-stu-id="74e40-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="74e40-p110">Следующий шаг состоит в отфильтре CSV для событий **общего доступа** и **шарингинвитатионкреатед** , а также для отображения событий, для которых свойство **таржетусерорграуптипе** является " **гость**". Для этого используется функция Power Query в Excel. Следующая процедура выполняется в Excel 2016.</span><span class="sxs-lookup"><span data-stu-id="74e40-p110">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**. You'll use the Power Query feature in Excel to do this. The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="74e40-161">В Excel 2016 откройте пустую книгу.</span><span class="sxs-lookup"><span data-stu-id="74e40-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="74e40-162">Перейдите на вкладку **Данные**.</span><span class="sxs-lookup"><span data-stu-id="74e40-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="74e40-163">Выберите команду **создать запрос** \> **из файла** \> **из CSV**-файла.</span><span class="sxs-lookup"><span data-stu-id="74e40-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![На вкладке Данные выберите пункт Создать запрос, выберите из файла, а затем выберите из CSV-файла.](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="74e40-165">Откройте CSV-файл, скачанный в действии 1.</span><span class="sxs-lookup"><span data-stu-id="74e40-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="74e40-p111">CSV-файл открывается в редакторе запросов. Обратите внимание, что существует четыре столбца: **время**, **пользователь**, **действие**и **сведения**. Столбец **detail** является полем с несколькими свойствами. Следующий шаг — создание нового столбца для каждого свойства в столбце **Detail (сведения** ).</span><span class="sxs-lookup"><span data-stu-id="74e40-p111">The CSV file is opened in the Query Editor. Note that there are four columns: **Time**, **User**, **Action**, and **Detail**. The **Detail** column is a multi-property field. The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="74e40-170">Выберите столбец **сведения** , а затем на вкладке **Главная** нажмите кнопку **разделить столбец** \> **по разделителю**.</span><span class="sxs-lookup"><span data-stu-id="74e40-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![На вкладке Главная выберите команду разделить столбец, а затем щелкните разделитель](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="74e40-172">В окне **разделить столбец по разделителю** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="74e40-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="74e40-173">В разделе **Выбор и ввод разделителя**выберите **запятая**.</span><span class="sxs-lookup"><span data-stu-id="74e40-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="74e40-174">В разделе **разделить**выберите **при каждом возникновении разделителя**.</span><span class="sxs-lookup"><span data-stu-id="74e40-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="74e40-175">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74e40-175">Click **OK**.</span></span>
    
    <span data-ttu-id="74e40-p112">Столбец **detail** разделяется на несколько столбцов. Каждый новый столбец называется **detail. 1**, **detail. 2**, **detail. 3**и т. д. Вы заметите значения в каждой ячейке в столбцах **detail. n** с префиксом имя свойства; Например, **Operation: Sharing**, **Operation: шарингинвитатионакцептед**и **Operation: шарингинвитатионкреатед**.</span><span class="sxs-lookup"><span data-stu-id="74e40-p112">The **Detail** column is split into multiple columns. Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on. You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![Столбец Detail разделяется на несколько столбцов, по одному для каждого свойства.](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="74e40-180">На вкладке **файл** нажмите кнопку **Закрыть &amp; загрузку** , чтобы закрыть редактор запросов и открыть файл в книге Excel.</span><span class="sxs-lookup"><span data-stu-id="74e40-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="74e40-181">Следующий шаг состоит в том, чтобы отфильтровать файл, \*\*\*\* чтобы отображались только события Sharing и **шарингинвитатионкреатед** .</span><span class="sxs-lookup"><span data-stu-id="74e40-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="74e40-182">Перейдите на вкладку **Главная** и выберите столбец **Action (действие** ).</span><span class="sxs-lookup"><span data-stu-id="74e40-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="74e40-183">В раскрывающемся списке **фильтр &amp; сортировки** снимите все флажки, а затем выберите пункт **общий доступ** и **шарингинвитатионкреатед**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74e40-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="74e40-184">Excel отображает строки для событий **общего доступа** и **шарингинвитатионкреатед** .</span><span class="sxs-lookup"><span data-stu-id="74e40-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="74e40-185">Перейдите к столбцу с именем **detail. 17** (или к любому столбцу, содержащему свойство **таржетусерорграуптипе** ) и выберите его.</span><span class="sxs-lookup"><span data-stu-id="74e40-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="74e40-186">В раскрывающемся списке **Сортировка &amp; фильтра** снимите все флажки, затем выберите **таржетусерорграуптипе: гость**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="74e40-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="74e40-187">Теперь в Excel отображаются строки для событий **шарингинвитатионкреатед** и **общего доступа** , а целевой пользователь находится за пределами Организации, так как внешние пользователи определяются значением **таржетусерорграуптипе: гость**.</span><span class="sxs-lookup"><span data-stu-id="74e40-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="74e40-188">В приведенной ниже таблице показаны все пользователи в Организации, совместно использующих общие ресурсы с гостевым пользователем в указанном диапазоне дат.</span><span class="sxs-lookup"><span data-stu-id="74e40-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Общий доступ к событиям в журнале аудита Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="74e40-190">Несмотря на то, что он не включен в предыдущую таблицу, столбец **detail. 10** (или любой столбец содержит свойство **ObjectID** ) идентифицирует ресурс, к которому предоставлен доступ конечному пользователю; например `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`:.</span><span class="sxs-lookup"><span data-stu-id="74e40-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="74e40-191">Если вы хотите определить, когда гостевой пользователю фактически были назначены разрешения на доступ к ресурсу (а не только к ресурсам, в которых они совместно используются), повторите шаги 10, 11 и 12, а затем примените фильтр к **шарингинвитатионакцептед** и общему набору. \*\* \*\*события, которые находятся на шаге 10.</span><span class="sxs-lookup"><span data-stu-id="74e40-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
