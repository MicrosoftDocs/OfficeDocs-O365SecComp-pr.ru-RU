---
title: Изменение или удаление политик барьера информации
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/24/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Узнайте, как изменить или удалить политики для барьеров информации.
ms.openlocfilehash: e6bed4df2329d426f86bd4cde07bdc7d1a2792cd
ms.sourcegitcommit: 7c48ce016fa9f45a3813467f7c5a2fd72f9b8f49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/25/2019
ms.locfileid: "35215652"
---
# <a name="edit-or-remove-information-barrier-policies-preview"></a><span data-ttu-id="4e559-103">Изменение или удаление политик барьера информации (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="4e559-103">Edit or remove information barrier policies (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="4e559-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="4e559-104">Overview</span></span>

<span data-ttu-id="4e559-105">После [определения политик барьера информации](information-barriers-policies.md)может потребоваться внести изменения в эти политики или в сегменты пользователей в рамках [устранения неполадок](information-barriers-troubleshooting.md) или обычного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="4e559-105">After you have [defined information barrier policies](information-barriers-policies.md), you might need to make changes to those policies or to your user segments, as part of [troubleshooting](information-barriers-troubleshooting.md) or as regular maintenance.</span></span> <span data-ttu-id="4e559-106">Используйте эту статью в качестве руководства.</span><span class="sxs-lookup"><span data-stu-id="4e559-106">Use this article as a guide.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e559-107">Для выполнения задач, описанных в этой статье, необходимо назначить соответствующую роль, например один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="4e559-107">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span><br/><span data-ttu-id="4e559-108">— Корпоративный глобальный администратор Майкрософт 365</span><span class="sxs-lookup"><span data-stu-id="4e559-108">- Microsoft 365 Enterprise Global Administrator</span></span><br/><span data-ttu-id="4e559-109">— Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="4e559-109">- Office 365 Global Administrator</span></span><br/><span data-ttu-id="4e559-110">— Администратор соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="4e559-110">- Compliance Administrator</span></span><br/><span data-ttu-id="4e559-111">-"Управление соответствием требованиям" (это новая роль);</span><span class="sxs-lookup"><span data-stu-id="4e559-111">- IB Compliance Management (this is a new role!)</span></span><p><span data-ttu-id="4e559-112">Чтобы узнать больше о предварительных требованиях для барьеров информации, ознакомьтесь со статьей [Предварительные требования (для политик барьера информации)](information-barriers-policies.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="4e559-112">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span><p><span data-ttu-id="4e559-113">Обязательно подключитесь [к PowerShell центра безопасности Office 365 & соответствия требованиям](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="4e559-113">Make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="edit-user-account-attributes"></a><span data-ttu-id="4e559-114">Изменение атрибутов учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="4e559-114">Edit user account attributes</span></span>

<span data-ttu-id="4e559-115">Эта процедура используется для изменения атрибутов, используемых для сегментирования пользователей.</span><span class="sxs-lookup"><span data-stu-id="4e559-115">Use this procedure to edit attributes that are used for segmenting users.</span></span> 

<span data-ttu-id="4e559-116">Например, если вы используете атрибут Department, а одна или несколько учетных записей пользователей в данный момент не имеют значений для отдела, необходимо изменить эти учетные записи пользователей, включив сведения о отделе.</span><span class="sxs-lookup"><span data-stu-id="4e559-116">For example, if you are using a Department attribute, and one or more user accounts do not currently have any values listed for Department, you must edit those user accounts to include Department information.</span></span> 

<span data-ttu-id="4e559-117">Атрибуты учетной записи пользователя используются для определения сегментов, чтобы можно было назначать политики барьера информации.</span><span class="sxs-lookup"><span data-stu-id="4e559-117">User account attributes are used for defining segments so that information barrier policies can be assigned.</span></span>

