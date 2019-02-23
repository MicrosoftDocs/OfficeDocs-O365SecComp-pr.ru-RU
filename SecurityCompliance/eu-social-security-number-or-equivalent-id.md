---
title: Номер социального страхования ЕС или эквивалентный идентификатор
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает номер социального страхования ЕС или эквивалентный тип конфиденциальной информации. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: abcefb6930e9c02d2f32d84b65accfecf1e20d95
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216529"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="b0d4c-104">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="b0d4c-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="b0d4c-p102">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС или эквивалентный идентификатор. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="b0d4c-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="b0d4c-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="b0d4c-108">Формат</span><span class="sxs-lookup"><span data-stu-id="b0d4c-108">Format</span></span>

<span data-ttu-id="b0d4c-109">10 цифр в указанном формате</span><span class="sxs-lookup"><span data-stu-id="b0d4c-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0d4c-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="b0d4c-110">Pattern</span></span>

<span data-ttu-id="b0d4c-111">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-111">10 digits:</span></span>
  
-  <span data-ttu-id="b0d4c-112">Три цифры, соответствующие серийному номеру.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="b0d4c-113">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="b0d4c-113">One check digit</span></span>
    
- <span data-ttu-id="b0d4c-114">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="b0d4c-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0d4c-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="b0d4c-115">Checksum</span></span>

<span data-ttu-id="b0d4c-116">Да</span><span class="sxs-lookup"><span data-stu-id="b0d4c-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0d4c-117">Определение</span><span class="sxs-lookup"><span data-stu-id="b0d4c-117">Definition</span></span>

<span data-ttu-id="b0d4c-118">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-119">Функция `Func_austria_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0d4c-120">Найдено ключевое `Keywords_austria_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b0d4c-121">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-122">Функция `Func_austria_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b0d4c-123">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="b0d4c-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="b0d4c-124">Кэйвордс_аустриа_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="b0d4c-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b0d4c-125">социальное страхование нет</span><span class="sxs-lookup"><span data-stu-id="b0d4c-125">social security no</span></span>
  
<span data-ttu-id="b0d4c-126">social security number
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-126">social security number</span></span>
  
<span data-ttu-id="b0d4c-127">
social security code</span><span class="sxs-lookup"><span data-stu-id="b0d4c-127">social security code</span></span>
  
<span data-ttu-id="b0d4c-128">страховой номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-128">insurance number</span></span>
  
<span data-ttu-id="b0d4c-129">Австрийский SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-129">austrian ssn</span></span>
  
<span data-ttu-id="b0d4c-130">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-130">ssn#</span></span>
  
<span data-ttu-id="b0d4c-131">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-131">ssn</span></span>
  
<span data-ttu-id="b0d4c-132">код страхования</span><span class="sxs-lookup"><span data-stu-id="b0d4c-132">insurance code</span></span>
  
<span data-ttu-id="b0d4c-133">код страхования</span><span class="sxs-lookup"><span data-stu-id="b0d4c-133">insurance code#</span></span>
  
<span data-ttu-id="b0d4c-134">соЦиалсекуритино #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-134">socialsecurityno#</span></span>
  
<span data-ttu-id="b0d4c-135">созиалверсичерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="b0d4c-136">созиале сичерхеит Кеин</span><span class="sxs-lookup"><span data-stu-id="b0d4c-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="b0d4c-137">версичерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="b0d4c-138">Бельгия</span><span class="sxs-lookup"><span data-stu-id="b0d4c-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="b0d4c-139">Формат</span><span class="sxs-lookup"><span data-stu-id="b0d4c-139">Format</span></span>

<span data-ttu-id="b0d4c-140">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="b0d4c-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0d4c-141">Шаблон</span><span class="sxs-lookup"><span data-stu-id="b0d4c-141">Pattern</span></span>

<span data-ttu-id="b0d4c-142">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="b0d4c-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0d4c-143">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="b0d4c-143">Checksum</span></span>

