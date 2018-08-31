---
title: Применение или удаление политики удаления документов для сайта
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3e92668-f9b2-46ee-8e5e-c623870588b6
description: Организациям часто приходится хранить документы в течение определенного периода времени в соответствии с нормативными, законодательными или другими требованиями. Однако хранение документов дольше, чем требуется, может привести к возникновению юридических рисков. Поэтому организации могут создать политику удаления документов для сайта. Например, общие бизнес-документы могут в обязательном порядке удаляться через пять лет после их создания.
ms.openlocfilehash: abee0da7adfba6f653743d503f8b30770ee93c40
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535258"
---
# <a name="apply-or-remove-a-document-deletion-policy-for-a-site"></a><span data-ttu-id="ac7c9-105">Применение или удаление политики удаления документов для сайта</span><span class="sxs-lookup"><span data-stu-id="ac7c9-105">Apply or remove a document deletion policy for a site</span></span>

<span data-ttu-id="ac7c9-p102">Организациям часто приходится хранить документы в течение определенного периода времени в соответствии с нормативными, законодательными или другими требованиями. Однако хранение документов дольше, чем требуется, может привести к возникновению юридических рисков. Поэтому организации могут создать политику удаления документов для сайта. Например, общие бизнес-документы могут в обязательном порядке удаляться через пять лет после их создания.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p102">Organizations are often subject to compliance, legal, or other regulations that require them to retain documents for a certain period of time. However, retaining documents for longer than required can expose the organization to legal risk. For this reason, your organization may have created a document deletion policy for your site — for example, general business documents might be required to be deleted five years after they were created.</span></span>
  
<span data-ttu-id="ac7c9-109">В зависимости от организации существуют такие политики удаления документов:</span><span class="sxs-lookup"><span data-stu-id="ac7c9-109">Depending on your organization, a document deletion policy might be:</span></span>
  
- <span data-ttu-id="ac7c9-110">**Обязательный** Владелец сайта не может отказаться от обязательной политики, которая автоматически применяется к сайту.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-110">**Mandatory** A site owner can't opt out of a mandatory policy, which is automatically applied to the site.</span></span> 
    
- <span data-ttu-id="ac7c9-111">**Стандартная** Стандартная политика автоматически применяется к сайту, но его владелец может:</span><span class="sxs-lookup"><span data-stu-id="ac7c9-111">**Default** A default policy is automatically applied to a site, but a site owner can:</span></span> 
    
  - <span data-ttu-id="ac7c9-112">Выбрать другую политику, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-112">Choose another policy if available.</span></span>
    
  - <span data-ttu-id="ac7c9-113">Полностью отказаться от политики, если она не соответствует контенту сайта.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-113">Opt out of the policy entirely if it is not relevant to the content in the site.</span></span>
    
- <span data-ttu-id="ac7c9-114">**Не обязательная и не стандартная** В этом случае политика не применяется к сайту автоматически, и его владелец должен применить одну из них.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-114">**Neither mandatory nor default** In this case, no policy is automatically applied to the site, and the site owner needs to take action to apply one.</span></span> 
    
<span data-ttu-id="ac7c9-p103">Политика удаления документов может содержать несколько правил. Например, одно правило может предписывать удалять документы через один год после их создания, а другое правило — удалять документы через один год после последнего изменения. Если политика содержит несколько правил, вы можете выбрать то из них, которое лучше всего подходит для вашего сайта. Правило удаления будет применено ко всем библиотекам на сайте. Только одна политика и одно правило могут быть активными в сайте одновременно. Как и политика, правило может быть стандартным и применяться автоматически в случае применения политики.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p103">A document deletion policy may contain more than one rule — for example, one rule might say delete documents one year after they were created, but another rule might say delete documents one year after they were last modified. If a policy contains more than one rule, you can select the rule that best applies to your site. The delete rule will be applied to all libraries within the site. Only one policy and one rule can be active in a site at one time. Like a policy, a rule can be set as default, so that it is applied automatically when the policy is applied.</span></span>
  
<span data-ttu-id="ac7c9-p104">Наконец, политики удаления документов наследуются. Все подсайты наследуют выбранную для сайта политику или правило. Владелец подсайта может прервать наследование, выбрав другую политику или правило. Выбирая политику или правило, примите во внимание подсайты, находящиеся ниже вашего сайта.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p104">Finally, document deletion policies are inherited. When you select a policy or rule for your site, that selection is inherited by all subsites, although an owner of a subsite can break inheritance by selecting a different policy or rule. When you select a policy or rule, consider the content of any subsites below your site.</span></span>
  
