---
title: Идентификационный номер налогоплательщика ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации для идентификационного номера ЕС. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: adcd9be9b5f8775ad39010d771ff2ac214df1e17
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152961"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="0fa15-104">Идентификационный номер налогоплательщика ЕС</span><span class="sxs-lookup"><span data-stu-id="0fa15-104">EU Tax Identification Number</span></span>

<span data-ttu-id="0fa15-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации налогоплательщика (TIN).</span><span class="sxs-lookup"><span data-stu-id="0fa15-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="0fa15-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="0fa15-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="0fa15-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="0fa15-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-108">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-108">Format</span></span>

<span data-ttu-id="0fa15-109">Девять цифр с необязательным дефисом и косой чертой.</span><span class="sxs-lookup"><span data-stu-id="0fa15-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-110">Pattern</span></span>

<span data-ttu-id="0fa15-111">Девять цифр с необязательным дефисом и косой чертой.</span><span class="sxs-lookup"><span data-stu-id="0fa15-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="0fa15-112">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0fa15-112">Two digits</span></span> 
    
- <span data-ttu-id="0fa15-113">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0fa15-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="0fa15-114">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0fa15-114">Three digits</span></span>
    
- <span data-ttu-id="0fa15-115">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0fa15-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="0fa15-116">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0fa15-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-117">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-117">Checksum</span></span>

<span data-ttu-id="0fa15-118">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-119">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-119">Definition</span></span>

<span data-ttu-id="0fa15-120">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-121">Функция `Func_austria_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-122">Найдено ключевое `Keywords_austria_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-123">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-124">Функция `Func_austria_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-125">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="0fa15-126">Кэйвордс_аустриа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-127">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-127">tax number</span></span>
  
<span data-ttu-id="0fa15-128">число</span><span class="sxs-lookup"><span data-stu-id="0fa15-128">number</span></span>
  
<span data-ttu-id="0fa15-129">Регистрационный номер налогоплательщика</span><span class="sxs-lookup"><span data-stu-id="0fa15-129">tax registration number</span></span>
  
<span data-ttu-id="0fa15-130">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-130">tax id</span></span>
  
<span data-ttu-id="0fa15-131">st.nr.</span><span class="sxs-lookup"><span data-stu-id="0fa15-131">st.nr.</span></span>
  
<span data-ttu-id="0fa15-132">стеуернуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="0fa15-133">Бельгия</span><span class="sxs-lookup"><span data-stu-id="0fa15-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-134">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-134">Format</span></span>

<span data-ttu-id="0fa15-135">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-136">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-136">Pattern</span></span>

<span data-ttu-id="0fa15-137">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="0fa15-137">11 digits:</span></span>
  
- <span data-ttu-id="0fa15-138">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0fa15-138">Two digits</span></span>
    
- <span data-ttu-id="0fa15-139">"0" или "1"</span><span class="sxs-lookup"><span data-stu-id="0fa15-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="0fa15-140">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="0fa15-140">One digit</span></span>
    
- <span data-ttu-id="0fa15-141">"0" или "1" или "2" или "3"</span><span class="sxs-lookup"><span data-stu-id="0fa15-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="0fa15-142">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-143">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-143">Checksum</span></span>

<span data-ttu-id="0fa15-144">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-145">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-145">Definition</span></span>

<span data-ttu-id="0fa15-146">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-147">Регулярное выражение `Regex_belgium_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-148">Найдено ключевое `Keywords_belgium_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fa15-149">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="0fa15-150">Кэйвордс_белгиум_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-151">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-151">tax number</span></span>
  
<span data-ttu-id="0fa15-152">Национальный регистрационный номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-152">national registration number</span></span>
  
<span data-ttu-id="0fa15-153">Регистрационный номер налогоплательщика</span><span class="sxs-lookup"><span data-stu-id="0fa15-153">tax registration number</span></span>
  
<span data-ttu-id="0fa15-154">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-154">tax id</span></span>
  
<span data-ttu-id="0fa15-155">включена</span><span class="sxs-lookup"><span data-stu-id="0fa15-155">nif</span></span>
  
<span data-ttu-id="0fa15-156">включена</span><span class="sxs-lookup"><span data-stu-id="0fa15-156">nif#</span></span>
  
<span data-ttu-id="0fa15-157">нумéро de регистре National</span><span class="sxs-lookup"><span data-stu-id="0fa15-157">numéro de registre national</span></span>
  
<span data-ttu-id="0fa15-158">нумéро д'идентификатион Фин.</span><span class="sxs-lookup"><span data-stu-id="0fa15-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="0fa15-159">Болгария</span><span class="sxs-lookup"><span data-stu-id="0fa15-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-160">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-160">Format</span></span>

<span data-ttu-id="0fa15-161">Десять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-162">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-162">Pattern</span></span>

<span data-ttu-id="0fa15-163">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-164">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-164">Checksum</span></span>

<span data-ttu-id="0fa15-165">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-166">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-166">Definition</span></span>

<span data-ttu-id="0fa15-167">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-168">Функция `Func_bulgaria_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-169">Найдено ключевое `Keywords_bulgaria_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-170">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-171">Функция `Func_bulgaria_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-172">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="0fa15-173">Кэйвордс_булгариа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-174">Букн</span><span class="sxs-lookup"><span data-stu-id="0fa15-174">bucn</span></span>
  
<span data-ttu-id="0fa15-175">единое гражданское число</span><span class="sxs-lookup"><span data-stu-id="0fa15-175">uniform civil number</span></span>
  
<span data-ttu-id="0fa15-176">Букн #</span><span class="sxs-lookup"><span data-stu-id="0fa15-176">bucn#</span></span>
  
<span data-ttu-id="0fa15-177">униформЦивилнумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="0fa15-178">унифицированный гражданский идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-178">uniform civil id</span></span>
  
<span data-ttu-id="0fa15-179">равномерный гражданский номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-179">uniform civil no</span></span>
  
<span data-ttu-id="0fa15-180">ЕГН</span><span class="sxs-lookup"><span data-stu-id="0fa15-180">egn</span></span>
  
<span data-ttu-id="0fa15-181">номер унифицированного гражданства болгарского языка</span><span class="sxs-lookup"><span data-stu-id="0fa15-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="0fa15-182">униформЦивилно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-182">uniformcivilno#</span></span>
  
<span data-ttu-id="0fa15-183">ЕГН #</span><span class="sxs-lookup"><span data-stu-id="0fa15-183">egn#</span></span>
  
<span data-ttu-id="0fa15-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-184">униформ граждански номер</span></span>
  
<span data-ttu-id="0fa15-185">Идентификатор униформ</span><span class="sxs-lookup"><span data-stu-id="0fa15-185">униформ id</span></span>
  
<span data-ttu-id="0fa15-186">униформ граждански ID</span><span class="sxs-lookup"><span data-stu-id="0fa15-186">униформ граждански id</span></span>
  
<span data-ttu-id="0fa15-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="0fa15-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="0fa15-188">Хорватия</span><span class="sxs-lookup"><span data-stu-id="0fa15-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-189">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-189">Format</span></span>

<span data-ttu-id="0fa15-190">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-191">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-191">Pattern</span></span>

<span data-ttu-id="0fa15-192">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="0fa15-192">11 digits:</span></span>
  
- <span data-ttu-id="0fa15-193">Десять цифр, выбран случайным образом</span><span class="sxs-lookup"><span data-stu-id="0fa15-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="0fa15-194">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="0fa15-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-195">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-195">Checksum</span></span>

<span data-ttu-id="0fa15-196">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-197">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-197">Definition</span></span>

<span data-ttu-id="0fa15-198">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-199">Функция `Func_croatia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-200">Найдено ключевое `Keywords_croatia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-201">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-202">Функция `Func_croatia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-203">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="0fa15-204">Кэйвордс_кроатиа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-205">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-205">tax number</span></span>
  
<span data-ttu-id="0fa15-206">см</span><span class="sxs-lookup"><span data-stu-id="0fa15-206">tax</span></span>
  
<span data-ttu-id="0fa15-207">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-207">tax id</span></span>
  
<span data-ttu-id="0fa15-208">oid</span><span class="sxs-lookup"><span data-stu-id="0fa15-208">oid</span></span>
  
<span data-ttu-id="0fa15-209">идентификатора</span><span class="sxs-lookup"><span data-stu-id="0fa15-209">oid#</span></span>
  
<span data-ttu-id="0fa15-210">порезни Брож</span><span class="sxs-lookup"><span data-stu-id="0fa15-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="0fa15-211">Кипр</span><span class="sxs-lookup"><span data-stu-id="0fa15-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-212">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-212">Format</span></span>

<span data-ttu-id="0fa15-213">Восемь цифр и одна буква в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="0fa15-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-214">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-214">Pattern</span></span>

