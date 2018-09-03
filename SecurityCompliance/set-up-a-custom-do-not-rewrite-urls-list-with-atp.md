---
title: Настроить пользовательский список not переопределения URL-адресов с помощью Office 365 ATP безопасных ссылки
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
ms.assetid: 35dbfd99-da5a-422b-9b0e-c6caf3b645fa
description: При настройке политик безопасных ссылок анализа может включать действие переопределения не "список URL-адресов, чтобы включить некоторые пользователи в вашей организации на сайтах, которые включены в список.
ms.openlocfilehash: 0ee9c87c90e6e30d6c43fb0de5291dd85b03be07
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782166"
---
# <a name="set-up-a-custom-do-not-rewrite-urls-list-using-office-365-atp-safe-links"></a><span data-ttu-id="457f2-103">Настроить пользовательский список not переопределения URL-адресов с помощью Office 365 ATP безопасных ссылки</span><span class="sxs-lookup"><span data-stu-id="457f2-103">Set up a custom do-not-rewrite URLs list using Office 365 ATP Safe Links</span></span>

<span data-ttu-id="457f2-p101">[Защиту от угроз для Office 365 Advanced](office-365-atp.md) (ATP) ваша организация может иметь [настраиваемые заблокированных URL-адреса](set-up-a-custom-blocked-urls-list-wtih-atp.md), таким образом, когда люди нажмите кнопку на веб-адреса (URL-адреса) в сообщения электронной почты или в некоторых документах Office, они не смогут переход на этих URL-адресов. Организации могут также иметь настраиваемые списки «не rewrite» для определенных групп в организации. Список «не rewrite» позволяет кому посетите URL-адресов, в противном случае — блокирует [ATP безопасных ссылок в Office 365](atp-safe-links.md).</span><span class="sxs-lookup"><span data-stu-id="457f2-p101">With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can have a [custom blocked URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md), such that when people click on web addresses (URLs) in email messages or certain Office documents, they are prevented from going to those URLs. Your organization can also have custom "do not rewrite" lists for specific groups in your organization. A "do not rewrite" list enables some people to visit URLs that are otherwise blocked by [ATP Safe Links in Office 365](atp-safe-links.md).</span></span> 
  
<span data-ttu-id="457f2-107">В этой статье описывается, как для указания списка URL-адресов, исключенных из безопасных ссылок анализа сканирования и некоторые важные моменты, которые следует помнить.</span><span class="sxs-lookup"><span data-stu-id="457f2-107">This article describes how to specify a list of URLs that are excluded from ATP Safe Links scanning, and a few important points to keep in mind.</span></span>

## <a name="set-up-a-do-not-rewrite-list"></a><span data-ttu-id="457f2-108">Настройка списка «не rewrite»</span><span class="sxs-lookup"><span data-stu-id="457f2-108">Set up a "do not rewrite" list</span></span>

<span data-ttu-id="457f2-p102">Защита от безопасных ссылок анализа использует несколько списков, включая черный список URL-адресов вашей организации и списки «не rewrite» для исключения. При наличии необходимых разрешений можно настроить настраиваемых списков «не rewrite». Для этого после добавления или изменения политики безопасных ссылок, которые применяются к определенным получателям в организации.</span><span class="sxs-lookup"><span data-stu-id="457f2-p102">ATP Safe Links protection uses several lists, including your organization's blocked URLs list and the "do not rewrite" lists for exceptions. If you have the necessary permissions, you can set up your custom "do not rewrite" lists. You do this when you add or edit Safe Links policies that apply to specific recipients in your organization.</span></span> 
  
1. <span data-ttu-id="457f2-112">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и войдите с учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="457f2-112">Go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span> 
    
2. <span data-ttu-id="457f2-113">В левой панели навигации в разделе **Управление угроз** \> **политики** \> **Безопасных ссылки**.</span><span class="sxs-lookup"><span data-stu-id="457f2-113">In the left navigation, under **Threat management** \> **Policy** \> **Safe Links**.</span></span>
    
