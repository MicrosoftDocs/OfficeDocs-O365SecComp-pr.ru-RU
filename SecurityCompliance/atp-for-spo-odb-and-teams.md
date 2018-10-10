---
title: Office 365 ATP для SharePoint, OneDrive и Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
description: Расширение защиту от угроз для Office 365 дополнительные файлы в SharePoint Online, OneDrive для бизнеса и группами Майкрософт для включения более безопасной совместной работы для вашей организации.
ms.openlocfilehash: ff07d88a150d3f059681556feec9a5e89b5875a8
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454326"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="6fa4f-103">Office 365 ATP для SharePoint, OneDrive и Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6fa4f-103">Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

## <a name="overview-of-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a><span data-ttu-id="6fa4f-104">Обзор Office 365 ATP для SharePoint, OneDrive и группами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="6fa4f-104">Overview of Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>

<span data-ttu-id="6fa4f-p101">Регулярно людей файлы совместный доступ и совместная работа с помощью SharePoint, OneDrive и группами Майкрософт. С [Защиту от угроз для Office 365 Advanced](office-365-atp.md) (ATP) организации могут совместно работать более безопасным способом. ATP помогает обнаруживать и блокировать файлы, которые определены как вредоносный в веб-сайтов групп и библиотеки документов.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p101">People regularly share files and collaborate using SharePoint, OneDrive, and Microsoft Teams. With [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP), your organization can collaborate in a safer manner. ATP helps detect and block files that are identified as malicious in team sites and document libraries.</span></span>  
  
### <a name="how-it-works"></a><span data-ttu-id="6fa4f-108">Как это работает</span><span class="sxs-lookup"><span data-stu-id="6fa4f-108">How it works</span></span>

<span data-ttu-id="6fa4f-p102">При создании файла в SharePoint Online, OneDrive для бизнеса и группами Майкрософт определено как вредоносный, ATP непосредственно интегрируется с файловых хранилищ для блокировки файла. Ниже рисунке показан пример вредоносных файлов, обнаруженных в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p102">When a file in SharePoint Online, OneDrive for Business, and Microsoft Teams has been identified as malicious, ATP directly integrates with the file stores to lock that file. The following image shows an example of a malicious file detected in a library.</span></span>
  
