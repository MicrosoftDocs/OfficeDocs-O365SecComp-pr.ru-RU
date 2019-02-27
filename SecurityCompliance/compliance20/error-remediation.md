---
title: Исправление ошибок при обработке данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: bf48e605dc321da4b7a9d5343d18f90fbb179073
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296732"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="5fed9-102">Исправление ошибок при обработке данных</span><span class="sxs-lookup"><span data-stu-id="5fed9-102">Error remediation when processing data</span></span>

<span data-ttu-id="5fed9-p101">Устранение ошибок позволяет администраторам eDiscovery изменять проблемы с данными, которые предотвращают неправильное обработку содержимого с помощью расширенного обнаружения электронных данных (Предварительная версия). Например, файлы, защищенные паролем, не могут быть обработаны, так как файлы заблокированы или зашифрованы. С помощью исправления ошибок администраторы обнаружения электронных данных могут загружать файлы с такими ошибками, удалять парольную защиту и отправлять исправленные файлы.</span><span class="sxs-lookup"><span data-stu-id="5fed9-p101">Error remediation allows eDiscovery administrators the ability to rectify data issues which prevent Advanced eDiscovery (Preview) from properly processing the content. For example, files that are password protected cannot be processed since the files are locked or encrypted. Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="5fed9-106">Используйте следующий рабочий процесс для исправления файлов с ошибками в дополнительных случаях обнаружения электронных данных (Предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="5fed9-106">Use the following workflow to remediate files with errors in Advanced eDiscovery (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="5fed9-107">Создание сеанса исправления ошибок для исправления файлов с ошибками обработки</span><span class="sxs-lookup"><span data-stu-id="5fed9-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="5fed9-108">Если мастер исправления ошибок закрыт в любой момент во время выполнения следующей процедуры, вы можете вернуться к сеансу исправления ошибок на вкладке **Обработка** , выбрав в раскрывающемся меню **вид** параметр " **исправления ошибок** ".</span><span class="sxs-lookup"><span data-stu-id="5fed9-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="5fed9-109">На вкладке **Обработка** в расширенном варианте EDiscovery (Предварительная версия) выберите **ошибки** в раскрывающемся меню **вид** .</span><span class="sxs-lookup"><span data-stu-id="5fed9-109">On the **Processing** tab in an Advanced eDiscovery (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="5fed9-p102">Выберите подлежащие исправлению ошибки, нажав переключатель рядом с типом ошибки или типом файла.  В следующем примере мы устранение файл, защищенный паролем.</span><span class="sxs-lookup"><span data-stu-id="5fed9-p102">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.  In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="5fed9-112">Нажмите кнопку **+ новое исправление ошибок**.</span><span class="sxs-lookup"><span data-stu-id="5fed9-112">Click **+ New error remediation**.</span></span>

    ![Исправление ошибок](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="5fed9-114">Начнется сеанс исправления ошибок, начиная с стадии подготовки, в которой файлы с ошибками перемещаются в безопасное расположение Azure для скачивания.</span><span class="sxs-lookup"><span data-stu-id="5fed9-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![Подготовка исправления ошибок](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="5fed9-116">После завершения подготовки нажмите кнопку **Далее: Загрузка файлов** для продолжения загрузки.</span><span class="sxs-lookup"><span data-stu-id="5fed9-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Загрузка файлов](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="5fed9-p103">Чтобы скачать файлы, укажите **целевой путь для скачивания**; Это путь к локальному компьютеру, на который необходимо скачать файл.  Путь по умолчанию,%Усерпрофиле%\довнлоадс\еррорс, указывает на папку загрузок пользователя, вошедшего в систему; При необходимости его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="5fed9-p103">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.  The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="5fed9-120">Для оптимальной производительности рекомендуется использовать локальный путь к файлу вместо удаленного сетевого пути.</span><span class="sxs-lookup"><span data-stu-id="5fed9-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5fed9-121">Если вы не установили AzCopy, вы можете установить его отсюда:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="5fed9-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="5fed9-p104">Скопируйте предопределенную команду, нажав кнопку **Копировать в буфер обмена**. Запустите командную строку Windows, вставьте команду и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="5fed9-p104">Copy the predefined command by clicking **Copy to clipboard**. Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="5fed9-124">Файлы будут скачаны.</span><span class="sxs-lookup"><span data-stu-id="5fed9-124">The files will be downloaded.</span></span>

    ![Подготовка исправления ошибок](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > <span data-ttu-id="5fed9-126">Если у вас возникли проблемы с выполнением https://go.microsoft.com/fwlink/?linkid=2038117 этой команды, ознакомьтесь с советами по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="5fed9-126">If you have issues running this command, see https://go.microsoft.com/fwlink/?linkid=2038117 for troubleshooting tips.</span></span>

7. <span data-ttu-id="5fed9-p105">После загрузки файлов вы можете исправить их с помощью соответствующего средства. Для файлов, защищенных паролем, можно использовать несколько средств взлома паролей. Если вы знаете пароли этих файлов, вы можете открыть их и удалить защиту паролем.</span><span class="sxs-lookup"><span data-stu-id="5fed9-p105">After downloading the files, you can remediate them with an appropriate tool. For password protected files, there are a number of password cracking tools you can use. If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="5fed9-p106">Важно сохранить структуру каталогов и имена файлов исправленных файлов без изменений.  Все соглашения об именовании, используемые в скачанных файлах и папках, делают возможным сопоставление файлов ремдиатед с оригиналом.</span><span class="sxs-lookup"><span data-stu-id="5fed9-p106">IT is important that you retain the directory structure and file names of the remediated files in tact.  All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="5fed9-p107">Теперь вернитесь к расширенному eDiscovery (Предварительная версия) и нажмите кнопку **Далее: Отправка файлов**.  Это приведет к переходу на следующий шаг, на котором можно отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="5fed9-p107">Now, return to Advanced eDiscovery (Preview) and click **Next: Upload files**.  This will move to the next step where you can now upload the files.</span></span>

    ![Отправка файлов](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="5fed9-135">Укажите расположение исправленных файлов в текстовом поле **путь к расположению файлов** , а затем нажмите кнопку **Копировать в клибпбоард**.</span><span class="sxs-lookup"><span data-stu-id="5fed9-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="5fed9-136">Вставьте команду в командную строку Windows и нажмите клавишу **Ввод** , чтобы отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="5fed9-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="5fed9-138">Наконец, вернитесь к расширенному eDiscovery (Предварительная версия) и нажмите кнопку **Далее: обработка файлов**.</span><span class="sxs-lookup"><span data-stu-id="5fed9-138">Finally, return to Advanced eDiscovery (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="5fed9-p108">По завершении обработки.  Вы можете вернуться к рабочему набору и просмотреть исправленный файл.</span><span class="sxs-lookup"><span data-stu-id="5fed9-p108">When processing is complete.  You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="5fed9-141">Что происходит при исправлении файлов</span><span class="sxs-lookup"><span data-stu-id="5fed9-141">What happens when files are remediated</span></span>

<span data-ttu-id="5fed9-142">При отправке исправленных файлов исходные метаданные сохраняются с исключением следующих полей:</span><span class="sxs-lookup"><span data-stu-id="5fed9-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="5fed9-143">Документекстрактедурл</span><span class="sxs-lookup"><span data-stu-id="5fed9-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="5fed9-144">Екстрактедтекстсизе</span><span class="sxs-lookup"><span data-stu-id="5fed9-144">ExtractedTextSize</span></span>
- <span data-ttu-id="5fed9-145">Хастекст</span><span class="sxs-lookup"><span data-stu-id="5fed9-145">HasText</span></span>
- <span data-ttu-id="5fed9-146">Исеррорремедиате</span><span class="sxs-lookup"><span data-stu-id="5fed9-146">IsErrorRemediate</span></span>
- <span data-ttu-id="5fed9-147">Испарентекстрактедурл</span><span class="sxs-lookup"><span data-stu-id="5fed9-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="5fed9-148">Итемекстрактедурл</span><span class="sxs-lookup"><span data-stu-id="5fed9-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="5fed9-149">Лоадид</span><span class="sxs-lookup"><span data-stu-id="5fed9-149">LoadId</span></span>
- <span data-ttu-id="5fed9-150">Процессинжеррормессаже</span><span class="sxs-lookup"><span data-stu-id="5fed9-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="5fed9-151">Процессингстатус</span><span class="sxs-lookup"><span data-stu-id="5fed9-151">ProcessingStatus</span></span>
- <span data-ttu-id="5fed9-152">Текст</span><span class="sxs-lookup"><span data-stu-id="5fed9-152">Text</span></span>
- <span data-ttu-id="5fed9-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="5fed9-153">WordCount</span></span>
- <span data-ttu-id="5fed9-154">Воркингсетид</span><span class="sxs-lookup"><span data-stu-id="5fed9-154">WorkingsetId</span></span>

<span data-ttu-id="5fed9-155">Определение всех полей метаданных документа в Advanced eDiscovery (Предварительная версия) приведено в разделе [поля метаданных документа](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="5fed9-155">For a definition of all document metadata fields in Advanced eDiscovery (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>