---
title: Использование правил потока почты Настройка фильтрации в Exchange Online Protection массовыми сообщениями электронной почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: Администраторы могут узнать порядок использования правил поток почты в Exchange Online Protection для фильтрации массовых электронной почты.
ms.openlocfilehash: ce95872d3d80436dce4c62037caea9a5f735726d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "27382810"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a><span data-ttu-id="78b7e-103">Использование правил потока почты Настройка фильтрации в Exchange Online Protection массовыми сообщениями электронной почты</span><span class="sxs-lookup"><span data-stu-id="78b7e-103">Use mail flow rules to configure bulk email filtering in Exchange Online Protection</span></span>

<span data-ttu-id="78b7e-p101">Вы можете настроить фильтры содержимого на уровне всей компании для нежелательной почты и массовых сообщений электронной почты, используя политики фильтрации содержимого нежелательной почты по умолчанию. Сведения о настройке политик фильтрации содержимого см. в разделах [Настройте политики защиты от спама](configure-your-spam-filter-policies.md) и [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx).</span><span class="sxs-lookup"><span data-stu-id="78b7e-p101">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) on how to set the content filter policies.</span></span> 
  
<span data-ttu-id="78b7e-p102">Если вы хотите Дополнительные параметры для фильтрации массовых сообщений, можно создать правила для потока обработки почты (также известной как правила транспорта) для поиска текстовых шаблонов или фраз, которые часто используются в массовых сообщениях. Любое сообщение, содержащее эти характеристики помечаются как нежелательная почта. Эти правила помогут уменьшить количество нежелательных массовыми сообщениями электронной почты, который получает вашей организации.</span><span class="sxs-lookup"><span data-stu-id="78b7e-p102">If you want to more options to filter bulk messages, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases frequently found in bulk emails. Any message containing these characteristics will be marked as spam. Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>
  
<span data-ttu-id="78b7e-109">**Примечания**:</span><span class="sxs-lookup"><span data-stu-id="78b7e-109">**Notes**:</span></span>

