---
title: Загрузка не относящихся к Office 365 данных в набор для проверки
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
ms.openlocfilehash: 86d858994f95176ea4d415405c4043f7e7c5308e
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155011"
---
# <a name="load-non-office-365-data-into-a-review-set"></a><span data-ttu-id="f0dc0-102">Загрузка не относящихся к Office 365 данных в набор для проверки</span><span class="sxs-lookup"><span data-stu-id="f0dc0-102">Load non-Office 365 data into a review set</span></span>

<span data-ttu-id="f0dc0-103">Не все документы, которые может потребоваться проанализировать с помощью Office 365 Advanced eDiscovery, будут жить в Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-103">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365.</span></span> <span data-ttu-id="f0dc0-104">С помощью функции импорта содержимого, отличной от Office 365, в Advanced eDiscovery вы можете отправлять документы, не включенные в Office 365, в набор проверки, чтобы он анализировался с помощью расширенного обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-104">With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a review set so it is analyzed with Advanced eDiscovery.</span></span> <span data-ttu-id="f0dc0-105">В этой процедуре показано, как перенести документы, не относящиеся к Office 365, в Расширенное обнаружение электронных данных для анализа.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-105">This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="f0dc0-106">Для расширенного обнаружения электронных данных требуется Office 365 E3 с дополнительным соответствием или подпиской на систему с дополнительным соответствием в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-106">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization.</span></span> <span data-ttu-id="f0dc0-107">Если у вас нет этого плана и вы хотите попытаться использовать Расширенное обнаружение электронных данных, вы можете зарегистрироваться в пробной версии Office 365 Enterprise ~.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-107">If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="f0dc0-108">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="f0dc0-108">Before you begin</span></span>

<span data-ttu-id="f0dc0-109">Для использования функции отправки, отличной от Office 365, описанной в этой статье, необходимо следующее:</span><span class="sxs-lookup"><span data-stu-id="f0dc0-109">Using the upload Non-Office 365 feature as described in this article requires that you have the following:</span></span>

- <span data-ttu-id="f0dc0-110">Подписка на Office 365 или Microsoft 365 в качестве подписки на Office или E3 с дополнительным подпискум на надстройку.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-110">An Office 365 or Microsoft 365 E5 subscription or an E3 subscription with the Advanced Compliance add-on subscription.</span></span>

- <span data-ttu-id="f0dc0-111">Все custodians, для которых содержимое, не относящееся к Office 365, должно быть отправлено в лицензию E3 с дополнительным лицензионным соглашением на соответствие требованиям или иметь лицензию "от".</span><span class="sxs-lookup"><span data-stu-id="f0dc0-111">All custodians whose non-Office 365 content will be uploaded must have E3 license with an Advanced Compliance add-on license or have an E5 license.</span></span>

- <span data-ttu-id="f0dc0-112">Существующее расширенное дело обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-112">An existing Advanced eDiscovery case.</span></span>

- <span data-ttu-id="f0dc0-113">Custodians необходимо добавить в дело перед отправкой связанных с ними данных, отличных от Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-113">Custodians must be added to the case before you upload the non-Office 365 data that's associated to them.</span></span>

- <span data-ttu-id="f0dc0-114">Все файлы, которые будут отправлены, должны находиться в папках, в которых каждая папка связана с определенным хранитель.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-114">All files that will be uploaded must be located in folders, where each folder is associated with a specific custodian.</span></span> <span data-ttu-id="f0dc0-115">Имена этих папок должны иметь следующий формат имен: *Alias @ имя_домена*.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-115">The names for these folders must use the following naming format: *alias@domainname*.</span></span> <span data-ttu-id="f0dc0-116">*Псевдоним @ имя_домена* должен быть псевдонимом Office 365 пользователя и доменом.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-116">The *alias@domainname* must be the user's Office 365 alias and domain.</span></span> <span data-ttu-id="f0dc0-117">Вы можете собрать все папки *Alias @ имя_домена* в корневую папку.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-117">You can collect all the *alias@domainname* folders into a root folder.</span></span> <span data-ttu-id="f0dc0-118">Корневая папка может содержать только папки *Alias @ имя_домена* ; свободные файлы не допускаются в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-118">The root folder can only contain the *alias@domainname* folders; loose files aren't allowed in the root folder.</span></span>

   <span data-ttu-id="f0dc0-119">Например, структура папок для данных 365, которые вы хотите отправить, будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f0dc0-119">For example, the folder structure for the non-Office 365 data that you want to upload would be similar to the following:</span></span>

   - <span data-ttu-id="f0dc0-120">c:\nonO365\abraham.mcmahon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f0dc0-120">c:\nonO365\abraham.mcmahon@contoso.com</span></span>
   - <span data-ttu-id="f0dc0-121">c:\nonO365\jewell.gordon@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f0dc0-121">c:\nonO365\jewell.gordon@contoso.com</span></span>
   - <span data-ttu-id="f0dc0-122">c:\nonO365\staci.gonzalez@contoso.com</span><span class="sxs-lookup"><span data-stu-id="f0dc0-122">c:\nonO365\staci.gonzalez@contoso.com</span></span>

   <span data-ttu-id="f0dc0-123">Где abraham.mcmahon@contoso.com, jewell.gordon@contoso.com и staci.gonzalez@contoso.com — это SMTP-адреса custodians в случае.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-123">Where abraham.mcmahon@contoso.com, jewell.gordon@contoso.com, and staci.gonzalez@contoso.com are the SMTP addresses of custodians in the case.</span></span>

   ![Структура папок отправки данных, отличных от Office 365](../media/3f2dde84-294e-48ea-b44b-7437bd25284c.png)

