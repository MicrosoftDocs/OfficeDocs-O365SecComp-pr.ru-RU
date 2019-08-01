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
ms.openlocfilehash: 5168196dcac8a2cb3809f43fabb470c0f64cd0f7
ms.sourcegitcommit: 73dcdafb15b462223d1a670c781db260eb73c2f5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/01/2019
ms.locfileid: "36048174"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="ccd31-102">Исправление ошибок при обработке данных</span><span class="sxs-lookup"><span data-stu-id="ccd31-102">Error remediation when processing data</span></span>

<span data-ttu-id="ccd31-103">Устранение ошибок позволяет администраторам обнаружения электронных данных устранить проблемы с данными, которые предотвращают неправильное обработку содержимого для расширенного обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="ccd31-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="ccd31-104">Например, файлы, защищенные паролем, не могут быть обработаны, так как файлы заблокированы или зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="ccd31-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="ccd31-105">С помощью исправления ошибок администраторы обнаружения электронных данных могут загружать файлы с такими ошибками, удалять защиту паролем, а затем отправлять исправленные файлы.</span><span class="sxs-lookup"><span data-stu-id="ccd31-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="ccd31-106">Используйте следующий рабочий процесс для исправления файлов с ошибками в дополнительных случаях обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="ccd31-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="ccd31-107">Создание сеанса исправления ошибок для исправления файлов с ошибками обработки</span><span class="sxs-lookup"><span data-stu-id="ccd31-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="ccd31-108">Если мастер исправления ошибок закрыт в любой момент во время выполнения следующей процедуры, вы можете вернуться к сеансу исправления ошибок на вкладке **Обработка** , выбрав в раскрывающемся меню **вид** параметр " **исправления ошибок** ".</span><span class="sxs-lookup"><span data-stu-id="ccd31-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="ccd31-109">На вкладке **Обработка** в расширенном случае обнаружения электронных данных выберите **ошибки** в раскрывающемся меню **вид** .</span><span class="sxs-lookup"><span data-stu-id="ccd31-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop-down menu.</span></span>

