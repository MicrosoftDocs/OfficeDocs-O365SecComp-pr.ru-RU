---
title: Настройка службы управления правами Azure для шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: Предыдущие версии шифрования сообщений Office 365, зависит от Microsoft Azure Rights Management (ранее называлась управления правами Active Directory Windows Azure).
ms.openlocfilehash: f8759da8628d4c78fe5409f5c47e3fc2b3e9484e
ms.sourcegitcommit: c05076501dfe118e575998ecfc08ad69d13c8abc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25853074"
---
# <a name="this-article-applies-to-the-previous-version-of-ome"></a>Эта статья относится к предыдущей версии OME
Новые возможности OME еще еще не перемещены организации Office 365, но вы уже развернули OME, сведения в этой статье относятся для вашей организации. Корпорация Майкрософт рекомендует, чтобы сделать план для перемещения новых возможностей OME, как только целесообразно для вашей организации. Сведения содержатся в разделе [Set up новые возможности шифрования сообщений Office 365](set-up-new-message-encryption-capabilities.md). Если вы хотите узнать больше о новых возможностях сначала, ознакомьтесь со [Шифрования сообщений Office 365](ome.md). Далее в этой статье относится к OME поведение перед выпуском новых возможностей OME.

# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a>Настройка управления правами Azure для предыдущей версии шифрования сообщений Office 365

В этом разделе описаны действия, необходимые для активации и задайте его копирования Azure управления правами, частью защита информации Azure, для использования с помощью шифрования сообщений Office 365 (OME).
  
## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a>Необходимые условия для использования предыдущей версии шифрования сообщений Office 365
<a name="warmprereqs"> </a>

Office 365 Message Encryption (OME), включая IRM, зависит от службы управления правами Azure (Azure RMS). Службы управления правами Azure — это технология защиты, защита информации Azure. Чтобы использовать OME, организации Office 365 необходимо включить подписка на Exchange Online или Exchange Online Protection, в свою очередь, включает в себя подписка на службу управления правами Azure.
  
- Если вы не знаете подписка включает, ознакомьтесь со описания [политики сообщения, восстановление и соответствие требованиям](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx)службы Exchange Online.
    
- Если у вас нет подписки на службы управления правами Azure для Exchange Online или Exchange Online Protection, необходимо приобрести подписки и активации сначала.
    
    Сведения о приобретении подписка на службу управления правами Azure можно [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). В следующем разделе приводится сведения об активации Azure Rights Management.
    
- Если у вас есть Azure Rights Management, но не настроена для Exchange Online или Exchange Online Protection, в этой статье объясняется, как включить службу управления правами Azure и затем описываются лучший способ настройки OME для работы с Azure Rights Management.
    
- Если вы уже установлено OME для управления правами Azure для Exchange Online или Exchange Online Protection, в зависимости от того, как настроить его, можно приступить к работе с OME и новые возможности немедленно. В этой статье объясняется, как определить, если настройки OME правильно, что делать, если необходимо изменить настройки, и что произойдет, если не требуется изменить настройку. Например чтобы использовать новые возможности, необходимо использовать службы управления правами Azure с OME. Новые возможности нельзя использовать вместе с локальной Active Directory службы управления правами.
    
## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a>Активация службы управления правами Azure для предыдущей версии OME в Office 365
<a name="activatewarm"> </a>

