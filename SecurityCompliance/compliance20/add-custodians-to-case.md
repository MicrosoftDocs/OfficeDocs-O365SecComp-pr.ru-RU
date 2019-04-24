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
ms.openlocfilehash: fe208f4a9f7927d8481d5c6ec8b901baafb98626
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243591"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="f4b09-102">Добавление custodians к расширенному варианту обнаружения электронных данных (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="f4b09-102">Add custodians to an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="f4b09-103">С помощью расширенного обнаружения электронных данных (Preview) вы можете использовать встроенное средство управления хранитель, чтобы координировать рабочие процессы для управления custodians и определения релевантных источников данных кустодиал в этом случае.</span><span class="sxs-lookup"><span data-stu-id="f4b09-103">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case.</span></span> <span data-ttu-id="f4b09-104">При добавлении хранитель система может автоматически определять и размещать удержания на основном почтовом ящике Exchange и на сайте OneDrive для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="f4b09-104">When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site.</span></span> <span data-ttu-id="f4b09-105">При проведении обнаружения вы также можете обнаружить и сопоставить дополнительные почтовые ящики или сайты, к которым хранитель обращался в прошлое или в Teams, участником которых является хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-105">As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="f4b09-106">Используйте следующий рабочий процесс для добавления и управления custodians в дополнительных случаях обнаружения электронных данных (Preview) в центре безопасности _Амп_ соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="f4b09-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

![Вкладка "Управление хранитель"](../media/CustodianMgtPage.png)


## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="f4b09-108">Шаг 1: определение потенциальных custodians</span><span class="sxs-lookup"><span data-stu-id="f4b09-108">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="f4b09-109">Первым шагом является определение подходящей custodiansи для вашей важности.</span><span class="sxs-lookup"><span data-stu-id="f4b09-109">The first step is to identify the appropriate custodians for your matter.</span></span> <span data-ttu-id="f4b09-110">Чтобы добавить custodians к случаю, необходимо быть участником группы "руководители обнаружения электронных данных" или "Администраторы обнаружения электронных данных".</span><span class="sxs-lookup"><span data-stu-id="f4b09-110">To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

![Определение потенциальных custodians](../media/AddCustodianStep1.png)

<span data-ttu-id="f4b09-112">Чтобы добавить custodians к существующему расширенному случаю обнаружения электронных данных (Предварительная версия), выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="f4b09-112">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="f4b09-113">На странице **Advanced eDiscovery (предварительНая версия)** перейдите к своему случаю.</span><span class="sxs-lookup"><span data-stu-id="f4b09-113">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="f4b09-114">После выбора варианта перейдите на вкладку **custodians** и нажмите кнопку **+ Добавить хранитель**.</span><span class="sxs-lookup"><span data-stu-id="f4b09-114">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="f4b09-115">Выберите custodians, который вы хотите добавить в дело.</span><span class="sxs-lookup"><span data-stu-id="f4b09-115">Choose the custodians that you want to add to the case.</span></span> <span data-ttu-id="f4b09-116">Для начала введите Поиск и выберите пользователей из Azure Active Directory вашей организации.</span><span class="sxs-lookup"><span data-stu-id="f4b09-116">You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="f4b09-117">После завершения работы со списком custodians нажмите кнопку **Далее** , чтобы начать определять потенциальные источники данных.</span><span class="sxs-lookup"><span data-stu-id="f4b09-117">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
  
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="f4b09-118">Необязательно Шаг 2: выбор источников данных хранитель</span><span class="sxs-lookup"><span data-stu-id="f4b09-118">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="f4b09-119">После добавления custodians к случаю можно воспользоваться Office 365, чтобы помочь вам определить и сохранить основные источники данных хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-119">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources.</span></span> <span data-ttu-id="f4b09-120">Следующий шаг в этом рабочем процессе — выбор источников данных, принадлежащих custodians, указанному в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="f4b09-120">The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

![Выбор источников данных Кустодиал](../media/AddCustodianStep2.png)

