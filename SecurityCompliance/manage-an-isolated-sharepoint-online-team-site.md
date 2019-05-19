---
title: Управление изолированным сайтом группы SharePoint Online
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 79a61003-4905-4ba8-9e8a-16def7add37c
description: Сводка. Управляйте изолированным сайтом группы SharePoint Online с помощью этих процедур.
ms.openlocfilehash: 1670c806c799cdbd9ffa6d3c45568a3342b88815
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155821"
---
# <a name="manage-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="de0c5-103">Управление изолированным сайтом группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de0c5-103">Manage an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="de0c5-104">**Сводка.** Управляйте изолированным сайтом группы SharePoint Online с помощью этих процедур.</span><span class="sxs-lookup"><span data-stu-id="de0c5-104">**Summary:** Manage your isolated SharePoint Online team site with these procedures.</span></span>
  
<span data-ttu-id="de0c5-105">В этой статье описаны основные операции по управлению изолированным сайтом группы SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="de0c5-105">This article describes common management operations for an isolated SharePoint Online team site.</span></span>
  
## <a name="add-a-new-user"></a><span data-ttu-id="de0c5-106">Добавление нового пользователя</span><span class="sxs-lookup"><span data-stu-id="de0c5-106">Add a new user</span></span>

<span data-ttu-id="de0c5-107">Когда к сайту присоединяется новый участник, необходимо определить его роль.</span><span class="sxs-lookup"><span data-stu-id="de0c5-107">When someone new joins the site, you must decide their level of participation in the site:</span></span>
  
- <span data-ttu-id="de0c5-108">Администрирование: добавьте новую учетную запись пользователя в группу доступа "Администраторы сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-108">Administration: Add the new user account to the site admins access group</span></span>
    
- <span data-ttu-id="de0c5-109">Активная совместная работа: добавьте учетную запись пользователя в группу доступа "Участники сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-109">Active collaboration: Add the user account to the site members access group</span></span>
    
- <span data-ttu-id="de0c5-110">Просмотр: добавьте учетную запись пользователя в группу доступа "Посетители сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-110">Viewing: Add the user account to the site viewers access group</span></span>
    
<span data-ttu-id="de0c5-111">Если вы управляете учетными записями и группами пользователей с помощью Windows Server Active Directory (AD), добавьте пользователей в соответствующие группы доступа, применяя стандартные процедуры управления пользователями и группами в Windows Server AD, и дождитесь синхронизации со своей подпиской на Office 365.</span><span class="sxs-lookup"><span data-stu-id="de0c5-111">If you are managing user accounts and groups through Windows Server Active Directory (AD), add the appropriate users to the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="de0c5-112">Если вы управляете учетными записями и группами пользователей с помощью Office 365, вы можете воспользоваться Центром администрирования Office или оболочкой Microsoft PowerShell:</span><span class="sxs-lookup"><span data-stu-id="de0c5-112">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or Microsoft PowerShell:</span></span>
  
- <span data-ttu-id="de0c5-113">Войдите в Центр администрирования Office, используя учетную запись, которой назначена роль администратора учетных записей пользователей или администратора организации, и выберите раздел "Группы", чтобы добавить пользователей в соответствующие группы доступа.</span><span class="sxs-lookup"><span data-stu-id="de0c5-113">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate users to the appropriate access groups.</span></span>
    
