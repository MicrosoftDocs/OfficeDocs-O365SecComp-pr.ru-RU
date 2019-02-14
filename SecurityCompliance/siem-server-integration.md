---
title: Интеграция сервера SIEM с Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- SIEM
- M365-security-compliance
description: 'Сводка: В этой статье Обзор SIEM сервера интеграции с Microsoft 365.'
ms.openlocfilehash: a6e139d14a7ea3625b2d2fffec5ad5d913ea9184
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995200"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a>Интеграция сервера SIEM с Microsoft 365 служб и приложений

## <a name="overview"></a>Обзор

Если ваша организация использует сервер сведений о безопасности и управления событий (SIEM) или планируются к выпуску получение сервер SIEM, вы можете спросить, который будет интеграции с Microsoft 365, включая Office 365 для предприятия. Требуется ли сервер SIEM зависит от множество факторов, например требования к безопасности вашей организации. Microsoft 365 предлагает различные средства безопасности; Тем не менее если вашей организации контента и приложений локально и в облаке (как и в случае гибридного развертывания облака), можно добавить server SIEM для дополнительной защиты. Или, если вашей организации есть требования особенно строгие требования безопасности, которые должны соответствовать, можно добавить SIEM server к используемой среде.

## <a name="siem-server-integration-microsoft-365"></a>Интеграция сервера SIEM Microsoft 365

Сервер SIEM может получать данные из широкого Microsoft 365 служб и приложений. В следующей таблице перечислены несколько Microsoft 365 службы и приложения вместе с SIEM исходные данные сервера и ссылки для получения дополнительных сведений об интеграции сервера SIEM для. 

| Служба Microsoft 365 или приложения | Исходные данные сервера SIEM | Ресурсы для получения дополнительных сведений |
| --- | --- | --- |
| [Office 365 Advanced Threat Protection](office-365-atp.md) <br/>   или   <br/>[Office 365 Threat Intelligence](office-365-ti.md) | Журналы аудита | [SIEM интеграции с Office 365 Threat аналитики и расширенный защиту от угроз](siem-integration-with-office-365-ti.md) |
| [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | Журнал интеграции | [SIEM интеграция с Microsoft Cloud приложения безопасности](https://docs.microsoft.com/cloud-app-security/siem) |
| [Office 365 Cloud App Security](office-365-cas-overview.md) | Журнал интеграции | [Интеграция сервера SIEM с Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md) |
| [Advanced Threat Protection в Защитнике Windows](https://docs.microsoft.com/windows/security/threat-protection/) | Журнал интеграции | [По запросу оповещений в вашей SIEM tools](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| [Центр безопасности для Azure](https://docs.microsoft.com/azure/security-center/security-center-intro) (Защиту от угроз и угроз обнаружения) | Оповещения | [Экспорт данных Azure безопасности для предварительной версии SIEM - конвейер конфигурации-](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [Защита идентификации Azure Active Directory](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | Журналы аудита | [Интеграция журналы аудита Azure Active Directory](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [Аналитика Azure расширенной угроз](https://docs.microsoft.com/azure/security/azure-threat-detection) | Журнал интеграции | [Справочник по журналу ATA SIEM](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a>Должно быть включено ведение журнала аудита

Убедитесь, что включено ведение журнала аудита перед настройкой интеграции сервера SIEM. 

- Для SharePoint Online, OneDrive для бизнеса и Azure Active Directory, [журнал аудита включена в центре соответствия требованиям & безопасности](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).

- Для Exchange Online, [включено ведение журнала аудита с помощью Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).
 
## <a name="see-also"></a>См. также

[Освоение облака и гибридные решения](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[Руководства по лаборатории тестирования для облачных решений](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


