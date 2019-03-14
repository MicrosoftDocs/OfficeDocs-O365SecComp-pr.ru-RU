---
title: Интеграция сервера SIEM с Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Вы можете интегрировать сервер SIEM с Office 365 Cloud App Security. В этой статье приводятся общие сведения о том, как она работает и как ее настроить.
ms.openlocfilehash: 82b5e0e6467bd42acba3c40d67e4e0363a7e0f72
ms.sourcegitcommit: 4abcc03497478abf1ae7fc84792f44360d8e59c1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2019
ms.locfileid: "30548589"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a>Интеграция сервера SIEM с Office 365 Cloud App Security
  
|Ознакомительная версия * *\>**|Планирование * *\>**|Развертывание * *\>**|Использование * * * *|
|:-----|:-----|:-----|:-----|
|[Начало оценки](office-365-cas-overview.md) <br/> |[Начало планирования](get-ready-for-office-365-cas.md) <br/> |Вот что вам!  <br/> [Следующее действие](utilization-activities-for-ocas.md) <br/> |[Начало использования](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a>Общие сведения и необходимые условия

Для обеспечения централизованного мониторинга оповещений можно интегрировать [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) со сведениями о безопасности и сервером управления событиями (SIEM). Это особенно полезно для организаций, использующих облачные службы и локальные серверные приложения. Вы можете интегрировать сервер SIEM для получения оповещений и действий из Office 365 Cloud App Security на сервер SIEM. Интеграция с сервером SIEM позволяет группе безопасности улучшить защиту приложений Office 365, сохранив при этом обычный рабочий процесс безопасности, путем автоматизации определенных процедур безопасности и корреляции между облачными и локальными событиями.  
  
При первоначальной интеграции сервера SIEM с Office 365 Cloud App Security оповещения за последние два дня пересылаются на сервер SIEM, а также все оповещения в зависимости от выбранных фильтров. Кроме того, если отключить эту функцию для расширенного периода, то при его повторном включении будут переадресованы два предыдущих дня оповещения, а затем все оповещения.

### <a name="siem-integration-architecture"></a>Архитектура интеграции SIEM

Агент SIEM настраивается в сети Организации. При развертывании и настройке агент SIEM извлекает типы данных, которые были настроены (оповещения) с помощью API Office 365 Cloud App Security REST API. Затем трафик отправляется по зашифрованному HTTPS-каналу на порте 443.
  
Когда агент SIEM получает данные из Office 365 Cloud App Security, он отправляет сообщения syslog на локальный сервер SIEM с помощью конфигураций сети, которые предоставляются во время установки (TCP или UDP с настраиваемым портом).

![Архитектура Cloud App Security and SIEM and Cloud App](media/siem-architecture.png)

### <a name="supported-siem-servers"></a>Поддерживаемые серверы SIEM

Office 365 Cloud App Security в настоящее время поддерживает следующие серверы SIEM:
- Micro Focus Арксигхт
- Универсальный ЦЕФ

### <a name="prerequisites"></a>Необходимые компоненты

- Для выполнения задач, описанных в этой статье, необходимо быть глобальным администратором или администратором безопасности. Ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md)

- Для Организации необходимо [включить безопасность облачНого приложения Office 365](turn-on-office-365-cas.md) .

- Для Office 365 должна быть включена функция [ведения журнала аудита](turn-audit-log-search-on-or-off.md)

