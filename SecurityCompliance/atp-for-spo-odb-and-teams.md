---
title: Office 365 ATP для SharePoint, OneDrive и Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 11/08/2018
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
ms.collection:
- M365-security-compliance
description: Расширьте Office 365 Advanced Threat protection to Files in SharePoint Online, OneDrive для бизнеса и Microsoft Teams, чтобы обеспечить более безопасную совместную работу для вашей организации.
ms.openlocfilehash: d9d99041d002a6c43d7b6918f53aabb93f82339a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220609"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="f2ca8-103">Office 365 ATP для SharePoint, OneDrive и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f2ca8-103">Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

## <a name="overview-of-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="f2ca8-104">Обзор Office 365 ATP для SharePoint, OneDrive и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f2ca8-104">Overview of Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="f2ca8-p101">Пользователи регулярно совместно используют файлы и совместно работают с помощью SharePoint, OneDrive и Microsoft Teams. В [Office 365 Advanced Threat protection](office-365-atp.md) (ATP) ваша организация может быть более безопасной совместной работой. ATP позволяет обнаруживать и блокировать файлы, которые определены как вредоносные на сайтах групп и библиотеках документов.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p101">People regularly share files and collaborate using SharePoint, OneDrive, and Microsoft Teams. With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can collaborate in a safer manner. ATP helps detect and block files that are identified as malicious in team sites and document libraries.</span></span>  
  
## <a name="how-it-works"></a><span data-ttu-id="f2ca8-108">Как это работает</span><span class="sxs-lookup"><span data-stu-id="f2ca8-108">How it works</span></span>

<span data-ttu-id="f2ca8-p102">Когда файл в SharePoint Online, OneDrive для бизнеса и Microsoft Teams определен как вредоносный, ATP напрямую интегрируется с хранилищами файлов для блокировки этого файла. На следующем рисунке показан пример вредоносного файла, обнаруженного в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p102">When a file in SharePoint Online, OneDrive for Business, and Microsoft Teams has been identified as malicious, ATP directly integrates with the file stores to lock that file. The following image shows an example of a malicious file detected in a library.</span></span>
  
