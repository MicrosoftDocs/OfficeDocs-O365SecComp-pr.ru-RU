---
title: Идентификационный номер налогоплательщика ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации для идентификационного номера ЕС. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: 4914ff078695519c2a298190d82c86a6abebceb9
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410914"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="2ad59-104">Идентификационный номер налогоплательщика ЕС</span><span class="sxs-lookup"><span data-stu-id="2ad59-104">EU Tax Identification Number</span></span>

<span data-ttu-id="2ad59-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации налогоплательщика (TIN).</span><span class="sxs-lookup"><span data-stu-id="2ad59-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="2ad59-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="2ad59-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="2ad59-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="2ad59-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-108">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-108">Format</span></span>

<span data-ttu-id="2ad59-109">Девять цифр с необязательным дефисом и косой чертой.</span><span class="sxs-lookup"><span data-stu-id="2ad59-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-110">Pattern</span></span>

<span data-ttu-id="2ad59-111">Девять цифр с необязательным дефисом и косой чертой.</span><span class="sxs-lookup"><span data-stu-id="2ad59-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="2ad59-112">Две цифры</span><span class="sxs-lookup"><span data-stu-id="2ad59-112">Two digits</span></span> 
    
- <span data-ttu-id="2ad59-113">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="2ad59-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="2ad59-114">Три цифры</span><span class="sxs-lookup"><span data-stu-id="2ad59-114">Three digits</span></span>
    
- <span data-ttu-id="2ad59-115">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="2ad59-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="2ad59-116">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="2ad59-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-117">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-117">Checksum</span></span>

<span data-ttu-id="2ad59-118">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-119">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-119">Definition</span></span>

<span data-ttu-id="2ad59-120">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-121">Функция `Func_austria_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-122">Найдено ключевое `Keywords_austria_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-123">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-124">Функция `Func_austria_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-125">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="2ad59-126">Кэйвордс_аустриа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-127">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-127">tax number</span></span>
  
<span data-ttu-id="2ad59-128">number</span><span class="sxs-lookup"><span data-stu-id="2ad59-128">number</span></span>
  
<span data-ttu-id="2ad59-129">Регистрационный номер налогоплательщика</span><span class="sxs-lookup"><span data-stu-id="2ad59-129">tax registration number</span></span>
  
<span data-ttu-id="2ad59-130">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-130">tax id</span></span>
  
<span data-ttu-id="2ad59-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="2ad59-131">st.nr.</span></span>
  
<span data-ttu-id="2ad59-132">стеуернуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="2ad59-133">Бельгия</span><span class="sxs-lookup"><span data-stu-id="2ad59-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-134">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-134">Format</span></span>

<span data-ttu-id="2ad59-135">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-136">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-136">Pattern</span></span>

<span data-ttu-id="2ad59-137">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="2ad59-137">11 digits:</span></span>
  
- <span data-ttu-id="2ad59-138">Две цифры</span><span class="sxs-lookup"><span data-stu-id="2ad59-138">Two digits</span></span>
    
- <span data-ttu-id="2ad59-139">"0" или "1"</span><span class="sxs-lookup"><span data-stu-id="2ad59-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="2ad59-140">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="2ad59-140">One digit</span></span>
    
- <span data-ttu-id="2ad59-141">"0" или "1" или "2" или "3"</span><span class="sxs-lookup"><span data-stu-id="2ad59-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="2ad59-142">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-143">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-143">Checksum</span></span>

<span data-ttu-id="2ad59-144">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-145">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-145">Definition</span></span>

<span data-ttu-id="2ad59-146">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-147">Регулярное выражение `Regex_belgium_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-148">Найдено ключевое `Keywords_belgium_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-149">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="2ad59-150">Кэйвордс_белгиум_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-151">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-151">tax number</span></span>
  
<span data-ttu-id="2ad59-152">Национальный регистрационный номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-152">national registration number</span></span>
  
<span data-ttu-id="2ad59-153">Регистрационный номер налогоплательщика</span><span class="sxs-lookup"><span data-stu-id="2ad59-153">tax registration number</span></span>
  
<span data-ttu-id="2ad59-154">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-154">tax id</span></span>
  
<span data-ttu-id="2ad59-155">включена</span><span class="sxs-lookup"><span data-stu-id="2ad59-155">nif</span></span>
  
<span data-ttu-id="2ad59-156">включена</span><span class="sxs-lookup"><span data-stu-id="2ad59-156">nif#</span></span>
  
<span data-ttu-id="2ad59-157">нумéро de регистре National</span><span class="sxs-lookup"><span data-stu-id="2ad59-157">numéro de registre national</span></span>
  
<span data-ttu-id="2ad59-158">нумéро д'идентификатион Фин.</span><span class="sxs-lookup"><span data-stu-id="2ad59-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="2ad59-159">Болгария</span><span class="sxs-lookup"><span data-stu-id="2ad59-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-160">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-160">Format</span></span>

<span data-ttu-id="2ad59-161">Десять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-162">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-162">Pattern</span></span>

<span data-ttu-id="2ad59-163">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-164">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-164">Checksum</span></span>

<span data-ttu-id="2ad59-165">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-166">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-166">Definition</span></span>

<span data-ttu-id="2ad59-167">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-168">Функция `Func_bulgaria_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-169">Найдено ключевое `Keywords_bulgaria_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-170">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-171">Функция `Func_bulgaria_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-172">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="2ad59-173">Кэйвордс_булгариа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-174">Букн</span><span class="sxs-lookup"><span data-stu-id="2ad59-174">bucn</span></span>
  
<span data-ttu-id="2ad59-175">единое гражданское число</span><span class="sxs-lookup"><span data-stu-id="2ad59-175">uniform civil number</span></span>
  
<span data-ttu-id="2ad59-176">Букн #</span><span class="sxs-lookup"><span data-stu-id="2ad59-176">bucn#</span></span>
  
<span data-ttu-id="2ad59-177">униформЦивилнумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="2ad59-178">унифицированный гражданский идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-178">uniform civil id</span></span>
  
<span data-ttu-id="2ad59-179">равномерный гражданский номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-179">uniform civil no</span></span>
  
<span data-ttu-id="2ad59-180">ЕГН</span><span class="sxs-lookup"><span data-stu-id="2ad59-180">egn</span></span>
  
<span data-ttu-id="2ad59-181">номер унифицированного гражданства болгарского языка</span><span class="sxs-lookup"><span data-stu-id="2ad59-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="2ad59-182">униформЦивилно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-182">uniformcivilno#</span></span>
  
<span data-ttu-id="2ad59-183">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="2ad59-183">egn#</span></span>
  
<span data-ttu-id="2ad59-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-184">униформ граждански номер</span></span>
  
<span data-ttu-id="2ad59-185">Идентификатор униформ</span><span class="sxs-lookup"><span data-stu-id="2ad59-185">униформ id</span></span>
  
<span data-ttu-id="2ad59-186">униформ граждански ID</span><span class="sxs-lookup"><span data-stu-id="2ad59-186">униформ граждански id</span></span>
  
<span data-ttu-id="2ad59-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="2ad59-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="2ad59-188">Хорватия</span><span class="sxs-lookup"><span data-stu-id="2ad59-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-189">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-189">Format</span></span>

<span data-ttu-id="2ad59-190">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-191">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-191">Pattern</span></span>

<span data-ttu-id="2ad59-192">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="2ad59-192">11 digits:</span></span>
  
- <span data-ttu-id="2ad59-193">Десять цифр, выбран случайным образом</span><span class="sxs-lookup"><span data-stu-id="2ad59-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="2ad59-194">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="2ad59-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-195">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-195">Checksum</span></span>

<span data-ttu-id="2ad59-196">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-197">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-197">Definition</span></span>

<span data-ttu-id="2ad59-198">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-199">Функция `Func_croatia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-200">Найдено ключевое `Keywords_croatia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-201">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-202">Функция `Func_croatia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-203">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="2ad59-204">Кэйвордс_кроатиа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-205">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-205">tax number</span></span>
  
<span data-ttu-id="2ad59-206">см</span><span class="sxs-lookup"><span data-stu-id="2ad59-206">tax</span></span>
  
<span data-ttu-id="2ad59-207">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-207">tax id</span></span>
  
<span data-ttu-id="2ad59-208">oid</span><span class="sxs-lookup"><span data-stu-id="2ad59-208">oid</span></span>
  
<span data-ttu-id="2ad59-209">идентификатора</span><span class="sxs-lookup"><span data-stu-id="2ad59-209">oid#</span></span>
  
<span data-ttu-id="2ad59-210">порезни Брож</span><span class="sxs-lookup"><span data-stu-id="2ad59-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="2ad59-211">Кипр</span><span class="sxs-lookup"><span data-stu-id="2ad59-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-212">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-212">Format</span></span>

