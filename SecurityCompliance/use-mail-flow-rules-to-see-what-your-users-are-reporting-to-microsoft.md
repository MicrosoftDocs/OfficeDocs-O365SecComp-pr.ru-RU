---
title: Просмотр отчетов, передаваемых пользователями в Майкрософт, с помощью правил для потока обработки почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/23/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Можно создать правила транспорта Exchange пользователи не может отправлять сообщения электронной почты в корпорацию Майкрософт для анализа и назначить им процессы безопасности
ms.openlocfilehash: f2376668e2a1a16eba9913178a100fc31763b227
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026776"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="f1be0-103">Просмотр отчетов, передаваемых пользователями в Майкрософт, с помощью правил для потока обработки почты</span><span class="sxs-lookup"><span data-stu-id="f1be0-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="f1be0-p101">Существует несколько способов для отправки ложных положительных и ложные отрицательных сообщений в корпорацию Майкрософт для анализа. С правами администратора можно использовать правила потока почты видеть, что пользователи являются отчетность в корпорацию Майкрософт как нежелательной почты, не являющееся нежелательным и фишинг-атак. Дополнительные сведения можно [Отправить нежелательной почты, не являющееся нежелательным и фишинга мошенничество в корпорацию Майкрософт для анализа](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). С другой стороны можно создать правила транспорта Exchange пользователи не может отправлять сообщения электронной почты в корпорацию Майкрософт для анализа и назначить им процессы безопасности.</span><span class="sxs-lookup"><span data-stu-id="f1be0-p101">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis. As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Conversely, you can create an Exchange Transport rule to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f1be0-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="f1be0-108">What do you need to know before you begin?</span></span>
<span data-ttu-id="f1be0-109"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="f1be0-109"></span></span>

<span data-ttu-id="f1be0-110">Предполагаемое время для завершения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="f1be0-110">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="f1be0-p102">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье запись "Правила транспорта" в статье [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) и запись "Политики почтовых ящиков Outlook Web App" в статье [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1be0-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook Web App mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="f1be0-113">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="f1be0-113">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="f1be0-114">Создание правила для потока обработки почты для просмотра отправляемых пользователями отчетов о спаме, фишинге и не спаме в Центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="f1be0-114">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>
<span data-ttu-id="f1be0-115"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="f1be0-115"></span></span>

1. <span data-ttu-id="f1be0-116">В Центре администрирования Exchange последовательно выберите пункты **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="f1be0-116">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="f1be0-117">Щелкните ![Значок добавления](media/ITPro-EAC-AddIcon.png) и выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="f1be0-117">Click ![Add Icon](media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="f1be0-118">Присвойте правилу имя и нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="f1be0-118">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="f1be0-119">В области **Применить это правило, если** выберите **Получатель**, а затем  **Адрес содержит любое из этих слов**.</span><span class="sxs-lookup"><span data-stu-id="f1be0-119">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="f1be0-120">В поле **Укажите слова или фразы** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="f1be0-120">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="f1be0-p103">Введите **abuse@messaging.microsoft.com**, а затем щелкните ![Значок добавления](media/ITPro-EAC-AddIcon.png), после чего введите **junk@office365.microsoft.com** и щелкните ![Значок добавления](media/ITPro-EAC-AddIcon.png). Эти адреса электронной почты используются для отправки ошибочно отрицательных сообщений в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f1be0-p103">Type **abuse@messaging.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png), and then type **junk@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="f1be0-p104">Введите **phish@office365.microsoft.com** и нажмите кнопку ![Значок добавления](media/ITPro-EAC-AddIcon.png). Этот адрес электронной почты используется для отправки пропущенных фишинговых сообщений в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f1be0-p104">Type **phish@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="f1be0-p105">Введите **false_positive@messaging.microsoft.com**, а затем щелкните ![Значок добавления](media/ITPro-EAC-AddIcon.png), после чего введите **not_junk@office365.microsoft.com** и щелкните ![Значок добавления](media/ITPro-EAC-AddIcon.png). Эти адреса электронной почты используются для отправки ошибочно положительных сообщений в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f1be0-p105">Type **false_positive@messaging.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png), and then type **not_junk@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="f1be0-127">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f1be0-127">Click **ok**.</span></span>
    
6. <span data-ttu-id="f1be0-128">В разделе **Выполнить следующие действия** выберите **Отправить скрытую копию сообщения (СК)...** и выберите нужные почтовые ящики.</span><span class="sxs-lookup"><span data-stu-id="f1be0-128">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="f1be0-p106">При необходимости можно выбрать нужные параметры для аудита и проверки правила, его активации в течение определенного периода, а также выбрать другие настройки. Мы рекомендуем протестировать правило в течение определенного времени перед его применением. [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) содержит дополнительные сведения о выбранных элементах.</span><span class="sxs-lookup"><span data-stu-id="f1be0-p106">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contains more information about these selections.</span></span> 
    
8. <span data-ttu-id="f1be0-p107">Нажмите кнопку **Сохранить**, чтобы сохранить правило. Оно отобразится в вашем списке правил.</span><span class="sxs-lookup"><span data-stu-id="f1be0-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="f1be0-134">После создания и применения правила все сообщения, отправляемые из вашей организации на указанные адреса электронной почты, будут копироваться в указанный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="f1be0-134">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

