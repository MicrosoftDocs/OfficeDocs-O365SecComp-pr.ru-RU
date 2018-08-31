---
title: Увеличение скорости при экспорте результаты поиска обнаружения электронных данных из Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Сведения о настройке реестра Windows для повышения пропускной способности данных при загрузке результатов поиска и поиска данных из безопасности Office 365 &amp; центре соответствия требованиям и Office 365 расширенное обнаружения электронных данных.
ms.openlocfilehash: 3f456f5ee0312d4d4d7b95f868520e6756a90fd1
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535506"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a><span data-ttu-id="6e4b1-103">Увеличение скорости при экспорте результаты поиска обнаружения электронных данных из Office 365</span><span class="sxs-lookup"><span data-stu-id="6e4b1-103">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>

<span data-ttu-id="6e4b1-p101">При использовании средства Office 365 обнаружения электронных данных экспорта можно загрузить результаты поиска контента в Office 365 безопасность &amp; центре соответствия требованиям или файл для загрузки данных из Office 365 Advanced электронного обнаружения, средство запускает определенное количество параллельных экспорта операции для загрузки данных на локальном компьютере. По умолчанию число одновременных операций значение 8 раз число ядер на компьютере, используемом для загрузки данных. К примеру при наличии Двухъядерный процессор компьютера (то есть два центральных процессоров на одной микросхемы), по умолчанию число параллельных экспортирования равно 16. Чтобы повысить пропускную способность передачи данных и ускорить процесс загрузки, можно увеличить количество одновременных операций, настроив параметр реестра Windows на компьютере, на котором вы можете загрузить результаты поиска. Чтобы ускорить процесс загрузки рекомендуется начать с параметром 24 одновременных операций.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-p101">When you use the Office 365 eDiscovery Export tool to download the results of a Content Search in the Office 365 Security &amp; Compliance Center or download data from Office 365 Advanced eDiscovery, the tool starts a certain number of concurrent export operations to download the data to your local computer. By default, the number of concurrent operations is set to 8 times the number of cores in the computer you're using to download the data. For example, if you have a dual core computer (meaning two central processing units on one chip), the default number of concurrent export operations is 16. To increase the data transfer throughput and speed-up the download process, you can increase the number of concurrent operations by configuring a Windows Registry setting on the computer that you use to download the search results. To speed-up the download process, we recommend that you start with a setting of 24 concurrent operations.</span></span>
  
<span data-ttu-id="6e4b1-p102">Если загрузить результаты поиска по низкой пропускной способностью сети, увеличение значения этого параметра может негативно сказывается. Кроме того можно увеличить параметр, чтобы более 24 одновременных операций в высокой пропускной способностью сети (максимальное количество одновременных операций — 512). После настройки этот параметр реестра, может потребоваться изменить его найти оптимальное количество одновременных операций для вашей среды.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-p102">If you download search results over a low-bandwidth network, increasing this setting might have a negative impact. Alternatively, you might be able to increase the setting to more than 24 concurrent operations in a high-bandwidth network (the maximum number of concurrent operations is 512). After you configure this registry setting, you might have to change it to find the optimal number of concurrent operations for your environment.</span></span>
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a><span data-ttu-id="6e4b1-112">Создайте параметр реестра, чтобы изменить количество одновременных операций при экспорте данных</span><span class="sxs-lookup"><span data-stu-id="6e4b1-112">Create a registry setting to change the number of concurrent operations when exporting data</span></span>

<span data-ttu-id="6e4b1-113">Выполните следующую процедуру на компьютере, который используется для загрузки результатов поиска из безопасности &amp; центре соответствия требованиям или данных из расширенных обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-113">Perform the following procedure on the computer that you'll use to download search results from the Security &amp; Compliance Center or data from Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="6e4b1-114">Если открыта, закройте средство экспорта eDiscovery Office 365.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-114">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="6e4b1-115">Сохраните следующий текст в файл реестра окна с помощью суффикса имени файла в формате REG; Например ConcurrentOperations.reg.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-115">Save the following text to a Window registry file by using a filename suffix of .reg; for example, ConcurrentOperations.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    <span data-ttu-id="6e4b1-116">В предыдущем описано, мы рекомендуем начать с 24 параллельные операции, а затем изменение этого параметра соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-116">As previous explained, we recommend that you start with 24 concurrent operations, and then change this setting as appropriate.</span></span>
    
3. <span data-ttu-id="6e4b1-117">В проводнике Windows щелкните или дважды щелкните REG-файл, созданный на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-117">In Windows Explorer, click or double-click the .reg file that you created in the previous step.</span></span>
    