- <span data-ttu-id="f0dc0-125">Учетная запись, которая является диспетчером обнаружения электронных данных или администратором обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="f0dc0-125">An account that is either an eDiscovery Manager or eDiscovery Administrator</span></span>

- <span data-ttu-id="f0dc0-126">Средства Microsoft Azure Storage Tools, установленные на компьютере, который имеет доступ к структуре папки контента, отличной от Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-126">Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="f0dc0-127">Установите AzCopy, что можно сделать, выполнив указанные ниже действия.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="f0dc0-127">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="f0dc0-128">Отправка контента, отличного от Office 365, в Расширенное обнаружение электронных данных</span><span class="sxs-lookup"><span data-stu-id="f0dc0-128">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="f0dc0-129">В качестве диспетчера обнаружения электронных данных или администратора eDiscovery откройте компонент Advanced eDiscovery, а затем в случае отправки данных, отличных от Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-129">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.</span></span>  <span data-ttu-id="f0dc0-130">Перейдите на \*\*\*\* вкладку Рецензирование и выберите набор проверок, в который требуется загрузить данные 365, не относящиеся к Office.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-130">Click the **review sets** tab, then select the review set you wish to load the Non-Office 365 data to.</span></span>  <span data-ttu-id="f0dc0-131">Если вы еще не создали набор рецензирования, вы можете сделать это сейчас.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-131">If you have not already created a review set, you can do so now.</span></span>  <span data-ttu-id="f0dc0-132">Наконец, щелкните **Управление набором проверки** , а затем щелкните **Просмотреть отправки** в плитке данных \* \* не из Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-132">Finally, click **Manage review set** and then click **View uploads** in the \*\*Non-Office 365 data tile.</span></span>

2. <span data-ttu-id="f0dc0-133">Нажмите кнопку **отправить файлы** , чтобы запустить мастер импорта данных, не относящийся к Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-133">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

   ![Отправка файлов](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="f0dc0-135">На первом этапе мастера просто подготавливается безопасный большой двоичный объект Azure для отправляемых файлов.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-135">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.</span></span>  <span data-ttu-id="f0dc0-136">После завершения подготовки нажмите кнопку " **Далее": отправить файлы** .</span><span class="sxs-lookup"><span data-stu-id="f0dc0-136">Once preparation is completed, click the **Next: Upload files** button.</span></span>

   ![Импорт, не относящийся к Office 365, подготовка](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="f0dc0-138">На шаге **Отправка файлов** укажите **путь к расположению файлов**, где находятся данные, не относящиеся к Office 365, которые планируется импортировать.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-138">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.</span></span>  <span data-ttu-id="f0dc0-139">Задание правильного расположения гарантирует, что команда AzCopy будет правильно обновлена.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-139">Setting the correct location ensures the AzCopy command is properly updated.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f0dc0-140">Если вы еще не установили AzCopy, вы можете сделать это следующим образом:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="f0dc0-140">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="f0dc0-141">Скопируйте предопределенную команду, щелкнув ссылку **Копировать в буфер обмена** .</span><span class="sxs-lookup"><span data-stu-id="f0dc0-141">Copy the predefined command by clicking the **Copy to clipboard** link.</span></span> <span data-ttu-id="f0dc0-142">Запустите командную строку Windows, вставьте команду и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-142">Start a windows command prompt, paste the command and press enter.</span></span>  <span data-ttu-id="f0dc0-143">Файлы будут отправлены в безопасное хранилище BLOB-объектов Azure для следующего этапа.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-143">The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

   ![Импорт файлов, отличных от Office 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

   ![Импорт не для Office 365, AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

   > [!NOTE]
   > <span data-ttu-id="f0dc0-146">Если предоставленная команда AzCopy не удалась, обратитесь к разделу [Устранение неполадок AzCopy в Advanced eDiscovery](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="f0dc0-146">If the supplied AzCopy command fails, refer to [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md)</span></span>

6. <span data-ttu-id="f0dc0-147">Наконец, вернемся к политике безопасности _Амп_ и нажмите кнопку **Далее: обработка файлов** .</span><span class="sxs-lookup"><span data-stu-id="f0dc0-147">Finally, return back to the Security & Compliance and click the **Next: Process files** button.</span></span>  <span data-ttu-id="f0dc0-148">Это приведет к обработке, извлечению текста и индексированию отправленных файлов.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-148">This will initiate processing, text extraction and indexing of the uploaded files.</span></span>  <span data-ttu-id="f0dc0-149">Вы можете отслеживать ход обработки здесь или на вкладке **задания** .  После завершения новые файлы будут доступны в наборе проверки.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-149">You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the review set.</span></span>  <span data-ttu-id="f0dc0-150">После завершения обработки можно закрыть мастер.</span><span class="sxs-lookup"><span data-stu-id="f0dc0-150">Once processing is complete, you can dismiss the wizard.</span></span>

   ![Файлы импорта и обработки файлов, отличных от Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

