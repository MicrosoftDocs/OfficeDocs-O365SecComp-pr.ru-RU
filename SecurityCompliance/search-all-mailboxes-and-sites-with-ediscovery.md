---
title: Поиск по всем почтовых ящикам и сайтам с помощью центра обнаружения электронных данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 56e2978f-71b6-4141-b769-ad856d31bbec
description: В центре обнаружения электронных данных в Office 365 можно выполнить поиск всех почтовых ящиков Exchange Online, сайты SharePoint Online и OneDrive для бизнеса сайтов в поиск одного обнаружения электронных данных. Чтобы выполнить поиск всех источников контента в организации, диспетчер обнаружения электронных данных должны быть назначены разрешения соответствующие обнаружения электронных данных для каждого источника контента.
ms.openlocfilehash: 5612faf6113ceef292f90b49ec70ad7b30905646
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038102"
---
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a><span data-ttu-id="333cf-104">Поиск по всем почтовых ящикам и сайтам с помощью центра обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="333cf-104">Search all mailboxes and sites using the eDiscovery Center</span></span>

<span data-ttu-id="333cf-p102">В центре обнаружения электронных данных в Office 365 можно выполнить поиск всех почтовых ящиков Exchange Online, сайты SharePoint Online и OneDrive для бизнеса сайтов в поиск одного обнаружения электронных данных. Чтобы выполнить поиск всех источников контента в организации, диспетчер обнаружения электронных данных должны быть назначены разрешения соответствующие обнаружения электронных данных для каждого источника контента.</span><span class="sxs-lookup"><span data-stu-id="333cf-p102">In the eDiscovery Center in Office 365, you can search all Exchange Online mailboxes, SharePoint Online sites, and OneDrive for Business sites in a single eDiscovery search. To search all content sources in the organization, an eDiscovery manager must be assigned the appropriate eDiscovery permissions for each content source.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="333cf-107">Приступая к работе</span><span class="sxs-lookup"><span data-stu-id="333cf-107">Before you begin</span></span>

