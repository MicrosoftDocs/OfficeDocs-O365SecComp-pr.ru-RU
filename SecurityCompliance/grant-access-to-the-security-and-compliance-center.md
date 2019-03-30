---
title: Предоставление пользователям доступа к центру безопасности &amp; и соответствия требованиям Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
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
description: Пользователям необходимо назначить разрешения в центре безопасности &amp; Office 365, чтобы они могли управлять любыми функциями обеспечения безопасности или соответствия требованиям.
ms.openlocfilehash: 08b3781ceb48b9a8d5933a075106d7bd3b9ab17d
ms.sourcegitcommit: 799a958fcac643f62dfac6fa04020f2f4758635c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "30997242"
---
# <a name="give-users-access-to-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="d1034-103">Предоставление пользователям доступа к центру безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="d1034-103">Give users access to the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="d1034-104">Пользователям необходимо назначить разрешения в центре безопасности &amp; Office 365, чтобы они могли управлять любыми функциями обеспечения безопасности или соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d1034-104">Users need to be assigned permissions in the Office 365 Security &amp; Compliance Center before they can manage any of its security or compliance features.</span></span> <span data-ttu-id="d1034-105">В качестве глобального администратора Office 365 или члена группы ролей Организатионманажемент в центре безопасности &amp; и соответствия требованиям пользователи могут предоставить эти разрешения пользователям.</span><span class="sxs-lookup"><span data-stu-id="d1034-105">As an Office 365 global admin or member of the OrganizationManagement role group in the Security &amp; Compliance Center, you can give these permissions to users.</span></span> <span data-ttu-id="d1034-106">Пользователи смогут управлять только теми функциями безопасности и соответствия требованиям, к которым вы предоставите им доступ.</span><span class="sxs-lookup"><span data-stu-id="d1034-106">Users will only be able to manage the security or compliance features that you give them access to.</span></span> 
  
<span data-ttu-id="d1034-107">Для получения дополнительных сведений о различных разрешениях, которые вы можете предоставить пользователям &amp; в центре безопасности, ознакомьтесь с разрешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d1034-107">For more information about the different permissions you can give to users in the Security &amp; Compliance Center, check out [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d1034-108">Что нужно знать перед началом работы?</span><span class="sxs-lookup"><span data-stu-id="d1034-108">What do you need to know before you begin?</span></span>

- <span data-ttu-id="d1034-109">Для выполнения действий, описанных в данной статье, необходимо быть глобальным администратором Office 365 или членом &amp; группы ролей Организатионманажемент в центре безопасности.</span><span class="sxs-lookup"><span data-stu-id="d1034-109">You need to be an Office 365 global admin, or a member of the OrganizationManagement role group in the Security &amp; Compliance Center, to complete the steps in this article.</span></span>
    
- <span data-ttu-id="d1034-110">Группы ролей для центра соответствия &amp; требованиям безопасности могут иметь похожие имена для групп ролей в Exchange Online, но они не одинаковы.</span><span class="sxs-lookup"><span data-stu-id="d1034-110">Role groups for the Security &amp; Compliance Center might have similar names to the role groups in Exchange Online, but they're not the same.</span></span> 
    
- <span data-ttu-id="d1034-111">Членство в группах ролей не является общим для Exchange Online и центра &amp; соответствия требованиям безопасности.</span><span class="sxs-lookup"><span data-stu-id="d1034-111">Role group memberships aren't shared between Exchange Online and the Security &amp; Compliance Center.</span></span>
    
## <a name="use-the-office-365-admin-center-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="d1034-112">Использование центра администрирования Office 365 для предоставления другому пользователю доступа к центру соответствия требованиям &amp; безопасности</span><span class="sxs-lookup"><span data-stu-id="d1034-112">Use the Office 365 admin center to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="d1034-113">[Войдите в Office 365 и перейдите в центр администрирования](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span><span class="sxs-lookup"><span data-stu-id="d1034-113">[Sign in to Office 365 and go to the Admin center](https://go.microsoft.com/fwlink/p/?LinkId=525275).</span></span>
    
2. <span data-ttu-id="d1034-114">В центре администрирования Office 365 откройте **центр администрирования** и выберите \*\*соответствие требованиям безопасности &amp; \*\*.</span><span class="sxs-lookup"><span data-stu-id="d1034-114">In the Office 365 admin center, open **Admin centers** and then click **Security &amp; Compliance**.</span></span> 
    
3. <span data-ttu-id="d1034-115">В центре безопасности &amp; и соответствия требованиям выберите **разрешения**.</span><span class="sxs-lookup"><span data-stu-id="d1034-115">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
4. <span data-ttu-id="d1034-116">В списке выберите группу ролей, в которую нужно добавить пользователя, и нажмите кнопку **изменить** ![значок](media/O365_MDM_CreatePolicy_EditIcon.gif)редактирования.</span><span class="sxs-lookup"><span data-stu-id="d1034-116">From the list, choose the role group that you want to add the user to and click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
5. <span data-ttu-id="d1034-117">На странице свойств группы ролей в разделе **Участники**нажмите **Добавить**![значок](media/ITPro-EAC-AddIcon.gif) добавить и выберите имя пользователя (или пользователей), которого вы хотите добавить.</span><span class="sxs-lookup"><span data-stu-id="d1034-117">In the role group's properties page under **Members**, click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and select the name of the user (or users) you want to add.</span></span> 
    
