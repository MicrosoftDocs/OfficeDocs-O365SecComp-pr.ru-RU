---
title: Политики доступа в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Политики доступа к облачным приложениям Office 365 обеспечивают мониторинг и контроль доступа к облачным приложениям в режиме реального времени на основе пользователя, расположения, устройства и приложения. Вы можете создавать политики доступа для любого устройства, включая устройства, не присоединенные к домену, а не управлять Windows Intune, выполнив развертывание клиентских сертификатов на управляемые устройства или используя существующие сертификаты, такие как сторонние сертификаты MDM. Например, вы можете развернуть клиентские сертификаты на управляемых устройствах, а затем блокировать доступ к устройствам без сертификата.
ms.openlocfilehash: bb4404793647c65ab8addc148e6efe24242f3079
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103314"
---
# <a name="access-policies-in-office-365-cloud-app-security"></a><span data-ttu-id="72bff-105">Политики доступа в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="72bff-105">Access policies in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="72bff-106">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="72bff-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="72bff-107">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="72bff-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="72bff-108">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="72bff-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="72bff-109">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="72bff-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="72bff-110">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="72bff-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="72bff-111">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="72bff-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="72bff-112">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="72bff-112">You are here!</span></span>  <br/> [<span data-ttu-id="72bff-113">Следующее действие</span><span class="sxs-lookup"><span data-stu-id="72bff-113">Next step</span></span>](group-your-ip-addresses-in-ocas.md) <br/> |[<span data-ttu-id="72bff-114">Начало использования</span><span class="sxs-lookup"><span data-stu-id="72bff-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="72bff-p102">Политики доступа к облачным приложениям Office 365 обеспечивают мониторинг и контроль доступа к облачным приложениям в режиме реального времени на основе пользователя, расположения, устройства и приложения. Вы можете создавать политики доступа для любого устройства, включая устройства, не присоединенные к домену, а не управлять Windows Intune, выполнив развертывание клиентских сертификатов на управляемые устройства или используя существующие сертификаты, такие как сторонние сертификаты MDM. Например, вы можете развернуть клиентские сертификаты на управляемых устройствах, а затем блокировать доступ к устройствам без сертификата.</span><span class="sxs-lookup"><span data-stu-id="72bff-p102">Office 365 Cloud App Security access policies enable real-time monitoring and control over access to cloud apps based on user, location, device, and app. You can create access policies for any device, including devices that aren't domain joined, and not managed by Windows Intune by rolling out client certificates to managed devices or by using existing certificates, such as third-party MDM certificates. For example, you can deploy client certificates to managed devices, and then block access from devices without a certificate.</span></span>

<span data-ttu-id="72bff-118">Вместо того чтобы разрешать или блокировать доступ полностью [](ocas-session-policies.md) , с политиками сеансов вы можете разрешить доступ при наблюдении за сеансом и/или ограничения определенных действий сеансов.</span><span class="sxs-lookup"><span data-stu-id="72bff-118">Instead of allowing or blocking access completely, with [session policies](ocas-session-policies.md) you can allow access while monitoring the session and/or limit specific session activities.</span></span>

## <a name="prerequisites-to-using-access-policies"></a><span data-ttu-id="72bff-119">Предварительные требования для использования политик доступа</span><span class="sxs-lookup"><span data-stu-id="72bff-119">Prerequisites to using access policies</span></span>

- <span data-ttu-id="72bff-120">Лицензия Azure AD Premium P1</span><span class="sxs-lookup"><span data-stu-id="72bff-120">Azure AD Premium P1 license</span></span>

