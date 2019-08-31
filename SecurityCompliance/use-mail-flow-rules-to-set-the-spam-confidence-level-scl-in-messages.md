---
title: Указание вероятности нежелательной почты (SCL) в сообщениях с помощью правил потока обработки почты
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
ms.collection:
- M365-security-compliance
description: Администраторы могут научиться настраивать вероятность нежелательной почты для сообщений в Exchange Online Protection.
ms.openlocfilehash: 91252932671ec81d7269bb4e5e5c7680baa13580
ms.sourcegitcommit: 769b506c828c475c713dbb337e115714dcc7f17c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2019
ms.locfileid: "36699160"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a><span data-ttu-id="58eae-103">Указание вероятности нежелательной почты (SCL) в сообщениях с помощью правил потока обработки почты</span><span class="sxs-lookup"><span data-stu-id="58eae-103">Use mail flow rules to set the spam confidence level (SCL) in messages</span></span>

<span data-ttu-id="58eae-104">Вы можете создать правило для процесса обработки почты (также называемое правилом транспорта), которое задает уровень вероятности нежелательной почты (SCL) сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="58eae-104">You can create a mail flow rule (also known as a transport rule) that sets the spam confidence level (SCL) of an email message.</span></span> <span data-ttu-id="58eae-105">SCL показывает, какова вероятность того, что сообщение является нежелательным.</span><span class="sxs-lookup"><span data-stu-id="58eae-105">The SCL is a measure of how likely a message is to be spam.</span></span> <span data-ttu-id="58eae-106">Нежелательная почта  это нежелательные (и обычно ненужные) сообщения.</span><span class="sxs-lookup"><span data-stu-id="58eae-106">Spam is unsolicited (and typically unwanted) email messages.</span></span> <span data-ttu-id="58eae-107">Действия, которые эта служба выполняет с сообщениями, зависят от их уровня вероятности нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="58eae-107">The service takes different action on a message depending on its SCL rating.</span></span> <span data-ttu-id="58eae-108">Например, вам может потребоваться обойти фильтрацию содержимого нежелательной почты для сообщений, отправленных людьми из вашей организации, так как вы уверенны, что сообщения, отправленные коллегами, не могут быть нежелательными.</span><span class="sxs-lookup"><span data-stu-id="58eae-108">For example, you might want to bypass spam content filtering for messages that are sent from people inside your organization because you trust that a message sent internally from a colleague isn't spam.</span></span> <span data-ttu-id="58eae-109">Установка значения вероятности нежелательной почты для сообщения с помощью правил для почтового процесса позволяет повысить управляемость обработки спама.</span><span class="sxs-lookup"><span data-stu-id="58eae-109">Using mail flow rules to set the SCL value of a message gives you increased control in handling spam.</span></span> 
  
 <span data-ttu-id="58eae-110">**Что нужно знать перед началом работы**</span><span class="sxs-lookup"><span data-stu-id="58eae-110">**What do you need to know before you begin?**</span></span>
  
- <span data-ttu-id="58eae-111">Предполагаемое время для завершения каждой процедуры: 10 минут.</span><span class="sxs-lookup"><span data-stu-id="58eae-111">Estimated time to complete this procedure: 10 minutes.</span></span>
    
