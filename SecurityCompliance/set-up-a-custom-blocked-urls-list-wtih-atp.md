---
title: Настроить пользовательский заблокированных список URL-адресов с помощью Office 365 ATP безопасных ссылки
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.date: 12/11/2018
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: Узнайте, как настроить список заблокированных URL-адресов для вашей организации, с помощью защиты расширенного Threat Office 365. Заблокированные URL-адреса будут применяться ко сообщения электронной почты и документов Office в соответствии с политиках безопасных ссылок анализа.
ms.openlocfilehash: 25f01b767726ebf02d5da5d18444fa0428f144ac
ms.sourcegitcommit: 031781d0eecf33baabcd03ea53546d41076062b4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2018
ms.locfileid: "27240532"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="9618d-104">Настроить пользовательский заблокированных список URL-адресов с помощью Office 365 ATP безопасных ссылки</span><span class="sxs-lookup"><span data-stu-id="9618d-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="9618d-p102">С [Защиту от угроз для Office 365 Advanced](office-365-atp.md) (ATP) ваша организация может иметь настраиваемый список адресов веб-сайта (URL-адреса), которые блокируются. При блокировании URL-адрес людей, щелкните на ссылки, заблокированные URL-адрес, взяты [страницы предупреждение](atp-safe-links-warning-pages.md) , выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9618d-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Этот сайт будет блокировано](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="9618d-108">Черный список URL-адресов определяется группа безопасности вашей организации Office 365, и этот список применяется ко всем пользователям в организации, который покрывает безопасных связи с Office 365 ATP политик.</span><span class="sxs-lookup"><span data-stu-id="9618d-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="9618d-109">В этой статье, чтобы узнать, как настроить настраиваемые черный список URL-адресов вашей организации для [Анализа безопасных ссылок в Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="9618d-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="9618d-110">Просмотр или изменение настраиваемого списка заблокированных URL-адресов</span><span class="sxs-lookup"><span data-stu-id="9618d-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="9618d-p103">[ATP безопасных ссылок в Office 365](atp-safe-links.md) использует несколько списков, включая настраиваемые черный список URL-адресов вашей организации. При наличии необходимых разрешений можно настроить пользовательский список вашей организации. Это делается путем редактирования политики безопасных ссылки вашей организации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9618d-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>
  
1. <span data-ttu-id="9618d-114">Последовательно выберите пункты [https://security.microsoft.com](https://security.microsoft.com) и войдите с учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="9618d-114">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="9618d-115">В левой панели навигации в разделе **Управление угроз**, выберите **политику** \> **Безопасных ссылки**.</span><span class="sxs-lookup"><span data-stu-id="9618d-115">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="9618d-116">Раздел **политики, которые применяются во всей организации** выберите вариант **по умолчанию**и выберите команду **Изменить** ("Изменить" представляет Карандаш).</span><span class="sxs-lookup"><span data-stu-id="9618d-116">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span><br/><span data-ttu-id="9618d-117">![Нажмите кнопку Изменить для изменения политики по умолчанию для защиты безопасных ссылки](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span><span class="sxs-lookup"><span data-stu-id="9618d-117">![Click Edit to edit your default policy for Safe Links protection](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)</span></span><br/><span data-ttu-id="9618d-p104">Это позволяет просмотреть список заблокированных URL-адреса. В первую очередь может не иметь любое URL-адресов, перечисленных здесь.</span><span class="sxs-lookup"><span data-stu-id="9618d-p104">This enables you to view your list of blocked URLs. At first, you might not have any URLs listed here.</span></span><br/><span data-ttu-id="9618d-120">![Заблокировано список URL-адресов в политике безопасных ссылок по умолчанию](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span><span class="sxs-lookup"><span data-stu-id="9618d-120">![Blocked URLs list in the default Safe Links policy](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)</span></span>
  
4. <span data-ttu-id="9618d-121">Выберите поле **Введите допустимый URL-адрес** , введите URL-адрес и нажмите значок "плюс" (**+**).</span><span class="sxs-lookup"><span data-stu-id="9618d-121">Select the **Enter a valid URL** box, type a URL, and then choose the plus sign (**+**).</span></span> 

5. <span data-ttu-id="9618d-122">Завершив добавление URL-адресов, в правом нижнем углу экрана, выберите команду **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="9618d-122">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="a-few-things-to-keep-in-mind"></a><span data-ttu-id="9618d-123">Следует помнить о нескольких моментах</span><span class="sxs-lookup"><span data-stu-id="9618d-123">A few things to keep in mind</span></span>

<span data-ttu-id="9618d-124">При добавлении в список URL-адресов следует учитывать следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="9618d-124">While you add URLs to your list, keep the following points in mind:</span></span> 

- <span data-ttu-id="9618d-p105">Не включать косую черту ( **/**) в конце URL-адрес. Например, вместо ввода `http://www.contoso.com/`, введите `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="9618d-p105">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
- <span data-ttu-id="9618d-p106">Можно указать только для домена URL-адрес (например `contoso.com` или `tailspintoys.com`). Это будет блокировать щелчков на любой URL-адрес, содержащий домен.</span><span class="sxs-lookup"><span data-stu-id="9618d-p106">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>

- <span data-ttu-id="9618d-p107">Можно указать дочернего домена (например `toys.contoso.com*`) без блокировки полного доменного (как `contoso.com`). В этом будут блока щелкает любой URL-адрес, содержащего дочерний домен, но он не будет блокировать щелчков на URL-адрес, который содержит полное доменное.</span><span class="sxs-lookup"><span data-stu-id="9618d-p107">You can specify a subdomain (like `toys.contoso.com*`) without blocking a full domain (like `contoso.com`). This will block clicks any URL that contains the subdomain, but it won't block clicks to a URL that contains the full domain.</span></span>  
    
- <span data-ttu-id="9618d-p108">Может включать до трех подстановочные знаки звездочки (\*) на URL-адрес. В следующей таблице перечислены, имеют несколько примеров можно ввести и что в силу операций.</span><span class="sxs-lookup"><span data-stu-id="9618d-p108">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="9618d-133">**Пример записи**</span><span class="sxs-lookup"><span data-stu-id="9618d-133">**Example Entry**</span></span>|<span data-ttu-id="9618d-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9618d-134">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9618d-135">`contoso.com`или`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="9618d-135">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="9618d-136">Блокирует домен, поддомены и пути, такие как `https://www.contoso.com`, `http://sub.contoso.com`, и`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="9618d-136">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="9618d-137">Блокирует сайта `http://contoso.com/a` , но не дополнительные субконтуров like`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="9618d-137">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="9618d-138">Блокирует сайта `http://contoso.com/a` и дополнительные субконтуров, например`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="9618d-138">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://toys.contoso.com*`  <br/> |<span data-ttu-id="9618d-139">Блоки a дочернего домена («toys» в данном случае), но разрешать щелчков мыши другие URL-адреса домена (например `http://contoso.com` или `http://home.contoso.com`).</span><span class="sxs-lookup"><span data-stu-id="9618d-139">Blocks a subdomain ("toys" in this case) but allow clicks to other domain URLs (like `http://contoso.com` or `http://home.contoso.com`).</span></span>  <br/> |
   

## <a name="how-to-define-exceptions-for-certain-users-in-an-organization"></a><span data-ttu-id="9618d-140">Как определить исключения для некоторых пользователей в организации</span><span class="sxs-lookup"><span data-stu-id="9618d-140">How to define exceptions for certain users in an organization</span></span>

<span data-ttu-id="9618d-p109">Если вы хотите определенных групп, чтобы иметь возможность просматривать URL-адресов, которые могут быть заблокированы для других пользователей, можно указать безопасных ссылок анализа политику, применяемую к определенным получателям. В разделе [Настройка настраиваемого «не rewrite» URL-адреса списка с помощью надежных ссылок анализа](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="9618d-p109">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  

