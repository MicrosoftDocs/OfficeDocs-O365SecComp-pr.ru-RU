---
title: Автоматическое исследование и ответ (AIR) с Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/22/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Сведения об автоматическом расследовании и возможностях реагирования в Office 365 Advanced Threat protection.
ms.openlocfilehash: c6cfc03588e580382f673b2e9be8543bfcaf9ac1
ms.sourcegitcommit: f6073deec39a18581ed12abef18728417a52cdf4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2019
ms.locfileid: "30747565"
---
# <a name="automated-investigation-and-response-air-with-office-365"></a><span data-ttu-id="7e66c-103">Автоматическое исследование и ответ (AIR) с Office 365</span><span class="sxs-lookup"><span data-stu-id="7e66c-103">Automated Investigation and Response (AIR) with Office 365</span></span>

<span data-ttu-id="7e66c-104">Автоматическое исследование и ответ (AIR) (в скором времени в [Office 365 для расследования угроз и возможностей реагирования](office-365-ti.md)) позволяют выполнять автоматическое исследование и устранение известных угроз, существующих сегодня.</span><span class="sxs-lookup"><span data-stu-id="7e66c-104">Automated Investigation and Response (AIR) (coming soon to [Office 365 Threat investigation and response capabilities](office-365-ti.md)) enables you to run automated investigation and remediation to well-known threats that exist today.</span></span> <span data-ttu-id="7e66c-105">В этой статье приводятся общие сведения о AIR и о том, как она может помочь организациям и системам безопасности Teams, а также повысить эффективность и эффективность работы.</span><span class="sxs-lookup"><span data-stu-id="7e66c-105">Read this article to get an overview of AIR and how it can help your organization and security operations teams mitigate threats more effectively and efficiently.</span></span> <span data-ttu-id="7e66c-106">Дополнительные сведения о том, когда станут доступны дополнительные функции в среде AIR, можно найти в [статье план Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="7e66c-106">To learn more about when additional features in AIR will be available, see the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

## <a name="alerts"></a><span data-ttu-id="7e66c-107">Оповещения</span><span class="sxs-lookup"><span data-stu-id="7e66c-107">Alerts</span></span>

<span data-ttu-id="7e66c-108">[Оповещения](alert-policies.md#viewing-alerts) представляют триггеры для рабочих процессов группы операций безопасности для реагирования на инциденты.</span><span class="sxs-lookup"><span data-stu-id="7e66c-108">[Alerts](alert-policies.md#viewing-alerts) represent triggers for Security Operations team workflows for incident response.</span></span> <span data-ttu-id="7e66c-109">Приоритизация правильного набора оповещений для проведения расследования, чтобы убедиться, что угрозы не являются неадресными.</span><span class="sxs-lookup"><span data-stu-id="7e66c-109">Prioritizing the right set of alerts for investigation while making sure no threats are unaddressed is challenging.</span></span> <span data-ttu-id="7e66c-110">При расследовании в оповещениях выполняются вручную, поэтому Teams должны осуществлять слежение за сущностями (например, контент, устройства и пользователей) от угроз.</span><span class="sxs-lookup"><span data-stu-id="7e66c-110">When investigations into alerts are performed manually, Security Operations teams must hunt and correlate entities (e.g. content, devices and users) at risk from threats.</span></span> <span data-ttu-id="7e66c-111">Такие задачи и рабочие процессы занимают много времени и используют несколько средств и систем.</span><span class="sxs-lookup"><span data-stu-id="7e66c-111">Such tasks and workflows are very time consuming and involve multiple tools and systems.</span></span> <span data-ttu-id="7e66c-112">В среде AIR исследование и отклики автоматизированы по ключевым угрозам безопасности и управлению угрозами, которые автоматически инициируют ответ безопасности "Playbooks".</span><span class="sxs-lookup"><span data-stu-id="7e66c-112">With AIR, investigation and response are automated into key security and threat management alerts that trigger your security response playbooks automatically.</span></span> 

<span data-ttu-id="7e66c-113">В первоначальном выпуске воздуха в апреле 2019 оповещения, созданные на основе политик оповещений о событиях синжел, будут автоматически исследованы.</span><span class="sxs-lookup"><span data-stu-id="7e66c-113">In the initial release of AIR in April 2019, alerts generated from following singel events alert policies will be auto-investigated.</span></span> 

1. <span data-ttu-id="7e66c-114">Обнаружен потенциально вредоносный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7e66c-114">A potentially malicious URL click was detected</span></span>
2. <span data-ttu-id="7e66c-115">Сообщение электронной почты, предоставленное пользователем как фишинга \*</span><span class="sxs-lookup"><span data-stu-id="7e66c-115">Email reported by user as phish\*</span></span>
3. <span data-ttu-id="7e66c-116">Сообщения электронной почты, содержащие вредоносную программу, удалена после доставки \*</span><span class="sxs-lookup"><span data-stu-id="7e66c-116">Email messages containing malware removed after delivery\*</span></span>
4. <span data-ttu-id="7e66c-117">Сообщения электронной почты, содержащие URL-адреса фишинга, удаленные после доставки \*</span><span class="sxs-lookup"><span data-stu-id="7e66c-117">Email messages containing phish URLs removed after delivery\*</span></span>

<span data-ttu-id="7e66c-118">\* Примечание: этим оповещениям были назначены "информационные" уровни в соответствующих политиках оповещений в центре безопасности и соответствия требованиям с отключенными уведомлениями по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="7e66c-118">\*Note: These alerts have been assigned an "Informational" severity in the respective alert policies within the Security and Compliance Center with email notifications turned off.</span></span> <span data-ttu-id="7e66c-119">Их можно включить с помощью конфигурации политики оповещений.</span><span class="sxs-lookup"><span data-stu-id="7e66c-119">These can be turned on through the Alert policy configuration.</span></span>

<span data-ttu-id="7e66c-120">чтобы просмотреть оповещения, в центре безопасности _амп_ соответствия требованиям Office 365 выберите **alerts** > **view alerts**.</span><span class="sxs-lookup"><span data-stu-id="7e66c-120">To view alerts, in the Office 365 Security & Compliance Center, choose **Alerts** > **View alerts**.</span></span> <span data-ttu-id="7e66c-121">Выберите оповещение, чтобы просмотреть сведения о нем, а затем воспользуйтесь ссылкой **Просмотр расследования** , чтобы перейти к соответствующему [исследованию](#investigation-graph).</span><span class="sxs-lookup"><span data-stu-id="7e66c-121">Select an alert to view its details, and from there, use the **View investigation** link to go to the corresponding [investigation](#investigation-graph).</span></span>

![Оповещения, ссылающиеся на расследования](media/air-alerts-page-details.png) 


## <a name="security-playbooks"></a><span data-ttu-id="7e66c-123">"Playbooks" безопасности</span><span class="sxs-lookup"><span data-stu-id="7e66c-123">Security playbooks</span></span>

<span data-ttu-id="7e66c-124">"Playbooks" безопасности — это внутренние политики, которые находятся в сердце автоматизации в защите от угроз Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7e66c-124">Security playbooks are back-end policies that are at the heart of automation in Microsoft Threat Protection.</span></span> <span data-ttu-id="7e66c-125">"Playbooks" безопасности, предоставляемые в среде AIR, основаны на распространенных реальных сценариях безопасности.</span><span class="sxs-lookup"><span data-stu-id="7e66c-125">The security playbooks provided in AIR are based on common real-world security scenarios.</span></span> <span data-ttu-id="7e66c-126">Стратегия безопасности запускается автоматически при активации оповещения в Организации.</span><span class="sxs-lookup"><span data-stu-id="7e66c-126">A security playbook is launched automatically when an alert is triggered within your organization.</span></span> <span data-ttu-id="7e66c-127">После срабатывания триггера оповещения связанный стратегия запускается автоматически.</span><span class="sxs-lookup"><span data-stu-id="7e66c-127">Once the alert triggers, the associated playbook is run automatically.</span></span> <span data-ttu-id="7e66c-128">В стратегия выполняется исследование со всеми связанными метаданными (в том числе сообщениями электронной почты, пользователями, субъектами, отправителями и т. д.) и, в зависимости от полученных результатов, рекомендуется набор действий, которые Группа безопасности Организации может использовать для управления и устранения проблем. угроза.</span><span class="sxs-lookup"><span data-stu-id="7e66c-128">The playbook runs an investigation, looking at all the associated metadata (including email messages, users, subjects, senders, etc.) and, based on its findings, recommends a set of actions that your organization's security team can take to control and mitigate the threat.</span></span> 

<span data-ttu-id="7e66c-129">"Playbooks" по обеспечению безопасности, которые вы будете получать с помощью воздуха, предназначены для самых распространенных угроз, которые в настоящее время сталкиваются с организациями.</span><span class="sxs-lookup"><span data-stu-id="7e66c-129">The security playbooks you'll get with AIR are designed to tackle the most frequent threats that organizations face today.</span></span> <span data-ttu-id="7e66c-130">Они основываются на входных данных из операций безопасности и команд реагирования на инциденты, в том числе те, кто помогает защищать ресурсы Майкрософт и наших клиентов.</span><span class="sxs-lookup"><span data-stu-id="7e66c-130">They're based on input from Security Operations and Incident Response teams, including those who help defend Microsoft and our customers assets.</span></span>

### <a name="security-playbooks-are-rolling-out-in-phases"></a><span data-ttu-id="7e66c-131">Этапы безопасности "Playbooks"</span><span class="sxs-lookup"><span data-stu-id="7e66c-131">Security playbooks are rolling out in phases</span></span>

<span data-ttu-id="7e66c-132">Как часть воздуха, "Playbooks" безопасности — это этапы развертывания.</span><span class="sxs-lookup"><span data-stu-id="7e66c-132">As part of AIR, security playbooks are rolling out in phases</span></span>

- <span data-ttu-id="7e66c-133">**Этап 1 (апрель 2019)**: "Playbooks" включает рекомендации по действиям, которые администраторы безопасности просматривают и утверждают.</span><span class="sxs-lookup"><span data-stu-id="7e66c-133">**Phase 1 (April 2019)**: Playbooks include recommendations for actions that security administrators review and approve.</span></span> 

- <span data-ttu-id="7e66c-134">**Этап 2 (июнь 2019)**: Администраторы безопасности будут иметь возможность настройки безопасности "Playbooks" для автоматического выполнения действий без участия администратора.</span><span class="sxs-lookup"><span data-stu-id="7e66c-134">**Phase 2 (June 2019)**: Security administrators will have the option to configure security playbooks to take action automatically, without administrative interaction.</span></span>

<span data-ttu-id="7e66c-135">Этап 1 будет включать следующие "Playbooks":</span><span class="sxs-lookup"><span data-stu-id="7e66c-135">Phase 1 will include the following playbooks:</span></span>
- <span data-ttu-id="7e66c-136">Сообщение о phishing-атаке, сообщенное пользователем</span><span class="sxs-lookup"><span data-stu-id="7e66c-136">User-reported phish message</span></span>
- <span data-ttu-id="7e66c-137">URL-адрес нажмите кнопку вредоносности Change (изменить)</span><span class="sxs-lookup"><span data-stu-id="7e66c-137">URL click verdict change</span></span> 
- <span data-ttu-id="7e66c-138">Вредоносная программа обнаружила пост-Delivery (вредоносный ZAP)</span><span class="sxs-lookup"><span data-stu-id="7e66c-138">Malware detected post-delivery (Malware ZAP)</span></span>
- <span data-ttu-id="7e66c-139">АнтиФишинг обнаружил, что после доставки ZAP (фишинг ZAP)</span><span class="sxs-lookup"><span data-stu-id="7e66c-139">Phish detected post-delivery ZAP (Phish ZAP)</span></span>
- <span data-ttu-id="7e66c-140">Ручное расследования по электронной почте (с помощью обозревателя угроз)</span><span class="sxs-lookup"><span data-stu-id="7e66c-140">Manual e-mail investigations (using Threat Explorer)</span></span>

<span data-ttu-id="7e66c-141">Некоторые другие "Playbooks" запланированы на этапе 2.</span><span class="sxs-lookup"><span data-stu-id="7e66c-141">Several other playbooks are planned for Phase 2.</span></span>

### <a name="playbooks-include-investigation-and-recommendations"></a><span data-ttu-id="7e66c-142">"Playbooks": исследование и рекомендации</span><span class="sxs-lookup"><span data-stu-id="7e66c-142">Playbooks include investigation and recommendations</span></span>

<span data-ttu-id="7e66c-143">Каждый стратегия включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="7e66c-143">Each playbook includes:</span></span> 
- <span data-ttu-id="7e66c-144">корневое исследование,</span><span class="sxs-lookup"><span data-stu-id="7e66c-144">a root investigation,</span></span> 
- <span data-ttu-id="7e66c-145">действия, предпринимаемые для определения и сопоставления других потенциальных угроз, а также</span><span class="sxs-lookup"><span data-stu-id="7e66c-145">steps taken to identify and correlate other potential threats, and</span></span> 
- <span data-ttu-id="7e66c-146">Рекомендуемые действия по исправлению угроз.</span><span class="sxs-lookup"><span data-stu-id="7e66c-146">recommended threat remediation actions.</span></span>

<span data-ttu-id="7e66c-147">Каждый этап высокого уровня включает множество подшагов, которые выполняются для предоставления детальных, подробных и исчерпывающих ответов на угрозы.</span><span class="sxs-lookup"><span data-stu-id="7e66c-147">Each high-level step includes many sub-steps that are executed to provide a deep, detailed, and exhaustive response to threats.</span></span>

## <a name="example-user-reported-phish-message"></a><span data-ttu-id="7e66c-148">Пример: сообщение фишинга, зарегистрированное пользователем</span><span class="sxs-lookup"><span data-stu-id="7e66c-148">Example: User-reported phish message</span></span>

<span data-ttu-id="7e66c-149">Когда пользователь в Организации отправляет сообщение электронной почты и отправляет его в корпорацию Майкрософт с помощью надстройки [Report Message для Outlook или Outlook Web Access](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="7e66c-149">When a user in your organization submits an email message and reports it to Microsoft by using the [Report Message add-in for Outlook or Outlook Web Access](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="7e66c-150">Это запускает системное информационное оповещение, которое автоматически запускает исследование стратегия.</span><span class="sxs-lookup"><span data-stu-id="7e66c-150">This triggers a system-based informational alert that automatically launches the investigation playbook.</span></span>

<span data-ttu-id="7e66c-151">Во время корневого этапа исследования различные аспекты электронного исследования оцениваются.</span><span class="sxs-lookup"><span data-stu-id="7e66c-151">During the root investigation phase, various aspects of the email are assessed.</span></span> <span data-ttu-id="7e66c-152">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="7e66c-152">These include:</span></span>
- <span data-ttu-id="7e66c-153">Определение типа угрозы, который может быть таким:</span><span class="sxs-lookup"><span data-stu-id="7e66c-153">A determination about what type of threat it might be;</span></span>
- <span data-ttu-id="7e66c-154">Отправитель;</span><span class="sxs-lookup"><span data-stu-id="7e66c-154">Who sent it;</span></span>
- <span data-ttu-id="7e66c-155">Откуда отправлено сообщение (инфраструктура отправки);</span><span class="sxs-lookup"><span data-stu-id="7e66c-155">Where the email was sent from (sending infrastructure);</span></span>
- <span data-ttu-id="7e66c-156">Указывает, были ли доставляются или заблокированы другие экземпляры электронной почты;</span><span class="sxs-lookup"><span data-stu-id="7e66c-156">Whether other instances of the email were delivered or blocked;</span></span>
- <span data-ttu-id="7e66c-157">Оценка из наших аналитик;</span><span class="sxs-lookup"><span data-stu-id="7e66c-157">An assessment from our analysts;</span></span>
- <span data-ttu-id="7e66c-158">Связан ли электронная почта со всеми известными кампаниями;</span><span class="sxs-lookup"><span data-stu-id="7e66c-158">Whether the email is associated with any known campaigns;</span></span>
- <span data-ttu-id="7e66c-159">и многое другое.</span><span class="sxs-lookup"><span data-stu-id="7e66c-159">and more.</span></span>

<span data-ttu-id="7e66c-160">По завершении корневого исследования стратегия предоставляет список рекомендуемых действий.</span><span class="sxs-lookup"><span data-stu-id="7e66c-160">After the root investigation is complete, the playbook provides a list of recommended actions to take.</span></span>
  
<span data-ttu-id="7e66c-161">После этого выполняются некоторые этапы расследования и исследования угроз:</span><span class="sxs-lookup"><span data-stu-id="7e66c-161">Next, several threat investigation and hunting steps are executed:</span></span>

- <span data-ttu-id="7e66c-162">Поиск похожих сообщений электронной почты в других кластерах электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7e66c-162">Similar email messages in other email clusters are searched.</span></span>
- <span data-ttu-id="7e66c-163">Сигнал предоставляется совместно с другими платформами, например с помощью [пакета ATP для защитника Windows](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="7e66c-163">The signal is shared with other platforms, such as [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span></span>
- <span data-ttu-id="7e66c-164">Определяется, будут ли какие-либо пользователи щелкать по любым ссылкам в подозрительных сообщениях электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7e66c-164">A determination is made on whether any users have clicked through any links in suspicious email messages.</span></span>
- <span data-ttu-id="7e66c-165">Проверка выполняется в Office 365 Exchange Online Protection ([EOP]) (EOP/Exchange-Online-Protection-EOP. md) и Office 365 Advanced Серат Protection ([ATP]) (Office-365-atp.md), чтобы проверить наличие других подобных сообщений, предоставленных пользователями.</span><span class="sxs-lookup"><span data-stu-id="7e66c-165">A check is done across Office 365 Exchange Online Protection ([EOP])(eop/exchange-online-protection-eop.md) and Office 365 Advanced Therat Protection ([ATP])(office-365-atp.md) to see if there are any other similar messages reported by users.</span></span>
- <span data-ttu-id="7e66c-166">Проверка того, был ли пользователь скомпрометирован.</span><span class="sxs-lookup"><span data-stu-id="7e66c-166">A check is done to see if a user has been compromised.</span></span> <span data-ttu-id="7e66c-167">Эта проверка использует сигналы в [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) и [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), соотнесение со всеми связанными аномалиями действий пользователей.</span><span class="sxs-lookup"><span data-stu-id="7e66c-167">This check leverages signals across [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) and [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlating any related user activity anomalies.</span></span> 

<span data-ttu-id="7e66c-168">Во время фазы Поиск риски и угрозы назначаются для различных шагов по поиску.</span><span class="sxs-lookup"><span data-stu-id="7e66c-168">During the hunting phase, risks and threats are assigned to various hunting steps.</span></span>  

<span data-ttu-id="7e66c-169">Исправление является завершающим этапом стратегия.</span><span class="sxs-lookup"><span data-stu-id="7e66c-169">Remediation is the final phase of the playbook.</span></span> <span data-ttu-id="7e66c-170">На этом этапе выполняются действия по исправлению в соответствии с этапами сеинвестигатион и поиске.</span><span class="sxs-lookup"><span data-stu-id="7e66c-170">During this phase, remediation steps are taken, based on theinvestigation and hunting phases.</span></span>  

## <a name="getting-started"></a><span data-ttu-id="7e66c-171">Начало работы</span><span class="sxs-lookup"><span data-stu-id="7e66c-171">Getting started</span></span>

<span data-ttu-id="7e66c-172">Чтобы получить доступ к расследованию, как глобальный администратор Office 365, администратор безопасности или средство чтения безопасности, перейдите в центр безопасности Office 365 _Амп_ соответствие требованиям[https://protection.office.com](https://protection.office.com)() и войдите в систему.</span><span class="sxs-lookup"><span data-stu-id="7e66c-172">To access your investigations, as an Office 365 global administrator, security administrator, or security reader, Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span> <span data-ttu-id="7e66c-173">Затем выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="7e66c-173">Then, do one of the following:</span></span>

- <span data-ttu-id="7e66c-174">В области навигации слева перейдите к разделу **Управление** > \*\*\*\* угрозами.</span><span class="sxs-lookup"><span data-stu-id="7e66c-174">In the left navigation, go to **Threat management** > **Investigations**.</span></span>

    <span data-ttu-id="7e66c-175">или</span><span class="sxs-lookup"><span data-stu-id="7e66c-175">or</span></span>

- <span data-ttu-id="7e66c-176">Посетите панель мониторинга управления угрозами (в центре безопасности _амп_ соответствия требованиям перейдите на**панель мониторинга** **управления** > угрозами).</span><span class="sxs-lookup"><span data-stu-id="7e66c-176">Visit the Threat management dashboard (In the Security & Compliance Center, go to **Threat management** > **Dashboard**).</span></span>

![Мини – элементы AIR](media/air-widgets.png)

<span data-ttu-id="7e66c-178">Мини, которые будут отображаться в верхней части [панели мониторинга безопасности](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="7e66c-178">Your AIR widgets will appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="7e66c-179">Выберите мини-приложение, чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="7e66c-179">Select a widget to get started.</span></span>

<span data-ttu-id="7e66c-180">Вы также можете получить доступ к инвеситгатион непосредственно из связанных оповещений.</span><span class="sxs-lookup"><span data-stu-id="7e66c-180">You may also access an invesitgation directly from the related Alerts.</span></span>

### <a name="automated-investigations"></a><span data-ttu-id="7e66c-181">Автоматическое расследование</span><span class="sxs-lookup"><span data-stu-id="7e66c-181">Automated investigations</span></span>

<span data-ttu-id="7e66c-182">Страница автоматизированного исследования показывает расследования Организации и их текущие состояния.</span><span class="sxs-lookup"><span data-stu-id="7e66c-182">The automated investigations page shows your organization's investigations and their current states.</span></span>

![Страница основного исследования для воздуха](media/air-maininvestigationpage.png) 
  
<span data-ttu-id="7e66c-184">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-184">You can:</span></span>
- <span data-ttu-id="7e66c-185">Перейти непосредственно к расследованию (выберите **идентификатор исследования**).</span><span class="sxs-lookup"><span data-stu-id="7e66c-185">Navigate directly to an investigation (select an **Investigation ID**).</span></span>
- <span data-ttu-id="7e66c-186">Примените фильтры.</span><span class="sxs-lookup"><span data-stu-id="7e66c-186">Apply filters.</span></span> <span data-ttu-id="7e66c-187">Выберите **тип расследования**, **диапазон времени**, **состояние**или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="7e66c-187">Choose from **Investigation Type**, **Time range**, **Status**, or a combination of these.</span></span>
- <span data-ttu-id="7e66c-188">Экспортируйте данные в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="7e66c-188">Export the data to a CSV file.</span></span>

### <a name="investigation-graph"></a><span data-ttu-id="7e66c-189">График расследования</span><span class="sxs-lookup"><span data-stu-id="7e66c-189">Investigation graph</span></span>

<span data-ttu-id="7e66c-190">Когда вы откроете конкретное исследование, отобразится страница "исследование".</span><span class="sxs-lookup"><span data-stu-id="7e66c-190">When you open a specific investigation, you see the investigation graph page.</span></span> <span data-ttu-id="7e66c-191">На этой странице показаны все различные объекты: сообщения электронной почты, пользователи (и их действия), а также устройства, которые были автоматически проверены как часть инициированного оповещения.</span><span class="sxs-lookup"><span data-stu-id="7e66c-191">This page shows all the different entities: email messages, users (and their activities), and devices that were automatically investigated as part of the alert that was triggered.</span></span>

![Страница графа расследования воздуха](media/air-investigationgraphpage.png)

<span data-ttu-id="7e66c-193">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-193">You can:</span></span>
- <span data-ttu-id="7e66c-194">Ознакомьтесь с визуальным обзором текущего исследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-194">Get a visual overview of the current investigation.</span></span>
- <span data-ttu-id="7e66c-195">Просмотр сводки времени расследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-195">View a summary of the investigation timings.</span></span>
- <span data-ttu-id="7e66c-196">Выберите узел в зрительном образе, чтобы просмотреть сведения об этом узле.</span><span class="sxs-lookup"><span data-stu-id="7e66c-196">Select a node in the visualization to view details for that node.</span></span>
- <span data-ttu-id="7e66c-197">Выберите вкладку в верхней части, чтобы просмотреть сведения для этой вкладки.</span><span class="sxs-lookup"><span data-stu-id="7e66c-197">Select a tab across the top to view details for that tab.</span></span>

### <a name="alert-investigation"></a><span data-ttu-id="7e66c-198">Исследование оповещений</span><span class="sxs-lookup"><span data-stu-id="7e66c-198">Alert investigation</span></span>

<span data-ttu-id="7e66c-199">На вкладке **оповещения** вы можете просмотреть оповещения, относящиеся к расследованию.</span><span class="sxs-lookup"><span data-stu-id="7e66c-199">On the **Alerts** tab for an investigation, you can see alerts relevant to the investigation.</span></span> <span data-ttu-id="7e66c-200">Подробные сведения включают оповещение, которое инициировало исследование и другие оповещения, такие как рискованный вход, массовый пакет загрузки и т. д., которые сопоставлены с исследованием.</span><span class="sxs-lookup"><span data-stu-id="7e66c-200">Details include the alert that triggered the investigation and other alerts, such as risky sign-in, mass download, etc., that are correlated to the investigation.</span></span> <span data-ttu-id="7e66c-201">На этой странице Аналитика безопасности также может просматривать дополнительные сведения об индивидуальных оповещениях.</span><span class="sxs-lookup"><span data-stu-id="7e66c-201">From this page, a security analyst can also view additional details on individual alerts.</span></span>

![Страница "оповещения о ВОЗДУШном воздухе"](media/air-investigationalertspage.png)

<span data-ttu-id="7e66c-203">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-203">You can:</span></span>
- <span data-ttu-id="7e66c-204">Ознакомьтесь с визуальным обзором текущего триггерного оповещения и всех связанных оповещений.</span><span class="sxs-lookup"><span data-stu-id="7e66c-204">Get a visual overview of the current triggering alert and any associated alerts.</span></span>
- <span data-ttu-id="7e66c-205">Выберите оповещение в списке, чтобы открыть выпадающую страницу со сведениями об оповещениях.</span><span class="sxs-lookup"><span data-stu-id="7e66c-205">Select an alert in the list to open a fly-out page that shows full alert details.</span></span>

### <a name="email-investigation"></a><span data-ttu-id="7e66c-206">Исследование электронной почты</span><span class="sxs-lookup"><span data-stu-id="7e66c-206">Email investigation</span></span>

<span data-ttu-id="7e66c-207">На вкладке **Электронная почта** вы можете просмотреть все кластеры электронной почты, указанные в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-207">On the **Email** tab for an investigation, you can see all the email clusters identified as part of the investigation.</span></span> 

<span data-ttu-id="7e66c-208">С учетом объема электронной почты, который пользователи в организации отправляют и получают, процесс</span><span class="sxs-lookup"><span data-stu-id="7e66c-208">Given the sheer volume of email that users in an organization send and receive, the process of</span></span> 
- <span data-ttu-id="7e66c-209">Кластеризация сообщений электронной почты на основе аналогичных атрибутов из заголовка, основного текста, URL-адреса и вложения в сообщениях электронной почты;</span><span class="sxs-lookup"><span data-stu-id="7e66c-209">clustering email messages based on similar attributes from a message header, body, URL and attachment;</span></span> 
- <span data-ttu-id="7e66c-210">Отделение вредоносных сообщений электронной почты от хороших сообщений; с</span><span class="sxs-lookup"><span data-stu-id="7e66c-210">separating malicious email from the good email; and</span></span> 
- <span data-ttu-id="7e66c-211">выполнение действий с вредоносными сообщениями электронной почты</span><span class="sxs-lookup"><span data-stu-id="7e66c-211">taking action on malicious email messages</span></span> 

<span data-ttu-id="7e66c-212">может занять несколько часов.</span><span class="sxs-lookup"><span data-stu-id="7e66c-212">can take many hours.</span></span> <span data-ttu-id="7e66c-213">ВОЗДУХ теперь автоматизирует этот процесс, сохраняя время и усилия группы безопасности Организации.</span><span class="sxs-lookup"><span data-stu-id="7e66c-213">AIR now automates this process, saving your organization's security team time and effort.</span></span> 

<span data-ttu-id="7e66c-214">В качестве примера рассмотрим следующий сценарий.</span><span class="sxs-lookup"><span data-stu-id="7e66c-214">As an example, consider the following scenario.</span></span> <span data-ttu-id="7e66c-215">Первый кластер из трех сообщений электронной почты был признан фишингом.</span><span class="sxs-lookup"><span data-stu-id="7e66c-215">The first cluster of three email messages were deemed to be phish.</span></span> <span data-ttu-id="7e66c-216">Существует другой кластер похожих сообщений с тем же IP-АДРЕСом и темой, которые считаются вредоносными, так как некоторые из них были идентифицированы как фишинг во время первоначального обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7e66c-216">Another cluster of similar messages with the same IP and subject was found and considered  malicious, as some of them were identified as phish during initial detection.</span></span> 

![Страница расследования по электронной почте для AIR](media/air-investigationemailpage.png)

<span data-ttu-id="7e66c-218">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-218">You can:</span></span>
- <span data-ttu-id="7e66c-219">Получение визуального обзора текущих результатов кластера и обнаруженных угроз.</span><span class="sxs-lookup"><span data-stu-id="7e66c-219">Get a visual overview of the current clustering results and threats found.</span></span>
- <span data-ttu-id="7e66c-220">Щелкните объект кластера или список угроз, чтобы открыть выпадающую страницу с подробными сведениями об оповещениях.</span><span class="sxs-lookup"><span data-stu-id="7e66c-220">Click a cluster entity or a threat list to open a fly-out page that shows the full alert details.</span></span>

![Сведения об использовании почтовых сообщений при расследовании воздуха](media/air-investigationemailpageflyoutdetails.png)

<span data-ttu-id="7e66c-222">\* Примечание. в контексте электронной почты в ходе расследования вы можете увидеть зону угроз громкости.</span><span class="sxs-lookup"><span data-stu-id="7e66c-222">\*Note: In the context of email, you may see a volume anomaly threat surface as part of the investigation.</span></span> <span data-ttu-id="7e66c-223">Аномалия тома указывает на копилку аналогичных сообщений в сравнении с более ранними периодами события.</span><span class="sxs-lookup"><span data-stu-id="7e66c-223">A volume anomaly indicates a spike in similar emails around the investigation event time compared to earlier timeframes.</span></span> <span data-ttu-id="7e66c-224">Этот пик в почтовых сообщениях с аналогичными характеристиками (например, субъектом и доменом отправителя, подобия основного текста и IP-адреса отправителя) типичен при запуске кампаний по электронной почте или атак.</span><span class="sxs-lookup"><span data-stu-id="7e66c-224">This spike in email traffic with similar characteristics (e.g. subject and sender domain, body similarity and sender IP) is typical of the start of email campaigns or attacks.</span></span> <span data-ttu-id="7e66c-225">Однако массовые и спомные кампании электронной почты также совместно используют эти характеристики.</span><span class="sxs-lookup"><span data-stu-id="7e66c-225">However, bulk and spom email campaigns at times also share these characteristics.</span></span> <span data-ttu-id="7e66c-226">Аномалии тома представляют потенциальную угрозу, и они могут быть менее серьезными по сравнению с вредоносными программами или антифишингом, которые определены с помощью антивирусных ядер, детонации или вредоносной репутации.</span><span class="sxs-lookup"><span data-stu-id="7e66c-226">Volume anomalies represent a potential threat, and accordingly could be less severe compared to malware or phish threats that are identified using anti-virus engines, detonation or malicious reputation.</span></span>

### <a name="user-investigation"></a><span data-ttu-id="7e66c-227">Исследование пользователей</span><span class="sxs-lookup"><span data-stu-id="7e66c-227">User investigation</span></span>

<span data-ttu-id="7e66c-228">На вкладке **Пользователи** отображаются все пользователи, указанные в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-228">On the **Users** tab, you can see all the users identified as part of the investigation.</span></span> 

<span data-ttu-id="7e66c-229">Например, на следующем изображении в ЭФИРе определены индикаторы компромиссов и аномалий на основе созданного правила для папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="7e66c-229">For example, in the following image, AIR has identified indicators of compromise and anomalies based on a new inbox rule that was created.</span></span> <span data-ttu-id="7e66c-230">Дополнительные сведения (свидетельства) об анализе доступны через подробные представления на этой вкладке. Индикаторы компромиссов и аномалий могут также включать обнаружение аномалий в [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security).</span><span class="sxs-lookup"><span data-stu-id="7e66c-230">Additional details (evidence) of the investigation are available through detailed views within this tab. Indicators of compromise and anomalies may also include anomaly detections from [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security).</span></span>

![Страница пользователей расследования воздуха](media/air-investigationuserspage.png)

<span data-ttu-id="7e66c-232">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-232">You can:</span></span>
- <span data-ttu-id="7e66c-233">Получение визуального обзора идентифицированных результатов пользователей и обнаруженных рисков.</span><span class="sxs-lookup"><span data-stu-id="7e66c-233">Get a visual overview of identified user results and risks found.</span></span>
- <span data-ttu-id="7e66c-234">Выберите пользователя, чтобы открыть выпадающую страницу с полными сведениями о предупреждениях.</span><span class="sxs-lookup"><span data-stu-id="7e66c-234">Select a user to open a fly-out page that shows the full alert details.</span></span>

### <a name="machine-investigation"></a><span data-ttu-id="7e66c-235">Машинный расследований</span><span class="sxs-lookup"><span data-stu-id="7e66c-235">Machine investigation</span></span>

<span data-ttu-id="7e66c-236">На вкладке **машины** отображаются все компьютеры, указанные в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-236">On the **Machines** tab, you can see all the machines identified as part of the investigation.</span></span> 

![Страница машины расследования воздуха](media/air-investigationmachinepage.png)

<span data-ttu-id="7e66c-238">В рамках расследования воздух сопоставляет угрозы электронной почты с устройствами.</span><span class="sxs-lookup"><span data-stu-id="7e66c-238">As part of the investigation, AIR correlates email threats to devices.</span></span> <span data-ttu-id="7e66c-239">Например, исследование передает хэш-файл в пакет ATP для [защитника Windows](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) для изучения.</span><span class="sxs-lookup"><span data-stu-id="7e66c-239">For example, an investigation passes a file hash across to [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) to investigate.</span></span> <span data-ttu-id="7e66c-240">Это позволяет автоматически исследовать важные компьютеры для пользователей и помогает гарантировать, что угрозы разрешаются как в облаке, так и на устройствах.</span><span class="sxs-lookup"><span data-stu-id="7e66c-240">This allows for automated investigation of relevant machines for your users and helps to ensure that threats are addressed both in the cloud and across your devices.</span></span> 

<span data-ttu-id="7e66c-241">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-241">You can:</span></span>
- <span data-ttu-id="7e66c-242">Получение визуального обзора текущих компьютеров и обнаруженных угроз.</span><span class="sxs-lookup"><span data-stu-id="7e66c-242">Get a visual overview of the current machines and threats found.</span></span>
- <span data-ttu-id="7e66c-243">Выберите компьютер, чтобы открыть представление, которое будет изменяться в связанном с ним [расследованИи Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection) в центре безопасности ATP защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="7e66c-243">Select a machine to open a view that into the related [Windows Defender ATP investigations](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection) in the Windows Defender ATP Security Center.</span></span>

### <a name="entity-investigation"></a><span data-ttu-id="7e66c-244">Исследование сущностей</span><span class="sxs-lookup"><span data-stu-id="7e66c-244">Entity investigation</span></span>

<span data-ttu-id="7e66c-245">На вкладке **сущности** можно просмотреть все компьютеры, указанные в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-245">On the **Entities** tab, you can see all the machines identified as part of the investigation.</span></span> 

<span data-ttu-id="7e66c-246">Здесь вы можете просмотреть проверенные объекты.</span><span class="sxs-lookup"><span data-stu-id="7e66c-246">Here, you can see the investigated entities.</span></span> <span data-ttu-id="7e66c-247">Вы можете просматривать сведения о типах сущностей, таких как сообщения электронной почты, кластеры, IP-адреса, пользователей и другие.</span><span class="sxs-lookup"><span data-stu-id="7e66c-247">You can see details of the types of entities, such as email messages, clusters, IP addresses, users, and more.</span></span> <span data-ttu-id="7e66c-248">Вы также можете узнать, сколько сущностей было проанализировано, а также о угрозах, которые были связаны с каждым из них.</span><span class="sxs-lookup"><span data-stu-id="7e66c-248">You can also see how many entities were analyzed, and the threats that were associated with each.</span></span> 

![Страница сущностей для исследования воздуха](media/air-investigationentitiespage.png)

<span data-ttu-id="7e66c-250">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-250">You can:</span></span>
- <span data-ttu-id="7e66c-251">Получение визуального обзора обнаруженных сущностей и угроз.</span><span class="sxs-lookup"><span data-stu-id="7e66c-251">Get a visual overview of the investigation entities and threats found.</span></span>
- <span data-ttu-id="7e66c-252">Выберите сущность, чтобы открыть выпадающую страницу со сведениями о связанном объекте.</span><span class="sxs-lookup"><span data-stu-id="7e66c-252">Select an entity to open a fly-out page that shows the related entity detail.</span></span>

![Сведения об объектах для исследования воздуха](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a><span data-ttu-id="7e66c-254">Журнал стратегия</span><span class="sxs-lookup"><span data-stu-id="7e66c-254">Playbook log</span></span>

<span data-ttu-id="7e66c-255">На вкладке **Журнал** можно просмотреть все действия стратегия, произошедшие во время расследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-255">On the **Log** tab, you can see all the playbook steps that have occurred during the investigation.</span></span> <span data-ttu-id="7e66c-256">Журнал записывает полный набор всех действий, выполненных средствами автоматического исследования Office 365, в составе воздуха.</span><span class="sxs-lookup"><span data-stu-id="7e66c-256">The log captures a complete inventory of all actions completed by Office 365 auto-investigation capabilities as part of AIR.</span></span> <span data-ttu-id="7e66c-257">Он предоставляет четкое представление обо всех действиях, выполняемых, включая само действие, описание и продолжительность фактического от начала до конца.</span><span class="sxs-lookup"><span data-stu-id="7e66c-257">It provides a clear view of all the steps taken, including the Action itself, a description and the duration of the actual from start to finish.</span></span> 

![Страница журнала расследования воздуха](media/air-investigationlogpage.png)

<span data-ttu-id="7e66c-259">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-259">You can:</span></span>
- <span data-ttu-id="7e66c-260">Ознакомьтесь с визуальным обзором выполненных действий по стратегия.</span><span class="sxs-lookup"><span data-stu-id="7e66c-260">Get see a visual overview of the playbook steps taken.</span></span>
- <span data-ttu-id="7e66c-261">Экспорт результатов в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="7e66c-261">Export the results to a CSV file.</span></span>
- <span data-ttu-id="7e66c-262">ОтФильтровать представление.</span><span class="sxs-lookup"><span data-stu-id="7e66c-262">Filter the view.</span></span>

### <a name="recommended-actions"></a><span data-ttu-id="7e66c-263">Рекомендуемые действия</span><span class="sxs-lookup"><span data-stu-id="7e66c-263">Recommended actions</span></span>

<span data-ttu-id="7e66c-264">На вкладке **действия** отображаются все действия по стратегия, Рекомендуемые для исправления после завершения расследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-264">On the **Actions** tab, you can see all the playbook actions that are recommended for remediation after the investigation has completed.</span></span> 

<span data-ttu-id="7e66c-265">Действия захватывают действия, которые корпорация Майкрософт рекомендует предпринять в конце расследования.</span><span class="sxs-lookup"><span data-stu-id="7e66c-265">Actions capture the steps Microsoft recommends you take at the end of a investigation.</span></span> <span data-ttu-id="7e66c-266">Действия по исправлению можно выполнить здесь, выбрав одно или несколько действий.</span><span class="sxs-lookup"><span data-stu-id="7e66c-266">You can take remediation actions here by selecting one or more actions.</span></span> <span data-ttu-id="7e66c-267">Чтобы \*\*\*\* начать исправление, нажмите кнопку одобрить.</span><span class="sxs-lookup"><span data-stu-id="7e66c-267">Clicking **Approve** will allow remediation to begin.</span></span> <span data-ttu-id="7e66c-268">(Нужные разрешения будут обязательными.</span><span class="sxs-lookup"><span data-stu-id="7e66c-268">(Appropriate permissions will be required.</span></span> <span data-ttu-id="7e66c-269">Например, средство чтения безопасности может просматривать действия, но не утверждать их.)</span><span class="sxs-lookup"><span data-stu-id="7e66c-269">For example, a Security Reader can view actions but not approve them.)</span></span>  

![Страница "действия по расследованию воздуха"](media/air-investigationactionspage.png)

<span data-ttu-id="7e66c-271">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="7e66c-271">You can:</span></span>
- <span data-ttu-id="7e66c-272">Ознакомьтесь с визуальным обзором действий, рекомендованных для стратегия.</span><span class="sxs-lookup"><span data-stu-id="7e66c-272">Get a visual overview of the playbook-recommended actions.</span></span>
- <span data-ttu-id="7e66c-273">Выберите одно или несколько действий.</span><span class="sxs-lookup"><span data-stu-id="7e66c-273">Select a single action or multiple actions.</span></span>
- <span data-ttu-id="7e66c-274">Утверждение или отклонение рекомендуемых действий с комментариями.</span><span class="sxs-lookup"><span data-stu-id="7e66c-274">Approve or reject recommended actions with comments.</span></span>
- <span data-ttu-id="7e66c-275">Экспорт результатов в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="7e66c-275">Export the results to a CSV file.</span></span>
- <span data-ttu-id="7e66c-276">ОтФильтровать представление.</span><span class="sxs-lookup"><span data-stu-id="7e66c-276">Filter the view.</span></span>

## <a name="how-to-get-air"></a><span data-ttu-id="7e66c-277">Как получить воздух</span><span class="sxs-lookup"><span data-stu-id="7e66c-277">How to get AIR</span></span>

<span data-ttu-id="7e66c-278">В настоящее время Office 365 AIR находится в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="7e66c-278">Currently, Office 365 AIR is in preview.</span></span> <span data-ttu-id="7e66c-279">Office 365 AIR будет включено в следующие подписки:</span><span class="sxs-lookup"><span data-stu-id="7e66c-279">Office 365 AIR will be included in the following subscriptions:</span></span>

- <span data-ttu-id="7e66c-280">Microsoft 365 корпоративный E5</span><span class="sxs-lookup"><span data-stu-id="7e66c-280">Microsoft 365 Enterprise E5</span></span>
- <span data-ttu-id="7e66c-281">Office 365 корпоративный E5</span><span class="sxs-lookup"><span data-stu-id="7e66c-281">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="7e66c-282">Защита от угроз Майкрософт</span><span class="sxs-lookup"><span data-stu-id="7e66c-282">Microsoft Threat Protection</span></span>
- <span data-ttu-id="7e66c-283">Office 365 Advanced Threat protection (план 2)</span><span class="sxs-lookup"><span data-stu-id="7e66c-283">Office 365 Advanced Threat Protection Plan 2</span></span>

<span data-ttu-id="7e66c-284">Для получения дополнительных сведений о доступности функций посетите [план Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="7e66c-284">To learn more about feature availability, visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>