<span data-ttu-id="0fa15-215">Восемь цифр и одна буква:</span><span class="sxs-lookup"><span data-stu-id="0fa15-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="0fa15-216">"0"</span><span class="sxs-lookup"><span data-stu-id="0fa15-216">A "0"</span></span> 
    
- <span data-ttu-id="0fa15-217">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0fa15-217">Seven digits</span></span>
    
- <span data-ttu-id="0fa15-218">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-219">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-219">Checksum</span></span>

<span data-ttu-id="0fa15-220">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-221">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-221">Definition</span></span>

<span data-ttu-id="0fa15-222">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-223">Функция `Func_cyprus_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-224">Найдено ключевое `Keywords_cyprus_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-225">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-226">Функция `Func_cyprus_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="0fa15-228">Кэйвордс_ципрус_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-229">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-229">tax number</span></span>
  
<span data-ttu-id="0fa15-230">см</span><span class="sxs-lookup"><span data-stu-id="0fa15-230">tax</span></span>
  
<span data-ttu-id="0fa15-231">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-231">tax id</span></span>
  
<span data-ttu-id="0fa15-232">Налоговый код идентификации</span><span class="sxs-lookup"><span data-stu-id="0fa15-232">tax identification code</span></span>
  
<span data-ttu-id="0fa15-233">Тик</span><span class="sxs-lookup"><span data-stu-id="0fa15-233">tic</span></span>
  
<span data-ttu-id="0fa15-234">Тик #</span><span class="sxs-lookup"><span data-stu-id="0fa15-234">tic#</span></span>
  
<span data-ttu-id="0fa15-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0fa15-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="0fa15-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="0fa15-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="0fa15-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0fa15-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="0fa15-238">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="0fa15-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-239">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-239">Format</span></span>

<span data-ttu-id="0fa15-240">Девять или десять цифр с необязательной обратной косой чертой</span><span class="sxs-lookup"><span data-stu-id="0fa15-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-241">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-241">Pattern</span></span>

<span data-ttu-id="0fa15-242">Девять или десять цифр с необязательной обратной косой чертой.</span><span class="sxs-lookup"><span data-stu-id="0fa15-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="0fa15-243">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0fa15-243">Six digits</span></span> 
    
- <span data-ttu-id="0fa15-244">Обратная косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0fa15-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="0fa15-245">Три или четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0fa15-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-246">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-246">Checksum</span></span>

<span data-ttu-id="0fa15-247">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-248">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-248">Definition</span></span>

<span data-ttu-id="0fa15-249">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-250">Регулярное выражение `Regex_czech_republic_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-251">Найдено ключевое `Keywords_czech_republic_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fa15-252">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="0fa15-253">Кэйвордс_кзеч_републик_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-254">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-254">tax number</span></span>
  
<span data-ttu-id="0fa15-255">см</span><span class="sxs-lookup"><span data-stu-id="0fa15-255">tax</span></span>
  
<span data-ttu-id="0fa15-256">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-256">tax id</span></span>
  
<span data-ttu-id="0fa15-257">персональный номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-257">personal number</span></span>
  
<span data-ttu-id="0fa15-258">даňовé číсло</span><span class="sxs-lookup"><span data-stu-id="0fa15-258">daňové číslo</span></span>
  
<span data-ttu-id="0fa15-259">особнí číсло</span><span class="sxs-lookup"><span data-stu-id="0fa15-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="0fa15-260">Дания</span><span class="sxs-lookup"><span data-stu-id="0fa15-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-261">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-261">Format</span></span>

<span data-ttu-id="0fa15-262">Десять цифр, содержащие дефис</span><span class="sxs-lookup"><span data-stu-id="0fa15-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-263">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-263">Pattern</span></span>

<span data-ttu-id="0fa15-264">Десять цифр с дефисом:</span><span class="sxs-lookup"><span data-stu-id="0fa15-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="0fa15-265">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="0fa15-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="0fa15-266">дефис;</span><span class="sxs-lookup"><span data-stu-id="0fa15-266">A hyphen</span></span>
    
- <span data-ttu-id="0fa15-267">Четыре цифры, которые соответствуют порядковому номеру, где первая цифра соответствует столетию рождения, а последняя цифра соответствует полу лица (нечетный для пола и даже для женщина)</span><span class="sxs-lookup"><span data-stu-id="0fa15-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-268">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-268">Checksum</span></span>

<span data-ttu-id="0fa15-269">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-270">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-270">Definition</span></span>

<span data-ttu-id="0fa15-271">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-272">Функция `Func_denmark_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-273">Найдено ключевое `Keywords_denmark_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-275">Функция `Func_denmark_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-276">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="0fa15-277">Кэйвордс_денмарк_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-278">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-278">tax number</span></span>
  
<span data-ttu-id="0fa15-279">см</span><span class="sxs-lookup"><span data-stu-id="0fa15-279">tax</span></span>
  
<span data-ttu-id="0fa15-280">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-280">tax id</span></span>
  
<span data-ttu-id="0fa15-281">CPR Number</span><span class="sxs-lookup"><span data-stu-id="0fa15-281">cpr number</span></span>
  
<span data-ttu-id="0fa15-282">CPR</span><span class="sxs-lookup"><span data-stu-id="0fa15-282">cpr#</span></span>
  
<span data-ttu-id="0fa15-283">Скат нуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-283">skat nummer</span></span>
  
<span data-ttu-id="0fa15-284">Идентификатор Скат</span><span class="sxs-lookup"><span data-stu-id="0fa15-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="0fa15-285">Эстония</span><span class="sxs-lookup"><span data-stu-id="0fa15-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-286">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-286">Format</span></span>

<span data-ttu-id="0fa15-287">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-288">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-288">Pattern</span></span>

<span data-ttu-id="0fa15-289">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="0fa15-289">11 digits:</span></span>
  
-  <span data-ttu-id="0fa15-290">Одна цифра, соответствующая пол и столетию рождения, где нечетное число означает "штекер", а четное число указывает на женщина следующим образом: 1, 2 для 19 века; 3, 4 — 20 века; и 5, 6 для 21 века</span><span class="sxs-lookup"><span data-stu-id="0fa15-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="0fa15-291">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="0fa15-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="0fa15-292">Три цифры, которые соответствуют порядковому номеру, разделенному на одну и ту же дату.</span><span class="sxs-lookup"><span data-stu-id="0fa15-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="0fa15-293">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="0fa15-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-294">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-294">Checksum</span></span>

<span data-ttu-id="0fa15-295">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-296">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-296">Definition</span></span>

<span data-ttu-id="0fa15-297">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-298">Функция `Func_estonia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-299">Найдено ключевое `Keywords_estonia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-300">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-301">Функция `Func_estonia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-302">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="0fa15-303">Кэйвордс_естониа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-304">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-304">tax number</span></span>
  
<span data-ttu-id="0fa15-305">см</span><span class="sxs-lookup"><span data-stu-id="0fa15-305">tax</span></span>
  
<span data-ttu-id="0fa15-306">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-306">tax id</span></span>
  
<span data-ttu-id="0fa15-307">персональный код</span><span class="sxs-lookup"><span data-stu-id="0fa15-307">personal code</span></span>
  
<span data-ttu-id="0fa15-308">максунумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-308">maksunumber</span></span>
  
<span data-ttu-id="0fa15-309">Идентификатор Максу</span><span class="sxs-lookup"><span data-stu-id="0fa15-309">maksu id</span></span>
  
<span data-ttu-id="0fa15-310">исикукуд</span><span class="sxs-lookup"><span data-stu-id="0fa15-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="0fa15-311">Финляндия</span><span class="sxs-lookup"><span data-stu-id="0fa15-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-312">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-312">Format</span></span>

<span data-ttu-id="0fa15-313">Сочетание цифр, букв и плюса, а также знак минуса</span><span class="sxs-lookup"><span data-stu-id="0fa15-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-314">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-314">Pattern</span></span>

<span data-ttu-id="0fa15-315">Сочетание цифр, букв и плюса и знака "плюс" и "минус" (11 символов).</span><span class="sxs-lookup"><span data-stu-id="0fa15-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="0fa15-316">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0fa15-316">Six digits</span></span>
    
- <span data-ttu-id="0fa15-317">Один из следующих элементов: знак плюса, знак минуса или буква "a" (без учета регистра), где знак "плюс" (без учета регистра) означает 1900-1999, что знак "плюс" находится в диапазоне от 1 до 1800-1899, а "a" означает, что порожденный 2000 и после</span><span class="sxs-lookup"><span data-stu-id="0fa15-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="0fa15-318">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0fa15-318">Three digits</span></span>
    
- <span data-ttu-id="0fa15-319">Одна буква или один номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-320">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-320">Checksum</span></span>

<span data-ttu-id="0fa15-321">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-322">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-322">Definition</span></span>