<span data-ttu-id="2ad59-213">Восемь цифр и одна буква в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="2ad59-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-214">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-214">Pattern</span></span>

<span data-ttu-id="2ad59-215">Восемь цифр и одна буква:</span><span class="sxs-lookup"><span data-stu-id="2ad59-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="2ad59-216">"0"</span><span class="sxs-lookup"><span data-stu-id="2ad59-216">A "0"</span></span> 
    
- <span data-ttu-id="2ad59-217">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="2ad59-217">Seven digits</span></span>
    
- <span data-ttu-id="2ad59-218">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-219">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-219">Checksum</span></span>

<span data-ttu-id="2ad59-220">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-221">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-221">Definition</span></span>

<span data-ttu-id="2ad59-222">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-223">Функция `Func_cyprus_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-224">Найдено ключевое `Keywords_cyprus_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-225">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-226">Функция `Func_cyprus_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="2ad59-228">Кэйвордс_ципрус_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-229">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-229">tax number</span></span>
  
<span data-ttu-id="2ad59-230">см</span><span class="sxs-lookup"><span data-stu-id="2ad59-230">tax</span></span>
  
<span data-ttu-id="2ad59-231">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-231">tax id</span></span>
  
<span data-ttu-id="2ad59-232">Налоговый код идентификации</span><span class="sxs-lookup"><span data-stu-id="2ad59-232">tax identification code</span></span>
  
<span data-ttu-id="2ad59-233">Тик</span><span class="sxs-lookup"><span data-stu-id="2ad59-233">tic</span></span>
  
<span data-ttu-id="2ad59-234">Тик #</span><span class="sxs-lookup"><span data-stu-id="2ad59-234">tic#</span></span>
  
<span data-ttu-id="2ad59-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="2ad59-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="2ad59-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="2ad59-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="2ad59-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="2ad59-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="2ad59-238">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="2ad59-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-239">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-239">Format</span></span>

<span data-ttu-id="2ad59-240">Девять или десять цифр с необязательной обратной косой чертой</span><span class="sxs-lookup"><span data-stu-id="2ad59-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-241">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-241">Pattern</span></span>

<span data-ttu-id="2ad59-242">Девять или десять цифр с необязательной обратной косой чертой.</span><span class="sxs-lookup"><span data-stu-id="2ad59-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="2ad59-243">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="2ad59-243">Six digits</span></span> 
    
- <span data-ttu-id="2ad59-244">Обратная косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="2ad59-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="2ad59-245">Три или четыре цифры</span><span class="sxs-lookup"><span data-stu-id="2ad59-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-246">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-246">Checksum</span></span>

<span data-ttu-id="2ad59-247">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-248">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-248">Definition</span></span>

<span data-ttu-id="2ad59-249">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-250">Регулярное выражение `Regex_czech_republic_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-251">Найдено ключевое `Keywords_czech_republic_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-252">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="2ad59-253">Кэйвордс_кзеч_републик_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-254">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-254">tax number</span></span>
  
<span data-ttu-id="2ad59-255">см</span><span class="sxs-lookup"><span data-stu-id="2ad59-255">tax</span></span>
  
<span data-ttu-id="2ad59-256">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-256">tax id</span></span>
  
<span data-ttu-id="2ad59-257">персональный номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-257">personal number</span></span>
  
<span data-ttu-id="2ad59-258">даňовé číсло</span><span class="sxs-lookup"><span data-stu-id="2ad59-258">daňové číslo</span></span>
  
<span data-ttu-id="2ad59-259">особнí číсло</span><span class="sxs-lookup"><span data-stu-id="2ad59-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="2ad59-260">Дания</span><span class="sxs-lookup"><span data-stu-id="2ad59-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-261">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-261">Format</span></span>

<span data-ttu-id="2ad59-262">Десять цифр, содержащие дефис</span><span class="sxs-lookup"><span data-stu-id="2ad59-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-263">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-263">Pattern</span></span>

<span data-ttu-id="2ad59-264">Десять цифр с дефисом:</span><span class="sxs-lookup"><span data-stu-id="2ad59-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="2ad59-265">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="2ad59-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="2ad59-266">дефис;</span><span class="sxs-lookup"><span data-stu-id="2ad59-266">A hyphen</span></span>
    
- <span data-ttu-id="2ad59-267">Четыре цифры, которые соответствуют порядковому номеру, где первая цифра соответствует столетию рождения, а последняя цифра соответствует полу лица (нечетный для пола и даже для женщина)</span><span class="sxs-lookup"><span data-stu-id="2ad59-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-268">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-268">Checksum</span></span>

<span data-ttu-id="2ad59-269">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-270">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-270">Definition</span></span>

<span data-ttu-id="2ad59-271">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-272">Функция `Func_denmark_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-273">Найдено ключевое `Keywords_denmark_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-275">Функция `Func_denmark_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-276">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="2ad59-277">Кэйвордс_денмарк_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-278">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-278">tax number</span></span>
  
<span data-ttu-id="2ad59-279">см</span><span class="sxs-lookup"><span data-stu-id="2ad59-279">tax</span></span>
  
<span data-ttu-id="2ad59-280">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-280">tax id</span></span>
  
<span data-ttu-id="2ad59-281">CPR Number</span><span class="sxs-lookup"><span data-stu-id="2ad59-281">cpr number</span></span>
  
<span data-ttu-id="2ad59-282">CPR</span><span class="sxs-lookup"><span data-stu-id="2ad59-282">cpr#</span></span>
  
<span data-ttu-id="2ad59-283">Скат нуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-283">skat nummer</span></span>
  
<span data-ttu-id="2ad59-284">Идентификатор Скат</span><span class="sxs-lookup"><span data-stu-id="2ad59-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="2ad59-285">Эстония</span><span class="sxs-lookup"><span data-stu-id="2ad59-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-286">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-286">Format</span></span>

<span data-ttu-id="2ad59-287">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-288">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-288">Pattern</span></span>

<span data-ttu-id="2ad59-289">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="2ad59-289">11 digits:</span></span>
  
-  <span data-ttu-id="2ad59-290">Одна цифра, соответствующая пол и столетию рождения, где нечетное число означает "штекер", а четное число указывает на женщина следующим образом: 1, 2 для 19 века; 3, 4 — 20 века; и 5, 6 для 21 века</span><span class="sxs-lookup"><span data-stu-id="2ad59-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="2ad59-291">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="2ad59-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="2ad59-292">Три цифры, которые соответствуют порядковому номеру, разделенному на одну и ту же дату.</span><span class="sxs-lookup"><span data-stu-id="2ad59-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="2ad59-293">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="2ad59-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-294">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-294">Checksum</span></span>

<span data-ttu-id="2ad59-295">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-296">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-296">Definition</span></span>

<span data-ttu-id="2ad59-297">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-298">Функция `Func_estonia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-299">Найдено ключевое `Keywords_estonia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-300">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-301">Функция `Func_estonia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-302">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="2ad59-303">Кэйвордс_естониа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-304">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-304">tax number</span></span>
  
<span data-ttu-id="2ad59-305">см</span><span class="sxs-lookup"><span data-stu-id="2ad59-305">tax</span></span>
  
<span data-ttu-id="2ad59-306">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-306">tax id</span></span>
  
<span data-ttu-id="2ad59-307">персональный код</span><span class="sxs-lookup"><span data-stu-id="2ad59-307">personal code</span></span>
  
<span data-ttu-id="2ad59-308">максунумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-308">maksunumber</span></span>
  
<span data-ttu-id="2ad59-309">Идентификатор Максу</span><span class="sxs-lookup"><span data-stu-id="2ad59-309">maksu id</span></span>
  
<span data-ttu-id="2ad59-310">исикукуд</span><span class="sxs-lookup"><span data-stu-id="2ad59-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="2ad59-311">Финляндия</span><span class="sxs-lookup"><span data-stu-id="2ad59-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-312">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-312">Format</span></span>

<span data-ttu-id="2ad59-313">Сочетание цифр, букв и плюса, а также знак минуса</span><span class="sxs-lookup"><span data-stu-id="2ad59-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-314">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-314">Pattern</span></span>

<span data-ttu-id="2ad59-315">Сочетание цифр, букв и плюса и знака "плюс" и "минус" (11 символов).</span><span class="sxs-lookup"><span data-stu-id="2ad59-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="2ad59-316">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="2ad59-316">Six digits</span></span>
    
- <span data-ttu-id="2ad59-317">Один из следующих элементов: знак плюса, знак минуса или буква "A" (без учета регистра), где знак "плюс" (без учета регистра) означает, что знак "плюс" находится в диапазоне от 1 до 1800-1899, а "A" означает, что порожденный 2000 и после</span><span class="sxs-lookup"><span data-stu-id="2ad59-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="2ad59-318">Три цифры</span><span class="sxs-lookup"><span data-stu-id="2ad59-318">Three digits</span></span>
    
