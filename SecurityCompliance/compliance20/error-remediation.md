---
title: Исправление ошибок при обработке данных
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
ms.openlocfilehash: c9c2660929037430535c9b612218563c51b1f056
ms.sourcegitcommit: 3f3f3ecb28ef65d023f3573f9a4e09a0586d8f53
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2019
ms.locfileid: "36490796"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="97312-102">Исправление ошибок при обработке данных</span><span class="sxs-lookup"><span data-stu-id="97312-102">Error remediation when processing data</span></span>

<span data-ttu-id="97312-103">Устранение ошибок позволяет администраторам обнаружения электронных данных устранить проблемы с данными, которые предотвращают неправильное обработку содержимого для расширенного обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="97312-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="97312-104">Например, файлы, защищенные паролем, не могут быть обработаны, так как файлы заблокированы или зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="97312-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="97312-105">С помощью исправления ошибок администраторы обнаружения электронных данных могут загружать файлы с такими ошибками, удалять защиту паролем, а затем отправлять исправленные файлы.</span><span class="sxs-lookup"><span data-stu-id="97312-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="97312-106">Используйте следующий рабочий процесс для исправления файлов с ошибками в дополнительных случаях обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="97312-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="97312-107">Создание сеанса исправления ошибок для исправления файлов с ошибками обработки</span><span class="sxs-lookup"><span data-stu-id="97312-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="97312-108">Если мастер исправления ошибок закрыт в любой момент во время выполнения следующей процедуры, вы можете вернуться к сеансу исправления ошибок на вкладке **Обработка** , выбрав в раскрывающемся меню **вид** параметр " **исправления ошибок** ".</span><span class="sxs-lookup"><span data-stu-id="97312-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="97312-109">На вкладке **Обработка** в расширенном случае обнаружения электронных данных выберите **ошибки** в раскрывающемся меню **вид** .</span><span class="sxs-lookup"><span data-stu-id="97312-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop-down menu.</span></span>

