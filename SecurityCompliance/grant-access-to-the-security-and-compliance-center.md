---
title: Предоставление пользователям доступа к Office 365 безопасность &amp; центре соответствия требованиям
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/18/2017
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.PermissionsHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 2cfce2c8-20c5-47f9-afc4-24b059c1bd76
description: Пользователи должны быть назначены разрешения безопасности Office 365 &amp; центре соответствия требованиям, прежде чем они могут управлять его функции безопасности и соответствия требованиям.
ms.openlocfilehash: 5055c64d914e15a6570c339ade48bb8f7e802ea7
ms.sourcegitcommit: a56fa2e184a2662fd8a7881ccea0891e9a26d497
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2018
ms.locfileid: "27221070"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="53feb-103">Предоставление пользователям доступа к Office 365 безопасность &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="53feb-103">Give users access to the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="53feb-p101">Пользователи должны быть назначены разрешения безопасности Office 365 &amp; центре соответствия требованиям, прежде чем они могут управлять его функции безопасности и соответствия требованиям. Как глобальный администратор Office 365 или участника группы ролей OrganizationManagement безопасности &amp; центре соответствия требованиям, можно предоставить эти разрешения пользователей. Пользователи только смогут управлять возможностями безопасности и соответствия требованиям, предоставьте им доступ к.</span><span class="sxs-lookup"><span data-stu-id="53feb-p101">Users need to be assigned permissions in the Office 365 Security &amp; Compliance Center before they can manage any of its security or compliance features. As an Office 365 global admin or member of the OrganizationManagement role group in the Security &amp; Compliance Center, you can give these permissions to users. Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="53feb-107">Дополнительные сведения о различных разрешения могут предоставить пользователям в разделе Безопасность &amp; центре соответствия требованиям, извлечение [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="53feb-107">For more information about the different permissions you can give to users in the Security &amp; Compliance Center, check out [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="53feb-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="53feb-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="53feb-109">Необходимо быть глобальный администратор Office 365 или участником группы ролей OrganizationManagement безопасности &amp; центре соответствия требованиям, чтобы выполнить действия, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="53feb-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security &amp; Compliance Center, to complete the steps in this article.</span></span>
    
- <span data-ttu-id="53feb-110">Группы ролей для системы безопасности &amp; центре соответствия требованиям может иметь аналогичные имена для группы ролей в Exchange Online, но они не то же самое.</span><span class="sxs-lookup"><span data-stu-id="53feb-110">Role groups for the Security &amp; Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span> 
    
- <span data-ttu-id="53feb-111">Роль в группах не совместно Exchange Online и безопасность &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="53feb-111">Role group memberships aren't shared between Exchange Online and the Security &amp; Compliance Center.</span></span>
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="53feb-112">Использование центра администрирования Office 365 для предоставить другому пользователю доступ к безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="53feb-112">Use the Office 365 admin center to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="53feb-113">[Входа в Office 365 и перейдите в центр администрирования](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span><span class="sxs-lookup"><span data-stu-id="53feb-113">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>
    
2. <span data-ttu-id="53feb-114">В центре администрирования Office 365 откройте **центры администрирования** и нажмите кнопку **безопасности &amp; соответствия**.</span><span class="sxs-lookup"><span data-stu-id="53feb-114">In the Office 365 admin center, open **Admin centers** and then click **Security &amp; Compliance**.</span></span> 
    
3. <span data-ttu-id="53feb-115">В разделе Безопасность &amp; центре соответствия требованиям, чтобы перейти на **разрешения**.</span><span class="sxs-lookup"><span data-stu-id="53feb-115">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
4. <span data-ttu-id="53feb-116">В списке выберите группу ролей, которую требуется добавить пользователя и нажмите кнопку **Изменить** ![значок Правка](media/O365_MDM_CreatePolicy_EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="53feb-116">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
5. <span data-ttu-id="53feb-117">На странице свойств группы ролей в разделе **членов**, нажмите кнопку **Добавить**![добавить значок](media/ITPro-EAC-AddIcon.gif) и выберите имя пользователя (или пользователей) необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="53feb-117">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span> 
    
6. <span data-ttu-id="53feb-118">После выбора всех пользователей, необходимо добавить в группу ролей, нажмите кнопку \*\*Добавьте-\> \*\* и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="53feb-118">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>
    
7. <span data-ttu-id="53feb-119">Нажмите кнопку **Сохранить**, чтобы сохранить изменения в группе ролей.</span><span class="sxs-lookup"><span data-stu-id="53feb-119">Click **Save** to save the changes to the role group.</span></span> 
    
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="53feb-120">Как убедиться, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="53feb-120">How do you know this worked?</span></span>

1. <span data-ttu-id="53feb-121">В разделе Безопасность &amp; центре соответствия требованиям, чтобы перейти на **разрешения**.</span><span class="sxs-lookup"><span data-stu-id="53feb-121">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
2. <span data-ttu-id="53feb-122">В списке выберите группу ролей для просмотра элементов.</span><span class="sxs-lookup"><span data-stu-id="53feb-122">From the list, select the role group to view the members.</span></span>
    
3. <span data-ttu-id="53feb-123">В правой части окна в сведения о группе ролей, можно просмотреть членов группы ролей.</span><span class="sxs-lookup"><span data-stu-id="53feb-123">On the right, in the role group details, you can view the members of the role group.</span></span>
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="53feb-124">С помощью PowerShell можно предоставить другому пользователю доступ к безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="53feb-124">Use PowerShell to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="53feb-125">[Подключение к Office 365 безопасности & PowerShell центре соответствия требованиям](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="53feb-125">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="53feb-126">Воспользуйтесь командой **Add-RoleGroupMember**, чтобы добавить пользователя в группу ролей Organization Management (Управление организацией), как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="53feb-126">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span> 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 <span data-ttu-id="53feb-127">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="53feb-127">**Parameters**</span></span>
  
- <span data-ttu-id="53feb-128">_-Identity_ — группа ролей, в которую необходимо добавить участника.</span><span class="sxs-lookup"><span data-stu-id="53feb-128">_-Identity_ is the role group to add a member to.</span></span> 
    
- <span data-ttu-id="53feb-p102">_Член_ является почтового ящика, универсальной группе безопасности (USG) или компьютер для добавления в группу ролей. Одновременно можно указать только один элемент.</span><span class="sxs-lookup"><span data-stu-id="53feb-p102">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group. You can specify only one member at a time.</span></span> 
    
<span data-ttu-id="53feb-131">Подробные сведения о синтаксисе и параметрах видеть [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span><span class="sxs-lookup"><span data-stu-id="53feb-131">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="53feb-132">Как убедиться, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="53feb-132">How do you know this worked?</span></span>

<span data-ttu-id="53feb-133">Чтобы убедиться, что пользователи получает доступ к безопасности &amp; центре соответствия требованиям, командлет **Get-RoleGroupMember** для просмотра членов в группы ролей управления организацией, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="53feb-133">To verify that you've given users access to the Security &amp; Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span> 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

<span data-ttu-id="53feb-134">[Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860)подробные сведения о синтаксисе и параметрах см.</span><span class="sxs-lookup"><span data-stu-id="53feb-134">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
  

