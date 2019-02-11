---
title: Просмотр оповещений и реагирование на них в Office 365 Cloud App Security
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
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Использование страницы оповещений в облаке приложения Office 365 безопасности для страница потенциальных проблем. Можно закрыть или разрешении предупреждений и при необходимости отключать учетной записи пользователя.
ms.openlocfilehash: ff20b913553414d796f9653108ac9b8a3d84cb74
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603680"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="6531d-104">Просмотр оповещений и реагирование на них в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="6531d-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="6531d-105">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="6531d-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="6531d-106">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="6531d-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="6531d-107">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="6531d-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="6531d-108">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="6531d-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="6531d-109">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="6531d-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="6531d-110">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="6531d-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="6531d-111">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="6531d-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="6531d-112">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="6531d-112">You are here!</span></span>  <br/> [<span data-ttu-id="6531d-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6531d-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="6531d-114">Страница оповещений в облаке приложения Office 365 безопасности для просмотра потенциальных проблем и при необходимости выполнять действия.</span><span class="sxs-lookup"><span data-stu-id="6531d-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6531d-p102">Необходимо быть глобальным администратором или администратор безопасности для выполнения задач в этой статье. Просмотреть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="6531d-p102">You must be a global administrator or security administrator to perform the tasks in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="6531d-117">Как получить на странице оповещений</span><span class="sxs-lookup"><span data-stu-id="6531d-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="6531d-118">Последовательно выберите пункты портал облачных приложений безопасности ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="6531d-118">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="6531d-119">На панели навигации в верхней части экрана выберите **оповещения**.</span><span class="sxs-lookup"><span data-stu-id="6531d-119">In the navigation bar across the top of the screen, choose **Alerts**.</span></span><br/><span data-ttu-id="6531d-120">![На странице "оповещения" можно просмотреть оповещений, которое было запущено и любые действия, предпринятые.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span><span class="sxs-lookup"><span data-stu-id="6531d-120">![On the Alerts page, you can see alerts that were triggered and any actions taken.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span></span>
  
## <a name="review-and-handle-alerts"></a><span data-ttu-id="6531d-121">Просмотр, а также обрабатывать оповещений</span><span class="sxs-lookup"><span data-stu-id="6531d-121">Review and handle alerts</span></span>

<span data-ttu-id="6531d-p103">Оповещения помочь определить действия в облачной среде Office 365, может потребоваться исследование. Также можно создать новые политики или редактирование существующих политик на основании оповещений, которое появится. Например если вход в систему из подозрительные расположения администратора, можно настроить политики, которая не позволяет администраторам вход в Office 365 из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="6531d-p103">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further. You might also decide to create new policies or edit existing policies based on the alerts you see. For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="6531d-125">Можно отфильтровать оповещения по **категории** или по **уровню серьезности** , наиболее важные из них могут управлять сначала.</span><span class="sxs-lookup"><span data-stu-id="6531d-125">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="6531d-p104">Для каждого оповещения поиска в причину, чтобы выбрать действие для обработки. Для получения дополнительных сведений о оповещения и выполнять действия, такие как разрешение оповещения или приостановка учетной записи пользователей, выберите оповещение, чтобы открыть веб-страницу. На странице сведений о просмотрите журнал активности, учетных записей и пользователей, которые связаны с оповещение и выполнение действий, например следующие:</span><span class="sxs-lookup"><span data-stu-id="6531d-p104">For each alert, look into what caused it so you can decide what action to take. To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page. On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="6531d-p105">**Отклонение** Если оповещение было Ложное срабатывание, закройте его. При необходимости можно добавить примечание о том, почему закрытия.</span><span class="sxs-lookup"><span data-stu-id="6531d-p105">**Dismiss** If the alert was a false positive, dismiss it. You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="6531d-p106">**Разрешить оповещения** Если оповещение вызвано действие, которое вы знаете не угрозы, ее решения. При необходимости можно добавить примечание о том, почему разрешен.</span><span class="sxs-lookup"><span data-stu-id="6531d-p106">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it. You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="6531d-133">**Приостановка** Если предполагается несанкционированного входа ins на учетную запись, например, кто-то вход в другой стране, когда вы знаете, что контакт находится физически локального офиса, можно [Приостановить учетной записи](suspend-or-restore-an-account-in-ocas.md) при изучении, что происходит.</span><span class="sxs-lookup"><span data-stu-id="6531d-133">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="6531d-134">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6531d-134">Next steps</span></span>

- [<span data-ttu-id="6531d-135">Анализ деятельности</span><span class="sxs-lookup"><span data-stu-id="6531d-135">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="6531d-136">Приостановка или восстановление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="6531d-136">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="6531d-137">Просмотр списка поддерживаемых [веб-трафика журналов и источников данных](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="6531d-137">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="6531d-138">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="6531d-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

