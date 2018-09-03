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
ms.openlocfilehash: 40c84b9d7b7ec4c9b15383e3ffbbabf839294def
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782146"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a><span data-ttu-id="45e8b-103">SIEM интеграции с Office 365 Threat аналитики и расширенный защиту от угроз</span><span class="sxs-lookup"><span data-stu-id="45e8b-103">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>

<span data-ttu-id="45e8b-p101">Если ваша организация использует сервер безопасности происшествия и события управления (SIEM), можно интегрировать с сервером SIEM анализ угроз Office 365 и расширенный защиту от угроз. Интеграция SIEM позволяет просматривать сведения, такие как вредоносных программ, обнаруженных с Office 365 расширенного защиты и анализ угроз в отчетах сервера SIEM. Чтобы настроить интеграцию SIEM, используйте [API управления Office 365 активности](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="45e8b-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence and Advanced Threat Protection with your SIEM server. SIEM integration enables you to view information, such as malware detected by Office 365 Advanced Protection and Threat Intelligence, in your SIEM server reports. To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="45e8b-p102">API для управления Office 365 активности извлекаются сведения о пользователя, администрирования, система и действия в рамках политики и события из вашей организации Office 365 и Azure Active Directory ведение журнала. [Защита расширенного Threat Office 365 и анализ угроз схемы](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) для работы с анализ угроз и/или дополнительные защиту от угроз, если вашей организации есть дополнительные защиту от угроз, кроме не анализ угроз (и наоборот), вы можете по-прежнему используйте тот же API для интеграции сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="45e8b-p102">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs. The [Office 365 Advanced Threat Protection and Threat Intelligence schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Threat Intelligence and/or Advanced Threat Protection, so if your organization has Advanced Threat Protection but not Threat Intelligence (or vice versa), you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="45e8b-p103">Сервер SIEM или другие аналогичные системы период опроса **audit.general** нагрузку на события обнаружения доступа. Чтобы узнать больше видеть, [Начало работы с API -интерфейсы управления Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="45e8b-p103">The SIEM server or other similar system should poll the **audit.general** workload to access detection events. To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="45e8b-111">Необходимо иметь права глобального администратора Office 365 или роль администратора безопасности, назначенные в центр соответствия требованиям и безопасности для настройки SIEM интеграции с Office 365 Threat аналитики и расширенный защиту от угроз.</span><span class="sxs-lookup"><span data-stu-id="45e8b-111">You must be an Office 365 global administrator or have the security administrator role assigned in the Security & Compliance Center to set up SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection.</span></span></br><span data-ttu-id="45e8b-p104">Ведение журнала аудита может быть включена для вашей среды Office 365. Чтобы получить справку, обратитесь к разделу [Включить Office 365 проводить аудит операций поиска журнала включено или отключено](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="45e8b-p104">Audit logging must be turned on for your Office 365 environment. To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45e8b-114">Смежные темы</span><span class="sxs-lookup"><span data-stu-id="45e8b-114">Related topics</span></span>

[<span data-ttu-id="45e8b-115">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="45e8b-115">Office 365 Threat Intelligence</span></span>](office-365-ti.md)

[<span data-ttu-id="45e8b-116">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="45e8b-116">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="45e8b-117">Смарт-отчеты и полезные сведения о безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="45e8b-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="45e8b-118">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="45e8b-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

