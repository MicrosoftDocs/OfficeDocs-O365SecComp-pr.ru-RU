---
title: Использование уведомлений пользователей о спаме для освобождения сообщений из карантина и создания отчетов о них в Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
ms.collection:
- M365-security-compliance
description: Если администратор включает уведомления для пользователей, вы получите сообщение с уведомлением о том, что сообщения, отправленные в ваш почтовый ящик, были идентифицированы как спам, массовые или фишинговые сообщения. Вы можете отпустить или отправить отчет о сообщениях после получения уведомления.
ms.openlocfilehash: 7f68b70298fca7d8ed5f5e5b8dc9c727c3a6a6c1
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492728"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="726ea-104">Использование уведомлений пользователей о спаме для освобождения сообщений из карантина и создания отчетов о них в Office 365</span><span class="sxs-lookup"><span data-stu-id="726ea-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="726ea-105">Если администратор включает уведомления о нежелательной почте для пользователей, вы получите сообщение с уведомлением, в котором перечисляются сообщения, адресованные почтовому ящику, которые были идентифицированы как спам и помещены в карантин.</span><span class="sxs-lookup"><span data-stu-id="726ea-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="726ea-106">Если вы являетесь администратором и хотите включить эту функцию, вы можете выбрать параметр при [изменении политики защиты от нежелательной почты по умолчанию](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="726ea-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="726ea-107">Полученное сообщение включает в себя количество сообщений, помещенных в карантин нежелательной почты, а также дату и время (в формате UTC) последнего сообщения в списке.</span><span class="sxs-lookup"><span data-stu-id="726ea-107">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list.</span></span> <span data-ttu-id="726ea-108">Список содержит следующие сведения для каждого сообщения:</span><span class="sxs-lookup"><span data-stu-id="726ea-108">The list includes the following for each message:</span></span>
  
- <span data-ttu-id="726ea-109">**Sender** (отправитель) Имя отправителя и адрес электронной почты почтового сообщения, помещенного в карантин.</span><span class="sxs-lookup"><span data-stu-id="726ea-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="726ea-110">**Тема.** Текст в строке темы помещенного в карантин сообщения.</span><span class="sxs-lookup"><span data-stu-id="726ea-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="726ea-111">**Дата.** Дата и время (в формате UTC) помещения сообщения в карантин.</span><span class="sxs-lookup"><span data-stu-id="726ea-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="726ea-112">**Size (размер** ) Размер сообщения в килобайтах (КБ).</span><span class="sxs-lookup"><span data-stu-id="726ea-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="726ea-113">В настоящее время существует два действия, которые можно выполнить с сообщением в карантине:</span><span class="sxs-lookup"><span data-stu-id="726ea-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="726ea-114">**Отпустить до папки "Входящие"** Выберите этот параметр, чтобы отправить сообщение в папку "Входящие", где его можно просмотреть.</span><span class="sxs-lookup"><span data-stu-id="726ea-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="726ea-115">**Отчет не является** нежелательным Нажмите эту кнопку, чтобы отправить копию сообщения в корпорацию Майкрософт для анализа.</span><span class="sxs-lookup"><span data-stu-id="726ea-115">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis.</span></span> <span data-ttu-id="726ea-116">Отдел анализа нежелательной почты оценивает и анализирует сообщение и в зависимости от результатов анализа настраивает правила фильтрации нежелательной почты, чтобы разрешить доставку сообщения.</span><span class="sxs-lookup"><span data-stu-id="726ea-116">The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="726ea-117">Необходимо учитывать следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="726ea-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="726ea-118">Сообщения, помещенные в карантин, так как они отвечают правилу обработки почты, не включаются в сообщения, помещенные в карантин пользователя.</span><span class="sxs-lookup"><span data-stu-id="726ea-118">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages.</span></span> <span data-ttu-id="726ea-119">В список включаются только помещенные в карантин нежелательные сообщения.</span><span class="sxs-lookup"><span data-stu-id="726ea-119">Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="726ea-120">Освободить сообщение и сообщить о ложном срабатывании (о том, что сообщение не является нежелательным) можно только один раз.</span><span class="sxs-lookup"><span data-stu-id="726ea-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