- <span data-ttu-id="2ad59-319">Одна буква или один номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-320">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-320">Checksum</span></span>

<span data-ttu-id="2ad59-321">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-322">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-322">Definition</span></span>

<span data-ttu-id="2ad59-323">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-324">Функция `Func_finland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-325">Найдено ключевое `Keywords_finland_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-326">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-327">Функция `Func_finland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-328">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="2ad59-329">Кэйвордс_финланд_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-330">identification number</span><span class="sxs-lookup"><span data-stu-id="2ad59-330">identification number</span></span>
  
<span data-ttu-id="2ad59-331">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-331">personal id</span></span>
  
<span data-ttu-id="2ad59-332">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-332">identity number</span></span>
  
<span data-ttu-id="2ad59-333">Финский национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-333">finnish national id number</span></span>
  
<span data-ttu-id="2ad59-334">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-334">personalidnumber#</span></span>
  
<span data-ttu-id="2ad59-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="2ad59-335">national identification number</span></span>
  
<span data-ttu-id="2ad59-336">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-336">id number</span></span>
  
<span data-ttu-id="2ad59-337">код страны</span><span class="sxs-lookup"><span data-stu-id="2ad59-337">national id no.</span></span>
  
<span data-ttu-id="2ad59-338">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-338">national id number</span></span>
  
<span data-ttu-id="2ad59-339">ID No</span><span class="sxs-lookup"><span data-stu-id="2ad59-339">id no</span></span>
  
<span data-ttu-id="2ad59-340">туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="2ad59-340">tunnistenumero</span></span>
  
<span data-ttu-id="2ad59-341">хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="2ad59-341">henkilötunnus</span></span>
  
<span data-ttu-id="2ad59-342">иксилöллинен хенкилöкохтаинен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="2ad59-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="2ad59-343">аинутлаатуинен хенкилöкохтаинен туннус</span><span class="sxs-lookup"><span data-stu-id="2ad59-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="2ad59-344">идентититти нумеро</span><span class="sxs-lookup"><span data-stu-id="2ad59-344">identiteetti numero</span></span>
  
<span data-ttu-id="2ad59-345">Суомен кансаллинен хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="2ad59-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="2ad59-346">хенкилöтуннуснумеро #</span><span class="sxs-lookup"><span data-stu-id="2ad59-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="2ad59-347">кансаллисен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="2ad59-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="2ad59-348">туннуснумеро</span><span class="sxs-lookup"><span data-stu-id="2ad59-348">tunnusnumero</span></span>
  
<span data-ttu-id="2ad59-349">кансаллинен туннус нумеро</span><span class="sxs-lookup"><span data-stu-id="2ad59-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="2ad59-350">Франция</span><span class="sxs-lookup"><span data-stu-id="2ad59-350">France</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-351">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-351">Format</span></span>

<span data-ttu-id="2ad59-352">13 цифр для отдельных пользователей и девять цифр для сущностей</span><span class="sxs-lookup"><span data-stu-id="2ad59-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-353">Pattern</span></span>

<span data-ttu-id="2ad59-354">13 цифр для отдельных пользователей:</span><span class="sxs-lookup"><span data-stu-id="2ad59-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="2ad59-355">Одна цифра, которая должна быть равна 0, 1, 2 или 3</span><span class="sxs-lookup"><span data-stu-id="2ad59-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="2ad59-356">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-356">12 digits</span></span>
    
<span data-ttu-id="2ad59-357">Девять цифр для сущностей</span><span class="sxs-lookup"><span data-stu-id="2ad59-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-358">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-358">Checksum</span></span>

<span data-ttu-id="2ad59-359">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-360">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-360">Definition</span></span>

<span data-ttu-id="2ad59-361">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-362">Функция `Func_france_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-363">Найдено ключевое `Keywords_france_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-365">Функция `Func_france_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-366">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="2ad59-367">Кэйвордс_франце_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-368">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-368">tax identification number</span></span>
  
<span data-ttu-id="2ad59-369">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-369">tax number</span></span>
  
<span data-ttu-id="2ad59-370">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-370">tax id</span></span>
  
<span data-ttu-id="2ad59-371">нумéро д'идентификатион Фин.</span><span class="sxs-lookup"><span data-stu-id="2ad59-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="2ad59-372">Германия</span><span class="sxs-lookup"><span data-stu-id="2ad59-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-373">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-373">Format</span></span>

<span data-ttu-id="2ad59-374">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-375">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-375">Pattern</span></span>

<span data-ttu-id="2ad59-376">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="2ad59-376">11 digits :</span></span>
  
-  <span data-ttu-id="2ad59-377">Десять цифр</span><span class="sxs-lookup"><span data-stu-id="2ad59-377">Ten digits</span></span> 
    
- <span data-ttu-id="2ad59-378">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="2ad59-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-379">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-379">Checksum</span></span>

<span data-ttu-id="2ad59-380">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-381">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-381">Definition</span></span>

<span data-ttu-id="2ad59-382">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-383">Функция `Func_germany_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-384">Найдено ключевое `Keywords_germany_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-385">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-386">Функция `Func_germany_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-387">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="2ad59-388">Кэйвордс_жермани_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-389">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-389">tax number</span></span>
  
<span data-ttu-id="2ad59-390">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-390">tax no.</span></span>
  
<span data-ttu-id="2ad59-391">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-391">taxno#</span></span>
  
<span data-ttu-id="2ad59-392">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-392">taxnumber#</span></span>
  
<span data-ttu-id="2ad59-393">такснумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-393">taxnumber</span></span>
  
<span data-ttu-id="2ad59-394">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-394">tax id</span></span>
  
<span data-ttu-id="2ad59-395">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-395">taxid#</span></span>
  
<span data-ttu-id="2ad59-396">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-396">tax identification number</span></span>
  
<span data-ttu-id="2ad59-397">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-397">tax identification no.</span></span>
  
<span data-ttu-id="2ad59-398">стеуернуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-398">steuernummer</span></span>
  
<span data-ttu-id="2ad59-399">Идентификатор стеуер</span><span class="sxs-lookup"><span data-stu-id="2ad59-399">steuer id</span></span>
  
<span data-ttu-id="2ad59-400">стеуеридентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="2ad59-401">Греция</span><span class="sxs-lookup"><span data-stu-id="2ad59-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-402">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-402">Format</span></span>

<span data-ttu-id="2ad59-403">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-404">Pattern</span></span>

<span data-ttu-id="2ad59-405">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-406">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-406">Checksum</span></span>

<span data-ttu-id="2ad59-407">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-408">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-408">Definition</span></span>

<span data-ttu-id="2ad59-409">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-410">Регулярное выражение `Regex_greece_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-411">Найдено ключевое `Keywords_greece_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-412">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="2ad59-413">Кэйвордс_грице_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-414">АФМ</span><span class="sxs-lookup"><span data-stu-id="2ad59-414">afm</span></span>
  
<span data-ttu-id="2ad59-415">ИНН</span><span class="sxs-lookup"><span data-stu-id="2ad59-415">tin</span></span>
  
<span data-ttu-id="2ad59-416">Налоговый код но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-416">tax id no.</span></span>
  
<span data-ttu-id="2ad59-417">Налоговый код No</span><span class="sxs-lookup"><span data-stu-id="2ad59-417">tax id no</span></span>
  
<span data-ttu-id="2ad59-418">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-418">tax identification number</span></span>
  
<span data-ttu-id="2ad59-419">Налоговый номер реестра</span><span class="sxs-lookup"><span data-stu-id="2ad59-419">tax registry number</span></span>
  
<span data-ttu-id="2ad59-420">реестр по номеру налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-420">tax registry no.</span></span>
  
<span data-ttu-id="2ad59-421">АФМ #</span><span class="sxs-lookup"><span data-stu-id="2ad59-421">afm#</span></span>
  
<span data-ttu-id="2ad59-422">ИНН</span><span class="sxs-lookup"><span data-stu-id="2ad59-422">tin#</span></span>
  
<span data-ttu-id="2ad59-423">таксидно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-423">taxidno#</span></span>
  
<span data-ttu-id="2ad59-424">таксрегистрино #</span><span class="sxs-lookup"><span data-stu-id="2ad59-424">taxregistryno#</span></span>
  
<span data-ttu-id="2ad59-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="2ad59-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="2ad59-426">аφμ</span><span class="sxs-lookup"><span data-stu-id="2ad59-426">aφμ</span></span>
  
<span data-ttu-id="2ad59-427">аφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="2ad59-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="2ad59-428">φορολογικού μητρώου Νο.</span><span class="sxs-lookup"><span data-stu-id="2ad59-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="2ad59-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="2ad59-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="2ad59-430">Венгрия</span><span class="sxs-lookup"><span data-stu-id="2ad59-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-431">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-431">Format</span></span>

<span data-ttu-id="2ad59-432">Десять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-433">Pattern</span></span>

<span data-ttu-id="2ad59-434">Десять цифр:</span><span class="sxs-lookup"><span data-stu-id="2ad59-434">Ten digits:</span></span>
  
-  <span data-ttu-id="2ad59-435">Одна цифра, которая должна быть "8"</span><span class="sxs-lookup"><span data-stu-id="2ad59-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="2ad59-436">Пять цифр, которые соответствуют количеству дней между датой 01/01/1867 и датой рождения отдельного лица.</span><span class="sxs-lookup"><span data-stu-id="2ad59-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="2ad59-437">Три цифры, которые соответствуют номеру, созданному шансом выделить людей, которые поставили один и тот же день.</span><span class="sxs-lookup"><span data-stu-id="2ad59-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="2ad59-438">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="2ad59-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-439">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-439">Checksum</span></span>

<span data-ttu-id="2ad59-440">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-441">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-441">Definition</span></span>

<span data-ttu-id="2ad59-442">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-443">Функция `Func_hungary_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-444">Найдено ключевое `Keywords_hungary_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-445">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-446">Функция `Func_hungary_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-447">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="2ad59-448">Кэйвордс_хунгари_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-449">идентификационный номер для венгерского налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="2ad59-450">Венгерский Tin</span><span class="sxs-lookup"><span data-stu-id="2ad59-450">hungarian tin</span></span>
  
