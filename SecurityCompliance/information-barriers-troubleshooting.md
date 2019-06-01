---
title: Устранение неполадок, связанных с информацией
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
description: Используйте эту статью в качестве руководства по устранению проблем со сведениями.
ms.openlocfilehash: b37585469ec8bb299b7976f8a330f4c6b29e3f95
ms.sourcegitcommit: 4fedeb06a6e7796096fc6279cfb091c7b89d484d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/31/2019
ms.locfileid: "34668333"
---
# <a name="troubleshooting-information-barriers-preview"></a><span data-ttu-id="5e980-103">Препятствия информации об устранении неполадок (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="5e980-103">Troubleshooting information barriers (Preview)</span></span>

<span data-ttu-id="5e980-104">Информационные барьеры помогают Организации в соответствии с юридическими требованиями и отраслевыми нормативами.</span><span class="sxs-lookup"><span data-stu-id="5e980-104">Information barriers can help your organization remain compliant with legal requirements and industry regulations.</span></span> <span data-ttu-id="5e980-105">Например, с помощью информационных барьеров вы можете ограничить обмен данными между определенными группами пользователей, чтобы избежать конфликта интересов или других проблем.</span><span class="sxs-lookup"><span data-stu-id="5e980-105">For example, with information barriers, you can restrict communication between specific groups of users to avoid a conflict of interest or other issues.</span></span> <span data-ttu-id="5e980-106">Дополнительные сведения см. [](information-barriers.md)</span><span class="sxs-lookup"><span data-stu-id="5e980-106">To learn more, see [Information barriers (Preview)](information-barriers.md).</span></span>

<span data-ttu-id="5e980-107">В этой статье представлены рекомендации по получению ответов на вопросы и устранению проблем, которые могут возникать при работе с барьерами информации.</span><span class="sxs-lookup"><span data-stu-id="5e980-107">This article provides guidance you can use to get answers to questions or resolve issues that may arise with information barriers.</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="5e980-108">Перед началом работы...</span><span class="sxs-lookup"><span data-stu-id="5e980-108">Before you begin...</span></span>

<span data-ttu-id="5e980-109">Для выполнения задач, описанных в этой статье, необходимо назначить соответствующую роль, например один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="5e980-109">To perform the tasks described in this article, you must be assigned an appropriate role, such as one of the following:</span></span>
- <span data-ttu-id="5e980-110">Глобальный администратор Microsoft 365 корпоративный</span><span class="sxs-lookup"><span data-stu-id="5e980-110">Microsoft 365 Enterprise Global Administrator</span></span>
- <span data-ttu-id="5e980-111">Глобальный администратор Office 365</span><span class="sxs-lookup"><span data-stu-id="5e980-111">Office 365 Global Administrator</span></span>
- <span data-ttu-id="5e980-112">Администратор соответствия</span><span class="sxs-lookup"><span data-stu-id="5e980-112">Compliance Administrator</span></span>
- <span data-ttu-id="5e980-113">Управление соответствием требованиям (это новая роль)</span><span class="sxs-lookup"><span data-stu-id="5e980-113">IB Compliance Management (this is a new role!)</span></span>

