---
title: 'Запустите отчет о группе ролей администратора в EOP '
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 23b47b57-0eec-46a3-a03b-366ea014ab31
description: Когда администратор добавляет или удаляет участников из группы ролей администраторов, Microsoft Exchange Online Protection (EOP) регистрирует каждое такое действие в журнале.
ms.openlocfilehash: 49311faa4ee54fafa1c05a2314ed2f9d74cbe5a5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027206"
---
# <a name="run-an-administrator-role-group-report-in-eop"></a><span data-ttu-id="e2d48-103">Запустите отчет о группе ролей администратора в EOP</span><span class="sxs-lookup"><span data-stu-id="e2d48-103">Run an administrator role group report in EOP</span></span> 

 <span data-ttu-id="e2d48-p101">Когда администратор добавляет или удаляет участников из группы ролей администраторов, Microsoft Exchange Online Protection (EOP) регистрирует каждое такое действие в журнале. При запуске отчета о группе ролей администраторов в Центре администрирования Exchange записи отображаются в виде результатов поиска и включают затронутые группы ролей, сведения о том, кто и когда изменял состав группы, а также о том, какие изменения произошли в составе группы. Этот отчет можно использовать для отслеживания изменений в административных разрешениях, назначенных пользователям в организации.</span><span class="sxs-lookup"><span data-stu-id="e2d48-p101">When an administrator adds members to or removes members from administrator role groups, Microsoft Exchange Online Protection (EOP) logs each occurrence. When you run an administrator role group report in the Exchange admin center, entries are displayed as search results and include the role groups affected, who changed the role group membership and when, and what membership updates were made. Use this report to monitor changes to the administrative permissions assigned to users in your organization.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="e2d48-107">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="e2d48-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="e2d48-108">Предполагаемое время для завершения: 2 минуты.</span><span class="sxs-lookup"><span data-stu-id="e2d48-108">Estimated time to complete: 2 minutes</span></span>
    
