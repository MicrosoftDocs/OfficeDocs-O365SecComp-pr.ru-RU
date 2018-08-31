---
title: Начало работы со стандартной политикой защиты от потери данных
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/10/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
description: Перед созданием даже первой политики предотвращения (DLP) потери данных, защиты от потери данных помогает защитить конфиденциальные сведения с политикой по умолчанию. Эту политику по умолчанию и его сохранить справки рекомендации (как показано ниже), конфиденциальные контента безопасной, о том, когда номер электронной почты или документов, содержащих данные о банковской карты были совместно с пользователей из других организаций.
ms.openlocfilehash: 1b522a2c04e72353970ef5dfcd62183023a01994
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535510"
---
# <a name="get-started-with-the-default-dlp-policy"></a><span data-ttu-id="152cf-104">Начало работы со стандартной политикой защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="152cf-104">Get started with the default DLP policy</span></span>

<span data-ttu-id="152cf-p102">Перед созданием даже первой политики предотвращения (DLP) потери данных, защиты от потери данных помогает защитить конфиденциальные сведения с политикой по умолчанию. Эту политику по умолчанию и его сохранить справки рекомендации (как показано ниже), конфиденциальные контента безопасной, о том, когда номер электронной почты или документов, содержащих данные о банковской карты были совместно с пользователей из других организаций. Эта рекомендация будет отображаться на **домашней** странице безопасности &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="152cf-p102">Before you even create your first data loss prevention (DLP) policy, DLP is helping to protect your sensitive information with a default policy. This default policy and its recommendation (shown below) help keep your sensitive content secure by notifying you when email or documents containing a credit card number were shared with someone outside your organization. You'll see this recommendation on the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="152cf-p103">Можно использовать этот мини-приложения для быстрого просмотра и когда общий объем конфиденциальной информации и затем уточнить политику защиты от потери данных по умолчанию в одним щелчком или двумя. Можно также изменить политику защиты от потери данных по умолчанию в любое время, так как он является полностью настраиваемым. Обратите внимание, что если отсутствует рекомендуется в первую очередь, попробуйте нажать кнопку **+ Дополнительные** в нижней части раздела **рекомендуется для вас** .</span><span class="sxs-lookup"><span data-stu-id="152cf-p103">You can use this widget to quickly view when and how much sensitive information was shared, and then refine the default DLP policy in just a click or two. You can also edit the default DLP policy at any time because it's fully customizable. Note that if you don't see the recommendation at first, try clicking **+More** at the bottom of the **Recommended for you** section.</span></span> 
  