<span data-ttu-id="0fa15-323">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-324">Функция `Func_finland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-325">Найдено ключевое `Keywords_finland_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-326">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-327">Функция `Func_finland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-328">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="0fa15-329">Кэйвордс_финланд_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-330">identification number</span><span class="sxs-lookup"><span data-stu-id="0fa15-330">identification number</span></span>
  
<span data-ttu-id="0fa15-331">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-331">personal id</span></span>
  
<span data-ttu-id="0fa15-332">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-332">identity number</span></span>
  
<span data-ttu-id="0fa15-333">Финский национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-333">finnish national id number</span></span>
  
<span data-ttu-id="0fa15-334">персоналиднумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-334">personalidnumber#</span></span>
  
<span data-ttu-id="0fa15-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="0fa15-335">national identification number</span></span>
  
<span data-ttu-id="0fa15-336">идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-336">id number</span></span>
  
<span data-ttu-id="0fa15-337">код страны</span><span class="sxs-lookup"><span data-stu-id="0fa15-337">national id no.</span></span>
  
<span data-ttu-id="0fa15-338">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-338">national id number</span></span>
  
<span data-ttu-id="0fa15-339">ID No</span><span class="sxs-lookup"><span data-stu-id="0fa15-339">id no</span></span>
  
<span data-ttu-id="0fa15-340">туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="0fa15-340">tunnistenumero</span></span>
  
<span data-ttu-id="0fa15-341">хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="0fa15-341">henkilötunnus</span></span>
  
<span data-ttu-id="0fa15-342">иксилöллинен хенкилöкохтаинен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="0fa15-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="0fa15-343">аинутлаатуинен хенкилöкохтаинен туннус</span><span class="sxs-lookup"><span data-stu-id="0fa15-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="0fa15-344">идентититти нумеро</span><span class="sxs-lookup"><span data-stu-id="0fa15-344">identiteetti numero</span></span>
  
<span data-ttu-id="0fa15-345">Суомен кансаллинен хенкилöтуннус</span><span class="sxs-lookup"><span data-stu-id="0fa15-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="0fa15-346">хенкилöтуннуснумеро #</span><span class="sxs-lookup"><span data-stu-id="0fa15-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="0fa15-347">кансаллисен туннистенумеро</span><span class="sxs-lookup"><span data-stu-id="0fa15-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="0fa15-348">туннуснумеро</span><span class="sxs-lookup"><span data-stu-id="0fa15-348">tunnusnumero</span></span>
  
<span data-ttu-id="0fa15-349">кансаллинен туннус нумеро</span><span class="sxs-lookup"><span data-stu-id="0fa15-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="0fa15-350">Франция</span><span class="sxs-lookup"><span data-stu-id="0fa15-350">France</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-351">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-351">Format</span></span>

<span data-ttu-id="0fa15-352">13 цифр для отдельных пользователей и девять цифр для сущностей</span><span class="sxs-lookup"><span data-stu-id="0fa15-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-353">Pattern</span></span>

<span data-ttu-id="0fa15-354">13 цифр для отдельных пользователей:</span><span class="sxs-lookup"><span data-stu-id="0fa15-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="0fa15-355">Одна цифра, которая должна быть равна 0, 1, 2 или 3</span><span class="sxs-lookup"><span data-stu-id="0fa15-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="0fa15-356">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-356">12 digits</span></span>
    
<span data-ttu-id="0fa15-357">Девять цифр для сущностей</span><span class="sxs-lookup"><span data-stu-id="0fa15-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-358">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-358">Checksum</span></span>

<span data-ttu-id="0fa15-359">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-360">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-360">Definition</span></span>

<span data-ttu-id="0fa15-361">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-362">Функция `Func_france_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-363">Найдено ключевое `Keywords_france_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-365">Функция `Func_france_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-366">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="0fa15-367">Кэйвордс_франце_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-368">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-368">tax identification number</span></span>
  
<span data-ttu-id="0fa15-369">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-369">tax number</span></span>
  
<span data-ttu-id="0fa15-370">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-370">tax id</span></span>
  
<span data-ttu-id="0fa15-371">нумéро д'идентификатион Фин.</span><span class="sxs-lookup"><span data-stu-id="0fa15-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="0fa15-372">Германия</span><span class="sxs-lookup"><span data-stu-id="0fa15-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-373">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-373">Format</span></span>

<span data-ttu-id="0fa15-374">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-375">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-375">Pattern</span></span>

<span data-ttu-id="0fa15-376">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="0fa15-376">11 digits :</span></span>
  
-  <span data-ttu-id="0fa15-377">Десять цифр</span><span class="sxs-lookup"><span data-stu-id="0fa15-377">Ten digits</span></span> 
    
- <span data-ttu-id="0fa15-378">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="0fa15-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-379">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-379">Checksum</span></span>

<span data-ttu-id="0fa15-380">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-381">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-381">Definition</span></span>

<span data-ttu-id="0fa15-382">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-383">Функция `Func_germany_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-384">Найдено ключевое `Keywords_germany_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-385">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-386">Функция `Func_germany_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-387">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="0fa15-388">Кэйвордс_жермани_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-389">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-389">tax number</span></span>
  
<span data-ttu-id="0fa15-390">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-390">tax no.</span></span>
  
<span data-ttu-id="0fa15-391">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-391">taxno#</span></span>
  
<span data-ttu-id="0fa15-392">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-392">taxnumber#</span></span>
  
<span data-ttu-id="0fa15-393">такснумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-393">taxnumber</span></span>
  
<span data-ttu-id="0fa15-394">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-394">tax id</span></span>
  
<span data-ttu-id="0fa15-395">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-395">taxid#</span></span>
  
<span data-ttu-id="0fa15-396">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-396">tax identification number</span></span>
  
<span data-ttu-id="0fa15-397">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-397">tax identification no.</span></span>
  
<span data-ttu-id="0fa15-398">стеуернуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-398">steuernummer</span></span>
  
<span data-ttu-id="0fa15-399">Идентификатор стеуер</span><span class="sxs-lookup"><span data-stu-id="0fa15-399">steuer id</span></span>
  
<span data-ttu-id="0fa15-400">стеуеридентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="0fa15-401">Греция</span><span class="sxs-lookup"><span data-stu-id="0fa15-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-402">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-402">Format</span></span>

<span data-ttu-id="0fa15-403">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-404">Pattern</span></span>

<span data-ttu-id="0fa15-405">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-406">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-406">Checksum</span></span>

<span data-ttu-id="0fa15-407">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-408">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-408">Definition</span></span>

<span data-ttu-id="0fa15-409">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-410">Регулярное выражение `Regex_greece_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-411">Найдено ключевое `Keywords_greece_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fa15-412">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="0fa15-413">Кэйвордс_грице_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-414">АФМ</span><span class="sxs-lookup"><span data-stu-id="0fa15-414">afm</span></span>
  
<span data-ttu-id="0fa15-415">ИНН</span><span class="sxs-lookup"><span data-stu-id="0fa15-415">tin</span></span>
  
<span data-ttu-id="0fa15-416">Налоговый код но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-416">tax id no.</span></span>
  
<span data-ttu-id="0fa15-417">Налоговый код No</span><span class="sxs-lookup"><span data-stu-id="0fa15-417">tax id no</span></span>
  
<span data-ttu-id="0fa15-418">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-418">tax identification number</span></span>
  
<span data-ttu-id="0fa15-419">Налоговый номер реестра</span><span class="sxs-lookup"><span data-stu-id="0fa15-419">tax registry number</span></span>
  
<span data-ttu-id="0fa15-420">реестр по номеру налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-420">tax registry no.</span></span>
  
<span data-ttu-id="0fa15-421">АФМ #</span><span class="sxs-lookup"><span data-stu-id="0fa15-421">afm#</span></span>
  
<span data-ttu-id="0fa15-422">ИНН</span><span class="sxs-lookup"><span data-stu-id="0fa15-422">tin#</span></span>
  
<span data-ttu-id="0fa15-423">таксидно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-423">taxidno#</span></span>
  
<span data-ttu-id="0fa15-424">таксрегистрино #</span><span class="sxs-lookup"><span data-stu-id="0fa15-424">taxregistryno#</span></span>
  
<span data-ttu-id="0fa15-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0fa15-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="0fa15-426">аφμ</span><span class="sxs-lookup"><span data-stu-id="0fa15-426">aφμ</span></span>
  
<span data-ttu-id="0fa15-427">аφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="0fa15-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="0fa15-428">φορολογικού μητρώου Νο.</span><span class="sxs-lookup"><span data-stu-id="0fa15-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="0fa15-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0fa15-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="0fa15-430">Венгрия</span><span class="sxs-lookup"><span data-stu-id="0fa15-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-431">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-431">Format</span></span>

<span data-ttu-id="0fa15-432">Десять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-433">Pattern</span></span>

<span data-ttu-id="0fa15-434">Десять цифр:</span><span class="sxs-lookup"><span data-stu-id="0fa15-434">Ten digits:</span></span>
  
-  <span data-ttu-id="0fa15-435">Одна цифра, которая должна быть "8"</span><span class="sxs-lookup"><span data-stu-id="0fa15-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="0fa15-436">Пять цифр, которые соответствуют количеству дней между датой 01/01/1867 и датой рождения отдельного лица.</span><span class="sxs-lookup"><span data-stu-id="0fa15-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="0fa15-437">Три цифры, которые соответствуют номеру, созданному шансом выделить людей, которые поставили один и тот же день.</span><span class="sxs-lookup"><span data-stu-id="0fa15-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="0fa15-438">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="0fa15-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-439">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-439">Checksum</span></span>

<span data-ttu-id="0fa15-440">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-441">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-441">Definition</span></span>

<span data-ttu-id="0fa15-442">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-443">Функция `Func_hungary_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-444">Найдено ключевое `Keywords_hungary_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-445">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-446">Функция `Func_hungary_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-447">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="0fa15-448">Кэйвордс_хунгари_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-449">идентификационный номер для венгерского налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="0fa15-450">Венгерский Tin</span><span class="sxs-lookup"><span data-stu-id="0fa15-450">hungarian tin</span></span>
  
