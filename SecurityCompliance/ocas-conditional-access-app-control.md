---
title: Защита приложений с помощью управления условным доступом к приложениям в Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.reviewer: alesibov
ms.audience: Admin
ms.topic: reference
ms.date: 02/14/2019
ms.service: O365-seccomp
localization_priority: Normal
description: Прекращение нарушений и утечки в режиме реального времени с помощью управления приложением Office 365 Cloud App Security.
ms.openlocfilehash: 23c4b29e86eb8ba92cfa8a544d6484965ec6372b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217089"
---
# <a name="protect-apps-with-office-365-cloud-app-security-conditional-access-app-control"></a><span data-ttu-id="fc51f-103">Защита приложений с помощью управления условным доступом к приложениям в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fc51f-103">Protect apps with Office 365 Cloud App Security Conditional Access App Control</span></span>

|<span data-ttu-id="fc51f-104">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="fc51f-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="fc51f-105">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="fc51f-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="fc51f-106">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="fc51f-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="fc51f-107">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fc51f-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="fc51f-108">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="fc51f-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="fc51f-109">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="fc51f-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="fc51f-110">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="fc51f-110">You are here!</span></span>  <br/> [<span data-ttu-id="fc51f-111">Следующее действие</span><span class="sxs-lookup"><span data-stu-id="fc51f-111">Next step</span></span>](ocas-deploy-conditional-access-app-control.md) <br/> |[<span data-ttu-id="fc51f-112">Начало использования</span><span class="sxs-lookup"><span data-stu-id="fc51f-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |

<span data-ttu-id="fc51f-p101">На современном рабочем месте, как правило, недостаточно знать, что происходит в облачной среде после фактического выполнения. Вы хотите прекратить нарушения и утечки в режиме реального времени, прежде чем сотрудники намеренно или случайно помещают свои данные и организацию под угрозой. Важно позволить пользователям в вашей организации максимально использовать службы и средства, доступные для них в облачных приложениях, и позволить им работать с собственными устройствами. В то же время необходимы средства, помогающие защитить организацию от потерь данных, а также кражи данных в режиме реального времени. Вместе с Azure Active Directory, Office 365 Cloud App Security предоставляет эти возможности в едином и интегрированном интерфейсе управления приложением условного доступа.</span><span class="sxs-lookup"><span data-stu-id="fc51f-p101">In today’s workplace, it’s often not enough to know what’s happening in your cloud environment after the fact. You want to stop breaches and leaks in real time, before employees intentionally or inadvertently put your data and your organization at risk. It's important to enable users in your organization to make the most of the services and tools available to them in cloud apps, and let them bring their own devices to work. At the same time, you need tools to help protect your organization from data leaks, and data theft, in real time. Together with Azure Active Directory, Office 365 Cloud App Security delivers these capabilities in a holistic and integrated experience with Conditional Access App Control.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc51f-118">Чтобы использовать элемент управления приложением "условный доступ" в Cloud App Security, вам потребуется  [Лицензия Azure Active Directory P1](https://azure.microsoft.com/pricing/details/active-directory/)и активная подписка на [Cloud App Cloud App Security](office-365-cas-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="fc51f-118">To use Cloud App Security Conditional Access App Control, you need an [Azure Active Directory P1 license](https://azure.microsoft.com/pricing/details/active-directory/) and an active [Office 365 Cloud App Security](office-365-cas-overview.md) subscription.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="fc51f-119">Как это работает</span><span class="sxs-lookup"><span data-stu-id="fc51f-119">How it works</span></span>

<span data-ttu-id="fc51f-p102">Элемент управления "условный доступ" использует архитектуру обратного прокси-сервера и уникально интегрируется с условным доступом к Azure AD. Условный доступ в Azure AD позволяет принудительно применять элементы управления доступом в приложениях вашей организации на основе определенных условий. В условиях определяются пользователи или группы пользователей, а *также то*  *,* что (какие приложения \*\* и какие расположения и сети) применяется к политике условного доступа. После определения условий можно перенаправить пользователей на Office 365 Cloud App Security, где можно защищать данные с помощью элемента управления приложением условного доступа, применяя элементы управления доступом и сеансы.</span><span class="sxs-lookup"><span data-stu-id="fc51f-p102">Conditional Access App Control uses a reverse proxy architecture and is uniquely integrated with Azure AD conditional access. Azure AD conditional access allows you to enforce access controls on your organization’s apps based on certain conditions. The conditions define *who* (user or group of users) and *what* (which cloud apps) and *where* (which locations and networks) a conditional access policy is applied to. After you’ve determined the conditions, you can route users to Office 365 Cloud App Security where you can protect data with Conditional Access App Control by applying access and session controls.</span></span>

