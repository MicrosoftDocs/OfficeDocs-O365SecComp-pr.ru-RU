---
title: Office 365 внутренних ведения журнала для разработки Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/18/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Объяснение как внутренних ведения журнала для разработчиков Office 365 группы works.
ms.openlocfilehash: 1a613584b6b815524435acb20db7a8022d95e3bc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534555"
---
# <a name="internal-logging-for-office-365-engineering"></a>Внутренняя регистрация для инженеров Office 365
В дополнение к событиям и журнала данных, которые доступны для клиентов имеется также системой семейства внутренних данных, доступные для инженеров Office 365. Различные типы данных журнала загружаются из серверов Office 365 внутренним, большая данных, службы с именем Cosmos вычислений. Каждой группы службы отправляет журналы аудита из соответствующих серверах в базу данных Cosmos для объединения и анализа. Передача данных происходит через FIPS 140-2-проверенные подключения по протоколу TLS на специально утвержденных порты и протоколы, с помощью инструмента конфиденциальным автоматизации загрузчик данных Office (ODL).

Служба группы используют Cosmos функции централизованного хранилища для проведения анализа использования приложений, для измерения системы и эффективности производства и выполнять поиск отклонений и шаблоны, которые может указывать на проблемы или проблемы безопасности. Каждой группы службы отправляет базового журналов в Cosmos, в зависимости от того, необходимых для анализа, которые часто включают:
- Журналы событий
- Журналы AppLocker
- Данные о производительности
- Данных System Center
- Записи регистрации вызовов
- Качество взаимодействия данных
- Журналы служб IIS веб-сервера
- Журналы SQL Server
- Syslog данных
- Журналы аудита безопасности

Перед загрузкой данных в Cosmos, ODL приложением очистки службы для маскирование всех полей, которые содержат данные клиента, например сведения клиента и характера конечных пользователей и замените этим полям значения хэш-функции. Журналы анонимен и хэш переопределяются и затем отправить в Cosmos. Группы обслуживания запросов с заданной областью выполняться для своих данных в Cosmos для корреляции предупреждений и отчетов. Период хранения данных журнала аудита в Cosmos определяет, какие группы обслуживания; Большинство данных журнала аудита сохраняется 90 дней или больше для поддержки расследований инцидентов безопасности и для соответствия нормативным требованиям.

Доступ к данным Office 365, хранящиеся в Cosmos ограничен авторизованный персонал. Microsoft ограничивает управления функциональные возможности аудита ограниченный набор службы участников группы, ответственных за функциональные возможности аудита. Эти участники группы не имеют возможности для изменения или удаления данных Cosmos и регистрируются все изменения механизма ведения журнала для Cosmos и проверены.

Каждой группы службы обращается к его данных журнала для анализа с помощью авторизации определенных приложений для проведения анализа определенного. Например группа безопасности Office 365 использует данные из Cosmos через средство синтаксического анализа собственный журнал событий для согласования, оповещение и статистические отчеты, предусматривающей действие подозрительные возможные действия в рабочей среде Office 365. Отчеты на основе этих данных используются, чтобы исправить уязвимые места системы, а также для повышения общей производительности службы. Если определенного оповещения или отчета требуется для дальнейшей исследования, персонала службы можно запросить импортировать данные обратно в службе Office 365. Начиная с определенным журнала, импортированные из Cosmos в шифрования и персонала службы не имеют доступа к ключам расшифровки, журнала конечного программными средствами передается через службу расшифровки, которая возвращает результаты с областью для авторизованного службы персонала. Любой уязвимостей в системе из этого упражнения сообщает и развертывает использование каналов управления происшествиями стандартных безопасности корпорации Майкрософт.