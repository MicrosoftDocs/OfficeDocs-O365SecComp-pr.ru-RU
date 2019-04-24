---
title: Номер социального страхования ЕС или эквивалентный идентификатор
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает номер социального страхования ЕС или эквивалентный тип конфиденциальной информации. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: c0c808eafa52209c79f3b4e8a2113f587fd8a771
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255557"
---
# <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="d0d31-104">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="d0d31-104">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="d0d31-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС или эквивалентный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="d0d31-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Social Security Number (SSN) or Equivalent ID sensitive information type.</span></span> <span data-ttu-id="d0d31-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="d0d31-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="d0d31-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="d0d31-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="d0d31-108">Format</span><span class="sxs-lookup"><span data-stu-id="d0d31-108">Format</span></span>

<span data-ttu-id="d0d31-109">10 цифр в указанном формате</span><span class="sxs-lookup"><span data-stu-id="d0d31-109">10 digits in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d0d31-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d0d31-110">Pattern</span></span>

<span data-ttu-id="d0d31-111">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="d0d31-111">10 digits:</span></span>
  
-  <span data-ttu-id="d0d31-112">Три цифры, соответствующие серийному номеру.</span><span class="sxs-lookup"><span data-stu-id="d0d31-112">Three digits that correspond to a serial number</span></span> 
    
- <span data-ttu-id="d0d31-113">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="d0d31-113">One check digit</span></span>
    
- <span data-ttu-id="d0d31-114">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="d0d31-114">Six digits that correspond to the birth date (DDMMYY)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d0d31-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="d0d31-115">Checksum</span></span>

<span data-ttu-id="d0d31-116">Да</span><span class="sxs-lookup"><span data-stu-id="d0d31-116">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d0d31-117">Определение</span><span class="sxs-lookup"><span data-stu-id="d0d31-117">Definition</span></span>

<span data-ttu-id="d0d31-118">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-118">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-119">Функция `Func_austria_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-119">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d0d31-120">Найдено ключевое `Keywords_austria_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="d0d31-120">A keyword from  `Keywords_austria_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="d0d31-121">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-122">Функция `Func_austria_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-122">The function  `Func_austria_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d0d31-123">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="d0d31-123">Keywords</span></span>

#### <a name="keywordsaustriaeussnorequivalent"></a><span data-ttu-id="d0d31-124">Кэйвордс_аустриа_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="d0d31-124">Keywords_austria_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="d0d31-125">социальное страхование нет</span><span class="sxs-lookup"><span data-stu-id="d0d31-125">social security no</span></span>
  
<span data-ttu-id="d0d31-126">social security number</span><span class="sxs-lookup"><span data-stu-id="d0d31-126">social security number</span></span>
  
<span data-ttu-id="d0d31-127">social security code</span><span class="sxs-lookup"><span data-stu-id="d0d31-127">social security code</span></span>
  
<span data-ttu-id="d0d31-128">страховой номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-128">insurance number</span></span>
  
<span data-ttu-id="d0d31-129">Австрийский SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-129">austrian ssn</span></span>
  
<span data-ttu-id="d0d31-130">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-130">ssn#</span></span>
  
<span data-ttu-id="d0d31-131">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-131">ssn</span></span>
  
<span data-ttu-id="d0d31-132">код страхования</span><span class="sxs-lookup"><span data-stu-id="d0d31-132">insurance code</span></span>
  
<span data-ttu-id="d0d31-133">код страхования</span><span class="sxs-lookup"><span data-stu-id="d0d31-133">insurance code#</span></span>
  
<span data-ttu-id="d0d31-134">соЦиалсекуритино #</span><span class="sxs-lookup"><span data-stu-id="d0d31-134">socialsecurityno#</span></span>
  
<span data-ttu-id="d0d31-135">созиалверсичерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="d0d31-135">sozialversicherungsnummer</span></span>
  
<span data-ttu-id="d0d31-136">созиале сичерхеит Кеин</span><span class="sxs-lookup"><span data-stu-id="d0d31-136">soziale sicherheit kein</span></span>
  
<span data-ttu-id="d0d31-137">версичерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="d0d31-137">versicherungsnummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="d0d31-138">Бельгия</span><span class="sxs-lookup"><span data-stu-id="d0d31-138">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="d0d31-139">Format</span><span class="sxs-lookup"><span data-stu-id="d0d31-139">Format</span></span>

