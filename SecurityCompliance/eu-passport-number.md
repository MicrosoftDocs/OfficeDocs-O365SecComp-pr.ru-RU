---
title: Номер паспорта ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении номер паспорта ЕС тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 71acc39b885c057e1771ec13b2f3c25017ac1bb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534931"
---
# <a name="eu-passport-number"></a><span data-ttu-id="087f8-104">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="087f8-104">EU Passport Number</span></span>

<span data-ttu-id="087f8-p102">В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении номер паспорта ЕС тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="087f8-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="087f8-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="087f8-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="087f8-108">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-108">Format</span></span>

<span data-ttu-id="087f8-109">Один буквы, необязательное поле и семь цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-110">Pattern</span></span>

<span data-ttu-id="087f8-111">Сочетание одной буквы, семь цифр и один пробел:</span><span class="sxs-lookup"><span data-stu-id="087f8-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="087f8-112">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="087f8-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="087f8-113">Один пробел (необязательно)</span><span class="sxs-lookup"><span data-stu-id="087f8-113">One space (optional)</span></span>
    
- <span data-ttu-id="087f8-114">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="087f8-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-115">Checksum</span></span>

<span data-ttu-id="087f8-116">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="087f8-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-117">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-117">Definition</span></span>

<span data-ttu-id="087f8-118">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-119">Регулярное выражение `Regex_austria_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-120">Ключевое слово из `Keywords_austria_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-121">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-121">Keywords</span></span>

<span data-ttu-id="087f8-122">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-122"></span></span>
|<span data-ttu-id="087f8-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-124">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-124">passport number</span></span>  <br/> <span data-ttu-id="087f8-125">Номер паспорта Австрия</span><span class="sxs-lookup"><span data-stu-id="087f8-125">austrian passport number</span></span>  <br/> <span data-ttu-id="087f8-126">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-126">passport no</span></span>  <br/> <span data-ttu-id="087f8-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="087f8-127">reisepass</span></span>  <br/> <span data-ttu-id="087f8-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="087f8-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="087f8-129">Бельгия</span><span class="sxs-lookup"><span data-stu-id="087f8-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="087f8-130">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-130">Format</span></span>

<span data-ttu-id="087f8-131">Две буквы, а затем шести цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-132">Pattern</span></span>

<span data-ttu-id="087f8-133">Две буквы и следуют шести цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-134">Checksum</span></span>

<span data-ttu-id="087f8-135">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="087f8-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-136">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-136">Definition</span></span>

<span data-ttu-id="087f8-137">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-138">Регулярное выражение `Regex_belgium_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-139">Ключевое слово из `Keywords_belgium_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-140">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-140">Keywords</span></span>

<span data-ttu-id="087f8-141">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-141"></span></span>
|<span data-ttu-id="087f8-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-143">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-143">passport number</span></span>  <br/> <span data-ttu-id="087f8-144">Номер паспорта Бельгия</span><span class="sxs-lookup"><span data-stu-id="087f8-144">belgian passport number</span></span>  <br/> <span data-ttu-id="087f8-145">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-145">passport no</span></span>  <br/> <span data-ttu-id="087f8-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="087f8-146">paspoort</span></span>  <br/> <span data-ttu-id="087f8-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="087f8-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="087f8-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="087f8-148">reisepass kein</span></span>  <br/> <span data-ttu-id="087f8-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="087f8-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="087f8-150">Болгария</span><span class="sxs-lookup"><span data-stu-id="087f8-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="087f8-151">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-151">Format</span></span>

<span data-ttu-id="087f8-152">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-153">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-153">Pattern</span></span>

 <span data-ttu-id="087f8-154">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="087f8-155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-155">Checksum</span></span>

<span data-ttu-id="087f8-156">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-157">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-157">Definition</span></span>

