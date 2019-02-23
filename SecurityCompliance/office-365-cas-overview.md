---
title: Обзор Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'Office 365 Cloud App Security предоставляет вам информацию о подозрительных действиях в Office 365, чтобы можно было исследовать потенциально проблематичные ситуации и при необходимости предпринять меры по устранению проблем с безопасностью. '
ms.openlocfilehash: 974858a547d9af2db600f9856efbce619a3b38e4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220179"
---
# <a name="overview-of-office-365-cloud-app-security"></a><span data-ttu-id="904b6-103">Обзор Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-103">Overview of Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="904b6-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="904b6-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="904b6-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="904b6-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="904b6-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="904b6-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="904b6-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="904b6-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="904b6-108">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="904b6-108">You are here!</span></span>  <br/> [<span data-ttu-id="904b6-109">Следующее действие</span><span class="sxs-lookup"><span data-stu-id="904b6-109">Next step</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="904b6-110">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="904b6-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="904b6-111">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="904b6-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="904b6-112">Начало использования</span><span class="sxs-lookup"><span data-stu-id="904b6-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="904b6-p101">Office 365 Cloud App Security доступен в Office 365 корпоративный "~". Если ваша организация использует другую подписку на Office 365 Enterprise, можно приобрести надстройку Office 365 для облачных приложений. в центре администрирования Office 365 (как глобальный администратор) выберите пункт **подписки**на надстройки для **выставления счетов** \> . Дополнительные сведения см. в статье [office 365 Platform Service Description: центр соответствия &amp; требованиям безопасности Office 365](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) и [приобретение или изменение надстройки для Office 365 для бизнеса](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on).</span><span class="sxs-lookup"><span data-stu-id="904b6-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on).</span></span> 
  
<span data-ttu-id="904b6-p102">Office 365 Cloud App Security предоставляет представление о подозрительных действиях в Office 365, позволяющих исследовать проблемы, которые могут вызывать проблемы, и при необходимости предпринимать меры по устранению проблем с безопасностью. С помощью Office 365 Cloud App Security вы можете получать уведомления о вызываемых оповещениях о нетипичных или подозрительных действиях, просмотре доступа к данным в Office 365 и их использование, приостановка учетных записей пользователей с подозрительными действиями и потребовать Пользователи могут снова выполнить вход в приложения Office 365 после запуска оповещения. В этой статье приводятся общие сведения о функциях и возможностях Cloud App Security для Office 365.</span><span class="sxs-lookup"><span data-stu-id="904b6-p102">Office 365 Cloud App Security gives you insight into suspicious activity in Office 365 so you can investigate situations that are potentially problematic and, if needed, take action to address security issues. With Office 365 Cloud App Security, you can receive notifications of triggered alerts for atypical or suspicious activities, see how your organization's data in Office 365 is accessed and used, suspend user accounts exhibiting suspicious activity, and require users to log back in to Office 365 apps after an alert has been triggered. Read this article to get an overview of Office 365 Cloud App Security features and capabilities.</span></span>
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="904b6-119">Как найти портал Cloud App Security для Office 365</span><span class="sxs-lookup"><span data-stu-id="904b6-119">How to find the Office 365 Cloud App Security portal</span></span>

> [!NOTE]
> <span data-ttu-id="904b6-p103">Для доступа к порталу Cloud App Security (Office 365) необходимо быть глобальным администратором Office 365, администратором безопасности или средством чтения безопасности. Чтобы узнать больше, ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="904b6-p103">To access the Office 365 Cloud App Security portal, you must be an Office 365 global administrator, security administrator, or security reader. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
<span data-ttu-id="904b6-122">Вы можете перейти на портал Office 365 Cloud App Security, перейдя по [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) адресу и войдя в систему.</span><span class="sxs-lookup"><span data-stu-id="904b6-122">You can get to the Office 365 Cloud App Security portal by going to [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) and signing in.</span></span> 

<span data-ttu-id="904b6-p104">Вы также можете получить его из центра безопасности &amp; Office 365. Вот один хороший способ выполнения этой задачи:</span><span class="sxs-lookup"><span data-stu-id="904b6-p104">You can also get there from the Office 365 Security &amp; Compliance Center. Here's one good way to do it:</span></span>
  
