---
title: Рекомендации по обеспечению безопасности в Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
- MET150
ms.assetid: 9295e396-e53d-49b9-ae9b-0b5828cdedc3
description: Чтобы свести к минимуму вероятность нарушения данных или скомпрометированных учетных записей, следуйте приведенным ниже рекомендациям.
ms.openlocfilehash: d40fa5e4534bef1bb8389989022c44967a162aee
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212819"
---
# <a name="security-best-practices-for-office-365"></a><span data-ttu-id="83796-103">Рекомендации по обеспечению безопасности в Office 365</span><span class="sxs-lookup"><span data-stu-id="83796-103">Security best practices for Office 365</span></span>

<span data-ttu-id="83796-104">Чтобы свести к минимуму вероятность нарушения данных или скомпрометированных учетных записей, следуйте приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="83796-104">Minimize the potential of a data breach or a compromised account by following these recommended best practices.</span></span>
  
<span data-ttu-id="83796-p101">В этой статье приведен краткий список рекомендаций. Более подробные сведения о настройке безопасности можно найти в статье [Office 365 Security Security: Top приоритеты для первых 30 дней, 90 дней и](security-roadmap.md)более поздних. В этой статье вы найдете информацию, основанную на расследовании реальных атак, где наши лучшие специалисты по Microsoft Office 365 циберсекурити предоставляют сведения о том, как оценивать риски и реализовывать наиболее важные вопросы безопасности, соответствия требованиям и информации. элементы управления защитой для защиты клиента Office 365. Вы узнаете, как определять приоритет угроз, преобразовывать угрозы в техническую стратегию, а затем делать систематический подход к внедрению функций и элементов управления.</span><span class="sxs-lookup"><span data-stu-id="83796-p101">This article contains a quick list of best practices. For more in-depth analysis and information on setting up security, see [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](security-roadmap.md). In that article, you'll find information based on investigations of real-world attacks, where our top Microsoft Office 365 cybersecurity experts provide coaching on how to assess risk and implement the most critical security, compliance, and information protection controls to protect your Office 365 tenant. You'll learn how to prioritize threats, translate threats into technical strategy, and then take a systematic approach to implementing features and controls.</span></span>
  
## <a name="use-office-365-secure-score"></a><span data-ttu-id="83796-109">Использование оценки безопасности Office 365</span><span class="sxs-lookup"><span data-stu-id="83796-109">Use Office 365 Secure Score</span></span>

<span data-ttu-id="83796-p102">Показатель безопасности — это средство аналитики безопасности, в котором описывается, что можно сделать для дальнейшего снижения риска. Показатель безопасности рассматривает параметры и действия Office 365 и сравнивает их с базовым планом, установленным корпорацией Майкрософт. Вы получите оценку на основе соответствия рекомендациям по обеспечению безопасности. Для получения дополнительных сведений о том, как получить оценку безопасности и использовать ее для повышения безопасности вашей организации Office 365, ознакомьтесь со статьей, посвященной [безопасной оценке office 365](office-365-secure-score.md).</span><span class="sxs-lookup"><span data-stu-id="83796-p102">Secure Score is a security analytics tool that recommends what you can do to further reduce risk. Secure Score looks at your Office 365 settings and activities and compares them to a baseline established by Microsoft. You'll get a score based on how aligned you are with best security practices. For more information about how to get Secure Score and use it to increase the security of your Office 365 organization, see [Introducing the Office 365 Secure Score](office-365-secure-score.md).</span></span>
  
<span data-ttu-id="83796-114">Хотите испытать оценку безопасности?</span><span class="sxs-lookup"><span data-stu-id="83796-114">Want to try out Secure Score?</span></span>
  
