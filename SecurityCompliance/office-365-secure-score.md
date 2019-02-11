---
title: Оценка безопасности Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/25/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Когда-либо возникнуть как безопасной организации действительно в Office 365? Безопасной показатель — здесь справки. Безопасный показатель служит для анализа безопасности вашей организации на основании регулярного действия и параметры безопасности в Office 365 и назначает оценки.
ms.openlocfilehash: bc0379e40b09e63e5fded1b1a289d40c306def91
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559092"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="23318-105">Оценка безопасности Office 365</span><span class="sxs-lookup"><span data-stu-id="23318-105">Office 365 Secure Score</span></span>

<span data-ttu-id="23318-p102">**Сводка** Когда-либо возникнуть как безопасной организации действительно в Office 365? Безопасной показатель — здесь справки. Безопасный показатель служит для анализа безопасности вашей организации на основании регулярного действия и параметры безопасности в Office 365 и назначает оценки. В этой статье Обзор безопасного счета и как его использовать.</span><span class="sxs-lookup"><span data-stu-id="23318-p102">**Summary** Ever wonder how secure your organization really is in Office 365? Secure Score is here to help. Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score. Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="23318-110">Как получить безопасного счета</span><span class="sxs-lookup"><span data-stu-id="23318-110">How to get to Secure Score</span></span>

