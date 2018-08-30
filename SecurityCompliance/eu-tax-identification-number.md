---
title: Идентификационный номер налога ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении идентификационный номер налога ЕС тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534821"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="93c6f-104">Идентификационный номер налога ЕС</span><span class="sxs-lookup"><span data-stu-id="93c6f-104">EU Tax Identification Number</span></span>

<span data-ttu-id="93c6f-p102">В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных ЕС Tax код (TIN). Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="93c6f-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="93c6f-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="93c6f-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-108">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-108">Format</span></span>

<span data-ttu-id="93c6f-109">Девяти цифр с необязательным дефис и косой черты</span><span class="sxs-lookup"><span data-stu-id="93c6f-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-110">Pattern</span></span>

<span data-ttu-id="93c6f-111">Девять цифры с необязательным дефис и косой черты:</span><span class="sxs-lookup"><span data-stu-id="93c6f-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="93c6f-112">Две цифры</span><span class="sxs-lookup"><span data-stu-id="93c6f-112">Two digits</span></span> 
    
- <span data-ttu-id="93c6f-113">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="93c6f-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="93c6f-114">Три цифры</span><span class="sxs-lookup"><span data-stu-id="93c6f-114">Three digits</span></span>
    
- <span data-ttu-id="93c6f-115">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="93c6f-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="93c6f-116">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="93c6f-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-117">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-117">Checksum</span></span>

<span data-ttu-id="93c6f-118">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-119">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-119">Definition</span></span>

<span data-ttu-id="93c6f-120">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-121">Функция `Func_austria_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-122">Ключевое слово из `Keywords_austria_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-123">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-124">Функция `Func_austria_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-125">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="93c6f-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-127">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-127">tax number</span></span>
  
<span data-ttu-id="93c6f-128">номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-128">number</span></span>
  
<span data-ttu-id="93c6f-129">номер налогоплательщика</span><span class="sxs-lookup"><span data-stu-id="93c6f-129">tax registration number</span></span>
  
<span data-ttu-id="93c6f-130">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-130">tax id</span></span>
  
<span data-ttu-id="93c6f-131">ST.nr.</span><span class="sxs-lookup"><span data-stu-id="93c6f-131">st.nr.</span></span>
  
<span data-ttu-id="93c6f-132">steuernummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="93c6f-133">Бельгия</span><span class="sxs-lookup"><span data-stu-id="93c6f-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-134">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-134">Format</span></span>

<span data-ttu-id="93c6f-135">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-136">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-136">Pattern</span></span>

<span data-ttu-id="93c6f-137">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="93c6f-137">11 digits:</span></span>
  
- <span data-ttu-id="93c6f-138">Две цифры</span><span class="sxs-lookup"><span data-stu-id="93c6f-138">Two digits</span></span>
    
- <span data-ttu-id="93c6f-139">«0» или «1»</span><span class="sxs-lookup"><span data-stu-id="93c6f-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="93c6f-140">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="93c6f-140">One digit</span></span>
    
- <span data-ttu-id="93c6f-141">«0» или «1» или «2» или «3»</span><span class="sxs-lookup"><span data-stu-id="93c6f-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="93c6f-142">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-143">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-143">Checksum</span></span>

<span data-ttu-id="93c6f-144">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-145">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-145">Definition</span></span>

<span data-ttu-id="93c6f-146">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-147">Регулярное выражение `Regex_belgium_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-148">Ключевое слово из `Keywords_belgium_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="93c6f-149">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="93c6f-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-151">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-151">tax number</span></span>
  
<span data-ttu-id="93c6f-152">Национальный номер регистрации</span><span class="sxs-lookup"><span data-stu-id="93c6f-152">national registration number</span></span>
  
<span data-ttu-id="93c6f-153">номер налогоплательщика</span><span class="sxs-lookup"><span data-stu-id="93c6f-153">tax registration number</span></span>
  
<span data-ttu-id="93c6f-154">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-154">tax id</span></span>
  
<span data-ttu-id="93c6f-155">NIF</span><span class="sxs-lookup"><span data-stu-id="93c6f-155">nif</span></span>
  
<span data-ttu-id="93c6f-156">NIF #</span><span class="sxs-lookup"><span data-stu-id="93c6f-156">nif#</span></span>
  
<span data-ttu-id="93c6f-157">Национальный registre де numéro</span><span class="sxs-lookup"><span data-stu-id="93c6f-157">numéro de registre national</span></span>
  
<span data-ttu-id="93c6f-158">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="93c6f-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="93c6f-159">Болгария</span><span class="sxs-lookup"><span data-stu-id="93c6f-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-160">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-160">Format</span></span>

<span data-ttu-id="93c6f-161">10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-162">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-162">Pattern</span></span>

<span data-ttu-id="93c6f-163">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-164">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-164">Checksum</span></span>

<span data-ttu-id="93c6f-165">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-166">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-166">Definition</span></span>

<span data-ttu-id="93c6f-167">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-168">Функция `Func_bulgaria_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-169">Ключевое слово из `Keywords_bulgaria_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-170">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-171">Функция `Func_bulgaria_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-172">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="93c6f-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-174">bucn</span><span class="sxs-lookup"><span data-stu-id="93c6f-174">bucn</span></span>
  
<span data-ttu-id="93c6f-175">Универсальный правах номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-175">uniform civil number</span></span>
  
<span data-ttu-id="93c6f-176">bucn #</span><span class="sxs-lookup"><span data-stu-id="93c6f-176">bucn#</span></span>
  
<span data-ttu-id="93c6f-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="93c6f-178">универсальный идентификатор правах</span><span class="sxs-lookup"><span data-stu-id="93c6f-178">uniform civil id</span></span>
  
<span data-ttu-id="93c6f-179">Унифицированный правах no</span><span class="sxs-lookup"><span data-stu-id="93c6f-179">uniform civil no</span></span>
  
<span data-ttu-id="93c6f-180">egn</span><span class="sxs-lookup"><span data-stu-id="93c6f-180">egn</span></span>
  
<span data-ttu-id="93c6f-181">болгарский универсальный правах номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="93c6f-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-182">uniformcivilno#</span></span>
  
<span data-ttu-id="93c6f-183">egn #</span><span class="sxs-lookup"><span data-stu-id="93c6f-183">egn#</span></span>
  
<span data-ttu-id="93c6f-184">УНИФОРМ ГРАЖДАНСКИ НОМЕР</span><span class="sxs-lookup"><span data-stu-id="93c6f-184">униформ граждански номер</span></span>
  
<span data-ttu-id="93c6f-185">Идентификатор униформ</span><span class="sxs-lookup"><span data-stu-id="93c6f-185">униформ id</span></span>
  
<span data-ttu-id="93c6f-186">Идентификатор граждански униформ</span><span class="sxs-lookup"><span data-stu-id="93c6f-186">униформ граждански id</span></span>
  
<span data-ttu-id="93c6f-187">УНИФОРМ ГРАЖДАНСКИ НЕ</span><span class="sxs-lookup"><span data-stu-id="93c6f-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="93c6f-188">Хорватия</span><span class="sxs-lookup"><span data-stu-id="93c6f-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-189">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-189">Format</span></span>

<span data-ttu-id="93c6f-190">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-191">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-191">Pattern</span></span>

<span data-ttu-id="93c6f-192">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="93c6f-192">11 digits:</span></span>
  
- <span data-ttu-id="93c6f-193">10 цифр, случайным образом выбранные</span><span class="sxs-lookup"><span data-stu-id="93c6f-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="93c6f-194">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="93c6f-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-195">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-195">Checksum</span></span>

<span data-ttu-id="93c6f-196">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-197">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-197">Definition</span></span>

<span data-ttu-id="93c6f-198">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-199">Функция `Func_croatia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-200">Ключевое слово из `Keywords_croatia_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-201">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-202">Функция `Func_croatia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-203">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="93c6f-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-205">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-205">tax number</span></span>
  
<span data-ttu-id="93c6f-206">налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-206">tax</span></span>
  
<span data-ttu-id="93c6f-207">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-207">tax id</span></span>
  
<span data-ttu-id="93c6f-208">Идентификатор объекта</span><span class="sxs-lookup"><span data-stu-id="93c6f-208">oid</span></span>
  
<span data-ttu-id="93c6f-209">Идентификатор объекта #</span><span class="sxs-lookup"><span data-stu-id="93c6f-209">oid#</span></span>
  
