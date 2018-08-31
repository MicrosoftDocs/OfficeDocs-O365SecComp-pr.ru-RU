---
title: Ограничения ресурсов для Office 365
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
description: 'Сводка: Сведения о ресурсе ограничения для различных приложений в Office 365.'
ms.openlocfilehash: a2e7ef42f9bf224363f3b10a5e450d6127f11585
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535512"
---
# <a name="resource-limits"></a>Ограничения ресурсов

С помощью квот (ограничения) и регулирования принудительно применяются ограничения ресурсов. Отдельные службы Office 365 и Azure Active Directory используйте их вместе. Ограничения для конкретной службы и измените по времени по мере добавления новых возможностей. Сведения о текущем ограничения для различных служб содержатся в следующих разделах:
- [Ограничения для службы Active Directory и ограничения для Azure](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [Ограничения Exchange Online](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [Ограничения Exchange Online Protection](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [SharePoint Online программные ограничения и лимиты](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Скайп для ограничения для бизнеса](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [Ограничения скорости и API-Интерфейс REST Yammer](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Ограничения на размер файла в Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

В дополнение к эти ограничения несколько механизмы регулирования используются в Office 365 и Azure Active Directory. Регулирование службы особенно важно, учитывая, что сетевых ресурсов в центрах обработки данных Майкрософт, оптимизированные для широкий набор клиентов, использующих службы. Механизмы регулирования, относятся:
- Azure Active Directory и регулирования уровня пользователя компонентов Office 365, которые ограничить число транзакций или одновременных звонков (по сценарий или код), которые могут выполняться с одним пользователем.
- По умолчанию политики регулирования PowerShell назначается для каждого клиента при создании клиента. Эти параметры влияют на других элементов, таких как максимальное количество одновременных сеансов PowerShell, которые можно открыть в одной администратор.
- Каждый клиент Exchange Online имеет политику по умолчанию веб-служб Exchange (EWS), который настроен для операций клиента веб-служб Exchange и регулирования, который применяется для всех клиентов Outlook.
