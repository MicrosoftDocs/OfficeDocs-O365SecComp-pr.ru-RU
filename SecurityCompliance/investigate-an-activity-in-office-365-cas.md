---
title: Анализ действий в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Office 365 облачных приложений безопасности можно увидеть, что происходит в вашей среде Office 365, поиск и исследование мероприятий и учетных записей. '
ms.openlocfilehash: 03db572ebddbdf27371f8e6fd2f0cdd91c14a12f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534437"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="491f1-103">Анализ действий в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="491f1-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="491f1-104">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="491f1-104">****Evaluation** \>**</span></span>|<span data-ttu-id="491f1-105">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="491f1-105">****Planning** \>**</span></span>|<span data-ttu-id="491f1-106">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="491f1-106">****Deployment** \>**</span></span>|<span data-ttu-id="491f1-107">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="491f1-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="491f1-108">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="491f1-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="491f1-109">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="491f1-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="491f1-110">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="491f1-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="491f1-111">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="491f1-111">You are here!</span></span>  <br/> [<span data-ttu-id="491f1-112">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="491f1-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="491f1-p101">Office 365 безопасности приложения облачных работает с [Office 365 журнал аудита](detailed-properties-in-the-office-365-audit-log.md). С помощью Office 365 облачных приложений безопасность как глобальный администратор или администратор безопасности можно использовать страницы журнал активности для просмотра потенциальных проблем в том, как ваша организация использует Office 365.</span><span class="sxs-lookup"><span data-stu-id="491f1-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="491f1-115">Получение страницы журналов активности</span><span class="sxs-lookup"><span data-stu-id="491f1-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="491f1-p102">Как глобальный администратор или администратор безопасности, перейдите к [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы. (Увидеть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="491f1-p102">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>
    
2. <span data-ttu-id="491f1-118">В разделе Безопасность &amp; центре соответствия требованиям, выберите **оповещения** \> **Расширенное Управление оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="491f1-118">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="491f1-119">Выберите, **перейдите к безопасности приложения Office 365 облака**.</span><span class="sxs-lookup"><span data-stu-id="491f1-119">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите дополнительные оповещения для перехода к безопасности Office 365 облаке приложения](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="491f1-121">На панели навигации в верхней части экрана нажмите кнопку **Проверить** \> **Журнал активности**.</span><span class="sxs-lookup"><span data-stu-id="491f1-121">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span>
    
    ![На портале O365 сервера клиентского доступа нажмите кнопку Проверить.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="491f1-123">Просмотрите и проверьте действия</span><span class="sxs-lookup"><span data-stu-id="491f1-123">Review and investigate activities</span></span>

<span data-ttu-id="491f1-p103">На странице "журнал активности" можно просмотреть список различных действий, которые выполняются в рамках организации с помощью Office 365. Фильтры можно использовать в верхней части экрана сосредоточиться на определенный тип действия или отдельного пользователя. Например на следующем рисунке показана сведения об изменении записи для организации Office 365 admin password:</span><span class="sxs-lookup"><span data-stu-id="491f1-p103">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![В облаке приложения Office 365 Безопасность выберите проверить \> журнал активности.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="491f1-p104">При просмотре каждого элемента в журнал активности можно нажмите кнопку с многоточием, чтобы найти другие связанные задачи. Например можно просмотреть другие задачи одного типа, с одной IP-адреса или из одной страны или региона.</span><span class="sxs-lookup"><span data-stu-id="491f1-p104">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="491f1-p105">Можно просмотреть сведения о многих других видов действий, слишком. Например ниже приведены некоторые действия, которые можно просмотреть в журнале активности.</span><span class="sxs-lookup"><span data-stu-id="491f1-p105">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="491f1-132">Добавление или удаление из группы участников</span><span class="sxs-lookup"><span data-stu-id="491f1-132">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="491f1-133">Изменения в пользовательских лицензий</span><span class="sxs-lookup"><span data-stu-id="491f1-133">Changes in user licenses</span></span>
    
- <span data-ttu-id="491f1-134">Файлы и папки общих внутреннем или внешнем ресурсе</span><span class="sxs-lookup"><span data-stu-id="491f1-134">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="491f1-135">Создаваемые или удаленных сайтов или семейств веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="491f1-135">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="491f1-136">Правила переадресации электронной почты</span><span class="sxs-lookup"><span data-stu-id="491f1-136">Email forwarding rules</span></span>
    
<span data-ttu-id="491f1-137">Использование страницы журнал активности, чтобы познакомиться с использования людей в организации Office 365 и что проблемы, они возникли по пути.</span><span class="sxs-lookup"><span data-stu-id="491f1-137">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="491f1-138">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="491f1-138">Next steps</span></span>

- [<span data-ttu-id="491f1-139">Просмотр оповещений и реагирование на них в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="491f1-139">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="491f1-140">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="491f1-140">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