<span data-ttu-id="93c6f-210">porezni broj</span><span class="sxs-lookup"><span data-stu-id="93c6f-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="93c6f-211">Кипр</span><span class="sxs-lookup"><span data-stu-id="93c6f-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-212">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-212">Format</span></span>

<span data-ttu-id="93c6f-213">Восемь цифр и одной буквы в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="93c6f-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-214">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-214">Pattern</span></span>

<span data-ttu-id="93c6f-215">Восемь цифр и одной буквы:</span><span class="sxs-lookup"><span data-stu-id="93c6f-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="93c6f-216">«0»</span><span class="sxs-lookup"><span data-stu-id="93c6f-216">A "0"</span></span> 
    
- <span data-ttu-id="93c6f-217">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="93c6f-217">Seven digits</span></span>
    
- <span data-ttu-id="93c6f-218">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-219">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-219">Checksum</span></span>

<span data-ttu-id="93c6f-220">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-221">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-221">Definition</span></span>

<span data-ttu-id="93c6f-222">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-223">Функция `Func_cyprus_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-224">Ключевое слово из `Keywords_cyprus_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-225">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-226">Функция `Func_cyprus_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-227">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="93c6f-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-229">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-229">tax number</span></span>
  
<span data-ttu-id="93c6f-230">налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-230">tax</span></span>
  
<span data-ttu-id="93c6f-231">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-231">tax id</span></span>
  
<span data-ttu-id="93c6f-232">Код налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-232">tax identification code</span></span>
  
<span data-ttu-id="93c6f-233">крестики</span><span class="sxs-lookup"><span data-stu-id="93c6f-233">tic</span></span>
  
<span data-ttu-id="93c6f-234">крестики #</span><span class="sxs-lookup"><span data-stu-id="93c6f-234">tic#</span></span>
  
<span data-ttu-id="93c6f-235">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="93c6f-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="93c6f-236">ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ</span><span class="sxs-lookup"><span data-stu-id="93c6f-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="93c6f-237">ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="93c6f-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="93c6f-238">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="93c6f-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-239">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-239">Format</span></span>

<span data-ttu-id="93c6f-240">9 или 10 цифр с необязательным обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="93c6f-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-241">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-241">Pattern</span></span>

<span data-ttu-id="93c6f-242">9 или 10 цифр с необязательным backslashl:</span><span class="sxs-lookup"><span data-stu-id="93c6f-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="93c6f-243">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-243">Six digits</span></span> 
    
- <span data-ttu-id="93c6f-244">Обратная косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="93c6f-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="93c6f-245">Три или четыре цифры</span><span class="sxs-lookup"><span data-stu-id="93c6f-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-246">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-246">Checksum</span></span>

<span data-ttu-id="93c6f-247">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-248">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-248">Definition</span></span>

<span data-ttu-id="93c6f-249">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-250">Регулярное выражение `Regex_czech_republic_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-251">Ключевое слово из `Keywords_czech_republic_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="93c6f-252">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="93c6f-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-254">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-254">tax number</span></span>
  
<span data-ttu-id="93c6f-255">налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-255">tax</span></span>
  
<span data-ttu-id="93c6f-256">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-256">tax id</span></span>
  
<span data-ttu-id="93c6f-257">личный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-257">personal number</span></span>
  
<span data-ttu-id="93c6f-258">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="93c6f-258">daňové číslo</span></span>
  
<span data-ttu-id="93c6f-259">osobní číslo</span><span class="sxs-lookup"><span data-stu-id="93c6f-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="93c6f-260">Дания</span><span class="sxs-lookup"><span data-stu-id="93c6f-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-261">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-261">Format</span></span>

<span data-ttu-id="93c6f-262">10 цифр, содержащий дефис</span><span class="sxs-lookup"><span data-stu-id="93c6f-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-263">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-263">Pattern</span></span>

<span data-ttu-id="93c6f-264">10 цифр, содержащий hyphenl:</span><span class="sxs-lookup"><span data-stu-id="93c6f-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="93c6f-265">Шести цифр, которые соответствуют Дата рождения (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="93c6f-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="93c6f-266">дефис;</span><span class="sxs-lookup"><span data-stu-id="93c6f-266">A hyphen</span></span>
    
- <span data-ttu-id="93c6f-267">Четыре цифры, которые соответствуют порядковый номер, где первая цифра соответствует века рождения и последней цифры соответствует Пол сотрудника (нечетной м и даже женщина)</span><span class="sxs-lookup"><span data-stu-id="93c6f-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-268">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-268">Checksum</span></span>

<span data-ttu-id="93c6f-269">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-270">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-270">Definition</span></span>

<span data-ttu-id="93c6f-271">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-272">Функция `Func_denmark_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-273">Ключевое слово из `Keywords_denmark_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-275">Функция `Func_denmark_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-276">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="93c6f-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-278">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-278">tax number</span></span>
  
<span data-ttu-id="93c6f-279">налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-279">tax</span></span>
  
<span data-ttu-id="93c6f-280">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-280">tax id</span></span>
  
<span data-ttu-id="93c6f-281">Номер CPR</span><span class="sxs-lookup"><span data-stu-id="93c6f-281">cpr number</span></span>
  
<span data-ttu-id="93c6f-282">CPR #</span><span class="sxs-lookup"><span data-stu-id="93c6f-282">cpr#</span></span>
  
<span data-ttu-id="93c6f-283">skat nummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-283">skat nummer</span></span>
  
<span data-ttu-id="93c6f-284">Идентификатор skat</span><span class="sxs-lookup"><span data-stu-id="93c6f-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="93c6f-285">Эстония</span><span class="sxs-lookup"><span data-stu-id="93c6f-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-286">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-286">Format</span></span>

<span data-ttu-id="93c6f-287">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-288">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-288">Pattern</span></span>

<span data-ttu-id="93c6f-289">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="93c6f-289">11 digits:</span></span>
  
-  <span data-ttu-id="93c6f-290">Одна цифра, соответствующий пол и века рождения где нечетным количеством указывает м, а четного числа женщина следующим образом: 1, 2 19 века; 3, 4 20 века; и 5, 6 для 21 веке</span><span class="sxs-lookup"><span data-stu-id="93c6f-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="93c6f-291">Шести цифр, которые соответствуют Дата рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="93c6f-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="93c6f-292">Три цифры, которые соответствуют серийный номер, отделяя лиц на тот же день рождения</span><span class="sxs-lookup"><span data-stu-id="93c6f-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="93c6f-293">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="93c6f-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-294">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-294">Checksum</span></span>

<span data-ttu-id="93c6f-295">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-296">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-296">Definition</span></span>

<span data-ttu-id="93c6f-297">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-298">Функция `Func_estonia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-299">Ключевое слово из `Keywords_estonia_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-300">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-301">Функция `Func_estonia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-302">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="93c6f-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-304">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-304">tax number</span></span>
  
<span data-ttu-id="93c6f-305">налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-305">tax</span></span>
  
<span data-ttu-id="93c6f-306">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-306">tax id</span></span>
  
<span data-ttu-id="93c6f-307">личный код</span><span class="sxs-lookup"><span data-stu-id="93c6f-307">personal code</span></span>
  
<span data-ttu-id="93c6f-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-308">maksunumber</span></span>
  
<span data-ttu-id="93c6f-309">Идентификатор maksu</span><span class="sxs-lookup"><span data-stu-id="93c6f-309">maksu id</span></span>
  
<span data-ttu-id="93c6f-310">isikukood</span><span class="sxs-lookup"><span data-stu-id="93c6f-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="93c6f-311">Финляндия</span><span class="sxs-lookup"><span data-stu-id="93c6f-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-312">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-312">Format</span></span>

<span data-ttu-id="93c6f-313">Комбинация 11 символов цифры, буквы, и плюс и минус</span><span class="sxs-lookup"><span data-stu-id="93c6f-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-314">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-314">Pattern</span></span>

<span data-ttu-id="93c6f-315">Комбинация 11 символов цифры, буквы, и плюс и минус:</span><span class="sxs-lookup"><span data-stu-id="93c6f-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="93c6f-316">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-316">Six digits</span></span>
    
- <span data-ttu-id="93c6f-317">Одно из следующих значений: знак плюс, минус или букву «» (не регистр), где значок "плюс" означает рождения между 1800-1899 вход "минус" означает, что рождения между 1900-1999 и «A» означает, что рождения 2000 и после</span><span class="sxs-lookup"><span data-stu-id="93c6f-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="93c6f-318">Три цифры</span><span class="sxs-lookup"><span data-stu-id="93c6f-318">Three digits</span></span>
    