Вам потребуется активация службы управления правами Azure, чтобы пользователи в вашей организации можно применить защиту сведения для сообщения, отправленные и открытие сообщений и файлов, защищенных службой управления правами Azure. [Активация службы управления правами Azure](https://go.microsoft.com/fwlink/p/?LinkId=525775)инструкции, см. После выполнения активации, вернитесь сюда и продолжите задач, описанных в этой статье.
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a>Настройка предыдущей версии OME для использования службы управления правами Azure путем импорта доверенные домены публикации (доверенных доменов публикации)
<a name="importTPDs"> </a>

Доверенный — это XML-файл, который содержит сведения о параметрах управления правами вашей организации. Например доверенный домен публикации содержит сведения об серверный сертификат лицензиара (SLC), используемый для подписи и шифрования сертификатов и лицензий, URL-адреса, используемые для лицензирования и публикации и т. д. Импортировать доверенный домен публикации в организации Office 365 с помощью Windows PowerShell.
  
> [!IMPORTANT]
> Ранее можно выбрать для импорта доверенных доменов публикации из службы управления правами Active Directory (AD RMS) в организации Office 365. Тем не менее, при этом будет препятствовать с помощью новых возможностей OME и не рекомендуется. Если Office 365 организации в настоящий момент настроена таким образом, корпорация Майкрософт рекомендует создания плана для переноса из вашей локальной Active Directory службы управления правами для защиты информации Azure на основе облака. Для получения дополнительных сведений см [AD RMS для защиты информации Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Вы не сможете использовать новые возможности OME до завершения переноса для защиты информации Azure. 
  
 **Для импорта доверенных доменов публикации из службы управления правами Azure**
  
1. [Подключение к Exchange Online с помощью удаленной оболочки PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Выберите общий доступ к ключ URL-адрес, соответствующий географическое положение организации Office 365:
    
|**Расположение**|**Ключ, общий доступ к URL-адрес расположения**|
|:-----|:-----|
|Северная Америка  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Европейский Союз  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Азия  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Южная Америка  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|Office 365 для государственных учреждений (облако сообщества госучреждений)  <br/> Это расположение общего доступа к ключ службы управления правами зарезервирован для клиентов, которые приобрели Office 365 для государственных учреждений.  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. Настройка расположения совместного использования ключа, выполнив командлет [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) следующим образом: 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    Например, чтобы настроить Если организация находится в Северной Америке расположение для обмена ключами:
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. Выполните командлет [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) с параметром - RMSOnline, чтобы импортировать доверенный домен публикации из службы управления правами Azure: 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    Где *TPDName* — это имя будет использоваться для доверенный домен публикации. Например «Contoso Северной Америки доверенный домен публикации». 
    
5. Чтобы убедиться, что вы успешно настроили организации Office 365 с помощью службы управления правами Azure, запустите командлет [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) с параметром - RMSOnline следующим образом: 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    Помимо прочего этот командлет проверяет возможность доступа с помощью службы управления правами Azure, файлы для загрузки доверенный домен публикации и проверяет его допустимость.
    
6. Выполните командлет [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) , как показано ниже, чтобы отключить службу управления правами Azure шаблоны, доступные в Outlook в Outlook и веб: 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. Выполните командлет [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) следующим образом для включения службы управления правами Azure для вашей организации электронной почты на основе облака и настроить его для использования службы управления правами Azure для шифрования сообщений Office 365: 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. Чтобы убедиться, что вы успешно импортировали TPD и включена служба управления правами Azure, используйте командлет Test-IRMConfiguration для тестирования функции управления правами Azure. Дополнительные сведения см «В примере 1» в [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a>У меня есть предыдущей версии OME настройку с помощью управления правами Active Directory Azure защита информации, что делать?
<a name="importTPDs"> </a>

Можно продолжить использование существующих правил потока почты шифрования сообщений Office 365 с помощью управления правами Active Directory, но не могут использовать новые возможности OME или настроить. Вместо этого необходимо перенести защита информации Azure. Сведения о миграции и это означает для вашей организации см [AD RMS для защиты информации Azure](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).
  
## <a name="next-steps"></a>Дальнейшие действия
<a name="importTPDs"> </a>

После выполнения программы установки службы управления правами Azure, если вы хотите включить новые возможности OME, просматривать [настроить новые возможности шифрования сообщений Office 365, построенные защита информации Azure.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)
  
После настройки вашей организации для использования новых возможностей OME, вы готовы к [Определение правил поток обработки почты для защиты сообщений электронной почты с новыми возможностями OME](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="related-topics"></a>См. также:
<a name="importTPDs"> </a>

[Шифрование в Office 365](encryption.md)
  
[Технические сведения о шифровании в Office 365](technical-reference-details-about-encryption.md)
  
[Что такое служба управления правами Azure?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  