<span data-ttu-id="fc51f-p103">Управление приложениями условного доступа позволяет отслеживать и контролировать доступ пользователей к приложениям, а также контролировать их в режиме реального времени на основе политик доступа и сеансов. Политики доступа и сеансов используются в портале Cloud App Security для дальнейшего уточнения фильтров и установки действий, выполняемых с пользователем. С помощью политик доступа и сеансов можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="fc51f-p103">Conditional Access App Control enables user app access and sessions to be monitored and controlled in real time based on access and session policies. Access and session policies are used within the Cloud App Security portal to further refine filters and set actions to be taken on a user. With the access and session policies, you can:</span></span>

- <span data-ttu-id="fc51f-p104">**Блокировать при загрузке**: вы можете заблокировать скачивание конфиденциальных документов. Например, на неуправляемых устройствах.</span><span class="sxs-lookup"><span data-stu-id="fc51f-p104">**Block on download**: You can block the download of sensitive documents. For example, on unmanaged devices.</span></span>

- <span data-ttu-id="fc51f-p105">**Защитить при загрузке**: вместо блокирования загрузки конфиденциальных документов можно включить защиту документов с помощью шифрования при загрузке. Это шифрование гарантирует, что документ защищен, а пользователь получает доступ к нему, если данные загружаются на недоверенное устройство.</span><span class="sxs-lookup"><span data-stu-id="fc51f-p105">**Protect on download**: Instead of blocking the download of sensitive documents, you can require documents to be protected via encryption on download. This encryption makes sure the document is protected and user access is authenticated if the data is downloaded to an untrusted device.</span></span>

- <span data-ttu-id="fc51f-p106">**Мониторинг сеансов пользователей с небольшим уровнем доверия**: рискованные пользователи отслеживаются при входе в приложения, и их действия заносятся в журнал из сеанса. Вы можете изучить и проанализировать поведение пользователя, чтобы узнать, где и при каких условиях политики сеансов следует применять в будущем.</span><span class="sxs-lookup"><span data-stu-id="fc51f-p106">**Monitor low-trust user sessions**: Risky users are monitored when they sign into apps and their actions are logged from within the session. You can investigate and analyze user behavior to understand where, and under what conditions, session policies should be applied in the future.</span></span>

- <span data-ttu-id="fc51f-133">**Блокировать доступ**: вы можете полностью заблокировать доступ к определенным приложениям для пользователей, поступающих из неуправляемых устройств или из некорпоративных сетей.</span><span class="sxs-lookup"><span data-stu-id="fc51f-133">**Block access**: You can completely block access to specific apps for users coming from unmanaged devices or from non-corporate networks.</span></span>

- <span data-ttu-id="fc51f-134">**Создать режим только для чтения**: отслеживая и блокируя настраиваемые действия в приложении, вы можете создать режим только для чтения для определенных приложений для определенных пользователей.</span><span class="sxs-lookup"><span data-stu-id="fc51f-134">**Create read-only mode**: By monitoring and blocking custom in-app activities, you can create a read-only mode to specific apps for specific users.</span></span>

- <span data-ttu-id="fc51f-p107">**Ограничение сеансов пользователей из некорпоративных сетей**: пользователи, обращающиеся к защищенному приложению из расположения, не входящего в корпоративную сеть, могут использовать ограниченный доступ. Загрузка конфиденциальных материалов заблокирована или защищена.</span><span class="sxs-lookup"><span data-stu-id="fc51f-p107">**Restrict user sessions from non-corporate networks**: Users accessing a protected app from a location that isn't part of your corporate network are allowed restricted access. The download of sensitive materials is blocked or protected.</span></span>

### <a name="how-session-control-works"></a><span data-ttu-id="fc51f-137">Принцип работы управления сеансом</span><span class="sxs-lookup"><span data-stu-id="fc51f-137">How session control works</span></span>

