---
title: Интеграция SIEM с Office 365 Threat Intelligence и Advanced Threat protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Интегрируйте сервер SIEM в Организации с помощью Office 365 Threat Intelligence и Advanced Threat protection с помощью API управления действиями Office 365.
ms.openlocfilehash: cecfb3910520ddf535c50bbe4bccbf200ae8e121
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212739"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a><span data-ttu-id="196b1-103">Интеграция SIEM с Office 365 Threat Intelligence и Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="196b1-103">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>

<span data-ttu-id="196b1-p101">Если в организации используется сервер управления инцидентами и событиями SIEM, вы можете интегрировать систему Microsoft Office 365 Threat Intelligence и Advanced Threat protection с сервером SIEM. Интеграция SIEM позволяет просматривать сведения, такие как вредоносные программы, обнаруженные в Office 365 Advanced Protection and Threat Intelligence, в отчетах сервера SIEM. Для настройки интеграции с SIEM используется [API управления действияМи Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="196b1-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence and Advanced Threat Protection with your SIEM server. SIEM integration enables you to view information, such as malware detected by Office 365 Advanced Protection and Threat Intelligence, in your SIEM server reports. To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="196b1-p102">API управления действиями Office 365 извлекает сведения о действиях пользователя, администратора, системы, а также о событиях и политиках из журналов активности Office 365 и Azure Active Directory. [Схема логики Advanced Threat Protection и Threat Protection в Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) работает с логикой системы обмена данными и/или Advanced Threat Protection, поэтому если в организации используется Advanced Threat protection (или наоборот), можно по-прежнему используйте тот же API для интеграции сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="196b1-p102">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs. The [Office 365 Advanced Threat Protection and Threat Intelligence schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Threat Intelligence and/or Advanced Threat Protection, so if your organization has Advanced Threat Protection but not Threat Intelligence (or vice versa), you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="196b1-p103">Сервер SIEM или другая подобная система должны опрашивать события **аудита. Общая** Рабочая нагрузка для доступа к событиям обнаружения. Чтобы узнать больше, ознакомьтесь [со статьей начало работы с API управления Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="196b1-p103">The SIEM server or other similar system should poll the **audit.general** workload to access detection events. To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="196b1-111">Вы должны быть глобальным администратором Office 365 или иметь роль администратора безопасности, назначенную в центре безопасности _Амп_ соответствия требованиям, для настройки интеграции SIEM с Office 365 Advanced Threat protection.</span><span class="sxs-lookup"><span data-stu-id="196b1-111">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="196b1-p104">Для среды Office 365 должна быть включена функция ведения журнала аудита. Чтобы получить помощь, ознакомьтесь со статьей [Включение и отключение поиска в журнале аудита Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="196b1-p104">Audit logging must be turned on for your Office 365 environment. To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="196b1-114">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="196b1-114">Related topics</span></span>

[<span data-ttu-id="196b1-115">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="196b1-115">Office 365 Threat Intelligence</span></span>](office-365-ti.md)

[<span data-ttu-id="196b1-116">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="196b1-116">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="196b1-117">Интеллектуальные отчеты и аналитика в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="196b1-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="196b1-118">Разрешения в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="196b1-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

