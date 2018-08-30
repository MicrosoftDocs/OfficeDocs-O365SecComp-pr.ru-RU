---
title: Отключение отчетов после экспорта результатов поиска контента в Office 365 безопасность &amp; центре соответствия требованиям
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Изменение реестра Windows на локальном компьютере, чтобы отключить отчеты при экспорте результатов поиска контента из безопасности Office 365 &amp; Comliance центр. Отключение этих отчетов можно ускорить время загрузки и сохранить на диске.
ms.openlocfilehash: 3c09e0563ddd4469f21950dc3a698ce08b0014df
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535373"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="d6b50-104">Отключение отчетов после экспорта результатов поиска контента в Office 365 безопасность &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d6b50-104">Disable reports when you export Content Search results in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="d6b50-p102">При использовании средства экспорта eDiscovery Office 365 для экспорта результатов поиска содержимого в системы &amp; центре соответствия требованиям, средство автоматически создает и экспортирует два отчета, которые содержат дополнительные сведения о экспортированное содержимое. Эти отчеты являются Results.csv файл и файл Manifest.xml (в разделе [часто задаваемые вопросы об отключении экспорт отчетов](#frequently-asked-questions-about-disabling-export-reports) в данном разделе приведены подробные описания этих отчетов). Так как эти файлы могут быть очень большой, может ускорить время загрузки и сохраните дискового пространства, предотвращая этих файлов экспорта. Это можно сделать с помощью изменения реестра Windows на компьютере, которая используется для экспорта результатов поиска. Если вы хотите включить отчеты в дальнейшем, можно изменить параметр реестра.</span><span class="sxs-lookup"><span data-stu-id="d6b50-p102">When you use the Office 365 eDiscovery Export tool to export the results of a Content Search in the Security &amp; Compliance Center, the tool automatically creates and exports two reports that contain additional information about the exported content. These reports are the Results.csv file and the Manifest.xml file (see the [Frequently asked questions about disabling export reports](#frequently-asked-questions-about-disabling-export-reports) section in this topic for detailed descriptions of these reports). Because these files can be very large, you can speed up the download time and save disk space by preventing these files from being exported. You can do this by changing the Windows Registry on the computer that you use to export the search results. If you want to include the reports at a later time, you can edit the registry setting.</span></span> 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a><span data-ttu-id="d6b50-110">Создание параметров реестра для отключения отчетов экспорта</span><span class="sxs-lookup"><span data-stu-id="d6b50-110">Create registry settings to disable the export reports</span></span>

<span data-ttu-id="d6b50-111">Выполните следующую процедуру на компьютере, на котором используется для экспорта результатов поиска контента.</span><span class="sxs-lookup"><span data-stu-id="d6b50-111">Perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="d6b50-112">Если открыта, закройте средство экспорта eDiscovery Office 365.</span><span class="sxs-lookup"><span data-stu-id="d6b50-112">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="d6b50-113">Выполните одно или оба из следующих действий, в зависимости от того, какой отчет экспорта необходимо отключить.</span><span class="sxs-lookup"><span data-stu-id="d6b50-113">Perform one or both of the following steps, depending on which export report you want to disable.</span></span>
    
    - <span data-ttu-id="d6b50-114">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="d6b50-114">**Results.csv**</span></span>
    
      <span data-ttu-id="d6b50-115">Сохраните следующий текст в файл реестра Windows с помощью суффикса имени файла в формате REG; Например DisableResultsCsv.reg.</span><span class="sxs-lookup"><span data-stu-id="d6b50-115">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableResultsCsv.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - <span data-ttu-id="d6b50-116">**Файл manifest.XML**</span><span class="sxs-lookup"><span data-stu-id="d6b50-116">**Manifest.xml**</span></span>
    
      <span data-ttu-id="d6b50-117">Сохраните следующий текст в файл реестра Windows с помощью суффикса имени файла в формате REG; Например DisableManifestXml.reg.</span><span class="sxs-lookup"><span data-stu-id="d6b50-117">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableManifestXml.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. <span data-ttu-id="d6b50-118">В проводнике Windows щелкните или дважды щелкните REG-файл, созданный на предыдущих шагах.</span><span class="sxs-lookup"><span data-stu-id="d6b50-118">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
4. <span data-ttu-id="d6b50-119">В окне Управление доступом пользователей, нажмите кнопку **Да** для перехода на редактор реестра.</span><span class="sxs-lookup"><span data-stu-id="d6b50-119">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="d6b50-120">Чтобы продолжить, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="d6b50-120">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="d6b50-121">В редакторе реестра отображается появится сообщение о том, что параметр был успешно добавлен в реестр.</span><span class="sxs-lookup"><span data-stu-id="d6b50-121">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a><span data-ttu-id="d6b50-122">Изменение параметров реестра для повторного включения отчетов экспорта</span><span class="sxs-lookup"><span data-stu-id="d6b50-122">Edit registry settings to re-enable the export reports</span></span>

<span data-ttu-id="d6b50-p103">Если вы отключили отчетов Results.csv и файл Manifest.xml, создав REG-файлы в предыдущей процедуре, можно изменить эти файлы, чтобы повторно включить отчет, чтобы экспортируется с результатами поиска. Еще раз выполните следующую процедуру на компьютере, на котором используется для экспорта результатов поиска контента.</span><span class="sxs-lookup"><span data-stu-id="d6b50-p103">If you disabled the Results.csv and Manifest.xml reports by creating the .reg files in the previous procedure, you can edit those files to re-enable a report so that it's exported with the search results. Again, perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="d6b50-125">Если открыта, закройте средство экспорта eDiscovery Office 365.</span><span class="sxs-lookup"><span data-stu-id="d6b50-125">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="d6b50-126">Измените одно или оба изменить REG-файлов, созданных в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="d6b50-126">Edit one or both of the .reg edit files that you created in the previous procedure.</span></span>
    
    - <span data-ttu-id="d6b50-127">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="d6b50-127">**Results.csv**</span></span>
    
        <span data-ttu-id="d6b50-p104">Откройте файл DisableResultsCsv.reg в блокноте, измените значение `False` для `True`, а затем сохраните файл. Например при изменении файла, он выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d6b50-p104">Open the DisableResultsCsv.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - <span data-ttu-id="d6b50-130">**Файл manifest.XML**</span><span class="sxs-lookup"><span data-stu-id="d6b50-130">**Manifest.xml**</span></span>
    
        <span data-ttu-id="d6b50-p105">Откройте файл DisableManifestXml.reg в блокноте, измените значение `False` для `True`, а затем сохраните файл. Например при изменении файла, он выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d6b50-p105">Open the DisableManifestXml.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. <span data-ttu-id="d6b50-133">В проводнике Windows щелкните или дважды щелкните файл REG, который изменяется на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="d6b50-133">In Windows Explorer, click or double-click a .reg file that you edited in the previous step.</span></span>
    
4. <span data-ttu-id="d6b50-134">В окне Управление доступом пользователей, нажмите кнопку **Да** для перехода на редактор реестра.</span><span class="sxs-lookup"><span data-stu-id="d6b50-134">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="d6b50-135">Чтобы продолжить, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="d6b50-135">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="d6b50-136">В редакторе реестра отображается появится сообщение о том, что параметр был успешно добавлен в реестр.</span><span class="sxs-lookup"><span data-stu-id="d6b50-136">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a><span data-ttu-id="d6b50-137">Часто задаваемые вопросы об отключении экспорт отчетов</span><span class="sxs-lookup"><span data-stu-id="d6b50-137">Frequently asked questions about disabling export reports</span></span>
<span data-ttu-id="d6b50-138"><a name="faqs"> </a></span><span class="sxs-lookup"><span data-stu-id="d6b50-138"></span></span>

 <span data-ttu-id="d6b50-139">**Что такое отчеты Results.csv и файл Manifest.xml**</span><span class="sxs-lookup"><span data-stu-id="d6b50-139">**What are the Results.csv and Manifest.xml reports?**</span></span>
  
<span data-ttu-id="d6b50-140">Файлы Results.csv и файл Manifest.xml содержат дополнительные сведения о контент, который был экспортирован.</span><span class="sxs-lookup"><span data-stu-id="d6b50-140">The Results.csv and Manifest.xml files contain additional information about the content that was exported.</span></span>
  
- <span data-ttu-id="d6b50-p106">Документ Excel **Results.csv** , который содержит сведения о каждого элемента, который можно загрузить в качестве результата поиска. Для электронной почты, журнал результатов содержит сведения о каждом сообщении, включая:</span><span class="sxs-lookup"><span data-stu-id="d6b50-p106">**Results.csv** An Excel document that contains information about each item that is download as a search result. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="d6b50-143">Расположение сообщения в исходном почтовом ящике (включая сведения о том, в каком почтовом ящике находится сообщение, в основном или в архивном).</span><span class="sxs-lookup"><span data-stu-id="d6b50-143">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="d6b50-144">Дата отправки или получения сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6b50-144">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="d6b50-145">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6b50-145">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="d6b50-146">Отправитель и получатели сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6b50-146">The sender and recipients of the message.</span></span>
    
  - <span data-ttu-id="d6b50-p107">Сообщение является ли повторяющихся сообщения Если этот параметр включен дедупликация при экспорте результатов поиска. Дублирующиеся сообщения будут иметь значение в столбце **Идентификатор родительского элемента** , который определяет сообщение как дубликат. Значение в столбце **Идентификатор родительского элемента** — то же, что значение в столбце **DocumentId элемента** , который был экспортирован сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6b50-p107">Whether the message is a duplicate message if you enabled de-duplication when exporting the search results. Duplicate messages will have a value in the **Parent ItemId** column that identifies the message as a duplicate. The value in the **Parent ItemId** column is the same as the value in the **Item DocumentId** column of the message that was exported.</span></span> 
    
    <span data-ttu-id="d6b50-150">Для документов из SharePoint и OneDrive для бизнеса сайтов журнал результатов содержит сведения о каждого документа, включая:</span><span class="sxs-lookup"><span data-stu-id="d6b50-150">For documents from SharePoint and OneDrive for Business sites, the result log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="d6b50-151">URL-адрес документа.</span><span class="sxs-lookup"><span data-stu-id="d6b50-151">The URL for the document.</span></span>
    
  - <span data-ttu-id="d6b50-152">URL-адрес семейства веб-сайтов, в котором расположен документ.</span><span class="sxs-lookup"><span data-stu-id="d6b50-152">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="d6b50-153">Дата последнего изменения документа.</span><span class="sxs-lookup"><span data-stu-id="d6b50-153">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="d6b50-154">Имя документа (которое указано в столбце "Тема" журнала результатов).</span><span class="sxs-lookup"><span data-stu-id="d6b50-154">The name of the document (which is located in the Subject column in the result log).</span></span>
    
- <span data-ttu-id="d6b50-p108">**Файл manifest.XML** файл манифеста (в формате XML), который содержит сведения о каждом элементе, включенные в результатах поиска. Сведения, приведенные в этом отчете совпадает с Results.csv отчета, но его в формате указан с электронного обнаружения Справочник по модели данных (EDRM). Дополнительные сведения о EDRM перейдите к [https://www.edrm.net](https://www.edrm.net).</span><span class="sxs-lookup"><span data-stu-id="d6b50-p108">**Manifest.xml** A manifest file (in XML format) that contains information about each item included in the search results. The information in this report is the same as the Results.csv report, but it's in the format specified by the Electronic Discovery Reference Model (EDRM). For more information about EDRM, go to [https://www.edrm.net](https://www.edrm.net).</span></span>
    
 <span data-ttu-id="d6b50-158">**Когда следует отключить Экспорт этих отчетов?**</span><span class="sxs-lookup"><span data-stu-id="d6b50-158">**When should I disable exporting these reports?**</span></span>
  
<span data-ttu-id="d6b50-p109">Он зависит от конкретных потребностей. Многие организации не требуются дополнительные сведения о результатах поиска, а не требуется этих отчетов.</span><span class="sxs-lookup"><span data-stu-id="d6b50-p109">It depends on your specific needs. Many organizations don't require additional information about search results, and don't need these reports.</span></span>
  
 <span data-ttu-id="d6b50-161">**Какой компьютер следует сделать это в?**</span><span class="sxs-lookup"><span data-stu-id="d6b50-161">**What computer do I have to do this on?**</span></span>
  
 <span data-ttu-id="d6b50-162">Необходимо изменить значение параметра реестра на локальном компьютере, которую можно запускать средство экспорта Office 365 обнаружения электронных данных на.</span><span class="sxs-lookup"><span data-stu-id="d6b50-162">You have to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span> 
  
 <span data-ttu-id="d6b50-163">**После изменения этого параметра, необходимо перезагрузить компьютер?**</span><span class="sxs-lookup"><span data-stu-id="d6b50-163">**After I change this setting, do I have to restart the computer?**</span></span>
  
<span data-ttu-id="d6b50-p110">Нет, не требуется перезагрузка компьютера. Однако если выполняется средство экспорта eDiscovery Office 365, необходимо закрыть его и запустите ее снова после изменения параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="d6b50-p110">No, you don't have to restart the computer. But if the Office 365 eDiscovery Export tool is running, you have to close it and then restart it after you change the registry setting.</span></span>
  
 <span data-ttu-id="d6b50-166">**Получите изменить существующий раздел реестра или создается новый ключ?**</span><span class="sxs-lookup"><span data-stu-id="d6b50-166">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="d6b50-p111">Раздел реестра создается при первом запуске REG-файл, созданный в процедуру, описанную в этом разделе. Выберите параметр изменяется каждый раз, изменять и повторно запустить файл Правка.</span><span class="sxs-lookup"><span data-stu-id="d6b50-p111">A new registry key is created the first time you run the .reg file that you created in the procedure in this topic. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
