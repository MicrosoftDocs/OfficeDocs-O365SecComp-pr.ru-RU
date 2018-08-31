---
title: Управление шифрованием сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
description: Закончив параметр копирование шифрования сообщений Office 365 (OME), можно настроить параметры конфигурации развертывания в следующих случаях. Например можно настроить для включения одноразовый проход коды, отображать кнопку Защита в Outlook на веб-сайта и многое другое. Задач, описанных в этой статье описывается способ.
ms.openlocfilehash: ddc86bdf0d0ce5480587862a4ed438b6c138987f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534585"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="cfd87-105">Управление шифрованием сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="cfd87-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="cfd87-p102">Закончив параметр копирование шифрования сообщений Office 365 (OME), можно настроить параметры конфигурации развертывания в следующих случаях. Например можно настроить для включения одноразовый проход коды, отображать кнопку **Защита** в Outlook на веб-сайта и многое другое. Задач, описанных в этой статье описывается способ.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p102">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways. For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more. The tasks in this article describe how.</span></span> 
  
||
|:-----|
|<span data-ttu-id="cfd87-p103">В этой статье является частью серии статей о шифровании сообщений Office 365, размер которых. Эта статья предназначена для администраторов и ИТ-специалистов. Если вы только что подробную информацию об отправке или получении зашифрованного сообщения, просматривать список статей в [Шифрования сообщений Office 365 (OME)](ome.md) и найдите статьи, который лучше все соответствует вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and IT Pros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
   
## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="cfd87-112">Управление ли получателей Google Yahoo и учетную запись Майкрософт можно использовать эти учетные записи выполнить вход на портал шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="cfd87-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>
<span data-ttu-id="cfd87-113"><a name="PermitSocialID"> </a></span><span class="sxs-lookup"><span data-stu-id="cfd87-113"></span></span>

<span data-ttu-id="cfd87-p104">По умолчанию при создании новых возможностей шифрования сообщений Office 365, пользователи в вашей организации могут отправлять сообщения получателям, которые расположены вне вашей организации Office 365. Если получатель использует *социальных ID* , например Google учетной записи, Yahoo учетной записи или учетной записи Майкрософт, получатель могут выполнить вход на портал OME, с помощью социальных кода. Если вы хотите, вы можете запретить использование получателей для использования социальных идентификаторов для входа в портал OME.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p104">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization. If the recipient uses a  *social ID*  such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID. If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span> 
  
 <span data-ttu-id="cfd87-117">**Для управления ли разрешить получателей для использования социальных идентификаторов для входа в портал OME**</span><span class="sxs-lookup"><span data-stu-id="cfd87-117">**To manage whether or not to allow recipients to use social IDs to sign in to the OME portal**</span></span>
  
