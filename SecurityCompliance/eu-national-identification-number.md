---
title: Национальный идентификационный номер ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС по национальному идентификационному номеру. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: 205019d040648f0600f3dbf4403063edf9f31c41
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154466"
---
# <a name="eu-national-identification-number"></a><span data-ttu-id="35269-104">Национальный идентификационный номер ЕС</span><span class="sxs-lookup"><span data-stu-id="35269-104">EU National Identification Number</span></span>

<span data-ttu-id="35269-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС по национальному идентификационному номеру.</span><span class="sxs-lookup"><span data-stu-id="35269-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU National Identification Number sensitive information type.</span></span> <span data-ttu-id="35269-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="35269-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="35269-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="35269-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="35269-108">Format</span><span class="sxs-lookup"><span data-stu-id="35269-108">Format</span></span>

<span data-ttu-id="35269-109">24 – символическое сочетание букв, цифр и специальных символов;</span><span class="sxs-lookup"><span data-stu-id="35269-109">A 24-character combination of letters, digits, and special characters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-110">Pattern</span></span>

<span data-ttu-id="35269-111">24 символа:</span><span class="sxs-lookup"><span data-stu-id="35269-111">24 characters:</span></span>
  
-  <span data-ttu-id="35269-112">22 буквы (без учета регистра), цифры, обратные косые черты, косые черты и знаки плюса</span><span class="sxs-lookup"><span data-stu-id="35269-112">22 letters (not case-sensitive), digits, backslashes, forward slashes, or plus signs</span></span> 
    
- <span data-ttu-id="35269-113">Две буквы (без учета регистра), цифры, обратные косые черты, знаки косой черты, знаки плюса и знаки равенства.</span><span class="sxs-lookup"><span data-stu-id="35269-113">Two letters (not case-sensitive), digits, backslashes, forward slashes, plus signs, or equal signs</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-114">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-114">Checksum</span></span>

<span data-ttu-id="35269-115">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="35269-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-116">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-116">Definition</span></span>

<span data-ttu-id="35269-117">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-118">Регулярное выражение `Regex_austria_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-118">The regular expression  `Regex_austria_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-119">Найдено ключевое `Keywords_austria_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-119">A keyword from  `Keywords_austria_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="35269-120">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-120">Keywords</span></span>

#### <a name="keywordsaustriaeunationalidcard"></a><span data-ttu-id="35269-121">Кэйвордс_аустриа_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-121">Keywords_austria_eu_national_id_card</span></span>

<span data-ttu-id="35269-122">Австрийский номер удостоверения</span><span class="sxs-lookup"><span data-stu-id="35269-122">austrian identity number</span></span>
  
<span data-ttu-id="35269-123">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-123">national identity number</span></span>
  
<span data-ttu-id="35269-124">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-124">identity number</span></span>
  
<span data-ttu-id="35269-125">national id</span><span class="sxs-lookup"><span data-stu-id="35269-125">national id</span></span>
  
<span data-ttu-id="35269-126">персоналаусвеис Републик öстерреич</span><span class="sxs-lookup"><span data-stu-id="35269-126">personalausweis republik österreich</span></span>
  
## <a name="belgium"></a><span data-ttu-id="35269-127">Бельгия</span><span class="sxs-lookup"><span data-stu-id="35269-127">Belgium</span></span>

<span data-ttu-id="35269-128">Дополнительные сведения можно найти в разделе "Бельгии National Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-128">For details, see the section "Belgium National Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="35269-129">Болгария</span><span class="sxs-lookup"><span data-stu-id="35269-129">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="35269-130">Format</span><span class="sxs-lookup"><span data-stu-id="35269-130">Format</span></span>

<span data-ttu-id="35269-131">Десять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-131">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-132">Pattern</span></span>

<span data-ttu-id="35269-133">Десять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-133">Ten digits without spaces and delimiters</span></span>
  
-  <span data-ttu-id="35269-134">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="35269-134">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="35269-135">Две цифры, соответствующие порядку рождения</span><span class="sxs-lookup"><span data-stu-id="35269-135">Two digits that correspond to the birth order</span></span>
    
- <span data-ttu-id="35269-136">Одна цифра, соответствующая Пол: четное число для пола и нечетная цифра для розетки</span><span class="sxs-lookup"><span data-stu-id="35269-136">One digit that corresponds to gender: An even digit for male and an odd digit for female</span></span>
    
- <span data-ttu-id="35269-137">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="35269-137">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-138">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-138">Checksum</span></span>

<span data-ttu-id="35269-139">Да</span><span class="sxs-lookup"><span data-stu-id="35269-139">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-140">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-140">Definition</span></span>

<span data-ttu-id="35269-141">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-141">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-142">Функция `Func_bulgaria_national_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-142">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-143">Найдено ключевое `Keywords_bulgaria_national_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-143">A keyword from  `Keywords_bulgaria_national_number` is found.</span></span> 
    
<span data-ttu-id="35269-144">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-144">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-145">Функция `Func_bulgaria_national_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-145">The function  `Func_bulgaria_national_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-146">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-146">Keywords</span></span>

#### <a name="keywordsbulgarianationalnumber"></a><span data-ttu-id="35269-147">Кэйвордс_булгариа_натионал_нумбер</span><span class="sxs-lookup"><span data-stu-id="35269-147">Keywords_bulgaria_national_number</span></span>

<span data-ttu-id="35269-148">ЕГН</span><span class="sxs-lookup"><span data-stu-id="35269-148">egn</span></span>
  
<span data-ttu-id="35269-149">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="35269-149">egn#</span></span>
  
<span data-ttu-id="35269-150">Национальный номер для болгарского языка</span><span class="sxs-lookup"><span data-stu-id="35269-150">bulgarian national number</span></span>
  
<span data-ttu-id="35269-151">номер страны</span><span class="sxs-lookup"><span data-stu-id="35269-151">national number</span></span>
  
<span data-ttu-id="35269-152">social security number</span><span class="sxs-lookup"><span data-stu-id="35269-152">social security number</span></span>
  
<span data-ttu-id="35269-153">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="35269-153">nationalnumber#</span></span>
  
<span data-ttu-id="35269-154">SSN</span><span class="sxs-lookup"><span data-stu-id="35269-154">ssn#</span></span>
  
<span data-ttu-id="35269-155">SSN</span><span class="sxs-lookup"><span data-stu-id="35269-155">ssn</span></span>
  
<span data-ttu-id="35269-156">натионалнумбер</span><span class="sxs-lookup"><span data-stu-id="35269-156">nationalnumber</span></span>
  
<span data-ttu-id="35269-157">БНН #</span><span class="sxs-lookup"><span data-stu-id="35269-157">bnn#</span></span>
  
<span data-ttu-id="35269-158">БНН</span><span class="sxs-lookup"><span data-stu-id="35269-158">bnn</span></span>
  
<span data-ttu-id="35269-159">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-159">personal id number</span></span>
  
<span data-ttu-id="35269-160">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="35269-160">personalidnumber#</span></span>
  
<span data-ttu-id="35269-161">единен граждански номер</span><span class="sxs-lookup"><span data-stu-id="35269-161">единен граждански номер</span></span>
  
<span data-ttu-id="35269-162">единен граздански номер</span><span class="sxs-lookup"><span data-stu-id="35269-162">edinen grazhdanski nomer</span></span>
  
