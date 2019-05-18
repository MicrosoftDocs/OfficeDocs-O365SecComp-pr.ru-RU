---
title: Устранение ошибок при обработке данных для расследования
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
description: ''
ms.openlocfilehash: bca6967fd99696ffb4b610105e448011b9837be4
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150861"
---
# <a name="error-remediation-when-processing-data-for-an-investigation"></a><span data-ttu-id="13c57-102">Устранение ошибок при обработке данных для расследования</span><span class="sxs-lookup"><span data-stu-id="13c57-102">Error remediation when processing data for an investigation</span></span>

<span data-ttu-id="13c57-103">Устранение ошибок позволяет проанализировать проблемы с данными, которые предотвращают неправильное обработку контента при расследовании данных (Предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="13c57-103">Error remediation allows investigators the ability to rectify data issues which prevent Data Investigations (Preview) from properly processing the content.</span></span> <span data-ttu-id="13c57-104">Например, файлы, защищенные паролем, не могут быть обработаны, так как файлы заблокированы или зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="13c57-104">For example, files that are password protected cannot be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="13c57-105">При исправлении ошибок средства исследования могут загружать файлы с такими ошибками, удалять парольную защиту и отправлять исправленные файлы.</span><span class="sxs-lookup"><span data-stu-id="13c57-105">Using error remediation, investigators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="13c57-106">Используйте следующий рабочий процесс для исправления файлов с ошибками в случаях расследования данных (Preview).</span><span class="sxs-lookup"><span data-stu-id="13c57-106">Use the following workflow to remediate files with errors in Data Investigations (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="13c57-107">Создание сеанса исправления ошибок для исправления файлов с ошибками обработки</span><span class="sxs-lookup"><span data-stu-id="13c57-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="13c57-108">Если мастер исправления ошибок закрыт в любой момент во время выполнения следующей процедуры, вы можете вернуться к сеансу исправления ошибок на вкладке **Обработка** , выбрав в раскрывающемся меню **вид** параметр " **исправления ошибок** ".</span><span class="sxs-lookup"><span data-stu-id="13c57-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="13c57-109">На вкладке **Обработка** в варианте расследования данных (Предварительная версия) выберите **ошибки** в раскрывающемся меню **вид** .</span><span class="sxs-lookup"><span data-stu-id="13c57-109">On the **Processing** tab in an Data Investigations (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="13c57-110">Выберите подлежащие исправлению ошибки, нажав переключатель рядом с типом ошибки или типом файла.</span><span class="sxs-lookup"><span data-stu-id="13c57-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="13c57-111">В следующем примере мы устранение файл, защищенный паролем.</span><span class="sxs-lookup"><span data-stu-id="13c57-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="13c57-112">Нажмите кнопку **+ новое исправление ошибок**.</span><span class="sxs-lookup"><span data-stu-id="13c57-112">Click **+ New error remediation**.</span></span>

    ![Исправление ошибок](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="13c57-114">Начнется сеанс исправления ошибок, начиная с стадии подготовки, в которой файлы с ошибками перемещаются в безопасное расположение Azure для скачивания.</span><span class="sxs-lookup"><span data-stu-id="13c57-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![Подготовка исправления ошибок](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="13c57-116">После завершения подготовки нажмите кнопку **Далее: Загрузка файлов** для продолжения загрузки.</span><span class="sxs-lookup"><span data-stu-id="13c57-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Загрузка файлов](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="13c57-118">Чтобы скачать файлы, укажите **целевой путь для скачивания**; Это путь к локальному компьютеру, на который необходимо скачать файл.</span><span class="sxs-lookup"><span data-stu-id="13c57-118">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.</span></span>  <span data-ttu-id="13c57-119">Путь по умолчанию,%Усерпрофиле%\довнлоадс\еррорс, указывает на папку загрузок пользователя, вошедшего в систему; При необходимости его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="13c57-119">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="13c57-120">Для оптимальной производительности рекомендуется использовать локальный путь к файлу вместо удаленного сетевого пути.</span><span class="sxs-lookup"><span data-stu-id="13c57-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13c57-121">Если вы не установили AzCopy, вы можете установить его отсюда:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="13c57-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="13c57-122">Скопируйте предопределенную команду, нажав кнопку **Копировать в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="13c57-122">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="13c57-123">Запустите командную строку Windows, вставьте команду и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="13c57-123">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="13c57-124">Файлы будут скачаны.</span><span class="sxs-lookup"><span data-stu-id="13c57-124">The files will be downloaded.</span></span>

    ![Подготовка исправления ошибок](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > <span data-ttu-id="13c57-126">Если у вас возникли проблемы с выполнением https://go.microsoft.com/fwlink/?linkid=2038117 этой команды, ознакомьтесь с советами по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="13c57-126">If you have issues running this command, see https://go.microsoft.com/fwlink/?linkid=2038117 for troubleshooting tips.</span></span>

7. <span data-ttu-id="13c57-127">После загрузки файлов вы можете исправить их с помощью соответствующего средства.</span><span class="sxs-lookup"><span data-stu-id="13c57-127">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="13c57-128">Для файлов, защищенных паролем, можно использовать несколько средств взлома паролей.</span><span class="sxs-lookup"><span data-stu-id="13c57-128">For password protected files, there are a number of password cracking tools you can use.</span></span> <span data-ttu-id="13c57-129">Если вы знаете пароли этих файлов, вы можете открыть их и удалить защиту паролем.</span><span class="sxs-lookup"><span data-stu-id="13c57-129">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="13c57-130">Важно сохранить структуру каталогов и имена файлов исправленных файлов без изменений.</span><span class="sxs-lookup"><span data-stu-id="13c57-130">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="13c57-131">Все соглашения об именовании, используемые в скачанных файлах и папках, делают возможным сопоставление файлов ремдиатед с оригиналом.</span><span class="sxs-lookup"><span data-stu-id="13c57-131">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="13c57-132">Теперь вернитесь к расследованию данных (Предварительная версия) и нажмите кнопку **Далее: Отправка файлов**.</span><span class="sxs-lookup"><span data-stu-id="13c57-132">Now, return to Data Investigations (Preview) and click **Next: Upload files**.</span></span>  <span data-ttu-id="13c57-133">Это приведет к переходу на следующий шаг, на котором можно отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="13c57-133">This will move to the next step where you can now upload the files.</span></span>

    ![Отправка файлов](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="13c57-135">Укажите расположение исправленных файлов в текстовом поле **путь к расположению файлов** , а затем нажмите кнопку **Копировать в клибпбоард**.</span><span class="sxs-lookup"><span data-stu-id="13c57-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="13c57-136">Вставьте команду в командную строку Windows и нажмите клавишу **Ввод** , чтобы отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="13c57-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="13c57-138">Наконец, вернитесь к расследованию данных (Предварительная версия) и нажмите кнопку **Далее: обработка файлов**.</span><span class="sxs-lookup"><span data-stu-id="13c57-138">Finally, return to Data Investigations (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="13c57-139">По завершении обработки.</span><span class="sxs-lookup"><span data-stu-id="13c57-139">When processing is complete.</span></span>  <span data-ttu-id="13c57-140">Вы можете вернуться к рабочему набору и просмотреть исправленный файл.</span><span class="sxs-lookup"><span data-stu-id="13c57-140">You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="13c57-141">Что происходит при исправлении файлов</span><span class="sxs-lookup"><span data-stu-id="13c57-141">What happens when files are remediated</span></span>

<span data-ttu-id="13c57-142">При отправке исправленных файлов исходные метаданные сохраняются с исключением следующих полей:</span><span class="sxs-lookup"><span data-stu-id="13c57-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="13c57-143">Документекстрактедурл</span><span class="sxs-lookup"><span data-stu-id="13c57-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="13c57-144">Екстрактедтекстсизе</span><span class="sxs-lookup"><span data-stu-id="13c57-144">ExtractedTextSize</span></span>
- <span data-ttu-id="13c57-145">HasText</span><span class="sxs-lookup"><span data-stu-id="13c57-145">HasText</span></span>
- <span data-ttu-id="13c57-146">Исеррорремедиате</span><span class="sxs-lookup"><span data-stu-id="13c57-146">IsErrorRemediate</span></span>
- <span data-ttu-id="13c57-147">Испарентекстрактедурл</span><span class="sxs-lookup"><span data-stu-id="13c57-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="13c57-148">Итемекстрактедурл</span><span class="sxs-lookup"><span data-stu-id="13c57-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="13c57-149">Лоадид</span><span class="sxs-lookup"><span data-stu-id="13c57-149">LoadId</span></span>
- <span data-ttu-id="13c57-150">Процессинжеррормессаже</span><span class="sxs-lookup"><span data-stu-id="13c57-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="13c57-151">Процессингстатус</span><span class="sxs-lookup"><span data-stu-id="13c57-151">ProcessingStatus</span></span>
- <span data-ttu-id="13c57-152">Текст</span><span class="sxs-lookup"><span data-stu-id="13c57-152">Text</span></span>
- <span data-ttu-id="13c57-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="13c57-153">WordCount</span></span>
- <span data-ttu-id="13c57-154">Воркингсетид</span><span class="sxs-lookup"><span data-stu-id="13c57-154">WorkingsetId</span></span>

<span data-ttu-id="13c57-155">Определение всех полей метаданных документа в исследованиях данных (Предварительная версия) приведено в разделе [поля метаданных документа](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="13c57-155">For a definition of all document metadata fields in Data Investigations (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>