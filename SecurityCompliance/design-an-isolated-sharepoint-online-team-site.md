---
title: Разработка изолированного сайта группы SharePoint Online
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Ent_O365
ms.custom: Ent_Solutions
ms.assetid: 775a4e9e-3135-4a48-b32f-bbdd9f2bd0aa
description: Сводка. Пошаговое руководство по разработке изолированных сайтов групп SharePoint Online.
ms.openlocfilehash: 19f030f5210fb6742098543ae91117a90d583242
ms.sourcegitcommit: 6122eb026c558a5126c40845e656fbb0c40cb32a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2019
ms.locfileid: "36053126"
---
# <a name="design-an-isolated-sharepoint-online-team-site"></a><span data-ttu-id="e38ed-103">Разработка изолированного сайта группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="e38ed-103">Design an isolated SharePoint Online team site</span></span>

 <span data-ttu-id="e38ed-104">**Сводка.** Пошаговое руководство по разработке изолированных сайтов групп SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="e38ed-104">**Summary:** Step through the design process for isolated SharePoint Online team sites.</span></span>
  
<span data-ttu-id="e38ed-105">В этой статье описаны основные проектные решения, которые необходимо принять перед созданием изолированного сайта группы SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="e38ed-105">This article takes you through the key design decisions you must make before creating an isolated SharePoint Online team site.</span></span>
  
## <a name="phase-1-determine-your-sharepoint-groups-and-permission-levels"></a><span data-ttu-id="e38ed-106">Этап 1. Определение групп SharePoint и уровней разрешений</span><span class="sxs-lookup"><span data-stu-id="e38ed-106">Phase 1: Determine your SharePoint groups and permission levels</span></span>

<span data-ttu-id="e38ed-107">Каждый сайт группы SharePoint Online по умолчанию создается со следующими группами SharePoint:</span><span class="sxs-lookup"><span data-stu-id="e38ed-107">Every SharePoint Online team site by default is created with the following SharePoint groups:</span></span>
  
- <span data-ttu-id="e38ed-108">\<имя сайта> элементы</span><span class="sxs-lookup"><span data-stu-id="e38ed-108">\<site name> Members</span></span>
    
- <span data-ttu-id="e38ed-109">\<имя сайта> посетителей</span><span class="sxs-lookup"><span data-stu-id="e38ed-109">\<site name> Visitors</span></span>
    
- <span data-ttu-id="e38ed-110">\<Владельцы> имен сайтов</span><span class="sxs-lookup"><span data-stu-id="e38ed-110">\<site name> Owners</span></span>
    
<span data-ttu-id="e38ed-111">Эти группы не связаны с группами Office 365 и Azure Active Directory (AD) и позволяют назначать разрешения для ресурсов сайта.</span><span class="sxs-lookup"><span data-stu-id="e38ed-111">These groups are separate from Office 365 and Azure Active Directory (AD) groups and are the basis for assigning permissions for the resources of the site.</span></span>
  
<span data-ttu-id="e38ed-p101">Набор разрешений, определяющий возможности члена группы SharePoint на сайте, — это уровень разрешений. По умолчанию для сайта группы SharePoint Online доступно три уровня разрешений: "Изменение", "Чтение" и "Полный доступ". В приведенной ниже таблице показаны группы SharePoint и назначенные им по умолчанию уровни разрешений.</span><span class="sxs-lookup"><span data-stu-id="e38ed-p101">The set of specific permissions that determines what a member of a SharePoint group can do in a site is a permission level. There are three permission levels by default for a SharePoint Online team site: Edit, Read, and Full control. The following table shows the default correlation of SharePoint groups and assigned permission levels:</span></span>
  