1. <span data-ttu-id="4e559-118">Чтобы просмотреть сведения об определенной учетной записи пользователя, например значений атрибутов и назначенных сегментах, используйте командлет **Get-информатионбарриерреЦипиентстатус** с параметром Identity.</span><span class="sxs-lookup"><span data-stu-id="4e559-118">To view details for a specific user account, such as attribute values and assigned segment(s), use the **Get-InformationBarrierRecipientStatus** cmdlet with Identity parameters.</span></span> 

   <span data-ttu-id="4e559-119">Инструкции`Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span><span class="sxs-lookup"><span data-stu-id="4e559-119">Syntax: `Get-InformationBarrierRecipientStatus -Identity <value> -Identity2 <value>`</span></span> 
    
   <span data-ttu-id="4e559-120">Можно использовать любое значение, однозначно идентифицирующее каждого пользователя, например, имя, псевдоним, различающееся имя, каноническое имя домена, адрес электронной почты или GUID.</span><span class="sxs-lookup"><span data-stu-id="4e559-120">You can use any value that uniquely identifies each user, such as name, alias, distinguished name, canonical domain name, email address, or GUID.</span></span> 
    
   <span data-ttu-id="4e559-121">Пример: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span><span class="sxs-lookup"><span data-stu-id="4e559-121">Example: `Get-InformationBarrierRecipientStatus -Identity meganb -Identity2 alexw`</span></span> 
    
   <span data-ttu-id="4e559-122">В этом примере мы будем называть две учетные записи пользователей в Office 365: *меганб* для *Меган*и *алексв* для *Алекс*.</span><span class="sxs-lookup"><span data-stu-id="4e559-122">In this example, we refer to two user accounts in Office 365: *meganb* for *Megan*, and *alexw* for *Alex*.</span></span> 
    
   <span data-ttu-id="4e559-123">(Вы также можете использовать этот командлет для одного пользователя: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span><span class="sxs-lookup"><span data-stu-id="4e559-123">(You can also use this cmdlet for a single user: `Get-InformationBarrierRecipientStatus -Identity <value>`)</span></span> 
    
2. <span data-ttu-id="4e559-124">Определите атрибут, который вы хотите изменить, для профилей учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="4e559-124">Determine which attribute you want to edit for your user account profile(s).</span></span> <span data-ttu-id="4e559-125">Дополнительные сведения см. в разделе [Attributes for Information Information Policies (Preview)](information-barriers-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="4e559-125">Refer to [Attributes for information barrier policies (Preview)](information-barriers-attributes.md) for more details.</span></span> 

3. <span data-ttu-id="4e559-126">Измените одну или несколько учетных записей пользователей, чтобы включить значения для атрибута, выбранного на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="4e559-126">Edit one or more user accounts to include values for the attribute you selected in the previous step.</span></span> <span data-ttu-id="4e559-127">Для этого используйте одну из следующих процедур:</span><span class="sxs-lookup"><span data-stu-id="4e559-127">To do this, use one of the following procedures:</span></span>

    - <span data-ttu-id="4e559-128">Чтобы изменить одну учетную запись, ознакомьтесь со статьей [Добавление или обновление данных профиля пользователя с помощью Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="4e559-128">To edit a single account, see [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal).</span></span>

    - <span data-ttu-id="4e559-129">Чтобы изменить несколько учетных записей (или с помощью PowerShell для редактирования одной учетной записи), ознакомьтесь со статьей [Настройка свойств учетной записи пользователя с помощью Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="4e559-129">To edit multiple accounts (or use PowerShell to edit a single account), see [Configure user account properties with Office 365 PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/configure-user-account-properties-with-office-365-powershell).</span></span>

## <a name="edit-a-segment"></a><span data-ttu-id="4e559-130">Изменение сегмента</span><span class="sxs-lookup"><span data-stu-id="4e559-130">Edit a segment</span></span>

<span data-ttu-id="4e559-131">Используйте эту процедуру, чтобы изменить определение пользовательского сегмента.</span><span class="sxs-lookup"><span data-stu-id="4e559-131">Use this procedure edit the definition of a user segment.</span></span> <span data-ttu-id="4e559-132">Например, вы можете изменить имя сегмента или фильтр, который используется для определения пользователей, включенных в сегмент.</span><span class="sxs-lookup"><span data-stu-id="4e559-132">For example, you might change the name of a segment, or the filter that is used to determine who's included in the segment.</span></span>

1. <span data-ttu-id="4e559-133">Чтобы просмотреть все существующие сегменты, используйте командлет **Get – организатионсегмент** .</span><span class="sxs-lookup"><span data-stu-id="4e559-133">To view all existing segments, use the **Get-OrganizationSegment** cmdlet.</span></span>
    
    <span data-ttu-id="4e559-134">Инструкции`Get-OrganizationSegment`</span><span class="sxs-lookup"><span data-stu-id="4e559-134">Syntax: `Get-OrganizationSegment`</span></span>

    <span data-ttu-id="4e559-135">Вы увидите список сегментов и сведений для каждого из них, например тип сегмента, его значение Усерграупфилтер, кто создал или последним изменил его, GUID и т. д.</span><span class="sxs-lookup"><span data-stu-id="4e559-135">You will see a list of segments and details for each, such as segment type, its UserGroupFilter value, who created or last modified it, GUID, and so on.</span></span>

    > [!TIP]
    > <span data-ttu-id="4e559-136">Печать или сохранение списка сегментов для последующей ссылки.</span><span class="sxs-lookup"><span data-stu-id="4e559-136">Print or save your list of segments for reference later.</span></span> <span data-ttu-id="4e559-137">Например, если вы хотите изменить сегмент, необходимо знать его имя или указать значение (используется с параметром Identity).</span><span class="sxs-lookup"><span data-stu-id="4e559-137">For example, if you want to edit a segment, you will need to know its name or identify value (this is used with the Identity parameter).</span></span>

2. <span data-ttu-id="4e559-138">Чтобы изменить сегмент, используйте командлет **Set – организатионсегмент** с параметром **Identity** и соответствующими сведениями.</span><span class="sxs-lookup"><span data-stu-id="4e559-138">To edit a segment, use the **Set-OrganizationSegment** cmdlet with the **Identity** parameter and relevant details.</span></span> 

    <span data-ttu-id="4e559-139">Инструкции`Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span><span class="sxs-lookup"><span data-stu-id="4e559-139">Syntax: `Set-OrganizationSegment -Identity GUID -UserGroupFilter "attribute -eq 'attributevalue'"`</span></span>

    <span data-ttu-id="4e559-140">Пример: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span><span class="sxs-lookup"><span data-stu-id="4e559-140">Example: `Set-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd -UserGroupFilter "Department -eq 'HRDept'"`</span></span>

    <span data-ttu-id="4e559-141">В этом примере для сегмента с GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*мы обновили название отдела на "хрдепт".</span><span class="sxs-lookup"><span data-stu-id="4e559-141">In this example, for the segment that has the GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*, we updated the department name to "HRDept".</span></span>

