---
title: 'Центр администрирования Exchange в Exchange Online Protection '
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
description: "Центр администрирования Exchange \x97 это веб-консоль управления для Microsoft Exchange Online Protection."
ms.openlocfilehash: 144907110af9fcbec1c6399e0695abb705bef409
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002948"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a><span data-ttu-id="d74b0-103">Центр администрирования Exchange в Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="d74b0-103">Exchange admin center in Exchange Online Protection</span></span> 

<span data-ttu-id="d74b0-104">Центр администрирования Exchange  это веб-консоль управления для Microsoft Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="d74b0-104">The Exchange admin center (EAC) is the web-based management console for Microsoft Exchange Online Protection (EOP).</span></span> 
  
<span data-ttu-id="d74b0-p101">Ищете версию этой статьи для Exchange 2013? См. статью [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span><span class="sxs-lookup"><span data-stu-id="d74b0-p101">Looking for the Exchange 2013 version of this topic? See [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span></span>
  
<span data-ttu-id="d74b0-p102">Ищете версию этой статьи для Exchange Online? См. статью [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="d74b0-p102">Looking for the Exchange Online version of this topic? See [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>
  
## <a name="accessing-the-eac"></a><span data-ttu-id="d74b0-109">Вход в Центр администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="d74b0-109">Accessing the EAC</span></span>

<span data-ttu-id="d74b0-p103">В большинстве случаев клиенты Exchange Online Protection получают доступ к Центру администрирования Exchange через Центр администрирования Office 365. Ссылка на Exchange Online Protection расположена в раскрывающемся меню на плитке **Администратор**, находящейся рядом с плиткой **Я**. Чтобы перейти в Центр администрирования Exchange, щелкните плитку **Администратор** и в раскрывающемся меню выберите **Exchange Online Protection**.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p103">In most cases, EOP customers will access the EAC through the Office 365 admin center. You can find a link to EOP in the drop-down menu in the **Admin** tile, which is next to the **Me** tile. Click the **Admin** tile and select **Exchange Online Protection** from the drop down menu to be taken to the EAC.</span></span> 
  
<span data-ttu-id="d74b0-p104">Перейти к странице входа в Центр администрирования Exchange можно также непосредственно по URL-адресу: https://admin.protection.outlook.com/ecp/\<companydomain\>. Например, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. После того как вы укажете свои учетные данные пользователя, вы перейдете непосредственно в Центр администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p104">You can also access the EAC sign in page directly via the following URL: https://admin.protection.outlook.com/ecp/\<companydomain\>. For example, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. After specifying your user credentials you will be taken directly into the EAC.</span></span>
  
## <a name="common-user-interface-elements-in-the-eac"></a><span data-ttu-id="d74b0-116">Общие элементы пользовательского интерфейса в Центре администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="d74b0-116">Common user interface elements in the EAC</span></span>

<span data-ttu-id="d74b0-117">В этом разделе рассматриваются элементы интерфейса пользователя в Центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="d74b0-117">This section describes the user interface elements that are found in the EAC.</span></span>
  
![EOP AdminCenter](media/EOP-AdminCenter.png)
  
### <a name="feature-pane"></a><span data-ttu-id="d74b0-119">Панель "Функции"</span><span class="sxs-lookup"><span data-stu-id="d74b0-119">Feature Pane</span></span>

<span data-ttu-id="d74b0-p105">Это первый уровень навигации для большинства заданий, выполняемых в Центре администрирования Exchange. Панель функций состоит из областей функций.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p105">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>
  
1. <span data-ttu-id="d74b0-122">**Получатели**. Здесь представлены внутренние пользователи и внешние контакты.</span><span class="sxs-lookup"><span data-stu-id="d74b0-122">**Recipients** This is where you'll view internal users and external contacts.</span></span> 
    
2. <span data-ttu-id="d74b0-123">**Разрешения**. Здесь выполняется управление ролями администратора.</span><span class="sxs-lookup"><span data-stu-id="d74b0-123">**Permissions** This where you'll manage administrator roles.</span></span> 
    
3. <span data-ttu-id="d74b0-124">**Управление соответствием**. Здесь представлены журналы и отчеты аудита, такие как отчет группы ролей администратора.</span><span class="sxs-lookup"><span data-stu-id="d74b0-124">**Compliance Management** This is where you'll find audit logs and reports, such as the administrator role group report.</span></span> 
    
4. <span data-ttu-id="d74b0-125">**Защита**. Здесь выполняется управление защитой организации от вредоносных программ и нежелательной почты, а также сообщениями, поставленными на карантин.</span><span class="sxs-lookup"><span data-stu-id="d74b0-125">**Protection** This is where you'll manage anti-malware and anti-spam protection for your organization, as well as manage messages in quarantine.</span></span> 
    
5. <span data-ttu-id="d74b0-126">**Поток обработки почты**. В этой области выполняется трассировка сообщений, а также управление правилами, обслуживаемыми доменами и соединителями.</span><span class="sxs-lookup"><span data-stu-id="d74b0-126">**Mail Flow** This is where you'll manage rules, accepted domains, and connectors, as well as where you'll go to perform message trace.</span></span> 
    
### <a name="tabs"></a><span data-ttu-id="d74b0-127">Вкладки</span><span class="sxs-lookup"><span data-stu-id="d74b0-127">Tabs</span></span>

<span data-ttu-id="d74b0-p106">Вкладки — это второй уровень навигации. Каждый из компонентов содержит различные вкладки, на каждой из которых будет представлена функция.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p106">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>
  
### <a name="toolbar"></a><span data-ttu-id="d74b0-130">Панель инструментов</span><span class="sxs-lookup"><span data-stu-id="d74b0-130">Toolbar</span></span>

<span data-ttu-id="d74b0-p107">При выборе большинства вкладок отображается панель инструментов. Панель инструментов содержит значки, которые выполняют определенное действие. Значки и их действия описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p107">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>
  
|<span data-ttu-id="d74b0-134">**Значок**</span><span class="sxs-lookup"><span data-stu-id="d74b0-134">**Icon**</span></span>|<span data-ttu-id="d74b0-135">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d74b0-135">**Name**</span></span>|<span data-ttu-id="d74b0-136">**Действие**</span><span class="sxs-lookup"><span data-stu-id="d74b0-136">**Action**</span></span>|
|:-----|:-----|:-----|
|![Значок добавления](media/ITPro-EAC-AddIcon.gif)           <br/> |<span data-ttu-id="d74b0-138">"Добавить", "Создать"</span><span class="sxs-lookup"><span data-stu-id="d74b0-138">Add, New</span></span>  <br/> |<span data-ttu-id="d74b0-p108">Используйте этот значок для создания нового объекта. Некоторые из этих значков имеют стрелку вниз, щелкнув которую, можно отобразить дополнительные объекты, которые можно создать.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p108">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>  <br/> |
|![Значок редактирования](media/ITPro-EAC-EditIcon.gif)           <br/> |<span data-ttu-id="d74b0-142">Изменить</span><span class="sxs-lookup"><span data-stu-id="d74b0-142">Edit</span></span>  <br/> |<span data-ttu-id="d74b0-143">Используйте этот значок для редактирования объекта.</span><span class="sxs-lookup"><span data-stu-id="d74b0-143">Use this icon to edit an object.</span></span>  <br/> |
|![Значок удаления](media/ITPro-EAC-DeleteIcon.gif)           <br/> |<span data-ttu-id="d74b0-145">Удаление</span><span class="sxs-lookup"><span data-stu-id="d74b0-145">Delete</span></span>  <br/> |<span data-ttu-id="d74b0-p109">Используйте этот значок для удаления объекта. У некоторых значков удаления есть стрелка вниз, которая позволяет отобразить дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p109">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>  <br/> |
|![значок поиска](media/ITPro-EAC-.gif)           <br/> |<span data-ttu-id="d74b0-149">Поиск</span><span class="sxs-lookup"><span data-stu-id="d74b0-149">Search</span></span>  <br/> |<span data-ttu-id="d74b0-150">Этот значок позволяет открыть поле поиска, в котором можно ввести фразу поиска для объекта, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="d74b0-150">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>  <br/> |
|![Значок обновления](media/ITPro-EAC-RefreshIcon.gif)           <br/> |<span data-ttu-id="d74b0-152">Обновить</span><span class="sxs-lookup"><span data-stu-id="d74b0-152">Refresh</span></span>  <br/> |<span data-ttu-id="d74b0-153">Используйте этот значок, чтобы обновить представление списка.</span><span class="sxs-lookup"><span data-stu-id="d74b0-153">Use this icon to refresh the list view.</span></span>  <br/> |
|![Значок дополнительных параметров](media/ITPro-EAC-MoreOptionsIcon.gif)           <br/> |<span data-ttu-id="d74b0-155">Дополнительные параметры</span><span class="sxs-lookup"><span data-stu-id="d74b0-155">More options</span></span>  <br/> |<span data-ttu-id="d74b0-p110">Используйте этот значок для просмотра дополнительных действий, которые можно выполнить для объектов этой вкладки. Например, при нажатии этого значка в области **Получатели \> Пользователи** отображается параметр для выполнения **расширенного поиска**.  </span><span class="sxs-lookup"><span data-stu-id="d74b0-p110">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.  </span></span><br/> |
|![Значок "Стрелка вверх"](media/ITPro-EAC-UpArrowIcon.gif)![Значок "Стрелка вниз"](media/ITPro-EAC-DownArrowIcon.gif)           <br/> |<span data-ttu-id="d74b0-160">Стрелка вверх и стрелка вниз</span><span class="sxs-lookup"><span data-stu-id="d74b0-160">Up arrow and down arrow</span></span>  <br/> |<span data-ttu-id="d74b0-161">Используйте эти значки для изменения приоритета объекта.</span><span class="sxs-lookup"><span data-stu-id="d74b0-161">Use these icons to move an object's priority up or down.</span></span>  <br/> |
|![Значок "Удалить"](media/ITPro-EAC-RemoveIcon.gif)           <br/> |<span data-ttu-id="d74b0-163">Удалить</span><span class="sxs-lookup"><span data-stu-id="d74b0-163">Remove</span></span>  <br/> |<span data-ttu-id="d74b0-164">Используйте этот значок, чтобы удалять объекты из списка.</span><span class="sxs-lookup"><span data-stu-id="d74b0-164">Use this icon to remove objects from a list.</span></span>  <br/> |
   
### <a name="list-view"></a><span data-ttu-id="d74b0-165">Представление списка</span><span class="sxs-lookup"><span data-stu-id="d74b0-165">List View</span></span>

<span data-ttu-id="d74b0-p111">При выборе вкладки в большинстве случаев отображается представление списка. Лимит просмотра в Центре администрирования Exchange составляет около 10 000 объектов. Кроме того, включено постраничное разделение, так что вы можете листать страницы результатов.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p111">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>
  
### <a name="details-pane"></a><span data-ttu-id="d74b0-169">Область сведений</span><span class="sxs-lookup"><span data-stu-id="d74b0-169">Details Pane</span></span>

<span data-ttu-id="d74b0-p112">При выборе объекта в представлении списка информация об этом объекте отображается в области сведений. В некоторых случаях область сведений включает задачи управления.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p112">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>
  
### <a name="me-tile-and-help"></a><span data-ttu-id="d74b0-172">Иконка "Я" и справка</span><span class="sxs-lookup"><span data-stu-id="d74b0-172">Me tile and Help</span></span>

<span data-ttu-id="d74b0-p113">Плитка **Я** позволяет выйти из Центра администрирования Exchange и войти в него как другой пользователь. При помощи раскрывающегося меню справки **Справка**![Значок справки](media/ITPro-EAC-HelpIcon.gif) можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d74b0-p113">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](media/ITPro-EAC-HelpIcon.gif) drop-down menu, you can perform the following actions:</span></span> 
  
1. <span data-ttu-id="d74b0-175">**Справка** Щелкните ![Значок справки](media/ITPro-EAC-HelpIcon.gif) для просмотра справки в Интернете.</span><span class="sxs-lookup"><span data-stu-id="d74b0-175">**Help** Click ![Help Icon](media/ITPro-EAC-HelpIcon.gif) to view the online help content.</span></span> 
    
2. <span data-ttu-id="d74b0-p114">**Отключение всплывающей справки** Всплывающая справка отображает контекстно-зависимую справку для полей при создании или редактировании объекта. Всплывающую справку можно отключить. Если она отключена, ее можно включить.</span><span class="sxs-lookup"><span data-stu-id="d74b0-p114">**Disable Help bubble** The Help bubble displays contextual help for fields when you create or edit an object. You can turn off the Help bubble or turn it on if it has been disabled.</span></span> 
    
3. <span data-ttu-id="d74b0-178">**Авторские права** Перейдите по этой ссылке, чтобы прочитать уведомление об авторских правах для Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="d74b0-178">**Copyright** Click this link to read the copyright notice for Exchange Online Protection.</span></span> 
    
4. <span data-ttu-id="d74b0-179">**Конфиденциальность** Нажмите, чтобы прочитать политику конфиденциальности для Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="d74b0-179">**Privacy** Click to read the privacy policy for Exchange Online Protection.</span></span> 
    
## <a name="supported-browsers"></a><span data-ttu-id="d74b0-180">Поддерживаемые браузеры</span><span class="sxs-lookup"><span data-stu-id="d74b0-180">Supported Browsers</span></span>

<span data-ttu-id="d74b0-p115">Чтобы работа с Центром администрирования Exchange (EAC) была максимально продуктивной, рекомендуется всегда использовать только последние версии браузеров, клиентов Office и приложений. Мы также рекомендуем устанавливать обновления по мере их доступности. Для получения дополнительных сведений о поддерживаемых браузерах и системных требованиях для службы см. раздел [Требования к системе для Office 365](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span><span class="sxs-lookup"><span data-stu-id="d74b0-p115">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps. We also recommend that you install software updates when they become available. For more information about the supported browsers and system requirements for the service, see [Office 365 System Requirements](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span></span> 
  
## <a name="supported-languages-in-eop"></a><span data-ttu-id="d74b0-184">Поддерживаемые в EOP языки</span><span class="sxs-lookup"><span data-stu-id="d74b0-184">Supported languages in EOP</span></span>

<span data-ttu-id="d74b0-185">Для Exchange Online Protection доступны и поддерживаются следующие языки.</span><span class="sxs-lookup"><span data-stu-id="d74b0-185">The following languages are supported and available for Exchange Online Protection.</span></span>
  
- <span data-ttu-id="d74b0-186">Амхарский</span><span class="sxs-lookup"><span data-stu-id="d74b0-186">Amharic</span></span>
    
- <span data-ttu-id="d74b0-187">Арабский</span><span class="sxs-lookup"><span data-stu-id="d74b0-187">Arabic</span></span>
    
- <span data-ttu-id="d74b0-188">Баскский (Basque)</span><span class="sxs-lookup"><span data-stu-id="d74b0-188">Basque (Basque)</span></span>
    
- <span data-ttu-id="d74b0-189">Бенгальский (Индия)</span><span class="sxs-lookup"><span data-stu-id="d74b0-189">Bengali (India)</span></span>
    
- <span data-ttu-id="d74b0-190">Болгарский</span><span class="sxs-lookup"><span data-stu-id="d74b0-190">Bulgarian</span></span>
    
- <span data-ttu-id="d74b0-191">Каталанский</span><span class="sxs-lookup"><span data-stu-id="d74b0-191">Catalan</span></span>
    
- <span data-ttu-id="d74b0-192">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="d74b0-192">Chinese (Simplified)</span></span>
    
- <span data-ttu-id="d74b0-193">Китайский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="d74b0-193">Chinese (Traditional)</span></span>
    
- <span data-ttu-id="d74b0-194">Хорватский</span><span class="sxs-lookup"><span data-stu-id="d74b0-194">Croatian</span></span>
    
- <span data-ttu-id="d74b0-195">Чешский</span><span class="sxs-lookup"><span data-stu-id="d74b0-195">Czech</span></span>
    
- <span data-ttu-id="d74b0-196">Датский</span><span class="sxs-lookup"><span data-stu-id="d74b0-196">Danish</span></span>
    
- <span data-ttu-id="d74b0-197">Голландский</span><span class="sxs-lookup"><span data-stu-id="d74b0-197">Dutch</span></span>
    
- <span data-ttu-id="d74b0-198">Голландский</span><span class="sxs-lookup"><span data-stu-id="d74b0-198">Dutch</span></span>
    
- <span data-ttu-id="d74b0-199">Английский</span><span class="sxs-lookup"><span data-stu-id="d74b0-199">English</span></span>
    
- <span data-ttu-id="d74b0-200">Эстонский</span><span class="sxs-lookup"><span data-stu-id="d74b0-200">Estonian</span></span>
    
- <span data-ttu-id="d74b0-201">Филиппинский (Филиппины)</span><span class="sxs-lookup"><span data-stu-id="d74b0-201">Filipino (Philippines)</span></span>
    
- <span data-ttu-id="d74b0-202">Финский</span><span class="sxs-lookup"><span data-stu-id="d74b0-202">Finnish</span></span>
    
- <span data-ttu-id="d74b0-203">Французский</span><span class="sxs-lookup"><span data-stu-id="d74b0-203">French</span></span>
    
- <span data-ttu-id="d74b0-204">Галисийский</span><span class="sxs-lookup"><span data-stu-id="d74b0-204">Galician</span></span>
    
- <span data-ttu-id="d74b0-205">Немецкий</span><span class="sxs-lookup"><span data-stu-id="d74b0-205">German</span></span>
    
- <span data-ttu-id="d74b0-206">Греческий</span><span class="sxs-lookup"><span data-stu-id="d74b0-206">Greek</span></span>
    
- <span data-ttu-id="d74b0-207">Гуджарати</span><span class="sxs-lookup"><span data-stu-id="d74b0-207">Gujarati</span></span>
    
- <span data-ttu-id="d74b0-208">Иврит</span><span class="sxs-lookup"><span data-stu-id="d74b0-208">Hebrew</span></span>
    
- <span data-ttu-id="d74b0-209">Хинди</span><span class="sxs-lookup"><span data-stu-id="d74b0-209">Hindi</span></span>
    
- <span data-ttu-id="d74b0-210">Венгерский</span><span class="sxs-lookup"><span data-stu-id="d74b0-210">Hungarian</span></span>
    
- <span data-ttu-id="d74b0-211">Исландский</span><span class="sxs-lookup"><span data-stu-id="d74b0-211">Icelandic</span></span>
    
- <span data-ttu-id="d74b0-212">Индонезийский</span><span class="sxs-lookup"><span data-stu-id="d74b0-212">Indonesian</span></span>
    
- <span data-ttu-id="d74b0-213">Итальянский</span><span class="sxs-lookup"><span data-stu-id="d74b0-213">Italian</span></span>
    
- <span data-ttu-id="d74b0-214">Японский</span><span class="sxs-lookup"><span data-stu-id="d74b0-214">Japanese</span></span>
    
- <span data-ttu-id="d74b0-215">Каннада</span><span class="sxs-lookup"><span data-stu-id="d74b0-215">Kannada</span></span>
    
- <span data-ttu-id="d74b0-216">Казахский</span><span class="sxs-lookup"><span data-stu-id="d74b0-216">Kazakh</span></span>
    
- <span data-ttu-id="d74b0-217">Суахили</span><span class="sxs-lookup"><span data-stu-id="d74b0-217">Kiswahili</span></span>
    
- <span data-ttu-id="d74b0-218">Корейский</span><span class="sxs-lookup"><span data-stu-id="d74b0-218">Korean</span></span>
    
- <span data-ttu-id="d74b0-219">Латышский</span><span class="sxs-lookup"><span data-stu-id="d74b0-219">Latvian</span></span>
    
- <span data-ttu-id="d74b0-220">Литовский</span><span class="sxs-lookup"><span data-stu-id="d74b0-220">Lithuanian</span></span>
    
- <span data-ttu-id="d74b0-221">Малайский (Бруней-Даруссалам)</span><span class="sxs-lookup"><span data-stu-id="d74b0-221">Malay (Brunei Darussalam)</span></span>
    
- <span data-ttu-id="d74b0-222">Малайский (Малайзия)</span><span class="sxs-lookup"><span data-stu-id="d74b0-222">Malay (Malaysia)</span></span>
    
- <span data-ttu-id="d74b0-223">Малаялам</span><span class="sxs-lookup"><span data-stu-id="d74b0-223">Malayalam</span></span>
    
- <span data-ttu-id="d74b0-224">Маратхи</span><span class="sxs-lookup"><span data-stu-id="d74b0-224">Marathi</span></span>
    
- <span data-ttu-id="d74b0-225">Норвежский (букмол)</span><span class="sxs-lookup"><span data-stu-id="d74b0-225">Norwegian (Bokmål)</span></span>
    
- <span data-ttu-id="d74b0-226">Норвежский (нюнорск)</span><span class="sxs-lookup"><span data-stu-id="d74b0-226">Norwegian (Nynorsk)</span></span>
    
- <span data-ttu-id="d74b0-227">Ория</span><span class="sxs-lookup"><span data-stu-id="d74b0-227">Oriya</span></span>
    
- <span data-ttu-id="d74b0-228">Персидский</span><span class="sxs-lookup"><span data-stu-id="d74b0-228">Persian</span></span>
    
- <span data-ttu-id="d74b0-229">Польский</span><span class="sxs-lookup"><span data-stu-id="d74b0-229">Polish</span></span>
    
- <span data-ttu-id="d74b0-230">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="d74b0-230">Portuguese (Brazil)</span></span>
    
- <span data-ttu-id="d74b0-231">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="d74b0-231">Portuguese (Portugal)</span></span>
    
- <span data-ttu-id="d74b0-232">Румынский</span><span class="sxs-lookup"><span data-stu-id="d74b0-232">Romanian</span></span>
    
- <span data-ttu-id="d74b0-233">Русский</span><span class="sxs-lookup"><span data-stu-id="d74b0-233">Russian</span></span>
    
- <span data-ttu-id="d74b0-234">Сербский (кириллица, Сербия)</span><span class="sxs-lookup"><span data-stu-id="d74b0-234">Serbian (Cyrillic, Serbia)</span></span>
    
- <span data-ttu-id="d74b0-235">Сербский (латиница)</span><span class="sxs-lookup"><span data-stu-id="d74b0-235">Serbian (Latin)</span></span>
    
- <span data-ttu-id="d74b0-236">Словацкий</span><span class="sxs-lookup"><span data-stu-id="d74b0-236">Slovak</span></span>
    
- <span data-ttu-id="d74b0-237">Словенский</span><span class="sxs-lookup"><span data-stu-id="d74b0-237">Slovenian</span></span>
    
- <span data-ttu-id="d74b0-238">Испанский</span><span class="sxs-lookup"><span data-stu-id="d74b0-238">Spanish</span></span>
    
- <span data-ttu-id="d74b0-239">Шведский</span><span class="sxs-lookup"><span data-stu-id="d74b0-239">Swedish</span></span>
    
- <span data-ttu-id="d74b0-240">Тамильский</span><span class="sxs-lookup"><span data-stu-id="d74b0-240">Tamil</span></span>
    
- <span data-ttu-id="d74b0-241">Телугу</span><span class="sxs-lookup"><span data-stu-id="d74b0-241">Telugu</span></span>
    
- <span data-ttu-id="d74b0-242">Тайский</span><span class="sxs-lookup"><span data-stu-id="d74b0-242">Thai</span></span>
    
- <span data-ttu-id="d74b0-243">Турецкий</span><span class="sxs-lookup"><span data-stu-id="d74b0-243">Turkish</span></span>
    
- <span data-ttu-id="d74b0-244">Украинский</span><span class="sxs-lookup"><span data-stu-id="d74b0-244">Ukrainian</span></span>
    
- <span data-ttu-id="d74b0-245">Урду</span><span class="sxs-lookup"><span data-stu-id="d74b0-245">Urdu</span></span>
    
- <span data-ttu-id="d74b0-246">Вьетнамский</span><span class="sxs-lookup"><span data-stu-id="d74b0-246">Vietnamese</span></span>
    
- <span data-ttu-id="d74b0-247">Валлийский</span><span class="sxs-lookup"><span data-stu-id="d74b0-247">Welsh</span></span>
    