|<span data-ttu-id="e38ed-115">**Группа SharePoint**</span><span class="sxs-lookup"><span data-stu-id="e38ed-115">**SharePoint group**</span></span>|<span data-ttu-id="e38ed-116">**Уровень разрешений**</span><span class="sxs-lookup"><span data-stu-id="e38ed-116">**Permission level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e38ed-117">\<имя сайта> элементы</span><span class="sxs-lookup"><span data-stu-id="e38ed-117">\<site name> Members</span></span>  <br/> |<span data-ttu-id="e38ed-118">Edit</span><span class="sxs-lookup"><span data-stu-id="e38ed-118">Edit</span></span>  <br/> |
|<span data-ttu-id="e38ed-119">\<имя сайта> посетителей</span><span class="sxs-lookup"><span data-stu-id="e38ed-119">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="e38ed-120">Чтение</span><span class="sxs-lookup"><span data-stu-id="e38ed-120">Read</span></span>  <br/> |
|<span data-ttu-id="e38ed-121">\<Владельцы> имен сайтов</span><span class="sxs-lookup"><span data-stu-id="e38ed-121">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="e38ed-122">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="e38ed-122">Full control</span></span>  <br/> |
   
 <span data-ttu-id="e38ed-p102">**Рекомендация.** Вы можете создавать дополнительные группы SharePoint и уровни разрешений. Но мы рекомендуем использовать заданные по умолчанию группы SharePoint и уровни разрешений для изолированного сайта SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="e38ed-p102">**Best practice:** You can create additional SharePoint groups and permission levels. However, we recommend using the default SharePoint groups and permission levels for your isolated SharePoint Online site.</span></span>
  
<span data-ttu-id="e38ed-125">Ниже указаны группы SharePoint по умолчанию и уровни разрешений.</span><span class="sxs-lookup"><span data-stu-id="e38ed-125">Here are the default SharePoint groups and permission levels.</span></span>
  
![Группы SharePoint по умолчанию и уровни разрешений для сайта SharePoint Online.](media/3f892ab4-6479-42f0-a505-1ba0ef94b9c6.png)
  
## <a name="phase-2-assign-permissions-to-users-with-access-groups"></a><span data-ttu-id="e38ed-127">Этап 2. Назначение разрешений пользователям с помощью групп доступа</span><span class="sxs-lookup"><span data-stu-id="e38ed-127">Phase 2: Assign permissions to users with access groups</span></span>

<span data-ttu-id="e38ed-p103">Вы можете назначить разрешения пользователям, добавив либо их учетные записи, либо группы Office 365 или Azure AD, в которых они состоят, в группы SharePoint. После добавления учетным записям пользователей Office 365 назначается уровень разрешений, связанный с группой SharePoint. Это происходит либо непосредственно, либо благодаря членству в группе Office 365 или Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e38ed-p103">You can assign permissions to users by adding their user account, or an Office 365 or Azure AD group of which the user account is a member, to the SharePoint groups. Once added, the Office 365 user accounts, either directly or indirectly via membership in an Office 365 or Azure AD group, are assigned the permission level associated with the SharePoint group.</span></span>
  
<span data-ttu-id="e38ed-130">Предоставление разрешений на примере групп SharePoint по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="e38ed-130">Using the default SharePoint groups as an example:</span></span>
  
- <span data-ttu-id="e38ed-131">Членам группы " \*\* \<имя сайта> участников\*\* SharePoint", которая может включать как учетные записи пользователей, так и группы, назначается уровень разрешений " **изменить** ".</span><span class="sxs-lookup"><span data-stu-id="e38ed-131">Members of the **\<site name> Members** SharePoint group, which can include both user accounts and groups, are assigned the **Edit** permission level</span></span>
    
- <span data-ttu-id="e38ed-132">Членам группы " \*\* \<имя сайта>\*\* SharePoint", которая может включать как учетные записи пользователей, так и группы, назначается уровень разрешений " **Чтение** ".</span><span class="sxs-lookup"><span data-stu-id="e38ed-132">Members of the **\<site name> Visitors** SharePoint group, which can include both user accounts and groups, are assigned the **Read** permission level</span></span>
    
