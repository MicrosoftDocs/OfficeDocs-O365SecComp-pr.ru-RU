---
title: Национальный ЕС идентификационный номер
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных ЕС национальный идентификационный номер. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534788"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="00edf-104">Национальный ЕС идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-104">EU National Identification Number</span></span>

<span data-ttu-id="00edf-p102">В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных ЕС национальный идентификационный номер. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="00edf-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="00edf-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="00edf-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="00edf-108">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-108">Format</span></span>

<span data-ttu-id="00edf-109">Сочетание 24 знаков буквы, цифры и специальные символы</span><span class="sxs-lookup"><span data-stu-id="00edf-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-110">Pattern</span></span>

<span data-ttu-id="00edf-111">24 символов:</span><span class="sxs-lookup"><span data-stu-id="00edf-111">24 characters:</span></span>
  
-  <span data-ttu-id="00edf-112">22 букв (без учета регистра), цифр, обратной косой черты, прямая косая черта и "плюс"</span><span class="sxs-lookup"><span data-stu-id="00edf-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="00edf-113">(Без учета регистра) две буквы, цифры, обратной косой черты, пересылать косая черта, плюс или знак равенства</span><span class="sxs-lookup"><span data-stu-id="00edf-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-114">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-114">Checksum</span></span>

<span data-ttu-id="00edf-115">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="00edf-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-116">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-116">Definition</span></span>

<span data-ttu-id="00edf-117">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-118">Регулярное выражение `Regex_austria_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-119">Ключевое слово из `Keywords_austria_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-120">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="00edf-121">Keywords_austria_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="00edf-122">Номер Австрия удостоверений</span><span class="sxs-lookup"><span data-stu-id="00edf-122">austrian identity number</span></span>
  
<span data-ttu-id="00edf-123">Национальный идентификатор номер</span><span class="sxs-lookup"><span data-stu-id="00edf-123">national identity number</span></span>
  
<span data-ttu-id="00edf-124">Количество идентификаторов</span><span class="sxs-lookup"><span data-stu-id="00edf-124">identity number</span></span>
  
<span data-ttu-id="00edf-125">
national id</span><span class="sxs-lookup"><span data-stu-id="00edf-125">national id</span></span>
  
<span data-ttu-id="00edf-126">personalausweis republik österreich</span><span class="sxs-lookup"><span data-stu-id="00edf-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="00edf-127">Бельгия</span><span class="sxs-lookup"><span data-stu-id="00edf-127">Belgium</span></span>

<span data-ttu-id="00edf-128">Для получения дополнительных сведений обратитесь к разделу «Бельгия национальный номер» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="00edf-129">Болгария</span><span class="sxs-lookup"><span data-stu-id="00edf-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="00edf-130">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-130">Format</span></span>

<span data-ttu-id="00edf-131">10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-132">Pattern</span></span>

<span data-ttu-id="00edf-133">10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="00edf-134">Шести цифр, которые соответствуют Дата рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="00edf-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="00edf-135">Две цифры, которые соответствуют порядке рождения</span><span class="sxs-lookup"><span data-stu-id="00edf-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="00edf-136">Одна цифра, соответствующий Пол: четное м и нечетной цифры для женщина</span><span class="sxs-lookup"><span data-stu-id="00edf-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="00edf-137">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="00edf-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-138">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-138">Checksum</span></span>

<span data-ttu-id="00edf-139">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-140">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-140">Definition</span></span>

<span data-ttu-id="00edf-141">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-142">Функция `Func_bulgaria_national_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-143">Ключевое слово из `Keywords_bulgaria_national_number` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="00edf-144">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-145">Функция `Func_bulgaria_national_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-146">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="00edf-147">Keywords_bulgaria_national_number</span><span class="sxs-lookup"><span data-stu-id="00edf-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="00edf-148">egn</span><span class="sxs-lookup"><span data-stu-id="00edf-148">egn</span></span>
  
<span data-ttu-id="00edf-149">egn #</span><span class="sxs-lookup"><span data-stu-id="00edf-149">egn#</span></span>
  
<span data-ttu-id="00edf-150">болгарский национальный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-150">bulgarian national number</span></span>
  
<span data-ttu-id="00edf-151">Национальный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-151">national number</span></span>
  
<span data-ttu-id="00edf-152">social security number
</span><span class="sxs-lookup"><span data-stu-id="00edf-152">social security number</span></span>
  
<span data-ttu-id="00edf-153">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="00edf-153">nationalnumber#</span></span>
  
<span data-ttu-id="00edf-154">SSN #</span><span class="sxs-lookup"><span data-stu-id="00edf-154">ssn#</span></span>
  
<span data-ttu-id="00edf-155">SSN</span><span class="sxs-lookup"><span data-stu-id="00edf-155">ssn</span></span>
  
<span data-ttu-id="00edf-156">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="00edf-156">nationalnumber</span></span>
  
<span data-ttu-id="00edf-157">bnn #</span><span class="sxs-lookup"><span data-stu-id="00edf-157">bnn#</span></span>
  
<span data-ttu-id="00edf-158">bnn</span><span class="sxs-lookup"><span data-stu-id="00edf-158">bnn</span></span>
  
<span data-ttu-id="00edf-159">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-159">personal id number</span></span>
  
<span data-ttu-id="00edf-160">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="00edf-160">personalidnumber#</span></span>
  
<span data-ttu-id="00edf-161">ЕДИНЕН ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="00edf-161">единен граждански номер</span></span>
  
<span data-ttu-id="00edf-162">edinen grazhdanski nomer</span><span class="sxs-lookup"><span data-stu-id="00edf-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="00edf-163">ЕГН</span><span class="sxs-lookup"><span data-stu-id="00edf-163">егн</span></span>
  
<span data-ttu-id="00edf-164">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="00edf-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="00edf-165">Хорватия</span><span class="sxs-lookup"><span data-stu-id="00edf-165">Croatia</span></span>

<span data-ttu-id="00edf-166">Для получения дополнительных сведений обратитесь к разделу «Номер Хорватия удостоверений» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="00edf-167">Кипр</span><span class="sxs-lookup"><span data-stu-id="00edf-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="00edf-168">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-168">Format</span></span>

<span data-ttu-id="00edf-169">10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-170">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-170">Pattern</span></span>

 <span data-ttu-id="00edf-171">10 цифр</span><span class="sxs-lookup"><span data-stu-id="00edf-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="00edf-172">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-172">Checksum</span></span>

<span data-ttu-id="00edf-173">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="00edf-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-174">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-174">Definition</span></span>

<span data-ttu-id="00edf-175">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-176">Регулярное выражение `Regex_cyprus_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-177">Ключевое слово из `Keywords_cyprus_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-178">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="00edf-179">Keywords_cyprus_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="00edf-180">Номер идентификационной карты</span><span class="sxs-lookup"><span data-stu-id="00edf-180">id card number</span></span>
  
