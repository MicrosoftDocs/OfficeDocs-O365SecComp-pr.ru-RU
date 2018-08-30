---
title: Создайте сертификат APN для устройств операций ввода-вывода
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 8/5/2016
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_APNCertMDM
- O365E_APNCertMDM
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 522b43f4-a2ff-46f6-962a-dd4f47e546a7
description: Для управления iOS устройств iPad и iPhones в управлении мобильных устройств для Office 365, выполните следующие действия, чтобы создать новый сертификат APN.
ms.openlocfilehash: 28e8888d7dd57c3052cdcb5994725f11a5f0445f
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272054"
---
# <a name="create-an-apns-certificate-for-ios-devices"></a><span data-ttu-id="5593c-103">Создайте сертификат APN для устройств операций ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="5593c-103">Create an APNs Certificate for iOS devices</span></span>

 <span data-ttu-id="5593c-104">Для управления iOS устройств iPad и iPhones в управлении мобильных устройств для Office 365 необходимо создать новый сертификат APN.</span><span class="sxs-lookup"><span data-stu-id="5593c-104">To manage iOS devices like iPad and iPhones in Mobile Device Management for Office 365 you must create an APNs certificate.</span></span> 
  
<span data-ttu-id="5593c-p101">Чтобы сделать это, следуйте указаниям по ссылке **настроить** на странице портала. (Перейдите к **безопасности &amp; центре соответствия требованиям** \> **политики безопасности** \> **Управление устройствами** \> **Управление параметрами**.)</span><span class="sxs-lookup"><span data-stu-id="5593c-p101">To do this, follow the steps from the **Set up** link on the portal page. (Go to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings**.)</span></span>
  
![Настройка мобильного устройства управления обязательные и рекомендуемые действия](media/d71e3c76-b6b9-4549-ade6-cbfab846d908.png)
  
1. <span data-ttu-id="5593c-108">**Настройка сертификата APN для устройств операций ввода-вывода**выберите **Настройка**.</span><span class="sxs-lookup"><span data-stu-id="5593c-108">Next to **Configure a APNs Certificate for iOS devices**, select **Set up**.</span></span>
    
2. <span data-ttu-id="5593c-109">Выберите **загрузить файл CSR** и в другое место для сохранения запроса подписи сертификата на компьютере, который необходимо передать.</span><span class="sxs-lookup"><span data-stu-id="5593c-109">Select **Download your CSR file** and save the Certificate signing request to a somewhere on your computer that you'll remember.</span></span> 
    
    ![Установка сертификата APN диалоговое окно ""](media/03aa8a24-e95c-4077-9b6b-ef76a86bafd7.png)
  
3. <span data-ttu-id="5593c-111">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5593c-111">Select **Next**.</span></span>
    
4. <span data-ttu-id="5593c-112">Создайте сертификат APN.</span><span class="sxs-lookup"><span data-stu-id="5593c-112">Create an APN certificate.</span></span>
    
  - <span data-ttu-id="5593c-113">Выберите **Apple APNS портала** для открытия портале Apple Push-сертификаты.</span><span class="sxs-lookup"><span data-stu-id="5593c-113">Select **Apple APNS Portal** to open the Apple Push Certificates Portal.</span></span> 
    
    ![Установка диалоговое окно сертификата APN уведомление с выбрано портала APNS Apple](media/ce19f53c-f44a-470b-baf3-9278dfda2ba5.png)
  
  - <span data-ttu-id="5593c-115">Вход с помощью идентификатора Apple.</span><span class="sxs-lookup"><span data-stu-id="5593c-115">Sign in with an Apple ID.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="5593c-p102">Используйте компании Apple идентификатор, связанное с учетной записью электронной почты, который будет оставаться с организацией, даже в том случае, если пользователь, который управляет учетной записи оставляет. Сохраните этот код, так как вам потребуется использовать тот же идентификатор, если время для обновления сертификата.</span><span class="sxs-lookup"><span data-stu-id="5593c-p102">Use a company Apple ID associated with an email account that will remain with your organization even if the user who manages the account leaves. Save this ID because you'll need to use the same ID when it's time to renew the certificate.</span></span> 
  
  - <span data-ttu-id="5593c-118">Выберите команду **создать сертификат** и примите **Условия использования**.</span><span class="sxs-lookup"><span data-stu-id="5593c-118">Select **Create a Certificate** and accept the **Terms of Use**.</span></span>
    
  - <span data-ttu-id="5593c-119">**Обзор** запрос подписи сертификата был загружен на компьютер с Office 365 и выберите **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="5593c-119">**Browse** to the Certificate signing request you downloaded to your computer from Office 365 and select **Upload**.</span></span>
    
  - <span data-ttu-id="5593c-120">**Загрузите** сертификат APN, созданных Apple Push-сертификат портала на своем компьютере.</span><span class="sxs-lookup"><span data-stu-id="5593c-120">**Download** the APN certificate created by the Apple Push Certificate Portal to your computer.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="5593c-121">Если у вас возникли проблемы при загрузке сертификата, обновите окно обозревателя.</span><span class="sxs-lookup"><span data-stu-id="5593c-121">If you're having trouble downloading the certificate, refresh your browser.</span></span> 
  
5. <span data-ttu-id="5593c-122">Вернитесь в Office 365 и нажмите кнопку **Далее** для перехода к странице **APNS Загрузка сертификата** .</span><span class="sxs-lookup"><span data-stu-id="5593c-122">Go back to Office 365 and select **Next** to get to the **Upload APNS certificate** page.</span></span> 
    
6. <span data-ttu-id="5593c-123">Перейдите к APN сертификат, который был загружен из портала Apple Push-сертификаты.</span><span class="sxs-lookup"><span data-stu-id="5593c-123">Browse to the APN certificate you downloaded from the Apple Push Certificates Portal.</span></span>
    
    ![Нажмите кнопку Обзор, чтобы выбрать сертификат APNS, загруженные из Apple](media/afe2849d-af23-4c55-9009-d8f25edaf6c0.png)
  
7. <span data-ttu-id="5593c-125">Нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="5593c-125">Select **Finish**.</span></span>
    
<span data-ttu-id="5593c-126">Вернуться к **безопасности &amp; центре соответствия требованиям** \> **политики безопасности** \> **Управление устройствами** \> **Управление параметрами** , чтобы завершить настройку.</span><span class="sxs-lookup"><span data-stu-id="5593c-126">Go back to **Security &amp; Compliance Center** \> **Security policies** \> **Device management** \> **Manage settings** to complete setup.</span></span> 
  

