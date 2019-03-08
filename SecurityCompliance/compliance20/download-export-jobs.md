---
title: Скачивание заданий экспорта
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
ms.openlocfilehash: 904bc5f8a6d6cef937d55336e8f383957713769a
ms.sourcegitcommit: 9f38ba72eba0b656e507860ca228726e4199f7ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/07/2019
ms.locfileid: "30475699"
---
# <a name="download-export-jobs"></a><span data-ttu-id="6c81a-102">Скачивание заданий экспорта</span><span class="sxs-lookup"><span data-stu-id="6c81a-102">Download export jobs</span></span>

<span data-ttu-id="6c81a-103">Все экспортированные данные добавляются в большой двоичный объект Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6c81a-103">All exported data is added to a Microsoft Azure blob.</span></span> <span data-ttu-id="6c81a-104">Это предоставляет несколько вариантов для обработки данных в нисходящем направлении.</span><span class="sxs-lookup"><span data-stu-id="6c81a-104">This provides multiple options to handle the data downstream.</span></span> <span data-ttu-id="6c81a-105">Существует несколько способов доступа к большому двоичному объекту Azure.</span><span class="sxs-lookup"><span data-stu-id="6c81a-105">There are several ways to access an Azure blob.</span></span> <span data-ttu-id="6c81a-106">Один из способов — использовать Обозреватель хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="6c81a-106">One method is to use Azure Storage Explorer.</span></span> <span data-ttu-id="6c81a-107">Этот метод поддерживает простое подключение, просмотр и скачивание.</span><span class="sxs-lookup"><span data-stu-id="6c81a-107">This method supports simple connection, browsing and downloading.</span></span> <span data-ttu-id="6c81a-108">Для получения дополнительных сведений посетите страницу<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span><span class="sxs-lookup"><span data-stu-id="6c81a-108">For more information, visit <https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span></span>

1.  <span data-ttu-id="6c81a-109">Чтобы скачать контент после завершения задания экспорта, перейдите на вкладку экспорты и выберите задание экспорта.</span><span class="sxs-lookup"><span data-stu-id="6c81a-109">To download content after an export job is complete, go to the Exports tab and select an export job.</span></span>

2.  <span data-ttu-id="6c81a-110">Скопируйте текст в разделе "расположения" всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="6c81a-110">Copy the text in the “Locations” section of the flyout.</span></span>

![](../media/eDiscoExportJob.png)

3.  <span data-ttu-id="6c81a-111">Откройте Обозреватель хранилищ Azure и нажмите кнопку "подключиться"</span><span class="sxs-lookup"><span data-stu-id="6c81a-111">Open Azure Storage Explorer and click the “Connect” button</span></span>

![](../media/AzureStorageConnect.png)

4.  <span data-ttu-id="6c81a-112">Выберите "использовать универсальный код ресурса (URI) для подписи общего доступа" и нажмите кнопку Далее.</span><span class="sxs-lookup"><span data-stu-id="6c81a-112">Select “Use a shared access signature URI” and click next</span></span>

![](../media/AzureStorageConnect2.png)

5.  <span data-ttu-id="6c81a-113">Вставьте текст расположения в текстовое поле URI и нажмите кнопку Далее.</span><span class="sxs-lookup"><span data-stu-id="6c81a-113">Paste the Location text in the URI text box and click next</span></span>

![](../media/AzureStorageConnect3.png)

6.  <span data-ttu-id="6c81a-114">Нажмите кнопку Подключить.</span><span class="sxs-lookup"><span data-stu-id="6c81a-114">Click Connect</span></span>

![](../media/AzureStorageConnect4.png)

<span data-ttu-id="6c81a-115">Это приведет к добавлению экспорта в качестве объекта в учетных записях хранения/контейнерах, вложенных в службы/BLOB-объекты.</span><span class="sxs-lookup"><span data-stu-id="6c81a-115">This will add the export as an object in Storage Accounts/SAS-Attached Services/Blob Containers.</span></span> <span data-ttu-id="6c81a-116">Вы сможете изучить экспорт и загрузку всех или частей экспорта.</span><span class="sxs-lookup"><span data-stu-id="6c81a-116">You will be able to explore the export and download all or portions of the export.</span></span>

![](../media/AzureStorageConnect5.png)