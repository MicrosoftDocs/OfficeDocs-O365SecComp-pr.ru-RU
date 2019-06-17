---
title: Общие сведения о барьерах
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 06/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Используйте информационные барьеры, чтобы обеспечить соответствие требованиям, используя Microsoft Teams в вашей организации.
ms.openlocfilehash: a2c202d08f1de60f92f13b2ac4c2b9d3c7f900e8
ms.sourcegitcommit: eeb51470d8996e93fac28d7f12c6117e2aeb0cf0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/14/2019
ms.locfileid: "34935941"
---
# <a name="information-barriers-preview"></a><span data-ttu-id="3924c-103">Препятствия для информационных заданных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="3924c-103">Information barriers (Preview)</span></span>

## <a name="overview"></a><span data-ttu-id="3924c-104">Обзор</span><span class="sxs-lookup"><span data-stu-id="3924c-104">Overview</span></span>

<span data-ttu-id="3924c-105">Облачные службы Майкрософт включают мощные возможности общения и совместной работы.</span><span class="sxs-lookup"><span data-stu-id="3924c-105">Microsoft cloud services include powerful communication and collaboration capabilities.</span></span> <span data-ttu-id="3924c-106">Однако предположим, что вы хотите ограничить связь между двумя группами, чтобы избежать конфликта интересов в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="3924c-106">But suppose that you want to restrict communications between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="3924c-107">Или, возможно, вы хотите ограничить связь между определенными пользователями в Организации, чтобы защитить внутреннюю информацию.</span><span class="sxs-lookup"><span data-stu-id="3924c-107">Or, perhaps you want to restrict communications between certain people inside your organization in order to safeguard internal information.</span></span> <span data-ttu-id="3924c-108">Microsoft 365 обеспечивает взаимодействие и совместную работу между группами и организациями, поэтому существует ли способ ограничения взаимодействия между определенными группами пользователей, когда это необходимо?</span><span class="sxs-lookup"><span data-stu-id="3924c-108">Microsoft 365 enables communication and collaboration across groups and organizations, so is there a way to restrict communications among specific groups of users when necessary?</span></span> <span data-ttu-id="3924c-109">С помощью информационных барьеров вы можете!</span><span class="sxs-lookup"><span data-stu-id="3924c-109">With information barriers, you can!</span></span> 

<span data-ttu-id="3924c-110">Информационные барьеры теперь доступны в предварительной версии, начиная с Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="3924c-110">Information barriers are in preview now, beginning with Microsoft Teams.</span></span> <span data-ttu-id="3924c-111">Если эти функции доступны в вашей организации, администратор соответствия требованиям или администратору по управлению сведениями могут определять политики для разрешения или запрета связи между группами пользователей в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="3924c-111">When these features are available for your organization, a compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="3924c-112">Политики барьера информации могут использоваться в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="3924c-112">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="3924c-113">День торговца не может вызвать кого-либо в группе маркетинга</span><span class="sxs-lookup"><span data-stu-id="3924c-113">A day trader cannot call someone on the marketing team</span></span>
- <span data-ttu-id="3924c-114">Сотрудники отдела финансов, работающие с конфиденциальной информацией о компании, не могут принимать звонки из определенных групп в своей организации.</span><span class="sxs-lookup"><span data-stu-id="3924c-114">Finance personnel working on confidential company information cannot receive calls from certain groups within their organization</span></span>
- <span data-ttu-id="3924c-115">Внутренняя группа с коммерческими секретными материалами не может звонить или общаться с пользователями в определенных группах в Организации</span><span class="sxs-lookup"><span data-stu-id="3924c-115">An internal team with trade secret material cannot call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="3924c-116">Команда исследования может звонить или общаться через Интернет только с помощью команды разработчиков продуктов</span><span class="sxs-lookup"><span data-stu-id="3924c-116">A research team can only call or chat online with a product development team</span></span>

