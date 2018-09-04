---
title: Шифрование в Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/3/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 0a322724-08ca-43db-b69a-afbfa20484cd
description: С помощью Office 365 контента шифрования статических и во время передачи, с помощью надежного шифрования, протоколы и технологиях, доступных. Обзор шифрования в Office 365.
ms.openlocfilehash: e5c21cf456f9ccca2393b8985dd47e34745902cf
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534856"
---
# <a name="encryption-in-office-365"></a>Шифрование в Office 365

Шифрование является важной частью стратегии файл защиты и сведения о защите. Прочитайте данную статью Обзор шифрования, используемый для всех версий Office 365 и получение справки с помощью шифрования задачи от настройки шифрования для вашей организации для защиты паролем с документами Office.
  
- Если вы ищете сведения о сертификатах и технологии, такие как TLS, ознакомиться с [подробными сведениями Техническая справка о шифровании в Office 365](technical-reference-details-about-encryption.md).
    
- Если вы ищете информацию о том, как настроить или шифрование для вашей организации, просмотрите [шифрование в Office 365 для предприятия](set-up-encryption.md).
    
## <a name="what-is-encryption-and-how-does-it-work-in-office-365"></a>Что такое шифрования, и как это работает в Office 365?

На высоком уровне шифрования — это процесс кодирования данных (называется открытым текстом) в зашифрованного текста, который не может использоваться с пользователей или компьютеров, до тех пор, пока не расшифрован зашифрованного текста. Расшифровка необходим ключ шифрования, для которого настроено только авторизованным пользователям. Шифрование гарантирует, что только авторизованные получатели могут расшифровки содержимого, такие как сообщения электронной почты и файлы.
  
Шифрование сам по себе не запрещает контент, например файлы, сообщения электронной почты, элементы календаря и т. д начало в руки. Шифрование является частью стратегии защиты увеличенное сведения для вашей организации. С помощью шифрования, можно обеспечить существует возможность, что только тех, кто должен иметь возможность использовать зашифрованные данные.
  
В то же время, могут иметь несколько слоев шифрования на месте. Например можно шифрование сообщений электронной почты, а также каналы связи, через которые потоки электронную почту. В Office 365 зашифрованные данные статических и во время передачи, с помощью нескольких шифрование протоколов и технологий, которые включают в себя транспортного уровня безопасности/Secure Sockets Layer (TLS/SSL), безопасность протокола IP (IPSec) и расширенный шифрования Стандартный (AES).
  
## <a name="encryption-for-data-at-rest-and-data-in-transit"></a>Шифрование статических данных и данных во время передачи

 Примеры **статических данных** файлов, которые были отправлены в библиотеке SharePoint, Project Online данные, документы, которые были отправлены в Скайп для бизнеса собрания, сообщений электронной почты и вложения, которые хранятся в папках в Office 365 почтовый ящик и файлы, загруженные в OneDrive для бизнеса. 
  
 **Данных во время передачи** примеры почтовых сообщений, для которых идет доставки или беседах, в которых с удалением собрания по сети. В Office 365 данных — во время передачи, каждый раз, когда устройство пользователя связывается с сервером Office 365 или при взаимодействии сервер Office 365 с другого сервера. 
  
С помощью Office 365 может иметь несколько уровней и видов шифрования совместная работа для защиты данных. В следующей таблице приведено несколько примеров, а также ссылки на дополнительные сведения.
  
