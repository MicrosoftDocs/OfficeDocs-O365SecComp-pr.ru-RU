---
title: Настройка уведомлений об исходящей нежелательной почте в Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: Администраторы могут узнать, как изменить параметры уведомлений для обнаружений исходящих нежелательной почты в Office 365.
ms.openlocfilehash: c48b6cd634417a00040fb5479313782b44f6aa8d
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822519"
---
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a><span data-ttu-id="44c3e-103">Настройка уведомлений об исходящей нежелательной почте в Office 365</span><span class="sxs-lookup"><span data-stu-id="44c3e-103">Configure outbound spam policy notifications in Office 365</span></span>

<span data-ttu-id="44c3e-104">Фильтрация исходящей нежелательной почты всегда включена, если эта служба используется для отправки исходящей почты, тем самым помогая защищать организации, использующие эту службу, и их получателей.</span><span class="sxs-lookup"><span data-stu-id="44c3e-104">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients.</span></span> <span data-ttu-id="44c3e-105">Как и в случае входящих сообщений, процесс фильтрации исходящих сообщений состоит из фильтрации подключений и фильтрации содержимого, однако настройки исходящей фильтрации не настраиваются.</span><span class="sxs-lookup"><span data-stu-id="44c3e-105">Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable.</span></span> <span data-ttu-id="44c3e-106">Если исходящее сообщение определено как нежелательное, оно маршрутизируется через пул доставки более высокого риска, что снижает вероятность добавления в список блокировок обычного пула исходящих IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="44c3e-106">If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list.</span></span> <span data-ttu-id="44c3e-107">Если клиент продолжит отправлять через службу нежелательную почту, отправка сообщений для него будет заблокирована.</span><span class="sxs-lookup"><span data-stu-id="44c3e-107">If a customer continues to send outbound spam through the service, they will be blocked from sending messages.</span></span>

<span data-ttu-id="44c3e-108">Несмотря на то, что отключить или изменить фильтрацию нежелательной почты невозможно, можно настроить следующие параметры уведомлений об исходящей нежелательной почте:</span><span class="sxs-lookup"><span data-stu-id="44c3e-108">Although you can't disable or change outbound spam filtering, you can configure the following outbound spam notification settings:</span></span>

- <span data-ttu-id="44c3e-109">**Отправлять копии подозрительных сообщений**: эти сообщения помечаются как спам (независимо от оценки вероятности нежелательной почты) и не отклоняются фильтром, но направляются через пул доставки с более высоким уровнем риска.</span><span class="sxs-lookup"><span data-stu-id="44c3e-109">**Send copies of suspicious messages**: These messages are marked as spam (regardless of the SCL rating) and are not rejected by the filter, but are routed through the higher risk delivery pool.</span></span> <span data-ttu-id="44c3e-110">Чтобы указать получателей для этих обнаруженных сообщений, вы можете использовать командлеты центра администрирования Exchange или командлеты \*\* \*-хостедаутбаундспамфилтерполици\*\* в Exchange Online PowerShell или Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="44c3e-110">You can use the Exchange admin center (EAC) or the **\*-HostedOutboundSpamFilterPolicy** cmdlets in Exchange Online PowerShell or Exchange Online Protection PowerShell to specify addition recipients for these detected messages.</span></span> <span data-ttu-id="44c3e-111">Обратите внимание, что получатели добавляются как получатели **скрытой копии** (поля " **от** " и " **Кому** " являются исходными отправителями и получателями).</span><span class="sxs-lookup"><span data-stu-id="44c3e-111">Note that the recipients are added as **Bcc** recipients (the **From** and **To** fields are the original sender and recipient).</span></span>