<span data-ttu-id="00edf-181">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-181">national identification number</span></span>
  
<span data-ttu-id="00edf-182">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-182">personal id number</span></span>
  
<span data-ttu-id="00edf-183">Номер идентификационной карты</span><span class="sxs-lookup"><span data-stu-id="00edf-183">identity card number</span></span>
  
<span data-ttu-id="00edf-184">ΤΑΥΤΟΤΗΤΑΣ</span><span class="sxs-lookup"><span data-stu-id="00edf-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="00edf-185">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="00edf-185">Czech Republic</span></span>

<span data-ttu-id="00edf-186">Для получения дополнительных сведений обратитесь к разделу «Чешский национальный номер удостоверений» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="00edf-187">Дания</span><span class="sxs-lookup"><span data-stu-id="00edf-187">Denmark</span></span>

<span data-ttu-id="00edf-188">Для получения дополнительных сведений обратитесь к разделу «Дания личный идентификационный номер» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="00edf-189">Эстония</span><span class="sxs-lookup"><span data-stu-id="00edf-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="00edf-190">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-190">Format</span></span>

<span data-ttu-id="00edf-191">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-192">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-192">Pattern</span></span>

<span data-ttu-id="00edf-193">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="00edf-193">11 digits:</span></span>
  
- <span data-ttu-id="00edf-194">Одна цифра, соответствующий пол и века рождения (м четных чисел, четного числа гнездо; 1-2: 19 века; 3-4: 20 века; 5-6: 21 веке)</span><span class="sxs-lookup"><span data-stu-id="00edf-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="00edf-195">Шести цифр, которые соответствуют Дата рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="00edf-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="00edf-196">Три цифры, которые соответствуют серийный номер, отделяя лиц на тот же день рождения</span><span class="sxs-lookup"><span data-stu-id="00edf-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="00edf-197">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="00edf-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-198">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-198">Checksum</span></span>

<span data-ttu-id="00edf-199">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-200">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-200">Definition</span></span>

<span data-ttu-id="00edf-201">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-202">Функция `Func_estonia_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-203">Ключевое слово из `Keywords_estonia_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-204">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-205">Функция `Func_estonia_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-206">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="00edf-207">Keywords_estonia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="00edf-208">персональный идентификационный код</span><span class="sxs-lookup"><span data-stu-id="00edf-208">personal identification code</span></span>
  
<span data-ttu-id="00edf-209">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-209">personal identification number</span></span>
  
<span data-ttu-id="00edf-210">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-210">national identification number</span></span>
  
<span data-ttu-id="00edf-211">Национальный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-211">national number</span></span>
  
<span data-ttu-id="00edf-212">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-212">personal id number</span></span>
  
<span data-ttu-id="00edf-213">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="00edf-213">personalidnumber#</span></span>
  
<span data-ttu-id="00edf-214">ОК</span><span class="sxs-lookup"><span data-stu-id="00edf-214">ik</span></span>
  
<span data-ttu-id="00edf-215">isikukood</span><span class="sxs-lookup"><span data-stu-id="00edf-215">isikukood</span></span>
  
<span data-ttu-id="00edf-216">Идентификатор kaart</span><span class="sxs-lookup"><span data-stu-id="00edf-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="00edf-217">Финляндия</span><span class="sxs-lookup"><span data-stu-id="00edf-217">Finland</span></span>

<span data-ttu-id="00edf-218">Для получения дополнительных сведений обратитесь к разделу «Национальный идентификатор для Финляндии» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="00edf-219">Франция</span><span class="sxs-lookup"><span data-stu-id="00edf-219">France</span></span>

<span data-ttu-id="00edf-220">Для получения дополнительных сведений обратитесь к разделу «Франция национальной ИДЕНТИФИКАЦИОННОЙ карты (CNI)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="00edf-221">Германия</span><span class="sxs-lookup"><span data-stu-id="00edf-221">Germany</span></span>

<span data-ttu-id="00edf-222">Для получения дополнительных сведений обратитесь к разделу «Номер идентификационной карты для Германии» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="00edf-223">Греция</span><span class="sxs-lookup"><span data-stu-id="00edf-223">Greece</span></span>

<span data-ttu-id="00edf-224">Для получения дополнительных сведений обратитесь к разделу «Греция национальной ИДЕНТИФИКАЦИОННОЙ карты» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="00edf-225">Венгрия</span><span class="sxs-lookup"><span data-stu-id="00edf-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="00edf-226">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-226">Format</span></span>

<span data-ttu-id="00edf-227">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="00edf-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-228">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-228">Pattern</span></span>

