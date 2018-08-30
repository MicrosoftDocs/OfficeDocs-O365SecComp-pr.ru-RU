---
title: Приостановка или восстановление учетной записи пользователя в Office 365 Cloud App Security
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
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'С Office 365 облачных приложений безопасность управления действия, которые нужно выполнить, приостановить или отменить приостановку учетной записи пользователя. '
ms.openlocfilehash: a5c75edefc6ddb87b5676c4253aafe04817f6a1d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534440"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="86dfd-103">Приостановка или восстановление учетной записи пользователя в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="86dfd-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="86dfd-104">Расширенное управление безопасностью для Office 365 является теперь приложения облаке Безопасность в Office 365.</span><span class="sxs-lookup"><span data-stu-id="86dfd-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="86dfd-105">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="86dfd-105">****Evaluation** \>**</span></span>|<span data-ttu-id="86dfd-106">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="86dfd-106">****Planning** \>**</span></span>|<span data-ttu-id="86dfd-107">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="86dfd-107">****Deployment** \>**</span></span>|<span data-ttu-id="86dfd-108">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="86dfd-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="86dfd-109">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="86dfd-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="86dfd-110">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="86dfd-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="86dfd-111">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="86dfd-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="86dfd-112">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="86dfd-112">You are here!</span></span>  <br/> [<span data-ttu-id="86dfd-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="86dfd-113">Next steps</span></span>](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="86dfd-p101">Предположим, что вы получаете оповещение, что один из вашей организации учетных записей пользователей для Office 365 фраза оказались раскрыты. Или Предположим, что вы получили предупреждения, которое указывает, что при наличии проблем с учетной записью пользователя. С помощью Office 365 облачных приложений безопасность можно приостановить учетной записи пользователя и восстанавливать после изучению оповещений, которое вы получаете.</span><span class="sxs-lookup"><span data-stu-id="86dfd-p101">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised. Or, suppose that you've received an alert that indicates something is wrong with a user account. With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="86dfd-p102">Безопасности приложения Office 365 облаке доступна в Office 365 корпоративный E5. Если ваша организация использует другой подписки Office 365 для предприятия, облачных приложений Office 365 безопасности можно приобрести в виде дополнительного компонента. (Как глобальный администратор, в центре администрирования Office 365 нажмите кнопку **выставления счетов** \> **Добавить подписок**.) Дополнительные сведения можно [Описание платформы Office 365: безопасность Office 365 &amp; центре соответствия требованиям](https://technet.microsoft.com/en-us/library/dn933793.aspx) и [покупке и изменить надстройки для Office 365 для бизнеса](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="86dfd-p102">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="86dfd-120">Чтобы приостановить учетной записи пользователя в облаке приложения Office 365 безопасности</span><span class="sxs-lookup"><span data-stu-id="86dfd-120">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="86dfd-p103">Чтобы запретить попытку пользователя, приостановить учетной записи пользователя. Это то же, что изменение учетной записи пользователя непосредственно в Office 365 для настройки состояние входа для **входа в заблокировано**.</span><span class="sxs-lookup"><span data-stu-id="86dfd-p103">When you suspend a user account, you prevent the user from signing in again. It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="86dfd-p104">Если запретить пользователю вход в Office 365, приостановка их или посредством изменения их состояние входа, обратите внимание, что может потребоваться час или, чтобы вступили в силу на всех устройствах и клиенты ([Редактирование или изменение пользователя в Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)) пользователя. Если пользователь входит в систему Office 365, блока вступят в силу при каждом Office 365 обязаны выполнять вход повторно.</span><span class="sxs-lookup"><span data-stu-id="86dfd-p104">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="86dfd-p105">Как [глобальный администратор или администратор безопасности](permissions-in-the-security-and-compliance-center.md), перейдите к [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы. (Вы перейдете к безопасности &amp; центре соответствия требованиям.)</span><span class="sxs-lookup"><span data-stu-id="86dfd-p105">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="86dfd-127">В разделе Безопасность &amp; центре соответствия требованиям, выберите **оповещения** \> **Расширенное Управление оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="86dfd-127">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="86dfd-128">Выберите, **перейдите к безопасности приложения Office 365 облака**.</span><span class="sxs-lookup"><span data-stu-id="86dfd-128">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите дополнительные оповещения для перехода к безопасности Office 365 облаке приложения](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="86dfd-130">На панели навигации в верхней части экрана выберите **оповещения**.</span><span class="sxs-lookup"><span data-stu-id="86dfd-130">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="86dfd-131">В столбце **оповещение** дважды щелкните предупреждение, которое относится к учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="86dfd-131">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="86dfd-132">В разделе **учетные записи**, в столбце **состояние** выбрать параметры ![значок Параметры](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend пользователя**.</span><span class="sxs-lookup"><span data-stu-id="86dfd-132">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="86dfd-133">Для восстановления учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="86dfd-133">To restore a user account</span></span>

<span data-ttu-id="86dfd-134">Просмотреть [Восстановление пользователя в Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span><span class="sxs-lookup"><span data-stu-id="86dfd-134">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="86dfd-135">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="86dfd-135">Next steps</span></span>

- [<span data-ttu-id="86dfd-136">Просмотр оповещений и реагирование на них в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="86dfd-136">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="86dfd-137">Управление разрешениями приложений с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="86dfd-137">Manage app permissions using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="86dfd-138">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="86dfd-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

