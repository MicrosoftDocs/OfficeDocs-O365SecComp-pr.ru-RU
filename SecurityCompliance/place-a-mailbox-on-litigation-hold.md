---
title: Перевод почтового ящика в режим хранения для судебного разбирательства
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Поместите почтовый ящик на хранение для судебного разбирательства, чтобы сохранить все его содержимое, в том числе удаленные элементы и исходные версии измененных элементов. '
ms.openlocfilehash: a4d0939ffed32a8442b4b705bd15804b9f3eb7ea
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693128"
---
# <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="06eb0-103">Перевод почтового ящика в режим хранения для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="06eb0-103">Place a mailbox on Litigation Hold</span></span>
 
<span data-ttu-id="06eb0-104">Поместите почтовый ящик на хранение для судебного разбирательства, чтобы сохранить все его содержимое, в том числе удаленные элементы и исходные версии измененных элементов.</span><span class="sxs-lookup"><span data-stu-id="06eb0-104">Place a mailbox on Litigation Hold to preserve all mailbox content, including deleted items and original versions of modified items.</span></span> <span data-ttu-id="06eb0-105">Когда вы помещаете почтовый ящик пользователя на хранение для судебного разбирательства, содержимое архивного почтового ящика пользователя (если он включен) также размещается на удержании.</span><span class="sxs-lookup"><span data-stu-id="06eb0-105">When you place a user' mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also placed on hold.</span></span> <span data-ttu-id="06eb0-106">Удаленные и измененные элементы сохраняются в течение определенного периода или до тех пор, пока почтовый ящик не будет удален из удержания для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-106">Deleted and modified items are preserved for a specified period, or until you remove the mailbox from Litigation Hold.</span></span> <span data-ttu-id="06eb0-107">Все такие элементы почтового ящика возвращаются при поиске [Обнаружение электронных данных на месте](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx).</span><span class="sxs-lookup"><span data-stu-id="06eb0-107">All such mailbox items are returned in an [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) search.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="06eb0-108">В режиме хранения для судебного разбирательства элементы сохраняются в папке "Элементы с возможностью восстановления" почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="06eb0-108">Litigation Hold preserves items in the Recoverable Items folder in the user's mailbox.</span></span> <span data-ttu-id="06eb0-109">В зависимости от количества и размера удаленных или измененных элементов размер папки может быстро увеличиться.</span><span class="sxs-lookup"><span data-stu-id="06eb0-109">Depending on number and size of items deleted or modified, the size of the Recoverable Items folder of the mailbox may increase quickly.</span></span> <span data-ttu-id="06eb0-110">Для папки "Элементы с возможностью восстановления" по умолчанию задается высокая квота.</span><span class="sxs-lookup"><span data-stu-id="06eb0-110">The Recoverable Items folder is configured with a high quota by default.</span></span> <span data-ttu-id="06eb0-111">В Exchange Online эта квота автоматически увеличивается при помещении почтового ящика на удержание для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-111">In Exchange Online, this quota is automatically increased when you place a mailbox on Litigation Hold.</span></span> <span data-ttu-id="06eb0-112">В Exchange Server 2013 рекомендуется отслеживать почтовые ящики, которые помещаются на хранение для судебного разбирательства еженедельно, чтобы убедиться, что они не достигают предельных квот элементов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="06eb0-112">In Exchange Server 2013, we recommend that you monitor mailboxes that are placed on Litigation Hold on a weekly basis to ensure they don't reach the limits of the Recoverable Items quotas.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="06eb0-113">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="06eb0-113">What do you need to know before you begin?</span></span>
<span data-ttu-id="06eb0-114"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="06eb0-114"></span></span>

- <span data-ttu-id="06eb0-115">Предполагаемое время для завершения: 5 минут.</span><span class="sxs-lookup"><span data-stu-id="06eb0-115">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="06eb0-116">Вступление в силу режима хранения для судебного разбирательства может занять до 60 минут.</span><span class="sxs-lookup"><span data-stu-id="06eb0-116">The Litigation Hold setting may take up to 60 minutes to take effect.</span></span>
    
