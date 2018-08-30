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
# <a name="set-up-virtual-certificate-collection-to-validate-smime"></a><span data-ttu-id="d5515-103">Настройка коллекции виртуальных сертификатов для проверки S/MIME</span><span class="sxs-lookup"><span data-stu-id="d5515-103">Set up virtual certificate collection to validate S/MIME</span></span>

<span data-ttu-id="d5515-p101">Администратору клиента потребуется настроить коллекцию виртуальных сертификатов, которая будет использоваться для проверки сертификатов S/MIME. Эта коллекция виртуальных сертификатов настраивается как тип файла хранилища сертификатов с расширением имени файла SST. SST-файл содержит все корневые и промежуточные сертификаты, которые используются при проверке сертификата S/MIME.</span><span class="sxs-lookup"><span data-stu-id="d5515-p101">As a tenant administrator you will need to configure a virtual certificate collection that will be used to validate S/MIME certificates. This virtual certificate collection is set up as a certificate store file type with an SST filename extension. The SST file contains all the root and intermediate certificates that are used when validating an S/MIME certificate.</span></span>
  
## <a name="create-and-save-an-sst"></a><span data-ttu-id="d5515-107">Создание и сохранение SST-файла</span><span class="sxs-lookup"><span data-stu-id="d5515-107">Create and save an SST</span></span>
<span data-ttu-id="d5515-108"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="d5515-108"></span></span>

<span data-ttu-id="d5515-p102">Для выполнения этой процедуры можно использовать только командную консоль. Сведения о том, как открыть командную консоль Exchange в локальной организации Exchange, см. в статье **Open the Shell**. Сведения о том, как с помощью Оболочка Windows PowerShell подключаться к Exchange Online, см. в статье [Подключение к PowerShell для Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="d5515-p102">You can only use the Shell to perform this procedure. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
<span data-ttu-id="d5515-p103">Администратор может создать этот SST-файл, экспортировав сертификаты с доверенного компьютера с помощью командлета  `Export-Certificate` и указав тип SST. Дополнительные сведения о командлете  `Export-Certificate` см. в справочной статье [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5515-p103">As an administrator, you can create this SST file by exporting the certificates from a trusted machine using the  `Export-Certificate` cmdlet and specifying the type as SST. For more information the  `Export-Certificate` cmdlet, see the [Export-Certificate](https://technet.microsoft.com/en-us/library/hh848628.aspx) reference topic.</span></span> 
  
<span data-ttu-id="d5515-p104">После создания SST-файла используйте командлет  `Set-Smimeconfig`, чтобы сохранить его в хранилище виртуальных сертификатов с использованием параметра  _-SMIMECertificateIssuingCA_. Например:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span><span class="sxs-lookup"><span data-stu-id="d5515-p104">Once the SST file is generated, use the  `Set-Smimeconfig` cmdlet to save it in the virtual certificate store by using the  _-SMIMECertificateIssuingCA_ parameter. For example:  `Set-SmimeConfig -SMIMECertificateIssuingCA (Get-Content filename.sst -Encoding Byte)`</span></span>
  
## <a name="ensuring-a-certificate-is-valid"></a><span data-ttu-id="d5515-116">Проверка действительности сертификата</span><span class="sxs-lookup"><span data-stu-id="d5515-116">Ensuring a certificate is valid</span></span>
<span data-ttu-id="d5515-117"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="d5515-117"></span></span>

<span data-ttu-id="d5515-p105">Exchange 2013 с пакетом обновления 1 (SP1) сначала проверяет SST-файл, а затем — сертификат. При неудачной проверке сертификат будет проверен путем поиска в хранилище сертификатов на локальном компьютере. Это поведение — нововведение в Exchange 2013 с пакетом обновления 1 (SP1), которое отличается от предыдущих версий Exchange. В Exchange Online для проверки используется только SST.</span><span class="sxs-lookup"><span data-stu-id="d5515-p105">Exchange 2013 SP1 first checks for the SST file and validates the certificate. If the validation fails, it will look at the local machine certificate store to validate the certificate. This behavior is new for Exchange 2013 SP1 and different from prior versions of Exchange. In Exchange Online only the SST will be used for validation.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="d5515-122">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d5515-122">More Information</span></span>
<span data-ttu-id="d5515-123"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="d5515-123"></span></span>

[<span data-ttu-id="d5515-124">S/MIME для подписи и шифрования сообщений</span><span class="sxs-lookup"><span data-stu-id="d5515-124">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  
[<span data-ttu-id="d5515-125">Get-SmimeConfig</span><span class="sxs-lookup"><span data-stu-id="d5515-125">Get-SmimeConfig</span></span>](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx)
  