<span data-ttu-id="fc51f-p108">Создание политики сеансов с помощью элемента управления "условный доступ" позволяет управлять сеансами пользователей путем перенаправления пользователя с помощью обратного прокси-сервера, а не непосредственно к приложению. После этого запросы пользователей и ответы проходят через Office 365 Cloud App Security, а не непосредственно к приложению.</span><span class="sxs-lookup"><span data-stu-id="fc51f-p108">Creating a session policy with Conditional Access App Control enables you to control user sessions by redirecting the user through a reverse proxy instead of directly to the app. From then on, user requests and responses go through Office 365 Cloud App Security rather than directly to the app.</span></span>

<span data-ttu-id="fc51f-p109">Чтобы сохранить пользователя в сеансе, все нужные URL-адреса, сценарии Java и файлы cookie в сеансе приложения заменяются на URL-адреса безопасности облачных приложений Office 365. Например, если приложение возвращает страницу со ссылками, чьи домены заканчиваются на myapp.com, то ссылка заменяется на домены, заканчивающиеся следующим образом: myapp.com.us.cas.ms</span><span class="sxs-lookup"><span data-stu-id="fc51f-p109">To keep the user within the session, all the relevant URLs, Java scripts, and cookies within the app session are replaced with Office 365 Cloud App Security URLs. For example, if the app returns a page with links whose domains end with myapp.com, the link is replaced with domains ending with something like: myapp.com.us.cas.ms</span></span>

<span data-ttu-id="fc51f-p110">Этот метод не требует установки каких-либо объектов на устройстве. Этот метод идеально подходит при наблюдении за сеансами неуправляемых устройств.</span><span class="sxs-lookup"><span data-stu-id="fc51f-p110">This method doesn't require you to install anything on the device. This method is ideal when monitoring sessions from unmanaged devices.</span></span>

<span data-ttu-id="fc51f-144">После направления сеанса через Office 365 Cloud App Security можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="fc51f-144">After a session is directed through Office 365 Cloud App Security, the following actions can be done:</span></span>

1. <span data-ttu-id="fc51f-145">Проверка трафика для действий пользователей</span><span class="sxs-lookup"><span data-stu-id="fc51f-145">Inspect the traffic for user activities</span></span>

2. <span data-ttu-id="fc51f-146">Отображение определенных действий в журнале действий Cloud App Security для Office 365</span><span class="sxs-lookup"><span data-stu-id="fc51f-146">Display the identified activities in the Office 365 Cloud App Security Activity log</span></span>

3. <span data-ttu-id="fc51f-147">Сохранение и анализ журналов трафика</span><span class="sxs-lookup"><span data-stu-id="fc51f-147">Save the traffic logs and analyze them</span></span>

4. <span data-ttu-id="fc51f-148">Разрешить администратору экспортировать журналы трафика</span><span class="sxs-lookup"><span data-stu-id="fc51f-148">Enable the admin to export the traffic logs</span></span>

5. <span data-ttu-id="fc51f-149">Принудительное применение политик для сеанса</span><span class="sxs-lookup"><span data-stu-id="fc51f-149">Enforce policies on the session</span></span>

## <a name="managed-device-identification"></a><span data-ttu-id="fc51f-150">Идентификация управляемого устройства</span><span class="sxs-lookup"><span data-stu-id="fc51f-150">Managed device identification</span></span>

<span data-ttu-id="fc51f-p111">Элемент управления "условный доступ" позволяет создавать политики, которые определяют, является ли устройство управляемым. Чтобы определить, является ли устройство управляемым, компонент использует:</span><span class="sxs-lookup"><span data-stu-id="fc51f-p111">Conditional Access App Control enables you to create policies that take into account whether a device is managed or not. To identify whether a device is managed or not, the feature uses:</span></span>

- <span data-ttu-id="fc51f-153">Совместимые устройства</span><span class="sxs-lookup"><span data-stu-id="fc51f-153">Compliant devices</span></span>

- <span data-ttu-id="fc51f-154">Устройства, присоединенные к домену</span><span class="sxs-lookup"><span data-stu-id="fc51f-154">Domain-joined devices</span></span>

- <span data-ttu-id="fc51f-155">Развертывание сертификатов клиентов</span><span class="sxs-lookup"><span data-stu-id="fc51f-155">Client certificates deployment</span></span>

### <a name="compliant-and-domain-joined-devices"></a><span data-ttu-id="fc51f-156">Совместимые и подключенные к домену устройства</span><span class="sxs-lookup"><span data-stu-id="fc51f-156">Compliant and domain-joined devices</span></span>

