---
title: Overview of importing your organization PST files to Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.IngestionHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MET150
ms.assetid: ba688e0a-0fcb-4bd7-8e57-2b669564ea84
description: 'Для администраторов: сведения об использовании службы импорта в центре безопасности _Амп_ соответствие требованиям для массового импорта данных электронной почты (PST-файлов) в почтовые ящики пользователей в Exchange Online. В этом разделе приведены часто заДаваемые вопросы и сведения о том, как работает процесс импорта PST-файлов.'
ms.openlocfilehash: 3a7dba3db608eb45347609acef396faf73da483f
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000242"
---
# <a name="overview-of-importing-your-organization-pst-files-to-office-365"></a>Overview of importing your organization PST files to Office 365

> [!NOTE]
> Эта статья предназначена для администраторов. Вы пытаетесь импортировать PST-файлы в свой почтовый ящик? [В разделе Импорт электронной почты, контактов и календаря из PST-файла Outlook](https://go.microsoft.com/fwlink/p/?LinkID=785075)

С помощью службы импорта в центре безопасности _Амп_ соответствие требованиям можно быстро массово импортировать PST-файлы в почтовые ящики Exchange Online в организации Office 365. Импортировать PST-файлы в Office 365 можно двумя способами:
   
- **Отправка по сети** ![Отправка](media/54ab16ee-3822-4551-abef-3d926f4e1c01.png) в облако — отправка PST-файлов по сети во временное хранилище Azure в облаке Майкрософт. Затем вы можете импортировать данные PST в почтовые ящики в организации Office 365 с помощью службы импорта Office 365. 

- **Доставка дисков** ![Жесткий диск](media/e72b76f3-1f73-4296-b749-c325d95d9ef6.png) — копирование PST-файлов на жесткий диск с шифрованием BitLocker и физическая доставка диска в корпорацию Майкрософт. Когда корпорация Майкрософт получает жесткий диск, сотрудники центра обработки данных отправляют данные в временное место хранения Azure в облаке Майкрософт. Затем вы можете импортировать данные в почтовые ящики в организации Office 365 с помощью службы импорта Office 365.

## <a name="step-by-step-instructions"></a>Пошаговые инструкции
  
В следующих разделах представлены подробные и пошаговые инструкции по массовому импорту PST-файлов Организации в Office 365. 
   
- [Импорт PST-файлов в Office 365 с помощью отправки по сети](use-network-upload-to-import-pst-files.md)
- [Импорт PST-файлов в Office 365 с помощью отправки дисков](use-drive-shipping-to-import-pst-files-to-office-365.md)

## <a name="how-importing-pst-files-works"></a>Принципы работы импорта PST-файлов

Ниже приведена иллюстрация и описание полного процесса импорта PST-файлов. На рисунке показан основной рабочий процесс и выделяются различия между методами доставки и отправки в сеть.
  
![Рабочий процесс импорта PST-файлов](media/76997b69-67d7-433a-a0ca-9389f85a36a1.png)
  
1. **Скачайте средства импорта PST-файлов и ключ к частному хранилищу Azure** — первым этапом является загрузка средства и ключа доступа, используемого для отправки PST-файлов, или их копирования на жесткий диск. Их можно получить на странице **Импорт** в центре безопасности _Амп_ соответствия требованиям. Ключ предоставляет вам (или персоналу центра обработки данных Майкрософт в случае доставки дисков) с необходимыми разрешениями для отправки PST-файлов в частное и безопасное место хранения Azure. Этот ключ доступа уникален для Организации и помогает предотвратить несанкционированный доступ к PST-файлам после их отправки в Microsoft Cloud. Обратите внимание, что при импорте PST-файлов в Office 365 не требуется, чтобы в Организации была отдельная подписка на Azure. 
    
2. **Отправка или копирование PST-файлов** : следующий шаг зависит от того, используется ли отправка по сети или доставка дисков для импорта PST-файлов. В обоих случаях вы будете использовать средство и ключ защищенного хранилища, полученный на предыдущем шаге.
    
    - **Отправка по сети** Средство AzCopy. exe (загруженное на этапе 1) используется для отправки и хранения PST-файлов в хранилище Azure в облаке Майкрософт. Обратите внимание на то, что расположение хранилища Azure, в которое вы отправляете PST-файлы, находится в том же региональном центре обработки данных Майкрософт, в котором расположена организация Office 365. 
    
      Для их отправки необходимо, чтобы PST-файлы, которые вы хотите импортировать в Office 365, были размещены в общей папке или на файловом сервере в Организации.
    
    - **Доставка дисков** Средство WAImportExport. exe (загруженное на этапе 1) используется для копирования PST-файлов на жесткий диск. Это средство шифрует жесткий диск с помощью BitLocker и копирует PST на жесткий диск. Как и при отправке по сети, PST-файлы, которые необходимо скопировать на жесткий диск, должны находиться в общей папке или на файловом сервере в Организации.
    
3. **Создание файла сопоставления для импорта PST** -файлов: после отправки PST-файлов в хранилище Azure или их копирования на жесткий диск необходимо создать файл с разделителями-запятыми (CSV), указывающий, в какие почтовые ящики пользователей будут импортированы PST-файлы (a файл PST можно импортировать в основной или архивный почтовый ящик пользователя. Служба импорта Office 365 будет использовать эти сведения для импорта PST-файлов. 
    
4. **Создание задания импорта PST** -файла. следующий шаг — создание задания импорта PST-файла на странице **Импорт** в центре безопасности _амп_ соответствие требованиям и предоставление файла сопоставления для импорта PST, созданного на предыдущем шаге. Для отправки по сети (так как PST-файлы были отправлены в Azure) Office 365 анализирует данные в PST-файлах, а затем предоставляет возможность настраивать фильтры, которые контролируют, какие данные фактически импортируются в почтовые ящики, указанные в файле сопоставления для импорта PST-файлов. 
    
    Для доставки дисков в данный момент происходит несколько дополнительных моментов.
    
    - Физически отгрузка жесткого диска в центр обработки данных Майкрософт (при создании задания импорта отображается адрес доставки для центра обработки данных Майкрософт).
    
    - Когда корпорация Майкрософт получает жесткий диск, персонал центра обработки данных отправляет файлы PST на жесткий диск в место хранения Azure для вашей организации. Как описывалось ранее, ваши PST-файлы отправляются в расположение хранилища Azure, которое находится в том же региональном центре обработки данных Майкрософт, где расположена организация Office 365.
    
      > [!NOTE]
      > PST-файлы на жестком диске передаются в Azure в течение 7 – 10 рабочих дней после получения жесткого диска корпорацией Майкрософт. 
  
      Как и в случае с процессом сетевой загрузки, Office 365 анализирует данные в PST-файлах и предоставляет возможность настраивать фильтры, которые контролируют, какие данные фактически импортируются в почтовые ящики, указанные в файле сопоставления PST-импорта.
    
    - Корпорация Майкрософт отгружается к вам жесткого диска. 
    
5. **Фильтрация данных PST, которые будут импортированы в почтовые ящики,** после создания задания импорта (и после загрузки PST-файлов из задания по доставке диска в расположение хранилища Azure) Office 365 анализирует данные в PST-файлах (безопасно и безопасно), выполняя Определение возраста элементов и различных типов сообщений, включенных в PST-файлы. После завершения анализа и готовности к импорту данных можно импортировать все данные, содержащиеся в PST-файлах, или можно обрезать импортируемые данные, задав фильтры, которые контролируют, какие данные следует импортировать. 
    
6. **Запустите задание импорта PST** -файла после запуска задания импорта, Office 365 использует сведения из файла сопоставления PST-файла для импорта PST-файлов из расположения хранилища Azure в почтовые ящики пользователей. Сведения о состоянии задания импорта (в том числе сведения о каждом импортируемом PST-файле) отображаются на странице " **Импорт** " в центре безопасности _Амп_ соответствия требованиям. После завершения задания импорта в качестве состояния задания устанавливается значение **завершено**.
  
## <a name="why-import-email-data-to-office-365"></a>Зачем импортировать данные электронной почты в Office 365?

- Импорт PST-файлов в почтовые ящики пользователей — это один из способов переноса электронной почты организации в Office 365.
    
- С помощью функции [интеллектуальнОго импорта](filter-data-when-importing-pst-files.md) можно отфильтровать элементы в PST-файлах, которые фактически импортируются в целевые почтовые ящики. Это позволяет обрезать импортируемые данные, устанавливая фильтры, которые контролируют, какие данные следует импортировать. 
    
- Импорт данных электронной почты в Office 365 помогает устранить требования вашей организации, предоставляя следующие возможности:
    
  - Включите [Архивные](enable-archive-mailboxes.md) почтовые ящики и [неограниченное архивирование](unlimited-archiving.md) , чтобы предоставить пользователям дополнительное место для хранения почтовы 
    
  - Помещение почтовых ящиков на [Хранение](https://go.microsoft.com/fwlink/?linkid=841243) для судебного разбирательства для хранения контента. 
    
  - Используйте [средство "поиск контента](content-search.md) " для поиска содержимого почтового ящика. 
    
  - Использование [обращенИй eDiscovery](ediscovery-cases.md) для работы с юридическими исследованиями Организации 
    
  - Используйте [политики хранения](retention-policies.md) в центре безопасности _Амп_ соответствие требованиям для управления продолжительностью хранения содержимого почтового ящика и удаления контента по истечении срока хранения. 
    
- Импорт данных в Office 365 помогает защититься от потери данных. Данные электронной почты, импортированные в Office 365, наследуют функции высокой доступности в Exchange Online.
    
- Данные электронной почты в Office 365 доступны пользователям на всех устройствах, так как они хранятся в облаке.
    
## <a name="importing-sharepoint-data-to-office-365"></a>Импорт данных SharePoint в Office 365

Вы также можете импортировать файлы и документы на сайты SharePoint и учетные записи OneDrive в организации Office 365. Дополнительные сведения см. в следующих статьях:

- [Миграция в SharePoint Online](https://docs.microsoft.com/sharepointmigration/migrate-to-sharepoint-online)

- [Знакомство со средством миграции SharePoint](https://docs.microsoft.com/sharepointmigration/introducing-the-sharepoint-migration-tool)

- [Миграция на SharePoint Online с помощью PowerShell](https://docs.microsoft.com/sharepointmigration/overview-spmt-ps-cmdlets)

- [Перенос содержимого общего файлового ресурса в SharePoint Online с помощью поля данных Azure](https://docs.microsoft.com/sharepointmigration/how-to-migrate-file-share-content-to-spo-using-azuredatabox)


## <a name="frequently-asked-questions-about-importing-pst-files-to-office-365"></a>Часто задаваемые вопросы об импорте PST-файлов в Office 365
  
Ниже приведены часто задаваемые вопросы об использовании службы импорта Office 365 для массового импорта PST-файлов в почтовые ящики Office 365. 
  
- [Использование отправки по сети для импорта PST-файлов](#using-network-upload-to-import-pst-files)
  
- [Использование доставки дисков для импорта PST-файлов](#using-drive-shipping-to-import-pst-files)
  
### <a name="using-network-upload-to-import-pst-files"></a>Использование отправки по сети для импорта PST-файлов

 **Какие разрешения необходимы для создания заданий импорта в службе импорта Office 365?**
  
Необходимо назначить роль экспорта для импорта поЧтовых ящиков в Exchange Online, чтобы импортировать PST-файлы в почтовые ящики Office 365. По умолчанию эта роль не назначается ни одной группе ролей в Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. Дополнительные сведения можно найти в разделах "Добавление роли в группу ролей" или "Создание группы ролей" в разделе [Управление группами ролей в Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Кроме того, для создания заданий импорта в центре безопасности _Амп_ соответствия требованиям необходимо выполнить одно из следующих условий:
  
- Вы должны быть назначены роли получателей почты в Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Или
    
- Вам необходимо быть глобальным администратором в организации Office 365.
    
> [!TIP]
> РасСмотрите возможность создания новой группы ролей в Exchange Online, специально предназначенной для импорта PST-файлов в Office 365. Для доступа к минимальному уровню привилегий, необходимых для импорта PST-файлов, назначьте роли "Импорт импорта почтового ящика" и "Получатели почты" новой группе ролей, а затем добавьте участников. 
  
 **Где доступна отправка по сети?**
  
Network upload is currently available in the United States, Canada, Brazil, the United Kingdom, Europe, India, East Asia, Southeast Asia, Japan, Republic of Korea, and Australia. Network upload will be available in more regions soon.
  
 **What is the pricing for importing PST files by using network upload?**
  
Using network upload to import PST files is free.
  
Это также означает, что после удаления PST-файлов из области хранилища Azure они больше не отображаются в списке файлов для завершенного задания импорта в центре администрирования Microsoft 365. Несмотря на то, что задание импорта по-прежнему может отображаться на странице **Импорт данных в Office 365** , список PST-файлов может быть пустым при просмотре сведений о старых заданиях импорта. 
  
 **What version of the PST file format is supported for importing to Office 365?**
  
There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. Тем не менее файлы, в которых используется формат PST-файлов в формате ANSI (например, для языков, использующих ДВУХБАЙТОВУЮ кодировку (DBCS)), также можно импортировать в Office 365. Дополнительные сведения об импорте PST-файлов в формате ANSI приведены в разделе Шаг 4 раздела [Использование отправки по сети для импорта PST-файлов в Office 365](https://go.microsoft.com/fwlink/p/?LinkId=823074).
  
Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.
  
 **Когда я отправил PST-файлы в область хранилища Azure, как долго они хранятся в Azure, прежде чем они будут удалены?**
  
При импорте PST-файлов с помощью метода отправки в сети вы отправляете их в контейнер BLOB-объектов Azure с именем **ingestiondata**. Если на странице **импорта** в центре безопасности _амп_ соответствие нет заданий импорта, все PST-файлы в контейнере **ingestiondata** в Azure удаляются через 30 дней после создания последнего задания импорта в _амп_ безопасности Центр соответствия требованиям. Это также означает, что необходимо создать новое задание импорта в центре безопасности _Амп_ соответствие требованиям (описанном в шаге 5 в инструкциях по отправке в сети) в течение 30 дней с момента отправки PST-файлов в Azure. 
  
Это также означает, что после удаления PST-файлов из области хранилища Azure они больше не отображаются в списке файлов для завершенного задания импорта в центре безопасности _Амп_ соответствие требованиям. Несмотря на то, что задание импорта по-прежнему может отображаться на странице **Импорт** центра соответствия требованиям безопасности _амп_, список PST-файлов может быть пустым при просмотре сведений о старых заданиях импорта. 
  
 **Сколько времени требуется для импорта PST-файла в почтовый ящик?**
  
It depends on the capacity of your network, but it typically takes several hours for each terabyte (TB) of data to be uploaded to the Azure storage area for your organization. После того как PST-файлы будут скопированы в область хранилища Azure, PST-файл будет импортирован в почтовый ящик Office 365 по крайней мере 24 ГБ в день. Если это значение не соответствует вашим потребностям, вы можете рассмотреть другие способы переноса данных электронной почты в Office 365. Дополнительные сведения см. [в статье способы переноса нескольких учетных записей электронной почты в Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Аналогично, если несколько PST-файлов импортируются в один почтовый ящик, они будут импортированы одновременно.
  
 **Is there a message size limit when importing PST files?**
  
Да. Если PST-файл содержит элемент почтового ящика размером более 150 МБ, он будет пропущен во время процесса импорта.
  
 **— Это свойства сообщений, например, когда сообщение было отправлено или получено, список получателей и другие свойства сохраняются при импорте PST-файлов в почтовый ящик Office 365.**
  
Да. Исходные метаданные сообщения не изменяются во время процесса импорта.
  
 **Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**
  
Yes. You can't import a PST file that has 300 or more levels of nested folders.
  
 **Can I use network upload to import PST files to an inactive mailbox in Office 365?**
  
Yes, this capability is now available. 
  
 **Can I use network upload to import PST files to an online archive mailbox in an Exchange hybrid deployment?**
  
Yes, this capability is now available. 
  
 **Можно ли использовать отправку по сети для импорта PST-файлов в общедоступные папки в Exchange Online?**
  
Нет, вы не можете импортировать PST-файлы в общедоступные папки.
  
### <a name="using-drive-shipping-to-import-pst-files"></a>Использование доставки дисков для импорта PST-файлов

 **Какие разрешения необходимы для создания заданий импорта в службе импорта Office 365?**
  
Необходимо назначить роль экспорта для импорта почтового ящика для импорта PST-файлов в почтовые ящики Office 365. По умолчанию эта роль не назначается ни одной группе ролей в Exchange Online. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself or other users as a member. Дополнительные сведения можно найти в разделах "Добавление роли в группу ролей" или "Создание группы ролей" в разделе [Управление группами ролей в Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=730688).
  
Кроме того, для создания заданий импорта в центре безопасности _Амп_ соответствия требованиям необходимо выполнить одно из следующих условий:
  
- Вы должны быть назначены роли получателей почты в Exchange Online. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Или
    
- Вам необходимо быть глобальным администратором в организации Office 365.
    
> [!TIP]
> РасСмотрите возможность создания новой группы ролей в Exchange Online, специально предназначенной для импорта PST-файлов в Office 365. Для доступа к минимальному уровню привилегий, необходимых для импорта PST-файлов, назначьте роли "Импорт импорта почтового ящика" и "Получатели почты" новой группе ролей, а затем добавьте участников. 
  
 **Где доступна доставка накопителей?**
  
В настоящее время доставка дисков доступна в США, Канаде, Бразилии, Великобритании, Европе, Индии, Восточной Азии, Юго-Восточной Азии, Японии, Республика Корея и Австралии. Drive shipping will be available in more regions soon.
  
 **What commercial licensing agreements support drive shipping?**
  
Доставка дисков для импорта PST-файлов в Office 365 доступна через соглашение Майкрософт Enterprise Agreement (EA). Доставка дисков недоступна через соглашение о продуктах и службах Майкрософт (МПСА).
  
 **Каковы цены на использование доставки дисков для импорта PST-файлов в Office 365?**
  
The cost to use drive shipping to import PST files to Office 365 mailboxes is $2 USD per GB of data. For example, if you ship a hard drive that contains 1,000 GB (1 TB) of PST files, the cost is $2,000 USD. You can work with a partner to pay the import fee. Сведения о том, как найти партнера, можно [найти в статье Find Your партнер или торговый посредник Office 365](https://go.microsoft.com/fwlink/p/?LinkId=785197).
  
 **What kind of hard drives are supported for drive shipping?**
  
Для службы импорта Office 365 поддерживаются только диски с твердотельными накопителями 2,5 дюймов (SSDs) или 2,5 или 3,5 дюймов для жестких дисков SATA II/III. You can use hard drives up to 10 TB. Для заданий импорта будет обработано только первый том данных на жестком диске. The data volume must be formatted with NTFS. При копировании данных на жесткий диск вы можете присоединить его непосредственно с помощью соединителя SATA II или 2,5 или 3,5 дюйма или с помощью разъема SATA II/III или с внешним подключением с помощью USB-адаптера SATA II/III или 2,5 с SATA II/III.
  
> [!IMPORTANT]
> Внешние жесткие диски, которые поставляются со встроенным USB-адаптером, не поддерживаются службой импорта Office 365. Additionally, the disk inside the casing of an external hard drive can't be used. Please don't ship external hard drives. 
  
 **How many hard drives can I ship for a single import job?**
  
You can ship a maximum of 10 hard drives for a single import job.
  
 **After I ship my hard drive, how long does it take to get to the Microsoft data center?**
  
That depends on a few things, such as your proximity to the Microsoft data center and what kind of shipping option you used to ship your hard drive (such as, next-day delivery, two-day delivery, or ground-delivery). With most shippers, you can use the tracking number to track the status of your delivery.
  
 **Когда мой жесткий диск поступает в центр обработки данных Майкрософт, сколько времени займет отправка личных PST-файлов в Azure?**
  
После получения жесткого диска в центре обработки данных Майкрософт для отправки PST-файлов в область хранилища Microsoft Azure для Организации потребуется от 7 до 10 рабочих дней. PST-файлы будут отправлены в контейнер BLOB-объектов Azure `ingestiondata`с именем. 
  
 **Сколько времени требуется для импорта PST-файла в почтовый ящик?**
  
После того как PST-файлы будут отправлены в область хранилища Azure, Office 365 анализирует данные в PST-файлах (безопасным и безопасным способом), чтобы определить возраст элементов и типы сообщений, включенные в PST-файлы. После завершения анализа можно будет импортировать все данные в PST-файлы или установить фильтры для этого элемента управления, какие данные будут импортированы. После запуска задания импорта PST-файл импортируется в почтовый ящик Office 365 с частотой не менее 24 ГБ в день. Если это значение не соответствует вашим потребностям, вы можете рассмотреть другие методы импорта данных электронной почты в Office 365. Дополнительные сведения см. [в статье способы переноса нескольких учетных записей электронной почты в Office 365](https://support.office.com/article/ways-to-migrate-multiple-email-accounts-to-office-365-0a4913fe-60fb-498f-9155-a86516418842).
  
If different PST files are imported to different target mailboxes, the import process occurs in parallel; in other words, each PST/mailbox pair is imported simultaneously. Аналогично, если несколько PST-файлов импортируются в один почтовый ящик, они будут импортированы одновременно.
  
 **Когда корпорация Майкрософт отправляет PST-файлы в Azure, как долго они хранятся в Azure, прежде чем они будут удалены?**
  
Все PST-файлы в расположении хранилища Azure для организации (в контейнере BLOB `ingestiondata`-объектов с именем) удаляются через 30 дней после создания последнего задания импорта на странице " **Импорт** " центра соответствия требованиям безопасности _амп_. 
  
Это также означает, что после удаления PST-файлов из области хранилища Azure они больше не отображаются в списке файлов для завершенного задания импорта в центре безопасности _Амп_ соответствие требованиям. Несмотря на то, что задание импорта по-прежнему может отображаться на странице **Импорт** центра соответствия требованиям безопасности _амп_, список PST-файлов может быть пустым при просмотре сведений о старых заданиях импорта. 
  
 **What version of the PST file format is supported for importing to Office 365?**
  
There are two versions of the PST file format: ANSI and Unicode. We recommend importing files that use the Unicode PST file format. Тем не менее файлы, в которых используется формат PST-файлов в формате ANSI (например, для языков, использующих ДВУХБАЙТОВУЮ кодировку (DBCS)), также можно импортировать в Office 365. Дополнительные сведения об импорте PST-файлов в формате ANSI приведены в разделе Шаг 3 в разделе [Использование доставки дисков для импорта PST-файлов Организации в Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step-3-create-the-pst-import-mapping-file).
  
Additionally, PST files from Outlook 2007 and later versions can be imported to Office 365.
  
 **Is there a message size limit when importing PST files?**
  
Да. Если PST-файл содержит элемент почтового ящика размером более 150 МБ, он будет пропущен во время процесса импорта.
  
 **— Это свойства сообщений, например, когда сообщение было отправлено или получено, список получателей и другие свойства сохраняются при импорте PST-файлов в почтовый ящик Office 365.**
  
Да. Исходные метаданные сообщения не изменяются во время процесса импорта
  
 **Is there a limit to the number of levels in a folder hierarchy for a PST file that I want to import to a mailbox?**
  
Yes. You can't import a PST file that has 300 or more levels of nested folders.
  
 **Can I use drive shipping to import PST files to an inactive mailbox in Office 365?**
  
Yes, this capability is now available.
  
 **Can I use drive shipping to import PST files to an online archive mailbox in an Exchange hybrid deployment?**
  
Yes, this capability is now available. 
  
 **Можно ли использовать доставку дисков для импорта PST-файлов в общедоступные папки в Exchange Online?**
  
Нет, вы не можете импортировать PST-файлы в общедоступные папки.
  
 **Can Microsoft wipe my hard drive before they ship it back to me?**
  
No, Microsoft can't wipe hard drives before shipping them back to customers. Hard drives are returned to you in the same state they were in when they were received by Microsoft.
  
 **Можно ли Майкрософт разложить жесткий диск вместо того, чтобы отгрузить его?**
  
No, Microsoft can't destroy your hard drive. Hard drives are returned to you in the same state they were in when they were received by Microsoft.
  
 **Какие службы курьеров поддерживаются для отгрузки возврата?**
  
If you're a customer in the United States or Europe, Microsoft uses FedEx to return your hard drive. For all other regions, Microsoft uses DHL.
  
 **Каковы затраты на поставку возврата?**
  
Return shipping costs vary, depending on your proximity to the Microsoft data center that you shipped your hard drive to. Microsoft will bill your FedEx or DHL account to return your hard drive. The cost of return shipping is your responsibility.
  
 **Можно ли использовать пользовательскую службу доставки курьеров, например Федекс настраиваемую отГрузку, для доставки жесткого диска в корпорацию Майкрософт?**
  
Да.
  
 **If I have to ship my hard drive to another country, is there anything I need to do?**
  
The hard drive that you ship to Microsoft might have to cross international borders. If this is the case, you're responsible for ensuring that the hard drive and the data it contains are imported and/or exported in accordance with the applicable laws. Before shipping a hard drive, check with your advisors to verify that your drive and data can legally be shipped to the specified Microsoft data center. This will help to ensure that it reaches Microsoft in a timely manner.
