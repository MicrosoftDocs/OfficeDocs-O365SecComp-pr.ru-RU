---
title: Контроль данных в Office 365 с помощью ключа клиента
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/1/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
ms.collection:
- M365-security-compliance
description: Узнайте, как настроить ключ клиента для Office 365 для Exchange Online, Skype для бизнеса, SharePoint Online и OneDrive для бизнеса. С помощью ключа клиента вы можете управлять ключами шифрования вашей организации, а затем настроить Office 365 на их использование для шифрования данных на REST в центрах обработки данных Майкрософт.
ms.openlocfilehash: 219ddb94727cd2b708f734a77a8397b3bc3f1064
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296672"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="91338-104">Контроль данных в Office 365 с помощью ключа клиента</span><span class="sxs-lookup"><span data-stu-id="91338-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="91338-p102">С помощью ключа клиента вы можете управлять ключами шифрования вашей организации, а затем настроить Office 365 на их использование для шифрования данных на REST в центрах обработки данных Майкрософт. Другими словами, ключ клиента позволяет клиентам добавлять к ним слой шифрования с их ключами. Данные на REST включают данные из Exchange Online и Skype для бизнеса, которые хранятся в почтовых ящиках и файлах, хранящихся в SharePoint Online и OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="91338-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. In other words, Customer Key allows customers to add a layer of encryption that belongs to them, with their keys. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="91338-p103">Вы должны настроить Azure, прежде чем вы сможете использовать ключ клиента для Office 365. В этом разделе описываются действия, которые необходимо выполнить, чтобы создать и настроить необходимые ресурсы Azure, а затем пошаговые инструкции по настройке ключа клиента в Office 365. После завершения установки Azure Определите политику и, следовательно,, какие ключи необходимо назначить почтовым ящикам и файлам в Организации. ПоЧтовые ящики и файлы, для которых не назначена политика, будут использовать политики шифрования, контролируемые и управляемые корпорацией Майкрософт. Для получения дополнительных сведений о ключе клиента или общем обзоре обратитесь к [разделу клиент для Office 365 вопросы и ответы](service-encryption-with-customer-key-faq.md).</span><span class="sxs-lookup"><span data-stu-id="91338-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="91338-p104">Мы настоятельно рекомендуем следовать рекомендациям, приведенным в этой статье. Они вызываются в качестве **Совета** и **важны**. Ключ клиента позволяет контролировать корневые ключи шифрования, область действия которых может быть такой же, как и вся Организация. Это означает, что ошибки, выполненные с помощью этих ключей, могут оказать широкое влияние и могут привести к перерыву в обслуживании или потере данных ирревокабле.</span><span class="sxs-lookup"><span data-stu-id="91338-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="91338-117">Прежде чем приступить к настройке ключа клиента</span><span class="sxs-lookup"><span data-stu-id="91338-117">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="91338-118"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-118"></span></span>

<span data-ttu-id="91338-p105">Прежде чем приступить к работе, убедитесь, что у вас есть подходящие лицензии для вашей организации. Ключ клиента в Office 365 предлагается в Office 365 а или в расширенном соответствии с КОНФИГУРАЦИей.</span><span class="sxs-lookup"><span data-stu-id="91338-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="91338-p106">Затем, чтобы ознакомиться с основными понятиями и процедурами, описанными в этом разделе, ознакомьтесь с документацией по [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . Кроме того, ознакомьтесь с терминами, используемыми в Azure, например, " [клиент](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant)".</span><span class="sxs-lookup"><span data-stu-id="91338-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="91338-123">Чтобы оставить отзыв о ключе клиента, в том числе документации, отправьте свои идеи, предложения и перспективы в customerkeyfeedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="91338-123">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="91338-124">Общие сведения о настройке ключа клиента для Office 365</span><span class="sxs-lookup"><span data-stu-id="91338-124">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="91338-125"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-125"></span></span>

<span data-ttu-id="91338-p107">Чтобы настроить ключ клиента, выполните указанные ниже действия. В оставшейся части этого раздела приводятся подробные инструкции по каждой задаче или ссылки на дополнительные сведения для каждого этапа процесса.</span><span class="sxs-lookup"><span data-stu-id="91338-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="91338-128">**В Azure и Microsoft FastTrack:**</span><span class="sxs-lookup"><span data-stu-id="91338-128">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="91338-p108">Для выполнения большинства этих задач необходимо удаленно подключиться к Azure PowerShell. Для достижения лучших результатов используйте Azure PowerShell версии 4.4.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="91338-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="91338-131">Создание двух новых подписок Azure</span><span class="sxs-lookup"><span data-stu-id="91338-131">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="91338-132">Регистрация подписок Azure для использования обязательного периода хранения</span><span class="sxs-lookup"><span data-stu-id="91338-132">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="91338-133">Регистрация может занять от одного до пяти рабочих дней.</span><span class="sxs-lookup"><span data-stu-id="91338-133">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="91338-134">Отправьте запрос на активацию ключа клиента для Office 365</span><span class="sxs-lookup"><span data-stu-id="91338-134">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="91338-p109">После создания двух новых подписок Azure вам потребуется отправить соответствующий запрос клиентского ключа, заполнив веб-форму, размещенную на портале Microsoft FastTrack. **Команда FastTrack не предоставляет помощь с ключом клиента. Office просто использует портал FastTrack, чтобы разрешить отправку формы и помощь в отслеживании соответствующих предложений для ключа клиента**.</span><span class="sxs-lookup"><span data-stu-id="91338-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. **The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key**.</span></span>
  
<span data-ttu-id="91338-p110">После того как вы отправили ключ клиента, корпорация Майкрософт просматривает запрос и уведомляет вас, когда можете продолжить выполнение всех задач программы установки. Этот процесс может занять до пяти рабочих дней.</span><span class="sxs-lookup"><span data-stu-id="91338-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="91338-139">Создание расширенного Azure Key Vault в каждой подписке</span><span class="sxs-lookup"><span data-stu-id="91338-139">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="91338-140">Назначение разрешений для каждого хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="91338-140">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="91338-141">Включение и подтверждение обратимого удаления в ключевых хранилищах</span><span class="sxs-lookup"><span data-stu-id="91338-141">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="91338-142">Добавление ключа в каждое основное хранилище с помощью создания или импорта ключа</span><span class="sxs-lookup"><span data-stu-id="91338-142">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="91338-143">Проверка уровня восстановления ключей</span><span class="sxs-lookup"><span data-stu-id="91338-143">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="91338-144">Резервное копирование Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-144">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="91338-145">Проверка параметров конфигурации Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-145">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="91338-146">Получение URI для каждого ключа Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-146">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="91338-147">**В Office 365:**</span><span class="sxs-lookup"><span data-stu-id="91338-147">**In Office 365:**</span></span>
  
