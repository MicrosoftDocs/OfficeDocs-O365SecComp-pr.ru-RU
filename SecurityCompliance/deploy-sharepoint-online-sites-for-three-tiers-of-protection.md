---
title: Развертывание сайтов SharePoint Online с тремя уровнями защиты
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/29/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 1e8e3cfd-b878-4088-b941-9940363a5fae
description: Сводка. Сведения о создании и настройке сайтов группы в SharePoint Online для применения различных уровней защиты информации.
ms.openlocfilehash: 77bf7b67d4ec1b93e5a470e69a014ee608a1465a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153381"
---
# <a name="deploy-sharepoint-online-sites-for-three-tiers-of-protection"></a><span data-ttu-id="ba572-103">Развертывание сайтов SharePoint Online с тремя уровнями защиты</span><span class="sxs-lookup"><span data-stu-id="ba572-103">Deploy SharePoint Online sites for three tiers of protection</span></span>

 <span data-ttu-id="ba572-104">**Сводка.** Сведения о создании и настройке сайтов группы в SharePoint Online для применения различных уровней защиты информации.</span><span class="sxs-lookup"><span data-stu-id="ba572-104">**Summary:** Create and configure SharePoint Online team sites for various levels of information protection.</span></span>
  
<span data-ttu-id="ba572-p101">В этой статье приводятся инструкции по разработке и развертыванию сайтов групп SharePoint Online с базовым, конфиденциальным и строго конфиденциальным уровнями защиты. Дополнительные сведения об этих трех уровнях защиты см. в статье [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md) (Защита сайтов и файлов SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="ba572-p101">Use the steps in this article to design and deploy baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="baseline-sharepoint-online-team-sites"></a><span data-ttu-id="ba572-107">Сайты групп SharePoint Online с базовым уровнем защиты</span><span class="sxs-lookup"><span data-stu-id="ba572-107">Baseline SharePoint Online team sites</span></span>

<span data-ttu-id="ba572-p102">Базовый уровень защиты распространяется на частные и общедоступные сайты групп. Обнаруживать общедоступные сайты групп и получать к ним доступ может любой пользователь в организации. Обнаруживать частные сайты и получать к ним доступ могут только участники группы Office 365, связанной с сайтом группы. Оба этих типа сайтов групп позволяют участникам предоставлять доступ к сайту другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="ba572-p102">Baseline protection includes both public and private team sites. Public team sites can be discovered and accessed by anybody in the organization. Private sites can only be discovered and accessed by members of the Office 365 group associated with the team site. Both of these types of team sites allow members to share the site with others.</span></span>
  
### <a name="public"></a><span data-ttu-id="ba572-112">Общедоступные</span><span class="sxs-lookup"><span data-stu-id="ba572-112">Public</span></span>

<span data-ttu-id="ba572-113">Чтобы создать сайт группы SharePoint Online с базовым уровнем защиты и общим доступом и разрешениями, выполните приведенные далее действия.</span><span class="sxs-lookup"><span data-stu-id="ba572-113">To create a baseline SharePoint Online team site with public access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="ba572-114">Войдите в Центр администрирования с помощью учетной записи, которая также используется для администрирования сайта группы SharePoint Online (учетной записи администратора SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="ba572-114">Sign in to the admin center with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="ba572-115">Дополнительные сведения см. в статье [Вход в Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="ba572-115">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="ba572-116">В списке плиток выберите **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="ba572-116">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="ba572-117">На новой вкладке **SharePoint** в браузере щелкните **+ Создать сайт**.</span><span class="sxs-lookup"><span data-stu-id="ba572-117">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="ba572-118">На странице **Создание сайта** щелкните **Сайт группы**.</span><span class="sxs-lookup"><span data-stu-id="ba572-118">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="ba572-119">В поле **Имя сайта** введите имя для открытого сайта группы.</span><span class="sxs-lookup"><span data-stu-id="ba572-119">In **Site name**, type a name for the public team site.</span></span> 
    
6. <span data-ttu-id="ba572-120">В поле **Описание сайта группы** введите описание назначения сайта.</span><span class="sxs-lookup"><span data-stu-id="ba572-120">In **Team site description**, type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="ba572-121">В разделе **Параметры конфиденциальности** выберите **Общедоступная группа: все в организации имеют доступ к этому сайту** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba572-121">In **Privacy settings**, select **Public - anyone in the organization can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="ba572-122">В области **Кого вы хотите добавить?** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="ba572-122">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="ba572-123">Ниже показана полученная в итоге конфигурация.</span><span class="sxs-lookup"><span data-stu-id="ba572-123">Here is your resulting configuration.</span></span>
  
![Базовый уровень защиты для общедоступного сайта группы SharePoint Online.](media/bcd46b8d-3f89-4398-80ce-4da17ee85e03.png)
  
### <a name="private"></a><span data-ttu-id="ba572-125">Частный</span><span class="sxs-lookup"><span data-stu-id="ba572-125">Private</span></span>

<span data-ttu-id="ba572-126">Чтобы создать сайт группы SharePoint Online с базовым уровнем защиты, закрытым доступом и разрешениями, выполните приведенные далее действия.</span><span class="sxs-lookup"><span data-stu-id="ba572-126">To create a baseline SharePoint Online team site with private access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="ba572-127">Войдите в Центр администрирования с помощью учетной записи, которая также используется для администрирования сайта группы SharePoint Online (учетной записи администратора SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="ba572-127">Sign in to the admin center with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="ba572-128">Дополнительные сведения см. в статье [Вход в Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="ba572-128">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="ba572-129">В списке плиток выберите **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="ba572-129">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="ba572-130">На новой вкладке **SharePoint** в браузере щелкните **+ Создать сайт**.</span><span class="sxs-lookup"><span data-stu-id="ba572-130">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="ba572-131">На странице **Создание сайта** щелкните **Сайт группы**.</span><span class="sxs-lookup"><span data-stu-id="ba572-131">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="ba572-132">В поле **Имя сайта** введите имя для частного сайта группы.</span><span class="sxs-lookup"><span data-stu-id="ba572-132">In **Site name**, type a name for the private team site.</span></span> 
    
6. <span data-ttu-id="ba572-133">В поле **Описание сайта группы** введите описание назначения сайта.</span><span class="sxs-lookup"><span data-stu-id="ba572-133">In **Team site description,** type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="ba572-134">В разделе **Параметры конфиденциальности** выберите **Закрытая группа: только участники имеют доступ к этому сайту** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba572-134">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="ba572-135">В области **Who do you want to add?** (Кого нужно добавить?) в поле **Добавить участников** введите имена учетных записей пользователей, имеющих доступ к этому частному сайту группы.</span><span class="sxs-lookup"><span data-stu-id="ba572-135">On the **Who do you want to add?** pane, in **Add members**, type the names of user accounts that have access to this private team site.</span></span>
    
9. <span data-ttu-id="ba572-136">Добавив начальный набор участников сайта, нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="ba572-136">When you are done adding the initial set of members to the site, click **Finish**</span></span>
    
<span data-ttu-id="ba572-137">Ниже показана полученная в итоге конфигурация.</span><span class="sxs-lookup"><span data-stu-id="ba572-137">Here is your resulting configuration.</span></span>
  
![Базовый уровень защиты для частного сайта группы SharePoint Online.](media/91769026-37e3-4383-ac3c-dbf7aca98e41.png)
  
## <a name="sensitive-sharepoint-online-team-sites"></a><span data-ttu-id="ba572-139">Конфиденциальные сайты группы SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ba572-139">Sensitive SharePoint Online team sites</span></span>

<span data-ttu-id="ba572-140">Конфиденциальный сайт группы SharePoint Online — это изолированный сайт группы, разрешения на доступ к которому определяются членством в группах SharePoint, а не в группе Office 365, связанной с этим сайтом группы.</span><span class="sxs-lookup"><span data-stu-id="ba572-140">A sensitive SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="ba572-141">Есть два основных этапа создания изолированного сайта группы.</span><span class="sxs-lookup"><span data-stu-id="ba572-141">To create an isolated team site, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="ba572-142">Шаг 1. Разработка изолированного сайта</span><span class="sxs-lookup"><span data-stu-id="ba572-142">Step 1: Design your isolated site</span></span>

<span data-ttu-id="ba572-143">Чтобы разработать изолированный сайт группы, необходимо определить:</span><span class="sxs-lookup"><span data-stu-id="ba572-143">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="ba572-144">Группы SharePoint и уровни разрешений.</span><span class="sxs-lookup"><span data-stu-id="ba572-144">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="ba572-145">Набор групп доступа, которые будут участниками групп SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ba572-145">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="ba572-146">Рекомендуется следующий набор групп доступа: один для участников сайта, один для посетителей сайта и один для администраторов сайта.</span><span class="sxs-lookup"><span data-stu-id="ba572-146">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="ba572-147">Будут ли использоваться вложенные группы внутри групп доступа.</span><span class="sxs-lookup"><span data-stu-id="ba572-147">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="ba572-148">Например, рекомендуемая структура групп и уровни разрешений выглядят следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ba572-148">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="ba572-149">**Группа SharePoint**</span><span class="sxs-lookup"><span data-stu-id="ba572-149">**SharePoint group**</span></span>|<span data-ttu-id="ba572-150">**Уровень разрешений**</span><span class="sxs-lookup"><span data-stu-id="ba572-150">**Permission level**</span></span>|<span data-ttu-id="ba572-151">**Группа доступа (примеры)**</span><span class="sxs-lookup"><span data-stu-id="ba572-151">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba572-152">[имя сайта] — участники</span><span class="sxs-lookup"><span data-stu-id="ba572-152">[site name] Members</span></span>  <br/> |<span data-ttu-id="ba572-153">Правка</span><span class="sxs-lookup"><span data-stu-id="ba572-153">Edit</span></span>  <br/> |<span data-ttu-id="ba572-154">[имя сайта] — участники</span><span class="sxs-lookup"><span data-stu-id="ba572-154">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="ba572-155">[имя сайта] — посетители</span><span class="sxs-lookup"><span data-stu-id="ba572-155">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="ba572-156">Чтение</span><span class="sxs-lookup"><span data-stu-id="ba572-156">Read</span></span>  <br/> |<span data-ttu-id="ba572-157">[имя сайта] — посетители</span><span class="sxs-lookup"><span data-stu-id="ba572-157">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="ba572-158">[имя сайта] — владельцы</span><span class="sxs-lookup"><span data-stu-id="ba572-158">[site name] Owners</span></span>  <br/> |<span data-ttu-id="ba572-159">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="ba572-159">Full control</span></span>  <br/> |<span data-ttu-id="ba572-160">[имя сайта] — администраторы</span><span class="sxs-lookup"><span data-stu-id="ba572-160">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="ba572-p105">Группы и уровни разрешений SharePoint создаются по умолчанию для сайта группы. Необходимо определить имена групп доступа.</span><span class="sxs-lookup"><span data-stu-id="ba572-p105">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="ba572-163">Сведения о процессе разработки см. в статье [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md) (Разработка изолированного сайта группы SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="ba572-163">For the details of the design process, see [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="ba572-164">Шаг 2. Развертывание изолированного сайта</span><span class="sxs-lookup"><span data-stu-id="ba572-164">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="ba572-165">Для развертывания изолированного сайта сначала необходимо:</span><span class="sxs-lookup"><span data-stu-id="ba572-165">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="ba572-166">определить учетные записи пользователей и группы пользователей для добавления в каждую группу доступа;</span><span class="sxs-lookup"><span data-stu-id="ba572-166">Determine the user accounts and groups to add to each of your access groups.</span></span>
    
- <span data-ttu-id="ba572-167">создать группы доступа и добавить пользователей и членов групп.</span><span class="sxs-lookup"><span data-stu-id="ba572-167">Create the access groups and add the user and group members.</span></span>
    
<span data-ttu-id="ba572-168">Подробные инструкции см. в разделе **Этап 1** статьи [Развертывание изолированного сайта группы в SharePoint Online](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="ba572-168">For the detailed steps, see **Phase 1** of [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="ba572-169">Далее следует создать сайт группы SharePoint Online, следуя приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="ba572-169">Next, you create the SharePoint Online team site with these steps.</span></span>
  
1. <span data-ttu-id="ba572-170">Войдите в Центр администрирования с помощью учетной записи, которая также используется для администрирования сайта группы SharePoint Online (учетной записи администратора SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="ba572-170">Sign in to the admin center with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator).</span></span> <span data-ttu-id="ba572-171">Дополнительные сведения см. в статье [Вход в Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="ba572-171">For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="ba572-172">В списке плиток выберите **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="ba572-172">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="ba572-173">На новой вкладке **SharePoint** в браузере щелкните **+ Создать сайт**.</span><span class="sxs-lookup"><span data-stu-id="ba572-173">In the new **SharePoint** tab of your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="ba572-174">На странице **Создайте сайт** щелкните **Сайт группы**.</span><span class="sxs-lookup"><span data-stu-id="ba572-174">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="ba572-175">В поле **Имя сайта** введите имя для частного сайта группы.</span><span class="sxs-lookup"><span data-stu-id="ba572-175">In **Site name**, type a name for the private team site.</span></span>
    
6. <span data-ttu-id="ba572-176">В поле **Описание сайта группы** введите описание (необязательно).</span><span class="sxs-lookup"><span data-stu-id="ba572-176">In **Team site description**, type an optional description.</span></span>
    
7. <span data-ttu-id="ba572-177">В разделе **Параметры конфиденциальности** выберите **Закрытая группа: только участники имеют доступ к этому сайту** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ba572-177">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="ba572-178">В области **Кого вы хотите добавить?** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="ba572-178">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="ba572-179">С помощью действий, приведенных ниже, настройте разрешения на новом сайте группы SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="ba572-179">Next, from the new SharePoint Online team site, configure permissions with these steps.</span></span>
  
1. <span data-ttu-id="ba572-180">Определите имя участника-пользователя (UPN) для ИТ-администратора или другого человека, который будет обрабатывать запросы на получение доступа к сайту и отвечать на них (reginap@contoso.com — пример имени участника-пользователя).</span><span class="sxs-lookup"><span data-stu-id="ba572-180">Determine the User Principal Name (UPN) of the IT administrator or other person who will be responsible for responding to and addressing requests for access to the site (belindan@contoso.com is an example of a UPN).</span></span> 
    
2. <span data-ttu-id="ba572-181">На панели инструментов щелкните значок параметров и выберите вариант **Разрешения для сайта**.</span><span class="sxs-lookup"><span data-stu-id="ba572-181">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
3. <span data-ttu-id="ba572-182">В области **Разрешения для сайта** щелкните **Параметры дополнительных разрешений**.</span><span class="sxs-lookup"><span data-stu-id="ba572-182">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
4. <span data-ttu-id="ba572-183">На новой вкладке браузера **Разрешения** щелкните **Параметры запроса доступа**.</span><span class="sxs-lookup"><span data-stu-id="ba572-183">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
    
5. <span data-ttu-id="ba572-184">В диалоговом окне **Параметры запросов доступа**:</span><span class="sxs-lookup"><span data-stu-id="ba572-184">In the **Access Requests Settings** dialog box:</span></span>
    
  - <span data-ttu-id="ba572-185">Снимите флажки **Разрешить участникам совместный доступ к этому сайту, а также отдельным файлам и папкам** и **Разрешить участникам приглашать других пользователей в группу участников сайта**.</span><span class="sxs-lookup"><span data-stu-id="ba572-185">Clear the **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** check boxes.</span></span>
    
  - <span data-ttu-id="ba572-186">В поле **Отправлять все запросы на доступ** введите имя UPN ИТ-администратора из шага 1.</span><span class="sxs-lookup"><span data-stu-id="ba572-186">Type the UPN of your IT administrator from step 1 in **Send all requests for access**.</span></span>
    
  - <span data-ttu-id="ba572-187">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="ba572-187">Click **OK**.</span></span>
    
6. <span data-ttu-id="ba572-188">На вкладке браузера **Разрешения** в списке выберите **[имя сайта] — участники**.</span><span class="sxs-lookup"><span data-stu-id="ba572-188">On the **Permissions** tab of your browser, click **[site name] Members** in the list.</span></span>
    
7. <span data-ttu-id="ba572-189">В разделе **Пользователи и группы** нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ba572-189">In **People and Groups**, click **New**.</span></span>
    
8. <span data-ttu-id="ba572-190">В диалоговом окне **Общий доступ** введите имя группы доступа участников сайта, выделите его и нажмите кнопку **Предоставить общий доступ**.</span><span class="sxs-lookup"><span data-stu-id="ba572-190">In the **Share** dialog box, type the name of your site members access group for this site, select it, and then click **Share**.</span></span>
    
9. <span data-ttu-id="ba572-191">Нажмите кнопку "Назад" в браузере.</span><span class="sxs-lookup"><span data-stu-id="ba572-191">Click the back button on your browser.</span></span>
    
10. <span data-ttu-id="ba572-192">В списке выберите пункт **[имя_сайта] — владельцы**.</span><span class="sxs-lookup"><span data-stu-id="ba572-192">Click **[site name] Owners** in the list.</span></span>
    
11. <span data-ttu-id="ba572-193">В разделе **Пользователи и группы** нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ba572-193">In **People and Groups**, click **New**.</span></span>
    
12. <span data-ttu-id="ba572-194">В диалоговом окне **Общий доступ** введите имя группы доступа администраторов сайта, выделите его и нажмите кнопку **Предоставить общий доступ**.</span><span class="sxs-lookup"><span data-stu-id="ba572-194">In the **Share** dialog box, type the name of the site administrators access group for this site, select it, and then click **Share**.</span></span>
    
13. <span data-ttu-id="ba572-195">Нажмите кнопку "Назад" в браузере.</span><span class="sxs-lookup"><span data-stu-id="ba572-195">Click the back button on your browser.</span></span>
    
14. <span data-ttu-id="ba572-196">В списке выберите пункт **[имя_сайта] — посетители**.</span><span class="sxs-lookup"><span data-stu-id="ba572-196">Click **[site name] Visitors** in the list.</span></span>
    
15. <span data-ttu-id="ba572-197">В разделе **Пользователи и группы** нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="ba572-197">In **People and Groups**, click **New**.</span></span>
    
16. <span data-ttu-id="ba572-198">В диалоговом окне **Общий доступ** введите имя группы доступа посетителей сайта, выделите его и нажмите кнопку **Предоставить общий доступ**.</span><span class="sxs-lookup"><span data-stu-id="ba572-198">In the **Share** dialog box, type the name of the site viewers access group for this site, select it, and then click **Share**.</span></span>
    
17. <span data-ttu-id="ba572-199">Закройте вкладку браузера **Разрешения**.</span><span class="sxs-lookup"><span data-stu-id="ba572-199">Close the **Permissions** tab of your browser.</span></span>
    
<span data-ttu-id="ba572-200">Ознакомьтесь с результатами настройки разрешений.</span><span class="sxs-lookup"><span data-stu-id="ba572-200">The results of these permission settings are:</span></span>
  
- <span data-ttu-id="ba572-201">Группа SharePoint **[имя сайта] — владельцы** содержит группу доступа администраторов сайта, все члены которой имеют уровень разрешений **Полный доступ**.</span><span class="sxs-lookup"><span data-stu-id="ba572-201">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="ba572-202">Группа SharePoint **[имя сайта] — участники** содержит группу доступа участников сайта, в которой все участники имеют уровень разрешений **Изменение**.</span><span class="sxs-lookup"><span data-stu-id="ba572-202">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="ba572-203">Группа SharePoint **[имя сайта] — посетители** содержит группу доступа посетителей сайта, в которой все участники имеют уровень разрешений **Чтение**.</span><span class="sxs-lookup"><span data-stu-id="ba572-203">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="ba572-204">Для участников отключена возможность приглашать других участников.</span><span class="sxs-lookup"><span data-stu-id="ba572-204">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="ba572-205">Для пользователей, не входящих в группу, включена возможность запроса доступа.</span><span class="sxs-lookup"><span data-stu-id="ba572-205">The ability for non-members to request access is enabled.</span></span>
    
<span data-ttu-id="ba572-206">Ниже показана полученная в итоге конфигурация.</span><span class="sxs-lookup"><span data-stu-id="ba572-206">Here is your resulting configuration.</span></span>
  
![Уровень защиты для конфиденциальных данных в случае изолированного сайта группы SharePoint Online.](media/7a6ab9c6-560a-4674-ac39-8175644dbe6f.png)
  
<span data-ttu-id="ba572-208">Благодаря членству в одной из групп доступа участники сайта теперь могут безопасно работать с ресурсами сайта.</span><span class="sxs-lookup"><span data-stu-id="ba572-208">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="highly-confidential-sharepoint-online-team-sites"></a><span data-ttu-id="ba572-209">Сайты групп SharePoint Online со строго конфиденциальным уровнем защиты</span><span class="sxs-lookup"><span data-stu-id="ba572-209">Highly confidential SharePoint Online team sites</span></span>

<span data-ttu-id="ba572-210">Сайт группы SharePoint Online со строго конфиденциальным уровнем защиты является изолированным сайтом группы. Это означает, что управление разрешениями осуществляется за счет членства в группах SharePoint, а не членства в группе Office 365, связанной с сайтом группы.</span><span class="sxs-lookup"><span data-stu-id="ba572-210">A highly confidential SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="ba572-211">Создание изолированного сайта для строго конфиденциальных данных и совместной работы выполняется в два основных этапа.</span><span class="sxs-lookup"><span data-stu-id="ba572-211">To create an isolated team site for highly confidential information and collaboration, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="ba572-212">Шаг 1. Разработка изолированного сайта</span><span class="sxs-lookup"><span data-stu-id="ba572-212">Step 1: Design your isolated site</span></span>

<span data-ttu-id="ba572-213">Чтобы разработать изолированный сайт группы, необходимо определить:</span><span class="sxs-lookup"><span data-stu-id="ba572-213">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="ba572-214">Группы SharePoint и уровни разрешений.</span><span class="sxs-lookup"><span data-stu-id="ba572-214">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="ba572-215">Набор групп доступа, которые будут участниками групп SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ba572-215">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="ba572-216">Рекомендуется следующий набор групп доступа: один для участников сайта, один для посетителей сайта и один для администраторов сайта.</span><span class="sxs-lookup"><span data-stu-id="ba572-216">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="ba572-217">Будут ли использоваться вложенные группы внутри групп доступа.</span><span class="sxs-lookup"><span data-stu-id="ba572-217">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="ba572-218">Например, рекомендуемая структура групп и уровни разрешений выглядят следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ba572-218">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="ba572-219">**Группа SharePoint**</span><span class="sxs-lookup"><span data-stu-id="ba572-219">**SharePoint group**</span></span>|<span data-ttu-id="ba572-220">**Уровень разрешений**</span><span class="sxs-lookup"><span data-stu-id="ba572-220">**Permission level**</span></span>|<span data-ttu-id="ba572-221">**Группа доступа (примеры)**</span><span class="sxs-lookup"><span data-stu-id="ba572-221">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba572-222">[имя сайта] — участники</span><span class="sxs-lookup"><span data-stu-id="ba572-222">[site name] Members</span></span>  <br/> |<span data-ttu-id="ba572-223">Правка</span><span class="sxs-lookup"><span data-stu-id="ba572-223">Edit</span></span>  <br/> |<span data-ttu-id="ba572-224">[имя сайта] — участники</span><span class="sxs-lookup"><span data-stu-id="ba572-224">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="ba572-225">[имя сайта] — посетители</span><span class="sxs-lookup"><span data-stu-id="ba572-225">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="ba572-226">Чтение</span><span class="sxs-lookup"><span data-stu-id="ba572-226">Read</span></span>  <br/> |<span data-ttu-id="ba572-227">[имя сайта] — посетители</span><span class="sxs-lookup"><span data-stu-id="ba572-227">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="ba572-228">[имя сайта] — владельцы</span><span class="sxs-lookup"><span data-stu-id="ba572-228">[site name] Owners</span></span>  <br/> |<span data-ttu-id="ba572-229">Полный доступ</span><span class="sxs-lookup"><span data-stu-id="ba572-229">Full control</span></span>  <br/> |<span data-ttu-id="ba572-230">[имя сайта] — администраторы</span><span class="sxs-lookup"><span data-stu-id="ba572-230">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="ba572-p107">Группы и уровни разрешений SharePoint создаются по умолчанию для сайта группы. Необходимо определить имена групп доступа.</span><span class="sxs-lookup"><span data-stu-id="ba572-p107">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="ba572-233">Сведения о процессе разработки см. в статье [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md) (Разработка изолированного сайта группы SharePoint Online).</span><span class="sxs-lookup"><span data-stu-id="ba572-233">For the details of the design process, see [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="ba572-234">Шаг 2. Развертывание изолированного сайта</span><span class="sxs-lookup"><span data-stu-id="ba572-234">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="ba572-235">Для развертывания изолированного сайта сначала необходимо:</span><span class="sxs-lookup"><span data-stu-id="ba572-235">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="ba572-236">Определить пользователя и членов каждой из групп доступа.</span><span class="sxs-lookup"><span data-stu-id="ba572-236">Determine the user and group members of each of your access groups</span></span>
    
- <span data-ttu-id="ba572-237">Создать группы доступа и добавить пользователя и членов группы.</span><span class="sxs-lookup"><span data-stu-id="ba572-237">Create the access groups and add the user and group members</span></span>
    
- <span data-ttu-id="ba572-238">Создать изолированный сайт группы, для которого используются группы доступа.</span><span class="sxs-lookup"><span data-stu-id="ba572-238">Create an isolated team site that uses your access groups</span></span>
    
<span data-ttu-id="ba572-239">Подробные инструкции см. в статье [Развертывание изолированного сайта группы SharePoint Online](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="ba572-239">For the detailed steps, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="ba572-240">Ниже приведены результаты настройки разрешений.</span><span class="sxs-lookup"><span data-stu-id="ba572-240">The results of the permission settings are:</span></span>
  
- <span data-ttu-id="ba572-241">Группа SharePoint **[имя сайта] — владельцы** содержит группу доступа администраторов сайта, все члены которой имеют уровень разрешений **Полный доступ**.</span><span class="sxs-lookup"><span data-stu-id="ba572-241">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="ba572-242">Группа SharePoint **[имя сайта] — участники** содержит группу доступа участников сайта, в которой все участники имеют уровень разрешений **Изменение**.</span><span class="sxs-lookup"><span data-stu-id="ba572-242">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="ba572-243">Группа SharePoint **[имя сайта] — посетители** содержит группу доступа посетителей сайта, в которой все участники имеют уровень разрешений **Чтение**.</span><span class="sxs-lookup"><span data-stu-id="ba572-243">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="ba572-244">Для участников отключена возможность приглашать других участников.</span><span class="sxs-lookup"><span data-stu-id="ba572-244">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="ba572-245">Для пользователей, не являющихся участниками, отключена возможность запроса доступа.</span><span class="sxs-lookup"><span data-stu-id="ba572-245">The ability for non-members to request access is disabled.</span></span>
    
<span data-ttu-id="ba572-246">Ниже показана полученная в итоге конфигурация.</span><span class="sxs-lookup"><span data-stu-id="ba572-246">Here is your resulting configuration.</span></span>
  
![Уровень защиты строго конфиденциальных данных для изолированного сайта группы SharePoint Online.](media/196359ab-d7ed-4fcf-97b4-61820a74aca4.png)
  
<span data-ttu-id="ba572-248">Благодаря членству в одной из групп доступа участники сайта теперь могут безопасно работать с ресурсами сайта.</span><span class="sxs-lookup"><span data-stu-id="ba572-248">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="ba572-249">Следующий этап</span><span class="sxs-lookup"><span data-stu-id="ba572-249">Next step</span></span>

[<span data-ttu-id="ba572-250">Защита файлов SharePoint Online с помощью меток Office 365 и DLP</span><span class="sxs-lookup"><span data-stu-id="ba572-250">Protect SharePoint Online files with Office 365 labels and DLP</span></span>](protect-sharepoint-online-files-with-office-365-labels-and-dlp.md)

## <a name="see-also"></a><span data-ttu-id="ba572-251">См. также</span><span class="sxs-lookup"><span data-stu-id="ba572-251">See also</span></span>

[<span data-ttu-id="ba572-252">Безопасность сайтов и файлов SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ba572-252">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="ba572-253">Руководство по безопасности (Майкрософт) для политических кампаний, некоммерческих и других динамических организаций</span><span class="sxs-lookup"><span data-stu-id="ba572-253">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="ba572-254">Освоение облака и гибридные решения</span><span class="sxs-lookup"><span data-stu-id="ba572-254">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
