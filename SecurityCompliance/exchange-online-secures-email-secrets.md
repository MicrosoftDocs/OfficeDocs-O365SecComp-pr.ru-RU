---
title: Как Exchange Online защищает секреты вашей электронной почты
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/24/2018
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 989ba10c-f73f-4efb-ad1b-af3322e5f376
ms.collection:
- M365-security-compliance
description: Помимо центра управления безопасностью Office 365, который предоставляет сведения о безопасности, конфиденциальности и совместимости для Office 365, вы можете узнать, как Office 365 помогает защитить секреты, предоставляемые в центрах обработки данных. Мы используем технологию, именуемую диспетчером распределенных ключей (DKM).
ms.openlocfilehash: 609d59b6e4da779e0fa663b40fdbf26036753669
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154591"
---
# <a name="how-exchange-online-secures-your-email-secrets"></a><span data-ttu-id="2c4fa-104">Как Exchange Online защищает секреты вашей электронной почты</span><span class="sxs-lookup"><span data-stu-id="2c4fa-104">How Exchange Online secures your email secrets</span></span>

<span data-ttu-id="2c4fa-105">В этой статье описывается, как корпорация Майкрософт защищает вашу электронную почту в своих центрах обработки данных.</span><span class="sxs-lookup"><span data-stu-id="2c4fa-105">This article describes how Microsoft secures your email secrets in its datacenters.</span></span>
  
## <a name="how-do-we-secure-secret-information-provided-by-you"></a><span data-ttu-id="2c4fa-106">Как мы защищаем секретные сведения, предоставленные вами?</span><span class="sxs-lookup"><span data-stu-id="2c4fa-106">How do we secure secret information provided by you?</span></span>