<span data-ttu-id="2ad59-451">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="2ad59-451">tax id number</span></span>
  
<span data-ttu-id="2ad59-452">номер НДС</span><span class="sxs-lookup"><span data-stu-id="2ad59-452">vat number</span></span>
  
<span data-ttu-id="2ad59-453">Налоговый орган без</span><span class="sxs-lookup"><span data-stu-id="2ad59-453">tax authority no</span></span>
  
<span data-ttu-id="2ad59-454">идентификационный номер налогоплательщика для налогового кода</span><span class="sxs-lookup"><span data-stu-id="2ad59-454">tax id tax identity number</span></span>
  
<span data-ttu-id="2ad59-455">таксиднумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-455">taxidnumber#</span></span>
  
<span data-ttu-id="2ad59-456">ИНН</span><span class="sxs-lookup"><span data-stu-id="2ad59-456">tin#</span></span>
  
<span data-ttu-id="2ad59-457">хунгатиантин #</span><span class="sxs-lookup"><span data-stu-id="2ad59-457">hungatiantin#</span></span>
  
<span data-ttu-id="2ad59-458">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-458">tax identification no</span></span>
  
<span data-ttu-id="2ad59-459">таксидно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-459">taxidno#</span></span>
  
<span data-ttu-id="2ad59-460">адóазоносíтó сзáм</span><span class="sxs-lookup"><span data-stu-id="2ad59-460">adóazonosító szám</span></span>
  
<span data-ttu-id="2ad59-461">адóсзáм</span><span class="sxs-lookup"><span data-stu-id="2ad59-461">adószám</span></span>
  
<span data-ttu-id="2ad59-462">адóхатóсáг сзáм</span><span class="sxs-lookup"><span data-stu-id="2ad59-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="2ad59-463">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="2ad59-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-464">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-464">Format</span></span>

<span data-ttu-id="2ad59-465">Семь цифр, за которыми следует буква без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-466">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-466">Pattern</span></span>

<span data-ttu-id="2ad59-467">Семь цифр, за которыми следует буква:</span><span class="sxs-lookup"><span data-stu-id="2ad59-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="2ad59-468">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="2ad59-468">Seven digits</span></span> 
    
- <span data-ttu-id="2ad59-469">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-470">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-470">Checksum</span></span>

<span data-ttu-id="2ad59-471">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-472">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-472">Definition</span></span>

<span data-ttu-id="2ad59-473">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-474">Функция `Func_ireland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-475">Найдено ключевое `Keywords_ireland_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-476">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-477">Функция `Func_ireland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-478">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="2ad59-479">Кэйвордс_иреланд_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-480">общедоступная служба</span><span class="sxs-lookup"><span data-stu-id="2ad59-480">public service no</span></span>
  
<span data-ttu-id="2ad59-481">Личная общедоступная служба</span><span class="sxs-lookup"><span data-stu-id="2ad59-481">personal public service no</span></span>
  
<span data-ttu-id="2ad59-482">PPS нет</span><span class="sxs-lookup"><span data-stu-id="2ad59-482">pps no</span></span>
  
<span data-ttu-id="2ad59-483">Личная служба</span><span class="sxs-lookup"><span data-stu-id="2ad59-483">personal service no</span></span>
  
<span data-ttu-id="2ad59-484">Служба PPS нет</span><span class="sxs-lookup"><span data-stu-id="2ad59-484">pps service no</span></span>
  
<span data-ttu-id="2ad59-485">ппсно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-485">ppsno#</span></span>
  
<span data-ttu-id="2ad59-486">Ирландский PPS No</span><span class="sxs-lookup"><span data-stu-id="2ad59-486">irish pps no</span></span>
  
<span data-ttu-id="2ad59-487">публиксервицено #</span><span class="sxs-lookup"><span data-stu-id="2ad59-487">publicserviceno#</span></span>
  
<span data-ttu-id="2ad59-488">номер личной общедоступной службы</span><span class="sxs-lookup"><span data-stu-id="2ad59-488">personal public service number</span></span>
  
<span data-ttu-id="2ad59-489">уимхир феарсанта сеирбхíсе поиблí</span><span class="sxs-lookup"><span data-stu-id="2ad59-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="2ad59-490">PPS уимх</span><span class="sxs-lookup"><span data-stu-id="2ad59-490">pps uimh</span></span>
  
<span data-ttu-id="2ad59-491">уимхир аисеантаис феарсанта</span><span class="sxs-lookup"><span data-stu-id="2ad59-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="2ad59-492">Италия</span><span class="sxs-lookup"><span data-stu-id="2ad59-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-493">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-493">Format</span></span>

<span data-ttu-id="2ad59-494">16 букв и цифр в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="2ad59-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-495">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-495">Pattern</span></span>

<span data-ttu-id="2ad59-496">16 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="2ad59-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="2ad59-497">Три буквы, соответствующие первым трем согласным в имени семейства</span><span class="sxs-lookup"><span data-stu-id="2ad59-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="2ad59-498">Три буквы, соответствующие первым, третьим и четвертым согласным в имени.</span><span class="sxs-lookup"><span data-stu-id="2ad59-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="2ad59-499">Две цифры, соответствующие последним цифрам года рождения</span><span class="sxs-lookup"><span data-stu-id="2ad59-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="2ad59-500">Одна цифра, соответствующая месяцу рождения, буквы используются в алфавитном порядке, но используются только буквы от A до E, H, L, M, P, R — T (то есть Январь — это R, а Октябрь — R)</span><span class="sxs-lookup"><span data-stu-id="2ad59-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="2ad59-501">Две цифры, которые соответствуют дню рождения, где 40 добавляется к дню рождения женщин, чтобы отличать от мужчин</span><span class="sxs-lookup"><span data-stu-id="2ad59-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="2ad59-502">Четыре цифры, соответствующие коду города, соответствующему органу государственной власти, в котором был создан пользователь, — коды уровня страны используются для иностранных стран</span><span class="sxs-lookup"><span data-stu-id="2ad59-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="2ad59-503">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="2ad59-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-504">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-504">Checksum</span></span>

<span data-ttu-id="2ad59-505">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-506">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-506">Definition</span></span>

<span data-ttu-id="2ad59-507">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-508">Функция `Func_italy_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-509">Найдено ключевое `Keywords_italy_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-510">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-511">Функция `Func_italy_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-512">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="2ad59-513">Кэйвордс_итали_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-514">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-514">tax number</span></span>
  
<span data-ttu-id="2ad59-515">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-515">tax no.</span></span>
  
<span data-ttu-id="2ad59-516">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-516">taxno#</span></span>
  
<span data-ttu-id="2ad59-517">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-517">taxnumber#</span></span>
  
<span data-ttu-id="2ad59-518">такснумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-518">taxnumber</span></span>
  
<span data-ttu-id="2ad59-519">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-519">tax id</span></span>
  
<span data-ttu-id="2ad59-520">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-520">taxid#</span></span>
  
<span data-ttu-id="2ad59-521">Финансовый код</span><span class="sxs-lookup"><span data-stu-id="2ad59-521">fiscal code</span></span>
  
<span data-ttu-id="2ad59-522">финансовый отчет по сокостям</span><span class="sxs-lookup"><span data-stu-id="2ad59-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="2ad59-523">Латвия</span><span class="sxs-lookup"><span data-stu-id="2ad59-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-524">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-524">Format</span></span>

<span data-ttu-id="2ad59-525">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-526">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-526">Pattern</span></span>

