---
title: Мониторинг и составление отчетов о состоянии приложений в Microsoft 365 Security
description: В этой статье описывается, как можно получить более подробные сведения об использовании облачных приложений в Организации.
keywords: безопасность, вредоносные программы, Microsoft 365, M365, центр безопасности, монитор, отчет, приложения
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 33a10996ceaf3023d5aee58aaabf3fef54372c30
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263355"
---
# <a name="monitor-and-report-app-status-in-microsoft-365-security"></a><span data-ttu-id="040e2-104">Мониторинг и составление отчетов о состоянии приложений в Microsoft 365 Security</span><span class="sxs-lookup"><span data-stu-id="040e2-104">Monitor and report app status in Microsoft 365 security</span></span>


<span data-ttu-id="040e2-105">Эти отчеты позволяют получить более подробные сведения о том, как облачные приложения используются в Организации, в том числе типы приложений, их уровень риска и оповещения.</span><span class="sxs-lookup"><span data-stu-id="040e2-105">These reports provide more insight into how cloud apps are being used in your organization, including what kinds of apps, their level of risk, and alerts.</span></span>

## <a name="monitor-email-accounts-at-risk"></a><span data-ttu-id="040e2-106">Отслеживание учетных записей электронной почты под угрозой</span><span class="sxs-lookup"><span data-stu-id="040e2-106">Monitor email accounts at risk</span></span>

<span data-ttu-id="040e2-107">**Защита электронной почты** показывает, что учетные записи электронной почты подвержены риску.</span><span class="sxs-lookup"><span data-stu-id="040e2-107">**Email protection** shows email accounts at risk.</span></span> <span data-ttu-id="040e2-108">Вы можете выбрать учетную запись для дальнейшего изучения в центре безопасности защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="040e2-108">You can click an account to investigate further in Windows Defender Security Center.</span></span>

![Карта защиты электронной почты](./media/security-docs/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a><span data-ttu-id="040e2-110">Отслеживание разрешений на доступ к приложениям, предоставленных пользователями</span><span class="sxs-lookup"><span data-stu-id="040e2-110">Monitor app permissions granted by users</span></span>

<span data-ttu-id="040e2-111">**Cloud App Security — приложения OAuth** список приложений, обнаруженных в Cloud App Security, которым были предоставлены разрешения пользователей.</span><span class="sxs-lookup"><span data-stu-id="040e2-111">**Cloud App Security - OAuth apps** lists apps discovered by Cloud App Security that have been granted permissions by users.</span></span> <span data-ttu-id="040e2-112">В каталоге риска Cloud App Security входит свыше 16 000 приложений, которые оцениваются с помощью более 70 факторов риска.</span><span class="sxs-lookup"><span data-stu-id="040e2-112">Cloud App Security's risk catalog includes over 16,000 apps that are assessed using over 70 risk factors.</span></span>

<span data-ttu-id="040e2-113">Факторы риска начинаются с общей информации, например издателя приложения, в меры безопасности и элементы управления, например, поддерживает ли приложение шифрование на REST или предоставляет журнал аудита действий пользователя.</span><span class="sxs-lookup"><span data-stu-id="040e2-113">The risk factors start from general information, such as the app publisher, to security measures and controls, such as whether the app supports for encryption at rest or provides an audit log of user activity.</span></span>

![Карточка приложений OAuth Cloud App Security](./media/security-docs/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a><span data-ttu-id="040e2-115">Отслеживание учетных записей пользователей облачного приложения</span><span class="sxs-lookup"><span data-stu-id="040e2-115">Monitor cloud app user accounts</span></span>

<span data-ttu-id="040e2-116">**Учетные записи облачных приложений для** учетных записей списков проверки, которые могут потребовать внимания.</span><span class="sxs-lookup"><span data-stu-id="040e2-116">**Cloud app accounts for review** lists accounts that may require attention.</span></span>

![Карточка облачных учетных записей приложений для пересмотра](./media/security-docs/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a><span data-ttu-id="040e2-118">Сведения о том, какие облачные приложения используются</span><span class="sxs-lookup"><span data-stu-id="040e2-118">Understand which cloud apps are used</span></span>

<span data-ttu-id="040e2-119">**Обнаруженные облачные приложения (категории)** показывают, какие типы приложений используются в вашей организации, и ссылки на панель мониторинга облачного обнаружения в Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="040e2-119">**Discovered cloud apps (categories)** show what kinds of apps are being used in your organization and links to the Cloud Discovery dashboard in Cloud App Security.</span></span> <span data-ttu-id="040e2-120">Более подробную информацию можно найти [в разделе Краткое руководство: Working with обнаруженным приложениям](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span><span class="sxs-lookup"><span data-stu-id="040e2-120">For more information, see [Quickstart: Work with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span></span>  

![Карточка с обнаруженными категориями облачных приложений](./media/security-docs/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a><span data-ttu-id="040e2-122">Отслеживание пользователей, обращающихся к облачным приложениям</span><span class="sxs-lookup"><span data-stu-id="040e2-122">Monitor where users access cloud apps</span></span>

<span data-ttu-id="040e2-123">**Расположения облачных действий приложения** показывают, где у пользователей есть доступ к облачным приложениям.</span><span class="sxs-lookup"><span data-stu-id="040e2-123">**Cloud app activity locations** show where users are accessing cloud apps.</span></span>

![Карточка "расположение действий облачного приложения"](./media/security-docs/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a><span data-ttu-id="040e2-125">Отслеживание работоспособности для рабочих нагрузок инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="040e2-125">Monitor health for infrastructure workloads</span></span>

<span data-ttu-id="040e2-126">В центре безопасности Azure для рабочих нагрузок инфраструктуры отображаются оповещения о работоспособности **инфраструктуры** .</span><span class="sxs-lookup"><span data-stu-id="040e2-126">**Infrastructure health** shows health status alerts for infrastructure workloads in Azure Security Center.</span></span>

<span data-ttu-id="040e2-127">Центр безопасности Azure обеспечивает единую систему управления безопасностью и Advanced Threat Protection в локальной и облачной рабочих нагрузках.</span><span class="sxs-lookup"><span data-stu-id="040e2-127">Azure Security Center provides unified security management and advanced threat protection across on-premises and cloud workloads.</span></span> <span data-ttu-id="040e2-128">Вы можете собирать, искать и анализировать данные безопасности из различных источников, в том числе брандмауэров и других партнерских решений.</span><span class="sxs-lookup"><span data-stu-id="040e2-128">You can collect, search, and analyze security data from a variety of sources, including firewalls and other partner solutions.</span></span>

<span data-ttu-id="040e2-129">Для получения дополнительных сведений обратитесь [к документации центра безопасности Azure](https://docs.microsoft.com/azure/security-center/).</span><span class="sxs-lookup"><span data-stu-id="040e2-129">For more information, see [Azure Security Center Documentation](https://docs.microsoft.com/azure/security-center/).</span></span>

![Карта работоспособности инфраструктуры](./media/security-docs/infrastructure-health.png)
