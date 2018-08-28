---
title: В чем разница между нежелательной почтой и массовыми сообщениями электронной почты?
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/7/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
description: Клиенты иногда askwhat's разница между нежелательной почтой и массовых сообщений электронной почты? Этот раздел предназначен для пояснения разницы и приведены сведения о различных параметрах, доступных для них в Exchange Online и Exchange Online Protection (EOP).
ms.openlocfilehash: 2cd9d9d91cf44af910983c045192ed7639d27417
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026246"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a><span data-ttu-id="7665a-103">В чем разница между нежелательной почтой и массовыми сообщениями электронной почты?</span><span class="sxs-lookup"><span data-stu-id="7665a-103">What's the difference between junk email and bulk email?</span></span>

<span data-ttu-id="7665a-p101">Иногда пользователи спрашивают: "В чем разница между нежелательной почтой и массовыми сообщениями электронной почты?". В этом разделе описываются различия, а также различные параметры, доступные для Exchange Online и Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="7665a-p101">Customers sometimes ask "what's the difference between junk email and bulk email messages?" The purpose of this topic is to explain the difference and to provide information about the different options that are available for both in Exchange Online and Exchange Online Protection (EOP).</span></span>
  
 <span data-ttu-id="7665a-106">**Что такое нежелательная почта?**</span><span class="sxs-lookup"><span data-stu-id="7665a-106">**What's junk email?**</span></span>
  
<span data-ttu-id="7665a-p102">Нежелательные сообщения  это "спам", т. е. незапрашиваемые (и обычно совсем не желательные) сообщения электронной почты, фильтруемые службой. По умолчанию служба отклоняет нежелательное сообщение, основываясь на репутации IP-адреса отправителя. Однако если сообщение проходит проверку IP-адреса, но классифицируется как нежелательное фильтрами содержимого, оно отправляется в папку "Нежелательные сообщения" получателей.</span><span class="sxs-lookup"><span data-stu-id="7665a-p102">Junk email messages are "spam" messages, which are unsolicited (and typically unwanted) email messages that are filtered by the service. By default, the service rejects the spam message based on the reputation of the sending IP address. However, if it passes IP inspection but is classified as spam by the content filters, the message is sent to the Junk Email folder of the intended recipients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7665a-p103">Действие, выполняемое с такими сообщениями, можно настроить с помощью политик фильтрации содержимого в центре администрирования Exchange (EAC), как описано в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md). Кроме того, если вы не согласны с классификацией определенных сообщений, вы можете отправить их корпорации Майкрософт, используя несколько способов, как описано в разделе [Отправка обычных, нежелательных и фишинговых сообщений в корпорацию Майкрософт для анализа](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7665a-p103">The action performed on content-filtered messages is configurable via content filter policies in the Exchange admin center (EAC), as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md). Also, if you disagree with the spam classification, you can report messages that you consider to be spam or non-spam to Microsoft in several ways, as described in [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> 
  
 <span data-ttu-id="7665a-112">**Что такое массовые сообщения электронной почты?**</span><span class="sxs-lookup"><span data-stu-id="7665a-112">**What's bulk email?**</span></span>
  
<span data-ttu-id="7665a-p104">Массовые сообщения электронной почты, которые также называют "серой" почтой  это более трудно классифицируемый тип почтовых сообщений. Нежелательная почта  это стопроцентная угроза, а массовые сообщения содержат рекламную информацию, которая вряд ли будет отправляться периодически. Для некоторых пользователей массовые сообщения являются желательными, например если они преднамеренно подписались на них, а другие же пользователи могут считать такие сообщения нежелательными. Например, некоторые пользователи могут желать получать рекламные сообщения от Contoso Corporation или приглашения на предстоящую конференцию по кибербезопасности, в то время как другие пользователи посчитают такие сообщения спамом.</span><span class="sxs-lookup"><span data-stu-id="7665a-p104">Bulk email, also referred to as gray mail, is a type of email message that's more difficult to classify. Whereas junk email is a constant threat, bulk email is typically comprised of an advertisement or marketing message that's not likely to get sent repeatedly. Bulk email is wanted by some users, and in fact they may have deliberately signed up to receive these messages, while other users may consider these types of messages to be spam. For example, some users want to receive advertising emails from the Contoso Corporation or invitations to an upcoming conference on cyber security, while other users consider such emails to be spam.</span></span>
  
## <a name="how-to-manage-bulk-email"></a><span data-ttu-id="7665a-117">Управление массовыми сообщениями электронной почты</span><span class="sxs-lookup"><span data-stu-id="7665a-117">How to manage bulk email</span></span>

<span data-ttu-id="7665a-p105">Способ управления массовыми сообщениями электронной почты выбрать не так просто, так как если все они будут классифицированы как нежелательные, пользователи могут начать жаловаться и отправлять их как ложные положительные срабатывания (не являющиеся нежелательными), которые были неверно классифицированы как спам. С другой стороны, если пропускать все массовые сообщения электронной почты, пользователи, которые не хотят их получать, будут отправлять их как пропущенные нежелательные сообщения (ложные отрицательные срабатывания), которые не по праву попали в папку "Входящие",</span><span class="sxs-lookup"><span data-stu-id="7665a-p105">How to manage bulk email isn't a clear cut decision, because if all bulk email is classified as spam, the users that want it may complain and submit it as a false positive (non-spam) message that was wrongly marked as spam. On the other hand, if all bulk email is let through, the users that don't want it may complain and submit it as a missed spam message (false negative) that wrongly arrived in their inbox.</span></span>
  
### <a name="enable-bulk-mail-sensitivity-control-in-the-content-filter-policy"></a><span data-ttu-id="7665a-120">Включение управление чувствительностью массовой почты в политике фильтрации содержимого</span><span class="sxs-lookup"><span data-stu-id="7665a-120">Enable bulk mail sensitivity control in the content filter policy</span></span>

<span data-ttu-id="7665a-p106">В зависимости от политики компании в отношении массовой рассылки, администраторы могут выбрать пороговое значение для такой рассылки. Этот параметр можно изменить с помощью политики фильтрации содержимого в Центре администрирования Exchange. Сведения об этом см. в статье [Настройте политики защиты от спама](configure-your-spam-filter-policies.md). Вы можете выбрать пороговое значение с 1 до 9. При использовании 1 большая часть сообщений массовой рассылки помечается как спам, а при использовании 9 разрешается отправка большинства таких сообщений. После этого служба выполняет настроенное действие (например, перемещает сообщение в папку "Нежелательная почта" получателя).</span><span class="sxs-lookup"><span data-stu-id="7665a-p106">Depending on your company's policy on bulk email messages, admins can select a threshold to assign the bulk email. The setting is is configurable via content filter policies in the EAC. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md)) for the steps. You can choose a threshold setting from 1 - 9, where 1 marks most bulk email as spam, and 9 allows the most bulk email to be delivered. The service then performs the configured action, such as sending the message to the recipient's Junk Email folder.</span></span> 
  