- <span data-ttu-id="333cf-p103">Диспетчеру обнаружения электронных данных должны быть назначены соответствующие разрешения на поиск по источнику содержимого. Дополнительные сведения о назначении разрешений на обнаружение электронных данных в почтовых ящиках и на сайтах см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="333cf-p103">An eDiscovery manager must be assigned the appropriate permissions to search a content source. For more information about assigning eDiscovery permissions to mailboxes and sites, see the following:</span></span> 
    
  - [<span data-ttu-id="333cf-110">Назначение разрешений обнаружения электронных данных в Exchange</span><span class="sxs-lookup"><span data-stu-id="333cf-110">Assign eDiscovery permissions in Exchange</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [<span data-ttu-id="333cf-111">Назначение разрешений обнаружения электронных данных в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="333cf-111">Assign eDiscovery permissions in SharePoint Online</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [<span data-ttu-id="333cf-112">Назначение разрешений на обнаружение электронных данных для сайтов OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="333cf-112">Assign eDiscovery permissions to OneDrive for Business sites</span></span>](assign-permissions-to-onedrive-for-business-sites.md)
    
- <span data-ttu-id="333cf-p104">Можно выполнить поиск не более 10 000 почтовых ящиков и неограниченное число SharePoint Online и OneDrive для бизнеса сайтов в запросе поиска одного обнаружения электронных данных. Тем не менее если указать определенных сайтов для поиска, ограничение составляет 100 сайтов.</span><span class="sxs-lookup"><span data-stu-id="333cf-p104">You can search a maximum of 10,000 mailboxes and an unlimited number of SharePoint Online and OneDrive for Business sites in a single eDiscovery search query. However, if you specify the specific sites to search, the limit is 100 sites.</span></span>
    
- <span data-ttu-id="333cf-115">В разделе [Дополнительные сведения](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) Описание ограничений при просмотре результатов при поиске всех почтовых ящиков и сайтов.</span><span class="sxs-lookup"><span data-stu-id="333cf-115">See the [More information](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) section for a description of the limits when viewing the results when searching all mailboxes and sites.</span></span> 
    
- <span data-ttu-id="333cf-116">Дополнительные сведения о создании запросов поиска в центре eDiscovery см [запросов выполнения обнаружения электронных данных](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span><span class="sxs-lookup"><span data-stu-id="333cf-116">For more information about creating search queries in the eDiscovery Center, see [Create and run eDiscovery queries](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span></span>
    
## <a name="search-all-locations"></a><span data-ttu-id="333cf-117">Поиск по всем расположениям</span><span class="sxs-lookup"><span data-stu-id="333cf-117">Search all locations</span></span>

1. <span data-ttu-id="333cf-118">В центре обнаружения электронных данных откройте дело eDiscovery, по которому нужно выполнить поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="333cf-118">In the eDiscovery Center, open the eDiscovery case that you want to run the search query for.</span></span>
    
2. <span data-ttu-id="333cf-119">В разделе **Поиск и экспорт**нажмите кнопку существующего запроса или щелкните **новый элемент** , чтобы создать новый запрос поиска.</span><span class="sxs-lookup"><span data-stu-id="333cf-119">Under **Search and Export**, click an existing query or click **New item** to create a new search query.</span></span> 
    
3. <span data-ttu-id="333cf-120">На странице поискового запроса, в разделе **Источники**, выберите **Изменение области запроса**.</span><span class="sxs-lookup"><span data-stu-id="333cf-120">On the search query page, in the **Sources** section, click **Modify Query Scope**.</span></span>
    
4. <span data-ttu-id="333cf-121">На странице **Изменение области запроса** выберите **Искать везде**, а затем — нужные расположения контента.</span><span class="sxs-lookup"><span data-stu-id="333cf-121">On the **Modify Query Scope** page, click **Search everything**, and select the content locations to search.</span></span>
    
  - <span data-ttu-id="333cf-122">Выбор **Exchange** для поиска всех почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="333cf-122">Select **Exchange** to search all mailboxes.</span></span> 
    
  - <span data-ttu-id="333cf-123">Выберите **SharePoint** , чтобы найти все SharePoint Online и OneDrive для бизнеса сайтов.</span><span class="sxs-lookup"><span data-stu-id="333cf-123">Select **SharePoint** to search all SharePoint Online and OneDrive for Business sites.</span></span> 
    
  - <span data-ttu-id="333cf-124">Выберите **Exchange** и **SharePoint** , чтобы найти все расположения контента в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="333cf-124">Select both **Exchange** and **SharePoint** to search all content locations in your organization.</span></span> 
    
![Поиск по всем почтовым ящикам и сайтам](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. <span data-ttu-id="333cf-126">Нажмите кнопку **OK**, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="333cf-126">Click **OK** to save the changes.</span></span> 
    
6. <span data-ttu-id="333cf-p105">Укажите или измените другие сведения на странице поискового запроса (например, использование ключевых слов, диапазона дат или выбор определенных типов содержимого). Когда вы будете готовы выполнить запрос, нажмите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="333cf-p105">Complete or revise other information on the search query page, such as the keyword query, the date range, or narrowing the specific types of content to search for. When you're ready to run the query, click **Search**.</span></span> 
    
## <a name="more-information"></a><span data-ttu-id="333cf-129">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="333cf-129">More information</span></span>
<span data-ttu-id="333cf-130"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="333cf-130"></span></span>

- <span data-ttu-id="333cf-131">Первые 500 почтовых ящиков и первые 500 сайтов с наибольшим количеством результатов перечислены в разделе **Источники** на странице **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="333cf-131">The top 500 mailboxes and the top 500 sites with the most results are listed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="333cf-132">Общее количество элементов, найденных во всех источниках контента, и их общий размер отображаются в разделе **Источники** на странице **Запрос**. 
</span><span class="sxs-lookup"><span data-stu-id="333cf-132">The total number of items found in all content sources and their combined total size are displayed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="333cf-133">Вы можете предварительно просмотреть последние 200 результатов поиска, которые находятся в почтовых ящиках Exchange или на сайтах SharePoint на странице **Запрос**.</span><span class="sxs-lookup"><span data-stu-id="333cf-133">You can preview the 200 most recent search results located in Exchange mailboxes or SharePoint sites on the **Query** page.</span></span> 
    
    <span data-ttu-id="333cf-134">На снимке экрана ниже показан пример результатов поиска, отображаемых на странице **Запрос** при поиске по всем почтовым ящикам и сайтам.</span><span class="sxs-lookup"><span data-stu-id="333cf-134">The following screenshot shows an example of the search results displayed on the **Query** page when you search all mailboxes and sites.</span></span> 
    
    ![Снимок экрана с результатами поиска во всех расположениях](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  