<span data-ttu-id="d0d31-140">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="d0d31-140">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d0d31-141">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d0d31-141">Pattern</span></span>

<span data-ttu-id="d0d31-142">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="d0d31-142">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d0d31-143">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="d0d31-143">Checksum</span></span>

<span data-ttu-id="d0d31-144">Да</span><span class="sxs-lookup"><span data-stu-id="d0d31-144">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d0d31-145">Определение</span><span class="sxs-lookup"><span data-stu-id="d0d31-145">Definition</span></span>

<span data-ttu-id="d0d31-146">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-146">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-147">Функция `Func_belgium_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-147">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d0d31-148">Найдено ключевое `Keywords_belgium_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="d0d31-148">A keyword from  `Keywords_belgium_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="d0d31-149">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-149">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-150">Функция `Func_belgium_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-150">The function  `Func_belgium_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d0d31-151">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="d0d31-151">Keywords</span></span>

#### <a name="keywordsbelgiumeussnorequivalent"></a><span data-ttu-id="d0d31-152">Кэйвордс_белгиум_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="d0d31-152">Keywords_belgium_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="d0d31-153">Бельгийский национальный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-153">belgian national number</span></span>
  
<span data-ttu-id="d0d31-154">номер страны</span><span class="sxs-lookup"><span data-stu-id="d0d31-154">national number</span></span>
  
<span data-ttu-id="d0d31-155">social security number</span><span class="sxs-lookup"><span data-stu-id="d0d31-155">social security number</span></span>
  
<span data-ttu-id="d0d31-156">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-156">nationalnumber#</span></span>
  
<span data-ttu-id="d0d31-157">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-157">ssn#</span></span>
  
<span data-ttu-id="d0d31-158">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-158">ssn</span></span>
  
<span data-ttu-id="d0d31-159">натионалнумбер</span><span class="sxs-lookup"><span data-stu-id="d0d31-159">nationalnumber</span></span>
  
<span data-ttu-id="d0d31-160">БНН #</span><span class="sxs-lookup"><span data-stu-id="d0d31-160">bnn#</span></span>
  
<span data-ttu-id="d0d31-161">БНН</span><span class="sxs-lookup"><span data-stu-id="d0d31-161">bnn</span></span>
  
<span data-ttu-id="d0d31-162">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-162">personal id number</span></span>
  
<span data-ttu-id="d0d31-163">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-163">personalidnumber#</span></span>
  
<span data-ttu-id="d0d31-164">Национальный нумéро</span><span class="sxs-lookup"><span data-stu-id="d0d31-164">numéro national</span></span>
  
<span data-ttu-id="d0d31-165">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="d0d31-165">numéro de sécurité</span></span>
  
<span data-ttu-id="d0d31-166">нумéро д'ассурé</span><span class="sxs-lookup"><span data-stu-id="d0d31-166">numéro d'assuré</span></span>
  
<span data-ttu-id="d0d31-167">Идентификация National</span><span class="sxs-lookup"><span data-stu-id="d0d31-167">identifiant national</span></span>
  
<span data-ttu-id="d0d31-168">идентифиантнатионал #</span><span class="sxs-lookup"><span data-stu-id="d0d31-168">identifiantnational#</span></span>
  
<span data-ttu-id="d0d31-169">нумéронатионал #</span><span class="sxs-lookup"><span data-stu-id="d0d31-169">numéronational#</span></span>
  
## <a name="croatia"></a><span data-ttu-id="d0d31-170">Хорватия</span><span class="sxs-lookup"><span data-stu-id="d0d31-170">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="d0d31-171">Format</span><span class="sxs-lookup"><span data-stu-id="d0d31-171">Format</span></span>

<span data-ttu-id="d0d31-172">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="d0d31-172">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d0d31-173">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d0d31-173">Pattern</span></span>

 <span data-ttu-id="d0d31-174">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="d0d31-174">11 digits:</span></span> 
  
-  <span data-ttu-id="d0d31-175">Десять цифр</span><span class="sxs-lookup"><span data-stu-id="d0d31-175">Ten digits</span></span> 
    
- <span data-ttu-id="d0d31-176">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="d0d31-176">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d0d31-177">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="d0d31-177">Checksum</span></span>