<span data-ttu-id="0fa15-451">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="0fa15-451">tax id number</span></span>
  
<span data-ttu-id="0fa15-452">номер НДС</span><span class="sxs-lookup"><span data-stu-id="0fa15-452">vat number</span></span>
  
<span data-ttu-id="0fa15-453">Налоговый орган без</span><span class="sxs-lookup"><span data-stu-id="0fa15-453">tax authority no</span></span>
  
<span data-ttu-id="0fa15-454">идентификационный номер налогоплательщика для налогового кода</span><span class="sxs-lookup"><span data-stu-id="0fa15-454">tax id tax identity number</span></span>
  
<span data-ttu-id="0fa15-455">таксиднумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-455">taxidnumber#</span></span>
  
<span data-ttu-id="0fa15-456">ИНН</span><span class="sxs-lookup"><span data-stu-id="0fa15-456">tin#</span></span>
  
<span data-ttu-id="0fa15-457">хунгатиантин #</span><span class="sxs-lookup"><span data-stu-id="0fa15-457">hungatiantin#</span></span>
  
<span data-ttu-id="0fa15-458">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-458">tax identification no</span></span>
  
<span data-ttu-id="0fa15-459">таксидно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-459">taxidno#</span></span>
  
<span data-ttu-id="0fa15-460">адóазоносíтó сзáм</span><span class="sxs-lookup"><span data-stu-id="0fa15-460">adóazonosító szám</span></span>
  
<span data-ttu-id="0fa15-461">адóсзáм</span><span class="sxs-lookup"><span data-stu-id="0fa15-461">adószám</span></span>
  
<span data-ttu-id="0fa15-462">адóхатóсáг сзáм</span><span class="sxs-lookup"><span data-stu-id="0fa15-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="0fa15-463">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="0fa15-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-464">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-464">Format</span></span>

<span data-ttu-id="0fa15-465">Семь цифр, за которыми следует буква без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-466">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-466">Pattern</span></span>

<span data-ttu-id="0fa15-467">Семь цифр, за которыми следует буква:</span><span class="sxs-lookup"><span data-stu-id="0fa15-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="0fa15-468">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0fa15-468">Seven digits</span></span> 
    
- <span data-ttu-id="0fa15-469">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-470">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-470">Checksum</span></span>

<span data-ttu-id="0fa15-471">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-472">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-472">Definition</span></span>

<span data-ttu-id="0fa15-473">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-474">Функция `Func_ireland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-475">Найдено ключевое `Keywords_ireland_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-476">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-477">Функция `Func_ireland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-478">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="0fa15-479">Кэйвордс_иреланд_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-480">общедоступная служба</span><span class="sxs-lookup"><span data-stu-id="0fa15-480">public service no</span></span>
  
<span data-ttu-id="0fa15-481">Личная общедоступная служба</span><span class="sxs-lookup"><span data-stu-id="0fa15-481">personal public service no</span></span>
  
<span data-ttu-id="0fa15-482">PPS нет</span><span class="sxs-lookup"><span data-stu-id="0fa15-482">pps no</span></span>
  
<span data-ttu-id="0fa15-483">Личная служба</span><span class="sxs-lookup"><span data-stu-id="0fa15-483">personal service no</span></span>
  
<span data-ttu-id="0fa15-484">Служба PPS нет</span><span class="sxs-lookup"><span data-stu-id="0fa15-484">pps service no</span></span>
  
<span data-ttu-id="0fa15-485">ппсно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-485">ppsno#</span></span>
  
<span data-ttu-id="0fa15-486">Ирландский PPS No</span><span class="sxs-lookup"><span data-stu-id="0fa15-486">irish pps no</span></span>
  
<span data-ttu-id="0fa15-487">публиксервицено #</span><span class="sxs-lookup"><span data-stu-id="0fa15-487">publicserviceno#</span></span>
  
<span data-ttu-id="0fa15-488">номер личной общедоступной службы</span><span class="sxs-lookup"><span data-stu-id="0fa15-488">personal public service number</span></span>
  
<span data-ttu-id="0fa15-489">уимхир феарсанта сеирбхíсе поиблí</span><span class="sxs-lookup"><span data-stu-id="0fa15-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="0fa15-490">PPS уимх</span><span class="sxs-lookup"><span data-stu-id="0fa15-490">pps uimh</span></span>
  
<span data-ttu-id="0fa15-491">уимхир аисеантаис феарсанта</span><span class="sxs-lookup"><span data-stu-id="0fa15-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="0fa15-492">Италия</span><span class="sxs-lookup"><span data-stu-id="0fa15-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-493">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-493">Format</span></span>

<span data-ttu-id="0fa15-494">16 букв и цифр в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="0fa15-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-495">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-495">Pattern</span></span>

<span data-ttu-id="0fa15-496">16 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="0fa15-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="0fa15-497">Три буквы, соответствующие первым трем согласным в имени семейства</span><span class="sxs-lookup"><span data-stu-id="0fa15-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="0fa15-498">Три буквы, соответствующие первым, третьим и четвертым согласным в имени.</span><span class="sxs-lookup"><span data-stu-id="0fa15-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="0fa15-499">Две цифры, соответствующие последним цифрам года рождения</span><span class="sxs-lookup"><span data-stu-id="0fa15-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="0fa15-500">Одна цифра, соответствующая месяцу рождения, буквы используются в алфавитном порядке, но используются только буквы от A до E, H, L, M, P, R — T (то есть Январь — это R, а Октябрь — R)</span><span class="sxs-lookup"><span data-stu-id="0fa15-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="0fa15-501">Две цифры, которые соответствуют дню рождения, где 40 добавляется к дню рождения женщин, чтобы отличать от мужчин</span><span class="sxs-lookup"><span data-stu-id="0fa15-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="0fa15-502">Четыре цифры, соответствующие коду города, соответствующему органу государственной власти, в котором был создан пользователь, — коды уровня страны используются для иностранных стран</span><span class="sxs-lookup"><span data-stu-id="0fa15-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="0fa15-503">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="0fa15-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-504">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-504">Checksum</span></span>

<span data-ttu-id="0fa15-505">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-506">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-506">Definition</span></span>

<span data-ttu-id="0fa15-507">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-508">Функция `Func_italy_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-509">Найдено ключевое `Keywords_italy_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-510">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-511">Функция `Func_italy_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-512">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="0fa15-513">Кэйвордс_итали_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-514">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-514">tax number</span></span>
  
<span data-ttu-id="0fa15-515">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-515">tax no.</span></span>
  
<span data-ttu-id="0fa15-516">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-516">taxno#</span></span>
  
<span data-ttu-id="0fa15-517">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-517">taxnumber#</span></span>
  
<span data-ttu-id="0fa15-518">такснумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-518">taxnumber</span></span>
  
<span data-ttu-id="0fa15-519">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-519">tax id</span></span>
  
<span data-ttu-id="0fa15-520">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-520">taxid#</span></span>
  
<span data-ttu-id="0fa15-521">Финансовый код</span><span class="sxs-lookup"><span data-stu-id="0fa15-521">fiscal code</span></span>
  
<span data-ttu-id="0fa15-522">финансовый отчет по сокостям</span><span class="sxs-lookup"><span data-stu-id="0fa15-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="0fa15-523">Латвия</span><span class="sxs-lookup"><span data-stu-id="0fa15-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-524">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-524">Format</span></span>

<span data-ttu-id="0fa15-525">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-526">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-526">Pattern</span></span>

<span data-ttu-id="0fa15-527">11 цифр в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="0fa15-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="0fa15-528">Шесть цифр, соответствующих дате рождения (ДДММГГ —)</span><span class="sxs-lookup"><span data-stu-id="0fa15-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="0fa15-529">Одна цифра, соответствующая столетию рождения, где "0" соответствует 19 века, "1" соответствует 20 столетию, а "2" соответствует 21 столетию</span><span class="sxs-lookup"><span data-stu-id="0fa15-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="0fa15-530">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0fa15-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-531">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-531">Checksum</span></span>