2. <span data-ttu-id="ccd31-110">Выберите подлежащие исправлению ошибки, нажав переключатель рядом с типом ошибки или типом файла.</span><span class="sxs-lookup"><span data-stu-id="ccd31-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="ccd31-111">В следующем примере мы устранение файл, защищенный паролем.</span><span class="sxs-lookup"><span data-stu-id="ccd31-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="ccd31-112">Нажмите кнопку **новое исправление ошибок**.</span><span class="sxs-lookup"><span data-stu-id="ccd31-112">Click **New error remediation**.</span></span>

    ![Исправление ошибок](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="ccd31-114">Сеанс исправления ошибок начинается с стадии подготовки, в которой файлы с ошибками копируются в хранилище Azure, предоставленное корпорацией Майкрософт, чтобы их можно было загрузить на локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="ccd31-114">The error remediation session starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![Подготовка исправления ошибок](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="ccd31-116">После завершения подготовки нажмите кнопку **Далее: Загрузка файлов** для продолжения загрузки.</span><span class="sxs-lookup"><span data-stu-id="ccd31-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Загрузка файлов](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="ccd31-118">Чтобы скачать файлы, укажите **целевой путь для скачивания**.</span><span class="sxs-lookup"><span data-stu-id="ccd31-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="ccd31-119">Это путь к локальному компьютеру, на который будет загружен файл.</span><span class="sxs-lookup"><span data-stu-id="ccd31-119">This is a path on your local computer where the file will be downloaded.</span></span>  <span data-ttu-id="ccd31-120">Путь по умолчанию,%Усерпрофиле%\довнлоадс\еррорс, указывает на папку загрузок пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="ccd31-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="ccd31-121">При необходимости вы можете изменить этот путь.</span><span class="sxs-lookup"><span data-stu-id="ccd31-121">You can change this path if necessary.</span></span> <span data-ttu-id="ccd31-122">Если вы сделаете это, мы рекомендуем использовать локальный путь к файлу вместо удаленного сетевого пути для достижения оптимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="ccd31-122">If you do change it, we recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

6. <span data-ttu-id="ccd31-123">Скопируйте предопределенную команду, нажав кнопку **Копировать в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="ccd31-123">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="ccd31-124">Запустите командную строку Windows, вставьте команду и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="ccd31-124">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="ccd31-125">Файлы будут скачаны.</span><span class="sxs-lookup"><span data-stu-id="ccd31-125">The files are downloaded.</span></span>

    ![Подготовка исправления ошибок](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="ccd31-127">Для успешного использования команды, указанной на странице **Загрузка файлов** , необходимо использовать AzCopy v 8.1.</span><span class="sxs-lookup"><span data-stu-id="ccd31-127">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="ccd31-128">Кроме того, для отправки файлов на шаге 10 необходимо использовать AzCopy v 8.1.</span><span class="sxs-lookup"><span data-stu-id="ccd31-128">You also must use AzCopy v8.1 to upload the files in step 10 below.</span></span> <span data-ttu-id="ccd31-129">Чтобы установить эту версию AzCopy, обратитесь к разделу [Transfer Data with a AzCopy v 8.1 в Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="ccd31-129">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="ccd31-130">Если предоставленная команда AzCopy не удалась, обратитесь к разделу [Устранение неполадок AzCopy в Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="ccd31-130">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="ccd31-131">После загрузки файлов вы можете исправить их с помощью соответствующего средства.</span><span class="sxs-lookup"><span data-stu-id="ccd31-131">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="ccd31-132">Для файлов, защищенных паролем, можно использовать несколько средств взлома паролей.</span><span class="sxs-lookup"><span data-stu-id="ccd31-132">For password-protected files, there several password cracking tools you can use.</span></span> <span data-ttu-id="ccd31-133">Если вы знаете пароли этих файлов, вы можете открыть их и удалить защиту паролем.</span><span class="sxs-lookup"><span data-stu-id="ccd31-133">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="ccd31-134">Важно сохранить структуру каталогов и имена файлов исправленных файлов без изменений.</span><span class="sxs-lookup"><span data-stu-id="ccd31-134">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="ccd31-135">Все соглашения об именовании, используемые в скачанных файлах и папках, делают возможным сопоставление файлов ремдиатед с оригиналом.</span><span class="sxs-lookup"><span data-stu-id="ccd31-135">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="ccd31-136">Теперь вернитесь к расширенному eDiscovery и нажмите кнопку **Далее: отправить файлы**.</span><span class="sxs-lookup"><span data-stu-id="ccd31-136">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="ccd31-137">Это приведет к переходу на следующий шаг, на котором можно отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="ccd31-137">This will move to the next step where you can now upload the files.</span></span>

    ![Отправка файлов](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="ccd31-139">Укажите расположение исправленных файлов в текстовом поле **путь к расположению файлов** , а затем нажмите кнопку **Копировать в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="ccd31-139">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="ccd31-140">Вставьте команду в командную строку Windows и нажмите клавишу **Ввод** , чтобы отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="ccd31-140">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="ccd31-142">Вернитесь к расширенному eDiscovery и нажмите кнопку **Далее: обработка файлов**.</span><span class="sxs-lookup"><span data-stu-id="ccd31-142">Return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="ccd31-143">По завершении обработки.</span><span class="sxs-lookup"><span data-stu-id="ccd31-143">When processing is complete.</span></span>  <span data-ttu-id="ccd31-144">Вы можете вернуться к набору проверки и просмотреть исправленный файл.</span><span class="sxs-lookup"><span data-stu-id="ccd31-144">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="ccd31-145">Что происходит при исправлении файлов</span><span class="sxs-lookup"><span data-stu-id="ccd31-145">What happens when files are remediated</span></span>

<span data-ttu-id="ccd31-146">При отправке исправленных файлов исходные метаданные сохраняются, за исключением следующих полей:</span><span class="sxs-lookup"><span data-stu-id="ccd31-146">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="ccd31-147">Екстрактедтекстсизе</span><span class="sxs-lookup"><span data-stu-id="ccd31-147">ExtractedTextSize</span></span>
- <span data-ttu-id="ccd31-148">HasText</span><span class="sxs-lookup"><span data-stu-id="ccd31-148">HasText</span></span>
- <span data-ttu-id="ccd31-149">Исеррорремедиате</span><span class="sxs-lookup"><span data-stu-id="ccd31-149">IsErrorRemediate</span></span>
- <span data-ttu-id="ccd31-150">Лоадид</span><span class="sxs-lookup"><span data-stu-id="ccd31-150">LoadId</span></span>
- <span data-ttu-id="ccd31-151">Процессинжеррормессаже</span><span class="sxs-lookup"><span data-stu-id="ccd31-151">ProcessingErrorMessage</span></span>
- <span data-ttu-id="ccd31-152">Процессингстатус</span><span class="sxs-lookup"><span data-stu-id="ccd31-152">ProcessingStatus</span></span>
- <span data-ttu-id="ccd31-153">Текст</span><span class="sxs-lookup"><span data-stu-id="ccd31-153">Text</span></span>
- <span data-ttu-id="ccd31-154">WordCount</span><span class="sxs-lookup"><span data-stu-id="ccd31-154">WordCount</span></span>
- <span data-ttu-id="ccd31-155">Воркингсетид</span><span class="sxs-lookup"><span data-stu-id="ccd31-155">WorkingsetId</span></span>

<span data-ttu-id="ccd31-156">Определение всех полей метаданных документа в Advanced eDiscovery приведено в разделе [поля метаданных документа](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="ccd31-156">For a definition of all document metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
