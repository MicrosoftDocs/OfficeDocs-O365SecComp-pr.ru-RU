---
title: Общие сведения о хранении, зависящем от возникновения события
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: При помощи меток в Office 365 можно задавать периоды хранения с учетом возникновения событий определенного типа. Событие активирует начало периода хранения, и ко всему содержимому с меткой для событий такого типа применяются соответствующие действия по хранению. Хранение, зависящее от возникновения события, обычно используется в процессе управления записями.
ms.openlocfilehash: ceb4b2fde10e43235d8d310243fe56cce1a2b240
ms.sourcegitcommit: a79eb9907759d4cd849c3f948695a9ff890b19bf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2019
ms.locfileid: "30866365"
---
# <a name="overview-of-event-driven-retention"></a><span data-ttu-id="73095-105">Общие сведения о хранении, зависящем от возникновения события</span><span class="sxs-lookup"><span data-stu-id="73095-105">Overview of event-driven retention</span></span>

<span data-ttu-id="73095-p102">Период хранения содержимого часто зависит от возраста содержимого. Например, можно хранить документы в течение семи лет с даты создания и затем удалять их. Но с помощью меток в Office 365 можно задать период хранения, начинающийся при возникновении события определенного типа. Событие активирует начало периода хранения, и ко всему содержимому с меткой для событий такого типа применяются соответствующие действия по хранению.</span><span class="sxs-lookup"><span data-stu-id="73095-p102">When you retain content, the retention period is often based on the age of the content - for example, you might retain documents for seven years after they're created and then delete them. But with labels in Office 365, you can also base a retention period on when a specific type of event occurs. The event triggers the start of the retention period, and all content with a label applied for that type of event get the label's retention actions enforced on them.</span></span>
  
<span data-ttu-id="73095-109">Метки с хранением, зависящим от возникновения события, можно использовать, например, в таких случаях:</span><span class="sxs-lookup"><span data-stu-id="73095-109">For example, you can use labels with event-driven retention for:</span></span>
  
- <span data-ttu-id="73095-p103">**Уход сотрудника из организации.** Предположим, что записи о сотруднике нужно хранить в течение 10 лет с момента его ухода из организации. Через 10 лет все документы, касающиеся найма и результатов работы этого сотрудника, расторжения трудовых отношений с ним нужно уничтожить. Событие, активирующее начало 10-летнего периода хранения, — это уход сотрудника из организации.</span><span class="sxs-lookup"><span data-stu-id="73095-p103">**Employees leaving the organization** Suppose that employee records must be retained for 10 years from the time an employee leaves the organization. After 10 years elapse, all documents related to the hiring, performance, and termination of that employee need to be disposed. The event that triggers the 10-year retention period is the employee leaving the organization.</span></span> 
    
- <span data-ttu-id="73095-p104">**Завершение срока действия контракта.** Предположим, что все записи, относящиеся к контрактам, нужно хранить пять лет после окончания срока действия контракта. Событие, активирующее начало 5-летнего периода хранения, — это завершение срока действия контракта.</span><span class="sxs-lookup"><span data-stu-id="73095-p104">**Contract expiration** Suppose that all records related to contracts need to be retained for five years from the time the contract expires. The event that triggers the five-year retention period is the expiration of the contract.</span></span> 
    
- <span data-ttu-id="73095-p105">**Время существования продукта.** У вашей организации могут быть требования к хранению, связанные с датой последнего выпуска продуктов, в отношении такого контента, как технические спецификации. В таком случае последний выпуск — это событие, активирующее начало периода хранения.</span><span class="sxs-lookup"><span data-stu-id="73095-p105">**Product lifetime** Your organization might have retention requirements related to the last manufacturing date of products for content such as technical specifications. In this case, the last manufacturing date is the event that triggers the retention period.</span></span> 
    
<span data-ttu-id="73095-p106">Хранение, зависящее от возникновения события, обычно используется в процессе управления записями. Это означает следующее:</span><span class="sxs-lookup"><span data-stu-id="73095-p106">Event-driven retention is typically used as part of a records-management process. This means that:</span></span>
  
