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
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Можно создать правила транспорта Exchange пользователи не может отправлять сообщения электронной почты в корпорацию Майкрософт для анализа и назначить им процессы безопасности
ms.openlocfilehash: 6c6af23e6a5f345e26c7dc09c898f2978ea51a5f
ms.sourcegitcommit: df1e9590a9fa152fa776f16d9b25c180ba7198f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/07/2018
ms.locfileid: "22122589"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="d9190-103">Просмотр отчетов, передаваемых пользователями в Майкрософт, с помощью правил для потока обработки почты</span><span class="sxs-lookup"><span data-stu-id="d9190-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="d9190-p101">Существует несколько способов для отправки ложных положительных и ложные отрицательных сообщений в корпорацию Майкрософт для анализа. С правами администратора можно использовать правила потока почты видеть, что пользователи являются отчетность в корпорацию Майкрософт как нежелательной почты, не являющееся нежелательным и фишинг-атак. Дополнительные сведения можно [Отправить нежелательной почты, не являющееся нежелательным и фишинга мошенничество в корпорацию Майкрософт для анализа](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). С другой стороны можно создать правила транспорта Exchange пользователи не может отправлять сообщения электронной почты в корпорацию Майкрософт для анализа и назначить им процессы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d9190-p101">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis. As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Conversely, you can create an Exchange Transport rule to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d9190-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="d9190-108">What do you need to know before you begin?</span></span>

<span data-ttu-id="d9190-109">Предполагаемое время для завершения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="d9190-109">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="d9190-p102">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье запись "Правила транспорта" в статье [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) и запись "Политики почтовых ящиков Outlook Web App" в статье [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx).</span><span class="sxs-lookup"><span data-stu-id="d9190-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook Web App mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="d9190-112">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="d9190-112">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="d9190-113">Создание правила для потока обработки почты для просмотра отправляемых пользователями отчетов о спаме, фишинге и не спаме в Центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="d9190-113">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>

1. <span data-ttu-id="d9190-114">В Центре администрирования Exchange последовательно выберите пункты **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="d9190-114">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="d9190-115">Щелкните ![Значок добавления](media/ITPro-EAC-AddIcon.png) и выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="d9190-115">Click ![Add Icon](media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="d9190-116">Присвойте правилу имя и нажмите **Дополнительные параметры**.</span><span class="sxs-lookup"><span data-stu-id="d9190-116">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="d9190-117">В области **Применить это правило, если** выберите **Получатель**, а затем  **Адрес содержит любое из этих слов**.</span><span class="sxs-lookup"><span data-stu-id="d9190-117">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="d9190-118">В поле **Укажите слова или фразы** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d9190-118">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="d9190-p103">Тип `abuse@messaging.microsoft.com` и нажмите кнопку ![добавить значок](media/ITPro-EAC-AddIcon.png)и затем введите `junk@office365.microsoft.com` и нажмите кнопку ![добавить значок](media/ITPro-EAC-AddIcon.png). Эти адреса электронной почты используются для отправки сообщений с ложным отрицательным в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d9190-p103">Type `abuse@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.png), and then type `junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="d9190-p104">Тип `phish@office365.microsoft.com` и нажмите кнопку ![добавить значок](media/ITPro-EAC-AddIcon.png). Этот адрес электронной почты используется для отправки сообщений с пропущенных фишинга в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d9190-p104">Type `phish@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="d9190-p105">Тип `false_positive@messaging.microsoft.com` и нажмите кнопку ![добавить значок](media/ITPro-EAC-AddIcon.png)и затем введите `not_junk@office365.microsoft.com` и нажмите кнопку ![добавить значок](media/ITPro-EAC-AddIcon.png). Эти адреса электронной почты используются для отправки сообщений с ложным положительным в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="d9190-p105">Type `false_positive@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.png), and then type `not_junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="d9190-125">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d9190-125">Click **ok**.</span></span>
    
6. <span data-ttu-id="d9190-126">В разделе **Выполнить следующие действия** выберите **Отправить скрытую копию сообщения (СК)...** и выберите нужные почтовые ящики.</span><span class="sxs-lookup"><span data-stu-id="d9190-126">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="d9190-p106">Если вы хотите, можно сделать выбранных элементов для аудита правило, проверка правила, активировать правило определенный период и других элементов управления. Рекомендуется тестировать правила в течение периода перед его применением. В разделе [процедуры для правила потока почты](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span><span class="sxs-lookup"><span data-stu-id="d9190-p106">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. See [Procedures for mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span></span> 
    
8. <span data-ttu-id="d9190-p107">Нажмите кнопку **Сохранить**, чтобы сохранить правило. Оно отобразится в вашем списке правил.</span><span class="sxs-lookup"><span data-stu-id="d9190-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="d9190-132">После создания и применения правила все сообщения, отправляемые из вашей организации на указанные адреса электронной почты, будут копироваться в указанный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="d9190-132">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

