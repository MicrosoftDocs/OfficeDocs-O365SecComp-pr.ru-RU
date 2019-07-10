---
title: Обнаружение вирусов в SharePoint Online
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 01/14/2019
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
ms.collection:
- M365-security-compliance
description: Office 365 помогает защитить рабочую среду от вредоносных программ, обнаруживая вирусы в файлах, которые пользователи отправляют в SharePoint Online. Файлы проверяются на наличие вирусов после отправки. Если вирус заражен, для него задается соответствующее свойство, которое не позволяет пользователям скачать его из браузера или синхронизировать.
ms.openlocfilehash: 8b15ac8e82082c2c6d940986d2018fa559835146
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598345"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="6f1ff-105">Обнаружение вирусов в SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6f1ff-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="6f1ff-p102">Office 365 помогает защитить рабочую среду от вредоносных программ, обнаруживая вирусы в файлах, которые пользователи отправляют в SharePoint Online. Файлы проверяются на наличие вирусов после отправки. Если вирус заражен, для него задается соответствующее свойство, которое не позволяет пользователям скачать его из браузера или синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6f1ff-p103">[!Важно!] Эти антивирусные функции в SharePoint Online лишь помогают сдержать распространение вирусов. Они не должны быть единственным средством защиты от вредоносных программ в вашей среде. Мы рекомендуем всем клиентам развертывать средства антивирусной защиты на разных уровнях и пользоваться лучшими методиками обеспечения безопасности корпоративной инфраструктуры. Дополнительные сведения о стратегиях и рекомендациях см. в статье [Security best practices for Office 365](security-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="6f1ff-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="6f1ff-113">Что происходит при отправке зараженного файла в SharePoint Online?</span><span class="sxs-lookup"><span data-stu-id="6f1ff-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="6f1ff-114">Office 365 использует стандартный модуль обнаружения вирусов.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-114">Office 365 uses a common virus detection engine.</span></span> <span data-ttu-id="6f1ff-115">Ядро работает асинхронно в SharePoint Online и сканирует файлы после их отправки.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-115">The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded.</span></span> <span data-ttu-id="6f1ff-116">Если выясняется, что файл содержит вирус, он помечается, чтобы его нельзя было снова скачать.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-116">When a file is found to contain a virus, it's flagged so that it can't be downloaded again.</span></span> <span data-ttu-id="6f1ff-117">В апреле 2018 был удален лимит в 25 МБ для сканированных файлов.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-117">In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="6f1ff-118">Ниже вкратце описано, что происходит.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="6f1ff-119">Пользователь отправляет файл в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="6f1ff-120">Модуль поиска вирусов проверяет файл.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="6f1ff-121">Если обнаруживается вирус, антивирусный модуль устанавливает для файла свойство, которое обозначает, что он заражен.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="6f1ff-122">Что происходит, когда пользователь пытается скачать зараженный файл через браузер?</span><span class="sxs-lookup"><span data-stu-id="6f1ff-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="6f1ff-123">Если файл заражен вирусом, пользователь не может скачать его из SharePoint Online с помощью браузера.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="6f1ff-124">Ниже вкратце описано, что происходит.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="6f1ff-125">Пользователь открывает веб-браузер и пытается скачать зараженный файл из SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="6f1ff-126">Пользователю выдается предупреждение о том, что вирус обнаружен.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-126">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="6f1ff-127">Пользователю предоставляется возможность загрузить файл и попытаться очистить его с помощью собственного антивирусного программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-127">The user is given the option to download the file and attempt to clean it using their own virus software.</span></span>

> [!NOTE]
> <span data-ttu-id="6f1ff-128">Командлет Set – SPOTenant можно использовать с параметром **дисалловинфектедфиледовнлоад** , чтобы запретить пользователям скачивать обнаруженный файл даже в окне предупреждения о защите от вирусов.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-128">You can use the Set-SPOTenant cmdlet with the **DisallowInfectedFileDownload** parameter to not allow users to download a detected file, even in the anti-virus warning window.</span></span> <span data-ttu-id="6f1ff-129">См. раздел [Дисалловинфектедфиледовнлоадhttps://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant)] (.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-129">See [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="6f1ff-130">Что происходит, когда клиент синхронизации OneDrive пытается синхронизировать зараженный файл?</span><span class="sxs-lookup"><span data-stu-id="6f1ff-130">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="6f1ff-p107">Неважно, какой клиент вы используете  новый клиент синхронизации OneDrive (OneDrive.exe) или старый клиент синхронизации OneDrive для бизнеса(Groove.exe),  если файл содержит вирус, он не будет скачан. Клиент выведет уведомление о том, что файл невозможно синхронизировать.</span><span class="sxs-lookup"><span data-stu-id="6f1ff-p107">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

