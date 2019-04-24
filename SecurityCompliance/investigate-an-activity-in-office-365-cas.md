---
title: Анализ действий в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'С помощью Office 365 Cloud App Security вы можете узнать, что происходит в вашей среде Office 365, проанализировать и изучить действия и учетные записи. '
ms.openlocfilehash: 0cc3860d953b40b0b0c247af6fb2b157d1abb235
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254845"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="900a4-103">Анализ действий в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="900a4-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="900a4-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="900a4-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="900a4-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="900a4-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="900a4-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="900a4-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="900a4-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="900a4-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="900a4-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="900a4-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="900a4-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="900a4-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="900a4-110">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="900a4-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="900a4-111">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="900a4-111">You are here!</span></span>  <br/> [<span data-ttu-id="900a4-112">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="900a4-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="900a4-113">Office 365 Cloud App Security работает с [журналом аудита office 365](detailed-properties-in-the-office-365-audit-log.md).</span><span class="sxs-lookup"><span data-stu-id="900a4-113">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md).</span></span> <span data-ttu-id="900a4-114">С помощью Office 365 Cloud App Security, как глобальный администратор или администратор безопасности, вы можете использовать страницу журнала активности для просмотра потенциальных проблем в том, как ваша организация использует Office 365.</span><span class="sxs-lookup"><span data-stu-id="900a4-114">With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="900a4-115">Получение страницы журнала активности</span><span class="sxs-lookup"><span data-stu-id="900a4-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="900a4-116">Перейдите на портал Cloud App Security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполните вход.</span><span class="sxs-lookup"><span data-stu-id="900a4-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="900a4-117">В области навигации в верхней части экрана выберите пункт **изучить** \> **Журнал действий**.</span><span class="sxs-lookup"><span data-stu-id="900a4-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="900a4-118">![На портале Office 365 CAS нажмите кнопку исследовать.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="900a4-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="900a4-119">Просмотр и исследование действий</span><span class="sxs-lookup"><span data-stu-id="900a4-119">Review and investigate activities</span></span>

<span data-ttu-id="900a4-120">На странице Журнал активности можно просмотреть список различных действий, выполняемых в Организации с помощью Office 365.</span><span class="sxs-lookup"><span data-stu-id="900a4-120">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365.</span></span> <span data-ttu-id="900a4-121">Вы можете использовать фильтры в верхней части экрана, чтобы сосредоточиться на определенных типах действий или определенных пользователях.</span><span class="sxs-lookup"><span data-stu-id="900a4-121">You can use filters across the top of the screen to focus on a specific type of activity or a specific user.</span></span> <span data-ttu-id="900a4-122">Например, на следующем рисунке показаны сведения об изменении пароля учетной записи администратора Office 365 в Организации:</span><span class="sxs-lookup"><span data-stu-id="900a4-122">For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![В Office 365 Cloud App Security выберите исследовать \> журнал активности.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="900a4-124">По мере просмотра каждого элемента в журнале активности можно нажать кнопку с многоточием, чтобы найти другие связанные действия.</span><span class="sxs-lookup"><span data-stu-id="900a4-124">As you look at each item in the Activity log, you can click the ellipses to find other related activities.</span></span> <span data-ttu-id="900a4-125">Например, вы можете просматривать другие действия того же типа, используя один и тот же IP-адрес, или из одной страны или региона.</span><span class="sxs-lookup"><span data-stu-id="900a4-125">For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="900a4-126">Кроме того, вы можете просматривать сведения о многих других видах действий.</span><span class="sxs-lookup"><span data-stu-id="900a4-126">You can view information about many other kinds of activities, too.</span></span> <span data-ttu-id="900a4-127">Например, ниже приведены некоторые действия, которые можно просмотреть в журнале активности:</span><span class="sxs-lookup"><span data-stu-id="900a4-127">For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="900a4-128">Элементы, добавленные в группы или удаленные из них</span><span class="sxs-lookup"><span data-stu-id="900a4-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="900a4-129">Изменения в пользовательских лицензиях</span><span class="sxs-lookup"><span data-stu-id="900a4-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="900a4-130">Общие внутренние или внешние файлы или папки</span><span class="sxs-lookup"><span data-stu-id="900a4-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="900a4-131">Созданные или удаленные сайты или семейства веб-сайтов;</span><span class="sxs-lookup"><span data-stu-id="900a4-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="900a4-132">Правила переадресации электронной почты</span><span class="sxs-lookup"><span data-stu-id="900a4-132">Email forwarding rules</span></span>
    
<span data-ttu-id="900a4-133">Используйте страницу журнала активности, чтобы познакомиться с тем, как пользователи в вашей организации используют Office 365 и какие проблемы могут возникать на пути.</span><span class="sxs-lookup"><span data-stu-id="900a4-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="900a4-134">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="900a4-134">Next steps</span></span>

- [<span data-ttu-id="900a4-135">Просмотр оповещений и реагирование на них в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="900a4-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="900a4-136">Обзор [действий по использованию для Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="900a4-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

