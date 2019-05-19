---
title: Расширенная индексация данных хранителя
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
ms.openlocfilehash: be163d3272dbe027cb0f4b4b4fe379bf28fa5a85
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151761"
---
# <a name="advanced-indexing-of-custodian-data"></a>Расширенная индексация данных хранителя

Когда хранитель добавляется к расширенному варианту обнаружения электронных данных, любое содержимое в Office 365, которое было признано частичным индексированием, повторно обрабатывается, чтобы сделать его полным поиском.  Этот процесс называется *расширенной индексацией*. Контент может частично индексироваться по ряду причин, в том числе наличия изображений, неподдерживаемых типов файлов или при обнаружении ограничения на размер файлов индексирования.

Дополнительные сведения о поддержке обработки в Office 365 и частично индексированных элементах приведены в следующих статьях:

- [Поддерживаемые типы файлов в Advanced eDiscovery](supported-filetypes-ediscovery20.md)
- [Частично индексированные элементы в средстве "Поиск контента" в Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)
- [Форматы файлов, индексируемые службой поиска Exchange](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)
- [Анализируемые типы файлов и расширения имен файлов для обхода по умолчанию в SharePoint Server](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a>Просмотр результатов расширенного индексирования

После выполнения расширенного процесса индексирования можно получить сведения о эффективности повторной обработки.  В представлении индексирования хранитель на диаграмме перечислены все элементы, добавленные в *гибридный индекс*.  Гибридный индекс — там, где Advanced eDiscovery сохраняет повторно обработанное содержимое.

На диаграмме также представлено количество элементов, для которых требуется исправление, и еще один график ошибок по типам файлов. Дополнительные сведения см. в разделе [Устранение ошибок при обработке данных](error-remediation.md).

## <a name="updating-advanced-indexes-for-custodians"></a>Обновление расширенных индексов для custodians

Когда хранитель добавляется к расширенному варианту обнаружения электронных данных, все частично индексированные элементы обрабатываются повторно. Однако с течением времени в почтовый ящик пользователя или в учетную запись OneDrive можно добавить более частично индексированные элементы.  При необходимости вы можете обновить индексы.

> [!NOTE]
> Обновление индексов хранитель выполняется длительным процессом. Рекомендуется не обновлять индексы более одного раза в день.
