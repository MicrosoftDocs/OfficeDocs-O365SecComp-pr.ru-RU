---
title: Указание вероятности нежелательной почты (SCL) в сообщениях с помощью правил потока обработки почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 4ccab17a-6d49-4786-aa28-92fb28893e99
description: "Вы можете создать правило транспорта, которое устанавливает для сообщений уровень вероятности нежелательной почты (SCL). SCL показывает, какова вероятность того, что сообщение является нежелательным. Нежелательная почта \x97 это нежелательные (и обычно ненужные) сообщения. Действия, которые эта служба выполняет с сообщениями, зависят от их уровня вероятности нежелательной почты. Например, вам может потребоваться обойти фильтрацию содержимого нежелательной почты для сообщений, отправленных людьми из вашей организации, так как вы уверенны, что сообщения, отправленные коллегами, не могут быть нежелательными. Используя правила транспорта, чтобы задать для сообщения уровень вероятности нежелательной почты, вы получаете больше возможностей в управлении нежелательной почтой."
ms.openlocfilehash: 7abd0d1881374b1f2a4bd32ee480445f7683d1b3
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002898"
---
# <a name="use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages"></a><span data-ttu-id="f1564-108">Указание вероятности нежелательной почты (SCL) в сообщениях с помощью правил потока обработки почты</span><span class="sxs-lookup"><span data-stu-id="f1564-108">Use mail flow rules to set the spam confidence level (SCL) in messages</span></span>

<span data-ttu-id="f1564-p102">Вы можете создать правило транспорта, которое устанавливает для сообщений уровень вероятности нежелательной почты (SCL). SCL показывает, какова вероятность того, что сообщение является нежелательным. Нежелательная почта  это нежелательные (и обычно ненужные) сообщения. Действия, которые эта служба выполняет с сообщениями, зависят от их уровня вероятности нежелательной почты. Например, вам может потребоваться обойти фильтрацию содержимого нежелательной почты для сообщений, отправленных людьми из вашей организации, так как вы уверенны, что сообщения, отправленные коллегами, не могут быть нежелательными. Используя правила транспорта, чтобы задать для сообщения уровень вероятности нежелательной почты, вы получаете больше возможностей в управлении нежелательной почтой.</span><span class="sxs-lookup"><span data-stu-id="f1564-p102">You can create a transport rule that sets the spam confidence level (SCL) of an email message. The SCL is a measure of how likely a message is to be spam. Spam is unsolicited (and typically unwanted) email messages. The service takes different action on a message depending on its SCL rating. For example, you might want to bypass spam content filtering for messages that are sent from people inside your organization because you trust that a message sent internally from a colleague isn't spam. Using transport rules to set the SCL value of a message gives you increased control in handling spam.</span></span> 
  
 <span data-ttu-id="f1564-115">**Что нужно знать перед началом работы**</span><span class="sxs-lookup"><span data-stu-id="f1564-115">**What do you need to know before you begin?**</span></span>
  
- <span data-ttu-id="f1564-116">Предполагаемое время для завершения каждой процедуры: 10 минут.</span><span class="sxs-lookup"><span data-stu-id="f1564-116">Estimated time to complete this procedure: 10 minutes.</span></span>
    