- <span data-ttu-id="73095-p107">Метки, основанные на событиях, обычно относят содержимое к категории записей. Дополнительные сведения см. в статье [Использование средства "Поиск контента" для поиска содержимого с определенной меткой хранения](labels.md#using-content-search-to-find-all-content-with-a-specific-retention-label-applied-to-it).</span><span class="sxs-lookup"><span data-stu-id="73095-p107">Labels based on events also usually classify content as a record. For more information, see [Using Content Search to find all content with a specific retention label applied to it](labels.md#using-content-search-to-find-all-content-with-a-specific-retention-label-applied-to-it).</span></span>
    
- <span data-ttu-id="73095-121">Документ, который был объявлен записью, но для которого событие-триггер еще не наступило, хранится в течение неограниченного времени (окончательно удалить записи невозможно), пока событие не активирует период его хранения.</span><span class="sxs-lookup"><span data-stu-id="73095-121">A document that's been declared as a record but whose event trigger has not yet happened is retained indefinitely (records can't be permanently deleted), until an event triggers that document's retention period.</span></span>
    
- <span data-ttu-id="73095-p108">Метки, основанные на событиях, обычно служат триггером для проверки перед ликвидацией в конце периода хранения, поэтому документовед может вручную просмотреть и удалить содержимое. Дополнительные сведения см. в статье [Общие сведения о проверках перед ликвидацией](disposition-reviews.md).</span><span class="sxs-lookup"><span data-stu-id="73095-p108">Labels based on events usually trigger a disposition review at the end of the retention period, so that a records manager can manually review and dispose the content. For more information, see [Overview of disposition reviews](disposition-reviews.md).</span></span>
    
<span data-ttu-id="73095-p109">Метка, основанная на событии, имеет такие же возможности, что и любая другая метка в Office 365. Дополнительные сведения см. в статье [Общие сведения о метках](labels.md).</span><span class="sxs-lookup"><span data-stu-id="73095-p109">A label based on an event has the same capabilities as any label in Office 365. To learn more, see [Overview of labels](labels.md).</span></span>
    
## <a name="understanding-the-relationship-between-event-types-labels-events-and-asset-ids"></a><span data-ttu-id="73095-126">Взаимосвязь между типами событий, метками, событиями и идентификаторами ресурсов</span><span class="sxs-lookup"><span data-stu-id="73095-126">Understanding the relationship between event types, labels, events, and asset IDs</span></span>

<span data-ttu-id="73095-p110">Чтобы успешно применять хранение, зависящее от события, важно понимать, как связаны между собой типы событий, метки, события и идентификаторы ресурсов. Пояснения к приведенной ниже схеме вы найдете сразу под ней.</span><span class="sxs-lookup"><span data-stu-id="73095-p110">To successfully use event-driven retention, it's important to understand the relationship between event types, labels, events, and asset IDs as illustrated here. An explanation follows the diagram.</span></span>
  
![Схема взаимосвязей между типами событий, метками, событиями и идентификаторами ресурсов](media/a5141a6b-61ca-4a60-9ab0-24e6bb45bbdb.png)
  
![Схема взаимосвязей между типами событий, метками, событиями и идентификаторами ресурсов](media/ce89a91f-49aa-4b5a-933c-ac3a13dccd5d.png)
  
1. <span data-ttu-id="73095-p111">Сначала нужно создать метки для разных типов содержимого, а затем связать их с типом события. Например, метки для разных типов записей и материалов по продуктам связываются с типом события "Время существования продукта", так как эти записи необходимо хранить 10 лет с момента прекращения существования продукта.</span><span class="sxs-lookup"><span data-stu-id="73095-p111">You create labels for different types of content and then associate them with a type of event. For example, labels for different types of product files and records are associated with an event type named Product Lifetime because those records must be retained for 10 years from the time the product reaches its end of life.</span></span>
    
