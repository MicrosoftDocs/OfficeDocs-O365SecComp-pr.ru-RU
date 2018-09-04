---
title: Технические сведения о шифровании в Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2018
ms.audience: ITPro
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: 862cbe93-4268-4ef9-ba79-277545ecf221
description: Технические сведения о обязательно просмотра в Office 365.
ms.openlocfilehash: d86692119f7558d74e2083165b4eb6ab4a07da70
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535250"
---
# <a name="technical-reference-details-about-encryption-in-office-365"></a>Технические сведения о шифровании в Office 365

Найти в этой статье содержатся общие сведения о сертификатах, технологий и TLS наборы шифрования, используемый для [шифрования в Office 365](encryption.md). В этой статье также представлена информация о запланированных сведения о неподдерживаемых.
  
- Если вы ищете сведения, см [в Office 365](encryption.md).
    
- Если вы ищете сведения об установке, видеть [шифрование в Office 365 для предприятия](set-up-encryption.md).
    
## <a name="microsoft-office-365-certificate-ownership-and-management"></a>Владение и управление сертификатами Microsoft Office 365

Вам не нужно приобретать или обслуживать сертификаты для Office 365, так как корпорация Майкрософт использует собственные.
  
## <a name="current-encryption-standards-and-planned-deprecations"></a>Текущие стандарты шифрования и сведения о неподдерживаемых запланированных

Для продолжения для предоставления лучшие в своем классе шифрования для Office 365 Майкрософт регулярно дается обзор поддерживаемых шифрования стандартов. В некоторых случаях необходимо отказаться от старого стандартов как только они становятся устаревший и поэтому менее безопасным. В этом разделе описываются наборы в настоящее время поддерживаются шифрования и других стандартов, а также подробные сведения о запланированных сведения о неподдерживаемых.
  
## <a name="versions-of-tls-supported-by-office-365"></a>Версии протокола TLS, поддерживаемые Office 365

Протокол TLS и его предшественник SSL защищают данные при передаче в сети, шифруя соединения между компьютерами с помощью сертификатов безопасности. Office 365 поддерживает несколько версий TLS, в том числе:
  
- TLS версии 1.2 (TLS 1.2);
    
- TLS версии 1.1 (TLS 1.1);
    
