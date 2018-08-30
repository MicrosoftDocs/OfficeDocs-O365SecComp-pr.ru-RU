---
title: API действий управления Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Краткая сводка об API действия для управления Office 365.
ms.openlocfilehash: 4753be89c008676d5244b5c659c3dd1a545975b2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534343"
---
# <a name="office-365-management-activity-api"></a><span data-ttu-id="35a32-103">API действий управления Office 365</span><span class="sxs-lookup"><span data-stu-id="35a32-103">Office 365 Management Activity API</span></span>
<span data-ttu-id="35a32-p101">Корпорация Майкрософт предоставляет службы отчетов, которые позволяют администраторам получить сводный транзакций информацию о своих клиента Office 365. [API действия для управления Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) использует стандартные RESTful разработки и OAuth версии 2 для проверки подлинности, что упрощает запуск экспериментировать с извлечения данных и ingesting в средств визуализации и приложения. API-Интерфейс предоставляет данные веб-канал, который содержит сведения об активности пользователей, администратор, операций и безопасности в Office 365. Данные можно в прежнем в целях регулятивным требованиям или в сочетании с данными журнала получены из других источников, чтобы создать мониторинга решение для операций, безопасности и соответствия требованиям в корпоративной среде или локальной инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="35a32-p101">Microsoft provides reporting services that enable administrators to obtain aggregated transactional information about their Office 365 tenant. The [Office 365 Management Activity API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview) uses an industry-standard RESTful design and OAuth v2 for authentication, which makes it easy to start experimenting with retrieving data and ingesting it into visualization tools and applications. The API provides a data feed that includes information about user, administrator, operations, and security activity in Office 365. The data can be kept for regulatory purposes, or combined with log data procured from an on-premises infrastructure or other sources to build a monitoring solution for operations, security, and compliance across the enterprise.</span></span>

<span data-ttu-id="35a32-p102">API действия для управления Office 365 предоставляет сведения о различных пользователей, администрирования, система и действия в рамках политики и события из Office 365 и Azure Active Directory ведение журнала. API-Интерфейс предоставляет схема согласованные аудита с более чем 10 полей, которые являются общими для всех служб. Это позволяет организациям easy подключений между событиями и позволяет новых способов причине по данным. Множество независимых поставщиков программного обеспечения (ISV) партнерские отношения с корпорацией Майкрософт и построение решения, основанные на API. Некоторые решения сосредоточены исключительно на данные Office 365, в то время как другие предоставляют возможность потребления данных из нескольких поставщиков облаке и локальной системы создать единое представление всех операций, безопасности и действий, связанных с соответствием требованиям. Дополнительные сведения содержатся в разделе [Справочник по API действия для управления Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="35a32-p102">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs. The API provides a consistent audit schema with over 10 fields that are in common across all the services. This allows organizations to make easy connections between events, and it enables new ways to reason over the data. Dozens of Independent Software Vendors (ISVs) have partnered with Microsoft and built solutions based on the API. Some solutions are focused solely on Office 365 data, while others provide the ability to ingest data from multiple cloud providers and on-premises systems to create a unified view of all operations, security, and compliance-related activity. For more information, see the [Office 365 Management Activity API reference](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>
