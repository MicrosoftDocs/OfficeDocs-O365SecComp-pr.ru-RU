---
title: Действия, связанные с использованием, после развертывания Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: После настройки и для развертывания Office 365 облачных приложений безопасности, необходимые для выполнения некоторых задач конфигурации является правильным и, что быть готовым регулярных проверок.
ms.openlocfilehash: 71b6793f2e325fcba3431ba5157640b29814ad30
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603710"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="80321-103">Действия, связанные с использованием, после развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="80321-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="80321-104">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="80321-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="80321-105">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="80321-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="80321-106">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="80321-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="80321-107">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="80321-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="80321-108">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="80321-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="80321-109">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="80321-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="80321-110">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="80321-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="80321-111">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="80321-111">You are here!</span></span>  <br/> [<span data-ttu-id="80321-112">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="80321-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="80321-p101">Безопасности приложения Office 365 облаке доступна в Office 365 корпоративный E5. Если ваша организация использует другой подписки Office 365 для предприятия, облачных приложений Office 365 безопасности можно приобрести в виде дополнительного компонента. (Как глобальный администратор, в центре администрирования Office 365 нажмите кнопку **выставления счетов** \> **Добавить подписок**.) Дополнительные сведения можно [Описание платформы Office 365: безопасность Office 365 &amp; центре соответствия требованиям](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) и [покупке и изменить надстройки для Office 365 для бизнеса](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="80321-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="80321-116">После установки и настройки безопасности Office 365 облаке приложения может потребоваться для выполнения некоторых задач использование как глобальный администратор Office 365 или администратора безопасности для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="80321-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="80321-p102">Выполнение этих задач, будет обеспечения безопасности Office 365 облаке приложения настроена правильно, политик в актуальном состоянии и ваша организация реализует значение из Office 365. Используйте эту статью в качестве руководства при планировании для выполнения этих задач.</span><span class="sxs-lookup"><span data-stu-id="80321-p102">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365. Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="80321-p103">Необходимо быть глобальным администратором или администратор безопасности для выполнения задач, описанных в этой статье. Чтобы получить дополнительные сведения, обратитесь к разделу [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="80321-p103">You must be a global administrator or security administrator to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="80321-121">Действия после начальной настройки и развертывания приложения облаке Безопасность в Office 365</span><span class="sxs-lookup"><span data-stu-id="80321-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="80321-122">После настройки и для развертывания, как глобальный администратор или администраторов безопасности приложения Office 365 облаке у вас есть несколько моментов, которые следует учесть:</span><span class="sxs-lookup"><span data-stu-id="80321-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="80321-123">Какие задачи должны быть добавлены в календарь отдела ИТ?</span><span class="sxs-lookup"><span data-stu-id="80321-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="80321-124">Как сделать настройки безопасности Office 365 облаке приложения для использования правильный набор политик по времени</span><span class="sxs-lookup"><span data-stu-id="80321-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="80321-125">Какие виды сводную информацию следует отправить по цепочке управления ИТ?</span><span class="sxs-lookup"><span data-stu-id="80321-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="80321-126">В следующей таблице кратко перечислены текущие задачи, необходимые для выполнения и периодических задач, рекомендуется добавить в календарь ИТ-подразделения.</span><span class="sxs-lookup"><span data-stu-id="80321-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="80321-127">**Текущие задачи**</span><span class="sxs-lookup"><span data-stu-id="80321-127">**Ongoing tasks**</span></span>|<span data-ttu-id="80321-128">**Периодические задачи**</span><span class="sxs-lookup"><span data-stu-id="80321-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="80321-129">Мониторинг учетных записей электронной почты, к которым выполняется отправка сообщения с оповещением</span><span class="sxs-lookup"><span data-stu-id="80321-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="80321-130">Монитор отрасли cybersecurity новостей для получения последних сведений о новой атаки через Интернет</span><span class="sxs-lookup"><span data-stu-id="80321-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="80321-131">Работать с оповещение системы безопасности для выявления и устранения угрозы безопасности и риски, связанные с</span><span class="sxs-lookup"><span data-stu-id="80321-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="80321-132">Сведение каждого происшествия безопасности и разрешения в центре журнала</span><span class="sxs-lookup"><span data-stu-id="80321-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="80321-133">Помесячный или Поквартальный обзоров безопасности приложения Office 365 облачных оповещения для плашечных ошибок и анализировать тенденции</span><span class="sxs-lookup"><span data-stu-id="80321-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="80321-134">Помесячный или Поквартальный обзоров существующих политик безопасности Office 365 облаке приложения для включения усовершенствований в облаке приложения Office 365 безопасности и адрес новой cyberattacks и тенденций cybersecurity</span><span class="sxs-lookup"><span data-stu-id="80321-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="80321-135">В зависимости от размера и мониторинг и обслуживание stature безопасности вашей организации можно компилировать ежемесячный Сводка для вашей цепочки управления ИТ, которая включает в себя:</span><span class="sxs-lookup"><span data-stu-id="80321-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="80321-136">Различные типы угрозы безопасности с помощью приложения облаке Безопасность в Office 365</span><span class="sxs-lookup"><span data-stu-id="80321-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="80321-137">Сводные сведения из центра журнала угрозы безопасности, такие как количество проблем, обнаруженных</span><span class="sxs-lookup"><span data-stu-id="80321-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="80321-138">Оповещения тенденции и как они были исправлены</span><span class="sxs-lookup"><span data-stu-id="80321-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="80321-139">Последние тенденции cybersecurity</span><span class="sxs-lookup"><span data-stu-id="80321-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="80321-140">Рекомендации для изменения политики безопасности Office 365 облачных приложений и их влияние на конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="80321-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="80321-141">Действия после истечения времени с момента развертывания приложения облаке Безопасность в Office 365</span><span class="sxs-lookup"><span data-stu-id="80321-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="80321-142">Если длительного количество времени, прошедшее изначально настроены или обслуживать политик безопасности Office 365 облачных приложений, выполните следующие действия, чтобы вернуться к конфигурации, показывающая целям безопасности вашей организации и текущих возможностях Office 365 облачных приложений средств обеспечения безопасности:</span><span class="sxs-lookup"><span data-stu-id="80321-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="80321-143">Определите дату последнего изменения конфигурации для приложения облаке Безопасность в Office 365.</span><span class="sxs-lookup"><span data-stu-id="80321-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="80321-p104">Понять конфигурацию безопасности Office 365 облаке приложения и при необходимости измените этих политик. Например убедитесь, что вы знаете, где отправляются оповещения по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="80321-p104">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed. For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="80321-146">С момента последнего настройки безопасности Office 365 облаке приложения в разделе [новые возможности в облаке приложения Office 365 безопасности](new-in-office-365-cas.md) для изменения продукта.</span><span class="sxs-lookup"><span data-stu-id="80321-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="80321-147">Выполните анализ безопасности приложения Office 365 облачных оповещений и журналов для плашечных ошибок и анализа тенденций.</span><span class="sxs-lookup"><span data-stu-id="80321-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="80321-148">Установите флажок отраслевых тенденций cybersecurity, чтобы узнать о последних угроз безопасности.</span><span class="sxs-lookup"><span data-stu-id="80321-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="80321-p105">Выполните анализ изменений, которые должны быть выполнены для текущего набора политик безопасности приложения Office 365 облака. Включить изменения в функциональных возможностях безопасности приложения Office 365 облаке, текущий ошибок и cybersecurity тенденций. Рекомендуем изменения существующей политики или создания новой политики.</span><span class="sxs-lookup"><span data-stu-id="80321-p105">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies. Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends. Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="80321-p106">Создайте план реализации изменения политики. Взаимодействие (общаться) последствия предложенного изменения с конечных пользователей при необходимости.</span><span class="sxs-lookup"><span data-stu-id="80321-p106">Make a plan for implementing the policy changes. Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="80321-154">Реализует изменения политики безопасности приложения Office 365 облака.</span><span class="sxs-lookup"><span data-stu-id="80321-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="80321-155">Мониторинг отзыв конечного пользователя и оповещения по безопасности Office 365 облаке приложения и корректировка политик по времени.</span><span class="sxs-lookup"><span data-stu-id="80321-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="80321-156">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="80321-156">Next steps</span></span>

- [<span data-ttu-id="80321-157">Анализ деятельности</span><span class="sxs-lookup"><span data-stu-id="80321-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="80321-158">Приостановка или восстановление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="80321-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="80321-159">Управление приложениями OAuth</span><span class="sxs-lookup"><span data-stu-id="80321-159">Manage OAuth apps</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="80321-160">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="80321-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="80321-161">Просмотр списка поддерживаемых [веб-трафика журналов и источников данных](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="80321-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

