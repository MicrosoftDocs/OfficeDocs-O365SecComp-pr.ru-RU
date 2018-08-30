---
title: Отчеты о контроле
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 5/12/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2a762db5-e1c9-4c09-aa8e-bef49ce97209
description: С помощью контроля отчетов, чтобы узнать, какие сообщения электронной почты требуется просмотрите соответствия требованиям и пользователей, которые необходимо выполнить.
ms.openlocfilehash: e18d083c0aad8be945c628516e593462da8e3898
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534445"
---
# <a name="supervision-reports"></a><span data-ttu-id="a26ff-103">Отчеты о контроле</span><span class="sxs-lookup"><span data-stu-id="a26ff-103">Supervision reports</span></span>

<span data-ttu-id="a26ff-p101">Определить, какие политики контроля коммуникаций в вашей организации требуется проверка для соответствия требованиям и пользователей, которые будут выполнять их проверки. Использование отчетов о контроля для просмотра действий Обзор на уровне политики и редактор. Для каждой политики можно также просмотреть live статистики на текущее состояние проверки активности. [Дополнительные сведения о политики контроля](configure-supervision-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="a26ff-p101">Supervision policies define which communications in your organization need review for compliance, and who will perform those reviews. Use the supervision reports to see the review activity at the policy and reviewer level. For each policy, you can also view live statistics on the current state of review activity. [Learn more about supervision policies ](configure-supervision-policies.md) .</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a26ff-p102">С помощью политики контроля требуется подписка на Office 365 E5 для вашей организации. Если нет этого плана и попытайтесь контроля, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="a26ff-p102">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="a26ff-110">Можно использовать отчеты контроля:</span><span class="sxs-lookup"><span data-stu-id="a26ff-110">You can use the supervision reports to:</span></span>
  
- <span data-ttu-id="a26ff-111">Убедитесь, что политик работают, как нужно.</span><span class="sxs-lookup"><span data-stu-id="a26ff-111">Verify that your policies are working as you intended.</span></span> 
    
- <span data-ttu-id="a26ff-112">Узнайте, сколько по электронной почте определены для проверки.</span><span class="sxs-lookup"><span data-stu-id="a26ff-112">Find out how many emails are being identified for review.</span></span>
    
- <span data-ttu-id="a26ff-p103">Узнайте, сколько по электронной почте не соответствует спецификации и какие из них являются проверки передачи. Эти сведения могут помочь вам решить, следует ли получить более точные политик или изменения номера рецензентов.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p103">Find out how many emails aren't compliant and which ones are passing review. This information can help you decide whether to fine-tune your policies or change the number of reviewers.</span></span>
    
## <a name="view-the-supervision-report"></a><span data-ttu-id="a26ff-115">Просмотр отчета о контроля</span><span class="sxs-lookup"><span data-stu-id="a26ff-115">View the Supervision report</span></span>

1. <span data-ttu-id="a26ff-116">Вход в [безопасности &amp; центре соответствия требованиям](https://protection.office.com/) с использованием учетных данных для учетной записи администратора в организации Office 365, имеющая разрешения на просмотр отчетов контроля...</span><span class="sxs-lookup"><span data-stu-id="a26ff-116">Sign into the [Security &amp; Compliance Center](https://protection.office.com/) using the credentials for an admin account in your Office 365 organization that has permissions to view supervision reports..</span></span> 
    
2. <span data-ttu-id="a26ff-p104">Последовательно выберите пункты **отчеты** \> **панели мониторинга**. Вы увидите отчетов мини-приложения для контроля и другие отчеты у вас есть доступ.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p104">Go to **Reports** \> **Dashboard**. You'll see a reporting widget for supervision and other reports you have access to.</span></span>
    
3. <span data-ttu-id="a26ff-119">Нажмите кнопку **контроля** мини-приложения для открытия страницы подробный отчет.</span><span class="sxs-lookup"><span data-stu-id="a26ff-119">Click the **Supervision** widget to open the detailed report page.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a26ff-p105">Если вы не могут получить доступ к странице " **отчеты** ", проверьте, что вы являетесь участником группы ролей контролирующий проверки, как описано в [сделать контроля недоступны в вашей организации](configure-supervision-policies.md#SRavailable). Включение в группу ролей позволяет создание и управление ими контроля политик и запустить отчет.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p105">If you aren't able to access the **Reports** page, check that you're a member of the Supervisory Review role group, as described in [Make supervision available in your organization](configure-supervision-policies.md#SRavailable). Being included in this role group lets you create and manage supervision polices and run the report.</span></span> 
  
## <a name="how-to-use-the-report"></a><span data-ttu-id="a26ff-122">Как использовать в отчете</span><span class="sxs-lookup"><span data-stu-id="a26ff-122">How to use the report</span></span>

<span data-ttu-id="a26ff-p106">Когда политика контроля идентифицирует сообщение электронной почты для просмотра, сообщение электронной почты доставляется в папку контроля рецензента в Outlook и Outlook web app. В данном отчете показано имя каждой политики и число коммуникаций на каждой стадии в процессе проверки.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p106">When a supervision policy identifies an email for review, the email is delivered to the reviewer's Supervision folder in Outlook and Outlook web app. This report lists each policy's name and the number of communications at each stage in the review process.</span></span>
  
<span data-ttu-id="a26ff-125">Используйте в отчете:</span><span class="sxs-lookup"><span data-stu-id="a26ff-125">Use the report to:</span></span>
  
- <span data-ttu-id="a26ff-126">Просмотр данных для всех или определенных политик.</span><span class="sxs-lookup"><span data-stu-id="a26ff-126">View data for all or specific policies.</span></span>
    
- <span data-ttu-id="a26ff-127">Просмотр данных, сгруппированные по типу тег (например, соответствует, Questionable, и т.д.), рецензент или тип сообщения.</span><span class="sxs-lookup"><span data-stu-id="a26ff-127">View data grouped by tag type (such as Compliant, Questionable, etc.), reviewer, or message type.</span></span>
    
- <span data-ttu-id="a26ff-128">Экспорт данных в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="a26ff-128">Export data to a CSV file.</span></span>
    
- <span data-ttu-id="a26ff-129">Фильтрация данных на основе просмотрите Дата действия, типа тега, редактор, тип сообщения.</span><span class="sxs-lookup"><span data-stu-id="a26ff-129">Filter data based on review activity date, tag type, reviewer, message type.</span></span>
    
<span data-ttu-id="a26ff-130">Вот декомпозиции из значения, которые можно увидеть в столбце **тип тега** .</span><span class="sxs-lookup"><span data-stu-id="a26ff-130">Here's a breakdown of the values you might see in the **Tag type** column.</span></span> 
  
|<span data-ttu-id="a26ff-131">**Тип тега**</span><span class="sxs-lookup"><span data-stu-id="a26ff-131">**Tag type**</span></span>|<span data-ttu-id="a26ff-132">**Что означает**</span><span class="sxs-lookup"><span data-stu-id="a26ff-132">**What it means**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a26ff-133">Проверять</span><span class="sxs-lookup"><span data-stu-id="a26ff-133">Not Reviewed</span></span>  <br/> |<span data-ttu-id="a26ff-p107">Количество по электронной почте, которые не были просмотрены еще. Эти сообщения ожидают проверки в папке контроля рецензента в Outlook.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p107">The number of emails that have not been reviewed yet. These emails are awaiting review in the reviewer's supervision folder in Outlook.</span></span>  <br/> |
|<span data-ttu-id="a26ff-136">Спецификации</span><span class="sxs-lookup"><span data-stu-id="a26ff-136">Compliant</span></span>  <br/> |<span data-ttu-id="a26ff-p108">Количество по электронной почте просматривается и помечена как соответствующая требованиям. Не требуется никаких действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p108">The number of emails reviewed and marked as compliant. No further action is needed.</span></span>  <br/> |
|<span data-ttu-id="a26ff-139">Сомнительные</span><span class="sxs-lookup"><span data-stu-id="a26ff-139">Questionable</span></span>  <br/> |<span data-ttu-id="a26ff-p109">Количество по электронной почте анализа и помечается сомнительные. Этот параметр действует как флаг; другие проверяющие могут помочь проверять, должна ли сообщения электронной почты расследования для соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p109">The number of emails reviewed and marked questionable. This acts as a flag; other reviewers can help check whether an email needs investigation for compliance.</span></span>  <br/> |
|<span data-ttu-id="a26ff-142">Не соответствует спецификации (Active)</span><span class="sxs-lookup"><span data-stu-id="a26ff-142">Non-Compliant (Active)</span></span>  <br/> |<span data-ttu-id="a26ff-143">Количество не соответствует спецификации по электронной почте, которые в настоящее время ведется расследование рецензентов.</span><span class="sxs-lookup"><span data-stu-id="a26ff-143">The number of non-compliant emails that reviewers are currently investigating.</span></span>  <br/> |
|<span data-ttu-id="a26ff-144">Не соответствует спецификации (Разрешить)</span><span class="sxs-lookup"><span data-stu-id="a26ff-144">Non-Compliant (Resolved)</span></span>  <br/> |<span data-ttu-id="a26ff-145">Количество не соответствует спецификации по электронной почте, которые рецензентов изучению и разрешения.</span><span class="sxs-lookup"><span data-stu-id="a26ff-145">The number of non-compliant emails that reviewers investigated and resolved.</span></span>  <br/> |
   
## <a name="more-details"></a><span data-ttu-id="a26ff-146">Более подробные сведения</span><span class="sxs-lookup"><span data-stu-id="a26ff-146">More details</span></span>

- <span data-ttu-id="a26ff-147">Политики контроля необходимо сначала подготовить к работе, прежде чем они будут отображаться в данном отчете.</span><span class="sxs-lookup"><span data-stu-id="a26ff-147">Supervision policies must first be provisioned before they will appear in this report.</span></span>
    
- <span data-ttu-id="a26ff-p110">Если удаляются политики, статистические данные по-прежнему отображается. Тем не менее они будет указано как «политика не существует», и функции **экспорта** не доступна.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p110">If policies are deleted, historical data is still shown. However, they're indicated as a "Non-existent policy", and the **Export** function isn't available.</span></span> 
    
- <span data-ttu-id="a26ff-p111">Если отчет не отображается все данные по умолчанию, возможно, текущей даты не содержит данных для отображения. В таких случаях используйте элемент управления **фильтры** , чтобы изменить диапазон дат.</span><span class="sxs-lookup"><span data-stu-id="a26ff-p111">If the report doesn't show any data by default, it might be because the current date range doesn't have any data to show. In these cases, use the **Filters** control to change the date range.</span></span> 
    

