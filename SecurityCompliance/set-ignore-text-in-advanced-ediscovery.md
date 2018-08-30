---
title: Настройка параметра "Игнорировать текст" для анализа в Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Узнайте, как определить правило игнорировать определенного текста при использовании модулей процесс и анализ в Office 365 расширенного обнаружения электронных данных.  '
ms.openlocfilehash: eb7e7052979087b7dba98aac3b0c9ab75ec0d02a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534890"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="adb99-103">Настройка параметра "Игнорировать текст" для анализа в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="adb99-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="adb99-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="adb99-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="adb99-p102">Компонент игнорировать текст может применяться к полностью или любой из следующих модулей расширенной обнаружения электронных данных: анализ (рядом с-дубликаты, потоки электронной почты, тем) и релевантности. Игнорируемыми текст не отображается в файлах, отображаемых в релевантности и анализа/расчетов удалит игнорируемыми текста.</span><span class="sxs-lookup"><span data-stu-id="adb99-p102">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance. Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="adb99-p103">Если компонент игнорировать текст ранее был определен для модулей, которые уже выполнена, параметр Игнорировать текст теперь быть защищены от изменения. Тем не менее функцию игнорировать текст для модуля релевантности по-прежнему могут изменяться в любое время.</span><span class="sxs-lookup"><span data-stu-id="adb99-p103">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified. However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="adb99-110">Применение фильтров игнорировать текста</span><span class="sxs-lookup"><span data-stu-id="adb99-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="adb99-p104">Несколько фильтров игнорировать текст, применяются в том порядке, в том, что они были введены. Для изменения порядка, в котором они применяются, они должен быть удален и повторно введен в установленном порядке.</span><span class="sxs-lookup"><span data-stu-id="adb99-p104">Multiple Ignore Text filters are applied in the order that they were entered. To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="adb99-113">Например, если текстовое содержимое: «ДЕЙВ BOB АЛИСЫ CAROL НОЧЬ», далее представлены примеры записей игнорировать текст и результаты:</span><span class="sxs-lookup"><span data-stu-id="adb99-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="adb99-114">**Пропуск записи текста**</span><span class="sxs-lookup"><span data-stu-id="adb99-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="adb99-115">**Результаты**</span><span class="sxs-lookup"><span data-stu-id="adb99-115">**Results**</span></span> <br/> |
|<span data-ttu-id="adb99-116">«МАРИЯ», «БОБ CAROL»</span><span class="sxs-lookup"><span data-stu-id="adb99-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="adb99-117">«ДЕЙВ НОЧЬ»</span><span class="sxs-lookup"><span data-stu-id="adb99-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="adb99-118">«МАРИЯ», «BOB АЛИСЫ CAROL»</span><span class="sxs-lookup"><span data-stu-id="adb99-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="adb99-119">«ДЕЙВ BOB CAROL НОЧЬ»</span><span class="sxs-lookup"><span data-stu-id="adb99-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="adb99-120">Второй ввода игнорировать текста не реализованы, так как строка не найден таким образом после применения первого текста игнорировать.</span><span class="sxs-lookup"><span data-stu-id="adb99-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="adb99-121">Использование регулярных выражений при определении игнорировать текста</span><span class="sxs-lookup"><span data-stu-id="adb99-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="adb99-p105">Регулярные выражения поддерживаются для использования при определении игнорировать текст. Ниже приведены примеры синтаксиса регулярных выражений и об использовании:</span><span class="sxs-lookup"><span data-stu-id="adb99-p105">Regular expressions are supported for use when defining Ignore Text. The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="adb99-124">Чтобы удалить (игнорировать) текст от начала до конца строки:</span><span class="sxs-lookup"><span data-stu-id="adb99-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="adb99-125">где «Начало» — это начальное появления этой строки в строке.</span><span class="sxs-lookup"><span data-stu-id="adb99-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="adb99-126">Например, следующий текст:</span><span class="sxs-lookup"><span data-stu-id="adb99-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="adb99-127">**«Это первое предложение и первая строка**</span><span class="sxs-lookup"><span data-stu-id="adb99-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="adb99-128">**Это второй предложение и второй строке»**</span><span class="sxs-lookup"><span data-stu-id="adb99-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="adb99-129">Регулярное выражение first(.\*) $ приведет к:</span><span class="sxs-lookup"><span data-stu-id="adb99-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="adb99-130">**«Это**</span><span class="sxs-lookup"><span data-stu-id="adb99-130">**"This is**</span></span>
    
    <span data-ttu-id="adb99-131">**Это второй предложение и второй строке»**</span><span class="sxs-lookup"><span data-stu-id="adb99-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="adb99-132">Чтобы удалить заявления об отказе и Правовая информация, автоматически вставляется в конце потоков электронной почты:</span><span class="sxs-lookup"><span data-stu-id="adb99-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="adb99-133">где «Начало» и «End» имеют уникальные строки в начале и конца абзаца текст с переносами.</span><span class="sxs-lookup"><span data-stu-id="adb99-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="adb99-134">Например заявления об отказе и Правовая информация, которые были в потоке электронной почты между строк начала и окончания, будут удалены следующее регулярное выражение:</span><span class="sxs-lookup"><span data-stu-id="adb99-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="adb99-135">**Это сообщение содержит конфиденциальные сведения (. | \s)\*Если проверка необходима запросите бумажных копий версии**</span><span class="sxs-lookup"><span data-stu-id="adb99-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="adb99-136">Чтобы удалить заявление об отказе (в том числе специальные символы):</span><span class="sxs-lookup"><span data-stu-id="adb99-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="adb99-137">Например, следующий текст (с заявление об отказе, представленные здесь, передавая):</span><span class="sxs-lookup"><span data-stu-id="adb99-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="adb99-138">**/\*\ Сообщение содержит конфиденциальные сведения. xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="adb99-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="adb99-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="adb99-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="adb99-140">\**xxxx xxxx, если проверка необходима, запросите версии бумажных копий. /\*\**</span><span class="sxs-lookup"><span data-stu-id="adb99-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="adb99-141">регулярное выражение для удаления выше заявление об отказе должно быть:</span><span class="sxs-lookup"><span data-stu-id="adb99-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="adb99-142">**\/\\*\\Это сообщение содержит конфиденциальные сведения\.(. | \s)\* Если проверка необходима запросите бумажных копий версии\.\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="adb99-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="adb99-143">Регулярных выражений правила:</span><span class="sxs-lookup"><span data-stu-id="adb99-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="adb99-144">Все символы, не являющихся частью алфавита за исключением пространства, «_» и «-» должен предшествовать "\".</span><span class="sxs-lookup"><span data-stu-id="adb99-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="adb99-145">Поле регулярных eExpression может иметь длину не ограничен.</span><span class="sxs-lookup"><span data-stu-id="adb99-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="adb99-146">Описание и подробный синтаксис регулярных выражений, в разделе: [Язык регулярных выражений - краткий справочник по](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="adb99-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="adb99-147">Определение правила игнорировать текста</span><span class="sxs-lookup"><span data-stu-id="adb99-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="adb99-148">В **Управление \> анализ \> анализ параметры** вкладке в разделе **Игнорировать текст** **+** значок, чтобы добавить правило.</span><span class="sxs-lookup"><span data-stu-id="adb99-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="adb99-149">В диалоговом окне **Добавить игнорировать текст** в поле **имя** введите имя для правила игнорировать текст.</span><span class="sxs-lookup"><span data-stu-id="adb99-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![Добавление текста, который нужно игнорировать](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="adb99-p106">В **текстовом** поле введите текст, который будет игнорироваться. Текстовое поле позволяет неограниченное число символов.</span><span class="sxs-lookup"><span data-stu-id="adb99-p106">In the **Text** box, type the text to be ignored. The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="adb99-153">Как показано в приведенном выше окне, нажмите кнопку **кратковременное расширение light** , чтобы просмотреть общие рекомендации по синтаксис правила игнорировать текст.</span><span class="sxs-lookup"><span data-stu-id="adb99-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="adb99-154">Установите флажок **регистр** , если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="adb99-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="adb99-155">В списке **Применить к** выберите модули расширенных eDiscovery применения определение.</span><span class="sxs-lookup"><span data-stu-id="adb99-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="adb99-p107">Если необходимо, чтобы тест на образец текста, введите образец текста в поле **ввода** и нажмите кнопку **Проверить**. Результаты отображаются в текстовом поле **выходных данных** .</span><span class="sxs-lookup"><span data-stu-id="adb99-p107">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**. The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="adb99-p108">Нажмите **кнопку ОК** , чтобы сохранить правило игнорировать текст. Отображается определенный правило игнорировать текст.</span><span class="sxs-lookup"><span data-stu-id="adb99-p108">Click **OK** to save the Ignore Text rule. The defined Ignore Text rule is displayed.</span></span> 
    
    ![Указание имени для игнорируемого текста](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="adb99-161">См. также</span><span class="sxs-lookup"><span data-stu-id="adb99-161">See also</span></span>

[<span data-ttu-id="adb99-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="adb99-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="adb99-163">Общие сведения о документе подобия</span><span class="sxs-lookup"><span data-stu-id="adb99-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="adb99-164">Настройка параметров анализа</span><span class="sxs-lookup"><span data-stu-id="adb99-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="adb99-165">Анализ параметр Дополнительные параметры</span><span class="sxs-lookup"><span data-stu-id="adb99-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="adb99-166">Просмотр результатов анализа</span><span class="sxs-lookup"><span data-stu-id="adb99-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

