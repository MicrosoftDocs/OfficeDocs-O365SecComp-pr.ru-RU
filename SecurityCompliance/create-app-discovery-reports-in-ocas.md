---
title: Создание отчетов об обнаружении приложений с помощью Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Создавайте отчеты с помощью Office 365 Cloud App Security, которые позволяют узнать, как пользователи в вашей организации используют Office 365 и другие приложения.
ms.openlocfilehash: 23165a52a09e5bcde46ee3ab2110dc17d0faf7f4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259646"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="c0e20-103">Создание отчетов об обнаружении приложений с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c0e20-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="c0e20-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c0e20-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="c0e20-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c0e20-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="c0e20-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="c0e20-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="c0e20-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c0e20-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="c0e20-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="c0e20-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="c0e20-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="c0e20-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="c0e20-110">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="c0e20-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="c0e20-111">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="c0e20-111">You are here!</span></span>  <br/> [<span data-ttu-id="c0e20-112">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="c0e20-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="c0e20-113">Office 365 Cloud App Security помогает глобальным администраторам, администраторам безопасности и средствам чтения безопасности получать информацию об облачных службах, которые используются в Организации.</span><span class="sxs-lookup"><span data-stu-id="c0e20-113">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using.</span></span> <span data-ttu-id="c0e20-114">Например, вы можете видеть, где пользователи хранятся и работают над документами, а также какие данные отправляются в приложения или службы вне Office 365.</span><span class="sxs-lookup"><span data-stu-id="c0e20-114">For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="c0e20-115">Чтобы создать отчет об обнаружении приложений, вручную отправьте файлы журнала веб-трафика из брандмауэров и прокси-серверов, а затем Office 365 Cloud App Security анализирует и анализирует эти файлы в отчете.</span><span class="sxs-lookup"><span data-stu-id="c0e20-115">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c0e20-116">Для выполнения задач, описанных в этой статье, необходимо быть глобальным администратором, администратором безопасности или средством чтения безопасности.</span><span class="sxs-lookup"><span data-stu-id="c0e20-116">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article.</span></span> <span data-ttu-id="c0e20-117">Чтобы узнать больше, ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="c0e20-117">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="c0e20-118">Создание отчета с обнаружением приложений</span><span class="sxs-lookup"><span data-stu-id="c0e20-118">Create a report with app discovery</span></span>

<span data-ttu-id="c0e20-119">Чтобы создать отчет об обнаружении приложений, определите источник данных поставщика для файлов журнала, которые необходимо проанализировать, выберите файлы журнала и запросите отчет.</span><span class="sxs-lookup"><span data-stu-id="c0e20-119">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c0e20-120">Используйте файлы журналов веб-трафика, которые включают пиковые периоды трафика, чтобы получить лучшее представление об использовании в Организации.</span><span class="sxs-lookup"><span data-stu-id="c0e20-120">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="c0e20-121">Сбор [журналов и источников данных веб-трафика для Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="c0e20-121">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="c0e20-122">Перейдите на портал Cloud App Security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполните вход.</span><span class="sxs-lookup"><span data-stu-id="c0e20-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="c0e20-123">Выберите **Обнаружение** \> **создать новый отчет**.</span><span class="sxs-lookup"><span data-stu-id="c0e20-123">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="c0e20-124">![На портале Office 365 CAS нажмите кнопку Обнаружение](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="c0e20-124">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="c0e20-125">Укажите имя и описание для отчета, а затем выберите источник данных для журналов веб-трафика в списке **источник данных** .</span><span class="sxs-lookup"><span data-stu-id="c0e20-125">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="c0e20-126">![В центре администрирования Office 365 выберите \> пункт Обнаружение для создания нового отчета](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="c0e20-126">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="c0e20-127">Если источник данных, который вы хотите использовать, отсутствует в списке, можно запросить его добавление.</span><span class="sxs-lookup"><span data-stu-id="c0e20-127">If a data source that you'd like to use is not listed, you can request that it be added.</span></span> <span data-ttu-id="c0e20-128">Выберите **другой** для **источника данных**, а затем введите имя источника данных, который вы пытаетесь отправить.</span><span class="sxs-lookup"><span data-stu-id="c0e20-128">Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload.</span></span> <span data-ttu-id="c0e20-129">Мы проверим журнал и узнаете, будет ли добавлена поддержка созданного им источника данных.</span><span class="sxs-lookup"><span data-stu-id="c0e20-129">We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="c0e20-130">Перейдите к расположению собранных файлов журнала и выберите файлы.</span><span class="sxs-lookup"><span data-stu-id="c0e20-130">Browse to the location of the log files you collected and select the files.</span></span> <span data-ttu-id="c0e20-131">Файлы журнала должны быть созданы источником данных, выбранным для отчета.</span><span class="sxs-lookup"><span data-stu-id="c0e20-131">The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="c0e20-132">Нажмите кнопку **создать** , чтобы начать процесс создания отчета.</span><span class="sxs-lookup"><span data-stu-id="c0e20-132">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="c0e20-133">Чтобы просмотреть состояние отчета, щелкните **Управление отчетами моментальных снимков**.</span><span class="sxs-lookup"><span data-stu-id="c0e20-133">To see the status of the report, click **Manage snapshot reports**.</span></span> <span data-ttu-id="c0e20-134">Когда отчет будет готов, вы увидите параметр **Просмотреть отчет** .</span><span class="sxs-lookup"><span data-stu-id="c0e20-134">When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="c0e20-135">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="c0e20-135">Next steps</span></span>

- [<span data-ttu-id="c0e20-136">Просмотр оповещений и выполнение действий с ними</span><span class="sxs-lookup"><span data-stu-id="c0e20-136">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="c0e20-137">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="c0e20-137">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="c0e20-138">Обзор [действий по использованию для Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="c0e20-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

