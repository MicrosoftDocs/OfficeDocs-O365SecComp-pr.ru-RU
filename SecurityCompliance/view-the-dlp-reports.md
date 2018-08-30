---
title: Просмотр отчетов о защите от потери данных
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 41eb4324-c513-4fa5-91c8-8fbd8aaba83b
description: В отчетах защиты от потери данных в Office 365 можно быстро просмотреть число соответствия политике защиты от потери данных, переопределений или ложные срабатывания; Просмотрите ли они в случае прибора вверх или вниз по времени; отчет можно фильтровать по-разному; и посмотреть дополнительные сведения, выбрав точку на линии на диаграмме.
ms.openlocfilehash: 379e66fc3f2611cf338739d030c2b1d48e7416d8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013913"
---
# <a name="view-the-reports-for-data-loss-prevention"></a><span data-ttu-id="8d2fe-103">Просмотр отчетов о защите от потери данных</span><span class="sxs-lookup"><span data-stu-id="8d2fe-103">View the reports for data loss prevention</span></span>

<span data-ttu-id="8d2fe-p101">После создания вашего потери данных политик предотвращения (DLP), необходимо убедиться, что при работе как предназначен и помогает соответствия требованиям. С помощью защиты от потери данных отчетов в Office 365 безопасность &amp; центре соответствия требованиям, можно быстро просматривать:</span><span class="sxs-lookup"><span data-stu-id="8d2fe-p101">After you create your data loss prevention (DLP) policies, you'll want to verify that they're working as you intended and helping you to stay compliant. With the DLP reports in the Office 365 Security &amp; Compliance Center, you can quickly view:</span></span>
  
- <span data-ttu-id="8d2fe-p102">**Соответствия политике** В этом отчете отображается количество соответствия политике DLP по времени. Отчет можно фильтровать по дате, расположение, политики или действие. Можно использовать этот отчет, чтобы:</span><span class="sxs-lookup"><span data-stu-id="8d2fe-p102">**DLP policy matches** This report shows the count of DLP policy matches over time. You can filter the report by date, location, policy, or action. You can use this report to:</span></span> 
    
  - <span data-ttu-id="8d2fe-p103">Настройка параметров или уточнить политик защиты от потери данных при выполнении в тестовом режиме. Вы можете просмотреть правило, соответствие в содержимом.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-p103">Tune or refine your DLP policies as you run them in test mode. You can view the specific rule that matched the content.</span></span>
    
  - <span data-ttu-id="8d2fe-111">Сосредоточиться на определенных временных промежутках и определить причины скачков и тенденций.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-111">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>
    
  - <span data-ttu-id="8d2fe-112">Определение бизнес-процессов, которые нарушают политик защиты от потери данных вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-112">Discover business processes that violate your organization's DLP policies.</span></span>
    
  - <span data-ttu-id="8d2fe-113">Основные сведения о политик защиты от потери данных для любого бизнеса, достаточно действия, которые применяются к контенту.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-113">Understand any business impact of the DLP policies by seeing what actions are being applied to content.</span></span>
    
  - <span data-ttu-id="8d2fe-114">проверить соответствие требованиям конкретной политики защиты от потери данных, отображая все совпадения с правилами этой политики;</span><span class="sxs-lookup"><span data-stu-id="8d2fe-114">Verify compliance with a specific DLP policy by showing any matches for that policy.</span></span>
    
  - <span data-ttu-id="8d2fe-115">Просмотрите список наиболее активных пользователей и повторите пользователей, которые вносят вклад в происшествия в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-115">View a list of top users and repeat users who are contributing to incidents in your organization.</span></span>
    
  - <span data-ttu-id="8d2fe-116">Просмотр списка верхней типов конфиденциальной информации в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-116">View a list of the top types of sensitive information in your organization.</span></span>
    
- <span data-ttu-id="8d2fe-p104">**Происшествия защиты от потери данных** В этом отчете показано политики соответствия постепенно, как политики соответствует отчета. Тем не менее политика соответствует совпадения показан отчет на уровне правила; к примеру при совпадении сообщения электронной почты с трех различных правил, политики сопоставляет показаны три различных элементов строки отчета. В то же время, в отчете происшествия отображается совпадения на уровне элемента; к примеру при совпадении сообщения электронной почты с трех различных правил, отчет о происшествия показывает одного элемента строки для этой части содержимого.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-p104">**DLP incidents** This report also shows policy matches over time, like the policy matches report. However, the policy matches report shows matches at a rule level; for example, if an email matched three different rules, the policy matches report shows three different line items. By contrast, the incidents report shows matches at an item level; for example, if an email matched three different rules, the incidents report shows a single line item for that piece of content.</span></span> 
    
  <span data-ttu-id="8d2fe-p105">Так как счетчики отчета суммируются по-разному, отчет соответствия политике лучше подходит для идентификации совпадения с конкретными правилами и по настройке политик защиты от потери данных. Отчет о происшествия лучше подходит для идентификации определенные части содержимого, которые являются инспектором для политик защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-p105">Because the report counts are aggregated differently, the policy matches report is better for identifying matches with specific rules and fine tuning DLP policies. The incidents report is better for identifying specific pieces of content that are problematic for your DLP policies.</span></span>
    
