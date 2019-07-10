---
title: Разрешения на функции в службе EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 1/30/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 34674847-a6b7-4a7e-9eaa-b64f22bc150d
description: Разрешения, необходимые для выполнения задач по управлению службой Microsoft Exchange Online Protection (EOP), зависят от управляемых функций.
ms.openlocfilehash: 02c27609ef39ce971db2c555d6a345e94e98f470
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599685"
---
# <a name="feature-permissions-in-eop"></a>Разрешения на функции в службе EOP

Разрешения, необходимые для выполнения задач по управлению службой Microsoft Exchange Online Protection (EOP), зависят от управляемых функций. 
  
Для настройки EOP ваша ученая запись должна обладать правами глобального администратора Office 365 или администратора компании Exchange (группа ролей управления организацией).
  
## <a name="exchange-online-protection-permissions"></a>Разрешения Exchange Online Protection

Чтобы узнать, какие нужны разрешения для управления функциями EOP, обратитесь к таблице ниже. Если для функции указано несколько групп ролей, то для ее использования достаточно относиться к одной из этих групп.
  
|**Функция**|**Необходимые разрешения**|
|:-----|:-----|
|Функции защиты от вредоносных программ  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Управление санацией](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Защита от нежелательной почты  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Управление санацией](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Правила потока обработки почты  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Records Management](http://technet.microsoft.com/library/0e0c95ce-6109-4591-b86d-c6cfd44d21f5.aspx) <br/> |
|Домены  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> |
|Advanced Threat protection (ATP)  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [Управление санацией](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Соединители Office 365  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> |
|Трассировка сообщений  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> |
|Конфигурация организации  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> |
|Карантин  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Пользователи, контакты и группы ролей  <br/> |[Управление организацией](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Группы рассылки и группы безопасности  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx) <br/> [View-Only Organization Management](http://technet.microsoft.com/library/c514c6d0-0157-4c52-9ec6-441d9a30f3df.aspx) <br/> [Hygiene Management](http://technet.microsoft.com/library/fc0a9ec2-9c3d-42f6-8442-8603fb29d464.aspx) <br/> |
|Просмотр отчетов  <br/> |[Organization Management](http://technet.microsoft.com/library/0bfd21c1-86ac-4369-86b7-aeba386741c8.aspx)  у пользователей есть доступ к отчетам по защите электронной почты.  <br/> [View-Only Recipients](http://technet.microsoft.com/library/37e66b92-81d3-412f-b7a9-e1bb8cbeb468.aspx)  у пользователей есть доступ к отчетам о защите почты.  <br/> [Compliance Management](http://technet.microsoft.com/library/b91b23a4-e9c7-4bd0-9ee3-ec5cb498da15.aspx)  у пользователей есть доступ к отчетам по защите электронной почты и отчетам защиты от потери данных (DLP) (если их подписка поддерживает возможности DLP).  <br/> |
   

