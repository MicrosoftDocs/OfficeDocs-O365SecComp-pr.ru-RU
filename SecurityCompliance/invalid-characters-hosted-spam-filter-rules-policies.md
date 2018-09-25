---
title: Избегайте недопустимые символы в вашей правил фильтрации нежелательной почты и политики фильтрации нежелательной почты
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Содержит справочную информацию для администраторов, которые имеют недопустимые символы в их конфигурации защиты от нежелательной почты и работе возникли проблемы при попытке использовать безопасности &amp; центре соответствия требованиям.
ms.openlocfilehash: ca409b4daa7bec01417adb7cbfdfa2a128929e81
ms.sourcegitcommit: c168410974bc90aaf55f1dcaa9e05c09b2b78d76
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/25/2018
ms.locfileid: "25018738"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="61f88-103">Избегайте недопустимые символы в правилах фильтра нежелательной почты и политики фильтрации нежелательной почты</span><span class="sxs-lookup"><span data-stu-id="61f88-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="61f88-p101">Ранее Office 365 для администраторов и настроив правил фильтрации нежелательной почты и политики фильтрации нежелательной почты с помощью центра администрирования Exchange (EAC). Теперь, используйте безопасности &amp; центре соответствия требованиям для управления конфигурации защиты от нежелательной почты. Следующие символы поддерживаются в центре администрирования Exchange, но не поддерживаются для использования в безопасности &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="61f88-p101">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange Admin Center (EAC). Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration. The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="61f88-107">**Недопустимые символы:**</span><span class="sxs-lookup"><span data-stu-id="61f88-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="61f88-108">Если ваше правил фильтрации нежелательной почты или политики фильтрации нежелательной почты содержит недопустимые символы, может появиться некоторые или все следующие проблемы:</span><span class="sxs-lookup"><span data-stu-id="61f88-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="61f88-109">Не удается найти политики или правил в системы &amp; центре соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="61f88-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="61f88-110">Вы можете получить ошибки при попытке получить правила или политики с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61f88-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="61f88-111">Может оказаться, что политики или параметры не запустите или как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="61f88-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="61f88-112">Удалить недопустимые символы из политики фильтрации нежелательной почты и правила</span><span class="sxs-lookup"><span data-stu-id="61f88-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="61f88-113">После определения политики и правила, которые содержат недопустимые символы, можно изменить имена с помощью командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="61f88-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="61f88-114">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="61f88-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>
    
2. <span data-ttu-id="61f88-115">Чтобы изменить имя политики фильтрации нежелательной почты, выполните командлет Set-HostedContentFilterPolicy следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61f88-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="61f88-116">Чтобы изменить имя правила фильтрации нежелательной почты, выполните командлет Set-HostedContentFilterRule следующим образом:</span><span class="sxs-lookup"><span data-stu-id="61f88-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="61f88-117">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="61f88-117">For more information</span></span>

[<span data-ttu-id="61f88-118">Угроз управления в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="61f88-118">Threat management in the Security &amp; Compliance Center</span></span>](threat-management.md)
  
[<span data-ttu-id="61f88-119">SET-HostedContentFilterPolicy</span><span class="sxs-lookup"><span data-stu-id="61f88-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy?view=exchange-ps)

[<span data-ttu-id="61f88-120">SET-HostedContentFilterRule</span><span class="sxs-lookup"><span data-stu-id="61f88-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule?view=exchange-ps)