<span data-ttu-id="f4b09-122">Идентификация источников данных хранитель:</span><span class="sxs-lookup"><span data-stu-id="f4b09-122">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="f4b09-123">Для каждого хранитель выберите **Exchange** , если вы хотите, чтобы система автоматически определяла и СОА основной почтовый ящик Exchange хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-123">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="f4b09-124">Для каждого хранитель выберите **OneDrive** , если вы хотите, чтобы система автоматически определяла и СОА основной URL-адрес OneDrive хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-124">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="f4b09-125">После того как вы сделаете выбор, система автоматически попытается определить источники данных и добавить их в ваш случай.</span><span class="sxs-lookup"><span data-stu-id="f4b09-125">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="f4b09-126">Нажмите кнопку **Далее** , чтобы начать сопоставление дополнительных источников данных с хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-126">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="f4b09-127">Необязательно Шаг 3: сопоставление дополнительных источников данных</span><span class="sxs-lookup"><span data-stu-id="f4b09-127">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="f4b09-128">В зависимости от вашего случая можно добавить почтовые ящики, в которых в данный момент хранитель может использоваться заданный, группы, в которых в данный момент находится хранитель, или сайты, к которым у хранитель есть доступ в прошлое.</span><span class="sxs-lookup"><span data-stu-id="f4b09-128">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past.</span></span> <span data-ttu-id="f4b09-129">Кроме первичных источников данных хранитель, вы можете добавить дополнительные источники данных Office 365 в хранитель или использовать Office 365, чтобы помочь определить потенциально релевантные источники данных.</span><span class="sxs-lookup"><span data-stu-id="f4b09-129">In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

![Сопоставление дополнительных источников данных](../media/AddCustodianStep3.PNG)

<span data-ttu-id="f4b09-131">Сопоставление почтовых ящиков, сайтов или рабочих групп с определенным хранитель:</span><span class="sxs-lookup"><span data-stu-id="f4b09-131">To map mailboxes, sites, or teams to a specific custodian:</span></span>
1. <span data-ttu-id="f4b09-132">Нажмите кнопку **Добавить** , чтобы назначить расположение содержимого, например почтовые ящики, сайты и команды, определенному хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-132">Select **Add** to assign content locations, like mailboxes, sites, and Teams, to a specific custodian.</span></span> 

2. <span data-ttu-id="f4b09-133">В всплывающем меню укажите следующее: ![сопоставление источников данных](../media/AddCustodianStep4.PNG)</span><span class="sxs-lookup"><span data-stu-id="f4b09-133">In the flyout, specify the following: ![Map Data Sources](../media/AddCustodianStep4.PNG)</span></span>
  -  <span data-ttu-id="f4b09-134">**Почтовые ящики Exchange** — выберите **Пользователи, группы или Teams** , а затем снова нажмите кнопку **выбрать пользователей, группы или Teams** .</span><span class="sxs-lookup"><span data-stu-id="f4b09-134">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again.</span></span> <span data-ttu-id="f4b09-135">Чтобы указать почтовые ящики, которые необходимо назначить выбранному хранитель, используйте поле поиска для поиска почтовых ящиков пользователей и групп рассылки.</span><span class="sxs-lookup"><span data-stu-id="f4b09-135">To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups.</span></span> <span data-ttu-id="f4b09-136">Можно также назначить связанный почтовый ящик для группы Office 365 или группы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f4b09-136">You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="f4b09-137">Установите флажок Пользователь, группа, группа, нажмите кнопку **выбрать**, а затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="f4b09-137">Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f4b09-138">При нажатии кнопки выбрать пользователей, группы или Teams для указания почтовых ящиков, отображается пустое средство выбора почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="f4b09-138">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty.</span></span> <span data-ttu-id="f4b09-139">Это вызвано мерами по повышению скорости работы.</span><span class="sxs-lookup"><span data-stu-id="f4b09-139">This is by design to enhance performance.</span></span> <span data-ttu-id="f4b09-140">Чтобы добавить пользователей в этот список, введите в поле поиска имя (не менее 3 символов).</span><span class="sxs-lookup"><span data-stu-id="f4b09-140">To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
     - <span data-ttu-id="f4b09-141">**Сайты SharePoint** — щелкните **выбрать сайты** , а затем выберите пункт **выбрать сайты** еще раз, чтобы указать дополнительные сайты SharePoint и OneDrive для бизнеса, которые вы хотите назначить выбранному хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-141">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian.</span></span> <span data-ttu-id="f4b09-142">Вы также можете добавить URL-адрес сайта SharePoint для группы Office 365 или группы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f4b09-142">You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="f4b09-143">Введите URL-адрес для каждого сайта, который необходимо назначить.</span><span class="sxs-lookup"><span data-stu-id="f4b09-143">Type the URL for each site that you want to assign.</span></span> <span data-ttu-id="f4b09-144">Нажмите кнопку **выбрать**, а затем кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="f4b09-144">Click **Choose**, and then click **Done**.</span></span>
     - <span data-ttu-id="f4b09-145">**Microsoft** Teams — выберите команду **выбрать Teams** и снова нажмите кнопку **выбрать Teams** , чтобы просмотреть список групп Microsoft Teams, участником которых является хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-145">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today.</span></span> <span data-ttu-id="f4b09-146">Выберите команды, которые вы хотите добавить в свой хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-146">Select the Teams that you would like to add to your custodian.</span></span> <span data-ttu-id="f4b09-147">После выбора система автоматически определит _Амп_ выберите связанный сайт SharePoint и поЧтовые ящики групп, связанные с этой командой Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f4b09-147">Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team.</span></span> <span data-ttu-id="f4b09-148">Нажмите кнопку **выбрать**, а затем кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="f4b09-148">Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="f4b09-149">Чтобы добавить дополнительные Microsoft Teams, вам потребуется отдельно добавить почтовый ящик и сайт SharePoint, как показано выше.</span><span class="sxs-lookup"><span data-stu-id="f4b09-149">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="f4b09-150">По завершении сопоставления источников вы можете просмотреть общее количество почтовых ящиков, сайтов и Teams для custodians, который вы только что добавили.</span><span class="sxs-lookup"><span data-stu-id="f4b09-150">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added.</span></span> <span data-ttu-id="f4b09-151">После завершения работы с источниками данных, относящимися к определенному хранитель, это сопоставление будет поддерживаться и расширено до коллекции обнаружения электронных данных, обработки и проверки рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="f4b09-151">When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="f4b09-152">Необязательно Шаг 4: помещение custodians на удержание</span><span class="sxs-lookup"><span data-stu-id="f4b09-152">(Optional) Step 4: Place custodians on hold</span></span>