3. <span data-ttu-id="457f2-p103">В разделе **политики, которые применяются к определенным получателям** , нажмите кнопку **Создать** (новой кнопки имеет следующий вид: знак плюс ( **+**)) для создания новой политики. (Кроме того, можно изменить существующую политику.)</span><span class="sxs-lookup"><span data-stu-id="457f2-p103">In the **Policies that apply to specific recipients** section, choose **New** (the New button resembles a plus sign ( **+**)) to create a new policy. (Alternatively, you can edit an existing policy.)</span></span>
    
    ![Нажмите кнопку Создать, чтобы добавить политику безопасных ссылки для конкретных электронной почты получателей](media/01073f42-3cec-4ddb-8c10-4d33ec434676.png)
  
4. <span data-ttu-id="457f2-117">Укажите имя и описание политики.</span><span class="sxs-lookup"><span data-stu-id="457f2-117">Specify a name and description for your policy.</span></span>
    
5. <span data-ttu-id="457f2-118">В разделе **не переопределить следующие URL-адреса** выберите поле **Введите допустимый URL-адрес** и введите URL-адрес и затем нажмите знак плюс (+).</span><span class="sxs-lookup"><span data-stu-id="457f2-118">In the **Do not rewrite the following URLs** section, select the **Enter a valid URL** box, and then type a URL, and then choose the plus sign (+).</span></span> 
    
6. <span data-ttu-id="457f2-p104">В разделе **Применить к** выберите **получатель входит в состав**и выберите группы, которые необходимо включить в политике. Последовательно выберите пункты **Добавить**и затем нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="457f2-p104">In the **Applied To** section, choose **The recipient is a member of**, and then choose the group(s) you want to include in your policy. Choose **Add**, and then choose **OK**.</span></span>
    
