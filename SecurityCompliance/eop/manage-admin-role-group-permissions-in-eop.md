---
title: Управление разрешениями группы ролей администраторов в EOP
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 125834f4-1024-4325-ad5a-d2573cfb005e
description: В Microsoft Exchange Online Protection (EOP) с помощью Центра администрирования Exchange можно назначать пользователя членом одной или нескольких групп ролей, чтобы предоставлять ему права на выполнение определенных задач администрирования. С помощью Центра администрирования Exchange можно также удалять пользователя из одной или нескольких групп ролей.
ms.openlocfilehash: aed32c8a9224bc60ef3e4a1ac9be9d797e61bda8
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693428"
---
# <a name="manage-admin-role-group-permissions-in-eop"></a><span data-ttu-id="282f8-104">Управление разрешениями группы ролей администраторов в EOP</span><span class="sxs-lookup"><span data-stu-id="282f8-104">Manage admin role group permissions in EOP</span></span>
  
<span data-ttu-id="282f8-p102">В Microsoft Exchange Online Protection (EOP) с помощью Центра администрирования Exchange можно назначать пользователя членом одной или нескольких групп ролей, чтобы предоставлять ему права на выполнение определенных задач администрирования. С помощью Центра администрирования Exchange можно также удалять пользователя из одной или нескольких групп ролей.</span><span class="sxs-lookup"><span data-stu-id="282f8-p102">In Microsoft Exchange Online Protection (EOP), you can use the Exchange admin center (EAC) to make a user a member of a role group or groups in order to assign them permissions to perform specific administrative tasks. You can also remove a user from a role group or groups by using the EAC.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="282f8-107">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="282f8-107">What do you need to know before you begin?</span></span>

- <span data-ttu-id="282f8-108">Предполагаемое время для завершения: 5-10 минут.</span><span class="sxs-lookup"><span data-stu-id="282f8-108">Estimated time to complete: 5-10 minutes</span></span>
    
