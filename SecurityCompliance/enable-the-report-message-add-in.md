---
title: Включение надстройки Report Message
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Узнайте, как включить сообщения отчета надстройки для Outlook и Outlook на веб-сайте, для отдельных пользователей или всей организации.
ms.openlocfilehash: 8c061d14d11aa868567487186c5dcca534b86215
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995160"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="1fe1d-103">Включение надстройки Report Message</span><span class="sxs-lookup"><span data-stu-id="1fe1d-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="1fe1d-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="1fe1d-104">Overview</span></span>

<span data-ttu-id="1fe1d-p101">Отчет о надстройки для Outlook и Outlook в Интернете позволяют пользователям легко сообщать о неправильно классифицированных электронной почты как безопасный, так и сообщение о нежелательном, корпорацией Майкрософт и ее дочерних компаний для анализа. Корпорация Майкрософт использует эти отправки для повышения эффективности технологии защиты электронной почты. Кроме того Если ваша организация использует [Защиту от угроз для Office 365 расширенного](office-365-atp.md) или [Анализ угроз Office 365](office-365-ti.md), надстройка сообщения отчета содержит группы безопасности вашей организации полезную информацию, которые они могут использовать для просмотра и обновления политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p101">The Report Message add-in for Outlook and Outlook on the web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="1fe1d-p102">Например, предположим, что пользователи являются отчетность с большим количеством сообщений как фишинга. В этом поверхности сведения в панели [Мониторинга безопасности](security-dashboard.md) и другие отчеты. Группа безопасности вашей организации эти сведения можно использовать как это свидетельствует о том, что фишинга политики могут быть обновлены. Или, если пользователи являются отчетность с большим количеством сообщений, которые были помечены как нежелательная почта, как не являющееся нежелательным с помощью надстройки сообщения отчета, группа безопасности вашей организации может потребоваться настройка [политик защиты от нежелательной почты](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="1fe1d-112">Надстройка сообщения отчета для работы с подписки Office 365 и следующих продуктов:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="1fe1d-113">Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="1fe1d-113">Outlook on the web</span></span>
 - <span data-ttu-id="1fe1d-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="1fe1d-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="1fe1d-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fe1d-115">Outlook 2016</span></span>
 - <span data-ttu-id="1fe1d-116">Outlook 2016 для Mac</span><span class="sxs-lookup"><span data-stu-id="1fe1d-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="1fe1d-117">Outlook, включенные в состав Office 365 профессиональный плюс</span><span class="sxs-lookup"><span data-stu-id="1fe1d-117">Outlook included with Office 365 ProPlus</span></span>

> [!NOTE]
> <span data-ttu-id="1fe1d-p103">Отчет о надстройки для Outlook и Outlook в Интернете именно не то же самое [Фильтр нежелательной почты Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), несмотря на то, что оба можно использовать для обозначения электронной почты как нежелательные, не список нежелательной почты и фишинга. Отчет о надстройки для Outlook и Outlook в Интернете уведомляет Microsoft о неправильно классифицированных электронной почтой, то время как фильтр нежелательной почты Outlook используется для упорядочения сообщений электронной почты в почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p103">The Report Message add-in for Outlook and Outlook on the web is not exactly the same thing as the [Outlook Junk Email Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), although both can be used to mark email as junk, not junk, or a phishing attempt. The Report Message add-in for Outlook and Outlook on the web notifies Microsoft about misclassified email, whereas the Outlook Junk Email Filter is used to organize email messages in a user's mailbox.</span></span> 
  
