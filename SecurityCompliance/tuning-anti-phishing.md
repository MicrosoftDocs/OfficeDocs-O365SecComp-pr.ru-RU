---
title: Настройка защиты от фишинга в Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Администраторы могут узнать причины, по которым и как проходят фишинговые сообщения, а также что делать, чтобы предотвратить большее количество фишинговых сообщений в будущем.
ms.openlocfilehash: efda9e16c23e4533b6951e43ac085b7640e84576
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/28/2019
ms.locfileid: "30937830"
---
# <a name="tune-anti-phishing-protection-in-office-365"></a>Настройка защиты от фишинга в Office 365

Несмотря на то, что в Office 365 есть разнообразные функции защиты от фишинга, которые включены по умолчанию, некоторые фишинговые сообщения могут быть по-прежнему доставляются в почтовые ящики. В этом разделе описывается, что можно сделать, чтобы узнать, почему сообщение фишинга было получено, и что можно сделать для настройки параметров защиты от фишинга в организации Exchange Online _без случайного внесения_.

## <a name="first-things-first-deal-with-any-compromised-accounts-and-make-sure-you-block-any-more-phishing-messages-from-getting-through"></a>Сначала выполните действия, связанные с любыми скомпрометированными учетными записями, и убедитесь, что вы блокируете все сообщения с фишингом от получения

Если учетная запись получателя была скомпрометирована в результате фишингового сообщения, выполните действия, описанные в разделе [ответ на скомпрометированную учетную запись электронной почты в Office 365](responding-to-a-compromised-email-account.md).

Если ваша подписка включает Advanced Threat protection (ATP), вы можете использовать [Office 365 Threat Intelligence](office-365-ti.md) , чтобы определить других пользователей, которые также получили сообщение фишинга. Вы можете заблокировать фишинговые сообщения с дополнительными параметрами:

- [Безопасные ссылки ATP](set-up-atp-safe-links-policies.md)

- [Безопасные вложения ATP](set-up-atp-safe-attachments-policies.md)

- [Политики защиты от фишинга ATP](set-up-anti-phishing-policies.md). Обратите внимание, что вы можете временно увеличить **пороговые значения расширенного фишинга** в политике от **стандарта** к **агрессивному**, **более агрессивному**или **наиболее агрессивному**.

Убедитесь, что функции ATP включены.

## <a name="report-the-phishing-message-to-microsoft"></a>Сообщить о phishing-сообщениях корпорации Майкрософт

Создание отчетов о фишинговых сообщениях полезно при настройке фильтров, используемых для защиты всех клиентов в Office 365.

