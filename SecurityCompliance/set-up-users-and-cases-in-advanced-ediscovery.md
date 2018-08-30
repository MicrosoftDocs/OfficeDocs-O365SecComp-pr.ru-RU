---
title: Настройка пользователей и дел в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 60ffd80b-4376-419d-b6e4-a72029b9907c
description: 'Узнайте, как настроить роли пользователей, создайте случаев и назначение пользователям вариантов в Office 365 расширенного обнаружения электронных данных.  '
ms.openlocfilehash: 49f76b415d86035cecafc19c23b36c413f7576e5
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535104"
---
# <a name="set-up-users-and-cases-in-office-365-advanced-ediscovery"></a><span data-ttu-id="6babd-103">Настройка пользователей и дел в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6babd-103">Set up users and cases in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="6babd-104">В этом разделе описывается настройка параметров пользователей и случаи для Office 365 расширенного обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="6babd-104">This topic describes how to set up users and cases for Office 365 Advanced eDiscovery.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6babd-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="6babd-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="6babd-107">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="6babd-107">Prerequisites</span></span>

<span data-ttu-id="6babd-108">Перед настройкой случаев и пользователей в расширенной eDiscovery, следующие является обязательным:</span><span class="sxs-lookup"><span data-stu-id="6babd-108">Before setting up cases and users in Advanced eDiscovery, the following is required:</span></span>
  
- <span data-ttu-id="6babd-p102">Для анализа данных с помощью расширенных eDiscovery, пользователя (custodian данные) должны быть назначены лицензии Office 365 E5 пользователя. Кроме того пользователи, имеющие лицензию на Office 365 E1 или E3 может быть назначен расширенной eDiscovery отдельная лицензия. Администраторы и контролеры, назначенных для случаев и использовать расширенные обнаружения электронных данных для анализа данных, не требуется лицензия на E5.</span><span class="sxs-lookup"><span data-stu-id="6babd-p102">To analyze a user's data using Advanced eDiscovery, the user (the custodian of the data) must be assigned an Office 365 E5 license. Alternatively, users with an Office 365 E1 or E3 license can be assigned an Advanced eDiscovery standalone license. Administrators and compliance officers who are assigned to cases and use Advanced eDiscovery to analyze data don't need an E5 license.</span></span> 
    