![Размещение удержаний](../media/AddCustodianStep5.PNG)

<span data-ttu-id="f4b09-154">После завершения работы с custodians и источниками данных, которые вы хотите добавить в ваш случай, можно поместить некоторые или все custodians в режим удержания.</span><span class="sxs-lookup"><span data-stu-id="f4b09-154">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold.</span></span> <span data-ttu-id="f4b09-155">Когда вы помещаете хранитель на удержание, контент, сопоставленный с этим пользователем, будет удерживаться до тех пор, пока вы не освободите хранитель из случая или пока не удалите удержание.</span><span class="sxs-lookup"><span data-stu-id="f4b09-155">When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold.</span></span> <span data-ttu-id="f4b09-156">В некоторых случаях может потребоваться добавить custodians к случаю, не помещая их на удержание.</span><span class="sxs-lookup"><span data-stu-id="f4b09-156">In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="f4b09-157">Чтобы поместить выбранные custodians и источники данных на удержание, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="f4b09-157">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="f4b09-158">Проверьте настройки хранитель и установите флажок, чтобы поместить каждую хранитель в удержание.</span><span class="sxs-lookup"><span data-stu-id="f4b09-158">Verify your custodian selections and select the checkbox to place each custodian on hold.</span></span> <span data-ttu-id="f4b09-159">После включения хранитель в удержание политика удержания хранитель, содержащая все источники кустодиал, будет автоматически создана.</span><span class="sxs-lookup"><span data-stu-id="f4b09-159">After a custodian is placed on hold, a custodian hold policy containing all custodial sources will be automatically created.</span></span> <span data-ttu-id="f4b09-160">Если флажок не установлен, хранитель и выбранные источники данных будут добавлены к этому случаю, но содержимое не будет сохранено.</span><span class="sxs-lookup"><span data-stu-id="f4b09-160">If the option is not checked, the custodian and selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="f4b09-161">Перейдите на вкладку **удержания** и выберите **политику хранения хранитель**.</span><span class="sxs-lookup"><span data-stu-id="f4b09-161">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="f4b09-162">Нажмите кнопку **изменить** , чтобы просмотреть все выбранные источники данных хранитель.</span><span class="sxs-lookup"><span data-stu-id="f4b09-162">Click **Edit** to view all the selected custodian data sources.</span></span>

   
