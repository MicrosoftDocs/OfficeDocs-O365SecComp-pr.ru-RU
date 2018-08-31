---
title: Эмулятор атак в Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/19/2018
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Узнайте о трех различных типов атаки через Интернет, которые можно запустить с помощью имитатора атаки.
ms.openlocfilehash: 364144c0b2f8109c67fb262ce879414088380ebe
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534582"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="f46a0-103">Эмулятор атак в Office 365</span><span class="sxs-lookup"><span data-stu-id="f46a0-103">Attack Simulator in Office 365</span></span>

<span data-ttu-id="f46a0-p101">С помощью имитатора атаки (включены в [Анализ угроз Office 365](office-365-ti.md)) Если вы являетесь членом группы безопасности вашей организации, можно запустить сценарии реалистичной атаки в вашей организации. Это может помочь определить и найти уязвимы пользователей перед реальных атаки влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p101">With Attack Simulator (included in [Office 365 Threat Intelligence](office-365-ti.md)), if you are a member of your organization's security team, you can run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="f46a0-106">Атаки</span><span class="sxs-lookup"><span data-stu-id="f46a0-106">The Attacks</span></span>

<span data-ttu-id="f46a0-107">В предварительном выпуске мы предлагаем три вида при моделировании атаки, которые могут работать:</span><span class="sxs-lookup"><span data-stu-id="f46a0-107">At preview release we offer three kinds of attack simulations that you can run:</span></span>
  
