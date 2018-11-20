---
title: Включение надстройки Report Message
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Узнайте, как включить сообщения отчета надстройки для Outlook и Outlook на веб-сайте, для отдельных пользователей или всей организации.
ms.openlocfilehash: a62e3e6250d2eccd2109a71f994713e2dd1b262e
ms.sourcegitcommit: 6669b7aae26965145e85d9613d3091bf389f000b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/19/2018
ms.locfileid: "26618925"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="08208-103">Включение надстройки Report Message</span><span class="sxs-lookup"><span data-stu-id="08208-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="08208-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="08208-104">Overview</span></span>

<span data-ttu-id="08208-p101">Отчет о надстройки для Outlook и Outlook в Интернете позволяют пользователям легко сообщать о неправильно классифицированных электронной почты как безопасный, так и сообщение о нежелательном, корпорацией Майкрософт и ее дочерних компаний для анализа. Корпорация Майкрософт использует эти отправки для повышения эффективности технологии защиты электронной почты. Кроме того Если ваша организация использует [Защиту от угроз для Office 365 расширенного](office-365-atp.md) или [Анализ угроз Office 365](office-365-ti.md), надстройка сообщения отчета содержит группы безопасности вашей организации полезную информацию, которые они могут использовать для просмотра и обновления политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="08208-p101">The Report Message add-in for Outlook and Outlook on the Web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="08208-p102">Например, предположим, что пользователи являются отчетность с большим количеством сообщений как фишинга. В этом поверхности сведения в панели [Мониторинга безопасности](security-dashboard.md) и другие отчеты. Группа безопасности вашей организации эти сведения можно использовать как это свидетельствует о том, что фишинга политики могут быть обновлены. Или, если пользователи являются отчетность с большим количеством сообщений, которые были помечены как нежелательная почта, как не являющееся нежелательным с помощью надстройки сообщения отчета, группа безопасности вашей организации может потребоваться настройка [политик защиты от нежелательной почты](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="08208-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="08208-112">Надстройка сообщения отчета для работы с подписки Office 365 и следующих продуктов:</span><span class="sxs-lookup"><span data-stu-id="08208-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="08208-113">Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="08208-113">Outlook on the Web</span></span>
 - <span data-ttu-id="08208-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="08208-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="08208-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08208-115">Outlook 2016</span></span>
 - <span data-ttu-id="08208-116">Outlook 2016 для Mac</span><span class="sxs-lookup"><span data-stu-id="08208-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="08208-117">Outlook, включенные в состав Office 365 профессиональный плюс</span><span class="sxs-lookup"><span data-stu-id="08208-117">Outlook included with Office 365 ProPlus</span></span>
  
<span data-ttu-id="08208-118">Если вы отдельного пользователя, можно [включить надстройку отчета сообщения для самостоятельно](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="08208-118">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="08208-p103">Если вы глобального администратора Office 365 или администратор Exchange Online и Exchange настроен для использования проверки подлинности OAuth, можно [включить надстройку сообщения отчета для вашей организации](#get-and-enable-the-report-message-add-in-for-your-organization). Надстройка сообщения отчета теперь доступен через [Централизованного развертывания](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span><span class="sxs-lookup"><span data-stu-id="08208-p103">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="08208-121">Сообщение отчета надстройки для себя</span><span class="sxs-lookup"><span data-stu-id="08208-121">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="08208-122">В [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps)поиск [надстройки сообщения отчета](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="08208-122">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="08208-123">Выберите **получить ИТ ТЕПЕРЬ**.</span><span class="sxs-lookup"><span data-stu-id="08208-123">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="08208-124">![Сообщение — получить сейчас](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="08208-124">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="08208-p104">Ознакомьтесь с условиями использования и конфиденциальность политики. Выберите **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="08208-p104">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="08208-127">Войдите в Office 365 электронной почты с помощью работу или учетная запись school (для использования в бизнесе) или свою учетную запись Майкрософт (для личного использования).</span><span class="sxs-lookup"><span data-stu-id="08208-127">Sign in to your Office 365 email using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="08208-128">После надстройка установлена и включена, вы увидите следующие значки:</span><span class="sxs-lookup"><span data-stu-id="08208-128">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="08208-129">В программе Outlook значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="08208-129">In Outlook the icon looks like this:</span></span> <br/> ![Добавить в сообщение значок отчета для Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="08208-131">В Outlook Web App значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="08208-131">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook для значка Добавить в сообщение отчета Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

<span data-ttu-id="08208-133">В качестве следующего шага, узнайте, как [использования надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="08208-133">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="08208-134">Получение и включить надстройку сообщения отчета для вашей организации</span><span class="sxs-lookup"><span data-stu-id="08208-134">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08208-p105">Должен быть глобального администратора Office 365 или администратора Exchange Online для выполнения этой задачи. Кроме того Exchange должен быть настроен для использования проверки подлинности OAuth на дополнительные сведения, в разделе [requirements Exchange (централизованного развертывания надстроек)](https://docs.microsoft.com/en-us/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="08208-p105">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/en-us/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="08208-137">Перейдите на [службы & страницы надстроек](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) в центре администрирования нового Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="08208-137">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="08208-138">![Страница служб и надстройки в центре администрирования нового 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="08208-138">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="08208-139">Нажмите кнопку **+ Развертывание надстройки**.</span><span class="sxs-lookup"><span data-stu-id="08208-139">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="08208-140">![Выберите развертывание надстройки](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="08208-140">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="08208-141">В окне New Add-In ознакомьтесь со сведениями и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="08208-141">In the New Add-In screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="08208-142">![Новые сведения о Add-In](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="08208-142">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="08208-143">Выберите **Добавить надстройку в магазине Office**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="08208-143">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="08208-144">![Чтобы добавить новые надстройки](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="08208-144">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="08208-145">Отчет о сообщении и в списке результатов, рядом с элементом отчета сообщение надстройки поиска, выберите Добавить.</span><span class="sxs-lookup"><span data-stu-id="08208-145">Search for Report Message, and in the list of results, next to the Report Message Add-In, choose Add.</span></span><br/>![Поиск сообщения отчета и нажмите кнопку Добавить](media/NewAddInScreen3.png)<br/>
    
6. <span data-ttu-id="08208-147">На экране сообщения отчета ознакомьтесь со сведениями и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="08208-147">On the Report Message screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="08208-148">![Сведения о сообщении отчета](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="08208-148">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="08208-149">Указывать параметры пользователя по умолчанию для Outlook и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="08208-149">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="08208-150">![Сообщить о сообщении параметры по умолчанию для Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="08208-150">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="08208-151">Укажите, кто несет добавить в сообщение и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="08208-151">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="08208-152">![Кто возвращает сообщение для отчета надстройки](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="08208-152">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="08208-153">Мы рекомендуем [Настройка правила для получения копии сообщения электронной почты, о которых сообщает пользователям](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span><span class="sxs-lookup"><span data-stu-id="08208-153">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span></span>

<span data-ttu-id="08208-p106">В зависимости от того, какой выбран с помощью мастера пользователи в вашей организации будет иметь [надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) недоступны. Пользователи в вашей организации отображаются следующие значки:</span><span class="sxs-lookup"><span data-stu-id="08208-p106">Depending on what you selected using the wizard, people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="08208-156">В программе Outlook значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="08208-156">In Outlook the icon looks like this:</span></span> <br/> ![Добавить в сообщение значок отчета для Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="08208-158">В Outlook Web App значок выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="08208-158">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook для значка Добавить в сообщение отчета Web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="08208-160">Настройка правила для получения копии сообщения электронной почты, о которых сообщает пользователям</span><span class="sxs-lookup"><span data-stu-id="08208-160">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08208-161">Необходимо быть администратором Exchange Online для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="08208-161">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="08208-p107">Можно настроить правила для получения копии сообщения электронной почты, обнаруженных пользователями в вашей организации. Для этого после загрузки и поддержкой надстройки сообщения отчета для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="08208-p107">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="08208-164">В центре администрирования Exchange выберите **поток почты** \> **правила**.</span><span class="sxs-lookup"><span data-stu-id="08208-164">In the EAC, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="08208-165">Выберите **+** \> **Создать новое правило**.</span><span class="sxs-lookup"><span data-stu-id="08208-165">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="08208-166">В поле **имя** введите имя, например, отправке.</span><span class="sxs-lookup"><span data-stu-id="08208-166">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="08208-167">Выберите в списке **Применить это правило, если** **адрес получателя содержит...**.</span><span class="sxs-lookup"><span data-stu-id="08208-167">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="08208-168">В окне **Укажите слова или фразы** добавьте `junk@office365.microsoft.com` и `phish@office365.microsoft.com`, а затем нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="08208-168">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="08208-169">![Укажите Нежелательная почта и ловят адреса электронной почты для правила](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="08208-169">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="08208-170">Выберите в списке **выполните следующие...** **скрытой копии сообщения для...**.</span><span class="sxs-lookup"><span data-stu-id="08208-170">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="08208-171">Добавление глобального администратора, администратора безопасности и/или чтения безопасности, следует получения копии всех сообщений электронной почты людей сообщить в корпорацию Майкрософт, а затем нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="08208-171">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="08208-172">![Добавление глобальных или безопасности администратора для получения копии каждого переданные сообщения](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="08208-172">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="08208-173">Выберите **аудита этого правила с степень серьезности**и задайте **среднего**.</span><span class="sxs-lookup"><span data-stu-id="08208-173">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="08208-174">В разделе **Выбор режима для этого правила**нажмите кнопку **Применить**.</span><span class="sxs-lookup"><span data-stu-id="08208-174">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="08208-175">![Настройка правила для получения копии каждого переданные сообщения](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="08208-175">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="08208-176">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="08208-176">Choose **Save**.</span></span> 
    
<span data-ttu-id="08208-p108">С этим правилом на месте каждый раз, когда кто-то в вашей организации сообщает сообщения электронной почты с помощью сообщения отчета надстройки, глобального администратора, администратора безопасности и чтения безопасности будет получать копию этого сообщения. Эти сведения можно включить для установки и настройки политики, например политики [Office 365 ATP безопасных ссылки](atp-safe-links.md) .</span><span class="sxs-lookup"><span data-stu-id="08208-p108">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies.</span></span> 

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="08208-179">Просмотреть или изменить параметры для надстройки сообщения отчета</span><span class="sxs-lookup"><span data-stu-id="08208-179">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="08208-180">Можно просмотреть и изменить параметры по умолчанию для отчета сообщение надстройки [служб & надстройки страницы](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="08208-180">You can review and edit the default settings for the Report Message Add-In in the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="08208-181">Должен быть глобального администратора Office 365 или администратора Exchange Online для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="08208-181">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="08208-182">Перейдите на [службы & страницы надстроек](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) в центре администрирования нового Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="08208-182">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="08208-183">![Страница служб и надстройки в центре администрирования нового 365 Microsoft](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="08208-183">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="08208-184">Найдите и выберите надстройку сообщения отчета.</span><span class="sxs-lookup"><span data-stu-id="08208-184">Find and select the Report Message Add-In.</span></span><br/>![Найдите и выберите надстройки сообщения отчета](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="08208-186">На экране сообщения отчета Просмотр и изменение параметров в зависимости от вашей организации.</span><span class="sxs-lookup"><span data-stu-id="08208-186">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Параметры для надстройки сообщения отчета](media/EditReportMessageAddIn.png)<br/> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="08208-188">Сведения об использовании надстройки сообщения отчета</span><span class="sxs-lookup"><span data-stu-id="08208-188">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="08208-189">Показано [Использование надстройки сообщения отчета](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="08208-189">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="08208-190">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="08208-190">Related topics</span></span>

[<span data-ttu-id="08208-191">Использование надстройки Report Message</span><span class="sxs-lookup"><span data-stu-id="08208-191">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="08208-192">Просмотр отчетов по безопасности электронной почты в безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="08208-192">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="08208-193">Просмотр отчетов для защиты расширенного Threat Office 365</span><span class="sxs-lookup"><span data-stu-id="08208-193">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="08208-194">Используйте проводник в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="08208-194">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

