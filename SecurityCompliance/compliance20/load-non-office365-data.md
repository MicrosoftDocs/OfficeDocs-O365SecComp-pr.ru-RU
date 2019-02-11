---
title: Загрузка не относящихся к Office 365 данных в рабочий набор
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
ms.openlocfilehash: 1dad52075303450673e7f48b87e2952e35629a5e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706090"
---
# <a name="load-non-office-365-data-into-a-working-set"></a><span data-ttu-id="c16c6-102">Загрузка не относящихся к Office 365 данных в рабочий набор</span><span class="sxs-lookup"><span data-stu-id="c16c6-102">Load non-Office 365 data into a working set</span></span>

<span data-ttu-id="c16c6-p101">Не все документы, которые может потребоваться при анализе с Office 365 расширенного обнаружения электронных данных будет live в Office 365. С содержимым без поддержки Office 365 импорта компонента в расширенной обнаружения электронных данных, можно публиковать документы, которые не live в Office 365 в рабочее множество, анализируется с расширенной обнаружения электронных данных. Этой процедуре показано, как для переноса документов Office 365 в расширенной обнаружения электронных данных для анализа.</span><span class="sxs-lookup"><span data-stu-id="c16c6-p101">Not all documents that you may need to analyze with Office 365 Advanced eDiscovery will live in Office 365. With the Non-Office 365 content import feature in Advanced eDiscovery you can upload documents that don't live in Office 365 into a working set so it is analyzed with Advanced eDiscovery. This procedure shows you how to bring your non-Office 365 documents into Advanced eDiscovery for analysis.</span></span>

>[!Note]
><span data-ttu-id="c16c6-p102">Чтобы можно было использовать Advanced eDiscovery, требуется подписка на Office 365 E3 с надстройкой Advanced Compliance или E5 для организации. Если у вас этого плана нет и вы хотите попробовать Advanced eDiscovery, можете зарегистрироваться для получения пробной версии Office 365 корпоративный E5.</span><span class="sxs-lookup"><span data-stu-id="c16c6-p102">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can sign up for a trial of Office 365 Enterprise E5.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="c16c6-108">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="c16c6-108">Before you begin</span></span>
<span data-ttu-id="c16c6-109">С помощью функции загрузки без поддержки Office 365, как описано в этой процедуры требуется, что у вас есть:</span><span class="sxs-lookup"><span data-stu-id="c16c6-109">Using the upload Non-Office 365 feature as described in this procedure requires that you have:</span></span>

- <span data-ttu-id="c16c6-110">E3 365 Office с дополнительный компонент Advanced соответствия или E5 подписки.</span><span class="sxs-lookup"><span data-stu-id="c16c6-110">An Office 365 E3 with Advanced Compliance add-on or E5 subscription.</span></span>

- <span data-ttu-id="c16c6-111">Все custodians, содержимое которого Office 365 будет отправлен необходимо E3 с дополнительный компонент Advanced соответствия или E5 лицензии.</span><span class="sxs-lookup"><span data-stu-id="c16c6-111">All custodians whose non-Office 365 content will be uploaded must have E3 with Advanced Compliance add-on or E5 licenses.</span></span>

- <span data-ttu-id="c16c6-112">Существующие случая обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="c16c6-112">An existing eDiscovery case.</span></span>

- <span data-ttu-id="c16c6-p103">Файлы для загрузки для сбора в папки, где существует отдельную папку для каждого custodian и имя папки, находится в этом формате *alias@domainname* . *Alias@domainname* должен быть псевдоним пользователей Office 365 и домен. Все папки *alias@domainname* можно объединить в корневую папку. В корневой папке может содержать только папки *alias@domainname* , в корневом каталоге должны быть свободные файлы отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="c16c6-p103">All the files for uploading gathered into folders where there is one folder per custodian and the folders' name is in this format *alias@domainname* . The *alias@domainname* must be users Office 365 alias and domain. You can collect all the *alias@domainname* folders into a root folder. The root folder can only contain the *alias@domainname* folders, there must be no loose files in the root folder.</span></span>

- <span data-ttu-id="c16c6-117">Учетная запись, которая является либо диспетчеру eDiscovery или обнаружения электронных данных Microsoft Azure хранилища Администрирование установить на компьютер, имеющий доступ к структуре папок содержимого Office 365.</span><span class="sxs-lookup"><span data-stu-id="c16c6-117">An account that is either an eDiscovery Manager or eDiscovery Administrator Microsoft Azure Storage Tools installed on a computer that has access to the non-Office 365 content folder structure.</span></span>

- <span data-ttu-id="c16c6-118">Установка AzCopy, что можно сделать здесь:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="c16c6-118">Install AzCopy, which you can do from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

