---
title: Просмотр custodian аудита активности
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
ms.openlocfilehash: 8219ae8a061f6d08dd37da5b7f2974dd86c68f04
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608230"
---
# <a name="viewing-custodian-audit-activity"></a>Просмотр custodian аудита активности

Требуется для поиска, если пользователь просматривать конкретного документа или очищены элемента из их почтовых ящиков? Расширенные обнаружения электронных данных (Просмотр) теперь интегрированы с существующей аудита журнала средства поиска в центре соответствия требованиям & безопасности. С помощью этой внедренных качества, можно использовать средство управления Custodian расширенной обнаружения электронных данных (Предварительная версия) для облегчения изучение, легко доступ к и найдите действие custodians в случае.

## <a name="before-you-begin"></a>Перед началом работы

Вы должны быть назначены роли журналы аудита только для просмотра или журналов аудита в Exchange Online поиск в журнале аудита Office 365. По умолчанию эти роли назначенные Управление соответствием требованиям и группы ролей управления организацией на странице "разрешения" в центре администрирования Exchange. Чтобы предоставить пользователю возможность выполнять поиск в журнал аудита расширенной обнаружения электронных данных (Просмотр) с минимальным уровнем привилегий, можно создать пользовательскую группу ролей в Exchange Online, добавить роль журналы аудита только для просмотра или журналов аудита и нажмите Добавить пользователя в качестве нового группа роль должна быть членом згруппировать. Для получения дополнительных сведений см ролей в Exchange Online.

> [!IMPORTANT]
> Если пользователь назначение роли журналы аудита только для просмотра или журналов аудита на странице "разрешения" в центре соответствия требованиям & безопасности, они будут поиск в журнале аудита Office 365. Необходимо назначить разрешения в Exchange Online. Это основной командлет используется для поиска по журналу аудита — это командлет командной Exchange Online.

## <a name="step-1-create-an-advanced-ediscovery-preview-audit-log-search"></a>Шаг 1: Создание поискового запроса журнала аудита расширенной обнаружения электронных данных (Предварительная версия)

   1. Выберите существующий случай **безопасности & центре соответствия требованиям > расширенной обнаружения электронных данных (Просмотр)**.
   
   2. Перейдите на вкладку « **Custodians** » и выберите custodian.
   
   3. Выбрав custodian, нажмите кнопку **Просмотр Custodian активности** в панели сведений.
   
   4. Настройте следующие условия поиска:
      
      a. **мероприятий** - нажмите кнопку раскрывающегося списка для отображения действия, которые можно выполнить поиск. После запуска поиска отображаются только записи аудита для выбранного действия. Выбрав **Показать результаты для всех действий** будет отображаться результаты для всех действий, необходимых для других критериев поиска.
      
      б. **Дата начала и Дата окончания** — выберите дату и время диапазона просмотра событий, возникших в течение этого периода. По умолчанию выбрано за последние семь дней. Дата и время представлены в формате по Гринвичу (UTC). Максимальный период, которые можно выбрать — один год.
      
      c. **Custodians** - щелкните в этом поле выберите определенного custodian для отображения поиска по результатам. В списке результатов отображаются записи аудита для выбранной операции, выполненные для пользователей, выбранного в этом поле.
    
    1. Нажмите кнопку **поиска** , чтобы запустить поиск, используя условия поиска. Результаты поиска загружаются и после некоторое время они отображаются в области результатов на странице поиска Custodian действий. 

## <a name="step-2-view-the-audit-log-search-results"></a>Шаг 2: Просмотр результатов поиска журнала аудита

Результаты поиска журнала аудита отображаются в области результатов на странице журнала аудита Custodian. Не более 5000 (самые новые) событий отображаются с шагом 150 событий. Чтобы отобразить дополнительные события можно использовать полосы прокрутки в области результатов или вы нажимаете клавишу Shift + End просмотра событий, затем 150.

Результаты содержат следующие сведения о каждом событии, возвращенных в результате поиска.
- **Дата**: Дата и время (в формате UTC) при возникновении события.

- **IP-адрес**: IP-адрес устройства, который использовался при входе действия. IP-адрес отображается в формате адреса IPv4 или IPv6.

- **Пользователь**: пользователя (или учетная запись службы), выполнить действие, которое вызвало событие.

