---
title: Использование правил транспорта для настройки массового фильтрации электронной почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/20/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: Вы можете настроить фильтры содержимого на уровне всей компании для нежелательной почты и массовых сообщений электронной почты, используя политики фильтрации содержимого нежелательной почты по умолчанию. Сведения о настройке политик фильтрации содержимого см. в разделах Настройте политики защиты от спама и Set-HostedContentFilterPolicy.
ms.openlocfilehash: f72fa5cc50ab6aa5447e3af9fabc365457c82973
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027686"
---
# <a name="use-transport-rules-to-configure-bulk-email-filtering"></a><span data-ttu-id="cd1ee-104">Использование правил транспорта для настройки массового фильтрации электронной почты</span><span class="sxs-lookup"><span data-stu-id="cd1ee-104">Use transport rules to configure bulk email filtering</span></span>

<span data-ttu-id="cd1ee-p102">Вы можете настроить фильтры содержимого на уровне всей компании для нежелательной почты и массовых сообщений электронной почты, используя политики фильтрации содержимого нежелательной почты по умолчанию. Сведения о настройке политик фильтрации содержимого см. в разделах [Настройте политики защиты от спама](configure-your-spam-filter-policies.md) и [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx).</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p102">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) on how to set the content filter policies.</span></span> 
  