- <span data-ttu-id="93c6f-319">Одна буква или один номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-320">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-320">Checksum</span></span>

<span data-ttu-id="93c6f-321">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-322">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-322">Definition</span></span>

<span data-ttu-id="93c6f-323">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-324">Функция `Func_finland_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-325">Ключевое слово из `Keywords_finland_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-326">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-327">Функция `Func_finland_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-328">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="93c6f-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-330">identification number
</span><span class="sxs-lookup"><span data-stu-id="93c6f-330">identification number</span></span>
  
<span data-ttu-id="93c6f-331">личный код</span><span class="sxs-lookup"><span data-stu-id="93c6f-331">personal id</span></span>
  
<span data-ttu-id="93c6f-332">Количество идентификаторов</span><span class="sxs-lookup"><span data-stu-id="93c6f-332">identity number</span></span>
  
<span data-ttu-id="93c6f-333">Национальный идентификатор для Финляндии номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-333">finnish national id number</span></span>
  
<span data-ttu-id="93c6f-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-334">personalidnumber#</span></span>
  
<span data-ttu-id="93c6f-335">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-335">national identification number</span></span>
  
<span data-ttu-id="93c6f-336">Табельный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-336">id number</span></span>
  
<span data-ttu-id="93c6f-337">Национальный идентификатор для не.</span><span class="sxs-lookup"><span data-stu-id="93c6f-337">national id no.</span></span>
  
<span data-ttu-id="93c6f-338">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-338">national id number</span></span>
  
<span data-ttu-id="93c6f-339">Идентификатор не</span><span class="sxs-lookup"><span data-stu-id="93c6f-339">id no</span></span>
  
<span data-ttu-id="93c6f-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="93c6f-340">tunnistenumero</span></span>
  
<span data-ttu-id="93c6f-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="93c6f-341">henkilötunnus</span></span>
  
<span data-ttu-id="93c6f-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="93c6f-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="93c6f-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="93c6f-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="93c6f-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="93c6f-344">identiteetti numero</span></span>
  
<span data-ttu-id="93c6f-345">suomen kansallinen henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="93c6f-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="93c6f-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="93c6f-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="93c6f-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="93c6f-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="93c6f-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="93c6f-348">tunnusnumero</span></span>
  
<span data-ttu-id="93c6f-349">kansallinen tunnus numero</span><span class="sxs-lookup"><span data-stu-id="93c6f-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="93c6f-350">Франция</span><span class="sxs-lookup"><span data-stu-id="93c6f-350">France</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-351">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-351">Format</span></span>

<span data-ttu-id="93c6f-352">13 цифр для отдельных пользователей и девяти цифр для сущностей</span><span class="sxs-lookup"><span data-stu-id="93c6f-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-353">Pattern</span></span>

<span data-ttu-id="93c6f-354">13 цифр для отдельных пользователей:</span><span class="sxs-lookup"><span data-stu-id="93c6f-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="93c6f-355">Одной цифры, которые должны быть 0, 1, 2 или 3</span><span class="sxs-lookup"><span data-stu-id="93c6f-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="93c6f-356">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-356">12 digits</span></span>
    
<span data-ttu-id="93c6f-357">Девяти цифр для сущностей</span><span class="sxs-lookup"><span data-stu-id="93c6f-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-358">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-358">Checksum</span></span>

<span data-ttu-id="93c6f-359">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-360">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-360">Definition</span></span>

<span data-ttu-id="93c6f-361">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-362">Функция `Func_france_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-363">Ключевое слово из `Keywords_france_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-365">Функция `Func_france_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-366">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="93c6f-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-368">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-368">tax identification number</span></span>
  
<span data-ttu-id="93c6f-369">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-369">tax number</span></span>
  
<span data-ttu-id="93c6f-370">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-370">tax id</span></span>
  
<span data-ttu-id="93c6f-371">numéro d'identification fiscale</span><span class="sxs-lookup"><span data-stu-id="93c6f-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="93c6f-372">Германия</span><span class="sxs-lookup"><span data-stu-id="93c6f-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-373">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-373">Format</span></span>

<span data-ttu-id="93c6f-374">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-375">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-375">Pattern</span></span>

<span data-ttu-id="93c6f-376">11 разрядов:</span><span class="sxs-lookup"><span data-stu-id="93c6f-376">11 digits :</span></span>
  
-  <span data-ttu-id="93c6f-377">10 цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-377">Ten digits</span></span> 
    
- <span data-ttu-id="93c6f-378">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="93c6f-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-379">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-379">Checksum</span></span>

<span data-ttu-id="93c6f-380">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-381">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-381">Definition</span></span>

<span data-ttu-id="93c6f-382">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-383">Функция `Func_germany_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-384">Ключевое слово из `Keywords_germany_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-385">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-386">Функция `Func_germany_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-387">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="93c6f-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-389">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-389">tax number</span></span>
  
<span data-ttu-id="93c6f-390">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-390">tax no.</span></span>
  
<span data-ttu-id="93c6f-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-391">taxno#</span></span>
  
<span data-ttu-id="93c6f-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-392">taxnumber#</span></span>
  
<span data-ttu-id="93c6f-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-393">taxnumber</span></span>
  
<span data-ttu-id="93c6f-394">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-394">tax id</span></span>
  
<span data-ttu-id="93c6f-395">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-395">taxid#</span></span>
  
<span data-ttu-id="93c6f-396">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-396">tax identification number</span></span>
  
<span data-ttu-id="93c6f-397">не налогах идентификации.</span><span class="sxs-lookup"><span data-stu-id="93c6f-397">tax identification no.</span></span>
  
<span data-ttu-id="93c6f-398">steuernummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-398">steuernummer</span></span>
  
<span data-ttu-id="93c6f-399">Идентификатор steuer</span><span class="sxs-lookup"><span data-stu-id="93c6f-399">steuer id</span></span>
  
<span data-ttu-id="93c6f-400">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="93c6f-401">Греция</span><span class="sxs-lookup"><span data-stu-id="93c6f-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-402">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-402">Format</span></span>

<span data-ttu-id="93c6f-403">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-404">Pattern</span></span>

<span data-ttu-id="93c6f-405">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-406">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-406">Checksum</span></span>

<span data-ttu-id="93c6f-407">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-408">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-408">Definition</span></span>

<span data-ttu-id="93c6f-409">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-410">Регулярное выражение `Regex_greece_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-411">Ключевое слово из `Keywords_greece_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="93c6f-412">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="93c6f-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-414">afm</span><span class="sxs-lookup"><span data-stu-id="93c6f-414">afm</span></span>
  
<span data-ttu-id="93c6f-415">tin
</span><span class="sxs-lookup"><span data-stu-id="93c6f-415">tin</span></span>
  
<span data-ttu-id="93c6f-416">не налогах идентификатор.</span><span class="sxs-lookup"><span data-stu-id="93c6f-416">tax id no.</span></span>
  
<span data-ttu-id="93c6f-417">не налогах идентификатор</span><span class="sxs-lookup"><span data-stu-id="93c6f-417">tax id no</span></span>
  
<span data-ttu-id="93c6f-418">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-418">tax identification number</span></span>
  
<span data-ttu-id="93c6f-419">Номер реестра налоговые</span><span class="sxs-lookup"><span data-stu-id="93c6f-419">tax registry number</span></span>
  
<span data-ttu-id="93c6f-420">не налогах реестра.</span><span class="sxs-lookup"><span data-stu-id="93c6f-420">tax registry no.</span></span>
  
<span data-ttu-id="93c6f-421">afm #</span><span class="sxs-lookup"><span data-stu-id="93c6f-421">afm#</span></span>
  
<span data-ttu-id="93c6f-422">TIN #</span><span class="sxs-lookup"><span data-stu-id="93c6f-422">tin#</span></span>
  
<span data-ttu-id="93c6f-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-423">taxidno#</span></span>
  
<span data-ttu-id="93c6f-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-424">taxregistryno#</span></span>
  
<span data-ttu-id="93c6f-425">ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="93c6f-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="93c6f-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="93c6f-426">aφμ</span></span>
  
<span data-ttu-id="93c6f-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="93c6f-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="93c6f-428">ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ ΝΟ.</span><span class="sxs-lookup"><span data-stu-id="93c6f-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="93c6f-429">ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ</span><span class="sxs-lookup"><span data-stu-id="93c6f-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="93c6f-430">Венгрия</span><span class="sxs-lookup"><span data-stu-id="93c6f-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-431">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-431">Format</span></span>

<span data-ttu-id="93c6f-432">10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-433">Pattern</span></span>

<span data-ttu-id="93c6f-434">Десять цифры:</span><span class="sxs-lookup"><span data-stu-id="93c6f-434">Ten digits:</span></span>
  
-  <span data-ttu-id="93c6f-435">Одной цифры, которые должны быть «8»</span><span class="sxs-lookup"><span data-stu-id="93c6f-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="93c6f-436">Пяти цифр, которые соответствуют число дней между датами 01/01/1867 и Дата рождения отдельных</span><span class="sxs-lookup"><span data-stu-id="93c6f-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="93c6f-437">Три цифры, которые соответствуют номер, который создается случайно для различения отдельных пользователей в тот же день рождения</span><span class="sxs-lookup"><span data-stu-id="93c6f-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="93c6f-438">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="93c6f-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-439">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-439">Checksum</span></span>

<span data-ttu-id="93c6f-440">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-441">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-441">Definition</span></span>

<span data-ttu-id="93c6f-442">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-443">Функция `Func_hungary_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-444">Ключевое слово из `Keywords_hungary_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-445">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-446">Функция `Func_hungary_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-447">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="93c6f-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-449">Венгерский tax идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="93c6f-450">Венгерский tin</span><span class="sxs-lookup"><span data-stu-id="93c6f-450">hungarian tin</span></span>
  
