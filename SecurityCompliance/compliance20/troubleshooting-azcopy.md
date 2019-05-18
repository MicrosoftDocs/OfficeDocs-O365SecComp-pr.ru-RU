---
title: Устранение неполадок AzCopy в Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 2c8378cf7b9bd21f901b1babbebdcb0b69a8ed73
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151521"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery"></a>Устранение неполадок AzCopy в Advanced eDiscovery

При загрузке данных или документов, отличных от Office 365, для исправления ошибок в Advanced eDiscovery, Пользовательский интерфейс предоставляет команду Azure AzCopy, содержащую параметры с расположением файлов, которые требуется отправить, и хранилищем Azure. расположение, в которое будут загружаться файлы. Чтобы отправить документы, скопируйте эту команду и запустите ее в командной строке на локальном компьютере.  На снимке экрана ниже показан пример команды AzCopy:

![Отправка файлов, отличных от Office 365](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

В большинстве случаев предоставленная команда будет работать при запуске. Однако возможны случаи, когда отображаемая команда не запустится успешно. Вот несколько возможных причин.

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a>AzCopy не установлен на локальном компьютере, или он не установлен в расположении по умолчанию

Если AzCopy не установлен или он установлен в расположении, отличном от расположения установки по умолчанию ( `%ProgramFiles(x86)%`то есть), при выполнении команды AzCopy может появиться следующее сообщение об ошибке:

    The system cannot find the path specified.

Если AzCopy не установлен на локальном компьютере, можно выполнить установку отсюда (установите его в расположении по умолчанию): [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).


Если AzCopy установлен, но он установлен в расположении, отличном от расположения по умолчанию, можно скопировать команду, вставить ее в текстовый файл, а затем изменить путь к расположению, где фактически устанавливается AzCopy. Например, если Azcopy находится в `%ProgramFiles%`, то вы можете заменить первую часть команды `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` на. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy` После внесения изменений скопируйте его из текстового файла и запустите в командной строки.

> [!TIP]
> Если AzCopy установлен в расположении, отличном от местоположения установки по умолчанию, попробуйте удалить его, а затем повторно установить в расположении по умолчанию. Это позволит избежать этой ситуации в будущем.