<span data-ttu-id="d0d31-178">Да</span><span class="sxs-lookup"><span data-stu-id="d0d31-178">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d0d31-179">Определение</span><span class="sxs-lookup"><span data-stu-id="d0d31-179">Definition</span></span>

<span data-ttu-id="d0d31-180">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-180">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-181">Функция `Func_croatia_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-181">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d0d31-182">Найдено ключевое `Keywords_croatia_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="d0d31-182">A keyword from  `Keywords_croatia_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="d0d31-183">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-184">Функция `Func_croatia_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-184">The function  `Func_croatia_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d0d31-185">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="d0d31-185">Keywords</span></span>

#### <a name="keywordscroatiaeussnorequivalent"></a><span data-ttu-id="d0d31-186">Кэйвордс_кроатиа_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="d0d31-186">Keywords_croatia_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="d0d31-187">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-187">personal identification number</span></span>
  
<span data-ttu-id="d0d31-188">основной номер в соотношении</span><span class="sxs-lookup"><span data-stu-id="d0d31-188">master citizen number</span></span>
  
<span data-ttu-id="d0d31-189">national identification number</span><span class="sxs-lookup"><span data-stu-id="d0d31-189">national identification number</span></span>
  
<span data-ttu-id="d0d31-190">social security number</span><span class="sxs-lookup"><span data-stu-id="d0d31-190">social security number</span></span>
  
<span data-ttu-id="d0d31-191">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-191">nationalnumber#</span></span>
  
<span data-ttu-id="d0d31-192">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-192">ssn#</span></span>
  
<span data-ttu-id="d0d31-193">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-193">ssn</span></span>
  
<span data-ttu-id="d0d31-194">натионалнумбер</span><span class="sxs-lookup"><span data-stu-id="d0d31-194">nationalnumber</span></span>
  
<span data-ttu-id="d0d31-195">БНН #</span><span class="sxs-lookup"><span data-stu-id="d0d31-195">bnn#</span></span>
  
<span data-ttu-id="d0d31-196">БНН</span><span class="sxs-lookup"><span data-stu-id="d0d31-196">bnn</span></span>
  
<span data-ttu-id="d0d31-197">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-197">personal id number</span></span>
  
<span data-ttu-id="d0d31-198">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-198">personalidnumber#</span></span>
  
<span data-ttu-id="d0d31-199">OIB</span><span class="sxs-lookup"><span data-stu-id="d0d31-199">oib</span></span>
  
<span data-ttu-id="d0d31-200">особни идентификаЦижски Брож</span><span class="sxs-lookup"><span data-stu-id="d0d31-200">osobni identifikacijski broj</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="d0d31-201">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="d0d31-201">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="d0d31-202">Format</span><span class="sxs-lookup"><span data-stu-id="d0d31-202">Format</span></span>

<span data-ttu-id="d0d31-203">Десять цифр и обратная косая черта в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="d0d31-203">Ten digits and a backslash in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d0d31-204">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d0d31-204">Pattern</span></span>

<span data-ttu-id="d0d31-205">Десять цифр и обратная косая черта:</span><span class="sxs-lookup"><span data-stu-id="d0d31-205">Ten digits and a backslash:</span></span>
  
- <span data-ttu-id="d0d31-206">Шесть цифр, соответствующих дате рождения (ГГММДД):</span><span class="sxs-lookup"><span data-stu-id="d0d31-206">Six digits that correspond to the birth date (YYMMDD):</span></span> 
    
- <span data-ttu-id="d0d31-207">Обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="d0d31-207">A backslash</span></span>
    
- <span data-ttu-id="d0d31-208">Три цифры, которые соответствуют серийному номеру, которые отделяют пользователей на одну и ту же дату.</span><span class="sxs-lookup"><span data-stu-id="d0d31-208">Three digits that correspond to a serial number that separates persons born on the same date</span></span>
    
- <span data-ttu-id="d0d31-209">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="d0d31-209">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d0d31-210">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="d0d31-210">Checksum</span></span>

<span data-ttu-id="d0d31-211">Да</span><span class="sxs-lookup"><span data-stu-id="d0d31-211">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d0d31-212">Определение</span><span class="sxs-lookup"><span data-stu-id="d0d31-212">Definition</span></span>

<span data-ttu-id="d0d31-213">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-213">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-214">Функция `Func_czech_republic_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-214">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d0d31-215">Найдено ключевое `Keywords_czech_republic_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="d0d31-215">A keyword from  `Keywords_czech_republic_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="d0d31-216">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-217">Функция `Func_czech_republic_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-217">The function  `Func_czech_republic_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d0d31-218">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="d0d31-218">Keywords</span></span>