2. <span data-ttu-id="97312-110">Выберите подлежащие исправлению ошибки, нажав переключатель рядом с типом ошибки или типом файла.</span><span class="sxs-lookup"><span data-stu-id="97312-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="97312-111">В следующем примере мы устранение файл, защищенный паролем.</span><span class="sxs-lookup"><span data-stu-id="97312-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="97312-112">Нажмите кнопку **новое исправление ошибок**.</span><span class="sxs-lookup"><span data-stu-id="97312-112">Click **New error remediation**.</span></span>

    ![Исправление ошибок](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="97312-114">Сеанс исправления ошибок начинается с стадии подготовки, в которой файлы с ошибками копируются в хранилище Azure, предоставленное корпорацией Майкрософт, чтобы их можно было загрузить на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="97312-114">The error remediation session starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![Подготовка исправления ошибок](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="97312-116">По завершении подготовки нажмите кнопку **Далее: Загрузка файлов** для продолжения загрузки.</span><span class="sxs-lookup"><span data-stu-id="97312-116">After the preparation is complete, click **Next: Download files** to proceed with download.</span></span>

    ![Загрузка файлов](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="97312-118">Чтобы скачать файлы, укажите **целевой путь для скачивания**.</span><span class="sxs-lookup"><span data-stu-id="97312-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="97312-119">Это путь к локальному компьютеру, на который загружается файл.</span><span class="sxs-lookup"><span data-stu-id="97312-119">This is a path on your local computer where the file is downloaded.</span></span>  <span data-ttu-id="97312-120">Путь по умолчанию,%Усерпрофиле%\довнлоадс\еррорс, указывает на папку загрузок пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="97312-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="97312-121">При необходимости вы можете изменить этот путь.</span><span class="sxs-lookup"><span data-stu-id="97312-121">You can change this path if necessary.</span></span> <span data-ttu-id="97312-122">Если вы сделаете это, рекомендуем использовать локальный путь к файлу для достижения оптимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="97312-122">If you do change it, we recommend that you use a local file path for the best performance.</span></span> <span data-ttu-id="97312-123">Не используйте удаленный сетевой путь.</span><span class="sxs-lookup"><span data-stu-id="97312-123">Don't use a remote network path.</span></span>

6. <span data-ttu-id="97312-124">Скопируйте предопределенную команду, нажав кнопку **Копировать в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="97312-124">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="97312-125">Запустите командную строку Windows, вставьте команду и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="97312-125">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="97312-126">Файлы будут скачаны.</span><span class="sxs-lookup"><span data-stu-id="97312-126">The files are downloaded.</span></span>

    ![Подготовка к исправлению ошибок](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="97312-128">Для успешного использования команды, указанной на странице **Загрузка файлов** , необходимо использовать AzCopy v 8.1.</span><span class="sxs-lookup"><span data-stu-id="97312-128">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="97312-129">Кроме того, для отправки файлов на шаге 10 необходимо использовать AzCopy v 8.1.</span><span class="sxs-lookup"><span data-stu-id="97312-129">You also must use AzCopy v8.1 to upload the files in step 10 below.</span></span> <span data-ttu-id="97312-130">Чтобы установить эту версию AzCopy, обратитесь к разделу [Transfer Data with a AzCopy v 8.1 в Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="97312-130">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="97312-131">Если предоставленная команда AzCopy не удалась, обратитесь к разделу [Устранение неполадок AzCopy в Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="97312-131">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="97312-132">После загрузки файлов вы можете исправить их с помощью соответствующего средства.</span><span class="sxs-lookup"><span data-stu-id="97312-132">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="97312-133">Для файлов, защищенных паролем, можно использовать несколько средств взлома паролей.</span><span class="sxs-lookup"><span data-stu-id="97312-133">For password-protected files, there several password cracking tools you can use.</span></span> <span data-ttu-id="97312-134">Если вы знаете пароли этих файлов, вы можете открыть их и удалить защиту паролем.</span><span class="sxs-lookup"><span data-stu-id="97312-134">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="97312-135">Важно сохранить структуру каталогов и имена файлов исправленных файлов.</span><span class="sxs-lookup"><span data-stu-id="97312-135">It's important that you retain the directory structure and file names of the remediated files.</span></span> <span data-ttu-id="97312-136">Пути к скачанным файлам и папкам позволяют сопоставить исправленные файлы с исходными файлами.</span><span class="sxs-lookup"><span data-stu-id="97312-136">The path names of the downloaded files and folders make it possible to associate the remediated files with the original files.</span></span>  <span data-ttu-id="97312-137">Если изменилась структура каталогов или имена файлов, появится следующее сообщение об ошибке: `Cannot apply Error Remediation to the current Workingset`.</span><span class="sxs-lookup"><span data-stu-id="97312-137">If the directory structure or file names are changed, you'll receive the following error: `Cannot apply Error Remediation to the current Workingset`.</span></span>

8. <span data-ttu-id="97312-138">Теперь вернитесь к расширенному eDiscovery и нажмите кнопку **Далее: отправить файлы**.</span><span class="sxs-lookup"><span data-stu-id="97312-138">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="97312-139">Это приведет к переходу на следующий шаг, на котором можно отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="97312-139">This will move to the next step where you can now upload the files.</span></span>

    ![Отправка файлов](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="97312-141">Укажите расположение исправленных файлов в текстовом поле **путь к расположению файлов** , а затем нажмите кнопку **Копировать в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="97312-141">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="97312-142">Вставьте команду в командную строку Windows и нажмите клавишу **Ввод** , чтобы отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="97312-142">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="97312-144">Вернитесь к расширенному eDiscovery и нажмите кнопку **Далее: обработка файлов**.</span><span class="sxs-lookup"><span data-stu-id="97312-144">Return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="97312-145">По завершении обработки.</span><span class="sxs-lookup"><span data-stu-id="97312-145">When processing is complete.</span></span> <span data-ttu-id="97312-146">Вы можете вернуться к набору проверки и просмотреть исправленный файл.</span><span class="sxs-lookup"><span data-stu-id="97312-146">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="97312-147">Что происходит при исправлении файлов</span><span class="sxs-lookup"><span data-stu-id="97312-147">What happens when files are remediated</span></span>

<span data-ttu-id="97312-148">При отправке исправленных файлов исходные метаданные сохраняются, за исключением следующих полей:</span><span class="sxs-lookup"><span data-stu-id="97312-148">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="97312-149">екстрактедтекстсизе</span><span class="sxs-lookup"><span data-stu-id="97312-149">ExtractedTextSize</span></span>
- <span data-ttu-id="97312-150">HasText</span><span class="sxs-lookup"><span data-stu-id="97312-150">HasText</span></span>
- <span data-ttu-id="97312-151">исеррорремедиате</span><span class="sxs-lookup"><span data-stu-id="97312-151">IsErrorRemediate</span></span>
- <span data-ttu-id="97312-152">лоадид</span><span class="sxs-lookup"><span data-stu-id="97312-152">LoadId</span></span>
- <span data-ttu-id="97312-153">процессинжеррормессаже</span><span class="sxs-lookup"><span data-stu-id="97312-153">ProcessingErrorMessage</span></span>
- <span data-ttu-id="97312-154">процессингстатус</span><span class="sxs-lookup"><span data-stu-id="97312-154">ProcessingStatus</span></span>
- <span data-ttu-id="97312-155">Текст</span><span class="sxs-lookup"><span data-stu-id="97312-155">Text</span></span>
- <span data-ttu-id="97312-156">WordCount</span><span class="sxs-lookup"><span data-stu-id="97312-156">WordCount</span></span>
- <span data-ttu-id="97312-157">воркингсетид</span><span class="sxs-lookup"><span data-stu-id="97312-157">WorkingsetId</span></span>

<span data-ttu-id="97312-158">Для определения всех полей метаданных в Advanced eDiscovery просмотрите [поля метаданных документа](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="97312-158">For a definition of all metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
