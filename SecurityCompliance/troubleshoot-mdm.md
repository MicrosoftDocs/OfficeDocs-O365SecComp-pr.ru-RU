---
title: Устранение неполадок устройства подачи заявок с MDM для Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/17/2015
ms.audience: Admin
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: c863b2bf-45f3-483a-ba05-29fc7f4d6434
description: Если вы используете за ошибок при попытке зарегистрировать устройства в Mobile Device Management (MDM) для Office 365, попробуйте выполните следующие действия для отслеживания проблемы. Общие действия не устранена, в статье один из более поздней версии разделов с помощью действия для вашего типа устройства.
ms.openlocfilehash: 490259fc623b38ab5ad6cf8553c5074c77b77426
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272114"
---
# <a name="troubleshoot-device-enrollment-with-mdm-for-office-365"></a><span data-ttu-id="930fb-104">Устранение неполадок устройства подачи заявок с MDM для Office 365</span><span class="sxs-lookup"><span data-stu-id="930fb-104">Troubleshoot device enrollment with MDM for Office 365</span></span>

<span data-ttu-id="930fb-p102">Если вы используете за ошибок при попытке зарегистрировать устройства в Mobile Device Management (MDM) для Office 365, попробуйте выполните следующие действия для отслеживания проблемы. Общие действия не устранена, в статье один из более поздней версии разделов с помощью действия для вашего типа устройства.</span><span class="sxs-lookup"><span data-stu-id="930fb-p102">If you're running into issues when you try to enroll a device in Mobile Device Management (MDM) for Office 365, try the steps listed here to track down the problem. If the general steps don't fix the issue, see one of the later sections with specific steps for your device type.</span></span>
  
## <a name="steps-to-try-first"></a><span data-ttu-id="930fb-107">Действия, чтобы сначала</span><span class="sxs-lookup"><span data-stu-id="930fb-107">Steps to try first</span></span>

<span data-ttu-id="930fb-108">Чтобы начать, проверьте следующее:</span><span class="sxs-lookup"><span data-stu-id="930fb-108">To start, check the following:</span></span>
  
- <span data-ttu-id="930fb-109">Убедитесь в том, что устройство является не уже участвуют с другой поставщик управления мобильных устройств, такие как Intune.</span><span class="sxs-lookup"><span data-stu-id="930fb-109">Make sure that the device is not already enrolled with another mobile device management provider, such as Intune.</span></span>
    
- <span data-ttu-id="930fb-110">Убедитесь в том, что устройства задано значение правильность установки даты и времени.</span><span class="sxs-lookup"><span data-stu-id="930fb-110">Make sure that the device is set to the correct date and time.</span></span>
    
- <span data-ttu-id="930fb-111">Перейдите в разных Wi-Fi или сотовой сети на устройстве.</span><span class="sxs-lookup"><span data-stu-id="930fb-111">Switch to a different Wi-Fi or cellular network on the device.</span></span>
    
- <span data-ttu-id="930fb-112">Для устройств Android или операций ввода-вывода удаление и повторная установка приложения портала компании Intune на устройстве.</span><span class="sxs-lookup"><span data-stu-id="930fb-112">For Android or iOS devices, uninstall and reinstall the Intune Company Portal app on the device.</span></span>
    
## <a name="ios-phone-or-tablet"></a><span data-ttu-id="930fb-113">операций ввода-вывода телефон или планшет</span><span class="sxs-lookup"><span data-stu-id="930fb-113">iOS phone or tablet</span></span>

- <span data-ttu-id="930fb-114">Убедитесь в том, что [Настройка сертификат APN](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).</span><span class="sxs-lookup"><span data-stu-id="930fb-114">Make sure that you've [set up an APNs certificate](https://support.office.com/article/522b43f4-a2ff-46f6-962a-dd4f47e546a7).</span></span>
    