#### <a name="keywordsczechrepubliceussnorequivalent"></a><span data-ttu-id="d0d31-219">Кэйвордс_кзеч_републик_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="d0d31-219">Keywords_czech_republic_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="d0d31-220">номер рождения</span><span class="sxs-lookup"><span data-stu-id="d0d31-220">birth number</span></span>
  
<span data-ttu-id="d0d31-221">national identification number</span><span class="sxs-lookup"><span data-stu-id="d0d31-221">national identification number</span></span>
  
<span data-ttu-id="d0d31-222">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-222">personal identification number</span></span>
  
<span data-ttu-id="d0d31-223">social security number</span><span class="sxs-lookup"><span data-stu-id="d0d31-223">social security number</span></span>
  
<span data-ttu-id="d0d31-224">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-224">nationalnumber#</span></span>
  
<span data-ttu-id="d0d31-225">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-225">ssn#</span></span>
  
<span data-ttu-id="d0d31-226">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-226">ssn</span></span>
  
<span data-ttu-id="d0d31-227">номер страны</span><span class="sxs-lookup"><span data-stu-id="d0d31-227">national number</span></span>
  
<span data-ttu-id="d0d31-228">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-228">personal id number</span></span>
  
<span data-ttu-id="d0d31-229">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-229">personalidnumber#</span></span>
  
<span data-ttu-id="d0d31-230">рč</span><span class="sxs-lookup"><span data-stu-id="d0d31-230">rč</span></span>
  
<span data-ttu-id="d0d31-231">роднé číсло</span><span class="sxs-lookup"><span data-stu-id="d0d31-231">rodné číslo</span></span>
  
<span data-ttu-id="d0d31-232">родне Цисло</span><span class="sxs-lookup"><span data-stu-id="d0d31-232">rodne cislo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="d0d31-233">Дания</span><span class="sxs-lookup"><span data-stu-id="d0d31-233">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="d0d31-234">Format</span><span class="sxs-lookup"><span data-stu-id="d0d31-234">Format</span></span>

<span data-ttu-id="d0d31-235">Десять цифр и дефис в заданном шаблоне</span><span class="sxs-lookup"><span data-stu-id="d0d31-235">Ten digits and a hyphen in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d0d31-236">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d0d31-236">Pattern</span></span>

<span data-ttu-id="d0d31-237">Десять цифр и дефис:</span><span class="sxs-lookup"><span data-stu-id="d0d31-237">Ten digits and a hyphen:</span></span>
  
- <span data-ttu-id="d0d31-238">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="d0d31-238">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="d0d31-239">дефис;</span><span class="sxs-lookup"><span data-stu-id="d0d31-239">A hyphen</span></span>
    
- <span data-ttu-id="d0d31-240">Четыре цифры, которые соответствуют порядковому номеру</span><span class="sxs-lookup"><span data-stu-id="d0d31-240">Four digits that correspond to a sequence number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d0d31-241">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="d0d31-241">Checksum</span></span>

<span data-ttu-id="d0d31-242">Да</span><span class="sxs-lookup"><span data-stu-id="d0d31-242">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d0d31-243">Определение</span><span class="sxs-lookup"><span data-stu-id="d0d31-243">Definition</span></span>

<span data-ttu-id="d0d31-244">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-244">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-245">Функция `Func_denmark_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-245">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d0d31-246">Найдено ключевое `Keywords_denmark_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="d0d31-246">A keyword from  `Keywords_denmark_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="d0d31-247">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-248">Функция `Func_denmark_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-248">The function  `Func_denmark_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d0d31-249">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="d0d31-249">Keywords</span></span>

#### <a name="keywordsdenmarkeussnorequivalent"></a><span data-ttu-id="d0d31-250">Кэйвордс_денмарк_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="d0d31-250">Keywords_denmark_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="d0d31-251">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-251">personal identification number</span></span>
  
<span data-ttu-id="d0d31-252">national identification number</span><span class="sxs-lookup"><span data-stu-id="d0d31-252">national identification number</span></span>
  
<span data-ttu-id="d0d31-253">social security number</span><span class="sxs-lookup"><span data-stu-id="d0d31-253">social security number</span></span>
  
