---
title: Политики действий и оповещения в Office 365 Cloud App Security
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
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Определение активности политик безопасности Office 365 облаке приложения для настройки оповещений для запуска, когда деятельности происходить или происходит слишком часто. Настраивая политики для запуска оповещения, можно получать уведомления о и отслеживать действия.
ms.openlocfilehash: a239e2bf453a01bf852a702a66cb2f09c02b8c96
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272374"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="05a94-104">Политики действий и оповещения в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="05a94-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

<span data-ttu-id="05a94-105">Расширенное управление безопасностью для Office 365 является теперь приложения облаке Безопасность в Office 365.</span><span class="sxs-lookup"><span data-stu-id="05a94-105">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="05a94-106">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="05a94-106">****Evaluation** \>**</span></span>|<span data-ttu-id="05a94-107">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="05a94-107">****Planning** \>**</span></span>|<span data-ttu-id="05a94-108">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="05a94-108">****Deployment** \>**</span></span>|<span data-ttu-id="05a94-109">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="05a94-109">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="05a94-110">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="05a94-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="05a94-111">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="05a94-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="05a94-112">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="05a94-112">You are here!</span></span>  <br/> [<span data-ttu-id="05a94-113">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="05a94-113">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="05a94-114">Начать использование</span><span class="sxs-lookup"><span data-stu-id="05a94-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="05a94-p102">С Office 365 облачных приложений безопасность политик управления расширенной облачных активируют оповещения для конкретных действий, которые происходят или происходит слишком часто. Предположим, например, пользователь пытается выполнить вход в Office 365 и не удается выполнить 70 раз в минуту. Предположим, что другой пользователь загружает 7000 файлы или, отображаемого для входить в систему из Канады, когда этот пользователь должен находится в другом месте. Или того, предположим, что оказались раскрыты учетной записи другого пользователя, и он использует эту учетную запись для доступа к вашей организации облачных приложений и конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="05a94-p102">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently. For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute. Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location. Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="05a94-p103">Если вы являетесь [глобальный администратор или администратор безопасности](permissions-in-the-security-and-compliance-center.md), активности оповещения могут возникать при события, такие как следующие. Затем вы можете воспользоваться конкретные действия, такие как задержки учетной записи пользователя, пока не выяснить, что произошло.</span><span class="sxs-lookup"><span data-stu-id="05a94-p103">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur. You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="05a94-p104">Политики безопасности облаке приложения Office 365, отличаются от [предупреждения политики безопасности Office 365 &amp; центре соответствия требованиям](alert-policies.md). Действия политики, описанные в этой статье определяются на портале облачных приложений Office 365 безопасности и помогут вам лучше управлять облачной среде вашей организации.</span><span class="sxs-lookup"><span data-stu-id="05a94-p104">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md). The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="05a94-123">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="05a94-123">Before you begin</span></span>

<span data-ttu-id="05a94-124">Убедитесь, что:</span><span class="sxs-lookup"><span data-stu-id="05a94-124">Make sure that:</span></span>
  
- <span data-ttu-id="05a94-125">Вашей организации есть [Облачных приложений Office 365 безопасности](office-365-cas-overview.md)и служба является [включенным](turn-on-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="05a94-125">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="05a94-126">[Ведение журнала аудита](turn-audit-log-search-on-or-off.md) для вашей среде Office 365 включено.</span><span class="sxs-lookup"><span data-stu-id="05a94-126">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="05a94-127">Вы являетесь глобального администратора или администратора безопасности для Office 365.</span><span class="sxs-lookup"><span data-stu-id="05a94-127">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="05a94-128">Создать новую политику активности</span><span class="sxs-lookup"><span data-stu-id="05a94-128">Create a new activity policy</span></span>

1. <span data-ttu-id="05a94-129">Как глобальный администратор или администратор безопасности, перейдите к [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="05a94-129">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> 
    
2. <span data-ttu-id="05a94-130">В разделе Безопасность &amp; центре соответствия требованиям, выберите **оповещения** \> **Расширенное Управление оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="05a94-130">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="05a94-131">Выберите, **перейдите к безопасности приложения Office 365 облака**.</span><span class="sxs-lookup"><span data-stu-id="05a94-131">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    <span data-ttu-id="05a94-132">Откроется страница политики безопасности Office 365 облачных приложений.</span><span class="sxs-lookup"><span data-stu-id="05a94-132">This takes you to the Office 365 Cloud App Security Policies page.</span></span>
    
    ![При переходе к порталу Office 365 облачных приложений безопасности, запустите со страницей политик](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)
  
4. <span data-ttu-id="05a94-134">Нажмите кнопку **Создать политику**, а затем выберите **действие политики**.</span><span class="sxs-lookup"><span data-stu-id="05a94-134">Click **Create policy**, and then select **Activity policy**.</span></span>
    
    ![При создании политики в O365 сервера клиентского доступа, можно выбрать между активности и политики обнаружение неполадок.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)
  
5. <span data-ttu-id="05a94-p105">На странице " **Создать политику активности** " укажите **имя** и **Описание**политики. Чтобы политики на шаблон по умолчанию, выберите его в списке **шаблон политики** или создайте свои собственные политики без использования шаблона.</span><span class="sxs-lookup"><span data-stu-id="05a94-p105">On the **Create activity policy** page, specify the **Policy name** and **Description**. To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span> 
    
    ![Можно создать активности политик с Office 365 облачных приложений безопасности.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)
  
6. <span data-ttu-id="05a94-p106">Выберите **уровень серьезности политики** (низкий, средний или высокий) меры, насколько это вам Если эта политика запускает оповещение. Эта информация поможет фильтрация оповещения, когда вы просмотра более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="05a94-p106">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert. This will help you filter alerts when you're reviewing them later.</span></span> 
    
7. <span data-ttu-id="05a94-p107">Выберите **категорию** для этой политики. Эта информация поможет фильтрации и сортировки оповещений, которое было запущено, или групповых политик, когда вы просмотра для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="05a94-p107">Choose a **Category** for this policy. This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
8. <span data-ttu-id="05a94-143">Выберите **Действие фильтры** для настройки других действий или показатели, вызывающее уведомление на основе этой политики.</span><span class="sxs-lookup"><span data-stu-id="05a94-143">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
9. <span data-ttu-id="05a94-144">В разделе **действия совпадают с параметрами**укажите ли нарушение политики будет применяться при одно действие соответствует фильтры, а если указанное число повторные действия необходимо оповещения триггеров.</span><span class="sxs-lookup"><span data-stu-id="05a94-144">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span>
    
    <span data-ttu-id="05a94-145">При выборе **активности встречается повторно**указать число действий, временные рамки и ли число нарушение, для пользователя в рамках определенного приложения или для одного пользователя с помощью любого приложения.</span><span class="sxs-lookup"><span data-stu-id="05a94-145">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
10. <span data-ttu-id="05a94-146">При необходимости вы можете выбрать **создать оповещение** , чтобы создать дополнительные оповещения для получения уведомлений из этой политики (по электронной почте, текстовое сообщение или оба).</span><span class="sxs-lookup"><span data-stu-id="05a94-146">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="05a94-147">Убедитесь, что ваш поставщик электронной почты не блокирует сообщений, отправляемых из no-reply@cloudappsecurity.com.</span><span class="sxs-lookup"><span data-stu-id="05a94-147">Make sure that your email provider doesn't block emails sent from no-reply@cloudappsecurity.com.</span></span> 
  
11. <span data-ttu-id="05a94-148">Выберите **действия** , должны быть выполнены при оповещения для приостановки пользователя или, необходимо снова войти в приложениях Office 365.</span><span class="sxs-lookup"><span data-stu-id="05a94-148">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
12. <span data-ttu-id="05a94-149">Нажмите кнопку **Создать** , чтобы завершить создание политики.</span><span class="sxs-lookup"><span data-stu-id="05a94-149">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="05a94-150">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="05a94-150">Next steps</span></span>
<span data-ttu-id="05a94-151"><a name="nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="05a94-151"></span></span>

- [<span data-ttu-id="05a94-152">Функция обнаружения неполадок политик</span><span class="sxs-lookup"><span data-stu-id="05a94-152">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="05a94-153">Интеграция сервера SIEM</span><span class="sxs-lookup"><span data-stu-id="05a94-153">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="05a94-154">Просмотрите и выполнять операции с оповещениями</span><span class="sxs-lookup"><span data-stu-id="05a94-154">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="05a94-155">Групповой IP-адреса для упрощения управления</span><span class="sxs-lookup"><span data-stu-id="05a94-155">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

