---
title: Настроить пользовательский заблокированных список URL-адресов с помощью Office 365 ATP безопасных ссылки
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 896a7efb-1683-465e-a394-261349e5d866
description: В этой статье описан процесс настройки списка заблокированных URL-адресов для вашей организации, с помощью защиты расширенного Threat Office 365. Заблокированные URL-адреса будут применяться ко сообщения электронной почты и документов Office в соответствии с политиках безопасных ссылок анализа.
ms.openlocfilehash: 36d295e6924d2e9972c185657885fa25bd96bf08
ms.sourcegitcommit: 7032830867eb3fc71760e04b8342aff174c5d757
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/01/2018
ms.locfileid: "25353255"
---
# <a name="set-up-a-custom-blocked-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="66730-104">Настроить пользовательский заблокированных список URL-адресов с помощью Office 365 ATP безопасных ссылки</span><span class="sxs-lookup"><span data-stu-id="66730-104">Set up a custom blocked URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="66730-p102">С [Защиту от угроз для Office 365 Advanced](office-365-atp.md) (ATP) ваша организация может иметь настраиваемый список адресов веб-сайта (URL-адреса), которые блокируются. При блокировании URL-адрес людей, щелкните на ссылки, заблокированные URL-адрес, взяты [страницы предупреждение](atp-safe-links-warning-pages.md) , выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="66730-p102">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a custom list of website addresses (URLs) that are blocked. When a URL is blocked, people who click on links to the blocked URL are taken to a [warning page](atp-safe-links-warning-pages.md) that resembles the following image:</span></span> 
  
![Этот сайт будет блокировано](media/6b4bda2d-a1e6-419e-8b10-588e83c3af3f.png)
  
<span data-ttu-id="66730-108">Черный список URL-адресов определяется группа безопасности вашей организации Office 365, и этот список применяется ко всем пользователям в организации, который покрывает безопасных связи с Office 365 ATP политик.</span><span class="sxs-lookup"><span data-stu-id="66730-108">The blocked URLs list is defined by your organization's Office 365 security team, and that list applies to everyone in the organization who is covered by Office 365 ATP Safe Links policies.</span></span> 
  
<span data-ttu-id="66730-109">В этой статье, чтобы узнать, как настроить настраиваемые черный список URL-адресов вашей организации для [Анализа безопасных ссылок в Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="66730-109">Read this article to learn how to set up your organization's custom blocked URLs list for [ATP Safe Links in Office 365](atp-safe-links.md).</span></span>
  
## <a name="view-or-edit-a-custom-list-of-blocked-urls"></a><span data-ttu-id="66730-110">Просмотр или изменение настраиваемого списка заблокированных URL-адресов</span><span class="sxs-lookup"><span data-stu-id="66730-110">View or edit a custom list of blocked URLs</span></span>

<span data-ttu-id="66730-p103">[ATP безопасных ссылок в Office 365](atp-safe-links.md) использует несколько списков, включая настраиваемые черный список URL-адресов вашей организации. При наличии необходимых разрешений можно настроить пользовательский список вашей организации. Это делается путем редактирования политики безопасных ссылки вашей организации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="66730-p103">[ATP Safe Links in Office 365](atp-safe-links.md) uses several lists, including your organization's custom blocked URLs list. If you have the necessary permissions, you can set up your organization's custom list. You do this by editing your organization's default Safe Links policy.</span></span>
  
1. <span data-ttu-id="66730-114">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и войдите с учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="66730-114">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="66730-115">В левой панели навигации в разделе **Управление угроз**, выберите **политику** \> **Безопасных ссылки**.</span><span class="sxs-lookup"><span data-stu-id="66730-115">In the left navigation, under **Threat management**, choose **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="66730-116">Раздел **политики, которые применяются во всей организации** выберите вариант **по умолчанию**и выберите команду **Изменить** ("Изменить" представляет Карандаш).</span><span class="sxs-lookup"><span data-stu-id="66730-116">In the **Policies that apply to the entire organization** section, select **Default**, and then choose **Edit** (the Edit button resembles a pencil).</span></span> 
    
    ![Нажмите кнопку Изменить для изменения политики по умолчанию для защиты безопасных ссылки](media/d08f9615-d947-4033-813a-d310ec2c8cca.png)
  
    <span data-ttu-id="66730-p104">Здесь указывается, куда просматривать список заблокированных URL-адреса. Обратите внимание, что в первую очередь, не будут иметь все URL-адреса из списка.</span><span class="sxs-lookup"><span data-stu-id="66730-p104">This is where you go to view your list of blocked URLs. Note that at first, you won't have any URLs listed.</span></span>
    
    ![В списке заблокированных URL-адреса — в по умолчанию безопасных ссылки политику, применяемую ко всей организации.](media/575e1449-6191-40ac-b626-030a2fd3fb11.png)
  
4. <span data-ttu-id="66730-p105">Выберите поле **Введите допустимый URL-адрес** и введите URL-адрес, а затем нажмите знак плюс (+). Ниже перечислены следует помнить о нескольких моментах:</span><span class="sxs-lookup"><span data-stu-id="66730-p105">Select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+). Here are a few things to keep in mind:</span></span> 
    
  - <span data-ttu-id="66730-p106">Можно указать только для домена URL-адрес (например `contoso.com` или `tailspintoys.com`). Это будет блокировать щелчков на любой URL-адрес, содержащий домен.</span><span class="sxs-lookup"><span data-stu-id="66730-p106">You can specify a domain-only URL (like `contoso.com` or `tailspintoys.com`). This will block clicks on any URL that contains the domain.</span></span>
    
  - <span data-ttu-id="66730-p107">Не включать косую черту ( **/**) в конце URL-адрес. Например, вместо ввода `http://www.contoso.com/`, введите `http://www.contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="66730-p107">Do not include a forward slash ( **/**) at the end of the URL. For example, instead of entering `http://www.contoso.com/`, enter `http://www.contoso.com`.</span></span>
    
  - <span data-ttu-id="66730-p108">Может включать до трех подстановочные знаки звездочки (\*) на URL-адрес. В следующей таблице перечислены, имеют несколько примеров можно ввести и что в силу операций.</span><span class="sxs-lookup"><span data-stu-id="66730-p108">You can include up to three wildcard asterisks (\*) per URL. The following table lists some examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="66730-129">**Пример записи**</span><span class="sxs-lookup"><span data-stu-id="66730-129">**Example Entry**</span></span>|<span data-ttu-id="66730-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66730-130">**What It Does**</span></span>|
