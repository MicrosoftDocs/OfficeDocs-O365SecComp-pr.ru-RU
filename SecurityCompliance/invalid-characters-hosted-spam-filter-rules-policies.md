---
title: Избегайте недопустимые символы в вашей правил фильтрации нежелательной почты и политики фильтрации нежелательной почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Содержит справочную информацию для администраторов, которые имеют недопустимые символы в их конфигурации защиты от нежелательной почты и работе возникли проблемы при попытке использовать безопасности &amp; центре соответствия требованиям.
ms.openlocfilehash: ca409b4daa7bec01417adb7cbfdfa2a128929e81
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018738"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a>Избегайте недопустимые символы в правилах фильтра нежелательной почты и политики фильтрации нежелательной почты 

Ранее Office 365 для администраторов и настроив правил фильтрации нежелательной почты и политики фильтрации нежелательной почты с помощью центра администрирования Exchange (EAC). Теперь, используйте безопасности &amp; центре соответствия требованиям для управления конфигурации защиты от нежелательной почты. Следующие символы поддерживаются в центре администрирования Exchange, но не поддерживаются для использования в безопасности &amp; центре соответствия требованиям.  

**Недопустимые символы:**
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

Если ваше правил фильтрации нежелательной почты или политики фильтрации нежелательной почты содержит недопустимые символы, может появиться некоторые или все следующие проблемы:
- Не удается найти политики или правил в системы &amp; центре соответствия требованиям.
- Вы можете получить ошибки при попытке получить правила или политики с помощью Windows PowerShell.
- Может оказаться, что политики или параметры не запустите или как ожидалось.

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a>Удалить недопустимые символы из политики фильтрации нежелательной почты и правила

После определения политики и правила, которые содержат недопустимые символы, можно изменить имена с помощью командлетов Windows PowerShell. 

1. [Подключение к Exchange Online с помощью удаленной оболочки PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Чтобы изменить имя политики фильтрации нежелательной почты, выполните командлет Set-HostedContentFilterPolicy следующим образом:
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. Чтобы изменить имя правила фильтрации нежелательной почты, выполните командлет Set-HostedContentFilterRule следующим образом:
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a>Дополнительные сведения

[Угроз управления в системы &amp; центре соответствия требованиям](threat-management.md)
  
[SET-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[SET-HostedContentFilterRule](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
