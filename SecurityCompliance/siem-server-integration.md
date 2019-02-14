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
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="256c7-103">Интеграция сервера SIEM с Microsoft 365 служб и приложений</span><span class="sxs-lookup"><span data-stu-id="256c7-103">SIEM server integration with Microsoft 365 services and applications</span></span>

## <a name="overview"></a><span data-ttu-id="256c7-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="256c7-104">Overview</span></span>

<span data-ttu-id="256c7-p101">Если ваша организация использует сервер сведений о безопасности и управления событий (SIEM) или планируются к выпуску получение сервер SIEM, вы можете спросить, который будет интеграции с Microsoft 365, включая Office 365 для предприятия. Требуется ли сервер SIEM зависит от множество факторов, например требования к безопасности вашей организации. Microsoft 365 предлагает различные средства безопасности; Тем не менее если вашей организации контента и приложений локально и в облаке (как и в случае гибридного развертывания облака), можно добавить server SIEM для дополнительной защиты. Или, если вашей организации есть требования особенно строгие требования безопасности, которые должны соответствовать, можно добавить SIEM server к используемой среде.</span><span class="sxs-lookup"><span data-stu-id="256c7-p101">If your organization is using a Security Information and Event Management (SIEM) server, or if you are planning to get a SIEM server soon, you might be wondering how that'll integrate with your Microsoft 365, including Office 365 Enterprise. Whether you need a SIEM server depends on many factors, such as your organization's security requirements. Microsoft 365 offers a variety of security features; however, if your organization has content and applications on premises and in the cloud (as in the case of a hybrid cloud deployment), you might consider adding a SIEM server for extra protection. Or, if your organization has particularly stringent security requirements you must meet, you might consider adding a SIEM server to your environment.</span></span>

## <a name="siem-server-integration-microsoft-365"></a><span data-ttu-id="256c7-109">Интеграция сервера SIEM Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="256c7-109">SIEM server integration Microsoft 365</span></span>

<span data-ttu-id="256c7-p102">Сервер SIEM может получать данные из широкого Microsoft 365 служб и приложений. В следующей таблице перечислены несколько Microsoft 365 службы и приложения вместе с SIEM исходные данные сервера и ссылки для получения дополнительных сведений об интеграции сервера SIEM для.</span><span class="sxs-lookup"><span data-stu-id="256c7-p102">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications. The following table lists several Microsoft 365 services and applications along with SIEM server inputs and where to go to learn more about SIEM server integration.</span></span> 

