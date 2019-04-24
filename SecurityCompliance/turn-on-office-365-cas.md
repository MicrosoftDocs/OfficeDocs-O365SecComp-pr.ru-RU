---
title: Включение Cloud App Security для Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: ba919c73-d021-404d-9850-eec57e78678c
description: В этой статье рассказывается, как включить Office 365 Cloud App Security, на платформе Cloud App Security в Microsoft Azure.
ms.openlocfilehash: 1227545b1e4d1521dc1820342f09aabdf16ec2c6
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264131"
---
# <a name="turn-on-office-365-cloud-app-security"></a><span data-ttu-id="566ae-103">Включение Cloud App Security для Office 365</span><span class="sxs-lookup"><span data-stu-id="566ae-103">Turn on Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="566ae-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="566ae-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="566ae-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="566ae-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="566ae-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="566ae-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="566ae-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="566ae-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="566ae-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="566ae-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="566ae-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="566ae-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="566ae-110">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="566ae-110">You are here!</span></span>  <br/> [<span data-ttu-id="566ae-111">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="566ae-111">Next step</span></span>](activity-policies-and-alerts.md) <br/> |[<span data-ttu-id="566ae-112">Начало использования</span><span class="sxs-lookup"><span data-stu-id="566ae-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
  
## <a name="turn-on-office-365-cloud-app-security"></a><span data-ttu-id="566ae-113">Включение Cloud App Security для Office 365</span><span class="sxs-lookup"><span data-stu-id="566ae-113">Turn on Office 365 Cloud App Security</span></span>

> [!IMPORTANT]
> <span data-ttu-id="566ae-114">Для выполнения следующей задачи необходимо быть глобальным администратором или администратором безопасности.</span><span class="sxs-lookup"><span data-stu-id="566ae-114">You must be a global administrator or security administrator to perform the following task.</span></span> <span data-ttu-id="566ae-115">Чтобы узнать больше, ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="566ae-115">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> <span data-ttu-id="566ae-116">Для правильной работы Office 365 Cloud App Security **необходимо включить ведение журнала аудита** для среды Office 365.</span><span class="sxs-lookup"><span data-stu-id="566ae-116">In order for Office 365 Cloud App Security to work correct, **audit logging must be turned on** for your Office 365 environment.</span></span> <span data-ttu-id="566ae-117">Дополнительную информацию можно узнать [в статье Включение и отключение поиска в журнале аудита Office 365](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="566ae-117">For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
1. <span data-ttu-id="566ae-118">В качестве глобального администратора или администратора безопасности войдите в рабочую [https://protection.office.com](https://security.microsoft.com) или учебную учетную запись Office 365, используя рабочую или учебную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="566ae-118">As a global administrator or security administrator, go to [https://protection.office.com](https://security.microsoft.com) and sign in using your work or school account for Office 365.</span></span> <span data-ttu-id="566ae-119">(Откроется центр соответствия требованиям безопасности &amp; .)</span><span class="sxs-lookup"><span data-stu-id="566ae-119">(This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="566ae-120">Перейдите к разделу **оповещения** \> **Управление расширенными оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="566ae-120">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="566ae-121">Выберите **включить Office 365 Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="566ae-121">Select **Turn on Office 365 Cloud App Security**.</span></span>
    
4. <span data-ttu-id="566ae-122">Выберите **Перейти к Office 365 Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="566ae-122">Choose **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="566ae-123">![В центре безопасности &amp; и соответствия требованиям выберите Управление расширенными оповещениями для перехода к Office 365 Cloud App Security.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="566ae-123">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="566ae-124">Откроется портал Office 365 Cloud App Security, где можно просматривать отчеты, а также создавать и изменять политики.</span><span class="sxs-lookup"><span data-stu-id="566ae-124">This takes you to the Office 365 Cloud App Security portal, where you can view reports and create or edit your policies.</span></span>

<span data-ttu-id="566ae-125">После включения безопасности облачных приложений Office 365 вы можете перейти на портал Cloud App Security, посетив [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) и войдя в систему.</span><span class="sxs-lookup"><span data-stu-id="566ae-125">After you have turned on Office 365 Cloud App Security, you can go to the Cloud App Security portal by visiting [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) and signing in.</span></span>
    
> [!NOTE]
> <span data-ttu-id="566ae-126">Когда вы включаете Office 365 Cloud App Security, аудит сведений об учетных записях пользователей Office 365 и действий пользователей передается в [Microsoft Cloud App Security](https://aka.ms/whatiscas).</span><span class="sxs-lookup"><span data-stu-id="566ae-126">When you turn on Office 365 Cloud App Security, auditing information about your Office 365 user accounts and user activities is transferred to [Microsoft Cloud App Security](https://aka.ms/whatiscas).</span></span> <span data-ttu-id="566ae-127">Это позволяет Office 365 предоставлять расширенные оповещения, фильтрацию и другие функции для получения сведений и выполнения действий по подозрительным действиям.</span><span class="sxs-lookup"><span data-stu-id="566ae-127">This allows Office 365 to provide advanced alerts, filtering, and other features so you can get information and take action about suspicious activities.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="566ae-128">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="566ae-128">Next steps</span></span>

- [<span data-ttu-id="566ae-129">Политики действий</span><span class="sxs-lookup"><span data-stu-id="566ae-129">Activity policies</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="566ae-130">Политики обнаружения аномалий</span><span class="sxs-lookup"><span data-stu-id="566ae-130">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="566ae-131">Интеграция сервера SIEM</span><span class="sxs-lookup"><span data-stu-id="566ae-131">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="566ae-132">Группировка IP-адресов для упрощения управления</span><span class="sxs-lookup"><span data-stu-id="566ae-132">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

