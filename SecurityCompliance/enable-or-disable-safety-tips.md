---
<span data-ttu-id="e229c-101">Title: "Включение или отключение советов по безопасности в Office 365" MS. author: кровлэй author: кккросс Manager: лаурави MS. Date: 12/05/2018 МС. аудитория: MS. Topic: статья MS. Service: O365 — администрирование локализатион_приорити: обычный поиск. аппверид:</span><span class="sxs-lookup"><span data-stu-id="e229c-101">title: "Enable or disable safety tips in Office 365" ms.author: krowley author: kccross manager: laurawi ms.date: 12/05/2018 ms.audience: Admin ms.topic: article ms.service: o365-administration localization_priority: Normal search.appverid:</span></span> 
- <span data-ttu-id="e229c-102">MET150 MS. ассетид: f09668bd-fe1a-4c01-89e3-e88c370e66c7 MS. Collection:</span><span class="sxs-lookup"><span data-stu-id="e229c-102">MET150 ms.assetid: f09668bd-fe1a-4c01-89e3-e88c370e66c7   ms.collection:</span></span>
    - <span data-ttu-id="e229c-103">M365 — описание соответствия требованиям безопасности: "сообщает администраторам Office 365 и EOP о том, как включать и отключать советы по безопасности в сообщениях электронной почты."</span><span class="sxs-lookup"><span data-stu-id="e229c-103">M365-security-compliance description: "Tells Office 365 and EOP admins how to enable and disable safety tips in email messages."</span></span>
---

# <a name="enable-or-disable-safety-tips-in-office-365"></a><span data-ttu-id="e229c-104">Включение и отключение советов по безопасности в Office 365</span><span class="sxs-lookup"><span data-stu-id="e229c-104">Enable or disable safety tips in Office 365</span></span>

<span data-ttu-id="e229c-105">Exchange Online Protection (EOP) добавляет (или отметок) подсказку безопасности к сообщениям электронной почты, которые она предоставляет.</span><span class="sxs-lookup"><span data-stu-id="e229c-105">Exchange Online Protection (EOP) adds, or stamps, a safety tip to email messages that it delivers.</span></span> <span data-ttu-id="e229c-106">Эти советы по обеспечению безопасности предоставляют получателям быстрый, визуальный способ определения того, находится ли сообщение из надежного, проверенного отправителя, если сообщение помечено как нежелательная почта в Office 365, если сообщение содержит что-нибудь подозрительные, например фишинг или внешние изображения заблокирована.</span><span class="sxs-lookup"><span data-stu-id="e229c-106">These safety tips provide recipients with a quick, visual way to determine if a message is from a safe, verified sender, if the message has been marked as spam by Office 365, if the message contains something suspicious such as a phishing scam, or if external images have been blocked.</span></span> <span data-ttu-id="e229c-107">Office 365 и EOP — автономные администраторы могут редактировать параметр политики спама, чтобы включить или отключить отображение советов по безопасности в электронной почте в Outlook и других почтовых клиентах для настольных ПК.</span><span class="sxs-lookup"><span data-stu-id="e229c-107">Office 365 and EOP-standalone admins can edit a spam policy setting to enable or disable safety tips from being displayed in email in Outlook and other desktop email clients.</span></span> 
  
<span data-ttu-id="e229c-108">Office 365 предоставляет советы по безопасности по умолчанию для вашей организации, и мы рекомендуем оставить их включенными для борьбы с нежелательной почтой и фишингом.</span><span class="sxs-lookup"><span data-stu-id="e229c-108">Office 365 enables safety tips by default for your organization and we recommend that you leave them enabled to help combat spam and phishing attacks.</span></span> <span data-ttu-id="e229c-109">Вы не можете отключить советы по безопасности для Outlook в Интернете.</span><span class="sxs-lookup"><span data-stu-id="e229c-109">You can't disable safety tips for Outlook on the web.</span></span>
  