7. <span data-ttu-id="457f2-121">Завершив добавление URL-адресов, в правом нижнем углу экрана, выберите команду **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="457f2-121">When you are finished adding URLs, in the lower right corner of the screen, choose **Save**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="457f2-p105">Убедитесь, что для просмотра вашей организации настраиваемый список заблокированных URL-адресов. В разделе [Настройка настраиваемого заблокированных список URL-адресов с помощью безопасных ссылок анализа](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span><span class="sxs-lookup"><span data-stu-id="457f2-p105">Make sure to review your organization's custom list of blocked URLs. See [Set up a custom blocked URLs list using ATP Safe Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).</span></span> 
  
## <a name="important-points-to-keep-in-mind"></a><span data-ttu-id="457f2-124">Важные вопросы, на которые следует помнить</span><span class="sxs-lookup"><span data-stu-id="457f2-124">Important points to keep in mind</span></span>

- <span data-ttu-id="457f2-125">Любые URL-адресов, указанных в список «не rewrite», исключаются из анализа безопасных ссылки сканирования для получателей можно указать.</span><span class="sxs-lookup"><span data-stu-id="457f2-125">Any URLs that you specify in the "do not rewrite" list are excluded from ATP Safe Links scanning for the recipients that you specify.</span></span>
 
- <span data-ttu-id="457f2-p106">При указании список «не rewrite» для политики ATP безопасных ссылок, может включать до трех подстановочные знаки звездочки (\*). Подстановочные знаки (\*) предполагается, что для операций, таких как `contoso.com`, которого не включить явным образом префиксами или дочерние домены, как `http://` или `https://`. Это означает, что записи, такие как `contoso.com` аналогичен `\*contoso.com\*` для списка «не rewrite».</span><span class="sxs-lookup"><span data-stu-id="457f2-p106">When you specify a "do not rewrite" list for an ATP Safe Links policy, you can include up to three wildcard asterisks (\*). Wildcards (\*) are assumed for entries such as `contoso.com`, which do not explicitly include prefixes or subdomains, like `http://` or `https://`. This means an entry, such as `contoso.com` is similar to `\*contoso.com\*` for your "do not rewrite" list.</span></span>

- <span data-ttu-id="457f2-p107">Если уже имеется список URL-адресов в списке «не rewrite», обязательно просмотрите этот список и добавьте подстановочные знаки соответствующим образом. Например, если имеется существующий список запись, например `http://contoso.com/a` и вы хотите включить субконтуров как `http://contoso.com/a/b` в политике, добавьте подстановочный знак в запись, чтобы он выглядел, как `http://contoso.com/a\*`.</span><span class="sxs-lookup"><span data-stu-id="457f2-p107">If you already have a list of URLs in your "do not rewrite" list, make sure to review that list and add wildcards as appropriate. For example, if your existing list has an entry like `http://contoso.com/a` and you want to include subpaths like `http://contoso.com/a/b` in your policy, add a wildcard to your entry so it looks like `http://contoso.com/a\*`.</span></span>
    
- <span data-ttu-id="457f2-p108">Не включайте в URL-адресов, указанных в списке «не rewrite» косую черту (/). Например вместо ввода `contoso.com/` в список «не rewrite» введите `contoso.com`.</span><span class="sxs-lookup"><span data-stu-id="457f2-p108">Do not include a forward slash (/) in the URLs that you specify in your "do not rewrite" list. For example, rather than enter `contoso.com/` in your "do not rewrite" list, enter `contoso.com`.</span></span>
    
<span data-ttu-id="457f2-133">В следующих примерах списков в таблице можно ввести и что в силу эти записи имеют.</span><span class="sxs-lookup"><span data-stu-id="457f2-133">The following table lists examples of what you can enter and what effect those entries have.</span></span>
    
|<span data-ttu-id="457f2-134">**Пример записи**</span><span class="sxs-lookup"><span data-stu-id="457f2-134">**Example Entry**</span></span>|<span data-ttu-id="457f2-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="457f2-135">**What It Does**</span></span>|
|:-----|:-----|
|`\*contoso.com\*`  <br/> |<span data-ttu-id="457f2-136">Позволяет определенным получателям посетите домена, поддомены и пути, такие как `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, или`http://www.contoso.com/a`</span><span class="sxs-lookup"><span data-stu-id="457f2-136">Allows specific recipients to visit a domain, subdomains, and paths, such as `http://www.contoso.com`, `https://www.contoso.com`, `https://maps.contoso.com`, or `http://www.contoso.com/a`</span></span>  <br/> |
|`http://contoso.com/a`  <br/> |<span data-ttu-id="457f2-137">Позволяет определенным получателям, посетите веб-сайт как `http://contoso.com/a`, но не субконтуров`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="457f2-137">Allows specific recipients to visit a site like `http://contoso.com/a`, but not subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
|`http://contoso.com/a\*`  <br/> |<span data-ttu-id="457f2-138">Позволяет определенным получателям, посетите веб-сайт как `http://contoso.com/a` и субконтуров, например`http://contoso.com/a/b`</span><span class="sxs-lookup"><span data-stu-id="457f2-138">Allows specific recipients to visit a site like `http://contoso.com/a` and subpaths like `http://contoso.com/a/b`</span></span>  <br/> |
   
  

## <a name="related-topics"></a><span data-ttu-id="457f2-139">Смежные темы</span><span class="sxs-lookup"><span data-stu-id="457f2-139">Related topics</span></span>

[<span data-ttu-id="457f2-140">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="457f2-140">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="457f2-141">Безопасно ATP ссылок в Office 365</span><span class="sxs-lookup"><span data-stu-id="457f2-141">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="457f2-142">Настройка политик ATP безопасных ссылок в Office 365</span><span class="sxs-lookup"><span data-stu-id="457f2-142">Set up ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
  
[<span data-ttu-id="457f2-143">Настройка пользовательских заблокированных список URL-адресов с помощью безопасных ссылок анализа</span><span class="sxs-lookup"><span data-stu-id="457f2-143">Set up a custom blocked URLs list using ATP Safe Links</span></span>](set-up-a-custom-blocked-urls-list-wtih-atp.md)

[<span data-ttu-id="457f2-144">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="457f2-144">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="457f2-145">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="457f2-145">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

