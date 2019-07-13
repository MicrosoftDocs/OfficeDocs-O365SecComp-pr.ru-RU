---
title: Предоставление пользователям доступа к Центру безопасности и соответствия требованиям Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Пользователям необходимо назначить разрешения в центре безопасности & безопасности Office 365, прежде чем они смогут управлять любыми функциями обеспечения безопасности и соответствия требованиям.
ms.openlocfilehash: 7963a8c3db64e83566960abe9298b9a2d636ae53
ms.sourcegitcommit: 6302a43d947a908dd10a8e40550b806f491692fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2019
ms.locfileid: "35645124"
---
# <a name="give-users-access-to-the-office-365-security--compliance-center"></a><span data-ttu-id="93506-103">Предоставление пользователям доступа к Центру безопасности и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="93506-103">Give users access to the Office 365 Security & Compliance Center</span></span>

<span data-ttu-id="93506-104">Пользователям необходимо назначить разрешения в центре безопасности & безопасности Office 365, прежде чем они смогут управлять любыми функциями обеспечения безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="93506-104">Users need to be assigned permissions in the Office 365 Security & Compliance Center before they can manage any of its security or compliance features.</span></span> <span data-ttu-id="93506-105">В качестве глобального администратора Office 365 или члена группы ролей Организатионманажемент в центре безопасности & соответствия требованиям пользователи могут предоставить эти разрешения пользователям.</span><span class="sxs-lookup"><span data-stu-id="93506-105">As an Office 365 global admin or member of the OrganizationManagement role group in the Security & Compliance Center, you can give these permissions to users.</span></span> <span data-ttu-id="93506-106">Пользователи смогут управлять только теми функциями безопасности и соответствия требованиям, к которым вы предоставите им доступ.</span><span class="sxs-lookup"><span data-stu-id="93506-106">Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="93506-107">Для получения дополнительных сведений о различных разрешениях, которые вы можете предоставить пользователям в центре безопасности & соответствия требованиям, изучите [разрешения в центре обеспечения безопасности & Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="93506-107">For more information about the different permissions you can give to users in the Security & Compliance Center, check out [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="93506-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="93506-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="93506-109">Для выполнения действий, описанных в данной статье, необходимо быть глобальным администратором Office 365 или членом группы ролей Организатионманажемент в центре безопасности & соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="93506-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security & Compliance Center, to complete the steps in this article.</span></span>

- <span data-ttu-id="93506-110">Группы ролей для центра безопасности & соответствия требованиям могут иметь похожие имена для групп ролей в Exchange Online, но они не совпадают.</span><span class="sxs-lookup"><span data-stu-id="93506-110">Role groups for the Security & Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span>

- <span data-ttu-id="93506-111">Сведения о членстве в группах ролей не являются общими для Exchange Online и центра безопасности & соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="93506-111">Role group memberships aren't shared between Exchange Online and the Security & Compliance Center.</span></span>

- <span data-ttu-id="93506-112">Права на делегированный доступ (с правами администратора) с правами администратора от имени (АОБО) не могут получить доступ к центру безопасности & соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="93506-112">Delegated Access Permission (DAP) partners with Administer On Behalf Of (AOBO) permissions can't access the Security & Compliance Center.</span></span>

## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="93506-113">Предоставление другому пользователю доступа к центру безопасности & соответствия требованиям с помощью центра администрирования Office 365</span><span class="sxs-lookup"><span data-stu-id="93506-113">Use the Office 365 admin center to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="93506-114">[Войдите в Office 365 и перейдите в центр администрирования](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span><span class="sxs-lookup"><span data-stu-id="93506-114">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>

2. <span data-ttu-id="93506-115">В центре администрирования Office 365 откройте **центр администрирования** и выберите **Безопасность & соответствия требованиям**.</span><span class="sxs-lookup"><span data-stu-id="93506-115">In the Office 365 admin center, open **Admin centers** and then click **Security & Compliance**.</span></span>

3. <span data-ttu-id="93506-116">В центре безопасности & соответствия требованиям перейдите к разделу **разрешения**.</span><span class="sxs-lookup"><span data-stu-id="93506-116">In the Security & Compliance Center, go to **Permissions**.</span></span>

4. <span data-ttu-id="93506-117">В списке выберите группу ролей, в которую нужно добавить пользователя, и нажмите кнопку **изменить** ![значок](media/O365-MDM-CreatePolicy-EditIcon.gif)редактирования.</span><span class="sxs-lookup"><span data-stu-id="93506-117">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365-MDM-CreatePolicy-EditIcon.gif).</span></span>

5. <span data-ttu-id="93506-118">На странице свойств группы ролей в разделе **Участники**нажмите **Добавить**![значок](media/ITPro-EAC-AddIcon.gif) добавить и выберите имя пользователя (или пользователей), которого вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="93506-118">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span>

6. <span data-ttu-id="93506-119">Выбрав всех пользователей, которых вы хотите добавить в группу ролей, нажмите кнопку **Add (добавить\> )** , а затем кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="93506-119">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>

7. <span data-ttu-id="93506-120">Нажмите кнопку **Сохранить**, чтобы сохранить изменения в группе ролей.</span><span class="sxs-lookup"><span data-stu-id="93506-120">Click **Save** to save the changes to the role group.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="93506-121">Как проверить, что все получилось</span><span class="sxs-lookup"><span data-stu-id="93506-121">How do you know this worked?</span></span>

1. <span data-ttu-id="93506-122">В центре безопасности & соответствия требованиям перейдите к разделу **разрешения**.</span><span class="sxs-lookup"><span data-stu-id="93506-122">In the Security & Compliance Center, go to **Permissions**.</span></span>

2. <span data-ttu-id="93506-123">В списке выберите группу ролей, чтобы просмотреть ее участников.</span><span class="sxs-lookup"><span data-stu-id="93506-123">From the list, select the role group to view the members.</span></span>

3. <span data-ttu-id="93506-124">Справа в разделе сведения о группе ролей можно просмотреть членов группы ролей.</span><span class="sxs-lookup"><span data-stu-id="93506-124">On the right, in the role group details, you can view the members of the role group.</span></span>

## <a name="use-powershell-to-give-another-user-access-to-the-security--compliance-center"></a><span data-ttu-id="93506-125">Предоставление другому пользователю доступа к центру безопасности & соответствия требованиям с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="93506-125">Use PowerShell to give another user access to the Security & Compliance Center</span></span>

1. <span data-ttu-id="93506-126">[Подключение к PowerShell центра безопасности & центра соответствия требованиям Office 365](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="93506-126">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="93506-127">Воспользуйтесь командой **Add-RoleGroupMember**, чтобы добавить пользователя в группу ролей Organization Management (Управление организацией), как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="93506-127">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span>

   ```
   Add-RoleGroupMember -Identity "Organization Management" -Member MatildaS
   ```

   <span data-ttu-id="93506-128">**Параметры**:</span><span class="sxs-lookup"><span data-stu-id="93506-128">**Parameters**:</span></span>
  
   - <span data-ttu-id="93506-129">_Identity_ — группа ролей, в которую добавляется участник.</span><span class="sxs-lookup"><span data-stu-id="93506-129">_Identity_ is the role group to add a member to.</span></span>

   - <span data-ttu-id="93506-130">_Member_ является почтовым ящиком, универсальной группой безопасности (универсальную группу безопасности) или компьютером, который требуется добавить в группу ролей.</span><span class="sxs-lookup"><span data-stu-id="93506-130">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group.</span></span> <span data-ttu-id="93506-131">За один раз можно добавить только одного участника.</span><span class="sxs-lookup"><span data-stu-id="93506-131">You can specify only one member at a time.</span></span>

<span data-ttu-id="93506-132">Подробную информацию о синтаксисе и параметрах можно узнать в статье [Add/RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span><span class="sxs-lookup"><span data-stu-id="93506-132">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="93506-133">Как убедиться, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="93506-133">How do you know this worked?</span></span>

<span data-ttu-id="93506-134">Чтобы убедиться, что у пользователей есть доступ к центру безопасности & соответствия требованиям, используйте командлет **Get – RoleGroupMember** для просмотра членов в группе ролей Управление организацией, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="93506-134">To verify that you've given users access to the Security & Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span>
  
```
Get-RoleGroupMember -Identity "Organization Management"
```

<span data-ttu-id="93506-135">Подробную информацию о синтаксисе и параметрах можно найти в статье [Get – RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span><span class="sxs-lookup"><span data-stu-id="93506-135">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