<span data-ttu-id="f2ca8-111">[![Файлы в OneDrive для бизнеса с одной обнаруженной вредоносной службой](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="f2ca8-111">[![Files in OneDrive for Business with one detected as malicious](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="f2ca8-p103">Несмотря на то, что заблокированный файл по-прежнему отображается в библиотеке документов и в веб-приложениях, на мобильных или для настольных компьютерах, заблокированный файл не может быть открыт, скопирован, перемещен или открыт для совместного использования. Тем не менее, пользователи могут удалить заблокированный файл. Вот пример того, что выглядит на мобильном устройстве пользователя:</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p103">Although the blocked file is still listed in the document library and web, mobile, or desktop applications, the blocked file cannot be opened, copied, moved, or shared. People can, however, delete a blocked file. Here's an example of what that looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="f2ca8-115">[![Удаление заблокированного файла из OneDrive для бизнеса из мобильного приложения OneDrive](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="f2ca8-115">[![Deleting a blocked file from OneDrive for Business from the OneDrive mobile app](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="f2ca8-p104">В зависимости от того, как настроен Office 365, пользователи могут или не могут скачать заблокированный файл. Вот как будет выглядеть заблокированный файл на мобильном устройстве пользователя:</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p104">Depending on how Office 365 is configured, people might or might not have the ability to download a blocked file. Here's what downloading a blocked file looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="f2ca8-118">[![Скачивание заблокированного файла в OneDrive для бизнеса](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="f2ca8-118">[![Downloading a blocked file in OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="f2ca8-119">Чтобы узнать больше, ознакомьтесь [со статьЕй включение Office 365 ATP для SharePoint, OneDrive и Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="f2ca8-119">To learn more, see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>
  
## <a name="keep-these-points-in-mind"></a><span data-ttu-id="f2ca8-120">Помните об этих моментах</span><span class="sxs-lookup"><span data-stu-id="f2ca8-120">Keep these points in mind</span></span>

- <span data-ttu-id="f2ca8-p105">ATP не будет сканировать каждый отдельный файл в SharePoint Online, OneDrive для бизнеса или Microsoft Teams. Это сделано по проектированию. Файлы сканируются асинхронно, с помощью процесса, который использует события общего доступа и гостевых действий, а также интеллектуальные эвристики и сигналы угроз для идентификации вредоносных файлов.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p105">ATP will not scan every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams. This is by design. Files are scanned asynchronously, through a process that uses sharing and guest activity events along with smart heuristics and threat signals to identify malicious files.</span></span>

- <span data-ttu-id="f2ca8-p106">Убедитесь, что сайты SharePoint настроены на использование [современного интерфейса](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience). Если файл определен как вредоносный и заблокированный, люди могут видеть, что это произошло в современном интерфейсе, но не является классическим представлением. Защита ATP определяет, используется ли современный интерфейс или классическое представление; Однако визуальные индикаторы, заблокированные файлом, присутствуют только в современном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p106">Make sure your SharePoint sites are configured to use the [Modern experience](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience). When a file is identified as malicious and blocked, people can see that this has occurred in the Modern experience, but not the Classic view. ATP protection applies whether the Modern experience or the Classic view is used; however, visual indicators that a file is blocked are present only in the Modern experience.</span></span>
    
- <span data-ttu-id="f2ca8-127">Файлы, которые определены как вредоносные в SharePoint Online, OneDrive для бизнеса или Microsoft Teams, будут отображаться в [отчетах по Office 365 Advanced Threat protection](view-reports-for-atp.md) и в обозревателе угроз (компоненте [Office 365 Threat Intelligence](office-365-ti.md)).</span><span class="sxs-lookup"><span data-stu-id="f2ca8-127">Files that are identified as malicious in SharePoint Online, OneDrive for Business, or Microsoft Teams will show up in [reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md) and in Threat Explorer (part of [Office 365 Threat Intelligence](office-365-ti.md)).</span></span>
    
- <span data-ttu-id="f2ca8-p107">ATP является частью общей стратегии защиты от угроз, включающей защиту от нежелательной почты и вредоносных программ, а также безопасные ссылки и безопасные вложения. Чтобы узнать больше, ознакомьтесь [со статьЕй защита от угроз в Office 365](protect-against-threats.md).</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p107">ATP is part of your organization's overall threat protection strategy, which includes anti-spam and anti-malware protection, as well as Safe Links and Safe Attachments. To learn more, see [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="f2ca8-p108">Администратор SharePoint Online может определить, следует ли разрешить пользователям загружать файлы, обнаруженные как вредоносные. Для этого необходимо выполнить командлет PowerShell Set-SPOTenant с параметром Дисалловинфектедфиледовнлоад ( [включить Office 365 ATP для SharePoint, OneDrive и Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)).</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p108">A SharePoint Online administrator can determine whether to enable people to download files that are detected as malicious. This is done by running the Set-SPOTenant PowerShell cmdlet using a DisallowInfectedFileDownload parameter (see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)).</span></span>
    
## <a name="quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="f2ca8-132">Карантин в ATP для SharePoint Online, OneDrive для бизнеса и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f2ca8-132">Quarantine in ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams</span></span>

 <span data-ttu-id="f2ca8-133">Начиная с опоздания, Май [](quarantine-email-messages.md) 2018, функции карантина &amp; в центре безопасности соответствуют расширению ATP для SharePoint Online, OneDrive для бизнеса и Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-133">Beginning in late May 2018, [quarantine](quarantine-email-messages.md) capabilities in the Security &amp; Compliance Center are being extended to ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>
  
<span data-ttu-id="f2ca8-p109">Если файл в SharePoint Online, OneDrive для бизнеса или Microsoft Teams определен как вредоносный, помимо того, что ATP блокирует файл из-за открытия или предоставления общего доступа, этот файл включается в список элементов, помещенных в карантин. (В центре соответствия &amp; требованиям безопасности перейдите к разделу \> **Обзор** \> \*\*\*\* **управления угрозами** карантина и отфильтруйте **содержимое**.)</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p109">When a file in SharePoint Online, OneDrive for Business, or Microsoft Teams is identified as malicious, in addition to ATP blocking the file from being opened or shared, that file is included in a list of quarantined items. (In the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Quarantine** and filter for **Content**.)</span></span> 
  
<span data-ttu-id="f2ca8-136">Если вы являетесь участником группы безопасности Office 365 и у вас есть необходимые [разрешения в центре безопасности &amp; Office 365](permissions-in-the-security-and-compliance-center.md), вы можете скачать, освободить, отчитываться и удалять файлы, обнаруженные как вредоносные, с помощью ATP. из карантина.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-136">If you're part of your organization's Office 365 security team and have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), you can download, release, report, and delete files that are detected as malicious by ATP from quarantine.</span></span>
  
- <span data-ttu-id="f2ca8-p110">При **освобождении и составлении отчетов** файл удаляется в файле на соответствующем сайте группы или в библиотеке документов для SharePoint, OneDrive или Microsoft Teams. После этого пользователи смогут открывать, предоставлять к ним общий доступ и скачивать файл. Если выбран параметр **Отправить отчет корпорации Майкрософт** , файл сообщается о ложном срабатывании в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p110">**Releasing and reporting** a file removes the ATP block on the file in the respective team site or document library for SharePoint, OneDrive, or Microsoft Teams. Users are then able to open, share, and download the file. And, when the **Send report to Microsoft** option is selected, the file is reported as a false positive to Microsoft.</span></span> 
    
- <span data-ttu-id="f2ca8-p111">При **удалении файла** удаляется файл из карантина; Тем не менее, файл по-прежнему заблокирован от открытия или предоставления общего доступа. Файл также должен быть удален в соответствующей библиотеке документов или на сайте группы (SharePoint Online, OneDrive для бизнеса или Microsoft Teams).</span><span class="sxs-lookup"><span data-stu-id="f2ca8-p111">**Deleting a file** removes the file from quarantine; however, the file is still blocked from being opened or shared. The file must also be deleted in its respective document library or team site (SharePoint Online, OneDrive for Business, or Microsoft Teams).</span></span> 
    
- <span data-ttu-id="f2ca8-142">**Загрузка файла** позволяет скачать и проанализировать файл на наличие ложных срабатываний.</span><span class="sxs-lookup"><span data-stu-id="f2ca8-142">**Downloading a file** enables you to download and analyze the file for any false positives.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="f2ca8-143">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f2ca8-143">Next steps</span></span>

1. [<span data-ttu-id="f2ca8-144">Включение Office 365 ATP для SharePoint, OneDrive и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f2ca8-144">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)
    
2. [<span data-ttu-id="f2ca8-145">Просмотр сведений о вредоносных файлах, обнаруженных в SharePoint, OneDrive или Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f2ca8-145">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