<span data-ttu-id="2ad59-527">11 цифр в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="2ad59-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="2ad59-528">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="2ad59-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="2ad59-529">Одна цифра, соответствующая столетию рождения, где "0" соответствует 19 века, "1" соответствует 20 столетию, а "2" соответствует 21 столетию</span><span class="sxs-lookup"><span data-stu-id="2ad59-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="2ad59-530">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="2ad59-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-531">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-531">Checksum</span></span>

<span data-ttu-id="2ad59-532">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-533">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-533">Definition</span></span>

<span data-ttu-id="2ad59-534">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-535">Функция `Func_latvia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-536">Найдено ключевое `Keywords_latvia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-537">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-538">Функция `Func_latvia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-539">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="2ad59-540">Кэйвордс_латвиа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-541">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-541">tax number</span></span>
  
<span data-ttu-id="2ad59-542">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-542">tax no.</span></span>
  
<span data-ttu-id="2ad59-543">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-543">taxno#</span></span>
  
<span data-ttu-id="2ad59-544">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-544">taxnumber#</span></span>
  
<span data-ttu-id="2ad59-545">такснумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-545">taxnumber</span></span>
  
<span data-ttu-id="2ad59-546">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-546">tax id</span></span>
  
<span data-ttu-id="2ad59-547">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-547">taxid#</span></span>
  
<span data-ttu-id="2ad59-548">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-548">tax identification number</span></span>
  
<span data-ttu-id="2ad59-549">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-549">tax identification no.</span></span>
  
<span data-ttu-id="2ad59-550">нодокļа нумурс</span><span class="sxs-lookup"><span data-stu-id="2ad59-550">nodokļa numurs</span></span>
  
<span data-ttu-id="2ad59-551">нодокļу идентификāЦижас нумурс</span><span class="sxs-lookup"><span data-stu-id="2ad59-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="2ad59-552">нодокļу идентификāЦижа нумурс</span><span class="sxs-lookup"><span data-stu-id="2ad59-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="2ad59-553">Литва</span><span class="sxs-lookup"><span data-stu-id="2ad59-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-554">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-554">Format</span></span>

<span data-ttu-id="2ad59-555">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-556">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-556">Pattern</span></span>

<span data-ttu-id="2ad59-557">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-558">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-558">Checksum</span></span>

<span data-ttu-id="2ad59-559">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-560">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-560">Definition</span></span>

<span data-ttu-id="2ad59-561">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-562">Функция `Func_lithuania_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-563">Найдено ключевое `Keywords_lithuania_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-564">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-565">Функция `Func_lithuania_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-566">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="2ad59-567">Кэйвордс_лисуаниа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-568">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-568">tax number</span></span>
  
<span data-ttu-id="2ad59-569">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-569">tax no.</span></span>
  
<span data-ttu-id="2ad59-570">налог No #</span><span class="sxs-lookup"><span data-stu-id="2ad59-570">tax no#</span></span>
  
<span data-ttu-id="2ad59-571">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-571">taxnumber#</span></span>
  
<span data-ttu-id="2ad59-572">такснумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-572">taxnumber</span></span>
  
<span data-ttu-id="2ad59-573">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-573">tax id</span></span>
  
<span data-ttu-id="2ad59-574">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-574">taxid#</span></span>
  
<span data-ttu-id="2ad59-575">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-575">tax identification number</span></span>
  
<span data-ttu-id="2ad59-576">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-576">tax identification no.</span></span>
  
<span data-ttu-id="2ad59-577">Идентификатор мокесčиų</span><span class="sxs-lookup"><span data-stu-id="2ad59-577">mokesčių id</span></span>
  
<span data-ttu-id="2ad59-578">мокесčиų нумерис</span><span class="sxs-lookup"><span data-stu-id="2ad59-578">mokesčių numeris</span></span>
  
<span data-ttu-id="2ad59-579">мокесčиų идентификавимас нумерис</span><span class="sxs-lookup"><span data-stu-id="2ad59-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="2ad59-580">Луксембург</span><span class="sxs-lookup"><span data-stu-id="2ad59-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-581">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-581">Format</span></span>

<span data-ttu-id="2ad59-582">13 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-583">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-583">Pattern</span></span>

<span data-ttu-id="2ad59-584">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="2ad59-584">13 digits:</span></span>
  
-  <span data-ttu-id="2ad59-585">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-585">11 digits</span></span> 
    
- <span data-ttu-id="2ad59-586">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="2ad59-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-587">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-587">Checksum</span></span>

<span data-ttu-id="2ad59-588">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-589">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-589">Definition</span></span>

<span data-ttu-id="2ad59-590">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-591">Функция `Func_luxemburg_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-592">Найдено ключевое `Keywords_luxemburg_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-593">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-594">Функция `Func_luxemburg_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-595">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="2ad59-596">Кэйвордс_луксембург_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-597">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-597">tax number</span></span>
  
<span data-ttu-id="2ad59-598">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-598">tax no.</span></span>
  
<span data-ttu-id="2ad59-599">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-599">taxno#</span></span>
  
<span data-ttu-id="2ad59-600">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-600">taxnumber#</span></span>
  
<span data-ttu-id="2ad59-601">такснумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-601">taxnumber</span></span>
  
<span data-ttu-id="2ad59-602">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-602">tax id</span></span>
  
<span data-ttu-id="2ad59-603">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-603">taxid#</span></span>
  
<span data-ttu-id="2ad59-604">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-604">tax identification number</span></span>
  
<span data-ttu-id="2ad59-605">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-605">tax identification no.</span></span>
  
<span data-ttu-id="2ad59-606">стеуернуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-606">steuernummer</span></span>
  
<span data-ttu-id="2ad59-607">Идентификатор стеуер</span><span class="sxs-lookup"><span data-stu-id="2ad59-607">steuer id</span></span>
  
<span data-ttu-id="2ad59-608">стеуеридентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="2ad59-609">Мальта</span><span class="sxs-lookup"><span data-stu-id="2ad59-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-610">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-610">Format</span></span>

<span data-ttu-id="2ad59-611">Для национальных заМальтийский: 7 цифр и одна буква в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="2ad59-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="2ad59-612">Мальтийскийные страны и Мальтийский, не являющиеся субъектами: 9 цифр</span><span class="sxs-lookup"><span data-stu-id="2ad59-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-613">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-613">Pattern</span></span>

<span data-ttu-id="2ad59-614">Мальтийский национальные условия: 7 цифр и одна буква</span><span class="sxs-lookup"><span data-stu-id="2ad59-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="2ad59-615">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="2ad59-615">Seven digits</span></span> 
    
- <span data-ttu-id="2ad59-616">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="2ad59-617">Мальтийскийные страны и Мальтийский, не являющиеся субъектами: 9 цифр</span><span class="sxs-lookup"><span data-stu-id="2ad59-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="2ad59-618">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="2ad59-619">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-619">Checksum</span></span>

<span data-ttu-id="2ad59-620">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-621">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-621">Definition</span></span>

<span data-ttu-id="2ad59-622">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-623">Функция `Func_malta_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-624">Найдено ключевое `Keywords_malta_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-625">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-626">Функция `Func_malta_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-627">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="2ad59-628">Кэйвордс_малта_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-629">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-629">tax number</span></span>
  
<span data-ttu-id="2ad59-630">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-630">tax no.</span></span>
  
<span data-ttu-id="2ad59-631">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-631">taxno#</span></span>
  
<span data-ttu-id="2ad59-632">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-632">taxnumber#</span></span>
  
<span data-ttu-id="2ad59-633">такснумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-633">taxnumber</span></span>
  
<span data-ttu-id="2ad59-634">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-634">tax id</span></span>
  
<span data-ttu-id="2ad59-635">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-635">taxid#</span></span>
  
<span data-ttu-id="2ad59-636">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-636">tax identification number</span></span>
  
<span data-ttu-id="2ad59-637">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-637">tax identification no.</span></span>
  
<span data-ttu-id="2ad59-638">нумру ТАТ — такскса</span><span class="sxs-lookup"><span data-stu-id="2ad59-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="2ad59-639">ID ТАТ — такскса</span><span class="sxs-lookup"><span data-stu-id="2ad59-639">id tat-taxxa</span></span>
  
<span data-ttu-id="2ad59-640">нумру Ta ' идентификаззжони ТАТ такскса</span><span class="sxs-lookup"><span data-stu-id="2ad59-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="2ad59-641">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="2ad59-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-642">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-642">Format</span></span>

<span data-ttu-id="2ad59-643">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-644">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-644">Pattern</span></span>

<span data-ttu-id="2ad59-645">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="2ad59-646">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-646">Checksum</span></span>

<span data-ttu-id="2ad59-647">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-648">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-648">Definition</span></span>

