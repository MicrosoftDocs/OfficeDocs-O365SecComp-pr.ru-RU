---
title: Изоляция и управление доступом в Office 365 в Azure Active Directory
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Сводка. как работают изоляция и управление доступом в Azure Active Directory.
ms.openlocfilehash: 01103361a084d50adbc6c0a8351d9af8311a39fd
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090511"
---
# <a name="isolation-and-access-control-in-azure-active-directory"></a><span data-ttu-id="fc4cf-103">Изоляция и управление доступом в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fc4cf-103">Isolation and Access Control in Azure Active Directory</span></span>

<span data-ttu-id="fc4cf-p101">Azure Active Directory была разработана для более надежного размещения нескольких клиентов с помощью логической изоляции данных. Доступ к Azure Active Directory наследуется уровнем авторизации. Azure Active Directory изолирует клиентов с помощью контейнеров клиентов как границы безопасности для защиты контента клиента, чтобы получить доступ к содержимому и получить к нему доступ с помощью совместных клиентов. Уровень авторизации Azure Active Directory выполняется для трех проверок:</span><span class="sxs-lookup"><span data-stu-id="fc4cf-p101">Azure Active Directory was designed to host multiple tenants in a highly secure way through logical data isolation. Access to Azure Active Directory is gated by an authorization layer. Azure Active Directory isolates customers using tenant containers as security boundaries to safeguard a customer's content so that the content cannot be accessed or compromised by co-tenants. Three checks are performed by Azure Active Directory's authorization layer:</span></span>
- <span data-ttu-id="fc4cf-108">Включен участник для доступа к клиенту Azure Active Directory?</span><span class="sxs-lookup"><span data-stu-id="fc4cf-108">Is the principal enabled for access to Azure Active Directory tenant?</span></span>
- <span data-ttu-id="fc4cf-109">Включен участник для доступа к данным в этом клиенте?</span><span class="sxs-lookup"><span data-stu-id="fc4cf-109">Is the principal enabled for access to data in this tenant?</span></span>
- <span data-ttu-id="fc4cf-110">Роль субъекта в этом клиенте авторизована для типа запрашиваемого доступа к данным?</span><span class="sxs-lookup"><span data-stu-id="fc4cf-110">Is the principal's role in this tenant authorized for the type of data access requested?</span></span>

<span data-ttu-id="fc4cf-p102">Нет приложений, пользователей, серверов и служб, которые могут получить доступ к Azure Active Directory без соответствующей проверки подлинности, маркера или сертификата. Запросы отклоняются, если они не сопровождаются правильными учетными данными.</span><span class="sxs-lookup"><span data-stu-id="fc4cf-p102">No application, user, server, or service can access Azure Active Directory without the proper authentication and token or certificate. Requests are rejected if they are not accompanied by proper credentials.</span></span>

<span data-ttu-id="fc4cf-113">Фактически, Azure Active Directory размещает каждый клиент в собственном защищенном контейнере, с политиками и разрешениями, а также в контейнере исключительно владельцем и управлением клиентом.</span><span class="sxs-lookup"><span data-stu-id="fc4cf-113">Effectively, Azure Active Directory hosts each tenant in its own protected container, with policies and permissions to and within the container solely owned and managed by the tenant.</span></span>
 
![Контейнер Azure](media/office-365-isolation-azure-container.png)

<span data-ttu-id="fc4cf-p103">Понятие контейнеров клиентов глубоко недетализировано в службе каталогов на всех уровнях, от всех порталов до постоянного хранилища. Даже если несколько метаданных клиента Azure Active Directory хранятся на одном физическом диске, связь между контейнерами, отличными от того, что определено службой каталогов, в свою очередь определяется администратором клиента. Не существует прямого подключения к хранилищу Azure Active Directory из запрашивающего приложения или службы без предварительного прохода по уровню авторизации.</span><span class="sxs-lookup"><span data-stu-id="fc4cf-p103">The concept of tenant containers is deeply ingrained in the directory service at all layers, from portals all the way to persistent storage. Even when multiple Azure Active Directory tenant metadata is stored on the same physical disk, there is no relationship between the containers other than what is defined by the directory service, which in turn is dictated by the tenant administrator. There can be no direct connections to Azure Active Directory storage from any requesting application or service without first going through the authorization layer.</span></span>

