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
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a>Настройка уведомлений об исходящей нежелательной почте в Office 365

Фильтрация исходящей нежелательной почты всегда включена, если эта служба используется для отправки исходящей почты, тем самым помогая защищать организации, использующие эту службу, и их получателей. Как и в случае входящих сообщений, процесс фильтрации исходящих сообщений состоит из фильтрации подключений и фильтрации содержимого, однако настройки исходящей фильтрации не настраиваются. Если исходящее сообщение определено как нежелательное, оно маршрутизируется через пул доставки более высокого риска, что снижает вероятность добавления в список блокировок обычного пула исходящих IP-адресов. Если клиент продолжит отправлять через службу нежелательную почту, отправка сообщений для него будет заблокирована.

Несмотря на то, что отключить или изменить фильтрацию нежелательной почты невозможно, можно настроить следующие параметры уведомлений об исходящей нежелательной почте:

- **Отправлять копии подозрительных сообщений**: эти сообщения помечаются как спам (независимо от оценки вероятности нежелательной почты) и не отклоняются фильтром, но направляются через пул доставки с более высоким уровнем риска. Чтобы указать получателей для этих обнаруженных сообщений, вы можете использовать командлеты центра администрирования Exchange или командлеты ** \*-хостедаутбаундспамфилтерполици** в Exchange Online PowerShell или Exchange Online Protection PowerShell. Обратите внимание, что получатели добавляются как получатели **скрытой копии** (поля " **от** " и " **Кому** " являются исходными отправителями и получателями).

- **Отправлять уведомления при блокировке отправителя**: при достижении значительных нежелательных сообщений от определенного пользователя отключается отправка сообщений электронной почты. По умолчанию администраторы получают уведомление, но вы можете использовать пользователя, не отправившего [политику оповещений](alert-policies.md) **по электронной почте** , в центре безопасности Office 365 & соответствия требованиям для настройки дополнительных получателей уведомлений.

  Чтобы узнать, как выглядит это уведомление, ознакомьтесь с [примером уведомления о том, что отправитель блокирует отправку исходящих нежелательных сообщений](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Сведения о том, как повторно включить пользователю отправку сообщений, см. в статье [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).

## <a name="what-do-you-need-to-know-before-you-begin"></a>Что нужно знать перед началом работы?

- Предполагаемое время для завершения: 5 минут.

- Сведения о том, как открыть Центр безопасности и соответствия требованиям, см. в статье [Центр безопасности и соответствия требованиям Office 365](go-to-the-securitycompliance-center.md).

- Чтобы открыть центр администрирования Exchange, ознакомьтесь со статьей [центр администрирования Exchange в Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) или [центр администрирования Exchange в Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).

- Чтобы открыть Exchange Online PowerShell, ознакомьтесь [со статьей подключение к Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Чтобы открыть консоль Exchange Online Protection PowerShell, ознакомьтесь со статьей [Подключение к PowerShell для Exchange Online Protection](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).

- Перед выполнением этой процедуры учетной записи необходимо назначить разрешения. Чтобы узнать, какие разрешения вам нужны, просмотрите запись роли "Управление оповещениями" в разделе [разрешения в центре безопасности Office 365 & соответствия требованиям](permissions-in-the-security-and-compliance-center.md).

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a>Настройка дополнительных получателей для исходящих сообщений нежелательной почты с помощью центра администрирования Exchange

1. В центре администрирования Exchange перейдите к разделу **Защита** \> **исходящих нежелательных сообщений**.

2. Выберите политику **по умолчанию**и нажмите кнопку **изменить** ![значок](media/ITPro-EAC-EditIcon.png)редактирования.

3. На открывшейся странице свойств убедитесь, что выбрана вкладка **настройки исходящих нежелательных сообщений** , а затем настройте следующий параметр:

   **Отправить копию всех подозрительных исходящих сообщений электронной почты по следующим адресам электронной почты или**адресам: Установите этот флажок и введите адреса электронной почты одного или нескольких администраторов, которые следует добавить в поле **"СК"** обнаруженных сообщений. Разделяйте адреса электронной почты точками с запятой (;).

   Когда закончите, нажмите кнопку **Сохранить**.

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a>Настройка дополнительных получателей для исходящих сообщений нежелательной почты с помощью Exchange Online PowerShell или Exchange Online Protection PowerShell

Чтобы включить и настроить дополнительные получатели для исходящих сообщений о нежелательной почте, используйте следующий синтаксис:

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- Чтобы указать получателей, которые перезапишут все существующие значения, используйте `emailaddress1,emailaddress2,...emailaddressN`синтаксис.

- Чтобы выборочно добавлять или удалять получателей, не затрагивая другие элементы, используйте синтаксис `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.

В этом примере показано, как включить и настроить chris@contoso.com, laura@contoso.com и julia@contoso.com как получателей скрытой копии для исходящих сообщений нежелательной почты.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

В этом примере показано, как добавить michelle@contoso.com в качестве дополнительного получателя скрытой копии.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

В этом примере показано удаление chris@contoso.com и julia@contoso.com из списка получателей скрытой копии.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

Подробные сведения о синтаксисе и параметрах можно найти в статье [Set – хостедаутбаундспамфилтерполици](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).

**Note**: выполните команду `Get-HostedOutboundSpamFilterPolicy | Format-List` , чтобы просмотреть текущие значения свойств *бкксуспиЦиаусаутбаундмаил* и *бкксуспиЦиаусаутбаундаддитионалреЦипиентс* .

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a>Использование центра безопасности & соответствия требованиям для настройки уведомлений при блокировке отправителя

1. В центре безопасности & соответствия требованиям перейдите к разделу **оповещения** \> **о политиках оповещений**.

2. Найдите и выберите политику с именем " **пользователь не ограничен отправкой электронной почты**".

3. В открывшемся диалоговом окне щелкните **изменить политику**.

4. На открывшейся странице **Изменение получателей** настройте указанные ниже параметры.

   - **Отправлять уведомления по электронной почте**: Убедитесь, что установлен флажок **вкл** .

   - **Получатели электронной почты**: по умолчанию **тенантадминс** — единственное значение. Чтобы добавить дополнительных получателей, щелкните пустое место в этом поле, начните ввод получателя и выберите получателя при разрешении его имени. Чтобы удалить получателей, щелкните **X** рядом с их именами.

   - **Число ежедневных уведомлений**: значение по умолчанию не **ограничено**, но можно настроить различные ограничения от 1 до 200.

   Когда закончите, нажмите кнопку **Сохранить**.

## <a name="for-more-information"></a>Дополнительные сведения

[Пул доставки сообщений с высоким уровнем опасности](high-risk-delivery-pool-for-outbound-messages.md)

[Вопросы и ответы по защите от нежелательной почты](anti-spam-protection-faq.md)
