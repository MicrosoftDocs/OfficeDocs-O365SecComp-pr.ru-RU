---
title: Office 365 приходится иметь дело с повреждение данных
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
description: Объяснение повреждение данных в Office 365 и усилия корпорации Майкрософт для защиты и восстановления.
ms.openlocfilehash: 087be23ce5dad1daf62357cb08e27c0a15962792
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534939"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="6352f-103">Работа с повреждение данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="6352f-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="6352f-p101">Один из сложного аспектов выполнения большими объемами облачная служба — обработка повреждение данных, присвоенное большого объема данных и системам independent. Повреждение данных может быть вызвана:</span><span class="sxs-lookup"><span data-stu-id="6352f-p101">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems. Data corruption can be caused by:</span></span>
- <span data-ttu-id="6352f-106">Ошибки приложения или инфраструктуры, не повреждая код некоторые или все состояния приложения</span><span class="sxs-lookup"><span data-stu-id="6352f-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="6352f-107">Оборудование в силу своей потерю данных или невозможность чтения данных</span><span class="sxs-lookup"><span data-stu-id="6352f-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="6352f-108">Человеческого действующие ошибки</span><span class="sxs-lookup"><span data-stu-id="6352f-108">Human operational errors</span></span> 
- <span data-ttu-id="6352f-109">Сообщение о нежелательном злоумышленников и недовольные сотрудники</span><span class="sxs-lookup"><span data-stu-id="6352f-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="6352f-110">Происшествия в внешних служб, которые возникают в некоторых потери данных</span><span class="sxs-lookup"><span data-stu-id="6352f-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="6352f-p102">Так как более устойчивости в целостность данных означает, что не более чем происшествия повреждение данных, корпорация Майкрософт создала в Office 365 механизмов защиты, чтобы предотвратить повреждение из-за проблемы, а также систем, которые позволяют "мне нравится" для восстановления данных, если это так. Проверки и процессы существуют в различных этапах проектирования процесса выпуска для повышения устойчивости от повреждения данных, включая:</span><span class="sxs-lookup"><span data-stu-id="6352f-p102">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does. Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="6352f-113">Проект системы</span><span class="sxs-lookup"><span data-stu-id="6352f-113">System Design</span></span>
- <span data-ttu-id="6352f-114">Код организации и структура</span><span class="sxs-lookup"><span data-stu-id="6352f-114">Code organization and structure</span></span> 
- <span data-ttu-id="6352f-115">Проверка кода</span><span class="sxs-lookup"><span data-stu-id="6352f-115">Code review</span></span> 
- <span data-ttu-id="6352f-116">Модульных тестов, тесты интеграции и тестирования системы</span><span class="sxs-lookup"><span data-stu-id="6352f-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="6352f-117">Приема-передачи проводов тестов/шлюзов</span><span class="sxs-lookup"><span data-stu-id="6352f-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="6352f-p103">В производственной среде Office 365 одноранговой репликации между центрами обработки данных гарантирует, что всегда существует несколько live копий всех данных. Стандартные изображения и сценарии используются для восстановления потерянных серверов и реплицированные данные используется для восстановления данных клиента. Из-за проверки устойчивости встроенных данных и процессов Корпорация Майкрософт поддерживает резервное копирование только документации сведения о системе Office 365 (включая документацию, связанные с безопасностью), с помощью встроенных репликации в SharePoint Online и внутреннего кода Средство репозитория хранилищем исходного кода. Документация по системе хранится в SharePoint Online и хранилищем исходного кода содержит изображения, системы и приложений. SharePoint Online и хранилищем исходного кода использования управления версиями и реплицируются в почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="6352f-p103">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data. Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data. Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot. System documentation is stored in SharePoint Online, and Source Depot contains system and application images. Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 