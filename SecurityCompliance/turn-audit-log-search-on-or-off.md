---
title: Включение и отключение поиска в журнале аудита Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Вы можете включить функцию поиска журнала аудита в центре безопасности _Амп_ соответствия требованиям. Если вы передумали, вы можете включить его в любое время. Если поиск в журнале аудита отключен, администраторы не могут выполнять поиск действий пользователей и администраторов в журнале аудита Office 365 в Организации.
ms.openlocfilehash: a77114ac9b5de18d4718a543983f7a1f94ebc41f
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000932"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a><span data-ttu-id="a7dd8-105">Включение и отключение поиска в журнале аудита Office 365</span><span class="sxs-lookup"><span data-stu-id="a7dd8-105">Turn Office 365 audit log search on or off</span></span>

<span data-ttu-id="a7dd8-106">Перед началом поиска в журнале аудита Office 365 вы (или другой администратор) должны включить ведение журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-106">You (or another admin) must turn on audit logging before you can start searching the Office 365 audit log.</span></span> <span data-ttu-id="a7dd8-107">Когда включен Поиск в журнале аудита в центре безопасности _Амп_ соответствие требованиям, действия пользователей и администраторов из вашей организации записываются в журнал аудита и хранятся в течение 90 дней.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-107">When audit log search in the Security & Compliance Center is turned on, user and admin activity from your organization is recorded in the audit log and retained for 90 days.</span></span> <span data-ttu-id="a7dd8-108">Тем не менее, Организация может не зафиксировать и сохранить данные журнала аудита.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-108">However, your organization might not want to record and retain audit log data.</span></span> <span data-ttu-id="a7dd8-109">Кроме того, для доступа к данным аудита можно использовать сторонние сведения о безопасности и приложение управления событиями (SIEM).</span><span class="sxs-lookup"><span data-stu-id="a7dd8-109">Or you might be using a third-party security information and event management (SIEM) application to access your auditing data.</span></span> <span data-ttu-id="a7dd8-110">В таких случаях глобальный администратор может отключить поиск в журнале аудита в Office 365.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-110">In those cases, a global admin can turn off audit log search in Office 365.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="a7dd8-111">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="a7dd8-111">Before you begin</span></span>

- <span data-ttu-id="a7dd8-112">Роль журналов аудита в Exchange Online должна быть назначена для включения или отключения поиска журнала аудита в организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-112">You have to be assigned the Audit Logs role in Exchange Online to turn audit log search on or off in your Office 365 organization.</span></span> <span data-ttu-id="a7dd8-113">По умолчанию эта роль назначается группам ролей "Управление соответствием требованиям" и "Управление организацией" на странице " **разрешения** " в центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-113">By default, this role is assigned to the Compliance Management and Organization Management role groups on the **Permissions** page in the Exchange admin center.</span></span> <span data-ttu-id="a7dd8-114">Глобальные администраторы в Office 365 являются участниками группы ролей Управление организацией в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-114">Global admins in Office 365 are members of the Organization Management role group in Exchange Online.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="a7dd8-115">Пользователям необходимо назначить разрешения в Exchange Online, чтобы включить или отключить поиск в журнале аудита.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-115">Users have to be assigned permissions in Exchange Online to turn audit log search on or off.</span></span> <span data-ttu-id="a7dd8-116">Если вы назначили пользователям роль "журналы аудита" на странице " **разрешения** " в центре безопасности _амп_, они не смогут включать или отключать поиск в журнале аудита.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-116">If you assign users the Audit Logs role on the **Permissions** page in the Security & Compliance Center, they won't be able to turn audit log search on or off.</span></span> <span data-ttu-id="a7dd8-117">Это вызвано тем, что базовый командлет является командлетом Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-117">This is because the underlying cmdlet is an Exchange Online cmdlet.</span></span> 
  
- <span data-ttu-id="a7dd8-118">Если вы отключите Поиск журнала аудита в Office 365, вы по-прежнему можете использовать API действий управления Office 365 для доступа к данным аудита в Организации.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-118">If you turn off audit log search in Office 365, you can still use the Office 365 Management Activity API to access auditing data for your organization.</span></span> <span data-ttu-id="a7dd8-119">Отключение поиска в журнале аудита в соответствии с инструкциями, описанными в этой статье, означает, что при поиске в журнале аудита с помощью центра безопасности _Амп_ соответствия требованиям или при запуске командлета **Search-UnifiedAuditLog** в Exchange Online не будет возвращено никаких результатов. Типов.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-119">Turning off audit log search by following the steps in this article means that no results will be returned when you search the audit log using the Security & Compliance Center or when you run the **Search-UnifiedAuditLog** cmdlet in Exchange Online PowerShell.</span></span> <span data-ttu-id="a7dd8-120">Тем не менее, если вы уполномочены любому приложению получать доступ к данным аудита вашей организации с помощью API действий управления Office 365, эти приложения продолжат работать.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-120">However, if you've authorized any application to access your organization's auditing data via the Office 365 Management Activity API , those applications will continue to work.</span></span> 
    