<span data-ttu-id="35269-163">ЕГН</span><span class="sxs-lookup"><span data-stu-id="35269-163">егн</span></span>
  
<span data-ttu-id="35269-164">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="35269-164">егн#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="35269-165">Хорватия</span><span class="sxs-lookup"><span data-stu-id="35269-165">Croatia</span></span>

<span data-ttu-id="35269-166">Дополнительные сведения см. в разделе "номер идентификатора Хорватия" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-166">For details, see the section "Croatia Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="35269-167">Кипр</span><span class="sxs-lookup"><span data-stu-id="35269-167">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="35269-168">Format</span><span class="sxs-lookup"><span data-stu-id="35269-168">Format</span></span>

<span data-ttu-id="35269-169">Десять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-169">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-170">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-170">Pattern</span></span>

 <span data-ttu-id="35269-171">Десять цифр</span><span class="sxs-lookup"><span data-stu-id="35269-171">Ten digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="35269-172">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-172">Checksum</span></span>

<span data-ttu-id="35269-173">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="35269-173">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-174">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-174">Definition</span></span>

<span data-ttu-id="35269-175">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-175">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-176">Регулярное выражение `Regex_cyprus_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-176">The regular expression  `Regex_cyprus_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-177">Найдено ключевое `Keywords_cyprus_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-177">A keyword from  `Keywords_cyprus_eu_national_id_card` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="35269-178">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-178">Keywords</span></span>

#### <a name="keywordscypruseunationalidcard"></a><span data-ttu-id="35269-179">Кэйвордс_ципрус_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-179">Keywords_cyprus_eu_national_id_card</span></span>

<span data-ttu-id="35269-180">идентификационный номер карточки</span><span class="sxs-lookup"><span data-stu-id="35269-180">id card number</span></span>
  
<span data-ttu-id="35269-181">national identification number</span><span class="sxs-lookup"><span data-stu-id="35269-181">national identification number</span></span>
  
<span data-ttu-id="35269-182">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-182">personal id number</span></span>
  
<span data-ttu-id="35269-183">Номер идентификационной карточки</span><span class="sxs-lookup"><span data-stu-id="35269-183">identity card number</span></span>
  
<span data-ttu-id="35269-184">ταυτοτητασ</span><span class="sxs-lookup"><span data-stu-id="35269-184">ταυτοτητασ</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="35269-185">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="35269-185">Czech Republic</span></span>

<span data-ttu-id="35269-186">Для получения дополнительных сведений обратитесь к разделу "Чешский Национальный идентификационный номер", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-186">For details, see the section "Czech National Identity Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="denmark"></a><span data-ttu-id="35269-187">Дания</span><span class="sxs-lookup"><span data-stu-id="35269-187">Denmark</span></span>

<span data-ttu-id="35269-188">Дополнительные сведения можно найти в разделе "Дания персонального идентификационного номера", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-188">For details, see the section "Denmark Personal Identification Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="estonia"></a><span data-ttu-id="35269-189">Эстония</span><span class="sxs-lookup"><span data-stu-id="35269-189">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="35269-190">Format</span><span class="sxs-lookup"><span data-stu-id="35269-190">Format</span></span>

<span data-ttu-id="35269-191">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-191">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-192">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-192">Pattern</span></span>

<span data-ttu-id="35269-193">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="35269-193">11 digits:</span></span>
  
- <span data-ttu-id="35269-194">Одна цифра, соответствующая упоминанию секса и столетию рождения (нечетный номер, четная розетка), 1-2:19 века; 3-4:20 века; 5-6:21 столетие)</span><span class="sxs-lookup"><span data-stu-id="35269-194">One digit that corresponds to sex and century of birth (odd number male, even number female; 1-2: 19th century; 3-4: 20th century; 5-6: 21st century)</span></span>
    
- <span data-ttu-id="35269-195">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="35269-195">Six digits that correspond to date of birth (YYMMDD)</span></span>
    
- <span data-ttu-id="35269-196">Три цифры, которые соответствуют порядковому номеру, разделенному на одну и ту же дату.</span><span class="sxs-lookup"><span data-stu-id="35269-196">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="35269-197">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="35269-197">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-198">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-198">Checksum</span></span>

<span data-ttu-id="35269-199">Да</span><span class="sxs-lookup"><span data-stu-id="35269-199">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-200">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-200">Definition</span></span>

<span data-ttu-id="35269-201">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-201">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-202">Функция `Func_estonia_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-202">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-203">Найдено ключевое `Keywords_estonia_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-203">A keyword from  `Keywords_estonia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-204">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-204">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-205">Функция `Func_estonia_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-205">The function  `Func_estonia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-206">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-206">Keywords</span></span>

#### <a name="keywordsestoniaeunationalidcard"></a><span data-ttu-id="35269-207">Кэйвордс_естониа_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-207">Keywords_estonia_eu_national_id_card</span></span>

<span data-ttu-id="35269-208">персональный идентификационный код</span><span class="sxs-lookup"><span data-stu-id="35269-208">personal identification code</span></span>
  
<span data-ttu-id="35269-209">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-209">personal identification number</span></span>
  
<span data-ttu-id="35269-210">national identification number</span><span class="sxs-lookup"><span data-stu-id="35269-210">national identification number</span></span>
  
<span data-ttu-id="35269-211">номер страны</span><span class="sxs-lookup"><span data-stu-id="35269-211">national number</span></span>
  
<span data-ttu-id="35269-212">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-212">personal id number</span></span>
  
<span data-ttu-id="35269-213">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="35269-213">personalidnumber#</span></span>
  
<span data-ttu-id="35269-214">фигуры</span><span class="sxs-lookup"><span data-stu-id="35269-214">ik</span></span>
  
<span data-ttu-id="35269-215">исикукуд</span><span class="sxs-lookup"><span data-stu-id="35269-215">isikukood</span></span>
  
<span data-ttu-id="35269-216">ID — каарт</span><span class="sxs-lookup"><span data-stu-id="35269-216">id-kaart</span></span>
  
## <a name="finland"></a><span data-ttu-id="35269-217">Финляндия</span><span class="sxs-lookup"><span data-stu-id="35269-217">Finland</span></span>

<span data-ttu-id="35269-218">Дополнительные сведения можно найти в разделе "Финляндия национального ID", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-218">For details, see the section "Finland National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="35269-219">Франция</span><span class="sxs-lookup"><span data-stu-id="35269-219">France</span></span>

