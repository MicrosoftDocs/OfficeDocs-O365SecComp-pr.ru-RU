---
title: Изменение размера PST-файлов при экспорте результаты поиска обнаружения электронных данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Можно изменить размер по умолчанию PST-файлы, которые загружаются на компьютер, после экспорта результатов поиска обнаружения электронных данных.
ms.openlocfilehash: c01f05a02fd94941eb2eb7a05b4c84ffecec9b39
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522250"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a><span data-ttu-id="04f6e-103">Изменение размера PST-файлов при экспорте результаты поиска обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="04f6e-103">Change the size of PST files when exporting eDiscovery search results</span></span>

<span data-ttu-id="04f6e-p101">При использовании средства экспорта eDiscovery Office 365 для экспорта результатов поиска методом электронного обнаружения электронной почты с помощью различных средств обнаружения электронных данных Microsoft размер по умолчанию в PST-файл, который можно экспортировать — 10 ГБ. Если вы хотите изменить этот размер по умолчанию, можно изменить реестра Windows на компьютере, которая используется для экспорта результатов поиска. Одной из причин для этого — можно для размещения в PST-файл на съемный носитель, такой DVD-ДИСК, компакт-диска или USB-диска.</span><span class="sxs-lookup"><span data-stu-id="04f6e-p101">When you use the Office 365 eDiscovery Export tool to export the email results of an eDiscovery search from the different Microsoft eDiscovery tools, the default size of a PST file that can be exported is 10 GB. If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results. One reason to do this is so a PST file can fit on removable media, such a DVD, a compact disc, or a USB drive.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="04f6e-107">Средство экспорта Office 365 eDiscovery используется для экспорта результатов поиска при использовании поиска контента в Office 365 безопасность &amp; центре соответствия требованиям, обнаружение электронных данных на месте в Exchange Online и центр обнаружения электронных данных в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="04f6e-107">The Office 365 eDiscovery Export tool is used to export the search results when using Content Search in the Office 365 Security &amp; Compliance Center, In-Place eDiscovery in Exchange Online, and the eDiscovery Center in SharePoint Online.</span></span> 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="04f6e-108">Создание параметров реестра для изменения размера PST-файлов при экспорте результаты поиска обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="04f6e-108">Create a registry setting to change the size of PST files when you export eDiscovery search results</span></span>

<span data-ttu-id="04f6e-109">Выполните следующую процедуру на компьютере, на котором используется для экспорта результатов поиска методом электронного обнаружения.</span><span class="sxs-lookup"><span data-stu-id="04f6e-109">Perform the following procedure on the computer that you'll use to export the results of an eDiscovery search.</span></span>
  
1. <span data-ttu-id="04f6e-110">Если открыта, закройте средство экспорта eDiscovery Office 365.</span><span class="sxs-lookup"><span data-stu-id="04f6e-110">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="04f6e-111">Сохраните следующий текст в файл реестра окна с помощью суффикса имени файла в формате REG; Например PstExportSize.reg.</span><span class="sxs-lookup"><span data-stu-id="04f6e-111">Save the following text to a Window registry file by using a filename suffix of .reg; for example, PstExportSize.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    <span data-ttu-id="04f6e-p102">В предыдущем примере `PstSizeLimitInBytes` значение 1 073 741 824 байт или приблизительно 1 ГБ. Ниже приведены некоторые другие образцы значений для `PstSizeLimitInBytes` параметр.</span><span class="sxs-lookup"><span data-stu-id="04f6e-p102">In the example above, the  `PstSizeLimitInBytes` value is set to 1,073,741,824 bytes or approximately 1 GB. Here are some other sample values for the  `PstSizeLimitInBytes` setting.</span></span> 
    
    |<span data-ttu-id="04f6e-114">**Размер в ГБ (приблизительно до)**</span><span class="sxs-lookup"><span data-stu-id="04f6e-114">**Size in GB (approx.)**</span></span>|<span data-ttu-id="04f6e-115">**Размер в байтах**</span><span class="sxs-lookup"><span data-stu-id="04f6e-115">**Size in bytes**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="04f6e-116">.7 ГБ (700 МБ)</span><span class="sxs-lookup"><span data-stu-id="04f6e-116">.7 GB (700 MB)</span></span>  <br/> |<span data-ttu-id="04f6e-117">751619277</span><span class="sxs-lookup"><span data-stu-id="04f6e-117">751619277</span></span>  <br/> |
    |<span data-ttu-id="04f6e-118">2 ГБ</span><span class="sxs-lookup"><span data-stu-id="04f6e-118">2 GB</span></span>  <br/> |<span data-ttu-id="04f6e-119">2147483648</span><span class="sxs-lookup"><span data-stu-id="04f6e-119">2147483648</span></span>  <br/> |
    |<span data-ttu-id="04f6e-120">4 ГБ</span><span class="sxs-lookup"><span data-stu-id="04f6e-120">4 GB</span></span>  <br/> |<span data-ttu-id="04f6e-121">4294967296</span><span class="sxs-lookup"><span data-stu-id="04f6e-121">4294967296</span></span>  <br/> |
    |<span data-ttu-id="04f6e-122">8 ГБ</span><span class="sxs-lookup"><span data-stu-id="04f6e-122">8 GB</span></span>  <br/> |<span data-ttu-id="04f6e-123">8589934592</span><span class="sxs-lookup"><span data-stu-id="04f6e-123">8589934592</span></span>  <br/> |
   