- <span data-ttu-id="8d2fe-p106">**Переопределения и ложные срабатывания защиты от потери данных** Если вашей политике защиты от потери данных пользователи могут переопределить или сообщить о ложном срабатывании, в этом отчете отображается количество таких случаях по времени. Отчет можно фильтровать по дате, расположение или политики. Можно использовать этот отчет, чтобы:</span><span class="sxs-lookup"><span data-stu-id="8d2fe-p106">**DLP false positives and overrides** If your DLP policy allows users to override it or report a false positive, this report shows a count of such instances over time. You can filter the report by date, location, or policy. You can use this report to:</span></span> 
    
  - <span data-ttu-id="8d2fe-125">Настройка параметров или уточнить политик защиты от потери данных, видеть, какие политики вызовет большое количество ложных срабатываний.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-125">Tune or refine your DLP policies by seeing which policies incur a high number of false positives.</span></span>
    
  - <span data-ttu-id="8d2fe-126">Вы можете просмотрите обоснования, полученных от пользователей при устранении подсказку политики путем переопределения политики.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-126">View the justifications submitted by users when they resolve a policy tip by overriding the policy.</span></span>
    
  - <span data-ttu-id="8d2fe-127">Узнайте, где переопределяет конфликта политик защиты от потери данных с помощью допустимого бизнес-процессов с дополнительными большое количество пользователей.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-127">Discover where DLP policies conflict with valid business processes by incurring a high number of user overrides.</span></span>
    
<span data-ttu-id="8d2fe-p107">Все отчеты защиты от потери данных можно показать данные с самыми последними периодом четыре месяца. Самых последних данных может занять более 24 часов отображаться в отчетах.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-p107">All DLP reports can show data from the most recent four-month time period. The most recent data can take up to 24 hours to appear in the reports.</span></span>
  
<span data-ttu-id="8d2fe-130">Эти отчеты можно найти в безопасности &amp; центре соответствия требованиям \> **отчетов** \> **панели мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-130">You can find these reports in the Security &amp; Compliance Center \> **Reports** \> **Dashboard**.</span></span>
  
![Политики защиты от потери данных соответствует отчета](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a><span data-ttu-id="8d2fe-132">Просмотрите обоснование, предоставленные пользователем для переопределения</span><span class="sxs-lookup"><span data-stu-id="8d2fe-132">View the justification submitted by a user for an override</span></span>

<span data-ttu-id="8d2fe-133">Если вашей политике защиты от потери данных пользователи могут переопределить его, можно использовать ложных положительных и переопределить отчетов для просмотра текста, отправленных пользователями в подсказке политики.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-133">If your DLP policy allows users to override it, you can use the false positive and override report to view the text submitted by users in the policy tip.</span></span>
  
![Выравнивание поля в сведения о ложном срабатывании защиты от потери данных и переопределение отчета](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a><span data-ttu-id="8d2fe-135">Выполнение действий на исследования и рекомендации</span><span class="sxs-lookup"><span data-stu-id="8d2fe-135">Take action on insights and recommendations</span></span>

<span data-ttu-id="8d2fe-136">Отчеты можно показать рекомендации и полезные сведения о котором щелкните красный значок предупреждения, чтобы ознакомиться с подробными сведениями о возможных проблемах и ответить на возможные устранение недостатков.</span><span class="sxs-lookup"><span data-stu-id="8d2fe-136">Reports can show insights and recommendations where you can click the red warning icon to see details about potential issues and take possible remedial action.</span></span>
  
![Щелкнув значок средствами для просмотра сведений и действий, выполняемых](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a><span data-ttu-id="8d2fe-138">Ищите командлеты для защиты от потери данных отчетов</span><span class="sxs-lookup"><span data-stu-id="8d2fe-138">Find the cmdlets for the DLP reports</span></span>

<span data-ttu-id="8d2fe-139">Чтобы использовать большинство функций командлеты для системы безопасности &amp; центре соответствия требованиям, необходимо:</span><span class="sxs-lookup"><span data-stu-id="8d2fe-139">To use most of the cmdlets for the Security &amp; Compliance Center, you need to:</span></span>
  
1. [<span data-ttu-id="8d2fe-140">Подключение к Office 365 безопасность &amp; центре соответствия требованиям, с помощью удаленной оболочки PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d2fe-140">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. <span data-ttu-id="8d2fe-141">Используйте любой из этих [безопасности Office 365 &amp; центре соответствия требованиям командлеты](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="8d2fe-141">Use any of these [Office 365 Security &amp; Compliance Center cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span></span>
    
<span data-ttu-id="8d2fe-p108">Тем не менее отчеты DLP требуется запрашивать данные из по Office 365, включая Exchange Online. По этой причине командлеты для защиты от потери данных отчетов, доступны в Exchange Online Powershell — не в безопасности &amp; Powershell центр соответствия требованиям. Таким образом Чтобы использовать командлеты для защиты от потери данных отчетов, необходимо:</span><span class="sxs-lookup"><span data-stu-id="8d2fe-p108">However, DLP reports need pull data from across Office 365, including Exchange Online. For this reason, the cmdlets for the DLP reports are available in Exchange Online Powershell—not in Security &amp; Compliance Center Powershell. Therefore, to use the cmdlets for the DLP reports, you need to:</span></span>
  
1. [<span data-ttu-id="8d2fe-145">Connect to Exchange Online using remote PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d2fe-145">Connect to Exchange Online using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. <span data-ttu-id="8d2fe-146">Использование этих командлетов для защиты от потери данных отчетов:</span><span class="sxs-lookup"><span data-stu-id="8d2fe-146">Use any of these cmdlets for the DLP reports:</span></span>
    
      - [<span data-ttu-id="8d2fe-147">Get-DlpDetectionsReport</span><span class="sxs-lookup"><span data-stu-id="8d2fe-147">Get-DlpDetectionsReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [<span data-ttu-id="8d2fe-148">Get-DlpDetailReport</span><span class="sxs-lookup"><span data-stu-id="8d2fe-148">Get-DlpDetailReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

