---
title: Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/21/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
description: Интеграция с Windows Защитник расширенного защиту от угроз для просмотра более подробные сведения об управлении угроз защиту от угроз для Office 365 расширенный.
ms.openlocfilehash: 1198f53c47811d69b93106c413e3d3a09d83e736
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706143"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="479d9-103">Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows</span><span class="sxs-lookup"><span data-stu-id="479d9-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="479d9-p101">Если вы являетесь участником группы безопасности вашей организации, можно интегрировать Office 365 с помощью Windows Защитник расширенного угроз защиты анализа. Это может помочь быстро понимать, если компьютеров пользователей в группу риска при изучении угрозы безопасности в Office 365. Например после включения интеграции вы сможете для просмотра списка компьютеров, используемых получателей сообщения электронной почты вредоносным, а также как количество оповещений компьютеры, имеют в ATP Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="479d9-p101">If you are part of your organization's security team, you can integrate Office 365 with Windows Defender Advanced Threat Protection (ATP). This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender ATP.</span></span>
  
<span data-ttu-id="479d9-107">На следующем рисунке показана вкладка **устройств** , что вы увидите, когда у интеграция ATP Защитник Windows включена:</span><span class="sxs-lookup"><span data-stu-id="479d9-107">The following image shows the **Devices** tab that you'll see when have Windows Defender ATP integration enabled:</span></span> 
  
![При включении анализа Защитник Windows можно просмотреть список компьютеров с оповещениями.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="479d9-p102">В этом примере видно, что получателей сообщения электронной почты имеют четыре компьютера и одно оповещение в ATP Защитника Windows. Щелкнув ссылку на компьютер открывает страницу компьютера в ATP Защитника Windows в новую вкладку.</span><span class="sxs-lookup"><span data-stu-id="479d9-p102">In this example, you can see that the recipients of the email message have four machines and one has an alert in Windows Defender ATP. Clicking the link to a machine opens the machine page in Windows Defender ATP in a new tab.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="479d9-111">Требования</span><span class="sxs-lookup"><span data-stu-id="479d9-111">Requirements</span></span>

- <span data-ttu-id="479d9-112">Вашей организации должны иметь анализ угроз Office 365 и анализа Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="479d9-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="479d9-p103">Необходимо обладать правами глобального администратора Office 365 или роль администратора безопасности, назначенные в [безопасности &amp; центре соответствия требованиям](https://security.microsoft.com). (Увидеть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="479d9-p103">You must be an Office 365 global administrator or have a security administrator role assigned in the [Security &amp; Compliance Center](https://security.microsoft.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="479d9-115">Необходимо иметь доступ к анализ угроз Office 365 и портала ATP Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="479d9-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender ATP portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="479d9-116">Чтобы интегрировать анализ угроз Office 365 с ATP Защитника Windows</span><span class="sxs-lookup"><span data-stu-id="479d9-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="479d9-117">Интеграция анализ угроз Office 365 с ATP Защитник Windows настроена в Office 365 и на портале ATP Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="479d9-117">Integrating Office 365 Threat Intelligence with Windows Defender ATP is set up both in Office 365 and in the Windows Defender ATP portal.</span></span>
  
1. <span data-ttu-id="479d9-118">Как глобальный Office 365 или администратор безопасности, перейдите к [https://security.microsoft.com](https://security.microsoft.com) и войдите с работы или школы учетную запись на Office 365.</span><span class="sxs-lookup"><span data-stu-id="479d9-118">As an Office 365 global or a security administrator, go to [https://security.microsoft.com](https://security.microsoft.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="479d9-119">Выберите **Threat management** \> **explorer угроз**.</span><span class="sxs-lookup"><span data-stu-id="479d9-119">Choose **Threat management** \> **Threat explorer**.</span></span>
    
3. <span data-ttu-id="479d9-120">В меню **Дополнительные** выберите **Параметры WDATP**.</span><span class="sxs-lookup"><span data-stu-id="479d9-120">On the **More** menu, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="479d9-121">Выберите **подключение к Windows анализа**.</span><span class="sxs-lookup"><span data-stu-id="479d9-121">Select **Connect to Windows ATP**.</span></span>
    
<span data-ttu-id="479d9-p104">После изменения параметров в Office 365, необходимо включить подключение от ATP Защитника Windows. Для этого показано [Использование портала защиту от угроз дополнительные Защитника Windows](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="479d9-p104">After you have changed the settings in Office 365, you must enable the connection from Windows Defender ATP. To do that, see [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="479d9-124">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="479d9-124">Related topics</span></span>

[<span data-ttu-id="479d9-125">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="479d9-125">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="479d9-126">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="479d9-126">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