2. <span data-ttu-id="73095-p112">Пользователи (как правило, документоведы) применяют эти метки к содержимому и (если речь идет о документах SharePoint и OneDrive) вводят для каждого из них идентификатор ресурса. В этом примере идентификатор ресурса — это имя или код продукта, используемые организацией. Таким образом, каждой записи продукта присвоена метка, каждая запись имеет свойство, содержащее идентификатор ресурса. На схеме показано **все содержимое** для всех записей продуктов в организации, и для каждого элемента предусмотрен идентификатор ресурса продукта, которому посвящена запись.</span><span class="sxs-lookup"><span data-stu-id="73095-p112">Users (typically records managers) apply those labels to content and (for SharePoint and OneDrive documents) enter an asset ID for each item. In this example, the asset ID is a product name or code used by the organization. Thus, each product's records are assigned a label, and each record has a property that contains an asset ID. The diagram represents **all of the content** for all product records in an organization, and each item bears the asset ID of the product whose record it is.</span></span> 
    
3. <span data-ttu-id="73095-p113">"Время существования продукта" — это тип события, которое наступает при завершении существования продукта. Когда возникает такого рода события, т. е. когда время существования продукта заканчивается, создается событие, для которого указывается следующее:</span><span class="sxs-lookup"><span data-stu-id="73095-p113">Product Lifetime is the event type; a specific product reaching end of life is an event. When an event of that event type occurs - in this case, when a product reaches its end of life - you create an event that specifies:</span></span>
    
  - <span data-ttu-id="73095-139">Идентификатор ресурса (для документов SharePoint и OneDrive).</span><span class="sxs-lookup"><span data-stu-id="73095-139">An asset ID (for SharePoint and OneDrive documents)</span></span>
    
  - <span data-ttu-id="73095-p114">Ключевые слова (для элементов Exchange). В этом примере организация использует код продукта в сообщениях, содержащих записи продукта, поэтому ключевое слово для элементов Exchange совпадает с идентификатором ресурса для документов SharePoint и OneDrive.</span><span class="sxs-lookup"><span data-stu-id="73095-p114">Keywords (for Exchange items). In this example, the organization uses a product code in messages containing product records, so the keyword for Exchange items is the same as the asset ID for SharePoint and OneDrive documents.</span></span>
    
  - <span data-ttu-id="73095-p115">Дата возникновения события. С этой даты начинается период хранения, она может быть только текущей или будущей, не прошедшей.</span><span class="sxs-lookup"><span data-stu-id="73095-p115">The date when the event occurred. This date is used as the start of the retention period. This date can only be the current or a future date, not a past date.</span></span>
    
4. <span data-ttu-id="73095-p116">После создания события его дата синхронизируется со всем содержимым, у которого есть метка такого типа события и указанный идентификатор ресурса или ключевое слово. Как и для любой другой метки, эта синхронизация может выполняться до 7 дней. На схеме выше все элементы, обведенные красным, имеют свой период хранения, который отсчитывается с даты наступления этого события-триггера. Иными словами, когда время существования продукта подходит к концу, такое событие активирует период хранения для записей, касающихся этого продукта.</span><span class="sxs-lookup"><span data-stu-id="73095-p116">After you create an event, that event date is synced to all of the content that has a label of that event type and that contains the specified asset ID or keyword. Like any label, this syncing can take up to 7 days. In the diagram above, all of the items circled in red have their retention period triggered by this event - in other words, when this product reaches its end of life, that event triggers the retention period for that product's records.</span></span>
    
<span data-ttu-id="73095-p117">Важно понимать, что если не указать идентификатор ресурса или ключевые слова для события, оно активирует период хранения **для всего содержимого** с меткой такого типа события. В случае приведенной выше диаграммы период хранения начнется для всего содержимого. Это может не соответствовать вашим намерениям.</span><span class="sxs-lookup"><span data-stu-id="73095-p117">It's important to understand that if you don't specify an asset ID or keywords for an event, **all of the content** with a label of that event type will have its retention period triggered by the event. This means that in the diagram above, all of the content would start being retained. This may not be what you intend.</span></span> 
  
