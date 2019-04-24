---
title: Оценка безопасности Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Хотите узнать, как безопасность вашей организации действительно в Office 365? Показатель безопасности здесь поможет. Показатель безопасности анализирует безопасность Организации в соответствии с обычными действиями и параметрами безопасности в Office 365 и назначает оценку.
ms.openlocfilehash: dd0dc87910853eba9f2ec3ec6752e857462b46e5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262485"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="1f8ff-105">Оценка безопасности Office 365</span><span class="sxs-lookup"><span data-stu-id="1f8ff-105">Office 365 Secure Score</span></span>

<span data-ttu-id="1f8ff-106">**Сводка** Хотите узнать, как безопасность вашей организации действительно в Office 365?</span><span class="sxs-lookup"><span data-stu-id="1f8ff-106">**Summary** Ever wonder how secure your organization really is in Office 365?</span></span> <span data-ttu-id="1f8ff-107">Показатель безопасности здесь поможет.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-107">Secure Score is here to help.</span></span> <span data-ttu-id="1f8ff-108">Показатель безопасности анализирует безопасность Организации в соответствии с обычными действиями и параметрами безопасности в Office 365 и назначает оценку.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-108">Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score.</span></span> <span data-ttu-id="1f8ff-109">В этой статье приводятся общие сведения о безопасном показателе и его использовании.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-109">Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="1f8ff-110">Получение оценки безопасности</span><span class="sxs-lookup"><span data-stu-id="1f8ff-110">How to get to Secure Score</span></span>

