---
title: Изменение срока хранения неактивного почтового ящика в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Когда почтовый ящик Office 365 становится неактивным, вы можете изменить продолжительность удержания или политики хранения Office 365, назначенной неактивному почтовому ящику. Срок хранения определяет, как долго удерживаются элементы в папке "элементы с возможностью восстановления".
ms.openlocfilehash: f51750a0e822a4786f332639203b08ba4b5e2ba7
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295892"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="880aa-104">Изменение срока хранения неактивного почтового ящика в Office 365</span><span class="sxs-lookup"><span data-stu-id="880aa-104">Change the hold duration for an inactive mailbox in Office 365</span></span>

<span data-ttu-id="880aa-p102">Неактивный почтовый ящик используется для хранения электронной почты бывшего сотрудника после увольнения. Почтовый ящик становится неактивным, когда к нему применяется хранение для судебного разбирательства, удержание на месте, политика хранения Office 365 или удержание, связанное с делом обнаружения электронных данных, и соответствующая учетная запись пользователя Office 365 удаляется. Срок удержания определяет срок хранения элементов в папке "Элементы с возможностью восстановления". Когда он истекает, элемент окончательно удаляется из неактивного почтового ящика. После отключения почтового ящика вы можете изменить срок удержания или назначенную политику хранения Office 365.</span><span class="sxs-lookup"><span data-stu-id="880aa-p102">An inactive mailbox is used to retain a former employee's email after he or she leaves your organization. A mailbox becomes inactive when a Litigation Hold, an In-Place Hold, an Office 365 retention policy, or a hold that's associated with an eDiscovery case is placed on the mailbox, and the corresponding Office 365 user account is deleted. The contents of an inactive mailbox are retained for the duration of the hold that was placed on the mailbox before it was made inactive. The hold duration defines how long items in the Recoverable Items folder are held. When the hold duration expires for an item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. After a mailbox is made inactive, you can change the duration of the hold or Office 365 retention policy assigned to the inactive mailbox.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="880aa-p103">Мы перенесли дату, до которой можно создавать запросы на удержание на месте в Exchange Online для отключения почтового ящика, с 1 июля 2017 г. на конец этого года. Возможно, она будет перенесена в самое начало следующего года. Когда она настанет, для создания неактивного почтового ящика можно будет использовать только хранение для судебного разбирательства и политики хранения Office 365. Однако вы по-прежнему сможете управлять удержанием на месте, уже назначенным для неактивных почтовых ящиков. Это значит, что вы сможете изменять сроки такого удержания и окончательно удалять эти почтовые ящики, отменяя для них удержание на месте.</span><span class="sxs-lookup"><span data-stu-id="880aa-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds to make a mailbox inactive. But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. At that time, only Litigation Holds and Office 365 retention policies can be used to create an inactive mailbox. However, existing inactive mailboxes that are on In-Place Hold will still be supported, and you can continue to manage the In-Place Holds on inactive mailboxes. This includes changing the duration of an In-Place Hold and permanently deleting an inactive mailbox by removing the In-Place Hold.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="880aa-116">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="880aa-116">Before you begin</span></span>

- <span data-ttu-id="880aa-p104">Чтобы изменить срок хранения для судебного разбирательства для неактивного почтового ящика, необходимо использовать Exchange Online PowerShell. Вы не можете использовать центр администрирования Exchange. Но вы можете использовать Exchange Online PowerShell или центр администрирования Exchange, чтобы изменить срок хранения для хранения на месте. Вы можете изменить срок хранения для политики &amp; хранения Office 365 с помощью &amp; центра безопасности и соответствия требованиям безопасности (PowerShell) центра безопасности Office 365.</span><span class="sxs-lookup"><span data-stu-id="880aa-p104">You have to use Exchange Online PowerShell to change the hold duration for a Litigation Hold on an inactive mailbox. You can't use the Exchange admin center (EAC). But you can use Exchange Online PowerShell or the EAC to change the hold duration for an In-Place Hold. You can use the Office 365 Security &amp; Compliance Center or the Security &amp; Compliance Center PowerShell to change the hold duration for an Office 365 retention policy.</span></span>
    
