---
title: Просмотр статистики ключевых слов для результатов поиска контента
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/30/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 9701a024-c52e-43f0-b545-9a53478aec04
description: Использовать функцию поиска статистики для отображения и сравнения статистики для нескольких поиска контента по безопасности Office 365 &amp; центре соответствия требованиям. Список ключевых слов можно также настроить при создании или изменении поискового запроса для получения усовершенствованные статистики, показывающие количество элементов соответствуют каждой ключевое слово или фразу с ключевыми словами.
ms.openlocfilehash: cb71b30b32ff6a24cd68ea5728063c2997d8ada0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534911"
---
# <a name="view-keyword-statistics-for-content-search-results"></a>Просмотр статистики ключевых слов для результатов поиска контента

После создания и выполнения поиска контента, можно просмотреть статистических данных об оценке результатов поиска. Это включает сводку результатов поиска (аналогично Сводка по оценке результатов поиска отображаются в области сведений), статистику запросов, такие как количество размещения содержимого с элементами, которые соответствуют запросов поиска и имя расположения контента у которых наиболее подходящие элементы. Вы можете отобразить статистики для поиска контента. Это позволяет быстро сравнение результатов для нескольких операций поиска и принятия решений о эффективность поисковых запросов.
  
Кроме того можно настроить поиск новых и существующих для возврата статистики для каждого ключевого слова в запросе поиска. Это позволяет сравнить количество результатов для каждого ключевого слова в запросе, а также для сравнения статистики ключевых слов из нескольких поиска.
  
Также можно загрузить Статистика поиска и статистику по ключевым словам в CSV-файл. Это позволяет использовать функции фильтрации и сортировки в Excel для сравнения результатов и подготовки отчетов для результатов поиска.
  
## <a name="get-statistics-for-content-searches"></a>Получение статистики для поиска контента

Отображение статистики для поиска контента:
  
1. В Office 365 безопасность &amp; центре соответствия требованиям, чтобы перейти на **поиска &amp; расследования** \> **поиска контента**.
    
2. В списке поиска выберите один или несколько операций поиска и нажмите кнопку **Статистика поиска**![кнопку поиска Статистика](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png).
    
    ![Выберите несколько операций поиска и нажмите кнопку Статистика поиска](media/1195c6c3-2e00-469d-8c29-85c1c7ebe6c7.png)
  
