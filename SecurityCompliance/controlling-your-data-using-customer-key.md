---
title: Контроль данных в Office 365 с помощью ключа клиента
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f2cd475a-e592-46cf-80a3-1bfb0fa17697
description: Узнайте, как настроить ключ клиента Office 365 для Exchange Online, Скайп для бизнеса, SharePoint Online и OneDrive для бизнеса. С ключом клиента управления ключами шифрования вашей организации и затем настроить Office 365 их использования для шифрования данных статических в центрах обработки данных корпорации Майкрософт.
ms.openlocfilehash: f8d7c12c32ca74b842f676f4a2ccde4d1c758361
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559234"
---
# <a name="controlling-your-data-in-office-365-using-customer-key"></a><span data-ttu-id="45aeb-104">Контроль данных в Office 365 с помощью ключа клиента</span><span class="sxs-lookup"><span data-stu-id="45aeb-104">Controlling your data in Office 365 using Customer Key</span></span>

<span data-ttu-id="45aeb-p102">С ключом клиента управления ключами шифрования вашей организации и затем настроить Office 365 их использования для шифрования данных статических в центрах обработки данных корпорации Майкрософт. Статических данных включает в себя данные из Exchange Online и Скайп для бизнеса, которые хранятся в почтовые ящики и файлы, которые хранятся в SharePoint Online и OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p102">With Customer Key, you control your organization's encryption keys and then configure Office 365 to use them to encrypt your data at rest in Microsoft's data centers. Data at rest includes data from Exchange Online and Skype for Business that is stored in mailboxes and files that are stored in SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="45aeb-p103">Прежде чем использовать ключ клиента Office 365, необходимо настроить Azure. В этом разделе описаны действия, которые необходимо выполнить для создания и настройки необходимые ресурсы Azure и затем пошаговые инструкции по настройке ключа клиента в Office 365. После завершения установки Azure вам определить, какая политика, а таким образом, какие ключи для назначения почтовые ящики и файлы в вашей организации. Почтовые ящики и файлы, для которых не назначение политики будут использовать политики шифрования, контролируемые и управляемые корпорацией Майкрософт. Дополнительные сведения о ключевых клиента, а также общие сведения просмотрите [Ключа клиента для вопросы и ответы по Office 365](service-encryption-with-customer-key-faq.md).</span><span class="sxs-lookup"><span data-stu-id="45aeb-p103">You must set up Azure before you can use Customer Key for Office 365. This topic describes the steps you need to follow to create and configure the required Azure resources and then provides the steps for setting up Customer Key in Office 365. After you have completed Azure setup, you determine which policy, and therefore, which keys, to assign to mailboxes and files in your organization. Mailboxes and files for which you don't assign a policy will use encryption policies that are controlled and managed by Microsoft. For more information about Customer Key, or for a general overview, see the [Customer Key for Office 365 FAQ](service-encryption-with-customer-key-faq.md).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="45aeb-p104">Мы настоятельно рекомендуем придерживаться рекомендации в этом разделе. Они называются как **ПОДСКАЗКИ** и **важно**. Клиент ключ позволяет корневой ключами шифрования, область действия может быть задано как всей организации. Это означает, что ошибки, сделанных с помощью этих ключей может иметь широкое влияние и может привести к перерыва в обслуживании или безотзывным потери данных.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p104">We strongly recommend that you follow the best practices in this topic. These are called out as **TIP** and **IMPORTANT**. Customer Key gives you control over root encryption keys whose scope can be as large as your entire organization. This means that mistakes made with these keys can have a broad impact and may result in service interruptions or irrevocable loss of your data.</span></span> 
  
## <a name="before-you-begin-setting-up-customer-key"></a><span data-ttu-id="45aeb-116">Перед началом настройки ключа клиента</span><span class="sxs-lookup"><span data-stu-id="45aeb-116">Before you begin setting up Customer Key</span></span>
<span data-ttu-id="45aeb-117"><a name="Beforeyoustart"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-117"></span></span>

<span data-ttu-id="45aeb-p105">Перед началом работы убедитесь, что у вас есть соответствующие лицензирования для вашей организации. Ключ клиента в Office 365, предлагаемых в Office 365 E5 или SKU дополнительные соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p105">Before you get started, be sure you have the appropriate licensing for your organization. Customer Key in Office 365 is offered in Office 365 E5 or the Advanced Compliance SKU.</span></span>
  