![Мини-приложения с именем дополнительных защитить общее содержимое](media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a><span data-ttu-id="152cf-112">Просмотр отчета и уточнение политики защиты от потери данных по умолчанию</span><span class="sxs-lookup"><span data-stu-id="152cf-112">View the report and refine the default DLP policy</span></span>

<span data-ttu-id="152cf-113">Когда мини-приложения показывает, что пользователи общих конфиденциальной информации с людьми за пределами вашей организации, выберите **политики предотвращения потери данных уточнения** в нижней.</span><span class="sxs-lookup"><span data-stu-id="152cf-113">When the widget shows you that users have shared sensitive information with people outside your organization, choose **Refine DLP policy** at the bottom.</span></span> 
  
<span data-ttu-id="152cf-p104">Подробный отчет показывает, когда и как большего количества содержимого, содержащие цифры, данные о банковской карте предоставлен общий доступ в за последние 30 дней. Обратите внимание на то, что соответствия правилам может занять до 48 часов, отображаемых в мини-приложения.</span><span class="sxs-lookup"><span data-stu-id="152cf-p104">The detailed report shows you when and how much content containing credit card numbers was shared in the past 30 days. Note that rule matches can take up to 48 hours to show up in the widget.</span></span>
  
<span data-ttu-id="152cf-116">Для защиты конфиденциальных данных, политику защиты от потери данных по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="152cf-116">To help protect the sensitive information, the default DLP policy:</span></span>
  
- <span data-ttu-id="152cf-117">Определяет, когда содержимое в Exchange, SharePoint и OneDrive, который содержит по крайней мере один кредитной карты номер используется совместно с людьми за пределами вашей организации.</span><span class="sxs-lookup"><span data-stu-id="152cf-117">Detects when content in Exchange, SharePoint, and OneDrive that contains at least one credit card number is shared with people outside your organization.</span></span>
    
- <span data-ttu-id="152cf-p105">Отображает подсказки политики и отправляет уведомления по электронной почте пользователи при попытке общий доступ к этой конфиденциальной информации с людьми за пределами вашей организации. Дополнительные сведения об этих параметрах можно [отправлять уведомления по электронной почте и советы политики для политики защиты от потери данных](use-notifications-and-policy-tips.md).</span><span class="sxs-lookup"><span data-stu-id="152cf-p105">Shows a policy tip and sends an email notification to users when they attempt to share this sensitive information with people outside your organization. For more information on these options, see [Send email notifications and show policy tips for DLP policies](use-notifications-and-policy-tips.md).</span></span>
    
- <span data-ttu-id="152cf-p106">Создает отчеты, подробные активности, чтобы кто общее содержимое с людьми за пределами вашей организации и когда они были можно отслеживать. Можно использовать [отчеты защиты от потери данных](view-the-dlp-reports.md) и [данных журнала аудита](search-the-audit-log-in-security-and-compliance.md) (где **активности** = **защиты от потери данных**) чтобы видеть эти сведения.</span><span class="sxs-lookup"><span data-stu-id="152cf-p106">Generates detailed activity reports so that you can track things like who shared the content with people outside your organization and when they did it. You can use the [DLP reports](view-the-dlp-reports.md) and [audit log data](search-the-audit-log-in-security-and-compliance.md) (where **Activity** = **DLP**) to see this information.</span></span>
    
<span data-ttu-id="152cf-122">Чтобы быстро уточнить политику защиты от потери данных по умолчанию, можно выбрать для его:</span><span class="sxs-lookup"><span data-stu-id="152cf-122">To quickly refine the default DLP policy, you can choose to have it:</span></span>
  
- <span data-ttu-id="152cf-123">Отправлено сообщение электронной почты отчет об инциденте при пользователям общий доступ к этой конфиденциальной информации с людьми за пределами вашей организации.</span><span class="sxs-lookup"><span data-stu-id="152cf-123">Send you an incident report email when users share this sensitive information with people outside your organization.</span></span>
    
- <span data-ttu-id="152cf-124">Добавление других пользователей в отчет об инциденте электронной почты.</span><span class="sxs-lookup"><span data-stu-id="152cf-124">Add other users to the email incident report.</span></span>
    
- <span data-ttu-id="152cf-125">Заблокируйте доступ к контенту, содержащих конфиденциальные данные, но пользователи могут переопределить и совместно использовать или отправить, если нужно.</span><span class="sxs-lookup"><span data-stu-id="152cf-125">Block access to the content containing the sensitive information, but allow the user to override and share or send if they need to.</span></span>
    
<span data-ttu-id="152cf-126">Дополнительные сведения об инциденте отчеты или ограничение доступа можно [Обзор политик предотвращения потери данных](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="152cf-126">For more information on incident reports or restricting access, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
<span data-ttu-id="152cf-127">Если вы хотите изменить эти параметры позже, можно изменить значение по умолчанию политики предотвращения потери данных в любое время - содержится в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="152cf-127">If you want to change these options later, you can edit the default DLP policy at any time - see the next section.</span></span>
  
![Параметры для мини-приложения с именем дополнительных защитить общее содержимое](media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a><span data-ttu-id="152cf-129">Изменение политики защиты от потери данных по умолчанию</span><span class="sxs-lookup"><span data-stu-id="152cf-129">Edit the default DLP policy</span></span>

<span data-ttu-id="152cf-130">Эту политику с именем **политики по умолчанию Office 365 защиты от потери данных** и отображается в разделе **Защита от потери данных** на странице **Политика** безопасности &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="152cf-130">This policy is named **Default Office 365 DLP policy** and appears under **Data loss prevention** on the **Policy** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="152cf-p107">Эта политика является полностью настраиваемым и то же, что все политики предотвращения потери данных, создайте самостоятельно «с нуля». Кроме того, можно отключить или удалить политику, чтобы пользователи больше не получать советы по политикам или по электронной почте уведомления.</span><span class="sxs-lookup"><span data-stu-id="152cf-p107">This policy is fully customizable, the same as any DLP policy that you create yourself from scratch. You can also turn off or delete the policy, so that your users no longer receive policy tips or email notifications.</span></span>
  
![Политики защиты от потери данных с именем политики по умолчанию Office 365 защиты от потери данных](media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a><span data-ttu-id="152cf-134">Если мини-приложения и не отображается</span><span class="sxs-lookup"><span data-stu-id="152cf-134">When the widget does and does not appear</span></span>

<span data-ttu-id="152cf-135">Мини-приложения с именем **защиты общего содержимого** отображается в разделе **рекомендуется для вас** на **домашней** странице приложения безопасности &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="152cf-135">The widget named **Further protect shared content** appears in the **Recommended for you** section of the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="152cf-136">В этом мини-приложения отображается, только если:</span><span class="sxs-lookup"><span data-stu-id="152cf-136">This widget appears only when:</span></span>
  
- <span data-ttu-id="152cf-p108">Существует не политики предотвращения потери данных в системы &amp; центре соответствия требованиям или центра администрирования Exchange. В этом мини-приложения, предназначенного для помогут приступить к работе с защиты от потери данных, поэтому он не отображается, если у вас уже есть политик защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="152cf-p108">There are no data loss prevention policies in the Security &amp; Compliance Center or Exchange Admin Center. This widget is intended to help you get started with DLP, so it doesn't appear if you already have DLP policies.</span></span>
    
- <span data-ttu-id="152cf-139">Контент, содержащий как минимум одной кредитной карты общего пользователя не из вашей организации за последние 30 дней.</span><span class="sxs-lookup"><span data-stu-id="152cf-139">Content containing least one credit card has been shared with someone outside your organization in the past 30 days.</span></span>
    
<span data-ttu-id="152cf-140">Обратите внимание на то, что соответствия правилам может занять до 48 часов должно быть доступно мини-приложения, поэтому после обнаружения общих извне конфиденциальной информации может потребоваться до двух дней рекомендация по отображаются.</span><span class="sxs-lookup"><span data-stu-id="152cf-140">Note that rule matches can take up to 48 hours to be available to the widget, so after sensitive information shared externally is detected, it may take up to two days for the recommendation to appear.</span></span>
  
<span data-ttu-id="152cf-141">И, наконец уточните политику защиты от потери данных по умолчанию с помощью мини-приложения, мини-приложения исчезнет из на **домашней** странице.</span><span class="sxs-lookup"><span data-stu-id="152cf-141">Finally, after you use the widget to refine the default DLP policy, the widget disappears from the **Home** page.</span></span> 
  