<span data-ttu-id="0fa15-532">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-533">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-533">Definition</span></span>

<span data-ttu-id="0fa15-534">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-535">Функция `Func_latvia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-536">Найдено ключевое `Keywords_latvia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-537">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-538">Функция `Func_latvia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-539">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="0fa15-540">Кэйвордс_латвиа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-541">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-541">tax number</span></span>
  
<span data-ttu-id="0fa15-542">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-542">tax no.</span></span>
  
<span data-ttu-id="0fa15-543">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-543">taxno#</span></span>
  
<span data-ttu-id="0fa15-544">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-544">taxnumber#</span></span>
  
<span data-ttu-id="0fa15-545">такснумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-545">taxnumber</span></span>
  
<span data-ttu-id="0fa15-546">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-546">tax id</span></span>
  
<span data-ttu-id="0fa15-547">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-547">taxid#</span></span>
  
<span data-ttu-id="0fa15-548">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-548">tax identification number</span></span>
  
<span data-ttu-id="0fa15-549">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-549">tax identification no.</span></span>
  
<span data-ttu-id="0fa15-550">нодокļа нумурс</span><span class="sxs-lookup"><span data-stu-id="0fa15-550">nodokļa numurs</span></span>
  
<span data-ttu-id="0fa15-551">нодокļу идентификāЦижас нумурс</span><span class="sxs-lookup"><span data-stu-id="0fa15-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="0fa15-552">нодокļу идентификāЦижа нумурс</span><span class="sxs-lookup"><span data-stu-id="0fa15-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="0fa15-553">Литва</span><span class="sxs-lookup"><span data-stu-id="0fa15-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-554">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-554">Format</span></span>

<span data-ttu-id="0fa15-555">11 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-556">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-556">Pattern</span></span>

<span data-ttu-id="0fa15-557">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-558">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-558">Checksum</span></span>

<span data-ttu-id="0fa15-559">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-560">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-560">Definition</span></span>

<span data-ttu-id="0fa15-561">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-562">Функция `Func_lithuania_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-563">Найдено ключевое `Keywords_lithuania_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-564">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-565">Функция `Func_lithuania_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-566">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="0fa15-567">Кэйвордс_лисуаниа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-568">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-568">tax number</span></span>
  
<span data-ttu-id="0fa15-569">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-569">tax no.</span></span>
  
<span data-ttu-id="0fa15-570">налог No #</span><span class="sxs-lookup"><span data-stu-id="0fa15-570">tax no#</span></span>
  
<span data-ttu-id="0fa15-571">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-571">taxnumber#</span></span>
  
<span data-ttu-id="0fa15-572">такснумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-572">taxnumber</span></span>
  
<span data-ttu-id="0fa15-573">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-573">tax id</span></span>
  
<span data-ttu-id="0fa15-574">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-574">taxid#</span></span>
  
<span data-ttu-id="0fa15-575">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-575">tax identification number</span></span>
  
<span data-ttu-id="0fa15-576">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-576">tax identification no.</span></span>
  
<span data-ttu-id="0fa15-577">Идентификатор мокесčиų</span><span class="sxs-lookup"><span data-stu-id="0fa15-577">mokesčių id</span></span>
  
<span data-ttu-id="0fa15-578">мокесčиų нумерис</span><span class="sxs-lookup"><span data-stu-id="0fa15-578">mokesčių numeris</span></span>
  
<span data-ttu-id="0fa15-579">мокесčиų идентификавимас нумерис</span><span class="sxs-lookup"><span data-stu-id="0fa15-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="0fa15-580">Луксембург</span><span class="sxs-lookup"><span data-stu-id="0fa15-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-581">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-581">Format</span></span>

<span data-ttu-id="0fa15-582">13 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-583">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-583">Pattern</span></span>

<span data-ttu-id="0fa15-584">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="0fa15-584">13 digits:</span></span>
  
-  <span data-ttu-id="0fa15-585">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-585">11 digits</span></span> 
    
- <span data-ttu-id="0fa15-586">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="0fa15-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-587">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-587">Checksum</span></span>

<span data-ttu-id="0fa15-588">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-589">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-589">Definition</span></span>

<span data-ttu-id="0fa15-590">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-591">Функция `Func_luxemburg_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-592">Найдено ключевое `Keywords_luxemburg_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-593">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-594">Функция `Func_luxemburg_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-595">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="0fa15-596">Кэйвордс_луксембург_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-597">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-597">tax number</span></span>
  
<span data-ttu-id="0fa15-598">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-598">tax no.</span></span>
  
<span data-ttu-id="0fa15-599">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-599">taxno#</span></span>
  
<span data-ttu-id="0fa15-600">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-600">taxnumber#</span></span>
  
<span data-ttu-id="0fa15-601">такснумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-601">taxnumber</span></span>
  
<span data-ttu-id="0fa15-602">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-602">tax id</span></span>
  
<span data-ttu-id="0fa15-603">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-603">taxid#</span></span>
  
<span data-ttu-id="0fa15-604">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-604">tax identification number</span></span>
  
<span data-ttu-id="0fa15-605">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-605">tax identification no.</span></span>
  
<span data-ttu-id="0fa15-606">стеуернуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-606">steuernummer</span></span>
  
<span data-ttu-id="0fa15-607">Идентификатор стеуер</span><span class="sxs-lookup"><span data-stu-id="0fa15-607">steuer id</span></span>
  
<span data-ttu-id="0fa15-608">стеуеридентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="0fa15-609">Мальта</span><span class="sxs-lookup"><span data-stu-id="0fa15-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-610">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-610">Format</span></span>

<span data-ttu-id="0fa15-611">Для национальных замальтийский: 7 цифр и одна буква в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="0fa15-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="0fa15-612">Мальтийскийные страны и Мальтийский, не являющиеся субъектами: 9 цифр</span><span class="sxs-lookup"><span data-stu-id="0fa15-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-613">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-613">Pattern</span></span>

<span data-ttu-id="0fa15-614">Мальтийский национальные условия: 7 цифр и одна буква</span><span class="sxs-lookup"><span data-stu-id="0fa15-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="0fa15-615">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0fa15-615">Seven digits</span></span> 
    
- <span data-ttu-id="0fa15-616">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="0fa15-617">Мальтийскийные страны и Мальтийский, не являющиеся субъектами: 9 цифр</span><span class="sxs-lookup"><span data-stu-id="0fa15-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="0fa15-618">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="0fa15-619">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-619">Checksum</span></span>

<span data-ttu-id="0fa15-620">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-621">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-621">Definition</span></span>

<span data-ttu-id="0fa15-622">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-623">Функция `Func_malta_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-624">Найдено ключевое `Keywords_malta_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-625">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-626">Функция `Func_malta_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-627">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="0fa15-628">Кэйвордс_малта_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-629">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-629">tax number</span></span>
  
<span data-ttu-id="0fa15-630">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-630">tax no.</span></span>
  
<span data-ttu-id="0fa15-631">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-631">taxno#</span></span>
  
<span data-ttu-id="0fa15-632">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-632">taxnumber#</span></span>
  
<span data-ttu-id="0fa15-633">такснумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-633">taxnumber</span></span>
  
<span data-ttu-id="0fa15-634">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-634">tax id</span></span>
  
<span data-ttu-id="0fa15-635">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-635">taxid#</span></span>
  
<span data-ttu-id="0fa15-636">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-636">tax identification number</span></span>
  
<span data-ttu-id="0fa15-637">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-637">tax identification no.</span></span>
  
<span data-ttu-id="0fa15-638">нумру ТАТ — такскса</span><span class="sxs-lookup"><span data-stu-id="0fa15-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="0fa15-639">ID ТАТ — такскса</span><span class="sxs-lookup"><span data-stu-id="0fa15-639">id tat-taxxa</span></span>
  
<span data-ttu-id="0fa15-640">нумру Ta ' идентификаззжони ТАТ такскса</span><span class="sxs-lookup"><span data-stu-id="0fa15-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="0fa15-641">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="0fa15-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-642">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-642">Format</span></span>

<span data-ttu-id="0fa15-643">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-644">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-644">Pattern</span></span>

<span data-ttu-id="0fa15-645">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0fa15-646">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-646">Checksum</span></span>

<span data-ttu-id="0fa15-647">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-648">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-648">Definition</span></span>

<span data-ttu-id="0fa15-649">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-650">Функция `Func_netherlands_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-651">Найдено ключевое `Keywords_netherlands_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-652">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-653">Функция `Func_netherlands_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-654">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="0fa15-655">Кэйвордс_несерландс_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-656">идентификационный номер налога Нидерландов</span><span class="sxs-lookup"><span data-stu-id="0fa15-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="0fa15-657">Идентификация налога Нидерландов</span><span class="sxs-lookup"><span data-stu-id="0fa15-657">netherlands tax identification</span></span>
  