<span data-ttu-id="93c6f-451">номер идентификатора налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-451">tax id number</span></span>
  
<span data-ttu-id="93c6f-452">номер НДС</span><span class="sxs-lookup"><span data-stu-id="93c6f-452">vat number</span></span>
  
<span data-ttu-id="93c6f-453">не налогах центра сертификации</span><span class="sxs-lookup"><span data-stu-id="93c6f-453">tax authority no</span></span>
  
<span data-ttu-id="93c6f-454">Номер удостоверения tax идентификатора налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-454">tax id tax identity number</span></span>
  
<span data-ttu-id="93c6f-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-455">taxidnumber#</span></span>
  
<span data-ttu-id="93c6f-456">TIN #</span><span class="sxs-lookup"><span data-stu-id="93c6f-456">tin#</span></span>
  
<span data-ttu-id="93c6f-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="93c6f-457">hungatiantin#</span></span>
  
<span data-ttu-id="93c6f-458">не налогах идентификации</span><span class="sxs-lookup"><span data-stu-id="93c6f-458">tax identification no</span></span>
  
<span data-ttu-id="93c6f-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-459">taxidno#</span></span>
  
<span data-ttu-id="93c6f-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="93c6f-460">adóazonosító szám</span></span>
  
<span data-ttu-id="93c6f-461">adószám</span><span class="sxs-lookup"><span data-stu-id="93c6f-461">adószám</span></span>
  
<span data-ttu-id="93c6f-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="93c6f-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="93c6f-463">Ireland</span><span class="sxs-lookup"><span data-stu-id="93c6f-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-464">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-464">Format</span></span>

<span data-ttu-id="93c6f-465">Семь цифр, а затем буквы без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-466">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-466">Pattern</span></span>

<span data-ttu-id="93c6f-467">Семь цифр, а затем буквы:</span><span class="sxs-lookup"><span data-stu-id="93c6f-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="93c6f-468">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="93c6f-468">Seven digits</span></span> 
    
- <span data-ttu-id="93c6f-469">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-470">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-470">Checksum</span></span>

<span data-ttu-id="93c6f-471">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-472">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-472">Definition</span></span>

<span data-ttu-id="93c6f-473">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-474">Функция `Func_ireland_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-475">Ключевое слово из `Keywords_ireland_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-476">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-477">Функция `Func_ireland_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-478">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="93c6f-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-480">общего пользования нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-480">public service no</span></span>
  
<span data-ttu-id="93c6f-481">личные общего пользования нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-481">personal public service no</span></span>
  
<span data-ttu-id="93c6f-482">PPS нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-482">pps no</span></span>
  
<span data-ttu-id="93c6f-483">личные службы нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-483">personal service no</span></span>
  
<span data-ttu-id="93c6f-484">PPS-службы нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-484">pps service no</span></span>
  
<span data-ttu-id="93c6f-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-485">ppsno#</span></span>
  
<span data-ttu-id="93c6f-486">Ирландский pps нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-486">irish pps no</span></span>
  
<span data-ttu-id="93c6f-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-487">publicserviceno#</span></span>
  
<span data-ttu-id="93c6f-488">число личных общего пользования</span><span class="sxs-lookup"><span data-stu-id="93c6f-488">personal public service number</span></span>
  
<span data-ttu-id="93c6f-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="93c6f-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="93c6f-490">PPS uimh</span><span class="sxs-lookup"><span data-stu-id="93c6f-490">pps uimh</span></span>
  
<span data-ttu-id="93c6f-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="93c6f-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="93c6f-492">Италия</span><span class="sxs-lookup"><span data-stu-id="93c6f-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-493">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-493">Format</span></span>

<span data-ttu-id="93c6f-494">16 только буквы и цифры в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="93c6f-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-495">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-495">Pattern</span></span>

<span data-ttu-id="93c6f-496">16 только буквы и цифры:</span><span class="sxs-lookup"><span data-stu-id="93c6f-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="93c6f-497">Три буквы, которые соответствуют первым трем согласных в поле имя семейства</span><span class="sxs-lookup"><span data-stu-id="93c6f-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="93c6f-498">Три буквы, которые соответствуют первый, третий и четвертый согласных в поле имя</span><span class="sxs-lookup"><span data-stu-id="93c6f-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="93c6f-499">Две цифры, которые соответствуют к последнему цифры года рождения</span><span class="sxs-lookup"><span data-stu-id="93c6f-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="93c6f-500">Одна цифра, соответствующий месяц рождения — буквы используются в алфавитном порядке, но используются только буквы A E, H, L, M, P, R, чтобы T (таким образом, января-A и октября является R)</span><span class="sxs-lookup"><span data-stu-id="93c6f-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="93c6f-501">Две цифры, которые соответствуют день месяца рождения, где 40 добавляется в день рождения для женщин для различения мужчины</span><span class="sxs-lookup"><span data-stu-id="93c6f-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="93c6f-502">Четыре цифры, которые соответствуют код города, относящиеся к государственный орган, где рождения лица — коды всей страны, используемые для иностранных стран</span><span class="sxs-lookup"><span data-stu-id="93c6f-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="93c6f-503">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="93c6f-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-504">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-504">Checksum</span></span>

<span data-ttu-id="93c6f-505">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-506">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-506">Definition</span></span>

<span data-ttu-id="93c6f-507">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-508">Функция `Func_italy_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-509">Ключевое слово из `Keywords_italy_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-510">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-511">Функция `Func_italy_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-512">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="93c6f-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-514">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-514">tax number</span></span>
  
<span data-ttu-id="93c6f-515">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-515">tax no.</span></span>
  
<span data-ttu-id="93c6f-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-516">taxno#</span></span>
  
<span data-ttu-id="93c6f-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-517">taxnumber#</span></span>
  
<span data-ttu-id="93c6f-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-518">taxnumber</span></span>
  
<span data-ttu-id="93c6f-519">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-519">tax id</span></span>
  
<span data-ttu-id="93c6f-520">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-520">taxid#</span></span>
  
<span data-ttu-id="93c6f-521">Финансовый код</span><span class="sxs-lookup"><span data-stu-id="93c6f-521">fiscal code</span></span>
  
<span data-ttu-id="93c6f-522">codice fiscale</span><span class="sxs-lookup"><span data-stu-id="93c6f-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="93c6f-523">Латвия</span><span class="sxs-lookup"><span data-stu-id="93c6f-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-524">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-524">Format</span></span>

<span data-ttu-id="93c6f-525">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-526">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-526">Pattern</span></span>

<span data-ttu-id="93c6f-527">11 разрядов в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="93c6f-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="93c6f-528">Шести цифр, которые соответствуют Дата рождения (DDMMYY)</span><span class="sxs-lookup"><span data-stu-id="93c6f-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="93c6f-529">Одна цифра, соответствующий века рождения, которой соответствует 19 век «0», «1» соответствует 20 века, а «2» соответствует 21 веке</span><span class="sxs-lookup"><span data-stu-id="93c6f-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="93c6f-530">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="93c6f-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-531">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-531">Checksum</span></span>

<span data-ttu-id="93c6f-532">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-533">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-533">Definition</span></span>

