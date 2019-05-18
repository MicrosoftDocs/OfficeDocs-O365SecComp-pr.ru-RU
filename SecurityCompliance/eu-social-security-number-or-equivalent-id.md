---
title: Номер социального страхования ЕС или эквивалентный идентификатор
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает номер социального страхования ЕС или эквивалентный тип конфиденциальной информации. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: b42a8d927e18f813eb6ef6d1d55b2de15ea9dcd5
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34154491"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="e1aed-104">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="e1aed-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="e1aed-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС или эквивалентный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="e1aed-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="e1aed-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="e1aed-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="e1aed-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="e1aed-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="e1aed-108">Format</span><span class="sxs-lookup"><span data-stu-id="e1aed-108">Format</span></span>

<span data-ttu-id="e1aed-109">10 цифр в указанном формате</span><span class="sxs-lookup"><span data-stu-id="e1aed-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e1aed-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e1aed-110">Pattern</span></span>

<span data-ttu-id="e1aed-111">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="e1aed-111">10 digits:</span></span>
  
-  <span data-ttu-id="e1aed-112">Три цифры, соответствующие серийному номеру.</span><span class="sxs-lookup"><span data-stu-id="e1aed-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="e1aed-113">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="e1aed-113">One check digit</span></span>
    
- <span data-ttu-id="e1aed-114">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="e1aed-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e1aed-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="e1aed-115">Checksum</span></span>

<span data-ttu-id="e1aed-116">Да</span><span class="sxs-lookup"><span data-stu-id="e1aed-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e1aed-117">Определение</span><span class="sxs-lookup"><span data-stu-id="e1aed-117">Definition</span></span>

<span data-ttu-id="e1aed-118">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-119">Функция `Func_austria_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e1aed-120">Найдено ключевое `Keywords_austria_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="e1aed-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e1aed-121">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-122">Функция `Func_austria_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e1aed-123">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="e1aed-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="e1aed-124">Кэйвордс_аустриа_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="e1aed-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e1aed-125">социальное страхование нет</span><span class="sxs-lookup"><span data-stu-id="e1aed-125">social security no</span></span>
  
<span data-ttu-id="e1aed-126">social security number</span><span class="sxs-lookup"><span data-stu-id="e1aed-126">social security number</span></span>
  
<span data-ttu-id="e1aed-127">social security code</span><span class="sxs-lookup"><span data-stu-id="e1aed-127">social security code</span></span>
  
<span data-ttu-id="e1aed-128">страховой номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-128">insurance number</span></span>
  
<span data-ttu-id="e1aed-129">Австрийский SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-129">austrian ssn</span></span>
  
<span data-ttu-id="e1aed-130">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-130">ssn#</span></span>
  
<span data-ttu-id="e1aed-131">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-131">ssn</span></span>
  
<span data-ttu-id="e1aed-132">код страхования</span><span class="sxs-lookup"><span data-stu-id="e1aed-132">insurance code</span></span>
  
<span data-ttu-id="e1aed-133">код страхования</span><span class="sxs-lookup"><span data-stu-id="e1aed-133">insurance code#</span></span>
  
<span data-ttu-id="e1aed-134">соЦиалсекуритино #</span><span class="sxs-lookup"><span data-stu-id="e1aed-134">socialsecurityno#</span></span>
  
<span data-ttu-id="e1aed-135">созиалверсичерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="e1aed-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="e1aed-136">созиале сичерхеит Кеин</span><span class="sxs-lookup"><span data-stu-id="e1aed-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="e1aed-137">версичерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="e1aed-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="e1aed-138">Бельгия</span><span class="sxs-lookup"><span data-stu-id="e1aed-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="e1aed-139">Format</span><span class="sxs-lookup"><span data-stu-id="e1aed-139">Format</span></span>

<span data-ttu-id="e1aed-140">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="e1aed-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e1aed-141">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e1aed-141">Pattern</span></span>

<span data-ttu-id="e1aed-142">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="e1aed-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e1aed-143">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="e1aed-143">Checksum</span></span>

<span data-ttu-id="e1aed-144">Да</span><span class="sxs-lookup"><span data-stu-id="e1aed-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e1aed-145">Определение</span><span class="sxs-lookup"><span data-stu-id="e1aed-145">Definition</span></span>