<span data-ttu-id="23318-111">Если вашей организации есть подписка, которая включает в себя [Office 365 для предприятия](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/)или бизнеса расширенный Office 365, и у вас есть [соответствующие разрешения](#required-permissions), могут просматривать безопасной показатель вашей организации, посетив [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="23318-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="23318-112">Кроме того, можно воспользоваться & безопасности центре соответствия требованиям ([https://protection.office.com](https://protection.office.com)), можно найти мини-приложения безопасного показатель, который предоставляет ваш текущий отчет.</span><span class="sxs-lookup"><span data-stu-id="23318-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![Secure показатель мини-приложения](media/SecureScoreWidget-o365.png)

<span data-ttu-id="23318-114">Мини-приложения содержит ссылку на панель мониторинга безопасного показателя.</span><span class="sxs-lookup"><span data-stu-id="23318-114">The widget includes a link to your Secure Score dashboard.</span></span>

![Secure показатель панели мониторинга](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="23318-116">Как это работает</span><span class="sxs-lookup"><span data-stu-id="23318-116">How it works</span></span>

<span data-ttu-id="23318-p103">Безопасной показатель определяет, какие службы Office 365, вы используете (например, OneDrive, SharePoint и Exchange), затем сравнивает параметры и действия, которые базового, установленные Microsoft. Вы получите оценку, основанную на том, как также выравнивания вашей организации — это с помощью рекомендации по обеспечению безопасности. Вы получите рекомендации о действиях, которые нужно выполнить для улучшения показатель вашей организации.</span><span class="sxs-lookup"><span data-stu-id="23318-p103">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft. You'll get a score based on how well aligned your organization is with security best practices. You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![Очередь действия в средство оценки безопасности Microsoft Office 365](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="23318-p104">Безопасный показатель расчет результатов на основе служб, которую можно приобрести. Например если приобретен только план Exchange Online, ваш не результат для SharePoint Online функции безопасности. Делителя показателя — это сумма всех исходных значений для элементов управления, которые применяются к продуктам, которую можно приобрести. Числитель — это сумма всех элементов управления, для которого выполнено, или частично завершения действия для выполнения этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="23318-p104">Secure Score calculates your score based on the services you purchased. For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features. The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased. The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="23318-125">Разверните узел действие для изучения что действия, необходимые для, угрозы, он будет защиты от, и сколько указывает результатов будет увеличиваться после следовать рекомендации.</span><span class="sxs-lookup"><span data-stu-id="23318-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Расширенное действие в средство оценки безопасности Microsoft Office 365](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="23318-127">Чтобы увидеть влияние на действия пользователя в вашей организации безопасности, перейдите на вкладку **Анализатора счета** и предварительный просмотр журнала.</span><span class="sxs-lookup"><span data-stu-id="23318-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Показатель анализатора на вкладке счета безопасного Office 365](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="23318-129">Ниже диаграмме вы увидите список показателям и действия по категориям.</span><span class="sxs-lookup"><span data-stu-id="23318-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![График на вкладке анализатора показатель отображается выбранная точка данных](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="23318-131">Действия, которые помечены как **[Не фиксируются]** , можно выполнить для вашей организации, но поскольку они не подключены к безопасного показатель, они не оцениваются.</span><span class="sxs-lookup"><span data-stu-id="23318-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="23318-p105">На странице **Анализатора показатель** щелкните точки данных определенный день, затем прокрутите вниз до изменены завершенные и незавершенные действия для данного для сведения о действиях, см. Показатель вычисляется один раз в день (около 1:00 по тихоокеанскому времени). Если производится изменение измеренное действие оценки будет автоматически обновлять следующий день. Необходимое до 48 часов для изменений в силу в результатов.</span><span class="sxs-lookup"><span data-stu-id="23318-p105">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed. The score is calculated once per day (around 1:00 AM PST). If you make a change to a measured action, the score will automatically update the next day. It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="23318-p106">Безопасной показатель не express абсолютный измерения из вероятность, получение нарушенным. Он представляет область, в который были приняты функции, которые могут смещение риск нарушенным. Служба не может гарантировать, что вы не быть нарушенным и счета безопасного не следует рассматривать как было указано ранее, в каких-либо изменений.</span><span class="sxs-lookup"><span data-stu-id="23318-p106">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted features that can offset the risk of being breached. No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="23318-139">Как помогает защитить счета</span><span class="sxs-lookup"><span data-stu-id="23318-139">How Secure Score helps</span></span>

<span data-ttu-id="23318-p107">С помощью Secure счета могут помочь повышения уровня безопасности вашей организации с помощью функции встроенные функции безопасности в Office 365 (многие из которых вы уже приобрести отдельно, но необходимо учитывать). Дополнительные сведения об этих функций может дать возможность мира помните, что вы получаете правом действия, чтобы защитить организацию от угроз.</span><span class="sxs-lookup"><span data-stu-id="23318-p107">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of). Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="23318-p108">Однако не только что наш word для него. Пользователи, которые используют безопасного показатель видели их показатель увеличение пять раз больше, чем пользователи, которые не с помощью. (Повышение их показатель соответствует функции безопасности, используемых в своей организации).</span><span class="sxs-lookup"><span data-stu-id="23318-p108">But don't just take our word for it. Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it. (The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="23318-p109">Безопасной показатель не express абсолютный измерения из вероятность, получение нарушенным. Он представляет область, в который были приняты элементов управления, которые можно смещение риск нарушенным. Служба не может гарантировать, что вы не быть нарушенным и безопасного показатель не следует рассматривать как было указано ранее, в каких-либо изменений.</span><span class="sxs-lookup"><span data-stu-id="23318-p109">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted controls which can offset the risk of being breached. No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="23318-148">Необходимые разрешения</span><span class="sxs-lookup"><span data-stu-id="23318-148">Required permissions</span></span>

<span data-ttu-id="23318-149">Для просмотра и использования безопасного показатель панели мониторинга, вам необходимо назначить один из следующих ролей в Azure Active Directory:</span><span class="sxs-lookup"><span data-stu-id="23318-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in Azure Active Directory:</span></span>
- <span data-ttu-id="23318-150">Глобальный администратор</span><span class="sxs-lookup"><span data-stu-id="23318-150">Global Administrator</span></span>
- <span data-ttu-id="23318-151">Администратор выставления счетов</span><span class="sxs-lookup"><span data-stu-id="23318-151">Billing Administrator</span></span>
- <span data-ttu-id="23318-152">Администратор пользователей</span><span class="sxs-lookup"><span data-stu-id="23318-152">User Administrator</span></span>
- <span data-ttu-id="23318-153">Администратор паролей</span><span class="sxs-lookup"><span data-stu-id="23318-153">Password Administrator</span></span>
- <span data-ttu-id="23318-154">администратор безопасности (Security Administrator).</span><span class="sxs-lookup"><span data-stu-id="23318-154">Security Administrator</span></span>
- <span data-ttu-id="23318-155">Средство чтения безопасности</span><span class="sxs-lookup"><span data-stu-id="23318-155">Security Reader</span></span>
- <span data-ttu-id="23318-156">Администратор Exchange</span><span class="sxs-lookup"><span data-stu-id="23318-156">Exchange Administrator</span></span>
- <span data-ttu-id="23318-157">Администратор SharePoint</span><span class="sxs-lookup"><span data-stu-id="23318-157">SharePoint Administrator</span></span>

 <span data-ttu-id="23318-158">Пользователей, которые не назначена роль администратора не сможет получить доступ к безопасного показателя.</span><span class="sxs-lookup"><span data-stu-id="23318-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23318-159">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="23318-159">Related topics</span></span>

[<span data-ttu-id="23318-160">Общие сведения о безопасности панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="23318-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="23318-161">Какая у меня подписка?</span><span class="sxs-lookup"><span data-stu-id="23318-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)