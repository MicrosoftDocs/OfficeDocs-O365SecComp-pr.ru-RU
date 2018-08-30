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
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a>Отключение в Outlook в Интернете о нежелательной почте

Нежелательная почта, фишинга и не является нежелательным сообщения можно отправить в корпорацию Майкрософт для анализа с помощью Outlook на web сообщения о нежелательной почте параметры, как описано в [отчет о нежелательной почте и фишинге в Outlook в Интернете ](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md). Если не хотите использовать эти параметры, администраторы могут быть отключены с помощью командлета [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) . 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Что нужно знать перед началом работы
<a name="sectionSection0"> </a>

- Осталось времени до завершения: 5 минут
    
- Вы должны быть назначены разрешения, перед выполнением этой процедуры или процедуры. Чтобы увидеть, какие нужны разрешения, видеть запись» политики почтовых ящиков Outlook Web App «в разделе [разрешения Outlook Web App](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) . 
    
- Перед запуском командлетов, необходимых для выключения отчетов нежелательной почты может оказаться полезным просмотреть справочную информацию в разделах [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) и [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) . 
    
## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a>Отключить нежелательной, фишинга и не является нежелательным отчетов в корпорацию Майкрософт
<a name="sectionSection1"> </a>

Для начала выполните следующий командлет, чтобы получить виртуальные каталоги, для которых требуется отключить отчеты:
  
```
Get-OwaMailboxPolicy -Identity <parameter>
```

Затем выполните следующий командлет, чтобы отключить отправку отчетов о нежелательных сообщениях и сообщениях, не являющихся таковыми, в корпорацию Майкрософт:
  
```
Set-OwaMailboxPolicy -Identity <parameter> -ReportJunkEmailEnabled $false
```

Например, следующий командлет отключает отчеты для виртуального каталога Contoso\owa:
  
```
Set-OwaMailboxPolicy -Identity Default -ReportJunkEmailEnabled $false
```

## <a name="how-do-you-know-this-worked"></a>Как проверить, что все получилось?
<a name="sectionSection2"> </a>

Выполните Get-OWAMailboxPolicy для проверки значения параметров и получить доступ к Outlook в Интернете и убедитесь, что параметры, чтобы сообщить о нежелательной фишинга и не является нежелательным недоступны. Вы сможете, по-прежнему возможность пометить сообщения как нежелательные, фишинга и не является нежелательным, но не будут иметь возможность сообщать о них. 
  

