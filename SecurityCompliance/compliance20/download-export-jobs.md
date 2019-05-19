---
title: Скачивание заданий экспорта
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 56ed8eac259974b43ca0cd26b2bd0c339a5fc05b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155151"
---
# <a name="download-export-jobs"></a>Скачивание заданий экспорта

Все экспортированные данные добавляются в большой двоичный объект Microsoft Azure. Это предоставляет несколько вариантов для обработки данных в нисходящем направлении. Существует несколько способов доступа к большому двоичному объекту Azure. Один из способов — использовать Обозреватель хранилищ Azure. Этот метод поддерживает простое подключение, просмотр и скачивание. Для получения дополнительных сведений посетите страницу<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer>

1.  Чтобы скачать контент после завершения задания экспорта, перейдите на вкладку экспорты и выберите задание экспорта.

2.  Скопируйте текст в разделе "расположения" всплывающего меню.

![](../media/eDiscoExportJob.png)

3.  Откройте Обозреватель хранилищ Azure и нажмите кнопку "подключиться"

![](../media/AzureStorageConnect.png)

4.  Выберите "использовать универсальный код ресурса (URI) для подписи общего доступа" и нажмите кнопку Далее.

![](../media/AzureStorageConnect2.png)

5.  Вставьте текст расположения в текстовое поле URI и нажмите кнопку Далее.

![](../media/AzureStorageConnect3.png)

6.  Нажмите кнопку Подключить.

![](../media/AzureStorageConnect4.png)

Это приведет к добавлению экспорта в качестве объекта в учетных записях хранения/контейнерах, вложенных в службы/BLOB-объекты. Вы сможете изучить экспорт и загрузку всех или частей экспорта.

![](../media/AzureStorageConnect5.png)