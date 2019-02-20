---
title: Интеграция SIEM с Office 365 Threat Intelligence и Advanced Threat protection
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
description: Интегрируйте сервер SIEM в Организации с помощью Office 365 Threat Intelligence и Advanced Threat protection с помощью API управления действиями Office 365.
ms.openlocfilehash: 854f763b72dfac1a5dc1442b1d9d123ed5439257
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087248"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>Интеграция SIEM с Office 365 Threat Intelligence и Advanced Threat protection

Если в организации используется сервер управления инцидентами и событиями SIEM, вы можете интегрировать систему Microsoft Office 365 Threat Intelligence и Advanced Threat protection с сервером SIEM. Интеграция SIEM позволяет просматривать сведения, такие как вредоносные программы, обнаруженные в Office 365 Advanced Protection and Threat Intelligence, в отчетах сервера SIEM. Для настройки интеграции с SIEM используется [API управления действияМи Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

API управления действиями Office 365 извлекает сведения о действиях пользователя, администратора, системы, а также о событиях и политиках из журналов активности Office 365 и Azure Active Directory. [Схема логики Advanced Threat Protection и Threat Protection в Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) работает с логикой системы обмена данными и/или Advanced Threat Protection, поэтому если в организации используется Advanced Threat protection (или наоборот), можно по-прежнему используйте тот же API для интеграции сервера SIEM. 

Сервер SIEM или другая подобная система должны опрашивать события **аудита. Общая** Рабочая нагрузка для доступа к событиям обнаружения. Чтобы узнать больше, ознакомьтесь [со статьей начало работы с API управления Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). 

> [!IMPORTANT]
> Вы должны быть глобальным администратором Office 365 или иметь роль администратора безопасности, назначенную в центре безопасности _Амп_ соответствия требованиям, для настройки интеграции SIEM с Office 365 Advanced Threat protection.<br/>Для среды Office 365 должна быть включена функция ведения журнала аудита. Чтобы получить помощь, ознакомьтесь со статьей [Включение и отключение поиска в журнале аудита Office 365](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Связанные статьи

[Office 365 Threat Intelligence](office-365-ti.md)

[Office 365 Advanced Threat Protection](office-365-atp.md)

[Интеллектуальные отчеты и аналитика в центре безопасности &amp; и соответствия требованиям Office 365](reports-and-insights-in-security-and-compliance.md)
  
[Разрешения в центре безопасности &amp; и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md)
  

