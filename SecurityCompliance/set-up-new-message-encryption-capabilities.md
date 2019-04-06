---
title: Настройка новых возможностей шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Новые возможности шифрования сообщений Office 365, основанные на Azure Information Protection, ваша организация может использовать защищенную электронную связь с пользователями внутри и за пределами Организации. Новые возможности OME работают с другими организациями Office 365, Outlook.com, Gmail и другими почтовыми службами.
ms.openlocfilehash: fd237e537aa1ff961d2d975b3b30f4a51744ba7c
ms.sourcegitcommit: e24f70699021c4f4ba56508ad0afb6f65010c357
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2019
ms.locfileid: "31479655"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a><span data-ttu-id="e5ac5-104">Настройка новых возможностей шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="e5ac5-104">Set up new Office 365 Message Encryption capabilities</span></span>

<span data-ttu-id="e5ac5-105">Новые возможности шифрования сообщений Office 365 (OME) позволяют организациям обмениваться защищенной электронной почтой с любыми устройствами.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-105">The new Office 365 Message Encryption (OME) capabilities allow organizations to share protected email with anyone on any device.</span></span> <span data-ttu-id="e5ac5-106">Пользователи могут обмениваться защищенными сообщениями с другими организациями Office 365, а также клиентами, не являющимися клиентами Office 365, с помощью Outlook.com, Gmail и других почтовых служб.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-106">Users can exchange protected messages with other Office 365 organizations, as well as non-Office 365 customers using Outlook.com, Gmail, and other email services.</span></span>


>[!NOTE]
><span data-ttu-id="e5ac5-107">Эта статья предназначена для администраторов и ИТ-специалистов.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-107">This article is intended for administrators and IT professionals.</span></span> <span data-ttu-id="e5ac5-108">Если вы являетесь конечным пользователем, просмотрите список статей в статье [Шифрование сообщений Office 365 (OME)](ome.md) для соответствующих решений.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-108">If you're an end-user, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) for appropriate solutions.</span></span>

<span data-ttu-id="e5ac5-109">Выполните приведенные ниже действия, чтобы убедиться, что новые возможности OME доступны в клиенте Office 365.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-109">Follow the steps below to ensure that the New OME capabilities are available in your Office 365 tenant.</span></span>

## <a name="verify-azure-rights-management-arm-is-active"></a><span data-ttu-id="e5ac5-110">Проверка активности Azure Rights Management (ARM)</span><span class="sxs-lookup"><span data-stu-id="e5ac5-110">Verify Azure Rights Management (ARM) is active</span></span>

>[!NOTE]
><span data-ttu-id="e5ac5-111">Новые возможности OME используют функции защиты в [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), технологии, используемой службой [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).</span><span class="sxs-lookup"><span data-stu-id="e5ac5-111">The new OME capabilities leverage the protection features in [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), the technology used by [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).</span></span>

<span data-ttu-id="e5ac5-112">Единственным необходимым условием для использования новых возможностей OME является то, что служба [управления правами Azure (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) должна быть активирована в клиенте Office 365.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-112">The only prerequisite for using the new OME capabilities is that [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) must be activated in your Office 365 tenant.</span></span> <span data-ttu-id="e5ac5-113">Если это так, Office 365 автоматически активирует новые возможности OME, и вам не нужно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-113">If it is, Office 365 activates the new OME capabilities automatically and you don't need to do anything.</span></span>

<span data-ttu-id="e5ac5-114">ARM также активизируется автоматически для большинства соответствующих планов, поэтому вам, скорее всего, не придется ничего делать.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-114">ARM is also activated automatically for most eligible plans, so you probably don't have to do anything in this regard either.</span></span> <span data-ttu-id="e5ac5-115">Дополнительную поддержку вы найдете в статье [Активация управления правами Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .</span><span class="sxs-lookup"><span data-stu-id="e5ac5-115">See [Activating Azure Rights Management](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) for more.</span></span>

>[!IMPORTANT]
><span data-ttu-id="e5ac5-116">Если вы используете службу управления правами Active Directory (AD RMS) с Exchange Online, вам необходимо [выполнить миграцию в Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) , прежде чем вы сможете использовать новые возможности OME.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-116">If you use Active Directory Rights Management service (AD RMS) with Exchange Online, you need to [migrate to Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) before you can use the new OME capabilities.</span></span> <span data-ttu-id="e5ac5-117">Служба AD RMS несовместима с ARM.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-117">AD RMS is not compatible with ARM.</span></span>  

<span data-ttu-id="e5ac5-118">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-118">For more, see:</span></span>

- <span data-ttu-id="e5ac5-119">[Какие подписки необходимы для использования новых возможностей OME?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) чтобы проверить, включается ли план подписки в Azure Information Protection (включая ARM).</span><span class="sxs-lookup"><span data-stu-id="e5ac5-119">[What subscriptions do I need to use the new OME capabilities?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) to check whether your subscription plan includes Azure Information Protection (which includes ARM).</span></span>
- <span data-ttu-id="e5ac5-120">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) для получения сведений о приобретении подлежащей подписке.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-120">[Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) for information about purchasing an eligible subscription.</span></span>  