<span data-ttu-id="b0d4c-144">Да</span><span class="sxs-lookup"><span data-stu-id="b0d4c-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0d4c-145">Определение</span><span class="sxs-lookup"><span data-stu-id="b0d4c-145">Definition</span></span>

<span data-ttu-id="b0d4c-146">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-147">Функция `Func_belgium_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0d4c-148">Найдено ключевое `Keywords_belgium_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b0d4c-149">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-150">Функция `Func_belgium_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b0d4c-151">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="b0d4c-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="b0d4c-152">Кэйвордс_белгиум_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="b0d4c-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b0d4c-153">Бельгийский национальный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-153">belgian national number</span></span>
  
<span data-ttu-id="b0d4c-154">номер страны</span><span class="sxs-lookup"><span data-stu-id="b0d4c-154">national number</span></span>
  
<span data-ttu-id="b0d4c-155">social security number
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-155">social security number</span></span>
  
<span data-ttu-id="b0d4c-156">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-156">nationalnumber#</span></span>
  
<span data-ttu-id="b0d4c-157">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-157">ssn#</span></span>
  
<span data-ttu-id="b0d4c-158">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-158">ssn</span></span>
  
<span data-ttu-id="b0d4c-159">натионалнумбер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-159">nationalnumber</span></span>
  
<span data-ttu-id="b0d4c-160">БНН #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-160">bnn#</span></span>
  
<span data-ttu-id="b0d4c-161">БНН</span><span class="sxs-lookup"><span data-stu-id="b0d4c-161">bnn</span></span>
  
<span data-ttu-id="b0d4c-162">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-162">personal id number</span></span>
  
<span data-ttu-id="b0d4c-163">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-163">personalidnumber#</span></span>
  
<span data-ttu-id="b0d4c-164">Национальный нумéро</span><span class="sxs-lookup"><span data-stu-id="b0d4c-164">numéro national</span></span>
  
<span data-ttu-id="b0d4c-165">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-165">numéro de sécurité</span></span>
  
<span data-ttu-id="b0d4c-166">нумéро д'ассурé</span><span class="sxs-lookup"><span data-stu-id="b0d4c-166">numéro d'assuré</span></span>
  
<span data-ttu-id="b0d4c-167">Идентификация National</span><span class="sxs-lookup"><span data-stu-id="b0d4c-167">identifiant national</span></span>
  
<span data-ttu-id="b0d4c-168">идентифиантнатионал #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-168">identifiantnational#</span></span>
  
<span data-ttu-id="b0d4c-169">нумéронатионал #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="b0d4c-170">Хорватия</span><span class="sxs-lookup"><span data-stu-id="b0d4c-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="b0d4c-171">Формат</span><span class="sxs-lookup"><span data-stu-id="b0d4c-171">Format</span></span>

<span data-ttu-id="b0d4c-172">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="b0d4c-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0d4c-173">Шаблон</span><span class="sxs-lookup"><span data-stu-id="b0d4c-173">Pattern</span></span>

 <span data-ttu-id="b0d4c-174">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-174">11 digits:</span></span> 
  
-  <span data-ttu-id="b0d4c-175">Десять цифр</span><span class="sxs-lookup"><span data-stu-id="b0d4c-175">Ten digits</span></span> 
    
- <span data-ttu-id="b0d4c-176">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="b0d4c-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0d4c-177">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="b0d4c-177">Checksum</span></span>

<span data-ttu-id="b0d4c-178">Да</span><span class="sxs-lookup"><span data-stu-id="b0d4c-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0d4c-179">Определение</span><span class="sxs-lookup"><span data-stu-id="b0d4c-179">Definition</span></span>

<span data-ttu-id="b0d4c-180">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-181">Функция `Func_croatia_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0d4c-182">Найдено ключевое `Keywords_croatia_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b0d4c-183">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-184">Функция `Func_croatia_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b0d4c-185">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="b0d4c-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="b0d4c-186">Кэйвордс_кроатиа_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="b0d4c-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b0d4c-187">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-187">personal identification number</span></span>
  
<span data-ttu-id="b0d4c-188">основной номер в соотношении</span><span class="sxs-lookup"><span data-stu-id="b0d4c-188">master citizen number</span></span>
  
