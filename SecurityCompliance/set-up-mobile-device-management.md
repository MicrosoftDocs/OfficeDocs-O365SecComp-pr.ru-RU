---
title: Задайте копирование Mobile Device Management (MDM) в Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_OverviewMDM
- 'O365E_OverviewMDM '
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: dd892318-bc44-4eb1-af00-9db5430be3cd
description: Встроенные управление устройствами Mobile для Office 365 помогает защитить и управлять ими пользователей мобильных устройств, например iPhones, iPad, Androids, и телефоны Windows. Чтобы начать работу, выполните следующие действия для активации и настройка управления мобильных устройств для Office 365.
ms.openlocfilehash: c92290170b2937067e7407787282eaaa368b25b7
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272364"
---
# <a name="set-up-mobile-device-management-mdm-in-office-365"></a><span data-ttu-id="c9f1b-104">Задайте копирование Mobile Device Management (MDM) в Office 365</span><span class="sxs-lookup"><span data-stu-id="c9f1b-104">Set up Mobile Device Management (MDM) in Office 365</span></span>

<span data-ttu-id="c9f1b-p102">Встроенные Mobile Device Management (MDM) для Office 365 помогает защитить и управлять ими пользователей мобильных устройств, например iPhones, iPad, Androids, и телефоны Windows. Можно создать и управлять политики безопасности устройств, удаленно стирание устройства и просматривать отчеты подробные устройства.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p102">The built-in Mobile Device Management (MDM) for Office 365 helps you secure and manage your users' mobile devices like iPhones, iPads, Androids, and Windows phones. You can create and manage device security policies, remotely wipe a device, and view detailed device reports.</span></span>
  
<span data-ttu-id="c9f1b-p103">Есть вопросы? Мы собрали [вопросы и ответы для распространенные вопросы](frequently-asked-questions-about-mdm.md). Помните, что нельзя использовать [партнеров: предложение делегированного администрирования](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) для управления мобильного устройства управления для Office 365.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p103">Have questions? We've put together [a FAQ to help address common questions](frequently-asked-questions-about-mdm.md). Be aware that you cannot use a [Partners: Offer delegated administration](https://support.office.com/article/26530dc0-ebba-415b-86b1-b55bc06b073e) to manage Mobile Device Management for Office 365.</span></span> 
  
<span data-ttu-id="c9f1b-110">Управление устройствами является частью безопасности &amp; центре соответствия требованиям, поэтому необходимо перейти по ссылке для запуска программы установки MDM.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-110">Device management is part of the Security &amp; Compliance Center so you'll need to go there to kick off MDM setup.</span></span>
  
<span data-ttu-id="c9f1b-111">Для настройки мобильного устройства управления для Office 365 вам потребуется:</span><span class="sxs-lookup"><span data-stu-id="c9f1b-111">To set up Mobile Device Management for Office 365 you'll need to:</span></span>
  