<span data-ttu-id="3924c-117">Для всех приведенных ниже примеров сценариев (и более) можно определить политики информационных барьеров, чтобы запретить или разрешить взаимодействие в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="3924c-117">For all of these example scenarios (and more), information barrier policies can be defined to prevent or allow communications in Microsoft Teams.</span></span> <span data-ttu-id="3924c-118">Такие политики могут препятствовать абонентам звонить или общаться, которые им не нужны, или разрешить пользователям общаться только с определенными группами в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="3924c-118">Such policies can prevent people from calling or chatting with those they shouldn't, or enable people to communicate only with specific groups in Microsoft Teams.</span></span> <span data-ttu-id="3924c-119">С действующими политиками для работы с информационными барьерами, когда пользователи, покрытые этими политиками, пытаются связаться с другими пользователями в Microsoft Teams, выполняются проверки, чтобы запретить (или разрешить) связь (как определено политиками барьера информации).</span><span class="sxs-lookup"><span data-stu-id="3924c-119">With information barrier policies in effect, whenever users who are covered by those policies attempt to communicate with others in Microsoft Teams, checks are done to prevent (or allow) communication (as defined by information barrier policies).</span></span> <span data-ttu-id="3924c-120">Чтобы узнать больше о пользовательском интерфейсе с помощью барьеров информации, ознакомьтесь с разделом [Information барьеры в Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span><span class="sxs-lookup"><span data-stu-id="3924c-120">To learn more about the user experience with information barriers, see [information barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span></span>

> [!NOTE]
> <span data-ttu-id="3924c-121">Информационные барьеры не будут применяться к сообщениям электронной почты или к общему доступу к файлам через SharePoint Online или OneDrive.</span><span class="sxs-lookup"><span data-stu-id="3924c-121">Information barriers will not apply to email communications or to file sharing through SharePoint Online or OneDrive.</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="3924c-122">Необходимые лицензии и разрешения</span><span class="sxs-lookup"><span data-stu-id="3924c-122">Required licenses and permissions</span></span>

<span data-ttu-id="3924c-123">В **настоящее время функция "барьер данных" находится в частном предварительной версии**.</span><span class="sxs-lookup"><span data-stu-id="3924c-123">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="3924c-124">Если эти функции, как правило, доступны, они будут включены в подписки, например:</span><span class="sxs-lookup"><span data-stu-id="3924c-124">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="3924c-125">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="3924c-125">Microsoft 365 E5</span></span>
- <span data-ttu-id="3924c-126">Office 365</span><span class="sxs-lookup"><span data-stu-id="3924c-126">Office 365 E5</span></span>
- <span data-ttu-id="3924c-127">Office 365 Advanced Compliance</span><span class="sxs-lookup"><span data-stu-id="3924c-127">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="3924c-128">Microsoft 365, защита информации и соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="3924c-128">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="3924c-129">Дополнительные сведения см. [](https://products.office.com/business/security-and-compliance/compliance-solutions)</span><span class="sxs-lookup"><span data-stu-id="3924c-129">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

<span data-ttu-id="3924c-130">Чтобы [определить или изменить политики барьера данных](information-barriers-policies.md), необходимо назначить одну из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="3924c-130">To [define or edit information barrier policies](information-barriers-policies.md), you must be assigned one of the following roles:</span></span>

- <span data-ttu-id="3924c-131">Глобальный администратор Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3924c-131">Microsoft 365 global administrator</span></span>
- <span data-ttu-id="3924c-132">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="3924c-132">Office 365 global administrator</span></span>
- <span data-ttu-id="3924c-133">Администратор соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="3924c-133">Compliance administrator</span></span>
- <span data-ttu-id="3924c-134">Администратор барьеров информации</span><span class="sxs-lookup"><span data-stu-id="3924c-134">Information barriers administrator</span></span>

<span data-ttu-id="3924c-135">Вы должны быть знакомы с командлетами PowerShell, чтобы определить, проверить или изменить политики барьера данных.</span><span class="sxs-lookup"><span data-stu-id="3924c-135">You must be familiar with PowerShell cmdlets in order to define, validate, or edit information barrier policies.</span></span> <span data-ttu-id="3924c-136">Несмотря на то, что мы предоставляем несколько примеров командлетов PowerShell в [инструкции](information-barriers-policies.md), для Организации необходимо знать дополнительные сведения, например параметры.</span><span class="sxs-lookup"><span data-stu-id="3924c-136">Although we provide several examples of PowerShell cmdlets in the [how-to information](information-barriers-policies.md), you'll need to know additional details, such as parameters, for your organization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3924c-137">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="3924c-137">Next steps</span></span>

- [<span data-ttu-id="3924c-138">Дополнительные сведения об барьерах информации в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3924c-138">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [<span data-ttu-id="3924c-139">Просмотр атрибутов, которые можно использовать для политик барьера информации</span><span class="sxs-lookup"><span data-stu-id="3924c-139">See the attributes that can be used for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="3924c-140">Определение политик для барьеров информации</span><span class="sxs-lookup"><span data-stu-id="3924c-140">Define policies for information barriers</span></span>](information-barriers-policies.md) 

