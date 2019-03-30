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
ms.openlocfilehash: 232de4df1d1eb4debdddcee2c1d8672d1aeb4b21
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999952"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="b9a69-103">Действия, связанные с использованием, после развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b9a69-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="b9a69-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b9a69-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="b9a69-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b9a69-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="b9a69-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="b9a69-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="b9a69-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b9a69-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="b9a69-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="b9a69-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="b9a69-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="b9a69-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="b9a69-110">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="b9a69-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="b9a69-111">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="b9a69-111">You are here!</span></span>  <br/> [<span data-ttu-id="b9a69-112">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="b9a69-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="b9a69-113">Office 365 Cloud App Security доступен в Office 365 корпоративный "~".</span><span class="sxs-lookup"><span data-stu-id="b9a69-113">Office 365 Cloud App Security is available in Office 365 Enterprise E5.</span></span> <span data-ttu-id="b9a69-114">Если ваша организация использует другую подписку на Office 365 Enterprise, можно приобрести надстройку Office 365 для облачных приложений.</span><span class="sxs-lookup"><span data-stu-id="b9a69-114">If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on.</span></span> <span data-ttu-id="b9a69-115">в центре администрирования Microsoft 365 (как глобальный администратор) выберите пункт **подписки**на надстройки для **выставления счетов** \> . Дополнительные сведения см. в статье [office 365 Platform Service Description: центр соответствия &amp; требованиям безопасности Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) и [приобретение или изменение надстройки для Office 365 для бизнеса](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="b9a69-115">(As a global administrator, in the Microsoft 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="b9a69-116">После настройки и настройки Office 365 Cloud App Security вы захотите выполнить определенные задачи в качестве глобального администратора Office или администратора безопасности для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="b9a69-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="b9a69-117">Выполняя эти задачи, вы можете убедиться, что Office 365 Cloud App Security настроен правильно, ваши политики обновлены, а ваша организация понимает значение из Office 365.</span><span class="sxs-lookup"><span data-stu-id="b9a69-117">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365.</span></span> <span data-ttu-id="b9a69-118">Используйте эту статью в качестве руководства по планированию этих задач.</span><span class="sxs-lookup"><span data-stu-id="b9a69-118">Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b9a69-119">Для выполнения задач, описанных в этой статье, необходимо быть глобальным администратором или администратором безопасности.</span><span class="sxs-lookup"><span data-stu-id="b9a69-119">You must be a global administrator or security administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="b9a69-120">Чтобы узнать больше, ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="b9a69-120">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="b9a69-121">Действия после первоначальной настройки и развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b9a69-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="b9a69-122">После настройки и развертывания Office 365 Cloud App Security в качестве глобального администратора или администратора безопасности необходимо учесть следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="b9a69-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="b9a69-123">Какие задачи необходимо добавить в календарь ИТ отдела?</span><span class="sxs-lookup"><span data-stu-id="b9a69-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="b9a69-124">Как убедиться, что приложение Office 365 Cloud App Security настроено на использование правильного набора политик с течением времени?</span><span class="sxs-lookup"><span data-stu-id="b9a69-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="b9a69-125">Какие типы сводных данных следует отправлять вверх по цепочке управления ИТ?</span><span class="sxs-lookup"><span data-stu-id="b9a69-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="b9a69-126">В следующей таблице кратко описаны текущие задачи, которые необходимо выполнить и периодические задачи, которые следует рассмотреть для добавления в календарь ИТ отдела.</span><span class="sxs-lookup"><span data-stu-id="b9a69-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="b9a69-127">**Текущие задачи**</span><span class="sxs-lookup"><span data-stu-id="b9a69-127">**Ongoing tasks**</span></span>|<span data-ttu-id="b9a69-128">**Периодические задачи**</span><span class="sxs-lookup"><span data-stu-id="b9a69-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b9a69-129">Мониторинг учетных записей электронной почты, на которые отправляются оповещения</span><span class="sxs-lookup"><span data-stu-id="b9a69-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="b9a69-130">Для получения последних сведений о новых атаках кибератак в индустрии отраслевых циберсекурити новостей</span><span class="sxs-lookup"><span data-stu-id="b9a69-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="b9a69-131">Действия с оповещениями системы безопасности для определения и устранения проблем безопасности и рисков</span><span class="sxs-lookup"><span data-stu-id="b9a69-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="b9a69-132">Сводка по каждому инциденту и разрешению системы безопасности в центральном журнале</span><span class="sxs-lookup"><span data-stu-id="b9a69-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="b9a69-133">ВыПолняйте ежемесячный или ежеквартальный анализ оповещений о безопасности облачного приложения Office 365 для выявления аномалий и анализа тенденций</span><span class="sxs-lookup"><span data-stu-id="b9a69-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="b9a69-134">ВыПолняйте ежемесячные или ежеквартальные обзоры существующих политик безопасности облачных приложений Office 365, чтобы включить в Office 365 Cloud App Security and New кибератаки and Trends in циберсекурити</span><span class="sxs-lookup"><span data-stu-id="b9a69-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="b9a69-135">В зависимости от размера организации и заинтересованности в мониторинге и обслуживании статуре безопасности вы можете скомпилировать ежемесячную сводку для своей цепочки управления ИТ, которая включает:</span><span class="sxs-lookup"><span data-stu-id="b9a69-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="b9a69-136">Различные типы инцидентов безопасности, обнаруженных в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b9a69-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="b9a69-137">Сводные сведения из центрального журнала инцидентов безопасности, таких как количество обнаруженных инцидентов.</span><span class="sxs-lookup"><span data-stu-id="b9a69-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="b9a69-138">Тенденции оповещений и их устранение</span><span class="sxs-lookup"><span data-stu-id="b9a69-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="b9a69-139">Последние тенденции циберсекурити</span><span class="sxs-lookup"><span data-stu-id="b9a69-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="b9a69-140">Рекомендации по изменению политики безопасности Cloud App в Office 365 и их влиянии на конечных пользователей</span><span class="sxs-lookup"><span data-stu-id="b9a69-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="b9a69-141">Действия после прохождения времени после развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b9a69-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="b9a69-142">Если время, прошедшее с момента первоначальной настройки или обслуживания политик безопасности облачных приложений Office 365, прошло успешно, выполните следующие действия, чтобы вернуться к конфигурации, которая отражает цели безопасности Организации и текущие возможности Office 365 Cloud App Security:</span><span class="sxs-lookup"><span data-stu-id="b9a69-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="b9a69-143">Определите дату последнего изменения конфигурации для Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="b9a69-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="b9a69-144">Ознакомьтесь с текущей конфигурацией безопасности облачных приложений Office 365 и при необходимости настройте эти политики.</span><span class="sxs-lookup"><span data-stu-id="b9a69-144">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed.</span></span> <span data-ttu-id="b9a69-145">Например, убедитесь, что вы знаете, куда отправляются оповещения по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="b9a69-145">For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="b9a69-146">Узнайте [о новых возможноСтях office 365 Cloud App Security](new-in-office-365-cas.md) для изменений продуктов с момента последней настройки безопасности облачных приложений Office 365.</span><span class="sxs-lookup"><span data-stu-id="b9a69-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="b9a69-147">Выполните анализ оповещений и журналов Office 365 Cloud App Security для выявления аномалий и анализа тенденций.</span><span class="sxs-lookup"><span data-stu-id="b9a69-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="b9a69-148">Проверьте тенденции отраслевых циберсекурити, чтобы узнать о новейших угрозах безопасности.</span><span class="sxs-lookup"><span data-stu-id="b9a69-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="b9a69-149">Выполните анализ изменений, которые необходимо внести в текущий набор политик безопасности облачных приложений Office 365.</span><span class="sxs-lookup"><span data-stu-id="b9a69-149">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies.</span></span> <span data-ttu-id="b9a69-150">Включение изменений в функции безопасности облачных приложений Office 365, текущих аномалий и тенденций циберсекурити.</span><span class="sxs-lookup"><span data-stu-id="b9a69-150">Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends.</span></span> <span data-ttu-id="b9a69-151">Рекомендации по изменению существующих политик или созданию новых политик.</span><span class="sxs-lookup"><span data-stu-id="b9a69-151">Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="b9a69-152">Создайте план для реализации изменений политики.</span><span class="sxs-lookup"><span data-stu-id="b9a69-152">Make a plan for implementing the policy changes.</span></span> <span data-ttu-id="b9a69-153">Обмен данными (соЦиализе) о последствиях предполагаемых изменений для конечных пользователей в случае необходимости.</span><span class="sxs-lookup"><span data-stu-id="b9a69-153">Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="b9a69-154">Реализация изменений в политике безопасности облачного приложения Office 365.</span><span class="sxs-lookup"><span data-stu-id="b9a69-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="b9a69-155">Отслеживание отзывов конечных пользователей и оповещений системы безопасности облачного приложения Office 365 и Настройка политик с течением времени.</span><span class="sxs-lookup"><span data-stu-id="b9a69-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="b9a69-156">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="b9a69-156">Next steps</span></span>

- [<span data-ttu-id="b9a69-157">Исследование действия</span><span class="sxs-lookup"><span data-stu-id="b9a69-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="b9a69-158">ПриОстановка или восстановление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="b9a69-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="b9a69-159">Управление приложениями OAuth</span><span class="sxs-lookup"><span data-stu-id="b9a69-159">Manage OAuth apps</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="b9a69-160">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b9a69-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="b9a69-161">Просмотр списка поддерживаемых [журналов веб-трафика и источников данных](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="b9a69-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