- <span data-ttu-id="6babd-p103">Необходимо быть участником группы обнаружения электронных данных диспетчера ролей безопасности Office 365 &amp; центре соответствия требованиям для создания обращению eDiscovery и добавления в него участников. Добавление себя в группу ролей диспетчер обнаружения электронных данных в безопасности &amp; центре соответствия требованиям, необходимо быть глобальным администратором в организации Office 365. Если вы не глобального администратора, вам придется попросить глобального администратора добавить вас в группу обнаружения электронных данных диспетчера ролей. Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="6babd-p103">You have to be a member of the eDiscovery Manager role group in the Office 365 Security &amp; Compliance Center to create an eDiscovery case and add members to it. To add yourself to the eDiscovery Manager role group in Security &amp; Compliance Center, you have to be a global administrator in your Office 365 organization. If you're not a global administrator, you 'll have to ask a global administrator to add you to the eDiscovery Manager role group. For more information, see:</span></span>
    
  - [<span data-ttu-id="6babd-116">Разрешения безопасности Office 365 &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="6babd-116">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
    
  - [<span data-ttu-id="6babd-117">Назначение разрешений обнаружения электронных данных в Office 365 безопасность &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="6babd-117">Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center</span></span>](assign-ediscovery-permissions.md)
    
## <a name="step-1-assign-users-ediscovery-permissions"></a><span data-ttu-id="6babd-118">Шаг 1: Разрешения пользователей обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="6babd-118">Step 1: Assign users eDiscovery permissions</span></span>

<span data-ttu-id="6babd-p104">Первый шаг состоит в назначении пользователям разрешения требования безопасности &amp; центру соответствия требованиям, чтобы их можно меня добавляется в качестве члена случая обнаружения электронных данных. После добавления пользователя как член дела в системы &amp; центре соответствия требованиям, они будут иметь доступ в случае расширенные обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="6babd-p104">The first step is to assign users the requirement permissions in the Security &amp; Compliance Center so that they can me added as a member of an eDiscovery case. After a user is added as a member of a case in the Security &amp; Compliance Center, they'll be able to access the case in Advanced eDiscovery.</span></span>
  
<span data-ttu-id="6babd-121">Чтобы назначить пользователю все необходимые разрешения, поэтому они могут быть добавлены как член случая обнаружения электронных данных, обратитесь к разделу шаг 1 в [вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span><span class="sxs-lookup"><span data-stu-id="6babd-121">To assign a user the necessary permissions so they can be added as a member of an eDiscovery case, see Step 1 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-1-assign-ediscovery-permissions-to-potential-case-members).</span></span>
  
## <a name="step-2-create-an-ediscovery-case-and-add-members"></a><span data-ttu-id="6babd-122">Шаг 2: Создание обращению eDiscovery и добавлять элементы</span><span class="sxs-lookup"><span data-stu-id="6babd-122">Step 2: Create an eDiscovery case and add members</span></span>

<span data-ttu-id="6babd-p105">Следующим шагом является создание новое обращение eDiscovery в системы &amp; центре соответствия требованиям и добавить участников. Члены варианта будет иметь доступ в случае расширенные обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="6babd-p105">The next step is to create a new eDiscovery case in the Security &amp; Compliance Center and add members. Members of the case will then be able to access the case in Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="6babd-125">Чтобы создать новое обращение eDiscovery, обратитесь к разделу шаг 2 в [вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям](ediscovery-cases.md#step-2-create-a-new-case).</span><span class="sxs-lookup"><span data-stu-id="6babd-125">To create a new eDiscovery case, see Step 2 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-2-create-a-new-case).</span></span>
    
2. <span data-ttu-id="6babd-126">Чтобы добавить участников к обращению eDiscovery, обратитесь к разделу шаг 3 в [вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям](ediscovery-cases.md#step-3-add-members-to-a-case)</span><span class="sxs-lookup"><span data-stu-id="6babd-126">To add members to an eDiscovery case, see Step 3 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-3-add-members-to-a-case)</span></span>
    
## <a name="step-3-go-a-case-in-advanced-ediscovery"></a><span data-ttu-id="6babd-127">Шаг 3: Выберите дела в расширенной обнаружения электронных данных</span><span class="sxs-lookup"><span data-stu-id="6babd-127">Step 3: Go a case in Advanced eDiscovery</span></span>

<span data-ttu-id="6babd-p106">После создания обращению eDiscovery и добавлять элементы вы (или любой участник регистр) можно получить доступ к соответствующий регистр в расширенной обнаружения электронных данных. Для доступа к дела в расширенной eDiscovery, видеть шаг 8 в [вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span><span class="sxs-lookup"><span data-stu-id="6babd-p106">After you create an eDiscovery case and add members, you (or any member of the case) can access the corresponding case in Advanced eDiscovery. To access a case in Advanced eDiscovery, see Step 8 in [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md#step-8-go-to-the-case-in-advanced-ediscovery).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6babd-130">См. также</span><span class="sxs-lookup"><span data-stu-id="6babd-130">See also</span></span>

[<span data-ttu-id="6babd-131">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6babd-131">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="6babd-132">Подготовка данных</span><span class="sxs-lookup"><span data-stu-id="6babd-132">Preparing data</span></span>](prepare-data-for-advanced-ediscovery.md)
  
[<span data-ttu-id="6babd-133">Роли пользователей и доступ</span><span class="sxs-lookup"><span data-stu-id="6babd-133">User roles and access</span></span>](user-roles-and-access-in-advanced-ediscovery.md)

