---
title: Вопросы и ответы, посвященные карантину
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
description: В этой статье приведены часто задаваемые вопросы о размещенном карантине.
ms.openlocfilehash: cc8a05b575e17dbc71d4b9e214cb29a4cafe8b6b
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003198"
---
# <a name="quarantine-faq"></a><span data-ttu-id="8aa1f-103">Вопросы и ответы, посвященные карантину</span><span class="sxs-lookup"><span data-stu-id="8aa1f-103">Quarantine FAQ</span></span>

<span data-ttu-id="8aa1f-p101">В этой статье приведены часто задаваемые вопросы о размещенном карантине. Ответы предназначены для клиентов Microsoft Exchange Online и Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p101">This topic provides frequently asked questions and answers about the hosted quarantine. Answers are applicable for Microsoft Exchange Online and Exchange Online Protection customers.</span></span>
  
 <span data-ttu-id="8aa1f-106">**В. как управлять вредоносных программ на карантин сообщения в карантин?**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-106">**Q. How do I manage malware-quarantined messages in quarantine?**</span></span>
  
<span data-ttu-id="8aa1f-p102">Необходимо использовать безопасности &amp; центре соответствия требованиям для просмотра и работы с сообщениями, которые были отправлены на карантин, так как они содержат вредоносных программ. Дополнительные сведения см в [карантин сообщения электронной почты в Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p102">You need to use the Security &amp; Compliance Center in order to view and work with messages that were sent to quarantine because they contain malware. For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span></span>
  
 <span data-ttu-id="8aa1f-109">**В. Как настроить службу для отправки нежелательных сообщений на карантин?**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-109">**Q. How do I configure the service to send spam-quarantined messages to the quarantine?**</span></span>
  
<span data-ttu-id="8aa1f-p103">О. По умолчанию сообщения с фильтрованным содержимым отправляются в папку нежелательной почты получателя. Однако администраторы могут настроить политики фильтрации содержимого для помещения таких сообщений на карантин. Дополнительные сведения о различных действиях, которые можно применять к сообщениям с фильтрацией содержимого, см. в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p103">A. By default, content-filtered messages are sent to the recipients Junk Email folder. However, admins can configure content filter policies to send spam-quarantined messages to the quarantine instead. For more information about the different actions that can be performed on content-filtered messages, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="8aa1f-114">**В. Имеется ли в службе возможность управления сообщениями, помещенными в карантин нежелательной почты, для администратора и конечных пользователей?**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-114">**Q. Does the service have administrator and end user management of spam-quarantined messages?**</span></span>
  
<span data-ttu-id="8aa1f-p104">О. Администратор может выполнять поиск и просматривать подробные сведения о сообщениях электронной почты, помещенных на карантин, в Центре администрирования Exchange. Найдя нужное сообщение, можно разблокировать его для определенных пользователей и даже пометить его как "жертву" ложного срабатывания и отправить группе анализа нежелательной почты Майкрософт. Дополнительные сведения см. в разделе [Поиск и освобождение сообщений на карантине для администратора](find-and-release-quarantined-messages-as-an-administrator.md).</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p104">A. As an administrator, you can search for and view details about all quarantined email messages in the Exchange admin center (EAC). After locating the message, you can release it to specific users and optionally report it as a false positive (not junk) to the Microsoft Spam Analysis Team. For more information, see [Find and release quarantined messages as an administrator](find-and-release-quarantined-messages-as-an-administrator.md).</span></span>
  
<span data-ttu-id="8aa1f-119">Конечный пользователь может управлять своими сообщениями, помещенными в карантин нежелательной почты, используя следующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-119">As an end user, you can manage your own spam-quarantined messages via:</span></span> 
  
- <span data-ttu-id="8aa1f-p105">Пользовательский интерфейс карантина нежелательной почты. Дополнительные сведения см. в разделе [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p105">The spam quarantine user interface. For more information, see [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).</span></span>
        
 <span data-ttu-id="8aa1f-122">**В. Как предоставить доступ к карантину нежелательной почты для конечных пользователей?**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-122">**Q. How do I grant access to the spam quarantine for my end users?**</span></span>
  
<span data-ttu-id="8aa1f-p106">А. Чтобы получить доступ к карантину нежелательной почты, конечные пользователи должны иметь допустимый идентификатор пользователя Office 365 и пароль. Клиенты EOP защита локальных почтовых ящиков должен быть допустимый адрес электронной почты пользователей, созданных с помощью синхронизации службы каталогов или центра администрирования Exchange. Дополнительные сведения об управлении пользователями администраторам EOP можно обратиться к [Управление почтовыми пользователями в EOP](eop/manage-mail-users-in-eop.md). Для клиентов автономной EOP мы рекомендуем с помощью синхронизации службы каталогов, а также включение Directory пограничной блокировки на основе; Для получения дополнительных сведений см [Использования Directory Based Edge Blocking to Reject Messages Sent to недопустимых получателей](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p106">A. In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password. EOP customers protecting on-premises mailboxes must be valid email users created via directory synchronization or the EAC. For more information about managing users, EOP admins can refer to [Manage mail users in EOP](eop/manage-mail-users-in-eop.md). For EOP standalone customers, we recommend using directory synchronization and enabling Directory Based Edge Blocking; for more information, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span>
  
 <span data-ttu-id="8aa1f-128">**В. Можно ли отправить на карантин не только нежелательные сообщения?**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-128">**Q. Can anything other than spam be sent to the quarantine?**</span></span>
  
<span data-ttu-id="8aa1f-p107">О. Сообщения, соответствующие правилу транспорта, также можно отправить на карантин администратора, если это действие настроено. Карантин конечного пользователя предназначен только для нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p107">A. Messages that match a transport rule can also be sent to the administrator quarantine, if that's the configured action. The end user quarantine is for spam only.</span></span>
  
 <span data-ttu-id="8aa1f-132">**В. Как долго сообщения хранятся в карантине?**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-132">**Q. For how long are messages kept in the quarantine?**</span></span>
  
<span data-ttu-id="8aa1f-p108">О. По умолчанию сообщения в карантине нежелательной почте хранятся 15 дней, а сообщения в карантине, соответствующие правилу транспорта, хранятся в карантине 7 дней. После этого сообщения удаляются без возможности восстановления. Период хранения сообщений в карантине, соответствующих правилу транспорта, не изменяется. Однако период хранения сообщений в карантине нежелательной почты можно сократить с помощью параметра **Сохранять нежелательную почту в течение (дней)** в политиках фильтрации содержимого. Дополнительные сведения см. в разделе [Настройте политики защиты от спама](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p108">A. By default, spam-quarantined messages are kept in the quarantine for 15 days, while quarantined messages that matched a transport rule are kept in the quarantine for 7 days. After this period of time the messages are deleted and are not retrievable. The retention period for quarantined messages that matched a transport rule is not configurable. However, the retention period for spam-quarantined messages can be lowered via the **Retain spam for (days)** setting in your content filter policies. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="8aa1f-139">**В. Можно ли освободить одновременно несколько сообщений, помещенных на карантин, или сообщить о них?**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-139">**Q. Can I release or report more than one quarantined message at a time?**</span></span>
  
<span data-ttu-id="8aa1f-p109">О. Возможность одновременного освобождения нескольких сообщений или передачи отчета о них в текущий момент недоступна в Центре администрирования Exchange или карантине нежелательной почты пользователя. Однако администраторы могут скрипт удаленного модуля Windows PowerShell для выполнения этой задачи. Используйте командлет [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) для поиска сообщений и командлет [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) для их освобождения.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p109">A. The ability to release or report multiple messages at once is not currently available in the EAC or the end user spam quarantine. However, admins can create a remote Windows PowerShell script to accomplish this task. Use the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for messages, and the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet to release them.</span></span> 
  
 <span data-ttu-id="8aa1f-144">**В. Поддерживаются ли подстановочные знаки при поиске сообщений, помещенных на карантин? Можно ли искать помещенные на карантин сообщения для определенного домена?**</span><span class="sxs-lookup"><span data-stu-id="8aa1f-144">**Q. Are wildcards supported when searching for quarantined messages? Can I search for quarantined messages for a specific domain?**</span></span>
  
<span data-ttu-id="8aa1f-p110">О. Подстановочные знаки не поддерживаются при указании условий поиска в Центре администрирования Exchange. Например, при поиске отправителя необходимо указать полны адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p110">A. Wildcards are not supported when specifying search criteria in the Exchange admin center. For example, when searching for a sender, you must specify the full email address.</span></span>
  
<span data-ttu-id="8aa1f-148">С помощью удаленного модуля Windows PowerShell можно выполнить командлет [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx), чтобы найти в карантине сообщения для определенного домена (например, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="8aa1f-148">Using remote Windows PowerShell, admins can specify the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for quarantined messages for a specific domain (for example, contoso.com):</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

<span data-ttu-id="8aa1f-p111">Результаты можно передать командлету [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx). Укажите параметр -ReleaseToAll, чтобы освободить сообщение для всех получателей. После освобождения сообщения снова освободить его нельзя.</span><span class="sxs-lookup"><span data-stu-id="8aa1f-p111">The results can be passed to the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet. Include the -ReleaseToAll parameter to release the message to all recipients. Once a message is released, it can't be released again.</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```