<span data-ttu-id="73095-p118">Наконец, не забывайте, что у каждой метки свои параметры хранения. В данном примере во всех случаях указан 10-летний период, но событие может стать триггером для меток, имеющих разный период хранения.</span><span class="sxs-lookup"><span data-stu-id="73095-p118">Finally, remember that each label has its own retention settings. In this example, they all specify 10 years, but it's possible for an event to trigger labels where each label has a different retention period.</span></span>
  
## <a name="how-to-set-up-event-driven-retention"></a><span data-ttu-id="73095-153">Настройка хранения, зависящего от возникновения события</span><span class="sxs-lookup"><span data-stu-id="73095-153">How to set up event-driven retention</span></span>

<span data-ttu-id="73095-p119">Ниже в общих чертах описан рабочий процесс для хранения, зависящего от возникновения события. Более подробно шаги изложены далее.</span><span class="sxs-lookup"><span data-stu-id="73095-p119">Here's the high-level workflow for event-driven retention. More detailed steps follow below.</span></span>
  
![Схема, иллюстрирующая рабочий процесс для настройки хранения, зависящего от возникновения события](media/161146d9-e0fc-4248-abc1-a18045eaad5c.png)
  
### <a name="step-1-create-a-label-whose-retention-period-is-based-on-an-event"></a><span data-ttu-id="73095-157">Шаг 1. Создайте метку, период хранения которой зависит от возникновения события</span><span class="sxs-lookup"><span data-stu-id="73095-157">Step 1: Create a label whose retention period is based on an event</span></span>

<span data-ttu-id="73095-158">Откройте Центр безопасности и соответствия требованиям и на панели навигации слева выберите **Классификации** > **Метки** \> **Создать метку**.</span><span class="sxs-lookup"><span data-stu-id="73095-158">In the Security &amp; Compliance Center, in the left navigation, under **Classifications**, choose **Labels** \> **Create a label**.</span></span>
  
<span data-ttu-id="73095-p120">При создании метки включите хранение, а затем выберите параметр, показанный ниже, для хранения или удаления содержимого в связи с событием. Это означает, что параметры хранения не вступят в силу, пока не будет выполнен шаг 5 (создание события на странице **События**).</span><span class="sxs-lookup"><span data-stu-id="73095-p120">When you create the label, turn on retention, and then choose the option shown below to retain or delete the content based on an event. This means that the retention settings won't go into effect until Step 5, when you create an event on the **Events** page.</span></span> 
  
<span data-ttu-id="73095-p121">Обратите внимание, что хранение, зависящее от возникновения события, обычно применяется к содержимому, классифицированному как запись. Поэтому при создании меток на основе события, как правило, выбирают параметр **Использовать метку, чтобы классифицировать содержимое как "Запись"**.</span><span class="sxs-lookup"><span data-stu-id="73095-p121">Note that event-driven retention is typically used for content that's classified as a record. For this reason, when you create labels based on an event, you typically choose the option to **Use label to classify content as a "Record"**.</span></span>
  
<span data-ttu-id="73095-163">Обратите внимание также на то, что для хранения, зависящего от возникновения события, требуются настройки, согласно которым будет выполняться:</span><span class="sxs-lookup"><span data-stu-id="73095-163">Also note that event-driven retention requires retention settings that:</span></span>
  
- <span data-ttu-id="73095-164">хранение содержимого;</span><span class="sxs-lookup"><span data-stu-id="73095-164">Retain the content.</span></span>
    
- <span data-ttu-id="73095-165">автоматическое удаление содержимого или активация проверки перед ликвидацией в конце периода хранения.</span><span class="sxs-lookup"><span data-stu-id="73095-165">Delete the content automatically or trigger a disposition review at the end of the retention period.</span></span>
    
![Возможность создать метку на основе события](media/a4902281-5196-4194-9737-f30231d95861.png)
  
### <a name="step-2-choose-an-event-type-for-that-label"></a><span data-ttu-id="73095-167">Шаг 2. Выберите тип события для такой метки</span><span class="sxs-lookup"><span data-stu-id="73095-167">Step 2: Choose an event type for that label</span></span>