<span data-ttu-id="b0d4c-189">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-189">national identification number</span></span>
  
<span data-ttu-id="b0d4c-190">social security number
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-190">social security number</span></span>
  
<span data-ttu-id="b0d4c-191">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-191">nationalnumber#</span></span>
  
<span data-ttu-id="b0d4c-192">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-192">ssn#</span></span>
  
<span data-ttu-id="b0d4c-193">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-193">ssn</span></span>
  
<span data-ttu-id="b0d4c-194">натионалнумбер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-194">nationalnumber</span></span>
  
<span data-ttu-id="b0d4c-195">БНН #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-195">bnn#</span></span>
  
<span data-ttu-id="b0d4c-196">БНН</span><span class="sxs-lookup"><span data-stu-id="b0d4c-196">bnn</span></span>
  
<span data-ttu-id="b0d4c-197">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-197">personal id number</span></span>
  
<span data-ttu-id="b0d4c-198">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-198">personalidnumber#</span></span>
  
<span data-ttu-id="b0d4c-199">OIB</span><span class="sxs-lookup"><span data-stu-id="b0d4c-199">oib</span></span>
  
<span data-ttu-id="b0d4c-200">особни идентификаЦижски Брож</span><span class="sxs-lookup"><span data-stu-id="b0d4c-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="b0d4c-201">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="b0d4c-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="b0d4c-202">Формат</span><span class="sxs-lookup"><span data-stu-id="b0d4c-202">Format</span></span>

<span data-ttu-id="b0d4c-203">Десять цифр и обратная косая черта в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="b0d4c-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0d4c-204">Шаблон</span><span class="sxs-lookup"><span data-stu-id="b0d4c-204">Pattern</span></span>

<span data-ttu-id="b0d4c-205">Десять цифр и обратная косая черта:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="b0d4c-206">Шесть цифр, соответствующих дате рождения (ГГММДД):</span><span class="sxs-lookup"><span data-stu-id="b0d4c-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="b0d4c-207">Обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="b0d4c-207">A backslash</span></span>
    
- <span data-ttu-id="b0d4c-208">Три цифры, которые соответствуют серийному номеру, которые отделяют пользователей на одну и ту же дату.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="b0d4c-209">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="b0d4c-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0d4c-210">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="b0d4c-210">Checksum</span></span>

<span data-ttu-id="b0d4c-211">Да</span><span class="sxs-lookup"><span data-stu-id="b0d4c-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0d4c-212">Определение</span><span class="sxs-lookup"><span data-stu-id="b0d4c-212">Definition</span></span>

<span data-ttu-id="b0d4c-213">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-214">Функция `Func_czech_republic_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0d4c-215">Найдено ключевое `Keywords_czech_republic_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b0d4c-216">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-217">Функция `Func_czech_republic_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b0d4c-218">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="b0d4c-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="b0d4c-219">Кэйвордс_кзеч_републик_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="b0d4c-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b0d4c-220">номер рождения</span><span class="sxs-lookup"><span data-stu-id="b0d4c-220">birth number</span></span>
  
<span data-ttu-id="b0d4c-221">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-221">national identification number</span></span>
  
<span data-ttu-id="b0d4c-222">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-222">personal identification number</span></span>
  
<span data-ttu-id="b0d4c-223">social security number
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-223">social security number</span></span>
  
<span data-ttu-id="b0d4c-224">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-224">nationalnumber#</span></span>
  
<span data-ttu-id="b0d4c-225">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-225">ssn#</span></span>
  
<span data-ttu-id="b0d4c-226">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-226">ssn</span></span>
  
<span data-ttu-id="b0d4c-227">номер страны</span><span class="sxs-lookup"><span data-stu-id="b0d4c-227">national number</span></span>
  
<span data-ttu-id="b0d4c-228">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-228">personal id number</span></span>
  
<span data-ttu-id="b0d4c-229">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-229">personalidnumber#</span></span>
  