<span data-ttu-id="d0d31-254">натионалнумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-254">nationalnumber#</span></span>
  
<span data-ttu-id="d0d31-255">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-255">ssn#</span></span>
  
<span data-ttu-id="d0d31-256">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-256">ssn</span></span>
  
<span data-ttu-id="d0d31-257">номер страны</span><span class="sxs-lookup"><span data-stu-id="d0d31-257">national number</span></span>
  
<span data-ttu-id="d0d31-258">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-258">personal id number</span></span>
  
<span data-ttu-id="d0d31-259">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-259">personalidnumber#</span></span>
  
<span data-ttu-id="d0d31-260">CPR — нуммер</span><span class="sxs-lookup"><span data-stu-id="d0d31-260">cpr-nummer</span></span>
  
<span data-ttu-id="d0d31-261">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="d0d31-261">personnummer</span></span>
  
## <a name="finland"></a><span data-ttu-id="d0d31-262">Финляндия</span><span class="sxs-lookup"><span data-stu-id="d0d31-262">Finland</span></span>

### <a name="format"></a><span data-ttu-id="d0d31-263">Format</span><span class="sxs-lookup"><span data-stu-id="d0d31-263">Format</span></span>

<span data-ttu-id="d0d31-264">11 символов в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="d0d31-264">An 11-character combination in the specified format</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d0d31-265">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d0d31-265">Pattern</span></span>

<span data-ttu-id="d0d31-266">Сочетание из 11 символов в указанном формате:</span><span class="sxs-lookup"><span data-stu-id="d0d31-266">An 11-character combination in the specified format:</span></span>
  
-  <span data-ttu-id="d0d31-267">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="d0d31-267">Six digits</span></span> 
    
- <span data-ttu-id="d0d31-268">Один из следующих экземпляров:</span><span class="sxs-lookup"><span data-stu-id="d0d31-268">One instance of one of the following:</span></span>
    
  - <span data-ttu-id="d0d31-269">Символ "плюс"</span><span class="sxs-lookup"><span data-stu-id="d0d31-269">Plus symbol</span></span>
    
  - <span data-ttu-id="d0d31-270">Символ "минус"</span><span class="sxs-lookup"><span data-stu-id="d0d31-270">Minus symbol</span></span>
    
  - <span data-ttu-id="d0d31-271">Буква "A" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="d0d31-271">The letter "A" (not case-sensitive)</span></span>
    
- <span data-ttu-id="d0d31-272">Три цифры</span><span class="sxs-lookup"><span data-stu-id="d0d31-272">Three digits</span></span>
    
- <span data-ttu-id="d0d31-273">Одна буква или одна цифра</span><span class="sxs-lookup"><span data-stu-id="d0d31-273">One letter or one digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d0d31-274">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="d0d31-274">Checksum</span></span>

<span data-ttu-id="d0d31-275">Да</span><span class="sxs-lookup"><span data-stu-id="d0d31-275">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d0d31-276">Определение</span><span class="sxs-lookup"><span data-stu-id="d0d31-276">Definition</span></span>

<span data-ttu-id="d0d31-277">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-277">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-278">Функция `Func_finland_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-278">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d0d31-279">Найдено ключевое `Keywords_finland_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="d0d31-279">A keyword from  `Keywords_finland_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="d0d31-280">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-281">Функция `Func_finland_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-281">The function  `Func_finland_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d0d31-282">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="d0d31-282">Keywords</span></span>

#### <a name="keywordsfinlandeussnorequivalent"></a><span data-ttu-id="d0d31-283">Кэйвордс_финланд_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="d0d31-283">Keywords_finland_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="d0d31-284">identification number</span><span class="sxs-lookup"><span data-stu-id="d0d31-284">identification number</span></span>
  
<span data-ttu-id="d0d31-285">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="d0d31-285">personal id</span></span>
  
<span data-ttu-id="d0d31-286">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-286">identity number</span></span>
  
<span data-ttu-id="d0d31-287">Финский национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-287">finnish national id number</span></span>
  
<span data-ttu-id="d0d31-288">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-288">personalidnumber#</span></span>
  
<span data-ttu-id="d0d31-289">national identification number</span><span class="sxs-lookup"><span data-stu-id="d0d31-289">national identification number</span></span>
  
<span data-ttu-id="d0d31-290">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-290">id number</span></span>
  