## <a name="upload-non-office-365-content-into-advanced-ediscovery"></a><span data-ttu-id="c16c6-119">Office 365 содержимое загружается в расширенной обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="c16c6-119">Upload non-Office 365 content into Advanced eDiscovery</span></span>

1. <span data-ttu-id="c16c6-p104">Как eDiscovery Manager или eDiscovery администратор откройте дополнительные обнаружения электронных данных, а затем случай, который будет передан данные Office 365.  Перейдите на вкладку **Работа наборы** , а затем выберите рабочее множество, которую вы хотите загрузить данные без поддержки Office 365.  Если вы еще не создали рабочее множество, это можно сделать сейчас.  И, наконец нажмите кнопку **Управление работой** затем **Передача представления** в разделе данных без поддержки Office 365</span><span class="sxs-lookup"><span data-stu-id="c16c6-p104">As an eDiscovery Manager or eDiscovery Administrator, open Advanced eDiscovery, then the case that the non-Office 365 data will be uploaded to.  Click the **Working sets** tab, then select the working set you wish to load the Non-Office 365 data to.  If you have not already created a working set, you can do so now.  Finally, click **Manage workings set** then **View uploads** in the Non-Office 365 data section</span></span>

2. <span data-ttu-id="c16c6-124">Нажмите кнопку **загрузки файлов** , чтобы запустить мастер импорта данных без поддержки Office 365.</span><span class="sxs-lookup"><span data-stu-id="c16c6-124">Click the **Upload files** button to start the Non-Office 365 data import wizard.</span></span>

![Отправка файлов](../media/574f4059-4146-4058-9df3-ec97cf28d7c7.png)

3. <span data-ttu-id="c16c6-p105">Первый шаг в мастере просто подготавливает безопасной Azure blob для файлов для отправки.  После подготовки compelted, щелкните **Далее: загрузки файлов** кнопка.</span><span class="sxs-lookup"><span data-stu-id="c16c6-p105">The first step in the wizard simply prepares a secure Azure blob for the files to be uploaded.  Once preparation is compelted, click the **Next: Upload files** button.</span></span>

![Не относящегося к Office 365 импорта: Подготовка](../media/0670a347-a578-454a-9b3d-e70ef47aec57.png)
 
4. <span data-ttu-id="c16c6-p106">На этапе **загрузки файлов** укажите **путь к папке, файлы**, это где расположена данных без поддержки Office 365, которые планируется на импорт.  Установка в нужном месте обеспечивает AzCopy, команда надлежащим образом обновляются.</span><span class="sxs-lookup"><span data-stu-id="c16c6-p106">In the **Upload files** step, specify the **Path to location of files**, this is where the Non-Office 365 data you plan on importing is located.  Setting the correct location ensures the AzCopy command is properly updated.</span></span>

> [!NOTE]
> <span data-ttu-id="c16c6-131">Если AzCopy еще не установлен, это можно сделать здесь:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="c16c6-131">If you have not already installed AzCopy, you can do this from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

5. <span data-ttu-id="c16c6-p107">Предварительно определенные команда "Копировать", щелкнув ссылку **Копировать в буфер обмена** . Откройте окно командной строки windows, вставьте команду и нажмите клавишу ВВОД.  Файлы будет передан хранилище безопасной Azure больших двоичных объектов для следующего шага.</span><span class="sxs-lookup"><span data-stu-id="c16c6-p107">Copy the predefined command by clicking the **Copy to clipboard** link. Start a windows command prompt, paste the command and press enter.  The files will be uploaded to the secure Azure blob storage for the next step.</span></span>

![Импорт не относящиеся к Office 365 — отправить файлы](../media/3ea53b5d-7f9b-4dfc-ba63-90a38c14d41a.png)

![Импорт не относящегося к Office 365 - AzCopy](../media/504e2dbe-f36f-4f36-9b08-04aea85d8250.png)

6. <span data-ttu-id="c16c6-p108">И, наконец, вернуться к & безопасности соответствия требованиям и нажмите кнопку **Далее: обработка файлов** кнопка.  Это начнет обработку извлечение текста и индексирования загружаемых файлов.  Можно отслеживать ход выполнения обработки здесь или на вкладке **заданий** .  После завершения, будут доступны в рабочее множество новых файлов.  После завершения обработки можно закрыть мастер.</span><span class="sxs-lookup"><span data-stu-id="c16c6-p108">Finally, return back to the Security & Compliance and click the **Next: Process files** button.  This will initiate processing, text extraction and indexing of the uploaded files.  You can track the progress of processing here or in the **Jobs** tab.  Once completed, the new files will be available in the working set.  Once processing is complete, you can dismiss the wizard.</span></span>

![Импорт не относящиеся к Office 365 - обработки файлов](../media/218b1545-416a-4a9f-9b25-3b70e8508f67.png)

