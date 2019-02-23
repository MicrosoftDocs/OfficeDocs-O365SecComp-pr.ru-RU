---
title: Настройка Microsoft Azure AD Rights Management для предыдущей версии шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/30/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2cba47b3-f09e-4911-9207-ac056fcb9db7
description: Предыдущая версия шифрования сообщений Office 365 зависит от Microsoft Azure Rights Management (ранее известной как Windows Azure Active Directory Rights Management).
ms.openlocfilehash: 89b86035f57699457c86fefb49888b8428f4e01c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214379"
---
# <a name="set-up-azure-rights-management-for-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="68233-103">Настройка Microsoft Azure AD Rights Management для предыдущей версии шифрования сообщений Office 365</span><span class="sxs-lookup"><span data-stu-id="68233-103">Set up Azure Rights Management for the previous version of Office 365 Message Encryption</span></span>

<span data-ttu-id="68233-104">В этом разделе описываются действия, которые необходимо выполнить, чтобы активировать и затем настроить Azure Rights Management (RMS), часть Azure Information Protection для использования с предыдущей версией Office 365 Message encryption (OME).</span><span class="sxs-lookup"><span data-stu-id="68233-104">This topic describes the steps you need to follow in order to activate and then set up Azure Rights Management (RMS), part of Azure Information Protection, for use with the previous version of Office 365 Message Encryption (OME).</span></span>

## <a name="this-article-only-applies-to-the-previous-version-of-ome"></a><span data-ttu-id="68233-105">Эта статья относится только к предыдущей версии OME</span><span class="sxs-lookup"><span data-stu-id="68233-105">This article only applies to the previous version of OME</span></span>
<span data-ttu-id="68233-p101">Если вы еще не переместили организацию Office 365 в новые возможности OME, но вы уже развернули OME, то сведения, приведенные в этой статье, применимы к вашей организации. Корпорация Майкрософт рекомендует создавать план для перехода на новые возможности OME, как только она будет приемлема для вашей организации. Инструкции приведены в разделе [Настройка новых возможностей шифрования сообщений Office 365](set-up-new-message-encryption-capabilities.md). Если вы хотите узнать больше о том, как новые возможности работают первыми, ознакомьтесь со статьей [Office 365 Message Encryption](ome.md). В оставшейся части этой статьи рассматривается поведение OME перед выпуском новых возможностей OME.</span><span class="sxs-lookup"><span data-stu-id="68233-p101">If you haven't yet moved your Office 365 organization to the new OME capabilities, but you have already deployed OME, then the information in this article applies to your organization. Microsoft recommends that you make a plan to move to the new OME capabilities as soon as it is reasonable for your organization. For instructions, see [Set up new Office 365 Message Encryption capabilities](set-up-new-message-encryption-capabilities.md). If you want to find out more about how the new capabilities work first, see [Office 365 Message Encryption](ome.md). The rest of this article refers to OME behavior before the release of the new OME capabilities.</span></span>

## <a name="prerequisites-for-using-the-previous-version-of-office-365-message-encryption"></a><span data-ttu-id="68233-111">Необходимые условия для использования предыдущей версии Office 365 шифрования сообщений</span><span class="sxs-lookup"><span data-stu-id="68233-111">Prerequisites for using the previous version of Office 365 Message Encryption</span></span>
<span data-ttu-id="68233-112"><a name="warmprereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="68233-112"></span></span>

<span data-ttu-id="68233-p102">Шифрование сообщений Office 365 (OME), в том числе IRM, зависит от управления правами Azure (Azure RMS). Azure RMS — это технология защиты, используемая службой Azure Information Protection. Чтобы использовать OME, ваша организация Office 365 должна включать подписку на Exchange Online или Exchange Online Protection, которая, в свою очередь, включает подписку на Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="68233-p102">Office 365 Message Encryption (OME), including IRM, depends on Azure Rights Management (Azure RMS). Azure RMS is the protection technology used by Azure Information Protection. To use OME, your Office 365 organization must include an Exchange Online or Exchange Online Protection subscription that, in turn, includes an Azure Rights Management subscription.</span></span>
  