<span data-ttu-id="93c6f-534">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-535">Функция `Func_latvia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-536">Ключевое слово из `Keywords_latvia_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-537">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-538">Функция `Func_latvia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-539">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="93c6f-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-541">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-541">tax number</span></span>
  
<span data-ttu-id="93c6f-542">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-542">tax no.</span></span>
  
<span data-ttu-id="93c6f-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-543">taxno#</span></span>
  
<span data-ttu-id="93c6f-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-544">taxnumber#</span></span>
  
<span data-ttu-id="93c6f-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-545">taxnumber</span></span>
  
<span data-ttu-id="93c6f-546">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-546">tax id</span></span>
  
<span data-ttu-id="93c6f-547">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-547">taxid#</span></span>
  
<span data-ttu-id="93c6f-548">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-548">tax identification number</span></span>
  
<span data-ttu-id="93c6f-549">не налогах идентификации.</span><span class="sxs-lookup"><span data-stu-id="93c6f-549">tax identification no.</span></span>
  
<span data-ttu-id="93c6f-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="93c6f-550">nodokļa numurs</span></span>
  
<span data-ttu-id="93c6f-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="93c6f-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="93c6f-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="93c6f-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="93c6f-553">Литва</span><span class="sxs-lookup"><span data-stu-id="93c6f-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-554">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-554">Format</span></span>

<span data-ttu-id="93c6f-555">11 знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-556">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-556">Pattern</span></span>

<span data-ttu-id="93c6f-557">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="93c6f-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-558">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-558">Checksum</span></span>

<span data-ttu-id="93c6f-559">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-560">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-560">Definition</span></span>

<span data-ttu-id="93c6f-561">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-562">Функция `Func_lithuania_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-563">Ключевое слово из `Keywords_lithuania_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-564">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-565">Функция `Func_lithuania_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-566">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="93c6f-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-568">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-568">tax number</span></span>
  
<span data-ttu-id="93c6f-569">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-569">tax no.</span></span>
  
<span data-ttu-id="93c6f-570">налогах нет #</span><span class="sxs-lookup"><span data-stu-id="93c6f-570">tax no#</span></span>
  
<span data-ttu-id="93c6f-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-571">taxnumber#</span></span>
  
<span data-ttu-id="93c6f-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-572">taxnumber</span></span>
  
<span data-ttu-id="93c6f-573">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-573">tax id</span></span>
  
<span data-ttu-id="93c6f-574">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-574">taxid#</span></span>
  
<span data-ttu-id="93c6f-575">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-575">tax identification number</span></span>
  
<span data-ttu-id="93c6f-576">не налогах идентификации.</span><span class="sxs-lookup"><span data-stu-id="93c6f-576">tax identification no.</span></span>
  
<span data-ttu-id="93c6f-577">Идентификатор mokesčių</span><span class="sxs-lookup"><span data-stu-id="93c6f-577">mokesčių id</span></span>
  
<span data-ttu-id="93c6f-578">mokesčių numeris</span><span class="sxs-lookup"><span data-stu-id="93c6f-578">mokesčių numeris</span></span>
  
<span data-ttu-id="93c6f-579">mokesčių identifikavimas numeris</span><span class="sxs-lookup"><span data-stu-id="93c6f-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="93c6f-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="93c6f-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-581">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-581">Format</span></span>

<span data-ttu-id="93c6f-582">13 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-583">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-583">Pattern</span></span>

<span data-ttu-id="93c6f-584">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="93c6f-584">13 digits:</span></span>
  
-  <span data-ttu-id="93c6f-585">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="93c6f-585">11 digits</span></span> 
    
- <span data-ttu-id="93c6f-586">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="93c6f-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-587">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-587">Checksum</span></span>

<span data-ttu-id="93c6f-588">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-589">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-589">Definition</span></span>

<span data-ttu-id="93c6f-590">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-591">Функция `Func_luxemburg_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-592">Ключевое слово из `Keywords_luxemburg_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-593">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-594">Функция `Func_luxemburg_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-595">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="93c6f-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-597">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-597">tax number</span></span>
  
<span data-ttu-id="93c6f-598">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-598">tax no.</span></span>
  
<span data-ttu-id="93c6f-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-599">taxno#</span></span>
  
<span data-ttu-id="93c6f-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-600">taxnumber#</span></span>
  
<span data-ttu-id="93c6f-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-601">taxnumber</span></span>
  
<span data-ttu-id="93c6f-602">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-602">tax id</span></span>
  
<span data-ttu-id="93c6f-603">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-603">taxid#</span></span>
  
<span data-ttu-id="93c6f-604">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-604">tax identification number</span></span>
  
<span data-ttu-id="93c6f-605">не налогах идентификации.</span><span class="sxs-lookup"><span data-stu-id="93c6f-605">tax identification no.</span></span>
  
<span data-ttu-id="93c6f-606">steuernummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-606">steuernummer</span></span>
  
<span data-ttu-id="93c6f-607">Идентификатор steuer</span><span class="sxs-lookup"><span data-stu-id="93c6f-607">steuer id</span></span>
  
<span data-ttu-id="93c6f-608">steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="93c6f-609">Мальта</span><span class="sxs-lookup"><span data-stu-id="93c6f-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-610">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-610">Format</span></span>

<span data-ttu-id="93c6f-611">Для Maltese представителями: 7 цифр и одной буквы в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="93c6f-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="93c6f-612">Не Мальтийский представителями и Maltese сущностей: 9 цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-613">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-613">Pattern</span></span>

<span data-ttu-id="93c6f-614">Maltese представителями: 7 цифр и одной буквы</span><span class="sxs-lookup"><span data-stu-id="93c6f-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="93c6f-615">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="93c6f-615">Seven digits</span></span> 
    
- <span data-ttu-id="93c6f-616">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="93c6f-617">Не Мальтийский представителями и Maltese сущностей: 9 цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="93c6f-618">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="93c6f-619">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-619">Checksum</span></span>

<span data-ttu-id="93c6f-620">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-621">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-621">Definition</span></span>

<span data-ttu-id="93c6f-622">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-623">Функция `Func_malta_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-624">Ключевое слово из `Keywords_malta_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-625">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-626">Функция `Func_malta_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-627">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="93c6f-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-629">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-629">tax number</span></span>
  
<span data-ttu-id="93c6f-630">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-630">tax no.</span></span>
  
<span data-ttu-id="93c6f-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-631">taxno#</span></span>
  
<span data-ttu-id="93c6f-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-632">taxnumber#</span></span>
  
<span data-ttu-id="93c6f-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-633">taxnumber</span></span>
  
<span data-ttu-id="93c6f-634">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-634">tax id</span></span>
  
<span data-ttu-id="93c6f-635">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-635">taxid#</span></span>
  
<span data-ttu-id="93c6f-636">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-636">tax identification number</span></span>
  
<span data-ttu-id="93c6f-637">не налогах идентификации.</span><span class="sxs-lookup"><span data-stu-id="93c6f-637">tax identification no.</span></span>
  
<span data-ttu-id="93c6f-638">numru tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="93c6f-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="93c6f-639">Идентификатор tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="93c6f-639">id tat-taxxa</span></span>
  
<span data-ttu-id="93c6f-640">numru ta "identifikazzjoni tat-taxxa</span><span class="sxs-lookup"><span data-stu-id="93c6f-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="93c6f-641">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="93c6f-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-642">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-642">Format</span></span>

<span data-ttu-id="93c6f-643">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-644">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-644">Pattern</span></span>

<span data-ttu-id="93c6f-645">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="93c6f-646">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-646">Checksum</span></span>

<span data-ttu-id="93c6f-647">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-648">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-648">Definition</span></span>

<span data-ttu-id="93c6f-649">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-650">Функция `Func_netherlands_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-651">Ключевое слово из `Keywords_netherlands_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-652">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-653">Функция `Func_netherlands_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-654">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="93c6f-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-656">Нидерландские tax идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="93c6f-657">Идентификация tax Нидерланды</span><span class="sxs-lookup"><span data-stu-id="93c6f-657">netherlands tax identification</span></span>
  
<span data-ttu-id="93c6f-658">Идентификационный номер абонента Нидерландские налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="93c6f-659">Идентификация tax Нидерландские абонента</span><span class="sxs-lookup"><span data-stu-id="93c6f-659">netherland's tax identification</span></span>
  
<span data-ttu-id="93c6f-660">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-660">tax identification number</span></span>
  
<span data-ttu-id="93c6f-661">Голландский ИД.</span><span class="sxs-lookup"><span data-stu-id="93c6f-661">dutch tax id</span></span>
  