- <span data-ttu-id="72bff-121">Подходящие приложения следует [развертывать с помощью элемента управления приложением условНого доступа](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)</span><span class="sxs-lookup"><span data-stu-id="72bff-121">The relevant apps should be [deployed with Conditional Access App Control](https://docs.microsoft.com/en-us/cloud-app-security/proxy-deployment-aad)</span></span>

- <span data-ttu-id="72bff-122">должна быть указана  [политика условного доступа Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal), которая перенаправляет пользователей на Office 365 Cloud App Security, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="72bff-122">An [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) should be in place that redirects users to Office 365 Cloud App Security, as described below.</span></span>

## <a name="create-an-azure-ad-conditional-access-policy"></a><span data-ttu-id="72bff-123">Создание политики условного доступа Azure AD</span><span class="sxs-lookup"><span data-stu-id="72bff-123">Create an Azure AD conditional access policy</span></span>

<span data-ttu-id="72bff-p103">Политики условного доступа Azure Active Directory и политики сеанса безопасности Cloud App действуют в сочетании для изучения каждого сеанса пользователя и принятия решений по политике для каждого приложения. Чтобы настроить политику условного доступа в Azure AD, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="72bff-p103">Azure Active Directory conditional access policies and Cloud App Security session policies work in tandem to examine each user session and make policy decisions for each app. To set up a conditional access policy in Azure AD, follow this procedure:</span></span>

1. <span data-ttu-id="72bff-126">Настройка  [политики условного доступа Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)с назначениями для пользователя или группы пользователей и приложения, которым необходимо управлять с помощью элемента управления приложением условного доступа.</span><span class="sxs-lookup"><span data-stu-id="72bff-126">Configure an [Azure AD conditional access policy](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal) with assignments for user or group of users and the app you want to control with Conditional Access App Control.</span></span><br><span data-ttu-id="72bff-127">Note: Эта политика влияет только на приложения, развернутые [с помощью элемента управления](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad) "условный доступ".</span><span class="sxs-lookup"><span data-stu-id="72bff-127">NOTE: Only apps that were [deployed with Conditional Access App Control](https://docs.microsoft.com/cloud-app-security/proxy-deployment-aad) will be affected by this policy.</span></span>

2. <span data-ttu-id="72bff-128">направьте пользователей на Office 365 Cloud app Security, установив флажок **использовать управление приложениями условного доступа** , принудительно заданное ограничения в разделе **сеанс**.</span><span class="sxs-lookup"><span data-stu-id="72bff-128">Route users to Office 365 Cloud App Security by selecting the **Use Conditional Access App Control enforced restrictions** under **Session**.</span></span>

## <a name="create-a-cloud-app-security-access-policy"></a><span data-ttu-id="72bff-129">Создание политики доступа к Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="72bff-129">Create a Cloud App Security access policy</span></span>

<span data-ttu-id="72bff-130">Чтобы создать новую политику доступа, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="72bff-130">To create a new access policy, follow this procedure:</span></span>

1. <span data-ttu-id="72bff-131">На портале выберите **элемент Управление** , а затем **политики**.</span><span class="sxs-lookup"><span data-stu-id="72bff-131">In the portal, select **Control** followed by **Policies**.</span></span>

2. <span data-ttu-id="72bff-132">На странице " **политики** " щелкните **создать политику** и выберите **Политика доступа**.</span><span class="sxs-lookup"><span data-stu-id="72bff-132">In the **Policies** page, click **Create policy** and select **Access policy**.</span></span>

3. <span data-ttu-id="72bff-133">В окне **Политика** доступа назначьте имя политики, например *блокировать доступ с неуправляемых устройств*.</span><span class="sxs-lookup"><span data-stu-id="72bff-133">In the **Access policy** window, assign a name for your policy, such as *Block access from unmanaged devices*.</span></span>

4. <span data-ttu-id="72bff-p104">В разделе **действия, которые соответствуют всем следующим** разделам, в разделе **Источник действия**выберите дополнительные фильтры активности, которые необходимо применить к политике. Фильтры включают следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="72bff-p104">In the **Activities matching all of the following** section, Under **Activity source**, select additional activity filters to apply to the policy. Filters include the following options:</span></span>
    
    - <span data-ttu-id="72bff-136">**Теги устройств**: Используйте этот фильтр для определения неуправляемых устройств.</span><span class="sxs-lookup"><span data-stu-id="72bff-136">**Device tags**: Use this filter to identify unmanaged devices.</span></span>
    
    - <span data-ttu-id="72bff-137">**Расположение**: Используйте этот фильтр для определения неизвестных (и, следовательно) расположений.</span><span class="sxs-lookup"><span data-stu-id="72bff-137">**Location**: Use this filter to identify unknown (and therefore risky) locations.</span></span>
    
    - <span data-ttu-id="72bff-138">**IP-адрес**: Используйте этот фильтр для ФИЛЬТРАЦИИ по IP-адресам или использования ранее назначенных тегов IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="72bff-138">**IP address**: Use this filter to filter per IP addresses or use previously assigned IP address tags.</span></span>
    
    - <span data-ttu-id="72bff-p105">**Тег агента пользователя**: Используйте этот фильтр, чтобы включить эвристику для определения приложений для мобильных устройств и настольных ПК. Этот фильтр может иметь значение равно или не равно. Значения необходимо протестировать для мобильных и настольных приложений для каждого облачного приложения.</span><span class="sxs-lookup"><span data-stu-id="72bff-p105">**User agent tag**: Use this filter to enable the heuristic to identify mobile and desktop apps. This filter can be set to equals or does not equal. The values should be tested against your mobile and desktop apps for each cloud app.</span></span>

5. <span data-ttu-id="72bff-142">В разделе **действия**выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="72bff-142">Under **Actions**, select one of the following options:</span></span>
    
    - <span data-ttu-id="72bff-143">**Разрешить**: установите для этого действия явно разрешение доступа в соответствии с заданными фильтрами политики.</span><span class="sxs-lookup"><span data-stu-id="72bff-143">**Allow**: Set this action to explicitly allow access according to the policy filters you set.</span></span>
    
    - <span data-ttu-id="72bff-144">**Блокировать**: установите для этого действия явный блокирование доступа в соответствии с заданными фильтрами политики.</span><span class="sxs-lookup"><span data-stu-id="72bff-144">**Block**: Set this action to explicitly block access according to the policy filters you set.</span></span>

6. <span data-ttu-id="72bff-145">Вы можете **создать оповещение для каждого сопоставленного события с уровнем серьезности политики** и задать лимит оповещений и выбрать, следует ли оповещать как сообщение электронной почты, текстовое сообщение или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="72bff-145">You can **Create an alert for each matching event with the policy's severity** and set an alert limit and select whether you want the alert as an email, a text message or both.</span></span>

## <a name="next-steps"></a><span data-ttu-id="72bff-146">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="72bff-146">Next steps</span></span>

- [<span data-ttu-id="72bff-147">Группирование IP-адресов для упрощения управления в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="72bff-147">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)