<span data-ttu-id="087f8-158">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-159">Регулярное выражение `Regex_bulgaria_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-160">Ключевое слово из `Keywords_bulgaria_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-161">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-161">Keywords</span></span>

<span data-ttu-id="087f8-162">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-162"></span></span>
|<span data-ttu-id="087f8-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-164">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-164">passport number</span></span>  <br/> <span data-ttu-id="087f8-165">Номер паспорта болгарский</span><span class="sxs-lookup"><span data-stu-id="087f8-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="087f8-166">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-166">passport no</span></span>  <br/> <span data-ttu-id="087f8-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="087f8-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="087f8-168">Хорватия</span><span class="sxs-lookup"><span data-stu-id="087f8-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="087f8-169">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-169">Format</span></span>

<span data-ttu-id="087f8-170">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-171">Pattern</span></span>

 <span data-ttu-id="087f8-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="087f8-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-173">Checksum</span></span>

<span data-ttu-id="087f8-174">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-175">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-175">Definition</span></span>

<span data-ttu-id="087f8-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-177">Регулярное выражение `Regex_croatia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-178">Ключевое слово из `Keywords_croatia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-179">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-179">Keywords</span></span>

<span data-ttu-id="087f8-180">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-180"></span></span>
|<span data-ttu-id="087f8-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-182">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-182">passport number</span></span>  <br/> <span data-ttu-id="087f8-183">Номер паспорта Хорватский</span><span class="sxs-lookup"><span data-stu-id="087f8-183">croatian passport number</span></span>  <br/> <span data-ttu-id="087f8-184">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-184">passport no</span></span>  <br/> <span data-ttu-id="087f8-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="087f8-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="087f8-186">Кипр</span><span class="sxs-lookup"><span data-stu-id="087f8-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="087f8-187">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-187">Format</span></span>

<span data-ttu-id="087f8-188">Один буквы, цифры 6-8 без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-189">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-189">Pattern</span></span>

<span data-ttu-id="087f8-190">Один буквы, цифры 6-8</span><span class="sxs-lookup"><span data-stu-id="087f8-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-191">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-191">Checksum</span></span>

<span data-ttu-id="087f8-192">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-193">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-193">Definition</span></span>

<span data-ttu-id="087f8-194">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-195">Регулярное выражение `Regex_cyprus_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-196">Ключевое слово из `Keywords_cyprus_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-197">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-197">Keywords</span></span>

<span data-ttu-id="087f8-198">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-198"></span></span>
|<span data-ttu-id="087f8-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-200">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-200">passport number</span></span>  <br/> <span data-ttu-id="087f8-201">Номер паспорта Кипр</span><span class="sxs-lookup"><span data-stu-id="087f8-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="087f8-202">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-202">passport no</span></span>  <br/> <span data-ttu-id="087f8-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="087f8-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="087f8-204">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="087f8-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="087f8-205">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-205">Format</span></span>

<span data-ttu-id="087f8-206">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-207">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-207">Pattern</span></span>

<span data-ttu-id="087f8-208">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-209">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-209">Checksum</span></span>

<span data-ttu-id="087f8-210">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-211">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-211">Definition</span></span>

<span data-ttu-id="087f8-212">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-213">Регулярное выражение `Regex_czech_republic_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-214">Ключевое слово из `Keywords_czech_republic_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-215">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-215">Keywords</span></span>

<span data-ttu-id="087f8-216">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-216"></span></span>
|<span data-ttu-id="087f8-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-218">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-218">passport number</span></span>  <br/> <span data-ttu-id="087f8-219">Номер паспорта чешский</span><span class="sxs-lookup"><span data-stu-id="087f8-219">czech passport number</span></span>  <br/> <span data-ttu-id="087f8-220">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-220">passport no</span></span>  <br/> <span data-ttu-id="087f8-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="087f8-221">cestovní pas</span></span>  <br/> <span data-ttu-id="087f8-222">PAS</span><span class="sxs-lookup"><span data-stu-id="087f8-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="087f8-223">Дания</span><span class="sxs-lookup"><span data-stu-id="087f8-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="087f8-224">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-224">Format</span></span>

<span data-ttu-id="087f8-225">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-226">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-226">Pattern</span></span>

 <span data-ttu-id="087f8-227">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="087f8-228">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-228">Checksum</span></span>

<span data-ttu-id="087f8-229">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-230">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-230">Definition</span></span>