<span data-ttu-id="b0d4c-230">рč</span><span class="sxs-lookup"><span data-stu-id="b0d4c-230">rč</span></span>
  
<span data-ttu-id="b0d4c-231">роднé číсло</span><span class="sxs-lookup"><span data-stu-id="b0d4c-231">rodné číslo</span></span>
  
<span data-ttu-id="b0d4c-232">родне Цисло</span><span class="sxs-lookup"><span data-stu-id="b0d4c-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="b0d4c-233">Дания</span><span class="sxs-lookup"><span data-stu-id="b0d4c-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="b0d4c-234">Формат</span><span class="sxs-lookup"><span data-stu-id="b0d4c-234">Format</span></span>

<span data-ttu-id="b0d4c-235">Десять цифр и дефис в заданном шаблоне</span><span class="sxs-lookup"><span data-stu-id="b0d4c-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0d4c-236">Шаблон</span><span class="sxs-lookup"><span data-stu-id="b0d4c-236">Pattern</span></span>

<span data-ttu-id="b0d4c-237">Десять цифр и дефис:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="b0d4c-238">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="b0d4c-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="b0d4c-239">дефис;</span><span class="sxs-lookup"><span data-stu-id="b0d4c-239">A hyphen</span></span>
    
- <span data-ttu-id="b0d4c-240">Четыре цифры, которые соответствуют порядковому номеру</span><span class="sxs-lookup"><span data-stu-id="b0d4c-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0d4c-241">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="b0d4c-241">Checksum</span></span>

<span data-ttu-id="b0d4c-242">Да</span><span class="sxs-lookup"><span data-stu-id="b0d4c-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0d4c-243">Определение</span><span class="sxs-lookup"><span data-stu-id="b0d4c-243">Definition</span></span>

<span data-ttu-id="b0d4c-244">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-245">Функция `Func_denmark_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0d4c-246">Найдено ключевое `Keywords_denmark_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b0d4c-247">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-248">Функция `Func_denmark_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b0d4c-249">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="b0d4c-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="b0d4c-250">Кэйвордс_денмарк_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="b0d4c-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b0d4c-251">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-251">personal identification number</span></span>
  
<span data-ttu-id="b0d4c-252">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-252">national identification number</span></span>
  
<span data-ttu-id="b0d4c-253">social security number
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-253">social security number</span></span>
  
<span data-ttu-id="b0d4c-254">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-254">nationalnumber#</span></span>
  
<span data-ttu-id="b0d4c-255">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-255">ssn#</span></span>
  
<span data-ttu-id="b0d4c-256">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-256">ssn</span></span>
  
<span data-ttu-id="b0d4c-257">номер страны</span><span class="sxs-lookup"><span data-stu-id="b0d4c-257">national number</span></span>
  
<span data-ttu-id="b0d4c-258">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-258">personal id number</span></span>
  
<span data-ttu-id="b0d4c-259">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-259">personalidnumber#</span></span>
  
<span data-ttu-id="b0d4c-260">CPR — нуммер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-260">cpr-nummer</span></span>
  
<span data-ttu-id="b0d4c-261">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="b0d4c-262">Финляндия</span><span class="sxs-lookup"><span data-stu-id="b0d4c-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="b0d4c-263">Формат</span><span class="sxs-lookup"><span data-stu-id="b0d4c-263">Format</span></span>

<span data-ttu-id="b0d4c-264">11 символов в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0d4c-265">Шаблон</span><span class="sxs-lookup"><span data-stu-id="b0d4c-265">Pattern</span></span>

<span data-ttu-id="b0d4c-266">Сочетание из 11 символов в указанном формате:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="b0d4c-267">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="b0d4c-267">Six digits</span></span> 
    
- <span data-ttu-id="b0d4c-268">Один из следующих экземпляров:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="b0d4c-269">Символ "плюс"</span><span class="sxs-lookup"><span data-stu-id="b0d4c-269">Plus symbol</span></span>
    
  - <span data-ttu-id="b0d4c-270">Символ "минус"</span><span class="sxs-lookup"><span data-stu-id="b0d4c-270">Minus symbol</span></span>
    
  - <span data-ttu-id="b0d4c-271">Буква "A" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="b0d4c-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="b0d4c-272">Три цифры</span><span class="sxs-lookup"><span data-stu-id="b0d4c-272">Three digits</span></span>
    