<span data-ttu-id="93c6f-662">Голландский tax идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-662">dutch tax identification number</span></span>
  
<span data-ttu-id="93c6f-663">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-663">tax id</span></span>
  
<span data-ttu-id="93c6f-664">Идентификатор Tax #</span><span class="sxs-lookup"><span data-stu-id="93c6f-664">tax id#</span></span>
  
<span data-ttu-id="93c6f-665">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-665">tax number</span></span>
  
<span data-ttu-id="93c6f-666">налогах нет #</span><span class="sxs-lookup"><span data-stu-id="93c6f-666">tax no#</span></span>
  
<span data-ttu-id="93c6f-667">Tax #</span><span class="sxs-lookup"><span data-stu-id="93c6f-667">tax#</span></span>
  
<span data-ttu-id="93c6f-668">tin
</span><span class="sxs-lookup"><span data-stu-id="93c6f-668">tin</span></span>
  
<span data-ttu-id="93c6f-669">TIN #</span><span class="sxs-lookup"><span data-stu-id="93c6f-669">tin#</span></span>
  
<span data-ttu-id="93c6f-670">Нидерландские tin</span><span class="sxs-lookup"><span data-stu-id="93c6f-670">netherlands tin</span></span>
  
<span data-ttu-id="93c6f-671">Нидерландские 's tin</span><span class="sxs-lookup"><span data-stu-id="93c6f-671">netherland's tin</span></span>
  
<span data-ttu-id="93c6f-672">Nederlands belasting identificatienummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="93c6f-673">identificatienummer van belasting</span><span class="sxs-lookup"><span data-stu-id="93c6f-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="93c6f-674">identificatienummer belasting</span><span class="sxs-lookup"><span data-stu-id="93c6f-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="93c6f-675">Nederlands belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="93c6f-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="93c6f-676">Идентификатор nummer Nederlands belasting</span><span class="sxs-lookup"><span data-stu-id="93c6f-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="93c6f-677">Nederlands belastingnummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="93c6f-678">btw nummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-678">btw nummer</span></span>
  
<span data-ttu-id="93c6f-679">nederlandse belasting identificatie</span><span class="sxs-lookup"><span data-stu-id="93c6f-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="93c6f-680">Польша</span><span class="sxs-lookup"><span data-stu-id="93c6f-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-681">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-681">Format</span></span>

<span data-ttu-id="93c6f-682">Одиннадцать цифры без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-683">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-683">Pattern</span></span>

<span data-ttu-id="93c6f-684">Одиннадцать цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-685">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-685">Checksum</span></span>

<span data-ttu-id="93c6f-686">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-687">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-687">Definition</span></span>

<span data-ttu-id="93c6f-688">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-689">Функция `Func_poland_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-690">Ключевое слово из `Keywords_poland_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-691">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-692">Функция `Func_poland_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-693">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="93c6f-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-695">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-695">tax number</span></span>
  
<span data-ttu-id="93c6f-696">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-696">tax no.</span></span>
  
<span data-ttu-id="93c6f-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-697">taxno#</span></span>
  
<span data-ttu-id="93c6f-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-698">taxnumber#</span></span>
  
<span data-ttu-id="93c6f-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-699">taxnumber</span></span>
  
<span data-ttu-id="93c6f-700">ИНН</span><span class="sxs-lookup"><span data-stu-id="93c6f-700">nip</span></span>
  
<span data-ttu-id="93c6f-701">ИНН #</span><span class="sxs-lookup"><span data-stu-id="93c6f-701">nip#</span></span>
  
<span data-ttu-id="93c6f-702">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-702">tax id</span></span>
  
<span data-ttu-id="93c6f-703">Идентификатор Tax #</span><span class="sxs-lookup"><span data-stu-id="93c6f-703">tax id#</span></span>
  
<span data-ttu-id="93c6f-704">Идентификатор ИНН</span><span class="sxs-lookup"><span data-stu-id="93c6f-704">nip id</span></span>
  
<span data-ttu-id="93c6f-705">Идентификатор уще #</span><span class="sxs-lookup"><span data-stu-id="93c6f-705">nip id#</span></span>
  
<span data-ttu-id="93c6f-706">Идентификационный номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-706">tax identification number</span></span>
  
<span data-ttu-id="93c6f-707">не налогах идентификации.</span><span class="sxs-lookup"><span data-stu-id="93c6f-707">tax identification no.</span></span>
  
<span data-ttu-id="93c6f-708">номер НДС</span><span class="sxs-lookup"><span data-stu-id="93c6f-708">vat number</span></span>
  
<span data-ttu-id="93c6f-709">НДС нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-709">vat no.</span></span>
  
<span data-ttu-id="93c6f-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-710">vatno#</span></span>
  
<span data-ttu-id="93c6f-711">Идентификатор НДС</span><span class="sxs-lookup"><span data-stu-id="93c6f-711">vat id</span></span>
  
<span data-ttu-id="93c6f-712">Идентификатор НДС #</span><span class="sxs-lookup"><span data-stu-id="93c6f-712">vat id#</span></span>
  
<span data-ttu-id="93c6f-713">Номер identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="93c6f-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="93c6f-714">podatkowej identyfikacji polski номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="93c6f-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="93c6f-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="93c6f-716">Португалия</span><span class="sxs-lookup"><span data-stu-id="93c6f-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-717">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-717">Format</span></span>

<span data-ttu-id="93c6f-718">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-719">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-719">Pattern</span></span>

<span data-ttu-id="93c6f-720">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-721">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-721">Checksum</span></span>

<span data-ttu-id="93c6f-722">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-723">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-723">Definition</span></span>

<span data-ttu-id="93c6f-724">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-725">Функция `Func_portugal_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-726">Ключевое слово из `Keywords_portugal_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-727">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-728">Функция `Func_portugal_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-729">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="93c6f-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-731">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-731">tax number</span></span>
  
<span data-ttu-id="93c6f-732">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-732">tax no.</span></span>
  
<span data-ttu-id="93c6f-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-733">taxno#</span></span>
  
<span data-ttu-id="93c6f-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="93c6f-734">taxnumber#</span></span>
  
<span data-ttu-id="93c6f-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="93c6f-735">taxnumber</span></span>
  
<span data-ttu-id="93c6f-736">NIF</span><span class="sxs-lookup"><span data-stu-id="93c6f-736">nif</span></span>
  
<span data-ttu-id="93c6f-737">NIF #</span><span class="sxs-lookup"><span data-stu-id="93c6f-737">nif#</span></span>
  
<span data-ttu-id="93c6f-738">финансовые numero</span><span class="sxs-lookup"><span data-stu-id="93c6f-738">numero fiscal</span></span>
  
<span data-ttu-id="93c6f-739">финансовые identificação де número</span><span class="sxs-lookup"><span data-stu-id="93c6f-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="93c6f-740">Румыния</span><span class="sxs-lookup"><span data-stu-id="93c6f-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-741">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-741">Format</span></span>

<span data-ttu-id="93c6f-742">13 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-743">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-743">Pattern</span></span>

<span data-ttu-id="93c6f-744">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-745">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-745">Checksum</span></span>

<span data-ttu-id="93c6f-746">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-747">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-747">Definition</span></span>

<span data-ttu-id="93c6f-748">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-749">Регулярное выражение `Regex_romania_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-750">Ключевое слово из `Keywords_romania_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="93c6f-751">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="93c6f-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-753">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-753">tax id</span></span>
  
<span data-ttu-id="93c6f-754">номер идентификатора налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-754">tax id number</span></span>
  
<span data-ttu-id="93c6f-755">не налогах файла</span><span class="sxs-lookup"><span data-stu-id="93c6f-755">tax file no</span></span>
  
<span data-ttu-id="93c6f-756">

tax file number</span><span class="sxs-lookup"><span data-stu-id="93c6f-756">tax file number</span></span>
  
<span data-ttu-id="93c6f-757">налогах нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-757">tax no</span></span>
  
<span data-ttu-id="93c6f-758">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-758">tax number</span></span>
  
<span data-ttu-id="93c6f-759">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-759">taxid#</span></span>
  
<span data-ttu-id="93c6f-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-760">taxno#</span></span>
  
<span data-ttu-id="93c6f-761">Идентификатор ul taxei</span><span class="sxs-lookup"><span data-stu-id="93c6f-761">id-ul taxei</span></span>
  
<span data-ttu-id="93c6f-762">fiscală identificare де numărul</span><span class="sxs-lookup"><span data-stu-id="93c6f-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="93c6f-763">Словакия</span><span class="sxs-lookup"><span data-stu-id="93c6f-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-764">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-764">Format</span></span>

<span data-ttu-id="93c6f-765">10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-766">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-766">Pattern</span></span>

<span data-ttu-id="93c6f-767">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-768">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-768">Checksum</span></span>

<span data-ttu-id="93c6f-769">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="93c6f-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-770">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-770">Definition</span></span>

<span data-ttu-id="93c6f-771">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-772">Регулярное выражение `Regex_slovakia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-773">Ключевое слово из `Keywords_slovakia_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="93c6f-774">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="93c6f-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-776">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-776">tax id</span></span>
  