| <span data-ttu-id="256c7-112">Служба Microsoft 365 или приложения</span><span class="sxs-lookup"><span data-stu-id="256c7-112">Microsoft 365 Service or Application</span></span> | <span data-ttu-id="256c7-113">Исходные данные сервера SIEM</span><span class="sxs-lookup"><span data-stu-id="256c7-113">SIEM server inputs</span></span> | <span data-ttu-id="256c7-114">Ресурсы для получения дополнительных сведений</span><span class="sxs-lookup"><span data-stu-id="256c7-114">Resources to learn more</span></span> |
| --- | --- | --- |
| [<span data-ttu-id="256c7-115">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="256c7-115">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md) <br/>   <span data-ttu-id="256c7-116">или</span><span class="sxs-lookup"><span data-stu-id="256c7-116">or</span></span>   <br/>[<span data-ttu-id="256c7-117">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="256c7-117">Office 365 Threat Intelligence</span></span>](office-365-ti.md) | <span data-ttu-id="256c7-118">Журналы аудита</span><span class="sxs-lookup"><span data-stu-id="256c7-118">Audit logs</span></span> | [<span data-ttu-id="256c7-119">SIEM интеграции с Office 365 Threat аналитики и расширенный защиту от угроз</span><span class="sxs-lookup"><span data-stu-id="256c7-119">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md) |
| [<span data-ttu-id="256c7-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="256c7-120">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="256c7-121">Журнал интеграции</span><span class="sxs-lookup"><span data-stu-id="256c7-121">Log integration</span></span> | [<span data-ttu-id="256c7-122">SIEM интеграция с Microsoft Cloud приложения безопасности</span><span class="sxs-lookup"><span data-stu-id="256c7-122">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |
| [<span data-ttu-id="256c7-123">Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="256c7-123">Office 365 Cloud App Security</span></span>](office-365-cas-overview.md) | <span data-ttu-id="256c7-124">Журнал интеграции</span><span class="sxs-lookup"><span data-stu-id="256c7-124">Log integration</span></span> | [<span data-ttu-id="256c7-125">Интеграция сервера SIEM с Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="256c7-125">Integrate your SIEM server with Office 365 Cloud App Security</span></span>](integrate-your-siem-server-with-office-365-cas.md) |
| [<span data-ttu-id="256c7-126">Advanced Threat Protection в Защитнике Windows</span><span class="sxs-lookup"><span data-stu-id="256c7-126">Windows Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/) | <span data-ttu-id="256c7-127">Журнал интеграции</span><span class="sxs-lookup"><span data-stu-id="256c7-127">Log integration</span></span> | [<span data-ttu-id="256c7-128">По запросу оповещений в вашей SIEM tools</span><span class="sxs-lookup"><span data-stu-id="256c7-128">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| <span data-ttu-id="256c7-129">[Центр безопасности для Azure](https://docs.microsoft.com/azure/security-center/security-center-intro) (Защиту от угроз и угроз обнаружения)</span><span class="sxs-lookup"><span data-stu-id="256c7-129">[Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-intro) (Threat Protection and Threat Detection)</span></span> | <span data-ttu-id="256c7-130">Оповещения</span><span class="sxs-lookup"><span data-stu-id="256c7-130">Alerts</span></span> | [<span data-ttu-id="256c7-131">Экспорт данных Azure безопасности для предварительной версии SIEM - конвейер конфигурации-</span><span class="sxs-lookup"><span data-stu-id="256c7-131">Azure Security data export to SIEM - Pipeline Configuration - Preview</span></span>](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [<span data-ttu-id="256c7-132">Защита идентификации Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="256c7-132">Azure Active Directory Identity Protection</span></span>](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | <span data-ttu-id="256c7-133">Журналы аудита</span><span class="sxs-lookup"><span data-stu-id="256c7-133">Audit logs</span></span> | [<span data-ttu-id="256c7-134">Интеграция журналы аудита Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="256c7-134">Integrate Azure Active Directory audit logs</span></span>](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [<span data-ttu-id="256c7-135">Аналитика Azure расширенной угроз</span><span class="sxs-lookup"><span data-stu-id="256c7-135">Azure Advanced Threat Analytics</span></span>](https://docs.microsoft.com/azure/security/azure-threat-detection) | <span data-ttu-id="256c7-136">Журнал интеграции</span><span class="sxs-lookup"><span data-stu-id="256c7-136">Log integration</span></span> | [<span data-ttu-id="256c7-137">Справочник по журналу ATA SIEM</span><span class="sxs-lookup"><span data-stu-id="256c7-137">ATA SIEM log reference</span></span>](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="256c7-138">Должно быть включено ведение журнала аудита</span><span class="sxs-lookup"><span data-stu-id="256c7-138">Audit logging must be turned on</span></span>

<span data-ttu-id="256c7-139">Убедитесь, что включено ведение журнала аудита перед настройкой интеграции сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="256c7-139">Make sure audit logging is turned on before you configure SIEM server integration.</span></span> 

- <span data-ttu-id="256c7-140">Для SharePoint Online, OneDrive для бизнеса и Azure Active Directory, [журнал аудита включена в центре соответствия требованиям & безопасности](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span><span class="sxs-lookup"><span data-stu-id="256c7-140">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span></span>

- <span data-ttu-id="256c7-141">Для Exchange Online, [включено ведение журнала аудита с помощью Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span><span class="sxs-lookup"><span data-stu-id="256c7-141">For Exchange Online, [audit logging is turned on with Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span></span>
 
## <a name="see-also"></a><span data-ttu-id="256c7-142">См. также</span><span class="sxs-lookup"><span data-stu-id="256c7-142">See Also</span></span>

[<span data-ttu-id="256c7-143">Освоение облака и гибридные решения</span><span class="sxs-lookup"><span data-stu-id="256c7-143">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="256c7-144">Руководства по лаборатории тестирования для облачных решений</span><span class="sxs-lookup"><span data-stu-id="256c7-144">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