- <span data-ttu-id="b0d4c-273">Одна буква или одна цифра</span><span class="sxs-lookup"><span data-stu-id="b0d4c-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0d4c-274">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="b0d4c-274">Checksum</span></span>

<span data-ttu-id="b0d4c-275">Да</span><span class="sxs-lookup"><span data-stu-id="b0d4c-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0d4c-276">Определение</span><span class="sxs-lookup"><span data-stu-id="b0d4c-276">Definition</span></span>

<span data-ttu-id="b0d4c-277">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-278">Функция `Func_finland_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0d4c-279">Найдено ключевое `Keywords_finland_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b0d4c-280">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-281">Функция `Func_finland_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b0d4c-282">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="b0d4c-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="b0d4c-283">Кэйвордс_финланд_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="b0d4c-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b0d4c-284">identification number
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-284">identification number</span></span>
  
<span data-ttu-id="b0d4c-285">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="b0d4c-285">personal id</span></span>
  
<span data-ttu-id="b0d4c-286">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-286">identity number</span></span>
  
<span data-ttu-id="b0d4c-287">Финский национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-287">finnish national id number</span></span>
  
<span data-ttu-id="b0d4c-288">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-288">personalidnumber#</span></span>
  
<span data-ttu-id="b0d4c-289">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-289">national identification number</span></span>
  
<span data-ttu-id="b0d4c-290">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-290">id number</span></span>
  
<span data-ttu-id="b0d4c-291">код страны</span><span class="sxs-lookup"><span data-stu-id="b0d4c-291">national id no.</span></span>
  
<span data-ttu-id="b0d4c-292">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-292">national id number</span></span>
  
<span data-ttu-id="b0d4c-293">ID No</span><span class="sxs-lookup"><span data-stu-id="b0d4c-293">id no</span></span>
  
<span data-ttu-id="b0d4c-294">туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="b0d4c-294">tunnistenumero</span></span>
  
<span data-ttu-id="b0d4c-295">хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="b0d4c-295">henkilötunnus</span></span>
  
<span data-ttu-id="b0d4c-296">иксилöллинен хенкилöкохтаинен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="b0d4c-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="b0d4c-297">аинутлаатуинен хенкилöкохтаинен туннус</span><span class="sxs-lookup"><span data-stu-id="b0d4c-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="b0d4c-298">идентититти нумеро</span><span class="sxs-lookup"><span data-stu-id="b0d4c-298">identiteetti numero</span></span>
  
<span data-ttu-id="b0d4c-299">Суомен кансаллинен хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="b0d4c-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="b0d4c-300">хенкилöтуннуснумеро #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="b0d4c-301">кансаллисен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="b0d4c-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="b0d4c-302">туннуснумеро</span><span class="sxs-lookup"><span data-stu-id="b0d4c-302">tunnusnumero</span></span>
  
<span data-ttu-id="b0d4c-303">кансаллинен туннус нумеро</span><span class="sxs-lookup"><span data-stu-id="b0d4c-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="b0d4c-304">Хету</span><span class="sxs-lookup"><span data-stu-id="b0d4c-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="b0d4c-305">Франция</span><span class="sxs-lookup"><span data-stu-id="b0d4c-305">France</span></span>

<span data-ttu-id="b0d4c-306">Дополнительные сведения см. в разделе "номер социального страхования для Франции (INSEE)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0d4c-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="b0d4c-307">Германия</span><span class="sxs-lookup"><span data-stu-id="b0d4c-307">Germany</span></span>

<span data-ttu-id="b0d4c-308">Дополнительные сведения можно найти в разделе "номер идентификационной карточки для Германии" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0d4c-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="b0d4c-309">Греция</span><span class="sxs-lookup"><span data-stu-id="b0d4c-309">Greece</span></span>

