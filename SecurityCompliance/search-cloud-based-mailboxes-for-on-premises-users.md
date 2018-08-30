---
title: Поиск облачные почтовые ящики для локальных пользователей в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/4/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MST160
- MET150
ms.assetid: 3f7dde1a-a8ea-4366-86da-8ee6777f357c
description: Использовать средство поиска контента в Office 365 безопасность &amp; центре соответствия требованиям для поиска и экспортировать данные чата MicrosoftTeams (называемые чаты 1xN) для локальных пользователей в гибридном развертывании Exchange.
ms.openlocfilehash: a504dfcf4c82bec036137b90312c01a0b2326ccc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534656"
---
# <a name="searching-cloud-based-mailboxes-for-on-premises-users-in-office-365"></a><span data-ttu-id="8f85a-103">Поиск облачные почтовые ящики для локальных пользователей в Office 365</span><span class="sxs-lookup"><span data-stu-id="8f85a-103">Searching cloud-based mailboxes for on-premises users in Office 365</span></span>

<span data-ttu-id="8f85a-p101">Если ваша организация имеет гибридного развертывания Exchange и включил группами Майкрософт, пользователи могут использовать приложения разговора группами для обмена мгновенными сообщениями. Для пользователей на основе облака группы чата данные (также называемая чаты 1xN) сохраняются свой основной почтовый ящик на основе облака. Если локальный пользователь использует приложения разговора группы, их основной почтовый ящик — расположены в локальной. Чтобы обойти данное ограничение, Microsoft выпущен новая функция, где создан области хранилища на основе облака (называемые облачного почтового ящика для локальных пользователей) для хранения данных группы чата для локальных пользователей. Это позволяет использовать средство поиска контента в Office 365 безопасность &amp; центре соответствия требованиям для поиска и экспорт групп данных чата для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p101">If your organization has an Exchange hybrid deployment and has enabled Microsoft Teams, users can use the Teams chat application for instant messaging. For the cloud-based user, the Teams chat data (also called 1xN chats) is saved to their primary cloud-based mailbox. When an on-premises user uses the Team chat application, their primary mailbox is located on-premises. To get around this limitation, Microsoft has released a new feature where a cloud-based storage area (called a cloud-based mailbox for on-premises users) is created to store Teams chat data for on-premises users. This lets you use the Content Search tool in the Office 365 Security &amp; Compliance Center to search and export Teams chat data for on-premises users.</span></span> 
  
<span data-ttu-id="8f85a-109">Ниже приведены требования и ограничения по настройке и для установки и выполните поиск облачные почтовые ящики для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f85a-109">Here are the requirements and limitation for setting up and to set up and search cloud-based mailboxes for on-premises users:</span></span>
  
- <span data-ttu-id="8f85a-p102">Учетные записи пользователей в вашей локальной службы каталогов (такими как Active Directory) должны быть синхронизированы с Azure Active Directory, службы каталогов в Office 365. Это означает, что учетная запись пользователя почты создается в Office 365 и связанный с пользователем, основной почтовый ящик которого находится в локальной организации.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p102">The user accounts in your on-premises directory service (such as Active Directory) must be synchronized with Azure Active Directory, the directory service in Office 365. This means that a mail user account is created in Office 365 and is associated with a user whose primary mailbox is located in the on-premises organization.</span></span>
    
- <span data-ttu-id="8f85a-p103">Облачного почтового ящика для локальных пользователей — чата групп используется только для хранения данных. Локальный пользователь не может войти в почтовый ящик на основе облака или доступ к каким-либо образом. Он не может использоваться для отправки и получения сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p103">The cloud-based mailbox for on-premises users is used only store Teams chat data. An on-premises user can't sign in to the cloud-based mailbox or access in any way. It can't be used to send or receive email messages.</span></span> 
    