## <a name="view-the-document-deletion-policies-available-in-a-site-collection"></a><span data-ttu-id="ac7c9-123">Просмотр политик удаления документов, доступных в семействе веб-сайтов</span><span class="sxs-lookup"><span data-stu-id="ac7c9-123">View the document deletion policies available in a site collection</span></span>

<span data-ttu-id="ac7c9-p105">Организация может назначать различные политики для разных семейств веб-сайтов. На уровне семейства веб-сайтов его владелец может просматривать все политики удаления документов, доступные для такого семейства веб-сайтов. Политики могут быть доступными для шаблона семейства веб-сайтов (и, следовательно, для всех семейств веб-сайтов, созданных из этого шаблона) или для определенного семейства веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p105">Your organization may assign different policies to different site collections. At the site collection level, an owner of a site collection can view all of the document deletion policies that are available to that site collection. The policies may have been made available to the site collection template (and therefore all site collections created from this template) or to this specific site collection.</span></span>
  
1. <span data-ttu-id="ac7c9-127">На сайте верхнего уровня в семействе сайтов, в правом верхнем углу выберите элемент **Параметры** [значок с шестеренкой] \> **Параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-127">In the top-level site in the site collection, in the upper-right corner, choose **Settings** [gear icon] \> **Site Settings**.</span></span>
    
2. <span data-ttu-id="ac7c9-128">В разделе **Администрирование семейства веб-сайтов** \> **политики удаления документов**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-128">Under **Site Collection Administration** \> **Document Deletion Policies**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ac7c9-p106">Ссылки **Политики удаления документов** не отображается, если политики, назначенные в коллекции веб-сайтов. Кроме того, ссылка не отображается сразу же после назначения политики сайта, может потребоваться до 24 часов с при политик назначаются при отображении ссылки **Политики удаления документов** .</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p106">The **Document Deletion Policies** link won't appear unless policies have been assigned to the site collection. Also, the link doesn't appear immediately after policies have been assigned to the site — it can take up to 24 hours from when the policies are assigned to when the **Document Deletion Policies** link appears.</span></span> 
  
3. <span data-ttu-id="ac7c9-131">На этой странице вы можете просмотреть такие сведения:</span><span class="sxs-lookup"><span data-stu-id="ac7c9-131">On this page you can view:</span></span>
    
  - <span data-ttu-id="ac7c9-p107">Текущая назначенная политика и связанные с ней правила. Выберите политику для просмотра правил в правой области.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p107">The currently assigned policies and the associated rules. Select a policy to view the rules in the right pane.</span></span>
    
  - <span data-ttu-id="ac7c9-134">При наличии стандартной политики в столбце **Стандартная** отображается **Да**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-134">The default policy, if any, displays **Yes** in the **Default** column.</span></span> 
    
  - <span data-ttu-id="ac7c9-135">Если политика назначена как **Обязательная**, под списком отображается сообщение.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-135">A message is displayed below the list if the policy has been assigned as **Mandatory**.</span></span>
    
<span data-ttu-id="ac7c9-p108">Этот список предназначен только для просмотра, чтобы владелец сайта мог просмотреть все доступные политики и правила. Сведения о применении политики см. в разделе далее.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p108">This list is view only, for the site collection owner to see all of the available policies and rules. To apply a policy, see the next section.</span></span>
  
![Просмотр политик удаления документов, назначенных семейству веб-сайтов](media/f2c0433b-2bb5-407d-a364-ae07c9627176.png)
  
## <a name="apply-or-remove-a-document-deletion-policy-for-a-site"></a><span data-ttu-id="ac7c9-139">Применение или удаление политики удаления документов для сайта</span><span class="sxs-lookup"><span data-stu-id="ac7c9-139">Apply or remove a document deletion policy for a site</span></span>

<span data-ttu-id="ac7c9-140">Как владелец сайта или семейства веб-сайтов ваша организация может создавать политики, которые вы можете применять к своему сайту или полностью отказываться от них.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-140">As a site owner or site collection owner, your organization may have created policies that you can either apply to your site or opt out of entirely.</span></span>
  
