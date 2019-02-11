---
title: Отзыв электронных писем, зашифрованных с помощью шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Как администратор Office 365 можно отозвать конкретные сообщения, зашифрованные с помощью шифрования сообщений Office 365.
ms.openlocfilehash: 018f12105e19382372a8a4b3a91248bb60b228be
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696243"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="28c16-103">Office 365 шифрования сообщений электронной почты отзыва</span><span class="sxs-lookup"><span data-stu-id="28c16-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="28c16-p101">В этой статье является частью серии статей о [Шифровании сообщений Office 365](ome.md), размер которых. Отзыва электронной почты прямо сейчас, шифрованного соединения — в режиме предварительного просмотра. Ожидать обновления и изменения компонента и контент по мере улучшить наш предложения.</span><span class="sxs-lookup"><span data-stu-id="28c16-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="28c16-p102">Может оказаться необходимым отзыв сообщения электронной почты, который уже был отправлен. Если вы — администратор Office 365 зашифрованного сообщения электронной почты с помощью шифрования сообщений Office 365, это можно сделать для электронной почты при определенных условиях. В этой статье описываются в разделе каких обстоятельствах это возможно и как это сделать.</span><span class="sxs-lookup"><span data-stu-id="28c16-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="28c16-110">Зашифрованные сообщения электронной почты, которые можно отменить</span><span class="sxs-lookup"><span data-stu-id="28c16-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="28c16-p103">Можно отозвать зашифрованные сообщения электронной почты, когда получатель получить ссылку на основе, зашифрованное сообщение электронной почты с фирменной символикой. Если получатель полученные с программой собственный встроенный в поддерживаемых клиент Outlook, нельзя отозвать сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="28c16-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="28c16-p104">Ли получателя ссылку-взаимодействия или обеспечения взаимодействия встроенного зависит от типа получателя удостоверения: Office 365 и учетную запись Майкрософт получателей (например, outlook.com пользователей) получить обеспечения взаимодействия встроенного в поддерживаемых клиентах Outlook. Всех других типов получателей, такие как получатели Gmail Получение ссылок-взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="28c16-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="28c16-p105">Готовится к выпуску, организации имеют возможность принудительно возможности связи вне зависимости от получателя удостоверения. Таким образом, всех получателей будет фирменной символики электронной почты со ссылкой на портал шифрования сообщений Office 365, где они смогут читать и отвечать на зашифрованные сообщения электронной почты. Все такие зашифрованные сообщения электронной почты будут отзыва.</span><span class="sxs-lookup"><span data-stu-id="28c16-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="28c16-118">Получателей взаимодействия для отозванного зашифрованные сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="28c16-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="28c16-119">После отзыва сообщения электронной почты получателя появится сообщение об ошибке при попытке доступа к зашифрованное сообщение электронной почты через портал шифрования сообщений Office 365: «сообщение был отозван отправителем».</span><span class="sxs-lookup"><span data-stu-id="28c16-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Снимок экрана, показывающий отозванного зашифрованное сообщение электронной почты.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="28c16-121">Порядок отмены зашифрованное сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="28c16-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="28c16-p106">Шаг 1. Получить идентификатор сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="28c16-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="28c16-p107">Прежде чем можно отозвать зашифрованных сообщений, которые необходимо собрать идентификатор сообщения электронной почты. Код (ID) — это обычно формата:</span><span class="sxs-lookup"><span data-stu-id="28c16-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="28c16-p108">Существует несколько способов получить идентификатор сообщения электронной почты, которое необходимо отменить. В этом разделе описывается несколько параметров, но можно использовать любой метод, который содержит код.</span><span class="sxs-lookup"><span data-stu-id="28c16-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="28c16-128">Для определения идентификатора сообщения электронной почты, необходимо отменить с помощью Трассировка сообщений в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="28c16-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="28c16-129">Поиск сообщений электронной почты отправителя или получателя с помощью [Новых Трассировка сообщений в Office 365 безопасность & центре соответствия требованиям](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="28c16-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="28c16-p109">После, чтобы найти сообщение электронной почты выберите его, чтобы открыть область **сведений трассировки** . Разверните узел **Дополнительные сведения** , чтобы найти идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="28c16-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="28c16-132">Для определения идентификатора сообщения электронной почты, необходимо отменить с помощью шифрования сообщений Office отчеты в безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="28c16-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="28c16-133">В разделе Безопасность &amp; центре соответствия требованиям, перейдите к **Отчета о шифрования сообщений**.</span><span class="sxs-lookup"><span data-stu-id="28c16-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="28c16-134">Выберите пункт **Просмотр подробных сведений о** таблицу и определите сообщение, которое необходимо отменить.</span><span class="sxs-lookup"><span data-stu-id="28c16-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="28c16-135">Дважды щелкните сообщение, чтобы Просмотр сведений, включая идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="28c16-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-verify-that-the-mail-is-revocable"></a><span data-ttu-id="28c16-p110">Шаг 2. Убедитесь, что почта, отзыва</span><span class="sxs-lookup"><span data-stu-id="28c16-p110">Step 2. Verify that the mail is revocable</span></span>

<span data-ttu-id="28c16-138">Чтобы проверить ли можно отозвать сообщение определенного электронной почты, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="28c16-138">To verify whether or not you can revoke a particular email message, complete these steps.</span></span>

1. <span data-ttu-id="28c16-p111">Использование рабочего или школы учетной записи, имеющей права глобального администратора в организации Office 365, начало сеанса Windows PowerShell и подключитесь к Exchange Online. Сведения содержатся в разделе [подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="28c16-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="28c16-141">Используйте командлет Set-OMEMessageStatus следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28c16-141">Run the Set-OMEMessageStatus cmdlet as follows:</span></span>
     ```powershell
     Get-OMEMessageStatus -MessageId "<messagieid>" | ft -a  Subject, IsRevocable
     ```

   <span data-ttu-id="28c16-p112">При этом будет получен тему сообщения и является ли сообщение отзыва. Например</span><span class="sxs-lookup"><span data-stu-id="28c16-p112">This returns the subject of the message and whether the message is revocable. For example,</span></span>

     ```text
     Subject IsRevocable
     ------- -----------
     “Test message”  True
     ```

### <a name="step-3-revoke-the-mail"></a><span data-ttu-id="28c16-p113">Шаг 3. Отзыв по почте</span><span class="sxs-lookup"><span data-stu-id="28c16-p113">Step 3. Revoke the mail</span></span>  

<span data-ttu-id="28c16-146">Один раз вы знаете код сообщения электронной почты, которые необходимо отменить и убедитесь, что сообщение отзыва, сообщение электронной почты можно отменить с помощью командлета Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="28c16-146">Once you know the Message ID of the email you want to revoke, and you have verified that the message is revocable, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="28c16-147">[Подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="28c16-147">[Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="28c16-148">Используйте командлет Set-OMEMessageRevocation следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28c16-148">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```

3. <span data-ttu-id="28c16-149">Чтобы проверить, был отозван ли сообщение электронной почты, выполните командлет Get-OMEMessageStatus следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28c16-149">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | ft -a  Subject, Revoked
    ```  
    <span data-ttu-id="28c16-150">В случае успешного отзыва, командлет возвращает следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="28c16-150">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
