---
title: Автоматическая очистка для защиты от нежелательной почты и вредоносных программ
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
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
ms.openlocfilehash: 1e90e69018b7640bb36011287abd5bcd77d43358
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749323"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="1edf2-104">Автоматическая очистка для защиты от нежелательной почты и вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="1edf2-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="1edf2-105">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1edf2-105">Overview</span></span>

<span data-ttu-id="1edf2-p102">Критическую автоматически очищать (ZAP) — это функция защиты электронной почты, которая определяет сообщения с ловят нежелательной почты и вредоносных программ, которые уже были доставлены для почтовых ящиков пользователей, а затем отображает сообщение о нежелательном содержимое безопасным. Как ZAP это зависит от вредоносного содержимого обнаружено; почта может zapped из-за содержимое электронной почты, URL-адреса или вложения.</span><span class="sxs-lookup"><span data-stu-id="1edf2-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="1edf2-108">ZAP доступен по умолчанию Exchange Online Protection, который входит в состав любого подписки Office 365, который содержит почтовые ящики Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="1edf2-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="1edf2-109">ZAP включен по умолчанию, но должны быть выполнены следующие условия:</span><span class="sxs-lookup"><span data-stu-id="1edf2-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="1edf2-110">**Действие нежелательной почты** присвоено значение **переместить сообщение в папку нежелательной почты**.</span><span class="sxs-lookup"><span data-stu-id="1edf2-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <br/><span data-ttu-id="1edf2-111">Кроме того, можно создать новую политику фильтра нежелательной почты, который применяется только к определенным пользователям, если вы не хотите всех почтовых ящиков в экранироваться с ZAP.</span><span class="sxs-lookup"><span data-stu-id="1edf2-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="1edf2-p103">Пользователи хранится по умолчанию параметров нежелательной почты и защиты от нежелательной почты не отключаются. (Увидеть [можно изменить уровень защиты фильтра нежелательной почты](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) для получения дополнительных сведений о параметрах пользователя в Outlook).</span><span class="sxs-lookup"><span data-stu-id="1edf2-p103">Users have kept their default junk mail settings, and have not turned off junk email protection. (See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-does-zap-work"></a><span data-ttu-id="1edf2-114">Каков принцип работы ZAP?</span><span class="sxs-lookup"><span data-stu-id="1edf2-114">How does ZAP work?</span></span>

<span data-ttu-id="1edf2-p104">Обновления Microsoft Office 365 подписи подсистемы и вредоносных программ защиты от нежелательной почты в режиме реального времени на ежедневной основе. Тем не менее пользователи могут получить сообщение о нежелательном сообщения, доставленные в их почтовые ящики для различных причинам, например, если содержимое является weaponized после доставки для пользователей. Удалите адреса, при этом наблюдая за постоянно обновляется подписей нежелательной почты и вредоносных программ Office 365. ZAP можно найти и удалить ранее отправки сообщений, которые уже в почтовые ящики пользователей.</span><span class="sxs-lookup"><span data-stu-id="1edf2-p104">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures. ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span> 

- <span data-ttu-id="1edf2-119">Для почты, помечаются как нежелательная почта ZAP перемещается непрочитанных сообщений в папку нежелательной почты пользователей.</span><span class="sxs-lookup"><span data-stu-id="1edf2-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span> 

- <span data-ttu-id="1edf2-120">Для почты, помечаются как нежелательная почта ZAP перемещает сообщения в папку нежелательной почты пользователей, независимо от того, является ли прочитано сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1edf2-120">For mail that is identified as spam, ZAP moves messages to users' Junk mail folder, regardless of whether the email has been read.</span></span>

- <span data-ttu-id="1edf2-121">Для недавно обнаруженных вредоносных программ ZAP удаляет вложения в сообщениях электронной почты, независимо от того, является ли прочитано сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1edf2-121">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span> 
  