<span data-ttu-id="e1aed-146">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-147">Функция `Func_belgium_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e1aed-148">Найдено ключевое `Keywords_belgium_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="e1aed-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e1aed-149">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-150">Функция `Func_belgium_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e1aed-151">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="e1aed-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="e1aed-152">Кэйвордс_белгиум_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="e1aed-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e1aed-153">Бельгийский национальный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-153">belgian national number</span></span>
  
<span data-ttu-id="e1aed-154">номер страны</span><span class="sxs-lookup"><span data-stu-id="e1aed-154">national number</span></span>
  
<span data-ttu-id="e1aed-155">social security number</span><span class="sxs-lookup"><span data-stu-id="e1aed-155">social security number</span></span>
  
<span data-ttu-id="e1aed-156">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-156">nationalnumber#</span></span>
  
<span data-ttu-id="e1aed-157">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-157">ssn#</span></span>
  
<span data-ttu-id="e1aed-158">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-158">ssn</span></span>
  
<span data-ttu-id="e1aed-159">натионалнумбер</span><span class="sxs-lookup"><span data-stu-id="e1aed-159">nationalnumber</span></span>
  
<span data-ttu-id="e1aed-160">БНН #</span><span class="sxs-lookup"><span data-stu-id="e1aed-160">bnn#</span></span>
  
<span data-ttu-id="e1aed-161">БНН</span><span class="sxs-lookup"><span data-stu-id="e1aed-161">bnn</span></span>
  
<span data-ttu-id="e1aed-162">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-162">personal id number</span></span>
  
<span data-ttu-id="e1aed-163">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-163">personalidnumber#</span></span>
  
<span data-ttu-id="e1aed-164">Национальный нумéро</span><span class="sxs-lookup"><span data-stu-id="e1aed-164">numéro national</span></span>
  
<span data-ttu-id="e1aed-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="e1aed-165">numéro de sécurité</span></span>
  
<span data-ttu-id="e1aed-166">нумéро д'ассурé</span><span class="sxs-lookup"><span data-stu-id="e1aed-166">numéro d'assuré</span></span>
  
<span data-ttu-id="e1aed-167">Идентификация National</span><span class="sxs-lookup"><span data-stu-id="e1aed-167">identifiant national</span></span>
  
<span data-ttu-id="e1aed-168">идентифиантнатионал #</span><span class="sxs-lookup"><span data-stu-id="e1aed-168">identifiantnational#</span></span>
  
<span data-ttu-id="e1aed-169">нумéронатионал #</span><span class="sxs-lookup"><span data-stu-id="e1aed-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="e1aed-170">Хорватия</span><span class="sxs-lookup"><span data-stu-id="e1aed-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="e1aed-171">Format</span><span class="sxs-lookup"><span data-stu-id="e1aed-171">Format</span></span>

<span data-ttu-id="e1aed-172">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="e1aed-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e1aed-173">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e1aed-173">Pattern</span></span>

 <span data-ttu-id="e1aed-174">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="e1aed-174">11 digits:</span></span> 
  
-  <span data-ttu-id="e1aed-175">Десять цифр</span><span class="sxs-lookup"><span data-stu-id="e1aed-175">Ten digits</span></span> 
    
- <span data-ttu-id="e1aed-176">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="e1aed-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e1aed-177">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="e1aed-177">Checksum</span></span>

<span data-ttu-id="e1aed-178">Да</span><span class="sxs-lookup"><span data-stu-id="e1aed-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e1aed-179">Определение</span><span class="sxs-lookup"><span data-stu-id="e1aed-179">Definition</span></span>

<span data-ttu-id="e1aed-180">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-181">Функция `Func_croatia_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e1aed-182">Найдено ключевое `Keywords_croatia_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="e1aed-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e1aed-183">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-184">Функция `Func_croatia_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e1aed-185">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="e1aed-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="e1aed-186">Кэйвордс_кроатиа_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="e1aed-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e1aed-187">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-187">personal identification number</span></span>
  
<span data-ttu-id="e1aed-188">основной номер в соотношении</span><span class="sxs-lookup"><span data-stu-id="e1aed-188">master citizen number</span></span>
  
