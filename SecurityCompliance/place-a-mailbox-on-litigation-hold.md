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
localization_priority: Normal
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Поместите почтовый ящик на хранение для судебного разбирательства, чтобы сохранить все его содержимое, в том числе удаленные элементы и исходные версии измененных элементов. '
ms.openlocfilehash: 8f440f5fc0bc7dafd639bdf8136808aa2f3bd35f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026446"
---
# <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="d5551-103">Перевод почтового ящика в режим хранения для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="d5551-103">Place a mailbox on Litigation Hold</span></span>
 
<span data-ttu-id="d5551-p101">Переведите почтовый ящик в режим хранения для судебного разбирательства, чтобы сохранить все содержимое ящика, в том числе удаленные элементы и исходные версии измененных элементов. Когда вы задаете для почтового ящика пользователя хранение для судебного разбирательства, содержимое в архивном почтовом ящике пользователя (если он включен) также помещается на хранение. Удаленные и измененные элементы хранятся в течение указанного периода или пока вы не отключите режим хранения для судебного разбирательства. Все такие элементы почтового ящика возвращаются при поиске [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5551-p101">Place a mailbox on Litigation Hold to preserve all mailbox content, including deleted items and original versions of modified items. When you place a user' mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also placed on hold. Deleted and modified items are preserved for a specified period, or until you remove the mailbox from Litigation Hold. All such mailbox items are returned in an [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) search.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d5551-p102">Хранение для судебного разбирательства сохраняет элементов в папке восстанавливаемых элементов в почтовом ящике пользователя. В зависимости от числа и размера элементов удаления или изменения, может быстро увеличить размер папки элементов для восстановления почтового ящика. Папка элементов для восстановления настроена с высокой квот по умолчанию. В Exchange Online эта квота автоматически увеличивается при постановка почтового ящика на хранение для судебного разбирательства. В Exchange Server 2013, мы рекомендуем наблюдения за почтовые ящики, помещенные на хранение для судебного разбирательства неделю убедитесь, что они не достигнут ограничения квот элементов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="d5551-p102">Litigation Hold preserves items in the Recoverable Items folder in the user's mailbox. Depending on number and size of items deleted or modified, the size of the Recoverable Items folder of the mailbox may increase quickly. The Recoverable Items folder is configured with a high quota by default. In Exchange Online, this quota is automatically increased when you place a mailbox on Litigation Hold. In Exchange Server 2013, we recommend that you monitor mailboxes that are placed on Litigation Hold on a weekly basis to ensure they don't reach the limits of the Recoverable Items quotas.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="d5551-113">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="d5551-113">What do you need to know before you begin?</span></span>
<span data-ttu-id="d5551-114"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="d5551-114"></span></span>

- <span data-ttu-id="d5551-115">Предполагаемое время для завершения: 5 минут</span><span class="sxs-lookup"><span data-stu-id="d5551-115">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="d5551-116">Вступление в силу режима хранения для судебного разбирательства может занять до 60 минут.</span><span class="sxs-lookup"><span data-stu-id="d5551-116">The Litigation Hold setting may take up to 60 minutes to take effect.</span></span>
    
- <span data-ttu-id="d5551-p103">Для выполнения этих процедур необходимы соответствующие разрешения. Сведения о необходимых разрешениях см. в статье запись "Хранение на месте" в статье [Политика обмена сообщениями и разрешения для соответствия требованиям](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5551-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "In-Place Hold" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="d5551-p104">Чтобы поставить почтовый ящик Exchange Online на хранение для судебного разбирательства, она должна быть назначена лицензия Exchange Online (план 2). Если почтовый ящик назначается лицензии Exchange Online (план 1), необходимо назначить его отдельная лицензия архивации Exchange Online чтобы поставить на удержание.</span><span class="sxs-lookup"><span data-stu-id="d5551-p104">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online (Plan 2) license. If a mailbox is assigned an Exchange Online (Plan 1) license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    
- <span data-ttu-id="d5551-p105">Как объяснялось ранее при выполнении хранение для судебного разбирательства на почтовый ящик пользователя, контента в архивный почтовый ящик пользователя также ставится на удержание. Если указать хранение для судебного разбирательства для локального основного почтового ящика в гибридном развертывании Exchange облачной архивного почтового ящика (Если эта возможность включена) также ставится на удержание.</span><span class="sxs-lookup"><span data-stu-id="d5551-p105">As previously explained, when you place a Litigation Hold on a user's mailbox, content in the user's archive mailbox is also placed on hold. If you place a Litigation Hold on an on-premises primary mailbox in an Exchange hybrid deployment, the cloud-based archive mailbox (if enabled) is also placed on hold.</span></span>
    
- <span data-ttu-id="d5551-p106">В Exchange Online квота для папки элементов для восстановления автоматически увеличивается до 100 ГБ при постановка почтового ящика на хранение для судебного разбирательства. Размер этой папки по умолчанию — 30 ГБ.</span><span class="sxs-lookup"><span data-stu-id="d5551-p106">In Exchange Online, the quota for the Recoverable Items folder is automatically increased to 100 GB when you place a mailbox on Litigation Hold. The default size of this folder is 30 GB.</span></span>
    
- <span data-ttu-id="d5551-p107">Хранение для судебного разбирательства сохраняет "Удаленные", а также сохраняет оригинальных версий измененных элементов, пока не будет снято удержание. При необходимости можно указать продолжительность удержания, который сохраняет элемента почтового ящика для указанного длительности периода. При указании периода продолжительность удержания, рассчитывается от даты выдается сообщение или создания элемента почтового ящика. Для сохранения элементов, соответствующих заданным условиям, используйте хранение на месте для создания запроса на удержание. Дополнительные сведения см [Создание или удаление хранение на месте](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5551-p107">Litigation Hold preserves deleted items and also preserves original versions of modified items until the hold is removed. You can optionally specify a hold duration, which preserves a mailbox item for the specified duration period. If you specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created. To preserve items that meet your specified criteria, use an In-Place Hold to create a query-based hold. For details, see [Create or Remove an In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span></span>
    
- <span data-ttu-id="d5551-p108">Использование командной консоли Exchange для удержание почтовый ящик Exchange Online, необходимо использовать Exchange Online PowerShell. Дополнительные сведения можно [Подключить к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5551-p108">To use the Shell to place an Exchange Online mailbox on hold, you have to use Exchange Online PowerShell. For more information, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="d5551-p109">Хранение для судебного разбирательства в почтовом ящике общедоступной папки не поддерживается. В общедоступных папках нужно использовать удержание на месте.</span><span class="sxs-lookup"><span data-stu-id="d5551-p109">Placing a Litigation Hold on a public folder mailbox isn't supported. You have to use In-Place Hold to place a hold on public folders.</span></span>
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="d5551-134">Как поместить почтовый ящик на хранение для судебного разбирательства, используя Центр администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="d5551-134">Use the EAC to place a mailbox on Litigation Hold</span></span>
<span data-ttu-id="d5551-135"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="d5551-135"></span></span>

1. <span data-ttu-id="d5551-136">Последовательно выберите пункты **Получатели** \> **Почтовые ящики**.</span><span class="sxs-lookup"><span data-stu-id="d5551-136">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="d5551-137">В списке почтовых ящиков пользователей выберите почтовый ящик, к которому нужно применить хранение для судебного разбирательства, а затем нажмите кнопку **Изменить**![Значок редактирования](media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="d5551-137">In the list of user mailboxes, click the mailbox that you want to place on Litigation Hold, and then click **Edit**![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>
    
3. <span data-ttu-id="d5551-138">На странице свойств почтового ящика выберите **функции почтового ящика.**</span><span class="sxs-lookup"><span data-stu-id="d5551-138">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="d5551-139">В разделе **Хранение для судебного разбирательства: отключено** нажмите кнопку **Включить**, чтобы применить к почтовому ящику хранение для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="d5551-139">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span> 
    
5. <span data-ttu-id="d5551-140">На странице **Хранение для судебного разбирательства** введите значения для приведенных ниже дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="d5551-140">On the **Litigation Hold** page, enter the following optional information:</span></span> 
    
  - <span data-ttu-id="d5551-p110">**Срок хранения для судебного разбирательства (в днях)**. В этом поле можно указать, как долго хранятся элементы почтового ящика при применении к нему хранения для судебного разбирательства. Длительность будет вычислена с даты получения или создания элемента почтового ящика. Если оставить это поле пустым, элементы будут храниться в течение неопределенного времени или до отмены хранения. Длительность указывается в днях.</span><span class="sxs-lookup"><span data-stu-id="d5551-p110">**Litigation hold duration (days)** Use this box to specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span> 
    
  - <span data-ttu-id="d5551-p111">**Примечание** Это поле используется для оповещения пользователя, почтовый ящик находится на хранение для судебного разбирательства. Если при использовании Outlook 2010 или более поздняя версия Примечание будет отображаться в почтовом ящике пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5551-p111">**Note** Use this box to inform the user their mailbox is on Litigation Hold. The note will appear in the user's mailbox if they're using Outlook 2010 or later.</span></span> 
    
  - <span data-ttu-id="d5551-p112">**URL-адрес** Это поле используется для направления пользователя веб-сайта, Дополнительные сведения о хранение для судебного разбирательства. Этот URL-адрес отображается в почтовом ящике пользователя, если они используют Outlook 2010 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="d5551-p112">**URL** Use this box to direct the user to a website for more information about Litigation Hold. This URL appears in the user's mailbox if they are using Outlook 2010 or later.</span></span> 
    
6. <span data-ttu-id="d5551-149">Нажмите кнопку **Сохранить** на странице **Хранение для судебного разбирательства**, а затем щелкните **Сохранить** на странице свойств почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="d5551-149">Click **Save** on the **Litigation Hold** page, and then click **Save** on the mailbox properties page.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a><span data-ttu-id="d5551-150">Использование командной консоли для применения к почтовому ящику хранения для судебного разбирательства в течение неопределенного времени</span><span class="sxs-lookup"><span data-stu-id="d5551-150">Use the Shell to place a mailbox on Litigation Hold indefinitely</span></span>
<span data-ttu-id="d5551-151"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="d5551-151"></span></span>

<span data-ttu-id="d5551-p113">В этом примере к почтовому ящику bsuneja@contoso.com применяется хранение для судебного разбирательства. Элементы в почтовом ящике хранятся в течение неопределенного времени или до отмены хранения.</span><span class="sxs-lookup"><span data-stu-id="d5551-p113">This example places the mailbox bsuneja@contoso.com on Litigation Hold. Items in the mailbox are held indefinitely or until the hold is removed.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> <span data-ttu-id="d5551-154">Если к почтовому ящику применяется хранение для судебного разбирательства в течение неопределенного времени (без указания длительности), для свойства почтового ящика  _LitigationHoldDuration_ задается значение  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="d5551-154">When you place a mailbox on Litigation Hold indefinitely (by not specifying a duration period), the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a><span data-ttu-id="d5551-155">Использование командной консоли для применения к почтовому ящику хранения для судебного разбирательства и сохранения элементов в течение указанного времени</span><span class="sxs-lookup"><span data-stu-id="d5551-155">Use the Shell to place a mailbox on Litigation Hold and preserve items for a specified duration</span></span>
<span data-ttu-id="d5551-156"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="d5551-156"></span></span>

<span data-ttu-id="d5551-157">В этом примере к почтовому ящику bsuneja@contoso.com применяется хранение для судебного разбирательства, а элементы сохраняются в течение 2555 дней (приблизительно 7 лет).</span><span class="sxs-lookup"><span data-stu-id="d5551-157">This example places the mailbox bsuneja@contoso.com on Litigation Hold and preserves items for 2555 days (approximately 7 years).</span></span> 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a><span data-ttu-id="d5551-158">Использование командной консоли для перевода всех почтовых ящиков в режим хранения для судебного разбирательства в течение указанного времени</span><span class="sxs-lookup"><span data-stu-id="d5551-158">Use the Shell to place all mailboxes on Litigation Hold for a specified duration</span></span>
<span data-ttu-id="d5551-159"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="d5551-159"></span></span>

<span data-ttu-id="d5551-p114">В вашей организации может понадобиться сохранить данные всех почтовых ящиков в течение указанного периода времени. Прежде чем перевести все почтовые ящики в организации в режим хранения для судебного разбирательства, попробуйте сделать следующее.</span><span class="sxs-lookup"><span data-stu-id="d5551-p114">Your organization may require that all mailbox data be preserved for a specific period of time. Before you place all mailboxes in an organization on Litigation Hold, consider the following:</span></span>
  
<span data-ttu-id="d5551-162">В этом примере все почтовые ящики пользователей в организации переводятся в режим хранения для судебного разбирательства на один год (365 дней).</span><span class="sxs-lookup"><span data-stu-id="d5551-162">This example places all user mailboxes in the organization on Litigation Hold for one year (365 days).</span></span>
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

<span data-ttu-id="d5551-163">В этом примере используется командлет [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx), чтобы получить все почтовые ящики в организации, указать фильтр получателей для включения всех почтовых ящиков пользователей, а затем передать список почтовых ящиков командлету [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx), который в свою очередь активирует хранение для судебного разбирательства и задает длительность хранения.</span><span class="sxs-lookup"><span data-stu-id="d5551-163">The example uses the [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet to retrieve all mailboxes in the organization, specifies a recipient filter to include all user mailboxes, and then pipes the list of mailboxes to the [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet to enable the Litigation Hold and hold duration.</span></span> 
  
<span data-ttu-id="d5551-164">Чтобы перевести все почтовые ящики пользователей в режим хранения в течение неопределенного времени, выполните предыдущую команду, не включая параметр  _LitigationHoldDuration_.</span><span class="sxs-lookup"><span data-stu-id="d5551-164">To place all user mailboxes on an indefinite hold, run the previous command but don't include the  _LitigationHoldDuration_ parameter.</span></span> 
  
<span data-ttu-id="d5551-165">Примеры включения или исключения одного либо нескольких почтовых ящиков с помощью других свойств получателей в фильтре приведены в разделе [Дополнительные сведения](#moreinfo.md).</span><span class="sxs-lookup"><span data-stu-id="d5551-165">See the [More information](#moreinfo.md) section for examples of using other recipient properties in a filter to include or exclude one or more mailboxes.</span></span> 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a><span data-ttu-id="d5551-166">Использование командной консоли для снятия с почтового ящика функции хранения для судебного разбирательства</span><span class="sxs-lookup"><span data-stu-id="d5551-166">Use the Shell to remove a mailbox from Litigation Hold</span></span>
<span data-ttu-id="d5551-167"><a name="sectionSection5"> </a></span><span class="sxs-lookup"><span data-stu-id="d5551-167"></span></span>

<span data-ttu-id="d5551-168">В этом примере с почтового ящика bsuneja@contoso.com снимается функция хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="d5551-168">This example removes the mailbox bsuneja@contoso.com from Litigation Hold.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

<span data-ttu-id="d5551-169">P</span><span class="sxs-lookup"><span data-stu-id="d5551-169">P</span></span>
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="d5551-170">Как проверить, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="d5551-170">How do you know this worked?</span></span>
<span data-ttu-id="d5551-171"><a name="sectionSection6"> </a></span><span class="sxs-lookup"><span data-stu-id="d5551-171"></span></span>

<span data-ttu-id="d5551-172">Чтобы убедиться, что почтовый ящик успешно переведен в режим хранения для судебного разбирательства, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="d5551-172">To verify that you have successfully placed a mailbox on Litigation Hold, do the one of the following:</span></span>
  
- <span data-ttu-id="d5551-173">В Центре администрирования Exchange:</span><span class="sxs-lookup"><span data-stu-id="d5551-173">In the EAC:</span></span>
    
1. <span data-ttu-id="d5551-174">Последовательно выберите пункты **Получатели** \> **Почтовые ящики**.</span><span class="sxs-lookup"><span data-stu-id="d5551-174">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="d5551-175">В списке почтовых ящиков пользователей щелкните ящик, для которого нужно проверить параметры хранения для судебного разбирательства, а затем выберите команду **Изменить**![Значок редактирования](media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="d5551-175">In the list of user mailboxes, click the mailbox that you want to verify Litigation Hold settings for, and then click **Edit**![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>
    
3. <span data-ttu-id="d5551-176">На странице свойств почтового ящика выберите **функции почтового ящика.**</span><span class="sxs-lookup"><span data-stu-id="d5551-176">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="d5551-177">В разделе **Хранение для судебного разбирательства** убедитесь, что включен режим хранения.</span><span class="sxs-lookup"><span data-stu-id="d5551-177">Under **Litigation hold**, verify that hold is enabled.</span></span>
    
5. <span data-ttu-id="d5551-p115">Щелкните **Просмотр сведений**, чтобы проверить, кто и когда перевел почтовый ящик в режим хранения для судебного разбирательства. Вы также можете проверить или изменить значения дополнительных параметров в полях **Длительность хранения для судебного разбирательства (дней)**, **Примечание** и **URL-адрес**.</span><span class="sxs-lookup"><span data-stu-id="d5551-p115">Click **View details** to verify when the mailbox was placed on Litigation Hold and by whom. You can also verify or change the values in the optional **Litigation hold duration (days)**, **Note**, and **URL** boxes.</span></span> 
    
- <span data-ttu-id="d5551-180">В командной консоли выполните одну из следующих команд:</span><span class="sxs-lookup"><span data-stu-id="d5551-180">In the Shell, run one of the following commands:</span></span>
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    <span data-ttu-id="d5551-181">или</span><span class="sxs-lookup"><span data-stu-id="d5551-181">or</span></span>
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    <span data-ttu-id="d5551-182">Если почтовый ящик переведен в режим хранения для судебного разбирательства на неопределенное время, для свойства почтового ящика  _LitigationHoldDuration_ задается значение  `Unlimited`.</span><span class="sxs-lookup"><span data-stu-id="d5551-182">If a mailbox is placed on Litigation Hold indefinitely, the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span>
    
## <a name="more-information"></a><span data-ttu-id="d5551-183">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d5551-183">More information</span></span>
<span data-ttu-id="d5551-184"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="d5551-184"></span></span>

- <span data-ttu-id="d5551-185">Если в организации требуется сохранять данные всех почтовых ящиков в течение определенного периода времени, следует учесть следующие моменты, прежде чем перевести все почтовые ящики в организации в режим хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="d5551-185">If your organization requires that all mailbox data has to preserved for a specific period of time, consider the following before you place all mailboxes in an organization on Litigation Hold.</span></span>
    
  - <span data-ttu-id="d5551-p116">Если вы используете предыдущую команду для перевода всех почтовых ящиков в организации (или подмножества почтовых ящиков, соответствующих требованиям указанного фильтра получателей) в режим хранения для судебного разбирательства, на хранение помещаются только почтовые ящики, доступные на момент выполнения команды. Чтобы применить функцию хранения к позднее созданным почтовым ящикам, команду понадобится выполнить еще раз. Если вы часто создаете почтовые ящики, можно запланировать выполнение команды с необходимой частотой.</span><span class="sxs-lookup"><span data-stu-id="d5551-p116">When you use the previous command to place a hold on all mailboxes in an organization (or a subset of mailboxes matching a specified recipient filter) only mailboxes that exist at the time that you run the command are placed on hold. If you create new mailboxes later, you have to run the command again to place the new mailboxes on hold. If you create new mailboxes often, you can run the command as a scheduled task as frequently as required.</span></span>
    
  - <span data-ttu-id="d5551-p117">Помещение всех почтовых ящиков на хранение для судебного разбирательства оказывают значительное влияние на размер почтового ящика. В организации Exchange Server 2013 планирование достаточно места для удовлетворения требований организации хранения.</span><span class="sxs-lookup"><span data-stu-id="d5551-p117">Placing all mailboxes on Litigation Hold can significantly impact mailbox sizes. In an Exchange Server 2013 organization, plan for adequate storage to meet your organization's preservation requirements.</span></span>
    
  - <span data-ttu-id="d5551-p118">Папка элементов для восстановления имеет свой собственный ограничение хранилища, поэтому элементов в папке не считаются достигло предельного значения хранилища почтовых ящиков. Как объяснялось ранее сохранение данных почтовых ящиков на длительный период времени будет привести к росту папки восстанавливаемых элементов в почтовом ящике пользователя и архивация. Чтобы обеспечить для этого увеличения в Exchange Online, квота для папки элементов для восстановления автоматически увеличивается от 30 ГБ на 100 ГБ при постановка почтового ящика на хранение для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="d5551-p118">The Recoverable Items folder has its own storage limit, so items in the folder don't count towards the mailbox storage limit. As previously explained, preserving mailbox data for a long period of time will result in growth of the Recoverable Items folder in a user's mailbox and archive. To accommodate for this increase in Exchange Online, the quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when you place a mailbox on Litigation Hold.</span></span> 
    
    <span data-ttu-id="d5551-p119">В Exchange Server 2013, ограничение хранилища по умолчанию для папки элементов для восстановления также — 30 ГБ. Рекомендуется периодически отслеживать размер этой папки, чтобы убедиться, что она не достигает предела. Для получения дополнительных сведений см [Папки восстанавливаемых элементов](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5551-p119">In Exchange Server 2013, the default storage limit for the Recoverable Items folder is also 30 GB. We recommend that you periodically monitor the size of this folder to ensure it doesn't reach the limit. For more information, see [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span></span>
    
- <span data-ttu-id="d5551-p120">В предыдущей команде, которая переводит все почтовые ящики в режим хранения, используется фильтр получателей, возвращающий все почтовые ящики пользователей. Вы можете использовать другие свойства получателей, чтобы вернуть список определенных почтовых ящиков, которые затем можно передать командлету **Set-Mailbox** для перевода этих почтовых ящиков в режим хранения для судебного разбирательства.</span><span class="sxs-lookup"><span data-stu-id="d5551-p120">The previous command to place a hold on all mailboxes uses a recipient filter that returns all user mailboxes. You can use other recipient properties to return a list of specific mailboxes that you can then pipe to the **Set-Mailbox** cmdlet to place a Litigation Hold on those mailboxes.</span></span> 
    
    <span data-ttu-id="d5551-p121">Вот несколько примеров использования командлетов **Get-Mailbox** и **Get-Recipient** для получения подмножества пользователей на основе общих свойств пользователей или почтовых ящиков. В этих примерах предполагается, что соответствующие свойства почтовых ящиков (например,  _CustomAttributeN_ или  _Department_) заполнены.</span><span class="sxs-lookup"><span data-stu-id="d5551-p121">Here are some examples of using the **Get-Mailbox** and **Get-Recipient** cmdlets to return a subset of mailboxes based on common user or mailbox properties. These examples assume that relevant mailbox properties (such as  _CustomAttributeN_ or  _Department_) have been populated.</span></span>
    
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

    <span data-ttu-id="d5551-p122">Вы можете использовать в фильтре другие свойства, чтобы включать и исключать почтовые ящики. Подробные сведения см. в статье [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span><span class="sxs-lookup"><span data-stu-id="d5551-p122">You can use other user mailbox properties in a filter to include or exclude mailboxes. For details, see [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span></span>
    

