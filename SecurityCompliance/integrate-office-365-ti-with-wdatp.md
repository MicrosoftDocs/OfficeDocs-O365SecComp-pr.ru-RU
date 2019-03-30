---
title: Интеграция Office 365 Advanced Threat protection с Advanced Threat Protection в Защитнике Windows
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
ms.openlocfilehash: 832b9c6bc600366e1ed6b7c6e60442bec8b5002c
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998962"
---
# <a name="integrate-office-365-advanced-threat-protection-with-windows-defender-advanced-threat-protection"></a>Интеграция Office 365 Advanced Threat protection с Advanced Threat Protection в Защитнике Windows

Если вы участвуете в группе безопасности Организации, вы можете интегрировать Office 365 Advanced Threat Protection и соответствующие функции расследования и ответа с помощью Advanced Threat Protection в Защитнике Windows. Это поможет быстро выяснить, подвержены ли компьютеры пользователям риску при изучении угроз в Office 365. Например, когда интеграция включена, вы сможете увидеть список компьютеров, используемых получателями обнаруженного сообщения электронной почты, а также о том, сколько последних оповещений у этих компьютеров в Advanced Threat Protection в Защитнике Windows.
  
На следующем рисунке показана вкладка " **устройства** ", которая будет отображаться, когда включена интеграция с Advanced Threat Protection в Защитнике Windows: 
  
![Когда пакет ATP для защитника Windows включен, вы можете просмотреть список компьютеров с оповещениями.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
В этом примере видно, что получатели сообщения электронной почты имеют четыре устройства, а одно — оповещение. Если щелкнуть ссылку на устройство, откроется его страница на портале Advanced Threat Protection в Защитнике Windows.
  
## <a name="requirements"></a>Требования

- В вашей организации должен быть Office 365 Advanced Threat Protection Plan 2 (или Office 365 в) и пакет ATP для защитника Windows.
    
- Необходимо быть глобальным администратором Office 365 или иметь роль администратора безопасности (например, администратора безопасности), назначенную в [центре &amp; безопасности и соответствия требованиям](https://protection.office.com). (См. [разрешения в центре безопасности &amp; и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md))
    
- У вас должен быть доступ к проводнику угроз Office 365 в центре безопасности _Амп_ соответствие требованиям и портале Advanced Threat Protection в Защитнике Windows.
    
## <a name="to-integrate-office-365-advanced-threat-protection-with-windows-defender-atp"></a>Интеграция Office 365 Advanced Threat protection с помощью пакета ATP для защитника Windows

Интеграция Office 365 Advanced Threat protection с помощью Advanced Threat Protection в Защитнике Windows настраивается с помощью центра безопасности _Амп_ соответствие требованиям и портала Advanced Threat Protection в Защитнике Windows.
  
1. Как глобальный администратор Office 365 или администратор безопасности перейдите к [https://protection.office.com](https://protection.office.com) рабочей или учебной учетной записи для Office 365 с помощью рабочей или учебной учетной записи. 
    
2. Выберите **Обозреватель** **управления** \> угрозами.<br>![Проводник в меню "Управление угрозами"](media/ThreatMgmt-Explorer-nav.png)<br>
    
3. В правом верхнем углу экрана выберите **Параметры вдатп**.
    
4. В диалоговом окне Подключение ATP для защитника Windows включите параметр подключиться к Windows ATP.<br>![Подключение ATP для защитника Windows](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. Включите подключение в Advanced Threat Protection в Защитнике Windows. [Используйте портал Advanced Threat Protection в Защитнике Windows](https://go.microsoft.com/fwlink/?linkid=859690).

  
## <a name="related-topics"></a>Статьи по теме

[Исследование угроз для Office 365 и ответ на них](office-365-ti.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  

