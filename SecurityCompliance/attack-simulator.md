---
title: Эмулятор атак в Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/02/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: da5845db-c578-4a41-b2cb-5a09689a551b
description: Как глобальный администратор Office 365 имитатора атаки можно использовать для запуска сценариев реалистичной атак в вашей организации. Это может помочь определить и найти уязвимы пользователей перед реальных атаки попадает бизнеса.
ms.openlocfilehash: 1a1d22b0b36ce8b6a2086296be8f8b5d47d79280
ms.sourcegitcommit: d512c1df01377e305e8d5c0170c822cf78f09565
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "27472002"
---
# <a name="attack-simulator-in-office-365"></a><span data-ttu-id="ac1a3-104">Эмулятор атак в Office 365</span><span class="sxs-lookup"><span data-stu-id="ac1a3-104">Attack Simulator in Office 365</span></span>

<span data-ttu-id="ac1a3-p102">**Сводка** Если вы глобального администратора Office 365 и вашей организации есть [Анализ угроз Office 365](office-365-ti.md), имитатора атаки можно использовать для запуска сценариев реалистичной атак в вашей организации. Это может помочь определить и найти уязвимы пользователей перед реальных атаки влияет на производительность. В этой статье, чтобы получить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p102">**Summary** If you are an Office 365 global administrator and your organization has [Office 365 Threat Intelligence](office-365-ti.md), you can use Attack Simulator to run realistic attack scenarios in your organization. This can help you identify and find vulnerable users before a real attack impacts your bottom line. Read this article to learn more.</span></span>
  
## <a name="the-attacks"></a><span data-ttu-id="ac1a3-108">Атаки</span><span class="sxs-lookup"><span data-stu-id="ac1a3-108">The Attacks</span></span>

<span data-ttu-id="ac1a3-109">В настоящее время доступны три вида при моделировании атаки:</span><span class="sxs-lookup"><span data-stu-id="ac1a3-109">Three kinds of attack simulations are currently available:</span></span>
  