<span data-ttu-id="cd1ee-p103">Если вам нужны дополнительные параметры для фильтрации массовых сообщений, можно создать правила транспорта Exchange для поиска текстовых шаблонов или фраз, которые часто используются в массовых сообщениях. Каждое сообщение, обладающее этими характеристиками, будет отмечено как нежелательное. Использование этих правил может сократить объем нежелательных сообщений, которые получает ваша организация.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p103">If you want to more options to filter bulk messages, you can create Exchange Transport rules to search for text patterns or phrases frequently found in bulk emails. Any message containing these characteristics will be marked as spam. Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cd1ee-110">Прежде чем создавать правила транспорта, описанные в этой статье, рекомендуем ознакомиться с разделами [В чем разница между нежелательной почтой и массовыми сообщениями электронной почты?](what-s-the-difference-between-junk-email-and-bulk-email.md) и [Уровни жалоб на массовые сообщения](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="cd1ee-110">Before creating the Transport rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cd1ee-p104">Следующие процедуры отмечают сообщение как нежелательное для всей организации. Однако можно добавить другое условие, чтобы применить эти правила только к определенным получателям в вашей организации. Таким образом агрессивные параметры фильтрации массовой электронной почты могут применяться к нескольким пользователям, которые часто становятся адресатом нежелательной почты, не затрагивая других пользователей (которые, в основном, получают массовые сообщения, на которые они подписаны).</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p104">The following procedures mark a message as spam for your entire organization. However, you can add another condition to apply these rules only to specific recipients in your organization. This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span> 
  
### <a name="create-an-exchange-transport-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="cd1ee-114">Создание правила транспорта Exchange для фильтрации массовых сообщений электронной почты на основе текстовых шаблонов</span><span class="sxs-lookup"><span data-stu-id="cd1ee-114">Create an Exchange Transport rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="cd1ee-115">В центре администрирования Exchange перейдите в раздел **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-115">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="cd1ee-116">Нажмите кнопку **Добавить**![Значок добавления](media/ITPro-EAC-AddIcon.png) и выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-116">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="cd1ee-117">Укажите имя правила.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-117">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="cd1ee-p105">Нажмите кнопку **Дополнительные параметры**. В разделе **Применить это правило, если** выберите **Тема или текст** \> **соответствует этим текстовым шаблонам**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p105">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>
    
5. <span data-ttu-id="cd1ee-120">В диалоговом окне **Задайте слова или фразы** добавьте следующие регулярные выражения, которые часто используются в массовых сообщениях, по одному и затем нажмите кнопку **ОК**:</span><span class="sxs-lookup"><span data-stu-id="cd1ee-120">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
  - <span data-ttu-id="cd1ee-121">Если вы не можете просмотреть содержимое этого сообщения\,</span><span class="sxs-lookup"><span data-stu-id="cd1ee-121">If you are unable to view the content of this email\, please</span></span>
    
  - <span data-ttu-id="cd1ee-122">\\>(safe )?отпишитесь(here)?\\</a\\></span><span class="sxs-lookup"><span data-stu-id="cd1ee-122">\\>(safe )?unsubscribe( here)?\\</a\\></span></span>
    
  - <span data-ttu-id="cd1ee-123">Если вы не хотите получать дальнейшие communications следующим образом\, Пожалуйста</span><span class="sxs-lookup"><span data-stu-id="cd1ee-123">If you do not wish to receive further communications like this\, please</span></span>
    
  - <span data-ttu-id="cd1ee-p106">\\<img height\="?1"? width\="?1"? src\=.?http\://</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p106">\\<img height\="?1"? width\="?1"? src\=.?http\://</span></span>
    
  - <span data-ttu-id="cd1ee-127">Чтобы перестать получать такие\s+сообщения\:http\://</span><span class="sxs-lookup"><span data-stu-id="cd1ee-127">To stop receiving these\s+emails\:http\://</span></span>
    
  - <span data-ttu-id="cd1ee-128">Чтобы отписаться от \w+ (e\-?писем|e?-?сообщений|бюллетеней)</span><span class="sxs-lookup"><span data-stu-id="cd1ee-128">To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)</span></span>
    
  - <span data-ttu-id="cd1ee-129">больше не (желаете)?(отправлять|получать) \w+ сообщения</span><span class="sxs-lookup"><span data-stu-id="cd1ee-129">no longer (wish )?(to )?(be sent|receive) \w+ email</span></span>
    
  - <span data-ttu-id="cd1ee-130">Если вы не можете просмотреть содержимое этого сообщения\, щелкните здесь</span><span class="sxs-lookup"><span data-stu-id="cd1ee-130">If you are unable to view the content of this email\, please click here</span></span>
    
  - <span data-ttu-id="cd1ee-131">Чтобы получать (ежедневные предложения|наши сообщения)\, добавьте</span><span class="sxs-lookup"><span data-stu-id="cd1ee-131">To ensure you receive (your daily deals|our e-?mails)\, add</span></span>
    
  - <span data-ttu-id="cd1ee-132">Чтобы перестать получать эти сообщения</span><span class="sxs-lookup"><span data-stu-id="cd1ee-132">If you no longer wish to receive these emails</span></span>
    
  - <span data-ttu-id="cd1ee-133">чтобы изменить (настройки подписки|настройки или отписаться)</span><span class="sxs-lookup"><span data-stu-id="cd1ee-133">to change your (subscription preferences|preferences or unsubscribe)</span></span>
    
  - <span data-ttu-id="cd1ee-134">щелкните (здесь, чтобы|) отписаться</span><span class="sxs-lookup"><span data-stu-id="cd1ee-134">click (here to|the) unsubscribe</span></span>
    
    <span data-ttu-id="cd1ee-135">**Примечания.**</span><span class="sxs-lookup"><span data-stu-id="cd1ee-135">**Notes**:</span></span>
    
  - <span data-ttu-id="cd1ee-p107">Список выше не исчерпывающий набор регулярные выражения используются в массовых сообщениях; Дополнительные можно добавлять или удалять при необходимости. Тем не менее он является хорошей отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p107">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
  - <span data-ttu-id="cd1ee-p108">Поиск слов или текстовые шаблоны в теме или другие поля заголовка сообщения возникает *после* сообщение были расшифровать передачи содержимого MIME, кодировку метод, который использовался для передачи двоичных сообщений между серверами SMTP в текст в формате ASCII. Нельзя использовать для поиска необработанные условий и исключений (как правило, Base64) закодированные значения темы или другие поля заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p108">The search for words or text patterns in the subject or other header fields in the message occurs  *after*  the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span> 
    
