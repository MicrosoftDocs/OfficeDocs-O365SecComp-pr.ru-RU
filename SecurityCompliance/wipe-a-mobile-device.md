---
title: Стирание мобильного устройства в Office 365
ms.author: dianef
author: dianef77
manager: scotv
ms.date: 6/11/2018
ms.audience: Admin
ms.topic: get-started-article
f1_keywords:
- O365M_WipeDevice
- O365E_WipeDevice
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 9d727c7d-8b47-4499-bf24-d046b449214c
description: Выполнять Выборочный очистки для удаления только корпоративной информации или полный очистку, чтобы удалить все данные с мобильного устройства и восстановить параметры фабрики можно использовать управление встроенных мобильных устройств для Office 365.
ms.openlocfilehash: d3eb28575924ca3bb4a647ae9af2f96b55116a53
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272504"
---
# <a name="wipe-a-mobile-device-in-office-365"></a><span data-ttu-id="6211f-103">Стирание мобильного устройства в Office 365</span><span class="sxs-lookup"><span data-stu-id="6211f-103">Wipe a mobile device in Office 365</span></span>
  
<span data-ttu-id="6211f-104">Выполнять Выборочный очистки для удаления только корпоративной информации или полный очистку, чтобы удалить все данные с мобильного устройства и восстановить параметры фабрики можно использовать управление встроенных мобильных устройств для Office 365.</span><span class="sxs-lookup"><span data-stu-id="6211f-104">You can use built-in mobile device management for Office 365 to do a selective wipe to remove only organizational information, or a full wipe to delete all information from a mobile device and restore it to its factory settings.</span></span>
  
## <a name="what-to-know-before-you-begin"></a><span data-ttu-id="6211f-105">Что следует знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="6211f-105">What to know before you begin</span></span>

- <span data-ttu-id="6211f-p101">Мобильных устройств можно хранить конфиденциальные корпоративной информации и предоставляют доступ к ресурсам организации Office 365. Для защиты информации в вашей организации, вы можете выполнять полный очистки или Выборочный очистки:</span><span class="sxs-lookup"><span data-stu-id="6211f-p101">Mobile devices can store sensitive organizational information and provide access to your organization's Office 365 resources. To help protect your organization's information, you can do a full wipe or a selective wipe:</span></span>
    
  - <span data-ttu-id="6211f-p102">**Полный очистки**: Удаляет все данные на мобильном устройстве пользователя, включая установленные приложения, фотографии и личные сведения. После завершения очистки устройства восстанавливается его параметры фабрики.</span><span class="sxs-lookup"><span data-stu-id="6211f-p102">**Full wipe**: Deletes all data on a user's mobile device, including installed applications, photos, and personal information. When the wipe is complete, the device is restored to its factory settings.</span></span> 
    
  - <span data-ttu-id="6211f-110">**Функция выборочной стирание**: удаляется только данные организации и оставляет установленные приложения, фотографии и личные сведения на мобильном устройстве пользователя.</span><span class="sxs-lookup"><span data-stu-id="6211f-110">**Selective wipe**: Removes only organization data and leaves installed applications, photos, and personal information on a user's mobile device.</span></span> 
    
- <span data-ttu-id="6211f-111">Если устройство является Очистить (очистки полный или Выборочный очистки), устройство удаляется из списка управляемых устройств.</span><span class="sxs-lookup"><span data-stu-id="6211f-111">When a device is wiped (full wipe or selective wipe), the device is removed from the list of managed devices.</span></span>
    
