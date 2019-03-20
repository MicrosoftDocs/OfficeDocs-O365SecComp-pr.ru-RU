---
title: Настройка коллекции виртуальных сертификатов в Exchange Online для проверки S/MIME
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: Администраторы могут узнать, как создать коллекцию виртуальных сертификатов, которая будет использоваться для проверки сертификатов S/MIME в Exchange Online.
ms.openlocfilehash: 15998bce1971952286d8dd4401a92f1e9e47c25d
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693558"
---
# <a name="set-up-virtual-certificate-collection-in-exchange-online-to-validate-smime"></a>Настройка коллекции виртуальных сертификатов в Exchange Online для проверки S/MIME

В качестве администратора вам потребуется настроить виртуальную коллекцию сертификатов в Exchange Online, которая будет использоваться для проверки сертификатов S/MIME. Эта коллекция виртуальных сертификатов настроена как хранилище сертификатов с расширением имени файла SST. SST-файл содержит все корневые и промежуточные сертификаты, которые используются при проверке сертификата S/MIME.

## <a name="create-and-save-an-sst"></a>Создание и сохранение SST-файла

Вы можете создать SST файл хранилища сертификатов, экспортировав сертификаты с доверенного компьютера, используя командлет **Export/Certificate** в Windows PowerShell, и указав _тип_ значения SST. Инструкции можно найти в разделе [Export/Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).

Когда у вас будет файл хранилища сертификатов SST, используйте следующий синтаксис в Exchange Online PowerShell, чтобы сохранить содержимое SST-файла в виртуальном хранилище сертификатов Exchange Online. Чтобы подключиться к Exchange Online PowerShell, ознакомьтесь [со статьЕй подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content <FileNameAndPath>.sst -Encoding Byte)
```

В этом примере импортируется SST файл с параметром Documents\exported Rules Certificate Store. SST. SST.

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content "C:\My Documents\Exported Certificate Store.sst" -Encoding Byte)
```

Подробные сведения о синтаксисе и параметрах можно найти в статье [Set – SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).

## <a name="ensuring-a-certificate-is-valid"></a>Проверка действительности сертификата

В Exchange Online для проверки сертификата используется только SST.

## <a name="more-information"></a>Дополнительные сведения

[S/MIME для подписи и шифрования сообщений](s-mime-for-message-signing-and-encryption.md)

[Get — SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