<span data-ttu-id="b0d4c-310">Дополнительные сведения можно найти в разделе "Греция National ID Card", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0d4c-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="b0d4c-311">Венгрия</span><span class="sxs-lookup"><span data-stu-id="b0d4c-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="b0d4c-312">Формат</span><span class="sxs-lookup"><span data-stu-id="b0d4c-312">Format</span></span>

<span data-ttu-id="b0d4c-313">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="b0d4c-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0d4c-314">Шаблон</span><span class="sxs-lookup"><span data-stu-id="b0d4c-314">Pattern</span></span>

<span data-ttu-id="b0d4c-315">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0d4c-316">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="b0d4c-316">Checksum</span></span>

<span data-ttu-id="b0d4c-317">Да</span><span class="sxs-lookup"><span data-stu-id="b0d4c-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0d4c-318">Определение</span><span class="sxs-lookup"><span data-stu-id="b0d4c-318">Definition</span></span>

<span data-ttu-id="b0d4c-319">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-320">Функция `Func_hungary_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0d4c-321">Найдено ключевое `Keywords_hungary_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b0d4c-322">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-323">Функция `Func_hungary_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b0d4c-324">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="b0d4c-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="b0d4c-325">Кэйвордс_хунгари_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="b0d4c-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b0d4c-326">Венгерский номер социального страхования</span><span class="sxs-lookup"><span data-stu-id="b0d4c-326">hungarian social security number</span></span>
  
<span data-ttu-id="b0d4c-327">social security number
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-327">social security number</span></span>
  
<span data-ttu-id="b0d4c-328">соЦиалсекуритинумбер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="b0d4c-329">хссн #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-329">hssn#</span></span>
  
<span data-ttu-id="b0d4c-330">соЦиалсекуритинно</span><span class="sxs-lookup"><span data-stu-id="b0d4c-330">socialsecuritynno</span></span>
  
<span data-ttu-id="b0d4c-331">хссн</span><span class="sxs-lookup"><span data-stu-id="b0d4c-331">hssn</span></span>
  
<span data-ttu-id="b0d4c-332">Таж</span><span class="sxs-lookup"><span data-stu-id="b0d4c-332">taj</span></span>
  
<span data-ttu-id="b0d4c-333">Таж #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-333">taj#</span></span>
  
<span data-ttu-id="b0d4c-334">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-334">ssn</span></span>
  
<span data-ttu-id="b0d4c-335">SSN</span><span class="sxs-lookup"><span data-stu-id="b0d4c-335">ssn#</span></span>
  
<span data-ttu-id="b0d4c-336">социальное страхование нет</span><span class="sxs-lookup"><span data-stu-id="b0d4c-336">social security no</span></span>
  
<span data-ttu-id="b0d4c-337">áфа</span><span class="sxs-lookup"><span data-stu-id="b0d4c-337">áfa</span></span>
  
<span data-ttu-id="b0d4c-338">кöзöссéги адóсзáм</span><span class="sxs-lookup"><span data-stu-id="b0d4c-338">közösségi adószám</span></span>
  
<span data-ttu-id="b0d4c-339">áлталáнос форгалми адó сзáм</span><span class="sxs-lookup"><span data-stu-id="b0d4c-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="b0d4c-340">хоззáадоттéртéк адó</span><span class="sxs-lookup"><span data-stu-id="b0d4c-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="b0d4c-341">áфа сзáм</span><span class="sxs-lookup"><span data-stu-id="b0d4c-341">áfa szám</span></span>
  
<span data-ttu-id="b0d4c-342">магяр áфа сзáм</span><span class="sxs-lookup"><span data-stu-id="b0d4c-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="b0d4c-343">Португалия</span><span class="sxs-lookup"><span data-stu-id="b0d4c-343">Portugal</span></span>