1. <span data-ttu-id="904b6-p105">Перейдите к [https://protection.office.com](https://protection.office.com) рабочей или учебной учетной записи Office 365 и войдите в нее с помощью рабочей или учебной учетной записи. (Откроется центр соответствия требованиям безопасности &amp; .)</span><span class="sxs-lookup"><span data-stu-id="904b6-p105">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span>
    
2. <span data-ttu-id="904b6-127">В центре безопасности &amp; и соответствия требованиям выберите **оповещения** \> **Управление расширенными оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="904b6-127">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span> <br/><span data-ttu-id="904b6-128">![Выберите Управление расширенными оповещениями, чтобы перейти к Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="904b6-128">![Choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="904b6-129">(Если приложение Office 365 Cloud App Security еще не включено, и вы являетесь глобальным администратором, [включите Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span><span class="sxs-lookup"><span data-stu-id="904b6-129">(If Office 365 Cloud App Security is not yet enabled, and you are a global administrator, [turn on Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span></span>
    
3. <span data-ttu-id="904b6-130">Выберите **Перейти к Office 365 Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="904b6-130">Choose **Go to Office 365 Cloud App Security**.</span></span> 
    
## <a name="policies"></a><span data-ttu-id="904b6-131">Политики.</span><span class="sxs-lookup"><span data-stu-id="904b6-131">Policies</span></span>

<span data-ttu-id="904b6-p106">Office 365 Cloud App Security работает с политиками, определенными для Организации. В Office 365 Cloud App Security организация получает множество стандартных политик обнаружения аномалий и несколько шаблонов для политик действий. Эти политики предназначены для обнаружения общих аномалий, идентификации пользователей, которые входят в систему с опасного IP-адреса, обнаружения действий, выполняемых программой-шантажистом, обнаружения действий администратора с некорпоративных IP-адресов и многого другого.</span><span class="sxs-lookup"><span data-stu-id="904b6-p106">Office 365 Cloud App Security works with the policies that are defined for your organization. With Office 365 Cloud App Security, your organization gets many predefined anomaly detection policies and several templates for activity policies. These policies are designed to detect general anomalies, identify users logging in from a risky IP address, detect ransomware activities, detect administrator activities from non-corporate IP addresses, and more.</span></span>
  
![На портале CAS выберите пункт Шаблоны \> элементов управления для просмотра или создания шаблонов политик](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
<span data-ttu-id="904b6-136">чтобы просмотреть или использовать шаблоны политик, на портале Cloud App Security (Office 365) перейдите на страницу **шаблоны** **элементов управления** \> .</span><span class="sxs-lookup"><span data-stu-id="904b6-136">To view/use policy templates, in the Office 365 Cloud App Security portal, go to **Control** \> **Templates**.</span></span> 
  
![На портале Office 365 CAS выберите элемент Управление](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
<span data-ttu-id="904b6-138">Чтобы узнать больше о политиках, ознакомьтесь со следующими материалами:</span><span class="sxs-lookup"><span data-stu-id="904b6-138">To learn more about policies, see the following resources:</span></span>
  
- [<span data-ttu-id="904b6-139">Политики действий и оповещения в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-139">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="904b6-140">Политики обнаружения аномалий в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-140">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a><span data-ttu-id="904b6-141">Оповещения</span><span class="sxs-lookup"><span data-stu-id="904b6-141">Alerts</span></span>

<span data-ttu-id="904b6-p107">При определении политик оповещения уведомляют о подозрительных или нетипичных действиях, которые были обнаружены. Чтобы просмотреть оповещения для Организации, нажмите кнопку **оповещения** на панели навигации в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="904b6-p107">When policies are defined, alerts notify you about suspicious or atypical activities that were detected. To view alerts for your organization, choose **Alerts** in the navigation bar across the top of the screen.</span></span> 
  
![На странице оповещения можно просмотреть оповещения, которые были активированы, и все выполненные действия.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
<span data-ttu-id="904b6-p108">По мере активации оповещений вы можете просмотреть их, чтобы узнать больше о том, что происходит. Затем, если действие все еще подозрительно, вы можете предпринять действия. Например, вы можете уведомить пользователя о возникшей ошибке, приостановить вход пользователя в Office 365 или потребовать от пользователя войти в приложение Office 365.</span><span class="sxs-lookup"><span data-stu-id="904b6-p108">As alerts are triggered you can review them to learn more about what is going on. Then, if the activity is still suspicious, you can take action. For example, you can notify a user about an issue, suspend a user from signing in to Office 365, or require a user to sign back in to Office 365 apps.</span></span>
  
<span data-ttu-id="904b6-148">Дополнительные сведения об оповещениях можно найти в следующих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="904b6-148">To learn more about alerts, see the following resources:</span></span>
  
- [<span data-ttu-id="904b6-149">Политики действий и оповещения в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-149">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="904b6-150">Политики обнаружения аномалий в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-150">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="904b6-151">Проверка оповещений системы безопасности облачного приложения Office 365 и выполнение действий с ними</span><span class="sxs-lookup"><span data-stu-id="904b6-151">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a><span data-ttu-id="904b6-152">Журналы активности</span><span class="sxs-lookup"><span data-stu-id="904b6-152">Activity logs</span></span>

<span data-ttu-id="904b6-153">Просмотр сведений о действиях пользователей на странице журнала активности в Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="904b6-153">View information about user activities on your Activity log page in Office 365 Cloud App Security.</span></span>
  
![На портале Office 365 CAS выберите пункт \> исследование журнала активности](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
<span data-ttu-id="904b6-155">чтобы перейти на эту страницу, на портале Cloud App Security (Office 365) перейдите к разделу **исследование** \> **журнала активности**.</span><span class="sxs-lookup"><span data-stu-id="904b6-155">To get to this page, in the Office 365 Cloud App Security portal, go to **Investigate** \> **Activity log**.</span></span> 
  
![На портале Office 365 CAS нажмите кнопку исследовать.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
<span data-ttu-id="904b6-p109">Вы также можете использовать журналы веб-трафика с Office 365 Cloud App Security. Дополнительные сведения, которые включены в эти файлы журналов, лучше отображаются в действиях пользователей. Вы можете использовать файлы журналов из Barracuda, голубого покрытия, контрольной точки, Cisco, Клавистер, Dell Сониквалл, Фортинет, шаблоны Juniper, McAfee, Microsoft, Palo Alto, Софос, Скуид, вебсенце, Зскалер и т. д.</span><span class="sxs-lookup"><span data-stu-id="904b6-p109">You can use your web traffic logs with Office 365 Cloud App Security, too. The more details that are included in those log files, the better visibility you'll have into user activity. You can use log files from Barracuda, Blue Coat, Check Point, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, Squid, Websence, Zscaler, and more.</span></span>
  
[<span data-ttu-id="904b6-160">Сведения о журналах веб-трафика и источниках данных для Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-160">Learn about web traffic logs and data sources for Office 365 Cloud App Security</span></span>](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="oauth-apps"></a><span data-ttu-id="904b6-161">Приложения OAuth</span><span class="sxs-lookup"><span data-stu-id="904b6-161">OAuth apps</span></span>

<span data-ttu-id="904b6-162">С помощью Office 365 Cloud App Security вы можете разрешить или запретить пользователям в Организации использовать сторонние приложения, обращающиеся к данным в Office 365.</span><span class="sxs-lookup"><span data-stu-id="904b6-162">With Office 365 Cloud App Security, you can allow or prevent people in your organization to use third-party apps that access data in Office 365.</span></span>
  
![В ЦС O365 можно получить доступ к странице "Управление приложениями OAuth" в меню "исследование".](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
<span data-ttu-id="904b6-164">Чтобы перейти на эту страницу, перейдите к разделу **изучение** \> **приложений OAuth**.</span><span class="sxs-lookup"><span data-stu-id="904b6-164">To get to this page, go to **Investigate** \> **OAuth apps**.</span></span> 
  
![На портале Office 365 CAS нажмите кнопку исследовать.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[<span data-ttu-id="904b6-166">Управление приложениями OAuth с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-166">Manage OAuth apps using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a><span data-ttu-id="904b6-167">Панель мониторинга облачного обнаружения</span><span class="sxs-lookup"><span data-stu-id="904b6-167">Cloud Discovery Dashboard</span></span>

<span data-ttu-id="904b6-p110">**Панель мониторинга облачНого обнаружения**, также называемая **приложением для работы**с производительностью, отображает сведения об использовании облачных приложений в Организации. Эту панель мониторинга можно использовать для просмотра сведений о приложениях, пользователях, трафике, транзакциях и других возможностях. Панель мониторинга облачного обнаружения напоминает следующее изображение:</span><span class="sxs-lookup"><span data-stu-id="904b6-p110">The **Cloud Discovery Dashboard**, also referred to as **Productivity App Discovery**, shows information about cloud app usage within your organization. You can view information about apps, users, traffic, transactions, and more using this dashboard. The Cloud Discovery Dashboard resembles the following image:</span></span> 
  
![На портале Office 365 CAS выберите пункт Обнаружение \> облачной панели мониторинга](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="904b6-172">чтобы открыть эту информационную панель, на портале cloud App Security (Office 365) перейдите на страницу **обнаружение** \> **облачной панели мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="904b6-172">To get to this dashboard, in the Office 365 Cloud App Security portal, go to **Discover** \> **Cloud Discovery dashboard**.</span></span> 
  
![На портале Office 365 CAS нажмите кнопку Обнаружение](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[<span data-ttu-id="904b6-174">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-174">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a><span data-ttu-id="904b6-175">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="904b6-175">Next steps</span></span>

- <span data-ttu-id="904b6-176">Получение [вариантов использования и руководство по использованию Cloud App Security для Office 365](https://aka.ms/O365CASGuide)</span><span class="sxs-lookup"><span data-stu-id="904b6-176">Get the [Office 365 Cloud App Security Use Cases and Usage Guide](https://aka.ms/O365CASGuide)</span></span>
    
- [<span data-ttu-id="904b6-177">Подготовка к использованию Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="904b6-177">Get ready for Office 365 Cloud App Security</span></span>](get-ready-for-office-365-cas.md)
    

