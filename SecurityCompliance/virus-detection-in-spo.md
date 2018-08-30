---
title: Обнаружение вирусов в SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: Office 365 помогает защитить рабочую среду от вредоносных программ, обнаруживая вирусы в файлах, которые пользователи отправляют в SharePoint Online. Файлы проверяются на наличие вирусов после отправки. Если вирус заражен, для него задается соответствующее свойство, которое не позволяет пользователям скачать его из браузера или синхронизировать.
ms.openlocfilehash: 22e983d35283ff96e1469fdf913e25b8d1d1c485
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535103"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="6ad5f-105">Обнаружение вирусов в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6ad5f-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="6ad5f-p102">Office 365 помогает защитить рабочую среду от вредоносных программ, обнаруживая вирусы в файлах, которые пользователи отправляют в SharePoint Online. Файлы проверяются на наличие вирусов после отправки. Если вирус заражен, для него задается соответствующее свойство, которое не позволяет пользователям скачать его из браузера или синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6ad5f-p103">[!Важно!] Эти антивирусные функции в SharePoint Online лишь помогают сдержать распространение вирусов. Они не должны быть единственным средством защиты от вредоносных программ в вашей среде. Мы рекомендуем всем клиентам развертывать средства антивирусной защиты на разных уровнях и пользоваться лучшими методиками обеспечения безопасности корпоративной инфраструктуры. Дополнительные сведения о стратегиях и рекомендациях см. в статье [Security best practices for Office 365](security-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="6ad5f-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="6ad5f-113">Что происходит при отправке зараженного файла в SharePoint Online?</span><span class="sxs-lookup"><span data-stu-id="6ad5f-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="6ad5f-p104">Office 365 использует общие модуля обнаружения вирусов. Модуль выполняется асинхронно в SharePoint Online и сканирует файлы после их передачи. Если файл содержит вирус, она помечена, чтобы он не удается загрузить еще раз. В 2018 апреля были удалены ограничение 25 МБ для поиска файлов.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-p104">Office 365 uses a common virus detection engine. The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded. When a file is found to contain a virus, it's flagged so that it can't be downloaded again. In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="6ad5f-118">Ниже вкратце описано, что происходит.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="6ad5f-119">Пользователь отправляет файл в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="6ad5f-120">Модуль поиска вирусов проверяет файл.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="6ad5f-121">Если обнаруживается вирус, антивирусный модуль устанавливает для файла свойство, которое обозначает, что он заражен.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="6ad5f-122">Что происходит, когда пользователь пытается скачать зараженный файл через браузер?</span><span class="sxs-lookup"><span data-stu-id="6ad5f-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="6ad5f-123">Если файл заражен вирусом, пользователь не может скачать его из SharePoint Online с помощью браузера.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="6ad5f-124">Ниже вкратце описано, что происходит.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="6ad5f-125">Пользователь открывает веб-браузер и пытается скачать зараженный файл из SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="6ad5f-126">Пользователю выводится предупреждение о том, что обнаружен вирус, и предлагается скачать файл и попытаться очистить его, используя собственную антивирусную программу.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-126">The user is given a warning that a virus has been detected, and is given the option to download the file and attempt to clean it using their own virus software.</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="6ad5f-127">Что происходит, когда клиент синхронизации OneDrive пытается синхронизировать зараженный файл?</span><span class="sxs-lookup"><span data-stu-id="6ad5f-127">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="6ad5f-p105">Неважно, какой клиент вы используете  новый клиент синхронизации OneDrive (OneDrive.exe) или старый клиент синхронизации OneDrive для бизнеса(Groove.exe),  если файл содержит вирус, он не будет скачан. Клиент выведет уведомление о том, что файл невозможно синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="6ad5f-p105">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