<span data-ttu-id="6fa4f-111">[![Снимок экрана с файлов в OneDrive для бизнеса с одним обнаруженных вредоносных](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="6fa4f-111">[![Screenshot of files in OneDrive for Business with one detected as malicious](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="6fa4f-p103">Хотя заблокированных файлов по-прежнему отображается в библиотеки документов и веб-сайта с мобильных устройств или настольных приложений, заблокированных файлов не может быть открыт, скопировать, перемещен или общих. Люди могут тем не менее, удаление заблокированных файлов. Вот пример того, что похожа на мобильном устройстве пользователя:</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p103">Although the blocked file is still listed in the document library and web, mobile, or desktop applications, the blocked file cannot be opened, copied, moved, or shared. People can, however, delete a blocked file. Here's an example of what that looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="6fa4f-115">[![Снимок экрана с Удаление заблокированных файлов из службы OneDrive для бизнеса из OneDrive мобильного приложения](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="6fa4f-115">[![Screenshot of deleting a blocked file from OneDrive for Business from the OneDrive mobile app](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="6fa4f-p104">В зависимости от способа настройки Office 365 пользователи могут или может не иметь возможность загружать заблокированных файлов. Вот что загрузка заблокированных файлов похожа на мобильном устройстве пользователя:</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p104">Depending on how Office 365 is configured, people might or might not have the ability to download a blocked file. Here's what downloading a blocked file looks like on a user's mobile device:</span></span>
  
<span data-ttu-id="6fa4f-118">[![Снимок экрана загрузки заблокированных файлов в OneDrive для бизнеса](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span><span class="sxs-lookup"><span data-stu-id="6fa4f-118">[![Screenshot of downloading a blocked file in OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)</span></span>
  
<span data-ttu-id="6fa4f-119">Для получения дополнительных сведений см. [Включение анализа Office 365 для SharePoint, OneDrive и группами Майкрософт](turn-on-atp-for-spo-odb-and-teams.md).</span><span class="sxs-lookup"><span data-stu-id="6fa4f-119">To learn more, see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).</span></span>
  
### <a name="keep-the-following-points-in-mind"></a><span data-ttu-id="6fa4f-120">Помнить следующее</span><span class="sxs-lookup"><span data-stu-id="6fa4f-120">Keep the following points in mind</span></span>

- <span data-ttu-id="6fa4f-p105">Пакет анализа не будет выполнять сканирование каждый отдельный файл в SharePoint Online, OneDrive для бизнеса, или группами Майкрософт. Это предусмотрено при проектировании. Файлы проверяются асинхронно, через процесс, который использует общего доступа и гостя события активности наряду с эвристическую и сигналы угрозы для идентификации вредоносных файлов.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p105">ATP will not scan every single file in SharePoint Online, OneDrive for Business, or Microsoft Teams. This is by design. Files are scanned asynchronously, through a process that uses sharing and guest activity events along with smart heuristics and threat signals to identify malicious files.</span></span>

- <span data-ttu-id="6fa4f-p106">Убедитесь, что сайты SharePoint настроен для использования [современных качества](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience). Если файл помечаются как вредоносных и заблокированные, люди могут видеть, что происходит в современном качества, но не классический вид. Защита ATP применяется ли современный интерфейс или классический вид используется; Тем не менее графические индикаторы, что файл блокирован присутствуют только в современном качества.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p106">Make sure your SharePoint sites are configured to use the [Modern experience](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience). When a file is identified as malicious and blocked, people can see that this has occurred in the Modern experience, but not the Classic view. ATP protection applies whether the Modern experience or the Classic view is used; however, visual indicators that a file is blocked are present only in the Modern experience.</span></span>
    
- <span data-ttu-id="6fa4f-127">Файлы, которые определяются как вредоносных в SharePoint Online, OneDrive для бизнеса, или группами Майкрософт будет отображаться в [отчетах для защиты от угроз для Office 365 Дополнительно](view-reports-for-atp.md) и в обозревателе угроз (часть [Анализ угроз Office 365](office-365-ti.md)).</span><span class="sxs-lookup"><span data-stu-id="6fa4f-127">Files that are identified as malicious in SharePoint Online, OneDrive for Business, or Microsoft Teams will show up in [reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md) and in Threat Explorer (part of [Office 365 Threat Intelligence](office-365-ti.md)).</span></span>
    
- <span data-ttu-id="6fa4f-p107">Пакет анализа является частью вашей организации общий threat стратегии защиты, включая защиты от нежелательной почты и вредоносных программ, а также безопасных ссылок и безопасные вложения. Чтобы получить дополнительные сведения, обратитесь к разделу [Защита от угроз в Office 365](protect-against-threats.md).</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p107">ATP is part of your organization's overall threat protection strategy, which includes anti-spam and anti-malware protection, as well as Safe Links and Safe Attachments. To learn more, see [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="6fa4f-p108">Определяет администратору SharePoint Online, следует ли разрешить пользователям загружать файлы, которые распознаются как вредоносный. Это делается с помощью командлета Set-SPOTenant PowerShell с помощью параметра DisallowInfectedFileDownload (см. [Включение анализа Office 365 для SharePoint, OneDrive и группами Майкрософт](turn-on-atp-for-spo-odb-and-teams.md)).</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p108">A SharePoint Online administrator can determine whether to enable people to download files that are detected as malicious. This is done by running the Set-SPOTenant PowerShell cmdlet using a DisallowInfectedFileDownload parameter (see [Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)).</span></span>
    
## <a name="quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a><span data-ttu-id="6fa4f-132">Карантин в ATP для SharePoint Online, OneDrive для бизнеса и группами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="6fa4f-132">Quarantine in ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams</span></span>

 <span data-ttu-id="6fa4f-133">Приступая к работе в позднее мая 2018, [карантина](quarantine-email-messages.md) возможностях безопасности &amp; центре соответствия требованиям расширяются для анализа для SharePoint Online, OneDrive для бизнеса и группами Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-133">Beginning in late May 2018, [quarantine](quarantine-email-messages.md) capabilities in the Security &amp; Compliance Center are being extended to ATP for SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>
  
<span data-ttu-id="6fa4f-p109">При создании файла в SharePoint Online, OneDrive для бизнеса, или группами Майкрософт определяется как вредоносных, помимо анализа блокировка файла открывать и общих, этот файл будет включено в список элементов, помещенных в карантин. (В системы &amp; центре соответствия требованиям, чтобы перейти на **угроз управления** \> **проверки** \> фильтра для **контента**и **карантина** .)</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p109">When a file in SharePoint Online, OneDrive for Business, or Microsoft Teams is identified as malicious, in addition to ATP blocking the file from being opened or shared, that file is included in a list of quarantined items. (In the Security &amp; Compliance Center, go to **Threat management** \> **Review** \> **Quarantine** and filter for **Content**.)</span></span> 
  
<span data-ttu-id="6fa4f-136">Если вы частью группы безопасности вашей организации Office 365 и имеют необходимые [разрешений, назначенных безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md), можно загрузить, выпуск, сообщить о и удалить файлы, которые распознаются как вредоносный ATP из карантина.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-136">If you're part of your organization's Office 365 security team and have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), you can download, release, report, and delete files that are detected as malicious by ATP from quarantine.</span></span>
  
- <span data-ttu-id="6fa4f-p110">**Releasing и отчетности** файл удаляется блока ATP на файл в соответствующие группы сайта или библиотеки документов для SharePoint, OneDrive или группами Майкрософт. Затем пользователи могут открыть, совместно использовать и загрузите файл. И, если выбран параметр **Отправить отчет в корпорацию Майкрософт** , файл отображается как Ложное срабатывание в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p110">**Releasing and reporting** a file removes the ATP block on the file in the respective team site or document library for SharePoint, OneDrive, or Microsoft Teams. Users are then able to open, share, and download the file. And, when the **Send report to Microsoft** option is selected, the file is reported as a false positive to Microsoft.</span></span> 
    
- <span data-ttu-id="6fa4f-p111">**Удаление файла** удаляет файл из карантина; Тем не менее файл по-прежнему заблокирован не открывается или Общие. Файл также должно быть удалено в его соответствующих документов библиотеки или рабочая группа сайта (SharePoint Online, OneDrive для бизнеса, или группами Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="6fa4f-p111">**Deleting a file** removes the file from quarantine; however, the file is still blocked from being opened or shared. The file must also be deleted in its respective document library or team site (SharePoint Online, OneDrive for Business, or Microsoft Teams).</span></span> 
    
- <span data-ttu-id="6fa4f-142">**Загрузка файла** позволяет загрузить и проанализировать файл для любого числа ошибочных срабатываний фильтра.</span><span class="sxs-lookup"><span data-stu-id="6fa4f-142">**Downloading a file** enables you to download and analyze the file for any false positives.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="6fa4f-143">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6fa4f-143">Next steps</span></span>

- [<span data-ttu-id="6fa4f-144">Включить ATP Office 365 для SharePoint, OneDrive и группами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="6fa4f-144">Turn on Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams</span></span>](turn-on-atp-for-spo-odb-and-teams.md)
    
- [<span data-ttu-id="6fa4f-145">Просмотр сведений о вредоносных файлов, обнаруженных в SharePoint, OneDrive или группами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="6fa4f-145">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>](malicious-files-detected-in-spo-odb-or-teams.md)
    
## <a name="related-topics"></a><span data-ttu-id="6fa4f-146">Смежные темы</span><span class="sxs-lookup"><span data-stu-id="6fa4f-146">Related topics</span></span>

[<span data-ttu-id="6fa4f-147">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="6fa4f-147">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="6fa4f-148">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="6fa4f-148">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="6fa4f-149">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="6fa4f-149">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

