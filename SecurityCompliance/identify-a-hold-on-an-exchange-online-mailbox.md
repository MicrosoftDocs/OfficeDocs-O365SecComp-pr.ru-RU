---
title: Как определить тип удержания, примененного для почтового ящика Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6057daa8-6372-4e77-a636-7ea599a76128
ms.openlocfilehash: d24e51bca0e3d290f110b1ab40f3ee9ae7993678
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535113"
---
# <a name="how-to-identify-the-type-of-hold-placed-on-an-exchange-online-mailbox"></a>Как определить тип удержания, примененного для почтового ящика Exchange Online

В этой статье объясняется, как определить удержаний, помещенные на почтовые ящики Exchange Online в Office 365.

Office 365 предлагает несколько способов организации можно предотвратить без возможности восстановления удаление содержимого почтового ящика. Это позволяет сохранять содержимое в соответствии с обычные соответствия требованиям вашей организации или во время выполнения, требованиям законодательства или других типов расследований. Ниже приведен список возможностей хранения (также называемое удержаний) в Office 365:

- **Хранение для судебного разбирательства** - удержаний, которые применяются к почтовым ящикам пользователей в Exchange Online.

- **хранение электронных данных** - удержаний, связанные с вариантом eDiscovery в центр соответствия требованиям и безопасности. Удержание электронных данных может быть применена к почтовым ящикам пользователей и соответствующего почтового ящика для группы Office 365 и Microsoft рабочих групп.

- **Хранение на месте** - удержаний, которые применяются к почтовым ящикам пользователей с помощью электронного обнаружения на месте и удержания средство в Exchange admin центра в Exchange Online.

- **Политика хранения office 365** — сохраняет контента в пользовательских почтовых ящиков в Exchange Online и в соответствующий почтовый ящик для группы Office 365 и Microsoft рабочих групп. Можно создать удержание политики сохраняет Скайп для бизнеса бесед, которые хранятся в почтовые ящики пользователей.

  Существует два типа политик хранения Office 365, которые могут быть назначены почтовые ящики.

    - **Политики хранения определенное расположение** — это политик, назначенных для размещения содержимого определенных пользователей. Используйте командлет Get-Mailbox в Exchange Online PowerShell для получения сведений о политики хранения, назначенные для определенных почтовых ящиков.

    - **Политики хранения всей организации** — это, политики, которые были им назначены все расположения контента в вашей организации. Используйте командлет Get-OrganizationConfig в Exchange Online PowerShell для получения сведений о политиках хранения всей организации. Для получения дополнительных сведений обратитесь к разделу «Применение политики хранения для всей организации или определенные расположения» в политики хранения Обзор Office 365.

Для управления почтовыми ящиками на удержание, необходимо определить тип удержания, которое размещается на почтовый ящик, чтобы можно было выполнять задачи, такие как изменение продолжительность удержания, временно или постоянно удаление удержание или исключение почтового ящика из политики хранения Office 365. В таких случаях первый шаг — это позволяет определить тип удержания, помещенные на почтовый ящик. И так как несколько удержаний (и различных типов удержаний) могут размещаться на одного почтового ящика, вам придется для идентификации всех удержаний, помещенные на почтовый ящик, если вы хотите удалить или изменить этих удержаний.

## <a name="step-1-obtaining-the-guid-for-holds-placed-on-a-mailbox"></a>Шаг 1: Получение идентификатор GUID для удержаний помещенных на почтовый ящик

Следующие два командлеты можно запустить в Exchange Online PowerShell, чтобы получить GUID удержаний, помещенные на почтовый ящик. После получения идентификатора GUID используется для определения конкретного удержания в шаге 2. Обратите внимание на то, что Судебное удержание, не идентифицируются идентификатором GUID. Хранение для судебного удержания либо включены или отключены для почтового ящика.

- **Get-Mailbox** - используйте этот командлет для определения, включено ли хранение для судебного разбирательства для почтового ящика и получение идентификатора GUID для обнаружения электронных данных содержит, удержание на месте и политик хранения Office 365, в частности назначенных почтовому ящику. Вывод командлета будет также указать, если почтовый ящик был явно исключен из политику хранения всей организации.

- **Get-OrganizationConfig** - используйте этот командлет, чтобы получить идентификаторы GUID для политики хранения всей организации.

Чтобы подключиться к Exchange Online PowerShell, обратитесь к разделу [подключение к Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).

### <a name="get-mailbox"></a>Get-Mailbox

Выполните следующую команду для получения сведений об удержаниях и политик хранения Office 365, применяемых к почтовому ящику.

```
Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
```

> [!TIP]
> Если в свойстве InPlaceHolds слишком много значений, и не все из них отображаются, можно выполнить `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` команду, чтобы отобразить каждый идентификатор GUID в отдельной строке.

