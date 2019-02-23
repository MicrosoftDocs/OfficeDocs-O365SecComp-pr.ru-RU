---
title: Настройка управления привилегированным доступом в Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: В этом разделе вы найдете дополнительные сведения о настройке привилегированного управления доступом в Office 365
ms.openlocfilehash: af8058ff852bbf290084e42d1f4c72d6fcee0e27
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221089"
---
# <a name="configuring-privileged-access-management-in-office-365"></a><span data-ttu-id="24906-103">Настройка управления привилегированным доступом в Office 365</span><span class="sxs-lookup"><span data-stu-id="24906-103">Configuring privileged access management in Office 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24906-104">В этом разделе рассматривается руководство по развертыванию и настройке для функций, доступных в Office 365 и расширенных конфигураций соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="24906-104">This topic covers deployment and configuration guidance for features only currently available in Office 365 E5 and Advanced Compliance SKUs.</span></span>

<span data-ttu-id="24906-p101">В этом разделе рассматривается включение и Настройка управления привилегированным доступом в организации Office 365. Для управления привилегированным доступом можно использовать центр администрирования Microsoft 365 или PowerShell управления Exchange.</span><span class="sxs-lookup"><span data-stu-id="24906-p101">This topic will guide you through enabling and configuring privileged access management in your Office 365 organization. You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span> 

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="24906-107">Включение и Настройка управления привилегированным доступом</span><span class="sxs-lookup"><span data-stu-id="24906-107">Enable and configure privileged access management</span></span>

<span data-ttu-id="24906-108">Выполните следующие действия, чтобы настроить и использовать привилегированный доступ в организации Office 365:</span><span class="sxs-lookup"><span data-stu-id="24906-108">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="24906-109">Шаг 1: создание группы утверждающего</span><span class="sxs-lookup"><span data-stu-id="24906-109">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="24906-p102">Прежде чем приступить к работе с правами на доступ к данным, определите, кто будет иметь право на утверждение входящих запросов на доступ к задачам с повышенными правами и привилегированным пользователям. Любой пользователь, являющийся участником группы утверждающих, сможет утверждать запросы на доступ. Эта возможность включена путем создания группы безопасности с включенной поддержкой почты в Office 365.</span><span class="sxs-lookup"><span data-stu-id="24906-p102">Before you start using privilege access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks. Any user who is part of the Approvers’ group will be able to approve access requests. This is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="24906-113">Шаг 2: включение привилегированного доступа</span><span class="sxs-lookup"><span data-stu-id="24906-113">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="24906-114">Привилегированный доступ должен быть явно включен в Office 365 с группой утверждающих по умолчанию и включать набор системных учетных записей, которые необходимо исключить из управления доступом для управления привилегированным доступом.</span><span class="sxs-lookup"><span data-stu-id="24906-114">Privileged access needs to be explicitly turned on in Office 365 with the default approver group and including a set of system accounts that you’d want to be excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="24906-115">Шаг 3: Создание политики доступа</span><span class="sxs-lookup"><span data-stu-id="24906-115">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="24906-p103">Создание политики утверждения позволяет определять конкретные требования к утверждению в рамках отдельных задач. Возможные варианты типа утверждения: **Auto** или **вручную**.</span><span class="sxs-lookup"><span data-stu-id="24906-p103">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks. The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="24906-118">Шаг 4: передача и утверждение привилегированных запросов доступа</span><span class="sxs-lookup"><span data-stu-id="24906-118">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="24906-p104">После включения привилегированный доступ требует утверждения для выполнения любой задачи, для которой определена соответствующая политика утверждения. Пользователи, которым требуется выполнить задачи, включенные в политику утверждения, должны запросить и получить утверждение доступа, чтобы иметь разрешения, необходимые для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="24906-p104">Once enabled, privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="24906-p105">После предоставления утверждения пользователь, выполняющий запрос, может выполнить предполагаемую задачу, а привилегированный доступ будет авторизовать и выполнить задачу от имени пользователя. Утверждение остается действительным в течение запрошенного периода (длительность по умолчанию составляет 4 часа), в течение которого инициатор запроса может выполнить нужную задачу несколько раз. Все подобные выполнения записываются в журнал и становятся доступны для аудита безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="24906-p105">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on users’ behalf. The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times. All such executions are logged and made available for security and compliance auditing.</span></span> 