6. <span data-ttu-id="cd1ee-140">В разделе **Выполните следующее** выберите пункт **Изменить свойства сообщения** \> **задать значение для вероятности нежелательной почты (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-140">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="cd1ee-141">В диалоговом окне **Укажите вероятность нежелательной почты** выберите для SCL значение **5**, **6** или **9** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-141">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
    <span data-ttu-id="cd1ee-p109">Выбор для SCL значения 5 или 6 приводит к выполнению действия **Нежелательная почта**. Выбор значения 9 приводит к выполнению действия **Нежелательное сообщение высокого уровня** согласно настройке политики фильтрации содержимого. Служба выполняет действие, указанное в политике фильтрации содержимого. По умолчанию это действие  доставка сообщения в папку получателя "Нежелательная почта", однако можно настроить и другие действия, как описано в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p109">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cd1ee-145">Если в качестве действия выбрано добавление сообщения в карантин, а не отправка в папки "Нежелательные сообщения" получателей, сообщение будет отправлено в карантин администратора как соответствие правилу транспорта, и оно будет недоступно в карантине нежелательной почты конечного пользователя и через уведомления о нежелательной почте.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-145">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a transport rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
    <span data-ttu-id="cd1ee-146">Дополнительные сведения о значениях SCL в службе см. в статье [Вероятность нежелательной почты](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="cd1ee-146">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="cd1ee-147">Сохраните правило.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-147">Save the rule.</span></span>
    
### <a name="create-an-exchange-transport-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="cd1ee-148">Создание правила транспорта Exchange для фильтрации массовых сообщений электронной почты на основе фраз</span><span class="sxs-lookup"><span data-stu-id="cd1ee-148">Create an Exchange Transport rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="cd1ee-149">В центре администрирования Exchange перейдите в раздел **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-149">In the EAC, go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="cd1ee-150">Нажмите кнопку **Добавить**![Значок добавления](media/ITPro-EAC-AddIcon.png) и выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-150">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="cd1ee-151">Укажите имя правила.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-151">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="cd1ee-p110">Нажмите кнопку **Дополнительные параметры**. В разделе **Применить это правило, если** выберите **Тема или текст** \> **тема включает любое из этих слов**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p110">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>
    
5. <span data-ttu-id="cd1ee-154">В диалоговом окне **Задайте слова или фразы** добавьте следующие фразы, которые часто используются в массовых сообщениях, по одному и затем нажмите кнопку **ОК**:</span><span class="sxs-lookup"><span data-stu-id="cd1ee-154">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
  - <span data-ttu-id="cd1ee-155">чтобы изменить настройки или отписаться</span><span class="sxs-lookup"><span data-stu-id="cd1ee-155">to change your preferences or unsubscribe</span></span>
    
  - <span data-ttu-id="cd1ee-156">Изменить настройки электронной почты или отписаться</span><span class="sxs-lookup"><span data-stu-id="cd1ee-156">Modify email preferences or unsubscribe</span></span>
    
  - <span data-ttu-id="cd1ee-157">Это рекламное сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="cd1ee-157">This is a promotional email</span></span>
    
  - <span data-ttu-id="cd1ee-158">Вы получаете это сообщение, потому что вы запросили подписку</span><span class="sxs-lookup"><span data-stu-id="cd1ee-158">You are receiving this email because you requested a subscription</span></span>
    
  - <span data-ttu-id="cd1ee-159">щелкните здесь, чтобы отписаться</span><span class="sxs-lookup"><span data-stu-id="cd1ee-159">click here to unsubscribe</span></span>
    
  - <span data-ttu-id="cd1ee-160">Вы получили это сообщение, потому что вы подписаны на рассылку</span><span class="sxs-lookup"><span data-stu-id="cd1ee-160">You have received this email because you are subscribed</span></span>
    
  - <span data-ttu-id="cd1ee-161">Чтобы перестать получать наш новостной бюллетень</span><span class="sxs-lookup"><span data-stu-id="cd1ee-161">If you no longer wish to receive our email newsletter</span></span>
    
  - <span data-ttu-id="cd1ee-162">чтобы отписаться от этого бюллетеня</span><span class="sxs-lookup"><span data-stu-id="cd1ee-162">to unsubscribe from this newsletter</span></span>
    
  - <span data-ttu-id="cd1ee-163">Если у вас возникают проблемы с просмотром этого сообщения</span><span class="sxs-lookup"><span data-stu-id="cd1ee-163">If you have trouble viewing this email</span></span>
    
  - <span data-ttu-id="cd1ee-164">Это реклама</span><span class="sxs-lookup"><span data-stu-id="cd1ee-164">This is an advertisement</span></span>
    
  - <span data-ttu-id="cd1ee-165">вы хотите отписаться или изменить</span><span class="sxs-lookup"><span data-stu-id="cd1ee-165">you would like to unsubscribe or change your</span></span>
    
  - <span data-ttu-id="cd1ee-166">просмотреть это сообщение как веб-страницу</span><span class="sxs-lookup"><span data-stu-id="cd1ee-166">view this email as a webpage</span></span>
    
  - <span data-ttu-id="cd1ee-167">Вы получили это сообщение, потому что вы подписаны на рассылку</span><span class="sxs-lookup"><span data-stu-id="cd1ee-167">You are receiving this email because you are subscribed</span></span>
    
    <span data-ttu-id="cd1ee-p111">**Примечание**: еще раз, этот список не исчерпывающий набор фраз, которые используются в массовых сообщениях; Дополнительные можно добавлять или удалять при необходимости. Тем не менее он является хорошей отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p111">**Note**: Once again, this list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
6. <span data-ttu-id="cd1ee-170">В разделе **Выполните следующее** выберите пункт **Изменить свойства сообщения** \> **задать значение для вероятности нежелательной почты (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-170">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="cd1ee-171">В диалоговом окне **Укажите вероятность нежелательной почты** выберите для SCL значение **5**, **6** или **9** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-171">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
    <span data-ttu-id="cd1ee-p112">Выбор для SCL значения 5 или 6 приводит к выполнению действия **Нежелательная почта**. Выбор значения 9 приводит к выполнению действия **Нежелательное сообщение высокого уровня** согласно настройке политики фильтрации содержимого. Служба выполняет действие, указанное в политике фильтрации содержимого. По умолчанию это действие  доставка сообщения в папку получателя "Нежелательная почта", однако можно настроить и другие действия, как описано в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cd1ee-p112">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cd1ee-175">Если в качестве действия выбрано добавление сообщения в карантин, а не отправка в папки "Нежелательные сообщения" получателей, сообщение будет отправлено в карантин администратора как соответствие правилу транспорта, и оно будет недоступно в карантине нежелательной почты конечного пользователя и через уведомления о нежелательной почте.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-175">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a transport rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
    <span data-ttu-id="cd1ee-176">Дополнительные сведения о значениях SCL в службе см. в статье [Вероятность нежелательной почты](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="cd1ee-176">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="cd1ee-177">Сохраните правило.</span><span class="sxs-lookup"><span data-stu-id="cd1ee-177">Save the rule.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="cd1ee-178">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="cd1ee-178">For more information</span></span>

[<span data-ttu-id="cd1ee-179">В чем разница между нежелательной почтой и массовыми сообщениями электронной почты?</span><span class="sxs-lookup"><span data-stu-id="cd1ee-179">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)
  
[<span data-ttu-id="cd1ee-180">Уровни жалоб на массовые сообщения</span><span class="sxs-lookup"><span data-stu-id="cd1ee-180">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)
  
[<span data-ttu-id="cd1ee-181">Настройте политики защиты от спама</span><span class="sxs-lookup"><span data-stu-id="cd1ee-181">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)
  
[<span data-ttu-id="cd1ee-182">Дополнительные параметры фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="cd1ee-182">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
  

