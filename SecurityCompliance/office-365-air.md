---
title: Автоматическое исследование угроз в Office 365 и реагирование на них
keywords: ВОЗДУШный, Аутоир, ATP, автоматизированный, исследование, ответ, исправление, угрозы, усовершенствованный, угроза, защита
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/04/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Приступите к работе с автоматизированным исследованием и возможностями реагирования в Office 365 Advanced Threat Protection Plan 2.
ms.openlocfilehash: 2c64ea936170524811839db7c593d67bfe11a928
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/05/2019
ms.locfileid: "36762031"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a><span data-ttu-id="d3636-104">Автоматическое исследование угроз в Office 365 и реагирование на них</span><span class="sxs-lookup"><span data-stu-id="d3636-104">Automatically investigate and respond to threats in Office 365</span></span>

## <a name="overview"></a><span data-ttu-id="d3636-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="d3636-105">Overview</span></span>

<span data-ttu-id="d3636-106">[Office 365 Advanced Threat protection](office-365-atp.md) План 2 включает возможности автоматического исследования и реагирования (AIR), которые могут сэкономить время и усилия группы управления безопасностью при работе с оповещениями и угрозами.</span><span class="sxs-lookup"><span data-stu-id="d3636-106">[Office 365 Advanced Threat Protection](office-365-atp.md) Plan 2 includes automated investigation and response (AIR) capabilities that can save your security operations team time and effort in dealing with alerts and threats.</span></span> <span data-ttu-id="d3636-107">В этой статье приводятся сведения о том, как приступить к работе с возможностями AIR в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d3636-107">Read this article to get started using AIR capabilities in Office 365.</span></span> <span data-ttu-id="d3636-108">Чтобы узнать больше о работе воздуха, ознакомьтесь с разработкой [автоматизированного расследования и ответа (AIR) с Office 365](automated-investigation-response-office.md).</span><span class="sxs-lookup"><span data-stu-id="d3636-108">To learn more about how AIR works, see [Automated Investigation and Response (AIR) with Office 365](automated-investigation-response-office.md).</span></span>

<span data-ttu-id="d3636-109">В среде AIR при запуске определенных оповещений запускается один или несколько "Playbooks" безопасности, и начинается автоматическое исследование.</span><span class="sxs-lookup"><span data-stu-id="d3636-109">With AIR, when certain alerts are triggered, one or more security playbooks initiate, and automated investigation begins.</span></span> <span data-ttu-id="d3636-110">Во время и после автоматического исследования администраторы и группы управления безопасностью могут выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d3636-110">During and after an automated investigation process, your administrators and security operations team can:</span></span>

