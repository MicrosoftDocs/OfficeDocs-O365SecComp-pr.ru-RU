---
title: Защита файлов SharePoint Online с помощью меток Office 365 и DLP
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: c9f837af-8d71-4df1-a285-dedb1c5618b3
description: Сводка. Применяйте метки Office 365 и политики защиты от потери данных для сайтов групп SharePoint Online с различными уровнями защиты информации.
ms.openlocfilehash: fd2fedf23b4e65bd32642b8528548f8a85533051
ms.sourcegitcommit: 6ff0233b5a1a07595f8b4d55db6b1327bcaa174c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2019
ms.locfileid: "28023459"
---
# <a name="protect-sharepoint-online-files-with-office-365-labels-and-dlp"></a><span data-ttu-id="c6c11-103">Защита файлов SharePoint Online с помощью меток Office 365 и DLP</span><span class="sxs-lookup"><span data-stu-id="c6c11-103">Protect SharePoint Online files with Office 365 labels and DLP</span></span>

 <span data-ttu-id="c6c11-104">**Сводка.** Применяйте метки Office 365 и политики защиты от потери данных для сайтов групп SharePoint Online с различными уровнями защиты информации.</span><span class="sxs-lookup"><span data-stu-id="c6c11-104">**Summary:** Apply Office 365 labels and data loss prevention (DLP) policies for SharePoint Online team sites with various levels of information protection.</span></span>
  
