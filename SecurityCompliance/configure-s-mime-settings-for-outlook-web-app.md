---
title: Настройка параметров S/MIME для Outlook Web App
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/8/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
description: Как администратор организации Exchange 2013 и Exchange Online можно настроить Outlook Web App, чтобы разрешить отправки и получения сообщений S/MIME-защищенного. Командлет SMIMEConfig используется для управления этой функции через интерфейс командной консоли Exchange.
ms.openlocfilehash: e4bbf6cb8b0e2976b856045fc8a474bc2aa2a55a
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002520"
---
# <a name="configure-smime-settings-for-outlook-web-app"></a><span data-ttu-id="4955b-104">Настройка параметров S/MIME для Outlook Web App</span><span class="sxs-lookup"><span data-stu-id="4955b-104">Configure S/MIME settings for Outlook Web App</span></span>

<span data-ttu-id="4955b-p102">Администратор организации для Exchange 2013 и Exchange Online может настроить Outlook Web App так, чтобы разрешить отправку и получение сообщений с защитой S/MIME. Для управления этой функцией в интерфейсе командной консоли Exchange используйте командлет  `SMIMEConfig`.</span><span class="sxs-lookup"><span data-stu-id="4955b-p102">As an organization administrator for both Exchange 2013 and Exchange Online, you can set up Outlook Web App to allow sending and receiving S/MIME-protected messages. Use the  `SMIMEConfig` cmdlet to manage this feature through the Exchange Management Shell interface.</span></span> 
  
<span data-ttu-id="4955b-107">Подробное описание параметров и примеры для  `get-SMIMEConfig` и  `set-SMIMEConfig` смотрите в документации к [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) и [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).</span><span class="sxs-lookup"><span data-stu-id="4955b-107">For more information such as a detailed description of parameters and examples for  `get-SMIMEConfig` and  `set-SMIMEConfig`, see the [Get-SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) and [Set-SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx) documentation.</span></span> 
  
<span data-ttu-id="4955b-p103">Для выполнения этой процедуры можно использовать только командную консоль. Сведения о том, как открыть командную консоль Exchange в локальной организации Exchange, см. в статье **Open the Shell**. Сведения о том, как с помощью Оболочка Windows PowerShell подключаться к Exchange Online, см. в статье [Подключение к PowerShell для Exchange Online](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="4955b-p103">You can only use the Shell to perform this procedure. To learn how to open the Exchange Management Shell in your on-premises Exchange organization, see **Open the Shell**. To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="4955b-111">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="4955b-111">For more information</span></span>

[<span data-ttu-id="4955b-112">S/MIME для подписи и шифрования сообщений</span><span class="sxs-lookup"><span data-stu-id="4955b-112">S/MIME for message signing and encryption</span></span>](s-mime-for-message-signing-and-encryption.md)
  

