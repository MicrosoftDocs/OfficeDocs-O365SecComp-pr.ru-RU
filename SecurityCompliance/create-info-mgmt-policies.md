---
title: Создание и применение политик управления сведениями
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/16/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- OSU150
- OSU160
- MET150
ms.assetid: 8ccac9e4-3a50-49fa-a95b-d186032a6ee3
description: Политики управления сведениями включите вашей организации для элемента управления, сколько времени требуется сохранение контента, для аудита, что делать с контентом, а также добавлять штрих-коды или метки в документ. Политику можно помощь при внедрении соблюдения юридических и правительственными нормативами или внутренних бизнес-процессов. С правами администратора, можно настроить политику для управления как для отслеживания документов и сколько времени требуется сохранять документы.
ms.openlocfilehash: cc15b7d830e6c13e00045f7e4b672ac4a755a70e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534533"
---
# <a name="create-and-apply-information-management-policies"></a>Создание и применение политик управления сведениями

Политики управления сведениями включите вашей организации для элемента управления, сколько времени требуется сохранение контента, для аудита, что делать с контентом, а также добавлять штрих-коды или метки в документ. Политику можно помощь при внедрении соблюдения юридических и правительственными нормативами или внутренних бизнес-процессов. С правами администратора, можно настроить политику для управления как для отслеживания документов и сколько времени требуется сохранять документы.
  
Можно создать могут получать политики управления сведения в трех различных местах в иерархии сайтов из широкой для узкой:
  
- Создайте политику для использования на нескольких типов контента в пределах семейства веб-сайтов.
    
- Создание политики для типа контента сайта.
    
- Создание политики для списка или библиотеки.
    
Для получения дополнительных сведений см [политик управления сведениями](intro-to-info-mgmt-policies.md).
  
## <a name="create-a-policy-for-multiple-content-types-within-a-site-collection"></a>Создание политики для нескольких типов контента в пределах семейства веб-сайтов
<a name="__toc261001590"> </a>

Чтобы убедиться, что политики сведениями применяется ко всем документам определенного типа в пределах семейства веб-сайтов, рассмотрите возможность создания политики на уровне семейства сайтов и затем применить политику к типам контента. Они называются политики семейства узлов. 
  
