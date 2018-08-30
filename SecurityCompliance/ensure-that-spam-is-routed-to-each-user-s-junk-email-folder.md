---
title: Настройка гарантированной отправки нежелательной почты в соответствующую папку каждого пользователя
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/16/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0cbaccf8-4afc-47e3-a36d-a84598a55fb8
description: Для пользователей EOP нежелательная почта по умолчанию перемещается в соответствующую папку получателя. Чтобы применить это действие к локальным почтовым ящикам, необходимо настроить правила транспорта Exchange на локальных серверах (сервере-концентраторе или пограничном сервере) для обнаружения заголовков нежелательной почты, добавляемых службой EOP. Эти правила транспорта настроят вероятность нежелательной почты, используемую свойством SclJunkThreshold командлета Set-OrganizationConfig, на перемещение спама в соответствующую папку каждого почтового ящика.
ms.openlocfilehash: 1b0a9e5ee39820baade714612ca0b0bdb7a81bb9
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002858"
---
# <a name="ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a><span data-ttu-id="82883-105">Настройка гарантированной отправки нежелательной почты в соответствующую папку каждого пользователя</span><span class="sxs-lookup"><span data-stu-id="82883-105">Ensure that spam is routed to each user's Junk Email folder</span></span>

> [!IMPORTANT]
> <span data-ttu-id="82883-p102">Сведения, представленные в этом разделе, касаются только пользователей Exchange Online Protection (EOP), чьи почтовые ящики размещаются локально в гибридном развертывании. Пользователям Exchange Online, чьи почтовые ящики размещаются в Office 365, не нужно выполнять эти команды.</span><span class="sxs-lookup"><span data-stu-id="82883-p102">This topic only applies to Exchange Online Protection (EOP) customers who host mailboxes on-premises in a hybrid deployment. Exchange Online customers whose mailboxes are fully-hosted in Office 365 do not need to run these commands.</span></span> 
  
<span data-ttu-id="82883-p103">Для пользователей EOP нежелательная почта по умолчанию перемещается в соответствующую папку получателя. Чтобы применить это действие к локальным почтовым ящикам, необходимо настроить правила транспорта Exchange на локальных серверах (сервере-концентраторе или пограничном сервере) для обнаружения заголовков нежелательной почты, добавляемых службой EOP. Эти правила транспорта настроят вероятность нежелательной почты, используемую свойством SclJunkThreshold командлета Set-OrganizationConfig, на перемещение спама в соответствующую папку каждого почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="82883-p103">The default anti-spam action for EOP customers is to move spam messages to the recipients' Junk Email folder. In order for this action to work with on-premises mailboxes, you must configure Exchange Transport rules on your on-premises Edge or Hub servers to detect spam headers added by EOP. These Transport rules set the spam confidence level (SCL) used by the SclJunkThreshold property of the Set-OrganizationConfig cmdlet to move spam into the Junk Email folder of each mailbox.</span></span> 
  
### <a name="to-add-transport-rules-to-ensure-spam-is-moved-to-the-junk-email-folder-by-using-windows-powershell"></a><span data-ttu-id="82883-111">Как добавить правила транспорта для перемещения спама в папку нежелательной почты с помощью Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="82883-111">To add transport rules to ensure spam is moved to the Junk Email folder by using Windows PowerShell</span></span>

1. <span data-ttu-id="82883-p104">Откройте командную консоль Exchange для локального сервера Exchange Server. Сведения о том, как открыть командную консоль Exchange в локальной организации Exchange, см. в статье **Open the Shell**.</span><span class="sxs-lookup"><span data-stu-id="82883-p104">Access the Exchange Management Shell for your on-premises Exchange server. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**.</span></span>
    
2. <span data-ttu-id="82883-114">Выполните следующую команду, чтобы перенаправлять отфильтрованную по содержимому нежелательную почту в папку "Нежелательная почта":</span><span class="sxs-lookup"><span data-stu-id="82883-114">Run the following command to route content-filtered spam messages to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SPM" -SetSCL 6
  ```

    <span data-ttu-id="82883-115">Где  _NameForRule_  имя нового правила, например JunkContentFilteredMail.</span><span class="sxs-lookup"><span data-stu-id="82883-115">Where  _NameForRule_ is the name for the new rule, for example, JunkContentFilteredMail.</span></span> 
    
3. <span data-ttu-id="82883-116">Выполните следующую команду, чтобы перенаправлять сообщения, отмеченные как нежелательные, перед их попаданием в фильтр содержимого и папку нежелательной почты:</span><span class="sxs-lookup"><span data-stu-id="82883-116">Run the following command to route messages marked as spam prior to reaching the content filter to the Junk Email folder:</span></span>
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKS" -SetSCL 6
  ```

    <span data-ttu-id="82883-117">Где  _NameForRule_  это имя нового правила, например JunkMailBeforeReachingContentFilter.</span><span class="sxs-lookup"><span data-stu-id="82883-117">Where  _NameForRule_ is the name for the new rule, for example, JunkMailBeforeReachingContentFilter.</span></span> 
    
4. <span data-ttu-id="82883-118">Выполните следующую команду, чтобы направлять сообщения от заблокированных отправителей, например в списке **блокировок отправителя**, в папку нежелательной почты:</span><span class="sxs-lookup"><span data-stu-id="82883-118">Run the following command to ensure that messages from senders in a block list in the spam filter policy, such as the **Sender block** list, are routed to the Junk Email folder:</span></span> 
    
  ```
  New-TransportRule "NameForRule" -HeaderContainsMessageHeader "X-Forefront-Antispam-Report" -HeaderContainsWords "SFV:SKB" -SetSCL 6
  ```

    <span data-ttu-id="82883-119">Где  _NameForRule_  это имя нового правила, например JunkMailInSenderBlockList.</span><span class="sxs-lookup"><span data-stu-id="82883-119">Where  _NameForRule_ is the name for the new rule, for example, JunkMailInSenderBlockList.</span></span> 
    
<span data-ttu-id="82883-p105">Если вы не хотите использовать действие **Переместить сообщение в папку нежелательной почты**, можно выбрать другое действие с помощью политик фильтрации содержимого в Центре администрирования Exchange. Дополнительные сведения см. в статье [Настройте политики защиты от спама](configure-your-spam-filter-policies.md). Дополнительные сведения об этих полях в заголовке сообщения см. в статье [Заголовки сообщений по защите от нежелательной почты](anti-spam-message-headers.md).</span><span class="sxs-lookup"><span data-stu-id="82883-p105">If you do not want to use the **Move message to Junk Email folder** action, you can choose another action in your content filter policies in the Exchange admin center. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md). For more information about these fields in the message header, see [Anti-spam message headers](anti-spam-message-headers.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82883-123">See also</span><span class="sxs-lookup"><span data-stu-id="82883-123">See also</span></span>

[<span data-ttu-id="82883-124">Командлет New-TransportRule</span><span class="sxs-lookup"><span data-stu-id="82883-124">New-TransportRule cmdlet</span></span>](https://technet.microsoft.com/library/bb125138%28v=exchg.160%29.aspx)