- [<span data-ttu-id="d3636-111">Просмотр сведений о расследовании</span><span class="sxs-lookup"><span data-stu-id="d3636-111">View the details of an investigation</span></span>](#view-details-of-an-investigation)

- [<span data-ttu-id="d3636-112">Просмотр и утверждение действий в результате расследования</span><span class="sxs-lookup"><span data-stu-id="d3636-112">Review and approve actions as a result of an investigation</span></span>](#review-and-approve-actions) 

- [<span data-ttu-id="d3636-113">Просмотр сведений о предупреждении, связанных с исследованием</span><span class="sxs-lookup"><span data-stu-id="d3636-113">View details about an alert related to an investigation</span></span>](#view-details-about-an-alert-related-to-an-investigation)

> [!NOTE]
> <span data-ttu-id="d3636-114">Для выполнения задач, описанных в этой статье, необходимо быть глобальным администратором, администратором безопасности, оператором безопасности или средством чтения безопасности.</span><span class="sxs-lookup"><span data-stu-id="d3636-114">You must be a global administrator, security administrator, security operator, or security reader to perform the tasks described in this article.</span></span> <span data-ttu-id="d3636-115">Чтобы узнать больше, ознакомьтесь [со статьей Microsoft 365 Security Center: Roles and Permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span><span class="sxs-lookup"><span data-stu-id="d3636-115">To learn more, see [Microsoft 365 security center: roles and permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span></span>

## <a name="view-details-of-an-investigation"></a><span data-ttu-id="d3636-116">Просмотр сведений о расследовании</span><span class="sxs-lookup"><span data-stu-id="d3636-116">View details of an investigation</span></span>

1. <span data-ttu-id="d3636-117">Как глобальный администратор Office 365, администратор безопасности или средство чтения безопасности, перейдите на [https://protection.office.com](https://protection.office.com) страницу и войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="d3636-117">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="d3636-118">Откроется Центр безопасности & соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d3636-118">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="d3636-119">Выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="d3636-119">Do one of the following:</span></span>

    - <span data-ttu-id="d3636-120">Перейдите на > **панель мониторинга** **управления угрозами**.</span><span class="sxs-lookup"><span data-stu-id="d3636-120">Go to **Threat management** > **Dashboard**.</span></span> <span data-ttu-id="d3636-121">Откроется [панель мониторинга безопасности](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="d3636-121">This takes you to the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="d3636-122">Мини – приложение AIR отображается в верхней части [панели мониторинга безопасности](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="d3636-122">Your AIR widgets appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="d3636-123">Выберите мини-приложение, например " **Сводка по расследованию**".</span><span class="sxs-lookup"><span data-stu-id="d3636-123">Select a widget, such as **Investigations summary**.</span></span>

    - <span data-ttu-id="d3636-124">Перейдите на страницу > **расследования**по **управлению угрозами**.</span><span class="sxs-lookup"><span data-stu-id="d3636-124">Go to **Threat management** > **Investigations**.</span></span> 

    <span data-ttu-id="d3636-125">Любой из способов переводит вас в список расследования.</span><span class="sxs-lookup"><span data-stu-id="d3636-125">Either method takes you to a list of investigations.</span></span>

    ![Страница основного исследования для воздуха](media/air-maininvestigationpage.png) 

3. <span data-ttu-id="d3636-127">В списке исследований выберите элемент в столбце **идентификатор** .</span><span class="sxs-lookup"><span data-stu-id="d3636-127">In the list of investigations, select an item in the **ID** column.</span></span> <span data-ttu-id="d3636-128">Откроется страница "сведения об исследовании", начиная с графика расследования.</span><span class="sxs-lookup"><span data-stu-id="d3636-128">This opens investigation details page, starting with the investigation graph.</span></span>

    ![Страница графа расследования воздуха](media/air-investigationgraphpage.png)

4. <span data-ttu-id="d3636-130">Используйте различные вкладки, чтобы узнать больше о расследовании.</span><span class="sxs-lookup"><span data-stu-id="d3636-130">Use the various tabs to learn more about the investigation.</span></span>

## <a name="review-and-approve-actions"></a><span data-ttu-id="d3636-131">Просмотр и утверждение действий</span><span class="sxs-lookup"><span data-stu-id="d3636-131">Review and approve actions</span></span>

<span data-ttu-id="d3636-132">В Office 365 автоматизированное расследования обычно приводит к одному или нескольким рекомендуемым действиям.</span><span class="sxs-lookup"><span data-stu-id="d3636-132">In Office 365, automated investigations typically result in one or more recommended actions.</span></span> <span data-ttu-id="d3636-133">Тем не менее никакие действия не выполняются до тех пор, пока не будут утверждены Группой действий по обеспечению безопасности.</span><span class="sxs-lookup"><span data-stu-id="d3636-133">However, no actions are taken until they are approved by your security operations team.</span></span> <span data-ttu-id="d3636-134">Используйте следующую процедуру для просмотра и утверждения действий.</span><span class="sxs-lookup"><span data-stu-id="d3636-134">Use the following procedure to review and approve actions.</span></span>

1. <span data-ttu-id="d3636-135">Как глобальный администратор Office 365, администратор безопасности или средство чтения безопасности, перейдите на [https://protection.office.com](https://protection.office.com) страницу и войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="d3636-135">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> 

2. <span data-ttu-id="d3636-136">Перейдите на страницу > **расследования**по **управлению угрозами**.</span><span class="sxs-lookup"><span data-stu-id="d3636-136">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="d3636-137">В списке исследований выберите элемент в столбце **идентификатор** .</span><span class="sxs-lookup"><span data-stu-id="d3636-137">In the list of investigations, select an item in the **ID** column.</span></span> 

3. <span data-ttu-id="d3636-138">В представлении сведения об расследовании перейдите на вкладку **действия** . Здесь перечислены все действия, ожидающие утверждения.</span><span class="sxs-lookup"><span data-stu-id="d3636-138">On the investigation details view, select the **Actions** tab. Any actions that are pending approval are listed here.</span></span>

4. <span data-ttu-id="d3636-139">Выберите элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="d3636-139">Select an item in the list.</span></span>

5. <span data-ttu-id="d3636-140">Выберите **утвердить** , чтобы выполнить рекомендуемое действие (или **отклонить** , чтобы закрыть исследование без принятия действия).</span><span class="sxs-lookup"><span data-stu-id="d3636-140">Select **Approve** to take the recommended action (or **Reject** to close the investigation without taking action).</span></span>

## <a name="view-details-about-an-alert-related-to-an-investigation"></a><span data-ttu-id="d3636-141">Просмотр сведений о предупреждении, связанных с исследованием</span><span class="sxs-lookup"><span data-stu-id="d3636-141">View details about an alert related to an investigation</span></span>

<span data-ttu-id="d3636-142">Определенные виды оповещений инициируют автоматическое исследование в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d3636-142">Certain kinds of alerts trigger automated investigation in Office 365.</span></span> <span data-ttu-id="d3636-143">Чтобы узнать больше, ознакомьтесь со статьей [оповещения](automated-investigation-response-office.md#alerts).</span><span class="sxs-lookup"><span data-stu-id="d3636-143">To learn more, see [Alerts](automated-investigation-response-office.md#alerts).</span></span> <span data-ttu-id="d3636-144">Используйте следующую процедуру для просмотра подробных сведений об оповещении, связанных с автоматическим исследованием.</span><span class="sxs-lookup"><span data-stu-id="d3636-144">Use the following procedure to view details about an alert that is associated with an automated investigation.</span></span>

1. <span data-ttu-id="d3636-145">Как глобальный администратор Office 365, администратор безопасности или средство чтения безопасности, перейдите на [https://protection.office.com](https://protection.office.com) страницу и войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="d3636-145">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="d3636-146">Откроется Центр безопасности & соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="d3636-146">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="d3636-147">Перейдите на страницу > **расследования**по **управлению угрозами**.</span><span class="sxs-lookup"><span data-stu-id="d3636-147">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="d3636-148">В списке исследований выберите элемент в столбце **идентификатор** .</span><span class="sxs-lookup"><span data-stu-id="d3636-148">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="d3636-149">С подробностями открытого исследования перейдите на вкладку **оповещения** . Здесь перечислены все оповещения, которые запускаются в ходе расследования.</span><span class="sxs-lookup"><span data-stu-id="d3636-149">With details of an investigation open, select the **Alerts** tab. Any alerts that triggered the investigation are listed here.</span></span>

5. <span data-ttu-id="d3636-150">Выберите элемент в списке.</span><span class="sxs-lookup"><span data-stu-id="d3636-150">Select an item in the list.</span></span> <span data-ttu-id="d3636-151">Откроется раскрывающееся меню со сведениями об оповещении и ссылками на дополнительные сведения и действия.</span><span class="sxs-lookup"><span data-stu-id="d3636-151">A flyout opens, with details about the alert and links to additional information and actions.</span></span>

6. <span data-ttu-id="d3636-152">Просмотрите сведения в всплывающем меню и, в зависимости от конкретного оповещения, выполните действие, например " **Разрешить**", " **запретить**" или " **уведомить пользователей**".</span><span class="sxs-lookup"><span data-stu-id="d3636-152">Review the information on the flyout, and, depending on the particular alert, take an action, such as **Resolve**, **Suppress**, or **Notify users**.</span></span> 

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="d3636-153">Использование API действий управления Office 365 для настраиваемых и сторонних решений для создания отчетов</span><span class="sxs-lookup"><span data-stu-id="d3636-153">Use the Office 365 Management Activity API for custom or third-party reporting solutions</span></span>

<span data-ttu-id="d3636-154">Если в организации используется пользовательское решение для создания отчетов или решение для создания отчетов стороннего производителя, можно просмотреть сведения об автоматическом расследовании в этом решении с помощью API действий управления Office 365.</span><span class="sxs-lookup"><span data-stu-id="d3636-154">If your organization is using a custom reporting solution, or a third-party reporting solution, you can view information about automated investigations in that solution by using the Office 365 Management Activity API.</span></span>

<span data-ttu-id="d3636-155">Используйте следующие ресурсы для настройки:</span><span class="sxs-lookup"><span data-stu-id="d3636-155">Use the following resources to set this up:</span></span>

|<span data-ttu-id="d3636-156">Ресурс</span><span class="sxs-lookup"><span data-stu-id="d3636-156">Resource</span></span>  |<span data-ttu-id="d3636-157">Описание</span><span class="sxs-lookup"><span data-stu-id="d3636-157">Description</span></span>  |
|---------|---------|
|[<span data-ttu-id="d3636-158">Обзор API управления Office 365</span><span class="sxs-lookup"><span data-stu-id="d3636-158">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)     |<span data-ttu-id="d3636-159">API действий управления Office 365 обеспечивает получение информации о различных действиях и событиях, касающихся пользователей, администраторов, систем и политик, из отчетов о действиях касательно Office 365 и Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3636-159">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span>         |
|[<span data-ttu-id="d3636-160">Начало работы с API управления Office 365</span><span class="sxs-lookup"><span data-stu-id="d3636-160">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |<span data-ttu-id="d3636-161">API управления Office 365 использует Azure AD для предоставления служб проверки подлинности приложениям доступа к данным Office 365.</span><span class="sxs-lookup"><span data-stu-id="d3636-161">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Office 365 data.</span></span> <span data-ttu-id="d3636-162">Выполните действия, описанные в этой статье, чтобы настроить ее.</span><span class="sxs-lookup"><span data-stu-id="d3636-162">Follow the steps in this article to set this up.</span></span>          |
|[<span data-ttu-id="d3636-163">Справочник по API действий управления Office 365</span><span class="sxs-lookup"><span data-stu-id="d3636-163">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |<span data-ttu-id="d3636-164">Вы можете использовать API действий управления Office 365, чтобы получить сведения о действиях пользователя, администратора, системы, а также о событиях и политиках из журналов активности Office 365 и Azure AD.</span><span class="sxs-lookup"><span data-stu-id="d3636-164">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Office 365 and Azure AD activity logs.</span></span> <span data-ttu-id="d3636-165">Прочтите эту статью, чтобы узнать больше о том, как это работает.</span><span class="sxs-lookup"><span data-stu-id="d3636-165">Read this article to learn more about how this works.</span></span>        |
|[<span data-ttu-id="d3636-166">Схема API действий управления Office 365</span><span class="sxs-lookup"><span data-stu-id="d3636-166">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |<span data-ttu-id="d3636-167">В этой статье представлены общие сведения о конкретных типах данных, доступных через API действий управления Office 365, а также сведения о том, как ознакомиться с [общими схемами](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) и сведениями об [анализе и ответе на Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) .</span><span class="sxs-lookup"><span data-stu-id="d3636-167">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>         |

## <a name="next-steps"></a><span data-ttu-id="d3636-168">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="d3636-168">Next steps</span></span>

[<span data-ttu-id="d3636-169">Дополнительные сведения об оповещениях</span><span class="sxs-lookup"><span data-stu-id="d3636-169">Learn more about alerts</span></span>](alert-policies.md)

[<span data-ttu-id="d3636-170">Поиск и исследование вредоносных сообщений электронной почты, доставляемых в Office 365, вручную</span><span class="sxs-lookup"><span data-stu-id="d3636-170">Manually find and investigate malicious email that was delivered in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)

[<span data-ttu-id="d3636-171">Сведения о воздухе воздуха в защитнике Майкрософт для ATP</span><span class="sxs-lookup"><span data-stu-id="d3636-171">Learn about AIR in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

[<span data-ttu-id="d3636-172">Посетите план Microsoft 365, чтобы узнать, что скоро ожидается и как выполняется развертывание.</span><span class="sxs-lookup"><span data-stu-id="d3636-172">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)