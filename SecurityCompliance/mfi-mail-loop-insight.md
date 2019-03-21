---
title: Аналитика почтового цикла
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: cb801985-3c89-4979-9c18-17829a4cb563
description: Администраторы могут узнать о цикле обработки почты в панели мониторинга почтовых ящиков в центре безопасности Office 365 Security _Амп_.
ms.openlocfilehash: 5fa7267d68183ea9f8117e420a769a2beaafdac1
ms.sourcegitcommit: fec1010e405f14e792d650aee0312b78fced3343
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/21/2019
ms.locfileid: "30720299"
---
# <a name="mail-loop-insight"></a><span data-ttu-id="87e4a-103">Аналитика почтового цикла</span><span class="sxs-lookup"><span data-stu-id="87e4a-103">Mail loop insight</span></span>

<span data-ttu-id="87e4a-104">Почтовый цикл является недопустимым, так как он создает неисправность системных ресурсов, использует квоту почтового ящика организации и отправляет исходным отправителям неправильные отчеты о недоставке (также называемые сообщениями NDR и Bounce).</span><span class="sxs-lookup"><span data-stu-id="87e4a-104">A mail loop is bad because it wastes system resources, consumes your organization's mail volume quota, and sends confusing non-delivery reports (also known as NDRs or bounce messages) to the original senders.</span></span> <span data-ttu-id="87e4a-105">Эти отчеты отображаются при обнаружении почтового ящика в Организации, о почтовых доменах, участвующих в цикле, а также о количестве сообщений, отправленных с предыдущего дня в цикле.</span><span class="sxs-lookup"><span data-stu-id="87e4a-105">This insight reports when a mail loop is found in your organization, the email domains that are involved in the loop, and the number of messages from the previous day that were in the loop.</span></span>

![Цикл обработки почты в панели мониторинга почтовых ящиков в центре безопасности _Амп_ соответствия требованиям Office 365](media/c3f707cb-4c89-4e88-989c-81ce1d1d6b99.png)

<span data-ttu-id="87e4a-107">Вы можете щелкнуть **Просмотреть сведения** , чтобы просмотреть подробные сведения в раскрывающейся области.</span><span class="sxs-lookup"><span data-stu-id="87e4a-107">You can click **View details** to see the details in a flyout pane.</span></span> <span data-ttu-id="87e4a-108">Мы также указываем наиболее распространенные сценарии циклов и предлагаемые действия (если они доступны) для исправления цикла.</span><span class="sxs-lookup"><span data-stu-id="87e4a-108">We also identify the most common loop scenarios and provide the recommended actions (if available) to fix the loop.</span></span>

![РасКрывающаяся панель после нажатия кнопки Просмотр сведений в неправильном цикле в панели мониторинга почтового процесса](media/f7e21300-c62f-41ec-853f-4a2775cd8aa7.png)

## <a name="see-also"></a><span data-ttu-id="87e4a-110">См. также</span><span class="sxs-lookup"><span data-stu-id="87e4a-110">See also</span></span>

<span data-ttu-id="87e4a-111">Для получения дополнительных сведений о других аналитиках почтовых ящиков в панели мониторинга для почтового процесса ознакомьтесь с разрешениями поЧтовых ящиков [в центре безопасности _Амп_ соответствия требованиям](mail-flow-insights.md).</span><span class="sxs-lookup"><span data-stu-id="87e4a-111">For more information about other mail flow insights in the mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights.md).</span></span>
