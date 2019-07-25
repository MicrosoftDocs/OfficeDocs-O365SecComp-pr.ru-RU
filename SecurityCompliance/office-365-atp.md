---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 03/28/2019
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection включает в себя безопасные вложения, безопасные ссылки, расширенные средства защиты от фишинга, средства создания отчетов и возможности анализа угроз.
ms.openlocfilehash: 96e79a8aabe0788388473da9fcd514b9285e1c00
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854783"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

> [!IMPORTANT]
> Эта статья предназначена для корпоративных клиентов, у которых есть [Office 365 Advanced Threat protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). Если вы используете Outlook.com, Office 365 Home или Office 365 Personal, а вы ищете сведения о безопасных ссылках в Outlook, ознакомьтесь со статьей [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

## <a name="overview"></a>Обзор

Office 365 Advanced Threat protection (ATP) защищает организацию от вредоносных угроз, исносящихся к сообщениям электронной почты, ссылкам (URL-адресам) и средствам совместной работы. Пакет ATP включает в себя:

- [Политики защиты от угроз](#configure-atp-policies): определение политик защиты от угроз для установки подходящего уровня защиты для Организации. 

- [Отчеты](#view-atp-reports): Просмотр отчетов в режиме реального времени для мониторинга производительности ATP в Организации. 

- [Исследование угроз и возможности реагирования](#use-threat-investigation-and-response-capabilities): используйте ведущие инструменты для изучения, анализа, имитации и предотвращения угроз. 

- [Автоматизированное исследование и возможности реагирования](#save-time-with-automated-investigation-and-response): экономия времени и сил при исследовании и уменьшении угроз.

## <a name="office-365-atp-plan-1-and-plan-2"></a>Office 365 ATP (план 1) и план 2

ATP включена в Office 365 в ~; Тем не менее, план ATP и пакет ATP 2 доступны в качестве надстройки для некоторых подписок. Чтобы узнать больше, ознакомьтесь со статьей [доступность функций в планах ATP](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).

## <a name="configure-atp-policies"></a>Настройка политик ATP

Office 365 ATP предоставляет множество средств для настройки соответствующего уровня защиты в Организации. 

Группа безопасности Организации должна определять политики для каждого средства ATP в центре безопасности Office 365 & соответствия требованиям. Перейдите к разделу**Политика** **управления** > угрозами, чтобы получить доступ к параметрам политики. Для получения справки по этому представлению в разделе [Краткое руководство по началу работы: Настройка Office 365 Advanced Threat protection](checklist-atp-setup.md).)

Политики, определенные для Организации, определяют поведение и уровень защиты для предварительно определенных угроз. Параметры политики очень гибки. Например, группа безопасности Организации может установить детальную защиту от угроз на уровне пользователя, Организации, получателя и домена. Важно регулярно проверять свои политики, так как новые угрозы и проблемы возникают ежедневно.  

- [Безопасные вложения ATP](atp-safe-attachments.md): обеспечивает защиту системы обмена сообщениями с нулевым сроком действия путем проверки вложений электронной почты для вредоносного контента. Он маршрутизирует все сообщения и вложения, для которых нет подписи вирусов или вредоносных программ, в специальную среду, а затем использует приемы машинного обучения и анализа для обнаружения вредоносных целей. Если подозрительное действие не найдено, сообщение перенаправляется в почтовый ящик. Чтобы узнать больше, ознакомьтесь со статьей [Настройка политик безопасных вложений Office 365 ATP](set-up-atp-safe-attachments-policies.md).

- [Ссылки ATP Safe](atp-safe-links.md): предоставляет время на проверку URL-адресов, например, в сообщениях электронной почты и файлах Office. Защита работает и применяется в вашей среде обмена сообщениями и Office. Ссылки проверяются по нажатию кнопки: безопасные ссылки продолжают работать, а вредоносные ссылки динамически блокируются. Чтобы узнать больше, ознакомьтесь со статьей [Настройка политик безопасных ссылок на Office 365 ATP](https://docs.microsoft.com/en-us/office365/securitycompliance/set-up-atp-safe-links-policies). 

- [ATP для SharePoint, OneDrive и Microsoft Teams](atp-for-spo-odb-and-teams.md): защищает организацию, когда пользователи совместно работают и совместно используют файлы, определяя и блокируя вредоносные файлы на сайтах групп и библиотеках документов. Чтобы узнать больше, ознакомьтесь [со статьей включение Office 365 ATP для SharePoint, OneDrive и Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md). 

- [Защита от фишинга ATP](atp-anti-phishing.md): обнаруживает попытки олицетворения пользователей и пользовательских доменов. В нем применяются модели машинного обучения и расширенные алгоритмы обнаружения олицетворения для Аверт фишинговых атак. Чтобы узнать больше, ознакомьтесь со статьей [Настройка защиты от фишинга и антифишинга Office 365 ATP](set-up-anti-phishing-policies.md).

## <a name="view-atp-reports"></a>Просмотр отчетов ATP

Office 365 ATP включает расширенную [информационную панель отчетов](view-reports-for-atp.md) для наблюдения за производительностью ATP. Вы можете получить доступ к нему в **отчетах > панели мониторинга** в центре обеспечения безопасности &. 

Отчеты обновляются в режиме реального времени и обеспечивают получение последних сведений. В этих отчетах также представлены рекомендации и оповещения о возможных угрозах. К предопределенным отчетам относятся следующие: 

- [Обозреватель угроз (или обнаружение в режиме реального времени)](threat-explorer.md)

- [Отчет о состоянии защиты от угроз](view-reports-for-atp.md#threat-protection-status-report)

- [Отчет о типах файлов ATP](view-reports-for-atp.md#atp-file-types-report)

- [Отчет об ликвидации сообщений ATP](view-reports-for-atp.md#atp-message-disposition-report)

- ... и многое другое. 

## <a name="use-threat-investigation-and-response-capabilities"></a>Использование средств расследования и реагирования на угрозы

Office 365 ATP (план 2) содержит лучшие средства для [расследования и реагирования на угрозы](office-365-ti.md) , которые позволяют группе безопасности Организации ожидать, уяснить и предотвращать вредоносные атаки. 

- Средства [отслеживания угроз](threat-trackers.md) предоставляют вам самую актуальную аналитику при возникновении проблем с циберсекурити. Например, вы можете просмотреть сведения о последних вредоносных программах и принять контрмеры, прежде чем она станет действительной угрозой для вашей организации. Доступные средства отслеживания включают [отслеживаемые средства отслеживания](threat-trackers.md#noteworthy-trackers), [Отслеживание тенденций](threat-trackers.md#trending-trackers), [отслеживаемые запросы](threat-trackers.md#tracked-queries)и [сохраненные запросы](threat-trackers.md#saved-queries).

- [Обозреватель угроз (или обнаружение в режиме реального времени)](threat-explorer.md) (также называется проводником) — это отчет в реальном времени, который позволяет идентифицировать и проанализировать последние угрозы. Вы можете настроить обозреватель для отображения данных для настраиваемых периодов.

- [Имитатор атаки](attack-simulator.md) позволяет запускать реалистичные сценарии атак в Организации для определения вулнерабилитес. Доступны имитации текущих типов атак, в том числе отображаемое [имя спеар-фишинговых](attack-simulator.md#display-name-spear-phishing-attack)атак, атаки с использованием [паролей](attack-simulator.md#password-spray-attack), атаки с помощью [](attack-simulator.md#brute-force-password-attack)пароля и т. д.
    
## <a name="save-time-with-automated-investigation-and-response"></a>Экономия времени с помощью автоматического исследования и ответа

(**New!**) Когда вы изучаете потенциальную атаку кибератак, время представляет собой суть. Чем раньше вы сможете определять и устранять угрозы, тем выше будет организация. В Office 365 ATP (план 2) теперь включены возможности [автоматического исследования и реагирования (AIR)](automated-investigation-response-office.md) . (Если у вас еще нет этих возможностей, вы получите их в ближайшее время с помощью ATP Plan 2.)

В воздух включен набор "Playbooks" безопасности, который можно запустить автоматически, например при срабатывании оповещения или вручную, например из представления в проводнике. Воздушный поток может сэкономить время и усилия группы управления безопасностью при снижении угроз, а также эффективно и эффективно. Чтобы узнать больше, ознакомьтесь [со статьей автоматизированное исследование и ответ (AIR) с Office 365](automated-investigation-response-office.md).

## <a name="permissions-required-to-use-atp-features"></a>Разрешения, необходимые для использования функций ATP

Чтобы получить доступ к функциям ATP в центре безопасности & соответствия требованиям, необходимо назначить соответствующую роль. В следующей таблице приводятся некоторые примеры.

|Роль или группа ролей  |Ресурсы для получения дополнительных сведений  |
|---------|---------|
|Глобальный администратор Office 365 |[Роли администраторов в Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|администратор безопасности (Security Administrator). |[Разрешения роли администратора в Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Управление организацией Exchange Online |[Разрешения в Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>и<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Дополнительные сведения см. в следующих статьях:

- [Разрешения в Центре безопасности и соответствия требованиям](permissions-in-the-security-and-compliance-center.md) 

- [Предоставление пользователям доступа к Центру безопасности и соответствия требованиям](grant-access-to-the-security-and-compliance-center.md)

## <a name="get-office-365-atp"></a>Получение пакета Office 365 ATP

Office 365 ATP (план 2) включен в Office 365 корпоративный, Office 365 для образования A5 и Microsoft 365 бизнес. Если ваша подписка не включает Office 365 ATP, вы можете приобрести заказ ATP 1 или ATP (план 2) в качестве надстройки для некоторых подписок. Чтобы узнать больше, ознакомьтесь со следующими материалами:

- Список подписок, включающих планы ATP, можно найти в статье [Office 365 Advanced Threat protection (ATP)](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#office-365-advanced-threat-protection-atp-availability) .

- Список компонентов, включенных в план 1 и 2, представлен в статье сведения о [доступности функций в планах расширенной защиты от угроз (ATP)](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans) .

- Ознакомьтесь [со статьей получение расширенной защиты от угроз для office 365](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content) , в которой вы можете сравнить планы и приобрести пакет ATP для Office 365.

## <a name="new-features-in-office-365-atp"></a>Новые возможности в Office 365 ATP

Новые функции добавляются в Office 365 ATP непрерывно. Чтобы узнать больше, ознакомьтесь со следующими материалами:

- [План Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection) содержит список новых функций в разработке и развертывании.

- В [описании службы Advanced Threat Protection в Office 365](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) описываются функции и доступность в планах ATP.