- <span data-ttu-id="44c3e-112">**Отправлять уведомления при блокировке отправителя**: при достижении значительных нежелательных сообщений от определенного пользователя отключается отправка сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="44c3e-112">**Send notifications when a sender is blocked**: When a significant amount of spam is coming from a particular user, the user is disabled from sending email messages.</span></span> <span data-ttu-id="44c3e-113">По умолчанию администраторы получают уведомление, но вы можете использовать пользователя, не отправившего [политику оповещений](alert-policies.md) **по электронной почте** , в центре безопасности Office 365 & соответствия требованиям для настройки дополнительных получателей уведомлений.</span><span class="sxs-lookup"><span data-stu-id="44c3e-113">Admins are notified by default, but you can use the **User restricted from sending email** [alert policy](alert-policies.md) in the Office 365 Security & Compliance Center to configure additional notification recipients.</span></span>

  <span data-ttu-id="44c3e-114">Чтобы узнать, как выглядит это уведомление, ознакомьтесь с [примером уведомления о том, что отправитель блокирует отправку исходящих нежелательных сообщений](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span><span class="sxs-lookup"><span data-stu-id="44c3e-114">To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span></span> <span data-ttu-id="44c3e-115">Сведения о том, как повторно включить пользователю отправку сообщений, см. в статье [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span><span class="sxs-lookup"><span data-stu-id="44c3e-115">For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="44c3e-116">Что нужно знать перед началом работы?</span><span class="sxs-lookup"><span data-stu-id="44c3e-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="44c3e-117">Предполагаемое время для завершения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="44c3e-117">Estimated time to complete: 5 minutes</span></span>

- <span data-ttu-id="44c3e-118">Сведения о том, как открыть Центр безопасности и соответствия требованиям, см. в статье [Центр безопасности и соответствия требованиям Office 365](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="44c3e-118">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="44c3e-119">Чтобы открыть центр администрирования Exchange, ознакомьтесь со статьей [центр администрирования Exchange в Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) или [центр администрирования Exchange в Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="44c3e-119">To open the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) or [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="44c3e-120">Чтобы открыть Exchange Online PowerShell, ознакомьтесь [со статьей подключение к Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="44c3e-120">To open Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="44c3e-121">Чтобы открыть консоль Exchange Online Protection PowerShell, ознакомьтесь со статьей [Подключение к PowerShell для Exchange Online Protection](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="44c3e-121">To open Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="44c3e-122">Перед выполнением этой процедуры учетной записи необходимо назначить разрешения.</span><span class="sxs-lookup"><span data-stu-id="44c3e-122">Your account needs to be assigned permissions before you can perform this procedure.</span></span> <span data-ttu-id="44c3e-123">Чтобы узнать, какие разрешения вам нужны, просмотрите запись роли "Управление оповещениями" в разделе [разрешения в центре безопасности Office 365 & соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="44c3e-123">To see what permissions you need, see the "Manage Alerts" role entry in [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="44c3e-124">Настройка дополнительных получателей для исходящих сообщений нежелательной почты с помощью центра администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="44c3e-124">Use the EAC to configure additional recipients for outbound spam messages</span></span>

1. <span data-ttu-id="44c3e-125">В центре администрирования Exchange перейдите к разделу **Защита** \> **исходящих нежелательных сообщений**.</span><span class="sxs-lookup"><span data-stu-id="44c3e-125">In the EAC, go to **Protection** \> **Outbound spam**.</span></span>

2. <span data-ttu-id="44c3e-126">Выберите политику **по умолчанию**и нажмите кнопку **изменить** ![значок](media/ITPro-EAC-EditIcon.png)редактирования.</span><span class="sxs-lookup"><span data-stu-id="44c3e-126">Select the policy named **Default**, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>

3. <span data-ttu-id="44c3e-127">На открывшейся странице свойств убедитесь, что выбрана вкладка **настройки исходящих нежелательных сообщений** , а затем настройте следующий параметр:</span><span class="sxs-lookup"><span data-stu-id="44c3e-127">In the properties page that opens, verify that the **Outbound spam preferences** tab is selected, and then configure the following setting:</span></span>

   <span data-ttu-id="44c3e-128">**Отправить копию всех подозрительных исходящих сообщений электронной почты по следующим адресам электронной почты или**адресам: Установите этот флажок и введите адреса электронной почты одного или нескольких администраторов, которые следует добавить в поле **"СК"** обнаруженных сообщений.</span><span class="sxs-lookup"><span data-stu-id="44c3e-128">**Send a copy of all suspicious outbound email messages to the following email address or addresses**: Select the check box and enter the email addresses of one or more administrators who should be added to the **Bcc** field of detected messages.</span></span> <span data-ttu-id="44c3e-129">Разделяйте адреса электронной почты точками с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="44c3e-129">Separate multiple email addresses with a semicolon ( ; ).</span></span>

   <span data-ttu-id="44c3e-130">Когда закончите, нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44c3e-130">When you're finished, click **Save**.</span></span>

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="44c3e-131">Настройка дополнительных получателей для исходящих сообщений нежелательной почты с помощью Exchange Online PowerShell или Exchange Online Protection PowerShell</span><span class="sxs-lookup"><span data-stu-id="44c3e-131">Use Exchange Online PowerShell or Exchange Online Protection PowerShell to configure additional recipients for outbound spam messages</span></span>

<span data-ttu-id="44c3e-132">Чтобы включить и настроить дополнительные получатели для исходящих сообщений о нежелательной почте, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="44c3e-132">To enable and configure additional recipients for outbound spam messages, use the following syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- <span data-ttu-id="44c3e-133">Чтобы указать получателей, которые перезапишут все существующие значения, используйте `emailaddress1,emailaddress2,...emailaddressN`синтаксис.</span><span class="sxs-lookup"><span data-stu-id="44c3e-133">To specify recipients that overwrite all existing values, use the syntax `emailaddress1,emailaddress2,...emailaddressN`.</span></span>

- <span data-ttu-id="44c3e-134">Чтобы выборочно добавлять или удалять получателей, не затрагивая другие элементы, используйте синтаксис `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.</span><span class="sxs-lookup"><span data-stu-id="44c3e-134">To selectively add or remove recipients without affecting the other entries, use the syntax `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.</span></span>

<span data-ttu-id="44c3e-135">В этом примере показано, как включить и настроить chris@contoso.com, laura@contoso.com и julia@contoso.com как получателей скрытой копии для исходящих сообщений нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="44c3e-135">This example enables and configures chris@contoso.com, laura@contoso.com and julia@contoso.com as Bcc recipients for outbound spam messages.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

<span data-ttu-id="44c3e-136">В этом примере показано, как добавить michelle@contoso.com в качестве дополнительного получателя скрытой копии.</span><span class="sxs-lookup"><span data-stu-id="44c3e-136">This example adds michelle@contoso.com as an additional Bcc recipient.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

<span data-ttu-id="44c3e-137">В этом примере показано удаление chris@contoso.com и julia@contoso.com из списка получателей скрытой копии.</span><span class="sxs-lookup"><span data-stu-id="44c3e-137">This example removes chris@contoso.com and julia@contoso.com from the list of Bcc recipients.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

<span data-ttu-id="44c3e-138">Подробные сведения о синтаксисе и параметрах можно найти в статье [Set – хостедаутбаундспамфилтерполици](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="44c3e-138">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span></span>

<span data-ttu-id="44c3e-139">**Note**: выполните команду `Get-HostedOutboundSpamFilterPolicy | Format-List` , чтобы просмотреть текущие значения свойств *бкксуспиЦиаусаутбаундмаил* и *бкксуспиЦиаусаутбаундаддитионалреЦипиентс* .</span><span class="sxs-lookup"><span data-stu-id="44c3e-139">**Note**: Run the command `Get-HostedOutboundSpamFilterPolicy | Format-List` to see the current values of the *BccSuspiciousOutboundMail* and *BccSuspiciousOutboundAdditionalRecipients* properties.</span></span>

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a><span data-ttu-id="44c3e-140">Использование центра безопасности & соответствия требованиям для настройки уведомлений при блокировке отправителя</span><span class="sxs-lookup"><span data-stu-id="44c3e-140">Use the Security & Compliance Center to configure notifications when a sender is blocked</span></span>

1. <span data-ttu-id="44c3e-141">В центре безопасности & соответствия требованиям перейдите к разделу **оповещения** \> **о политиках оповещений**.</span><span class="sxs-lookup"><span data-stu-id="44c3e-141">In the Security & Compliance Center, go to **Alerts** \> **Alert Policies**.</span></span>

2. <span data-ttu-id="44c3e-142">Найдите и выберите политику с именем " **пользователь не ограничен отправкой электронной почты**".</span><span class="sxs-lookup"><span data-stu-id="44c3e-142">Find and select the policy named **User restricted from sending email**.</span></span>

3. <span data-ttu-id="44c3e-143">В открывшемся диалоговом окне щелкните **изменить политику**.</span><span class="sxs-lookup"><span data-stu-id="44c3e-143">In the fly out that opens, click **Edit policy**.</span></span>

4. <span data-ttu-id="44c3e-144">На открывшейся странице **Изменение получателей** настройте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="44c3e-144">In the **Edit recipients** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="44c3e-145">**Отправлять уведомления по электронной почте**: Убедитесь, что установлен флажок **вкл** .</span><span class="sxs-lookup"><span data-stu-id="44c3e-145">**Send email notifications**: Verify that **On** is selected.</span></span>

   - <span data-ttu-id="44c3e-146">**Получатели электронной почты**: по умолчанию **тенантадминс** — единственное значение.</span><span class="sxs-lookup"><span data-stu-id="44c3e-146">**Email recipients**: By default **TenantAdmins** is the only value here.</span></span> <span data-ttu-id="44c3e-147">Чтобы добавить дополнительных получателей, щелкните пустое место в этом поле, начните ввод получателя и выберите получателя при разрешении его имени.</span><span class="sxs-lookup"><span data-stu-id="44c3e-147">To add additional recipients, click in an empty spot in this box, start typing the recipient, and select the recipient when their name resolves.</span></span> <span data-ttu-id="44c3e-148">Чтобы удалить получателей, щелкните **X** рядом с их именами.</span><span class="sxs-lookup"><span data-stu-id="44c3e-148">To remove recipients, click on the **X** next to their names.</span></span>

   - <span data-ttu-id="44c3e-149">**Число ежедневных уведомлений**: значение по умолчанию не **ограничено**, но можно настроить различные ограничения от 1 до 200.</span><span class="sxs-lookup"><span data-stu-id="44c3e-149">**Daily notification limit**: The default value is **No limit**, but you can configure various limits from 1 to 200.</span></span>

   <span data-ttu-id="44c3e-150">Когда закончите, нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="44c3e-150">When you're finished, click **Save**.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="44c3e-151">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="44c3e-151">For more information</span></span>

[<span data-ttu-id="44c3e-152">Пул доставки сообщений с высоким уровнем опасности</span><span class="sxs-lookup"><span data-stu-id="44c3e-152">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="44c3e-153">Вопросы и ответы по защите от нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="44c3e-153">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
