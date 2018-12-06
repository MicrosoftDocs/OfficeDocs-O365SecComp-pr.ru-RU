---
title: Включение и отключение советов по безопасности в Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7
description: Сведения о Office 365 и EOP "Администраторы" Включить и отключить советы по безопасности в сообщениях электронной почты.
ms.openlocfilehash: 8e5d8bf1d2f831b5d74ca3accd8b434519bfeaab
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180859"
---
# <a name="enable-or-disable-safety-tips-in-office-365"></a><span data-ttu-id="14fb9-103">Включение и отключение советов по безопасности в Office 365</span><span class="sxs-lookup"><span data-stu-id="14fb9-103">Enable or disable safety tips in Office 365</span></span>

<span data-ttu-id="14fb9-p101">Добавляет Exchange Online Protection (EOP) или штампы, безопасность подсказки для сообщений электронной почты, которые он обеспечивает. Эти советы по безопасности предоставляют получателей быстрого, visual позволяют определить, является ли сообщение от safe проверки отправителя, если сообщение было помечено как нежелательная почта с Office 365, если сообщение содержит то, что-то подозрительные, такие как мошенничество или иметь внешние изображения заблокировано. Office 365 и "Администраторы" изолированная EOP можно изменить параметр политики нежелательной почты, чтобы включить или отключить советы по безопасности не будет отображаться в электронной почты в Outlook и другие клиенты настольных систем электронной почты.</span><span class="sxs-lookup"><span data-stu-id="14fb9-p101">Exchange Online Protection (EOP) adds, or stamps, a safety tip to email messages that it delivers. These safety tips provide recipients with a quick, visual way to determine if a message is from a safe, verified sender, if the message has been marked as spam by Office 365, if the message contains something suspicious such as a phishing scam, or if external images have been blocked. Office 365 and EOP-standalone admins can edit a spam policy setting to enable or disable safety tips from being displayed in email in Outlook and other desktop email clients.</span></span> 
  
<span data-ttu-id="14fb9-p102">Office 365 включает советы по безопасности по умолчанию для вашей организации и рекомендуется оставить их включить, чтобы помочь борьбы с нежелательной почты и фишинга атаки. Невозможно отключить советы по безопасности для Outlook в Интернете.</span><span class="sxs-lookup"><span data-stu-id="14fb9-p102">Office 365 enables safety tips by default for your organization and we recommend that you leave them enabled to help combat spam and phishing attacks. You can't disable safety tips for Outlook on the web.</span></span>
  
