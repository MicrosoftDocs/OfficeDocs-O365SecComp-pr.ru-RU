---
title: Работайте с custodians в Advanced eDiscovery (Предварительная версия)
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
ms.openlocfilehash: 538fd7e67456bc669b9f5cf140c995a716239fc2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32240991"
---
# <a name="work-with-custodians-in-advanced-ediscovery-preview"></a><span data-ttu-id="40505-102">Работайте с custodians в Advanced eDiscovery (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="40505-102">Work with custodians in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="40505-103">Когда организация отвечает за судебное исследование, Рабочий процесс, определяющий, сохраняя и собирающий потенциально релевантный контент, отключается от людей или custodians данных в своей организации.</span><span class="sxs-lookup"><span data-stu-id="40505-103">When an organization is responding to a legal investigation, the workflow around identifying, preserving, and collecting potentially relevant content is based off people or data custodians within their organization.</span></span> <span data-ttu-id="40505-104">В случае обнаружения электронных данных эти пользователи называются *Data custodians* (или просто *custodians*) и определяются как "лица, имеющие административный контроль над документом или электронным файлом.</span><span class="sxs-lookup"><span data-stu-id="40505-104">In eDiscovery, these individuals are called *data custodians* (or just *custodians*) and are defined as "persons having administrative control of a document or electronic file.</span></span> <span data-ttu-id="40505-105">Например, хранитель сообщения электронной почты может быть владельцем почтового ящика, содержащего соответствующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="40505-105">For example, the custodian of an email message could be the owner of the mailbox which contains the relevant message.</span></span>  

<span data-ttu-id="40505-106">После начала расследования Группа обнаружения электронных данных должна быстро определить все соответствующие custodians и источники данных, связанные с этим обращением.</span><span class="sxs-lookup"><span data-stu-id="40505-106">When an investigation begins, the eDiscovery team must quickly identify all the relevant custodians and data sources related to the case.</span></span> <span data-ttu-id="40505-107">Со временем список custodians и их источники данных могут увеличиться или декреассеся.</span><span class="sxs-lookup"><span data-stu-id="40505-107">Over time, the list of custodians and their data sources may increase or decreasse.</span></span> <span data-ttu-id="40505-108">В результате организации должны поддерживать контролируемый процесс определения, сохранения и сбора контента кустодиал в течение всего жизненного цикла дела.</span><span class="sxs-lookup"><span data-stu-id="40505-108">As a result, organizations must maintain a controlled process around identifying, preserving, and collecting custodial content throughout the life cycle of a case.</span></span>

<span data-ttu-id="40505-109">В расширенном варианте обнаружения электронных данных (Preview) юридические команды могут добавлять пользователей в своей организации в виде custodians и автоматически определять и сохранять источники данных кустодиал, такие как почтовые ящики Exchange, учетные записи OneDrive и сайты SharePoint и Teams.</span><span class="sxs-lookup"><span data-stu-id="40505-109">Within an Advanced eDiscovery (Preview) case, legal teams can add individuals in their organization as custodians and automatically identify and preserve custodial data sources such as Exchange mailboxes, OneDrive accounts, and SharePoint and Teams sites.</span></span> <span data-ttu-id="40505-110">С помощью встроенного средства управления хранитель в Advanced eDiscovery (Предварительная версия) Организации могут защищать электронно хранимые данные от случайного (или намеренного) удаления и придерживаться ручного, расходного и погрешного удержания. процесса.</span><span class="sxs-lookup"><span data-stu-id="40505-110">By using the built-in custodian management tool in Advanced eDiscovery (Preview), organizations can secure electronically stored information from inadvertent (or intentional) deletion and say goodbye to manual, time consuming, and error-prone legal hold processes.</span></span> 

<span data-ttu-id="40505-111">Дополнительные сведения о работе с custodians можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="40505-111">For more information about working with custodians, see the following articles:</span></span> 

- [<span data-ttu-id="40505-112">Добавление хранителей в дело</span><span class="sxs-lookup"><span data-stu-id="40505-112">Add custodians to a case</span></span>](add-custodians-to-case.md)

- [<span data-ttu-id="40505-113">Управление custodians в случае</span><span class="sxs-lookup"><span data-stu-id="40505-113">Manage custodians in a case</span></span>](manage-new-custodians.md)

- [<span data-ttu-id="40505-114">Просмотр действий хранителя</span><span class="sxs-lookup"><span data-stu-id="40505-114">View custodian activity</span></span>](view-custodian-activity.md)

## <a name="roles-and-permissions"></a><span data-ttu-id="40505-115">Роли и разрешения</span><span class="sxs-lookup"><span data-stu-id="40505-115">Roles and permissions</span></span>

<span data-ttu-id="40505-116">В Advanced eDiscovery (Preview) можно использовать встроенную группу ролей "Диспетчер обнаружения электронных данных", чтобы назначить необходимые разрешения пользователям, чтобы они могли управлять сквозным рабочим процессом в Advanced eDiscovery (Предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="40505-116">In Advanced eDiscovery (Preview), you can use the built-in eDiscovery Manager role group to assign the necessary permissions to users so they can manage the end-to-end workflow in Advanced eDiscovery (Preview).</span></span>
