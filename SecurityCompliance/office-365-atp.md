---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 10/09/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
description: Office 365 расширенной защитой включает в себя подделка аналитики, безопасных ссылок, безопасные вложения и расширенные возможности фишинга. Расширенные защиту от угроз также расширяемый для файлов в SharePoint Online, OneDrive для бизнеса и группами Майкрософт.
ms.openlocfilehash: fed816ec8cd0e3e7a6b5118fde35d81647b94f02
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454356"
---
# <a name="office-365-advanced-threat-protection"></a><span data-ttu-id="44f08-104">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="44f08-104">Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="44f08-105">Office 365 расширенного угроз защиты анализа помогает защитить организацию от злонамеренных атак с:</span><span class="sxs-lookup"><span data-stu-id="44f08-105">Office 365 Advanced Threat Protection (ATP) helps to protect your organization from malicious attacks by:</span></span>
  
- <span data-ttu-id="44f08-106">Проверка вложений электронной почты на наличие вредоносных программ с [ATP безопасные вложения](atp-safe-attachments.md)</span><span class="sxs-lookup"><span data-stu-id="44f08-106">Scanning email attachments for malware with [ATP Safe Attachments](atp-safe-attachments.md)</span></span>
    
- <span data-ttu-id="44f08-107">Сканирования веб-адресов (URL-адреса) в документах Office со [Ссылками безопасных анализа](atp-safe-links.md) и сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="44f08-107">Scanning web addresses (URLs) in email messages and Office documents with [ATP Safe Links](atp-safe-links.md)</span></span>
    
- <span data-ttu-id="44f08-108">Идентификации и блокировки вредоносных файлов в библиотеках online с помощью [ПАКЕТА для SharePoint, OneDrive и группами Майкрософт](atp-for-spo-odb-and-teams.md)</span><span class="sxs-lookup"><span data-stu-id="44f08-108">Identifying and blocking malicious files in online libraries with [ATP for SharePoint, OneDrive, and Microsoft Teams](atp-for-spo-odb-and-teams.md)</span></span>
    
- <span data-ttu-id="44f08-109">Проверка сообщений электронной почты для несанкционированного Спуфинг с [Подделка аналитики](learn-about-spoof-intelligence.md)</span><span class="sxs-lookup"><span data-stu-id="44f08-109">Checking email messages for unauthorized spoofing with [spoof intelligence](learn-about-spoof-intelligence.md)</span></span>
    
- <span data-ttu-id="44f08-110">Определение, когда кто-то пытается олицетворять пользователей и пользовательских доменов вашей организации с [возможностями фишинга ATP в Office 365](atp-anti-phishing.md)</span><span class="sxs-lookup"><span data-stu-id="44f08-110">Detecting when someone attempts to impersonate your users and your organization's custom domains with [ATP anti-phishing capabilities in Office 365](atp-anti-phishing.md)</span></span>
    