- <span data-ttu-id="58eae-112">Для выполнения этих процедур необходимы соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="58eae-112">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="58eae-113">Чтобы просмотреть необходимые разрешения, обратитесь к разделу "правила обработки почтового процесса" в разделе [разрешения функций в Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) или [в разделе разрешения компонентов в EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="58eae-113">To see what permissions you need, see the "Mail flow rules" entry in [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) or [Feature permissions in EOP](eop/feature-permissions-in-eop.md).</span></span> 
    
- <span data-ttu-id="58eae-114">Дополнительные сведения о сочетаниях клавиш, которые могут применяться к процедурам, описанным в этой статье, приведены в статье [сочетания клавиш для центра администрирования Exchange в Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span><span class="sxs-lookup"><span data-stu-id="58eae-114">For information about keyboard shortcuts that may apply to the procedures in this topic, see [Keyboard shortcuts for the Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/accessibility/keyboard-shortcuts-in-admin-center).</span></span>
    
### <a name="to-create-a-mail-flow-rule-that-sets-the-scl-of-a-message"></a><span data-ttu-id="58eae-115">Создание правила для почтового процесса, которое задает значение вероятности нежелательной почты для сообщения</span><span class="sxs-lookup"><span data-stu-id="58eae-115">To create a mail flow rule that sets the SCL of a message</span></span>

1. <span data-ttu-id="58eae-116">В Центре администрирования Exchange выберите **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="58eae-116">In the Exchange admin center (EAC), choose **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="58eae-117">Щелкните **Создать**![Значок добавления](media/ITPro-EAC-AddIcon.gif), затем выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="58eae-117">Choose **New**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="58eae-118">Укажите имя правила.</span><span class="sxs-lookup"><span data-stu-id="58eae-118">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="58eae-119">Выберите **Дополнительные параметры**, а затем под пунктом **Применить это правило, если...** выберите условие, запускающее действие, которые вы собираетесь задать для этого правила (а именно, "Задать значение вероятности нежелательной почты (SCL)").</span><span class="sxs-lookup"><span data-stu-id="58eae-119">Choose **More options**, and then under **Apply this rule if**, specify a condition that will trigger the action you'll be setting for this rule (which is to set the SCL value).</span></span>
    
    <span data-ttu-id="58eae-120">Например, вы можете установить значение **Отправитель** \> **является внешним/внутренним**, а затем в диалогом окне **выбор местоположения отправителя** выбрать **Внутри организации** и нажать **ок**.</span><span class="sxs-lookup"><span data-stu-id="58eae-120">For example, you can set **The sender** \> **is internal/external**, and then in the **select sender location** dialog box, select **Inside the organization**, and choose **ok**.</span></span><br/>
    <span data-ttu-id="58eae-121">![Выбор расположения отправителя](media/EOP-ETR-SetSCL-1.jpg)</span><span class="sxs-lookup"><span data-stu-id="58eae-121">![Select sender location](media/EOP-ETR-SetSCL-1.jpg)</span></span>
  
5. <span data-ttu-id="58eae-122">В разделе **Выполните следующее** выберите пункт **Изменить свойства сообщения** \> **задать значение для вероятности нежелательной почты (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="58eae-122">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
  
6. <span data-ttu-id="58eae-123">В диалоговом окне **указать вероятность нежелательной почты** выберите одно из следующих значений и нажмите **ок**:</span><span class="sxs-lookup"><span data-stu-id="58eae-123">In the **specify SCL** dialog box, select one of the following values, and choose **ok**:</span></span>
    
  - <span data-ttu-id="58eae-124">**Обойти фильтр нежелательной почты**  устанавливает для уровня вероятности нежелательной почты значение -1, при котором фильтрация нежелательной почты не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="58eae-124">**Bypass spam filtering** - This sets the SCL to -1, which means that content filtering won't be performed.</span></span> 
    
  - <span data-ttu-id="58eae-125">**0-4**  если вы установите для уровня вероятности нежелательной почты одно из этих значений, сообщения будут пропускаться через фильтр содержимого для дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="58eae-125">**0-4** - When you set the SCL to one of these values, the message will be passed along to the content filter for additional processing.</span></span> 
    
  - <span data-ttu-id="58eae-p103">**5, 6**  если вы установите для уровня вероятности нежелательной почты одно из этих значений, к сообщениям будет применяться действие, указанное для **Нежелательных сообщений** в соответствующих политиках фильтрации содержимого. По умолчанию это действие  отправка сообщений в папку "Нежелательная почта" получателя.</span><span class="sxs-lookup"><span data-stu-id="58eae-p103">**5, 6** - When you set the SCL to one of these values, the action specified for **Spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
  - <span data-ttu-id="58eae-p104">**7-9**  если вы установите для уровня вероятности нежелательной почты одно из этих значений, к сообщениям будет применяться действие, указанное для **Нежелательной почты высокого уровня**, в соответствующих политиках фильтрации содержимого. По умолчанию это действие  отправка сообщений в папку "Нежелательная почта" получателя.</span><span class="sxs-lookup"><span data-stu-id="58eae-p104">**7-9** - When you set the SCL to one of these values, the action specified for **High confidence spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
    <span data-ttu-id="58eae-p105">Дополнительные сведения о настройке политик фильтрации содержимого см. в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md). Дополнительные сведения о значениях SCL в службе см. в разделе [Вероятность нежелательной почты](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="58eae-p105">For more information about configuring your content filter policies, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
7. <span data-ttu-id="58eae-132">Укажите для правила дополнительные свойства и нажмите **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="58eae-132">Specify additional properties for the rule, and choose **save**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="58eae-133">Дополнительные сведения о дополнительных свойствах, которые можно выбрать или указать для этого правила, см в разделе Использование центра администрирования Exchange [для создания правил для почтового процесса](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures#use-the-eac-to-create-mail-flow-rules).</span><span class="sxs-lookup"><span data-stu-id="58eae-133">For more information about the additional properties you can select or specify for this rule, see [Use the EAC to create mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures#use-the-eac-to-create-mail-flow-rules).</span></span> 
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="58eae-134">Как убедиться, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="58eae-134">How do you know this worked?</span></span>

<span data-ttu-id="58eae-p106">Чтобы убедиться, что эта процедура работает правильно, отправьте сообщение одному из пользователей в вашей организации и убедитесь, что с сообщением выполняется ожидаемое действие. Например, если вы **задали значение для вероятности нежелательной почты (SCL)** **Обход фильтрации нежелательной почты**, сообщение должно быть отправлено в папку "Входящие" указанного получателя. Если же вы **задали значение для вероятности нежелательной почты (SCL)** **9**, а действие, которое выполняется с **Нежелательными сообщениями высокого уровня** для соответствующих политик фильтрации содержимого,  перемещение сообщения в папку "Нежелательная почта", то сообщение должно быть отправлено в папку "Нежелательная почта" указанного получателя.</span><span class="sxs-lookup"><span data-stu-id="58eae-p106">To verify that this procedure is working correctly, send an email message to someone inside your organization, and verify that the action performed on the message is as expected. For example, if you **set the spam confidence level (SCL)** to **Bypass spam filtering**, then the message should be sent to the specified recipient's inbox. However, if you **set the spam confidence level (SCL)** to **9**, and the **High confidence spam** action for your applicable content filter policies is to move the message to the Junk Email folder, then the message should be sent to the specified recipient's Junk Email folder.</span></span> 
  

