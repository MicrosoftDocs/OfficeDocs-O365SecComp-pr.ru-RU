---
title: Использование уведомлений пользователей о спаме для освобождения сообщений из карантина и создания отчетов о них в Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
description: Если ваш администратор включает уведомления для пользователей, вы получите сообщение уведомления, в котором приведены сообщений, отправленных в ваш почтовый ящик, которые были помечаются как нежелательная почта, массовое или фишинга. Можно освободить или отправка отчетов о сообщениях после получения уведомления.
ms.openlocfilehash: e355a94af5ac295503a8e205b1a896afc1c54fb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534593"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="f3af5-104">Использование уведомлений пользователей о спаме для освобождения сообщений из карантина и создания отчетов о них в Office 365</span><span class="sxs-lookup"><span data-stu-id="f3af5-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="f3af5-105">Если ваш администратор включает уведомлений о нежелательной почте для пользователей, вы получите сообщение уведомления, в котором приведены сообщения, адресованные ваш почтовый ящик, который были помечаются как нежелательная почта и вместо этого на карантин.</span><span class="sxs-lookup"><span data-stu-id="f3af5-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="f3af5-106">Если вы администратор и необходимо включить эту функцию, можно выбрать вариант при [Изменение политики защиты от нежелательной почты по умолчанию](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="f3af5-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="f3af5-p102">Сообщение, которое появляется в списке включает число сообщения, помещенные на карантин, которые у вас есть и дату и время (в универсальное время в формате UTC) последнего сообщения. Список содержит следующие параметры для каждого сообщения:</span><span class="sxs-lookup"><span data-stu-id="f3af5-p102">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list. The list includes the following for each message:</span></span>
  
- <span data-ttu-id="f3af5-109">**Отправитель** Отправить имя и адрес электронной почты помещенного в карантин сообщения.</span><span class="sxs-lookup"><span data-stu-id="f3af5-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="f3af5-110">**Тема.** Текст в строке темы помещенного в карантин сообщения.</span><span class="sxs-lookup"><span data-stu-id="f3af5-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="f3af5-111">**Дата.** Дата и время (в формате UTC) помещения сообщения в карантин.</span><span class="sxs-lookup"><span data-stu-id="f3af5-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="f3af5-112">**Размер** Размер сообщения в килобайтах (КБ).</span><span class="sxs-lookup"><span data-stu-id="f3af5-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="f3af5-113">На данный момент существует два действия, которые можно выполнить с помещенного на карантин сообщения.</span><span class="sxs-lookup"><span data-stu-id="f3af5-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="f3af5-114">**Выпуск для папки "Входящие"** Нажмите кнопку, чтобы отправить сообщение в папку "Входящие", где вы можете просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="f3af5-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="f3af5-p103">**Отчет о как не являющееся нежелательным** Выберите этот вариант отправить копию сообщения в корпорацию Майкрософт для анализа. Группа нежелательной почты оценивает анализирует сообщение и, в зависимости от результаты анализа изменяет правил фильтрации нежелательной почты для отправки сообщения через.</span><span class="sxs-lookup"><span data-stu-id="f3af5-p103">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis. The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="f3af5-117">Необходимо учитывать следующее:</span><span class="sxs-lookup"><span data-stu-id="f3af5-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="f3af5-p104">Сообщений, помещенных на карантин, так как они соответствия правилу поток почты не включаются в сообщениях, помещенных в карантин пользователя. Отображаются только сообщения, помещенные на карантин.</span><span class="sxs-lookup"><span data-stu-id="f3af5-p104">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages. Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="f3af5-120">Освободить сообщение и сообщить о ложном срабатывании (о том, что сообщение не является нежелательным) можно только один раз.</span><span class="sxs-lookup"><span data-stu-id="f3af5-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

