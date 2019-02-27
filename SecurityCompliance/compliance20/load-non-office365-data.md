---
title: Загрузка не относящихся к Office 365 данных в рабочий набор
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
ms.openlocfilehash: b177fc292c748f21907621196dc28d6b8fe17959
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296792"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="2d81a-102">Загрузка не относящихся к Office 365 данных в рабочий набор</span><span class="sxs-lookup"><span data-stu-id="2d81a-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="2d81a-p101">Не все документы, которые может потребоваться проанализировать с помощью Office 365 Advanced eDiscovery, будут жить в Office 365. С помощью функции импорта содержимого, отличной от Office 365, в Advanced eDiscovery вы можете отправлять документы, не включенные в Office 365, в рабочий набор, чтобы их было анализировать с помощью расширенного обнаружения электронных данных. В этой процедуре показано, как перенести документы, не относящиеся к Office 365, в Расширенное обнаружение электронных данных для анализа.</span><span class="sxs-lookup"><span data-stu-id="2d81a-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="2d81a-p102">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете зарегистрироваться для получения пробной версии Office 365 корпоративный E5.</span><span class="sxs-lookup"><span data-stu-id="2d81a-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="2d81a-108">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="2d81a-108">Before you begin</span></span>
<span data-ttu-id="2d81a-109">Для использования функции отправки, отличной от Office 365, описанной в этой процедуре, необходимо следующее:</span><span class="sxs-lookup"><span data-stu-id="2d81a-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="2d81a-110">Office 365 E3 с дополнительным подпискум на надстройку или на дополнительные требования.</span><span class="sxs-lookup"><span data-stu-id="2d81a-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="2d81a-111">Все custodians, для которых содержимое, не относящееся к Office 365, должно быть отправлено в виде E3 с дополнительными лицензиями на надстройку или для установки и возврата.</span><span class="sxs-lookup"><span data-stu-id="2d81a-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="2d81a-112">Существующее дело обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="2d81a-112">An existing eDiscovery case.</span></span>

- <span data-ttu-id="2d81a-p103">Все файлы для отправки собраны в папки, для которых в одной папке есть папка хранитель, а имя папки имеет следующий формат: *псевдоним @ имя_домена* . *Псевдоним @ имя_домена* должен быть пользователем Office 365 Alias and domain. Вы можете собрать все папки *Alias @ имя_домена* в корневую папку. Корневая папка может содержать только папки *Alias @ имя_домена* , но в корневой папке не должно быть свободных файлов.</span><span class="sxs-lookup"><span data-stu-id="2d81a-p103">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* . The *alias@domainname* must be users Office 365 alias and domain. You can collect all the *alias@domainname* folders into a root folder. The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

- <span data-ttu-id="2d81a-117">Учетная запись, которая является диспетчером eDiscovery или Microsoft Azure Storage Tools, установленных на компьютере, который имеет доступ к структуре папки контента, отличной от Office 365.</span><span class="sxs-lookup"><span data-stu-id="2d81a-117">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="2d81a-118">Установите AzCopy, что можно сделать, выполнив указанные ниже действия.https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="2d81a-118">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="2d81a-119">Отправка контента, отличного от Office 365, в Расширенное обнаружение электронных данных</span><span class="sxs-lookup"><span data-stu-id="2d81a-119">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="2d81a-p104">В качестве диспетчера обнаружения электронных данных или администратора eDiscovery откройте компонент Advanced eDiscovery, а затем в случае отправки данных, отличных от Office 365.  Перейдите на вкладку **рабочие наборы** , а затем выберите рабочий набор, в который вы хотите загрузить данные, не относящиеся к Office 365.  Если вы еще не создали рабочее множество, вы можете сделать это сейчас.  Наконец, щелкните **Управление заданиями Set** , а затем **Просмотр** отправок в разделе данные, не относящиеся к Office 365</span><span class="sxs-lookup"><span data-stu-id="2d81a-p104">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.  Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.  If you have not already created a working set, you can do so now.  Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="2d81a-124">Нажмите кнопку **отправить файлы** , чтобы запустить мастер импорта данных, не относящийся к Office 365.</span><span class="sxs-lookup"><span data-stu-id="2d81a-124">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Отправка файлов](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="2d81a-p105">На первом этапе мастера просто подготавливается безопасный большой двоичный объект Azure для отправляемых файлов.  После подготовки компелтед нажмите кнопку " **Далее: Отправка файлов** ".</span><span class="sxs-lookup"><span data-stu-id="2d81a-p105">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.  Once preparation is compelted, click the **Next: Upload files** button.</span></span>

![Импорт, не относящийся к Office 365, подготовка](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="2d81a-p106">На шаге **Отправка файлов** укажите **путь к расположению файлов**, где находятся данные, не относящиеся к Office 365, которые планируется импортировать.  Задание правильного расположения гарантирует, что команда AzCopy будет правильно обновлена.</span><span class="sxs-lookup"><span data-stu-id="2d81a-p106">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.  Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="2d81a-131">Если вы еще не установили AzCopy, вы можете сделать это следующим образом:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="2d81a-131">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="2d81a-p107">Скопируйте предопределенную команду, щелкнув ссылку **Копировать в буфер обмена** . Запустите командную строку Windows, вставьте команду и нажмите клавишу ВВОД.  Файлы будут отправлены в безопасное хранилище BLOB-объектов Azure для следующего этапа.</span><span class="sxs-lookup"><span data-stu-id="2d81a-p107">Copy the predefined command by clicking the **Copy to clipboard** link. Start a windows command prompt, paste the command and press enter.  The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Импорт файлов, отЛичных от Office 365](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Импорт не для Office 365, AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="2d81a-p108">Наконец, вернемся к политике безопасности _Амп_ и нажмите кнопку **Далее: обработка файлов** .  Это приведет к обработке, извлечению текста и индексированию отправленных файлов.  Вы можете отслеживать ход обработки здесь или на вкладке **задания** .  После завершения новые файлы будут доступны в рабочем наборе.  После завершения обработки можно закрыть мастер.</span><span class="sxs-lookup"><span data-stu-id="2d81a-p108">Finally, return back to the Security & Compliance and click the **Next: Process files** button.  This will initiate processing, text extraction and indexing of the uploaded files.  You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.  Once processing is complete, you can dismiss the wizard.</span></span>

![Файлы импорта и обработки файлов, отЛичных от Office 365](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