<span data-ttu-id="e1aed-189">national identification number</span><span class="sxs-lookup"><span data-stu-id="e1aed-189">national identification number</span></span>
  
<span data-ttu-id="e1aed-190">social security number</span><span class="sxs-lookup"><span data-stu-id="e1aed-190">social security number</span></span>
  
<span data-ttu-id="e1aed-191">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-191">nationalnumber#</span></span>
  
<span data-ttu-id="e1aed-192">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-192">ssn#</span></span>
  
<span data-ttu-id="e1aed-193">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-193">ssn</span></span>
  
<span data-ttu-id="e1aed-194">натионалнумбер</span><span class="sxs-lookup"><span data-stu-id="e1aed-194">nationalnumber</span></span>
  
<span data-ttu-id="e1aed-195">БНН #</span><span class="sxs-lookup"><span data-stu-id="e1aed-195">bnn#</span></span>
  
<span data-ttu-id="e1aed-196">БНН</span><span class="sxs-lookup"><span data-stu-id="e1aed-196">bnn</span></span>
  
<span data-ttu-id="e1aed-197">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-197">personal id number</span></span>
  
<span data-ttu-id="e1aed-198">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-198">personalidnumber#</span></span>
  
<span data-ttu-id="e1aed-199">OIB</span><span class="sxs-lookup"><span data-stu-id="e1aed-199">oib</span></span>
  
<span data-ttu-id="e1aed-200">особни идентификаЦижски Брож</span><span class="sxs-lookup"><span data-stu-id="e1aed-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="e1aed-201">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="e1aed-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="e1aed-202">Format</span><span class="sxs-lookup"><span data-stu-id="e1aed-202">Format</span></span>

<span data-ttu-id="e1aed-203">Десять цифр и обратная косая черта в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="e1aed-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e1aed-204">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e1aed-204">Pattern</span></span>

<span data-ttu-id="e1aed-205">Десять цифр и обратная косая черта:</span><span class="sxs-lookup"><span data-stu-id="e1aed-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="e1aed-206">Шесть цифр, соответствующих дате рождения (ГГММДД):</span><span class="sxs-lookup"><span data-stu-id="e1aed-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="e1aed-207">Обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="e1aed-207">A backslash</span></span>
    
- <span data-ttu-id="e1aed-208">Три цифры, которые соответствуют серийному номеру, которые отделяют пользователей на одну и ту же дату.</span><span class="sxs-lookup"><span data-stu-id="e1aed-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="e1aed-209">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="e1aed-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e1aed-210">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="e1aed-210">Checksum</span></span>

<span data-ttu-id="e1aed-211">Да</span><span class="sxs-lookup"><span data-stu-id="e1aed-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e1aed-212">Определение</span><span class="sxs-lookup"><span data-stu-id="e1aed-212">Definition</span></span>

<span data-ttu-id="e1aed-213">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-214">Функция `Func_czech_republic_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e1aed-215">Найдено ключевое `Keywords_czech_republic_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="e1aed-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e1aed-216">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-217">Функция `Func_czech_republic_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e1aed-218">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="e1aed-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="e1aed-219">Кэйвордс_кзеч_републик_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="e1aed-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e1aed-220">номер рождения</span><span class="sxs-lookup"><span data-stu-id="e1aed-220">birth number</span></span>
  
<span data-ttu-id="e1aed-221">national identification number</span><span class="sxs-lookup"><span data-stu-id="e1aed-221">national identification number</span></span>
  
<span data-ttu-id="e1aed-222">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-222">personal identification number</span></span>
  
<span data-ttu-id="e1aed-223">social security number</span><span class="sxs-lookup"><span data-stu-id="e1aed-223">social security number</span></span>
  
<span data-ttu-id="e1aed-224">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-224">nationalnumber#</span></span>
  
<span data-ttu-id="e1aed-225">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-225">ssn#</span></span>
  
<span data-ttu-id="e1aed-226">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-226">ssn</span></span>
  
<span data-ttu-id="e1aed-227">номер страны</span><span class="sxs-lookup"><span data-stu-id="e1aed-227">national number</span></span>
  
<span data-ttu-id="e1aed-228">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-228">personal id number</span></span>
  
