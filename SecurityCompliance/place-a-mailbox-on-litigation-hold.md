---
title: Перевод почтового ящика в режим хранения для судебного разбирательства
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Поместите почтовый ящик на хранение для судебного разбирательства, чтобы сохранить все его содержимое, в том числе удаленные элементы и исходные версии измененных элементов. '
ms.openlocfilehash: b2d2a60fddb51aa310d01a765c1ebbbf127ecd19
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296982"
---
# <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="77256-103">Перевод почтового ящика в режим хранения для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="77256-103">Place a mailbox on Litigation Hold</span></span>
 
<span data-ttu-id="77256-p101">Переведите почтовый ящик в режим хранения для судебного разбирательства, чтобы сохранить все содержимое ящика, в том числе удаленные элементы и исходные версии измененных элементов. Когда вы задаете для почтового ящика пользователя хранение для судебного разбирательства, содержимое в архивном почтовом ящике пользователя (если он включен) также помещается на хранение. Удаленные и измененные элементы хранятся в течение указанного периода или пока вы не отключите режим хранения для судебного разбирательства. Все такие элементы почтового ящика возвращаются при поиске [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx).</span><span class="sxs-lookup"><span data-stu-id="77256-p101">Place a mailbox on Litigation Hold to preserve all mailbox content, including deleted items and original versions of modified items. When you place a user' mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also placed on hold. Deleted and modified items are preserved for a specified period, or until you remove the mailbox from Litigation Hold. All such mailbox items are returned in an [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) search.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="77256-p102">Удержание для судебного разбирательства сохраняет элементы в папке "элементы с возможностью восстановления" в почтовом ящике пользователя. В зависимости от количества и размера элементов, которые были удалены или изменены, размер папки "элементы с возможностью восстановления" в почтовом ящике может быстро увеличиваться. Для папки "элементы с возможностью восстановления" по умолчанию задана высокая квота. В Exchange Online эта квота автоматически увеличивается при помещении почтового ящика на удержание для судебного разбирательства. В Exchange Server 2013 рекомендуется отслеживать почтовые ящики, которые помещаются на хранение для судебного разбирательства еженедельно, чтобы убедиться, что они не достигают предельных квот элементов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="77256-p102">Litigation Hold preserves items in the Recoverable Items folder in the user's mailbox. Depending on number and size of items deleted or modified, the size of the Recoverable Items folder of the mailbox may increase quickly. The Recoverable Items folder is configured with a high quota by default. In Exchange Online, this quota is automatically increased when you place a mailbox on Litigation Hold. In Exchange Server 2013, we recommend that you monitor mailboxes that are placed on Litigation Hold on a weekly basis to ensure they don't reach the limits of the Recoverable Items quotas.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="77256-113">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="77256-113">What do you need to know before you begin?</span></span>
<span data-ttu-id="77256-114"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="77256-114"></span></span>

- <span data-ttu-id="77256-115">Предполагаемое время для завершения: 5 минут</span><span class="sxs-lookup"><span data-stu-id="77256-115">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="77256-116">Вступление в силу режима хранения для судебного разбирательства может занять до 60 минут.</span><span class="sxs-lookup"><span data-stu-id="77256-116">The Litigation Hold setting may take up to 60 minutes to take effect.</span></span>
    
