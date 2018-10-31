---
title: Автоматическая очистка для защиты от нежелательной почты и вредоносных программ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: Критическую автоматически очищать (ZAP) — это функция защиты электронной почты, которая определяет сообщения с нежелательной почты и вредоносных программ, которые уже были доставлены для почтовых ящиков пользователей, а затем отображает сообщение о нежелательном содержимое безопасным. Как ZAP это зависит от типа обнаруженных вредоносных содержимого.
ms.openlocfilehash: dabe4caf8916d3f0de7a70cb3d056dd9a7fdcc3f
ms.sourcegitcommit: ceb70ea863d8b97afea077a04fc7ec612b870695
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25857247"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="5bc65-104">Автоматическая очистка для защиты от нежелательной почты и вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="5bc65-104">Zero-hour auto purge - protection against spam and malware</span></span>

<span data-ttu-id="5bc65-p102">Критическую автоматически очищать (ZAP) — это функция защиты электронной почты, которая определяет сообщения с нежелательной почты и вредоносных программ, которые уже были доставлены для почтовых ящиков пользователей, а затем отображает сообщение о нежелательном содержимое безопасным. Как ZAP это зависит от типа обнаруженных вредоносных содержимого.</span><span class="sxs-lookup"><span data-stu-id="5bc65-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with spam or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected.</span></span>
  
<span data-ttu-id="5bc65-107">ZAP доступен по умолчанию Exchange Online Protection, который входит в состав любого подписки Office 365, который содержит почтовые ящики Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="5bc65-107">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>
  
## <a name="how-does-zap-work"></a><span data-ttu-id="5bc65-108">Каков принцип работы ZAP?</span><span class="sxs-lookup"><span data-stu-id="5bc65-108">How does ZAP work?</span></span>

<span data-ttu-id="5bc65-p103">Обновления Microsoft Office 365 подписи подсистемы и вредоносных программ защиты от нежелательной почты в режиме реального времени на ежедневной основе. Тем не менее пользователи могут получить сообщение о нежелательном сообщения, доставленные в их почтовые ящики для различных причин, в том числе контент был weaponized во время после сначала доставки для пользователей. Удалите адреса, при этом наблюдая за постоянно обновляется подписей нежелательной почты и вредоносных программ Office 365, таким образом и позволяет уже удалить ранее полученным сообщения из папки "Входящие". Для почты, который уже был распознан как нежелательная почта ZAP перемещает непрочитанных сообщений в папку нежелательной почты. Для недавно обнаруженных вредоносных программ ZAP удаляет вложения из сообщения электронной почты, независимо от того, ли почта была чтение или нет. Для сообщений, которые были неправильно классифицированных как вредоносный верно обратное.</span><span class="sxs-lookup"><span data-stu-id="5bc65-p103">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including when the content was weaponized at a time after it was first delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures, and can therefore find and remove previously delivered messages already in inboxes. For mail that was already identified as spam, ZAP moves unread messages to the user's Junk mail folder. For newly detected malware, ZAP removes the attachments from the email message, regardless of whether the mail was read or not. The reverse is true for messages that were incorrectly classified as malicious.</span></span>
  
<span data-ttu-id="5bc65-115">Для пользователя почтового ящика, он или она не получает уведомление, почта была перемещена ZAP действие не вызывает затруднений.</span><span class="sxs-lookup"><span data-stu-id="5bc65-115">The ZAP action is seamless for the mailbox user, he or she is not notified the mail has been moved.</span></span>
  
