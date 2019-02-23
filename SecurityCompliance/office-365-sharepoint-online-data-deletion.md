---
title: Удаление данных в Office 365 SharePoint Online
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Пояснения об удалении данных в SharePoint Online.
ms.openlocfilehash: 6d4989bc4b503309ba50237a164bffebaff1e7af
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218429"
---
# <a name="sharepoint-online-data-deletion-in-office-365"></a><span data-ttu-id="aea2c-103">Удаление данных в SharePoint Online в Office 365</span><span class="sxs-lookup"><span data-stu-id="aea2c-103">SharePoint Online Data Deletion in Office 365</span></span>

<span data-ttu-id="aea2c-p101">SharePoint Online хранит объекты в виде абстрактного кода в базах данных приложений. Когда пользователь отправляет файл в SharePoint Online, этот файл разбивается и преобразуется в код приложения и хранится в нескольких таблицах нескольких баз данных. В SharePoint Online весь контент, который отправляет клиент, разбивается на блоки, шифруются (потенциально с несколькими ключами AES 256-bit) и распределяются в центре обработки данных. Конкретные сведения о процессе фрагментирования и шифровании приведены в разделе [Шифрование в Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span><span class="sxs-lookup"><span data-stu-id="aea2c-p101">SharePoint Online stores objects as abstracted code within application databases. When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases. In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter. For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](office-365-encryption-in-the-microsoft-cloud-overview.md).</span></span> 

<span data-ttu-id="aea2c-p102">В SharePoint Online элементы сохраняются в течение 93 дней с момента их удаления из исходного расположения. Они остаются в корзине сайта все время, если кто-то не удаляет их из нее или очищает корзину. В этом случае элементы помещаются в корзину семейства веб-сайтов, где они остаются в оставшейся части 93 дней. Сведения о восстановлении удаленных элементов см [в разделе Восстановление элементов в корзине сайта SharePoint](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) и [Восстановление удаленных элементов из корзины семейства веб-сайтов](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). Время хранения в корзине не настраивается в SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="aea2c-p102">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location. They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin. In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days. For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/en-us/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b). The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="aea2c-113">При удалении семейства веб-сайтов вы также удаляете иерархию сайтов в коллекции и весь контент в них:</span><span class="sxs-lookup"><span data-stu-id="aea2c-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>
- <span data-ttu-id="aea2c-114">документы и библиотеки документов;</span><span class="sxs-lookup"><span data-stu-id="aea2c-114">Documents and document libraries</span></span>
- <span data-ttu-id="aea2c-115">Списки и данные списков</span><span class="sxs-lookup"><span data-stu-id="aea2c-115">Lists and list data</span></span>
- <span data-ttu-id="aea2c-116">Параметры конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="aea2c-116">Site configuration settings</span></span>
- <span data-ttu-id="aea2c-117">Сведения о ролях и безопасности, связанные с сайтом или его дочерними сайтами</span><span class="sxs-lookup"><span data-stu-id="aea2c-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="aea2c-118">Дочерние сайты веб-сайта верхнего уровня, их содержимое и сведения о пользователях</span><span class="sxs-lookup"><span data-stu-id="aea2c-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="aea2c-119">Если вы случайно удалили семейство веб-сайтов, его можно восстановить с помощью глобального администратора или администратора SharePoint с помощью центра администрирования SharePoint.</span><span class="sxs-lookup"><span data-stu-id="aea2c-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span> 

<span data-ttu-id="aea2c-p103">Окончательное удаление происходит, когда пользователь удаляет удаленные элементы из корзины семейства веб-сайтов, когда истечет срок хранения и сроки резервного копирования, или когда администратор окончательно удаляет семейство сайтов с помощью [командлета Recycle-SPODeletedSite](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). При окончательном удалении (окончательном удалении или очистке) контента из SharePoint Online все ключи шифрования для удаленных блоков также удаляются. Блоки на дисках, которые ранее сохраняли удаленные блоки, помечаются как неиспользуемые и доступны для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="aea2c-p103">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/Remove-SPODeletedSite?view=sharepoint-ps). When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted. The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