Отправка фишингового сообщения в _виде вложения_ в новое, в ином случае пустое сообщение в **Phish@office365.microsoft.com**. Не просто пересылайте исходное сообщение; в противном случае мы не можем проверить заголовки исходного сообщения. Кроме того, вы можете использовать надстройку [сообщения отчета](https://docs.microsoft.com/office365/securitycompliance/enable-the-report-message-add-in) в Outlook или Outlook в Интернете (прежнее название — Outlook Web App).

Дополнительные сведения о том, [как отправлять сообщения о нежелательной почте и мошеннических сообщениях в корпорацию Майкрософт для анализа](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).

## <a name="inspect-the-message-headers"></a>Проверка заголовков сообщений

Вы можете проверить заголовки сообщения фишинга, чтобы убедиться, что вы можете сделать что-либо, чтобы предотвратить появление более фишинговых сообщений. Другими словами, исследование заголовков сообщений поможет определить параметры в Организации, которые отвечают за разрешение фишинговых сообщений в.

В частности, следует проверить поле заголовка **X-Forefront-защиты от спама-Report** в заголовках сообщений для указания пропущенных фильтров нежелательной почты или фишинга в значении фильтра неЖелательной почты ВРЕДОНОСНОСТИ (SFV). Для `SCL:-1`сообщений, пропускаемых при фильтрации, будет задано значение, то есть одно из параметров, разрешенное этим сообщением путем переопределения спама или вердиктс фишинга, определенных службой. Дополнительные сведения о том, как получить заголовки сообщений и полный список всех доступных заголовков сообщений для защиты от нежелательной почты и фишинга, приведены в разделе [заголовки сообщений](https://docs.microsoft.com/office365/SecurityCompliance/anti-spam-message-headers)по защите от нежелательной почты.

## <a name="best-practices-to-stay-protected"></a>Рекомендации по обеспечению защиты

- При ежемесячном запуске [office 365 Secure Score](office-365-secure-score.md) для оценки параметров безопасности организации Office 365.

- Периодически проверяйте [отчет о подделке](learn-about-spoof-intelligence.md) и [включите защиту от фишинга в политике защиты от фишинга](learn-about-spoof-intelligence.md#configuring-the-anti-spoofing-policy) для помещения подозрительных сообщений вместо того, чтобы помещать их в папку нежелательной почты пользователя. ****

- Периодически изучите [отчет о состоянии защиты от угроз](view-reports-for-atp.md#threat-protection-status-report).

- Некоторые пользователи случайно разрешают фишинговые сообщения, помещая собственные домены в списке Разрешить отправителя или разрешить домены в политиках защиты от нежелательной почты. При выборе этого варианта следует соблюдать особую осторожность. Несмотря на то, что эта конфигурация позволит использовать некоторые законные сообщения, она также будет допускать вредоносные сообщения, которые обычно блокируются фильтрами спама и/или фишинга Office 365.

  Лучший способ работы с законными сообщениями, которые заблокированы в Office 365 (ложные срабатывания), которые включают отправителей в вашем домене, — полностью и полностью настраивают записи SPF, DKIM и DMARC в DNS для _всех_ доменов электронной почты в Office 365:

  - Убедитесь, что запись SPF определяет _все_ источники электронной почты для отправителей в вашем домене (не забывайте о сторонних службах!).

  - Используйте жесткое отказ (\-), чтобы убедиться, что нежелательные отправители отклоняются почтовыми системами, настроенными для этого. Можно использовать [логику подделки](https://docs.microsoft.com/office365/securitycompliance/learn-about-spoof-intelligence) для определения отправителей, использующих ваш домен, чтобы вы могли добавить авторизованных отправителей сторонних поставщиков в запись SPF.

  Инструкции по настройке можно найти в следующих статьях:
  
  - [Настройка SPF в Office 365 для предотвращения спуфинга](set-up-spf-in-office-365-to-help-prevent-spoofing.md)

  - [Проверка исходящей электронной почты, отправляемой с личного домена в Office 365, с помощью DKIM](use-dkim-to-validate-outbound-email.md)

  - [Проверка электронной почты в Office 365 с помощью DMARC](use-dmarc-to-validate-email.md)

- По мере возможности рекомендуется доставлять электронную почту для домена непосредственно в Office 365. Другими словами, укажите запись MX домена Office 365 в Office 365. Exchange Online Protection (EOP) может предоставить лучшую защиту облачных пользователей, когда их почта доставляется непосредственно в Office 365. Если вам необходимо использовать сторонние системы электронной почты санацией перед EOP, убедитесь, что вы выполнили указания, приведенные [здесь](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-mail-flow-using-third-party-cloud).

- Многофакторная проверка подлинности (MFA) — это действительно хороший способ предотвращения скомпрометированных учетных записей. Необходимо строго рассмотреть включение MFA для всех пользователей. Для поэтапного подхода Начните с включения MFA для наиболее важных пользователей (администраторов, руководителей и т. д.), прежде чем включать MFA для всех. Инструкции приведены в разделе [Настройка многофакторной проверки](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication)подлинности.

- Правила переСылки внешним получателям часто используются злоумышленниками для извлечения данных. Используйте сведения **** о правилах пересылки почтовых ящиков в [Office 365 Secure Score](office-365-secure-score.md) , чтобы найти и даже предотвратить появление правил переадресации внешним получателям. Дополнительные сведения приведены в статье [устраненИе внешних правил переадресации клиентов с помощью оценки безопасности](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/).