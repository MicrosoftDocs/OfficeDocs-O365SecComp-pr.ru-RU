---
title: Отправлять уведомления по электронной почте и отображение подсказок политики для политики защиты от потери данных
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleNotifyUser
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 87496bc5-9601-4473-8021-cb05c71369c1
description: 'Совет политики — это уведомление или предупреждение, которое появляется, когда кто-то работы с контентом конфликтует с политики защиты от потери данных. Увеличение поддержка и помощь в информировать пользователей о политиках вашей организации, можно использовать уведомления по электронной почте и советы по политикам. Можно также представлены необходимые пользователи могут переопределить политику, чтобы они не будет блокировано, если у них есть действительный business или если политика является обнаружение Ложное срабатывание. '
ms.openlocfilehash: a24afe6dd1203af4dc1f0f21468e828751bc5f3b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535455"
---
# <a name="send-email-notifications-and-show-policy-tips-for-dlp-policies"></a>Отправлять уведомления по электронной почте и отображение подсказок политики для политики защиты от потери данных

Политики (DLP) защита от потери данных можно использовать для идентификации, контроля и защиты конфиденциальной информации между Office 365. Необходимо предоставить пользователям в вашей организации, пользователей, которые работают с конфиденциальной информации соответствия требованиям, с помощью политик защиты от потери данных, но вы не хотите запретить их без необходимости выполнять свою работу. Здесь указывается, где может помочь уведомлений по электронной почте и советы по политикам.
  
