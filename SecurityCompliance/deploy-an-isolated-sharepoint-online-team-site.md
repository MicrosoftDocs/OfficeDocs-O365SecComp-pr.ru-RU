---
title: Развертывание изолированного сайта группы SharePoint Online
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 05/14/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 3033614b-e23b-4f68-9701-f62525eafaab
description: Сводка. С помощью этих пошаговых инструкций можно развернуть новый изолированный сайт группы SharePoint Online.
ms.openlocfilehash: 4cb60cd55f526592cb469d80a061375a4f556afe
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257024"
---
# <a name="deploy-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="c5020-103">Развертывание изолированного сайта группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c5020-103">Deploy an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="c5020-104">**Сводка.** С помощью этих пошаговых инструкций можно развернуть новый изолированный сайт группы SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c5020-104">**Summary:** Deploy a new isolated SharePoint Online team site with these step-by-step instructions.</span></span>
  
<span data-ttu-id="c5020-p101">Эта статья представляет собой пошаговое руководство по созданию и настройке изолированного сайта группы SharePoint Online в Microsoft Office 365. Эти инструкции предполагают использование трех групп SharePoint по умолчанию и соответствующих уровней разрешений (по одной группе доступа на основе Azure Active Directory (AD) для каждого уровня доступа).</span><span class="sxs-lookup"><span data-stu-id="c5020-p101">This article is a step-by-step deployment guide for creating and configuring an isolated SharePoint Online team site in Microsoft Office 365. These steps assume the use of the three default SharePoint groups and corresponding permission levels, with a single Azure Active Directory (AD)-based access group for each level of access.</span></span>
  
## <a name="phase-1-create-and-populate-the-team-site-access-groups"></a><span data-ttu-id="c5020-107">Этап 1: создание и заполнение групп доступа к сайту группы</span><span class="sxs-lookup"><span data-stu-id="c5020-107">Phase 1: Create and populate the team site access groups</span></span>

<span data-ttu-id="c5020-108">На этом этапе вы создаете три группы доступа на основе Azure AD для трех групп SharePoint по умолчанию и заполняете их соответствующими учетными записями пользователей.</span><span class="sxs-lookup"><span data-stu-id="c5020-108">In this phase, you create the three Azure AD-based access groups for the three default SharePoint groups and populate them with the appropriate user accounts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c5020-p102">При выполнении последующих шагов предполагается, что все необходимые учетные записи пользователей уже существуют и для них назначены соответствующие лицензии. Если это не сделано, завершите требуемые действия, прежде чем переходить к шагу 1.</span><span class="sxs-lookup"><span data-stu-id="c5020-p102">The following steps assume that all necessary user accounts already exist and are assigned the appropriate licenses. If not, please add them and assign licenses before proceeding to step 1.</span></span> 
  
### <a name="step-1-list-the-sharepoint-online-admins-for-the-site"></a><span data-ttu-id="c5020-111">Шаг 1. Составление списка администраторов сайта SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c5020-111">Step 1: List the SharePoint Online admins for the site</span></span>

<span data-ttu-id="c5020-112">Определите набор учетных записей пользователей для администраторов изолированного сайта группы SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c5020-112">Determine the set of user accounts corresponding to the SharePoint Online admins for the isolated team site.</span></span>
  
<span data-ttu-id="c5020-113">Если вы управляете учетными записями и группами пользователей с помощью Office 365 и хотите использовать Windows PowerShell, составьте список имен участников-пользователей (например, marthaa@contoso.com).</span><span class="sxs-lookup"><span data-stu-id="c5020-113">If you are managing user accounts and groups through Office 365 and want to use Windows PowerShell, make a list of their user principal names (UPNs) (example UPN: belindan@contoso.com).</span></span>
  
### <a name="step-2-list-the-members-for-the-site"></a><span data-ttu-id="c5020-114">Шаг 2. Составление списка участников сайта</span><span class="sxs-lookup"><span data-stu-id="c5020-114">Step 2: List the members for the site</span></span>

