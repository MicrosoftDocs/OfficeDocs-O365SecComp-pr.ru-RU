---
title: Просмотр custodian аудита активности
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
description: ''
ms.openlocfilehash: 8219ae8a061f6d08dd37da5b7f2974dd86c68f04
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608230"
---
# <a name="viewing-custodian-audit-activity"></a><span data-ttu-id="faa30-102">Просмотр custodian аудита активности</span><span class="sxs-lookup"><span data-stu-id="faa30-102">Viewing custodian audit activity</span></span>

<span data-ttu-id="faa30-p101">Требуется для поиска, если пользователь просматривать конкретного документа или очищены элемента из их почтовых ящиков? Расширенные обнаружения электронных данных (Просмотр) теперь интегрированы с существующей аудита журнала средства поиска в центре соответствия требованиям & безопасности. С помощью этой внедренных качества, можно использовать средство управления Custodian расширенной обнаружения электронных данных (Предварительная версия) для облегчения изучение, легко доступ к и найдите действие custodians в случае.</span><span class="sxs-lookup"><span data-stu-id="faa30-p101">Need to find if a user viewed a specific document or purged an item from their mailbox? Advanced eDiscovery (Preview) is now integrated with the existing audit log search tool in the Security & Compliance Center. Using this embedded experience, you can use the Advanced eDiscovery (Preview) Custodian Management tool to facilitate your investigation by easily accessing and searching the activity for custodians within your case.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="faa30-106">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="faa30-106">Before you begin</span></span>

<span data-ttu-id="faa30-p102">Вы должны быть назначены роли журналы аудита только для просмотра или журналов аудита в Exchange Online поиск в журнале аудита Office 365. По умолчанию эти роли назначенные Управление соответствием требованиям и группы ролей управления организацией на странице "разрешения" в центре администрирования Exchange. Чтобы предоставить пользователю возможность выполнять поиск в журнал аудита расширенной обнаружения электронных данных (Просмотр) с минимальным уровнем привилегий, можно создать пользовательскую группу ролей в Exchange Online, добавить роль журналы аудита только для просмотра или журналов аудита и нажмите Добавить пользователя в качестве нового группа роль должна быть членом згруппировать. Для получения дополнительных сведений см ролей в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="faa30-p102">You have to be assigned the View-Only Audit Logs or Audit Logs role in Exchange Online to search the Office 365 audit log. By default, these roles are assigned to the Compliance Management and Organization Management role groups on the Permissions page in the Exchange admin center. To give a user the ability to search the Advanced eDiscovery (Preview) audit log with the minimum level of privileges, you can create a custom role group in Exchange Online, add the View-Only Audit Logs or Audit Logs role, and then add the user as a member of the new role group. For more information, see Manage role groups in Exchange Online.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="faa30-p103">Если пользователь назначение роли журналы аудита только для просмотра или журналов аудита на странице "разрешения" в центре соответствия требованиям & безопасности, они будут поиск в журнале аудита Office 365. Необходимо назначить разрешения в Exchange Online. Это основной командлет используется для поиска по журналу аудита — это командлет командной Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="faa30-p103">If you assign a user the View-Only Audit Logs or Audit Logs role on the Permissions page in the Security & Compliance Center, they won't be able to search the Office 365 audit log. You have to assign the permissions in Exchange Online. This is because the underlying cmdlet used to search the audit log is an Exchange Online cmdlet.</span></span>

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a><span data-ttu-id="faa30-114">Шаг 1: Создание поискового запроса журнала аудита расширенной обнаружения электронных данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="faa30-114">Step 1: Create an Advanced eDiscovery (Preview) audit log search</span></span>

   1. <span data-ttu-id="faa30-115">Выберите существующий случай **безопасности & центре соответствия требованиям > расширенной обнаружения электронных данных (Просмотр)**.</span><span class="sxs-lookup"><span data-stu-id="faa30-115">Select an existing case from the **Security & Compliance Center > Advanced eDiscovery (Preview)**.</span></span>
   
   2. <span data-ttu-id="faa30-116">Перейдите на вкладку « **Custodians** » и выберите custodian.</span><span class="sxs-lookup"><span data-stu-id="faa30-116">Navigate to the **Custodians** tab and select a custodian.</span></span>
   
   3. <span data-ttu-id="faa30-117">Выбрав custodian, нажмите кнопку **Просмотр Custodian активности** в панели сведений.</span><span class="sxs-lookup"><span data-stu-id="faa30-117">Once you have selected a custodian, click **View Custodian Activity** from the details panel.</span></span>
   
   4. <span data-ttu-id="faa30-118">Настройте следующие условия поиска:</span><span class="sxs-lookup"><span data-stu-id="faa30-118">Configure the following search criteria:</span></span>
      
      <span data-ttu-id="faa30-p104">a. **мероприятий** - нажмите кнопку раскрывающегося списка для отображения действия, которые можно выполнить поиск. После запуска поиска отображаются только записи аудита для выбранного действия. Выбрав **Показать результаты для всех действий** будет отображаться результаты для всех действий, необходимых для других критериев поиска.</span><span class="sxs-lookup"><span data-stu-id="faa30-p104">a. **Activities** - Click the drop-down list to display the activities that you can search for. After you run the search, only the audit records for the selected activities are displayed. Selecting **Show results for all activities** will display results for all activities that meet the other search criteria.</span></span>
      
      <span data-ttu-id="faa30-p105">б. **Дата начала и Дата окончания** — выберите дату и время диапазона просмотра событий, возникших в течение этого периода. По умолчанию выбрано за последние семь дней. Дата и время представлены в формате по Гринвичу (UTC). Максимальный период, которые можно выбрать — один год.</span><span class="sxs-lookup"><span data-stu-id="faa30-p105">b. **Start date and End date** - Select a date and time range to display the events that occurred within that period. The last seven days are selected by default. The date and time are presented in Coordinated Universal Time (UTC) format. The maximum date range that you can specify is one year.</span></span>
      
      <span data-ttu-id="faa30-p106">c. **Custodians** - щелкните в этом поле выберите определенного custodian для отображения поиска по результатам. В списке результатов отображаются записи аудита для выбранной операции, выполненные для пользователей, выбранного в этом поле.</span><span class="sxs-lookup"><span data-stu-id="faa30-p106">c. **Custodians** - Click in this box and then select a specific custodian to display search results for. Audit records for the selected activity performed by the users you select in this box are displayed in the list of results.</span></span>
    
    1. <span data-ttu-id="faa30-p107">Нажмите кнопку **поиска** , чтобы запустить поиск, используя условия поиска. Результаты поиска загружаются и после некоторое время они отображаются в области результатов на странице поиска Custodian действий.</span><span class="sxs-lookup"><span data-stu-id="faa30-p107">Click **Search** to run the search using your search criteria. The search results are loaded, and after a few moments they are displayed under Results on the Custodian Activities search page.</span></span> 