- <span data-ttu-id="78b7e-110">Перед создание правил потока обработки почты задокументированные в этом разделе, мы рекомендуем сначала прочитать [в чем разница между нежелательной почтой и массовыми сообщениями электронной почты?](what-s-the-difference-between-junk-email-and-bulk-email.md) и [уровень жалоб массового значения](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="78b7e-110">Before creating the mail flow rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span> 
  
- <span data-ttu-id="78b7e-p103">Следующие процедуры отмечают сообщение как нежелательное для всей организации. Однако можно добавить другое условие, чтобы применить эти правила только к определенным получателям в вашей организации. Таким образом агрессивные параметры фильтрации массовой электронной почты могут применяться к нескольким пользователям, которые часто становятся адресатом нежелательной почты, не затрагивая других пользователей (которые, в основном, получают массовые сообщения, на которые они подписаны).</span><span class="sxs-lookup"><span data-stu-id="78b7e-p103">The following procedures mark a message as spam for your entire organization. However, you can add another condition to apply these rules only to specific recipients in your organization. This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span> 
  
### <a name="create-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="78b7e-114">Создание правила поток почты для фильтрации массовых сообщений электронной почты на основе текстовых шаблонов</span><span class="sxs-lookup"><span data-stu-id="78b7e-114">Create mail flow rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="78b7e-115">В центре администрирования Exchange перейдите в раздел **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-115">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="78b7e-116">Нажмите кнопку **Добавить**![Значок добавления](media/ITPro-EAC-AddIcon.gif) и выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-116">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="78b7e-117">Укажите имя правила.</span><span class="sxs-lookup"><span data-stu-id="78b7e-117">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="78b7e-p104">Нажмите кнопку **Дополнительные параметры**. В разделе **Применить это правило, если** выберите **Тема или текст** \> **соответствует этим текстовым шаблонам**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-p104">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>
    
5. <span data-ttu-id="78b7e-120">В диалоговом окне **Задайте слова или фразы** добавьте следующие регулярные выражения, которые часто используются в массовых сообщениях, по одному и затем нажмите кнопку **ОК**:</span><span class="sxs-lookup"><span data-stu-id="78b7e-120">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="78b7e-121">Если вы не можете просмотреть содержимое этого сообщения\,</span><span class="sxs-lookup"><span data-stu-id="78b7e-121">If you are unable to view the content of this email\, please</span></span>
    
   - <span data-ttu-id="78b7e-122">\\>(safe )?отпишитесь(here)?\\</a\\></span><span class="sxs-lookup"><span data-stu-id="78b7e-122">\\>(safe )?unsubscribe( here)?\\</a\\></span></span>
    
   - <span data-ttu-id="78b7e-123">Если вы не хотите получать дальнейшие communications следующим образом\, Пожалуйста</span><span class="sxs-lookup"><span data-stu-id="78b7e-123">If you do not wish to receive further communications like this\, please</span></span>
    
   - <span data-ttu-id="78b7e-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span><span class="sxs-lookup"><span data-stu-id="78b7e-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span></span>
    
   - <span data-ttu-id="78b7e-127">Чтобы перестать получать такие\s+сообщения\:http\://</span><span class="sxs-lookup"><span data-stu-id="78b7e-127">To stop receiving these\s+emails\:http\://</span></span>
    
   - <span data-ttu-id="78b7e-128">Чтобы отписаться от \w+ (e\-?писем|e?-?сообщений|бюллетеней)</span><span class="sxs-lookup"><span data-stu-id="78b7e-128">To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)</span></span>
    
   - <span data-ttu-id="78b7e-129">больше не (желаете)?(отправлять|получать) \w+ сообщения</span><span class="sxs-lookup"><span data-stu-id="78b7e-129">no longer (wish )?(to )?(be sent|receive) \w+ email</span></span>
    
   - <span data-ttu-id="78b7e-130">Если вы не можете просмотреть содержимое этого сообщения\, щелкните здесь</span><span class="sxs-lookup"><span data-stu-id="78b7e-130">If you are unable to view the content of this email\, please click here</span></span>
    
   - <span data-ttu-id="78b7e-131">Чтобы получать (ежедневные предложения|наши сообщения)\, добавьте</span><span class="sxs-lookup"><span data-stu-id="78b7e-131">To ensure you receive (your daily deals|our e-?mails)\, add</span></span>
    
   - <span data-ttu-id="78b7e-132">Чтобы перестать получать эти сообщения</span><span class="sxs-lookup"><span data-stu-id="78b7e-132">If you no longer wish to receive these emails</span></span>
    
   - <span data-ttu-id="78b7e-133">чтобы изменить (настройки подписки|настройки или отписаться)</span><span class="sxs-lookup"><span data-stu-id="78b7e-133">to change your (subscription preferences|preferences or unsubscribe)</span></span>
    
   - <span data-ttu-id="78b7e-134">щелкните (здесь, чтобы|) отписаться</span><span class="sxs-lookup"><span data-stu-id="78b7e-134">click (here to|the) unsubscribe</span></span>
    
   <span data-ttu-id="78b7e-135">**Примечания**:</span><span class="sxs-lookup"><span data-stu-id="78b7e-135">**Notes**:</span></span>

   - <span data-ttu-id="78b7e-p106">Список выше не исчерпывающий набор регулярные выражения используются в массовых сообщениях; Дополнительные можно добавлять или удалять при необходимости. Тем не менее он является хорошей отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="78b7e-p106">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
   - <span data-ttu-id="78b7e-p107">Поиск слов или текстовые шаблоны в теме или другие поля заголовка сообщения возникает *после* сообщение были расшифровать передачи содержимого MIME, кодировку метод, который использовался для передачи двоичных сообщений между серверами SMTP в текст в формате ASCII. Нельзя использовать для поиска необработанные условий и исключений (как правило, Base64) закодированные значения темы или другие поля заголовка сообщения.</span><span class="sxs-lookup"><span data-stu-id="78b7e-p107">The search for words or text patterns in the subject or other header fields in the message occurs  *after*  the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span> 
    
