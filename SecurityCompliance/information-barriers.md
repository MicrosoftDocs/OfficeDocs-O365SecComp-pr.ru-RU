---
title: Общие сведения о барьерах
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: None
description: Используйте информационные барьеры, чтобы обеспечить соответствие требованиям, используя Microsoft Teams в вашей организации.
ms.openlocfilehash: e52a62ca0b80aed577be1978b81c8a01ac2371b9
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668332"
---
# <a name="information-barriers-preview"></a><span data-ttu-id="f8a5f-103">Препятствия для информационных заданных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="f8a5f-103">Information barriers (Preview)</span></span>

<span data-ttu-id="f8a5f-104">Облачные службы Майкрософт включают мощные возможности общения и совместной работы.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-104">Microsoft cloud services include powerful communication and collaboration capabilities.</span></span> <span data-ttu-id="f8a5f-105">Однако предположим, что вы хотите ограничить связь между двумя группами, чтобы избежать конфликта интересов в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-105">But suppose that you want to restrict communications between two groups to avoid a conflict of interest from occurring in your organization.</span></span> <span data-ttu-id="f8a5f-106">Или, возможно, вы хотите ограничить связь между определенными пользователями в Организации, чтобы защитить внутреннюю информацию.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-106">Or, perhaps you want to restrict communications between certain people inside your organization in order to safeguard internal information.</span></span> <span data-ttu-id="f8a5f-107">Microsoft 365 обеспечивает взаимодействие и совместную работу между группами и организациями, поэтому существует ли способ ограничения взаимодействия между определенными группами пользователей, когда это необходимо?</span><span class="sxs-lookup"><span data-stu-id="f8a5f-107">Microsoft 365 enables communication and collaboration across groups and organizations, so is there a way to restrict communications among specific groups of users when necessary?</span></span> <span data-ttu-id="f8a5f-108">С помощью информационных барьеров вы можете!</span><span class="sxs-lookup"><span data-stu-id="f8a5f-108">With information barriers, you can!</span></span> 

<span data-ttu-id="f8a5f-109">Информационные барьеры теперь доступны в предварительной версии, начиная с Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-109">Information barriers are in preview now, beginning with Microsoft Teams.</span></span> <span data-ttu-id="f8a5f-110">Если эти функции доступны в вашей организации, администратор соответствия требованиям или администратору по управлению сведениями могут определять политики для разрешения или запрета связи между группами пользователей в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-110">When these features are available for your organization, a compliance administrator or information barriers administrator can define policies to allow or prevent communications between groups of users in Microsoft Teams.</span></span> <span data-ttu-id="f8a5f-111">Политики барьера информации могут использоваться в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="f8a5f-111">Information barrier policies can be used for situations like these:</span></span>

- <span data-ttu-id="f8a5f-112">День торговца не может вызвать кого-либо в группе маркетинга</span><span class="sxs-lookup"><span data-stu-id="f8a5f-112">A day trader cannot call someone on the marketing team</span></span>
- <span data-ttu-id="f8a5f-113">Сотрудники отдела финансов, работающие с конфиденциальной информацией о компании, не могут принимать звонки из определенных групп в своей организации.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-113">Finance personnel working on confidential company information cannot receive calls from certain groups within their organization</span></span>
- <span data-ttu-id="f8a5f-114">Внутренняя группа с коммерческими секретными материалами не может звонить или общаться с пользователями в определенных группах в Организации</span><span class="sxs-lookup"><span data-stu-id="f8a5f-114">An internal team with trade secret material cannot call or chat online with people in certain groups within their organization</span></span>
- <span data-ttu-id="f8a5f-115">Команда исследования может звонить или общаться через Интернет только с помощью команды разработчиков продуктов</span><span class="sxs-lookup"><span data-stu-id="f8a5f-115">A research team can only call or chat online with a product development team</span></span>

