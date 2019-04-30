---
title: Защита информации
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 4/26/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Целевая страница для защиты информации
ms.openlocfilehash: 1c673c2417b399c57ca7ac7e5c5a7b7351de1edd
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473198"
---
# <a name="protect-information"></a>Защита информации

Microsoft 365 и Office 365 включают возможности, которые можно применять к определенным типам данных для защиты информации. 


|**Возможность**|**Дополнительные сведения**|
|:-----|:-----|
|[Метки конфиденциальности](sensitivity-labels.md) <br/> |С помощью меток конфиденциальности вы можете классифицировать и защитить конфиденциальный контент. Параметры защиты включают метки, подложки и шифрование. Метки конфиденциальности используют Azure Information Protection. Если вы используете метки Azure Information Protection, рекомендуем не создавать новые метки в других центрах администрирования до завершения миграции. См.: [Миграция Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-migrate-labels). <br/> [Метки хранения](retention-policies.md) отличаются от меток чувствительности. Метки хранения помогают сохранить или удалить контент на основе определяемых вами политик. Они помогают организациям соответствовать отраслевым нормам и внутренним политикам.|
|[Защита от потери данных](data-loss-prevention-policies.md) DLP  <br/> |С помощью политик защиты от потери данных можно определять, отслеживать и автоматически защищать конфиденциальные данные в Office 365. Политики защиты от потери данных могут использовать метки конфиденциальности и типы конфиденциальной информации для идентификации конфиденциальной информации. <br/> |
|[Типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)  <br/> |DLP включает множество типов конфиденциальных данных, готовых к использованию в политиках защиты от потери данных. Типы конфиденциальной информации определяют, как автоматизированный процесс распознает конкретные типы данных, такие как номера службы работоспособности и номера кредитных карт.   <br/> |
|[Шифрование сообщений Office 365](ome.md) OMe  <br/> |С помощью шифрования сообщений Office 365 ваша организация может отправлять и получать зашифрованные сообщения электронной почты между людьми в Организации и за ее пределами. Шифрование сообщений Office 365 работает с Outlook.com, Yahoo!, Gmail и другими почтовыми службами. Шифрование сообщений электронной почты гарантирует, что только предназначенные для получателей сообщения могут просматривать содержимое сообщения.  <br/> |
|[Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/)<br/> |Если вы используете метки чувствительности или шифрование сообщений Office, вы уже используете Azure Information Protection. Если вы еще не перенесли метки Azure Information Protection в Office 365, продолжайте управлять ими в Azure Information Protection.  <br/>[Сканер Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/deploy-aip-scanner) можно запустить на локальном сервере, чтобы классифицировать и защитить файлы в Windows Server, сетевых ресурсах и сайтах и библиотеках SharePoint Server. Это может быть первый шаг к идентификации данных для переноса в Office 365.
|Azure Information Protection с решениями БЙОК или ХЙОК <br/> |Некоторые организации предъявляют требования к бизнес-потребностям или требованиям для обеспечения управления ключами енциптион в локальной среде или в облаке. Это нетипичный сценарий. Дополнительные сведения см. [в разделе удержание собственного ключа (хйок) для Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-adrms-restrictions) и [перенесите свой ключ (Бйок) для Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/byok-price-restrictions). <br/> |
    