<span data-ttu-id="e1aed-229">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-229">personalidnumber#</span></span>
  
<span data-ttu-id="e1aed-230">рč</span><span class="sxs-lookup"><span data-stu-id="e1aed-230">rč</span></span>
  
<span data-ttu-id="e1aed-231">роднé číсло</span><span class="sxs-lookup"><span data-stu-id="e1aed-231">rodné číslo</span></span>
  
<span data-ttu-id="e1aed-232">родне Цисло</span><span class="sxs-lookup"><span data-stu-id="e1aed-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="e1aed-233">Дания</span><span class="sxs-lookup"><span data-stu-id="e1aed-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="e1aed-234">Format</span><span class="sxs-lookup"><span data-stu-id="e1aed-234">Format</span></span>

<span data-ttu-id="e1aed-235">Десять цифр и дефис в заданном шаблоне</span><span class="sxs-lookup"><span data-stu-id="e1aed-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e1aed-236">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e1aed-236">Pattern</span></span>

<span data-ttu-id="e1aed-237">Десять цифр и дефис:</span><span class="sxs-lookup"><span data-stu-id="e1aed-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="e1aed-238">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="e1aed-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="e1aed-239">дефис;</span><span class="sxs-lookup"><span data-stu-id="e1aed-239">A hyphen</span></span>
    
- <span data-ttu-id="e1aed-240">Четыре цифры, которые соответствуют порядковому номеру</span><span class="sxs-lookup"><span data-stu-id="e1aed-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e1aed-241">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="e1aed-241">Checksum</span></span>

<span data-ttu-id="e1aed-242">Да</span><span class="sxs-lookup"><span data-stu-id="e1aed-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e1aed-243">Определение</span><span class="sxs-lookup"><span data-stu-id="e1aed-243">Definition</span></span>

<span data-ttu-id="e1aed-244">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-245">Функция `Func_denmark_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e1aed-246">Найдено ключевое `Keywords_denmark_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="e1aed-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e1aed-247">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-248">Функция `Func_denmark_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e1aed-249">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="e1aed-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="e1aed-250">Кэйвордс_денмарк_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="e1aed-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e1aed-251">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-251">personal identification number</span></span>
  
<span data-ttu-id="e1aed-252">national identification number</span><span class="sxs-lookup"><span data-stu-id="e1aed-252">national identification number</span></span>
  
<span data-ttu-id="e1aed-253">social security number</span><span class="sxs-lookup"><span data-stu-id="e1aed-253">social security number</span></span>
  
<span data-ttu-id="e1aed-254">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-254">nationalnumber#</span></span>
  
<span data-ttu-id="e1aed-255">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-255">ssn#</span></span>
  
<span data-ttu-id="e1aed-256">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-256">ssn</span></span>
  
<span data-ttu-id="e1aed-257">номер страны</span><span class="sxs-lookup"><span data-stu-id="e1aed-257">national number</span></span>
  
<span data-ttu-id="e1aed-258">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-258">personal id number</span></span>
  
<span data-ttu-id="e1aed-259">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-259">personalidnumber#</span></span>
  
<span data-ttu-id="e1aed-260">CPR — нуммер</span><span class="sxs-lookup"><span data-stu-id="e1aed-260">cpr-nummer</span></span>
  
<span data-ttu-id="e1aed-261">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="e1aed-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="e1aed-262">Финляндия</span><span class="sxs-lookup"><span data-stu-id="e1aed-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="e1aed-263">Format</span><span class="sxs-lookup"><span data-stu-id="e1aed-263">Format</span></span>

<span data-ttu-id="e1aed-264">11 символов в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="e1aed-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e1aed-265">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e1aed-265">Pattern</span></span>

<span data-ttu-id="e1aed-266">Сочетание из 11 символов в указанном формате:</span><span class="sxs-lookup"><span data-stu-id="e1aed-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="e1aed-267">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="e1aed-267">Six digits</span></span> 
    
