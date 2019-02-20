---
title: Просмотр результатов обнаружения приложений в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Обзор отчетов обнаружения приложений в Office 365 Cloud App Security поможет вам узнать больше об использовании облачных приложений для пользователей в вашей организации. После создания отчетов об обнаружении приложений с помощью файлов журнала, полученных от брандмауэров и прокси-серверов, просмотрите результаты в панели мониторинга обнаружения приложений.
ms.openlocfilehash: fa5ab7c6cd734feb26878cf1a97f7ce708aa1478
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087338"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="f376a-104">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="f376a-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="f376a-105">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f376a-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="f376a-106">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f376a-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="f376a-107">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f376a-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="f376a-108">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f376a-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="f376a-109">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="f376a-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="f376a-110">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="f376a-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="f376a-111">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="f376a-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="f376a-112">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="f376a-112">You are here!</span></span>  <br/> [<span data-ttu-id="f376a-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f376a-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="f376a-p102">Панель мониторинга облачного обнаружения работает с журналами веб-трафика вашей организации, чтобы предоставить подробные сведения об использовании облачных приложений. Если вы являетесь глобальным администратором, администратором безопасности или средством чтения безопасности, а ваша организация [создала отчеты об обнаружении приложений в Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), вы можете использовать панель мониторинга облачного обнаружения для получения сведений о том, как люди в вашей организации организация использует Office 365 и другие облачные приложения. (Панель мониторинга облачного обнаружения также называется производительностью обнаружения приложений.)</span><span class="sxs-lookup"><span data-stu-id="f376a-p102">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage. If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps. (The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="f376a-117">Панель мониторинга облачного обнаружения позволяет просматривать подробные сведения о том, как пользователи в организации используют Office 365 и другие приложения.</span><span class="sxs-lookup"><span data-stu-id="f376a-117">The Cloud Discovery dashboard enables you to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![Обновлена панель мониторинга облачного обнаружения](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="f376a-119">Переход на панель мониторинга облачного обнаружения</span><span class="sxs-lookup"><span data-stu-id="f376a-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="f376a-120">Перейдите на портал Cloud App Security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполните вход.</span><span class="sxs-lookup"><span data-stu-id="f376a-120">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="f376a-121">Перейдите на страницу **Обнаружение** \> **облачной панели мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="f376a-121">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="f376a-122">Просмотр лучших пользователей, IP-адресов, приложений и уровней риска</span><span class="sxs-lookup"><span data-stu-id="f376a-122">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="f376a-123">С помощью панели мониторинга облачного обнаружения вы получите общий обзор приложений, которые используются с Office 365 в вашей организации, все открытые оповещения, лучшие пользователи и уровни риска.</span><span class="sxs-lookup"><span data-stu-id="f376a-123">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Дашбоаард облачного обнаружения](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="f376a-125">На вкладке **Dashboard (панель мониторинга** ) просмотрите общее использование облачного приложения в Организации в разделе Обзор в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="f376a-125">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="f376a-126">Просмотрите **категории Office 365** для приложений, используемых в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f376a-126">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="f376a-127">Просмотрите мини-приложение " **обнаруженные приложения** ", чтобы увидеть использование Office 365 и других приложений в этом представлении.</span><span class="sxs-lookup"><span data-stu-id="f376a-127">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="f376a-128">ПроУчите мини-приложение **Топ пользователей** и **Топ IP-адресов** , чтобы определить тех, кто использует Office 365 и облачные приложения в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f376a-128">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="f376a-129">Узнайте, где люди используют приложения, по географическому расположению с помощью карты расположений в **офисе приложений** .</span><span class="sxs-lookup"><span data-stu-id="f376a-129">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="f376a-p103">Над областью "карты" Взгляните на показатель риска обнаруженных приложений в обзоре **уровней риска** . Вы можете просмотреть риски, используя те же группы и категории, которые использовались в области **обнаруженных приложений** . Например, вы можете узнать, какой объем трафика в каждой группе относится к приложениям высокого, среднего или низкого риска.</span><span class="sxs-lookup"><span data-stu-id="f376a-p103">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview. You can look at risks by the same groups and categories that you used in the **Discovered apps** area. For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="f376a-133">Подробное углубление</span><span class="sxs-lookup"><span data-stu-id="f376a-133">Dive deeper into the information</span></span>

<span data-ttu-id="f376a-134">Облачное обнаружение можно использовать для более глубокого изучения приложений, поддоменов, IP-адресов и пользователей.</span><span class="sxs-lookup"><span data-stu-id="f376a-134">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="f376a-135">В панели мониторинга облачного обнаружения перейдите на вкладку **обнаруженные приложения** .</span><span class="sxs-lookup"><span data-stu-id="f376a-135">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="f376a-136">Используйте раздел фильтры для просмотра приложений по имени, категории, уровню использования или дате последнего рассмотрения.</span><span class="sxs-lookup"><span data-stu-id="f376a-136">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="f376a-137">В списке результатов наведите указатель мыши на имя приложения, чтобы открыть ссылку **Просмотр дочерних доменов** .</span><span class="sxs-lookup"><span data-stu-id="f376a-137">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span><br/> <span data-ttu-id="f376a-138">![НаВедите указатель рядом с приложением, чтобы открыть ссылку для просмотра сведений о дочернем домене](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span><span class="sxs-lookup"><span data-stu-id="f376a-138">![Hover next to an app to reveal a link to view subdomain details](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span></span><br/><span data-ttu-id="f376a-139">Будут отображены подробные сведения о выбранном приложении.</span><span class="sxs-lookup"><span data-stu-id="f376a-139">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="f376a-140">Чтобы просмотреть сведения об IP-адресах, перейдите на вкладку **IP-адреса** .</span><span class="sxs-lookup"><span data-stu-id="f376a-140">To view details about IP addresses, choose the **IP addresses** tab.</span></span><br/><span data-ttu-id="f376a-141">![В облачном поиске отображаются подробные сведения об IP-адресах](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span><span class="sxs-lookup"><span data-stu-id="f376a-141">![Cloud Discovery shows detailed information about IP addresses](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span></span><br/><span data-ttu-id="f376a-142">В списке результатов выберите отдельный IP-адрес, чтобы просмотреть более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="f376a-142">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="f376a-143">Чтобы просмотреть сведения о пользователях Office 365 в Организации, перейдите на вкладку **Пользователи** .</span><span class="sxs-lookup"><span data-stu-id="f376a-143">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span><br/><span data-ttu-id="f376a-144">![Облачное обнаружение — сведения о пользователях](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span><span class="sxs-lookup"><span data-stu-id="f376a-144">![Cloud Discovery - users info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span></span>
  
## <a name="exclude-entities"></a><span data-ttu-id="f376a-145">Исключение сущностей</span><span class="sxs-lookup"><span data-stu-id="f376a-145">Exclude entities</span></span>

<span data-ttu-id="f376a-146">Вы можете исключить некоторые системные пользователи или IP-адреса, чтобы сосредоточиться на более конкретных данных.</span><span class="sxs-lookup"><span data-stu-id="f376a-146">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="f376a-147">Выберите **Параметры** \> **облачного обнаружения**.</span><span class="sxs-lookup"><span data-stu-id="f376a-147">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="f376a-148">Выберите **исключить сущности**.</span><span class="sxs-lookup"><span data-stu-id="f376a-148">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="f376a-149">Выберите **исключенных пользователей** или **исключенных IP-адресов**.</span><span class="sxs-lookup"><span data-stu-id="f376a-149">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="f376a-150">Укажите пользователей или IP-адреса, а в поле **Комментарии** введите сведения о причинах исключения этих пользователей или IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="f376a-150">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="f376a-151">Выберите **Add** (Добавить).</span><span class="sxs-lookup"><span data-stu-id="f376a-151">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="f376a-152">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f376a-152">Next steps</span></span>

- [<span data-ttu-id="f376a-153">Просмотр оповещений и выполнение действий с ними</span><span class="sxs-lookup"><span data-stu-id="f376a-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="f376a-154">Создание отчетов об обнаружении приложений</span><span class="sxs-lookup"><span data-stu-id="f376a-154">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="f376a-155">Обзор [действий по использованию для Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="f376a-155">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

