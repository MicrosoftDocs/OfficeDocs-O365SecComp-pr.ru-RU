---
title: Справочные сведения о политике безопасности для Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aef6c88f-7f47-40ef-9503-2b400e3bc6fd
description: Справка по политикам действий для Office 365 и политикам обнаружения аномалий.
ms.openlocfilehash: db44b6cbf5b8c2783cba9862107120d2c33c1559
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264631"
---
# <a name="security-policy-reference-information-for-office-365-cloud-app-security"></a><span data-ttu-id="3612a-103">Справочные сведения о политике безопасности для Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3612a-103">Security policy reference information for Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="3612a-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3612a-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="3612a-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3612a-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="3612a-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="3612a-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="3612a-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="3612a-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="3612a-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="3612a-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="3612a-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="3612a-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="3612a-110">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="3612a-110">You are here!</span></span>  <br/> [<span data-ttu-id="3612a-111">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="3612a-111">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |[<span data-ttu-id="3612a-112">Начало использования</span><span class="sxs-lookup"><span data-stu-id="3612a-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="3612a-113">Если вы являетесь глобальным администратором или администратором безопасности, в Office 365 вы можете определить или изменить политики двух типов в Организации:</span><span class="sxs-lookup"><span data-stu-id="3612a-113">With Office 365 Cloud App Security, if you are a global administrator or security administrator, you can define or edit two kinds of policies for your organization:</span></span>
  
- <span data-ttu-id="3612a-114">Определяемые **[политики действий](activity-policies-and-alerts.md)** .</span><span class="sxs-lookup"><span data-stu-id="3612a-114">**[Activity policies](activity-policies-and-alerts.md)** that you define.</span></span> <span data-ttu-id="3612a-115">Эти политики основываются на действиях, которые вы задаете как подозрительные, например пользователи, пытающиеся выполнить вход с использованием учетных данных администратора в других регионах или в других странах, не входящих в число попыток входа для пользователя в течение часа. .</span><span class="sxs-lookup"><span data-stu-id="3612a-115">These policies are based on activities that you define as suspicious, such as users attempting to sign in with admin credentials in other regions/countries outside what's normal for your organization, or an extreme number of sign-in attempts for a user within an hour.</span></span> <span data-ttu-id="3612a-116">Чтобы узнать больше, ознакомьтесь со статьей [политики действий и оповещения в Office 365 Cloud App Security](activity-policies-and-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="3612a-116">To learn more, see [Activity policies and alerts in Office 365 Cloud App Security](activity-policies-and-alerts.md).</span></span>
    
- <span data-ttu-id="3612a-117">**[Политики обнаружения аномалий](anomaly-detection-policies-in-ocas.md)** , доступные "из" из поля "в Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="3612a-117">**[Anomaly detection policies](anomaly-detection-policies-in-ocas.md)** that are available "out of the box" with Office 365 Cloud App Security.</span></span> <span data-ttu-id="3612a-118">Эти политики основываются на автоматических алгоритмах, которые обнаруживают подозрительные действия.</span><span class="sxs-lookup"><span data-stu-id="3612a-118">These policies are based on automatic algorithms that detect suspicious activity.</span></span> <span data-ttu-id="3612a-119">Эти политики по умолчанию проводят наблюдение за аномалией и автоматически инициируют оповещения.</span><span class="sxs-lookup"><span data-stu-id="3612a-119">These default policies watch for anomalies and trigger alerts automatically.</span></span> <span data-ttu-id="3612a-120">Чтобы узнать больше, ознакомьтесь со статьей [политики обнаружения аномалий в Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="3612a-120">To learn more, see [Anomaly detection policies in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md).</span></span>
    

