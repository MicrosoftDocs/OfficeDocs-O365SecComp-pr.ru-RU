---
title: Поиск в журнале аудита для действия пользователя и администратора в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: 'Журнал аудита Office 365 — это журнала объединенных аудита. Почему журнал объединенных аудита? Так как события из большинство служб Office 365, с которым вы организации подписывается на данные записываются в журнал аудита единого, можно выполнить поиск. Это означает, что можно выполнить поиск пользователей и действия администратора в следующих служб:'
ms.openlocfilehash: 230502f331babeef8f89eacce0d19a7756cb96fc
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038032"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="188f8-106">Поиск в журнале аудита для действия пользователя и администратора в Office 365</span><span class="sxs-lookup"><span data-stu-id="188f8-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="188f8-p102">Журнал аудита Office 365 — это журнала объединенных аудита. Почему журнал объединенных аудита? Так как события из большинство служб Office 365, с которым вы организации подписывается на данные записываются в журнал аудита единого, можно выполнить поиск. Это означает, что можно выполнить поиск пользователей и действия администратора в следующих служб:</span><span class="sxs-lookup"><span data-stu-id="188f8-p102">The Office 365 audit log is a unified audit log. Why a unified audit log? Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search. That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="188f8-111">SharePoint;</span><span class="sxs-lookup"><span data-stu-id="188f8-111">SharePoint</span></span>
- <span data-ttu-id="188f8-112">OneDrive;</span><span class="sxs-lookup"><span data-stu-id="188f8-112">OneDrive</span></span>
- <span data-ttu-id="188f8-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="188f8-113">Exchange</span></span>
- <span data-ttu-id="188f8-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="188f8-114">Azure Active Directory</span></span>
- <span data-ttu-id="188f8-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="188f8-115">Microsoft Teams</span></span>
- <span data-ttu-id="188f8-116">Обнаружение электронных данных</span><span class="sxs-lookup"><span data-stu-id="188f8-116">eDiscovery</span></span>
- <span data-ttu-id="188f8-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="188f8-117">Power BI</span></span>
- <span data-ttu-id="188f8-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="188f8-118">Yammer</span></span>
- <span data-ttu-id="188f8-119">Sway</span><span class="sxs-lookup"><span data-stu-id="188f8-119">Sway</span></span>
- <span data-ttu-id="188f8-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="188f8-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="188f8-121">Настройка аудита</span><span class="sxs-lookup"><span data-stu-id="188f8-121">Set up auditing</span></span>
  
<span data-ttu-id="188f8-122">Есть несколько вещей, которые необходимо выполнить перед можно выполнить поиск в Office 365 журнал аудита.</span><span class="sxs-lookup"><span data-stu-id="188f8-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="188f8-123">[Включение поиска журнала аудита](turn-audit-log-search-on-or-off.md) , чтобы начать запись событий, которые можно выполнить поиск</span><span class="sxs-lookup"><span data-stu-id="188f8-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="188f8-124">[Включение аудита почтовых ящиков](enable-mailbox-auditing.md) , можно выполнить поиск события, связанные с почтовых ящиков; Например, когда пользователь входит в свои почтового ящика или удаляет элементы из папки элементов для восстановления</span><span class="sxs-lookup"><span data-stu-id="188f8-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="188f8-125">Поиск в журнале аудита</span><span class="sxs-lookup"><span data-stu-id="188f8-125">Search the audit log</span></span>
  
<span data-ttu-id="188f8-126">После включения аудита, поиск сотни отдельных типов событий из нескольких служб Office 365.</span><span class="sxs-lookup"><span data-stu-id="188f8-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="188f8-127">[Поиск журнала аудита](search-the-audit-log-in-security-and-compliance.md) для пользователя и администратора действий</span><span class="sxs-lookup"><span data-stu-id="188f8-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="188f8-128">[Изучить подробные свойства](detailed-properties-in-the-office-365-audit-log.md) в каждой записи аудита, включенные в результатах поиска</span><span class="sxs-lookup"><span data-stu-id="188f8-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="188f8-129">[Поиск действий, связанных с обнаружения электронных данных](search-for-ediscovery-activities-in-the-audit-log.md) с помощью руководители "Администраторы" и обеспечения соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="188f8-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
