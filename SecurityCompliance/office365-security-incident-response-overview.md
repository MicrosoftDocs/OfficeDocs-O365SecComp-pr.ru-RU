---
title: Реагирование на инциденты, связанные с безопасностью, в Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 04/27/2018
ms.audience: ITPro
ms.topic: overview
ms.collection:
- o365_security_incident_response
- Strat_O365_IP
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: В этом решении рассказывается о том, как наиболее распространенные атаки с кибератак по безопасности могут выглядеть в Office 365, а также о том, как реагировать на них.
ms.openlocfilehash: 473a7db30df72ecbe0bdc58d578f4c82c31beaca
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217269"
---
# <a name="office-365-security-incident-response"></a><span data-ttu-id="beb7d-103">Реагирование на инциденты, связанные с безопасностью, в Office 365</span><span class="sxs-lookup"><span data-stu-id="beb7d-103">Office 365 Security Incident Response</span></span>

 <span data-ttu-id="beb7d-104">**Сводка:** В этом решении рассказывается о том, что означают индикаторы для наиболее распространенных атак кибератак на систему безопасности в Office 365, как однозначно подтверждать любую атаку и как реагировать на нее.</span><span class="sxs-lookup"><span data-stu-id="beb7d-104">**Summary:** This solution tells you what the indicators are for the most common cyber-security attacks in Office 365, how to positively confirm any given attack, and how to respond to it.</span></span>
  
## <a name="overview"></a><span data-ttu-id="beb7d-105">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="beb7d-105">Overview</span></span>
<span data-ttu-id="beb7d-p101">Не все атаки кибератак могут быть отключены. Злоумышленники постоянно ищет новые слабые места в стратегии защитного обмена или используют старые. Знание того, как распознать атаку, позволяет быстрее реагировать на нее, что сокращает продолжительность инцидента безопасности.</span><span class="sxs-lookup"><span data-stu-id="beb7d-p101">Not all cyber attacks can be thwarted. Attackers are constantly looking for new weaknesses in your defensive strategy or they are exploiting old ones. Knowing how to recognize an attack allows you to respond to it faster, which shortens the duration of the security incident.</span></span>

<span data-ttu-id="beb7d-p102">Эта серия статей поможет вам разобраться, что может выглядеть, как в Office 365, и пошаговые инструкции для ответа. Они являются краткими точками ввода для понимания:</span><span class="sxs-lookup"><span data-stu-id="beb7d-p102">This series of article helps you understand what a particular type of attack might look like in Office 365 and gives you steps you can take to respond. They are quick entry points to understanding:</span></span>
 
- <span data-ttu-id="beb7d-111">Что такое атака и как она работает.</span><span class="sxs-lookup"><span data-stu-id="beb7d-111">What the attack is and how it works.</span></span>
- <span data-ttu-id="beb7d-112">Символы, называемые индикаторами компромиссов (IOC), и способы их поиска.</span><span class="sxs-lookup"><span data-stu-id="beb7d-112">What signs, called indicators of compromise (IOC), to look for and how to look for them.</span></span>
- <span data-ttu-id="beb7d-113">Как вы можете подтвердить атаку.</span><span class="sxs-lookup"><span data-stu-id="beb7d-113">How to positively confirm the attack.</span></span>
- <span data-ttu-id="beb7d-114">Действия, которые необходимо выполнить, чтобы отрезаться от атак и лучше защитить организацию в будущем.</span><span class="sxs-lookup"><span data-stu-id="beb7d-114">Steps to take to cut off the attack and better protect your organization in the future.</span></span>
- <span data-ttu-id="beb7d-115">Ссылки на подробные сведения о каждом типе атаки.</span><span class="sxs-lookup"><span data-stu-id="beb7d-115">Links to in-depth information on each attack type.</span></span>

<span data-ttu-id="beb7d-116">Вернитесь сюда ежемесячно, когда будут добавляться новые статьи со временем.</span><span class="sxs-lookup"><span data-stu-id="beb7d-116">Check back here monthly as more articles will be added over time.</span></span>

## <a name="detect-and-remediate-articles"></a><span data-ttu-id="beb7d-117">Обнаружение и исправление статей</span><span class="sxs-lookup"><span data-stu-id="beb7d-117">Detect and remediate articles</span></span>

- [<span data-ttu-id="beb7d-118">Обнаружение случаев незаконного предоставления разрешений и устранение их последствий в Office 365</span><span class="sxs-lookup"><span data-stu-id="beb7d-118">Detect and Remediate Illicit Consent Grants in Office 365</span></span>](detect-and-remediate-illicit-consent-grants.md)
- [<span data-ttu-id="beb7d-119">Обнаружение атак с внедрением правил и пользовательских форм Outlook и устранение их последствий в Office 365</span><span class="sxs-lookup"><span data-stu-id="beb7d-119">Detect and Remediate Outlook Rules and Custom Forms Injections Attacks in Office 365</span></span>](detect-and-remediate-outlook-rules-forms-attack.md)
 
## <a name="incident-response-articles"></a><span data-ttu-id="beb7d-120">Статьи об отклике инцидента</span><span class="sxs-lookup"><span data-stu-id="beb7d-120">Incident response articles</span></span>

- [<span data-ttu-id="beb7d-121">Реагирование на компрометацию учетной записи электронной почты в Office 365</span><span class="sxs-lookup"><span data-stu-id="beb7d-121">Responding to a Compromised Email Account in Office 365</span></span>](responding-to-a-compromised-email-account.md)

## <a name="secure-office-365-like-a-cybersecurity-pro"></a><span data-ttu-id="beb7d-122">Безопасность Office 365, например, циберсекурити Pro</span><span class="sxs-lookup"><span data-stu-id="beb7d-122">Secure Office 365 like a cybersecurity pro</span></span>
<span data-ttu-id="beb7d-p103">Ваша подписка на Office 365 поставляется с мощным набором возможностей обеспечения безопасности, которые можно использовать для защиты данных и пользователей.  Использование [плана безопасности Office 365: лучшие приоритеты для первых 30 дней, 90 дней и](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) более поздних для реализации рекомендуемых рекомендаций по обеспечению безопасности клиента Office 365.</span><span class="sxs-lookup"><span data-stu-id="beb7d-p103">Your Office 365 subscription comes with a powerful set of security capabilities that you can use to protect your data and your users.  Use the [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) to implement Microsoft recommended best practices for securing your Office 365 tenant.</span></span>
- <span data-ttu-id="beb7d-p104">Задачи, которые необходимо выполнить в течение первых 30 дней.  Они немедленно влияют на работу пользователей и оказывают низкую воздействие.</span><span class="sxs-lookup"><span data-stu-id="beb7d-p104">Tasks to accomplish in the first 30 days.  These have immediate affect and are low-impact to your users.</span></span>
- <span data-ttu-id="beb7d-p105">Задачи, которые необходимо выполнить в течение 90 дней. Для планирования и реализации потребуется немного больше времени, но значительно улучшить безопасность</span><span class="sxs-lookup"><span data-stu-id="beb7d-p105">Tasks to accomplish in 90 days. These take a bit more time to plan and implement but greatly improve your security posture</span></span>
- <span data-ttu-id="beb7d-p106">Больше 90 дней. Эти расширения задействуются в течение первых 90 дней.</span><span class="sxs-lookup"><span data-stu-id="beb7d-p106">Beyond 90 days. These enhancements build in your first 90 days work.</span></span>