## <a name="step-2-view-the-audit-log-search-results"></a><span data-ttu-id="faa30-133">Шаг 2: Просмотр результатов поиска журнала аудита</span><span class="sxs-lookup"><span data-stu-id="faa30-133">Step 2: View the audit log search results</span></span>

<span data-ttu-id="faa30-p108">Результаты поиска журнала аудита отображаются в области результатов на странице журнала аудита Custodian. Не более 5000 (самые новые) событий отображаются с шагом 150 событий. Чтобы отобразить дополнительные события можно использовать полосы прокрутки в области результатов или вы нажимаете клавишу Shift + End просмотра событий, затем 150.</span><span class="sxs-lookup"><span data-stu-id="faa30-p108">The results of an audit log search are displayed under Results on the Custodian Audit log page. A maximum of 5,000 (newest) events are displayed in increments of 150 events. To display more events you can use the scroll bar in the Results pane or you can press Shift + End to display the next 150 events.</span></span>

<span data-ttu-id="faa30-137">Результаты содержат следующие сведения о каждом событии, возвращенных в результате поиска.</span><span class="sxs-lookup"><span data-stu-id="faa30-137">The results contain the following information about each event returned by the search.</span></span>
- <span data-ttu-id="faa30-138">**Дата**: Дата и время (в формате UTC) при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="faa30-138">**Date**: The date and time (in UTC format) when the event occurred.</span></span>

- <span data-ttu-id="faa30-p109">**IP-адрес**: IP-адрес устройства, который использовался при входе действия. IP-адрес отображается в формате адреса IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="faa30-p109">**IP address**: The IP address of the device that was used when the activity was logged. The IP address is displayed in either an IPv4 or IPv6 address format.</span></span>

- <span data-ttu-id="faa30-141">**Пользователь**: пользователя (или учетная запись службы), выполнить действие, которое вызвало событие.</span><span class="sxs-lookup"><span data-stu-id="faa30-141">**User**: The user (or service account) who performed the action that triggered the event.</span></span>