<span data-ttu-id="0fa15-658">идентификационный номер налога несерланд</span><span class="sxs-lookup"><span data-stu-id="0fa15-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="0fa15-659">Налоговый код несерланд</span><span class="sxs-lookup"><span data-stu-id="0fa15-659">netherland's tax identification</span></span>
  
<span data-ttu-id="0fa15-660">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-660">tax identification number</span></span>
  
<span data-ttu-id="0fa15-661">Налоговый идентификатор голландского налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-661">dutch tax id</span></span>
  
<span data-ttu-id="0fa15-662">идентификационный номер налога на нидерландском языке</span><span class="sxs-lookup"><span data-stu-id="0fa15-662">dutch tax identification number</span></span>
  
<span data-ttu-id="0fa15-663">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-663">tax id</span></span>
  
<span data-ttu-id="0fa15-664">Налоговый идентификатор #</span><span class="sxs-lookup"><span data-stu-id="0fa15-664">tax id#</span></span>
  
<span data-ttu-id="0fa15-665">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-665">tax number</span></span>
  
<span data-ttu-id="0fa15-666">налог No #</span><span class="sxs-lookup"><span data-stu-id="0fa15-666">tax no#</span></span>
  
<span data-ttu-id="0fa15-667">см</span><span class="sxs-lookup"><span data-stu-id="0fa15-667">tax#</span></span>
  
<span data-ttu-id="0fa15-668">ИНН</span><span class="sxs-lookup"><span data-stu-id="0fa15-668">tin</span></span>
  
<span data-ttu-id="0fa15-669">ИНН</span><span class="sxs-lookup"><span data-stu-id="0fa15-669">tin#</span></span>
  
<span data-ttu-id="0fa15-670">Tin Нидерландов</span><span class="sxs-lookup"><span data-stu-id="0fa15-670">netherlands tin</span></span>
  
<span data-ttu-id="0fa15-671">Tin несерланд</span><span class="sxs-lookup"><span data-stu-id="0fa15-671">netherland's tin</span></span>
  
<span data-ttu-id="0fa15-672">Недерландс идентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="0fa15-673">идентификатиенуммер Van</span><span class="sxs-lookup"><span data-stu-id="0fa15-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="0fa15-674">идентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="0fa15-675">Недерландс идентификатие</span><span class="sxs-lookup"><span data-stu-id="0fa15-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="0fa15-676">Недерландс — идентификатор нуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="0fa15-677">Недерландс беластингнуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="0fa15-678">БТВ нуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-678">btw nummer</span></span>
  
<span data-ttu-id="0fa15-679">Недерландсе идентификатие</span><span class="sxs-lookup"><span data-stu-id="0fa15-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="0fa15-680">Польша</span><span class="sxs-lookup"><span data-stu-id="0fa15-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-681">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-681">Format</span></span>

<span data-ttu-id="0fa15-682">Одиннадцать цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-683">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-683">Pattern</span></span>

<span data-ttu-id="0fa15-684">Одиннадцать цифр</span><span class="sxs-lookup"><span data-stu-id="0fa15-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-685">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-685">Checksum</span></span>

<span data-ttu-id="0fa15-686">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-687">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-687">Definition</span></span>

<span data-ttu-id="0fa15-688">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-689">Функция `Func_poland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-690">Найдено ключевое `Keywords_poland_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-691">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-692">Функция `Func_poland_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-693">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="0fa15-694">Кэйвордс_поланд_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-695">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-695">tax number</span></span>
  
<span data-ttu-id="0fa15-696">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-696">tax no.</span></span>
  
<span data-ttu-id="0fa15-697">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-697">taxno#</span></span>
  
<span data-ttu-id="0fa15-698">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-698">taxnumber#</span></span>
  
<span data-ttu-id="0fa15-699">такснумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-699">taxnumber</span></span>
  
<span data-ttu-id="0fa15-700">НИП</span><span class="sxs-lookup"><span data-stu-id="0fa15-700">nip</span></span>
  
<span data-ttu-id="0fa15-701">НИП #</span><span class="sxs-lookup"><span data-stu-id="0fa15-701">nip#</span></span>
  
<span data-ttu-id="0fa15-702">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-702">tax id</span></span>
  
<span data-ttu-id="0fa15-703">Налоговый идентификатор #</span><span class="sxs-lookup"><span data-stu-id="0fa15-703">tax id#</span></span>
  
<span data-ttu-id="0fa15-704">Идентификатор НИП</span><span class="sxs-lookup"><span data-stu-id="0fa15-704">nip id</span></span>
  
<span data-ttu-id="0fa15-705">Идентификатор НИП</span><span class="sxs-lookup"><span data-stu-id="0fa15-705">nip id#</span></span>
  
<span data-ttu-id="0fa15-706">идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="0fa15-706">tax identification number</span></span>
  
<span data-ttu-id="0fa15-707">Налоговый идентификатор</span><span class="sxs-lookup"><span data-stu-id="0fa15-707">tax identification no.</span></span>
  
<span data-ttu-id="0fa15-708">номер НДС</span><span class="sxs-lookup"><span data-stu-id="0fa15-708">vat number</span></span>
  
<span data-ttu-id="0fa15-709">НДС номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-709">vat no.</span></span>
  
<span data-ttu-id="0fa15-710">ватно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-710">vatno#</span></span>
  
<span data-ttu-id="0fa15-711">Код НДС</span><span class="sxs-lookup"><span data-stu-id="0fa15-711">vat id</span></span>
  
<span data-ttu-id="0fa15-712">Идентификатор НДС</span><span class="sxs-lookup"><span data-stu-id="0fa15-712">vat id#</span></span>
  
<span data-ttu-id="0fa15-713">Нумер идентификакжи податковеж</span><span class="sxs-lookup"><span data-stu-id="0fa15-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="0fa15-714">полски нумер идентификакжи податковеж</span><span class="sxs-lookup"><span data-stu-id="0fa15-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="0fa15-715">нумеридентификакжиподатковеж #</span><span class="sxs-lookup"><span data-stu-id="0fa15-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="0fa15-716">Португалия</span><span class="sxs-lookup"><span data-stu-id="0fa15-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-717">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-717">Format</span></span>

<span data-ttu-id="0fa15-718">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-719">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-719">Pattern</span></span>

<span data-ttu-id="0fa15-720">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-721">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-721">Checksum</span></span>

<span data-ttu-id="0fa15-722">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-723">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-723">Definition</span></span>

<span data-ttu-id="0fa15-724">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-725">Функция `Func_portugal_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-726">Найдено ключевое `Keywords_portugal_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-727">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-728">Функция `Func_portugal_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-729">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="0fa15-730">Кэйвордс_португал_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-731">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-731">tax number</span></span>
  
<span data-ttu-id="0fa15-732">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-732">tax no.</span></span>
  
<span data-ttu-id="0fa15-733">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-733">taxno#</span></span>
  
<span data-ttu-id="0fa15-734">такснумбер #</span><span class="sxs-lookup"><span data-stu-id="0fa15-734">taxnumber#</span></span>
  
<span data-ttu-id="0fa15-735">такснумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-735">taxnumber</span></span>
  
<span data-ttu-id="0fa15-736">включена</span><span class="sxs-lookup"><span data-stu-id="0fa15-736">nif</span></span>
  
<span data-ttu-id="0fa15-737">включена</span><span class="sxs-lookup"><span data-stu-id="0fa15-737">nif#</span></span>
  
<span data-ttu-id="0fa15-738">финансовый нумеро</span><span class="sxs-lookup"><span data-stu-id="0fa15-738">numero fiscal</span></span>
  
<span data-ttu-id="0fa15-739">нúмеро de идентификаçãо Фин.</span><span class="sxs-lookup"><span data-stu-id="0fa15-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="0fa15-740">Румыния</span><span class="sxs-lookup"><span data-stu-id="0fa15-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-741">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-741">Format</span></span>

<span data-ttu-id="0fa15-742">13 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-743">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-743">Pattern</span></span>

<span data-ttu-id="0fa15-744">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-745">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-745">Checksum</span></span>

<span data-ttu-id="0fa15-746">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-747">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-747">Definition</span></span>