4. <span data-ttu-id="6e4b1-118">В окне Управление доступом пользователей, нажмите кнопку **Да** для перехода на редактор реестра.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-118">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="6e4b1-119">Чтобы продолжить, нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-119">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="6e4b1-120">В редакторе реестра отображается появится сообщение о том, что параметр был успешно добавлен в реестр.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-120">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
6. <span data-ttu-id="6e4b1-121">Повторите шаги 2 – 5 для изменения значения для `DownloadConcurrency` параметр реестра.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-121">You can repeat steps 2 - 5 to change the value for the  `DownloadConcurrency` registry setting.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6e4b1-p103">После создания или изменения `DownloadConcurrency` реестра, убедитесь, что для создания нового задания экспорта или перезапуск существующие задания экспорта результатов поиска или данные, которые нужно загрузить. В разделе [Дополнительные сведения](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-p103">After you create or change the  `DownloadConcurrency` registry setting, be sure to create a new export job or restart an existing export job for the search results or data that you want to download. See the [More information](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) section for more details.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="6e4b1-124">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="6e4b1-124">More information</span></span>

- <span data-ttu-id="6e4b1-p104">При первом запуске REG-файл, созданный в этой процедуре создается новый раздел реестра. Затем `DownloadConcurrency` параметр реестра изменяется каждый раз, изменять и повторно запустить файл Правка.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-p104">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the  `DownloadConcurrency` registry setting is edited each time you change and re-run the .reg edit file.</span></span> 
    
- <span data-ttu-id="6e4b1-p105">Средство экспорта eDiscovery Office 365 использует [Azure AzCopy служебной программы](https://go.microsoft.com/fwlink/?linkid=849949) для загрузки данных поиска из безопасности &amp; центре соответствия требованиям или из расширенных обнаружения электронных данных. Настройка `DownloadConcurrency` параметр реестра аналогичен с помощью параметра **/NC** при запуске программы AzCopy. Поэтому параметр реестра из `"DownloadConcurrency=24"` должен использовать тот же эффект, что и использование значения параметра `/NC:24` с помощью служебной программы AzCopy.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-p105">The Office 365 eDiscovery Export tool uses the [Azure AzCopy utility](https://go.microsoft.com/fwlink/?linkid=849949) to download search data from the Security &amp; Compliance Center or from Advanced eDiscovery. Configuring the  `DownloadConcurrency` registry setting is similar to using the **/NC** parameter when running the AzCopy utility. So the registry setting of  `"DownloadConcurrency=24"` would have the same effect as using the parameter value of  `/NC:24` with the AzCopy utility.</span></span> 
    
- <span data-ttu-id="6e4b1-p106">Если остановить экспорта файл для загрузки, который в данный момент находится в стадии разработки и запустите ее снова (при попытке повторно загрузить результаты поиска), средство экспорта eDiscovery Office 365 пытается возобновить же загрузки. Таким образом, если запустить файл для загрузки, остановить его, а затем измените `DownloadConcurrency` реестра установка, загрузка может привести к ошибкам при перезагрузке (щелкнув **файл для загрузки экспортировать результаты**). Это средство экспорта будет пытаться возобновить предыдущей загрузки, с помощью параметров, которых нет действительного из-за изменения параметров реестра.</span><span class="sxs-lookup"><span data-stu-id="6e4b1-p106">If you stop an export download that's currently in progress and then restart it (by trying to download the search results again), the Office 365 eDiscovery Export tool will attempt to resume the same download. So, if you start a download, stop it, and then change the  `DownloadConcurrency` registry setting, the download will probably fail if you restart it (by clicking **Download exported results**). This is because the export tool will attempt to resume the previous download using settings that aren't valid because you changed the registry setting.</span></span>
    
    <span data-ttu-id="6e4b1-p107">Таким образом, после того, как изменить `DownloadConcurrency` реестра, не забудьте перезапустить задания экспорта (щелкнув **перезапустите экспорта**) в безопасности &amp; центре соответствия требованиям. Затем можно загрузить экспортированного результатов. Дополнительные сведения о Экспорт результатов поиска и данных можно:</span><span class="sxs-lookup"><span data-stu-id="6e4b1-p107">Therefore, after you change the  `DownloadConcurrency` registry setting, be sure to restart the export job (by clicking **Restart export**) in the Security &amp; Compliance Center. Then you can download the exported results. For more information about exporting search results and data, see:</span></span>
    
  - [<span data-ttu-id="6e4b1-136">Экспорт результатов поиска контента из безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="6e4b1-136">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
  - [<span data-ttu-id="6e4b1-137">Экспорт результатов в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6e4b1-137">Export results in Office 365 Advanced eDiscovery</span></span>](export-results-in-advanced-ediscovery.md)
    