<span data-ttu-id="91338-148">Exchange Online и Skype для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="91338-148">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="91338-149">Создание политики шифрования данных (DEP) для использования в Exchange Online и Skype для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-149">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="91338-150">Назначение функции предотвращения выполнения данных для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="91338-150">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="91338-151">Проверка шифрования почтового ящика</span><span class="sxs-lookup"><span data-stu-id="91338-151">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="91338-152">SharePoint Online и OneDrive для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="91338-152">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="91338-153">Создание политики шифрования данных (DEP) для всех географических регионов SharePoint Online и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-153">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="91338-154">Проверка шифрования сайтов групп, сайтов групп и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-154">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="91338-155">Выполнение задач в Azure Key Vault и Microsoft FastTrack для клиентского ключа</span><span class="sxs-lookup"><span data-stu-id="91338-155">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="91338-156"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-156"></span></span>

<span data-ttu-id="91338-p111">Выполните эти задачи в Azure Key Vault, чтобы настроить ключ клиента для Office 365. Вам потребуется выполнить эти действия независимо от того, хотите ли вы настроить ключ клиента для Exchange Online и Skype для бизнеса или SharePoint Online и OneDrive для бизнеса или для всех поддерживаемых служб в Office 365.</span><span class="sxs-lookup"><span data-stu-id="91338-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="91338-159">Создание двух новых подписок Azure</span><span class="sxs-lookup"><span data-stu-id="91338-159">Create two new Azure subscriptions</span></span>
<span data-ttu-id="91338-160"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-160"></span></span>