- <span data-ttu-id="f1564-p103">Вы должны быть назначены разрешения, перед выполнением этой процедуры или процедуры. Чтобы увидеть, какие нужны разрешения, видеть запись «Правила транспорта» в [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) или [разрешения компонентов в EOP](eop/feature-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="f1564-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) or [Feature permissions in EOP](eop/feature-permissions-in-eop.md).</span></span> 
    
- <span data-ttu-id="f1564-119">Сочетания клавиш для процедур, описанных в этой статье, приведены в статье **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="f1564-119">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
    
### <a name="to-create-a-transport-rule-that-sets-the-scl-of-a-message"></a><span data-ttu-id="f1564-120">Чтобы создать правило транспорта, которое устанавливает для сообщения уровень вероятности нежелательной почты, сделайте так.</span><span class="sxs-lookup"><span data-stu-id="f1564-120">To create a transport rule that sets the SCL of a message</span></span>

1. <span data-ttu-id="f1564-121">В Центре администрирования Exchange выберите **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="f1564-121">In the Exchange admin center (EAC), choose **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="f1564-122">Щелкните **Создать**![Значок добавления](media/ITPro-EAC-AddIcon.gif), затем выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="f1564-122">Choose **New**![Add Icon](media/ITPro-EAC-AddIcon.gif), and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="f1564-123">Укажите имя правила.</span><span class="sxs-lookup"><span data-stu-id="f1564-123">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="f1564-124">Выберите **Дополнительные параметры**, а затем под пунктом **Применить это правило, если...** выберите условие, запускающее действие, которые вы собираетесь задать для этого правила (а именно, "Задать значение вероятности нежелательной почты (SCL)").</span><span class="sxs-lookup"><span data-stu-id="f1564-124">Choose **More options**, and then under **Apply this rule if**, specify a condition that will trigger the action you'll be setting for this rule (which is to set the SCL value).</span></span>
    
    <span data-ttu-id="f1564-125">Например, вы можете установить значение **Отправитель** \> **является внешним/внутренним**, а затем в диалогом окне **выбор местоположения отправителя** выбрать **Внутри организации** и нажать **ок**.</span><span class="sxs-lookup"><span data-stu-id="f1564-125">For example, you can set **The sender** \> **is internal/external**, and then in the **select sender location** dialog box, select **Inside the organization**, and choose **ok**.</span></span></br>
    <span data-ttu-id="f1564-126">![Выбор расположения отправителя](media/EOP-ETR-SetSCL-1.jpg)</span><span class="sxs-lookup"><span data-stu-id="f1564-126">![Select sender location](media/EOP-ETR-SetSCL-1.jpg)</span></span>
  
5. <span data-ttu-id="f1564-127">В разделе **Выполните следующее** выберите пункт **Изменить свойства сообщения** \> **задать значение для вероятности нежелательной почты (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="f1564-127">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
  
6. <span data-ttu-id="f1564-128">В диалоговом окне **указать вероятность нежелательной почты** выберите одно из следующих значений и нажмите **ок**:</span><span class="sxs-lookup"><span data-stu-id="f1564-128">In the **specify SCL** dialog box, select one of the following values, and choose **ok**:</span></span>
    
  - <span data-ttu-id="f1564-129">**Обойти фильтр нежелательной почты**  устанавливает для уровня вероятности нежелательной почты значение -1, при котором фильтрация нежелательной почты не будет выполняться.</span><span class="sxs-lookup"><span data-stu-id="f1564-129">**Bypass spam filtering** - This sets the SCL to -1, which means that content filtering won't be performed.</span></span> 
    
  - <span data-ttu-id="f1564-130">**0-4**  если вы установите для уровня вероятности нежелательной почты одно из этих значений, сообщения будут пропускаться через фильтр содержимого для дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="f1564-130">**0-4** - When you set the SCL to one of these values, the message will be passed along to the content filter for additional processing.</span></span> 
    
  - <span data-ttu-id="f1564-p104">**5, 6**  если вы установите для уровня вероятности нежелательной почты одно из этих значений, к сообщениям будет применяться действие, указанное для **Нежелательных сообщений** в соответствующих политиках фильтрации содержимого. По умолчанию это действие  отправка сообщений в папку "Нежелательная почта" получателя.</span><span class="sxs-lookup"><span data-stu-id="f1564-p104">**5, 6** - When you set the SCL to one of these values, the action specified for **Spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
  - <span data-ttu-id="f1564-p105">**7-9**  если вы установите для уровня вероятности нежелательной почты одно из этих значений, к сообщениям будет применяться действие, указанное для **Нежелательной почты высокого уровня**, в соответствующих политиках фильтрации содержимого. По умолчанию это действие  отправка сообщений в папку "Нежелательная почта" получателя.</span><span class="sxs-lookup"><span data-stu-id="f1564-p105">**7-9** - When you set the SCL to one of these values, the action specified for **High confidence spam** in the applicable content filter policies will be applied. By default, the action is to send the message to the recipient's Junk Email folder.</span></span> 
    
    <span data-ttu-id="f1564-p106">Дополнительные сведения о настройке политик фильтрации содержимого см. в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md). Дополнительные сведения о значениях SCL в службе см. в разделе [Вероятность нежелательной почты](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f1564-p106">For more information about configuring your content filter policies, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
7. <span data-ttu-id="f1564-137">Укажите для правила дополнительные свойства и нажмите **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="f1564-137">Specify additional properties for the rule, and choose **save**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="f1564-138">Дополнительные сведения о дополнительных свойствах, которые вы можете задать для этого правила, см. в разделе [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span><span class="sxs-lookup"><span data-stu-id="f1564-138">For more information about the additional properties you can select or specify for this rule, see [Use the EAC to create a transport rule](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx#CreateEAC).</span></span> 
  
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="f1564-139">Как проверить, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="f1564-139">How do you know this worked?</span></span>

<span data-ttu-id="f1564-p107">Чтобы убедиться, что эта процедура работает правильно, отправьте сообщение одному из пользователей в вашей организации и убедитесь, что с сообщением выполняется ожидаемое действие. Например, если вы **задали значение для вероятности нежелательной почты (SCL)** **Обход фильтрации нежелательной почты**, сообщение должно быть отправлено в папку "Входящие" указанного получателя. Если же вы **задали значение для вероятности нежелательной почты (SCL)** **9**, а действие, которое выполняется с **Нежелательными сообщениями высокого уровня** для соответствующих политик фильтрации содержимого,  перемещение сообщения в папку "Нежелательная почта", то сообщение должно быть отправлено в папку "Нежелательная почта" указанного получателя.</span><span class="sxs-lookup"><span data-stu-id="f1564-p107">To verify that this procedure is working correctly, send an email message to someone inside your organization, and verify that the action performed on the message is as expected. For example, if you **set the spam confidence level (SCL)** to **Bypass spam filtering**, then the message should be sent to the specified recipient's inbox. However, if you **set the spam confidence level (SCL)** to **9**, and the **High confidence spam** action for your applicable content filter policies is to move the message to the Junk Email folder, then the message should be sent to the specified recipient's Junk Email folder.</span></span> 
  