- TLS версии 1.0 (TLS 1.0).
    
 Поддержка TLS 1.0 и TLS 1.1 является устаревшим 31 октября 2018. Для получения дополнительных сведений в разделе [Поддержка Deprecating TLS 1.0 и 1.1, что означает для вас](technical-reference-details-about-encryption.md#TLS11and12deprecation) . 
  
## <a name="deprecating-support-for-tls-10-and-11-and-what-this-means-for-you"></a>Неподдерживаемые поддержка TLS 1.0 и 1.1, что означает для вас
<a name="TLS11and12deprecation"> </a>

Важные изменения будут внесены в параметры шифрования, поддерживаемые для Office 365. По состоянию на 31 октября 2018 Office 365 больше не поддерживает использование TLS 1.0 или 1.1 для обмена данными в Office 365. Когда Office 365 deprecates поддержку следующих протоколов, все коммуникации с серверами Office 365 потребуется использовать TLS 1.2. Сведения о том, как это влияет на вы см [обязательного использования TLS 1.2 в Office 365](https://support.microsoft.com/en-us/help/4057306/preparing-for-tls-1-2-in-office-365). Серверов и клиентов, связи с O365 после указанной даты должна поддерживать TLS 1.2.
  
## <a name="deprecating-support-for-3des"></a>Неподдерживаемые поддержка 3DES
<a name="TLS11and12deprecation"> </a>

По состоянию на 31 октября 2018 Office 365 больше не поддерживает использование наборов шифрования 3DES для обмена данными в Office 365. В частности Office 365 suite шифр TLS_RSA_WITH_3DES_EDE_CBC_SHA больше не поддерживаются. Клиенты и серверы связь с O365 после указанной даты должен поддерживать по крайней мере один из более безопасной шифр, представленные в этом разделе (см. [TLS зашифрованного наборов поддерживаются в Office 365](technical-reference-details-about-encryption.md#TLSCipherSuites)).
  
## <a name="deprecating-sha-1-certificate-support-in-office-365"></a>Прекращение поддержки сертификата SHA-1 в Office 365
<a name="TLS11and12deprecation"> </a>

По состоянию на июнь 2016 Office 365 больше не принимает сертификат SHA-1 для входящие и исходящие подключения. Если в настоящее время используется сертификат с SHA-1 в цепочку сертификатов, необходимо обновить цепочки использовать SHA-2 (Secure 2 алгоритм хэш-функции) или более надежная алгоритм хэширования.
  
## <a name="deprecating-rc4-support-in-office-365"></a>Прекращение поддержки RC4 в Office 365
<a name="TLS11and12deprecation"> </a>

В июле 2015 г. была прекращена поддержка следующих наборов шифров RC4:
  
- TLS_RSA_WITH_RC4_128_SHA
    
- TLS_RSA_WITH_RC4_128_MD5
    
## <a name="deprecating-secure-sockets-layer-ssl-30-support-in-office-365"></a>Неподдерживаемые Secure Sockets Layer (SSL) 3.0 поддержки в Office 365
<a name="TLS11and12deprecation"> </a>

Запуск 1 декабря 2014 г., Office 365 начала отключение поддержки для Secure Sockets Layer (SSL) 3.0, предыдущей, что протокол TLS. Для получения дополнительных сведений см [advisory 3009008](https://technet.microsoft.com/library/security/3009008.aspx). Инструкции для обеспечения клиентов используется протокол TLS 1.0 или более поздней и отключение SSL 3.0 видеть [уязвимость защита SSL 3.0](http://blogs.office.com/2014/10/29/protecting-ssl-3-0-vulnerability/).
  
## <a name="tls-cipher-suites-supported-by-office-365"></a>Наборы приложений шифрования TLS, поддерживаются в Office 365
<a name="TLSCipherSuites"> </a>

Набор шифров — это совокупность алгоритмов шифрования, которые TLS использует для установки безопасного соединения. Наборы шифров, поддерживаемые Office 365, перечислены в таблице ниже в порядке убывания степени надежности с первого по последний. При получении запроса на соединение Office 365 сначала пытается подключиться с помощью первого набора шифров, а затем, в случае неудачной попытки, пробует следующий по списку и т. д. Когда Office 365 отправляет запрос на соединение на другой сервер или клиент, последние должны либо выбрать набор шифров, либо вообще отклонить протокол TLS.
  
|**Протоколы**|**Имя набора шифров**|**Алгоритм/надежность обмена ключами**|**Поддержка безопасной пересылки (PFS)**|**Алгоритм/надежность проверки подлинности**|**Шифр и его надежность**|
|:-----|:-----|:-----|:-----|:-----|:-----|
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384_P384  <br/> |ECDH/192  <br/> |Да  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256_P256  <br/> |ECDH/128  <br/> |Да  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA_P384  <br/> |ECDH/192  <br/> |Да  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA_P256  <br/> |ECDH/128  <br/> |Да  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA256  <br/> |RSA/112  <br/> |Нет  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA256  <br/> |RSA/112  <br/> |Нет  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_256_CBC_SHA  <br/> |RSA/112  <br/> |Нет  <br/> |RSA/112  <br/> |AES/256  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_AES_128_CBC_SHA  <br/> |RSA/112  <br/> |Нет  <br/> |RSA/112  <br/> |AES/128  <br/> |
|TLS 1.0, 1.1, 1.2  <br/> |TLS_RSA_WITH_3DES_EDE_CBC_SHA  <br/> |RSA/112  <br/> |Нет  <br/> |RSA/112  <br/> |3DES/192  <br/> |
   
## <a name="related-topics"></a>Статьи по теме
<a name="TLSCipherSuites"> </a>

[Шифрование в Office 365](encryption.md)
  
[Настройка шифрования в Office 365 корпоративный](set-up-encryption.md)
  
[Реализация Schannel TLS 1.0 в обновление состояния системы безопасности Windows: 24 ноября 2015](https://support.microsoft.com/kb/3117336)
  
[Улучшения шифрования TLS/SSL (Windows ИТ центр)](https://technet.microsoft.com/en-us/library/cc766285%28v=ws.10%29.aspx)
  