<span data-ttu-id="0fa15-748">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-749">Регулярное выражение `Regex_romania_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-750">Найдено ключевое `Keywords_romania_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fa15-751">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="0fa15-752">Кэйвордс_романиа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-753">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-753">tax id</span></span>
  
<span data-ttu-id="0fa15-754">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="0fa15-754">tax id number</span></span>
  
<span data-ttu-id="0fa15-755">Налоговый файл нет</span><span class="sxs-lookup"><span data-stu-id="0fa15-755">tax file no</span></span>
  
<span data-ttu-id="0fa15-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="0fa15-756">tax file number</span></span>
  
<span data-ttu-id="0fa15-757">налог без</span><span class="sxs-lookup"><span data-stu-id="0fa15-757">tax no</span></span>
  
<span data-ttu-id="0fa15-758">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-758">tax number</span></span>
  
<span data-ttu-id="0fa15-759">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-759">taxid#</span></span>
  
<span data-ttu-id="0fa15-760">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-760">taxno#</span></span>
  
<span data-ttu-id="0fa15-761">ID — UL таксеи</span><span class="sxs-lookup"><span data-stu-id="0fa15-761">id-ul taxei</span></span>
  
<span data-ttu-id="0fa15-762">нумăрул де идентификаре фискалă</span><span class="sxs-lookup"><span data-stu-id="0fa15-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="0fa15-763">Словакия</span><span class="sxs-lookup"><span data-stu-id="0fa15-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-764">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-764">Format</span></span>

<span data-ttu-id="0fa15-765">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-766">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-766">Pattern</span></span>

<span data-ttu-id="0fa15-767">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-768">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-768">Checksum</span></span>

<span data-ttu-id="0fa15-769">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="0fa15-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-770">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-770">Definition</span></span>

<span data-ttu-id="0fa15-771">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-772">Регулярное выражение `Regex_slovakia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-773">Найдено ключевое `Keywords_slovakia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fa15-774">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="0fa15-775">Кэйвордс_словакиа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-776">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-776">tax id</span></span>
  
<span data-ttu-id="0fa15-777">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="0fa15-777">tax id number</span></span>
  
<span data-ttu-id="0fa15-778">Идентификатор Tin</span><span class="sxs-lookup"><span data-stu-id="0fa15-778">tin id</span></span>
  
<span data-ttu-id="0fa15-779">номер Tin</span><span class="sxs-lookup"><span data-stu-id="0fa15-779">tin no</span></span>
  
<span data-ttu-id="0fa15-780">Идентификатор Tin словакиан</span><span class="sxs-lookup"><span data-stu-id="0fa15-780">slovakian tin id</span></span>
  
<span data-ttu-id="0fa15-781">ИНН</span><span class="sxs-lookup"><span data-stu-id="0fa15-781">tin</span></span>
  
<span data-ttu-id="0fa15-782">Налоговый файл нет</span><span class="sxs-lookup"><span data-stu-id="0fa15-782">tax file no</span></span>
  
<span data-ttu-id="0fa15-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="0fa15-783">tax file number</span></span>
  
<span data-ttu-id="0fa15-784">налог без</span><span class="sxs-lookup"><span data-stu-id="0fa15-784">tax no</span></span>
  
<span data-ttu-id="0fa15-785">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-785">tax number</span></span>
  
<span data-ttu-id="0fa15-786">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-786">taxid#</span></span>
  
<span data-ttu-id="0fa15-787">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-787">taxno#</span></span>
  
<span data-ttu-id="0fa15-788">даňовé идентификаčнé číсло</span><span class="sxs-lookup"><span data-stu-id="0fa15-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="0fa15-789">даňовé číсло</span><span class="sxs-lookup"><span data-stu-id="0fa15-789">daňové číslo</span></span>
  
<span data-ttu-id="0fa15-790">даňовé číсло сúбору</span><span class="sxs-lookup"><span data-stu-id="0fa15-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="0fa15-791">Словения</span><span class="sxs-lookup"><span data-stu-id="0fa15-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-792">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-792">Format</span></span>

<span data-ttu-id="0fa15-793">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-794">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-794">Pattern</span></span>

<span data-ttu-id="0fa15-795">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-796">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-796">Checksum</span></span>

<span data-ttu-id="0fa15-797">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-798">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-798">Definition</span></span>

<span data-ttu-id="0fa15-799">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-800">Функция `Func_slovenia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-801">Найдено ключевое `Keywords_slovenia_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-802">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-803">Функция `Func_slovenia_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-804">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="0fa15-805">Кэйвордс_словениа_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-806">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-806">tax id</span></span>
  
<span data-ttu-id="0fa15-807">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="0fa15-807">tax id number</span></span>
  
<span data-ttu-id="0fa15-808">Идентификатор Tin</span><span class="sxs-lookup"><span data-stu-id="0fa15-808">tin id</span></span>
  
<span data-ttu-id="0fa15-809">номер Tin</span><span class="sxs-lookup"><span data-stu-id="0fa15-809">tin no</span></span>
  
<span data-ttu-id="0fa15-810">Словенский идентификатор Tin</span><span class="sxs-lookup"><span data-stu-id="0fa15-810">slovenian tin id</span></span>
  
<span data-ttu-id="0fa15-811">ИНН</span><span class="sxs-lookup"><span data-stu-id="0fa15-811">tin</span></span>
  
<span data-ttu-id="0fa15-812">Налоговый файл нет</span><span class="sxs-lookup"><span data-stu-id="0fa15-812">tax file no</span></span>
  
<span data-ttu-id="0fa15-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="0fa15-813">tax file number</span></span>
  
<span data-ttu-id="0fa15-814">налог без</span><span class="sxs-lookup"><span data-stu-id="0fa15-814">tax no</span></span>
  
<span data-ttu-id="0fa15-815">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-815">tax number</span></span>
  
<span data-ttu-id="0fa15-816">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-816">taxid#</span></span>
  
<span data-ttu-id="0fa15-817">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-817">taxno#</span></span>
  
<span data-ttu-id="0fa15-818">идентификаЦижска šтевилка Давка</span><span class="sxs-lookup"><span data-stu-id="0fa15-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="0fa15-819">давčна šтевилка</span><span class="sxs-lookup"><span data-stu-id="0fa15-819">davčna številka</span></span>
  
<span data-ttu-id="0fa15-820">šтевилка давčне датотеке</span><span class="sxs-lookup"><span data-stu-id="0fa15-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="0fa15-821">Испания</span><span class="sxs-lookup"><span data-stu-id="0fa15-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-822">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-822">Format</span></span>

<span data-ttu-id="0fa15-823">Семь или восемь цифр, а также одна или две буквы в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="0fa15-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-824">Pattern</span></span>

<span data-ttu-id="0fa15-825">Испанские пользователи с национальной идентификационной карточкой Испании Испания:</span><span class="sxs-lookup"><span data-stu-id="0fa15-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="0fa15-826">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0fa15-826">Eight digits</span></span> 
    
