---
title: Атрибуты политик барьера информации
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Используйте эту статью в качестве справки по различным атрибутам, которые можно использовать в политиках барьера информации.
ms.openlocfilehash: e72e37950442974897de479c7c11f0053a578d1c
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668336"
---
# <a name="attributes-for-information-barrier-policies-preview"></a>Атрибуты политик барьера информации (Предварительная версия)

Некоторые атрибуты в Azure Active Directory можно использовать для сегментирования пользователей. Сегменты затем используются в качестве фильтров для политик барьера данных. Например, вы можете использовать **Отдел** , чтобы определять сегменты пользователей по Отделу в Организации (предполагается, что ни один сотрудник не работает одновременно для двух отделов). 

В этой статье представлен список атрибутов, которые можно использовать. Дополнительные сведения о барьерах информации можно найти в следующих ресурсах:
- [Препятствия для информационных заданных (Предварительная версия)](information-barriers.md)
- [Определение политик для барьеров информации в Microsoft Teams (Предварительная версия)](information-barriers-policies.md)

## <a name="how-to-use-attributes-in-information-barrier-policies"></a>Использование атрибутов в политиках барьера информационных заданных

Атрибуты, приведенные в этой статье, можно использовать для определения (или изменения) сегментов пользователей. Сегменты используются в качестве параметров (Усерграупфилтер) в политиках барьера данных, как показано в следующих примерах:

|Пример  |Командлет  |
|---------|---------|
|Определите сегмент под названием Segment1 с помощью атрибута Department     | `New-OrganizationSegment -Name "Segment1" -UserGroupFilter "Department -eq 'Department1'"`        |
|Определите сегмент с именем Segment с помощью атрибута MemberOf (предположим, что этот атрибут содержит имена групп, например, "Блуеграуп").     | `New-OrganizationSegment -Name "SegmentA" -UserGroupFilter "MemberOf -eq 'BlueGroup'"`        |
|Определите сегмент с именем Дайтрадерс, используя от extensionattribute1 (предположим, что этот атрибут содержит заголовки заданий, например "Дайтрадер").|`New-OrganizationSegment -Name "DayTraders" -UserGroupFilter "ExtensionAttribute1 -eq 'DayTrader'"` |

При определении сегментов используйте один и тот же атрибут для всех сегментов. Например, если вы определили некоторые сегменты с помощью *отдела*, определите все сегменты с помощью *отдела*. Не определяйте некоторые сегменты, используя *Отдел* и другие, используя *MemberOf*. Убедитесь, что сегменты не перекрываются; Каждый пользователь должен быть назначен только одному сегменту. 

Дополнительную информацию можно узнать в статье [Определение сегментов с помощью PowerShell](information-barriers-policies.md#define-segments-using-powershell).

## <a name="reference"></a>Справочные материалы

В следующей таблице перечислены атрибуты, которые можно использовать с барьерами информации.

|Имя свойства Azure Active Directory (отображаемое имя LDAP)  |Имя свойства Exchange  |
|---------|---------|
|Управляющ       | Управляющ        |
|Company     |Company         |
|Отдел     |Отдел         |
|От extensionattribute1 |CustomAttribute1  |
|ExtensionAttribute2 |CustomAttribute2  |
|ExtensionAttribute3 |CustomAttribute3  |
|ExtensionAttribute4 |CustomAttribute4  |
|ExtensionAttribute5 |CustomAttribute5  |
|ExtensionAttribute6 |CustomAttribute6  |
|ExtensionAttribute7 |CustomAttribute7  |
|ExtensionAttribute8 |CustomAttribute8  |
|ExtensionAttribute9 |CustomAttribute9  |
|ExtensionAttribute10 |CustomAttribute10  |
|ExtensionAttribute11 |CustomAttribute11  |
|ExtensionAttribute12 |CustomAttribute12  |
|ExtensionAttribute13 |CustomAttribute13  |
|ExtensionAttribute14 |CustomAttribute14  |
|ExtensionAttribute15 |CustomAttribute15  |
|От msexchextensioncustomattribute1 |ExtensionCustomAttribute1 |
|MSExchExtensionCustomAttribute2 |ExtensionCustomAttribute2 |
|MSExchExtensionCustomAttribute3 |ExtensionCustomAttribute3 |
|MSExchExtensionCustomAttribute4 |ExtensionCustomAttribute4 |
|MSExchExtensionCustomAttribute5 |ExtensionCustomAttribute5 |
|MailNickname |Псевдоним |
|Фисикалделиверйоффиценаме |Office |
|PostalCode |PostalCode |
|ProxyAddresses |EmailAddresses |
|StreetAddress |StreetAddress |
|TargetAddress |ExternalEmailAddress |
|UsageLocation |UsageLocation |
|UserPrincipalName  |UserPrincipalName  |
|Почта   |WindowsEmailAddress    |
|Описание    |Описание    |
|Групп   |Мемберофграуп  |

## <a name="related-topics"></a>Статьи по теме

[Определение политик для барьеров информации в Microsoft Teams (Предварительная версия)](information-barriers-policies.md)

[Препятствия информации об устранении неполадок (Предварительная версия)](information-barriers-troubleshooting.md)

[Препятствия для информационных заданных (Предварительная версия)](information-barriers.md)