- <span data-ttu-id="faa30-p110">**Действие**: операции, выполненные пользователем. Это значение соответствует действия, выбранные в раскрывающемся списке действия. Для события из журнала аудита действий администратора Exchange значение в этом столбце — это командлет Exchange.</span><span class="sxs-lookup"><span data-stu-id="faa30-p110">**Activity**: The activity performed by the user. This value corresponds to the activities that you selected in the Activities drop down list. For an event from the Exchange admin audit log, the value in this column is an Exchange cmdlet.</span></span>

- <span data-ttu-id="faa30-p111">**Элемент**: объектов, которые были созданы или изменены в результате соответствующих действий. Например файл, который был просматривать или изменять или учетная запись пользователя, который был обновлен. Не все действия иметь значение в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="faa30-p111">**Item**: The object that was created or modified as a result of the corresponding activity. For example, the file that was viewed or modified or the user account that was updated. Not all activities have a value in this column.</span></span>

- <span data-ttu-id="faa30-p112">**Подробности**: Дополнительная информация об активности. Еще раз не все действия будут иметь значение.</span><span class="sxs-lookup"><span data-stu-id="faa30-p112">**Detail**: Additional detail about an activity. Again, not all activities will have a value.</span></span>

## <a name="step-3-filter-the-search-results"></a><span data-ttu-id="faa30-150">Шаг 3: Фильтровать результаты поиска</span><span class="sxs-lookup"><span data-stu-id="faa30-150">Step 3: Filter the search results</span></span>

<span data-ttu-id="faa30-p113">В дополнение к сортировке, также можно отфильтровать результаты поиска журнала аудита. Это может помочь быстро фильтровать результаты для определенных пользователей или активности.</span><span class="sxs-lookup"><span data-stu-id="faa30-p113">In addition to sorting, you can also filter the results of an audit log search. This can help you quickly filter the results for a specific user or activity.</span></span> 

<span data-ttu-id="faa30-153">Для фильтрации результатов:</span><span class="sxs-lookup"><span data-stu-id="faa30-153">To filter the results:</span></span>

 1. <span data-ttu-id="faa30-154">Создание и выполнение поискового запроса журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="faa30-154">Create and run an audit log search.</span></span>
  
2. <span data-ttu-id="faa30-155">При отображении результатов, щелкните **фильтровать результаты**.</span><span class="sxs-lookup"><span data-stu-id="faa30-155">When the results are displayed, click **Filter results**.</span></span>
 
3. <span data-ttu-id="faa30-156">Ключевое слово полей отображаются под заголовком каждого столбца.</span><span class="sxs-lookup"><span data-stu-id="faa30-156">Keyword boxes are displayed under each column header.</span></span>
  
4. <span data-ttu-id="faa30-p114">Выберите один из поля в разделе заголовка столбца и введите слово или фразу, в зависимости от столбца, по которому выполняется фильтрация на. Результаты будут динамически перенастроить просмотра событий, которые соответствуют фильтра.</span><span class="sxs-lookup"><span data-stu-id="faa30-p114">Click one of the boxes under a column header and type a word or phrase, depending on the column you're filtering on. The results will dynamically readjust to display the events that match your filter.</span></span>
  
5. <span data-ttu-id="faa30-159">Чтобы очистить фильтр, нажмите кнопку **X** в поле фильтра или просто щелкните **Скрыть фильтрации**.</span><span class="sxs-lookup"><span data-stu-id="faa30-159">To clear a filter, click the **X** in the filter box or just click **Hide filtering**.</span></span>

## <a name="export-the-search-results-to-a-file"></a><span data-ttu-id="faa30-160">Экспорт результатов поиска в файл</span><span class="sxs-lookup"><span data-stu-id="faa30-160">Export the search results to a file</span></span>

<span data-ttu-id="faa30-p115">Результаты поиска журнала аудита можно экспортировать в файл значений, разделенных запятыми (CSV) запятой на локальном компьютере. Можно открыть этот файл в Microsoft Excel и использовать компонентов, таких как поиск, сортировка, фильтрация и Разделение одного столбца (, который содержит ячейки с несколькими значениями) в несколько столбцов.</span><span class="sxs-lookup"><span data-stu-id="faa30-p115">You can export the results of an audit log search to a comma separated value (CSV) file on your local computer. You can open this file in Microsoft Excel and use features such as search, sorting, filtering, and splitting a single column (that contains multi-value cells) into multiple columns.</span></span>

1. <span data-ttu-id="faa30-163">Запустить поиск журнала аудита и нажмите Изменить условия поиска, пока получите требуемых результатов.</span><span class="sxs-lookup"><span data-stu-id="faa30-163">Run an audit log search, and then revise the search criteria until you have the desired results.</span></span>
  
