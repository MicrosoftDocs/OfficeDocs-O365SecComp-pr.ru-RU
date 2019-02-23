---
title: Создание поискового запроса для сбора данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 09af09c4a538bb43fed5fce044eb1be60c235aaa
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212649"
---
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="c0fe1-102">Создание поискового запроса для сбора данных</span><span class="sxs-lookup"><span data-stu-id="c0fe1-102">Create a search to collect data</span></span>

<span data-ttu-id="c0fe1-103">На вкладке **поиски** можно создать новый поиск, нажав кнопку **Новый поиск** и следуя инструкциям мастера.</span><span class="sxs-lookup"><span data-stu-id="c0fe1-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="c0fe1-104">Назвать Поиск и присвоить описание</span><span class="sxs-lookup"><span data-stu-id="c0fe1-104">Name your search and give description</span></span>

<span data-ttu-id="c0fe1-p101">Каждый Поиск с обращением должен иметь уникальное имя. При необходимости можно ввести описание поиска.</span><span class="sxs-lookup"><span data-stu-id="c0fe1-p101">Each search with a case should have a unique name. You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="c0fe1-107">Определение условий</span><span class="sxs-lookup"><span data-stu-id="c0fe1-107">Define your conditions</span></span>

<span data-ttu-id="c0fe1-p102">Вы можете определить условия поиска с помощью встроенных карточек условий или с помощью языка запросов по ключевым словам (KQL). Более подробную информацию можно узнать в статье [Создание поисковых запросов](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="c0fe1-p102">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL). For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="c0fe1-110">Выбор custodians для поиска</span><span class="sxs-lookup"><span data-stu-id="c0fe1-110">Choose the custodians to search from</span></span>

<span data-ttu-id="c0fe1-p103">Определив условия, необходимо выбрать расположения, в которых будет выполняться поиск. Один из способов сделать это — указать, какие custodians вы уже добавили в тот случай, когда вы хотите выполнить поиск. Выбрав хранитель, вы будете выполнять поиск по всем источникам данных, сопоставленным с хранитель. Для получения дополнительных сведений о том, как добавить custodians к своему случаю и управлять их источниками данных, ознакомьтесь со статьей [Working with custodians](managing-custodians.md) .</span><span class="sxs-lookup"><span data-stu-id="c0fe1-p103">Once you have defined your conditions, you need to choose which locations you want to search. One way to do it is by specifying which custodians you have already added to the case you want to search. By selecting a custodian, you will run the search against all data sources mapped to the custodian. See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="c0fe1-115">Выбор расположений, не являющихся кустодиалми</span><span class="sxs-lookup"><span data-stu-id="c0fe1-115">Choose non-custodial locations</span></span>

<span data-ttu-id="c0fe1-p104">В некоторых случаях может потребоваться поиск в источниках данных, которые не сопоставлены с хранитель. В этом случае можно указать расположения, в которых требуется выполнить поиск, или выбрать поиск по всем расположениям для определенной службы Office 365 (например, поиск по всем почтовым ящикам Exchange или всем сайтам SharePoint и OneDrive для бизнеса).</span><span class="sxs-lookup"><span data-stu-id="c0fe1-p104">In some cases, you may wish to search data sources that are not mapped to a custodian. In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>