1. На домашней странице семейства сайтов \> **Параметры**![кнопка параметров 2016 SharePoint в строке заголовка. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Параметры сайта**.
    
    На сайте SharePoint подключенной группы нажмите кнопку **Параметры**, щелкните **Содержимое сайта**и выберите пункт **Параметры сайта**. 
    
2. На странице "Параметры узла" в разделе **Администрирование семейства веб-сайтов** \> **Содержимого шаблоны политики типов**. 
  
![Ссылка на шаблон политики типа содержимого на странице "Параметры сайта"](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. На странице политики \> **Создать**. 
    
4. Введите имя и описание для политики и затем запись правила политики краткое описание пользователям возможности политики.
    
5. Содержится в следующем разделе о создании политик для типа контента сайта узнать, как настроить компоненты, которые необходимо связать с политикой. 
    
6. Нажмите кнопку **ОК**.
    
## <a name="create-a-policy-for-a-site-content-type"></a>Создание политики для типа контента сайта
<a name="__create_a_policy"> </a>

Добавление политики управления сведениями к типу контента упрощает связывание компонентов политики с несколько списков или библиотек. Вы можете добавить существующей политики управления сведениями к типу контента или создать политику уникальный, относящиеся к определенным типом содержимого.
  
 Также можно добавить политику управления сведениями к типу контента, относящуюся к спискам. Это приводит к применения политики только для элементов списка, использующих этот тип контента. 
  
1. На домашней странице семейства сайтов \> **Параметры**![кнопка параметров 2016 SharePoint в строке заголовка. ](media/1c22d2d8-39e0-4930-82c6-c3eee44211d3.png) \> **Параметры сайта**.
    
    На сайте SharePoint подключенной группы нажмите кнопку **Параметры**, щелкните **Содержимое сайта**и выберите пункт **Параметры сайта**. 
    
2. На странице "Параметры узла" в разделе **Коллекции веб-дизайнера** \> **типы содержимого узла**.
  
![Ссылка "Типы контента сайта" на странице "Параметры сайта"](media/6f6fa51f-15d7-4782-b06f-a7b36e874cd3.png)
  
3. На странице параметров типа контента сайта выберите тип контента, который вы хотите добавить политику.
    
4. На странице "тип содержимого узла" в разделе **Параметры** \> **Параметры политики управления сведениями**.
    
5. На странице "Изменение политики" введите имя и описание для политики и затем записать краткое описание, объясняющее пользователям возможности политики.
    
6. В следующих разделах выберите возможности индивидуальной политики, которые требуется добавить к политике управления сведениями. 
  
![Типы политик содержимого](media/19fcb8a3-974b-40d3-a13f-b76088d122f8.png)
  
7. Чтобы указать период хранения для документов и элементов, относящихся к этой политике, выберите **Включить хранения**и укажите период хранения и действия, которые должны происходить при срок действия элементов.
    
    Чтобы указать период хранения
    
||||||**1.**|** Выберите ** Добавить этап хранения для записей... ***|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> | Выберите параметр периода хранения, чтобы указать, когда документы или элементы срок действия которых истекает. Выполните одно из следующих действий.<br/>  Чтобы установить срок действия на основе свойства даты, в разделе **событие** \> в **основе этой стадии свойству даты для элемента**и выберите действие документа или элемента (например, для создания или изменения) и промежуток времени после этой (действие) Например, число дней, месяцев или лет) при необходимости срока действия элемента.  <br/>  Чтобы использовать специальную формулу хранения для указания прекращения действия, выберите команду **назначить с настраиваемой формулой хранения на этом сервере**.  <br/> > [!NOTE]> Этот параметр доступен только в том случае, если настроить настраиваемой формулой администратором.           |
||||||3.  <br/> |**Запуск рабочего процесса** доступен только в том случае, если вы определяете политики для списка, библиотеки или типа контента, которые уже имеют рабочего процесса, связанного с ним. Появится, нажмите возможность выбора рабочих процессов, из которых можно выбрать.<br/> |
||||||4.  <br/> |В разделе **повторения** выберите **повторите действия этого этапа...** и введите, как часто требуется действие повторяется.  <br/> > [!NOTE]> Этот параметр доступен только в том случае, если можно повторить действие, которое выбрано. Например нельзя задать повторения для действия, **Удалить без возможности восстановления**.           |
||||||5.  <br/> |Затем нажмите **кнопку ОК**.  <br/> |
   
1. Чтобы включить аудит для документов и элементов, которые могут быть эту политику, выберите **Включить аудит**и укажите события, для которых требуется аудит.
    
    Чтобы включить аудит
    
||||||1.* **|На странице "Изменение политики" ** **в разделе** **Аудит** **\>** **Включить аудит** **, а затем установите флажки рядом с событиями, которой следует сохранять аудита аудита for.* **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |**Чтобы предлагать пользователям вставлять такие штрихкоды в документы,** **Выбор** **Предлагать пользователям вставлять штрих-код перед сохранением или печатью** **.** <br/> |
||||||**3.** <br/> |**Выбор** **ОК** ** применение функции аудита политики. ** <br/> |
|||||||Функции аудита политики позволяет организациям создавать и анализировать журналы аудита для документов и элементов списка, такие как списки задач, списки вопросов, групп обсуждения и календарей. Этот компонент политики предоставляет журнал аудита, записи о событиях, например, когда содержимое просматривать, удалены или изменены.  <br/> |
|||||||Если аудит включен в рамках политики управления сведениями, администраторы могут просматривать данные аудита в отчеты об использовании политик, размещенных в Microsoft Excel и, сведение текущего использования. Администраторы могут использовать эти отчеты для определения способов использования сведений в организации. Эти отчеты также могут помочь организациям для проверки и документировать их соблюдение правовых норм или для изучения потенциальных проблем.  <br/> |
|||||||В журнале аудита записывается следующая информация: название события, его дата и время, системное имя пользователя, выполнившего действия.  <br/> |
   
1. Если штрих-коды включены в рамках политики, они добавляются свойства документа и отображается в области заголовка документа, к которому применяется штрих-кода. Как метки штрих-коды можно также вручную удалить из документа. Можно указать ли пользователям следует приглашение включить штрих-кода при печати или сохранения элемента, или если штрих-код должен быть вставлен вручную с помощью вкладку **Вставка** в 2010 Office выпуск программы. 
    
    Чтобы включить штрих-кодов
    
||||||1.* **|**На странице "Изменение политики" в разделе **штрих-коды** \> **Включить штрих-коды**.**|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||**2.** <br/> |Чтобы предлагать пользователям вставлять такие штрихкоды в документы, выберите пункт **предлагать пользователям вставлять штрих-код перед сохранением или печатью**.  <br/> |
||||||**3.** <br/> |Нажмите **кнопку ОК** , чтобы применить компонент штрих-кода в политике.  <br/> |
|||||||
 Политика штрих-кода создает стандартный код 39 штрих-коды. Каждое изображение штрих-кода включает в себя текста под символ штрих-кода, который представляет значение штрих-кода. Это позволяет данные штрих-кода для использования даже в том случае, если сканирование оборудование не поддерживается. Пользователи могут вручную введите номер штрих-кода в поле «Поиск» для выбора элемента на сайте.  <br/> |
   
1. Чтобы потребовать меток документов, которые могут быть эту политику, выберите **Включить метки**и укажите параметры, которые требуются для метки.
    
    Чтобы включить метки
    
||||||**1.**|** Чтобы пользователи добавляли метки в документ, выберите **предлагают пользователям вставку метки перед сохранением или печатью**.  <br/> > [!NOTE]> Если вы хотите меток по желанию, не устанавливайте этот флажок.        **|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
||||||2.  <br/> |Чтобы заблокировать содержимое метки, поэтому его нельзя изменить после его вставки, выберите **Запретить изменение меток после их добавления**.  <br/>  Этот параметр запрещает с надписью обновление после метку был вставлен в элемент в клиентском приложении, таких как Word, Excel и PowerPoint. Если необходимо, чтобы метки обновлялись при обновлении свойств для данного документа или элемента, не устанавливайте этот флажок.<br/> |
||||||3.  <br/> |В поле Формат метки введите текст надписи, которое будет отображаться. Метки могут содержать до 10 ссылок на столбцы, каждый из которых может быть длиной до 255 символов. Для создания формата для вашей метки, выполните следующие действия.  <br/> Введите имена столбцов, которые необходимо включить в метки в том порядке, в которой будут их отображения. Заключите имена столбцов в фигурные скобки ({}), как показано в примере на странице Изменение политики.  <br/> Введите слова для идентификации столбцы за пределами квадратные скобки, как показано в примере на странице Изменение политики.  <br/> |
||||||4.  <br/> |Чтобы добавить разрыв строки, введите **\n** , в котором требуется добавить разрыв строки.  <br/> |
||||||5.  <br/> |Выберите размер шрифта и стиля и укажите, требуется ли метку размещенный слева, по центру или вправо в документе.  <br/>  Выберите шрифт и стиль, доступные на компьютеры пользователей. Размер шрифта, влияет на количество текста может отображаться на метку.  <br/> |
||||||6.  <br/> |Введите высоту и ширину метки. Высоту метки в диапазоне от.25 дюймов до 20 дюймов и ширину метки в диапазоне от.25 дюймов до 20 дюймов. Текст надписи всегда по вертикали по центру в пределах изображения подписи.  <br/> |
||||||7.  <br/> |Нажмите кнопку **Обновить** , чтобы предварительного просмотра содержимого метки.  <br/> |
   
1. Нажмите кнопку **ОК**.
    
## <a name="create-a-policy-for-a-list-library-or-folder-location-based-retention-policy"></a>Создание политики для списка, библиотеки или папки (политика хранения в зависимости от местоположения)
<a name="__create_a_policy"> </a>

Можно определить политику хранения, которое применяется только к определенному списку, библиотеки или папки. Тем не менее при создании политики хранения таким образом, не может использовать эту политику на других списков, библиотек, папок или сайты и невозможно применить политику семейства сайтов для политики на основе местоположения.
  
Если вы хотите применить политику хранения одного ко всем типам контента в одном месте, вероятнее всего необходимо использовать хранения в зависимости от расположения. В большинстве других случаях необходимо убедиться, что указанный политику хранения для всех типов контента.
  
 Каждой вложенной папке наследует политику хранения родительского, пока не будет выбрано прекращение наследования и определить политику хранения на уровне дочерних. 
  
Если вы хотите определить политику управления сведениями, отличный от хранения для списка или библиотеки, необходимо определить политику управления сведениями для каждого отдельного типа контента, связанные с этого списка или библиотеки.
  
 Если в любой момент следует переключиться из типа контента на основе расположения политики для списка или библиотеки, только политики хранения будет использоваться как политика на основе местоположения. Все другие политики управления (аудит, штрих-коды и штрих-кодов) будет наследоваться от связанных типов контента. 
  
 Политики на основе расположения можно отключить для семейства веб-сайтов посредством отключения компонента библиотеки и хранения на основе папок. Это позволяет администраторам семейства сайтов убедитесь, что их политики типов контента не переопределено политик расположения на основе администратора списка. 
  
Требуется по крайней мере разрешение на управление списками, чтобы изменить параметры политики управления сведениями для списка или библиотеки.
  
1. Перейдите в список или библиотеку, для которого требуется задать политику управления сведениями. 
    
2. На ленте откройте вкладку **Библиотека** или **список** \> **Параметры библиотеки** или **Списка параметров**.
    
    В SharePoint Online нажмите кнопку **Параметры** и нажмите кнопку **Параметры списка** или **Параметры библиотеки**. 
    
3. В разделе **разрешения и управление** \> **Параметры политики управления сведениями**.
  
![Ссылка "Политика управления сведениями" на странице "Параметры" для библиотеки документов](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. На странице "Параметры политики управления сведениями" Убедитесь в том, что источник хранения для списка или библиотеки задано значение библиотеки и папки. 
  
Если **Тип контента** отображается как источник, нажмите кнопку **Изменить источник**и нажмите кнопку **библиотеки и папки**. Оповещения, что политики хранения типов контента будет игнорироваться. Нажмите **кнопку ОК**. 
    
5. На странице "Изменение политики" в разделе **Расписание хранения на основе библиотеки**введите краткое описание для политики, которую вы создаете. 
    
6. Последовательно выберите пункты **Добавить этап хранения...**
    
     Обратите внимание, что в разделе записей, вы можете определить политики различных хранения для записей, выбрав определить разные этапы хранения для записей варианта. 
    
7. В диалоговом окне Свойства рабочей области выберите параметр периода хранения, чтобы указать, если параметр документы или элементы срок действия которых истекает. Выполните одно из следующих действий.
    
  - Чтобы установить срок действия на основе свойства даты, в разделе **событие** \> в **основе этой стадии свойству даты для элемента**и выберите действие документа или элемента (например, для создания или изменения) и промежуток времени после этой (действие) Например, число дней, месяцев или лет) при необходимости срока действия элемента. 
    
  - Чтобы использовать специальную формулу хранения для указания прекращения действия, выберите команду **назначить с настраиваемой формулой хранения на этом сервере**. 
    
    > [!NOTE]
    >  Этот параметр доступен только в том случае, если настроить настраиваемой формулой администратором. 
  
  - В разделе **Действие**укажите, что должно происходить при документа или элемента истекает. Чтобы включить определенное действие происходить для документа или элемента (например, удаление), выберите нужное действие из списка. 
    
8. **Запуск рабочего процесса** доступен только в том случае, если вы определяете политики для списка, библиотеки или типа контента, которые уже имеют рабочего процесса, связанного с ним. Появится, нажмите возможность выбора рабочих процессов, из которых можно выбрать. 
    
9. В разделе **повторения**выберите параметр **повторите действия этого этапа...** и введите, как часто требуется действие повторяется. 
    
    > [!NOTE]
    >  Этот параметр доступен только в том случае, если можно повторить действие, которое выбрано. Например нельзя задать повторения для действия, **Удалить без возможности восстановления**. 
  
10. Нажмите кнопку **ОК**.
    
## <a name="apply-a-site-collection-policy-to-a-content-type"></a>Применить политику семейства сайтов в тип контента
<a name="__apply_a_site"> </a>

Если уже были созданы политик управления сведениями для вашего сайта как политики семейства сайтов, можно применить одну из политик в тип контента. В этом случае можно применить та же политика для нескольких типов контента в семействе сайтов, которые не имеют общий того же родительского типа контента.
  
 Если требуется применить политики для нескольких типов контента в семейства веб-сайтов и у вас есть службы управляемых метаданных настроен, можно использовать публикации типа контента для публикации в работе Управление политиками для нескольких семейств веб-сайтов. В разделе [Применение политики к типам контента в семействах сайтов](create-info-mgmt-policies.md#__apply_a_policy) для получения дополнительных сведений. 
  
1. Перейдите к списку или библиотеке, которая содержит тип контента, к которому следует применить политику.
    
2. На ленте откройте вкладку **Библиотека** или **список** \> **Параметры библиотеки** или **Списка параметров**.
    
    В SharePoint Online нажмите кнопку **Параметры** и нажмите кнопку **Параметры списка** или **Параметры библиотеки**. 
    
3. В разделе **разрешения и управление** \> **Параметры политики управления сведениями**.
  
![Ссылка "Политика управления сведениями" на странице "Параметры" для библиотеки документов](media/9fa6d366-6aab-49e1-a05c-898ac6f536e6.png)
  
4. Убедитесь, что источник политики к **Типам контента**, а также в области **Политики типов контента** выберите тип контента, который вы хотите применить политику к. 
    
5. В поле **Укажите политику** \> **использовать политику семейства сайтов**, а затем выберите политику, которую нужно применить из списка. 
    
    > [!NOTE]
    >  Если параметр **использовать политику семейства сайтов** недоступна, не политики семейства сайтов не определено для семейства веб-сайтов. 
  
6. Нажмите кнопку **ОК**.
    
     Если список или библиотеку, в которой вы работаете, поддерживает управление несколькими типами контента, в разделе **Типы контента** можно выбрать тип контента, для которого требуется задать политику управления сведениями. Это требуется непосредственно на шаге 5. 
    
## <a name="apply-a-policy-across-site-collections"></a>Применение политики в семействах сайтов
<a name="__toc260646789"> </a>

Совместное использование типов контента в семействах сайтов с помощью приложения-службы управляемых метаданных для настройки публикации типа контента. Публикация типов контента помогает управлять контента и метаданных постоянно через веб-узлы, так как типы контента можно создавать и обновлены централизованно и обновления могут быть опубликованы в работе с несколькими подписки семейств веб-сайтов или веб-приложений.
  
## <a name="create-a-template-from-an-existing-policy-to-use-across-site-collections"></a>Создание шаблона из существующей политики для использования в семействах сайтов
<a name="__toc262125409"> </a>

Можно определить политику управления сведениями и затем создать шаблон на основе его для использования при необходимости в нескольких семействах сайтов. Этот метод можно использовать, если необходимо иметь резервную копию политик информации или его можно использовать также в качестве альтернативного метода публикации типа контента, используя одну политику применения в семействах сайтов. Создание резервной копии политики или шаблон с экспорт политики из одного семейства сайтов, а затем импортировать его в сохраненный папку или другом семействе веб-сайтов.
  
> [!IMPORTANT]
>  Если вы с помощью экспорта и импорта в функциях, чтобы сделать набор шаблонов политики, имейте в виду, существует ли уникальный идентификатор в XML-файл политики. В связи с этим нельзя импортировать политики в сайт более одного раза без изменения этот уникальный идентификатор. 
  
### <a name="export-a-policy"></a>Экспорт политики
<a name="__toc260646790"> </a>

1. На домашней странице семейства сайтов выберите **Параметры**![шестеренки небольшой параметры, когда был выполнен параметры сайта. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **Параметры сайта**.
    
    На сайте SharePoint подключенной группы нажмите кнопку **Параметры**, щелкните **Содержимое сайта**и выберите пункт **Параметры сайта**. 
    
2. На странице "Параметры узла" в разделе **Администрирование семейства веб-сайтов** \> **Содержимого шаблоны политики типов**. 
  
![Ссылка на шаблон политики типа содержимого на странице "Параметры сайта"](media/26d3466a-23ec-443f-88f0-2aaff38e992b.png)
  
3. Выберите политику, который необходимо экспортировать \> в нижней \> **Экспорт**.
    
4. В командной строке сохранить или открыть файл выберите команду **Сохранить**и выберите местоположение для сохранения файла. Обязательно выберите расположение, доступные для семейств веб-сайтов, которые импорта политики.
    
5. Когда загрузка завершена диалоговое окно отображается, нажмите кнопку **Закрыть**.
    
### <a name="import-a-policy-to-a-different-site-collection"></a>Импортировать политику в другом семействе сайтов
<a name="__toc260646791"> </a>

Импорт политики управления сведениями позволяет применять для нескольких типов контента на уровне сайта или списка в рамках любого указанного семейства сайтов. Преимущества для этого есть две причины: не нужно повторно определение и применение политики для каждого типа контента, и позволяет управлять изменения политики при внесении изменений в политике в одном месте.
  
1. На домашней странице семейства сайтов, к которому требуется применить политику, выберите **Параметры**![шестеренки небольшой параметры, когда был выполнен параметры сайта. ](media/a47a06c3-83fb-46b2-9c52-d1bad63e3e60.png) \> **Параметры сайта**.
    
    На сайте SharePoint подключенной группы нажмите кнопку **Параметры**, щелкните **Содержимое сайта**и выберите пункт **Параметры сайта**. 
    
2. На странице "Параметры узла" в разделе **Администрирование семейства веб-сайтов** \> **Содержимого шаблоны политики типов**.
    
3. На странице политики \> **импорта** \> **Обзор** , чтобы найти XML-файл для политики. 
    
4. Выберите XML-файл, в которой был сохранен политики \> **Open**. 
    
5. При импорте политику семейства сайтов страницы \> **импорта** для добавления политики семейства веб-сайтов. 
    
Импортированные политики теперь могут применяться к одной или нескольких типов контента на уровне сайта или списка. 
  
[Политики управления сведениями включите вашей организации для элемента управления, сколько времени требуется сохранение контента, для аудита, что делать с контентом, а также добавлять штрих-коды или метки в документ. Политику можно помощь при внедрении соблюдения юридических и правительственными нормативами или внутренних бизнес-процессов. С правами администратора, можно настроить политику для управления как для отслеживания документов и сколько времени требуется сохранять документы. Можно создать могут получать политики управления сведения в трех различных местах в иерархии сайтов из широкой для узкой: создать политику для использования на нескольких типов контента в пределах семейства веб-сайтов. Создание политики для типа контента сайта. Создание политики для списка или библиотеки. Для получения дополнительных сведений см политик управления сведениями.](create-info-mgmt-policies.md#__top)
  
