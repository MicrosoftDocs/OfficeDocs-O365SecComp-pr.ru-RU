---
title: Поиск содержимого при обнаружении электронных данных
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 55f31488-288a-473a-9b9e-831a11e3711a
description: 'Использование скрипта PowerShell для создания поискового запроса на локальное обнаружение электронных данных в Exchange Online на основании поиска, созданные в Office 365 безопасность &amp; центре соответствия требованиям. '
ms.openlocfilehash: d2f4f845e8c819eed67c3a234bff208a11fb571c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534909"
---
# <a name="use-content-search-in-your-ediscovery-workflow"></a><span data-ttu-id="c8a98-103">Поиск содержимого при обнаружении электронных данных</span><span class="sxs-lookup"><span data-stu-id="c8a98-103">Use Content Search in your eDiscovery workflow</span></span>

<span data-ttu-id="c8a98-p101">Компонент поиска контента в Office 365 безопасность &amp; центре соответствия требованиям позволяет выполнять поиск всех почтовых ящиков в организации. В отличие от электронного обнаружения на месте в Exchange Online (где можно выполнить поиск до 10 000 почтовых ящиков) не предусмотрено ограничений для количество почтовых ящиков конечного одним. Для сценариев, где требуется выполнение поиска по всей организации можно использовать поиск контента для поиска всех почтовых ящиков. Затем можно использовать возможности рабочего процесса электронного обнаружения на месте для выполнения других задач, связанных с обнаружения электронных данных, таких как размещение почтовые ящики на хранение и результатов поиска в экспорт. Например предположим, необходимо выполнить поиск всех почтовых ящиков для идентификации определенного custodians, которые реагирует на юридических дела. Поиск контента можно использовать в системы &amp; центре соответствия требованиям для поиска всех почтовых ящиков в организации, чтобы определить те, которые реагирует на регистр. Затем можно использовать этот список почтовых ящиков custodian как исходных почтовых ящиков для поиска обнаружения электронных данных на месте в Exchange Online. С помощью электронного обнаружения на месте позволяет блокировка этих исходных почтовых ящиков и копирование результатов поиска в почтовый ящик обнаружения экспортировать результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p101">The Content Search feature in the Office 365 Security &amp; Compliance Center allows you to search all mailboxes in your organization. Unlike In-Place eDiscovery in Exchange Online (where you can search up to 10,000 mailboxes), there are no limits for the number of target mailboxes in a single search. For scenarios that require you to perform organization-wide searches, you can use Content Search to search all mailboxes. Then you can use the workflow features of In-Place eDiscovery to perform other eDiscovery-related tasks, such as placing mailboxes on hold and exporting search results. For example, let's say you have to search all mailboxes to identify specific custodians that are responsive to a legal case. You can use Content Search in the Security &amp; Compliance Center to search all mailboxes in your organization to identify those that are responsive to the case. Then you can use that list of custodian mailboxes as the source mailboxes for an In-Place eDiscovery search in Exchange Online. Using In-Place eDiscovery also allows you to put a hold on those source mailboxes, copy search results to a discovery mailbox, and export the search results.</span></span>
  
<span data-ttu-id="c8a98-p102">Этот раздел содержит скрипт, который можно запустить для создания поискового запроса на локальное обнаружение электронных данных в Exchange Online с помощью список исходных почтовых ящиков и запросов поиска из поиска, созданные в системы &amp; центре соответствия требованиям. Ниже приведен обзор процесса:</span><span class="sxs-lookup"><span data-stu-id="c8a98-p102">This topic includes a script that you can run to create an In-Place eDiscovery search in Exchange Online by using the list of source mailboxes and search query from a search created in the Security &amp; Compliance Center. Here's an overview of the process:</span></span>
  