В следующей таблице описаны способы идентификации различных типов удержаний на основе значений в свойстве *InPlaceHolds* при запуске командлета **Get-Mailbox** .


|Тип удержания  |Пример значения  |Как определить удержания  |
|---------|---------|---------|
|Хранение для судебного разбирательства     |    `True`     |     Хранение для судебного разбирательства включен для почтового ящика, если свойство *LitigationHoldEnabled* имеет значение `True`.    |
|Удержание электронных данных     |  `UniH7d895d48-7e23-4a8d-8346-533c3beac15d`       |   *Свойство InPlaceHolds* содержит идентификатор GUID для любого удержания, связанные с вариантом eDiscovery в центр соответствия требованиям и безопасности. Чтобы узнать, это удержание электронных данных, так как код GUID начинается с `UniH` префикс (который обозначает единой хранения).      |
|Хранение на месте     |     `c0ba3ce811b6432a8751430937152491` <br/> или <br/> `cld9c0a984ca74b457fbe4504bf7d3e00de`  |     Свойство *InPlaceHolds* содержит идентификатор GUID режима сохранения, помещенные на почтовый ящик. Чтобы узнать, это хранение на месте, так как код GUID не начинается с префикса или начинается с `cld` префикса.     |
|Политика хранения Office 365, в частности применяется к почтовому ящику     |    `mbxcdbbb86ce60342489bff371876e7f224:1` <br/> или <br/> `skp127d7cf1076947929bf136b7a2a8c36f:3`     |     Свойство InPlaceHolds содержит GUID политики хранения любого заданного расположения, которая применяется к почтовому ящику. Можно определить политики хранения, так как код GUID начинается с `mbx` или `skp` префикса. `skp` Префикс указывает, что политика хранения применяется к Скайп для бизнеса бесед в почтовый ящик пользователя.    |
|Исключить из политики хранения всей организации Office 365     |   `-mbxe9b52bf7ab3b46a286308ecb29624696`      |     Если почтовый ящик исключены из политики хранения всей организации Office 365, идентификатор GUID для почтового ящика исключается из политики хранения отображаемое в свойстве InPlaceHolds и отмечаются `-mbx` префикса.    |

### <a name="get-organizationconfig"></a>Get-OrganizationConfig
Если свойство *InPlaceHolds* пустое при запуске командлета **Get-Mailbox** , по-прежнему могут существовать один или несколько всей организации Office 365 политики хранения применяется к почтовому ящику. Выполните следующую команду в Exchange Online PowerShell, чтобы получить список идентификаторов GUID для политики хранения всей организации Office 365.

```
Get-OrganizationConfig | FL InPlaceHolds
```

> [!TIP]
> Если в свойстве InPlaceHolds слишком много значений, и не все из них отображаются, можно выполнить `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` команду, чтобы отобразить каждый идентификатор GUID в отдельной строке.

В следующей таблице описаны различные типы удержаний всей организации, а также для идентификации каждого типа на основании идентификаторы GUID, содержащихся в свойстве *InPlaceHolds* при запуске командлета **Get-OrganizationConfig** .


|Тип удержания  |Пример значения  |Описание  |
|---------|---------|---------|
|Office 365 хранения политики применены к почтовые ящики Exchange, общих папок Exchange или группам чаты    |      `mbx7cfb30345d454ac0a989ab3041051209:2`   |   Политики хранения всей организации применяются к почтовым ящикам Exchange, общие папки Exchange и чаты 1xN в группах Microsoft идентифицируются по GUID, начинающиеся со `mbx` префикса. Обратите внимание на то, что 1xN чаты хранятся в почтовом ящике отдельных чата участникам.      |
|Office 365 хранения политики, применяемые к сообщениям, канал группы Office 365 и рабочих групп     |   `grp1a0a132ee8944501a4bb6a452ec31171:3`      |    Политики хранения всей организации, применяемые к группам Office 365 и сообщения в группах Microsoft идентифицируются по GUID, начинающиеся со `grp` префикса. Обратите внимание на то, что сообщения хранятся в почтовом ящике группы, связанный с группы разработчиков Microsoft.     |

