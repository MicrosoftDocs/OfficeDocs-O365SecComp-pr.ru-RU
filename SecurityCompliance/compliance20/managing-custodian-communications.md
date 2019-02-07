---
title: Работа с коммуникации в расширенной обнаружения электронных данных (Предварительная версия)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: b27d6cca0382b18123cae4106f77ce0dcdf5e525
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608295"
---
# <a name="working-with-communications-in-advanced-ediscovery-preview"></a>Работа с коммуникации в расширенной обнаружения электронных данных (Предварительная версия)

Расширенные обнаружения электронных данных (Просмотр) позволяет юридических отделов для упрощения их процессов отслеживания и распространения уведомлений удержания по юридическим причинам. Функция communications custodian позволяет юридических отделов для управления и автоматизации процессы всей удержания по юридическим причинам--из уведомления, напоминаний и эскалации — все в одном месте.

## <a name="what-is-a-legal-hold-notification"></a>Что такое удержания по юридическим причинам уведомления?

Уведомление удержания по юридическим причинам (также известной как *Судебное удержание*) — это уведомление о из юридический отдел организации сотрудников, временного персонала или других custodians данных. Такие уведомления Проинструктируйте custodians для сохранения электронных сведения (ESI), а также все материалы, которые можно применять активного или предстоящее правовых вопросах. Юридические групп необходимо знать, что каждый custodian получил, читать и понимания и согласования в соответствии с заданным инструкции.

## <a name="the-legal-hold-notification-process"></a>Юридические удержания процесс уведомления

Организация имеет долг, чтобы сохранить информацию, при подразделения о предстоящих судебного разбирательства или нормативные расследования. Для соответствия требованиям его сохранение организации сразу же сообщает о возможных custodians о своих долг, чтобы сохранить информацию. 

С расширенной обнаружения электронных данных (Предварительная версия) юридических групп можно создавать и настраивать их рабочий процесс уведомления удержания по юридическим причинам. Функция Custodian коммуникаций позволяет юридических команд для настройки следующих уведомления и рабочих процессов:

1. **Обратите внимание на выдачу**: уведомление удержания по юридическим причинам является выдается (или инициировал) с уведомление от юридического отдела для custodians, которые могут иметь информацию о делами данному. Это сообщение указывает, что эти custodians, чтобы сохранить все сведения, может понадобиться для обнаружения. 
   
2.  **Обратите внимание на то повторное присвоение**: во время случае custodians может потребоваться сохранить дополнительные или меньше сведений, чем было указано ранее. Для этого сценария можно обновлять существующие уведомление о удержания и повторно выдача вашей custodians.

3.  **Обратите внимание, выпуск**: после решена вопрос и custodian больше не может быть долг хранения, custodian можно отменить, чтобы сведения — это больше не сохраняется, если не требуется. Кроме того ваше custodian будут извещены, они не были в разделе долг хранением и не выполнено инструкции для возобновления их активности.

4. **Напоминания и эскалации**: в некоторых случаях в только что выдачи уведомление недостаточно для удовлетворения требований законодательной проверки. С каждым уведомлением юридических команды можно запланировать набор напоминание и распространение рабочих процессов для исполнения автоматически с custodians не отвечает.

    - **Напоминания**: после удержания по юридическим причинам уведомление выдается или повторно отправлен в набор custodians, организации могут настроить напоминания для оповещения не отвечает custodians. 

    - **Эскалации**: В некоторых случаях, если custodian остается отвечает даже после набора напоминаний, юридических группы можно настроить рабочего процесса распространения для уведомления custodian и его руководителю.

## <a name="role-groups-and-permissions"></a>Группы ролей и разрешений 

Юридические команды можно управлять и разделять их действия с помощью групп ролей, связанных с обнаружения электронных данных и разрешения в центре соответствия требованиям & безопасности. 

Создание и управление уведомлениями удержания по юридическим причинам, пользователя необходимо быть членом следующих групп ролей:

- **Обнаружение электронных данных диспетчера** - участникам группы ролей можно создавать и управлять вариантах eDiscovery. Они добавлять и удалять участников, поместите custodians и размещения содержимого на удержание, управление уведомлениями удержания по юридическим причинам, создание и изменение поиск содержимого, связанного с дела, экспортировать результаты поиска контента и Подготовка результатов поиска для анализа в расширенной обнаружение электронных данных (Просмотр). Существуют две подгруппы в эту группу ролей. Различия между этих подгруппы основано на область.

  - **Обнаружение электронных данных диспетчера** - можно просмотреть и изменить вариантах eDiscovery, создаваемые и должны быть членом. Если другой eDiscovery Manager создает случай, но не добавляет второй обнаружения электронных данных диспетчера как член этого варианта, второй eDiscovery диспетчер не сможет для просмотра или откройте case на странице электронных данных в центре соответствия требованиям & безопасности. Диспетчеры обнаружения электронных данных можно также получить доступ их вариантов в расширенной обнаружения электронных данных (Просмотр) для выполнения задач анализа.

  - **Обнаружение электронных данных администратор** - могут выполнять все задачи Управление делами, которые можно выполнять диспетчеру eDiscovery. Кроме того eDiscovery администратору выполнить следующие действия.
    
    - Просматривать все дела, отображаемые на странице Обнаружение электронных данных.
    - Управление любом случае в организации, после они добавляют себя в качестве члена обращения.
    - Доступ к данным вариантов в расширенной eDiscovery (Просмотр) для любого случая в организации.

Дополнительные сведения можно [назначать разрешения обнаружения электронных данных в центре соответствия требованиям & безопасности Office 365](../assign-ediscovery-permissions.md).