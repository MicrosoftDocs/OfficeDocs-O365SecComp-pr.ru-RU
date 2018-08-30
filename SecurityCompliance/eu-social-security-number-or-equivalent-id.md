---
title: Страховой номер для ЕС или иметь эквивалентные права идентификатор
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении страховой номер для ЕС или эквивалентный код тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534728"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="84452-104">Страховой номер для ЕС или иметь эквивалентные права идентификатор</span><span class="sxs-lookup"><span data-stu-id="84452-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="84452-p102">В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении ЕС страховой номер (SSN) или эквивалентный код тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="84452-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="84452-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="84452-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="84452-108">Формат</span><span class="sxs-lookup"><span data-stu-id="84452-108">Format</span></span>

<span data-ttu-id="84452-109">10 цифр в указанном формате</span><span class="sxs-lookup"><span data-stu-id="84452-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="84452-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="84452-110">Pattern</span></span>

<span data-ttu-id="84452-111">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="84452-111">10 digits:</span></span>
  
-  <span data-ttu-id="84452-112">Три цифры, которые соответствуют серийный номер</span><span class="sxs-lookup"><span data-stu-id="84452-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="84452-113">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="84452-113">One check digit</span></span>
    
- <span data-ttu-id="84452-114">Шести цифр, которые соответствуют Дата рождения (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="84452-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="84452-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="84452-115">Checksum</span></span>

<span data-ttu-id="84452-116">Да</span><span class="sxs-lookup"><span data-stu-id="84452-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="84452-117">Определение</span><span class="sxs-lookup"><span data-stu-id="84452-117">Definition</span></span>

<span data-ttu-id="84452-118">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-119">Функция `Func_austria_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="84452-120">Ключевое слово из `Keywords_austria_eu_ssn_or_equivalent` найден.</span><span class="sxs-lookup"><span data-stu-id="84452-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="84452-121">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-122">Функция `Func_austria_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="84452-123">Keywords</span><span class="sxs-lookup"><span data-stu-id="84452-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="84452-124">Keywords_austria_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="84452-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="84452-125">социального страхования нет</span><span class="sxs-lookup"><span data-stu-id="84452-125">social security no</span></span>
  
<span data-ttu-id="84452-126">social security number
</span><span class="sxs-lookup"><span data-stu-id="84452-126">social security number</span></span>
  
<span data-ttu-id="84452-127">
social security code</span><span class="sxs-lookup"><span data-stu-id="84452-127">social security code</span></span>
  
<span data-ttu-id="84452-128">страховой номер</span><span class="sxs-lookup"><span data-stu-id="84452-128">insurance number</span></span>
  
<span data-ttu-id="84452-129">Австрия ssn</span><span class="sxs-lookup"><span data-stu-id="84452-129">austrian ssn</span></span>
  
<span data-ttu-id="84452-130">SSN #</span><span class="sxs-lookup"><span data-stu-id="84452-130">ssn#</span></span>
  
<span data-ttu-id="84452-131">SSN</span><span class="sxs-lookup"><span data-stu-id="84452-131">ssn</span></span>
  
<span data-ttu-id="84452-132">страховой кода</span><span class="sxs-lookup"><span data-stu-id="84452-132">insurance code</span></span>
  
<span data-ttu-id="84452-133">страховой код #</span><span class="sxs-lookup"><span data-stu-id="84452-133">insurance code#</span></span>
  
<span data-ttu-id="84452-134">socialsecurityno #</span><span class="sxs-lookup"><span data-stu-id="84452-134">socialsecurityno#</span></span>
  
<span data-ttu-id="84452-135">sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="84452-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="84452-136">soziale sicherheit kein</span><span class="sxs-lookup"><span data-stu-id="84452-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="84452-137">versicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="84452-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="84452-138">Бельгия</span><span class="sxs-lookup"><span data-stu-id="84452-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="84452-139">Формат</span><span class="sxs-lookup"><span data-stu-id="84452-139">Format</span></span>

<span data-ttu-id="84452-140">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="84452-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="84452-141">Шаблон</span><span class="sxs-lookup"><span data-stu-id="84452-141">Pattern</span></span>

<span data-ttu-id="84452-142">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="84452-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="84452-143">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="84452-143">Checksum</span></span>

<span data-ttu-id="84452-144">Да</span><span class="sxs-lookup"><span data-stu-id="84452-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="84452-145">Определение</span><span class="sxs-lookup"><span data-stu-id="84452-145">Definition</span></span>

<span data-ttu-id="84452-146">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-147">Функция `Func_belgium_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="84452-148">Ключевое слово из `Keywords_belgium_eu_ssn_or_equivalent` найден.</span><span class="sxs-lookup"><span data-stu-id="84452-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="84452-149">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-150">Функция `Func_belgium_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="84452-151">Keywords</span><span class="sxs-lookup"><span data-stu-id="84452-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="84452-152">Keywords_belgium_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="84452-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="84452-153">Бельгия национальный номер</span><span class="sxs-lookup"><span data-stu-id="84452-153">belgian national number</span></span>
  
<span data-ttu-id="84452-154">Национальный номер</span><span class="sxs-lookup"><span data-stu-id="84452-154">national number</span></span>
  
<span data-ttu-id="84452-155">social security number
</span><span class="sxs-lookup"><span data-stu-id="84452-155">social security number</span></span>
  
<span data-ttu-id="84452-156">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-156">nationalnumber#</span></span>
  
<span data-ttu-id="84452-157">SSN #</span><span class="sxs-lookup"><span data-stu-id="84452-157">ssn#</span></span>
  
<span data-ttu-id="84452-158">SSN</span><span class="sxs-lookup"><span data-stu-id="84452-158">ssn</span></span>
  
<span data-ttu-id="84452-159">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="84452-159">nationalnumber</span></span>
  
<span data-ttu-id="84452-160">bnn #</span><span class="sxs-lookup"><span data-stu-id="84452-160">bnn#</span></span>
  
<span data-ttu-id="84452-161">bnn</span><span class="sxs-lookup"><span data-stu-id="84452-161">bnn</span></span>
  
<span data-ttu-id="84452-162">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="84452-162">personal id number</span></span>
  
<span data-ttu-id="84452-163">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-163">personalidnumber#</span></span>
  
<span data-ttu-id="84452-164">Национальный numéro</span><span class="sxs-lookup"><span data-stu-id="84452-164">numéro national</span></span>
  
<span data-ttu-id="84452-165">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="84452-165">numéro de sécurité</span></span>
  
<span data-ttu-id="84452-166">numéro d'assuré</span><span class="sxs-lookup"><span data-stu-id="84452-166">numéro d'assuré</span></span>
  
<span data-ttu-id="84452-167">Национальный identifiant</span><span class="sxs-lookup"><span data-stu-id="84452-167">identifiant national</span></span>
  
<span data-ttu-id="84452-168">identifiantnational #</span><span class="sxs-lookup"><span data-stu-id="84452-168">identifiantnational#</span></span>
  
<span data-ttu-id="84452-169">numéronational #</span><span class="sxs-lookup"><span data-stu-id="84452-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="84452-170">Хорватия</span><span class="sxs-lookup"><span data-stu-id="84452-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="84452-171">Формат</span><span class="sxs-lookup"><span data-stu-id="84452-171">Format</span></span>

<span data-ttu-id="84452-172">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="84452-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="84452-173">Шаблон</span><span class="sxs-lookup"><span data-stu-id="84452-173">Pattern</span></span>

 <span data-ttu-id="84452-174">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="84452-174">11 digits:</span></span> 
  
-  <span data-ttu-id="84452-175">10 цифр</span><span class="sxs-lookup"><span data-stu-id="84452-175">Ten digits</span></span> 
    
- <span data-ttu-id="84452-176">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="84452-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="84452-177">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="84452-177">Checksum</span></span>

<span data-ttu-id="84452-178">Да</span><span class="sxs-lookup"><span data-stu-id="84452-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="84452-179">Определение</span><span class="sxs-lookup"><span data-stu-id="84452-179">Definition</span></span>

<span data-ttu-id="84452-180">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-181">Функция `Func_croatia_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="84452-182">Ключевое слово из `Keywords_croatia_eu_ssn_or_equivalent` найден.</span><span class="sxs-lookup"><span data-stu-id="84452-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="84452-183">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-184">Функция `Func_croatia_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="84452-185">Keywords</span><span class="sxs-lookup"><span data-stu-id="84452-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="84452-186">Keywords_croatia_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="84452-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="84452-187">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="84452-187">personal identification number</span></span>
  
<span data-ttu-id="84452-188">Число главных граждан</span><span class="sxs-lookup"><span data-stu-id="84452-188">master citizen number</span></span>
  
<span data-ttu-id="84452-189">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="84452-189">national identification number</span></span>
  
<span data-ttu-id="84452-190">social security number
</span><span class="sxs-lookup"><span data-stu-id="84452-190">social security number</span></span>
  
<span data-ttu-id="84452-191">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-191">nationalnumber#</span></span>
  
<span data-ttu-id="84452-192">SSN #</span><span class="sxs-lookup"><span data-stu-id="84452-192">ssn#</span></span>
  
<span data-ttu-id="84452-193">SSN</span><span class="sxs-lookup"><span data-stu-id="84452-193">ssn</span></span>
  
<span data-ttu-id="84452-194">nationalnumber</span><span class="sxs-lookup"><span data-stu-id="84452-194">nationalnumber</span></span>
  
<span data-ttu-id="84452-195">bnn #</span><span class="sxs-lookup"><span data-stu-id="84452-195">bnn#</span></span>
  
<span data-ttu-id="84452-196">bnn</span><span class="sxs-lookup"><span data-stu-id="84452-196">bnn</span></span>
  
<span data-ttu-id="84452-197">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="84452-197">personal id number</span></span>
  
<span data-ttu-id="84452-198">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-198">personalidnumber#</span></span>
  
<span data-ttu-id="84452-199">oib</span><span class="sxs-lookup"><span data-stu-id="84452-199">oib</span></span>
  
<span data-ttu-id="84452-200">osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="84452-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="84452-201">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="84452-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="84452-202">Формат</span><span class="sxs-lookup"><span data-stu-id="84452-202">Format</span></span>

<span data-ttu-id="84452-203">10 цифр и обратная косая черта в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="84452-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="84452-204">Шаблон</span><span class="sxs-lookup"><span data-stu-id="84452-204">Pattern</span></span>

<span data-ttu-id="84452-205">10 цифр и обратную косую черту:</span><span class="sxs-lookup"><span data-stu-id="84452-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="84452-206">Шесть цифры, которые соответствуют Дата рождения (ГГММДД):</span><span class="sxs-lookup"><span data-stu-id="84452-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="84452-207">Обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="84452-207">A backslash</span></span>
    
- <span data-ttu-id="84452-208">Три цифры, которые соответствуют серийный номер, отделяющий лиц на тот же день рождения</span><span class="sxs-lookup"><span data-stu-id="84452-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="84452-209">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="84452-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="84452-210">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="84452-210">Checksum</span></span>

<span data-ttu-id="84452-211">Да</span><span class="sxs-lookup"><span data-stu-id="84452-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="84452-212">Определение</span><span class="sxs-lookup"><span data-stu-id="84452-212">Definition</span></span>

<span data-ttu-id="84452-213">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-214">Функция `Func_czech_republic_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="84452-215">Ключевое слово из `Keywords_czech_republic_eu_ssn_or_equivalent` найден.</span><span class="sxs-lookup"><span data-stu-id="84452-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="84452-216">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-217">Функция `Func_czech_republic_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="84452-218">Keywords</span><span class="sxs-lookup"><span data-stu-id="84452-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="84452-219">Keywords_czech_republic_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="84452-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="84452-220">Номер рождения</span><span class="sxs-lookup"><span data-stu-id="84452-220">birth number</span></span>
  
<span data-ttu-id="84452-221">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="84452-221">national identification number</span></span>
  
<span data-ttu-id="84452-222">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="84452-222">personal identification number</span></span>
  
<span data-ttu-id="84452-223">social security number
</span><span class="sxs-lookup"><span data-stu-id="84452-223">social security number</span></span>
  
<span data-ttu-id="84452-224">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-224">nationalnumber#</span></span>
  
<span data-ttu-id="84452-225">SSN #</span><span class="sxs-lookup"><span data-stu-id="84452-225">ssn#</span></span>
  
<span data-ttu-id="84452-226">SSN</span><span class="sxs-lookup"><span data-stu-id="84452-226">ssn</span></span>
  
<span data-ttu-id="84452-227">Национальный номер</span><span class="sxs-lookup"><span data-stu-id="84452-227">national number</span></span>
  
<span data-ttu-id="84452-228">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="84452-228">personal id number</span></span>
  
<span data-ttu-id="84452-229">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-229">personalidnumber#</span></span>
  
<span data-ttu-id="84452-230">rč</span><span class="sxs-lookup"><span data-stu-id="84452-230">rč</span></span>
  
<span data-ttu-id="84452-231">rodné číslo</span><span class="sxs-lookup"><span data-stu-id="84452-231">rodné číslo</span></span>
  
<span data-ttu-id="84452-232">rodne cislo</span><span class="sxs-lookup"><span data-stu-id="84452-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="84452-233">Дания</span><span class="sxs-lookup"><span data-stu-id="84452-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="84452-234">Формат</span><span class="sxs-lookup"><span data-stu-id="84452-234">Format</span></span>

<span data-ttu-id="84452-235">10 цифр и дефис в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="84452-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="84452-236">Шаблон</span><span class="sxs-lookup"><span data-stu-id="84452-236">Pattern</span></span>

<span data-ttu-id="84452-237">10 цифр и дефис:</span><span class="sxs-lookup"><span data-stu-id="84452-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="84452-238">Шести цифр, которые соответствуют Дата рождения (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="84452-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="84452-239">дефис;</span><span class="sxs-lookup"><span data-stu-id="84452-239">A hyphen</span></span>
    
- <span data-ttu-id="84452-240">Четыре цифры, которые соответствуют порядковый номер</span><span class="sxs-lookup"><span data-stu-id="84452-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="84452-241">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="84452-241">Checksum</span></span>

<span data-ttu-id="84452-242">Да</span><span class="sxs-lookup"><span data-stu-id="84452-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="84452-243">Определение</span><span class="sxs-lookup"><span data-stu-id="84452-243">Definition</span></span>

<span data-ttu-id="84452-244">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-245">Функция `Func_denmark_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="84452-246">Ключевое слово из `Keywords_denmark_eu_ssn_or_equivalent` найден.</span><span class="sxs-lookup"><span data-stu-id="84452-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="84452-247">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-248">Функция `Func_denmark_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="84452-249">Keywords</span><span class="sxs-lookup"><span data-stu-id="84452-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="84452-250">Keywords_denmark_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="84452-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="84452-251">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="84452-251">personal identification number</span></span>
  
<span data-ttu-id="84452-252">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="84452-252">national identification number</span></span>
  
<span data-ttu-id="84452-253">social security number
</span><span class="sxs-lookup"><span data-stu-id="84452-253">social security number</span></span>
  
<span data-ttu-id="84452-254">nationalnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-254">nationalnumber#</span></span>
  
<span data-ttu-id="84452-255">SSN #</span><span class="sxs-lookup"><span data-stu-id="84452-255">ssn#</span></span>
  
<span data-ttu-id="84452-256">SSN</span><span class="sxs-lookup"><span data-stu-id="84452-256">ssn</span></span>
  
<span data-ttu-id="84452-257">Национальный номер</span><span class="sxs-lookup"><span data-stu-id="84452-257">national number</span></span>
  
<span data-ttu-id="84452-258">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="84452-258">personal id number</span></span>
  
<span data-ttu-id="84452-259">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-259">personalidnumber#</span></span>
  
<span data-ttu-id="84452-260">CPR nummer</span><span class="sxs-lookup"><span data-stu-id="84452-260">cpr-nummer</span></span>
  
<span data-ttu-id="84452-261">personnummer</span><span class="sxs-lookup"><span data-stu-id="84452-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="84452-262">Финляндия</span><span class="sxs-lookup"><span data-stu-id="84452-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="84452-263">Формат</span><span class="sxs-lookup"><span data-stu-id="84452-263">Format</span></span>

<span data-ttu-id="84452-264">Комбинация 11 символов в указанном формате</span><span class="sxs-lookup"><span data-stu-id="84452-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="84452-265">Шаблон</span><span class="sxs-lookup"><span data-stu-id="84452-265">Pattern</span></span>

<span data-ttu-id="84452-266">Комбинация 11 символов в указанном формате:</span><span class="sxs-lookup"><span data-stu-id="84452-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="84452-267">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="84452-267">Six digits</span></span> 
    
- <span data-ttu-id="84452-268">Один экземпляр одно из следующих действий:</span><span class="sxs-lookup"><span data-stu-id="84452-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="84452-269">А также символ</span><span class="sxs-lookup"><span data-stu-id="84452-269">Plus symbol</span></span>
    
  - <span data-ttu-id="84452-270">Знак минус</span><span class="sxs-lookup"><span data-stu-id="84452-270">Minus symbol</span></span>
    
  - <span data-ttu-id="84452-271">Буква «A» (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="84452-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="84452-272">Три цифры</span><span class="sxs-lookup"><span data-stu-id="84452-272">Three digits</span></span>
    
- <span data-ttu-id="84452-273">Одна буква или одной цифры</span><span class="sxs-lookup"><span data-stu-id="84452-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="84452-274">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="84452-274">Checksum</span></span>

<span data-ttu-id="84452-275">Да</span><span class="sxs-lookup"><span data-stu-id="84452-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="84452-276">Определение</span><span class="sxs-lookup"><span data-stu-id="84452-276">Definition</span></span>

<span data-ttu-id="84452-277">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-278">Функция `Func_finland_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="84452-279">Ключевое слово из `Keywords_finland_eu_ssn_or_equivalent` найден.</span><span class="sxs-lookup"><span data-stu-id="84452-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="84452-280">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-281">Функция `Func_finland_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="84452-282">Keywords</span><span class="sxs-lookup"><span data-stu-id="84452-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="84452-283">Keywords_finland_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="84452-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="84452-284">identification number
</span><span class="sxs-lookup"><span data-stu-id="84452-284">identification number</span></span>
  
<span data-ttu-id="84452-285">личный код</span><span class="sxs-lookup"><span data-stu-id="84452-285">personal id</span></span>
  
<span data-ttu-id="84452-286">Количество идентификаторов</span><span class="sxs-lookup"><span data-stu-id="84452-286">identity number</span></span>
  
<span data-ttu-id="84452-287">Национальный идентификатор для Финляндии номер</span><span class="sxs-lookup"><span data-stu-id="84452-287">finnish national id number</span></span>
  
<span data-ttu-id="84452-288">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="84452-288">personalidnumber#</span></span>
  
<span data-ttu-id="84452-289">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="84452-289">national identification number</span></span>
  
<span data-ttu-id="84452-290">Табельный номер</span><span class="sxs-lookup"><span data-stu-id="84452-290">id number</span></span>
  
<span data-ttu-id="84452-291">Национальный идентификатор для не.</span><span class="sxs-lookup"><span data-stu-id="84452-291">national id no.</span></span>
  
<span data-ttu-id="84452-292">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="84452-292">national id number</span></span>
  
<span data-ttu-id="84452-293">Идентификатор не</span><span class="sxs-lookup"><span data-stu-id="84452-293">id no</span></span>
  
<span data-ttu-id="84452-294">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="84452-294">tunnistenumero</span></span>
  
<span data-ttu-id="84452-295">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="84452-295">henkilötunnus</span></span>
  
<span data-ttu-id="84452-296">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="84452-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="84452-297">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="84452-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="84452-298">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="84452-298">identiteetti numero</span></span>
  
<span data-ttu-id="84452-299">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="84452-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="84452-300">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="84452-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="84452-301">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="84452-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="84452-302">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="84452-302">tunnusnumero</span></span>
  
<span data-ttu-id="84452-303">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="84452-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="84452-304">hetu</span><span class="sxs-lookup"><span data-stu-id="84452-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="84452-305">Франция</span><span class="sxs-lookup"><span data-stu-id="84452-305">France</span></span>

<span data-ttu-id="84452-306">Для получения дополнительных сведений обратитесь к разделу «Франция страховой номер (INSEE)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="84452-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="84452-307">Германия</span><span class="sxs-lookup"><span data-stu-id="84452-307">Germany</span></span>

<span data-ttu-id="84452-308">Для получения дополнительных сведений обратитесь к разделу «Номер идентификационной карты для Германии» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="84452-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="84452-309">Греция</span><span class="sxs-lookup"><span data-stu-id="84452-309">Greece</span></span>

<span data-ttu-id="84452-310">Для получения дополнительных сведений обратитесь к разделу «Греция национальной ИДЕНТИФИКАЦИОННОЙ карты» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="84452-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="84452-311">Венгрия</span><span class="sxs-lookup"><span data-stu-id="84452-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="84452-312">Формат</span><span class="sxs-lookup"><span data-stu-id="84452-312">Format</span></span>

<span data-ttu-id="84452-313">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="84452-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="84452-314">Шаблон</span><span class="sxs-lookup"><span data-stu-id="84452-314">Pattern</span></span>

<span data-ttu-id="84452-315">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="84452-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="84452-316">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="84452-316">Checksum</span></span>

<span data-ttu-id="84452-317">Да</span><span class="sxs-lookup"><span data-stu-id="84452-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="84452-318">Определение</span><span class="sxs-lookup"><span data-stu-id="84452-318">Definition</span></span>

<span data-ttu-id="84452-319">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-320">Функция `Func_hungary_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="84452-321">Ключевое слово из `Keywords_hungary_eu_ssn_or_equivalent` найден.</span><span class="sxs-lookup"><span data-stu-id="84452-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="84452-322">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-323">Функция `Func_hungary_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="84452-324">Keywords</span><span class="sxs-lookup"><span data-stu-id="84452-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="84452-325">Keywords_hungary_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="84452-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="84452-326">Венгерский страховой номер</span><span class="sxs-lookup"><span data-stu-id="84452-326">hungarian social security number</span></span>
  
<span data-ttu-id="84452-327">social security number
</span><span class="sxs-lookup"><span data-stu-id="84452-327">social security number</span></span>
  
<span data-ttu-id="84452-328">socialsecuritynumber #</span><span class="sxs-lookup"><span data-stu-id="84452-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="84452-329">hssn #</span><span class="sxs-lookup"><span data-stu-id="84452-329">hssn#</span></span>
  
<span data-ttu-id="84452-330">socialsecuritynno</span><span class="sxs-lookup"><span data-stu-id="84452-330">socialsecuritynno</span></span>
  
<span data-ttu-id="84452-331">hssn</span><span class="sxs-lookup"><span data-stu-id="84452-331">hssn</span></span>
  
<span data-ttu-id="84452-332">сэкономленные</span><span class="sxs-lookup"><span data-stu-id="84452-332">taj</span></span>
  
<span data-ttu-id="84452-333">сэкономленные #</span><span class="sxs-lookup"><span data-stu-id="84452-333">taj#</span></span>
  
<span data-ttu-id="84452-334">SSN</span><span class="sxs-lookup"><span data-stu-id="84452-334">ssn</span></span>
  
<span data-ttu-id="84452-335">SSN #</span><span class="sxs-lookup"><span data-stu-id="84452-335">ssn#</span></span>
  
<span data-ttu-id="84452-336">социального страхования нет</span><span class="sxs-lookup"><span data-stu-id="84452-336">social security no</span></span>
  
<span data-ttu-id="84452-337">áfa</span><span class="sxs-lookup"><span data-stu-id="84452-337">áfa</span></span>
  
<span data-ttu-id="84452-338">közösségi adószám</span><span class="sxs-lookup"><span data-stu-id="84452-338">közösségi adószám</span></span>
  
<span data-ttu-id="84452-339">általános forgalmi adó szám</span><span class="sxs-lookup"><span data-stu-id="84452-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="84452-340">hozzáadottérték adó</span><span class="sxs-lookup"><span data-stu-id="84452-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="84452-341">áfa szám</span><span class="sxs-lookup"><span data-stu-id="84452-341">áfa szám</span></span>
  
<span data-ttu-id="84452-342">szám magyar áfa</span><span class="sxs-lookup"><span data-stu-id="84452-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="84452-343">Португалия</span><span class="sxs-lookup"><span data-stu-id="84452-343">Portugal</span></span>

<span data-ttu-id="84452-344">Для получения дополнительных сведений обратитесь к разделу «Номер карты Португалия граждане» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="84452-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="84452-345">Испания</span><span class="sxs-lookup"><span data-stu-id="84452-345">Spain</span></span>

<span data-ttu-id="84452-346">Для получения дополнительных сведений обратитесь к разделу «Испания страховой номер (SSN)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="84452-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="84452-347">Швеция</span><span class="sxs-lookup"><span data-stu-id="84452-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="84452-348">Формат</span><span class="sxs-lookup"><span data-stu-id="84452-348">Format</span></span>

<span data-ttu-id="84452-349">12 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="84452-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="84452-350">Шаблон</span><span class="sxs-lookup"><span data-stu-id="84452-350">Pattern</span></span>

<span data-ttu-id="84452-351">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="84452-351">12 digits:</span></span>
  
-  <span data-ttu-id="84452-352">Восемь символов, которые соответствуют Дата рождения (ГГГГММДД)</span><span class="sxs-lookup"><span data-stu-id="84452-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="84452-353">Три цифры, которые соответствуют серийный номер где:</span><span class="sxs-lookup"><span data-stu-id="84452-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="84452-354">Последний знак в серийный номер указывает пол, назначение нечетным количеством для м и четным женщина</span><span class="sxs-lookup"><span data-stu-id="84452-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="84452-355">До 1990, назначения серийный номер откорреспондирован для Район, где рождения носителя номер или (если рождения перед 1947) которых он/она живущих, в соответствии с записями налогах на 1 января 1947, с помощью специального кода (обычно 9 7 цифр) для immigrants</span><span class="sxs-lookup"><span data-stu-id="84452-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="84452-356">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="84452-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="84452-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="84452-357">Checksum</span></span>

<span data-ttu-id="84452-358">Да</span><span class="sxs-lookup"><span data-stu-id="84452-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="84452-359">Определение</span><span class="sxs-lookup"><span data-stu-id="84452-359">Definition</span></span>

<span data-ttu-id="84452-360">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-361">Функция `Func_sweden_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="84452-362">Ключевое слово из `Keywords_sweden_eu_ssn_or_equivalent` найден.</span><span class="sxs-lookup"><span data-stu-id="84452-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="84452-363">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="84452-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="84452-364">Функция `Func_sweden_eu_ssn_or_equivalent` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="84452-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="84452-365">Keywords</span><span class="sxs-lookup"><span data-stu-id="84452-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="84452-366">Keywords_sweden_eu_ssn_or_equivalent</span><span class="sxs-lookup"><span data-stu-id="84452-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="84452-367">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="84452-367">personal id number</span></span>
  
<span data-ttu-id="84452-368">identification number
</span><span class="sxs-lookup"><span data-stu-id="84452-368">identification number</span></span>
  
<span data-ttu-id="84452-369">личный идентификатор не</span><span class="sxs-lookup"><span data-stu-id="84452-369">personal id no</span></span>
  
<span data-ttu-id="84452-370">удостоверение не</span><span class="sxs-lookup"><span data-stu-id="84452-370">identity no</span></span>
  
<span data-ttu-id="84452-371">Идентификация нет</span><span class="sxs-lookup"><span data-stu-id="84452-371">identification no</span></span>
  
<span data-ttu-id="84452-372">персональный идентификационный нет</span><span class="sxs-lookup"><span data-stu-id="84452-372">personal identification no</span></span>
  
<span data-ttu-id="84452-373">Идентификатор personnummer</span><span class="sxs-lookup"><span data-stu-id="84452-373">personnummer id</span></span>
  
<span data-ttu-id="84452-374">Идентификатор personligt-nummer</span><span class="sxs-lookup"><span data-stu-id="84452-374">personligt id-nummer</span></span>
  
<span data-ttu-id="84452-375">Идентификатор unikt-nummer</span><span class="sxs-lookup"><span data-stu-id="84452-375">unikt id-nummer</span></span>
  
<span data-ttu-id="84452-376">personnummer</span><span class="sxs-lookup"><span data-stu-id="84452-376">personnummer</span></span>
  
<span data-ttu-id="84452-377">identifikationsnumret</span><span class="sxs-lookup"><span data-stu-id="84452-377">identifikationsnumret</span></span>
  
<span data-ttu-id="84452-378">personnummer #</span><span class="sxs-lookup"><span data-stu-id="84452-378">personnummer#</span></span>
  
<span data-ttu-id="84452-379">identifikationsnumret #</span><span class="sxs-lookup"><span data-stu-id="84452-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84452-380">См. также</span><span class="sxs-lookup"><span data-stu-id="84452-380">See also</span></span>

[<span data-ttu-id="84452-381">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="84452-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