<span data-ttu-id="73095-p122">Когда вы в настройках метки выберите **Событие** в качестве условия для метки, отобразится ссылка **Выберите тип события**. Тип события — это его простое описание, которое можно связать с меткой.</span><span class="sxs-lookup"><span data-stu-id="73095-p122">In the label settings, after you choose the option to base the label on **an event**, you'll see the option to **Choose an event type**. An event type is simply a general description of an event that you want to associate a label with.</span></span>
  
<span data-ttu-id="73095-170">Например, если вы создали тип события "Время существования продукта", то создали и метки на основе событий с именами, которые описывают типы содержимого, к которым нужно применить метки, например: "Файлы разработки продукта" или "Записи о принятии бизнес-решений в отношении продукта".</span><span class="sxs-lookup"><span data-stu-id="73095-170">For example, if you create an event type named Product Lifetime, you'll create event-based labels with names that describe what types of content you want the labels to be applied to, such as "Product development files" or "Product business decision records".</span></span>
  
<span data-ttu-id="73095-171">Обратите внимание на то, что после выбора типа события и создания метки тип события изменить невозможно.</span><span class="sxs-lookup"><span data-stu-id="73095-171">Note that once you choose an event type and create the label, the event type cannot be changed.</span></span>
  
![Возможности создания или выбора типа события](media/8b7afe79-72cb-462e-81d4-b5ddbe899dbc.png)
  
### <a name="step-3-publish-or-auto-apply-the-label"></a><span data-ttu-id="73095-173">Шаг 3. Опубликуйте или автоматически примените метку</span><span class="sxs-lookup"><span data-stu-id="73095-173">Step 3: Publish or auto-apply the label</span></span>

<span data-ttu-id="73095-p123">Как и в случае с любой другой меткой, нужно опубликовать или автоматически применить метку на основе события, чтобы ее можно было вручную или автоматически применить к содержимому. Это делается на странице **Метки**. Обратите внимание, что метки, относящие содержимое к записям, можно только публиковать и вручную применять к содержимому. Их невозможно применить к содержимому автоматически.</span><span class="sxs-lookup"><span data-stu-id="73095-p123">Just like any label, you need to publish or auto-apply an event-based label, so that it's manually or automatically applied to content. Do this on the **Labels** page. Note that labels that classify content as a record can only be published and manually applied to content; they can't be auto-applied to content.</span></span> 
  
![Возможности публиковать или автоматически применять метки](media/c9232c54-bbc0-40d2-abc2-122d5d1e70af.png)
  
### <a name="step-4-enter-an-asset-id"></a><span data-ttu-id="73095-178">Шаг 4. Введите идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="73095-178">Step 4: Enter an asset ID</span></span>

<span data-ttu-id="73095-p124">После применения к содержимому метки на основе события можно ввести идентификатор ресурса для каждого элемента. Например, ваша организация может использовать следующее:</span><span class="sxs-lookup"><span data-stu-id="73095-p124">After an event-driven label is applied to content, you can enter an asset ID for each item. For example, your organization might use:</span></span>
  
- <span data-ttu-id="73095-181">коды продуктов для хранения содержимого, касающегося только определенного продукта;</span><span class="sxs-lookup"><span data-stu-id="73095-181">Product codes that you can use to retain content for only a specific product.</span></span>
    
- <span data-ttu-id="73095-182">коды проектов для хранения содержимого, касающегося только определенного проекта;</span><span class="sxs-lookup"><span data-stu-id="73095-182">Project codes that you can use to retain content for only a specific project.</span></span>
    
- <span data-ttu-id="73095-183">идентификаторы сотрудников для хранения содержимого, касающегося только конкретного лица.</span><span class="sxs-lookup"><span data-stu-id="73095-183">Employee IDs that you can use to retain content for only a specific person.</span></span>
    