- [<span data-ttu-id="f46a0-108">Отображение имени направленных фишинга</span><span class="sxs-lookup"><span data-stu-id="f46a0-108">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="f46a0-109">Пароль распылителя атаки</span><span class="sxs-lookup"><span data-stu-id="f46a0-109">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="f46a0-110">Перебора атаки пароль</span><span class="sxs-lookup"><span data-stu-id="f46a0-110">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="f46a0-111">Атака для успешного запуска учетная запись, под управлением атаки и вход в систему необходимо использовать многофакторной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f46a0-111">For an attack to be successfully launched, the account that is running the attack and logged on must use multi-factor authentication.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f46a0-112">Поддержка условного доступа в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="f46a0-112">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="f46a0-113">Для доступа к имитатора атаки, в системы &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.</span><span class="sxs-lookup"><span data-stu-id="f46a0-113">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="f46a0-114">Перед началом...</span><span class="sxs-lookup"><span data-stu-id="f46a0-114">Before you begin...</span></span>

<span data-ttu-id="f46a0-115">Убедитесь в том, что вам и вашей организации соответствуют следующим требованиям для атаки имитатора:</span><span class="sxs-lookup"><span data-stu-id="f46a0-115">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
  
- <span data-ttu-id="f46a0-116">Вашей организации есть [Анализ угроз Office 365](office-365-ti.md), с помощью атаки имитатора видимы в безопасности &amp; центре соответствия требованиям (перейдите к **разделу Управление угроз** \> **атаки имитатора**)</span><span class="sxs-lookup"><span data-stu-id="f46a0-116">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span>
    
- <span data-ttu-id="f46a0-p102">Электронной почты вашей организации размещается в Exchange Online. (Атаки имитатора недоступно для локальных серверов электронной почты).</span><span class="sxs-lookup"><span data-stu-id="f46a0-p102">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="f46a0-119">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="f46a0-119">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="f46a0-120">Ваша организация использует [многофакторной проверки подлинности для пользователей Office 365](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span><span class="sxs-lookup"><span data-stu-id="f46a0-120">Your organization is using [Multi-factor authentication for Office 365 users](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)</span></span>
    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="f46a0-121">Отображение имени направленных фишинга</span><span class="sxs-lookup"><span data-stu-id="f46a0-121">Display name spear-phishing attack</span></span>

<span data-ttu-id="f46a0-p103">Фишинг — это общий термин для широкого набора classed как атака стиль социальная инженерия атаки. В этом атаки, ориентированный на направленные фишинга, более целевой атаки, направленные на конкретной группы отдельных пользователей или организации. Как правило выполненных настраиваемого атаки с некоторые reconnaissance и использование отображаемое имя, которое будет создавать доверия в получателя, таких как сообщения электронной почты, которая выглядит как он поступил от руководителя вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p103">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="f46a0-p104">В этом атаки основное внимание уделяется возможности работы с которого была инициирована, изменив отображаемое имя и исходный адрес отображается сообщение. При успешной направленных фишинга компьютерных преступников получить доступ к учетных данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p104">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="f46a0-127">Для моделирования работы направленных фишинга</span><span class="sxs-lookup"><span data-stu-id="f46a0-127">To simulate a spear-phishing attack</span></span>

![Создайте текст электронной почты](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="f46a0-p105">Вы можете создавать расширенного редактора HTML непосредственно в поле **текст сообщения электронной почты** , самого или работать с исходного HTML-кода. Существует два важных поля для включения в HTML-код.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p105">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source. There are two important fields for inclusion in the HTML:</span></span> 
  
1. <span data-ttu-id="f46a0-131">В разделе Безопасность &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.</span><span class="sxs-lookup"><span data-stu-id="f46a0-131">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="f46a0-132">Укажите имя удобной для восприятия кампании для атаки или выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="f46a0-132">Specify a meaningful campaign name for the attack or select a template.</span></span>
    
    ![Начальная страница фишинга](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="f46a0-p106">Укажите в целевой список получателей. Это может быть отдельных пользователей или групп в вашей организации. Целевые получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p106">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
    ![Выбор получателей](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="f46a0-138">Настройка сведений фишинга электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f46a0-138">Configure the Phishing email details.</span></span>
    
    ![Настройка сведений о электронной почты](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)
  
    <span data-ttu-id="f46a0-p107">Форматирование HTML-код может быть следующим сложных или базовой должна кампании. Как HTML, можно вставить изображения и текст для улучшения believability. У вас есть элемент управления на полученного сообщения будет выглядеть в клиенте получение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p107">The HTML formatting can be as complex or basic as your campaign needs. As it is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
1. <span data-ttu-id="f46a0-p108">Введите текст для полей **из (имя)** . Это поле, которое отображает в поле **Отображаемое имя** в клиенте получение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p108">Enter text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
2. <span data-ttu-id="f46a0-p109">Введите текст или **из** поля. Это поле, которое показывает, как адрес электронной почты отправителя в получающей клиента электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p109">Enter text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="f46a0-p110">Можно ввести существующих имен электронной почты в пределах организации (это сделает адрес электронной почты, которые фактически решения в клиент-получатель, упрощение модели очень высоким уровнем доверия), или можно ввести внешний адрес электронной почты. Адрес электронной почты, который указан не существует, но его нужно формат является допустимым адресом SMTP, таких как user@domainname.extension.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p110">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
3. <span data-ttu-id="f46a0-p111">С помощью раскрывающегося списка выбора, установите для входа фишинга URL-адрес сервера, который отражает тип контента, которые должны быть в рамках вашей атаки. Несколько URL-адреса, темой предоставляются для выбора, такие как документов доставки, технические, о начислении заработной платы и т.д. Это эффективно конечных пользователей будет предложено щелкните URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p111">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
4. <span data-ttu-id="f46a0-p112">Введите URL-адрес настраиваемого целевую страницы. С помощью этого перенаправление пользователей в URL-адрес, укажите в конце атаки. Если у вас есть внутренний курса обучения, например, можно указать, здесь.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p112">Enter a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
5. <span data-ttu-id="f46a0-p113">Введите текст в поле **Тема** . Это поле, которое показывает, как **Имя субъекта** в клиенте получение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p113">Enter text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
5. <span data-ttu-id="f46a0-156">Создайте **текст сообщения электронной почты** , который будет получать целевой объект.</span><span class="sxs-lookup"><span data-stu-id="f46a0-156">Compose the **Email body** that the target will receive.</span></span> 
  
 <span data-ttu-id="f46a0-157">**${имя_пользователя}** вставляет имя целевых значений в текст электронной почты</span><span class="sxs-lookup"><span data-stu-id="f46a0-157">**${username}** inserts the targets name into the Email body</span></span> 
  
 <span data-ttu-id="f46a0-158">URL-адрес, мы конечного пользователям нажмите кнопку Вставка **${loginserverurl}**</span><span class="sxs-lookup"><span data-stu-id="f46a0-158">**${loginserverurl}** inserts the URL we want target users to click</span></span> 
    
6. <span data-ttu-id="f46a0-p114">Нажмите кнопку **Далее,** а затем **Готово** для запуска атаки. Сообщение электронной почты фишинга направленных доставляется в почтовые ящики получателей целевой.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p114">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="f46a0-161">Пароль распылителя атаки</span><span class="sxs-lookup"><span data-stu-id="f46a0-161">Password-spray attack</span></span>

<span data-ttu-id="f46a0-p115">После actor очень плохо успешно перечислены список допустимых пользователей от клиента, использующие их знаний распространенных паролей, используемых обычно используется распылителя пароль, против организации. Это используемые широко как есть дешевое атаки для запуска и труднее обнаруживать чем перебора подходов.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p115">A password spray attack against an organization is typically used after a bad actor has successfully enumerated a list of valid users from the tenant, utilizing their knowledge of common passwords used. It is utilized widely as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="f46a0-164">В этом атаки основное внимание уделяется позволяет указать общий пароль для крупных целевой базы пользователей.</span><span class="sxs-lookup"><span data-stu-id="f46a0-164">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="f46a0-165">Для моделирования атаки распылителя пароль</span><span class="sxs-lookup"><span data-stu-id="f46a0-165">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="f46a0-166">В разделе Безопасность &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.</span><span class="sxs-lookup"><span data-stu-id="f46a0-166">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="f46a0-167">Укажите имя удобной для восприятия кампании для атаки.</span><span class="sxs-lookup"><span data-stu-id="f46a0-167">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="f46a0-p116">Укажите в целевой список получателей. Это может быть отдельных пользователей или групп в вашей организации. Целевые получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p116">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="f46a0-p117">Укажите пароль, используемый для атаки. Например одного общего, соответствующий пароль, попробуйте — `Fall2017`. Другой может быть `Spring2018`, или `Password1`.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p117">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="f46a0-174">Нажмите кнопку **Готово** , чтобы запустить атаки.</span><span class="sxs-lookup"><span data-stu-id="f46a0-174">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="f46a0-175">Перебора атаки пароль</span><span class="sxs-lookup"><span data-stu-id="f46a0-175">Brute-force password attack</span></span>

<span data-ttu-id="f46a0-p118">Пароль перебора против организации обычно используется после actor очень плохо успешно перечислены список ключей пользователей от клиента. В этом атаки основное внимание уделяется позволяет указать паролей от одного пользователя.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p118">A brute-force password attack against an organization is typically used after a bad actor has successfully enumerated a list of key users from the tenant. This attack focuses on letting you specify a set of passwords against a single user.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="f46a0-178">Для моделирования атаки перебора паролей</span><span class="sxs-lookup"><span data-stu-id="f46a0-178">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="f46a0-179">В разделе Безопасность &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.</span><span class="sxs-lookup"><span data-stu-id="f46a0-179">In the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="f46a0-180">Укажите имя удобной для восприятия кампании для атаки.</span><span class="sxs-lookup"><span data-stu-id="f46a0-180">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="f46a0-p119">Указание конечного получателя. Целевые получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p119">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="f46a0-p120">Задать пароли для атаки. Например одного общего, соответствующий пароль, попробуйте — `Fall2017`. Другой может быть `Spring2018`, или `Password1`.</span><span class="sxs-lookup"><span data-stu-id="f46a0-p120">Specify a set of passwords to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="f46a0-186">Нажмите кнопку **Готово** , чтобы запустить атаки.</span><span class="sxs-lookup"><span data-stu-id="f46a0-186">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="related-topics"></a><span data-ttu-id="f46a0-187">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f46a0-187">Related topics</span></span>

[<span data-ttu-id="f46a0-188">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="f46a0-188">Office 365 Threat Intelligence</span></span>](office-365-ti.md)
  

