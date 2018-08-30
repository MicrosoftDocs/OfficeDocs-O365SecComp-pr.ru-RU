---
title: Просмотр сведений о вредоносных файлов, обнаруженных в SharePoint, OneDrive или группами Майкрософт
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 5/31/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Узнайте, куда обращаться, чтобы просмотреть сведения о вредоносных файлов, обнаруженных в SharePoint, OneDrive и группам, а также выполнять операции эти файлы.
ms.openlocfilehash: e9a68c1cee1f2f3fb7fba148365449f0136fe637
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534830"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="a21f0-103">Просмотр сведений о вредоносных файлов, обнаруженных в SharePoint, OneDrive или группами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="a21f0-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="a21f0-p101">[Office 365 ATP для SharePoint, OneDrive и группами Майкрософт](atp-for-spo-odb-and-teams.md) защищает вашей организации от вредоносных файлов в библиотеках документов и сайтов групп. При обнаружении вредоносных файлов, этот файл блокируется, чтобы никто можно открыть, скопируйте, перемещение или совместно использовать до дополнительных действий группой безопасности в организации. В этой статье, чтобы узнать, как просматривать сведения об обнаруженных файлов и действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="a21f0-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 
  
> [!TIP]
> <span data-ttu-id="a21f0-107">Для выполнения задач, описанных в этой статье, необходимо иметь необходимые [разрешений, назначенных безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="a21f0-107">In order to perform the tasks described in this article, you must have the necessary [permissions assigned in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="a21f0-108">Просмотр отчетов со сведениями об обнаруженных файлов</span><span class="sxs-lookup"><span data-stu-id="a21f0-108">View reports with information about detected files</span></span>

<span data-ttu-id="a21f0-109">Чтобы просмотреть состояние, а также подробные сведения о файлах, обнаруженных с Office 365 ATP, можно использовать отчет о состоянии защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="a21f0-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat protection status report.</span></span>
  
1. <span data-ttu-id="a21f0-110">В Office 365 безопасность &amp; центре соответствия требованиям, выберите **отчеты о** \> **панели мониторинга** \> **состояние защиты от угроз**.</span><span class="sxs-lookup"><span data-stu-id="a21f0-110">In the Office 365 Security &amp; Compliance Center, choose **Reports** \> **Dashboard** \> **Threat protection status**.</span></span>
    
2. <span data-ttu-id="a21f0-111">В правом верхнем углу отчета выберите **Таблица сведения о представлении**.</span><span class="sxs-lookup"><span data-stu-id="a21f0-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="a21f0-112">Просмотр списка файлов, обнаруженные в отчете.</span><span class="sxs-lookup"><span data-stu-id="a21f0-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="a21f0-113">Выберите элемент в списке, чтобы просмотреть подробные сведения, включая действия, предпринимаемые, имя файла, путь к файлу и другие.</span><span class="sxs-lookup"><span data-stu-id="a21f0-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="a21f0-114">Перейдите на вкладку **Дополнительно анализа** для просмотра информации, например наблюдаемой поведение и анализа сведений.</span><span class="sxs-lookup"><span data-stu-id="a21f0-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
    
> [!TIP]
> <span data-ttu-id="a21f0-115">[Просмотр отчетов для защиты от угроз для Office 365 расширенного](view-reports-for-atp.md)Дополнительные сведения о доступных отчетов, см.</span><span class="sxs-lookup"><span data-stu-id="a21f0-115">To learn more about available reports, see [View reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md).</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="a21f0-116">Просмотр и выполнение действий на файлы на карантине</span><span class="sxs-lookup"><span data-stu-id="a21f0-116">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="a21f0-117">В Office 365 безопасность &amp; центре соответствия требованиям, выберите **Threat management** \> **проверки** \> **карантина**.</span><span class="sxs-lookup"><span data-stu-id="a21f0-117">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="a21f0-118">В верхнем левом углу измените фильтр из **электронной почты** для **контента**.</span><span class="sxs-lookup"><span data-stu-id="a21f0-118">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="a21f0-119">Выберите элемент в списке, чтобы просмотреть подробные сведения, включая URL-адреса файла.</span><span class="sxs-lookup"><span data-stu-id="a21f0-119">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="a21f0-120">Выбор доступного действия.</span><span class="sxs-lookup"><span data-stu-id="a21f0-120">Choose an available action.</span></span>
    
  - <span data-ttu-id="a21f0-121">Выберите **выпуске &amp; отчета** разблокировать файл.</span><span class="sxs-lookup"><span data-stu-id="a21f0-121">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="a21f0-122">Установите флажок **Отправить отчет в корпорацию Майкрософт** для занесения в файл как Ложное срабатывание в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a21f0-122">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="a21f0-123">Выберите **загружать файл** для файла дальнейшего изучения.</span><span class="sxs-lookup"><span data-stu-id="a21f0-123">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="a21f0-p102">Выберите команду **Удалить** для удаления файла из списка элементы, помещенные на карантин. Если выбран этот параметр, необходимо также удалите файл из его соответствующих библиотеки в SharePoint Online, OneDrive для бизнеса, или группами Майкрософт. Этот параметр не разблокировать файл не открывается или общих.</span><span class="sxs-lookup"><span data-stu-id="a21f0-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="a21f0-127">Нажмите кнопку **Закрыть** , чтобы закрыть сведений для выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="a21f0-127">Choose **Close** to close the details for a selected item.</span></span> 
    
> [!TIP]
> <span data-ttu-id="a21f0-128">Чтобы Дополнительные сведения об управлении из карантина файлы, обратитесь к разделу [Управление в карантин сообщения и файлы с правами администратора в Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="a21f0-128">To learn more about managing quarantined files, see [Manage quarantined messages and files as an administrator in Office 365](manage-quarantined-messages-and-files.md).</span></span> 
  
## <a name="related-topics"></a><span data-ttu-id="a21f0-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a21f0-129">Related topics</span></span>

[<span data-ttu-id="a21f0-130">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a21f0-130">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="a21f0-131">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="a21f0-131">View the reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="a21f0-132">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="a21f0-132">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

