---
title: Имитатор атак в Office 365
ms.author: chrisda
author: chrisda
manager: dansimp
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
ms.collection:
- M365-security-compliance
description: В качестве глобального администратора Office 365 вы можете использовать Симуляторы для атаки, чтобы выполнять реальные сценарии атак в Организации. Это поможет определить и найти уязвимых пользователей, прежде чем реальная атака будет возобновлением вашей компании.
ms.openlocfilehash: e72350fb8ca3ef8d7ed0218934097d2383f5ad53
ms.sourcegitcommit: ff370e93b792204547694139ef99bc0848304570
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/11/2019
ms.locfileid: "36852781"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="eef5a-104">Имитатор атак в Office 365</span><span class="sxs-lookup"><span data-stu-id="eef5a-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="eef5a-105">**Сводка** Если вы являетесь глобальным администратором Office 365 или администратором системы безопасности и у вашей организации есть Office 365 Advanced Threat Protection Plan 2, который включает [функции расследования и реагирования на угрозы](office-365-ti.md), можно использовать симулятор для запуска сценарии с реалистичной атакой в Организации.</span><span class="sxs-lookup"><span data-stu-id="eef5a-105">**Summary** If you are an Office 365 global administrator or a security administrator and your organization has Office 365 Advanced Threat Protection Plan 2, which includes [Threat Investigation and Response capabilities](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization.</span></span> <span data-ttu-id="eef5a-106">Это поможет определить и найти уязвимых пользователей, прежде чем реальная атака повлияет на нижнюю линию.</span><span class="sxs-lookup"><span data-stu-id="eef5a-106">This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span> <span data-ttu-id="eef5a-107">Ознакомьтесь с этой статьей, чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="eef5a-107">Read this article to learn more.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="eef5a-108">Атаки</span><span class="sxs-lookup"><span data-stu-id="eef5a-108">The Attacks</span></span>