<span data-ttu-id="00edf-229">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="00edf-229">11 digits:</span></span>
  
-  <span data-ttu-id="00edf-230">Одна цифра, соответствующий Пол (1-м, 2-женщина, другие номера можно также использовать для жителей рождения перед 1900 или жителей с двойной Гражданская позиция)</span><span class="sxs-lookup"><span data-stu-id="00edf-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="00edf-231">Шести цифр, которые соответствуют Дата рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="00edf-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="00edf-232">Три цифры, которые соответствуют серийный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="00edf-233">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="00edf-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-234">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-234">Checksum</span></span>

<span data-ttu-id="00edf-235">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-236">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-236">Definition</span></span>

<span data-ttu-id="00edf-237">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-238">Функция `Func_hungary_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-239">Ключевое слово из `Keywords_hungary_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-240">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-241">Функция `Func_hungary_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-242">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="00edf-243">Keywords_hungary_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="00edf-244">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-244">personal identification number</span></span>
  
<span data-ttu-id="00edf-245">identification number
</span><span class="sxs-lookup"><span data-stu-id="00edf-245">identification number</span></span>
  
<span data-ttu-id="00edf-246">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-246">personal id number</span></span>
  
<span data-ttu-id="00edf-247">személyazonosító igazolvány</span><span class="sxs-lookup"><span data-stu-id="00edf-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="00edf-248">Ireland</span><span class="sxs-lookup"><span data-stu-id="00edf-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="00edf-249">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-249">Format</span></span>

<span data-ttu-id="00edf-250">Сочетание девяти символ буквы, цифры и места в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="00edf-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-251">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-251">Pattern</span></span>

<span data-ttu-id="00edf-252">Сочетание девяти символ буквы, цифры и места в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="00edf-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="00edf-253">От 01 января 2013 г сейчас:</span><span class="sxs-lookup"><span data-stu-id="00edf-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="00edf-254">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="00edf-254">Seven digits</span></span> 
    
- <span data-ttu-id="00edf-255">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="00edf-255">One check digit</span></span>
    
