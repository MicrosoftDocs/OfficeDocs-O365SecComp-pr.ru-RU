---
title: Просмотр отчетов, передаваемых пользователями в Майкрософт, с помощью правил для потока обработки почты
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Вы можете создать правило транспорта Exchange, чтобы пользователи не могли отправлять сообщения электронной почты в корпорацию Майкрософт для анализа и использовать их в собственных процессах безопасности.
ms.openlocfilehash: 7ee8fb2bca1071ccd4080379485c1670a5e66a73
ms.sourcegitcommit: 06d6e63225f912d0f3c6bb836c61eb11c1dbe97a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/22/2019
ms.locfileid: "30206412"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="46f86-103">Просмотр отчетов, передаваемых пользователями в Майкрософт, с помощью правил для потока обработки почты</span><span class="sxs-lookup"><span data-stu-id="46f86-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="46f86-p101">Существует несколько способов отправки ложных положительных и ложных отрицательных сообщений в корпорацию Майкрософт для анализа. Как администратор вы можете использовать правила для обработки почтового ящика, чтобы увидеть, что пользователи отправляют отчеты корпорации Майкрософт в качестве спама, нежелательной почты и фишинговых мошенничествов. Дополнительные сведения о том, [как отправлять сообщения о нежелательной почте и мошеннических сообщениях в корпорацию Майкрософт для анализа](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Кроме того, вы можете создать правило транспорта Exchange, чтобы пользователи не могли отправлять сообщения электронной почты в корпорацию Майкрософт для анализа и использовать их в собственных процессах безопасности.</span><span class="sxs-lookup"><span data-stu-id="46f86-p101">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis. As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Conversely, you can create an Exchange Transport rule to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="46f86-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="46f86-108">What do you need to know before you begin?</span></span>

<span data-ttu-id="46f86-109">Предполагаемое время для завершения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="46f86-109">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="46f86-p102">Перед выполнением этой процедуры или процедур необходимо назначить разрешения. В разделе "правила транспорта" в разделе "правила транспорта" в разделе " [политики обмена сообщениями и соответствия требованиям](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) " и в разделе "политики почтовых ящиков Outlook в Интернете" в разделе [clients and Mobile Devices Permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) .</span><span class="sxs-lookup"><span data-stu-id="46f86-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook on the web mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="46f86-112">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="46f86-112">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="46f86-113">Создание правила для потока обработки почты для просмотра отправляемых пользователями отчетов о спаме, фишинге и не спаме в Центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="46f86-113">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>

1. <span data-ttu-id="46f86-114">В Центре администрирования Exchange последовательно выберите пункты **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="46f86-114">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="46f86-115">Щелкните ![Значок добавления](media/ITPro-EAC-AddIcon.gif) и выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="46f86-115">Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="46f86-116">Присвойте правилу имя и нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="46f86-116">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="46f86-117">В области **Применить это правило, если** выберите **Получатель**, а затем  **Адрес содержит любое из этих слов**.</span><span class="sxs-lookup"><span data-stu-id="46f86-117">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="46f86-118">В поле **Укажите слова или фразы** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="46f86-118">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="46f86-p103">Введите `abuse@messaging.microsoft.com` , а затем ![нажмите кнопку](media/ITPro-EAC-AddIcon.gif)добавить значок, а `junk@office365.microsoft.com` затем введите, ![а затем](media/ITPro-EAC-AddIcon.gif)нажмите кнопку Добавить значок. Эти адреса электронной почты используются для отправки ложных негативных сообщений в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="46f86-p103">Type `abuse@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="46f86-p104">Введите `phish@office365.microsoft.com` команду и нажмите ![кнопку Добавить](media/ITPro-EAC-AddIcon.gif)значок. Этот адрес электронной почты используется для отправки пропущенных фишинговых сообщений в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="46f86-p104">Type `phish@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="46f86-p105">Введите `false_positive@messaging.microsoft.com` , а затем ![нажмите кнопку](media/ITPro-EAC-AddIcon.gif)добавить значок, а `not_junk@office365.microsoft.com` затем введите, ![а затем](media/ITPro-EAC-AddIcon.gif)нажмите кнопку Добавить значок. Эти адреса электронной почты используются для отправки ложных ложных сообщений в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="46f86-p105">Type `false_positive@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `not_junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="46f86-125">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="46f86-125">Click **ok**.</span></span>
    
6. <span data-ttu-id="46f86-126">В разделе **Выполнить следующие действия** выберите **Отправить скрытую копию сообщения (СК)...** и выберите нужные почтовые ящики.</span><span class="sxs-lookup"><span data-stu-id="46f86-126">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="46f86-p106">При желании можно сделать выбор для аудита правила, проверки правила, активации правила в течение определенного периода времени и других вариантов. Мы рекомендуем проверить правило в течение периода, прежде чем приступать к его применению. [В разделе процедуры для правил для почтового процесса](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span><span class="sxs-lookup"><span data-stu-id="46f86-p106">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. See [Procedures for mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span></span> 
    
8. <span data-ttu-id="46f86-p107">Нажмите кнопку **Сохранить**, чтобы сохранить правило. Оно отобразится в вашем списке правил.</span><span class="sxs-lookup"><span data-stu-id="46f86-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="46f86-132">После создания и применения правила все сообщения, отправляемые из вашей организации на указанные адреса электронной почты, будут копироваться в указанный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="46f86-132">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