|**Типов контента**|**Технологии шифрования**|**Ресурсы для получения дополнительных сведений**|
|:-----|:-----|:-----|
|Файлы на устройстве. Это могут быть сохранены в папке, документов Office, сохраненный на компьютере, планшетном ПК или телефон или данных, сохраненных в облако Microsoft сообщений электронной почты.  <br/> |BitLocker в центрах обработки данных Майкрософт. BitLocker также может использоваться на клиентских компьютерах, такие как компьютеры Windows и планшетные ПК  <br/> Диспетчер распределенных ключ (DKM) в центрах обработки данных Майкрософт  <br/> Клавиша клиентов для Office 365  <br/> |[Windows ИТ центр: BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) <br/> [Центр управления безопасностью Microsoft: шифрования](https://www.microsoft.com/en-us/TrustCenter/Security/Encryption) <br/> [Безопасность в облаке управляет серии: шифрование статических данных](https://blogs.microsoft.com/microsoftsecure/2015/09/10/cloud-security-controls-series-encrypting-data-at-rest) <br/> [Как Exchange Online защищает секреты вашей электронной почты](exchange-online-secures-email-secrets.md) <br/> [Контроль данных в Office 365 с помощью ключа клиента](controlling-your-data-using-customer-key.md) <br/> |
|Файлы во время передачи между пользователями. Это может включать Office документы или элементы списка SharePoint, доступные для всех пользователей.  <br/> |Протокол TLS для файлов во время передачи  <br/> |[Шифрование данных в OneDrive для бизнеса и SharePoint Online](data-encryption-in-odb-and-spo.md) <br/> [Скайп для бизнеса в Интернете: архивации и обеспечения безопасности](https://technet.microsoft.com/library/skype-for-business-online-security-and-archiving.aspx) <br/> |
|Электронной почты во время передачи между получателями. Этот компонент включает электронной почты, размещенного в Exchange Online.  <br/> |Шифрование сообщений Office 365 с помощью службы управления правами Azure, S/MIME и протокол TLS для электронной почты во время передачи  <br/> |[Шифрование сообщений Office 365 (OME)](ome.md) <br/> [Шифрование электронной почты в Office 365](email-encryption.md) <br/> [Использование протокола TLS службой Exchange Online для защиты электронной почты в Office 365](exchange-online-uses-tls-to-secure-email-connections.md) <br/> |
   
## <a name="what-if-i-need-more-control-over-encryption-to-meet-security-and-compliance-requirements"></a>Что делать, если я требуется дополнительный контроль над шифрования для удовлетворения требований к безопасности и соответствия требованиям?

В дополнение к управляемой корпорацией Майкрософт решений шифрование тома, шифрования файлов и шифрования почтовых ящиков в Office 365 параметры управляемого клиента можно использовать в соответствии с более строгие требования к безопасности и соответствия требованиям. Такие решения использовать службу управления правами Azure (Azure RMS) вместе с Office 365.
  
Воспользуйтесь следующими ресурсами для получения дополнительных сведений:
  
- [Что такое служба управления правами Azure?](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
    
- [Активация службы управления правами в Центре администрирования Office 365](https://support.office.com/article/5b6d3ac7-b1ac-428e-b03e-50e882f85a6e)
    
- [Задайте копирование управления правами на доступ к данным (IRM) в центре администрирования SharePoint](set-up-irm-in-sp-admin-center.md)
    
## <a name="how-do-i"></a>Как мне...

|**Для выполнения этой задачи**|**Вам помогут следующие ресурсы**|
|:-----|:-----|
|Настройка шифрования для организации  <br/> |[Настройка шифрования в Office 365 корпоративный](set-up-encryption.md) <br/> |
|Просмотр сведений о сертификатах, технологий и наборы шифрования TLS в Office 365  <br/> |[Технические сведения о шифрования в Office 365](technical-reference-details-about-encryption.md) <br/> |
|Работа с шифрованными сообщениями на мобильном устройстве  <br/> |[Просматривать зашифрованные сообщения на устройстве Android](https://support.office.com/article/83d60f17-2305-407a-a762-7d518401fdeb) <br/> [Просмотр зашифрованных сообщений на iPhone и iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf) <br/> |
|Шифрование документа с помощью защиты паролем  <br/></br>  На данный момент защиты паролем не поддерживается в Microsoft Office Online. Использование рабочего стола версий Word, Excel и PowerPoint для защиты паролем.           |[Добавление или изменение защиты в документе, книге или презентации](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Выберите раздел **Защита Add** и попытайтесь **Зашифровать паролем** )  <br/> |
|Удалить шифрование из документа  <br/> |[Добавление или изменение защиты в документе, книге или презентации](https://support.office.com/article/05084cc3-300d-4c1a-8416-38d3e37d6826) (Выберите раздел **Снять защиту** и попытайтесь **удалить шифрование пароля** )  <br/> |
   
## <a name="related-topics"></a>Статьи по теме

[Планирование возможностей защиты безопасности и данные Office 365](https://support.office.com/article/3d4ac4a1-3920-4ff9-918f-011f3ce60408)
  
[Безопасность и соответствие требованиям в Office 365 для бизнеса - Admin справки](https://support.office.com/article/7fe448f7-49bd-4d3e-919d-0a6d1cf675bb)
  
