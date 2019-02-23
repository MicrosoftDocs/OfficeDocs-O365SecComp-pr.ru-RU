---
title: API действий управления Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
description: Краткое описание API действий управления Office 365.
ms.openlocfilehash: df90eba0d019a862d4699f3e2aa0a04e88b0c371
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214579"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="09e7a-103">API действий управления Office 365</span><span class="sxs-lookup"><span data-stu-id="09e7a-103">Office 365 Management Activity API</span></span>
<span data-ttu-id="09e7a-p101">Корпорация Майкрософт предоставляет службы отчетов, которые позволяют администраторам получать объединенные сведения о транзакциях о своем клиенте Office 365. В [API действий управления Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) для проверки подлинности используется стандартная схема RESTful и OAuth v2 для проверки подлинности, что упрощает эксперименты с извлечением данных и их использованием в средствах и приложениях для визуализации. API предоставляет канал данных, включающий сведения о пользователях, администраторах, операциях и действиях по обеспечению безопасности в Office 365. Данные можно хранить в соответствии с нормативными требованиями или в сочетании с данными журналов, полученными из локальной инфраструктуры или других источников, для создания решения мониторинга для операций, безопасности и соответствия требованиям в Организации.</span><span class="sxs-lookup"><span data-stu-id="09e7a-p101">Microsoft provides reporting services that enable administrators to obtain aggregated transactional information about their Office 365 tenant. The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) uses an industry-standard RESTful design and OAuth v2 for authentication, which makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications. The API provides a data feed that includes information about user, administrator, operations, and security activity in Office 365. The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources to build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="09e7a-p102">API действий управления Office 365 предоставляет сведения о различных действиях и событиях пользователя, администратора, системы и политики из журналов активности Office 365 и Azure Active Directory. API предоставляет единообразную схему аудита с более чем 10 полями, которые являются общими для всех служб. Это позволяет организациям легко подключаться между событиями и обеспечивает новые способы определения причин для данных. Десятки независимых поставщиков программного обеспечения (ISV) поСтавляются с корпорацией Майкрософт и построенными решениями на основе API. Некоторые решения ориентированы исключительно на данные Office 365, а другие предоставляют возможность получения данных от нескольких облачных поставщиков и локальных систем для создания единого представления всех операций, безопасности и действий, связанных с соответствием соответствия требованиям. Дополнительные сведения см. в справочнике по [API действий управления Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="09e7a-p102">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs. The API provides a consistent audit schema with over 10 fields that are in common across all the services. This allows organizations to make easy connections between events, and it enables new ways to reason over the data. Dozens of Independent Software Vendors (ISVs) have partnered with Microsoft and built solutions based on the API. Some solutions are focused solely on Office 365 data, while others provide the ability to ingest data from multiple cloud providers and on-premises systems to create a unified view of all operations, security, and compliance-related activity. For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>