<span data-ttu-id="14fb9-109">Чтобы просмотреть примеры и сведения о данных, отображаемых в советы по безопасности, увидеть [Советы по безопасности в сообщениях электронной почты в Office 365.](safety-tips-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="14fb9-109">To see examples and to learn about the information displayed in safety tips, see [Safety tips in email messages in Office 365.](safety-tips-in-office-365.md)</span></span>
  
<span data-ttu-id="14fb9-110">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="14fb9-110">In this topic:</span></span>
  
- [<span data-ttu-id="14fb9-111">Чтобы включить или отключить советы по безопасности с помощью Office 365 безопасность &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="14fb9-111">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [<span data-ttu-id="14fb9-112">Чтобы включить или отключить советы по безопасности с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="14fb9-112">To enable or disable safety tips by using PowerShell</span></span>](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="14fb9-113">Чтобы включить или отключить советы по безопасности с помощью Office 365 безопасность &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="14fb9-113">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>
<span data-ttu-id="14fb9-114"><a name="SandCCsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="14fb9-114"></span></span>

1. <span data-ttu-id="14fb9-115">Перейдите по ссылке [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="14fb9-115">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="14fb9-116">Войдите в Office 365 с помощью своей рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="14fb9-116">Sign in to Office 365 with your work or school account.</span></span>
    
3. <span data-ttu-id="14fb9-117">Выберите **Threat Management** \> **политики**.</span><span class="sxs-lookup"><span data-stu-id="14fb9-117">Choose **Threat Management** \> **Policy**.</span></span> 
    
4. <span data-ttu-id="14fb9-118">На странице " **Политика** " выберите **защиты от нежелательной почты**.</span><span class="sxs-lookup"><span data-stu-id="14fb9-118">On the **Policy** page, choose **Anti-Spam**.</span></span>
    
    ![На этом снимке экрана показано, как получить на страницу параметров защиты от нежелательной почты в системы &amp; центре соответствия требованиям.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. <span data-ttu-id="14fb9-120">На странице " **Параметры защиты от нежелательной почты** " выберите вкладку **настраиваемые** .</span><span class="sxs-lookup"><span data-stu-id="14fb9-120">On the **Anti-spam settings** page choose the **Custom** tab.</span></span> 
    
    ![На этом снимке экрана показано расположение вкладку настраиваемые на странице параметров защиты от нежелательной почты в системы &amp; центре соответствия требованиям.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. <span data-ttu-id="14fb9-p103">При необходимости выберите переключатель **пользовательские параметры** для включения пользовательских параметров. Если параметр пользовательских параметров — это значение **отключено**, нельзя будет для изменения политик фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="14fb9-p103">If necessary, choose the **Custom settings** switch to turn on custom settings. If the custom settings switch is set to **Off**, you won't be able to modify spam filter policies.</span></span>
    
    ![В этом снимке экрана показан настраиваемый фильтр нежелательной почты отключить параметры политики.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. <span data-ttu-id="14fb9-p104">Разверните узел нежелательной почты политику, которую требуется изменить, а затем выберите команду **изменить политику**. Например нажмите стрелку вниз рядом с пунктом **политики фильтрации нежелательной почты по умолчанию**. Или, если вы хотите, можно создать новую политику, выбрав **Добавить политику**.</span><span class="sxs-lookup"><span data-stu-id="14fb9-p104">Expand the spam policy you want to modify and then choose **Edit policy**. For example, choose the down arrow next to **Default spam filter policy**. Or, if you want, you can create a new policy by choosing **Add a policy**.</span></span>
    
8. <span data-ttu-id="14fb9-128">Разверните узел **нежелательной почты и массовых** действия.</span><span class="sxs-lookup"><span data-stu-id="14fb9-128">Expand **Spam and bulk** actions.</span></span> 
    
9. <span data-ttu-id="14fb9-p105">Чтобы включить советы по безопасности, в разделе **Советы по безопасности**, установите флажок **на** . Чтобы отключить советы по безопасности, снимите флажок **на** .</span><span class="sxs-lookup"><span data-stu-id="14fb9-p105">To enable safety tips, under **Safety Tips**, check the **On** checkbox. To disable safety tips, clear the **On** checkbox.</span></span> 
    
10. <span data-ttu-id="14fb9-131">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="14fb9-131">Choose **Save**.</span></span>
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a><span data-ttu-id="14fb9-132">Чтобы включить или отключить советы по безопасности с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="14fb9-132">To enable or disable safety tips by using PowerShell</span></span>
<span data-ttu-id="14fb9-133"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="14fb9-133"></span></span>

<span data-ttu-id="14fb9-p106">Администраторы могут использовать Exchange Online PowerShell, чтобы включить или отключить советы по безопасности. Командлет Set-HostedContentFilterPolicy используется для включения или отключения советы по безопасности в политике фильтров нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="14fb9-p106">Admins can use Exchange Online PowerShell to enable or disable safety tips. Use the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips in a spam filter policy.</span></span>
  
1. <span data-ttu-id="14fb9-p107">Подключение к Exchange Online PowerShell. Сведения можно [Подключить к Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="14fb9-p107">Connect to Exchange Online PowerShell. For information, see [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="14fb9-138">Выполните командлет Set-HostedContentFilterPolicy, чтобы включить или отключить советы по безопасности:</span><span class="sxs-lookup"><span data-stu-id="14fb9-138">Run the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips:</span></span>
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

<span data-ttu-id="14fb9-139">Где:</span><span class="sxs-lookup"><span data-stu-id="14fb9-139">Where:</span></span>
    
  -  <span data-ttu-id="14fb9-140">*Имя политики* — это имя политики, которую требуется изменить, например **по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="14fb9-140">*policy name*  is the name of the policy you want to modify, for example **default**.</span></span>
    
  -  <span data-ttu-id="14fb9-141">`$true`Включение советы по безопасности для политики фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="14fb9-141">`$true` enables safety tips for the spam filter policy.</span></span> 
    
  -  <span data-ttu-id="14fb9-142">`$false`Отключает советы по безопасности для политики фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="14fb9-142">`$false` disables safety tips for the spam filter policy.</span></span> 
    
    <span data-ttu-id="14fb9-143">Например чтобы отключить советы по безопасности для политики фильтрации нежелательной почты по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="14fb9-143">For example, to disable safety tips for the default spam filter policy, run the following command:</span></span>
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

<span data-ttu-id="14fb9-144">Дополнительные сведения о этот командлет [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="14fb9-144">For more information about this cmdlet, see [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span></span>
    
## <a name="still-need-help"></a><span data-ttu-id="14fb9-145">Есть дополнительные вопросы?</span><span class="sxs-lookup"><span data-stu-id="14fb9-145">Still need help?</span></span>
<span data-ttu-id="14fb9-146"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="14fb9-146"></span></span>

<span data-ttu-id="14fb9-147">Если вы отключены советы по безопасности, но по-прежнему отображается их в сообщениях электронной почты, проверьте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="14fb9-147">If you disabled safety tips but are still seeing them in your email messages, check these things:</span></span>
  
- <span data-ttu-id="14fb9-p108">Невозможно отключить советы по безопасности для Outlook в Интернете. Повторите попытку же сообщение электронной почты в другой клиентом, например Outlook.</span><span class="sxs-lookup"><span data-stu-id="14fb9-p108">You can't disable safety tips for Outlook on the web. Try viewing the same email in another client, such as Outlook.</span></span>
    
- <span data-ttu-id="14fb9-p109">Советы по безопасности включены по умолчанию для всех пользователей, которые использует EOP, включая всем пользователям, имеющим Office 365. Чтобы отключить советы по безопасности от отображенной в электронной почты, необходимо отключить их с помощью политики фильтрации нежелательной почты, как описано в этом разделе. После настройки политики, убедитесь, что он включен. Сведения о включении политик фильтрации нежелательной почты в разделе [Настройка политик фильтрации нежелательной почты](https://technet.microsoft.com/library/jj200684.aspx).</span><span class="sxs-lookup"><span data-stu-id="14fb9-p109">Safety tips are on by default for every one who uses EOP, this includes everyone who has Office 365. In order to disable safety tips from showing up in email, you must disable them by using a spam filter policy as described in this topic. Once you've set up the policy, ensure that it is enabled. For information on enabling spam filter policies, see [Configure your spam filter policies](https://technet.microsoft.com/library/jj200684.aspx).</span></span>
    
<span data-ttu-id="14fb9-154">Дополнительные способы борьбы с нежелательной почты и фишинга в разделе [Защита от нежелательной почты Office 365](anti-spam-protection.md).</span><span class="sxs-lookup"><span data-stu-id="14fb9-154">For more ways to combat spam and phishing, see [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span></span>
  

