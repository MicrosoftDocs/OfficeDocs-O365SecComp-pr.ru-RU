---
title: Внешние контакты массового импорта в Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: End User
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOP150
ms.assetid: bed936bc-0969-4a6d-a7a5-66305c14e958
description: Узнайте, как администраторы могут использовать Exchange Online PowerShell и CSV-файла для массового импортировать внешние контакты в глобальном списке адресов.
ms.openlocfilehash: 4bde56d49ccf94dc91993df90e1ae693e25c961a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534335"
---
# <a name="bulk-import-external-contacts-to-exchange-online"></a>Внешние контакты массового импорта в Exchange Online

**Эта статья предназначена для администраторов. Вы пытаетесь импортировать контакты в почтовый ящик пользователя? Просмотреть [Импорт контактов в Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**
   
Имеет ли вашей компании большое количество существующих бизнес-контакты, которые необходимо включить в общей адресной книги (также называемая глобального списка адресов) в Exchange Online? Хотите ли вы добавить внешние контакты в качестве членов групп рассылки, так же, как можно с пользователями внутри организации? Если Да, можно использовать Exchange Online PowerShell и файл CSV (разделителями-запятыми) для массового импортируйте внешние контакты в Exchange Online. Это три этапа:
  
[Шаг 1: Создание CSV-файл, который содержит сведения о внешних контактов](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[Шаг 2: Создание внешних контактов с помощью PowerShell](#step-2-create-the-external-contacts-with-powershell) 

[Шаг 3: Добавление сведений на свойства внешние контакты](#step-3-add-information-to-the-properties-of-the-external-contacts)

После выполнения этих действий, чтобы импортировать контакты можно выполнить следующие дополнительные задачи:
  
- [Добавьте дополнительные внешние контакты](bulk-import-external-contacts.md#AddMore)
  
- [Скрыть внешние контакты из общей адресной книги](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a>Шаг 1: Создание CSV-файл, который содержит сведения о внешних контактов

Первым шагом является создание CSV-файл, содержащий сведения о каждом внешний контакт, который требуется импортировать в Exchange Online. 
  
1. Скопируйте следующий текст в текстовый файл в Блокнот и сохраните его на рабочий стол в CSV-файл с помощью суффикса имени файла .csv; Например ExternalContacts.csv.
    
    > [!TIP]
    > Если язык содержит специальные символы (например, **е**, **ä**и **ö** в шведский) сохранить CSV-файл с UTF-8 или другом варианте кодировки Юникод при сохранении файла в "Блокнот". 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    Первую строку или строки заголовка, в CSV-файле список свойств контакты, которые могут быть использованы при импорте в Exchange Online. Имя каждого свойства разделенных запятыми. Каждая строка в строке заголовков представляет значения свойств для импорта один внешний контакт. 
    
    > [!NOTE]
    > Этот текст включает данные, которые можно удалить. Но не удалить или изменить первой строки (заголовок). Он содержит все свойства для внешних контактов. 
  
2. Откройте файл CSV в Microsoft Excel для изменения CSV-файла, так как намного проще использовать Excel для редактирования файла CSV.
    
3. Создайте строку для каждого контакта, который необходимо импортировать в Exchange Online. Заполните столько ячеек, насколько это возможно. Эти сведения будут отображаться в общей адресной книги для каждого контакта. 
    
    > [!IMPORTANT]
    >  Следующие свойства (которые являются четыре первых элементов в строке заголовка) необходимы для создания внешних контактов и должны устанавливаться в CSV-файл: **ExternalEmailAddress**, **имя**, **FirstName**, **LastName**. Команда PowerShell, которые выполняются на шаге 2 будут использоваться значения для этих свойств для создания контактов. 

## <a name="step-2-create-the-external-contacts-with-powershell"></a>Шаг 2: Создание внешних контактов с помощью PowerShell

Следующим шагом является использование CSV-файл, созданный на шаге 1, и PowerShell для массового импорта внешние контакты, перечисленные в CSV-файл в Exchange Online. 
  
1.  Подключения PowerShell к организации Exchange Online. Пошаговые инструкции в разделе [подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Убедитесь, что для использования при подключении к Exchange Online PowerShell имя пользователя и пароль для учетной записи глобального администратора Office 365. 
    
2. После подключения к Exchange Online PowerShell, перейдите к папке рабочего стола, CSV-файла, сохраненного в шаге 1. например `C:\Users\Administrator\desktop`.
    
3. Выполните следующую команду, чтобы создать внешние контакты.

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    Он может занять некоторое время создание новых контактов, в зависимости от того, сколько импорте. После завершения команды PowerShell под управлением, отображается список новых контактов, которые были созданы. 
    
4. Чтобы просмотреть новые внешние контакты, перейдите в центр администрирования Exchange (EAC) и нажмите кнопку **получателей** \> **Контакты**. 
    
    > [!TIP]
    > Инструкции по подключению к центра администрирования Exchange в разделе [Exchange admin center в Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197). 
  
5. При необходимости нажмите кнопку **Обновить** ![значок обновления](media/O365-MDM-Policy-RefreshIcon.gif) обновить список и посмотрите, внешние контакты, которые были импортированы. 
    
    Импортированные контакты будут отображаться в общей адресной книги в Outlook и Outlook в Интернете.
    
    > [!NOTE]
    > Можно также просмотреть контакты в центре администрирования Office 365, перейдя на **пользователей** \> **Контакты**. 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a>Шаг 3: Добавление сведений на свойства внешние контакты

После выполнения команды на шаге 2, создаются внешние контакты, но они не содержат сведения контактного лица или организации, являющийся сведения от наибольшего ячеек в CSV-файл. Это, так как при создании нового внешние контакты заполняются только необходимые свойства. Не обращайте, если у вас нет всей информации, появится в CSV-файл. Если он не существует, он не будет добавлен.
  
1.  Подключения PowerShell к организации Exchange Online. Пошаговые инструкции в разделе [подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Перейдите в папку рабочего стола, CSV-файла, сохраненного в шаге 1. например `C:\Users\Administrator\desktop`.
    
3. Выполните следующие две команды, чтобы добавить другие свойства из CSV-файла для внешних контактов, созданный на шаге 2.
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > Параметр _Manager_ может вызывать трудности. Если ячейки не задан в CSV-файл, появится сообщение об ошибке и ни один из сведения о свойствах будет добавлен для контакта. Если вам не нужно указать руководителя, просто удалите ` -Manager $_.Manager ` из предыдущей команды PowerShell. 
  
    Опять же он может занять некоторое время для обновления «контакты», в зависимости от того, сколько был импортирован на шаге 1. 
    
4. Чтобы убедиться, что свойства были добавлены к контактам: 
    
1. В Центре администрирования Exchange перейдите в раздел **Получатели** \> **Контакты**.
    
2. Щелкните контакт и нажмите кнопку **Изменить** ![значок Правка](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) для отображения свойства контакта. 
    
Ну вот! Пользователи могут видеть контакты и Дополнительные сведения в адресной книге Outlook и Outlook в Интернете.
  
## <a name="add-more-external-contacts"></a>Добавьте дополнительные внешние контакты

Повторите шаги с 1 по шаг 3, чтобы добавить новые внешние контакты в Exchange Online. Вы или пользователей в вашей компании так же можно добавить новую строку в CSV-файл для нового контакта. Затем можно запустить команды PowerShell шаг 2 и шаг 3, чтобы создать и добавление сведений на новые контакты.
  
> [!NOTE]
> При выполнении команды для создания новых контактов, можно получить возникнет ошибка, сообщающая, что контакты, которые были созданы в более ранних версий уже существует. Однако создать любой новый контакт, добавлены в CSV-файл. 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a>Скрыть внешние контакты из общей адресной книги >

Некоторые организации могут использовать внешние контакты, только в том случае, поэтому они могут быть добавлены в качестве членов группы рассылки. В этом случае они может потребоваться скрыть внешние контакты из общей адресной книги. Вот как:
  
1.  Подключения PowerShell к организации Exchange Online. Пошаговые инструкции в разделе [подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).
    
2. Чтобы скрыть один внешний контакт, выполните следующую команду.
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    Например чтобы скрыть Елены Матвеевой из общей адресной книги, запустите следующую команду:

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. Чтобы скрыть все внешние контакты из общей адресной книги, выполните следующую команду.

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

После скрытия их внешние контакты не отображаются в общей адресной книги, но по-прежнему можно добавить их в группу рассылки.
