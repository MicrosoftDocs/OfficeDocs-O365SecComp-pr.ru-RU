---
title: Обзор Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 81f0ee9a-9645-45ab-ba56-de9cbccab475
description: 'Безопасности облаке приложения Office 365 предоставляет представление о подозрительных активности в Office 365, поэтому могут исследовать ситуаций, которые являются проблемы и при необходимости выполнять действия по устранению проблем безопасности. '
ms.openlocfilehash: 84d5b412b62bf113101d6322032f3b643d87d741
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534573"
---
# <a name="overview-of-office-365-cloud-app-security"></a><span data-ttu-id="aa0a2-103">Обзор Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="aa0a2-103">Overview of Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="aa0a2-104">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="aa0a2-104">****Evaluation** \>**</span></span>|<span data-ttu-id="aa0a2-105">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="aa0a2-105">****Planning** \>**</span></span>|<span data-ttu-id="aa0a2-106">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="aa0a2-106">****Deployment** \>**</span></span>|<span data-ttu-id="aa0a2-107">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="aa0a2-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aa0a2-108">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="aa0a2-108">You are here!</span></span>  <br/> [<span data-ttu-id="aa0a2-109">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="aa0a2-109">Next step</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="aa0a2-110">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="aa0a2-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="aa0a2-111">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="aa0a2-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="aa0a2-112">Начать использование</span><span class="sxs-lookup"><span data-stu-id="aa0a2-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="aa0a2-p101">Безопасности приложения Office 365 облаке доступна в Office 365 корпоративный E5. Если ваша организация использует другой подписки Office 365 для предприятия, облачных приложений Office 365 безопасности можно приобрести в виде дополнительного компонента. (Как глобальный администратор, в центре администрирования Office 365 нажмите кнопку **выставления счетов** \> **Добавить подписок**.) Дополнительные сведения можно [Описание платформы Office 365: безопасность Office 365 &amp; центре соответствия требованиям](https://technet.microsoft.com/en-us/library/dn933793.aspx) и [покупке и изменить надстройки для Office 365 для бизнеса](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="aa0a2-p102">Безопасности облаке приложения Office 365 предоставляет вам понимание подозрительные действия в Office 365, могут исследовать ситуаций, которые являются проблемы и при необходимости выполнять действия по устранению проблем безопасности. Office 365 облачных приложений безопасности можно получать уведомления о включаемая оповещений для необычных или подозрительные операций, см вашей организации в Office 365 — это получить доступ и данных используется, приостановить ящиков подозрительные действия учетных записей пользователей и требуют Пользователи, чтобы войти в Office 365 приложениям запускаться оповещение. В этой статье Обзор безопасности приложения Office 365 облачных функций и возможностей.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p102">Office 365 Cloud App Security gives you insight into suspicious activity in Office 365 so you can investigate situations that are potentially problematic and, if needed, take action to address security issues. With Office 365 Cloud App Security, you can receive notifications of triggered alerts for atypical or suspicious activities, see how your organization's data in Office 365 is accessed and used, suspend user accounts exhibiting suspicious activity, and require users to log back in to Office 365 apps after an alert has been triggered. Read this article to get an overview of Office 365 Cloud App Security features and capabilities.</span></span>
  
    
## <a name="how-to-find-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="aa0a2-119">Как найти портала Office 365 облачных приложений безопасности</span><span class="sxs-lookup"><span data-stu-id="aa0a2-119">How to find the Office 365 Cloud App Security portal</span></span>

