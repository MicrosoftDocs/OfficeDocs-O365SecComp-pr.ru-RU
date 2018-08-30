---
title: Общие сведения об управлении мобильных устройств (MDM) для Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- O365M_MDMConfigDomains
- O365E_MDMConfigDomains
- ms.o365.cc.DevicePolicy
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: faa7d8e5-645d-4d59-839c-c8d4c1869e4a
description: Можно управлять и обеспечения безопасности мобильных устройств, при подключении к организации Office 365 с помощью мобильного устройства управления для Office 365. Мобильные устройства, такие как смартфоны и планшетные ПК, которые используются для доступа к работы электронной почты, календарь, контакты и документы воспроизведение большая часть в проверке того, что сотрудникам выполнять свою работу в любое время и в любом месте. Поэтому важно для защиты данных организации людей с помощью устройств. Установка устройства безопасности правила политики и доступа и стирание мобильного устройства, если они в случае потери или кражи можно использовать MDM для Office 365.
ms.openlocfilehash: f06cef11b68ee0673f13c54738f07f4556495fdd
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272494"
---
# <a name="overview-of-mobile-device-management-mdm-for-office-365"></a><span data-ttu-id="783fe-106">Общие сведения об управлении мобильных устройств (MDM) для Office 365</span><span class="sxs-lookup"><span data-stu-id="783fe-106">Overview of Mobile Device Management (MDM) for Office 365</span></span>

<span data-ttu-id="783fe-p102">Можно управлять и обеспечения безопасности мобильных устройств, при подключении к организации Office 365 с помощью мобильного устройства управления для Office 365. Мобильные устройства, такие как смартфоны и планшетные ПК, которые используются для доступа к работы электронной почты, календарь, контакты и документы воспроизведение большая часть в проверке того, что сотрудникам выполнять свою работу в любое время и в любом месте. Поэтому важно для защиты данных организации людей с помощью устройств. Установка устройства безопасности правила политики и доступа и стирание мобильного устройства, если они в случае потери или кражи можно использовать MDM для Office 365.</span><span class="sxs-lookup"><span data-stu-id="783fe-p102">You can manage and secure mobile devices when they're connected to your Office 365 organization by using Mobile Device Management for Office 365. Mobile devices like smartphones and tablets that are used to access work email, calendar, contacts, and documents play a big part in making sure that employees get their work done anytime, from anywhere. So it's critical that you help protect your organization's information when people use devices. You can use MDM for Office 365 to set device security policies and access rules, and to wipe mobile devices if they're lost or stolen.</span></span>
  
![MDM на телефоне Android](media/69b9a9f6-13ac-4e36-99ca-95e82e0375aa.png)
  
## <a name="what-types-of-devices-can-you-manage"></a><span data-ttu-id="783fe-112">Устройствами каких типов можно управлять?</span><span class="sxs-lookup"><span data-stu-id="783fe-112">What types of devices can you manage?</span></span>

<span data-ttu-id="783fe-p103">MDM для Office 365 можно использовать для управления типами множество мобильных устройств, такие как Windows Phone, Android, iPhone и iPad. Для управления мобильных устройств, используемых сотрудникам вашей организации, каждый пользователь должен иметь лицензию применимых Office 365 и свои устройства должны быть зарегистрированы в MDM для Office 365.</span><span class="sxs-lookup"><span data-stu-id="783fe-p103">You can use MDM for Office 365 to manage many types of mobile devices like Windows Phone, Android, iPhone, and iPad. To manage mobile devices used by people in your organization, each person must have an applicable Office 365 license and their device must be enrolled in MDM for Office 365.</span></span> 
  