<span data-ttu-id="2ad59-649">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-650">Функция `Func_netherlands_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-651">Найдено ключевое `Keywords_netherlands_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-652">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-653">Функция `Func_netherlands_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-654">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="2ad59-655">Кэйвордс_несерландс_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-656">идентификационный номер налога Нидерландов</span><span class="sxs-lookup"><span data-stu-id="2ad59-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="2ad59-657">Идентификация налога Нидерландов</span><span class="sxs-lookup"><span data-stu-id="2ad59-657">netherlands tax identification</span></span>
  
<span data-ttu-id="2ad59-658">идентификационный номер налога несерланд</span><span class="sxs-lookup"><span data-stu-id="2ad59-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="2ad59-659">Налоговый код несерланд</span><span class="sxs-lookup"><span data-stu-id="2ad59-659">netherland's tax identification</span></span>
  
<span data-ttu-id="2ad59-660">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-660">tax identification number</span></span>
  
<span data-ttu-id="2ad59-661">Налоговый идентификатор голландского налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-661">dutch tax id</span></span>
  
<span data-ttu-id="2ad59-662">идентификационный номер налога на нидерландском языке</span><span class="sxs-lookup"><span data-stu-id="2ad59-662">dutch tax identification number</span></span>
  
<span data-ttu-id="2ad59-663">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-663">tax id</span></span>
  
<span data-ttu-id="2ad59-664">Налоговый идентификатор #</span><span class="sxs-lookup"><span data-stu-id="2ad59-664">tax id#</span></span>
  
<span data-ttu-id="2ad59-665">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-665">tax number</span></span>
  
<span data-ttu-id="2ad59-666">налог No #</span><span class="sxs-lookup"><span data-stu-id="2ad59-666">tax no#</span></span>
  
<span data-ttu-id="2ad59-667">см</span><span class="sxs-lookup"><span data-stu-id="2ad59-667">tax#</span></span>
  
<span data-ttu-id="2ad59-668">ИНН</span><span class="sxs-lookup"><span data-stu-id="2ad59-668">tin</span></span>
  
<span data-ttu-id="2ad59-669">ИНН</span><span class="sxs-lookup"><span data-stu-id="2ad59-669">tin#</span></span>
  
<span data-ttu-id="2ad59-670">Tin Нидерландов</span><span class="sxs-lookup"><span data-stu-id="2ad59-670">netherlands tin</span></span>
  
<span data-ttu-id="2ad59-671">Tin несерланд</span><span class="sxs-lookup"><span data-stu-id="2ad59-671">netherland's tin</span></span>
  
<span data-ttu-id="2ad59-672">Недерландс идентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="2ad59-673">идентификатиенуммер Van</span><span class="sxs-lookup"><span data-stu-id="2ad59-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="2ad59-674">идентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="2ad59-675">Недерландс идентификатие</span><span class="sxs-lookup"><span data-stu-id="2ad59-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="2ad59-676">Недерландс — идентификатор нуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="2ad59-677">Недерландс беластингнуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="2ad59-678">БТВ нуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-678">btw nummer</span></span>
  
<span data-ttu-id="2ad59-679">Недерландсе идентификатие</span><span class="sxs-lookup"><span data-stu-id="2ad59-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="2ad59-680">Польша</span><span class="sxs-lookup"><span data-stu-id="2ad59-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-681">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-681">Format</span></span>

<span data-ttu-id="2ad59-682">Одиннадцать цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-683">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-683">Pattern</span></span>

<span data-ttu-id="2ad59-684">Одиннадцать цифр</span><span class="sxs-lookup"><span data-stu-id="2ad59-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-685">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-685">Checksum</span></span>

<span data-ttu-id="2ad59-686">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-687">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-687">Definition</span></span>

<span data-ttu-id="2ad59-688">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-689">Функция `Func_poland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-690">Найдено ключевое `Keywords_poland_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-691">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-692">Функция `Func_poland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-693">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="2ad59-694">Кэйвордс_поланд_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-695">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-695">tax number</span></span>
  
<span data-ttu-id="2ad59-696">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-696">tax no.</span></span>
  
<span data-ttu-id="2ad59-697">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-697">taxno#</span></span>
  
<span data-ttu-id="2ad59-698">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-698">taxnumber#</span></span>
  
<span data-ttu-id="2ad59-699">такснумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-699">taxnumber</span></span>
  
<span data-ttu-id="2ad59-700">НИП</span><span class="sxs-lookup"><span data-stu-id="2ad59-700">nip</span></span>
  
<span data-ttu-id="2ad59-701">НИП #</span><span class="sxs-lookup"><span data-stu-id="2ad59-701">nip#</span></span>
  
<span data-ttu-id="2ad59-702">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-702">tax id</span></span>
  
<span data-ttu-id="2ad59-703">Налоговый идентификатор #</span><span class="sxs-lookup"><span data-stu-id="2ad59-703">tax id#</span></span>
  
<span data-ttu-id="2ad59-704">Идентификатор НИП</span><span class="sxs-lookup"><span data-stu-id="2ad59-704">nip id</span></span>
  
<span data-ttu-id="2ad59-705">Идентификатор НИП</span><span class="sxs-lookup"><span data-stu-id="2ad59-705">nip id#</span></span>
  
<span data-ttu-id="2ad59-706">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="2ad59-706">tax identification number</span></span>
  
<span data-ttu-id="2ad59-707">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="2ad59-707">tax identification no.</span></span>
  
<span data-ttu-id="2ad59-708">номер НДС</span><span class="sxs-lookup"><span data-stu-id="2ad59-708">vat number</span></span>
  
<span data-ttu-id="2ad59-709">НДС номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-709">vat no.</span></span>
  
<span data-ttu-id="2ad59-710">ватно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-710">vatno#</span></span>
  
<span data-ttu-id="2ad59-711">Код НДС</span><span class="sxs-lookup"><span data-stu-id="2ad59-711">vat id</span></span>
  
<span data-ttu-id="2ad59-712">Идентификатор НДС</span><span class="sxs-lookup"><span data-stu-id="2ad59-712">vat id#</span></span>
  
<span data-ttu-id="2ad59-713">Нумер идентификакжи податковеж</span><span class="sxs-lookup"><span data-stu-id="2ad59-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="2ad59-714">полски нумер идентификакжи податковеж</span><span class="sxs-lookup"><span data-stu-id="2ad59-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="2ad59-715">нумеридентификакжиподатковеж #</span><span class="sxs-lookup"><span data-stu-id="2ad59-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="2ad59-716">Португалия</span><span class="sxs-lookup"><span data-stu-id="2ad59-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-717">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-717">Format</span></span>

<span data-ttu-id="2ad59-718">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-719">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-719">Pattern</span></span>

<span data-ttu-id="2ad59-720">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-721">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-721">Checksum</span></span>

<span data-ttu-id="2ad59-722">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-723">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-723">Definition</span></span>

<span data-ttu-id="2ad59-724">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-725">Функция `Func_portugal_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-726">Найдено ключевое `Keywords_portugal_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-727">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-728">Функция `Func_portugal_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-729">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="2ad59-730">Кэйвордс_португал_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-731">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-731">tax number</span></span>
  
<span data-ttu-id="2ad59-732">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-732">tax no.</span></span>
  
<span data-ttu-id="2ad59-733">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-733">taxno#</span></span>
  
<span data-ttu-id="2ad59-734">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="2ad59-734">taxnumber#</span></span>
  
<span data-ttu-id="2ad59-735">такснумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-735">taxnumber</span></span>
  
<span data-ttu-id="2ad59-736">включена</span><span class="sxs-lookup"><span data-stu-id="2ad59-736">nif</span></span>
  
<span data-ttu-id="2ad59-737">включена</span><span class="sxs-lookup"><span data-stu-id="2ad59-737">nif#</span></span>
  
<span data-ttu-id="2ad59-738">финансовый нумеро</span><span class="sxs-lookup"><span data-stu-id="2ad59-738">numero fiscal</span></span>
  
<span data-ttu-id="2ad59-739">нúмеро de идентификаçãо Фин.</span><span class="sxs-lookup"><span data-stu-id="2ad59-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="2ad59-740">Румыния</span><span class="sxs-lookup"><span data-stu-id="2ad59-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-741">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-741">Format</span></span>

<span data-ttu-id="2ad59-742">13 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-743">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-743">Pattern</span></span>

<span data-ttu-id="2ad59-744">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-745">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-745">Checksum</span></span>

<span data-ttu-id="2ad59-746">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-747">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-747">Definition</span></span>