[<span data-ttu-id="c8a98-114">Шаг 1. Создание запроса на поиск содержимого по всем почтовым ящикам в организации</span><span class="sxs-lookup"><span data-stu-id="c8a98-114">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>](#step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization)

[<span data-ttu-id="c8a98-115">Шаг 2: Подключение к безопасности &amp; центре соответствия требованиям и Exchange Online в одном удаленного сеанса PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8a98-115">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>](#step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session)
  
[<span data-ttu-id="c8a98-116">Шаг 3. Запуск сценария для создания запроса на обнаружение электронных данных на месте, в основе которого лежит поиск содержимого</span><span class="sxs-lookup"><span data-stu-id="c8a98-116">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>](#step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search)

[<span data-ttu-id="c8a98-117">Шаг 4. Запуск поиска с обнаружением электронных данных на месте</span><span class="sxs-lookup"><span data-stu-id="c8a98-117">Step 4: Start the In-Place eDiscovery search</span></span>](#step-4-start-the-in-place-ediscovery-search)

## <a name="step-1-create-a-content-search-to-search-all-mailboxes-in-your-organization"></a><span data-ttu-id="c8a98-118">Шаг 1. Создание запроса на поиск содержимого по всем почтовым ящикам в организации</span><span class="sxs-lookup"><span data-stu-id="c8a98-118">Step 1: Create a Content Search to search all mailboxes in your organization</span></span>

<span data-ttu-id="c8a98-p103">Первым этапом является использование защиты &amp; центре соответствия требованиям (или безопасность и соответствие требованиям центр PowerShell) для создания поиска контента, который осуществляет поиск по всем почтовым ящикам в организации. Нет ограничений для количество почтовых ящиков для одного поиска контента. Укажите запрос на соответствующее ключевое слово (или запрос для типов конфиденциальной информации), чтобы поиск возвращает только тех исходных почтовых ящиков важные для расследования. При необходимости уточнения запросов поиска, чтобы сузить результаты поиска и исходных почтовых ящиков, которые возвращаются.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p103">The first step is to use the Security &amp; Compliance Center (or Security & Compliance Center PowerShell) to create a Content Search that searches all mailboxes in your organization. There's no limit for the number of mailboxes for a single Content Search. Specify an appropriate keyword query (or a query for sensitive information types) so that the search returns only those source mailboxes that are relevant to your investigation. If necessary, refine the search query to narrow the scope of search results and source mailboxes that are returned.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c8a98-p104">Если ничего не найдено, операция обнаружения электронных данных на месте не будет создана при выполнении сценария на шаге 3. Возможно, потребуется изменить поисковый запрос, а затем повторить поиск содержимого.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p104">If the source Content Search doesn't return any results, an In-Place eDiscovery won't be created when you run the script in Step 3. You may have to revise the search query then rerun the Content Search to return search results.</span></span> 
  
### <a name="use-the-security-amp-compliance-center-to-search-all-mailboxes"></a><span data-ttu-id="c8a98-125">Использование безопасности &amp; центре соответствия требованиям для поиска всех почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="c8a98-125">Use the Security &amp; Compliance Center to search all mailboxes</span></span>

1. <span data-ttu-id="c8a98-126">[Откройте раздел безопасность Office 365 &amp; центре соответствия требованиям](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="c8a98-126">[Go to the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md).</span></span> 
    
2. <span data-ttu-id="c8a98-127">Нажмите кнопку **поиска &amp; расследования**, нажмите кнопку **Поиск контента**и нажмите кнопку **Создать** ![значком Добавить](media/O365-MDM-CreatePolicy-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="c8a98-127">Click **Search &amp; investigation**, click **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
3. <span data-ttu-id="c8a98-128">На странице **Новый поиск** введите имя запроса на поиск содержимого.</span><span class="sxs-lookup"><span data-stu-id="c8a98-128">On the **New search** page, type a name for the Content Search.</span></span> 
    
4. <span data-ttu-id="c8a98-129">В разделе **Где нужно искать?** выберите **Поиск во всех почтовых ящиках** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="c8a98-129">Under **Where do you want us to look?**, click **Search all mailboxes**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="c8a98-p105">В поле в разделе **необходимые действия "мне нравится" следует искать?**, введите в поле запрос поиска. Можно указать ключевые слова, сообщение свойства, например, отправленных и полученных даты, или свойств документа, таких как имена файлов или Дата последнего изменения документа. Можно использовать более сложные запросы, не используйте логический оператор, например и, или или РЯДОМ, или можно также выполнить поиск конфиденциальной информации (например, номера социального страхования) в сообщениях. Дополнительные сведения о создании поисковых запросов можно [запросах по ключевым словам для поиска контента](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="c8a98-p105">In the box under **What do you want us to look for?**, type a search query in the box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as AND, OR, NOT or NEAR, or you can also search for sensitive information (such as social security numbers) in messages. For more information about creating search queries, see [Keyword queries for Content Search](keyword-queries-and-search-conditions.md).</span></span>
    
6. <span data-ttu-id="c8a98-134">Щелкните **Поиск**, чтобы сохранить параметры поиска и начать поиск.</span><span class="sxs-lookup"><span data-stu-id="c8a98-134">Click **Search** to save the search settings and start the search.</span></span> 
    
    <span data-ttu-id="c8a98-p106">Через некоторое время оценку результатов поиска, отображаемые в области сведений. Оценка включает в себя общего размера и числа элементов для результатов поиска. После завершения поиска можно выполнить предварительный просмотр результатов поиска. При необходимости нажмите кнопку **Обновить**![значок обновления](media/O365-MDM-Policy-RefreshIcon.gif) для обновления данных в области сведений.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p106">After a while, an estimate of the search results displayed in the details pane. The estimate includes the total size and number of items for the search results. After the search is completed, you can preview the search results. If necessary, click **Refresh**![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
7.  <span data-ttu-id="c8a98-139">При необходимости уточните поисковый запрос, чтобы сузить область результатов поиска, а затем повторите поиск.</span><span class="sxs-lookup"><span data-stu-id="c8a98-139">If necessary, refine the search query to narrow the scope of search results and then restart the search.</span></span> 
    
### <a name="use-security--compliance-center-powershell-to-search-all-mailboxes"></a><span data-ttu-id="c8a98-140">Использование безопасности и соответствия требованиям центр PowerShell для поиска всех почтовых ящиков</span><span class="sxs-lookup"><span data-stu-id="c8a98-140">Use Security & Compliance Center PowerShell to search all mailboxes</span></span>

<span data-ttu-id="c8a98-p107">Также можно использовать командлет **New-ComplianceSearch** для поиска всех почтовых ящиков в организации. Первым шагом является [подключение к Office 365 безопасность &amp; PowerShell центр соответствия](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span><span class="sxs-lookup"><span data-stu-id="c8a98-p107">You can also use the **New-ComplianceSearch** cmdlet to search all mailboxes in your organization. The first step is to [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=627084).</span></span>
  
<span data-ttu-id="c8a98-p108">Ниже приведен пример использования PowerShell для поиска всех почтовых ящиков в организации. Поисковый запрос возвращает все сообщения, отправленные между 1 января 2015 и 30 июня 2015, которые содержат фразу «финансовых отчетов» в строке темы. Первая команда создает поиск, и вторая команда запускается поиск.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p108">Here's an example of using PowerShell to search all mailboxes in your organization. The search query returns all messages sent between January 1, 2015 and June 30, 2015 and that contain the phrase "financial report" in the subject line. The first command creates the search, and the second command runs the search.</span></span> 
  
```
New-ComplianceSearch -Name "Search All-Financial Report" -ExchangeLocation all -ContentMatchQuery 'sent>=01/01/2015 AND sent<=06/30/2015 AND subject:"financial report"'
```

```
Start-ComplianceSearch -Identity "Search All-Financial Report"
```

<span data-ttu-id="c8a98-146">Дополнительные сведения см. в статье [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span><span class="sxs-lookup"><span data-stu-id="c8a98-146">For more information, see [New-ComplianceSearch](https://go.microsoft.com/fwlink/p/?LinkId=517935).</span></span>
  
### <a name="verify-the-number-of-source-mailboxes-in-the-content-search"></a><span data-ttu-id="c8a98-147">Проверка количества исходных почтовых ящиков в запросе на поиск содержимого</span><span class="sxs-lookup"><span data-stu-id="c8a98-147">Verify the number of source mailboxes in the Content Search</span></span>

<span data-ttu-id="c8a98-p109">Поиск контента возвращает не более 1 000 почтовых ящиков источника, содержащих результаты поиска. При наличии более 1000 почтовых ящиков, которые содержат контента, отвечающей поисковому запросу, только в начало 1 000 почтовых ящиков с большинства результатов поиска включаются в поиск содержимого, созданной на предыдущем шаге. Поэтому если более 1000 почтовых ящиков содержит результаты поиска, некоторые из этих почтовых ящиков не включены в список исходных почтовых ящиков скопирован в новый поиск обнаружения электронных данных на месте, созданные в шаге 3.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p109">A Content Search returns a maximum of 1,000 source mailboxes that contain search results. If there are more than 1,000 mailboxes that contain content that matches the search query, only the top 1,000 mailboxes with the most search results are included in the Content Search that you created in the previous step. So if more than 1,000 mailboxes contain search results, some of those mailboxes won't be included in the list of source mailboxes copied to the new In-Place eDiscovery search created in Step 3.</span></span> 
  
<span data-ttu-id="c8a98-151">Для создания поиска контента с не более 1 000 исходных почтовых ящиков, выполните следующие действия для запуска скрипта, который отображает количество исходных почтовых ящиков (, содержащих результаты поиска), возвращенных в результате поиска контента, созданной на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="c8a98-151">To help you create a Content Search with no more than 1,000 source mailboxes, follow these steps to run a script that displays the number of source mailboxes (that contain search results) returned by the Content Search you created in Step 1.</span></span> 
  
1. <span data-ttu-id="c8a98-p110">Сохраните следующий текст в файл сценария PowerShell с помощью суффикса имени файла .ps1. Например, можно сохранить в файл с именем `SourceMailboxes.ps1`.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p110">Save the following text to a PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `SourceMailboxes.ps1`.</span></span>
    
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

2. <span data-ttu-id="c8a98-154">В безопасности и соответствия требованиям центр PowerShell перейдите к папке, где находится сценарий, созданный на предыдущем шаге и запустите сценарий; Например:</span><span class="sxs-lookup"><span data-stu-id="c8a98-154">In Security & Compliance Center PowerShell, go to the folder where the script you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\SourceMailboxes.ps1
    ```

3. <span data-ttu-id="c8a98-155">Когда вам это будет предложено, введите имя запроса на поиск содержимого, созданного на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="c8a98-155">When prompted by the script, type the name of the Content Search that you created in Step 1.</span></span>
    
    <span data-ttu-id="c8a98-156">Сценарий отобразит количество исходных почтовых ящиков, которые содержат результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-156">The script displays the number of source mailboxes that contain search results.</span></span>
    
<span data-ttu-id="c8a98-p111">При наличии более 1000 исходных почтовых ящиков, попробуйте создать два (или более) контента поиска. К примеру поиск половину почтовых ящиков вашей организации в один поиска контента и вторая в другой поиска контента. Можно также изменить критерии поиска, чтобы уменьшить количество почтовых ящиков, которые содержат результатов поиска. Например может включать диапазон дат или уточнения запроса ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p111">If there are more than 1,000 source mailboxes, try creating two (or more) Content Searches. For example, search half of your organization's mailboxes in one Content Search and the other half in another Content Search. You could also change the search criteria to reduce the number of mailboxes that contain search results. For example, you could include a date range or refine the keyword query.</span></span>
  
## <a name="step-2-connect-to-the-security-amp-compliance-center-and-exchange-online-in-a-single-remote-powershell-session"></a><span data-ttu-id="c8a98-161">Шаг 2: Подключение к безопасности &amp; центре соответствия требованиям и Exchange Online в одном удаленного сеанса PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8a98-161">Step 2: Connect to the Security &amp; Compliance Center and Exchange Online in a single remote PowerShell session</span></span>

<span data-ttu-id="c8a98-p112">Следующим шагом является подключение Windows PowerShell для обоих безопасности &amp; центре соответствия требованиям и организацию Exchange Online. Это необходимо, так как для сценариев, которые выполняются на шаге 3 требуется доступ к командлетам поиска контента в системы &amp; центре соответствия требованиям и командлеты обнаружения электронных данных на месте в Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p112">The next step is to connect Windows PowerShell to both the Security &amp; Compliance Center and to your Exchange Online organization. This is necessary because the script that you run in Step 3 requires access to the Content Search cmdlets in the Security &amp; Compliance Center and the In-Place eDiscovery cmdlets in Exchange Online.</span></span>
  
1. <span data-ttu-id="c8a98-p113">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1. Например, можно сохранить в файл с именем `ConnectEXO-CC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1. For example, you could save it to a file named `ConnectEXO-CC.ps1`.</span></span>
    
    ```
    $UserCredential = Get-Credential
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -DisableNameChecking
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
    Import-PSSession $Session -AllowClobber -DisableNameChecking
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Exchange Online + Compliance Center)"
    ```

2. <span data-ttu-id="c8a98-166">На локальном компьютере откройте Windows PowerShell, перейдите к папке, где находится сценарий, созданный на предыдущем шаге и затем запустите сценарий; Например:</span><span class="sxs-lookup"><span data-stu-id="c8a98-166">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectEXO-CC.ps1
    ```

<span data-ttu-id="c8a98-p114">Как узнать, если это работает? После запуска сценария командлеты из безопасности &amp; центре соответствия требованиям и Exchange Online могут быть импортированы в локальный сеанс PowerShell. Если сообщений об ошибках нет, то подключение успешно. Быстрой проверки должна выполняться безопасности &amp; центре соответствия требованиям командлета —, например **Install-UnifiedCompliancePrerequisite** — и Exchange Online командлета, таких как **Get-Mailbox**.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p114">How do you know if this worked? After you run the script, cmdlets from the Security &amp; Compliance Center and Exchange Online are imported into your local PowerShell session. If you don't receive any errors, you connected successfully. A quick test is to run a Security &amp; Compliance Center cmdlet—for example, **Install-UnifiedCompliancePrerequisite** —and an Exchange Online cmdlet, such as **Get-Mailbox**.</span></span> 
  
## <a name="step-3-run-the-script-to-create-an-in-place-ediscovery-search-from-the-content-search"></a><span data-ttu-id="c8a98-171">Шаг 3. Запуск сценария для создания запроса на обнаружение электронных данных на месте, в основе которого лежит поиск содержимого</span><span class="sxs-lookup"><span data-stu-id="c8a98-171">Step 3: Run the script to create an In-Place eDiscovery search from the Content Search</span></span>

<span data-ttu-id="c8a98-p115">После создания двух сеанс PowerShell на шаге 2, следующим шагом является выполнение скрипта, который преобразует существующего контента поиска для поиска методом электронного обнаружения на месте. Вот что означает скрипта:</span><span class="sxs-lookup"><span data-stu-id="c8a98-p115">After you create the dual PowerShell session in Step 2, the next step is to run a script that will convert an existing Content Search to an In-Place eDiscovery search. Here's what the script does:</span></span>
  
- <span data-ttu-id="c8a98-174">Запрашивает имя запроса на поиск содержимого, который требуется преобразовать.</span><span class="sxs-lookup"><span data-stu-id="c8a98-174">Prompts you for the name of the Content Search to convert.</span></span>
    
- <span data-ttu-id="c8a98-p116">Проверяет, завершен ли поиск содержимого. Если ничего не найдено, запрос на обнаружение электронных данных на месте не будет создан.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p116">Verifies that the Content Search has completed running. If the Content Search doesn't return any results, and In-Place eDiscovery won't be created.</span></span>
    
- <span data-ttu-id="c8a98-177">Сохраняет в переменной список тех исходных почтовых ящиков из запроса на поиск содержимого, которые содержат результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-177">Saves a list of the source mailboxes from the Content Search that contain search results to a variable.</span></span>
    
- <span data-ttu-id="c8a98-p117">Создает поиск с обнаружением электронных данных на месте с указанными ниже свойствами. Обратите внимание, что новый поиск не запускается. Он запускается на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p117">Creates a new In-Place eDiscovery search, with the following properties. Note that the new search isn't started. You'll start it in step 4.</span></span>
    
  - <span data-ttu-id="c8a98-p118">**Имя** — имя нового поиска используется в этом формате: \<имя поиска контента\>_MBSearch1. Если снова запустить сценарий и использовать тот же источник контента поиска с именем поиска \<имя поиска контента\>_MBSearch2.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p118">**Name** - The name of the new search uses this format: \<Name of Content Search\>_MBSearch1. If you run the script again and use the same source Content Search, the search will be named \<Name of Content Search\>_MBSearch2.</span></span>
    
  - <span data-ttu-id="c8a98-183">**Исходные почтовые ящики** - всех почтовых ящиков из поиска контента, содержащих результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-183">**Source mailboxes** - All mailboxes from the Content Search that contain search results.</span></span> 
    
  - <span data-ttu-id="c8a98-p119">**Поисковый запрос** - новый поиск с помощью запросов поиска из поиска контента. Если содержимое поиска включает в себя весь контент (где запросов поиска не заполнено) новый поиск также будет иметь пустой поискового запроса и будет включать все содержимое, обнаруженных в исходных почтовых ящиков.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p119">**Search query** - The new search uses the search query from the Content Search. If the Content Search includes all content (where the search query is blank) the new search will also have a blank search query and will include all content found in the source mailboxes.</span></span> 
    
  - <span data-ttu-id="c8a98-p120">**Оценка только поиска** - новый поиск отмечен как только для оценки поиска. Он не будет копирование результатов поиска в почтовый ящик обнаружения после его запуска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p120">**Estimate only search** - The new search is marked as an estimate-only search. It won't copy search results to a discovery mailbox after you start it.</span></span> 
    
1. <span data-ttu-id="c8a98-p121">Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла ps1. Например, можно сохранить в файл с именем `CreateMBSearchFromComplianceSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of ps1. For example, you could save it to a file named `CreateMBSearchFromComplianceSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="c8a98-190">Во время сеанса Windows PowerShell, созданный на шаге 2 Перейдите к папке, где находится сценарий, созданный на предыдущем шаге и запустите сценарии; Например:</span><span class="sxs-lookup"><span data-stu-id="c8a98-190">In the Windows PowerShell session that you created in Step 2, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\CreateMBSearchFromComplianceSearch.ps1
    ```

3. <span data-ttu-id="c8a98-191">При появлении запроса с помощью сценария введите имя поиска контента, который требуется преобразовать в поиск обнаружения электронных данных на месте (например, поиска, созданной на шаге 1) и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="c8a98-191">When prompted by the script, type the name of the Content Search that you want to covert to an In-Place eDiscovery search (for example, the search that you created in Step 1), and then press **Enter**.</span></span>
    
    <span data-ttu-id="c8a98-p122">При успешном выполнении сценария создается поиск с обнаружением электронных данных на месте с состоянием **NotStarted**. Выполните команду  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL`, чтобы отобразить свойства нового поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p122">If the script is successful, a new In-Place eDiscovery search is created with a status of **NotStarted**. Run the command  `Get-MailboxSearch <Name of Content Search>_MBSearch1 | FL` to display the properties of the new search.</span></span> 
  
## <a name="step-4-start-the-in-place-ediscovery-search"></a><span data-ttu-id="c8a98-194">Шаг 4. Запуск поиска с обнаружением электронных данных на месте</span><span class="sxs-lookup"><span data-stu-id="c8a98-194">Step 4: Start the In-Place eDiscovery search</span></span>

<span data-ttu-id="c8a98-p123">Сценарий, выполняемый на шаге 3, создает запрос на поиск с обнаружением электронных данных на месте, но не запускает его. Теперь необходимо запустить поиск, чтобы получить оценку его результатов.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p123">The script that you run in Step 3 creates a new In-Place eDiscovery search, but doesn't start it. The next step is to start the search so you can get an estimate of the search results.</span></span>
  
1. <span data-ttu-id="c8a98-197">В центре администрирования Exchange (EAC) перейдите к **разделу Управление соответствием требованиям** \> **In-Place eDiscovery &amp; хранения**.</span><span class="sxs-lookup"><span data-stu-id="c8a98-197">In the Exchange admin center (EAC), go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="c8a98-198">В списке выберите поиск с обнаружением электронных данных на месте, созданный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="c8a98-198">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="c8a98-199">Щелкните **Поиск** ![значок поиска](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **оценки результатов поиска** для запуска службы поиска и возврата оценку общего размера и количества элементов, возвращенных в результате поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-199">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif) \> **Estimate search results** to start the search and return an estimate of the total size and number of items returned by the search.</span></span> 
    
    <span data-ttu-id="c8a98-p124">Оценки отображаются в области сведений. Нажмите кнопку **Обновить** ![значок обновления](media/O365-MDM-Policy-RefreshIcon.gif) обновить сведения, отображаемые в области сведений.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p124">The estimates are displayed in the details pane. Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information displayed in the details pane.</span></span> 
    
4. <span data-ttu-id="c8a98-202">Для предварительного просмотра результатов после завершения поиска нажмите кнопку **Предварительный просмотр результатов поиска** в области сведений.</span><span class="sxs-lookup"><span data-stu-id="c8a98-202">To preview the results after the search is completed, click **Preview search results** in the details pane.</span></span>
  
## <a name="next-steps-after-creating-and-running-the-in-place-ediscovery-search"></a><span data-ttu-id="c8a98-203">Действия после создания и запуска поиска с обнаружением электронных данных на месте</span><span class="sxs-lookup"><span data-stu-id="c8a98-203">Next steps after creating and running the In-Place eDiscovery search</span></span>

<span data-ttu-id="c8a98-204">После создания и запуска поиска с обнаружением электронных данных на месте, который был создан с помощью сценария на шаге 3, можно выполнять различные стандартные действия над результатами поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-204">After you create and start the In-Place eDiscovery search that was created by the script in Step 3, you can use the normal In-Place eDiscovery workflow to perform different eDiscovery actions on the search results.</span></span>
  
### <a name="create-an-in-place-hold"></a><span data-ttu-id="c8a98-205">Создание хранения на месте</span><span class="sxs-lookup"><span data-stu-id="c8a98-205">Create an In-Place Hold</span></span>

1. <span data-ttu-id="c8a98-206">В центре администрирования Exchange перейдите к **разделу Управление соответствием требованиям** \> **In-Place eDiscovery &amp; хранения**.</span><span class="sxs-lookup"><span data-stu-id="c8a98-206">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="c8a98-207">В представлении списка выберите Поиск обнаружения электронных данных на месте, созданной на шаге 3 и нажмите кнопку **Изменить** ![значок Правка](media/O365_MDM_CreatePolicy_EditIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="c8a98-207">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Edit** ![Edit icon](media/O365_MDM_CreatePolicy_EditIcon.gif).</span></span>
    
3. <span data-ttu-id="c8a98-208">На странице **Удержание на месте** установите флажок **Поставить содержимое выбранных почтовых ящиков, соответствующее поисковому запросу, на удержание**, а затем выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="c8a98-208">On the **In-Place Hold** page, select the **Place content matching the search query in selected mailboxes on hold** check box and then select one of the following options:</span></span> 
    
  - <span data-ttu-id="c8a98-p125">**Удержании неопределенное время** — выберите этот параметр, чтобы поместить элементы, возвращенные операцией поиска на неограниченное удержание. До удаления почтового ящика из поиска или удалить поиск элементов на удержании будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p125">**Hold indefinitely** - Choose this option to place items returned by the search on an indefinite hold. Items on hold will be preserved until you remove the mailbox from the search or remove the search.</span></span> 
    
  - <span data-ttu-id="c8a98-p126">**Укажите число дней для хранения элементов, относящиеся к их Дата получения** — выберите этот параметр для хранения элементов в течение определенного периода. Во время выполнения рассчитывается из даты, полученного или созданного элемента почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p126">**Specify number of days to hold items relative to their received date** - Choose this option to hold items for a specific period. The duration is calculated from the date a mailbox item is received or created.</span></span> 
    
4. <span data-ttu-id="c8a98-213">Нажмите кнопку **Сохранить**, чтобы создать запрос на удержание на месте, а затем повторите поиск.</span><span class="sxs-lookup"><span data-stu-id="c8a98-213">Click **Save** to create the In-Place Hold and restart the search.</span></span> 
    
[<span data-ttu-id="c8a98-214">Return to top</span><span class="sxs-lookup"><span data-stu-id="c8a98-214">Return to top</span></span>](use-content-search-in-ediscovery.md#top)
  
### <a name="copy-the-search-results"></a><span data-ttu-id="c8a98-215">Копирование результатов поиска</span><span class="sxs-lookup"><span data-stu-id="c8a98-215">Copy the search results</span></span>

1. <span data-ttu-id="c8a98-216">В центре администрирования Exchange перейдите к **разделу Управление соответствием требованиям** \> **In-Place eDiscovery &amp; хранения**.</span><span class="sxs-lookup"><span data-stu-id="c8a98-216">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="c8a98-217">В списке выберите поиск с обнаружением электронных данных на месте, созданный на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="c8a98-217">In the list view, select the In-Place eDiscovery search that you created in Step 3.</span></span>
    
3. <span data-ttu-id="c8a98-218">Щелкните **Поиск** ![значок поиска](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif)и нажмите кнопку **Копировать результаты поиска** из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="c8a98-218">Click **Search** ![Search icon](media/5f6f9463-50e9-460b-8738-b67e759c2efc.gif), and then click **Copy search results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="c8a98-219">В окне **Копировать результаты поиска** выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="c8a98-219">In **Copy Search Results**, select from the following options:</span></span>
    
    - <span data-ttu-id="c8a98-220">**Включить не включаемые элементы** — установите этот флажок, чтобы включить элементы почтовых ящиков, которые не удалось найти (например, сообщения с вложениями типов файлов, которые невозможно индексировать службой поиска Exchange).</span><span class="sxs-lookup"><span data-stu-id="c8a98-220">**Include unsearchable items** - Select this check box to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search).</span></span> 
    
    - <span data-ttu-id="c8a98-p127">**Включение дедупликация** — установите этот флажок, чтобы исключить повторяющиеся сообщения. Только один экземпляр сообщение будет копировать в почтовый ящик обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p127">**Enable de-duplication** - Select this check box to exclude duplicate messages. Only a single instance of a message will be copied to the discovery mailbox.</span></span> 
    
    - <span data-ttu-id="c8a98-223">**Ведение журнала в полный** — установите этот флажок для включения журнала full сохраняется в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-223">**Enable full logging** - Select this check box to include a full log in search results.</span></span> 
    
    - <span data-ttu-id="c8a98-224">**Отправлять почту после завершения эту копию** — установите этот флажок, чтобы получить уведомление по электронной почте после завершения поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-224">**Send me mail when the copy is completed** - Select this check box to get an email notification when the search is completed.</span></span> 
    
    - <span data-ttu-id="c8a98-225">**Копирование результатов для этого почтового ящика обнаружения** - нажмите кнопку **Обзор** , чтобы выбрать почтового ящика обнаружения, где будут результаты поиска скопирован.</span><span class="sxs-lookup"><span data-stu-id="c8a98-225">**Copy results to this discovery mailbox** - Click **Browse** to select the discovery mailbox where you want the search results copied to.</span></span> 
    
5. <span data-ttu-id="c8a98-226">Нажмите кнопку **Копировать**, чтобы начать процесс копирования результатов поиска в указанный почтовый ящик найденных сообщений.</span><span class="sxs-lookup"><span data-stu-id="c8a98-226">Click **Copy** to start the process to copy the search results to the specified discovery mailbox.</span></span> 
    
6. <span data-ttu-id="c8a98-227">Нажмите кнопку **Обновить** ![значок обновления](media/O365-MDM-Policy-RefreshIcon.gif) для обновления сведений о ходе выполнения копирования, который отображается в области сведений.</span><span class="sxs-lookup"><span data-stu-id="c8a98-227">Click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information about the copying status that is displayed in the details pane.</span></span> 
    
7. <span data-ttu-id="c8a98-228">После завершения копирования нажмите кнопку **Открыть**, чтобы открыть почтовый ящик найденных сообщений для просмотра результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="c8a98-228">When copying is complete, click **Open** to open the discovery mailbox to view the search results.</span></span> 
  
### <a name="export-the-search-results"></a><span data-ttu-id="c8a98-229">Экспорт результатов поиска</span><span class="sxs-lookup"><span data-stu-id="c8a98-229">Export the search results</span></span>

1. <span data-ttu-id="c8a98-230">В центре администрирования Exchange перейдите к **разделу Управление соответствием требованиям** \> **In-Place eDiscovery &amp; хранения**.</span><span class="sxs-lookup"><span data-stu-id="c8a98-230">In the EAC, go to **Compliance management** \> **In-Place eDiscovery &amp; Hold**.</span></span>
    
2. <span data-ttu-id="c8a98-231">В списке выберите запрос на поиск с обнаружением электронных данных на месте, созданный на шаге 3, и нажмите кнопку **Экспорт в PST-файл**.</span><span class="sxs-lookup"><span data-stu-id="c8a98-231">In the list view, select the In-Place eDiscovery search that you created in Step 3, and then click **Export to a PST file**.</span></span>
    
3. <span data-ttu-id="c8a98-232">В окне **Средство экспорта PST обнаружения электронных данных** выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c8a98-232">In the **eDiscovery PST Export Tool** window, do the following:</span></span> 
    
    - <span data-ttu-id="c8a98-233">Нажмите кнопку **Обзор**, чтобы указать, откуда нужно загрузить PST-файл.</span><span class="sxs-lookup"><span data-stu-id="c8a98-233">Click **Browse** to specify the location where you want to download the PST file.</span></span> 
    
    - <span data-ttu-id="c8a98-p128">Установите флажок **Включить дедупликацию**, чтобы исключить повторяющиеся сообщения. В PST-файл будет включен только один экземпляр сообщения.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p128">Click the **Enable deduplication** checkbox to exclude duplicate messages. Only a single instance of a message will be included in the PST file.</span></span> 
    
    - <span data-ttu-id="c8a98-p129">Установите флажок **Включить элементы, недоступные для поиска.**, чтобы добавить недоступные для поиска элементы почтовых ящиков (например, сообщения с вложенными файлами таких типов, которые не могут быть индексированы поиском Exchange). Недоступные для поиска элементы экспортируются в отдельный PST-файл.</span><span class="sxs-lookup"><span data-stu-id="c8a98-p129">Click the **Include unsearchable items** checkbox to include mailbox items that couldn't be searched (for example, messages with attachments of file types that couldn't be indexed by Exchange Search). Unsearchable items are exported to a separate PST file.</span></span> 
    
4. <span data-ttu-id="c8a98-238">Нажмите кнопку **Начать** для экспорта результатов поиска в PST-файл.</span><span class="sxs-lookup"><span data-stu-id="c8a98-238">Click **Start** to export the search results to a PST file.</span></span> 
    
    <span data-ttu-id="c8a98-239">Откроется окно со сведениями о состоянии процесса экспорта.</span><span class="sxs-lookup"><span data-stu-id="c8a98-239">A window is displayed that contains status information about the export process.</span></span>
