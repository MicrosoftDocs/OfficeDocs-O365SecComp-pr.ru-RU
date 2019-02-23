---
title: Поиск содержимого при обнаружении электронных данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'Используйте сценарий PowerShell для создания поискового запроса на обнаружение электронных данных на месте в Exchange Online на основе поиска, созданного в центре &amp; безопасности и соответствия требованиям Office 365. '
ms.openlocfilehash: fff50b7dcd89790c84bb2911f560ce1b061b8f17
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216049"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="9c4ad-103">Поиск содержимого при обнаружении электронных данных</span><span class="sxs-lookup"><span data-stu-id="9c4ad-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="9c4ad-p101">Функция поиска контента в центре безопасности &amp; и соответствия требованиям Office 365 позволяет выполнять поиск во всех почтовых ящиках в Организации. В отличие от обнаружения электронных данных на месте в Exchange Online (где можно выполнить поиск до 10 000 почтовых ящиков), количество целевых почтовых ящиков в одной функции поиска не ограничено. Для сценариев, требующих проведения поиска на уровне Организации, можно использовать поиск контента для поиска во всех почтовых ящиках. Затем вы можете использовать функции рабочего процесса обнаружения электронных данных на месте для выполнения других задач, связанных с обнаружением электронных данных, таких как помещение почтовых ящиков в удержание и экспорт результатов поиска. Например, предположим, что необходимо выполнить поиск по всем почтовым ящикам, чтобы определить конкретные custodians, которые отвечают на юридический случай. Вы можете использовать поиск контента в центре безопасности &amp; и соответствия требованиям для поиска всех почтовых ящиков в Организации, чтобы определить, какие из них отвечают. Затем вы можете использовать этот список почтовых ящиков хранитель в качестве исходных почтовых ящиков для поиска с обнаружением электронных данных на месте в Exchange Online. Использование обнаружения электронных данных на месте также позволяет хранить эти почтовые ящики, копировать результаты поиска в почтовый ящик обнаружения и экспортировать результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p101">The Content Search feature in the Office 365 Security &amp; Compliance Center allows you to search all mailboxes in your organization. Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search. For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes. Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results. For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case. You can use Content Search in the Security &amp; Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case. Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online. Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="9c4ad-p102">В этой статье описывается сценарий, который можно использовать для создания поискового запроса на обнаружение электронных данных на месте в Exchange Online с помощью списка исходных почтовых ящиков и поискового запроса из &amp; поиска, созданного в центре соответствия требованиям безопасности. Ниже представлен обзор процесса.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p102">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security &amp; Compliance Center. Here's an overview of the process:</span></span>
  
