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
description: Рецензирование отчеты обнаружения приложения в расширенного управления безопасностью, которые помогут узнать больше об облачных приложений, как использовать сотрудникам вашей организации. После создания отчетов о обнаружения приложения с помощью файлов журнала с помощью брандмауэров и прокси-серверы, просмотрите результаты на панели мониторинга обнаружения приложения.
ms.openlocfilehash: 6195c9aae7ae5e398ac555cc820de04dee05d4fd
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603750"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="4e761-104">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="4e761-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="4e761-105">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="4e761-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="4e761-106">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="4e761-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="4e761-107">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="4e761-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="4e761-108">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="4e761-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="4e761-109">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="4e761-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="4e761-110">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="4e761-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="4e761-111">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="4e761-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="4e761-112">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="4e761-112">You are here!</span></span>  <br/> [<span data-ttu-id="4e761-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="4e761-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="4e761-p102">Панель мониторинга обнаружения облака для работы с вашей организации веб-трафика журналов должна предоставить подробные сведения об использовании облачных приложений. Если вы глобального администратора, администратора безопасности или безопасности чтения и вашей организации есть [создания отчетов обнаружения приложения в облаке приложения Office 365 безопасности](create-app-discovery-reports-in-ocas.md), можно использовать панель мониторинга обнаружения облачных получить представление о том, как пользователи в вашей организации с помощью Office 365 и другие облачных приложений. (Панель мониторинга обнаружения облака также называется обнаружения приложения повышения производительности.)</span><span class="sxs-lookup"><span data-stu-id="4e761-p102">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage. If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps. (The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="4e761-117">Панель мониторинга обнаружения облако позволяет просматривать подробные сведения об использовании людей в организации Office 365 и другие приложения.</span><span class="sxs-lookup"><span data-stu-id="4e761-117">The Cloud Discovery dashboard enables you to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![Панель мониторинга обнаружения облака были обновлены](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="4e761-119">Перейдите к панели мониторинга обнаружения облако</span><span class="sxs-lookup"><span data-stu-id="4e761-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="4e761-120">Последовательно выберите пункты портал облачных приложений безопасности ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="4e761-120">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="4e761-121">Последовательно выберите пункты **обнаружить** \> **облаке обнаружения панели мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="4e761-121">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="4e761-122">Иллюстрация вашей наиболее активных пользователей, IP-адресов адреса, приложений и определенными уровнями риска</span><span class="sxs-lookup"><span data-stu-id="4e761-122">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="4e761-123">Панель мониторинга обнаружения облачных дается обзор в быстрого приложений, используемых в вашей организации, все открытые оповещения, наиболее активных пользователей и определенными уровнями риска с Office 365.</span><span class="sxs-lookup"><span data-stu-id="4e761-123">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Облако обнаружения dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="4e761-125">На вкладке **панели мониторинга** просмотрите общего использования приложения облака в вашей организации в разделе Обзор в верхней части экрана.</span><span class="sxs-lookup"><span data-stu-id="4e761-125">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="4e761-126">В разделе **категории Office 365** для приложений, используемых в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="4e761-126">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="4e761-127">Просмотрите **приложения Discovered** мини-приложения для просмотра об использовании Office 365 и других приложений в этом представлении.</span><span class="sxs-lookup"><span data-stu-id="4e761-127">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="4e761-128">Обратите внимание на **наиболее активных пользователей** и **в начало IP-адреса** мини-приложения для идентификации подразумевает использование Office 365 и облачных приложений наиболее в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="4e761-128">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="4e761-129">Узнать, где приложения, которые пользователи используют по географическому местоположению с помощью map **расположения штаб-квартире Apps** .</span><span class="sxs-lookup"><span data-stu-id="4e761-129">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="4e761-p103">Над областью карт рассмотрим оценки риска обнаруженных приложений в Обзор **определенными уровнями риска** . Вы можете просмотреть риски, связанные с одной группы и категории, которые используются в области **приложений Discovered** . Например можно увидеть, какой объем трафика в каждой группы — от приложения высокий, средний или низкий риск.</span><span class="sxs-lookup"><span data-stu-id="4e761-p103">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview. You can look at risks by the same groups and categories that you used in the **Discovered apps** area. For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="4e761-133">Подробнее об более подробные сведения</span><span class="sxs-lookup"><span data-stu-id="4e761-133">Dive deeper into the information</span></span>

