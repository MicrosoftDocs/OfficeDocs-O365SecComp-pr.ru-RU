---
title: Office 365 работа с повреждением данных
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Объяснение повреждений данных в Office 365 и действий корпорации Майкрософт по предотвращению и восстановлению.
ms.openlocfilehash: 9bf55243399ecd9f01f736e2da70d7c07231fa63
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262831"
---
# <a name="dealing-with-data-corruption-in-office-365"></a><span data-ttu-id="780e1-103">Работа с Повреждениеми данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="780e1-103">Dealing with Data Corruption in Office 365</span></span>

<span data-ttu-id="780e1-104">Одним из незначительных аспектов запуска крупномасштабной облачной службы является способ обработки повреждений данных с учетом большого объема данных и независимых систем.</span><span class="sxs-lookup"><span data-stu-id="780e1-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="780e1-105">Повреждение данных может быть вызвано следующими причинами:</span><span class="sxs-lookup"><span data-stu-id="780e1-105">Data corruption can be caused by:</span></span>
- <span data-ttu-id="780e1-106">Ошибки приложений или инфраструктуры, повреждение некоторых или всех состояний приложения</span><span class="sxs-lookup"><span data-stu-id="780e1-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span> 
- <span data-ttu-id="780e1-107">Проблемы с оборудованием, приводящие к потере данных или невозможности чтения данных</span><span class="sxs-lookup"><span data-stu-id="780e1-107">Hardware issues that result in lost data or an inability to read data</span></span> 
- <span data-ttu-id="780e1-108">Рабочие ошибки людей</span><span class="sxs-lookup"><span data-stu-id="780e1-108">Human operational errors</span></span> 
- <span data-ttu-id="780e1-109">Вредоносные хакеры и дисгрунтлед сотрудники</span><span class="sxs-lookup"><span data-stu-id="780e1-109">Malicious hackers and disgruntled employees</span></span> 
- <span data-ttu-id="780e1-110">Инциденты во внешних службах, которые приводят к потере данных</span><span class="sxs-lookup"><span data-stu-id="780e1-110">Incidents in external services that result in some loss of data</span></span> 

<span data-ttu-id="780e1-111">Так как более высокая устойчивость целостности данных означает меньше случаев повреждения данных, корпорация Майкрософт встроена в механизмы защиты Office 365, чтобы предотвратить возникновение повреждений, а также системы и процессы, которые позволяют нам восстанавливать данные, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="780e1-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Office 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="780e1-112">Проверки и процессы существуют на различных стадиях процесса инженерного выпуска, чтобы повысить устойчивость к повреждению данных, в том числе:</span><span class="sxs-lookup"><span data-stu-id="780e1-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>
- <span data-ttu-id="780e1-113">Проектирование системы</span><span class="sxs-lookup"><span data-stu-id="780e1-113">System Design</span></span>
- <span data-ttu-id="780e1-114">Организация и структура кода</span><span class="sxs-lookup"><span data-stu-id="780e1-114">Code organization and structure</span></span> 
- <span data-ttu-id="780e1-115">Проверка кода</span><span class="sxs-lookup"><span data-stu-id="780e1-115">Code review</span></span> 
- <span data-ttu-id="780e1-116">Модульные тесты, тесты интеграции и системные тесты</span><span class="sxs-lookup"><span data-stu-id="780e1-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="780e1-117">Тесты и вентили для обработки проводов</span><span class="sxs-lookup"><span data-stu-id="780e1-117">Trip wires tests/gates</span></span> 

<span data-ttu-id="780e1-118">В рабочих средах Office 365 одноранговая репликация между центрами обработки данных гарантирует, что всегда существует несколько динамических копий данных.</span><span class="sxs-lookup"><span data-stu-id="780e1-118">Within Office 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="780e1-119">Для восстановления потерянных серверов используются стандартные изображения и сценарии, а реплицированные данные используются для восстановления данных клиента.</span><span class="sxs-lookup"><span data-stu-id="780e1-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="780e1-120">Из-за встроенных проверок и процедур обеспечения устойчивости данных корпорация Майкрософт поддерживает только резервные копии документации по информационным системам Office 365 (включая документацию по безопасности), используя встроенную репликацию в SharePoint Online и внутренний код средство репозитория, Source Депот.</span><span class="sxs-lookup"><span data-stu-id="780e1-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Office 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="780e1-121">Системная документация хранится в SharePoint Online, а Source Депот содержит изображения системы и приложения.</span><span class="sxs-lookup"><span data-stu-id="780e1-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="780e1-122">SharePoint Online и Source Депот используют управление версиями и реплицируются почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="780e1-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real-time.</span></span> 