1. <span data-ttu-id="cfd87-118">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfd87-118">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="cfd87-119">Используйте командлет Set-OMEConfiguration с параметром SocialIdSignIn следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cfd87-119">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true |$false >
  ```

    <span data-ttu-id="cfd87-120">Например, чтобы отключить социальных идентификаторы:</span><span class="sxs-lookup"><span data-stu-id="cfd87-120">For example, to disable social IDs:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

    <span data-ttu-id="cfd87-121">Для включения социальных идентификаторы:</span><span class="sxs-lookup"><span data-stu-id="cfd87-121">To enable social IDs:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="cfd87-122">Управление одноразовый проход коды для вход на портал шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="cfd87-122">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>
<span data-ttu-id="cfd87-123"><a name="GenerateOTPC"> </a></span><span class="sxs-lookup"><span data-stu-id="cfd87-123"></span></span>

<span data-ttu-id="cfd87-p105">По умолчанию если получатель сообщения, зашифрованные с OME не использует Outlook, независимо от того, учетная запись, используемая для получателя получатель получает ограниченной по времени веб Просмотр ссылку, которая позволяет им читать сообщения. Этот компонент включает одноразовый проход кода. Как администратор могут управлять ли одноразовый проход коды можно использовать для входа в систему на портале OME.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p105">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message. This includes a one-time pass code. As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
 <span data-ttu-id="cfd87-127">**Для управления ли одноразовый проход коды для OME**</span><span class="sxs-lookup"><span data-stu-id="cfd87-127">**To manage whether or not one-time pass codes are generated for OME**</span></span>
  
1. <span data-ttu-id="cfd87-128">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfd87-128">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="cfd87-129">Используйте командлет Set-OMEConfiguration с параметром OTPEnabled следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cfd87-129">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter as follows:</span></span>
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true |$false >
  ```

    <span data-ttu-id="cfd87-130">Например, чтобы отключить коды одноразовый проход:</span><span class="sxs-lookup"><span data-stu-id="cfd87-130">For example, to disable one-time pass codes:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
  ```

    <span data-ttu-id="cfd87-131">Чтобы включить одноразовый проход коды:</span><span class="sxs-lookup"><span data-stu-id="cfd87-131">To enable one-time pass codes:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
  ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="cfd87-132">Управление отображение кнопки защита в Outlook в Интернете</span><span class="sxs-lookup"><span data-stu-id="cfd87-132">Managing the display of the Protect button in Outlook on the web</span></span>
<span data-ttu-id="cfd87-133"><a name="DisplayProtectButton"> </a></span><span class="sxs-lookup"><span data-stu-id="cfd87-133"></span></span>

<span data-ttu-id="cfd87-p106">По умолчанию при установке OME кнопку **Защита** в Outlook в Интернете не включено. Как администратор могут управлять ли отображать эту кнопку для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p106">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME. As an administrator, you can manage whether or not to display this button to end users.</span></span> 
  
 <span data-ttu-id="cfd87-136">**Для управления ли "защитить" отображается в Outlook в Интернете**</span><span class="sxs-lookup"><span data-stu-id="cfd87-136">**To manage whether or not the Protect button appears in Outlook on the web**</span></span>
  
1. <span data-ttu-id="cfd87-137">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfd87-137">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="cfd87-138">Используйте командлет Set-IRMConfiguration с параметром - SimplifiedClientAccessEnabled следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cfd87-138">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true |$false >
  ```

    <span data-ttu-id="cfd87-139">Например, чтобы отключить " **защитить** ":</span><span class="sxs-lookup"><span data-stu-id="cfd87-139">For example, to disable the **Protect** button:</span></span> 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

    <span data-ttu-id="cfd87-140">Чтобы активировать кнопку **защитить** :</span><span class="sxs-lookup"><span data-stu-id="cfd87-140">To enable the **Protect** button:</span></span> 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
  ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="cfd87-141">Включение расшифровки со стороны службы сообщений электронной почты для пользователей приложения почты операций ввода-вывода</span><span class="sxs-lookup"><span data-stu-id="cfd87-141">Enable service-side decryption of email messages for iOS mail app users</span></span>
<span data-ttu-id="cfd87-142"><a name="EnableServiceSideDecrypt"> </a></span><span class="sxs-lookup"><span data-stu-id="cfd87-142"></span></span>

