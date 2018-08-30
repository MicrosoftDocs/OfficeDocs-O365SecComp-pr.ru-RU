---
title: Подготовка к использованию Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: d9ee4d67-f2b3-42b4-9c9e-c4529904990a
description: Приступая к работе с Office 365 облачных приложений безопасности
ms.openlocfilehash: 906570c6607c70b63fa9d2059d56b50f7807124a
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2018
ms.locfileid: "23229991"
---
# <a name="get-ready-for-office-365-cloud-app-security"></a><span data-ttu-id="fcec5-103">Подготовка к использованию Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fcec5-103">Get ready for Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="fcec5-104">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="fcec5-104">****Evaluation** \>**</span></span>|<span data-ttu-id="fcec5-105">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="fcec5-105">****Planning** \>**</span></span>|<span data-ttu-id="fcec5-106">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="fcec5-106">****Deployment** \>**</span></span>|<span data-ttu-id="fcec5-107">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="fcec5-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="fcec5-108">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="fcec5-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |<span data-ttu-id="fcec5-109">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="fcec5-109">You are here!</span></span>  <br/> [<span data-ttu-id="fcec5-110">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="fcec5-110">Next step</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="fcec5-111">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="fcec5-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |[<span data-ttu-id="fcec5-112">Начать использование</span><span class="sxs-lookup"><span data-stu-id="fcec5-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="fcec5-p101">При подготовке и реализации Office 365 облачных приложений безопасности (ранее называлась расширенного управления безопасностью) для вашей организации есть необходимо принять во внимание на несколько моментов. Используйте эту статью в качестве руководства по планированию для Office 365 облачных приложений безопасности.</span><span class="sxs-lookup"><span data-stu-id="fcec5-p101">As you prepare to turn on and implement Office 365 Cloud App Security (formerly known as Advanced Security Management) for your organization, there are a few things to take into account. Use this article as a guide to plan for Office 365 Cloud App Security.</span></span>
    
## <a name="step-1-identify-and-protect-your-global-and-security-administrator-accounts"></a><span data-ttu-id="fcec5-115">Шаг 1: Определение и защиты учетных записей администратора глобальные и безопасность</span><span class="sxs-lookup"><span data-stu-id="fcec5-115">Step 1: Identify and protect your global and security administrator accounts</span></span>

