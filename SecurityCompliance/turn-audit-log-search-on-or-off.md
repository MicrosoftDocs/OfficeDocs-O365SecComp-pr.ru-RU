---
title: Включение и отключение поиска в журнале аудита Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Можно включить функцию поиска журнала аудита безопасности Office 365 &amp; центре соответствия требованиям. Чтобы изменить вам необходимо учитывать, можно включить, если выключены в любое время. При отключенном поиска журналов аудита администраторов нельзя поиск в журнале аудита Office 365 для действия пользователя и администратора в вашей организации.
ms.openlocfilehash: 4fa6ac095222addce578294813cbd22dfc50a2ab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534862"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="f2dd5-105">Включение и отключение поиска в журнале аудита Office 365</span><span class="sxs-lookup"><span data-stu-id="f2dd5-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="f2dd5-p102">Вы (или другой администрирования) необходимо включить ведение журнала аудита, перед тем как начать поиск в журнале аудита Office 365. Когда проводить аудит операций поиска журнала безопасности Office 365 &amp; включена центре соответствия требованиям, записанные в журнал аудита и сохраняются в течение 90 дней действия администратора и пользователя из вашей организации. Тем не менее организации могут не нужно записать и сохранять данные журнала аудита. Или можно использовать приложения сторонних производителей безопасности сведения и события управления (SIEM) для доступа к данным аудита. В таких случаях глобального администратора можно отключить поиск журнала аудита в Office 365.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-p102">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log. When audit log search in the Office 365 Security &amp; Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days. However, your organization might not want to record and retain audit log data. Or you might be using a third-party security information and event management (SIEM) application to access your auditing data. In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="f2dd5-111">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="f2dd5-111">Before you begin</span></span>

- <span data-ttu-id="f2dd5-p103">Вы должны быть назначены роли журналов аудита в Exchange Online Включение и отключение поиска журнала аудита в организации Office 365. По умолчанию эта роль назначается группы ролей управления организацией и Управление соответствием требованиям на странице " **разрешения** " в центре администрирования Exchange. Глобальные администраторы в Office 365 являются участниками группы ролей управления организацией и в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-p103">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization. By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="f2dd5-p104">Пользователи имеют соответствующие разрешения в Exchange Online для включения поиска журнала аудита, включено или отключено. Если назначение пользователю роли журналов аудита на странице " **разрешения** " в параметрах безопасности &amp; центре соответствия требованиям, они не сможет получить отключение поиска журнала аудита. Это основной командлет — это командлет командной Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-p104">Users have to be assigned permissions in Exchange Online to turn audit log search on or off. If you assign users the Audit Logs role on the **Permissions** page in the Security &amp; Compliance Center, they won't be able to turn audit log search on or off. This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="f2dd5-p105">При выключении поиска журнала аудита в Office 365 API действия для управления Office 365 по-прежнему можно использовать для доступа к данным аудита для вашей организации. Отключение поиска журнала аудита, выполнив действия, описанные в этой статье означает, что не будет возвращать результатов при выполнении поиска с помощью безопасность журнала аудита &amp; центре соответствия требованиям или при запуске командлета **Search-UnifiedAuditLog** в Exchange Online PowerShell. Тем не менее, если вы задали любого приложения для доступа к вашей организации данных аудита с помощью API действия для управления Office 365, эти приложения будут работать.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-p105">If you turn off audit log search in Office 365, you can still use the Office 365 Management Activity API to access auditing data for your organization. Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security &amp; Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell. However, if you've authorized any application to access your organization's auditing data via the Office 365 Management Activity API , those applications will continue to work.</span></span> 
    
- <span data-ttu-id="f2dd5-121">Пошаговые инструкции по поиску Office 365 журнал аудита, см [Поиск в журнале аудита безопасности Office 365 &amp; центре соответствия требованиям](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="f2dd5-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="f2dd5-122">Включение поиска журнала аудита</span><span class="sxs-lookup"><span data-stu-id="f2dd5-122">Turn on audit log search</span></span>

<span data-ttu-id="f2dd5-p106">Можно использовать безопасность &amp; центре соответствия требованиям или PowerShell для включения поиска журнала аудита в Office 365. Выполнение может занять несколько часов после включения поиска журнала аудита перед может возвращать результаты при поиске в журнал аудита. Необходимо назначить роль журналов аудита в Exchange Online для включения поиска журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-p106">You can use the Security &amp; Compliance Center or PowerShell to turn on audit log search in Office 365. It might take several hours after you turn on audit log search before you can return results when you search the audit log. You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="f2dd5-126">Использование безопасности &amp; центре соответствия требованиям для включения поиска журнала аудита</span><span class="sxs-lookup"><span data-stu-id="f2dd5-126">Use the Security &amp; Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="f2dd5-127">В разделе Безопасность &amp; центре соответствия требованиям, чтобы перейти на **поиска &amp; расследования** \> **поиска журнала аудита**.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-127">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="f2dd5-128">Нажмите кнопку **Начать запись пользователя и действия администратора**.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Выберите элемент "Начать запись действий пользователей и администраторов", чтобы включить аудит](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="f2dd5-130">Диалоговое окно о том, что пользователь и действия администратора в вашей организации будет записанные в журнал аудита Office 365 и доступны для просмотра в отчете.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="f2dd5-131">Нажмите кнопку **Включить**.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="f2dd5-132">Отображается сообщение, рекомендующее подготовлено журнала аудита и что можно выполнить поиск в нескольких часов после завершения подготовки.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="f2dd5-133">Включение поиска журнала аудита с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="f2dd5-133">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="f2dd5-134">Подключение к PowerShell Exchange Online</span><span class="sxs-lookup"><span data-stu-id="f2dd5-134">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="f2dd5-135">Выполните следующую команду PowerShell для включения поиска журнала аудита в Office 365.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="f2dd5-136">Сообщение о том, что может занять более 60 минут, чтобы изменения вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="f2dd5-137">Отключить поиск журнала аудита</span><span class="sxs-lookup"><span data-stu-id="f2dd5-137">Turn off audit log search</span></span>

<span data-ttu-id="f2dd5-p107">Необходимо использовать удаленную консоль PowerShell, подключенных к организации Exchange Online для отключения поиска журнала аудита. Как и для включения поиска журнала аудита, необходимо назначить роль журналов аудита в Exchange Online отключить поиск в журнале аудита.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-p107">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search. Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="f2dd5-140">Подключение к PowerShell Exchange Online</span><span class="sxs-lookup"><span data-stu-id="f2dd5-140">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="f2dd5-141">Выполните следующую команду PowerShell, чтобы отключить поиск в журнале аудита в Office 365.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="f2dd5-p108">После while убедитесь, что поиск журнала аудита выключен (отключено). Существует два способа сделать это:</span><span class="sxs-lookup"><span data-stu-id="f2dd5-p108">After a while, verify that audit log search is turned off (disabled). There are two ways to do this:</span></span>
    
    - <span data-ttu-id="f2dd5-144">В PowerShell выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="f2dd5-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="f2dd5-145">Значение `False` для _UnifiedAuditLogIngestionEnabled_ свойство указывает, что поиск журнала аудита отключена.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="f2dd5-146">В разделе Безопасность &amp; центре соответствия требованиям, чтобы перейти на **поиска &amp; расследования** \> **поиска журнала аудита**и нажмите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-146">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="f2dd5-147">Сообщение о том, что поиск журнала аудита не включено.</span><span class="sxs-lookup"><span data-stu-id="f2dd5-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![Сообщение является dispayed, если аудит отключен](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