- <span data-ttu-id="a7dd8-121">Пошаговые инструкции по поиску в журнале аудита Office 365 можно узнать в статье [Поиск в журнале аудита в центре безопасности _Амп_ соответствие требованиям](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="a7dd8-121">For step-by-step instructions on searching the Office 365 audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
    
## <a name="turn-on-audit-log-search"></a><span data-ttu-id="a7dd8-122">Включение поиска в журнале аудита</span><span class="sxs-lookup"><span data-stu-id="a7dd8-122">Turn on audit log search</span></span>

<span data-ttu-id="a7dd8-123">Для включения поиска журнала аудита в Office 365 можно использовать центр обеспечения безопасности _Амп_ или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-123">You can use the Security & Compliance Center or PowerShell to turn on audit log search in Office 365.</span></span> <span data-ttu-id="a7dd8-124">После включения поиска в журнале аудита может потребоваться несколько часов, прежде чем вы сможете вернуть результаты при поиске в журнале аудита.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-124">It might take several hours after you turn on audit log search before you can return results when you search the audit log.</span></span> <span data-ttu-id="a7dd8-125">Чтобы включить поиск журнала аудита, необходимо назначить роль журналов аудита в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-125">You have to be assigned the Audit Logs role in Exchange Online to turn on audit log search.</span></span>
  
### <a name="use-the-security--compliance-center-to-turn-on-audit-log-search"></a><span data-ttu-id="a7dd8-126">Использование центра соответствия требованиям безопасности _Амп_ для включения поиска в журнале аудита</span><span class="sxs-lookup"><span data-stu-id="a7dd8-126">Use the Security & Compliance Center to turn on audit log search</span></span>

1. <span data-ttu-id="a7dd8-127">В центре безопасности _амп_ соответствия требованиям выберите Поиск в \*\*\*\* \> **журнале аудита**поиска.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-127">In the Security & Compliance Center, go to **Search** \> **Audit log search**.</span></span>
    
2. <span data-ttu-id="a7dd8-128">Нажмите кнопку **начать запись действий пользователей и администраторов**.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-128">Click **Start recording user and admin activities**.</span></span>
    
    ![Нажмите кнопку начать запись действий пользователей и администраторов, чтобы включить аудит](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    <span data-ttu-id="a7dd8-130">Отображается диалоговое окно с сообщением о том, что действия пользователя и администратора в вашей организации будут записаны в журнал аудита Office 365 и доступны для просмотра в отчете.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-130">A dialog box is displayed saying that user and admin activity in your organization will be recorded to the Office 365 audit log and available to view in a report.</span></span> 
    
3. <span data-ttu-id="a7dd8-131">Нажмите кнопку **Включить**.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-131">Click **Turn on**.</span></span>
    
    <span data-ttu-id="a7dd8-132">Отобразится сообщение с сообщением о том, что журнал аудита готов и вы можете выполнить поиск в течение нескольких часов после завершения подготовки.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-132">A message is displayed that says the audit log is being prepared and that you can run a search in a couple of hours after the preparation is complete.</span></span>
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a><span data-ttu-id="a7dd8-133">Включение поиска в журнале аудита с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="a7dd8-133">Use PowerShell to turn on audit log search</span></span>

1. [<span data-ttu-id="a7dd8-134">Подключение к PowerShell Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a7dd8-134">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="a7dd8-135">Выполните следующую команду PowerShell, чтобы включить поиск журнала аудита в Office 365.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-135">Run the following PowerShell command to turn on audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    <span data-ttu-id="a7dd8-136">Отображается сообщение о том, что изменение вступит в силу до 60 минут.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-136">A message is displayed saying that it might take up to 60 minutes for the change to take effect.</span></span>
  
## <a name="turn-off-audit-log-search"></a><span data-ttu-id="a7dd8-137">Отключение поиска в журнале аудита</span><span class="sxs-lookup"><span data-stu-id="a7dd8-137">Turn off audit log search</span></span>

<span data-ttu-id="a7dd8-138">Чтобы отключить поиск в журнале аудита, необходимо использовать удаленную оболочку PowerShell, подключенную к организации Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-138">You have to use remote PowerShell connected to your Exchange Online organization to turn off audit log search.</span></span> <span data-ttu-id="a7dd8-139">Аналогично включению поиска в журнале аудита необходимо назначить роль журналов аудита в Exchange Online, чтобы отключить поиск в журнале аудита.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-139">Similar to turning on audit log search, you have to be assigned the Audit Logs role in Exchange Online to turn off audit log search.</span></span>
  
1. [<span data-ttu-id="a7dd8-140">Подключение к PowerShell Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a7dd8-140">Connect to Exchange Online PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=396554)
    
2. <span data-ttu-id="a7dd8-141">Выполните следующую команду PowerShell, чтобы отключить поиск в журнале аудита в Office 365.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-141">Run the following PowerShell command to turn off audit log search in Office 365.</span></span>
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. <span data-ttu-id="a7dd8-142">Через некоторое время убедитесь, что поиск в журнале аудита отключен (отключен).</span><span class="sxs-lookup"><span data-stu-id="a7dd8-142">After a while, verify that audit log search is turned off (disabled).</span></span> <span data-ttu-id="a7dd8-143">Это можно сделать двумя способами:</span><span class="sxs-lookup"><span data-stu-id="a7dd8-143">There are two ways to do this:</span></span>
    
    - <span data-ttu-id="a7dd8-144">В PowerShell выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a7dd8-144">In PowerShell, run the following command:</span></span>

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        <span data-ttu-id="a7dd8-145">Значение `False` свойства _унифиедаудитлогинжестионенаблед_ указывает на то, что поиск журнала аудита отключен.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-145">The value of  `False` for the  _UnifiedAuditLogIngestionEnabled_ property indicates that audit log search is turned off.</span></span> 
    
    - <span data-ttu-id="a7dd8-146">В центре безопасности _амп_ соответствие выберите Поиск в **журнале аудита** **поиска** \> и нажмите кнопку **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-146">In the Security & Compliance Center, go to **Search** \> **Audit log search**, and then click **Search**.</span></span>
    
      <span data-ttu-id="a7dd8-147">Отображается сообщение о том, что поиск по журналу аудита не включен.</span><span class="sxs-lookup"><span data-stu-id="a7dd8-147">A message is displayed saying that audit log search isn't turned on.</span></span> 
    
      ![При отключенном аудите отображается сообщение](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