<span data-ttu-id="c6c11-p101">В этой статье описано создание и развертывание меток Office 365 и политик защиты от потери данных для базовых, конфиденциальных и строго конфиденциальных сайтов группы SharePoint Online. Дополнительные сведения об этих трех уровнях защиты см. в статье [Безопасность сайтов и файлов SharePoint Online](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="c6c11-p101">Use the steps in this article to design and deploy Office 365 labels and DLP policies for baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="how-this-works"></a><span data-ttu-id="c6c11-107">Как это работает</span><span class="sxs-lookup"><span data-stu-id="c6c11-107">How this works</span></span>
1. <span data-ttu-id="c6c11-p102">Создайте нужные метки и опубликуйте их. Для их публикации может потребоваться до 12 часов.</span><span class="sxs-lookup"><span data-stu-id="c6c11-p102">Create the desired labels and publish these. It can take up to 12 hours for these to be published.</span></span>
2. <span data-ttu-id="c6c11-110">Для нужных сайтов SharePoint измените параметры библиотеки документов, чтобы присвоить метку к элементам в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c6c11-110">For the desired SharePoint sites, edit the document library settings to apply a label to items in the library.</span></span>
3. <span data-ttu-id="c6c11-111">Создайте политики защиты от потери данных, чтобы выполнять действия на основе меток.</span><span class="sxs-lookup"><span data-stu-id="c6c11-111">Create DLP policies to take action based on the labels.</span></span>

<span data-ttu-id="c6c11-p103">Когда пользователи добавляют документ в библиотеку, этот документ получает назначенную метку по умолчанию. При необходимости пользователи могут изменить метку. Если пользователь делится документом за пределами организации, служба защиты от потери данных проверяет, назначена ли метка, и выполняет действия, если политика защиты от потери данных соответствует метке. Служба защиты от потери данных также проверяет соответствие другим политикам, таким как защита файлов с номерами кредитных карт, если этот тип политики настроен.</span><span class="sxs-lookup"><span data-stu-id="c6c11-p103">When users add a document to the library, the document will receive the assigned label by default. Users can change the label, if needed. When a user shares a document outside the organization, DLP will check to see if a label is assigned and take action if a DLP policy matches the label. DLP will look for other policy matches as well, such as protecting files with credit card numbers if this type of policy is configured.</span></span> 

## <a name="office-365-labels-for-your-sharepoint-online-sites"></a><span data-ttu-id="c6c11-116">Метки Office 365 для сайтов SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c6c11-116">Office 365 labels for your SharePoint Online sites</span></span>

<span data-ttu-id="c6c11-117">Существует три этапа создания и назначения меток Office 365 для сайтов группы SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c6c11-117">There are three phases to creating and then assigning Office 365 labels to SharePoint Online team sites.</span></span>
  
### <a name="phase-1-determine-the-office-365-label-names"></a><span data-ttu-id="c6c11-118">Этап 1. Определение имен меток Office 365</span><span class="sxs-lookup"><span data-stu-id="c6c11-118">Phase 1: Determine the Office 365 label names</span></span>

<span data-ttu-id="c6c11-p104">На этом этапе нужно определить названия меток Office 365 для четырех уровней защиты информации, применяемых к сайтам группы SharePoint Online. В приведенной ниже таблице перечислены рекомендуемые имена для каждого уровня.</span><span class="sxs-lookup"><span data-stu-id="c6c11-p104">In this phase, you determine the names of your Office 365 labels for the four levels of information protection applied to SharePoint Online team sites. The following table lists the recommended names for each level.</span></span>
  
|<span data-ttu-id="c6c11-121">**Уровень защиты сайта группы SharePoint Online**</span><span class="sxs-lookup"><span data-stu-id="c6c11-121">**SharePoint Online team site protection level**</span></span>|<span data-ttu-id="c6c11-122">**Имя метки**</span><span class="sxs-lookup"><span data-stu-id="c6c11-122">**Label name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6c11-123">Базовый общедоступный</span><span class="sxs-lookup"><span data-stu-id="c6c11-123">Baseline-Public</span></span>  <br/> |<span data-ttu-id="c6c11-124">Внутренний общедоступный</span><span class="sxs-lookup"><span data-stu-id="c6c11-124">Internal public</span></span>  <br/> |
|<span data-ttu-id="c6c11-125">Базовый частный</span><span class="sxs-lookup"><span data-stu-id="c6c11-125">Baseline-Private</span></span>  <br/> |<span data-ttu-id="c6c11-126">Private</span><span class="sxs-lookup"><span data-stu-id="c6c11-126">Private</span></span>  <br/> |
|<span data-ttu-id="c6c11-127">Конфиденциальный</span><span class="sxs-lookup"><span data-stu-id="c6c11-127">Sensitive</span></span>  <br/> |<span data-ttu-id="c6c11-128">Конфиденциальный</span><span class="sxs-lookup"><span data-stu-id="c6c11-128">Sensitive</span></span>  <br/> |
|<span data-ttu-id="c6c11-129">Строго конфиденциально</span><span class="sxs-lookup"><span data-stu-id="c6c11-129">Highly Confidential</span></span>  <br/> |<span data-ttu-id="c6c11-130">Строго конфиденциально</span><span class="sxs-lookup"><span data-stu-id="c6c11-130">Highly Confidential</span></span>  <br/> |
   
### <a name="phase-2-create-the-office-365-labels"></a><span data-ttu-id="c6c11-131">Этап 2. Создание меток Office 365</span><span class="sxs-lookup"><span data-stu-id="c6c11-131">Phase 2: Create the Office 365 labels</span></span>

<span data-ttu-id="c6c11-132">На этом этапе нужно создать и опубликовать определенные метки для разных уровней защиты информации.</span><span class="sxs-lookup"><span data-stu-id="c6c11-132">In this phase, you create and then publish your determined labels for the different levels of information protection.</span></span>
  
<span data-ttu-id="c6c11-133">Создать метки можно с помощью Microsoft PowerShell или Центра администрирования Office 365.</span><span class="sxs-lookup"><span data-stu-id="c6c11-133">To create the labels, you can use the Office 365 Admin center or Microsoft PowerShell.</span></span>
  
### <a name="create-office-365-labels-with-the-office-365-admin-center"></a><span data-ttu-id="c6c11-134">Создание меток Office 365 в Центре администрирования Office 365</span><span class="sxs-lookup"><span data-stu-id="c6c11-134">Create Office 365 labels with the Office 365 Admin center</span></span>

1. <span data-ttu-id="c6c11-p105">Войдите на портал Office 365, используя учетную запись с ролью администратора компании или администратора безопасности. Справочные сведения см. в статье [Вход в Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="c6c11-p105">Sign in to the Office 365 portal with an account that has the Security Administrator or Company Administrator role. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="c6c11-137">На вкладке **Домашняя страница Microsoft Office** щелкните плитку **Администрирование**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-137">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
3. <span data-ttu-id="c6c11-138">На новой вкладке браузера **Центр администрирования Office** выберите **Центры администрирования > Безопасность и соответствие требованиям**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-138">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
4. <span data-ttu-id="c6c11-139">На новой вкладке браузера **Главная — безопасность и соответствие требованиям** выберите **Классификации > Метки**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-139">From the new **Home - Security &amp; Compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
5. <span data-ttu-id="c6c11-140">В области **Главная > Метки** щелкните вкладку **Хранение** и нажмите кнопку **Создать метку**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-140">From the **Home > Labels** pane, click the **Retention** tab, and then click **Create a label**.</span></span>
    
6. <span data-ttu-id="c6c11-141">В области **Назовите метку** введите название метки и описание для администраторов и пользователей, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-141">On the **Name your label** pane, type the name of the label and a description for admins and users, and then click **Next**.</span></span>

7. <span data-ttu-id="c6c11-142">В области **Параметры метки** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-142">On the **Label settings** pane, click **Next**.</span></span>
    
8. <span data-ttu-id="c6c11-143">В области **Проверьте параметры** нажмите **Создать**, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-143">On the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="c6c11-144">Повторите действия 5–8, чтобы создать дополнительные метки.</span><span class="sxs-lookup"><span data-stu-id="c6c11-144">Repeat steps 5-8 for your additional labels.</span></span>
    
### <a name="create-office-365-labels-with-powershell"></a><span data-ttu-id="c6c11-145">Создание меток Office 365 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="c6c11-145">Create Office 365 labels with PowerShell</span></span>

1. <span data-ttu-id="c6c11-146">[Подключитесь к Центру безопасности и соответствия требованиям Office 365 с помощью удаленного сеанса PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409) и укажите данные учетной записи, которой назначена роль администратора безопасности или роль администратора организации.</span><span class="sxs-lookup"><span data-stu-id="c6c11-146">[Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409) and specify the credentials of an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="c6c11-147">Заполните список имен меток, а затем выполните эти команды в командной строке PowerShell:</span><span class="sxs-lookup"><span data-stu-id="c6c11-147">Fill out the list of label names, and then run these commands at the PowerShell command prompt:</span></span>
    
  ```
  $labelNames=@(<list of label names, each enclosed in quotes and separated by commas>)
ForEach ($element in $labelNames){ New-ComplianceTag -Name $element }
  ```

### <a name="publish-your-new-labels"></a><span data-ttu-id="c6c11-148">Публикация новых меток</span><span class="sxs-lookup"><span data-stu-id="c6c11-148">Publish your new labels</span></span>

<span data-ttu-id="c6c11-149">Для публикации новых меток Office 365 выполните действия, указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="c6c11-149">Next, use these steps to publish the new Office 365 labels.</span></span>
  
1. <span data-ttu-id="c6c11-150">В области **Главная > Метки** Центра безопасности и соответствия требованиям выберите вкладку **Хранение** и нажмите кнопку **Опубликовать метки**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-150">From the **Home > Labels** pane of the Security &amp; Compliance Center, click the **Retention** tab, and then click **Publish labels**.</span></span>
    
2. <span data-ttu-id="c6c11-151">В области **Выберите метки для публикации** щелкните **Выберите метки для публикации**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-151">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
3. <span data-ttu-id="c6c11-152">В области **Выбор меток** нажмите кнопку **Добавить** и выберите все четыре метки.</span><span class="sxs-lookup"><span data-stu-id="c6c11-152">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
4. <span data-ttu-id="c6c11-153">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-153">Click **Done**.</span></span>
    
5. <span data-ttu-id="c6c11-154">В области **Выберите метки для публикации** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-154">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="c6c11-155">В области **Выбор расположений** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-155">On the **Choose locations** pane, click **Next**.</span></span>
    
7. <span data-ttu-id="c6c11-156">В области **Назовите политику** введите название для своего набора меток в поле **Название**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-156">On the **Name your policy** pane, type a name for your set of labels in **Name**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="c6c11-157">В области **Проверьте настройки** выберите **Опубликовать метки** и нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-157">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

    
### <a name="phase-3-apply-the-office-365-labels-to-your-sharepoint-online-sites"></a><span data-ttu-id="c6c11-158">Этап 3. Применение меток Office 365 к сайтам SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c6c11-158">Phase 3: Apply the Office 365 labels to your SharePoint Online sites</span></span>

<span data-ttu-id="c6c11-159">Инструкции по применению меток Office 365 к папкам документов, размещенным на сайтах группы SharePoint Online, приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="c6c11-159">Use these steps to apply the Office 365 labels to the documents folders of your SharePoint Online team sites.</span></span>
  
1. <span data-ttu-id="c6c11-160">На вкладке браузера **Домашняя страница Microsoft Office** щелкните плитку **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-160">From the **Microsoft Office Home** tab of your browser, click the **SharePoint** tile.</span></span>
    
2. <span data-ttu-id="c6c11-161">На новой вкладке **SharePoint** в браузере выберите сайт, которому нужно назначить метку Office 365.</span><span class="sxs-lookup"><span data-stu-id="c6c11-161">On the new **SharePoint** tab in your browser, click a site that needs an Office 365 label assigned.</span></span>
    
3. <span data-ttu-id="c6c11-162">На новой вкладке SharePoint в браузере щелкните **Документы**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-162">In the new SharePoint site tab of your browser, click **Documents**.</span></span>
    
4. <span data-ttu-id="c6c11-163">Щелкните значок параметров, а затем **Параметры библиотеки**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-163">Click the settings icon, and then click **Library settings**.</span></span>
    
5. <span data-ttu-id="c6c11-164">В разделе **Разрешения и управление** нажмите **Применить метку к элементам в этой библиотеке**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-164">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
6. <span data-ttu-id="c6c11-165">В разделе **Параметры — применение метки** выберите соответствующую метку, а затем нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-165">In **Settings-Apply Label**, select the appropriate label, and then click **Save**.</span></span>
    
7. <span data-ttu-id="c6c11-166">Закройте вкладку сайта SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c6c11-166">Close the tab for the SharePoint Online site.</span></span>
    
8. <span data-ttu-id="c6c11-167">Повторите шаги с 3 по 8, чтобы назначить метки Office 365 для дополнительных сайтов SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c6c11-167">Repeat steps 3-8 to assign Office 365 labels to your additional SharePoint Online sites.</span></span>
    
<span data-ttu-id="c6c11-168">Ниже показана итоговая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="c6c11-168">Here is your resulting configuration.</span></span>
  
![Метки Office 365 для четырех типов сайтов групп SharePoint Online.](media/e0a4fdd2-1c30-4d93-8af4-a6f0c6c29966.png)
  
## <a name="dlp-policies-for-your-sharepoint-online-sites"></a><span data-ttu-id="c6c11-170">Политики защиты от потери данных для сайтов SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c6c11-170">DLP policies for your SharePoint Online sites</span></span>

<span data-ttu-id="c6c11-171">Выполните указанные ниже действия, чтобы настроить политику защиты от потери данных, которая уведомляет пользователей, когда они предоставляют доступ к документу с конфиденциального сайта группы SharePoint Online пользователям не из организации.</span><span class="sxs-lookup"><span data-stu-id="c6c11-171">Use these steps to configure a DLP policy that notifies users when they share a document on a SharePoint Online sensitive team site outside the organization.</span></span>

1. <span data-ttu-id="c6c11-172">На вкладке **Домашняя страница Microsoft Office** щелкните плитку **Администрирование**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-172">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="c6c11-173">На новой вкладке браузера **Центр администрирования Office** выберите **Центры администрирования > Безопасность и соответствие требованиям**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-173">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
3. <span data-ttu-id="c6c11-174">На новой вкладке **Безопасность и соответствие требованиям** выберите **Защита от потери данных > Политика**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-174">On the new **Security &amp; Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>
    
4. <span data-ttu-id="c6c11-175">В области **Защита от потери данных** нажмите кнопку **+ Создание политики**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-175">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>
    
5. <span data-ttu-id="c6c11-176">В области **Начать с шаблона или создать настраиваемую политику** выберите **Настраиваемая**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-176">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="c6c11-177">В области **Назовите политику** введите название для политики защиты от потери конфиденциальных данных в поле **Название**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-177">In the **Name your policy** pane, type the name for the sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="c6c11-178">В области **Выберите расположения** щелкните **Позволить мне выбрать расположения** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-178">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="c6c11-179">В списке расположений отключите параметры **Электронная почта Exchange** и **Учетные записи OneDrive**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-179">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="c6c11-180">В области **Выберите тип содержимого, которое вы хотите защитить** щелкните ссылку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-180">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="c6c11-181">В области **Выбрать типы содержимого для защиты** выберите **Добавить** в раскрывающемся списке, а затем выберите **Метки**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-181">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>
    
10. <span data-ttu-id="c6c11-182">В области **Метки** нажмите кнопку **+ Добавить**, укажите метку **Конфиденциальный** и последовательно нажмите кнопки **Добавить** > **Готово**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-182">In the **Labels** pane, click **+ Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="c6c11-183">В области **Выбрать типы содержимого для защиты** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-183">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="c6c11-184">В области **Выберите тип содержимого, которое вы хотите защитить** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-184">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="c6c11-185">В области **Что необходимо делать, если мы обнаружим конфиденциальные сведения?** щелкните **Настройка подсказки и уведомления**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-185">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="c6c11-186">В области **Настройка подсказок политики и уведомлений по электронной почте** щелкните **Измените текст подсказки политики**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-186">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="c6c11-187">В текстовом поле введите или вставьте одну из следующих подсказок в зависимости от того, применена ли служба Azure Information Protection, чтобы защитить строго конфиденциальные файлы:</span><span class="sxs-lookup"><span data-stu-id="c6c11-187">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="c6c11-p106">Чтобы предоставить доступ пользователю за пределами организации, скачайте файл и откройте его. Выберите пункты "Файл > Защитить документ > Зашифровать паролем", а затем укажите надежный пароль. Отправьте пароль в отдельном сообщении или с помощью других средств связи.</span><span class="sxs-lookup"><span data-stu-id="c6c11-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
  - <span data-ttu-id="c6c11-p107">Строго конфиденциальные файлы защищены с помощью шифрования. Их могут просматривать только те внешние пользователи, которым ваш ИТ-отдел предоставил разрешения для этих файлов.</span><span class="sxs-lookup"><span data-stu-id="c6c11-p107">Highly confidential files are protected with encryption. Only external users who are granted permissions to these files by your IT department can read them.</span></span>
    
    <span data-ttu-id="c6c11-193">Вы также можете ввести или вставить собственную подсказку политики, которая укажет пользователям, как делиться файлом с людьми за пределами организации.</span><span class="sxs-lookup"><span data-stu-id="c6c11-193">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="c6c11-194">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-194">Click **OK**.</span></span>
    
17. <span data-ttu-id="c6c11-195">В области **Что необходимо делать, если мы обнаружим конфиденциальные сведения?** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-195">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="c6c11-196">В области **Вы хотите включить политику или сначала проверить, как все работает?** выберите пункт **Да, включить сразу**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-196">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="c6c11-197">В области **Проверьте параметры** нажмите **Создать**, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-197">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="c6c11-198">Здесь показана итоговая конфигурация для конфиденциальных сайтов групп SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c6c11-198">Here is your resulting configuration for sensitive SharePoint Online team sites.</span></span>
  
![Политика защиты от потери данных для изолированного сайта группы SharePoint Online с использованием метки "Конфиденциальный" в Office 365.](media/2ff4cc53-87a8-43e3-b637-3068d88409f3.png)
  
<span data-ttu-id="c6c11-200">Выполните следующие действия, чтобы настроить политику защиты от потери данных, которая блокирует пользователей, когда они совместно используют документы на строго конфиденциальном сайте группы SharePoint Online за пределами организации.</span><span class="sxs-lookup"><span data-stu-id="c6c11-200">Next, use these steps to configure a DLP policy that blocks users when they share a document on a SharePoint Online highly confidential team site outside the organization.</span></span>
  
1. <span data-ttu-id="c6c11-201">На вкладке браузера **Домашняя страница Microsoft Office** щелкните плитку **Безопасность и соответствие требованиям**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-201">From the **Microsoft Office Home** tab in your browser, click the **Security &amp; Compliance** tile.</span></span>
    
2. <span data-ttu-id="c6c11-202">На новой вкладке **Безопасность и соответствие требованиям** выберите **Защита от потери данных > Политика**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-202">On the new **Security &amp; Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>
    
3. <span data-ttu-id="c6c11-203">В области **Защита от потери данных** нажмите кнопку **+ Создание политики**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-203">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>
    
4. <span data-ttu-id="c6c11-204">В области **Начать с шаблона или создать настраиваемую политику** выберите **Настраиваемая**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-204">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="c6c11-205">В области **Назовите политику** введите название для политики защиты от потери строго конфиденциальных данных в поле **Название**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-205">In the **Name your policy** pane, type the name for the highly sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="c6c11-206">В области **Выберите расположения** щелкните **Позволить мне выбрать расположения** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-206">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="c6c11-207">В списке расположений отключите параметры **Электронная почта Exchange** и **Учетные записи OneDrive**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-207">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="c6c11-208">В области **Выберите тип содержимого, которое вы хотите защитить** щелкните ссылку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-208">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="c6c11-209">В области **Выбрать типы содержимого для защиты** выберите **Добавить** в раскрывающемся списке, а затем выберите **Метки**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-209">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>
    
10. <span data-ttu-id="c6c11-210">В области **Метки** нажмите кнопку **+ Добавить**, выберите метку **Строго конфиденциальный**, нажмите **Добавить**, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-210">In the **Labels** pane, click **+ Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="c6c11-211">В области **Выбрать типы содержимого для защиты** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-211">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="c6c11-212">В области **Выберите тип содержимого, которое вы хотите защитить** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-212">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>
    
13. <span data-ttu-id="c6c11-213">В области **Что необходимо делать, если мы обнаружим конфиденциальные сведения?** щелкните **Настройка подсказки и уведомления**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-213">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="c6c11-214">В области **Настройка подсказок политики и уведомлений по электронной почте** щелкните **Измените текст подсказки политики**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-214">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="c6c11-215">В текстовом поле введите или вставьте следующее:</span><span class="sxs-lookup"><span data-stu-id="c6c11-215">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="c6c11-p108">Чтобы предоставить доступ пользователю за пределами организации, скачайте файл и откройте его. Выберите пункты "Файл > Защитить документ > Зашифровать паролем", а затем укажите надежный пароль. Отправьте пароль в отдельном сообщении или с помощью других средств связи.</span><span class="sxs-lookup"><span data-stu-id="c6c11-p108">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
    <span data-ttu-id="c6c11-219">Вы также можете ввести или вставить, скопировав, собственную подсказку политики, которая укажет пользователям, как делиться файлом с людьми за пределами организации.</span><span class="sxs-lookup"><span data-stu-id="c6c11-219">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="c6c11-220">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-220">Click **OK**.</span></span>
    
17. <span data-ttu-id="c6c11-221">В области **Что необходимо делать, если мы обнаружим конфиденциальные сведения?** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-221">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="c6c11-222">В области **Вы хотите включить политику или сначала проверить, как все работает?** выберите пункт **Да, включить сразу**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-222">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="c6c11-223">В области **Проверьте параметры** нажмите **Создать**, а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="c6c11-223">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="c6c11-224">Ниже показана итоговая конфигурация для строго конфиденциальных сайтов групп SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c6c11-224">Here is your resulting configuration for high confidentiality SharePoint Online team sites.</span></span>
  
![Политика защиты от потери данных для изолированного сайта группы SharePoint Online с использованием метки "Строго конфиденциальный" в Office 365.](media/f705d3d0-23c9-4333-8b70-ad3b91f835ea.png)
  
## <a name="next-step"></a><span data-ttu-id="c6c11-226">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="c6c11-226">Next step</span></span>

[<span data-ttu-id="c6c11-227">Защита файлов SharePoint Online с помощью Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="c6c11-227">Protect SharePoint Online files with Azure Information Protection</span></span>](protect-sharepoint-online-files-with-azure-information-protection.md)
    
## <a name="see-also"></a><span data-ttu-id="c6c11-228">См. также</span><span class="sxs-lookup"><span data-stu-id="c6c11-228">See Also</span></span>

[<span data-ttu-id="c6c11-229">Безопасность сайтов и файлов SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c6c11-229">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="c6c11-230">Защита сайтов SharePoint Online в среде разработки и тестирования</span><span class="sxs-lookup"><span data-stu-id="c6c11-230">Secure SharePoint Online sites in a dev/test environment</span></span>](secure-sharepoint-online-sites-in-a-dev-test-environment.md)
  
[<span data-ttu-id="c6c11-231">Руководство по безопасности (Майкрософт) для политических кампаний, некоммерческих и других динамических организаций</span><span class="sxs-lookup"><span data-stu-id="c6c11-231">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="c6c11-232">Освоение облака и гибридные решения</span><span class="sxs-lookup"><span data-stu-id="c6c11-232">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)