### <a name="manually-activating-arm"></a><span data-ttu-id="e5ac5-121">Ручная активация ARM</span><span class="sxs-lookup"><span data-stu-id="e5ac5-121">Manually activating ARM</span></span>

<span data-ttu-id="e5ac5-122">Если вы отключили ARM или не активировали его автоматически по какой бы то ни было причине, вы можете активировать его вручную в:</span><span class="sxs-lookup"><span data-stu-id="e5ac5-122">If you disabled ARM, or if it was not automatically activated for any reason, you can activated it manually in the:</span></span>

- <span data-ttu-id="e5ac5-123">**Центр администрирования office 365**: в этой статье приведены инструкции по [активации Azure Rights Management из центра администрирования Office 365](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) .</span><span class="sxs-lookup"><span data-stu-id="e5ac5-123">**Office 365 admin center**: See [How to activate Azure Rights Management from the Office 365 admin center](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) for instructions.</span></span>
- <span data-ttu-id="e5ac5-124">**Портал Azure**: Узнайте [, как активировать управление правами Azure на портале Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) для получения инструкций.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-124">**Azure portal**: See [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) for instructions.</span></span>

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a><span data-ttu-id="e5ac5-125">Настройка управления ключом клиента Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="e5ac5-125">Configure management of your Azure Information Protection tenant key</span></span>

<span data-ttu-id="e5ac5-126">Этот шаг является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-126">This is an optional step.</span></span> <span data-ttu-id="e5ac5-127">Предоставление корпорации Майкрософт возможности управлять корневым ключом для Azure Information Protection является параметром по умолчанию и рекомендуемой практикой для большинства клиентов Office 365.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-127">Allowing Microsoft to manage the root key for Azure Information Protection is the default setting and recommended best practice for most Office 365 tenants.</span></span> <span data-ttu-id="e5ac5-128">В этом случае вам не нужно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-128">If this is the case, you don't need to do anything.</span></span>

<span data-ttu-id="e5ac5-129">Существует множество причин, например требований соответствия требованиям, которые могут быть готовы к созданию и управлению собственным корневым ключом (также известным как перенесите свой ключ (БЙОК)).</span><span class="sxs-lookup"><span data-stu-id="e5ac5-129">There are many reasons, for example compliance requirements, that may necessitate you generating and managing your own root key (also known as bring your own key (BYOK)).</span></span> <span data-ttu-id="e5ac5-130">В этом случае рекомендуется выполнить необходимые действия перед настройкой новых возможностей OME.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-130">If this is the case, we recommend that you complete the required steps before setting up the new OME capabilities.</span></span> <span data-ttu-id="e5ac5-131">Чтобы узнать больше [, ознакомьтесь с разделом Планирование и реализация клиентского ключа клиента для Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .</span><span class="sxs-lookup"><span data-stu-id="e5ac5-131">See [Planning and implementing your Azure Information Protection tenant key](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) for more.</span></span>

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a><span data-ttu-id="e5ac5-132">Проверка новой конфигурации OME в Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5ac5-132">Verify new OME configuration in Exchange Online PowerShell</span></span>

