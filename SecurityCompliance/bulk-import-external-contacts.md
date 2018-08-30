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
# <a name="bulk-import-external-contacts-to-exchange-online"></a><span data-ttu-id="b61d7-103">Внешние контакты массового импорта в Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b61d7-103">Bulk import external contacts to Exchange Online</span></span>

<span data-ttu-id="b61d7-104">**Эта статья предназначена для администраторов. Вы пытаетесь импортировать контакты в почтовый ящик пользователя? Просмотреть [Импорт контактов в Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span><span class="sxs-lookup"><span data-stu-id="b61d7-104">**This article is for administrators. Are you trying to import contacts to your own mailbox? See [Import contacts to Outlook](https://support.office.com/article/bb796340-b58a-46c1-90c7-b549b8f3c5f8)**</span></span>
   
<span data-ttu-id="b61d7-p101">Имеет ли вашей компании большое количество существующих бизнес-контакты, которые необходимо включить в общей адресной книги (также называемая глобального списка адресов) в Exchange Online? Хотите ли вы добавить внешние контакты в качестве членов групп рассылки, так же, как можно с пользователями внутри организации? Если Да, можно использовать Exchange Online PowerShell и файл CSV (разделителями-запятыми) для массового импортируйте внешние контакты в Exchange Online. Это три этапа:</span><span class="sxs-lookup"><span data-stu-id="b61d7-p101">Does your company have lots of existing business contacts that you want to include in the shared address book (also called the global address list) in Exchange Online? Do you want to add external contacts as members of distribution groups, just like you can with users inside your company? If so, you can use Exchange Online PowerShell and a CSV (Comma Separated Value) file to bulk import external contacts into Exchange Online. It's a three-step process:</span></span>
  
[<span data-ttu-id="b61d7-109">Шаг 1: Создание CSV-файл, который содержит сведения о внешних контактов</span><span class="sxs-lookup"><span data-stu-id="b61d7-109">Step 1: Create a CSV file that contains information about the external contacts</span></span>](#step-1-create-a-csv-file-that-contains-information-about-the-external-contacts)

[<span data-ttu-id="b61d7-110">Шаг 2: Создание внешних контактов с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="b61d7-110">Step 2: Create the external contacts with PowerShell</span></span>](#step-2-create-the-external-contacts-with-powershell) 

[<span data-ttu-id="b61d7-111">Шаг 3: Добавление сведений на свойства внешние контакты</span><span class="sxs-lookup"><span data-stu-id="b61d7-111">Step 3: Add information to the properties of the external contacts</span></span>](#step-3-add-information-to-the-properties-of-the-external-contacts)

<span data-ttu-id="b61d7-112">После выполнения этих действий, чтобы импортировать контакты можно выполнить следующие дополнительные задачи:</span><span class="sxs-lookup"><span data-stu-id="b61d7-112">After you complete these steps to import contacts, you can perform these additional tasks:</span></span>
  
- [<span data-ttu-id="b61d7-113">Добавьте дополнительные внешние контакты</span><span class="sxs-lookup"><span data-stu-id="b61d7-113">Add more external contacts</span></span>](bulk-import-external-contacts.md#AddMore)
  
- [<span data-ttu-id="b61d7-114">Скрыть внешние контакты из общей адресной книги</span><span class="sxs-lookup"><span data-stu-id="b61d7-114">Hide external contacts from the shared address book</span></span>](bulk-import-external-contacts.md#Hide)
  
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-external-contacts"></a><span data-ttu-id="b61d7-115">Шаг 1: Создание CSV-файл, который содержит сведения о внешних контактов</span><span class="sxs-lookup"><span data-stu-id="b61d7-115">Step 1: Create a CSV file that contains information about the external contacts</span></span>

<span data-ttu-id="b61d7-116">Первым шагом является создание CSV-файл, содержащий сведения о каждом внешний контакт, который требуется импортировать в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b61d7-116">The first step is to create a CSV file that contains information about each external contact that you want to import to Exchange Online.</span></span> 
  
1. <span data-ttu-id="b61d7-117">Скопируйте следующий текст в текстовый файл в Блокнот и сохраните его на рабочий стол в CSV-файл с помощью суффикса имени файла .csv; Например ExternalContacts.csv.</span><span class="sxs-lookup"><span data-stu-id="b61d7-117">Copy the following text to a text file in NotePad, and save it to your desktop as a CSV file by using a filename suffix of .csv; for example, ExternalContacts.csv.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="b61d7-118">Если язык содержит специальные символы (например, **е**, **ä**и **ö** в шведский) сохранить CSV-файл с UTF-8 или другом варианте кодировки Юникод при сохранении файла в "Блокнот".</span><span class="sxs-lookup"><span data-stu-id="b61d7-118">If your language contains special characters (such as **å**, **ä**, and **ö** in Swedish) save the CSV file with UTF-8 or other Unicode encoding when you save the file in NotePad.</span></span> 
  
    ```
    ExternalEmailAddress,Name,FirstName,LastName,StreetAddress,City,StateorProvince,PostalCode,Phone,MobilePhone,Pager,HomePhone,Company,Title,OtherTelephone,Department,CountryOrRegion,Fax,Initials,Notes,Office,Manager
    danp@fabrikam.com,Dan Park,Dan,Park,1234 23rd Ave,Golden,CO,80215,206-111-1234,303-900-1234,555-1212,123-456-7890,Fabrikam,Shipping clerk,555-5555,Shipping,US,123-4567,R.,Good worker,31/1663,Dan Park
    pilar@contoso.com,Pilar Pinilla,Pilar,Pinilla,1234 Main St.,Seattle,WA,98017,206-555-0100,206-555-0101,206-555-0102,206-555-1234,Contoso,HR Manager,206-555-0104,Executive,US,206-555-0105,P.,Technical decision maker,31/1000,Dan Park 
    ```

    <span data-ttu-id="b61d7-p102">Первую строку или строки заголовка, в CSV-файле список свойств контакты, которые могут быть использованы при импорте в Exchange Online. Имя каждого свойства разделенных запятыми. Каждая строка в строке заголовков представляет значения свойств для импорта один внешний контакт.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p102">The first row, or header row, of the CSV file lists the properties of contacts that can be used when you import them to Exchange Online. Each property name is separated by a comma. Each row under the header row represents the property values for importing a single external contact.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b61d7-p103">Этот текст включает данные, которые можно удалить. Но не удалить или изменить первой строки (заголовок). Он содержит все свойства для внешних контактов.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p103">This text includes sample data, which you can delete. But don't delete or change the first (header) row. It contains all of the properties for the external contacts.</span></span> 
  
2. <span data-ttu-id="b61d7-125">Откройте файл CSV в Microsoft Excel для изменения CSV-файла, так как намного проще использовать Excel для редактирования файла CSV.</span><span class="sxs-lookup"><span data-stu-id="b61d7-125">Open the CSV file in Microsoft Excel to edit the CSV file because it's much easier to use Excel to edit the CSV file.</span></span>
    
3. <span data-ttu-id="b61d7-p104">Создайте строку для каждого контакта, который необходимо импортировать в Exchange Online. Заполните столько ячеек, насколько это возможно. Эти сведения будут отображаться в общей адресной книги для каждого контакта.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p104">Create a row for each contact that you want to import to Exchange Online. Populate as many of the cells as possible. This information will be displayed in the shared address book for each contact.</span></span> 
    
    > [!IMPORTANT]
    >  <span data-ttu-id="b61d7-p105">Следующие свойства (которые являются четыре первых элементов в строке заголовка) необходимы для создания внешних контактов и должны устанавливаться в CSV-файл: **ExternalEmailAddress**, **имя**, **FirstName**, **LastName**. Команда PowerShell, которые выполняются на шаге 2 будут использоваться значения для этих свойств для создания контактов.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p105">The following properties (which are the first four items in the header row) are required to create an external contact and must be populated in the CSV file: **ExternalEmailAddress**, **Name**, **FirstName**, **LastName**. The PowerShell command that you run in Step 2 will use the values for these properties to create the contacts.</span></span> 

## <a name="step-2-create-the-external-contacts-with-powershell"></a><span data-ttu-id="b61d7-131">Шаг 2: Создание внешних контактов с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="b61d7-131">Step 2: Create the external contacts with PowerShell</span></span>

<span data-ttu-id="b61d7-132">Следующим шагом является использование CSV-файл, созданный на шаге 1, и PowerShell для массового импорта внешние контакты, перечисленные в CSV-файл в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b61d7-132">The next step is to use the CSV file that you created in Step 1 and PowerShell to bulk import the external contacts listed in the CSV file to Exchange Online.</span></span> 
  
1.  <span data-ttu-id="b61d7-p106">Подключения PowerShell к организации Exchange Online. Пошаговые инструкции в разделе [подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Убедитесь, что для использования при подключении к Exchange Online PowerShell имя пользователя и пароль для учетной записи глобального администратора Office 365.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p106">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554). Be sure to use the user name and password for your Office 365 global administrator account when you connect to Exchange Online PowerShell.</span></span> 
    
2. <span data-ttu-id="b61d7-136">После подключения к Exchange Online PowerShell, перейдите к папке рабочего стола, CSV-файла, сохраненного в шаге 1. например `C:\Users\Administrator\desktop`.</span><span class="sxs-lookup"><span data-stu-id="b61d7-136">After you connect PowerShell to Exchange Online, go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="b61d7-137">Выполните следующую команду, чтобы создать внешние контакты.</span><span class="sxs-lookup"><span data-stu-id="b61d7-137">Run the following command to create the external contacts:</span></span>

    ```
    Import-Csv .\ExternalContacts.csv|%{New-MailContact -Name $_.Name -DisplayName $_.Name -ExternalEmailAddress $_.ExternalEmailAddress -FirstName $_.FirstName -LastName $_.LastName}
    ```

    <span data-ttu-id="b61d7-p107">Он может занять некоторое время создание новых контактов, в зависимости от того, сколько импорте. После завершения команды PowerShell под управлением, отображается список новых контактов, которые были созданы.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p107">It might take a while to create the new contacts, depending on how many you're importing. When the command is finished running, PowerShell displays a list of the new contacts that were created.</span></span> 
    
4. <span data-ttu-id="b61d7-140">Чтобы просмотреть новые внешние контакты, перейдите в центр администрирования Exchange (EAC) и нажмите кнопку **получателей** \> **Контакты**.</span><span class="sxs-lookup"><span data-stu-id="b61d7-140">To view the new external contacts, go to the Exchange admin center (EAC), and then click **Recipients** \> **Contacts**.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="b61d7-141">Инструкции по подключению к центра администрирования Exchange в разделе [Exchange admin center в Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197).</span><span class="sxs-lookup"><span data-stu-id="b61d7-141">For instructions for connecting to the EAC, see [Exchange admin center in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=328197).</span></span> 
  
5. <span data-ttu-id="b61d7-142">При необходимости нажмите кнопку **Обновить** ![значок обновления](media/O365-MDM-Policy-RefreshIcon.gif) обновить список и посмотрите, внешние контакты, которые были импортированы.</span><span class="sxs-lookup"><span data-stu-id="b61d7-142">If necessary, click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the list and see the external contacts that were imported.</span></span> 
    
    <span data-ttu-id="b61d7-143">Импортированные контакты будут отображаться в общей адресной книги в Outlook и Outlook в Интернете.</span><span class="sxs-lookup"><span data-stu-id="b61d7-143">The imported contacts will appear in the shared address book in Outlook and Outlook on the web.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b61d7-144">Можно также просмотреть контакты в центре администрирования Office 365, перейдя на **пользователей** \> **Контакты**.</span><span class="sxs-lookup"><span data-stu-id="b61d7-144">You can also view the contacts in the Office 365 admin center by going to **Users** \> **Contacts**.</span></span> 

## <a name="step-3-add-information-to-the-properties-of-the-external-contacts"></a><span data-ttu-id="b61d7-145">Шаг 3: Добавление сведений на свойства внешние контакты</span><span class="sxs-lookup"><span data-stu-id="b61d7-145">Step 3: Add information to the properties of the external contacts</span></span>

<span data-ttu-id="b61d7-p108">После выполнения команды на шаге 2, создаются внешние контакты, но они не содержат сведения контактного лица или организации, являющийся сведения от наибольшего ячеек в CSV-файл. Это, так как при создании нового внешние контакты заполняются только необходимые свойства. Не обращайте, если у вас нет всей информации, появится в CSV-файл. Если он не существует, он не будет добавлен.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p108">After you run the command in Step 2, the external contacts are created, but they don't contain any of the contact or organization information, which is the information from the most of the cells in the CSV file. This is because when you create new external contacts, only the required properties are populated. Don't worry if you don't have all the information populated in the CSV file. If it's not there, it won't be added.</span></span>
  
1.  <span data-ttu-id="b61d7-p109">Подключения PowerShell к организации Exchange Online. Пошаговые инструкции в разделе [подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="b61d7-p109">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="b61d7-152">Перейдите в папку рабочего стола, CSV-файла, сохраненного в шаге 1. например `C:\Users\Administrator\desktop`.</span><span class="sxs-lookup"><span data-stu-id="b61d7-152">Go to the desktop folder where you saved the CSV file in Step 1; for example `C:\Users\Administrator\desktop`.</span></span>
    
3. <span data-ttu-id="b61d7-153">Выполните следующие две команды, чтобы добавить другие свойства из CSV-файла для внешних контактов, созданный на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="b61d7-153">Run the following two commands to add the other properties from the CSV file to the external contacts that you created in Step 2.</span></span>
    
    ```
    $Contacts = Import-CSV .\ExternalContacts.csv
  
    ```

    ```
    $contacts | ForEach {Set-Contact $_.Name -StreetAddress $_.StreetAddress -City $_.City -StateorProvince $_.StateorProvince -PostalCode $_.PostalCode -Phone $_.Phone -MobilePhone $_.MobilePhone -Pager $_.Pager -HomePhone $_.HomePhone -Company $_.Company -Title $_.Title -OtherTelephone $_.OtherTelephone -Department $_.Department -Fax $_.Fax -Initials $_.Initials -Notes  $_.Notes -Office $_.Office -Manager $_.Manager}
    ```

    > [!NOTE]
    > <span data-ttu-id="b61d7-p110">Параметр _Manager_ может вызывать трудности. Если ячейки не задан в CSV-файл, появится сообщение об ошибке и ни один из сведения о свойствах будет добавлен для контакта. Если вам не нужно указать руководителя, просто удалите ` -Manager $_.Manager ` из предыдущей команды PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p110">The  _Manager_ parameter might be problematic. If the cell is blank in the CSV file, you will get an error and none of the property information will be added to the contact. If you don't need to specify a manager, then just delete  ` -Manager $_.Manager ` from the previous PowerShell command.</span></span> 
  
    <span data-ttu-id="b61d7-157">Опять же он может занять некоторое время для обновления «контакты», в зависимости от того, сколько был импортирован на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="b61d7-157">Again, it might take a while to update the contacts, depending on how many you imported in Step 1.</span></span> 
    
4. <span data-ttu-id="b61d7-158">Чтобы убедиться, что свойства были добавлены к контактам:</span><span class="sxs-lookup"><span data-stu-id="b61d7-158">To verify that the properties were added to the contacts:</span></span> 
    
1. <span data-ttu-id="b61d7-159">В Центре администрирования Exchange перейдите в раздел **Получатели** \> **Контакты**.</span><span class="sxs-lookup"><span data-stu-id="b61d7-159">In the EAC, go to **Recipients** \> **Contacts**.</span></span>
    
2. <span data-ttu-id="b61d7-160">Щелкните контакт и нажмите кнопку **Изменить** ![значок Правка](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) для отображения свойства контакта.</span><span class="sxs-lookup"><span data-stu-id="b61d7-160">Click a contact and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) to display the contact's properties.</span></span> 
    
<span data-ttu-id="b61d7-p111">Ну вот! Пользователи могут видеть контакты и Дополнительные сведения в адресной книге Outlook и Outlook в Интернете.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p111">That's it! Users can see the contacts and the additional information in the address book Outlook and Outlook on the web.</span></span>
  
## <a name="add-more-external-contacts"></a><span data-ttu-id="b61d7-163">Добавьте дополнительные внешние контакты</span><span class="sxs-lookup"><span data-stu-id="b61d7-163">Add more external contacts</span></span>

<span data-ttu-id="b61d7-p112">Повторите шаги с 1 по шаг 3, чтобы добавить новые внешние контакты в Exchange Online. Вы или пользователей в вашей компании так же можно добавить новую строку в CSV-файл для нового контакта. Затем можно запустить команды PowerShell шаг 2 и шаг 3, чтобы создать и добавление сведений на новые контакты.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p112">You can repeat Steps 1 through Step 3 to add new external contacts in Exchange Online. You or users in your company can just add a new row in the CSV file for the new contact. Then you can run the PowerShell commands from Step 2 and Step 3 to create and add information to the new contacts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b61d7-p113">При выполнении команды для создания новых контактов, можно получить возникнет ошибка, сообщающая, что контакты, которые были созданы в более ранних версий уже существует. Однако создать любой новый контакт, добавлены в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="b61d7-p113">When you run the command to create new contacts, you might get an error saying that the contacts that were created earlier already exist. But any new contact added to the CSV file is created.</span></span> 
  
## <a name="hide-external-contacts-from-the-shared-address-book"></a><span data-ttu-id="b61d7-169">Скрыть внешние контакты из общей адресной книги ></span><span class="sxs-lookup"><span data-stu-id="b61d7-169">Hide external contacts from the shared address book></span></span>

<span data-ttu-id="b61d7-p114">Некоторые организации могут использовать внешние контакты, только в том случае, поэтому они могут быть добавлены в качестве членов группы рассылки. В этом случае они может потребоваться скрыть внешние контакты из общей адресной книги. Вот как:</span><span class="sxs-lookup"><span data-stu-id="b61d7-p114">Some companies may use external contacts only so they can be added as members of distribution groups. In this scenario, they may want to hide external contacts from the shared address book. Here's how:</span></span>
  
1.  <span data-ttu-id="b61d7-p115">Подключения PowerShell к организации Exchange Online. Пошаговые инструкции в разделе [подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="b61d7-p115">Connect PowerShell to your Exchange Online organization. For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="b61d7-175">Чтобы скрыть один внешний контакт, выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="b61d7-175">To hide a single external contact, run the following command.</span></span>
    
    ```
    Set-MailContact <external contact> -HiddenFromAddressListsEnabled $true 
    ```
 
    <span data-ttu-id="b61d7-176">Например чтобы скрыть Елены Матвеевой из общей адресной книги, запустите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b61d7-176">For example, to hide Pilar Pinilla from the shared address book, run this command:</span></span>

    ```
    Set-MailContact "Pilar Pinilla" -HiddenFromAddressListsEnabled $true
    ```
   
3. <span data-ttu-id="b61d7-177">Чтобы скрыть все внешние контакты из общей адресной книги, выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="b61d7-177">To hide all external contacts from the shared address book, run this command:</span></span>

    ```
    Get-Contact -ResultSize unlimited -Filter {(RecipientTypeDetails -eq 'MailContact')} | Set-MailContact -HiddenFromAddressListsEnabled $true  
    ```

<span data-ttu-id="b61d7-178">После скрытия их внешние контакты не отображаются в общей адресной книги, но по-прежнему можно добавить их в группу рассылки.</span><span class="sxs-lookup"><span data-stu-id="b61d7-178">After you hide them, external contacts aren't displayed in the shared address book, but you can still add them as members of a distribution group.</span></span>
