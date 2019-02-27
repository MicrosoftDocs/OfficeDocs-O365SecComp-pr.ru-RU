---
title: ПоШаговое руководство по подделке для анализа
ms.author: tracyp
author: MSFTTracyP
ms.date: 7/30/2018
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 59a3ecaf-15ed-483b-b824-d98961d88bdd
ms.collection:
- M365-security-compliance
description: Узнайте, как работает новая аналитика подделки.
ms.openlocfilehash: 4303b8f2524e6722e7febbbd06ab9daa853ed802
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275919"
---
# <a name="walkthrough-spoof-intelligence-insight"></a><span data-ttu-id="600e1-103">ПоШаговое руководство: аналитика подделки</span><span class="sxs-lookup"><span data-stu-id="600e1-103">Walkthrough: spoof intelligence insight</span></span>

<span data-ttu-id="600e1-p101">С помощью анализа анализа подДелки можно быстро определить, какие отправители подлиннее отправляют вам сообщения, не прошедшие проверку подлинности. Если вы разрешаете отправлять поддельные сообщения, вы можете снизить риск возникновения любых ложных срабатываний, отправляемых пользователям.</span><span class="sxs-lookup"><span data-stu-id="600e1-p101">By using the Spoof Intelligence insight, you can quickly determine which senders are legitimately sending you unauthenticated email. By permitting them to send spoofed messages, you can reduce the risk of any false positives going to your users.</span></span>
  
<span data-ttu-id="600e1-106">Кроме того, можно использовать монитор логики подДелки и управлять разрешенными парами доменов, чтобы обеспечить дополнительный уровень безопасности и предотвратить поступление небезопасных сообщений в организацию.</span><span class="sxs-lookup"><span data-stu-id="600e1-106">In addition, you can also use Spoof Intelligence monitor and manage permitted domain-pairs to provide an additional layer of security and prevent unsafe messages from arriving in your organization.</span></span>
  
