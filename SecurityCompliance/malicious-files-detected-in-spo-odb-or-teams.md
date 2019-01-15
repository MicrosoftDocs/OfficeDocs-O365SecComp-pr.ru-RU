---
title: Просмотр сведений о вредоносных файлов, обнаруженных в SharePoint, OneDrive или группами Майкрософт
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Узнайте, куда обращаться, чтобы просмотреть сведения о вредоносных файлов, обнаруженных в SharePoint, OneDrive и группам, а также выполнять операции эти файлы.
ms.openlocfilehash: 435e1f449003f670f698c4e6813e18f5e83c498d
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014801"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a><span data-ttu-id="64d41-103">Просмотр сведений о вредоносных файлов, обнаруженных в SharePoint, OneDrive или группами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="64d41-103">View information about malicious files detected in SharePoint, OneDrive, or Microsoft Teams</span></span>

<span data-ttu-id="64d41-p101">[Office 365 ATP для SharePoint, OneDrive и группами Майкрософт](atp-for-spo-odb-and-teams.md) защищает вашей организации от вредоносных файлов в библиотеках документов и сайтов групп. При обнаружении вредоносных файлов, этот файл блокируется, чтобы никто можно открыть, скопируйте, перемещение или совместно использовать до дополнительных действий группой безопасности в организации. В этой статье, чтобы узнать, как просматривать сведения об обнаруженных файлов и действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="64d41-p101">[Office 365 ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md) protects your organization from malicious files in document libraries and team sites. When a malicious file is detected, that file is blocked so that no one can open, copy, move, or share it until further actions are taken by the organization's security team. Read this article to learn how to view information about detected files and what actions to take.</span></span> 

<span data-ttu-id="64d41-107">Для выполнения задач, описанных в этой статье, необходимо иметь необходимые [разрешения для системы безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="64d41-107">In order to perform the tasks described in this article, you must have the necessary [permissions for the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="view-reports-with-information-about-detected-files"></a><span data-ttu-id="64d41-108">Просмотр отчетов со сведениями об обнаруженных файлов</span><span class="sxs-lookup"><span data-stu-id="64d41-108">View reports with information about detected files</span></span>

<span data-ttu-id="64d41-109">Чтобы просмотреть состояние, а также подробные сведения о файлах, обнаруженных с Office 365 ATP, можно использовать отчет о состоянии защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="64d41-109">To view status and detailed information about files that were detected by Office 365 ATP, you can use the Threat Protection Status report.</span></span>
  
1. <span data-ttu-id="64d41-110">В [безопасности Office 365 &amp; центре соответствия требованиям](https://protection.office.com), выберите **отчеты о** \> **панели мониторинга** \> **Состояние защиты от угроз**.</span><span class="sxs-lookup"><span data-stu-id="64d41-110">In the [Office 365 Security &amp; Compliance Center](https://protection.office.com), choose **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
    
2. <span data-ttu-id="64d41-111">В правом верхнем углу отчета выберите **Таблица сведения о представлении**.</span><span class="sxs-lookup"><span data-stu-id="64d41-111">In the upper right corner of the report, choose **View details table**.</span></span>
    
3. <span data-ttu-id="64d41-112">Просмотр списка файлов, обнаруженные в отчете.</span><span class="sxs-lookup"><span data-stu-id="64d41-112">View the list of files that were detected in the report.</span></span>
    
4. <span data-ttu-id="64d41-113">Выберите элемент в списке, чтобы просмотреть подробные сведения, включая действия, предпринимаемые, имя файла, путь к файлу и другие.</span><span class="sxs-lookup"><span data-stu-id="64d41-113">Select an item in the list to view detailed information, including actions taken, the file name, the file path, and more.</span></span>
    
5. <span data-ttu-id="64d41-114">Перейдите на вкладку **Дополнительно анализа** для просмотра информации, например наблюдаемой поведение и анализа сведений.</span><span class="sxs-lookup"><span data-stu-id="64d41-114">Choose the **Advanced Analysis** tab to view information, such as observed behavior and analysis details.</span></span> 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a><span data-ttu-id="64d41-115">Просмотр и выполнение действий на файлы на карантине</span><span class="sxs-lookup"><span data-stu-id="64d41-115">View and take action on files in quarantine</span></span>

1. <span data-ttu-id="64d41-116">В Office 365 безопасность &amp; центре соответствия требованиям, выберите **Threat management** \> **проверки** \> **карантина**.</span><span class="sxs-lookup"><span data-stu-id="64d41-116">In the Office 365 Security &amp; Compliance Center, choose **Threat management** \> **Review** \> **Quarantine**.</span></span>
    
2. <span data-ttu-id="64d41-117">В верхнем левом углу измените фильтр из **электронной почты** для **контента**.</span><span class="sxs-lookup"><span data-stu-id="64d41-117">In the upper left corner, change the filter from **Email** to **Content**.</span></span>
    
3. <span data-ttu-id="64d41-118">Выберите элемент в списке, чтобы просмотреть подробные сведения, включая URL-адреса файла.</span><span class="sxs-lookup"><span data-stu-id="64d41-118">Select an item in the list to view detailed information, including the file's URL.</span></span>
    
4. <span data-ttu-id="64d41-119">Выбор доступного действия.</span><span class="sxs-lookup"><span data-stu-id="64d41-119">Choose an available action.</span></span>
    
  - <span data-ttu-id="64d41-120">Выберите **выпуске &amp; отчета** разблокировать файл.</span><span class="sxs-lookup"><span data-stu-id="64d41-120">Choose **Release &amp; report** to unblock the file.</span></span> 
    
    <span data-ttu-id="64d41-121">Установите флажок **Отправить отчет в корпорацию Майкрософт** для занесения в файл как Ложное срабатывание в корпорацию Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="64d41-121">Select **Send report to Microsoft** to report the file as a false positive to Microsoft.</span></span> 
    
  - <span data-ttu-id="64d41-122">Выберите **загружать файл** для файла дальнейшего изучения.</span><span class="sxs-lookup"><span data-stu-id="64d41-122">Choose **Download file** to investigate the file further.</span></span> 
    
  - <span data-ttu-id="64d41-p102">Выберите команду **Удалить** для удаления файла из списка элементы, помещенные на карантин. Если выбран этот параметр, необходимо также удалите файл из его соответствующих библиотеки в SharePoint Online, OneDrive для бизнеса, или группами Майкрософт. Этот параметр не разблокировать файл не открывается или общих.</span><span class="sxs-lookup"><span data-stu-id="64d41-p102">Choose **Delete** to remove the file from the list of quarantined items. If you choose this option, you must also delete the file from its respective library in SharePoint Online, OneDrive for Business, or Microsoft Teams. This option does not unblock a file from being opened or shared.</span></span> 
    
5. <span data-ttu-id="64d41-126">Нажмите кнопку **Закрыть** , чтобы закрыть сведений для выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="64d41-126">Choose **Close** to close the details for a selected item.</span></span> 
  
  

