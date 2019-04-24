---
title: Отзыв электронных писем, зашифрованных с помощью шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Администратор Office 365 может отозвать определенные сообщения электронной почты, зашифрованные с помощью шифрования сообщений Office 365.
ms.openlocfilehash: 75b5e46e25f447ddac0de5a7911d0df8385da6b9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264830"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="55db2-103">Отзыв электронной почты по шифрованию сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="55db2-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="55db2-104">Эта статья входит в набор статей, посвященных [шифрованИю сообщений Office 365](ome.md).</span><span class="sxs-lookup"><span data-stu-id="55db2-104">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md).</span></span> <span data-ttu-id="55db2-105">В настоящее время отзыв зашифрованной электронной почты возможен предварительный просмотр.</span><span class="sxs-lookup"><span data-stu-id="55db2-105">Right now, encrypted email revocation is in preview.</span></span> <span data-ttu-id="55db2-106">Ожидайте обновления и изменения компонентов и контента, так как мы будем совершенствовать наш выпуск.</span><span class="sxs-lookup"><span data-stu-id="55db2-106">Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="55db2-107">Может потребоваться отзыв уже отправленного сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="55db2-107">You may find it necessary to revoke an email that has already been sent.</span></span> <span data-ttu-id="55db2-108">Если сообщение было зашифровано с помощью шифрования сообщений Office 365 и вы являетесь администратором Office 365, это можно сделать для сообщений электронной почты при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="55db2-108">If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions.</span></span> <span data-ttu-id="55db2-109">В этой статье описывается, какие обстоятельства возможны, и как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="55db2-109">This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="55db2-110">Зашифрованные сообщения электронной почты, которые можно отозвать</span><span class="sxs-lookup"><span data-stu-id="55db2-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="55db2-111">Вы можете отозвать зашифрованные сообщения, если получатель получил зашифрованную электронную почту на основе ссылок.</span><span class="sxs-lookup"><span data-stu-id="55db2-111">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email.</span></span> <span data-ttu-id="55db2-112">Если получатель получил собственный встроенный интерфейс в поддерживаемом клиенте Outlook, эти сообщения не могут быть отозваны.</span><span class="sxs-lookup"><span data-stu-id="55db2-112">If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="55db2-113">Сведения о том, получает ли получатель доступ на основе ссылок или встроенные возможности, зависят от типа удостоверения получателя: получатели Office 365 и учетной записи Майкрософт (например, пользователи outlook.com) получают встроенные возможности в поддерживаемых клиентах Outlook.</span><span class="sxs-lookup"><span data-stu-id="55db2-113">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients.</span></span> <span data-ttu-id="55db2-114">Все другие типы получателей, например получатели Gmail, получают интерфейс, основанный на ссылке.</span><span class="sxs-lookup"><span data-stu-id="55db2-114">All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="55db2-115">В ближайшее время организации смогут принудительно использовать интерфейс, основанный на связи, независимо от удостоверения получателя.</span><span class="sxs-lookup"><span data-stu-id="55db2-115">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity.</span></span> <span data-ttu-id="55db2-116">В этом случае все получатели получат Фирменное сообщение со ссылкой на портал шифрования сообщений Office 365, где они смогут читать зашифрованные сообщения и отвечать на них.</span><span class="sxs-lookup"><span data-stu-id="55db2-116">This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails.</span></span> <span data-ttu-id="55db2-117">Все такие зашифрованные сообщения электронной почты будут ревокабле.</span><span class="sxs-lookup"><span data-stu-id="55db2-117">All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="55db2-118">Получатель отзыва о отозванных зашифрованных сообщениях</span><span class="sxs-lookup"><span data-stu-id="55db2-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="55db2-119">После того как электронная почта будет отозвана, получатель получит сообщение об ошибке при попытке получить доступ к зашифрованной электронной почте через портал шифрования сообщений Office 365: "сообщение было отозвано отправителем".</span><span class="sxs-lookup"><span data-stu-id="55db2-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Снимок экрана, на котором показан отозванный зашифрованный адрес электронной почты.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="55db2-121">Отзыв зашифрованного сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="55db2-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="55db2-122">Действие 1.</span><span class="sxs-lookup"><span data-stu-id="55db2-122">Step 1.</span></span> <span data-ttu-id="55db2-123">Получение идентификатора сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="55db2-123">Obtain the Message ID of the email</span></span>

