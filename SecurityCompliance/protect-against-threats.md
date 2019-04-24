---
title: Защита от угроз в Office 365
ms.author: tracyp
author: msfttracyp
manager: laurawi
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: b10023f6-f30f-45d3-b3ad-b71aa4aa0d58
ms.collection:
- M365-security-compliance
description: Используйте эту статью в качестве руководства по настройке функций защиты от угроз.
ms.openlocfilehash: 065071999130f209d63bcafc09ad72daceceac04
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261637"
---
# <a name="protect-against-threats-in-office-365"></a><span data-ttu-id="76b43-103">Защита от угроз в Office 365</span><span class="sxs-lookup"><span data-stu-id="76b43-103">Protect against threats in Office 365</span></span>

<span data-ttu-id="76b43-104">Office 365 включает различные функции защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="76b43-104">Office 365 includes a variety of threat protection features.</span></span> <span data-ttu-id="76b43-105">Вот краткое руководство, которое можно использовать в качестве контрольного списка, чтобы убедиться в том, что функции защиты от угроз настроены для Организации.</span><span class="sxs-lookup"><span data-stu-id="76b43-105">Here's a quick-start guide you can use as a checklist to make sure your threat protection features are set up for your organization.</span></span> <span data-ttu-id="76b43-106">Если вы не знакомы с функциями защиты от угроз в Office 365, или вы только не знаете, с чего начать, используйте следующие рекомендации в качестве отправной точки.</span><span class="sxs-lookup"><span data-stu-id="76b43-106">If you're new to threat protection features in Office 365, or you're just not sure where to begin, use the following guidance as a starting point.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="76b43-107">**Начальные Рекомендуемые параметры включены для каждого типа политики, но многие варианты доступны, и вы можете настроить параметры в соответствии с потребностями конкретной организации**.</span><span class="sxs-lookup"><span data-stu-id="76b43-107">**Initial recommended settings are included for each kind of policy; however, many options are available, and you can adjust your settings to meet your specific organization's needs**.</span></span> <span data-ttu-id="76b43-108">РазРешите около 30 минут, чтобы политики или изменения работали с центром обработки данных.</span><span class="sxs-lookup"><span data-stu-id="76b43-108">Allow approximately 30 minutes for your policies or changes to work their way through your datacenter.</span></span>

## <a name="requirements"></a><span data-ttu-id="76b43-109">Требования</span><span class="sxs-lookup"><span data-stu-id="76b43-109">Requirements</span></span>

### <a name="licenses"></a><span data-ttu-id="76b43-110">Лицензии</span><span class="sxs-lookup"><span data-stu-id="76b43-110">Licenses</span></span>

<span data-ttu-id="76b43-111">Функции защиты от угроз включены во все подписки на Office 365; Однако некоторые подписки включают более сложные функции, например, в Office 365 Advanced Threat protection.</span><span class="sxs-lookup"><span data-stu-id="76b43-111">Threat protection features are included in all Office 365 subscriptions; however, some subscriptions include more advanced features, such as those in Office 365 Advanced Threat Protection.</span></span> <span data-ttu-id="76b43-112">В этой статье мы включаем требования к подписке для каждой области защиты.</span><span class="sxs-lookup"><span data-stu-id="76b43-112">In this article we include subscription requirements for each protection area.</span></span>

<span data-ttu-id="76b43-113">Дополнительные сведения о функциях защиты от угроз и субсриптионс содержатся в следующих ресурсах:</span><span class="sxs-lookup"><span data-stu-id="76b43-113">To learn more about threat protection features and subsriptions, see the following resources:</span></span>
- [<span data-ttu-id="76b43-114">Описание службы Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="76b43-114">Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)
- [<span data-ttu-id="76b43-115">Описание службы Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="76b43-115">Exchange Online Protection Service Description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/exchange-online-protection-service-description/exchange-online-protection-service-description)
- [<span data-ttu-id="76b43-116">Центр безопасности и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="76b43-116">Office 365 Security & Compliance Center</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)