<span data-ttu-id="4e761-134">Можно использовать обнаружения облачных вступило подробно рассматриваются приложения, дочерние домены, IP-адресов и пользователей.</span><span class="sxs-lookup"><span data-stu-id="4e761-134">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="4e761-135">В панели мониторинга обнаружения облачных откройте вкладку **Discovered приложений** .</span><span class="sxs-lookup"><span data-stu-id="4e761-135">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="4e761-136">Используйте раздел фильтры для просмотра приложения по имени, категории, уровень использования или Дата последнего просмотр.</span><span class="sxs-lookup"><span data-stu-id="4e761-136">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="4e761-137">В списке результатов наведите указатель мыши по имени приложения, чтобы показать ссылку **Просмотр поддоменов** .</span><span class="sxs-lookup"><span data-stu-id="4e761-137">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span><br/> <span data-ttu-id="4e761-138">![Наведите указатель мыши рядом с элементом приложения, чтобы показать ссылку для просмотра сведений о дочернего домена](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span><span class="sxs-lookup"><span data-stu-id="4e761-138">![Hover next to an app to reveal a link to view subdomain details](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span></span><br/><span data-ttu-id="4e761-139">Подробные сведения о выбранного приложения будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="4e761-139">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="4e761-140">Чтобы просмотреть подробные сведения о IP-адресов, перейдите на вкладку **IP-адресов** .</span><span class="sxs-lookup"><span data-stu-id="4e761-140">To view details about IP addresses, choose the **IP addresses** tab.</span></span><br/><span data-ttu-id="4e761-141">![Облако обнаружения показаны подробные сведения о IP-адресов](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span><span class="sxs-lookup"><span data-stu-id="4e761-141">![Cloud Discovery shows detailed information about IP addresses](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span></span><br/><span data-ttu-id="4e761-142">В списке результатов выберите отдельный IP-адрес для просмотра более подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="4e761-142">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="4e761-143">Чтобы просмотреть сведения об Office 365 пользователи вашей организации, перейдите на вкладку **Пользователи** .</span><span class="sxs-lookup"><span data-stu-id="4e761-143">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span><br/><span data-ttu-id="4e761-144">![Обнаружение Cloud - info пользователей](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span><span class="sxs-lookup"><span data-stu-id="4e761-144">![Cloud Discovery - users info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span></span>
  
## <a name="exclude-entities"></a><span data-ttu-id="4e761-145">Исключить сущности</span><span class="sxs-lookup"><span data-stu-id="4e761-145">Exclude entities</span></span>

<span data-ttu-id="4e761-146">Чтобы получать более детальную информацию можно исключить определенных пользователей системы или IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="4e761-146">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="4e761-147">Выбор **параметров** \> **Параметры обнаружения облака**.</span><span class="sxs-lookup"><span data-stu-id="4e761-147">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="4e761-148">Выберите **исключить сущностей**.</span><span class="sxs-lookup"><span data-stu-id="4e761-148">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="4e761-149">Выберите **Исключенные пользователи** или **исключаются IP-адресов**.</span><span class="sxs-lookup"><span data-stu-id="4e761-149">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="4e761-150">Укажите пользователей или IP-адресов, а в поле **комментарии** введите сведения о почему кроме тех пользователей или IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="4e761-150">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="4e761-151">Выберите **Add** (Добавить).</span><span class="sxs-lookup"><span data-stu-id="4e761-151">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="4e761-152">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="4e761-152">Next steps</span></span>

- [<span data-ttu-id="4e761-153">Просмотрите и выполнять операции с оповещениями</span><span class="sxs-lookup"><span data-stu-id="4e761-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="4e761-154">Создание отчетов обнаружения приложения</span><span class="sxs-lookup"><span data-stu-id="4e761-154">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="4e761-155">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="4e761-155">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