<span data-ttu-id="1f8ff-111">Если в вашей организации есть подписка, включающая в себя [office 365 корпоративный](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 бизнес](https://docs.microsoft.com/microsoft-365/business/)или Office 365 бизнес премиум, а у вас есть [необходимые разрешения](#required-permissions), вы можете просмотреть его оценку, посетив [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="1f8ff-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="1f8ff-112">Кроме того, вы можете посетить центр безопасности _Амп_ соответствие требованиям[https://protection.office.com](https://protection.office.com)(), где вы найдете мини-приложение "Оценка безопасности", которое обеспечивает текущий рейтинг.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![Мини-приложение "безопасность оценки"](media/SecureScoreWidget-o365.png)

<span data-ttu-id="1f8ff-114">Мини-приложение содержит ссылку на панель мониторинга безопасной оценки.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-114">The widget includes a link to your Secure Score dashboard.</span></span>

![Информационная панель безопасной оценки](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="1f8ff-116">Принципы работы</span><span class="sxs-lookup"><span data-stu-id="1f8ff-116">How it works</span></span>

<span data-ttu-id="1f8ff-117">Показатель безопасности определяет, какие службы Office 365 вы используете (например, OneDrive, SharePoint и Exchange), а затем сравнивает параметры и действия с базовым планом, установленным корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-117">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft.</span></span> <span data-ttu-id="1f8ff-118">Вы получите оценку с учетом того, насколько хорошо выровнена ваша организация с рекомендациями по обеспечению безопасности.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-118">You'll get a score based on how well aligned your organization is with security best practices.</span></span> <span data-ttu-id="1f8ff-119">Кроме того, вы можете получить рекомендации по повышению оценки Организации.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-119">You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![Очередь действий в средстве Office 365 Secure Score](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="1f8ff-121">Показатель безопасности вычисляет оценку на основе приобретенных услуг.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-121">Secure Score calculates your score based on the services you purchased.</span></span> <span data-ttu-id="1f8ff-122">Например, если вы приобрели план Exchange Online, вы не будете рассматривать функции безопасности SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-122">For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features.</span></span> <span data-ttu-id="1f8ff-123">Знаменатель показателя — это сумма всех базовых показателей для элементов управления, которые применяются к приобретенным продуктам.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-123">The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased.</span></span> <span data-ttu-id="1f8ff-124">Числитель — это сумма всех элементов управления, для которых завершены или частично завершены действия, выполняемые для выполнения этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-124">The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="1f8ff-125">Разверните действие, чтобы узнать о возможных действиях, угрозах, с которыми он поможет защитить вас, а также о количестве баллов, которые будут увеличиваться после выполнения рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Расширенное действие в средстве "безопасное средство оценки Office 365"](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="1f8ff-127">Чтобы узнать, как влияют ваши действия в системе безопасности Организации, откройте вкладку **анализатор оценок** и просмотрите историю.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Вкладка "анализатор оценок" средства "безопасное средство оценки Office 365"](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="1f8ff-129">Под диаграммой вы увидите список оценок и действий по категориям.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![Диаграмма на вкладке анализатора оценок, на которой показана Выбранная точка данных](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="1f8ff-131">Действия, помеченные как **[не подсчитаны]** , это те, которые можно выполнять в Организации, но так как они не подключены к безопасному показателю, они не оцениваются.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="1f8ff-132">На странице **анализатор оценок** щелкните точку данных на определенный день, а затем прокрутите вниз, чтобы просмотреть завершенные и незавершенные действия в этот день, чтобы узнать, какие изменения были внесены.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-132">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed.</span></span> <span data-ttu-id="1f8ff-133">Оценка вычисляется один раз в день (около 1:00 по тихоокеанскому времени).</span><span class="sxs-lookup"><span data-stu-id="1f8ff-133">The score is calculated once per day (around 1:00 AM PST).</span></span> <span data-ttu-id="1f8ff-134">Если вы вносите изменения в измеряемое действие, оценка будет автоматически обновляться на следующий день.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-134">If you make a change to a measured action, the score will automatically update the next day.</span></span> <span data-ttu-id="1f8ff-135">Изменение, которое будет отображаться в рейтинге, занимает до 48 часов.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-135">It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="1f8ff-136">Показатель безопасности не дает абсолютной меры относительно того, насколько вероятность нарушения.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-136">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="1f8ff-137">В нем выражается область, к которой вы предприняли функции, которые могут отменять риск нарушения.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-137">It expresses the extent to which you have adopted features that can offset the risk of being breached.</span></span> <span data-ttu-id="1f8ff-138">Служба не может гарантировать нарушение безопасности, и показатель безопасности не должен интерпретироваться как гарантированный.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-138">No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="1f8ff-139">Как оценка безопасности помогает</span><span class="sxs-lookup"><span data-stu-id="1f8ff-139">How Secure Score helps</span></span>

<span data-ttu-id="1f8ff-140">С помощью показателя безопасности можно повысить уровень безопасности Организации с помощью встроенных функций безопасности в Office 365 (многие из которых уже приобретены, но, возможно, не знаются).</span><span class="sxs-lookup"><span data-stu-id="1f8ff-140">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of).</span></span> <span data-ttu-id="1f8ff-141">Дополнительные сведения об этих функциях помогут вам обеспечить все заботы о том, чтобы защитить организацию от угроз.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-141">Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="1f8ff-142">Но не просто сделайте это слово.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-142">But don't just take our word for it.</span></span> <span data-ttu-id="1f8ff-143">Оценки пользователей, использующих показатель безопасности, показали, что их рейтинг возрастает в пять раз больше, чем клиенты, которые не используют его.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-143">Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it.</span></span> <span data-ttu-id="1f8ff-144">(Увеличение оценки соответствует функциям безопасности, используемым в организациях.)</span><span class="sxs-lookup"><span data-stu-id="1f8ff-144">(The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="1f8ff-145">Показатель безопасности не дает абсолютной меры относительно того, насколько вероятность нарушения.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-145">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="1f8ff-146">В нем выражается область, к которой вы предприняли элементы управления, которые могут быть смещены на нарушение риска.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-146">It expresses the extent to which you have adopted controls which can offset the risk of being breached.</span></span> <span data-ttu-id="1f8ff-147">Служба не может гарантировать нарушение безопасности, и показатель безопасности не должен интерпретироваться как гарантированный.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-147">No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="1f8ff-148">Обязательные разрешения</span><span class="sxs-lookup"><span data-stu-id="1f8ff-148">Required permissions</span></span>

<span data-ttu-id="1f8ff-149">Для просмотра и использования панели мониторинга безопасной оценки необходимо назначить одну из следующих ролей в [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span><span class="sxs-lookup"><span data-stu-id="1f8ff-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span></span>
- <span data-ttu-id="1f8ff-150">Глобальный администратор</span><span class="sxs-lookup"><span data-stu-id="1f8ff-150">Global Administrator</span></span>
- <span data-ttu-id="1f8ff-151">Администратор выставления счетов</span><span class="sxs-lookup"><span data-stu-id="1f8ff-151">Billing Administrator</span></span>
- <span data-ttu-id="1f8ff-152">Администратор пользователей</span><span class="sxs-lookup"><span data-stu-id="1f8ff-152">User Administrator</span></span>
- <span data-ttu-id="1f8ff-153">Администратор паролей</span><span class="sxs-lookup"><span data-stu-id="1f8ff-153">Password Administrator</span></span>
- <span data-ttu-id="1f8ff-154">администратор безопасности (Security Administrator).</span><span class="sxs-lookup"><span data-stu-id="1f8ff-154">Security Administrator</span></span>
- <span data-ttu-id="1f8ff-155">Средство чтения безопасности</span><span class="sxs-lookup"><span data-stu-id="1f8ff-155">Security Reader</span></span>
- <span data-ttu-id="1f8ff-156">Администратор Exchange</span><span class="sxs-lookup"><span data-stu-id="1f8ff-156">Exchange Administrator</span></span>
- <span data-ttu-id="1f8ff-157">Администратор SharePoint</span><span class="sxs-lookup"><span data-stu-id="1f8ff-157">SharePoint Administrator</span></span>

 <span data-ttu-id="1f8ff-158">Пользователи, которым не назначена роль администратора, не смогут получить доступ к показателю безопасности.</span><span class="sxs-lookup"><span data-stu-id="1f8ff-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f8ff-159">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="1f8ff-159">Related topics</span></span>

[<span data-ttu-id="1f8ff-160">Обзор панели мониторинга безопасности</span><span class="sxs-lookup"><span data-stu-id="1f8ff-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="1f8ff-161">Какая у меня подписка?</span><span class="sxs-lookup"><span data-stu-id="1f8ff-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