- <span data-ttu-id="e2d48-p102">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье Статья "Отчеты" раздела [Разрешения на функции в службе EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="e2d48-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Reports" section of the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="e2d48-111">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Сочетания клавиш в Центре администрирования Exchange**.</span><span class="sxs-lookup"><span data-stu-id="e2d48-111">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="e2d48-p103">Возникли проблемы? Обратитесь за помощью к участникам форумов, посвященных Exchange. Посетите форумы по таким продуктам: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) или [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="e2d48-p103">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="use-the-eac-to-run-an-administrator-role-group-report"></a><span data-ttu-id="e2d48-115">Запуск отчета о группе ролей администраторов с помощью Центра администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="e2d48-115">Use the EAC to run an administrator role group report</span></span>

<span data-ttu-id="e2d48-116">Чтобы найти изменения в группах ролей управления в организации за определенный интервал времени, запустите отчет о группе ролей администраторов.</span><span class="sxs-lookup"><span data-stu-id="e2d48-116">Run the administrator role group report to find the changes to management role groups in your organization within a particular timeframe.</span></span>
  
1. <span data-ttu-id="e2d48-117">В Центре администрирования Exchange выберите пункты **Управление соответствием требованиям** \> **Аудит**, а затем выберите команду **Запустить отчет о группе ролей администраторов**.</span><span class="sxs-lookup"><span data-stu-id="e2d48-117">In the EAC, navigate to **Compliance management** \> **Auditing**, and choose **Run an administrator role group report**.</span></span>
    
2. <span data-ttu-id="e2d48-p104">Задайте параметры **Дата начала** и **Дата окончания**. По умолчанию отчет выполняет поиск изменений в группе ролей администраторов за последние две недели.</span><span class="sxs-lookup"><span data-stu-id="e2d48-p104">Choose the **Start date** and **End date**. By default, the report searches for changes made to administrator role groups in the past two weeks.</span></span>
    
3. <span data-ttu-id="e2d48-p105">Чтобы просмотреть изменения в определенной группе ролей, нажмите кнопку **Выбрать группы ролей**. В появившемся диалоговом окне выберите группу или группы ролей, затем нажмите кнопку **ОК**. Чтобы найти все изменения групп ролей, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="e2d48-p105">To view the changes for a specific role group, click **Select role groups**. Select the role group (or groups) in the subsequent dialog box, and click **OK**. You can also leave the field blank to find all changed role groups.</span></span>
    
4. <span data-ttu-id="e2d48-123">Нажмите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="e2d48-123">Click **Search**.</span></span>
    
<span data-ttu-id="e2d48-p106">Если будут найдены любые изменения, соответствующие заданным критериям, они появятся в области результатов. Чтобы в области сведений увидеть изменения, выберите группу ролей в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="e2d48-p106">If any changes are found using the criteria you specified, they will appear in the results pane. Click a role group in the search results to see the changes in the details pane.</span></span>
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="e2d48-126">Как проверить, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="e2d48-126">How do you know this worked?</span></span>

<span data-ttu-id="e2d48-p107">Если отчет о группе ролей администрирования запущен успешно, группы ролей, измененные в рамках диапазона дат, отображаются в области результатов поиска. Если результатов нет  в указанный диапазон дат группы ролей изменены не были. Если вы считаете, что результаты должны быть, измените диапазон дат и повторно запустите отчет.</span><span class="sxs-lookup"><span data-stu-id="e2d48-p107">If you've successfully run an administrator role group report, role groups that have been changed within the date range are displayed in the search results pane. If there are no results, then no changes to role groups have taken place within the specified date range. If you think there should be results, change the date range and then run the report again.</span></span>
  
## <a name="monitor-changes-to-role-group-membership"></a><span data-ttu-id="e2d48-130">Отслеживание изменений состава группы ролей</span><span class="sxs-lookup"><span data-stu-id="e2d48-130">Monitor changes to role group membership</span></span>

<span data-ttu-id="e2d48-p108">При добавлении или удалении участников группы ролей результаты поиска в области сведений указывают на изменение состава группы ролей с указанием ее текущих участников. В результатах не говорится явно, кто был добавлен или удален.</span><span class="sxs-lookup"><span data-stu-id="e2d48-p108">When members are added to or removed from a role group, the search results displayed in the details pane indicate that the role group membership was updated and lists the current members. The results don't explicitly state which user was added or removed.</span></span>
  
<span data-ttu-id="e2d48-p109">Чтобы определить, был ли добавлен или удален пользователь, следует сравнить две записи в отчете. Например, рассмотрим следующие записи журнала для группы ролей **HelpDesk**.</span><span class="sxs-lookup"><span data-stu-id="e2d48-p109">To determine if a user was added or removed, you have to compare two separate entries in the report. For example, let's look at the following log entries for the **HelpDesk** role group:</span></span> 
  
 <span data-ttu-id="e2d48-135">**27.01.2013 16:43:00**</span><span class="sxs-lookup"><span data-stu-id="e2d48-135">**1/27/2013 4:43 PM**</span></span>
  
 <span data-ttu-id="e2d48-136">**Администратор**</span><span class="sxs-lookup"><span data-stu-id="e2d48-136">**Administrator**</span></span>
  
 <span data-ttu-id="e2d48-137">**Обновленные участники: Administrator;annb,florencef;pilarp**</span><span class="sxs-lookup"><span data-stu-id="e2d48-137">**Updated members: Administrator;annb,florencef;pilarp**</span></span>
  
 <span data-ttu-id="e2d48-138">**06.02.2013 10:09:00**</span><span class="sxs-lookup"><span data-stu-id="e2d48-138">**2/06/2013 10:09 AM**</span></span>
  
 <span data-ttu-id="e2d48-139">**Администратор**</span><span class="sxs-lookup"><span data-stu-id="e2d48-139">**Administrator**</span></span>
  
 <span data-ttu-id="e2d48-140">**Обновленные участники: Administrator;annb;florencef;pilarp;tonip**</span><span class="sxs-lookup"><span data-stu-id="e2d48-140">**Updated members: Administrator;annb;florencef;pilarp;tonip**</span></span>
  
 <span data-ttu-id="e2d48-141">**19.02.2013 14:12**</span><span class="sxs-lookup"><span data-stu-id="e2d48-141">**2/19/2013 2:12 PM**</span></span>
  
 <span data-ttu-id="e2d48-142">**Администратор**</span><span class="sxs-lookup"><span data-stu-id="e2d48-142">**Administrator**</span></span>
  
 <span data-ttu-id="e2d48-143">**Обновленные участники: Administrator;annb;florencef;tonip**</span><span class="sxs-lookup"><span data-stu-id="e2d48-143">**Updated members: Administrator;annb;florencef;tonip**</span></span>
  
<span data-ttu-id="e2d48-144">В этом примере администратор внес следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="e2d48-144">In this example, the Administrator user account made the following changes:</span></span>
  
- <span data-ttu-id="e2d48-145">06.02.2013 был добавлен пользователь tonip.</span><span class="sxs-lookup"><span data-stu-id="e2d48-145">On 2/06/2013, it added the user tonip.</span></span>
    
- <span data-ttu-id="e2d48-146">19.02.2013 был удален пользователь pilarp.</span><span class="sxs-lookup"><span data-stu-id="e2d48-146">On 2/19/2013, it removed the user pilarp.</span></span>
    

