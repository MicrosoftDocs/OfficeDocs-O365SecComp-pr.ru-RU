---
title: Настройка новых возможностей шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/12/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Новые возможности шифрования сообщений Office 365, основанные на Azure Information Protection, ваша организация может использовать защищенную электронную связь с пользователями внутри и за пределами Организации. Новые возможности OME работают с другими организациями Office 365, Outlook.com, Gmail и другими почтовыми службами.
ms.openlocfilehash: ea8756d08b1c172c433d6cd8ad1752c4c7ad64e9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260757"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="cd33f-104">Настройка новых возможностей шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="cd33f-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="cd33f-105">Новые возможности шифрования сообщений Office 365 (OME) позволяют организациям обмениваться защищенной электронной почтой с любыми устройствами.</span><span class="sxs-lookup"><span data-stu-id="cd33f-105">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device.</span></span> <span data-ttu-id="cd33f-106">Пользователи могут обмениваться защищенными сообщениями с другими организациями Office 365, а также клиентами, не являющимися клиентами Office 365, с помощью Outlook.com, Gmail и других почтовых служб.</span><span class="sxs-lookup"><span data-stu-id="cd33f-106">Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>

||
|:-----|
|<span data-ttu-id="cd33f-107">Эта статья входит в набор статей, посвященных шифрованию сообщений Office 365.</span><span class="sxs-lookup"><span data-stu-id="cd33f-107">This article is part of a larger series of articles about Office 365 Message Encryption.</span></span> <span data-ttu-id="cd33f-108">Эта статья предназначена для администраторов и ИТ-специалистов.</span><span class="sxs-lookup"><span data-stu-id="cd33f-108">This article is intended for administrators and IT Pros.</span></span> <span data-ttu-id="cd33f-109">Если вы просто ищете сведения о том, как отправлять или получать зашифрованные сообщения, ознакомьтесь со статьей, посвященной [шифрованИю сообщений Office 365 (OME)](ome.md) , и выберите статью, которая наилучшим образом соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="cd33f-109">If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

<span data-ttu-id="cd33f-110">Выполните приведенные ниже действия, чтобы убедиться, что новые возможности OME доступны в организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="cd33f-110">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 organization.</span></span>

## <a name="verify-that-azure-rights-management-is-active"></a><span data-ttu-id="cd33f-111">Проверка активности Azure Rights Management</span><span class="sxs-lookup"><span data-stu-id="cd33f-111">Verify that Azure Rights Management is active</span></span>

<span data-ttu-id="cd33f-112">Новые возможности OME используют функции защиты в Azure [Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), технология, используемая службой [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) для защиты сообщений электронной почты и документов с помощью средств шифрования и управления доступом.</span><span class="sxs-lookup"><span data-stu-id="cd33f-112">The new OME capabilities leverage the protection features in [Azure Rights Management Services (Azure RMS)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) to protect emails and documents via encryption and access controls.</span></span>

<span data-ttu-id="cd33f-113">Единственным необходимым условием для использования новых возможностей OME является то, что служба [управления правами Azure](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) должна быть активирована в клиенте Организации.</span><span class="sxs-lookup"><span data-stu-id="cd33f-113">The only prerequisite for using the new OME capabilities is that [Azure Rights Management](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your organization's tenant.</span></span> <span data-ttu-id="cd33f-114">Если это так, Office 365 автоматически активирует новые возможности OME, и вам не нужно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="cd33f-114">If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span>

<span data-ttu-id="cd33f-115">Служба Azure RMS также автоматически активируется для большинства соответствующих планов, поэтому вам, скорее всего, не придется ничего делать.</span><span class="sxs-lookup"><span data-stu-id="cd33f-115">Azure RMS is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either.</span></span> <span data-ttu-id="cd33f-116">Дополнительную информацию можно узнать в статье [Активация управления правами Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .</span><span class="sxs-lookup"><span data-stu-id="cd33f-116">See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more information.</span></span>

>[!IMPORTANT]
><span data-ttu-id="cd33f-117">Если вы используете службу управления правами Active Directory (AD RMS) с Exchange Online, вам необходимо [выполнить миграцию в Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) , прежде чем вы сможете использовать новые возможности OME.</span><span class="sxs-lookup"><span data-stu-id="cd33f-117">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities.</span></span> <span data-ttu-id="cd33f-118">OME несовместим с AD RMS.</span><span class="sxs-lookup"><span data-stu-id="cd33f-118">OME is not compatible with AD RMS.</span></span>  

<span data-ttu-id="cd33f-119">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="cd33f-119">For more information, see:</span></span>

- <span data-ttu-id="cd33f-120">[Какие подписки необходимы для использования новых возможностей OME?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) чтобы проверить, включается ли план подписки в Azure Information Protection (в том числе функциональность Azure RMS).</span><span class="sxs-lookup"><span data-stu-id="cd33f-120">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes Azure RMS functionality).</span></span>
- <span data-ttu-id="cd33f-121">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) для получения сведений о приобретении подлежащей подписке.</span><span class="sxs-lookup"><span data-stu-id="cd33f-121">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-azure-rights-management"></a><span data-ttu-id="cd33f-122">Активация службы управления правами Azure вручную</span><span class="sxs-lookup"><span data-stu-id="cd33f-122">Manually activating Azure Rights Management</span></span>

