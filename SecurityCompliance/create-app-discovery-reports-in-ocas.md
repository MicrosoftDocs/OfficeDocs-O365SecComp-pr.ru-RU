---
title: Создание отчетов об обнаружении приложений с помощью Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Создание отчетов с помощью приложения Office 365 облачных безопасности, которая позволяет понять, как пользователи в вашей организации с помощью Office 365 и другие приложения.
ms.openlocfilehash: 543a194ec9d441a4feea97b8ad49022094565d7a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603720"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="cc4cd-103">Создание отчетов об обнаружении приложений с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cc4cd-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

<span data-ttu-id="cc4cd-104">Расширенное управление безопасностью для Office 365 является теперь приложения облаке Безопасность в Office 365.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="cc4cd-105">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="cc4cd-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="cc4cd-106">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="cc4cd-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="cc4cd-107">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="cc4cd-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="cc4cd-108">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="cc4cd-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="cc4cd-109">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="cc4cd-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="cc4cd-110">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="cc4cd-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="cc4cd-111">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="cc4cd-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="cc4cd-112">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="cc4cd-112">You are here!</span></span>  <br/> [<span data-ttu-id="cc4cd-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cc4cd-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="cc4cd-p101">Office 365 облачных приложений помогает глобальных администраторов, администраторов безопасности и безопасности читатели получить представление о облачных служб, которые используют людей в организации. Например можно увидеть пользователи хранения и совместная работа над документами и какой объем данных загружается для приложения или служб, которые расположены вне Office 365.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="cc4cd-116">Создание отчета обнаружения приложения, вручную передать файлам журнала веб-трафика с помощью брандмауэров и прокси-серверы, а затем безопасности приложения Office 365 облачных анализирует и анализирует эти файлы для отчета.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-116">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cc4cd-p102">Необходимо быть глобальным администратором, администратор безопасности или безопасности чтения выполнять задачи, описанные в этой статье. Чтобы получить дополнительные сведения, обратитесь к разделу [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="cc4cd-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="cc4cd-119">Создание отчета с помощью приложения обнаружения</span><span class="sxs-lookup"><span data-stu-id="cc4cd-119">Create a report with app discovery</span></span>

<span data-ttu-id="cc4cd-120">Создание отчета обнаружения приложения, определение поставщика источника данных для файлов журнала, которые необходимо анализ файлов журнала и запросите отчета.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-120">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cc4cd-121">Использование веб-трафика журнала файлов, содержащих периоды пиковой нагрузки трафика для получения наиболее представление об использовании в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-121">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="cc4cd-122">Сбор вашей [веб-трафика журналов и источники данных для приложения облаке Безопасность в Office 365](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="cc4cd-122">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="cc4cd-123">Последовательно выберите пункты портал облачных приложений безопасности ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-123">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="cc4cd-124">Нажмите кнопку **обнаружить** \> **Создание нового отчета**.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-124">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="cc4cd-125">![На портале Office 365 CAS выберите обнаружения](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="cc4cd-125">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="cc4cd-126">Укажите имя и описание для отчета и выберите источник данных для веб-трафика в списке **источник данных** .</span><span class="sxs-lookup"><span data-stu-id="cc4cd-126">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="cc4cd-127">![В O365 сервера клиентского доступа, нажмите кнопку обнаружить \> создать новый отчет](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="cc4cd-127">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="cc4cd-p103">Если источник данных, который вы хотите использовать отсутствует в списке, можно запросить, что он добавляется. Выберите **другие** для **источника данных**и затем введите имя источника данных, который вы пытаетесь передать. Мы будем просмотрите журнал и сообщить, если мы добавить поддержку для источника данных, созданных его.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="cc4cd-p104">Перейдите к папке файлов журнала, собранных и выберите файлы. Файлы журнала необходимо создавать источник данных, выбранный для отчета.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="cc4cd-133">Нажмите кнопку **Создать** , чтобы начать процесс создания отчета.</span><span class="sxs-lookup"><span data-stu-id="cc4cd-133">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="cc4cd-p105">Чтобы просмотреть состояние отчета, нажмите кнопку **Управление отчетами моментальный снимок**. Когда отчет будет готов, вы увидите параметр **просмотреть отчет** .</span><span class="sxs-lookup"><span data-stu-id="cc4cd-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="cc4cd-136">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="cc4cd-136">Next steps</span></span>

- [<span data-ttu-id="cc4cd-137">Просмотрите и выполнять операции с оповещениями</span><span class="sxs-lookup"><span data-stu-id="cc4cd-137">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="cc4cd-138">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cc4cd-138">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="cc4cd-139">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="cc4cd-139">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