- <span data-ttu-id="880aa-121">Чтобы подключиться к Exchange Online PowerShell или центру &amp; соответствия требованиям безопасности PowerShell, ознакомьтесь со следующими разделами:</span><span class="sxs-lookup"><span data-stu-id="880aa-121">To connect to Exchange Online PowerShell or Security &amp; Compliance Center PowerShell, see one of the following topics:</span></span>
    
  - [<span data-ttu-id="880aa-122">Подключение к PowerShell Exchange Online</span><span class="sxs-lookup"><span data-stu-id="880aa-122">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?linkid=396554)
    
  - [<span data-ttu-id="880aa-123">Подключение к PowerShell Центра безопасности и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="880aa-123">Connect to Office 365 Security &amp; Compliance Center PowerShell</span></span>](https://go.microsoft.com/fwlink/?linkid=799771)
    
- <span data-ttu-id="880aa-p105">Обратите внимание, что удержания, связанные с делами обнаружения электронных данных, являются бесконечными, то есть их срок изменить нельзя. Элементы хранятся бессрочно или до отмены удержания и удаления неактивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="880aa-p105">Note that holds associated with eDiscovery cases are infinite holds, which means there is no hold duration that can be changed. Items are held forever or until the hold is removed and the inactive mailbox is deleted.</span></span>
    
- <span data-ttu-id="880aa-126">Дополнительные сведения о неактивных почтовых ящиках приведены в статье неАктивные почтовые [ящики в Office 365](inactive-mailboxes-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="880aa-126">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a><span data-ttu-id="880aa-127">Этап 1. Определение инцидентов удержания для неактивного почтового ящика</span><span class="sxs-lookup"><span data-stu-id="880aa-127">Step 1: Identify the holds on an inactive mailbox</span></span>

<span data-ttu-id="880aa-128">Так как к неактивному почтовому ящику могут применяться различные удержания и политики хранения Office 365, сначала нужно определить, какие удержания применены.</span><span class="sxs-lookup"><span data-stu-id="880aa-128">Because different types of holds or one or more Office 365 retention policies might be placed on an inactive mailbox, the first step is to identify the holds on an inactive mailbox.</span></span>
  
<span data-ttu-id="880aa-129">Выполните следующую команду в PowerShell Exchange Online, чтобы отобразить сведения об удержании для всех неактивных почтовых ящиков в организации.</span><span class="sxs-lookup"><span data-stu-id="880aa-129">Run the following command in Exchange Online PowerShell to display the hold information for all inactive mailboxes in your organization.</span></span>
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
<span data-ttu-id="880aa-p106">Значение **true** для свойства **LitigationHoldEnabled** указывает на то, что неактивный почтовый ящик находится на удержании судебного разбирательства. Если для неактивного почтового ящика размещается удержание на месте, удержание eDiscovery или политика хранения Office 365, идентификатор GUID для удержания или политики хранения отображается как значение свойства **InPlaceHolds** . Например, ниже показаны результаты для 5 неактивных почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="880aa-p106">The value of **True** for the **LitigationHoldEnabled** property indicates that the inactive mailbox is on Litigation Hold. If an In-Place Hold, eDiscovery hold, or Office 365 retention policy is placed on an inactive mailbox, a GUID for the hold or retention policy is displayed as the value for the **InPlaceHolds** property. For example, the following shows results for 5 inactive mailboxes.</span></span> 
  
||
|:-----|
|
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```
   
<span data-ttu-id="880aa-133">В следующей таблице перечислены пять типов удержания, использовавшиеся для отключения каждого почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="880aa-133">The following table identifies the five different hold types that were used to make each mailbox inactive.</span></span>
  
|<span data-ttu-id="880aa-134">**Неактивный почтовый ящик**</span><span class="sxs-lookup"><span data-stu-id="880aa-134">**Inactive mailbox**</span></span>|<span data-ttu-id="880aa-135">**Тип удержания**</span><span class="sxs-lookup"><span data-stu-id="880aa-135">**Hold type**</span></span>|<span data-ttu-id="880aa-136">**Как определить удержание для неактивного почтового ящика**</span><span class="sxs-lookup"><span data-stu-id="880aa-136">**How to identify the hold on the inactive mailbox**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="880aa-137">Ann Beebe</span><span class="sxs-lookup"><span data-stu-id="880aa-137">Ann Beebe</span></span>  <br/> |<span data-ttu-id="880aa-138">Хранение для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="880aa-138">Litigation Hold</span></span>  <br/> |<span data-ttu-id="880aa-139">Свойство  *LitigationHoldEnabled*  имеет значение  `True`.</span><span class="sxs-lookup"><span data-stu-id="880aa-139">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="880aa-140">Pilar Pinilla</span><span class="sxs-lookup"><span data-stu-id="880aa-140">Pilar Pinilla</span></span>  <br/> |<span data-ttu-id="880aa-141">Удержание на месте</span><span class="sxs-lookup"><span data-stu-id="880aa-141">In-Place Hold</span></span>  <br/> |<span data-ttu-id="880aa-p107">Свойство  *InPlaceHolds*  содержит GUID удержания на месте, которое применено к неактивному почтовому ящику. Определить, что это удержание на месте, можно по тому, что идентификатор не начинается с префикса.  </span><span class="sxs-lookup"><span data-stu-id="880aa-p107">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the inactive mailbox. You can tell this is an In-Place Hold because the ID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="880aa-144">Вы можете использовать `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` команду в Exchange Online PowerShell, чтобы получить сведения об удержанИи на месте для неактивного почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="880aa-144">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the inactive mailbox.</span></span>  <br/> |
|<span data-ttu-id="880aa-145">Mario Necaise</span><span class="sxs-lookup"><span data-stu-id="880aa-145">Mario Necaise</span></span>  <br/> |<span data-ttu-id="880aa-146">Политика хранения Office 365 на уровне всей Организации в центре &amp; безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="880aa-146">Organization-wide Office 365 retention policy in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="880aa-p108">Свойство *InPlaceHolds* пусто. Это означает, что к неактивному почтовому ящику применяется одна или несколько политик хранения Office 365 (на уровне всей организации или Exchange). В этом случае можно выполнить `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` команду в Exchange Online PowerShell, чтобы получить список идентификаторов GUID для политик хранения Office 365 на уровне Организации. GUID для политик хранения на уровне Организации, применяемых к почтовым ящикам Exchange, начинаются `mbx` с префикса; например `mbxa3056bb15562480fadb46ce523ff7b02`:.</span><span class="sxs-lookup"><span data-stu-id="880aa-p108">The  *InPlaceHolds*  property is empty. This indicates that one or more organization-wide or (Exchange-wide) Office 365 retention policy is applied to the inactive mailbox. In this case, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies that are applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  </span></span><br/> <br/><span data-ttu-id="880aa-151">Чтобы определить политику хранения Office 365, которая применяется к неактивному почтовому ящику, выполните следующую команду &amp; в PowerShell центра соответствия требованиям безопасности.</span><span class="sxs-lookup"><span data-stu-id="880aa-151">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span>  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>
|<span data-ttu-id="880aa-152">Carol Olson</span><span class="sxs-lookup"><span data-stu-id="880aa-152">Carol Olson</span></span>  <br/> |<span data-ttu-id="880aa-153">Политика хранения Office 365 в центре соответствия &amp; требованиям безопасности, применяемая к определенным почтовым ящикам</span><span class="sxs-lookup"><span data-stu-id="880aa-153">Office 365 retention policy in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> |<span data-ttu-id="880aa-p109">Свойство  *InPlaceHolds*  содержит GUID политики хранения Office 365, которая применена к неактивному почтовому ящику. То, что политика хранения применяется к определенному почтовому ящику, можно определить по префиксу GUID  `mbx`. Обратите внимание, что если GUID начинается с префикса  `skp`, это означает, что политика хранения применяется к беседам Skype для бизнеса.  </span><span class="sxs-lookup"><span data-stu-id="880aa-p109">The  *InPlaceHolds*  property contains the GUID of the Office 365 retention policy that's applied to the inactive mailbox. You can tell this is a retention policy that applied to specific mailboxes because the GUID starts with the  `mbx` prefix. Note that if GUID of the retention policy applied to the inactive mailbox started with the  `skp` prefix, that would indicate that the retention policy is applied to Skype for Business conversations.  </span></span><br/><br/> <span data-ttu-id="880aa-157">Чтобы определить политику хранения Office 365, которая применяется к неактивному почтовому ящику, выполните следующую команду &amp; в PowerShell центра соответствия требованиям безопасности.</span><span class="sxs-lookup"><span data-stu-id="880aa-157">To identity the Office 365 retention policy that's applied to the inactive mailbox, run the following command in Security &amp; Compliance Center PowerShell.</span></span><br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name` <br/><br/><span data-ttu-id="880aa-158">При выполнении этой команды обязательно `mbx` удалите `skp` префикс или префикс.</span><span class="sxs-lookup"><span data-stu-id="880aa-158">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="880aa-159">Abraham McMahon</span><span class="sxs-lookup"><span data-stu-id="880aa-159">Abraham McMahon</span></span>  <br/> |<span data-ttu-id="880aa-160">удержание дел eDiscovery в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="880aa-160">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="880aa-p110">Свойство  *InPlaceHolds*  содержит GUID удержания по делу обнаружения электронных данных, которое применено к неактивному почтовому ящику. То, что это удержание по делу обнаружения электронных данных, можно понять по префиксу GUID  `UniH`.  </span><span class="sxs-lookup"><span data-stu-id="880aa-p110">The  *InPlaceHolds*  property contains the GUID of the eDiscovery case hold that's placed on the inactive mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="880aa-p111">Вы можете использовать `Get-CaseHoldPolicy` командлет в PowerShell центра &amp; соответствия требованиям безопасности, чтобы получить сведения о том случае обнаружения электронных данных, с которым связано удержание на неактивном почтовом ящике. Например, вы можете выполнить команду `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` , чтобы отобразить имя удержания для случая, которое находится в неактивном почтовом ящике. При выполнении этой команды обязательно `UniH` удалите префикс.</span><span class="sxs-lookup"><span data-stu-id="880aa-p111">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the inactive mailbox is associated with. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the inactive mailbox. Be sure to remove the  `UniH` prefix when you run this command.  </span></span><br/><br/> <span data-ttu-id="880aa-166">Чтобы определить дело обнаружения электронных данных, с которым связано удержание для неактивного почтового ящика, выполните следующие команды.</span><span class="sxs-lookup"><span data-stu-id="880aa-166">To identity the eDiscovery case that the hold on the inactive mailbox is associated with, run the following commands.</span></span>  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId | FL Name`<br/><br/><br/> <span data-ttu-id="880aa-p112">**Примечание:** Мы не рекомендуем использовать удержания электронных данных для неактивных почтовых ящиков. Это обусловлено тем, что варианты обнаружения электронных данных предназначены для определенных и ограниченных временных случаев, связанных с юридическим вопросом. В какой-то момент юридический случай, скорее всего, будет удален, и удержания, связанные с этим обращением, будут удалены, а ситуация обнаружения электронных данных будет закрыта (или удалена). На самом деле, если удержание, размещенное на неактивном почтовом ящике, связано с вариантом обнаружения электронных данных, а удержание отключено или закрыто или удалено, неактивный почтовый ящик будет безвозвратно удален.</span><span class="sxs-lookup"><span data-stu-id="880aa-p112">**Note:** We don't recommend using eDiscovery holds for inactive mailboxes. That's because eDiscovery cases are intended for specific, time-bound cases related to a legal issue. At some point, a legal case will probably end and the holds associated with the case will be removed and the eDiscovery case will be closed (or deleted). In fact, if a hold that's placed on an inactive mailbox is associated with an eDiscovery case, and the hold is released or the eDiscovery case is closed or deleted, the inactive mailbox will be permanently deleted.</span></span> 

<span data-ttu-id="880aa-171">Для получения дополнительных сведений о политиках хранения Office 365, ознакомьтесь со статьей [Обзор политик хранения](retention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="880aa-171">For more information about Office 365 retention policies, see [Overview of retention policies](retention-policies.md).</span></span>
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a><span data-ttu-id="880aa-172">Этап 2. Изменение срока удержания неактивного почтового ящика</span><span class="sxs-lookup"><span data-stu-id="880aa-172">Step 2: Change the hold duration for an inactive mailbox</span></span>

<span data-ttu-id="880aa-173">После определения типа удержания и количества инцидентов удержания для неактивного почтового ящика следующий шаг  изменение срока удержания.</span><span class="sxs-lookup"><span data-stu-id="880aa-173">After you identify what type of hold is placed on the inactive mailbox (and whether there are multiple holds), the next step is to change the duration for the hold.</span></span> 
  
### <a name="change-the-duration-for-a-litigation-hold"></a><span data-ttu-id="880aa-174">Изменение срока хранения для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="880aa-174">Change the duration for a Litigation Hold</span></span>

<span data-ttu-id="880aa-p113">Ниже описано, как изменить срок хранения неактивного почтового ящика для судебного разбирательства с помощью Exchange Online PowerShell. Использовать Центр администрирования Exchange нельзя. Чтобы изменить срок хранения, выполните указанную ниже команду. В этом примере срок хранения изменяется на неограниченный период времени.</span><span class="sxs-lookup"><span data-stu-id="880aa-p113">Here's how to use Exchange Online PowerShell to change the hold duration for a Litigation Hold that is placed on an inactive mailbox. You can't use the EAC. Run the following command to change the hold duration. In this example, the hold duration is changed to an unlimited period of time.</span></span>
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

<span data-ttu-id="880aa-179">В результате элементы в неактивном почтовом ящике хранятся бессрочно (до снятия удержания или изменения срока хранения).</span><span class="sxs-lookup"><span data-stu-id="880aa-179">The result is that items in the inactive mailbox are retained indefinitely or until the hold is removed or the hold duration is changed to a different value.</span></span>
  
> [!TIP]
> <span data-ttu-id="880aa-p114">Лучший способ идентификации неактивного почтового ящика  использовать его **Distinguished Name** или **Exchange GUID**. Используя одно из этих значений, вы не укажете по ошибке неверный почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="880aa-p114">The best way to identify an inactive mailbox is by using its **Distinguished Name** or **Exchange GUID** value. Using one of these values helps prevent accidentally specifying the wrong mailbox.</span></span> 
  
### <a name="change-the-duration-for-an-in-place-hold"></a><span data-ttu-id="880aa-182">Изменение срока хранения на месте</span><span class="sxs-lookup"><span data-stu-id="880aa-182">Change the duration for an In-Place Hold</span></span>

 <span data-ttu-id="880aa-183">Для изменения срока удержания на месте можно использовать Центр администрирования Exchange или Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="880aa-183">You can use the EAC or Exchange Online PowerShell to change the hold duration for an In-Place Hold.</span></span> 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a><span data-ttu-id="880aa-184">Изменение срока хранения на месте с помощью EAC</span><span class="sxs-lookup"><span data-stu-id="880aa-184">Use the EAC to change the hold duration</span></span>

1. <span data-ttu-id="880aa-p115">Если вы знаете имя хранения на месте, которое нужно изменить, перейдите к следующему шагу. В противном случае выполните следующую команду, чтобы получить имя удержания на месте для неактивного почтового ящика. Используйте идентификатор GUID хранения на месте, полученный на [шаге 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="880aa-p115">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="880aa-188">В центре администрирования Exchange перейдите к разделу **Управление** \> соответствием при обнаружении \*\* &amp; электронных данных на месте\*\*.</span><span class="sxs-lookup"><span data-stu-id="880aa-188">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
3. <span data-ttu-id="880aa-189">Выберите удержание на месте, которое нужно изменить, а затем щелкните **изменить** ![значок](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)редактирования.</span><span class="sxs-lookup"><span data-stu-id="880aa-189">Select the In-Place Hold you want to change, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
4. <span data-ttu-id="880aa-190">На странице свойств **хранения для обнаружения &amp; электронных** данных на месте нажмите кнопку **удержание на месте**.</span><span class="sxs-lookup"><span data-stu-id="880aa-190">On the **In-Place eDiscovery &amp; Hold** properties page, click **In-Place Hold**.</span></span> 
    
5. <span data-ttu-id="880aa-191">Выполните одно из следующих действий в зависимости от текущего срока хранения.</span><span class="sxs-lookup"><span data-stu-id="880aa-191">Do one of the following based on the current hold duration:</span></span>
    
1. <span data-ttu-id="880aa-192">Установите флажок **Хранить неопределенное время**, чтобы хранить элементы в течение неограниченного времени.</span><span class="sxs-lookup"><span data-stu-id="880aa-192">Click **Hold indefinitely** to hold items for an unlimited period of time.</span></span> 
    
2. <span data-ttu-id="880aa-p116">Щелкните **указать количество дней, в течение которых элементы хранятся относительно даты получения** для хранения элементов за определенный период. Введите количество дней, в течение которых следует хранить элементы.</span><span class="sxs-lookup"><span data-stu-id="880aa-p116">Click **Specify number of days to hold items relative to their received date** to hold items for a specific period. Type the number of days that you want to hold items for.</span></span> 
    
    ![Снимок экрана: изменение длительности параметра хранения на месте.](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. <span data-ttu-id="880aa-196">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="880aa-196">Click **Save**.</span></span>
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a><span data-ttu-id="880aa-197">Изменение срока хранения в PowerShell Exchange Online</span><span class="sxs-lookup"><span data-stu-id="880aa-197">Use Exchange Online PowerShell to change the hold duration</span></span>

1. <span data-ttu-id="880aa-p117">Если вы знаете имя хранения на месте, которое нужно изменить, перейдите к следующему шагу. В противном случае выполните следующую команду, чтобы получить имя удержания на месте для неактивного почтового ящика. Используйте идентификатор GUID хранения на месте, полученный на [шаге 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span><span class="sxs-lookup"><span data-stu-id="880aa-p117">If you know the name of the In-Place Hold that you want to change, go to the next step. Otherwise, run the following command to get the name of the In-Place Hold that is placed on the inactive mailbox. Use the In-Place Hold GUID that you obtained in [Step 1](#step-1-identify-the-holds-on-an-inactive-mailbox).</span></span>

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. <span data-ttu-id="880aa-p118">Чтобы изменить срок хранения, выполните следующую команду. В этом примере срок хранения изменяется на 2555 дней (приблизительно 7 лет).</span><span class="sxs-lookup"><span data-stu-id="880aa-p118">Run the following command to change the hold duration. In this example, the hold duration is changed to 2,555 days (approximately 7 years).</span></span> 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     <span data-ttu-id="880aa-203">Чтобы изменить срок хранения на неограниченный период, используйте параметр  _-ItemHoldPeriod unlimited_.</span><span class="sxs-lookup"><span data-stu-id="880aa-203">To change the hold duration to an unlimited period of time, use  _-ItemHoldPeriod unlimited_.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="880aa-204">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="880aa-204">More information</span></span>

- <span data-ttu-id="880aa-p119">**Как рассчитывается срок хранения для элемента в неактивном почтовом ящике?** Отсчет срока хранения начинается с исходной даты получения или создания элемента почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="880aa-p119">**How is the hold duration calculated for an item in an inactive mailbox?** The duration is calculated from the original date a mailbox item was received or created.</span></span> 
    
- <span data-ttu-id="880aa-p120">**Что происходит по истечении срока удержания?** По истечении срока хранения элемента в папке "Элементы с возможностью восстановления" он будет окончательно удален из неактивного почтового ящика. Если срок для удержания неактивного почтового ящика не указан, элементы в папке "Элементы с возможность восстановления" никогда не удаляются (если срок удержания не изменяется).</span><span class="sxs-lookup"><span data-stu-id="880aa-p120">**What happens when the hold duration expires?** When the hold duration expires for a mailbox item in the Recoverable Items folder, the item is permanently deleted (purged) from the inactive mailbox. If there is no duration specified for the hold placed on the inactive mailbox, items in the Recoverable Items folder are never purged (unless the hold duration for the inactive mailbox is changed).</span></span> 
    
- <span data-ttu-id="880aa-p121">**Политика хранения Exchange для неактивных почтовых ящиков по-прежнему обрабатывается?** Если политика хранения Exchange (функция управления записями сообщений в Exchange Online) была применена к почтовому ящику, когда он стал неактивным, для него по-прежнему будут обрабатываться политики удаления (теги хранения, настроенные с действием хранения **Delete** ). Это означает, что после истечения срока хранения элементы, отмеченные политикой удаления, перемещаются в папку "Элементы с возможностью восстановления". Затем они удаляются из неактивного почтового ящика после истечения срока удержания.</span><span class="sxs-lookup"><span data-stu-id="880aa-p121">**Is an Exchange retention policy still processed on inactive mailboxes?** If an Exchange retention policy (the messaging records management, or MRM, feature in Exchange Online) was applied to a mailbox when it was made inactive, the deletion policies (which are retention tags configured with a **Delete** retention action) will continue to be processed on the inactive mailbox. That means items that are tagged with a deletion policy are moved to the Recoverable Items folder when the retention period expires. Those items are then purged from the inactive mailbox when the hold duration for an item expires.</span></span> 
    
    <span data-ttu-id="880aa-p122">И наоборот, любые политики архивации (теги хранения, настроенные с действием хранения **MoveToArchive** ), включенные в политику хранения для почтового ящика, игнорируются. Это означает, что после истечения срока хранения элементы в неактивном почтовом ящике, помеченные политикой архивации, остаются в основном почтовом ящике. Они не перемещаются в архивный почтовый ящик или в папку "Элементы с возможностью восстановления" в архивном почтовом ящике. Так как пользователь не может войти в неактивный почтовый ящик, не имеет смысла использовать ресурсы центра обработки данных для обработки политик архивации.</span><span class="sxs-lookup"><span data-stu-id="880aa-p122">Conversely, any archive policies (which are retention tags configured with a **MoveToArchive** retention action) that are included in the retention policy assigned to an inactive mailbox are ignored. That means items in an inactive mailbox that are tagged with an archive policy remain in the primary mailbox when the retention period expires. They're not moved to the archive mailbox or to the Recoverable Items folder in the archive mailbox. Because a user can't sign in to an inactive mailbox, there's no reason to consume datacenter resources to process archive policies.</span></span> 
    
- <span data-ttu-id="880aa-p123">**Чтобы проверить новый срок удержания, выполните одну из приведенных ниже команд.** Первая команда предназначена для хранения для судебного разбирательства, а вторая  для хранения на месте.</span><span class="sxs-lookup"><span data-stu-id="880aa-p123">**To check the new hold duration, run one of the following commands.** The first command is for Litigation Hold; the second is for In-Place Hold.</span></span> 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- <span data-ttu-id="880aa-p124">**Помощник по обслуживанию управляемых папок (MFA) также обрабатывает неактивные почтовые ящики, как и обычные почтовые ящики.** В Exchange Online MFA обрабатывает почтовые ящики приблизительно каждые 7 дней. После изменения срока удержания для неактивного почтового ящика вы можете использовать командлет **Start-ManagedFolderAssistant** для немедленного запуска обработки нового срока удержания неактивного почтового ящика. Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="880aa-p124">**Like regular mailboxes, the Managed Folder Assistant (MFA) also processes inactive mailboxes.** In Exchange Online, the MFA processes mailboxes approximately once every 7 days. After you change the hold duration for an inactive mailbox, you can use the **Start-ManagedFolderAssistant** cmdlet to immediately start processing the new hold duration for the inactive mailbox. Run the following command.</span></span> 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- <span data-ttu-id="880aa-p125">**Если к неактивному почтовому ящику применено большое количество удержаний, будут отображены не все GUID.** Чтобы просмотреть GUID всех удержаний (кроме хранения для судебного разбирательства), выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="880aa-p125">**If a lot of holds are placed on an inactive mailbox, not all of the hold GUIDs will be displayed.** You can run the following command to display the GUIDs for all holds (except Litigation Holds) that are placed on an inactive mailbox.</span></span> 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
