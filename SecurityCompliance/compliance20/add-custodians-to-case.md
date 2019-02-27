---
title: Добавление custodians к расширенному варианту обнаружения электронных данных (Предварительная версия)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 730e1fe40756bcb38f3b071137828072f4e2dcb5
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296722"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="5309d-102">Добавление custodians к расширенному варианту обнаружения электронных данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="5309d-102">Add custodians to an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="5309d-p101">С помощью расширенного обнаружения электронных данных (Preview) вы можете использовать встроенное средство управления хранитель, чтобы координировать рабочие процессы для управления custodians и определения релевантных источников данных кустодиал в этом случае. При добавлении хранитель система может автоматически определять и размещать удержания на основном почтовом ящике Exchange и на сайте OneDrive для бизнеса. При проведении обнаружения вы также можете обнаружить и сопоставить дополнительные почтовые ящики или сайты, к которым хранитель обращался в прошлое или в Teams, участником которых является хранитель.</span><span class="sxs-lookup"><span data-stu-id="5309d-p101">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case. When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site. As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="5309d-106">Используйте следующий рабочий процесс для добавления и управления custodians в дополнительных случаях обнаружения электронных данных (Preview) в центре безопасности _Амп_ соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="5309d-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

![Вкладка "Управление хранитель"](../media/CustodianMgtPage.png)


## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="5309d-108">Шаг 1: определение потенциальных custodians</span><span class="sxs-lookup"><span data-stu-id="5309d-108">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="5309d-p102">Первым шагом является определение подходящей custodiansи для вашей важности. Чтобы добавить custodians к случаю, необходимо быть участником группы "руководители обнаружения электронных данных" или "Администраторы обнаружения электронных данных".</span><span class="sxs-lookup"><span data-stu-id="5309d-p102">The first step is to identify the appropriate custodians for your matter. To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

![Определение потенциальных custodians](../media/AddCustodianStep1.png)

<span data-ttu-id="5309d-112">Чтобы добавить custodians к существующему расширенному случаю обнаружения электронных данных (Предварительная версия), выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5309d-112">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="5309d-113">На странице **Advanced eDiscovery (предварительНая версия)** перейдите к своему случаю.</span><span class="sxs-lookup"><span data-stu-id="5309d-113">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="5309d-114">После выбора варианта перейдите на вкладку **custodians** и нажмите кнопку **+ Добавить хранитель**.</span><span class="sxs-lookup"><span data-stu-id="5309d-114">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="5309d-p103">Выберите custodians, который вы хотите добавить в дело. Для начала введите Поиск и выберите пользователей из Azure Active Directory вашей организации.</span><span class="sxs-lookup"><span data-stu-id="5309d-p103">Choose the custodians that you want to add to the case. You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="5309d-117">После завершения работы со списком custodians нажмите кнопку **Далее** , чтобы начать определять потенциальные источники данных.</span><span class="sxs-lookup"><span data-stu-id="5309d-117">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
  
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="5309d-118">Необязательно Шаг 2: выбор источников данных хранитель</span><span class="sxs-lookup"><span data-stu-id="5309d-118">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="5309d-p104">После добавления custodians к случаю можно воспользоваться Office 365, чтобы помочь вам определить и сохранить основные источники данных хранитель. Следующий шаг в этом рабочем процессе — выбор источников данных, принадлежащих custodians, указанному в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="5309d-p104">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources. The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

![Выбор источников данных Кустодиал](../media/AddCustodianStep2.png)

<span data-ttu-id="5309d-122">Идентификация источников данных хранитель:</span><span class="sxs-lookup"><span data-stu-id="5309d-122">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="5309d-123">Для каждого хранитель выберите **Exchange** , если вы хотите, чтобы система автоматически определяла и СОА основной почтовый ящик Exchange хранитель.</span><span class="sxs-lookup"><span data-stu-id="5309d-123">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="5309d-124">Для каждого хранитель выберите **OneDrive** , если вы хотите, чтобы система автоматически определяла и СОА основной URL-адрес OneDrive хранитель.</span><span class="sxs-lookup"><span data-stu-id="5309d-124">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="5309d-125">После того как вы сделаете выбор, система автоматически попытается определить источники данных и добавить их в ваш случай.</span><span class="sxs-lookup"><span data-stu-id="5309d-125">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="5309d-126">Нажмите кнопку **Далее** , чтобы начать сопоставление дополнительных источников данных с хранитель.</span><span class="sxs-lookup"><span data-stu-id="5309d-126">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="5309d-127">Необязательно Шаг 3: сопоставление дополнительных источников данных</span><span class="sxs-lookup"><span data-stu-id="5309d-127">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="5309d-p105">В зависимости от вашего случая можно добавить почтовые ящики, в которых в данный момент хранитель может использоваться заданный, группы, в которых в данный момент находится хранитель, или сайты, к которым у хранитель есть доступ в прошлое. Кроме первичных источников данных хранитель, вы можете добавить дополнительные источники данных Office 365 в хранитель или использовать Office 365, чтобы помочь определить потенциально релевантные источники данных.</span><span class="sxs-lookup"><span data-stu-id="5309d-p105">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past. In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

![Сопоставление дополнительных источников данных](../media/AddCustodianStep3.PNG)

