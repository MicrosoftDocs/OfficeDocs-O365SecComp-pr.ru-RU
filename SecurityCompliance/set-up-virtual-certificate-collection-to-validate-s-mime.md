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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260727"
---
# <a name="set-up-virtual-certificate-collection-in-exchange-online-to-validate-smime"></a><span data-ttu-id="518f7-103">Настройка коллекции виртуальных сертификатов в Exchange Online для проверки S/MIME</span><span class="sxs-lookup"><span data-stu-id="518f7-103">Set up virtual certificate collection in Exchange Online to validate S/MIME</span></span>

<span data-ttu-id="518f7-104">В качестве администратора вам потребуется настроить виртуальную коллекцию сертификатов в Exchange Online, которая будет использоваться для проверки сертификатов S/MIME.</span><span class="sxs-lookup"><span data-stu-id="518f7-104">As an admin, you will need to configure a virtual certificate collection in Exchange Online that will be used to validate S/MIME certificates.</span></span> <span data-ttu-id="518f7-105">Эта коллекция виртуальных сертификатов настроена как хранилище сертификатов с расширением имени файла SST.</span><span class="sxs-lookup"><span data-stu-id="518f7-105">This virtual certificate collection is set up as a certificate store with an SST filename extension.</span></span> <span data-ttu-id="518f7-106">SST-файл содержит все корневые и промежуточные сертификаты, которые используются при проверке сертификата S/MIME.</span><span class="sxs-lookup"><span data-stu-id="518f7-106">The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>

## <a name="create-and-save-an-sst"></a><span data-ttu-id="518f7-107">Создание и сохранение SST-файла</span><span class="sxs-lookup"><span data-stu-id="518f7-107">Create and save an SST</span></span>

<span data-ttu-id="518f7-108">Вы можете создать SST файл хранилища сертификатов, экспортировав сертификаты с доверенного компьютера, используя командлет **Export/Certificate** в Windows PowerShell, и указав _тип_ значения SST.</span><span class="sxs-lookup"><span data-stu-id="518f7-108">You can create this SST certificate store file by exporting the certificates from a trusted machine using the **Export-Certificate** cmdlet in Windows PowerShell and specifying the _Type_ value as SST.</span></span> <span data-ttu-id="518f7-109">Инструкции можно найти в разделе [Export/Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span><span class="sxs-lookup"><span data-stu-id="518f7-109">For instructions, see [Export-Certificate](https://docs.microsoft.com/powershell/module/pkiclient/export-certificate).</span></span>

<span data-ttu-id="518f7-110">Когда у вас будет файл хранилища сертификатов SST, используйте следующий синтаксис в Exchange Online PowerShell, чтобы сохранить содержимое SST-файла в виртуальном хранилище сертификатов Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="518f7-110">Once you have the SST certificate store file, use the following syntax in Exchange Online PowerShell to save the SST file contents in the Exchange Online virtual certificate store.</span></span> <span data-ttu-id="518f7-111">Сведения о подключении к Exchange Online PowerShell см. в статье [Подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="518f7-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content <FileNameAndPath>.sst -Encoding Byte)
```

<span data-ttu-id="518f7-112">В этом примере импортируется SST файл с параметром Documents\exported Rules Certificate Store. SST. SST.</span><span class="sxs-lookup"><span data-stu-id="518f7-112">This example imports the SST file C:\My Documents\Exported Certificate Store.sst.</span></span>

```
Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content "C:\My Documents\Exported Certificate Store.sst" -Encoding Byte)
```

<span data-ttu-id="518f7-113">Подробные сведения о синтаксисе и параметрах можно найти в статье [Set – SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).</span><span class="sxs-lookup"><span data-stu-id="518f7-113">For detailed syntax and parameter information, see [Set-SmimeConfig](https://docs.microsoft.com/en-us/powershell/module/exchange/encryption-and-certificates/set-smimeconfig).</span></span>

## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="518f7-114">Проверка действительности сертификата</span><span class="sxs-lookup"><span data-stu-id="518f7-114">Ensuring a certificate is valid</span></span>

<span data-ttu-id="518f7-115">В Exchange Online для проверки сертификата используется только SST.</span><span class="sxs-lookup"><span data-stu-id="518f7-115">In Exchange Online, only the SST is used for certificate validation.</span></span>

## <a name="more-information"></a><span data-ttu-id="518f7-116">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="518f7-116">More Information</span></span>

[<span data-ttu-id="518f7-117">S/MIME для подписи и шифрования сообщений</span><span class="sxs-lookup"><span data-stu-id="518f7-117">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)

[<span data-ttu-id="518f7-118">Get — SmimeConfig</span><span class="sxs-lookup"><span data-stu-id="518f7-118">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
