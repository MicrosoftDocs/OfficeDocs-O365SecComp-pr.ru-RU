---
title: Защита доступа к данным и службам в Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Главная страница для защиты доступа к данным O365 и служб
ms.openlocfilehash: 6ea617b1a7a7a34492689908d4816a851d58e776
ms.sourcegitcommit: 0ce722533d72fa8dcc1d8a58d3c649cb345b938d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/19/2018
ms.locfileid: "24009105"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a><span data-ttu-id="ea082-103">Защита доступа к данным и службам в Office 365</span><span class="sxs-lookup"><span data-stu-id="ea082-103">Protect access to data and services in Office 365</span></span>

<span data-ttu-id="ea082-p101">Защита доступа к данным Office 365 и службы важно защита от атаки через Интернет и защита от потери данных. Те же средства защиты может применяться к другим приложениям SaaS в вашей среде и опубликован даже для локальных приложений с Azure Active Directory приложения прокси.</span><span class="sxs-lookup"><span data-stu-id="ea082-p101">Protecting access to your Office 365 data and services is crucial to defending against cyber-attacks and guarding against data loss. The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="ea082-106">Шаг 1: Ознакомления с рекомендациями</span><span class="sxs-lookup"><span data-stu-id="ea082-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="ea082-107">Рекомендуемые возможности для защиты удостоверений и устройств, имеющих доступ к Office 365 и отличных от SaaS-служб и локальных приложений, которые опубликованы с помощью прокси приложения Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ea082-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="ea082-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Другие языки](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="ea082-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-configure-mfa"></a><span data-ttu-id="ea082-109">Шаг 2: Настройка многофакторной проверкой Подлинности</span><span class="sxs-lookup"><span data-stu-id="ea082-109">Step 2: Configure MFA</span></span>

<span data-ttu-id="ea082-110">Используйте следующие ресурсы для сориентироваться самостоятельно многофакторной проверкой Подлинности, решить, какую версию, а затем планировании и развертывании многофакторной проверкой Подлинности для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="ea082-110">Use these resources to orient yourself to MFA, decide which version is right for you, and then plan and deploy MFA for your environment.</span></span>
  
- [<span data-ttu-id="ea082-111">Что такое многофакторная проверка подлинности Azure?</span><span class="sxs-lookup"><span data-stu-id="ea082-111">What is Azure multi-factor authentication?</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [<span data-ttu-id="ea082-112">Выберите решение многофакторная проверка подлинности Azure</span><span class="sxs-lookup"><span data-stu-id="ea082-112">Choose the Azure multi-factor authentication solution for you</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="ea082-113">Как получить многофакторная проверка подлинности Azure</span><span class="sxs-lookup"><span data-stu-id="ea082-113">How to get Azure multi-factor authentication</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [<span data-ttu-id="ea082-114">Планирование для многофакторной проверки подлинности для развертываний Office 365</span><span class="sxs-lookup"><span data-stu-id="ea082-114">Plan for multi-factor authentication for Office 365 deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="ea082-115">Настройка многофакторной проверки подлинности для пользователей Office 365</span><span class="sxs-lookup"><span data-stu-id="ea082-115">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [<span data-ttu-id="ea082-116">Планирование места развертывания многофакторной проверкой Подлинности, облако или локальный</span><span class="sxs-lookup"><span data-stu-id="ea082-116">Plan where to deploy MFA, Cloud or on-premises</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="ea082-117">Настройка параметров многофакторная проверка подлинности Azure</span><span class="sxs-lookup"><span data-stu-id="ea082-117">Configure Azure multi-factor authentication settings</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a><span data-ttu-id="ea082-118">Шаг 3: Обеспечение многофакторной проверкой Подлинности с помощью правил условного доступа Azure AD</span><span class="sxs-lookup"><span data-stu-id="ea082-118">Step 3: Enforce MFA with Azure AD conditional access rules</span></span>

<span data-ttu-id="ea082-119">При использовании многофакторной проверкой Подлинности Azure AD создания правила условного доступа для поддержки требования многофакторной проверкой Подлинности для доступа к Office 365 и других приложений SaaS в вашей среде.</span><span class="sxs-lookup"><span data-stu-id="ea082-119">If you are using Azure AD MFA, create a conditional access rule to require MFA for access to Office 365 and other SaaS apps in your environment.</span></span>
  
- [<span data-ttu-id="ea082-120">Условное доступа в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ea082-120">Conditional access in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a><span data-ttu-id="ea082-121">Шаг 4: Настройка управления правами доступа</span><span class="sxs-lookup"><span data-stu-id="ea082-121">Step 4: Configure privileged access management</span></span>

<span data-ttu-id="ea082-p102">Привилегированный доступ управления позволяет управлять детального доступа задачи правами администратора в Office 365.  Он может помочь защитить организацию от нарушения безопасности, которые могут использовать существующие учетные записи с правами администратора с положение доступа к конфиденциальным данным или доступ к параметрам конфигурации важных.</span><span class="sxs-lookup"><span data-stu-id="ea082-p102">Privileged access management allows granular access control over privileged admin tasks in Office 365.  It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span>

- [<span data-ttu-id="ea082-124">Общие сведения о полномочиями доступ к управлению</span><span class="sxs-lookup"><span data-stu-id="ea082-124">Overview of privileged access management</span></span>](privileged-access-managment-overview.md)
- [<span data-ttu-id="ea082-125">Настройка управления правами доступа</span><span class="sxs-lookup"><span data-stu-id="ea082-125">Configure privileged access management</span></span>](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a><span data-ttu-id="ea082-126">Шаг 5: Настройка политик доступа устройства SharePoint</span><span class="sxs-lookup"><span data-stu-id="ea082-126">Step 5: Configure SharePoint device access policies</span></span>

<span data-ttu-id="ea082-p103">Для защиты конфиденциальных секретная и регулируемого данных рекомендуется использовать политики доступа устройств для SharePoint Online и OneDrive для бизнеса. Готовится к выпуску — это возможность применения политик доступа устройств к сайтам отдельные группы.</span><span class="sxs-lookup"><span data-stu-id="ea082-p103">Device access policies for SharePoint Online and OneDrive for Business are recommended for protecting sensitive, classified, and regulated data. Coming soon is the ability to apply device access policies to individual team sites.</span></span>
  
- [<span data-ttu-id="ea082-129">Управление доступом с неуправляемых устройств</span><span class="sxs-lookup"><span data-stu-id="ea082-129">Control access from unmanaged devices</span></span>](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a><span data-ttu-id="ea082-130">Шаг 6: Настройте приложения и защиты данных для устройств</span><span class="sxs-lookup"><span data-stu-id="ea082-130">Step 6: Configure app and data protection for devices</span></span>

<span data-ttu-id="ea082-p104">Можно управлять приложениями на мобильных устройствах, независимо от того, ли участвуют устройств для мобильных устройств management. Это обеспечивает защиту от случайного утечки данных в Office 365, включая электронную почту и файлы.</span><span class="sxs-lookup"><span data-stu-id="ea082-p104">You can manage applications on mobile devices regardless of whether the devices are enrolled for mobile device management. This protects against accidental leakage of data in Office 365, including mail and files.</span></span>
  
- <span data-ttu-id="ea082-133">Для операций ввода-вывода и Android: [защитить данные приложения с помощью политики в отношении защиты приложений с помощью Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="ea082-133">For iOS and Android: [Protect app data using app protection policies with Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span></span>
    
<span data-ttu-id="ea082-134">Для Windows 10 настройте сведения о защите Windows (НЗП) для предотвращения случайного данных утечек.</span><span class="sxs-lookup"><span data-stu-id="ea082-134">For Windows 10, configure Windows Information Protection (WIP) to prevent accidental data leaks.</span></span>
  
- <span data-ttu-id="ea082-135">Для управляемых устройств: [Создание защиты информации Windows (НЗП) с политикой регистрации с помощью Azure портала Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span><span class="sxs-lookup"><span data-stu-id="ea082-135">For managed devices: [Create a Windows Information Protection (WIP) with enrollment policy using the Azure portal for Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span></span>
    
- <span data-ttu-id="ea082-136">Отмена управляемых устройств: [Создание и развертывание политики защиты от приложения Windows сведения о защите (НЗП) с Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span><span class="sxs-lookup"><span data-stu-id="ea082-136">For un-managed devices: [Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span></span>
    
## <a name="step-7-manage-devices-with-intune"></a><span data-ttu-id="ea082-137">Шаг 7: Управление устройствами с Intune</span><span class="sxs-lookup"><span data-stu-id="ea082-137">Step 7: Manage devices with Intune</span></span>

<span data-ttu-id="ea082-p105">Управление устройствами позволяет убедиться в их работоспособности перед тем как разрешить доступ к ресурсам в вашей среде. Устройства на основе правил гарантировать, что злоумышленники не может получить доступ к ресурсам с неуправляемых устройств условного доступа.</span><span class="sxs-lookup"><span data-stu-id="ea082-p105">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment. Device based conditional access rules help ensure attackers can't gain access to your resources from unmanaged devices.</span></span>
  
- [<span data-ttu-id="ea082-140">Регистрация устройств для управления в Intune</span><span class="sxs-lookup"><span data-stu-id="ea082-140">Enroll devices for management in Intune</span></span>](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a><span data-ttu-id="ea082-141">Шаг 8: Настройка дополнительных политик Intune и правила условного доступа для вашей среды</span><span class="sxs-lookup"><span data-stu-id="ea082-141">Step 8: Configure additional Intune policies and conditional access rules for your environment</span></span>

<span data-ttu-id="ea082-142">Используйте эти рекомендуемые конфигурации в качестве отправной точки для масштаба предприятия или доступа сложных сценариев обеспечения безопасности.</span><span class="sxs-lookup"><span data-stu-id="ea082-142">Use these recommended configurations as a starting point for enterprise scale or sophisticated access security scenarios.</span></span>
  
- [<span data-ttu-id="ea082-143">Политики защиты электронной почты и конфигурации</span><span class="sxs-lookup"><span data-stu-id="ea082-143">Secure email policies and configurations</span></span>](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

