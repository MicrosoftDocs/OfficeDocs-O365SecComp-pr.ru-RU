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
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214899"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="f59e0-103">Отзыв электронной почты по шифрованию сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="f59e0-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="f59e0-p101">Эта статья входит в набор статей, посвященных [шифрованИю сообщений Office 365](ome.md). В настоящее время отзыв зашифрованной электронной почты возможен предварительный просмотр. Ожидайте обновления и изменения компонентов и контента, так как мы будем совершенствовать наш выпуск.</span><span class="sxs-lookup"><span data-stu-id="f59e0-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="f59e0-p102">Может потребоваться отзыв уже отправленного сообщения электронной почты. Если сообщение было зашифровано с помощью шифрования сообщений Office 365 и вы являетесь администратором Office 365, это можно сделать для сообщений электронной почты при определенных условиях. В этой статье описывается, какие обстоятельства возможны, и как это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="f59e0-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="f59e0-110">Зашифрованные сообщения электронной почты, которые можно отозвать</span><span class="sxs-lookup"><span data-stu-id="f59e0-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="f59e0-p103">Вы можете отозвать зашифрованные сообщения, если получатель получил зашифрованную электронную почту на основе ссылок. Если получатель получил собственный встроенный интерфейс в поддерживаемом клиенте Outlook, эти сообщения не могут быть отозваны.</span><span class="sxs-lookup"><span data-stu-id="f59e0-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="f59e0-p104">Сведения о том, получает ли получатель доступ на основе ссылок или встроенные возможности, зависят от типа удостоверения получателя: получатели Office 365 и учетной записи Майкрософт (например, пользователи outlook.com) получают встроенные возможности в поддерживаемых клиентах Outlook. Все другие типы получателей, например получатели Gmail, получают интерфейс, основанный на ссылке.</span><span class="sxs-lookup"><span data-stu-id="f59e0-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="f59e0-p105">В ближайшее время организации смогут принудительно использовать интерфейс, основанный на связи, независимо от удостоверения получателя. В этом случае все получатели получат Фирменное сообщение со ссылкой на портал шифрования сообщений Office 365, где они смогут читать зашифрованные сообщения и отвечать на них. Все такие зашифрованные сообщения электронной почты будут ревокабле.</span><span class="sxs-lookup"><span data-stu-id="f59e0-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="f59e0-118">Получатель отзыва о отозванных зашифрованных сообщениях</span><span class="sxs-lookup"><span data-stu-id="f59e0-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="f59e0-119">После того как электронная почта будет отозвана, получатель получит сообщение об ошибке при попытке получить доступ к зашифрованной электронной почте через портал шифрования сообщений Office 365: "сообщение было отозвано отправителем".</span><span class="sxs-lookup"><span data-stu-id="f59e0-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Снимок экрана, на котором показан отозванный зашифрованный адрес электронной почты.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="f59e0-121">Отзыв зашифрованного сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="f59e0-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="f59e0-p106">Шаг 1. Получение идентификатора сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="f59e0-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="f59e0-p107">Прежде чем отозвать зашифрованную почту, необходимо собрать идентификатор сообщения. MessageId обычно имеет следующий формат:</span><span class="sxs-lookup"><span data-stu-id="f59e0-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="f59e0-p108">Существует несколько способов поиска идентификатора сообщения электронной почты, которое нужно отозвать. В этом разделе описывается несколько вариантов, но вы можете использовать любой метод, который предоставляет идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f59e0-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="f59e0-128">Определение идентификатора сообщения электронной почты, которое нужно отозвать, с помощью трассировки сообщений в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f59e0-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="f59e0-129">Поиск почты по отправителям или получателям с помощью [новой трассировки сообщений в центре безопасности Office 365 Security _амп_](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="f59e0-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="f59e0-p109">После того как вы нашли сообщение, выберите его, чтобы открыть область **сведений трассировки сообщений** . Разверните **Дополнительные сведения** , чтобы узнать идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="f59e0-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="f59e0-132">Определение идентификатора сообщения электронной почты, которое вы хотите отозвать, с помощью отчетов о шифровании сообщений Office в центре безопасности &amp; и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="f59e0-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="f59e0-133">В центре безопасности &amp; и соответствия требованиям перейдите к **отчету шифрование сообщений**.</span><span class="sxs-lookup"><span data-stu-id="f59e0-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="f59e0-134">Выберите таблицу **Просмотр сведений** и определите сообщение, которое нужно отозвать.</span><span class="sxs-lookup"><span data-stu-id="f59e0-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="f59e0-135">Дважды щелкните сообщение, чтобы просмотреть сведения, содержащие идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="f59e0-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="f59e0-p110">Шаг 2. Проверка подлинности почты ревокабле</span><span class="sxs-lookup"><span data-stu-id="f59e0-p110">Step 2. Verify that the mail is revocable</span></span>

<span data-ttu-id="f59e0-138">Чтобы проверить, можно ли отозвать конкретное сообщение электронной почты, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f59e0-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="f59e0-p111">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online. Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="f59e0-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="f59e0-141">Выполните командлет Set – Омемессажестатус следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f59e0-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="f59e0-p112">Возвращает тему сообщения и о том, является ли сообщение ревокабле. Например</span><span class="sxs-lookup"><span data-stu-id="f59e0-p112">This returns the subject of the message and whether the message is revocable. For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="f59e0-p113">Шаг 3. Отзыв почты</span><span class="sxs-lookup"><span data-stu-id="f59e0-p113">Step 3. Revoke the mail</span></span>  

<span data-ttu-id="f59e0-146">Зная идентификатор сообщения, которое вы хотите отозвать, и убедитесь, что оно ревокабле, вы можете отозвать сообщение электронной почты с помощью командлета Set-Омемессажеревокатион.</span><span class="sxs-lookup"><span data-stu-id="f59e0-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="f59e0-147">[Подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="f59e0-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="f59e0-148">Выполните командлет Set – Омемессажеревокатион следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f59e0-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="f59e0-149">Чтобы проверить, было ли отозвано сообщение электронной почты, выполните командлет Get – Омемессажестатус следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f59e0-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="f59e0-150">Если отзыв был выполнен успешно, командлет возвращает следующий результат:</span><span class="sxs-lookup"><span data-stu-id="f59e0-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
