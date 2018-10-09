---
title: Интеграция сервера SIEM с Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Сервер SIEM можно интегрировать с Office 365 облачных приложений безопасности. В этой статье Обзор принцип работы и способы ее настройки.
ms.openlocfilehash: d8603d53e156e89c53f13153cd90d400b1312538
ms.sourcegitcommit: 2e41cc24ad92005084f2ba432e724bdcc4e295ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25450764"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a>Интеграция сервера SIEM с Office 365 Cloud App Security
  
|Оценка **\>**|Планирование **\>**|Развертывание **\>**|Использование ***|
|:-----|:-----|:-----|:-----|
|[Начать оценку](office-365-cas-overview.md) <br/> |[Начать планирование](get-ready-for-office-365-cas.md) <br/> |Вы находитесь здесь!  <br/> [Следующий шаг](utilization-activities-for-ocas.md) <br/> |[Начать использование](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a>Обзор и необходимые условия

Можно интегрировать [Приложения облаке Безопасность в Office 365](get-ready-for-office-365-cas.md) с сервером для включения централизованного мониторинга предупреждений безопасности сведения и события управления (SIEM). Это особенно удобно использовать для организаций, использующих облачных служб и локального сервера приложений. Интеграция с сервером SIEM позволяет ваша группа безопасности для улучшения защиты приложений Office 365 без снижения безопасности обычного рабочего процесса, автоматизация некоторых процедуры безопасности и сопоставления между облачной и локальной события.  
  
При SIEM сервера сначала интеграции с Office 365 облачных приложений безопасности, оповещения о от последних двух дней будут переадресовываться SIEM сервера, а также все оповещения из then на (основан на все фильтры, которые вы выбрали). Кроме того Если отключить этот компонент в течение длительного, при включении его еще раз, он будет перенаправлять за последние два дня оповещений и затем все оповещения в дальнейшем.

### <a name="siem-integration-architecture"></a>Архитектура интеграции SIEM

Агент SIEM настраивается в сети организации. При развертывания и настройки агента SIEM берет типов данных, которые были настроены (оповещения) с помощью Office 365 облачных приложений безопасности RESTful API-интерфейсы. Затем передачи через зашифрованный канал HTTPS через порт 443.
  
Когда SIEM агент получает данные из приложения облаке Безопасность в Office 365, он отправляет сообщения Syslog на локальном сервере SIEM, с помощью конфигурации сети, которые предоставляются во время установки (TCP или UDP-ПОРТ с помощью настраиваемых портов).

![Архитектура SIEM и облачных безопасности приложения](media/siem-architecture.png)

### <a name="supported-siem-servers"></a>Поддерживаемые SIEM серверы

В настоящее время безопасности облаке приложения Office 365 поддерживает следующие серверы SIEM:
- Разработанное Micro Focus
- Универсальный CEF

### <a name="prerequisites"></a>Требования

- Необходимо быть глобальным администратором или администратор безопасности для выполнения задач, описанных в этой статье. Просмотреть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md)

- Необходимо иметь [поддержкой безопасности приложения Office 365 облако](turn-on-office-365-cas.md) для вашей организации.

- [Ведение журнала аудита](turn-audit-log-search-on-or-off.md) может быть включена для Office 365

