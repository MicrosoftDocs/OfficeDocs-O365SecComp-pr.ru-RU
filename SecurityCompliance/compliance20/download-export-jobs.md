---
title: Скачивание заданий экспорта
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Установка и использование обозревателя хранилищ Azure для скачивания документов, экспортированных из набора проверки в Advanced eDiscovery.
ms.openlocfilehash: f236f53be9dda88fe5b8448011aa651603e38182
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/07/2019
ms.locfileid: "36231044"
---
# <a name="download-export-jobs"></a><span data-ttu-id="14b39-103">Скачивание заданий экспорта</span><span class="sxs-lookup"><span data-stu-id="14b39-103">Download export jobs</span></span>

<span data-ttu-id="14b39-104">При экспорте документов из набора проверки в расширенном случае обнаружения электронных данных документы передаются в предоставленное корпорацией Майкрософт место хранения Azure или в место хранения Azure, управляемое вашей организацией.</span><span class="sxs-lookup"><span data-stu-id="14b39-104">When you export documents from a review set in an Advanced eDiscovery case, the documents are uploaded to a Microsoft-provided Azure Storage location or to an Azure Storage location managed by your organization.</span></span> <span data-ttu-id="14b39-105">Тип используемого расположения хранилища Azure зависит от того, какой параметр был выбран при экспорте документов.</span><span class="sxs-lookup"><span data-stu-id="14b39-105">The type of Azure Storage location used depends on which option was selected when the documents were exported.</span></span> 

<span data-ttu-id="14b39-106">В этой статье приведены инструкции по использованию обозревателя хранилищ Microsoft Azure для подключения к хранилищу Azure для просмотра и скачивания экспортированных документов.</span><span class="sxs-lookup"><span data-stu-id="14b39-106">This article provides instructions for how to use the Microsoft Azure Storage Explorer to connect to an Azure Storage location to browse and download the exported documents.</span></span> <span data-ttu-id="14b39-107">Дополнительные сведения об обозревателе хранилищ Azure можно найти в статье [Краткое руководство: use Azure Storage Explorer](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer).</span><span class="sxs-lookup"><span data-stu-id="14b39-107">For more information about Azure Storage Explorer, see [Quickstart: Use Azure Storage Explorer](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer).</span></span>

## <a name="step-1-install-the-azure-storage-explorer"></a><span data-ttu-id="14b39-108">Шаг 1: Установка обозревателя хранилищ Azure</span><span class="sxs-lookup"><span data-stu-id="14b39-108">Step 1: Install the Azure Storage Explorer</span></span>