<span data-ttu-id="4e559-142">После завершения редактирования сегментов для организации можно [определить](information-barriers-policies.md#part-2-define-information-barrier-policies) или [изменить](#edit-a-policy) политики барьера информации.</span><span class="sxs-lookup"><span data-stu-id="4e559-142">When you have finished editing segments for your organization, you can either [define](information-barriers-policies.md#part-2-define-information-barrier-policies) or [edit](#edit-a-policy) information barrier policies.</span></span>

## <a name="edit-a-policy"></a><span data-ttu-id="4e559-143">Изменение политики</span><span class="sxs-lookup"><span data-stu-id="4e559-143">Edit a policy</span></span>

1. <span data-ttu-id="4e559-144">Чтобы просмотреть список текущих политик барьера информации, используйте командлет **Get – информатионбарриерполици** .</span><span class="sxs-lookup"><span data-stu-id="4e559-144">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="4e559-145">Инструкции`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="4e559-145">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="4e559-146">В списке результатов Определите политику, которую необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="4e559-146">In the list of results, identify the policy that you want to change.</span></span> <span data-ttu-id="4e559-147">Обратите внимание на GUID и имя политики.</span><span class="sxs-lookup"><span data-stu-id="4e559-147">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="4e559-148">Используйте командлет **Set – информатионбарриерполици** с параметром **Identity** и укажите изменения, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="4e559-148">Use the **Set-InformationBarrierPolicy** cmdlet with an **Identity** parameter, and specify the changes you want to make.</span></span>

    <span data-ttu-id="4e559-149">Пример: Предположим, что политика была определена для блокирования связи между сегментом *исследований* и сегментами *сбыта* и *маркетинга* .</span><span class="sxs-lookup"><span data-stu-id="4e559-149">Example: Suppose a policy was defined to block the *Research* segment from communicating with the *Sales* and *Marketing* segments.</span></span> <span data-ttu-id="4e559-150">Политика была определена с помощью этого командлета:`New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span><span class="sxs-lookup"><span data-stu-id="4e559-150">The policy was defined by using this cmdlet: `New-InformationBarrierPolicy -Name "Research-SalesMarketing" -AssignedSegment "Research" -SegmentsBlocked "Sales","Marketing"`</span></span>
    
    <span data-ttu-id="4e559-151">Предположим, что мы хотим изменить его, чтобы люди в сегменте *исследований* могли общаться только с людьми в сегменте *кадров* .</span><span class="sxs-lookup"><span data-stu-id="4e559-151">Suppose we want to change it so that people in the *Research* segment can only communicate with people in the *HR* segment.</span></span> <span data-ttu-id="4e559-152">Чтобы внести это изменение, мы используем следующий командлет:`Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span><span class="sxs-lookup"><span data-stu-id="4e559-152">To make this change, we use this cmdlet: `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471 -SegmentsAllowed "HR"`</span></span>

    <span data-ttu-id="4e559-153">В этом примере мы изменили "Сегментсблоккед" на "Сегментсалловед" и указали сегмент *HR* .</span><span class="sxs-lookup"><span data-stu-id="4e559-153">In this example, we changed "SegmentsBlocked" to "SegmentsAllowed" and specified the *HR* segment.</span></span>

3. <span data-ttu-id="4e559-154">Завершив изменение политики, не забудьте применить внесенные изменения.</span><span class="sxs-lookup"><span data-stu-id="4e559-154">When you are finished editing a policy, make sure to apply your changes.</span></span> <span data-ttu-id="4e559-155">(См. раздел [применение политик барьера информации](information-barriers-policies.md#part-3-apply-information-barrier-policies)).</span><span class="sxs-lookup"><span data-stu-id="4e559-155">(See [Apply information barrier policies](information-barriers-policies.md#part-3-apply-information-barrier-policies).)</span></span>

## <a name="set-a-policy-to-inactive-status"></a><span data-ttu-id="4e559-156">Установка для политики неактивного состояния</span><span class="sxs-lookup"><span data-stu-id="4e559-156">Set a policy to inactive status</span></span>

1. <span data-ttu-id="4e559-157">Чтобы просмотреть список текущих политик барьера информации, используйте командлет **Get – информатионбарриерполици** .</span><span class="sxs-lookup"><span data-stu-id="4e559-157">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="4e559-158">Инструкции`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="4e559-158">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="4e559-159">В списке результатов Определите политику, которую необходимо изменить (или удалить).</span><span class="sxs-lookup"><span data-stu-id="4e559-159">In the list of results, identify the policy that you want to change (or remove).</span></span> <span data-ttu-id="4e559-160">Обратите внимание на GUID и имя политики.</span><span class="sxs-lookup"><span data-stu-id="4e559-160">Note the policy's GUID and name.</span></span>

2. <span data-ttu-id="4e559-161">Чтобы присвоить параметру состояние "неактивно", используйте командлет **Set – информатионбарриерполици** с параметром Identity, а параметр state имеет значение Inactive.</span><span class="sxs-lookup"><span data-stu-id="4e559-161">To set the policy's status to inactive, use the **Set-InformationBarrierPolicy** cmdlet with an Identity parameter and the State parameter set to Inactive.</span></span>

    <span data-ttu-id="4e559-162">Инструкции`Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span><span class="sxs-lookup"><span data-stu-id="4e559-162">Syntax: `Set-InformationBarrierPolicy -Identity GUID -State Inactive`</span></span>

    `Set-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c9377247 -State Inactive`

    <span data-ttu-id="4e559-163">В этом примере мы настроили политику барьера данных с идентификатором GUID *43c37853/EA10/4b90 – a23d – ab8c9377247* на неактивное состояние.</span><span class="sxs-lookup"><span data-stu-id="4e559-163">In this example, we set an information barrier policy that has GUID *43c37853-ea10-4b90-a23d-ab8c9377247* to an inactive status.</span></span>

3. <span data-ttu-id="4e559-164">Чтобы применить изменения, используйте командлет **Start – информатионбарриерполиЦиесаппликатион** .</span><span class="sxs-lookup"><span data-stu-id="4e559-164">To apply your changes, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="4e559-165">Инструкции`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="4e559-165">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="4e559-166">Для организации применяются изменения, пользовательские пользователи.</span><span class="sxs-lookup"><span data-stu-id="4e559-166">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="4e559-167">Если ваша организация имеет большой объем, для завершения этого процесса может потребоваться до 24 часов.</span><span class="sxs-lookup"><span data-stu-id="4e559-167">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span> <span data-ttu-id="4e559-168">(Как правило, для обработки 5 000 учетных записей пользователей требуется около часа.)</span><span class="sxs-lookup"><span data-stu-id="4e559-168">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span>

<span data-ttu-id="4e559-169">На этом шаге для одной или нескольких политик барьера информации задано состояние "неактивно".</span><span class="sxs-lookup"><span data-stu-id="4e559-169">At this point, one or more information barrier policies are set to inactive status.</span></span> <span data-ttu-id="4e559-170">Отсюда можно выполнить одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="4e559-170">From here, you can do any of the following:</span></span>
- <span data-ttu-id="4e559-171">Оставьте это значение (политика, настроенная на неактивное состояние, не оказывает никакого действия для пользователей).</span><span class="sxs-lookup"><span data-stu-id="4e559-171">Keep it as is (a policy set to inactive status has no effect on users)</span></span>
- [<span data-ttu-id="4e559-172">Изменение политики</span><span class="sxs-lookup"><span data-stu-id="4e559-172">Edit a policy</span></span>](#edit-a-policy) 
- [<span data-ttu-id="4e559-173">Удаление политики</span><span class="sxs-lookup"><span data-stu-id="4e559-173">Remove a policy</span></span>](#remove-a-policy)

## <a name="remove-a-policy"></a><span data-ttu-id="4e559-174">Удаление политики</span><span class="sxs-lookup"><span data-stu-id="4e559-174">Remove a policy</span></span>

1. <span data-ttu-id="4e559-175">Чтобы просмотреть список текущих политик барьера информации, используйте командлет **Get – информатионбарриерполици** .</span><span class="sxs-lookup"><span data-stu-id="4e559-175">To view a list of current information barrier policies, use the **Get-InformationBarrierPolicy** cmdlet.</span></span>

    <span data-ttu-id="4e559-176">Инструкции`Get-InformationBarrierPolicy`</span><span class="sxs-lookup"><span data-stu-id="4e559-176">Syntax: `Get-InformationBarrierPolicy`</span></span>

    <span data-ttu-id="4e559-177">В списке результатов Определите политику, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="4e559-177">In the list of results, identify the policy that you want to remove.</span></span> <span data-ttu-id="4e559-178">Обратите внимание на GUID и имя политики.</span><span class="sxs-lookup"><span data-stu-id="4e559-178">Note the policy's GUID and name.</span></span> <span data-ttu-id="4e559-179">Убедитесь, что для политики задано состояние неактивно.</span><span class="sxs-lookup"><span data-stu-id="4e559-179">Make sure the policy is set to inactive status.</span></span>

2. <span data-ttu-id="4e559-180">Используйте командлет **Remove – информатионбарриерполици** с параметром Identity.</span><span class="sxs-lookup"><span data-stu-id="4e559-180">Use the **Remove-InformationBarrierPolicy** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="4e559-181">Инструкции`Remove-InformationBarrierPolicy -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="4e559-181">Syntax: `Remove-InformationBarrierPolicy -Identity GUID`</span></span>

    <span data-ttu-id="4e559-182">Пример: Предположим, мы хотим удалить политику с идентификатором GUID *43c37853-EA10-4b90-a23d-ab8c93772471*.</span><span class="sxs-lookup"><span data-stu-id="4e559-182">Example: Suppose we want to remove a policy that has GUID *43c37853-ea10-4b90-a23d-ab8c93772471*.</span></span> <span data-ttu-id="4e559-183">Для этого необходимо использовать следующий командлет:</span><span class="sxs-lookup"><span data-stu-id="4e559-183">To do this, we use this cmdlet:</span></span>
    
    `Remove-InformationBarrierPolicy -Identity 43c37853-ea10-4b90-a23d-ab8c93772471`

    <span data-ttu-id="4e559-184">При появлении соответствующего запроса подтвердите изменение.</span><span class="sxs-lookup"><span data-stu-id="4e559-184">When prompted, confirm the change.</span></span>

3. <span data-ttu-id="4e559-185">Повторите шаги 1-2 для каждой политики, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="4e559-185">Repeat steps 1-2 for each policy you want to remove.</span></span>

4. <span data-ttu-id="4e559-186">После завершения удаления политик примените изменения.</span><span class="sxs-lookup"><span data-stu-id="4e559-186">When you are finished removing policies, apply your changes.</span></span> <span data-ttu-id="4e559-187">Для этого используйте командлет **Start – информатионбарриерполиЦиесаппликатион** .</span><span class="sxs-lookup"><span data-stu-id="4e559-187">To do this, use the **Start-InformationBarrierPoliciesApplication** cmdlet.</span></span>

    <span data-ttu-id="4e559-188">Инструкции`Start-InformationBarrierPoliciesApplication`</span><span class="sxs-lookup"><span data-stu-id="4e559-188">Syntax: `Start-InformationBarrierPoliciesApplication`</span></span>

    <span data-ttu-id="4e559-189">Для организации применяются изменения, пользовательские пользователи.</span><span class="sxs-lookup"><span data-stu-id="4e559-189">Changes are applied, user by user, for your organization.</span></span> <span data-ttu-id="4e559-190">Если ваша организация имеет большой объем, для завершения этого процесса может потребоваться до 24 часов.</span><span class="sxs-lookup"><span data-stu-id="4e559-190">If your organization is large, it can take 24 hours (or more) for this process to complete.</span></span>

## <a name="stop-a-policy-application"></a><span data-ttu-id="4e559-191">Остановка применения политики</span><span class="sxs-lookup"><span data-stu-id="4e559-191">Stop a policy application</span></span>

<span data-ttu-id="4e559-192">Если после начала применения политик барьера информации вы хотите запретить применение этих политик, выполните следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="4e559-192">If, after you have started applying information barrier policies, you want to stop those policies from being applied, use the following procedure.</span></span> <span data-ttu-id="4e559-193">Помните, что для начала процесса потребуется около 30-35 минут.</span><span class="sxs-lookup"><span data-stu-id="4e559-193">Keep in mind that it will take approximately 30-35 minutes for the process to begin.</span></span>

1. <span data-ttu-id="4e559-194">Чтобы просмотреть состояние самого последнего приложения политики барьера данных, используйте командлет **Get – информатионбарриерполиЦиесаппликатионстатус** .</span><span class="sxs-lookup"><span data-stu-id="4e559-194">To view the status of the most recent information barrier policy application, use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet.</span></span>

    <span data-ttu-id="4e559-195">Инструкции`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="4e559-195">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="4e559-196">Обратите внимание на GUID приложения.</span><span class="sxs-lookup"><span data-stu-id="4e559-196">Note the application's GUID.</span></span>

2. <span data-ttu-id="4e559-197">Используйте командлет **Stop – информатионбарриерполиЦиесаппликатион** с параметром Identity.</span><span class="sxs-lookup"><span data-stu-id="4e559-197">Use the **Stop-InformationBarrierPoliciesApplication** cmdlet with an Identity parameter.</span></span>

    <span data-ttu-id="4e559-198">Инструкции`Stop-InformationBarrierPoliciesApplication -Identity GUID`</span><span class="sxs-lookup"><span data-stu-id="4e559-198">Syntax:  `Stop-InformationBarrierPoliciesApplication -Identity GUID`</span></span>

    <span data-ttu-id="4e559-199">Пример: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span><span class="sxs-lookup"><span data-stu-id="4e559-199">Example: `Stop-InformationBarrierPoliciesApplication -Identity 46237888-12ca-42e3-a541-3fcb7b5231d1`</span></span>

    <span data-ttu-id="4e559-200">В этом примере выполняется остановка применения политик барьера информации.</span><span class="sxs-lookup"><span data-stu-id="4e559-200">In this example, we are stopping information barrier policies from being applied.</span></span>

## <a name="related-articles"></a><span data-ttu-id="4e559-201">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4e559-201">Related articles</span></span>

[<span data-ttu-id="4e559-202">Обзор информационных препятствий</span><span class="sxs-lookup"><span data-stu-id="4e559-202">Get an overview of information barriers</span></span>](information-barriers.md)

[<span data-ttu-id="4e559-203">Определение политик для барьеров информации (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="4e559-203">Define policies for information barriers (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="4e559-204">Дополнительные сведения об барьерах информации в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4e559-204">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)

[<span data-ttu-id="4e559-205">Атрибуты политик барьера информации (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="4e559-205">Attributes for information barrier policies (Preview)</span></span>](information-barriers-attributes.md)

[<span data-ttu-id="4e559-206">Препятствия информации об устранении неполадок (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="4e559-206">Troubleshooting information barriers (Preview)</span></span>](information-barriers-troubleshooting.md)
