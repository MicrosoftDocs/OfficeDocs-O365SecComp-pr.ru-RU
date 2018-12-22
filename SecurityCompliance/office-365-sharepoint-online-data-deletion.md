---
title: Удаление Office 365 SharePoint Online данных
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Описание удаления данных в SharePoint Online.
ms.openlocfilehash: 8a84859ce170a4c3ca713c751aef2b6d5b911c55
ms.sourcegitcommit: 29ba4c36af8e90ddc8d885863ef25bac2cffbe94
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/22/2018
ms.locfileid: "27411165"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a><span data-ttu-id="ca3dd-103">Удаление SharePoint Online данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="ca3dd-103">SharePoint Online Data Deletion in Office 365</span></span>

<span data-ttu-id="ca3dd-p101">SharePoint Online хранятся объекты как абстрактные код внутри баз данных приложения. Когда пользователь отправляет файл в SharePoint Online, этот файл является демонтировать и преобразуется в код приложения и сохраняются в нескольких таблиц по нескольким базам данных. В SharePoint Online все содержимое, которая передает клиенту разбивается на части, шифруется (потенциально несколько ключей AES 256-разрядная версия) и распределены по центра обработки данных. Подробные сведения о процессе фрагментации и шифрования см [в облаке Майкрософт](office-365-encryption-in-the-microsoft-cloud-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ca3dd-p101">SharePoint Online stores objects as abstracted code within application databases. When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases. In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter. For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span></span> 

<span data-ttu-id="ca3dd-p102">В SharePoint Online элементы будут храниться на 93 дней с момента удаления их из исходного расположения. Они остаются в корзину сайта все время, пока кто-то удалит их из него или приводит к очистке этого корзины. В этом случае элементы перейдите к семейству сайтов корзины, где они остаются в оставшейся части 93 дней. Сведения о восстановлении "Удаленные" в разделе [Восстановление элементов из корзины сайта SharePoint](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) и [Восстановление удаленных элементов из корзины семейства сайтов](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). Время хранения корзины не настраивается в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="ca3dd-p102">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location. They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin. In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days. For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="ca3dd-113">При удалении семейства веб-сайтов, необходимо также удалить иерархии сайтов в коллекции и все содержимое в них:</span><span class="sxs-lookup"><span data-stu-id="ca3dd-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>
- <span data-ttu-id="ca3dd-114">документы и библиотеки документов;</span><span class="sxs-lookup"><span data-stu-id="ca3dd-114">Documents and document libraries</span></span>
- <span data-ttu-id="ca3dd-115">Списки и данные списков</span><span class="sxs-lookup"><span data-stu-id="ca3dd-115">Lists and list data</span></span>
- <span data-ttu-id="ca3dd-116">Параметры конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="ca3dd-116">Site configuration settings</span></span>
- <span data-ttu-id="ca3dd-117">Сведения о ролях и безопасности, связанные с сайтом или дочерним сайтам</span><span class="sxs-lookup"><span data-stu-id="ca3dd-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="ca3dd-118">Дочерние сайты верхнего уровня веб-сайта, их содержимое и сведения о пользователе</span><span class="sxs-lookup"><span data-stu-id="ca3dd-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="ca3dd-119">Случайного удаления семейства веб-сайтов, его можно было восстановить глобального или SharePoint администрирования с помощью центра администрирования SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ca3dd-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span> 

<span data-ttu-id="ca3dd-p103">Жестко удаления происходит, когда пользователь удаляет удаленных элементов из корзины, семейства сайтов по истечении периода хранения и резервного копирования или администратора используется для удаления семейства веб-сайтов с помощью [командлета Remove-SPODeletedSite](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). При удалении жестко пользователем (окончательно удаляет или очищает) контента из SharePoint Online, все ключи шифрования для удаленных фрагментов, также удаляются. Блоки на дисках, сохраненные ранее удаленного фрагментов, помечаются как неиспользуемых и доступны для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="ca3dd-p103">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted. The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
