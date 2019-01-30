---
title: Исправление ошибок при обработке данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608288"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="41930-102">Исправление ошибок при обработке данных</span><span class="sxs-lookup"><span data-stu-id="41930-102">Error remediation when processing data</span></span>

<span data-ttu-id="41930-p101">Исправление ошибок позволяет администраторам eDiscovery возможность устранения ошибок данных, предотвращающие расширенной обнаружения электронных данных (Просмотр) должным образом обработки содержимого. Например файлы, которые защищены паролем не удается обработать с момента заблокированы или зашифрованных файлов. С помощью исправления ошибок, администраторы обнаружения электронных данных можно загружать файлы с помощью таких ошибок, удаления защиты паролем и загрузки проверка файлов.</span><span class="sxs-lookup"><span data-stu-id="41930-p101">Error remediation allows eDiscovery administrators the ability to rectify data issues which prevent Advanced eDiscovery (Preview) from properly processing the content. For example, files that are password protected cannot be processed since the files are locked or encrypted. Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="41930-106">Используйте следующий порядок действий для устранения файлы с ошибками в тех случаях, расширенные обнаружения электронных данных (Просмотр).</span><span class="sxs-lookup"><span data-stu-id="41930-106">Use the following workflow to remediate files with errors in Advanced eDiscovery (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="41930-107">Создание сеанс исправлению ошибок обновления файлов с обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="41930-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="41930-108">Если мастер исправлению ошибок работает в любое время во время следующей процедуры, вы можете вернуться к сеанса исправлению ошибок из вкладки **обработки** , выбрав **исправлений ошибок** в **представлении** раскрывающегося меню.</span><span class="sxs-lookup"><span data-stu-id="41930-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="41930-109">На вкладке **Обработка** вариантом расширенной eDiscovery (Просмотр) выберите **ошибки** в раскрывающемся меню **представление** .</span><span class="sxs-lookup"><span data-stu-id="41930-109">On the **Processing** tab in an Advanced eDiscovery (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="41930-p102">Выберите ошибки, которые необходимо исправить, нажав кнопку переключатель рядом с тип ошибки или тип файла.  В следующем примере мы в случае устранению защищенных паролем файлов.</span><span class="sxs-lookup"><span data-stu-id="41930-p102">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.  In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="41930-112">Нажмите кнопку **+ новый исправлению ошибок**.</span><span class="sxs-lookup"><span data-stu-id="41930-112">Click **+ New error remediation**.</span></span>

    ![Исправление ошибок](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="41930-114">Начинает сеанс исправлению ошибок, начиная с этапа подготовки, где то поврежденные файлы перемещаются в безопасное место Azure веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="41930-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![Подготовка исправлению ошибок](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="41930-116">После выполнения подготовительных действий, нажмите кнопку **Далее: загрузка файлов** с файл для загрузки.</span><span class="sxs-lookup"><span data-stu-id="41930-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Загрузка файлов](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="41930-p103">Чтобы загрузить файлы, укажите **конечный путь для загрузки**; Это путь на локальном компьютере, где необходимо загрузить файл.  Путь по умолчанию, % USERPROFILE%\Downloads\errors, указывает на папку файлы для загрузки при входе пользователя; При необходимости его можно изменить.</span><span class="sxs-lookup"><span data-stu-id="41930-p103">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.  The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="41930-120">Мы рекомендуем использовать путь к локальному файлу вместо удаленного сетевой путь для обеспечения оптимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="41930-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="41930-121">Если вы еще не установили AzCopy, можно установить его здесь:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="41930-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="41930-p104">Скопируйте предварительно определенные команды, нажав кнопку **Копировать в буфер обмена**. Откройте окно командной строки windows, вставьте команду и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="41930-p104">Copy the predefined command by clicking **Copy to clipboard**. Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="41930-124">Файлы будут загружаться.</span><span class="sxs-lookup"><span data-stu-id="41930-124">The files will be downloaded.</span></span>

    ![Подготовка исправлению ошибок](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > <span data-ttu-id="41930-126">Если у вас есть вопросы, выполнив эту команду, https://go.microsoft.com/fwlink/?linkid=2038117 советами по устранению проблем.</span><span class="sxs-lookup"><span data-stu-id="41930-126">If you have issues running this command, see https://go.microsoft.com/fwlink/?linkid=2038117 for troubleshooting tips.</span></span>

7. <span data-ttu-id="41930-p105">После загрузки файлов, можно исправить их с соответствующее средство. Для файлов, защищенных паролем существует ряд средств, которые можно использовать для взлома паролей. Если вы знаете пароли для файлов, можно открыть их и удаления защиты паролем.</span><span class="sxs-lookup"><span data-stu-id="41930-p105">After downloading the files, you can remediate them with an appropriate tool. For password protected files, there are a number of password cracking tools you can use. If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="41930-p106">ИТ важно сохранить имена структуры и файл проверка файлов в списке.  Все соглашения о наименовании, используемые в загруженных файлов и папок делают его можно сопоставить обратно в исходные файлы remdiated.</span><span class="sxs-lookup"><span data-stu-id="41930-p106">IT is important that you retain the directory structure and file names of the remediated files in tact.  All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="41930-p107">Теперь вернитесь к расширенной обнаружения электронных данных (Предварительная версия) и нажмите кнопку **Далее: загрузки файлов**.  Перемещение к следующему шагу где теперь можно загрузить файлы.</span><span class="sxs-lookup"><span data-stu-id="41930-p107">Now, return to Advanced eDiscovery (Preview) and click **Next: Upload files**.  This will move to the next step where you can now upload the files.</span></span>

    ![Отправка файлов](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="41930-135">Укажите расположение проверка файлов в текстовом поле **путь к расположению файлов** нажмите кнопку **Копировать в clibpboard**.</span><span class="sxs-lookup"><span data-stu-id="41930-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="41930-136">Вставьте команду в командной строке Windows и нажмите клавишу **Ввод** для отправки файлов.</span><span class="sxs-lookup"><span data-stu-id="41930-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="41930-138">И, наконец, вернитесь к расширенной обнаружения электронных данных (Предварительная версия) и нажмите кнопку **Далее: обработка файлов**.</span><span class="sxs-lookup"><span data-stu-id="41930-138">Finally, return to Advanced eDiscovery (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="41930-p108">При завершении обработки.  Можно вернуться к рабочее множество и проверка в файле.</span><span class="sxs-lookup"><span data-stu-id="41930-p108">When processing is complete.  You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="41930-141">Что происходит при файлов выполняется проверка</span><span class="sxs-lookup"><span data-stu-id="41930-141">What happens when files are remediated</span></span>

<span data-ttu-id="41930-142">При передаче проверка файлов, исходные метаданные сохраняется, за исключением следующих полей:</span><span class="sxs-lookup"><span data-stu-id="41930-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="41930-143">DocumentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="41930-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="41930-144">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="41930-144">ExtractedTextSize</span></span>
- <span data-ttu-id="41930-145">HasText</span><span class="sxs-lookup"><span data-stu-id="41930-145">HasText</span></span>
- <span data-ttu-id="41930-146">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="41930-146">IsErrorRemediate</span></span>
- <span data-ttu-id="41930-147">IsParentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="41930-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="41930-148">ItemExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="41930-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="41930-149">LoadId</span><span class="sxs-lookup"><span data-stu-id="41930-149">LoadId</span></span>
- <span data-ttu-id="41930-150">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="41930-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="41930-151">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="41930-151">ProcessingStatus</span></span>
- <span data-ttu-id="41930-152">Текст</span><span class="sxs-lookup"><span data-stu-id="41930-152">Text</span></span>
- <span data-ttu-id="41930-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="41930-153">WordCount</span></span>
- <span data-ttu-id="41930-154">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="41930-154">WorkingsetId</span></span>

<span data-ttu-id="41930-155">Определение всех полей метаданных документа в расширенной обнаружения электронных данных (Предварительная версия) [полей метаданных документа](document-metadata-fields.md)см.</span><span class="sxs-lookup"><span data-stu-id="41930-155">For a definition of all document metadata fields in Advanced eDiscovery (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>