<span data-ttu-id="d0d31-291">код страны</span><span class="sxs-lookup"><span data-stu-id="d0d31-291">national id no.</span></span>
  
<span data-ttu-id="d0d31-292">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-292">national id number</span></span>
  
<span data-ttu-id="d0d31-293">ID No</span><span class="sxs-lookup"><span data-stu-id="d0d31-293">id no</span></span>
  
<span data-ttu-id="d0d31-294">туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="d0d31-294">tunnistenumero</span></span>
  
<span data-ttu-id="d0d31-295">хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="d0d31-295">henkilötunnus</span></span>
  
<span data-ttu-id="d0d31-296">иксилöллинен хенкилöкохтаинен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="d0d31-296">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="d0d31-297">аинутлаатуинен хенкилöкохтаинен туннус</span><span class="sxs-lookup"><span data-stu-id="d0d31-297">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="d0d31-298">идентититти нумеро</span><span class="sxs-lookup"><span data-stu-id="d0d31-298">identiteetti numero</span></span>
  
<span data-ttu-id="d0d31-299">Суомен кансаллинен хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="d0d31-299">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="d0d31-300">хенкилöтуннуснумеро #</span><span class="sxs-lookup"><span data-stu-id="d0d31-300">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="d0d31-301">кансаллисен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="d0d31-301">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="d0d31-302">туннуснумеро</span><span class="sxs-lookup"><span data-stu-id="d0d31-302">tunnusnumero</span></span>
  
<span data-ttu-id="d0d31-303">кансаллинен туннус нумеро</span><span class="sxs-lookup"><span data-stu-id="d0d31-303">kansallinen tunnus numero</span></span>
  
<span data-ttu-id="d0d31-304">Хету</span><span class="sxs-lookup"><span data-stu-id="d0d31-304">hetu</span></span>
  
## <a name="france"></a><span data-ttu-id="d0d31-305">Франция</span><span class="sxs-lookup"><span data-stu-id="d0d31-305">France</span></span>

<span data-ttu-id="d0d31-306">Дополнительные сведения см. в разделе "номер социального страхования для Франции (INSEE)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d0d31-306">For details, see the section "France Social Security Number (INSEE)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="d0d31-307">Германия</span><span class="sxs-lookup"><span data-stu-id="d0d31-307">Germany</span></span>

<span data-ttu-id="d0d31-308">Дополнительные сведения можно найти в разделе "номер идентификационной карточки для Германии" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d0d31-308">For details, see the section "Germany Identity Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="d0d31-309">Греция</span><span class="sxs-lookup"><span data-stu-id="d0d31-309">Greece</span></span>

<span data-ttu-id="d0d31-310">Дополнительные сведения можно найти в разделе "Греция National ID Card", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d0d31-310">For details, see the section "Greece National ID Card" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="hungary"></a><span data-ttu-id="d0d31-311">Венгрия</span><span class="sxs-lookup"><span data-stu-id="d0d31-311">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="d0d31-312">Format</span><span class="sxs-lookup"><span data-stu-id="d0d31-312">Format</span></span>

<span data-ttu-id="d0d31-313">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="d0d31-313">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d0d31-314">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d0d31-314">Pattern</span></span>

<span data-ttu-id="d0d31-315">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="d0d31-315">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="d0d31-316">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="d0d31-316">Checksum</span></span>

<span data-ttu-id="d0d31-317">Да</span><span class="sxs-lookup"><span data-stu-id="d0d31-317">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d0d31-318">Определение</span><span class="sxs-lookup"><span data-stu-id="d0d31-318">Definition</span></span>

<span data-ttu-id="d0d31-319">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-319">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-320">Функция `Func_hungary_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-320">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d0d31-321">Найдено ключевое `Keywords_hungary_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="d0d31-321">A keyword from  `Keywords_hungary_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="d0d31-322">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-322">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-323">Функция `Func_hungary_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-323">The function  `Func_hungary_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d0d31-324">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="d0d31-324">Keywords</span></span>

#### <a name="keywordshungaryeussnorequivalent"></a><span data-ttu-id="d0d31-325">Кэйвордс_хунгари_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="d0d31-325">Keywords_hungary_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="d0d31-326">Венгерский номер социального страхования</span><span class="sxs-lookup"><span data-stu-id="d0d31-326">hungarian social security number</span></span>
  
