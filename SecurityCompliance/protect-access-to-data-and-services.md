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
# <a name="protect-access-to-data-and-services-in-office-365"></a>Защита доступа к данным и службам в Office 365

Защита доступа к данным и службам Office 365 важна для защиты от кибератак-атак и защиты от потери данных. Одни и те же защиты можно применять к другим приложениям SaaS в среде и даже к локальным приложениям, публикуемым с помощью прокси-сервера приложения Azure Active Directory.
  
## <a name="step-1-review-recommendations"></a>Шаг 1: проверка рекомендаций

Рекомендуемые возможности для защиты удостоверений и устройств, имеющих доступ к Office 365 и отличных от SaaS-служб и локальных приложений, которые опубликованы с помощью прокси приложения Azure AD.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Другие языки](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>Шаг 2: Настройка MFA

Используйте эти ресурсы для ориентации себя на MFA, выберите нужную версию, а затем запланируйте и разверните MFA для своей среды.
  
- [Что такое многофакторная проверка подлинности Azure?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Выбор решения многофакторной проверки подлинности Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Получение многофакторной проверки подлинности Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Планирование многофакторной проверки подлинности для развертываний Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Настройка многофакторной проверки подлинности для пользователей Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [Планирование развертывания MFA, облака или локальной](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Настройка параметров многофакторной проверки подлинности Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>Шаг 3: принудительное применение MFA с правилами условного доступа Azure AD

Если вы используете Azure AD для Azure, создайте правило условного доступа, чтобы оно требовало использования MFA для доступа к Office 365 и другим приложениям SaaS в вашей среде.
  
- [Условный доступ в Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>Шаг 4: Настройка управления привилегированным доступом

Управление привилегированным доступом позволяет осуществлять детализированный контроль над задачами привилегированного администрирования в Office 365.  Это помогает защитить организацию от нарушений, которые могут использовать существующие привилегированные учетные записи администраторов с ограниченным доступом к конфиденциальным данным или к критическим параметрам конфигурации.

- [Общие сведения об управлении привилегированным доступом](privileged-access-management-overview.md)
- [Настройка управления привилегированным доступом](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>Шаг 5: Настройка политик доступа к устройствам SharePoint

Политики доступа к устройствам для SharePoint Online и OneDrive для бизнеса рекомендуются для защиты конфиденциальных, классифицированных и регулируемых данных. Появилась возможность применять политики доступа к устройствам к отдельным сайтам групп.
  
- [Управление доступом с неуправляемых устройств](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>Шаг 6: Настройка защиты приложений и данных для устройств

Вы можете управлять приложениями на мобильных устройствах независимо от того, зарегистрированы ли устройства для управления мобильными устройствами. Это обеспечивает защиту от случайного утечки данных в Office 365, в том числе почты и файлов.
  
- Для iOS и Android: [Защита данных приложений с помощью политик защиты приложений с помощью Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Для Windows 10 настройте Windows Information Protection (WIP), чтобы предотвратить случайные утечки данных.
  
- Для управляемых устройств: [Создание Windows Information Protection (WIP) с политикой регистрации с помощью портала Azure для Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- Для неуправляемых устройств: [Создание и развертывание политики защиты приложений Windows Information Protection (WIP) с помощью Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>Шаг 7: Управление устройствами с помощью Intune

Управление устройствами позволяет убедиться, что они являются работоспособными и совместимыми, прежде чем разрешить им доступ к ресурсам в вашей среде. Правила условного доступа на основе устройств гарантируют, что злоумышленники не смогут получить доступ к ресурсам из неуправляемых устройств.
  
- [Регистрация устройств для управления в Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>Шаг 8: Настройка дополнительных политик Intune и правил условного доступа для среды

Используйте эти Рекомендуемые конфигурации в качестве отправной точки для сценариев масштаба предприятия или сложных сценариев безопасности доступа.
  
- [Безопасные политики электронной почты и конфигурации](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