<span data-ttu-id="55db2-124">Прежде чем отозвать зашифрованную почту, необходимо собрать идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="55db2-124">Before you can revoke an encrypted mail you need to gather the Message ID of the mail.</span></span> <span data-ttu-id="55db2-125">MessageId обычно имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="55db2-125">The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="55db2-126">Существует несколько способов поиска идентификатора сообщения электронной почты, которое нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="55db2-126">There are multiple ways to find the Message ID of the email that you want to revoke.</span></span> <span data-ttu-id="55db2-127">В этом разделе описывается несколько вариантов, но вы можете использовать любой метод, который предоставляет идентификатор.</span><span class="sxs-lookup"><span data-stu-id="55db2-127">This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="55db2-128">Определение идентификатора сообщения электронной почты, которое нужно отозвать, с помощью трассировки сообщений в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="55db2-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="55db2-129">Поиск почты по отправителям или получателям с помощью [новой трассировки сообщений в центре безопасности Office 365 Security _амп_](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="55db2-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="55db2-130">После того как вы нашли сообщение, выберите его, чтобы открыть область **сведений трассировки сообщений** .</span><span class="sxs-lookup"><span data-stu-id="55db2-130">Once you've located the email select it to bring up the **Message trace details** pane.</span></span> <span data-ttu-id="55db2-131">Разверните **Дополнительные сведения** , чтобы узнать идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="55db2-131">Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="55db2-132">Определение идентификатора сообщения электронной почты, которое вы хотите отозвать, с помощью отчетов о шифровании сообщений Office в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="55db2-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="55db2-133">В центре безопасности &amp; и соответствия требованиям перейдите к **отчету шифрование сообщений**.</span><span class="sxs-lookup"><span data-stu-id="55db2-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="55db2-134">Выберите таблицу **Просмотр сведений** и определите сообщение, которое нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="55db2-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="55db2-135">Дважды щелкните сообщение, чтобы просмотреть сведения, содержащие идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="55db2-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="55db2-136">Действие 2.</span><span class="sxs-lookup"><span data-stu-id="55db2-136">Step 2.</span></span> <span data-ttu-id="55db2-137">Проверка подлинности почты ревокабле</span><span class="sxs-lookup"><span data-stu-id="55db2-137">Verify that the mail is revocable</span></span>

<span data-ttu-id="55db2-138">Чтобы проверить, можно ли отозвать конкретное сообщение электронной почты, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="55db2-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="55db2-139">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="55db2-139">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="55db2-140">Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="55db2-140">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="55db2-141">Выполните командлет Set – Омемессажестатус следующим образом:</span><span class="sxs-lookup"><span data-stu-id="55db2-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="55db2-142">Возвращает тему сообщения и о том, является ли сообщение ревокабле.</span><span class="sxs-lookup"><span data-stu-id="55db2-142">This returns the subject of the message and whether the message is revocable.</span></span> <span data-ttu-id="55db2-143">For example,</span><span class="sxs-lookup"><span data-stu-id="55db2-143">For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="55db2-144">Действие 3.</span><span class="sxs-lookup"><span data-stu-id="55db2-144">Step 3.</span></span> <span data-ttu-id="55db2-145">Отзыв почты</span><span class="sxs-lookup"><span data-stu-id="55db2-145">Revoke the mail</span></span>  

<span data-ttu-id="55db2-146">Зная идентификатор сообщения, которое вы хотите отозвать, и убедитесь, что оно ревокабле, вы можете отозвать сообщение электронной почты с помощью командлета Set-Омемессажеревокатион.</span><span class="sxs-lookup"><span data-stu-id="55db2-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="55db2-147">[Подключитесь к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="55db2-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="55db2-148">Выполните командлет Set – Омемессажеревокатион следующим образом:</span><span class="sxs-lookup"><span data-stu-id="55db2-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="55db2-149">Чтобы проверить, было ли отозвано сообщение электронной почты, выполните командлет Get – Омемессажестатус следующим образом:</span><span class="sxs-lookup"><span data-stu-id="55db2-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="55db2-150">Если отзыв был выполнен успешно, командлет возвращает следующий результат:</span><span class="sxs-lookup"><span data-stu-id="55db2-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
