---
title: Анализ состояния почтовых процессов верхнего домена
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Администраторы могут узнать о состоянии верхнего уровня почтовых ящиков в почтовых процессах в панели мониторинга "почтовый ящик" в центре безопасности _Амп_.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: baa69c3373623d4742d6d957a5022012fb60f7e7
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32267046"
---
# <a name="top-domain-mail-flow-status-insight"></a><span data-ttu-id="3f3a8-103">Анализ состояния почтовых процессов верхнего домена</span><span class="sxs-lookup"><span data-stu-id="3f3a8-103">Top domain mail flow status insight</span></span>

> [!NOTE]
> <span data-ttu-id="3f3a8-104">Функции, описанные в этом разделе, не были развернуты во всех организациях Office 365 и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="3f3a8-105">Сведения **о состоянии почтовых процессов верхнего уровня** предоставляют сведения о текущем состоянии доменов организации в отношении почтового процесса.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-105">The **Top domain mail flow status** insight gives you the current status for your organization's domains in terms of mail flow.</span></span> <span data-ttu-id="3f3a8-106">Эта информация поможет вам определить и устранить неполадки в доменах \*\*\*\*\*\* , в которых возникают проблемы с почтовыми сообщениями (например, невозможно получить внешние сообщения электронной почты), особенно истечения срока действия домена или доменов с неверными записями MX.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-106">This insight helps you identify and troubleshoot domains that are experiencing ***mail flow impacting*** issues (for example, unable to receive external email), especially domain expirations or domains with incorrect MX records.</span></span>

![Состояние поВерх верхнего уровня домена в панели мониторинга "почтовые потоки" в центре безопасности _Амп_ соответствия требованиям](media/domain-mail-flow-status-selected.png)

<span data-ttu-id="3f3a8-108">При нажатии кнопки **Просмотреть сведения в представлении** отобразится раскрывающееся меню, в котором вы увидите дополнительные сведения о состоянии каждого домена.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-108">When you click **View details** in the insight, a flyout appears that shows you more details for the status of each domain.</span></span>

<span data-ttu-id="3f3a8-109">Зеленая галочка для домена указывает, что текущая запись MX (при переходе на панель мониторинга "Сводка обработки почты") соответствует значению, указанному в записи, и что в течение последних двух часов домен получил электронную почту.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-109">A green check mark for a domain indicates the current MX record (when you browsed to the mail flow insights dashboard) matches the value we have on record, and that the domain has received email during the past two hours.</span></span>

<span data-ttu-id="3f3a8-110">Красный крестик для домена указывает на то, что запись MX была изменена и что в течение предыдущих 6 часов домен не получил электронную почту.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-110">A red x for a domain indicates the MX record has been changed, and that the domain has received no email during the past 6 hours.</span></span> <span data-ttu-id="3f3a8-111">Это может указывать на то, что срок действия домена истек или запись MX была неправильно обновлена.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-111">This likely indicates that your domain has expired, or that the MX record has been incorrectly updated.</span></span> <span data-ttu-id="3f3a8-112">Обратитесь к регистратору доменных имен или в службе хостинга DNS, чтобы узнать, истек ли срок действия домена, или если запись MX домена неверна.</span><span class="sxs-lookup"><span data-stu-id="3f3a8-112">Check with your domain registrar or DNS hosting service to see if the domain has expired, or if the domain's MX record is incorrect.</span></span>

![Всплывающее окно сведений в самом верхнем состоянии управления состоянием неактивных доменов](media/domain-mail-flow-status-flyout.png)

## <a name="see-also"></a><span data-ttu-id="3f3a8-114">См. также</span><span class="sxs-lookup"><span data-stu-id="3f3a8-114">See also</span></span>

<span data-ttu-id="3f3a8-115">Для получения дополнительных сведений о других аналитиках почтовых ящиков в панели мониторинга для почтового процесса ознакомьтесь с разрешениями поЧтовых ящиков [в центре безопасности _Амп_ соответствия требованиям](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="3f3a8-115">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
