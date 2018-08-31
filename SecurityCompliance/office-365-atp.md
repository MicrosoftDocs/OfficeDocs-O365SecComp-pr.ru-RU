---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/1/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Office 365 расширенной защитой включает в себя подделка аналитики, безопасных ссылок, безопасные вложения и расширенные возможности фишинга. Расширенные защиту от угроз также расширяемый для файлов в SharePoint Online, OneDrive для бизнеса и группами Майкрософт.
ms.openlocfilehash: dbf604dfc6367ac225e57158e6b784952c081773
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534884"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

Office 365 расширенного угроз защиты анализа помогает защитить организацию от злонамеренных атак с:
  
- Проверка вложений электронной почты с [Вложениями безопасных ATP](atp-safe-attachments.md)
    
- Сканирования веб-адресов (URL-адреса) в документах Office со [Ссылками безопасных анализа](atp-safe-links.md) и сообщений электронной почты
    
- Идентификации и блокировки вредоносных файлов в библиотеках online с помощью [ПАКЕТА для SharePoint, OneDrive и группами Майкрософт](atp-for-spo-odb-and-teams.md)
    
- Проверка сообщений электронной почты для несанкционированного Спуфинг с [Подделка аналитики](learn-about-spoof-intelligence.md)
    
- Определение, когда кто-то пытается олицетворять пользователей и пользовательских доменов вашей организации с [возможностями фишинга ATP в Office 365](atp-anti-phishing.md)
    
Защита через Office 365 ATP определяет, какие политики, которые группа безопасности вашей организации определяет для безопасных ссылок, безопасные вложения и фишинга. [Отчеты доступны](view-reports-for-atp.md) для отображения как работа ATP для вашей организации. А также можно [Отправить подозрительных файлов в корпорацию Майкрософт для анализа](office-365-atp.md#submitlalware).
  
> [!IMPORTANT]
> Office 365 ATP включен в подписки, Office 365 Enterprise E5 и Office 365 Education A5 и, по состоянию на 30 апреля 2018, также [функции обеспечения безопасности Microsoft 365 для бизнеса](https://support.office.com/article/c123694a-1efb-459e-a8d5-2187975373dc). Если в вашей организации есть подписка на Office 365, которая не включает Office 365 ATP, вы можете приобрести ATP потенциально как дополнительный компонент. Дополнительные сведения см в [Office 365 расширенного угроз защиты описание службы](https://technet.microsoft.com/library/exchange-online-advanced-threat-protection-service-description.aspx). 
      
## <a name="get-office-365-atp"></a>Получение ПАКЕТА Office 365

1. Как администратор глобальной или безопасности, перейдите к [https://portal.office.com](https://portal.office.com) и войдите с работы или школы учетную запись на Office 365. 
    
2. Выберите пункты **Администрирование** \> **выставления счетов** для просмотра текущего подписка включает. 
    
    ![Как глобальный администратор, войдите в систему в portal.office.com и перейдите к разделу администратор \> по выставлению счетов](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)
  
3. Если отображаются **Office 365 Enterprise E5**, **Office 365 Education A5**или **Microsoft 365 Business**вашей организации есть анализа. 
    
    Если отображаются разные подписки, например **Office 365 для предприятий E3** или **Office 365 корпоративный E1**, рассмотрите возможность добавления анализа. Для этого нажмите кнопку **+ Добавить подписку**.
    
После получения ATP следующим шагом является для группы безопасности для определения политик для защиты [Безопасных ссылок](atp-safe-links.md), [Безопасные вложения](atp-safe-attachments.md)и [фишинга](set-up-atp-anti-phishing-policies.md) . 
  
[Что необходимо сделать?](office-365-atp.md#TOC)
  
## <a name="define-policies-for-atp"></a>Определение политик для анализа

- **[Настройка политик ATP безопасных ссылок в Office 365](set-up-atp-safe-links-policies.md)** включая [Настраиваемый список заблокированных URL-адреса](set-up-a-custom-blocked-urls-list-wtih-atp.md) и [Настраиваемый список «Не rewrite» URL-адреса](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) вашей организации
    
- **[Настройка безопасных вложений ATP политики в Office 365](set-up-atp-safe-attachments-policies.md)** , который может содержать [динамические доставки и предварительный просмотр](dynamic-delivery-and-previewing.md)
    
- **[Настройка политик фишинга ATP в Office 365](set-up-atp-anti-phishing-policies.md)** включая олицетворения-атак защита от злоумышленников отправлять сообщения электронной почты, который выглядит от доверенных пользователей или доменов 
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Как работает ATP отчеты

После политиках ATP отчеты доступны для отображения как работа службы.

[![Безопасность &amp; панели мониторинга в центре соответствия требованиям, которые помогут посмотреть, где работает расширенного защиту от угроз](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Убедитесь в том, что вы являетесь глобального администратора, администратора безопасности или чтения безопасности Office 365. (Увидеть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).)
    
2. [Просмотр отчетов для расширенного защиту от угроз и Exchange Online Protection](view-reports-for-atp.md).
    
3. При необходимости, внести изменения в политиках безопасности. Воспользуйтесь следующими ресурсами:
    
  - [Безопасные ссылки ATP политики в Office 365](set-up-atp-safe-links-policies.md)
    
  - [Безопасные вложения ATP политики в Office 365](set-up-atp-safe-attachments-policies.md)
    
  - [Пакет анализа фишинга политики в Office 365](set-up-atp-anti-phishing-policies.md)
    
[Что необходимо сделать?](office-365-atp.md)
  
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Отправка подозрительных файлов в корпорацию Майкрософт для анализа

Если файл, который может быть вредоносных программ, можно отправить этот файл в корпорацию Майкрософт для анализа. Посетите [портал отправки аналитики безопасности Защитника Windows](https://go.microsoft.com/fwlink/?linkid=857185).
  
## <a name="related-topics"></a>Статьи по теме

[Обзор системы безопасности Office 365 &amp; центре соответствия требованиям](https://support.office.com/article/a5f2fd18-b029-4257-b5a8-ae83e7768c85)
  
[Просмотр отчетов для расширенного защиту от угроз](view-reports-for-atp.md)
  
[Угроз управления безопасности Office 365 &amp; центре соответствия требованиям](threat-management.md)
  

