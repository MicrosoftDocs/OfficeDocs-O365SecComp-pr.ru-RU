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
ms.openlocfilehash: 8653ebd82e9c045c4fc49b00fcb82bf22ab3f906
ms.sourcegitcommit: 6eb51931242d07abde2e37f1bd57d13bc724f0de
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34547944"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="a14d2-102">Исправление ошибок при обработке данных</span><span class="sxs-lookup"><span data-stu-id="a14d2-102">Error remediation when processing data</span></span>

<span data-ttu-id="a14d2-103">Устранение ошибок позволяет администраторам обнаружения электронных данных исправить проблемы с данными, которые предотвращают обработку содержимого с помощью расширенного обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="a14d2-103">Error remediation allows eDiscovery administrators the ability to rectify data issues which prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="a14d2-104">Например, файлы, защищенные паролем, не могут быть обработаны, так как файлы заблокированы или зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="a14d2-104">For example, files that are password protected cannot be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="a14d2-105">С помощью исправления ошибок администраторы обнаружения электронных данных могут загружать файлы с такими ошибками, удалять парольную защиту и отправлять исправленные файлы.</span><span class="sxs-lookup"><span data-stu-id="a14d2-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="a14d2-106">Используйте следующий рабочий процесс для исправления файлов с ошибками в дополнительных случаях обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="a14d2-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="a14d2-107">Создание сеанса исправления ошибок для исправления файлов с ошибками обработки</span><span class="sxs-lookup"><span data-stu-id="a14d2-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="a14d2-108">Если мастер исправления ошибок закрыт в любой момент во время выполнения следующей процедуры, вы можете вернуться к сеансу исправления ошибок на вкладке **Обработка** , выбрав в раскрывающемся меню **вид** параметр " **исправления ошибок** ".</span><span class="sxs-lookup"><span data-stu-id="a14d2-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="a14d2-109">На вкладке **Обработка** в расширенном случае обнаружения электронных данных выберите **ошибки** в раскрывающемся меню **вид** .</span><span class="sxs-lookup"><span data-stu-id="a14d2-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="a14d2-110">Выберите подлежащие исправлению ошибки, нажав переключатель рядом с типом ошибки или типом файла.</span><span class="sxs-lookup"><span data-stu-id="a14d2-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="a14d2-111">В следующем примере мы устранение файл, защищенный паролем.</span><span class="sxs-lookup"><span data-stu-id="a14d2-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="a14d2-112">Нажмите кнопку **+ новое исправление ошибок**.</span><span class="sxs-lookup"><span data-stu-id="a14d2-112">Click **+ New error remediation**.</span></span>

    ![Исправление ошибок](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="a14d2-114">Начнется сеанс исправления ошибок, начиная с стадии подготовки, в которой файлы с ошибками копируются в безопасное расположение Azure, чтобы их можно было скачать.</span><span class="sxs-lookup"><span data-stu-id="a14d2-114">The error remediation session will begin, starting with a preparation stage where the files with errors are copied to a secure Azure location so that they can be downloaded.</span></span>

    ![Подготовка исправления ошибок](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="a14d2-116">После завершения подготовки нажмите кнопку **Далее: Загрузка файлов** для продолжения загрузки.</span><span class="sxs-lookup"><span data-stu-id="a14d2-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Загрузка файлов](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="a14d2-118">Чтобы скачать файлы, укажите **целевой путь для скачивания**; Это путь к локальному компьютеру, на который необходимо скачать файл.</span><span class="sxs-lookup"><span data-stu-id="a14d2-118">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.</span></span>  <span data-ttu-id="a14d2-119">Путь по умолчанию,%Усерпрофиле%\довнлоадс\еррорс, указывает на папку загрузок пользователя, вошедшего в систему; При необходимости его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="a14d2-119">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="a14d2-120">Для оптимальной производительности рекомендуется использовать локальный путь к файлу вместо удаленного сетевого пути.</span><span class="sxs-lookup"><span data-stu-id="a14d2-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a14d2-121">Если вы не установили AzCopy, вы можете установить его отсюда:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="a14d2-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="a14d2-122">Скопируйте предопределенную команду, нажав кнопку **Копировать в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="a14d2-122">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="a14d2-123">Запустите командную строку Windows, вставьте команду и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="a14d2-123">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="a14d2-124">Файлы будут скачаны.</span><span class="sxs-lookup"><span data-stu-id="a14d2-124">The files will be downloaded.</span></span>

    ![Подготовка исправления ошибок](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="a14d2-126">Если предоставленная команда AzCopy не удалась, обратитесь к разделу [Устранение неполадок AzCopy в Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="a14d2-126">If the supplied AzCopy command fails, see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="a14d2-127">После загрузки файлов вы можете исправить их с помощью соответствующего средства.</span><span class="sxs-lookup"><span data-stu-id="a14d2-127">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="a14d2-128">Для файлов, защищенных паролем, можно использовать несколько средств взлома паролей.</span><span class="sxs-lookup"><span data-stu-id="a14d2-128">For password protected files, there are a number of password cracking tools you can use.</span></span> <span data-ttu-id="a14d2-129">Если вы знаете пароли этих файлов, вы можете открыть их и удалить защиту паролем.</span><span class="sxs-lookup"><span data-stu-id="a14d2-129">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="a14d2-130">Важно сохранить структуру каталогов и имена файлов исправленных файлов без изменений.</span><span class="sxs-lookup"><span data-stu-id="a14d2-130">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="a14d2-131">Все соглашения об именовании, используемые в скачанных файлах и папках, делают возможным сопоставление файлов ремдиатед с оригиналом.</span><span class="sxs-lookup"><span data-stu-id="a14d2-131">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="a14d2-132">Теперь вернитесь к расширенному eDiscovery и нажмите кнопку **Далее: отправить файлы**.</span><span class="sxs-lookup"><span data-stu-id="a14d2-132">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="a14d2-133">Это приведет к переходу на следующий шаг, на котором можно отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="a14d2-133">This will move to the next step where you can now upload the files.</span></span>

    ![Отправка файлов](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="a14d2-135">Укажите расположение исправленных файлов в текстовом поле **путь к расположению файлов** , а затем нажмите кнопку **Копировать в буфер обмена**.</span><span class="sxs-lookup"><span data-stu-id="a14d2-135">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="a14d2-136">Вставьте команду в командную строку Windows и нажмите клавишу **Ввод** , чтобы отправить файлы.</span><span class="sxs-lookup"><span data-stu-id="a14d2-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="a14d2-138">Наконец, вернитесь к расширенному eDiscovery и нажмите кнопку **Далее: обработка файлов**.</span><span class="sxs-lookup"><span data-stu-id="a14d2-138">Finally, return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="a14d2-139">По завершении обработки.</span><span class="sxs-lookup"><span data-stu-id="a14d2-139">When processing is complete.</span></span>  <span data-ttu-id="a14d2-140">Вы можете вернуться к набору проверки и просмотреть исправленный файл.</span><span class="sxs-lookup"><span data-stu-id="a14d2-140">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="a14d2-141">Что происходит при исправлении файлов</span><span class="sxs-lookup"><span data-stu-id="a14d2-141">What happens when files are remediated</span></span>

<span data-ttu-id="a14d2-142">При отправке исправленных файлов исходные метаданные сохраняются с исключением следующих полей:</span><span class="sxs-lookup"><span data-stu-id="a14d2-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="a14d2-143">Екстрактедтекстсизе</span><span class="sxs-lookup"><span data-stu-id="a14d2-143">ExtractedTextSize</span></span>
- <span data-ttu-id="a14d2-144">HasText</span><span class="sxs-lookup"><span data-stu-id="a14d2-144">HasText</span></span>
- <span data-ttu-id="a14d2-145">Исеррорремедиате</span><span class="sxs-lookup"><span data-stu-id="a14d2-145">IsErrorRemediate</span></span>
- <span data-ttu-id="a14d2-146">Лоадид</span><span class="sxs-lookup"><span data-stu-id="a14d2-146">LoadId</span></span>
- <span data-ttu-id="a14d2-147">Процессинжеррормессаже</span><span class="sxs-lookup"><span data-stu-id="a14d2-147">ProcessingErrorMessage</span></span>
- <span data-ttu-id="a14d2-148">Процессингстатус</span><span class="sxs-lookup"><span data-stu-id="a14d2-148">ProcessingStatus</span></span>
- <span data-ttu-id="a14d2-149">Текст</span><span class="sxs-lookup"><span data-stu-id="a14d2-149">Text</span></span>
- <span data-ttu-id="a14d2-150">WordCount</span><span class="sxs-lookup"><span data-stu-id="a14d2-150">WordCount</span></span>
- <span data-ttu-id="a14d2-151">Воркингсетид</span><span class="sxs-lookup"><span data-stu-id="a14d2-151">WorkingsetId</span></span>

<span data-ttu-id="a14d2-152">Определение всех полей метаданных документа в Advanced eDiscovery приведено в разделе [поля метаданных документа](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="a14d2-152">For a definition of all document metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