<span data-ttu-id="2ad59-748">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-749">Регулярное выражение `Regex_romania_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-750">Найдено ключевое `Keywords_romania_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-751">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="2ad59-752">Кэйвордс_романиа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-753">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-753">tax id</span></span>
  
<span data-ttu-id="2ad59-754">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="2ad59-754">tax id number</span></span>
  
<span data-ttu-id="2ad59-755">Налоговый файл нет</span><span class="sxs-lookup"><span data-stu-id="2ad59-755">tax file no</span></span>
  
<span data-ttu-id="2ad59-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="2ad59-756">tax file number</span></span>
  
<span data-ttu-id="2ad59-757">налог без</span><span class="sxs-lookup"><span data-stu-id="2ad59-757">tax no</span></span>
  
<span data-ttu-id="2ad59-758">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-758">tax number</span></span>
  
<span data-ttu-id="2ad59-759">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-759">taxid#</span></span>
  
<span data-ttu-id="2ad59-760">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-760">taxno#</span></span>
  
<span data-ttu-id="2ad59-761">ID — UL таксеи</span><span class="sxs-lookup"><span data-stu-id="2ad59-761">id-ul taxei</span></span>
  
<span data-ttu-id="2ad59-762">нумăрул де идентификаре фискалă</span><span class="sxs-lookup"><span data-stu-id="2ad59-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="2ad59-763">Словакия</span><span class="sxs-lookup"><span data-stu-id="2ad59-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-764">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-764">Format</span></span>

<span data-ttu-id="2ad59-765">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-766">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-766">Pattern</span></span>

<span data-ttu-id="2ad59-767">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-768">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-768">Checksum</span></span>

<span data-ttu-id="2ad59-769">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="2ad59-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-770">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-770">Definition</span></span>

<span data-ttu-id="2ad59-771">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-772">Регулярное выражение `Regex_slovakia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-773">Найдено ключевое `Keywords_slovakia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-774">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="2ad59-775">Кэйвордс_словакиа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-776">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-776">tax id</span></span>
  
<span data-ttu-id="2ad59-777">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="2ad59-777">tax id number</span></span>
  
<span data-ttu-id="2ad59-778">Идентификатор Tin</span><span class="sxs-lookup"><span data-stu-id="2ad59-778">tin id</span></span>
  
<span data-ttu-id="2ad59-779">номер Tin</span><span class="sxs-lookup"><span data-stu-id="2ad59-779">tin no</span></span>
  
<span data-ttu-id="2ad59-780">Идентификатор Tin словакиан</span><span class="sxs-lookup"><span data-stu-id="2ad59-780">slovakian tin id</span></span>
  
<span data-ttu-id="2ad59-781">ИНН</span><span class="sxs-lookup"><span data-stu-id="2ad59-781">tin</span></span>
  
<span data-ttu-id="2ad59-782">Налоговый файл нет</span><span class="sxs-lookup"><span data-stu-id="2ad59-782">tax file no</span></span>
  
<span data-ttu-id="2ad59-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="2ad59-783">tax file number</span></span>
  
<span data-ttu-id="2ad59-784">налог без</span><span class="sxs-lookup"><span data-stu-id="2ad59-784">tax no</span></span>
  
<span data-ttu-id="2ad59-785">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-785">tax number</span></span>
  
<span data-ttu-id="2ad59-786">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-786">taxid#</span></span>
  
<span data-ttu-id="2ad59-787">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-787">taxno#</span></span>
  
<span data-ttu-id="2ad59-788">даňовé идентификаčнé číсло</span><span class="sxs-lookup"><span data-stu-id="2ad59-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="2ad59-789">даňовé číсло</span><span class="sxs-lookup"><span data-stu-id="2ad59-789">daňové číslo</span></span>
  
<span data-ttu-id="2ad59-790">даňовé číсло сúбору</span><span class="sxs-lookup"><span data-stu-id="2ad59-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="2ad59-791">Словения</span><span class="sxs-lookup"><span data-stu-id="2ad59-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-792">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-792">Format</span></span>

<span data-ttu-id="2ad59-793">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-794">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-794">Pattern</span></span>

<span data-ttu-id="2ad59-795">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-796">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-796">Checksum</span></span>

<span data-ttu-id="2ad59-797">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-798">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-798">Definition</span></span>

<span data-ttu-id="2ad59-799">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-800">Функция `Func_slovenia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-801">Найдено ключевое `Keywords_slovenia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-802">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-803">Функция `Func_slovenia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-804">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="2ad59-805">Кэйвордс_словениа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-806">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-806">tax id</span></span>
  
<span data-ttu-id="2ad59-807">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="2ad59-807">tax id number</span></span>
  
<span data-ttu-id="2ad59-808">Идентификатор Tin</span><span class="sxs-lookup"><span data-stu-id="2ad59-808">tin id</span></span>
  
<span data-ttu-id="2ad59-809">номер Tin</span><span class="sxs-lookup"><span data-stu-id="2ad59-809">tin no</span></span>
  
<span data-ttu-id="2ad59-810">Словенский идентификатор Tin</span><span class="sxs-lookup"><span data-stu-id="2ad59-810">slovenian tin id</span></span>
  
<span data-ttu-id="2ad59-811">ИНН</span><span class="sxs-lookup"><span data-stu-id="2ad59-811">tin</span></span>
  
<span data-ttu-id="2ad59-812">Налоговый файл нет</span><span class="sxs-lookup"><span data-stu-id="2ad59-812">tax file no</span></span>
  
<span data-ttu-id="2ad59-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="2ad59-813">tax file number</span></span>
  
<span data-ttu-id="2ad59-814">налог без</span><span class="sxs-lookup"><span data-stu-id="2ad59-814">tax no</span></span>
  
<span data-ttu-id="2ad59-815">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-815">tax number</span></span>
  
<span data-ttu-id="2ad59-816">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-816">taxid#</span></span>
  
<span data-ttu-id="2ad59-817">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-817">taxno#</span></span>
  
<span data-ttu-id="2ad59-818">идентификаЦижска šтевилка Давка</span><span class="sxs-lookup"><span data-stu-id="2ad59-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="2ad59-819">давčна šтевилка</span><span class="sxs-lookup"><span data-stu-id="2ad59-819">davčna številka</span></span>
  
<span data-ttu-id="2ad59-820">šтевилка давčне датотеке</span><span class="sxs-lookup"><span data-stu-id="2ad59-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="2ad59-821">Испания</span><span class="sxs-lookup"><span data-stu-id="2ad59-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-822">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-822">Format</span></span>

<span data-ttu-id="2ad59-823">Семь или восемь цифр, а также одна или две буквы в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="2ad59-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-824">Pattern</span></span>

<span data-ttu-id="2ad59-825">Испанские пользователи с национальной идентификационной карточкой Испании Испания:</span><span class="sxs-lookup"><span data-stu-id="2ad59-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="2ad59-826">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="2ad59-826">Eight digits</span></span> 
    
- <span data-ttu-id="2ad59-827">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="2ad59-828">Нерезидентские Спаниардс без национальной идентификационной карточки Испании</span><span class="sxs-lookup"><span data-stu-id="2ad59-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="2ad59-829">Одна прописная буква L (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="2ad59-830">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="2ad59-830">Seven digits</span></span>
    
- <span data-ttu-id="2ad59-831">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="2ad59-832">Резидентный Спаниардс в течение 14 лет без международной идентификационной карточки для Испании:</span><span class="sxs-lookup"><span data-stu-id="2ad59-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="2ad59-833">Одна прописная буква K (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="2ad59-834">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="2ad59-834">Seven digits</span></span> 
    
- <span data-ttu-id="2ad59-835">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="2ad59-836">Фореигнерс с идентификационным номером внешнего получателя</span><span class="sxs-lookup"><span data-stu-id="2ad59-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="2ad59-837">Одна прописная буква "X", "Y" или "Z" (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="2ad59-838">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="2ad59-838">Seven digits</span></span>
    
- <span data-ttu-id="2ad59-839">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="2ad59-840">Фореигнерс без идентификационного номера внешнего получателя</span><span class="sxs-lookup"><span data-stu-id="2ad59-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="2ad59-841">Одна прописная буква "M" (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="2ad59-842">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="2ad59-842">Seven digits</span></span>
    
- <span data-ttu-id="2ad59-843">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="2ad59-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="2ad59-844">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-844">Checksum</span></span>

<span data-ttu-id="2ad59-845">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-846">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-846">Definition</span></span>

<span data-ttu-id="2ad59-847">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-848">Функция `Func_spain_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-849">Найдено ключевое `Keywords_spain_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-850">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-851">Функция `Func_spain_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-852">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="2ad59-853">Кэйвордс_спаин_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-854">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-854">tax id</span></span>
  
<span data-ttu-id="2ad59-855">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="2ad59-855">tax id number</span></span>
  
<span data-ttu-id="2ad59-856">Идентификатор CIF</span><span class="sxs-lookup"><span data-stu-id="2ad59-856">cif id</span></span>
  
<span data-ttu-id="2ad59-857">CIF нет</span><span class="sxs-lookup"><span data-stu-id="2ad59-857">cif no</span></span>
  
<span data-ttu-id="2ad59-858">код испанского CIF</span><span class="sxs-lookup"><span data-stu-id="2ad59-858">spanish cif id</span></span>
  
