---
title: Настройка настраиваемого списка "не перезаписывать URL-адреса" с помощью безОпасных ссылок Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/06/2019
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
ms.collection: M365-security-compliance
description: При настройке политик безопасных ссылок ATP можно включить список URL-адресов Do-not-Rewrite, чтобы разрешить некоторым пользователям в Организации посещать сайты, включенные в список.
ms.openlocfilehash: 7fbc7d0d0caec79dcdbb3dc5b1b5a8a4e085dc09
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215029"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="46869-103">Настройка настраиваемого списка "не перезаписывать URL-адреса" с помощью безОпасных ссылок Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="46869-103">Set up a custom do-not-rewrite URLs list using Office 365 ATP Safe Links</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46869-p101">Эта статья предназначена для корпоративных клиентов. Если вы являетесь домашним пользователем, который ищет сведения о безОпасных ссылках в Outlook, ознакомьтесь со статьей [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span><span class="sxs-lookup"><span data-stu-id="46869-p101">This article is intended for business customers. If you are a home user looking for information about Safe Links in Outlook, see [Advanced Outlook.com security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).</span></span>

<span data-ttu-id="46869-p102">В [Office 365 Advanced Threat protection](office-365-atp.md) (ATP) в организации могут быть [Настраиваемые заблокированНые URL-адреса](set-up-a-custom-blocked-urls-list-wtih-atp.md), например, если пользователи щелкают веб-адреса (URL-адреса) в сообщениях электронной почты или определенных документах Office, они не смогут переходить к этим URL-адресам. В организации также могут быть настроены списки "не переопределять" для определенных групп в Организации. Список "не переопределять" позволяет некоторым пользователям посещать URL-адреса, которые в противном случае блокируются [безопасными ссылкаМи ATP в Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="46869-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a [custom blocked URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md), such that when people click on web addresses (URLs) in email messages or certain Office documents, they are prevented from going to those URLs. Your organization can also have custom "do not rewrite" lists for specific groups in your organization. A "do not rewrite" list enables some people to visit URLs that are otherwise blocked by [ATP Safe Links in Office 365](atp-safe-links.md).</span></span> 
  
<span data-ttu-id="46869-109">В этой статье описывается, как указать список URL-адресов, исключаемых из проверки безОпасных ссылок ATP, и некоторые важные моменты, которые следует учитывать.</span><span class="sxs-lookup"><span data-stu-id="46869-109">This article describes how to specify a list of URLs that are excluded from ATP Safe Links scanning, and a few important points to keep in mind.</span></span>

## <a name="set-up-a-do-not-rewrite-list"></a><span data-ttu-id="46869-110">Настройка списка "не переопределять"</span><span class="sxs-lookup"><span data-stu-id="46869-110">Set up a "do not rewrite" list</span></span>

<span data-ttu-id="46869-p103">Защита безОпасных ссылок ATP использует несколько списков, в том числе список заблокированных URL-адресов вашей организации, а также списки "не переопределять" для исключений. Если у вас есть необходимые разрешения, вы можете настроить настраиваемые списки "не переопределять". Это делается при добавлении или изменении политик безОпасных ссылок, которые применяются к определенным получателям в Организации.</span><span class="sxs-lookup"><span data-stu-id="46869-p103">ATP Safe Links protection uses several lists, including your organization's blocked URLs list and the "do not rewrite" lists for exceptions. If you have the necessary permissions, you can set up your custom "do not rewrite" lists. You do this when you add or edit Safe Links policies that apply to specific recipients in your organization.</span></span> 

<span data-ttu-id="46869-114">Чтобы изменить (или определить) политики ATP, необходимо назначить одну из ролей, описанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="46869-114">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span>

|<span data-ttu-id="46869-115">Роль</span><span class="sxs-lookup"><span data-stu-id="46869-115">Role</span></span>  |<span data-ttu-id="46869-116">Где/как назначено</span><span class="sxs-lookup"><span data-stu-id="46869-116">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="46869-117">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="46869-117">Office 365 Global Administrator</span></span> |<span data-ttu-id="46869-p104">Пользователь, который подписывается на приобретение Office 365, по умолчанию является глобальным администратором. (Чтобы узнать больше, ознакомьтесь со статьей [о ролях администратора Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)</span><span class="sxs-lookup"><span data-stu-id="46869-p104">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="46869-120">администратор безопасности (Security Administrator).</span><span class="sxs-lookup"><span data-stu-id="46869-120">Security Administrator</span></span> |<span data-ttu-id="46869-121">Центр администрирования Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span><span class="sxs-lookup"><span data-stu-id="46869-121">Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com))</span></span>|
|<span data-ttu-id="46869-122">Управление организацией Exchange Online</span><span class="sxs-lookup"><span data-stu-id="46869-122">Exchange Online Organization Management</span></span> |<span data-ttu-id="46869-123">Центр администрирования Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="46869-123">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="46869-124">или</span><span class="sxs-lookup"><span data-stu-id="46869-124">or</span></span> <br>  <span data-ttu-id="46869-125">Командлеты PowerShell (см. [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="46869-125">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |

> [!TIP]
> <span data-ttu-id="46869-126">Дополнительные сведения о ролях и разрешениях приведены [в разделе разрешения в центре безопасности &amp; и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="46869-126">To learn more about roles and permissions, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

### <a name="to-view-or-edit-a-custom-do-not-rewrite-urls-list"></a><span data-ttu-id="46869-127">Просмотр и редактирование настраиваемого списка URL-адресов "не переопределять"</span><span class="sxs-lookup"><span data-stu-id="46869-127">To view or edit a custom "do not rewrite" URLs list</span></span>
  
1. <span data-ttu-id="46869-128">Перейдите к [https://protection.office.com](https://protection.office.com) рабочей или учебной учетной записи и войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="46869-128">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="46869-129">На левой панели навигации в разделе **безопасные ссылки** **политики** \> **управления** \> угрозой.</span><span class="sxs-lookup"><span data-stu-id="46869-129">In the left navigation, under **Threat management** \> **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="46869-p105">В разделе **политики, которые применяются к определенным получателям** нажмите кнопку **создать** (Новая кнопка напоминает знак плюса ( **+**)), чтобы создать новую политику. (Кроме того, вы можете изменить существующую политику.)</span><span class="sxs-lookup"><span data-stu-id="46869-p105">In the **Policies that apply to specific recipients** section, choose **New** (the New button resembles a plus sign ( **+**)) to create a new policy. (Alternatively, you can edit an existing policy.)</span></span><br/><span data-ttu-id="46869-132">![Нажмите кнопку Создать, чтобы добавить политику безОпасных ссылок для определенных получателей электронной почты.](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)</span><span class="sxs-lookup"><span data-stu-id="46869-132">![Choose New to add a Safe Links policy for specific email recipients](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)</span></span>
  
4. <span data-ttu-id="46869-133">Укажите имя и описание для политики.</span><span class="sxs-lookup"><span data-stu-id="46869-133">Specify a name and description for your policy.</span></span>
    
5. <span data-ttu-id="46869-134">В разделе **не переопределять следующие URL-адреса** установите флажок **введите ДОПУСТИМЫй URL-** адрес, а затем введите URL-адрес, а затем выберите знак плюс (+).</span><span class="sxs-lookup"><span data-stu-id="46869-134">In the **Do not rewrite the following URLs** section, select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+).</span></span> 
    
6. <span data-ttu-id="46869-p106">В разделе **применено** выберите **получатель**, а затем выберите группу (группы), которую нужно включить в политику. Нажмите кнопку **Добавить**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="46869-p106">In the **Applied To** section, choose **The recipient is a member of**, and then choose the group(s) you want to include in your policy. Choose **Add**, and then choose **OK**.</span></span>
    
7. <span data-ttu-id="46869-137">Завершив добавление URL-адресов, в правом нижнем углу экрана нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="46869-137">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="46869-p107">Обязательно изучите свой список заблокированных URL-адресов в Организации. [В разделе Настройка настраиваемого списка заблокированНых URL-адресов с помощью ссылок ATP Safe](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span><span class="sxs-lookup"><span data-stu-id="46869-p107">Make sure to review your organization's custom list of blocked URLs. See [Set up a custom blocked URLs list using ATP Safe Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span></span> 
  
## <a name="important-points-to-keep-in-mind"></a><span data-ttu-id="46869-140">Важные моменты, которые следует учитывать</span><span class="sxs-lookup"><span data-stu-id="46869-140">Important points to keep in mind</span></span>

- <span data-ttu-id="46869-141">Все URL-адреса, указанные в списке "не перезаписывать", будут исключены из проверки безОпасных ссылок ATP для указанных получателей.</span><span class="sxs-lookup"><span data-stu-id="46869-141">Any URLs that you specify in the "do not rewrite" list are excluded from ATP Safe Links scanning for the recipients that you specify.</span></span>
 
- <span data-ttu-id="46869-p108">При указании списка "не переопределять" для политики безОпасных ссылок ATP можно добавить до трех символов "звездочка" (\*). Подстановочные знаки\*() предполагаются для таких записей `contoso.com`, как, например, не включая префиксы или поддомены, `http://` например `https://`или. Это означает, `contoso.com` `*contoso.com*` что запись в списке "не переопределять".</span><span class="sxs-lookup"><span data-stu-id="46869-p108">When you specify a "do not rewrite" list for an ATP Safe Links policy, you can include up to three wildcard asterisks (\*). Wildcards (\*) are assumed for entries such as `contoso.com`, which do not explicitly include prefixes or subdomains, like `http://` or `https://`. This means an entry, such as `contoso.com` is similar to `*contoso.com*` for your "do not rewrite" list.</span></span>

- <span data-ttu-id="46869-p109">Если у вас уже есть список URL-адресов в списке "не переопределять", обязательно просмотрите список и добавьте подстановочные знаки. Например, если у имеющегося списка есть запись, `http://contoso.com/a` а вы хотите включить подпути, такие как `http://contoso.com/a/b` в вашей политике, добавьте к записи подстановочный знак, чтобы он выглядел `http://contoso.com/a*`так:</span><span class="sxs-lookup"><span data-stu-id="46869-p109">If you already have a list of URLs in your "do not rewrite" list, make sure to review that list and add wildcards as appropriate. For example, if your existing list has an entry like `http://contoso.com/a` and you want to include subpaths like `http://contoso.com/a/b` in your policy, add a wildcard to your entry so it looks like `http://contoso.com/a*`.</span></span>
    
- <span data-ttu-id="46869-p110">Не включайте косую черту (/) в URL-адресах, указанных в списке "не переопределять". Например, вместо того, чтобы `contoso.com/` вводить в списке "не переопределять", введите `contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="46869-p110">Do not include a forward slash (/) in the URLs that you specify in your "do not rewrite" list. For example, rather than enter `contoso.com/` in your "do not rewrite" list, enter `contoso.com`.</span></span>
    
<span data-ttu-id="46869-149">В следующей таблице приведены примеры того, что можно ввести и какие действия имеют эти записи.</span><span class="sxs-lookup"><span data-stu-id="46869-149">The following table lists examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="46869-150">**Пример записи**</span><span class="sxs-lookup"><span data-stu-id="46869-150">**Example Entry**</span></span>|<span data-ttu-id="46869-151">**Что он делает**</span><span class="sxs-lookup"><span data-stu-id="46869-151">**What It Does**</span></span>|
|:-----|:-----|
|`*contoso.com*`  <br/> |<span data-ttu-id="46869-152">Позволяет конкретным получателям посещать домен, дочерние домены и пути, например `http://www.contoso.com`, `https://www.contoso.com` `https://maps.contoso.com`,, или`http://www.contoso.com/a`</span><span class="sxs-lookup"><span data-stu-id="46869-152">Allows specific recipients to visit a domain, subdomains, and paths, such as `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, or `http://www.contoso.com/a`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="46869-153">Позволяет конкретным получателям посетить сайт, например `http://contoso.com/a`, недопустимые подпути, такие как`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="46869-153">Allows specific recipients to visit a site like `http://contoso.com/a`, but not subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="46869-154">Позволяет конкретным получателям посещать подобные `http://contoso.com/a` и вложенные пути, такие как`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="46869-154">Allows specific recipients to visit a site like `http://contoso.com/a` and subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
 