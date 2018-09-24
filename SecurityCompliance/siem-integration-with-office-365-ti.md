---
title: SIEM интеграции с Office 365 Threat аналитики и расширенный защиту от угроз
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Интеграция с анализ угроз Office 365 и расширенный защиту от угроз с API для управления Office 365 активности сервера SIEM вашей организации.
ms.openlocfilehash: 057d8ac101b96f37846ac751645934279d45dc88
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972261"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>SIEM интеграции с Office 365 Threat аналитики и расширенный защиту от угроз

Если ваша организация использует сервер безопасности происшествия и события управления (SIEM), можно интегрировать с сервером SIEM анализ угроз Office 365 и расширенный защиту от угроз. Интеграция SIEM позволяет просматривать сведения, такие как вредоносных программ, обнаруженных с Office 365 расширенного защиты и анализ угроз в отчетах сервера SIEM. Чтобы настроить интеграцию SIEM, используйте [API управления Office 365 активности](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

API для управления Office 365 активности извлекаются сведения о пользователя, администрирования, система и действия в рамках политики и события из вашей организации Office 365 и Azure Active Directory ведение журнала. [Защита расширенного Threat Office 365 и анализ угроз схемы](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) для работы с анализ угроз и/или дополнительные защиту от угроз, если вашей организации есть дополнительные защиту от угроз, кроме не анализ угроз (и наоборот), вы можете по-прежнему используйте тот же API для интеграции сервера SIEM. 

Сервер SIEM или другие аналогичные системы период опроса **audit.general** нагрузку на события обнаружения доступа. Чтобы узнать больше видеть, [Начало работы с API -интерфейсы управления Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). 

> [!IMPORTANT]
> Необходимо иметь права глобального администратора Office 365 или роль администратора безопасности, назначенные в центр соответствия требованиям и безопасности для настройки SIEM интеграции с Office 365 Threat аналитики и расширенный защиту от угроз.<br/>Ведение журнала аудита может быть включена для вашей среды Office 365. Чтобы получить справку, обратитесь к разделу [Включить Office 365 проводить аудит операций поиска журнала включено или отключено](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Смежные темы

[Office 365 Threat Intelligence](office-365-ti.md)

[Office 365 Advanced Threat Protection](office-365-atp.md)

[Смарт-отчеты и полезные сведения о безопасности Office 365 &amp; центре соответствия требованиям](reports-and-insights-in-security-and-compliance.md)
  
[Разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md)
  