### <a name="roles-and-permissions"></a><span data-ttu-id="76b43-117">Роли и разрешения</span><span class="sxs-lookup"><span data-stu-id="76b43-117">Roles and permissions</span></span>

<span data-ttu-id="76b43-118">Для настройки политик в [центре безопасности _Амп_ соответствия требованиям](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center)необходимо назначить соответствующую роль.</span><span class="sxs-lookup"><span data-stu-id="76b43-118">You must be assigned an appropriate role to configure policies in the [Security & Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center).</span></span> <span data-ttu-id="76b43-119">В следующей таблице приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="76b43-119">The following table includes some examples:</span></span> 

|<span data-ttu-id="76b43-120">Роль или группа ролей</span><span class="sxs-lookup"><span data-stu-id="76b43-120">Role or role group</span></span>  |<span data-ttu-id="76b43-121">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="76b43-121">Where to learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="76b43-122">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="76b43-122">Office 365 Global Administrator</span></span> |[<span data-ttu-id="76b43-123">Роли администраторов в Office 365</span><span class="sxs-lookup"><span data-stu-id="76b43-123">About Office 365 admin roles</span></span>](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|<span data-ttu-id="76b43-124">администратор безопасности (Security Administrator).</span><span class="sxs-lookup"><span data-stu-id="76b43-124">Security Administrator</span></span> |[<span data-ttu-id="76b43-125">Разрешения роли администратора в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="76b43-125">Administrator role permissions in Azure Active Directory</span></span>](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|<span data-ttu-id="76b43-126">Управление организацией Exchange Online</span><span class="sxs-lookup"><span data-stu-id="76b43-126">Exchange Online Organization Management</span></span> |[<span data-ttu-id="76b43-127">Разрешения в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="76b43-127">Permissions in Exchange Online</span></span>](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br><span data-ttu-id="76b43-128">и</span><span class="sxs-lookup"><span data-stu-id="76b43-128">and</span></span><br> [<span data-ttu-id="76b43-129">Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="76b43-129">Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

<span data-ttu-id="76b43-130">Чтобы узнать больше, ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="76b43-130">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="part-1---anti-malware"></a><span data-ttu-id="76b43-131">Часть 1 — Защита от вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="76b43-131">Part 1 - Anti-malware</span></span>

<span data-ttu-id="76b43-132">[Защита от вредоносных программ](anti-malware-protection.md) доступна в подписках, включающих [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span><span class="sxs-lookup"><span data-stu-id="76b43-132">[Anti-malware protection](anti-malware-protection.md) is available in subscriptions that include [Exchange Online Protection](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description) (EOP).</span></span> 

1. <span data-ttu-id="76b43-133">В [центре безопасности _амп_ соответствие требованиям](https://protection.office.com)выберите**Политика** >  **управления** > угрозами для**защиты от вредоносных программ**.</span><span class="sxs-lookup"><span data-stu-id="76b43-133">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-malware**.</span></span>

2. <span data-ttu-id="76b43-134">Дважды щелкните политику **по умолчанию** , а затем выберите **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="76b43-134">Double-click the **Default** policy, and then choose **settings**.</span></span>

3. <span data-ttu-id="76b43-135">Укажите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="76b43-135">Specify the following settings:</span></span>
    
    - <span data-ttu-id="76b43-136">В разделе **ответ на обнаружение вредоносНых программ** оставьте значение по умолчанию ( **нет**).</span><span class="sxs-lookup"><span data-stu-id="76b43-136">In the **Malware Detection Response** section, keep the default setting of **No**.</span></span>
   
    - <span data-ttu-id="76b43-137">В разделе **фильтр типов вложений** выберите **включено**.</span><span class="sxs-lookup"><span data-stu-id="76b43-137">In the **Common Attachment Types Filter** section, choose **On**.</span></span>

4. <span data-ttu-id="76b43-138">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="76b43-138">Click **Save**.</span></span>

<span data-ttu-id="76b43-139">Дополнительные сведения о параметрах политики защиты от вредоносных программ приведены в разделе [Настройка политик защиты](configure-anti-malware-policies.md)от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="76b43-139">To learn more about anti-malware policy options, see [Configure anti-malware policies](configure-anti-malware-policies.md).</span></span>

## <a name="part-2---zero-day-protection"></a><span data-ttu-id="76b43-140">Часть 2 — Защита от нулевого дня</span><span class="sxs-lookup"><span data-stu-id="76b43-140">Part 2 - Zero-day protection</span></span>

<span data-ttu-id="76b43-141">Защита от нулевого дня доступна в подписках, включающих в себя [Office 365 Advanced Threat protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), и настраивается с помощью политик безопасных [вложений](atp-safe-attachments.md) ATP и безопасных [ссылок ATP](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="76b43-141">Zero-day protection is available in subscriptions that include [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description) (ATP), and is set up through [ATP Safe Attachments](atp-safe-attachments.md) and [ATP Safe Links](atp-safe-links.md) policies.</span></span>

### <a name="atp-safe-attachments-policies"></a><span data-ttu-id="76b43-142">Политики безОпасных вложений ATP</span><span class="sxs-lookup"><span data-stu-id="76b43-142">ATP Safe Attachments policies</span></span>

<span data-ttu-id="76b43-143">Для настройки [безопасных вложенИй ATP](atp-safe-attachments.md)необходимо определить по крайней мере одну политику безопасных вложений ATP.</span><span class="sxs-lookup"><span data-stu-id="76b43-143">To set up [ATP Safe Attachments](atp-safe-attachments.md), you must define at least one ATP Safe Attachments policy.</span></span> 

1. <span data-ttu-id="76b43-144">В [центре безопасности _амп_ соответствие требованиям](https://protection.office.com)выберите**Политика** >  **управления** > угрозами**безопасные вложения ATP**.</span><span class="sxs-lookup"><span data-stu-id="76b43-144">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP safe attachments**.</span></span>

2. <span data-ttu-id="76b43-145">Выберите параметр **включить ATP для SharePoint, OneDrive и Microsoft Teams**.</span><span class="sxs-lookup"><span data-stu-id="76b43-145">Select the option **Turn on ATP for SharePoint, OneDrive, and Microsoft Teams**.</span></span>

3. <span data-ttu-id="76b43-146">В разделе **защита вложений электронной почты** щелкните знак "плюс"**+**().</span><span class="sxs-lookup"><span data-stu-id="76b43-146">In the **Protect email attachments** section, click the plus sign (**+**).</span></span>

4. <span data-ttu-id="76b43-147">Укажите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="76b43-147">Specify the following settings:</span></span>

    - <span data-ttu-id="76b43-148">В поле **имя** введите `Block malware`.</span><span class="sxs-lookup"><span data-stu-id="76b43-148">In the **Name** box, type `Block malware`.</span></span>

    - <span data-ttu-id="76b43-149">В разделе ответ выберите пункт **блокировать**.</span><span class="sxs-lookup"><span data-stu-id="76b43-149">In the response section, choose **Block**.</span></span>

    - <span data-ttu-id="76b43-150">В разделе **Перенаправление вложения** выберите параметр **включить перенаправление**, а затем укажите адрес электронной почты администратора безопасности Организации или оператора, который будет просматривать обнаруженные файлы.</span><span class="sxs-lookup"><span data-stu-id="76b43-150">In the **Redirect attachment** section, select the option **Enable redirect**, and then specify the email address for your organization's security administrator or operator who will review detected files.</span></span>

    - <span data-ttu-id="76b43-151">В разделе **применено** выберите **домен получателя**.</span><span class="sxs-lookup"><span data-stu-id="76b43-151">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="76b43-152">Затем выберите свой домен, нажмите кнопку **Добавить**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="76b43-152">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

5. <span data-ttu-id="76b43-153">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="76b43-153">Click **Save**.</span></span>

6. <span data-ttu-id="76b43-154">(**Рекомендуемое дополнительное действие**) Как глобальный администратор или администратор SharePoint Online выполните командлет **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** с параметром **дисалловинфектедфиледовнлоад** , для которого установлено значение *true* , для среды Office 365.</span><span class="sxs-lookup"><span data-stu-id="76b43-154">(**Recommended additional step**) As a global administrator or a SharePoint Online administrator run the **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** cmdlet with the **DisallowInfectedFileDownload** parameter set to  *true* for your Office 365 environment.</span></span> <span data-ttu-id="76b43-155">(Это предотвращает открытие, перемещение, копирование или совместное использование файлов, обнаруженных как вредоносные.)</span><span class="sxs-lookup"><span data-stu-id="76b43-155">(This prevents people from opening, moving, copying, or sharing files that are detected as malicious.)</span></span>  

<span data-ttu-id="76b43-156">Дополнительные сведения см. в статьях</span><span class="sxs-lookup"><span data-stu-id="76b43-156">To learn more, see:</span></span> 
- [<span data-ttu-id="76b43-157">Настройка политик безОпасных вложений Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="76b43-157">Set up Office 365 ATP Safe Attachments policies</span></span>](set-up-atp-safe-attachments-policies.md)
- [<span data-ttu-id="76b43-158">Включение Office 365 ATP для SharePoint, OneDrive и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="76b43-158">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)

### <a name="atp-safe-links-policies"></a><span data-ttu-id="76b43-159">Политики безОпасных ссылок ATP</span><span class="sxs-lookup"><span data-stu-id="76b43-159">ATP Safe Links policies</span></span>

<span data-ttu-id="76b43-160">Чтобы настроить [безопасные ссылки ATP](atp-safe-links.md), просмотрите и измените политику по умолчанию и добавьте политику для определенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="76b43-160">To set up [ATP Safe Links](atp-safe-links.md), review and edit your default policy, and add a policy for specific users.</span></span>

1. <span data-ttu-id="76b43-161">В [центре безопасности _амп_ соответствие требованиям](https://protection.office.com)выберите**Политика** >  **управления** > угрозой**безопасные ссылки ATP**.</span><span class="sxs-lookup"><span data-stu-id="76b43-161">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP Safe Links**.</span></span>

2. <span data-ttu-id="76b43-162">Дважды щелкните политику **по умолчанию** .</span><span class="sxs-lookup"><span data-stu-id="76b43-162">Double-click the **Default** policy.</span></span>

3. <span data-ttu-id="76b43-163">В разделе **использовать безопасные ссылки в** выберите вариант **Office 365 профессиональный плюс, Office для iOS и Android**, а затем нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="76b43-163">In the **Use safe links in** section, select the option **Office 365 ProPlus, Office for iOS and Android**, and then click **Save**.</span></span>

4. <span data-ttu-id="76b43-164">В разделе **политики, которые применяются к определенным получателям** щелкните знак "плюс"**+**().</span><span class="sxs-lookup"><span data-stu-id="76b43-164">In the **Policies that apply to specific recipients** section, click the plus sign (**+**).</span></span>

5. <span data-ttu-id="76b43-165">Укажите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="76b43-165">Specify the following settings:</span></span>

    - <span data-ttu-id="76b43-166">В поле **имя** введите имя, например `Safe Links`.</span><span class="sxs-lookup"><span data-stu-id="76b43-166">In the **Name** box, type a name, such as `Safe Links`.</span></span>

    - <span data-ttu-id="76b43-167">В разделе **Выбор действия** выберите **включить**.</span><span class="sxs-lookup"><span data-stu-id="76b43-167">In the **Select the action** section, choose **On**.</span></span>

    - <span data-ttu-id="76b43-168">Выберите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="76b43-168">Select these options:</span></span>

        - <span data-ttu-id="76b43-169">**Использование безопасных вложений для сканирования загружаемого контента**</span><span class="sxs-lookup"><span data-stu-id="76b43-169">**Use safe attachments to scan downloadable content**</span></span> 

        - <span data-ttu-id="76b43-170">**Применение безопасных ссылок к сообщениям электронной почты, отправленным в Организации**</span><span class="sxs-lookup"><span data-stu-id="76b43-170">**Apply safe links to email messages sent within the organization**</span></span>

        - <span data-ttu-id="76b43-171">**Не разрешать пользователям щелкать ссылки с исходным URL-АДРЕСом.**</span><span class="sxs-lookup"><span data-stu-id="76b43-171">**Do not let users click through safe links to original URL**</span></span>

    - <span data-ttu-id="76b43-172">В разделе **применено** выберите **домен получателя**.</span><span class="sxs-lookup"><span data-stu-id="76b43-172">In the **Applied to** section, choose **The recipient domain is**.</span></span> <span data-ttu-id="76b43-173">Затем выберите свой домен, нажмите кнопку **Добавить**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="76b43-173">Then, select your domain, choose **Add**, and then click **OK**.</span></span>

6. <span data-ttu-id="76b43-174">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="76b43-174">Click **Save**.</span></span>

<span data-ttu-id="76b43-175">Чтобы узнать больше, ознакомьтесь со статьей [Настройка политик безопасных ссылок на Office 365 ATP](set-up-atp-safe-links-policies.md).</span><span class="sxs-lookup"><span data-stu-id="76b43-175">To learn more, see [Set up Office 365 ATP Safe Links policies](set-up-atp-safe-links-policies.md).</span></span> 

## <a name="part-3---anti-phishing"></a><span data-ttu-id="76b43-176">Часть 3 — Защита от фишинга</span><span class="sxs-lookup"><span data-stu-id="76b43-176">Part 3 - Anti-phishing</span></span> 

<span data-ttu-id="76b43-177">[Защита от фишинга](anti-phishing-protection.md) доступна в подписках, включающих [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="76b43-177">[Anti-phishing protection](anti-phishing-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="76b43-178">Расширенная защита от фишинга доступна в [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="76b43-178">Advanced anti-phishing protection is available in [ATP](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span> <span data-ttu-id="76b43-179">В следующей процедуре описывается настройка антифишинговой политики ATP.</span><span class="sxs-lookup"><span data-stu-id="76b43-179">The following procedure describes how to configure an ATP anti-phishing policy.</span></span> <span data-ttu-id="76b43-180">Эти действия похожи на настройку антифишинговой политики (без ATP).</span><span class="sxs-lookup"><span data-stu-id="76b43-180">The steps are similar for configuring an anti-phishing policy (without ATP).</span></span>

1. <span data-ttu-id="76b43-181">В [центре безопасности _амп_ соответствие требованиям](https://protection.office.com)выберите**Политика** >  **управления** > угрозами для**защиты от фишинга ATP**.</span><span class="sxs-lookup"><span data-stu-id="76b43-181">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **ATP anti-phishing**.</span></span>

2. <span data-ttu-id="76b43-182">Щелкните **Политика по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="76b43-182">Click **Default policy**.</span></span>

3. <span data-ttu-id="76b43-183">В разделе **олицетворение** нажмите кнопку **изменить**, а затем укажите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="76b43-183">In the **Impersonation** section, click **Edit**, and then specify the following settings:</span></span>

    -  <span data-ttu-id="76b43-184">На вкладке **Добавление пользователей для защиты** включите защиту.</span><span class="sxs-lookup"><span data-stu-id="76b43-184">On the **Add users to protect** tab, turn protection on.</span></span> <span data-ttu-id="76b43-185">Затем добавьте пользователей, например, участников вашей организации, ГЕНЕРАЛЬНого директора, финансового директора и других старших руководителей.</span><span class="sxs-lookup"><span data-stu-id="76b43-185">Then add users, such as your organization's board members, your CEO, CFO, and other senior leaders.</span></span> <span data-ttu-id="76b43-186">(Вы можете ввести отдельный адрес электронной почты или щелкнуть для отображения списка.)</span><span class="sxs-lookup"><span data-stu-id="76b43-186">(You can type an individual email address, or click to display a list.)</span></span>

    - <span data-ttu-id="76b43-187">На вкладке **Добавление доменов для защиты** включите **Автоматическое включение доменов, которыми я владеют**.</span><span class="sxs-lookup"><span data-stu-id="76b43-187">On the **Add domains to protect** tab, turn on **Automatically include the domains I own**.</span></span> <span data-ttu-id="76b43-188">Если у вас есть пользовательские домены, добавьте их также.</span><span class="sxs-lookup"><span data-stu-id="76b43-188">If you have custom domains, add those as well.</span></span>

    - <span data-ttu-id="76b43-189">На вкладке **действия** выберите **переместить сообщение в папку нежелательной почты получателей** для олицетворенного пользователя и олицетворенного домена и включите советы по безопасности.</span><span class="sxs-lookup"><span data-stu-id="76b43-189">On the **Actions** tab, select **Move message to the recipients' Junk Email folders** for both impersonated user and impersonated domain, and turn on safety tips.</span></span>

    - <span data-ttu-id="76b43-190">На вкладке **аналитика** поЧтовых ящиков убедитесь, что включена функция интеллектуального анализа почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="76b43-190">On the **Mailbox intelligence** tab, make sure mailbox intelligence is turned on.</span></span>

    - <span data-ttu-id="76b43-191">На вкладке **Проверка параметров** после просмотра параметров нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="76b43-191">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span>

4. <span data-ttu-id="76b43-192">В разделе **подделка** нажмите кнопку **изменить**, а затем укажите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="76b43-192">In the **Spoof** section, click **Edit**, and then specify the following settings:</span></span>

    - <span data-ttu-id="76b43-193">На вкладке **Параметры фильтра подделки** убедитесь, что включена защита от спуфинга.</span><span class="sxs-lookup"><span data-stu-id="76b43-193">On the **Spoofing filter settings** tab, make sure anti-spoofing protection is turned on.</span></span>

    - <span data-ttu-id="76b43-194">На вкладке **действия** выберите Переместить сообщение в папку нежелательной почты получателей.</span><span class="sxs-lookup"><span data-stu-id="76b43-194">On the **Actions** tab, choose Move message to the recipients' Junk Email folders.</span></span>

    - <span data-ttu-id="76b43-195">На вкладке **Проверка параметров** после просмотра параметров нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="76b43-195">On the **Review your settings** tab, after you have reviewed your settings, click **Save**.</span></span> <span data-ttu-id="76b43-196">(Если изменения не были внесены, нажмите кнопку **Отмена**.)</span><span class="sxs-lookup"><span data-stu-id="76b43-196">(If you didn't make any changes, click **Cancel**.)</span></span>

5. <span data-ttu-id="76b43-197">Закройте страницу параметров политики по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76b43-197">Close the default policy settings page.</span></span>

<span data-ttu-id="76b43-198">Чтобы узнать больше о параметрах политики защиты от фишинга, ознакомьтесь со статьей [Настройка политик защиты от фишинга](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="76b43-198">To learn more about your anti-phishing policy options, see [Set up anti-phishing policies](set-up-anti-phishing-policies.md).</span></span>

## <a name="part-4---anti-spam"></a><span data-ttu-id="76b43-199">Часть 4: защита от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="76b43-199">Part 4 - Anti-spam</span></span>

<span data-ttu-id="76b43-200">[Защита от нежелательной почты](anti-spam-protection.md) доступна в подписках, включающих [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="76b43-200">[Anti-spam protection](anti-spam-protection.md) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span>

1. <span data-ttu-id="76b43-201">В [центре безопасности _амп_ соответствие требованиям](https://protection.office.com)выберите**Политика** >  **управления** > угрозами**Защита от нежелательной почты**.</span><span class="sxs-lookup"><span data-stu-id="76b43-201">In the [Security & Compliance Center](https://protection.office.com), choose **Threat management** > **Policy** > **Anti-spam**.</span></span>

2. <span data-ttu-id="76b43-202">На вкладке **Настройка** включите **пользовательские параметры** .</span><span class="sxs-lookup"><span data-stu-id="76b43-202">On the **Custom** tab, turn **Custom settings** on.</span></span>

3. <span data-ttu-id="76b43-203">Разверните узел **Политика фильтрации нежелательной почты по умолчанию**, щелкните **изменить политику**, а затем укажите следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="76b43-203">Expand **Default spam filter policy**, click **Edit policy**, and then specify the following settings:</span></span>

    - <span data-ttu-id="76b43-204">В разделе **Нежелательная почта и групповые действия** установите для порогового значения 5 или 6.</span><span class="sxs-lookup"><span data-stu-id="76b43-204">In the **Spam and bulk actions** section, set the threshold to a value of 5 or 6.</span></span>

    - <span data-ttu-id="76b43-205">В разделе **разрешить списки** просмотрите (и при необходимости измените) разрешенных отправителей и доменов.</span><span class="sxs-lookup"><span data-stu-id="76b43-205">In the **Allow lists** section, review (and if necessary, edit) your allowed senders and domains.</span></span>

4. <span data-ttu-id="76b43-206">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="76b43-206">Click **Save**.</span></span>

<span data-ttu-id="76b43-207">Чтобы узнать больше о параметрах политики защиты от нежелательной почты, ознакомьтесь со статьей [Настройка политик защиты от нежелательной почты](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="76b43-207">To learn more about your anti-spam policy options, see [Configure the anti-spam policies](configure-the-anti-spam-policies.md).</span></span>

## <a name="part-5---service-wide-settings"></a><span data-ttu-id="76b43-208">Часть 5 — параметры на уровне службы</span><span class="sxs-lookup"><span data-stu-id="76b43-208">Part 5 - Service-wide settings</span></span>

### <a name="zero-hour-auto-purge"></a><span data-ttu-id="76b43-209">Автоматическое удаление нулевых часов</span><span class="sxs-lookup"><span data-stu-id="76b43-209">Zero-hour auto purge</span></span>

<span data-ttu-id="76b43-210">[Автоматическое удаление нулевых часов](zero-hour-auto-purge.md) (ZAP) доступен в подписках, включающих [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="76b43-210">[Zero-hour auto purge](zero-hour-auto-purge.md) (ZAP) is available in subscriptions that include [EOP](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description).</span></span> <span data-ttu-id="76b43-211">Эта защита включается по умолчанию; Однако для вступления в последствия защиты должны выполняться следующие условия:</span><span class="sxs-lookup"><span data-stu-id="76b43-211">This protection is turned on by default; however, the following conditions must be met for protection to be in effect:</span></span>

- <span data-ttu-id="76b43-212">Для действий неЖелательной почты настраивается **Перемещение сообщения в папку нежелательной почты** в [политиках защиты от нежелательной почты](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="76b43-212">Spam actions are set to **Move message to Junk Email folder** in [anti-spam policies](anti-spam-protection.md).</span></span>

- <span data-ttu-id="76b43-213">Пользователи сохраняли свои [Параметры нежелательной почты](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md)по умолчанию и не отключили защиту от нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="76b43-213">Users have kept their default [junk email settings](ensure-that-spam-is-routed-to-each-user-s-junk-email-folder.md), and have not turned off junk email protection.</span></span>

<span data-ttu-id="76b43-214">Для получения дополнительных сведений о [нежелательной почте и вредоносном программном обеспечении автоматическая очистка без защиты](zero-hour-auto-purge.md)от нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="76b43-214">To learn more, see [Zero-hour auto purge - protection against spam and malware](zero-hour-auto-purge.md).</span></span>

### <a name="audit-logging"></a><span data-ttu-id="76b43-215">Ведение журнала аудита</span><span class="sxs-lookup"><span data-stu-id="76b43-215">Audit logging</span></span>

<span data-ttu-id="76b43-216">Ведение журнала аудита доступно в подписках, включающих [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span><span class="sxs-lookup"><span data-stu-id="76b43-216">Audit logging is available in subscriptions that include [Exchange Online](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description).</span></span> <span data-ttu-id="76b43-217">Для просмотра данных в отчетах защиты от угроз, таких как [панель мониторинга безопасности](security-dashboard.md), [отчеты о безопасности электронной почты](view-email-security-reports.md)и [проводник](use-explorer-in-security-and-compliance.md), для Организации необходимо включить ведение журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="76b43-217">In order to view data in threat protection reports, such as the [Security Dashboard](security-dashboard.md), [email security reports](view-email-security-reports.md), and [Explorer](use-explorer-in-security-and-compliance.md), audit logging must be turned on for your organization.</span></span> <span data-ttu-id="76b43-218">Чтобы узнать больше, ознакомьтесь [со статьЕй включение и отключение поиска в журнале аудита Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="76b43-218">To learn more, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="post-setup-tasks"></a><span data-ttu-id="76b43-219">Задачи, выполняемые после установки</span><span class="sxs-lookup"><span data-stu-id="76b43-219">Post-setup tasks</span></span>

### <a name="watch-for-new-features-and-service-updates"></a><span data-ttu-id="76b43-220">Просмотр новых компонентов и обновлений служб</span><span class="sxs-lookup"><span data-stu-id="76b43-220">Watch for new features and service updates</span></span>

- [<span data-ttu-id="76b43-221">Настройка стандартных или целевых вариантов выпуска</span><span class="sxs-lookup"><span data-stu-id="76b43-221">Set up the Standard or Targeted release options</span></span>](https://docs.microsoft.com/office365/admin/manage/release-options-in-office-365?view=o365-worldwide)

- [<span data-ttu-id="76b43-222">Переход в центр сообщений для просмотра объявлений о функциях</span><span class="sxs-lookup"><span data-stu-id="76b43-222">Go to your Message center to view feature announcements</span></span>](https://docs.microsoft.com/office365/admin/manage/message-center?view=o365-worldwide) 

- [<span data-ttu-id="76b43-223">Посетите план Microsoft 365, чтобы просмотреть состояние новых функций</span><span class="sxs-lookup"><span data-stu-id="76b43-223">Visit the Microsoft 365 Roadmap to see status of new features</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection)

- [<span data-ttu-id="76b43-224">Обзор описаний служб Office 365</span><span class="sxs-lookup"><span data-stu-id="76b43-224">Review the Office 365 Service Descriptions</span></span>](https://docs.microsoft.com/office365/servicedescriptions/office-365-service-descriptions-technet-library)

### <a name="see-how-threat-protection-features-are-working-for-your-organization"></a><span data-ttu-id="76b43-225">Узнайте, как работают функции защиты от угроз для вашей организации</span><span class="sxs-lookup"><span data-stu-id="76b43-225">See how threat protection features are working for your organization</span></span>

- [<span data-ttu-id="76b43-226">Посетите панель мониторинга безопасности</span><span class="sxs-lookup"><span data-stu-id="76b43-226">Visit your security dashboard</span></span>](security-dashboard.md)

- <span data-ttu-id="76b43-227">[Просмотр отчетов для Office 365 ATP](view-reports-for-atp.md), включая [Explorer](use-explorer-in-security-and-compliance.md)</span><span class="sxs-lookup"><span data-stu-id="76b43-227">[View the reports for Office 365 ATP](view-reports-for-atp.md), including [Explorer](use-explorer-in-security-and-compliance.md)</span></span>

- [<span data-ttu-id="76b43-228">Просмотр отчетов о безопасности электронной почты</span><span class="sxs-lookup"><span data-stu-id="76b43-228">View your email security reports</span></span>](view-email-security-reports.md)

### <a name="periodically-review-and-revise-your-threat-protection-policies"></a><span data-ttu-id="76b43-229">Периодическая проверка и пересмотр политик защиты от угроз</span><span class="sxs-lookup"><span data-stu-id="76b43-229">Periodically review and revise your threat protection policies</span></span>

- [<span data-ttu-id="76b43-230">Просмотр оценки безопасности</span><span class="sxs-lookup"><span data-stu-id="76b43-230">Review your Secure Score</span></span>](microsoft-secure-score.md)

- [<span data-ttu-id="76b43-231">Использование смарт-отчетов и аналитических данных в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="76b43-231">Use your smart reports and insights in the Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md) 

- [<span data-ttu-id="76b43-232">Обеспечение безопасности пользователей с помощью Office 365 для расследования угроз и функции ответа</span><span class="sxs-lookup"><span data-stu-id="76b43-232">Keep users safe with Office 365 threat investigation and response features</span></span>](keep-users-safe-with-office-365-ti.md) 
 