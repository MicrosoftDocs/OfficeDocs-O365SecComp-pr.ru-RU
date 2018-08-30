---
title: Подготовка данных для Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 2fb94c23-1846-4a0e-994d-da6d02445f15
description: 'Сведения об использовании безопасности Office 365 &amp; центре соответствия требованиям для подготовки данные Office 365 для анализа с Office 365 расширенного обнаружения электронных данных. '
ms.openlocfilehash: cf0c76b0c274121da435de7829c769abf5111cab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535241"
---
# <a name="prepare-data-for-office-365-advanced-ediscovery"></a><span data-ttu-id="d15ce-103">Подготовка данных для Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d15ce-103">Prepare data for Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="d15ce-104">В этом разделе описывается, как загрузить результаты поиска контента в к варианту в расширенной обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="d15ce-104">This topic describes how to load the results of a Content Search in to a case in Advanced eDiscovery.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d15ce-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="d15ce-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="step-1-prepare-office-365-data-for-advanced-ediscovery"></a><span data-ttu-id="d15ce-107">Шаг 1: Подготовьте данные Office 365 для расширенной обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="d15ce-107">Step 1: Prepare Office 365 data for Advanced eDiscovery</span></span>

<span data-ttu-id="d15ce-108">Для анализа данных с помощью расширенных обнаружения электронных данных, можно использовать результаты поиска контента, которую можно запускать в Office 365 безопасность &amp; центре соответствия требованиям (в списке на странице **поиска контента** в Office 365 безопасность &amp; центре соответствия требованиям) для поиска связанные с вариантом eDiscovery (в списке на странице **электронных данных** в безопасности &amp; центре соответствия требованиям).</span><span class="sxs-lookup"><span data-stu-id="d15ce-108">To analyze data with Advanced eDiscovery, you can use the results of a Content Search that you run in the Office 365 Security &amp; Compliance Center (listed on the **Content search** page in the Office 365 Security &amp; Compliance Center) or a search associated with an eDiscovery case (listed on the **eDiscovery** page in the Security &amp; Compliance Center).</span></span> 
  
