---
title: Анализ действий в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Office 365 облачных приложений безопасности можно увидеть, что происходит в вашей среде Office 365, поиск и исследование мероприятий и учетных записей. '
ms.openlocfilehash: e463323cf28738e1d54fcdb65ed0d15290c79994
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603660"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="82378-103">Анализ действий в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="82378-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="82378-104">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="82378-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="82378-105">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="82378-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="82378-106">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="82378-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="82378-107">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="82378-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="82378-108">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="82378-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="82378-109">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="82378-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="82378-110">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="82378-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="82378-111">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="82378-111">You are here!</span></span>  <br/> [<span data-ttu-id="82378-112">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="82378-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="82378-p101">Office 365 безопасности приложения облачных работает с [Office 365 журнал аудита](detailed-properties-in-the-office-365-audit-log.md). С помощью Office 365 облачных приложений безопасность как глобальный администратор или администратор безопасности можно использовать страницы журнал активности для просмотра потенциальных проблем в том, как ваша организация использует Office 365.</span><span class="sxs-lookup"><span data-stu-id="82378-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="82378-115">Получение страницы журналов активности</span><span class="sxs-lookup"><span data-stu-id="82378-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="82378-116">Последовательно выберите пункты портал облачных приложений безопасности ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="82378-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="82378-117">На панели навигации в верхней части экрана нажмите кнопку **Проверить** \> **Журнал активности**.</span><span class="sxs-lookup"><span data-stu-id="82378-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="82378-118">![На портале O365 сервера клиентского доступа нажмите кнопку Проверить.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="82378-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="82378-119">Просмотрите и проверьте действия</span><span class="sxs-lookup"><span data-stu-id="82378-119">Review and investigate activities</span></span>

<span data-ttu-id="82378-p102">На странице "журнал активности" можно просмотреть список различных действий, которые выполняются в рамках организации с помощью Office 365. Фильтры можно использовать в верхней части экрана сосредоточиться на определенный тип действия или отдельного пользователя. Например на следующем рисунке показана сведения об изменении записи для организации Office 365 admin password:</span><span class="sxs-lookup"><span data-stu-id="82378-p102">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![В облаке приложения Office 365 Безопасность выберите проверить \> журнал активности.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="82378-p103">При просмотре каждого элемента в журнал активности можно нажмите кнопку с многоточием, чтобы найти другие связанные задачи. Например можно просмотреть другие задачи одного типа, с одной IP-адреса или из одной страны или региона.</span><span class="sxs-lookup"><span data-stu-id="82378-p103">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="82378-p104">Можно просмотреть сведения о многих других видов действий, слишком. Например ниже приведены некоторые действия, которые можно просмотреть в журнале активности.</span><span class="sxs-lookup"><span data-stu-id="82378-p104">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="82378-128">Добавление или удаление из группы участников</span><span class="sxs-lookup"><span data-stu-id="82378-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="82378-129">Изменения в пользовательских лицензий</span><span class="sxs-lookup"><span data-stu-id="82378-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="82378-130">Файлы и папки общих внутреннем или внешнем ресурсе</span><span class="sxs-lookup"><span data-stu-id="82378-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="82378-131">Создаваемые или удаленных сайтов или семейств веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="82378-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="82378-132">Правила переадресации электронной почты</span><span class="sxs-lookup"><span data-stu-id="82378-132">Email forwarding rules</span></span>
    
<span data-ttu-id="82378-133">Использование страницы журнал активности, чтобы познакомиться с использования людей в организации Office 365 и что проблемы, они возникли по пути.</span><span class="sxs-lookup"><span data-stu-id="82378-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="82378-134">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="82378-134">Next steps</span></span>

- [<span data-ttu-id="82378-135">Просмотр оповещений и реагирование на них в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="82378-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="82378-136">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="82378-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

