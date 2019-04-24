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
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 14f90b29cbff9c1a588b816563178039c7af7da6
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243417"
---
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="5647e-102">Создание поискового запроса для сбора данных</span><span class="sxs-lookup"><span data-stu-id="5647e-102">Create a search to collect data</span></span>

<span data-ttu-id="5647e-103">На вкладке **поиски** можно создать новый поиск, нажав кнопку **Новый поиск** и следуя инструкциям мастера.</span><span class="sxs-lookup"><span data-stu-id="5647e-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="5647e-104">Назвать Поиск и присвоить описание</span><span class="sxs-lookup"><span data-stu-id="5647e-104">Name your search and give description</span></span>

<span data-ttu-id="5647e-105">Каждый Поиск с обращением должен иметь уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="5647e-105">Each search with a case should have a unique name.</span></span> <span data-ttu-id="5647e-106">При необходимости можно ввести описание поиска.</span><span class="sxs-lookup"><span data-stu-id="5647e-106">You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="5647e-107">Определение условий</span><span class="sxs-lookup"><span data-stu-id="5647e-107">Define your conditions</span></span>

<span data-ttu-id="5647e-108">Вы можете определить условия поиска с помощью встроенных карточек условий или с помощью языка запросов по ключевым словам (KQL).</span><span class="sxs-lookup"><span data-stu-id="5647e-108">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL).</span></span> <span data-ttu-id="5647e-109">Более подробную информацию можно узнать в статье [Создание поисковых запросов](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="5647e-109">For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="5647e-110">Выбор custodians для поиска</span><span class="sxs-lookup"><span data-stu-id="5647e-110">Choose the custodians to search from</span></span>

<span data-ttu-id="5647e-111">Определив условия, необходимо выбрать расположения, в которых будет выполняться поиск.</span><span class="sxs-lookup"><span data-stu-id="5647e-111">Once you have defined your conditions, you need to choose which locations you want to search.</span></span> <span data-ttu-id="5647e-112">Один из способов сделать это — указать, какие custodians вы уже добавили в тот случай, когда вы хотите выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="5647e-112">One way to do it is by specifying which custodians you have already added to the case you want to search.</span></span> <span data-ttu-id="5647e-113">Выбрав хранитель, вы будете выполнять поиск по всем источникам данных, сопоставленным с хранитель.</span><span class="sxs-lookup"><span data-stu-id="5647e-113">By selecting a custodian, you will run the search against all data sources mapped to the custodian.</span></span> <span data-ttu-id="5647e-114">Для получения дополнительных сведений о том, как добавить custodians к своему случаю и управлять их источниками данных, ознакомьтесь со статьей [Working with custodians](managing-custodians.md) .</span><span class="sxs-lookup"><span data-stu-id="5647e-114">See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="5647e-115">Выбор расположений, не являющихся кустодиалми</span><span class="sxs-lookup"><span data-stu-id="5647e-115">Choose non-custodial locations</span></span>

<span data-ttu-id="5647e-116">В некоторых случаях может потребоваться поиск в источниках данных, которые не сопоставлены с хранитель.</span><span class="sxs-lookup"><span data-stu-id="5647e-116">In some cases, you may wish to search data sources that are not mapped to a custodian.</span></span> <span data-ttu-id="5647e-117">В этом случае можно указать расположения, в которых требуется выполнить поиск, или выбрать поиск по всем расположениям для определенной службы Office 365 (например, поиск по всем почтовым ящикам Exchange или всем сайтам SharePoint и OneDrive для бизнеса).</span><span class="sxs-lookup"><span data-stu-id="5647e-117">In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>