<span data-ttu-id="2c4fa-107">Помимо центра управления безопасностью Office 365, который предоставляет [сведения о безопасности, конфиденциальности и совместимости для office 365](https://go.microsoft.com/fwlink/?linkid=874644), вы можете узнать, как Office 365 помогает защитить секреты, предоставляемые в центрах обработки данных.</span><span class="sxs-lookup"><span data-stu-id="2c4fa-107">In addition to the Office 365 Trust Center which provides [Security, Privacy and Compliance Information for Office 365](https://go.microsoft.com/fwlink/?linkid=874644), you might want to know how Office 365 helps protects secrets you provide in its datacenters.</span></span> <span data-ttu-id="2c4fa-108">Мы используем технологию, именуемую диспетчером распределенных ключей (DKM).</span><span class="sxs-lookup"><span data-stu-id="2c4fa-108">We use a technology called Distributed Key Manager (DKM).</span></span>
  
<span data-ttu-id="2c4fa-p103">Распределенный диспетчер ключей (DKM) — это клиентский компонент, который использует набор секретных ключей для шифрования и расшифровки информации. Только члены определенной группы безопасности в доменных службах Active Directory могут получать доступ к этим ключам для расшифровки данных, зашифрованных DKM. В Exchange Online только некоторые учетные записи служб, под которыми выполняются процессы Exchange, входят в эту группу безопасности. В рамках стандартной процедуры в центре обработки данных ни один человек не получает учетные данные, включенные в эту группу безопасности, и поэтому ни один человек не получает доступ к ключам, которые могут расшифровать эти секреты.</span><span class="sxs-lookup"><span data-stu-id="2c4fa-p103">Distributed Key Manager (DKM) is a client-side functionality that uses a set of secret keys to encrypt and decrypt information. Only members of a specific security group in Active Directory Domain Services can access those keys in order to decrypt the data that is encrypted by DKM. In Exchange Online, only certain service accounts under which the Exchange processes run are part of that security group. As part of standard operating procedure in the datacenter, no human is given credentials that are part of this security group and therefore no human has access to the keys that can decrypt these secrets.</span></span>
  
<span data-ttu-id="2c4fa-p104">Для отладки, устранения неполадок и аудита администратор центра обработки данных должен запросить повышенные права доступа для получения временных учетных данных, которые входят в группу безопасности. Для этого процесса требуется несколько уровней юридического утверждения. Если доступ предоставлен, все действия заносятся в журнал и проходят аудиторскую проверку. Кроме того, доступ предоставляется только в течение заданного интервала, после чего он автоматически отключается.</span><span class="sxs-lookup"><span data-stu-id="2c4fa-p104">For debugging, troubleshooting, or auditing purposes, a datacenter administrator must request elevated access to gain temporary credentials that are part of the security group. This process requires multiple levels of legal approval. If access is granted, all activity is logged and audited. In addition access is only granted for a set interval of time after which it automatically expires.</span></span>
  
<span data-ttu-id="2c4fa-117">Для дополнительной защиты технология DKM использует автоматический откат и архивацию ключей.</span><span class="sxs-lookup"><span data-stu-id="2c4fa-117">For extra protection, DKM technology includes automated key rollover and archiving.</span></span> <span data-ttu-id="2c4fa-118">Это также гарантирует, что вы сможете получить доступ к старому контенту, не используя все время один и тот же ключ.</span><span class="sxs-lookup"><span data-stu-id="2c4fa-118">This also ensures that you can continue to access your older content without having to rely on the same key indefinitely.</span></span>
  
## <a name="where-does-exchange-online-make-use-of-dkm"></a><span data-ttu-id="2c4fa-119">Где Exchange Online использует DKM?</span><span class="sxs-lookup"><span data-stu-id="2c4fa-119">Where does Exchange Online make use of DKM?</span></span>

<span data-ttu-id="2c4fa-p106">Корпорация Майкрософт использует DKM, чтобы шифровать секретные данные в центрах обработки данных Exchange Online. Например:</span><span class="sxs-lookup"><span data-stu-id="2c4fa-p106">Microsoft uses DKM to encrypt your secrets in Exchange Online datacenters. For example:</span></span>
  
- <span data-ttu-id="2c4fa-p107">Учетные данные для подключенных учетных записей электронной почты. Подключенные учетные записи — это сторонние учетные записи, такие как Hotmail, Yahoo! и Gmail.</span><span class="sxs-lookup"><span data-stu-id="2c4fa-p107">Email account credentials for connected accounts. Connected accounts are third-party accounts such as Hotmail, Gmail, and Yahoo! mail accounts.</span></span>
    
- <span data-ttu-id="2c4fa-125">Корневые ключи службы управления правами (RMS).</span><span class="sxs-lookup"><span data-stu-id="2c4fa-125">Rights Management service (RMS) root keys.</span></span> <span data-ttu-id="2c4fa-126">Это ключи клиентов, которые импортируются из Azure RMS или из локальных развертываний службы управления правами доменных служб Active Directory клиента, которые используются для шифрования и расшифровки электронных сообщений с помощью RMS или Microsoft 365 Message encryption (OME).</span><span class="sxs-lookup"><span data-stu-id="2c4fa-126">These are customer keys that are either imported from Azure RMS or from customer's on-premises Active Directory Domain Services RMS deployments that are used for encrypting and decrypting emails with RMS or Office 365 Message Encryption (OME).</span></span>
    
## <a name="related-topics"></a><span data-ttu-id="2c4fa-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2c4fa-127">Related topics</span></span>

[<span data-ttu-id="2c4fa-128">Шифрование в Office 365</span><span class="sxs-lookup"><span data-stu-id="2c4fa-128">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="2c4fa-129">Техническая справка по шифрованию в Office 365</span><span class="sxs-lookup"><span data-stu-id="2c4fa-129">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="2c4fa-130">Гарантия обслуживания в центре безопасности &amp; Office 365</span><span class="sxs-lookup"><span data-stu-id="2c4fa-130">Service assurance in the Office 365 Security &amp; Compliance Center</span></span>](https://go.microsoft.com/fwlink/?linkid=874645)
  

