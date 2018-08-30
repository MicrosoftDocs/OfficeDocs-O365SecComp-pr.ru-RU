---
title: Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Интеграция с Windows Защитник расширенного защиту от угроз для просмотра более подробные сведения об управлении угроз защиту от угроз для Office 365 расширенный.
ms.openlocfilehash: 574594d5881853b268713e0bb74444ae80ffcf46
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534556"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows

Если вы являетесь участником группы безопасности вашей организации, можно интегрировать Office 365 с помощью Windows Защитник расширенного угроз защиты анализа. Это может помочь быстро понимать, если компьютеров пользователей в группу риска при изучении угрозы безопасности в Office 365. Например после включения интеграции вы сможете для просмотра списка компьютеров, используемых получателей сообщения электронной почты вредоносным, а также как количество оповещений компьютеры, имеют в ATP Защитника Windows.
  
На следующем рисунке показана вкладка **устройств** , что вы увидите, когда у интеграция ATP Защитник Windows включена: 
  
![При включении анализа Защитник Windows можно просмотреть список компьютеров с оповещениями.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
В этом примере видно, что получателей сообщения электронной почты имеют четыре компьютера и одно оповещение в ATP Защитника Windows. Щелкнув ссылку на компьютер открывает страницу компьютера в ATP Защитника Windows в новую вкладку.
  
## <a name="requirements"></a>Требования

- Вашей организации должны иметь анализ угроз Office 365 и анализа Защитника Windows.
    
- Необходимо быть глобального администратора Office 365 или роль администратора безопасности, назначенные в системы &amp; центре соответствия требованиям. (Увидеть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md))
    
- Необходимо иметь доступ к анализ угроз Office 365 и портала ATP Защитника Windows.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Чтобы интегрировать анализ угроз Office 365 с ATP Защитника Windows

Интеграция анализ угроз Office 365 с ATP Защитник Windows настроена в Office 365 и на портале ATP Защитника Windows.
  
1. Как глобальный Office 365 или администратор безопасности, перейдите к [https://portal.office.com](https://portal.office.com) и войдите с работы или школы учетную запись на Office 365. 
    
2. Выберите **Threat management** \> **explorer угроз**.
    
3. В меню **Дополнительные** выберите **Параметры WDATP**.
    
4. Выберите **подключение к Windows анализа**.
    
После изменения параметров в Office 365, необходимо включить подключение от ATP Защитника Windows. Для этого показано [Использование портала защиту от угроз дополнительные Защитника Windows](https://go.microsoft.com/fwlink/?linkid=859690).
  
## <a name="related-topics"></a>Статьи по теме

[Office 365 Threat Intelligence](office-365-ti.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  