<span data-ttu-id="cd33f-123">Если вы отключили Azure RMS или она не была автоматически активирована по какой либо причине, ее можно активировать вручную в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="cd33f-123">If you disabled Azure RMS, or if it was not automatically activated for any reason, you can activate it manually in the:</span></span>

- <span data-ttu-id="cd33f-124">**Центр администрирования office 365**: в этой статье приведены инструкции по [активации Azure Rights Management из центра администрирования Office 365](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) .</span><span class="sxs-lookup"><span data-stu-id="cd33f-124">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions.</span></span>
- <span data-ttu-id="cd33f-125">**Портал Azure**: Узнайте [, как активировать управление правами Azure на портале Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) для получения инструкций.</span><span class="sxs-lookup"><span data-stu-id="cd33f-125">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span>

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="cd33f-126">Настройка управления ключом клиента Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="cd33f-126">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="cd33f-127">Этот шаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="cd33f-127">This is an optional step.</span></span> <span data-ttu-id="cd33f-128">Предоставление корпорации Майкрософт возможности управлять корневым ключом для Azure Information Protection является параметром по умолчанию и рекомендуемой практикой для большинства клиентов Office 365.</span><span class="sxs-lookup"><span data-stu-id="cd33f-128">Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants.</span></span> <span data-ttu-id="cd33f-129">В этом случае вам не нужно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="cd33f-129">If this is the case, you don't need to do anything.</span></span>

