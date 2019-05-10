---
title: Поддерживаемые типы файлов в Advanced eDiscovery
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
ms.openlocfilehash: 378bd9ae88269d6a6d15a672473550e50179f772
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834938"
---
# <a name="supported-file-types-in-advanced-ediscovery"></a>Поддерживаемые типы файлов в Advanced eDiscovery

Расширенное обнаружение электронных данных поддерживает множество типов файлов и поддерживает их на различных уровнях, описанных в следующей таблице. Этот список еще не завершен, и мы добавим новые типы файлов, когда мы продолжим проверочное тестирование. В таблице также указано, можно ли просматривать тип файла в доступных средствах просмотра в Advanced eDiscovery.

| Тип MIME | Описание | Встроенное средство просмотра | Средство просмотра текста | Средство просмотра примечаний | Извлечение контейнера | Расширения |
| :- | :- | :- | :- | :- | :- | :- |
| приложение/мбокс | Архив/контейнер |  |  |  | Да | . мбокс |
| application/msword | Производительность труда | Да | Да | Да |  | . doc;. dat |
| application/pdf | Производительность труда | Да | Да | Да |  | PDF |
| приложение/RTF | Document | Да | Да | Да |  | RTF;. гостей |
| Application/ВНД. МС-ексцел | Производительность труда | Да | Да | Да |  | XLS; dat |
| Application/ВНД. МС-ексцел. sheet. binary. макроенаблед. 12 | Производительность труда | Да | Да | Нет |  | . xlsb |
| Application/ВНД. МС-ексцел. sheet. макроенаблед. 12 | Производительность труда | Да | Да | Да |  | . xlsm |
| Application/ВНД. МС-ексцел. Template. макроенаблед. 12 | Производительность труда | Нет | Да | Нет |  | . xltm |
| Application/ВНД. МС-Аутлук | Совместная работа | Да | Да | Да |  | . MSG |
| Application/ВНД. МС-Аутлук-ПСТ | Архив/контейнер |  |  |  | Да | PST-файл |
| Application/ВНД. МС-поверпоинт | Производительность труда | Да | Да | Да |  | PPT; PPS;. Pot |
| Application/ВНД. МС-Ворд. Document. макроенаблед. 12 | Производительность труда | Да | Да | Да |  | DOCM |
| Application/ВНД. МС-Ворд. Template. макроенаблед. 12 | Производительность труда | Да | Да | Да |  | . dotm |
| Application/ВНД. Oasis. OpenDocument. Text | Производительность труда | Да | Да | Да |  | Detection  |
| application/vnd.openxmlformats-officedocument.presentationml.presentation | Производительность труда | Да | Да | Да |  | PPTX |
| Application/ВНД. опенксмлформатс-оффицедокумент. PresentationML. показ слайдов | Производительность труда | Да | Да | Да |  | . ppsx |
| Application/ВНД. опенксмлформатс-оффицедокумент. PresentationML. Template | Производительность труда | Да | Да | Да |  | . potx |
| application/vnd.openxmlformats-officedocument.spreadsheetml.sheet | Производительность труда | Да | Да | Да |  | XLSX |
| Application/ВНД. опенксмлформатс-оффицедокумент. SpreadsheetML. Template | Производительность труда | Да | Да | Да |  | . xltx |
| application/vnd.openxmlformats-officedocument.wordprocessingml.document | Производительность труда | Да | Да | Да |  | DOCX |
| Application/ВНД. опенксмлформатс-оффицедокумент. WordprocessingML. Template | Производительность труда | Да | Да | Да |  | . dotx |
| Application/ВНД. Visio | Производительность труда | Да | Да | Да |  | . VSD |
| приложение/x-7z-сжатый | Архив/контейнер |  |  |  | Да | .7z |
| приложение/XHTML + XML | Document | Да | Да | Да |  | . XHTML |
| Application/XML | Document | Да | Да | Да |  | . XML |
| приложение/x-Msaccess | Производительность труда | Да | Да | Да |  | . mdb |
| Application/x-мспублишер | Производительность труда | Да | Да | Да |  | . pub |
| приложение/x-сжатый архив RAR | Архив/контейнер |  |  |  | Да | . rar |
| приложение/x-tar | Архив/контейнер |  |  |  | Да | . tar |
| приложение/ZIP-индекс | Архив/контейнер |  |  |  | Да | ZIP- |
| Image/BMP | Изображение | Да | Да | Да |  | BMP |
| Image/EMF | Изображение | Да | Да | Да |  | EMF |
| image/gif | Изображение | Да | Да | Да |  | GIF |
| image/jpeg | Изображение | Да | Да | Да |  | JPG;. JPEG;. dat;. жпгт |
| image/png | Изображение | Да | Да | Да |  | PNG |
| Image/TIFF | Изображение | Да | Да | Да |  | TIF |
| Image/ВНД. DWG | Рисования | Да | Да | Да |  | . DWG;. DXF |
| Image/WMF | Document | Да | Да | Да |  | . WMF |
| message/rfc822 | Совместная работа | Да | Да | Да |  | EML |
| Text/CSV | Document | Да | Да | Да |  | CSV-файл |
| Text/HTML | Document | Да | Да | Да |  | . HTML;. shtml; htm |
| text/plain | Document | Да | Да | Да |  | . txt;. CSS;. Con;. pl;. csv;. dat |
| текст/vCard-Contact | Совместная работа | Да | Да | Да |  | . vcf |
||||||||
