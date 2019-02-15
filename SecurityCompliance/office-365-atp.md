---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/08/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Расширенная защита от угроз для Office 365 включает в себя логику подделки, безопасные ссылки, безопасные вложения, расширенные возможности защиты от фишинга и логику защиты от угроз.
ms.openlocfilehash: d78b37ca048187a298b6e083b54ad68b949638ef
ms.sourcegitcommit: 2af6c3e8a74995294a67429530af8f085e6ca136
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2019
ms.locfileid: "30051180"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

## <a name="overview-of-office-365-advanced-threat-protection"></a>Обзор расширенной защиты от угроз для Office 365

> [!IMPORTANT]
> Эта статья предназначена для корпоративных клиентов. Если вы являетесь домашним пользователем, который ищет сведения о безОпасных ссылках в Outlook, ознакомьтесь со статьей [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Office 365 Advanced Threat protection (ATP) помогает защитить организацию от вредоносных атак, выполнив следующие действия:
  
- Сканирование вложений электронной почты для вредоносных программ с [безопасными вложенияМи ATP](atp-safe-attachments.md)
    
- Проверка веб-адресов (URL-адресов) в сообщениях электронной почты и документах Office с помощью [безопасных ссылок ATP](atp-safe-links.md)
    
- Определение и Блокировка вредоносных файлов в Интернет-библиотеках с помощью [ATP для SharePoint, OneDrive и Microsoft Teams](atp-for-spo-odb-and-teams.md)
    
- Проверка сообщений электронной почты на несанкционированную подмену с помощью [аналитики подделки](learn-about-spoof-intelligence.md)
    
- Обнаружение, когда кто-то пытается олицетворять пользователей и пользовательские домены вашей организации с [функциями защиты от фишинга ATP в Office 365](atp-anti-phishing.md)
    
**Защита с помощью Office 365 ATP определяется политиками, которые Группа безопасности Организации определяет для безопасных ссылок, безопасных вложений и защиты от фишинга**. Важно определить политики, а также регулярно просматривать и изменять эти политики, чтобы они не превышали актуальности и применялись к преимуществам новых функций, добавляемых в службу. 

[Доступны отчеты](view-reports-for-atp.md) , в которых показано, как работает ATP для вашей организации. В этих отчетах также могут отображаться области, в которых может потребоваться просмотреть и обновить политики. Если у вас есть файлы, помеченные как вредоносные программы, которые не должны быть, или файлы, которые вы хотели бы проверить в Майкрософт, вы можете [передать файл в корпорацию Майкрософт для анализа](#submit-a-suspicious-file-to-microsoft-for-analysis).

## <a name="new-features-are-continually-being-added-to-atp"></a>Новые функции постоянно добавляются в ATP.

Мы продолжаем добавлять новые функции в Office 365, включающие ATP. Ниже приведен список нескольких новых функций, некоторые из которых вызывают политику ATP для просмотра и обновления. Для получения дополнительных сведений о новых возможностях, поступающих в ATP (или Microsoft 365 в целом), посетите [план Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap?filters=O365).


|Обновления функций  |Элементы Action  |
|---------|---------|
|Начиная с 2019 февраля и выходящиеся в течение нескольких месяцев в течение нескольких месяцев, в ATP добавляются возможности аналитики угроз. Кроме того, если у вашей организации еще нет ATP, вы получите новые возможности, в том числе ATP (план 1) и ATP (план 2). Чтобы узнать больше, ознакомьтесь со статьями [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). |ИзУчите подписку Организации и при необходимости [купите или](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/buy-or-edit-an-add-on)изменяйте надстройку.  |
|Начиная с 2018 октября и выполнив эти несколько месяцев, когда люди используют Outlook или веб-приложение Outlook (OWA), безопасные ссылки ATP отображают исходные URL-адреса, а не переписывают их. (Мы вызываем эту собственную визуализацию ссылок.)<br>Если для вашей организации доступна собственная визуализация ссылок, эта функция будет работать в Outlook 365 ("нажми и работай") и OWA.|Нет         |
|Начиная с сентября 2018, [страницы предупреждений Office 365 ATP](atp-safe-links-warning-pages.md) — новая цветовая схема, дополнительные сведения и возможность перехода на сайт, несмотря на заданные предупреждения и рекомендации. |Нет         |
|Начиная со второй половины 2018, защита "безопасные ссылки ATP" расширена для применения к URL-адресам в Office Online (Word Online, Excel Online, PowerPoint Online и OneNote Online) и Office 365 профессиональный плюс на компьютере Mac.   |[Просмотр и изменение политик безОпасных ссылок ATP](set-up-atp-safe-links-policies.md)  |
|Начиная с опоздания, Май [](quarantine-email-messages.md) 2018, функции карантина &amp; в центре безопасности соответствуют расширению [ATP для SharePoint Online, OneDrive для бизнеса и Microsoft Teams](atp-for-spo-odb-and-teams.md). |[Просмотр и изменение политик безОпасных вложений ATP](set-up-atp-safe-attachments-policies.md) |
|Начиная с 2018 марта Recovery Links Protection расширяется для применения к электронной почте, отправляемой между пользователями в Организации. |[Просмотр и изменение политик безОпасных ссылок ATP](set-up-atp-safe-links-policies.md) |
|Начиная с октября 2017, защита ссылок ATP расширена для применения к URL-адресам в сообщениях электронной почты, а также URL-адресам в документах Office 365 профессиональный плюс, таких как Word, Excel, PowerPoint и Visio в Windows, а также для приложений Office на устройствах с iOS и Android.  |Убедитесь, что используется [современная проверка подлинности для Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016) . |

## <a name="get-office-365-atp"></a>Получение пакета Office 365 ATP

Office 365 ATP входит в подписки, такие как [microsoft 365 корпоративный](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 бизнес](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise и Office 365 образования A5. Если в вашей организации есть подписка на Office 365, не включающая в себя Office 365 ATP, вы можете приобрести ATP как надстройку. Дополнительные сведения см. в статье [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 

## <a name="define-policies-for-atp"></a>Определение политик для ATP

Для определения (или изменения) политик ATP необходимо быть назначена одна из ролей, описанных в следующей таблице.

|Роль  |Где/как назначено  |
|---------|---------|
|Глобальный администратор Office 365 |Пользователь, который подписывается на приобретение Office 365, по умолчанию является глобальным администратором. (Чтобы узнать больше, ознакомьтесь со статьей [о ролях администратора Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|администратор безопасности (Security Administrator). |Центр администрирования Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Управление организацией Exchange Online |Центр администрирования Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>или <br>  Командлеты PowerShell (см. [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |

> [!TIP]
> Дополнительные сведения о ролях и разрешениях приведены [в разделе разрешения в центре безопасности &amp; и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).

Существует несколько видов политик ATP, которые необходимо определить и периодически просматривать.

1. **[Настройте антифишинговые политики ATP в Office 365](set-up-anti-phishing-policies.md)** , включая атаки на основе олицетворения, чтобы защититься от злоумышленников, которые отправляют сообщения электронной почты от доверенных пользователей или доменов. 

2. **[Настройте политики безопасных ссылок ATP в Office 365](set-up-atp-safe-links-policies.md)** , включая список [пользовательских заблокированных URL-адресов](set-up-a-custom-blocked-urls-list-wtih-atp.md) вашей организации и [Пользовательский список URL-адресов "не переопределять"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md).
    
3. **[Настройте политики безопасных вложенИЙ ATP в Office 365](set-up-atp-safe-attachments-policies.md)** и выберите один из нескольких вариантов, таких как [Динамическая Доставка и предварительный просмотр](dynamic-delivery-and-previewing.md).
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a>Узнайте, как работает ATP, просмотрев отчеты

После выполнения политик ATP можно получить доступ к отчетам, показывающим, как работает служба. в центре безопасности Office 365 Security _амп_ откройте**панель мониторинга** **отчетов** > .

[![Информационная &amp; панель центра соответствия требованиям безопасности поможет вам узнать, где работает Расширенная защита от угроз](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)
  
1. Как глобальный администратор Office 365, администратор безопасности или средство чтения безопасности, перейдите на [https://protection.office.com](https://protection.office.com) страницу и войдите в нее.
    
2. Перейдите на **** > **панель мониторинга**отчетов. (Чтобы получить справку по этим отчетам, ознакомьтесь со статьей [Просмотр отчетов для Advanced Threat protection](view-reports-for-atp.md).)
    
3. При необходимости внесите изменения в политики безопасности. Чтобы получить помощь по этой статье, ознакомьтесь со следующими материалами:
    - [Политики защиты от фишинга ATP](set-up-anti-phishing-policies.md)
    - [Политики безОпасных ссылок ATP](set-up-atp-safe-links-policies.md)
    - [Политики безОпасных вложений ATP](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a>Передача подозрительных файлов в корпорацию Майкрософт для анализа

- Если вы получаете подозрительный файл вредоносной программы, вы можете передать его в корпорацию Майкрософт для анализа. Посетите [портал отправки системы безопасности для защитника Windows](https://go.microsoft.com/fwlink/?linkid=857185).

- Если вы получили сообщение электронной почты (с вложением или без него), которое вы хотите отправить в корпорацию Майкрософт для анализа, используйте [надстройку Report Message](enable-the-report-message-add-in.md). 
  