<span data-ttu-id="cd33f-130">Существует множество причин, например требований соответствия требованиям, которые могут быть готовы к созданию и управлению собственным корневым ключом (также известным как перенесите свой ключ (БЙОК)).</span><span class="sxs-lookup"><span data-stu-id="cd33f-130">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)).</span></span> <span data-ttu-id="cd33f-131">В этом случае рекомендуется выполнить необходимые действия перед настройкой новых возможностей OME.</span><span class="sxs-lookup"><span data-stu-id="cd33f-131">If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities.</span></span> <span data-ttu-id="cd33f-132">Чтобы узнать больше [, ознакомьтесь с разделом Планирование и реализация клиентского ключа клиента для Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .</span><span class="sxs-lookup"><span data-stu-id="cd33f-132">See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span>

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="cd33f-133">Проверка новой конфигурации OME в Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="cd33f-133">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="cd33f-134">Вы можете убедиться, что клиент Office 365 правильно настроен для использования новых возможностей OME в [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="cd33f-134">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="cd33f-135">[Подключитесь к Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) , используя учетную запись с разрешениями глобального администратора в клиенте Office 365.</span><span class="sxs-lookup"><span data-stu-id="cd33f-135">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="cd33f-136">Выполните командлет Get – IRMConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cd33f-136">Run the Get-IRMConfiguration cmdlet.</span></span>

     <span data-ttu-id="cd33f-137">Вы увидите значение $True для параметра Азурермсенаблед, которое указывает на то, что в клиенте настроен OME.</span><span class="sxs-lookup"><span data-stu-id="cd33f-137">You should see a value of $True for the AzureRMSEnabled parameter, which indicates that OME is configured in your tenant.</span></span> <span data-ttu-id="cd33f-138">Если это не так, используйте Set-IRMConfiguration, чтобы задать для Азурермсенаблед значение $True, чтобы включить OME.</span><span class="sxs-lookup"><span data-stu-id="cd33f-138">If it is not, use Set-IRMConfiguration to set the value of AzureRMSEnabled to $True to enable OME.</span></span>

3. <span data-ttu-id="cd33f-139">Запустите командлет Test-IRMConfiguration, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="cd33f-139">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="cd33f-140">**Пример**:</span><span class="sxs-lookup"><span data-stu-id="cd33f-140">**Example**:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - <span data-ttu-id="cd33f-141">Предоставление электронной почты отправителя необязательно, но заставляет систему выполнять дополнительные проверки.</span><span class="sxs-lookup"><span data-stu-id="cd33f-141">Providing a sender email is optional, but forces the system to perform additional checks.</span></span> <span data-ttu-id="cd33f-142">Используйте адрес электронной почты любого пользователя в клиенте Office 365.</span><span class="sxs-lookup"><span data-stu-id="cd33f-142">Use the email address of any user in your Office 365 tenant.</span></span>

     <span data-ttu-id="cd33f-143">Результаты должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cd33f-143">Your results should be similar to:</span></span>

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

   - <span data-ttu-id="cd33f-144">Имя вашей организации Office 365 заменит *contoso*.</span><span class="sxs-lookup"><span data-stu-id="cd33f-144">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="cd33f-145">Имена шаблонов по умолчанию могут отличаться от показанных выше.</span><span class="sxs-lookup"><span data-stu-id="cd33f-145">The default template names may be different from those displayed above.</span></span> <span data-ttu-id="cd33f-146">Дополнительную информацию можно узнать в статье [Настройка шаблонов для Azure Information Protection и управление ими](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .</span><span class="sxs-lookup"><span data-stu-id="cd33f-146">See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

4. <span data-ttu-id="cd33f-147">Запустите командлет reMove – PSSession, чтобы отключиться от службы управления правами.</span><span class="sxs-lookup"><span data-stu-id="cd33f-147">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="cd33f-148">Дальнейшие действия: определение правил для почтового процесса для использования новых возможностей OME</span><span class="sxs-lookup"><span data-stu-id="cd33f-148">Next steps: Define mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="cd33f-149">Если вы уже настроили правила обработки почты для шифрования электронной почты в организации Office 365, необходимо обновить существующие правила, чтобы использовать новые возможности OME.</span><span class="sxs-lookup"><span data-stu-id="cd33f-149">If there are previously configured mail flow rules to encrypt email in your Office 365 organization, you need to update the existing rules to use the new OME capabilities.</span></span> <span data-ttu-id="cd33f-150">Для новых развертываний необходимо создать новые правила для процесса обработки почты.</span><span class="sxs-lookup"><span data-stu-id="cd33f-150">For new deployments, you need to create new mail flow rules.</span></span>

>[!IMPORTANT]
><span data-ttu-id="cd33f-151">Если вы не обновите существующие правила для почтовых ящиков, ваши пользователи продолжат получать зашифрованную почту, использующую предыдущий формат вложений HTML, а не новый прямой интерфейс OME.</span><span class="sxs-lookup"><span data-stu-id="cd33f-151">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new seamless OME experience.</span></span>

<span data-ttu-id="cd33f-152">Правила для почтового процесса определяют, при каких условиях сообщения электронной почты должны шифроваться, а также условия удаления этого шифрования.</span><span class="sxs-lookup"><span data-stu-id="cd33f-152">Mail flow rules determine under what conditions email messages should be encrypted, as well as conditions for removing that encryption.</span></span> <span data-ttu-id="cd33f-153">Когда вы настраиваете действие для правила, все сообщения, которые удовлетворяют условиям правила, шифруются при отправке.</span><span class="sxs-lookup"><span data-stu-id="cd33f-153">When you set an action for a rule, any messages that match the rule conditions are encrypted when they're sent.</span></span>
  
<span data-ttu-id="cd33f-154">Действия по созданию правил для обработки почты для OME приведены [в разделе Определение правил для почтового процесса для шифрования сообщений электронной почты в Office 365](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="cd33f-154">For steps on creating mail flow rules for OME, see [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).</span></span>

<span data-ttu-id="cd33f-155">Чтобы обновить существующие правила для использования новых возможностей OME:</span><span class="sxs-lookup"><span data-stu-id="cd33f-155">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="cd33f-156">В центре администрирования Office 365 откройте центр **администрирования _Гт_ Exchange**.</span><span class="sxs-lookup"><span data-stu-id="cd33f-156">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>
2. <span data-ttu-id="cd33f-157">В центре администрирования Exchange перейдите к разделу **_Гт_ Mail Flow Rules**.</span><span class="sxs-lookup"><span data-stu-id="cd33f-157">In the Exchange admin center, go to **Mail flow > Rules**.</span></span>
3. <span data-ttu-id="cd33f-158">Для каждого правила **выполните следующие**действия:</span><span class="sxs-lookup"><span data-stu-id="cd33f-158">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="cd33f-159">Выберите **изменить безопасность сообщения**.</span><span class="sxs-lookup"><span data-stu-id="cd33f-159">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="cd33f-160">Выберите **применить шифрование сообщений Office 365 и защиту прав**.</span><span class="sxs-lookup"><span data-stu-id="cd33f-160">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="cd33f-161">Выберите шаблон RMS в списке.</span><span class="sxs-lookup"><span data-stu-id="cd33f-161">Select an RMS template from the list.</span></span>
    - <span data-ttu-id="cd33f-162">Нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="cd33f-162">Select **Save**.</span></span>
    - <span data-ttu-id="cd33f-163">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="cd33f-163">Select **OK**.</span></span>
