---
title: Динамическая Доставка и предварительный просмотр с безопасными вложениями Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/08/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: f16c9928-8e3d-4219-b994-271dc9a16272
ms.collection:
- M365-security-compliance
description: Когда вы настраиваете политики безопасных вложений ATP, вы выбираете динамическое предоставление, чтобы избежать задержки сообщений и разрешить пользователям просматривать сканируемые вложения.
ms.openlocfilehash: 1fb221d28a4089db8a4278903107c610d6825f5e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218399"
---
# <a name="dynamic-delivery-and-previewing-with-office-365-atp-safe-attachments"></a><span data-ttu-id="c6cc6-103">Динамическая Доставка и предварительный просмотр с безопасными вложениями Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="c6cc6-103">Dynamic Delivery and previewing with Office 365 ATP Safe Attachments</span></span>

<span data-ttu-id="c6cc6-p101">**Сводка**. Динамическая доставка — это вариант, который можно выбрать для [безОпасных вложений ATP](atp-safe-attachments.md). В этой статье рассказывается о возможностях динамической доставки и предварительного просмотра вложений в [безопасных вложениях ATP в Office 365](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="c6cc6-p101">**Summary**: Dynamic Delivery is an option that can be selected for [ATP Safe Attachments](atp-safe-attachments.md). Read this article to learn about Dynamic Delivery and attachment preview capabilities in [ATP Safe Attachments in Office 365](atp-safe-attachments.md).</span></span>

<span data-ttu-id="c6cc6-p102">Если для организации [настроены политики безопасных вложенИй ATP](set-up-atp-safe-attachments-policies.md) , существует несколько способов обработки вложений электронной почты. К ним относятся **Блокировка**, **Замена**и **Динамическая доставка**. В зависимости от того, как настроены политики безОпасных вложений ATP, при сканировании их вложений могут возникать небольшие задержки при доставке электронных сообщений. Чтобы избежать задержки в сообщениях, выберите **Динамическая доставка**.</span><span class="sxs-lookup"><span data-stu-id="c6cc6-p102">When [ATP Safe Attachments policies are set up](set-up-atp-safe-attachments-policies.md) for your organization, there are several options for how email attachments are handled. These include **Block**, **Replace**, and **Dynamic Delivery**. Depending on how ATP Safe Attachments policies are configured, email recipients might experience a minor delay in email delivery while their attachments are scanned. To avoid message delays, choose **Dynamic Delivery**.</span></span>
  
## <a name="how-dynamic-delivery-works"></a><span data-ttu-id="c6cc6-110">Принцип работы динамической доставки</span><span class="sxs-lookup"><span data-stu-id="c6cc6-110">How Dynamic Delivery works</span></span>
  
<span data-ttu-id="c6cc6-p103">Динамическая доставка исключает задержки электронной почты, отправляя текст сообщения электронной почты получателю с заполнительом для каждого вложения электронной почты. Заполнитель остается до тех пор, пока копия вложения не будет проверена и не станет безопасной для [безопасных вложенИй ATP](atp-safe-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="c6cc6-p103">Dynamic Delivery eliminates email delays by sending the body of an email message through to the recipient with a placeholder for each email attachment. The placeholder remains until a copy of the attachment is scanned and determined to be safe by [ATP Safe Attachments](atp-safe-attachments.md).</span></span> 

- <span data-ttu-id="c6cc6-113">После очистки каждое вложение можно открыть или скачать.</span><span class="sxs-lookup"><span data-stu-id="c6cc6-113">As each attachment is cleared, it is available to open or download.</span></span> 

- <span data-ttu-id="c6cc6-114">Если вложение определено как вредоносное, оно отправляется в карантин, если кто-то из участников группы безопасности Организации (таких как глобальный администратор Office 365 или администратор безопасности) может [управлять сообщениями, помещенными в карантин в Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="c6cc6-114">If an attachment is determined to be malicious, it is sent to quarantine, where someone on your organization's security team (such as an Office 365 global administrator or security administrator) can [manage quarantined messages in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="c6cc6-p104">Большинство файлов PDF и документов Office можно просматривать в безопасном режиме, пока выполняется сканирование ATP. Если вложение несовместимо с предварительным просмотром динамической доставки, получатели сообщения видят заполнитель вложения до завершения проверки безОпасных вложений в ATP.</span><span class="sxs-lookup"><span data-stu-id="c6cc6-p104">Most PDFs and Office documents can be previewed in safe mode while ATP scanning is underway. If an attachment is not compatible with the Dynamic Delivery previewer, email recipients see an attachment placeholder until ATP Safe Attachments scanning is complete.</span></span>

> [!TIP]
> <span data-ttu-id="c6cc6-117">Если вы используете мобильное устройство, а PDF-файлы не отображаются в предварительном просмотре при динамической доСтавке, попробуйте войти в Office 365 с помощью браузера для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="c6cc6-117">If you're using a mobile device, and PDFs are not rendering in Dynamic Delivery previewer at first, try signing into Office 365 using your mobile browser.</span></span>

<span data-ttu-id="c6cc6-118">При динамической доСтавке люди могут читать и отвечать на сообщения электронной почты сразу же, пока их вложения анализируются.</span><span class="sxs-lookup"><span data-stu-id="c6cc6-118">With Dynamic Delivery, people can read and respond to their email messages right away, while their attachments are being analyzed.</span></span> 

<span data-ttu-id="c6cc6-p105">Проверка безОпасных вложений ATP выполняется в том же регионе, в котором хранятся данные Office 365. Для получения дополнительных сведений о географическом отношении центра обработки данных Узнайте, [где находятся ваши данные?](https://products.office.com/where-is-your-data-located?geo=All)</span><span class="sxs-lookup"><span data-stu-id="c6cc6-p105">ATP Safe Attachments scanning takes place in the same region where your Office 365 data resides. For more information about data center geography, see [Where is your data located?](https://products.office.com/where-is-your-data-located?geo=All)</span></span> 
  
## <a name="what-happens-when-someone-forwards-an-email-that-contains-an-attachment"></a><span data-ttu-id="c6cc6-121">Что происходит, когда кто-то пересылает сообщение электронной почты, которое содержит вложение?</span><span class="sxs-lookup"><span data-stu-id="c6cc6-121">What happens when someone forwards an email that contains an attachment?</span></span>

<span data-ttu-id="c6cc6-p106">Предположим, что Организация использует динамическую доставку для своей [политики безопасных вложенИй ATP](set-up-atp-safe-attachments-policies.md), а кто-то получает сообщение электронной почты, содержащее вложение. Теперь предположим, что пользователь переадресует сообщение электронной почты кому-то другому. Что происходит? Это зависит от того, включены ли дополнительные получатели в политики безОпасных вложений ATP.</span><span class="sxs-lookup"><span data-stu-id="c6cc6-p106">Suppose that an organization is using Dynamic Delivery for their [ATP Safe Attachments policy](set-up-atp-safe-attachments-policies.md), and someone receives an email that contains an attachment. Now suppose that person forwards the email message to someone else. What happens? It depends on whether the additional recipients are included in ATP Safe Attachments policies.</span></span>
  
- <span data-ttu-id="c6cc6-126">Если для получателя применяется политика безОпасных вложений ATP, использующая параметр динамической доставки, то получатель видит заполнитель с возможностью предварительного просмотра совместимых файлов.</span><span class="sxs-lookup"><span data-stu-id="c6cc6-126">If a recipient is covered by an ATP Safe Attachments policy using the Dynamic Delivery option, then the recipient sees the placeholder, with the ability to preview compatible files.</span></span>
    
- <span data-ttu-id="c6cc6-127">Если у получателя нет политики безОпасных вложений ATP, то электронная почта и вложение будут проходить без проверки безОпасных вложений ATP и заполнительов вложений.</span><span class="sxs-lookup"><span data-stu-id="c6cc6-127">If a recipient is not covered by an ATP Safe Attachments policy, then the email and attachment will go through, without ATP Safe Attachments scanning or attachment placeholders.</span></span>
    
## <a name="whats-required-for-dynamic-delivery-to-work"></a><span data-ttu-id="c6cc6-128">Что требуется для работы динамической доставки?</span><span class="sxs-lookup"><span data-stu-id="c6cc6-128">What's required for Dynamic Delivery to work?</span></span>

- <span data-ttu-id="c6cc6-129">В вашей организации должна быть установлена [расширенНая защита от угроз для Office 365](office-365-atp.md)</span><span class="sxs-lookup"><span data-stu-id="c6cc6-129">Your organization must have [Office 365 Advanced Threat Protection](office-365-atp.md)</span></span>
    
- <span data-ttu-id="c6cc6-130">Политики должны быть определены для безОпасных вложений ATP с помощью параметра динамической доставки (см. раздел [Настройка политик безопасных вложенИЙ ATP в Office 365](set-up-atp-safe-attachments-policies.md))</span><span class="sxs-lookup"><span data-stu-id="c6cc6-130">Policies must be defined for ATP Safe Attachments using the Dynamic Delivery option (See [Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md))</span></span>
    
- <span data-ttu-id="c6cc6-131">Электронная почта Организации должна размещаться в Office 365</span><span class="sxs-lookup"><span data-stu-id="c6cc6-131">Your organization's email must be hosted in Office 365</span></span>
    
## <a name="are-there-scenarios-for-which-dynamic-delivery-is-not-available"></a><span data-ttu-id="c6cc6-132">Существуют ли сценарии, для которых динамическая доставка недоступна?</span><span class="sxs-lookup"><span data-stu-id="c6cc6-132">Are there scenarios for which Dynamic Delivery is not available?</span></span>

<span data-ttu-id="c6cc6-p107">Существует несколько сценариев, в которых динамическая доставка не поддерживается. К ним относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="c6cc6-p107">There are certain scenarios in which Dynamic Delivery is not supported. These include the following:</span></span>
  
- <span data-ttu-id="c6cc6-135">Сообщения электронной почты, которые находятся в общедоступных папках</span><span class="sxs-lookup"><span data-stu-id="c6cc6-135">Email messages that are in public folders</span></span>
    
- <span data-ttu-id="c6cc6-136">Сообщения электронной почты, которые передаются из почтового ящика, а затем обратно в почтовый ящик пользователя с помощью настраиваемых правил</span><span class="sxs-lookup"><span data-stu-id="c6cc6-136">Email messages that are routed out of and then back into the user's mailbox using custom rules</span></span>
    
- <span data-ttu-id="c6cc6-137">Сообщения электронной почты, которые перемещаются (автоматически или вручную) из размещенного почтового ящика и в другие расположения, включая архивные папки</span><span class="sxs-lookup"><span data-stu-id="c6cc6-137">Email messages that are moved (automatically or manually) out of the hosted mailbox and into other locations, including archive folders</span></span>
    
- <span data-ttu-id="c6cc6-138">Удаленные сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="c6cc6-138">Email messages that are deleted</span></span>
    
- <span data-ttu-id="c6cc6-139">Папка поиска почтового ящика пользователя в состоянии ошибки</span><span class="sxs-lookup"><span data-stu-id="c6cc6-139">A user's mailbox search folder that is in an error state</span></span>
    
- <span data-ttu-id="c6cc6-p108">Среды, в которых администратор Exchange Online включил Ексклаимер. Чтобы устранить эту проблему, в статье [сообщения с вложениями не доставляются при использовании динамической доставки ATP и ексклаимер](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span><span class="sxs-lookup"><span data-stu-id="c6cc6-p108">Environments in which an Exchange Online admin has enabled Exclaimer. To resolve this, see [Messages with attachments are not delivered when ATP Dynamic Delivery and Exclaimer are used](https://support.microsoft.com/help/4014438/messages-with-attachments-are-not-delivered-when-atp-dynamic-delivery)</span></span>

- <span data-ttu-id="c6cc6-142">Сообщения, зашифрованные с помощью протоколов [S/MIME и Secure/многоцелевЫе расширения почты Интернета (S/MIME](s-mime-for-message-signing-and-encryption.md))</span><span class="sxs-lookup"><span data-stu-id="c6cc6-142">Messages encrypted with [Secure/Multipurpose Internet Mail Extensions (S/MIME)](s-mime-for-message-signing-and-encryption.md))</span></span>