<span data-ttu-id="45aeb-p106">Затем изучить основные понятия и процедуры, описанные в этом разделе, необходимо проверить документации [Помещение ключ Azure](https://azure.microsoft.com/en-us/documentation/services/key-vault/) . Кроме того ознакомиться с терминов, используемых в Azure, например, для [клиента](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span><span class="sxs-lookup"><span data-stu-id="45aeb-p106">Then, to understand the concepts and procedures in this topic, you should review the [Azure Key Vault](https://azure.microsoft.com/en-us/documentation/services/key-vault/) documentation. Also, become familiar with the terms used in Azure, for example, [tenant](https://msdn.microsoft.com/library/azure/jj573650.aspx#BKMK_WhatIsAnAzureADTenant).</span></span>
  
<span data-ttu-id="45aeb-122">Чтобы оставить отзыв по ключу клиента, включая документацию, отправьте customerkeyfeedback@microsoft.com идеи, предложения и перспективы.</span><span class="sxs-lookup"><span data-stu-id="45aeb-122">To provide feedback on Customer Key, including the documentation, send your ideas, suggestions and perspectives to customerkeyfeedback@microsoft.com.</span></span>
  
## <a name="overview-of-setting-up-customer-key-for-office-365"></a><span data-ttu-id="45aeb-123">Общие сведения о настройке ключа клиента Office 365</span><span class="sxs-lookup"><span data-stu-id="45aeb-123">Overview of setting up Customer Key for Office 365</span></span>
<span data-ttu-id="45aeb-124"><a name="Overview"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-124"></span></span>

<span data-ttu-id="45aeb-p107">Чтобы настроить ключ клиента будет выполнить эти задачи. В этом разделе содержатся подробные инструкции по каждой задачи или ссылки на более подробные сведения для каждого шага процесса в работе.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p107">To set up Customer Key you will complete these tasks. The rest of this topic provides detailed instructions for each task, or links out to more information for each step in the process.</span></span>
  
<span data-ttu-id="45aeb-127">**В Azure и она Майкрософт:**</span><span class="sxs-lookup"><span data-stu-id="45aeb-127">**In Azure and Microsoft FastTrack:**</span></span>
  
<span data-ttu-id="45aeb-p108">С помощью удаленного подключения к Windows Azure PowerShell завершит большая часть этих задач. Для достижения наилучших результатов используйте версию 4.4.0 или более поздней версии для Windows Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p108">You will complete most of these tasks by remotely connecting to Azure PowerShell. For best results, use version 4.4.0 or later of Azure PowerShell.</span></span>
  
- [<span data-ttu-id="45aeb-130">Создание двух новых подписок Azure</span><span class="sxs-lookup"><span data-stu-id="45aeb-130">Create two new Azure subscriptions</span></span>](controlling-your-data-using-customer-key.md#Create2newsubs)
    
- [<span data-ttu-id="45aeb-131">Регистрация Azure подписок для использования период обязательные хранения</span><span class="sxs-lookup"><span data-stu-id="45aeb-131">Register Azure subscriptions to use a mandatory retention period</span></span>](controlling-your-data-using-customer-key.md#RegisterSubsforMRP)
    
    <span data-ttu-id="45aeb-132">Регистрация может занять от одного до пяти рабочих дней.</span><span class="sxs-lookup"><span data-stu-id="45aeb-132">Registration can take from one to five business days.</span></span>
    
- [<span data-ttu-id="45aeb-133">Отправка запроса для активации ключа клиента Office 365</span><span class="sxs-lookup"><span data-stu-id="45aeb-133">Submit a request to activate Customer Key for Office 365</span></span>](controlling-your-data-using-customer-key.md#FastTrack)
    
    <span data-ttu-id="45aeb-p109">После создания двух новых подписок Azure, необходимые для отправки соответствующих предложения запроса ключа клиента, выполнив веб-форму, которая размещена на портале Microsoft эту. Группа она не оказание помощи с ключом клиента. Office просто использует эту портала для для отправки формы и для отслеживания соответствующих предложений для ключа клиента.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p109">Once you've created the two new Azure subscriptions, you'll need to submit the appropriate Customer Key offer request by completing a web form that is hosted in the Microsoft FastTrack portal. The FastTrack team doesn't provide assistance with Customer Key. Office simply uses the FastTrack portal to allow you to submit the form and to help us track the relevant offers for Customer Key.</span></span>
  
<span data-ttu-id="45aeb-p110">После отправки предложения ключа клиента Microsoft просматривает запрос и уведомляет можно перейти к дальнейшей задачи настройки. Этот процесс может занять до пяти рабочих дней.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p110">Once you have submitted a Customer Key offer, Microsoft reviews your request and notifies you when you can proceed with the rest of the setup tasks. This process can take up to five business days.</span></span>
    
- [<span data-ttu-id="45aeb-139">Создание premium помещение ключ Azure в каждой подписки</span><span class="sxs-lookup"><span data-stu-id="45aeb-139">Create a premium Azure Key Vault in each subscription</span></span>](controlling-your-data-using-customer-key.md#CreateKeyVault)
    
- [<span data-ttu-id="45aeb-140">Назначение разрешений каждого ключа хранилище</span><span class="sxs-lookup"><span data-stu-id="45aeb-140">Assign permissions to each key vault</span></span>](controlling-your-data-using-customer-key.md#KeyVaultPerms)
    
- [<span data-ttu-id="45aeb-141">Включение и подтвердите обратимым удалением на ключевых хранилищах</span><span class="sxs-lookup"><span data-stu-id="45aeb-141">Enable and then confirm soft delete on your key vaults</span></span>](controlling-your-data-using-customer-key.md#SoftDelete)
    
- [<span data-ttu-id="45aeb-142">Добавление ключа для каждого ключа помещение либо путем создания или импорта ключа</span><span class="sxs-lookup"><span data-stu-id="45aeb-142">Add a key to each key vault either by creating or importing a key</span></span>](controlling-your-data-using-customer-key.md#AddKeystoKeyVault)
    
- [<span data-ttu-id="45aeb-143">Установите флажок для уровня восстановления ключи</span><span class="sxs-lookup"><span data-stu-id="45aeb-143">Check the recovery level of your keys</span></span>](controlling-your-data-using-customer-key.md#CheckKeyRecoveryLevel)
    
- [<span data-ttu-id="45aeb-144">Помещение резервного копирования Azure ключа</span><span class="sxs-lookup"><span data-stu-id="45aeb-144">Backup Azure Key Vault</span></span>](controlling-your-data-using-customer-key.md#BackupAzureKeyVaultkeys)
    
- [<span data-ttu-id="45aeb-145">Проверка параметров конфигурации помещение ключ Azure</span><span class="sxs-lookup"><span data-stu-id="45aeb-145">Validate Azure Key Vault configuration settings</span></span>](controlling-your-data-using-customer-key.md#Validateconfiguration)
    
- [<span data-ttu-id="45aeb-146">Получение URI для каждого ключа помещение ключ Azure</span><span class="sxs-lookup"><span data-stu-id="45aeb-146">Obtain the URI for each Azure Key Vault key</span></span>](controlling-your-data-using-customer-key.md#GetKeyURI)
    
<span data-ttu-id="45aeb-147">**В Office 365:**</span><span class="sxs-lookup"><span data-stu-id="45aeb-147">**In Office 365:**</span></span>
  
<span data-ttu-id="45aeb-148">Exchange Online и Скайп для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="45aeb-148">Exchange Online and Skype for Business:</span></span>
  
- [<span data-ttu-id="45aeb-149">Создание политики шифрования данных (DEP) для использования с Exchange Online и Скайп для бизнеса</span><span class="sxs-lookup"><span data-stu-id="45aeb-149">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4EXOSkype)
    
- [<span data-ttu-id="45aeb-150">Назначение DEP почтовому ящику</span><span class="sxs-lookup"><span data-stu-id="45aeb-150">Assign a DEP to a mailbox</span></span>](controlling-your-data-using-customer-key.md#assignDEPtomailbox)
    
- [<span data-ttu-id="45aeb-151">Проверка шифрования почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="45aeb-151">Validate mailbox encryption</span></span>](controlling-your-data-using-customer-key.md#validatemailboxencryption)
    
<span data-ttu-id="45aeb-152">SharePoint Online и OneDrive для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="45aeb-152">SharePoint Online and OneDrive for Business:</span></span>
  
- [<span data-ttu-id="45aeb-153">Создание политики шифрования данных (DEP) для каждого SharePoint Online и OneDrive для бизнеса географически</span><span class="sxs-lookup"><span data-stu-id="45aeb-153">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>](controlling-your-data-using-customer-key.md#CreateDEP4SPOODfB)
    
- [<span data-ttu-id="45aeb-154">Проверка шифрования группы сайтов, веб-сайтов групп и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="45aeb-154">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>](controlling-your-data-using-customer-key.md#validateencryptionSPO)
    
## <a name="complete-tasks-in-azure-key-vault-and-microsoft-fasttrack-for-customer-key"></a><span data-ttu-id="45aeb-155">Выполните задачи в хранилище ключа Azure и она Microsoft для ключа клиента</span><span class="sxs-lookup"><span data-stu-id="45aeb-155">Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key</span></span>
<span data-ttu-id="45aeb-156"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-156"></span></span>

<span data-ttu-id="45aeb-p111">Выполните эти задачи в хранилище Azure ключ для настройки ключа клиента для Office 365. Необходимо выполнить следующие действия, независимо от того, является ли планируется настроить ключ клиента для Exchange Online и Скайп для бизнеса или SharePoint Online и OneDrive для бизнеса или для всех поддерживаемых служб в Office 365.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p111">Complete these tasks in Azure Key Vault in order to set up Customer Key for Office 365. You will need to complete these steps regardless of whether you intend to set up Customer Key for Exchange Online and Skype for Business or SharePoint Online and OneDrive for Business or for all supported services in Office 365.</span></span>
  
### <a name="create-two-new-azure-subscriptions"></a><span data-ttu-id="45aeb-159">Создание двух новых подписок Azure</span><span class="sxs-lookup"><span data-stu-id="45aeb-159">Create two new Azure subscriptions</span></span>
<span data-ttu-id="45aeb-160"><a name="Create2newsubs"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-160"></span></span>

<span data-ttu-id="45aeb-p112">Для ключа клиента требуются две Azure подписки. Рекомендуется Корпорация Майкрософт рекомендует создавать новые Azure подписки для использования с ключом клиента. Azure ключи помещение ключ только авторизации для приложений тому же владельцу Azure Active Directory (AAD), необходимо создать новые подписки, с помощью же Azure AD клиента, который используется в организации Office 365, в которой будет назначен DEPs. Например с помощью вашего рабочего или школы учетной записи, имеющей права глобального администратора в организации Office 365. Подробное описание процедуры в разделе [Регистрация для Azure в организации](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span><span class="sxs-lookup"><span data-stu-id="45aeb-p112">Two Azure subscriptions are required for Customer Key. As a best practice, Microsoft recommends that you create new Azure subscriptions for use with Customer Key. Azure Key Vault keys can only be authorized for applications in the same Azure Active Directory (AAD) tenant, you must create the new subscriptions using the same Azure AD tenant used with your Office 365 organization where the DEPs will be assigned. For example, using your work or school account that has global administrator privileges in your Office 365 organization. For detailed steps, see [Sign up for Azure as an organization](https://azure.microsoft.com/en-us/documentation/articles/sign-up-organization/).</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="45aeb-p113">Ключ клиента требуется два ключи для каждой политики шифрования данных (DEP). Для этого необходимо создать два Azure подписок. Рекомендуется Корпорация Майкрософт рекомендует наличие отдельных членов вашей организации настроить один ключ в каждой подписки. Кроме того эти Azure подписки должен использоваться только для управления ключами шифрования для Office 365. Это обеспечивает защиту вашей организации в случае один из вашего операторов случайно, специально или намеренно удаляет или в противном случае mismanages ключи, для которых они отвечают.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p113">Customer Key requires two keys for each data encryption policy (DEP). In order to achieve this, you must create two Azure subscriptions. As a best practice, Microsoft recommends that you have separate members of your organization configure one key in each subscription. In addition, these Azure subscriptions should only be used to administer encryption keys for Office 365. This protects your organization in case one of your operators accidentally, intentionally, or maliciously deletes or otherwise mismanages the keys for which they are responsible. </span></span><br/> <span data-ttu-id="45aeb-p114">Рекомендуется настроить новые Azure подписки, используемые исключительно для управления ресурсами хранилища Azure ключ для использования с ключом клиента. Нет практические ограничения на число Azure подписок, которые можно создать для вашей организации. Рекомендации будет свести к минимуму влияние человеческого ошибка при помощь в управлении ресурсы, используемые ключа клиента.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p114">We recommend that you set up new Azure subscriptions that are solely used for managing Azure Key Vault resources for use with Customer Key. There is no practical limit to the number of Azure subscriptions that you can create for your organization. Following these best practices will minimize the impact of human error while helping to manage the resources used by Customer Key.</span></span> 
  
### <a name="submit-a-request-to-activate-customer-key-for-office-365"></a><span data-ttu-id="45aeb-174">Отправка запроса для активации ключа клиента Office 365</span><span class="sxs-lookup"><span data-stu-id="45aeb-174">Submit a request to activate Customer Key for Office 365</span></span>
<span data-ttu-id="45aeb-175"><a name="FastTrack"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-175"></span></span>

<span data-ttu-id="45aeb-p115">После выполнения действия Azure, вам потребуются для отправки запроса предложения в [портал Microsoft эту](https://fasttrack.microsoft.com/). После отправки запроса через эту веб-портала Microsoft проверяет Azure ключ хранилище данных и контакт сведения о конфигурации, указанного. Выбором, сделанным в форме предложение о авторизованного ответственные за вашей организации является важным и необходимые для завершения регистрации ключа клиента. Ответственные за вашей организации, выбранного в форме будет использоваться для обеспечения подлинности все запросы для отмены и удалить все клавиши, которые используются с политикой шифрования данных ключа клиента. Вам потребуется сделать это действие один раз, чтобы активировать ключ клиента для Exchange Online и Скайп для бизнеса покрытия и еще раз активировать ключ клиента для SharePoint Online и OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p115">Once you've completed the Azure steps, you'll need to submit an offer request in the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/). Once you have submitted a request through the FastTrack web portal, Microsoft verifies the Azure Key Vault configuration data and contact information you provided. The selections that you make in the offer form regarding the authorized officers of your organization is critical and necessary for completion of Customer Key registration. The officers of your organization that you select in the form will be the used to ensure the authenticity of any request to revoke and destroy all keys used with a Customer Key data encryption policy. You'll need to do this step once to activate Customer Key for Exchange Online and Skype for Business coverage and a second time to activate Customer Key for SharePoint Online and OneDrive for Business.</span></span>
  
<span data-ttu-id="45aeb-181">Чтобы отправить предложение для активации ключа клиента, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="45aeb-181">To submit an offer to activate Customer Key, complete these steps:</span></span>
  
1. <span data-ttu-id="45aeb-182">Использование рабочего или школы учетной записи, имеющей права глобального администратора в организации Office 365, выполните вход в [портал Microsoft эту](https://fasttrack.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="45aeb-182">Using a work or school account that has global administrator permissions in your Office 365 organization, log in to the [Microsoft FastTrack portal](https://fasttrack.microsoft.com/).</span></span>
    
2. <span data-ttu-id="45aeb-183">После входа в, перейдите к **панели мониторинга**.</span><span class="sxs-lookup"><span data-stu-id="45aeb-183">Once you're logged in, browse to the **Dashboard**.</span></span>
    
3. <span data-ttu-id="45aeb-184">Выберите **предлагает**и просмотрите список текущего предложения.</span><span class="sxs-lookup"><span data-stu-id="45aeb-184">Choose **Offers**, and review the list of current offers.</span></span>
    
4. <span data-ttu-id="45aeb-185">Выберите **Дополнительные** предложения, которое применяется к вам:</span><span class="sxs-lookup"><span data-stu-id="45aeb-185">Choose **Learn More** for the offer that applies to you:</span></span> 
    
  - <span data-ttu-id="45aeb-186">**Exchange Online и Скайп для бизнеса:** Выберите команду **Дополнительные** предложение **Ключа клиента для Exchange** .</span><span class="sxs-lookup"><span data-stu-id="45aeb-186">**Exchange Online and Skype for Business:** Choose **Learn More** on the **Customer Key for Exchange** offer.</span></span> 
    
  - <span data-ttu-id="45aeb-187">**SharePoint Online и OneDrive для бизнеса:** Выберите **Дополнительные** на предложение **Ключа клиента для SharePoint и OneDrive для бизнеса** .</span><span class="sxs-lookup"><span data-stu-id="45aeb-187">**SharePoint Online and OneDrive for Business:** Chose **Learn More** on the **Customer Key for SharePoint and OneDrive for Business** offer.</span></span> 
    
5. <span data-ttu-id="45aeb-188">На странице **получения подробных сведений** выберите **Создать запрос**.</span><span class="sxs-lookup"><span data-stu-id="45aeb-188">On the **Offer details** page, choose **Create Request**.</span></span>
    
6. <span data-ttu-id="45aeb-p116">Заполните все сведения, которые применяются и запрошенные данные в форме предложение. Обратите особое внимание выбранных элементов для каких ответственные за вашей организации будет использоваться для авторизации для утверждения уничтожения постоянные и нельзя обратить ключами шифрования и данных. После выполнения формы, нажмите кнопку **Submit**.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p116">Fill out all applicable details and requested information on the offer form. Pay particular attention to your selections for which officers of your organization you want to authorize to approve the permanent and irreversible destruction of encryption keys and data. Once you've completed the form, choose **Submit**.</span></span>
    
    <span data-ttu-id="45aeb-192">Этот процесс может занять до пяти рабочих дней после Microsoft получила уведомление запроса.</span><span class="sxs-lookup"><span data-stu-id="45aeb-192">This process can take up to five business days once Microsoft has been notified of your request.</span></span>
    
7. <span data-ttu-id="45aeb-193">Перейдите на обязательные хранения периода ниже раздел.</span><span class="sxs-lookup"><span data-stu-id="45aeb-193">Continue on to the mandatory retention period section below.</span></span>
    
### <a name="register-azure-subscriptions-to-use-a-mandatory-retention-period"></a><span data-ttu-id="45aeb-194">Регистрация Azure подписок для использования период обязательные хранения</span><span class="sxs-lookup"><span data-stu-id="45aeb-194">Register Azure subscriptions to use a mandatory retention period</span></span>
<span data-ttu-id="45aeb-195"><a name="RegisterSubsforMRP"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-195"></span></span>

<span data-ttu-id="45aeb-p117">Временное или постоянное потеря ключами шифрования корневой может быть очень аварийные или даже аварийное операции службы и может привести к потере данных. По этой причине ресурсы, используемые с ключом клиента требуется усиленная защита. Все Azure ресурсы, которые используются с ключом клиента предлагают механизмов защиты за пределы конфигурация по умолчанию. Azure подписок можно с меткой или зарегистрирована, чтобы не позволит немедленные и безотзывным отмены. Это называется регистрации в течение обязательные хранения. Действия, необходимые для регистрации Azure подписок в течение обязательные хранения требуется совместной работы с Office 365 team. Этот процесс может занять от одного до пяти рабочих дней. Ранее это было иногда называется «Не отменить».</span><span class="sxs-lookup"><span data-stu-id="45aeb-p117">The temporary or permanent loss of root encryption keys can be very disruptive or even catastrophic to service operation and can result in data loss. For this reason, the resources used with Customer Key require strong protection. All the Azure resources that are used with Customer Key offer protection mechanisms beyond the default configuration. Azure subscriptions can be tagged or registered in a way that will prevent immediate and irrevocable cancellation. This is referred to as registering for a mandatory retention period. The steps required to register Azure subscriptions for a mandatory retention period require collaboration with the Office 365 team. This process can take from one to five business days. Previously, this was sometimes referred to as "Do Not Cancel".</span></span>
  
<span data-ttu-id="45aeb-204">Перед обращением группы Office 365, необходимо выполнить следующие действия для каждой подписки Azure, используемая с ключом клиента:</span><span class="sxs-lookup"><span data-stu-id="45aeb-204">Before contacting the Office 365 team, you must perform the following steps for each Azure subscription that you use with Customer Key:</span></span>
  
1. <span data-ttu-id="45aeb-p118">Выполните вход Azure подписки с помощью Azure PowerShell. Инструкции [Войдите в систему с Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)см.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p118">Log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
2. <span data-ttu-id="45aeb-207">Выполните командлет Register-AzureRmProviderFeature для регистрации подписок на использование обязательных срок.</span><span class="sxs-lookup"><span data-stu-id="45aeb-207">Run the Register-AzureRmProviderFeature cmdlet to register your subscriptions to use a mandatory retention period.</span></span>
    
  ```
  Register-AzureRmProviderFeature -FeatureName mandatoryRetentionPeriodEnabled -ProviderNamespace Microsoft.Resources
  ```

3. <span data-ttu-id="45aeb-p119">Обратитесь в Майкрософт, чтобы завершить процесс. Для SharePoint и OneDrive для бизнеса группы контактов [spock@microsoft.com](mailto:spock@microsoft.com). Для Exchange Online и Скайп для бизнеса обратитесь в [exock@microsoft.com](mailto:exock@microsoft.com). Соглашение об уровне службы (SLA) для завершения этой процедуры, пяти рабочих дней после Microsoft был получают уведомление в случае (и проверить), который вы зарегистрировали подписок на использование обязательных срок. В электронную почту, относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="45aeb-p119">Contact Microsoft to have the process finalized. For the SharePoint and OneDrive for Business team, contact [spock@microsoft.com](mailto:spock@microsoft.com). For Exchange Online and Skype for Business, contact [exock@microsoft.com](mailto:exock@microsoft.com). The Service Level Agreement (SLA) for completion of this process is five business days once Microsoft has been notified (and verified) that you have registered your subscriptions to use a mandatory retention period. Include the following in your email:</span></span>
    
    <span data-ttu-id="45aeb-213">**Тема**: ключа клиента для \< *полное доменное имя вашего клиента*\></span><span class="sxs-lookup"><span data-stu-id="45aeb-213">**Subject**: Customer Key for \<*Your tenant's fully-qualified domain name*\></span></span> 
    
    <span data-ttu-id="45aeb-214">**Body**: идентификаторы подписки, для которых требуется предоставить обязательные хранения период завершен.</span><span class="sxs-lookup"><span data-stu-id="45aeb-214">**Body**: Subscription IDs for which you want to have the mandatory retention period finalized.</span></span> 
    
4. <span data-ttu-id="45aeb-215">Как только вы получите уведомление от Майкрософт о завершении регистрации, проверьте состояние регистрацию с помощью командлета Get-AzureRmProviderFeature следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-215">Once you receive notification from Microsoft that registration is complete, verify the status of your registration by running the Get-AzureRmProviderFeature cmdlet as follows:</span></span>
    
  ```
  Get-AzureRmProviderFeature -ProviderNamespace Microsoft.Resources -FeatureName mandatoryRetentionPeriodEnabled
  ```

5. <span data-ttu-id="45aeb-216">Убедившись, что свойство **Состояние регистрации** из командлета Get-AzureRmProviderFeature возвращает значение **зарегистрирован**, выполните следующую команду, чтобы завершить процесс:</span><span class="sxs-lookup"><span data-stu-id="45aeb-216">After verifying that the **Registration State** property from the Get-AzureRmProviderFeature cmdlet returns a value of **Registered**, run the following command to complete the process:</span></span>
    
  ```
  Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"
  ```

### <a name="create-a-premium-azure-key-vault-in-each-subscription"></a><span data-ttu-id="45aeb-217">Создание premium помещение ключ Azure в каждой подписки</span><span class="sxs-lookup"><span data-stu-id="45aeb-217">Create a premium Azure Key Vault in each subscription</span></span>
<span data-ttu-id="45aeb-218"><a name="CreateKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-218"></span></span>

<span data-ttu-id="45aeb-219">Порядок создания ключа помещение описаны в [Начало работы с Azure ключ помещение](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), содержащий инструкции по установки и запуска Azure PowerShell, подключение к своей подписке Azure, создания группы ресурсов и создание ключа хранилище, в которой Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45aeb-219">The steps to create a key vault are documented in [Getting Started with Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-get-started/), which guides you through installing and launching Azure PowerShell, connecting to your Azure subscription, creating a resource group, and creating a key vault in that resource group.</span></span>
  
<span data-ttu-id="45aeb-p120">При создании ключа хранилище, необходимо выбрать SKU: стандартный или расширенный. Стандартный SKU позволяет ключи хранилище Azure ключ защищен с помощью программ - нет ключа защиты аппаратного модуля безопасности (HSM) - и Premium SKU позволяет использовать HSM для защиты ключей помещение ключ. Ключ клиента принимает ключевые хранилищах, использующие либо SKU Хотя корпорация Майкрософт рекомендует использовать только SKU Premium. Стоимость операций с ключами любого из этих типов не изменяется, поэтому только разница в себестоимости расходы в месяц для каждого защищенного HSM ключа. Для получения дополнительных сведений в разделе [Цена помещение ключ](https://azure.microsoft.com/pricing/details/key-vault/) .</span><span class="sxs-lookup"><span data-stu-id="45aeb-p120">When you create a key vault, you must choose a SKU: either Standard or Premium. The Standard SKU allows Azure Key Vault keys to be protected with software - there is no Hardware Security Module (HSM) key protection - and the Premium SKU allows the use of HSMs for protection of Key Vault keys. Customer Key accepts key vaults that use either SKU, though Microsoft strongly recommends that you use only the Premium SKU. The cost of operations with keys of either type is the same, so the only difference in cost is the cost per month for each HSM-protected key. See [Key Vault pricing](https://azure.microsoft.com/pricing/details/key-vault/) for details.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="45aeb-225">Используйте хранилищах ключевые Premium SKU и защищенные HSM ключи для производственных данных, а только с помощью клавиш и стандартных SKU ключевые хранилищах для целей тестирования и проверки.</span><span class="sxs-lookup"><span data-stu-id="45aeb-225">Use the Premium SKU key vaults and HSM-protected keys for production data, and only use Standard SKU key vaults and keys for testing and validation purposes.</span></span> 
  
<span data-ttu-id="45aeb-p121">Для каждой службы Office 365, с которым будет использовать ключ клиента Создание ключа помещение в каждой из двух Azure подписки, которые вы создали. Например для Exchange Online, а Скайп для работы только или SharePoint Online и OneDrive для бизнеса только, создается только одна пара хранилищах. Чтобы включить ключа клиента для Exchange Online и SharePoint Online, создается две пары ключей хранилищах.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p121">For each Office 365 service with which you will use Customer Key, create a key vault in each of the two Azure subscriptions that you created. For example, for Exchange Online and Skype for Business only or SharePoint Online and OneDrive for Business only, you will create only one pair of vaults. To enable Customer Key for both Exchange Online and SharePoint Online, you will create two pairs of key vaults.</span></span>
  
<span data-ttu-id="45aeb-p122">Используйте схему именования для ключа хранилищах, отражает целям использования DEP, с которым будет связана хранилищах. В разделе Рекомендации по ниже naming convention рекомендации.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p122">Use a naming convention for key vaults that reflects the intended use of the DEP with which you will associate the vaults. See the Best Practices section below for naming convention recommendations.</span></span>
  
<span data-ttu-id="45aeb-p123">Создайте отдельный, парного набор хранилищах для каждой политики шифрования данных. Для Exchange Online область политика шифрования данных выбранные вами при назначении политики почтовых ящиков. Почтовый ящик может иметь только одну политику, назначенную и можно создать до 50 политики. Для SharePoint Online область политики — все данные из организации в месте или географически.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p123">Create a separate, paired set of vaults for each data encryption policy. For Exchange Online, the scope of a data encryption policy is chosen by you when you assign the policy to mailbox. A mailbox can have only one policy assigned, and you can create up to fifty policies. For SharePoint Online the scope of a policy is all of the data within an organization in a geographic location, or geo.</span></span>
  
<span data-ttu-id="45aeb-p124">Создание ключа хранилищах также требует создания группы Azure ресурсов, поскольку ключевые хранилищах необходимы емкость хранилища (хотя очень маленькие) и помещение ключ ведение журнала, если этот параметр включен, также создает хранимых данных. Рекомендуется Корпорация Майкрософт рекомендует использовать отдельный администраторам управлять каждой группе ресурсов с помощью администрирования по краю с набором администраторов, которые будет управлять всех связанных с ними ресурсы ключа клиента.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p124">The creation of key vaults also requires the creation of Azure resource groups, since key vaults need storage capacity (though very small) and Key Vault logging, if enabled, also generates stored data. As a best practice Microsoft recommends using separate administrators to manage each resource group, with the administration aligned with the set of administrators that will manage all related Customer Key resources.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="45aeb-p125">Для обеспечения максимальной доступности, ключевые хранилищах должен находиться в области ближе к службе Office 365. К примеру Если организации Exchange Online в Северной Америке, поместите ключевые хранилищах в Северной Америке. Если организации Exchange Online в Европе, поместите ключевые хранилищах в Европе.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p125">To maximize availability, your key vaults should be in regions close to your Office 365 service. For example, if your Exchange Online organization is in North America, place your key vaults in North America. If your Exchange Online organization is in Europe, place your key vaults in Europe.</span></span><br/><span data-ttu-id="45aeb-p126">Использовать общий префикс для ключа хранилищах и включают сокращение использования и область применения ключа хранилище и разделов (например, для службы Contoso SharePoint, расположение хранилищах в Северной Америке, пара возможных имен Contoso-O365SP-NA-VaultA1 и Contoso-O365SP-NA-VaultA2. Помещение имена являются глобальный уникальный строками в Azure, поэтому может потребоваться попробуйте вариантов желаемую имен в случае, если требуемый имена уже заявленным другой Azure клиенты. По состоянию на июля 2017 помещение имена нельзя изменить, поэтому рекомендуется составить план написанного для программы установки и использование второго пользователя для проверки, что план выполняется правильно.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p126">Use a common prefix for key vaults, and include an abbreviation of the use and scope of the key vault and keys (e.g., for the Contoso SharePoint service where the vaults will be located in North America, a possible pair of names is Contoso-O365SP-NA-VaultA1 and Contoso-O365SP-NA-VaultA2. Vault names are globally unique strings within Azure, so you may need to try variations of your desired names in case the desired names are already claimed by other Azure customers. As of July 2017 vault names cannot be changed, so a best practice is to have a written plan for setup and use a second person to verify the plan is executed correctly.</span></span><br/><span data-ttu-id="45aeb-p127">Если это возможно создайте вашей хранилищах не пару регионов. Парного Azure областей обеспечения высокой доступности в доменах сбоя службы. Таким образом региональных пары может рассматриваться как резервного копирования область друг друга. Это означает, что Azure ресурс, который переводится в одной области, автоматически увеличит отказоустойчивость через парного область. По этой причине выбор областей для двух хранилищах, используемые в DEP, где области, парного означает, что используются только всего двух областей доступности. Большинство географических расположениях только имеют двух областей, поэтому он еще не можно выбрать, не сопоставленных областей. Если это возможно выберите двух областей не пару для двух хранилищах используется с предотвращения выполнения данных. Это преимущества всего четыре области доступности. Дополнительные сведения можно [Business continuity и аварийное восстановление (BCDR): областей в сочетании Azure](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) для текущего списка региональных пар.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p127">If possible, create your vaults in non-paired regions. Paired Azure regions provide high availability across service failure domains. Therefore, regional pairs can be thought of as each other's backup region. This means that an Azure resource that is placed in one region is automatically gaining fault tolerance through the paired region. For this reason, choosing regions for two vaults used in a DEP where the regions are paired means that only a total of two regions of availability are in use. Most geographies only have two regions, so it's not yet possible to select non-paired regions. If possible, choose two non-paired regions for the two vaults used with a DEP. This benefits from a total of four regions of availability. For more information, see [Business continuity and disaster recovery (BCDR): Azure Paired Regions](https://docs.microsoft.com/azure/best-practices-availability-paired-regions) for a current list of regional pairs.</span></span> 
  
### <a name="assign-permissions-to-each-key-vault"></a><span data-ttu-id="45aeb-252">Назначение разрешений каждого ключа хранилище</span><span class="sxs-lookup"><span data-stu-id="45aeb-252">Assign permissions to each key vault</span></span>
<span data-ttu-id="45aeb-253"><a name="KeyVaultPerms"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-253"></span></span>

<span data-ttu-id="45aeb-p128">Для каждого ключа хранилище необходимо определить три отдельных наборов разрешений для ключа клиента, в зависимости от реализации. Например необходимо определить один набор разрешений для каждой из следующих:</span><span class="sxs-lookup"><span data-stu-id="45aeb-p128">For each key vault, you will need to define three separate sets of permissions for Customer Key, depending on your implementation. For example, you will need to define one set of permissions for each of the following:</span></span>
  
- <span data-ttu-id="45aeb-p129">**Администраторы хранилище ключа** , которое будет выполнять повседневного управления ключевые хранилище для вашей организации. Эти задачи включают резервного копирования, создание, получение, также импортировать, список и восстановления.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p129">**Key vault administrators** that will perform day-to-day management of your key vault for your organization. These tasks include backup, create, get, import, list, and restore.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="45aeb-p130">Набор разрешений, назначенных ключевых помещение администраторы не включает разрешение на удаление ключей. Это не является ошибкой и важные рекомендации. Удаление ключей шифрования не происходит обычно, так как это так без возможности восстановления приведет к потере данных. Рекомендуется не предоставить такое разрешение администраторам ключевые хранилище по умолчанию. Вместо этого зарезервировать это для ключа помещение участники только его и назначьте администратора на основе краткосрочной перспективе после поняты понять последствия.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p130">The set of permissions assigned to key vault administrators does not include the permission to delete keys. This is intentional and an important practice. Deleting encryption keys is not typically done, since doing so permanently destroys data. As a best practice, do not grant this permission to key vault administrators by default. Instead, reserve this for key vault contributors and only assign it to an administrator on a short term basis once a clear understanding of the consequences is understood.</span></span> 
  
    <span data-ttu-id="45aeb-p131">Чтобы назначить эти разрешения для пользователей в организации Office 365, выполните вход в Azure подписки с помощью Azure PowerShell. Инструкции [Войдите в систему с Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1)см.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p131">To assign these permissions to a user in your Office 365 organization, log in to your Azure subscription with Azure PowerShell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps?view=azurermps-4.3.1).</span></span>
    
- <span data-ttu-id="45aeb-265">Запустите командлет Set-AzureRmKeyVaultAccessPolicy, чтобы предоставить необходимые разрешения.</span><span class="sxs-lookup"><span data-stu-id="45aeb-265">Run the Set-AzureRmKeyVaultAccessPolicy cmdlet to assign the necessary permissions.</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
  -UserPrincipalName <UPN of user> -PermissionsToKeys create,import,list,get,backup,restore
  ```

  <span data-ttu-id="45aeb-266">Пример:</span><span class="sxs-lookup"><span data-stu-id="45aeb-266">For example:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -UserPrincipalName alice@contoso.com -PermissionsToKeys create,import,list,get,backup,restore
  ```

- <span data-ttu-id="45aeb-p132">**Участники помещение ключ** , который можно изменить разрешения на помещение ключ Azure самого. Вам потребуется изменить эти разрешения, как сотрудники оставьте или присоединиться к группе или в очень редких случаях, что ключ помещение Администраторы законного необходимы разрешения, чтобы удалить или восстановить ключ. Этот набор ключевых помещение участники необходимо предоставить роли **корреспондента** на ключевых хранилище. Эту роль можно назначить с помощью диспетчера ресурсов Azure. Подробное описание шагов см [Use Role-Based для управления доступом к ресурсам подпиской Azure](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). Администратор, который создает подписку имеет доступ неявно, а также возможность назначать другим администраторам роли корреспондента.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p132">**Key vault contributors** that can change permissions on the Azure Key Vault itself. You'll need to change these permissions as employees leave or join your team, or in the extremely rare situation that the key vault administrators legitimately need permission to delete or restore a key. This set of key vault contributors needs to be granted the **Contributor** role on your key vault. You can assign this role by using Azure Resource Manager. For detailed steps, see [Use Role-Based Access Control to manage access to your Azure subscription resources](https://docs.microsoft.com/azure/active-directory/role-based-access-control-configure). The administrator who creates a subscription has this access implicitly, as well as the ability to assign other administrators to the Contributor role.</span></span>
    
- <span data-ttu-id="45aeb-p133">Если вы планируете использовать ключ клиента с помощью Exchange Online и Скайп для бизнеса, необходимо предоставить разрешение в Office 365 для использования ключа помещение от имени Exchange Online и Скайп для бизнеса. Аналогичным образом Если вы планируете использовать ключ клиента с помощью SharePoint Online и OneDrive для бизнеса, необходимо добавить разрешение для Office 365 для использования ключа помещение от имени SharePoint Online и OneDrive для бизнеса. Чтобы предоставить разрешение в Office 365, выполните командлет **Set-AzureRmKeyVaultAccessPolicy** , используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="45aeb-p133">If you intend to use Customer Key with Exchange Online and Skype for Business, you need to give permission to Office 365 to use the key vault on behalf of Exchange Online and Skype for Business. Likewise, if you intend to use Customer Key with SharePoint Online and OneDrive for Business, you need to add permission for the Office 365 to use the key vault on behalf of SharePoint Online and OneDrive for Business. To give permission to Office 365, run the **Set-AzureRmKeyVaultAccessPolicy** cmdlet using the following syntax:</span></span> 
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
  ```

    <span data-ttu-id="45aeb-276">Где:</span><span class="sxs-lookup"><span data-stu-id="45aeb-276">Where:</span></span>
    
  - <span data-ttu-id="45aeb-277">*vaultname* — это имя ключа vault, которую вы создали.</span><span class="sxs-lookup"><span data-stu-id="45aeb-277">*vaultname* is the name of the key vault you created.</span></span> 
    
  - <span data-ttu-id="45aeb-278">Exchange Online и Скайп для бизнеса замените *appID Office 365* с помощью`00000002-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="45aeb-278">For Exchange Online and Skype for Business, replace  *Office 365 appID* with `00000002-0000-0ff1-ce00-000000000000`</span></span>
    
  - <span data-ttu-id="45aeb-279">SharePoint Online и OneDrive для бизнеса замените *appID Office 365* с помощью`00000003-0000-0ff1-ce00-000000000000`</span><span class="sxs-lookup"><span data-stu-id="45aeb-279">For SharePoint Online and OneDrive for Business, replace  *Office 365 appID* with `00000003-0000-0ff1-ce00-000000000000`</span></span>
    
  <span data-ttu-id="45aeb-280">Пример: Задание разрешений для Exchange Online и Скайп для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="45aeb-280">Example: Setting permissions for Exchange Online and Skype for Business:</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
  ```

  <span data-ttu-id="45aeb-281">Пример: Задание разрешений для SharePoint Online и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="45aeb-281">Example: Setting permissions for SharePoint Online and OneDrive for Business</span></span>
    
  ```
  Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
  -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000003-0000-0ff1-ce00-000000000000
  ```

### <a name="enable-and-then-confirm-soft-delete-on-your-key-vaults"></a><span data-ttu-id="45aeb-282">Включение и подтвердите обратимым удалением на ключевых хранилищах</span><span class="sxs-lookup"><span data-stu-id="45aeb-282">Enable and then confirm soft delete on your key vaults</span></span>
<span data-ttu-id="45aeb-283"><a name="SoftDelete"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-283"></span></span>

<span data-ttu-id="45aeb-p134">Когда можно быстро восстановить ключи, вы вероятность продолжаться расширенные службы из-за намеренно или случайно удаленных разделов. Необходимо включить конфигурацию, называется программных удалить, прежде чем использовать ключи с ключом клиента. Включение программных удаление позволяет восстанавливать ключи или хранилищами в течение 90 дней после удаления без необходимости их восстановления из резервной копии.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p134">When you can quickly recover your keys, you are less likely to experience an extended service outage due to accidentally or maliciously deleted keys. You need to enable this configuration, referred to as Soft Delete, before you can use your keys with Customer Key. Enabling Soft Delete allows you to recover keys or vaults within 90 days of deletion without having to restore them from backup.</span></span>
  
<span data-ttu-id="45aeb-287">Чтобы включить удаление использования программных на ключевых хранилищах, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="45aeb-287">To enable Soft Delete on your key vaults, complete these steps:</span></span>
  
1. <span data-ttu-id="45aeb-p135">Выполните вход Azure подписки с помощью Windows Powershell. Инструкции [Войдите в систему с Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps)см.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p135">Log in to your Azure subscription with Windows Powershell. For instructions, see [Log in with Azure PowerShell](https://docs.microsoft.com/powershell/azure/authenticate-azureps).</span></span>
    
2. <span data-ttu-id="45aeb-p136">Выполните командлет [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) . В этом примере *vaultname* — это имя ключа vault, для которого включается обратимым удалением:</span><span class="sxs-lookup"><span data-stu-id="45aeb-p136">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/azurerm.keyvault/get-azurermkeyvault) cmdlet. In this example, *vaultname* is the name of the key vault for which you are enabling soft delete:</span></span> 
    
   ```
   $v = Get-AzureRmKeyVault -VaultName <vaultname>
   $r = Get-AzureRmResource -ResourceId $v.ResourceId
   $r.Properties | Add-Member -MemberType NoteProperty -Name enableSoftDelete -Value 'True'
   Set-AzureRmResource -ResourceId $r.ResourceId -Properties $r.Properties
   ``` 
    
3. <span data-ttu-id="45aeb-p137">Убедитесь, что настройки обратимым удалением для ключа хранилище с помощью командлета **Get-AzureRmKeyVault** . Если обратимым удалением настроена должным образом ключевые vault, обратимо удалять включено? свойство возвращает значение **True**:</span><span class="sxs-lookup"><span data-stu-id="45aeb-p137">Confirm soft delete is configured for the key vault by running the **Get-AzureRmKeyVault** cmdlet. If soft delete is configured properly for the key vault, then the  Soft Delete Enabled? property returns a value of **True**:</span></span> 
    
   ```
   Get-AzureRmKeyVault -VaultName <vaultname> | fl
   ```

   
    
### <a name="add-a-key-to-each-key-vault-either-by-creating-or-importing-a-key"></a><span data-ttu-id="45aeb-294">Добавление ключа для каждого ключа помещение либо путем создания или импорта ключа</span><span class="sxs-lookup"><span data-stu-id="45aeb-294">Add a key to each key vault either by creating or importing a key</span></span>
<span data-ttu-id="45aeb-295"><a name="AddKeystoKeyVault"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-295"></span></span>

<span data-ttu-id="45aeb-p138">Существует два способа добавления ключей Azure хранилище ключа; можно создать ключ непосредственно в хранилище ключа или импорта ключа. Создание ключа непосредственно в хранилище ключ — это метод проще Импорт ключа обеспечивает полного контроля над созданием ключ.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p138">There are two ways to add keys to an Azure Key Vault; you can create a key directly in Key Vault, or you can import a key. Creating a key directly in Key Vault is the less complicated method, while importing a key provides total control over how the key is generated.</span></span>
  
<span data-ttu-id="45aeb-298">Для создания ключа непосредственно в ключевых vault, выполните командлет [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-298">To create a key directly in your key vault, run the [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Add-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> -Destination <HSM|Software> -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="45aeb-299">Где:</span><span class="sxs-lookup"><span data-stu-id="45aeb-299">Where:</span></span>
  
-  <span data-ttu-id="45aeb-300">*vaultname* — это имя ключа хранилище, в котором вы хотите создать ключ.</span><span class="sxs-lookup"><span data-stu-id="45aeb-300">*vaultname*  is the name of the key vault in which you want to create the key.</span></span> 
    
-  <span data-ttu-id="45aeb-301">*keyName* — это имя, которое будет нового ключа.</span><span class="sxs-lookup"><span data-stu-id="45aeb-301">*keyname*  is the name you want to give the new key.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="45aeb-p139">Имя клавиш с помощью следующего соглашение об именовании, как описано выше для ключа хранилищах. Таким образом, в меню Сервис, которые показывают только имя ключа, строка собственное описание.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p139">Name keys using a similar naming convention as described above for key vaults. This way, in tools that show only the key name, the string is self-describing.</span></span> 
  
- <span data-ttu-id="45aeb-304">Если для защиты ключа с аппаратного, убедитесь, что указать **HSM** в качестве значения параметра _назначения_ , в противном случае **программного обеспечения**.</span><span class="sxs-lookup"><span data-stu-id="45aeb-304">If you intend to protect the key with an HSM, ensure that you specify **HSM** as the value of the  _Destination_ parameter, otherwise, specify **Software**.</span></span>
    
<span data-ttu-id="45aeb-305">Например:</span><span class="sxs-lookup"><span data-stu-id="45aeb-305">For example,</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination Software -KeyOps wrapKey,unwrapKey
```

<span data-ttu-id="45aeb-306">Чтобы импортировать ключ непосредственно в ключевые хранилище, необходимо иметь Thales nShield аппаратного модуля безопасности.</span><span class="sxs-lookup"><span data-stu-id="45aeb-306">To import a key directly into your key vault, you need to have a Thales nShield Hardware Security Module.</span></span>
  
<span data-ttu-id="45aeb-307">Некоторые организации предпочитают этот подход для установления provenance их ключей и этого метода также предоставляет следующее:</span><span class="sxs-lookup"><span data-stu-id="45aeb-307">Some organizations prefer this approach to establish the provenance of their keys, and the this method also provides the following:</span></span>
  
- <span data-ttu-id="45aeb-308">Набор инструментов, используемый для импорта включает в себя аттестации из Thales, что ключ Exchange ключ (KEK), который используется для шифрования ключа, создаваемые невозможен и создается внутри подлинность HSM, произведена корпорацией Thales.</span><span class="sxs-lookup"><span data-stu-id="45aeb-308">The toolset used for import includes attestation from Thales that the Key Exchange Key (KEK) that is used to encrypt the key you generate is not exportable and is generated inside a genuine HSM that was manufactured by Thales.</span></span>
    
- <span data-ttu-id="45aeb-p140">Набор инструментов включает в себя аттестации из Thales, что мир хранилище Azure ключ безопасности также был создан на подлинность HSM производства Thales. В этом аттестации подтверждает вам, что Майкрософт также использует подлинность Thales оборудования.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p140">The toolset includes attestation from Thales that the Azure Key Vault security world was also generated on a genuine HSM manufactured by Thales. This attestation proves to you that Microsoft is also using genuine Thales hardware.</span></span>
    
<span data-ttu-id="45aeb-p141">Обратитесь к вашей группы безопасности, чтобы определить, требуются ли выше attestations. Подробное описание шагов для создания ключа в локальной и импортировать ключевые помещение Узнайте, [как для создания и перемещения защищенного HSM ключи для ключа хранилище Azure](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Используйте Azure инструкции для создания ключа в каждой ключевые хранилище.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p141">Check with your security group to determine if the above attestations are required. For detailed steps to create a key on-premises and import it into your key vault, see [How to generate and transfer HSM-protected keys for Azure Key Vault](https://azure.microsoft.com/documentation/articles/key-vault-hsm-protected-keys/). Use the Azure instructions to create a key in each key vault.</span></span>
  
### <a name="check-the-recovery-level-of-your-keys"></a><span data-ttu-id="45aeb-314">Установите флажок для уровня восстановления ключи</span><span class="sxs-lookup"><span data-stu-id="45aeb-314">Check the recovery level of your keys</span></span>
<span data-ttu-id="45aeb-315"><a name="CheckKeyRecoveryLevel"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-315"></span></span>

<span data-ttu-id="45aeb-p142">Office 365 требует подписки на хранилище Azure ключ имеет значение не отменить и иметь обратимым удалением включено клавиш, используемых ключа клиента. В этом можно убедиться, посмотрев уровень восстановления на ключи.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p142">Office 365 requires that the Azure Key Vault subscription is set to Do Not Cancel and that the keys used by Customer Key have soft delete enabled. You can confirm this by looking at the recovery level on your keys.</span></span>
  
<span data-ttu-id="45aeb-318">Чтобы проверить уровень восстановления ключа в Windows Azure PowerShell, выполните командлет Get-AzureKeyVaultKey следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-318">To check the recovery level of a key, in Azure PowerShell, run the Get-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname>).Attributes 
```

<span data-ttu-id="45aeb-319">Свойство _Уровень восстановления_ возвращает отличное от значения **Устранимая + ProtectedSubscription**, необходимо изучить раздел и убедитесь, что выполнены все действия, чтобы поместить подписки на список не отменить и наличие обратимым удалением включен на каждом из ключевых хранилищах.</span><span class="sxs-lookup"><span data-stu-id="45aeb-319">If the  _Recovery Level_ property returns anything other than a value of **Recoverable+ProtectedSubscription**, you will need to review this topic and ensure that you have followed all of the steps to put the subscription on the Do Not Cancel list and that you have soft delete enabled on each of your key vaults.</span></span>
  
### <a name="backup-azure-key-vault"></a><span data-ttu-id="45aeb-320">Помещение резервного копирования Azure ключа</span><span class="sxs-lookup"><span data-stu-id="45aeb-320">Backup Azure Key Vault</span></span>
<span data-ttu-id="45aeb-321"><a name="BackupAzureKeyVaultkeys"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-321"></span></span>

<span data-ttu-id="45aeb-p143">Сразу после создания или изменения в раздел создания резервной копии и храните резервного копирования и в автономном режиме. Автономные копии не должен быть подключен к сети, такие как физическое хранилище безопасных или коммерческие услуг. По крайней мере одна копия резервного копирования должны храниться в папке, которая будет доступна в случае аварии. Резервного копирования большие двоичные объекты являются единственным способом восстановления материала ключа следует ключ помещение ключ безвозвратно потеряны или в противном случае отображается из строя. Ключи, внешними по отношению к помещение ключ Azure и завершен хранилище ключа Azure не связаны для резервного копирования, так как метаданные, необходимые для ключа клиента для использования ключа не существует с помощью внешнего ключа. Только резервной копии, созданной из хранилища Azure ключ может использоваться для выполнения операций восстановления с ключом клиента. Очень важно сделать резервную копию ключа хранилище Azure загружаться или создав ключа.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p143">Immediately following creation or any change to a key, perform a backup and store copies of the backup, both online and offline. Offline copies should not be connected to any network, such as in a physical safe or commercial storage facility. At least one copy of the backup should be stored in a location that will be accessible in the event of a disaster. The backup blobs are the sole means of restoring key material should a Key Vault key be permanently destroyed or otherwise rendered inoperable. Keys that are external to Azure Key Vault and were imported to Azure Key Vault do not qualify as a backup because the metadata necessary for Customer Key to use the key does not exist with the external key. Only a backup taken from Azure Key Vault can be used for restore operations with Customer Key. Therefore, it is essential that a backup of Azure Key Vault be made once a key is uploaded or created.</span></span>
  
<span data-ttu-id="45aeb-329">Чтобы создать резервную копию ключа помещение ключ Azure, выполните командлет [AzureKeyVaultKey резервного копирования](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-329">To create a backup of an Azure Key Vault key, run the [Backup-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Backup-AzureKeyVaultKey) cmdlet as follows:</span></span>
```
Backup-AzureKeyVaultKey -VaultName <vaultname> -Name <keyname> 
-OutputFile <filename .backup>

```

<span data-ttu-id="45aeb-330">Убедитесь, что в выходной файл используется суффикс `.backup`.</span><span class="sxs-lookup"><span data-stu-id="45aeb-330">Ensure that your output file uses the suffix  `.backup`.</span></span>
  
<span data-ttu-id="45aeb-p144">Выходной файл, результатом этого командлета шифрования и не может использоваться за пределами Azure ключ хранилище. Резервная копия восстанавливаются только с подпиской Azure, из которого была создана резервная копия.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p144">The output file resulting from this cmdlet is encrypted and cannot be used outside of Azure Key Vault. The backup can be restored only to the Azure subscription from which the backup was taken.</span></span>
  
> [!TIP]
> <span data-ttu-id="45aeb-p145">Для файла вывода выберите сочетание помещение имя и имя ключа. Это делает имя файла собственное описание. Он также гарантирует, что имена файла резервной копии не перекрывались.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p145">For the output file, choose a combination of your vault name and key name. This will make the file name self-describing. It will also ensure that backup file names do not collide.</span></span> 
  
<span data-ttu-id="45aeb-336">Пример:</span><span class="sxs-lookup"><span data-stu-id="45aeb-336">For example:</span></span>
  
```
Backup-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -OutputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

### <a name="validate-azure-key-vault-configuration-settings"></a><span data-ttu-id="45aeb-337">Проверка параметров конфигурации помещение ключ Azure</span><span class="sxs-lookup"><span data-stu-id="45aeb-337">Validate Azure Key Vault configuration settings</span></span>
<span data-ttu-id="45aeb-338"><a name="Validateconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-338"></span></span>

<span data-ttu-id="45aeb-p146">Для выполнения проверки перед использованием ключей в DEP является обязательным, но настоятельно рекомендуется. В частности при использовании действия для настройки ключей и хранилищами отличным от из них, описанных в этом разделе должно проверять работоспособности ресурсов хранилище Azure ключа перед настройкой ключа клиента.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p146">Performing validation before using keys in a DEP is optional, but highly recommended. In particular, if you use steps to set up your keys and vaults other than the ones described in this topic, you should validate the health of your Azure Key Vault resources before you configure Customer Key.</span></span>
  
<span data-ttu-id="45aeb-341">Чтобы убедитесь, что ключи операции get, wrapKey и unwrapKey включено:</span><span class="sxs-lookup"><span data-stu-id="45aeb-341">To verify that your keys have get, wrapKey, and unwrapKey operations enabled:</span></span>
  
<span data-ttu-id="45aeb-342">Используйте командлет [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-342">Run the [Get-AzureRmKeyVault](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureRmKeyVault) cmdlet as follows:</span></span> 
  
```
Get-AzureRMKeyVault -VaultName <vaultname>
```

<span data-ttu-id="45aeb-p147">В выходных данных найдите для политики доступа и Exchange Online идентификатор (GUID) или SharePoint Online идентификатор (GUID) соответствующим образом. Все три выше разрешения должны отображаться в области разрешения для ключей.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p147">In the output, look for the Access Policy and for the Exchange Online identity (GUID) or the SharePoint Online identity (GUID) as appropriate. All three of the above permissions must be shown under Permissions to Keys.</span></span>
  
<span data-ttu-id="45aeb-345">Неправильная настройка политики доступа, выполните командлет Set-AzureRmKeyVaultAccessPolicy следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-345">If the access policy configuration is incorrect, run the Set-AzureRmKeyVaultAccessPolicy cmdlet as follows:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> -PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName <Office 365 appID>
```

<span data-ttu-id="45aeb-346">Например для Exchange Online и Скайп для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="45aeb-346">For example, for Exchange Online and Skype for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName 00000002-0000-0ff1-ce00-000000000000
```

<span data-ttu-id="45aeb-347">Например для SharePoint Online и OneDrive для бизнеса:</span><span class="sxs-lookup"><span data-stu-id="45aeb-347">For example, for SharePoint Online and OneDrive for Business:</span></span>
  
```
Set-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365SP-NA-VaultA1 
-PermissionsToKeys wrapKey,unwrapKey,get -ServicePrincipalName TBD
```

<span data-ttu-id="45aeb-348">Чтобы убедиться, что дату окончания срока действия не установлен для ключей выполните командлет [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-348">To verify that an expiration date is not set for your keys run the [Get-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Get-AzureKeyVaultKey) cmdlet as follows:</span></span> 
  
```
Get-AzureKeyVaultKey -VaultName <vaultname> 
```

<span data-ttu-id="45aeb-p148">Просроченные ключа не может использоваться с ключом клиента и попытка с истекшим сроком действия ключом операции с ошибкой и привести к в недоступности службы. Мы настоятельно рекомендуем, клавиши, которые используются с ключом клиента нет дату окончания срока действия. Срок действия, после набора, не может быть удалена, но может быть изменено на другую дату. Если ключ должен использоваться с датой истечения срока действия задайте, измените значение срока действия 12/31/9999. Клавиши со сроком значение даты, отличное от 12/31/9999 не пройдет проверку Office 365.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p148">An expired key cannot be used by Customer Key and operations attempted with an expired key will fail, and possibly result in a service outage. We strongly recommend that keys used with Customer Key do not have an expiration date. An expiration date, once set, cannot be removed, but can be changed to a different date. If a key must be used that has an expiration date set, change the expiration value to 12/31/9999. Keys with an expiration date set to a date other than 12/31/9999 will not pass Office 365 validation.</span></span>
  
<span data-ttu-id="45aeb-354">Чтобы изменить дату окончания срока действия, который имеет значение для любого значения, кроме 12/31/9999, выполните командлет [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-354">To change an expiration date that has been set to any value other than 12/31/9999, run the [Set-AzureKeyVaultKeyAttribute](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Set-AzureKeyVaultKeyAttribute) cmdlet as follows:</span></span> 
  
```
Set-AzureKeyVaultKeyAttribute -VaultName <vaultname> -Name <keyname> 
-Expires (Get-Date -Date "12/31/9999")
```

> [!CAUTION]
> <span data-ttu-id="45aeb-355">Не задавать даты окончания срока действия ключами шифрования, используемого с ключом клиента.</span><span class="sxs-lookup"><span data-stu-id="45aeb-355">Don't set expiration dates on encryption keys you use with Customer Key.</span></span> 
  
### <a name="obtain-the-uri-for-each-azure-key-vault-key"></a><span data-ttu-id="45aeb-356">Получение URI для каждого ключа помещение ключ Azure</span><span class="sxs-lookup"><span data-stu-id="45aeb-356">Obtain the URI for each Azure Key Vault key</span></span>
<span data-ttu-id="45aeb-357"><a name="GetKeyURI"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-357"></span></span>

<span data-ttu-id="45aeb-p149">После выполнить все действия, описанные в Azure для настройки ключа хранилищах и добавлена ключи, выполните следующую команду для получения URI для ключа в каждой ключевые хранилище. Вам потребуется использовать эти коды URI, при создании и назначение каждого DEP более поздних версий, поэтому сохраните эти сведения в надежном месте. Не забудьте выполнить эту команду один раз для каждого ключа хранилище.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p149">Once you have completed all the steps in Azure to set up your key vaults and added your keys, run the following command to get the URI for the key in each key vault. You will need to use these URIs when you create and assign each DEP later, so save this information in a safe place. Remember to run this command once for each key vault.</span></span>
  
<span data-ttu-id="45aeb-361">В Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="45aeb-361">In Azure PowerShell:</span></span>
  
```
(Get-AzureKeyVaultKey -VaultName <vaultname>).Id
```

## <a name="office-365-setting-up-customer-key-for-exchange-online-and-skype-for-business"></a><span data-ttu-id="45aeb-362">Office 365: Настройка ключа клиента для Exchange Online и Скайп для бизнеса</span><span class="sxs-lookup"><span data-stu-id="45aeb-362">Office 365: Setting up Customer Key for Exchange Online and Skype for Business</span></span>
<span data-ttu-id="45aeb-363"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-363"></span></span>

<span data-ttu-id="45aeb-p150">Прежде чем начать, убедитесь, что вы выполнили действия, необходимые для настройки помещение ключ Azure. Дополнительные сведения содержатся [завершения задачи в хранилище ключа Azure и она Microsoft для ключа клиента](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="45aeb-p150">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="45aeb-366">Для настройки ключа клиента для Exchange Online и Скайп для бизнеса, необходимо выполнить следующие действия с помощью удаленного подключения к Exchange Online с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45aeb-366">To set up Customer Key for Exchange Online and Skype for Business, you will need to perform these steps by remotely connecting to Exchange Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-use-with-exchange-online-and-skype-for-business"></a><span data-ttu-id="45aeb-367">Создание политики шифрования данных (DEP) для использования с Exchange Online и Скайп для бизнеса</span><span class="sxs-lookup"><span data-stu-id="45aeb-367">Create a data encryption policy (DEP) for use with Exchange Online and Skype for Business</span></span>
<span data-ttu-id="45aeb-368"><a name="CreateDEP4EXOSkype"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-368"></span></span>

<span data-ttu-id="45aeb-p151">Предотвращение выполнения данных связан с набор разделов, хранящиеся в хранилище Azure ключ. Назначьте DEP почтового ящика в Office 365. Office 365 будет использовать клавишам в политике для шифрования почтового ящика. Чтобы создать DEP, необходимо коды URI помещение ключ, полученный ранее. В разделе [получить URI для каждого ключа Azure ключ помещение](controlling-your-data-using-customer-key.md#GetKeyURI) инструкции.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p151">A DEP is associated with a set of keys stored in Azure Key Vault. You assign a DEP to a mailbox in Office 365. Office 365 will then use the keys identified in the policy to encrypt the mailbox. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="45aeb-p152">Не забудьте! При создании DEP, задается два разделы, которые находятся в двух различных хранилищах ключ Azure. Убедитесь, что эти разделы находятся в двух разных регионов Azure для обеспечения избыточности географически.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p152">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="45aeb-377">Чтобы создать DEP, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="45aeb-377">To create the DEP, follow these steps:</span></span>
  
1. <span data-ttu-id="45aeb-378">На локальном компьютере с помощью рабочего или школы учетной записи, имеющей права глобального администратора в организации Office 365, [подключение к Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) , выполнив следующую команду Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45aeb-378">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [connect to Exchange Online PowerShell](https://technet.microsoft.com/en-us/library/jj984289%28v=exchg.160%29.aspx) by opening Windows PowerShell and running the following command.</span></span> 
    
   ```
   $UserCredential = Get-Credential
   ```

2. <span data-ttu-id="45aeb-379">В диалоговом окне запрос учетных данных Windows PowerShell введите работу или школе сведений об учетной записи, нажмите **кнопку ОК**и введите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="45aeb-379">In the Windows PowerShell Credential Request dialog box, enter your work or school account information, click **OK**, and then enter the following command.</span></span> 
    
   ```
   $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
   ```

3. <span data-ttu-id="45aeb-380">Выполните следующую команду.</span><span class="sxs-lookup"><span data-stu-id="45aeb-380">Run the following command.</span></span>
    
   ```
   Import-PSSession $Session
   ```

4. <span data-ttu-id="45aeb-381">Чтобы создать DEP, командлет New-DataEncryptionPolicy, введя следующую команду.</span><span class="sxs-lookup"><span data-stu-id="45aeb-381">To create a DEP, use the New-DataEncryptionPolicy cmdlet by typing the following command.</span></span>
    
   ```
   New-DataEncryptionPolicy -Name <PolicyName> -Description "PolicyDescription " -AzureKeyIDs <KeyVaultURI1>, <KeyVaultURI2>
   ```

   <span data-ttu-id="45aeb-382">Где:</span><span class="sxs-lookup"><span data-stu-id="45aeb-382">Where:</span></span>
    
   -  <span data-ttu-id="45aeb-p153">*PolicyName* — это имя, которое будет использоваться для политики. Имена не могут содержать пробелов. Например USA_mailboxes.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p153">*PolicyName*  is the name you want to use for the policy. Names cannot contain spaces. For example, USA_mailboxes.</span></span> 
    
   -  <span data-ttu-id="45aeb-p154">*PolicyDescription* — это понятное описание политики, которая поможет вам Имейте в виду, что политики для. В описании могут содержать пробелов. Например корневой ключ для почтовых ящиков в США и их территорий.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p154">*PolicyDescription*  is a user friendly description of the policy that will help you remember what the policy is for. You can include spaces in the description. For example, Root key for mailboxes in USA and its territories.</span></span> 
    
   -  <span data-ttu-id="45aeb-p155">*KeyVaultURI1* — это URI для первого ключа в политике. Например https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p155">*KeyVaultURI1*  is the URI for the first key in the policy. For example, https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01.</span></span> 
    
   -  <span data-ttu-id="45aeb-p156">*KeyVaultURI2* — это URI для второго ключа в политике. Например https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Для разделения двух URI с запятой и пробелом.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p156">*KeyVaultURI2*  is the URI for the second key in the policy. For example, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02. Separate the two URIs by a comma and a space.</span></span> 
    
   <span data-ttu-id="45aeb-394">Пример.</span><span class="sxs-lookup"><span data-stu-id="45aeb-394">Example:</span></span>
  
   ```
   New-DataEncryptionPolicy -Name USA_mailboxes -Description "Root key for mailboxes in USA and its territories" -AzureKeyIDs https://contoso_EastUSvault01.vault.azure.net/keys/USA_key_01, https://contoso_EastUS2vault01.vault.azure.net/keys/USA_Key_02
   ```

### <a name="assign-a-dep-to-a-mailbox"></a><span data-ttu-id="45aeb-395">Назначение DEP почтовому ящику</span><span class="sxs-lookup"><span data-stu-id="45aeb-395">Assign a DEP to a mailbox</span></span>
<span data-ttu-id="45aeb-396"><a name="assignDEPtomailbox"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-396"></span></span>

<span data-ttu-id="45aeb-p157">Назначение DEP почтовому ящику с помощью командлета Set-Mailbox. После того как политики, Office 365 зашифровывать почтового ящика с ключом, указанный в функции.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p157">Assign the DEP to a mailbox by using the Set-Mailbox cmdlet. Once you assign the policy, Office 365 can encrypt the mailbox with the key designated in the DEP.</span></span>
  
```
Set-Mailbox -Identity <MailboxIdParameter> -DataEncryptionPolicy <PolicyName>
```

<span data-ttu-id="45aeb-p158">Где *MailboxIdParameter* указывает почтовый ящик. Дополнительные сведения о командлет Set-Mailbox можно [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="45aeb-p158">Where *MailboxIdParameter* specifies a mailbox. For more information about the Set-Mailbox cmdlet, see [Set-Mailbox](https://technet.microsoft.com/library/bb123981%28v=exchg.160%29.aspx).</span></span>
  
### <a name="validate-mailbox-encryption"></a><span data-ttu-id="45aeb-401">Проверка шифрования почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="45aeb-401">Validate mailbox encryption</span></span>
<span data-ttu-id="45aeb-402"><a name="validatemailboxencryption"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-402"></span></span>

<span data-ttu-id="45aeb-p159">Шифрование почтового ящика может занять некоторое время. Для назначения политики первый раз перед службу зашифровывать почтового ящика почтового ящика необходимо выполнить перемещение из одной базы данных на другой. Корпорация Майкрософт рекомендует отложить 72 часа перед выполнением проверки шифрования после изменения DEP или впервые DEP назначить почтовому ящику.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p159">Encrypting a mailbox can take some time. For first time policy assignment, the mailbox must also complete the move from one database to another before the service can encrypt the mailbox. We recommend that you wait 72 hours before you attempt to validate encryption after you change a DEP or the first time you assign a DEP to a mailbox.</span></span>
  
<span data-ttu-id="45aeb-406">Командлет Get-MailboxStatistics для определения, если шифруется почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="45aeb-406">Use the Get-MailboxStatistics cmdlet to determine if a mailbox is encrypted.</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl IsEncrypted
```

<span data-ttu-id="45aeb-407">Свойство IsEncrypted возвращает значение **true** при шифровании почтового ящика и значение **false** , если почтовый ящик не зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="45aeb-407">The IsEncrypted property returns a value of **true** if the mailbox is encrypted and a value of **false** if the mailbox is not encrypted.</span></span> 

<span data-ttu-id="45aeb-p160">Время для завершения перемещения почтовых ящиков зависит от того, количество почтовых ящиков, к которым нужно назначить DEP в первый раз, а также размер почтовых ящиков. Если почтовые ящики не зашифрованных после недели с момента назначен DEP, инициировать перемещения почтовых ящиков для зашифрованных почтовых ящиков с помощью командлета New-MoveRequest.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p160">The time to complete mailbox moves depends on the number of mailboxes to which you assign a DEP for the first time, as well as the size of the mailboxes. If the mailboxes have not been encrypted after a week from the time you assigned the DEP, initiate a mailbox move for the unencrypted mailboxes by using the New-MoveRequest cmdlet.</span></span>

```
New-MoveRequest <mailbox alias>
``` 

## <a name="office-365-setting-up-customer-key-for-sharepoint-online-and-onedrive-for-business"></a><span data-ttu-id="45aeb-410">Office 365: Настройка ключа клиента для SharePoint Online и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="45aeb-410">Office 365: Setting up Customer Key for SharePoint Online and OneDrive for Business</span></span>
<span data-ttu-id="45aeb-411"><a name="AzureSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-411"></span></span>

<span data-ttu-id="45aeb-p161">Прежде чем начать, убедитесь, что вы выполнили действия, необходимые для настройки помещение ключ Azure. Дополнительные сведения содержатся [завершения задачи в хранилище ключа Azure и она Microsoft для ключа клиента](controlling-your-data-using-customer-key.md#AzureSteps) .</span><span class="sxs-lookup"><span data-stu-id="45aeb-p161">Before you begin, ensure that you have completed the tasks required to set up Azure Key Vault. See [Complete tasks in Azure Key Vault and Microsoft FastTrack for Customer Key](controlling-your-data-using-customer-key.md#AzureSteps) for information.</span></span> 
  
<span data-ttu-id="45aeb-414">Чтобы настроить ключ клиента для SharePoint Online и OneDrive для бизнеса, необходимо выполнить эти шаги удаленно подключается к SharePoint Online с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45aeb-414">To set up Customer Key for SharePoint Online and OneDrive for Business, you will need to perform these steps by remotely connecting to SharePoint Online with Windows PowerShell.</span></span>
  
### <a name="create-a-data-encryption-policy-dep-for-each-sharepoint-online-and-onedrive-for-business-geo"></a><span data-ttu-id="45aeb-415">Создание политики шифрования данных (DEP) для каждого SharePoint Online и OneDrive для бизнеса географически</span><span class="sxs-lookup"><span data-stu-id="45aeb-415">Create a data encryption policy (DEP) for each SharePoint Online and OneDrive for Business geo</span></span>
<span data-ttu-id="45aeb-416"><a name="CreateDEP4SPOODfB"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-416"></span></span>

<span data-ttu-id="45aeb-p162">Предотвращение выполнения данных связан с набор разделов, хранящиеся в хранилище Azure ключ. Функция DEP применяется для всех данных в одной географическому положению, также называемый географически. Если функция несколькими географически Office 365 (в настоящее время в предварительной версии), можно создать одну DEP на географически. Если вы не используете несколькими географически, можно создать одну DEP в Office 365 для использования с SharePoint Online и OneDrive для бизнеса. Office 365 будет использовать клавишам в DEP для шифрования данных в этой географически. Чтобы создать DEP, необходимо коды URI помещение ключ, полученный ранее. В разделе [получить URI для каждого ключа Azure ключ помещение](controlling-your-data-using-customer-key.md#GetKeyURI) инструкции.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p162">A DEP is associated with a set of keys stored in Azure Key Vault. You apply a DEP to all of your data in one geographic location, also called a geo. If you use the multi-geo feature of Office 365 (currently in Preview), you can create one DEP per geo. If you are not using multi-geo, you can create one DEP in Office 365 for use with SharePoint Online and OneDrive for Business. Office 365 will then use the keys identified in the DEP to encrypt your data in that geo. To create the DEP, you need the Key Vault URIs you obtained earlier. See [Obtain the URI for each Azure Key Vault key](controlling-your-data-using-customer-key.md#GetKeyURI) for instructions.</span></span> 
  
<span data-ttu-id="45aeb-p163">Не забудьте! При создании DEP, задается два разделы, которые находятся в двух различных хранилищах ключ Azure. Убедитесь, что эти разделы находятся в двух разных регионов Azure для обеспечения избыточности географически.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p163">Remember! When you create a DEP, you specify two keys that reside in two different Azure Key Vaults. Ensure that these keys are located in two separate Azure regions to ensure geo-redundancy.</span></span>
  
<span data-ttu-id="45aeb-427">Для создания DEP, необходимо подключиться к SharePoint Online с помощью Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="45aeb-427">To create a DEP, you need to remotely connect to SharePoint Online by using Windows PowerShell.</span></span>
  
1. <span data-ttu-id="45aeb-428">На локальном компьютере с помощью рабочего или школы учетной записи, имеющей права глобального администратора в организации Office 365, [подключиться к SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span><span class="sxs-lookup"><span data-stu-id="45aeb-428">On your local computer, using a work or school account that has global administrator permissions in your Office 365 organization, [Connect to SharePoint Online Powershell](https://technet.microsoft.com/library/fp161372.aspx).</span></span>
    
2. <span data-ttu-id="45aeb-429">В Microsoft SharePoint Online командной консоли выполните командлет [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-429">In the Microsoft SharePoint Online Management Shell, run the [Register-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843950.aspx) cmdlet as follows:</span></span> 
    
   ```
   Register-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -PrimaryKeyVaultName <PrimaryKeyVaultName> -PrimaryKeyName <PrimaryKeyName> -PrimaryKeyVersion <PrimaryKeyVersion> -SecondaryKeyVaultName <SecondaryKeyVaultName> -SecondaryKeyName <SecondaryKeyName> -SecondaryKeyVersion <SecondaryKeyVersion>
   ```

   <span data-ttu-id="45aeb-p164">При регистрации DEP шифрования начинается с данными в географически. Этот процесс может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p164">When you register the DEP, encryption begins on the data in the geo. This can take some time.</span></span>
    
### <a name="validate-encryption-of-group-sites-team-sites-and-onedrive-for-business"></a><span data-ttu-id="45aeb-432">Проверка шифрования группы сайтов, веб-сайтов групп и OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="45aeb-432">Validate encryption of Group Sites, Team Sites, and OneDrive for Business</span></span>
<span data-ttu-id="45aeb-433"><a name="validateencryptionSPO"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-433"></span></span>

<span data-ttu-id="45aeb-434">Вы можете проверить состояние шифрования с помощью командлета Get-SPODataEncryptionPolicy следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-434">You can check on the status of encryption by running the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

<span data-ttu-id="45aeb-435">Выходные данные этот командлет включает в себя:</span><span class="sxs-lookup"><span data-stu-id="45aeb-435">The output from this cmdlet includes:</span></span>
  
- <span data-ttu-id="45aeb-436">URI первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="45aeb-436">The URI of the primary key.</span></span>
    
- <span data-ttu-id="45aeb-437">URI дополнительный ключ.</span><span class="sxs-lookup"><span data-stu-id="45aeb-437">The URI of the secondary key.</span></span>
    
- <span data-ttu-id="45aeb-p165">Состояние шифрования для географически. Следующие возможные состояния.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p165">The encryption status for the geo. Possible states include:</span></span>
    
  - <span data-ttu-id="45aeb-440">**Незарегистрированных:** Ключ шифрования клиента еще не были применены.</span><span class="sxs-lookup"><span data-stu-id="45aeb-440">**Unregistered:** Customer Key encryption has not yet been applied.</span></span> 
    
  - <span data-ttu-id="45aeb-p166">**Регистрации:** Клиент ключ шифрования был применен и файлы находятся в процессе выполнения шифрования. Если ваше географически это состояние означает, вы также показывается сведения на какой процент сайтов в географически завершены, таким образом, можно отслеживать ход выполнения шифрования.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p166">**Registering:** Customer Key encryption has been applied and your files are in the process of being encrypted. If your geo is in this state, you'll also be shown information on what percentage of sites in the geo are complete so that you can monitor encryption progress.</span></span> 
    
  - <span data-ttu-id="45aeb-443">**Зарегистрирован:** Клиент ключ шифрования был применен и зашифрованных все файлы всех веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="45aeb-443">**Registered:** Customer Key encryption has been applied, and all files in all sites have been encrypted.</span></span> 
    
  - <span data-ttu-id="45aeb-p167">**Ваши:** Ключевые путем развертывания находится в стадии разработки. Если ваше географически это состояние, вы также показывается сведения на какой процент сайты выполнить операцию ключевые ролл (en) таким образом, можно отслеживать ход выполнения.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p167">**Rolling:** A key roll is in progress. If your geo is in this state, you'll also be shown information on what percentage of sites have completed the key roll operation so that you can monitor progress.</span></span> 
    
## <a name="managing-customer-key-for-office-365"></a><span data-ttu-id="45aeb-446">Управление ключом клиента для Office 365</span><span class="sxs-lookup"><span data-stu-id="45aeb-446">Managing Customer Key for Office 365</span></span>
<span data-ttu-id="45aeb-447"><a name="ManageCustomerKey"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-447"></span></span>

<span data-ttu-id="45aeb-448">После настройки ключа клиента Office 365, можно выполнить эти задачи дополнительное управление.</span><span class="sxs-lookup"><span data-stu-id="45aeb-448">After you've set up Customer Key for Office 365, you can perform these additional management tasks.</span></span>
  
- [<span data-ttu-id="45aeb-449">Восстановление ключа хранилище Azure разделов</span><span class="sxs-lookup"><span data-stu-id="45aeb-449">Restore Azure Key Vault keys</span></span>](controlling-your-data-using-customer-key.md#RestoreAzureKeyVaultKeys)
    
- [<span data-ttu-id="45aeb-450">Ваши или вращающимся ключа в хранилище Azure ключ, используйте с ключом клиента</span><span class="sxs-lookup"><span data-stu-id="45aeb-450">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>](controlling-your-data-using-customer-key.md#RollCKkey)
    
- [<span data-ttu-id="45aeb-451">Управление разрешениями для ключа хранилище</span><span class="sxs-lookup"><span data-stu-id="45aeb-451">Manage key vault permissions</span></span>](controlling-your-data-using-customer-key.md#Managekeyvaultperms)
    
- [<span data-ttu-id="45aeb-452">Определение DEP, назначенных почтовому ящику</span><span class="sxs-lookup"><span data-stu-id="45aeb-452">Determine the DEP assigned to a mailbox</span></span>](controlling-your-data-using-customer-key.md#DeterminemailboxDEP)
    
### <a name="restore-azure-key-vault-keys"></a><span data-ttu-id="45aeb-453">Восстановление ключа хранилище Azure разделов</span><span class="sxs-lookup"><span data-stu-id="45aeb-453">Restore Azure Key Vault keys</span></span>
<span data-ttu-id="45aeb-454"><a name="RestoreAzureKeyVaultKeys"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-454"></span></span>

<span data-ttu-id="45aeb-p168">Перед выполнением восстановления, используйте возможности восстановления, предоставляемые обратимым удалением. Все разделы, которые используются с ключом клиента должны иметь обратимым удалением включен. Обратимым удалением действует как recycle bin и разрешает восстановление до 90 дней без необходимости восстановления. Восстановление должно быть необходимо только в условиях чрезмерную или нестандартный, например если ключ или ключевые помещение теряется. Если необходимо восстановить ключ для использования с ключом клиента в Azure PowerShell используйте командлет Restore-AzureKeyVaultKey следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-p168">Before performing a restore, use the recovery capabilities provided by soft delete. All keys that are used with Customer Key are required to have soft delete enabled. Soft delete acts like a recycle bin and allows recovery for up to 90 days without the need to restore. Restore should only be required in extreme or unusual circumstances, for example if the key or key vault is lost. If you must restore a key for use with Customer Key, in Azure PowerShell, run the Restore-AzureKeyVaultKey cmdlet as follows:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName <vaultname> -InputFile <filename>
```

<span data-ttu-id="45aeb-460">Пример:</span><span class="sxs-lookup"><span data-stu-id="45aeb-460">For example:</span></span>
  
```
Restore-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -InputFile Contoso-O365EX-NA-VaultA1-Key001-Backup-20170802.backup
```

<span data-ttu-id="45aeb-p169">Если ключ с таким же именем уже существует в хранилище ключа, произойдет сбой операции восстановления. Восстановление AzureKeyVaultKey восстанавливает все основные версии и все метаданные для ключа, включая имя раздела.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p169">If a key with the same name already exists in the key vault, the restore operation will fail. Restore-AzureKeyVaultKey restores all key versions and all metadata for the key including the key name.</span></span>
  
### <a name="rolling-or-rotating-a-key-in-azure-key-vault-that-you-use-with-customer-key"></a><span data-ttu-id="45aeb-463">Ваши или вращающимся ключа в хранилище Azure ключ, используйте с ключом клиента</span><span class="sxs-lookup"><span data-stu-id="45aeb-463">Rolling or rotating a key in Azure Key Vault that you use with Customer Key</span></span>
<span data-ttu-id="45aeb-464"><a name="RollCKkey"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-464"></span></span>

<span data-ttu-id="45aeb-p170">Ваши ключи не является обязательным, либо помещение ключ Azure, либо по ключу клиента. Кроме того разделы, защищенные с помощью аппаратного практически невозможно безопасности. Даже в том случае, если были корневой раздел во временном пользовании вредоносных actor нет отсутствуют средства использования для расшифровки данных, поскольку только кода Office 365 может использовать его. Тем не менее ваши ключа поддерживается ключа клиента.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p170">Rolling keys is not required by either Azure Key Vault or by Customer Key. In addition, keys that are protected with an HSM are virtually impossible to compromise. Even if a root key were in the possession of a malicious actor there is no feasible means of using it to decrypt data, since only Office 365 code knows how to use it. However, rolling a key is supported by Customer Key.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="45aeb-p171">Только восстановить ключ шифрования, которая будет использоваться с ключом клиента для существует снимите флажок технические причина или требование соответствия определяет, что вам необходимо откатить ключ. Кроме того не удаляйте разделы, или были связаны с политиками. Если ключи, будут содержимое зашифрован с предыдущих разделов. К примеру во время активной почтовые ящики будут зашифрованы заново часто, неактивных, отключенные и отключенных почтовых ящиков может по-прежнему зашифрован с предыдущих разделов. SharePoint Online выполняет резервное копирование содержимого для целей восстановления и восстановления, поэтому может быть по-прежнему архивных контента с использованием старых ключей.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p171">Only roll an encryption key that you use with Customer Key when a clear technical reason exists or a compliance requirement dictates that you have to roll the key. In addition, do not delete any keys that are or were associated with policies. When you roll your keys, there will be content encrypted with the previous keys. For example, while active mailboxes will be re-encrypted frequently, inactive, disconnected, and disabled mailboxes may still be encrypted with the previous keys. SharePoint Online performs backup of content for restore and recovery purposes, so there may still be archived content using older keys. </span></span><br/> <span data-ttu-id="45aeb-p172">Чтобы обеспечить безопасность данных, SharePoint Online позволяет не более одной операции отката ключ к обработке за раз. Если вам нужно развертывать оба разделов ключевые так, вам будет ожидать первого операции ключа roll полностью завершена. Мы рекомендуем является составляйте работы ключевых roll с разными интервалами, чтобы эта проблема не возникает.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p172">To ensure the safety of your data, SharePoint Online will allow no more than one Key Roll operation to be in progress at a time. If you want to roll both of the keys in a key vault, you'll need to wait for the first key roll operation to fully complete. Our recommendation is to stagger your key roll operations at different intervals, so that this is not an issue.</span></span> 
  
<span data-ttu-id="45aeb-p173">Если ключ, вы запрашиваете новой версии существующего ключа. Чтобы запросить новую версию существующий раздел, используйте же командлет [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey)с тем же синтаксисом, который использовался для создания ключа в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p173">When you roll a key, you are requesting a new version of an existing key. In order to request a new version of an existing key, you use the same cmdlet, [Add-AzureKeyVaultKey](https://docs.microsoft.com/powershell/module/AzureRM.KeyVault/Add-AzureKeyVaultKey), with the same syntax that you used to create the key in the first place.</span></span>
  
<span data-ttu-id="45aeb-479">Пример:</span><span class="sxs-lookup"><span data-stu-id="45aeb-479">For example:</span></span>
  
```
Add-AzureKeyVaultKey -VaultName Contoso-O365EX-NA-VaultA1 -Name Contoso-O365EX-NA-VaultA1-Key001 -Destination HSM -KeyOps @('wrapKey','unwrapKey') -NotBefore (Get-Date -Date "12/27/2016 12:01 AM")
```

<span data-ttu-id="45aeb-p174">В этом примере ключ с именем **Contoso-O365EX-NA-VaultA1-Key001** уже существует в **Contoso-O365EX-NA-VaultA1** помещение нового ключа версии создается. Операция добавляет новую версию ключа. Эта операция сохраняет предыдущих версий ключа в раздел: журнал версий, таким образом, по-прежнему можно расшифровать данные, зашифрованные с помощью этого ключа. После завершения развертывания любую клавишу, который связан с DEP необходимо снова запустить дополнительные командлет, чтобы убедиться, что ключ клиента начинается с помощью нового ключа.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p174">In this example, since a key named **Contoso-O365EX-NA-VaultA1-Key001** already exists in the **Contoso-O365EX-NA-VaultA1** vault, a new key version will be created. The operation adds a new key version. This operation preserves the previous key versions in the key's version history, so that data previously encrypted with that key can still be decrypted. Once you have completed rolling any key that is associated with a DEP, you must then run an additional cmdlet to ensure Customer Key begins using the new key.</span></span> 
  
#### <a name="enable-exchange-online-and-skype-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="45aeb-484">Разрешить Exchange Online и Скайп для бизнеса, чтобы использовать новый ключ после отката или поворот ключей в хранилище ключа Azure</span><span class="sxs-lookup"><span data-stu-id="45aeb-484">Enable Exchange Online and Skype for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="45aeb-485">Если любой из ключи помещение ключ Azure, связанного с DEP используется с Exchange Online и Скайп для бизнеса, необходимо выполнить следующую команду, чтобы обновить DEP и включить Office 365 начать работу с использованием нового ключа.</span><span class="sxs-lookup"><span data-stu-id="45aeb-485">When you roll either of the Azure Key Vault keys associated with a DEP used with Exchange Online and Skype for Business, you must run the following command to update the DEP and enable Office 365 to start using the new key.</span></span>
  
<span data-ttu-id="45aeb-486">Чтобы указать ключ клиента для использования нового ключа шифрования почтовых ящиков в Office 365, выполните командлет Set-DataEncryptionPolicy следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-486">To instruct Customer Key to use the new key to encrypt mailboxes in Office 365 run the Set-DataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Set-DataEncryptionPolicy <policyname> -Refresh 
```

<span data-ttu-id="45aeb-p175">В течение 48 часов станет связанное с ключом обновленные active почтовые ящики, зашифрованные с помощью этой политики. Выполните действия в [Определение DEP, назначенных почтовому ящику](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) для проверки значения для свойства DataEncryptionPolicyID для почтового ящика. Значение для этого свойства будет изменить, когда была применена обновленный ключ.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p175">Within 48 hours, the active mailboxes encrypted using this policy will become associated with the updated key. Use the steps in [Determine the DEP assigned to a mailbox](controlling-your-data-using-customer-key.md#DeterminemailboxDEP) to check the value for the DataEncryptionPolicyID property for the mailbox. The value for this property will change once the updated key has been applied.</span></span> 
  
#### <a name="enable-sharepoint-online-and-onedrive-for-business-to-use-a-new-key-after-you-roll-or-rotate-keys-in-azure-key-vault"></a><span data-ttu-id="45aeb-490">Включение SharePoint Online и OneDrive для бизнеса использовать новый ключ после отката или поворот ключей в хранилище ключа Azure</span><span class="sxs-lookup"><span data-stu-id="45aeb-490">Enable SharePoint Online and OneDrive for Business to use a new key after you roll or rotate keys in Azure Key Vault</span></span>

<span data-ttu-id="45aeb-491">Если любой из ключи помещение ключ Azure, связанного с DEP используется с SharePoint Online и OneDrive для бизнеса, необходимо запустить командлет [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) для обновления DEP и включить Office 365 начать работу с использованием нового ключа.</span><span class="sxs-lookup"><span data-stu-id="45aeb-491">When you roll either of the Azure Key Vault keys associated with a DEP used with SharePoint Online and OneDrive for Business, you must run the [Update-SPODataEncryptionPolicy](https://technet.microsoft.com/library/mt843948.aspx) cmdlet to update the DEP and enable Office 365 to start using the new key.</span></span> 
  
```
Update-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl> -KeyVaultName <ReplacementKeyVaultName> -KeyName <ReplacementKeyName> -KeyVersion <ReplacementKeyVersion> -KeyType <Primary | Secondary>
```

<span data-ttu-id="45aeb-p176">Будет запущен ключевых roll операции для SharePoint Online и OneDrive для бизнеса. Это действие не интерпретации. Для просмотра хода выполнения ключа откатить операции, выполните командлет Get-SPODataEncryptionPolicy следующим образом:</span><span class="sxs-lookup"><span data-stu-id="45aeb-p176">This will start the key roll operation for SharePoint Online and OneDrive for Business. This action is not immediate. To see the progress of the key roll operation, run the Get-SPODataEncryptionPolicy cmdlet as follows:</span></span>
  
```
Get-SPODataEncryptionPolicy -Identity <SPOAdminSiteUrl>
```

### <a name="manage-key-vault-permissions"></a><span data-ttu-id="45aeb-495">Управление разрешениями для ключа хранилище</span><span class="sxs-lookup"><span data-stu-id="45aeb-495">Manage key vault permissions</span></span>
<span data-ttu-id="45aeb-496"><a name="Managekeyvaultperms"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-496"></span></span>

<span data-ttu-id="45aeb-p177">Доступны несколько командлеты, позволяющие просматривать и при необходимости удаления ключа помещение разрешений. Может понадобиться для удаления разрешений, например, когда сотрудник покидает группу.</span><span class="sxs-lookup"><span data-stu-id="45aeb-p177">Several cmdlets are available that enable you to view and, if necessary, remove key vault permissions. You might need to remove permissions, for example, when an employee leaves the team.</span></span>
  
<span data-ttu-id="45aeb-499">Для ключа помещение разрешения на просмотр, выполните командлет Get-AzureRmKeyVault:</span><span class="sxs-lookup"><span data-stu-id="45aeb-499">To view key vault permissions, run the Get-AzureRmKeyVault cmdlet:</span></span>
  
```
Get-AzureRmKeyVault -VaultName <vaultname>
```

<span data-ttu-id="45aeb-500">Пример:</span><span class="sxs-lookup"><span data-stu-id="45aeb-500">For example:</span></span>
  
```
Get-AzureRmKeyVault -VaultName Contoso-O365EX-NA-VaultA1
```

<span data-ttu-id="45aeb-501">Чтобы удалить разрешения администратора, выполните командлет Remove-AzureRmKeyVaultAccessPolicy:</span><span class="sxs-lookup"><span data-stu-id="45aeb-501">To remove an administrator's permissions, run the Remove-AzureRmKeyVaultAccessPolicy cmdlet:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName <vaultname> 
-UserPrincipalName <UPN of user>
```

<span data-ttu-id="45aeb-502">Пример:</span><span class="sxs-lookup"><span data-stu-id="45aeb-502">For example:</span></span>
  
```
Remove-AzureRmKeyVaultAccessPolicy -VaultName Contoso-O365EX-NA-VaultA1 
-UserPrincipalName alice@contoso.com
```

### <a name="determine-the-dep-assigned-to-a-mailbox"></a><span data-ttu-id="45aeb-503">Определение DEP, назначенных почтовому ящику</span><span class="sxs-lookup"><span data-stu-id="45aeb-503">Determine the DEP assigned to a mailbox</span></span>
<span data-ttu-id="45aeb-504"><a name="DeterminemailboxDEP"> </a></span><span class="sxs-lookup"><span data-stu-id="45aeb-504"></span></span>

<span data-ttu-id="45aeb-p178">Чтобы определить DEP, назначенных почтовому ящику, используйте командлет Get-MailboxStatistics. Командлет возвращает уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="45aeb-p178">To determine the DEP assigned to a mailbox, use the Get-MailboxStatistics cmdlet. The cmdlet returns a unique identifier (GUID).</span></span>
  
```
Get-MailboxStatistics -Identity <GeneralMailboxOrMailUserIdParameter> | fl DataEncryptionPolicyID
```

<span data-ttu-id="45aeb-p179">Где *GeneralMailboxOrMailUserIdParameter* указывает почтовый ящик. Дополнительные сведения о командлет Get-MailboxStatistics можно [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="45aeb-p179">Where *GeneralMailboxOrMailUserIdParameter* specifies a mailbox. For more information about the Get-MailboxStatistics cmdlet, see [Get-MailboxStatistics](https://technet.microsoft.com/library/bb124612%28v=exchg.160%29.aspx).</span></span>
  
<span data-ttu-id="45aeb-509">Используйте идентификатор GUID для получения понятное имя DEP, назначенных почтовому ящику, выполнив следующий командлет.</span><span class="sxs-lookup"><span data-stu-id="45aeb-509">Use the GUID to find out the friendly name of the DEP to which the mailbox is assigned by running the following cmdlet.</span></span>
  
```
Get-DataEncryptionPolicy <GUID>
```

<span data-ttu-id="45aeb-510">Где *GUID* — это идентификатор GUID, возвращаемых командлетом Get-MailboxStatistics в предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="45aeb-510">Where *GUID* is the GUID returned by the Get-MailboxStatistics cmdlet in the previous step.</span></span> 
  