- <span data-ttu-id="8f85a-p104">Необходимо отправить запрос в службу поддержки Майкрософт для включения вашей организации для поиска групп данные чата в облачные почтовые ящики для локальных пользователей. Просмотреть [контроля над заполнением записей запроса с помощью службы поддержки Майкрософт для включения этой функции безопасности &amp; центре соответствия требованиям](#filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center) в этой статье.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p104">You have to submit a request to Microsoft Support to enable your organization to search for Teams chat data in the cloud-based mailboxes for on-premises users. See [Filing a request with Microsoft Support to enable this feature in the Security &amp; Compliance Center](#filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center) in this article.</span></span> 
    
 <span data-ttu-id="8f85a-p105">**Примечание:** Беседы канала группы всегда хранятся в облачного почтового ящика, связанный с группой. Это означает, что поиск контента можно использовать канал поиска беседы не имеют в файл запрос на обслуживание. Дополнительные сведения о поиске группами channel бесед, [Поиск групп Майкрософт и Office 365 группы](content-search.md#searching-microsoft-teams-and-office-365-groups)отображается.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p105">**Note:** Teams channel conversations are always stored in the cloud-based mailbox that's associated with the Team. That means you can use Content Search to search channel conversations without have to file a support request. For more information about searching Teams channel conversations, see [Searching Microsoft Teams and Office 365 Groups](content-search.md#searching-microsoft-teams-and-office-365-groups).</span></span>
  
## <a name="how-it-works"></a><span data-ttu-id="8f85a-120">Как это работает</span><span class="sxs-lookup"><span data-stu-id="8f85a-120">How it works</span></span>

<span data-ttu-id="8f85a-p106">Если пользователь включен группы Microsoft имеет локального почтового ящика и своей учетной записи и удостоверения пользователя были синхронизированы с облаком, Microsoft создает облачного почтового ящика для хранения данных чата 1xN группами. После данных чата группы хранится в облачного почтового ящика, будет индексирован для поиска. Это позволяет использовать поиска контента (и операций поиска, связанного с вариантах eDiscovery) для поиска, предварительный просмотр и экспорт данных чата группами для локальных пользователей. Вы также можете использовать \*\* \*ComplianceSearch\*\* командлеты безопасности Office 365 &amp; PowerShell центр соответствия требованиям для поиска группы чата данных для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p106">If a Microsoft Teams-enabled user has an on-premises mailbox and their user account/identity has been synched to the cloud, Microsoft creates a cloud-based mailbox to store 1xN Teams chat data. After the Teams chat data is stored in the cloud-based mailbox, it's indexed for search. This lets you Use Content Search (and searches associated with eDiscovery cases) to search, preview, and export Teams chat data for on-premises users. You can also use **\*ComplianceSearch** cmdlets in the Office 365 Security &amp; Compliance Center PowerShell to search for Teams chat data for on-premises users.</span></span> 
  
<span data-ttu-id="8f85a-125">На следующем рисунке показано, что рабочего процесса как группы чата данных для локальных пользователей доступен для поиска, предварительный просмотр и экспорт.</span><span class="sxs-lookup"><span data-stu-id="8f85a-125">The following graphic shows the workflow of how Teams chat data for on-premises users is available to search, preview, and export.</span></span>
  
![Облачная хранилища для локальных пользователей в группах Майкрософт](media/895845f8-2ceb-47ed-96c9-5ab7f1aea916.png)
  
<span data-ttu-id="8f85a-127">В дополнение к этой новой возможности по-прежнему можно использовать поиска контента для поиска, предварительный просмотр и экспорт специалистов по содержимого в облачной сайт SharePoint и почтовых ящиков Exchange с каждой группы разработчиков Microsoft и рабочих групп 1xN данные чата в почтовом ящике Exchange Online пользователи на основе облака.</span><span class="sxs-lookup"><span data-stu-id="8f85a-127">In addition to this new capability, you can still use Content Search to search, preview, and export Teams content in the cloud-based SharePoint site and Exchange mailbox associated with each Microsoft Team and 1xN Teams chat data in the Exchange Online mailbox for cloud-based users.</span></span>

## <a name="filing-a-request-with-microsoft-support-to-enable-this-feature-in-the-security-amp-compliance-center"></a><span data-ttu-id="8f85a-128">Контроля над заполнением записей запроса с помощью службы поддержки Майкрософт для включения этой функции безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8f85a-128">Filing a request with Microsoft Support to enable this feature in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="8f85a-p107">Необходимо файл запроса с помощью службы поддержки Майкрософт для включения организации использовать графический интерфейс пользователя в системы &amp; центре соответствия требованиям для поиска групп данные чата в облачные почтовые ящики для локальных пользователей. Обратите внимание на то, что эта функция доступна в Office 365 безопасность &amp; PowerShell центр соответствия требованиям. Не требуется отправить запрос поддержки на использование PowerShell для поиска данных чата группами для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p107">You must file a request with Microsoft Support to enable your organization to use the graphical user interface in the Security &amp; Compliance Center to search for Teams chat data in the cloud-based mailboxes for on-premises users. Note that this feature is available in Office 365 Security &amp; Compliance Center PowerShell. You don't have to submit a support request to use PowerShell to search for Teams chat data for on-premises users.</span></span> 
  
<span data-ttu-id="8f85a-132">Отправьте этот запрос в службу технической поддержки Майкрософт содержат следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="8f85a-132">Include the following information when you submit the request to Microsoft Support:</span></span>
  
- <span data-ttu-id="8f85a-133">Имя домена по умолчанию организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="8f85a-133">The default domain name of your Office 365 organization.</span></span>
    
- <span data-ttu-id="8f85a-p108">Имя клиента и идентификатор клиента для организации Office 365. Их можно найти на портале Azure Active Directory (в разделе **Управление** \> **Свойства**). В разделе [Поиск идентификатора клиента Office 365](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b).</span><span class="sxs-lookup"><span data-stu-id="8f85a-p108">The tenant name and tenant ID of your Office 365 organization. You can find these in the Azure Active Directory portal (under **Manage** \> **Properties**). See [Find your Office 365 tenant ID](https://support.office.com/article/6891b561-a52d-4ade-9f39-b492285e2c9b).</span></span>
    
- <span data-ttu-id="8f85a-p109">Ниже заголовок и описание назначения запроса поддержки: «Включить поиск контента приложения для локальных пользователей». Это позволит маршрутизации запроса для Office 365 обнаружения электронных данных команды разработчиков пользователей, которые будут реализованы запроса.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p109">The following title or description of the purpose of the support request: "Enable Application Content Search for On-premises Users". This will help route the request to the Office 365 eDiscovery engineering team who will implement the request.</span></span> 
    
<span data-ttu-id="8f85a-p110">После изменения инженерной поддержки корпорации Майкрософт будет отправлять дату примерный развертывания. Обратите внимание на то, что процесс развертывания обычно занимает 2-3 недель после отправки запроса поддержки.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p110">After the engineering change is made, Microsoft Support will send you an estimated deployment date. Note that the deployment process usually takes 2-3 weeks after you submit the support request.</span></span> 
  
### <a name="what-happens-after-this-feature-is-enabled"></a><span data-ttu-id="8f85a-141">Что происходит после включения этой функции?</span><span class="sxs-lookup"><span data-stu-id="8f85a-141">What happens after this feature is enabled?</span></span>

<span data-ttu-id="8f85a-142">После развертывания этой функции в организации Office 365 следующие изменения вносятся в поиск контента и поиска, связанного с eDiscovery случае в системы &amp; центре соответствия требованиям:</span><span class="sxs-lookup"><span data-stu-id="8f85a-142">After this feature is deployed in your Office 365 organization, the following changes are made in Content Search and in searches associated with an eDiscovery case in the Security &amp; Compliance Center:</span></span>
  
- <span data-ttu-id="8f85a-143">Флажок **контента приложения добавьте Office для локальных пользователей** добавляется в разделе **расположения** в поиске содержимого.</span><span class="sxs-lookup"><span data-stu-id="8f85a-143">The **Add Office app content for on-premises users** checkbox is added under the **Locations** in Content Search.</span></span> 
    
    ![Флажок «Добавление контента приложения Office для локальных пользователей» добавляется в пользовательский интерфейс поиска контента](media/599e751e-17bd-408d-a18c-127538de6e85.png)
  
- <span data-ttu-id="8f85a-145">Локальные пользователи отображаются в средстве выбора расположения контента, используемая для выбора почтовых ящиков пользователей для поиска.</span><span class="sxs-lookup"><span data-stu-id="8f85a-145">On-premises users are displayed in the content locations picker that you use to select user mailboxes to search.</span></span> 
    

  
## <a name="searching-for-teams-chat-content-in-cloud-based-mailboxes-for-on-premises-users"></a><span data-ttu-id="8f85a-146">Поиск групп чата контента в облачные почтовые ящики для локальных пользователей</span><span class="sxs-lookup"><span data-stu-id="8f85a-146">Searching for Teams chat content in cloud-based mailboxes for on-premises users</span></span>

<span data-ttu-id="8f85a-147">После включения компонента поиска контента можно использовать в системы &amp; центре соответствия требованиям для поиска групп данные чата в облачные почтовые ящики для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f85a-147">After the feature has been enabled, you can use Content Search in the Security &amp; Compliance Center to search for Teams chat data in the cloud-based mailboxes for on-premises users.</span></span> 
  
1. <span data-ttu-id="8f85a-148">В разделе Безопасность &amp; центре соответствия требованиям, чтобы перейти на **поиска &amp; расследования** \> **поиска контента**</span><span class="sxs-lookup"><span data-stu-id="8f85a-148">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**</span></span>
    
2. <span data-ttu-id="8f85a-149">На странице **поиска** выберите ![значком Добавить](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **новый поиск**.</span><span class="sxs-lookup"><span data-stu-id="8f85a-149">On the **Search** page, click ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**.</span></span>
    
    <span data-ttu-id="8f85a-p111">Как объяснялось ранее checkbox **контента приложения добавьте Office для локальных пользователей** отображается в разделе **расположения**. Обратите внимание на то, что установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p111">As previously explained, the **Add Office app content for on-premises users** checkbox is displayed under **Locations**. Note that it is selected by default.</span></span>
    
3. <span data-ttu-id="8f85a-p112">Создание запроса ключевого слова и при необходимости добавьте условия в поисковый запрос. Для поиска только для групп обсуждений данных, можно добавить следующий запрос в поле **ключевые слова** :</span><span class="sxs-lookup"><span data-stu-id="8f85a-p112">Create the keyword query and add conditions to the search query if necessary. To only search for Team chats data, you can add the following query in the **Keywords** box:</span></span> 
    
    ```
    kind:im
    ``` 

4. <span data-ttu-id="8f85a-154">На этом этапе можно выбрать один из следующих параметров в разделе **расположения**:</span><span class="sxs-lookup"><span data-stu-id="8f85a-154">At this point, you can choose one of the following options under **Locations**:</span></span>
    
    - <span data-ttu-id="8f85a-p113">**Все расположения** — выберите этот параметр для поиска почтовых ящиков из всех пользователей в организации. Если флажок установлен, будет также поиск всех почтовых ящиков на основе облака для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p113">**All locations** - Select this option to search the mailboxes of all users in your organization. When the checkbox is selected, all cloud-based mailboxes for on-premises users will also be searched.</span></span> 
    
    - <span data-ttu-id="8f85a-p114">**Определенные расположения** — установите этот флажок и выберите команду **Изменить** \> выберите пользователей, групп и группам, для поиска определенных почтовых ящиков. Как объяснялось ранее средство выбора расположения можно найти локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p114">**Specific locations** - Select this option and then click **Modify** \> Choose user, groups, or teams to search specific mailboxes. As previously explained, the locations picker will let you search for on-premises users.</span></span> 
    
5. <span data-ttu-id="8f85a-p115">Сохраните и выполните поиск. Как и другие результаты поиска можно просматривать результаты поиска из облачные почтовые ящики для локальных пользователей. Кроме того, вы можете можно экспортировать в PST-файл результатов поиска (включая все данные команды чата). Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p115">Save and run the search. Any search results from the cloud-based mailboxes for on-premises users can be previewed like any other search results. Additionally, you can you can export the search results (including any Teams chat data) to a PST file. For more information, see:</span></span> 
    
    - [<span data-ttu-id="8f85a-163">Создать новый поиск</span><span class="sxs-lookup"><span data-stu-id="8f85a-163">Create a new search</span></span>](content-search.md#create-a-new-search)
    
    - [<span data-ttu-id="8f85a-164">Просмотр результатов поиска</span><span class="sxs-lookup"><span data-stu-id="8f85a-164">Preview search results</span></span>](content-search.md#preview-search-results)
    
    - [<span data-ttu-id="8f85a-165">Экспорт результатов поиска контента из безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8f85a-165">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
## <a name="using-powershell-to-search-for-teams-chat-data-in-cloud-based-mailboxes-for-on-premises-users"></a><span data-ttu-id="8f85a-166">Использование PowerShell для поиска групп данные чата в облачные почтовые ящики для локальных пользователей</span><span class="sxs-lookup"><span data-stu-id="8f85a-166">Using PowerShell to search for Teams chat data in cloud-based mailboxes for on-premises users</span></span>

<span data-ttu-id="8f85a-p116">Можно использовать командлеты **New-ComplianceSearch** и **Set-ComplianceSearch** безопасности Office 365 &amp; PowerShell центр соответствия требованиям для поиска облачного почтового ящика для локальных пользователей. Как объяснялось ранее не требуется отправить запрос поддержки на использование PowerShell для поиска данных чата группами для локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p116">You can use the **New-ComplianceSearch** and **Set-ComplianceSearch** cmdlets in the Office 365 Security &amp; Compliance Center PowerShell to search the cloud-based mailbox for on-premises users. As previously explained, you don't have to submit a support request to use PowerShell to search for Teams chat data for on-premises users.</span></span> 
  
1. <span data-ttu-id="8f85a-169">[Подключение к Office 365: безопасность &amp; PowerShell центре соответствия требованиям](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="8f85a-169">[Connect to Office 365 Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
    
2. <span data-ttu-id="8f85a-170">Запустите PowerShell следующую команду, чтобы создать новое содержимое выполняет поиск облачные почтовые ящики пользователей в локальной.</span><span class="sxs-lookup"><span data-stu-id="8f85a-170">Run the following PowerShell command to create a new content searches the cloud-based mailboxes of on-premises users.</span></span>
    
    ```
    New-ComplianceSearch <name of new search> -ContentMatchQuery <search query> -ExchangeLocation <on-premises user> -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```
   
    <span data-ttu-id="8f85a-p117">Параметр *IncludeUserAppContent* используется для указания облачного почтового ящика для одного или нескольких пользователей, у которых указан с помощью параметра *ExchangeLocation* . *AllowNotFoundExchangeLocationsEnabled* позволяет облачные почтовые ящики для локальных пользователей. При использовании `$true` значение для этого параметра поиска не пытается проверить существование почтового ящика, перед выполнением. Это требуется для поиска облачные почтовые ящики для локальных пользователей, так как эти типы почтовых ящиков не решения как обычных почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p117">The  *IncludeUserAppContent*  parameter is used to specify the cloud-based mailbox for the user or users who are specified by the  *ExchangeLocation*  parameter. The  *AllowNotFoundExchangeLocationsEnabled*  allows cloud-based mailboxes for on-premises users. When you use the `$true` value for this parameter, the search doesn't try to validate the existence of the mailbox before it runs. This is required to search the cloud-based mailboxes for on-premises users because these types of mailboxes don't resolve as regular mailboxes.</span></span> 
    
    <span data-ttu-id="8f85a-175">Следующий пример выполняет для групп обсуждения (которые являются мгновенные сообщения), которые содержат ключевое слово «redstone» в облачного почтового ящика для пользователя Валентины Дэвис, который является локального пользователя в организации Contoso.</span><span class="sxs-lookup"><span data-stu-id="8f85a-175">The following example searches for Teams chats (which are instant messages) that contain keyword "redstone" in the cloud-based mailbox of Sara Davis, who is an on-premises user in the Contoso organization.</span></span>
  
    ```
    New-ComplianceSearch "Redstone_Search" -ContentMatchQuery "redstone AND kind:im" -ExchangeLocation sarad@contoso.com -IncludeUserAppContent $true -AllowNotFoundExchangeLocationsEnabled $true  
    ```

   <span data-ttu-id="8f85a-176">После создания нового поиска, убедитесь, что командлет **Start-ComplianceSearch** используется для запуска поиска.</span><span class="sxs-lookup"><span data-stu-id="8f85a-176">After you create a new search, be sure to use the **Start-ComplianceSearch** cmdlet to run the search.</span></span> 
  
<span data-ttu-id="8f85a-177">Дополнительные сведения об использовании этих командлетов см.</span><span class="sxs-lookup"><span data-stu-id="8f85a-177">For more information using these cmdlets, see:</span></span>
  
- [<span data-ttu-id="8f85a-178">New-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="8f85a-178">New-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/new-compliancesearch)
    
- [<span data-ttu-id="8f85a-179">Set-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="8f85a-179">Set-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/set-compliancesearch)
    
- [<span data-ttu-id="8f85a-180">Start-ComplianceSearch</span><span class="sxs-lookup"><span data-stu-id="8f85a-180">Start-ComplianceSearch</span></span>](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-content-search/start-compliancesearch)
    

## <a name="known-issues"></a><span data-ttu-id="8f85a-181">Известные проблемы</span><span class="sxs-lookup"><span data-stu-id="8f85a-181">Known issues</span></span>

- <span data-ttu-id="8f85a-p118">На данный момент можно только для поиска, просмотра и экспорта контента в облачные почтовые ящики для локальных пользователей. Включение для почтового ящика на основе облака для локального пользователя на удержание, связанные с eDiscovery case или ее назначения политики хранения к Office 365 не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p118">Currently, you can only search, preview, and export content in cloud-based mailboxes for on-premises users. Placing a cloud-based mailbox for an on-premises user on a hold associated with an eDiscovery case or assigning it to an Office 365 retention policy is not supported.</span></span> 
    
- <span data-ttu-id="8f85a-p119">Средство выбора расположение содержимого для обнаружения электронных данных содержит отображает локальных пользователей и будет позволяют выбирать их. Тем не менее как ранее описано, удержание не будет применяться для локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p119">The content location picker for eDiscovery holds displays on-premises users and will let you select them. However, as previously explained the hold will not be applied to the on-premises user.</span></span>
    
## <a name="frequently-asked-questions"></a><span data-ttu-id="8f85a-186">Вопросы и ответы</span><span class="sxs-lookup"><span data-stu-id="8f85a-186">Frequently asked questions</span></span>

 <span data-ttu-id="8f85a-187">**Где находятся облачные почтовые ящики для локальных пользователей**</span><span class="sxs-lookup"><span data-stu-id="8f85a-187">**Where are cloud-based mailboxes for on-premises users located?**</span></span>
  
<span data-ttu-id="8f85a-188">Облачные почтовые ящики, которые хранятся в одном центре данных как организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="8f85a-188">Cloud-based mailboxes are created and stored in the same datacenter as your Office 365 organization.</span></span> 
  
 <span data-ttu-id="8f85a-189">**Существуют ли другие требования, отличный от отправки запроса поддержки?**</span><span class="sxs-lookup"><span data-stu-id="8f85a-189">**Are there any other requirements other than submitting a support request?**</span></span>
  
 <span data-ttu-id="8f85a-p120">Как объяснялось ранее удостоверения пользователей с почтовыми ящиками prem должны быть синхронизированы для вашей облачной организации, чтобы для каждой учетной записи пользователя в локальной в Office 365 создается соответствующая учетная запись пользователя почты. Кроме того, ваша организация должна иметь корпоративной подписки Office 365, такие как Office 365 корпоративный E1, E3 или E5 подписки.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p120">As previously explained, the identities of users with on-prem mailboxes must be synchronized to your cloud-based organization so that a corresponding mail user account is created for each on-premises user account in Office 365. Additionally, your organization must have an Office 365 enterprise subscription, such as an Office 365 Enterprise E1, E3, or E5 subscription.</span></span> 
  
 <span data-ttu-id="8f85a-192">**Существует ли риск утраты данных чата групп при миграции пользователя локального почтового ящика в облако?**</span><span class="sxs-lookup"><span data-stu-id="8f85a-192">**Is there a risk of losing the Teams chat data if the user's on-premises mailbox is migrated to the cloud?**</span></span>
  
<span data-ttu-id="8f85a-p121">Нет. При переходе в облако основной почтовый ящик пользователя с локальных данных чата групп для этого пользователя будут перенесены в их новой облачной основной почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p121">No. When you migrate the primary mailbox of an on-premises user to the cloud, the Teams chat data for that user will be migrated to their new cloud-based primary mailbox.</span></span>
  
 <span data-ttu-id="8f85a-195">**Можно ли применять удержание электронных данных и политики хранения Office 365 для локальных пользователей?**</span><span class="sxs-lookup"><span data-stu-id="8f85a-195">**Can I apply an eDiscovery hold or Office 365 retention policies to on-premises users?**</span></span>
  
<span data-ttu-id="8f85a-196">Нет.</span><span class="sxs-lookup"><span data-stu-id="8f85a-196">No.</span></span>
  
 <span data-ttu-id="8f85a-197">**Можно найти поиска контента старых групп обсуждений для локальных пользователей до времени Моя организация отправившего запрос для включения этой функции?**</span><span class="sxs-lookup"><span data-stu-id="8f85a-197">**Can Content Search find older Teams chats for on-premises users before the time my organization submitted the request to enable this feature?**</span></span>
  
<span data-ttu-id="8f85a-p122">Microsoft работы, хранение данных чата группами для локальных пользователей на 31 января 2018. Таким образом Если удостоверение пользователя с локальной группы было синхронизировано между Active Directory и Azure Active Directory с этой даты, данные чата их группами, будет храниться в облачные почтовые и будет доступен для поиска с помощью поиска контента. Корпорация Майкрософт также работает на хранение данных чата группами до 31 января 2018 облачные почтовые ящики для локальных пользователей. Дополнительные сведения об этом скоро будет доступен.</span><span class="sxs-lookup"><span data-stu-id="8f85a-p122">Microsoft started storing the Teams chat data for on-premises users on January 31, 2018. So, if the identity of an on-premises Teams user has been synched between Active Directory and Azure Active Directory since this date, then their Teams chat data will be stored in a cloud-based mailbox and will be searchable using Content Search. Microsoft is also working on storing Teams chat data from prior to January 31, 2018 in the cloud-based mailboxes for on-premises users. More information about this will be available soon.</span></span>
