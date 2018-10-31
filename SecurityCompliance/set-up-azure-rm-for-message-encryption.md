---
title: Настройка службы управления правами Azure для шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: Предыдущие версии шифрования сообщений Office 365, зависит от Microsoft Azure Rights Management (ранее называлась управления правами Active Directory Windows Azure).
ms.openlocfilehash: f8759da8628d4c78fe5409f5c47e3fc2b3e9484e
ms.sourcegitcommit: c05076501dfe118e575998ecfc08ad69d13c8abc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25853074"
---
# <a name="this-article-applies-to-the-previous-version-of-ome"></a><span data-ttu-id="e7d94-103">Эта статья относится к предыдущей версии OME</span><span class="sxs-lookup"><span data-stu-id="e7d94-103">This article applies to the previous version of OME</span></span>
<span data-ttu-id="e7d94-p101">Новые возможности OME еще еще не перемещены организации Office 365, но вы уже развернули OME, сведения в этой статье относятся для вашей организации. Корпорация Майкрософт рекомендует, чтобы сделать план для перемещения новых возможностей OME, как только целесообразно для вашей организации. Сведения содержатся в разделе [Set up новые возможности шифрования сообщений Office 365](set-up-new-message-encryption-capabilities.md). Если вы хотите узнать больше о новых возможностях сначала, ознакомьтесь со [Шифрования сообщений Office 365](ome.md). Далее в этой статье относится к OME поведение перед выпуском новых возможностей OME.</span><span class="sxs-lookup"><span data-stu-id="e7d94-p101">If you haven't yet moved your Office 365 organization to the new OME capabilities, but you have already deployed OME, then the information in this article applies to your organization. Microsoft recommends that you make a plan to move to the new OME capabilities as soon as it is reasonable for your organization. For instructions, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md). If you want to find out more about how the new capabilities work first, see [Office 365 Message Encryption](ome.md). The rest of this article refers to OME behavior before the release of the new OME capabilities.</span></span>

# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="e7d94-109">Настройка управления правами Azure для предыдущей версии шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="e7d94-109">Set up Azure Rights Management for the previous version of Office 365 Message Encryption</span></span>

<span data-ttu-id="e7d94-110">В этом разделе описаны действия, необходимые для активации и задайте его копирования Azure управления правами, частью защита информации Azure, для использования с помощью шифрования сообщений Office 365 (OME).</span><span class="sxs-lookup"><span data-stu-id="e7d94-110">This topic describes the steps you need to follow in order to activate and then set up Azure Rights Management (RMS), part of Azure Information Protection, for use with Office 365 Message Encryption (OME).</span></span>
  
## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="e7d94-111">Необходимые условия для использования предыдущей версии шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="e7d94-111">Prerequisites for using the previous version of Office 365 Message Encryption</span></span>
<span data-ttu-id="e7d94-112"><a name="warmprereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="e7d94-112"></span></span>

<span data-ttu-id="e7d94-p102">Office 365 Message Encryption (OME), включая IRM, зависит от службы управления правами Azure (Azure RMS). Службы управления правами Azure — это технология защиты, защита информации Azure. Чтобы использовать OME, организации Office 365 необходимо включить подписка на Exchange Online или Exchange Online Protection, в свою очередь, включает в себя подписка на службу управления правами Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d94-p102">Office 365 Message Encryption (OME), including IRM, depends on Azure Rights Management (Azure RMS). Azure RMS is the protection technology used by Azure Information Protection. To use OME, your Office 365 organization must include an Exchange Online or Exchange Online Protection subscription that, in turn, includes an Azure Rights Management subscription.</span></span>
  
- <span data-ttu-id="e7d94-116">Если вы не знаете подписка включает, ознакомьтесь со описания [политики сообщения, восстановление и соответствие требованиям](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx)службы Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="e7d94-116">If you're not sure of what your subscription includes, see the Exchange Online service descriptions for [Message Policy, Recovery, and Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span></span>
    
- <span data-ttu-id="e7d94-117">Если у вас нет подписки на службы управления правами Azure для Exchange Online или Exchange Online Protection, необходимо приобрести подписки и активации сначала.</span><span class="sxs-lookup"><span data-stu-id="e7d94-117">If you don't have an Azure RMS subscription for Exchange Online or Exchange Online Protection, you must purchase a subscription and activate it first.</span></span>
    
    <span data-ttu-id="e7d94-p103">Сведения о приобретении подписка на службу управления правами Azure можно [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). В следующем разделе приводится сведения об активации Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="e7d94-p103">For information about purchasing a subscription to Azure Rights Management, see [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). The next section gives you information about activating Azure Rights Management.</span></span>
    