- Для настройки интеграции сервера SIEM должен быть установлен стандартный сервер, отвечающий следующим требованиям:
    - ОС: Windows или Linux (это может быть виртуальная машина)
    - ЦП: 2
    - Место на диске: 20 ГБ
    - ОЗУ: 2 ГБ
    - Установлен [Java Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
    - Брандмауэр настроен в соответствии с [требованиями к сети](https://docs.microsoft.com/cloud-app-security/network-requirements)

- Необходимо получить сведения об удаленном **узле syslog** и **номере порта сислот**. Эту информацию можно искать администратору сети или администратору безопасности. 

- Вы должны согласиться с [условиями лицензионного соглашения](https://go.microsoft.com/fwlink/?linkid=862491) на использование программного обеспечения, чтобы скачать [JAR – файл](https://go.microsoft.com/fwlink/?linkid=838596) , который потребуется для интеграции сервера SIEM.
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a>Шаг 1: Настройка агента SIEM в Office 365 Cloud App Security

1. Перейдите на портал Cloud App Security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполните вход.
  
2. Щелкните **Параметры** \> **расширения безопасности**, а затем выберите SIEM агенты.<br/>
![Выберите параметры _Гт_ расширения безопасности](media/Settings-SecurityExtensions.png)

3. Выберите **Добавить агент SIEM**.<br/>![Выберите Добавить агент SIEM.](media/SIEMAgents.png)
    
4. Нажмите кнопку **запустить мастер**.<br/>![Получение справки или запуск мастера](media/HelpOrWizard.png) 
    
5. В разделе **Общие** действия укажите имя и **выберите формат SIEM** и настройте любые **Дополнительные параметры** , относящиеся к этому формату. Затем нажмите кнопку **Далее**.<br/>![Укажите имя и тип](media/ChooseAgentTypeAndName.png)
    
6. На удаленном этапе **syslog** укажите IP-адрес или имя узла **удаленного сервера Syslog** и **номер порта syslog**. Выберите TCP или UDP в качестве удаленного протокола syslog. (Вы можете обратиться к администратору сети или администратору безопасности, чтобы получить эти сведения, если у вас их нет.) Затем нажмите кнопку **Далее**.<br/>![Указание сведений об удаленном syslog](media/ArcSightS1Syslog.png)
  
7. На шаге **типы данных** выполните одно из следующих действий, а затем нажмите кнопку **Далее**.
    - Оставить значение по умолчанию для **всех оповещений**<br/>OR
    - Щелкните **все оповещения**, а затем выберите **определенные фильтры**. Определите фильтры, чтобы выбрать типы оповещений, которые нужно отправить на сервер SIEM.
<br/>![Типы данных шаг мастера](media/ArcSightS1ExportOptions.png)
  
8. На экране приветствия Скопируйте маркер и сохраните его для последующего использования.<br/>![Экран агента SIEM](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> На этом шаге вы настроили агент SIEM в Office 365 Cloud App Security, но интеграция сервера SIEM еще не завершена. Перейдите к следующему шагу, чтобы продолжить интеграцию сервера SIEM.

После нажатия кнопки Закрыть и закрытия мастера на экране расширения безопасности можно увидеть агент SIEM, добавленный в таблице. Отображается состояние **создано** , пока оно не будет подключено позже.

![Создан агент SIEM](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a>Шаг 2: Скачайте JAR — файл и запустите его на сервере SIEM

1. Скачайте [агент Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) и распакуйте папку. Чтобы продолжить, необходимо согласиться с [условиями лицензионного соглашения](https://go.microsoft.com/fwlink/?linkid=862491) на использование программного обеспечения. 
    
2. ИзВлеките JAR файл из архивной папки и запустите его на сервере SIEM.
    
3. После запуска файла выполните следующую команду:<br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a>Важные замечания

- Имя файла может различаться в зависимости от версии агента SIEM. 

- Рекомендуется запускать файл JAR на сервере SIEM во время установки сервера.

    - **Windows**: запуск в качестве запланированного задания, поэтому необходимо настроить задачу для запуска независимо от того, **вошел ли пользователь в систему, или нет** , **остановить задачу, если она выполняется дольше, чем** параметр.

    - **Linux**: добавьте команду Run с параметром **&** в `rc.local` файл. <br/>Пример:<br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- Параметры в квадратных скобках являются необязательными, и их следует использовать только в случае необходимости. Используйте следующие переменные:

    - **Дирнаме** это путь к каталогу, который вы хотите использовать для локальных журналов отладки агентов.

    - **Address [:P ОРТ]** — это адрес прокси-сервера и порт, который сервер использует для подключения к Интернету.

    - **Token** — это маркер агента SIEM, скопированный в первой процедуре.

    - Чтобы получить справку, введите `-h`. 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a>Шаг 3: Проверка работоспособности агента SIEM

1. Убедитесь, что состояние агента SIEM на портале Cloud App Security (Office 365) не отображается как **Ошибка подключения** или **отключено** , а также отсутствуют уведомления агентов.<br/>Например, здесь можно увидеть, что сервер SIEM подключен:<br/>![Подключенный сервер SIEM](media/siem-connected.png)<br/>Кроме того, вы увидите, что сервер SIEM отключен:<br/>![Сервер SIEM не подключен](media/siem-not-connected.png) 
  
2. Убедитесь, что в вашем syslog/SIEM Server получены оповещения от Office 365 Cloud App Security.
  
## <a name="what-the-logfiles-look-like"></a>Как выглядят файлы журнала

Ниже приведен пример файла журнала оповещений, который можно отправить на сервер SIEM:

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

А вот еще один пример, на этот раз в формате ЦЕФ:


|Имя поля ЦЕФ  | Описание  |
|---------|---------|
|start     | Метка времени оповещения        |
|end     | Метка времени оповещения        |
|RT     | Метка времени оповещения        |
|направлен     | Описание оповещения, как показано на портале Cloud App Security для Office 365        |
|SUSE     | пользователь темы оповещения        |
|Дестинатионсервиценаме     | исходное приложение оповещения, например Office 365, SharePoint или OneDrive        |
|Кслабел     | Различаются (метки имеют разный смысл). Как правило, метки говорят сами по себе, как Таржетобжектс.        |
|cs     | Сведения, соответствующие метке (например, конечному пользователю оповещения в соответствии с примером метки);        |

## <a name="additional-tasks-as-needed"></a>Дополнительные задачи (при необходимости)

После настройки сервера SIEM и интеграции его с Office 365 Cloud App Security может потребоваться повторно создать маркер, изменить агент SIEM или удалить агент SIEM. В следующих разделах описано, как выполнить эти задачи.

### <a name="regenerate-a-token"></a>Повторное создание маркера

Если вы потеряете маркер, вы можете восстановить его. 

1. [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)на портале Cloud App security () Office 365 выберите **параметры** > **расширения безопасности**.

2. В таблице выберите строку для агента SIEM. 

3. Нажмите многоточие, а затем выберите пункт **повторно создать маркер**.<br/>![Повторно создайте маркер, нажав кнопку с многоточием для своего агента SIEM.](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
### <a name="edit-a-siem-agent"></a>Изменение агента SIEM

1. [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)на портале Cloud App security () Office 365 выберите **параметры** > **расширения безопасности**.

2. Поиск строки для агента SIEM. 

3. Нажмите кнопку с многоточием, а затем выберите команду **изменить**. (Если вы изменяете агент SIEM, вам не потребуется повторно запускать файл. jar; он обновляется автоматически.) <br/>![Чтобы изменить агент SIEM, нажмите многоточия, а затем нажмите кнопку Изменить.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
### <a name="delete-a-siem-agent"></a>Удаление агента SIEM

1. [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)на портале Cloud App security () Office 365 выберите **параметры** > **расширения безопасности**.

2. Поиск строки для агента SIEM. 

3. Нажмите многоточие, а затем выберите команду **Удалить**.<br/>![Чтобы удалить агент SIEM, нажмите многоточия, а затем нажмите кнопку Удалить.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

  
## <a name="next-steps"></a>Дальнейшие действия

- [Действия, связанные с использованием, после развертывания Office 365 Cloud App Security](utilization-activities-for-ocas.md)
    
- [Просмотр оповещений и выполнение действий с ними](review-office-365-cas-alerts.md)
    
- [Группировка IP-адресов для упрощения управления](group-your-ip-addresses-in-ocas.md)
    