- <span data-ttu-id="06eb0-p103">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье запись "Хранение на месте" в статье [Политика обмена сообщениями и разрешения для соответствия требованиям](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx).</span><span class="sxs-lookup"><span data-stu-id="06eb0-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "In-Place Hold" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="06eb0-119">Чтобы поместить почтовый ящик Exchange Online на удержание для судебного разбирательства, ему должна быть назначена лицензия на Exchange Online (план 2).</span><span class="sxs-lookup"><span data-stu-id="06eb0-119">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online (Plan 2) license.</span></span> <span data-ttu-id="06eb0-120">Если почтовому ящику назначена лицензия на Exchange Online (план 1), необходимо назначить ему отдельную лицензию на архивацию на базе Exchange Online, чтобы задать для него хранение.</span><span class="sxs-lookup"><span data-stu-id="06eb0-120">If a mailbox is assigned an Exchange Online (Plan 1) license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    
- <span data-ttu-id="06eb0-121">Как описывалось ранее, при помещении хранения для судебного разбирательства в почтовый ящик пользователя, содержимое архивного почтового ящика пользователя также помещается на удержание.</span><span class="sxs-lookup"><span data-stu-id="06eb0-121">As previously explained, when you place a Litigation Hold on a user's mailbox, content in the user's archive mailbox is also placed on hold.</span></span> <span data-ttu-id="06eb0-122">Если вы помещаете хранение для судебного разбирательства на локальный основной почтовый ящик в гибридном развертывании Exchange, в облачном архивном почтовом ящике (если этот параметр включен) также помещается на удержание.</span><span class="sxs-lookup"><span data-stu-id="06eb0-122">If you place a Litigation Hold on an on-premises primary mailbox in an Exchange hybrid deployment, the cloud-based archive mailbox (if enabled) is also placed on hold.</span></span>
    
- <span data-ttu-id="06eb0-123">В Exchange Online квота для папки "элементы с возможностью восстановления" автоматически увеличивается до 100 ГБ при помещении почтового ящика на удержание для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-123">In Exchange Online, the quota for the Recoverable Items folder is automatically increased to 100 GB when you place a mailbox on Litigation Hold.</span></span> <span data-ttu-id="06eb0-124">Размер этой папки по умолчанию составляет 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="06eb0-124">The default size of this folder is 30 GB.</span></span>
    