<span data-ttu-id="eef5a-109">В настоящее время доступны три типа имитации атак:</span><span class="sxs-lookup"><span data-stu-id="eef5a-109">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="eef5a-110">Отображаемое имя спеар — Фишинговая атака</span><span class="sxs-lookup"><span data-stu-id="eef5a-110">Display name spear-phishing attack</span></span>](#display-name-spear-phishing-attack)

- [<span data-ttu-id="eef5a-111">Парольная атака с распылителем</span><span class="sxs-lookup"><span data-stu-id="eef5a-111">Password-spray attack</span></span>](#password-spray-attack)

- [<span data-ttu-id="eef5a-112">Принудительная атака пароля методом грубого подбора</span><span class="sxs-lookup"><span data-stu-id="eef5a-112">Brute-force password attack</span></span>](#brute-force-password-attack)
    
<span data-ttu-id="eef5a-113">Для успешного запуска атаки убедитесь, что учетная запись, используемая для запуска имитации атак, использует многофакторную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="eef5a-113">For an attack to be successfully launched, make sure that the account you are using to run simulated attacks is using multi-factor authentication.</span></span> <span data-ttu-id="eef5a-114">Кроме того, вы должны быть глобальным администратором Office 365 или администратором безопасности.</span><span class="sxs-lookup"><span data-stu-id="eef5a-114">In addition, you must be an Office 365 global administrator or a security administrator.</span></span> <span data-ttu-id="eef5a-115">(Дополнительные сведения о ролях и разрешениях см. [в разделе разрешения в центре безопасности Office 365 & соответствия требованиям](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="eef5a-115">(To learn more about roles and permissions, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>
    
<span data-ttu-id="eef5a-116">Чтобы получить доступ к симулятору атак, &amp; в центре безопасности и соответствия требованиям выберите \> **симулятор атак** **управления угрозами** .</span><span class="sxs-lookup"><span data-stu-id="eef5a-116">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="eef5a-117">Перед началом работы...</span><span class="sxs-lookup"><span data-stu-id="eef5a-117">Before you begin...</span></span>

<span data-ttu-id="eef5a-118">Убедитесь, что ваша организация отвечает следующим требованиям для атаки на симулятор:</span><span class="sxs-lookup"><span data-stu-id="eef5a-118">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="eef5a-119">Электронная почта вашей организации размещена в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="eef5a-119">Your organization's email is hosted in Exchange Online.</span></span> <span data-ttu-id="eef5a-120">(Симулятор атак недоступен для локальных почтовых серверов.)</span><span class="sxs-lookup"><span data-stu-id="eef5a-120">(Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="eef5a-121">Вы являетесь глобальным администратором Office 365 или администратором безопасности</span><span class="sxs-lookup"><span data-stu-id="eef5a-121">You are an Office 365 global administrator or security administrator</span></span>
    
- <span data-ttu-id="eef5a-122">[Многофакторная проверка подлинности и условный доступ](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide) включены, по крайней мере для учетной записи глобального администратора Office 365 и администраторам безопасности, которые будут использовать симулятор для атаки.</span><span class="sxs-lookup"><span data-stu-id="eef5a-122">[Multi-factor authentication/Conditional Access](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide) is turned on, for at least the Office 365 global administrator account and security administrators who will be using Attack Simulator.</span></span> <span data-ttu-id="eef5a-123">(В идеале многофакторная проверка подлинности и условный доступ включены для всех пользователей в Организации.)</span><span class="sxs-lookup"><span data-stu-id="eef5a-123">(Ideally, multi-factor authentication/conditional access is turned on for all users in your organization.)</span></span>
 
- <span data-ttu-id="eef5a-124">В вашей организации [имеется Office 365 Advanced Threat protection (план 2](office-365-atp.md)) с симулятором атак, &amp; видимым в центре безопасности и соответствия требованиям (перейти к \> **симулятору атаки** **управления угрозами** )</span><span class="sxs-lookup"><span data-stu-id="eef5a-124">Your organization has [Office 365 Advanced Threat Protection Plan 2](office-365-atp.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span>

    ![Управление угрозами — симулятор атак](media/ThreatMgmt-AttackSimulator.png)

## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="eef5a-126">Отображаемое имя спеар — Фишинговая атака</span><span class="sxs-lookup"><span data-stu-id="eef5a-126">Display name spear-phishing attack</span></span>

<span data-ttu-id="eef5a-127">Фишинг — это универсальный термин для широкого набора атак, предназначенных для атаки со стилем социального проектирования.</span><span class="sxs-lookup"><span data-stu-id="eef5a-127">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack.</span></span> <span data-ttu-id="eef5a-128">Эта атака сосредоточена на phishing-атаках спеар, что более целевая атака предназначена для определенной группы пользователей или организации.</span><span class="sxs-lookup"><span data-stu-id="eef5a-128">This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization.</span></span> <span data-ttu-id="eef5a-129">Как правило, пользовательская атака с некоторым реконнаиссанце выполнена и с использованием отображаемого имени, которое будет создавать доверие для получателя, например сообщение электронной почты, которое выглядит так, как оно было получено от руководителя в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="eef5a-129">Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="eef5a-130">Эта атака нацелена на то, что вы можете управлять тем, кто поступил с сообщениями, изменив отображаемое имя и адрес источника.</span><span class="sxs-lookup"><span data-stu-id="eef5a-130">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address.</span></span> <span data-ttu-id="eef5a-131">Когда спеар-фишинг будет успешным, цибераттаккерс получить доступ к учетным данным пользователей.</span><span class="sxs-lookup"><span data-stu-id="eef5a-131">When spear-phishing attacks are successful, cyberattackers gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="eef5a-132">Имитация атаки спеар-фишинга</span><span class="sxs-lookup"><span data-stu-id="eef5a-132">To simulate a spear-phishing attack</span></span>

![Создание сообщения электронной почты](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="eef5a-134">Вы можете создавать редактор форматированного HTML-кода непосредственно в самом поле **текста сообщения электронной почты** или работать с HTML-кодом.</span><span class="sxs-lookup"><span data-stu-id="eef5a-134">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="eef5a-135">В [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)выберите **симулятор для атак** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="eef5a-135">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="eef5a-136">Укажите понятное имя кампании для атаки или выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="eef5a-136">Specify a meaningful campaign name for the attack or select a template.</span></span> 

    ![Страница "начало фишинга"](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="eef5a-138">Укажите получателей назначения.</span><span class="sxs-lookup"><span data-stu-id="eef5a-138">Specify the target recipients.</span></span> <span data-ttu-id="eef5a-139">Это могут быть отдельные пользователи или группы в Организации.</span><span class="sxs-lookup"><span data-stu-id="eef5a-139">This can be individuals or groups in your organization.</span></span> <span data-ttu-id="eef5a-140">Чтобы атака достигла успеха, у каждого целевого получателя должен быть почтовый ящик Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="eef5a-140">Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> 

    ![Выбор получателей](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="eef5a-142">Настройте сведения об фишинговых сообщениях.</span><span class="sxs-lookup"><span data-stu-id="eef5a-142">Configure the Phishing email details.</span></span> 

    ![Настройка сведений об электронной почте](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
    
    <span data-ttu-id="eef5a-144">Форматирование HTML может быть как сложным, так и базовым по отношению к потребностям кампании.</span><span class="sxs-lookup"><span data-stu-id="eef5a-144">The HTML formatting can be as complex or basic as your campaign needs.</span></span> <span data-ttu-id="eef5a-145">Как и формат электронной почты HTML, вы можете вставить изображения и текст, чтобы улучшить белиевабилити.</span><span class="sxs-lookup"><span data-stu-id="eef5a-145">As the email format is HTML, you can insert images and text to enhance believability.</span></span> <span data-ttu-id="eef5a-146">Вы можете управлять тем, как будет выглядеть полученное сообщение в принимающем почтовом клиенте.</span><span class="sxs-lookup"><span data-stu-id="eef5a-146">You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="eef5a-147">Укажите текст для поля " **от" (имя)** .</span><span class="sxs-lookup"><span data-stu-id="eef5a-147">Specify text for the **From (Name)** field.</span></span> <span data-ttu-id="eef5a-148">Это поле показывается в **отображаемом имени** принимающего почтового клиента.</span><span class="sxs-lookup"><span data-stu-id="eef5a-148">This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="eef5a-149">Укажите текст или поле " **от** ".</span><span class="sxs-lookup"><span data-stu-id="eef5a-149">Specify text or the **From** field.</span></span> <span data-ttu-id="eef5a-150">Это поле, которое отображается в качестве адреса электронной почты отправителя в принимающем почтовом клиенте.</span><span class="sxs-lookup"><span data-stu-id="eef5a-150">This is the field that shows as the email address of the sender in the receiving email client.</span></span>

    <span data-ttu-id="eef5a-151">Вы можете ввести существующее пространство имен электронной почты в своей организации (это сделает адрес электронной почты действительно в принимающем клиенте, который упрощает модель доверенности), или вы можете ввести внешний адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="eef5a-151">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address.</span></span> <span data-ttu-id="eef5a-152">Указанный адрес электронной почты не обязательно должен существовать, но необходимо отформатировать допустимый SMTP-адрес, например: `user@domainname.extension`.</span><span class="sxs-lookup"><span data-stu-id="eef5a-152">The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as `user@domainname.extension`.</span></span> 
  
7. <span data-ttu-id="eef5a-153">В раскрывающемся списке выберите URL-адрес сервера фишингового входа, который отражает тип контента, который будет находиться в вашей атаке.</span><span class="sxs-lookup"><span data-stu-id="eef5a-153">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack.</span></span> <span data-ttu-id="eef5a-154">Можно выбрать несколько URL-адресов с темой, таких как доставка документов, техническая, зарплата и т. д. Это фактически URL-адрес, по которому пользователям предлагается щелкнуть.</span><span class="sxs-lookup"><span data-stu-id="eef5a-154">Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="eef5a-155">Укажите URL-адрес настраиваемой целевой страницы.</span><span class="sxs-lookup"><span data-stu-id="eef5a-155">Specify a custom landing page URL.</span></span> <span data-ttu-id="eef5a-156">При этом пользователи будут перенаправляться на URL-адрес, указанный в конце успешной атаки.</span><span class="sxs-lookup"><span data-stu-id="eef5a-156">Using this will redirect users to a URL you specify at the end of a successful attack.</span></span> <span data-ttu-id="eef5a-157">Если у вас есть обучение по внутренней осведомленности, например, вы можете указать здесь.</span><span class="sxs-lookup"><span data-stu-id="eef5a-157">If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="eef5a-158">Укажите текст для поля **subject** .</span><span class="sxs-lookup"><span data-stu-id="eef5a-158">Specify text for the **Subject** field.</span></span> <span data-ttu-id="eef5a-159">Это поле, которое отображается в качестве **имени субъекта** в принимающем почтовом клиенте.</span><span class="sxs-lookup"><span data-stu-id="eef5a-159">This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="eef5a-160">Создайте **текст сообщения электронной почты** , который будет получать целевой объект.</span><span class="sxs-lookup"><span data-stu-id="eef5a-160">Compose the **Email body** that the target will receive.</span></span> 

    <span data-ttu-id="eef5a-161">`${username}`Вставляет имя целевого значения в текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="eef5a-161">`${username}` inserts the targets name into the Email body.</span></span> 

    <span data-ttu-id="eef5a-162">`${loginserverurl}`вставляет URL-адрес, по которому будут щелкать конечные пользователи</span><span class="sxs-lookup"><span data-stu-id="eef5a-162">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="eef5a-163">Нажмите кнопку **Далее,** а затем кнопку **Готово** , чтобы запустить атаку.</span><span class="sxs-lookup"><span data-stu-id="eef5a-163">Choose **Next,** then **Finish** to launch the attack.</span></span> <span data-ttu-id="eef5a-164">Phishing-сообщения электронной почты спеар доставляются в почтовые ящики целевых получателей.</span><span class="sxs-lookup"><span data-stu-id="eef5a-164">The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="eef5a-165">Парольная атака с распылителем</span><span class="sxs-lookup"><span data-stu-id="eef5a-165">Password-spray attack</span></span>

<span data-ttu-id="eef5a-166">Использование распылителя пароля в организации обычно используется после того, как ошибочный субъект успешно получил список действительных пользователей от клиента.</span><span class="sxs-lookup"><span data-stu-id="eef5a-166">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant.</span></span> <span data-ttu-id="eef5a-167">Неверный субъект знает об общих паролях, используемых пользователями.</span><span class="sxs-lookup"><span data-stu-id="eef5a-167">The bad actor knows about common passwords that people use.</span></span> <span data-ttu-id="eef5a-168">Это широко используемая атака, так как она является дешевой атакой и сложнее, чем методы грубой силы.</span><span class="sxs-lookup"><span data-stu-id="eef5a-168">This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="eef5a-169">Эта атака фокусируется на том, что вы указываете общий пароль для большой целевой базы пользователей.</span><span class="sxs-lookup"><span data-stu-id="eef5a-169">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="eef5a-170">Имитация атаки с использованием пароля</span><span class="sxs-lookup"><span data-stu-id="eef5a-170">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="eef5a-171">В [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)выберите **симулятор для атак** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="eef5a-171">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="eef5a-172">Укажите понятное имя кампании для атаки.</span><span class="sxs-lookup"><span data-stu-id="eef5a-172">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="eef5a-173">Укажите получателей назначения.</span><span class="sxs-lookup"><span data-stu-id="eef5a-173">Specify the target recipients.</span></span> <span data-ttu-id="eef5a-174">Это могут быть отдельные пользователи или группы в Организации.</span><span class="sxs-lookup"><span data-stu-id="eef5a-174">This can be individuals or groups in your organization.</span></span> <span data-ttu-id="eef5a-175">Чтобы атака достигла результата, целевой получатель должен иметь почтовый ящик Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="eef5a-175">A targeted recipient must have an Exchange Online mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="eef5a-176">Укажите пароль, который будет использоваться для атаки.</span><span class="sxs-lookup"><span data-stu-id="eef5a-176">Specify a password to use for the attack.</span></span> <span data-ttu-id="eef5a-177">Например, вы можете попытаться использовать один общий, подходящий `Summer2019`пароль.</span><span class="sxs-lookup"><span data-stu-id="eef5a-177">For example, one common, relevant password you could try is `Summer2019`.</span></span> <span data-ttu-id="eef5a-178">Другое может быть `Fall2019`или `Password1`.</span><span class="sxs-lookup"><span data-stu-id="eef5a-178">Another might be `Fall2019`, or `Password1`.</span></span>
    
5. <span data-ttu-id="eef5a-179">Нажмите кнопку **Готово** , чтобы запустить атаку.</span><span class="sxs-lookup"><span data-stu-id="eef5a-179">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="eef5a-180">Принудительная атака пароля методом грубого подбора</span><span class="sxs-lookup"><span data-stu-id="eef5a-180">Brute-force password attack</span></span>

<span data-ttu-id="eef5a-181">Атака с помощью прямого прямого пароля для организации обычно используется после того, как ошибочный субъект успешно получил список ключевых пользователей от клиента.</span><span class="sxs-lookup"><span data-stu-id="eef5a-181">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant.</span></span> <span data-ttu-id="eef5a-182">Эта атака фокусируется на попытке использовать набор паролей для учетной записи одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="eef5a-182">This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="eef5a-183">Имитация атаки с использованием пароля методом грубой силы</span><span class="sxs-lookup"><span data-stu-id="eef5a-183">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="eef5a-184">В [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)выберите **симулятор для атак** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="eef5a-184">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="eef5a-185">Укажите понятное имя кампании для атаки.</span><span class="sxs-lookup"><span data-stu-id="eef5a-185">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="eef5a-186">Укажите целевого получателя.</span><span class="sxs-lookup"><span data-stu-id="eef5a-186">Specify the target recipient.</span></span> <span data-ttu-id="eef5a-187">Чтобы атака достигла результата, целевой получатель должен иметь почтовый ящик Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="eef5a-187">A targeted recipient must have an Exchange Online mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="eef5a-188">Укажите набор паролей, который будет использоваться для атаки.</span><span class="sxs-lookup"><span data-stu-id="eef5a-188">Specify a set of passwords to use for the attack.</span></span> <span data-ttu-id="eef5a-189">Для этого можно использовать текстовый файл (txt) для списка паролей.</span><span class="sxs-lookup"><span data-stu-id="eef5a-189">To do this, you can use a text (.txt) file for your list of passwords.</span></span> <span data-ttu-id="eef5a-190">Размер текстового файла не может превышать 10 МБ.</span><span class="sxs-lookup"><span data-stu-id="eef5a-190">The text file cannot exceed 10 MB in file size.</span></span> <span data-ttu-id="eef5a-191">Используйте один пароль для каждой строки и убедитесь, что после последнего пароля в списке включен жесткий возврат.</span><span class="sxs-lookup"><span data-stu-id="eef5a-191">Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="eef5a-192">Нажмите кнопку **Готово** , чтобы запустить атаку.</span><span class="sxs-lookup"><span data-stu-id="eef5a-192">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="eef5a-193">Новые возможности в симуляторе атак</span><span class="sxs-lookup"><span data-stu-id="eef5a-193">New features in Attack Simulator</span></span>

<span data-ttu-id="eef5a-194">В симулятор атак недавно были добавлены новые функции.</span><span class="sxs-lookup"><span data-stu-id="eef5a-194">New features have recently been added to Attack Simulator.</span></span> <span data-ttu-id="eef5a-195">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="eef5a-195">These include:</span></span>

- <span data-ttu-id="eef5a-196">Расширенные возможности создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="eef5a-196">Advanced reporting capabilities.</span></span> <span data-ttu-id="eef5a-197">Возможность просмотра данных, таких как самое быстрое (или самое медленное) время, для открытия электронного сообщения с моделированием атак, наиболее быстрого (или наиболее медленного) времени для щелчка ссылки в сообщении и других зрительных образов.</span><span class="sxs-lookup"><span data-stu-id="eef5a-197">The ability to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more visualizations.</span></span>

- <span data-ttu-id="eef5a-198">Редактор шаблонов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="eef5a-198">Email template editor.</span></span> <span data-ttu-id="eef5a-199">Возможность создания настраиваемого, повторно используемого шаблона электронной почты, который можно использовать для имитации атак в будущем.</span><span class="sxs-lookup"><span data-stu-id="eef5a-199">The ability to create a custom, reusable email template's that you can use for future attack simulations.</span></span>

- <span data-ttu-id="eef5a-200">Импорт получателей CSV.</span><span class="sxs-lookup"><span data-stu-id="eef5a-200">CSV Recipient Import.</span></span> <span data-ttu-id="eef5a-201">Возможность использовать CSV-файл для импорта целевого списка получателей вместо использования средства выбора адресной книги.</span><span class="sxs-lookup"><span data-stu-id="eef5a-201">The ability to use a .csv file to import your target recipient list instead of using the address book picker.</span></span>

<span data-ttu-id="eef5a-202">Новые возможности скоро появятся в симуляторе атак.</span><span class="sxs-lookup"><span data-stu-id="eef5a-202">More new features are coming soon to Attack Simulator.</span></span> <span data-ttu-id="eef5a-203">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="eef5a-203">These include:</span></span>

- <span data-ttu-id="eef5a-204">Имитация фишинговых фишинговых данных вложений.</span><span class="sxs-lookup"><span data-stu-id="eef5a-204">Attachment payload phishing simulation.</span></span> <span data-ttu-id="eef5a-205">Возможность использовать вложение в качестве полезных данных для имитации фишинга вместо URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="eef5a-205">The ability to use an attachment as the payload for phishing simulation in place of a URL.</span></span>

<span data-ttu-id="eef5a-206">Посетите [план Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) , чтобы узнать, что находится в разработке, что такое развертывание и какие из них уже запущены.</span><span class="sxs-lookup"><span data-stu-id="eef5a-206">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>

## <a name="see-also"></a><span data-ttu-id="eef5a-207">См. также</span><span class="sxs-lookup"><span data-stu-id="eef5a-207">See also</span></span>

[<span data-ttu-id="eef5a-208">Описание службы Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="eef5a-208">Office 365 Advanced Threat Protection Service Description</span></span>](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)

[<span data-ttu-id="eef5a-209">Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="eef5a-209">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)