<span data-ttu-id="087f8-231">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-232">Регулярное выражение `Regex_denmark_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-233">Ключевое слово из `Keywords_denmark_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-234">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-234">Keywords</span></span>

<span data-ttu-id="087f8-235">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-235"></span></span>
|<span data-ttu-id="087f8-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-237">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-237">passport number</span></span>  <br/> <span data-ttu-id="087f8-238">Номер паспорта датский</span><span class="sxs-lookup"><span data-stu-id="087f8-238">danish passport number</span></span>  <br/> <span data-ttu-id="087f8-239">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-239">passport no</span></span>  <br/> <span data-ttu-id="087f8-240">PAS</span><span class="sxs-lookup"><span data-stu-id="087f8-240">pas</span></span>  <br/> <span data-ttu-id="087f8-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="087f8-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="087f8-242">Эстония</span><span class="sxs-lookup"><span data-stu-id="087f8-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="087f8-243">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-243">Format</span></span>

<span data-ttu-id="087f8-244">Один буквы, семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-245">Pattern</span></span>

<span data-ttu-id="087f8-246">Один буквы, семь цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-247">Checksum</span></span>

<span data-ttu-id="087f8-248">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-249">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-249">Definition</span></span>

<span data-ttu-id="087f8-250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-251">Регулярное выражение `Regex_estonia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-252">Ключевое слово из `Keywords_estonia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-253">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-253">Keywords</span></span>

<span data-ttu-id="087f8-254">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-254"></span></span>
|<span data-ttu-id="087f8-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-256">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-256">passport number</span></span>  <br/> <span data-ttu-id="087f8-257">Номер паспорта эстонский</span><span class="sxs-lookup"><span data-stu-id="087f8-257">estonian passport number</span></span>  <br/> <span data-ttu-id="087f8-258">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-258">passport no</span></span>  <br/> <span data-ttu-id="087f8-259">этап kodaniku eesti</span><span class="sxs-lookup"><span data-stu-id="087f8-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="087f8-260">Финляндия</span><span class="sxs-lookup"><span data-stu-id="087f8-260">Finland</span></span>

<span data-ttu-id="087f8-261">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Финляндия» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="087f8-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="087f8-262">Франция</span><span class="sxs-lookup"><span data-stu-id="087f8-262">France</span></span>

<span data-ttu-id="087f8-263">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Гражданина Франции» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="087f8-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="087f8-264">Германия</span><span class="sxs-lookup"><span data-stu-id="087f8-264">Germany</span></span>

<span data-ttu-id="087f8-265">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Германия» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="087f8-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="087f8-266">Греция</span><span class="sxs-lookup"><span data-stu-id="087f8-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="087f8-267">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-267">Format</span></span>

<span data-ttu-id="087f8-268">Две буквы, затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-269">Pattern</span></span>

<span data-ttu-id="087f8-270">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-271">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-271">Checksum</span></span>

<span data-ttu-id="087f8-272">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-273">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-273">Definition</span></span>

<span data-ttu-id="087f8-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-275">Регулярное выражение `Regex_greece_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-276">Ключевое слово из `Keywords_greece_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-277">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-277">Keywords</span></span>

<span data-ttu-id="087f8-278">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-278"></span></span>
|<span data-ttu-id="087f8-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-280">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-280">passport number</span></span>  <br/> <span data-ttu-id="087f8-281">Номер паспорта греческий</span><span class="sxs-lookup"><span data-stu-id="087f8-281">greek passport number</span></span>  <br/> <span data-ttu-id="087f8-282">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-282">passport no</span></span>  <br/> <span data-ttu-id="087f8-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="087f8-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="087f8-284">Венгрия</span><span class="sxs-lookup"><span data-stu-id="087f8-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="087f8-285">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-285">Format</span></span>

<span data-ttu-id="087f8-286">Две буквы, затем шесть или семь цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-287">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-287">Pattern</span></span>

<span data-ttu-id="087f8-288">Две буквы, затем шесть или семь цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-289">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-289">Checksum</span></span>

<span data-ttu-id="087f8-290">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-291">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-291">Definition</span></span>

<span data-ttu-id="087f8-292">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-293">Регулярное выражение `Regex_hungary_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-294">Ключевое слово из `Keywords_hungary_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-295">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-295">Keywords</span></span>

<span data-ttu-id="087f8-296">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-296"></span></span>
|<span data-ttu-id="087f8-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-298">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-298">passport number</span></span>  <br/> <span data-ttu-id="087f8-299">Номер паспорта венгерский</span><span class="sxs-lookup"><span data-stu-id="087f8-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="087f8-300">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-300">passport no</span></span>  <br/> <span data-ttu-id="087f8-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="087f8-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="087f8-302">Ireland</span><span class="sxs-lookup"><span data-stu-id="087f8-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="087f8-303">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-303">Format</span></span>

<span data-ttu-id="087f8-304">Два букв или цифр, а затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-305">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-305">Pattern</span></span>

<span data-ttu-id="087f8-306">Два букв или цифр, а затем семь цифр:</span><span class="sxs-lookup"><span data-stu-id="087f8-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="087f8-307">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="087f8-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="087f8-308">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="087f8-309">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-309">Checksum</span></span>

<span data-ttu-id="087f8-310">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-311">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-311">Definition</span></span>

<span data-ttu-id="087f8-312">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-313">Регулярное выражение `Regex_ireland_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-314">Ключевое слово из `Keywords_ireland_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-315">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-315">Keywords</span></span>

