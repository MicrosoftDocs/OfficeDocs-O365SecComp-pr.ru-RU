---
title: Имитатор атак в Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
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
ms.openlocfilehash: ba5658dfa9075b5779f8ca09ccad3547dbddcbb5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216279"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="9faee-104">Имитатор атак в Office 365</span><span class="sxs-lookup"><span data-stu-id="9faee-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="9faee-p102">**Сводка** Если вы являетесь глобальным администратором Office 365 и ваша организация имеет [логику office 365 Threat Intelligence](office-365-ti.md), вы можете использовать Симуляторы для проведения реалистичных атак в Организации. Это поможет определить и найти уязвимых пользователей, прежде чем реальная атака повлияет на нижнюю линию. Ознакомьтесь с этой статьей, чтобы узнать больше.</span><span class="sxs-lookup"><span data-stu-id="9faee-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9faee-p103">Начиная с 2019 февраля и заканчивая на ближайшие несколько месяцев, управление угрозами безопасности Office 365 становится Office 365 Advanced Threat Protection Plan 2 с дополнительными возможностями защиты от угроз. Чтобы узнать больше, ознакомьтесь со статьями [office 365 Advanced Threat protection Plans and ценах](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="9faee-p103">Beginning in February 2019 and rolling out over the next several months, Office 365 Threat Intelligence is becoming Office 365 Advanced Threat Protection Plan 2, with additional threat protection capabilities. To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="9faee-110">Атаки</span><span class="sxs-lookup"><span data-stu-id="9faee-110">The Attacks</span></span>

<span data-ttu-id="9faee-111">В настоящее время доступны три типа имитации атак:</span><span class="sxs-lookup"><span data-stu-id="9faee-111">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="9faee-112">Отображаемое имя спеар — Фишинговая атака</span><span class="sxs-lookup"><span data-stu-id="9faee-112">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="9faee-113">Парольная атака с распылителем</span><span class="sxs-lookup"><span data-stu-id="9faee-113">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="9faee-114">Принудительная атака пароля методом грубого подбора</span><span class="sxs-lookup"><span data-stu-id="9faee-114">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="9faee-p104">Для успешного запуска атаки необходимо использовать многофакторную проверку подлинности для учетной записи, которая используется для имитации атак. Кроме того, вы должны быть глобальным администратором Office 365.</span><span class="sxs-lookup"><span data-stu-id="9faee-p104">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9faee-117">Поддержка условного доступа ожидается в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="9faee-117">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="9faee-118">Чтобы получить доступ к симулятору атак, &amp; в центре безопасности и соответствия требованиям выберите **симулятор атак** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="9faee-118">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="9faee-119">Перед началом работы...</span><span class="sxs-lookup"><span data-stu-id="9faee-119">Before you begin...</span></span>

<span data-ttu-id="9faee-120">Убедитесь, что ваша организация отвечает следующим требованиям для атаки на симулятор:</span><span class="sxs-lookup"><span data-stu-id="9faee-120">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="9faee-p105">Электронная почта вашей организации размещена в Exchange Online. (Симулятор атак недоступен для локальных почтовых серверов.)</span><span class="sxs-lookup"><span data-stu-id="9faee-p105">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="9faee-123">Вы являетесь глобальным администратором Office 365</span><span class="sxs-lookup"><span data-stu-id="9faee-123">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="9faee-124">В организации используется многофакторная [Проверка подлинности для пользователей Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="9faee-124">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="9faee-125">в вашей организации [имеется Office 365 Threat Intelligence](office-365-ti.md), а симулятор атак виден в центре &amp; обеспечения безопасности (перейдите в **симулятор для атаки** **управления** \> угрозами)</span><span class="sxs-lookup"><span data-stu-id="9faee-125">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="9faee-126">![Управление угрозами — симулятор атак](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="9faee-126">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="9faee-127">Отображаемое имя спеар — Фишинговая атака</span><span class="sxs-lookup"><span data-stu-id="9faee-127">Display name spear-phishing attack</span></span>

<span data-ttu-id="9faee-p106">Фишинг — это универсальный термин для широкого набора атак, предназначенных для атаки со стилем социального проектирования. Эта атака сосредоточена на phishing-атаках спеар, что более целевая атака предназначена для определенной группы пользователей или организации. Как правило, пользовательская атака с некоторым реконнаиссанце выполнена и с использованием отображаемого имени, которое будет создавать доверие для получателя, например сообщение электронной почты, которое выглядит так, как оно было получено от руководителя в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="9faee-p106">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="9faee-p107">Эта атака нацелена на то, что вы можете управлять тем, кто поступил с сообщениями, изменив отображаемое имя и адрес источника. Когда спеар-фишинг будет успешным, циберкриминалс получить доступ к учетным данным пользователей.</span><span class="sxs-lookup"><span data-stu-id="9faee-p107">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="9faee-133">Имитация атаки спеар-фишинга</span><span class="sxs-lookup"><span data-stu-id="9faee-133">To simulate a spear-phishing attack</span></span>

![Создание сообщения электронной почты](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="9faee-135">Вы можете создавать редактор форматированного HTML-кода непосредственно в самом поле **текста сообщения электронной почты** или работать с HTML-кодом.</span><span class="sxs-lookup"><span data-stu-id="9faee-135">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="9faee-136">В [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)выберите **симулятор для атак** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="9faee-136">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="9faee-137">Укажите понятное имя кампании для атаки или выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="9faee-137">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![Страница "начало фишинга"](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="9faee-p108">Укажите получателей назначения. Это могут быть отдельные пользователи или группы в Организации. Чтобы атака достигла успеха, у каждого целевого получателя должен быть почтовый ящик Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9faee-p108">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![Выбор получателей](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="9faee-143">Настройте сведения об фишинговых сообщениях.</span><span class="sxs-lookup"><span data-stu-id="9faee-143">Configure the Phishing email details.</span></span> <br/>![Настройка сведений об электронной почте](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="9faee-p109">Форматирование HTML может быть как сложным, так и базовым по отношению к потребностям кампании. Как и формат электронной почты HTML, вы можете вставить изображения и текст, чтобы улучшить белиевабилити. Вы можете управлять тем, как будет выглядеть полученное сообщение в принимающем почтовом клиенте.</span><span class="sxs-lookup"><span data-stu-id="9faee-p109">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="9faee-p110">Укажите текст для поля " **от" (имя)** . Это поле показывается в **отображаемОм имени** принимающего почтового клиента.</span><span class="sxs-lookup"><span data-stu-id="9faee-p110">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="9faee-p111">Укажите текст или поле " **от** ". Это поле, которое отображается в качестве адреса электронной почты отправителя в принимающем почтовом клиенте.</span><span class="sxs-lookup"><span data-stu-id="9faee-p111">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="9faee-p112">Вы можете ввести существующее пространство имен электронной почты в своей организации (это сделает адрес электронной почты действительно в принимающем клиенте, который упрощает модель доверенности), или вы можете ввести внешний адрес электронной почты. Указанный адрес электронной почты не обязательно должен существовать, но необходимо отформатировать допустимый SMTP-адрес, например user @ ИмяДомена. extension.</span><span class="sxs-lookup"><span data-stu-id="9faee-p112">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="9faee-p113">В раскрывающемся списке выберите URL-адрес сервера фишингового входа, который отражает тип контента, который будет находиться в вашей атаке. Можно выбрать несколько URL-адресов с темой, таких как доставка документов, техническая, зарплата и т. д. Это фактически URL-адрес, по которому пользователям предлагается щелкнуть.</span><span class="sxs-lookup"><span data-stu-id="9faee-p113">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="9faee-p114">Укажите URL-адрес настраиваемой целевой страницы. При этом пользователи будут перенаправляться на URL-адрес, указанный в конце успешной атаки. Если у вас есть обучение по внутренней осведомленности, например, вы можете указать здесь.</span><span class="sxs-lookup"><span data-stu-id="9faee-p114">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="9faee-p115">Укажите текст для поля **subject** . Это поле, которое отображается в качестве **имени субъекта** в принимающем почтовом клиенте.</span><span class="sxs-lookup"><span data-stu-id="9faee-p115">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="9faee-161">Создайте **текст сообщения электронной почты** , который будет получать целевой объект.</span><span class="sxs-lookup"><span data-stu-id="9faee-161">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="9faee-162">`${username}`Вставляет имя целевого значения в текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="9faee-162">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="9faee-163">`${loginserverurl}`вставляет URL-адрес, по которому будут щелкать конечные пользователи</span><span class="sxs-lookup"><span data-stu-id="9faee-163">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="9faee-p116">Нажмите кнопку **Далее,** а затем кнопку **Готово** , чтобы запустить атаку. Phishing-сообщения электронной почты спеар доставляются в почтовые ящики целевых получателей.</span><span class="sxs-lookup"><span data-stu-id="9faee-p116">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="9faee-166">Парольная атака с распылителем</span><span class="sxs-lookup"><span data-stu-id="9faee-166">Password-spray attack</span></span>

<span data-ttu-id="9faee-p117">Использование распылителя пароля в организации обычно используется после того, как ошибочный субъект успешно получил список действительных пользователей от клиента. Неверный субъект знает об общих паролях, используемых пользователями. Это широко используемая атака, так как она является дешевой атакой и сложнее, чем методы грубой силы.</span><span class="sxs-lookup"><span data-stu-id="9faee-p117">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="9faee-170">Эта атака фокусируется на том, что вы указываете общий пароль для большой целевой базы пользователей.</span><span class="sxs-lookup"><span data-stu-id="9faee-170">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="9faee-171">Имитация атаки с использованием пароля</span><span class="sxs-lookup"><span data-stu-id="9faee-171">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="9faee-172">В [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)выберите **симулятор для атак** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="9faee-172">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="9faee-173">Укажите понятное имя кампании для атаки.</span><span class="sxs-lookup"><span data-stu-id="9faee-173">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="9faee-p118">Укажите получателей назначения. Это могут быть отдельные пользователи или группы в Организации. Чтобы атака достигла результата, целевой получатель должен иметь почтовый ящик Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9faee-p118">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="9faee-p119">Укажите пароль, который будет использоваться для атаки. Например, вы можете попытаться использовать один общий, подходящий `Fall2017`пароль. Другое может быть `Spring2018`или `Password1`.</span><span class="sxs-lookup"><span data-stu-id="9faee-p119">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="9faee-180">Нажмите кнопку **Готово** , чтобы запустить атаку.</span><span class="sxs-lookup"><span data-stu-id="9faee-180">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="9faee-181">Принудительная атака пароля методом грубого подбора</span><span class="sxs-lookup"><span data-stu-id="9faee-181">Brute-force password attack</span></span>

<span data-ttu-id="9faee-p120">Атака с помощью прямого прямого пароля для организации обычно используется после того, как ошибочный субъект успешно получил список ключевых пользователей от клиента. Эта атака фокусируется на попытке использовать набор паролей для учетной записи одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="9faee-p120">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="9faee-184">Имитация атаки с использованием пароля методом грубой силы</span><span class="sxs-lookup"><span data-stu-id="9faee-184">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="9faee-185">В [центре безопасности &amp; и соответствия требованиям](https://protection.office.com)выберите **симулятор для атак** **управления** \> угрозами.</span><span class="sxs-lookup"><span data-stu-id="9faee-185">In the [Security &amp; Compliance Center](https://protection.office.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="9faee-186">Укажите понятное имя кампании для атаки.</span><span class="sxs-lookup"><span data-stu-id="9faee-186">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="9faee-p121">Укажите целевого получателя. Чтобы атака достигла результата, целевой получатель должен иметь почтовый ящик Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9faee-p121">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="9faee-p122">Укажите набор паролей, который будет использоваться для атаки. Для этого можно использовать текстовый файл (txt) для списка паролей. Размер текстового файла не может превышать 10 МБ. Используйте один пароль для каждой строки и убедитесь, что после последнего пароля в списке включен жесткий возврат.</span><span class="sxs-lookup"><span data-stu-id="9faee-p122">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="9faee-193">Нажмите кнопку **Готово** , чтобы запустить атаку.</span><span class="sxs-lookup"><span data-stu-id="9faee-193">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="9faee-194">Новые возможности в симуляторе атак</span><span class="sxs-lookup"><span data-stu-id="9faee-194">New features in Attack Simulator</span></span>

<span data-ttu-id="9faee-p123">Новые функции добавляются в симулятор атак. К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="9faee-p123">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="9faee-p124">**Расширенные возможности создания отчетов**. Вы сможете видеть такие данные, как самое медленное (или самое медленное) время, чтобы открыть электронное сообщение с моделированием атак, самое быстрое (или самое медленное) время щелкнуть ссылку в сообщении и многое другое.</span><span class="sxs-lookup"><span data-stu-id="9faee-p124">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="9faee-p125">**Редактор шаблонов электронной почты**. Вы можете создать настраиваемый шаблон электронной почты для повторного использования, который можно использовать для имитации атак в будущем.</span><span class="sxs-lookup"><span data-stu-id="9faee-p125">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="9faee-201">Посетите [план Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap) , чтобы узнать, что находится в разработке, что такое развертывание и какие из них уже запущены.</span><span class="sxs-lookup"><span data-stu-id="9faee-201">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>



