---
title: Отзыв электронных писем, зашифрованных с помощью расширенного шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
description: Администратор Office 365 может отозвать определенные сообщения электронной почты, зашифрованные с помощью расширенного шифрования сообщений Office 365.
ms.openlocfilehash: 098ce50791152c8bbb4e4692d6fb85e4c2c7cb58
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156791"
---
# <a name="revoke-email-encrypted-by-office-365-advanced-message-encryption"></a><span data-ttu-id="c2afe-103">Отзыв электронных писем, зашифрованных с помощью расширенного шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="c2afe-103">Revoke email encrypted by Office 365 Advanced Message Encryption</span></span>

<span data-ttu-id="c2afe-104">Отзыв электронной почты предлагается как часть расширенного шифрования сообщения Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2afe-104">Email revocation is offered as part of Office 365 Advanced Message Encryption.</span></span> <span data-ttu-id="c2afe-105">Расширенное шифрование сообщений Office 365 в определенных подписках доступно на основе шифрования сообщений Office 365.</span><span class="sxs-lookup"><span data-stu-id="c2afe-105">Office 365 Advanced Message Encryption is available on top of Office 365 Message Encryption in certain subscriptions.</span></span> <span data-ttu-id="c2afe-106">Расширенное шифрование сообщений включено в [Microsoft 365 корпоративный](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise и Office 365 образования A5.</span><span class="sxs-lookup"><span data-stu-id="c2afe-106">Advanced Message Encryption is included in [Microsoft 365 Enterprise E5](https://www.microsoft.com/microsoft-365/enterprise/home), Office 365 Enterprise E5, and Office 365 Education A5.</span></span> <span data-ttu-id="c2afe-107">Если в вашей организации есть подписка на Office 365, которая не включает расширенное шифрование сообщений Office 365, вы можете приобрести дополнительное шифрование сообщений в качестве надстройки с соответствием требованиям к расширенному набору для обеспечения соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="c2afe-107">If your organization has an Office 365 subscription that does not include Office 365 Advanced Message Encryption, you can purchase Advanced Message Encryption as an add-on with E5 Compliance of the Advanced Compliance SKU.</span></span>

