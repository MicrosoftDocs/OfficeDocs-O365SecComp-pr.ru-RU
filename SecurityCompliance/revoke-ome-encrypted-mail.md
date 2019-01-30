---
title: Отзыв электронных писем, зашифрованных с помощью шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/29/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
description: Как администратор Office 365 можно отозвать конкретные сообщения, зашифрованные с помощью шифрования сообщений Office 365.
ms.openlocfilehash: a3f5c08d2c8660e56c378fc5fa7a850ff2c12eb5
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614393"
---
# <a name="office-365-message-encryption-email-revocation"></a><span data-ttu-id="4de4c-103">Office 365 шифрования сообщений электронной почты отзыва</span><span class="sxs-lookup"><span data-stu-id="4de4c-103">Office 365 Message Encryption email revocation</span></span>

<span data-ttu-id="4de4c-p101">В этой статье является частью серии статей о [Шифровании сообщений Office 365](ome.md), размер которых. Отзыва электронной почты прямо сейчас, шифрованного соединения — в режиме предварительного просмотра. Ожидать обновления и изменения компонента и контент по мере улучшить наш предложения.</span><span class="sxs-lookup"><span data-stu-id="4de4c-p101">This article is part of a larger series of articles about [Office 365 Message Encryption](ome.md). Right now, encrypted email revocation is in preview. Expect updates and changes to the feature and the content as we continue to improve our offering.</span></span>

<span data-ttu-id="4de4c-p102">Может оказаться необходимым отзыв сообщения электронной почты, который уже был отправлен. Если вы — администратор Office 365 зашифрованного сообщения электронной почты с помощью шифрования сообщений Office 365, это можно сделать для электронной почты при определенных условиях. В этой статье описываются в разделе каких обстоятельствах это возможно и как это сделать.</span><span class="sxs-lookup"><span data-stu-id="4de4c-p102">You may find it necessary to revoke an email that has already been sent. If the email was encrypted using Office 365 Message Encryption, and you are an Office 365 admin, you can do this for email under certain conditions. This article describes under what circumstances this is possible and how to do it.</span></span>
  
## <a name="encrypted-emails-that-you-can-revoke"></a><span data-ttu-id="4de4c-110">Зашифрованные сообщения электронной почты, которые можно отменить</span><span class="sxs-lookup"><span data-stu-id="4de4c-110">Encrypted emails that you can revoke</span></span>

<span data-ttu-id="4de4c-p103">Можно отозвать зашифрованные сообщения электронной почты, когда получатель получить ссылку на основе, зашифрованное сообщение электронной почты с фирменной символикой. Если получатель полученные с программой собственный встроенный в поддерживаемых клиент Outlook, нельзя отозвать сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4de4c-p103">You can revoke encrypted emails if the recipient received a link-based, branded encrypted email. If the recipient received a native inline experience in a supported Outlook client, then those emails cannot be revoked.</span></span>

<span data-ttu-id="4de4c-p104">Ли получателя ссылку-взаимодействия или обеспечения взаимодействия встроенного зависит от типа получателя удостоверения: Office 365 и учетную запись Майкрософт получателей (например, outlook.com пользователей) получить обеспечения взаимодействия встроенного в поддерживаемых клиентах Outlook. Всех других типов получателей, такие как получатели Gmail Получение ссылок-взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="4de4c-p104">Whether a recipient receives a link-based experience or an inline experience depends on the recipient identity type: Office 365 and Microsoft Account recipients (for example, outlook.com users) get an inline experience in supported Outlook clients. All other recipient types, such as Gmail recipients, get a link-based experience.</span></span>

<span data-ttu-id="4de4c-p105">Готовится к выпуску, организации имеют возможность принудительно возможности связи вне зависимости от получателя удостоверения. Таким образом, всех получателей будет фирменной символики электронной почты со ссылкой на портал шифрования сообщений Office 365, где они смогут читать и отвечать на зашифрованные сообщения электронной почты. Все такие зашифрованные сообщения электронной почты будут отзыва.</span><span class="sxs-lookup"><span data-stu-id="4de4c-p105">Coming soon, organizations will have the ability to force a link-based experience regardless of the recipient identity. This way, all recipients will get a branded email with a link to the Office 365 Message Encryption portal where they will be able to read and reply to encrypted emails. All such encrypted emails will be revocable.</span></span>
  
## <a name="recipient-experience-for-revoked-encrypted-emails"></a><span data-ttu-id="4de4c-118">Получателей взаимодействия для отозванного зашифрованные сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="4de4c-118">Recipient experience for revoked encrypted emails</span></span>

<span data-ttu-id="4de4c-119">После отзыва сообщения электронной почты получателя появится сообщение об ошибке при попытке доступа к зашифрованное сообщение электронной почты через портал шифрования сообщений Office 365: «сообщение был отозван отправителем».</span><span class="sxs-lookup"><span data-stu-id="4de4c-119">Once an email has been revoked, the recipient will get an error when trying to access the encrypted email through the Office 365 Message Encryption portal: “The message has been revoked by the sender”.</span></span>

![Снимок экрана, показывающий отозванного зашифрованное сообщение электронной почты.](media/revoked-encrypted-email.png)

## <a name="how-to-revoke-an-encrypted-email"></a><span data-ttu-id="4de4c-121">Порядок отмены зашифрованное сообщение электронной почты</span><span class="sxs-lookup"><span data-stu-id="4de4c-121">How to revoke an encrypted email</span></span>