<span data-ttu-id="d0d31-327">social security number</span><span class="sxs-lookup"><span data-stu-id="d0d31-327">social security number</span></span>
  
<span data-ttu-id="d0d31-328">соЦиалсекуритинумбер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-328">socialsecuritynumber#</span></span>
  
<span data-ttu-id="d0d31-329">хссн #</span><span class="sxs-lookup"><span data-stu-id="d0d31-329">hssn#</span></span>
  
<span data-ttu-id="d0d31-330">соЦиалсекуритинно</span><span class="sxs-lookup"><span data-stu-id="d0d31-330">socialsecuritynno</span></span>
  
<span data-ttu-id="d0d31-331">хссн</span><span class="sxs-lookup"><span data-stu-id="d0d31-331">hssn</span></span>
  
<span data-ttu-id="d0d31-332">Таж</span><span class="sxs-lookup"><span data-stu-id="d0d31-332">taj</span></span>
  
<span data-ttu-id="d0d31-333">Таж #</span><span class="sxs-lookup"><span data-stu-id="d0d31-333">taj#</span></span>
  
<span data-ttu-id="d0d31-334">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-334">ssn</span></span>
  
<span data-ttu-id="d0d31-335">SSN</span><span class="sxs-lookup"><span data-stu-id="d0d31-335">ssn#</span></span>
  
<span data-ttu-id="d0d31-336">социальное страхование нет</span><span class="sxs-lookup"><span data-stu-id="d0d31-336">social security no</span></span>
  
<span data-ttu-id="d0d31-337">áфа</span><span class="sxs-lookup"><span data-stu-id="d0d31-337">áfa</span></span>
  
<span data-ttu-id="d0d31-338">кöзöссéги адóсзáм</span><span class="sxs-lookup"><span data-stu-id="d0d31-338">közösségi adószám</span></span>
  
<span data-ttu-id="d0d31-339">áлталáнос форгалми адó сзáм</span><span class="sxs-lookup"><span data-stu-id="d0d31-339">általános forgalmi adó szám</span></span>
  
<span data-ttu-id="d0d31-340">хоззáадоттéртéк адó</span><span class="sxs-lookup"><span data-stu-id="d0d31-340">hozzáadottérték adó</span></span>
  
<span data-ttu-id="d0d31-341">áфа сзáм</span><span class="sxs-lookup"><span data-stu-id="d0d31-341">áfa szám</span></span>
  
<span data-ttu-id="d0d31-342">магяр áфа сзáм</span><span class="sxs-lookup"><span data-stu-id="d0d31-342">magyar áfa szám</span></span>
  
## <a name="portugal"></a><span data-ttu-id="d0d31-343">Португалия</span><span class="sxs-lookup"><span data-stu-id="d0d31-343">Portugal</span></span>