<span data-ttu-id="fc4cf-118">В приведенном ниже примере Contoso и Fabrikam имеют отдельные выделенные контейнеры, и даже несмотря на то, что эти контейнеры могут совместно использовать одну и ту же базовую инфраструктуру, например серверы и хранилища, они не отличаются друг от друга и имеют уровни авторизации и управления доступом.</span><span class="sxs-lookup"><span data-stu-id="fc4cf-118">In the example below, Contoso and Fabrikam both have separate, dedicated containers, and even though those containers may share some of the same underlying infrastructure, such as servers and storage, they remain separate and isolated from each other, and gated by layers of authorization and access control.</span></span>
 
![Выделенные контейнеры Azure](media/office-365-isolation-azure-dedicated-containers.png)

<span data-ttu-id="fc4cf-120">Кроме того, не существует компонентов приложений, которые можно выполнить из Azure Active Directory, и невозможно принудительно подсчитать целостность другого клиента, получить доступ к ключам шифрования другого клиента или прочитать необработанные данные с сервера.</span><span class="sxs-lookup"><span data-stu-id="fc4cf-120">In addition, there are no application components that can execute from within Azure Active Directory, and it is not possible for one tenant to forcibly breach the integrity of another tenant, access encryption keys of another tenant, or read raw data from the server.</span></span>

<span data-ttu-id="fc4cf-p104">По умолчанию Azure Active Directory запрещает все операции, выданные удостоверениями в других клиентах. Каждый клиент логически изолирован в Azure Active Directory с помощью управления доступом на основе утверждений. Операции чтения и записи данных каталога ограничены контейнерами клиента и разделяются внутренним уровнем абстракции и уровнем управления доступом на основе ролей (RBAC), который совместно применяет клиент к границе безопасности. Каждый запрос на доступ к данным каталога обрабатывается этими слоями, и каждый запрос на доступ в Office 365 наследует логику выше.</span><span class="sxs-lookup"><span data-stu-id="fc4cf-p104">By default, Azure Active Directory disallows all operations issued by identities in other tenants. Each tenant is logically isolated within Azure Active Directory through claims-based access controls. Reads and writes of directory data are scoped to tenant containers, and gated by an internal abstraction layer and a role-based access control (RBAC) layer, which together enforce the tenant as the security boundary. Every directory data access request is processed by these layers and every access request in Office 365 is policed by the logic above.</span></span>

<span data-ttu-id="fc4cf-p105">У Azure Active Directory есть Северная Америка, США, Европейский союз, Европейский союз, Германия и Международный раздел. Клиент существует в отдельном разделе, а разделы могут содержать несколько клиентов. Сведения о разделах отменяются от пользователей. Данный раздел (включая все клиенты в нем) реплицируется в несколько центров обработки данных. Раздел для клиента выбирается на основе свойств клиента (например, кода страны). Секреты и другие конфиденциальные сведения в каждом разделе шифруются с помощью выделенного ключа. Ключи создаются автоматически при создании нового раздела.</span><span class="sxs-lookup"><span data-stu-id="fc4cf-p105">Azure Active Directory has North America, U.S. Government, European Union, Germany, and World Wide partitions. A tenant exists in a single partition, and partitions can contain multiple tenants. Partition information is abstracted away from users. A given partition (including all the tenants within it) is replicated to multiple datacenters. The partition for a tenant is chosen based on properties of the tenant (e.g., the country code). Secrets and other sensitive information in each partition is encrypted with a dedicated key. The keys are generated automatically when a new partition is created.</span></span>

<span data-ttu-id="fc4cf-p106">Функциональные возможности системы Azure Active Directory — это уникальный экземпляр для каждого сеанса пользователя. Кроме того, в Azure Active Directory используются технологии шифрования для обеспечения изоляции общих системных ресурсов на уровне сети для предотвращения несанкционированных и нежелательных передач данных.</span><span class="sxs-lookup"><span data-stu-id="fc4cf-p106">Azure Active Directory system functionalities are a unique instance to each user session. In addition, Azure Active Directory uses encryption technologies to provide isolation of shared system resources at the network level to prevent unauthorized and unintended transfer of information.</span></span>