<span data-ttu-id="44f08-p102">**Защита через Office 365 ATP определяет, какие политики, которые группа безопасности вашей организации определяет для безопасных ссылок, безопасные вложения и фишинга**. Очень важно периодически просмотреть и изменить политик хранения их в актуальном состоянии и воспользоваться преимуществами новых функций, которые добавляются к службе. [Отчеты доступны](view-reports-for-atp.md) для отображения как работа ATP для вашей организации. Эти отчеты можно также показывают областях, где может потребоваться просмотр и обновление политик. И, если у вас есть файлы, которые помечены как вредоносных программ, которые не должны быть или файлов, предоставляемых Microsoft для проверки, можно [Отправить файл в корпорацию Майкрософт для анализа](#submit-a-suspicious-file-to-microsoft-for-analysis).</span><span class="sxs-lookup"><span data-stu-id="44f08-p102">**Protection through Office 365 ATP is determined by policies that your organization's security team defines for Safe Links, Safe Attachments, and Anti-Phishing**. It's important to periodically review and revise your policies to keep them up to date and to take advantages of new features that are added to the service. [Reports are available](view-reports-for-atp.md) to show how ATP is working for your organization. These reports can also show you areas where you might need to review and update your policies. And, if you have files that are marked as malware that shouldn't be, or files you'd like Microsoft to examine, you can [submit a file to Microsoft for analysis](#submit-a-suspicious-file-to-microsoft-for-analysis).</span></span>
      
## <a name="get-office-365-atp"></a><span data-ttu-id="44f08-116">Получение ПАКЕТА Office 365</span><span class="sxs-lookup"><span data-stu-id="44f08-116">Get Office 365 ATP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44f08-p103">Office 365 ATP включен в подписки, например Microsoft 365 Enterprise, Office 365 корпоративный E5, Office 365 Education A5 и [365 Microsoft Business](https://support.office.com/article/c123694a-1efb-459e-a8d5-2187975373dc). Если в вашей организации есть подписка на Office 365, которая не включает Office 365 ATP, вы можете приобрести ATP потенциально как дополнительный компонент. Дополнительные сведения см в [Office 365 расширенного угроз защиты описание службы](https://technet.microsoft.com/library/exchange-online-advanced-threat-protection-service-description.aspx).</span><span class="sxs-lookup"><span data-stu-id="44f08-p103">Office 365 ATP is included in subscriptions, such as Microsoft 365 Enterprise, Office 365 Enterprise E5, Office 365 Education A5, and [Microsoft 365 Business](https://support.office.com/article/c123694a-1efb-459e-a8d5-2187975373dc). If your organization has an Office 365 subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on. For more information, see [Office 365 Advanced Threat Protection Service Description](https://technet.microsoft.com/library/exchange-online-advanced-threat-protection-service-description.aspx).</span></span> 

1. <span data-ttu-id="44f08-120">Как администратор глобальной или безопасности, перейдите к [https://portal.office.com](https://portal.office.com) и войдите с работы или школы учетную запись на Office 365.</span><span class="sxs-lookup"><span data-stu-id="44f08-120">As a global or security administrator, go to [https://portal.office.com](https://portal.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="44f08-121">Выберите пункты **Администрирование** \> **выставления счетов** для просмотра текущего подписка включает.</span><span class="sxs-lookup"><span data-stu-id="44f08-121">Choose **Admin** \> **Billing** to see what your current subscription includes.</span></span> <br/><span data-ttu-id="44f08-122">![Как глобальный администратор, войдите в систему в portal.office.com и перейдите к разделу администратор \> по выставлению счетов](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)</span><span class="sxs-lookup"><span data-stu-id="44f08-122">![As a global admin, sign in at portal.office.com and go to Admin \> Billing](media/18a3546c-bd1f-4f49-82ec-0184909b42c2.png)</span></span>
  
3. <span data-ttu-id="44f08-123">Если отображаются **Office 365 Enterprise E5**, **Office 365 Education A5**или **Microsoft 365 Business**вашей организации есть анализа.</span><span class="sxs-lookup"><span data-stu-id="44f08-123">If you see **Office 365 Enterprise E5**, **Office 365 Education A5**, or **Microsoft 365 Business**, then your organization has ATP.</span></span> <br/><span data-ttu-id="44f08-p104">Если отображаются разные подписки, например **Office 365 для предприятий E3** или **Office 365 корпоративный E1**, рассмотрите возможность добавления анализа. Для этого нажмите кнопку **+ Добавить подписку**.</span><span class="sxs-lookup"><span data-stu-id="44f08-p104">If you see a different subscription, such as **Office 365 Enterprise E3** or **Office 365 Enterprise E1**, consider adding ATP. To do that, choose **+ Add subscription**.</span></span>
    
<span data-ttu-id="44f08-126">После получения ATP следующим шагом является для группы безопасности для определения политик.</span><span class="sxs-lookup"><span data-stu-id="44f08-126">Once you have ATP, the next step is for your security team to define policies.</span></span> 
  
## <a name="define-policies-for-atp"></a><span data-ttu-id="44f08-127">Определение политик для анализа</span><span class="sxs-lookup"><span data-stu-id="44f08-127">Define policies for ATP</span></span>

- <span data-ttu-id="44f08-128">**[Настройка политик фишинга ATP в Office 365](set-up-atp-anti-phishing-policies.md)** включая олицетворения-атак защита от злоумышленников отправлять сообщения электронной почты, который выглядит от доверенных пользователей или доменов</span><span class="sxs-lookup"><span data-stu-id="44f08-128">**[Set up ATP anti-phishing policies in Office 365](set-up-atp-anti-phishing-policies.md)** including impersonation-based attacks to protect against attackers who send email messages that appear to be from trusted people or domains</span></span> 

- <span data-ttu-id="44f08-129">**[Настройка политик ATP безопасных ссылок в Office 365](set-up-atp-safe-links-policies.md)** включая [Настраиваемый список заблокированных URL-адреса](set-up-a-custom-blocked-urls-list-wtih-atp.md) и [Настраиваемый список «Не rewrite» URL-адреса](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) вашей организации</span><span class="sxs-lookup"><span data-stu-id="44f08-129">**[Set up ATP Safe Links policies in Office 365](set-up-atp-safe-links-policies.md)** including your organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md) and [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md)</span></span>
    
- <span data-ttu-id="44f08-130">**[Настройка безопасных вложений ATP политики в Office 365](set-up-atp-safe-attachments-policies.md)** , который может содержать [динамические доставки и предварительный просмотр](dynamic-delivery-and-previewing.md)</span><span class="sxs-lookup"><span data-stu-id="44f08-130">**[Set up ATP Safe Attachments policies in Office 365](set-up-atp-safe-attachments-policies.md)** that can include [dynamic delivery and previewing](dynamic-delivery-and-previewing.md)</span></span>
  
## <a name="see-how-atp-is-working-by-viewing-reports"></a><span data-ttu-id="44f08-131">Как работает ATP отчеты</span><span class="sxs-lookup"><span data-stu-id="44f08-131">See how ATP is working by viewing reports</span></span>

<span data-ttu-id="44f08-132">После политиках ATP отчеты доступны для отображения как работа службы.</span><span class="sxs-lookup"><span data-stu-id="44f08-132">After your ATP policies are in place, reports are available to show how the service is working.</span></span>

<span data-ttu-id="44f08-133">[![Безопасность &amp; панели мониторинга в центре соответствия требованиям, которые помогут посмотреть, где работает расширенного защиту от угроз](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)</span><span class="sxs-lookup"><span data-stu-id="44f08-133">[![The Security &amp; Compliance Center dashboard can help you see where Advanced Threat Protection is working](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)](view-reports-for-atp.md)</span></span>
  
1. <span data-ttu-id="44f08-p105">Убедитесь в том, что вы являетесь глобального администратора, администратора безопасности или чтения безопасности Office 365. (Увидеть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="44f08-p105">Make sure that you are an Office 365 global administrator, security administrator, or security reader. (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>
    
2. <span data-ttu-id="44f08-136">[Просмотр отчетов для расширенного защиту от угроз](view-reports-for-atp.md).</span><span class="sxs-lookup"><span data-stu-id="44f08-136">[View reports for Advanced Threat Protection](view-reports-for-atp.md).</span></span>
    
3. <span data-ttu-id="44f08-p106">При необходимости, внести изменения в политиках безопасности. Воспользуйтесь следующими ресурсами:</span><span class="sxs-lookup"><span data-stu-id="44f08-p106">If needed, make adjustments to your security policies. See the following resources:</span></span>

  - [<span data-ttu-id="44f08-139">Пакет анализа фишинга политики в Office 365</span><span class="sxs-lookup"><span data-stu-id="44f08-139">ATP anti-phishing policies in Office 365</span></span>](set-up-atp-anti-phishing-policies.md)
    
  - [<span data-ttu-id="44f08-140">Безопасные ссылки ATP политики в Office 365</span><span class="sxs-lookup"><span data-stu-id="44f08-140">ATP Safe Links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
    
  - [<span data-ttu-id="44f08-141">Безопасные вложения ATP политики в Office 365</span><span class="sxs-lookup"><span data-stu-id="44f08-141">ATP Safe Attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
    
    
## <a name="submit-a-suspicious-file-to-microsoft-for-analysis"></a><span data-ttu-id="44f08-142">Отправка подозрительных файлов в корпорацию Майкрософт для анализа</span><span class="sxs-lookup"><span data-stu-id="44f08-142">Submit a suspicious file to Microsoft for analysis</span></span>

- <span data-ttu-id="44f08-p107">Если файл, который может быть вредоносных программ, можно отправить этот файл в корпорацию Майкрософт для анализа. Посетите [портал отправки аналитики безопасности Защитника Windows](https://go.microsoft.com/fwlink/?linkid=857185).</span><span class="sxs-lookup"><span data-stu-id="44f08-p107">If you get a file that you suspect could be malware, you can submit that file to Microsoft for analysis. Visit the [Windows Defender Security Intelligence submission portal](https://go.microsoft.com/fwlink/?linkid=857185).</span></span>

- <span data-ttu-id="44f08-145">Если вы получите сообщение электронной почты (с или без вложения), который вы хотите отправить в корпорацию Майкрософт для анализа, используйте [надстройки сообщения отчета](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="44f08-145">If you get an email message (with or without an attachment) that you'd like to submit to Microsoft for analysis, use the [Report Message add-in](enable-the-report-message-add-in.md).</span></span> 
  
## <a name="related-topics"></a><span data-ttu-id="44f08-146">Смежные темы</span><span class="sxs-lookup"><span data-stu-id="44f08-146">Related topics</span></span>

[<span data-ttu-id="44f08-147">Просмотр отчетов для расширенного защиту от угроз</span><span class="sxs-lookup"><span data-stu-id="44f08-147">View the reports for Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  
[<span data-ttu-id="44f08-148">Угроз управления безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="44f08-148">Threat management in the Office 365 Security &amp; Compliance Center</span></span>](threat-management.md)
  