<span data-ttu-id="b0d4c-344">Дополнительные сведения можно найти в разделе "номер карты для Португалия" в разделе [сведения о типах конфиденциальной информации для поиска](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0d4c-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="b0d4c-345">Испания</span><span class="sxs-lookup"><span data-stu-id="b0d4c-345">Spain</span></span>

<span data-ttu-id="b0d4c-346">Дополнительные сведения см. в разделе "номер социального страхования для Испании (SSN)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0d4c-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="b0d4c-347">Швеция</span><span class="sxs-lookup"><span data-stu-id="b0d4c-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="b0d4c-348">Формат</span><span class="sxs-lookup"><span data-stu-id="b0d4c-348">Format</span></span>

<span data-ttu-id="b0d4c-349">12 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="b0d4c-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0d4c-350">Шаблон</span><span class="sxs-lookup"><span data-stu-id="b0d4c-350">Pattern</span></span>

<span data-ttu-id="b0d4c-351">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-351">12 digits:</span></span>
  
-  <span data-ttu-id="b0d4c-352">Восемь цифр, которые соответствуют дате рождения (ГГГГММДД)</span><span class="sxs-lookup"><span data-stu-id="b0d4c-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="b0d4c-353">Три цифры, которые соответствуют серийному номеру, где:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="b0d4c-354">Последняя цифра в числовом номере указывает на пол, назначая нечетное число для пола и четное число для розетки.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="b0d4c-355">До 1990, назначение серийного номера соответствует району, в котором был выпущен номер, или (если он родился до 1947), где он был удален, в соответствии с налоговыми записями 1 января 1947, с помощью специального кода (как правило, 9 в качестве седьмой цифры). иммигрантс</span><span class="sxs-lookup"><span data-stu-id="b0d4c-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="b0d4c-356">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="b0d4c-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0d4c-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="b0d4c-357">Checksum</span></span>

<span data-ttu-id="b0d4c-358">Да</span><span class="sxs-lookup"><span data-stu-id="b0d4c-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0d4c-359">Определение</span><span class="sxs-lookup"><span data-stu-id="b0d4c-359">Definition</span></span>

<span data-ttu-id="b0d4c-360">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-361">Функция `Func_sweden_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0d4c-362">Найдено ключевое `Keywords_sweden_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="b0d4c-363">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="b0d4c-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0d4c-364">Функция `Func_sweden_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="b0d4c-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="b0d4c-365">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="b0d4c-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="b0d4c-366">Кэйвордс_сведен_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="b0d4c-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="b0d4c-367">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-367">personal id number</span></span>
  
<span data-ttu-id="b0d4c-368">identification number
</span><span class="sxs-lookup"><span data-stu-id="b0d4c-368">identification number</span></span>
  
<span data-ttu-id="b0d4c-369">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="b0d4c-369">personal id no</span></span>
  
<span data-ttu-id="b0d4c-370">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="b0d4c-370">identity no</span></span>
  
<span data-ttu-id="b0d4c-371">Идентификация нет</span><span class="sxs-lookup"><span data-stu-id="b0d4c-371">identification no</span></span>
  
<span data-ttu-id="b0d4c-372">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-372">personal identification no</span></span>
  
<span data-ttu-id="b0d4c-373">Идентификатор персоннуммер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-373">personnummer id</span></span>
  
<span data-ttu-id="b0d4c-374">Идентификатор персонлигт — нуммер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-374">personligt id-nummer</span></span>
  
<span data-ttu-id="b0d4c-375">Идентификатор уникт — нуммер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-375">unikt id-nummer</span></span>
  
<span data-ttu-id="b0d4c-376">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="b0d4c-376">personnummer</span></span>
  
<span data-ttu-id="b0d4c-377">идентификатионснумрет</span><span class="sxs-lookup"><span data-stu-id="b0d4c-377">identifikationsnumret</span></span>
  
<span data-ttu-id="b0d4c-378">персоннуммер #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-378">personnummer#</span></span>
  
<span data-ttu-id="b0d4c-379">идентификатионснумрет #</span><span class="sxs-lookup"><span data-stu-id="b0d4c-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0d4c-380">См. также</span><span class="sxs-lookup"><span data-stu-id="b0d4c-380">See also</span></span>

[<span data-ttu-id="b0d4c-381">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="b0d4c-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