1. [<span data-ttu-id="c9f1b-112">Активация службы управления мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="c9f1b-112">Activate the Mobile Device Management service</span></span>](#activate-the-mobile-device-management-service)  
2. [<span data-ttu-id="c9f1b-113">Настройка управления мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="c9f1b-113">Set up Mobile Device Management</span></span>](#set-up-mobile-device-management)
3. [<span data-ttu-id="c9f1b-114">Убедитесь, что пользователи зарегистрируйте свои устройства</span><span class="sxs-lookup"><span data-stu-id="c9f1b-114">Make sure users enroll their devices</span></span>](#step-4-recommended-manage-device-security-policies)
  
## <a name="activate-the-mobile-device-management-service"></a><span data-ttu-id="c9f1b-115">Активация службы управления мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="c9f1b-115">Activate the Mobile Device Management service</span></span>

1. <span data-ttu-id="c9f1b-116">Войдите в Office 365 с помощью рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-116">Sign in to Office 365 with your work or school account.</span></span> 
    
2. <span data-ttu-id="c9f1b-117">Последовательно выберите пункты [безопасности &amp; центре соответствия требованиям](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="c9f1b-117">Go to [Security &amp; Compliance Center](https://protection.office.com).</span></span>
    
3. <span data-ttu-id="c9f1b-118">Выберите пункты **Защита от потери данных** \> **Управление устройствами** и выберите **давайте начнем** с началом процесса активации.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-118">Navigate to **Data loss prevention** \> **Device management** and click **Let's get started** to kick off the activation process.</span></span> 
    
    ![Настройка мобильного устройства управления для Office 365](media/368e1026-9aa5-431b-a722-8f7cf528f263.png)
  
4. <span data-ttu-id="c9f1b-p104">Мы создали политика безопасности по умолчанию, которые помогут приступить к работе. Обновите имя политики безопасности на этой странице и нажмите кнопку **Запуск программы установки**.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p104">We created a default security policy for you to help you get started. Update the name of the security policy on this page, and then click **Start setup**.</span></span>
    
    ![Установка политики безопасности мобильных устройств Management](media/5619a2d1-f900-4268-9050-5d7eb57429a5.png)
  
5. <span data-ttu-id="c9f1b-123">Появится экран программы установки, которая показывает ход выполнения по настройке службы.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-123">You'll see the setup screen that shows progress on setting up the service.</span></span>
    
    ![Ход выполнения установки MDM](media/db45d1bb-d247-4ac0-9deb-1b0c1ace9bfa.png)
  
> [!TIP]
> <span data-ttu-id="c9f1b-p105">Можно также найти **Программы установки MDM** посредством поиска. В центре администрирования Office 365 \> **Главная** страница, управление мобильными устройствами тип в поле « **Поиск** ». > ![Поиска для управление мобильными устройствами в центре администрирования](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p105">You can also locate **MDM Setup** through Search. In the Office 365 admin center \> **Home** page, type mobile device management in the **Search** box. > ![Search for mobile device management in the admin center](media/cd0ebf15-ef79-4eaa-ab5b-041ac0bd4e5b.png)</span></span>
  
<span data-ttu-id="c9f1b-128">Может потребоваться некоторое время для активации управления мобильных устройств для Office 365, но после завершения работы, вы получите сообщение электронной почты, описывающий последующих действий.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-128">It can take some time to activate Mobile Device Management for Office 365, but when it finishes, you'll receive an email that explains the next steps to take.</span></span>
  
## <a name="set-up-mobile-device-management"></a><span data-ttu-id="c9f1b-129">Настройка управления мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="c9f1b-129">Set up Mobile Device Management</span></span>

<span data-ttu-id="c9f1b-p106">Если служба готова, выполните следующие четыре действия для завершения работы программы установки. Выберите [Управление параметрами](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) на странице **Управление устройствами** в безопасности может потребоваться &amp; центре соответствия требованиям, чтобы просмотреть следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p106">When the service is ready, complete the following four steps to finish setup. You may need to click [Manage settings](https://portal.office.com/EAdmin/Device/IntuneInventory.aspx) on the **Device management** page in the Security &amp; Compliance Center to see the following settings.</span></span> 
  
![Настройка мобильного устройства управления обязательные и рекомендуемые действия](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
### <a name="step-1-required-configure-domains-for-mdm"></a><span data-ttu-id="c9f1b-133">Шаг 1: (Обязательный) Настройка доменов для MDM</span><span class="sxs-lookup"><span data-stu-id="c9f1b-133">Step 1: (Required) Configure domains for MDM</span></span>

<span data-ttu-id="c9f1b-p107">Если у вас нет настраиваемого домена, связанного с Office 365 или если вы не управляете устройств Windows, можно пропустить этот раздел. В противном случае вам потребуются для добавления записей DNS для домена на сервере DNS. Если вы добавили записи уже, как часть настройки домена в Office 365, все установлен. После добавления записи Office 365 пользователи в вашей организации, зарегистрированные на свои устройства Windows с адресом электронной почты, использующий настраиваемый домен перенаправляются для регистрации в MDM для Office 365.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p107">If you don't have a custom domain associated with Office 365 or if you're not managing Windows devices, you can skip this section. Otherwise, you'll need to add DNS records for the domain at your DNS host. If you've added the records already, as part of setting up your domain with Office 365, you're all set. After you add the records, Office 365 users in your organization who sign in on their Windows device with an email address that uses your custom domain are redirected to enroll in MDM for Office 365.</span></span>
  
<span data-ttu-id="c9f1b-p108">Требуется помощь при установке записи? Найдите вашего регистратора доменных имен в списке, доступном в [статье Создание записей DNS для Office 365 при самостоятельном управлении записями DNS-записей](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) и выберите имя регистратора, перейдите к пошаговых инструкций по созданию записей DNS. Используйте эти инструкции для добавления следующие две записи:</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p108">Need help setting up the records? Find your domain registrar in the list provided in [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23) and select the registrar name to go to step-by-step help for creating DNS records. Use those instructions to add the following two records:</span></span> 
  
|<span data-ttu-id="c9f1b-141">**Имя узла**</span><span class="sxs-lookup"><span data-stu-id="c9f1b-141">**Host name**</span></span>|<span data-ttu-id="c9f1b-142">**Тип записи**</span><span class="sxs-lookup"><span data-stu-id="c9f1b-142">**Record type**</span></span>|<span data-ttu-id="c9f1b-143">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="c9f1b-143">**Address**</span></span>|<span data-ttu-id="c9f1b-144">**TTL**</span><span class="sxs-lookup"><span data-stu-id="c9f1b-144">**TTL**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c9f1b-145">EnterpriseEnrollment</span><span class="sxs-lookup"><span data-stu-id="c9f1b-145">EnterpriseEnrollment</span></span>  <br/> |<span data-ttu-id="c9f1b-146">CNAME</span><span class="sxs-lookup"><span data-stu-id="c9f1b-146">CNAME</span></span>  <br/> |<span data-ttu-id="c9f1b-147">EnterpriseEnrollment.manage.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="c9f1b-147">EnterpriseEnrollment.manage.microsoft.com</span></span>  <br/> |<span data-ttu-id="c9f1b-148">3600</span><span class="sxs-lookup"><span data-stu-id="c9f1b-148">3600</span></span>  <br/> |
|<span data-ttu-id="c9f1b-149">EnterpriseRegistration</span><span class="sxs-lookup"><span data-stu-id="c9f1b-149">EnterpriseRegistration</span></span>  <br/> |<span data-ttu-id="c9f1b-150">CNAME</span><span class="sxs-lookup"><span data-stu-id="c9f1b-150">CNAME</span></span>  <br/> |<span data-ttu-id="c9f1b-151">EnterpriseRegistration.windows.net</span><span class="sxs-lookup"><span data-stu-id="c9f1b-151">EnterpriseRegistration.windows.net</span></span>  <br/> |<span data-ttu-id="c9f1b-152">3600</span><span class="sxs-lookup"><span data-stu-id="c9f1b-152">3600</span></span>  <br/> |
   
<span data-ttu-id="c9f1b-153">После добавления двух записей, вернитесь на безопасность &amp; центре соответствия требованиям и перейдите к **разделу Управление устройства** \> **Управление параметрами** для выполнения к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-153">After you add the two records, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-2-required-configure-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="c9f1b-154">Шаг 2: (Обязательный) Настройка сертификат APN для устройства iOS</span><span class="sxs-lookup"><span data-stu-id="c9f1b-154">Step 2: (Required) Configure an APNs Certificate for iOS devices</span></span>

<span data-ttu-id="c9f1b-155">Для управления iOS устройств iPad и iPhones, необходимо создать новый сертификат APN.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-155">To manage iOS devices like iPad and iPhones, you need to create an APNs certificate.</span></span>
  
<span data-ttu-id="c9f1b-156">Для этого выполните действия из ссылки **Set up** на **Setup страницы Управление мобильного устройства**.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-156">To do this, follow the steps from the **Set up** links on the **Setup mobile device management page**.</span></span>
  
1. <span data-ttu-id="c9f1b-157">**Настройка сертификата APN для устройств операций ввода-вывода**выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-157">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="c9f1b-158">Выберите **загрузить файл CSR** и в другое место для сохранения запроса подписи сертификата на компьютере, который необходимо передать.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-158">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Установка сертификата APN диалоговое окно ""](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="c9f1b-160">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-160">Select **Next**.</span></span>
    
4. <span data-ttu-id="c9f1b-161">Создайте сертификат APN.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-161">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="c9f1b-162">Выберите **Apple APNS портала** для открытия портале Apple Push-сертификаты.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-162">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Установка диалоговое окно сертификата APN уведомление с выбрано портала APNS Apple](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="c9f1b-164">Вход с помощью идентификатора Apple.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-164">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="c9f1b-p109">Используйте компании Apple идентификатор, связанное с учетной записью электронной почты, который будет оставаться с организацией, даже в том случае, если пользователь, который управляет учетной записи оставляет. Сохраните этот код, так как вам потребуется использовать тот же идентификатор, если время для обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p109">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="c9f1b-167">Выберите команду **создать сертификат** и примите **Условия использования**.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-167">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="c9f1b-168">**Обзор** запрос подписи сертификата был загружен на компьютер с Office 365 и выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-168">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="c9f1b-169">**Загрузите** сертификат APN, созданных Apple Push-сертификат портала на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-169">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="c9f1b-170">Если у вас возникли проблемы при загрузке сертификата, обновите окно обозревателя.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-170">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="c9f1b-171">Вернитесь в Office 365 и нажмите кнопку **Далее** для перехода к странице **APNS Загрузка сертификата** .</span><span class="sxs-lookup"><span data-stu-id="c9f1b-171">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="c9f1b-172">Перейдите к APN сертификат, который был загружен из портала Apple Push-сертификаты.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-172">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Нажмите кнопку Обзор, чтобы выбрать сертификат APNS, загруженные из Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="c9f1b-174">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-174">Select **Finish**.</span></span>
    
<span data-ttu-id="c9f1b-175">После добавления сертификата APN вернуться к безопасности &amp; центре соответствия требованиям и перейдите к **разделу Управление устройства** \> **Управление параметрами** для выполнения к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-175">After you add APN Certificate, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-3-recommended-set-up-multi-factor-authentication"></a><span data-ttu-id="c9f1b-176">Шаг 3: (Рекомендуемый вариант) Настройка многофакторной проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="c9f1b-176">Step 3: (Recommended) Set up multi-factor authentication</span></span>

<span data-ttu-id="c9f1b-p110">Если многофакторная проверка подлинности (многофакторной проверкой Подлинности) в разделе **Рекомендуемые действия**не отображается, можно пропустить этот раздел. Если этот параметр указан, мы рекомендуем включить многофакторной проверкой Подлинности на портале Azure AD для повышения безопасности управления мобильного устройства для процесса регистрации Office 365. По умолчанию он отключен.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p110">If you don't see multi-factor authentication (MFA) under **Recommended steps**, you can skip this section. If this option is listed, we recommend you turn on MFA in the Azure AD portal to increase the security of the Mobile Device Management for Office 365 enrollment process. It is turned off by default.</span></span>
  
<span data-ttu-id="c9f1b-p111">Многофакторной проверкой Подлинности позволяет обеспечить безопасность входа в Office 365 для подачи заявок на мобильном устройстве, требуя вторую форму проверки подлинности. Пользователи не требуется для подтверждения телефонный звонок, текстовое сообщение или уведомление приложения на мобильное устройство после правильно ввода пароля учетной записи их работы. Они могут зарегистрировать свое устройство только после завершения этой второй способ проверки подлинности. После устройствах пользователей участвуют в управлении мобильных устройств для Office 365, пользователи могут обращаться к ресурсов Office 365 с только что своей учетной записи рабочего.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p111">MFA helps secure the sign in to Office 365 for mobile device enrollment by requiring a second form of authentication. Users are required to acknowledge a phone call, text message, or app notification on their mobile device after correctly entering their work account password. They can only enroll their device after this second form of authentication is completed. After users' devices are enrolled in Mobile Device Management for Office 365, users can access Office 365 resources with just their work account.</span></span>
  
<span data-ttu-id="c9f1b-p112">**Настройка многофакторной проверки подлинности**выберите **Настройка**. В этой статье описывается включение многофакторной проверкой Подлинности на портале Azure AD, см [многофакторной проверки подлинности](https://go.microsoft.com/fwlink/p/?LinkId=519255).</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p112">Next to **Set up multi-factor authentication**, select **Set up**. To learn how to turn on MFA in the Azure AD portal, see [Set up multi-factor authentication](https://go.microsoft.com/fwlink/p/?LinkId=519255).</span></span>
  
<span data-ttu-id="c9f1b-186">После настройки многофакторной проверкой Подлинности вернуться к безопасности &amp; центре соответствия требованиям и перейдите к **разделу Управление устройства** \> **Управление параметрами** для выполнения к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-186">After you set up MFA, go back to the Security &amp; Compliance Center and navigate to **Device management** \> **Manage settings** to complete the next step.</span></span> 
  
### <a name="step-4-recommended-manage-device-security-policies"></a><span data-ttu-id="c9f1b-187">Шаг 4: Политики безопасности устройств управление (рекомендуемый вариант)</span><span class="sxs-lookup"><span data-stu-id="c9f1b-187">Step 4: (Recommended) Manage device security policies</span></span>

<span data-ttu-id="c9f1b-p113">Следующим шагом является создание и развертывание политик безопасности устройств для защиты данных организации Office 365. Например, может помочь предотвратить потерю данных, если пользователь теряет свои устройства путем создания политики для блокировки устройств через 5 минут бездействия и устройств очистить после 3 отказов.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p113">The next step is to create and deploy device security policies to help protect your Office 365 organization's data. For example, you can help prevent data loss if a user loses their device by creating a policy to lock devices after 5 minutes of inactivity and have devices wiped after 3 sign-in failures.</span></span>
  
<span data-ttu-id="c9f1b-190">В **безопасности &amp; центре соответствия требованиям**, последовательно выберите пункты **политики безопасности** \> **политики безопасности устройств** для создания политики безопасности устройств и правил доступа.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-190">In the **Security &amp; Compliance Center**, go to **Security policies** \> **Device security policies** to create device security policies and access rules.</span></span> 
  
![Добавление политики безопасности устройств](media/69a027f5-fbfb-482a-b850-9ccb280b8c62.png)
  
<span data-ttu-id="c9f1b-192">Пошаговые инструкции о том, как создать новую политику, в разделе [Создание и развертывание политик безопасности устройств](create-device-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="c9f1b-192">For step by step instructions on how to create a new policy, see [Create and deploy device security policies](create-device-security-policies.md).</span></span>
  
> [!TIP]
>  <span data-ttu-id="c9f1b-p114">При создании новой политики можно настроить политику, чтобы разрешить нарушение политики доступа и отчет, где устройств пользователя не совместимый с политикой. Это позволяет видеть, сколько мобильных устройств может повлиять на работу политики без блокировки доступа к Office 365. > Перед развертыванием новой политики для всех пользователей в организации рекомендуется проверить на устройствах, используемых небольшого числа пользователей. > Кроме того перед развертыванием политик позволяют организации знать последствиях регистрации устройства в MDM для Office 365. В зависимости от того, как настроить политики устройств, которые не соответствуют их (несовместимых устройств) может быть заблокирован доступ к Office 365. Non совместимые устройства также могут иметь установленные приложения, фотографии и другие личные сведения, которые зарегистрированных устройства, может быть удален, если Очистить устройство. Дополнительные сведения: [стирание мобильного устройства в Office 365](wipe-a-mobile-device.md).</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p114">When you create a new policy, you might want to set the policy to allow access and report policy violation where a user's device isn't compliant with the policy. This lets you see how many mobile devices would be impacted by the policy without blocking access to Office 365. >  Before you deploy a new policy to everyone in your organization, we recommend you test it on the devices used by a small number of users. >  Also, before you deploy policies, let your organization know the potential impacts of enrolling a device in MDM for Office 365. Depending on how you set up the policies, devices that don't comply with them (non-compliant devices) could be blocked from accessing Office 365. Non-compliant devices might also have apps installed, photos, and other personal information which, on an enrolled device, could be deleted if the device is wiped. More info: [Wipe a mobile device in Office 365](wipe-a-mobile-device.md).</span></span> 
  
## <a name="make-sure-users-enroll-their-devices"></a><span data-ttu-id="c9f1b-200">Убедитесь, что пользователи зарегистрируйте свои устройства</span><span class="sxs-lookup"><span data-stu-id="c9f1b-200">Make sure users enroll their devices</span></span>

<span data-ttu-id="c9f1b-p115">После создания и развертывания политики управления мобильных устройств каждого лицензированных пользователей Office 365 в вашей организации, к которому применяется политика устройства появляется сообщение регистрации следующем входе в Office 365 с мобильного устройства. Они должны выполнить действия регистрации и активации, прежде чем они могут получить доступ к электронной почты Office 365 и документы. В разделе [Регистрация мобильного устройства для работы или school](enroll-your-mobile-device.md).</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p115">After you've created and deployed a mobile device management policy, each licensed Office 365 user in your organization that the device policy applies to will receive an enrollment message the next time they sign into Office 365 from their mobile device. They must complete the enrollment and activation steps before they can access Office 365 email and documents. See [Enroll your mobile device for work or school](enroll-your-mobile-device.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c9f1b-p116">Если предпочтительный язык пользователя не поддерживается процессом подачи заявок, пользователи могут получать уведомления о регистрации и действия на мобильных устройствах на другом языке. Не все языки, поддерживаемые в Office 365 в настоящее время поддерживаются для процесса подачи заявок на мобильных устройствах.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-p116">If a user's preferred language isn't supported by the enrollment process, users may receive enrollment notification and steps on their mobile devices in another language. Not all languages supported in Office 365 are currently supported for the enrollment process on mobile devices.</span></span> 
  
<span data-ttu-id="c9f1b-206">Пользователи с мобильными устройствами Android или операций ввода-вывода требуется установить приложение портала компании в рамках процесса регистрации.</span><span class="sxs-lookup"><span data-stu-id="c9f1b-206">Users with Android or iOS devices are required to install the Company Portal app as part of the enrollment process.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="c9f1b-207">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c9f1b-207">Related Topics</span></span>

[<span data-ttu-id="c9f1b-208">Возможности управления для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="c9f1b-208">Capabilities of Mobile Device Management</span></span>](capabilities-of-mobile-device-management.md)
  
[<span data-ttu-id="c9f1b-209">Создание и развертывание политик безопасности устройств</span><span class="sxs-lookup"><span data-stu-id="c9f1b-209">Create and deploy device security policies</span></span>](create-device-security-policies.md)
  