1. <span data-ttu-id="ac7c9-141">В правом верхнем углу выберите элемент **Параметры** [значок с шестеренкой] \> **Параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-141">In the upper-right corner, choose **Settings** [gear icon] \> **Site Settings**.</span></span>
    
2. <span data-ttu-id="ac7c9-142">В разделе **Администрирование** \> **политики удаления документов**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-142">Under **Site Administration** \> **Document Deletion Policies**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="ac7c9-p109">Ссылки **Политики удаления документов** не отображается, если политики, назначенные в коллекции веб-сайтов. Кроме того, ссылка не отображается сразу же после назначения политики сайта, может потребоваться до 24 часов с при политик назначаются при отображении ссылки **Политики удаления документов** .</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p109">The **Document Deletion Policies** link won't appear unless policies have been assigned to the site collection. Also, the link doesn't appear immediately after policies have been assigned to the site — it can take up to 24 hours from when the policies are assigned to when the **Document Deletion Policies** link appears.</span></span> 
  
3. <span data-ttu-id="ac7c9-145">Выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-145">Do one of the following:</span></span>
    
  - <span data-ttu-id="ac7c9-146">**Для применения политики** Выберите политику \> выберите правило в ней \> **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-146">**To apply a policy** Select a policy \> select a rule in that policy \> **Save**.</span></span>
    
    <span data-ttu-id="ac7c9-p110">Только одна политика и одно правило могут быть активными в сайте одновременно. Ваша организация может предоставить несколько политик и правил, из которых можно выбрать, либо всего одну политику или правило.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p110">Only one policy and one rule can be active in a site at one time. Your organization may provide several policies and rules to choose from, or only one policy or rule.</span></span>
    
    ![Выберите параметр политики](media/f7c7c055-fca7-4a4f-bb97-63e35a65beac.png)
  
  - <span data-ttu-id="ac7c9-150">**Отказ от политики** Выберите **отказаться: Обратите внимание, удалить** \> **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-150">**To opt out of a policy** Choose **Opt-Out: Do Note Delete** \> **Save**.</span></span>
    
    <span data-ttu-id="ac7c9-p111">Как владелец сайта вы можете отказаться от политики удаления документов, если определите, что такая политика неприменима к контенту вашего сайта. Однако невозможно отказаться от политики, которая помечена как **Обязательная**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p111">As a site owner, you can opt out of a document deletion policy if you determine that the policy is not applicable to the content in your site. However, you cannot opt out of a policy that has been marked as **Mandatory**.</span></span>
    
    ![Параметр явного в работе](media/efac709c-bef7-4a02-a09d-5bc7d2b4ec63.png)
  
## <a name="document-deletion-policies-override-other-policies"></a><span data-ttu-id="ac7c9-154">Политики удаления документов переопределяют другие политики</span><span class="sxs-lookup"><span data-stu-id="ac7c9-154">Document deletion policies override other policies</span></span>

<span data-ttu-id="ac7c9-155">На сайте могут использоваться другие политики хранения и удаления контента:</span><span class="sxs-lookup"><span data-stu-id="ac7c9-155">A site may use other policies for retaining and deleting content:</span></span>
  
- <span data-ttu-id="ac7c9-156">Политики типов контента для семейства веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-156">Content type policies for the site collection.</span></span>
    
- <span data-ttu-id="ac7c9-157">Политики управления сведениями для списка или библиотеки.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-157">Information management policies for a list or library.</span></span>
    
<span data-ttu-id="ac7c9-p112">Применение политики удаления документов на сайт, где уже использует политики типов контента или политики управления сведениями для списка или библиотеки, эти политики, игнорируются ли время политики удаления документов. Если учитываются другие политики, появится сообщение «Контента на этом сайте используется политики удаления документов».</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p112">If you apply a document deletion policy to a site that already uses content type policies or information management policies for a list or library, those policies are ignored while the document deletion policy is in effect. If other policies are ignored, you will see the message "Content on this site uses Document Deletion Policies".</span></span>
  