<span data-ttu-id="93c6f-777">номер идентификатора налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-777">tax id number</span></span>
  
<span data-ttu-id="93c6f-778">Идентификатор кода TIN</span><span class="sxs-lookup"><span data-stu-id="93c6f-778">tin id</span></span>
  
<span data-ttu-id="93c6f-779">Нет кода TIN</span><span class="sxs-lookup"><span data-stu-id="93c6f-779">tin no</span></span>
  
<span data-ttu-id="93c6f-780">Идентификатор кода tin словацкий</span><span class="sxs-lookup"><span data-stu-id="93c6f-780">slovakian tin id</span></span>
  
<span data-ttu-id="93c6f-781">tin
</span><span class="sxs-lookup"><span data-stu-id="93c6f-781">tin</span></span>
  
<span data-ttu-id="93c6f-782">не налогах файла</span><span class="sxs-lookup"><span data-stu-id="93c6f-782">tax file no</span></span>
  
<span data-ttu-id="93c6f-783">

tax file number</span><span class="sxs-lookup"><span data-stu-id="93c6f-783">tax file number</span></span>
  
<span data-ttu-id="93c6f-784">налогах нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-784">tax no</span></span>
  
<span data-ttu-id="93c6f-785">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-785">tax number</span></span>
  
<span data-ttu-id="93c6f-786">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-786">taxid#</span></span>
  
<span data-ttu-id="93c6f-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-787">taxno#</span></span>
  
<span data-ttu-id="93c6f-788">daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="93c6f-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="93c6f-789">daňové číslo</span><span class="sxs-lookup"><span data-stu-id="93c6f-789">daňové číslo</span></span>
  
<span data-ttu-id="93c6f-790">daňové číslo súboru</span><span class="sxs-lookup"><span data-stu-id="93c6f-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="93c6f-791">Словения</span><span class="sxs-lookup"><span data-stu-id="93c6f-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-792">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-792">Format</span></span>

<span data-ttu-id="93c6f-793">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-794">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-794">Pattern</span></span>

<span data-ttu-id="93c6f-795">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-796">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-796">Checksum</span></span>

<span data-ttu-id="93c6f-797">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-798">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-798">Definition</span></span>

<span data-ttu-id="93c6f-799">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-800">Функция `Func_slovenia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-801">Ключевое слово из `Keywords_slovenia_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-802">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-803">Функция `Func_slovenia_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-804">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="93c6f-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-806">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-806">tax id</span></span>
  
<span data-ttu-id="93c6f-807">номер идентификатора налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-807">tax id number</span></span>
  
<span data-ttu-id="93c6f-808">Идентификатор кода TIN</span><span class="sxs-lookup"><span data-stu-id="93c6f-808">tin id</span></span>
  
<span data-ttu-id="93c6f-809">Нет кода TIN</span><span class="sxs-lookup"><span data-stu-id="93c6f-809">tin no</span></span>
  
<span data-ttu-id="93c6f-810">Словенский кода tin идентификатор</span><span class="sxs-lookup"><span data-stu-id="93c6f-810">slovenian tin id</span></span>
  
<span data-ttu-id="93c6f-811">tin
</span><span class="sxs-lookup"><span data-stu-id="93c6f-811">tin</span></span>
  
<span data-ttu-id="93c6f-812">не налогах файла</span><span class="sxs-lookup"><span data-stu-id="93c6f-812">tax file no</span></span>
  
<span data-ttu-id="93c6f-813">

tax file number</span><span class="sxs-lookup"><span data-stu-id="93c6f-813">tax file number</span></span>
  
<span data-ttu-id="93c6f-814">налогах нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-814">tax no</span></span>
  
<span data-ttu-id="93c6f-815">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-815">tax number</span></span>
  
<span data-ttu-id="93c6f-816">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-816">taxid#</span></span>
  
<span data-ttu-id="93c6f-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-817">taxno#</span></span>
  
<span data-ttu-id="93c6f-818">identifikacijska številka davka</span><span class="sxs-lookup"><span data-stu-id="93c6f-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="93c6f-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="93c6f-819">davčna številka</span></span>
  
<span data-ttu-id="93c6f-820">Številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="93c6f-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="93c6f-821">Испания</span><span class="sxs-lookup"><span data-stu-id="93c6f-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-822">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-822">Format</span></span>

<span data-ttu-id="93c6f-823">Семь или восемь цифр и один или два буквы указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="93c6f-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-824">Pattern</span></span>

<span data-ttu-id="93c6f-825">Испанский физических лиц с Испания национальный личность:</span><span class="sxs-lookup"><span data-stu-id="93c6f-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="93c6f-826">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="93c6f-826">Eight digits</span></span> 
    