<span data-ttu-id="1edf2-122">Действие ZAP не вызывает затруднений для пользователя почтового ящика. они не будут уведомлены при перемещении сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1edf2-122">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="1edf2-123">Разрешить списки, [правила потока почты](https://go.microsoft.com/fwlink/p/?LinkId=722755)и правил конечного пользователя или дополнительные фильтры, имеют приоритет перед ZAP.</span><span class="sxs-lookup"><span data-stu-id="1edf2-123">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="1edf2-124">Для просмотра или настройки политики фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="1edf2-124">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="1edf2-125">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы для Office 365.</span><span class="sxs-lookup"><span data-stu-id="1edf2-125">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="1edf2-126">В разделе **Управление угроз**выберите **защиты от нежелательной почты**.</span><span class="sxs-lookup"><span data-stu-id="1edf2-126">Under **Threat management**, choose **Anti-spam**.</span></span>

3. <span data-ttu-id="1edf2-127">Просмотрите стандартных параметров.</span><span class="sxs-lookup"><span data-stu-id="1edf2-127">Review the standard settings.</span></span> 

4. <span data-ttu-id="1edf2-p105">Если вы хотите настроить параметры, перейдите на вкладку **настраиваемые** и включить **пользовательские параметры**. Измените параметры и, выберите **+ Создать политику** для добавления новой политики.</span><span class="sxs-lookup"><span data-stu-id="1edf2-p105">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**. Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span> 
    
## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="1edf2-130">Чтобы увидеть, если ZAP перемещены в сообщение</span><span class="sxs-lookup"><span data-stu-id="1edf2-130">To see if ZAP moved your message</span></span>

<span data-ttu-id="1edf2-131">Если вы хотите просмотреть, если ZAP перемещены в сообщение, можно использовать либо [отчет о состоянии защиты от угроз](view-email-security-reports.md#threat-protection-status-report) (или [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span><span class="sxs-lookup"><span data-stu-id="1edf2-131">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>
    
## <a name="to-disable-zap"></a><span data-ttu-id="1edf2-132">Чтобы отключить ZAP</span><span class="sxs-lookup"><span data-stu-id="1edf2-132">To disable ZAP</span></span>
  
<span data-ttu-id="1edf2-133">Если вы хотите отключить удалите для клиента Office 365 или группы пользователей, используйте параметр **ZapEnabled** [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), это командлет EOP.</span><span class="sxs-lookup"><span data-stu-id="1edf2-133">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
<span data-ttu-id="1edf2-134">В следующем примере ZAP отключена для политики фильтрации содержимого с именем «Test».</span><span class="sxs-lookup"><span data-stu-id="1edf2-134">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="1edf2-135">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="1edf2-135">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="1edf2-136">Что произойдет, если допустимых сообщение перемещается в папку нежелательной почты?</span><span class="sxs-lookup"><span data-stu-id="1edf2-136">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="1edf2-p106">Необходимо соблюдать обычный процесс работы с отчетами для ложных срабатываний. Единственная причина сообщение будет перемещено из папки «Входящие» в папку нежелательной почты равен так как служба определила, что сообщение являлось нежелательным или намеренного.</span><span class="sxs-lookup"><span data-stu-id="1edf2-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="1edf2-139">Что делать, если использовать в Office 365 карантин вместо папки нежелательной почты?</span><span class="sxs-lookup"><span data-stu-id="1edf2-139">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="1edf2-140">ZAP не перемещать сообщения в карантин из папки «Входящие» в данный момент.</span><span class="sxs-lookup"><span data-stu-id="1edf2-140">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="1edf2-141">Что делать, если имеется правило порядка настраиваемых почты (блокировать / разрешить правила)?</span><span class="sxs-lookup"><span data-stu-id="1edf2-141">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="1edf2-p107">Правила, созданные "Администраторы" (правила потока обработки почты) или блокировки и разрешить правил, имеют приоритет. Такие сообщения, исключаются из условий компонента.</span><span class="sxs-lookup"><span data-stu-id="1edf2-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="1edf2-144">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1edf2-144">Related Topics</span></span>

[<span data-ttu-id="1edf2-145">Защита от спама в Office 365</span><span class="sxs-lookup"><span data-stu-id="1edf2-145">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="1edf2-146">Блокировка спама с помощью фильтра нежелательной почты Office 365 для предотвращения ошибочных результатов</span><span class="sxs-lookup"><span data-stu-id="1edf2-146">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