<span data-ttu-id="5e980-114">Чтобы узнать больше о ролях и разрешениях, ознакомьтесь со статьей [разрешения в центре безопасности Office 365 & соответствия требованиям](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="5e980-114">To learn more about roles and permissions, see [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="5e980-115">Чтобы узнать больше о предварительных требованиях для барьеров информации, ознакомьтесь со статьей [Предварительные требования (для политик барьера информации)](information-barriers-policies.md#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="5e980-115">To learn more about prerequisites for information barriers, see [Prerequisites (for information barrier policies)](information-barriers-policies.md#prerequisites).</span></span>

<span data-ttu-id="5e980-116">Кроме того, необходимо [подключиться к PowerShell центра безопасности & центра соответствия требованиям Office 365](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="5e980-116">Also, make sure to [connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).</span></span>

## <a name="issue-people-are-unexpectedly-blocked-from-communicating-in-microsoft-teams"></a><span data-ttu-id="5e980-117">Вопрос: пользователи неожиданно блокировали связь в Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5e980-117">Issue: People are unexpectedly blocked from communicating in Microsoft Teams</span></span> 

<span data-ttu-id="5e980-118">В этом случае люди сообщают о непредвиденных проблемах связи в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5e980-118">In this case, people are reporting unexpected issues communicating in Microsoft Teams.</span></span> <span data-ttu-id="5e980-119">Примеры:</span><span class="sxs-lookup"><span data-stu-id="5e980-119">Examples:</span></span>
- <span data-ttu-id="5e980-120">Пользователь не может найти или подключиться к другому пользователю в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5e980-120">A user is unable to find or communicate with another user in Microsoft Teams.</span></span>
- <span data-ttu-id="5e980-121">Пользователь не может просматривать или выбирать другого пользователя в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5e980-121">A user cannot see or select another user in Microsoft Teams.</span></span>
- <span data-ttu-id="5e980-122">Пользователь может видеть, но не может отправлять сообщения другому пользователю в Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5e980-122">A user can see, but cannot send messages to, another user in Microsoft Teams.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="5e980-123">Действия</span><span class="sxs-lookup"><span data-stu-id="5e980-123">What to do</span></span>

1. <span data-ttu-id="5e980-124">Определите, повлияет ли политика информационного барьера на пользователей.</span><span class="sxs-lookup"><span data-stu-id="5e980-124">Determine whether the users are affected by an information barrier policy.</span></span> <span data-ttu-id="5e980-125">Для этого используйте командлет **Get – информатионбарриерреЦипиентстатус** с параметром Identity.</span><span class="sxs-lookup"><span data-stu-id="5e980-125">To do this, use the **Get-InformationBarrierRecipientStatus** cmdlet with the Identity parameter.</span></span> 

    <span data-ttu-id="5e980-126">Синтаксис`Get-InformationBarrierRecipientStatus -Identity`</span><span class="sxs-lookup"><span data-stu-id="5e980-126">The syntax is `Get-InformationBarrierRecipientStatus -Identity`</span></span>

    <span data-ttu-id="5e980-127">Можно использовать любое значение Identity, однозначно идентифицирующее каждого получателя, например имя, псевдоним, различающееся имя (DN), каноническое имя, адрес электронной почты или GUID.</span><span class="sxs-lookup"><span data-stu-id="5e980-127">You can use any identity value that uniquely identifies each recipient, such as Name, Alias, Distinguished name (DN), Canonical DN, Email address, or GUID.</span></span>

    <span data-ttu-id="5e980-128">Пример: `Get-InformationBarrierRecipientStatus -Identity meganb`</span><span class="sxs-lookup"><span data-stu-id="5e980-128">Example: `Get-InformationBarrierRecipientStatus -Identity meganb`</span></span>

    <span data-ttu-id="5e980-129">В этом примере используется псевдоним (*меганб*) для параметра Identity.</span><span class="sxs-lookup"><span data-stu-id="5e980-129">In this example, we are using an alias (*meganb*) for the Identity parameter.</span></span> <span data-ttu-id="5e980-130">Этот командлет возвращает сведения, указывающие на то, затрагивает ли пользователь политику барьера информации.</span><span class="sxs-lookup"><span data-stu-id="5e980-130">This cmdlet will return information that indicates whether the user is affected by an information barrier policy.</span></span> <span data-ttu-id="5e980-131">(Искать \* Ексополициид: \<GUID>.)</span><span class="sxs-lookup"><span data-stu-id="5e980-131">(Look for \*ExoPolicyId: \<GUID>.)</span></span>

    <span data-ttu-id="5e980-132">Если пользователи не включены в политики барьера информации, обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="5e980-132">If the users are not included in information barrier policies, contact support.</span></span> <span data-ttu-id="5e980-133">В противном случае перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="5e980-133">Otherwise, proceed to the next step.</span></span>

2. <span data-ttu-id="5e980-134">Сведения о том, какие сегменты включены в политику барьера информации.</span><span class="sxs-lookup"><span data-stu-id="5e980-134">Find out which segments are included in an information barrier policy.</span></span> <span data-ttu-id="5e980-135">Для этого используйте `Get-InformationBarrierPolicy` командлет с параметром Identity.</span><span class="sxs-lookup"><span data-stu-id="5e980-135">To do this, use the `Get-InformationBarrierPolicy` cmdlet with the Identity parameter.</span></span> <span data-ttu-id="5e980-136">Используйте сведения, такие как идентификатор GUID политики (Ексополициид), полученный на предыдущем этапе, в качестве значения Identity.</span><span class="sxs-lookup"><span data-stu-id="5e980-136">Use details, such as the policy GUID (ExoPolicyId) you received during the previous step, as an identity value.</span></span>

    <span data-ttu-id="5e980-137">Пример: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span><span class="sxs-lookup"><span data-stu-id="5e980-137">Example: `Get-InformationBarrierPolicy -Identity b42c3d0f-49e9-4506-a0a5-bf2853b5df6f`</span></span>

    <span data-ttu-id="5e980-138">В этом примере мы получаем подробные сведения о политике барьера информации, которая имеет Ексополициид *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.</span><span class="sxs-lookup"><span data-stu-id="5e980-138">In this example, we are getting detailed information about the information barrier policy that has ExoPolicyId *b42c3d0f-49e9-4506-a0a5-bf2853b5df6f*.</span></span>
    
    <span data-ttu-id="5e980-139">После выполнения командлета в результатах найдите значения **ассигнедсегмент**, **сегментсалловед**и **сегментсблоккед** .</span><span class="sxs-lookup"><span data-stu-id="5e980-139">After you run the cmdlet, in the results, look for **AssignedSegment**, **SegmentsAllowed**, and **SegmentsBlocked** values.</span></span>

    <span data-ttu-id="5e980-140">Пример: после выполнения `Get-InformationBarrierPolicy` командлета в нашем списке результатов мы видели следующее:</span><span class="sxs-lookup"><span data-stu-id="5e980-140">Example: After running the `Get-InformationBarrierPolicy` cmdlet, we saw the following in our list of results:</span></span>

    ```powershell
        AssignedSegment      : Sales
        SegmentsAllowed      : {}
        SegmentsBlocked      : {Research}
    ```
    <span data-ttu-id="5e980-141">В этом случае мы видим, что политика информационного барьера влияет на пользователей, находящихся в сегментах продаж и исследований.</span><span class="sxs-lookup"><span data-stu-id="5e980-141">In this case, we can see that an information barrier policy affects people who are in the Sales and Research segments.</span></span> <span data-ttu-id="5e980-142">В этом случае людям из отдела продаж запрещено взаимодействовать с людьми в справочных материалах.</span><span class="sxs-lookup"><span data-stu-id="5e980-142">In this case, people in Sales are prevented from communicating with people in Research.</span></span> <span data-ttu-id="5e980-143">Если это правильно, то информационные барьеры работают должным образом.</span><span class="sxs-lookup"><span data-stu-id="5e980-143">If this seems correct, then information barriers are working as expected.</span></span> <span data-ttu-id="5e980-144">В противном случае перейдите к следующему шагу.</span><span class="sxs-lookup"><span data-stu-id="5e980-144">If not, proceed to the next step.</span></span>

4. <span data-ttu-id="5e980-145">Убедитесь, что сегменты определены правильно.</span><span class="sxs-lookup"><span data-stu-id="5e980-145">Make sure your segments are defined correctly.</span></span> <span data-ttu-id="5e980-146">Для этого используйте `Get-OrganizationSegment` командлет и просмотрите список результатов.</span><span class="sxs-lookup"><span data-stu-id="5e980-146">To do this, use the `Get-OrganizationSegment` cmdlet, and review the list of results.</span></span> 

    <span data-ttu-id="5e980-147">Чтобы просмотреть сведения об определенном сегменте, используйте `Get-OrganizationSegment` командлет с параметром Identity.</span><span class="sxs-lookup"><span data-stu-id="5e980-147">To view details for a specific segment, use the `Get-OrganizationSegment` cmdlet with an Identity parameter.</span></span> 

    <span data-ttu-id="5e980-148">Пример: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span><span class="sxs-lookup"><span data-stu-id="5e980-148">Example: `Get-OrganizationSegment -Identity c96e0837-c232-4a8a-841e-ef45787d8fcd`</span></span>

    <span data-ttu-id="5e980-149">В этом примере мы получаем сведения о сегменте с GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*.</span><span class="sxs-lookup"><span data-stu-id="5e980-149">In this example, we are getting information about the segment that has GUID *c96e0837-c232-4a8a-841e-ef45787d8fcd*.</span></span>

    <span data-ttu-id="5e980-150">Просмотрите сведения о сегменте.</span><span class="sxs-lookup"><span data-stu-id="5e980-150">Review the details for the segment.</span></span> <span data-ttu-id="5e980-151">При необходимости [измените сегмент](information-barriers-policies.md#edit-a-segment), а затем повторно используйте `Start-InformationBarrierPoliciesApplication` командлет.</span><span class="sxs-lookup"><span data-stu-id="5e980-151">If necessary, [edit a segment](information-barriers-policies.md#edit-a-segment), and then re-use the `Start-InformationBarrierPoliciesApplication` cmdlet.</span></span>

    <span data-ttu-id="5e980-152">Если у вас по-прежнему возникают проблемы с политикой барьера информации, обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="5e980-152">If you are still having issues with your information barrier policy, contact support.</span></span>
    
## <a name="issue-the-information-barrier-application-process-is-taking-too-long"></a><span data-ttu-id="5e980-153">Вопрос: процесс Application барьера занимает слишком много времени</span><span class="sxs-lookup"><span data-stu-id="5e980-153">Issue: The information barrier application process is taking too long</span></span>

<span data-ttu-id="5e980-154">После выполнения командлета **Start-информатионбарриерполиЦиесаппликатион** процесс занимает очень много времени.</span><span class="sxs-lookup"><span data-stu-id="5e980-154">After running the **Start-InformationBarrierPoliciesApplication** cmdlet, the process is taking a really long time to finish.</span></span>

### <a name="what-to-do"></a><span data-ttu-id="5e980-155">Действия</span><span class="sxs-lookup"><span data-stu-id="5e980-155">What to do</span></span>

1. <span data-ttu-id="5e980-156">Имейте в виду, что при запуске командлета приложения политики политики информационных барьеров применяются (или удаляются), пользователь по пользователям для всех учетных записей в Организации.</span><span class="sxs-lookup"><span data-stu-id="5e980-156">Keep in mind that when you run the policy application cmdlet, information barrier policies are being applied (or removed), user by user, for all accounts in your organization.</span></span> <span data-ttu-id="5e980-157">Если у вас много пользователей, обработка займет некоторое время.</span><span class="sxs-lookup"><span data-stu-id="5e980-157">If you have a lot of users, it will take a while to process.</span></span> <span data-ttu-id="5e980-158">(Как правило, для обработки 5 000 учетных записей пользователей требуется около часа.)</span><span class="sxs-lookup"><span data-stu-id="5e980-158">(As a general guideline, it takes about an hour to process 5,000 user accounts.)</span></span> 

2. <span data-ttu-id="5e980-159">Используйте командлет **Get – информатионбарриерполиЦиесаппликатионстатус** для проверки состояния.</span><span class="sxs-lookup"><span data-stu-id="5e980-159">Use the **Get-InformationBarrierPoliciesApplicationStatus** cmdlet to verify status.</span></span>

    <span data-ttu-id="5e980-160">Инструкции`Get-InformationBarrierPoliciesApplicationStatus`</span><span class="sxs-lookup"><span data-stu-id="5e980-160">Syntax: `Get-InformationBarrierPoliciesApplicationStatus`</span></span>

    <span data-ttu-id="5e980-161">Чтобы отобразить состояние всех приложений политики для работы с информационными барьерами, используйте`Get-InformationBarrierPoliciesApplicationStatus -All $true`</span><span class="sxs-lookup"><span data-stu-id="5e980-161">To display status for all information barrier policy applications, use `Get-InformationBarrierPoliciesApplicationStatus -All $true`</span></span>

    <span data-ttu-id="5e980-162">При этом будут отображены сведения о том, завершено ли выполнение приложения политики, оно завершилось сбоем или находится в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="5e980-162">This will display information about whether policy application completed, failed, or is in progress..</span></span>

3. <span data-ttu-id="5e980-163">В зависимости от результатов действия 2 выполните одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="5e980-163">Depending on the results of step 2, take one of the following steps:</span></span>

    - <span data-ttu-id="5e980-164">Если приложение не запущено и прошло более 45 минут после запуска командлета **Start – информатионбарриерполиЦиесаппликатион** , просмотрите журнал аудита, чтобы проверить наличие ошибок в определениях политик, или по другой причине приложение не запущено.</span><span class="sxs-lookup"><span data-stu-id="5e980-164">If the application has not started, and it has been more than 45 minutes since the **Start-InformationBarrierPoliciesApplication** cmdlet has been run, review your audit log to see if there are any errors in policy definitions, or some other reason why the application has not started.</span></span>

    - <span data-ttu-id="5e980-165">Если произошел сбой приложения, изучите сегменты и политики.</span><span class="sxs-lookup"><span data-stu-id="5e980-165">If the application has failed, review your segments and policies.</span></span> <span data-ttu-id="5e980-166">При необходимости [измените сегменты](information-barriers-policies.md#edit-a-segment) и/или [измените политики](information-barriers-policies.md#edit-a-policy), а затем снова запустите командлет **Start-информатионбарриерполиЦиесаппликатион** .</span><span class="sxs-lookup"><span data-stu-id="5e980-166">If necessary, [edit segments](information-barriers-policies.md#edit-a-segment) and/or [edit policies](information-barriers-policies.md#edit-a-policy), and then run the **Start-InformationBarrierPoliciesApplication** cmdlet again.</span></span>

    - <span data-ttu-id="5e980-167">Если приложение все еще выполняется, дождитесь его завершения.</span><span class="sxs-lookup"><span data-stu-id="5e980-167">If the application is still in progress, allow more time for it to complete.</span></span> <span data-ttu-id="5e980-168">Если оно было несколько дней, обратитесь в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="5e980-168">If it has been several days, contact support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e980-169">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5e980-169">Related topics</span></span>

[<span data-ttu-id="5e980-170">Определение политик для барьеров информации в Microsoft Teams (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="5e980-170">Define policies for information barriers in Microsoft Teams (Preview)</span></span>](information-barriers-policies.md)

[<span data-ttu-id="5e980-171">Препятствия для информационных заданных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="5e980-171">Information barriers (Preview)</span></span>](information-barriers.md)