2. <span data-ttu-id="faa30-164">Нажмите кнопку Экспорт результатов и выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="faa30-164">Click Export results and select one of the following options:</span></span>

    - <span data-ttu-id="faa30-p116">**Сохранить загружены результатов:** Выберите этот параметр, чтобы экспортировать только записи, которые отображаются в области **результатов** на странице **поиска журнала аудита Custodian** . CSV-файл, который будет загружен содержит те же столбцы (и данные) отображается на странице (даты, пользователей, активность, элемента и подробные сведения). (Под названием **более**) дополнительный столбец включен в CSV-файл, содержащий дополнительные сведения из записи журнала аудита. Так как экспорте одинаковые результаты, которые загружаются (и для просмотра) на странице поиска журнала аудита экспортируются не более 5000 записей.</span><span class="sxs-lookup"><span data-stu-id="faa30-p116">**Save loaded results:** Choose this option to export only the entries that are displayed under **Results** on the **Custodian Audit log search** page. The CSV file that is downloaded contains the same columns (and data) displayed on the page (Date, User, Activity, Item, and Details). An additional column (titled **More**) is included in the CSV file that contains more information from the audit log entry. Because you're exporting the same results that are loaded (and viewable) on the Audit log search page, a maximum of 5,000 entries are exported.</span></span>
        
    - <span data-ttu-id="faa30-p117">**Загрузка всех результатов:** Выберите этот параметр, чтобы экспортировать все записи из журнала аудита Office 365, которые соответствуют условиям поиска. Для большого набора результатов поиска выберите этот параметр, чтобы загрузить все записи из журнала аудита в дополнение к 5000 результатов, которые могут быть отображены на странице поиска **журнала аудита Custodian** . Этот параметр, загрузите необработанные данные из журнала аудита в CSV-файл и содержит дополнительные сведения из журнала аудита записи в столбце с именем AuditData. Может потребоваться больше времени для загрузки файла, если выбран этот параметр экспорта, так как файл может быть значительно больше, если выбран параметр других загружается.</span><span class="sxs-lookup"><span data-stu-id="faa30-p117">**Download all results:** Choose this option to export all entries from the Office 365 audit log that meet the search criteria. For a large set of search results, choose this option to download all entries from the audit log in addition to the 5,000 results that can be displayed on the **Custodian Audit log** search page. This option will download the raw data from the audit log to a CSV file, and contains additional information from the audit log entry in a column named AuditData. It may take longer to download the file if you choose this export option because the file may be much larger than the one that's downloaded if you choose the other option.</span></span>
    
      > [!IMPORTANT]
      > <span data-ttu-id="faa30-p118">Не более 50 000 записей в CSV-файл можно загрузить из поиска журналов аудита единого. Если 50 000 записей загружаются в CSV-файл, вероятно, можно предположить, что более 50 000 событий, выполнены условия поиска. Чтобы экспортировать больше, чем это ограничение, попробуйте использовать диапазон дат для уменьшения количества записей журнала аудита. Может потребоваться использовать несколько поисков для работы с меньшего размера диапазона дат для экспорта более 50 000 записей.</span><span class="sxs-lookup"><span data-stu-id="faa30-p118">You can download a maximum of 50,000 entries to a CSV file from a single audit log search. If 50,000 entries are downloaded to the CSV file, you can probably assume there are more than 50,000 events that met the search criteria. To export more than this limit, try using a date range to reduce the number of audit log entries. You might have to run multiple searches with smaller date ranges to export more than 50,000 entries.</span></span>
        

3. <span data-ttu-id="faa30-177">Когда вы выберете параметр экспорта, появится в нижней части окна, предлагающее Открытие CSV-файл, сохраните его в папку файлы для загрузки и сохраните его в указанную папку</span><span class="sxs-lookup"><span data-stu-id="faa30-177">After you select an export option, a message is displayed at the bottom of the window that prompts you to open the CSV file, save it to the Downloads folder, or save it to a specific folder</span></span>

[!NOTE] 
 <span data-ttu-id="faa30-178">Дополнительные сведения о просмотре, фильтрация или экспорт результатов поиска в журнале аудита см.</span><span class="sxs-lookup"><span data-stu-id="faa30-178">For more information about viewing, filtering, or exporting audit log search results, see:</span></span>
   - <span data-ttu-id="faa30-179">Просмотр списка аудита действий</span><span class="sxs-lookup"><span data-stu-id="faa30-179">View List of Audited Activities</span></span> 
   - <span data-ttu-id="faa30-180">Перед началом: Журналы единой аудита</span><span class="sxs-lookup"><span data-stu-id="faa30-180">Before You Begin: Unified Audit Logs</span></span>
 