> [!NOTE]
> <span data-ttu-id="24906-p106">Чтобы включить и настроить привилегированный доступ с помощью PowerShell для Exchange Management PowerShell, выполните действия, описанные в статье [Подключение к Exchange Online PowerShell с использованием многофакторной проверки](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) подлинности для подключения к Exchange Online PowerShell с помощью Office 365 записей. В организации Office 365 не требуется включать многофакторную проверку подлинности для включения привилегированного доступа при подключении к Exchange Online PowerShell. При подключении с многофакторной проверкой подлинности создается маркер OAuth, используемый привилегированным доступом для подписи запросов.</span><span class="sxs-lookup"><span data-stu-id="24906-p106">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials. You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell. Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="24906-127"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="24906-127"></span></span>

## <a name="step-1---create-an-approvers-group"></a><span data-ttu-id="24906-128">Шаг 1: создание группы утверждающего</span><span class="sxs-lookup"><span data-stu-id="24906-128">Step 1 - Create an approver's group</span></span>

1. <span data-ttu-id="24906-129">Войдите в [центр администрирования Microsoft 365](https://portal.office.com) с помощью учетных данных для учетной записи администратора в Организации.</span><span class="sxs-lookup"><span data-stu-id="24906-129">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="24906-130">В центре администрирования последовательно выберите пункты **группы** > **Добавить группу**.</span><span class="sxs-lookup"><span data-stu-id="24906-130">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="24906-131">Выберите тип группы **безопасности с поддержкой электронной почты** , а затем заполните поля **имя**, **адрес электронной почты группы**и **Описание** для новой группы.</span><span class="sxs-lookup"><span data-stu-id="24906-131">Select the **mail-enabled security group** group type and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="24906-p107">Сохраните группу. Для полной настройки группы и ее отображения в центре администрирования Office 365 может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="24906-p107">Save the group. It may take a few minutes for the group to be fully configured and to appear in the Office 365 Admin Center.</span></span>

5. <span data-ttu-id="24906-134">Выберите новую группу утверждающего и нажмите кнопку **изменить** , чтобы добавить пользователей в группу.</span><span class="sxs-lookup"><span data-stu-id="24906-134">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="24906-135">Сохраните группу.</span><span class="sxs-lookup"><span data-stu-id="24906-135">Save the group.</span></span>

<span data-ttu-id="24906-136"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="24906-136"></span></span>

## <a name="step-2---enable-privileged-access"></a><span data-ttu-id="24906-137">Шаг 2: включение привилегированного доступа</span><span class="sxs-lookup"><span data-stu-id="24906-137">Step 2 - Enable privileged access</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="24906-138">Использование центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24906-138">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="24906-139">Войдите в [центр администрирования Microsoft 365](https://portal.office.com) с помощью учетных данных для учетной записи администратора в Организации.</span><span class="sxs-lookup"><span data-stu-id="24906-139">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="24906-140">В центре администрирования перейдите к разделу **Параметры _гт_ безопасности _амп_** > безопасность с**правами на доступ к данным**.</span><span class="sxs-lookup"><span data-stu-id="24906-140">In the Admin Center, go to **Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="24906-141">Включите разрешение " **требовать утверждения для контроля привилегированного доступа** ".</span><span class="sxs-lookup"><span data-stu-id="24906-141">Enable the **Require approvals for privileged access** control.</span></span>

4. <span data-ttu-id="24906-142">Назначьте группу утверждающих, созданную на шаге 1, в качестве **группы утверждаЮщих по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="24906-142">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="24906-143">**Сохраните** и **закройте диалоговое окно**.</span><span class="sxs-lookup"><span data-stu-id="24906-143">**Save** and **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="24906-144">Использование PowerShell для управления Exchange</span><span class="sxs-lookup"><span data-stu-id="24906-144">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="24906-145">Выполните следующую команду в Exchange Online PowerShell, чтобы разрешить привилегированный доступ и назначить группу утверждающего:</span><span class="sxs-lookup"><span data-stu-id="24906-145">Run the following command in Exchange Online PowerShell to enable privileged access and to assign the approver's group:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```
<span data-ttu-id="24906-146">Пример.</span><span class="sxs-lookup"><span data-stu-id="24906-146">Example:</span></span>
```
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

> [!NOTE]
> <span data-ttu-id="24906-147">Функция "системные учетные записи" доступна, чтобы гарантировать, что определенные автоматизации в организациях могут работать без зависимости от привилегированного доступа, однако рекомендуется, чтобы такие исключения были исключительными и были разрешены и проверены. менять.</span><span class="sxs-lookup"><span data-stu-id="24906-147">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="24906-148"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="24906-148"></span></span>

## <a name="step-3---create-an-access-policy"></a><span data-ttu-id="24906-149">Шаг 3: Создание политики доступа</span><span class="sxs-lookup"><span data-stu-id="24906-149">Step 3 - Create an access policy</span></span>

<span data-ttu-id="24906-150">Вы можете создать и настроить до 30 политик доступа для организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="24906-150">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="24906-151">Использование центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24906-151">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="24906-152">Войдите в [центр администрирования Microsoft 365](https://portal.office.com) с помощью учетных данных для учетной записи администратора в Организации.</span><span class="sxs-lookup"><span data-stu-id="24906-152">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="24906-153">В центре администрирования перейдите к разделу **Параметры** > **безопасности _амп_ "конфиденциальность** > —**привилегированный доступ**".</span><span class="sxs-lookup"><span data-stu-id="24906-153">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="24906-154">Выберите **Управление политиками доступа и запросами**.</span><span class="sxs-lookup"><span data-stu-id="24906-154">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="24906-155">Выберите пункт **Настройка политик** и нажмите кнопку **Добавить политику**.</span><span class="sxs-lookup"><span data-stu-id="24906-155">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="24906-156">В раскрывающихся полях выберите соответствующие значения для вашей организации:</span><span class="sxs-lookup"><span data-stu-id="24906-156">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="24906-157">**Тип политики**: задача, роль или группа ролей</span><span class="sxs-lookup"><span data-stu-id="24906-157">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="24906-158">**Область применения политики**: Exchange или Office 365</span><span class="sxs-lookup"><span data-stu-id="24906-158">**Policy scope**: Exchange or Office 365</span></span>

    <span data-ttu-id="24906-159">**Имя политики**: выберите из доступных политик</span><span class="sxs-lookup"><span data-stu-id="24906-159">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="24906-160">**Тип утверждения**: вручную или автоматически</span><span class="sxs-lookup"><span data-stu-id="24906-160">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="24906-161">**Группа утверждения**: выберите группу утверждающих, созданную на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="24906-161">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="24906-p108">Выберите **создать** , а затем **Закрыть**. Полная настройка и включение политики может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="24906-p108">Select **Create** and then **Close**. It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="24906-164">Использование PowerShell для управления Exchange</span><span class="sxs-lookup"><span data-stu-id="24906-164">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="24906-165">Выполните следующую команду в Exchange Online PowerShell, чтобы создать и определить политику утверждения:</span><span class="sxs-lookup"><span data-stu-id="24906-165">Run the following command in Exchange Online PowerShell to create and define an approval policy:</span></span>

```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```
<span data-ttu-id="24906-166">Пример.</span><span class="sxs-lookup"><span data-stu-id="24906-166">Example:</span></span>
```
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="24906-167"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="24906-167"></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="24906-168">Шаг 4: передача и утверждение привилегированных запросов доступа</span><span class="sxs-lookup"><span data-stu-id="24906-168">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="24906-169">Запрос разрешения на повышение прав для выполнения привилегированных задач</span><span class="sxs-lookup"><span data-stu-id="24906-169">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="24906-p109">Запросы для привилегированного доступа действительны в течение 24 часов после отправки запроса. Если оно не утверждено или отклонено, срок действия запросов истечет и доступ не утверждается.</span><span class="sxs-lookup"><span data-stu-id="24906-p109">Requests for privileged access are valid for up to 24 hours after the request is submitted. If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="24906-172">Использование центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24906-172">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="24906-173">Войдите в [центр администрирования Microsoft 365](https://portal.office.com) , используя свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="24906-173">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="24906-174">В центре администрирования перейдите к разделу **Параметры** > **безопасности _амп_ "конфиденциальность** > —**привилегированный доступ**".</span><span class="sxs-lookup"><span data-stu-id="24906-174">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="24906-175">Выберите **Управление политиками доступа и запросами**.</span><span class="sxs-lookup"><span data-stu-id="24906-175">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="24906-p110">Выберите пункт **создать запрос**. В раскрывающихся полях выберите соответствующие значения для вашей организации:</span><span class="sxs-lookup"><span data-stu-id="24906-p110">Select **New request**. From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="24906-178">**Тип запроса**: задача, роль или группа ролей</span><span class="sxs-lookup"><span data-stu-id="24906-178">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="24906-179">**Область запроса**: Exchange</span><span class="sxs-lookup"><span data-stu-id="24906-179">**Request scope**: Exchange</span></span>

    <span data-ttu-id="24906-180">**Запрос для**: выберите из доступных политик</span><span class="sxs-lookup"><span data-stu-id="24906-180">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="24906-p111">**Продолжительность (часы)**: количество часов запрошенного доступа. Количество часов, которые можно запросить, не ограничено.</span><span class="sxs-lookup"><span data-stu-id="24906-p111">**Duration (hours)**: Number of hours of requested access. There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="24906-183">**Comments**: текстовое поле для комментариев, связанных с вашим запросом на доступ</span><span class="sxs-lookup"><span data-stu-id="24906-183">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="24906-p112">Нажмите кнопку **сохранить** , а затем кнопку **Закрыть**. Ваш запрос будет отправлен в группу утверждающего через электронную почту.</span><span class="sxs-lookup"><span data-stu-id="24906-p112">Select **Save** and then **Close**. Your request will be sent to the approver's group via email.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="24906-186">Использование PowerShell для управления Exchange</span><span class="sxs-lookup"><span data-stu-id="24906-186">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="24906-187">Выполните следующую команду в Exchange Online PowerShell, чтобы создать и отправить запрос на утверждение группе утверждающего.</span><span class="sxs-lookup"><span data-stu-id="24906-187">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```
<span data-ttu-id="24906-188">Пример.</span><span class="sxs-lookup"><span data-stu-id="24906-188">Example:</span></span>
```
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```
### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="24906-189">Просмотр состояния запросов на повышение прав</span><span class="sxs-lookup"><span data-stu-id="24906-189">View status of elevation requests</span></span>
<span data-ttu-id="24906-190">После создания запроса на утверждение состояние запроса на повышение прав можно просмотреть в центре администрирования или в Exchange Management PowerShell с помощью соответствующего идентификатора запроса.</span><span class="sxs-lookup"><span data-stu-id="24906-190">After an approval request is created, elevation request status can be reviewed in the Admin Center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="24906-191">Использование центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24906-191">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="24906-192">Войдите в [центр администрирования Microsoft 365](https://portal.office.com) , используя свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="24906-192">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="24906-193">В центре администрирования перейдите к разделу **Параметры** > **безопасности _амп_ "конфиденциальность** > —**привилегированный доступ**".</span><span class="sxs-lookup"><span data-stu-id="24906-193">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="24906-194">Выберите **Управление политиками доступа и запросами**.</span><span class="sxs-lookup"><span data-stu-id="24906-194">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="24906-195">Выберите **представление** , чтобы отфильтровать отправленные запросы по \*\*\*\* **очереди**, **утвержденИю**, отклонению или статусу **защищенного хранилища клиента** .</span><span class="sxs-lookup"><span data-stu-id="24906-195">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="24906-196">Использование PowerShell для управления Exchange</span><span class="sxs-lookup"><span data-stu-id="24906-196">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="24906-197">Выполните следующую команду в Exchange Online PowerShell, чтобы просмотреть состояние запроса на утверждение для определенного идентификатора запроса:</span><span class="sxs-lookup"><span data-stu-id="24906-197">Run the following command in Exchange Online PowerShell to view a approval request status for a specific request ID:</span></span>
```
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```
<span data-ttu-id="24906-198">Пример.</span><span class="sxs-lookup"><span data-stu-id="24906-198">Example:</span></span>
```
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="24906-199">Утверждение запроса на повышение прав на авторизацию</span><span class="sxs-lookup"><span data-stu-id="24906-199">Approving an elevation authorization request</span></span>
<span data-ttu-id="24906-p113">Когда создается запрос на утверждение, участники соответствующей группы утверждающего будут получать уведомления по электронной почте и могут утверждать запрос, связанный с ИДЕНТИФИКАТОРом запроса. Запрашивающий уведомляет об утверждении или отказе от запроса через электронное сообщение.</span><span class="sxs-lookup"><span data-stu-id="24906-p113">When an approval request is created, members of the relevant approver group will receive an email notification and can approve the request associated with the request ID. The requestor will be notified of the request approval or denial via email message.</span></span>

#### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="24906-202">Использование центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24906-202">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="24906-203">Войдите в [центр администрирования Microsoft 365](https://portal.office.com) , используя свои учетные данные.</span><span class="sxs-lookup"><span data-stu-id="24906-203">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using your credentials.</span></span>

2. <span data-ttu-id="24906-204">В центре администрирования перейдите к разделу **Параметры** > **безопасности _амп_ "конфиденциальность** > —**привилегированный доступ**".</span><span class="sxs-lookup"><span data-stu-id="24906-204">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="24906-205">Выберите **Управление политиками доступа и запросами**.</span><span class="sxs-lookup"><span data-stu-id="24906-205">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="24906-206">Выберите указанный запрос для просмотра сведений и выполнения действий по запросу.</span><span class="sxs-lookup"><span data-stu-id="24906-206">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="24906-p114">Выберите **утвердить** , чтобы утвердить запрос, или выберите **запретить** , чтобы отклонить запрос. Чтобы получить доступ к ранее утвержденным запросам, нажмите кнопку **отозвать**.</span><span class="sxs-lookup"><span data-stu-id="24906-p114">Select **Approve** to approve the request or select **Deny** to deny the request. Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="using-exchange-management-powershell"></a><span data-ttu-id="24906-209">Использование PowerShell для управления Exchange</span><span class="sxs-lookup"><span data-stu-id="24906-209">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="24906-210">Выполните следующую команду в Exchange Online PowerShell, чтобы утвердить запрос на повышение прав доступа:</span><span class="sxs-lookup"><span data-stu-id="24906-210">Run the following command in Exchange Online PowerShell to approve an elevation authorization request:</span></span>

```
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```
<span data-ttu-id="24906-211">Пример.</span><span class="sxs-lookup"><span data-stu-id="24906-211">Example:</span></span>
```
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="24906-212">Выполните следующую команду в Exchange Online PowerShell, чтобы отклонить запрос на повышение прав на авторизацию:</span><span class="sxs-lookup"><span data-stu-id="24906-212">Run the following command in Exchange Online PowerShell to deny an elevation authorization request:</span></span>

```
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```
<span data-ttu-id="24906-213">Пример.</span><span class="sxs-lookup"><span data-stu-id="24906-213">Example:</span></span>
```
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="24906-214">Удаление политики привилегированного доступа в Office 365</span><span class="sxs-lookup"><span data-stu-id="24906-214">Delete a privileged access policy in Office 365</span></span>
<span data-ttu-id="24906-215">Вы можете удалить политику привилегированного доступа, если она больше не нужна в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="24906-215">You can delete a privileged access policy if it is no longer needed in your organization.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="24906-216">Использование центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24906-216">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="24906-217">Войдите в [центр администрирования Microsoft 365](https://portal.office.com) с помощью учетных данных для учетной записи администратора в Организации.</span><span class="sxs-lookup"><span data-stu-id="24906-217">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="24906-218">В центре администрирования перейдите к разделу **Параметры** > **безопасности _амп_ "конфиденциальность** > —**привилегированный доступ**".</span><span class="sxs-lookup"><span data-stu-id="24906-218">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="24906-219">Выберите **Управление политиками доступа и запросами**.</span><span class="sxs-lookup"><span data-stu-id="24906-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="24906-220">Выберите пункт **Настройка политик**.</span><span class="sxs-lookup"><span data-stu-id="24906-220">Select **Configure policies**.</span></span>

5. <span data-ttu-id="24906-221">Выберите политику, которую нужно удалить, а затем нажмите кнопку **удалить политику**.</span><span class="sxs-lookup"><span data-stu-id="24906-221">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="24906-222">Нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="24906-222">Select **Close**.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="24906-223">Использование PowerShell для управления Exchange</span><span class="sxs-lookup"><span data-stu-id="24906-223">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="24906-224">Выполните следующую команду в Exchange Online PowerShell, чтобы удалить политику привилегированного доступа:</span><span class="sxs-lookup"><span data-stu-id="24906-224">Run the following command in Exchange Online Powershell to delete a privileged access policy:</span></span>

```
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="24906-225">Отключение привилегированного доступа в Office 365</span><span class="sxs-lookup"><span data-stu-id="24906-225">Disable privileged access in Office 365</span></span>

<span data-ttu-id="24906-p115">При необходимости вы можете отключить управление привилегированным доступом для своей организации. При отключении привилегированного доступа не удаляются все связанные с ним политики утверждения или группы утверждающих.</span><span class="sxs-lookup"><span data-stu-id="24906-p115">If needed, you can disable privileged access management for your organization. Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="using-the-microsoft-365-admin-center"></a><span data-ttu-id="24906-228">Использование центра администрирования Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="24906-228">Using the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="24906-229">Войдите в [центр администрирования Microsoft 365](https://portal.office.com) с помощью учетных данных для учетной записи администратора в Организации.</span><span class="sxs-lookup"><span data-stu-id="24906-229">Sign into the [Microsoft 365 Admin Center](https://portal.office.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="24906-230">В центре администрирования перейдите к разделу **Параметры** > **безопасности _амп_ "конфиденциальность** > —**привилегированный доступ**".</span><span class="sxs-lookup"><span data-stu-id="24906-230">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="24906-231">Включите разрешение " **требовать утверждения для контроля привилегированного доступа** ".</span><span class="sxs-lookup"><span data-stu-id="24906-231">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="using-exchange-management-powershell"></a><span data-ttu-id="24906-232">Использование PowerShell для управления Exchange</span><span class="sxs-lookup"><span data-stu-id="24906-232">Using Exchange Management PowerShell</span></span>

<span data-ttu-id="24906-233">Выполните следующую команду в Exchange Online PowerShell, чтобы отключить привилегированный доступ:</span><span class="sxs-lookup"><span data-stu-id="24906-233">Run the following command in Exchange Online Powershell to disable privileged access:</span></span>

```
Disable-ElevatedAccessControl
```