<span data-ttu-id="83796-115">С помощью рабочей или учебной учетной записи, которой назначена роль администратора Office 365 для Office [365](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) , [войдите в Office 365](https://www.office.com/signin).</span><span class="sxs-lookup"><span data-stu-id="83796-115">Using a work or school account that has been assigned the Office 365 [About Office 365 admin roles](https://support.office.com/article/da585eea-f576-4f55-a1e0-87090b6aaa9d) role, [sign in to Office 365](https://www.office.com/signin).</span></span>
  
<span data-ttu-id="83796-116">Оценка безопасности доступа по [https://SecureScore.office.com](https://SecureScore.office.com)адресу.</span><span class="sxs-lookup"><span data-stu-id="83796-116">Access Secure Score at [https://SecureScore.office.com](https://SecureScore.office.com).</span></span>
  
## <a name="use-multi-factor-authentication-mfa"></a><span data-ttu-id="83796-117">Использование многофакторной проверки подлинности (MFA)</span><span class="sxs-lookup"><span data-stu-id="83796-117">Use multi-factor authentication (MFA)</span></span>

<span data-ttu-id="83796-p103">MFA добавляет дополнительный уровень защиты в стратегию надежных паролей, требуя от пользователей подтвердить телефонный звонок, текстовое сообщение или уведомление приложения на смарт-телефоне после правильного ввода пароля. При использовании MFA учетные записи пользователей Office 365 по-прежнему защищены от несанкционированного доступа, даже если пароль пользователя скомпрометирован. Учетные записи защищены, так как доступ не предоставляется учетной записи до тех пор, пока не будет удовлетворен дополнительный запрос. Скомпрометированный или украденный пароль недостаточно.</span><span class="sxs-lookup"><span data-stu-id="83796-p103">MFA adds an additional layer of protection to a strong password strategy by requiring users to acknowledge a phone call, text message, or an app notification on their smart phone after correctly entering their password. With MFA in place, Office 365 user accounts are still protected against unauthorized access even if a user's password is compromised. Accounts are protected because access is not granted to an account until after the additional challenge has been satisfied. A compromised or stolen password is not enough.</span></span>
  
- [<span data-ttu-id="83796-122">Планирование многофакторной проверки подлинности для развертываний Office 365</span><span class="sxs-lookup"><span data-stu-id="83796-122">Plan for multi-factor authentication for Office 365 Deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="83796-123">Настройка многофакторной проверки подлинности для пользователей Office 365</span><span class="sxs-lookup"><span data-stu-id="83796-123">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
## <a name="use-office-365-cloud-app-security"></a><span data-ttu-id="83796-124">Использование Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="83796-124">Use Office 365 Cloud App Security</span></span>

<span data-ttu-id="83796-p104">Настройка политик на основе бизнес-потребностей для отслеживания аномальных действий и выполнения действий над ней. Настройте оповещения с помощью Office 365 Cloud App Security, чтобы администраторы могли просматривать необычные или рискованные действия пользователей, такие как загрузка больших объемов данных, несколько неудачных попыток входа или вход из неизвестного или опасного IP-адреса. Для организаций, использующих план Office 365 корпоративный, вы можете сразу же начать использовать Office 365 Cloud App Security. Если у вас другой план предприятия, вы можете приобрести Office 365 Cloud App Security в качестве надстройки.</span><span class="sxs-lookup"><span data-stu-id="83796-p104">Set up policies based on your business needs to track anomalous activity and act on it. Set up alerts with Office 365 Cloud App Security so that admins can review unusual or risky user activity, such as downloading large amounts of data, multiple failed sign-in attempts, or sign-ins from an unknown or dangerous IP address. For organizations with an Office 365 Enterprise E5 plan, you can start using Office 365 Cloud App Security right away. If you have a different enterprise plan, you can purchase Office 365 Cloud App Security as an add-on.</span></span>
  
- [<span data-ttu-id="83796-129">Общие сведения о Cloud App Security для Office 365</span><span class="sxs-lookup"><span data-stu-id="83796-129">Overview of O365 Cloud App Security</span></span>](office-365-cas-overview.md)
    
- [<span data-ttu-id="83796-130">Включение Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="83796-130">Turn on Office 365 Cloud App Security</span></span>](turn-on-office-365-cas.md)
    
## <a name="secure-mail-flow"></a><span data-ttu-id="83796-131">Безопасный процесс обработки почты</span><span class="sxs-lookup"><span data-stu-id="83796-131">Secure mail flow</span></span>

<span data-ttu-id="83796-132">Реализуйте богатый набор функций в Exchange Online Protection и получите более высокую гарантию подлинности отправителя каждого сообщения электронной почты и защититься от неизвестных вредоносных программ, вирусов и вредоносных URL-адресов, передаваемых по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="83796-132">Implement the rich feature set in Exchange Online Protection and gain greater assurance about the identity of the sender of each email message, and protect against unknown malware, viruses, and malicious URLs transmitted through emails.</span></span>
  
- <span data-ttu-id="83796-133">Настройка политик [защиты от нежелательной почты в Office 365](anti-spam-protection.md) для Организации.</span><span class="sxs-lookup"><span data-stu-id="83796-133">Configure [Office 365 Email Anti-Spam Protection](anti-spam-protection.md) policies for your organization.</span></span> 
    
- <span data-ttu-id="83796-134">Узнайте, а затем используйте [расширенную защиту от угроз для безопасных вложений и безопасных ссылок](https://technet.microsoft.com/library/mt148491.aspx).</span><span class="sxs-lookup"><span data-stu-id="83796-134">Learn about and then use [Advanced threat protection for safe attachments and safe links](https://technet.microsoft.com/library/mt148491.aspx).</span></span>
    
- <span data-ttu-id="83796-135">[Добавление защиты от вредоносных программ в Организации](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="83796-135">[Add anti-malware protection to your organization](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx).</span></span>
    
- <span data-ttu-id="83796-136">Сведения о безопасности и включении [советов по безопасности в сообщениях электронной почты в Office 365](safety-tips-in-office-365.md) для пользователей.</span><span class="sxs-lookup"><span data-stu-id="83796-136">Learn about and enable [Safety tips in email messages in Office 365](safety-tips-in-office-365.md) for your users.</span></span> 
    
- <span data-ttu-id="83796-137">Если вы используете личный домен для Организации в Office 365, настройте SPF, DKIM, а затем DMARC, чтобы проверить почту, отправленную вашей организацией, и предотвратить подмену данных:</span><span class="sxs-lookup"><span data-stu-id="83796-137">If you're using a custom domain for your organization in Office 365, set up SPF, DKIM, and then DMARC to validate mail sent by your organization and to help prevent spoofing:</span></span>
    
  - <span data-ttu-id="83796-138">[Настройте SPF в Office 365, чтобы предотвратить подмену](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span><span class="sxs-lookup"><span data-stu-id="83796-138">[Set up SPF in Office 365 to help prevent spoofing](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span></span>
    
  - <span data-ttu-id="83796-139">[Используйте DKIM для проверки исходящей электронной почты, отправленной из личного домена в Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span><span class="sxs-lookup"><span data-stu-id="83796-139">[Use DKIM to validate outbound email sent from your custom domain in Office 365](https://docs.microsoft.com/office365/SecurityCompliance/set-up-spf-in-office-365-to-help-prevent-spoofing).</span></span>
    
  - <span data-ttu-id="83796-140">[Используйте DMARC для проверки электронной почты в Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="83796-140">[Use DMARC to validate email in Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).</span></span>
    
## <a name="enable-mailbox-audit-logging"></a><span data-ttu-id="83796-141">Включение ведения журнала аудита почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="83796-141">Enable mailbox audit logging</span></span>

<span data-ttu-id="83796-p105">В Office 365 для вас автоматически включено ведение журнала аудита. Однако ведение журнала аудита почтовых ящиков по умолчанию отключено. Вы включаете ведение журнала аудита для всех почтовых ящиков пользователей в Office 365 с помощью Exchange Online PowerShell. Сведения о том, как [включить аудит почтовых ящиков в Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).</span><span class="sxs-lookup"><span data-stu-id="83796-p105">Some audit logging is automatically enabled for you in Office 365; however, mailbox audit logging is not turned on by default. You turn on audit logging for all user mailboxes in Office 365 by using Exchange Online PowerShell. For information, see [Enable mailbox auditing in Office 365](https://go.microsoft.com/fwlink/p/?LinkID=626109).</span></span>
  
<span data-ttu-id="83796-p106">После включения ведения журнала аудита вы можете [выполнить поиск в журнале аудита в центре безопасности &amp; и соответствия требованиям Office 365](search-the-audit-log-in-security-and-compliance.md) , чтобы узнать, кто вошел в почтовые ящики пользователей, отправленные сообщения и другие действия, выполняемые владельцем почтового ящика, делегированным пользователем, или администратором. Список действий почтовых ящиков, включенных в журнал аудита Office 365 по умолчанию, можно узнать в статье действия с почтовыми [ящикАми Exchange](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).</span><span class="sxs-lookup"><span data-stu-id="83796-p106">After you've enabled audit logging you can [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md) to find out who has logged into your user mailboxes, sent messages, and other activities performed by the mailbox owner, a delegated user, or an administrator. For a list of mailbox activities that are included in the Office 365 audit log by default, see [Exchange mailbox activities](search-the-audit-log-in-security-and-compliance.md#exchange-mailbox-activities).</span></span>
  
<span data-ttu-id="83796-147">Сведения о других действиях, которые можно выполнять с журналом аудита, например изменение количества времени для сохранения записей в журнале аудита, можно найти в разделе [ведение журнала аудита почтовоГо ящика в Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="83796-147">For information about other actions you can perform with the audit log, such as changing the amount of time to save entries in the audit log, see [Mailbox audit logging in Exchange 2016](https://technet.microsoft.com/en-us/library/ff459237%28v=exchg.160%29.aspx).</span></span>
  
## <a name="configure-data-loss-prevention-dlp"></a><span data-ttu-id="83796-148">Настройка защиты от потери данных (DLP)</span><span class="sxs-lookup"><span data-stu-id="83796-148">Configure Data Loss Prevention (DLP)</span></span>

<span data-ttu-id="83796-p107">DLP позволяет определять конфиденциальные данные и создавать политики, которые помогают предотвратить случайное или намеренное совместное использование данных пользователями. DLP работает в Office 365, включая Exchange Online, SharePoint Online и OneDrive, чтобы пользователи могли оставаться соответствующими, не прерывая рабочий процесс. Дополнительные сведения можно найти в статье [Обзор политик защиты от потери данных](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="83796-p107">DLP allows you to identify sensitive data and create policies that help prevent your users from accidentally or intentionally sharing the data. DLP works across Office 365 including Exchange Online, SharePoint Online, and OneDrive so that your users can stay compliant without interrupting their workflow. For more information, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
## <a name="use-customer-lockbox"></a><span data-ttu-id="83796-152">Использование защищенного хранилища клиентов</span><span class="sxs-lookup"><span data-stu-id="83796-152">Use Customer Lockbox</span></span>

<span data-ttu-id="83796-p108">Как администратор Office 365, вы можете использовать защищенное хранилище клиентов для управления доступом к данным специалистом службы поддержки Майкрософт во время сеанса справки. В тех случаях, когда специалисту требуется доступ к данным для устранения неполадок и устранения проблем, защищенное хранилище клиента позволяет утверждать или отклонять запросы на доступ. Если вы утверждаете его, инженер может получить доступ к данным. Каждый запрос имеет срок действия, и после устранения проблемы запрос будет закрыт, а доступ будет отозван. Защищенный доступ клиентов включен в план Office 365 корпоративный, или вы можете приобрести отдельную подписку с любым другим планом Office 365 корпоративный. Сведения о том, как получить сведения о [клиентах защищенНого хранилища Office 365](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).</span><span class="sxs-lookup"><span data-stu-id="83796-p108">As an Office 365 admin, you can use Customer Lockbox to control how a Microsoft support engineer accesses your data during a help session. In cases where the engineer requires access to your data to troubleshoot and fix an issue, Customer Lockbox allows you to approve or reject the access request. If you approve it, the engineer can access the data. Each request has an expiration time, and once the issue is resolved, the request is closed and access is revoked. Customer Lockbox is included in the Office 365 Enterprise E5 plan, or you can purchase a separate subscription with any other Office 365 enterprise plan. For information, see [Office 365 Customer Lockbox Requests](https://support.office.com/article/36f9cdd1-e64c-421b-a7e4-4a54d16440a2).</span></span>
  
## <a name="try-it-yourself"></a><span data-ttu-id="83796-159">Пробная проверка</span><span class="sxs-lookup"><span data-stu-id="83796-159">Try it yourself</span></span>
<span data-ttu-id="83796-160"><a name="SecureScore"> </a></span><span class="sxs-lookup"><span data-stu-id="83796-160"></span></span>

<span data-ttu-id="83796-161">Ознакомьтесь с этими функциями безопасности, которые работают в пробной подписке Office 365, прежде чем приступать к ним в рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="83796-161">See these security features working in an Office 365 trial subscription prior to adopting them in production.</span></span>
  
- [<span data-ttu-id="83796-162">Создание пробной подписки на Office 365</span><span class="sxs-lookup"><span data-stu-id="83796-162">Create an Office 365 trial subscription</span></span>](https://technet.microsoft.com/library/mt736406.aspx)
    
- [<span data-ttu-id="83796-163">Настройка и проверка MFA для учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="83796-163">Configure and test MFA for a user account</span></span>](https://technet.microsoft.com/library/mt492459.aspx)
    
- [<span data-ttu-id="83796-164">Настройте и проверьте Office 365 Cloud App Security, чтобы уведомить вас о глобальных действиях администратора</span><span class="sxs-lookup"><span data-stu-id="83796-164">Configure and test Office 365 Cloud App Security to notify you of global admin activity</span></span>](https://technet.microsoft.com/library/mt757250.aspx)
    
- [<span data-ttu-id="83796-165">Настройка и тестирование ATP для подозрительных сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="83796-165">Configure and test ATP for suspicious email</span></span>](https://technet.microsoft.com/library/mt490479.aspx)
    
- <span data-ttu-id="83796-166">Проверьте правильность [оценки безопасности Office 365](https://securescore.office.com/) для пробной подписки, выполнив указанные выше действия.</span><span class="sxs-lookup"><span data-stu-id="83796-166">Check the [Office 365 Secure Score](https://securescore.office.com/) for your trial subscription for each of the above steps</span></span> 
    