<span data-ttu-id="35269-220">Дополнительные сведения можно найти в разделе "Французская Национальная ИДЕНТИФИКАЦИОНная карточка (CNI)" [, в которой отображаются типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-220">For details, see the section "France National ID Card (CNI)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="35269-221">Германия</span><span class="sxs-lookup"><span data-stu-id="35269-221">Germany</span></span>

<span data-ttu-id="35269-222">Дополнительные сведения можно найти в разделе "номер идентификационной карточки для Германии" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-222">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="35269-223">Греция</span><span class="sxs-lookup"><span data-stu-id="35269-223">Greece</span></span>

<span data-ttu-id="35269-224">Дополнительные сведения можно найти в разделе "Греция National ID Card", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-224">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="35269-225">Венгрия</span><span class="sxs-lookup"><span data-stu-id="35269-225">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="35269-226">Format</span><span class="sxs-lookup"><span data-stu-id="35269-226">Format</span></span>

<span data-ttu-id="35269-227">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="35269-227">11 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-228">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-228">Pattern</span></span>

<span data-ttu-id="35269-229">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="35269-229">11 digits:</span></span>
  
-  <span data-ttu-id="35269-230">Одна цифра, соответствующая пол (1-м-штекер, 2-гнездо, другие номера также могут иметь гражданские телефоны перед 1900 или гражданами с удвоенной гражданией)</span><span class="sxs-lookup"><span data-stu-id="35269-230">One digit that corresponds to gender (1-male, 2-female, other numbers are also possible for citizens born before 1900 or citizens with double citizenship)</span></span> 
    
- <span data-ttu-id="35269-231">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="35269-231">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="35269-232">Три цифры, соответствующие серийному номеру.</span><span class="sxs-lookup"><span data-stu-id="35269-232">Three digits that correspond to a serial number</span></span>
    
- <span data-ttu-id="35269-233">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="35269-233">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-234">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-234">Checksum</span></span>

<span data-ttu-id="35269-235">Да</span><span class="sxs-lookup"><span data-stu-id="35269-235">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-236">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-236">Definition</span></span>

<span data-ttu-id="35269-237">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-237">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-238">Функция `Func_hungary_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-238">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-239">Найдено ключевое `Keywords_hungary_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-239">A keyword from  `Keywords_hungary_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-240">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-240">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-241">Функция `Func_hungary_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-241">The function  `Func_hungary_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-242">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-242">Keywords</span></span>

#### <a name="keywordshungaryeunationalidcard"></a><span data-ttu-id="35269-243">Кэйвордс_хунгари_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-243">Keywords_hungary_eu_national_id_card</span></span>

<span data-ttu-id="35269-244">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-244">personal identification number</span></span>
  
<span data-ttu-id="35269-245">identification number</span><span class="sxs-lookup"><span data-stu-id="35269-245">identification number</span></span>
  
<span data-ttu-id="35269-246">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-246">personal id number</span></span>
  
<span data-ttu-id="35269-247">сземéлязоносíтó игазолвáни</span><span class="sxs-lookup"><span data-stu-id="35269-247">személyazonosító igazolvány</span></span>
  
## <a name="ireland"></a><span data-ttu-id="35269-248">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="35269-248">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="35269-249">Format</span><span class="sxs-lookup"><span data-stu-id="35269-249">Format</span></span>

<span data-ttu-id="35269-250">Сочетание букв, цифр и пробела в указанном шаблоне.</span><span class="sxs-lookup"><span data-stu-id="35269-250">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-251">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-251">Pattern</span></span>

<span data-ttu-id="35269-252">Сочетание букв, цифр и пробела в указанном шаблоне.</span><span class="sxs-lookup"><span data-stu-id="35269-252">A nine-character combination of letters, digits, and a space in the specified pattern</span></span>
  
<span data-ttu-id="35269-253">От 01 января 2013 до Now:</span><span class="sxs-lookup"><span data-stu-id="35269-253">From 01 January 2013 to now:</span></span>
  
-  <span data-ttu-id="35269-254">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="35269-254">Seven digits</span></span> 
    
- <span data-ttu-id="35269-255">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="35269-255">One check digit</span></span>
    
- <span data-ttu-id="35269-256">Один пробел или буква в верхнем регистре "W" (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="35269-256">One space or the uppercase letter "W" (Case sensitive)</span></span>
    
<span data-ttu-id="35269-257">До 01 января 2013:</span><span class="sxs-lookup"><span data-stu-id="35269-257">Prior to 01 January 2013:</span></span>
  
-  <span data-ttu-id="35269-258">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="35269-258">Seven digits</span></span> 
    
- <span data-ttu-id="35269-259">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="35269-259">One check digit</span></span>
    
- <span data-ttu-id="35269-260">Один пробел или буква в верхнем регистре (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="35269-260">One space or an uppercase letter (Case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-261">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-261">Checksum</span></span>

<span data-ttu-id="35269-262">Да</span><span class="sxs-lookup"><span data-stu-id="35269-262">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-263">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-263">Definition</span></span>

<span data-ttu-id="35269-264">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-264">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-265">Функция находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-265">The function finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="35269-266">Найдено ключевое слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-266">A keyword from is found.</span></span>
    
<span data-ttu-id="35269-267">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-268">Функция находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-268">The function finds content that matches the pattern.</span></span>
    
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

### <a name="keywords"></a><span data-ttu-id="35269-269">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-269">Keywords</span></span>

#### <a name="keywordsirelandeunationalidcard"></a><span data-ttu-id="35269-270">Кэйвордс_иреланд_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-270">Keywords_ireland_eu_national_id_card</span></span>

<span data-ttu-id="35269-271">номер личной общедоступной службы</span><span class="sxs-lookup"><span data-stu-id="35269-271">personal public service number</span></span>
  
<span data-ttu-id="35269-272">PPS нет</span><span class="sxs-lookup"><span data-stu-id="35269-272">pps no</span></span>
  
<span data-ttu-id="35269-273">номер дохода и социального страхования</span><span class="sxs-lookup"><span data-stu-id="35269-273">revenue and social insurance number</span></span>
  
<span data-ttu-id="35269-274">RSI нет</span><span class="sxs-lookup"><span data-stu-id="35269-274">rsi no</span></span>
  
<span data-ttu-id="35269-275">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-275">personal identification number</span></span>
  
<span data-ttu-id="35269-276">identification number</span><span class="sxs-lookup"><span data-stu-id="35269-276">identification number</span></span>
  
<span data-ttu-id="35269-277">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-277">personal id number</span></span>
  
<span data-ttu-id="35269-278">уимхир феарсанта сеирбхíсе поиблí</span><span class="sxs-lookup"><span data-stu-id="35269-278">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="35269-279">уимх.</span><span class="sxs-lookup"><span data-stu-id="35269-279">uimh.</span></span> <span data-ttu-id="35269-280">настроен</span><span class="sxs-lookup"><span data-stu-id="35269-280">psp</span></span>
  
## <a name="italy"></a><span data-ttu-id="35269-281">Италия</span><span class="sxs-lookup"><span data-stu-id="35269-281">Italy</span></span>

### <a name="format"></a><span data-ttu-id="35269-282">Format</span><span class="sxs-lookup"><span data-stu-id="35269-282">Format</span></span>

<span data-ttu-id="35269-283">16 – символическое сочетание букв и цифр в указанном шаблоне.</span><span class="sxs-lookup"><span data-stu-id="35269-283">A 16-character combination of letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-284">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-284">Pattern</span></span>

<span data-ttu-id="35269-285">16 – буквенное сочетание букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="35269-285">A 16-character combination of letters and digits:</span></span>
  
- <span data-ttu-id="35269-286">Три буквы, соответствующие первым трем согласным в имени семейства</span><span class="sxs-lookup"><span data-stu-id="35269-286">Three letters that correspond to the first three consonants in the family name</span></span>
    
- <span data-ttu-id="35269-287">Три буквы, соответствующие первым, третьим и четвертым согласным в имени.</span><span class="sxs-lookup"><span data-stu-id="35269-287">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="35269-288">Две цифры, соответствующие последним цифрам года рождения</span><span class="sxs-lookup"><span data-stu-id="35269-288">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="35269-289">Одна буква, соответствующая букве дня рождения, буквы используются в алфавитном порядке, но используются только буквы от A до E, H, L, M, P, R — T (то есть Январь — это R, а Октябрь — R)</span><span class="sxs-lookup"><span data-stu-id="35269-289">One letter that corresponds to the letter for the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="35269-290">Две цифры, которые соответствуют дню месяца рождения, для различения пола, 40 добавляется в день рождения для женщин</span><span class="sxs-lookup"><span data-stu-id="35269-290">Two digits that correspond to the day of the month of birth—in order to differentiate between genders, 40 is added to the day of birth for women</span></span>
    
- <span data-ttu-id="35269-291">Четыре цифры, соответствующие коду города, который относится к органу государственной власти, в котором был создан пользователь, (для иностранных стран используются коды уровня страны).</span><span class="sxs-lookup"><span data-stu-id="35269-291">Four digits that corresponds to the area code specific to the municipality where the person was born (country-wide codes are used for foreign countries)</span></span>
    
- <span data-ttu-id="35269-292">Одна цифра четности</span><span class="sxs-lookup"><span data-stu-id="35269-292">One parity digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-293">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-293">Checksum</span></span>

<span data-ttu-id="35269-294">Да</span><span class="sxs-lookup"><span data-stu-id="35269-294">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-295">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-295">Definition</span></span>

<span data-ttu-id="35269-296">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-296">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-297">Функция `Func_italy_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-297">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-298">Найдено ключевое `Keywords_italy_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-298">A keyword from  `Keywords_italy_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-299">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-299">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-300">Функция `Func_italy_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-300">The function  `Func_italy_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-301">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-301">Keywords</span></span>

#### <a name="keywordsitalyeunationalidcard"></a><span data-ttu-id="35269-302">Кэйвордс_итали_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-302">Keywords_italy_eu_national_id_card</span></span>

<span data-ttu-id="35269-303">персональный код</span><span class="sxs-lookup"><span data-stu-id="35269-303">personal code</span></span>
  
<span data-ttu-id="35269-304">номер личного кода</span><span class="sxs-lookup"><span data-stu-id="35269-304">personal code number</span></span>
  
<span data-ttu-id="35269-305">личный номер сертификата</span><span class="sxs-lookup"><span data-stu-id="35269-305">personal certificate number</span></span>
  
<span data-ttu-id="35269-306">Финансовый код</span><span class="sxs-lookup"><span data-stu-id="35269-306">fiscal code</span></span>
  
<span data-ttu-id="35269-307">персоналкодено #</span><span class="sxs-lookup"><span data-stu-id="35269-307">personalcodeno#</span></span>
  
<span data-ttu-id="35269-308">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-308">personal id number</span></span>
  
<span data-ttu-id="35269-309">личный код</span><span class="sxs-lookup"><span data-stu-id="35269-309">personal id code</span></span>
  
<span data-ttu-id="35269-310">Персональные подкодеки</span><span class="sxs-lookup"><span data-stu-id="35269-310">codice personale</span></span>
  
<span data-ttu-id="35269-311">Нумеро цертификато персональный</span><span class="sxs-lookup"><span data-stu-id="35269-311">numero certificato personale</span></span>
  
<span data-ttu-id="35269-312">персональные настройки нумеро</span><span class="sxs-lookup"><span data-stu-id="35269-312">numero personale</span></span>
  
<span data-ttu-id="35269-313">личный идентификатор нумеро</span><span class="sxs-lookup"><span data-stu-id="35269-313">numero id personale</span></span>
  
<span data-ttu-id="35269-314">личные коды для сокодовых костей</span><span class="sxs-lookup"><span data-stu-id="35269-314">codice id personale</span></span>
  
<span data-ttu-id="35269-315">финансовый отчет по сокостям</span><span class="sxs-lookup"><span data-stu-id="35269-315">codice fiscale</span></span>
  
## <a name="italy"></a><span data-ttu-id="35269-316">Италия</span><span class="sxs-lookup"><span data-stu-id="35269-316">Italy</span></span>

### <a name="format"></a><span data-ttu-id="35269-317">Format</span><span class="sxs-lookup"><span data-stu-id="35269-317">Format</span></span>

<span data-ttu-id="35269-318">11 цифр и дефис в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="35269-318">11 digits and a hyphen in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-319">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-319">Pattern</span></span>

<span data-ttu-id="35269-320">11 цифр и дефис:</span><span class="sxs-lookup"><span data-stu-id="35269-320">11 digits and a hyphen:</span></span>
  
-  <span data-ttu-id="35269-321">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="35269-321">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="35269-322">дефис;</span><span class="sxs-lookup"><span data-stu-id="35269-322">A hyphen</span></span>
    
- <span data-ttu-id="35269-323">Одна цифра, соответствующая столетию рождения ("0" для 19 века, "1" для 20-й век) и "2" для 21 века)</span><span class="sxs-lookup"><span data-stu-id="35269-323">One digit that corresponds to the century of birth ("0" for 19th century, "1" for 20th century, and "2" for 21st century)</span></span>
    
- <span data-ttu-id="35269-324">Четыре цифры, созданные случайным образом</span><span class="sxs-lookup"><span data-stu-id="35269-324">Four digits, randomly generated</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-325">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-325">Checksum</span></span>

<span data-ttu-id="35269-326">Да</span><span class="sxs-lookup"><span data-stu-id="35269-326">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-327">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-327">Definition</span></span>

<span data-ttu-id="35269-328">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-328">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-329">Функция `Func_latvia_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-329">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-330">Найдено ключевое `Keywords_latvia_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-330">A keyword from  `Keywords_latvia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-331">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-331">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-332">Функция `Func_latvia_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-332">The function  `Func_latvia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-333">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-333">Keywords</span></span>

#### <a name="keywordslatviaeunationalidcard"></a><span data-ttu-id="35269-334">Кэйвордс_латвиа_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-334">Keywords_latvia_eu_national_id_card</span></span>

<span data-ttu-id="35269-335">персональный код</span><span class="sxs-lookup"><span data-stu-id="35269-335">personal code</span></span>
  
<span data-ttu-id="35269-336">номер личного кода</span><span class="sxs-lookup"><span data-stu-id="35269-336">personal code number</span></span>
  
<span data-ttu-id="35269-337">личный номер сертификата</span><span class="sxs-lookup"><span data-stu-id="35269-337">personal certificate number</span></span>
  
<span data-ttu-id="35269-338">персоналкодено #</span><span class="sxs-lookup"><span data-stu-id="35269-338">personalcodeno#</span></span>
  
<span data-ttu-id="35269-339">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-339">personal id number</span></span>
  
<span data-ttu-id="35269-340">личный код</span><span class="sxs-lookup"><span data-stu-id="35269-340">personal id code</span></span>
  
<span data-ttu-id="35269-341">Пользователи Кодс</span><span class="sxs-lookup"><span data-stu-id="35269-341">personas kods</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="35269-342">Литва</span><span class="sxs-lookup"><span data-stu-id="35269-342">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="35269-343">Format</span><span class="sxs-lookup"><span data-stu-id="35269-343">Format</span></span>

<span data-ttu-id="35269-344">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-344">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-345">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-345">Pattern</span></span>

<span data-ttu-id="35269-346">11 цифр без пробелов и разделителей:</span><span class="sxs-lookup"><span data-stu-id="35269-346">11 digits without spaces and delimiters:</span></span>
  
- <span data-ttu-id="35269-347">Одна цифра, соответствующая пол и век рождения человека</span><span class="sxs-lookup"><span data-stu-id="35269-347">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="35269-348">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="35269-348">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="35269-349">Три цифры, которые соответствуют серийному числу даты рождения.</span><span class="sxs-lookup"><span data-stu-id="35269-349">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="35269-350">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="35269-350">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-351">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-351">Checksum</span></span>

<span data-ttu-id="35269-352">Да</span><span class="sxs-lookup"><span data-stu-id="35269-352">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-353">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-353">Definition</span></span>

<span data-ttu-id="35269-354">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-354">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-355">Функция `Func_lithuania_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-355">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-356">Найдено ключевое `Keywords_lithuania_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-356">A keyword from  `Keywords_lithuania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-357">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-358">Функция `Func_lithuania_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-358">The function  `Func_lithuania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-359">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-359">Keywords</span></span>

#### <a name="keywordslithuaniaeunationalidcard"></a><span data-ttu-id="35269-360">Кэйвордс_лисуаниа_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-360">Keywords_lithuania_eu_national_id_card</span></span>

<span data-ttu-id="35269-361">персональный числовой код</span><span class="sxs-lookup"><span data-stu-id="35269-361">personal numeric code</span></span>
  
<span data-ttu-id="35269-362">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-362">unique identification number</span></span>
  
<span data-ttu-id="35269-363">номер службы для себя</span><span class="sxs-lookup"><span data-stu-id="35269-363">citizen service number</span></span>
  
<span data-ttu-id="35269-364">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-364">unique identity number</span></span>
  
<span data-ttu-id="35269-365">уникуеидентитино #</span><span class="sxs-lookup"><span data-stu-id="35269-365">uniqueidentityno#</span></span>
  
<span data-ttu-id="35269-366">персональный код.</span><span class="sxs-lookup"><span data-stu-id="35269-366">personal code.</span></span>
  
<span data-ttu-id="35269-367">асменинис скаитменинис кодас</span><span class="sxs-lookup"><span data-stu-id="35269-367">asmeninis skaitmeninis kodas</span></span>
  
<span data-ttu-id="35269-368">уникалус идентификавимо нумерис</span><span class="sxs-lookup"><span data-stu-id="35269-368">unikalus identifikavimo numeris</span></span>
  
<span data-ttu-id="35269-369">пилиеčио паслаугос нумерис</span><span class="sxs-lookup"><span data-stu-id="35269-369">piliečio paslaugos numeris</span></span>
  
<span data-ttu-id="35269-370">уникалус идентификавимо кодас</span><span class="sxs-lookup"><span data-stu-id="35269-370">unikalus identifikavimo kodas</span></span>
  
<span data-ttu-id="35269-371">асменс кодас.</span><span class="sxs-lookup"><span data-stu-id="35269-371">asmens kodas.</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="35269-372">Луксембург</span><span class="sxs-lookup"><span data-stu-id="35269-372">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="35269-373">Format</span><span class="sxs-lookup"><span data-stu-id="35269-373">Format</span></span>

<span data-ttu-id="35269-374">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-375">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-375">Pattern</span></span>

<span data-ttu-id="35269-376">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="35269-376">11 digits</span></span>
  
- <span data-ttu-id="35269-377">Одна цифра, соответствующая пол и век рождения человека</span><span class="sxs-lookup"><span data-stu-id="35269-377">One digit that corresponds to the person's gender and century of birth</span></span>
    
-  <span data-ttu-id="35269-378">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="35269-378">Six digits that correspond to birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="35269-379">Три цифры, которые соответствуют серийному числу даты рождения.</span><span class="sxs-lookup"><span data-stu-id="35269-379">Three digits that correspond to the serial number of the date of birth</span></span>
    
- <span data-ttu-id="35269-380">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="35269-380">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-381">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-381">Checksum</span></span>

<span data-ttu-id="35269-382">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="35269-382">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-383">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-383">Definition</span></span>

<span data-ttu-id="35269-384">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-384">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-385">Регулярное выражение `Regex_luxemburg_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-385">The regular expression  `Regex_luxemburg_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-386">Найдено ключевое `Keywords_luxemburg_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-386">A keyword from  `Keywords_luxemburg_eu_national_id_card` is found.</span></span> 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="35269-387">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-387">Keywords</span></span>

#### <a name="keywordsluxemburgeunationalidcard"></a><span data-ttu-id="35269-388">Кэйвордс_луксембург_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-388">Keywords_luxemburg_eu_national_id_card</span></span>

<span data-ttu-id="35269-389">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="35269-389">personal id</span></span>
  
<span data-ttu-id="35269-390">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-390">personal id number</span></span>
  
<span data-ttu-id="35269-391">персоналидно #</span><span class="sxs-lookup"><span data-stu-id="35269-391">personalidno#</span></span>
  
<span data-ttu-id="35269-392">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-392">unique id number</span></span>
  
<span data-ttu-id="35269-393">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="35269-393">personalidnumber#</span></span>
  
<span data-ttu-id="35269-394">уникальный ключ идентификатора</span><span class="sxs-lookup"><span data-stu-id="35269-394">unique id key</span></span>
  
<span data-ttu-id="35269-395">личный код</span><span class="sxs-lookup"><span data-stu-id="35269-395">personal id code</span></span>
  
<span data-ttu-id="35269-396">уникуеидкэй #</span><span class="sxs-lookup"><span data-stu-id="35269-396">uniqueidkey#</span></span>
  
<span data-ttu-id="35269-397">отдельный код</span><span class="sxs-lookup"><span data-stu-id="35269-397">individual code</span></span>
  
<span data-ttu-id="35269-398">индивидуальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="35269-398">individual id</span></span>
  
<span data-ttu-id="35269-399">Идентификатор еиндеутиже — нуммер</span><span class="sxs-lookup"><span data-stu-id="35269-399">eindeutige id-nummer</span></span>
  
<span data-ttu-id="35269-400">Идентификатор еиндеутиже</span><span class="sxs-lookup"><span data-stu-id="35269-400">eindeutige id</span></span>
  
<span data-ttu-id="35269-401">ID персоннелле</span><span class="sxs-lookup"><span data-stu-id="35269-401">id personnelle</span></span>
  
<span data-ttu-id="35269-402">нумéро д'идентификатион сотрудники</span><span class="sxs-lookup"><span data-stu-id="35269-402">numéro d'identification personnel</span></span>
  
<span data-ttu-id="35269-403">идперсоннелле #</span><span class="sxs-lookup"><span data-stu-id="35269-403">idpersonnelle#</span></span>
  
<span data-ttu-id="35269-404">персöнличе идентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="35269-404">persönliche identifikationsnummer</span></span>
  
<span data-ttu-id="35269-405">еиндеутижеид #</span><span class="sxs-lookup"><span data-stu-id="35269-405">eindeutigeid#</span></span>
  
## <a name="malta"></a><span data-ttu-id="35269-406">Мальта</span><span class="sxs-lookup"><span data-stu-id="35269-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="35269-407">Format</span><span class="sxs-lookup"><span data-stu-id="35269-407">Format</span></span>

<span data-ttu-id="35269-408">Семь цифр, за которыми следует одна буква</span><span class="sxs-lookup"><span data-stu-id="35269-408">Seven digits followed by one letter</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-409">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-409">Pattern</span></span>

<span data-ttu-id="35269-410">Семь цифр, за которыми следует одна буква:</span><span class="sxs-lookup"><span data-stu-id="35269-410">Seven digits followed by one letter:</span></span>
  
-  <span data-ttu-id="35269-411">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="35269-411">Seven digits</span></span> 
    
- <span data-ttu-id="35269-412">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="35269-412">One uppercase letter (case sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-413">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-413">Checksum</span></span>

<span data-ttu-id="35269-414">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="35269-414">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-415">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-415">Definition</span></span>

<span data-ttu-id="35269-416">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-416">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-417">Регулярное выражение `Regex_malta_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-417">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-418">Найдено ключевое `Keywords_malta_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-418">A keyword from  `Keywords_malta_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-419">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-419">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-420">Регулярное выражение `Regex_malta_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-420">The regular expression  `Regex_malta_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-421">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-421">Keywords</span></span>

#### <a name="keywordsmaltaeunationalidcard"></a><span data-ttu-id="35269-422">Кэйвордс_малта_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-422">Keywords_malta_eu_national_id_card</span></span>

<span data-ttu-id="35269-423">персональный числовой код</span><span class="sxs-lookup"><span data-stu-id="35269-423">personal numeric code</span></span>
  
<span data-ttu-id="35269-424">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-424">unique identification number</span></span>
  
<span data-ttu-id="35269-425">номер службы для себя</span><span class="sxs-lookup"><span data-stu-id="35269-425">citizen service number</span></span>
  
<span data-ttu-id="35269-426">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-426">unique identity number</span></span>
  
<span data-ttu-id="35269-427">уникуеидентитино #</span><span class="sxs-lookup"><span data-stu-id="35269-427">uniqueidentityno#</span></span>
  
<span data-ttu-id="35269-428">кодиċи нумерали персонали</span><span class="sxs-lookup"><span data-stu-id="35269-428">kodiċi numerali personali</span></span>
  
<span data-ttu-id="35269-429">нумру Ta ' идентификаззжони унику</span><span class="sxs-lookup"><span data-stu-id="35269-429">numru ta 'identifikazzjoni uniku</span></span>
  
<span data-ttu-id="35269-430">нумруные зада сервизз таċ ċиттадин</span><span class="sxs-lookup"><span data-stu-id="35269-430">numru tas-servizz taċ-ċittadin</span></span>
  
<span data-ttu-id="35269-431">нумру Ta ' идентитà унику</span><span class="sxs-lookup"><span data-stu-id="35269-431">numru ta' identità uniku</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="35269-432">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="35269-432">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="35269-433">Format</span><span class="sxs-lookup"><span data-stu-id="35269-433">Format</span></span>

<span data-ttu-id="35269-434">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-434">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-435">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-435">Pattern</span></span>

<span data-ttu-id="35269-436">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="35269-436">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="35269-437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-437">Checksum</span></span>

<span data-ttu-id="35269-438">Да</span><span class="sxs-lookup"><span data-stu-id="35269-438">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-439">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-439">Definition</span></span>

<span data-ttu-id="35269-440">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-440">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-441">Функция `Func_netherlands_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-441">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-442">Найдено ключевое слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-442">A keyword from is found.</span></span>
    
<span data-ttu-id="35269-443">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-443">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-444">Функция `Func_netherlands_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-444">The function  `Func_netherlands_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-445">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-445">Keywords</span></span>

#### <a name="keywordsnetherlandseunationalidcard"></a><span data-ttu-id="35269-446">Кэйвордс_несерландс_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-446">Keywords_netherlands_eu_national_id_card</span></span>

<span data-ttu-id="35269-447">персональный числовой код</span><span class="sxs-lookup"><span data-stu-id="35269-447">personal numeric code</span></span>
  
<span data-ttu-id="35269-448">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-448">unique identification number</span></span>
  
<span data-ttu-id="35269-449">номер службы для себя</span><span class="sxs-lookup"><span data-stu-id="35269-449">citizen service number</span></span>
  
<span data-ttu-id="35269-450">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-450">unique identity number</span></span>
  
<span data-ttu-id="35269-451">уникуеидентитино #</span><span class="sxs-lookup"><span data-stu-id="35269-451">uniqueidentityno#</span></span>
  
<span data-ttu-id="35269-452">BSN</span><span class="sxs-lookup"><span data-stu-id="35269-452">bsn</span></span>
  
<span data-ttu-id="35269-453">BSN</span><span class="sxs-lookup"><span data-stu-id="35269-453">bsn#</span></span>
  
<span data-ttu-id="35269-454">персунлижке нумериеке код</span><span class="sxs-lookup"><span data-stu-id="35269-454">persoonlijke numerieke code</span></span>
  
<span data-ttu-id="35269-455">униек идентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="35269-455">uniek identificatienummer</span></span>
  
<span data-ttu-id="35269-456">буржерсервиценуммер</span><span class="sxs-lookup"><span data-stu-id="35269-456">burgerservicenummer</span></span>
  
<span data-ttu-id="35269-457">униек идентитеитснуммер</span><span class="sxs-lookup"><span data-stu-id="35269-457">uniek identiteitsnummer</span></span>
  
## <a name="poland"></a><span data-ttu-id="35269-458">Польша</span><span class="sxs-lookup"><span data-stu-id="35269-458">Poland</span></span>

<span data-ttu-id="35269-459">Дополнительные сведения см. в разделе "Польша National ID (PESEL)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-459">For details, see the section "Poland National ID (PESEL)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="35269-460">Португалия</span><span class="sxs-lookup"><span data-stu-id="35269-460">Portugal</span></span>

<span data-ttu-id="35269-461">Дополнительные сведения можно найти в разделе "номер карты для Португалия" в разделе [сведения о типах конфиденциальной информации для поиска](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-461">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="romania"></a><span data-ttu-id="35269-462">Румыния</span><span class="sxs-lookup"><span data-stu-id="35269-462">Romania</span></span>

### <a name="format"></a><span data-ttu-id="35269-463">Format</span><span class="sxs-lookup"><span data-stu-id="35269-463">Format</span></span>

<span data-ttu-id="35269-464">13 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-464">13 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-465">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-465">Pattern</span></span>

<span data-ttu-id="35269-466">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="35269-466">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="35269-467">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-467">Checksum</span></span>

<span data-ttu-id="35269-468">Да</span><span class="sxs-lookup"><span data-stu-id="35269-468">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-469">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-469">Definition</span></span>

<span data-ttu-id="35269-470">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-471">Функция `Func_romania_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-471">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-472">Найдено ключевое `Keywords_romania_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-472">A keyword from  `Keywords_romania_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-473">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-473">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-474">Функция `Func_romania_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-474">The function  `Func_romania_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-475">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-475">Keywords</span></span>

#### <a name="keywordsromaniaeunationalidcard"></a><span data-ttu-id="35269-476">Кэйвордс_романиа_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-476">Keywords_romania_eu_national_id_card</span></span>

<span data-ttu-id="35269-477">персональный числовой код</span><span class="sxs-lookup"><span data-stu-id="35269-477">personal numeric code</span></span>
  
<span data-ttu-id="35269-478">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-478">unique identification number</span></span>
  
<span data-ttu-id="35269-479">КНП</span><span class="sxs-lookup"><span data-stu-id="35269-479">cnp</span></span>
  
<span data-ttu-id="35269-480">КНП #</span><span class="sxs-lookup"><span data-stu-id="35269-480">cnp#</span></span>
  
<span data-ttu-id="35269-481">крепления</span><span class="sxs-lookup"><span data-stu-id="35269-481">pin</span></span>
  
<span data-ttu-id="35269-482">крепления</span><span class="sxs-lookup"><span data-stu-id="35269-482">pin#</span></span>
  
<span data-ttu-id="35269-483">страховой номер</span><span class="sxs-lookup"><span data-stu-id="35269-483">insurance number</span></span>
  
<span data-ttu-id="35269-484">инсуранценумбер #</span><span class="sxs-lookup"><span data-stu-id="35269-484">insurancenumber#</span></span>
  
<span data-ttu-id="35269-485">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-485">unique identity number</span></span>
  
<span data-ttu-id="35269-486">уникуеидентитино #</span><span class="sxs-lookup"><span data-stu-id="35269-486">uniqueidentityno#</span></span>
  
<span data-ttu-id="35269-487">цифровой платеж, персональный</span><span class="sxs-lookup"><span data-stu-id="35269-487">cod numeric personal</span></span>
  
<span data-ttu-id="35269-488">Личный идентификаре наложенного платежа</span><span class="sxs-lookup"><span data-stu-id="35269-488">cod identificare personal</span></span>
  
<span data-ttu-id="35269-489">наложенный Уник идентификаре</span><span class="sxs-lookup"><span data-stu-id="35269-489">cod unic identificare</span></span>
  
<span data-ttu-id="35269-490">нумăр Personal Уник</span><span class="sxs-lookup"><span data-stu-id="35269-490">număr personal unic</span></span>
  
<span data-ttu-id="35269-491">нумăр идентитате</span><span class="sxs-lookup"><span data-stu-id="35269-491">număr identitate</span></span>
  
<span data-ttu-id="35269-492">нумăр идентификаре персональный</span><span class="sxs-lookup"><span data-stu-id="35269-492">număr identificare personal</span></span>
  
<span data-ttu-id="35269-493">нумăридентитате #</span><span class="sxs-lookup"><span data-stu-id="35269-493">număridentitate#</span></span>
  
<span data-ttu-id="35269-494">коднумерикперсонал #</span><span class="sxs-lookup"><span data-stu-id="35269-494">codnumericpersonal#</span></span>
  
<span data-ttu-id="35269-495">нумăрперсоналуник #</span><span class="sxs-lookup"><span data-stu-id="35269-495">numărpersonalunic#</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="35269-496">Словакия</span><span class="sxs-lookup"><span data-stu-id="35269-496">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="35269-497">Format</span><span class="sxs-lookup"><span data-stu-id="35269-497">Format</span></span>

<span data-ttu-id="35269-498">Десять цифр, содержащих одну обратную косую черту;</span><span class="sxs-lookup"><span data-stu-id="35269-498">Ten digits containing one backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-499">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-499">Pattern</span></span>

<span data-ttu-id="35269-500">Десять цифр, содержащих одну обратную косую черту:</span><span class="sxs-lookup"><span data-stu-id="35269-500">Ten digits containing one backslash:</span></span>
  
### <a name="checksum"></a><span data-ttu-id="35269-501">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-501">Checksum</span></span>

<span data-ttu-id="35269-502">Да</span><span class="sxs-lookup"><span data-stu-id="35269-502">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-503">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-503">Definition</span></span>

<span data-ttu-id="35269-504">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-504">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-505">Функция `Func_slovakia_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-505">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-506">Найдено ключевое `Keywords_slovakia_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-506">A keyword from  `Keywords_slovakia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-507">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-507">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-508">Функция `Func_slovakia_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-508">The function  `Func_slovakia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-509">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-509">Keywords</span></span>

#### <a name="keywordsslovakiaeunationalidcard"></a><span data-ttu-id="35269-510">Кэйвордс_словакиа_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-510">Keywords_slovakia_eu_national_id_card</span></span>

<span data-ttu-id="35269-511">номер рождения</span><span class="sxs-lookup"><span data-stu-id="35269-511">birth number</span></span>
  
<span data-ttu-id="35269-512">national identification number</span><span class="sxs-lookup"><span data-stu-id="35269-512">national identification number</span></span>
  
<span data-ttu-id="35269-513">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-513">personal identification number</span></span>
  
<span data-ttu-id="35269-514">social security number</span><span class="sxs-lookup"><span data-stu-id="35269-514">social security number</span></span>
  
<span data-ttu-id="35269-515">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="35269-515">nationalnumber#</span></span>
  
<span data-ttu-id="35269-516">SSN</span><span class="sxs-lookup"><span data-stu-id="35269-516">ssn#</span></span>
  
<span data-ttu-id="35269-517">SSN</span><span class="sxs-lookup"><span data-stu-id="35269-517">ssn</span></span>
  
<span data-ttu-id="35269-518">номер страны</span><span class="sxs-lookup"><span data-stu-id="35269-518">national number</span></span>
  
<span data-ttu-id="35269-519">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-519">personal id number</span></span>
  
<span data-ttu-id="35269-520">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="35269-520">personalidnumber#</span></span>
  
<span data-ttu-id="35269-521">рč</span><span class="sxs-lookup"><span data-stu-id="35269-521">rč</span></span>
  
<span data-ttu-id="35269-522">роднé číсло</span><span class="sxs-lookup"><span data-stu-id="35269-522">rodné číslo</span></span>
  
<span data-ttu-id="35269-523">родне Цисло</span><span class="sxs-lookup"><span data-stu-id="35269-523">rodne cislo</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="35269-524">Словения</span><span class="sxs-lookup"><span data-stu-id="35269-524">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="35269-525">Format</span><span class="sxs-lookup"><span data-stu-id="35269-525">Format</span></span>

<span data-ttu-id="35269-526">13 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="35269-526">13 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-527">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-527">Pattern</span></span>

<span data-ttu-id="35269-528">13 цифр в указанном шаблоне:</span><span class="sxs-lookup"><span data-stu-id="35269-528">13 digits in the specified pattern:</span></span>
  
-  <span data-ttu-id="35269-529">Семь цифр, которые соответствуют дате рождения (ДДММЛЛЛ), где "ЛЛЛ" соответствует последним трем цифрам года рождения</span><span class="sxs-lookup"><span data-stu-id="35269-529">Seven digits that correspond to the birth date (DDMMLLL) where "LLL" corresponds to the last three digits of the birth year</span></span> 
    
- <span data-ttu-id="35269-530">Две цифры, соответствующие области рождения</span><span class="sxs-lookup"><span data-stu-id="35269-530">Two digits that correspond to the area of birth</span></span>
    
- <span data-ttu-id="35269-531">Три цифры, которые соответствуют сочетанию пола и серийного номера для людей, которые приставили один и тот же день (000-499 для пола и 500-999 для розетки)</span><span class="sxs-lookup"><span data-stu-id="35269-531">Three digits that correspond to a combination of gender and serial number for persons born on the same day (000-499 for male and 500-999 for female)</span></span>
    
- <span data-ttu-id="35269-532">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="35269-532">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-533">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-533">Checksum</span></span>

<span data-ttu-id="35269-534">Да</span><span class="sxs-lookup"><span data-stu-id="35269-534">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-535">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-535">Definition</span></span>

<span data-ttu-id="35269-536">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-536">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-537">Функция `Func_slovenia_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-537">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-538">Найдено ключевое `Keywords_slovenia_eu_national_id_card` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-538">A keyword from  `Keywords_slovenia_eu_national_id_card` is found.</span></span> 
    
<span data-ttu-id="35269-539">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-540">Функция `Func_slovenia_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-540">The function  `Func_slovenia_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="35269-541">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-541">Keywords</span></span>

#### <a name="keywordssloveniaeunationalidcard"></a><span data-ttu-id="35269-542">Кэйвордс_словениа_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-542">Keywords_slovenia_eu_national_id_card</span></span>

<span data-ttu-id="35269-543">персональный числовой код</span><span class="sxs-lookup"><span data-stu-id="35269-543">personal numeric code</span></span>
  
<span data-ttu-id="35269-544">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-544">unique identification number</span></span>
  
<span data-ttu-id="35269-545">уникальный регистрационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-545">unique registration number</span></span>
  
<span data-ttu-id="35269-546">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-546">unique identity number</span></span>
  
<span data-ttu-id="35269-547">уникуеидентитино #</span><span class="sxs-lookup"><span data-stu-id="35269-547">uniqueidentityno#</span></span>
  
<span data-ttu-id="35269-548">уникальный основной номер</span><span class="sxs-lookup"><span data-stu-id="35269-548">unique master citizen number</span></span>
  
<span data-ttu-id="35269-549">единствена идентификаЦижска šтевилка</span><span class="sxs-lookup"><span data-stu-id="35269-549">edinstvena identifikacijska številka</span></span>
  
<span data-ttu-id="35269-550">уникуеидентитино #</span><span class="sxs-lookup"><span data-stu-id="35269-550">uniqueidentityno #</span></span>
  
<span data-ttu-id="35269-551">единствена šтевилка главнега дрžавлжана</span><span class="sxs-lookup"><span data-stu-id="35269-551">edinstvena številka glavnega državljana</span></span>
  
<span data-ttu-id="35269-552">емšо</span><span class="sxs-lookup"><span data-stu-id="35269-552">emšo</span></span>
  
## <a name="spain"></a><span data-ttu-id="35269-553">Испания</span><span class="sxs-lookup"><span data-stu-id="35269-553">Spain</span></span>

### <a name="format"></a><span data-ttu-id="35269-554">Format</span><span class="sxs-lookup"><span data-stu-id="35269-554">Format</span></span>

<span data-ttu-id="35269-555">Семь цифр, за которыми следует один символ</span><span class="sxs-lookup"><span data-stu-id="35269-555">Seven digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="35269-556">Шаблон</span><span class="sxs-lookup"><span data-stu-id="35269-556">Pattern</span></span>

<span data-ttu-id="35269-557">Семь цифр, за которыми следует один символ</span><span class="sxs-lookup"><span data-stu-id="35269-557">Seven digits followed by one character</span></span>
  
- <span data-ttu-id="35269-558">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="35269-558">Seven digits</span></span>
    
- <span data-ttu-id="35269-559">Одна цифра или буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="35269-559">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="35269-560">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="35269-560">Checksum</span></span>

<span data-ttu-id="35269-561">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="35269-561">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="35269-562">Определение</span><span class="sxs-lookup"><span data-stu-id="35269-562">Definition</span></span>

<span data-ttu-id="35269-563">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="35269-563">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="35269-564">Регулярное выражение `Regex_spain_eu_national_id_card` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="35269-564">The regular expression  `Regex_spain_eu_national_id_card` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="35269-565">Найдено ключевое `Keywords_spain_eu_national_id_card"` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="35269-565">A keyword from  `Keywords_spain_eu_national_id_card"` is found.</span></span> 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="35269-566">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="35269-566">Keywords</span></span>

#### <a name="keywordsspaineunationalidcard"></a><span data-ttu-id="35269-567">Кэйвордс_спаин_еу_натионал_ид_кард</span><span class="sxs-lookup"><span data-stu-id="35269-567">Keywords_spain_eu_national_id_card</span></span>

<span data-ttu-id="35269-568">DNI</span><span class="sxs-lookup"><span data-stu-id="35269-568">dni</span></span>
  
<span data-ttu-id="35269-569">national identification number</span><span class="sxs-lookup"><span data-stu-id="35269-569">national identification number</span></span>
  
<span data-ttu-id="35269-570">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-570">national identity number</span></span>
  
<span data-ttu-id="35269-571">страховой номер</span><span class="sxs-lookup"><span data-stu-id="35269-571">insurance number</span></span>
  
<span data-ttu-id="35269-572">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-572">personal identification number</span></span>
  
<span data-ttu-id="35269-573">Национальная идентификация</span><span class="sxs-lookup"><span data-stu-id="35269-573">national identity</span></span>
  
<span data-ttu-id="35269-574">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="35269-574">personal identity no</span></span>
  
<span data-ttu-id="35269-575">уникальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="35269-575">unique identity number</span></span>
  
<span data-ttu-id="35269-576">натионалидно #</span><span class="sxs-lookup"><span data-stu-id="35269-576">nationalidno#</span></span>
  
<span data-ttu-id="35269-577">уникальным</span><span class="sxs-lookup"><span data-stu-id="35269-577">uniqueid#</span></span>
  
<span data-ttu-id="35269-578">DNI</span><span class="sxs-lookup"><span data-stu-id="35269-578">dni#</span></span>
  
<span data-ttu-id="35269-579">натионалид #</span><span class="sxs-lookup"><span data-stu-id="35269-579">nationalid#</span></span>
  
<span data-ttu-id="35269-580">ние #</span><span class="sxs-lookup"><span data-stu-id="35269-580">nie#</span></span>
  
<span data-ttu-id="35269-581">ние</span><span class="sxs-lookup"><span data-stu-id="35269-581">nie</span></span>
  
<span data-ttu-id="35269-582">ниенúмеро #</span><span class="sxs-lookup"><span data-stu-id="35269-582">nienúmero#</span></span>
  
<span data-ttu-id="35269-583">ние нúмеро</span><span class="sxs-lookup"><span data-stu-id="35269-583">nie número</span></span>
  
<span data-ttu-id="35269-584">документо наЦионал де ИДЕНТИДАД</span><span class="sxs-lookup"><span data-stu-id="35269-584">documento nacional de identidad</span></span>
  
<span data-ttu-id="35269-585">ИДЕНТИДАД úнико</span><span class="sxs-lookup"><span data-stu-id="35269-585">identidad único</span></span>
  
<span data-ttu-id="35269-586">нúмеро наЦионал ИДЕНТИДАД</span><span class="sxs-lookup"><span data-stu-id="35269-586">número nacional identidad</span></span>
  
<span data-ttu-id="35269-587">DNI нúмеро</span><span class="sxs-lookup"><span data-stu-id="35269-587">dni número</span></span>
  
<span data-ttu-id="35269-588">днинúмеро #</span><span class="sxs-lookup"><span data-stu-id="35269-588">dninúmero#</span></span>
  
<span data-ttu-id="35269-589">идентидадúнико #</span><span class="sxs-lookup"><span data-stu-id="35269-589">identidadúnico#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="35269-590">Швеция</span><span class="sxs-lookup"><span data-stu-id="35269-590">Sweden</span></span>

<span data-ttu-id="35269-591">Для получения дополнительных сведений обратитесь к разделу "Швеции National ID", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="35269-591">For details, see the section "Sweden National ID" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="35269-592">См. также</span><span class="sxs-lookup"><span data-stu-id="35269-592">See also</span></span>

[<span data-ttu-id="35269-593">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="35269-593">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