- <span data-ttu-id="0fa15-827">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0fa15-828">Нерезидентские Спаниардс без национальной идентификационной карточки Испании</span><span class="sxs-lookup"><span data-stu-id="0fa15-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="0fa15-829">Одна прописная буква L (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="0fa15-830">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0fa15-830">Seven digits</span></span>
    
- <span data-ttu-id="0fa15-831">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0fa15-832">Резидентный Спаниардс в течение 14 лет без международной идентификационной карточки для Испании:</span><span class="sxs-lookup"><span data-stu-id="0fa15-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="0fa15-833">Одна прописная буква K (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="0fa15-834">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0fa15-834">Seven digits</span></span> 
    
- <span data-ttu-id="0fa15-835">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="0fa15-836">Фореигнерс с идентификационным номером внешнего получателя</span><span class="sxs-lookup"><span data-stu-id="0fa15-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="0fa15-837">Одна прописная буква "X", "Y" или "Z" (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="0fa15-838">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0fa15-838">Seven digits</span></span>
    
- <span data-ttu-id="0fa15-839">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0fa15-840">Фореигнерс без идентификационного номера внешнего получателя</span><span class="sxs-lookup"><span data-stu-id="0fa15-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="0fa15-841">Одна прописная буква "M" (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="0fa15-842">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0fa15-842">Seven digits</span></span>
    
- <span data-ttu-id="0fa15-843">Одна прописная буква (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0fa15-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="0fa15-844">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-844">Checksum</span></span>

<span data-ttu-id="0fa15-845">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-846">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-846">Definition</span></span>

<span data-ttu-id="0fa15-847">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-848">Функция `Func_spain_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-849">Найдено ключевое `Keywords_spain_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-850">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-851">Функция `Func_spain_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-852">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="0fa15-853">Кэйвордс_спаин_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-854">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-854">tax id</span></span>
  
<span data-ttu-id="0fa15-855">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="0fa15-855">tax id number</span></span>
  
<span data-ttu-id="0fa15-856">Идентификатор CIF</span><span class="sxs-lookup"><span data-stu-id="0fa15-856">cif id</span></span>
  
<span data-ttu-id="0fa15-857">CIF нет</span><span class="sxs-lookup"><span data-stu-id="0fa15-857">cif no</span></span>
  
<span data-ttu-id="0fa15-858">код испанского CIF</span><span class="sxs-lookup"><span data-stu-id="0fa15-858">spanish cif id</span></span>
  
<span data-ttu-id="0fa15-859">CIF</span><span class="sxs-lookup"><span data-stu-id="0fa15-859">cif</span></span>
  
<span data-ttu-id="0fa15-860">Налоговый файл нет</span><span class="sxs-lookup"><span data-stu-id="0fa15-860">tax file no</span></span>
  
<span data-ttu-id="0fa15-861">номер испанского CIF</span><span class="sxs-lookup"><span data-stu-id="0fa15-861">spanish cif number</span></span>
  
<span data-ttu-id="0fa15-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="0fa15-862">tax file number</span></span>
  
<span data-ttu-id="0fa15-863">Испанская CIF</span><span class="sxs-lookup"><span data-stu-id="0fa15-863">spanish cif no</span></span>
  
<span data-ttu-id="0fa15-864">налог без</span><span class="sxs-lookup"><span data-stu-id="0fa15-864">tax no</span></span>
  
<span data-ttu-id="0fa15-865">Налоговый номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-865">tax number</span></span>
  
<span data-ttu-id="0fa15-866">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-866">taxid#</span></span>
  
<span data-ttu-id="0fa15-867">таксно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-867">taxno#</span></span>
  
<span data-ttu-id="0fa15-868">Цифид #</span><span class="sxs-lookup"><span data-stu-id="0fa15-868">cifid#</span></span>
  
<span data-ttu-id="0fa15-869">спанишЦифид #</span><span class="sxs-lookup"><span data-stu-id="0fa15-869">spanishcifid#</span></span>
  
<span data-ttu-id="0fa15-870">спанишЦифно #</span><span class="sxs-lookup"><span data-stu-id="0fa15-870">spanishcifno#</span></span>
  
<span data-ttu-id="0fa15-871">нúмеро de контрибуйенте</span><span class="sxs-lookup"><span data-stu-id="0fa15-871">número de contribuyente</span></span>
  
<span data-ttu-id="0fa15-872">нúмеро де импуесто корпоративо</span><span class="sxs-lookup"><span data-stu-id="0fa15-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="0fa15-873">нúмеро de идентификаЦиóн Фин.</span><span class="sxs-lookup"><span data-stu-id="0fa15-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="0fa15-874">CIF нúмеро</span><span class="sxs-lookup"><span data-stu-id="0fa15-874">cif número</span></span>
  
<span data-ttu-id="0fa15-875">Цифнúмеро #</span><span class="sxs-lookup"><span data-stu-id="0fa15-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="0fa15-876">Швеция</span><span class="sxs-lookup"><span data-stu-id="0fa15-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-877">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-877">Format</span></span>

<span data-ttu-id="0fa15-878">Десять цифр и символ в указанном шаблоне;</span><span class="sxs-lookup"><span data-stu-id="0fa15-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-879">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-879">Pattern</span></span>

<span data-ttu-id="0fa15-880">Десять цифр и символ:</span><span class="sxs-lookup"><span data-stu-id="0fa15-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="0fa15-881">Шесть цифр, соответствующих дате рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="0fa15-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="0fa15-882">Знак плюс, знак минус или обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="0fa15-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="0fa15-883">Три цифры, которые делают идентификационный номер уникальным, где:</span><span class="sxs-lookup"><span data-stu-id="0fa15-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="0fa15-884">Для номеров, выпущенных до 1990, седьмой и восьмой цифрой определяют район рождения или пользователей, порожденных иностранным пользователем.</span><span class="sxs-lookup"><span data-stu-id="0fa15-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="0fa15-885">Цифра в девятой позиции указывает на пол, который нечетен для пола или даже для розетки.</span><span class="sxs-lookup"><span data-stu-id="0fa15-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="0fa15-886">Одна контрольная цифра</span><span class="sxs-lookup"><span data-stu-id="0fa15-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0fa15-887">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-887">Checksum</span></span>

<span data-ttu-id="0fa15-888">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-889">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-889">Definition</span></span>

<span data-ttu-id="0fa15-890">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-891">Функция `Func_sweden_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-892">Найдено ключевое `Keywords_sweden_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0fa15-893">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-894">Функция `Func_sweden_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="0fa15-895">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="0fa15-896">Кэйвордс_сведен_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-897">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-897">tax id</span></span>
  
<span data-ttu-id="0fa15-898">Налоговый код но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-898">tax id no.</span></span>
  
<span data-ttu-id="0fa15-899">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="0fa15-899">tax id number</span></span>
  
<span data-ttu-id="0fa15-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="0fa15-900">tax identification</span></span>
  
<span data-ttu-id="0fa15-901">Налоговый идентификатор #</span><span class="sxs-lookup"><span data-stu-id="0fa15-901">tax identification#</span></span>
  
<span data-ttu-id="0fa15-902">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-902">tax no.</span></span>
  
<span data-ttu-id="0fa15-903">см</span><span class="sxs-lookup"><span data-stu-id="0fa15-903">tax#</span></span>
  
<span data-ttu-id="0fa15-904">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-904">taxid#</span></span>
  
<span data-ttu-id="0fa15-905">Налоговый файл</span><span class="sxs-lookup"><span data-stu-id="0fa15-905">tax file</span></span>
  
<span data-ttu-id="0fa15-906">Налоговый файл но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-906">tax file no.</span></span>
  
<span data-ttu-id="0fa15-907">личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0fa15-907">personal id number</span></span>
  
<span data-ttu-id="0fa15-908">Идентификатор СКАТТ нуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-908">skatt id nummer</span></span>
  
<span data-ttu-id="0fa15-909">СКАТТ идентификатион</span><span class="sxs-lookup"><span data-stu-id="0fa15-909">skatt identifikation</span></span>
  
<span data-ttu-id="0fa15-910">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="0fa15-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="0fa15-911">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="0fa15-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="0fa15-912">Format</span><span class="sxs-lookup"><span data-stu-id="0fa15-912">Format</span></span>

<span data-ttu-id="0fa15-913">Уникальная справочная информация о налогоплательщиках (утр): 10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0fa15-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="0fa15-914">Национальный страховой номер (Нино): Дополнительные сведения см. в разделе "Великобритания</span><span class="sxs-lookup"><span data-stu-id="0fa15-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="0fa15-915">Национальный страховой номер (Нино) " [, чтобы найти типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0fa15-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0fa15-916">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0fa15-916">Pattern</span></span>

<span data-ttu-id="0fa15-917">Уникальная справочная информация о налогоплательщиках (утр): 10 цифр</span><span class="sxs-lookup"><span data-stu-id="0fa15-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="0fa15-918">Национальный страховой номер (Нино): Дополнительные сведения см. в разделе "Великобритания</span><span class="sxs-lookup"><span data-stu-id="0fa15-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="0fa15-919">Национальный страховой номер (Нино) " [, чтобы найти типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0fa15-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0fa15-920">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0fa15-920">Checksum</span></span>

<span data-ttu-id="0fa15-921">Да</span><span class="sxs-lookup"><span data-stu-id="0fa15-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0fa15-922">Определение</span><span class="sxs-lookup"><span data-stu-id="0fa15-922">Definition</span></span>

<span data-ttu-id="0fa15-923">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0fa15-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0fa15-924">Функция `Func_uk_eu_tax_file_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0fa15-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0fa15-925">Найдено ключевое `Keywords_uk_eu_tax_file_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0fa15-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0fa15-926">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0fa15-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="0fa15-927">Кэйвордс_ук_еу_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="0fa15-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="0fa15-928">tax id</span><span class="sxs-lookup"><span data-stu-id="0fa15-928">tax id</span></span>
  
<span data-ttu-id="0fa15-929">Налоговый код но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-929">tax id no.</span></span>
  
<span data-ttu-id="0fa15-930">номер налогового удостоверения</span><span class="sxs-lookup"><span data-stu-id="0fa15-930">tax id number</span></span>
  
<span data-ttu-id="0fa15-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="0fa15-931">tax identification</span></span>
  
<span data-ttu-id="0fa15-932">Налоговый идентификатор #</span><span class="sxs-lookup"><span data-stu-id="0fa15-932">tax identification#</span></span>
  
<span data-ttu-id="0fa15-933">налог но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-933">tax no.</span></span>
  
<span data-ttu-id="0fa15-934">см</span><span class="sxs-lookup"><span data-stu-id="0fa15-934">tax#</span></span>
  
<span data-ttu-id="0fa15-935">номер для такси</span><span class="sxs-lookup"><span data-stu-id="0fa15-935">taxid#</span></span>
  
<span data-ttu-id="0fa15-936">Налоговый файл</span><span class="sxs-lookup"><span data-stu-id="0fa15-936">tax file</span></span>
  
<span data-ttu-id="0fa15-937">Налоговый файл но.</span><span class="sxs-lookup"><span data-stu-id="0fa15-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0fa15-938">См. также</span><span class="sxs-lookup"><span data-stu-id="0fa15-938">See also</span></span>

[<span data-ttu-id="0fa15-939">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="0fa15-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

