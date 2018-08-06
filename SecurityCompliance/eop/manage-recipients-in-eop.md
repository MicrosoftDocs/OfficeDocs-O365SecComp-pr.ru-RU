---
title: Управление получателями в EOP
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 2921f544-8257-4bae-8e3a-ce9250e9f162
description: Microsoft Exchange Online Protection (EOP) предлагает несколько способов управления получателями электронной почты. Как администратор вы можете выполнять определенные задачи управления в Центре администрирования Exchange или с помощью удаленного Windows PowerShell и проверять другие задачи управления, выполняемые в Центре администрирования Microsoft Office 365.
ms.openlocfilehash: 0159604eaa4e021d9ccef544306e8b274af11f18
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027576"
---
# <a name="manage-recipients-in-eop"></a><span data-ttu-id="6c92c-104">Управление получателями в EOP</span><span class="sxs-lookup"><span data-stu-id="6c92c-104">Manage recipients in EOP</span></span>

<span data-ttu-id="6c92c-p102">Microsoft Exchange Online Protection (EOP) предлагает несколько способов управления получателями электронной почты. Как администратор вы можете выполнять определенные задачи управления в Центре администрирования Exchange или с помощью удаленного Windows PowerShell и проверять другие задачи управления, выполняемые в Центре администрирования Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="6c92c-p102">Microsoft Exchange Online Protection (EOP) offers several ways to manage your mail recipients. As an administrator, you can perform certain management tasks within the Exchange admin center (EAC) or using remote Windows PowerShell, and verify other management tasks performed in the Microsoft Office 365 admin center.</span></span>
  
<span data-ttu-id="6c92c-107">EOP поддерживает приведенные ниже типы получателей.</span><span class="sxs-lookup"><span data-stu-id="6c92c-107">EOP supports the following types of recipients:</span></span>
  
- <span data-ttu-id="6c92c-p103">**Пользователи почты** Пользователи почты — это список получателей в вашей EOP управляемых доменов. Эти получателей иметь учетные данные для входа в своей организации Office 365, но они имеют адреса электронной почты внешним, что означает, что их почтовые ящики получателей расположены за пределами вашей организации в облако. Можно добавить пользователей почты, чтобы иметь возможность принимать почту и можно также создать правила транспорта для определенных пользователей. Можно также назначить роли пользователей почты в вашей организации; Пользователи с правами группы ролей управления можно доступа к центру администрирования Exchange (EAC) и выполнять определенные задачи управления. Дополнительные сведения о ролях пользователей и назначение ролей пользователей в службе EOP видеть [Управление разрешениями группы ролей администратора в EOP](manage-admin-role-group-permissions-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="6c92c-p103">**Mail Users** Mail users are recipients in your EOP managed domains. These recipients have logon credentials in your Office 365 organization, but they have external email addresses, meaning that their recipient mailboxes are located outside of your cloud organization. You can add mail users so that they can receive mail and you can also create transport rules for specific users. You can also assign roles to mail users in your organization; users with management role group privileges can access the Exchange admin center (EAC) and perform certain management tasks. To learn more about user roles and how to assign user roles in EOP, see [Manage admin role group permissions in EOP](manage-admin-role-group-permissions-in-eop.md).</span></span>
    
    <span data-ttu-id="6c92c-113">Дополнительные сведения об управлении почтовыми пользователями в EOP см. в разделе [Управление почтовыми пользователями в EOP](manage-mail-users-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="6c92c-113">For more information about managing mail users in EOP, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>
    
- <span data-ttu-id="6c92c-114">**Группы**. Почтовых пользователей можно объединять в группы рассылки или группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6c92c-114">**Groups** Mail users can be grouped together into distribution groups or security groups.</span></span> 
    
    <span data-ttu-id="6c92c-115">Дополнительные сведения об управлении группами в EOP см. в разделе [Управление группами в EOP](manage-groups-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="6c92c-115">For more information about managing groups in EOP, see [Manage groups in EOP](manage-groups-in-eop.md).</span></span>
    
<span data-ttu-id="6c92c-p104">Хотите узнать, какая версия Exchange Online описана в этом разделе? См. раздел [Recipients in Exchange Online](http://technet.microsoft.com/library/50d16941-5cd7-435d-8715-e2b69f8410ab.aspx).</span><span class="sxs-lookup"><span data-stu-id="6c92c-p104">Looking for the Exchange Online version of this topic? See [Recipients in Exchange Online](http://technet.microsoft.com/library/50d16941-5cd7-435d-8715-e2b69f8410ab.aspx).</span></span>
  
<span data-ttu-id="6c92c-p105">Необходима версия данного раздела для Exchange Server? См. раздел [Recipients](http://technet.microsoft.com/library/40300ed4-85a5-463d-bb3a-cf787bd44e9d.aspx).</span><span class="sxs-lookup"><span data-stu-id="6c92c-p105">Looking for the Exchange Server version of this topic? See [Recipients](http://technet.microsoft.com/library/40300ed4-85a5-463d-bb3a-cf787bd44e9d.aspx).</span></span>
  

