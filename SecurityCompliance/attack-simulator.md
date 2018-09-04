---
title: Эмулятор атак в Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/19/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Узнайте о трех различных типов атаки через Интернет, которые можно запустить с помощью имитатора атаки.
ms.openlocfilehash: 364144c0b2f8109c67fb262ce879414088380ebe
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534582"
---
# <a name="attack-simulator-in-office-365"></a>Эмулятор атак в Office 365

С помощью имитатора атаки (включены в [Анализ угроз Office 365](office-365-ti.md)) Если вы являетесь членом группы безопасности вашей организации, можно запустить сценарии реалистичной атаки в вашей организации. Это может помочь определить и найти уязвимы пользователей перед реальных атаки влияет на производительность.
  
## <a name="the-attacks"></a>Атаки

В предварительном выпуске мы предлагаем три вида при моделировании атаки, которые могут работать:
  
- [Отображение имени направленных фишинга](attack-simulator.md#spearphish)
    
- [Пароль распылителя атаки](attack-simulator.md#passwordspray)
    
- [Перебора атаки пароль](attack-simulator.md#bruteforce)
    
Атака для успешного запуска учетная запись, под управлением атаки и вход в систему необходимо использовать многофакторной проверки подлинности.
  
> [!NOTE]
> Поддержка условного доступа в ближайшее время. 
  
Для доступа к имитатора атаки, в системы &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.
  
## <a name="before-you-begin"></a>Перед началом...

Убедитесь в том, что вам и вашей организации соответствуют следующим требованиям для атаки имитатора:
  
- Вашей организации есть [Анализ угроз Office 365](office-365-ti.md), с помощью атаки имитатора видимы в безопасности &amp; центре соответствия требованиям (перейдите к **разделу Управление угроз** \> **атаки имитатора**)
    
- Электронной почты вашей организации размещается в Exchange Online. (Атаки имитатора недоступно для локальных серверов электронной почты).
    
- Глобальный администратор Office 365
    
- Ваша организация использует [многофакторной проверки подлинности для пользователей Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="display-name-spear-phishing-attack"></a>Отображение имени направленных фишинга

Фишинг — это общий термин для широкого набора classed как атака стиль социальная инженерия атаки. В этом атаки, ориентированный на направленные фишинга, более целевой атаки, направленные на конкретной группы отдельных пользователей или организации. Как правило выполненных настраиваемого атаки с некоторые reconnaissance и использование отображаемое имя, которое будет создавать доверия в получателя, таких как сообщения электронной почты, которая выглядит как он поступил от руководителя вашей организации.
  
В этом атаки основное внимание уделяется возможности работы с которого была инициирована, изменив отображаемое имя и исходный адрес отображается сообщение. При успешной направленных фишинга компьютерных преступников получить доступ к учетных данных пользователей.
  
### <a name="to-simulate-a-spear-phishing-attack"></a>Для моделирования работы направленных фишинга

![Создайте текст электронной почты](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
Вы можете создавать расширенного редактора HTML непосредственно в поле **текст сообщения электронной почты** , самого или работать с исходного HTML-кода. Существует два важных поля для включения в HTML-код. 
  
1. В разделе Безопасность &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.
    
2. Укажите имя удобной для восприятия кампании для атаки или выберите шаблон.
    
    ![Начальная страница фишинга](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. Укажите в целевой список получателей. Это может быть отдельных пользователей или групп в вашей организации. Целевые получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.
    
    ![Выбор получателей](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. Настройка сведений фишинга электронной почты.
    
    ![Настройка сведений о электронной почты](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
  
    Форматирование HTML-код может быть следующим сложных или базовой должна кампании. Как HTML, можно вставить изображения и текст для улучшения believability. У вас есть элемент управления на полученного сообщения будет выглядеть в клиенте получение электронной почты.
    
1. Введите текст для полей **из (имя)** . Это поле, которое отображает в поле **Отображаемое имя** в клиенте получение электронной почты. 
    
2. Введите текст или **из** поля. Это поле, которое показывает, как адрес электронной почты отправителя в получающей клиента электронной почты. 
    
    > [!IMPORTANT]
    > Можно ввести существующих имен электронной почты в пределах организации (это сделает адрес электронной почты, которые фактически решения в клиент-получатель, упрощение модели очень высоким уровнем доверия), или можно ввести внешний адрес электронной почты. Адрес электронной почты, который указан не существует, но его нужно формат является допустимым адресом SMTP, таких как user@domainname.extension. 
  
3. С помощью раскрывающегося списка выбора, установите для входа фишинга URL-адрес сервера, который отражает тип контента, которые должны быть в рамках вашей атаки. Несколько URL-адреса, темой предоставляются для выбора, такие как документов доставки, технические, о начислении заработной платы и т.д. Это эффективно конечных пользователей будет предложено щелкните URL-адреса.
    
4. Введите URL-адрес настраиваемого целевую страницы. С помощью этого перенаправление пользователей в URL-адрес, укажите в конце атаки. Если у вас есть внутренний курса обучения, например, можно указать, здесь.
    
5. Введите текст в поле **Тема** . Это поле, которое показывает, как **Имя субъекта** в клиенте получение электронной почты. 
    
5. Создайте **текст сообщения электронной почты** , который будет получать целевой объект. 
  
 **${имя_пользователя}** вставляет имя целевых значений в текст электронной почты 
  
 URL-адрес, мы конечного пользователям нажмите кнопку Вставка **${loginserverurl}** 
    
6. Нажмите кнопку **Далее,** а затем **Готово** для запуска атаки. Сообщение электронной почты фишинга направленных доставляется в почтовые ящики получателей целевой. 
    
## <a name="password-spray-attack"></a>Пароль распылителя атаки

После actor очень плохо успешно перечислены список допустимых пользователей от клиента, использующие их знаний распространенных паролей, используемых обычно используется распылителя пароль, против организации. Это используемые широко как есть дешевое атаки для запуска и труднее обнаруживать чем перебора подходов.
  
В этом атаки основное внимание уделяется позволяет указать общий пароль для крупных целевой базы пользователей.
  
### <a name="to-simulate-a-password-spray-attack"></a>Для моделирования атаки распылителя пароль

1. В разделе Безопасность &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.
    
2. Укажите имя удобной для восприятия кампании для атаки.
    
3. Укажите в целевой список получателей. Это может быть отдельных пользователей или групп в вашей организации. Целевые получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.
    
4. Укажите пароль, используемый для атаки. Например одного общего, соответствующий пароль, попробуйте — `Fall2017`. Другой может быть `Spring2018`, или `Password1`.
    
5. Нажмите кнопку **Готово** , чтобы запустить атаки. 
    
## <a name="brute-force-password-attack"></a>Перебора атаки пароль

Пароль перебора против организации обычно используется после actor очень плохо успешно перечислены список ключей пользователей от клиента. В этом атаки основное внимание уделяется позволяет указать паролей от одного пользователя.
  
### <a name="to-simulate-a-brute-force-password-attack"></a>Для моделирования атаки перебора паролей

1. В разделе Безопасность &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.
    
2. Укажите имя удобной для восприятия кампании для атаки.
    
3. Указание конечного получателя. Целевые получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.
    
4. Задать пароли для атаки. Например одного общего, соответствующий пароль, попробуйте — `Fall2017`. Другой может быть `Spring2018`, или `Password1`.
    
5. Нажмите кнопку **Готово** , чтобы запустить атаки. 
    
## <a name="related-topics"></a>Статьи по теме

[Office 365 Threat Intelligence](office-365-ti.md)
  