<span data-ttu-id="2ad59-859">CIF</span><span class="sxs-lookup"><span data-stu-id="2ad59-859">cif</span></span>
  
<span data-ttu-id="2ad59-860">Налоговый файл нет</span><span class="sxs-lookup"><span data-stu-id="2ad59-860">tax file no</span></span>
  
<span data-ttu-id="2ad59-861">номер испанского CIF</span><span class="sxs-lookup"><span data-stu-id="2ad59-861">spanish cif number</span></span>
  
<span data-ttu-id="2ad59-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="2ad59-862">tax file number</span></span>
  
<span data-ttu-id="2ad59-863">Испанская CIF</span><span class="sxs-lookup"><span data-stu-id="2ad59-863">spanish cif no</span></span>
  
<span data-ttu-id="2ad59-864">налог без</span><span class="sxs-lookup"><span data-stu-id="2ad59-864">tax no</span></span>
  
<span data-ttu-id="2ad59-865">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-865">tax number</span></span>
  
<span data-ttu-id="2ad59-866">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-866">taxid#</span></span>
  
<span data-ttu-id="2ad59-867">таксно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-867">taxno#</span></span>
  
<span data-ttu-id="2ad59-868">Цифид #</span><span class="sxs-lookup"><span data-stu-id="2ad59-868">cifid#</span></span>
  
<span data-ttu-id="2ad59-869">спанишЦифид #</span><span class="sxs-lookup"><span data-stu-id="2ad59-869">spanishcifid#</span></span>
  
<span data-ttu-id="2ad59-870">спанишЦифно #</span><span class="sxs-lookup"><span data-stu-id="2ad59-870">spanishcifno#</span></span>
  
<span data-ttu-id="2ad59-871">нúмеро de контрибуйенте</span><span class="sxs-lookup"><span data-stu-id="2ad59-871">número de contribuyente</span></span>
  
<span data-ttu-id="2ad59-872">нúмеро де импуесто корпоративо</span><span class="sxs-lookup"><span data-stu-id="2ad59-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="2ad59-873">нúмеро de идентификаЦиóн Фин.</span><span class="sxs-lookup"><span data-stu-id="2ad59-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="2ad59-874">CIF нúмеро</span><span class="sxs-lookup"><span data-stu-id="2ad59-874">cif número</span></span>
  
<span data-ttu-id="2ad59-875">Цифнúмеро #</span><span class="sxs-lookup"><span data-stu-id="2ad59-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="2ad59-876">Швеция</span><span class="sxs-lookup"><span data-stu-id="2ad59-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-877">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-877">Format</span></span>

<span data-ttu-id="2ad59-878">Десять цифр и символ в указанном шаблоне;</span><span class="sxs-lookup"><span data-stu-id="2ad59-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-879">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-879">Pattern</span></span>

<span data-ttu-id="2ad59-880">Десять цифр и символ:</span><span class="sxs-lookup"><span data-stu-id="2ad59-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="2ad59-881">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="2ad59-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="2ad59-882">Знак плюс, знак минус или обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="2ad59-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="2ad59-883">Три цифры, которые делают идентификационный номер уникальным, где:</span><span class="sxs-lookup"><span data-stu-id="2ad59-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="2ad59-884">Для номеров, выпущенных до 1990, седьмой и восьмой цифрой определяют район рождения или пользователей, порожденных иностранным пользователем.</span><span class="sxs-lookup"><span data-stu-id="2ad59-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="2ad59-885">Цифра в девятой позиции указывает на пол, который нечетен для пола или даже для розетки.</span><span class="sxs-lookup"><span data-stu-id="2ad59-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="2ad59-886">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="2ad59-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="2ad59-887">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-887">Checksum</span></span>

<span data-ttu-id="2ad59-888">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-889">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-889">Definition</span></span>

<span data-ttu-id="2ad59-890">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-891">Функция `Func_sweden_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-892">Найдено ключевое `Keywords_sweden_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="2ad59-893">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-894">Функция `Func_sweden_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-895">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="2ad59-896">Кэйвордс_сведен_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-897">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-897">tax id</span></span>
  
<span data-ttu-id="2ad59-898">Налоговый код но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-898">tax id no.</span></span>
  
<span data-ttu-id="2ad59-899">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="2ad59-899">tax id number</span></span>
  
<span data-ttu-id="2ad59-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="2ad59-900">tax identification</span></span>
  
<span data-ttu-id="2ad59-901">Налоговый идентификатор #</span><span class="sxs-lookup"><span data-stu-id="2ad59-901">tax identification#</span></span>
  
<span data-ttu-id="2ad59-902">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-902">tax no.</span></span>
  
<span data-ttu-id="2ad59-903">см</span><span class="sxs-lookup"><span data-stu-id="2ad59-903">tax#</span></span>
  
<span data-ttu-id="2ad59-904">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-904">taxid#</span></span>
  
<span data-ttu-id="2ad59-905">Налоговый файл</span><span class="sxs-lookup"><span data-stu-id="2ad59-905">tax file</span></span>
  
<span data-ttu-id="2ad59-906">Налоговый файл но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-906">tax file no.</span></span>
  
<span data-ttu-id="2ad59-907">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="2ad59-907">personal id number</span></span>
  
<span data-ttu-id="2ad59-908">Идентификатор СКАТТ нуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-908">skatt id nummer</span></span>
  
<span data-ttu-id="2ad59-909">СКАТТ идентификатион</span><span class="sxs-lookup"><span data-stu-id="2ad59-909">skatt identifikation</span></span>
  
<span data-ttu-id="2ad59-910">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="2ad59-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="2ad59-911">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="2ad59-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="2ad59-912">Format</span><span class="sxs-lookup"><span data-stu-id="2ad59-912">Format</span></span>

<span data-ttu-id="2ad59-913">Уникальная справочная информация о налогоплательщиках (утр): 10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="2ad59-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="2ad59-914">Национальный страховой номер (Нино): Дополнительные сведения см. в разделе "Великобритания</span><span class="sxs-lookup"><span data-stu-id="2ad59-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="2ad59-915">Национальный страховой номер (Нино) " [, чтобы найти типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="2ad59-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="2ad59-916">Шаблон</span><span class="sxs-lookup"><span data-stu-id="2ad59-916">Pattern</span></span>

<span data-ttu-id="2ad59-917">Уникальная справочная информация о налогоплательщиках (утр): 10 цифр</span><span class="sxs-lookup"><span data-stu-id="2ad59-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="2ad59-918">Национальный страховой номер (Нино): Дополнительные сведения см. в разделе "Великобритания</span><span class="sxs-lookup"><span data-stu-id="2ad59-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="2ad59-919">Национальный страховой номер (Нино) " [, чтобы найти типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="2ad59-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="2ad59-920">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="2ad59-920">Checksum</span></span>

<span data-ttu-id="2ad59-921">Да</span><span class="sxs-lookup"><span data-stu-id="2ad59-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="2ad59-922">Определение</span><span class="sxs-lookup"><span data-stu-id="2ad59-922">Definition</span></span>

<span data-ttu-id="2ad59-923">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="2ad59-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="2ad59-924">Функция `Func_uk_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="2ad59-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="2ad59-925">Найдено ключевое `Keywords_uk_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="2ad59-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="2ad59-926">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="2ad59-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="2ad59-927">Кэйвордс_ук_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="2ad59-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="2ad59-928">tax id</span><span class="sxs-lookup"><span data-stu-id="2ad59-928">tax id</span></span>
  
<span data-ttu-id="2ad59-929">Налоговый код но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-929">tax id no.</span></span>
  
<span data-ttu-id="2ad59-930">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="2ad59-930">tax id number</span></span>
  
<span data-ttu-id="2ad59-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="2ad59-931">tax identification</span></span>
  
<span data-ttu-id="2ad59-932">Налоговый идентификатор #</span><span class="sxs-lookup"><span data-stu-id="2ad59-932">tax identification#</span></span>
  
<span data-ttu-id="2ad59-933">налог но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-933">tax no.</span></span>
  
<span data-ttu-id="2ad59-934">см</span><span class="sxs-lookup"><span data-stu-id="2ad59-934">tax#</span></span>
  
<span data-ttu-id="2ad59-935">номер для такси</span><span class="sxs-lookup"><span data-stu-id="2ad59-935">taxid#</span></span>
  
<span data-ttu-id="2ad59-936">Налоговый файл</span><span class="sxs-lookup"><span data-stu-id="2ad59-936">tax file</span></span>
  
<span data-ttu-id="2ad59-937">Налоговый файл но.</span><span class="sxs-lookup"><span data-stu-id="2ad59-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ad59-938">См. также</span><span class="sxs-lookup"><span data-stu-id="2ad59-938">See also</span></span>

[<span data-ttu-id="2ad59-939">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="2ad59-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