<span data-ttu-id="cfd87-p107">Почтовое приложение операций ввода-вывода не удалось расшифровать сообщения, защищенные с помощью шифрования сообщений Office 365. Как администратор Office 365 можно применить расшифровки со стороны службы для сообщения, доставленные в почтовом приложении операций ввода-вывода. При выборе для этого служба отправляет копию расшифрованного сообщения на устройство операций ввода-вывода. Сообщение сохраняется расшифрован на клиентском устройстве. Сообщение также сохраняет информацию о правах на использование, несмотря на то, что почтовое приложение операций ввода-вывода не применима правах на использование со стороны клиента для пользователя. Это означает, что пользователь можно скопировать или распечатать сообщение, даже в том случае, если они изначально не имел прав для этого. Тем не менее если пользователь пытается выполнить действие, которое требует почтовый сервер Office 365, например пересылать, сервер не позволяет действие Если пользователь не было изначально право использования для этого. Тем не менее конечные пользователи могут обойти не пересылать ограничение использования, Переадресация сообщения из другой учетной записи в их app. почты операций ввода-вывода, независимо от того, копирование расшифровки со стороны службы почты, любого вложения на зашифрованные и права Защищенная почта не удается просмотреть почтовое приложение операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p107">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption. As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app. When you choose to do this, the service sends a decrypted copy of the message to the iOS device. The message is stored decrypted on the client device. The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user. This means that the user can copy or print the message even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so. However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app. Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="cfd87-p108">Если принято решение не разрешать расшифрованного сообщения для отправки операций ввода-вывода почты пользователей приложения, пользователи получают сообщение о том, что у них нет права на просмотр сообщения. По умолчанию со стороны службы расшифровки сообщений электронной почты не включено.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p108">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message. By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="cfd87-154">Для получения дополнительных сведений и для представления с клиентом обратитесь к разделу «[Просмотр зашифрованных сообщений на iPhone и iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)» в [Просмотр зашифрованных сообщений на iPhone и iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="cfd87-154">For more information, and for a view of the client experience, see the section, "[View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" in [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
 <span data-ttu-id="cfd87-155">**Для управления ли iOS почтовые приложения пользователи могут просматривать шифрования сообщений Office 365 для защиты сообщений**</span><span class="sxs-lookup"><span data-stu-id="cfd87-155">**To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption**</span></span>
  
1. <span data-ttu-id="cfd87-156">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfd87-156">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="cfd87-157">Используйте командлет Set-ActiveSyncOrganizations с параметром AllowRMSSupportForUnenlightenedApps следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cfd87-157">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter as follows:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true |$false >
  ```

    <span data-ttu-id="cfd87-158">Например для настройки службы для расшифровки сообщения перед отправкой unenlightened приложений таких как iOS почтового приложения:</span><span class="sxs-lookup"><span data-stu-id="cfd87-158">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
  ```

    <span data-ttu-id="cfd87-159">Например, чтобы настроить службу не следует отправлять расшифрованного сообщения unenlightened приложений:</span><span class="sxs-lookup"><span data-stu-id="cfd87-159">For example, to configure the service not to send decrypted messages to unenlightened apps:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
  ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="cfd87-160">Включение расшифровки со стороны службы вложений электронной почты для веб-браузера почтовых клиентов</span><span class="sxs-lookup"><span data-stu-id="cfd87-160">Enable service-side decryption of email attachments for web browser mail clients</span></span>
<span data-ttu-id="cfd87-161"><a name="EnableServiceSideDecrypt"> </a></span><span class="sxs-lookup"><span data-stu-id="cfd87-161"></span></span>

<span data-ttu-id="cfd87-p109">Как правило при использовании шифрования сообщений Office 365, вложения, автоматически шифруются. Как администратор Office 365 можно применить расшифровки со стороны службы для вложений электронной почты, которые пользователи загружать из веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p109">Normally, when you use Office 365 message encryption, attachments are automatically encrypted. As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span> 
  
<span data-ttu-id="cfd87-p110">При выборе для этого служба отправляет расшифрованного копию файла на устройство. По-прежнему шифруется сообщение. Вложения электронной почты также сохраняет информацию о правах на использование, несмотря на то, что браузер не применяется правах на использование со стороны клиента для пользователя. Это означает, что пользователь может копировать или печатать вложения электронной почты, даже в том случае, если они изначально не имел прав для этого. Тем не менее если пользователь пытается выполнить действие, которое требуется на сервере почты Office 365, например переадресации вложение, сервер не позволяет действие Если пользователь не было изначально право использования для этого.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p110">When you choose to do this, the service sends a decrypted copy of the file to the device. The message is still encrypted. The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user. This means that the user can copy or print the email attachment even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="cfd87-169">Независимо от того, копирование расшифровки со стороны службы вложений шифруются все вложения и почты защищенные правами, нельзя просматривать в почтовом приложении операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="cfd87-169">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="cfd87-p111">Если принято решение не разрешать вложения расшифрованного электронной почты, который используется по умолчанию, пользователи получают сообщение о том, что у них нет права на просмотр вложения. \* \* \* вставить рисунок?</span><span class="sxs-lookup"><span data-stu-id="cfd87-p111">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment. \*\*\* insert picture?</span></span>
  
<span data-ttu-id="cfd87-172">Дополнительные сведения о реализации шифрования сообщения электронной почты и вложения электронной почты с параметром только для шифрования в Office 365 можно [зашифровать-режим только для сообщений электронной почты.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="cfd87-172">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
 <span data-ttu-id="cfd87-173">**Для управления ли вложения электронной почты расшифрованы при загрузке из веб-браузера**</span><span class="sxs-lookup"><span data-stu-id="cfd87-173">**To manage whether or not email attachments are decrypted on download from a web browser**</span></span>
  
1. <span data-ttu-id="cfd87-174">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfd87-174">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="cfd87-175">Используйте командлет Set-IRMConfiguration с параметром DecryptAttachmentFromPortal следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cfd87-175">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal <$true |$false >
  ```

    <span data-ttu-id="cfd87-176">Например для настройки службы для расшифровки вложений электронной почты, когда пользователь загружает их из веб-браузера:</span><span class="sxs-lookup"><span data-stu-id="cfd87-176">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $true
  ```

    <span data-ttu-id="cfd87-177">Настройка службы оставить вложения зашифрованное сообщение электронной почты, как и при их загрузке:</span><span class="sxs-lookup"><span data-stu-id="cfd87-177">To configure the service to leave encrypted email attachments as they are upon download:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $false
  ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="cfd87-178">Настройка внешнего вида сообщений электронной почты и портала OME</span><span class="sxs-lookup"><span data-stu-id="cfd87-178">Customizing the appearance of email messages and the OME portal</span></span>
<span data-ttu-id="cfd87-179"><a name="CustomizeAppearance"> </a></span><span class="sxs-lookup"><span data-stu-id="cfd87-179"></span></span>

<span data-ttu-id="cfd87-180">Подробные сведения о настройке OME для вашей организации в разделе [Добавление марки вашей организации в зашифрованные сообщения](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="cfd87-180">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="cfd87-181">Отключение новые возможности для OME</span><span class="sxs-lookup"><span data-stu-id="cfd87-181">Disabling the new capabilities for OME</span></span>
<span data-ttu-id="cfd87-182"><a name="CustomizeAppearance"> </a></span><span class="sxs-lookup"><span data-stu-id="cfd87-182"></span></span>

<span data-ttu-id="cfd87-p112">Мы желаем его не поступают в нее, но если вам потребуется, отключение новые возможности для OME является очень просто. Во-первых вам потребуется удалить любые почты поток обработки правила, созданные пользователем, использовать новые возможности OME. Сведения об удалении правила потока почты см [Управление правилами поток почты](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Затем выполните следующие действия в Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cfd87-p112">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward. First, you'll need to remove any mail flow rules you've created that use the new OME capabilities. For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Then, complete these steps in Exchange Online PowerShell.</span></span>
  
 <span data-ttu-id="cfd87-187">**Чтобы отключить новые возможности для OME**</span><span class="sxs-lookup"><span data-stu-id="cfd87-187">**To disable the new capabilities for OME**</span></span>
  
1. <span data-ttu-id="cfd87-188">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfd87-188">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span></span>
    
2. <span data-ttu-id="cfd87-189">Если этот параметр включен "защитить" в Outlook в Интернете, отключите его с помощью командлета Set-IRMConfiguration с параметром SimplifiedClientAccessEnabled следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cfd87-189">If you enabled the Protect button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

3. <span data-ttu-id="cfd87-190">Используйте командлет Set-IRMConfiguration с параметром AzureRMSLicensingEnabled следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cfd87-190">Run the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -AzureRMSLicensingEnabled $false
  ```


