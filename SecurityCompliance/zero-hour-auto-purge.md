---
title: Автоматическая очистка для защиты от спама и вредоносных программ
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: Автоматическая очистка (ZAP) с нулевым временем (ZAP) — это функция защиты электронной почты, которая обнаруживает сообщения с нежелательной почтой или вредоносной программой, которая уже доставляется в ящики "Входящие" пользователя, а затем отрисовывает вредоносный контент. Принцип работы ZAP зависит от типа обнаруженного вредоносного содержимого.
ms.openlocfilehash: 7a357b50a75012408d6958ce528fddf8c203540a
ms.sourcegitcommit: e24f70699021c4f4ba56508ad0afb6f65010c357
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2019
ms.locfileid: "31479635"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="3569b-104">Автоматическая очистка для защиты от спама и вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="3569b-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="3569b-105">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="3569b-105">Overview</span></span>

<span data-ttu-id="3569b-106">Автоматическая очистка (ZAP) с нулевым временем (ZAP) — это функция защиты электронной почты, которая определяет сообщения с помощью фишинга, спама или вредоносных программ, которые уже были доставлены в папки "Входящие" пользователя, а затем отрисовывает вредоносный контент.</span><span class="sxs-lookup"><span data-stu-id="3569b-106">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless.</span></span> <span data-ttu-id="3569b-107">Принцип работы ZAP зависит от типа обнаруженного вредоносного содержимого; почта может быть заппед из-за содержимого почты, URL-адресов или вложений.</span><span class="sxs-lookup"><span data-stu-id="3569b-107">How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="3569b-108">ZAP доступен по умолчанию для Exchange Online Protection, которая входит в состав любой подписки на Office 365, содержащей почтовые ящики Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="3569b-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="3569b-109">ZAP включен по умолчанию, но должны быть выполнены следующие условия:</span><span class="sxs-lookup"><span data-stu-id="3569b-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="3569b-110">Для **действия спама** задано **Перемещение сообщения в папку**"Нежелательная почта".</span><span class="sxs-lookup"><span data-stu-id="3569b-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <span data-ttu-id="3569b-111">Вы также можете создать новую политику фильтрации нежелательной почты, которая применяется только к набору пользователей, если вы не хотите, чтобы все почтовые ящики были на экране ZAP.</span><span class="sxs-lookup"><span data-stu-id="3569b-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="3569b-112">Пользователи сохраняли параметры нежелательной почты по умолчанию и не отключили защиту от нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="3569b-112">Users have kept their default junk mail settings, and have not turned off junk email protection.</span></span> <span data-ttu-id="3569b-113">(См. [изменение уровня защиты в фильтре нежелательной почты](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) для получения сведений о параметрах пользователя в Outlook).</span><span class="sxs-lookup"><span data-stu-id="3569b-113">(See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-zap-works"></a><span data-ttu-id="3569b-114">Как работает ZAP</span><span class="sxs-lookup"><span data-stu-id="3569b-114">How ZAP works</span></span>

<span data-ttu-id="3569b-115">Office 365 обновляет антивирусную подсистему и сигнатуры вредоносных программ в режиме реального времени ежедневно.</span><span class="sxs-lookup"><span data-stu-id="3569b-115">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis.</span></span> <span data-ttu-id="3569b-116">Тем не менее, пользователи могут по-прежнему получать вредоносные сообщения, доставляемые в свои папки "Входящие" по ряду причин, в том числе если контент веапонизед после доставки пользователям.</span><span class="sxs-lookup"><span data-stu-id="3569b-116">However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users.</span></span> <span data-ttu-id="3569b-117">ZAP решает эту функцию, постоянно отслеживая обновления подписей спама и вредоносных программ Office 365.</span><span class="sxs-lookup"><span data-stu-id="3569b-117">ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures.</span></span> <span data-ttu-id="3569b-118">ZAP может находить и удалять ранее доставленные сообщения, которые уже находятся в папках "Входящие" пользователей.</span><span class="sxs-lookup"><span data-stu-id="3569b-118">ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span>

- <span data-ttu-id="3569b-119">Для почты, которая определена как спам, ZAP перемещает непрочитанные сообщения в папку неЖелательной почты пользователей.</span><span class="sxs-lookup"><span data-stu-id="3569b-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span>

- <span data-ttu-id="3569b-120">Для почты, идентифицированной как фишинг, ZAP перемещает сообщения в папку неЖелательной почты пользователей независимо от того, было ли Прочитано электронное письмо.</span><span class="sxs-lookup"><span data-stu-id="3569b-120">For mail that is identified as phish, ZAP moves messages to users' Junk mail folder, regardless of whether the email has been read.</span></span>

- <span data-ttu-id="3569b-121">Для недавно обнаруженных вредоносных программ ZAP удаляет вложения из сообщений электронной почты независимо от того, было ли Прочитано электронное письмо.</span><span class="sxs-lookup"><span data-stu-id="3569b-121">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span>
  
<span data-ttu-id="3569b-122">Команда ZAP легко работает для пользователя почтового ящика; они не уведомляются при перемещении сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3569b-122">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="3569b-123">Разрешения для списков, [правил для почтового процесса](https://go.microsoft.com/fwlink/p/?LinkId=722755)и конечных пользователей, а также дополнительные фильтры имеют приоритет перед ZAP.</span><span class="sxs-lookup"><span data-stu-id="3569b-123">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="3569b-124">Просмотр или Настройка политики фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="3569b-124">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="3569b-125">Перейдите к [https://protection.office.com](https://protection.office.com) рабочей или учебной учетной записи Office 365 и войдите в нее с помощью рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3569b-125">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="3569b-126">В разделе **Управление угрозой**выберите пункт **Защита от нежелательной почты**.</span><span class="sxs-lookup"><span data-stu-id="3569b-126">Under **Threat management**, choose **Anti-spam**.</span></span>

3. <span data-ttu-id="3569b-127">Просмотрите стандартные параметры.</span><span class="sxs-lookup"><span data-stu-id="3569b-127">Review the standard settings.</span></span>

4. <span data-ttu-id="3569b-128">Если вы хотите настроить параметры, выберите вкладку Настраиваемый \*\*\*\* и включите **Настраиваемые параметры**.</span><span class="sxs-lookup"><span data-stu-id="3569b-128">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**.</span></span> <span data-ttu-id="3569b-129">Измените параметры и при необходимости нажмите кнопку **+ создать политику** , чтобы добавить новую политику.</span><span class="sxs-lookup"><span data-stu-id="3569b-129">Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span>

## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="3569b-130">Просмотр сообщения об перемещении ZAP</span><span class="sxs-lookup"><span data-stu-id="3569b-130">To see if ZAP moved your message</span></span>

<span data-ttu-id="3569b-131">Если вы хотите узнать, перенесли ли сообщение ZAP, вы можете использовать [отчет о состоянии защиты от угроз](view-email-security-reports.md#threat-protection-status-report) (или [Обозреватель угроз](use-explorer-in-security-and-compliance.md)).</span><span class="sxs-lookup"><span data-stu-id="3569b-131">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>

## <a name="to-disable-zap"></a><span data-ttu-id="3569b-132">Чтобы отключить ZAP</span><span class="sxs-lookup"><span data-stu-id="3569b-132">To disable ZAP</span></span>
  
<span data-ttu-id="3569b-133">Если вы хотите отключить ZAP для клиента Office 365 или группы пользователей, используйте параметр **запенаблед** командлета [Set HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), командлета EOP.</span><span class="sxs-lookup"><span data-stu-id="3569b-133">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>

<span data-ttu-id="3569b-134">В следующем примере ZAP отключен для политики фильтрации содержимого с именем "Test".</span><span class="sxs-lookup"><span data-stu-id="3569b-134">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>

```Powershell
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="3569b-135">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="3569b-135">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="3569b-136">Что произойдет при перемещении законного сообщения в папку "Нежелательная почта"?</span><span class="sxs-lookup"><span data-stu-id="3569b-136">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="3569b-137">Для [ложных срабатываний](prevent-email-from-being-marked-as-spam.md)необходимо следовать обычным процессам отчетов.</span><span class="sxs-lookup"><span data-stu-id="3569b-137">You should follow the normal reporting process for [false-positives](prevent-email-from-being-marked-as-spam.md).</span></span> <span data-ttu-id="3569b-138">Единственная причина, по которой сообщение было бы перемещено из папки "Входящие" в папку нежелательной почты, будет вызвано тем, что эта служба определила, что сообщение является спамом или вредоносным.</span><span class="sxs-lookup"><span data-stu-id="3569b-138">The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="3569b-139">Что делать, если вместо папки нежелательной почты используется карантин Office 365?</span><span class="sxs-lookup"><span data-stu-id="3569b-139">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="3569b-140">ZAP не перемещает сообщения в карантин из папки "Входящие" в данный момент.</span><span class="sxs-lookup"><span data-stu-id="3569b-140">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="3569b-141">Что делать, если вы создали правило для обработки почтового процесса (Block/Allow Rule)?</span><span class="sxs-lookup"><span data-stu-id="3569b-141">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="3569b-142">Правила, созданные администраторами (правила для почтового процесса) или блокировать и разРешать правила, имеют приоритет.</span><span class="sxs-lookup"><span data-stu-id="3569b-142">Rules created by admins (mail flow rules) or Block and Allow rules take precedence.</span></span> <span data-ttu-id="3569b-143">Такие сообщения исключаются из критериев функции, поэтому потоки обработки почты будут следовать действию правила (Block/Allow Rule).</span><span class="sxs-lookup"><span data-stu-id="3569b-143">Such messages are excluded from the feature criteria so the mail flow will follow the rule action (Block/Allow Rule).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="3569b-144">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3569b-144">Related Topics</span></span>

[<span data-ttu-id="3569b-145">Защита от нежелательной электронной почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="3569b-145">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="3569b-146">Блокирование спама с помощью фильтра нежелательной почты Office 365 для предотвращения ошибочных результатов</span><span class="sxs-lookup"><span data-stu-id="3569b-146">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](reduce-spam-email.md)