<span data-ttu-id="087f8-316">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-316"></span></span>
|<span data-ttu-id="087f8-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-318">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-318">passport number</span></span>  <br/> <span data-ttu-id="087f8-319">Номер паспорта Ирландский</span><span class="sxs-lookup"><span data-stu-id="087f8-319">irish passport number</span></span>  <br/> <span data-ttu-id="087f8-320">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-320">passport no</span></span>  <br/> <span data-ttu-id="087f8-321">PAS</span><span class="sxs-lookup"><span data-stu-id="087f8-321">pas</span></span>  <br/> <span data-ttu-id="087f8-322">passport</span><span class="sxs-lookup"><span data-stu-id="087f8-322">passport</span></span>  <br/> <span data-ttu-id="087f8-323">passeport</span><span class="sxs-lookup"><span data-stu-id="087f8-323">passeport</span></span>  <br/> <span data-ttu-id="087f8-324">passeport numero</span><span class="sxs-lookup"><span data-stu-id="087f8-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="087f8-325">Италия</span><span class="sxs-lookup"><span data-stu-id="087f8-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="087f8-326">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-326">Format</span></span>

<span data-ttu-id="087f8-327">Два букв или цифр, а затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-328">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-328">Pattern</span></span>

<span data-ttu-id="087f8-329">Два букв или цифр, а затем семь цифр:</span><span class="sxs-lookup"><span data-stu-id="087f8-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="087f8-330">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="087f8-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="087f8-331">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="087f8-332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-332">Checksum</span></span>

<span data-ttu-id="087f8-333">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="087f8-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-334">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-334">Definition</span></span>

<span data-ttu-id="087f8-335">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-336">Регулярное выражение `Regex_italy_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-337">Ключевое слово из `Keywords_italy_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-338">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-338">Keywords</span></span>

<span data-ttu-id="087f8-339">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-339"></span></span>
|<span data-ttu-id="087f8-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-341">Номер паспорта итальянский</span><span class="sxs-lookup"><span data-stu-id="087f8-341">italian passport number</span></span>  <br/> <span data-ttu-id="087f8-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="087f8-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="087f8-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="087f8-343">passaporto</span></span>  <br/> <span data-ttu-id="087f8-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="087f8-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="087f8-345">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-345">passport number</span></span>  <br/> <span data-ttu-id="087f8-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="087f8-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="087f8-347">passaporto numero</span><span class="sxs-lookup"><span data-stu-id="087f8-347">passaporto numero</span></span>  <br/> <span data-ttu-id="087f8-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="087f8-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="087f8-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="087f8-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="087f8-350">Латвия</span><span class="sxs-lookup"><span data-stu-id="087f8-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="087f8-351">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-351">Format</span></span>

<span data-ttu-id="087f8-352">Два букв или цифр, а затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-353">Pattern</span></span>

<span data-ttu-id="087f8-354">Два букв или цифр, а затем семь цифр:</span><span class="sxs-lookup"><span data-stu-id="087f8-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="087f8-355">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="087f8-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="087f8-356">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="087f8-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-357">Checksum</span></span>

<span data-ttu-id="087f8-358">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-359">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-359">Definition</span></span>

<span data-ttu-id="087f8-360">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-361">Регулярное выражение `Regex_latvia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-362">Ключевое слово из `Keywords_latvia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-363">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-363">Keywords</span></span>

<span data-ttu-id="087f8-364">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-364"></span></span>
|<span data-ttu-id="087f8-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-366">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-366">passport number</span></span>  <br/> <span data-ttu-id="087f8-367">Номер паспорта латышский</span><span class="sxs-lookup"><span data-stu-id="087f8-367">latvian passport number</span></span>  <br/> <span data-ttu-id="087f8-368">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-368">passport no</span></span>  <br/> <span data-ttu-id="087f8-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="087f8-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="087f8-370">Литва</span><span class="sxs-lookup"><span data-stu-id="087f8-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="087f8-371">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-371">Format</span></span>

