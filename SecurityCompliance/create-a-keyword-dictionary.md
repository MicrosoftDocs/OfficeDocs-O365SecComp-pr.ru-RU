---
title: Создание словаря ключевых слов
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: c8a95d1b-c3b6-4613-98ab-0331d1872cf3
description: Для определения конфиденциальной информации иногда требуется искать ключевые слова, в частности, при определении универсального контента (например, коммуникаций в сфере здравоохранения) либо неприемлемой или нецензурной лексики. Списки ключевых слов можно создавать в типах конфиденциальной информации, но размер этих списков ограничен, а для их создания и редактирования требуется модифицировать XML. Словари ключевых слов упрощают управление ключевыми словами и позволяют управлять ими в намного более крупных масштабах — до 100 000 терминов на словарь.
ms.openlocfilehash: 5dd41223cd3ce5ac45614abcc3926bf5e49fbb5a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217379"
---
# <a name="create-a-keyword-dictionary"></a><span data-ttu-id="a72b0-105">Создание словаря ключевых слов</span><span class="sxs-lookup"><span data-stu-id="a72b0-105">Create a keyword dictionary</span></span>

<span data-ttu-id="a72b0-p102">Защита от потери данных (DLP) в Office 365 позволяет определять, отслеживать и защищать конфиденциальную информацию. Для определения конфиденциальной информации иногда требуется искать ключевые слова, в частности, при определении универсального контента (например, коммуникаций в сфере здравоохранения) либо неприемлемой или нецензурной лексики. Списки ключевых слов можно создавать в типах конфиденциальной информации, но размер этих списков ограничен, а для их создания и редактирования требуется модифицировать XML. Словари ключевых слов упрощают управление ключевыми словами и позволяют управлять ими в намного более крупных масштабах — до 100 000 терминов на словарь.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p102">Data loss prevention (DLP) in Office 365 can identify, monitor, and protect your sensitive information. Identifying sensitive information sometimes requires looking for keywords, particularly when identifying generic content (such as healthcare-related communication) or inappropriate or explicit language. While you can create keyword lists in sensitive information types, keyword lists are limited in size and require modifying XML to create or edit them. Keyword dictionaries provide simpler management of keywords and at a much larger scale, supporting up to 100,000 terms per dictionary.</span></span>
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a><span data-ttu-id="a72b0-110">Основные этапы создания словаря ключевых слов</span><span class="sxs-lookup"><span data-stu-id="a72b0-110">Basic steps to creating a keyword dictionary</span></span>

<span data-ttu-id="a72b0-p103">Ключевые слова можно брать из различных источников, наиболее распространенными из которых являются файлы (например, списки в формате CSV или TXT), списки, вводимые непосредственно в командлете, и имеющиеся словари. При создании словаря ключевых слов всегда используются одни и те же основные действия:</span><span class="sxs-lookup"><span data-stu-id="a72b0-p103">The keywords for your dictionary could come from a variety of sources, most commonly from a file (such as a .csv or .txt list), from a list you enter directly in the cmdlet, or from an existing dictionary. When you create a keyword dictionary, you follow the same core steps:</span></span>
  