<span data-ttu-id="f8a5f-116">Для всех приведенных ниже примеров сценариев (и более) можно определить политики информационных барьеров, чтобы запретить или разрешить взаимодействие в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-116">For all of these example scenarios (and more), information barrier policies can be defined to prevent or allow communications in Microsoft Teams.</span></span> <span data-ttu-id="f8a5f-117">Такие политики могут препятствовать абонентам звонить или общаться, которые им не нужны, или разрешить пользователям общаться только с определенными группами в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-117">Such policies can prevent people from calling or chatting with those they shouldn't, or enable people to communicate only with specific groups in Microsoft Teams.</span></span> <span data-ttu-id="f8a5f-118">С действующими политиками для работы с информационными барьерами, когда пользователи, покрытые этими политиками, пытаются связаться с другими пользователями в Microsoft Teams, выполняются проверки, чтобы запретить (или разрешить) связь (как определено политиками барьера информации).</span><span class="sxs-lookup"><span data-stu-id="f8a5f-118">With information barrier policies in effect, whenever users who are covered by those policies attempt to communicate with others in Microsoft Teams, checks are done to prevent (or allow) communication (as defined by information barrier policies).</span></span> 

> [!NOTE]
> <span data-ttu-id="f8a5f-119">Информационные барьеры не будут применяться к сообщениям электронной почты или к общему доступу к файлам через SharePoint Online или OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-119">Information barriers will not apply to email communications or to file sharing through SharePoint Online or OneDrive.</span></span>

<span data-ttu-id="f8a5f-120">Политики для работы с информационными барьерами применяются к следующим типам действий связи:</span><span class="sxs-lookup"><span data-stu-id="f8a5f-120">Information barrier policies apply to the following kinds of communication activities:</span></span>

- <span data-ttu-id="f8a5f-121">Поиск пользователя</span><span class="sxs-lookup"><span data-stu-id="f8a5f-121">Searching for user</span></span>
- <span data-ttu-id="f8a5f-122">Добавление участника в группу</span><span class="sxs-lookup"><span data-stu-id="f8a5f-122">Adding a member to a team</span></span>
- <span data-ttu-id="f8a5f-123">Начало сеанса беседы с пользователем</span><span class="sxs-lookup"><span data-stu-id="f8a5f-123">Starting a chat session with someone</span></span>
- <span data-ttu-id="f8a5f-124">Начало сеанса групповой беседы</span><span class="sxs-lookup"><span data-stu-id="f8a5f-124">Starting a group chat</span></span> 
- <span data-ttu-id="f8a5f-125">Приглашение пользователя присоединиться к собранию</span><span class="sxs-lookup"><span data-stu-id="f8a5f-125">Inviting someone to join a meeting</span></span>
- <span data-ttu-id="f8a5f-126">Совместное использование экрана</span><span class="sxs-lookup"><span data-stu-id="f8a5f-126">Sharing a screen</span></span> 
- <span data-ttu-id="f8a5f-127">Размещение звонка</span><span class="sxs-lookup"><span data-stu-id="f8a5f-127">Placing a call</span></span>

<span data-ttu-id="f8a5f-128">Если вовлеченные люди включены в политику барьера данных, предотвращающую действие, они не смогут продолжить работу.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-128">If the people involved are included in an information barrier policy that prevents the activity, they will not be able to proceed.</span></span> <span data-ttu-id="f8a5f-129">Чтобы узнать больше о пользовательском интерфейсе с помощью барьеров информации, ознакомьтесь с разделом [Information барьеры в Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span><span class="sxs-lookup"><span data-stu-id="f8a5f-129">To learn more about the user experience with information barriers, see [information barriers in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams).</span></span>

<span data-ttu-id="f8a5f-130">В настоящее время политики информационных барьеров определяются и управляются в Office 365 с помощью командлетов PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-130">Currently, information barrier policies are defined and managed in Office 365 by using PowerShell cmdlets.</span></span> <span data-ttu-id="f8a5f-131">Это обычно делается администратором соответствия требованиям или глобальным администратором, а также требует знакомства с командлетами PowerShell (и параметрами).</span><span class="sxs-lookup"><span data-stu-id="f8a5f-131">This is typically done by a compliance administrator or a global administrator, and requires familiarity with PowerShell cmdlets (and parameters).</span></span> <span data-ttu-id="f8a5f-132">Для получения дополнительных сведений обратитесь к статье [PowerShell (для определения препятствий)](information-barriers-policies.md#powershell).</span><span class="sxs-lookup"><span data-stu-id="f8a5f-132">To learn more, see [PowerShell (for defining information barriers)](information-barriers-policies.md#powershell).</span></span>