- <span data-ttu-id="e7d94-120">Если у вас есть Azure Rights Management, но не настроена для Exchange Online или Exchange Online Protection, в этой статье объясняется, как включить службу управления правами Azure и затем описываются лучший способ настройки OME для работы с Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="e7d94-120">If you have Azure Rights Management but it's not set up for Exchange Online or Exchange Online Protection, this article explains how to activate Azure Rights Management and then the describes the best way to set up OME to work with Azure Rights Management.</span></span>
    
- <span data-ttu-id="e7d94-p104">Если вы уже установлено OME для управления правами Azure для Exchange Online или Exchange Online Protection, в зависимости от того, как настроить его, можно приступить к работе с OME и новые возможности немедленно. В этой статье объясняется, как определить, если настройки OME правильно, что делать, если необходимо изменить настройки, и что произойдет, если не требуется изменить настройку. Например чтобы использовать новые возможности, необходимо использовать службы управления правами Azure с OME. Новые возможности нельзя использовать вместе с локальной Active Directory службы управления правами.</span><span class="sxs-lookup"><span data-stu-id="e7d94-p104">If you've already set up OME to work with Azure Rights Management for Exchange Online or Exchange Online Protection, depending on how you set it up, you may be ready to start using OME and its new capabilities right away. This article explains how to determine if you've set OME up correctly, what to do if you need to change your setup, and what happens if you choose not to change your setup. For example, in order to use the new capabilities, you must use Azure RMS with OME. You can't use the new capabilities with an on-premises Active Directory RMS.</span></span>
    
## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a><span data-ttu-id="e7d94-125">Активация службы управления правами Azure для предыдущей версии OME в Office 365</span><span class="sxs-lookup"><span data-stu-id="e7d94-125">Activate Azure Rights Management for  the previous version of OME in Office 365</span></span>
<span data-ttu-id="e7d94-126"><a name="activatewarm"> </a></span><span class="sxs-lookup"><span data-stu-id="e7d94-126"></span></span>

