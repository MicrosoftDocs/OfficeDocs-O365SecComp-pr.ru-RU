---
title: Политика шифрования сообщений Office 365 для конфиденциальной информации
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Сводка. Политика шифрования сообщений Office 365 для типов конфиденциальной информации теперь доступны.
ms.openlocfilehash: 99cb7a9f94c9cf4036c11b74a5208ddf0e819ceb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261267"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>Политика шифрования сообщений Office 365 для конфиденциальной информации

Update (1/30/19): в октябре 2018 мы работали с небольшим примером клиентов, чтобы узнать, можно ли упростить защиту, автоматически шифруя конфиденциальные сообщения электронной почты, основанные на определенных типах конфиденциальной информации. На основе положительной обратной связи из этого примера мы решили расширить профиль клиентов на более разнообразную версию в декабре 2018 декабря. После того, как вы выберете сведения о клиентах, мы прослушали ваш отзыв и определили, что клиенты с более сложными средами хотели бы реализовать эти правила с осторожностью, и поэтому мы намерены настроить наши планы.

Если ваша организация была выбрана для выпуска с 15 января 2019, то автоматическая политика не выполняется. Вместо этого мы предоставляем инструкции, приведенные в этой статье, о том, как можно выполнить развертывание йоурселвес. Продолжайте чтение, чтобы узнать, как.

||
|:-----|
|Эта статья входит в набор статей, посвященных шифрованию сообщений Office 365. Эта статья предназначена для администраторов и Итпрос. Если вы просто ищете сведения о том, как отправлять или получать зашифрованные сообщения, ознакомьтесь со статьей, посвященной [шифрованИю сообщений Office 365 (OME)](ome.md) , и выберите статью, которая наилучшим образом соответствует вашим потребностям. |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a>Создание политики типов конфиденциальной информации для клиента

Для создания политики типов конфиденциальной информации можно использовать правила для обработки почты Exchange или предотвращение потери данных (DLP) Office 365. Чтобы создать правило для процесса обработки почты Exchange, вы можете использовать центр администрирования Exchange или PowerShell.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>Создание политики с помощью правил для почтового процесса в центре администрирования Exchange

Войдите в центр администрирования Exchange и перейдите к разделу > **правила**для поток обработки **почты**. В этом случае создайте правило, которое применяет шифрование сообщений Office 365 на основе таких условий, как присутствие определенных ключевых слов или типов конфиденциальной информации в сообщении или вложении.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>Создание политики с помощью правил для почтового процесса в PowerShell

С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online. Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell). Используйте командлеты Set – IRMConfiguration и New – Транспорруле для создания политики.

### <a name="example-mail-flow-rule-created-with-powershell"></a>Пример правила для процесса обработки почты, созданного с помощью PowerShell

Выполнение следующих команд в PowerShell создание правила для обработки почты Exchange, которое автоматически шифрует сообщения, находящихся за пресроком Организации, с помощью политики *только для шифрования* , если сообщения электронной почты или их вложения содержат следующие конфиденциальные данные типы сведений:

- Номер маршрутизации код банка ABA
- Номер кредитной карты
- Номер агентства для применения наркотиков (DEA)
- США/ВЕЛИКОБРИТАНИЯ passport number
- Номер банковского счета США
- Идентификационный номер налогоплательщика для США (ITIN)
- Страховой номер для США (SSN)

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a>Как получатели обращаются к вложениям

После шифрования сообщения у получателей будет неограниченный доступ к вложениям после того, как они обращаются к ним и открывают зашифрованную электронную почту.

## <a name="to-prepare-for-this-change"></a>Подготовка к выполнению этого изменения

Вам может потребоваться обновить любую документацию конечного пользователя и обучающие материалы, чтобы подготовить пользователей в Организации к этому изменению. Предоставьте им доступ к этим ресурсам по шифрованию сообщений Office 365, используя соответствующие пользователи:

- [Отправка, просмотр зашифрованных сообщений и ответ на них в Outlook для компьютера](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Видео Office 365 Essentials: шифрование сообщений Office](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>Просмотр изменений в журнале аудита

Это действие подлежит аудиту и доступно администраторам Office 365. Операция — "New-TransportRule", а фрагмент примера записи аудита из поиска в журнале аудита в центре безопасности _Амп_ соответствия требованиям ниже:

|     |
| --- |
| *{"CreationTime": "2018 г. – 11 — 28T23:35:01", "ID": "a1b2c3d4-daa0-4c4f-A019-03a1234a1b0c", "Operation": "New/TransportRule", "Организатионид": "123456 – 221d – 12345", "RecordType": "ResultStatus", "", "UserKey": "оператор Майкрософт", " UserType ": 3," Version ": 1," Рабочая нагрузка ":" Exchange "," Клиентип ":" 123.456.147.68:17584 "," ObjectId ":", "UserId": "Microsoft оператор", "Екстерналакцесс":Труе, "Организатионнаме":"contoso. onmicrosoft. com", "OriginatingServer": "CY4PR13MBXXXX ( 15.20.1382.008) "," Parameters ": {" имя ":" Организация "," значение ":" 123456-221d-12346 "{" Name ":" Апплиригхтспротектионтемплате "," value ":" Encrypting "}, {" Name ":" Name "," value ":" заШифровать исходящие сообщения электронной почты (")"}, {"Name": " MessageContainsDataClassifications "... документов.* |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>Отключение или Настройка политики типов конфиденциальной информации

После создания правила для почтовых ящиков Exchange вы можете [отключить или изменить правило](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , перейдя к **** > **правилам** обработки почтового ящика в центре администрирования Exchange, и отключить правило "*шифровать исходящие сообщения электронной почты от"* . ".
