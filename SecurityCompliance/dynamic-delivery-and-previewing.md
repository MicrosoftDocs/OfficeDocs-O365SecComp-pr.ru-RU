---
title: Динамические доставки и предварительный просмотр с Office 365 ATP безопасные вложения
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
description: При настройке политик безопасные вложения ATP выберите динамических доставки, чтобы избежать задержек сообщение и включить людей для предварительного просмотра вложений, которые выполняется сканирование.
ms.openlocfilehash: b7b5f05170e6f27cbec9e0d5a121b2f71f16f41a
ms.sourcegitcommit: cda46434094bc2837dba90256d044ba77552df12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/30/2018
ms.locfileid: "25850823"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="9c7e8-103">Динамические доставки и предварительный просмотр с Office 365 ATP безопасные вложения</span><span class="sxs-lookup"><span data-stu-id="9c7e8-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="9c7e8-p101">**Сводка**: динамические доставки — это параметр, который можно выбрать для [Анализа безопасные вложения](atp-safe-attachments.md). В этой статье, чтобы узнать о динамических доставки и возможности предварительного просмотра вложений в [ATP безопасные вложения в Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="9c7e8-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="9c7e8-106">Как работает динамических доставки</span><span class="sxs-lookup"><span data-stu-id="9c7e8-106">How Dynamic Delivery works</span></span>

<span data-ttu-id="9c7e8-p102">Если [Настройка политики ATP безопасные вложения](set-up-atp-safe-attachments-policies.md) для вашей организации, существует несколько вариантов для обработки вложений электронной почты. К ним относятся **блокировки**, **Замена**и **Динамических доставки**. В зависимости от того, как безопасные вложения ATP политик получателям сообщений электронной почты можно задержка незначительные доставки сообщений электронной почты во время их вложений, выполняется поиск вирусов. Чтобы избежать задержек сообщения, выберите **Динамических доставки**.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients can experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
<span data-ttu-id="9c7e8-p103">Динамические доставки устраняет задержки электронной почты, отправив тело сообщения электронной почты через получателю с заполнитель для каждого вложения электронной почты. Заполнитель остается до сканирования и определяет, какие безопасные [ATP безопасные вложения](atp-safe-attachments.md)копия вложения. Большинство PDF-файлов и Office документов можно просматривать в безопасном режиме, во время сканирования анализа. Вложение не совместим с средство просмотра динамических доставки, получателям сообщений электронной почты в статье местозаполнитель вложения до завершения анализа безопасные вложения сканирования.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md). Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

- <span data-ttu-id="9c7e8-115">Как очищенные каждого вложения, может использоваться для открытия или загрузки.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-115">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="9c7e8-116">Если вложение определяется как вредоносных, оно отправляется карантина, где другого пользователя в группу безопасности вашей организации (например, Office 365 глобальный администратор или администратор безопасности) можно [управлять сообщений на карантине в Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="9c7e8-116">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="9c7e8-117">С помощью динамических доставки получателям сообщений электронной почты можно читать и отвечать на сообщения электронной почты, помещенные сразу, знать, что их вложений выполнения анализа.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-117">With Dynamic Delivery, email recipients can read and respond to their email messages right away, knowing that their attachments are being analyzed.</span></span> 