<span data-ttu-id="73095-p125">Нужно понимать, что идентификатор ресурса — это всего лишь одно из свойств документа в SharePoint и OneDrive для бизнеса. Возможно, ваша организация уже использует другие свойства документов и идентификаторы для классификации содержимого. В таком случае вы тоже можете использовать эти свойства и значения при создании события (см. описание этапа 6 далее). Важный момент: ваша организация должна использовать сочетание свойства и значения в свойствах документа для связи этого элемента с типом события.</span><span class="sxs-lookup"><span data-stu-id="73095-p125">Understand that Asset ID is simply another document property in SharePoint and OneDrive for Business. Your organization may already use other document properties and IDs to classify content. If so, you can also use those properties and values when you create an event - see Step 6 below. The important point is that your organization must use some property:value combination in the document properties to associate that item with an event type.</span></span>
  
![Текстовое поле для ввода идентификатора ресурса](media/6d31628e-7162-4370-a8d7-de704aafa350.png)
  
### <a name="step-5-create-an-event"></a><span data-ttu-id="73095-189">Шаг 5. Создайте событие</span><span class="sxs-lookup"><span data-stu-id="73095-189">Step 5: Create an event</span></span>

<span data-ttu-id="73095-p126">Когда возникнет определенный экземпляр события такого типа (например, когда завершится время существования продукта), перейдите на страницу "События" в Центре безопасности и соответствия требованиям и создайте событие. Вам нужно вручную активировать событие, создав его.</span><span class="sxs-lookup"><span data-stu-id="73095-p126">When a particular instance of that event type occurs - for example, a product reaches its end of life - go to the Events page in the Security &amp; Compliance Center and create an event. You need to manually trigger an event by creating it.</span></span>
  
![Страница "События" в Центре безопасности и соответствия требованиям](media/811bddfb-a7e9-4990-bf5e-abe0dfb91809.png)
  
### <a name="step-6-choose-the-same-event-type-used-by-the-label-in-step-2"></a><span data-ttu-id="73095-193">Шаг 6. Выберите тип события, который использовался для метки из описания шага 2</span><span class="sxs-lookup"><span data-stu-id="73095-193">Step 6: Choose the same event type used by the label in step 2</span></span>

<span data-ttu-id="73095-p127">При создании события выберите для него тот же тип, который использовался для метки из описания шага 2 (например, "Время существования продукта"). Периода хранения активируется только для содержимого с метками такого типа событий.</span><span class="sxs-lookup"><span data-stu-id="73095-p127">When you create the event, choose the same event type used by the label in step 2 - for example, Product Lifetime. Only content with labels applied to it of that event type will have its retention period triggered.</span></span>
  
![Возможность выбора типа события в параметрах события](media/11663591-5628-419e-9537-61eb8f5c741f.png)
  
### <a name="step-7-enter-keywords-or-an-asset-id"></a><span data-ttu-id="73095-197">Шаг 7. Введите ключевые слова или идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="73095-197">Step 7: Enter keywords or an asset ID</span></span>

<span data-ttu-id="73095-p128">Теперь нужно сузить область поиска содержимого, указав идентификаторы ресурсов для содержимого SharePoint и OneDrive или ключевые слова для содержимого Exchange. Для идентификаторов ресурсов хранение будет применяться только к содержимому с указанной парой "свойство-значение". Если не ввести идентификатор ресурса, **ко всему содержимому** с метками такого типа события будет применена та же дата для хранения.</span><span class="sxs-lookup"><span data-stu-id="73095-p128">Now you narrow the scope of the content by specifying asset IDs for SharePoint and OneDrive content or keywords for Exchange content. For asset IDs, retention will be enforced only on content with the specified property:value pair. If an asset ID is not entered, **all of the content** with labels of that event type get the same retention date applied to them.</span></span> 
  
<span data-ttu-id="73095-p129">Необходимо понимать, что идентификатор ресурса — всего лишь одно из свойств документа SharePoint и OneDrive для бизнеса. При использовании свойства идентификатора ресурса нужно ввести пару ComplianceAssetID:\<значение\> в поле для идентификаторов ресурсов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="73095-p129">Understand that Asset ID is simply another document property in SharePoint and OneDrive for Business. If you're using the Asset ID property, you would enter ComplianceAssetID:\<value\> in the box for asset IDs shown below.</span></span>
  
