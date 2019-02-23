---
title: Защита доступа к данным и службам в Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Целевая страница для защиты доступа к данным и службам O365
ms.openlocfilehash: 95933c5a7bc95f9fd70e8f3470055b57193971d4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213539"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a><span data-ttu-id="bb56f-103">Защита доступа к данным и службам в Office 365</span><span class="sxs-lookup"><span data-stu-id="bb56f-103">Protect access to data and services in Office 365</span></span>

<span data-ttu-id="bb56f-p101">Защита доступа к данным и службам Office 365 важна для защиты от кибератак-атак и защиты от потери данных. Одни и те же защиты можно применять к другим приложениям SaaS в среде и даже к локальным приложениям, публикуемым с помощью прокси-сервера приложения Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bb56f-p101">Protecting access to your Office 365 data and services is crucial to defending against cyber-attacks and guarding against data loss. The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="bb56f-106">Шаг 1: проверка рекомендаций</span><span class="sxs-lookup"><span data-stu-id="bb56f-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="bb56f-107">Рекомендуемые возможности для защиты удостоверений и устройств, имеющих доступ к Office 365 и отличных от SaaS-служб и локальных приложений, которые опубликованы с помощью прокси приложения Azure AD.</span><span class="sxs-lookup"><span data-stu-id="bb56f-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="bb56f-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Другие языки](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="bb56f-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-configure-mfa"></a><span data-ttu-id="bb56f-109">Шаг 2: Настройка MFA</span><span class="sxs-lookup"><span data-stu-id="bb56f-109">Step 2: Configure MFA</span></span>

<span data-ttu-id="bb56f-110">Используйте эти ресурсы для ориентации себя на MFA, выберите нужную версию, а затем запланируйте и разверните MFA для своей среды.</span><span class="sxs-lookup"><span data-stu-id="bb56f-110">Use these resources to orient yourself to MFA, decide which version is right for you, and then plan and deploy MFA for your environment.</span></span>
  
- [<span data-ttu-id="bb56f-111">Что такое многофакторная проверка подлинности Azure?</span><span class="sxs-lookup"><span data-stu-id="bb56f-111">What is Azure multi-factor authentication?</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [<span data-ttu-id="bb56f-112">Выбор решения многофакторной проверки подлинности Azure</span><span class="sxs-lookup"><span data-stu-id="bb56f-112">Choose the Azure multi-factor authentication solution for you</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="bb56f-113">Получение многофакторной проверки подлинности Azure</span><span class="sxs-lookup"><span data-stu-id="bb56f-113">How to get Azure multi-factor authentication</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [<span data-ttu-id="bb56f-114">Планирование многофакторной проверки подлинности для развертываний Office 365</span><span class="sxs-lookup"><span data-stu-id="bb56f-114">Plan for multi-factor authentication for Office 365 deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="bb56f-115">Настройка многофакторной проверки подлинности для пользователей Office 365</span><span class="sxs-lookup"><span data-stu-id="bb56f-115">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [<span data-ttu-id="bb56f-116">Планирование развертывания MFA, облака или локальной</span><span class="sxs-lookup"><span data-stu-id="bb56f-116">Plan where to deploy MFA, Cloud or on-premises</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="bb56f-117">Настройка параметров многофакторной проверки подлинности Azure</span><span class="sxs-lookup"><span data-stu-id="bb56f-117">Configure Azure multi-factor authentication settings</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a><span data-ttu-id="bb56f-118">Шаг 3: принудительное применение MFA с правилами условного доступа Azure AD</span><span class="sxs-lookup"><span data-stu-id="bb56f-118">Step 3: Enforce MFA with Azure AD conditional access rules</span></span>

<span data-ttu-id="bb56f-119">Если вы используете Azure AD для Azure, создайте правило условного доступа, чтобы оно требовало использования MFA для доступа к Office 365 и другим приложениям SaaS в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="bb56f-119">If you are using Azure AD MFA, create a conditional access rule to require MFA for access to Office 365 and other SaaS apps in your environment.</span></span>
  
- [<span data-ttu-id="bb56f-120">Условный доступ в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bb56f-120">Conditional access in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a><span data-ttu-id="bb56f-121">Шаг 4: Настройка управления привилегированным доступом</span><span class="sxs-lookup"><span data-stu-id="bb56f-121">Step 4: Configure privileged access management</span></span>

<span data-ttu-id="bb56f-p102">Управление привилегированным доступом позволяет осуществлять детализированный контроль над задачами привилегированного администрирования в Office 365.  Это помогает защитить организацию от нарушений, которые могут использовать существующие привилегированные учетные записи администраторов с ограниченным доступом к конфиденциальным данным или к критическим параметрам конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bb56f-p102">Privileged access management allows granular access control over privileged admin tasks in Office 365.  It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span>

- [<span data-ttu-id="bb56f-124">Общие сведения об управлении привилегированным доступом</span><span class="sxs-lookup"><span data-stu-id="bb56f-124">Overview of privileged access management</span></span>](privileged-access-management-overview.md)
- [<span data-ttu-id="bb56f-125">Настройка управления привилегированным доступом</span><span class="sxs-lookup"><span data-stu-id="bb56f-125">Configure privileged access management</span></span>](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a><span data-ttu-id="bb56f-126">Шаг 5: Настройка политик доступа к устройствам SharePoint</span><span class="sxs-lookup"><span data-stu-id="bb56f-126">Step 5: Configure SharePoint device access policies</span></span>

<span data-ttu-id="bb56f-p103">Политики доступа к устройствам для SharePoint Online и OneDrive для бизнеса рекомендуются для защиты конфиденциальных, классифицированных и регулируемых данных. Появилась возможность применять политики доступа к устройствам к отдельным сайтам групп.</span><span class="sxs-lookup"><span data-stu-id="bb56f-p103">Device access policies for SharePoint Online and OneDrive for Business are recommended for protecting sensitive, classified, and regulated data. Coming soon is the ability to apply device access policies to individual team sites.</span></span>
  
- [<span data-ttu-id="bb56f-129">Управление доступом с неуправляемых устройств</span><span class="sxs-lookup"><span data-stu-id="bb56f-129">Control access from unmanaged devices</span></span>](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a><span data-ttu-id="bb56f-130">Шаг 6: Настройка защиты приложений и данных для устройств</span><span class="sxs-lookup"><span data-stu-id="bb56f-130">Step 6: Configure app and data protection for devices</span></span>

<span data-ttu-id="bb56f-p104">Вы можете управлять приложениями на мобильных устройствах независимо от того, зарегистрированы ли устройства для управления мобильными устройствами. Это обеспечивает защиту от случайного утечки данных в Office 365, в том числе почты и файлов.</span><span class="sxs-lookup"><span data-stu-id="bb56f-p104">You can manage applications on mobile devices regardless of whether the devices are enrolled for mobile device management. This protects against accidental leakage of data in Office 365, including mail and files.</span></span>
  
- <span data-ttu-id="bb56f-133">Для iOS и Android: [Защита данных приложений с помощью политик защиты приложений с помощью Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="bb56f-133">For iOS and Android: [Protect app data using app protection policies with Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span></span>
    
<span data-ttu-id="bb56f-134">Для Windows 10 настройте Windows Information Protection (WIP), чтобы предотвратить случайные утечки данных.</span><span class="sxs-lookup"><span data-stu-id="bb56f-134">For Windows 10, configure Windows Information Protection (WIP) to prevent accidental data leaks.</span></span>
  
- <span data-ttu-id="bb56f-135">Для управляемых устройств: [Создание Windows Information Protection (WIP) с политикой регистрации с помощью портала Azure для Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span><span class="sxs-lookup"><span data-stu-id="bb56f-135">For managed devices: [Create a Windows Information Protection (WIP) with enrollment policy using the Azure portal for Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span></span>
    
- <span data-ttu-id="bb56f-136">Для неуправляемых устройств: [Создание и развертывание политики защиты приложений Windows Information Protection (WIP) с помощью Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span><span class="sxs-lookup"><span data-stu-id="bb56f-136">For un-managed devices: [Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span></span>
    
## <a name="step-7-manage-devices-with-intune"></a><span data-ttu-id="bb56f-137">Шаг 7: Управление устройствами с помощью Intune</span><span class="sxs-lookup"><span data-stu-id="bb56f-137">Step 7: Manage devices with Intune</span></span>

<span data-ttu-id="bb56f-p105">Управление устройствами позволяет убедиться, что они являются работоспособными и совместимыми, прежде чем разрешить им доступ к ресурсам в вашей среде. Правила условного доступа на основе устройств гарантируют, что злоумышленники не смогут получить доступ к ресурсам из неуправляемых устройств.</span><span class="sxs-lookup"><span data-stu-id="bb56f-p105">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment. Device based conditional access rules help ensure attackers can't gain access to your resources from unmanaged devices.</span></span>
  
- [<span data-ttu-id="bb56f-140">Регистрация устройств для управления в Intune</span><span class="sxs-lookup"><span data-stu-id="bb56f-140">Enroll devices for management in Intune</span></span>](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a><span data-ttu-id="bb56f-141">Шаг 8: Настройка дополнительных политик Intune и правил условного доступа для среды</span><span class="sxs-lookup"><span data-stu-id="bb56f-141">Step 8: Configure additional Intune policies and conditional access rules for your environment</span></span>

<span data-ttu-id="bb56f-142">Используйте эти Рекомендуемые конфигурации в качестве отправной точки для сценариев масштаба предприятия или сложных сценариев безопасности доступа.</span><span class="sxs-lookup"><span data-stu-id="bb56f-142">Use these recommended configurations as a starting point for enterprise scale or sophisticated access security scenarios.</span></span>
  
- [<span data-ttu-id="bb56f-143">Безопасные политики электронной почты и конфигурации</span><span class="sxs-lookup"><span data-stu-id="bb56f-143">Secure email policies and configurations</span></span>](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