<span data-ttu-id="9c7e8-p104">Безопасные вложения ATP сканирования вступит размещение в той же области, где находятся данные Office 365. Дополнительные сведения о geography центр данных можно [которых является данных находится?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="9c7e8-p104">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="9c7e8-120">Что происходит, когда кто-то отправляет сообщение электронной почты, которое содержит вложение?</span><span class="sxs-lookup"><span data-stu-id="9c7e8-120">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="9c7e8-p105">Предположим, что организация использует динамические доставки для их [анализа безопасные вложения политики](set-up-atp-safe-attachments-policies.md)и будет получено сообщение электронной почты с вложением. Теперь предположим, что он является переслать сообщение электронной почты другому пользователю. Что происходит? Он зависит от включении дополнительных получателей в политиках ATP безопасные вложения.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-p105">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person is about to forward the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="9c7e8-125">Если получатель будет рассмотрен политикой ATP безопасные вложения, выбрав пункт динамического доставки, получатель видит заполнитель с возможностью предварительного просмотра совместимые файлы.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-125">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="9c7e8-126">Если получатель не рассматриваются политикой ATP безопасные вложения, затем электронной почты и вложению проходит через, без безопасные вложения ATP сканирования и заполнители вложения.</span><span class="sxs-lookup"><span data-stu-id="9c7e8-126">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="9c7e8-127">Что необходимо для динамического доставки для работы?</span><span class="sxs-lookup"><span data-stu-id="9c7e8-127">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="9c7e8-128">Вашей организации должен иметь [Защиты расширенного Threat Office 365](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="9c7e8-128">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="9c7e8-129">Политики должны быть определены для анализа безопасные вложения с помощью параметра динамического доставки (см. [Настройка политики ATP безопасные вложения в Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="9c7e8-129">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="9c7e8-130">Электронной почты вашей организации должны быть размещены в Office 365</span><span class="sxs-lookup"><span data-stu-id="9c7e8-130">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="9c7e8-131">Существуют ли сценариев, для которых динамических доставки недоступен?</span><span class="sxs-lookup"><span data-stu-id="9c7e8-131">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="9c7e8-p106">Существуют некоторые сценарии, в которых не поддерживается динамической доставки. К ним относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="9c7e8-p106">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="9c7e8-134">Сообщения электронной почты, которые находятся в общих папках</span><span class="sxs-lookup"><span data-stu-id="9c7e8-134">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="9c7e8-135">Сообщения электронной почты, которые направляются об отсутствии на работе, а затем обратно в почтовый ящик пользователя с помощью настраиваемого правила</span><span class="sxs-lookup"><span data-stu-id="9c7e8-135">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="9c7e8-136">Сообщения, которые перемещаются (автоматически или вручную) из размещенной почтовых ящиков и в других местах, включая папки архива</span><span class="sxs-lookup"><span data-stu-id="9c7e8-136">Messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="9c7e8-137">Сообщения, которые будут удалены</span><span class="sxs-lookup"><span data-stu-id="9c7e8-137">Messages that are deleted</span></span>
    
- <span data-ttu-id="9c7e8-138">Папки поиска почтового ящика пользователя, который находится в состоянии ошибки</span><span class="sxs-lookup"><span data-stu-id="9c7e8-138">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="9c7e8-p107">Среды, в которых администратор Exchange Online включил Exclaimer. (Видеть [сообщения с вложениями не удается доставить при использовании доставки динамического анализа и Exclaimer](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span><span class="sxs-lookup"><span data-stu-id="9c7e8-p107">Environments in which an Exchange Online admin has enabled Exclaimer. (See [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery))</span></span>

- <span data-ttu-id="9c7e8-141">Сообщения, зашифрованные с безопасные многоцелевые расширения почтового стандарта Интернета ([S/MIME](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="9c7e8-141">Messages encrypted with Secure/Multipurpose Internet Mail Extensions ([S/MIME](s-mime-for-message-signing-and-encryption.md))</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="9c7e8-142">См. также:</span><span class="sxs-lookup"><span data-stu-id="9c7e8-142">Related topics</span></span>

[<span data-ttu-id="9c7e8-143">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="9c7e8-143">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="9c7e8-144">Безопасно ATP вложений в Office 365</span><span class="sxs-lookup"><span data-stu-id="9c7e8-144">ATP Safe Attachments in Office 365</span></span>](atp-safe-attachments.md)
  
[<span data-ttu-id="9c7e8-145">Настройка политик ATP безопасные вложения в Office 365</span><span class="sxs-lookup"><span data-stu-id="9c7e8-145">Set up ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
  
[<span data-ttu-id="9c7e8-146">Безопасно ATP ссылок в Office 365</span><span class="sxs-lookup"><span data-stu-id="9c7e8-146">ATP Safe Links in Office 365</span></span>](atp-safe-links.md)

[<span data-ttu-id="9c7e8-147">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="9c7e8-147">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