Дополнительные политики хранения сведения, применяемые к группам Майкрософт содержатся в разделе» Расположение команды « [Обзор политик хранения](retention-policies.md#applying-a-retention-policy-to-an-entire-organization-or-specific-locations).

### <a name="understanding-the-format-of-the-inplaceholds-value-for-retention-policies"></a>Общие сведения о формате значение InPlaceHolds для политики хранения

В дополнение к префикс (mbx, skp или группу), идентифицирующее элемент в свойство InPlaceHolds как политики хранения к Office 365 значение также содержит суффикс, идентифицирующий тип действия хранения, настроенной для политики. Например суффикс действие выделяется полужирным шрифтом в следующих примерах:

   `skp127d7cf1076947929bf136b7a2a8c36f`**: 1**

   `mbx7cfb30345d454ac0a989ab3041051209`**: 2**

   `grp1a0a132ee8944501a4bb6a452ec31171`**: 3**

В следующей таблице приведены три возможных хранения действия:

|Значение  |Описание  |
|---------|---------|
|**1**     | Указывает, что политика хранения настроена для удаления элементов; политика не сохраняет элементов.        |
|**2**    |    Указывает, что политика хранения настроена для хранения элементов; политика не удаляет элементы, по истечении срока хранения.     |
|**3**     |   Указывает, что политика хранения, настроенная для хранения элементов и удалять их по истечении срока хранения.      |

Дополнительные сведения о действиях хранения обратитесь к разделу «Сохранение содержимого в течение определенного периода времени» в статье [Overview of политики хранения](retention-policies.md#retaining-content-for-a-specific-period-of-time).
   
## <a name="step-2-using-the-guid-to-identify-the-hold"></a>Шаг 2: Использование GUID для обнаружения удержания

После получения идентификатора GUID для удержания, применяемый к почтовому ящику, следующим шагом является используйте этот идентификатор GUID для идентификации удержания. Приведенные ниже показано, как определить имя удержания (и другие сведения) с помощью удержания GUID.

### <a name="ediscovery-holds"></a>содержит eDiscovery

Выполните следующие команды в безопасности & PowerShell центр соответствия требованиям для идентификации удержание электронных данных, которая применяется к почтовому ящику. Идентификатор GUID (не включая префикс UniH) для обнаружения электронных данных разбирательства был определен на шаге 1. Первая команда создает переменную, которая содержит сведения об удержании; Эта переменная используется в другие команды. Вторая команда отображает имя случая обнаружения электронных данных, связанного с удержания. Третий команда отображает имени удержания и список почтовых ящиков, которой применяется удержания.

```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold | FL Name,ExchangeLocation
```

Чтобы подключиться к безопасности и соответствия требованиям центр PowerShell, обратитесь к разделу [подключение к Office 365 безопасность и соответствие требованиям центр PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

### <a name="in-place-holds"></a>Хранение на месте

Выполните следующую команду в Exchange Online PowerShell для идентификации хранение на месте, которая применяется к почтовому ящику. Используйте идентификатор GUID для хранения на месте, который был определен на шаге 1. Команда отображает имени удержания и список почтовых ящиков, которой применяется удержания.

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name,SourceMailboxes
```
Обратите внимание, если идентификатор GUID для хранения на месте начинается с `cld` префиксов, обязательно включите префикс при выполнении предыдущей команды.

### <a name="office-365-retention-policies"></a>Политики хранения Office 365

Выполните следующую команду в безопасности и соответствия требованиям центр PowerShell удостоверения политики хранения Office 365 (всей организации или определенного расположения), которая применяется к почтовому ящику. Используйте идентификатор GUID (не включая префикс mbx, skp или группу или суффикс действие), который был определен на шаге 1.

```
Get-RetentionCompliancePolicy <hold GUID without prefix or suffix> -DistributionDetail  | FL Name,*Location
```

## <a name="next-steps"></a>Дальнейшие действия

После определения удержаний, которые применяются к почтовому ящику может выполнять задачи, такие как изменить продолжительность удержания, временно или окончательно удалить удержание или в случае политики хранения Office 365, за исключением неактивного почтового ящика из политики. Дополнительные сведения о выполнении задачи, связанные с удержаний можно один из следующих разделов:

- Запустите [Set RetentionCompliancePolicy - AddExchangeLocationException \<почтовый ящик пользователя >](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-retention/Set-RetentionCompliancePolicy?view=exchange-ps) в безопасности & PowerShell центр соответствия исключать почтового ящика из политики хранения всей организации Office 365. Обратите внимание на то, что эта команда может использоваться только для политик хранения которых значение свойства *ExchangeLocation* равняется `All`.

- Запустите [Set-Mailbox - ExcludeFromOrgHolds \<хранение GUID без префикса или суффикса >](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox?view=exchange-ps) в Exchange Online PowerShell, чтобы исключить неактивного почтового ящика из политики хранения всей организации Office 365.

- [Изменить продолжительность удержания для неактивного почтового ящика в Office 365](change-the-hold-duration-for-an-inactive-mailbox.md)

- [Удаление неактивного почтового ящика в Office 365](delete-an-inactive-mailbox.md)

- [Удаление элементов в папке "Элементы с возможностью восстановления" облачных почтовых ящиков на удержании](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md)