![Панель сообщений отображает подсказку политики в Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Совет политики — это уведомление или предупреждение, которое появляется, когда кто-то работа с контентом, который конфликтует с политикой DLP —, например содержимого как книги Excel на OneDrive для бизнеса сайта, который содержит персональные данные Сотрудников, обработанные и является доступ внешних пользователей.
  
Увеличение поддержка и помощь в информировать пользователей о политиках вашей организации, можно использовать уведомления по электронной почте и советы по политикам. Можно также представлены необходимые пользователи могут переопределить политику, чтобы они не будет блокировано, если у них есть действительный business или если политика является обнаружение Ложное срабатывание.
  
В Office 365 безопасность &amp; центре соответствия требованиям, при создании политики защиты от потери данных, можно настроить уведомления пользователя:
  
- Отправлять уведомление по электронной почте для своих сотрудников выберите, который описывает проблему.
    
- Отобразить подсказку политики для контента, который конфликтует с политикой защиты от потери данных:
    
  - Для электронной почты в Outlook в Outlook 2013 и более поздних версий и веб-подсказку политики отображается в верхней части сообщения над получателей во время состоит сообщения.
    
  - Для документов в OneDrive для бизнеса учетной записи или сайт SharePoint Online подсказку политики указывает значок предупреждения, которое отображается для элемента. Чтобы просмотреть дополнительные сведения, выберите элемент и нажмите кнопку **сведения о**![значок области сведений](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) в правом верхнем углу страницы, чтобы открыть область сведений. 
    
  - Для Excel 2016, PowerPoint 2016 и Word 2016 документы, которые хранятся на OneDrive для бизнеса сайтов или сайт SharePoint Online, который включен в политику защиты от потери данных, подсказку политики отображается на панели сообщений и представление Backstage (меню " **файл** " \> ** Сведения о**).
    
## <a name="add-user-notifications-to-a-dlp-policy"></a>Добавление уведомления пользователей в политику защиты от потери данных

При создании политики защиты от потери данных уведомлений по электронной почте и советы по политикам являются частью в разделе **уведомления пользователя** . 
  
1. Последовательно выберите пункты [https://protection.office.com](https://protection.office.com).
    
2. Войдите в Office 365 с помощью учетной записи рабочего или школы. Теперь вы безопасности Office 365 &amp; центре соответствия требованиям.
    
3. В разделе Безопасность &amp; центре соответствия требованиям \> слева навигации \> **защиту от потери данных** \> **политики** \> **+ Создать политику**.
    
    ![Создание кнопки политики](media/b1e48a08-92e2-47ca-abdc-4341694ddc7c.png)
  
4. Выберите шаблон политики защиты от потери данных, которая обеспечивает защиту типов конфиденциальной информации, которую нужно \> **Далее**.
    
    Чтобы начать с пустого шаблона, выберите **Настраиваемый** \> **политики Custom** \> **Далее**.
    
5. Имя политики \> **Далее**.
    
6. Чтобы указать расположение, которые будут политику защиты от потери данных для защиты, выполните одно из следующих действий:
    
  - Выбор **всех расположений в Office 365** \> **Далее**.
    
  - Нажмите кнопку **выбрать определенные расположения** \> **Далее**.
    
    Для включения или исключения всего размещения, например всех сообщений электронной почты Exchange или все учетные записи OneDrive, переключите **состояние** эту папку включено или отключено. 
    
    Чтобы включить только определенные сайты SharePoint или учетные записи OneDrive, включить **состояние** и нажмите кнопку ссылки в разделе **Включить** для выбора определенных узлов или учетные записи. 
    
7. Выберите **Дополнительные параметры** \> **Далее**.
    
8. Нажмите кнопку **+ новое правило**.
    
9. В редакторе правил в разделе **уведомления пользователя**переключитесь состояние.
    
    ![Раздел уведомления пользователя редактора правила](media/47705927-c60b-4054-a072-ab914f33d15d.png)
  
## <a name="options-for-configuring-email-notifications"></a>Параметры уведомлений по электронной почте

Для каждого правила в политике защиты от потери данных вы можете:
  
- отправлять уведомления выбранным пользователям. В частности, это может быть владелец контента, автор последнего изменения, владелец сайта, где хранится контент, или конкретный пользователь;
    
- Настройте текст, включенный в области уведомлений с помощью HTML или на основе маркеров. Дополнительные сведения см.
    
> [!NOTE]
>  Уведомления электронной почты могут быть отправлены только для отдельных получателей — не группы или списки рассылки. > Только новое содержимое, будет вызвано уведомление по электронной почте. Изменение существующего контента будет вызвано подсказки политики, но не уведомления по электронной почте. 
  
![Параметры уведомлений по электронной почте](media/4e7b9500-2a78-44e6-9067-09f4bfd50301.png)
  
### <a name="default-email-notification"></a>Уведомление электронной почты по умолчанию

Уведомления о иметь строку темы, начинающийся с действия, такие как «Уведомление», «Сообщение заблокировано» для электронной почты или «Доступ запрещен» для документов. Если уведомление о документе, текст сообщения уведомлений ссылка, которая возвращает вас на сайт, где документ хранятся и открывается подсказку политики для документов, где можно разрешение некоторых вопросов, (обратитесь к разделу ниже подсказками политики). Если уведомление о сообщении, уведомление включает в себя как вложение сообщение, которое соответствует политики защиты от потери данных.
  
![Сообщение уведомления](media/35813d40-5fd8-425f-9624-55655e74fa6b.png)
  
По умолчанию уведомления для элемента на сайте содержат примерно следующий текст. Текст уведомления настраивается отдельно для каждого правила, поэтому он отличается в зависимости от того, с каким правилом произошло совпадение.
  
| |
|**Действие, выполняемое правилом**|**Затем уведомлений по умолчанию для SharePoint или OneDrive для бизнеса документов говорит это...**|**Затем уведомлений по умолчанию для сообщений Outlook указано следующее...**|
|:-----|:-----|:-----|
|Отправляет уведомление, но не допускает переопределение  <br/> |Этот элемент нарушает политику вашей организации.  <br/> |Конфликты сообщения электронной почты с политикой в вашей организации.  <br/> |
|Блокирует доступ и отправляет уведомление с возможностью переопределения  <br/> |Этот элемент конфликтует с политикой в вашей организации. Если вы не конфликтующие, доступ к файлу может быть заблокирован.  <br/> |Конфликты сообщения электронной почты с политикой в вашей организации. Сообщение не было доставлено всем получателям.  <br/> |
|Блокирует доступ и отправляет уведомление  <br/> |Этот элемент противоречит политике организации. Доступ к этому элементу заблокирован для всех, кроме владельца, автора последнего изменения и главного администратора семейства веб-сайтов.   <br/> |Конфликты сообщения электронной почты с политикой в вашей организации. Сообщение не было доставлено всем получателям.  <br/> |
   
### <a name="custom-email-notification"></a>Уведомления электронной почты

Можно создавать настраиваемые электронного уведомления вместо отправки уведомлений электронной почты по умолчанию конечных пользователей и администраторов. Уведомления электронной почты поддерживает HTML и имеет 5 000 знаков. HTML-код можно использовать для включения изображения, форматирование и другие фирменной символики в уведомлении.
  
Можно также использовать следующие токены помогут настроить уведомление по электронной почте. Эти маркеры — это переменные, которые заменил особые сведения в уведомление, которое отправляется.
  
| |
|**Маркеров**|**Описание**|
|:-----|:-----|
|%% AppliedActions %%  <br/> |Операции, применяемые к контенту.  <br/> |
|%% ContentURL %%  <br/> |URL-адрес документа на сайт SharePoint Online или OneDrive для бизнеса сайта.  <br/> |
|%% MatchedConditions %%  <br/> |Условия, которые были сопоставлены с содержимым. Используйте этот маркер для оповещения пользователей возможные проблемы с контентом.  <br/> |
   
![Сообщения с уведомлением о котором показано, где отображаются маркеры](media/cd3f36b3-40db-4f30-99e4-190750bd1955.png)
  
## <a name="options-for-configuring-policy-tips"></a>Параметры подсказок политики

Для каждого правила в политике защиты от потери данных вы можете настроить подсказки политики, чтобы:
  
- Просто уведомление, что содержимое конфликтует с политику предотвращения потери данных, чтобы их можно было действие для разрешения конфликта. Можно использовать текст по умолчанию (см. в таблицах ниже) или введите текст о отдельные политики для вашей организации.
    
- разрешить пользователю переопределять политику защиты от потери данных. При желании вы можете:
    
  - Требовать лицо введите деловое обоснование для переопределения политики. Эти сведения — это и его можно просмотреть в отчетах защиты от потери данных в разделе **отчеты** о безопасности &amp; центре соответствия требованиям. 
    
  - Разрешить пользователю сообщить о ложном срабатывании и обойти политику защиты от потери данных. Эти сведения также записываются для отчетов, чтобы вы могли использовать ложные срабатывания для точной настройки правил.
    
![Параметры подсказки политики](media/0d2f2c68-028a-4900-afe6-1d9fce5303ef.png)
  
Например в некоторых случаях применяется к OneDrive для бизнеса сайтов политику защиты от потери данных, обнаруживает персональные данные Сотрудников, обработанные и эта политика имеет трех правил:
  
1. Первое правило. Если в документе найдено менее пяти экземпляров конфиденциальных данных, а документ доступен пользователям в организации, действие **Отправить уведомление** выводит подсказку политики. Для подсказок политики не требуется возможность переопределения политики, поскольку правило просто информирует пользователей, не блокируя доступ. 
    
2. Во-вторых правила: если больше, чем пять экземпляров этой конфиденциальной информации обнаруженных в документе и документ используется совместно с людей в организации, действие **блокировки доступа к контенту** ограничивает разрешения файлов и ** Отправить уведомление** действие пользователи могут переопределить действия в это правило, предоставляя бизнес-требований. Вашей организации в некоторых случаях необходимы для внутренних пользователей для совместного использования данных личных сведений и не должен политики защиты от потери данных для блокировки этой функции. 
    
3. Третье правило. Если в документе найдено более пяти экземпляров конфиденциальных данных, а документ доступен пользователям за пределами организации, то действие **Блокировать доступ к контенту** ограничит разрешения для файла, а действие **Отправить уведомление** не позволяет пользователям переопределять действия в этом правиле, ведь сведения предоставляются внешним пользователям. Сотрудники организации ни при каких обстоятельствах не должны иметь возможности передавать персональные данные за пределы организации. 
    
Следует понимать следующие особенности использования подсказки политики для переопределения правила:
  
- — Это параметр, чтобы переопределить для каждого правила и переопределяет все действия правила (за исключением отправки уведомления, которая не может быть переопределен).
    
- Возможно для содержимого в соответствии с нескольких правил в политике защиты от потери данных, но будут отображаться только подсказки политики с наиболее строгими, наивысший приоритет правила. Например подсказку политики из правила, которое будет отображаться блокирует доступ к содержимому через подсказку политики из правила, которое просто отправляет уведомление. Это не людей отображается в виде каскада советы по политикам.
    
- Если подсказки политики самого строгого правила разрешают пользователям обойти правило, то при этом также будут переопределены все остальные правила, которым соответствует контент.
    
## <a name="policy-tips-on-onedrive-for-business-sites-and-sharepoint-online-sites"></a>Подсказки политики на сайтах OneDrive для бизнеса и SharePoint Online

Когда документ на OneDrive для бизнеса или сайте SharePoint Online соответствует правило в политику защиты от потери данных и правила с помощью подсказки политики, советы по политикам отображение специальных значков в документе:
  
1. Если правило отправляет уведомление о файле, появится значок предупреждения.
    
2. Если правило блокирует доступ к документу, появляется значок блокировки.
    
![Значки подсказки политики на документы в учетной записи OneDrive](media/d3e9f772-03f9-4d28-82f8-3064784332a2.png)
  
Действия в документе, можно выбрать элемент \> выберите **сведения о**![значок области сведений](media/50b6d51b-92b4-4c5f-bb4b-4ca2d4aa3d04.png) в правом верхнем углу страницы, чтобы открыть область сведений \> **подсказку политики представления**.
  
В подсказке политики перечисляются проблемы с контентом, а если настроены соответствующие параметры, то вы можете **Разрешить**, а затем **Обойти** подсказку политики или **Сообщить** о ложном срабатывании. 
  
![Подсказки политики Отображение области сведений](media/0a191e70-80f0-4702-90f4-7a5b7aabcaab.png)
  
![Подсказка политики с кнопкой ее перезаписи](media/e250bff9-41d5-4ce4-82ea-1dc2d043fab1.png)
  
Политики защиты от потери данных синхронизируются с сайтами, а контент сверяется с ними периодически и асинхронно, поэтому между созданием политики защиты от потери данных и появлением подсказок политики может пройти некоторое время. Аналогичная задержка может наблюдаться между разрешении или переопределением подсказки политики и исчезновением значка на документе.
  
### <a name="default-text-for-policy-tips-on-sites"></a>Текст по умолчанию для подсказок политики на сайтах

По умолчанию подсказки политики для элемента на сайте содержат примерно следующий текст. Текст уведомления настраивается отдельно для каждого правила, поэтому он отличается в зависимости от того, с каким правилом произошло совпадение.
  
| |
|**Действие, выполняемое правилом**|**Текст подсказки политики по умолчанию**|
|:-----|:-----|
|Отправляет уведомление, но не допускает переопределение  <br/> |Этот элемент нарушает политику вашей организации.  <br/> |
|Блокирует доступ и отправляет уведомление с возможностью переопределения  <br/> |Этот элемент конфликтует с политикой в вашей организации. Если вы не конфликтующие, доступ к файлу может быть заблокирован.  <br/> |
|Блокирует доступ и отправляет уведомление  <br/> |Этот элемент противоречит политике организации. Доступ к этому элементу заблокирован для всех, кроме владельца, автора последнего изменения и главного администратора семейства веб-сайтов.   <br/> |
   
### <a name="custom-text-for-policy-tips-on-sites"></a>Текст подсказки политики на веб-сайтах

Можно настроить текст для подсказки политики отдельно от уведомлений по электронной почте. В отличие от настраиваемого текста для уведомлений по электронной почте (см. выше раздел) текст для подсказки политики не принимает HTML или на основе маркеров. Вместо этого настраиваемого текста для подсказок политики — обычного текста только с 256 знаков.
  
## <a name="policy-tips-in-outlook-on-the-web-and-outlook-2013-and-later"></a>Советы политики в Outlook в Интернете и Outlook 2013 и более поздних версий

При создания новых сообщений электронной почты в Outlook в Интернете и Outlook 2013 и более поздних версий, вы увидите подсказку политики, если вы добавляете контента, соответствующего правилу в политике защиты от потери данных и это правило использует советы по политикам. Совет политики отображается в верхней части сообщения, над получателей, а состоит сообщения.
  
![Совет политики в верхней части сообщения формируются](media/9b3b6b74-17c5-4562-82d5-d17ecaaa8d95.png)
  
Политика советы рабочих ли конфиденциальной информации отображается в теле сообщения, в строку темы или даже вложения сообщения, как показано ниже.
  
![Подсказку политики, в котором показано, что вложения конфликт политики защиты от потери данных](media/59ae6655-215f-47d9-ad1d-39c0d1e61740.png)
  
Советы по политикам, настроенные на разрешить переопределение, нажмите кнопку **Показать подробности** \> **переопределить** \> введите деловое обоснование или сообщить о ложном срабатывании \> **переопределить**.
  
![Совет политики в сообщении, расширяется для отображения возможность изменения](media/28bfb997-48a6-41f0-8682-d5e62488458a.png)
  
![Диалоговое окно подсказки политики, где можно переопределить подсказки политики](media/f97e836c-04bd-44b4-aec6-ed9526ea31f8.png)
  
Обратите внимание на то, что при добавлении конфиденциальной информации в сообщение электронной почты может быть задержке при добавлении конфиденциальной информации и при появлении подсказки политики.
  
### <a name="policy-tips-in-the-exchange-admin-center-vs-the-office-365-security-amp-compliance-center"></a>Советы политики в центре администрирования Exchange и безопасности Office 365 &amp; центре соответствия требованиям

Советы по политикам можно работать с помощью политик защиты от потери данных и почтовые поток обработки правила, созданные в центре администрирования Exchange или с помощью политик защиты от потери данных, созданные в Office 365 безопасность &amp; центре соответствия требованиям, но не оба. Это, так как эти политики хранятся в различных местах, но советы по политикам можно создать только из одного расположения.
  
Если вы настроили подсказок политики в центре администрирования Exchange, советы политики для настройки безопасности Office 365 &amp; центре соответствия требованиям не будет отображаться для пользователей в Outlook в Интернете и Outlook 2013 и более поздних версий, пока не отключить советы, приведенные в Exchange Центр администрирования. Это гарантирует, что текущие правила транспорта Exchange будет продолжать работать, пока не будет выбрана для переключения на безопасность Office 365 &amp; центре соответствия требованиям.
  
Обратите внимание, что во время советы по политикам можно создать только из одного расположения уведомлений по электронной почте отправляются всегда, даже в том случае, если вы используете политик защиты от потери данных в обоих безопасности Office 365 &amp; центре соответствия требованиям и Центр администрирования Exchange.
  
### <a name="default-text-for-policy-tips-in-email"></a>Текст по умолчанию для подсказок политики по электронной почте

По умолчанию советы по политикам отображаемый текст, подобные приведенным ниже, для электронной почты.
  
| |
|**Действие, выполняемое правилом**|**Текст подсказки политики по умолчанию**|
|:-----|:-----|
|Отправляет уведомление, но не допускает переопределение  <br/> |Конфликты электронной почты с политикой в вашей организации.  <br/> |
|Блокирует доступ и отправляет уведомление с возможностью переопределения  <br/> |Конфликты электронной почты с политикой в вашей организации.  <br/> |
|Блокирует доступ и отправляет уведомление  <br/> |Конфликты электронной почты с политикой в вашей организации.  <br/> |
   
## <a name="policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Подсказки политики в Excel 2016, PowerPoint 2016 и Word 2016

Когда пользователи работают с конфиденциальным контентом в классических версиях Excel 2016, PowerPoint 2016 и Word 2016, подсказки политики могут сообщать им в реальном времени о конфликтах контента с политикой защиты от потери данных. Для этого необходимо следующее:
  
- Документ Office хранится на сайте OneDrive для бизнеса или SharePoint Online.
    
- Сайт включен в политику защиты от потери данных, настроенной на использование советы по политикам.
    
Эти настольных приложений Office 2016 автоматически синхронизировать политик защиты от потери данных непосредственно из Office 365, а затем проверьте документов для убедитесь, что они не конфликтов с политик защиты от потери данных и отображение подсказок политики в режиме реального времени.
  
В зависимости от настроек подсказок политики, пользователи могут просто проигнорировать подсказку, обойти политику с обоснованием или без него либо сообщить о ложном срабатывании.
  
Подсказки политики отображаются в области сообщений.
  
![Панель сообщений отображает подсказку политики в Excel 2016](media/7002ff54-1656-4a6c-993f-37427d6508c8.png)
  
Подсказки политики также отображаются в представлении Backstage (на вкладке **Файл**). 
  
![Backstage отображает подсказку политики в Excel 2016](media/44c561f6-8f3f-4878-b1b0-b7543f8a4120.png)
  
Если для подсказок политики защиты от потери данных настроены эти параметры, вы можете **разрешить** и **обойти** подсказку политики либо **сообщить** о ложном срабатывании. 
  
![Параметры подсказки политики в Backstage для Excel 2016](media/5b3857ba-907e-456e-ae43-888b594c049c.png)
  
В каждом из этих классических приложений Office 2016 пользователи могут отключить подсказки политики. При этом подсказки политики, которые являются простыми уведомлениями, не будут отображаться в области сообщений или представлении Backstage (на вкладке **Файл**). Тем не менее подсказки политики для блокировки и переопределения по-прежнему будут отображаться, а пользователи будут получать уведомления по электронной почте. Кроме того, отключение подсказок политики не исключает документ из каких-либо политик защиты от потери данных, которые были применены к нему. 
  
### <a name="default-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Текст по умолчанию для подсказок политики в Excel 2016, PowerPoint 2016 и Word 2016

По умолчанию подсказки политики содержат примерно следующий текст в панели сообщений и представлении Backstage открытого документа. Текст уведомления настраивается отдельно для каждого правила, поэтому он отличается в зависимости от того, с каким правилом произошло совпадение.
  
| |
|**Действие, выполняемое правилом**|**Текст подсказки политики по умолчанию**|
|:-----|:-----|
|Отправляет уведомление, но не допускает переопределение  <br/> |Этот файл конфликтует с политикой в вашей организации. Перейдите в меню " **файл** " для получения дополнительных сведений.<br/> |
|Блокирует доступ и отправляет уведомление с возможностью переопределения  <br/> |Этот файл конфликтует с политикой в вашей организации. Если вы не конфликтующие, доступ к файлу может быть заблокирован. Перейдите в меню " **файл** " для получения дополнительных сведений.<br/> |
|Блокирует доступ и отправляет уведомление  <br/> |Этот файл конфликтует с политикой в вашей организации. Если вы не конфликтующие, доступ к файлу может быть заблокирован. Перейдите в меню " **файл** " для получения дополнительных сведений.<br/> |
   
### <a name="custom-text-for-policy-tips-in-excel-2016-powerpoint-2016-and-word-2016"></a>Советы по настраиваемого текста для политики в Excel 2016, PowerPoint 2016 и Word 2016

Можно настроить текст для подсказки политики отдельно от уведомлений по электронной почте. В отличие от настраиваемого текста для уведомлений по электронной почте (см. выше раздел) текст для подсказки политики не принимает HTML или на основе маркеров. Вместо этого настраиваемого текста для подсказок политики — обычного текста только с 256 знаков.
  
## <a name="more-information"></a>Дополнительные сведения

- [Обзор политик защиты от потери данных](data-loss-prevention-policies.md)
    
- [Создание политики защиты от потери данных на основе шаблона](create-a-dlp-policy-from-a-template.md)
    
- [Создание политики защиты от потери данных для защиты документов с помощью FCI или других свойств](protect-documents-that-have-fci-or-other-properties.md)
    
- [Что входит в шаблоны политик защиты от потери данных](what-the-dlp-policy-templates-include.md)
    
- [Что позволяют искать типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)
    
