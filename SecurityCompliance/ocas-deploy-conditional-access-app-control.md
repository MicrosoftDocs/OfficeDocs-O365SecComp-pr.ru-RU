---
title: Развертывание приложения условного доступа для приложений Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: o365-administration
localization_priority: Normal
description: Выполните следующие действия, чтобы настроить приложения Azure AD Office 365 для управления приложением Office 365 Cloud App Security.
ms.openlocfilehash: ba3980615815fa45b1385a67560cc635506e2c22
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2019
ms.locfileid: "30103294"
---
# <a name="deploy-conditional-access-app-control-for-office-365-apps"></a><span data-ttu-id="2fe61-103">Развертывание приложения условного доступа для приложений Office 365</span><span class="sxs-lookup"><span data-stu-id="2fe61-103">Deploy Conditional Access App Control for Office 365 apps</span></span>

|<span data-ttu-id="2fe61-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="2fe61-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="2fe61-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="2fe61-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="2fe61-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="2fe61-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="2fe61-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="2fe61-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="2fe61-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="2fe61-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="2fe61-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="2fe61-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="2fe61-110">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="2fe61-110">You are here!</span></span>  <br/> [<span data-ttu-id="2fe61-111">Следующее действие</span><span class="sxs-lookup"><span data-stu-id="2fe61-111">Next step</span></span>](ocas-session-policies.md) <br/> |[<span data-ttu-id="2fe61-112">Начало использования</span><span class="sxs-lookup"><span data-stu-id="2fe61-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="2fe61-113">Выполните следующие действия, чтобы настроить приложения Azure AD Office 365 для управления приложением Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="2fe61-113">Follow these steps to configure Azure AD Office 365 apps to be controlled by Office 365 Cloud App Security Conditional Access App Control.</span></span>

<span data-ttu-id="2fe61-114">**Шаг 1: [Создание политики тестирования для условного доступа Azure AD](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span><span class="sxs-lookup"><span data-stu-id="2fe61-114">**Step 1: [Create an Azure AD conditional access test policy](#step-1-create-an-azure-ad-conditional-access-test-policy)**</span></span>

<span data-ttu-id="2fe61-115">**Шаг 2: [Вход с использованием области пользователя для политики в приложениях](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span><span class="sxs-lookup"><span data-stu-id="2fe61-115">**Step 2: [Sign in with a user scoped to the policy in the apps](#step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps)**</span></span>

<span data-ttu-id="2fe61-116">**Шаг 3: Если вы не выбрали встроенную политику безопасности облачных приложений в Azure AD или хотите применить эту политику к нерекомендуемому приложению, [Настройте дополнительные элементы управления на портале Cloud App Security](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal) .**</span><span class="sxs-lookup"><span data-stu-id="2fe61-116">**Step 3: If you did not select a built-in Cloud App Security policy in Azure AD or if you want to apply the policy to a non-featured app, [Configure advanced controls in the Cloud App Security portal](#step-3-configure-advanced-controls-in-the-cloud-app-security-portal)**</span></span>

<span data-ttu-id="2fe61-117">**Шаг 4: [Тестирование развертывания](#step-4-test-the-deployment)**</span><span class="sxs-lookup"><span data-stu-id="2fe61-117">**Step 4: [Test the deployment](#step-4-test-the-deployment)**</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fe61-118">чтобы развернуть элемент управления приложением для условного доступа для приложений Office 365, необходима действительная [лицензия на Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) и лицензия на Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="2fe61-118">To deploy Conditional Access App Control for Office 365 apps, you need a valid [license for Azure AD Premium P1](https://docs.microsoft.com/azure/active-directory/license-users-groups) as well as a Office 365 Cloud App Security license.</span></span>

## <a name="step-1-create-an-azure-ad-conditional-access-test-policy"></a><span data-ttu-id="2fe61-119">Шаг 1: Создание политики тестирования для условного доступа Azure AD</span><span class="sxs-lookup"><span data-stu-id="2fe61-119">Step 1: Create an Azure AD conditional access test policy</span></span> 

1. <span data-ttu-id="2fe61-120">В разделе **Безопасность**Azure Active Directory выберите пункт условный **доступ**.</span><span class="sxs-lookup"><span data-stu-id="2fe61-120">In Azure Active Directory, under **Security**, click on **Conditional access**.</span></span>

2. <span data-ttu-id="2fe61-121">Нажмите кнопку **создать политику** и создайте новую политику.</span><span class="sxs-lookup"><span data-stu-id="2fe61-121">Click **New policy** and create a new policy.</span></span>

3. <span data-ttu-id="2fe61-122">В политике тестирования в разделе **Пользователи**назначьте тестового пользователя или пользователя, которые можно использовать для начального входа и проверки.</span><span class="sxs-lookup"><span data-stu-id="2fe61-122">In the TEST policy, under **Users**, assign a test user or user that can be used for an initial sign-on and verification.</span></span>

4. <span data-ttu-id="2fe61-123">В разделе ТЕСТовая политика в разделе **Cloud App**назначьте приложения, которые вы хотите контролировать с помощью элемента управления приложением условного доступа.</span><span class="sxs-lookup"><span data-stu-id="2fe61-123">In the TEST policy, under **Cloud app**, assign the apps you want to control with Conditional Access App Control.</span></span>

5. <span data-ttu-id="2fe61-p101">В разделе **сеанс**настройте политику для использования любой из встроенных политик, **мониторинга** или **блокировки загрузки**. Или выберите **использовать настраиваемую политику** , чтобы задать расширенную политику на портале Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="2fe61-p101">Under **Session**, set the policy to use either of the built-in policies, **Monitor only** or **Block downloads**. Or select **Use custom policy** to set an advanced policy in the Cloud App Security portal.</span></span>

6. <span data-ttu-id="2fe61-126">Добавьте все необходимые **назначения** условий или **Предоставьте элементы управления** (необязательно).</span><span class="sxs-lookup"><span data-stu-id="2fe61-126">Add any applicable **Condition assignments** or **Grant controls** (optional).</span></span>

> ![Условный доступ к Azure AD](media/image1.png)

## <a name="step-2-sign-in-with-a-user-scoped-to-the-policy-in-the-apps"></a><span data-ttu-id="2fe61-128">Шаг 2: вход с использованием области пользователя для политики в приложениях</span><span class="sxs-lookup"><span data-stu-id="2fe61-128">Step 2: Sign in with a user scoped to the policy in the apps</span></span> 

<span data-ttu-id="2fe61-p102">После создания политики войдите в каждое приложение, настроенное в этой политике. Убедитесь, что входите в систему с использованием пользователя, настроенного в политике. Обязательно выйдите из существующих сеансов.</span><span class="sxs-lookup"><span data-stu-id="2fe61-p102">After you've created the policy, sign in to each app configured in that policy. Make sure you sign in using a user configured in the policy. Make sure to first sign out of existing sessions.</span></span>

<span data-ttu-id="2fe61-p103">Cloud App Security синхронизирует сведения политики с серверами для каждого нового приложения, в котором вы входите в систему. Это может занять до одной минуты.</span><span class="sxs-lookup"><span data-stu-id="2fe61-p103">Cloud App Security will sync your policy details to its servers for each new app you log in to. This may take up to one minute.</span></span>

## <a name="step-3-configure-advanced-controls-in-the-cloud-app-security-portal"></a><span data-ttu-id="2fe61-134">Шаг 3: Настройка дополнительных элементов управления на портале Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="2fe61-134">Step 3: Configure advanced controls in the Cloud App Security portal</span></span> 

<span data-ttu-id="2fe61-135">Приведенные выше инструкции помогли вам создать встроенную политику безопасности Cloud App для популярных приложений непосредственно в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2fe61-135">The instructions above helped you create a built-in Cloud App Security policy for featured apps directly in Azure AD.</span></span>

<span data-ttu-id="2fe61-136">чтобы настроить расширенную политику, создайте [политику](ocas-access-policies.md) доступа или [политику](ocas-session-policies.md) сеанса на портале Cloud App Security для Office 365.</span><span class="sxs-lookup"><span data-stu-id="2fe61-136">To configure an advanced policy, create an [access policy](ocas-access-policies.md) or a [session policy](ocas-session-policies.md) in the Office 365 Cloud App Security portal.</span></span>

### <a name="to-identify-devices-using-client-certificates-this-is-optional"></a><span data-ttu-id="2fe61-137">Для определения устройств с помощью клиентских сертификатов (необязательно):</span><span class="sxs-lookup"><span data-stu-id="2fe61-137">To identify devices using client certificates (this is optional):</span></span>

1. <span data-ttu-id="2fe61-138">Перейдите к разделу Параметры Ког и выберите пункт **Идентификация устройств**.</span><span class="sxs-lookup"><span data-stu-id="2fe61-138">Go to the settings cog and choose **Device identification**.</span></span>

2. <span data-ttu-id="2fe61-139">Загрузите один или несколько корневых или промежуточных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="2fe61-139">Upload one or more root or intermediate certificates.</span></span>

3. <span data-ttu-id="2fe61-140">После отправки сертификата вы можете создавать политики доступа и политики сеансов на основе **тега устройства** и **действительного сертификата клиента**.</span><span class="sxs-lookup"><span data-stu-id="2fe61-140">After the certificate is uploaded, you can create access policies and session policies based on **Device tag** and **Valid client certificate**.</span></span>

![ИДЕНТИФИКАТОР устройства управления приложениями условного доступа](media/image2.png)

> [!NOTE]
> <span data-ttu-id="2fe61-142">Сертификат запрашивается у пользователя только в том случае, если сеанс соответствует политике, использующей действительный фильтр сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="2fe61-142">A certificate is only requested from a user if the session matches a policy that uses the valid client certificate filter.</span></span>
> 
## <a name="step-4-test-the-deployment"></a><span data-ttu-id="2fe61-143">Шаг 4: тестирование развертывания</span><span class="sxs-lookup"><span data-stu-id="2fe61-143">Step 4: Test the deployment</span></span> 

1. <span data-ttu-id="2fe61-p104">Сначала выйдите из всех существующих сеансов. Затем попробуйте войти в каждое приложение, которое было успешно развернуто. Выполните вход, используя пользователя, который соответствует политике, настроенной в Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2fe61-p104">First sign out of any existing sessions. Then, try to sign in to each app that was successfully deployed. Sign in using a user that matches the policy configured in Azure AD.</span></span>

2. <span data-ttu-id="2fe61-147">На портале Cloud App Security разверните в разделе **исследование**, выберите **Журнал активности**и убедитесь, что действия входа для каждого приложения захвачены.</span><span class="sxs-lookup"><span data-stu-id="2fe61-147">In the Cloud App Security portal, under **Investigate**, select **Activity log**, and make sure the login activities are captured for each app.</span></span>

3. <span data-ttu-id="2fe61-148">Можно выполнить фильтрацию, нажав кнопку **Дополнительно**, а затем отменив фильтрацию с помощью **элемента управления доступом источника Equals**.</span><span class="sxs-lookup"><span data-stu-id="2fe61-148">You can filter by clicking on **Advanced**, and then filtering using **Source equals Access control**.</span></span>

4. <span data-ttu-id="2fe61-p105">Рекомендуется подписываться на мобильные и настольные приложения с управляемых и неуправляемых устройств. Это необходимо для того, чтобы убедиться, что действия правильно записаны в журнале активности. Чтобы убедиться в том, что действие захвачено правильно, щелкните журнал единого входа, чтобы открыть ящик активности. Убедитесь, что **тег агента пользователя**правильно указывает, является ли устройство собственным клиентом (то есть мобильным или классическим), либо устройство является управляемым устройством (соответствующим требованиям, присоединенным доменом или действительным сертификатом клиента).</span><span class="sxs-lookup"><span data-stu-id="2fe61-p105">It's recommended that you sign into mobile and desktop apps from managed and unmanaged devices. This is to make sure that the activities are properly captured in the activity log. To verify that the activity is properly captured, click on a single sign-on log on activity so that it opens the activity drawer. Make sure the **User agent tag** properly reflects whether the device is a native client (meaning either a mobile or desktop app) or the device is a managed device (compliant, domain joined, or valid client certificate).</span></span>

> [!NOTE]
> <span data-ttu-id="2fe61-p106">После развертывания приложение невозможно удалить на странице "Управление приложениями условного доступа". Пока вы не настроили политику сеанса или доступа к приложению, элемент управления "условный доступ" не изменит поведение приложения.</span><span class="sxs-lookup"><span data-stu-id="2fe61-p106">After it is deployed, you can't remove an app from the Conditional Access App Control page. As long as you don't set a session or access policy on the app, the Conditional Access App Control won't change any behavior for the app.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2fe61-155">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="2fe61-155">Next steps</span></span>

- [<span data-ttu-id="2fe61-156">Сведения о политиках сеансов в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="2fe61-156">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="2fe61-157">Сведения о политиках доступа в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="2fe61-157">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 

- [<span data-ttu-id="2fe61-158">Группирование IP-адресов для упрощения управления в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="2fe61-158">Group your IP addresses to simplify management in Office 365 Cloud App Security</span></span>](group-your-ip-addresses-in-ocas.md)