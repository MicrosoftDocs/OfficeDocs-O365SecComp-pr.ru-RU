---
title: Действия, связанные с использованием, после развертывания Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: После настройки и развертывания Office 365 Cloud App Security вам потребуется выполнить определенные задачи, чтобы убедиться, что конфигурация правильная и что вы готовы к обычным проверкам.
ms.openlocfilehash: 3afcfc307ea4a587287f3b71080bba89c715c908
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215949"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="bd76a-103">Действия, связанные с использованием, после развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bd76a-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="bd76a-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="bd76a-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="bd76a-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="bd76a-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="bd76a-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="bd76a-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="bd76a-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="bd76a-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="bd76a-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="bd76a-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="bd76a-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="bd76a-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="bd76a-110">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="bd76a-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="bd76a-111">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="bd76a-111">You are here!</span></span>  <br/> [<span data-ttu-id="bd76a-112">Следующее действие</span><span class="sxs-lookup"><span data-stu-id="bd76a-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="bd76a-p101">Office 365 Cloud App Security доступен в Office 365 корпоративный "~". Если ваша организация использует другую подписку на Office 365 Enterprise, можно приобрести надстройку Office 365 для облачных приложений. в центре администрирования Office 365 (как глобальный администратор) выберите пункт **подписки**на надстройки для **выставления счетов** \> . Дополнительные сведения см. в статье [office 365 Platform Service Description: центр соответствия &amp; требованиям безопасности Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) и [приобретение или изменение надстройки для Office 365 для бизнеса](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="bd76a-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="bd76a-116">После настройки и настройки Office 365 Cloud App Security вы захотите выполнить определенные задачи в качестве глобального администратора Office или администратора безопасности для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="bd76a-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="bd76a-p102">Выполняя эти задачи, вы можете убедиться, что Office 365 Cloud App Security настроен правильно, ваши политики обновлены, а ваша организация понимает значение из Office 365. Используйте эту статью в качестве руководства по планированию этих задач.</span><span class="sxs-lookup"><span data-stu-id="bd76a-p102">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365. Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bd76a-p103">Для выполнения задач, описанных в этой статье, необходимо быть глобальным администратором или администратором безопасности. Чтобы узнать больше, ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="bd76a-p103">You must be a global administrator or security administrator to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="bd76a-121">Действия после первоначальной настройки и развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bd76a-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="bd76a-122">После настройки и развертывания Office 365 Cloud App Security в качестве глобального администратора или администратора безопасности необходимо учесть следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="bd76a-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="bd76a-123">Какие задачи необходимо добавить в календарь ИТ отдела?</span><span class="sxs-lookup"><span data-stu-id="bd76a-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="bd76a-124">Как убедиться, что приложение Office 365 Cloud App Security настроено на использование правильного набора политик с течением времени?</span><span class="sxs-lookup"><span data-stu-id="bd76a-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="bd76a-125">Какие типы сводных данных следует отправлять вверх по цепочке управления ИТ?</span><span class="sxs-lookup"><span data-stu-id="bd76a-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="bd76a-126">В следующей таблице кратко описаны текущие задачи, которые необходимо выполнить и периодические задачи, которые следует рассмотреть для добавления в календарь ИТ отдела.</span><span class="sxs-lookup"><span data-stu-id="bd76a-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="bd76a-127">**Текущие задачи**</span><span class="sxs-lookup"><span data-stu-id="bd76a-127">**Ongoing tasks**</span></span>|<span data-ttu-id="bd76a-128">**Периодические задачи**</span><span class="sxs-lookup"><span data-stu-id="bd76a-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bd76a-129">Мониторинг учетных записей электронной почты, на которые отправляются оповещения</span><span class="sxs-lookup"><span data-stu-id="bd76a-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="bd76a-130">Для получения последних сведений о новых атаках кибератак в индустрии отраслевых циберсекурити новостей</span><span class="sxs-lookup"><span data-stu-id="bd76a-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="bd76a-131">Действия с оповещениями системы безопасности для определения и устранения проблем безопасности и рисков</span><span class="sxs-lookup"><span data-stu-id="bd76a-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="bd76a-132">Сводка по каждому инциденту и разрешению системы безопасности в центральном журнале</span><span class="sxs-lookup"><span data-stu-id="bd76a-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="bd76a-133">ВыПолняйте ежемесячный или ежеквартальный анализ оповещений о безопасности облачного приложения Office 365 для выявления аномалий и анализа тенденций</span><span class="sxs-lookup"><span data-stu-id="bd76a-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="bd76a-134">ВыПолняйте ежемесячные или ежеквартальные обзоры существующих политик безопасности облачных приложений Office 365, чтобы включить в Office 365 Cloud App Security and New кибератаки and Trends in циберсекурити</span><span class="sxs-lookup"><span data-stu-id="bd76a-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="bd76a-135">В зависимости от размера организации и заинтересованности в мониторинге и обслуживании статуре безопасности вы можете скомпилировать ежемесячную сводку для своей цепочки управления ИТ, которая включает:</span><span class="sxs-lookup"><span data-stu-id="bd76a-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="bd76a-136">Различные типы инцидентов безопасности, обнаруженных в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bd76a-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="bd76a-137">Сводные сведения из центрального журнала инцидентов безопасности, таких как количество обнаруженных инцидентов.</span><span class="sxs-lookup"><span data-stu-id="bd76a-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="bd76a-138">Тенденции оповещений и их устранение</span><span class="sxs-lookup"><span data-stu-id="bd76a-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="bd76a-139">Последние тенденции циберсекурити</span><span class="sxs-lookup"><span data-stu-id="bd76a-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="bd76a-140">Рекомендации по изменению политики безопасности Cloud App в Office 365 и их влиянии на конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="bd76a-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="bd76a-141">Действия после прохождения времени после развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bd76a-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="bd76a-142">Если время, прошедшее с момента первоначальной настройки или обслуживания политик безопасности облачных приложений Office 365, прошло успешно, выполните следующие действия, чтобы вернуться к конфигурации, которая отражает цели безопасности Организации и текущие возможности Office 365 Cloud App Security:</span><span class="sxs-lookup"><span data-stu-id="bd76a-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="bd76a-143">Определите дату последнего изменения конфигурации для Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="bd76a-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="bd76a-p104">Ознакомьтесь с текущей конфигурацией безопасности облачных приложений Office 365 и при необходимости настройте эти политики. Например, убедитесь, что вы знаете, куда отправляются оповещения по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="bd76a-p104">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed. For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="bd76a-146">Узнайте [о новых возможноСтях office 365 Cloud App Security](new-in-office-365-cas.md) для изменений продуктов с момента последней настройки безопасности облачных приложений Office 365.</span><span class="sxs-lookup"><span data-stu-id="bd76a-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="bd76a-147">Выполните анализ оповещений и журналов Office 365 Cloud App Security для выявления аномалий и анализа тенденций.</span><span class="sxs-lookup"><span data-stu-id="bd76a-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="bd76a-148">Проверьте тенденции отраслевых циберсекурити, чтобы узнать о новейших угрозах безопасности.</span><span class="sxs-lookup"><span data-stu-id="bd76a-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="bd76a-p105">Выполните анализ изменений, которые необходимо внести в текущий набор политик безопасности облачных приложений Office 365. Включение изменений в функции безопасности облачных приложений Office 365, текущих аномалий и тенденций циберсекурити. Рекомендации по изменению существующих политик или созданию новых политик.</span><span class="sxs-lookup"><span data-stu-id="bd76a-p105">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies. Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends. Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="bd76a-p106">Создайте план для реализации изменений политики. Обмен данными (соЦиализе) о последствиях предполагаемых изменений для конечных пользователей в случае необходимости.</span><span class="sxs-lookup"><span data-stu-id="bd76a-p106">Make a plan for implementing the policy changes. Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="bd76a-154">Реализация изменений в политике безопасности облачного приложения Office 365.</span><span class="sxs-lookup"><span data-stu-id="bd76a-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="bd76a-155">Отслеживание отзывов конечных пользователей и оповещений системы безопасности облачного приложения Office 365 и Настройка политик с течением времени.</span><span class="sxs-lookup"><span data-stu-id="bd76a-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="bd76a-156">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="bd76a-156">Next steps</span></span>

- [<span data-ttu-id="bd76a-157">Исследование действия</span><span class="sxs-lookup"><span data-stu-id="bd76a-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="bd76a-158">ПриОстановка или восстановление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="bd76a-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="bd76a-159">Управление приложениями OAuth</span><span class="sxs-lookup"><span data-stu-id="bd76a-159">Manage OAuth apps</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="bd76a-160">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bd76a-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="bd76a-161">Просмотр списка поддерживаемых [журналов веб-трафика и источников данных](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="bd76a-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

