---
title: Поддерживаемые типы файлов в Advanced eDiscovery (Предварительная версия)
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
ms.openlocfilehash: 7955debee750019d60b8016d736ba50f1ff70bce
ms.sourcegitcommit: cf9d9b545a7c153d314aa9c08c7fb16fcd785b3e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/21/2019
ms.locfileid: "30737709"
---
# <a name="supported-file-types-in-advanced-ediscovery-preview"></a>Поддерживаемые типы файлов в Advanced eDiscovery (Предварительная версия)

Расширенное обнаружение электронных данных (Preview) поддерживает множество типов файлов на различных уровнях, описанных в следующей таблице. Этот список не завершен, и мы добавим новые типы файлов, когда мы продолжим проверочное тестирование. В таблице также указано, можно ли просматривать тип файла в доступных средствах просмотра в авансовом электронных данных (Предварительная версия).

| Тип MIME | Класс File | Встроенное средство просмотра | Средство просмотра текста | Средство просмотра примечаний | Извлечение контейнера | Расширения |
| :- | :- | :- | :- | :- | :- | :- |
| application/msword | Document | Да | Да | Да | Нет | . doc;. dat |
| application/pdf | Document | Да | Да | Да | Нет | PDF |
| приложение/RTF | Document | Да | Да | Да | Нет | RTF;. гостей |
| Application/ВНД. МС-ексцел | Document | Да | Да | Да | Нет | XLS; dat |
| Application/ВНД. МС-ексцел. sheet. binary. макроенаблед. 12 | Производительность и формат открытого документа | Да | Да | Нет | Нет | . xlsb |
| Application/ВНД. МС-ексцел. sheet. макроенаблед. 12 | Document | Да | Да | Да | Нет | . xlsm |
| Application/ВНД. МС-ексцел. Template. макроенаблед. 12 | Производительность и формат открытого документа | Нет | Да | Нет | Нет | . xltm |
| Application/ВНД. МС-Аутлук | Производительность труда | Нет | Нет | Нет | Нет | . MSG |
| Application/ВНД. МС-Аутлук-ПСТ | Производительность и совместная работа | Нет | Нет | Нет | Да | PST-файл |
| Application/ВНД. МС-поверпоинт | Document | Да | Да | Да | Нет | PPT; PPS;. Pot |
| Application/ВНД. МС-Ворд. Document. макроенаблед. 12 | Document | Да | Да | Да | Нет | DOCM |
| Application/ВНД. МС-Ворд. Template. макроенаблед. 12 | Document | Да | Да | Да | Нет | . dotm |
| Application/ВНД. Oasis. OpenDocument. Text | Document | Да | Да | Да | Нет | Detection  |
| application/vnd.openxmlformats-officedocument.presentationml.presentation | Document | Да | Да | Да | Нет | PPTX |
| Application/ВНД. опенксмлформатс-оффицедокумент. PresentationML. показ слайдов | Производительность и формат открытого документа | Да | Да | Да | Нет | . ppsx |
| Application/ВНД. опенксмлформатс-оффицедокумент. PresentationML. Template | Document | Да | Да | Да | Нет | . potx |
| application/vnd.openxmlformats-officedocument.spreadsheetml.sheet | Document | Да | Да | Да | Нет | XLSX |
| Application/ВНД. опенксмлформатс-оффицедокумент. SpreadsheetML. Template | Document | Да | Да | Да | Нет | . xltx |
| application/vnd.openxmlformats-officedocument.wordprocessingml.document | Document | Да | Да | Да | Нет | DOCX |
| Application/ВНД. опенксмлформатс-оффицедокумент. WordprocessingML. Template | Document | Да | Да | Да | Нет | . dotx |
| Application/ВНД. Visio | Document | Да | Да | Да | Нет | . VSD |
| приложение/x-7z-сжатый | Архив/контейнер | Нет | Нет | Нет | Да | .7z |
| приложение/XHTML + XML | Document | Да | Да | Да | Нет | . XHTML |
| Application/XML | Document | Да | Да | Да | Нет | . XML |
| приложение/x-Msaccess | Document | Да | Да | Да | Нет | . mdb |
| Application/x-мспублишер | Document | Да | Да | Да | Нет | . pub |
| приложение/x-сжатый архив RAR | Архив/контейнер | Нет | Нет | Нет | Да | . rar |
| приложение/ZIP-индекс | Архив/контейнер | Нет | Нет | Нет | Да | ZIP- |
| Image/BMP | Изображение | Да | Да | Да | Нет | BMP |
| Image/EMF | Изображение | Да | Да | Да | Нет | EMF |
| image/gif | Document | Да | Да | Да | Нет | . gif |
| image/jpeg | Изображение | Да | Да | Да | Нет | JPG;. JPEG;. dat;. жпгт |
| image/png | Изображение | Да | Да | Да | Нет | . png |
| Image/TIFF | Изображение | Да | Да | Да | Нет | TIF |
| Image/ВНД. DWG | Document | Да | Да | Да | Нет | . DWG;. DXF |
| Image/WMF | Document | Да | Да | Да | Нет | . WMF |
| message/rfc822 | Производительность и совместная работа | Нет | Нет | Нет | Нет | EML |
| Text/CSV | Document | Да | Да | Да | Нет | CSV-файл |
| Text/HTML | Document | Да | Да | Да | Нет | . HTML;. shtml; htm |
| text/plain | Document | Да | Да | Да | Нет | . txt;. CSS;. Con;. pl;. csv;. dat |
| текст/vCard-Contact | Document | Да | Да | Да | Нет | . vcf |
||||||||