---
title: Создание отчетов об обнаружении приложений с помощью Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Создание отчетов с помощью приложения Office 365 облачных безопасности, которая позволяет понять, как пользователи в вашей организации с помощью Office 365 и другие приложения.
ms.openlocfilehash: f801c70e839a62b5bbb5423ff5e7c513dd1f09b4
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706303"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="9e347-103">Создание отчетов об обнаружении приложений с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9e347-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

<span data-ttu-id="9e347-104">Расширенное управление безопасностью для Office 365 является теперь приложения облаке Безопасность в Office 365.</span><span class="sxs-lookup"><span data-stu-id="9e347-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="9e347-105">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="9e347-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="9e347-106">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="9e347-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="9e347-107">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="9e347-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="9e347-108">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="9e347-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="9e347-109">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="9e347-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="9e347-110">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="9e347-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="9e347-111">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="9e347-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="9e347-112">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="9e347-112">You are here!</span></span>  <br/> [<span data-ttu-id="9e347-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="9e347-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="9e347-p101">Office 365 облачных приложений помогает глобальных администраторов, администраторов безопасности и безопасности читатели получить представление о облачных служб, которые используют людей в организации. Например можно увидеть пользователи хранения и совместная работа над документами и какой объем данных загружается для приложения или служб, которые расположены вне Office 365.</span><span class="sxs-lookup"><span data-stu-id="9e347-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="9e347-116">Создание отчета обнаружения приложения, вручную передать файлам журнала веб-трафика с помощью брандмауэров и прокси-серверы, а затем безопасности приложения Office 365 облачных анализирует и анализирует эти файлы для отчета.</span><span class="sxs-lookup"><span data-stu-id="9e347-116">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9e347-p102">Необходимо быть глобальным администратором, администратор безопасности или безопасности чтения выполнять задачи, описанные в этой статье. Чтобы получить дополнительные сведения, обратитесь к разделу [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9e347-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="9e347-119">Создание отчета с помощью приложения обнаружения</span><span class="sxs-lookup"><span data-stu-id="9e347-119">Create a report with app discovery</span></span>

<span data-ttu-id="9e347-120">Создание отчета обнаружения приложения, определение поставщика источника данных для файлов журнала, которые необходимо анализ файлов журнала и запросите отчета.</span><span class="sxs-lookup"><span data-stu-id="9e347-120">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9e347-121">Использование веб-трафика журнала файлов, содержащих периоды пиковой нагрузки трафика для получения наиболее представление об использовании в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="9e347-121">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="9e347-122">Сбор вашей [веб-трафика журналов и источники данных для приложения облаке Безопасность в Office 365](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="9e347-122">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="9e347-123">Последовательно выберите пункты [https://security.microsoft.com](https://security.microsoft.com) и выполнить вход с помощью учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="9e347-123">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in using your work or school account.</span></span> 
    
3. <span data-ttu-id="9e347-124">В разделе Безопасность &amp; центре соответствия требованиям, выберите **оповещения** \> **Расширенное Управление оповещениями**.</span><span class="sxs-lookup"><span data-stu-id="9e347-124">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
4. <span data-ttu-id="9e347-125">Выберите, **перейдите к безопасности приложения Office 365 облака**.</span><span class="sxs-lookup"><span data-stu-id="9e347-125">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
5. <span data-ttu-id="9e347-126">Нажмите кнопку **обнаружить** \> **Создание нового отчета**.</span><span class="sxs-lookup"><span data-stu-id="9e347-126">Choose **Discover** \> **Create new report**.</span></span>
    
    ![На портале Office 365 CAS выберите обнаружения](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)
  
6. <span data-ttu-id="9e347-128">Укажите имя и описание для отчета и выберите источник данных для веб-трафика в списке **источник данных** .</span><span class="sxs-lookup"><span data-stu-id="9e347-128">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> 
    
    ![В O365 сервера клиентского доступа, нажмите кнопку обнаружить \> создать новый отчет](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)
  
    > [!NOTE]
    > <span data-ttu-id="9e347-p103">Если источник данных, который вы хотите использовать отсутствует в списке, можно запросить, что он добавляется. Выберите **другие** для **источника данных**и затем введите имя источника данных, который вы пытаетесь передать. Мы будем просмотрите журнал и сообщить, если мы добавить поддержку для источника данных, созданных его.</span><span class="sxs-lookup"><span data-stu-id="9e347-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
7. <span data-ttu-id="9e347-p104">Перейдите к папке файлов журнала, собранных и выберите файлы. Файлы журнала необходимо создавать источник данных, выбранный для отчета.</span><span class="sxs-lookup"><span data-stu-id="9e347-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
8. <span data-ttu-id="9e347-135">Нажмите кнопку **Создать** , чтобы начать процесс создания отчета.</span><span class="sxs-lookup"><span data-stu-id="9e347-135">Click **Create** to start the report creation process.</span></span> 
    
9. <span data-ttu-id="9e347-p105">Чтобы просмотреть состояние отчета, нажмите кнопку **Управление отчетами моментальный снимок**. Когда отчет будет готов, вы увидите параметр **просмотреть отчет** .</span><span class="sxs-lookup"><span data-stu-id="9e347-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="9e347-138">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="9e347-138">Next steps</span></span>

- [<span data-ttu-id="9e347-139">Просмотрите и выполнять операции с оповещениями</span><span class="sxs-lookup"><span data-stu-id="9e347-139">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="9e347-140">Просмотр результатов обнаружения приложений в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9e347-140">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="9e347-141">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="9e347-141">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