- **Действие**: операции, выполненные пользователем. Это значение соответствует действия, выбранные в раскрывающемся списке действия. Для события из журнала аудита действий администратора Exchange значение в этом столбце — это командлет Exchange.

- **Элемент**: объектов, которые были созданы или изменены в результате соответствующих действий. Например файл, который был просматривать или изменять или учетная запись пользователя, который был обновлен. Не все действия иметь значение в этом столбце.

- **Подробности**: Дополнительная информация об активности. Еще раз не все действия будут иметь значение.

## <a name="step-3-filter-the-search-results"></a>Шаг 3: Фильтровать результаты поиска

В дополнение к сортировке, также можно отфильтровать результаты поиска журнала аудита. Это может помочь быстро фильтровать результаты для определенных пользователей или активности. 

Для фильтрации результатов:

 1. Создание и выполнение поискового запроса журнала аудита.
  
2. При отображении результатов, щелкните **фильтровать результаты**.
 
3. Ключевое слово полей отображаются под заголовком каждого столбца.
  
4. Выберите один из поля в разделе заголовка столбца и введите слово или фразу, в зависимости от столбца, по которому выполняется фильтрация на. Результаты будут динамически перенастроить просмотра событий, которые соответствуют фильтра.
  
5. Чтобы очистить фильтр, нажмите кнопку **X** в поле фильтра или просто щелкните **Скрыть фильтрации**.

## <a name="export-the-search-results-to-a-file"></a>Экспорт результатов поиска в файл

Результаты поиска журнала аудита можно экспортировать в файл значений, разделенных запятыми (CSV) запятой на локальном компьютере. Можно открыть этот файл в Microsoft Excel и использовать компонентов, таких как поиск, сортировка, фильтрация и Разделение одного столбца (, который содержит ячейки с несколькими значениями) в несколько столбцов.

1. Запустить поиск журнала аудита и нажмите Изменить условия поиска, пока получите требуемых результатов.
  
2. Нажмите кнопку Экспорт результатов и выберите один из следующих вариантов:

    - **Сохранить загружены результатов:** Выберите этот параметр, чтобы экспортировать только записи, которые отображаются в области **результатов** на странице **поиска журнала аудита Custodian** . CSV-файл, который будет загружен содержит те же столбцы (и данные) отображается на странице (даты, пользователей, активность, элемента и подробные сведения). (Под названием **более**) дополнительный столбец включен в CSV-файл, содержащий дополнительные сведения из записи журнала аудита. Так как экспорте одинаковые результаты, которые загружаются (и для просмотра) на странице поиска журнала аудита экспортируются не более 5000 записей.
        
    - **Загрузка всех результатов:** Выберите этот параметр, чтобы экспортировать все записи из журнала аудита Office 365, которые соответствуют условиям поиска. Для большого набора результатов поиска выберите этот параметр, чтобы загрузить все записи из журнала аудита в дополнение к 5000 результатов, которые могут быть отображены на странице поиска **журнала аудита Custodian** . Этот параметр, загрузите необработанные данные из журнала аудита в CSV-файл и содержит дополнительные сведения из журнала аудита записи в столбце с именем AuditData. Может потребоваться больше времени для загрузки файла, если выбран этот параметр экспорта, так как файл может быть значительно больше, если выбран параметр других загружается.
    
      > [!IMPORTANT]
      > Не более 50 000 записей в CSV-файл можно загрузить из поиска журналов аудита единого. Если 50 000 записей загружаются в CSV-файл, вероятно, можно предположить, что более 50 000 событий, выполнены условия поиска. Чтобы экспортировать больше, чем это ограничение, попробуйте использовать диапазон дат для уменьшения количества записей журнала аудита. Может потребоваться использовать несколько поисков для работы с меньшего размера диапазона дат для экспорта более 50 000 записей.
        

3. Когда вы выберете параметр экспорта, появится в нижней части окна, предлагающее Открытие CSV-файл, сохраните его в папку файлы для загрузки и сохраните его в указанную папку

[!NOTE] 
 Дополнительные сведения о просмотре, фильтрация или экспорт результатов поиска в журнале аудита см.
   - Просмотр списка аудита действий 
   - Перед началом: Журналы единой аудита
 