<span data-ttu-id="e229c-110">Чтобы просмотреть примеры и ознакомиться со сведениями, отображаемыми в подсказках по безопасности, ознакомьтесь со статьями [по безопасности в сообщениях электронной почты в Office 365.](safety-tips-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="e229c-110">To see examples and to learn about the information displayed in safety tips, see [Safety tips in email messages in Office 365.](safety-tips-in-office-365.md)</span></span>
  
<span data-ttu-id="e229c-111">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="e229c-111">In this topic:</span></span>
  
- [<span data-ttu-id="e229c-112">Включение и отключение советов по безопасности с помощью центра безопасности &amp; Office 365</span><span class="sxs-lookup"><span data-stu-id="e229c-112">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>](enable-or-disable-safety-tips.md#SandCCsafetytip)
    
- [<span data-ttu-id="e229c-113">Включение и отключение советов по безопасности с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="e229c-113">To enable or disable safety tips by using PowerShell</span></span>](enable-or-disable-safety-tips.md#pshellsafetytip)
    
## <a name="to-enable-or-disable-safety-tips-by-using-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="e229c-114">Включение и отключение советов по безопасности с помощью центра безопасности &amp; Office 365</span><span class="sxs-lookup"><span data-stu-id="e229c-114">To enable or disable safety tips by using the Office 365 Security &amp; Compliance Center</span></span>
<span data-ttu-id="e229c-115"><a name="SandCCsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="e229c-115"></span></span>

1. <span data-ttu-id="e229c-116">Перейдите по ссылке [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="e229c-116">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="e229c-117">Войдите в Office 365 с помощью своей рабочей или учебной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e229c-117">Sign in to Office 365 with your work or school account.</span></span>
    
3. <span data-ttu-id="e229c-118">Выберите **Политика** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="e229c-118">Choose **Threat Management** \> **Policy**.</span></span> 
    
4. <span data-ttu-id="e229c-119">На странице **Политика** выберите пункт **Защита от нежелательной почты**.</span><span class="sxs-lookup"><span data-stu-id="e229c-119">On the **Policy** page, choose **Anti-Spam**.</span></span>
    
    ![На этом снимке экрана показано, как получить страницу параметров защиты от нежелательной &amp; почты в центре безопасности и соответствия требованиям.](media/b8eb2ee3-2eb1-4ea2-b138-f6d7fb2e23de.png)
  
5. <span data-ttu-id="e229c-121">На странице " **Параметры защиты от нежелательной почты** " выберите вкладку **Настраиваемая** .</span><span class="sxs-lookup"><span data-stu-id="e229c-121">On the **Anti-spam settings** page choose the **Custom** tab.</span></span> 
    
    ![На этом снимке экрана показано расположение настраиваемой вкладки на странице параметров защиты от нежелательной почты &amp; в центре безопасности и соответствия требованиям.](media/1d688d23-e6f3-4de5-84a7-e8ce31786193.png)
  
6. <span data-ttu-id="e229c-123">При необходимости выберите параметр **Настраиваемые параметры** , чтобы включить настраиваемые параметры.</span><span class="sxs-lookup"><span data-stu-id="e229c-123">If necessary, choose the **Custom settings** switch to turn on custom settings.</span></span> <span data-ttu-id="e229c-124">Если параметр Custom Settings имеет значение " **отключено**", изменение политик фильтрации нежелательной почты невозможно.</span><span class="sxs-lookup"><span data-stu-id="e229c-124">If the custom settings switch is set to **Off**, you won't be able to modify spam filter policies.</span></span>
    
    ![На этом снимке экрана показаны пользовательские параметры политики фильтрации нежелательной почты.](media/94f900ad-b556-4a31-a3ac-acfcd72e71b8.png)
  
7. <span data-ttu-id="e229c-126">Разверните политику нежелательной почты, которую необходимо изменить, а затем выберите команду **изменить политику**.</span><span class="sxs-lookup"><span data-stu-id="e229c-126">Expand the spam policy you want to modify and then choose **Edit policy**.</span></span> <span data-ttu-id="e229c-127">Например, нажмите стрелку вниз рядом с **политикой фильтрации нежелательной почты по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e229c-127">For example, choose the down arrow next to **Default spam filter policy**.</span></span> <span data-ttu-id="e229c-128">Или, при желании, можно создать новую политику, выбрав **Добавить политику**.</span><span class="sxs-lookup"><span data-stu-id="e229c-128">Or, if you want, you can create a new policy by choosing **Add a policy**.</span></span>
    
8. <span data-ttu-id="e229c-129">Развертывание **нежелательных и массовых** действий.</span><span class="sxs-lookup"><span data-stu-id="e229c-129">Expand **Spam and bulk** actions.</span></span> 
    
9. <span data-ttu-id="e229c-130">Чтобы включить советы по безопасности, в разделе **Советы по обеспечению безопасности**установите флажок **вкл** .</span><span class="sxs-lookup"><span data-stu-id="e229c-130">To enable safety tips, under **Safety Tips**, check the **On** checkbox.</span></span> <span data-ttu-id="e229c-131">Чтобы отключить советы по безопасности, снимите флажок **вкл** .</span><span class="sxs-lookup"><span data-stu-id="e229c-131">To disable safety tips, clear the **On** checkbox.</span></span> 
    
10. <span data-ttu-id="e229c-132">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e229c-132">Choose **Save**.</span></span>
    
## <a name="to-enable-or-disable-safety-tips-by-using-powershell"></a><span data-ttu-id="e229c-133">Включение и отключение советов по безопасности с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="e229c-133">To enable or disable safety tips by using PowerShell</span></span>
<span data-ttu-id="e229c-134"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="e229c-134"></span></span>

<span data-ttu-id="e229c-135">Администраторы могут использовать Exchange Online PowerShell для включения или отключения советов по безопасности.</span><span class="sxs-lookup"><span data-stu-id="e229c-135">Admins can use Exchange Online PowerShell to enable or disable safety tips.</span></span> <span data-ttu-id="e229c-136">Используйте командлет Set – HostedContentFilterPolicy для включения или отключения советов по безопасности в политике фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="e229c-136">Use the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips in a spam filter policy.</span></span>
  
1. <span data-ttu-id="e229c-137">Подключение к Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e229c-137">Connect to Exchange Online PowerShell.</span></span> <span data-ttu-id="e229c-138">Дополнительные сведения можно найти [в статье подключение к Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span><span class="sxs-lookup"><span data-stu-id="e229c-138">For information, see [Connect to Exchange Online PowerShell](http://go.microsoft.com/fwlink/p/?LinkId=396554).</span></span>
    
2. <span data-ttu-id="e229c-139">Выполните командлет Set – HostedContentFilterPolicy, чтобы включить или отключить советы по безопасности:</span><span class="sxs-lookup"><span data-stu-id="e229c-139">Run the Set-HostedContentFilterPolicy cmdlet to enable or disable safety tips:</span></span>
    
  ```
  Set-HostedContentFilterPolicy -Identity "policy name " -InlineSafetyTipsEnabled <$true|$false>
  ```

<span data-ttu-id="e229c-140">Где:</span><span class="sxs-lookup"><span data-stu-id="e229c-140">Where:</span></span>
    
  -  <span data-ttu-id="e229c-141">*имя политики* — это имя политики, которую вы хотите изменить, например **по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="e229c-141">*policy name*  is the name of the policy you want to modify, for example **default**.</span></span>
    
  -  <span data-ttu-id="e229c-142">`$true`включает советы по безопасности для политики фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="e229c-142">`$true` enables safety tips for the spam filter policy.</span></span> 
    
  -  <span data-ttu-id="e229c-143">`$false`отключает советы по безопасности для политики фильтрации нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="e229c-143">`$false` disables safety tips for the spam filter policy.</span></span> 
    
    <span data-ttu-id="e229c-144">Например, чтобы отключить советы по безопасности для политики фильтрации нежелательной почты по умолчанию, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e229c-144">For example, to disable safety tips for the default spam filter policy, run the following command:</span></span>
    
  ```
  PS C:\> Set-HostedContentFilterPolicy -Identity "default" -InlineSafetyTipsEnabled $false
  ```

<span data-ttu-id="e229c-145">Дополнительные сведения об этом командлете приведены в разделе [Set – HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span><span class="sxs-lookup"><span data-stu-id="e229c-145">For more information about this cmdlet, see [Set-HostedContentFilterPolicy](https://technet.microsoft.com/library/jj200781.aspx).</span></span>
    
## <a name="still-need-help"></a><span data-ttu-id="e229c-146">Есть дополнительные вопросы?</span><span class="sxs-lookup"><span data-stu-id="e229c-146">Still need help?</span></span>
<span data-ttu-id="e229c-147"><a name="pshellsafetytip"> </a></span><span class="sxs-lookup"><span data-stu-id="e229c-147"></span></span>

<span data-ttu-id="e229c-148">Если вы отключили советы по безопасности, но не видите их в сообщениях электронной почты, проверьте следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="e229c-148">If you disabled safety tips but are still seeing them in your email messages, check these things:</span></span>
  
- <span data-ttu-id="e229c-149">Вы не можете отключить советы по безопасности для Outlook в Интернете.</span><span class="sxs-lookup"><span data-stu-id="e229c-149">You can't disable safety tips for Outlook on the web.</span></span> <span data-ttu-id="e229c-150">Попробуйте просмотреть одну и ту же электронную почту в другом клиенте, например Outlook.</span><span class="sxs-lookup"><span data-stu-id="e229c-150">Try viewing the same email in another client, such as Outlook.</span></span>
    
- <span data-ttu-id="e229c-151">Советы по безопасности включены по умолчанию для всех пользователей, использующих EOP, это включает в себя всех пользователей Office 365.</span><span class="sxs-lookup"><span data-stu-id="e229c-151">Safety tips are on by default for every one who uses EOP, this includes everyone who has Office 365.</span></span> <span data-ttu-id="e229c-152">Для отключения советов по безопасности в электронной почте необходимо отключить их, используя политику фильтрации нежелательной почты, как описано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="e229c-152">In order to disable safety tips from showing up in email, you must disable them by using a spam filter policy as described in this topic.</span></span> <span data-ttu-id="e229c-153">После настройки политики убедитесь, что она включена.</span><span class="sxs-lookup"><span data-stu-id="e229c-153">Once you've set up the policy, ensure that it is enabled.</span></span> <span data-ttu-id="e229c-154">Сведения о включении политик фильтрации нежелательной почты приведены в разделе [Настройка политик фильтрации](https://technet.microsoft.com/library/jj200684.aspx)нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="e229c-154">For information on enabling spam filter policies, see [Configure your spam filter policies](https://technet.microsoft.com/library/jj200684.aspx).</span></span>
    
<span data-ttu-id="e229c-155">Дополнительные способы борьбы с нежелательной почтой и фишингом можно найти в статье [Office 365 защита от](anti-spam-protection.md)нежелательной почты.</span><span class="sxs-lookup"><span data-stu-id="e229c-155">For more ways to combat spam and phishing, see [Office 365 Email Anti-Spam Protection](anti-spam-protection.md).</span></span>
  

