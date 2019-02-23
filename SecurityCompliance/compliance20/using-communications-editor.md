---
title: Использование редактора взаимодействия
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 967320aeb960258d77d90cca4e3b681849f9952e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215809"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="e49e1-102">Использование редактора взаимодействия</span><span class="sxs-lookup"><span data-stu-id="e49e1-102">Use the communications editor</span></span>

<span data-ttu-id="e49e1-103">При определении контента портала, уведомления о юридических удержаниях, а также связанных напоминаний и укрупнений можно использовать редактор взаимоДействий для форматирования и динамического настройки контента.</span><span class="sxs-lookup"><span data-stu-id="e49e1-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="e49e1-104">Редактор форматированного текста</span><span class="sxs-lookup"><span data-stu-id="e49e1-104">Rich text editor</span></span> 

<span data-ttu-id="e49e1-p101">Редактор взаимоДействий позволяет пользователю настраивать текст с помощью параметров редактора. Например, пользователи могут изменять типы шрифтов, создавать маркированные списки, выделять содержимое и многое другое.</span><span class="sxs-lookup"><span data-stu-id="e49e1-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="e49e1-107">Переменные поля слияния</span><span class="sxs-lookup"><span data-stu-id="e49e1-107">Merge field variables</span></span>

<span data-ttu-id="e49e1-p102">Вы можете использовать переменные слияния электронной почты из редактора взаимодействия для встраивания настраиваемых атрибутов хранитель в основной текст общения. При отправке в Хранитель поле слияния будет заполнено соответствующим полем. Например, при отправке в Хранитель John Smith поле слияния [хранитель name] будет преобразовано соответствующим именем.</span><span class="sxs-lookup"><span data-stu-id="e49e1-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="e49e1-p103">Вы можете использовать поля слияния электронной почты, щелкнув значки **поля слияния** в верхней части элемента управления Rich Text Editor. Заполнитель будет добавлен в соответствии с расположением курсора пользователя.</span><span class="sxs-lookup"><span data-stu-id="e49e1-p103">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="e49e1-113">Список переменных поля слияния</span><span class="sxs-lookup"><span data-stu-id="e49e1-113">List of merge field variables</span></span>

| <span data-ttu-id="e49e1-114">Имя поля</span><span class="sxs-lookup"><span data-stu-id="e49e1-114">Field name</span></span>                  | <span data-ttu-id="e49e1-115">Сведения о поле</span><span class="sxs-lookup"><span data-stu-id="e49e1-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="e49e1-116">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e49e1-116">Display Name</span></span>  | <span data-ttu-id="e49e1-117">Имя и фамилия хранитель.</span><span class="sxs-lookup"><span data-stu-id="e49e1-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="e49e1-118">Ссылка подтверждения</span><span class="sxs-lookup"><span data-stu-id="e49e1-118">Acknowledgement Link</span></span> | <span data-ttu-id="e49e1-119">Настраиваемая ссылка для записи подтверждения каждого хранитель.</span><span class="sxs-lookup"><span data-stu-id="e49e1-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="e49e1-120">Ссылка на портал</span><span class="sxs-lookup"><span data-stu-id="e49e1-120">Portal Link</span></span>     | <span data-ttu-id="e49e1-121">Настраиваемая ссылка на портал соответствия требованиям для хранитель.</span><span class="sxs-lookup"><span data-stu-id="e49e1-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="e49e1-122">ВыДача директора</span><span class="sxs-lookup"><span data-stu-id="e49e1-122">Issuing Officer</span></span>                   | <span data-ttu-id="e49e1-123">Адрес электронной почты указанного директора поставщика.</span><span class="sxs-lookup"><span data-stu-id="e49e1-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="e49e1-124">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="e49e1-124">Issuing Date</span></span>                   | <span data-ttu-id="e49e1-125">Дата выпуска уведомления (UTC).</span><span class="sxs-lookup"><span data-stu-id="e49e1-125">The date that the notice was issued (UTC).</span></span>              |