<span data-ttu-id="c5020-115">Определите набор учетных записей пользователей для участников изолированного сайта группы, т. е. для тех, кто будет совместно работать с ресурсами, хранящимися на сайте.</span><span class="sxs-lookup"><span data-stu-id="c5020-115">Determine the set of user accounts corresponding to the members for the isolated team site, those who will be collaborating on resources stored within the site.</span></span>
  
<span data-ttu-id="c5020-p103">Если вы управляете учетными записями и группами пользователей с помощью Office 365 и планируете использовать PowerShell, составьте список имен участников-пользователей. Если на сайте много участников, вы можете сохранить список имен участников-пользователей в текстовом файле и добавить их все с помощью одной команды PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c5020-p103">If you are managing user accounts and groups through Office 365 and want to use PowerShell, make a list of their UPNs. If there are a lot of site members, you can store the list of UPNs in a text file and add them all with a single PowerShell command.</span></span>
  
### <a name="step-3-list-the-viewers-for-the-site"></a><span data-ttu-id="c5020-118">Шаг 3. Составление списка посетителей сайта</span><span class="sxs-lookup"><span data-stu-id="c5020-118">Step 3: List the viewers for the site</span></span>

<span data-ttu-id="c5020-119">Определите набор учетных записей пользователей для посетителей изолированного сайта группы, т. е. для тех, кто может просматривать ресурсы, хранящиеся на сайте, но не может изменять их или напрямую совместно работать с их содержимым.</span><span class="sxs-lookup"><span data-stu-id="c5020-119">Determine the set of user accounts corresponding to the viewers of the isolated team site, those who can view the resources stored in the site but not modify them or directly collaborate on their contents.</span></span>
  
<span data-ttu-id="c5020-p104">Если вы управляете учетными записями и группами пользователей с помощью Office 365 и планируете использовать PowerShell, составьте список имен участников-пользователей. Если на сайте много участников, вы можете сохранить список имен участников-пользователей в текстовом файле и добавить их все с помощью одной команды PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c5020-p104">If you are managing user accounts and groups through Office 365 and want to use PowerShell, make a list of their UPNs. If there are a lot of site members, you can store the list of UPNs in a text file and add them all with a single PowerShell command.</span></span>
  
<span data-ttu-id="c5020-122">Читателями сайта могут быть руководители, юрисконсульты или межведомственные заинтересованные лица.</span><span class="sxs-lookup"><span data-stu-id="c5020-122">Viewers for the site might include executive management, legal counsel, or inter-departmental stakeholders.</span></span>
  
### <a name="step-4-create-the-three-access-groups-for-the-site-in-azure-ad"></a><span data-ttu-id="c5020-123">Шаг 4. Создание трех групп доступа для сайта в Azure AD</span><span class="sxs-lookup"><span data-stu-id="c5020-123">Step 4: Create the three access groups for the site in Azure AD</span></span>

<span data-ttu-id="c5020-124">Вам нужно создать в Azure AD следующие группы доступа:</span><span class="sxs-lookup"><span data-stu-id="c5020-124">You need to create the following access groups in Azure AD:</span></span>
  
- <span data-ttu-id="c5020-125">Администраторы сайта (список из шага 1)</span><span class="sxs-lookup"><span data-stu-id="c5020-125">Site admins (which will contain the list from step 1)</span></span>
    
- <span data-ttu-id="c5020-126">Участники сайта (список из шага 2)</span><span class="sxs-lookup"><span data-stu-id="c5020-126">Site members (which will contain the list from step 2)</span></span>
    
- <span data-ttu-id="c5020-127">Читатели сайта (список из шага 3)</span><span class="sxs-lookup"><span data-stu-id="c5020-127">Site viewers (which will contain the list from step 3)</span></span>
    