<span data-ttu-id="600e1-p102">Вы можете использовать сведения о подделке в центре безопасности &amp; , если ваша рабочая или учебная учетная запись была предоставлена пользователям Office 365 глобальный администратор, администратор безопасности или средство чтения безопасности. Дополнительные сведения см. [в разделе разрешения в центре безопасности &amp; и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="600e1-p102">You can use the spoof intelligence insight in the Security &amp; Compliance Center if your work or school account has been given Office 365 global administrator, security administrator, or security reader permissions. For more information, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
<span data-ttu-id="600e1-109">Если вы не знакомы с [отчетами и аналитическими сведениями в центре безопасности &amp; и соответствия требованиям Office 365](reports-and-insights-in-security-and-compliance.md), то можете понять, как легко переходить с панели мониторинга на подробные и рекомендуемые действия.</span><span class="sxs-lookup"><span data-stu-id="600e1-109">If you're new to [reports and insights in the Office 365 Security &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md), it might help to see how you can easily navigate from a dashboard to an insight and recommended actions.</span></span>
  
<span data-ttu-id="600e1-p103">В центре безопасности &amp; и соответствия требованиям вы можете просмотреть сведения о подделке. Независимо от того, какая панель мониторинга отображается, сведения о ней представлены одинаково и позволяют быстро выполнять те же задачи.</span><span class="sxs-lookup"><span data-stu-id="600e1-p103">You can view the spoof intelligence insight from more than one dashboard in the Security &amp; Compliance Center. Regardless of which dashboard you're looking at, the insight provides the same details and allows you to quickly perform the same tasks.</span></span>
  
<span data-ttu-id="600e1-p104">Это одно из нескольких пошаговых руководств для центра &amp; безопасности и соответствия требованиям. Сведения о том, как переходить по отчетам и аналитическим сведениям, можно найти в пошаговых руководствах раздела "связанные темы".</span><span class="sxs-lookup"><span data-stu-id="600e1-p104">This is one of several walkthroughs for the Security &amp; Compliance Center. To about navigating reports and insights, see the walkthroughs in the Related topics section.</span></span>
  
## <a name="getting-to-the-spoof-intelligence-insight-in-the-security-amp-compliance-center"></a><span data-ttu-id="600e1-114">Получение сведений о подделке в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="600e1-114">Getting to the spoof intelligence insight in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="600e1-115">Чтобы приступить к работе, вам потребуется [Перейти в центр &amp; безопасности и соответствия требованиям](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="600e1-115">To get started, you'll need [go to the Security &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span></span>
    
2. <span data-ttu-id="600e1-116">В центре безопасности &amp; и соответствия требованиям перейдите на **панель мониторинга** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="600e1-116">In the Security &amp; Compliance Center, go to **Threat Management** \> **Dashboard.**</span></span>
    
3. <span data-ttu-id="600e1-p105">В строке **аналитических сведений** найдите аналитику подделки. Если вы включили логику "анализ поддельных поддельных поддельных поддельных сведений", это подДельный **домен, который не прошел проверку подлинности за** Если вы не включили защиту от поддельных поддельных поддельных поддельных поддельных поддельных поддельных сведений, то вам будет предложено сделать это \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="600e1-p105">In the **Insights** row, look for the spoof intelligence insight. If you have enabled spoof intelligence, then the insight is entitled **Spoofed domains that failed authentication of the past 30 days**. If you haven't enabled spoof protection, then the insight will prompt you to do so by using the title **Enable Spoof Protection**.</span></span> 
    
## <a name="about-the-insight-on-the-dashboard"></a><span data-ttu-id="600e1-120">Сведения об аналитической панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="600e1-120">About the insight on the dashboard</span></span>

<span data-ttu-id="600e1-121">В панели мониторинга отображается информация, подобная приведенной ниже.</span><span class="sxs-lookup"><span data-stu-id="600e1-121">The insight on the dashboard shows you information like this.</span></span>
  
![Снимок экрана анализа анализа подделки](media/28aeabac-c1a1-4d16-9fbe-14996f742a9a.png)
  
<span data-ttu-id="600e1-123">Эта аналитика имеет два режима:</span><span class="sxs-lookup"><span data-stu-id="600e1-123">This insight has two modes:</span></span>
  
 <span data-ttu-id="600e1-p106">**Режим анализа**. Если у вас включена политика подмены, то в этой информации показывается, сколько почтовых ящиков было затронуты нашими функциями анализа подделки за прошедшие 30 дней.</span><span class="sxs-lookup"><span data-stu-id="600e1-p106">**Insight mode**. If you have any spoof policy enabled, then the insight shows you how many mails were impacted by our spoof intelligence capabilities over the past 30 days.</span></span> 
  
 <span data-ttu-id="600e1-p107">**Режим "что если**". Если политика подмены не включена, то в разделе сведения о количестве почтовых ящиков, на \*\* которые повлияла функция анализа подделки за прошедшие 30 дней.</span><span class="sxs-lookup"><span data-stu-id="600e1-p107">**What if mode**. If you do not have any spoof policy enabled, then the insight shows you how many mails  *would*  have been impacted by our spoof intelligence capabilities over the past 30 days.</span></span> 
  
<span data-ttu-id="600e1-p108">В обоих случаях поддельные домены, отображаемые в разделе Insights, делятся на две категории; подозрительные пары доменов и пары неподозрительных доменов. Эти категории далее делятся на три разных сегмента для просмотра.</span><span class="sxs-lookup"><span data-stu-id="600e1-p108">Either way, the spoofed domains displayed in the insight are separated into two categories; suspicious domain pairs and non-suspicious domain pairs. These categories are further subdivided into three different buckets for you to review.</span></span> 
  
<span data-ttu-id="600e1-130">*Пары домена* это сочетание адреса "от:" и инфраструктуры отправки.</span><span class="sxs-lookup"><span data-stu-id="600e1-130">A  *domain pair*  is a combination of the "From:" address and the sending infrastructure.</span></span> 
  
- <span data-ttu-id="600e1-p109">Адрес "от" — это адрес, отображаемый почтовым приложением как адрес отПравителя. Этот адрес определяет автора сообщения электронной почты. Это значит, что почтовый ящик человека или системы отвечает за написание сообщения. Иногда это называется адресом 5322. from.</span><span class="sxs-lookup"><span data-stu-id="600e1-p109">The "From" address is the address displayed as the From address by your mail application. This address identifies the author of the email. That is, the mailbox of the person or system responsible for writing the message. This is sometimes called the 5322.From address.</span></span>
    
- <span data-ttu-id="600e1-p110">Отправляющей инфраструктурой или отправителем является организационным доменом записи PTR для отправляющего IP-адреса. Если у отправляющего IP-адреса нет записи PTR, отправитель идентифицируется с помощью отправляющего IP-адреса с маской подсети 255.255.255.0 в нотации CIDR (/24). Например, если IP-адрес 192.168.100.100, то полный IP-адрес отправителя — 192.168.100.100/24.</span><span class="sxs-lookup"><span data-stu-id="600e1-p110">The sending infrastructure, or sender, is the organizational domain of the PTR record of the sending IP address. If the sending IP address has no PTR record, then the sender is identified by the sending IP with the 255.255.255.0 subnet mask in CIDR notation (/24). For example, if the IP address is 192.168.100.100 then the complete IP address of the sender is 192.168.100.100/24.</span></span>
    
 <span data-ttu-id="600e1-138">К **подозрительным парам доменов** относятся:</span><span class="sxs-lookup"><span data-stu-id="600e1-138">**Suspicious domain pairs** include:</span></span> 
  
- <span data-ttu-id="600e1-p111">**Подделка высокого уровня доверия**. Office 365 получил сильные сигналы о том, что эти домены являются подозрительными, в зависимости от исторических шаблонов отправки и оценки репутации доменов. Office 365 строго надежнее, так как домены поддаются подмене, а сообщения, отправляемые из этих доменов, считаются менее вероятными.</span><span class="sxs-lookup"><span data-stu-id="600e1-p111">**High-confidence spoof**. Office 365 received strong signals that these domains are suspicious, based on the historical sending patterns and the reputation score of the domains. Office 365 is highly confident that the domains are spoofing and that messages sent from these domains are less likely to be legitimate.</span></span> 
    
- <span data-ttu-id="600e1-p112">**Умеренное подмена**. Office 365 получил умеренные сигналы о том, что эти домены являются подозрительными, на основе прошлых шаблонов отправки и оценки репутации доменов. В Office 365 средний уровень уверенности в том, что домены являются подменами и сообщения, отправляемые из этих доменов, являются законными. Этот сегмент имеет большую вероятность того, что он содержит ложные срабатывания (кадров в процентах), чем сегмент подделки с высоким уровнем доверия.</span><span class="sxs-lookup"><span data-stu-id="600e1-p112">**Moderate confidence spoof**. Office 365 received moderate signals that these domains are suspicious, based on historical sending patterns and the reputation score of the domains. Office 365 is moderately confident that the domains are spoofing and that messages sent from these domains are legitimate. This bucket has a greater chance of containing false positives (FPs) than the high-confidence spoof bucket.</span></span> 
    
 <span data-ttu-id="600e1-p113">**Неподозрительные пары доменов** включают в себя **Аварийное подделку**. Аварийное подделка — домены, не прошедшие проверку подлинности ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)), но прошедшие проверку расширенной проверки подлинности. В результате Office 365 проводил сообщение от вашего имени и не предприняло никаких действий по борьбе с подменой почты.</span><span class="sxs-lookup"><span data-stu-id="600e1-p113">**Non-suspicious domain pairs** include **rescued spoof**. Rescued spoof are domains that have failed the explicit authentication checks ( [SPF](https://docs.microsoft.com/office365/SecurityCompliance/how-office-365-uses-spf-to-prevent-spoofing), [DKIM](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email), [DMARC](https://docs.microsoft.com/office365/SecurityCompliance/use-dmarc-to-validate-email)) but passed our extended authentication checks. As a result of this, Office 365 rescued the mail on your behalf and no anti-spoofing action was taken on the mail.</span></span> 
  
## <a name="view-detailed-information-about-suspicious-domain-pairs-from-the-spoof-intelligence-insight"></a><span data-ttu-id="600e1-149">Просмотр подробных сведений о подозрительных парах доменов из аналитической аналитики подделки</span><span class="sxs-lookup"><span data-stu-id="600e1-149">View detailed information about suspicious domain pairs from the spoof intelligence insight</span></span>

1. <span data-ttu-id="600e1-150">В поддельной информации выберите любую из пар доменов (высокая, средняя или копия).</span><span class="sxs-lookup"><span data-stu-id="600e1-150">On the spoof intelligence insight, click any of the domain pairs (high, moderate, or rescued).</span></span>
  
<span data-ttu-id="600e1-p114">Отобразится страница "сведения о **подделке** ", в которой отображается список отправителей, которые отправляют в организацию непроверенные сообщения. Сведения на этой странице помогут определить, авторизованы ли подложные сообщения или нет или требуется предпринять дальнейшие действия. Вы можете отсортировать информацию по количеству сообщений, дате и времени последнего обнаружения подделки и т. д. (Например, "количество сообщений" или " **Последнее**Просмотр" (например, " **количество сообщений** ").</span><span class="sxs-lookup"><span data-stu-id="600e1-p114">The **Spoof Intelligence Insight** page appears showing you a list of senders that are sending unauthenticated mail into your organization. The information on this page helps you determine whether spoofed messages are authorized or not or if you need to take further action. You can sort the information by message count, the date the spoof was last detected, and more. (Click column headings, such as **Message count** or **Last seen**, for example.)</span></span> 
    
2. <span data-ttu-id="600e1-p115">Выберите элемент в таблице, чтобы открыть область сведений, содержащую обширные сведения об этой учетной записи, в том числе почему мы перехватили это, что нужно сделать, сводка по домену, данные WhoIs о отправителе и Похожие сообщения электронной почты, которые мы видели у того же отправителя. Отсюда вы можете добавить или удалить комбинацию домена из списка надежных отправителей **алловедтоспуф** .</span><span class="sxs-lookup"><span data-stu-id="600e1-p115">Select an item in the table to open a details pane that contains rich information about the domain pair, including why we caught this, what you need to do, a domain summary, WhoIs data about the sender, and similar emails we have seen in your tenant from the same sender. From here, you can also choose to add or remove the domain pair from the **AllowedToSpoof** safe sender list.</span></span> 
  
![Снимок экрана с доменом в области подробных сведений о поддельной информации](media/03ad3e6e-2010-4e8e-b92e-accc8bbebb79.png)
  
## <a name="add-or-remove-a-domain-from-the-allowedtospoof-safe-sender-list"></a><span data-ttu-id="600e1-158">Добавление или удаление домена из списка надежных отправителей Алловедтоспуф</span><span class="sxs-lookup"><span data-stu-id="600e1-158">Add or remove a domain from the AllowedToSpoof safe sender list</span></span>

<span data-ttu-id="600e1-p116">Вы добавляете или удаляете домен из списка надежных отправителей Алловедтоспуф, а затем просматриваете доменную информацию в области сведений в области сведений о подделке. Просто установите переключатель соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="600e1-p116">You add or remove a domain from the AllowedToSpoof safe sender list while reviewing the domain pair in the details pane of the spoof intelligence insight. Simply set the toggle accordingly.</span></span>
  
<span data-ttu-id="600e1-p117">Это приводит к изменению пары доменных комбинаций поддельного домена и отправляющей инфраструктуры и не обеспечивает покрытие для всего поддельного домена или инфраструктуры отправки в изоляции. Например, если добавить следующую доменную связь в список разрешенных отправителей "Алловедтоспуф": подДельный *домен* "Gmail.com" и *отправляющий инфраструктуру* "TMS *. MX.com",* то подменить только почтовые сообщения из этой доменной области. Другие отправители, пытающиеся подделывать "gmail.com", и другие домены, которые "tms.mx.com" пытаются подменить, по-прежнему будут защищаться службой подделки.</span><span class="sxs-lookup"><span data-stu-id="600e1-p117">This modifies the unique domain pair combination of the spoofed domain and the sending infrastructure and does not provide coverage for the entire spoofed domain or the sending infrastructure in isolation. For example, if you add the following domain pair to the 'AllowedToSpoof' sender allow list:  *Spoofed Domain*  "gmail.com" and  *Sending Infrastructure*  "tms  *.mx.com",*  then only mail from that domain pair will be allowed to spoof. Other senders attempting to spoof "gmail.com", and other domains that "tms.mx.com" attempt to spoof will continue to be protected by spoof intelligence.</span></span> 
  
## <a name="related-topics"></a><span data-ttu-id="600e1-164">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="600e1-164">Related topics</span></span>

[<span data-ttu-id="600e1-165">Дополнительные сведения об аналитической защите от подделок</span><span class="sxs-lookup"><span data-stu-id="600e1-165">Learn more about spoof intelligence</span></span>](learn-about-spoof-intelligence.md)
  
[<span data-ttu-id="600e1-166">Защита от спуфинга в Office 365</span><span class="sxs-lookup"><span data-stu-id="600e1-166">Anti-spoofing protection in Office 365</span></span>](anti-spoofing-protection.md)
  
[<span data-ttu-id="600e1-167">Пошаговое руководство. Из панели мониторинга к аналитике</span><span class="sxs-lookup"><span data-stu-id="600e1-167">Walkthrough - From a dashboard to an insight</span></span>](from-a-dashboard-to-an-insight.md)
  
[<span data-ttu-id="600e1-168">Пошаговое руководство. Из подробного отчета к аналитике</span><span class="sxs-lookup"><span data-stu-id="600e1-168">Walkthrough - From a detailed report to an insight</span></span>](from-a-detailed-report-to-an-insight.md)
  
[<span data-ttu-id="600e1-169">Пошаговое руководство. Из аналитики к подробному отчету</span><span class="sxs-lookup"><span data-stu-id="600e1-169">Walkthrough - From an insight to a detailed report</span></span>](from-an-insight-to-a-detailed-report.md)
  