- <span data-ttu-id="e38ed-133">Членам группы SharePoint " \*\* \<имя сайта> владельцы\*\* ", которая может включать как учетные записи пользователей, так и группы, назначается уровень разрешений " **полный** доступ".</span><span class="sxs-lookup"><span data-stu-id="e38ed-133">Members of the **\<site name> Owners** SharePoint group, which can include both user accounts and groups, are assigned the **Full control** permission level</span></span>
    
 <span data-ttu-id="e38ed-p104">**Рекомендация.** Вы можете управлять разрешениями через отдельные учетные записи пользователей, но рекомендуем использовать для этого одну группу Azure AD (т. н. группу доступа). Это позволяет управлять разрешениями через членство в группе доступа, не управляя списком учетных записей для каждой группы SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e38ed-p104">**Best practice:** Although you can manage permissions through individual user accounts, we recommend that you use a single Azure AD group, known as an access group, instead. This simplifies the management of permissions through membership in the access group, rather than managing the list of user accounts for each SharePoint group.</span></span>
  
<span data-ttu-id="e38ed-136">Группы Azure AD для Office 365 отличаются от групп Office 365.</span><span class="sxs-lookup"><span data-stu-id="e38ed-136">Azure AD groups for Office 365 are different than Office 365 groups.</span></span> <span data-ttu-id="e38ed-137">Группы Azure AD отображаются в центре администрирования Microsoft 365 с **типом** " **Безопасность** " и не имеют адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="e38ed-137">Azure AD groups appear in the Microsoft 365 admin center with their **Type** set to **Security** and do not have an email address.</span></span> <span data-ttu-id="e38ed-138">Группами Azure AD можно управлять с помощью указанных ниже средств.</span><span class="sxs-lookup"><span data-stu-id="e38ed-138">Azure AD groups can be managed within:</span></span>
  
- <span data-ttu-id="e38ed-139">Доменные службы Active Directory</span><span class="sxs-lookup"><span data-stu-id="e38ed-139">Active Directory Domain Services (AD DS)</span></span>
    
    <span data-ttu-id="e38ed-140">Это группы, созданные в локальной инфраструктуре AD DS и синхронизированные с подпиской на Office 365.</span><span class="sxs-lookup"><span data-stu-id="e38ed-140">These are groups that have been created in your on-premises AD DS infrastructure and synchronized to your Office 365 subscription.</span></span> <span data-ttu-id="e38ed-141">В центре администрирования Microsoft 365 для этих групп задано **состояние** " **синхронизирован" с Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e38ed-141">In the Microsoft 365 admin center, these groups have a **Status** of **Synched with active directory**.</span></span>
    
- <span data-ttu-id="e38ed-142">Office 365</span><span class="sxs-lookup"><span data-stu-id="e38ed-142">Office 365</span></span>
    
    <span data-ttu-id="e38ed-143">Это группы, созданные с помощью центра администрирования Microsoft 365, портала Azure или Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e38ed-143">These are groups that have been created using either the Microsoft 365 admin center, the Azure portal, or Microsoft PowerShell.</span></span> <span data-ttu-id="e38ed-144">В центре администрирования Microsoft 365 для этих групп задано **состояние** **Cloud**.</span><span class="sxs-lookup"><span data-stu-id="e38ed-144">In the Microsoft 365 admin center, these groups have a **Status** of **Cloud**.</span></span>
    
 <span data-ttu-id="e38ed-145">**Рекомендация:** Если вы используете локальную службу доменных служб Active Directory и выполняете синхронизацию с вашей подпиской на Office 365, выполните Управление пользователями и группами с помощью AD DS.</span><span class="sxs-lookup"><span data-stu-id="e38ed-145">**Best practice:** If you are using AD DS on-premises and synchronizing with your Office 365 subscription, perform your user and group management with AD DS.</span></span>
  