3. На странице " **Статистика поиска** " выберите один из следующих ссылок для просмотра сведений о выбранных поисковые запросы. 
    
    **Сводка**
    
    Эта страница отображает статистику подобных тем, отображаемые в области сведений на странице " **Поиск контента** ". Отображается статистика для всех выбранных поиска. Обратите внимание, что можно также повторно запустить выбранный поисковые запросы на этой странице, для обновления статистики. 
    
    ![Сводка статистики для выбранного операций поиска](media/abb663eb-b3d6-4f4c-a99f-55d20b0848af.png)
  
    a. имя поиска контента. Как было сказано ранее можно отображать и сравнение статистики для нескольких операций поиска.
    
    б. тип расположение содержимого, который был выполнен поиск. Каждой строки отображается статистика для почтовых ящиков, узлов и общих папок с указанным поиска.
    
    c. число расположения контента, содержащего элементы, соответствующие поисковый запрос. Для почтовых ящиков в этом Статистика также включает число архивные почтовые ящики, которые содержат элементы, соответствующие поисковый запрос.
    
    г. Общее число элементов все указанные расположения контента, которые соответствуют поисковый запрос. Типы элементов примеры сообщений электронной почты, элементы календаря и документы. Если элемент содержит несколько экземпляров класса ключевое слово, которое является, поиск, он только считается один раз в общее число элементов. Например если вы ищете слова «stock» или «мошенничества» и сообщения электронной почты содержит три экземпляра word «stock», он только считается один раз в столбце **элементов** . 
    
    e. общий размер всех элементов, найденных в выбранном расположении контента, которые соответствуют поисковый запрос. 
    
    **Запросы**
    
    Эта страница отображает статистику запросов поиска.
    
    ![Статистику запросов поиска для выбранного поиска](media/dc817526-dfb9-43d3-a14c-4c58077eb7bb.png)
  
    a. имя поиска контента, содержащий статистику запросов для строки.
    
    б. тип расположение содержимого, которые применимы к статистику запросов.
    
    c. Этот столбец указывает, какая часть поисковых запросов, Статистика могут быть применены. **Основной** указывает весь поисковый запрос. Если вы используете список ключевых слов, при создании или изменении поискового запроса, статистика для каждого компонента запроса включены в этой таблице. В этой статье для получения дополнительных сведений см [получить статистику по ключевым словам для поиска контента](#get-keyword-statistics-for-content-searches) . 
    
    г. Этот столбец содержит фактические поиска запросов, которые выполняются с помощью данного средства поиска контента. Обратите внимание, что средство автоматически добавляет несколько дополнительных компонентов для запроса, созданного. 

    - При поиске для всего содержимого в почтовых ящиках (указав не все ключевые слова), фактический ключевое слово запроса — это `size>=0` , чтобы возвращаются все элементы. 
    
     - При выполнении поиска SharePoint Online и OneDrive для бизнеса сайтов добавляются две следующие компоненты:
    
          **Не IsExternalContent:1** - исключает любое содержимое из SharePoint в локальной организации. 
    
          **Не IsOneNotePage:1** - исключает все файлы OneNote, так как они должны быть дубликатов любого документа, отвечающей поисковому запросу. 

    
    e. число размещения содержимого (определяется ** тип расположения ** столбца), которые содержат элементы, которые соответствуют поисковый запрос, указанный в столбце **запроса** . 
    
    f. количество элементов (из указанного расположения контента), которые соответствуют поисковый запрос, указанный в столбце **запроса** . Как объяснялось ранее, если элемент содержит несколько экземпляров класса ключевое слово, которое является, поиск, он только считается один раз в этого столбца. 
    
    ж. общий размер всех элементов, которые были найдены (в выбранном расположении контента), соответствующие запросов поиска в столбце **запроса** . 
    
    **Основные расположения**
    
    Эта страница отображает статистические данные о количестве элементов, которые соответствуют запросов поиска в каждом расположение содержимого, который был. В начало 1000 расположения отображаются. При просмотре статистики для нескольких операций поиска отображаются верхней расположения 1 000 для каждого поиска. Обратите внимание, что расположение содержимого не содержится на этой странице, если он не содержит все элементы, соответствующие поисковый запрос.
    
    ![Статистические данные о количестве элементы, найденные в расположения контента поиска](media/35a820b0-85d9-45d1-9a0c-c74bec803e67.png)
  
    a. имя расположение содержимого.
    
    б. тип расположение содержимого, которые применимы к статистики расположения.
    
    c. существует столбцов для каждой операции поиска, который отображается статистика по. В этом столбце отображаются номер (и общий размер) элементы, соответствующие запросов поиска в каждом расположение содержимого. Обратите внимание, что при отображается статистика для нескольких операций поиска, «NA» в этом столбце указывает, что расположение содержимого не был включен в, что поиск. 

## <a name="get-keyword-statistics-for-content-searches"></a>Получить статистику по ключевым словам для поиска контента

В предыдущем описываются страницы **запросов** показаны в поисковый запрос и номер (и размер) элементов, которые соответствуют запроса. Если вы используете список ключевых слов, при создании или изменении поискового запроса, можно получить расширенные статистики, показывающие количество элементов соответствуют каждой ключевое слово или фразу с ключевыми словами. Это может помочь быстро определять, какие части запроса эффективны наиболее (и бы). Например если ключевое слово возвращает большое число элементов, можно выбрать для уточнения запроса ключевого слова, чтобы сузить результаты поиска. Список ключевых слов можно настроить при создании или изменении поиска контента. 
  
Для создания списка ключевых слов и просматривать статистику по ключевым словам для поиска контента:
  
1. В Office 365 безопасность &amp; центре соответствия требованиям, чтобы перейти на **поиска &amp; расследования** \> **поиска контента**.
    
2. В списке контента поиска, нажмите кнопку и поиска и нажмите кнопку **Изменить** ![значок Правка](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
3. Щелкните **запрос** , а затем выполните следующие действия: 
    
    ![Установите флажок Показать ключевое слово списка и введите ключевое слово в каждой строке](media/73ef46dd-3d5c-415d-b5e7-c3559caaafe2.png)
  
    а. Установите флажок **Показать список ключевых слов** . 
    
    б. Введите ключевое слово или этап ключевого слова в строке в таблице ключевых слов. Например введите **бюджета** в первой строке, а затем введите **безопасности** во второй строке. 
    
4. После добавления ключевых слов, которые следует выполнить поиск и получить статистику по, нажмите кнопку **поиска** , чтобы запустить измененный поиска. 
    
5. После завершения поиска выберите в списке операций поиска и нажмите кнопку **поиска Статистика** ![кнопку поиска Статистика](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png). Также можно отображать и сравнение статистику по ключевым словам для нескольких операций поиска.
    
6. На странице " **Статистика поиска** " выберите **запрос** для отображения статистики ключевых слов для выбранного поисковые запросы. 
    
    ![Отображается статистика для каждого ключевого слова для выбранного поиска](media/e7910fa9-af93-4df9-92d0-e1e3e089e14f.png)
  
    Как показано на предыдущем рисунке отображается статистика для каждого ключевого слова; в том числе: 
    
    - Статистика ключевое слово для каждого типа контента включен в поиск расположения.
    
    - Фактические поисковый запрос для каждого ключевого слова, который включает любые условия из поискового запроса. 
    
    - Полный и запросов поиска (помечаются как **основной** в столбце **части** ) статистики для завершения запроса. Обратите внимание, что это же статистические данные, отображаемые на странице " **Сводка** ". 