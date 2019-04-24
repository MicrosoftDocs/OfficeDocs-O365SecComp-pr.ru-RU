---
title: Политики действий и оповещения в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Определите политики активности с помощью Office 365 Cloud App Security, чтобы настроить оповещения для запуска при возникновении определенных или слишком часто выполняемых действий. Настраивая политики для запуска оповещений, вы можете получать уведомления о конкретных действиях и отслеживать их.
ms.openlocfilehash: cfa58182ea35551ca3a3807c23e09c9f87c7be82
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242732"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="39551-104">Политики действий и оповещения в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="39551-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="39551-105">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="39551-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="39551-106">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="39551-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="39551-107">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="39551-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="39551-108">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="39551-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="39551-109">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="39551-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="39551-110">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="39551-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="39551-111">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="39551-111">You are here!</span></span>  <br/> [<span data-ttu-id="39551-112">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="39551-112">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="39551-113">Начало использования</span><span class="sxs-lookup"><span data-stu-id="39551-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="39551-114">В Office 365 Cloud App Security расширенные политики управления облаком запускают оповещения для определенных действий, которые происходят или происходят слишком часто.</span><span class="sxs-lookup"><span data-stu-id="39551-114">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently.</span></span> <span data-ttu-id="39551-115">Например, предположим, что пользователь пытается войти в Office 365 и отказывает 70 раз за одну минуту.</span><span class="sxs-lookup"><span data-stu-id="39551-115">For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute.</span></span> <span data-ttu-id="39551-116">Предположим, что другой пользователь загрузит файлы 7 000 или войдет в систему из Канады, когда этот пользователь должен находиться в другом месте.</span><span class="sxs-lookup"><span data-stu-id="39551-116">Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location.</span></span> <span data-ttu-id="39551-117">И, что еще хуже, предположим, что учетная запись пользователя скомпрометирована, а злоумышленник использует эту учетную запись для доступа к облачным приложениям и конфиденциальным данным Организации.</span><span class="sxs-lookup"><span data-stu-id="39551-117">Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="39551-118">Если вы являетесь [глобальным администратором или администратором безопасности](permissions-in-the-security-and-compliance-center.md), оповещения об активности уведомляют Вас при возникновении таких событий.</span><span class="sxs-lookup"><span data-stu-id="39551-118">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur.</span></span> <span data-ttu-id="39551-119">После этого вы можете выполнять определенные действия, такие как приостановка учетной записи пользователя, пока не сможете исследовать то, что произошло.</span><span class="sxs-lookup"><span data-stu-id="39551-119">You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="39551-120">Политики безопасности облачных приложений Office 365 отличаются от [политик оповещений в центре безопасности &amp; и соответствия требованиям Office 365](alert-policies.md).</span><span class="sxs-lookup"><span data-stu-id="39551-120">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md).</span></span> <span data-ttu-id="39551-121">Политики действий, описанные в этой статье, определены на портале Cloud App Security для Office 365 и могут помочь вам лучше управлять облачной средой организации.</span><span class="sxs-lookup"><span data-stu-id="39551-121">The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="39551-122">До начала работы</span><span class="sxs-lookup"><span data-stu-id="39551-122">Before you begin</span></span>

<span data-ttu-id="39551-123">Убедитесь, что:</span><span class="sxs-lookup"><span data-stu-id="39551-123">Make sure that:</span></span>
  
- <span data-ttu-id="39551-124">У вашей организации есть [Office 365 Cloud App Security](office-365-cas-overview.md), а служба [включена](turn-on-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="39551-124">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="39551-125">[Ведение журнала аудита](turn-audit-log-search-on-or-off.md) включено для вашей среды Office 365.</span><span class="sxs-lookup"><span data-stu-id="39551-125">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="39551-126">Вы являетесь глобальным администратором или администратором безопасности для Office 365.</span><span class="sxs-lookup"><span data-stu-id="39551-126">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="39551-127">Создание новой политики действий</span><span class="sxs-lookup"><span data-stu-id="39551-127">Create a new activity policy</span></span>

1. <span data-ttu-id="39551-128">Как глобальный администратор или администратор безопасности перейдите на портал Cloud App Security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполните вход.</span><span class="sxs-lookup"><span data-stu-id="39551-128">As a global administrator or security administrator, go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> <br><span data-ttu-id="39551-129">Откроется страница "политики безопасности облачного приложения Office 365".</span><span class="sxs-lookup"><span data-stu-id="39551-129">This takes you to the Office 365 Cloud App Security Policies page.</span></span><br><span data-ttu-id="39551-130">![При переходе на портал Cloud App Security (Office 365) вы можете начать со страницы "политики"](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span><span class="sxs-lookup"><span data-stu-id="39551-130">![When you go to the Office 365 Cloud App Security portal, you start with the Policies page](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span></span>
  
2. <span data-ttu-id="39551-131">Нажмите кнопку **создать политику**, а затем выберите пункт **Политика действий**.</span><span class="sxs-lookup"><span data-stu-id="39551-131">Click **Create policy**, and then select **Activity policy**.</span></span><br><span data-ttu-id="39551-132">![При создании политики в CAS Office 365 можно выбирать между политиками действий и политиками обнаружения аномалий.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span><span class="sxs-lookup"><span data-stu-id="39551-132">![When you create a policy in O365 CAS, you can choose between Activity policies and Anomaly Detection policies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span></span>
  
3. <span data-ttu-id="39551-133">На странице **Создание политики действий** укажите имя и **Описание** **политики** .</span><span class="sxs-lookup"><span data-stu-id="39551-133">On the **Create activity policy** page, specify the **Policy name** and **Description**.</span></span> <span data-ttu-id="39551-134">Чтобы создать политику на основе шаблона по умолчанию, выберите одну из них в списке **шаблон политики** или создайте собственную политику, не используя шаблон.</span><span class="sxs-lookup"><span data-stu-id="39551-134">To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span><br><span data-ttu-id="39551-135">![Вы можете создавать политики действий с помощью Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span><span class="sxs-lookup"><span data-stu-id="39551-135">![You can create activity policies with Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span></span>
  
4. <span data-ttu-id="39551-136">Выберите **серьезноСть политики** (низкие, средние или высокие), которые измеряют важность, если эта политика вызывает оповещение.</span><span class="sxs-lookup"><span data-stu-id="39551-136">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert.</span></span> <span data-ttu-id="39551-137">Это позволит вам отфильтровать оповещения при их последующем просмотре.</span><span class="sxs-lookup"><span data-stu-id="39551-137">This will help you filter alerts when you're reviewing them later.</span></span> 
    
5. <span data-ttu-id="39551-138">Выберите **категорию** для этой политики.</span><span class="sxs-lookup"><span data-stu-id="39551-138">Choose a **Category** for this policy.</span></span> <span data-ttu-id="39551-139">Это поможет фильтровать и сортировать оповещения, которые были активированы, или для групповых политик, когда вы просматриваете их, чтобы внести изменения.</span><span class="sxs-lookup"><span data-stu-id="39551-139">This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
6. <span data-ttu-id="39551-140">Выберите **фильтры действий** , чтобы настроить другие действия или метрики, которые будут запускать оповещение на основе этой политики.</span><span class="sxs-lookup"><span data-stu-id="39551-140">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
7. <span data-ttu-id="39551-141">В разделе **Параметры сопоставления действий**укажите, будет ли нарушение политики срабатывать, когда одно действие соответствует фильтрам, или если для триггеров оповещений требуется указанное число повторных действий.</span><span class="sxs-lookup"><span data-stu-id="39551-141">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span><br><span data-ttu-id="39551-142">Если выбрано **повторяющееся действие**, укажите количество действий, временной кадр и то, будет ли нарушение счетчика для пользователя в определенном приложении или для одного и того же пользователя с приложением.</span><span class="sxs-lookup"><span data-stu-id="39551-142">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
8. <span data-ttu-id="39551-143">При необходимости можно выбрать **создать оповещение** , чтобы создать дополнительные оповещения для получения уведомлений от этой политики (через электронную почту, текстовые сообщения или и то, и другое).</span><span class="sxs-lookup"><span data-stu-id="39551-143">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span><br><span data-ttu-id="39551-144">\*\*Убедитесь, что ваш поставщик электронной почты не блокирует сообщения, `no-reply@cloudappsecurity.com`отправленные с \*\*.</span><span class="sxs-lookup"><span data-stu-id="39551-144">**Make sure that your email provider doesn't block emails sent from `no-reply@cloudappsecurity.com`**.</span></span> 
  
9. <span data-ttu-id="39551-145">Выберите **действия** , которые следует предпринять при срабатывании оповещения, чтобы приостановить пользователя или потребовать от пользователя повторного входа в приложения Office 365.</span><span class="sxs-lookup"><span data-stu-id="39551-145">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
10. <span data-ttu-id="39551-146">Нажмите кнопку **создать** , чтобы завершить создание политики.</span><span class="sxs-lookup"><span data-stu-id="39551-146">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="39551-147">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="39551-147">Next steps</span></span>

- [<span data-ttu-id="39551-148">Политики обнаружения аномалий</span><span class="sxs-lookup"><span data-stu-id="39551-148">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="39551-149">Интеграция сервера SIEM</span><span class="sxs-lookup"><span data-stu-id="39551-149">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="39551-150">Просмотр оповещений и выполнение действий с ними</span><span class="sxs-lookup"><span data-stu-id="39551-150">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="39551-151">Группировка IP-адресов для упрощения управления</span><span class="sxs-lookup"><span data-stu-id="39551-151">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

