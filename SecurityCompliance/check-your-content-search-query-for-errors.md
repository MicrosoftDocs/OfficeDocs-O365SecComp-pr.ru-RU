---
title: Проверка запроса на поиск контента на наличие ошибок
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: Проверка запроса ключевого слова для поиска контента для ошибки и опечатки, такие как неподдерживаемые символы и строчные логические операторы, прежде чем выполнять поиск. Если мы найти ошибку, будет рекомендуется измененный запрос.
ms.openlocfilehash: 0d2119ceef4ce3777d3967a56357551e235e426c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534837"
---
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="f5637-104">Проверка запроса на поиск контента на наличие ошибок</span><span class="sxs-lookup"><span data-stu-id="f5637-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="f5637-p102">При создании или изменении поиска контента могут иметь Office 365 проверить запрос для неподдерживаемые символы и логические операторы, которые не могут иметь разное. Каким образом? Только что нажмите кнопку **Проверить запрос опечаток** на странице запрос поиска контента.</span><span class="sxs-lookup"><span data-stu-id="f5637-p102">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized. How? Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
![Нажмите кнопку «Автоматически проверять запроса опечаток» Проверка запроса поиска для неподдерживаемые символы](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="f5637-p103">Ниже приведен список неподдерживаемые символы, проверки. Неподдерживаемые символы часто скрыты, и они обычно приводит к ошибке поиска или возвращать непредвиденные результаты.</span><span class="sxs-lookup"><span data-stu-id="f5637-p103">Here's a list of the unsupported characters that we check for. Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="f5637-p104">**Смарт-кавычки** - смарт-одиночные и двойные кавычки (также называемая парные кавычки) не поддерживаются. Можно использовать только прямые кавычки в поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="f5637-p104">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported. Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="f5637-p105">**Символы не печати и элемента управления** - без печати и управления символы не представляют написанного символов, таких как буквенно цифровых символов. Примеры управляющие и управления символы включают символы форматирования текста или отдельных строк текста.</span><span class="sxs-lookup"><span data-stu-id="f5637-p105">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character. Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="f5637-115">**Слева направо и справа налево метки** - это управляющие символы, служит для указания направление текста справа налево (например, английский и испанский) и языкам для письма справа налево (например, арабского языка и иврита).</span><span class="sxs-lookup"><span data-stu-id="f5637-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="f5637-p106">**Строчная логических операторов** - при использовании логический оператор, например **и**, **или**и **не** в поисковый запрос, он должен быть верхнего регистра. Мы проверить запрос опечаток, синтаксис запроса часто указывается, что несмотря на то, что может использоваться строчная операторы; используется логический оператор например `(WordA or WordB) and (WordC or WordD)`.</span><span class="sxs-lookup"><span data-stu-id="f5637-p106">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase. When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="f5637-118">Что произойдет, если запрос имеет неподдерживаемый символ?</span><span class="sxs-lookup"><span data-stu-id="f5637-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="f5637-p107">Если неподдерживаемые символы находятся в запросе, отображается предупреждение, что неподдерживаемые символы, которые были найдены и предлагает альтернативы. Затем выберите имеется возможность сохранить исходного запроса или замените предложенного измененный запрос. Ниже приведен пример предупреждающее сообщение, которое отображается после нажатия кнопки **Проверить запрос опечаток** для поискового запроса на предыдущем рисунке. Обратите внимание, что исходный запрос содержит парные кавычки и строчных логических операторов.</span><span class="sxs-lookup"><span data-stu-id="f5637-p107">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative. Then you then have the option keep the original query or replace it with the suggested revised query. Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot. Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![Предупреждение отображается с предлагаемые исправления для запроса](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="f5637-124">Предотвращение неподдерживаемые символы в поисковых запросов</span><span class="sxs-lookup"><span data-stu-id="f5637-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="f5637-p108">Неподдерживаемые символы обычно добавляются в запрос при копировании части запроса и запроса из других приложений (например, Microsoft Word или Microsoft Excel) и копировать их в поле ключевых слов на странице запрос поиска контента. Лучший способ неподдерживаемые символы не является введите запрос в поле ключевых слов. Кроме того можно копировать запрос из Word или Excel и вставьте его в файл в текстовый редактор, например Блокнот. Затем сохраните текстовый файл и выберите в раскрывающемся списке **Кодировка** **ANSI** . Удаление любого форматирования и неподдерживаемые символы. Затем можно скопируйте и вставьте запроса из текстового файла в окно запроса ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="f5637-p108">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search. The best way to prevent unsupported characters is to just type the query in the keyword box. Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad. Then save the text file and select **ANSI** in the **Encoding** drop-down list. This will remove any formatting and unsupported characters. Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