<span data-ttu-id="783fe-115">Поддерживает MDM для Office 365 для каждого типа устройства см [Возможности мобильного устройства управления для Office 365](capabilities-of-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="783fe-115">To see what MDM for Office 365 supports for each type of device, see [Capabilities of Mobile Device Management for Office 365](capabilities-of-mobile-device-management.md).</span></span>
  
## <a name="setup-steps-for-mdm"></a><span data-ttu-id="783fe-116">Шаги установки для MDM</span><span class="sxs-lookup"><span data-stu-id="783fe-116">Setup steps for MDM</span></span>

<span data-ttu-id="783fe-p104">Глобальный администратор Office 365 необходимо выполнить следующие действия, чтобы включить и настроить MDM для Office 365. Следуйте указаниям в разделе на [настройку MDM для Office 365](set-up-mobile-device-management.md) , чтобы просмотреть подробные инструкции. Здесь приводится краткое изложение:</span><span class="sxs-lookup"><span data-stu-id="783fe-p104">An Office 365 global admin must complete the following steps to activate and set up MDM for Office 365. Follow the guidance in the topic on [setting up MDM for Office 365](set-up-mobile-device-management.md) to see detailed steps. Here's a quick summary:</span></span> 
  
> <span data-ttu-id="783fe-120">Шаг 1: Включение MDM для Office 365, выполнив действия, описанные в [задать копирование Mobile Device Management (MDM) в Office 365](set-up-mobile-device-management.md).</span><span class="sxs-lookup"><span data-stu-id="783fe-120">Step 1: Activate MDM for Office 365 by following steps in the [Set up Mobile Device Management (MDM) in Office 365](set-up-mobile-device-management.md).</span></span>
    
> <span data-ttu-id="783fe-121">Шаг 2: Настройка MDM для Office 365, например, создание сертификат APN для управления iOS устройств и добавления записи доменных имен (DNS) для вашего домена для поддержки ОС Windows Phone.</span><span class="sxs-lookup"><span data-stu-id="783fe-121">Step 2: Set up MDM for Office 365 by, for example, creating an APNs certificate to manage iOS devices and adding a Domain Name System (DNS) record for your domain to support Windows phones.</span></span>
    
> <span data-ttu-id="783fe-p105">Шаг 3: Создание политики устройств и применить их к группам пользователей. При этом пользователей будет выведено [сообщение на мобильном устройстве](enroll-your-mobile-device.md). А после завершения регистрации они свои устройства будут применяться политики, настройки их.</span><span class="sxs-lookup"><span data-stu-id="783fe-p105">Step 3: Create device policies and apply them to groups of users. When you do this, your users will get an [enrollment message on their device](enroll-your-mobile-device.md). And when they've completed enrollment, their devices will be restricted by the policies you've set up for them.</span></span>
    
    ![Creating an MDN device policy under Device security policies](media/fbcdbecd-0016-42f1-81a9-9fbad610da90.png)
  
## <a name="device-management-tasks"></a><span data-ttu-id="783fe-125">Задачи управления устройствами</span><span class="sxs-lookup"><span data-stu-id="783fe-125">Device management tasks</span></span>

<span data-ttu-id="783fe-p106">После того как MDM у вас Office 365, настроить и пользователи зарегистрировали свои устройства, управления устройствами, заблокируйте доступ или стирание устройства, если это необходимо. Дополнительные сведения о [некоторых типичных задач управления устройства](manage-devices-in-mdm.md), включая where для выполнения задач.</span><span class="sxs-lookup"><span data-stu-id="783fe-p106">After you've got MDM for Office 365 set up and your users have enrolled their devices, you can manage the devices, block access, or wipe a device, if needed. Learn more about [some common device management tasks](manage-devices-in-mdm.md), including where to complete the tasks.</span></span>
  
## <a name="other-ways-to-manage-devices-and-apps"></a><span data-ttu-id="783fe-128">Другие способы управления устройствами и приложений</span><span class="sxs-lookup"><span data-stu-id="783fe-128">Other ways to manage devices and apps</span></span>

<span data-ttu-id="783fe-129">При необходимости в дополнительных функциональных возможностей, чем MDM для Office 365 включает в себя, извлечения это [сравнение возможностей MDM и Microsoft Intune](choose-between-mdm-and-intune.md) для просмотра, если подписка на Intune будет соответствовать требованиям вашей организации.</span><span class="sxs-lookup"><span data-stu-id="783fe-129">If you need more functionality than MDM for Office 365 includes, check out this [comparison of MDM and Microsoft Intune features](choose-between-mdm-and-intune.md) to see if an Intune subscription would meet your organization's needs.</span></span> 
  
<span data-ttu-id="783fe-p107">Если вам нужно только управления мобильных приложений (MAM), а возможно, для людей, обновление рабочих проектов на устройствах, Intune предоставляет другая возможность помимо Регистрация устройств и управление ими. Подписка на Intune можно настроить политики MAM с помощью Azure портала, даже если устройств людей не регистрируются в Intune. Просмотрите [защитить данные приложения с помощью политик MAM](https://go.microsoft.com/fwlink/?LinkId=825439).</span><span class="sxs-lookup"><span data-stu-id="783fe-p107">If you just need mobile app management (MAM), perhaps for people updating work projects on their own devices, Intune provides another option besides enrolling and managing devices. An Intune subscription allows you to set up MAM policies by using the Azure portal, even if people's devices aren't enrolled in Intune. See [Protect app data using MAM policies](https://go.microsoft.com/fwlink/?LinkId=825439).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="783fe-133">См. также</span><span class="sxs-lookup"><span data-stu-id="783fe-133">See also</span></span>

[<span data-ttu-id="783fe-134">Получение сведений об устройствах, управляется MDM</span><span class="sxs-lookup"><span data-stu-id="783fe-134">Get details about devices managed by MDM</span></span>](get-details-about-mdm-managed-devices.md)

[<span data-ttu-id="783fe-135">Настройка MDM для Office 365</span><span class="sxs-lookup"><span data-stu-id="783fe-135">Set up MDM for Office 365</span></span>](set-up-mobile-device-management.md)
  
[<span data-ttu-id="783fe-136">Регистрация мобильных устройств в MDM</span><span class="sxs-lookup"><span data-stu-id="783fe-136">Enroll mobile devices in MDM</span></span>](enroll-your-mobile-device.md)
  
[<span data-ttu-id="783fe-137">Управление устройствами, участвуют в MDM</span><span class="sxs-lookup"><span data-stu-id="783fe-137">Manage devices enrolled in MDM</span></span>](manage-devices-in-mdm.md)

