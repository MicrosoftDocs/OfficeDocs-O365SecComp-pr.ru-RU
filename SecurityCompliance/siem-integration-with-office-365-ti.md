---
title: Интеграция SIEM с Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Интеграция с анализ угроз Office 365 с помощью API-интерфейса управления Office 365 активности сервера SIEM вашей организации.
ms.openlocfilehash: 82aeeea53bf87f1555fa68b2784b8fe38a435e15
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535102"
---
# <a name="siem-integration-with-office-365-threat-intelligence"></a><span data-ttu-id="87cd1-103">Интеграция SIEM с Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="87cd1-103">SIEM integration with Office 365 Threat Intelligence</span></span>

<span data-ttu-id="87cd1-p101">Если ваша организация использует сервер безопасности происшествия и события управления (SIEM), можно интегрировать анализ угроз Office 365 с сервером SIEM. Это позволяет просмотреть сведения, такие как вредоносных программ, обнаруженных с анализ угроз Office 365, в отчетах сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="87cd1-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence with your SIEM server. This enables you to view information, such as malware detected by Office 365 Threat Intelligence, in your SIEM server reports.</span></span>
  
## <a name="use-the-office-365-activity-management-api"></a><span data-ttu-id="87cd1-106">Использование API для управления Office 365 активности</span><span class="sxs-lookup"><span data-stu-id="87cd1-106">Use the Office 365 Activity Management API</span></span>

<span data-ttu-id="87cd1-p102">Чтобы интегрировать анализ угроз Office 365 с сервером SIEM, используйте API для управления Office 365 активности. Этот интерфейс API извлекаются сведения о пользователя, администрирования, система и действия в рамках политики и события из вашей организации Office 365 и Azure AD журналы активности.</span><span class="sxs-lookup"><span data-stu-id="87cd1-p102">To integrate Office 365 Threat Intelligence with your SIEM server, use the Office 365 Activity Management API. This API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure AD activity logs.</span></span> 
  
<span data-ttu-id="87cd1-109">Необходимо быть глобального администратора Office 365 или роль администратора безопасности, назначенные в системы &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="87cd1-109">You must be an Office 365 global administrator or have the security administrator role assigned in the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="87cd1-110">Справочник [API действия для управления Office 365](https://msdn.microsoft.com/en-us/office-365/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="87cd1-110">See [Office 365 Management Activity API reference](https://msdn.microsoft.com/en-us/office-365/office-365-management-activity-api-reference).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="87cd1-111">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="87cd1-111">Related topics</span></span>

[<span data-ttu-id="87cd1-112">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="87cd1-112">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="87cd1-113">Защита от угроз в Office 365</span><span class="sxs-lookup"><span data-stu-id="87cd1-113">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="87cd1-114">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="87cd1-114">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

