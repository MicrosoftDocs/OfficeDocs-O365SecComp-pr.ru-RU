---
title: Поиск и исследовать вредоносных электронной почты, которое было доставлено (анализ угроз Office 365)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 8/6/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
description: Узнайте, как использовать анализ угроз для поиска и изучения вредоносного по электронной почте.
ms.openlocfilehash: 9d63bd69e11bca4bc76fa6d6d00a429ed1aac508
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534680"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-threat-intelligence"></a>Поиск и исследовать вредоносных электронной почты, которое было доставлено (анализ угроз Office 365)

[Анализ угроз Office 365](office-365-ti.md) позволяет вам изучить действий, которые пользователи поставить под угрозу и действие по защите вашей организации. Например если вы являетесь участником группы безопасности вашей организации, можно найти и отследить подозрительных сообщений, которые были доставлены для пользователей. Это можно сделать с помощью [Проводника угроз](get-started-with-ti.md#threat-explorer).
  
> [!NOTE]
> Анализ угроз Office 365 доступна в Office 365 корпоративный E5. Если ваша организация использует другой подписки Office 365 для предприятия, анализ угроз Office 365 можно приобрести в виде дополнительного компонента. (Как глобальный администратор, в центре администрирования Office 365 нажмите кнопку **выставления счетов** \> **Добавить подписок**.) Дополнительные сведения можно [Описание платформы Office 365: безопасность Office 365 &amp; центре соответствия требованиям](https://technet.microsoft.com/en-us/library/dn933793.aspx) и [покупке и изменить надстройки для Office 365 для бизнеса](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6). 
  
## <a name="before-you-begin"></a>Перед началом...

Убедитесь, что выполняются следующие требования:
  
- Вашей организации есть [Анализ угроз Office 365](office-365-ti.md) и [Назначение лицензий для пользователей в Office 365 для бизнеса](https://support.office.com/article/997596b5-4173-4627-b915-36abac6786dc).
    
- [Ведение журнала аудита Office 365](turn-audit-log-search-on-or-off.md) включена для вашей организации. 
    
- Вашей организации есть политик, определенных для защиты от нежелательной почты, вредоносных программ, фишинга и т. д. Просмотреть [угроз управления безопасности Office 365 &amp; центре соответствия требованиям](threat-management.md).
    
- Глобальный администратор Office 365 или у вас есть права администратора безопасности или поиска и очищать роли, назначенные в системы &amp; центре соответствия требованиям. Просмотреть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).
    
## <a name="dealing-with-suspicious-emails"></a>Работа с подозрительные сообщения электронной почты

Злоумышленников может отправки почты пользователям попробуйте и ловят их учетных данных и получить доступ к корпоративной секреты! Чтобы предотвратить это, следует использовать службы защиты от угроз, в Office 365, включая Exchange Online Protection и расширенный защиту от угроз. Тем не менее бывают ситуации при злоумышленник могли бы отправлять почту на компьютерах пользователей, содержащая URL-адрес и только более поздней версии для текущего момента URL-адрес для вредоносного содержимого (вредоносных программ, и т.д.). Кроме того вы может реализовать слишком позднего оказались раскрыты пользователей в вашей организации, что во время этого пользователя было атаке, он используется этой учетной записи для отправки электронной почты для других пользователей в вашей компании. Как часть Очистка оба сценария может потребоваться удаление сообщений электронной почты из папки "Входящие" пользователя. В подобных ситуациях вы можете использовать возможности Explorer угроз, поиск и удаление этих сообщений электронной почты.
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a>Поиск и удаление подозрительные электронной почты, которое было доставлено

> [!TIP]
> [Угрозы Explorer](get-started-with-ti.md#threat-explorer) (также называется Explorer), — это мощные отчета, который обслуживается сразу несколько целей, например, поиск и удаление сообщений, идентифицирующий IP-адрес отправителя вредоносного по электронной почте или запуск происшествия для дальнейшего изучения. Следующая процедура основное внимание уделяется с помощью проводника поиск и удаление вредоносного электронной почты из почтовых ящиков получателей. 
  
1. Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы для Office 365. Вы перейдете к безопасности &amp; центре соответствия требованиям. 
    
2. В левой панели навигации выберите **Threat management** \> **Explorer**.
    
3. В меню Вид выберите **всех сообщений электронной почты**.
    
    ![Используйте меню "Вид" для выбора между электронной почты и отчетов о контенте](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Обратите внимание на то метки, представленные в отчете, например **доставлено**, **Неизвестный**или **доставлено нежелательной**.
    
    ![Угрозы Explorer представлены данные для всех сообщений электронной почты](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)
  
    (В зависимости от действий, которые были сделаны в сообщения электронной почты для вашей организации, может появиться дополнительные метки, например **заблокирован** или **заменена**.)
    
5. В отчете выберите **доставлено** , чтобы просмотреть только по электронной почте, которые завершения в почтовые ящики пользователей. 
    
    ![Нажав кнопку «Доставлено нежелательной» удаляет эти данные из представления](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Ниже диаграмме просмотрите список **электронной почты** под диаграммой. 
    
    ![Ниже диаграмме Просмотр списка сообщений электронной почты, обнаруженные](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. В списке выберите элемент, чтобы просмотреть дополнительные сведения о сообщении электронной почты. К примеру можно щелкнуть строку темы для просмотра сведений о отправителя, получателей, вложения и другие аналогичные сообщений электронной почты.
    
    ![Можно просмотреть дополнительные сведения об элементе, включая подробные сведения и вложения](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. После просмотра сведений о сообщениях электронной почты, выберите один или несколько элементов в списке, чтобы активировать **+ действия**.
    
9. Используйте список **+ действия** для применения действия, такие как **Перемещение удаленных** элементов. Это приведет к удалению выбранных сообщений из почтовых ящиков получателей. 
    
    ![При выборе одного или нескольких сообщений электронной почты, можно выбрать несколько доступных действий](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
## <a name="related-topics"></a>Статьи по теме

[Office 365 Threat Intelligence](office-365-ti.md)
  
[Защита от угроз в Office 365](protect-against-threats.md)
  
[Просмотр отчетов для защиты расширенного Threat Office 365](view-reports-for-atp.md)
  
