---
title: Создайте сертификат APN для устройств операций ввода-вывода
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Для управления iOS устройств iPad и iPhones в управлении мобильных устройств для Office 365, выполните следующие действия, чтобы создать новый сертификат APN.
ms.openlocfilehash: 28e8888d7dd57c3052cdcb5994725f11a5f0445f
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272054"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a>Создайте сертификат APN для устройств операций ввода-вывода

 Для управления iOS устройств iPad и iPhones в управлении мобильных устройств для Office 365 необходимо создать новый сертификат APN. 
  
Чтобы сделать это, следуйте указаниям по ссылке **настроить** на странице портала. (Перейдите к **безопасности &amp; центре соответствия требованиям** \> **политики безопасности** \> **Управление устройствами** \> **Управление параметрами**.)
  
![Настройка мобильного устройства управления обязательные и рекомендуемые действия](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. **Настройка сертификата APN для устройств операций ввода-вывода**выберите **Настройка**.
    
2. Выберите **загрузить файл CSR** и в другое место для сохранения запроса подписи сертификата на компьютере, который необходимо передать. 
    
    ![Установка сертификата APN диалоговое окно ""](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. Нажмите кнопку **Далее**.
    
4. Создайте сертификат APN.
    
  - Выберите **Apple APNS портала** для открытия портале Apple Push-сертификаты. 
    
    ![Установка диалоговое окно сертификата APN уведомление с выбрано портала APNS Apple](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - Вход с помощью идентификатора Apple.
    
    > [!IMPORTANT]
    > Используйте компании Apple идентификатор, связанное с учетной записью электронной почты, который будет оставаться с организацией, даже в том случае, если пользователь, который управляет учетной записи оставляет. Сохраните этот код, так как вам потребуется использовать тот же идентификатор, если время для обновления сертификата. 
  
  - Выберите команду **создать сертификат** и примите **Условия использования**.
    
  - **Обзор** запрос подписи сертификата был загружен на компьютер с Office 365 и выберите **Отправить**.
    
  - **Загрузите** сертификат APN, созданных Apple Push-сертификат портала на своем компьютере. 
    
    > [!TIP]
    > Если у вас возникли проблемы при загрузке сертификата, обновите окно обозревателя. 
  
5. Вернитесь в Office 365 и нажмите кнопку **Далее** для перехода к странице **APNS Загрузка сертификата** . 
    
6. Перейдите к APN сертификат, который был загружен из портала Apple Push-сертификаты.
    
    ![Нажмите кнопку Обзор, чтобы выбрать сертификат APNS, загруженные из Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. Нажмите кнопку **Готово**.
    
Вернуться к **безопасности &amp; центре соответствия требованиям** \> **политики безопасности** \> **Управление устройствами** \> **Управление параметрами** , чтобы завершить настройку. 
  
