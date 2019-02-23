---
title: Создание сертификата APNs для устройств с iOS
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Для управления устройствами iOS, такими как iPad и iPhone, в управлении мобильными устройствами для Office 365, выполните следующие действия, чтобы создать сертификат APNs.
ms.openlocfilehash: 5f82690f0add5f1aae95a089d9cdfc0b320ae596
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220459"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="51bcf-103">Создание сертификата APNs для устройств с iOS</span><span class="sxs-lookup"><span data-stu-id="51bcf-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="51bcf-104">Для управления устройствами iOS, такими как iPad и iPhone, в управлении мобильными устройствами для Office 365, необходимо создать сертификат APNs.</span><span class="sxs-lookup"><span data-stu-id="51bcf-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="51bcf-p101">Для этого выполните действия, описанные в разделе **Настройка** ссылки на странице портала. (Перейдите в **раздел &amp; Security Security Security Center** \> Security **Policies** \> **Management** \> **Settings Управление параметрами**.)</span><span class="sxs-lookup"><span data-stu-id="51bcf-p101">To do this, follow the steps from the **Set up** link on the portal page. (Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Настройка необходимых действий для управления мобильными устройствами и рекомендации](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="51bcf-108">Далее, чтобы **настроить сертификат APNs для устройств с iOS**, нажмите кнопку **настроить**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="51bcf-109">Выберите **загрузить файл CSR** и сохранить запрос подписи сертификата в любом месте на вашем компьютере, который вы забудете запомнить.</span><span class="sxs-lookup"><span data-stu-id="51bcf-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Диалоговое окно установки сертификата точки доступа](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="51bcf-111">Нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="51bcf-112">Создайте сертификат APN.</span><span class="sxs-lookup"><span data-stu-id="51bcf-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="51bcf-113">Выберите **портал Apple APNs** , чтобы открыть портал Apple Push Certificate.</span><span class="sxs-lookup"><span data-stu-id="51bcf-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Диалоговое окно установки сертификата уведомления об APN с выбранным порталом Apple APNS](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="51bcf-115">Выполните вход с помощью идентификатора Apple ID.</span><span class="sxs-lookup"><span data-stu-id="51bcf-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="51bcf-p102">Используйте идентификатор Apple ID, связанный с учетной записью электронной почты, которая останется в вашей организации, даже если пользователь, управляющий учетной записью, не покидает ее. Сохраните этот идентификатор, так как вам потребуется использовать тот же идентификатор при продлении сертификата.</span><span class="sxs-lookup"><span data-stu-id="51bcf-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="51bcf-118">Выберите **создать сертификат** и принять **условия использования**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="51bcf-119">**Перейдите** к запросу подписи сертификата, загруженному на компьютер, из Office 365 и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="51bcf-120">**Скачайте** сертификат APN, созданный порталом сертификатов Apple Push на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="51bcf-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="51bcf-121">Если у вас возникли проблемы с загрузкой сертификата, обновите браузер.</span><span class="sxs-lookup"><span data-stu-id="51bcf-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="51bcf-122">Вернитесь в Office 365 и нажмите кнопку **Далее** , чтобы перейти на страницу **отправить сертификат APNs** .</span><span class="sxs-lookup"><span data-stu-id="51bcf-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="51bcf-123">Перейдите к сертификату APN, скачанному с портала Push-сертификатов Apple.</span><span class="sxs-lookup"><span data-stu-id="51bcf-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Нажмите кнопку "Обзор", чтобы выбрать сертификат APNS, загруженный с Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="51bcf-125">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="51bcf-125">Select **Finish**.</span></span>
    
<span data-ttu-id="51bcf-126">Вернитесь к \> **политикам** \> безопасности **центра соответствия требованиям &amp; безопасности** **Управление** \> устройствами **Управление параметрами** для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="51bcf-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