- <span data-ttu-id="77256-p103">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье запись "Хранение на месте" в статье [Политика обмена сообщениями и разрешения для соответствия требованиям](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx).</span><span class="sxs-lookup"><span data-stu-id="77256-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "In-Place Hold" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="77256-p104">Чтобы поместить почтовый ящик Exchange Online на удержание для судебного разбирательства, ему должна быть назначена лицензия на Exchange Online (план 2). Если почтовому ящику назначена лицензия на Exchange Online (план 1), необходимо назначить ему отдельную лицензию на архивацию на базе Exchange Online, чтобы разместить ее на удержании.</span><span class="sxs-lookup"><span data-stu-id="77256-p104">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online (Plan 2) license. If a mailbox is assigned an Exchange Online (Plan 1) license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    
- <span data-ttu-id="77256-p105">Как описывалось ранее, при помещении хранения для судебного разбирательства в почтовый ящик пользователя, содержимое архивного почтового ящика пользователя также помещается на удержание. Если вы помещаете хранение для судебного разбирательства на локальный основной почтовый ящик в гибридном развертывании Exchange, в облачном архивном почтовом ящике (если этот параметр включен) также помещается на удержание.</span><span class="sxs-lookup"><span data-stu-id="77256-p105">As previously explained, when you place a Litigation Hold on a user's mailbox, content in the user's archive mailbox is also placed on hold. If you place a Litigation Hold on an on-premises primary mailbox in an Exchange hybrid deployment, the cloud-based archive mailbox (if enabled) is also placed on hold.</span></span>
    
- <span data-ttu-id="77256-p106">В Exchange Online квота для папки "элементы с возможностью восстановления" автоматически увеличивается до 100 ГБ при помещении почтового ящика на удержание для судебного разбирательства. Размер этой папки по умолчанию составляет 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="77256-p106">In Exchange Online, the quota for the Recoverable Items folder is automatically increased to 100 GB when you place a mailbox on Litigation Hold. The default size of this folder is 30 GB.</span></span>
    