- Необходимо иметь стандартный сервер, который соответствует следующим требованиям для настройки интеграции сервера SIEM:
    - Операционная система: Windows или Linux (это может быть виртуальной машины)
    - ЦП: 2
    - Место на диске: 20 ГБ
    - ОЗУ: 2 ГБ
    - Установленные [Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
    - Брандмауэр, как описано в [требования к сети](https://docs.microsoft.com/cloud-app-security/network-requirements)

- Необходимо иметь подробные сведения об **удаленных syslog узла** и **номер порта Syslot**. Администратор или администратор безопасности должна появиться возможность помогают найти эти сведения. 

- Для загрузки [БАНКИ файлов](https://go.microsoft.com/fwlink/?linkid=838596) необходимо интегрировать сервера SIEM, необходимо согласиться [Лицензионное соглашение на использование программного обеспечения](https://go.microsoft.com/fwlink/?linkid=862491) .
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a>Шаг 1: Ее настройка агента SIEM в облаке приложения Office 365 безопасности

1. Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы для Office 365. (Вы перейдете к безопасности &amp; центре соответствия требованиям.) 
    
2. Последовательно выберите пункты **оповещения** \> **Управление расширенного оповещения**.
    
3. Выберите, **перейдите к безопасности приложения Office 365 облака**.<br/>
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите дополнительные оповещения для перехода к безопасности Office 365 облаке приложения](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. Щелкните **Параметры** \> **расширения безопасности**.<br/>
![Выберите параметры > расширения безопасности](media/Settings-SecurityExtensions.png)

5. Выберите пункт **Добавить SIEM агента**.<br/>![Выберите пункт Добавить SIEM агента.](media/SIEMAgents.png)
    
6. Нажмите кнопку **запустить мастер**.<br/>![Получение справки или запустить мастер](media/HelpOrWizard.png) 
    
7. **Общие** шаге укажите имя и **выберите в качестве формата SIEM формат** и задайте любые **Дополнительные параметры** , которые важны для этого формата. Нажмите кнопку **Далее**.<br/>![Укажите имя и тип](media/ChooseAgentTypeAndName.png)
    
8. На этапе **Удаленного Syslog** укажите IP-адрес или имя узла **удаленного syslog узла** и **номер порта Syslog**. Выберите в качестве протокола удаленного Syslog TCP или UDP-ПОРТ. (Можно работать с администратором сети или администратор безопасности для получения этих сведений, если у них нет.) Нажмите кнопку **Далее**.<br/>![Укажите сведения о удаленного Syslog](media/ArcSightS1Syslog.png)
  
9. На этапе **Типы данных** , выполните одно из следующих действий и нажмите кнопку **Далее**:
    - Оставьте значение по умолчанию **Все оповещения**<br/>OR
    - Щелкните **все оповещения**и нажмите кнопку **Специальные фильтры**. Определение фильтров для выбора типа оповещений, которое требуется отправить на сервер SIEM.<br/>![Этап типы данных мастера](media/ArcSightS1ExportOptions.png)
  
10. На странице приветствия Скопируйте маркер и сохраните его для последующих операций.<br/>![Агент создан SIEM экрана](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> На этом этапе настройки агента SIEM в облаке приложения Office 365 безопасности, однако интеграция сервера вашей SIEM еще не выполнено. Перейти к следующему шагу для продолжения интеграции сервера SIEM.

После нажмите кнопку Закрыть и закрыть мастер, на экране расширений безопасности, можно просмотреть агента SIEM, добавленной в таблице. Пока он подключен более поздней версии, он будет отображается статус **создано** .

![Агент SIEM создан](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a>Шаг 2: Загрузите файл БАНКЕ и запустите его на сервер SIEM

1. Загрузите [Microsoft Cloud приложения безопасности SIEM агента](https://go.microsoft.com/fwlink/?linkid=838596) и распакуйте папку. (Необходимо согласиться [Лицензионное соглашение на использование программного обеспечения](https://go.microsoft.com/fwlink/?linkid=862491) для продолжения.) 
    
2. Извлеките файл .jar из ZIP-папку и запустите его на сервере SIEM.
    
3. После запуска файла, выполните следующие действия: команду:<br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a>Важные замечания

- Имя файла может отличаться в зависимости от версии SIEM агента. 

- Мы рекомендуем, запустите файл БАНКЕ на сервере SIEM во время установки сервера.

    - **Windows**: запустите как запланированная задача, сохраняя настройки задачи для **запуска ли пользователь вошел в систему, или не** и снять флажок **останавливать при выполнении дольше, чем** .

    - **Linux**: Добавление выполнения команды с **&** для `rc.local` файла. <br/>Пример.<br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- Параметры в квадратных скобок являются необязательными и следует использовать только при необходимости. Используйте следующие переменные:
    - **DIRNAME** — это путь каталог, который вы хотите использовать для локального агента журналы отладки.
    - **Адрес [: ПОРТ]** — это адрес прокси-сервера и порт, который используется сервером для подключения к Интернету.
    - **МАРКЕР** является маркером агента SIEM, скопированные в первой процедуре.
    - Чтобы получить справку, введите `-h`. 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a>Шаг 3: Проверка работы агента SIEM

1. Убедитесь, что состояние агента SIEM на портале облачных приложений Office 365 безопасности не отображается как **Ошибка подключения** или **отключен** , который отсутствии агента уведомлений.<br/>Например здесь можно увидеть, что подключения к серверу SIEM:<br/>![Подключение сервера SIEM](media/siem-connected.png)<br/>А здесь, можно увидеть, что сервер SIEM отключен:<br/>![SIEM сервер не подключен](media/siem-not-connected.png) 
  
2. На сервере Syslog/SIEM убедитесь, что видно, что оповещения поступили от приложения облаке Безопасность в Office 365.
  
## <a name="what-the-logfiles-look-like"></a>Что собой файлов журналов

Ниже приведен пример файла журнала оповещений, которое может отправить на сервер SIEM:

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

А вот другой пример настоящее время в формате CEF:


|Имя поля CEF  | Описание  |
|---------|---------|
|Запуск     | Метка времени оповещения        |
|End     | Метка времени оповещения        |
|время выполнения     | Метка времени оповещения        |
|MSG     | предупреждения описание, как показано на портале облачных приложений Office 365 безопасности        |
|suser     | Тема оповещения пользователя        |
|destinationServiceName     | оповещение, поступающих приложения, такие как Office 365, SharePoint или OneDrive        |
|csLabel     | Зависит от (метки имеют различные значения). Как правило метки очевидны, как targetObjects.        |
|cs     | Сведения, относящиеся к метки (например, целевого пользователя оповещения на примере метки)        |

## <a name="additional-tasks-as-needed"></a>Дополнительные задачи (при необходимости)

После того как сервер настроен на SIEM и интегрировали с Office 365 облачных приложений безопасности может потребоваться повторно создать маркер, изменение SIEM агента, удаление агента SIEM. В следующих разделах описано для выполнения этих задач.

### <a name="regenerate-a-token"></a>Обновите маркера

При разрыве вашей маркера, можно повторно создать один. 

1. На портале облачных приложений Office 365 безопасности выберите **Параметры** > **расширения безопасности**.

2. В таблице найдите строку для агента SIEM. 

3. Нажмите кнопку с многоточием и выберите **восстановить маркер**.<br/>![Обновите маркера, нажав кнопку с многоточием для агента SIEM](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
### <a name="edit-a-siem-agent"></a>Изменение агента SIEM

1. На портале облачных приложений Office 365 безопасности выберите **Параметры** > **расширения безопасности**.

2. Найдите строку для агента SIEM. 

3. Нажмите кнопку с многоточием и выберите команду **Изменить**. (При редактировании агента SIEM не нужно повторно запустить файл .jar, автоматически обновляет).<br/>![Для изменения агента SIEM, щелкните многоточие и нажмите кнопку Изменить.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
### <a name="delete-a-siem-agent"></a>Удаление агента SIEM

1. На портале облачных приложений Office 365 безопасности выберите **Параметры** > **расширения безопасности**.

2. Найдите строку для агента SIEM. 

3. Нажмите кнопку с многоточием и затем выберите команду **Удалить**.<br/>![Чтобы удалить SIEM агентов, щелкните многоточие и нажмите кнопку Удалить.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

  
## <a name="next-steps"></a>Дальнейшие действия

- [Действия, связанные с использованием, после развертывания Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    
- [Просмотрите и выполнять операции с оповещениями](review-office-365-cas-alerts.md)
    
- [Групповой IP-адреса для упрощения управления](group-your-ip-addresses-in-ocas.md)
    

