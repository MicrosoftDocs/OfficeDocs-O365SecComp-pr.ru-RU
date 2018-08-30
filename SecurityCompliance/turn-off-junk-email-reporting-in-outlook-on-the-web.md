---
title: Отключение в Outlook в Интернете о нежелательной почте
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/9/2015
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
description: Как администратор Office 365 можно отключить возможность пользователям отчетов по электронной почте как нежелательная почта.
ms.openlocfilehash: 8ee5ff87408b80c443e4cf950ce49f624096becb
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272044"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="04a1d-103">Отключение в Outlook в Интернете о нежелательной почте</span><span class="sxs-lookup"><span data-stu-id="04a1d-103">Turn off junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="04a1d-p101">Нежелательная почта, фишинга и не является нежелательным сообщения можно отправить в корпорацию Майкрософт для анализа с помощью Outlook на web сообщения о нежелательной почте параметры, как описано в [отчет о нежелательной почте и фишинге в Outlook в Интернете ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Если не хотите использовать эти параметры, администраторы могут быть отключены с помощью командлета [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) .</span><span class="sxs-lookup"><span data-stu-id="04a1d-p101">You can send junk, phishing, and not junk messages to Microsoft for analysis using the Outlook on the web junk email reporting options, as described in [Report junk email and phishing scams in Outlook on the web ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). If you don't want to use these options,admins can turn them off via the [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="04a1d-106">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="04a1d-106">What do you need to know before you begin?</span></span>
<span data-ttu-id="04a1d-107"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="04a1d-107"></span></span>

- <span data-ttu-id="04a1d-108">Осталось времени до завершения: 5 минут</span><span class="sxs-lookup"><span data-stu-id="04a1d-108">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="04a1d-p102">Вы должны быть назначены разрешения, перед выполнением этой процедуры или процедуры. Чтобы увидеть, какие нужны разрешения, видеть запись» политики почтовых ящиков Outlook Web App «в разделе [разрешения Outlook Web App](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) .</span><span class="sxs-lookup"><span data-stu-id="04a1d-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Outlook Web App mailbox policies" entry in the [Outlook Web App permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) topic.</span></span> 
    
- <span data-ttu-id="04a1d-111">Перед запуском командлетов, необходимых для выключения отчетов нежелательной почты может оказаться полезным просмотреть справочную информацию в разделах [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) и [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) .</span><span class="sxs-lookup"><span data-stu-id="04a1d-111">Before you run the cmdlets required to turn off junk email reporting, it might be helpful to review the reference information in the [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) and [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) topics.</span></span> 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a><span data-ttu-id="04a1d-112">Отключить нежелательной, фишинга и не является нежелательным отчетов в корпорацию Майкрософт</span><span class="sxs-lookup"><span data-stu-id="04a1d-112">Turn off junk, phishing, and not junk reporting to Microsoft</span></span>
<span data-ttu-id="04a1d-113"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="04a1d-113"></span></span>

<span data-ttu-id="04a1d-114">Для начала выполните следующий командлет, чтобы получить виртуальные каталоги, для которых требуется отключить отчеты:</span><span class="sxs-lookup"><span data-stu-id="04a1d-114">First, run the following cmdlet to get the virtual directories for which you want to turn off reporting:</span></span>
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

<span data-ttu-id="04a1d-115">Затем выполните следующий командлет, чтобы отключить отправку отчетов о нежелательных сообщениях и сообщениях, не являющихся таковыми, в корпорацию Майкрософт:</span><span class="sxs-lookup"><span data-stu-id="04a1d-115">Next, run the following cmdlet to turn off junk and not junk reporting to Microsoft:</span></span>
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

<span data-ttu-id="04a1d-116">Например, следующий командлет отключает отчеты для виртуального каталога Contoso\owa:</span><span class="sxs-lookup"><span data-stu-id="04a1d-116">For example, the following cmdlet turns off reporting for virtual directory Contoso\owa:</span></span>
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="04a1d-117">Как проверить, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="04a1d-117">How do you know this worked?</span></span>
<span data-ttu-id="04a1d-118"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="04a1d-118"></span></span>

<span data-ttu-id="04a1d-p103">Выполните Get-OWAMailboxPolicy для проверки значения параметров и получить доступ к Outlook в Интернете и убедитесь, что параметры, чтобы сообщить о нежелательной фишинга и не является нежелательным недоступны. Вы сможете, по-прежнему возможность пометить сообщения как нежелательные, фишинга и не является нежелательным, но не будут иметь возможность сообщать о них.</span><span class="sxs-lookup"><span data-stu-id="04a1d-p103">Run Get-OWAMailboxPolicy to check the parameter values, and then access Outlook on the web and verify that the options to report junk, phishing, and not junk are not available. You'll still be able to mark messages as junk, phishing, and not junk, but you won't be able to report them.</span></span> 
  