- <span data-ttu-id="de0c5-114">Для PowerShell сначала подключитесь к [модулю PowerShell Azure Active Directory PowerShell для Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="de0c5-114">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span> <span data-ttu-id="de0c5-115">Чтобы добавить учетную запись пользователя в группу доступа по имени участника-пользователя (UPN), используйте следующий блок команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="de0c5-115">To add a user account to an access group with its user principal name (UPN), use the following PowerShell command block:</span></span>
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> <span data-ttu-id="de0c5-116">Текстовый файл со всеми командами PowerShell и лист Excel для создания команд PowerShell на основе имен групп и учетных записей пользователей вы найдете в [комплекте средств для развертывания изолированного сайта группы SharePoint Online](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span><span class="sxs-lookup"><span data-stu-id="de0c5-116">For a text file that contains all the PowerShell commands and an Excel configuration worksheet that generates PowerShell commands based on your group and user account names, download the [Isolated SharePoint Online Team Site Deployment Kit](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span></span> 

<span data-ttu-id="de0c5-117">Чтобы добавить учетную запись пользователя в группу доступа по отображаемому имени, используйте следующий блок команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="de0c5-117">To add a user account to an access group with its display name, use the following PowerShell command block:</span></span>

```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="add-a-new-group"></a><span data-ttu-id="de0c5-118">Добавление новой группы</span><span class="sxs-lookup"><span data-stu-id="de0c5-118">Add a new group</span></span>

<span data-ttu-id="de0c5-119">Чтобы добавить доступ для всей группы, необходимо определить роль всех членов группы на сайте:</span><span class="sxs-lookup"><span data-stu-id="de0c5-119">To add access to an entire group, you must decide the level of participation of all the members of the group in the site:</span></span>
  
- <span data-ttu-id="de0c5-120">Администрирование: добавьте группу в группу доступа "Администраторы сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-120">Administration: Add the group to the site admins access group</span></span>
    
- <span data-ttu-id="de0c5-121">Активная совместная работа: добавьте группу в группу доступа "Участники сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-121">Active collaboration: Add the group to the site members access group</span></span>
    
- <span data-ttu-id="de0c5-122">Просмотр: добавьте группу в группу доступа "Посетители сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-122">Viewing: Add the group to the site viewers access group</span></span>
    
<span data-ttu-id="de0c5-123">Если вы управляете учетными записями и группами пользователей с помощью Windows Server AD, добавьте группы в соответствующие группы, используя стандартные процедуры управления пользователями и группами в Windows Server AD, и дождитесь синхронизации со своей подпиской на Office 365.</span><span class="sxs-lookup"><span data-stu-id="de0c5-123">If you are managing user accounts and groups through Windows Server AD, add the appropriate groups to the appropriate groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="de0c5-124">Если вы управляете учетными записями и группами пользователей с помощью Office 365, выполните эту задачу в PowerShell или Центре администрирования Office:</span><span class="sxs-lookup"><span data-stu-id="de0c5-124">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="de0c5-125">Войдите в Центр администрирования Office, используя учетную запись, которой назначена роль администратора учетных записей пользователей или администратора организации, и выберите раздел "Группы", чтобы добавить группы в соответствующие группы доступа.</span><span class="sxs-lookup"><span data-stu-id="de0c5-125">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate groups to the appropriate access groups.</span></span>
    
- <span data-ttu-id="de0c5-126">Для PowerShell сначала подключитесь к [модулю PowerShell Azure Active Directory PowerShell для Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="de0c5-126">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
 <span data-ttu-id="de0c5-127">Затем используйте следующие команды PowerShell:</span><span class="sxs-lookup"><span data-stu-id="de0c5-127">Then, use the following PowerShell commands:</span></span>
 
```
$newGroupName="<display name of the new group to add>"
$siteGrpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $newGroupName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $siteGrpName }).ObjectID
```

## <a name="remove-a-user"></a><span data-ttu-id="de0c5-128">Удаление пользователя</span><span class="sxs-lookup"><span data-stu-id="de0c5-128">Remove a user</span></span>

<span data-ttu-id="de0c5-129">Чтобы закрыть доступ к сайту для пользователя, удалите его из группы доступа, в которой он в данный момент состоит.</span><span class="sxs-lookup"><span data-stu-id="de0c5-129">When someone's access must be removed from the site, you remove them from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="de0c5-130">Администрирование: удалите учетную запись пользователя из группы доступа "Администраторы сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-130">Administration: Remove the user account from the site admins access group</span></span>
    
- <span data-ttu-id="de0c5-131">Активная совместная работа: удалите учетную запись пользователя из группы доступа "Участники сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-131">Active collaboration: Remove the user account from the site members access group</span></span>
    
- <span data-ttu-id="de0c5-132">Просмотр: удалите учетную запись пользователя из группы доступа "Посетители сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-132">Viewing: Remove the user account from the site viewers access group</span></span>
    
<span data-ttu-id="de0c5-133">Если вы управляете учетными записями и группами пользователей с помощью Windows Server AD, удалите пользователей из соответствующих групп доступа, применяя стандартные процедуры управления пользователями и группами в Windows Server AD, и дождитесь синхронизации со своей подпиской на Office 365.</span><span class="sxs-lookup"><span data-stu-id="de0c5-133">If you are managing user accounts and groups through Windows Server AD, remove the appropriate users from the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="de0c5-134">Если вы управляете учетными записями и группами пользователей с помощью Office 365, выполните эту задачу в PowerShell или Центре администрирования Office:</span><span class="sxs-lookup"><span data-stu-id="de0c5-134">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="de0c5-135">Войдите в Центр администрирования Office, используя учетную запись, которой назначена роль администратора учетных записей пользователей или администратора организации, и выберите раздел "Группы", чтобы удалить пользователей из соответствующих групп доступа.</span><span class="sxs-lookup"><span data-stu-id="de0c5-135">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate users from the appropriate access groups.</span></span>
    
- <span data-ttu-id="de0c5-136">Для PowerShell сначала подключитесь к [модулю PowerShell Azure Active Directory PowerShell для Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="de0c5-136">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
<span data-ttu-id="de0c5-137">Чтобы удалить учетную запись пользователя из группы доступа по имени участника-пользователя, используйте следующий блок команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="de0c5-137">To remove a user account from an access group with its UPN, use the following PowerShell command block:</span></span>
    
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

<span data-ttu-id="de0c5-138">Чтобы удалить учетную запись пользователя из группы доступа по отображаемому имени, используйте следующий блок команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="de0c5-138">To remove a user account from an access group with its display name, use the following PowerShell command block:</span></span>
    
```
$userDisplayName="<display name of the user account>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADUser | Where { $_.DisplayName -eq $userDisplayName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="remove-a-group"></a><span data-ttu-id="de0c5-139">Удаление группы</span><span class="sxs-lookup"><span data-stu-id="de0c5-139">Remove a group</span></span>

<span data-ttu-id="de0c5-140">Чтобы закрыть доступ для всей группы, удалите ее из группы доступа, в которой она в данный момент состоит:</span><span class="sxs-lookup"><span data-stu-id="de0c5-140">To remove access for an entire group, you remove the group from the access group for which they are currently a member based on their participation in the site:</span></span>
  
- <span data-ttu-id="de0c5-141">Администрирование: удалите группу из группы доступа "Администраторы сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-141">Administration: Remove the group from the site admins access group</span></span>
    
- <span data-ttu-id="de0c5-142">Активная совместная работа: удалите группу из группы доступа "Участники сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-142">Active collaboration: Remove the group from the site members access group</span></span>
    
- <span data-ttu-id="de0c5-143">Просмотр: удалите группу из группы доступа "Посетители сайта".</span><span class="sxs-lookup"><span data-stu-id="de0c5-143">Viewing: Remove the group from the site viewers access group</span></span>
    
<span data-ttu-id="de0c5-144">Если вы управляете учетными записями и группами пользователей с помощью Windows Server Active Directory, удалите группы из соответствующих групп доступа, применяя стандартные процедуры управления пользователями и группами в Windows Server AD, и дождитесь синхронизации со своей подпиской на Office 365.</span><span class="sxs-lookup"><span data-stu-id="de0c5-144">If you are managing user accounts and groups through Windows Server Active Directory, remove the appropriate groups from the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="de0c5-145">Если вы управляете учетными записями и группами пользователей с помощью Office 365, выполните эту задачу в PowerShell или Центре администрирования Office:</span><span class="sxs-lookup"><span data-stu-id="de0c5-145">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell:</span></span>
  
- <span data-ttu-id="de0c5-146">Войдите в Центр администрирования Office, используя учетную запись, которой назначена роль администратора учетных записей пользователей или администратора организации, и выберите раздел "Группы", чтобы удалить группы из соответствующих групп доступа.</span><span class="sxs-lookup"><span data-stu-id="de0c5-146">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to remove the appropriate groups from the appropriate access groups.</span></span>
    
- <span data-ttu-id="de0c5-147">Для PowerShell сначала подключитесь к [модулю PowerShell Azure Active Directory PowerShell для Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="de0c5-147">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>    
<span data-ttu-id="de0c5-148">Чтобы удалить группу из группы доступа по отображаемому имени, используйте следующий блок команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="de0c5-148">To remove a group from an access group using their display names, use the following PowerShell command block:</span></span>
    
```
$groupMemberName="<display name of the group to remove>"
$grpName="<display name of the access group>"
Remove-AzureADGroupMember -MemberId (Get-AzureADGroup | Where { $_.DisplayName -eq $groupMemberName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

## <a name="create-a-documents-subfolder-with-custom-permissions"></a><span data-ttu-id="de0c5-149">Создание вложенной папки документов с настраиваемыми разрешениями</span><span class="sxs-lookup"><span data-stu-id="de0c5-149">Create a documents subfolder with custom permissions</span></span>

<span data-ttu-id="de0c5-p104">Группе людей, работающих на изолированном сайте, может потребоваться закрытое место для совместной работы. В SharePoint Online вы можете создать вложенную папку в папке сайта "Документы" и назначить ей особые разрешения. Пользователи без разрешений не увидят эту папку.</span><span class="sxs-lookup"><span data-stu-id="de0c5-p104">In some cases, a subset of the people working within the isolated site need a more private place to collaborate. For SharePoint Online sites, you can create a subfolder in the Documents folder of the site and assign custom permissions. Those without permissions will not see the subfolder.</span></span>
  
<span data-ttu-id="de0c5-153">Чтобы создать вложенную папку документов с настраиваемыми разрешениями, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="de0c5-153">To create a documents subfolder with custom permissions, do the following:</span></span>
  
1. <span data-ttu-id="de0c5-p105">Войдите в Office 365, используя учетную запись, состоящую в группе доступа "Администраторы" для сайта. Справочные материалы см. в статье [Вход в Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="de0c5-p105">Sign in to Office 365 with an account that is a member of the admins access group for the site. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="de0c5-156">Перейдите к изолированному сайту группы и нажмите **Документы**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-156">Go to the isolated team site and click **Documents**.</span></span>
    
3. <span data-ttu-id="de0c5-157">В папке "Документы" перейдите к нужной папке, создайте вложенную папку для настраиваемых разрешений и откройте ее.</span><span class="sxs-lookup"><span data-stu-id="de0c5-157">Browse to the folder in the documents folder that will contain the subfolder with custom permissions, create the folder, and then open it.</span></span>
    
4. <span data-ttu-id="de0c5-158">Щелкните **Общий доступ**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-158">Click **Share**.</span></span>
    
5. <span data-ttu-id="de0c5-159">Нажмите **Доступ > Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-159">Click **Shared with > Advanced**.</span></span>
    
6. <span data-ttu-id="de0c5-160">Нажмите **Прекратить наследование разрешений**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-160">Click **Stop inheriting permissions**, and then click **OK**.</span></span>
    
7. <span data-ttu-id="de0c5-161">Щелкните **Общий доступ**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-161">Click **Share**.</span></span>
    
8. <span data-ttu-id="de0c5-162">Нажмите **Доступ > Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-162">Click **Shared with > Advanced**.</span></span>
    
9. <span data-ttu-id="de0c5-163">Нажмите **Предоставить разрешения > Доступ > Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-163">Click **Grant Permissions > Shared with > Advanced**.</span></span>
    
10. <span data-ttu-id="de0c5-164">На странице разрешений выберите **\<имя сайта> Участники в списке**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-164">On the permissions page, click **\<site name> Members in the list**.</span></span>
    
11. <span data-ttu-id="de0c5-165">На странице **\<имя сайта> Участники** установите флажок рядом с группой доступа "Участники сайта", выберите **Действия** > **Удалить пользователей из группы** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-165">On the **\<site name> Members** page, select the checkmark next to the site members access group, click **Actions**, click **Remove users from group**, and then click **OK**.</span></span>
    
12. <span data-ttu-id="de0c5-166">Чтобы добавить участников в эту вложенную папку, нажмите **Создать > Добавить пользователей**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-166">To add specific members to this subfolder, click **New > Add users**.</span></span>
    
13. <span data-ttu-id="de0c5-167">В диалоговом окне **Общий доступ** введите имена учетных записей пользователей, которые могут совместно работать над файлами в папке, и нажмите кнопку **Поделиться**.</span><span class="sxs-lookup"><span data-stu-id="de0c5-167">In the **Share** dialog box, type the names of the user accounts that can collaborate on files in the subfolder, and then click **Share**.</span></span>
    
14. <span data-ttu-id="de0c5-168">Обновите веб-страницу, чтобы увидеть новые результаты.</span><span class="sxs-lookup"><span data-stu-id="de0c5-168">Refresh the web page to see the new results.</span></span>
    
15. <span data-ttu-id="de0c5-169">В области навигации слева выберите группу **\<имя сайта> Посетители** в разделе **Группы** и выполните действия 11–14, чтобы указать учетные записи пользователей, которые могут просматривать файлы во вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="de0c5-169">Under **Groups** in the left navigation, click the **\<site name> Visitors** group and use steps 11-14 to specify the set of user accounts that can view the files in the subfolder (as needed).</span></span>
    
16. <span data-ttu-id="de0c5-170">В области навигации слева выберите группу **\<имя сайта> -Владельцы** в разделе **Группы** и выполните действия 11–14, чтобы указать учетные записи пользователей, которые могут управлять разрешениями во вложенной папке.</span><span class="sxs-lookup"><span data-stu-id="de0c5-170">Under **Groups** in the left navigation, click the **\<site name> Owners** group and use steps 11-14 to specify the set of user accounts that can administer the permissions in the subfolder (as needed).</span></span>
    
17. <span data-ttu-id="de0c5-171">Закройте вкладку **Пользователи и группы** в браузере.</span><span class="sxs-lookup"><span data-stu-id="de0c5-171">Close the **People and Groups** tab in your browser.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de0c5-172">См. также</span><span class="sxs-lookup"><span data-stu-id="de0c5-172">See Also</span></span>

[<span data-ttu-id="de0c5-173">Изолированные сайты групп SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de0c5-173">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="de0c5-174">Разработка изолированного сайта группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de0c5-174">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="de0c5-175">Развертывание изолированного сайта группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="de0c5-175">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



