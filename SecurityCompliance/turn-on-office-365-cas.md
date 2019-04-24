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
# <a name="turn-on-office-365-cloud-app-security"></a>Включение Cloud App Security для Office 365
  
|Ознакомительная версия * *\>**|Планирование * *\>**|Развертывание * *\>**|Использование * * * *|
|:-----|:-----|:-----|:-----|
|[Начало оценки](office-365-cas-overview.md) <br/> |[Начало планирования](get-ready-for-office-365-cas.md) <br/> |Вот что вам!  <br/> [Следующий шаг](activity-policies-and-alerts.md) <br/> |[Начало использования](utilization-activities-for-ocas.md) <br/> |
  
## <a name="turn-on-office-365-cloud-app-security"></a>Включение Cloud App Security для Office 365

> [!IMPORTANT]
> Для выполнения следующей задачи необходимо быть глобальным администратором или администратором безопасности. Чтобы узнать больше, ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md). Для правильной работы Office 365 Cloud App Security **необходимо включить ведение журнала аудита** для среды Office 365. Дополнительную информацию можно узнать [в статье Включение и отключение поиска в журнале аудита Office 365](turn-audit-log-search-on-or-off.md). 
  
1. В качестве глобального администратора или администратора безопасности войдите в рабочую [https://protection.office.com](https://security.microsoft.com) или учебную учетную запись Office 365, используя рабочую или учебную учетную запись. (Откроется центр соответствия требованиям безопасности &amp; .) 
    
2. Перейдите к разделу **оповещения** \> **Управление расширенными оповещениями**.
    
3. Выберите **включить Office 365 Cloud App Security**.
    
4. Выберите **Перейти к Office 365 Cloud App Security**.<br/>![В центре безопасности &amp; и соответствия требованиям выберите Управление расширенными оповещениями для перехода к Office 365 Cloud App Security.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)<br/>Откроется портал Office 365 Cloud App Security, где можно просматривать отчеты, а также создавать и изменять политики.

После включения безопасности облачных приложений Office 365 вы можете перейти на портал Cloud App Security, посетив [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) и войдя в систему.
    
> [!NOTE]
> Когда вы включаете Office 365 Cloud App Security, аудит сведений об учетных записях пользователей Office 365 и действий пользователей передается в [Microsoft Cloud App Security](https://aka.ms/whatiscas). Это позволяет Office 365 предоставлять расширенные оповещения, фильтрацию и другие функции для получения сведений и выполнения действий по подозрительным действиям. 
  
## <a name="next-steps"></a>Дальнейшие действия

- [Политики действий](activity-policies-and-alerts.md)
    
- [Политики обнаружения аномалий](anomaly-detection-policies-in-ocas.md)
    
- [Интеграция сервера SIEM](integrate-your-siem-server-with-office-365-cas.md)
    
- [Группировка IP-адресов для упрощения управления](group-your-ip-addresses-in-ocas.md)
    