- <span data-ttu-id="00edf-256">Один пробел или прописная буква «W» (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="00edf-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="00edf-257">Перед 01 января 2013 г.:</span><span class="sxs-lookup"><span data-stu-id="00edf-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="00edf-258">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="00edf-258">Seven digits</span></span> 
    
- <span data-ttu-id="00edf-259">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="00edf-259">One check digit</span></span>
    
- <span data-ttu-id="00edf-260">Один пробел или прописные буквы (регистр)</span><span class="sxs-lookup"><span data-stu-id="00edf-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-261">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-261">Checksum</span></span>

<span data-ttu-id="00edf-262">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-263">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-263">Definition</span></span>

<span data-ttu-id="00edf-264">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-265">Функция находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="00edf-266">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="00edf-266">A keyword from is found.</span></span>
    
<span data-ttu-id="00edf-267">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-268">Функция находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-268">The function finds content that matches the pattern.</span></span>
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-269">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="00edf-270">Keywords_ireland_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="00edf-271">число личных общего пользования</span><span class="sxs-lookup"><span data-stu-id="00edf-271">personal public service number</span></span>
  
<span data-ttu-id="00edf-272">PPS нет</span><span class="sxs-lookup"><span data-stu-id="00edf-272">pps no</span></span>
  
<span data-ttu-id="00edf-273">Номер карты социального страхования и доходы</span><span class="sxs-lookup"><span data-stu-id="00edf-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="00edf-274">rsi нет</span><span class="sxs-lookup"><span data-stu-id="00edf-274">rsi no</span></span>
  
<span data-ttu-id="00edf-275">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-275">personal identification number</span></span>
  
<span data-ttu-id="00edf-276">identification number
</span><span class="sxs-lookup"><span data-stu-id="00edf-276">identification number</span></span>
  
<span data-ttu-id="00edf-277">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-277">personal id number</span></span>
  
<span data-ttu-id="00edf-278">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="00edf-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="00edf-p103">uimh. PSP</span><span class="sxs-lookup"><span data-stu-id="00edf-p103">uimh. psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="00edf-281">Италия</span><span class="sxs-lookup"><span data-stu-id="00edf-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="00edf-282">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-282">Format</span></span>

<span data-ttu-id="00edf-283">16 символов комбинацию букв или цифр в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="00edf-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-284">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-284">Pattern</span></span>

<span data-ttu-id="00edf-285">16 символов комбинацию букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="00edf-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="00edf-286">Три буквы, которые соответствуют первым трем согласных в поле имя семейства</span><span class="sxs-lookup"><span data-stu-id="00edf-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="00edf-287">Три буквы, которые соответствуют первый, третий и четвертый согласных в поле имя</span><span class="sxs-lookup"><span data-stu-id="00edf-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="00edf-288">Две цифры, которые соответствуют к последнему цифры года рождения</span><span class="sxs-lookup"><span data-stu-id="00edf-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="00edf-289">Одна буква, соответствующий букве за месяц рождения — буквы используются в алфавитном порядке, но используются только буквы A E, H, L, M, P, R, чтобы T (таким образом, января-A и октября является R)</span><span class="sxs-lookup"><span data-stu-id="00edf-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="00edf-290">Две цифры, которые соответствуют день месяца рождения — для различения мужчин и женщин, 40 добавляется в день рождения для женщин</span><span class="sxs-lookup"><span data-stu-id="00edf-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="00edf-291">Четыре цифры, соответствующий код города, относящиеся к государственный орган, где рождения лица (Страна всей коды используются для иностранных)</span><span class="sxs-lookup"><span data-stu-id="00edf-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="00edf-292">Одна цифра возможности</span><span class="sxs-lookup"><span data-stu-id="00edf-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-293">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-293">Checksum</span></span>

<span data-ttu-id="00edf-294">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-295">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-295">Definition</span></span>

<span data-ttu-id="00edf-296">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-297">Функция `Func_italy_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-298">Ключевое слово из `Keywords_italy_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-299">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-300">Функция `Func_italy_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-301">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="00edf-302">Keywords_italy_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="00edf-303">личный код</span><span class="sxs-lookup"><span data-stu-id="00edf-303">personal code</span></span>
  
<span data-ttu-id="00edf-304">личный код</span><span class="sxs-lookup"><span data-stu-id="00edf-304">personal code number</span></span>
  
<span data-ttu-id="00edf-305">число личных сертификатов</span><span class="sxs-lookup"><span data-stu-id="00edf-305">personal certificate number</span></span>
  
<span data-ttu-id="00edf-306">Финансовый код</span><span class="sxs-lookup"><span data-stu-id="00edf-306">fiscal code</span></span>
  
<span data-ttu-id="00edf-307">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="00edf-307">personalcodeno#</span></span>
  
<span data-ttu-id="00edf-308">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-308">personal id number</span></span>
  
<span data-ttu-id="00edf-309">личный код</span><span class="sxs-lookup"><span data-stu-id="00edf-309">personal id code</span></span>
  
<span data-ttu-id="00edf-310">codice personale</span><span class="sxs-lookup"><span data-stu-id="00edf-310">codice personale</span></span>
  
<span data-ttu-id="00edf-311">numero certificato personale</span><span class="sxs-lookup"><span data-stu-id="00edf-311">numero certificato personale</span></span>
  
<span data-ttu-id="00edf-312">numero personale</span><span class="sxs-lookup"><span data-stu-id="00edf-312">numero personale</span></span>
  
<span data-ttu-id="00edf-313">Идентификатор personale numero</span><span class="sxs-lookup"><span data-stu-id="00edf-313">numero id personale</span></span>
  
<span data-ttu-id="00edf-314">Идентификатор personale codice</span><span class="sxs-lookup"><span data-stu-id="00edf-314">codice id personale</span></span>
  
<span data-ttu-id="00edf-315">codice fiscale</span><span class="sxs-lookup"><span data-stu-id="00edf-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="00edf-316">Италия</span><span class="sxs-lookup"><span data-stu-id="00edf-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="00edf-317">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-317">Format</span></span>

<span data-ttu-id="00edf-318">11 разрядов и дефис в указанном формате</span><span class="sxs-lookup"><span data-stu-id="00edf-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-319">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-319">Pattern</span></span>

<span data-ttu-id="00edf-320">11 разрядов и дефис:</span><span class="sxs-lookup"><span data-stu-id="00edf-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="00edf-321">Шести цифр, которые соответствуют Дата рождения (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="00edf-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="00edf-322">дефис;</span><span class="sxs-lookup"><span data-stu-id="00edf-322">A hyphen</span></span>
    
- <span data-ttu-id="00edf-323">Одна цифра, соответствующий века рождения («0» для 19 века, для 20 века «1» и «2» для 21 веке)</span><span class="sxs-lookup"><span data-stu-id="00edf-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="00edf-324">Четыре цифры, случайным образом</span><span class="sxs-lookup"><span data-stu-id="00edf-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-325">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-325">Checksum</span></span>

<span data-ttu-id="00edf-326">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-327">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-327">Definition</span></span>

<span data-ttu-id="00edf-328">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-329">Функция `Func_latvia_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-330">Ключевое слово из `Keywords_latvia_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-331">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-332">Функция `Func_latvia_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-333">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="00edf-334">Keywords_latvia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="00edf-335">личный код</span><span class="sxs-lookup"><span data-stu-id="00edf-335">personal code</span></span>
  
<span data-ttu-id="00edf-336">личный код</span><span class="sxs-lookup"><span data-stu-id="00edf-336">personal code number</span></span>
  
<span data-ttu-id="00edf-337">число личных сертификатов</span><span class="sxs-lookup"><span data-stu-id="00edf-337">personal certificate number</span></span>
  
<span data-ttu-id="00edf-338">personalcodeno #</span><span class="sxs-lookup"><span data-stu-id="00edf-338">personalcodeno#</span></span>
  
<span data-ttu-id="00edf-339">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-339">personal id number</span></span>
  
<span data-ttu-id="00edf-340">личный код</span><span class="sxs-lookup"><span data-stu-id="00edf-340">personal id code</span></span>
  
<span data-ttu-id="00edf-341">действующие лица kods</span><span class="sxs-lookup"><span data-stu-id="00edf-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="00edf-342">Литва</span><span class="sxs-lookup"><span data-stu-id="00edf-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="00edf-343">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-343">Format</span></span>

<span data-ttu-id="00edf-344">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-345">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-345">Pattern</span></span>

<span data-ttu-id="00edf-346">11 знаков без пробелов и разделители:</span><span class="sxs-lookup"><span data-stu-id="00edf-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="00edf-347">Одна цифра, соответствующий века рождения и пол лица</span><span class="sxs-lookup"><span data-stu-id="00edf-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="00edf-348">Шести цифр, которые соответствуют Дата рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="00edf-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="00edf-349">Три цифры, которые соответствуют серийный номер Дата рождения</span><span class="sxs-lookup"><span data-stu-id="00edf-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="00edf-350">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="00edf-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-351">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-351">Checksum</span></span>

<span data-ttu-id="00edf-352">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-353">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-353">Definition</span></span>

<span data-ttu-id="00edf-354">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-355">Функция `Func_lithuania_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-356">Ключевое слово из `Keywords_lithuania_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-357">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-358">Функция `Func_lithuania_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-359">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="00edf-360">Keywords_lithuania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="00edf-361">личный цифровой код</span><span class="sxs-lookup"><span data-stu-id="00edf-361">personal numeric code</span></span>
  
<span data-ttu-id="00edf-362">Уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-362">unique identification number</span></span>
  
<span data-ttu-id="00edf-363">номер службы граждан</span><span class="sxs-lookup"><span data-stu-id="00edf-363">citizen service number</span></span>
  
<span data-ttu-id="00edf-364">количество уникальных идентификаторов</span><span class="sxs-lookup"><span data-stu-id="00edf-364">unique identity number</span></span>
  
<span data-ttu-id="00edf-365">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="00edf-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="00edf-366">личный код.</span><span class="sxs-lookup"><span data-stu-id="00edf-366">personal code.</span></span>
  
<span data-ttu-id="00edf-367">asmeninis skaitmeninis kodas</span><span class="sxs-lookup"><span data-stu-id="00edf-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="00edf-368">unikalus identifikavimo numeris</span><span class="sxs-lookup"><span data-stu-id="00edf-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="00edf-369">piliečio paslaugos numeris</span><span class="sxs-lookup"><span data-stu-id="00edf-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="00edf-370">unikalus identifikavimo kodas</span><span class="sxs-lookup"><span data-stu-id="00edf-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="00edf-371">asmens kodas.</span><span class="sxs-lookup"><span data-stu-id="00edf-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="00edf-372">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="00edf-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="00edf-373">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-373">Format</span></span>

<span data-ttu-id="00edf-374">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-375">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-375">Pattern</span></span>

<span data-ttu-id="00edf-376">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="00edf-376">11 digits</span></span>
  
- <span data-ttu-id="00edf-377">Одна цифра, соответствующий века рождения и пол лица</span><span class="sxs-lookup"><span data-stu-id="00edf-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="00edf-378">Шести цифр, которые соответствуют Дата рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="00edf-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="00edf-379">Три цифры, которые соответствуют серийный номер Дата рождения</span><span class="sxs-lookup"><span data-stu-id="00edf-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="00edf-380">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="00edf-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-381">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-381">Checksum</span></span>

<span data-ttu-id="00edf-382">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="00edf-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-383">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-383">Definition</span></span>

<span data-ttu-id="00edf-384">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-385">Регулярное выражение `Regex_luxemburg_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-386">Ключевое слово из `Keywords_luxemburg_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-387">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="00edf-388">Keywords_luxemburg_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="00edf-389">личный код</span><span class="sxs-lookup"><span data-stu-id="00edf-389">personal id</span></span>
  
<span data-ttu-id="00edf-390">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-390">personal id number</span></span>
  
<span data-ttu-id="00edf-391">personalidno #</span><span class="sxs-lookup"><span data-stu-id="00edf-391">personalidno#</span></span>
  
<span data-ttu-id="00edf-392">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-392">unique id number</span></span>
  
<span data-ttu-id="00edf-393">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="00edf-393">personalidnumber#</span></span>
  
<span data-ttu-id="00edf-394">Уникальный идентификатор ключа</span><span class="sxs-lookup"><span data-stu-id="00edf-394">unique id key</span></span>
  
<span data-ttu-id="00edf-395">личный код</span><span class="sxs-lookup"><span data-stu-id="00edf-395">personal id code</span></span>
  
<span data-ttu-id="00edf-396">uniqueidkey #</span><span class="sxs-lookup"><span data-stu-id="00edf-396">uniqueidkey#</span></span>
  
<span data-ttu-id="00edf-397">отдельные кода</span><span class="sxs-lookup"><span data-stu-id="00edf-397">individual code</span></span>
  
<span data-ttu-id="00edf-398">отдельные идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-398">individual id</span></span>
  
<span data-ttu-id="00edf-399">Идентификатор eindeutige-nummer</span><span class="sxs-lookup"><span data-stu-id="00edf-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="00edf-400">Идентификатор eindeutige</span><span class="sxs-lookup"><span data-stu-id="00edf-400">eindeutige id</span></span>
  
<span data-ttu-id="00edf-401">Идентификатор personnelle</span><span class="sxs-lookup"><span data-stu-id="00edf-401">id personnelle</span></span>
  
<span data-ttu-id="00edf-402">numéro d'identification персонала</span><span class="sxs-lookup"><span data-stu-id="00edf-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="00edf-403">idpersonnelle #</span><span class="sxs-lookup"><span data-stu-id="00edf-403">idpersonnelle#</span></span>
  
<span data-ttu-id="00edf-404">persönliche identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="00edf-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="00edf-405">eindeutigeid #</span><span class="sxs-lookup"><span data-stu-id="00edf-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="00edf-406">Мальта</span><span class="sxs-lookup"><span data-stu-id="00edf-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="00edf-407">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-407">Format</span></span>

<span data-ttu-id="00edf-408">Семь цифр, следуют одна буква</span><span class="sxs-lookup"><span data-stu-id="00edf-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-409">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-409">Pattern</span></span>

<span data-ttu-id="00edf-410">Семь цифр, следуют одна буква:</span><span class="sxs-lookup"><span data-stu-id="00edf-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="00edf-411">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="00edf-411">Seven digits</span></span> 
    
- <span data-ttu-id="00edf-412">Один прописные буквы (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="00edf-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-413">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-413">Checksum</span></span>

<span data-ttu-id="00edf-414">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="00edf-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-415">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-415">Definition</span></span>

<span data-ttu-id="00edf-416">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-417">Регулярное выражение `Regex_malta_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-418">Ключевое слово из `Keywords_malta_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-419">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-420">Регулярное выражение `Regex_malta_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-421">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="00edf-422">Keywords_malta_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="00edf-423">личный цифровой код</span><span class="sxs-lookup"><span data-stu-id="00edf-423">personal numeric code</span></span>
  
<span data-ttu-id="00edf-424">Уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-424">unique identification number</span></span>
  
<span data-ttu-id="00edf-425">номер службы граждан</span><span class="sxs-lookup"><span data-stu-id="00edf-425">citizen service number</span></span>
  
<span data-ttu-id="00edf-426">количество уникальных идентификаторов</span><span class="sxs-lookup"><span data-stu-id="00edf-426">unique identity number</span></span>
  
<span data-ttu-id="00edf-427">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="00edf-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="00edf-428">kodiċi numerali personali</span><span class="sxs-lookup"><span data-stu-id="00edf-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="00edf-429">numru ta "identifikazzjoni uniku</span><span class="sxs-lookup"><span data-stu-id="00edf-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="00edf-430">numru задач servizz taċ-ċittadin</span><span class="sxs-lookup"><span data-stu-id="00edf-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="00edf-431">numru ta "identità uniku</span><span class="sxs-lookup"><span data-stu-id="00edf-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="00edf-432">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="00edf-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="00edf-433">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-433">Format</span></span>

<span data-ttu-id="00edf-434">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-435">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-435">Pattern</span></span>

<span data-ttu-id="00edf-436">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="00edf-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="00edf-437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-437">Checksum</span></span>

<span data-ttu-id="00edf-438">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-439">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-439">Definition</span></span>

<span data-ttu-id="00edf-440">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-441">Функция `Func_netherlands_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-442">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="00edf-442">A keyword from is found.</span></span>
    
<span data-ttu-id="00edf-443">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-444">Функция `Func_netherlands_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-445">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="00edf-446">Keywords_netherlands_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="00edf-447">личный цифровой код</span><span class="sxs-lookup"><span data-stu-id="00edf-447">personal numeric code</span></span>
  
<span data-ttu-id="00edf-448">Уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-448">unique identification number</span></span>
  
<span data-ttu-id="00edf-449">номер службы граждан</span><span class="sxs-lookup"><span data-stu-id="00edf-449">citizen service number</span></span>
  
<span data-ttu-id="00edf-450">количество уникальных идентификаторов</span><span class="sxs-lookup"><span data-stu-id="00edf-450">unique identity number</span></span>
  
<span data-ttu-id="00edf-451">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="00edf-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="00edf-452">bsn</span><span class="sxs-lookup"><span data-stu-id="00edf-452">bsn</span></span>
  
<span data-ttu-id="00edf-453">bsn #</span><span class="sxs-lookup"><span data-stu-id="00edf-453">bsn#</span></span>
  
<span data-ttu-id="00edf-454">Код numerieke persoonlijke</span><span class="sxs-lookup"><span data-stu-id="00edf-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="00edf-455">uniek identificatienummer</span><span class="sxs-lookup"><span data-stu-id="00edf-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="00edf-456">burgerservicenummer</span><span class="sxs-lookup"><span data-stu-id="00edf-456">burgerservicenummer</span></span>
  
<span data-ttu-id="00edf-457">uniek identiteitsnummer</span><span class="sxs-lookup"><span data-stu-id="00edf-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="00edf-458">Польша</span><span class="sxs-lookup"><span data-stu-id="00edf-458">Poland</span></span>

<span data-ttu-id="00edf-459">Для получения дополнительных сведений обратитесь к разделу «Польша национальный идентификатор (PESEL)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="00edf-460">Португалия</span><span class="sxs-lookup"><span data-stu-id="00edf-460">Portugal</span></span>

<span data-ttu-id="00edf-461">Для получения дополнительных сведений обратитесь к разделу «Номер карты Португалия граждане» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="00edf-462">Румыния</span><span class="sxs-lookup"><span data-stu-id="00edf-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="00edf-463">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-463">Format</span></span>

<span data-ttu-id="00edf-464">13 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-465">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-465">Pattern</span></span>

<span data-ttu-id="00edf-466">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="00edf-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="00edf-467">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-467">Checksum</span></span>

<span data-ttu-id="00edf-468">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-469">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-469">Definition</span></span>

<span data-ttu-id="00edf-470">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-471">Функция `Func_romania_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-472">Ключевое слово из `Keywords_romania_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-473">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-474">Функция `Func_romania_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-475">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="00edf-476">Keywords_romania_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="00edf-477">личный цифровой код</span><span class="sxs-lookup"><span data-stu-id="00edf-477">personal numeric code</span></span>
  
<span data-ttu-id="00edf-478">Уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-478">unique identification number</span></span>
  
<span data-ttu-id="00edf-479">cnp</span><span class="sxs-lookup"><span data-stu-id="00edf-479">cnp</span></span>
  
<span data-ttu-id="00edf-480">cnp #</span><span class="sxs-lookup"><span data-stu-id="00edf-480">cnp#</span></span>
  
<span data-ttu-id="00edf-481">закрепить</span><span class="sxs-lookup"><span data-stu-id="00edf-481">pin</span></span>
  
<span data-ttu-id="00edf-482">ПИН-код #</span><span class="sxs-lookup"><span data-stu-id="00edf-482">pin#</span></span>
  
<span data-ttu-id="00edf-483">страховой номер</span><span class="sxs-lookup"><span data-stu-id="00edf-483">insurance number</span></span>
  
<span data-ttu-id="00edf-484">insurancenumber #</span><span class="sxs-lookup"><span data-stu-id="00edf-484">insurancenumber#</span></span>
  
<span data-ttu-id="00edf-485">количество уникальных идентификаторов</span><span class="sxs-lookup"><span data-stu-id="00edf-485">unique identity number</span></span>
  
<span data-ttu-id="00edf-486">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="00edf-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="00edf-487">числовой личные COD</span><span class="sxs-lookup"><span data-stu-id="00edf-487">cod numeric personal</span></span>
  
<span data-ttu-id="00edf-488">решить identificare личные</span><span class="sxs-lookup"><span data-stu-id="00edf-488">cod identificare personal</span></span>
  
<span data-ttu-id="00edf-489">COD unic identificare</span><span class="sxs-lookup"><span data-stu-id="00edf-489">cod unic identificare</span></span>
  
<span data-ttu-id="00edf-490">личные unic număr</span><span class="sxs-lookup"><span data-stu-id="00edf-490">număr personal unic</span></span>
  
<span data-ttu-id="00edf-491">număr identitate</span><span class="sxs-lookup"><span data-stu-id="00edf-491">număr identitate</span></span>
  
<span data-ttu-id="00edf-492">личные identificare număr</span><span class="sxs-lookup"><span data-stu-id="00edf-492">număr identificare personal</span></span>
  
<span data-ttu-id="00edf-493">număridentitate #</span><span class="sxs-lookup"><span data-stu-id="00edf-493">număridentitate#</span></span>
  
<span data-ttu-id="00edf-494">codnumericpersonal #</span><span class="sxs-lookup"><span data-stu-id="00edf-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="00edf-495">numărpersonalunic #</span><span class="sxs-lookup"><span data-stu-id="00edf-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="00edf-496">Словакия</span><span class="sxs-lookup"><span data-stu-id="00edf-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="00edf-497">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-497">Format</span></span>

<span data-ttu-id="00edf-498">10 цифр, содержащий один символ косой черты</span><span class="sxs-lookup"><span data-stu-id="00edf-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-499">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-499">Pattern</span></span>

<span data-ttu-id="00edf-500">10 цифр, содержащий один символ косой черты:</span><span class="sxs-lookup"><span data-stu-id="00edf-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="00edf-501">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-501">Checksum</span></span>

<span data-ttu-id="00edf-502">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-503">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-503">Definition</span></span>

<span data-ttu-id="00edf-504">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-505">Функция `Func_slovakia_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-506">Ключевое слово из `Keywords_slovakia_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-507">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-508">Функция `Func_slovakia_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-509">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="00edf-510">Keywords_slovakia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="00edf-511">Номер рождения</span><span class="sxs-lookup"><span data-stu-id="00edf-511">birth number</span></span>
  
<span data-ttu-id="00edf-512">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-512">national identification number</span></span>
  
<span data-ttu-id="00edf-513">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-513">personal identification number</span></span>
  
<span data-ttu-id="00edf-514">social security number
</span><span class="sxs-lookup"><span data-stu-id="00edf-514">social security number</span></span>
  
<span data-ttu-id="00edf-515">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="00edf-515">nationalnumber#</span></span>
  
<span data-ttu-id="00edf-516">SSN #</span><span class="sxs-lookup"><span data-stu-id="00edf-516">ssn#</span></span>
  
<span data-ttu-id="00edf-517">SSN</span><span class="sxs-lookup"><span data-stu-id="00edf-517">ssn</span></span>
  
<span data-ttu-id="00edf-518">Национальный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-518">national number</span></span>
  
<span data-ttu-id="00edf-519">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-519">personal id number</span></span>
  
<span data-ttu-id="00edf-520">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="00edf-520">personalidnumber#</span></span>
  
<span data-ttu-id="00edf-521">rč</span><span class="sxs-lookup"><span data-stu-id="00edf-521">rč</span></span>
  
<span data-ttu-id="00edf-522">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="00edf-522">rodné číslo</span></span>
  
<span data-ttu-id="00edf-523">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="00edf-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="00edf-524">Словения</span><span class="sxs-lookup"><span data-stu-id="00edf-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="00edf-525">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-525">Format</span></span>

<span data-ttu-id="00edf-526">13 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="00edf-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-527">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-527">Pattern</span></span>

<span data-ttu-id="00edf-528">13 цифр в указанному шаблону:</span><span class="sxs-lookup"><span data-stu-id="00edf-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="00edf-529">Семь цифр, которые соответствуют Дата рождения (DDMMLLL), где «LLL» к последнему соответствует трех цифр год рождения</span><span class="sxs-lookup"><span data-stu-id="00edf-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="00edf-530">Две цифры, которые соответствуют области рождения</span><span class="sxs-lookup"><span data-stu-id="00edf-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="00edf-531">Три цифры, которые соответствуют сочетание пол и серийный номер для лиц, рождения на тот же день (для м 000 499) и 500 до 999 женщина</span><span class="sxs-lookup"><span data-stu-id="00edf-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="00edf-532">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="00edf-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-533">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-533">Checksum</span></span>

<span data-ttu-id="00edf-534">Да</span><span class="sxs-lookup"><span data-stu-id="00edf-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-535">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-535">Definition</span></span>

<span data-ttu-id="00edf-536">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-537">Функция `Func_slovenia_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-538">Ключевое слово из `Keywords_slovenia_eu_national_id_card` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="00edf-539">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-540">Функция `Func_slovenia_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-541">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="00edf-542">Keywords_slovenia_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="00edf-543">личный цифровой код</span><span class="sxs-lookup"><span data-stu-id="00edf-543">personal numeric code</span></span>
  
<span data-ttu-id="00edf-544">Уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-544">unique identification number</span></span>
  
<span data-ttu-id="00edf-545">Уникальный номер регистрации</span><span class="sxs-lookup"><span data-stu-id="00edf-545">unique registration number</span></span>
  
<span data-ttu-id="00edf-546">количество уникальных идентификаторов</span><span class="sxs-lookup"><span data-stu-id="00edf-546">unique identity number</span></span>
  
<span data-ttu-id="00edf-547">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="00edf-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="00edf-548">число уникальных главных граждан</span><span class="sxs-lookup"><span data-stu-id="00edf-548">unique master citizen number</span></span>
  
<span data-ttu-id="00edf-549">edinstvena identifikacijska številka</span><span class="sxs-lookup"><span data-stu-id="00edf-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="00edf-550">uniqueidentityno #</span><span class="sxs-lookup"><span data-stu-id="00edf-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="00edf-551">edinstvena številka glavnega državljana</span><span class="sxs-lookup"><span data-stu-id="00edf-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="00edf-552">emšo</span><span class="sxs-lookup"><span data-stu-id="00edf-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="00edf-553">Испания</span><span class="sxs-lookup"><span data-stu-id="00edf-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="00edf-554">Формат</span><span class="sxs-lookup"><span data-stu-id="00edf-554">Format</span></span>

<span data-ttu-id="00edf-555">Семь цифр, за которой следует один символ</span><span class="sxs-lookup"><span data-stu-id="00edf-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="00edf-556">Шаблон</span><span class="sxs-lookup"><span data-stu-id="00edf-556">Pattern</span></span>

<span data-ttu-id="00edf-557">Семь цифр, за которой следует один символ</span><span class="sxs-lookup"><span data-stu-id="00edf-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="00edf-558">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="00edf-558">Seven digits</span></span>
    
- <span data-ttu-id="00edf-559">Одну цифру или букву (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="00edf-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="00edf-560">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="00edf-560">Checksum</span></span>

<span data-ttu-id="00edf-561">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="00edf-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="00edf-562">Определение</span><span class="sxs-lookup"><span data-stu-id="00edf-562">Definition</span></span>

<span data-ttu-id="00edf-563">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="00edf-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="00edf-564">Регулярное выражение `Regex_spain_eu_national_id_card` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="00edf-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="00edf-565">Ключевое слово из `Keywords_spain_eu_national_id_card"` найден.</span><span class="sxs-lookup"><span data-stu-id="00edf-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="00edf-566">Keywords</span><span class="sxs-lookup"><span data-stu-id="00edf-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="00edf-567">Keywords_spain_eu_national_id_card</span><span class="sxs-lookup"><span data-stu-id="00edf-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="00edf-568">не установлен</span><span class="sxs-lookup"><span data-stu-id="00edf-568">dni</span></span>
  
<span data-ttu-id="00edf-569">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-569">national identification number</span></span>
  
<span data-ttu-id="00edf-570">Национальный идентификатор номер</span><span class="sxs-lookup"><span data-stu-id="00edf-570">national identity number</span></span>
  
<span data-ttu-id="00edf-571">страховой номер</span><span class="sxs-lookup"><span data-stu-id="00edf-571">insurance number</span></span>
  
<span data-ttu-id="00edf-572">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="00edf-572">personal identification number</span></span>
  
<span data-ttu-id="00edf-573">Национальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="00edf-573">national identity</span></span>
  
<span data-ttu-id="00edf-574">личные нет</span><span class="sxs-lookup"><span data-stu-id="00edf-574">personal identity no</span></span>
  
<span data-ttu-id="00edf-575">количество уникальных идентификаторов</span><span class="sxs-lookup"><span data-stu-id="00edf-575">unique identity number</span></span>
  
<span data-ttu-id="00edf-576">nationalidno #</span><span class="sxs-lookup"><span data-stu-id="00edf-576">nationalidno#</span></span>
  
<span data-ttu-id="00edf-577">Уникальный идентификатор #</span><span class="sxs-lookup"><span data-stu-id="00edf-577">uniqueid#</span></span>
  
<span data-ttu-id="00edf-578">не установлен #</span><span class="sxs-lookup"><span data-stu-id="00edf-578">dni#</span></span>
  
<span data-ttu-id="00edf-579">nationalid #</span><span class="sxs-lookup"><span data-stu-id="00edf-579">nationalid#</span></span>
  
<span data-ttu-id="00edf-580">NIE #</span><span class="sxs-lookup"><span data-stu-id="00edf-580">nie#</span></span>
  
<span data-ttu-id="00edf-581">NIE</span><span class="sxs-lookup"><span data-stu-id="00edf-581">nie</span></span>
  
<span data-ttu-id="00edf-582">nienúmero #</span><span class="sxs-lookup"><span data-stu-id="00edf-582">nienúmero#</span></span>
  
<span data-ttu-id="00edf-583">NIE número</span><span class="sxs-lookup"><span data-stu-id="00edf-583">nie número</span></span>
  
<span data-ttu-id="00edf-584">documento nacional де identidad</span><span class="sxs-lookup"><span data-stu-id="00edf-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="00edf-585">identidad único</span><span class="sxs-lookup"><span data-stu-id="00edf-585">identidad único</span></span>
  
<span data-ttu-id="00edf-586">número nacional identidad</span><span class="sxs-lookup"><span data-stu-id="00edf-586">número nacional identidad</span></span>
  
<span data-ttu-id="00edf-587">número не установлен</span><span class="sxs-lookup"><span data-stu-id="00edf-587">dni número</span></span>
  
<span data-ttu-id="00edf-588">dninúmero #</span><span class="sxs-lookup"><span data-stu-id="00edf-588">dninúmero#</span></span>
  
<span data-ttu-id="00edf-589">identidadúnico #</span><span class="sxs-lookup"><span data-stu-id="00edf-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="00edf-590">Швеция</span><span class="sxs-lookup"><span data-stu-id="00edf-590">Sweden</span></span>

<span data-ttu-id="00edf-591">Для получения дополнительных сведений обратитесь к разделу «Национальный идентификатор для Швеции» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="00edf-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00edf-592">См. также</span><span class="sxs-lookup"><span data-stu-id="00edf-592">See also</span></span>

[<span data-ttu-id="00edf-593">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="00edf-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