1. <span data-ttu-id="a72b0-113">**Подключение к интерфейсу PowerShell Центра безопасности и соответствия требованиям** — см. [эту статью](https://docs.microsoft.com/ru-RU/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="a72b0-113">**Connect to Security &amp; Compliance Center PowerShell** - see [this topic](https://docs.microsoft.com/ru-RU/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
    
2. <span data-ttu-id="a72b0-114">**Определение или загрузка ключевых слов из нужного источника** — командлет для создания словаря ключевых слов принимает разделенный запятыми список ключевых слов, поэтому данный этап может слегка меняться в зависимости от источника ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="a72b0-114">**Define or load your keywords from your intended source** - the cmdlet to create a keyword dictionary accepts a comma-separated list of keywords, so this step will vary slightly depending on where your keywords come from.</span></span> 
    
3. <span data-ttu-id="a72b0-115">**Кодирование ключевых слов** — после загрузки они преобразуются в байтовый массив, а затем импортируются.</span><span class="sxs-lookup"><span data-stu-id="a72b0-115">**Encode your keywords** - once loaded, they're converted to a byte array before they're imported.</span></span> 
    
4. <span data-ttu-id="a72b0-116">**Создание словаря** — выберите имя и описание, а затем создайте словарь.</span><span class="sxs-lookup"><span data-stu-id="a72b0-116">**Create your dictionary** - choose a name and description and create your dictionary.</span></span> 
    
## <a name="create-a-keyword-dictionary-from-a-file"></a><span data-ttu-id="a72b0-117">Создание словаря ключевых слов из файла</span><span class="sxs-lookup"><span data-stu-id="a72b0-117">Create a keyword dictionary from a file</span></span>

<span data-ttu-id="a72b0-p104">Как правило, если требуется создать большой словарь, используются ключевые слова из файла или списка, экспортированного из другого источника. В данном случае создается словарь ключевых слов, содержащий список недопустимых слов для фильтрации внешней электронной почты. Для начала необходимо [подключиться к интерфейсу PowerShell Центра безопасности и соответствия требованиям в Office 365](https://docs.microsoft.com/ru-RU/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="a72b0-p104">Often when you need to create a large dictionary, it's to use keywords from a file or a list exported from some other source. In this case, you'll create a keyword dictionary containing a list of inappropriate language to screen in external email. You need to first [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/ru-RU/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
  
1. <span data-ttu-id="a72b0-121">Скопируйте ключевые слова в текстовый файл и убедитесь, что каждое ключевое слово находится на отдельной строке.</span><span class="sxs-lookup"><span data-stu-id="a72b0-121">Copy the keywords into a text file and make sure that each keyword is on a separate line.</span></span>
    
2. <span data-ttu-id="a72b0-p105">Сохраните текст с кодировкой Юникода. В Блокноте выберите пункты **Сохранить как** \> **Кодировка** \> **Юникод**.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p105">Save the text file with Unicode encoding. In Notepad \> **Save As** \> **Encoding** \> **Unicode**.</span></span>
    
3. <span data-ttu-id="a72b0-124">Считайте файл в переменную с помощью следующего командлета:</span><span class="sxs-lookup"><span data-stu-id="a72b0-124">Read the file into a variable by running this cmdlet:</span></span>
    
  ```
  $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
  ```

4. <span data-ttu-id="a72b0-125">Создайте словарь с помощью следующего командлета:</span><span class="sxs-lookup"><span data-stu-id="a72b0-125">Create the dictionary by running this cmdlet:</span></span>
    
  ```
  New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
  ```

## <a name="modifying-an-existing-keyword-dictionary"></a><span data-ttu-id="a72b0-126">Изменение имеющегося словаря ключевых слов</span><span class="sxs-lookup"><span data-stu-id="a72b0-126">Modifying an existing keyword dictionary</span></span>

<span data-ttu-id="a72b0-p106">Вам может потребоваться изменить ключевые слова в одном из словарей или отредактировать один из встроенных словарей. В этом примере мы изменим некоторые термины в PowerShell, сохраним их в локальной среде, где их можно изменить с помощью редактора, а затем обновим имеющиеся термины. Для начала получим объект словаря:</span><span class="sxs-lookup"><span data-stu-id="a72b0-p106">You might need to modify keywords in one of your keyword dictionaries, or modify one of the built-in dictionaries. In this example, we'll modify some terms in PowerShell, save the terms locally where you can modify them in an editor, and then update the previous terms in place. First, retrieve the dictionary object:</span></span>
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="a72b0-p107">По команде `$dict` отображаются различные переменные. Сами ключевые слова хранятся в объекте на фоновом сервере, но переменная `$dict.KeywordDictionary` содержит их строковое представление, которое будет использоваться для редактирования словаря. Прежде чем редактировать словарь, необходимо преобразовать строку терминов обратно в массив с помощью метода `.split(',')`. Затем следует удалить лишние пробелы между ключевыми словами при помощи метода `.trim()`, чтобы в массиве остались только ключевые слова.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p107">Printing  `$dict` will show the various variables. The keywords themselves are stored in an object on the backend, but  `$dict.KeywordDictionary` contains a string representation of them, which you'll use to modify the dictionary. Before you modify the dictionary, you need to turn the string of terms back into an array using the  `.split(',')` method. Then you'll clean up the unwanted spaces between the keywords with the  `.trim()` method, leaving just the keywords to work with.</span></span> 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

<span data-ttu-id="a72b0-p108">Теперь мы удалим некоторые термины из словаря. Так как наш словарь содержит лишь несколько ключевых слов, можно просто перейти к экспорту словаря и его редактированию в Блокноте. Однако словари обычно содержат большое количество текста, поэтому сначала следует научиться редактировать их в PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p108">Now you'll remove some terms from the dictionary. Because the example dictionary has only a few keywords, you could just as easily skip to exporting the dictionary and editing it in Notepad, but dictionaries generally contain a large amount of text, so you'll first learn this way to edit them easily in PowerShell.</span></span>
  
<span data-ttu-id="a72b0-p109">На предыдущем этапе мы сохранили ключевые слова в массив. Существует несколько способов [удаления элементов из массива](https://go.microsoft.com/fwlink/p/?linkid=852620), но для простоты мы создадим массив терминов, которые требуется удалить из словаря, а затем скопируем из словаря только те термины, которых нет в этом списке.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p109">In the last step, you saved the keywords to an array. There are several ways to [remove items from an array](https://go.microsoft.com/fwlink/p/?linkid=852620), but as a straightforward approach, you'll create an array of the terms you want to remove from the dictionary, and then copy only the dictionary terms to it that aren't in the list of terms to remove.</span></span>
  
<span data-ttu-id="a72b0-p110">Выполните команду `$terms`, чтобы вывести текущий список терминов. Выходные данные этой команды выглядят так:</span><span class="sxs-lookup"><span data-stu-id="a72b0-p110">Run the command  `$terms` to show the current list of terms. The output of the command looks like this:</span></span> 
  
```
aarskog's syndrome
abandonment
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipoproteinemia
abiotrophy
ablatio
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

<span data-ttu-id="a72b0-140">Выполните следующую команду, чтобы указать удаляемые элементы:</span><span class="sxs-lookup"><span data-stu-id="a72b0-140">Run this command to specify the terms that you want to remove:</span></span>
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

<span data-ttu-id="a72b0-141">Выполните следующую команду, чтобы фактически удалить термины из списка:</span><span class="sxs-lookup"><span data-stu-id="a72b0-141">Run this command to actually remove the terms from the list:</span></span>
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

<span data-ttu-id="a72b0-p111">Выполните команду `$updatedTerms`, чтобы вывести обновленный список элементов. Выходные данные команды выглядят так (указанные термины были удалены):</span><span class="sxs-lookup"><span data-stu-id="a72b0-p111">Run the command  `$updatedTerms` to show the updated list of terms. The output of the command looks like this (the specified terms have been removed):</span></span> 
  
```
aarskog's syndrome
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipo proteinemia
abiotrophy
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

<span data-ttu-id="a72b0-p112">Теперь сохраните словарь на локальном компьютере и добавьте еще несколько терминов. Вы можете добавить термины непосредственно в PowerShell, но вам по-прежнему потребуется экспортировать файл на локальный компьютер, чтобы убедиться, что он сохранен в кодировке Юникода и содержит BOM.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p112">Now save the dictionary locally and add a few more terms. You could add the terms right here in PowerShell, but you'll still need to export the file locally to ensure it's saved with Unicode encoding and contains the BOM.</span></span>
  
<span data-ttu-id="a72b0-146">Сохраните словарь на локальном компьютере с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="a72b0-146">Save the dictionary locally by running the following:</span></span>
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

<span data-ttu-id="a72b0-p113">Теперь просто откройте файл, добавьте нужные термины и сохраните его в кодировке Юникода (UTF-16). Затем мы отправим обновленные термины и обновим словарь на месте.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p113">Now simply open the file, add your additional terms, and save with Unicode encoding (UTF-16). Now you'll upload the updated terms and update the dictionary in place.</span></span>
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

<span data-ttu-id="a72b0-p114">Теперь словарь был обновлен на месте. Обратите внимание, что поле `Identity` принимает имя словаря. Если требуется изменить имя словаря, можно просто добавить в приведенный выше командлет `set-` параметр `-Name` с новым именем.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p114">Now the dictionary has been updated in place. Note that the  `Identity` field takes the name of the dictionary. If you wanted to also change the name of your dictionary using the  `set-` cmdlet, you would just need to add the  `-Name` parameter to what's above with your new dictionary name.</span></span> 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a><span data-ttu-id="a72b0-152">Использование словарей ключевых слов в типах конфиденциальной информации и политиках защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="a72b0-152">Using keyword dictionaries in custom sensitive information types and DLP policies</span></span>

<span data-ttu-id="a72b0-p115">Словари ключевых слов можно использовать как часть требований к совпадению для пользовательского типа конфиденциальной информации либо как сами типы конфиденциальной информации. В обоих случаях требуется [создать пользовательский тип конфиденциальной информации в PowerShell Центра безопасности и соответствия требованиям Office 365](create-a-custom-sensitive-information-type-in-scc-powershell.md). Чтобы создать тип конфиденциальной информации, следуйте инструкциям из статьи по приведенной ссылке. Когда XML-код будет готов, вам потребуется идентификатор GUID словаря для его использования.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p115">Keyword dictionaries can be used as part of the match requirements for a custom sensitive information type, or as a sensitive information type themselves. Both require [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). Follow the instructions in the linked article to create a sensitive information type. Once you have the XML, you'll need the GUID identifier for the dictionary to use it.</span></span>
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

<span data-ttu-id="a72b0-157">Чтобы получить идентификатор словаря, выполните следующую команду и скопируйте значение свойства **Identity**:</span><span class="sxs-lookup"><span data-stu-id="a72b0-157">To get the identity of your dictionary, run this command and copy the **Identity** property value:</span></span> 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="a72b0-158">Выходные данные команды выглядят так:</span><span class="sxs-lookup"><span data-stu-id="a72b0-158">The output of the command looks like this:</span></span>
  
```
RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255
Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f
Name              : Diseases
Description       : Names of diseases and injuries from ICD-10-CM lexicon
KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo
                    proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,
                    abrami's disease, abramo
IsValid           : True
ObjectState       : Unchanged
```

<span data-ttu-id="a72b0-p116">Вставьте идентификатор в XML-код вашего типа конфиденциальной информации и отправьте код. Словарь появится в списке типов конфиденциальной информации, и вы сможете использовать его непосредственно в политике, указав, сколько ключевых слов требуется для совпадения.</span><span class="sxs-lookup"><span data-stu-id="a72b0-p116">Paste the identity into your custom sensitive information type's XML and upload it. Now your dictionary will appear in your list of sensitive information types and you can use it right in your policy, specifying how many keywords are required to match.</span></span>
  
```
<Entity id="d333c6c2-5f4c-4131-9433-db3ef72a89e8" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f" />
      </Pattern>
    </Entity>
    <LocalizedStrings>
      <Resource idRef="d333c6c2-5f4c-4131-9433-db3ef72a89e8">
        <Name default="true" langcode="en-us">Diseases</Name>
        <Description default="true" langcode="en-us">Detects various diseases</Description>
      </Resource>
    </LocalizedStrings>
```


