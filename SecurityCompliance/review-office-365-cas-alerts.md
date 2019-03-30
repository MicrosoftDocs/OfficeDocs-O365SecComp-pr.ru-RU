---
title: Просмотр оповещений и реагирование на них в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Используйте страницу оповещения в Office 365 Cloud App Security для просмотра потенциальных проблем и выполнения действий. Вы можете отклонить или разрешить оповещения, а при необходимости приостановить учетную запись пользователя.
ms.openlocfilehash: ddef10293fca7b722a13babdca5c05bbe2398cb3
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000042"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="a40bd-104">Просмотр оповещений и реагирование на них в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a40bd-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="a40bd-105">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a40bd-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="a40bd-106">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a40bd-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="a40bd-107">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a40bd-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="a40bd-108">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a40bd-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="a40bd-109">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="a40bd-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="a40bd-110">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="a40bd-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="a40bd-111">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="a40bd-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="a40bd-112">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="a40bd-112">You are here!</span></span>  <br/> [<span data-ttu-id="a40bd-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="a40bd-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="a40bd-114">Вы можете использовать страницу оповещения в Office 365 Cloud App Security, чтобы просмотреть потенциальные проблемы и при необходимости выполнить действие.</span><span class="sxs-lookup"><span data-stu-id="a40bd-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a40bd-115">Для выполнения задач, описанных в этой статье, необходимо быть глобальным администратором или администратором безопасности.</span><span class="sxs-lookup"><span data-stu-id="a40bd-115">You must be a global administrator or security administrator to perform the tasks in this article.</span></span> <span data-ttu-id="a40bd-116">Ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a40bd-116">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="a40bd-117">Получение страницы оповещений</span><span class="sxs-lookup"><span data-stu-id="a40bd-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="a40bd-118">Перейдите на портал Cloud App Security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполните вход.</span><span class="sxs-lookup"><span data-stu-id="a40bd-118">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="a40bd-119">В области навигации, расположенной в верхней части экрана, выберите **оповещения**.</span><span class="sxs-lookup"><span data-stu-id="a40bd-119">In the navigation bar across the top of the screen, choose **Alerts**.</span></span><br/><span data-ttu-id="a40bd-120">![На странице оповещения можно просмотреть оповещения, которые были активированы, и все выполненные действия.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span><span class="sxs-lookup"><span data-stu-id="a40bd-120">![On the Alerts page, you can see alerts that were triggered and any actions taken.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span></span>
 
> [!NOTE]
> <span data-ttu-id="a40bd-121">Оповещения Cloud App Security также отображаются в центре безопасности _амп_ соответствие требованиям (перейдите к разделу **Alerts** > **View Alerts**.</span><span class="sxs-lookup"><span data-stu-id="a40bd-121">Cloud App Security alerts are also visible in the Security & Compliance Center (go to **Alerts** > **View alerts**.</span></span> <span data-ttu-id="a40bd-122">Однако в настоящее время необходимо разрешить эти оповещения на портале Cloud App Security и в центре безопасности _Амп_ соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="a40bd-122">Currently, however, you must resolve these alerts in both the Cloud App Security portal and the Security & Compliance Center.</span></span> <span data-ttu-id="a40bd-123">Чтобы узнать больше, ознакомьтесь со статьей [Просмотр оповещенИй системы безопасности облачНых приложений](alert-policies.md#viewing-cloud-app-security-alerts).</span><span class="sxs-lookup"><span data-stu-id="a40bd-123">To learn more, see [Viewing Cloud App Security alerts](alert-policies.md#viewing-cloud-app-security-alerts).)</span></span> 
 
## <a name="review-and-handle-alerts"></a><span data-ttu-id="a40bd-124">Просмотр и обработка оповещений</span><span class="sxs-lookup"><span data-stu-id="a40bd-124">Review and handle alerts</span></span>

<span data-ttu-id="a40bd-125">Оповещения помогают определить действия в облачной среде Office 365, которые вы можете использовать еще больше.</span><span class="sxs-lookup"><span data-stu-id="a40bd-125">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further.</span></span> <span data-ttu-id="a40bd-126">Вы также можете создать новые политики или изменить существующие, используя оповещения, которые вы видите.</span><span class="sxs-lookup"><span data-stu-id="a40bd-126">You might also decide to create new policies or edit existing policies based on the alerts you see.</span></span> <span data-ttu-id="a40bd-127">Например, если вы видите, что администратор входит в систему с неопределенного места, вы можете настроить политику, которая запрещает администраторам входить в Office 365 из определенных расположений.</span><span class="sxs-lookup"><span data-stu-id="a40bd-127">For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="a40bd-128">Вы можете отфильтровать оповещения по **категории** или по **степени серьезности** , чтобы вы могли управлять самыми важными из них первыми.</span><span class="sxs-lookup"><span data-stu-id="a40bd-128">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="a40bd-129">Для каждого оповещения рассмотрим то, что привело к тому, что вы можете решить, какие действия необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="a40bd-129">For each alert, look into what caused it so you can decide what action to take.</span></span> <span data-ttu-id="a40bd-130">Чтобы просмотреть дополнительные сведения о предупреждении и выполнить действия, такие как разрешение оповещения или приостановка учетной записи пользователя, выберите оповещение, чтобы открыть страницу сведений.</span><span class="sxs-lookup"><span data-stu-id="a40bd-130">To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page.</span></span> <span data-ttu-id="a40bd-131">На странице сведения можно просмотреть журнал активности, учетные записи и пользователей, связанные с оповещением, и выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a40bd-131">On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="a40bd-132">**Прекратить** Если предупреждение было ложным, закройте его.</span><span class="sxs-lookup"><span data-stu-id="a40bd-132">**Dismiss** If the alert was a false positive, dismiss it.</span></span> <span data-ttu-id="a40bd-133">Вы можете дополнительно добавить комментарий, поясняющий, почему вы его отпустили.</span><span class="sxs-lookup"><span data-stu-id="a40bd-133">You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="a40bd-134">**Устранение оповещения** Если оповещение было вызвано действием, которое не является угрозой, разрешите его.</span><span class="sxs-lookup"><span data-stu-id="a40bd-134">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it.</span></span> <span data-ttu-id="a40bd-135">Вы можете дополнительно добавить комментарий, объясняющий, почему вы его разрешали.</span><span class="sxs-lookup"><span data-stu-id="a40bd-135">You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="a40bd-136">**Suspend** (Приостановка) Если вы подозреваете несанкционированные входы в учетной записи, например, кто-то подключается из другой страны, когда вы знаете, что он физически находится в локальном офисе, вы можете [приостановить эту учетную запись](suspend-or-restore-an-account-in-ocas.md) , пока вы изучите то, что происходит.</span><span class="sxs-lookup"><span data-stu-id="a40bd-136">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="a40bd-137">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="a40bd-137">Next steps</span></span>

- [<span data-ttu-id="a40bd-138">Исследование действия</span><span class="sxs-lookup"><span data-stu-id="a40bd-138">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="a40bd-139">ПриОстановка или восстановление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="a40bd-139">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="a40bd-140">Просмотр списка поддерживаемых [журналов веб-трафика и источников данных](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="a40bd-140">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="a40bd-141">Обзор [действий по использованию для Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="a40bd-141">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

