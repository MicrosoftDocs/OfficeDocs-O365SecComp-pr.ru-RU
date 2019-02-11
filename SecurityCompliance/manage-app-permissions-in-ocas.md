---
title: Управление приложениями OAuth с помощью Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Приложение OAuth в облаке приложения Office 365 безопасности поможет вам управлять приложениями, пользователям для загрузки для использования с Office 365
ms.openlocfilehash: ae32e3c6b15f4ad4794a3dd08c3992adaeba655c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603690"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a><span data-ttu-id="76bd7-103">Управление приложениями OAuth с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="76bd7-103">Manage OAuth apps using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="76bd7-104">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="76bd7-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="76bd7-105">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="76bd7-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="76bd7-106">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="76bd7-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="76bd7-107">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="76bd7-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="76bd7-108">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="76bd7-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="76bd7-109">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="76bd7-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="76bd7-110">Начните развертывание</span><span class="sxs-lookup"><span data-stu-id="76bd7-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="76bd7-111">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="76bd7-111">You are here!</span></span>  <br/> [<span data-ttu-id="76bd7-112">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="76bd7-112">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="76bd7-p101">Люди привлекательности приложений и их загрузки часто, особенно приложения, с которыми пользователи обработки будет экономии времени, упрощая получить на их работе или школе сведения. Тем не менее некоторые приложения могут быть риска безопасности для вашей организации, в зависимости от какая информация они имеют доступ и как они работают эту информацию. С помощью [Приложения облаке Безопасность в Office 365](office-365-cas-overview.md)Если вы являетесь администратором глобальной или безопасности, можно управлять приложениями OAuth для вашей организации. Вы видите, используемых приложений пользователями с данными Office 365, какие разрешения эти приложения у и многое другое.</span><span class="sxs-lookup"><span data-stu-id="76bd7-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage OAuth apps for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="76bd7-117">В этой статье описывается, где можно управлять приложениями OAuth проверить, как утверждение, bПричиной уязвимости является или отчет приложения и как создать запрос на приложение.</span><span class="sxs-lookup"><span data-stu-id="76bd7-117">This article describes where to go to manage OAuth apps, how to approve, ban, or report an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a><span data-ttu-id="76bd7-118">Поиск страницы Управление OAuth приложений</span><span class="sxs-lookup"><span data-stu-id="76bd7-118">How to find the Manage OAuth apps page</span></span>

> [!NOTE]
> <span data-ttu-id="76bd7-p102">OAuth приложений осуществляется в портале облачных приложений Office 365 безопасности. Необходимо быть глобальным администратором или администратор безопасности для выполнения следующих задач. Дополнительные сведения см. Дополнительные [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="76bd7-p102">OAuth apps are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="76bd7-122">Последовательно выберите пункты портал облачных приложений безопасности ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="76bd7-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="76bd7-123">Выберите **исследовать** \> **OAuth приложений**.</span><span class="sxs-lookup"><span data-stu-id="76bd7-123">Choose **Investigate** \> **OAuth apps**.</span></span><br/><span data-ttu-id="76bd7-124">![На портале O365 сервера клиентского доступа нажмите кнопку Проверить.](media/OCAS-OAuthApps.png)</span><span class="sxs-lookup"><span data-stu-id="76bd7-124">![In the O365 CAS portal, choose Investigate.](media/OCAS-OAuthApps.png)</span></span><br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a><span data-ttu-id="76bd7-125">Что вы увидите на странице Управление OAuth приложений</span><span class="sxs-lookup"><span data-stu-id="76bd7-125">What you'll see on the Manage OAuth apps page</span></span>

<span data-ttu-id="76bd7-126">В следующей таблице описываются элементов управления и параметры, доступные на странице Управление OAuth приложений.</span><span class="sxs-lookup"><span data-stu-id="76bd7-126">The following table describes the controls and options available on the Manage OAuth apps page.</span></span>
  
|<span data-ttu-id="76bd7-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="76bd7-127">**Item**</span></span>|<span data-ttu-id="76bd7-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="76bd7-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76bd7-129">Базовая значок в панели запроса приложения</span><span class="sxs-lookup"><span data-stu-id="76bd7-129">Basic icon in the app query bar</span></span>  <br/> ![Значок, который показывает представление базового запроса для запроса](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="76bd7-131">Выберите этот параметр для переключения в расширенном режиме.</span><span class="sxs-lookup"><span data-stu-id="76bd7-131">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="76bd7-132">(Если **Базовая**, использовании расширенных представления)</span><span class="sxs-lookup"><span data-stu-id="76bd7-132">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="76bd7-133">Расширенные значок в панели запроса приложения</span><span class="sxs-lookup"><span data-stu-id="76bd7-133">Advanced icon in the app query bar</span></span>  <br/> ![Значок, который показывает представление расширенного запроса для запроса](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="76bd7-135">Выберите, чтобы переключиться в основном режиме.</span><span class="sxs-lookup"><span data-stu-id="76bd7-135">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="76bd7-136">(Если **Дополнительно**, использовании базового представления.)</span><span class="sxs-lookup"><span data-stu-id="76bd7-136">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="76bd7-137">Открытие и закрытие всех значок сведений в списке приложений</span><span class="sxs-lookup"><span data-stu-id="76bd7-137">Open or close all details icon in the app list</span></span>  <br/> ![Щелкните этот значок, чтобы открыть или закрыть все сведения для всех приложений](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="76bd7-139">Выберите этот значок, чтобы просмотреть большего или меньшего числа сведения о каждом приложения.</span><span class="sxs-lookup"><span data-stu-id="76bd7-139">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="76bd7-140">Значок экспорта в списке приложений</span><span class="sxs-lookup"><span data-stu-id="76bd7-140">Export icon in the app list</span></span>  <br/> ![Щелкните значок для экспорта в CSV-файл все приложения](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="76bd7-142">Выберите этот значок, чтобы экспортировать CSV-файл, который содержит список приложений, количество пользователей для каждого приложения разрешения, связанные с приложение, уровень разрешений, состояния приложения и использовать уровень сообщества.</span><span class="sxs-lookup"><span data-stu-id="76bd7-142">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="76bd7-143">Имя</span><span class="sxs-lookup"><span data-stu-id="76bd7-143">Name</span></span>  <br/> |<span data-ttu-id="76bd7-p103">Позволяет видеть имя app. Выберите имя, чтобы просмотреть дополнительные сведения, такие как ее описание, publisher, веб-страницы приложения и идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="76bd7-p103">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="76bd7-146">Утверждено</span><span class="sxs-lookup"><span data-stu-id="76bd7-146">Authorized by</span></span>  <br/> |<span data-ttu-id="76bd7-p104">Позволяет видеть, сколько пользователей право приложения для доступа к своей учетной записи Office 365. Выберите номер, чтобы просмотреть дополнительные сведения, такие как список учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="76bd7-p104">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="76bd7-149">Уровень разрешений</span><span class="sxs-lookup"><span data-stu-id="76bd7-149">Permissions Level</span></span>  <br/> ![Значок, указывающий на уровне permisiions для приложения](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="76bd7-p105">Используется для уровня доступа, когда приложение имеет к данным Office 365. Уровни разрешений указывают **низкий**, **Средний**или **высокий**, где **Low** могут указывать, что приложение только обращается к профиля пользователя и имя. Выберите уровень для получения дополнительных сведений, таких как разрешения полномочия для приложения, использование сообщества и связанных с ними действий в [Журнал управления](suspend-or-restore-an-account-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="76bd7-p105">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="76bd7-154">Последняя право</span><span class="sxs-lookup"><span data-stu-id="76bd7-154">Last authorized</span></span> <br/> |<span data-ttu-id="76bd7-155">Используется для просмотра дату и время последнего приложения OAuth авторизован для доступа к данным Office 365 вашей организации.</span><span class="sxs-lookup"><span data-stu-id="76bd7-155">Use this to see the date and time an OAuth app was last authorized to access your organization's Office 365 data.</span></span> <br/>  |
|<span data-ttu-id="76bd7-156">Действия</span><span class="sxs-lookup"><span data-stu-id="76bd7-156">Actions</span></span><br/>![OAuth приложений](media/OCAS-OAuthAppApproveBanReport.png)<br/> |<span data-ttu-id="76bd7-158">Используется для просмотра или чтобы пометить приложение как Утверждено или Banned, сообщить о приложении OAuth в корпорацию Майкрософт, или оставьте его как не определено.</span><span class="sxs-lookup"><span data-stu-id="76bd7-158">Use this to see or to mark an app as Approved or Banned, report an OAuth app to Microsoft, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="76bd7-159">Пометка приложения как Утверждено</span><span class="sxs-lookup"><span data-stu-id="76bd7-159">Mark an app as approved</span></span>

<span data-ttu-id="76bd7-160">На странице " **Управление OAuth приложений** " найдите приложением, которое необходимо утвердить и выберите значок **приложение пометить как Утверждено** .</span><span class="sxs-lookup"><span data-stu-id="76bd7-160">On the **Manage OAuth apps** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Выберите приложение пометить как утвержденные значок](media/OCAS-MarkOAuthApproved.png)
  
<span data-ttu-id="76bd7-162">Значок включает зеленого и приложение утверждено для пользователей Office 365.</span><span class="sxs-lookup"><span data-stu-id="76bd7-162">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="76bd7-p106">Если приложение помечены как утвержденные, нет не влияет на конечного пользователя. Визуально пометки приложений, одобренные позволяет разделять их из приложения, которые еще не были просмотрены.</span><span class="sxs-lookup"><span data-stu-id="76bd7-p106">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="76bd7-165">BПричиной уязвимости является приложения</span><span class="sxs-lookup"><span data-stu-id="76bd7-165">Ban an app</span></span>

1. <span data-ttu-id="76bd7-166">На странице " **Управление OAuth приложений** " найдите приложением, которое требуется для запрета и выберите значок **приложения пометить как запрещенный** .</span><span class="sxs-lookup"><span data-stu-id="76bd7-166">On the **Manage OAuth apps** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span><br/><span data-ttu-id="76bd7-167">![Выберите приложение пометить как запрещенных значок](media/OCAS-MarkOAuthBanned.png)</span><span class="sxs-lookup"><span data-stu-id="76bd7-167">![Choose the Mark app as banned icon](media/OCAS-MarkOAuthBanned.png)</span></span>
  
2. <span data-ttu-id="76bd7-p107">В окне сообщения уведомлений сохранить существующий текст как есть или настроить текст. Выберите, следует ли пользователи знали запретил, что их приложения.</span><span class="sxs-lookup"><span data-stu-id="76bd7-p107">In the notification message box, keep the existing text as it is, or customize the text. Choose whether to let users know that their app has been banned.</span></span> <br/>![Шаблон почты для запрещенных приложения](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. <span data-ttu-id="76bd7-171">Выберите **приложение запрещать**.</span><span class="sxs-lookup"><span data-stu-id="76bd7-171">Choose **Ban app**.</span></span>

## <a name="report-an-oauth-app-to-microsoft"></a><span data-ttu-id="76bd7-172">Сообщить о приложении OAuth в корпорацию Майкрософт</span><span class="sxs-lookup"><span data-stu-id="76bd7-172">Report an OAuth app to Microsoft</span></span>

<span data-ttu-id="76bd7-173">Если вы хотите отправить приложение OAuth в корпорацию Майкрософт для анализа, можно сообщить о этого приложения.</span><span class="sxs-lookup"><span data-stu-id="76bd7-173">If you want to submit an OAuth app to Microsoft for analysis, you can report that app.</span></span>

1. <span data-ttu-id="76bd7-174">На странице " **Управление OAuth приложений** " найдите приложение, которое вы хотите отправить для анализа.</span><span class="sxs-lookup"><span data-stu-id="76bd7-174">On the **Manage OAuth apps** page, locate the app you want to submit for analysis.</span></span>

2. <span data-ttu-id="76bd7-175">Выберите вертикальное многоточие, а затем выберите **отчет о app...**.</span><span class="sxs-lookup"><span data-stu-id="76bd7-175">Choose the vertical ellipsis, and then choose **Report app...**.</span></span><br/><span data-ttu-id="76bd7-176">![Сообщить о приложении OAuth](media/OCAS-MarkOAuthReported.png)</span><span class="sxs-lookup"><span data-stu-id="76bd7-176">![Report an OAuth app](media/OCAS-MarkOAuthReported.png)</span></span><br/>

3. <span data-ttu-id="76bd7-p108">В диалоговом окне **отчета данного приложения** чтобы указать вашей вопросов используйте раскрывающегося списка. По умолчанию выбран **этого приложения вредоносных** . Тем не менее можно выбрать один из доступных вариантов.</span><span class="sxs-lookup"><span data-stu-id="76bd7-p108">In the **Report this app** dialog box, use the drop-down list to indicate your concern. By default, **This app is malicious** is selected. However, you can choose on one of the other available options. </span></span><br/><span data-ttu-id="76bd7-180">![Сообщить о приложении OAuth](media/OCAS-ReportOAuthApp.png)</span><span class="sxs-lookup"><span data-stu-id="76bd7-180">![Report an OAuth app](media/OCAS-ReportOAuthApp.png)</span></span><br/>

4. <span data-ttu-id="76bd7-181">(Рекомендуется) Оставьте параметр для связи с вами выбран и подтвердить (или изменить) на указанный адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="76bd7-181">(Recommended) Keep the option to contact you selected, and confirm (or edit) the email address listed.</span></span>

5. <span data-ttu-id="76bd7-182">Нажмите кнопку **Submit** (Отправить).</span><span class="sxs-lookup"><span data-stu-id="76bd7-182">Choose **Submit**.</span></span> 
    
## <a name="create-an-app-query"></a><span data-ttu-id="76bd7-183">Создание запроса на приложение</span><span class="sxs-lookup"><span data-stu-id="76bd7-183">Create an app query</span></span>

<span data-ttu-id="76bd7-184">Рекомендуется использовать в расширенном режиме, которая выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="76bd7-184">We recommend using the Advanced view, which looks like this:</span></span> 

![Расширенное представление](media/OCAS-OAuthAppsAdvQueryView.png)

<span data-ttu-id="76bd7-p109">В панели запроса приложения **Дополнительно**, если вы используете базового представления. Щелкните (или коснитесь) **Дополнительно** , чтобы перейти в расширенном режиме.</span><span class="sxs-lookup"><span data-stu-id="76bd7-p109">In the app query bar, if you see **Advanced**, you're using the Basic view. Click (or tap) **Advanced** to go to the Advanced view.</span></span> 

![Основные представления](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. <span data-ttu-id="76bd7-189">В строке запроса используйте список **Выбор фильтра** для выбора параметра.</span><span class="sxs-lookup"><span data-stu-id="76bd7-189">In the query bar, use the **Select a filter** list to choose an option.</span></span> 
    - <span data-ttu-id="76bd7-190">**Приложения** Приложения с определенными именами</span><span class="sxs-lookup"><span data-stu-id="76bd7-190">**App** Apps with certain names</span></span>
    - <span data-ttu-id="76bd7-191">**Состояния приложения** Приложения, в зависимости от их состояния (утверждено, Banned или Undetermined)</span><span class="sxs-lookup"><span data-stu-id="76bd7-191">**App state** Apps based on their state (Approved, Banned, or Undetermined)</span></span>
    - <span data-ttu-id="76bd7-192">**Используйте сообщества** Приложения на основе в сообществе использовать уровни (Rare, Uncommon или общий)</span><span class="sxs-lookup"><span data-stu-id="76bd7-192">**Community use** Apps based on community use levels (Rare, Uncommon, or Common)</span></span>
    - <span data-ttu-id="76bd7-193">**Уровень разрешений** Приложения на основе определенных уровней разрешений</span><span class="sxs-lookup"><span data-stu-id="76bd7-193">**Permission level** Apps based on certain permission levels</span></span> 
    - <span data-ttu-id="76bd7-194">**Разрешения** Приложения, которым требуются определенные разрешения</span><span class="sxs-lookup"><span data-stu-id="76bd7-194">**Permissions** Apps that require certain permissions</span></span>
    - <span data-ttu-id="76bd7-195">**Publisher**  Приложения из определенных издателей</span><span class="sxs-lookup"><span data-stu-id="76bd7-195">**Publisher**  Apps from certain publishers</span></span>
    - <span data-ttu-id="76bd7-196">**Пользователь** Приложения, которые право конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="76bd7-196">**User** Apps that a certain user authorized</span></span>
   
2. <span data-ttu-id="76bd7-197">Выберите **равно** или **не равно**, а затем укажите значение для фильтра.</span><span class="sxs-lookup"><span data-stu-id="76bd7-197">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
3. <span data-ttu-id="76bd7-198">Чтобы добавить дополнительные фильтры, выберите "плюс")</span><span class="sxs-lookup"><span data-stu-id="76bd7-198">To add more filters, select the plus sign (</span></span>![Добавьте значок фильтра для запроса приложения](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="76bd7-200">), а затем повторите шаги 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="76bd7-200">), and then repeat steps 2 and 3.</span></span>
    
4. <span data-ttu-id="76bd7-201">Чтобы удалить фильтр, выберите x (</span><span class="sxs-lookup"><span data-stu-id="76bd7-201">To remove a filter, select the x (</span></span>![Удалить значок фильтра для запроса приложения](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="76bd7-203">) рядом с именем фильтра.</span><span class="sxs-lookup"><span data-stu-id="76bd7-203">) next to a filter name.</span></span>
    
<span data-ttu-id="76bd7-204">Фильтры применяются автоматически и соответствующим образом обновляется в список.</span><span class="sxs-lookup"><span data-stu-id="76bd7-204">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="76bd7-205">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="76bd7-205">Next steps</span></span>

- [<span data-ttu-id="76bd7-206">Просмотрите и выполнять операции с оповещениями</span><span class="sxs-lookup"><span data-stu-id="76bd7-206">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="76bd7-207">Проверьте [веб-трафика журналов и источники данных для приложения облаке Безопасность в Office 365](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="76bd7-207">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="76bd7-208">Обзор [использования действий для приложения облаке Безопасность в Office 365](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="76bd7-208">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

