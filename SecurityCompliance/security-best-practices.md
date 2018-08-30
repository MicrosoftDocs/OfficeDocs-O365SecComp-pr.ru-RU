---
title: Рекомендации по обеспечению безопасности в Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: Снизить риск нарушение данных или атаке учетной записи, выполнив Далее рекомендациям.
ms.openlocfilehash: 245302af0b08a4ee8183345fc386fe47985c93dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535409"
---
# <a name="security-best-practices-for-office-365"></a><span data-ttu-id="b9c0a-103">Рекомендации по обеспечению безопасности в Office 365</span><span class="sxs-lookup"><span data-stu-id="b9c0a-103">Security best practices for Office 365</span></span>

<span data-ttu-id="b9c0a-104">Снизить риск нарушение данных или атаке учетной записи, выполнив Далее рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-104">Minimize the potential of a data breach or a compromised account by following these recommended best practices.</span></span>
  
<span data-ttu-id="b9c0a-p101">В этой статье содержит краткий список рекомендаций. Более глубокий анализ и сведения о настройке безопасности в разделе [план обеспечения безопасности Office 365: наиболее распространенные приоритеты для первого 30 дней, 90 дней и за ее пределами](security-roadmap.md). В этой статье вы найдете сведения на основании расследований реальных атак, где эксперты cybersecurity верхней Microsoft Office 365 обеспечивает обучения по оценки рисков и внедрения наиболее важных безопасности, соответствия требованиям и сведения о элементы управления защиты для защиты клиента Office 365. Вы узнаете, как определять приоритеты угрозы, связанные с, оставляют угрозы, связанные с технической стратегии и последующий перевод систематического подхода к реализации функции и элементы управления.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-p101">This article contains a quick list of best practices. For more in-depth analysis and information on setting up security, see [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](security-roadmap.md). In that article, you'll find information based on investigations of real-world attacks, where our top Microsoft Office 365 cybersecurity experts provide coaching on how to assess risk and implement the most critical security, compliance, and information protection controls to protect your Office 365 tenant. You'll learn how to prioritize threats, translate threats into technical strategy, and then take a systematic approach to implementing features and controls.</span></span>
  
## <a name="use-office-365-secure-score"></a><span data-ttu-id="b9c0a-109">Используйте оценку безопасности Office 365</span><span class="sxs-lookup"><span data-stu-id="b9c0a-109">Use Office 365 Secure Score</span></span>

<span data-ttu-id="b9c0a-p102">Безопасной показатель — это средство анализа безопасности, в котором рекомендуется, что вы можете сделать, чтобы снизить риск. Безопасной показатель рассматриваются параметры Office 365 и действия и сравнивает их базового, установленная корпорацией Майкрософт. Вы получите оценку, основанную на способ выравнивания осуществляется с помощью рекомендации по безопасности. Дополнительные сведения о том, как получить безопасного счета и используйте его для повышения безопасности организации Office 365 [Показатель безопасного Office 365](office-365-secure-score.md)см.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-p102">Secure Score is a security analytics tool that recommends what you can do to further reduce risk. Secure Score looks at your Office 365 settings and activities and compares them to a baseline established by Microsoft. You'll get a score based on how aligned you are with best security practices. For more information about how to get Secure Score and use it to increase the security of your Office 365 organization, see [Introducing the Office 365 Secure Score](office-365-secure-score.md).</span></span>
  
<span data-ttu-id="b9c0a-114">Хотите попробовать безопасного счета?</span><span class="sxs-lookup"><span data-stu-id="b9c0a-114">Want to try out Secure Score?</span></span>
  