<span data-ttu-id="e7d94-p105">Вам потребуется активация службы управления правами Azure, чтобы пользователи в вашей организации можно применить защиту сведения для сообщения, отправленные и открытие сообщений и файлов, защищенных службой управления правами Azure. [Активация службы управления правами Azure](https://go.microsoft.com/fwlink/p/?LinkId=525775)инструкции, см. После выполнения активации, вернитесь сюда и продолжите задач, описанных в этой статье.</span><span class="sxs-lookup"><span data-stu-id="e7d94-p105">You need to activate Azure Rights Management so that the users in your organization can apply information protection to messages that they send, and open messages and files that have been protected by the Azure Rights Management service. For instructions, see [Activating Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Once you've completed the activation, return here and continue with the tasks in this article.</span></span>
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a><span data-ttu-id="e7d94-130">Настройка предыдущей версии OME для использования службы управления правами Azure путем импорта доверенные домены публикации (доверенных доменов публикации)</span><span class="sxs-lookup"><span data-stu-id="e7d94-130">Set up the previous version of OME to use Azure RMS by importing trusted publishing domains (TPDs)</span></span>
<span data-ttu-id="e7d94-131"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="e7d94-131"></span></span>

<span data-ttu-id="e7d94-p106">Доверенный — это XML-файл, который содержит сведения о параметрах управления правами вашей организации. Например доверенный домен публикации содержит сведения об серверный сертификат лицензиара (SLC), используемый для подписи и шифрования сертификатов и лицензий, URL-адреса, используемые для лицензирования и публикации и т. д. Импортировать доверенный домен публикации в организации Office 365 с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7d94-p106">A TPD is an XML file that contains information about your organization's rights management settings. For example, the TPD contains information about the server licensor certificate (SLC) used for signing and encrypting certificates and licenses, the URLs used for licensing and publishing, and so on. You import the TPD into your Office 365 organization by using Windows PowerShell.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e7d94-p107">Ранее можно выбрать для импорта доверенных доменов публикации из службы управления правами Active Directory (AD RMS) в организации Office 365. Тем не менее, при этом будет препятствовать с помощью новых возможностей OME и не рекомендуется. Если Office 365 организации в настоящий момент настроена таким образом, корпорация Майкрософт рекомендует создания плана для переноса из вашей локальной Active Directory службы управления правами для защиты информации Azure на основе облака. Для получения дополнительных сведений см [AD RMS для защиты информации Azure](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Вы не сможете использовать новые возможности OME до завершения переноса для защиты информации Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d94-p107">Previously, you could choose to import TPDs from the Active Directory Rights Management service (AD RMS) into your Office 365 organization. However, doing so will prevent you from using the new OME capabilities and is not recommended. If your Office 365 organization is currently configured this way, Microsoft recommends that you create a plan to migrate from your on-premises Active Directory RMS to cloud-based Azure Information Protection. For more information, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). You will not be able to use the new OME capabilities until you have completed the migration to Azure Information Protection.</span></span> 
  
 <span data-ttu-id="e7d94-140">**Для импорта доверенных доменов публикации из службы управления правами Azure**</span><span class="sxs-lookup"><span data-stu-id="e7d94-140">**To import TPDs from Azure RMS**</span></span>
  
1. <span data-ttu-id="e7d94-141">[Подключение к Exchange Online с помощью удаленной оболочки PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7d94-141">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="e7d94-142">Выберите общий доступ к ключ URL-адрес, соответствующий географическое положение организации Office 365:</span><span class="sxs-lookup"><span data-stu-id="e7d94-142">Choose the key-sharing URL that corresponds to your Office 365 organization's geographic location:</span></span>
    
|<span data-ttu-id="e7d94-143">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="e7d94-143">**Location**</span></span>|<span data-ttu-id="e7d94-144">**Ключ, общий доступ к URL-адрес расположения**</span><span class="sxs-lookup"><span data-stu-id="e7d94-144">**Key sharing location URL**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7d94-145">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="e7d94-145">North America</span></span>  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="e7d94-146">Европейский Союз</span><span class="sxs-lookup"><span data-stu-id="e7d94-146">European Union</span></span>  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="e7d94-147">Азия</span><span class="sxs-lookup"><span data-stu-id="e7d94-147">Asia</span></span>  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="e7d94-148">Южная Америка</span><span class="sxs-lookup"><span data-stu-id="e7d94-148">South America</span></span>  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="e7d94-149">Office 365 для государственных учреждений (облако сообщества госучреждений)</span><span class="sxs-lookup"><span data-stu-id="e7d94-149">Office 365 for Government (Government Community Cloud)</span></span>  <br/> <span data-ttu-id="e7d94-150">Это расположение общего доступа к ключ службы управления правами зарезервирован для клиентов, которые приобрели Office 365 для государственных учреждений.</span><span class="sxs-lookup"><span data-stu-id="e7d94-150">This RMS key-sharing location is reserved for customers who have purchased Office 365 for Government SKUs.</span></span>  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. <span data-ttu-id="e7d94-151">Настройка расположения совместного использования ключа, выполнив командлет [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e7d94-151">Configure the key-sharing location by running the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet as follows:</span></span> 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    <span data-ttu-id="e7d94-152">Например, чтобы настроить Если организация находится в Северной Америке расположение для обмена ключами:</span><span class="sxs-lookup"><span data-stu-id="e7d94-152">For example, to configure the key sharing location if your organization is located in North America:</span></span>
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. <span data-ttu-id="e7d94-153">Выполните командлет [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) с параметром - RMSOnline, чтобы импортировать доверенный домен публикации из службы управления правами Azure:</span><span class="sxs-lookup"><span data-stu-id="e7d94-153">Run the [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet with the -RMSOnline switch to import the TPD from Azure Rights Management:</span></span> 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    <span data-ttu-id="e7d94-p108">Где *TPDName* — это имя будет использоваться для доверенный домен публикации. Например «Contoso Северной Америки доверенный домен публикации».</span><span class="sxs-lookup"><span data-stu-id="e7d94-p108">Where  *TPDName*  is the name you want to use for the TPD. For example, "Contoso North American TPD".</span></span> 
    
5. <span data-ttu-id="e7d94-156">Чтобы убедиться, что вы успешно настроили организации Office 365 с помощью службы управления правами Azure, запустите командлет [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) с параметром - RMSOnline следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e7d94-156">To verify that you successfully configured your Office 365 organization to use the Azure Rights Management service, run the [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet with the -RMSOnline switch as follows:</span></span> 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    <span data-ttu-id="e7d94-157">Помимо прочего этот командлет проверяет возможность доступа с помощью службы управления правами Azure, файлы для загрузки доверенный домен публикации и проверяет его допустимость.</span><span class="sxs-lookup"><span data-stu-id="e7d94-157">Among other things, this cmdlet checks connectivity with the Azure Rights Management service, downloads the TPD, and checks its validity.</span></span>
    
6. <span data-ttu-id="e7d94-158">Выполните командлет [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) , как показано ниже, чтобы отключить службу управления правами Azure шаблоны, доступные в Outlook в Outlook и веб:</span><span class="sxs-lookup"><span data-stu-id="e7d94-158">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to disable Azure Rights Management templates from being available in Outlook on the web and Outlook:</span></span> 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. <span data-ttu-id="e7d94-159">Выполните командлет [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) следующим образом для включения службы управления правами Azure для вашей организации электронной почты на основе облака и настроить его для использования службы управления правами Azure для шифрования сообщений Office 365:</span><span class="sxs-lookup"><span data-stu-id="e7d94-159">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to enable Azure Rights Management for your cloud-based email organization and configure it to use Azure Rights Management for Office 365 Message Encryption:</span></span> 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. <span data-ttu-id="e7d94-p109">Чтобы убедиться, что вы успешно импортировали TPD и включена служба управления правами Azure, используйте командлет Test-IRMConfiguration для тестирования функции управления правами Azure. Дополнительные сведения см «В примере 1» в [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7d94-p109">To verify that you have successfully imported the TPD and enabled Azure Rights Management, use the Test-IRMConfiguration cmdlet to test Azure Rights Management functionality. For details, see "Example 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span></span>
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a><span data-ttu-id="e7d94-162">У меня есть предыдущей версии OME настройку с помощью управления правами Active Directory Azure защита информации, что делать?</span><span class="sxs-lookup"><span data-stu-id="e7d94-162">I have the previous version of OME set up with Active Directory Rights Management not Azure Information Protection, what do I do?</span></span>
<span data-ttu-id="e7d94-163"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="e7d94-163"></span></span>

<span data-ttu-id="e7d94-p110">Можно продолжить использование существующих правил потока почты шифрования сообщений Office 365 с помощью управления правами Active Directory, но не могут использовать новые возможности OME или настроить. Вместо этого необходимо перенести защита информации Azure. Сведения о миграции и это означает для вашей организации см [AD RMS для защиты информации Azure](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span><span class="sxs-lookup"><span data-stu-id="e7d94-p110">You can continue to use your existing Office 365 Message Encryption mail flow rules with Active Directory Rights Management, but you can't configure or use the new OME capabilities. Instead, you need to migrate to Azure Information Protection. For information about migration and what this means for your organization, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="e7d94-167">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e7d94-167">Next steps</span></span>
<span data-ttu-id="e7d94-168"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="e7d94-168"></span></span>

<span data-ttu-id="e7d94-169">После выполнения программы установки службы управления правами Azure, если вы хотите включить новые возможности OME, просматривать [настроить новые возможности шифрования сообщений Office 365, построенные защита информации Azure.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span><span class="sxs-lookup"><span data-stu-id="e7d94-169">Once you've completed Azure Rights Management setup, if you want to enable the new OME capabilities, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span></span>
  
<span data-ttu-id="e7d94-170">После настройки вашей организации для использования новых возможностей OME, вы готовы к [Определение правил поток обработки почты для защиты сообщений электронной почты с новыми возможностями OME](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="e7d94-170">After you've set up your organization to use the new OME capabilities, you're ready to [Define mail flow rules to protect email messages with new OME capabilities](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="e7d94-171">См. также:</span><span class="sxs-lookup"><span data-stu-id="e7d94-171">Related topics</span></span>
<span data-ttu-id="e7d94-172"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="e7d94-172"></span></span>

[<span data-ttu-id="e7d94-173">Шифрование в Office 365</span><span class="sxs-lookup"><span data-stu-id="e7d94-173">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="e7d94-174">Технические сведения о шифровании в Office 365</span><span class="sxs-lookup"><span data-stu-id="e7d94-174">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="e7d94-175">Что такое служба управления правами Azure?</span><span class="sxs-lookup"><span data-stu-id="e7d94-175">What is Azure Rights Management?</span></span>](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  

