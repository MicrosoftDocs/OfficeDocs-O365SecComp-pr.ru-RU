---
title: Настройка параметров поиска и аналитики
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
ms.openlocfilehash: d9528a4bcfaa77f2e232b25d03eda46cce42ebb9
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29608243"
---
# <a name="configure-search-and-analytics-settings"></a><span data-ttu-id="6ade0-102">Настройка параметров поиска и аналитики</span><span class="sxs-lookup"><span data-stu-id="6ade0-102">Configure search and analytics settings</span></span>


## <a name="near-duplicates-and-email-threading"></a><span data-ttu-id="6ade0-103">Рядом с дубликаты и работа с потоками электронной почты</span><span class="sxs-lookup"><span data-stu-id="6ade0-103">Near duplicates and email threading</span></span>

<span data-ttu-id="6ade0-104">В этом разделе можно задать параметры для повторяющихся рядом с поиска повторяющихся данных и потоков электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6ade0-104">In this section, you can set parameters for duplicate detection, near duplicate detection, and email threading.</span></span>

- <span data-ttu-id="6ade0-p101">Включение и отключение: включают повторяющихся рядом с поиска повторяющихся данных и потоков электронной почты как часть анализа потока, если этот параметр включен. Так как их создавать друг на друга, необходимо включить их все или отключить все из них.</span><span class="sxs-lookup"><span data-stu-id="6ade0-p101">Enable/disable: include duplicate detection, near duplicate detection, and email threading as part of analytics flow if enabled. Because they build on top of each other, you must enable all of them or disable all of them.</span></span>

- <span data-ttu-id="6ade0-107">Пороговое значение: если выше порога подобия уровень двух документов, они будут помещены в то же самое, рядом с дубликат набора.</span><span class="sxs-lookup"><span data-stu-id="6ade0-107">Threshold: if the similarity level of two documents are above the threshold, they will be put in the same near duplicate set.</span></span>

- <span data-ttu-id="6ade0-p102">Скрыть дубликаты по умолчанию: Если этот параметр включен, применяется фильтр повторяющиеся документы в разделе Работа по умолчанию. В разделе Работа по задать при необходимости можно удалить фильтра вручную.</span><span class="sxs-lookup"><span data-stu-id="6ade0-p102">Hide duplicates by default: if this setting is on, a filter to hide duplicate documents will be applied in the working set by default. The filter can be removed manually in the working set if necessary.</span></span>

- <span data-ttu-id="6ade0-p103">Минимальное/максимальное количество слов: рядом с дубликаты и адрес электронной почты threading будет выполняться только в документы, которые имеют по крайней мере минимальное количество слов и более максимальное количество слов. Для получения дополнительных сведений см [рядом с поиска повторяющихся данных](near-duplicates.md) и [Работа с потоками электронной почты](email-threading.md).</span><span class="sxs-lookup"><span data-stu-id="6ade0-p103">Minimum/maximum number of words: near duplicates and email threading will run only on documents that have at least the minimum number of words and at most the maximum number of words. For more information, see [Near duplicate detection](near-duplicates.md) and [Email threading](email-threading.md).</span></span>

## <a name="themes"></a><span data-ttu-id="6ade0-112">Темы</span><span class="sxs-lookup"><span data-stu-id="6ade0-112">Themes</span></span>

<span data-ttu-id="6ade0-113">В этом разделе можно задать параметры для темы.</span><span class="sxs-lookup"><span data-stu-id="6ade0-113">In this section, you can set parameters for themes.</span></span>

- <span data-ttu-id="6ade0-114">Включение и отключение: включают тем кластер как часть анализа потока, если этот параметр включен.</span><span class="sxs-lookup"><span data-stu-id="6ade0-114">Enable/disable: include themes clustering as part of analytics flow if enabled.</span></span>
- <span data-ttu-id="6ade0-p104">Настроить максимальное количество тем динамически динамически: в некоторых случаях не достаточно документы, чтобы создать требуемое число тем. Если этот параметр включен, затем вместо предпринята попытка желаемую максимальное количество тем, при настройке максимальное количество тем динамически.</span><span class="sxs-lookup"><span data-stu-id="6ade0-p104">Adjust maximum number of themes dynamically dynamically: in certain cases, there are not enough documents to produce the desired number of themes. If this setting is turned on, then rather than trying to force the desired maximum number of themes, the system adjusts maximum number of themes dynamically.</span></span>
- <span data-ttu-id="6ade0-117">Максимальное количество тем: желаемое число тем</span><span class="sxs-lookup"><span data-stu-id="6ade0-117">Maximum number of themes: desired number of themes</span></span>
- <span data-ttu-id="6ade0-118">Включение номера в тем: при включении этого параметра, он будет включать номера в при создании темы.</span><span class="sxs-lookup"><span data-stu-id="6ade0-118">Include numbers in themes: When enabled, it will include numbers in when generating themes.</span></span>  

## <a name="optical-character-recognition-ocr"></a><span data-ttu-id="6ade0-119">Распознавание текста (OCR)</span><span class="sxs-lookup"><span data-stu-id="6ade0-119">Optical character recognition (OCR)</span></span>

<span data-ttu-id="6ade0-120">Если этот параметр включен, распознавание текста будет выполняться в изображения, которые ingested в рабочие наборы, поэтому они могут быть доступен для поиска.</span><span class="sxs-lookup"><span data-stu-id="6ade0-120">When this setting is turned on, OCR will be run on images that are ingested into working sets so that they can be searchable.</span></span>

## <a name="ignore-text"></a><span data-ttu-id="6ade0-121">Пропуск текста</span><span class="sxs-lookup"><span data-stu-id="6ade0-121">Ignore text</span></span>

<span data-ttu-id="6ade0-p105">Существует экземпляры, где определенные тексты будет снизить качество анализа, такие как длительным заявления об отказе, которые добавляются на определенные сообщения электронной почты вне зависимости от содержимого электронной почты. Если принять во внимание таких случаях, можно исключить этот текст из analytics, указав текст (поддерживается регулярное выражение) и модули, которые следует исключить текст для.</span><span class="sxs-lookup"><span data-stu-id="6ade0-p105">There are instances where certain texts will diminish the quality of analytics, such as lengthy disclaimers that get added to certain emails regardless of the content of the email. If you are aware of such cases, you can exclude this text from analytics by specifying the text (RegEx is supported) and which modules that text should be excluded for.</span></span>