<span data-ttu-id="fcec5-p102">Глобальных администраторов, администраторов безопасности и читатели безопасности можно доступа к порталу Office 365 облачных приложений безопасности для просмотра политик, просмотрите оповещения и использовать отчеты. Глобальный администраторов и администраторов безопасности можно определить политик и других действий для защиты своей организации. (Дополнительные сведения можно [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).) Просмотрите учетные записи пользователей вашей организации с повышенными правами в качестве меры предосторожности.</span><span class="sxs-lookup"><span data-stu-id="fcec5-p102">Global administrators, security administrators, and security readers can access the Office 365 Cloud App Security portal to view policies, review alerts, and use reports. Global administrators and security administrators can define policies and take other actions to protect your organization. (For more information, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).) Review your organization's user accounts that have elevated permissions as a precaution.</span></span> 
  
 <span data-ttu-id="fcec5-119">**[Учетные записи глобального администратора защитить Office 365](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**.</span><span class="sxs-lookup"><span data-stu-id="fcec5-119">**[Protect your Office 365 global administrator accounts](https://docs.microsoft.com/office365/enterprise/protect-your-global-administrator-accounts)**.</span></span> 
  
## <a name="step-2-turn-on-audit-logging-for-your-organization"></a><span data-ttu-id="fcec5-120">Шаг 2: Включение ведения журнала аудита для вашей организации</span><span class="sxs-lookup"><span data-stu-id="fcec5-120">Step 2: Turn on audit logging for your organization</span></span>

<span data-ttu-id="fcec5-p103">Чтобы безопасности Office 365 облаке приложения для работы правильные ведение журнала аудита может быть включена. Обычно это делается путем глобальный администратор или администратор Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="fcec5-p103">In order for Office 365 Cloud App Security to work correct, audit logging must be turned on. This is typically done by an Exchange Online administrator or a global administrator.</span></span>
  
 <span data-ttu-id="fcec5-123">**[Включить Office 365 проводить аудит операций поиска журнала включено или отключено](turn-audit-log-search-on-or-off.md)**.</span><span class="sxs-lookup"><span data-stu-id="fcec5-123">**[Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md)**.</span></span> 
  
## <a name="step-3-go-to-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="fcec5-124">Шаг 3: Перейдите к порталу Office 365 облачных приложений безопасности</span><span class="sxs-lookup"><span data-stu-id="fcec5-124">Step 3: Go to the Office 365 Cloud App Security portal</span></span>

1. <span data-ttu-id="fcec5-p104">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы для Office 365. (Вы перейдете к безопасности &amp; центре соответствия требованиям.)</span><span class="sxs-lookup"><span data-stu-id="fcec5-p104">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="fcec5-127">Последовательно выберите пункты **оповещения** \> **Управление расширенного оповещения**.</span><span class="sxs-lookup"><span data-stu-id="fcec5-127">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="fcec5-128">Выберите, **перейдите к безопасности приложения Office 365 облачных** переход на портале облачных приложений Office 365 безопасности.</span><span class="sxs-lookup"><span data-stu-id="fcec5-128">Choose **Go to Office 365 Cloud App Security** to go to the Office 365 Cloud App Security portal.</span></span> 
    
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите дополнительные оповещения для перехода к безопасности Office 365 облаке приложения](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    <span data-ttu-id="fcec5-130">При переходе к порталу Office 365 облачных приложений безопасности первой страницы, отображаемые приведен на странице политики, которая выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fcec5-130">When you go to the Office 365 Cloud App Security portal, the first page you see is the Policies page, which resembles the following image:</span></span>
    
    ![При переходе к порталу Office 365 облачных приложений безопасности, запустите со страницей политик](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
## <a name="step-4-define-policies-and-set-up-alerts-amp-actions"></a><span data-ttu-id="fcec5-132">Шаг 4: Определение политики и настройка оповещений &amp; действия</span><span class="sxs-lookup"><span data-stu-id="fcec5-132">Step 4: Define policies and set up alerts &amp; actions</span></span>

<span data-ttu-id="fcec5-p105">Глобальный администраторов и администраторов безопасности определить политики безопасности Office 365 облачных приложений. Во время процесса определения политик оповещений и действий также необходимо задать. Оповещение — это уведомление на основе критериев, который отображается в представлении или отправки по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="fcec5-p105">Global administrators and security administrators define policies in Office 365 Cloud App Security. During the process of defining policies, alerts and actions are also set. An alert is a criteria-based notification that appears in a view or is sent via email.</span></span> 
  
<span data-ttu-id="fcec5-p106">Существует два типа оповещения в облаке приложения Office 365 безопасности: оповещения обнаружения неполадок, которые обнаруживать подозрительные действия и предупреждения действия, которые определены для действия, которые могут быть необычных для вашей организации. Оповещения глобальных администраторов и администраторов безопасности при отсутствии активности в среде Office 365, нестандартный для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="fcec5-p106">There are two types of alerts in Office 365 Cloud App Security: anomaly detection alerts that detect suspicious activity, and activity alerts, which are defined for activities that might be atypical for your organization. Alerts notify global administrators and security administrators when there's an activity in your Office 365 environment that's unusual for your organization.</span></span>
  
<span data-ttu-id="fcec5-138">Воспользуйтесь следующими ресурсами для получения дополнительных сведений:</span><span class="sxs-lookup"><span data-stu-id="fcec5-138">See the following resources to learn more:</span></span>
  
- [<span data-ttu-id="fcec5-139">Политики действий и оповещения в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fcec5-139">Activity policies and alerts in Office 365 Cloud App Security</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="fcec5-140">Политики обнаружения аномалий в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fcec5-140">Anomaly detection policies in Office 365 Cloud App Security</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="fcec5-141">Просмотрите и выполнение действий на оповещение системы безопасности приложения Office 365 облако</span><span class="sxs-lookup"><span data-stu-id="fcec5-141">Review and take action on Office 365 Cloud App Security alerts</span></span>](review-office-365-cas-alerts.md)
    
## <a name="step-5-learn-about-your-organizations-cloud-usage"></a><span data-ttu-id="fcec5-142">Шаг 5: Сведения об использовании облачных вашей организации</span><span class="sxs-lookup"><span data-stu-id="fcec5-142">Step 5: Learn about your organization's cloud usage</span></span>

<span data-ttu-id="fcec5-p107">Как глобальный администратор, администратор безопасности или безопасности чтения могут узнать о использования облака в организации через отчеты и панели мониторинга обнаружения облака (также называемая обнаружения повышения производительности приложения). Эту панель мониторинга показывает сведения о пользователях, приложения, веб-трафика и определенными уровнями риска.</span><span class="sxs-lookup"><span data-stu-id="fcec5-p107">As a global administrator, security administrator, or security reader, you can learn about your organization's cloud usage through reports and a Cloud Discovery dashboard (also called Productivity App Discovery). This dashboard shows information about users, apps, web traffic, and risk levels.</span></span>
  
![На портале Office 365 CAS выберите обнаружить \> облаке обнаружения панели мониторинга](media/61269290-fd82-4d4b-8045-aea1ebc82287.png)
  
<span data-ttu-id="fcec5-146">Переход на панели мониторинга производительности приложения обнаружения на портале облачных приложений Office 365 безопасности выберите **обнаружить** \> **облаке обнаружения панели мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="fcec5-146">To go to the Productivity App Discovery dashboard, in the Office 365 Cloud App Security portal, choose **Discover** \> **Cloud Discovery dashboard**.</span></span>
  
![На портале Office 365 CAS выберите обнаружения](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
<span data-ttu-id="fcec5-p108">Для заполнения отчетов с помощью информацию, необходимую отправьте файлы журнала из вашей организации брандмауэров и прокси-серверы. Дополнительные сведения, можно найти в следующих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="fcec5-p108">To populate reports with the information you need, upload your log files from your organization's firewalls and proxies. To learn more, see the following resources:</span></span>
  
- [<span data-ttu-id="fcec5-150">Создание отчетов обнаружения приложения в облаке приложения Office 365 безопасности</span><span class="sxs-lookup"><span data-stu-id="fcec5-150">Create app discovery reports in Office 365 Cloud App Security</span></span>](create-app-discovery-reports-in-ocas.md)
    
- [<span data-ttu-id="fcec5-151">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fcec5-151">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
## <a name="step-6-manage-apps-that-your-organization-is-using-to-access-office-365"></a><span data-ttu-id="fcec5-152">Шаг 6: Управление приложениями, которые ваша организация использует для доступа к Office 365</span><span class="sxs-lookup"><span data-stu-id="fcec5-152">Step 6: Manage apps that your organization is using to access Office 365</span></span>

<span data-ttu-id="fcec5-p109">Как глобальный администратор или администратор безопасности могут управлять приложений, таких как настраиваемые приложения или приложения сторонних производителей, использующих сотрудникам вашей организации на устройствах с Office 365. Например, предположим, что кто-то загруженные настраиваемые приложения, которые требуется использовать с Office 365. Просмотрите приложения, которые пользователи используют, bПричиной уязвимости является ненадежные приложения или Пометка приложения как Утверждено для ваших целей отслеживания. [Управление разрешениями приложения с помощью приложения облаке Безопасность в Office 365](manage-app-permissions-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="fcec5-p109">As a global administrator or security administrator, you can manage apps, such as custom apps or third-party apps, that people in your organization are using on their devices with Office 365. For example, suppose that someone has downloaded a custom app they want to use with Office 365. You can review the apps people are using, ban untrusted apps, or mark apps as approved for your tracking purposes. [Manage app permissions using Office 365 Cloud App Security](manage-app-permissions-in-ocas.md).</span></span>
  
## <a name="step-7-use-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="fcec5-157">Шаг 7: Используйте сервер SIEM с Office 365 облачных приложений безопасности</span><span class="sxs-lookup"><span data-stu-id="fcec5-157">Step 7: Use your SIEM server with Office 365 Cloud App Security</span></span>

<span data-ttu-id="fcec5-p110">Организации с помощью на сервере безопасности сведения и события управления (SIEM)? Office 365 безопасности приложения облачных теперь можно интегрировать с сервера SIEM для включения централизованного мониторинга оповещения. Интеграция со службой SIEM позволяет лучше защитить облачных приложений при обслуживание обычным безопасности рабочего процесса, автоматизации процедуры безопасности и сопоставления между облачной и локальной события. Агент SIEM выполняется на сервере, извлекает оповещений из приложения облаке Безопасность в Office 365 и отправляет эти оповещения на сервере SIEM. В разделе [SIEM интеграции с Office 365 облачных приложений безопасности](integrate-your-siem-server-with-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="fcec5-p110">Is your organization using a security information and event management (SIEM) server? Office 365 Cloud App Security can now integrate with your SIEM server to enable centralized monitoring of alerts. Integrating with a SIEM service allows you to better protect your cloud applications while maintaining your usual security workflow, automating security procedures and correlating between cloud-based and on-premises events. The SIEM agent runs on your server, pulls alerts from Office 365 Cloud App Security, and streams those alerts into your SIEM server. See [SIEM integration with Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="fcec5-163">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="fcec5-163">Next steps</span></span>

- [<span data-ttu-id="fcec5-164">Включение Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fcec5-164">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
- <span data-ttu-id="fcec5-165">Попробуйте наших [Руководство по лаборатории тестирования](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) для практические навыки, где демонстрация мощных возможностях безопасности Office 365 облаке приложения и создание пробной версии.</span><span class="sxs-lookup"><span data-stu-id="fcec5-165">Try our [Test Lab Guide](https://docs.microsoft.com/office365/enterprise/cloud-app-security-for-your-office-365-dev-test-environment) for a hands-on experience where you can demonstrate the powerful features of Office 365 Cloud App Security and create a proof of concept.</span></span> 
    