- <span data-ttu-id="93c6f-827">Один прописные буквы (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="93c6f-828">Без проживания Spaniards без Испания национальный личность</span><span class="sxs-lookup"><span data-stu-id="93c6f-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="93c6f-829">Один прописная буква «L» (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="93c6f-830">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="93c6f-830">Seven digits</span></span>
    
- <span data-ttu-id="93c6f-831">Один прописные буквы (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="93c6f-832">Встроенные Spaniards в разделе срок хранения в 14 лет без Испания национальный идентификатор карточки:</span><span class="sxs-lookup"><span data-stu-id="93c6f-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="93c6f-833">Один прописные буквы «K» (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="93c6f-834">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="93c6f-834">Seven digits</span></span> 
    
- <span data-ttu-id="93c6f-835">Один прописные буквы (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="93c6f-836">Foreigners с Foreigner идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="93c6f-837">То есть одно прописные буквы «X», «Y» или «Z» (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="93c6f-838">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="93c6f-838">Seven digits</span></span>
    
- <span data-ttu-id="93c6f-839">Один прописные буквы (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="93c6f-840">Foreigners без Foreigner идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="93c6f-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="93c6f-841">Один прописная буква, который является «M» (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="93c6f-842">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="93c6f-842">Seven digits</span></span>
    
- <span data-ttu-id="93c6f-843">Один прописные буквы (с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="93c6f-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="93c6f-844">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-844">Checksum</span></span>

<span data-ttu-id="93c6f-845">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-846">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-846">Definition</span></span>

<span data-ttu-id="93c6f-847">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-848">Функция `Func_spain_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-849">Ключевое слово из `Keywords_spain_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-850">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-851">Функция `Func_spain_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-852">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="93c6f-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-854">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-854">tax id</span></span>
  
<span data-ttu-id="93c6f-855">номер идентификатора налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-855">tax id number</span></span>
  
<span data-ttu-id="93c6f-856">Идентификатор CIF</span><span class="sxs-lookup"><span data-stu-id="93c6f-856">cif id</span></span>
  
<span data-ttu-id="93c6f-857">CIF нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-857">cif no</span></span>
  
<span data-ttu-id="93c6f-858">Идентификатор испанского cif</span><span class="sxs-lookup"><span data-stu-id="93c6f-858">spanish cif id</span></span>
  
<span data-ttu-id="93c6f-859">CIF</span><span class="sxs-lookup"><span data-stu-id="93c6f-859">cif</span></span>
  
<span data-ttu-id="93c6f-860">не налогах файла</span><span class="sxs-lookup"><span data-stu-id="93c6f-860">tax file no</span></span>
  
<span data-ttu-id="93c6f-861">Номер испанского cif</span><span class="sxs-lookup"><span data-stu-id="93c6f-861">spanish cif number</span></span>
  
<span data-ttu-id="93c6f-862">

tax file number</span><span class="sxs-lookup"><span data-stu-id="93c6f-862">tax file number</span></span>
  
<span data-ttu-id="93c6f-863">испанский cif нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-863">spanish cif no</span></span>
  
<span data-ttu-id="93c6f-864">налогах нет</span><span class="sxs-lookup"><span data-stu-id="93c6f-864">tax no</span></span>
  
<span data-ttu-id="93c6f-865">номер налога</span><span class="sxs-lookup"><span data-stu-id="93c6f-865">tax number</span></span>
  
<span data-ttu-id="93c6f-866">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-866">taxid#</span></span>
  
<span data-ttu-id="93c6f-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-867">taxno#</span></span>
  
<span data-ttu-id="93c6f-868">cifid #</span><span class="sxs-lookup"><span data-stu-id="93c6f-868">cifid#</span></span>
  
<span data-ttu-id="93c6f-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="93c6f-869">spanishcifid#</span></span>
  
<span data-ttu-id="93c6f-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="93c6f-870">spanishcifno#</span></span>
  
<span data-ttu-id="93c6f-871">contribuyente де número</span><span class="sxs-lookup"><span data-stu-id="93c6f-871">número de contribuyente</span></span>
  
<span data-ttu-id="93c6f-872">corporativo impuesto де número</span><span class="sxs-lookup"><span data-stu-id="93c6f-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="93c6f-873">финансовые identificación де número</span><span class="sxs-lookup"><span data-stu-id="93c6f-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="93c6f-874">CIF número</span><span class="sxs-lookup"><span data-stu-id="93c6f-874">cif número</span></span>
  
<span data-ttu-id="93c6f-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="93c6f-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="93c6f-876">Швеция</span><span class="sxs-lookup"><span data-stu-id="93c6f-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-877">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-877">Format</span></span>

<span data-ttu-id="93c6f-878">10 цифр и символ в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="93c6f-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-879">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-879">Pattern</span></span>

<span data-ttu-id="93c6f-880">10 цифр и символ:</span><span class="sxs-lookup"><span data-stu-id="93c6f-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="93c6f-881">Шести цифр, которые соответствуют Дата рождения (ГГММДД)</span><span class="sxs-lookup"><span data-stu-id="93c6f-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="93c6f-882">"Плюс", "минус" или обратная косая черта</span><span class="sxs-lookup"><span data-stu-id="93c6f-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="93c6f-883">Три цифры, которые делают идентификационный номер уникальный where:</span><span class="sxs-lookup"><span data-stu-id="93c6f-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="93c6f-884">Для номеров выдается, прежде чем 1990 цифры седьмой и восьмому идентификации район рождения или foreign-born людей</span><span class="sxs-lookup"><span data-stu-id="93c6f-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="93c6f-885">Цифра в девятого положение указывает пол, либо НЕЧЁТ для м или даже женщина</span><span class="sxs-lookup"><span data-stu-id="93c6f-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="93c6f-886">Один контрольный разряд</span><span class="sxs-lookup"><span data-stu-id="93c6f-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="93c6f-887">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-887">Checksum</span></span>

<span data-ttu-id="93c6f-888">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-889">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-889">Definition</span></span>

<span data-ttu-id="93c6f-890">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-891">Функция `Func_sweden_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-892">Ключевое слово из `Keywords_sweden_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="93c6f-893">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-894">Функция `Func_sweden_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
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

### <a name="keywords"></a><span data-ttu-id="93c6f-895">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="93c6f-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-897">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-897">tax id</span></span>
  
<span data-ttu-id="93c6f-898">не налогах идентификатор.</span><span class="sxs-lookup"><span data-stu-id="93c6f-898">tax id no.</span></span>
  
<span data-ttu-id="93c6f-899">номер идентификатора налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-899">tax id number</span></span>
  
<span data-ttu-id="93c6f-900">tax identification
</span><span class="sxs-lookup"><span data-stu-id="93c6f-900">tax identification</span></span>
  
<span data-ttu-id="93c6f-901">Идентификация Tax #</span><span class="sxs-lookup"><span data-stu-id="93c6f-901">tax identification#</span></span>
  
<span data-ttu-id="93c6f-902">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-902">tax no.</span></span>
  
<span data-ttu-id="93c6f-903">Tax #</span><span class="sxs-lookup"><span data-stu-id="93c6f-903">tax#</span></span>
  
<span data-ttu-id="93c6f-904">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-904">taxid#</span></span>
  
<span data-ttu-id="93c6f-905">файл налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-905">tax file</span></span>
  
<span data-ttu-id="93c6f-906">не налогах файла.</span><span class="sxs-lookup"><span data-stu-id="93c6f-906">tax file no.</span></span>
  
<span data-ttu-id="93c6f-907">личный идентификатор</span><span class="sxs-lookup"><span data-stu-id="93c6f-907">personal id number</span></span>
  
<span data-ttu-id="93c6f-908">Идентификатор nummer skatt</span><span class="sxs-lookup"><span data-stu-id="93c6f-908">skatt id nummer</span></span>
  
<span data-ttu-id="93c6f-909">skatt identifikation</span><span class="sxs-lookup"><span data-stu-id="93c6f-909">skatt identifikation</span></span>
  
<span data-ttu-id="93c6f-910">personnummer</span><span class="sxs-lookup"><span data-stu-id="93c6f-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="93c6f-911">(ВЕЛИКОБРИТАНИЯ)</span><span class="sxs-lookup"><span data-stu-id="93c6f-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="93c6f-912">Формат</span><span class="sxs-lookup"><span data-stu-id="93c6f-912">Format</span></span>

<span data-ttu-id="93c6f-913">Ссылка уникальный налогоплательщика (UTR): 10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="93c6f-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="93c6f-p103">Номер национальной страховых (НИНО): Для получения дополнительных сведений, обратитесь к разделу «Великобритания страховых национальный номер (НИНО)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="93c6f-p103">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="93c6f-916">Шаблон</span><span class="sxs-lookup"><span data-stu-id="93c6f-916">Pattern</span></span>

<span data-ttu-id="93c6f-917">Уникальной ссылки налогоплательщика (UTR): 10 цифр</span><span class="sxs-lookup"><span data-stu-id="93c6f-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="93c6f-p104">Номер национальной страховых (НИНО): Для получения дополнительных сведений, обратитесь к разделу «Великобритания страховых национальный номер (НИНО)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="93c6f-p104">National Insurance Number (NINO): For details, see the section "U.K. National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="93c6f-920">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="93c6f-920">Checksum</span></span>

<span data-ttu-id="93c6f-921">Да</span><span class="sxs-lookup"><span data-stu-id="93c6f-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="93c6f-922">Определение</span><span class="sxs-lookup"><span data-stu-id="93c6f-922">Definition</span></span>

<span data-ttu-id="93c6f-923">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="93c6f-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="93c6f-924">Функция `Func_uk_eu_tax_file_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="93c6f-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="93c6f-925">Ключевое слово из `Keywords_uk_eu_tax_file_number` найден.</span><span class="sxs-lookup"><span data-stu-id="93c6f-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="93c6f-926">Keywords</span><span class="sxs-lookup"><span data-stu-id="93c6f-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="93c6f-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="93c6f-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="93c6f-928">tax id
</span><span class="sxs-lookup"><span data-stu-id="93c6f-928">tax id</span></span>
  
<span data-ttu-id="93c6f-929">не налогах идентификатор.</span><span class="sxs-lookup"><span data-stu-id="93c6f-929">tax id no.</span></span>
  
<span data-ttu-id="93c6f-930">номер идентификатора налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-930">tax id number</span></span>
  
<span data-ttu-id="93c6f-931">tax identification
</span><span class="sxs-lookup"><span data-stu-id="93c6f-931">tax identification</span></span>
  
<span data-ttu-id="93c6f-932">Идентификация Tax #</span><span class="sxs-lookup"><span data-stu-id="93c6f-932">tax identification#</span></span>
  
<span data-ttu-id="93c6f-933">налогах нет.</span><span class="sxs-lookup"><span data-stu-id="93c6f-933">tax no.</span></span>
  
<span data-ttu-id="93c6f-934">Tax #</span><span class="sxs-lookup"><span data-stu-id="93c6f-934">tax#</span></span>
  
<span data-ttu-id="93c6f-935">код налогоплательщика #</span><span class="sxs-lookup"><span data-stu-id="93c6f-935">taxid#</span></span>
  
<span data-ttu-id="93c6f-936">файл налогах</span><span class="sxs-lookup"><span data-stu-id="93c6f-936">tax file</span></span>
  
<span data-ttu-id="93c6f-937">не налогах файла.</span><span class="sxs-lookup"><span data-stu-id="93c6f-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="93c6f-938">См. также</span><span class="sxs-lookup"><span data-stu-id="93c6f-938">See also</span></span>

[<span data-ttu-id="93c6f-939">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="93c6f-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