<span data-ttu-id="c2afe-108">Эта статья входит в набор статей, посвященных [шифрованию сообщений Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="c2afe-108">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span>

<span data-ttu-id="c2afe-109">Может потребоваться отзыв уже отправленного сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c2afe-109">You may find it necessary to revoke an email that has already been sent.</span></span> <span data-ttu-id="c2afe-110">Если сообщение было зашифровано с помощью расширенного шифрования сообщений Office 365 и вы являетесь администратором Office 365, это можно сделать для электронной почты при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="c2afe-110">If the email was encrypted using Office 365 Advanced Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions.</span></span> <span data-ttu-id="c2afe-111">В этой статье описывается, какие обстоятельства возможны, и как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="c2afe-111">This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="c2afe-112">Зашифрованные сообщения электронной почты, которые можно отозвать</span><span class="sxs-lookup"><span data-stu-id="c2afe-112">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="c2afe-113">Вы можете отозвать зашифрованные сообщения, если получатель получил зашифрованную электронную почту на основе ссылок.</span><span class="sxs-lookup"><span data-stu-id="c2afe-113">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="c2afe-114">Если получатель получил собственный встроенный интерфейс в поддерживаемом клиенте Outlook, эти сообщения не могут быть отозваны.</span><span class="sxs-lookup"><span data-stu-id="c2afe-114">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="c2afe-115">Сведения о том, получает ли получатель доступ на основе ссылок или встроенные возможности, зависят от типа удостоверения получателя: получатели Office 365 и учетной записи Майкрософт (например, пользователи outlook.com) получают встроенные возможности в поддерживаемых клиентах Outlook.</span><span class="sxs-lookup"><span data-stu-id="c2afe-115">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="c2afe-116">Все другие типы получателей, например получатели Gmail, получают интерфейс, основанный на ссылке.</span><span class="sxs-lookup"><span data-stu-id="c2afe-116">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="c2afe-117">Получатель отзыва о отозванных зашифрованных сообщениях</span><span class="sxs-lookup"><span data-stu-id="c2afe-117">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="c2afe-118">После того как электронная почта будет отозвана, получатель получит сообщение об ошибке при попытке получить доступ к зашифрованной электронной почте через портал шифрования сообщений Office 365: "сообщение было отозвано отправителем".</span><span class="sxs-lookup"><span data-stu-id="c2afe-118">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Снимок экрана, на котором показан отозванный зашифрованный адрес электронной почты.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="c2afe-120">Отзыв зашифрованного сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="c2afe-120">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="c2afe-121">Действие 1.</span><span class="sxs-lookup"><span data-stu-id="c2afe-121">Step 1.</span></span> <span data-ttu-id="c2afe-122">Получение идентификатора сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="c2afe-122">Obtain the Message ID of the email</span></span>

<span data-ttu-id="c2afe-123">Прежде чем отозвать зашифрованную почту, необходимо собрать идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="c2afe-123">Before you can revoke an encrypted mail you need to gather the Message ID of the mail.</span></span> <span data-ttu-id="c2afe-124">MessageId обычно имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="c2afe-124">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="c2afe-125">Существует несколько способов поиска идентификатора сообщения электронной почты, которое нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="c2afe-125">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="c2afe-126">В этом разделе описывается несколько вариантов, но вы можете использовать любой метод, который предоставляет идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c2afe-126">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="c2afe-127">Определение идентификатора сообщения электронной почты, которое нужно отозвать, с помощью трассировки сообщений в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="c2afe-127">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="c2afe-128">Поиск почты по отправителям или получателям с помощью [новой трассировки сообщений в центре безопасности Office 365 Security _амп_](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="c2afe-128">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>

2. <span data-ttu-id="c2afe-129">После того как вы нашли сообщение, выберите его, чтобы открыть область **сведений трассировки сообщений** .</span><span class="sxs-lookup"><span data-stu-id="c2afe-129">Once you've located the email, select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="c2afe-130">Разверните **Дополнительные сведения** , чтобы узнать идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="c2afe-130">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="c2afe-131">Определение идентификатора сообщения электронной почты, которое вы хотите отозвать, с помощью отчетов о шифровании сообщений Office в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="c2afe-131">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="c2afe-132">В центре безопасности &amp; и соответствия требованиям перейдите к **отчету шифрование сообщений**.</span><span class="sxs-lookup"><span data-stu-id="c2afe-132">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>

2. <span data-ttu-id="c2afe-133">Выберите таблицу **Просмотр сведений** и определите сообщение, которое нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="c2afe-133">Choose the **View details** table and identify the message that you want to revoke.</span></span>

3. <span data-ttu-id="c2afe-134">Дважды щелкните сообщение, чтобы просмотреть сведения, содержащие идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="c2afe-134">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="c2afe-135">Действие 2.</span><span class="sxs-lookup"><span data-stu-id="c2afe-135">Step 2.</span></span> <span data-ttu-id="c2afe-136">Проверка подлинности почты ревокабле</span><span class="sxs-lookup"><span data-stu-id="c2afe-136">Verify that the mail is revocable</span></span>

<span data-ttu-id="c2afe-137">Чтобы проверить, можно ли отозвать конкретное сообщение электронной почты, убедитесь, что поле состояние отзыва отображается в таблице **сведений** центра соответствия требованиям безопасности &amp; .</span><span class="sxs-lookup"><span data-stu-id="c2afe-137">To verify whether you can revoke a particular email message, check whether the Revocation Status field is visible in the **Details** table in the Security &amp; Compliance Center.</span></span>

<span data-ttu-id="c2afe-138">Чтобы проверить, можно ли отозвать конкретное сообщение электронной почты с помощью Windows PowerShell, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c2afe-138">To verify whether or not you can revoke a particular email message by using Windows Powershell, complete these steps.</span></span>

1. <span data-ttu-id="c2afe-139">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c2afe-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="c2afe-140">Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="c2afe-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="c2afe-141">Выполните командлет Set – Омемессажестатус следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c2afe-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>

     ```powershell
     Get-OMEMessageStatus -MessageId "<message id>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="c2afe-142">Возвращает тему сообщения и о том, является ли сообщение ревокабле.</span><span class="sxs-lookup"><span data-stu-id="c2afe-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="c2afe-143">For example,</span><span class="sxs-lookup"><span data-stu-id="c2afe-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="c2afe-144">Действие 3.</span><span class="sxs-lookup"><span data-stu-id="c2afe-144">Step 3.</span></span> <span data-ttu-id="c2afe-145">Отзыв почты</span><span class="sxs-lookup"><span data-stu-id="c2afe-145">Revoke the mail</span></span>  

<span data-ttu-id="c2afe-146">Когда вы узнаете идентификатор сообщения электронной почты, которое нужно отозвать, и убедитесь, что оно ревокабле, вы можете отозвать электронную почту.</span><span class="sxs-lookup"><span data-stu-id="c2afe-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email.</span></span>

<span data-ttu-id="c2afe-147">Чтобы отозвать электронную почту в центре безопасности &amp; и соответствия требованиям, в таблице **сведения** нажмите **отозвать**.</span><span class="sxs-lookup"><span data-stu-id="c2afe-147">To revoke the email in the Security &amp; Compliance Center, in the **Details** table, choose **Revoke**.</span></span>

<span data-ttu-id="c2afe-148">Отозвать электронную почту с помощью Windows PowerShell можно с помощью командлета Set – Омемессажеревокатион.</span><span class="sxs-lookup"><span data-stu-id="c2afe-148">You can revoke an email by using Windows Powershell by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="c2afe-149">[Подключитесь к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="c2afe-149">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="c2afe-150">Выполните командлет Set – Омемессажеревокатион следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c2afe-150">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="c2afe-151">Чтобы проверить, было ли отозвано сообщение электронной почты, выполните командлет Get – Омемессажестатус следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c2afe-151">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```

    <span data-ttu-id="c2afe-152">Если отзыв был выполнен успешно, командлет возвращает следующий результат:</span><span class="sxs-lookup"><span data-stu-id="c2afe-152">If revocation was successful, the cmdlet returns the following result:</span></span>  

     ```text
     Revoked: True
     ```

## <a name="more-information-about-office-365-advanced-message-encryption"></a><span data-ttu-id="c2afe-153">Дополнительные сведения о расширенном шифровании сообщений в Office 365</span><span class="sxs-lookup"><span data-stu-id="c2afe-153">More information about Office 365 Advanced Message Encryption</span></span>

- [<span data-ttu-id="c2afe-154">Расширенное шифрование сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="c2afe-154">Office 365 Advanced Message Encryption</span></span>](ome-advanced-message-encryption.md)

- [<span data-ttu-id="c2afe-155">Расширенное шифрование сообщения Office 365 — истечение срока действия электронной почты</span><span class="sxs-lookup"><span data-stu-id="c2afe-155">Office 365 Advanced Message Encryption - email expiration</span></span>](ome-advanced-expiration.md)

- [<span data-ttu-id="c2afe-156">Описание политики сообщений и службы соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="c2afe-156">Message policy and compliance service description</span></span>](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/message-policy-and-compliance)