- <span data-ttu-id="e1aed-268">Один из следующих экземпляров:</span><span class="sxs-lookup"><span data-stu-id="e1aed-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="e1aed-269">Символ "плюс"</span><span class="sxs-lookup"><span data-stu-id="e1aed-269">Plus symbol</span></span>
    
  - <span data-ttu-id="e1aed-270">Символ "минус"</span><span class="sxs-lookup"><span data-stu-id="e1aed-270">Minus symbol</span></span>
    
  - <span data-ttu-id="e1aed-271">Буква "A" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="e1aed-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="e1aed-272">Три цифры</span><span class="sxs-lookup"><span data-stu-id="e1aed-272">Three digits</span></span>
    
- <span data-ttu-id="e1aed-273">Одна буква или одна цифра</span><span class="sxs-lookup"><span data-stu-id="e1aed-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e1aed-274">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="e1aed-274">Checksum</span></span>

<span data-ttu-id="e1aed-275">Да</span><span class="sxs-lookup"><span data-stu-id="e1aed-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e1aed-276">Определение</span><span class="sxs-lookup"><span data-stu-id="e1aed-276">Definition</span></span>

<span data-ttu-id="e1aed-277">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-278">Функция `Func_finland_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e1aed-279">Найдено ключевое `Keywords_finland_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="e1aed-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e1aed-280">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-281">Функция `Func_finland_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e1aed-282">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="e1aed-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="e1aed-283">Кэйвордс_финланд_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="e1aed-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e1aed-284">identification number</span><span class="sxs-lookup"><span data-stu-id="e1aed-284">identification number</span></span>
  
<span data-ttu-id="e1aed-285">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="e1aed-285">personal id</span></span>
  
<span data-ttu-id="e1aed-286">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-286">identity number</span></span>
  
<span data-ttu-id="e1aed-287">Финский национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-287">finnish national id number</span></span>
  
<span data-ttu-id="e1aed-288">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-288">personalidnumber#</span></span>
  
<span data-ttu-id="e1aed-289">national identification number</span><span class="sxs-lookup"><span data-stu-id="e1aed-289">national identification number</span></span>
  
<span data-ttu-id="e1aed-290">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-290">id number</span></span>
  
<span data-ttu-id="e1aed-291">код страны</span><span class="sxs-lookup"><span data-stu-id="e1aed-291">national id no.</span></span>
  
<span data-ttu-id="e1aed-292">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-292">national id number</span></span>
  
<span data-ttu-id="e1aed-293">ID No</span><span class="sxs-lookup"><span data-stu-id="e1aed-293">id no</span></span>
  
<span data-ttu-id="e1aed-294">туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="e1aed-294">tunnistenumero</span></span>
  
<span data-ttu-id="e1aed-295">хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="e1aed-295">henkilötunnus</span></span>
  
<span data-ttu-id="e1aed-296">иксилöллинен хенкилöкохтаинен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="e1aed-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="e1aed-297">аинутлаатуинен хенкилöкохтаинен туннус</span><span class="sxs-lookup"><span data-stu-id="e1aed-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="e1aed-298">идентититти нумеро</span><span class="sxs-lookup"><span data-stu-id="e1aed-298">identiteetti numero</span></span>
  
<span data-ttu-id="e1aed-299">Суомен кансаллинен хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="e1aed-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="e1aed-300">хенкилöтуннуснумеро #</span><span class="sxs-lookup"><span data-stu-id="e1aed-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="e1aed-301">кансаллисен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="e1aed-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="e1aed-302">туннуснумеро</span><span class="sxs-lookup"><span data-stu-id="e1aed-302">tunnusnumero</span></span>
  
<span data-ttu-id="e1aed-303">кансаллинен туннус нумеро</span><span class="sxs-lookup"><span data-stu-id="e1aed-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="e1aed-304">Хету</span><span class="sxs-lookup"><span data-stu-id="e1aed-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="e1aed-305">Франция</span><span class="sxs-lookup"><span data-stu-id="e1aed-305">France</span></span>

<span data-ttu-id="e1aed-306">Дополнительные сведения см. в разделе "номер социального страхования для Франции (INSEE)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e1aed-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="e1aed-307">Германия</span><span class="sxs-lookup"><span data-stu-id="e1aed-307">Germany</span></span>

<span data-ttu-id="e1aed-308">Дополнительные сведения можно найти в разделе "номер идентификационной карточки для Германии" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e1aed-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="e1aed-309">Греция</span><span class="sxs-lookup"><span data-stu-id="e1aed-309">Greece</span></span>

