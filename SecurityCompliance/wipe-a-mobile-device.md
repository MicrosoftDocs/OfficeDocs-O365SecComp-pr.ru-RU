---
title: Стирание мобильного устройства в Office 365
ms.author: dianef
author: dianef77
manager: scotv
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_WipeDevice
- O365E_WipeDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9d727c7d-8b47-4499-bf24-d046b449214c
description: Выполнять Выборочный очистки для удаления только корпоративной информации или полный очистку, чтобы удалить все данные с мобильного устройства и восстановить параметры фабрики можно использовать управление встроенных мобильных устройств для Office 365.
ms.openlocfilehash: d3eb28575924ca3bb4a647ae9af2f96b55116a53
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272504"
---
# <a name="wipe-a-mobile-device-in-office-365"></a>Стирание мобильного устройства в Office 365
  
Выполнять Выборочный очистки для удаления только корпоративной информации или полный очистку, чтобы удалить все данные с мобильного устройства и восстановить параметры фабрики можно использовать управление встроенных мобильных устройств для Office 365.
  
## <a name="what-to-know-before-you-begin"></a>Что следует знать перед началом работы

- Мобильных устройств можно хранить конфиденциальные корпоративной информации и предоставляют доступ к ресурсам организации Office 365. Для защиты информации в вашей организации, вы можете выполнять полный очистки или Выборочный очистки:
    
  - **Полный очистки**: Удаляет все данные на мобильном устройстве пользователя, включая установленные приложения, фотографии и личные сведения. После завершения очистки устройства восстанавливается его параметры фабрики. 
    
  - **Функция выборочной стирание**: удаляется только данные организации и оставляет установленные приложения, фотографии и личные сведения на мобильном устройстве пользователя. 
    
- Если устройство является Очистить (очистки полный или Выборочный очистки), устройство удаляется из списка управляемых устройств.
    
- Можно настроить политики управления мобильного устройства, которая автоматически стирание (полный очистки) устройства после неудачных попыток пользователя ввести пароль устройства определенное количество раз. Выполните действия, описанные в [Создание и развертывание политик безопасности устройств](create-device-security-policies.md).
    
- Если вы хотите знать, что пользователь будет работать после стирание свои устройства, [влияет на пользователя и устройства?](wipe-a-mobile-device.md#BKMK_Impact).
    
## <a name="wipe-a-mobile-device"></a>Стирание мобильного устройства

1. Последовательно выберите пункты [ ![щелкните здесь, чтобы перейти в центр администрирования Office 365.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).

2. Последовательно выберите пункты [Откройте раздел безопасность Office 365 &amp; центре соответствия требованиям](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) \> **защиту от потери данных** \> **Управление устройствами**.
    
3. Выберите устройство, которое требуется удалить.
    
4. Выберите тип удаленной очистки, которые необходимо выполнить.
    
  - Выборочный очистки и удалить только Office 365 сведения об организации, в области справа выберите **функция выборочной стирание**.
    
  - Выполните полный очистки и восстановления устройства параметры фабрики, в области справа выберите **Полный очистки**.
    
![Выберите устройство и затем выберите тип очистки для выполнения.](media/ac940abe-0c4a-404e-a842-a1ad2af13ce3.png)
  
5. Выберите **Да** для подтверждения. 
    
До завершения очистки **Состояние устройства** будет показано, как **RetirePending** или **RetireIssued**.
  
### <a name="how-do-i-know-it-worked"></a>Как узнать, что она работает?

Больше не увидите мобильных устройств в списке управляемыми устройствами.
  
## <a name="why-would-you-want-to-wipe-a-device"></a>Почему бы вы хотите стирание устройства?

Существует несколько причин для полное удаление устройств.
  
- Мобильных устройствах, таких как смартфоны и планшетные ПК становятся более полнофункционального все время. Это означает, что проще для пользователей для хранения конфиденциальных данных организации (например, персональных и конфиденциальных сообщений) и получить к нему доступ в дороге. Если один из этих мобильных устройств потери или кражи, очистка устройства сразу же можно предотвратить вашей организации сведений заканчивающиеся руки.
    
- Когда пользователь покидает организации с личного устройства, участвуют в MDM для Office 365, могут предупредить корпоративной информации переход с этим пользователем, выполнив Выборочный очистки.
    
- Если организация предоставляет мобильных устройств для пользователей, может потребоваться переназначить устройств от времени. Выполните полный очистки устройства перед присвоением нового пользователя помогает гарантирует удаления любой конфиденциальной информации с прежнего владельца.
    
## <a name="whats-the-user-and-device-impact"></a>Что такое пользователя и влияние устройство?

Очистки сразу отправляется на мобильное устройство. Устройства также отмечен как не соответствует спецификации в AAD.
  
В следующей таблице описываются содержимого удаляется для каждого типа устройства при выборочно Очистить устройство.
  
|**Влияние контента**|**Windows Phone 8.1**|**iOS 7.1+**|**Android 4 и более поздние версии**|
|:-----|:-----|:-----|:-----|
|Приложение портала компании\* удаляется.  <br/> |Недоступно  <br/> |✔  <br/> |Недоступно  <br/> |
|Данные приложения Office 365, размещенных приложений, где контроля доступа поддерживаемый MDM для Office 365 — удалены (в настоящее время Outlook и OneDrive для бизнеса). Приложения не удаляются.  <br/> Outlook для Android не удаляет кэшированные по электронной почте.  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Параметры политики, которые были установлены с MDM для Office 365 на устройствах больше не применяются на устройстве и пользователи могут менять параметры.  <br/> |✔  <br/> |✔  <br/> |✔  <br/> |
|Профили электронной почты, созданные MDM для Office 365 и удалены кэшированные электронной почты в устройстве.  <br/> |Недоступно  <br/> |✔  <br/> |Недоступно  <br/> |
   
> [!NOTE]
> \*Приложение портала компании доступен на хранилище приложений для iOS и воспроизвести хранилища для устройства Android. 
  
## <a name="related-content"></a>Связанные материалы

[Управлять мобильными устройствами в Office 365](set-up-mobile-device-management.md)
  
