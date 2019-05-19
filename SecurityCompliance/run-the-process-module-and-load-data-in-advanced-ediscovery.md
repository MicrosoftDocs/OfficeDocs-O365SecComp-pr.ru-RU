---
title: Запуск модуля процесса и загрузка данных в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Узнайте, как использовать центр соответствия требованиям безопасности &amp; Office 365 для доступа к Office 365 Advanced eDiscovery и запуска модуля Process для случая.  '
ms.openlocfilehash: 89a4be9bf56f35d9d9cbd88494bcae5a5a10fe7a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157021"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="00199-103">Запуск модуля процесса и загрузка данных в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="00199-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="00199-p101">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете [зарегистрироваться для получения пробной версии Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="00199-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="00199-106">В этом разделе описываются функциональные возможности модуля "расширенный процесс обнаружения электронных данных".</span><span class="sxs-lookup"><span data-stu-id="00199-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="00199-107">Кроме данных файлов, метаданные, такие как тип файла, расширение, расположение или путь, Дата и время создания, автор, хранитель и тема, могут быть загружены в Расширенное обнаружение электронных данных и сохранены для каждого случая.</span><span class="sxs-lookup"><span data-stu-id="00199-107">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case.</span></span> <span data-ttu-id="00199-108">Некоторые метаданные рассчитываются с помощью расширенного обнаружения электронных данных, например при загрузке собственных файлов.</span><span class="sxs-lookup"><span data-stu-id="00199-108">Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="00199-109">Расширенные функции обнаружения электронных данных предоставляют значения системных метаданных, такие как почти повторяющиеся группы или показатели релевантности.</span><span class="sxs-lookup"><span data-stu-id="00199-109">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores.</span></span> <span data-ttu-id="00199-110">Администратор может добавить другие метаданные, например аннотации файлов.</span><span class="sxs-lookup"><span data-stu-id="00199-110">Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="00199-111">Запущенный процесс</span><span class="sxs-lookup"><span data-stu-id="00199-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="00199-112">Номера пакетов присваиваются файлу во время процесса, чтобы разрешить отслеживание файлов.</span><span class="sxs-lookup"><span data-stu-id="00199-112">Batch numbers are assigned to a file during Process to allow the tracking of files.</span></span> <span data-ttu-id="00199-113">Пакетный номер также позволяет идентифицировать пакеты процессов для параметров повторной обработки.</span><span class="sxs-lookup"><span data-stu-id="00199-113">The batch number also enables identification of Process batches for reprocessing options.</span></span> <span data-ttu-id="00199-114">Дополнительные фильтры доступны для фильтрации по номеру пакета и сеансам.</span><span class="sxs-lookup"><span data-stu-id="00199-114">Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="00199-115">Выполните указанные ниже действия, чтобы выполнить процесс.</span><span class="sxs-lookup"><span data-stu-id="00199-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="00199-116">[Откройте центр безопасности &amp; и соответствия требованиям Office 365](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="00199-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="00199-117">Перейдите к разделу \*\*Поиск &amp; \*\* \> с обнаружением **электронных** данных и нажмите кнопку **Перейти к расширенному eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="00199-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="00199-118">В разделе Расширенные функции обнаружения электронных данных выберите соответствующее обращение на странице отображаемые **варианты** и нажмите кнопку **Перейти к регистру**.</span><span class="sxs-lookup"><span data-stu-id="00199-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="00199-119">В окне **Подготовка** \> **процесса** \> **установки**выберите контейнер из списка доступных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="00199-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Нажмите кнопку процесс, чтобы добавить результаты поиска в обращение.](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="00199-121">Нажмите **Дополнительные параметры...** , если вы хотите добавить контейнер в качестве начальных файлов или в качестве файлов, помеченных как готовые.</span><span class="sxs-lookup"><span data-stu-id="00199-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="00199-122">Используйте начальные файлы для ускорения обучения проблем с низким уровнем насыщенности (обычно не более 2%).</span><span class="sxs-lookup"><span data-stu-id="00199-122">Use seed files to accelerate training for issues with low richness (usually 2%, or less).</span></span> <span data-ttu-id="00199-123">Для начальных файлов рекомендуется выбирать разнообразные файлы и обрабатывать их по 20-50 для каждой из них (слишком большое число начальных файлов может исказить результаты релевантности).</span><span class="sxs-lookup"><span data-stu-id="00199-123">For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results).</span></span> <span data-ttu-id="00199-124">Начальные файлы должны быть проверены одним и тем же человеком, который будет обучать эту ошибку.</span><span class="sxs-lookup"><span data-stu-id="00199-124">Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="00199-125">Используйте файлы, помеченные предварительно тегами, для автоматизации обучения релевантности.</span><span class="sxs-lookup"><span data-stu-id="00199-125">Use pre-tagged files to automate Relevance training.</span></span> <span data-ttu-id="00199-126">Необходимо отметить по крайней мере 1 500 файлов и сохранить пропорции релевантности для нерелевантных файлов таким же образом, как и в коллекции, добавленной к релевантности.</span><span class="sxs-lookup"><span data-stu-id="00199-126">You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance.</span></span> <span data-ttu-id="00199-127">Эти файлы следует замечать вручную, и вы должны быть уверены в качестве тегов.</span><span class="sxs-lookup"><span data-stu-id="00199-127">These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Снимок экрана со страницей дополнительных параметров для обработки пакетных файлов](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="00199-129">В разделе **SEED** :</span><span class="sxs-lookup"><span data-stu-id="00199-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="00199-130">Нажмите **Пометить как начальные файлы** , чтобы пометить контейнер как начальные файлы.</span><span class="sxs-lookup"><span data-stu-id="00199-130">Choose **Mark as seed files** to mark the container as seed files.</span></span> <span data-ttu-id="00199-131">Кроме того, в раскрывающемся списке **для устранения неполадок** необходимо назначить их для каждой из них.</span><span class="sxs-lookup"><span data-stu-id="00199-131">You also need choose to assign them per issue from the **For issue** drop-down.</span></span> <span data-ttu-id="00199-132">Выберите один \*\*\*\* из вариантов в раскрывающемся списке **тегов** или **не имеет отношения** .</span><span class="sxs-lookup"><span data-stu-id="00199-132">Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="00199-133">После того как вы задаете файлы как начальные, вы не сможете пометить их как **предварительно помеченные**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="00199-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="00199-134">В разделе **файлы с тегами** :</span><span class="sxs-lookup"><span data-stu-id="00199-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="00199-135">Выберите пункт пометить **как предварительно помеченные файлы** , чтобы пометить контейнер как файлы, помеченные как готовые.</span><span class="sxs-lookup"><span data-stu-id="00199-135">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files.</span></span> <span data-ttu-id="00199-136">Их также необходимо назначить в раскрывающемся списке **для устранения неполадок** .</span><span class="sxs-lookup"><span data-stu-id="00199-136">You also need to assign them per issue from the **For issue** drop-down.</span></span> <span data-ttu-id="00199-137">Выберите один \*\*\*\* из вариантов в раскрывающемся списке **тегов** или **не имеет отношения** .</span><span class="sxs-lookup"><span data-stu-id="00199-137">Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="00199-138">После того как вы задаете файлы в виде **предварительных тегов**, их нельзя пометить как **начальные**.</span><span class="sxs-lookup"><span data-stu-id="00199-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="00199-139">В разделе " **теги электронной почты** ".</span><span class="sxs-lookup"><span data-stu-id="00199-139">In the **Email tagging** section.</span></span> <span data-ttu-id="00199-140">Укажите, какая часть обработанного сообщения должна быть помечена как начальная или предварительно помеченная.</span><span class="sxs-lookup"><span data-stu-id="00199-140">set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="00199-141">Чтобы начать, нажмите кнопку **процесс**.</span><span class="sxs-lookup"><span data-stu-id="00199-141">To begin, click **Process**.</span></span> <span data-ttu-id="00199-142">По завершении отображаются результаты процесса.</span><span class="sxs-lookup"><span data-stu-id="00199-142">When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="00199-143">Необязательно Если вам нужно назначить источники данных определенному хранитель, вы можете добавлять и изменять имена хранитель в **custodians** \> **управления** и назначать custodians в **custodians** \> **Assign**.</span><span class="sxs-lookup"><span data-stu-id="00199-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="00199-144">Если вы добавляете к этому случаю, вы можете обработать его еще раз.</span><span class="sxs-lookup"><span data-stu-id="00199-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00199-145">См. также</span><span class="sxs-lookup"><span data-stu-id="00199-145">See also</span></span>

[<span data-ttu-id="00199-146">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="00199-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="00199-147">Просмотр результатов модуля процесса</span><span class="sxs-lookup"><span data-stu-id="00199-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

