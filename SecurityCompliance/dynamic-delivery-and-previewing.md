---
title: Динамические доставки и предварительный просмотр с Office 365 ATP безопасные вложения
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: При настройке политик безопасные вложения ATP выберите динамических доставки, чтобы избежать задержек сообщение и включить людей для предварительного просмотра вложений, которые выполняется сканирование.
ms.openlocfilehash: 23ef316ed35b89ef1fad5e9639dd10e76036a4f3
ms.sourcegitcommit: 82fd4c85b952819157fbb13175c7b2dbbdff510f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2018
ms.locfileid: "23965246"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="e0f41-103">Динамические доставки и предварительный просмотр с Office 365 ATP безопасные вложения</span><span class="sxs-lookup"><span data-stu-id="e0f41-103">Dynamic delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="e0f41-p101">Динамические доставки — это параметр, который можно выбрать для. В этой статье, чтобы узнать о динамических доставки и возможности предварительного просмотра вложений в [ATP безопасные вложения в Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="e0f41-p101">Dynamic delivery is an option that can be selected for . Read this article to learn about dynamic delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="e0f41-106">Как динамические works доставки</span><span class="sxs-lookup"><span data-stu-id="e0f41-106">How dynamic delivery works</span></span>

<span data-ttu-id="e0f41-p102">При [политиках ATP безопасные вложения в Office 365](set-up-atp-safe-attachments-policies.md), можно выбрать из нескольких параметров, таких как **блокировки**, **Замена**и **Динамических доставки**. В зависимости от способа настройки политики получателям сообщений электронной почты можно задержка незначительные доставки сообщений электронной почты во время их вложений, выполняется поиск вирусов. Чтобы избежать задержек сообщения, выберите **Динамических доставки**.</span><span class="sxs-lookup"><span data-stu-id="e0f41-p102">When you [set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md), you can choose from several options, such as **Block**, **Replace**, and **Dynamic Delivery**. Depending on how your policies are configured, email recipients can experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
<span data-ttu-id="e0f41-p103">Параметр динамического доставки устраняет задержки электронной почты, отправив тело сообщения электронной почты через с заполнитель для каждого вложения электронной почты. Заполнитель остается до сканирования вложение [ATP безопасные вложения в Office 365](atp-safe-attachments.md). Получателям сообщений электронной почты можно читать и отвечать на сообщения электронной почты, помещенные сразу знать, что их вложений выполнения анализа.</span><span class="sxs-lookup"><span data-stu-id="e0f41-p103">The dynamic delivery option eliminates email delays by sending the body of an email message through with a placeholder for each email attachment. The placeholder remains until the attachment is scanned by [ATP Safe Attachments in Office 365](atp-safe-attachments.md). Email recipients can read and respond to their email messages right away, knowing that their attachments are being analyzed.</span></span>
  
<span data-ttu-id="e0f41-p104">Большинство PDF-файлов и Office документов можно просматривать в безопасном режиме, во время сканирования анализа. Вложение не совместим с средство просмотра динамических доставки, получателям сообщений электронной почты в статье заполнитель вложения до завершения анализа безопасные вложения сканирования.</span><span class="sxs-lookup"><span data-stu-id="e0f41-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the dynamic delivery previewer, email recipients see the attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>
  
<span data-ttu-id="e0f41-p105">Что снят каждого вложения, она автоматически присоединению исходное сообщение электронной почты. Если вложение определяется как вредоносных, оно отправляется карантина, где другого пользователя в группу безопасности вашей организации (например, Office 365 глобальный администратор или администратор безопасности) можно [управлять сообщений на карантине в Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="e0f41-p105">As each attachment is cleared, it is automatically reattached to the original email message. If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="e0f41-117">Что происходит, когда кто-то отправляет сообщение электронной почты, которое содержит вложение?</span><span class="sxs-lookup"><span data-stu-id="e0f41-117">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="e0f41-p106">Предположим, что организация использует динамические доставки для их [анализа безопасные вложения политики](set-up-atp-safe-attachments-policies.md)и будет получено сообщение электронной почты с вложением. Теперь предположим, что он является переслать сообщение электронной почты другому пользователю. Что происходит? Он зависит от включении дополнительных получателей в политиках ATP безопасные вложения.</span><span class="sxs-lookup"><span data-stu-id="e0f41-p106">Suppose that an organization is using dynamic delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person is about to forward the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="e0f41-122">Если получатель будет рассмотрен политикой ATP безопасные вложения, выбрав пункт динамического доставки, получатель видит заполнитель с возможностью предварительного просмотра совместимые файлы.</span><span class="sxs-lookup"><span data-stu-id="e0f41-122">If a recipient is covered by an ATP Safe Attachments policy using the dynamic delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="e0f41-123">Если получатель не рассматриваются политикой ATP безопасные вложения, затем электронной почты и вложению проходит через, без безопасные вложения ATP сканирования и заполнители вложения.</span><span class="sxs-lookup"><span data-stu-id="e0f41-123">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="e0f41-124">Что необходимо для динамического доставки для работы?</span><span class="sxs-lookup"><span data-stu-id="e0f41-124">What's required for dynamic delivery to work?</span></span>

- <span data-ttu-id="e0f41-125">Вашей организации должен иметь [Защиты расширенного Threat Office 365](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="e0f41-125">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="e0f41-126">Политики должны быть определены для анализа безопасные вложения с помощью параметра динамического доставки (см. [Настройка политики ATP безопасные вложения в Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="e0f41-126">Policies must be defined for ATP Safe Attachments using the dynamic delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="e0f41-127">Электронной почты вашей организации должны быть размещены в Office 365</span><span class="sxs-lookup"><span data-stu-id="e0f41-127">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="e0f41-128">Существуют ли сценариев, для которых динамических доставки недоступен?</span><span class="sxs-lookup"><span data-stu-id="e0f41-128">Are there scenarios for which dynamic delivery is not available?</span></span>

<span data-ttu-id="e0f41-p107">Существуют некоторые сценарии, в которых не поддерживается динамической доставки. К ним относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="e0f41-p107">There are certain scenarios in which dynamic delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="e0f41-131">Сообщения электронной почты, которые находятся в общих папках</span><span class="sxs-lookup"><span data-stu-id="e0f41-131">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="e0f41-132">Сообщения электронной почты, которые направляются об отсутствии на работе, а затем обратно в почтовый ящик пользователя с помощью настраиваемого правила</span><span class="sxs-lookup"><span data-stu-id="e0f41-132">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="e0f41-133">Сообщения, которые перемещаются (автоматически или вручную) из размещенной почтовых ящиков и в других местах, включая папки архива</span><span class="sxs-lookup"><span data-stu-id="e0f41-133">Messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="e0f41-134">Сообщения, которые будут удалены</span><span class="sxs-lookup"><span data-stu-id="e0f41-134">Messages that are deleted</span></span>
    
- <span data-ttu-id="e0f41-135">Папки поиска почтового ящика пользователя, который находится в состоянии ошибки</span><span class="sxs-lookup"><span data-stu-id="e0f41-135">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="e0f41-p108">Среды, в которых администратор Exchange Online включил Exclaimer. (Видеть [сообщения с вложениями не удается доставить при использовании доставки динамического анализа и Exclaimer](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span><span class="sxs-lookup"><span data-stu-id="e0f41-p108">Environments in which an Exchange Online admin has enabled Exclaimer. (See [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span></span>

- <span data-ttu-id="e0f41-138">Сообщения, зашифрованные с безопасные многоцелевые расширения почтового стандарта Интернета ([S/MIME](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="e0f41-138">Messages encrypted with Secure/Multipurpose Internet Mail Extensions ([S/MIME](s-mime-for-message-signing-and-encryption.md))</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="e0f41-139">Смежные темы</span><span class="sxs-lookup"><span data-stu-id="e0f41-139">Related topics</span></span>

[<span data-ttu-id="e0f41-140">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e0f41-140">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="e0f41-141">Безопасно ATP вложений в Office 365</span><span class="sxs-lookup"><span data-stu-id="e0f41-141">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)
  
[<span data-ttu-id="e0f41-142">Настройка политик ATP безопасные вложения в Office 365</span><span class="sxs-lookup"><span data-stu-id="e0f41-142">Set up ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
  
[<span data-ttu-id="e0f41-143">Безопасно ATP ссылок в Office 365</span><span class="sxs-lookup"><span data-stu-id="e0f41-143">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)

[<span data-ttu-id="e0f41-144">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="e0f41-144">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

