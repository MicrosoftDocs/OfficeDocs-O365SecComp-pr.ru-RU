---
title: Интеграция SIEM с Office 365 Advanced Threat protection
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
ms.date: 03/11/2019
ms.collection:
- M365-security-compliance
description: Интеграция сервера SIEM в Организации с Office 365 Advanced Threat Protection и связанными событиями угроз в API управления действиями Office 365.
ms.openlocfilehash: fa9dcda0556684b748068cbe5ee848ba443d7667
ms.sourcegitcommit: f25a667e4c7d11c43c87604d576f1e6d6155b14f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2019
ms.locfileid: "30536179"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a><span data-ttu-id="b2c72-103">Интеграция SIEM с Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="b2c72-103">SIEM integration with Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="b2c72-104">Если в организации используется сервер управления инцидентами и событиями SIEM, вы можете интегрировать Office 365 Advanced Threat protection с сервером SIEM.</span><span class="sxs-lookup"><span data-stu-id="b2c72-104">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Advanced Threat Protection with your SIEM server.</span></span> <span data-ttu-id="b2c72-105">Интеграция SIEM позволяет просматривать сведения, такие как вредоносные программы и фишинг, обнаруженные в Office 365 Advanced Protection, в отчетах сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="b2c72-105">SIEM integration enables you to view information, such as malware or phish detected by Office 365 Advanced Protection, in your SIEM server reports.</span></span> <span data-ttu-id="b2c72-106">Для настройки интеграции с SIEM используется [API управления действияМи Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="b2c72-106">To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="b2c72-107">API управления действиями Office 365 извлекает сведения о действиях пользователя, администратора, системы, а также о событиях и политиках из журналов активности Office 365 и Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b2c72-107">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="b2c72-108">[Схема Advanced Threat Protection в office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) работает с Advanced Threat Protection, поэтому если в организации используется Advanced Threat protection (план 1) или план 2 или Office 365, вы по-прежнему можете использовать тот же API для интеграции сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="b2c72-108">The [Office 365 Advanced Threat Protection schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Advanced Threat Protection, so if your organization has the Office 365 Advanced Threat Protection Plan 1 or Plan 2 or Office 365 E5, you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="b2c72-109">Сервер SIEM или другая подобная система должны опрашивать события **аудита. Общая** Рабочая нагрузка для доступа к событиям обнаружения.</span><span class="sxs-lookup"><span data-stu-id="b2c72-109">The SIEM server or other similar system should poll the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="b2c72-110">Чтобы узнать больше, ознакомьтесь [со статьей начало работы с API управления Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="b2c72-110">To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> <span data-ttu-id="b2c72-111">Кроме того, для событий Office 365 ATP важны следующие значения **аудитлогрекордтипе** :</span><span class="sxs-lookup"><span data-stu-id="b2c72-111">In addition, the following values of **AuditLogRecordType** are relevant for Office 365 ATP events:</span></span>

### <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="b2c72-112">Enum: AuditLogRecordType; Type: Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="b2c72-112">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

#### <a name="auditlogrecordtype"></a><span data-ttu-id="b2c72-113">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="b2c72-113">AuditLogRecordType</span></span>

|<span data-ttu-id="b2c72-114">Значение</span><span class="sxs-lookup"><span data-stu-id="b2c72-114">Value</span></span>|<span data-ttu-id="b2c72-115">Имя элемента</span><span class="sxs-lookup"><span data-stu-id="b2c72-115">Member name</span></span>|<span data-ttu-id="b2c72-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b2c72-116">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2c72-117">8</span><span class="sxs-lookup"><span data-stu-id="b2c72-117">28</span></span>|<span data-ttu-id="b2c72-118">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="b2c72-118">ThreatIntelligence</span></span>|<span data-ttu-id="b2c72-119">События фишинга и вредоносных программ из Exchange Online Protection и Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="b2c72-119">Phishing and malware events from Exchange Online Protection and Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="b2c72-120">41</span><span class="sxs-lookup"><span data-stu-id="b2c72-120">41</span></span>|<span data-ttu-id="b2c72-121">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="b2c72-121">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="b2c72-122">События "безопасные ссылки" ATP "время блокировки" и "переопределение блока" из Office 365 Advanced Threat protection.</span><span class="sxs-lookup"><span data-stu-id="b2c72-122">ATP Safe Links time-of-block and block override events from Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="b2c72-123">47</span><span class="sxs-lookup"><span data-stu-id="b2c72-123">47</span></span>|<span data-ttu-id="b2c72-124">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="b2c72-124">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="b2c72-125">События фишинга и вредоносных программ для файлов в SharePoint Online, OneDrive для бизнеса и Microsoft Teams из Office 365 Advanced Threat protection.</span><span class="sxs-lookup"><span data-stu-id="b2c72-125">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams from Office 365 Advanced Threat Protection.</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="b2c72-126">Вы должны быть глобальным администратором Office 365 или иметь роль администратора безопасности, назначенную в центре безопасности _Амп_ соответствия требованиям, для настройки интеграции SIEM с Office 365 Advanced Threat protection.</span><span class="sxs-lookup"><span data-stu-id="b2c72-126">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="b2c72-127">Для среды Office 365 должна быть включена функция ведения журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="b2c72-127">Audit logging must be turned on for your Office 365 environment.</span></span> <span data-ttu-id="b2c72-128">Чтобы получить помощь, ознакомьтесь со статьей [Включение и отключение поиска в журнале аудита Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="b2c72-128">To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2c72-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="b2c72-129">Related topics</span></span>

[<span data-ttu-id="b2c72-130">Исследование угроз для Office 365 и ответ на них</span><span class="sxs-lookup"><span data-stu-id="b2c72-130">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)

[<span data-ttu-id="b2c72-131">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="b2c72-131">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="b2c72-132">Интеллектуальные отчеты и аналитика в центре безопасности &amp; и соответствия требованиям Office 365</span><span class="sxs-lookup"><span data-stu-id="b2c72-132">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="b2c72-133">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="b2c72-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  
