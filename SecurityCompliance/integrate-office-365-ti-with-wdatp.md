---
title: Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection: M365-security-compliance
description: Интеграция с Windows Защитник расширенного защиту от угроз для просмотра более подробные сведения об управлении угроз защиту от угроз для Office 365 расширенный.
ms.openlocfilehash: f8f5f50af10fb668aa67b68604e95e8dd19c9e69
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995210"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="576a8-103">Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows</span><span class="sxs-lookup"><span data-stu-id="576a8-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="576a8-p101">Если вы являетесь участником группы безопасности вашей организации, можно интегрировать функции защиты расширенного Threat Office 365 и анализ угроз с защитой расширенного Защитника Windows. Это может помочь быстро понимать, если компьютеров пользователей в группу риска при изучении угрозы безопасности в Office 365. Например после включения интеграции вы сможете также увидеть список компьютеров, используемых получателей сообщения электронной почты вредоносным, как количество оповещений компьютеры, имеют в защиту от угроз дополнительные Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="576a8-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="576a8-107">На следующем рисунке показана вкладка **устройств** , что вы увидите, когда у интеграция защиту от угроз дополнительные Защитник Windows включена:</span><span class="sxs-lookup"><span data-stu-id="576a8-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![При включении анализа Защитник Windows можно просмотреть список компьютеров с оповещениями.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="576a8-p102">В этом примере видно, что получателей сообщения электронной почты при наличии четырех устройств и один список имеет соответствующее оповещение. Щелкнув ссылку для устройства открывает ее страницу на портале защиту от угроз дополнительные Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="576a8-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="576a8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="576a8-111">Requirements</span></span>

- <span data-ttu-id="576a8-112">Вашей организации должны иметь анализ угроз Office 365 и анализа Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="576a8-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="576a8-p103">Необходимо быть глобального администратора Office 365 или роль администратора безопасности (например, администратор безопасности) в [безопасности &amp; центре соответствия требованиям](https://protection.office.com). (Увидеть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="576a8-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="576a8-115">Необходимо иметь доступ к анализ угроз Office 365 и портала защиту от угроз дополнительные Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="576a8-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="576a8-116">Чтобы интегрировать анализ угроз Office 365 с ATP Защитника Windows</span><span class="sxs-lookup"><span data-stu-id="576a8-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="576a8-117">Интеграция анализ угроз Office 365 с защитой расширенного Защитник Windows настраивается с помощью обоих безопасности Office 365 & центра соответствия требованиям и портала защиту от угроз дополнительные Защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="576a8-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="576a8-118">Как глобальный администратор Office 365 или администратор безопасности, перейдите к [https://protection.office.com](https://protection.office.com) и войдите с работы или школы учетную запись на Office 365.</span><span class="sxs-lookup"><span data-stu-id="576a8-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="576a8-119">Выберите **Threat management** \> **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="576a8-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="576a8-120">![Explorer в меню Threat Management](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="576a8-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="576a8-121">В правом верхнем углу экрана выберите **Параметры WDATP**.</span><span class="sxs-lookup"><span data-stu-id="576a8-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="576a8-122">В диалоговом окне подключения к ATP Защитник Windows преобразовать на подключение к Windows ATP.</span><span class="sxs-lookup"><span data-stu-id="576a8-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Подключение ATP Защитника Windows](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="576a8-p104">Разрешить подключения в защиту от угроз дополнительные Защитника Windows. Показано [Использование портала защиту от угроз дополнительные Защитника Windows](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="576a8-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="576a8-126">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="576a8-126">Related topics</span></span>

[<span data-ttu-id="576a8-127">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="576a8-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="576a8-128">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="576a8-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