<span data-ttu-id="e1aed-310">Дополнительные сведения можно найти в разделе "Греция National ID Card", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e1aed-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="e1aed-311">Венгрия</span><span class="sxs-lookup"><span data-stu-id="e1aed-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="e1aed-312">Format</span><span class="sxs-lookup"><span data-stu-id="e1aed-312">Format</span></span>

<span data-ttu-id="e1aed-313">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="e1aed-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e1aed-314">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e1aed-314">Pattern</span></span>

<span data-ttu-id="e1aed-315">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="e1aed-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="e1aed-316">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="e1aed-316">Checksum</span></span>

<span data-ttu-id="e1aed-317">Да</span><span class="sxs-lookup"><span data-stu-id="e1aed-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e1aed-318">Определение</span><span class="sxs-lookup"><span data-stu-id="e1aed-318">Definition</span></span>

<span data-ttu-id="e1aed-319">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-320">Функция `Func_hungary_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e1aed-321">Найдено ключевое `Keywords_hungary_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="e1aed-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e1aed-322">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-323">Функция `Func_hungary_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e1aed-324">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="e1aed-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="e1aed-325">Кэйвордс_хунгари_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="e1aed-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e1aed-326">Венгерский номер социального страхования</span><span class="sxs-lookup"><span data-stu-id="e1aed-326">hungarian social security number</span></span>
  
<span data-ttu-id="e1aed-327">social security number</span><span class="sxs-lookup"><span data-stu-id="e1aed-327">social security number</span></span>
  
<span data-ttu-id="e1aed-328">соЦиалсекуритинумбер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="e1aed-329">хссн #</span><span class="sxs-lookup"><span data-stu-id="e1aed-329">hssn#</span></span>
  
<span data-ttu-id="e1aed-330">соЦиалсекуритинно</span><span class="sxs-lookup"><span data-stu-id="e1aed-330">socialsecuritynno</span></span>
  
<span data-ttu-id="e1aed-331">хссн</span><span class="sxs-lookup"><span data-stu-id="e1aed-331">hssn</span></span>
  
<span data-ttu-id="e1aed-332">Таж</span><span class="sxs-lookup"><span data-stu-id="e1aed-332">taj</span></span>
  
<span data-ttu-id="e1aed-333">Таж #</span><span class="sxs-lookup"><span data-stu-id="e1aed-333">taj#</span></span>
  
<span data-ttu-id="e1aed-334">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-334">ssn</span></span>
  
<span data-ttu-id="e1aed-335">SSN</span><span class="sxs-lookup"><span data-stu-id="e1aed-335">ssn#</span></span>
  
<span data-ttu-id="e1aed-336">социальное страхование нет</span><span class="sxs-lookup"><span data-stu-id="e1aed-336">social security no</span></span>
  
<span data-ttu-id="e1aed-337">áфа</span><span class="sxs-lookup"><span data-stu-id="e1aed-337">áfa</span></span>
  
<span data-ttu-id="e1aed-338">кöзöссéги адóсзáм</span><span class="sxs-lookup"><span data-stu-id="e1aed-338">közösségi adószám</span></span>
  
<span data-ttu-id="e1aed-339">áлталáнос форгалми адó сзáм</span><span class="sxs-lookup"><span data-stu-id="e1aed-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="e1aed-340">хоззáадоттéртéк адó</span><span class="sxs-lookup"><span data-stu-id="e1aed-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="e1aed-341">áфа сзáм</span><span class="sxs-lookup"><span data-stu-id="e1aed-341">áfa szám</span></span>
  
<span data-ttu-id="e1aed-342">магяр áфа сзáм</span><span class="sxs-lookup"><span data-stu-id="e1aed-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="e1aed-343">Португалия</span><span class="sxs-lookup"><span data-stu-id="e1aed-343">Portugal</span></span>