- <span data-ttu-id="6211f-p103">Можно настроить политики управления мобильного устройства, которая автоматически стирание (полный очистки) устройства после неудачных попыток пользователя ввести пароль устройства определенное количество раз. Выполните действия, описанные в [Создание и развертывание политик безопасности устройств](create-device-security-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6211f-p103">You can set up a mobile device management policy that automatically wipes (full wipe) a device after the user unsuccessfully tries to enter the device's password a specific number of times. Follow the steps in [Create and deploy device security policies](create-device-security-policies.md).</span></span>
    
- <span data-ttu-id="6211f-114">Если вы хотите знать, что пользователь будет работать после стирание свои устройства, [влияет на пользователя и устройства?](wipe-a-mobile-device.md#BKMK_Impact).</span><span class="sxs-lookup"><span data-stu-id="6211f-114">If you want to know what a user will experience when you wipe their device, see [What's the user and device impact?](wipe-a-mobile-device.md#BKMK_Impact).</span></span>
    
## <a name="wipe-a-mobile-device"></a><span data-ttu-id="6211f-115">Стирание мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="6211f-115">Wipe a mobile device</span></span>

1. <span data-ttu-id="6211f-116">Последовательно выберите пункты [ ![щелкните здесь, чтобы перейти в центр администрирования Office 365.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).</span><span class="sxs-lookup"><span data-stu-id="6211f-116">Go to the [![Click here to go to the Office 365 admin center.](media/e00ba917-c3fb-4173-b344-43eb5c7eeb15.png)](https://portal.office.com/adminportal/home).</span></span>

2. <span data-ttu-id="6211f-117">Последовательно выберите пункты [Откройте раздел безопасность Office 365 &amp; центре соответствия требованиям](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8) \> **защиту от потери данных** \> **Управление устройствами**.</span><span class="sxs-lookup"><span data-stu-id="6211f-117">Go to [Go to the Office 365 Security &amp; Compliance Center](https://support.office.com/article/7e696a40-b86b-4a20-afcc-559218b7b1b8)\> **Data loss prevention** \> **Device management**.</span></span>
    
3. <span data-ttu-id="6211f-118">Выберите устройство, которое требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="6211f-118">Select the device you want to wipe.</span></span>
    
4. <span data-ttu-id="6211f-119">Выберите тип удаленной очистки, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="6211f-119">Select the type of remote wipe you want to do.</span></span>
    
  - <span data-ttu-id="6211f-120">Выборочный очистки и удалить только Office 365 сведения об организации, в области справа выберите **функция выборочной стирание**.</span><span class="sxs-lookup"><span data-stu-id="6211f-120">To do a selective wipe and delete only Office 365 organization information, in the right pane, select **Selective wipe**.</span></span>
    
  - <span data-ttu-id="6211f-121">Выполните полный очистки и восстановления устройства параметры фабрики, в области справа выберите **Полный очистки**.</span><span class="sxs-lookup"><span data-stu-id="6211f-121">To do a full wipe and restore the device to its factory settings, in the right pane, select **Full wipe**.</span></span>
    
![Выберите устройство и затем выберите тип очистки для выполнения.](media/ac940abe-0c4a-404e-a842-a1ad2af13ce3.png)
  
5. <span data-ttu-id="6211f-123">Выберите **Да** для подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6211f-123">Select **Yes** to confirm.</span></span> 
    
<span data-ttu-id="6211f-124">До завершения очистки **Состояние устройства** будет показано, как **RetirePending** или **RetireIssued**.</span><span class="sxs-lookup"><span data-stu-id="6211f-124">Until the wipe finishes, the **Device status** will show as **RetirePending** or **RetireIssued**.</span></span>
  
### <a name="how-do-i-know-it-worked"></a><span data-ttu-id="6211f-125">Как узнать, что она работает?</span><span class="sxs-lookup"><span data-stu-id="6211f-125">How do I know it worked?</span></span>

<span data-ttu-id="6211f-126">Больше не увидите мобильных устройств в списке управляемыми устройствами.</span><span class="sxs-lookup"><span data-stu-id="6211f-126">You'll no longer see the mobile device in the list of managed devices.</span></span>
  
## <a name="why-would-you-want-to-wipe-a-device"></a><span data-ttu-id="6211f-127">Почему бы вы хотите стирание устройства?</span><span class="sxs-lookup"><span data-stu-id="6211f-127">Why would you want to wipe a device?</span></span>

<span data-ttu-id="6211f-128">Существует несколько причин для полное удаление устройств.</span><span class="sxs-lookup"><span data-stu-id="6211f-128">There are several reasons for wiping devices:</span></span>
  
- <span data-ttu-id="6211f-p104">Мобильных устройствах, таких как смартфоны и планшетные ПК становятся более полнофункционального все время. Это означает, что проще для пользователей для хранения конфиденциальных данных организации (например, персональных и конфиденциальных сообщений) и получить к нему доступ в дороге. Если один из этих мобильных устройств потери или кражи, очистка устройства сразу же можно предотвратить вашей организации сведений заканчивающиеся руки.</span><span class="sxs-lookup"><span data-stu-id="6211f-p104">Mobile devices like smartphones and tablets are becoming more full-featured all the time. This means it's easier for your users to store sensitive corporate information (such as personal identification or confidential communications) and access it on the go. If one of these mobile devices is lost or stolen, wiping the device immediately can help prevent your organization's information from ending up in the wrong hands.</span></span>
    
- <span data-ttu-id="6211f-132">Когда пользователь покидает организации с личного устройства, участвуют в MDM для Office 365, могут предупредить корпоративной информации переход с этим пользователем, выполнив Выборочный очистки.</span><span class="sxs-lookup"><span data-stu-id="6211f-132">When a user leaves the organization with a personal device that is enrolled in MDM for Office 365, you can help prevent organizational information from going with that user by doing a selective wipe.</span></span>
    
- <span data-ttu-id="6211f-p105">Если организация предоставляет мобильных устройств для пользователей, может потребоваться переназначить устройств от времени. Выполните полный очистки устройства перед присвоением нового пользователя помогает гарантирует удаления любой конфиденциальной информации с прежнего владельца.</span><span class="sxs-lookup"><span data-stu-id="6211f-p105">If your organization provides mobile devices to users, you might need to reassign devices from time to time. Doing a full wipe on a device before assigning it to a new user helps ensures that any sensitive information from the previous owner is deleted.</span></span>
    
## <a name="whats-the-user-and-device-impact"></a><span data-ttu-id="6211f-135">Что такое пользователя и влияние устройство?</span><span class="sxs-lookup"><span data-stu-id="6211f-135">What's the user and device impact?</span></span>

<span data-ttu-id="6211f-p106">Очистки сразу отправляется на мобильное устройство. Устройства также отмечен как не соответствует спецификации в AAD.</span><span class="sxs-lookup"><span data-stu-id="6211f-p106">The wipe is sent immediately to the mobile device. The device is also marked as not compliant in AAD.</span></span>
  
<span data-ttu-id="6211f-138">В следующей таблице описываются содержимого удаляется для каждого типа устройства при выборочно Очистить устройство.</span><span class="sxs-lookup"><span data-stu-id="6211f-138">The following table describes what content is removed for each device type when a device is selectively wiped.</span></span>
  
|<span data-ttu-id="6211f-139">**Влияние контента**</span><span class="sxs-lookup"><span data-stu-id="6211f-139">**Content impact**</span></span>|<span data-ttu-id="6211f-140">**Windows Phone 8.1**</span><span class="sxs-lookup"><span data-stu-id="6211f-140">**Windows Phone 8.1**</span></span>|<span data-ttu-id="6211f-141">**iOS 7.1+**</span><span class="sxs-lookup"><span data-stu-id="6211f-141">**iOS 7.1+**</span></span>|<span data-ttu-id="6211f-142">**Android 4 и более поздние версии**</span><span class="sxs-lookup"><span data-stu-id="6211f-142">**Android 4+**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6211f-143">Приложение портала компании\* удаляется.</span><span class="sxs-lookup"><span data-stu-id="6211f-143">Company Portal app\* is uninstalled.</span></span>  <br/> |<span data-ttu-id="6211f-144">Недоступно</span><span class="sxs-lookup"><span data-stu-id="6211f-144">N/A</span></span>  <br/> |<span data-ttu-id="6211f-145">✔</span><span class="sxs-lookup"><span data-stu-id="6211f-145">✔</span></span>  <br/> |<span data-ttu-id="6211f-146">Недоступно</span><span class="sxs-lookup"><span data-stu-id="6211f-146">N/A</span></span>  <br/> |
|<span data-ttu-id="6211f-p107">Данные приложения Office 365, размещенных приложений, где контроля доступа поддерживаемый MDM для Office 365 — удалены (в настоящее время Outlook и OneDrive для бизнеса). Приложения не удаляются.</span><span class="sxs-lookup"><span data-stu-id="6211f-p107">Office 365 app data hosted by apps where access control is supported by MDM for Office 365 is removed (currently Outlook and OneDrive for Business). The apps are not removed.</span></span>  <br/> <span data-ttu-id="6211f-149">Outlook для Android не удаляет кэшированные по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="6211f-149">Outlook for Android does not remove cached emails.</span></span>  <br/> |<span data-ttu-id="6211f-150">✔</span><span class="sxs-lookup"><span data-stu-id="6211f-150">✔</span></span>  <br/> |<span data-ttu-id="6211f-151">✔</span><span class="sxs-lookup"><span data-stu-id="6211f-151">✔</span></span>  <br/> |<span data-ttu-id="6211f-152">✔</span><span class="sxs-lookup"><span data-stu-id="6211f-152">✔</span></span>  <br/> |
|<span data-ttu-id="6211f-153">Параметры политики, которые были установлены с MDM для Office 365 на устройствах больше не применяются на устройстве и пользователи могут менять параметры.</span><span class="sxs-lookup"><span data-stu-id="6211f-153">Policy settings that were applied by MDM for Office 365 to devices are no longer enforced on the device and users can change the settings.</span></span>  <br/> |<span data-ttu-id="6211f-154">✔</span><span class="sxs-lookup"><span data-stu-id="6211f-154">✔</span></span>  <br/> |<span data-ttu-id="6211f-155">✔</span><span class="sxs-lookup"><span data-stu-id="6211f-155">✔</span></span>  <br/> |<span data-ttu-id="6211f-156">✔</span><span class="sxs-lookup"><span data-stu-id="6211f-156">✔</span></span>  <br/> |
|<span data-ttu-id="6211f-157">Профили электронной почты, созданные MDM для Office 365 и удалены кэшированные электронной почты в устройстве.</span><span class="sxs-lookup"><span data-stu-id="6211f-157">Email profiles created by MDM for Office 365 are removed and cached email on the device is deleted.</span></span>  <br/> |<span data-ttu-id="6211f-158">Недоступно</span><span class="sxs-lookup"><span data-stu-id="6211f-158">N/A</span></span>  <br/> |<span data-ttu-id="6211f-159">✔</span><span class="sxs-lookup"><span data-stu-id="6211f-159">✔</span></span>  <br/> |<span data-ttu-id="6211f-160">Недоступно</span><span class="sxs-lookup"><span data-stu-id="6211f-160">N/A</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="6211f-161">\*Приложение портала компании доступен на хранилище приложений для iOS и воспроизвести хранилища для устройства Android.</span><span class="sxs-lookup"><span data-stu-id="6211f-161">\* Company Portal app is available at the App Store for iOS and the Play Store for Android devices.</span></span> 
  
## <a name="related-content"></a><span data-ttu-id="6211f-162">Связанные материалы</span><span class="sxs-lookup"><span data-stu-id="6211f-162">Related content</span></span>

[<span data-ttu-id="6211f-163">Управлять мобильными устройствами в Office 365</span><span class="sxs-lookup"><span data-stu-id="6211f-163">Manage mobile devices in Office 365</span></span>](set-up-mobile-device-management.md)
  