<span data-ttu-id="087f8-372">Восемь цифр или символов без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-373">Pattern</span></span>

<span data-ttu-id="087f8-374">Восемь цифр или символов (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="087f8-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-375">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-375">Checksum</span></span>

<span data-ttu-id="087f8-376">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="087f8-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-377">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-377">Definition</span></span>

<span data-ttu-id="087f8-378">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-379">Регулярное выражение `Regex_lithuania_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-380">Ключевое слово из `Keywords_lithuania_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-381">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-381">Keywords</span></span>

<span data-ttu-id="087f8-382">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-382"></span></span>
|<span data-ttu-id="087f8-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-384">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-384">passport number</span></span>  <br/> <span data-ttu-id="087f8-385">Номер паспорта lithunian</span><span class="sxs-lookup"><span data-stu-id="087f8-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="087f8-386">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-386">passport no</span></span>  <br/> <span data-ttu-id="087f8-387">paso numeris</span><span class="sxs-lookup"><span data-stu-id="087f8-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="087f8-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="087f8-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="087f8-389">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-389">Format</span></span>

<span data-ttu-id="087f8-390">Восемь цифр или символов без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-391">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-391">Pattern</span></span>

<span data-ttu-id="087f8-392">Восемь цифр или символов (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="087f8-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-393">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-393">Checksum</span></span>

<span data-ttu-id="087f8-394">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-395">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-395">Definition</span></span>

<span data-ttu-id="087f8-396">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-397">Регулярное выражение `Regex_nation_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-398">Ключевое слово из `Keywords_nation_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-399">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-399">Keywords</span></span>

<span data-ttu-id="087f8-400">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-400"></span></span>
|<span data-ttu-id="087f8-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-402">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-402">passport number</span></span>  <br/> <span data-ttu-id="087f8-403">Номер паспорта латышский</span><span class="sxs-lookup"><span data-stu-id="087f8-403">latvian passport number</span></span>  <br/> <span data-ttu-id="087f8-404">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-404">passport no</span></span>  <br/> <span data-ttu-id="087f8-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="087f8-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="087f8-406">Мальта</span><span class="sxs-lookup"><span data-stu-id="087f8-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="087f8-407">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-407">Format</span></span>

<span data-ttu-id="087f8-408">Семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-409">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-409">Pattern</span></span>

 <span data-ttu-id="087f8-410">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="087f8-411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-411">Checksum</span></span>

<span data-ttu-id="087f8-412">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-413">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-413">Definition</span></span>

<span data-ttu-id="087f8-414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-415">Регулярное выражение `Regex_malta_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-416">Ключевое слово из `Keywords_malta_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-417">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-417">Keywords</span></span>

<span data-ttu-id="087f8-418">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-418"></span></span>
|<span data-ttu-id="087f8-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-420">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-420">passport number</span></span>  <br/> <span data-ttu-id="087f8-421">Номер паспорта maltese</span><span class="sxs-lookup"><span data-stu-id="087f8-421">maltese passport number</span></span>  <br/> <span data-ttu-id="087f8-422">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-422">passport no</span></span>  <br/> <span data-ttu-id="087f8-423">всего numru-passaport</span><span class="sxs-lookup"><span data-stu-id="087f8-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="087f8-424">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="087f8-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="087f8-425">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-425">Format</span></span>

<span data-ttu-id="087f8-426">Девять букв или цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-427">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-427">Pattern</span></span>

<span data-ttu-id="087f8-428">Девять букв или цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-429">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-429">Checksum</span></span>

<span data-ttu-id="087f8-430">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="087f8-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-431">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-431">Definition</span></span>

<span data-ttu-id="087f8-432">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-433">Регулярное выражение `Regex_netherlands_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-434">Ключевое слово из `Keywords_netherlands_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-435">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-435">Keywords</span></span>

<span data-ttu-id="087f8-436">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-436"></span></span>
|<span data-ttu-id="087f8-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-438">Номер паспорта голландский</span><span class="sxs-lookup"><span data-stu-id="087f8-438">dutch passport number</span></span>  <br/> <span data-ttu-id="087f8-439">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-439">passport number</span></span>  <br/> <span data-ttu-id="087f8-440">Номер паспорта Нидерланды</span><span class="sxs-lookup"><span data-stu-id="087f8-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="087f8-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="087f8-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="087f8-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="087f8-442">paspoort</span></span>  <br/> <span data-ttu-id="087f8-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="087f8-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="087f8-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="087f8-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="087f8-445">Польша</span><span class="sxs-lookup"><span data-stu-id="087f8-445">Poland</span></span>

<span data-ttu-id="087f8-446">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта для Польши» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="087f8-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="087f8-447">Португалия</span><span class="sxs-lookup"><span data-stu-id="087f8-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="087f8-448">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-448">Format</span></span>

<span data-ttu-id="087f8-449">Один буквы, шести цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-450">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-450">Pattern</span></span>

<span data-ttu-id="087f8-451">Один буквы шести цифр:</span><span class="sxs-lookup"><span data-stu-id="087f8-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="087f8-452">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="087f8-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="087f8-453">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="087f8-454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-454">Checksum</span></span>

<span data-ttu-id="087f8-455">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-456">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-456">Definition</span></span>

<span data-ttu-id="087f8-457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-458">Регулярное выражение `Regex_portugal_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-459">Ключевое слово из `Keywords_portugal_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-460">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-460">Keywords</span></span>

<span data-ttu-id="087f8-461">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-461"></span></span>
|<span data-ttu-id="087f8-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-463">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-463">passport number</span></span>  <br/> <span data-ttu-id="087f8-464">Номер паспорта португальский</span><span class="sxs-lookup"><span data-stu-id="087f8-464">portugese passport number</span></span>  <br/> <span data-ttu-id="087f8-465">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-465">passport no</span></span>  <br/> <span data-ttu-id="087f8-466">Действие passaporte número</span><span class="sxs-lookup"><span data-stu-id="087f8-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="087f8-467">Румыния</span><span class="sxs-lookup"><span data-stu-id="087f8-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="087f8-468">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-468">Format</span></span>

<span data-ttu-id="087f8-469">Восемь или девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-470">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-470">Pattern</span></span>

<span data-ttu-id="087f8-471">Восемь или девяти цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-472">Checksum</span></span>

<span data-ttu-id="087f8-473">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-474">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-474">Definition</span></span>

<span data-ttu-id="087f8-475">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-476">Регулярное выражение `Regex_romania_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-477">Ключевое слово из `Keywords_romania_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-478">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-478">Keywords</span></span>

<span data-ttu-id="087f8-479">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-479"></span></span>
|<span data-ttu-id="087f8-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-481">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-481">passport number</span></span>  <br/> <span data-ttu-id="087f8-482">Номер паспорта румынской</span><span class="sxs-lookup"><span data-stu-id="087f8-482">romanian passport number</span></span>  <br/> <span data-ttu-id="087f8-483">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-483">passport no</span></span>  <br/> <span data-ttu-id="087f8-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="087f8-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="087f8-485">Словакия</span><span class="sxs-lookup"><span data-stu-id="087f8-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="087f8-486">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-486">Format</span></span>

<span data-ttu-id="087f8-487">Одной цифры или буквы, семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-488">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-488">Pattern</span></span>

<span data-ttu-id="087f8-489">Одной цифры или буквы (без учета регистра), семь цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="087f8-490">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-490">Checksum</span></span>

<span data-ttu-id="087f8-491">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-492">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-492">Definition</span></span>

<span data-ttu-id="087f8-493">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-494">Регулярное выражение `Regex_slovakia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-495">Ключевое слово из `Keywords_slovakia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-496">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-496">Keywords</span></span>

<span data-ttu-id="087f8-497">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-497"></span></span>
|<span data-ttu-id="087f8-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-499">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-499">passport number</span></span>  <br/> <span data-ttu-id="087f8-500">Номер паспорта словацкий</span><span class="sxs-lookup"><span data-stu-id="087f8-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="087f8-501">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-501">passport no</span></span>  <br/> <span data-ttu-id="087f8-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="087f8-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="087f8-503">Словения</span><span class="sxs-lookup"><span data-stu-id="087f8-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="087f8-504">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-504">Format</span></span>

<span data-ttu-id="087f8-505">Две буквы, затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-506">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-506">Pattern</span></span>

<span data-ttu-id="087f8-507">Две буквы, затем семь цифр:</span><span class="sxs-lookup"><span data-stu-id="087f8-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="087f8-508">Буква «P»</span><span class="sxs-lookup"><span data-stu-id="087f8-508">The letter "P"</span></span>
    
- <span data-ttu-id="087f8-509">Один прописная буква</span><span class="sxs-lookup"><span data-stu-id="087f8-509">One uppercase letter</span></span>
    
- <span data-ttu-id="087f8-510">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="087f8-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="087f8-511">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-511">Checksum</span></span>

<span data-ttu-id="087f8-512">Нет</span><span class="sxs-lookup"><span data-stu-id="087f8-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-513">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-513">Definition</span></span>

<span data-ttu-id="087f8-514">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-515">Регулярное выражение `Regex_slovenia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-516">Ключевое слово из `Keywords_slovenia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-517">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-517">Keywords</span></span>

<span data-ttu-id="087f8-518">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-518"></span></span>
|<span data-ttu-id="087f8-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-520">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-520">passport number</span></span>  <br/> <span data-ttu-id="087f8-521">Номер паспорта словенский</span><span class="sxs-lookup"><span data-stu-id="087f8-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="087f8-522">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-522">passport no</span></span>  <br/> <span data-ttu-id="087f8-523">Список a potnega številka</span><span class="sxs-lookup"><span data-stu-id="087f8-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="087f8-524">Испания</span><span class="sxs-lookup"><span data-stu-id="087f8-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="087f8-525">Формат</span><span class="sxs-lookup"><span data-stu-id="087f8-525">Format</span></span>

<span data-ttu-id="087f8-526">Сочетание восьми или девяти символов буквы и цифры без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="087f8-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="087f8-527">Шаблон</span><span class="sxs-lookup"><span data-stu-id="087f8-527">Pattern</span></span>

<span data-ttu-id="087f8-528">8 или 9 символ сочетание буквы и цифры:</span><span class="sxs-lookup"><span data-stu-id="087f8-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="087f8-529">Двух цифр или символов</span><span class="sxs-lookup"><span data-stu-id="087f8-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="087f8-530">Одну цифру или буква (необязательно)</span><span class="sxs-lookup"><span data-stu-id="087f8-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="087f8-531">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="087f8-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="087f8-532">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="087f8-532">Checksum</span></span>

<span data-ttu-id="087f8-533">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="087f8-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="087f8-534">Определение</span><span class="sxs-lookup"><span data-stu-id="087f8-534">Definition</span></span>

<span data-ttu-id="087f8-535">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="087f8-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="087f8-536">Регулярное выражение `Regex_spain_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="087f8-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="087f8-537">Ключевое слово из `Keywords_spain_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="087f8-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="087f8-538">Keywords</span><span class="sxs-lookup"><span data-stu-id="087f8-538">Keywords</span></span>

<span data-ttu-id="087f8-539">| |</span><span class="sxs-lookup"><span data-stu-id="087f8-539"></span></span>
|<span data-ttu-id="087f8-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="087f8-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="087f8-541">passport</span><span class="sxs-lookup"><span data-stu-id="087f8-541">passport</span></span>  <br/> <span data-ttu-id="087f8-542">Испания паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-542">spain passport</span></span>  <br/> <span data-ttu-id="087f8-543">Книга паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-543">passport book</span></span>  <br/> <span data-ttu-id="087f8-544">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="087f8-544">passport number</span></span>  <br/> <span data-ttu-id="087f8-545">Passport не</span><span class="sxs-lookup"><span data-stu-id="087f8-545">passport no</span></span>  <br/> <span data-ttu-id="087f8-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="087f8-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="087f8-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="087f8-547">número pasaporte</span></span>  <br/> <span data-ttu-id="087f8-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="087f8-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="087f8-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="087f8-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="087f8-550">Швеция</span><span class="sxs-lookup"><span data-stu-id="087f8-550">Sweden</span></span>

<span data-ttu-id="087f8-551">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Швеция» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="087f8-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="087f8-552">(ВЕЛИКОБРИТАНИЯ)</span><span class="sxs-lookup"><span data-stu-id="087f8-552">UK</span></span>

<span data-ttu-id="087f8-p103">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Великобритания США /» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="087f8-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="087f8-555">См. также</span><span class="sxs-lookup"><span data-stu-id="087f8-555">See also</span></span>

[<span data-ttu-id="087f8-556">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="087f8-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