<span data-ttu-id="e1aed-344">Дополнительные сведения можно найти в разделе "номер карты для Португалия" в разделе [сведения о типах конфиденциальной информации для поиска](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e1aed-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="e1aed-345">Испания</span><span class="sxs-lookup"><span data-stu-id="e1aed-345">Spain</span></span>

<span data-ttu-id="e1aed-346">Дополнительные сведения см. в разделе "номер социального страхования для Испании (SSN)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e1aed-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="e1aed-347">Швеция</span><span class="sxs-lookup"><span data-stu-id="e1aed-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="e1aed-348">Format</span><span class="sxs-lookup"><span data-stu-id="e1aed-348">Format</span></span>

<span data-ttu-id="e1aed-349">12 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="e1aed-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e1aed-350">Шаблон</span><span class="sxs-lookup"><span data-stu-id="e1aed-350">Pattern</span></span>

<span data-ttu-id="e1aed-351">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="e1aed-351">12 digits:</span></span>
  
-  <span data-ttu-id="e1aed-352">Восемь цифр, которые соответствуют дате рождения (ГГГГММДД)</span><span class="sxs-lookup"><span data-stu-id="e1aed-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="e1aed-353">Три цифры, которые соответствуют серийному номеру, где:</span><span class="sxs-lookup"><span data-stu-id="e1aed-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="e1aed-354">Последняя цифра в числовом номере указывает на пол, назначая нечетное число для пола и четное число для розетки.</span><span class="sxs-lookup"><span data-stu-id="e1aed-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="e1aed-355">До 1990, назначение серийного номера соответствует району, в котором был выпущен номер, или (если он родился до 1947), где он был удален, в соответствии с налоговыми записями 1 января 1947, с помощью специального кода (как правило, 9 в качестве седьмой цифры). иммигрантс</span><span class="sxs-lookup"><span data-stu-id="e1aed-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="e1aed-356">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="e1aed-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e1aed-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="e1aed-357">Checksum</span></span>

<span data-ttu-id="e1aed-358">Да</span><span class="sxs-lookup"><span data-stu-id="e1aed-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="e1aed-359">Определение</span><span class="sxs-lookup"><span data-stu-id="e1aed-359">Definition</span></span>

<span data-ttu-id="e1aed-360">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-361">Функция `Func_sweden_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e1aed-362">Найдено ключевое `Keywords_sweden_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="e1aed-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="e1aed-363">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="e1aed-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e1aed-364">Функция `Func_sweden_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="e1aed-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="e1aed-365">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="e1aed-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="e1aed-366">Кэйвордс_сведен_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="e1aed-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="e1aed-367">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-367">personal id number</span></span>
  
<span data-ttu-id="e1aed-368">identification number</span><span class="sxs-lookup"><span data-stu-id="e1aed-368">identification number</span></span>
  
<span data-ttu-id="e1aed-369">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="e1aed-369">personal id no</span></span>
  
<span data-ttu-id="e1aed-370">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e1aed-370">identity no</span></span>
  
<span data-ttu-id="e1aed-371">Идентификация нет</span><span class="sxs-lookup"><span data-stu-id="e1aed-371">identification no</span></span>
  
<span data-ttu-id="e1aed-372">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="e1aed-372">personal identification no</span></span>
  
<span data-ttu-id="e1aed-373">Идентификатор персоннуммер</span><span class="sxs-lookup"><span data-stu-id="e1aed-373">personnummer id</span></span>
  
<span data-ttu-id="e1aed-374">Идентификатор персонлигт — нуммер</span><span class="sxs-lookup"><span data-stu-id="e1aed-374">personligt id-nummer</span></span>
  
<span data-ttu-id="e1aed-375">Идентификатор уникт — нуммер</span><span class="sxs-lookup"><span data-stu-id="e1aed-375">unikt id-nummer</span></span>
  
<span data-ttu-id="e1aed-376">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="e1aed-376">personnummer</span></span>
  
<span data-ttu-id="e1aed-377">идентификатионснумрет</span><span class="sxs-lookup"><span data-stu-id="e1aed-377">identifikationsnumret</span></span>
  
<span data-ttu-id="e1aed-378">персоннуммер #</span><span class="sxs-lookup"><span data-stu-id="e1aed-378">personnummer#</span></span>
  
<span data-ttu-id="e1aed-379">идентификатионснумрет #</span><span class="sxs-lookup"><span data-stu-id="e1aed-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1aed-380">См. также</span><span class="sxs-lookup"><span data-stu-id="e1aed-380">See also</span></span>

[<span data-ttu-id="e1aed-381">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="e1aed-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