<span data-ttu-id="e5ac5-133">Вы можете убедиться, что клиент Office 365 правильно настроен для использования новых возможностей OME в [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="e5ac5-133">You can verify that your Office 365 tenant is properly configured to use the new OME capabilities in [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).</span></span>
  
1. <span data-ttu-id="e5ac5-134">[Подключитесь к Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) , используя учетную запись с разрешениями глобального администратора в клиенте Office 365.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-134">[Connect to Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) using an account with global administrator permissions in your Office 365 tenant.</span></span>

2. <span data-ttu-id="e5ac5-135">Запустите командлет Test-IRMConfiguration, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="e5ac5-135">Run the Test-IRMConfiguration cmdlet using the following syntax:</span></span>

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   <span data-ttu-id="e5ac5-136">**Пример**:</span><span class="sxs-lookup"><span data-stu-id="e5ac5-136">**Example**:</span></span>

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - <span data-ttu-id="e5ac5-137">Предоставление электронной почты отправителя необязательно, но заставляет систему выполнять дополнительные проверки.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-137">Providing a sender email is optional, but forces the system to perform additional checks.</span></span> <span data-ttu-id="e5ac5-138">Используйте адрес электронной почты любого пользователя в клиенте Office 365.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-138">Use the email address of any user in your Office 365 tenant.</span></span> 

     <span data-ttu-id="e5ac5-139">Результаты должны выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e5ac5-139">Your results should be similar to:</span></span>

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

   - <span data-ttu-id="e5ac5-140">Имя вашей организации Office 365 заменит *contoso*.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-140">Your Office 365 organization name will replace *Contoso*.</span></span>

   - <span data-ttu-id="e5ac5-141">Имена шаблонов по умолчанию могут отличаться от показанных выше.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-141">The default template names may be different from those displayed above.</span></span> <span data-ttu-id="e5ac5-142">Дополнительную информацию можно узнать в статье [Настройка шаблонов для Azure Information Protection и управление ими](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .</span><span class="sxs-lookup"><span data-stu-id="e5ac5-142">See [Configuring and managing templates for Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) for more.</span></span>

3. <span data-ttu-id="e5ac5-143">Запустите командлет reMove – PSSession, чтобы отключиться от службы управления правами.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-143">Run the Remove-PSSession cmdlet to disconnect from the Rights Management service.</span></span>

     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a><span data-ttu-id="e5ac5-144">Обновление правил для почтового процесса для использования новых возможностей OME</span><span class="sxs-lookup"><span data-stu-id="e5ac5-144">Update mail flow rules to use new OME capabilities</span></span>

<span data-ttu-id="e5ac5-145">Если вы уже настроили правила обработки почты [для шифрования электронной почты](define-mail-flow-rules-to-encrypt-email.md) в клиенте Office 365, необходимо обновить существующие правила, чтобы использовать новые возможности OME.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-145">If there are previously configured [mail flow rules to encrypt email](define-mail-flow-rules-to-encrypt-email.md) in your Office 365 tenant, you need to update these existing rules to use the new OME capabilities.</span></span> <span data-ttu-id="e5ac5-146">Для новых развертываний это действие не требуется на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-146">For new deployments, this step is unnecessary at this stage.</span></span>   

>[!Note]
><span data-ttu-id="e5ac5-147">Правила для поЧтовых ящиков определяют условия, при которых сообщения электронной почты шифруются, а также, когда необходимо удалить шифрование.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-147">Mail flow rules define the conditions under which email messages are encrypted, and when encryption should be removed.</span></span> <span data-ttu-id="e5ac5-148">Дополнительные сведения: [Определение правил для почтового процесса для шифрования сообщений электронной почты в Office 365](define-mail-flow-rules-to-encrypt-email.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ac5-148">See [Define mail flow rules to encrypt email messages in Office 365](define-mail-flow-rules-to-encrypt-email.md) for more.</span></span>

<span data-ttu-id="e5ac5-149">Чтобы обновить существующие правила для использования новых возможностей OME:</span><span class="sxs-lookup"><span data-stu-id="e5ac5-149">To update existing rules to use the new OME capabilities:</span></span>

1. <span data-ttu-id="e5ac5-150">В центре администрирования Office 365 откройте центр **администрирования _Гт_ Exchange**.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-150">In the Office 365 admin center, go to **Admin centers > Exchange**.</span></span>

2. <span data-ttu-id="e5ac5-151">В центре администрирования Exchange перейдите к разделу **_Гт_ Mail Flow Rules**.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-151">In the Exchange admin center, go to **Mail flow > Rules**.</span></span> 
3. <span data-ttu-id="e5ac5-152">Для каждого правила **выполните следующие**действия:</span><span class="sxs-lookup"><span data-stu-id="e5ac5-152">For each rule, in **Do the following**:</span></span>
    - <span data-ttu-id="e5ac5-153">Выберите **изменить безопасность сообщения**.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-153">Select **Modify the message security**.</span></span>
    - <span data-ttu-id="e5ac5-154">Выберите **применить шифрование сообщений Office 365 и защиту прав**.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-154">Select **Apply Office 365 Message Encryption and rights protection**.</span></span>
    - <span data-ttu-id="e5ac5-155">Выберите шаблон RMS в списке.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-155">Select an RMS template from the list.</span></span>
    - <span data-ttu-id="e5ac5-156">Нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-156">Select **Save**.</span></span>
    - <span data-ttu-id="e5ac5-157">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-157">Select **OK**.</span></span>
  
>[!IMPORTANT]
><span data-ttu-id="e5ac5-158">Если вы не обновите существующие правила для почтовых ящиков, ваши пользователи продолжат получать зашифрованную почту, использующую предыдущий формат вложений HTML, а не новые возможности OME.</span><span class="sxs-lookup"><span data-stu-id="e5ac5-158">If you do not update existing mail flow rules, your users will continue to receive encrypted mail that uses the previous HTML attachment format, instead of the new OME capabilities.</span></span>