- <span data-ttu-id="77256-p107">Для судебного разбирательства сохраняются удаленные элементы, а также сохраняются исходные версии измененных элементов до удаления удержания. При необходимости можно указать продолжительность удержания, которая сохранит элемент почтового ящика в течение указанного периода времени. Если указать период хранения, он вычисляется с момента получения сообщения или создания элемента почтового ящика. Чтобы сохранить элементы, удовлетворяющие заданным условиям, используйте удержание на месте, чтобы создать удержание на основе запроса. Дополнительные сведения см. [в статье Создание или удаление удержания на месте](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span><span class="sxs-lookup"><span data-stu-id="77256-p107">Litigation Hold preserves deleted items and also preserves original versions of modified items until the hold is removed. You can optionally specify a hold duration, which preserves a mailbox item for the specified duration period. If you specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created. To preserve items that meet your specified criteria, use an In-Place Hold to create a query-based hold. For details, see [Create or Remove an In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span></span>
    
- <span data-ttu-id="77256-p108">Чтобы использовать командную консоль для помещения почтового ящика Exchange Online на удержание, необходимо использовать Exchange Online PowerShell. Дополнительные сведения см. [в статье подключение к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span><span class="sxs-lookup"><span data-stu-id="77256-p108">To use the Shell to place an Exchange Online mailbox on hold, you have to use Exchange Online PowerShell. For more information, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="77256-p109">Хранение для судебного разбирательства в почтовом ящике общедоступной папки не поддерживается. В общедоступных папках нужно использовать удержание на месте.</span><span class="sxs-lookup"><span data-stu-id="77256-p109">Placing a Litigation Hold on a public folder mailbox isn't supported. You have to use In-Place Hold to place a hold on public folders.</span></span>
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="77256-134">Как поместить почтовый ящик на хранение для судебного разбирательства, используя Центр администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="77256-134">Use the EAC to place a mailbox on Litigation Hold</span></span>
<span data-ttu-id="77256-135"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="77256-135"></span></span>

1. <span data-ttu-id="77256-136">Последовательно выберите пункты **Получатели** \> **Почтовые ящики**.</span><span class="sxs-lookup"><span data-stu-id="77256-136">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="77256-137">В списке почтовых ящиков пользователей выберите почтовый ящик, который необходимо поместить на удержание для судебного разбирательства \*\*\*\* ![, а затем](media/ITPro-EAC-EditIcon.gif)щелкните Изменить значок редактирования.</span><span class="sxs-lookup"><span data-stu-id="77256-137">In the list of user mailboxes, click the mailbox that you want to place on Litigation Hold, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif).</span></span>
    
3. <span data-ttu-id="77256-138">На странице свойств почтового ящика нажмите кнопку **функции почтовоГо ящика.**</span><span class="sxs-lookup"><span data-stu-id="77256-138">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="77256-139">В разделе **Хранение для судебного разбирательства: отключено** нажмите кнопку **Включить**, чтобы применить к почтовому ящику хранение для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="77256-139">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span> 
    
5. <span data-ttu-id="77256-140">На странице **Хранение для судебного разбирательства** введите значения для приведенных ниже дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="77256-140">On the **Litigation Hold** page, enter the following optional information:</span></span> 
    
  - <span data-ttu-id="77256-p110">**Срок хранения для судебного разбирательства (в днях)**. В этом поле можно указать, как долго хранятся элементы почтового ящика при применении к нему хранения для судебного разбирательства. Длительность будет вычислена с даты получения или создания элемента почтового ящика. Если оставить это поле пустым, элементы будут храниться в течение неопределенного времени или до отмены хранения. Длительность указывается в днях.</span><span class="sxs-lookup"><span data-stu-id="77256-p110">**Litigation hold duration (days)** Use this box to specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span> 
    
  - <span data-ttu-id="77256-p111">**Note (Примечание** ) Используйте это поле, чтобы сообщить пользователю о своем почтовом ящике на удержание для судебного разбирательства. Примечание появится в почтовом ящике пользователя, если используется Outlook 2010 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="77256-p111">**Note** Use this box to inform the user their mailbox is on Litigation Hold. The note will appear in the user's mailbox if they're using Outlook 2010 or later.</span></span> 
    
  - <span data-ttu-id="77256-p112">**URL-адрес** Используйте это поле, чтобы направить пользователя на веб-сайт, чтобы получить дополнительные сведения о удержании судебного разбирательства. Этот URL-адрес отображается в почтовом ящике пользователя, если он использует Outlook 2010 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="77256-p112">**URL** Use this box to direct the user to a website for more information about Litigation Hold. This URL appears in the user's mailbox if they are using Outlook 2010 or later.</span></span> 
    
6. <span data-ttu-id="77256-149">Нажмите кнопку **Сохранить** на странице **Хранение для судебного разбирательства**, а затем щелкните **Сохранить** на странице свойств почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="77256-149">Click **Save** on the **Litigation Hold** page, and then click **Save** on the mailbox properties page.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a><span data-ttu-id="77256-150">Использование командной консоли для применения к почтовому ящику хранения для судебного разбирательства в течение неопределенного времени</span><span class="sxs-lookup"><span data-stu-id="77256-150">Use the Shell to place a mailbox on Litigation Hold indefinitely</span></span>
<span data-ttu-id="77256-151"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="77256-151"></span></span>

<span data-ttu-id="77256-p113">В этом примере к почтовому ящику bsuneja@contoso.com применяется хранение для судебного разбирательства. Элементы в почтовом ящике хранятся в течение неопределенного времени или до отмены хранения.</span><span class="sxs-lookup"><span data-stu-id="77256-p113">This example places the mailbox bsuneja@contoso.com on Litigation Hold. Items in the mailbox are held indefinitely or until the hold is removed.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> <span data-ttu-id="77256-154">Если к почтовому ящику применяется хранение для судебного разбирательства в течение неопределенного времени (без указания длительности), для свойства почтового ящика  _LitigationHoldDuration_ задается значение  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="77256-154">When you place a mailbox on Litigation Hold indefinitely (by not specifying a duration period), the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a><span data-ttu-id="77256-155">Использование командной консоли для применения к почтовому ящику хранения для судебного разбирательства и сохранения элементов в течение указанного времени</span><span class="sxs-lookup"><span data-stu-id="77256-155">Use the Shell to place a mailbox on Litigation Hold and preserve items for a specified duration</span></span>
<span data-ttu-id="77256-156"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="77256-156"></span></span>

<span data-ttu-id="77256-157">В этом примере к почтовому ящику bsuneja@contoso.com применяется хранение для судебного разбирательства, а элементы сохраняются в течение 2555 дней (приблизительно 7 лет).</span><span class="sxs-lookup"><span data-stu-id="77256-157">This example places the mailbox bsuneja@contoso.com on Litigation Hold and preserves items for 2555 days (approximately 7 years).</span></span> 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a><span data-ttu-id="77256-158">Использование командной консоли для перевода всех почтовых ящиков в режим хранения для судебного разбирательства в течение указанного времени</span><span class="sxs-lookup"><span data-stu-id="77256-158">Use the Shell to place all mailboxes on Litigation Hold for a specified duration</span></span>
<span data-ttu-id="77256-159"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="77256-159"></span></span>

<span data-ttu-id="77256-p114">В вашей организации может понадобиться сохранить данные всех почтовых ящиков в течение указанного периода времени. Прежде чем перевести все почтовые ящики в организации в режим хранения для судебного разбирательства, попробуйте сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="77256-p114">Your organization may require that all mailbox data be preserved for a specific period of time. Before you place all mailboxes in an organization on Litigation Hold, consider the following:</span></span>
  
<span data-ttu-id="77256-162">В этом примере все почтовые ящики пользователей в организации переводятся в режим хранения для судебного разбирательства на один год (365 дней).</span><span class="sxs-lookup"><span data-stu-id="77256-162">This example places all user mailboxes in the organization on Litigation Hold for one year (365 days).</span></span>
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

<span data-ttu-id="77256-163">В этом примере используется командлет [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx), чтобы получить все почтовые ящики в организации, указать фильтр получателей для включения всех почтовых ящиков пользователей, а затем передать список почтовых ящиков командлету [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx), который в свою очередь активирует хранение для судебного разбирательства и задает длительность хранения.</span><span class="sxs-lookup"><span data-stu-id="77256-163">The example uses the [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet to retrieve all mailboxes in the organization, specifies a recipient filter to include all user mailboxes, and then pipes the list of mailboxes to the [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet to enable the Litigation Hold and hold duration.</span></span> 
  
<span data-ttu-id="77256-164">Чтобы перевести все почтовые ящики пользователей в режим хранения в течение неопределенного времени, выполните предыдущую команду, не включая параметр  _LitigationHoldDuration_.</span><span class="sxs-lookup"><span data-stu-id="77256-164">To place all user mailboxes on an indefinite hold, run the previous command but don't include the  _LitigationHoldDuration_ parameter.</span></span> 
  
<span data-ttu-id="77256-165">Примеры включения или исключения одного либо нескольких почтовых ящиков с помощью других свойств получателей в фильтре приведены в разделе [Дополнительные сведения](#moreinfo.md).</span><span class="sxs-lookup"><span data-stu-id="77256-165">See the [More information](#moreinfo.md) section for examples of using other recipient properties in a filter to include or exclude one or more mailboxes.</span></span> 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a><span data-ttu-id="77256-166">Использование командной консоли для снятия с почтового ящика функции хранения для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="77256-166">Use the Shell to remove a mailbox from Litigation Hold</span></span>
<span data-ttu-id="77256-167"><a name="sectionSection5"> </a></span><span class="sxs-lookup"><span data-stu-id="77256-167"></span></span>

<span data-ttu-id="77256-168">В этом примере с почтового ящика bsuneja@contoso.com снимается функция хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="77256-168">This example removes the mailbox bsuneja@contoso.com from Litigation Hold.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

<span data-ttu-id="77256-169">P</span><span class="sxs-lookup"><span data-stu-id="77256-169">P</span></span>
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="77256-170">Как убедиться, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="77256-170">How do you know this worked?</span></span>
<span data-ttu-id="77256-171"><a name="sectionSection6"> </a></span><span class="sxs-lookup"><span data-stu-id="77256-171"></span></span>

<span data-ttu-id="77256-172">Чтобы убедиться, что почтовый ящик успешно переведен в режим хранения для судебного разбирательства, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="77256-172">To verify that you have successfully placed a mailbox on Litigation Hold, do the one of the following:</span></span>
  
- <span data-ttu-id="77256-173">В Центре администрирования Exchange:</span><span class="sxs-lookup"><span data-stu-id="77256-173">In the EAC:</span></span>
    
1. <span data-ttu-id="77256-174">Последовательно выберите пункты **Получатели** \> **Почтовые ящики**.</span><span class="sxs-lookup"><span data-stu-id="77256-174">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="77256-175">В списке почтовых ящиков пользователей выберите почтовый ящик, для которого нужно проверить параметры хранения для судебного разбирательства \*\*\*\* ![, а затем](media/ITPro-EAC-EditIcon.gif)нажмите кнопку изменить значок редактирования.</span><span class="sxs-lookup"><span data-stu-id="77256-175">In the list of user mailboxes, click the mailbox that you want to verify Litigation Hold settings for, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.gif).</span></span>
    
3. <span data-ttu-id="77256-176">На странице свойств почтового ящика нажмите кнопку **функции почтовоГо ящика.**</span><span class="sxs-lookup"><span data-stu-id="77256-176">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="77256-177">В разделе **Хранение для судебного разбирательства** убедитесь, что включен режим хранения.</span><span class="sxs-lookup"><span data-stu-id="77256-177">Under **Litigation hold**, verify that hold is enabled.</span></span>
    
5. <span data-ttu-id="77256-p115">Щелкните **Просмотр сведений**, чтобы проверить, кто и когда перевел почтовый ящик в режим хранения для судебного разбирательства. Вы также можете проверить или изменить значения дополнительных параметров в полях **Длительность хранения для судебного разбирательства (дней)**, **Примечание** и **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="77256-p115">Click **View details** to verify when the mailbox was placed on Litigation Hold and by whom. You can also verify or change the values in the optional **Litigation hold duration (days)**, **Note**, and **URL** boxes.</span></span> 
    
- <span data-ttu-id="77256-180">В командной консоли выполните одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="77256-180">In the Shell, run one of the following commands:</span></span>
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    <span data-ttu-id="77256-181">или</span><span class="sxs-lookup"><span data-stu-id="77256-181">or</span></span>
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    <span data-ttu-id="77256-182">Если почтовый ящик переведен в режим хранения для судебного разбирательства на неопределенное время, для свойства почтового ящика  _LitigationHoldDuration_ задается значение  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="77256-182">If a mailbox is placed on Litigation Hold indefinitely, the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span>
    
## <a name="more-information"></a><span data-ttu-id="77256-183">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="77256-183">More information</span></span>
<span data-ttu-id="77256-184"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="77256-184"></span></span>

- <span data-ttu-id="77256-185">Если в организации требуется сохранять данные всех почтовых ящиков в течение определенного периода времени, следует учесть следующие моменты, прежде чем перевести все почтовые ящики в организации в режим хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="77256-185">If your organization requires that all mailbox data has to preserved for a specific period of time, consider the following before you place all mailboxes in an organization on Litigation Hold.</span></span>
    
  - <span data-ttu-id="77256-p116">Если вы используете предыдущую команду для перевода всех почтовых ящиков в организации (или подмножества почтовых ящиков, соответствующих требованиям указанного фильтра получателей) в режим хранения для судебного разбирательства, на хранение помещаются только почтовые ящики, доступные на момент выполнения команды. Чтобы применить функцию хранения к позднее созданным почтовым ящикам, команду понадобится выполнить еще раз. Если вы часто создаете почтовые ящики, можно запланировать выполнение команды с необходимой частотой.</span><span class="sxs-lookup"><span data-stu-id="77256-p116">When you use the previous command to place a hold on all mailboxes in an organization (or a subset of mailboxes matching a specified recipient filter) only mailboxes that exist at the time that you run the command are placed on hold. If you create new mailboxes later, you have to run the command again to place the new mailboxes on hold. If you create new mailboxes often, you can run the command as a scheduled task as frequently as required.</span></span>
    
  - <span data-ttu-id="77256-p117">Помещение всех почтовых ящиков на судебное удержание может значительно повлиять на размер почтового ящика В организации Exchange Server 2013 запланируйте необходимое хранилище в соответствии с требованиями вашей организации относительно сохранения.</span><span class="sxs-lookup"><span data-stu-id="77256-p117">Placing all mailboxes on Litigation Hold can significantly impact mailbox sizes. In an Exchange Server 2013 organization, plan for adequate storage to meet your organization's preservation requirements.</span></span>
    
  - <span data-ttu-id="77256-p118">Папка "элементы с возможностью восстановления" имеет свой размер хранилища, поэтому элементы в папке не засчитаны ограничения на размер хранилища для почтового ящика. Как было сказано ранее, сохранение данных почтовых ящиков в течение длительного периода времени приведет к увеличению папки "элементы с возможностью восстановления" в почтовом ящике пользователя и архиве. Чтобы обеспечить это увеличение в Exchange Online, квота для папки "элементы с возможностью восстановления" автоматически увеличивается с 30 ГБ до 100 ГБ при помещении почтового ящика на удержание для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="77256-p118">The Recoverable Items folder has its own storage limit, so items in the folder don't count towards the mailbox storage limit. As previously explained, preserving mailbox data for a long period of time will result in growth of the Recoverable Items folder in a user's mailbox and archive. To accommodate for this increase in Exchange Online, the quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when you place a mailbox on Litigation Hold.</span></span> 
    
    <span data-ttu-id="77256-p119">В Exchange Server 2013 лимит хранения по умолчанию для папки "элементы с возможностью восстановления" также составляет 30 ГБ. Рекомендуется периодически следить за размером этой папки, чтобы убедиться, что она не достигает предела. Дополнительные сведения см. в разделе [Папка элементов для восстановления](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span><span class="sxs-lookup"><span data-stu-id="77256-p119">In Exchange Server 2013, the default storage limit for the Recoverable Items folder is also 30 GB. We recommend that you periodically monitor the size of this folder to ensure it doesn't reach the limit. For more information, see [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span></span>
    
- <span data-ttu-id="77256-p120">В предыдущей команде, которая переводит все почтовые ящики в режим хранения, используется фильтр получателей, возвращающий все почтовые ящики пользователей. Вы можете использовать другие свойства получателей, чтобы вернуть список определенных почтовых ящиков, которые затем можно передать командлету **Set-Mailbox** для перевода этих почтовых ящиков в режим хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="77256-p120">The previous command to place a hold on all mailboxes uses a recipient filter that returns all user mailboxes. You can use other recipient properties to return a list of specific mailboxes that you can then pipe to the **Set-Mailbox** cmdlet to place a Litigation Hold on those mailboxes.</span></span> 
    
    <span data-ttu-id="77256-p121">Вот несколько примеров использования командлетов **Get-Mailbox** и **Get-Recipient** для получения подмножества пользователей на основе общих свойств пользователей или почтовых ящиков. В этих примерах предполагается, что соответствующие свойства почтовых ящиков (например,  _CustomAttributeN_ или  _Department_) заполнены.</span><span class="sxs-lookup"><span data-stu-id="77256-p121">Here are some examples of using the **Get-Mailbox** and **Get-Recipient** cmdlets to return a subset of mailboxes based on common user or mailbox properties. These examples assume that relevant mailbox properties (such as  _CustomAttributeN_ or  _Department_) have been populated.</span></span>
    
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

    <span data-ttu-id="77256-p122">Вы можете использовать в фильтре другие свойства, чтобы включать и исключать почтовые ящики. Подробные сведения см. в статье [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span><span class="sxs-lookup"><span data-stu-id="77256-p122">You can use other user mailbox properties in a filter to include or exclude mailboxes. For details, see [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span></span>
    