<span data-ttu-id="ac7c9-p113">Это означает, что вы должны планировать использование на сайте исключительно политик, предназначенных для структурированного (политики управления сведениями и политики типов контента) или неструктурированного контента (политики удаления документов), но не тех и других одновременно. Если вы откажитесь от политики удаления документов, предупреждение не отобразится и другие типы политик будут продолжать работать.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p113">This means you should plan for a site to use only policies meant for structured content (information management policies and content type policies) or unstructured content (document deletion policies), not both. If you opt out of a document deletion policy, the warning will not be displayed and other types of policies will continue to work.</span></span>
  
<span data-ttu-id="ac7c9-162">Политика удаления документов не влияет на политики сайта.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-162">Site policies are not affected by document deletion policies.</span></span>
  
### <a name="determine-if-content-type-policies-are-being-ignored"></a><span data-ttu-id="ac7c9-163">Определение того, игнорируются ли политики типов контента</span><span class="sxs-lookup"><span data-stu-id="ac7c9-163">Determine if content type policies are being ignored</span></span>

<span data-ttu-id="ac7c9-p114">При использовании веб-узла политики типов контента и вы теперь это сообщение, эти политики больше не действует. Чтобы восстановить политики типов контента, можно удалить политики удаления документов с веб-узла, как описано выше, если имеется параметр отказаться. Если имеется возможность отключить, политики удаления документов является обязательным и обратитесь специалисты по соответствию требованиям в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p114">If your site was using content type policies and you now see this message, those policies are no longer in effect. To restore the content type policies, you can remove the document deletion policy from your site, as described earlier, if there's an opt-out option available. If there's no option to opt out, the document deletion policy is mandatory, and you need to contact the compliance officer in your organization.</span></span>
  
1. <span data-ttu-id="ac7c9-167">В правом верхнем углу выберите элемент **Параметры** [значок с шестеренкой] \> **Параметры сайта**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-167">In the upper-right corner, choose **Settings** [gear icon] \> **Site Settings**.</span></span>
    
2. <span data-ttu-id="ac7c9-168">В разделе **Администрирование** \> **Шаблоны политики типов контента**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-168">Under **Site Administration** \> **Content Type Policy Templates**.</span></span>
    
    ![Предупреждение на сайте использования политики удаления документов](media/4cc3d703-9aff-4695-9670-f78c291c0010.png)
  
### <a name="determine-if-information-management-policies-are-being-ignored"></a><span data-ttu-id="ac7c9-170">Определение того, игнорируются ли политики управления сведениями</span><span class="sxs-lookup"><span data-stu-id="ac7c9-170">Determine if information management policies are being ignored</span></span>

<span data-ttu-id="ac7c9-p115">Если сайт был с помощью политик управления сведениями и отобразиться это сообщение, эти политики больше не действует. Чтобы восстановить политики управления сведениями, можно удалить политики удаления документов с веб-узла, как описано выше, если имеется параметр отказаться. Если имеется возможность отключить, политики удаления документов является обязательным и обратитесь специалисты по соответствию требованиям в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-p115">If your site was using information management policies and you now see this message, those policies are no longer in effect. To restore the information management policies, you can remove the document deletion policy from your site, as described earlier, if there's an opt-out option available. If there's no option to opt out, the document deletion policy is mandatory, and you need to contact the compliance officer in your organization.</span></span>
  
- <span data-ttu-id="ac7c9-174">Для списка или библиотеки на ленте \> вкладку **Библиотека** \> **Параметры библиотеки** \> в разделе **разрешения и управление** \> **Параметры политики управления сведениями**.</span><span class="sxs-lookup"><span data-stu-id="ac7c9-174">For a list or library, on the Ribbon \> **Library** tab \> **Library Settings** \> under **Permissions and Management** \> **Information Management Policy Settings**.</span></span>
    
    ![Предупреждение на сайте использования политики удаления документов](media/3f043057-a741-4cd8-a165-6d139b986064.png)
  
## <a name="see-also"></a><span data-ttu-id="ac7c9-176">См. также</span><span class="sxs-lookup"><span data-stu-id="ac7c9-176">See also</span></span>

[<span data-ttu-id="ac7c9-177">Обзор политик удаления документов</span><span class="sxs-lookup"><span data-stu-id="ac7c9-177">Overview of document deletion policies</span></span>](document-deletion-policies.md)
  
[<span data-ttu-id="ac7c9-178">Создание политики удаления документов</span><span class="sxs-lookup"><span data-stu-id="ac7c9-178">Create a document deletion policy</span></span>](create-a-document-deletion-policy.md)

