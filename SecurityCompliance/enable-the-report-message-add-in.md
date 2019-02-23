---
title: Включение надстройки Report Message
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Сведения о том, как включить надстройку сообщения отчета для Outlook и Outlook в Интернете для отдельных пользователей или всей Организации.
ms.openlocfilehash: 48bd8937622588bbf5a1e07b9d4341e937c5cf7f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217389"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="d29fb-103">Включение надстройки Report Message</span><span class="sxs-lookup"><span data-stu-id="d29fb-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="d29fb-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="d29fb-104">Overview</span></span>

<span data-ttu-id="d29fb-p101">Надстройка сообщения отчета для Outlook и Outlook в Интернете позволяет людям легко сообщать о неклассифицированных сообщениях, будь то безопасное или вредоносное, в Майкрософт и ее дочерних подразделениех для анализа. Корпорация Майкрософт использует эти отправки для повышения эффективности технологий защиты электронной почты. Кроме того, если в организации используется [office 365 Advanced Threat protection](office-365-atp.md) или [Office 365 Threat Intelligence](office-365-ti.md), надстройка сообщений отчета предоставляет группе безопасности Организации полезную информацию, которую можно использовать для просмотра и обновления политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="d29fb-p101">The Report Message add-in for Outlook and Outlook on the web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="d29fb-p102">Например, предположим, что люди сообщают о большом числе фишинговых сообщений. Эта информация послужит в качестве поверхности в [панели мониторинга безопасности](security-dashboard.md) и других отчетов. Группа безопасности вашей организации может использовать эти сведения для указания того, что политики защиты от фишинга может потребоваться обновить. Или, если пользователи сообщают о большом количестве сообщений, помеченных как нежелательные, с помощью надстройки Report Message, группе безопасности Организации может потребоваться настроить [политики защиты от нежелательной почты](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d29fb-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="d29fb-112">Надстройка сообщения отчета работает с вашей подпиской на Office 365 и следующими продуктами:</span><span class="sxs-lookup"><span data-stu-id="d29fb-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="d29fb-113">Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="d29fb-113">Outlook on the web</span></span>
 - <span data-ttu-id="d29fb-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="d29fb-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="d29fb-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d29fb-115">Outlook 2016</span></span>
 - <span data-ttu-id="d29fb-116">Outlook 2016 для Mac</span><span class="sxs-lookup"><span data-stu-id="d29fb-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="d29fb-117">Outlook, включенный в Office 365 профессиональный плюс</span><span class="sxs-lookup"><span data-stu-id="d29fb-117">Outlook included with Office 365 ProPlus</span></span>

> [!NOTE]
> <span data-ttu-id="d29fb-p103">Надстройка сообщения отчета для Outlook и Outlook в Интернете — это не то же самое, что и [Фильтр нежелательной почты Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), хотя они могут быть использованы для пометки почты как нежелательных, нежелательных или фишинговых атак. Надстройка сообщения отчета для Outlook и Outlook в Интернете уведомляет Майкрософт о неклассифицированных сообщениях электронной почты, а фильтр неЖелательной почты Outlook используется для упорядочения сообщений электронной почты в почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="d29fb-p103">The Report Message add-in for Outlook and Outlook on the web is not exactly the same thing as the [Outlook Junk Email Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), although both can be used to mark email as junk, not junk, or a phishing attempt. The Report Message add-in for Outlook and Outlook on the web notifies Microsoft about misclassified email, whereas the Outlook Junk Email Filter is used to organize email messages in a user's mailbox.</span></span> 
  
<span data-ttu-id="d29fb-120">Если вы являетесь отдельным пользователем, вы можете [включить для себя надстройку сообщения отчета](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="d29fb-120">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="d29fb-p104">Если вы являетесь глобальным администратором Office 365 или администратором Exchange Online, а Exchange настроен на использование проверки подлинности OAuth, вы можете [включить надстройку сообщения отчета для Организации](#get-and-enable-the-report-message-add-in-for-your-organization). Теперь надстройка сообщений отчета доступна с помощью централизованного [развертывания](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="d29fb-p104">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="d29fb-123">Получение надстройки "сообщение отчета" для себя</span><span class="sxs-lookup"><span data-stu-id="d29fb-123">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="d29fb-124">В [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps)найдите [надстройку сообщения отчета](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="d29fb-124">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="d29fb-125">Нажмите кнопку **получить**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-125">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="d29fb-126">![Сообщение отчета: получить его сейчас](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-126">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="d29fb-p105">Ознакомьтесь с условиями использования и политики конфиденциальности. Затем нажмите кнопку **продолжить**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-p105">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="d29fb-129">Войдите в Office 365 с помощью рабочей или учебной учетной записи (для бизнес-использования) или учетной записи Майкрософт (для личного использования).</span><span class="sxs-lookup"><span data-stu-id="d29fb-129">Sign in to Office 365 using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="d29fb-130">После установки и включения надстройки вы увидите следующие значки:</span><span class="sxs-lookup"><span data-stu-id="d29fb-130">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="d29fb-131">В Outlook значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d29fb-131">In Outlook, the icon looks like this:</span></span> <br/> ![Значок надстройки сообщения отчета для Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="d29fb-133">В Outlook в Интернете (предыдущее название — Outlook Web App) значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d29fb-133">In Outlook on the web (formerly known as Outlook Web App), the icon looks like this:</span></span><br/>![Значок надстройки сообщения в веб-отчете Outlook](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="d29fb-135">На следующем этапе Узнайте, как [использовать надстройку Message Report](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="d29fb-135">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="d29fb-136">Получение и включение надстройки сообщений отчета для Организации</span><span class="sxs-lookup"><span data-stu-id="d29fb-136">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d29fb-p106">Для выполнения этой задачи необходимо быть глобальным администратором Office 365 или администратором Exchange Online. Кроме того, для получения дополнительных сведений в Exchange необходимо настроить проверку подлинности OAuth, используя [требования Exchange (централизованНое Развертывание надстроек)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="d29fb-p106">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="d29fb-139">Перейдите на [страницу "службы" _амп_](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) "надстройки" в центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d29fb-139">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="d29fb-140">![Страница "службы и надстройки" в новом центре администрирования Microsoft 365](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-140">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="d29fb-141">Выберите **+ развернуть надстройку**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-141">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="d29fb-142">![Выбор варианта развертывания надстройки](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-142">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="d29fb-143">На экране **Новая надстройка** просмотрите сведения, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-143">In the **New Add-In** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="d29fb-144">![Новые сведения о надстройке](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-144">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="d29fb-145">Выберите **я хочу добавить надстройку из магазина Office**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-145">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="d29fb-146">![Я хочу добавить новую надстройку](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-146">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="d29fb-147">Найдите **сообщение отчета**и в списке результатов рядом с пунктом **надстройка сообщения отчета**нажмите кнопку **добавить**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-147">Search for **Report Message**, and in the list of results, next to the **Report Message Add-In**, choose **Add**.</span></span><br/><span data-ttu-id="d29fb-148">![Найдите сообщение для отчета и нажмите кнопку Добавить](media/NewAddInScreen3.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-148">![Search for Report Message and then choose Add](media/NewAddInScreen3.png)</span></span><br/>
    
6. <span data-ttu-id="d29fb-149">На экране **сообщения отчета** просмотрите сведения, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-149">On the **Report Message** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="d29fb-150">![Сведения о сообщении отчета](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-150">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="d29fb-151">Укажите параметры пользователя по умолчанию для Outlook, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-151">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="d29fb-152">![Отчет о параметрах сообщений по умолчанию для Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-152">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="d29fb-153">Укажите, кто получает надстройку сообщения отчета, а затем нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-153">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="d29fb-154">![Кто получает надстройку сообщения отчета](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-154">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="d29fb-155">Мы рекомендуем [настроить правило для получения копии сообщений электронной почты, о которых сообщили ваши пользователи](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span><span class="sxs-lookup"><span data-stu-id="d29fb-155">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span></span>

<span data-ttu-id="d29fb-p107">В зависимости от того, что было выбрано при настройке надстройки (шаги 7-8 выше), пользователи в вашей организации будут иметь доступ к [надстройке сообщений отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) . Пользователи в вашей организации увидят следующие значки:</span><span class="sxs-lookup"><span data-stu-id="d29fb-p107">Depending on what you selected when you set up the add-in (steps 7-8 above), people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="d29fb-158">В Outlook значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d29fb-158">In Outlook, the icon looks like this:</span></span> <br/> ![Значок надстройки сообщения отчета для Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="d29fb-160">В Outlook в Интернете значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d29fb-160">In Outlook on the web, the icon looks like this:</span></span><br/>![Значок надстройки сообщения в веб-отчете Outlook](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="d29fb-162">При уведомлении пользователей о надстройке сообщения отчета добавьте ссылку для [использования надстройки Report Message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="d29fb-162">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="d29fb-163">Настройка правила для получения копии сообщений электронной почты, о которых сообщил пользователь</span><span class="sxs-lookup"><span data-stu-id="d29fb-163">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d29fb-164">Для выполнения этой задачи необходимо быть администратором Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d29fb-164">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="d29fb-p108">Вы можете настроить правило для получения копии сообщений электронной почты, о которых сообщили пользователи в вашей организации. Это можно сделать после того, как вы загрузили и включили надстройку Message Report для своей организации.</span><span class="sxs-lookup"><span data-stu-id="d29fb-p108">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="d29fb-167">В центре администрирования Exchange выберите **правила**для обработки **почтового процесса** \> .</span><span class="sxs-lookup"><span data-stu-id="d29fb-167">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="d29fb-168">Выберите **+** \> **создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-168">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="d29fb-169">В поле **имя** введите имя, например отправку.</span><span class="sxs-lookup"><span data-stu-id="d29fb-169">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="d29fb-170">В списке **Применить это правило, если** выберите **адрес получателя включает...**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-170">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="d29fb-171">В окне **Укажите слова или фразы** добавьте `junk@office365.microsoft.com` и `phish@office365.microsoft.com`нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-171">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="d29fb-172">![Указание нежелательных и ложных адресов электронной почты для правила](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-172">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="d29fb-173">В списке **выполнить следующие действия** выберите команду **СК для сообщения...**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-173">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="d29fb-174">Добавьте глобального администратора, администратора безопасности и/или читателя безопасности, которые должны получить копию каждого сообщения электронной почты, отправляемого пользователям в корпорацию Майкрософт, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-174">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="d29fb-175">![Добавление глобального администратора или администратора безопасности для получения копии каждого полученного сообщения](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-175">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="d29fb-176">Выберите пункт **аудит этого правила со степенью серьезности**, а затем выберите **средний**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-176">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="d29fb-177">В разделе **выберите режим для этого правила**нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-177">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="d29fb-178">![Настройка правила для получения копии каждого сообщения из отчета](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-178">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="d29fb-179">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d29fb-179">Choose **Save**.</span></span> 
    
<span data-ttu-id="d29fb-p109">С помощью этого правила, когда кто-то в Организации отправляет сообщение электронной почты с помощью надстройки Report Message, глобальный администратор, администратор безопасности и/или средство чтения безопасности получат копию этого сообщения. Эти сведения позволяют настраивать политики, такие как политики [безопасных ссылок Office 365 ATP](atp-safe-links.md) или параметры [защиты от нежелательной почты](anti-spam-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="d29fb-p109">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies, or your [anti-spam](anti-spam-protection.md) settings.</span></span> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="d29fb-182">Узнайте, как использовать надстройку "сообщение отчета"</span><span class="sxs-lookup"><span data-stu-id="d29fb-182">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="d29fb-183">Обратитесь [к разделу Использование надстройки Report Message](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="d29fb-183">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="d29fb-184">Просмотр или изменение параметров для надстройки "сообщение отчета"</span><span class="sxs-lookup"><span data-stu-id="d29fb-184">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="d29fb-185">Вы можете просмотреть и изменить параметры по умолчанию для надстройки "сообщения отчета" на [странице "службы" _амп_](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns)"надстройки".</span><span class="sxs-lookup"><span data-stu-id="d29fb-185">You can review and edit the default settings for the Report Message add-in on the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="d29fb-186">Для выполнения этой задачи необходимо быть глобальным администратором Office 365 или администратором Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d29fb-186">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="d29fb-187">Перейдите на [страницу "службы" _амп_](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) "надстройки" в центре администрирования Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d29fb-187">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="d29fb-188">![Страница "службы и надстройки" в новом центре администрирования Microsoft 365](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="d29fb-188">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="d29fb-189">Найдите и выберите надстройку сообщения отчета.</span><span class="sxs-lookup"><span data-stu-id="d29fb-189">Find and select the Report Message add-in.</span></span><br/>![Поиск и выбор надстройки "сообщение отчета"](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="d29fb-191">На экране сообщения отчета просмотрите и измените параметры в соответствии с требованиями Организации.</span><span class="sxs-lookup"><span data-stu-id="d29fb-191">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Параметры для надстройки сообщений отчета](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a><span data-ttu-id="d29fb-193">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="d29fb-193">Related topics</span></span>

[<span data-ttu-id="d29fb-194">Использование надстройки Report Message</span><span class="sxs-lookup"><span data-stu-id="d29fb-194">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="d29fb-195">Просмотр отчетов о безопасности электронной почты в &amp; центре безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d29fb-195">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="d29fb-196">Просмотр отчетов для Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="d29fb-196">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="d29fb-197">Использование проводника в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="d29fb-197">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

