---
title: Отчет о карте почтового процесса
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: ''
description: Администраторы могут узнать о отчете карты почтовых ящиков в панели мониторинга "Управление почтовыми сообщениями" в центре безопасности _Амп_ соответствия требованиям.
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: bd05ff5cb78adb9dd89dbe3f69c2c3a78d2b1df9
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001142"
---
# <a name="mail-flow-map-report"></a><span data-ttu-id="6eabb-103">Отчет о карте почтового процесса</span><span class="sxs-lookup"><span data-stu-id="6eabb-103">Mail flow map report</span></span>

> [!NOTE]
> <span data-ttu-id="6eabb-104">Функции, описанные в этом разделе, не были развернуты во всех организациях Office 365 и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="6eabb-104">The features described in this topic haven't been deployed to all Office 365 organizations, and are subject to change.</span></span>

<span data-ttu-id="6eabb-105">Этот отчет предоставляет подробные сведения о том, как почтовые сообщения проходят через организацию Office 365.</span><span class="sxs-lookup"><span data-stu-id="6eabb-105">This report gives insights as to how mail flows through your Office 365 organization.</span></span> <span data-ttu-id="6eabb-106">Вы можете использовать эти сведения для изучения шаблонов, выявления аномалий и устранения проблем по мере их возникновения.</span><span class="sxs-lookup"><span data-stu-id="6eabb-106">You can use this information to learn patterns, identify anomalies, and fix issues as they arise.</span></span>

![Отчет карты поЧтовых ящиков на панели мониторинга "почтовые потоки" в центре безопасности _Амп_ соответствия требованиям](media/mail-flow-map-selected.png)

## <a name="mail-flow-map-widget"></a><span data-ttu-id="6eabb-108">Мини-приложение карты поЧтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="6eabb-108">Mail flow map widget</span></span>

<span data-ttu-id="6eabb-109">По умолчанию в карте почтовых ящиков показан шаблон почтовых ящиков высокого уровня с предыдущего дня.</span><span class="sxs-lookup"><span data-stu-id="6eabb-109">By default, the mail flow map shows the high level mail flow pattern from the previous day.</span></span> <span data-ttu-id="6eabb-110">Для разных дней можно использовать стрелки влево и вправо.</span><span class="sxs-lookup"><span data-stu-id="6eabb-110">You can use the left and right arrows for different days.</span></span> <span data-ttu-id="6eabb-111">При наВедении курсора мыши на каждую область в отчете будет показан объем почты в организации Office 365, как показано на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="6eabb-111">Hovering your mouse cursor over each area in the report will show the volume of mail to and from your Office 365 organization as shown in the following diagram:</span></span>

![Стрелки влево и вправо в мини-приложении "карта процесса почты"](media/mail-flow-map-widget.png)

## <a name="overview"></a><span data-ttu-id="6eabb-113">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="6eabb-113">Overview</span></span>

<span data-ttu-id="6eabb-114">Щелкнув мини-приложение **карты** поЧтовых ящиков, вы перейдете к отчету **карты процесса обработки почты** .</span><span class="sxs-lookup"><span data-stu-id="6eabb-114">Clicking on the **Mail flow map** widget will take you to the **Mail flow map** report.</span></span> <span data-ttu-id="6eabb-115">Вы можете увидеть более детализированный уровень отчетов, щелкнув таблица Просмотр сведений для просмотра подробных данных.</span><span class="sxs-lookup"><span data-stu-id="6eabb-115">Here you can see more granular level of report, you can click View details table to see detailed data.</span></span> <span data-ttu-id="6eabb-116">Вы также можете скачать подробный отчет, щелкнув запрос отчет.</span><span class="sxs-lookup"><span data-stu-id="6eabb-116">You can also download the detailed report by clicking Request report.</span></span>

![Представление "Обзор" в отчете карты поЧтовых ящиков](media/mail-flow-map-overview.png)

## <a name="details"></a><span data-ttu-id="6eabb-118">Сведения</span><span class="sxs-lookup"><span data-stu-id="6eabb-118">Details</span></span>

<span data-ttu-id="6eabb-119">По умолчанию для параметра **Показать данные** задано значение **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="6eabb-119">By default, **Show data for** is set to the value **Overview**.</span></span> <span data-ttu-id="6eabb-120">Если щелкнуть раскрывающийся список и выбрать **сведения**, представление будет переключаться на сведения о уровне домена.</span><span class="sxs-lookup"><span data-stu-id="6eabb-120">When you click on the drop down and select **Detail**, the view switches to the domain level detail.</span></span>

![Выбор параметра "сведения в представлении" Показать данные для в обзоре в отчете карты поЧтовых ящиков "](media/mail-flow-map-select-detail.png)

<span data-ttu-id="6eabb-122">Отображаются домены верхнего отправителя и получателя, и остальные домены будут помещены в **другие** , как показано на следующих схемах:</span><span class="sxs-lookup"><span data-stu-id="6eabb-122">The top sender and recipient domains are listed, and the rest will be put in **Others** as shown in the following diagrams:</span></span>

![Представление "сведения" в отчете о схеме почтового процесса](media/mail-flow-map-detail.png)

## <a name="related-insights"></a><span data-ttu-id="6eabb-124">Связанная аналитика</span><span class="sxs-lookup"><span data-stu-id="6eabb-124">Related insights</span></span>

<span data-ttu-id="6eabb-125">Связанные сведения отображаются под схемой поЧтовых процессов, если они доступны (например, для получения сведений о домене отПравителя или в цикле обработки почты).</span><span class="sxs-lookup"><span data-stu-id="6eabb-125">Related insights are shown beneath the Mail flow map if they're available (for example, the Sender domain insight or the Mail loop insight).</span></span>

## <a name="see-also"></a><span data-ttu-id="6eabb-126">См. также</span><span class="sxs-lookup"><span data-stu-id="6eabb-126">See also</span></span>

<span data-ttu-id="6eabb-127">Для получения дополнительных сведений о других аналитиках почтовых ящиков в панели мониторинга для почтового процесса ознакомьтесь с разрешениями поЧтовых ящиков [в центре безопасности _Амп_ соответствия требованиям](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="6eabb-127">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>