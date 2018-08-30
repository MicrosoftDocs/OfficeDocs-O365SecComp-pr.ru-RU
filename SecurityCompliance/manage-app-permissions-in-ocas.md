---
title: Управление разрешениями приложений с помощью Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Разрешения для приложений в облаке приложения Office 365 безопасности помогают управлять им загрузить пользователей для использования с Office 365 данных приложений
ms.openlocfilehash: 7bda35bbbf3a16cd1d386adcb03b1c7c4176913a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535238"
---
# <a name="manage-app-permissions-using-office-365-cloud-app-security"></a><span data-ttu-id="9334e-103">Управление разрешениями приложений с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9334e-103">Manage app permissions using Office 365 Cloud App Security</span></span>

<span data-ttu-id="9334e-104">Расширенное управление безопасностью для Office 365 является теперь приложения облаке Безопасность в Office 365.</span><span class="sxs-lookup"><span data-stu-id="9334e-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="9334e-105">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="9334e-105">****Evaluation** \>**</span></span>|<span data-ttu-id="9334e-106">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="9334e-106">****Planning** \>**</span></span>|<span data-ttu-id="9334e-107">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="9334e-107">****Deployment** \>**</span></span>|<span data-ttu-id="9334e-108">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="9334e-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="9334e-109">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="9334e-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="9334e-110">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="9334e-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="9334e-111">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="9334e-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="9334e-112">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="9334e-112">You are here!</span></span>  <br/> [<span data-ttu-id="9334e-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="9334e-113">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="9334e-p101">Люди привлекательности приложений и их загрузки часто, особенно приложения, с которыми пользователи обработки будет экономии времени, упрощая получить на их работе или школе сведения. Тем не менее некоторые приложения могут быть риска безопасности для вашей организации, в зависимости от какая информация они имеют доступ и как они работают эту информацию. С помощью [Приложения облаке Безопасность в Office 365](office-365-cas-overview.md)Если вы являетесь администратором глобальной или безопасности, могут управлять разрешениями приложения для вашей организации. Вы видите, используемых приложений пользователями с данными Office 365, какие разрешения эти приложения у и многое другое.</span><span class="sxs-lookup"><span data-stu-id="9334e-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage app permissions for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="9334e-118">В этой статье описывается переход на управление разрешениями приложения, утверждении или bПричиной уязвимости является приложение и как создать запрос на приложение.</span><span class="sxs-lookup"><span data-stu-id="9334e-118">This article describes where to go to manage app permissions, how to approve or ban an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-app-permissions-page"></a><span data-ttu-id="9334e-119">Как найти страницу "Управление" разрешений приложения</span><span class="sxs-lookup"><span data-stu-id="9334e-119">How to find the Manage app permissions page</span></span>
<span data-ttu-id="9334e-120"><a name="findappperms"> </a></span><span class="sxs-lookup"><span data-stu-id="9334e-120"></span></span>