- <span data-ttu-id="930fb-p103">В **параметрах** \> **Общие** \> **профиля** (или **Управление устройствами**), убедитесь в том, что **Профиль управления** еще не установлен. Если это так, удалите его.</span><span class="sxs-lookup"><span data-stu-id="930fb-p103">In **Settings** \> **General** \> **Profile** (or **Device Management**), make sure that a **Management Profile** is not already installed. If it is, remove it.</span></span> 
    
- <span data-ttu-id="930fb-117">Если появится сообщение об ошибке «Устройство не удалось зарегистрировать,» вход на портал Office 365 и убедитесь в том, что лицензии, которая включает в себя Exchange Online была назначена пользователя, который входит в систему устройства.</span><span class="sxs-lookup"><span data-stu-id="930fb-117">If you see the error message, "Device failed to enroll," sign in to Office 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="930fb-118">Если появится сообщение об ошибке «Профиль не удалось установить,» выполните одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="930fb-118">If you see the error message, "Profile failed to install," try one of the following:</span></span>
    
  - <span data-ttu-id="930fb-119">Убедитесь в том, что Safari браузера по умолчанию на устройстве, и файлы cookie не отключены.</span><span class="sxs-lookup"><span data-stu-id="930fb-119">Make sure that Safari is the default browser on the device, and that cookies are not disabled.</span></span>
    
  - <span data-ttu-id="930fb-120">Перезагрузите устройство, а затем перейдите к portal.manage.microsoft.com вход с помощью Office 365 идентификатор пользователя и пароль и попытайтесь вручную установить профиль.</span><span class="sxs-lookup"><span data-stu-id="930fb-120">Reboot the device, then navigate to portal.manage.microsoft.com, sign in with your Office 365 user ID and password, and attempt to install the profile manually.</span></span>
    
## <a name="windows-rt-tablet"></a><span data-ttu-id="930fb-121">Планшет Windows RT</span><span class="sxs-lookup"><span data-stu-id="930fb-121">Windows RT tablet</span></span>

- <span data-ttu-id="930fb-122">Убедитесь в том, что ваш домен будет [задано в Office 365 для работы с MDM](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="930fb-122">Make sure that your domain is [set up in Office 365 to work with MDM](set-up-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="930fb-123">Убедитесь в том, что пользователь Выбор **Включение** вместо того чтобы выбирать **присоединиться к**.</span><span class="sxs-lookup"><span data-stu-id="930fb-123">Make sure that the user is choosing **Turn On** rather than choosing **Join**.</span></span>
    
## <a name="windows-phone"></a><span data-ttu-id="930fb-124">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="930fb-124">Windows Phone</span></span>

- <span data-ttu-id="930fb-125">Убедитесь в том, что ваш домен будет [задано в Office 365 для работы с MDM](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="930fb-125">Make sure that your domain is [set up in Office 365 to work with MDM](set-up-mobile-device-management.md).</span></span>
    
- <span data-ttu-id="930fb-126">Убедитесь, что устройство работает под управлением Windows 8.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="930fb-126">Make sure the device is running Windows 8.1 or later.</span></span>
    
## <a name="android-phone-or-tablet"></a><span data-ttu-id="930fb-127">Android телефон или планшет</span><span class="sxs-lookup"><span data-stu-id="930fb-127">Android phone or tablet</span></span>

- <span data-ttu-id="930fb-128">Убедитесь, что устройство работает под управлением Android версии 4.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="930fb-128">Make sure the device is running Android 4.0 or later.</span></span>
    
- <span data-ttu-id="930fb-129">Если появится сообщение об ошибке «Мы не удалось зарегистрировать это устройство» вход в Office 365 и убедитесь в том, что лицензии, которая включает в себя Exchange Online была назначена пользователя, который входит в систему устройства.</span><span class="sxs-lookup"><span data-stu-id="930fb-129">If you see the error message, "We couldn't enroll this device," sign in to Office 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="930fb-130">Проверьте в **Области уведомлений** на устройстве ли ожидающих любые действия, необходимые конечных пользователей и если да, выполните действия.</span><span class="sxs-lookup"><span data-stu-id="930fb-130">Check the **Notification Area** on the device to see if any required end-user actions are pending, and if they are, complete the actions.</span></span> 
    