|:-----|:-----|
|<span data-ttu-id="66730-131">`contoso.com`или`*contoso.com*`</span><span class="sxs-lookup"><span data-stu-id="66730-131">`contoso.com` or `*contoso.com*`</span></span>  <br/> |<span data-ttu-id="66730-132">Блокирует домен, поддомены и пути, такие как `https://www.contoso.com`, `http://sub.contoso.com`, и`http://contoso.com/abc`</span><span class="sxs-lookup"><span data-stu-id="66730-132">Blocks the domain, subdomains, and paths, such as `https://www.contoso.com`, `http://sub.contoso.com`, and `http://contoso.com/abc`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="66730-133">Блокирует сайта `http://contoso.com/a` , но не дополнительные субконтуров like`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="66730-133">Blocks a site `http://contoso.com/a` but not additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a*`  <br/> |<span data-ttu-id="66730-134">Блокирует сайта `http://contoso.com/a` и дополнительные субконтуров, например`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="66730-134">Blocks a site `http://contoso.com/a` and additional subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
5. <span data-ttu-id="66730-135">Завершив добавление URL-адресов, в правом нижнем углу экрана, выберите команду **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="66730-135">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
## <a name="what-if-i-want-to-define-exceptions-for-certain-users-in-my-organization"></a><span data-ttu-id="66730-136">Что делать, если хотите определить исключения для некоторых пользователей в организации?</span><span class="sxs-lookup"><span data-stu-id="66730-136">What if I want to define exceptions for certain users in my organization?</span></span>

<span data-ttu-id="66730-p109">Если вы хотите определенных групп, чтобы иметь возможность просматривать URL-адресов, которые могут быть заблокированы для других пользователей, можно указать безопасных ссылок анализа политику, применяемую к определенным получателям. В разделе [Настройка настраиваемого «не rewrite» URL-адреса списка с помощью надежных ссылок анализа](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span><span class="sxs-lookup"><span data-stu-id="66730-p109">If you want certain groups to be able to view URLs that might be blocked for others, you can specify an ATP Safe Links policy that applies to specific recipients. See [Set up a custom "do not rewrite" URLs list using ATP Safe Links](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="66730-139">Смежные темы</span><span class="sxs-lookup"><span data-stu-id="66730-139">Related topics</span></span>

[<span data-ttu-id="66730-140">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="66730-140">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="66730-141">Безопасно ATP ссылок в Office 365</span><span class="sxs-lookup"><span data-stu-id="66730-141">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="66730-142">Настройка политик ATP безопасных ссылок в Office 365</span><span class="sxs-lookup"><span data-stu-id="66730-142">Set up ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
  
[<span data-ttu-id="66730-143">Безопасно ATP вложений в Office 365</span><span class="sxs-lookup"><span data-stu-id="66730-143">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)

[<span data-ttu-id="66730-144">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="66730-144">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