- <span data-ttu-id="68233-116">Если вы не знаете, что включает подписка, ознакомьтесь со статьей описание службы Exchange Online для [политики сообщений, восстановления и соответствия требованиям](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span><span class="sxs-lookup"><span data-stu-id="68233-116">If you're not sure of what your subscription includes, see the Exchange Online service descriptions for [Message Policy, Recovery, and Compliance](https://technet.microsoft.com/library/exchange-online-message-policy-recovery-and-compliance.aspx).</span></span>

- <span data-ttu-id="68233-117">Если у вас нет подписки Azure RMS для Exchange Online или Exchange Online Protection, вы должны приобрести подписку и активировать ее первым.</span><span class="sxs-lookup"><span data-stu-id="68233-117">If you don't have an Azure RMS subscription for Exchange Online or Exchange Online Protection, you must purchase a subscription and activate it first.</span></span>

    <span data-ttu-id="68233-p103">Сведения о приобретении подписки на Azure Rights Management можно найти в статье [Управление правами Azure](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). В следующем разделе представлены сведения об активации Azure Rights Management.</span><span class="sxs-lookup"><span data-stu-id="68233-p103">For information about purchasing a subscription to Azure Rights Management, see [Azure Rights Management](https://portal.office.com/Signup/MainSignUp15.aspx?&amp;OfferId=9DF77AF9-DAAE-4d51-8E0E-EEEADD4866B8&amp;dl=RIGHTSMANAGEMENT). The next section gives you information about activating Azure Rights Management.</span></span>

- <span data-ttu-id="68233-120">Если у вас есть служба управления правами Azure, но она не настроена для Exchange Online или Exchange Online Protection, в этой статье описывается активация службы управления правами Azure, а затем описывается лучший способ настройки OME для работы с управлением правами Azure.</span><span class="sxs-lookup"><span data-stu-id="68233-120">If you have Azure Rights Management but it's not set up for Exchange Online or Exchange Online Protection, this article explains how to activate Azure Rights Management and then the describes the best way to set up OME to work with Azure Rights Management.</span></span>

- <span data-ttu-id="68233-p104">Если вы уже настроили OME для работы с управлением правами Azure для Exchange Online или Exchange Online Protection, в зависимости от того, как вы настроили ее, вы можете сразу приступить к использованию OME и новых возможностей. В этой статье объясняется, как определить, правильно ли настроен OME, что делать, если требуется изменить настройку, а что произойдет, если вы отказаться от изменения настроек. Например, чтобы использовать новые возможности, необходимо использовать Azure RMS с OME. Вы не можете использовать новые возможности с локальной службой управления правами Active Directory.</span><span class="sxs-lookup"><span data-stu-id="68233-p104">If you've already set up OME to work with Azure Rights Management for Exchange Online or Exchange Online Protection, depending on how you set it up, you may be ready to start using OME and its new capabilities right away. This article explains how to determine if you've set OME up correctly, what to do if you need to change your setup, and what happens if you choose not to change your setup. For example, in order to use the new capabilities, you must use Azure RMS with OME. You can't use the new capabilities with an on-premises Active Directory RMS.</span></span>

## <a name="activate-azure-rights-management-for--the-previous-version-of-ome-in-office-365"></a><span data-ttu-id="68233-125">Активация службы управления правами Azure для предыдущей версии OME в Office 365</span><span class="sxs-lookup"><span data-stu-id="68233-125">Activate Azure Rights Management for  the previous version of OME in Office 365</span></span>

<span data-ttu-id="68233-p105">Необходимо активировать управление правами Azure, чтобы пользователи в организации могли применять защиту информации к отправляемым им сообщениям, а также открывать сообщения и файлы, защищенные службой управления правами Azure. Инструкции см в разделе [Активация службы управления правами Azure](https://go.microsoft.com/fwlink/p/?LinkId=525775). После завершения активации вернитесь сюда и продолжайте выполнение задач, описанных в этой статье.</span><span class="sxs-lookup"><span data-stu-id="68233-p105">You need to activate Azure Rights Management so that the users in your organization can apply information protection to messages that they send, and open messages and files that have been protected by the Azure Rights Management service. For instructions, see [Activating Azure Rights Management](https://go.microsoft.com/fwlink/p/?LinkId=525775). Once you've completed the activation, return here and continue with the tasks in this article.</span></span>
  
## <a name="set-up-the-previous-version-of-ome-to-use-azure-rms-by-importing-trusted-publishing-domains-tpds"></a><span data-ttu-id="68233-129">Настройка предыдущей версии OME для использования Azure RMS путем импорта доверенных доменов публикации (TPD)</span><span class="sxs-lookup"><span data-stu-id="68233-129">Set up the previous version of OME to use Azure RMS by importing trusted publishing domains (TPDs)</span></span>

<span data-ttu-id="68233-p106">TPD — это XML-файл, который содержит сведения о параметрах управления правами организации. Например, TPD содержит сведения о сертификате лицензиара сервера (лицензиар), используемом для подписи и шифрования сертификатов и лицензий, URL-адресов, используемых для лицензирования и публикации, и т. д. Вы импортируете TPD в организацию Office 365 с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68233-p106">A TPD is an XML file that contains information about your organization's rights management settings. For example, the TPD contains information about the server licensor certificate (SLC) used for signing and encrypting certificates and licenses, the URLs used for licensing and publishing, and so on. You import the TPD into your Office 365 organization by using Windows PowerShell.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="68233-p107">Ранее вы можете импортировать TPD из службы управления правами Active Directory (AD RMS) в организацию Office 365. Тем не менее, это предотвратит использование новых возможностей OME и не рекомендуется. Если ваша организация Office 365 в данный момент настроена таким образом, корпорация Майкрософт рекомендует создать план для миграции из локальной службы управления правами Active Directory в облачную службу Azure Information Protection. Дополнительные сведения см. [в статье миграция из AD RMS в Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). Вы не сможете использовать новые возможности OME, пока миграция не будет завершена в Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="68233-p107">Previously, you could choose to import TPDs from the Active Directory Rights Management service (AD RMS) into your Office 365 organization. However, doing so will prevent you from using the new OME capabilities and is not recommended. If your Office 365 organization is currently configured this way, Microsoft recommends that you create a plan to migrate from your on-premises Active Directory RMS to cloud-based Azure Information Protection. For more information, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms). You will not be able to use the new OME capabilities until you have completed the migration to Azure Information Protection.</span></span>
  
 <span data-ttu-id="68233-138">**Импорт TPD из службы управления правами Azure**</span><span class="sxs-lookup"><span data-stu-id="68233-138">**To import TPDs from Azure RMS**</span></span>
  
1. <span data-ttu-id="68233-139">[Подключитесь к Exchange Online с помощью удаленной оболочки PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="68233-139">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="68233-140">Выберите URL-адрес для общего доступа к ключам, соответствующий географическому расположению организации Office 365:</span><span class="sxs-lookup"><span data-stu-id="68233-140">Choose the key-sharing URL that corresponds to your Office 365 organization's geographic location:</span></span>

|<span data-ttu-id="68233-141">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="68233-141">**Location**</span></span>|<span data-ttu-id="68233-142">**URL-адрес расположения для общего доступа к ключам**</span><span class="sxs-lookup"><span data-stu-id="68233-142">**Key sharing location URL**</span></span>|
|:-----|:-----|
|<span data-ttu-id="68233-143">Северная Америка</span><span class="sxs-lookup"><span data-stu-id="68233-143">North America</span></span>  <br/> |https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="68233-144">Европейский Союз</span><span class="sxs-lookup"><span data-stu-id="68233-144">European Union</span></span>  <br/> |https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="68233-145">Азия</span><span class="sxs-lookup"><span data-stu-id="68233-145">Asia</span></span>  <br/> |https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="68233-146">Южная Америка</span><span class="sxs-lookup"><span data-stu-id="68233-146">South America</span></span>  <br/> |https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
|<span data-ttu-id="68233-147">Office 365 для государственных учреждений (облако сообщества госучреждений)</span><span class="sxs-lookup"><span data-stu-id="68233-147">Office 365 for Government (Government Community Cloud)</span></span>  <br/> <span data-ttu-id="68233-148">Это расположение для общего доступа к ключам RMS зарезервировано для клиентов, которые приобрели Office 365 для государственных учреждений.</span><span class="sxs-lookup"><span data-stu-id="68233-148">This RMS key-sharing location is reserved for customers who have purchased Office 365 for Government SKUs.</span></span>  <br/> |https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc  <br/> |
   
3. <span data-ttu-id="68233-149">Настройте расположение для общего доступа к ключам, выполнив командлет [Set – IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="68233-149">Configure the key-sharing location by running the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.160%29.aspx) cmdlet as follows:</span></span> 
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "<RMSKeySharingURL >"
  ```

    <span data-ttu-id="68233-150">Например, чтобы настроить расположение для общего доступа к ключам, если ваша организация находится в Северной Америке:</span><span class="sxs-lookup"><span data-stu-id="68233-150">For example, to configure the key sharing location if your organization is located in North America:</span></span>
    
  ```
  Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
  ```

4. <span data-ttu-id="68233-151">Выполните командлет [Import – RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) с параметром – рмсонлине, чтобы импортировать TPD из службы управления правами Azure:</span><span class="sxs-lookup"><span data-stu-id="68233-151">Run the [Import-RMSTrustedPublishingDomain](https://technet.microsoft.com/library/jj200724%28v=exchg.150%29.aspx) cmdlet with the -RMSOnline switch to import the TPD from Azure Rights Management:</span></span> 
    
  ```
  Import-RMSTrustedPublishingDomain -RMSOnline -Name "<TPDName> "
  ```

    <span data-ttu-id="68233-p108">Где *тпднаме* — это имя, которое вы хотите использовать для TPD. Например, "Contoso Северная Америка TPD".</span><span class="sxs-lookup"><span data-stu-id="68233-p108">Where  *TPDName*  is the name you want to use for the TPD. For example, "Contoso North American TPD".</span></span> 
    
5. <span data-ttu-id="68233-154">Чтобы убедиться, что ваша организация Office 365 успешно настроена на использование службы управления правами Azure, запустите командлет [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) с параметром-рмсонлине следующим образом:</span><span class="sxs-lookup"><span data-stu-id="68233-154">To verify that you successfully configured your Office 365 organization to use the Azure Rights Management service, run the [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.160%29.aspx) cmdlet with the -RMSOnline switch as follows:</span></span> 
    
  ```
  Test-IRMConfiguration -RMSOnline
  ```

    <span data-ttu-id="68233-155">Помимо прочего, этот командлет проверяет возможность подключения к службе управления правами Azure, загружает TPD и проверяет его допустимость.</span><span class="sxs-lookup"><span data-stu-id="68233-155">Among other things, this cmdlet checks connectivity with the Azure Rights Management service, downloads the TPD, and checks its validity.</span></span>
    
6. <span data-ttu-id="68233-156">Выполните командлет [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) , как показано ниже, чтобы отключить доступ к шаблонам управления правами Azure в Outlook в Интернете и Outlook:</span><span class="sxs-lookup"><span data-stu-id="68233-156">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to disable Azure Rights Management templates from being available in Outlook on the web and Outlook:</span></span> 
    
  ```
  Set-IRMConfiguration -ClientAccessServerEnabled $false
  ```

7. <span data-ttu-id="68233-157">Выполните командлет [Set – IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) , как показано ниже, чтобы включить управление правами Azure для облачной организации электронной почты и настроить его для использования службы управления правами Azure для шифрования сообщений Office 365:</span><span class="sxs-lookup"><span data-stu-id="68233-157">Run the [Set-IRMConfiguration](https://technet.microsoft.com/library/dd979792%28v=exchg.150%29.aspx) cmdlet as follows to enable Azure Rights Management for your cloud-based email organization and configure it to use Azure Rights Management for Office 365 Message Encryption:</span></span> 
    
  ```
  Set-IRMConfiguration -InternalLicensingEnabled $true
  ```

8. <span data-ttu-id="68233-p109">Чтобы убедиться, что вы успешно импортировали TPD и включили управление правами Azure, используйте командлет Test-IRMConfiguration для проверки функции управления правами Azure. Дополнительные сведения: "Пример 1" в разделе [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="68233-p109">To verify that you have successfully imported the TPD and enabled Azure Rights Management, use the Test-IRMConfiguration cmdlet to test Azure Rights Management functionality. For details, see "Example 1" in [Test-IRMConfiguration](https://technet.microsoft.com/library/dd979798%28v=exchg.150%29.aspx).</span></span>
    
## <a name="i-have-the-previous-version-of-ome-set-up-with-active-directory-rights-management-not-azure-information-protection-what-do-i-do"></a><span data-ttu-id="68233-160">В предыдущей версии OME настроено управление правами Active Directory, а не Azure Information Protection, что делать?</span><span class="sxs-lookup"><span data-stu-id="68233-160">I have the previous version of OME set up with Active Directory Rights Management not Azure Information Protection, what do I do?</span></span>
<span data-ttu-id="68233-161"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="68233-161"></span></span>

<span data-ttu-id="68233-p110">Вы можете продолжать использовать существующие правила обработки почты для шифрования сообщений Office 365 с помощью управления правами Active Directory, но вы не можете настраивать или использовать новые возможности OME. Вместо этого необходимо выполнить миграцию в Azure Information Protection. Сведения о миграции и том, что это означает для вашей организации, можно узнать [в статье Миграция с AD RMS на Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span><span class="sxs-lookup"><span data-stu-id="68233-p110">You can continue to use your existing Office 365 Message Encryption mail flow rules with Active Directory Rights Management, but you can't configure or use the new OME capabilities. Instead, you need to migrate to Azure Information Protection. For information about migration and what this means for your organization, see [Migrating from AD RMS to Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/prepare-environment-adrms).</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="68233-165">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="68233-165">Next steps</span></span>
<span data-ttu-id="68233-166"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="68233-166"></span></span>

<span data-ttu-id="68233-167">После завершения настройки управления правами Azure, если вы хотите включить новые возможности OME, ознакомьтесь со статьей [Настройка новых возможностей шифрования сообщений Office 365, созданных на основе Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span><span class="sxs-lookup"><span data-stu-id="68233-167">Once you've completed Azure Rights Management setup, if you want to enable the new OME capabilities, see [Set up new Office 365 Message Encryption capabilities built on top of Azure Information Protection.](https://support.office.com/article/7ff0c040-b25c-4378-9904-b1b50210d00e)</span></span>
  
<span data-ttu-id="68233-168">После настройки организации для использования новых возможностей OME вы можете [определить правила обработки почты для защиты сообщений электронной почты с помощью новых возможностей OME](define-mail-flow-rules-to-encrypt-email.md).</span><span class="sxs-lookup"><span data-stu-id="68233-168">After you've set up your organization to use the new OME capabilities, you're ready to [Define mail flow rules to protect email messages with new OME capabilities](define-mail-flow-rules-to-encrypt-email.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="68233-169">Связанные статьи</span><span class="sxs-lookup"><span data-stu-id="68233-169">Related topics</span></span>
<span data-ttu-id="68233-170"><a name="importTPDs"> </a></span><span class="sxs-lookup"><span data-stu-id="68233-170"></span></span>

[<span data-ttu-id="68233-171">Шифрование в Office 365</span><span class="sxs-lookup"><span data-stu-id="68233-171">Encryption in Office 365</span></span>](encryption.md)
  
[<span data-ttu-id="68233-172">Технические сведения о шифровании в Office 365</span><span class="sxs-lookup"><span data-stu-id="68233-172">Technical reference details about encryption in Office 365</span></span>](technical-reference-details-about-encryption.md)
  
[<span data-ttu-id="68233-173">Что такое управление правами Azure?</span><span class="sxs-lookup"><span data-stu-id="68233-173">What is Azure Rights Management?</span></span>](https://docs.microsoft.com/information-protection/understand-explore/what-is-azure-rms)
  

