---
title: Настроить пользовательский заблокированных список URL-адресов с помощью Office 365 ATP безопасных ссылки
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 02/05/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Узнайте, как настроить список заблокированных URL-адресов для вашей организации, с помощью защиты расширенного Threat Office 365. Заблокированные URL-адреса будут применяться ко сообщения электронной почты и документов Office в соответствии с политиках безопасных ссылок анализа.
ms.openlocfilehash: 4146424056c9a5b30f51a58fd020df912fa048ef
ms.sourcegitcommit: a64af0ebd0b03e4a5e60a33e9108c44c7d74f356
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2019
ms.locfileid: "29741022"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="c0344-104">Настроить пользовательский заблокированных список URL-адресов с помощью Office 365 ATP безопасных ссылки</span><span class="sxs-lookup"><span data-stu-id="c0344-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="c0344-p102">С [Защиту от угроз для Office 365 Advanced](office-365-atp.md) (ATP) ваша организация может иметь настраиваемый список адресов веб-сайта (URL-адреса), которые блокируются. При блокировании URL-адрес людей, щелкните на ссылки, заблокированные URL-адрес, взяты [страницы предупреждение](atp-safe-links-warning-pages.md) , выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c0344-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Этот сайт будет блокировано](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="c0344-108">Черный список URL-адресов определяется группа безопасности вашей организации Office 365, и этот список применяется ко всем пользователям в организации, который покрывает безопасных связи с Office 365 ATP политик.</span><span class="sxs-lookup"><span data-stu-id="c0344-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="c0344-109">В этой статье, чтобы узнать, как настроить настраиваемые черный список URL-адресов вашей организации для [Анализа безопасных ссылок в Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="c0344-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="c0344-110">Просмотр или изменение настраиваемого списка заблокированных URL-адресов</span><span class="sxs-lookup"><span data-stu-id="c0344-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="c0344-p103">[ATP безопасных ссылок в Office 365](atp-safe-links.md) использует несколько списков, включая настраиваемые черный список URL-адресов вашей организации. При наличии необходимых разрешений можно настроить пользовательский список вашей организации. Это делается путем редактирования политики безопасных ссылки вашей организации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0344-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>

<span data-ttu-id="c0344-114">Для изменения (или задания) ATP политик, вам должна быть назначена одна из ролей описаны в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="c0344-114">To edit (or define) ATP policies, you must be assigned one of the roles described in the following table:</span></span> 

|<span data-ttu-id="c0344-115">Роль</span><span class="sxs-lookup"><span data-stu-id="c0344-115">Role</span></span>  |<span data-ttu-id="c0344-116">Где и как назначен</span><span class="sxs-lookup"><span data-stu-id="c0344-116">Where/how assigned</span></span>  |
|---------|---------|
|<span data-ttu-id="c0344-117">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="c0344-117">Office 365 Global Administrator</span></span> |<span data-ttu-id="c0344-p104">Человека, который регистрируется приобрести Office 365 — это глобального администратора по умолчанию. ( [Роли администраторов об Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) для получения дополнительных сведений см.)</span><span class="sxs-lookup"><span data-stu-id="c0344-p104">The person who signs up to buy Office 365 is a global admin by default. (See [About Office 365 admin roles](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) to learn more.)</span></span>         |
|<span data-ttu-id="c0344-120">Администратор безопасности Office 365</span><span class="sxs-lookup"><span data-stu-id="c0344-120">Office 365 Security Administrator</span></span> |<span data-ttu-id="c0344-121">Центр администрирования ([https://aka.ms/admincenter](https://aka.ms/admincenter))</span><span class="sxs-lookup"><span data-stu-id="c0344-121">Admin center ([https://aka.ms/admincenter](https://aka.ms/admincenter))</span></span>|
|<span data-ttu-id="c0344-122">Управление Exchange Online организацией</span><span class="sxs-lookup"><span data-stu-id="c0344-122">Exchange Online Organization Management</span></span> |<span data-ttu-id="c0344-123">Центр администрирования Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span><span class="sxs-lookup"><span data-stu-id="c0344-123">Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp))</span></span> <br><span data-ttu-id="c0344-124">или</span><span class="sxs-lookup"><span data-stu-id="c0344-124">or</span></span> <br>  <span data-ttu-id="c0344-125">Командлеты PowerShell (см. [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span><span class="sxs-lookup"><span data-stu-id="c0344-125">PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps))</span></span> |
  
1. <span data-ttu-id="c0344-126">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и войдите с учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="c0344-126">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="c0344-127">В левой панели навигации в разделе **Управление угроз**, выберите **политику** \> **Безопасных ссылки**.</span><span class="sxs-lookup"><span data-stu-id="c0344-127">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="c0344-128">Раздел **политики, которые применяются во всей организации** выберите вариант **по умолчанию**и выберите команду **Изменить** ("Изменить" представляет Карандаш).</span><span class="sxs-lookup"><span data-stu-id="c0344-128">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="c0344-129">![Нажмите кнопку Изменить для изменения политики по умолчанию для защиты безопасных ссылки](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="c0344-129">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="c0344-p105">Это позволяет просмотреть список заблокированных URL-адреса. В первую очередь может не иметь любое URL-адресов, перечисленных здесь.</span><span class="sxs-lookup"><span data-stu-id="c0344-p105">This enables you to view your list of blocked URLs. At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="c0344-132">![Заблокировано список URL-адресов в политике безопасных ссылок по умолчанию](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="c0344-132">![Blocked URLs list in the default Safe Links policy](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="c0344-133">Выберите поле **Введите допустимый URL-адрес** , введите URL-адрес и нажмите значок "плюс" (**+**).</span><span class="sxs-lookup"><span data-stu-id="c0344-133">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span> 

5. <span data-ttu-id="c0344-134">Завершив добавление URL-адресов, в правом нижнем углу экрана, выберите команду **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c0344-134">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="c0344-135">Следует помнить о нескольких моментах</span><span class="sxs-lookup"><span data-stu-id="c0344-135">A few things to keep in mind</span></span>

<span data-ttu-id="c0344-136">При добавлении в список URL-адресов следует учитывать следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="c0344-136">While you add URLs to your list, keep the following points in mind:</span></span> 

- <span data-ttu-id="c0344-p106">Не включать косую черту ( **/**) в конце URL-адрес. Например, вместо ввода `http://www.contoso.com/`, введите `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="c0344-p106">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
- <span data-ttu-id="c0344-p107">Можно указать только для домена URL-адрес (например `contoso.com` или `tailspintoys.com`). Это будет блокировать щелчков на любой URL-адрес, содержащий домен.</span><span class="sxs-lookup"><span data-stu-id="c0344-p107">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="c0344-p108">Можно указать дочернего домена (например `toys.contoso.com*`) без блокировки полного доменного (как `contoso.com`). В этом будут блока щелкает любой URL-адрес, содержащего дочерний домен, но он не будет блокировать щелчков на URL-адрес, который содержит полное доменное.</span><span class="sxs-lookup"><span data-stu-id="c0344-p108">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`). This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>  
    
- <span data-ttu-id="c0344-p109">Может включать до трех подстановочные знаки звездочки (\*) на URL-адрес. В следующей таблице перечислены, имеют несколько примеров можно ввести и что в силу операций.</span><span class="sxs-lookup"><span data-stu-id="c0344-p109">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="c0344-145">**Пример записи**</span><span class="sxs-lookup"><span data-stu-id="c0344-145">**Example Entry**</span></span>|<span data-ttu-id="c0344-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0344-146">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0344-147">`contoso.com`или`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="c0344-147">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="c0344-148">Блокирует домен, поддомены и пути, такие как `https://www.contoso.com`, `http://sub.contoso.com`, и`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="c0344-148">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="c0344-149">Блокирует сайта `http://contoso.com/a` , но не дополнительные субконтуров like`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="c0344-149">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="c0344-150">Блокирует сайта `http://contoso.com/a` и дополнительные субконтуров, например`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="c0344-150">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://toys.contoso.com*`  <br/> |<span data-ttu-id="c0344-151">Блоки a дочернего домена («toys» в данном случае), но разрешать щелчков мыши другие URL-адреса домена (например `http://contoso.com` или `http://home.contoso.com`).</span><span class="sxs-lookup"><span data-stu-id="c0344-151">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `http://contoso.com` or `http://home.contoso.com`).</span></span>  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="c0344-152">Как определить исключения для некоторых пользователей в организации</span><span class="sxs-lookup"><span data-stu-id="c0344-152">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="c0344-p110">Если вы хотите определенных групп, чтобы иметь возможность просматривать URL-адресов, которые могут быть заблокированы для других пользователей, можно указать безопасных ссылок анализа политику, применяемую к определенным получателям. В разделе [Настройка настраиваемого «не rewrite» URL-адреса списка с помощью надежных ссылок анализа](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="c0344-p110">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  