<span data-ttu-id="e38ed-146">Рекомендуемая структура изолированных сайтов групп SharePoint Online указана ниже.</span><span class="sxs-lookup"><span data-stu-id="e38ed-146">For isolated SharePoint Online team sites, the recommended group structure looks like this:</span></span>
  
|<span data-ttu-id="e38ed-147">**Группа SharePoint**</span><span class="sxs-lookup"><span data-stu-id="e38ed-147">**SharePoint group**</span></span>|<span data-ttu-id="e38ed-148">**Группа доступа на основе Azure AD**</span><span class="sxs-lookup"><span data-stu-id="e38ed-148">**Azure AD-based access group**</span></span>|<span data-ttu-id="e38ed-149">**Уровень разрешений**</span><span class="sxs-lookup"><span data-stu-id="e38ed-149">**Permission level**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e38ed-150">\<имя сайта> элементы</span><span class="sxs-lookup"><span data-stu-id="e38ed-150">\<site name> Members</span></span>  <br/> |<span data-ttu-id="e38ed-151">\<имя сайта> элементы</span><span class="sxs-lookup"><span data-stu-id="e38ed-151">\<site name> Members</span></span>  <br/> |<span data-ttu-id="e38ed-152">Edit</span><span class="sxs-lookup"><span data-stu-id="e38ed-152">Edit</span></span>  <br/> |
|<span data-ttu-id="e38ed-153">\<имя сайта> посетителей</span><span class="sxs-lookup"><span data-stu-id="e38ed-153">\<site name> Visitors</span></span>  <br/> |<span data-ttu-id="e38ed-154">\<имя сайта> средства просмотра</span><span class="sxs-lookup"><span data-stu-id="e38ed-154">\<site name> Viewers</span></span>  <br/> |<span data-ttu-id="e38ed-155">Чтение</span><span class="sxs-lookup"><span data-stu-id="e38ed-155">Read</span></span>  <br/> |
|<span data-ttu-id="e38ed-156">\<Владельцы> имен сайтов</span><span class="sxs-lookup"><span data-stu-id="e38ed-156">\<site name> Owners</span></span>  <br/> |<span data-ttu-id="e38ed-157">\<имя сайта> администраторов</span><span class="sxs-lookup"><span data-stu-id="e38ed-157">\<site name> Admins</span></span>  <br/> |<span data-ttu-id="e38ed-158">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="e38ed-158">Full control</span></span>  <br/> |
   
 <span data-ttu-id="e38ed-159">**Рекомендация:** Несмотря на то что вы можете использовать группы Office 365 или Azure AD в качестве членов групп SharePoint, мы рекомендуем использовать группы Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e38ed-159">**Best practice:** Although you can use either Office 365 or Azure AD groups as members of SharePoint groups, we recommend that you use Azure AD groups.</span></span> <span data-ttu-id="e38ed-160">Группы Azure AD, управляемые с помощью AD DS или Office 365, предоставляют более гибкие возможности для назначения разрешений с помощью вложенных групп.</span><span class="sxs-lookup"><span data-stu-id="e38ed-160">Azure AD groups, managed either through AD DS or Office 365, give you more flexibility to use nested groups to assign permissions.</span></span>
  
<span data-ttu-id="e38ed-161">Ниже приведены группы SharePoint по умолчанию, настроенные для использования групп доступа на основе Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e38ed-161">Here are the default SharePoint groups configured to use Azure AD-based access groups.</span></span>
  
![Использование групп доступа в качестве членов групп сайтов SharePoint Online по умолчанию.](media/50a76328-ae69-483e-9029-ac4e7357b5ef.png)
  
<span data-ttu-id="e38ed-163">При создании трех групп доступа учитывайте следующее:</span><span class="sxs-lookup"><span data-stu-id="e38ed-163">When designing the three access groups, keep the following in mind:</span></span>
  