### <a name="step-1-obtain-the-message-id-of-the-email"></a><span data-ttu-id="4de4c-p106">Шаг 1. Получить идентификатор сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="4de4c-p106">Step 1. Obtain the Message ID of the email</span></span>

<span data-ttu-id="4de4c-p107">Прежде чем можно отозвать зашифрованных сообщений, которые необходимо собрать идентификатор сообщения электронной почты. Код (ID) — это обычно формата:</span><span class="sxs-lookup"><span data-stu-id="4de4c-p107">Before you can revoke an encrypted mail you need to gather the Message ID of the mail. The MessageId is usually of the format:</span></span>

`<xxxxxxxxxxxxxxxxxxxxxxx@xxxxxx.xxxx.prod.outlook.com>`  

<span data-ttu-id="4de4c-p108">Существует несколько способов получить идентификатор сообщения электронной почты, которое необходимо отменить. В этом разделе описывается несколько параметров, но можно использовать любой метод, который содержит код.</span><span class="sxs-lookup"><span data-stu-id="4de4c-p108">There are multiple ways to find the Message ID of the email that you want to revoke. This section describes a couple of options, but you can use any method that provides the ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-message-trace-in-the-security-amp-compliance-center"></a><span data-ttu-id="4de4c-128">Для определения идентификатора сообщения электронной почты, необходимо отменить с помощью Трассировка сообщений в системы &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="4de4c-128">To identify the Message ID of the email you want to revoke by using Message Trace in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="4de4c-129">Поиск сообщений электронной почты отправителя или получателя с помощью [Новых Трассировка сообщений в Office 365 безопасность & центре соответствия требованиям](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span><span class="sxs-lookup"><span data-stu-id="4de4c-129">Search for the email by sender or recipient using [New Message Trace in Office 365 Security & Compliance Center](https://blogs.technet.microsoft.com/exchange/2018/05/02/new-message-trace-in-office-365-security-compliance-center/).</span></span>
2. <span data-ttu-id="4de4c-p109">После, чтобы найти сообщение электронной почты выберите его, чтобы открыть область **сведений трассировки** . Разверните узел **Дополнительные сведения** , чтобы найти идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="4de4c-p109">Once you've located the email select it to bring up the **Message trace details** pane. Expand **More Information** to locate the Message ID.</span></span>

#### <a name="to-identify-the-message-id-of-the-email-you-want-to-revoke-by-using-office-message-encryption-reports-in-the-security-amp-compliance-center"></a><span data-ttu-id="4de4c-132">Для определения идентификатора сообщения электронной почты, необходимо отменить с помощью шифрования сообщений Office отчеты в безопасности &amp; центре соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="4de4c-132">To identify the Message ID of the email you want to revoke by using Office Message Encryption reports in the Security &amp; Compliance Center</span></span>

1. <span data-ttu-id="4de4c-133">В разделе Безопасность &amp; центре соответствия требованиям, перейдите к **Отчета о шифрования сообщений**.</span><span class="sxs-lookup"><span data-stu-id="4de4c-133">In the Security &amp; Compliance Center, navigate to the **Message Encryption Report**.</span></span>
2. <span data-ttu-id="4de4c-134">Выберите пункт **Просмотр подробных сведений о** таблицу и определите сообщение, которое необходимо отменить.</span><span class="sxs-lookup"><span data-stu-id="4de4c-134">Choose the **View details** table and identify the message that you want to revoke.</span></span>
3. <span data-ttu-id="4de4c-135">Дважды щелкните сообщение, чтобы Просмотр сведений, включая идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="4de4c-135">Double-click the message to view details that include the Message ID.</span></span>

### <a name="step-2-revoke-the-mail"></a><span data-ttu-id="4de4c-p110">Шаг 2. Отзыв по почте</span><span class="sxs-lookup"><span data-stu-id="4de4c-p110">Step 2. Revoke the mail</span></span>  

<span data-ttu-id="4de4c-138">Получив идентификатор сообщения электронной почты, которые необходимо отменить можно отозвать сообщение электронной почты с помощью командлета Set-OMEMessageRevocation.</span><span class="sxs-lookup"><span data-stu-id="4de4c-138">Once you know the Message ID of the email you want to revoke, you can revoke the email by using the Set-OMEMessageRevocation cmdlet.</span></span>

1. <span data-ttu-id="4de4c-139">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="4de4c-139">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).</span></span>

2. <span data-ttu-id="4de4c-140">Используйте командлет Set-OMEMessageRevocation следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4de4c-140">Run the Set-OMEMessageRevocation cmdlet as follows:</span></span>

    ```powershell
    Set-OMEMessageRevocation -Revoke $true -MessageId "<messageId>"
    ```  

3. <span data-ttu-id="4de4c-141">Чтобы проверить, был отозван ли сообщение электронной почты, выполните командлет Get-OMEMessageStatus следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4de4c-141">To check whether the email was revoked, run the Get-OMEMessageStatus cmdlet as follows:</span></span>

    ```powershell
    Get-OMEMessageStatus -MessageId "<messageId>" | fl Revoked
    ```  
    <span data-ttu-id="4de4c-142">В случае успешного отзыва, командлет возвращает следующие результаты:</span><span class="sxs-lookup"><span data-stu-id="4de4c-142">If revocation was successful, the cmdlet returns the following result:</span></span>  

    `Revoked: True`