- <span data-ttu-id="282f8-p103">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье Пункт "Пользователи, контакты и группы ролей" в разделе [Разрешения на функции в службе EOP](feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="282f8-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Users, Contacts, and Role Groups" entry in the [Feature permissions in EOP](feature-permissions-in-eop.md) topic.</span></span> 
    
- <span data-ttu-id="282f8-p104">Определенные разрешения в Office 365 сопоставляются с разрешениями группы ролей администратора EOP. Подробнее см. в столбце "Роль в Exchange Online" в подразделе "На какие службы распространяются мои разрешения в Office 365?" в разделе [Назначение ролей администратора](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span><span class="sxs-lookup"><span data-stu-id="282f8-p104">Certain permissions in Office 365 map to EOP admin role group permissions. For more information, see the "Role in Exchange Online" column in the "Which services do my Office 365 permissions extend to?" section in [Assigning Admin Roles](https://go.microsoft.com/fwlink/p/?LinkId=286708).</span></span>
    
- <span data-ttu-id="282f8-114">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="282f8-114">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
> [!TIP]
> <span data-ttu-id="282f8-p105">Возникли проблемы? Обратитесь за помощью к участникам форумов, посвященных Exchange. Посетите форумы по таким продуктам: [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612), [Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542) или [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span><span class="sxs-lookup"><span data-stu-id="282f8-p105">Having problems? Ask for help in the Exchange forums. Visit the forums at [Exchange Server](https://go.microsoft.com/fwlink/p/?linkId=60612),[Exchange Online](https://go.microsoft.com/fwlink/p/?linkId=267542), or [Exchange Online Protection](https://go.microsoft.com/fwlink/p/?linkId=285351).</span></span> 
  
## <a name="what-do-you-want-to-do"></a><span data-ttu-id="282f8-118">Что необходимо сделать?</span><span class="sxs-lookup"><span data-stu-id="282f8-118">What do you want to do?</span></span>

### <a name="use-the-eac-to-assign-members-to-admin-role-groups"></a><span data-ttu-id="282f8-119">Использование Центра администрирования Exchange для добавления членов в группы ролей администратора</span><span class="sxs-lookup"><span data-stu-id="282f8-119">Use the EAC to assign members to admin role groups</span></span>

1. <span data-ttu-id="282f8-120">В центре администрирования Exchange перейдите к \*\*\*\* \> **роли администратора**разрешений, щелкните группу ролей, в которую нужно добавить пользователя или пользователей, а затем щелкните **изменить** ![значок](../media/ITPro-EAC-EditIcon.gif)редактирования.</span><span class="sxs-lookup"><span data-stu-id="282f8-120">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to add the user or users to, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span>
    
2. <span data-ttu-id="282f8-p106">В области "Члены" нажмите кнопку **Добавить**![Значок добавления](../media/ITPro-EAC-AddIcon.gif). Откроется окно "Выбор членов".</span><span class="sxs-lookup"><span data-stu-id="282f8-p106">Under Members, click **Add**![Add Icon](../media/ITPro-EAC-AddIcon.gif). The Select Members window will appear.</span></span>
    
3. <span data-ttu-id="282f8-123">Выполните поиск одного или нескольких пользователей, которых нужно добавить, или выберите их из списка.</span><span class="sxs-lookup"><span data-stu-id="282f8-123">Search for the user or users that you wish to add, or select them from the list.</span></span>
    
4. <span data-ttu-id="282f8-p107">Выбрав одного или нескольких пользователей, которых нужно добавить, нажмите кнопку **Добавить**, а затем  **ОК**. Окно "Выбор членов" закроется.</span><span class="sxs-lookup"><span data-stu-id="282f8-p107">When you have selected the user or users that you want to add, click **Add**, and then click **OK**. The Select Members window will close.</span></span>
    
5. <span data-ttu-id="282f8-p108">Вы увидите, что пользователь добавлен в область **Члены**. Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="282f8-p108">You will see that the user has been added to the **Members** pane. Click **Save**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="282f8-128">После добавления или удаления членов группы ролей данным пользователям необходимо выйти из системы, а затем снова войти в нее, чтобы изменить административные права.</span><span class="sxs-lookup"><span data-stu-id="282f8-128">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
### <a name="use-the-eac-to-remove-members-from-admin-role-groups"></a><span data-ttu-id="282f8-129">Использование Центра администрирования Exchange для удаления членов из группы ролей администратора</span><span class="sxs-lookup"><span data-stu-id="282f8-129">Use the EAC to remove members from admin role groups</span></span>

1. <span data-ttu-id="282f8-130">В центре администрирования Exchange перейдите к \*\*\*\* \> **роли администратора**разрешений, выберите группу ролей, из которой требуется удалить пользователя или пользователей, а затем нажмите кнопку **изменить** ![значок](../media/ITPro-EAC-EditIcon.gif)редактирования.</span><span class="sxs-lookup"><span data-stu-id="282f8-130">In the EAC, navigate to **Permissions** \> **Admin Roles**, click the role group that you want to remove a user or users from, and then click **Edit** ![Edit icon](../media/ITPro-EAC-EditIcon.gif).</span></span>
    
2. <span data-ttu-id="282f8-131">В разделе "Члены" выберите одного или нескольких пользователей, которых нужно удалить, и нажмите кнопку **Удалить**![Значок "Удалить"](../media/ITPro-EAC-RemoveIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="282f8-131">Under Members, select the user or users that you want to remove and click **Remove**![Remove icon](../media/ITPro-EAC-RemoveIcon.gif).</span></span>
    
3. <span data-ttu-id="282f8-p109">Нажмите кнопку **Сохранить**, чтобы сохранить изменение группы ролей и вернуться на страницу **Роли администратора**. Чтобы проверить, удален ли пользователь из группы ролей администратора, убедитесь, что он больше не отображается в разделе "Члены" в области сведений для выбранной группы ролей.</span><span class="sxs-lookup"><span data-stu-id="282f8-p109">Click **Save** to save the change to the role group and return to the **Admin Roles** page. To verify that you've successfully removed the user from the administrator role group, make sure the member is no longer displayed under Members in the details pane for the selected role group.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="282f8-134">После добавления или удаления членов группы ролей данным пользователям необходимо выйти из системы, а затем снова войти в нее, чтобы изменить административные права.</span><span class="sxs-lookup"><span data-stu-id="282f8-134">Users may have to sign out and sign in again to see the change in their administrative rights after you add or remove members from the role group.</span></span> 
  
## <a name="for-more-information"></a><span data-ttu-id="282f8-135">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="282f8-135">For more information</span></span>

[<span data-ttu-id="282f8-136">Разрешения на функции в службе EOP</span><span class="sxs-lookup"><span data-stu-id="282f8-136">Feature permissions in EOP</span></span>](feature-permissions-in-eop.md)
  