- <span data-ttu-id="e38ed-164">В группе \*\* \<"имя сайта> группы доступа" Администраторы "\*\* должно быть только несколько членов, соответствующих небольшому числу администраторов SharePoint Online, которые управляют сайтом группы.</span><span class="sxs-lookup"><span data-stu-id="e38ed-164">There should be only a few members in the **\<site name> Admins** access group, corresponding to a small number of SharePoint Online administrators who are managing the team site.</span></span>
    
- <span data-ttu-id="e38ed-165">Большинство участников сайта находятся в \*\* \<имени сайта> элементы\*\* или \*\* \<имя сайта>\*\* группы доступа к читателям.</span><span class="sxs-lookup"><span data-stu-id="e38ed-165">Most of your site members are in the **\<site name> Members** or **\<site name> Viewers** access groups.</span></span> <span data-ttu-id="e38ed-166">Так как члены сайта в группе доступа к \*\* \<имени сайта> участников\*\* имеют возможность удалять или изменять ресурсы на сайте, тщательно изучите их участников.</span><span class="sxs-lookup"><span data-stu-id="e38ed-166">Because site members in the **\<site name> Members** access group have the ability to delete or modify resources in the site, carefully consider its membership.</span></span> <span data-ttu-id="e38ed-167">При возникновении сомнений добавьте участника сайта в группу " \*\* \<имя сайта>\*\* доступ к зрителям".</span><span class="sxs-lookup"><span data-stu-id="e38ed-167">When in doubt, add the site member to the **\<site name> Viewers** access group.</span></span>
    
<span data-ttu-id="e38ed-168">Ниже приведен пример групп SharePoint и групп доступа для изолированного сайта с именем ProjectX.</span><span class="sxs-lookup"><span data-stu-id="e38ed-168">Here is an example of the SharePoint groups and access groups for an isolated site named ProjectX.</span></span>
  
![Пример использования групп доступа для сайта SharePoint Online с именем ProjectX.](media/13afe542-9ffd-4671-9f48-210a0e2a502a.png)
  
## <a name="phase-3-use-nested-azure-ad-groups"></a><span data-ttu-id="e38ed-170">Этап 3: использование вложенных групп Azure AD</span><span class="sxs-lookup"><span data-stu-id="e38ed-170">Phase 3: Use nested Azure AD groups</span></span>

<span data-ttu-id="e38ed-171">Если в проекте немного людей, один уровень групп доступа на основе Azure AD, добавленных в группы SharePoint сайта, подойдет для большинства сценариев.</span><span class="sxs-lookup"><span data-stu-id="e38ed-171">For a project confined to a small number of people, a single level of Azure AD-based access groups added to the SharePoint groups of the site will fit most scenarios.</span></span> <span data-ttu-id="e38ed-172">Тем не менее, если у вас большое количество людей, и эти пользователи уже являются участниками группы Azure AD, вы можете легко назначить разрешения SharePoint с помощью вложенных групп или групп, которые содержат другие группы в качестве участников.</span><span class="sxs-lookup"><span data-stu-id="e38ed-172">However, if you have a large number of people and those people are already members of established Azure AD groups, you can more easily assign SharePoint permissions by using nested groups, or groups that contain other groups as members.</span></span>
  
<span data-ttu-id="e38ed-p111">Например, вы хотите создать изолированный сайт группы SharePoint Online для совместной работы руководителей отделов продаж, маркетинга, поддержки, а также инженерно-технического и юридического отделов, и у этих отделов уже есть группы руководителей. Вместо того чтобы создавать группу для новых участников сайта и добавлять в нее все учетные записи руководителей, добавьте существующие группы руководителей каждого отдела в новую группу.</span><span class="sxs-lookup"><span data-stu-id="e38ed-p111">For example, you want to create an isolated SharePoint online team site for collaboration among the executives of the sales, marketing, engineering, legal, and support departments and those departments already their own groups with executive user account membership. Rather than creating a new group for the new site members and placing all the individual executive user accounts in it, put the existing executive groups for each department in the new group.</span></span>
  
 <span data-ttu-id="e38ed-p112"> Если у вас одна подписка на Office 365 на несколько организаций, одним уровнем членства в группе для изолированного сайта может быть трудно управлять из-за большого количества учетных записей пользователей. В этом случае можно использовать вложенные группы Azure AD для каждой организации, которые содержат группы в своей организации для управления разрешениями.</span><span class="sxs-lookup"><span data-stu-id="e38ed-p112">If you are sharing an Office 365 subscription between multiple organizations, a single level of group membership for an isolated site for an organization might become difficult to manage due to the sheer number of user accounts. In this case, you can use nested Azure AD groups for each organization that contain the groups within their organizations to manage the permissions.</span></span>
  
