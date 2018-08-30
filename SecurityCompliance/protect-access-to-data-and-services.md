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
ms.openlocfilehash: e6e2d8d3ba6482d4b80593bd9e09d49d6120af80
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535107"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a>Защита доступа к данным и службам в Office 365

Защита доступа к данным Office 365 и службы важно защита от атаки через Интернет и защита от потери данных. Те же средства защиты может применяться к другим приложениям SaaS в вашей среде и опубликован даже для локальных приложений с Azure Active Directory приложения прокси.
  
## <a name="step-1-review-recommendations"></a>Шаг 1: Ознакомления с рекомендациями

Рекомендуемые возможности для защиты удостоверений и устройств, имеющих доступ к Office 365 и отличных от SaaS-служб и локальных приложений, которые опубликованы с помощью прокси приложения Azure AD.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Другие языки](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>Шаг 2: Настройка многофакторной проверкой Подлинности

Используйте следующие ресурсы для сориентироваться самостоятельно многофакторной проверкой Подлинности, решить, какую версию, а затем планировании и развертывании многофакторной проверкой Подлинности для вашей среды.
  
- [Что такое многофакторная проверка подлинности Azure?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Выберите решение многофакторная проверка подлинности Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Как получить многофакторная проверка подлинности Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Планирование для многофакторной проверки подлинности для развертываний Office 365](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Настройка многофакторной проверки подлинности для пользователей Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [Планирование места развертывания многофакторной проверкой Подлинности, облако или локальный](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Настройка параметров многофакторная проверка подлинности Azure](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>Шаг 3: Обеспечение многофакторной проверкой Подлинности с помощью правил условного доступа Azure AD

При использовании многофакторной проверкой Подлинности Azure AD создания правила условного доступа для поддержки требования многофакторной проверкой Подлинности для доступа к Office 365 и других приложений SaaS в вашей среде.
  
- [Условное доступа в Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-sharepoint-device-access-policies"></a>Шаг 4: Настройка политик доступа устройства SharePoint

Для защиты конфиденциальных секретная и регулируемого данных рекомендуется использовать политики доступа устройств для SharePoint Online и OneDrive для бизнеса. Готовится к выпуску — это возможность применения политик доступа устройств к сайтам отдельные группы.
  
- [Управление доступом с неуправляемых устройств](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-5-configure-app-and-data-protection-for-devices"></a>Шаг 5: Настройте приложения и защиты данных для устройств

Можно управлять приложениями на мобильных устройствах, независимо от того, ли участвуют устройств для мобильных устройств management. Это обеспечивает защиту от случайного утечки данных в Office 365, включая электронную почту и файлы.
  
- Для операций ввода-вывода и Android: [защитить данные приложения с помощью политики в отношении защиты приложений с помощью Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Для Windows 10 настройте сведения о защите Windows (НЗП) для предотвращения случайного данных утечек.
  
- Для управляемых устройств: [Создание защиты информации Windows (НЗП) с политикой регистрации с помощью Azure портала Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- Отмена управляемых устройств: [Создание и развертывание политики защиты от приложения Windows сведения о защите (НЗП) с Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-6-manage-devices-with-intune"></a>Шаг 6: Управление устройствами с Intune

Управление устройствами позволяет убедиться в их работоспособности перед тем как разрешить доступ к ресурсам в вашей среде. Устройства на основе правил гарантировать, что злоумышленники не может получить доступ к ресурсам с неуправляемых устройств условного доступа.
  
- [Регистрация устройств для управления в Intune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-7-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>Шаг 7: Настройка дополнительных политик Intune и правила условного доступа для вашей среды

Используйте эти рекомендуемые конфигурации в качестве отправной точки для масштаба предприятия или доступа сложных сценариев обеспечения безопасности.
  
- [Политики защиты электронной почты и конфигурации](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

