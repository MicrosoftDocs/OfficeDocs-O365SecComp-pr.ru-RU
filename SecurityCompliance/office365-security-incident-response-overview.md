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
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.custom: ''
ms.assetid: ''
description: В этом решении сообщает о том, может выглядеть атаки вы какие наиболее распространенные через Интернет безопасности в Office 365 и реагировать на них
ms.openlocfilehash: 3b72b9bf8c68df2fcc1233b56ee33eaf45695bfe
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535263"
---
# <a name="office-365-security-incident-response"></a><span data-ttu-id="97011-103">Реагирование на инциденты, связанные с безопасностью, в Office 365</span><span class="sxs-lookup"><span data-stu-id="97011-103">Office 365 Security Incident Response</span></span>

 <span data-ttu-id="97011-104">**Сводка:** В этом решении вы найдете являются следующие показатели для самых распространенных атак через Интернет безопасности в Office 365, однозначно подтвердить любого заданного атаки и реагировать на них.</span><span class="sxs-lookup"><span data-stu-id="97011-104">**Summary:** This solution tells you what the indicators are for the most common cyber-security attacks in Office 365, how to positively confirm any given attack, and how to respond to it.</span></span>
  
## <a name="overview"></a><span data-ttu-id="97011-105">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="97011-105">Overview</span></span>
<span data-ttu-id="97011-p101">Не все атаки через Интернет может быть остановлен. Злоумышленники постоянно ищут новые слабые стороны в вашей стратегии безопасности или они развиваются старых. Знать, как будет распознавать атаки позволяет быстрее принимать решения, чтобы его, который сокращает продолжительность происшествие безопасности.</span><span class="sxs-lookup"><span data-stu-id="97011-p101">Not all cyber attacks can be thwarted. Attackers are constantly looking for new weaknesses in your defensive strategy or they are exploiting old ones. Knowing how to recognize an attack allows you to respond to it faster, which shortens the duration of the security incident.</span></span>

<span data-ttu-id="97011-p102">В этой серии статья поможет вам понять, как может выглядеть определенного типа атаки в Office 365 и дает действия, которые нужно выполнить для ответа. Они являются точки быстрого входа в общее представление о:</span><span class="sxs-lookup"><span data-stu-id="97011-p102">This series of article helps you understand what a particular type of attack might look like in Office 365 and gives you steps you can take to respond. They are quick entry points to understanding:</span></span>
 
- <span data-ttu-id="97011-111">Какие атаки и как он работает.</span><span class="sxs-lookup"><span data-stu-id="97011-111">What the attack is and how it works.</span></span>
- <span data-ttu-id="97011-112">Что входит вызывается индикаторы компромиссов (IOC) для поиска и способы их поиск.</span><span class="sxs-lookup"><span data-stu-id="97011-112">What signs, called indicators of compromise (IOC), to look for and how to look for them.</span></span>
- <span data-ttu-id="97011-113">Как однозначно подтвердить атаки.</span><span class="sxs-lookup"><span data-stu-id="97011-113">How to positively confirm the attack.</span></span>
- <span data-ttu-id="97011-114">Шаги по обрезанными атаки и лучше защитить организацию в будущем.</span><span class="sxs-lookup"><span data-stu-id="97011-114">Steps to take to cut off the attack and better protect your organization in the future.</span></span>
- <span data-ttu-id="97011-115">Ссылки на более подробные сведения о каждом атаки типа.</span><span class="sxs-lookup"><span data-stu-id="97011-115">Links to in-depth information on each attack type.</span></span>

<span data-ttu-id="97011-116">Обратитесь к этому списку ежемесячно будут добавлены дополнительные статьи по времени.</span><span class="sxs-lookup"><span data-stu-id="97011-116">Check back here monthly as more articles will be added over time.</span></span>

## <a name="detect-and-remediate-articles"></a><span data-ttu-id="97011-117">Обнаружение и устранение статьи</span><span class="sxs-lookup"><span data-stu-id="97011-117">Detect and Remediate Articles</span></span>
- [<span data-ttu-id="97011-118">Обнаружение случаев незаконного предоставления разрешений и устранение их последствий в Office 365</span><span class="sxs-lookup"><span data-stu-id="97011-118">Detect and Remediate Illicit Consent Grants in Office 365</span></span>](detect-and-remediate-illicit-consent-grants.md)
- [<span data-ttu-id="97011-119">Обнаружение атак с внедрением правил и пользовательских форм Outlook и устранение их последствий в Office 365</span><span class="sxs-lookup"><span data-stu-id="97011-119">Detect and Remediate Outlook Rules and Custom Forms Injections Attacks in Office 365</span></span>](detect-and-remediate-outlook-rules-forms-attack.md)
 
## <a name="secure-office-365-like-a-cybersecurity-pro"></a><span data-ttu-id="97011-120">Безопасность Office 365 как cybersecurity pro</span><span class="sxs-lookup"><span data-stu-id="97011-120">Secure Office 365 like a cybersecurity pro</span></span>
<span data-ttu-id="97011-p103">Подписки Office 365, поступающие с набором мощные возможности безопасности, которые можно использовать для защиты данных и вашим пользователям.  Использование [план обеспечения безопасности Office 365: наиболее распространенные приоритеты для первого 30 дней, 90 дней и за ее пределами](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) для реализации Майкрософт, рекомендации по обеспечению безопасности клиента Office 365.</span><span class="sxs-lookup"><span data-stu-id="97011-p103">Your Office 365 subscription comes with a powerful set of security capabilities that you can use to protect your data and your users.  Use the [Office 365 security roadmap: Top priorities for the first 30 days, 90 days, and beyond](https://support.office.com/article/Office-365-security-roadmap-Top-priorities-for-the-first-30-days-90-days-and-beyond-28c86a1c-e4dd-4aad-a2a6-c768a21cb352) to implement Microsoft recommended best practices for securing your Office 365 tenant.</span></span>
- <span data-ttu-id="97011-p104">Задачи, для выполнения в течение 30 дней.  Эти интерпретации влияют и низкой воздействия на компьютерах пользователей.</span><span class="sxs-lookup"><span data-stu-id="97011-p104">Tasks to accomplish in the first 30 days.  These have immediate affect and are low-impact to your users.</span></span>
- <span data-ttu-id="97011-p105">Задачи, для выполнения в течение 90 дней. Они имеют немного больше времени для планирования и реализации, но значительно повышения уровня безопасности</span><span class="sxs-lookup"><span data-stu-id="97011-p105">Tasks to accomplish in 90 days. These take a bit more time to plan and implement but greatly improve your security posture</span></span>
- <span data-ttu-id="97011-p106">Помимо 90 дней. Эти усовершенствования построения в первом работу 90 дней.</span><span class="sxs-lookup"><span data-stu-id="97011-p106">Beyond 90 days. These enhancements build in your first 90 days work.</span></span>