- [<span data-ttu-id="ac1a3-110">Отображение имени направленных фишинга</span><span class="sxs-lookup"><span data-stu-id="ac1a3-110">Display name spear-phishing attack</span></span>](attack-simulator.md#spearphish)
    
- [<span data-ttu-id="ac1a3-111">Пароль распылителя атаки</span><span class="sxs-lookup"><span data-stu-id="ac1a3-111">Password-spray attack</span></span>](attack-simulator.md#passwordspray)
    
- [<span data-ttu-id="ac1a3-112">Перебора атаки пароль</span><span class="sxs-lookup"><span data-stu-id="ac1a3-112">Brute-force password attack</span></span>](attack-simulator.md#bruteforce)
    
<span data-ttu-id="ac1a3-p103">Атака для успешного запуска используйте многофакторной проверки подлинности для учетной записи, используемой для запуска смоделированные атаки. Кроме того необходимо быть глобального администратора Office 365.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p103">For an attack to be successfully launched, you use multi-factor authentication on the account you are using to run simulated attacks. In addition, you must be an Office 365 global administrator.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ac1a3-115">Поддержка условного доступа в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-115">Support for Conditional Access is coming soon.</span></span> 
  
<span data-ttu-id="ac1a3-116">Для доступа к имитатора атаки, в системы &amp; центре соответствия требованиям, выберите **Threat management** \> **имитатора атаки**.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-116">To access Attack Simulator, in the Security &amp; Compliance Center, choose **Threat management** \> **Attack simulator**.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="ac1a3-117">Перед началом...</span><span class="sxs-lookup"><span data-stu-id="ac1a3-117">Before you begin...</span></span>

<span data-ttu-id="ac1a3-118">Убедитесь в том, что вам и вашей организации соответствуют следующим требованиям для атаки имитатора:</span><span class="sxs-lookup"><span data-stu-id="ac1a3-118">Make sure that you and your organization meet the following requirements for Attack Simulator:</span></span>
      
- <span data-ttu-id="ac1a3-p104">Электронной почты вашей организации размещается в Exchange Online. (Атаки имитатора недоступно для локальных серверов электронной почты).</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p104">Your organization's email is hosted in Exchange Online. (Attack Simulator is not available for on-premises email servers.)</span></span>
    
- <span data-ttu-id="ac1a3-121">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="ac1a3-121">You are an Office 365 global administrator</span></span>
    
- <span data-ttu-id="ac1a3-122">Ваша организация использует [многофакторной проверки подлинности для пользователей Office 365](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="ac1a3-122">Your organization is using [Multi-factor authentication for Office 365 users](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication?view=o365-worldwide)</span></span>
 
- <span data-ttu-id="ac1a3-123">Вашей организации есть [Анализ угроз Office 365](office-365-ti.md), с помощью атаки имитатора видимы в безопасности &amp; центре соответствия требованиям (перейдите к **разделу Управление угроз** \> **атаки имитатора**)</span><span class="sxs-lookup"><span data-stu-id="ac1a3-123">Your organization has [Office 365 Threat Intelligence](office-365-ti.md), with Attack Simulator visible in the Security &amp; Compliance Center (go to **Threat management** \> **Attack simulator**)</span></span><br/><span data-ttu-id="ac1a3-124">![Управление угроз — имитатора атаки](media/ThreatMgmt-AttackSimulator.png)</span><span class="sxs-lookup"><span data-stu-id="ac1a3-124">![Threat management - Attack Simulator](media/ThreatMgmt-AttackSimulator.png)</span></span>

    
## <a name="display-name-spear-phishing-attack"></a><span data-ttu-id="ac1a3-125">Отображение имени направленных фишинга</span><span class="sxs-lookup"><span data-stu-id="ac1a3-125">Display name spear-phishing attack</span></span>

<span data-ttu-id="ac1a3-p105">Фишинг — это общий термин для широкого набора classed как атака стиль социальная инженерия атаки. В этом атаки, ориентированный на направленные фишинга, более целевой атаки, направленные на конкретной группы отдельных пользователей или организации. Как правило выполненных настраиваемого атаки с некоторые reconnaissance и использование отображаемое имя, которое будет создавать доверия в получателя, таких как сообщения электронной почты, которая выглядит как он поступил от руководителя вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p105">Phishing is a generic term for a broad suite of attacks classed as a social engineering style attack. This attack is focused on spear phishing, a more targeted attack that is aimed at a specific group of individuals or an organization. Typically, a customized attack with some reconnaissance performed and using a display name that will generate trust in the recipient, such as an email message that looks like it came from an executive within your organization.</span></span>
  
<span data-ttu-id="ac1a3-p106">В этом атаки основное внимание уделяется возможности работы с которого была инициирована, изменив отображаемое имя и исходный адрес отображается сообщение. При успешной направленных фишинга компьютерных преступников получить доступ к учетных данных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p106">This attack focuses on letting you manipulate who the message appears to have originated from by changing the display name and source address. When spear-phishing attacks are successful, cybercriminals gain access to users' credentials.</span></span>
  
### <a name="to-simulate-a-spear-phishing-attack"></a><span data-ttu-id="ac1a3-131">Для моделирования работы направленных фишинга</span><span class="sxs-lookup"><span data-stu-id="ac1a3-131">To simulate a spear-phishing attack</span></span>

![Создайте текст электронной почты](media/9bd65af4-1f9d-45c1-8c06-796d7ccfd425.jpg)
  
<span data-ttu-id="ac1a3-133">Вы можете создавать расширенного редактора HTML непосредственно в поле **текст сообщения электронной почты** , самого или работать с исходного HTML-кода.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-133">You can craft the rich HTML editor directly in the **Email body** field itself or work with HTML source.</span></span>
  
1. <span data-ttu-id="ac1a3-134">В [безопасности &amp; центре соответствия требованиям](https://security.microsoft.com), выберите **Threat management** \> **имитатора атаки**.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-134">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="ac1a3-135">Укажите имя удобной для восприятия кампании для атаки или выберите шаблон.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-135">Specify a meaningful campaign name for the attack or select a template.</span></span> <br/>![Начальная страница фишинга](media/5e93b3cc-5981-462f-8b45-bdf85d97f1b8.jpg)
  
3. <span data-ttu-id="ac1a3-p107">Укажите в целевой список получателей. Это может быть отдельных пользователей или групп в вашей организации. Каждой целевой получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p107">Specify the target recipients. This can be individuals or groups in your organization. Each targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span> <br/>![Выбор получателей](media/faf8c2e0-6175-4cd7-8265-0c8e727f4d0f.jpg)
  
4. <span data-ttu-id="ac1a3-141">Настройка сведений фишинга электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-141">Configure the Phishing email details.</span></span> <br/>![Настройка сведений о электронной почты](media/f043608f-f8ce-4aae-be28-86e8ecc524a9.jpg)<br/><span data-ttu-id="ac1a3-p108">Форматирование HTML-код может быть следующим сложных или базовой должна кампании. Как формат электронной почты и HTML-код, можно вставить изображения и текст для улучшения believability. У вас есть элемент управления на полученного сообщения будет выглядеть в клиенте получение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p108">The HTML formatting can be as complex or basic as your campaign needs. As the email format is HTML, you can insert images and text to enhance believability. You have control on what the received message will look like in the receiving email client.</span></span>
    
5. <span data-ttu-id="ac1a3-p109">Указание текста для поля **из (имя)** . Это поле, которое отображает в поле **Отображаемое имя** в клиенте получение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p109">Specify text for the **From (Name)** field. This is the field that shows in the **Display Name** in the receiving email client.</span></span> 
    
6. <span data-ttu-id="ac1a3-p110">Укажите текст или **из** поля. Это поле, которое показывает, как адрес электронной почты отправителя в получающей клиента электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p110">Specify text or the **From** field. This is the field that shows as the email address of the sender in the receiving email client. </span></span><br/><span data-ttu-id="ac1a3-p111">Можно ввести существующих имен электронной почты в пределах организации (это сделает адрес электронной почты, которые фактически решения в клиент-получатель, упрощение модели очень высоким уровнем доверия), или можно ввести внешний адрес электронной почты. Адрес электронной почты, который указан не существует, но его нужно формат является допустимым адресом SMTP, таких как user@domainname.extension.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p111">You can enter an existing email namespace within your organization (doing this will make the email address actually resolve in the receiving client, facilitating a very high trust model), or you can enter an external email address. The email address that you specify does not have to actually exist, but it does need to following the format of a valid SMTP address, such as user@domainname.extension.</span></span> 
  
7. <span data-ttu-id="ac1a3-p112">С помощью раскрывающегося списка выбора, установите для входа фишинга URL-адрес сервера, который отражает тип контента, которые должны быть в рамках вашей атаки. Несколько URL-адреса, темой предоставляются для выбора, такие как документов доставки, технические, о начислении заработной платы и т.д. Это эффективно конечных пользователей будет предложено щелкните URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p112">Using the drop-down selector, select a Phishing Login server URL that reflects the type of content you will have within your attack. Several themed URLs are provided for you to choose from, such as document delivery, technical, payroll etc. This is effectively the URL that targeted users are asked to click.</span></span>
    
8. <span data-ttu-id="ac1a3-p113">Укажите URL-адрес настраиваемого целевую страницы. С помощью этого перенаправление пользователей в URL-адрес, укажите в конце атаки. Если у вас есть внутренний курса обучения, например, можно указать, здесь.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p113">Specify a custom landing page URL. Using this will redirect users to a URL you specify at the end of a successful attack. If you have internal awareness training, for example, you can specify that here.</span></span>
    
9. <span data-ttu-id="ac1a3-p114">Укажите текст в поле **Тема** . Это поле, которое показывает, как **Имя субъекта** в клиенте получение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p114">Specify text for the **Subject** field. This is the field that shows as the **Subject Name** in the receiving email client.</span></span> 
    
10. <span data-ttu-id="ac1a3-159">Создайте **текст сообщения электронной почты** , который будет получать целевой объект.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-159">Compose the **Email body** that the target will receive.</span></span> <br/><span data-ttu-id="ac1a3-160">`${username}`Вставляет имя целевых значений в текст электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-160">`${username}` inserts the targets name into the Email body.</span></span> <br/><span data-ttu-id="ac1a3-161">`${loginserverurl}`Вставляет URL-адрес, мы конечным пользователям, щелкните</span><span class="sxs-lookup"><span data-stu-id="ac1a3-161">`${loginserverurl}` inserts the URL we want target users to click</span></span> 
    
11. <span data-ttu-id="ac1a3-p115">Нажмите кнопку **Далее,** а затем **Готово** для запуска атаки. Сообщение электронной почты фишинга направленных доставляется в почтовые ящики получателей целевой.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p115">Choose **Next,** then **Finish** to launch the attack. The spear phishing email message is delivered to your target recipients' mailboxes.</span></span> 
    
## <a name="password-spray-attack"></a><span data-ttu-id="ac1a3-164">Пароль распылителя атаки</span><span class="sxs-lookup"><span data-stu-id="ac1a3-164">Password-spray attack</span></span>

<span data-ttu-id="ac1a3-p116">Распылитель пароль, против организации обычно используется после actor очень плохо успешно приобрел список допустимых пользователей от клиента. Actor очень плохо знает о распространенных паролей, с которыми пользователи использования. Это широко используемых атаки, как есть дешевое атаки для выполнения и труднее обнаруживать чем перебора подходов.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p116">A password spray attack against an organization is typically used after a bad actor has successfully acquired a list of valid users from the tenant. The bad actor knows about common passwords that people use. This is a widely used attack, as it is a cheap attack to run, and harder to detect than brute force approaches.</span></span>
  
<span data-ttu-id="ac1a3-168">В этом атаки основное внимание уделяется позволяет указать общий пароль для крупных целевой базы пользователей.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-168">This attack focuses on letting you specify a common password against a large target base of users.</span></span>
  
### <a name="to-simulate-a-password-spray-attack"></a><span data-ttu-id="ac1a3-169">Для моделирования атаки распылителя пароль</span><span class="sxs-lookup"><span data-stu-id="ac1a3-169">To simulate a password-spray attack</span></span>

1. <span data-ttu-id="ac1a3-170">В [безопасности &amp; центре соответствия требованиям](https://security.microsoft.com), выберите **Threat management** \> **имитатора атаки**.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-170">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="ac1a3-171">Укажите имя удобной для восприятия кампании для атаки.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-171">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="ac1a3-p117">Укажите в целевой список получателей. Это может быть отдельных пользователей или групп в вашей организации. Целевые получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p117">Specify the target recipients. This can be individuals or groups in your organization. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="ac1a3-p118">Укажите пароль, используемый для атаки. Например одного общего, соответствующий пароль, попробуйте — `Fall2017`. Другой может быть `Spring2018`, или `Password1`.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p118">Specify a password to use for the attack. For example, one common, relevant password you could try is `Fall2017`. Another might be `Spring2018`, or `Password1`.</span></span>
    
5. <span data-ttu-id="ac1a3-178">Нажмите кнопку **Готово** , чтобы запустить атаки.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-178">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="brute-force-password-attack"></a><span data-ttu-id="ac1a3-179">Перебора атаки пароль</span><span class="sxs-lookup"><span data-stu-id="ac1a3-179">Brute-force password attack</span></span>

<span data-ttu-id="ac1a3-p119">Пароль перебора против организации обычно используется после actor очень плохо успешно приобрел список ключей пользователей от клиента. В этом атаки фокусируется на проверке паролей одного пользователя для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p119">A brute-force password attack against an organization is typically used after a bad actor has successfully acquired a list of key users from the tenant. This attack focuses on trying a set of passwords on a single user's account.</span></span>
  
### <a name="to-simulate-a-brute-force-password-attack"></a><span data-ttu-id="ac1a3-182">Для моделирования атаки перебора паролей</span><span class="sxs-lookup"><span data-stu-id="ac1a3-182">To simulate a brute-force password attack</span></span>

1. <span data-ttu-id="ac1a3-183">В [безопасности &amp; центре соответствия требованиям](https://security.microsoft.com), выберите **Threat management** \> **имитатора атаки**.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-183">In the [Security &amp; Compliance Center](https://security.microsoft.com), choose **Threat management** \> **Attack simulator**.</span></span>
    
2. <span data-ttu-id="ac1a3-184">Укажите имя удобной для восприятия кампании для атаки.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-184">Specify a meaningful campaign name for the attack.</span></span>
    
3. <span data-ttu-id="ac1a3-p120">Указание конечного получателя. Целевые получателя должен быть Online почтовый ящик Exchange в порядке для атаки успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p120">Specify the target recipient. A targeted recipient must have an Exchange Online Mailbox in order for the attack to be successful.</span></span>
    
4. <span data-ttu-id="ac1a3-p121">Задать пароли для атаки. Для этого можно использовать текст (txt) файла для списка паролей. В текстовом файле не должна превышать 10 МБ в размер файла. Используйте один пароль в строке, а необходимо указать перевода строки после последнего пароль в списке.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p121">Specify a set of passwords to use for the attack. To do this, you can use a text (.txt) file for your list of passwords. The text file cannot exceed 10 MB in file size. Use one password per line, and make sure to include a hard return after the last password in your list.</span></span>
    
5. <span data-ttu-id="ac1a3-191">Нажмите кнопку **Готово** , чтобы запустить атаки.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-191">Choose **Finish** to launch the attack.</span></span> 
    
## <a name="new-features-in-attack-simulator"></a><span data-ttu-id="ac1a3-192">Новые возможности имитатора атаки</span><span class="sxs-lookup"><span data-stu-id="ac1a3-192">New features in Attack Simulator</span></span>

<span data-ttu-id="ac1a3-p122">Новые возможности, добавленных имитатора атаки. К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p122">New features are being added to Attack Simulator. These include:</span></span>
- <span data-ttu-id="ac1a3-p123">**Дополнительно, подготовки отчетов**. Вы сможете видеть данные, например, время максимальной (или самые медленные) для открытия сообщения электронной почты моделирования атаки быстрым (или самые медленные) раз щелкнуть ссылку в сообщении и многое другое.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p123">**Advanced reporting capabilities**. You'll be able to see data such as the fastest (or slowest) time to open an attack simulation email message, the fastest (or slowest) time to click a link in the message, and more.</span></span>
- <span data-ttu-id="ac1a3-p124">**Редактор шаблонов электронной почты**. Можно создать шаблон настраиваемого, для повторного использования электронной почты, которые можно использовать для моделирования будущих атаки.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-p124">**Email template editor**. You can create a custom, reusable email template that you can use for future attack simulations.</span></span>

<span data-ttu-id="ac1a3-199">Посетите [Стратегия Майкрософт 365](https://www.microsoft.com/microsoft-365/roadmap) возможности разработки, что вводит и что уже запущено.</span><span class="sxs-lookup"><span data-stu-id="ac1a3-199">Visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap) to see what's in development, what's rolling out, and what's already launched.</span></span>