<span data-ttu-id="14b39-109">Первый шаг — скачать и установить Обозреватель хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="14b39-109">The first step is to download and install the Azure Storage Explorer.</span></span> <span data-ttu-id="14b39-110">Для получения инструкций обратитесь к разделу [средство "Обозреватель хранилищ Azure](https://go.microsoft.com/fwlink/p/?LinkId=544842)".</span><span class="sxs-lookup"><span data-stu-id="14b39-110">For instructions, see [Azure Storage Explorer tool](https://go.microsoft.com/fwlink/p/?LinkId=544842).</span></span> <span data-ttu-id="14b39-111">Это средство используется для подключения к и скачивания экспортированных документов на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="14b39-111">You use this tool to connect to and download the exported documents in Step 3.</span></span>

## <a name="step-2-obtain-the-sas-url-from-the-export-job"></a><span data-ttu-id="14b39-112">Шаг 2: получение URL-адреса SAS из задания экспорта</span><span class="sxs-lookup"><span data-stu-id="14b39-112">Step 2: Obtain the SAS URL from the export job</span></span>

<span data-ttu-id="14b39-113">Следующий шаг — получение URL-адреса общего доступа к подписи доступа (SAS), созданного при создании задания экспорта для [экспорта документов из набора рецензирования](export-documents-from-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="14b39-113">The next step is to obtain the shared access signature (SAS) URL that's generated when you created the export job to [export documents from a review set](export-documents-from-review-set.md).</span></span> <span data-ttu-id="14b39-114">Вы можете скопировать URL-адрес SAS для документов, которые передаются в хранилище Azure, предоставленное Майкрософт, или место хранения Azure, управляемое вашей организацией.</span><span class="sxs-lookup"><span data-stu-id="14b39-114">You can copy the SAS URL for documents that are uploaded to a Microsoft-provided Azure Storage location or an Azure Storage location managed by your organization.</span></span> <span data-ttu-id="14b39-115">В любом случае URL-адрес SAS используется для подключения к расположению хранилища Azure на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="14b39-115">In either case, you use the SAS URL to connect to the Azure Storage location in Step 3.</span></span>

1. <span data-ttu-id="14b39-116">На странице **Advanced eDiscovery (дополнительные функции обнаружения электронных** данных) перейдите к случаю, \*\*\*\* а затем перейдите на вкладку экспорты.</span><span class="sxs-lookup"><span data-stu-id="14b39-116">On the **Advanced eDiscovery** page, go to the case, and then click the **Exports** tab.</span></span>

2. <span data-ttu-id="14b39-117">На вкладке " **Экспорт** " щелкните задание экспорта, которое нужно скачать.</span><span class="sxs-lookup"><span data-stu-id="14b39-117">On the **Exports** tab, click the export job that you want to download.</span></span>

3. <span data-ttu-id="14b39-118">На всплывающей странице в разделе **расположения**скопируйте отображаемый URL-адрес SAS.</span><span class="sxs-lookup"><span data-stu-id="14b39-118">On the flyout page, under **Locations**, copy the SAS URL that's displayed.</span></span> <span data-ttu-id="14b39-119">При необходимости вы можете сохранить его в файл, чтобы получить к нему доступ на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="14b39-119">If necessary, you can save it to a file so you can access it in Step 3.</span></span>
 
   ![Копирование URL-адреса SAS, отображаемого в разделе расположения](../media/eDiscoExportJob.png)

## <a name="step-3-connect-to-the-azure-storage-location"></a><span data-ttu-id="14b39-121">Шаг 3: подключение к хранилищу Azure</span><span class="sxs-lookup"><span data-stu-id="14b39-121">Step 3: Connect to the Azure Storage location</span></span>

<span data-ttu-id="14b39-122">Последним шагом является использование обозревателя хранилищ Azure и URL-адреса SAS для подключения к расположению хранилища Azure и загрузки документов, экспортированных на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="14b39-122">The final step is to use the Azure Storage Explorer and the SAS URL to connect to the Azure Storage location and download the documents that you exported to a local computer.</span></span>

1.  <span data-ttu-id="14b39-123">Откройте оснастку Azure Storage Explorer, установленную на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="14b39-123">Open the Azure Storage Explorer that you installed in Step 1.</span></span>

2. <span data-ttu-id="14b39-124">Щелкните значок **Добавить учетную запись** .</span><span class="sxs-lookup"><span data-stu-id="14b39-124">Click the **Add account** icon.</span></span> <span data-ttu-id="14b39-125">Кроме того, можно щелкнуть правой кнопкой мыши **учетные записи хранения**.</span><span class="sxs-lookup"><span data-stu-id="14b39-125">Alternatively, you can right-click **Storage Accounts**.</span></span>

   ![Щелкните значок "добавить учетную запись"](../media/AzureStorageConnect.png)

3.  <span data-ttu-id="14b39-127">На странице " **Подключение к хранилищу Azure** " щелкните **использовать универсальный код ресурса (URI) для подписи общего доступа (SAS)** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="14b39-127">On the **Connect to Azure Storage** page, click **Use a shared access signature (SAS) URI** and then click **Next**.</span></span>

    ![Щелкните использовать универсальный код ресурса (URI) для подписи общего доступа (SAS), а затем нажмите кнопку Далее](../media/AzureStorageConnect2.png)

4.  <span data-ttu-id="14b39-129">На странице " **присоединение с URI SAS** " щелкните в поле URI и вставьте URL-адрес SAS, полученный на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="14b39-129">On the **Attach with SAS URI** page, click in the URI box, and then paste the SAS URL that you obtained in Step 2.</span></span> 

    ![Вставьте URL-адрес SAS в поле URI](../media/AzureStorageConnect3.png)

    <span data-ttu-id="14b39-131">Обратите внимание, что часть URL-адреса SAS отображается в поле **Отображаемое имя** .</span><span class="sxs-lookup"><span data-stu-id="14b39-131">Notice that a portion of the SAS URL is displayed in the **Display name** box.</span></span> <span data-ttu-id="14b39-132">Он будет использоваться в качестве отображаемого имени контейнера, созданного в **учетных записях хранения** после подключения к месту хранения.</span><span class="sxs-lookup"><span data-stu-id="14b39-132">This will be used as the display name of the container that's created under the **Storage accounts** after you connect to the storage location.</span></span> <span data-ttu-id="14b39-133">Это имя состоит из идентификатора расширенного случая обнаружения электронных данных и уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="14b39-133">This name consists of the ID of the Advanced eDiscovery case is from and a unique identifier.</span></span> <span data-ttu-id="14b39-134">Вы можете оставить отображаемое имя по умолчанию или изменить его.</span><span class="sxs-lookup"><span data-stu-id="14b39-134">You can keep the default display name or change it.</span></span> <span data-ttu-id="14b39-135">Если изменить его, отображаемое имя должно быть уникальным.</span><span class="sxs-lookup"><span data-stu-id="14b39-135">If you change it, the display name must be unique.</span></span>

5.  <span data-ttu-id="14b39-136">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="14b39-136">Click **Next**.</span></span>

    <span data-ttu-id="14b39-137">Отобразится страница " **Сводка подключения** ".</span><span class="sxs-lookup"><span data-stu-id="14b39-137">The **Connection summary** page is displayed.</span></span>
   
    ![Нажмите кнопку подключиться на странице сводки подключения, чтобы подключиться к хранилищу Azure.](../media/AzureStorageConnect4.png)

6. <span data-ttu-id="14b39-139">На странице **Сводка** по подключению просмотрите сведения о подключении, а затем нажмите кнопку **подключить**.</span><span class="sxs-lookup"><span data-stu-id="14b39-139">On the **Connection summary** page, review the connection information, and then click **Connect**.</span></span> 

    <span data-ttu-id="14b39-140">Будет открыт узел **контейнеры больших двоичных объектов** (в разделе **учетные записи** > хранения **(прикрепленные контейнеры)** \> .</span><span class="sxs-lookup"><span data-stu-id="14b39-140">The **Blob containers** node (under **Storage Accounts** > **(Attached Containers)** \> is opened.</span></span> 

    ![](../media/AzureStorageConnect5.png)

    <span data-ttu-id="14b39-141">Он содержит контейнер с именем, отображаемым на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="14b39-141">It contains a container named with the display name from step 4.</span></span> <span data-ttu-id="14b39-142">Этот контейнер содержит папку для каждого созданного задания экспорта.</span><span class="sxs-lookup"><span data-stu-id="14b39-142">This container contains a folder for each export job that you've created.</span></span> <span data-ttu-id="14b39-143">Имена этих папок с ИДЕНТИФИКАТОРом, соответствующим ИДЕНТИФИКАТОРу задания экспорта.</span><span class="sxs-lookup"><span data-stu-id="14b39-143">These folders are named with an ID that corresponds to the ID of the export job.</span></span> <span data-ttu-id="14b39-144">Эти коды экспорта (и имя экспорта) можно найти в разделе **сведения о поддержке** на всплывающей странице для каждого **подготовить данные для задания экспорта** , указанного на вкладке **задания** .</span><span class="sxs-lookup"><span data-stu-id="14b39-144">You can find these export IDs (and the name of the export) under **Support information** on the flyout page for each **Preparing data for export** job listed on the **Jobs** tab.</span></span>

7. <span data-ttu-id="14b39-145">Дважды щелкните папку задания экспорта, чтобы открыть ее.</span><span class="sxs-lookup"><span data-stu-id="14b39-145">Double-click the export job folder to open it.</span></span>

   <span data-ttu-id="14b39-146">Отобразится список папок и отчетов экспорта.</span><span class="sxs-lookup"><span data-stu-id="14b39-146">A list of folders and export reports is displayed.</span></span>
   
    ![Папка Export содержит экспортированные файлы и отчеты об экспорте](../media/AzureStorageConnect6.png)

   <span data-ttu-id="14b39-148">Папка заданий экспорта содержит указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="14b39-148">The export job folder contains the following items.</span></span> <span data-ttu-id="14b39-149">Фактические элементы в папке экспорта определяются параметрами экспорта, настроенными при создании задания экспорта.</span><span class="sxs-lookup"><span data-stu-id="14b39-149">The actual items in the export folder are determined by the export options configured when the export job was created.</span></span> <span data-ttu-id="14b39-150">Дополнительные сведения см в разделе [Экспорт документов из набора рецензирования](export-documents-from-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="14b39-150">For more information, see [Export documents from a review set](export-documents-from-review-set.md).</span></span>

    - <span data-ttu-id="14b39-151">Export_load_file. csv: этот CSV-файл представляет собой подробный отчет о экспорте, который содержит сведения о каждом экспортированном документе.</span><span class="sxs-lookup"><span data-stu-id="14b39-151">Export_load_file.csv: This CSV file is a detail export report that contains information about each exported document.</span></span> <span data-ttu-id="14b39-152">Файл состоит из столбца для каждого свойства метаданных документа.</span><span class="sxs-lookup"><span data-stu-id="14b39-152">The file consists of a column for each metadata property for a document.</span></span> <span data-ttu-id="14b39-153">Список и описание метаданных, включенных в этот отчет, представлены в столбце **имя экспортируемого поля** в таблице в [полях метаданные документа в разделе Advanced eDiscovery](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="14b39-153">For a list and description of the metadata that's included in this report, see the **Exported field name** column in the table in [Document metadata fields in Advanced eDiscovery](document-metadata-fields.md).</span></span>
    
    - <span data-ttu-id="14b39-154">Summary. txt: текстовый файл, содержащий сводку по экспорту, включая статистику экспорта.</span><span class="sxs-lookup"><span data-stu-id="14b39-154">Summary.txt: A text file that contains a summary of the export including export statistics.</span></span>
    
    - <span data-ttu-id="14b39-155">Extracted_text_files: в этой папке содержится текстовый файл каждого экспортированного документа.</span><span class="sxs-lookup"><span data-stu-id="14b39-155">Extracted_text_files: This folder contains a text file version of each exported document.</span></span>
     
    - <span data-ttu-id="14b39-156">Нативефилес: в этой папке содержится собственная версия каждого экспортированного документа.</span><span class="sxs-lookup"><span data-stu-id="14b39-156">NativeFiles: This folder contains a native file version of each exported document.</span></span>
    
    - <span data-ttu-id="14b39-157">Error_files: в этой папке содержатся следующие элементы, если задание экспорта содержит какие бы то ни было файлы ошибок:</span><span class="sxs-lookup"><span data-stu-id="14b39-157">Error_files: This folder includes the following items when the export job contains any error files:</span></span> 
        
      - <span data-ttu-id="14b39-158">Екстрактионеррор. csv: этот CSV-файл содержит доступные метаданные для файлов, которые не были правильно извлечены из родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="14b39-158">ExtractionError.csv: This CSV file contains the available metadata for files that weren't properly extracted from their parent item.</span></span>
        
      - <span data-ttu-id="14b39-159">Процессинжеррор: в этой папке содержатся документы с ошибками обработки.</span><span class="sxs-lookup"><span data-stu-id="14b39-159">ProcessingError: This folder contains documents with processing errors.</span></span> <span data-ttu-id="14b39-160">Это содержимое находится на уровне элемента, что означает, что при возникновении ошибки обработки вложения в эту папку также будет включен документ, содержащий вложение.</span><span class="sxs-lookup"><span data-stu-id="14b39-160">This content is at an item level, which means if an attachment had a processing error, the document that contains the attachment will also be included in this folder.</span></span>
 
8. <span data-ttu-id="14b39-161">Чтобы экспортировать все содержимое в экспорте, выберите папку экспорт и нажмите кнопку **загрузить**.</span><span class="sxs-lookup"><span data-stu-id="14b39-161">To export all contents in the export, select the export folder, and then click **Download**.</span></span>

9. <span data-ttu-id="14b39-162">Укажите расположение, в которое вы хотите скачать экспортируемые файлы, а затем нажмите кнопку Выбрать папку.</span><span class="sxs-lookup"><span data-stu-id="14b39-162">Specify the location where you want to download the exported files, and then click Select folder.</span></span>

    <span data-ttu-id="14b39-163">В обозревателе службы хранилища Azure запускается процесс экспорта.</span><span class="sxs-lookup"><span data-stu-id="14b39-163">The Azure Storage Explorer starts the export process.</span></span> <span data-ttu-id="14b39-164">Состояние скачивания экспортированных элементов отображается в области **действия** .</span><span class="sxs-lookup"><span data-stu-id="14b39-164">The status of the downloading the exported items is displayed in the **Activities** pane.</span></span> <span data-ttu-id="14b39-165">По завершении скачивания отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="14b39-165">A message is displayed when the download is finished.</span></span>

    ![После завершения скачивания отображается сообщение](../media/AzureStorageConnect8.png)

> [!NOTE]
> <span data-ttu-id="14b39-167">Вместо того чтобы скачивать все задания экспорта, можно выбрать определенные элементы для скачивания.</span><span class="sxs-lookup"><span data-stu-id="14b39-167">Instead of downloading the entire export job, you can select specific items to download.</span></span> <span data-ttu-id="14b39-168">А вместо скачивания элементов можно дважды щелкнуть элемент, чтобы просмотреть его.</span><span class="sxs-lookup"><span data-stu-id="14b39-168">And instead of downloading items, you can double-click an item to view it.</span></span>