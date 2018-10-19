---
title: Включение надстройки Report Message
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/18/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Узнайте, как включить сообщения отчета надстройки для Outlook и Outlook на веб-сайте, для отдельных пользователей или всей организации.
ms.openlocfilehash: ad07d594a78b8134984b48f08898ad1ba697e03a
ms.sourcegitcommit: 49b565f6a57febe53f331b2605d6a06d11e2d0be
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2018
ms.locfileid: "25638013"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="8e2ae-103">Включение надстройки Report Message</span><span class="sxs-lookup"><span data-stu-id="8e2ae-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="8e2ae-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="8e2ae-104">Overview</span></span>

<span data-ttu-id="8e2ae-p101">Отчет о надстройки для Outlook и Outlook в Интернете позволяют пользователям легко сообщать о неправильно классифицированных электронной почты как безопасный, так и сообщение о нежелательном, корпорацией Майкрософт и ее дочерних компаний для анализа. Корпорация Майкрософт использует эти отправки для повышения эффективности технологии защиты электронной почты. Кроме того Если ваша организация использует [Защиту от угроз для Office 365 расширенного](office-365-atp.md) или [Анализ угроз Office 365](office-365-ti.md), надстройка сообщения отчета содержит группы безопасности вашей организации полезную информацию, которые они могут использовать для просмотра и обновления политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p101">The Report Message add-in for Outlook and Outlook on the Web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="8e2ae-p102">Например, предположим, что пользователи являются отчетность с большим количеством сообщений как фишинга. В этом поверхности сведения в панели [Мониторинга безопасности](security-dashboard.md) и другие отчеты. Группа безопасности вашей организации эти сведения можно использовать как это свидетельствует о том, что фишинга политики могут быть обновлены. Или, если пользователи являются отчетность с большим количеством сообщений, которые были помечены как нежелательная почта, как не являющееся нежелательным с помощью надстройки сообщения отчета, группа безопасности вашей организации может потребоваться настройка [политик защиты от нежелательной почты](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="8e2ae-112">Надстройка сообщения отчета для работы с подписки Office 365 и следующих продуктов:</span><span class="sxs-lookup"><span data-stu-id="8e2ae-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="8e2ae-113">Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="8e2ae-113">Outlook on the Web</span></span>
 - <span data-ttu-id="8e2ae-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="8e2ae-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="8e2ae-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e2ae-115">Outlook 2016</span></span>
 - <span data-ttu-id="8e2ae-116">Outlook 2016 для Mac</span><span class="sxs-lookup"><span data-stu-id="8e2ae-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="8e2ae-117">Outlook, включенные в состав Office 365 профессиональный плюс</span><span class="sxs-lookup"><span data-stu-id="8e2ae-117">Outlook included with Office 365 ProPlus</span></span>
  
