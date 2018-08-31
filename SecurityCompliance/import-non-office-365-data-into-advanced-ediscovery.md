---
title: Импорт не связанного с Office 365 содержимого для анализа в Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 5/25/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OEC150
- MET150
ms.assetid: 0ee60763-a30b-495b-8543-971c3384a801
description: Как для действия для импорта контента, не сохраняются в O365 в Azure больших двоичных объектов, чтобы можно было проанализировать с AeD
ms.openlocfilehash: ab6c7ac76a159603a34719aa8edb51de3a4fabbb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535511"
---
# <a name="import-non-office-365-content-for-advanced-ediscovery-analysis"></a><span data-ttu-id="a76f2-103">Импорт не связанного с Office 365 содержимого для анализа в Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a76f2-103">Import non-Office 365 content for Advanced eDiscovery analysis</span></span>

<span data-ttu-id="a76f2-p101">Не все документы, которые может потребоваться при анализе с Office 365 расширенного обнаружения электронных данных будет live в Office 365. С содержимым без поддержки Office 365 импорта компонента в расширенной обнаружения электронных данных, можно публиковать документы, которые не live в Office 365 (за исключением PST-файлы) в большой двоичный объект вариантов хранения связанных, Azure и их анализ с помощью расширенных обнаружения электронных данных. Этой процедуре показано, как для переноса документов Office 365 в расширенной обнаружения электронных данных для анализа.</span><span class="sxs-lookup"><span data-stu-id="a76f2-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 (except PST files) into a case linked, Azure storage blob and analyze them with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a76f2-p102">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="a76f2-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a76f2-p103">Вы можете приобрести Office 365 расширенного электронного обнаружения данных хранилища дополнительный компонент подписка на Office 365 содержимого. Этот параметр доступен только для контента, которые следует проанализировать с расширенной обнаружения электронных данных. Выполните действия, описанные в [приобретение или изменить и надстройки для Office 365 для бизнеса](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) и Приобретите надстроек Office 365 Дополнительные хранилища обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="a76f2-p103">You can purchase an Office 365 Advanced eDiscovery data storage add-on subscription for your non-Office 365 content. This is exclusively available for content that is to be analyzed with Advanced eDiscovery. Follow the steps in [Buy or edit and add-on for Office 365 for business](https://support.office.com/article/Buy-or-edit-an-add-on-for-Office-365-for-business-4e7b57d6-b93b-457d-aecd-0ea58bff07a6) and purchase the Office 365 Advanced eDiscovery storage add-on.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="a76f2-112">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="a76f2-112">Before you begin</span></span>

<span data-ttu-id="a76f2-113">С помощью функции загрузки без поддержки Office 365, как описано в этой процедуры требуется, что у вас есть:</span><span class="sxs-lookup"><span data-stu-id="a76f2-113">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>
  
- <span data-ttu-id="a76f2-114">Office 365 E3 с E5 подписки или надстройка расширенное соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="a76f2-114">An Office 365 E3 with Advanced Compliance add-on or E5 subscription</span></span>
    
- <span data-ttu-id="a76f2-115">Все custodians, содержимое которого Office 365 будет отправлен необходимо E3 с дополнительный компонент Advanced соответствия или лицензии E5</span><span class="sxs-lookup"><span data-stu-id="a76f2-115">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses</span></span>
    
- <span data-ttu-id="a76f2-116">Существующие случая обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="a76f2-116">An existing eDiscovery case</span></span>
    
- <span data-ttu-id="a76f2-p104">Файлы для загрузки для сбора в папки, где существует отдельную папку для каждого custodian и имя папки, находится в этом формате *alias@domainname* . *Alias@domainname* должен быть псевдоним пользователей Office 365 и домен. Все папки *alias@domainname* можно объединить в корневую папку. В корневой папке может содержать только папки *alias@domainname* , должен существовать не свободные файлы в корневой папке</span><span class="sxs-lookup"><span data-stu-id="a76f2-p104">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format  *alias@domainname*  . The  *alias@domainname*  must be users Office 365 alias and domain. You can collect all the  *alias@domainname*  folders into a root folder. The root folder can only contain the  *alias@domainname*  folders, there must be no loose files in the root folder</span></span> 
    
- <span data-ttu-id="a76f2-121">Требуется учетная запись eDiscovery администратора или диспетчер обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="a76f2-121">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>
    
- <span data-ttu-id="a76f2-122">[Средства хранения данных Microsoft Azure](https://aka.ms/downloadazcopy) установлен на компьютере, который имеет доступ к структуре папок содержимого Office 365.</span><span class="sxs-lookup"><span data-stu-id="a76f2-122">[Microsoft Azure Storage Tools](https://aka.ms/downloadazcopy) installed on a computer that has access to the non-Office 365 content folder structure.</span></span> 
    
## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="a76f2-123">Office 365 содержимое загружается в расширенной обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="a76f2-123">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="a76f2-p105">Как eDiscovery Manager или eDiscovery администратора открывать **обнаружения электронных данных**и случай, который будет передан данные Office 365. Если вам нужно создать обращение, [Управление вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям](manage-ediscovery-cases.md)</span><span class="sxs-lookup"><span data-stu-id="a76f2-p105">As an eDiscovery Manager or eDiscovery Administrator, open **eDiscovery**, and open the case that the non-Office 365 data will be uploaded to. If you need to create a case, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md)</span></span>
    
2. <span data-ttu-id="a76f2-126">Щелкните **переключатель, позволяющий расширенной обнаружения электронных данных**</span><span class="sxs-lookup"><span data-stu-id="a76f2-126">Click **Switch to Advanced eDiscovery**</span></span>
    
3. <span data-ttu-id="a76f2-127">В разделе **Тип источника** выберите **данных без поддержки Office 365**.</span><span class="sxs-lookup"><span data-stu-id="a76f2-127">Under **Source type** select **Non-Office 365 data**.</span></span>
    
4. <span data-ttu-id="a76f2-p106">Нажмите кнопку **Добавить контейнера**. Имя контейнера и добавить описание.</span><span class="sxs-lookup"><span data-stu-id="a76f2-p106">Click **Add container**. Name the container and add a description.</span></span>
    
5. <span data-ttu-id="a76f2-130">Выберите только что добавленный контейнер в списке контейнера и скопируйте URL-адрес, который отображается в области сведений контейнер, а затем закройте области</span><span class="sxs-lookup"><span data-stu-id="a76f2-130">Select the newly added container from the container list and copy the URL that appears in the container details pane and then close the pane</span></span>
    
6. <span data-ttu-id="a76f2-131">Откройте командную строку с правами администратора и перейдите в каталог после установки AzCopy папки...</span><span class="sxs-lookup"><span data-stu-id="a76f2-131">Open a command prompt as an administrator and change directory to folder where you have AzCopy installed..</span></span>
    
7. <span data-ttu-id="a76f2-132">Создайте AzCopy командной строки для загрузки файлов следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a76f2-132">Construct the AzCopy command line to upload the files like this:</span></span>
    
    <span data-ttu-id="a76f2-p107">/ Source AzCopy:» *полный путь к корневой папке на локальном компьютере* "/Dest:» *контейнер URL-адрес копирования, но не включая?* " /DestSAS:» *оставшейся части формы контейнер URL-адреса? в конец* «/ S.</span><span class="sxs-lookup"><span data-stu-id="a76f2-p107">AzCopy /Source:" *full path to root folder on local machine*  " /Dest:"  *container URL up to but not including the ?*  " /DestSAS:"  *remainder of the container url from the ? to the end*  " /S.</span></span> 
    
    <span data-ttu-id="a76f2-135">Например с помощью следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a76f2-135">For example, using these values:</span></span> 
    
  - <span data-ttu-id="a76f2-136">корневой папки - C:\Collected данных</span><span class="sxs-lookup"><span data-stu-id="a76f2-136">root folder - C:\Collected Data</span></span> 
    
  - <span data-ttu-id="a76f2-137">URL-адрес контейнер - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp; sr = c&amp;si = NonOfficeData15 %7 C 0&amp;подпись = Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA % 3D</span><span class="sxs-lookup"><span data-stu-id="a76f2-137">container url - https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D</span></span>
    
    <span data-ttu-id="a76f2-138">синтаксис командной строки AzCopy будет следующим:</span><span class="sxs-lookup"><span data-stu-id="a76f2-138">the AzCopy command line syntax would be:</span></span>
    
     `AzCopy /Source:"C:\CollectedData" /Dest:"https://zoomsabcprodeuss114.blob.core.windows.net/ingestion53d059efe5f74784afb308f66cdebf17" /DestSAS:"?sv=2015-04-05&amp;sr=c&amp;si=NonOfficeData15%7C0&amp;sig=Bk5INP8CUfv1y4CSJiJl3pJt3Ekvu8GS3P8NkOvoQxA%3D" /S`
    
    <span data-ttu-id="a76f2-139">Для получения дополнительных сведений о Azcopy просмотреть синтаксис, [Передача данных с AzCopy на Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span><span class="sxs-lookup"><span data-stu-id="a76f2-139">For more information on Azcopy syntax see, [Transfer data with the AzCopy on Windows](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy) .</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="a76f2-140">Должен быть один корневую папку каждого пользователя и имя папки должно быть в формате *alias@domainname* .</span><span class="sxs-lookup"><span data-stu-id="a76f2-140">There must be one root folder per user and the folder name must be in the  *alias@domainname*  format.</span></span> 
  
8. <span data-ttu-id="a76f2-p108">После завершения папки передачи данных, переключитесь обратно в расширенной обнаружения электронных данных. Содержимое папки, загруженный готов для обработки в расширенной обнаружения электронных данных. Выберите контейнер и нажмите кнопку процесса. Для получения дополнительных сведений о расширенных eDiscovery отображаются обработки, [запустите модуль процесса и загрузка данных в Office 365 расширенного обнаружения электронных данных](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="a76f2-p108">Once the folders have finished uploading, switch back to Advanced eDiscovery. The content in the folders you uploaded is now ready to be processed in Advanced eDiscovery. Select the container and click the Process button. For more details on Advanced eDiscovery Processing see, [Run the Process module and load data in Office 365 Advanced eDiscovery](run-the-process-module-and-load-data-in-advanced-ediscovery.md)</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="a76f2-p109">После контейнер успешно обработан в расширенной обнаружения электронных данных, который больше не смогут для добавления нового контента в хранилище SAS в Azure. Если сбор дополнительное содержимое и нужно добавить для случая для анализа расширенной обнаружения электронных данных, необходимо создать новый контейнер **данных без поддержки Office 365** и повторите эту процедуру.</span><span class="sxs-lookup"><span data-stu-id="a76f2-p109">Once the container is successfully processed in Advanced eDiscovery, you will no longer be able to add new content to the SAS storage in Azure. If you collect additional content and you want to add it to the case for Advanced eDiscovery analysis, you must create a new **Non-Office 365 data** container and repeat this procedure.</span></span> 
  
    > [!NOTE]
    > <span data-ttu-id="a76f2-147">Если контейнер, *не выполняет успешно из-за проблемы именования папки* и затем устранить проблемы, будет по-прежнему необходимо создать новый контейнер и повторное подключение и отправьте еще раз с помощью процедур, описанных в этой статье.</span><span class="sxs-lookup"><span data-stu-id="a76f2-147">If the container  *does not process successfully due to folder naming issues*  and you then fix the issues, you will still have to create a new container and the reconnect and upload again using the procedures in this article.</span></span> 
  