6. <span data-ttu-id="d1034-118">Выбрав всех пользователей, которых вы хотите добавить в группу ролей, нажмите кнопку **Add (добавить\> )** , а затем кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d1034-118">When you've selected all of the users you want to add to the role group, click **add-\>** and then **OK**.</span></span>
    
7. <span data-ttu-id="d1034-119">Нажмите кнопку **Сохранить**, чтобы сохранить изменения в группе ролей.</span><span class="sxs-lookup"><span data-stu-id="d1034-119">Click **Save** to save the changes to the role group.</span></span> 
    
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="d1034-120">Как проверить, что все получилось</span><span class="sxs-lookup"><span data-stu-id="d1034-120">How do you know this worked?</span></span>

1. <span data-ttu-id="d1034-121">В центре безопасности &amp; и соответствия требованиям выберите **разрешения**.</span><span class="sxs-lookup"><span data-stu-id="d1034-121">In the Security &amp; Compliance Center, go to **Permissions**.</span></span>
    
2. <span data-ttu-id="d1034-122">В списке выберите группу ролей, чтобы просмотреть ее участников.</span><span class="sxs-lookup"><span data-stu-id="d1034-122">From the list, select the role group to view the members.</span></span>
    
3. <span data-ttu-id="d1034-123">Справа в разделе сведения о группе ролей можно просмотреть членов группы ролей.</span><span class="sxs-lookup"><span data-stu-id="d1034-123">On the right, in the role group details, you can view the members of the role group.</span></span>
    
## <a name="use-powershell-to-give-another-user-access-to-the-security-amp-compliance-center"></a><span data-ttu-id="d1034-124">Использование PowerShell для предоставления другому пользователю доступа к центру безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d1034-124">Use PowerShell to give another user access to the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="d1034-125">[Подключитесь к PowerShell центра безопасности _амп_ для Office 365](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="d1034-125">[Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="d1034-126">Воспользуйтесь командой **Add-RoleGroupMember**, чтобы добавить пользователя в группу ролей Organization Management (Управление организацией), как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d1034-126">Use the **Add-RoleGroupMember** command to add a user to the Organization Management Role, as shown in the following example.</span></span> 
    
  ```
  Add-RoleGroupMember -Identity "OrganizationManagement" -Member MatildaS
  
  ```

 <span data-ttu-id="d1034-127">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="d1034-127">**Parameters**</span></span>
  
- <span data-ttu-id="d1034-128">_-Identity_ — группа ролей, в которую необходимо добавить участника.</span><span class="sxs-lookup"><span data-stu-id="d1034-128">_-Identity_ is the role group to add a member to.</span></span> 
    
- <span data-ttu-id="d1034-129">_Member_ является почтовым ящиком, универсальной группой безопасности (универсальную группу безопасности) или компьютером, который требуется добавить в группу ролей.</span><span class="sxs-lookup"><span data-stu-id="d1034-129">_Member_ is the mailbox, universal security group (USG), or computer to add to the role group.</span></span> <span data-ttu-id="d1034-130">За один раз можно добавить только одного участника.</span><span class="sxs-lookup"><span data-stu-id="d1034-130">You can specify only one member at a time.</span></span> 
    
<span data-ttu-id="d1034-131">Подробную информацию о синтаксисе и параметрах можно узнать в статье [Add/RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span><span class="sxs-lookup"><span data-stu-id="d1034-131">For detailed information on syntax and parameters, see [Add-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510859).</span></span>
  
### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="d1034-132">Как проверить, все ли получилось?</span><span class="sxs-lookup"><span data-stu-id="d1034-132">How do you know this worked?</span></span>

<span data-ttu-id="d1034-133">Чтобы убедиться, что у пользователей есть доступ к центру соответствия &amp; требованиям безопасности, используйте командлет **Get – RoleGroupMember** для просмотра членов группы ролей "Управление организацией", как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d1034-133">To verify that you've given users access to the Security &amp; Compliance Center, use the **Get-RoleGroupMember** cmdlet to view the members in the Organization Management role group, as shown in the following example.</span></span> 
  
```
Get-RoleGroupMember -Identity "OrganizationManagement"

```

<span data-ttu-id="d1034-134">Подробную информацию о синтаксисе и параметрах можно найти в статье [Get – RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span><span class="sxs-lookup"><span data-stu-id="d1034-134">For detailed information on syntax and parameters, see [Get-RoleGroupMember](https://go.microsoft.com/fwlink/p/?LinkId=510860).</span></span>
  

