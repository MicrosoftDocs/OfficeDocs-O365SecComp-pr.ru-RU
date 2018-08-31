---
title: Запуск модуля обработки и загрузка данных в Office 365 Advanced eDiscovery
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Сведения об использовании безопасности Office 365 &amp; центре соответствия требованиям для доступа к Office 365 расширенного обнаружения электронных данных и запуска модуля процесса для обращения.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534858"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="b1b03-103">Запуск модуля обработки и загрузка данных в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b1b03-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="b1b03-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="b1b03-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="b1b03-106">В этом разделе описываются функциональные возможности модуля процесса расширенной обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="b1b03-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="b1b03-p102">В дополнение к данным файл метаданных, такие как тип файлов, расширение, расположение или путь, Дата создания и время, автора, custodian и темы, могут быть загружены в расширенного обнаружения электронных данных и сохранения для каждого случая. Некоторые метаданные рассчитывается по расширенной eDiscovery, например при загрузке собственный файлов.</span><span class="sxs-lookup"><span data-stu-id="b1b03-p102">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case. Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="b1b03-p103">Расширенные eDiscovery предоставляет системы значения метаданных, например группирование почти повторяющиеся или показателям релевантности. Можно добавить других метаданных, например файл аннотации администратором.</span><span class="sxs-lookup"><span data-stu-id="b1b03-p103">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores. Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="b1b03-111">Запуск процесса</span><span class="sxs-lookup"><span data-stu-id="b1b03-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="b1b03-p104">Чтобы разрешить отслеживание файлы назначаются номера пакета в файл во время процесса. Номер пакета также позволяет Идентификация обработка пакетов для повторной обработки параметров. Для фильтрации, номер партии и сеансы доступны дополнительные фильтры.</span><span class="sxs-lookup"><span data-stu-id="b1b03-p104">Batch numbers are assigned to a file during Process to allow the tracking of files. The batch number also enables identification of Process batches for reprocessing options. Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="b1b03-115">Выполните следующие действия, чтобы запустить процесс.</span><span class="sxs-lookup"><span data-stu-id="b1b03-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="b1b03-116">[Откройте безопасности Office 365 &amp; центре соответствия требованиям](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="b1b03-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="b1b03-117">Последовательно выберите пункты **поиска &amp; расследования** \> **обнаружения электронных данных** и нажмите кнопку **Перейти к расширенной обнаружения электронных данных**.</span><span class="sxs-lookup"><span data-stu-id="b1b03-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="b1b03-118">В расширенной eDiscovery выберите соответствующий регистр в отображаемой страницы **случаев** и нажмите кнопку **Перейти на случай**.</span><span class="sxs-lookup"><span data-stu-id="b1b03-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="b1b03-119">В статье **Prepare** \> **процесс** \> **программы установки**, выберите контейнер из списка доступных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="b1b03-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Щелкните процесс, чтобы добавить результаты поиска в рамках данного экземпляра](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="b1b03-121">Нажмите кнопку **Дополнительные параметры...** , если вы хотите добавить в контейнер как файлы начального значения или как предварительно с тегами файлы.</span><span class="sxs-lookup"><span data-stu-id="b1b03-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="b1b03-p105">Использовать файлы начального значения для ускорения обучающие курсы по проблемы с низкой расширение (обычно % 2, или меньше). Для файлов, начального значения, рекомендуется выбрать различные явно соответствующие файлы и обработки о исходные значения 20-50 на проблему (слишком много файлов начального значения можно изменяют релевантности результатов). Начальное значение файлы следует изучить с одного человека, который будет обучение пользователей проблему.</span><span class="sxs-lookup"><span data-stu-id="b1b03-p105">Use seed files to accelerate training for issues with low richness (usually 2%, or less). For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results). Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="b1b03-p106">Используйте предварительно с тегами файлы для автоматизации учебный курс по релевантности. Следует отметить по крайней мере 1 500 файлы и сохранить пропорции относится к не соответствующие файлы такой же, как увеличить значимость коллекции. Эти файлы должны быть вручную с тегами и должны быть уверенным в качестве тегов.</span><span class="sxs-lookup"><span data-stu-id="b1b03-p106">Use pre-tagged files to automate Relevance training. You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance. These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Снимок экрана Дополнительные параметры страницы для обработки файлов пакета](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="b1b03-129">В разделе **начального значения** :</span><span class="sxs-lookup"><span data-stu-id="b1b03-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="b1b03-p107">Выберите **Пометить как файлы начальное значение** для контейнера отметить как файлы начального значения. Вы также должны выбрать назначать их на проблему с **проблемы** раскрывающемся списке. Выберите из раскрывающегося списка **тег** **Relevant** или **не соответствующие** .</span><span class="sxs-lookup"><span data-stu-id="b1b03-p107">Choose **Mark as seed files** to mark the container as seed files. You also need choose to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b1b03-133">После установки файлов в качестве **начального значения**их нельзя пометить как **предварительно с меткой**.</span><span class="sxs-lookup"><span data-stu-id="b1b03-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="b1b03-134">В разделе **предварительно с тегами файлы** :</span><span class="sxs-lookup"><span data-stu-id="b1b03-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="b1b03-p108">Выберите **Пометить как предварительно с тегами файлы** пометку контейнер, предварительно с тегами файлы. Также необходимо назначить их на проблемы **по вопросам** раскрывающемся списке. Выберите из раскрывающегося списка **тег** **Relevant** или **не соответствующие** .</span><span class="sxs-lookup"><span data-stu-id="b1b03-p108">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files. You also need to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="b1b03-138">После установки файлов как **предварительно с меткой**, их нельзя пометить как **начального значения**.</span><span class="sxs-lookup"><span data-stu-id="b1b03-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="b1b03-p109">В разделе **тегов электронной почты** . набор, какую часть обработанные электронной почты, которую надо отметить как инициирующий или предварительно с тегами.</span><span class="sxs-lookup"><span data-stu-id="b1b03-p109">In the **Email tagging** section. set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="b1b03-p110">Чтобы приступить к работе, щелкните **процесс**. После завершения процесса результаты отображаются.</span><span class="sxs-lookup"><span data-stu-id="b1b03-p110">To begin, click **Process**. When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="b1b03-143">(Необязательно) Если им необходимо назначить источников данных для конкретных custodian, можно добавлять и редактировать имена custodian в **Custodians** \> **Управление** и назначить custodians в **Custodians** \> **назначения**.</span><span class="sxs-lookup"><span data-stu-id="b1b03-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="b1b03-144">Если вы добавили в случае, затем можно обрабатывать еще раз.</span><span class="sxs-lookup"><span data-stu-id="b1b03-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b1b03-145">См. также</span><span class="sxs-lookup"><span data-stu-id="b1b03-145">See also</span></span>

[<span data-ttu-id="b1b03-146">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b1b03-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="b1b03-147">Просмотр результатов процесса модуля</span><span class="sxs-lookup"><span data-stu-id="b1b03-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