[<span data-ttu-id="9c4ad-114">Шаг 1. Создание запроса на поиск содержимого по всем почтовым ящикам в организации</span><span class="sxs-lookup"><span data-stu-id="9c4ad-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="9c4ad-115">Шаг 2: подключение к центру безопасности &amp; и соответствия требованиям Exchange Online в едином удаленном сеансе PowerShell</span><span class="sxs-lookup"><span data-stu-id="9c4ad-115">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="9c4ad-116">Шаг 3. Запуск сценария для создания запроса на обнаружение электронных данных на месте, в основе которого лежит поиск содержимого</span><span class="sxs-lookup"><span data-stu-id="9c4ad-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="9c4ad-117">Шаг 4. Запуск поиска с обнаружением электронных данных на месте</span><span class="sxs-lookup"><span data-stu-id="9c4ad-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="9c4ad-118">Шаг 1. Создание запроса на поиск содержимого по всем почтовым ящикам в организации</span><span class="sxs-lookup"><span data-stu-id="9c4ad-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="9c4ad-p103">Первым этапом является использование центра безопасности &amp; (или _Амп_ Security Security Center) для создания поиска контента, который выполняет поиск во всех почтовых ящиках в Организации. Количество почтовых ящиков для одного поиска контента не ограничено. Укажите соответствующий запрос ключевого слова (или запрос для типов конфиденциальной информации), чтобы поиск возвращал только те исходные почтовые ящики, которые относятся к расследованию. При необходимости уточните поисковый запрос, чтобы сузить область результатов поиска и исходные почтовые ящики, которые возвращаются.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p103">The first step is to use the Security &amp; Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization. There's no limit for the number of mailboxes for a single Content Search. Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation. If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9c4ad-p104">Если ничего не найдено, операция обнаружения электронных данных на месте не будет создана при выполнении сценария на шаге 3. Возможно, потребуется изменить поисковый запрос, а затем повторить поиск содержимого.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p104">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3. You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="9c4ad-125">Поиск во всех &amp; почтовых ящиках с помощью центра соответствия требованиям безопасности</span><span class="sxs-lookup"><span data-stu-id="9c4ad-125">Use the Security &amp; Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="9c4ad-126">[Перейдите в центр безопасности &amp; и соответствия требованиям Office 365](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9c4ad-126">[Go to the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="9c4ad-127">Нажмите **кнопку &amp; Поиск**в расследовании, выберите пункт **Поиск содержимого**, а затем](media/O365-MDM-CreatePolicy-AddIcon.gif)нажмите кнопку **создать** ![значок добавления.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-127">Click **Search &amp; investigation**, click **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="9c4ad-128">На странице **Новый поиск** введите имя запроса на поиск содержимого.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="9c4ad-129">В разделе **Где нужно искать?** выберите **Поиск во всех почтовых ящиках** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="9c4ad-p105">В поле в разделе **что вы хотите искать?** введите поисковый запрос в поле. Вы можете указать ключевые слова, свойства сообщений, такие как даты отправки и получения, или свойства документа, такие как имена файлов или Дата последнего изменения документа. Можно использовать более сложные запросы, использующие логический оператор (например, AND, OR, NOT или NEAR), а также выполнять поиск конфиденциальной информации (например, номера социального страхования) в сообщениях. Дополнительные сведения о создании поисковых запросов приведены в разделе [запросы ключевых слов для поиска контента](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p105">In the box under **What do you want us to look for?**, type a search query in the box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages. For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="9c4ad-134">Щелкните **Поиск**, чтобы сохранить параметры поиска и начать поиск.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="9c4ad-p106">Через некоторое время в области сведений отображается оценка результатов поиска. Оценка включает общий размер и количество элементов для результатов поиска. После завершения поиска можно выполнить предварительный просмотр результатов поиска. При необходимости нажмите кнопку **Обновить**![значок](media/O365-MDM-Policy-RefreshIcon.gif) обновления, чтобы обновить сведения в области сведений.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p106">After a while, an estimate of the search results displayed in the details pane. The estimate includes the total size and number of items for the search results. After the search is completed, you can preview the search results. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="9c4ad-139">При необходимости уточните поисковый запрос, чтобы сузить область результатов поиска, а затем повторите поиск.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="9c4ad-140">Использование PowerShell центра соответствия требованиям _Амп_ для поиска во всех почтовых ящиках</span><span class="sxs-lookup"><span data-stu-id="9c4ad-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="9c4ad-p107">Вы также можете использовать командлет **New – ComplianceSearch** для поиска всех почтовых ящиков в Организации. Первый шаг — [Подключение к PowerShell центра безопасности &amp; для Office 365](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p107">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization. The first step is to [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="9c4ad-p108">Ниже приведен пример использования PowerShell для поиска всех почтовых ящиков в Организации. Поисковый запрос возвращает все сообщения, отправленные между 1 января 2015 и 30 июня 2015 и содержащие фразу "финансовый отчет" в строке темы. Первая команда создает поиск, а вторая команда выполняет поиск.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p108">Here's an example of using PowerShell to search all mailboxes in your organization. The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line. The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="9c4ad-146">Дополнительные сведения см. в статье [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span><span class="sxs-lookup"><span data-stu-id="9c4ad-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="9c4ad-147">Проверка количества исходных почтовых ящиков в запросе на поиск содержимого</span><span class="sxs-lookup"><span data-stu-id="9c4ad-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="9c4ad-p109">Поиск контента Возвращает максимум 1 000 исходных почтовых ящиков, которые содержат результаты поиска. При наличии более чем 1 000 почтовых ящиков, которые содержат контент, соответствующий поисковому запросу, в поиск контента, созданный на предыдущем шаге, включаются только первые 1 000 почтовых ящиков с большинством результатов поиска. Таким образом, если почтовые ящики более чем 1 000 содержат результаты поиска, некоторые из них не будут включены в список исходных почтовых ящиков, скопированных в новый запрос на обнаружение электронных данных на месте, созданный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p109">A Content Search returns a maximum of 1,000 source mailboxes that contain search results. If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step. So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="9c4ad-151">Чтобы облегчить создание поиска контента, не превышающего 1 000 исходных почтовых ящиков, выполните указанные ниже действия, чтобы выполнить сценарий, в котором отображается количество исходных почтовых ящиков (которые содержат результаты поиска), возвращаемых при поиске контента, созданном на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="9c4ad-p110">Сохраните приведенный ниже текст в файле скрипта PowerShell с помощью суффикса имени файла. ps1. Например, вы можете сохранить его в файл с именем `SourceMailboxes.ps1`.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p110">Save the following text to a PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
                  "Please wait until the search finishes.";
                  break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
                  "The Content Search " + $SearchName + " didn't return any useful results.";
                  break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  "Number of mailboxes that have search hits: " + $mailboxes.Count
  ```

2. <span data-ttu-id="9c4ad-154">В PowerShell центра безопасности _Амп_ соответствие требованиям перейдите к папке, в которой расположен скрипт, созданный на предыдущем шаге, и запустите его. Например:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="9c4ad-155">Когда вам это будет предложено, введите имя запроса на поиск содержимого, созданного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="9c4ad-156">Сценарий отобразит количество исходных почтовых ящиков, которые содержат результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="9c4ad-p111">Если вы используете более 1 000 исходных почтовых ящиков, попробуйте создать два (или более) поиска контента. Например, найдите половину почтовых ящиков организации в одном поиске контента, а другую половину в другом поиске контента. Вы также можете изменить критерии поиска, чтобы уменьшить количество почтовых ящиков, содержащих результаты поиска. Например, можно включить диапазон дат или уточнить запрос ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p111">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches. For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search. You could also change the search criteria to reduce the number of mailboxes that contain search results. For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="9c4ad-161">Шаг 2: подключение к центру безопасности &amp; и соответствия требованиям Exchange Online в едином удаленном сеансе PowerShell</span><span class="sxs-lookup"><span data-stu-id="9c4ad-161">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="9c4ad-p112">Следующий шаг — подключение Windows PowerShell к центру безопасности &amp; и соответствия требованиям в организации Exchange Online. Это необходимо, так как скрипт, выполняемый на шаге 3, должен иметь доступ к командлетам поиска контента в &amp; центре соответствия требованиям безопасности и командлетам обнаружения электронных данных на месте в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p112">The next step is to connect Windows PowerShell to both the Security &amp; Compliance Center and to your Exchange Online organization. This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security &amp; Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="9c4ad-p113">Сохраните приведенный ниже текст в файле скрипта Windows PowerShell с помощью суффикса имени файла. ps1. Например, вы можете сохранить его в файл с именем `ConnectEXO-CC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="9c4ad-166">На локальном компьютере откройте Windows PowerShell, перейдите к папке, в которой расположен скрипт, созданный на предыдущем шаге, и запустите его. Например:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="9c4ad-p114">Как узнать, работает ли это? После выполнения сценария командлеты из центра соответствия требованиям безопасности &amp; и Exchange Online импортируются в локальный сеанс PowerShell. Если ошибки не появляются, вы успешно подключены. Быстрая проверка заключается в запуске командлета центра &amp; обеспечения безопасности (например, **Install-унифиедкомплианцепререкуисите** ) и командлета Exchange Online, например **Get-Mailbox**.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p114">How do you know if this worked? After you run the script, cmdlets from the Security &amp; Compliance Center and Exchange Online are imported into your local PowerShell session. If you don't receive any errors, you connected successfully. A quick test is to run a Security &amp; Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="9c4ad-171">Шаг 3. Запуск сценария для создания запроса на обнаружение электронных данных на месте, в основе которого лежит поиск содержимого</span><span class="sxs-lookup"><span data-stu-id="9c4ad-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="9c4ad-p115">После создания двойного сеанса PowerShell в действии 2 необходимо выполнить сценарий, который будет преобразовывать существующий поиск контента в поиск обнаружения электронных данных на месте. Вот что делает сценарий:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p115">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search. Here's what the script does:</span></span>
  
- <span data-ttu-id="9c4ad-174">Запрашивает имя запроса на поиск содержимого, который требуется преобразовать.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="9c4ad-p116">Проверяет, завершен ли поиск содержимого. Если ничего не найдено, запрос на обнаружение электронных данных на месте не будет создан.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p116">Verifies that the Content Search has completed running. If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="9c4ad-177">Сохраняет в переменной список тех исходных почтовых ящиков из запроса на поиск содержимого, которые содержат результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="9c4ad-p117">Создает поиск с обнаружением электронных данных на месте с указанными ниже свойствами. Обратите внимание, что новый поиск не запускается. Он запускается на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p117">Creates a new In-Place eDiscovery search, with the following properties. Note that the new search isn't started. You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="9c4ad-p118">**Name** — имя нового поиска использует следующий формат: \<имя _MBSearch1 поиска\>контента. Если выполнить сценарий повторно и использовать тот же Поиск исходного контента, будет использоваться \<имя _MBSearch2 поиска\>контента.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p118">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1. If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="9c4ad-183">**Исходные** почтовые ящики — все почтовые ящики из поиска контента, содержащие результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="9c4ad-p119">**Поисковый запрос** — новый поиск использует поисковый запрос из поиска контента. Если поиск контента включает весь контент (где запрос поиска пуст), новый поиск также будет содержать пустой поисковый запрос и будет включать весь контент, найденный в исходных почтовых ящиках.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p119">**Search query** - The new search uses the search query from the Content Search. If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="9c4ad-p120">**Только оценить Поиск** — новый поиск помечается как поиск только для оценки. После запуска он не будет копировать результаты поиска в почтовый ящик обнаружения.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p120">**Estimate only search** - The new search is marked as an estimate-only search. It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="9c4ad-p121">Сохраните приведенный ниже текст в файле скрипта Windows PowerShell, используя суффикс имени файла PS1. Например, вы можете сохранить его в файл с именем `CreateMBSearchFromComplianceSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1. For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
  ```
  [CmdletBinding()]
  Param(
      [Parameter(Mandatory=$True,Position=1)]
      [string]$SearchName,
      [switch]$original,
      [switch]$restoreOriginal
  )
  $search = Get-ComplianceSearch $SearchName
  if ($search.Status -ne "Completed")
  {
    "Please wait until the search finishes";
    break;
  }
  $results = $search.SuccessResults;
  if (($search.Items -le 0) -or ([string]::IsNullOrWhiteSpace($results)))
  {
    "The Content Search " + $SearchName + " didn't return any useful results";
    "A mailbox search object wasn't created";
    break;
  }
  $mailboxes = @();
  $lines = $results -split '[\r\n]+';
  foreach ($line in $lines)
  {
      if ($line -match 'Location: (\S+),.+Item count: (\d+)' -and $matches[2] -gt 0)
      {
          $mailboxes += $matches[1];
      }
  }
  $msPrefix = $SearchName + "_MBSearch";
  $I = 1;
  $mbSearches = Get-MailboxSearch;
  while ($true)
  {
      $found = $false;
      $mbsName = "$msPrefix$I";
      foreach ($mbs in $mbSearches)
      {
          if ($mbs.Name -eq $mbsName)
          {
              $found = $true;
              break;
          }
      }
      if (!$found)
      {
          break;
      }
      $I++;
  }
  $query = $search.KeywordQuery;
  if ([string]::IsNullOrWhiteSpace($query))
  {
      $query = $search.ContentMatchQuery;
  }
  if ([string]::IsNullOrWhiteSpace($query))
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -EstimateOnly;
  }
  else
  {
    New-MailboxSearch "$msPrefix$i" -SourceMailboxes $mailboxes -SearchQuery $query -EstimateOnly;
  }
  
  ```

2. <span data-ttu-id="9c4ad-190">В сеансе Windows PowerShell, созданном на шаге 2, перейдите к папке, в которой расположен скрипт, созданный на предыдущем шаге, и запустите его. Например:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="9c4ad-191">По запросу введите имя поиска контента, который нужно преобразовать в поиск с обнаружением электронных данных на месте (например, поиск, созданный на шаге 1), а затем нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="9c4ad-p122">При успешном выполнении сценария создается поиск с обнаружением электронных данных на месте с состоянием **NotStarted**. Выполните команду  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL`, чтобы отобразить свойства нового поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p122">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**. Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="9c4ad-194">Шаг 4. Запуск поиска с обнаружением электронных данных на месте</span><span class="sxs-lookup"><span data-stu-id="9c4ad-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="9c4ad-p123">Сценарий, выполняемый на шаге 3, создает запрос на поиск с обнаружением электронных данных на месте, но не запускает его. Теперь необходимо запустить поиск, чтобы получить оценку его результатов.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p123">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it. The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="9c4ad-197">В центре администрирования Exchange перейдите к разделу **Управление** \> соответствием для **обнаружения &amp; электронных данных на месте**.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="9c4ad-198">В списке выберите поиск с обнаружением электронных данных на месте, созданный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="9c4ad-199">Нажмите кнопку **Поиск поиска** ![](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Оценка результатов поиска** , чтобы начать поиск и получить оценку общего размера и количества элементов, возвращенных в результате поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="9c4ad-p124">Оценки отображаются в области сведений. Нажмите кнопку **Обновить** ![значок](media/O365-MDM-Policy-RefreshIcon.gif) обновления, чтобы обновить сведения, отображаемые в области сведений.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p124">The estimates are displayed in the details pane. Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="9c4ad-202">Для предварительного просмотра результатов после завершения поиска нажмите кнопку **Предварительный просмотр результатов поиска** в области сведений.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="9c4ad-203">Действия после создания и запуска поиска с обнаружением электронных данных на месте</span><span class="sxs-lookup"><span data-stu-id="9c4ad-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="9c4ad-204">После создания и запуска поиска с обнаружением электронных данных на месте, который был создан с помощью сценария на шаге 3, можно выполнять различные стандартные действия над результатами поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="9c4ad-205">Создание хранения на месте</span><span class="sxs-lookup"><span data-stu-id="9c4ad-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="9c4ad-206">В центре администрирования Exchange перейдите к разделу **Управление** \> соответствием при обнаружении \*\* &amp; электронных данных на месте\*\*.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="9c4ad-207">В представлении списка выберите Поиск с обнаружением электронных данных на месте, созданный на шаге 3, и нажмите кнопку **изменить** ![значок](media/O365_MDM_CreatePolicy_EditIcon.gif)редактирования.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="9c4ad-208">На странице **Удержание на месте** установите флажок **Поставить содержимое выбранных почтовых ящиков, соответствующее поисковому запросу, на удержание**, а затем выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="9c4ad-p125">**Хранить бессрочно** — выберите этот параметр, чтобы поместить элементы, возвращаемые поиском, в неопределенное удержание. Элементы на удержании будут сохранены до тех пор, пока почтовый ящик не будет удален из поиска или не будет удален Поиск.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p125">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold. Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="9c4ad-p126">**Укажите количество дней хранения элементов относительно даты получения** — выберите этот параметр, чтобы удерживать элементы для определенного периода. Продолжительность рассчитывается от даты получения или создания элемента почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p126">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period. The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="9c4ad-213">Нажмите кнопку **Сохранить**, чтобы создать запрос на удержание на месте, а затем повторите поиск.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="9c4ad-214">Return to top</span><span class="sxs-lookup"><span data-stu-id="9c4ad-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="9c4ad-215">Копирование результатов поиска</span><span class="sxs-lookup"><span data-stu-id="9c4ad-215">Copy the search results</span></span>

1. <span data-ttu-id="9c4ad-216">В центре администрирования Exchange перейдите к разделу **Управление** \> соответствием при обнаружении \*\* &amp; электронных данных на месте\*\*.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="9c4ad-217">В списке выберите поиск с обнаружением электронных данных на месте, созданный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="9c4ad-218">Щелкните \*\*\*\* ![значок](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)поиска поиска, а затем в раскрывающемся списке выберите команду **Копировать результаты поиска** .</span><span class="sxs-lookup"><span data-stu-id="9c4ad-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="9c4ad-219">В окне **Копировать результаты поиска** выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="9c4ad-220">**Включить элементы** , не включаемые в Поиск — установите этот флажок, чтобы включить элементы почтовых ящиков, для которых не удалось выполнить поиск (например, сообщения с вложениями типов файлов, которые не удалось индексировать при поиске Exchange).</span><span class="sxs-lookup"><span data-stu-id="9c4ad-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="9c4ad-p127">**Enable un— Дедупликация** — установите этот флажок, чтобы исключить повторяющиеся сообщения. В почтовый ящик найденных сообщений будет скопирован только один экземпляр сообщения.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p127">**Enable de-duplication** - Select this check box to exclude duplicate messages. Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="9c4ad-223">**Включить полное ведение журнала** — установите этот флажок, чтобы включить полный журнал в результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="9c4ad-224">**Отправить мне сообщение после завершения копирования** — установите этот флажок, чтобы получать уведомление по завершении поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="9c4ad-225">**Копировать результаты в этот почтовый ящик обнаружения** нажмите кнопку **Обзор** , чтобы выбрать почтовый ящик найденных сообщений, в который нужно скопировать результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="9c4ad-226">Нажмите кнопку **Копировать**, чтобы начать процесс копирования результатов поиска в указанный почтовый ящик найденных сообщений.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="9c4ad-227">Нажмите кнопку **Обновить** ![значок](media/O365-MDM-Policy-RefreshIcon.gif) обновления, чтобы обновить информацию о состоянии копирования, отображаемую в области сведений.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="9c4ad-228">После завершения копирования нажмите кнопку **Открыть**, чтобы открыть почтовый ящик найденных сообщений для просмотра результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="9c4ad-229">Экспорт результатов поиска</span><span class="sxs-lookup"><span data-stu-id="9c4ad-229">Export the search results</span></span>

1. <span data-ttu-id="9c4ad-230">В центре администрирования Exchange перейдите к разделу **Управление** \> соответствием при обнаружении \*\* &amp; электронных данных на месте\*\*.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="9c4ad-231">В списке выберите запрос на поиск с обнаружением электронных данных на месте, созданный на шаге 3, и нажмите кнопку **Экспорт в PST-файл**.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="9c4ad-232">В окне **Средство экспорта PST обнаружения электронных данных** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9c4ad-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="9c4ad-233">Нажмите кнопку **Обзор**, чтобы указать, откуда нужно загрузить PST-файл.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="9c4ad-p128">Установите флажок **Включить дедупликацию**, чтобы исключить повторяющиеся сообщения. В PST-файл будет включен только один экземпляр сообщения.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="9c4ad-p129">Установите флажок **Включить элементы, недоступные для поиска.**, чтобы добавить недоступные для поиска элементы почтовых ящиков (например, сообщения с вложенными файлами таких типов, которые не могут быть индексированы поиском Exchange). Недоступные для поиска элементы экспортируются в отдельный PST-файл.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="9c4ad-238">Нажмите кнопку **Начать** для экспорта результатов поиска в PST-файл.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="9c4ad-239">Откроется окно со сведениями о состоянии процесса экспорта.</span><span class="sxs-lookup"><span data-stu-id="9c4ad-239">A window is displayed that contains status information about the export process.</span></span>
