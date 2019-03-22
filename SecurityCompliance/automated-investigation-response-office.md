---
title: Автоматизированное исследование и реагирование (AIR) с помощью логики операций с угрозами Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Сведения об автоматическом расследовании и возможностях реагирования в Office 365 Advanced Threat protection.
ms.openlocfilehash: c2d5acd0bf26dc28b30f26488adf47de2c834fb6
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/21/2019
ms.locfileid: "30736471"
---
# <a name="automated-investigation-and-response-air-with-office-365-threat-intelligence"></a><span data-ttu-id="b4faf-103">Автоматизированное исследование и реагирование (AIR) с помощью логики операций с угрозами Office 365</span><span class="sxs-lookup"><span data-stu-id="b4faf-103">Automated Investigation and Response (AIR) with Office 365 Threat Intelligence</span></span>

<span data-ttu-id="b4faf-104">Автоматическое исследование и ответ (AIR) (в скором времени в [Office 365 для расследования угроз и возможностей реагирования](office-365-ti.md)) позволяют выполнять автоматическое исследование и устранение известных угроз, существующих сегодня.</span><span class="sxs-lookup"><span data-stu-id="b4faf-104">Automated Investigation and Response (AIR) (coming soon to [Office 365 Threat investigation and response capabilities](office-365-ti.md)) enables you to run automated investigation and remediation to well-known threats that exist today.</span></span> <span data-ttu-id="b4faf-105">В этой статье приводятся общие сведения о AIR и о том, как она позволит повысить эффективность и эффективность снижения угроз в Организации.</span><span class="sxs-lookup"><span data-stu-id="b4faf-105">Read this article to get an overview of AIR and how it can help your organization mitigate threats more effectively and efficiently.</span></span> <span data-ttu-id="b4faf-106">Толеарн дополнительные сведения о том, когда воздух будет доступен, вы найдете в [статье план выпуска Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="b4faf-106">Tolearn more about when AIR will be available, see the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

## <a name="alerts"></a><span data-ttu-id="b4faf-107">Оповещения</span><span class="sxs-lookup"><span data-stu-id="b4faf-107">Alerts</span></span>

<span data-ttu-id="b4faf-108">[Оповещения](alert-policies.md#viewing-alerts) представляют триггеры для рабочих процессов группы операций безопасности для реагирования на инциденты.</span><span class="sxs-lookup"><span data-stu-id="b4faf-108">[Alerts](alert-policies.md#viewing-alerts) represent triggers for Security Operations team workflows for incident response.</span></span> <span data-ttu-id="b4faf-109">Приоритизация правильного набора оповещений для проведения расследования, чтобы убедиться, что угрозы не являются неадресными.</span><span class="sxs-lookup"><span data-stu-id="b4faf-109">Prioritizing the right set of alerts for investigation while making sure no threats are unaddressed is challenging.</span></span> <span data-ttu-id="b4faf-110">При расследовании в оповещениях выполняются вручную, поэтому Teams должны осуществлять слежение за сущностями (например, контент, устройства и пользователей) от угроз.</span><span class="sxs-lookup"><span data-stu-id="b4faf-110">When investigations into alerts are performed manually, Security Operations teams must hunt and correlate entities (e.g. content, devices and users) at risk from threats.</span></span> <span data-ttu-id="b4faf-111">Такие задачи и рабочие процессы занимают много времени и используют несколько средств и систем.</span><span class="sxs-lookup"><span data-stu-id="b4faf-111">Such tasks and workflows are very time consuming and involve multiple tools and systems.</span></span> <span data-ttu-id="b4faf-112">В среде AIR исследование и отклики автоматизированы по ключевым угрозам безопасности и управлению угрозами, которые автоматически инициируют ответ безопасности "Playbooks".</span><span class="sxs-lookup"><span data-stu-id="b4faf-112">With AIR, investigation and response are automated into key security and threat management alerts that trigger your security response playbooks automatically.</span></span> 

<span data-ttu-id="b4faf-113">чтобы просмотреть оповещения, в центре безопасности _амп_ соответствия требованиям Office 365 выберите **alerts** > **view alerts**.</span><span class="sxs-lookup"><span data-stu-id="b4faf-113">To view alerts, in the Office 365 Security & Compliance Center, choose **Alerts** > **View alerts**.</span></span>

![Оповещения, ссылающиеся на расследования](media/air-alerts-page-details.png) 

<span data-ttu-id="b4faf-115">Выберите оповещение, чтобы просмотреть сведения о нем, а затем воспользуйтесь ссылкой **Просмотр расследования** , чтобы перейти к соответствующему [исследованию](#investigation-graph).</span><span class="sxs-lookup"><span data-stu-id="b4faf-115">Select an alert to view its details, and from there, use the **View investigation** link to go to the corresponding [investigation](#investigation-graph).</span></span>

## <a name="security-playbooks"></a><span data-ttu-id="b4faf-116">"Playbooks" безопасности</span><span class="sxs-lookup"><span data-stu-id="b4faf-116">Security playbooks</span></span>

<span data-ttu-id="b4faf-117">"Playbooks" безопасности — это внутренние политики, которые находятся в сердце автоматизации в защите от угроз Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b4faf-117">Security playbooks are back-end policies that are at the heart of automation in Microsoft Threat Protection.</span></span> <span data-ttu-id="b4faf-118">"Playbooks" безопасности, предоставляемые в среде AIR, основаны на распространенных реальных сценариях безопасности.</span><span class="sxs-lookup"><span data-stu-id="b4faf-118">The security playbooks provided in AIR are based on common real-world security scenarios.</span></span> <span data-ttu-id="b4faf-119">Стратегия безопасности запускается автоматически при активации оповещения в Организации.</span><span class="sxs-lookup"><span data-stu-id="b4faf-119">A security playbook is launched automatically when an alert is triggered within your organization.</span></span> <span data-ttu-id="b4faf-120">После срабатывания триггера оповещения связанный стратегия запускается автоматически.</span><span class="sxs-lookup"><span data-stu-id="b4faf-120">Once the alert triggers, the associated playbook is run automatically.</span></span> <span data-ttu-id="b4faf-121">В стратегия выполняется исследование со всеми связанными метаданными (в том числе сообщениями электронной почты, пользователями, субъектами, отправителями и т. д.) и, в зависимости от полученных результатов, рекомендуется набор действий, которые Группа безопасности Организации может использовать для управления и устранения проблем. угроза.</span><span class="sxs-lookup"><span data-stu-id="b4faf-121">The playbook runs an investigation, looking at all the associated metadata (including email messages, users, subjects, senders, etc.) and, based on its findings, recommends a set of actions that your organization's security team can take to control and mitigate the threat.</span></span> 

<span data-ttu-id="b4faf-122">"Playbooks" по обеспечению безопасности, которые вы будете получать с помощью воздуха, предназначены для самых распространенных угроз, которые в настоящее время сталкиваются с организациями.</span><span class="sxs-lookup"><span data-stu-id="b4faf-122">The security playbooks you'll get with AIR are designed to tackle the most frequent threats that organizations face today.</span></span> <span data-ttu-id="b4faf-123">Они основываются на входных данных из операций безопасности и команд реагирования на инциденты, в том числе пользователей, помогающих защищать ресурсы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b4faf-123">They're based on input from Security Operations and Incident Response teams, including those who help defend Microsoft assets.</span></span>

### <a name="security-playbooks-are-rolling-out-in-phases"></a><span data-ttu-id="b4faf-124">Этапы безопасности "Playbooks"</span><span class="sxs-lookup"><span data-stu-id="b4faf-124">Security playbooks are rolling out in phases</span></span>

<span data-ttu-id="b4faf-125">Как часть воздуха, "Playbooks" безопасности — это этапы развертывания.</span><span class="sxs-lookup"><span data-stu-id="b4faf-125">As part of AIR, security playbooks are rolling out in phases</span></span>

- <span data-ttu-id="b4faf-126">**Этап 1 (апрель 2019)**: "Playbooks" включает рекомендации, которые администраторы безопасности просматривают и утверждают.</span><span class="sxs-lookup"><span data-stu-id="b4faf-126">**Phase 1 (April 2019)**: Playbooks include recommendations that security administrators review and approve.</span></span> 

- <span data-ttu-id="b4faf-127">**Этап 2 (июнь 2019)**: Администраторы безопасности будут иметь возможность разрешить "Playbooks" действия автоматически, не обращаясь к административному взаимодействию.</span><span class="sxs-lookup"><span data-stu-id="b4faf-127">**Phase 2 (June 2019)**: Security administrators will have the option to allow security playbooks to take action automatically, without administrative interaction.</span></span>

<span data-ttu-id="b4faf-128">Этап 1 будет включать следующие "Playbooks":</span><span class="sxs-lookup"><span data-stu-id="b4faf-128">Phase 1 will include the following playbooks:</span></span>
- <span data-ttu-id="b4faf-129">Сообщение о phishing-атаке, сообщенное пользователем</span><span class="sxs-lookup"><span data-stu-id="b4faf-129">User-reported phish message</span></span>
- <span data-ttu-id="b4faf-130">URL-адрес щелкните вредоносности изменения и переопределение блоков безОпасных ссылок ATP</span><span class="sxs-lookup"><span data-stu-id="b4faf-130">URL click verdict change and ATP Safe Links block override</span></span>
- <span data-ttu-id="b4faf-131">Вредоносная программа ZAP</span><span class="sxs-lookup"><span data-stu-id="b4faf-131">Malware ZAP</span></span>
- <span data-ttu-id="b4faf-132">Фишинг ZAP</span><span class="sxs-lookup"><span data-stu-id="b4faf-132">Phish ZAP</span></span>
- <span data-ttu-id="b4faf-133">Ручное расследование (с помощью проводника)</span><span class="sxs-lookup"><span data-stu-id="b4faf-133">Manual investigations (using Explorer)</span></span>

<span data-ttu-id="b4faf-134">Несколько дополнительных "Playbooks" запланированы на этапе 2.</span><span class="sxs-lookup"><span data-stu-id="b4faf-134">Several more playbooks are planned for Phase 2.</span></span>

### <a name="playbooks-include-investigation-and-recommendations"></a><span data-ttu-id="b4faf-135">"Playbooks": исследование и рекомендации</span><span class="sxs-lookup"><span data-stu-id="b4faf-135">Playbooks include investigation and recommendations</span></span>

<span data-ttu-id="b4faf-136">Каждый стратегия включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="b4faf-136">Each playbook includes:</span></span> 
- <span data-ttu-id="b4faf-137">корневое исследование,</span><span class="sxs-lookup"><span data-stu-id="b4faf-137">a root investigation,</span></span> 
- <span data-ttu-id="b4faf-138">действия по обнаружению других потенциальных угроз и</span><span class="sxs-lookup"><span data-stu-id="b4faf-138">steps to hunt down other potential threats, and</span></span> 
- <span data-ttu-id="b4faf-139">рекомендуемое исправление угроз.</span><span class="sxs-lookup"><span data-stu-id="b4faf-139">recommended threat remediation.</span></span>

<span data-ttu-id="b4faf-140">Каждый этап высокого уровня включает множество подшагов, которые выполняются для предоставления детальных, подробных и исчерпывающих ответов на угрозы.</span><span class="sxs-lookup"><span data-stu-id="b4faf-140">Each high-level step includes many sub-steps that are executed to provide a deep, detailed, and exhaustive response to threats.</span></span>

## <a name="example-user-reported-phish-message"></a><span data-ttu-id="b4faf-141">Пример: сообщение фишинга, зарегистрированное пользователем</span><span class="sxs-lookup"><span data-stu-id="b4faf-141">Example: User-reported phish message</span></span>

<span data-ttu-id="b4faf-142">Когда пользователь в Организации отправляет сообщение электронной почты и отправляет его в корпорацию Майкрософт с помощью надстройки [Report Message для Outlook или Outlook Web Access](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="b4faf-142">When a user in your organization submits an email message and reports it to Microsoft by using the [Report Message add-in for Outlook or Outlook Web Access](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="b4faf-143">Это запускает системное информационное оповещение, которое автоматически запускает исследование стратегия.</span><span class="sxs-lookup"><span data-stu-id="b4faf-143">This triggers a system-based informational alert that automatically launches the investigation playbook.</span></span>

<span data-ttu-id="b4faf-144">Во время корневого этапа исследования различные аспекты электронного исследования оцениваются.</span><span class="sxs-lookup"><span data-stu-id="b4faf-144">During the root investigation phase, various aspects of the email are assessed.</span></span> <span data-ttu-id="b4faf-145">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="b4faf-145">These include:</span></span>
- <span data-ttu-id="b4faf-146">Определение типа угрозы, который может быть таким:</span><span class="sxs-lookup"><span data-stu-id="b4faf-146">A determination about what type of threat it might be;</span></span>
- <span data-ttu-id="b4faf-147">Отправитель;</span><span class="sxs-lookup"><span data-stu-id="b4faf-147">Who sent it;</span></span>
- <span data-ttu-id="b4faf-148">Откуда отправлено сообщение (инфраструктура отправки);</span><span class="sxs-lookup"><span data-stu-id="b4faf-148">Where the email was sent from (sending infrastructure);</span></span>
- <span data-ttu-id="b4faf-149">Указывает, были ли доставляются или заблокированы другие экземпляры электронной почты;</span><span class="sxs-lookup"><span data-stu-id="b4faf-149">Whether other instances of the email were delivered or blocked;</span></span>
- <span data-ttu-id="b4faf-150">Оценка из наших аналитик;</span><span class="sxs-lookup"><span data-stu-id="b4faf-150">An assessment from our analysts;</span></span>
- <span data-ttu-id="b4faf-151">Связан ли электронная почта со всеми известными кампаниями;</span><span class="sxs-lookup"><span data-stu-id="b4faf-151">Whether the email is associated with any known campaigns;</span></span>
- <span data-ttu-id="b4faf-152">и многое другое.</span><span class="sxs-lookup"><span data-stu-id="b4faf-152">and more.</span></span>

<span data-ttu-id="b4faf-153">По завершении корневого исследования стратегия предоставляет список рекомендуемых действий.</span><span class="sxs-lookup"><span data-stu-id="b4faf-153">After the root investigation is complete, the playbook provides a list of recommended actions to take.</span></span>
  
<span data-ttu-id="b4faf-154">Затем выполняются некоторые шаги по поиску:</span><span class="sxs-lookup"><span data-stu-id="b4faf-154">Next, several hunting steps are executed:</span></span>

- <span data-ttu-id="b4faf-155">Поиск похожих сообщений электронной почты в других кластерах электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b4faf-155">Similar email messages in other email clusters are searched.</span></span>
- <span data-ttu-id="b4faf-156">Сигнал предоставляется совместно с другими платформами, например с помощью [пакета ATP для защитника Windows](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="b4faf-156">The signal is shared with other platforms, such as [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span></span>
- <span data-ttu-id="b4faf-157">Определение, когда какие пользователи прощелкают подозрительные сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="b4faf-157">A determination is made on whether any users have clicked through on the suspicious email message.</span></span>
- <span data-ttu-id="b4faf-158">Проверка выполняется в Office 365 [EOP](eop/exchange-online-protection-eop.md) и [ATP](office-365-atp.md) , чтобы проверить наличие других подобных сообщений, о которых сообщили пользователи.</span><span class="sxs-lookup"><span data-stu-id="b4faf-158">A check is done across Office 365 [EOP](eop/exchange-online-protection-eop.md) and [ATP](office-365-atp.md) to see if there are any other similar messages reported by users.</span></span>
- <span data-ttu-id="b4faf-159">Проверка того, был ли пользователь скомпрометирован.</span><span class="sxs-lookup"><span data-stu-id="b4faf-159">A check is done to see if a user has been compromised.</span></span> <span data-ttu-id="b4faf-160">Эта проверка использует сигналы в [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) и [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), соотнесение с любыми связанными событиями или оповещениями.</span><span class="sxs-lookup"><span data-stu-id="b4faf-160">This check leverages signals across [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) and [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlating any related events or alerts.</span></span> 

<span data-ttu-id="b4faf-161">Во время фазы Поиск риски и угрозы назначаются для различных шагов по поиску.</span><span class="sxs-lookup"><span data-stu-id="b4faf-161">During the hunting phase, risks and threats are assigned to various hunting steps.</span></span>  

<span data-ttu-id="b4faf-162">Исправление является завершающим этапом стратегия.</span><span class="sxs-lookup"><span data-stu-id="b4faf-162">Remediation is the final phase of the playbook.</span></span> <span data-ttu-id="b4faf-163">На этом этапе выполняются действия по исправлению в соответствии с этапами сеинвестигатион и поиске.</span><span class="sxs-lookup"><span data-stu-id="b4faf-163">During this phase, remediation steps are taken, based on theinvestigation and hunting phases.</span></span>  

## <a name="getting-started"></a><span data-ttu-id="b4faf-164">Начало работы</span><span class="sxs-lookup"><span data-stu-id="b4faf-164">Getting started</span></span>

<span data-ttu-id="b4faf-165">Чтобы получить доступ к расследованию, как глобальный администратор Office 365 или администратор безопасности, перейдите в центр безопасности Office 365 _Амп_ соответствие требованиям[https://protection.office.com](https://protection.office.com)() и войдите в систему.</span><span class="sxs-lookup"><span data-stu-id="b4faf-165">To access your investigations, as an Office 365 global administrator or security administrator, Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span> <span data-ttu-id="b4faf-166">Затем выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="b4faf-166">Then, do one of the following:</span></span>

- <span data-ttu-id="b4faf-167">В области навигации слева перейдите к разделу **Управление** > \*\*\*\* угрозами.</span><span class="sxs-lookup"><span data-stu-id="b4faf-167">In the left navigation, go to **Threat management** > **Investigations**.</span></span>

    <span data-ttu-id="b4faf-168">или</span><span class="sxs-lookup"><span data-stu-id="b4faf-168">or</span></span>

- <span data-ttu-id="b4faf-169">Посетите панель мониторинга управления угрозами (в центре безопасности _амп_ соответствия требованиям перейдите на**панель мониторинга** **управления** > угрозами).</span><span class="sxs-lookup"><span data-stu-id="b4faf-169">Visit the Threat management dashboard (In the Security & Compliance Center, go to **Threat management** > **Dashboard**).</span></span>

![Мини – элементы AIR](media/air-widgets.png)

<span data-ttu-id="b4faf-171">Мини, которые будут отображаться в верхней части [панели мониторинга безопасности](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="b4faf-171">Your AIR widgets will appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="b4faf-172">Выберите мини-приложение, чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="b4faf-172">Select a widget to get started.</span></span>

### <a name="automated-investigations"></a><span data-ttu-id="b4faf-173">Автоматическое расследование</span><span class="sxs-lookup"><span data-stu-id="b4faf-173">Automated investigations</span></span>

<span data-ttu-id="b4faf-174">Страница автоматизированного исследования показывает расследования Организации и их текущие состояния.</span><span class="sxs-lookup"><span data-stu-id="b4faf-174">The automated investigations page shows your organization's investigations and their current states.</span></span>

![Страница основного исследования для воздуха](media/air-maininvestigationpage.png) 
  
<span data-ttu-id="b4faf-176">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-176">You can:</span></span>
- <span data-ttu-id="b4faf-177">Перейти непосредственно к расследованию (выберите **идентификатор исследования**).</span><span class="sxs-lookup"><span data-stu-id="b4faf-177">Navigate directly to an investigation (select an **Investigation ID**).</span></span>
- <span data-ttu-id="b4faf-178">Примените фильтры.</span><span class="sxs-lookup"><span data-stu-id="b4faf-178">Apply filters.</span></span> <span data-ttu-id="b4faf-179">Выберите **тип расследования**, **диапазон времени**, **состояние**или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="b4faf-179">Choose from **Investigation Type**, **Time range**, **Status**, or a combination of these.</span></span>
- <span data-ttu-id="b4faf-180">Экспортируйте данные в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="b4faf-180">Export the data to a CSV file.</span></span>

### <a name="investigation-graph"></a><span data-ttu-id="b4faf-181">График расследования</span><span class="sxs-lookup"><span data-stu-id="b4faf-181">Investigation graph</span></span>

<span data-ttu-id="b4faf-182">Когда вы откроете конкретное исследование, отобразится страница "исследование".</span><span class="sxs-lookup"><span data-stu-id="b4faf-182">When you open a specific investigation, you see the investigation graph page.</span></span> <span data-ttu-id="b4faf-183">На этой странице показаны все различные объекты: сообщения электронной почты, пользователи (и их действия), а также устройства, которые были автоматически проверены как часть инициированного оповещения.</span><span class="sxs-lookup"><span data-stu-id="b4faf-183">This page shows all the different entities: email messages, users (and their activities), and devices that were automatically investigated as part of the alert that was triggered.</span></span>

![Страница графа расследования воздуха](media/air-investigationgraphpage.png)

<span data-ttu-id="b4faf-185">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-185">You can:</span></span>
- <span data-ttu-id="b4faf-186">Ознакомьтесь с визуальным обзором текущего исследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-186">Get a visual overview of the current investigation.</span></span>
- <span data-ttu-id="b4faf-187">Просмотр сводки времени расследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-187">View a summary of the investigation timings.</span></span>
- <span data-ttu-id="b4faf-188">Выберите узел в зрительном образе, чтобы просмотреть сведения об этом узле.</span><span class="sxs-lookup"><span data-stu-id="b4faf-188">Select a node in the visualization to view details for that node.</span></span>
- <span data-ttu-id="b4faf-189">Выберите вкладку в верхней части, чтобы просмотреть сведения для этой вкладки.</span><span class="sxs-lookup"><span data-stu-id="b4faf-189">Select a tab across the top to view details for that tab.</span></span>

### <a name="alert-investigation"></a><span data-ttu-id="b4faf-190">Исследование оповещений</span><span class="sxs-lookup"><span data-stu-id="b4faf-190">Alert investigation</span></span>

<span data-ttu-id="b4faf-191">На вкладке **оповещения** вы можете просмотреть все оповещения, относящиеся к расследованию.</span><span class="sxs-lookup"><span data-stu-id="b4faf-191">On the **Alerts** tab for an investigation, you can see all of the alerts relevant to the investigation.</span></span> <span data-ttu-id="b4faf-192">Подробные сведения включают оповещение, которое инициировало исследование и другие оповещения, такие как рискованный вход, массовый пакет загрузки и т. д., которые сопоставлены с исследованием.</span><span class="sxs-lookup"><span data-stu-id="b4faf-192">Details include the alert that triggered the investigation and other alerts, such as risky sign-in, mass download, etc., that are correlated to the investigation.</span></span> <span data-ttu-id="b4faf-193">На этой странице Аналитика безопасности также может просматривать дополнительные сведения об индивидуальных оповещениях.</span><span class="sxs-lookup"><span data-stu-id="b4faf-193">From this page, a security analyst can also view additional details on individual alerts.</span></span>

![Страница "оповещения о ВОЗДУШном воздухе"](media/air-investigationalertspage.png)

<span data-ttu-id="b4faf-195">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-195">You can:</span></span>
- <span data-ttu-id="b4faf-196">Ознакомьтесь с визуальным обзором текущего триггерного оповещения и всех связанных оповещений.</span><span class="sxs-lookup"><span data-stu-id="b4faf-196">Get a visual overview of the current triggering alert and any associated alerts.</span></span>
- <span data-ttu-id="b4faf-197">Выберите оповещение в списке, чтобы открыть выпадающую страницу со сведениями об оповещениях.</span><span class="sxs-lookup"><span data-stu-id="b4faf-197">Select an alert in the list to open a fly-out page that shows full alert details.</span></span>

### <a name="email-investigation"></a><span data-ttu-id="b4faf-198">Исследование электронной почты</span><span class="sxs-lookup"><span data-stu-id="b4faf-198">Email investigation</span></span>

<span data-ttu-id="b4faf-199">На вкладке **Электронная почта** вы можете просмотреть все кластеры электронной почты, указанные в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-199">On the **Email** tab for an investigation, you can see all the email clusters identified as part of the investigation.</span></span> 

<span data-ttu-id="b4faf-200">С учетом объема электронной почты, который пользователи в организации отправляют и получают, процесс</span><span class="sxs-lookup"><span data-stu-id="b4faf-200">Given the sheer volume of email that users in an organization send and receive, the process of</span></span> 
- <span data-ttu-id="b4faf-201">Кластеризация сообщений электронной почты на основе аналогичных атрибутов из заголовка, основного текста, URL-адреса и вложения в сообщениях электронной почты;</span><span class="sxs-lookup"><span data-stu-id="b4faf-201">clustering email messages based on similar attributes from a message header, body, URL and attachment;</span></span> 
- <span data-ttu-id="b4faf-202">Отделение вредоносных сообщений электронной почты от хороших сообщений; с</span><span class="sxs-lookup"><span data-stu-id="b4faf-202">separating malicious email from the good email; and</span></span> 
- <span data-ttu-id="b4faf-203">выполнение действий с вредоносными сообщениями электронной почты</span><span class="sxs-lookup"><span data-stu-id="b4faf-203">taking action on malicious email messages</span></span> 

<span data-ttu-id="b4faf-204">может занять несколько часов.</span><span class="sxs-lookup"><span data-stu-id="b4faf-204">can take many hours.</span></span> <span data-ttu-id="b4faf-205">ВОЗДУХ теперь автоматизирует этот процесс, сохраняя время и усилия группы безопасности Организации.</span><span class="sxs-lookup"><span data-stu-id="b4faf-205">AIR now automates this process, saving your organization's security team time and effort.</span></span> 

<span data-ttu-id="b4faf-206">В качестве примера рассмотрим следующее изображение.</span><span class="sxs-lookup"><span data-stu-id="b4faf-206">As an example, consider the following image.</span></span> <span data-ttu-id="b4faf-207">Первый кластер из трех сообщений электронной почты был признан фишингом.</span><span class="sxs-lookup"><span data-stu-id="b4faf-207">The first cluster of three email messages were deemed to be phish.</span></span> <span data-ttu-id="b4faf-208">Обнаружен другой кластер аналогичных сообщений с тем же IP-АДРЕСом и темой и который считается вредоносным, так как некоторые из них были идентифицированы как фишинг во время первоначального обнаружения.</span><span class="sxs-lookup"><span data-stu-id="b4faf-208">Another cluster of similar messages with the same IP and subject was found and is considered to be malicious, as some of them were identified as phish during initial detection.</span></span> 

![Страница расследования по электронной почте для AIR](media/air-investigationemailpage.png)

<span data-ttu-id="b4faf-210">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-210">You can:</span></span>
- <span data-ttu-id="b4faf-211">Получение визуального обзора текущих результатов кластера и обнаруженных угроз.</span><span class="sxs-lookup"><span data-stu-id="b4faf-211">Get a visual overview of the current clustering results and threats found.</span></span>
- <span data-ttu-id="b4faf-212">Щелкните объект кластера или список угроз, чтобы открыть выпадающую страницу с подробными сведениями об оповещениях.</span><span class="sxs-lookup"><span data-stu-id="b4faf-212">Click a cluster entity or a threat list to open a fly-out page that shows the full alert details.</span></span>

![Сведения об использовании почтовых сообщений при расследовании воздуха](media/air-investigationemailpageflyoutdetails.png)

### <a name="user-investigation"></a><span data-ttu-id="b4faf-214">Исследование пользователей</span><span class="sxs-lookup"><span data-stu-id="b4faf-214">User investigation</span></span>

<span data-ttu-id="b4faf-215">На вкладке **Пользователи** отображаются все пользователи, указанные в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-215">On the **Users** tab, you can see all the users identified as part of the investigation.</span></span> 

<span data-ttu-id="b4faf-216">Например, на следующем изображении в ЭФИРе определены индикаторы компромиссов и аномалий на основе созданного правила для папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="b4faf-216">For example, in the following image, AIR has identified indicators of compromise and anomalies based on a new inbox rule that was created.</span></span> <span data-ttu-id="b4faf-217">Дополнительные сведения (свидетельства) об анализе доступны через подробные представления на этой вкладке.</span><span class="sxs-lookup"><span data-stu-id="b4faf-217">Additional details (evidence) of the investigation are available through detailed views within this tab.</span></span>

![Страница пользователей расследования воздуха](media/air-investigationuserspage.png)

<span data-ttu-id="b4faf-219">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-219">You can:</span></span>
- <span data-ttu-id="b4faf-220">Получение визуального обзора идентифицированных результатов пользователей и обнаруженных рисков.</span><span class="sxs-lookup"><span data-stu-id="b4faf-220">Get a visual overview of identified user results and risks found.</span></span>
- <span data-ttu-id="b4faf-221">Выберите пользователя, чтобы открыть выпадающую страницу с полными сведениями о предупреждениях.</span><span class="sxs-lookup"><span data-stu-id="b4faf-221">Select a user to open a fly-out page that shows the full alert details.</span></span>

### <a name="machine-investigation"></a><span data-ttu-id="b4faf-222">Машинный расследований</span><span class="sxs-lookup"><span data-stu-id="b4faf-222">Machine investigation</span></span>

<span data-ttu-id="b4faf-223">На вкладке **машины** отображаются все компьютеры, указанные в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-223">On the **Machines** tab, you can see all the machines identified as part of the investigation.</span></span> 

![Страница машины расследования воздуха](media/air-investigationmachinepage.png)

<span data-ttu-id="b4faf-225">В рамках расследования воздух сопоставляет угрозы электронной почты с устройствами.</span><span class="sxs-lookup"><span data-stu-id="b4faf-225">As part of the investigation, AIR correlates email threats to devices.</span></span> <span data-ttu-id="b4faf-226">Например, исследование передает хэш-файл в пакет ATP для [защитника Windows](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) для изучения.</span><span class="sxs-lookup"><span data-stu-id="b4faf-226">For example, an investigation passes a file hash across to [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) to investigate.</span></span> <span data-ttu-id="b4faf-227">Это позволяет автоматически исследовать важные компьютеры для пользователей и помогает гарантировать, что угрозы разрешаются как в облаке, так и на устройствах.</span><span class="sxs-lookup"><span data-stu-id="b4faf-227">This allows for automated investigation of relevant machines for your users and helps to ensure that threats are addressed both in the cloud and across your devices.</span></span> 

<span data-ttu-id="b4faf-228">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-228">You can:</span></span>
- <span data-ttu-id="b4faf-229">Получение визуального обзора текущих компьютеров и обнаруженных угроз.</span><span class="sxs-lookup"><span data-stu-id="b4faf-229">Get a visual overview of the current machines and threats found.</span></span>
- <span data-ttu-id="b4faf-230">Выберите компьютер, чтобы открыть представление, которое относится к связанному [расследованИю защитника Windows ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="b4faf-230">Select a machine to open a view that into the related [Windows Defender ATP investigations](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection).</span></span>

### <a name="entity-investigation"></a><span data-ttu-id="b4faf-231">Исследование сущностей</span><span class="sxs-lookup"><span data-stu-id="b4faf-231">Entity investigation</span></span>

<span data-ttu-id="b4faf-232">На вкладке **сущности** можно просмотреть все компьютеры, указанные в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-232">On the **Entities** tab, you can see all the machines identified as part of the investigation.</span></span> 

<span data-ttu-id="b4faf-233">Здесь вы можете просмотреть проверенные объекты.</span><span class="sxs-lookup"><span data-stu-id="b4faf-233">Here, you can see the investigated entities.</span></span> <span data-ttu-id="b4faf-234">Вы можете просматривать сведения о типах сущностей, таких как сообщения электронной почты, кластеры, IP-адреса, пользователей и другие.</span><span class="sxs-lookup"><span data-stu-id="b4faf-234">You can see details of the types of entities, such as email messages, clusters, IP addresses, users, and more.</span></span> <span data-ttu-id="b4faf-235">Вы также можете узнать, сколько сущностей было проанализировано, а также о угрозах, которые были связаны с каждым из них.</span><span class="sxs-lookup"><span data-stu-id="b4faf-235">You can also see how many entities were analyzed, and the threats that were associated with each.</span></span> 

![Страница сущностей для исследования воздуха](media/air-investigationentitiespage.png)

<span data-ttu-id="b4faf-237">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-237">You can:</span></span>
- <span data-ttu-id="b4faf-238">Получение визуального обзора обнаруженных сущностей и угроз.</span><span class="sxs-lookup"><span data-stu-id="b4faf-238">Get a visual overview of the investigation entities and threats found.</span></span>
- <span data-ttu-id="b4faf-239">Выберите сущность, чтобы открыть выпадающую страницу со сведениями о связанном объекте.</span><span class="sxs-lookup"><span data-stu-id="b4faf-239">Select an entity to open a fly-out page that shows the related entity detail.</span></span>

![Сведения об объектах для исследования воздуха](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a><span data-ttu-id="b4faf-241">Журнал стратегия</span><span class="sxs-lookup"><span data-stu-id="b4faf-241">Playbook log</span></span>

<span data-ttu-id="b4faf-242">На вкладке **Журнал** можно просмотреть все действия стратегия, произошедшие во время расследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-242">On the **Log** tab, you can see all the playbook steps that have occurred during the investigation.</span></span> <span data-ttu-id="b4faf-243">Журнал записывает полный набор всех действий, завершенных возможностями системы Microsoft Office 365 Threat Intelligence в составе воздуха.</span><span class="sxs-lookup"><span data-stu-id="b4faf-243">The log captures a complete inventory of all actions completed by Office 365 Threat Intelligence capabilities as part of AIR.</span></span> <span data-ttu-id="b4faf-244">Он предоставляет четкое представление обо всех действиях, выполняемых, включая само действие, описание и продолжительность фактического от начала до конца.</span><span class="sxs-lookup"><span data-stu-id="b4faf-244">It provides a clear view of all the steps taken, including the Action itself, a description and the duration of the actual from start to finish.</span></span> 

![Страница журнала расследования воздуха](media/air-investigationlogpage.png)

<span data-ttu-id="b4faf-246">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-246">You can:</span></span>
- <span data-ttu-id="b4faf-247">Ознакомьтесь с визуальным обзором выполненных действий по стратегия.</span><span class="sxs-lookup"><span data-stu-id="b4faf-247">Get see a visual overview of the playbook steps taken.</span></span>
- <span data-ttu-id="b4faf-248">Экспорт результатов в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="b4faf-248">Export the results to a CSV file.</span></span>
- <span data-ttu-id="b4faf-249">ОтФильтровать представление.</span><span class="sxs-lookup"><span data-stu-id="b4faf-249">Filter the view.</span></span>

### <a name="recommended-actions"></a><span data-ttu-id="b4faf-250">Рекомендуемые действия</span><span class="sxs-lookup"><span data-stu-id="b4faf-250">Recommended actions</span></span>

<span data-ttu-id="b4faf-251">На вкладке **действия** отображаются все действия по стратегия, Рекомендуемые для исправления после завершения расследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-251">On the **Actions** tab, you can see all the playbook actions that are recommended for remediation after the investigation has completed.</span></span> 

<span data-ttu-id="b4faf-252">Действия запишите полный список всех действий, которые корпорация Майкрософт рекомендует выполнить в конце расследования.</span><span class="sxs-lookup"><span data-stu-id="b4faf-252">Actions capture a complete list of all the steps Microsoft recommends you take at the end of a investigation.</span></span> <span data-ttu-id="b4faf-253">Действия по исправлению можно выполнить здесь, выбрав одно или несколько действий.</span><span class="sxs-lookup"><span data-stu-id="b4faf-253">You can take remediation actions here by selecting one or more actions.</span></span> <span data-ttu-id="b4faf-254">Чтобы \*\*\*\* начать исправление, нажмите кнопку одобрить.</span><span class="sxs-lookup"><span data-stu-id="b4faf-254">Clicking **Approve** will allow remediation to begin.</span></span> <span data-ttu-id="b4faf-255">(Могут потребоваться соответствующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="b4faf-255">(Appropriate permissions might be required.</span></span> <span data-ttu-id="b4faf-256">Например, средство чтения безопасности может просматривать действия, но не утверждать их.)</span><span class="sxs-lookup"><span data-stu-id="b4faf-256">For example, a Security Reader can view actions but not approve them.)</span></span>  

![Страница "действия по расследованию воздуха"](media/air-investigationactionspage.png)

<span data-ttu-id="b4faf-258">Варианты действий:</span><span class="sxs-lookup"><span data-stu-id="b4faf-258">You can:</span></span>
- <span data-ttu-id="b4faf-259">Ознакомьтесь с визуальным обзором действий, рекомендованных для стратегия.</span><span class="sxs-lookup"><span data-stu-id="b4faf-259">Get a visual overview of the playbook-recommended actions.</span></span>
- <span data-ttu-id="b4faf-260">Выберите одно или несколько действий.</span><span class="sxs-lookup"><span data-stu-id="b4faf-260">Select a single action or multiple actions.</span></span>
- <span data-ttu-id="b4faf-261">Утверждение рекомендуемых действий.</span><span class="sxs-lookup"><span data-stu-id="b4faf-261">Approve recommended actions.</span></span> <span data-ttu-id="b4faf-262">(Они сразу же записываются вместе с комментариями.)</span><span class="sxs-lookup"><span data-stu-id="b4faf-262">(These are started immediately with comments.)</span></span>
- <span data-ttu-id="b4faf-263">Экспорт результатов в CSV-файл.</span><span class="sxs-lookup"><span data-stu-id="b4faf-263">Export the results to a CSV file.</span></span>
- <span data-ttu-id="b4faf-264">ОтФильтровать представление.</span><span class="sxs-lookup"><span data-stu-id="b4faf-264">Filter the view.</span></span>

## <a name="how-to-get-air"></a><span data-ttu-id="b4faf-265">Как получить воздух</span><span class="sxs-lookup"><span data-stu-id="b4faf-265">How to get AIR</span></span>

<span data-ttu-id="b4faf-266">В настоящее время воздух находится в режиме предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="b4faf-266">Currently, AIR is in preview.</span></span> <span data-ttu-id="b4faf-267">После выпуска воздух будет включен в следующие подписки:</span><span class="sxs-lookup"><span data-stu-id="b4faf-267">When released, AIR will be included in the following subscriptions:</span></span>

- <span data-ttu-id="b4faf-268">Microsoft 365 корпоративный E5</span><span class="sxs-lookup"><span data-stu-id="b4faf-268">Microsoft 365 Enterprise E5</span></span>
- <span data-ttu-id="b4faf-269">Office 365 корпоративный E5</span><span class="sxs-lookup"><span data-stu-id="b4faf-269">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="b4faf-270">Защита от угроз Майкрософт</span><span class="sxs-lookup"><span data-stu-id="b4faf-270">Microsoft Threat Protection</span></span>
- <span data-ttu-id="b4faf-271">Office 365 Advanced Threat protection (план 2)</span><span class="sxs-lookup"><span data-stu-id="b4faf-271">Office 365 Advanced Threat Protection Plan 2</span></span>

<span data-ttu-id="b4faf-272">Для получения дополнительных сведений о доступности функций посетите [план Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="b4faf-272">To learn more about feature availability, visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>
