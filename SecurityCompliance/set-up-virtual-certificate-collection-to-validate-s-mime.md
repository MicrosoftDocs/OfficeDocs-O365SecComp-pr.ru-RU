---
title: Настройка коллекции виртуальных сертификатов для проверки S/MIME
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 04a616e6-197c-490c-ae8c-c8d5f0f0b3dd
description: s администратор клиента требуется настройка коллекции виртуальных сертификатов, который будет использоваться для проверки сертификатов S/MIME.
ms.openlocfilehash: 88d12b3c1d5f36c58f278cf304237a569a8b92c4
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003038"
---
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a>Настройка коллекции виртуальных сертификатов для проверки S/MIME

Администратору клиента потребуется настроить коллекцию виртуальных сертификатов, которая будет использоваться для проверки сертификатов S/MIME. Эта коллекция виртуальных сертификатов настраивается как тип файла хранилища сертификатов с расширением имени файла SST. SST-файл содержит все корневые и промежуточные сертификаты, которые используются при проверке сертификата S/MIME.
  
## <a name="create-and-save-an-sst"></a>Создание и сохранение SST-файла
<a name="sectionSection0"> </a>

Для выполнения этой процедуры можно использовать только командную консоль. Сведения о том, как открыть командную консоль Exchange в локальной организации Exchange, см. в статье **Open the Shell**. Сведения о том, как с помощью Оболочка Windows PowerShell подключаться к Exchange Online, см. в статье [Подключение к PowerShell для Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).
  
Администратор может создать этот SST-файл, экспортировав сертификаты с доверенного компьютера с помощью командлета  `Export-Certificate` и указав тип SST. Дополнительные сведения о командлете  `Export-Certificate` см. в справочной статье [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx). 
  
После создания SST-файла используйте командлет  `Set-Smimeconfig`, чтобы сохранить его в хранилище виртуальных сертификатов с использованием параметра  _-SMIMECertificateIssuingCA_. Например:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`
  
## <a name="ensuring-a-certificate-is-valid"></a>Проверка действительности сертификата
<a name="sectionSection1"> </a>

Exchange 2013 с пакетом обновления 1 (SP1) сначала проверяет SST-файл, а затем — сертификат. При неудачной проверке сертификат будет проверен путем поиска в хранилище сертификатов на локальном компьютере. Это поведение — нововведение в Exchange 2013 с пакетом обновления 1 (SP1), которое отличается от предыдущих версий Exchange. В Exchange Online для проверки используется только SST.
  
## <a name="more-information"></a>Дополнительные сведения
<a name="sectionSection2"> </a>

[S/MIME для подписи и шифрования сообщений](s-mime-for-message-signing-and-encryption.md)
  
[Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  