6. <span data-ttu-id="78b7e-140">В разделе **Выполните следующее** выберите пункт **Изменить свойства сообщения** \> **задать значение для вероятности нежелательной почты (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-140">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="78b7e-141">В диалоговом окне **Укажите вероятность нежелательной почты** выберите для SCL значение **5**, **6** или **9** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-141">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="78b7e-p108">Выбор для SCL значения 5 или 6 приводит к выполнению действия **Нежелательная почта**. Выбор значения 9 приводит к выполнению действия **Нежелательное сообщение высокого уровня** согласно настройке политики фильтрации содержимого. Служба выполняет действие, указанное в политике фильтрации содержимого. По умолчанию это действие  доставка сообщения в папку получателя "Нежелательная почта", однако можно настроить и другие действия, как описано в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="78b7e-p108">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="78b7e-145">Если настроенные действие заключается в карантин сообщения, а не отправьте его в папку нежелательной почты получателей, это сообщение будет отправлено в карантин администратор, как соответствие правила потока обработки почты и оно не будет доступен в карантину нежелательной почты или с помощью конечных пользователей защиты от нежелательной почты уведомления.</span><span class="sxs-lookup"><span data-stu-id="78b7e-145">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="78b7e-146">Дополнительные сведения о значениях SCL в службе см. в статье [Вероятность нежелательной почты](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="78b7e-146">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="78b7e-147">Сохраните правило.</span><span class="sxs-lookup"><span data-stu-id="78b7e-147">Save the rule.</span></span>
    
### <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="78b7e-148">Создание правила потока обработки почты для фильтрации массовых сообщений электронной почты на основе фраз</span><span class="sxs-lookup"><span data-stu-id="78b7e-148">Create a mail flow rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="78b7e-149">В центре администрирования Exchange перейдите в раздел **Поток обработки почты** \> **Правила**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-149">In the EAC, go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="78b7e-150">Нажмите кнопку **Добавить**![Значок добавления](media/ITPro-EAC-AddIcon.gif) и выберите **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-150">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="78b7e-151">Укажите имя правила.</span><span class="sxs-lookup"><span data-stu-id="78b7e-151">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="78b7e-p109">Нажмите кнопку **Дополнительные параметры**. В разделе **Применить это правило, если** выберите **Тема или текст** \> **тема включает любое из этих слов**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-p109">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>
    
5. <span data-ttu-id="78b7e-154">В диалоговом окне **Задайте слова или фразы** добавьте следующие фразы, которые часто используются в массовых сообщениях, по одному и затем нажмите кнопку **ОК**:</span><span class="sxs-lookup"><span data-stu-id="78b7e-154">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="78b7e-155">чтобы изменить настройки или отписаться</span><span class="sxs-lookup"><span data-stu-id="78b7e-155">to change your preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="78b7e-156">Изменить настройки электронной почты или отписаться</span><span class="sxs-lookup"><span data-stu-id="78b7e-156">Modify email preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="78b7e-157">Это рекламное сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="78b7e-157">This is a promotional email</span></span>
    
   - <span data-ttu-id="78b7e-158">Вы получаете это сообщение, потому что вы запросили подписку</span><span class="sxs-lookup"><span data-stu-id="78b7e-158">You are receiving this email because you requested a subscription</span></span>
    
   - <span data-ttu-id="78b7e-159">щелкните здесь, чтобы отписаться</span><span class="sxs-lookup"><span data-stu-id="78b7e-159">click here to unsubscribe</span></span>
    
   - <span data-ttu-id="78b7e-160">Вы получили это сообщение, потому что вы подписаны на рассылку</span><span class="sxs-lookup"><span data-stu-id="78b7e-160">You have received this email because you are subscribed</span></span>
    
   - <span data-ttu-id="78b7e-161">Чтобы перестать получать наш новостной бюллетень</span><span class="sxs-lookup"><span data-stu-id="78b7e-161">If you no longer wish to receive our email newsletter</span></span>
    
   - <span data-ttu-id="78b7e-162">чтобы отписаться от этого бюллетеня</span><span class="sxs-lookup"><span data-stu-id="78b7e-162">to unsubscribe from this newsletter</span></span>
    
   - <span data-ttu-id="78b7e-163">Если у вас возникают проблемы с просмотром этого сообщения</span><span class="sxs-lookup"><span data-stu-id="78b7e-163">If you have trouble viewing this email</span></span>
    
   - <span data-ttu-id="78b7e-164">Это реклама</span><span class="sxs-lookup"><span data-stu-id="78b7e-164">This is an advertisement</span></span>
    
   - <span data-ttu-id="78b7e-165">вы хотите отписаться или изменить</span><span class="sxs-lookup"><span data-stu-id="78b7e-165">you would like to unsubscribe or change your</span></span>
    
   - <span data-ttu-id="78b7e-166">просмотреть это сообщение как веб-страницу</span><span class="sxs-lookup"><span data-stu-id="78b7e-166">view this email as a webpage</span></span>
    
   - <span data-ttu-id="78b7e-167">Вы получили это сообщение, потому что вы подписаны на рассылку</span><span class="sxs-lookup"><span data-stu-id="78b7e-167">You are receiving this email because you are subscribed</span></span>
    
   <span data-ttu-id="78b7e-p110">**Примечание**: еще раз, этот список не исчерпывающий набор фраз, которые используются в массовых сообщениях; Дополнительные можно добавлять или удалять при необходимости. Тем не менее он является хорошей отправной точкой.</span><span class="sxs-lookup"><span data-stu-id="78b7e-p110">**Note**: Once again, this list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
6. <span data-ttu-id="78b7e-170">В разделе **Выполните следующее** выберите пункт **Изменить свойства сообщения** \> **задать значение для вероятности нежелательной почты (SCL)**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-170">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="78b7e-171">В диалоговом окне **Укажите вероятность нежелательной почты** выберите для SCL значение **5**, **6** или **9** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78b7e-171">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="78b7e-p111">Выбор для SCL значения 5 или 6 приводит к выполнению действия **Нежелательная почта**. Выбор значения 9 приводит к выполнению действия **Нежелательное сообщение высокого уровня** согласно настройке политики фильтрации содержимого. Служба выполняет действие, указанное в политике фильтрации содержимого. По умолчанию это действие  доставка сообщения в папку получателя "Нежелательная почта", однако можно настроить и другие действия, как описано в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="78b7e-p111">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="78b7e-175">Если настроенные действие заключается в карантин сообщения, а не отправьте его в папку нежелательной почты получателей, это сообщение будет отправлено в карантин администратор, как соответствие правила потока обработки почты и оно не будет доступен в карантину нежелательной почты или с помощью конечных пользователей защиты от нежелательной почты уведомления.</span><span class="sxs-lookup"><span data-stu-id="78b7e-175">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="78b7e-176">Дополнительные сведения о значениях SCL в службе см. в статье [Вероятность нежелательной почты](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="78b7e-176">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="78b7e-177">Сохраните правило.</span><span class="sxs-lookup"><span data-stu-id="78b7e-177">Save the rule.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="78b7e-178">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="78b7e-178">For more information</span></span>

[<span data-ttu-id="78b7e-179">В чем разница между нежелательной почтой и массовыми сообщениями электронной почты?</span><span class="sxs-lookup"><span data-stu-id="78b7e-179">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)

[<span data-ttu-id="78b7e-180">Уровни жалоб на массовые сообщения</span><span class="sxs-lookup"><span data-stu-id="78b7e-180">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)

[<span data-ttu-id="78b7e-181">Настройте политики защиты от спама</span><span class="sxs-lookup"><span data-stu-id="78b7e-181">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="78b7e-182">Дополнительные параметры фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="78b7e-182">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