<span data-ttu-id="e38ed-177">Чтобы использовать вложенные группы Azure AD:</span><span class="sxs-lookup"><span data-stu-id="e38ed-177">To use nested Azure AD groups:</span></span>
  
1. <span data-ttu-id="e38ed-178">Определите или создайте группы Azure AD, которые будут содержать учетные записи пользователей, и добавьте соответствующие учетные записи пользователей в качестве членов.</span><span class="sxs-lookup"><span data-stu-id="e38ed-178">Identify or create the Azure AD groups that will contain user accounts and add the appropriate user accounts as members.</span></span>
    
2. <span data-ttu-id="e38ed-179">Создайте общую группу доступа на основе Azure AD, которая будет содержать другие группы Azure AD, и добавьте эти группы в качестве членов.</span><span class="sxs-lookup"><span data-stu-id="e38ed-179">Create the container Azure AD-based access group that will contain the other Azure AD groups and add those groups as members.</span></span>
    
3.  <span data-ttu-id="e38ed-180"> Чтобы предоставить общей группе доступа нужный уровень доступа, укажите группу SharePoint и соответствующий уровень разрешений.</span><span class="sxs-lookup"><span data-stu-id="e38ed-180">For the appropriate level of access for the container access group, identify the SharePoint group and corresponding permission level.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e38ed-181">Вложенные группы Office 365 не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e38ed-181">You cannot use nested Office 365 groups.</span></span> 
  
<span data-ttu-id="e38ed-182">Ниже приведен пример вложенных групп Azure AD для группы доступа к членам ProjectX.</span><span class="sxs-lookup"><span data-stu-id="e38ed-182">Here is an example of nested Azure AD groups for the ProjectX member access group.</span></span>
  
![Пример использования вложенных групп доступа для группы доступа "участники" на сайте ProjectX.](media/2abca710-bf9e-4ce8-9bcd-a8e128264fb1.png)
  
<span data-ttu-id="e38ed-184">Так как все учетные записи пользователей в группах "исследование", "Проектирование" и "руководители проектов" предназначены для участников сайта, проще добавить свои группы Azure AD в группу доступа к участникам ProjectX.</span><span class="sxs-lookup"><span data-stu-id="e38ed-184">Because all of the user accounts in the Research, Engineering, and Project leads teams are intended to be site members, it is easier to add their Azure AD groups to the ProjectX Members access group.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="e38ed-185">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="e38ed-185">Next step</span></span>

<span data-ttu-id="e38ed-186">Сведения о создании и настройке изолированного сайта в рабочей среде см. в статье [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="e38ed-186">When you are ready to create and configure an isolated site in production, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e38ed-187">См. также</span><span class="sxs-lookup"><span data-stu-id="e38ed-187">See Also</span></span>

[<span data-ttu-id="e38ed-188">Изолированные сайты групп SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="e38ed-188">Isolated SharePoint Online team sites</span></span>](isolated-sharepoint-online-team-sites.md)
  
[<span data-ttu-id="e38ed-189">Управление изолированным сайтом группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="e38ed-189">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="e38ed-190">Развертывание изолированного сайта группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="e38ed-190">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)