<span data-ttu-id="1fe1d-120">Если вы отдельного пользователя, можно [включить надстройку отчета сообщения для самостоятельно](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-120">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="1fe1d-p104">Если вы глобального администратора Office 365 или администратор Exchange Online и Exchange настроен для использования проверки подлинности OAuth, можно [включить надстройку сообщения отчета для вашей организации](#get-and-enable-the-report-message-add-in-for-your-organization). Надстройка сообщения отчета теперь доступен через [Централизованного развертывания](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p104">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="1fe1d-123">Сообщение отчета надстройки для себя</span><span class="sxs-lookup"><span data-stu-id="1fe1d-123">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="1fe1d-124">В [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps)поиск [надстройки сообщения отчета](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-124">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="1fe1d-125">Выберите **получить ИТ ТЕПЕРЬ**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-125">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="1fe1d-126">![Сообщение — получить сейчас](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-126">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="1fe1d-p105">Ознакомьтесь с условиями использования и конфиденциальность политики. Выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p105">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="1fe1d-129">Войдите в Office 365 с помощью работу или учетная запись school (для использования в бизнесе) или свою учетную запись Майкрософт (для личного использования).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-129">Sign in to Office 365 using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="1fe1d-130">После надстройка установлена и включена, вы увидите следующие значки:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-130">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="1fe1d-131">В программе Outlook значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-131">In Outlook, the icon looks like this:</span></span> <br/> ![Сообщить о значок сообщения надстройки для Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="1fe1d-133">В Outlook Web App (или Outlook в Интернете) значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-133">In Outlook Web App (or Outlook on the web), the icon looks like this:</span></span><br/>![Outlook для значка web надстройки сообщения отчета](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="1fe1d-135">В качестве следующего шага, узнайте, как [использования надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-135">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="1fe1d-136">Получение и включить надстройку сообщения отчета для вашей организации</span><span class="sxs-lookup"><span data-stu-id="1fe1d-136">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1fe1d-p106">Должен быть глобального администратора Office 365 или администратора Exchange Online для выполнения этой задачи. Кроме того Exchange должен быть настроен для использования проверки подлинности OAuth на дополнительные сведения, в разделе [requirements Exchange (централизованного развертывания надстроек)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p106">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="1fe1d-139">Перейдите на [страницу надстроек служб &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) в центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-139">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="1fe1d-140">![Страница служб и надстройки в центре администрирования нового 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-140">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="1fe1d-141">Нажмите кнопку **+ Развертывание надстройки**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-141">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="1fe1d-142">![Выберите развертывание надстройки](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-142">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="1fe1d-143">В окне **New Add-In** ознакомьтесь со сведениями и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-143">In the **New Add-In** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="1fe1d-144">![Новые сведения о Add-In](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-144">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="1fe1d-145">Выберите **Добавить надстройку в магазине Office**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-145">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="1fe1d-146">![Чтобы добавить новые надстройки](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-146">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="1fe1d-147">**Отчет о**сообщении и в списке результатов, рядом с элементом **Отчета сообщение Add-In**поиска, выберите **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-147">Search for **Report Message**, and in the list of results, next to the **Report Message Add-In**, choose **Add**.</span></span><br/><span data-ttu-id="1fe1d-148">![Поиск сообщения отчета и нажмите кнопку Добавить](media/NewAddInScreen3.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-148">![Search for Report Message and then choose Add](media/NewAddInScreen3.png)</span></span><br/>
    
6. <span data-ttu-id="1fe1d-149">На экране **Сообщения отчета** ознакомьтесь со сведениями и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-149">On the **Report Message** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="1fe1d-150">![Сведения о сообщении отчета](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-150">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="1fe1d-151">Указывать параметры пользователя по умолчанию для Outlook и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-151">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="1fe1d-152">![Сообщить о сообщении параметры по умолчанию для Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-152">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="1fe1d-153">Укажите, кто несет добавить в сообщение и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-153">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="1fe1d-154">![Кто возвращает сообщение для отчета надстройки](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-154">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="1fe1d-155">Мы рекомендуем [Настройка правила для получения копии сообщения электронной почты, о которых сообщает пользователям](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-155">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span></span>

<span data-ttu-id="1fe1d-p107">В зависимости от выбранных при настройке надстройки (шаги 7-8) пользователи в вашей организации будет иметь [Добавить в отчет о](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) доступных. Пользователи в вашей организации отображаются следующие значки:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p107">Depending on what you selected when you set up the add-in (steps 7-8 above), people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="1fe1d-158">В программе Outlook значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-158">In Outlook, the icon looks like this:</span></span> <br/> ![Добавить в сообщение значок отчета для Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="1fe1d-160">В Outlook Web App (или Outlook в Интернете) значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1fe1d-160">In Outlook Web App (or Outlook on the web), the icon looks like this:</span></span><br/>![Outlook для значка Добавить в сообщение отчета Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="1fe1d-162">Когда сообщить пользователям о надстройки сообщения отчета, добавлена ссылка на статью для [использования надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-162">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="1fe1d-163">Настройка правила для получения копии сообщения электронной почты, о которых сообщает пользователям</span><span class="sxs-lookup"><span data-stu-id="1fe1d-163">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1fe1d-164">Необходимо быть администратором Exchange Online для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-164">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="1fe1d-p108">Можно настроить правила для получения копии сообщения электронной почты, обнаруженных пользователями в вашей организации. Для этого после загрузки и поддержкой надстройки сообщения отчета для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p108">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="1fe1d-167">В центре администрирования Exchange выберите **поток почты** \> **правила**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-167">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="1fe1d-168">Выберите **+** \> **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-168">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="1fe1d-169">В поле **имя** введите имя, например, отправке.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-169">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="1fe1d-170">Выберите в списке **Применить это правило, если** **адрес получателя содержит...**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-170">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="1fe1d-171">В окне **Укажите слова или фразы** добавьте `junk@office365.microsoft.com` и `phish@office365.microsoft.com`, а затем нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-171">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="1fe1d-172">![Укажите Нежелательная почта и ловят адреса электронной почты для правила](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-172">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="1fe1d-173">Выберите в списке **выполните следующие...** **скрытой копии сообщения для...**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-173">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="1fe1d-174">Добавление глобального администратора, администратора безопасности и/или чтения безопасности, следует получения копии всех сообщений электронной почты людей сообщить в корпорацию Майкрософт, а затем нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-174">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="1fe1d-175">![Добавление глобальных или безопасности администратора для получения копии каждого переданные сообщения](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-175">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="1fe1d-176">Выберите **аудита этого правила с степень серьезности**и задайте **среднего**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-176">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="1fe1d-177">В разделе **Выбор режима для этого правила**нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-177">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="1fe1d-178">![Настройка правила для получения копии каждого переданные сообщения](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-178">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="1fe1d-179">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-179">Choose **Save**.</span></span> 
    
<span data-ttu-id="1fe1d-p109">С этим правилом на месте каждый раз, когда кто-то в вашей организации сообщает сообщения электронной почты с помощью сообщения отчета надстройки, глобального администратора, администратора безопасности и чтения безопасности будет получать копию этого сообщения. Эти сведения могут включать для установки и настройки политики, такие как [Безопасные связи с Office 365 ATP](atp-safe-links.md) политик или параметров [защиты от нежелательной почты](anti-spam-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="1fe1d-p109">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies, or your [anti-spam](anti-spam-protection.md) settings.</span></span> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="1fe1d-182">Сведения об использовании надстройки сообщения отчета</span><span class="sxs-lookup"><span data-stu-id="1fe1d-182">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="1fe1d-183">Показано [Использование надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-183">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="1fe1d-184">Просмотреть или изменить параметры для надстройки сообщения отчета</span><span class="sxs-lookup"><span data-stu-id="1fe1d-184">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="1fe1d-185">Можно просмотреть и изменить параметры по умолчанию для надстройки сообщения отчета на [странице Add-Ins & служб](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="1fe1d-185">You can review and edit the default settings for the Report Message add-in on the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="1fe1d-186">Должен быть глобального администратора Office 365 или администратора Exchange Online для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-186">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="1fe1d-187">Перейдите на [страницу надстроек служб &](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) в центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-187">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="1fe1d-188">![Страница служб и надстройки в центре администрирования нового 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="1fe1d-188">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="1fe1d-189">Найдите и выберите надстройки сообщения отчета.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-189">Find and select the Report Message add-in.</span></span><br/>![Найдите и выберите надстройки сообщения отчета](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="1fe1d-191">На экране сообщения отчета Просмотр и изменение параметров в зависимости от вашей организации.</span><span class="sxs-lookup"><span data-stu-id="1fe1d-191">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Параметры для надстройки сообщения отчета](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a><span data-ttu-id="1fe1d-193">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="1fe1d-193">Related topics</span></span>

[<span data-ttu-id="1fe1d-194">Использование надстройки Report Message</span><span class="sxs-lookup"><span data-stu-id="1fe1d-194">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="1fe1d-195">Просмотр отчетов по безопасности электронной почты в безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="1fe1d-195">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="1fe1d-196">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="1fe1d-196">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="1fe1d-197">Используйте проводник в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="1fe1d-197">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

