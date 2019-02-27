---
title: Управление шифрованием сообщений Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- M365-security-compliance
description: После завершения настройки шифрования сообщений Office 365 (OME) можно настроить конфигурацию развертывания несколькими способами. Например, вы можете включить одноразовые коды проходов, отобразить кнопку Защита в Outlook в Интернете и многое другое. Задачи, описанные в этой статье, описывают, как.
ms.openlocfilehash: 7b5297ae42d3efa071408540863c6ff7dbdee407
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275979"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="ef715-105">Управление шифрованием сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="ef715-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="ef715-p102">После завершения настройки шифрования сообщений Office 365 (OME) можно настроить конфигурацию развертывания несколькими способами. Например, вы можете включить одноразовые коды проходов, отобразить кнопку **Защита** в Outlook в Интернете и многое другое. Задачи, описанные в этой статье, описывают, как.</span><span class="sxs-lookup"><span data-stu-id="ef715-p102">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways. For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more. The tasks in this article describe how.</span></span>
  
||
|:-----|
|<span data-ttu-id="ef715-p103">Эта статья входит в набор статей, посвященных шифрованию сообщений Office 365. Эта статья предназначена для администраторов и Итпрос. Если вы просто ищете сведения о том, как отправлять или получать зашифрованные сообщения, ознакомьтесь со статьей, посвященной [шифрованИю сообщений Office 365 (OME)](ome.md) , и выберите статью, которая наилучшим образом соответствует вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="ef715-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="ef715-112">Управление тем, могут ли получатели учетной записи Google, Yahoo и Майкрософт использовать эти учетные записи для входа на портал Office 365 для шифрования сообщений</span><span class="sxs-lookup"><span data-stu-id="ef715-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="ef715-p104">По умолчанию при настройке новых возможностей шифрования сообщений Office 365 пользователи в организации могут отправлять сообщения получателям, находящимся за пресроком вашей организации Office 365. Если получатель использует *социальные идентификаторы* , такие как учетная запись Google, учетная запись Yahoo или учетная запись Майкрософт, получатель может войти на портал OME с помощью идентификатора социального страхования. При необходимости вы можете запретить получателям использовать социальные идентификаторы для входа на портал OME.</span><span class="sxs-lookup"><span data-stu-id="ef715-p104">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization. If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID. If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="ef715-116">Чтобы указать, следует ли разрешить получателям использовать социальные идентификаторы для входа на портал OME</span><span class="sxs-lookup"><span data-stu-id="ef715-116">To manage whether or not to allow recipients to use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="ef715-117">[Подключитесь к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef715-117">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="ef715-118">Выполните командлет Set – OMEConfiguration с параметром СоЦиалидсигнин следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef715-118">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   <span data-ttu-id="ef715-119">Например, чтобы отключить социальные идентификаторы:</span><span class="sxs-lookup"><span data-stu-id="ef715-119">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="ef715-120">Чтобы включить социальные идентификаторы:</span><span class="sxs-lookup"><span data-stu-id="ef715-120">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="ef715-121">Управление использованием кодов одноразовых проходов для входа на портал Office 365 для шифрования сообщений</span><span class="sxs-lookup"><span data-stu-id="ef715-121">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="ef715-p105">По умолчанию, если получатель сообщения, зашифрованного с помощью OME, не использует Outlook независимо от учетной записи, используемой получателем, получатель получает ссылку на веб-просмотр в ограниченном времени, которая позволяет читать сообщение. Это включает однократный код прохода. Как администратор вы можете управлять тем, можно ли использовать для входа на портал OME одноразовые коды проходов.</span><span class="sxs-lookup"><span data-stu-id="ef715-p105">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message. This includes a one-time pass code. As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a><span data-ttu-id="ef715-125">Управление созданием кодов прохода для OME.</span><span class="sxs-lookup"><span data-stu-id="ef715-125">To manage whether or not one-time pass codes are generated for OME</span></span>
  
1. <span data-ttu-id="ef715-p106">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online. Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="ef715-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="ef715-128">Выполните командлет Set – OMEConfiguration с параметром Отпенаблед:</span><span class="sxs-lookup"><span data-stu-id="ef715-128">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="ef715-129">Например, чтобы отключить однократные коды прохода:</span><span class="sxs-lookup"><span data-stu-id="ef715-129">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="ef715-130">Чтобы включить однократные коды прохода:</span><span class="sxs-lookup"><span data-stu-id="ef715-130">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="ef715-131">Управление отображением кнопки "Защита" в Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="ef715-131">Managing the display of the Protect button in Outlook on the web</span></span>

<span data-ttu-id="ef715-p107">По умолчанию кнопка **защитить** в Outlook в Интернете не включена при настройке OME. Как администратор вы можете управлять отображением этой кнопки для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ef715-p107">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME. As an administrator, you can manage whether or not to display this button to end users.</span></span>
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="ef715-134">Чтобы управлять отображением кнопки "Защита" в Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="ef715-134">To manage whether or not the Protect button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="ef715-p108">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online. Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="ef715-p108">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="ef715-137">Выполните командлет Set – IRMConfiguration с параметром – Симплифиедклиентакцессенаблед:</span><span class="sxs-lookup"><span data-stu-id="ef715-137">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="ef715-138">Например, чтобы отключить кнопку **защитить** :</span><span class="sxs-lookup"><span data-stu-id="ef715-138">For example, to disable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="ef715-139">Чтобы включить кнопку **защитить** :</span><span class="sxs-lookup"><span data-stu-id="ef715-139">To enable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="ef715-140">Включение расшифровки сообщений электронной почты на стороне службы для пользователей почтового приложения для iOS</span><span class="sxs-lookup"><span data-stu-id="ef715-140">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="ef715-p109">Почтовое приложение iOS не может расшифровывать сообщения, защищенные с помощью шифрования сообщений Office 365. Как администратор Office 365, вы можете применять расшифровку на стороне службы для сообщений, доставляемых в почтовое приложение iOS. При выборе этого варианта служба отправляет расшифрованную копию сообщения на устройство iOS. Сообщение будет зашифровано на клиентском устройстве. Кроме того, в сообщении хранятся сведения о правах на использование, даже если почтовое приложение iOS не применяет к пользователю права на использование на стороне клиента. Это означает, что пользователь может скопировать или напечатать сообщение, даже если у них изначально нет прав на это. Тем не менее, если пользователь пытается выполнить действие, для которого требуется почтовый сервер Office 365, например пересылка сообщения, сервер не разрешает это действие, если пользователь изначально не имеет право использования. Тем не менее, конечные пользователи могут обойти ограничение использования, пересылая сообщение из другой учетной записи в своем почтовом приложении iOS. независимо от того, настроена ли расшифровка почты на стороне службы, любые вложения в зашифрованные и защищенные правами сообщения. невозможно просмотреть в почтовом приложении iOS.</span><span class="sxs-lookup"><span data-stu-id="ef715-p109">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption. As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app. When you choose to do this, the service sends a decrypted copy of the message to the iOS device. The message is stored decrypted on the client device. The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user. This means that the user can copy or print the message even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so. However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app. Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="ef715-p110">Если вы решили не разрешать отправку расшифрованных сообщений пользователям почтовых приложений iOS, пользователи получат сообщение о том, что у них нет прав на просмотр сообщения. По умолчанию Расшифровка сообщений электронной почты на стороне службы не включена.</span><span class="sxs-lookup"><span data-stu-id="ef715-p110">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message. By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="ef715-152">Более подробную информацию и представление интерфейса взаимодействия с клиентом можно узнать в статье [Просмотр зашифрованных сообщений на iPhone или iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="ef715-152">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="ef715-153">Управление тем, могут ли пользователи почтового приложения iOS просматривать сообщения, защищенные с помощью шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="ef715-153">To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="ef715-p111">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online. Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="ef715-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="ef715-156">Выполните командлет Set – Активесинкорганизатионс с параметром Алловрмссуппортфоруненлигхтенедаппс:</span><span class="sxs-lookup"><span data-stu-id="ef715-156">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="ef715-157">Например, чтобы настроить службу для расшифровки сообщений перед их отправкой в приложения уненлигхтенед, такие как почтовое приложение для iOS, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ef715-157">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="ef715-158">Или, чтобы настроить службу так, чтобы она не отправляла расшифрованные сообщения в приложения уненлигхтенед:</span><span class="sxs-lookup"><span data-stu-id="ef715-158">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="ef715-159">Включение расшифровки вложений электронной почты на стороне службы для почтовых клиентов веб-браузеров</span><span class="sxs-lookup"><span data-stu-id="ef715-159">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="ef715-p112">Как правило, при использовании шифрования сообщений Office 365 вложения автоматически шифруются. Как администратор Office 365, вы можете применять расшифровку на стороне службы для вложений электронной почты, которые пользователи скачивают из веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="ef715-p112">Normally, when you use Office 365 message encryption, attachments are automatically encrypted. As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="ef715-p113">При выборе этого параметра служба отправляет расшифрованную копию файла на устройство. Сообщение все еще зашифровано. Вложение электронной почты также сохраняет сведения о правах на использование, несмотря на то, что браузер не применяет к пользователю права на использование на стороне клиента. Это означает, что пользователь может скопировать или напечатать вложение электронной почты, даже если у них изначально нет таких прав. Тем не менее, если пользователь пытается выполнить действие, требующее наличия почтового сервера Office 365, например переадресацию вложения, сервер не разрешает это действие, если пользователь изначально не имеет право использования.</span><span class="sxs-lookup"><span data-stu-id="ef715-p113">When you choose to do this, the service sends a decrypted copy of the file to the device. The message is still encrypted. The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user. This means that the user can copy or print the email attachment even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="ef715-167">Независимо от того, настроена ли расшифровка вложений на стороне службы, любые вложения в зашифрованные и защищенные правами сообщения не могут быть просмотрены в почтовом приложении iOS.</span><span class="sxs-lookup"><span data-stu-id="ef715-167">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="ef715-168">Если вы не разрешите расшифровывать вложенные сообщения электронной почты (по умолчанию), пользователи получат сообщение о том, что у них нет прав на просмотр вложения.</span><span class="sxs-lookup"><span data-stu-id="ef715-168">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="ef715-169">Для получения дополнительных сведений о том, как Office 365 внедряет шифрование для сообщений электронной почты и вложений электронной почты с помощью параметра только шифрование, в разделе только [шифрование для сообщений](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails) электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ef715-169">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="ef715-170">Чтобы настроить расшифровку вложений электронной почты при загрузке из веб-браузера</span><span class="sxs-lookup"><span data-stu-id="ef715-170">To manage whether or not email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="ef715-p114">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online. Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="ef715-p114">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="ef715-173">Выполните командлет Set – IRMConfiguration с параметром Декриптаттачментфромпортал:</span><span class="sxs-lookup"><span data-stu-id="ef715-173">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   <span data-ttu-id="ef715-174">Например, чтобы настроить службу для расшифровки вложений электронной почты, когда пользователь загрузит их из веб-браузера, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ef715-174">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   <span data-ttu-id="ef715-175">Чтобы настроить службу для выхода из зашифрованных вложений электронной почты во время загрузки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ef715-175">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="ef715-176">Настройка внешнего вида сообщений электронной почты и портала OME</span><span class="sxs-lookup"><span data-stu-id="ef715-176">Customizing the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="ef715-177">Подробные сведения о том, как настроить OME для вашей организации, можно найти [в статье Добавление фирменной символики вашей организации в зашифрованные сообщения](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="ef715-177">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="ef715-178">Отключение новых возможностей для OME</span><span class="sxs-lookup"><span data-stu-id="ef715-178">Disabling the new capabilities for OME</span></span>

<span data-ttu-id="ef715-p115">Мы надеемся, что она не поступила, но если вам необходимо отключить новые возможности для OME, очень просто. Сначала необходимо удалить все созданные вами правила для процесса обработки почты, в которых используются новые возможности OME. Сведения об удалении правил для процесса обработки почты приведены в разделе [Управление правилами](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx)обработки почты. Затем выполните указанные ниже действия в Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ef715-p115">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward. First, you'll need to remove any mail flow rules you've created that use the new OME capabilities. For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="ef715-183">Отключение новых возможностей для OME</span><span class="sxs-lookup"><span data-stu-id="ef715-183">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="ef715-p116">С помощью рабочей или учебной учетной записи с разрешениями глобального администратора в организации Office 365 запустите сеанс Windows PowerShell и подключитесь к Exchange Online. Инструкции можно найти [в статье подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="ef715-p116">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="ef715-p117">Если вы включили кнопку **Защита** в Outlook в Интернете, отключите ее, выполнив командлет Set-IRMConfiguration с параметром симплифиедклиентакцессенаблед. В противном случае пропустите этот шаг.</span><span class="sxs-lookup"><span data-stu-id="ef715-p117">If you enabled the **Protect** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter. Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="ef715-188">Отключите новые возможности для OME, выполнив командлет Set – IRMConfiguration с параметром Азурермслиценсинженаблед, равным false:</span><span class="sxs-lookup"><span data-stu-id="ef715-188">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
