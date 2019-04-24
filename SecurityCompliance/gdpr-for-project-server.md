---
title: GDPR для Project Server
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Узнайте, как обеспечивать соблюдение требований GDPR в локальном развертывании Project Server.
ms.openlocfilehash: 67097cdab4fdab31537cf4b6dd27ce17234c2bdc
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255287"
---
# <a name="gdpr-for-project-server"></a><span data-ttu-id="4a2bc-103">GDPR для Project Server</span><span class="sxs-lookup"><span data-stu-id="4a2bc-103">GDPR for Project Server</span></span>

<span data-ttu-id="4a2bc-p101">Project Server использует специальные скрипты для экспорта и редактирования данных пользователя в Project Web App. Ниже описывается базовый процесс.</span><span class="sxs-lookup"><span data-stu-id="4a2bc-p101">Project Server uses custom scripts to export and redact user data in Project Web App. The basic process is:</span></span>

1.  <span data-ttu-id="4a2bc-106">Найдите сайты Project Web App в ферме.</span><span class="sxs-lookup"><span data-stu-id="4a2bc-106">Find the Project Web App sites in your farm.</span></span>

2.  <span data-ttu-id="4a2bc-107">Найдите на каждом сайте проекты, содержащие данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="4a2bc-107">Find the projects in each site that contain the user.</span></span>

3.  <span data-ttu-id="4a2bc-108">Экспортируйте и просмотрите нужные типы данных.</span><span class="sxs-lookup"><span data-stu-id="4a2bc-108">Export and review the types of data that you want to review.</span></span>

4.  <span data-ttu-id="4a2bc-109">Отредактируйте данные надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="4a2bc-109">Redact data as needed.</span></span>

<span data-ttu-id="4a2bc-110">Эти действия подробно рассматриваются в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="4a2bc-110">These steps are covered in detail in the following articles:</span></span>

- [<span data-ttu-id="4a2bc-111">Экспорт данных пользователя из Project Server</span><span class="sxs-lookup"><span data-stu-id="4a2bc-111">Export user data from Project Server</span></span>](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [<span data-ttu-id="4a2bc-112">Удаление данных пользователя из Project Server</span><span class="sxs-lookup"><span data-stu-id="4a2bc-112">Delete user data from Project Server</span></span>](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


<span data-ttu-id="4a2bc-p102">Обратите внимание, что Project Server основан на SharePoint Server и регистрирует события в журналах ULS SharePoint и базе данных использования. Дополнительные сведения см. в статье [GDPR для SharePoint Server](gdpr-for-sharepoint-server.md).</span><span class="sxs-lookup"><span data-stu-id="4a2bc-p102">Note that Project Server is built on top of SharePoint Server and logs events to the SharePoint ULS logs and Usage database. See [GDPR for SharePoint Server](gdpr-for-sharepoint-server.md) for more information.</span></span>