- <span data-ttu-id="06eb0-125">В режиме хранения для судебного разбирательства сохраняются удаленные элементы и исходные версии измененных элементов.</span><span class="sxs-lookup"><span data-stu-id="06eb0-125">Litigation Hold preserves deleted items and also preserves original versions of modified items until the hold is removed.</span></span> <span data-ttu-id="06eb0-126">При желании вы можете указать продолжительность хранения элемента почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="06eb0-126">You can optionally specify a hold duration, which preserves a mailbox item for the specified duration period.</span></span> <span data-ttu-id="06eb0-127">Длительность периода хранения рассчитывается с даты получения сообщения или создания элемента почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="06eb0-127">If you specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created.</span></span> <span data-ttu-id="06eb0-128">Чтобы сохранить элементы, удовлетворяющие заданным условиям, используйте удержание на месте, чтобы создать удержание на основе запроса.</span><span class="sxs-lookup"><span data-stu-id="06eb0-128">To preserve items that meet your specified criteria, use an In-Place Hold to create a query-based hold.</span></span> <span data-ttu-id="06eb0-129">Дополнительные сведения см. [в статье Создание или удаление удержания на месте](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span><span class="sxs-lookup"><span data-stu-id="06eb0-129">For details, see [Create or Remove an In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span></span>
    
- <span data-ttu-id="06eb0-130">Чтобы использовать командную консоль для помещения почтового ящика Exchange Online на удержание, необходимо использовать Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06eb0-130">To use the Shell to place an Exchange Online mailbox on hold, you have to use Exchange Online PowerShell.</span></span> <span data-ttu-id="06eb0-131">Подробнее см. в статье [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span><span class="sxs-lookup"><span data-stu-id="06eb0-131">For more information, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="06eb0-132">Размещение судебного удержания в почтовом ящике общедоступных папок не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="06eb0-132">Placing a Litigation Hold on a public folder mailbox isn't supported.</span></span> <span data-ttu-id="06eb0-133">Для размещения удержания в общедоступных папках необходимо использовать удержание на месте.</span><span class="sxs-lookup"><span data-stu-id="06eb0-133">You have to use In-Place Hold to place a hold on public folders.</span></span>
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="06eb0-134">Как поместить почтовый ящик на хранение для судебного разбирательства, используя Центр администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="06eb0-134">Use the EAC to place a mailbox on Litigation Hold</span></span>
<span data-ttu-id="06eb0-135"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="06eb0-135"></span></span>

1. <span data-ttu-id="06eb0-136">Перейдите к разделу **Получатели** \> **Почтовые ящики**.</span><span class="sxs-lookup"><span data-stu-id="06eb0-136">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="06eb0-137">В списке почтовых ящиков пользователей выберите почтовый ящик, который необходимо поместить на удержание для судебного разбирательства \*\*\*\* ![, а затем](media/ITPro-EAC-EditIcon.gif)щелкните Изменить значок редактирования.</span><span class="sxs-lookup"><span data-stu-id="06eb0-137">In the list of user mailboxes, click the mailbox that you want to place on Litigation Hold, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif).</span></span>
    
3. <span data-ttu-id="06eb0-138">На странице свойств почтового ящика нажмите кнопку **функции почтовоГо ящика.**</span><span class="sxs-lookup"><span data-stu-id="06eb0-138">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="06eb0-139">В разделе **Хранение для судебного разбирательства: отключено** нажмите кнопку **Включить**, чтобы применить к почтовому ящику хранение для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-139">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span> 
    
5. <span data-ttu-id="06eb0-140">На странице **Хранение для судебного разбирательства** введите значения для приведенных ниже дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="06eb0-140">On the **Litigation Hold** page, enter the following optional information:</span></span> 
    
  - <span data-ttu-id="06eb0-p110">**Срок хранения для судебного разбирательства (в днях)**. В этом поле можно указать, как долго хранятся элементы почтового ящика при применении к нему хранения для судебного разбирательства. Длительность будет вычислена с даты получения или создания элемента почтового ящика. Если оставить это поле пустым, элементы будут храниться в течение неопределенного времени или до отмены хранения. Длительность указывается в днях.</span><span class="sxs-lookup"><span data-stu-id="06eb0-p110">**Litigation hold duration (days)** Use this box to specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span> 
    
  - <span data-ttu-id="06eb0-145">**Note (Примечание** ) Используйте это поле, чтобы сообщить пользователю о своем почтовом ящике на удержание для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-145">**Note** Use this box to inform the user their mailbox is on Litigation Hold.</span></span> <span data-ttu-id="06eb0-146">Примечание появится в почтовом ящике пользователя, если используется Outlook 2010 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="06eb0-146">The note will appear in the user's mailbox if they're using Outlook 2010 or later.</span></span> 
    
  - <span data-ttu-id="06eb0-147">**URL-адрес** Используйте это поле, чтобы направить пользователя на веб-сайт, чтобы получить дополнительные сведения о удержании судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-147">**URL** Use this box to direct the user to a website for more information about Litigation Hold.</span></span> <span data-ttu-id="06eb0-148">Этот URL-адрес отображается в почтовом ящике пользователя, если он использует Outlook 2010 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="06eb0-148">This URL appears in the user's mailbox if they are using Outlook 2010 or later.</span></span> 
    
6. <span data-ttu-id="06eb0-149">Нажмите кнопку **Сохранить** на странице **Хранение для судебного разбирательства**, а затем щелкните **Сохранить** на странице свойств почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="06eb0-149">Click **Save** on the **Litigation Hold** page, and then click **Save** on the mailbox properties page.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a><span data-ttu-id="06eb0-150">Использование командной консоли Exchange для помещения почтового ящика на судебное удержание в течение неограниченного срока</span><span class="sxs-lookup"><span data-stu-id="06eb0-150">Use the Shell to place a mailbox on Litigation Hold indefinitely</span></span>
<span data-ttu-id="06eb0-151"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="06eb0-151"></span></span>

<span data-ttu-id="06eb0-p113">В этом примере к почтовому ящику bsuneja@contoso.com применяется хранение для судебного разбирательства. Элементы в почтовом ящике хранятся в течение неопределенного времени или до отмены хранения.</span><span class="sxs-lookup"><span data-stu-id="06eb0-p113">This example places the mailbox bsuneja@contoso.com on Litigation Hold. Items in the mailbox are held indefinitely or until the hold is removed.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> <span data-ttu-id="06eb0-154">Если к почтовому ящику применяется хранение для судебного разбирательства в течение неопределенного времени (без указания длительности), для свойства почтового ящика  _LitigationHoldDuration_ задается значение  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="06eb0-154">When you place a mailbox on Litigation Hold indefinitely (by not specifying a duration period), the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a><span data-ttu-id="06eb0-155">Использование командной консоли Exchange для помещения почтового ящика на удержание для судебного разбирательства и сохранения элементов в течение указанного периода времени</span><span class="sxs-lookup"><span data-stu-id="06eb0-155">Use the Shell to place a mailbox on Litigation Hold and preserve items for a specified duration</span></span>
<span data-ttu-id="06eb0-156"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="06eb0-156"></span></span>

<span data-ttu-id="06eb0-157">В этом примере к почтовому ящику bsuneja@contoso.com применяется хранение для судебного разбирательства, а элементы сохраняются в течение 2555 дней (приблизительно 7 лет).</span><span class="sxs-lookup"><span data-stu-id="06eb0-157">This example places the mailbox bsuneja@contoso.com on Litigation Hold and preserves items for 2555 days (approximately 7 years).</span></span> 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a><span data-ttu-id="06eb0-158">Использование командной консоли для помещения всех почтовых ящиков на удержание для судебного разбирательства в течение указанного периода времени</span><span class="sxs-lookup"><span data-stu-id="06eb0-158">Use the Shell to place all mailboxes on Litigation Hold for a specified duration</span></span>
<span data-ttu-id="06eb0-159"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="06eb0-159"></span></span>

<span data-ttu-id="06eb0-160">В Организации может потребоваться сохранить все данные почтового ящика в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="06eb0-160">Your organization may require that all mailbox data be preserved for a specific period of time.</span></span> <span data-ttu-id="06eb0-161">Прежде чем поместить все почтовые ящики в Организации на удержание для судебного разбирательства, примите во внимание следующее:</span><span class="sxs-lookup"><span data-stu-id="06eb0-161">Before you place all mailboxes in an organization on Litigation Hold, consider the following:</span></span>
  
<span data-ttu-id="06eb0-162">В этом примере все почтовые ящики пользователей в Организации на удержание для судебного разбирательства помещаются в течение одного года (365 дней).</span><span class="sxs-lookup"><span data-stu-id="06eb0-162">This example places all user mailboxes in the organization on Litigation Hold for one year (365 days).</span></span>
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

<span data-ttu-id="06eb0-163">В этом примере командлет [Get – Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) используется для получения всех почтовых ящиков в Организации, указывает фильтр получателей для включения всех почтовых ящиков пользователей, а затем передает список почтовых ящиков в командлет [Set – Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) , чтобы включить удержание для судебного разбирательства и срок хранения.</span><span class="sxs-lookup"><span data-stu-id="06eb0-163">The example uses the [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet to retrieve all mailboxes in the organization, specifies a recipient filter to include all user mailboxes, and then pipes the list of mailboxes to the [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet to enable the Litigation Hold and hold duration.</span></span> 
  
<span data-ttu-id="06eb0-164">Чтобы перевести все почтовые ящики пользователей в режим хранения в течение неопределенного времени, выполните предыдущую команду, не включая параметр  _LitigationHoldDuration_.</span><span class="sxs-lookup"><span data-stu-id="06eb0-164">To place all user mailboxes on an indefinite hold, run the previous command but don't include the  _LitigationHoldDuration_ parameter.</span></span> 
  
<span data-ttu-id="06eb0-165">Примеры включения или исключения одного либо нескольких почтовых ящиков с помощью других свойств получателей в фильтре приведены в разделе [Дополнительные сведения](#moreinfo.md).</span><span class="sxs-lookup"><span data-stu-id="06eb0-165">See the [More information](#moreinfo.md) section for examples of using other recipient properties in a filter to include or exclude one or more mailboxes.</span></span> 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a><span data-ttu-id="06eb0-166">Использование командной консоли для удаления почтового ящика из удержания для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="06eb0-166">Use the Shell to remove a mailbox from Litigation Hold</span></span>
<span data-ttu-id="06eb0-167"><a name="sectionSection5"> </a></span><span class="sxs-lookup"><span data-stu-id="06eb0-167"></span></span>

<span data-ttu-id="06eb0-168">В этом примере с почтового ящика bsuneja@contoso.com снимается функция хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-168">This example removes the mailbox bsuneja@contoso.com from Litigation Hold.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

<span data-ttu-id="06eb0-169">P</span><span class="sxs-lookup"><span data-stu-id="06eb0-169">P</span></span>
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="06eb0-170">Как проверить, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="06eb0-170">How do you know this worked?</span></span>
<span data-ttu-id="06eb0-171"><a name="sectionSection6"> </a></span><span class="sxs-lookup"><span data-stu-id="06eb0-171"></span></span>

<span data-ttu-id="06eb0-172">Чтобы убедиться, что почтовый ящик успешно переведен в режим хранения для судебного разбирательства, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="06eb0-172">To verify that you have successfully placed a mailbox on Litigation Hold, do the one of the following:</span></span>
  
- <span data-ttu-id="06eb0-173">В Центре администрирования Exchange:</span><span class="sxs-lookup"><span data-stu-id="06eb0-173">In the EAC:</span></span>
    
1. <span data-ttu-id="06eb0-174">Последовательно выберите пункты **Получатели** \> **Почтовые ящики**.</span><span class="sxs-lookup"><span data-stu-id="06eb0-174">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="06eb0-175">В списке почтовых ящиков пользователей выберите почтовый ящик, для которого нужно проверить параметры хранения для судебного разбирательства \*\*\*\* ![, а затем](media/ITPro-EAC-EditIcon.gif)нажмите кнопку изменить значок редактирования.</span><span class="sxs-lookup"><span data-stu-id="06eb0-175">In the list of user mailboxes, click the mailbox that you want to verify Litigation Hold settings for, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif).</span></span>
    
3. <span data-ttu-id="06eb0-176">На странице свойств почтового ящика нажмите кнопку **функции почтовоГо ящика.**</span><span class="sxs-lookup"><span data-stu-id="06eb0-176">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="06eb0-177">В разделе **Хранение для судебного разбирательства** убедитесь, что включен режим хранения.</span><span class="sxs-lookup"><span data-stu-id="06eb0-177">Under **Litigation hold**, verify that hold is enabled.</span></span>
    
5. <span data-ttu-id="06eb0-p115">Щелкните **Просмотр сведений**, чтобы проверить, кто и когда перевел почтовый ящик в режим хранения для судебного разбирательства. Вы также можете проверить или изменить значения дополнительных параметров в полях **Длительность хранения для судебного разбирательства (дней)**, **Примечание** и **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="06eb0-p115">Click **View details** to verify when the mailbox was placed on Litigation Hold and by whom. You can also verify or change the values in the optional **Litigation hold duration (days)**, **Note**, and **URL** boxes.</span></span> 
    
- <span data-ttu-id="06eb0-180">В командной консоли выполните одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="06eb0-180">In the Shell, run one of the following commands:</span></span>
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    <span data-ttu-id="06eb0-181">или</span><span class="sxs-lookup"><span data-stu-id="06eb0-181">or</span></span>
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    <span data-ttu-id="06eb0-182">Если почтовый ящик переведен в режим хранения для судебного разбирательства на неопределенное время, для свойства почтового ящика  _LitigationHoldDuration_ задается значение  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="06eb0-182">If a mailbox is placed on Litigation Hold indefinitely, the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span>
    
## <a name="more-information"></a><span data-ttu-id="06eb0-183">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="06eb0-183">More information</span></span>
<span data-ttu-id="06eb0-184"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="06eb0-184"></span></span>

- <span data-ttu-id="06eb0-185">Если в организации требуется сохранять данные всех почтовых ящиков в течение определенного периода времени, следует учесть следующие моменты, прежде чем перевести все почтовые ящики в организации в режим хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-185">If your organization requires that all mailbox data has to preserved for a specific period of time, consider the following before you place all mailboxes in an organization on Litigation Hold.</span></span>
    
  - <span data-ttu-id="06eb0-p116">Если вы используете предыдущую команду для перевода всех почтовых ящиков в организации (или подмножества почтовых ящиков, соответствующих требованиям указанного фильтра получателей) в режим хранения для судебного разбирательства, на хранение помещаются только почтовые ящики, доступные на момент выполнения команды. Чтобы применить функцию хранения к позднее созданным почтовым ящикам, команду понадобится выполнить еще раз. Если вы часто создаете почтовые ящики, можно запланировать выполнение команды с необходимой частотой.</span><span class="sxs-lookup"><span data-stu-id="06eb0-p116">When you use the previous command to place a hold on all mailboxes in an organization (or a subset of mailboxes matching a specified recipient filter) only mailboxes that exist at the time that you run the command are placed on hold. If you create new mailboxes later, you have to run the command again to place the new mailboxes on hold. If you create new mailboxes often, you can run the command as a scheduled task as frequently as required.</span></span>
    
  - <span data-ttu-id="06eb0-189">Перевод всех почтовых ящиков в режим хранения для судебного разбирательства может существенно повлиять на размер почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="06eb0-189">Placing all mailboxes on Litigation Hold can significantly impact mailbox sizes.</span></span> <span data-ttu-id="06eb0-190">В организации Exchange Server 2013 запланируйте необходимое хранилище в соответствии с требованиями вашей организации относительно сохранения.</span><span class="sxs-lookup"><span data-stu-id="06eb0-190">In an Exchange Server 2013 organization, plan for adequate storage to meet your organization's preservation requirements.</span></span>
    
  - <span data-ttu-id="06eb0-191">Для этой папки размер хранилища предусмотрен отдельно, и потому увеличение количества элементов в ней не может привести к превышению ограничения для хранилища почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="06eb0-191">The Recoverable Items folder has its own storage limit, so items in the folder don't count towards the mailbox storage limit.</span></span> <span data-ttu-id="06eb0-192">Как было сказано ранее, сохранение данных почтовых ящиков в течение длительного периода времени приведет к увеличению папки "элементы с возможностью восстановления" в почтовом ящике пользователя и архиве.</span><span class="sxs-lookup"><span data-stu-id="06eb0-192">As previously explained, preserving mailbox data for a long period of time will result in growth of the Recoverable Items folder in a user's mailbox and archive.</span></span> <span data-ttu-id="06eb0-193">Чтобы обеспечить это увеличение в Exchange Online, квота для папки "элементы с возможностью восстановления" автоматически увеличивается с 30 ГБ до 100 ГБ при помещении почтового ящика на удержание для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-193">To accommodate for this increase in Exchange Online, the quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when you place a mailbox on Litigation Hold.</span></span> 
    
    <span data-ttu-id="06eb0-194">В Exchange Server 2013 лимит хранения по умолчанию для папки "элементы с возможностью восстановления" также составляет 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="06eb0-194">In Exchange Server 2013, the default storage limit for the Recoverable Items folder is also 30 GB.</span></span> <span data-ttu-id="06eb0-195">Рекомендуется периодически следить за размером этой папки, чтобы убедиться, что она не достигает предела.</span><span class="sxs-lookup"><span data-stu-id="06eb0-195">We recommend that you periodically monitor the size of this folder to ensure it doesn't reach the limit.</span></span> <span data-ttu-id="06eb0-196">Дополнительные сведения см. в разделе [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span><span class="sxs-lookup"><span data-stu-id="06eb0-196">For more information, see [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span></span>
    
- <span data-ttu-id="06eb0-p120">В предыдущей команде, которая переводит все почтовые ящики в режим хранения, используется фильтр получателей, возвращающий все почтовые ящики пользователей. Вы можете использовать другие свойства получателей, чтобы вернуть список определенных почтовых ящиков, которые затем можно передать командлету **Set-Mailbox** для перевода этих почтовых ящиков в режим хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="06eb0-p120">The previous command to place a hold on all mailboxes uses a recipient filter that returns all user mailboxes. You can use other recipient properties to return a list of specific mailboxes that you can then pipe to the **Set-Mailbox** cmdlet to place a Litigation Hold on those mailboxes.</span></span> 
    
    <span data-ttu-id="06eb0-p121">Вот несколько примеров использования командлетов **Get-Mailbox** и **Get-Recipient** для возврата подмножества почтовых ящиков на основе общих свойств пользователей или почтовых ящиков. В этих примерах предполагается, что уже заполнены соответствующие свойства почтовых ящиков (такие как  _CustomAttributeN_ или  _Department_).</span><span class="sxs-lookup"><span data-stu-id="06eb0-p121">Here are some examples of using the **Get-Mailbox** and **Get-Recipient** cmdlets to return a subset of mailboxes based on common user or mailbox properties. These examples assume that relevant mailbox properties (such as  _CustomAttributeN_ or  _Department_) have been populated.</span></span>
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    <span data-ttu-id="06eb0-p122">Вы можете использовать в фильтре другие свойства, чтобы включать и исключать почтовые ящики. Подробные сведения см. в статье [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span><span class="sxs-lookup"><span data-stu-id="06eb0-p122">You can use other user mailbox properties in a filter to include or exclude mailboxes. For details, see [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span></span>
    