<span data-ttu-id="5309d-131">Сопоставление почтовых ящиков, сайтов или рабочих групп с определенным хранитель:</span><span class="sxs-lookup"><span data-stu-id="5309d-131">To map mailboxes, sites, or teams to a specific custodian:</span></span>

1. <span data-ttu-id="5309d-132">Выберите **Update (обновить** ), чтобы назначить расположение содержимого, например почтовые ящики, сайты и команды, определенному хранитель.</span><span class="sxs-lookup"><span data-stu-id="5309d-132">Select **Update** to assign content locations, like mailboxes, sites, and Teams to a specific custodian.</span></span> 

2. <span data-ttu-id="5309d-133">В всплывающем меню укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="5309d-133">In the flyout, specify the following:</span></span>
   
    -  <span data-ttu-id="5309d-p106">**Почтовые ящики Exchange** — выберите **Пользователи, группы или Teams** , а затем снова нажмите кнопку **выбрать пользователей, группы или Teams** . Чтобы указать почтовые ящики, которые необходимо назначить выбранному хранитель, используйте поле поиска для поиска почтовых ящиков пользователей и групп рассылки. Можно также назначить связанный почтовый ящик для группы Office 365 или группы Майкрософт. Установите флажок Пользователь, группа, группа, нажмите кнопку **выбрать**, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="5309d-p106">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again. To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups. You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team. Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="5309d-p107">При нажатии кнопки выбрать пользователей, группы или Teams для указания почтовых ящиков, отображается пустое средство выбора почтовых ящиков. Это сделано для улучшения производительности. Чтобы добавить пользователей в этот список, введите в поле поиска имя (не менее 3 символов).</span><span class="sxs-lookup"><span data-stu-id="5309d-p107">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
     - <span data-ttu-id="5309d-p108">**Сайты SharePoint** — щелкните **выбрать сайты** , а затем выберите пункт **выбрать сайты** еще раз, чтобы указать дополнительные сайты SharePoint и OneDrive для бизнеса, которые вы хотите назначить выбранному хранитель. Вы также можете добавить URL-адрес сайта SharePoint для группы Office 365 или группы Майкрософт. Введите URL-адрес для каждого сайта, который необходимо назначить. Нажмите кнопку **выбрать**, а затем кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="5309d-p108">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian. You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team. Type the URL for each site that you want to assign. Click **Choose**, and then click **Done**.</span></span>
     - <span data-ttu-id="5309d-p109">**Microsoft** Teams — выберите команду **выбрать Teams** и снова нажмите кнопку **выбрать Teams** , чтобы просмотреть список групп Microsoft Teams, участником которых является хранитель. Выберите команды, которые вы хотите добавить в свой хранитель. После выбора система автоматически определит _Амп_ выберите связанный сайт SharePoint и поЧтовые ящики групп, связанные с этой командой Майкрософт. Нажмите кнопку **выбрать**, а затем кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="5309d-p109">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today. Select the Teams that you would like to add to your custodian. Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team. Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="5309d-149">Чтобы добавить дополнительные Microsoft Teams, вам потребуется отдельно добавить почтовый ящик и сайт SharePoint, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="5309d-149">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="5309d-p110">По завершении сопоставления источников вы можете просмотреть общее количество почтовых ящиков, сайтов и Teams для custodians, который вы только что добавили. После завершения работы с источниками данных, относящимися к определенному хранитель, это сопоставление будет поддерживаться и расширено до коллекции обнаружения электронных данных, обработки и проверки рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="5309d-p110">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added. When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="5309d-152">Необязательно Шаг 4: помещение custodians на удержание</span><span class="sxs-lookup"><span data-stu-id="5309d-152">(Optional) Step 4: Place custodians on hold</span></span>

<span data-ttu-id="5309d-p111">После завершения работы с custodians и источниками данных, которые вы хотите добавить в ваш случай, можно поместить некоторые или все custodians в режим удержания. Когда вы помещаете хранитель на удержание, контент, сопоставленный с этим пользователем, будет удерживаться до тех пор, пока вы не освободите хранитель из случая или пока не удалите удержание. В некоторых случаях может потребоваться добавить custodians к случаю, не помещая их на удержание.</span><span class="sxs-lookup"><span data-stu-id="5309d-p111">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold. When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold. In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="5309d-156">Чтобы поместить выбранные custodians и источники данных на удержание, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5309d-156">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="5309d-p112">Проверьте настройки хранитель и установите флажок, чтобы поместить каждую хранитель в удержание. После включения хранитель в удержание политика удержания хранитель, содержащая все источники кустодиал, будет автоматически создана. Если флажок не установлен, хранитель и выбранные источники данных будут добавлены к этому случаю, но содержимое не будет сохранено.</span><span class="sxs-lookup"><span data-stu-id="5309d-p112">Verify your custodian selections and select the checkbox to place each custodian on hold. After a custodian is placed on hold, a custodian hold policy containing all custodial sources will be automatically created. If the option is not checked, the custodian and selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="5309d-160">Перейдите на вкладку **удержания** и выберите **политику хранения хранитель**.</span><span class="sxs-lookup"><span data-stu-id="5309d-160">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="5309d-161">Нажмите кнопку **изменить** , чтобы просмотреть все выбранные источники данных хранитель.</span><span class="sxs-lookup"><span data-stu-id="5309d-161">Click **Edit** to view all the selected custodian data sources.</span></span>

    ![Размещение удержаний](../media/AddCustodianStep4.PNG)