<span data-ttu-id="91338-p112">Для ключа клиента требуются две подписки Azure. Рекомендуется создавать новые подписки Azure для использования с ключом клиента. Ключи Azure Key Vault могут быть авторизованы только для приложений в том же клиенте Azure Active Directory (AAD), поэтому необходимо создать новые подписки, используя тот же клиент Azure AD, который используется в организации Office 365, в которой будет назначена ДЕПС. Например, с помощью рабочей или учебной учетной записи, имеющей права глобального администратора в организации Office 365. Подробное описание действий приведено в разделе [Регистрация в Azure в качестве организации](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span><span class="sxs-lookup"><span data-stu-id="91338-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="91338-p113">Для ключа клиента требуются два ключа для каждой политики шифрования данных (DEP). Чтобы добиться этого, необходимо создать две подписки Azure. Кроме того, корпорация Майкрософт рекомендует, чтобы отдельные члены вашей организации настроили один ключ в каждой подписке. Кроме того, эти подписки Azure следует использовать только для управления ключами шифрования для Office 365. Это позволяет защитить организацию, если один из операторов случайно, намеренно или злонамеренно удаляет или случайно управляет ключами, для которых они отвечают.</span><span class="sxs-lookup"><span data-stu-id="91338-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="91338-p114">Рекомендуется настроить новые подписки Azure, которые используются исключительно для управления ресурсами Azure Key Vault для использования с ключом клиента. Количество подписок Azure, которые можно создать для Организации, не ограничено. Следуйте приведенным ниже рекомендациям, чтобы свести к минимуму влияние человеческих ошибок, помогая управлять ресурсами, используемыми ключом клиента.</span><span class="sxs-lookup"><span data-stu-id="91338-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="91338-174">Отправьте запрос на активацию ключа клиента для Office 365</span><span class="sxs-lookup"><span data-stu-id="91338-174">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="91338-175"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-175"></span></span>

<span data-ttu-id="91338-p115">После выполнения действий Azure вам потребуется отправить запрос на предоставление заявки на [портале Microsoft FastTrack](https://fasttrack.microsoft.com/). Когда вы отправили запрос через веб-портал FastTrack, корпорация Майкрософт проверяет данные конфигурации Azure Key Vault и контактные данные, которые вы предоставили. Выбор, который вы задаете в форме создания, относящийся к авторизованным должностным лицам Организации, является критически важным и необходим для завершения регистрации ключей клиентов. Должностные лица Организации, выбранные в форме, будут использоваться для проверки подлинности любого запроса на отзыв и удаление всех ключей, используемых с политикой шифрования данных ключей клиентов. Этот шаг необходимо выполнить один раз, чтобы активировать ключ клиента для Exchange Online и Skype для бизнеса и второй раз активировать ключ клиента для SharePoint Online и OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="91338-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="91338-181">Чтобы предоставить заявку на активацию ключа клиента, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="91338-181">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="91338-182">С помощью рабочей или учебной учетной записи, имеющей разрешения глобального администратора в организации Office 365, войдите на [портал Microsoft FastTrack](https://fasttrack.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="91338-182">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="91338-183">Войдя в систему, перейдите на **панель мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="91338-183">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="91338-184">Выберите **предложения**и просмотрите список текущих предложений.</span><span class="sxs-lookup"><span data-stu-id="91338-184">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="91338-185">Выберите дополнительные **сведения** о предложении, которое относится к вам:</span><span class="sxs-lookup"><span data-stu-id="91338-185">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="91338-186">**Exchange Online и Skype для бизнеса:** Выберите дополнительные **сведения** в **разделе клиент для Exchange** .</span><span class="sxs-lookup"><span data-stu-id="91338-186">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="91338-187">**SharePoint Online и OneDrive для бизнеса:** Выберите дополнительные **сведения** о **ключе клиента для SharePoint и OneDrive для бизнеса** .</span><span class="sxs-lookup"><span data-stu-id="91338-187">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="91338-188">На странице " **сведения о** соотношении" выберите **создать запрос**.</span><span class="sxs-lookup"><span data-stu-id="91338-188">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="91338-p116">ЗаПолните все необходимые сведения и требуемые сведения в форме "Предложите". Следует уделить особое внимание выбранным должностным лицам Организации, которым требуется авторизоваться для утверждения постоянных и необратимых уничтожений ключей и данных шифрования. Завершив заполнение формы, нажмите кнопку **послать**.</span><span class="sxs-lookup"><span data-stu-id="91338-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="91338-192">Этот процесс может занять до пяти рабочих дней после того, как корпорация Майкрософт уведомит Ваш запрос.</span><span class="sxs-lookup"><span data-stu-id="91338-192">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="91338-193">Перейдите к обязательному разделу срок хранения, приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="91338-193">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="91338-194">Регистрация подписок Azure для использования обязательного периода хранения</span><span class="sxs-lookup"><span data-stu-id="91338-194">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="91338-195"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-195"></span></span>

<span data-ttu-id="91338-p117">Временная или постоянная потеря корневых ключей шифрования может быть очень недостаточной или даже разрушительной для работы службы и может привести к потере данных. По этой причине для ресурсов, используемых с ключом клиента, требуется усиленная защита. Все ресурсы Azure, используемые с механизмами защиты с помощью ключа клиента, выходят за рамки конфигурации по умолчанию. Подписки Azure можно пометить или зарегистрировать таким образом, чтобы предотвратить немедленную и ирревокабле отмену. Это называется регистрацией для обязательного периода хранения. Действия, необходимые для регистрации подписок Azure для обязательного периода хранения, требуют совместной работы с группой Office 365. Этот процесс может занять от одного до пяти рабочих дней. Ранее это было иногда называть "Do not Cancel".</span><span class="sxs-lookup"><span data-stu-id="91338-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="91338-204">Перед обращением к группе Office 365 необходимо выполнить следующие действия для каждой подписки Azure, которая используется с ключом клиента:</span><span class="sxs-lookup"><span data-stu-id="91338-204">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="91338-p118">Войдите в свою подписку на Azure с помощью Azure PowerShell. Инструкции см в разделе [Вход в систему с помощью Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="91338-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="91338-207">Выполните командлет Register – Азурермпровидерфеатуре, чтобы зарегистрировать подписки для использования обязательного периода хранения.</span><span class="sxs-lookup"><span data-stu-id="91338-207">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="91338-p119">Обратитесь в корпорацию Майкрософт, чтобы завершить процесс. Для команды SharePoint и OneDrive для бизнеса свяжитесь с [Spock@microsoft.com](mailto:spock@microsoft.com). Для Exchange Online и Skype для бизнеса обращайтесь в [exock@microsoft.com](mailto:exock@microsoft.com). Соглашение об уровне обслуживания (SLA) для завершения этого процесса составляет пять рабочих дней после того, как корпорация Майкрософт уведомит (и проверит), что вы зарегистрировали свои подписки, чтобы использовать обязательный срок хранения. Включите в свою электронную почту следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="91338-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="91338-213">**Subject**: ключ клиента для \< *полного доменного имени клиента*\></span><span class="sxs-lookup"><span data-stu-id="91338-213">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="91338-214">**Body**: идентификаторы подписок, для которых требуется завершать обязательный срок хранения.</span><span class="sxs-lookup"><span data-stu-id="91338-214">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="91338-215">После получения уведомления от корпорации Майкрософт о завершении регистрации проверьте состояние регистрации, выполнив командлет Get-Азурермпровидерфеатуре следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-215">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="91338-216">После проверки того, что свойство **состояния регистрации** из командлета Get – азурермпровидерфеатуре возвращает значение зарегистрировано \*\*\*\*, выполните следующую команду для завершения процесса:</span><span class="sxs-lookup"><span data-stu-id="91338-216">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="91338-217">Создание расширенного Azure Key Vault в каждой подписке</span><span class="sxs-lookup"><span data-stu-id="91338-217">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="91338-218"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-218"></span></span>

<span data-ttu-id="91338-219">Действия, необходимые для создания хранилища ключей, описаны в статье [Начало работы с Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), в которой описывается установка и запуск Azure PowerShell, подключение к подписке Azure, создание группы ресурсов и создание хранилища ключей в этой Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91338-219">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="91338-p120">При создании хранилища ключей необходимо выбрать значение SKU: Standard или Premium. Стандартное SKU позволяет защищать ключи Azure Key Vault с помощью программного обеспечения — отсутствует защита ключа для аппаратного модуля безопасности (HSM), а Расширенная конфигурация обеспечивает использование Хсмс для защиты ключей основного хранилища. Ключ клиента принимает ключевые хранилища, использующие любой SKU, хотя корпорация Майкрософт настоятельно рекомендует использовать только Premium SKU. Затраты на операции с ключами любого типа одинаковы, поэтому единственная разница в затратах — это затраты на месяц для каждого ключа, защищенного с помощью HSM. Дополнительные сведения: основные сведения о [ценах на хранилище](https://azure.microsoft.com/pricing/details/key-vault/) .</span><span class="sxs-lookup"><span data-stu-id="91338-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="91338-225">Используйте стандартные хранилища ключей Premium и ключи, защищенные с помощью HSM, для рабочих данных, и используйте стандартные хранилища ключей SKU и ключи для тестирования и проверки.</span><span class="sxs-lookup"><span data-stu-id="91338-225">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="91338-p121">Для каждой службы Office 365, с которой будет использоваться ключ клиента, создайте хранилище ключей в каждой из двух созданных подписок Azure. Например, только для Exchange Online и Skype для бизнеса, а также только для SharePoint Online и OneDrive для бизнеса, вы создадите только одну из двух хранилищ. Чтобы включить ключ клиента для Exchange Online и SharePoint Online, вы создадите две пары ключевых хранилищ.</span><span class="sxs-lookup"><span data-stu-id="91338-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="91338-p122">Используйте соглашение об именовании для ключевых хранилищ, которое отражает предполагаемое использование DEP, с которым будут сопоставлены хранилища. Ознакомьтесь с рекомендациями по соглашению об именовании в разделе рекомендации.</span><span class="sxs-lookup"><span data-stu-id="91338-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="91338-p123">Создайте отдельный набор хранилищ для каждой политики шифрования данных. Для Exchange Online область применения политики шифрования данных выбирается при назначении политики почтовому ящику. Почтовый ящик может иметь только одну назначенную политику, и вы можете создать до 50 политик. Для SharePoint Online область применения политики — все данные в Организации в географическом местоположении или в географическом местоположении.</span><span class="sxs-lookup"><span data-stu-id="91338-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="91338-p124">Создание хранилищ ключей также требует создания групп ресурсов Azure, так как для хранилищ ключей требуется емкость хранилища (хотя очень маленькая) и ведение журнала ключей, если этот параметр включен, также создаются хранимые данные. Рекомендуется использовать отдельные администраторы для управления каждой группой ресурсов, а администрирование — с набором администраторов, которые будут управлять всеми связанными ключевыми ресурсами клиента.</span><span class="sxs-lookup"><span data-stu-id="91338-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="91338-p125">Чтобы обеспечить максимальную доступность, ваши ключевые хранилища должны находиться в областях, близких к службе Office 365. Например, если ваша организация Exchange Online находится в Северной Америке, в Северной Америке разместите свои ключевые хранилища. Если ваша организация Exchange Online находится в Европе, разместите свои ключевые хранилища в Европе.</span><span class="sxs-lookup"><span data-stu-id="91338-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="91338-p126">Используйте общий префикс для ключевых хранилищ и включите аббревиатуру использования и области действия ключа и ключей (например, для службы Contoso SharePoint, в которой хранятся хранилища в Северной Америке, возможные комбинации имен — contoso-O365SP-NA-VaultA1 и Contoso — O365SP — NA – VaultA2. Имена хранилищ являются глобально уникальными строками в Azure, поэтому вам может потребоваться попробовать варианты желаемых имен, чтобы они уже были затребованы другими клиентами Azure. С 2017 до июля имена хранилищ не могут быть изменены, поэтому рекомендуется создать план для установки и использовать второй пользователь, чтобы проверить, правильно ли выполнен план.</span><span class="sxs-lookup"><span data-stu-id="91338-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="91338-p127">Если это возможно, создайте хранилища в несвязанных областях. Связанные регионы Azure обеспечивают высокую доступность в доменах отказов служб. Таким образом, региональные пары можно рассматривать как область резервного копирования каждого другого пользователя. Это означает, что ресурс Azure, размещаемый в одном регионе, автоматически подает отказоустойчивость через связанный регион. По этой причине выбор областей для двух хранилищ, используемых в функции DEP, где эти регионы связаны, означает, что используется всего две области доступности. Большинство географических регионов имеют только две области, поэтому еще невозможен выбор несвязанных областей. Если это возможно, выберите два несвязанных региона для двух хранилищ, используемых с DEP. Это выгодно из четырех областей доступности. Дополнительные сведения [: "непрерывНость бизнеса" и "аварийное восстановление" (бкдр): области](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) , связанные с Azure, для текущего списка региональных пар.</span><span class="sxs-lookup"><span data-stu-id="91338-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="91338-252">Назначение разрешений для каждого хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="91338-252">Assign permissions to each key vault</span></span>
<span data-ttu-id="91338-253"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-253"></span></span>

<span data-ttu-id="91338-p128">Для каждого ключевого хранилища необходимо определить три отдельных набора разрешений для ключа клиента в зависимости от реализации. Например, вам потребуется определить один набор разрешений для каждого из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="91338-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="91338-p129">**Администраторы основного хранилища** , которые будут выполнять повседневное управление вашим хранилищем ключей для Организации. Эти задачи включают резервное копирование, создание, получение, импорт, перечисление и восстановление.</span><span class="sxs-lookup"><span data-stu-id="91338-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="91338-p130">Набор разрешений, назначенных администраторам основного хранилища, не включает разрешение на удаление ключей. Это преднамеренное и важное упражнение. Удаление ключей шифрования обычно выполняется, так как это приведет к окончательному уничтожению данных. По умолчанию не предоставляйте это разрешение для администраторов основного хранилища. Вместо этого его можно зарезервировать для участников хранилища ключей и назначить его администратору на краткосрочной основе, только если четко понять, как эти последствия понятны.</span><span class="sxs-lookup"><span data-stu-id="91338-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="91338-p131">Чтобы назначить эти разрешения пользователю в организации Office 365, войдите в свою подписку на Azure с помощью Azure PowerShell. Инструкции см в разделе [Вход в систему с помощью Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span><span class="sxs-lookup"><span data-stu-id="91338-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="91338-265">Выполните командлет Set – Азурермкэйваултакцессполици, чтобы назначить необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="91338-265">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="91338-266">Пример:</span><span class="sxs-lookup"><span data-stu-id="91338-266">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="91338-p132">**Участники хранилища ключей** , которые могут изменять разрешения в самом Azure Key Vault. Эти разрешения необходимо изменить, так как сотрудники оставляют или присоединяются к команде, или в крайне редких случаях, когда администраторам основного хранилища необходимы разрешения на удаление или восстановление ключа. Этому набору участников хранилища ключей должна быть назначена роль " **участник** " в своем хранилище ключей. Эту роль можно назначить с помощью диспетчера ресурсов Azure. Подробное описание действий приведено [в разделе Использование управления доступом на основе ролей для управления доступом к ресурсам подписки Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). Администратор, который создает подписку, имеет этот доступ неявно, а также возможность назначать других администраторов для роли корреспондента.</span><span class="sxs-lookup"><span data-stu-id="91338-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="91338-p133">Если вы планируете использовать ключ клиента в Exchange Online и Skype для бизнеса, вам необходимо предоставить разрешение на Office 365 для использования хранилища ключей от имени Exchange Online и Skype для бизнеса. Аналогичным образом, если вы планируете использовать ключ клиента с SharePoint Online и OneDrive для бизнеса, вам необходимо добавить разрешение для Office 365, чтобы использовать основное хранилище от имени SharePoint Online и OneDrive для бизнеса. Чтобы предоставить разрешение на доступ к Office 365, выполните командлет **Set – азурермкэйваултакцессполици** , используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="91338-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="91338-276">Где:</span><span class="sxs-lookup"><span data-stu-id="91338-276">Where:</span></span>
    
  - <span data-ttu-id="91338-277">*ваултнаме* — имя созданного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="91338-277">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="91338-278">Для Exchange Online и Skype для бизнеса замените *Office 365 AppID* на`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="91338-278">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="91338-279">Для SharePoint Online и OneDrive для бизнеса замените *Office 365 AppID* на`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="91338-279">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="91338-280">Пример: Настройка разрешений для Exchange Online и Skype для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="91338-280">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="91338-281">Пример: Настройка разрешений для SharePoint Online и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-281">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="91338-282">Включение и подтверждение обратимого удаления в ключевых хранилищах</span><span class="sxs-lookup"><span data-stu-id="91338-282">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="91338-283"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-283"></span></span>

<span data-ttu-id="91338-p134">Если вы можете быстро восстановить свои ключи, вы не сможете столкнуться с расширенным отключением службы из-за случайного или злонамеренного удаления ключей. Необходимо включить эту конфигурацию, которая будет называться обратимым удалением, прежде чем можно будет использовать ключи с ключом клиента. Включение обратимого удаления позволяет восстанавливать ключи или хранилища в течение 90 дней с момента удаления без необходимости их восстановления из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="91338-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="91338-287">Чтобы включить обратимое удаление в своих ключевых хранилищах, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="91338-287">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="91338-p135">Войдите в свою подписку на Azure с помощью Windows PowerShell. Инструкции см в разделе [Вход в систему с помощью Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span><span class="sxs-lookup"><span data-stu-id="91338-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="91338-p136">Выполните командлет [Get – азурермкэйваулт](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . В этом примере *ваултнаме* — это имя хранилища ключей, для которого вы включите обратимое удаление:</span><span class="sxs-lookup"><span data-stu-id="91338-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="91338-p137">Подтвердите, что параметр "обратимое удаление" настроен для хранилища ключей, выполнив командлет **Get-азурермкэйваулт** . Если функция обратимого удаления настроена правильно для хранилища ключей, то функция обратимого удаления включена? свойство возвращает значение **true**:</span><span class="sxs-lookup"><span data-stu-id="91338-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="91338-294">Добавление ключа в каждое основное хранилище с помощью создания или импорта ключа</span><span class="sxs-lookup"><span data-stu-id="91338-294">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="91338-295"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-295"></span></span>

<span data-ttu-id="91338-p138">Существует два способа добавления ключей в хранилище ключей Azure; Вы можете создать ключ непосредственно в разделе Vault или импортировать ключ. Создание ключа непосредственно в разделе Vault является менее сложным методом, при этом при импорте ключа предоставляется полный контроль над способом создания ключа.</span><span class="sxs-lookup"><span data-stu-id="91338-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="91338-298">Чтобы создать ключ непосредственно в своем хранилище ключей, выполните командлет [Add – азурекэйваулткэй](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-298">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="91338-299">Где:</span><span class="sxs-lookup"><span data-stu-id="91338-299">Where:</span></span>
  
-  <span data-ttu-id="91338-300">*ваултнаме* это имя хранилища ключей, в котором вы хотите создать ключ.</span><span class="sxs-lookup"><span data-stu-id="91338-300">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="91338-301">*keyName* — это имя, которое вы хотите назначить новому ключу.</span><span class="sxs-lookup"><span data-stu-id="91338-301">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="91338-p139">Для ключей имен используется аналогичное соглашение об именовании, описанное выше для ключевых хранилищ. Таким образом, в средствах, в которых отображается только имя ключа, строка является самоописанием.</span><span class="sxs-lookup"><span data-stu-id="91338-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="91338-304">Если вы планируете защитить ключ с помощью HSM, убедитесь, что в качестве значения параметра _Destination_ указан **HSM** , в противном случае укажите **программное обеспечение**.</span><span class="sxs-lookup"><span data-stu-id="91338-304">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="91338-305">Например:</span><span class="sxs-lookup"><span data-stu-id="91338-305">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="91338-306">Чтобы импортировать ключ непосредственно в хранилище ключей, необходимо наличие модуля безопасности Салес Ншиелд.</span><span class="sxs-lookup"><span data-stu-id="91338-306">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="91338-307">Некоторые организации предпочитают этот подход для определения проверенных ключей, и этот метод также предоставляет следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="91338-307">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="91338-308">Набор средств, используемый для импорта, включает аттестацию из Салес, что ключ обмена ключами (Кек), используемый для шифрования созданного ключа, не экспортируется и создается в подлинном HSM-сервере, изготовленном Салес.</span><span class="sxs-lookup"><span data-stu-id="91338-308">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="91338-p140">Набор инструментов включает аттестацию из Салес, что мир безопасности Azure Key Vault также был создан в подлинном HSM, изготовленном Салес. Эта аттестация удостоверяется в том, что корпорация Майкрософт также использует подлинное оборудование Салес.</span><span class="sxs-lookup"><span data-stu-id="91338-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="91338-p141">Обратитесь к группе безопасности, чтобы определить, требуются ли вышеперечисленные подтверждения. Для получения подробных инструкций по созданию ключа на локальном уровне и его импорту в хранилище ключей ознакомьтесь [со статьей Создание и передача ключей, защищенных с помощью HSM, для Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). С помощью инструкций Azure создайте ключ в каждом хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="91338-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="91338-314">Проверка уровня восстановления ключей</span><span class="sxs-lookup"><span data-stu-id="91338-314">Check the recovery level of your keys</span></span>
<span data-ttu-id="91338-315"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-315"></span></span>

<span data-ttu-id="91338-p142">Для Office 365 требуется, чтобы для подписки на Azure Key Vault было задано значение "не отМенять", а для ключей, используемых ключом клиента, включено "обратимое удаление". Вы можете подтвердить это, изучив уровень восстановления в ключах.</span><span class="sxs-lookup"><span data-stu-id="91338-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="91338-318">Чтобы проверить уровень восстановления ключа, в Azure PowerShell выполните командлет Get – Азурекэйваулткэй следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-318">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="91338-319">Если свойство _Level Recovery_ возвращает что-либо, кроме значения **восстанавливаемого + протектедсубскриптион**, вам потребуется ознакомиться с этой статьей и убедиться в том, что вы выполнили все действия по размещению подписки в списке "не отменять" и на каждом из ваших ключевых хранилищ включено обратимое удаление.</span><span class="sxs-lookup"><span data-stu-id="91338-319">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="91338-320">Резервное копирование Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-320">Backup Azure Key Vault</span></span>
<span data-ttu-id="91338-321"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-321"></span></span>

<span data-ttu-id="91338-p143">Сразу же после создания или изменения ключа выполните резервное копирование и сохранение копий резервной копии, как в Интернете, так и в автономном режиме. Автономные копии не должны подключаться к сети, например, в физическом надежном или коммерческом хранилище. По крайней мере одна копия резервной копии должна храниться в расположении, которое будет доступно в случае аварии. Резервные объекты резервного копирования являются единственным способом восстановления ключевого материала, который должен быть безвозвратно удален или отображаться в неработоспособном виде. Ключи, являющиеся внешними по отношению к Azure Key Vault и импортированные в хранилище ключей Azure, не являются резервными копиями, так как метаданные, необходимые для использования ключа клиента для использования ключа, не существуют с внешним ключом. Для операций восстановления с ключом клиента можно использовать только резервную копию, полученную из Azure Key Vault. Поэтому важно создать резервную копию Azure Key Vault после отправки или создания ключа.</span><span class="sxs-lookup"><span data-stu-id="91338-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="91338-329">Чтобы создать резервную копию ключа Azure Key Vault, выполните командлет [BACKUP – азурекэйваулткэй](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-329">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="91338-330">Убедитесь, что выходной файл использует суффикс `.backup`.</span><span class="sxs-lookup"><span data-stu-id="91338-330">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="91338-p144">Выходной файл, полученный из этого командлета, шифруется и не может использоваться за преДелом Azure Key Vault. Резервное копирование можно восстановить только в подписке Azure, из которой была создана резервная копия.</span><span class="sxs-lookup"><span data-stu-id="91338-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="91338-p145">В качестве выходного файла выберите сочетание имени хранилища и имени ключа. Это сделает имя файла самоописанием. Кроме того, это гарантирует, что имена файлов резервных копий не будут конфликтовать.</span><span class="sxs-lookup"><span data-stu-id="91338-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="91338-336">Пример:</span><span class="sxs-lookup"><span data-stu-id="91338-336">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="91338-337">Проверка параметров конфигурации Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-337">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="91338-338"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-338"></span></span>

<span data-ttu-id="91338-p146">Выполнение проверки перед использованием ключей в функции DEP является необязательным, но настоятельно рекомендуется. В частности, если вы используете шаги для настройки ключей и хранилищ, отличных от описанных в этой статье, необходимо проверить работоспособность ресурсов Azure Key Vault перед настройкой ключа клиента.</span><span class="sxs-lookup"><span data-stu-id="91338-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="91338-341">Чтобы убедиться, что для ключей включены операции Get, Врапкэй и Унврапкэй:</span><span class="sxs-lookup"><span data-stu-id="91338-341">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="91338-342">Выполните командлет [Get – азурермкэйваулт](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-342">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="91338-p147">В выходных данных найдите нужную политику доступа и идентификатор GUID (GUID) в SharePoint Online (GUID) или удостоверение SharePoint Online (GUID). Все три из перечисленных выше разрешений должны отображаться в разделе разрешения для ключей.</span><span class="sxs-lookup"><span data-stu-id="91338-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="91338-345">Если конфигурация политики доступа неверна, выполните командлет Set-Азурермкэйваултакцессполици следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-345">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="91338-346">Например, для Exchange Online и Skype для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="91338-346">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="91338-347">Например, для SharePoint Online и OneDrive для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="91338-347">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="91338-348">Чтобы убедиться, что срок действия для ключей не задан, запустите командлет [Get-азурекэйваулткэй](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-348">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="91338-p148">Ключ клиента не может использовать ключ с истекшим сроком действия, который пытается выполнить операции с истекшим сроком действия, что может привести к сбою службы. Настоятельно рекомендуется, чтобы ключи, используемые с ключом клиента, не были иметь срок действия. Дата окончания срока действия, после установки, не может быть удалена, но ее можно изменить на другую дату. Если необходимо использовать ключ с установленным сроком действия, измените значение срока действия на 12/31/9999. Ключи со сроком действия, для которых задана дата, отличная от 12/31/9999, не проходят проверку Office 365.</span><span class="sxs-lookup"><span data-stu-id="91338-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="91338-354">Чтобы изменить срок действия, для которого задано значение, отличное от 12/31/9999, выполните командлет [Set – азурекэйваулткэйаттрибуте](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-354">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="91338-355">Не устанавливайте даты истечения срока действия ключей шифрования, которые вы используете с ключом клиента.</span><span class="sxs-lookup"><span data-stu-id="91338-355">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="91338-356">Получение URI для каждого ключа Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-356">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="91338-357"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-357"></span></span>

<span data-ttu-id="91338-p149">После выполнения всех действий, описанных в Azure, для настройки собственных хранилищ ключей и добавления ключей, выполните следующую команду, чтобы получить универсальный код ресурса (URI) для ключа в каждом хранилище ключей. Эти URI необходимо использовать при создании и назначении DEP позже, поэтому сохраните эти сведения в надежном месте. Не заБудьте выполнить эту команду один раз для каждого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="91338-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="91338-361">В Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="91338-361">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="91338-362">Office 365: Настройка ключа клиента для Exchange Online и Skype для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-362">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="91338-363"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-363"></span></span>

<span data-ttu-id="91338-p150">Прежде чем приступать к работе, убедитесь, что выполнены все задачи, необходимые для настройки Azure Key Vault. Для получения дополнительных сведений просмотрите [полные задачи в Azure Key Vault и Microsoft FastTrack для ключа клиента](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="91338-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="91338-366">Чтобы настроить ключ клиента для Exchange Online и Skype для бизнеса, вам потребуется выполнить эти действия, используя удаленное подключение к Exchange Online с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91338-366">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="91338-367">Создание политики шифрования данных (DEP) для использования в Exchange Online и Skype для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-367">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="91338-368"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-368"></span></span>

<span data-ttu-id="91338-p151">ФУНКЦИЯ DEP связана с набором ключей, сохраненных в Azure Key Vault. Вы назначаете функцию предотвращения выполнения данных для почтового ящика в Office 365. После этого Office 365 будет использовать ключи, указанные в политике, для шифрования почтового ящика. Для создания функции DEP необходимы ранее полученные URI для хранилища ключей. Чтобы получить инструкции, ознакомьтесь со статьей [Получение URI для каждого ключа Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI) .</span><span class="sxs-lookup"><span data-stu-id="91338-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="91338-p152">Запоминающее! При создании функции DEP необходимо указать два ключа, которые находятся в двух различных хранилищах ключей Azure. Убедитесь, что эти ключи размещены в двух отдельных регионах Azure для обеспечения геоизбыточности.</span><span class="sxs-lookup"><span data-stu-id="91338-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="91338-377">Чтобы создать DEP, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="91338-377">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="91338-378">На локальном компьютере с помощью рабочей или учебной учетной записи, имеющей разрешения глобального администратора в организации Office 365, [подключитесь к Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , открыв Windows PowerShell и выполнив указанную ниже команду.</span><span class="sxs-lookup"><span data-stu-id="91338-378">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="91338-379">В диалоговом окне Запрос учетных данных Windows PowerShell введите сведения о рабочей или учебной учетной записи, нажмите кнопку **ОК**, а затем введите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="91338-379">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="91338-380">Выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="91338-380">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="91338-381">Чтобы создать DEP, используйте командлет New – Dataencryptionpolicy используется, введя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="91338-381">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="91338-382">Где:</span><span class="sxs-lookup"><span data-stu-id="91338-382">Where:</span></span>
    
   -  <span data-ttu-id="91338-p153">*PolicyName* — имя, которое вы хотите использовать для этой политики. Имена не могут содержать пробелы. Например, Уса_маилбоксес.</span><span class="sxs-lookup"><span data-stu-id="91338-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="91338-p154">*Полицидескриптион* — понятное описание политики, с помощью которого вы сможете запомнить, для чего предназначена эта политика. В описание можно включить пробелы. Например, корневой ключ для почтовых ящиков в США и его территориях.</span><span class="sxs-lookup"><span data-stu-id="91338-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="91338-p155">*KeyVaultURI1* — универсальный код ресурса (URI) для первого ключа в политике. Пример: https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span><span class="sxs-lookup"><span data-stu-id="91338-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="91338-p156">*KeyVaultURI2* — универсальный код ресурса (URI) для второго ключа в политике. Пример: https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. РазДеляйте два URI запятыми и пробелом.</span><span class="sxs-lookup"><span data-stu-id="91338-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="91338-394">Пример.</span><span class="sxs-lookup"><span data-stu-id="91338-394">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="91338-395">Назначение функции предотвращения выполнения данных для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="91338-395">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="91338-396"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-396"></span></span>

<span data-ttu-id="91338-p157">Назначьте DEP почтовому ящику с помощью командлета Set — Mailbox. После назначения политики Office 365 может зашифровать почтовый ящик с помощью ключа, указанного в функции DEP.</span><span class="sxs-lookup"><span data-stu-id="91338-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="91338-p158">Где *маилбоксидпараметер* указывает почтовый ящик. Дополнительные сведения о командлете Set — Mailbox приведены в разделе [Set/Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="91338-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="91338-401">Проверка шифрования почтового ящика</span><span class="sxs-lookup"><span data-stu-id="91338-401">Validate mailbox encryption</span></span>
<span data-ttu-id="91338-402"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-402"></span></span>

<span data-ttu-id="91338-p159">Шифрование почтового ящика может занять некоторое время. При первом назначении политики почтовые ящики также должны завершить перемещение из одной базы данных в другую, прежде чем служба сможет зашифровать почтовый ящик. Рекомендуется подождать 72 часов, прежде чем пытаться проверить шифрование после изменения функции DEP или при первом назначении функции защиты почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="91338-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="91338-406">Используйте командлет Get-MailboxStatistics, чтобы определить, зашифрован ли почтовый ящик.</span><span class="sxs-lookup"><span data-stu-id="91338-406">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="91338-407">Свойство IsFalse возвращает значение **true** , если почтовый ящик зашифрован, и значение **false** , если почтовый ящик не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="91338-407">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="91338-p160">Время, в течение которого перемещаются почтовые ящики, зависит от количества почтовых ящиков, для которых была назначена функция DEP в первый раз, а также от размера почтовых ящиков. Если почтовые ящики не шифруются по прошествии недели с момента назначения функции DEP, запустите командлет New – MoveRequest, чтобы переместить почтовые ящики в незашифрованные почтовые ящики.</span><span class="sxs-lookup"><span data-stu-id="91338-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="91338-410">Office 365: Настройка ключа клиента для SharePoint Online и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-410">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="91338-411"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-411"></span></span>

<span data-ttu-id="91338-p161">Прежде чем приступать к работе, убедитесь, что выполнены все задачи, необходимые для настройки Azure Key Vault. Для получения дополнительных сведений просмотрите [полные задачи в Azure Key Vault и Microsoft FastTrack для ключа клиента](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="91338-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="91338-414">Чтобы настроить ключ клиента для SharePoint Online и OneDrive для бизнеса, вам потребуется выполнить эти действия, используя удаленное подключение к SharePoint Online с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91338-414">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="91338-415">Создание политики шифрования данных (DEP) для всех географических регионов SharePoint Online и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-415">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="91338-416"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-416"></span></span>

<span data-ttu-id="91338-p162">ФУНКЦИЯ DEP связана с набором ключей, сохраненных в Azure Key Vault. ФУНКЦИЯ DEP применяется ко всем данным в одном географическом местоположении, также называемом географическим. Если вы используете функцию поддержки нескольких регионов в Office 365 (в настоящее время находится в предварительной версии), вы можете создать функцию DEP для каждого из них. Если вы не используете поддержку нескольких регионов, вы можете создать единую функцию DEP в Office 365 для использования с SharePoint Online и OneDrive для бизнеса. После этого Office 365 будет использовать ключи, указанные в функции DEP, для шифрования данных в этой географической папке. Для создания функции DEP необходимы ранее полученные URI для хранилища ключей. Чтобы получить инструкции, ознакомьтесь со статьей [Получение URI для каждого ключа Azure Key Vault](controlling-your-data-using-customer-key.md#GetKeyURI) .</span><span class="sxs-lookup"><span data-stu-id="91338-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="91338-p163">Запоминающее! При создании функции DEP необходимо указать два ключа, которые находятся в двух различных хранилищах ключей Azure. Убедитесь, что эти ключи размещены в двух отдельных регионах Azure для обеспечения геоизбыточности.</span><span class="sxs-lookup"><span data-stu-id="91338-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="91338-427">Для создания функции DEP необходимо удаленно подключиться к SharePoint Online с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91338-427">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="91338-428">На локальном компьютере с помощью рабочей или учебной учетной записи, имеющей разрешения глобального администратора в организации Office 365, [подключитесь к SharePoint Online PowerShell](https://technet.microsoft.com/library/fp161372.aspx).</span><span class="sxs-lookup"><span data-stu-id="91338-428">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="91338-429">В командной консоли Microsoft SharePoint Online выполните командлет [Register-сподатаенкриптионполици](https://technet.microsoft.com/library/mt843950.aspx) , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="91338-429">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="91338-p164">При регистрации функции DEP шифрование начинается с данных в Geo. Это может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="91338-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="91338-432">Проверка шифрования сайтов групп, сайтов групп и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="91338-432">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="91338-433"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-433"></span></span>

<span data-ttu-id="91338-434">Состояние шифрования можно проверить, выполнив командлет Get – Сподатаенкриптионполици следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-434">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="91338-435">Выходные данные этого командлета включают:</span><span class="sxs-lookup"><span data-stu-id="91338-435">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="91338-436">УНИВЕРСАЛЬНЫЙ код ресурса (URI) первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="91338-436">The URI of the primary key.</span></span>
    
- <span data-ttu-id="91338-437">УНИВЕРСАЛЬНЫЙ код ресурса (URI) вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="91338-437">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="91338-p165">Состояние шифрования для Geo. Возможные состояния:</span><span class="sxs-lookup"><span data-stu-id="91338-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="91338-440">**Регистрация незарегистрирована:** Шифрование ключей клиентов еще не применено.</span><span class="sxs-lookup"><span data-stu-id="91338-440">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="91338-p166">**Регистрация:** Шифрование ключей клиентов применено, а файлы находятся в процессе шифрования. Если ваше географическое состояние находится в этом состоянии, вы также увидите сведения о том, какой процент сайтов в географическом расположении является полным, чтобы можно было отслеживать ход шифрования.</span><span class="sxs-lookup"><span data-stu-id="91338-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="91338-443">**Зарегистрировано:** Шифрование ключей клиентов применено, а все файлы на всех сайтах зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="91338-443">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="91338-p167">**Пошаговое руководство:** Выполняется основной этап. Если ваше географическое состояние находится в этом состоянии, вы также увидите сведения о том, на каком проценте сайтов выполнялась операция отката ключа, чтобы можно было отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="91338-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="91338-446">Управление ключом клиента для Office 365</span><span class="sxs-lookup"><span data-stu-id="91338-446">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="91338-447"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-447"></span></span>

<span data-ttu-id="91338-448">После того как вы настроили ключ клиента для Office 365, вы можете выполнить эти дополнительные задачи по управлению.</span><span class="sxs-lookup"><span data-stu-id="91338-448">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="91338-449">Восстановление ключей Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-449">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="91338-450">ПоШаговое или вращение ключа в хранилище ключей Azure, которое вы используете с ключом клиента</span><span class="sxs-lookup"><span data-stu-id="91338-450">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="91338-451">Управление разрешениями для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="91338-451">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="91338-452">Определение функции DEP, назначенной для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="91338-452">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="91338-453">Восстановление ключей Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-453">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="91338-454"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-454"></span></span>

<span data-ttu-id="91338-p168">Перед выполнением восстановления используйте возможности восстановления, предоставляемые функцией обратимого удаления. Для всех ключей, используемых с ключом клиента, необходимо включить функцию обратимого удаления. Обратимое удаление действует как корзина и позволяет выполнить восстановление до 90 дней без необходимости восстановления. Восстановление должно требоваться только в крайних или необычных обстоятельствах, например, при потере ключа или основного хранилища ключей. Если необходимо восстановить ключ для использования с ключом клиента, в Azure PowerShell запустите командлет reStore – Азурекэйваулткэй следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="91338-460">Пример:</span><span class="sxs-lookup"><span data-stu-id="91338-460">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="91338-p169">Если ключ с таким именем уже существует в этом хранилище ключей, операция восстановления завершится с ошибками. ReStore — Азурекэйваулткэй восстанавливает все ключевые версии и все метаданные для ключа, включая имя ключа.</span><span class="sxs-lookup"><span data-stu-id="91338-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="91338-463">ПоШаговое или вращение ключа в хранилище ключей Azure, которое вы используете с ключом клиента</span><span class="sxs-lookup"><span data-stu-id="91338-463">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="91338-464"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-464"></span></span>

<span data-ttu-id="91338-p170">Для Azure Key Vault или с помощью ключа клиента не требуются чередующиеся ключи. Кроме того, ключи, защищенные с помощью HSM, практически невозможны для взлома. Даже если корневой ключ был в наличии вредоносного субъекта, использовать его для расшифровки данных невозможно, так как только код Office 365 знает, как его использовать. Однако ключ клиента поддерживает пошаговое обновление.</span><span class="sxs-lookup"><span data-stu-id="91338-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="91338-p171">Только отменяйте ключ шифрования, который вы используете с ключом клиента, если существует четкая техническая причина, или требованием соответствия требованиям является поэтапное развертывание ключа. Кроме того, не удаляйте ключи, которые не были связаны с политиками. При откате ключей будет использоваться содержимое, зашифрованное с помощью предыдущих ключей. Например, несмотря на то, что активные почтовые ящики будут повторно зашифрованы, неактивные, отключенные и отключенные почтовые ящики, могут быть зашифрованы с помощью предыдущих ключей. SharePoint Online выполняет резервное копирование контента для восстановления и восстановления, поэтому по-прежнему можно заархивировать содержимое, используя старые ключи.</span><span class="sxs-lookup"><span data-stu-id="91338-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="91338-p172">Чтобы обеспечить безопасность данных, SharePoint Online разрешит одновременное выполнение нескольких операций отката. Если вы хотите выполнить оба этих ключа в каждом хранилище ключей, необходимо дождаться, пока первая операция отката ключа будет полностью завершена. Наша рекомендация состоит в том, чтобы пополнить основные операции с разными интервалами, чтобы избежать возникновения такой ситуации.</span><span class="sxs-lookup"><span data-stu-id="91338-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="91338-p173">При выполнении отката ключа вы запрашиваете новую версию существующего ключа. Чтобы запросить новую версию существующего ключа, используйте тот же командлет [Add – азурекэйваулткэй](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey)с тем же синтаксисом, который использовался для создания ключа в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="91338-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="91338-479">Пример:</span><span class="sxs-lookup"><span data-stu-id="91338-479">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="91338-p174">В этом примере, так как ключ с именем **contoso – O365EX — Na – VaultA1 – Key001** уже существует в хранилище **contoso — O365EX, Na/VaultA1** , будет создана новая версия ключа. При выполнении операции добавляется новая версия ключа. В этой операции предыдущие основные версии сохраняются в журнале версий ключа, поэтому данные, зашифрованные с помощью этого ключа, можно по-прежнему расшифровывать. После того как вы передаете какой-либо ключ, связанный с DEP, необходимо запустить дополнительный командлет, чтобы ключ клиента начал использовать новый ключ.</span><span class="sxs-lookup"><span data-stu-id="91338-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="91338-484">РазРешите Exchange Online и Skype для бизнеса использовать новый ключ после прокрутки или вращения ключей в Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-484">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="91338-485">При выполнении одного из ключей Azure Key Vault, связанных с функцией DEP, используемой в Exchange Online и Skype для бизнеса, необходимо выполнить следующую команду, чтобы обновить компонент DEP и включить Office 365, чтобы начать использовать новый ключ.</span><span class="sxs-lookup"><span data-stu-id="91338-485">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="91338-486">Чтобы назначить ключ клиента для шифрования почтовых ящиков в Office 365, выполните командлет Set – Dataencryptionpolicy используется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-486">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="91338-p175">В течение 48 часов активные почтовые ящики, зашифрованные с помощью этой политики, будут связаны с обновленным ключом. Выполните действия, описанные в статье [Определение функции DEP, назначенного](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) для почтового ящика, чтобы проверить значение свойства датаенкриптионполициид для почтового ящика. Значение этого свойства изменится после применения обновленного ключа.</span><span class="sxs-lookup"><span data-stu-id="91338-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="91338-490">Включение SharePoint Online и OneDrive для бизнеса для использования нового ключа после прокрутки или вращения ключей в Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="91338-490">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="91338-491">При выполнении одного из ключей Azure Key Vault, связанных с функцией DEP, используемой в SharePoint Online и OneDrive для бизнеса, необходимо выполнить командлет [Update-сподатаенкриптионполици](https://technet.microsoft.com/library/mt843948.aspx) , чтобы обновить компонент DEP и включить Office 365, чтобы начать использовать новый ключ.</span><span class="sxs-lookup"><span data-stu-id="91338-491">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="91338-p176">При этом будет запущена операция полного развертывания SharePoint Online и OneDrive для бизнеса. Это действие не является медленным. Чтобы просмотреть ход выполнения операции с ключом, выполните командлет Get – Сподатаенкриптионполици следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91338-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="91338-495">Управление разрешениями для хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="91338-495">Manage key vault permissions</span></span>
<span data-ttu-id="91338-496"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-496"></span></span>

<span data-ttu-id="91338-p177">Доступно несколько командлетов, которые позволяют просматривать и при необходимости удалять разрешения для хранилища ключей. Возможно, вам потребуется удалить разрешения, например, когда сотрудник покидает команду.</span><span class="sxs-lookup"><span data-stu-id="91338-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="91338-499">Чтобы просмотреть разрешения на доступ к хранилищу ключей, запустите командлет Get – Азурермкэйваулт:</span><span class="sxs-lookup"><span data-stu-id="91338-499">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="91338-500">Пример:</span><span class="sxs-lookup"><span data-stu-id="91338-500">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="91338-501">Чтобы удалить разрешения администратора, запустите командлет reMove – Азурермкэйваултакцессполици:</span><span class="sxs-lookup"><span data-stu-id="91338-501">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="91338-502">Пример:</span><span class="sxs-lookup"><span data-stu-id="91338-502">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="91338-503">Определение функции DEP, назначенной для почтового ящика</span><span class="sxs-lookup"><span data-stu-id="91338-503">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="91338-504"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="91338-504"></span></span>

<span data-ttu-id="91338-p178">Чтобы определить, какая функция DEP назначена почтовому ящику, используйте командлет Get – MailboxStatistics. Командлет возвращает уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="91338-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="91338-p179">Где *женералмаилбоксормаилусеридпараметер* указывает почтовый ящик. Дополнительные сведения о командлете Get – MailboxStatistics можно найти в статье [Get – MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="91338-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="91338-509">Используйте GUID, чтобы узнать понятное имя DEP, которому назначен почтовый ящик, выполнив следующий командлет.</span><span class="sxs-lookup"><span data-stu-id="91338-509">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="91338-510">Где *GUID* — это идентификатор GUID, возвращенный командлетом Get-MailboxStatistics на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="91338-510">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  

