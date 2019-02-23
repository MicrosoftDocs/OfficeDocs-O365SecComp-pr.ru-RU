---
title: Управление приложениями OAuth с помощью Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: Приложения OAuth в Office 365 Cloud App Security помогают управлять приложениями, которые пользователи загружают для использования с данными Office 365
ms.openlocfilehash: 510cb64f2267c99b783f86a69f7b7a84db8d84dd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219829"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a><span data-ttu-id="53c2d-103">Управление приложениями OAuth с помощью Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="53c2d-103">Manage OAuth apps using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="53c2d-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="53c2d-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="53c2d-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="53c2d-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="53c2d-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="53c2d-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="53c2d-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="53c2d-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="53c2d-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="53c2d-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="53c2d-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="53c2d-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="53c2d-110">Начало развертывания</span><span class="sxs-lookup"><span data-stu-id="53c2d-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="53c2d-111">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="53c2d-111">You are here!</span></span>  <br/> [<span data-ttu-id="53c2d-112">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="53c2d-112">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="53c2d-p101">Люди любят приложения и часто их скачивают, особенно в приложениях, которые просматривают люди, позволяя легко получить доступ к своей рабочей или учебной информации. Однако некоторые приложения могут представлять угрозу безопасности вашей организации, в зависимости от того, какие сведения им обращаются и как они обрабатывают эту информацию. С помощью [Office 365 Cloud App Security](office-365-cas-overview.md), если вы являетесь администратором глобального или безопасности, вы можете управлять приложениями OAuth для Организации. Вы можете видеть, что пользователи используют данные Office 365, какие разрешения у этих приложений и другие.</span><span class="sxs-lookup"><span data-stu-id="53c2d-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage OAuth apps for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="53c2d-117">В этой статье описывается, как можно перейти к разделу Управление приложениями OAuth, как утвердить, запретить или сообщить о приложении, а также о том, как создать запрос приложения.</span><span class="sxs-lookup"><span data-stu-id="53c2d-117">This article describes where to go to manage OAuth apps, how to approve, ban, or report an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a><span data-ttu-id="53c2d-118">Как найти страницу "Управление приложениями OAuth"</span><span class="sxs-lookup"><span data-stu-id="53c2d-118">How to find the Manage OAuth apps page</span></span>

> [!NOTE]
> <span data-ttu-id="53c2d-p102">Управление приложениями OAuth осуществляется на портале Cloud App Security для Office 365. Для выполнения следующей задачи необходимо быть глобальным администратором или администратором безопасности. Чтобы узнать больше, ознакомьтесь с разРешениями [в &amp; центре безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="53c2d-p102">OAuth apps are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="53c2d-122">Перейдите на портал Cloud App Security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполните вход.</span><span class="sxs-lookup"><span data-stu-id="53c2d-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="53c2d-123">Выберите пункт **исследование** \> **приложений OAuth**.</span><span class="sxs-lookup"><span data-stu-id="53c2d-123">Choose **Investigate** \> **OAuth apps**.</span></span><br/><span data-ttu-id="53c2d-124">![На портале Office 365 CAS нажмите кнопку исследовать.](media/OCAS-OAuthApps.png)</span><span class="sxs-lookup"><span data-stu-id="53c2d-124">![In the O365 CAS portal, choose Investigate.](media/OCAS-OAuthApps.png)</span></span><br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a><span data-ttu-id="53c2d-125">Что вы увидите на странице "Управление приложениями OAuth"</span><span class="sxs-lookup"><span data-stu-id="53c2d-125">What you'll see on the Manage OAuth apps page</span></span>

<span data-ttu-id="53c2d-126">В следующей таблице описываются элементы управления и параметры, доступные на странице "Управление приложениями OAuth".</span><span class="sxs-lookup"><span data-stu-id="53c2d-126">The following table describes the controls and options available on the Manage OAuth apps page.</span></span>
  
|<span data-ttu-id="53c2d-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="53c2d-127">**Item**</span></span>|<span data-ttu-id="53c2d-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="53c2d-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53c2d-129">Основной значок на панели запроса приложения</span><span class="sxs-lookup"><span data-stu-id="53c2d-129">Basic icon in the app query bar</span></span>  <br/> ![Значок, указывающий основное представление запроса для запросов](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="53c2d-131">Выберите этот параметр, чтобы перейти к расширенному режиму.</span><span class="sxs-lookup"><span data-stu-id="53c2d-131">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="53c2d-132">(Если вы видите раздел **Basic**, вы используете расширенное представление)</span><span class="sxs-lookup"><span data-stu-id="53c2d-132">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="53c2d-133">Расширенный значок на панели запроса приложения</span><span class="sxs-lookup"><span data-stu-id="53c2d-133">Advanced icon in the app query bar</span></span>  <br/> ![Значок, указывающий на расширенное представление запросов для запросов](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="53c2d-135">Выберите этот параметр, чтобы перейти в базовое представление.</span><span class="sxs-lookup"><span data-stu-id="53c2d-135">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="53c2d-136">(Если вы видите **Расширенный**, вы используете базовое представление.)</span><span class="sxs-lookup"><span data-stu-id="53c2d-136">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="53c2d-137">Значок "Открыть" или "закрыть все сведения" в списке приложений</span><span class="sxs-lookup"><span data-stu-id="53c2d-137">Open or close all details icon in the app list</span></span>  <br/> ![Щелкните этот значок, чтобы открыть или закрыть все сведения для всех приложений](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="53c2d-139">Щелкните этот значок, чтобы просмотреть больше или меньше сведений о каждом приложении.</span><span class="sxs-lookup"><span data-stu-id="53c2d-139">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="53c2d-140">Значок экспорта в списке приложений</span><span class="sxs-lookup"><span data-stu-id="53c2d-140">Export icon in the app list</span></span>  <br/> ![Щелкните этот значок, чтобы экспортировать CSV-файл всех приложений](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="53c2d-142">Выберите этот значок, чтобы экспортировать CSV-файл, содержащий список приложений, число пользователей для каждого приложения, разрешения, связанные с приложением, уровнем разрешений, состоянием приложения и уровнем использования сообщества.</span><span class="sxs-lookup"><span data-stu-id="53c2d-142">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="53c2d-143">Имя</span><span class="sxs-lookup"><span data-stu-id="53c2d-143">Name</span></span>  <br/> |<span data-ttu-id="53c2d-p103">Используйте этот параметр для просмотра имени приложения. Выберите имя, чтобы просмотреть дополнительные сведения, такие как описание, издатель, веб-сайт приложения и идентификатор приложения.</span><span class="sxs-lookup"><span data-stu-id="53c2d-p103">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="53c2d-146">Авторизовано</span><span class="sxs-lookup"><span data-stu-id="53c2d-146">Authorized by</span></span>  <br/> |<span data-ttu-id="53c2d-p104">Используйте этот параметр, чтобы узнать, сколько пользователей авторизовано в приложении для доступа к своей учетной записи Office 365. Выберите число, чтобы просмотреть дополнительные сведения, например список учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="53c2d-p104">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="53c2d-149">Уровень разрешений</span><span class="sxs-lookup"><span data-stu-id="53c2d-149">Permissions Level</span></span>  <br/> ![Значок, указывающий уровень пермисиионс для приложения](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="53c2d-p105">Используйте этот параметр, чтобы узнать, какой объем доступа к приложению имеет Office 365. Уровни разрешений указывают на **низкие**, **средние**или **высокие**, где **недостаток** может означать, что приложение получает доступ только к профилю и имени пользователя. Выберите уровень, чтобы просмотреть дополнительные сведения, такие как разрешения, предоставленные приложению, использованию сообщества и связанные действия в [журнале](suspend-or-restore-an-account-in-ocas.md)управления.</span><span class="sxs-lookup"><span data-stu-id="53c2d-p105">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="53c2d-154">Последняя авторизация</span><span class="sxs-lookup"><span data-stu-id="53c2d-154">Last authorized</span></span> <br/> |<span data-ttu-id="53c2d-155">Используйте этот параметр, чтобы узнать дату и время, когда приложение OAuth получило Последнее разрешение на доступ к данным Office 365 вашей организации.</span><span class="sxs-lookup"><span data-stu-id="53c2d-155">Use this to see the date and time an OAuth app was last authorized to access your organization's Office 365 data.</span></span> <br/>  |
|<span data-ttu-id="53c2d-156">Действия</span><span class="sxs-lookup"><span data-stu-id="53c2d-156">Actions</span></span><br/>![Приложения OAuth](media/OCAS-OAuthAppApproveBanReport.png)<br/> |<span data-ttu-id="53c2d-158">Используйте эту возможность, чтобы просмотреть или пометить приложение как утвержденное или запрещенное, сообщить о приложении OAuth в корпорацию Майкрософт или оставить его неопределенным.</span><span class="sxs-lookup"><span data-stu-id="53c2d-158">Use this to see or to mark an app as Approved or Banned, report an OAuth app to Microsoft, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="53c2d-159">ПоМетка приложения как утвержденного</span><span class="sxs-lookup"><span data-stu-id="53c2d-159">Mark an app as approved</span></span>

<span data-ttu-id="53c2d-160">На странице " **Управление приложениями OAuth** " выберите приложение, которое нужно утвердить, и щелкните значок пометить **приложение как утвержденное** .</span><span class="sxs-lookup"><span data-stu-id="53c2d-160">On the **Manage OAuth apps** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Выберите значок "поМетить приложение как утвержденное"](media/OCAS-MarkOAuthApproved.png)
  
<span data-ttu-id="53c2d-162">Значок становится зеленым, а приложение утверждается для всех пользователей Office 365.</span><span class="sxs-lookup"><span data-stu-id="53c2d-162">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="53c2d-p106">Если вы пометите приложение как утвержденное, не оказывает никакого действия для конечного пользователя. Визуальная маркировка утвержденных приложений поможет отделить их от приложений, которые еще не были проверены.</span><span class="sxs-lookup"><span data-stu-id="53c2d-p106">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="53c2d-165">Запретить приложение</span><span class="sxs-lookup"><span data-stu-id="53c2d-165">Ban an app</span></span>

1. <span data-ttu-id="53c2d-166">На странице " **Управление приложениями OAuth** " выберите приложение, которое нужно запретить, и нажмите значок пометить **приложение как заблокированный** .</span><span class="sxs-lookup"><span data-stu-id="53c2d-166">On the **Manage OAuth apps** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span><br/><span data-ttu-id="53c2d-167">![Выберите значок "поМетить приложение как заблокированные"](media/OCAS-MarkOAuthBanned.png)</span><span class="sxs-lookup"><span data-stu-id="53c2d-167">![Choose the Mark app as banned icon](media/OCAS-MarkOAuthBanned.png)</span></span>
  
2. <span data-ttu-id="53c2d-p107">В поле сообщение уведомления оставьте существующий текст как есть или настройте текст. Укажите, следует ли уведомить пользователей о том, что их приложение заблокировано.</span><span class="sxs-lookup"><span data-stu-id="53c2d-p107">In the notification message box, keep the existing text as it is, or customize the text. Choose whether to let users know that their app has been banned.</span></span> <br/>![Шаблон почты для запрещенного приложения](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. <span data-ttu-id="53c2d-171">Выберите пункт запретить **приложению**.</span><span class="sxs-lookup"><span data-stu-id="53c2d-171">Choose **Ban app**.</span></span>

## <a name="report-an-oauth-app-to-microsoft"></a><span data-ttu-id="53c2d-172">Отправка отчета о приложении OAuth в корпорацию Майкрософт</span><span class="sxs-lookup"><span data-stu-id="53c2d-172">Report an OAuth app to Microsoft</span></span>

<span data-ttu-id="53c2d-173">Если вы хотите отправить приложение OAuth в корпорацию Майкрософт для анализа, вы можете сообщить об этом приложении.</span><span class="sxs-lookup"><span data-stu-id="53c2d-173">If you want to submit an OAuth app to Microsoft for analysis, you can report that app.</span></span>

1. <span data-ttu-id="53c2d-174">На странице " **Управление приложениями OAuth** " выберите приложение, которое вы хотите послать для анализа.</span><span class="sxs-lookup"><span data-stu-id="53c2d-174">On the **Manage OAuth apps** page, locate the app you want to submit for analysis.</span></span>

2. <span data-ttu-id="53c2d-175">Нажмите вертикальное многоточие, а затем выберите пункт **приложение отчета...**.</span><span class="sxs-lookup"><span data-stu-id="53c2d-175">Choose the vertical ellipsis, and then choose **Report app...**.</span></span><br/><span data-ttu-id="53c2d-176">![Отчет о приложении OAuth](media/OCAS-MarkOAuthReported.png)</span><span class="sxs-lookup"><span data-stu-id="53c2d-176">![Report an OAuth app](media/OCAS-MarkOAuthReported.png)</span></span><br/>

3. <span data-ttu-id="53c2d-p108">В диалоговом окне **сообщить об этом приложении** используйте раскрывающийся список, чтобы указать вашу проблему. По умолчанию **это приложение является вредоносным** . Однако можно выбрать один из доступных вариантов.</span><span class="sxs-lookup"><span data-stu-id="53c2d-p108">In the **Report this app** dialog box, use the drop-down list to indicate your concern. By default, **This app is malicious** is selected. However, you can choose on one of the other available options. </span></span><br/><span data-ttu-id="53c2d-180">![Отчет о приложении OAuth](media/OCAS-ReportOAuthApp.png)</span><span class="sxs-lookup"><span data-stu-id="53c2d-180">![Report an OAuth app](media/OCAS-ReportOAuthApp.png)</span></span><br/>

4. <span data-ttu-id="53c2d-181">Предложен Оставьте параметр выбранным для контакта, а затем подтвердите (или измените) адрес электронной почты в списке.</span><span class="sxs-lookup"><span data-stu-id="53c2d-181">(Recommended) Keep the option to contact you selected, and confirm (or edit) the email address listed.</span></span>

5. <span data-ttu-id="53c2d-182">Нажмите кнопку **Submit** (Отправить).</span><span class="sxs-lookup"><span data-stu-id="53c2d-182">Choose **Submit**.</span></span> 
    
## <a name="create-an-app-query"></a><span data-ttu-id="53c2d-183">Создание запроса приложения</span><span class="sxs-lookup"><span data-stu-id="53c2d-183">Create an app query</span></span>

<span data-ttu-id="53c2d-184">Рекомендуется использовать расширенное представление, которое выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="53c2d-184">We recommend using the Advanced view, which looks like this:</span></span> 

![Расширенное представление](media/OCAS-OAuthAppsAdvQueryView.png)

<span data-ttu-id="53c2d-p109">В панели запроса приложения, если вы видите **Расширенный**, вы используете базовое представление. Нажмите кнопку **Дополнительно** , чтобы перейти к расширенному представлению.</span><span class="sxs-lookup"><span data-stu-id="53c2d-p109">In the app query bar, if you see **Advanced**, you're using the Basic view. Click (or tap) **Advanced** to go to the Advanced view.</span></span> 

![Основное представление](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. <span data-ttu-id="53c2d-189">В области запроса используйте список **Выбор фильтра** для выбора варианта.</span><span class="sxs-lookup"><span data-stu-id="53c2d-189">In the query bar, use the **Select a filter** list to choose an option.</span></span> 
    - <span data-ttu-id="53c2d-190">**Приложение** Приложения с определенными именами</span><span class="sxs-lookup"><span data-stu-id="53c2d-190">**App** Apps with certain names</span></span>
    - <span data-ttu-id="53c2d-191">**Состояние приложения** Приложения на основе их состояния (утверждено, не определено или не определено)</span><span class="sxs-lookup"><span data-stu-id="53c2d-191">**App state** Apps based on their state (Approved, Banned, or Undetermined)</span></span>
    - <span data-ttu-id="53c2d-192">**Использование сообщества** Приложения на основе сообщества используют уровни (редкие, редкие или распространенные)</span><span class="sxs-lookup"><span data-stu-id="53c2d-192">**Community use** Apps based on community use levels (Rare, Uncommon, or Common)</span></span>
    - <span data-ttu-id="53c2d-193">**Уровень разрешений** Приложения, основанные на определенных уровнях разрешений</span><span class="sxs-lookup"><span data-stu-id="53c2d-193">**Permission level** Apps based on certain permission levels</span></span> 
    - <span data-ttu-id="53c2d-194">**Разрешения** Приложения, для которых требуются определенные разрешения</span><span class="sxs-lookup"><span data-stu-id="53c2d-194">**Permissions** Apps that require certain permissions</span></span>
    - <span data-ttu-id="53c2d-195">**Приложение Publisher**  Приложения от определенных издателей</span><span class="sxs-lookup"><span data-stu-id="53c2d-195">**Publisher**  Apps from certain publishers</span></span>
    - <span data-ttu-id="53c2d-196">**User (пользователь** ) Приложения, авторизованные определенным пользователем</span><span class="sxs-lookup"><span data-stu-id="53c2d-196">**User** Apps that a certain user authorized</span></span>
   
2. <span data-ttu-id="53c2d-197">Выберите **равно** или **не равно**, а затем укажите значение для фильтра.</span><span class="sxs-lookup"><span data-stu-id="53c2d-197">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
3. <span data-ttu-id="53c2d-198">Чтобы добавить дополнительные фильтры, выберите знак "плюс" (</span><span class="sxs-lookup"><span data-stu-id="53c2d-198">To add more filters, select the plus sign (</span></span>![Добавление значка фильтра для запроса приложений](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="53c2d-200">), а затем повторите шаги 2 и 3.</span><span class="sxs-lookup"><span data-stu-id="53c2d-200">), and then repeat steps 2 and 3.</span></span>
    
4. <span data-ttu-id="53c2d-201">Чтобы удалить фильтр, выберите x (</span><span class="sxs-lookup"><span data-stu-id="53c2d-201">To remove a filter, select the x (</span></span>![Удаление значка фильтра для запроса приложений](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="53c2d-203">) рядом с именем фильтра.</span><span class="sxs-lookup"><span data-stu-id="53c2d-203">) next to a filter name.</span></span>
    
<span data-ttu-id="53c2d-204">Фильтры применяются автоматически, а список приложений соответствующим образом обновляется.</span><span class="sxs-lookup"><span data-stu-id="53c2d-204">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="53c2d-205">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="53c2d-205">Next steps</span></span>

- [<span data-ttu-id="53c2d-206">Просмотр оповещений и выполнение действий с ними</span><span class="sxs-lookup"><span data-stu-id="53c2d-206">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="53c2d-207">Просмотр [журналов и источников данных веб-трафика для Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="53c2d-207">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="53c2d-208">Обзор [действий по использованию для Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="53c2d-208">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