<span data-ttu-id="73095-p130">Возможно, ваша организация уже применила другие свойства и идентификаторы к документам, связанным с таким типом события. Например, если вам нужно найти записи для конкретного продукта, идентификатор может представлять собой сочетание пользовательского свойства ProductID и значения "XYZ". В этом случае вам нужно ввести ProductID:XYZ в поле для идентификаторов ресурсов, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="73095-p130">Your organization might have applied other properties and IDs to the documents related to this event type. For example, if you need to detect a specific product's records, the ID might be a combination of your custom property ProductID and the value "XYZ". In this case, you'd enter ProductID:XYZ in the box for asset IDs shown below.</span></span>
  
<span data-ttu-id="73095-p131">Для элементов Exchange можно добавить ключевые слова. Вы можете уточнить запрос с помощью таких операторов поиска, как AND, OR и NOT. Дополнительные сведения об этих операторах см. в статье [Запросы по ключевым словам и условия для средства "Поиск контента"](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="73095-p131">For Exchange items, you can include keywords. You can refine your query by using search operators like AND, OR, and NOT. For more information on operators, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
<span data-ttu-id="73095-p132">В заключение выберите дату возникновения события. С этой даты начнется период хранения. После создания события дата события синхронизируется со всем содержимым, имеющим метку такого типа события, идентификатор ресурса и ключевые слова. Как и в случае с любой другой меткой, такая синхронизация может длиться до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="73095-p132">Finally, choose the date when the event occurred; this date is used as the start of the retention period. After you create an event, that event date is synced to all of the content with a label of that event type, asset ID, and keywords. Like any label, this syncing can take up to 7 days.</span></span>
  
![Страница параметров события](media/40d3c9db-f624-49a5-b38a-d16bcce20231.png)
  
## <a name="use-content-search-to-find-all-content-with-a-specific-label-or-asset-id"></a><span data-ttu-id="73095-213">Использование средства "Поиск контента" для поиска всего содержимого с определенной меткой или определенным идентификатором ресурса</span><span class="sxs-lookup"><span data-stu-id="73095-213">Use Content Search to find all content with a specific label or asset ID</span></span>

<span data-ttu-id="73095-214">После присвоения меток содержимому можно воспользоваться средством "Поиск контента" в Центре безопасности и соответствия требованиям, чтобы найти все содержимое, классифицированное с помощью конкретной метки или содержащее определенный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="73095-214">After labels are assigned to content, you can use content search in the Security &amp; Compliance Center to find all content that's classified with a specific label or that contains a specific asset ID.</span></span>
  
<span data-ttu-id="73095-215">Применение запросов на поиск содержимого:</span><span class="sxs-lookup"><span data-stu-id="73095-215">When you create a content search:</span></span>
  
- <span data-ttu-id="73095-216">Чтобы найти все содержимое с определенной меткой, выберите условие **Тег соответствия требованиям**, а затем введите полное имя метки или его часть и используйте подстановочный знак.</span><span class="sxs-lookup"><span data-stu-id="73095-216">To find all content with a specific label, choose the **Compliance Tag** condition, and then enter the complete label name or part of the label name and use a wildcard.</span></span> 
    
- <span data-ttu-id="73095-217">Чтобы найти все содержимое с определенным идентификатором ресурса, введите свойство **ComplianceAssetID** и значение (например, ComplianceAssetID:\<значение\>).</span><span class="sxs-lookup"><span data-stu-id="73095-217">To find all content with a specific asset ID, enter the **ComplianceAssetID** property and a value, like ComplianceAssetID:\<value\>.</span></span> 
    
<span data-ttu-id="73095-218">Дополнительные сведения см. в статье [Запросы по ключевым словам и условия для средства "Поиск контента"](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="73095-218">For more information, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="permissions"></a><span data-ttu-id="73095-219">Разрешения</span><span class="sxs-lookup"><span data-stu-id="73095-219">Permissions</span></span>

<span data-ttu-id="73095-p133">Чтобы получить доступ к странице **События**, проверяющие должны быть членами группы ролей, включающей роли **Управление ликвидацией** и **Журналы аудита только для просмотра**. Рекомендуем создать новую группу ролей под названием "Проверяющие ликвидацию" и добавить в нее сначала эти две роли, а затем членов.</span><span class="sxs-lookup"><span data-stu-id="73095-p133">To get access to the **Events** page, reviewers must be members of a role group with the **Disposition Management** role and the **View-Only Audit Logs** role. We recommend creating a new role group called Disposition Reviewers, adding these two roles to that role group, and then adding members to the role group.</span></span> 
  
<span data-ttu-id="73095-222">Дополнительные сведения см. в статье [Предоставление пользователям доступа к Центру безопасности и соответствия требованиям Office 365](grant-access-to-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="73095-222">For more information, see [Give users access to the Office 365 Security &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md).</span></span>
  
## <a name="automate-events-by-using-powershell"></a><span data-ttu-id="73095-223">Автоматизация событий с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="73095-223">Automate events by using PowerShell</span></span>

<span data-ttu-id="73095-p134">В Центре безопасности и соответствия требованиям Office 365 можно создавать события только вручную. Невозможно автоматически активировать событие, когда оно происходит. Но с помощью скрипта PowerShell можно автоматизировать хранение, зависящее от возникновения события, из бизнес-приложений.</span><span class="sxs-lookup"><span data-stu-id="73095-p134">In the Office 365 Security &amp; Compliance Center, you can only create events manually; it's not possible to automatically trigger an event when it occurs. However, you can use a PowerShell script to automate event-based retention from your business applications.</span></span>
  
<span data-ttu-id="73095-p135">В настоящее время мы работаем над API, чтобы вы могли включить для своих бизнес-приложений (например, финансовых, для управления персоналом и управления взаимоотношениями с клиентами) хранение, зависящее от возникновения события. Например, вы сможете включить для системы управления персоналом такое хранение, чтобы в случае ухода сотрудника из организации событие этого типа активировалось автоматически.</span><span class="sxs-lookup"><span data-stu-id="73095-p135">We are currently working on APIs, so that you can connect your business applications (such as HR, CRM, or financial applications) to event-driven retention. For example, you'll be able to connect your HR system to event-driven retention, so that when an employee leaves the organization, and event of that event type is automatically triggered.</span></span>
  
<span data-ttu-id="73095-228">Пока что для хранения, зависящего от возникновения события, доступны такие командлеты PowerShell:</span><span class="sxs-lookup"><span data-stu-id="73095-228">Until then, here are the PowerShell cmdlets available for event-driven retention:</span></span>
  
- [<span data-ttu-id="73095-229">Get-ComplianceRetentionEventType</span><span class="sxs-lookup"><span data-stu-id="73095-229">Get-ComplianceRetentionEventType</span></span>](https://go.microsoft.com/fwlink/?linkid=873002)
    
- [<span data-ttu-id="73095-230">New-ComplianceRetentionEventType</span><span class="sxs-lookup"><span data-stu-id="73095-230">New-ComplianceRetentionEventType</span></span>](https://go.microsoft.com/fwlink/?linkid=873004)
    
- [<span data-ttu-id="73095-231">Remove-ComplianceRetentionEventType</span><span class="sxs-lookup"><span data-stu-id="73095-231">Remove-ComplianceRetentionEventType</span></span>](https://go.microsoft.com/fwlink/?linkid=873005)
    
- [<span data-ttu-id="73095-232">Set-ComplianceRetentionEventType</span><span class="sxs-lookup"><span data-stu-id="73095-232">Set-ComplianceRetentionEventType</span></span>](https://go.microsoft.com/fwlink/?linkid=873006)
    
- [<span data-ttu-id="73095-233">Get-ComplianceRetentionEvent</span><span class="sxs-lookup"><span data-stu-id="73095-233">Get-ComplianceRetentionEvent</span></span>](https://go.microsoft.com/fwlink/?linkid=873001)
    
- [<span data-ttu-id="73095-234">New-ComplianceRetentionEvent</span><span class="sxs-lookup"><span data-stu-id="73095-234">New-ComplianceRetentionEvent</span></span>](https://go.microsoft.com/fwlink/?linkid=873003)
    

