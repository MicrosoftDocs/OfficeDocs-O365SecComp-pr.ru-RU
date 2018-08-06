---
title: Синхронизация сертификатов пользователей с Office 365 для S/MIME
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 351c932e-99c1-4512-a6e8-788e90b7838f
description: Чтобы отправлять сообщения, защищенные с помощью S/MIME, необходимо настроить соответствующие сертификаты. Для отправки зашифрованных сообщений через Exchange Online программа электронной почты отправителя использует общедоступный сертификат получателя для шифрования сообщений. Этот общедоступный сертификат X.509 необходимо опубликовать в Office 365.
ms.openlocfilehash: aa94dfa6702a25b3fc6b8b883daceddf31d2f66a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026196"
---
# <a name="sync-user-certificates-to-office-365-for-smime"></a><span data-ttu-id="01dc8-105">Синхронизация сертификатов пользователей с Office 365 для S/MIME</span><span class="sxs-lookup"><span data-stu-id="01dc8-105">Sync user certificates to Office 365 for S/MIME</span></span>

<span data-ttu-id="01dc8-p102">Чтобы отправлять сообщения, защищенные с помощью S/MIME, необходимо настроить соответствующие сертификаты. Для отправки зашифрованных сообщений через Exchange Online программа электронной почты отправителя использует общедоступный сертификат получателя для шифрования сообщений. Этот общедоступный сертификат X.509 необходимо опубликовать в Office 365.</span><span class="sxs-lookup"><span data-stu-id="01dc8-p102">Before anyone can send S/MIME-protected messages, the appropriate certificates must be set up. In order to send encrypted messages through Exchange Online, the sender's email program uses the public certificate of the recipient to encrypt the message. This public X.509 certificate has to be published to Office 365.</span></span>
  
## <a name="to-sync-certificates-that-support-smime"></a><span data-ttu-id="01dc8-109">Синхронизация сертификатов, поддерживающих S/MIME</span><span class="sxs-lookup"><span data-stu-id="01dc8-109">To Sync certificates that support S/MIME</span></span>

<span data-ttu-id="01dc8-p103">Начните настройку S/MIME путем выдачи сертификатов и их публикации в локальной службе домена Active Directory. Дополнительные сведения об управлении сертификатами в Exchange 2013 см. в разделе [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).</span><span class="sxs-lookup"><span data-stu-id="01dc8-p103">Begin setting up S/MIME by issuing certificates and publishing them in your local Active Directory Domain Service. For more information about managing certificates in Exchange 2013, see [Digital Certificates and SSL](http://technet.microsoft.com/library/a9e2e08c-d46a-4135-a387-eb653212b676.aspx).</span></span>
  
<span data-ttu-id="01dc8-p104">После публикации сертификатов используйте Средство синхронизации Azure Active Directory для синхронизации пользовательских данных из локальной среды Exchange с Office 365. Дополнительные сведения об этом процессе см. в статье [DirSync: журнал выпуска версий средства синхронизации каталогов](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span><span class="sxs-lookup"><span data-stu-id="01dc8-p104">After your certificates are published, use the Azure Active Directory Sync tool to synchronize user data from your on-premises Exchange environment to Office 365. For more information on this process, see [DirSync: Directory Sync Tool Version Release History](https://go.microsoft.com/fwlink/p/?LinkId=392587).</span></span>
  
<span data-ttu-id="01dc8-114">Это средство синхронизирует не только данные других каталогов в целях поддержки S/MIME, но и атрибуты  `userCertificate` и  `userSMIMECertificate` для каждого объекта-пользователя, что позволит использовать данные для подписи и шифрования сообщений.</span><span class="sxs-lookup"><span data-stu-id="01dc8-114">Along with synchronizing other directory data, for S/MIME purposes, the tool will synchronize the  `userCertificate` and  `userSMIMECertificate` attributes for each user object so the data can be used to sign and encrypt messages.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="01dc8-115">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="01dc8-115">More Information</span></span>

[<span data-ttu-id="01dc8-116">S/MIME для подписи и шифрования сообщений</span><span class="sxs-lookup"><span data-stu-id="01dc8-116">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  
[<span data-ttu-id="01dc8-117">Средство синхронизации Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="01dc8-117">Azure Active Directory Sync tool</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=392587)
  

