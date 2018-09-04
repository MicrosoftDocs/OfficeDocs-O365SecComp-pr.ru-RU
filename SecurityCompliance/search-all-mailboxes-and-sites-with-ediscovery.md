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
search.appverid:
- MET150
ms.assetid: 56e2978f-71b6-4141-b769-ad856d31bbec
description: В центре обнаружения электронных данных в Office 365 можно выполнить поиск всех почтовых ящиков Exchange Online, сайты SharePoint Online и OneDrive для бизнеса сайтов в поиск одного обнаружения электронных данных. Чтобы выполнить поиск всех источников контента в организации, диспетчер обнаружения электронных данных должны быть назначены разрешения соответствующие обнаружения электронных данных для каждого источника контента.
ms.openlocfilehash: b3508d5929ca2b5b7a937eb2dccf677a2968cbbc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534688"
---
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a>Поиск по всем почтовых ящикам и сайтам с помощью центра обнаружения электронных данных

В центре обнаружения электронных данных в Office 365 можно выполнить поиск всех почтовых ящиков Exchange Online, сайты SharePoint Online и OneDrive для бизнеса сайтов в поиск одного обнаружения электронных данных. Чтобы выполнить поиск всех источников контента в организации, диспетчер обнаружения электронных данных должны быть назначены разрешения соответствующие обнаружения электронных данных для каждого источника контента. 
  
## <a name="before-you-begin"></a>Приступая к работе

- Диспетчеру обнаружения электронных данных должны быть назначены соответствующие разрешения на поиск по источнику содержимого. Дополнительные сведения о назначении разрешений на обнаружение электронных данных в почтовых ящиках и на сайтах см. в следующих статьях: 
    
  - [Назначение разрешений обнаружения электронных данных в Exchange](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [Назначение разрешений обнаружения электронных данных в SharePoint Online](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [Назначение разрешений на обнаружение электронных данных для сайтов OneDrive для бизнеса](assign-permissions-to-onedrive-for-business-sites.md)
    
- Можно выполнить поиск не более 10 000 почтовых ящиков и неограниченное число SharePoint Online и OneDrive для бизнеса сайтов в запросе поиска одного обнаружения электронных данных. Тем не менее если указать определенных сайтов для поиска, ограничение составляет 100 сайтов.
    
- В разделе [Дополнительные сведения](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) Описание ограничений при просмотре результатов при поиске всех почтовых ящиков и сайтов. 
    
- Дополнительные сведения о создании запросов поиска в центре eDiscovery см [запросов выполнения обнаружения электронных данных](https://go.microsoft.com/fwlink/p/?LinkID=404032).
    
## <a name="search-all-locations"></a>Поиск по всем расположениям

1. В центре обнаружения электронных данных откройте дело eDiscovery, по которому нужно выполнить поисковый запрос.
    
2. В разделе **Поиск и экспорт**нажмите кнопку существующего запроса или щелкните **новый элемент** , чтобы создать новый запрос поиска. 
    
3. На странице поискового запроса, в разделе **Источники**, выберите **Изменение области запроса**.
    
4. На странице **Изменение области запроса** выберите **Искать везде**, а затем — нужные расположения контента.
    
  - Выбор **Exchange** для поиска всех почтовых ящиков. 
    
  - Выберите **SharePoint** , чтобы найти все SharePoint Online и OneDrive для бизнеса сайтов. 
    
  - Выберите **Exchange** и **SharePoint** , чтобы найти все расположения контента в вашей организации. 
    
![Поиск по всем почтовым ящикам и сайтам](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. Нажмите кнопку **OK**, чтобы сохранить изменения. 
    
6. Укажите или измените другие сведения на странице поискового запроса (например, использование ключевых слов, диапазона дат или выбор определенных типов содержимого). Когда вы будете готовы выполнить запрос, нажмите кнопку **Поиск**. 
    
## <a name="more-information"></a>Дополнительные сведения
<a name="moreinfo"> </a>

- Первые 500 почтовых ящиков и первые 500 сайтов с наибольшим количеством результатов перечислены в разделе **Источники** на странице **Запрос**. 
    
- Общее количество элементов, найденных во всех источниках контента, и их общий размер отображаются в разделе **Источники** на странице **Запрос**. 
 
    
- Вы можете предварительно просмотреть последние 200 результатов поиска, которые находятся в почтовых ящиках Exchange или на сайтах SharePoint на странице **Запрос**. 
    
    На снимке экрана ниже показан пример результатов поиска, отображаемых на странице **Запрос** при поиске по всем почтовым ящикам и сайтам. 
    
    ![Снимок экрана с результатами поиска во всех расположениях](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  
