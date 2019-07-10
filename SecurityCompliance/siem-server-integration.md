---
title: Интеграция сервера SIEM с Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 06/17/2019
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
description: Сводка. Ознакомьтесь с этой статьей, чтобы получить обзор интеграции сервера SIEM с Microsoft 365.
ms.openlocfilehash: 97f1c1d1f1862d140e014b4460ac9f40cb1934bb
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600896"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="bae6a-103">Интеграция сервера SIEM со службами и приложениями Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bae6a-103">SIEM server integration with Microsoft 365 services and applications</span></span>

## <a name="overview"></a><span data-ttu-id="bae6a-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="bae6a-104">Overview</span></span>

<span data-ttu-id="bae6a-105">Если в Организации используются сведения о безопасности и управление событиями (SIEM), или если вы планируете немедленно получить сервер SIEM, вам может быть интересно узнать, как будет осуществляться интеграция с Microsoft 365, в том числе Office 365.</span><span class="sxs-lookup"><span data-stu-id="bae6a-105">If your organization is using a Security Information and Event Management (SIEM) server, or if you are planning to get a SIEM server soon, you might be wondering how that'll integrate with your Microsoft 365, including Office 365 E5.</span></span> <span data-ttu-id="bae6a-106">Необходимость использования сервера SIEM зависит от многих факторов, таких как требования к безопасности в Организации.</span><span class="sxs-lookup"><span data-stu-id="bae6a-106">Whether you need a SIEM server depends on many factors, such as your organization's security requirements.</span></span> <span data-ttu-id="bae6a-107">Microsoft 365 предлагает разнообразные функции обеспечения безопасности. Тем не менее, если в Организации есть контент и приложения в локальной среде и в облаке (как в случае гибридного развертывания в гибридном облаке), вы можете добавить сервер SIEM для дополнительной защиты.</span><span class="sxs-lookup"><span data-stu-id="bae6a-107">Microsoft 365 offers a variety of security features; however, if your organization has content and applications on premises and in the cloud (as in the case of a hybrid cloud deployment), you might consider adding a SIEM server for extra protection.</span></span> <span data-ttu-id="bae6a-108">Если у вашей организации есть особые требования к безопасности, которые необходимо учитывать, можно добавить сервер SIEM в среду.</span><span class="sxs-lookup"><span data-stu-id="bae6a-108">Or, if your organization has particularly stringent security requirements you must meet, you might consider adding a SIEM server to your environment.</span></span>

## <a name="siem-server-integration-microsoft-365"></a><span data-ttu-id="bae6a-109">Интеграция сервера SIEM Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bae6a-109">SIEM server integration Microsoft 365</span></span>

<span data-ttu-id="bae6a-110">Сервер SIEM может получать данные из разнообразных служб и приложений Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bae6a-110">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications.</span></span> <span data-ttu-id="bae6a-111">В следующей таблице приведены некоторые приложения и службы Microsoft 365, а также входные данные сервера SIEM, а также дополнительные сведения о интеграции сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="bae6a-111">The following table lists several Microsoft 365 services and applications along with SIEM server inputs and where to go to learn more about SIEM server integration.</span></span> 