> [!NOTE]
> <span data-ttu-id="9334e-p102">Разрешения для приложений осуществляется в портале облачных приложений Office 365 безопасности. Необходимо быть глобальным администратором или администратор безопасности для выполнения следующих задач. Дополнительные сведения см. Дополнительные [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9334e-p102">App permissions are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="9334e-p103">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы для Office 365. (Вы перейдете к безопасности &amp; центре соответствия требованиям.)</span><span class="sxs-lookup"><span data-stu-id="9334e-p103">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="9334e-126">Последовательно выберите пункты **оповещения** \> **Управление расширенного оповещения**.</span><span class="sxs-lookup"><span data-stu-id="9334e-126">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="9334e-127">Щелкните (или коснитесь) **перейдите к безопасности приложения Office 365 облака**.</span><span class="sxs-lookup"><span data-stu-id="9334e-127">Click (or tap) **Go to Office 365 Cloud App Security**.</span></span>
    
    ![В разделе Безопасность &amp; центре соответствия требованиям, выберите дополнительные оповещения для перехода к безопасности Office 365 облаке приложения](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    > [!NOTE]
    > <span data-ttu-id="9334e-p104">Если безопасности Office 365 облаке приложения не включен еще, можно сделать это на этой странице. В разделе [подготовиться к работе приложения облаке Безопасность в Office 365](get-ready-for-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="9334e-p104">If Office 365 Cloud App Security is not turned on yet, you can do that on this page. See [Get ready for Office 365 Cloud App Security](get-ready-for-office-365-cas.md).</span></span> 
  
4. <span data-ttu-id="9334e-131">Нажмите кнопку **Проверить** \> **разрешений приложения**.</span><span class="sxs-lookup"><span data-stu-id="9334e-131">Choose **Investigate** \> **App permissions**.</span></span>
    
    ![На портале O365 сервера клиентского доступа нажмите кнопку Проверить.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
## <a name="what-youll-see-on-the-manage-app-permissions-page"></a><span data-ttu-id="9334e-133">Что вы увидите на странице Управление приложения разрешения</span><span class="sxs-lookup"><span data-stu-id="9334e-133">What you'll see on the Manage app permissions page</span></span>
<span data-ttu-id="9334e-134"><a name="whatsonpage"> </a></span><span class="sxs-lookup"><span data-stu-id="9334e-134"></span></span>

<span data-ttu-id="9334e-135">Ниже перечислены элементы управления и параметры, доступные на странице Управление приложения разрешения.</span><span class="sxs-lookup"><span data-stu-id="9334e-135">The following table describes the controls and options available on the Manage app permissions page.</span></span>
  
|<span data-ttu-id="9334e-136">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9334e-136">**Item**</span></span>|<span data-ttu-id="9334e-137">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9334e-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9334e-138">Базовая значок в панели запроса приложения</span><span class="sxs-lookup"><span data-stu-id="9334e-138">Basic icon in the app query bar</span></span>  <br/> ![Значок, который показывает представление базового запроса для запроса разрешений приложения](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="9334e-140">Выберите этот параметр для переключения в расширенном режиме.</span><span class="sxs-lookup"><span data-stu-id="9334e-140">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="9334e-141">(Если **Базовая**, использовании расширенных представления)</span><span class="sxs-lookup"><span data-stu-id="9334e-141">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="9334e-142">Расширенные значок в панели запроса приложения</span><span class="sxs-lookup"><span data-stu-id="9334e-142">Advanced icon in the app query bar</span></span>  <br/> ![Значок, который показывает расширенного запроса для запроса разрешений приложения](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="9334e-144">Выберите, чтобы переключиться в основном режиме.</span><span class="sxs-lookup"><span data-stu-id="9334e-144">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="9334e-145">(Если **Дополнительно**, использовании базового представления.)</span><span class="sxs-lookup"><span data-stu-id="9334e-145">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="9334e-146">Открытие и закрытие всех значок сведений в списке приложений</span><span class="sxs-lookup"><span data-stu-id="9334e-146">Open or close all details icon in the app list</span></span>  <br/> ![Щелкните этот значок, чтобы открыть или закрыть все сведения для всех приложений](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="9334e-148">Выберите этот значок, чтобы просмотреть большего или меньшего числа сведения о каждом приложения.</span><span class="sxs-lookup"><span data-stu-id="9334e-148">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="9334e-149">Значок экспорта в списке приложений</span><span class="sxs-lookup"><span data-stu-id="9334e-149">Export icon in the app list</span></span>  <br/> ![Щелкните значок для экспорта в CSV-файл все приложения](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="9334e-151">Выберите этот значок, чтобы экспортировать CSV-файл, который содержит список приложений, количество пользователей для каждого приложения разрешения, связанные с приложение, уровень разрешений, состояния приложения и использовать уровень сообщества.</span><span class="sxs-lookup"><span data-stu-id="9334e-151">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="9334e-152">Name</span><span class="sxs-lookup"><span data-stu-id="9334e-152">Name</span></span>  <br/> |<span data-ttu-id="9334e-p105">Позволяет видеть имя app. Выберите имя, чтобы просмотреть дополнительные сведения, такие как ее описание, publisher, веб-страницы приложения и идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="9334e-p105">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="9334e-155">Утверждено</span><span class="sxs-lookup"><span data-stu-id="9334e-155">Authorized by</span></span>  <br/> |<span data-ttu-id="9334e-p106">Позволяет видеть, сколько пользователей право приложения для доступа к своей учетной записи Office 365. Выберите номер, чтобы просмотреть дополнительные сведения, такие как список учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="9334e-p106">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="9334e-158">Уровень разрешений</span><span class="sxs-lookup"><span data-stu-id="9334e-158">Permissions Level</span></span>  <br/> ![Значок, указывающий на уровне permisiions для приложения](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="9334e-p107">Используется для уровня доступа, когда приложение имеет к данным Office 365. Уровни разрешений указывают **низкий**, **Средний**или **высокий**, где **Low** могут указывать, что приложение только обращается к профиля пользователя и имя. Выберите уровень для получения дополнительных сведений, таких как разрешения полномочия для приложения, использование сообщества и связанных с ними действий в [Журнал управления](suspend-or-restore-an-account-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="9334e-p107">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="9334e-163">Состояния приложения ( **Banned**, **Утверждено**или **Undetermined**)</span><span class="sxs-lookup"><span data-stu-id="9334e-163">App state ( **Banned**, **Approved**, or **Undetermined**)</span></span>  <br/> <span data-ttu-id="9334e-164">![Значки разрешения приложения после с администратором был изъят разрешены, заблокированы или никаких действий](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)</span><span class="sxs-lookup"><span data-stu-id="9334e-164">![App permissions icons after being allowed, blocked, or no action has been taken by an admin](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)</span></span>|<span data-ttu-id="9334e-165">Используется для пометки приложения как Утверждено или Banned или оставьте его как не определено.</span><span class="sxs-lookup"><span data-stu-id="9334e-165">Use this to mark an app as Approved or Banned, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="9334e-166">Пометка приложения как Утверждено</span><span class="sxs-lookup"><span data-stu-id="9334e-166">Mark an app as approved</span></span>
<span data-ttu-id="9334e-167"><a name="approveapp"> </a></span><span class="sxs-lookup"><span data-stu-id="9334e-167"></span></span>

<span data-ttu-id="9334e-168">На странице " **Управление разрешениями приложения** " найдите приложением, которое необходимо утвердить и выберите значок **приложение пометить как Утверждено** .</span><span class="sxs-lookup"><span data-stu-id="9334e-168">On the **Manage app permissions** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Выберите приложение пометить как утвержденные значок](media/dd1b7690-441a-48c9-9c3a-58466513c63d.png)
  
<span data-ttu-id="9334e-170">Значок включает зеленого и приложение утверждено для пользователей Office 365.</span><span class="sxs-lookup"><span data-stu-id="9334e-170">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9334e-p108">Если приложение помечены как утвержденные, нет не влияет на конечного пользователя. Визуально пометки приложений, одобренные позволяет разделять их из приложения, которые еще не были просмотрены.</span><span class="sxs-lookup"><span data-stu-id="9334e-p108">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="9334e-173">BПричиной уязвимости является приложения</span><span class="sxs-lookup"><span data-stu-id="9334e-173">Ban an app</span></span>
<span data-ttu-id="9334e-174"><a name="banapp"> </a></span><span class="sxs-lookup"><span data-stu-id="9334e-174"></span></span>

1. <span data-ttu-id="9334e-175">На странице " **Управление разрешениями приложения** " найдите приложением, которое требуется для запрета и выберите значок **приложения пометить как запрещенный** .</span><span class="sxs-lookup"><span data-stu-id="9334e-175">On the **Manage app permissions** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span> 
    
    ![Выберите приложение пометить как запрещенных значок](media/b9b1c5f6-fde7-46d5-8589-1564d05702b3.png)
  
2. <span data-ttu-id="9334e-177">Выберите, следует ли пользователи знали запретил, что их приложения.</span><span class="sxs-lookup"><span data-stu-id="9334e-177">Choose whether to let users know that their app has been banned.</span></span>
    
    <span data-ttu-id="9334e-178">(Рекомендуется) Чтобы пользователи знали, выберите **уведомлять пользователей, которым предоставлен доступ к этому приложению запрещенных**и добавление или изменение настраиваемого уведомления.</span><span class="sxs-lookup"><span data-stu-id="9334e-178">(Recommended) To let users know, select **Notify users who granted access to this banned app**, and add or edit a custom notification message.</span></span>
    
    <span data-ttu-id="9334e-179">Чтобы не пользователи знали, снимите флажок **уведомлять пользователей, которым предоставлен доступ к этому приложению запрещенных**.</span><span class="sxs-lookup"><span data-stu-id="9334e-179">To not let users know, clear **Notify users who granted access to this banned app**.</span></span>
    
    ![Шаблон почты для запрещенных приложения](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)
  
3. <span data-ttu-id="9334e-181">Выберите **приложение запрещать**.</span><span class="sxs-lookup"><span data-stu-id="9334e-181">Choose **Ban app**.</span></span>
    
## <a name="create-an-app-query"></a><span data-ttu-id="9334e-182">Создание запроса на приложение</span><span class="sxs-lookup"><span data-stu-id="9334e-182">Create an app query</span></span>
<span data-ttu-id="9334e-183"><a name="createapp"> </a></span><span class="sxs-lookup"><span data-stu-id="9334e-183"></span></span>

1. <span data-ttu-id="9334e-p109">В панели запроса приложения Если **Дополнительно**, щелкните (или коснитесь) его для перехода в расширенном режиме. (Если отображаются Basic используется расширенный вид; сохранить представление как есть).</span><span class="sxs-lookup"><span data-stu-id="9334e-p109">In the app query bar, if you see **Advanced**, click (or tap) it to go to the Advanced view. (If you see Basic, you are using the Advanced view; keep your view as it is.)</span></span>
    
2. <span data-ttu-id="9334e-p110">Используйте список **Выбор фильтра** для выбора параметра. В следующей таблице обобщаются параметры доступных фильтров.</span><span class="sxs-lookup"><span data-stu-id="9334e-p110">Use the **Select a filter** list to choose an option. The following table summarizes your available filter options.</span></span> 
    
|<span data-ttu-id="9334e-188">**Используйте этот фильтр**</span><span class="sxs-lookup"><span data-stu-id="9334e-188">**Use this filter**</span></span>|<span data-ttu-id="9334e-189">**Отображаемый результат**</span><span class="sxs-lookup"><span data-stu-id="9334e-189">**To display**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9334e-190">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="9334e-190">**App**</span></span> <br/> |<span data-ttu-id="9334e-191">Приложения с определенными именами</span><span class="sxs-lookup"><span data-stu-id="9334e-191">Apps with certain names</span></span>  <br/> |
|<span data-ttu-id="9334e-192">**Состояния приложения**</span><span class="sxs-lookup"><span data-stu-id="9334e-192">**App state**</span></span> <br/> |<span data-ttu-id="9334e-193">Приложения, в зависимости от их состояния (утверждено, Banned или Undetermined)</span><span class="sxs-lookup"><span data-stu-id="9334e-193">Apps based on their state (Approved, Banned, or Undetermined)</span></span>  <br/> |
|<span data-ttu-id="9334e-194">**Использование сообщества**</span><span class="sxs-lookup"><span data-stu-id="9334e-194">**Community use**</span></span> <br/> |<span data-ttu-id="9334e-195">Приложения на основе в сообществе использовать уровни (Rare, Uncommon или общий)</span><span class="sxs-lookup"><span data-stu-id="9334e-195">Apps based on community use levels (Rare, Uncommon, or Common)</span></span>  <br/> |
|<span data-ttu-id="9334e-196">**Уровень разрешений**</span><span class="sxs-lookup"><span data-stu-id="9334e-196">**Permission level**</span></span> <br/> |<span data-ttu-id="9334e-197">Приложения на основе определенных уровней разрешений</span><span class="sxs-lookup"><span data-stu-id="9334e-197">Apps based on certain permission levels</span></span>  <br/> |
|<span data-ttu-id="9334e-198">**Разрешения**</span><span class="sxs-lookup"><span data-stu-id="9334e-198">**Permissions**</span></span> <br/> |<span data-ttu-id="9334e-199">Приложения, которым требуются определенные разрешения</span><span class="sxs-lookup"><span data-stu-id="9334e-199">Apps that require certain permissions</span></span>  <br/> |
|<span data-ttu-id="9334e-200">**Издатель**</span><span class="sxs-lookup"><span data-stu-id="9334e-200">**Publisher**</span></span> <br/> |<span data-ttu-id="9334e-201">Приложения из определенных издателей</span><span class="sxs-lookup"><span data-stu-id="9334e-201">Apps from certain publishers</span></span>  <br/> |
|<span data-ttu-id="9334e-202">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="9334e-202">**User**</span></span> <br/> |<span data-ttu-id="9334e-203">Приложения, которые право конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="9334e-203">Apps that a certain user authorized</span></span>  <br/> |
   
3. <span data-ttu-id="9334e-204">Выберите **равно** или **не равно**, а затем укажите значение для фильтра.</span><span class="sxs-lookup"><span data-stu-id="9334e-204">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
4. <span data-ttu-id="9334e-205">Чтобы добавить дополнительные фильтры, выберите "плюс")</span><span class="sxs-lookup"><span data-stu-id="9334e-205">To add more filters, select the plus sign (</span></span>![Добавьте значок фильтра для запроса приложения](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="9334e-207">), а затем повторите шаги 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="9334e-207">), and then repeat steps 2 and 3.</span></span>
    
5. <span data-ttu-id="9334e-208">Чтобы удалить фильтр, выберите x (</span><span class="sxs-lookup"><span data-stu-id="9334e-208">To remove a filter, select the x (</span></span>![Удалить значок фильтра для запроса приложения](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="9334e-210">) рядом с именем фильтра.</span><span class="sxs-lookup"><span data-stu-id="9334e-210">) next to a filter name.</span></span>
    
<span data-ttu-id="9334e-211">Фильтры применяются автоматически и соответствующим образом обновляется в список.</span><span class="sxs-lookup"><span data-stu-id="9334e-211">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="9334e-212">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="9334e-212">Next steps</span></span>
<span data-ttu-id="9334e-213"><a name="nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="9334e-213"></span></span>

- [<span data-ttu-id="9334e-214">Просмотрите и выполнять операции с оповещениями</span><span class="sxs-lookup"><span data-stu-id="9334e-214">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="9334e-215">Проверьте [веб-трафика журналов и источники данных для приложения облаке Безопасность в Office 365](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="9334e-215">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="9334e-216">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="9334e-216">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

