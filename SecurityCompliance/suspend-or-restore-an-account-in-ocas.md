---
title: Приостановка или восстановление учетной записи пользователя в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'С помощью Office 365 Cloud App Security действия по управлению можно приостановить или отменить приостановку работы учетной записи пользователя. '
ms.openlocfilehash: 3650a5304af0440dc537610994c4bd827f599989
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215099"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="a5afa-103">Приостановка или восстановление учетной записи пользователя в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a5afa-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="a5afa-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a5afa-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="a5afa-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a5afa-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="a5afa-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="a5afa-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="a5afa-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a5afa-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="a5afa-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="a5afa-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="a5afa-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="a5afa-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="a5afa-110">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="a5afa-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="a5afa-111">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="a5afa-111">You are here!</span></span>  <br/> [<span data-ttu-id="a5afa-112">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="a5afa-112">Next steps</span></span>](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="a5afa-p101">Предположим, что вы получили оповещение о том, что одна из учетных записей пользователей вашей организации для Office 365 была скомпрометирована. Предположим, вы получили оповещение о том, что у пользователя возникли проблемы с учетной записью пользователя. С помощью Office 365 Cloud App Security вы можете приостановить учетную запись пользователя и позже восстановить ее после того, как вы изучили полученные оповещения.</span><span class="sxs-lookup"><span data-stu-id="a5afa-p101">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised. Or, suppose that you've received an alert that indicates something is wrong with a user account. With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a5afa-p102">Office 365 Cloud App Security доступен в Office 365 корпоративный "~". Если ваша организация использует другую подписку на Office 365 Enterprise, можно приобрести надстройку Office 365 для облачных приложений. в центре администрирования Office 365 (как глобальный администратор) выберите пункт **подписки**на надстройки для **выставления счетов** \> . Дополнительные сведения см. в статье [office 365 Platform Service Description: центр соответствия &amp; требованиям безопасности Office 365](https://technet.microsoft.com/en-us/library/dn933793.aspx) и [приобретение или изменение надстройки для Office 365 для бизнеса](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="a5afa-p102">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="a5afa-119">Приостановка учетной записи пользователя в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a5afa-119">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="a5afa-p103">Когда вы приостанавливаете учетную запись пользователя, пользователь не сможет снова войти в систему. Это то же самое, что изменение учетной записи пользователя непосредственно в Office 365 для установки состояния входа в систему \*\*\*\* с блокированным входом.</span><span class="sxs-lookup"><span data-stu-id="a5afa-p103">When you suspend a user account, you prevent the user from signing in again. It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a5afa-p104">Если вы блокируете вход пользователя в Office 365, приостанавливаете его или редактируя его состояние входа, имейте в виду, что это может занять от часа или до того, чтобы оно вступило в силу на всех устройствах и клиентах пользователя ([изменение или изменение пользователя в Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). Если пользователь вошел в Office 365, этот блок вступит в силу всякий раз, когда необходимо будет войти в Office 365.</span><span class="sxs-lookup"><span data-stu-id="a5afa-p104">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="a5afa-p105">Как [глобальный администратор или администратор безопасности](permissions-in-the-security-and-compliance-center.md)Войдите в свою рабочую [https://protection.office.com](https://protection.office.com) или учебную учетную запись, используя свою рабочую или учебную учетную запись. (Откроется центр соответствия требованиям безопасности &amp; .)</span><span class="sxs-lookup"><span data-stu-id="a5afa-p105">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="a5afa-126">В центре безопасности &amp; и соответствия требованиям выберите **оповещения** \> **Управление расширенными оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="a5afa-126">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="a5afa-127">Выберите **Перейти к Office 365 Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="a5afa-127">Choose **Go to Office 365 Cloud App Security**.</span></span><br><span data-ttu-id="a5afa-128">![В центре безопасности &amp; и соответствия требованиям выберите Управление расширенными оповещениями для перехода к Office 365 Cloud App Security.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="a5afa-128">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br>
  
4. <span data-ttu-id="a5afa-129">В области навигации, расположенной в верхней части экрана, выберите **оповещения**.</span><span class="sxs-lookup"><span data-stu-id="a5afa-129">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="a5afa-130">В столбце **оповещение** дважды щелкните оповещение, относящееся к определенной учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="a5afa-130">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="a5afa-131">В разделе **учетные записи**в столбце **состояние** выберите ![параметры значок](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **приостановить пользователя**.</span><span class="sxs-lookup"><span data-stu-id="a5afa-131">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="a5afa-132">Восстановление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="a5afa-132">To restore a user account</span></span>

<span data-ttu-id="a5afa-133">Просмотр [в статье восстановление пользователя в Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span><span class="sxs-lookup"><span data-stu-id="a5afa-133">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="a5afa-134">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="a5afa-134">Next steps</span></span>

- [<span data-ttu-id="a5afa-135">Просмотр оповещений и реагирование на них в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a5afa-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="a5afa-136">Управление приложениями OAuth с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a5afa-136">Manage OAuth apps using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="a5afa-137">Обзор [действий по использованию для Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="a5afa-137">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