<span data-ttu-id="fc51f-p112">Условный доступ к Azure AD позволяет передавать соответствующие сведения и данные устройств, присоединенных к домену, непосредственно в Office 365 Cloud App Security. В ней можно разрабатывать политику доступа или политику сеанса, которая использует состояние устройства в качестве фильтра. Дополнительные сведения можно найти в статье [Введение в Управление устройствами в Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span><span class="sxs-lookup"><span data-stu-id="fc51f-p112">Azure AD conditional access enables compliant and domain-joined device information to be passed directly to Office 365 Cloud App Security. From there, an access policy or a session policy can be developed that uses device state as a filter. For more information, see the [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/device-management-introduction).</span></span>

### <a name="client-certificate-authenticated-devices"></a><span data-ttu-id="fc51f-160">Клиент — прошедшие проверку подлинности сертификаты устройств</span><span class="sxs-lookup"><span data-stu-id="fc51f-160">Client-certificate authenticated devices</span></span>

<span data-ttu-id="fc51f-p113">Механизм идентификации устройств может запрашивать проверку подлинности на соответствующих устройствах с помощью клиентских сертификатов. Вы можете использовать существующие сертификаты клиентов, уже развернутые в Организации, или развернуть новые сертификаты клиентов для управляемых устройств. Затем используйте сведения о присутствии этих сертификатов, чтобы задать политики доступа и сеансов. Сведения о том, как развертывать сертификаты клиентов, можно найти в разделе [развертывание приложения условНого доступа для приложений Office 365](ocas-deploy-conditional-access-app-control.md).</span><span class="sxs-lookup"><span data-stu-id="fc51f-p113">The device identification mechanism can request authentication from relevant devices using client certificates. You can either use existing client certificates already deployed in your organization or roll out new client certificates to managed devices. You then use the presence of those certificates to set access and session policies. For information on how to deploy client certificates see [Deploy Conditional Access App Control for Office 365 apps](ocas-deploy-conditional-access-app-control.md).</span></span>

## <a name="supported-apps-and-clients"></a><span data-ttu-id="fc51f-165">Поддерживаемые приложения и клиенты</span><span class="sxs-lookup"><span data-stu-id="fc51f-165">Supported apps and clients</span></span>

<span data-ttu-id="fc51f-166">Элемент управления приложением условного доступа для Office 365 поддерживает следующие популярные приложения:</span><span class="sxs-lookup"><span data-stu-id="fc51f-166">Conditional Access App Control for Office 365 supports the following featured apps:</span></span>

- <span data-ttu-id="fc51f-167">Exchange Online (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="fc51f-167">Exchange Online (preview)</span></span>

- <span data-ttu-id="fc51f-168">OneDrive для бизнеса (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="fc51f-168">OneDrive for Business (preview)</span></span>

- <span data-ttu-id="fc51f-169">Power BI (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="fc51f-169">Power BI (preview)</span></span>

- <span data-ttu-id="fc51f-170">SharePoint Online (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="fc51f-170">SharePoint Online (preview)</span></span>

- <span data-ttu-id="fc51f-171">Microsoft Teams (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="fc51f-171">Microsoft Teams (preview)</span></span>

- <span data-ttu-id="fc51f-172">Yammer (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="fc51f-172">Yammer (preview)</span></span>

<span data-ttu-id="fc51f-173">Дополнительные приложения постоянно переносятся на сервер управления сеансами.</span><span class="sxs-lookup"><span data-stu-id="fc51f-173">Additional apps are being continuously on-boarded to session control.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fc51f-174">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="fc51f-174">Next steps</span></span>

- [<span data-ttu-id="fc51f-175">Развертывание управления условным доступом к приложениям для приложений Office 365</span><span class="sxs-lookup"><span data-stu-id="fc51f-175">Deploy Conditional Access App Control for Office 365 apps</span></span>](ocas-deploy-conditional-access-app-control.md)

- [<span data-ttu-id="fc51f-176">Сведения о политиках сеансов в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fc51f-176">Learn about session policies in Office 365 Cloud App Security</span></span>](ocas-session-policies.md)

- [<span data-ttu-id="fc51f-177">Сведения о политиках доступа в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="fc51f-177">Learn about access policies in Office 365 Cloud App Security</span></span>](ocas-access-policies.md) 