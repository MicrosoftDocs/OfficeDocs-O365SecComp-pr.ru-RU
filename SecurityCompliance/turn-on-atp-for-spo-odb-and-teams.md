---
title: Включить ATP Office 365 для SharePoint, OneDrive и группами Майкрософт
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection: M365-security-compliance
description: Узнайте, как включить ATP для SharePoint, OneDrive и групп, включая способ настройки оповещения об обнаруженных файлах.
ms.openlocfilehash: 8c63110baf391fd727e296f34361047b4b67b0cb
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995340"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Включить ATP Office 365 для SharePoint, OneDrive и группами Майкрософт

[Office 365 ATP для SharePoint, OneDrive и группами Майкрософт](atp-for-spo-odb-and-teams.md) защищает вашей организации от случайно совместное использование вредоносных файлов. При обнаружении вредоносных файлов, этот файл блокируется, чтобы никто можно открыть, скопируйте, перемещение или совместно использовать до дополнительных действий группой безопасности в организации. Ознакомьтесь с этой статьей, чтобы включить ATP для SharePoint, OneDrive и рабочих групп, настроить оповещения для уведомления об обнаруженных файлов и выполните следующие действия. 
  
(Или изменение) ATP политик, вам должна быть назначена одна из ролей описаны в следующей таблице:

|Роль  |Где и как назначен  |
|---------|---------|
|Глобальный администратор Office 365 |Человека, который регистрируется приобрести Office 365 — это глобального администратора по умолчанию. ( [Роли администраторов об Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) для получения дополнительных сведений см.)         |
|администратор безопасности (Security Administrator). |Центр администрирования Azure Active Directory ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Управление Exchange Online организацией |Центр администрирования Exchange ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>или <br>  Командлеты PowerShell (см. [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Включение ATP для SharePoint, OneDrive и Microsoft Teams

**Перед началом этой процедуры убедитесь в том, что ведение журнала аудита уже включен для вашей среды Office 365**. Обычно это делается пользователем, обладающим журналы аудита роли, назначенные в Exchange Online. Дополнительные сведения можно [Включить Office 365 проводить аудит операций поиска журнала включено или отключено](turn-audit-log-search-on-or-off.md).
  
1. Последовательно выберите пункты [https://protection.office.com](https://protection.office.com)и войдите с учетной записи рабочего или школы.
    
2. В Office 365 безопасность &amp; центре соответствия требованиям в левой области навигации, в разделе **Управление угроз**, выберите **политику** \> **Безопасные вложения**. <br/>![В разделе Безопасность &amp; центре соответствия требованиям, выберите Threat management \> политики](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. Выберите **Включить ATP для SharePoint, OneDrive и группами Майкрософт**.<br/>![Включение расширенной защитой для SharePoint Online, OneDrive для бизнеса и группами Майкрософт](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. Нажмите кнопку **Сохранить**.
    
5. Просмотрите (и, отредактируйте) [политики безопасные вложения](set-up-atp-safe-attachments-policies.md) и [политики безопасных ссылки](set-up-atp-safe-links-policies.md)вашей организации.
    
6. (Рекомендуется) Как глобальный администратор или администратор SharePoint Online, выполните командлет **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** с параметром **DisallowInfectedFileDownload** установлено значение *true*. <br/>
      - Установка для параметра в *значение true,* блокирует все действия (за исключением Delete) для обнаруженных файлы. Пользователи не могут открыть, перемещение, копирование или общего доступа к файлам вредоносным.
      - Установка для параметра значение *false* блокирует все действия, за исключением Delete и загрузки. Люди могут выбрать для принятия риск и загрузите файл вредоносным.  
   
7. Разрешить до 30 минут для применения изменений для распространения для всех центров обработки данных Office 365.
    
8. (Рекомендуется) Перейдите к настройке оповещения об обнаруженных файлах.
    
Чтобы подробнее узнать об использовании PowerShell с помощью Office 365, обратитесь к разделу [Управление Office 365 с помощью PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). 

Чтобы узнать больше о взаимодействие с пользователем, при обнаружении файл как вредоносных, видеть [что делать при обнаружении вредоносных файлов в SharePoint Online, OneDrive или группами Майкрософт](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2). 
  
## <a name="set-up-alerts-for-detected-files"></a>Настройка оповещений для обнаруженных файлов

Чтобы получать уведомления, когда файл в SharePoint Online, OneDrive для бизнеса, или группами Майкрософт было определено как вредоносных, можно настроить оповещения.
  
1. В [безопасности Office 365 &amp; центре соответствия требованиям](https://protection.office.com), выберите **оповещения** \> **Управление оповещениями**.
    
2. Выберите **новую политику оповещения**.
    
3. Укажите имя для оповещения. Например вы введите вредоносных файлов в библиотеках.
    
4. Введите описание для оповещения. Например можно ввести уведомляет администраторов при обнаружении вредоносных файлов в SharePoint Online, OneDrive или группами Майкрософт.
    
5. В разделе **Отправить это уведомление, когда...** выполните следующие действия. 
    
    а. в списке **действий** выберите **вредоносные программы обнаружены в файл**.
    
    б. не заполняйте поле **Пользователи** . 
    
6. В разделе **Отправить это оповещение, чтобы...** выберите одного или нескольких глобальных администраторов, администраторов безопасности или читатели безопасности, которые будут получать уведомления при обнаружении вредоносных файлов. 
    
7. Нажмите кнопку **Сохранить**.
    
Чтобы узнать больше о оповещения, обратитесь к разделу [Создание оповещений активности безопасности Office 365 &amp; центре соответствия требованиям](create-activity-alerts.md). 
  
## <a name="next-steps"></a>Дальнейшие действия

1. [Просмотр сведений о вредоносных файлов, обнаруженных в SharePoint, OneDrive или группами Майкрософт](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [Управление сообщений на карантине и файлы с правами администратора в Office 365](manage-quarantined-messages-and-files.md)
    

  

