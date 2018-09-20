---
title: Настройка управления правами доступа в Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Используйте этот раздел для получения дополнительных сведений о настройке управление правами доступа в Office 365
ms.openlocfilehash: 6494505554a02f005df8f45839c9575094acbf1a
ms.sourcegitcommit: d31904e81f81d0fba75309a2bc8bbfb05565a0b4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/20/2018
ms.locfileid: "24055254"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="e81c1-103">Настройка управления правами доступа в Office 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e81c1-104">В этом разделе описывается развертывание и конфигурация рекомендации для функций в настоящее время доступны только в Office 365 E5 и дополнительные номера SKU соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="e81c1-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="e81c1-p101">В этом разделе приведены рекомендации по Включение и настройка управления правами доступа в организации Office 365. Можно использовать либо Центр администрирования Microsoft 365 или управления Exchange PowerShell для управления и использовать привилегированный доступ.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="e81c1-107">Включение и настройка управления правами доступа</span><span class="sxs-lookup"><span data-stu-id="e81c1-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="e81c1-108">Выполните следующие действия для установки и использования привилегированной доступа в организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="e81c1-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="e81c1-109">Шаг 1: Создание группы утверждающий</span><span class="sxs-lookup"><span data-stu-id="e81c1-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="e81c1-p102">Прежде чем начать, с помощью принципу предоставления минимальных прав доступа, определение пользователей, которые будут иметь Центр утверждения для входящих запросов для доступа к задачам с повышенными привилегиями и правами. Любой пользователь, который является частью в группе утверждающих будет иметь возможность утверждать запросы доступа. Этот параметр включен, создав группу безопасности с включенной поддержкой почты в Office 365.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="e81c1-113">Шаг 2: Включение привилегированный доступ</span><span class="sxs-lookup"><span data-stu-id="e81c1-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="e81c1-114">Привилегированный доступ должен явно включены в Office 365 с помощью группы утверждающий по умолчанию и включая набор системных учетных записей, которые необходимо исключить из управления доступом управления правами доступа.</span><span class="sxs-lookup"><span data-stu-id="e81c1-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="e81c1-115">Шаг 3: Создание политики доступа</span><span class="sxs-lookup"><span data-stu-id="e81c1-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="e81c1-p103">Создание политики утверждения позволяет определить требования к определенным утверждения, областью действия по отдельным задачам. Параметры типа утверждения, **автоматически** или **вручную**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="e81c1-118">Шаг 4: Отправка и утверждение привилегированный доступ запросов</span><span class="sxs-lookup"><span data-stu-id="e81c1-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="e81c1-p104">Один раз включена, правами доступа требует утверждения для выполнения любой задачи, с которой определена политика связанного утверждения. Пользователи, которым необходимо выполнение задач, включенных в политику утверждения необходимо запросить и получить утверждение доступа для разрешения, необходимые для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="e81c1-p105">После предоставления утверждения запроса пользователь может выполнять поставленной задачи и привилегированный доступ будет авторизации и выполнения задач от имени пользователя. Утверждение действителен для запрошенного duration (длительность по умолчанию — 4 часа), во время которого инициатор запроса может выполняться поставленной задачи несколько раз. Все выполнений вход и делаются доступными для безопасности и контроля соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="e81c1-p106">Чтобы с помощью PowerShell управления Exchange для включения и настройки привилегированный доступ, выполните действия, описанные в [подключение к Exchange Online PowerShell с помощью многофакторной проверки подлинности](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) для подключения к Exchange Online PowerShell с помощью Office 365 учетные данные пользователя. Необходимо включить многофакторной проверки подлинности для организации Office 365, выполните действия, чтобы включить привилегированный доступ при подключении к Exchange Online PowerShell. Подключение к многофакторной проверки подлинности создает маркер OAuth, используемый с правами доступа для ваших запросов для подписи.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="e81c1-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="e81c1-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="e81c1-128">Шаг 1 - Создание группы утверждающий</span><span class="sxs-lookup"><span data-stu-id="e81c1-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="e81c1-129">Войдите в [Центр администрирования Microsoft 365](https://portal.office.com) , используя учетные данные для учетной записи администратора в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e81c1-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="e81c1-130">В центре администрирования перейдите к **группам** > **Добавить группу**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="e81c1-131">Выберите тип группы **Группа безопасности с включенной поддержкой почты** и затем заполните поля **имя**, **адрес электронной почты группы**и **Описание** для новой группы.</span><span class="sxs-lookup"><span data-stu-id="e81c1-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="e81c1-p107">Сохраните группу. Может занять несколько минут для группы полностью задаются и отображаются в центре администрирования Office 365.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="e81c1-134">Выберите новый утверждающий группы и выберите **Изменить** , чтобы добавить пользователей в группу.</span><span class="sxs-lookup"><span data-stu-id="e81c1-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="e81c1-135">Сохраните группу.</span><span class="sxs-lookup"><span data-stu-id="e81c1-135">Save the group.</span></span>

<span data-ttu-id="e81c1-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="e81c1-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="e81c1-137">Шаг 2 - разрешение правами доступа</span><span class="sxs-lookup"><span data-stu-id="e81c1-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="e81c1-138">С помощью центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="e81c1-139">Войдите в [Центр администрирования Microsoft 365](https://portal.office.com) , используя учетные данные для учетной записи администратора в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e81c1-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="e81c1-140">В центре администрирования, перейдите в раздел **Параметры > Безопасность и конфиденциальность** > **правами доступа**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="e81c1-141">Включение управления **Требовать утверждения для привилегированный доступ** .</span><span class="sxs-lookup"><span data-stu-id="e81c1-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="e81c1-142">Назначьте его группы, созданной в шаге 1 в качестве **утверждающих группа по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="e81c1-143">**Сохранить** и **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="e81c1-144">С помощью PowerShell управления Exchange</span><span class="sxs-lookup"><span data-stu-id="e81c1-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="e81c1-145">Выполните следующую команду в Exchange Online PowerShell для включения правами доступа и Назначение группы утверждающий:</span><span class="sxs-lookup"><span data-stu-id="e81c1-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="e81c1-146">Пример.</span><span class="sxs-lookup"><span data-stu-id="e81c1-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="e81c1-147">Системных учетных записей, что компонент можно сделать доступной для обеспечения определенных automations в вашей организации могут работать без зависимостей привилегированный доступ, однако рекомендуется такое исключения быть исключительных и входящих должен быть одобрен и проверены регулярно.</span><span class="sxs-lookup"><span data-stu-id="e81c1-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="e81c1-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="e81c1-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="e81c1-149">Шаг 3 - Создание политики доступа</span><span class="sxs-lookup"><span data-stu-id="e81c1-149">Step 3 - Create an access policy</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="e81c1-150">С помощью центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-150">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="e81c1-151">Войдите в [Центр администрирования Microsoft 365](https://portal.office.com) , используя учетные данные для учетной записи администратора в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e81c1-151">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="e81c1-152">В центре администрирования, перейдите в раздел **Параметры** > **безопасности и конфиденциальности** > **правами доступа**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-152">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="e81c1-153">Выберите **Управление политиками доступа и запросов**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-153">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="e81c1-154">Выберите **Настройка политик** , а затем выберите **Добавить политику**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-154">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="e81c1-155">Из раскрывающегося списка полей выберите соответствующие значения для вашей организации:</span><span class="sxs-lookup"><span data-stu-id="e81c1-155">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="e81c1-156">**Тип политики**: задачи, роли или группе ролей</span><span class="sxs-lookup"><span data-stu-id="e81c1-156">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="e81c1-157">**Область действия политики**: Exchange или Office 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-157">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="e81c1-158">**Имя политики**: выберите из доступных политик</span><span class="sxs-lookup"><span data-stu-id="e81c1-158">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="e81c1-159">**Тип утверждения**: вручную или автоматически</span><span class="sxs-lookup"><span data-stu-id="e81c1-159">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="e81c1-160">**Группа утверждения**: выберите утверждающие группу, созданную на шаге 1</span><span class="sxs-lookup"><span data-stu-id="e81c1-160">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="e81c1-p108">Выберите **Создать** и затем **Закрыть**. Может занять несколько минут для политики, чтобы полностью настроить и включить.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="e81c1-163">С помощью PowerShell управления Exchange</span><span class="sxs-lookup"><span data-stu-id="e81c1-163">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="e81c1-164">Выполните следующую команду в Exchange Online PowerShell для создания и определить политику утверждения:</span><span class="sxs-lookup"><span data-stu-id="e81c1-164">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="e81c1-165">Пример.</span><span class="sxs-lookup"><span data-stu-id="e81c1-165">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="e81c1-166"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="e81c1-166"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="e81c1-167">Шаг 4: Отправка и утверждение привилегированный доступ запросов</span><span class="sxs-lookup"><span data-stu-id="e81c1-167">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="e81c1-168">Разрешения на запрос несанкционированное получение прав авторизации для выполнения привилегированных задач</span><span class="sxs-lookup"><span data-stu-id="e81c1-168">Requesting elevation authorization to execute privileged tasks</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="e81c1-169">С помощью центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-169">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="e81c1-170">Войдите в [Центр администрирования Microsoft 365](https://portal.office.com) , используя учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e81c1-170">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="e81c1-171">В центре администрирования, перейдите в раздел **Параметры** > **безопасности и конфиденциальности** > **правами доступа**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-171">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="e81c1-172">Выберите **Управление политиками доступа и запросов**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-172">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="e81c1-p109">Выберите **Создать запрос**. Из раскрывающегося списка полей выберите соответствующие значения для вашей организации:</span><span class="sxs-lookup"><span data-stu-id="e81c1-p109">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="e81c1-175">**Тип запроса**: задачи, роли или группе ролей</span><span class="sxs-lookup"><span data-stu-id="e81c1-175">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="e81c1-176">**Область запроса**: Exchange</span><span class="sxs-lookup"><span data-stu-id="e81c1-176">**Request scope**: Exchange</span></span>

    <span data-ttu-id="e81c1-177">**Запрос**: выберите из доступных политик</span><span class="sxs-lookup"><span data-stu-id="e81c1-177">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="e81c1-178">**Длительность (в часах)**: количество часов, запрашиваемый доступа</span><span class="sxs-lookup"><span data-stu-id="e81c1-178">**Duration (hours)**: Number of hours of requested access</span></span>

    <span data-ttu-id="e81c1-179">**Комментарии**: текстовое поле для примечаний, связанные с запрос на доступ</span><span class="sxs-lookup"><span data-stu-id="e81c1-179">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="e81c1-p110">Выберите **Сохранить** и **Закрыть**. Запрос будет отправляться группы утверждающий по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p110">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="e81c1-182">С помощью PowerShell управления Exchange</span><span class="sxs-lookup"><span data-stu-id="e81c1-182">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="e81c1-183">Выполните следующую команду в Exchange Online PowerShell для создания и отправки запроса на утверждение утверждающий группе:</span><span class="sxs-lookup"><span data-stu-id="e81c1-183">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="e81c1-184">Пример.</span><span class="sxs-lookup"><span data-stu-id="e81c1-184">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="e81c1-185">Просмотр состояния запросы на повышение прав</span><span class="sxs-lookup"><span data-stu-id="e81c1-185">View status of elevation requests</span></span>
<span data-ttu-id="e81c1-186">После создания запроса на утверждение, можно просматривать состояние запроса на повышение прав в центре администрирования или в Exchange PowerShell управления с помощью связанного с запросом на код.</span><span class="sxs-lookup"><span data-stu-id="e81c1-186">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="e81c1-187">С помощью центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-187">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="e81c1-188">Войдите в [Центр администрирования Microsoft 365](https://portal.office.com) , используя учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e81c1-188">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="e81c1-189">В центре администрирования, перейдите в раздел **Параметры** > **безопасности и конфиденциальности** > **правами доступа**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-189">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="e81c1-190">Выберите **Управление политиками доступа и запросов**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-190">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="e81c1-191">Выберите **представление** для фильтрации отправленных запросов по состоянию **ожидающих**, **Утверждено**, **Отклонено**или **Защищенного хранилища клиента** .</span><span class="sxs-lookup"><span data-stu-id="e81c1-191">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="e81c1-192">С помощью PowerShell управления Exchange</span><span class="sxs-lookup"><span data-stu-id="e81c1-192">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="e81c1-193">Выполните следующую команду в Exchange Online PowerShell для просмотра состояния запросов утверждения для код конкретного запроса:</span><span class="sxs-lookup"><span data-stu-id="e81c1-193">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="e81c1-194">Пример.</span><span class="sxs-lookup"><span data-stu-id="e81c1-194">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="e81c1-195">Утверждение запроса на повышение прав авторизации</span><span class="sxs-lookup"><span data-stu-id="e81c1-195">Approving an elevation authorization request</span></span>
<span data-ttu-id="e81c1-p111">При создании запроса на утверждение, участники группы соответствующих утверждающий будет получать уведомления по электронной почте и может утвердить запрос, связанный с идентификатором запроса. Утверждение запроса или отказ через сообщения электронной почты будут извещены инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p111">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="e81c1-198">С помощью центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-198">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="e81c1-199">Войдите в [Центр администрирования Microsoft 365](https://portal.office.com) , используя учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e81c1-199">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="e81c1-200">В центре администрирования, перейдите в раздел **Параметры** > **безопасности и конфиденциальности** > **правами доступа**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-200">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="e81c1-201">Выберите **Управление политиками доступа и запросов**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-201">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="e81c1-202">Выберите перечисленных запрос для просмотра сведений и выполнять операции запроса.</span><span class="sxs-lookup"><span data-stu-id="e81c1-202">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="e81c1-p112">Выберите **Утвердить** , чтобы утвердить запрос или выберите **Запретить** , чтобы отклонить запрос. Ранее одобренные запросы могут иметь доступ отозван, выбрав **Отозвать**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p112">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="e81c1-205">С помощью PowerShell управления Exchange</span><span class="sxs-lookup"><span data-stu-id="e81c1-205">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="e81c1-206">Выполните следующую команду в Exchange Online PowerShell, чтобы утвердить запрос повышения авторизации:</span><span class="sxs-lookup"><span data-stu-id="e81c1-206">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="e81c1-207">Пример.</span><span class="sxs-lookup"><span data-stu-id="e81c1-207">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="e81c1-208">Выполните следующую команду в Exchange Online PowerShell, чтобы запретить запрос повышения авторизации:</span><span class="sxs-lookup"><span data-stu-id="e81c1-208">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="e81c1-209">Пример.</span><span class="sxs-lookup"><span data-stu-id="e81c1-209">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="e81c1-210">Отключение правами доступа в Office 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-210">Disable privileged access in Office 365</span></span>

<span data-ttu-id="e81c1-p113">При необходимости можно отключить управление правами доступа для вашей организации. Отключение привилегиями доступа не удалять любые политики связанного утверждения или утверждающий группы.</span><span class="sxs-lookup"><span data-stu-id="e81c1-p113">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="e81c1-213">С помощью центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e81c1-213">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="e81c1-214">Войдите в [Центр администрирования Microsoft 365](https://portal.office.com) , используя учетные данные для учетной записи администратора в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e81c1-214">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="e81c1-215">В центре администрирования, перейдите в раздел **Параметры** > **безопасности и конфиденциальности** > **правами доступа**.</span><span class="sxs-lookup"><span data-stu-id="e81c1-215">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="e81c1-216">Включение управления **Требовать утверждения для привилегированный доступ** .</span><span class="sxs-lookup"><span data-stu-id="e81c1-216">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="e81c1-217">С помощью PowerShell управления Exchange</span><span class="sxs-lookup"><span data-stu-id="e81c1-217">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="e81c1-218">Выполните следующую команду в Exchange Online Powershell, чтобы отключить правами доступа:</span><span class="sxs-lookup"><span data-stu-id="e81c1-218">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```