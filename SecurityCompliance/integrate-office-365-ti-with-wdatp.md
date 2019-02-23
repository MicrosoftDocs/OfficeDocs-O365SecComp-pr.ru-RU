---
title: Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection: M365-security-compliance
description: Интеграция Office 365 Advanced Threat protection с Advanced Threat Protection в Защитнике Windows для просмотра подробных сведений об управлении угрозами.
ms.openlocfilehash: ec7c7f565a4a316085b586168512699bb13cad47
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220929"
---
# <a name="integrate-office-365-threat-intelligence-with-windows-defender-advanced-threat-protection"></a><span data-ttu-id="ad925-103">Интеграция Office 365 Threat Intelligence с Advanced Threat Protection в Защитнике Windows</span><span class="sxs-lookup"><span data-stu-id="ad925-103">Integrate Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection</span></span>

<span data-ttu-id="ad925-p101">Если вы являетесь участником группы безопасности Организации, вы можете интегрировать функции Office 365 Advanced Threat Protection и Threat Intelligence с помощью Advanced Threat Protection в Защитнике Windows. Это поможет быстро выяснить, подвержены ли компьютеры пользователям риску при изучении угроз в Office 365. Например, когда интеграция включена, вы сможете увидеть список компьютеров, используемых получателями обнаруженного сообщения электронной почты, а также о том, сколько последних оповещений у этих компьютеров в Advanced Threat Protection в Защитнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ad925-p101">If you are part of your organization's security team, you can integrate Office 365 Advanced Threat Protection and Threat Intelligence features with Windows Defender Advanced Threat Protection. This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365. For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Windows Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="ad925-107">На следующем рисунке показана вкладка " **устройства** ", которая будет отображаться, когда включена интеграция с Advanced Threat Protection в Защитнике Windows:</span><span class="sxs-lookup"><span data-stu-id="ad925-107">The following image shows the **Devices** tab that you'll see when have Windows Defender Advanced Threat Protection integration enabled:</span></span> 
  
![Когда пакет ATP для защитника Windows включен, вы можете просмотреть список компьютеров с оповещениями.](media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="ad925-p102">В этом примере видно, что получатели сообщения электронной почты имеют четыре устройства, а одно — оповещение. Если щелкнуть ссылку на устройство, откроется его страница на портале Advanced Threat Protection в Защитнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ad925-p102">In this example, you can see that the recipients of the email message have four devices and one has an alert. Clicking the link for a device opens its page in the Windows Defender Advanced Threat Protection portal.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="ad925-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ad925-111">Requirements</span></span>

- <span data-ttu-id="ad925-112">Ваша организация должна иметь Office 365 Threat Intelligence и пакет ATP для защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="ad925-112">Your organization must have Office 365 Threat Intelligence and Windows Defender ATP.</span></span>
    
- <span data-ttu-id="ad925-p103">Необходимо быть глобальным администратором Office 365 или иметь роль администратора безопасности (например, администратора безопасности), назначенную в [центре &amp; безопасности и соответствия требованиям](https://protection.office.com). (См. [разрешения в центре безопасности &amp; и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="ad925-p103">You must be an Office 365 Global Administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com). (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="ad925-115">Вам необходим доступ к Microsoft Office 365 Threat Intelligence и порталу Advanced Threat Protection в Защитнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ad925-115">You must have access to both Office 365 Threat Intelligence and the Windows Defender Advanced Threat Protection portal.</span></span>
    
## <a name="to-integrate-office-365-threat-intelligence-with-windows-defender-atp"></a><span data-ttu-id="ad925-116">Интеграция службы анализа угроз Office 365 с помощью пакета ATP для защитника Windows</span><span class="sxs-lookup"><span data-stu-id="ad925-116">To integrate Office 365 Threat Intelligence with Windows Defender ATP</span></span>

<span data-ttu-id="ad925-117">Интеграция службы контроля угроз Office 365 с помощью Advanced Threat Protection в Защитнике Windows настраивается с помощью центра безопасности Office 365 _Амп_ соответствие требованиям и портала Advanced Threat Protection в Защитнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ad925-117">Integrating Office 365 Threat Intelligence with Windows Defender Advanced Threat Protection is set up by using both the Office 365 Security & Compliance Center AND the Windows Defender Advanced Threat Protection portal.</span></span>
  
1. <span data-ttu-id="ad925-118">Как глобальный администратор Office 365 или администратор безопасности перейдите к [https://protection.office.com](https://protection.office.com) рабочей или учебной учетной записи для Office 365 с помощью рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ad925-118">As an Office 365 global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account for Office 365.</span></span> 
    
2. <span data-ttu-id="ad925-119">Выберите **Обозреватель** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="ad925-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="ad925-120">![Проводник в меню "Управление угрозами"](media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="ad925-120">![Explorer in Threat Management menu](media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="ad925-121">В правом верхнем углу экрана выберите **Параметры вдатп**.</span><span class="sxs-lookup"><span data-stu-id="ad925-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="ad925-122">В диалоговом окне Подключение ATP для защитника Windows включите параметр подключиться к Windows ATP.</span><span class="sxs-lookup"><span data-stu-id="ad925-122">In the Windows Defender ATP connection dialog box, turn on Connect to Windows ATP.</span></span><br>![Подключение ATP для защитника Windows](media/Explorer-WDATPConnection-dialog.png)<br>
    
5. <span data-ttu-id="ad925-p104">Включите подключение в Advanced Threat Protection в Защитнике Windows. [Используйте портал Advanced Threat Protection в Защитнике Windows](https://go.microsoft.com/fwlink/?linkid=859690).</span><span class="sxs-lookup"><span data-stu-id="ad925-p104">Enable the connection in Windows Defender Advanced Threat Protection. See [Use the Windows Defender Advanced Threat Protection portal](https://go.microsoft.com/fwlink/?linkid=859690).</span></span>

  
## <a name="related-topics"></a><span data-ttu-id="ad925-126">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="ad925-126">Related topics</span></span>

[<span data-ttu-id="ad925-127">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="ad925-127">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  
[<span data-ttu-id="ad925-128">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ad925-128">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

