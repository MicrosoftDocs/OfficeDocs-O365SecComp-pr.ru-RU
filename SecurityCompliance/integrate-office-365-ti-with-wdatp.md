---
title: Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Интеграция с Windows Защитник расширенного защиту от угроз для просмотра более подробные сведения об управлении угроз защиту от угроз для Office 365 расширенный.
ms.openlocfilehash: e5070e003972ae5308415dcdcca85b069d1163ac
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29382542"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows

Если вы являетесь участником группы безопасности вашей организации, можно интегрировать функции защиты расширенного Threat Office 365 и анализ угроз с защитой расширенного Защитника Windows. Это может помочь быстро понимать, если компьютеров пользователей в группу риска при изучении угрозы безопасности в Office 365. Например после включения интеграции вы сможете также увидеть список компьютеров, используемых получателей сообщения электронной почты вредоносным, как количество оповещений компьютеры, имеют в защиту от угроз дополнительные Защитника Windows.
  
На следующем рисунке показана вкладка **устройств** , что вы увидите, когда у интеграция защиту от угроз дополнительные Защитник Windows включена: 
  
![При включении анализа Защитник Windows можно просмотреть список компьютеров с оповещениями.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
В этом примере видно, что получателей сообщения электронной почты при наличии четырех устройств и один список имеет соответствующее оповещение. Щелкнув ссылку для устройства открывает ее страницу на портале защиту от угроз дополнительные Защитника Windows.
  
## <a name="requirements"></a>Требования

- Вашей организации должны иметь анализ угроз Office 365 и анализа Защитника Windows.
    
- Необходимо быть глобального администратора Office 365 или роль администратора безопасности (например, администратор безопасности) в [безопасности &amp; центре соответствия требованиям](https://protection.office.com). (Увидеть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md))
    
- Необходимо иметь доступ к анализ угроз Office 365 и портала защиту от угроз дополнительные Защитника Windows.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Чтобы интегрировать анализ угроз Office 365 с ATP Защитника Windows

Интеграция анализ угроз Office 365 с защитой расширенного Защитник Windows настраивается с помощью обоих безопасности Office 365 & центра соответствия требованиям и портала защиту от угроз дополнительные Защитника Windows.
  
1. Как глобальный администратор Office 365 или администратор безопасности, перейдите к [https://protection.office.com](https://protection.office.com) и войдите с работы или школы учетную запись на Office 365. 
    
2. Выберите **Threat management** \> **Explorer**.<br>![Explorer в меню Threat Management](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. В правом верхнем углу экрана выберите **Параметры WDATP**.
    
4. В диалоговом окне подключения к ATP Защитник Windows преобразовать на подключение к Windows ATP.<br>![Подключение ATP Защитника Windows](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Разрешить подключения в защиту от угроз дополнительные Защитника Windows. Показано [Использование портала защиту от угроз дополнительные Защитника Windows](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Статьи по теме

[Office 365 Threat Intelligence](office-365-ti.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  