<span data-ttu-id="b9c0a-115">С помощью учетной записи рабочего или школы, которому назначена роль Office 365 [роли администраторов об Office 365](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) , [войти в Office 365](https://www.office.com/signin).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-115">Using a work or school account that has been assigned the Office 365 [About Office 365 admin roles](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) role, [sign in to Office 365](https://www.office.com/signin).</span></span>
  
<span data-ttu-id="b9c0a-116">Показатель в безопасного доступа к [https://SecureScore.office.com](https://SecureScore.office.com).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-116">Access Secure Score at [https://SecureScore.office.com](https://SecureScore.office.com).</span></span>
  
## <a name="use-multi-factor-authentication-mfa"></a><span data-ttu-id="b9c0a-117">Используйте многофакторная проверка подлинности (многофакторной проверкой Подлинности)</span><span class="sxs-lookup"><span data-stu-id="b9c0a-117">Use multi-factor authentication (MFA)</span></span>

<span data-ttu-id="b9c0a-p103">Многофакторной проверкой Подлинности добавляет дополнительный уровень защиты стратегии надежный пароль, требуя от пользователей для подтверждения на телефонный звонок, текстовое сообщение или уведомление приложения на своем телефоне смарт-после правильно ввода пароля. С многофакторной проверкой Подлинности на месте учетными записями пользователей Office 365, по-прежнему защищены от несанкционированного доступа даже в том случае, если раскрыты пароля пользователя. Учетные записи защищены, так как не доступа к учетной записи до после дополнительная сложность были выполнены. Пароль атаке или украденных недостаточно.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-p103">MFA adds an additional layer of protection to a strong password strategy by requiring users to acknowledge a phone call, text message, or an app notification on their smart phone after correctly entering their password. With MFA in place, Office 365 user accounts are still protected against unauthorized access even if a user's password is compromised. Accounts are protected because access is not granted to an account until after the additional challenge has been satisfied. A compromised or stolen password is not enough.</span></span>
  
- [<span data-ttu-id="b9c0a-122">Планирование для многофакторной проверки подлинности для развертываний Office 365</span><span class="sxs-lookup"><span data-stu-id="b9c0a-122">Plan for multi-factor authentication for Office 365 Deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="b9c0a-123">Настройка многофакторной проверки подлинности для пользователей Office 365</span><span class="sxs-lookup"><span data-stu-id="b9c0a-123">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a><span data-ttu-id="b9c0a-124">Использование безопасности облаке приложения Office 365</span><span class="sxs-lookup"><span data-stu-id="b9c0a-124">Use Office 365 Cloud App Security</span></span>

<span data-ttu-id="b9c0a-p104">Настройка политик на основании потребностей бизнеса для отслеживания непредвиденных активности и реагировать на него. Настройка оповещений с помощью Office 365 облачных приложений безопасности, в котором администраторы могут просмотреть действие необычных или рискованный пользователя, такие как загрузка больших объемов данных, несколько сбой попыток входа или войти в систему от неизвестного или опасные IP-адрес. Для организаций с план Office 365 корпоративный E5 можно начать с помощью Office 365 облачных приложений безопасности немедленно. При наличии различных enterprise план, вы можете приобрести безопасности Office 365 облаке приложения как дополнительный компонент.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-p104">Set up policies based on your business needs to track anomalous activity and act on it. Set up alerts with Office 365 Cloud App Security so that admins can review unusual or risky user activity, such as downloading large amounts of data, multiple failed sign-in attempts, or sign-ins from an unknown or dangerous IP address. For organizations with an Office 365 Enterprise E5 plan, you can start using Office 365 Cloud App Security right away. If you have a different enterprise plan, you can purchase Office 365 Cloud App Security as an add-on.</span></span>
  
- [<span data-ttu-id="b9c0a-129">Общие сведения о безопасности приложения Cloud O365</span><span class="sxs-lookup"><span data-stu-id="b9c0a-129">Overview of O365 Cloud App Security</span></span>](office-365-cas-overview.md)
    
- [<span data-ttu-id="b9c0a-130">Включение Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b9c0a-130">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a><span data-ttu-id="b9c0a-131">Защиты потока электронной почты</span><span class="sxs-lookup"><span data-stu-id="b9c0a-131">Secure mail flow</span></span>

<span data-ttu-id="b9c0a-132">Реализация полнофункциональный набор в Exchange Online Protection возможностей и получить гарантии личность отправителя для каждого сообщения электронной почты и защита от неизвестного вредоносных программ, вирусов и вредоносного URL-адреса, передаваемых через по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-132">Implement the rich feature set in Exchange Online Protection and gain greater assurance about the identity of the sender of each email message, and protect against unknown malware, viruses, and malicious URLs transmitted through emails.</span></span>
  
- <span data-ttu-id="b9c0a-133">Настройка политик [Защиты от нежелательной почты Office 365 электронной почты](anti-spam-protection.md) для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-133">Configure [Office 365 Email Anti-Spam Protection](anti-spam-protection.md) policies for your organization.</span></span> 
    
- <span data-ttu-id="b9c0a-134">Описание, а затем с помощью [расширенной защитой для вложений надежных и безопасных ссылок](https://technet.microsoft.com/library/mt148491.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-134">Learn about and then use [Advanced threat protection for safe attachments and safe links](https://technet.microsoft.com/library/mt148491.aspx).</span></span>
    
- <span data-ttu-id="b9c0a-135">[Добавить защита от вредоносных программ в организации](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-135">[Add anti-malware protection to your organization](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).</span></span>
    
- <span data-ttu-id="b9c0a-136">Узнайте о и включить [Советы по безопасности в сообщениях электронной почты в Office 365](safety-tips-in-office-365.md) для пользователей.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-136">Learn about and enable [Safety tips in email messages in Office 365](safety-tips-in-office-365.md) for your users.</span></span> 
    
- <span data-ttu-id="b9c0a-137">При использовании настраиваемого домена для своей организации в Office 365, настройте SPF, ПРОВЕРКУ и DMARC для проверки почта, передаваемая вашей организацией и для предотвращения спуфинг:</span><span class="sxs-lookup"><span data-stu-id="b9c0a-137">If you're using a custom domain for your organization in Office 365, set up SPF, DKIM, and then DMARC to validate mail sent by your organization and to help prevent spoofing:</span></span>
    
  - <span data-ttu-id="b9c0a-138">[Настройка инфраструктуры политики Отправителей в Office 365 для предотвращения спуфинг](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-138">[Set up SPF in Office 365 to help prevent spoofing](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx).</span></span>
    
  - <span data-ttu-id="b9c0a-139">[Использовать ПРОВЕРКУ для проверки электронной почты, отправленной из настраиваемого домена в Office 365](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-139">[Use DKIM to validate outbound email sent from your custom domain in Office 365](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx).</span></span>
    
  - <span data-ttu-id="b9c0a-140">[DMARC используется для проверки электронной почты в Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-140">[Use DMARC to validate email in Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span></span>
    
## <a name="enable-mailbox-audit-logging"></a><span data-ttu-id="b9c0a-141">Включение ведения журнала аудита почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="b9c0a-141">Enable mailbox audit logging</span></span>

<span data-ttu-id="b9c0a-p105">Некоторые включено ведение журнала аудита автоматически для вас в Office 365; Тем не менее, ведение журнала аудита почтовых ящиков не включена по умолчанию. Включение ведения журнала аудита для всех почтовых ящиков пользователей в Office 365 с помощью Exchange Online PowerShell. Сведения можно [Включить аудит в Office 365 почтового ящика](https://go.microsoft.com/fwlink/p/?LinkID=626109).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-p105">Some audit logging is automatically enabled for you in Office 365; however, mailbox audit logging is not turned on by default. You turn on audit logging for all user mailboxes in Office 365 by using Exchange Online PowerShell. For information, see [Enable mailbox auditing in Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).</span></span>
  
<span data-ttu-id="b9c0a-p106">После включения ведения журнала, который аудита можно [Поиск в журнале аудита безопасности Office 365 &amp; центре соответствия требованиям](search-the-audit-log-in-security-and-compliance.md) чтобы узнать, кто вошедший в ваши почтовые ящики пользователей, отправленных сообщений и других действий, выполняемых владелец почтового ящика, делегированный пользователь или быть администратором. Список действий почтовых ящиков, включенных в Office 365 журнал аудита по умолчанию, отображаться [действия почтового ящика Exchange](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-p106">After you've enabled audit logging you can [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md) to find out who has logged into your user mailboxes, sent messages, and other activities performed by the mailbox owner, a delegated user, or an administrator. For a list of mailbox activities that are included in the Office 365 audit log by default, see [Exchange mailbox activities](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).</span></span>
  
<span data-ttu-id="b9c0a-147">Сведения о других действий, которые можно выполнять с помощью журнала аудита, такие как изменение временной интервал для сохранения записей в журнале аудита в разделе [Ведение журналов в Exchange 2016 аудита почтовых ящиков](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-147">For information about other actions you can perform with the audit log, such as changing the amount of time to save entries in the audit log, see [Mailbox audit logging in Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).</span></span>
  
## <a name="configure-data-loss-prevention-dlp"></a><span data-ttu-id="b9c0a-148">Настройка защиты от потери данных (DLP)</span><span class="sxs-lookup"><span data-stu-id="b9c0a-148">Configure Data Loss Prevention (DLP)</span></span>

<span data-ttu-id="b9c0a-p107">Защиты от потери данных можно определить конфиденциальные данные и создать политики, которые помогают предотвратить пользователи случайно или специально общего доступа к данным. Защиты от потери данных работает в Office 365, включая Exchange Online, SharePoint Online и OneDrive, чтобы пользователи могли оставаться спецификации, не прерывая их рабочего процесса. Для получения дополнительных сведений см [политики предотвращения потери данных](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-p107">DLP allows you to identify sensitive data and create policies that help prevent your users from accidentally or intentionally sharing the data. DLP works across Office 365 including Exchange Online, SharePoint Online, and OneDrive so that your users can stay compliant without interrupting their workflow. For more information, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
## <a name="use-customer-lockbox"></a><span data-ttu-id="b9c0a-152">Использование защищенного хранилища клиента</span><span class="sxs-lookup"><span data-stu-id="b9c0a-152">Use Customer Lockbox</span></span>

<span data-ttu-id="b9c0a-p108">Как администратор Office 365 защищенного хранилища клиента можно использовать для управления доступ данных во время сеанса справки сотрудник службы поддержки Майкрософт. В тех случаях, когда инженер требуется доступ к данным в диагностике и устранении неполадок защищенного хранилища клиента позволяет утвердить или отклонить запрос доступа. Если утверждения, инженер доступом к данным. Каждый запрос имеет срок его действия и после неполадки, запрос закрывается доступ отозван. Защищенного хранилища клиента включена в план Office 365 корпоративный 5, или вы можете приобрести отдельные подписки с другими плана корпоративного Office 365. Сведения можно [Запросы защищенного хранилища клиента Office 365](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).</span><span class="sxs-lookup"><span data-stu-id="b9c0a-p108">As an Office 365 admin, you can use Customer Lockbox to control how a Microsoft support engineer accesses your data during a help session. In cases where the engineer requires access to your data to troubleshoot and fix an issue, Customer Lockbox allows you to approve or reject the access request. If you approve it, the engineer can access the data. Each request has an expiration time, and once the issue is resolved, the request is closed and access is revoked. Customer Lockbox is included in the Office 365 Enterprise 5 plan, or you can purchase a separate subscription with any other Office 365 enterprise plan. For information, see [Office 365 Customer Lockbox Requests](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).</span></span>
  
## <a name="try-it-yourself"></a><span data-ttu-id="b9c0a-159">Попробуйте вручную</span><span class="sxs-lookup"><span data-stu-id="b9c0a-159">Try it yourself</span></span>
<span data-ttu-id="b9c0a-160"><a name="SecureScore"> </a></span><span class="sxs-lookup"><span data-stu-id="b9c0a-160"></span></span>

<span data-ttu-id="b9c0a-161">Просмотрите эти функции безопасности, работающих в пробную подписку на Office 365 перед принять их в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="b9c0a-161">See these security features working in an Office 365 trial subscription prior to adopting them in production.</span></span>
  
- [<span data-ttu-id="b9c0a-162">Создайте пробную подписку на Office 365</span><span class="sxs-lookup"><span data-stu-id="b9c0a-162">Create an Office 365 trial subscription</span></span>](https://technet.microsoft.com/library/mt736406.aspx)
    
- [<span data-ttu-id="b9c0a-163">Настройки и тестирования многофакторной проверкой Подлинности для учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="b9c0a-163">Configure and test MFA for a user account</span></span>](https://technet.microsoft.com/library/mt492459.aspx)
    
- [<span data-ttu-id="b9c0a-164">Настройки и тестирования безопасности Office 365 облаке приложения для уведомления пользователя об активности глобального администратора</span><span class="sxs-lookup"><span data-stu-id="b9c0a-164">Configure and test Office 365 Cloud App Security to notify you of global admin activity</span></span>](https://technet.microsoft.com/library/mt757250.aspx)
    
- [<span data-ttu-id="b9c0a-165">Настройки и тестирования ATP для подозрительных сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="b9c0a-165">Configure and test ATP for suspicious email</span></span>](https://technet.microsoft.com/library/mt490479.aspx)
    
- <span data-ttu-id="b9c0a-166">Проверьте [Счета безопасного Office 365](https://securescore.office.com/) для пробной подписки для каждого из приведенных выше шагов</span><span class="sxs-lookup"><span data-stu-id="b9c0a-166">Check the [Office 365 Secure Score](https://securescore.office.com/) for your trial subscription for each of the above steps</span></span> 
    