| <span data-ttu-id="bae6a-112">Служба или приложение Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="bae6a-112">Microsoft 365 Service or Application</span></span> | <span data-ttu-id="bae6a-113">Входные данные сервера SIEM</span><span class="sxs-lookup"><span data-stu-id="bae6a-113">SIEM server inputs</span></span> | <span data-ttu-id="bae6a-114">Ресурсы для получения дополнительных сведений</span><span class="sxs-lookup"><span data-stu-id="bae6a-114">Resources to learn more</span></span> |
| --- | --- | --- |
| [<span data-ttu-id="bae6a-115">Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="bae6a-115">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md) <br/><span data-ttu-id="bae6a-116">или</span><span class="sxs-lookup"><span data-stu-id="bae6a-116">or</span></span><br/>[<span data-ttu-id="bae6a-117">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="bae6a-117">Office 365 Threat Intelligence</span></span>](office-365-ti.md) | <span data-ttu-id="bae6a-118">Журналы аудита</span><span class="sxs-lookup"><span data-stu-id="bae6a-118">Audit logs</span></span> | [<span data-ttu-id="bae6a-119">Интеграция SIEM с Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="bae6a-119">SIEM integration with Office 365 Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md) |
| [<span data-ttu-id="bae6a-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bae6a-120">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="bae6a-121">Интеграция журналов</span><span class="sxs-lookup"><span data-stu-id="bae6a-121">Log integration</span></span> | [<span data-ttu-id="bae6a-122">Интеграция SIEM с Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="bae6a-122">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |
| [<span data-ttu-id="bae6a-123">Защита от угроз Майкрософт</span><span class="sxs-lookup"><span data-stu-id="bae6a-123">Microsoft Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/) | <span data-ttu-id="bae6a-124">Интеграция журналов</span><span class="sxs-lookup"><span data-stu-id="bae6a-124">Log integration</span></span> | [<span data-ttu-id="bae6a-125">Получение оповещений о средствах SIEM</span><span class="sxs-lookup"><span data-stu-id="bae6a-125">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-siem) |
| <span data-ttu-id="bae6a-126">[Центр безопасности Azure](https://docs.microsoft.com/azure/security-center/security-center-intro) (Защита от угроз и обнаружение угроз)</span><span class="sxs-lookup"><span data-stu-id="bae6a-126">[Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-intro) (Threat Protection and Threat Detection)</span></span> | <span data-ttu-id="bae6a-127">Оповещения</span><span class="sxs-lookup"><span data-stu-id="bae6a-127">Alerts</span></span> | [<span data-ttu-id="bae6a-128">Экспорт данных безопасности Azure в SIEM — Настройка конвейера — Предварительная версия</span><span class="sxs-lookup"><span data-stu-id="bae6a-128">Azure Security data export to SIEM - Pipeline Configuration - Preview</span></span>](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
|[<span data-ttu-id="bae6a-129">Служба Advanced Threat Analytics для Azure</span><span class="sxs-lookup"><span data-stu-id="bae6a-129">Azure Advanced Threat Analytics</span></span>](https://docs.microsoft.com/azure/security/azure-threat-detection) | <span data-ttu-id="bae6a-130">Azure Monitor</span><span class="sxs-lookup"><span data-stu-id="bae6a-130">Azure Monitor</span></span> | [<span data-ttu-id="bae6a-131">Блог Интеграция средств SIEM с помощью Azure Monitor</span><span class="sxs-lookup"><span data-stu-id="bae6a-131">(Blog) Use Azure Monitor to integrate with SIEM tools</span></span>](https://azure.microsoft.com/blog/use-azure-monitor-to-integrate-with-siem-tools) |
|[<span data-ttu-id="bae6a-132">Защита идентификации Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bae6a-132">Azure Active Directory Identity Protection</span></span>](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) |<span data-ttu-id="bae6a-133">Интеграция журналов</span><span class="sxs-lookup"><span data-stu-id="bae6a-133">Log integration</span></span> |[<span data-ttu-id="bae6a-134">Интеграция оповещений API безопасности Microsoft Graph с SIEM</span><span class="sxs-lookup"><span data-stu-id="bae6a-134">Integrate Microsoft Graph Security API alerts with a SIEM</span></span>](https://docs.microsoft.com/graph/security-siemintegration) |


## <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="bae6a-135">Необходимо включить ведение журнала аудита</span><span class="sxs-lookup"><span data-stu-id="bae6a-135">Audit logging must be turned on</span></span>

<span data-ttu-id="bae6a-136">Перед настройкой интеграции сервера SIEM убедитесь, что ведение журнала аудита включено.</span><span class="sxs-lookup"><span data-stu-id="bae6a-136">Make sure audit logging is turned on before you configure SIEM server integration.</span></span> 

- <span data-ttu-id="bae6a-137">Для SharePoint Online, OneDrive для бизнеса и Azure Active Directory [ведение журнала аудита включено в центре безопасности & соответствия требованиям](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span><span class="sxs-lookup"><span data-stu-id="bae6a-137">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span></span>

- <span data-ttu-id="bae6a-138">Для Exchange Online [ведение журнала аудита включено с помощью Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span><span class="sxs-lookup"><span data-stu-id="bae6a-138">For Exchange Online, [audit logging is turned on with Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span></span>
 
## <a name="see-also"></a><span data-ttu-id="bae6a-139">См. также</span><span class="sxs-lookup"><span data-stu-id="bae6a-139">See Also</span></span>

[<span data-ttu-id="bae6a-140">Освоение облака и гибридные решения</span><span class="sxs-lookup"><span data-stu-id="bae6a-140">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="bae6a-141">Руководства по лаборатории тестирования для облачных решений</span><span class="sxs-lookup"><span data-stu-id="bae6a-141">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