> [!NOTE]
> <span data-ttu-id="aa0a2-p103">Для доступа к порталу Office 365 облачных приложений безопасности, необходимо быть глобальным администратором, администратор безопасности или безопасности чтения. Чтобы получить дополнительные сведения, обратитесь к разделу [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p103">To access the Office 365 Cloud App Security portal, you must be a global administrator, security administrator, or security reader. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
<span data-ttu-id="aa0a2-p104">Можно получить на портале облачных приложений Office 365 безопасности через безопасности Office 365 &amp; центре соответствия требованиям. Вот хороший способ сделать это:</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p104">You can get to the Office 365 Cloud App Security portal through the Office 365 Security &amp; Compliance Center. Here's one good way to do it:</span></span>
  
1. <span data-ttu-id="aa0a2-p105">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы для Office 365. (Вы перейдете к безопасности &amp; центре соответствия требованиям.)</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p105">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="aa0a2-126">В разделе Безопасность &amp; центре соответствия требованиям, выберите **оповещения** \> **Расширенное Управление оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-126">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span> 
    
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите дополнительные оповещения для перехода к безопасности Office 365 облаке приложения](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    <span data-ttu-id="aa0a2-128">(Если еще не включено приложения облаке Безопасность в Office 365, и глобальный администратор, [Включите безопасности приложения Office 365 облачных](turn-on-office-365-cas.md).)</span><span class="sxs-lookup"><span data-stu-id="aa0a2-128">(If Office 365 Cloud App Security is not yet enabled, and you are a global administrator, [turn on Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span></span>
    
3. <span data-ttu-id="aa0a2-129">Выберите, **перейдите к безопасности приложения Office 365 облака**.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-129">Choose **Go to Office 365 Cloud App Security**.</span></span> 
    
## <a name="policies"></a><span data-ttu-id="aa0a2-130">Политики.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-130">Policies</span></span>

<span data-ttu-id="aa0a2-p106">Office 365 безопасности приложения облачных работает с политиками, определенных для вашей организации. С помощью Office 365 облачных приложений безопасность вашей организации получает 10 политик обнаружения неполадок предварительно заданных и несколько шаблонов для действия политики. Эти политики предназначены для обнаружения Общие ошибки, определение пользователей, ведение журналов в с рискованный IP-адреса, обнаруживать ransomware действий, обнаруживать действий администратора для индивидуальных IP-адресов и многое другое.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p106">Office 365 Cloud App Security works with the policies that are defined for your organization. With Office 365 Cloud App Security, your organization gets 10 predefined anomaly detection policies and several templates for activity policies. These policies are designed to detect general anomalies, identify users logging in from a risky IP address, detect ransomware activities, detect administrator activities from non-corporate IP addresses, and more.</span></span>
  
![На портале управления доступом для кода нажмите элемент управления \> шаблонов для просмотра или создания шаблонов политики](media/88f615b4-aa8a-480c-b239-323dfcd628e1.png)
  
<span data-ttu-id="aa0a2-135">Просмотр или использовать шаблоны политики на портале облачных приложений Office 365 безопасность, перейдите к **управления** \> **шаблонов**.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-135">To view/use policy templates, in the Office 365 Cloud App Security portal, go to **Control** \> **Templates**.</span></span> 
  
![На портале O365 сервера клиентского доступа нажмите элемент управления](media/287c2ea9-5172-4697-8e0e-b9ab654105bc.png)
  
<span data-ttu-id="aa0a2-137">Для получения дополнительных сведений о политиках, можно найти в следующих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="aa0a2-137">To learn more about policies, see the following resources:</span></span>
  
- [<span data-ttu-id="aa0a2-138">Политики действий и оповещения в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="aa0a2-138">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="aa0a2-139">Политики обнаружения аномалий в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="aa0a2-139">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
## <a name="alerts"></a><span data-ttu-id="aa0a2-140">Оповещения</span><span class="sxs-lookup"><span data-stu-id="aa0a2-140">Alerts</span></span>

<span data-ttu-id="aa0a2-p107">При определении политики оповещения о подозрительных или необычных операций, которые были обнаружены. Чтобы просмотреть оповещения для вашей организации, выберите **оповещений** в панели навигации в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p107">When policies are defined, alerts notify you about suspicious or atypical activities that were detected. To view alerts for your organization, choose **Alerts** in the navigation bar across the top of the screen.</span></span> 
  
![На странице "оповещения" можно просмотреть оповещений, которое было запущено и любые действия, предпринятые.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)
  
<span data-ttu-id="aa0a2-p108">Как оповещения запускаются их для получения дополнительных сведений о том, что происходит можно просмотреть. Затем если по-прежнему подозрительные действия может выполнять действия. К примеру может уведомлять пользователя о проблеме, отключать пользователей вход в Office 365 с или требуют пользователя для входа в приложения Office 365.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p108">As alerts are triggered you can review them to learn more about what is going on. Then, if the activity is still suspicious, you can take action. For example, you can notify a user about an issue, suspend a user from signing in to Office 365, or require a user to sign back in to Office 365 apps.</span></span>
  
<span data-ttu-id="aa0a2-147">Дополнительные сведения об оповещениях см ознакомьтесь со следующими ресурсами:</span><span class="sxs-lookup"><span data-stu-id="aa0a2-147">To learn more about alerts, see the following resources:</span></span>
  
- [<span data-ttu-id="aa0a2-148">Политики действий и оповещения в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="aa0a2-148">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="aa0a2-149">Политики обнаружения аномалий в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="aa0a2-149">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="aa0a2-150">Просмотрите и выполнение действий на оповещение системы безопасности приложения Office 365 облако</span><span class="sxs-lookup"><span data-stu-id="aa0a2-150">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    
## <a name="activity-logs"></a><span data-ttu-id="aa0a2-151">Журналы активности</span><span class="sxs-lookup"><span data-stu-id="aa0a2-151">Activity logs</span></span>

<span data-ttu-id="aa0a2-152">Просмотр сведений о действий пользователей на странице журнал активности в облаке приложения Office 365 безопасности.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-152">View information about user activities on your Activity log page in Office 365 Cloud App Security.</span></span>
  
![На портале O365 сервера клиентского доступа, нажмите кнопку Проверить \> журнала активности](media/ec19e77d-4e11-49fc-ab7c-0e8b0c29c93c.png)
  
<span data-ttu-id="aa0a2-154">Чтобы перейти к этой странице, на портале облачных приложений Office 365 безопасность перейдите к **изучению** \> **Журнал активности**.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-154">To get to this page, in the Office 365 Cloud App Security portal, go to **Investigate** \> **Activity log**.</span></span> 
  
![На портале O365 сервера клиентского доступа нажмите кнопку Проверить.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
<span data-ttu-id="aa0a2-p109">Можно использовать вашей веб-трафика журналов с Office 365 облачных приложений безопасность слишком. Дополнительные сведения, которые включены в тех файлов журнала, лучше контролировать, вам придется в действие пользователя. Файлы журнала из Barracuda, синий покрывающего, контрольной точке, Cisco, Clavister, Dell SonicWALL, Fortinet, можжевельник, McAfee, корпорация Майкрософт, Пало компьютер, Sophos, Squid, Websence, Zscaler и др., можно использовать.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p109">You can use your web traffic logs with Office 365 Cloud App Security, too. The more details that are included in those log files, the better visibility you'll have into user activity. You can use log files from Barracuda, Blue Coat, Check Point, Cisco, Clavister, Dell SonicWALL, Fortinet, Juniper, McAfee, Microsoft, Palo Alto, Sophos, Squid, Websence, Zscaler, and more.</span></span>
  
[<span data-ttu-id="aa0a2-159">Сведения о веб-трафика: источники данных и журналы для приложения облаке Безопасность в Office 365</span><span class="sxs-lookup"><span data-stu-id="aa0a2-159">Learn about web traffic logs and data sources for Office 365 Cloud App Security</span></span>](web-traffic-logs-and-data-sources-for-ocas.md)
  
## <a name="app-permissions"></a><span data-ttu-id="aa0a2-160">Разрешения для приложений</span><span class="sxs-lookup"><span data-stu-id="aa0a2-160">App permissions</span></span>

<span data-ttu-id="aa0a2-161">Office 365 облачных приложений безопасности можно разрешить или запретить людей в организации к использованию приложений сторонних производителей, доступ к данным в Office 365.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-161">With Office 365 Cloud App Security, you can allow or prevent people in your organization to use third-party apps that access data in Office 365.</span></span>
  
![В O365 сервера клиентского доступа можно получить доступ к страницы Управление разрешениями приложения из меню проверить.](media/78272cda-986f-4b3b-bbbe-8c236c74f5d3.png)
  
<span data-ttu-id="aa0a2-163">Чтобы получить доступ к этой странице, перейдите к **изучению** \> **разрешений приложения**.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-163">To get to this page, go to **Investigate** \> **App permissions**.</span></span> 
  
![На портале O365 сервера клиентского доступа нажмите кнопку Проверить.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
[<span data-ttu-id="aa0a2-165">Управление разрешениями приложений с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="aa0a2-165">Manage app permissions using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
  
## <a name="cloud-discovery-dashboard"></a><span data-ttu-id="aa0a2-166">Панель мониторинга обнаружения облако</span><span class="sxs-lookup"><span data-stu-id="aa0a2-166">Cloud Discovery Dashboard</span></span>

<span data-ttu-id="aa0a2-p110">Панели **Мониторинга обнаружения облачных**, также называются **Обнаружения повышения производительности приложения**отображаются сведения о использования облачных приложений в организации. Можно просмотреть сведения о приложениях, пользователи, трафик, транзакции и др. с помощью этой панели мониторинга. Панель мониторинга обнаружения облачных выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="aa0a2-p110">The **Cloud Discovery Dashboard**, also referred to as **Productivity App Discovery**, shows information about cloud app usage within your organization. You can view information about apps, users, traffic, transactions, and more using this dashboard. The Cloud Discovery Dashboard resembles the following image:</span></span> 
  
![На портале Office 365 CAS выберите обнаружить \> облаке обнаружения панели мониторинга](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="aa0a2-171">Для получения для этой панели мониторинга на портале облачных приложений Office 365 безопасность перейдите к **обнаружить** \> **облаке обнаружения панели мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="aa0a2-171">To get to this dashboard, in the Office 365 Cloud App Security portal, go to **Discover** \> **Cloud Discovery dashboard**.</span></span> 
  
![На портале Office 365 CAS выберите обнаружения](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
[<span data-ttu-id="aa0a2-173">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="aa0a2-173">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
  
## <a name="next-steps"></a><span data-ttu-id="aa0a2-174">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="aa0a2-174">Next steps</span></span>

- <span data-ttu-id="aa0a2-175">Получить [варианты использования безопасности Office 365 облаке приложения и руководство по использованию](https://aka.ms/O365CASGuide)</span><span class="sxs-lookup"><span data-stu-id="aa0a2-175">Get the [Office 365 Cloud App Security Use Cases and Usage Guide](https://aka.ms/O365CASGuide)</span></span>
    
- [<span data-ttu-id="aa0a2-176">Подготовка к использованию Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="aa0a2-176">Get ready for Office 365 Cloud App Security</span></span>](get-ready-for-office-365-cas.md)
    