<span data-ttu-id="8e2ae-118">Если вы отдельного пользователя, можно [включить надстройку отчета сообщения для самостоятельно](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="8e2ae-118">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="8e2ae-119">Если вы администратор Exchange Online можно [включить надстройку сообщения отчета для вашей организации](#get-and-enable-the-report-message-add-in-for-your-organization).</span><span class="sxs-lookup"><span data-stu-id="8e2ae-119">If you're an Exchange Online administrator, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="8e2ae-120">Сообщение отчета надстройки для себя</span><span class="sxs-lookup"><span data-stu-id="8e2ae-120">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="8e2ae-121">В поле, [хранения Office](https://appsource.microsoft.com/product/office/WA104381180?src=office)сообщение отчета надстройки.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-121">In the [Office store](https://appsource.microsoft.com/product/office/WA104381180?src=office), get the Report Message add-in.</span></span>
    
2. <span data-ttu-id="8e2ae-122">Выберите **получить ИТ ТЕПЕРЬ**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-122">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="8e2ae-123">![Сообщение — получить сейчас](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-123">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="8e2ae-p103">Ознакомьтесь с условиями использования и конфиденциальность политики. Выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p103">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="8e2ae-126">Войдите в Office 365 электронной почты с помощью работу или учетная запись school (для использования в бизнесе) или свою учетную запись Майкрософт (для личного использования).</span><span class="sxs-lookup"><span data-stu-id="8e2ae-126">Sign in to your Office 365 email using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    

<span data-ttu-id="8e2ae-127">После надстройка установлена и включена, вы увидите следующие значки:</span><span class="sxs-lookup"><span data-stu-id="8e2ae-127">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="8e2ae-128">В программе Outlook значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8e2ae-128">In Outlook the icon looks like this:</span></span> <br/> ![Добавить в сообщение значок отчета для Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="8e2ae-130">В Outlook Web App значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8e2ae-130">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook для значка Добавить в сообщение отчета Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

<span data-ttu-id="8e2ae-132">В качестве следующего шага, узнайте, как [использования надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="8e2ae-132">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="8e2ae-133">Получение и включить надстройку сообщения отчета для вашей организации</span><span class="sxs-lookup"><span data-stu-id="8e2ae-133">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e2ae-134">Должен быть глобального администратора Office 365 или администратора Exchange Online для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-134">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>

1. <span data-ttu-id="8e2ae-135">Последовательно выберите пункты [https://portal.office.com](https://portal.office.com) и выполнить вход с помощью учетной записи рабочего или школы.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-135">Go to [https://portal.office.com](https://portal.office.com) and sign in using your work or school account.</span></span> 
    
2. <span data-ttu-id="8e2ae-136">Выберите **администратора** , чтобы перейти в центр администрирования.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-136">Choose **Admin** to go to the Admin center.</span></span> 
    
3. <span data-ttu-id="8e2ae-137">Выберите **центры администрирования** \> **Exchange** , чтобы перейти в центр администрирования Exchange (EAC).</span><span class="sxs-lookup"><span data-stu-id="8e2ae-137">Choose **Admin centers** \> **Exchange** to go to the Exchange admin center (EAC).</span></span> 
    
4. <span data-ttu-id="8e2ae-138">Выбор **организации** \> **надстроек**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-138">Choose **organization** \> **add-ins**.</span></span> 
    
5. <span data-ttu-id="8e2ae-139">Выберите **+**  >  **Добавить из магазина Office**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-139">Choose **+** > **Add from the Office Store**.</span></span><br/><span data-ttu-id="8e2ae-140">![Выберите Добавить из магазина Office](media/EAC-Org-AddFromOfficeStore.png)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-140">![Choose Add from the Office Store](media/EAC-Org-AddFromOfficeStore.png)</span></span><br/><span data-ttu-id="8e2ae-141">В веб-браузере откроется в магазин Office.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-141">This opens the Office Store in your web browser.</span></span>
    
6. <span data-ttu-id="8e2ae-142">Поиск сообщения отчета.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-142">Search for Report Message.</span></span><br/>![Поиск сообщений отчета](media/ReportMessageSearchOfficeStore.png)<br/>
    
7. <span data-ttu-id="8e2ae-144">В списке **приложений** выберите **Отчет сообщение**и нажмите кнопку **Получить ИТ ТЕПЕРЬ**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-144">In the **Apps** list, select **Report Message**, and then choose **GET IT NOW**.</span></span><br/><span data-ttu-id="8e2ae-145">![Нажмите кнопку GET ТЕПЕРЬ ИТ](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-145">![Choose GET IT NOW](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
8. <span data-ttu-id="8e2ae-p104">Ознакомьтесь с условиями использования и конфиденциальность политики. Выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p104">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
    ![Нажмите кнопку Продолжить, чтобы принять условия соглашения и политику конфиденциальности](media/ReportMessageTermsAndConditions.png)
  
9. <span data-ttu-id="8e2ae-p105">Откроется мастер для настройки проверки надстройки сообщения отчета сведения и нажмите кнопку **Далее** для продолжения.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p105">A wizard opens to help you configure the Report Message add-in. Review the information, and choose **Next** to continue.</span></span><br/><span data-ttu-id="8e2ae-151">![Мастер добавления сообщения для Office 365 отчетов](media/ReportMessageAdminInstallUI.png)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-151">![Report Message add-in wizard for Office 365](media/ReportMessageAdminInstallUI.png)</span></span><br/> 

10. <span data-ttu-id="8e2ae-152">Укажите, требуется пользователям для надстройки сообщения отчета по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-152">Specify the default setting you want users to have for the Report Message add-in.</span></span><br/>![Укажите параметры по умолчанию для надстройки сообщения отчета](media/ReportMessageUserOptionsAdminsSet.png)<br/>
    
11. <span data-ttu-id="8e2ae-154">Укажите, кто возвращает сообщение для отчета надстройки.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-154">Specify who gets the Report Message add-in.</span></span> <br/>![Укажите, кто возвращает сообщение для отчета надстройки](media/ReportMessageChooseWhoGetsItAdminSettings.png)<br/>

12. <span data-ttu-id="8e2ae-156">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-156">Choose **Save**.</span></span> <br/>
> [!TIP]
> <span data-ttu-id="8e2ae-157">Мы рекомендуем [Настройка правила для получения копии сообщения электронной почты, о которых сообщает пользователям](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-157">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span></span>

<span data-ttu-id="8e2ae-p106">В зависимости от того, какой выбран с помощью мастера пользователи в вашей организации будет иметь [надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) недоступны. Пользователи в вашей организации отображаются следующие значки:</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p106">Depending on what you selected using the wizard, people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="8e2ae-160">В программе Outlook значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8e2ae-160">In Outlook the icon looks like this:</span></span> <br/> ![Добавить в сообщение значок отчета для Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="8e2ae-162">В Outlook Web App значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8e2ae-162">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook для значка Добавить в сообщение отчета Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="8e2ae-164">Настройка правила для получения копии сообщения электронной почты, о которых сообщает пользователям</span><span class="sxs-lookup"><span data-stu-id="8e2ae-164">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e2ae-165">Необходимо быть администратором Exchange Online для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-165">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="8e2ae-p107">Можно настроить правила для получения копии сообщения электронной почты, обнаруженных пользователями в вашей организации. Для этого после загрузки и поддержкой надстройки сообщения отчета для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p107">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="8e2ae-168">В центре администрирования Exchange выберите **поток почты** \> **правила**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-168">In the EAC, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="8e2ae-169">Выберите **+** \> **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-169">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="8e2ae-170">В поле **имя** введите имя, например, отправке.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-170">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="8e2ae-171">Выберите в списке **Применить это правило, если** **адрес получателя содержит...**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-171">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="8e2ae-172">В окне **Укажите слова или фразы** добавьте junk@office365.microsoft.com и phish@office365.microsoft.com и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-172">In the **specify words or phrases** screen, add junk@office365.microsoft.com and phish@office365.microsoft.com, and then choose **OK**.</span></span> 
    
    ![Укажите Нежелательная почта и ловят адреса электронной почты для правила](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)
  
6. <span data-ttu-id="8e2ae-174">Выберите в списке **выполните следующие...** **скрытой копии сообщения для...**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-174">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="8e2ae-175">Добавление глобального администратора, администратора безопасности и/или чтения безопасности, следует получения копии всех сообщений электронной почты людей сообщить в корпорацию Майкрософт, а затем нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-175">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span> 
    
    ![Добавление глобальных или безопасности администратора для получения копии каждого переданные сообщения](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)
  
8. <span data-ttu-id="8e2ae-177">Выберите **аудита этого правила с степень серьезности**и задайте **среднего**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-177">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="8e2ae-178">В разделе **Выбор режима для этого правила**нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-178">Under **Choose a mode for this rule**, choose **Enforce**.</span></span> 
    
    ![Настройка правила для получения копии каждого переданные сообщения](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)
  
10. <span data-ttu-id="8e2ae-180">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-180">Choose **Save**.</span></span> 
    
<span data-ttu-id="8e2ae-p108">С этим правилом на месте каждый раз, когда кто-то в вашей организации сообщает сообщения электронной почты с помощью сообщения отчета надстройки, глобального администратора, администратора безопасности и чтения безопасности будет получать копию этого сообщения. Эти сведения можно включить для установки и настройки политики, например политики [Office 365 ATP безопасных ссылки](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p108">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies.</span></span> 

## <a name="review-or-edit-the-default-settings-for-the-report-message-add-in"></a><span data-ttu-id="8e2ae-183">Просмотреть или изменить параметры по умолчанию для надстройки сообщения отчета</span><span class="sxs-lookup"><span data-stu-id="8e2ae-183">Review or edit the default settings for the Report Message add-in</span></span>

<span data-ttu-id="8e2ae-184">Можно просмотреть и изменить параметры по умолчанию для сообщений отчета надстройки с помощью центра администрирования.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-184">You can review and edit the default settings for the Report Message add-in using the Admin Center.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8e2ae-185">Должен быть глобального администратора Office 365 или администратора Exchange Online для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-185">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="8e2ae-p109">Если вы установили только что надстройка сообщения отчета для вашей организации, вы будете уже на странице служб и надстроек. В противном случае перейдите [здесь](https://portal.office.com/adminportal/home#/Settings/ServicesAndAddIns) и войти с помощью учетной записи рабочего или школы для Office 365.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-p109">If you've just installed the Report Message add-in for your organization, you'll already be on the Services & add-ins page. Otherwise, go [here](https://portal.office.com/adminportal/home#/Settings/ServicesAndAddIns) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="8e2ae-188">Поиск **Сообщений отчет**и выберите его.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-188">Search for **Report Message**, and then select it.</span></span><br/><span data-ttu-id="8e2ae-189">![Службы и надстройки для Office 365](media/ReportMessage-o365servicesaddins.png)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-189">![Services and add-ins for Office 365](media/ReportMessage-o365servicesaddins.png)</span></span><br/> 
    
3. <span data-ttu-id="8e2ae-190">Откроется область, которая отображает параметры, которые были выбраны в качестве надстройки отчета сообщения во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-190">A pane opens that displays the settings that were selected for the Report Message add-in during deployment.</span></span><br/>![Параметры для надстройки сообщения отчета](media/ReportMessage-reviewaddinsettings.png)<br/> 

4. <span data-ttu-id="8e2ae-192">Просмотрите и при необходимости измените параметры для надстройки сообщения отчета, а затем сохраните изменения.</span><span class="sxs-lookup"><span data-stu-id="8e2ae-192">Review and if needed, edit settings for the Report Message add-in, and then save your changes.</span></span>
    
## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="8e2ae-193">Сведения об использовании надстройки сообщения отчета</span><span class="sxs-lookup"><span data-stu-id="8e2ae-193">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="8e2ae-194">Показано [Использование надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="8e2ae-194">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="8e2ae-195">См. также:</span><span class="sxs-lookup"><span data-stu-id="8e2ae-195">Related topics</span></span>

[<span data-ttu-id="8e2ae-196">Использование надстройки Report Message</span><span class="sxs-lookup"><span data-stu-id="8e2ae-196">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="8e2ae-197">Просмотр отчетов по безопасности электронной почты в безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8e2ae-197">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="8e2ae-198">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="8e2ae-198">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="8e2ae-199">Используйте проводник в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="8e2ae-199">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

