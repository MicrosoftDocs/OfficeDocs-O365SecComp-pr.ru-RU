---
title: Использование редактора взаимодействия
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
ms.openlocfilehash: b148ff1a77cd9225a26f98e7612e9fb5b57331e3
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29706060"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="cc842-102">Использование редактора взаимодействия</span><span class="sxs-lookup"><span data-stu-id="cc842-102">Use the communications editor</span></span>

<span data-ttu-id="cc842-103">При определении контент портала контент, юридические удержания уведомлений и напоминаний/эскалации связанных с ними, вы можете использовать возможности редактора Communications форматирования и динамически настройки содержимого.</span><span class="sxs-lookup"><span data-stu-id="cc842-103">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can leverage the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="cc842-104">Редактор форматированного текста</span><span class="sxs-lookup"><span data-stu-id="cc842-104">Rich text editor</span></span> 

<span data-ttu-id="cc842-p101">Редактор коммуникаций позволяет пользователю настраивать текста, с помощью параметров редактора. Например пользователей можно изменить типы шрифтов, создание маркированных списков, выделение содержимого и др.</span><span class="sxs-lookup"><span data-stu-id="cc842-p101">The Communications Editor allows user to customize the text using the editor options. For example, users can change font types, create bulleted lists, highlight content, and more.</span></span> 

## <a name="merge-field-variables"></a><span data-ttu-id="cc842-107">Объединение переменных поля</span><span class="sxs-lookup"><span data-stu-id="cc842-107">Merge field variables</span></span>

<span data-ttu-id="cc842-p102">Можно использовать переменные слияния электронной почты в редакторе коммуникаций для внедрения атрибуты настраиваемого custodian в тексте обмена данными. При отправке custodian, поле слияния заполняется соответствующее поле. Например при отправке custodian John Smith, поле слияния [имя Custodian] будет переведенных по соответствующее имя.</span><span class="sxs-lookup"><span data-stu-id="cc842-p102">You can leverage email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text. When sent to the custodian, the merge field will be populated with the corresponding field. For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span> 

<span data-ttu-id="cc842-p103">Можно использовать поля слияния электронной почты, выбрав значки **поле слияния** верхней части элемента управления редактора форматированного текста. Заполнитель будут добавляться off расположения курсора пользователей.</span><span class="sxs-lookup"><span data-stu-id="cc842-p103">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control. The placeholder will be added based off the location of the users' cursor.</span></span> 

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="cc842-113">Список доступных переменных полей слияния</span><span class="sxs-lookup"><span data-stu-id="cc842-113">List of merge field variables</span></span>

| <span data-ttu-id="cc842-114">Имя поля</span><span class="sxs-lookup"><span data-stu-id="cc842-114">Field name</span></span>                  | <span data-ttu-id="cc842-115">Сведения о поле</span><span class="sxs-lookup"><span data-stu-id="cc842-115">Field details</span></span> | 
| :------------------- | :------------------- |
| <span data-ttu-id="cc842-116">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cc842-116">Display Name</span></span>  | <span data-ttu-id="cc842-117">Custodian и фамилию имя.</span><span class="sxs-lookup"><span data-stu-id="cc842-117">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="cc842-118">Подтверждение ссылок</span><span class="sxs-lookup"><span data-stu-id="cc842-118">Acknowledgement Link</span></span> | <span data-ttu-id="cc842-119">Настраиваемая ссылка для записи каждой custodian подтверждения.</span><span class="sxs-lookup"><span data-stu-id="cc842-119">A customized link to record each custodian's acknowledgement.</span></span>|                 |
| <span data-ttu-id="cc842-120">Ссылка портала</span><span class="sxs-lookup"><span data-stu-id="cc842-120">Portal Link</span></span>     | <span data-ttu-id="cc842-121">Настраиваемая ссылка для соответствия требованиям custodian портала.</span><span class="sxs-lookup"><span data-stu-id="cc842-121">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="cc842-122">Выдача ответственным за</span><span class="sxs-lookup"><span data-stu-id="cc842-122">Issuing Officer</span></span>                   | <span data-ttu-id="cc842-123">Адрес электронной почты указанного выдающего ответственным за.</span><span class="sxs-lookup"><span data-stu-id="cc842-123">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="cc842-124">Дата выпуска</span><span class="sxs-lookup"><span data-stu-id="cc842-124">Issuing Date</span></span>                   | <span data-ttu-id="cc842-125">Дата, уведомление о был отправлен (UTC).</span><span class="sxs-lookup"><span data-stu-id="cc842-125">The date that the notice was issued (UTC).</span></span>              |