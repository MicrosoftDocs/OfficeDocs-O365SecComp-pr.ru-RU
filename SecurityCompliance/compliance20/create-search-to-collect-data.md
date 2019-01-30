---
title: Создание поискового запроса для сбора данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 3ebb9a40d3fb055fbb88b32175a4a22df3da44af
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608289"
---
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="2e6b9-102">Создание поискового запроса для сбора данных</span><span class="sxs-lookup"><span data-stu-id="2e6b9-102">Create a search to collect data</span></span>

<span data-ttu-id="2e6b9-103">На вкладке **Поиск** в случае можно создать новый поиск, нажав кнопку **Создать поиска** и выполнив мастера.</span><span class="sxs-lookup"><span data-stu-id="2e6b9-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="2e6b9-104">Имя операции поиска и предоставить описание</span><span class="sxs-lookup"><span data-stu-id="2e6b9-104">Name your search and give description</span></span>

<span data-ttu-id="2e6b9-p101">Каждый поиска с дела должны иметь уникальные имена. Можно ввести описание для поиска.</span><span class="sxs-lookup"><span data-stu-id="2e6b9-p101">Each search with a case should have a unique name. You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="2e6b9-107">Определение условия</span><span class="sxs-lookup"><span data-stu-id="2e6b9-107">Define your conditions</span></span>

<span data-ttu-id="2e6b9-p102">Можно определить условия поиска с использованием карт готовые условие или с помощью ключевого слова Query Language (KQL). Для получения дополнительных сведений см [Построение поисковых запросов](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="2e6b9-p102">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL). For more information, see [Building search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="2e6b9-110">Выберите custodians выполнять поиск по</span><span class="sxs-lookup"><span data-stu-id="2e6b9-110">Choose the custodians to search from</span></span>

<span data-ttu-id="2e6b9-p103">После определения всех условий, необходимо выбрать местоположения, в которых требуется выполнить поиск. — Это один из способов сделать это путем указания каких custodians уже добавлен в рамках данного экземпляра, который нужно найти. Можно, выбрав пункт custodian поиска будет выполняться все источники данных, сопоставленные с custodian. [Работа с custodians](managing-custodians.md) более подробные сведения о том, как добавить custodians в случай и управлять их источники данных.</span><span class="sxs-lookup"><span data-stu-id="2e6b9-p103">Once you have defined your conditions, you need to choose which locations you want to search. One way to do it is by specifying which custodians you have already added to the case you want to search. By selecting a custodian, you will run the search against all data sources mapped to the custodian. See [Working with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="2e6b9-115">Выберите не наказание расположения</span><span class="sxs-lookup"><span data-stu-id="2e6b9-115">Choose non-custodial locations</span></span>

<span data-ttu-id="2e6b9-p104">В некоторых случаях вы можете выполнять поиск источников данных, которые не связан с custodian. В этом случае можно указать место, нужно выполнить поиск, или выберите Поиск все расположения контента для определенной службы Office 365 (например поиск всех почтовых ящиков Exchange или все SharePoint и OneDrive для бизнеса сайтов).</span><span class="sxs-lookup"><span data-stu-id="2e6b9-p104">In some cases, you may wish to search data sources that are not mapped to a custodian. In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>