<span data-ttu-id="d15ce-109">Подробное описание шагов по подготовке результатов поиска для анализа в расширенной обнаружения электронных данных Просмотр [результатов поиска Prepare Office 365 расширенного обнаружения электронных данных](prepare-search-results-for-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="d15ce-109">For the detailed steps on preparing search results for analysis in Advanced eDiscovery, see [Prepare search results for Office 365 Advanced eDiscovery](prepare-search-results-for-advanced-ediscovery.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="d15ce-110">Если данные за пределами Office 365 и необходимо импортировать его в Office 365, чтобы подготовить и анализ в расширенной eDiscovery, см. [Обзор Импорт PST-файлов в Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) и [Архивация данных сторонних производителей в Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).</span><span class="sxs-lookup"><span data-stu-id="d15ce-110">If you have data outside of Office 365 and want to import it to Office 365 so that you can prepare and analyze it in Advanced eDiscovery, a see [Overview of importing PST files to Office 365](https://support.office.com/article/ba688e0a-0fcb-4bd7-8e57-2b669564ea84) and [Archiving third-party data in Office 365](https://go.microsoft.com/fwlink/p/?linkid=716918).</span></span> 
  
## <a name="step-2-load-search-result-data-in-to-a-case-in-advanced-ediscovery"></a><span data-ttu-id="d15ce-111">Шаг 2: Нагрузки результатов данных поиска в к варианту в расширенной обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="d15ce-111">Step 2: Load search result data in to a case in Advanced eDiscovery</span></span>

<span data-ttu-id="d15ce-p102">После подготовки результатов поиска в системы &amp; центре соответствия требованиям для анализа, следующим шагом является загрузка результатов поиска в к варианту в расширенной обнаружения электронных данных. [Модуль процесса](run-the-process-module-in-advanced-ediscovery.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="d15ce-p102">After you prepare the search results in the Security &amp; Compliance Center for analysis, the next step is to load the search results in to a case in Advanced eDiscovery. For more detailed information, see [Run the Process module](run-the-process-module-in-advanced-ediscovery.md).</span></span>
  
1. <span data-ttu-id="d15ce-114">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="d15ce-114">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="d15ce-115">Войдите в Office 365 с помощью учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="d15ce-115">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="d15ce-116">В разделе Безопасность &amp; центре соответствия требованиям, нажмите кнопку **поиска &amp; расследования** \> **обнаружения электронных данных** для отображения списка случаев в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="d15ce-116">In the Security &amp; Compliance Center, click **Search &amp; investigation** \> **eDiscovery** to display the list of cases in your organization.</span></span> 
    
4. <span data-ttu-id="d15ce-117">Рядом с пунктом регистр, которую требуется загрузка данных в в расширенной обнаружения электронных данных, нажмите кнопку **Открыть** .</span><span class="sxs-lookup"><span data-stu-id="d15ce-117">Click **Open** next to the case that you want to load data in to in Advanced eDiscovery.</span></span> 
    
5. <span data-ttu-id="d15ce-118">На **домашней** странице для случая нажмите кнопку **Дополнительно обнаружения электронных данных**.</span><span class="sxs-lookup"><span data-stu-id="d15ce-118">On the **Home** page for the case, click **Advanced eDiscovery**.</span></span> 
    
    ![Щелкните переключатель расширенное eDiscovery для открытия в случае в расширенной обнаружения электронных данных](media/8e34ba23-62e3-4e68-a530-b6ece39b54be.png)
  
    <span data-ttu-id="d15ce-p103">Отображается индикатор **подключения к расширенной обнаружения электронных данных** . При подключении к расширенной обнаружения электронных данных на странице Настройка для случая отображается список контейнеров.</span><span class="sxs-lookup"><span data-stu-id="d15ce-p103">The **Connecting to Advanced eDiscovery** progress bar is displayed. When you're connected to Advanced eDiscovery, a list of containers is displayed on the setup page for the case.</span></span> 
    
    ![Регистр отображается в расширенной обнаружения электронных данных](media/8036e152-70dc-4bb7-9379-61c1ed8326b4.png)
  
     <span data-ttu-id="d15ce-p104">Эти контейнеры представляют результаты поиска, подготовленного для анализа в расширенной обнаружения электронных данных на шаге 1. Обратите внимание, что имя контейнера совпадает с именем поиска контента в случае в системы &amp; центре соответствия требованиям. Контейнеры в списке являются из них подготовленные. Если другой пользователь подготовлено результатов поиска для расширенной обнаружения электронных данных, соответствующих контейнеров не включены в список.</span><span class="sxs-lookup"><span data-stu-id="d15ce-p104">These containers represent the search results that you prepared for analysis in Advanced eDiscovery in Step 1. Note that the name of the container has the same name as the Content Search in the case in the Security &amp; Compliance Center. The containers in the list are the ones that you prepared. If a different user prepared search results for Advanced eDiscovery, the corresponding containers won't be included in the list.</span></span> 
    
6. <span data-ttu-id="d15ce-127">Для загрузки данных результатов поиска из контейнера в к варианту в расширенной eDiscovery, выберите контейнер и нажмите кнопку **процесса**.</span><span class="sxs-lookup"><span data-stu-id="d15ce-127">To load the search result data from a container in to the case in Advanced eDiscovery, select a container and then click **Process**.</span></span>
    
<span data-ttu-id="d15ce-128">После результатов поиска из безопасности &amp; центре соответствия требованиям добавляются в рамках данного экземпляра в расширенной eDiscovery следующим шагом является использование средств в расширенной обнаружения электронных данных для анализа и исключает данные, относящиеся к регистр, направленными.</span><span class="sxs-lookup"><span data-stu-id="d15ce-128">After the search results from the Security &amp; Compliance Center are added to the case in Advanced eDiscovery, the next step is to use the tools in Advanced eDiscovery to analyze and cull the data that's relevant to the case.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d15ce-129">См. также</span><span class="sxs-lookup"><span data-stu-id="d15ce-129">See also</span></span>

[<span data-ttu-id="d15ce-130">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d15ce-130">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="d15ce-131">Настройка параметров пользователей и случаи</span><span class="sxs-lookup"><span data-stu-id="d15ce-131">Set up users and cases</span></span>](set-up-users-and-cases-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d15ce-132">Анализ данных вариантов</span><span class="sxs-lookup"><span data-stu-id="d15ce-132">Analyzing case data</span></span>](analyze-case-data-with-advanced-ediscovery.md)
  
[<span data-ttu-id="d15ce-133">Управление релевантностью программы установки</span><span class="sxs-lookup"><span data-stu-id="d15ce-133">Managing Relevance setup</span></span>](manage-relevance-setup-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d15ce-134">С помощью модуля релевантности</span><span class="sxs-lookup"><span data-stu-id="d15ce-134">Using the Relevance module</span></span>](use-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d15ce-135">Экспорт данных вариантов</span><span class="sxs-lookup"><span data-stu-id="d15ce-135">Exporting case data</span></span>](export-case-data-in-advanced-ediscovery.md)