3. <span data-ttu-id="04f6e-124">Изменение `PstSizeLimitInBytes` значение нужный максимальный размер в PST-файл после экспорта результатов поиска, а затем сохраните файл.</span><span class="sxs-lookup"><span data-stu-id="04f6e-124">Change the `PstSizeLimitInBytes` value to the desired maximum size of a PST file when you export search results, and then save the file.</span></span> 
    
4. <span data-ttu-id="04f6e-125">В проводнике Windows щелкните или дважды щелкните REG-файл, созданный на предыдущих шагах.</span><span class="sxs-lookup"><span data-stu-id="04f6e-125">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
5. <span data-ttu-id="04f6e-126">В окне Управление доступом пользователей, нажмите кнопку **Да** для перехода на редактор реестра.</span><span class="sxs-lookup"><span data-stu-id="04f6e-126">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
6. <span data-ttu-id="04f6e-127">Чтобы продолжить, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="04f6e-127">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="04f6e-128">В редакторе реестра отображается появится сообщение о том, что параметр был успешно добавлен в реестр.</span><span class="sxs-lookup"><span data-stu-id="04f6e-128">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
7. <span data-ttu-id="04f6e-129">Повторите шаги 3 – 6, чтобы изменить значение для `PstSizeLimitInBytes` параметр реестра.</span><span class="sxs-lookup"><span data-stu-id="04f6e-129">You can repeat steps 3 - 6 to change the value for the  `PstSizeLimitInBytes` registry setting.</span></span> 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="04f6e-130">Часто задаваемые вопросы об изменении по умолчанию размер файлов PST-файлов при экспорте результаты поиска обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="04f6e-130">Frequently asked questions about changing the default size of PST files when you export eDiscovery search results</span></span>

 <span data-ttu-id="04f6e-131">**Почему используется по умолчанию размер 10 ГБ?**</span><span class="sxs-lookup"><span data-stu-id="04f6e-131">**Why is the default size 10 GB?**</span></span>
  
<span data-ttu-id="04f6e-132">По умолчанию размер 10 ГБ был на основе отзывов; 10 ГБ — это хороший баланс между оптимальную объем контента в одном PST и с минимальным вероятность повреждения файлов.</span><span class="sxs-lookup"><span data-stu-id="04f6e-132">The default size of 10 GB was based on customer feedback; 10 GB is a good balance between the optimal amount of content in a single PST and with a minimum chance of file corruption.</span></span>
  
 <span data-ttu-id="04f6e-133">**Следует ли увеличить или уменьшить размер по умолчанию PST-файлов?**</span><span class="sxs-lookup"><span data-stu-id="04f6e-133">**Should I increase or decrease the default size of PST files?**</span></span>
  
<span data-ttu-id="04f6e-p103">Клиенты, как правило, уменьшение ограничение размера, чтобы результаты поиска помещается на съемный носитель, что они физически поставляют другие расположения в своей организации. Не рекомендуется, увеличьте размер по умолчанию, так как файлы размером более 10 ГБ может быть повреждение файлов PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="04f6e-p103">Customers tend to decrease the size limit so that the search results will fit on removable media that they can physically ship other locations in their organization. We don't recommend that you increase the default size because PST files larger than 10 GB might have corruption issues.</span></span>
  
 <span data-ttu-id="04f6e-136">**Какой компьютер следует сделать это в?**</span><span class="sxs-lookup"><span data-stu-id="04f6e-136">**What computer do I have to do this on?**</span></span>
  
<span data-ttu-id="04f6e-137">Необходимо изменить значение параметра реестра на локальном компьютере, которую можно запускать средство экспорта Office 365 обнаружения электронных данных на.</span><span class="sxs-lookup"><span data-stu-id="04f6e-137">You need to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span>
  
 <span data-ttu-id="04f6e-138">**После изменения этого параметра, необходимо перезагрузить компьютер?**</span><span class="sxs-lookup"><span data-stu-id="04f6e-138">**After I change this setting, do I have to reboot the computer?**</span></span>
  
<span data-ttu-id="04f6e-p104">Нет, не требуется перезагрузка компьютера. Однако, если выполняется средство экспорта eDiscovery Office 365, необходимо закрыть его и перезагрузите его после изменения этого параметра.</span><span class="sxs-lookup"><span data-stu-id="04f6e-p104">No, you don't have to reboot the computer. But, if the Office 365 eDiscovery Export tool is running, you'll have to close it and the restart it after you change this setting.</span></span>
  
 <span data-ttu-id="04f6e-141">**Получите изменить существующий раздел реестра или создается новый ключ?**</span><span class="sxs-lookup"><span data-stu-id="04f6e-141">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="04f6e-p105">При первом запуске REG-файл, созданный в этой процедуре создается новый раздел реестра. Выберите параметр изменяется каждый раз, изменять и повторно запустить файл Правка.</span><span class="sxs-lookup"><span data-stu-id="04f6e-p105">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