<span data-ttu-id="d0d31-344">Дополнительные сведения можно найти в разделе "номер карты для Португалия" в разделе [сведения о типах конфиденциальной информации для поиска](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d0d31-344">For details, see the section "Portugal Citizen Card Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="spain"></a><span data-ttu-id="d0d31-345">Испания</span><span class="sxs-lookup"><span data-stu-id="d0d31-345">Spain</span></span>

<span data-ttu-id="d0d31-346">Дополнительные сведения см. в разделе "номер социального страхования для Испании (SSN)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="d0d31-346">For details, see the section "Spain Social Security Number (SSN)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="sweden"></a><span data-ttu-id="d0d31-347">Швеция</span><span class="sxs-lookup"><span data-stu-id="d0d31-347">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="d0d31-348">Format</span><span class="sxs-lookup"><span data-stu-id="d0d31-348">Format</span></span>

<span data-ttu-id="d0d31-349">12 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="d0d31-349">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="d0d31-350">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d0d31-350">Pattern</span></span>

<span data-ttu-id="d0d31-351">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="d0d31-351">12 digits:</span></span>
  
-  <span data-ttu-id="d0d31-352">Восемь цифр, которые соответствуют дате рождения (ГГГГММДД)</span><span class="sxs-lookup"><span data-stu-id="d0d31-352">Eight digits that correspond to the birth date (YYYYMMDD)</span></span> 
    
- <span data-ttu-id="d0d31-353">Три цифры, которые соответствуют серийному номеру, где:</span><span class="sxs-lookup"><span data-stu-id="d0d31-353">Three digits that correspond to a serial number where:</span></span> 
    
  - <span data-ttu-id="d0d31-354">Последняя цифра в числовом номере указывает на пол, назначая нечетное число для пола и четное число для розетки.</span><span class="sxs-lookup"><span data-stu-id="d0d31-354">The last digit in the serial number indicates gender by the assignment of an odd number for male and an even number for female</span></span>
    
  - <span data-ttu-id="d0d31-355">До 1990, назначение серийного номера соответствует району, в котором был выпущен номер, или (если он родился до 1947), где он был удален, в соответствии с налоговыми записями 1 января 1947, с помощью специального кода (как правило, 9 в качестве седьмой цифры). иммигрантс</span><span class="sxs-lookup"><span data-stu-id="d0d31-355">Up to 1990, the assignment of serial number corresponded to the county where the bearer of the number was born or (if born before 1947) where he/she had been living, according to tax records, on January 1, 1947, with a special code (usually 9 as the 7th digit) for immigrants</span></span> 
    
- <span data-ttu-id="d0d31-356">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="d0d31-356">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="d0d31-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="d0d31-357">Checksum</span></span>

<span data-ttu-id="d0d31-358">Да</span><span class="sxs-lookup"><span data-stu-id="d0d31-358">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="d0d31-359">Определение</span><span class="sxs-lookup"><span data-stu-id="d0d31-359">Definition</span></span>

<span data-ttu-id="d0d31-360">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-360">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-361">Функция `Func_sweden_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-361">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="d0d31-362">Найдено ключевое `Keywords_sweden_eu_ssn_or_equivalent` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="d0d31-362">A keyword from  `Keywords_sweden_eu_ssn_or_equivalent` is found.</span></span> 
    
<span data-ttu-id="d0d31-363">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="d0d31-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="d0d31-364">Функция `Func_sweden_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="d0d31-364">The function  `Func_sweden_eu_ssn_or_equivalent` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="d0d31-365">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="d0d31-365">Keywords</span></span>

#### <a name="keywordsswedeneussnorequivalent"></a><span data-ttu-id="d0d31-366">Кэйвордс_сведен_еу_ссн_ор_екуивалент</span><span class="sxs-lookup"><span data-stu-id="d0d31-366">Keywords_sweden_eu_ssn_or_equivalent</span></span>

<span data-ttu-id="d0d31-367">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-367">personal id number</span></span>
  
<span data-ttu-id="d0d31-368">identification number</span><span class="sxs-lookup"><span data-stu-id="d0d31-368">identification number</span></span>
  
<span data-ttu-id="d0d31-369">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="d0d31-369">personal id no</span></span>
  
<span data-ttu-id="d0d31-370">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="d0d31-370">identity no</span></span>
  
<span data-ttu-id="d0d31-371">Идентификация нет</span><span class="sxs-lookup"><span data-stu-id="d0d31-371">identification no</span></span>
  
<span data-ttu-id="d0d31-372">персональный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="d0d31-372">personal identification no</span></span>
  
<span data-ttu-id="d0d31-373">Идентификатор персоннуммер</span><span class="sxs-lookup"><span data-stu-id="d0d31-373">personnummer id</span></span>
  
<span data-ttu-id="d0d31-374">Идентификатор персонлигт — нуммер</span><span class="sxs-lookup"><span data-stu-id="d0d31-374">personligt id-nummer</span></span>
  
<span data-ttu-id="d0d31-375">Идентификатор уникт — нуммер</span><span class="sxs-lookup"><span data-stu-id="d0d31-375">unikt id-nummer</span></span>
  
<span data-ttu-id="d0d31-376">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="d0d31-376">personnummer</span></span>
  
<span data-ttu-id="d0d31-377">идентификатионснумрет</span><span class="sxs-lookup"><span data-stu-id="d0d31-377">identifikationsnumret</span></span>
  
<span data-ttu-id="d0d31-378">персоннуммер #</span><span class="sxs-lookup"><span data-stu-id="d0d31-378">personnummer#</span></span>
  
<span data-ttu-id="d0d31-379">идентификатионснумрет #</span><span class="sxs-lookup"><span data-stu-id="d0d31-379">identifikationsnumret#</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0d31-380">См. также</span><span class="sxs-lookup"><span data-stu-id="d0d31-380">See also</span></span>

[<span data-ttu-id="d0d31-381">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="d0d31-381">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

