---
title: Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection:
- M365-security-compliance
description: Интеграция Office 365 Advanced Threat protection с Advanced Threat Protection в Защитнике Windows для просмотра подробных сведений об управлении угрозами.
ms.openlocfilehash: 892d04152d6029c48a52d37c6235d45a8ba67b81
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222818"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a>Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows

Если вы являетесь участником группы безопасности Организации, вы можете интегрировать функции Office 365 Advanced Threat Protection и Threat Intelligence с помощью Advanced Threat Protection в Защитнике Windows. Это поможет быстро выяснить, подвержены ли компьютеры пользователям риску при изучении угроз в Office 365. Например, когда интеграция включена, вы сможете увидеть список компьютеров, используемых получателями обнаруженного сообщения электронной почты, а также о том, сколько последних оповещений у этих компьютеров в Advanced Threat Protection в Защитнике Windows.
  
На следующем рисунке показана вкладка " **устройства** ", которая будет отображаться, когда включена интеграция с Advanced Threat Protection в Защитнике Windows: 
  
![Когда пакет ATP для защитника Windows включен, вы можете просмотреть список компьютеров с оповещениями.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
В этом примере видно, что получатели сообщения электронной почты имеют четыре устройства, а одно — оповещение. Если щелкнуть ссылку на устройство, откроется его страница на портале Advanced Threat Protection в Защитнике Windows.
  
## <a name="requirements"></a>Требования

- Ваша организация должна иметь Office 365 Threat Intelligence и пакет ATP для защитника Windows.
    
- Необходимо быть глобальным администратором Office 365 или иметь роль администратора безопасности (например, администратора безопасности), назначенную в [центре &amp; безопасности и соответствия требованиям](https://protection.office.com). (См. [разрешения в центре безопасности &amp; и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md))
    
- Вам необходим доступ к Microsoft Office 365 Threat Intelligence и порталу Advanced Threat Protection в Защитнике Windows.
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a>Интеграция службы анализа угроз Office 365 с помощью пакета ATP для защитника Windows

Интеграция службы контроля угроз Office 365 с помощью Advanced Threat Protection в Защитнике Windows настраивается с помощью центра безопасности Office 365 _Амп_ соответствие требованиям и портала Advanced Threat Protection в Защитнике Windows.
  
1. Как глобальный администратор Office 365 или администратор безопасности перейдите к [https://protection.office.com](https://protection.office.com) рабочей или учебной учетной записи для Office 365 с помощью рабочей или учебной учетной записи. 
    
2. Выберите **Обозреватель** **управления** \> угрозами.<br>![Проводник в меню "Управление угрозами"](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. В правом верхнем углу экрана выберите **Параметры вдатп**.
    
4. В диалоговом окне Подключение ATP для защитника Windows включите параметр подключиться к Windows ATP.<br>![Подключение ATP для защитника Windows](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Включите подключение в Advanced Threat Protection в Защитнике Windows. [Используйте портал Advanced Threat Protection в Защитнике Windows](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Связанные статьи

[Office 365 Threat Intelligence](office-365-ti.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  