<span data-ttu-id="5bc65-116">Разрешить списки, [правила потока почты](https://go.microsoft.com/fwlink/p/?LinkId=722755)и правил конечного пользователя или дополнительные фильтры, имеют приоритет перед ZAP.</span><span class="sxs-lookup"><span data-stu-id="5bc65-116">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
 <span data-ttu-id="5bc65-117">**В этой статье**</span><span class="sxs-lookup"><span data-stu-id="5bc65-117">**In this article:**</span></span>
  
> [<span data-ttu-id="5bc65-118">Настройка политики фильтров нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="5bc65-118">Set spam filter policy</span></span>](zero-hour-auto-purge.md#BK_SetSpam)
    
> [<span data-ttu-id="5bc65-119">Просматривать, если ZAP перемещены в сообщение</span><span class="sxs-lookup"><span data-stu-id="5bc65-119">See if ZAP moved your message</span></span>](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [<span data-ttu-id="5bc65-120">Отключение ZAP</span><span class="sxs-lookup"><span data-stu-id="5bc65-120">Disable ZAP</span></span>](zero-hour-auto-purge.md#BK_Posh)
    
> [<span data-ttu-id="5bc65-121">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="5bc65-121">FAQ</span></span>](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a><span data-ttu-id="5bc65-122">Работа с ZAP</span><span class="sxs-lookup"><span data-stu-id="5bc65-122">Working with ZAP</span></span>

<span data-ttu-id="5bc65-123">ZAP включен по умолчанию, но необходимо убедитесь, что выполнены два условия:</span><span class="sxs-lookup"><span data-stu-id="5bc65-123">ZAP is turned on by default, but you do have to make sure a couple of conditions are met:</span></span>
  
- <span data-ttu-id="5bc65-124">Политики фильтрации нежелательной почты устанавливается для [перемещения сообщений в папку нежелательной почты](zero-hour-auto-purge.md#BK_SetSpam).</span><span class="sxs-lookup"><span data-stu-id="5bc65-124">Spam filter policy is set to [Move message to Junk Email folder](zero-hour-auto-purge.md#BK_SetSpam).</span></span>
    
    <span data-ttu-id="5bc65-125">Кроме того, можно создать новую политику фильтра нежелательной почты, который применяется только к определенным пользователям, если вы не хотите всех почтовых ящиков в экранироваться с ZAP.</span><span class="sxs-lookup"><span data-stu-id="5bc65-125">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>
    
- <span data-ttu-id="5bc65-126">Пользователя [Параметры \> Нежелательная почта](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span><span class="sxs-lookup"><span data-stu-id="5bc65-126">The user's [Options \> Junk Email](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span></span>
    
<span data-ttu-id="5bc65-127">Если вы хотите [просмотреть, если ZAP перемещены в сообщение](zero-hour-auto-purge.md#BK_DidZAPMove), можно использовать средства трассировки сообщений Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="5bc65-127">If you want [to see if ZAP moved your message](zero-hour-auto-purge.md#BK_DidZAPMove), you can use the Exchange Online message trace tool.</span></span>
  
<span data-ttu-id="5bc65-128">Администраторы могут также [Отключить ZAP](zero-hour-auto-purge.md#BK_Posh) с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5bc65-128">Admins can also [disable ZAP](zero-hour-auto-purge.md#BK_Posh) by using PowerShell.</span></span> 
  
 <span data-ttu-id="5bc65-129">**Чтобы задать политику фильтрации нежелательной почты**</span><span class="sxs-lookup"><span data-stu-id="5bc65-129">**To set spam filter policy**</span></span>
  
1. <span data-ttu-id="5bc65-130">Войдите в [Where для входа в Office 365 для бизнеса](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) и выберите **защиты** \> **фильтра нежелательной почты**.</span><span class="sxs-lookup"><span data-stu-id="5bc65-130">Sign in to the [Where to sign in to Office 365 for business](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) and choose **protection** \> **spam filter**.</span></span> 
    
    ![В центре администрирования Exchange выберите защиты, а затем защиты от нежелательной почты фильтра](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. <span data-ttu-id="5bc65-132">Выберите политику фильтрации, который требуется настроить, либо нажмите кнопку **Добавить**![значком Добавить](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) для создания нового.</span><span class="sxs-lookup"><span data-stu-id="5bc65-132">Either choose the filter policy you want to adjust, or choose **add**![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) to create a new one.</span></span> 
    
    <span data-ttu-id="5bc65-p104">В приведенном выше снимке экрана политику с именем «По умолчанию», но при создании политики фильтрации нежелательной почты дополнительные следует сообщить другое имя. Также можно применить политику к только ограниченный набор пользователей.</span><span class="sxs-lookup"><span data-stu-id="5bc65-p104">In the previous screen shot, the policy is named "Default", but if you create additional spam filter policies you can give them a different name. You can also apply the policy to only a limited set of users.</span></span>
    
3. <span data-ttu-id="5bc65-135">В окне политики выберите **нежелательной почты и массовых действия**и убедитесь в том, что **нежелательной почты** задано значение **переместить сообщение в папку нежелательной почты**.</span><span class="sxs-lookup"><span data-stu-id="5bc65-135">In the policy window, choose **spam and bulk actions**, and make sure that **Spam** is set to **Move message to Junk Email folder**.</span></span> 
    
    <span data-ttu-id="5bc65-136">Если вы решили **Сохранить** политику применяется к клиенту Office 365.</span><span class="sxs-lookup"><span data-stu-id="5bc65-136">If you choose **Save** at this point, the policy applies to your Office 365 tenant.</span></span> 
    
    ![Задать нежелательной почты и действия, чтобы переместить сообщение в папку нежелательной почты в пакетном режиме](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. <span data-ttu-id="5bc65-p105">Если вы создали новую политику и требуется применить политику для группы пользователей, прокрутки раздел **Применяется к** в окне Политика фильтра и в элементах управления меню выберите **получателей**, **домена**или **группах** вы необходимо применить политику. Также можно настроить дополнительные условия и исключения.</span><span class="sxs-lookup"><span data-stu-id="5bc65-p105">If you created a new policy, and you want to apply the policy to only a set of users, scroll to the **Applied To** section in the policy filter window, and in the menu controls choose the **recipients**, **domain**, or **group memberships** you want to apply the policy to. You can also set additional conditions and exceptions.</span></span> 
    
    ![Применяется в разделе Выбор получателей](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    <span data-ttu-id="5bc65-141">Нажмите кнопку **Сохранить** , чтобы применить политику для выбранных пользователей.</span><span class="sxs-lookup"><span data-stu-id="5bc65-141">Choose **Save** to apply the policy to the selected users.</span></span> 
    
 <span data-ttu-id="5bc65-142">**Чтобы увидеть, если ZAP перемещены в сообщение**</span><span class="sxs-lookup"><span data-stu-id="5bc65-142">**To see if ZAP moved your message**</span></span>
  
- <span data-ttu-id="5bc65-143">[Поиск и исправление проблем доставки электронной почты в Office 365 для бизнеса администрирования](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) можно использовать для определения, если сообщение перемещено с ZAP:</span><span class="sxs-lookup"><span data-stu-id="5bc65-143">You can use the [Find and fix email delivery issues as an Office 365 for business admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) to determine if the message was moved by ZAP:</span></span> 
    
    <span data-ttu-id="5bc65-144">Поиска в вашей сведений трассировки для идентификации сообщение, в котором был перемещен, ZAP текста «критическую Автоматическая очистка (ZAP)».</span><span class="sxs-lookup"><span data-stu-id="5bc65-144">Look for the text "Zero-Hour Auto Purge (ZAP)" in your trace details to identify a message that was moved by ZAP.</span></span>
    
 <span data-ttu-id="5bc65-145">**Чтобы отключить ZAP**</span><span class="sxs-lookup"><span data-stu-id="5bc65-145">**To disable ZAP**</span></span>
  
- <span data-ttu-id="5bc65-146">Если вы хотите отключить удалите для клиента Office 365 или группы пользователей, используйте параметр **ZapEnabled** [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), это командлет EOP.</span><span class="sxs-lookup"><span data-stu-id="5bc65-146">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
    <span data-ttu-id="5bc65-147">В следующем примере ZAP отключена для политики фильтрации содержимого с именем «Test».</span><span class="sxs-lookup"><span data-stu-id="5bc65-147">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a><span data-ttu-id="5bc65-148">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="5bc65-148">FAQ</span></span>
<span data-ttu-id="5bc65-149"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="5bc65-149"></span></span>

 <span data-ttu-id="5bc65-150">**Что произойдет, если допустимых сообщение перемещается в папку нежелательной почты?**</span><span class="sxs-lookup"><span data-stu-id="5bc65-150">**What happens if a legitimate message is moved to the junk mail folder?**</span></span>
  
<span data-ttu-id="5bc65-p106">Необходимо соблюдать обычный процесс работы с отчетами для ложных срабатываний. Единственная причина сообщение будет перемещено из папки «Входящие» в папку нежелательной почты равен так как служба определила, что сообщение являлось нежелательным или намеренного.</span><span class="sxs-lookup"><span data-stu-id="5bc65-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
 <span data-ttu-id="5bc65-153">**Что делать, если использовать в Office 365 карантин вместо папки нежелательной почты?**</span><span class="sxs-lookup"><span data-stu-id="5bc65-153">**What if I use the Office 365 quarantine instead of the junk mail folder?**</span></span>
  
<span data-ttu-id="5bc65-154">ZAP не перемещать сообщения в карантин из папки «Входящие» в данный момент.</span><span class="sxs-lookup"><span data-stu-id="5bc65-154">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
 <span data-ttu-id="5bc65-155">**Что делать, если имеется правило порядка настраиваемых почты (блокировать / разрешить правила)?**</span><span class="sxs-lookup"><span data-stu-id="5bc65-155">**What If I have a custom mail flow rule (Block/ Allow Rule)?**</span></span>
  
<span data-ttu-id="5bc65-p107">Правила, созданные "Администраторы" (правила потока обработки почты) или блокировки и разрешить правил, имеют приоритет. Такие сообщения, исключаются из условий компонента.</span><span class="sxs-lookup"><span data-stu-id="5bc65-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="5bc65-158">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5bc65-158">Related Topics</span></span>
<span data-ttu-id="5bc65-159"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="5bc65-159"></span></span>

[<span data-ttu-id="5bc65-160">Защита от спама в Office 365</span><span class="sxs-lookup"><span data-stu-id="5bc65-160">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="5bc65-161">Блокировка спама с помощью фильтра нежелательной почты Office 365 для предотвращения ошибочных результатов</span><span class="sxs-lookup"><span data-stu-id="5bc65-161">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