## <a name="required-licenses-and-permissions"></a><span data-ttu-id="f8a5f-133">Необходимые лицензии и разрешения</span><span class="sxs-lookup"><span data-stu-id="f8a5f-133">Required licenses and permissions</span></span>

<span data-ttu-id="f8a5f-134">В **настоящее время функция "барьер данных" находится в частном предварительной версии**.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-134">**Currently, the information barrier feature is in private preview**.</span></span> <span data-ttu-id="f8a5f-135">Если эти функции, как правило, доступны, они будут включены в подписки, например:</span><span class="sxs-lookup"><span data-stu-id="f8a5f-135">When these features are generally available, they'll be included in subscriptions, such as:</span></span>

- <span data-ttu-id="f8a5f-136">Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="f8a5f-136">Microsoft 365 E5</span></span>
- <span data-ttu-id="f8a5f-137">Office 365</span><span class="sxs-lookup"><span data-stu-id="f8a5f-137">Office 365 E5</span></span>
- <span data-ttu-id="f8a5f-138">Office 365 Advanced Compliance</span><span class="sxs-lookup"><span data-stu-id="f8a5f-138">Office 365 Advanced Compliance</span></span>
- <span data-ttu-id="f8a5f-139">Microsoft 365, защита информации и соответствие требованиям</span><span class="sxs-lookup"><span data-stu-id="f8a5f-139">Microsoft 365 E5 Information Protection and Compliance</span></span>

<span data-ttu-id="f8a5f-140">Дополнительные сведения см. [](https://products.office.com/business/security-and-compliance/compliance-solutions)</span><span class="sxs-lookup"><span data-stu-id="f8a5f-140">For more details, see [Compliance Solutions](https://products.office.com/business/security-and-compliance/compliance-solutions).</span></span>

<span data-ttu-id="f8a5f-141">Чтобы [определить или изменить политики барьера данных](information-barriers-policies.md), необходимо назначить одну из следующих ролей:</span><span class="sxs-lookup"><span data-stu-id="f8a5f-141">To [define or edit information barrier policies](information-barriers-policies.md), you must be assigned one of the following roles:</span></span>

- <span data-ttu-id="f8a5f-142">Глобальный администратор Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f8a5f-142">Microsoft 365 global administrator</span></span>
- <span data-ttu-id="f8a5f-143">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="f8a5f-143">Office 365 global administrator</span></span>
- <span data-ttu-id="f8a5f-144">Администратор соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f8a5f-144">Compliance administrator</span></span>
- <span data-ttu-id="f8a5f-145">Администратор барьеров информации</span><span class="sxs-lookup"><span data-stu-id="f8a5f-145">Information barriers administrator</span></span>

<span data-ttu-id="f8a5f-146">Вы должны быть знакомы с командлетами PowerShell, чтобы определить, проверить или изменить политики барьера данных.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-146">You must be familiar with PowerShell cmdlets in order to define, validate, or edit information barrier policies.</span></span> <span data-ttu-id="f8a5f-147">Несмотря на то, что мы предоставляем несколько примеров командлетов PowerShell в [инструкции](information-barriers-policies.md), для Организации необходимо знать дополнительные сведения, например параметры.</span><span class="sxs-lookup"><span data-stu-id="f8a5f-147">Although we provide several examples of PowerShell cmdlets in the [how-to information](information-barriers-policies.md), you'll need to know additional details, such as parameters, for your organization.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f8a5f-148">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="f8a5f-148">Next steps</span></span>

- [<span data-ttu-id="f8a5f-149">Дополнительные сведения об барьерах информации в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f8a5f-149">Learn more about information barriers in Microsoft Teams</span></span>](https://docs.microsoft.com/MicrosoftTeams/information-barriers-in-teams)
- [<span data-ttu-id="f8a5f-150">Просмотр атрибутов, которые можно использовать для политик барьера информации</span><span class="sxs-lookup"><span data-stu-id="f8a5f-150">See the attributes that can be used for information barrier policies</span></span>](information-barriers-attributes.md)
- [<span data-ttu-id="f8a5f-151">Определение политик для барьеров информации</span><span class="sxs-lookup"><span data-stu-id="f8a5f-151">Define policies for information barriers</span></span>](information-barriers-policies.md) 