1. <span data-ttu-id="c5020-128">В браузере перейдите на портал Azure [https://portal.azure.com](https://portal.azure.com) и войдите, используя учетные данные, назначенные администратором управления пользователями или ролью администратора организации.</span><span class="sxs-lookup"><span data-stu-id="c5020-128">In your browser, go to the Azure portal at [https://portal.azure.com](https://portal.azure.com) and sign in with the credentials of an account that has been assigned with User Management Admin or Company Administrator role.</span></span>
    
2. <span data-ttu-id="c5020-129">На портале Azure выберите **Azure Active Directory > Группы**.</span><span class="sxs-lookup"><span data-stu-id="c5020-129">In the Azure portal, click **Azure Active Directory > Groups**.</span></span>
    
3. <span data-ttu-id="c5020-130">В колонке **Группы — Все группы** выберите пункт **+ Создать группу**.</span><span class="sxs-lookup"><span data-stu-id="c5020-130">On the **Groups - All groups** blade, click **+ New group**.</span></span>
    
4. <span data-ttu-id="c5020-131">В колонке **Группа**:</span><span class="sxs-lookup"><span data-stu-id="c5020-131">On the **Group** blade:</span></span>
    
  - <span data-ttu-id="c5020-132">В разделе **Тип группы** выберите **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="c5020-132">Select **Office 365** in **Group type**.</span></span>
    
  - <span data-ttu-id="c5020-133">Введите имя группы в поле **имя**.</span><span class="sxs-lookup"><span data-stu-id="c5020-133">Type the group name in **Name**.</span></span>
    
  - <span data-ttu-id="c5020-134">Введите описание группы в поле **Описание группы**.</span><span class="sxs-lookup"><span data-stu-id="c5020-134">Type a description of the group in **Group description**.</span></span>
    
  - <span data-ttu-id="c5020-135">Выберите **Назначенные** в поле **Тип членства**.</span><span class="sxs-lookup"><span data-stu-id="c5020-135">Select **Assigned** in **Membership type**.</span></span>
    
5. <span data-ttu-id="c5020-136">Нажмите кнопку **Создать**, а затем закройте колонку **Группа**.</span><span class="sxs-lookup"><span data-stu-id="c5020-136">Click **Create**, and then close the **Group** blade.</span></span>
    
6. <span data-ttu-id="c5020-137">Повторите шаги 3-5 для дополнительных групп.</span><span class="sxs-lookup"><span data-stu-id="c5020-137">Repeat steps 3-5 for your additional groups.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c5020-138">Для создания групп с включенными функциями Office необходимо использовать портал Azure.</span><span class="sxs-lookup"><span data-stu-id="c5020-138">You need to use the Azure portal to create the groups so that they have Office features enabled.</span></span> <span data-ttu-id="c5020-139">Если изолированный сайт SharePoint Online позже настраивается как сайт с строго конфиденциальной информацией с меткой Azure Information Protection для шифрования файлов и назначения разрешений определенным группам, разрешенные группы должны быть созданы с включенными функциями Office.</span><span class="sxs-lookup"><span data-stu-id="c5020-139">If a SharePoint Online isolated site is later configured as a Highly Confidential site with an Azure Information Protection label to encrypt files and assign permission to specific groups, the permitted groups must have been created with Office features enabled.</span></span> <span data-ttu-id="c5020-140">После создания группы Azure AD невозможно изменить параметр компонентов Office для группы Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c5020-140">You cannot change the Office features setting of an Azure AD group after it has been created.</span></span> 
  
<span data-ttu-id="c5020-141">Ниже показана итоговая конфигурация с тремя группами доступа к сайту.</span><span class="sxs-lookup"><span data-stu-id="c5020-141">Here is your resulting configuration with the three site access groups.</span></span>
  
![Три группы доступа для развертывания изолированного сайта SharePoint Online.](media/c2557f61-478b-4494-95e9-d79fe5909e8b.png)
  
### <a name="step-5-add-the-user-accounts-to-the-access-groups"></a><span data-ttu-id="c5020-143">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="c5020-143">Step 5.</span></span> <span data-ttu-id="c5020-144">Добавление учетных записей пользователей в группы доступа</span><span class="sxs-lookup"><span data-stu-id="c5020-144">Add the user accounts to the access groups</span></span>

<span data-ttu-id="c5020-145">На этом шаге выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c5020-145">In this step, do the following:</span></span>
  
1. <span data-ttu-id="c5020-146">Добавьте список пользователей из шага 1 в группу доступа для администраторов сайта.</span><span class="sxs-lookup"><span data-stu-id="c5020-146">Add the list of users from step 1 to the site admins access group</span></span>
    
2. <span data-ttu-id="c5020-147">Добавьте список пользователей из шага 2 в группу доступа для участников сайта.</span><span class="sxs-lookup"><span data-stu-id="c5020-147">Add the list of users from step 2 to the site members access group</span></span>
    
3. <span data-ttu-id="c5020-148">Добавьте список пользователей из шага 3 в группу доступа для читателей сайта.</span><span class="sxs-lookup"><span data-stu-id="c5020-148">Add the list of users from step 3 to the site viewers access group</span></span>
    
<span data-ttu-id="c5020-149">Если вы управляете учетными записями и группами пользователей с помощью Windows Server AD, добавьте пользователей в соответствующие группы доступа, выполнив стандартные процедуры управления пользователями и группами в Windows Server AD, и дождитесь синхронизации со своей подпиской на Office 365.</span><span class="sxs-lookup"><span data-stu-id="c5020-149">If you are managing user accounts and groups through Windows Server AD, add users to the appropriate access groups using your normal Windows Server AD user and group management procedures and wait for synchronization with your Office 365 subscription.</span></span>
  
<span data-ttu-id="c5020-p107">Если вы управляете учетными записями и группами пользователей с помощью Office 365, вы можете воспользоваться Центром администрирования Office или PowerShell. Если имена групп доступа повторяются, следует воспользоваться Центром администрирования Office.</span><span class="sxs-lookup"><span data-stu-id="c5020-p107">If you are managing user accounts and groups through Office 365, you can use the Office Admin center or PowerShell. If you have duplicate group names for any of the access groups, you should use the Office Admin center.</span></span>
  
<span data-ttu-id="c5020-152">В центре администрирования Office Войдите с помощью учетной записи пользователя, которой назначена роль администратора учетной записи пользователя или администратора организации, и используйте группы, чтобы добавить соответствующие учетные записи пользователей и группы в соответствующие группы доступа.</span><span class="sxs-lookup"><span data-stu-id="c5020-152">For the Office Admin center, sign in with a user account that has been assigned the User Account Administrator or Company Administrator role and use Groups to add the appropriate user accounts and groups to the appropriate access groups.</span></span>
  
<span data-ttu-id="c5020-153">Для PowerShell сначала подключитесь к [модулю PowerShell Azure Active Directory PowerShell для Graph](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span><span class="sxs-lookup"><span data-stu-id="c5020-153">For PowerShell, first [Connect with the Azure Active Directory PowerShell for Graph module](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-office-365-powershell#connect-with-the-azure-active-directory-powershell-for-graph-module).</span></span>
  
<span data-ttu-id="c5020-154">Затем используйте следующий блок команд для добавления отдельной учетной записи пользователя в группу доступа:</span><span class="sxs-lookup"><span data-stu-id="c5020-154">Next, use the following command block to add an individual user account to an access group:</span></span>
  
```
$userUPN="<UPN of the user account>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
```

> [!TIP]
> <span data-ttu-id="c5020-155">Текстовый файл со всеми командами PowerShell и лист Excel для создания команд PowerShell на основе имен групп и учетных записей пользователей вы найдете в [комплекте средств для развертывания изолированного сайта группы SharePoint Online](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span><span class="sxs-lookup"><span data-stu-id="c5020-155">For a text file that contains all the PowerShell commands and an Excel configuration worksheet that generates PowerShell commands based on your group and user account names, download the [Isolated SharePoint Online Team Site Deployment Kit](https://gallery.technet.microsoft.com/Isolated-SharePoint-Online-0b364907).</span></span> 
  
<span data-ttu-id="c5020-156">Если вы сохранили имена участников-пользователей для учетных записей пользователей какой-либо из групп доступа в текстовом файле, воспользуйтесь следующим блоком команд PowerShell, чтобы добавить их все сразу:</span><span class="sxs-lookup"><span data-stu-id="c5020-156">If you stored the UPNs of user accounts for any of the access groups in a text file, you can use the following PowerShell command block to add them all at one time:</span></span>
  
```
$grpName="<display name of the access group>"
$fileName="<path and name of the file containing the list of account UPNs>"
$grpID=(Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID
Get-Content $fileName | ForEach { $userUPN=$_; Add-AzureADGroupMember -RefObjectId (Get-AzureADUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -ObjectID $grpID }
```

<span data-ttu-id="c5020-157">Для добавления отдельной группы в группу доступа PowerShell используйте следующий блок команд:</span><span class="sxs-lookup"><span data-stu-id="c5020-157">For PowerShell, use the following command block to add an individual group to an access group:</span></span>
  
```
$nestedGrpName="<display name of the group to add to the access group>"
$grpName="<display name of the access group>"
Add-AzureADGroupMember -RefObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $nestedGrpName }).ObjectID -ObjectID (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID

```

<span data-ttu-id="c5020-158">Результаты должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c5020-158">The results should be the following:</span></span>
  
- <span data-ttu-id="c5020-159">Группа Azure AD "Администраторы сайта" содержит учетные записи пользователей или группы администраторов сайта</span><span class="sxs-lookup"><span data-stu-id="c5020-159">The site admins Azure AD group contains the site admin user accounts or groups</span></span>
    
- <span data-ttu-id="c5020-160">Группа Azure AD "Участники сайта" содержит учетные записи пользователей или группы участников сайта.</span><span class="sxs-lookup"><span data-stu-id="c5020-160">The site members Azure AD group contains the site member user accounts or groups</span></span>
    
- <span data-ttu-id="c5020-161">Группа Azure AD для посетителей сайта содержит учетные записи пользователей или группы, которые могут просматривать только содержимое сайта.</span><span class="sxs-lookup"><span data-stu-id="c5020-161">The site viewers Azure AD group contains the user accounts or groups that can only view the site contents</span></span>
    
<span data-ttu-id="c5020-162">Проверьте список участников для каждой группы доступа в Центре администрирования Office или с помощью следующего блока команд PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c5020-162">Validate the list of group members for each access group with the Office Admin center or with the following PowerShell command block:</span></span>
  
```
$grpName="<display name of the access group>"
Get-AzureADGroupMember -ObjectId (Get-AzureADGroup | Where { $_.DisplayName -eq $grpName }).ObjectID | Sort UserPrincipalName | Select UserPrincipalName,DisplayName,UserType
```

<span data-ttu-id="c5020-163">Ниже показана итоговая конфигурация с тремя группами доступа к сайтам, заполненными учетными записями пользователей или группами.</span><span class="sxs-lookup"><span data-stu-id="c5020-163">Here is your resulting configuration with the three site access groups populated with user accounts or groups.</span></span>
  
![Три группы доступа, заполненные учетными записями пользователей.](media/2320107c-dad6-4c8f-94e5-f6427c125e71.png)
  
## <a name="phase-2-create-and-configure-the-isolated-team-site"></a><span data-ttu-id="c5020-165">Этап 2. Создание и настройка изолированного сайта группы</span><span class="sxs-lookup"><span data-stu-id="c5020-165">Phase 2: Create and configure the isolated team site</span></span>

<span data-ttu-id="c5020-166">На этом этапе вы создаете изолированный сайт SharePoint Online и настраиваете разрешения в соответствии с уровнями разрешений SharePoint Online по умолчанию, чтобы можно было использовать ваши новые группы доступа на основе Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c5020-166">In this phase, you create the isolated SharePoint Online site and configure the permissions for the default SharePoint Online permission levels to use your new Azure AD-based access groups.</span></span>
  
<span data-ttu-id="c5020-167">Сначала создайте сайт группы SharePoint Online, следуя приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="c5020-167">First, create the SharePoint Online team site with these steps.</span></span>
  
1. <span data-ttu-id="c5020-168">Войдите в Центр администрирования с помощью учетной записи, которая также используется для администрирования сайта группы SharePoint Online (учетной записи администратора SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="c5020-168">Sign in to the admin center with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="c5020-169">Дополнительные сведения см. в статье [Вход в Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="c5020-169">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="c5020-170">В списке плиток выберите **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="c5020-170">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="c5020-171">На новой вкладке **SharePoint** в браузере щелкните **+ Создать сайт**.</span><span class="sxs-lookup"><span data-stu-id="c5020-171">In the new **SharePoint** tab of your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="c5020-172">На странице **Создайте сайт** щелкните **Сайт группы**.</span><span class="sxs-lookup"><span data-stu-id="c5020-172">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="c5020-173">В поле **имя сайта**введите имя сайта группы.</span><span class="sxs-lookup"><span data-stu-id="c5020-173">In **Site name**, type a name for the team site.</span></span> 
    
6. <span data-ttu-id="c5020-174">В поле **Описание сайта группы** введите необязательное описание назначения сайта.</span><span class="sxs-lookup"><span data-stu-id="c5020-174">In **Team site description,** type an optional description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="c5020-175">В разделе **Параметры конфиденциальности** выберите **Закрытая группа: только участники имеют доступ к этому сайту** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c5020-175">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="c5020-176">В области **Кого вы хотите добавить?** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="c5020-176">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="c5020-177">Далее настройте разрешения на новом сайте группы SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c5020-177">Next, from the new SharePoint Online team site, configure permissions.</span></span>
  
1. <span data-ttu-id="c5020-178">На панели инструментов щелкните значок параметров и выберите вариант **Разрешения для сайта**.</span><span class="sxs-lookup"><span data-stu-id="c5020-178">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
2. <span data-ttu-id="c5020-179">В области **Разрешения для сайта** щелкните **Параметры дополнительных разрешений**.</span><span class="sxs-lookup"><span data-stu-id="c5020-179">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
3. <span data-ttu-id="c5020-180">На новой вкладке браузера **Разрешения** щелкните **Параметры запроса доступа**.</span><span class="sxs-lookup"><span data-stu-id="c5020-180">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
    
4. <span data-ttu-id="c5020-181">В диалоговом окне **параметры запросов на доступ** снимите **флажок Разрешить участнику предоставлять общий доступ к сайту, отдельным файлам и папкам** и разрешать запросы на **доступ** (чтобы снять все три флажка), а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c5020-181">In the **Access Requests Settings** dialog box, clear **Allow member to share the site and individual files and folders** and **Allow access requests** (so that all three check boxes are cleared), and then click **OK**.</span></span>
    
5. <span data-ttu-id="c5020-182">На вкладке **разрешения** браузера щелкните \*\* \<узел наме_гт_ участников\*\* в списке.</span><span class="sxs-lookup"><span data-stu-id="c5020-182">On the **Permissions** tab of your browser, click **\<site name> Members** in the list.</span></span>
    
6. <span data-ttu-id="c5020-183">В разделе **Пользователи и группы** нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c5020-183">In **People and Groups**, click **New**.</span></span>
    
7. <span data-ttu-id="c5020-184">В диалоговом окне **для предоставления общего доступа к элементу** введите имя группы доступа для участников сайта, выберите ее и нажмите **Поделиться**.</span><span class="sxs-lookup"><span data-stu-id="c5020-184">In the **Share** dialog box, type the name of the site members access group, select it, and then click **Share**.</span></span>
    
8. <span data-ttu-id="c5020-185">Нажмите кнопку "Назад" в браузере.</span><span class="sxs-lookup"><span data-stu-id="c5020-185">Click the back button on your browser.</span></span>
    
9. <span data-ttu-id="c5020-186">Выберите в списке \*\* \<наме_гт_ Owners (владельцы сайта\*\* ).</span><span class="sxs-lookup"><span data-stu-id="c5020-186">Click **\<site name> Owners** in the list.</span></span>
    
10. <span data-ttu-id="c5020-187">В разделе **Пользователи и группы** нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="c5020-187">In **People and Groups**, click **New**.</span></span>
    
11. <span data-ttu-id="c5020-188">В диалоговом окне **для предоставления общего доступа к элементу** введите имя группы доступа для администраторов сайта, выберите ее и нажмите **Поделиться**.</span><span class="sxs-lookup"><span data-stu-id="c5020-188">In the **Share** dialog box, type the name of the site admins access group, select it, and then click **Share**.</span></span>
    
12. <span data-ttu-id="c5020-189">Нажмите кнопку "Назад" в браузере.</span><span class="sxs-lookup"><span data-stu-id="c5020-189">Click the back button on your browser.</span></span>
    
13. <span data-ttu-id="c5020-190">Щелкните \*\* \<сайт наме_гт_ посетителей\*\* в списке.</span><span class="sxs-lookup"><span data-stu-id="c5020-190">Click **\<site name> Visitors** in the list.</span></span>
    
14. <span data-ttu-id="c5020-191">В разделе **Пользователи и группы** нажмите **Создание**.</span><span class="sxs-lookup"><span data-stu-id="c5020-191">In **People and Groups**, click **New**.</span></span>
    
15. <span data-ttu-id="c5020-192">В диалоговом окне **для предоставления общего доступа к элементу** введите имя группы доступа для читателей сайта, выберите ее и нажмите **Поделиться**.</span><span class="sxs-lookup"><span data-stu-id="c5020-192">In the **Share** dialog box, type the name of the site viewers access group, select it, and then click **Share**.</span></span>
    
16. <span data-ttu-id="c5020-193">Закройте вкладку браузера **Разрешения**.</span><span class="sxs-lookup"><span data-stu-id="c5020-193">Close the **Permissions** tab of your browser.</span></span>
    
<span data-ttu-id="c5020-194">Ознакомьтесь с результатами настройки разрешений.</span><span class="sxs-lookup"><span data-stu-id="c5020-194">The results of these permission settings are:</span></span>
  
- <span data-ttu-id="c5020-195">Группа SharePoint \*\* \<site наме_гт_ Owners\*\* содержит группу доступа "Администраторы сайта", в которой все участники имеют уровень разрешений " **полный** доступ".</span><span class="sxs-lookup"><span data-stu-id="c5020-195">The **\<site name> Owners** SharePoint group contains the site admins access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="c5020-196">Группа SharePoint \*\* \<site наме_гт_ Members\*\* содержит группу доступа "Участники сайта", в которой все участники имеют уровень разрешений " **изменить** ".</span><span class="sxs-lookup"><span data-stu-id="c5020-196">The **\<site name> Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="c5020-197">Группа SharePoint \*\* \<site наме_гт_ Sites\*\* содержит группу доступа посетителей сайта, в которой все участники имеют уровень разрешений **Чтение** .</span><span class="sxs-lookup"><span data-stu-id="c5020-197">The **\<site name> Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="c5020-198">Участники не могут приглашать других участников, равно как и запрашивать доступ для лиц, не являющихся участниками.</span><span class="sxs-lookup"><span data-stu-id="c5020-198">The ability for members to invite other members or for non-members to request access is disabled.</span></span>
    
<span data-ttu-id="c5020-199">Ниже показана итоговая конфигурация с тремя группами SharePoint для сайта, на котором настроено использование трех групп доступа, заполненных учетными записями пользователей или группами Azure AD.</span><span class="sxs-lookup"><span data-stu-id="c5020-199">Here is your resulting configuration with the three SharePoint groups for the site configured to use the three access groups, which are populated with user accounts or Azure AD groups.</span></span>
  
![Последняя конфигурация изолированного сайта SharePoint Online с группами доступа и учетными записями пользователей.](media/e7618971-06ab-447b-90ff-d8be3790fe63.png)
  
<span data-ttu-id="c5020-201">Теперь вы и участники сайта можете совместно работать с его материалами посредством участия в одной из групп доступа.</span><span class="sxs-lookup"><span data-stu-id="c5020-201">You and the members of the site, through group membership in one of the access groups, can now collaborate using the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="c5020-202">Следующий этап</span><span class="sxs-lookup"><span data-stu-id="c5020-202">Next step</span></span>

<span data-ttu-id="c5020-203">Если вам нужно изменить состав группы доступа к сайту или создать папку документов с особыми разрешениями, см. статью [Manage an isolated SharePoint Online team site](manage-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="c5020-203">When you need to change site access group membership or create a document folder with custom permissions, see [Manage an isolated SharePoint Online team site](manage-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5020-204">См. также</span><span class="sxs-lookup"><span data-stu-id="c5020-204">See Also</span></span>

[<span data-ttu-id="c5020-205">Изолированные сайты групп SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c5020-205">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="c5020-206">Разработка изолированного сайта группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c5020-206">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)
  
[<span data-ttu-id="c5020-207">Управление изолированным сайтом группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c5020-207">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)
  



