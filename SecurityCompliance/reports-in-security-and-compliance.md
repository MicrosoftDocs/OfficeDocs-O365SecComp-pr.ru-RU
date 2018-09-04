---
title: Отчеты о безопасности Office 365 &amp; центре соответствия требованиям
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/1/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.AuditingHelp
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 7acd33ce-1ec8-49fb-b625-43bac7b58c5a
description: 'Использование безопасности Office 365 &amp; центре соответствия требованиям для получения различных отчетов для вашей организации SharePoint Online и Exchange Online, а также Azure Active Directory отчетов.  '
ms.openlocfilehash: 0b633583e14a18c7cf579d10462cf41714397812
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534327"
---
# <a name="reports-in-the-office-365-security-amp-compliance-center"></a>Отчеты о безопасности Office 365 &amp; центре соответствия требованиям

Страница **Просмотр отчетов по** безопасности Office 365 &amp; центре соответствия требованиям для быстрого доступа к отчеты аудита для организаций, SharePoint Online и Exchange Online. Вы также можете открыть Azure Active Directory (AD) пользователя входа в отчетах, сообщает активность пользователей и аудита Azure AD входят на странице " **Просмотр отчетов** ". Это платной подписки Office 365 включает в себя бесплатная подписка на Microsoft Azure. При первом обращении к этих Azure отчетов необходимо завершить процесс однократного регистрации. 
  
> [!TIP]
> Для просмотра дополнительных отчетов об активности в организации Office 365, просмотрите [Отчеты об активности в центре администрирования Office 365](https://support.office.com/article/0d6dfb17-8582-4172-a9a9-aed798150263). 
  
 **Перед началом работы**
  
Необходимо иметь следующие разрешения для просмотра отчетов о безопасности &amp; центре соответствия требованиям.
  
- Необходимо назначить роль безопасности чтения в центре администрирования Exchange (EAC) для просмотра отчетов о безопасности &amp; центре соответствия требованиям. По умолчанию эта роль назначается группы ролей управления организацией и чтения безопасности в центре администрирования Exchange.
    
- Необходимо назначить роль управления соответствием требованиям защиты от потери данных в системы &amp; центре соответствия требованиям для просмотра отчетов защиты от потери данных (и политик DLP) в безопасности &amp; центре соответствия требованиям. По умолчанию эта роль назначается группы ролей администратора соответствия требованиям, управление организацией и права администратора безопасности в системы &amp; центре соответствия требованиям.
    
Кроме того необходимо назначить роль защиту от потери данных в центре администрирования Exchange для просмотра отчетов защиты от потери данных (и политик DLP) в центре администрирования Exchange. По умолчанию эта роль назначается группы ролей управления организацией и Управление соответствием требованиям в центре администрирования Exchange.
  
 **Чтобы открыть страницу представления отчетов в системы &amp; центре соответствия требованиям:**
  
1. Последовательно выберите пункты [https://protection.office.com/#/viewreports](https://protection.office.com/#/viewreports).
    
2. Войдите в Office 365 с помощью учетных данных для учетной записи пользователя в организации Office 365.
    
На странице " **Просмотр отчетов** " можно просмотреть следующие типы отчетов: 
  
- [Отчеты аудита в EOP](#auditing-reports)
- [Отчет о проверке контролирующий](#supervisory-review-report)
- [Отчеты службы защиты от потери данных](#data-loss-prevention-reports)
    
## <a name="auditing-reports"></a>Отчеты аудита

В следующей таблице описываются отчеты в разделе **Аудит** на странице " **Просмотр отчетов** " в параметрах безопасности &amp; центре соответствия требованиям. 
  
|**Отчет**|**Описание**|
|:-----|:-----|
|**Отчет по журналу аудита Office 365** <br/> |Можно выполнить поиск журнала аудита Office 365 для действия пользователя и администратора в организации Office 365. Отчет содержит записи активности пользователя и администратора в Exchange Online, SharePoint Online, OneDrive для бизнеса и Azure Active Directory, которая — это служба каталогов для Office 365. Дополнительные сведения можно [Поиск в журнале аудита безопасности Office 365 &amp; центре соответствия требованиям](search-the-audit-log-in-security-and-compliance.md).<br/> |
|**Отчеты Azure AD** <br/> |Для поиска нестандартный или подозрительные входа действия в организации Office 365, можно использовать вход и активности отчеты в Microsoft Azure. Можно также просмотреть события в журнале аудита Azure AD. Чтобы просмотреть отчеты в Azure, просто щелкните **Просмотр Azure AD отчетов**. Для получения дополнительных сведений см.<br/><br/>[Использование свободного подписки Azure Active Directory в Office 365](use-your-free-azure-ad-subscription-in-office-365.md). <br/> [Просмотр отчетов о доступа и использования](http://go.microsoft.com/fwlink/p/?LinkId=506902).  <br/> |
|**Отчеты об аудите Exchange** <br/> | Можно использовать функции проверки в Office 365 для отслеживания изменений, внесенных в Exchange Online конфигурации администраторами вашей организации. Изменения, внесенные в организацию Exchange Online с администратором центра обработки данных Майкрософт или делегированному администратору также регистрируются. Для Exchange Online аудита действий администратора ведения журнала включена по умолчанию, поэтому нет необходимости выполнять любые действия, чтобы включить эту возможность. Exchange Online также предоставляет почтового ящика журнала аудита для позволяют отслеживать доступ к почтовым ящикам никто, кроме владельца почтового ящика. Необходимо включить ведение журнала для каждого почтового ящика, который вы хотите отслеживать доступ не владельца аудита почтовых ящиков.<br/>  Ведение журнала аудита для администрирования и почтовых ящиков, можно запускать отчеты аудита для просмотра записей журнала аудита. Вы также можете экспортировать почтовых ящиков и администрирования журналы аудита, которые отправляются вы в течение 24 часов в XML-файл, подключенный к сообщении электронной почты.<br/><br/>Дополнительные сведения о экспорт журналов аудита см.  <br/><br/> [Экспорт журналов аудита почтовых ящиков](http://go.microsoft.com/fwlink/p/?LinkID=404104) <br/> [Просмотр и экспорт журнала аудита действий администратора центра обработки данных](http://go.microsoft.com/fwlink/p/?LinkId=404109) <br/> [Поиск изменений группы ролей или журналов аудита администратора](http://go.microsoft.com/fwlink/p/?LinkId=404105) <br/>   [Отчеты аудита Exchange](http://go.microsoft.com/fwlink/p/?LinkID=395232).  <br/> |
   
## <a name="supervisory-review-report"></a>Отчет о проверке контролирующий

В отчете контролирующий проверки можно просмотреть состояние всех политик контролирующий проверки в вашей организации. Дополнительные сведения можно [настроить контролирующий просмотрите политики для вашей организации](configure-supervision-policies.md).
  
## <a name="data-loss-prevention-reports"></a>Отчеты службы защиты от потери данных

Защита от потери данных (DLP) отчеты содержат сведения о политиках защиты от потери данных и правила, которые были применены к материалы содержат конфиденциальные данные в организации Office 365. Можно также настроить отчет для отображения сведений о действиях защиты от потери данных, основанные на политики предотвращения потери данных и правила. Дополнительные сведения можно [просмотреть отчет для предотвращения потери данных](view-the-dlp-reports.md).