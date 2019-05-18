---
title: GDPR для Skype для бизнеса Server
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
description: Узнайте, как обеспечивать соблюдение требований GDPR в локальном развертывании Skype для бизнеса Server и Lync Server.
ms.openlocfilehash: 835876af133dfbce056ee765336c9e981732226d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154391"
---
# <a name="gdpr-for-skype-for-business-server-and-lync-server"></a><span data-ttu-id="94dea-103">GDPR для Skype для бизнеса Server и Lync Server</span><span class="sxs-lookup"><span data-stu-id="94dea-103">GDPR for Skype for Business Server and Lync Server</span></span>

<span data-ttu-id="94dea-p101">Большая часть данных Skype для бизнеса Server и Lync Server хранится в Exchange Server. К этим данным относятся:</span><span class="sxs-lookup"><span data-stu-id="94dea-p101">Most Skype for Business Server and Lync Server data is stored in Exchange Server. This includes:</span></span>

-   <span data-ttu-id="94dea-106">журнал бесед;</span><span class="sxs-lookup"><span data-stu-id="94dea-106">Conversation history</span></span>

-   <span data-ttu-id="94dea-107">уведомления и записи голосовой почты;</span><span class="sxs-lookup"><span data-stu-id="94dea-107">Voicemail notifications and transcriptions</span></span>

-   <span data-ttu-id="94dea-108">приглашения на собрания.</span><span class="sxs-lookup"><span data-stu-id="94dea-108">Meeting invites</span></span>

<span data-ttu-id="94dea-109">Используйте процедуры, описанные в статье [GDPR для Exchange Server](gdpr-for-exchange-server.md), чтобы находить, экспортировать и удалять эти данные по запросам GDPR.</span><span class="sxs-lookup"><span data-stu-id="94dea-109">Use the procedures outlined for [GDPR for Exchange Server](gdpr-for-exchange-server.md) to find, export, or delete these types of data for GDPR requests.</span></span>

<span data-ttu-id="94dea-p102">Списки контактов хранятся в базе данных SQL Server. Их можно экспортировать следующими способами:</span><span class="sxs-lookup"><span data-stu-id="94dea-p102">Contact lists are stored in the SQL Server database. They can be exported in the following ways:</span></span>

-   <span data-ttu-id="94dea-p103">Пользователи могут самостоятельно экспортировать контакты, щелкнув правой кнопкой мыши заголовок группы и выбрав команду "Копировать". При этом все контакты из этой группы будут скопированы в буфер обмена, после чего их можно будет вставить в любом приложении.</span><span class="sxs-lookup"><span data-stu-id="94dea-p103">End users themselves can export the contacts by right clicking the group header and selecting Copy. This will copy all the contacts in that group into the clipboard, which can then be pasted into any app.</span></span>

-   <span data-ttu-id="94dea-114">Вы можете экспортировать эти данные с помощью командлета [Export-CsUserData](https://docs.microsoft.com/ru-RU/powershell/module/skype/export-csuserdata).</span><span class="sxs-lookup"><span data-stu-id="94dea-114">You can use the [Export-CsUserData](https://docs.microsoft.com/en-us/powershell/module/skype/export-csuserdata) cmdlet to export this data.</span></span>

<span data-ttu-id="94dea-p104">Контент, отправленный (файлы или раздаточные материалы PowerPoint) или созданный (доска, опросы или ответы на вопросы) на собрании хранится в систематизаторе. Его также можно экспортировать, если пользователь снова войдет в собрание, срок действия которого еще не истек, и скачает отправленный контент или сделает снимки экрана (в случае созданного контента).</span><span class="sxs-lookup"><span data-stu-id="94dea-p104">Content uploaded into meetings (such as PowerPoint files or handouts) or content generated in a meeting (such as whiteboard, polls, or Q/A) is stored in the filer. This can also be exported if end users log back into any meeting that has not expired and download any uploaded content or take screenshots in the case of generated content.</span></span>

<span data-ttu-id="94dea-p105">Собрания MeetNow, не занесенные в Календарь Exchange и список контактов, а также права контактов (родственники, сотрудники и т. д.) хранятся в базе данных пользователей. В Lync Server 2013 и более поздних версий эти данные можно экспортировать с помощью командлета [Export-CsUserData](https://docs.microsoft.com/ru-RU/powershell/module/skype/export-csuserdata).</span><span class="sxs-lookup"><span data-stu-id="94dea-p105">MeetNow meetings that are not in the Exchange Calendar and Contact List and contact rights (family, co-worker, etc.) are in the User Database. In Lync Server 2013 and later, you can use the [Export-CsUserData](https://docs.microsoft.com/en-us/powershell/module/skype/export-csuserdata) cmdlet to export this data.</span></span>
