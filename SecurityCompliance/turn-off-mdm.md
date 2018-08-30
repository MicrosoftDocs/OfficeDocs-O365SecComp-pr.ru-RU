---
title: Отключение управления мобильного устройства в Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- GPA150
- MET150
ms.assetid: 2709cafb-0a8b-44bc-8494-7e2fccfa2b19
description: Выполните следующие действия, чтобы остановить политик MDM применению для мобильных устройств в организации Office 365.
ms.openlocfilehash: 6b8f0036ed999b10263f5cc074df27175769e604
ms.sourcegitcommit: c31424cafbf1953f2864d7e2ceb95b329a694edb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/29/2018
ms.locfileid: "23272224"
---
# <a name="how-to-turn-off-mobile-device-management-in-office-365"></a><span data-ttu-id="7d7b1-103">Отключение управления мобильного устройства в Office 365</span><span class="sxs-lookup"><span data-stu-id="7d7b1-103">How to turn off Mobile Device Management in Office 365</span></span>

<span data-ttu-id="7d7b1-104">Чтобы эффективно отключить MDM для Office 365, удаление группы людей (определяется с помощью групп безопасности) из политики управления устройствами или удалить сами политики.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-104">To effectively turn off MDM for Office 365, you remove groups of people (defined by security groups) from the device management policies, or remove the policies themselves.</span></span> 
  
- <span data-ttu-id="7d7b1-105">Удаление групп пользователей путем удаления группы безопасности пользователя из политики устройств, созданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-105">Remove groups of users by removing user security groups from the device policies you've created.</span></span> 
    
- <span data-ttu-id="7d7b1-106">Отключите MDM для всех пользователей, удаление всех политик MDM устройства.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-106">Disable MDM for everyone by removing all MDM device policies.</span></span> 
    
<span data-ttu-id="7d7b1-p101">Эти параметры будут удалены принудительное применение MDM для устройств в вашей организации. К сожалению Вы не может «Отмена наполнения просто» MDM для Office 365 после настройки его.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-p101">These options will remove MDM enforcement for devices in your organization. Unfortunately, you can't simply "unprovision" MDM for Office 365 after you've set it up.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7d7b1-p102">Следует учитывать влияние на устройствах пользователей, при удалении группы безопасности пользователя из политик или удалить сами политики. Например, электронной почты профили и кэшированные сообщения электронной почты могут быть удалены в зависимости от устройства. См.: [влияет на политики безопасности для различных типов устройств?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)</span><span class="sxs-lookup"><span data-stu-id="7d7b1-p102">Be aware of the impact on users' devices when you remove user security groups from policies or remove the policies themselves. For example, email profiles and cached emails may be removed, depending on the device. See: [What is the impact of security policies on different device types?](create-device-security-policies.md#what-is-the-impact-of-security-policies-on-different-device-types)</span></span>
  
## <a name="remove-user-security-groups-from-mdm-device-policies"></a><span data-ttu-id="7d7b1-112">Удаление группы безопасности пользователя из политики устройств MDM</span><span class="sxs-lookup"><span data-stu-id="7d7b1-112">Remove user security groups from MDM device policies</span></span>

1. <span data-ttu-id="7d7b1-113">Последовательно выберите пункты **безопасности &amp; центре соответствия требованиям** \> **защиту от потери данных** \> **политик безопасности устройств**.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-113">Go to **Security &amp; Compliance Center**\> **Data loss prevention** \> **Device security polices**.</span></span>
    
2. <span data-ttu-id="7d7b1-114">Выберите политику устройства и нажмите кнопку ![значок Правка](media/O365-MDM-CreatePolicy-EditIcon.gif) **Изменение политики**.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-114">Select a device policy, and click ![Edit icon](media/O365-MDM-CreatePolicy-EditIcon.gif) **Edit policy**.</span></span>
    
3. <span data-ttu-id="7d7b1-115">В разделе **Развертывание**щелкните ссылку **- Удалить**.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-115">Under **Deployment**, click **- Remove**.</span></span>
    
    <span data-ttu-id="7d7b1-116">В разделе **группы**выберите группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-116">Under **Groups**, select a security group.</span></span>
    
4.  <span data-ttu-id="7d7b1-117">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-117">Click **Remove**.</span></span>
    
5. <span data-ttu-id="7d7b1-118">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-118">Click **Save**.</span></span>
    
## <a name="remove-mdm-device-policies"></a><span data-ttu-id="7d7b1-119">Удаление политики устройств MDM</span><span class="sxs-lookup"><span data-stu-id="7d7b1-119">Remove MDM device policies</span></span>

1. <span data-ttu-id="7d7b1-120">Последовательно выберите пункты **безопасности &amp; центре соответствия требованиям** \> **политики безопасности** \> **политики безопасности устройств**.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-120">Go to **Security &amp; Compliance Center**\> **Security policies** \> **Device security policies**.</span></span>
    
2. <span data-ttu-id="7d7b1-p103">Выберите политику устройства и нажмите кнопку ![изображение корзину можно значок. ](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Удаление политики**.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-p103">Select a device policy, and then click ![Image of the trash can icon.](media/b8bfa783-c0b5-46d9-9570-8a385088e8fe.png) **Delete policy**.</span></span>
    
3. <span data-ttu-id="7d7b1-123">В диалоговом окне **предупреждения** нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="7d7b1-123">In the **Warning** dialog, click **Yes**.</span></span> 
    

