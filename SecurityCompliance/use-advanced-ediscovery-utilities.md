---
title: Использование служебных программ Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Узнайте о служебных программ в Office 365 расширенного обнаружения электронных данных, включая журнал обращения, очистку данных, обработки ошибок, изменить прозрачность анализ и релевантности.  '
ms.openlocfilehash: a68c98dd353971fcaa13fdc6b8e12bcf00c2faf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534330"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a>Использование служебных программ Office 365 Advanced eDiscovery

> [!NOTE]
> Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Служебные программы, которые отображаются и доступны в расширенной eDiscovery зависят от роли пользователя и контекста.
  
## <a name="case-log"></a>Журнал обращений

Журнал обращения предоставляет подробный список функций приложения обработки действий, которые можно использовать для отслеживания, устранение неполадок и устранение ошибок и предупреждений. Журнал можно создается и хранятся на узел или сервер либо непосредственно в адрес электронной почты.
  
Файл журнала можно также загрузить на клиентский компьютер. Параметр загрузки клиента могут включаться и отключаться согласно конфигурации и роли.
  
1. В строке меню щелкните значок **Cogwheel** . 
    
2. В **Параметры и служебные программы \> служебных программ** выберите **журнала обращения \> установки**.
    
3. Выберите **уровень журнала** следующим образом: 
    
  - **Стандартный**: включает в себя данные журнала basic. Этот параметр обычно требуются для мониторинга и следует использовать, если не рекомендуется, в противном случае.
    
  - **Минимальная**: используется для очень больших случаев и возвращает только последних данных.
    
4. Нажмите кнопку **Запуск примера журнала**. Журнал создается и отображается путь. Сведения о ходе выполнения задач для текущего и последнего задачи отображается в области состояния задач.
    
## <a name="clear-data"></a>Очистка данных

Если это необходимо удалить или повторной инициализации данные вариантов, должен быть инициализирован экземпляр базы данных. Служебная программа очистки данных удаляет все указанные элементы из социальной базы данных, текстовые файлы, case папки и накопленная результатов. Функция может выполняться только администратором.
  
> [!IMPORTANT]
> Это действие не является обратимое и будет снимите все теги релевантности и анализа, выполняемой эксперт. Сохраните резервную копию данных, если это необходимо. Этот параметр используется с особой осторожностью. Удаление файлов с тегами и ранжированных могут влиять на релевантности результатов. 
  
1. В строке меню щелкните значок **Cogwheel** . 
    
2. В **Параметры и служебные программы \> служебных программ** выберите **очистку данных \> установки**.
    
3. Выберите соответствующее значение параметра сведения для инициализации:
    
  - **Релевантность**: Удаляет все операции, выполняемые в релевантности, включая определения нагрузок и связи файлов для загрузки. Удаляет все примеры и маркировки.
    
  - **Рядом с дубликаты и электронной почты потоков**: удаляются все данные анализа рядом с дубликатов и электронной почты потоков.
    
  - **Темы**: Удаляет данные, связанные с тем.
    
  - **Экспортировать журнал**: Удаляет сведения о журнале экспорт пакетов.
    
4. Нажмите кнопку **Очистить данные**. Данные вариантов снят. Сведения о ходе выполнения задач для текущего и последнего задачи отображается в области **состояния задачи** . 
    
## <a name="modify-relevance"></a>Изменение релевантности

В этом разделе описывается, как пропустить или откат примера релевантности.
  
1. В строке меню щелкните значок **Cogwheel** . 
    
2. В **Параметры и служебные программы \> служебных программ** выберите **Изменить релевантности**.
    
3. Выберите один из вариантов: 
    
  - **Пример текущей пропустить — для текущего пользователя**: это будет пометить, как **Пропустить**все файлы без тегов в образце open обращения пользователя, выполняющего программу. На файлы, помеченные как **Пропустить**не выполняется обработка релевантности.
    
  - **Пропустить текущий пример — все открытые примеры**: это будет пометить, как **Пропустить**все файлы без тегов в всех открытых примеры для всех пользователей. Этот параметр не рекомендуется, если пользователи в настоящее время тегов примеры.
    
  - **Откат последнего примера**: последнего выполненного релевантности, учебные примеры будет выполнен откат, независимо от того, будет ли это до или после процесса «Вычислить». Откат дополнительной пример не допускается.
    
4. Нажмите кнопку **выполнить** , чтобы выполнить. 
    
## <a name="transparency-analysis"></a>Анализ прозрачность

Служебная программа анализа прозрачность включает подробное представление файлов и их назначенный показатель релевантности. Отчет можно использовать, как выполняется проверка работоспособности или для сравнения релевантности файла, определяется специалиста по проверке по сравнению с релевантности, назначенный с расширенной обнаружения электронных данных. 
  
В дополнение к показателям релевантности расширенной eDiscovery вычисляет и назначает вес ключевого слова, которые необходимо учитывать контекст ключевого слова. То же слово в файле можно назначить разные веса, в зависимости от контекста и расположение. Каждое ключевое слово помечается с помощью увеличение масштаба интенсивности цвета от желтого цвета до темно-оранжевый и различная оттенки серого цвета. Цвет используется для отображения слово относительный положительное или отрицательное влияние на оценку релевантности. 
  
В сценарий делами проблем с несколькими прозрачность анализа созданием отчета для каждой проблемы.
  
1. В строке меню щелкните значок **Cogwheel** . 
    
2. В **Параметры и служебные программы \> служебных программ** выберите **анализа прозрачность \> установки**.
    
3. В ** идентификатор файла **, введите идентификатор файла файла для обработки.
    
4. В списке **проблему** выберите соответствующую проблему. 
    
5. Нажмите кнопку **прозрачность анализа**. По завершении отображается отчет анализа прозрачность для файла, показано, как цвета ключевое слово соответствуют общий показатель релевантности.
    
## <a name="see-also"></a>См. также

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Определение параметров case и клиента](define-case-and-tenant-settings-in-advanced-ediscovery.md)
