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
ms.openlocfilehash: 7a7fc1ff826aab4096c46535686eb0fd68173c6f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "25840328"
---
# <a name="eu-passport-number"></a><span data-ttu-id="18d72-104">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="18d72-104">EU Passport Number</span></span>

<span data-ttu-id="18d72-p102">В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении номер паспорта ЕС тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="18d72-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="18d72-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="18d72-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="18d72-108">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-108">Format</span></span>

<span data-ttu-id="18d72-109">Один буквы, необязательное поле и семь цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-110">Pattern</span></span>

<span data-ttu-id="18d72-111">Сочетание одной буквы, семь цифр и один пробел:</span><span class="sxs-lookup"><span data-stu-id="18d72-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="18d72-112">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="18d72-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="18d72-113">Один пробел (необязательно)</span><span class="sxs-lookup"><span data-stu-id="18d72-113">One space (optional)</span></span>
    
- <span data-ttu-id="18d72-114">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="18d72-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-115">Checksum</span></span>

<span data-ttu-id="18d72-116">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="18d72-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-117">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-117">Definition</span></span>

<span data-ttu-id="18d72-118">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-119">Регулярное выражение `Regex_austria_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-120">Ключевое слово из `Keywords_austria_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-121">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-121">Keywords</span></span>

<span data-ttu-id="18d72-122">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-122"></span></span>
|<span data-ttu-id="18d72-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-124">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-124">passport number</span></span>  <br/> <span data-ttu-id="18d72-125">Номер паспорта Австрия</span><span class="sxs-lookup"><span data-stu-id="18d72-125">austrian passport number</span></span>  <br/> <span data-ttu-id="18d72-126">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-126">passport no</span></span>  <br/> <span data-ttu-id="18d72-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="18d72-127">reisepass</span></span>  <br/> <span data-ttu-id="18d72-128">österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="18d72-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="18d72-129">Бельгия</span><span class="sxs-lookup"><span data-stu-id="18d72-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="18d72-130">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-130">Format</span></span>

<span data-ttu-id="18d72-131">Две буквы, а затем шести цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-132">Pattern</span></span>

<span data-ttu-id="18d72-133">Две буквы и следуют шести цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-134">Checksum</span></span>

<span data-ttu-id="18d72-135">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="18d72-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-136">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-136">Definition</span></span>

<span data-ttu-id="18d72-137">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-138">Регулярное выражение `Regex_belgium_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-139">Ключевое слово из `Keywords_belgium_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-140">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-140">Keywords</span></span>

<span data-ttu-id="18d72-141">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-141"></span></span>
|<span data-ttu-id="18d72-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-143">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-143">passport number</span></span>  <br/> <span data-ttu-id="18d72-144">Номер паспорта Бельгия</span><span class="sxs-lookup"><span data-stu-id="18d72-144">belgian passport number</span></span>  <br/> <span data-ttu-id="18d72-145">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-145">passport no</span></span>  <br/> <span data-ttu-id="18d72-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="18d72-146">paspoort</span></span>  <br/> <span data-ttu-id="18d72-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="18d72-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="18d72-148">reisepass kein</span><span class="sxs-lookup"><span data-stu-id="18d72-148">reisepass kein</span></span>  <br/> <span data-ttu-id="18d72-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="18d72-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="18d72-150">Болгария</span><span class="sxs-lookup"><span data-stu-id="18d72-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="18d72-151">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-151">Format</span></span>

<span data-ttu-id="18d72-152">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-153">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-153">Pattern</span></span>

 <span data-ttu-id="18d72-154">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="18d72-155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-155">Checksum</span></span>

<span data-ttu-id="18d72-156">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-157">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-157">Definition</span></span>

<span data-ttu-id="18d72-158">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-159">Регулярное выражение `Regex_bulgaria_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-160">Ключевое слово из `Keywords_bulgaria_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-161">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-161">Keywords</span></span>

<span data-ttu-id="18d72-162">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-162"></span></span>
|<span data-ttu-id="18d72-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-164">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-164">passport number</span></span>  <br/> <span data-ttu-id="18d72-165">Номер паспорта болгарский</span><span class="sxs-lookup"><span data-stu-id="18d72-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="18d72-166">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-166">passport no</span></span>  <br/> <span data-ttu-id="18d72-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="18d72-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="18d72-168">Хорватия</span><span class="sxs-lookup"><span data-stu-id="18d72-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="18d72-169">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-169">Format</span></span>

<span data-ttu-id="18d72-170">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-171">Pattern</span></span>

 <span data-ttu-id="18d72-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="18d72-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-173">Checksum</span></span>

<span data-ttu-id="18d72-174">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-175">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-175">Definition</span></span>

<span data-ttu-id="18d72-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-177">Регулярное выражение `Regex_croatia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-178">Ключевое слово из `Keywords_croatia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-179">Keywords</span></span>

<span data-ttu-id="18d72-180">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-180"></span></span>
|<span data-ttu-id="18d72-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-182">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-182">passport number</span></span>  <br/> <span data-ttu-id="18d72-183">Номер паспорта Хорватский</span><span class="sxs-lookup"><span data-stu-id="18d72-183">croatian passport number</span></span>  <br/> <span data-ttu-id="18d72-184">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-184">passport no</span></span>  <br/> <span data-ttu-id="18d72-185">broj putovnice</span><span class="sxs-lookup"><span data-stu-id="18d72-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="18d72-186">Кипр</span><span class="sxs-lookup"><span data-stu-id="18d72-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="18d72-187">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-187">Format</span></span>

<span data-ttu-id="18d72-188">Один буквы, цифры 6-8 без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-189">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-189">Pattern</span></span>

<span data-ttu-id="18d72-190">Один буквы, цифры 6-8</span><span class="sxs-lookup"><span data-stu-id="18d72-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-191">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-191">Checksum</span></span>

<span data-ttu-id="18d72-192">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-193">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-193">Definition</span></span>

<span data-ttu-id="18d72-194">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-195">Регулярное выражение `Regex_cyprus_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-196">Ключевое слово из `Keywords_cyprus_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-197">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-197">Keywords</span></span>

<span data-ttu-id="18d72-198">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-198"></span></span>
|<span data-ttu-id="18d72-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-200">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-200">passport number</span></span>  <br/> <span data-ttu-id="18d72-201">Номер паспорта Кипр</span><span class="sxs-lookup"><span data-stu-id="18d72-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="18d72-202">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-202">passport no</span></span>  <br/> <span data-ttu-id="18d72-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="18d72-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="18d72-204">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="18d72-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="18d72-205">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-205">Format</span></span>

<span data-ttu-id="18d72-206">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-207">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-207">Pattern</span></span>

<span data-ttu-id="18d72-208">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-209">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-209">Checksum</span></span>

<span data-ttu-id="18d72-210">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-211">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-211">Definition</span></span>

<span data-ttu-id="18d72-212">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-213">Регулярное выражение `Regex_czech_republic_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-214">Ключевое слово из `Keywords_czech_republic_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-215">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-215">Keywords</span></span>

<span data-ttu-id="18d72-216">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-216"></span></span>
|<span data-ttu-id="18d72-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-218">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-218">passport number</span></span>  <br/> <span data-ttu-id="18d72-219">Номер паспорта чешский</span><span class="sxs-lookup"><span data-stu-id="18d72-219">czech passport number</span></span>  <br/> <span data-ttu-id="18d72-220">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-220">passport no</span></span>  <br/> <span data-ttu-id="18d72-221">cestovní pas</span><span class="sxs-lookup"><span data-stu-id="18d72-221">cestovní pas</span></span>  <br/> <span data-ttu-id="18d72-222">PAS</span><span class="sxs-lookup"><span data-stu-id="18d72-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="18d72-223">Дания</span><span class="sxs-lookup"><span data-stu-id="18d72-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="18d72-224">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-224">Format</span></span>

<span data-ttu-id="18d72-225">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-226">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-226">Pattern</span></span>

 <span data-ttu-id="18d72-227">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="18d72-228">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-228">Checksum</span></span>

<span data-ttu-id="18d72-229">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-230">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-230">Definition</span></span>

<span data-ttu-id="18d72-231">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-232">Регулярное выражение `Regex_denmark_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-233">Ключевое слово из `Keywords_denmark_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-234">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-234">Keywords</span></span>

<span data-ttu-id="18d72-235">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-235"></span></span>
|<span data-ttu-id="18d72-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-237">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-237">passport number</span></span>  <br/> <span data-ttu-id="18d72-238">Номер паспорта датский</span><span class="sxs-lookup"><span data-stu-id="18d72-238">danish passport number</span></span>  <br/> <span data-ttu-id="18d72-239">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-239">passport no</span></span>  <br/> <span data-ttu-id="18d72-240">PAS</span><span class="sxs-lookup"><span data-stu-id="18d72-240">pas</span></span>  <br/> <span data-ttu-id="18d72-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="18d72-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="18d72-242">Эстония</span><span class="sxs-lookup"><span data-stu-id="18d72-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="18d72-243">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-243">Format</span></span>

<span data-ttu-id="18d72-244">Один буквы, семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-245">Pattern</span></span>

<span data-ttu-id="18d72-246">Один буквы, семь цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-247">Checksum</span></span>

<span data-ttu-id="18d72-248">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-249">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-249">Definition</span></span>

<span data-ttu-id="18d72-250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-251">Регулярное выражение `Regex_estonia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-252">Ключевое слово из `Keywords_estonia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-253">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-253">Keywords</span></span>

<span data-ttu-id="18d72-254">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-254"></span></span>
|<span data-ttu-id="18d72-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-256">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-256">passport number</span></span>  <br/> <span data-ttu-id="18d72-257">Номер паспорта эстонский</span><span class="sxs-lookup"><span data-stu-id="18d72-257">estonian passport number</span></span>  <br/> <span data-ttu-id="18d72-258">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-258">passport no</span></span>  <br/> <span data-ttu-id="18d72-259">этап kodaniku eesti</span><span class="sxs-lookup"><span data-stu-id="18d72-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="18d72-260">Финляндия</span><span class="sxs-lookup"><span data-stu-id="18d72-260">Finland</span></span>

<span data-ttu-id="18d72-261">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Финляндия» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="18d72-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="18d72-262">Франция</span><span class="sxs-lookup"><span data-stu-id="18d72-262">France</span></span>

<span data-ttu-id="18d72-263">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Гражданина Франции» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="18d72-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="18d72-264">Германия</span><span class="sxs-lookup"><span data-stu-id="18d72-264">Germany</span></span>

<span data-ttu-id="18d72-265">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Германия» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="18d72-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="18d72-266">Греция</span><span class="sxs-lookup"><span data-stu-id="18d72-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="18d72-267">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-267">Format</span></span>

<span data-ttu-id="18d72-268">Две буквы, затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-269">Pattern</span></span>

<span data-ttu-id="18d72-270">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-271">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-271">Checksum</span></span>

<span data-ttu-id="18d72-272">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-273">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-273">Definition</span></span>

<span data-ttu-id="18d72-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-275">Регулярное выражение `Regex_greece_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-276">Ключевое слово из `Keywords_greece_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-277">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-277">Keywords</span></span>

<span data-ttu-id="18d72-278">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-278"></span></span>
|<span data-ttu-id="18d72-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-280">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-280">passport number</span></span>  <br/> <span data-ttu-id="18d72-281">Номер паспорта греческий</span><span class="sxs-lookup"><span data-stu-id="18d72-281">greek passport number</span></span>  <br/> <span data-ttu-id="18d72-282">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-282">passport no</span></span>  <br/> <span data-ttu-id="18d72-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="18d72-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="18d72-284">Венгрия</span><span class="sxs-lookup"><span data-stu-id="18d72-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="18d72-285">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-285">Format</span></span>

<span data-ttu-id="18d72-286">Две буквы, затем шесть или семь цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-287">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-287">Pattern</span></span>

<span data-ttu-id="18d72-288">Две буквы, затем шесть или семь цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-289">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-289">Checksum</span></span>

<span data-ttu-id="18d72-290">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-291">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-291">Definition</span></span>

<span data-ttu-id="18d72-292">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-293">Регулярное выражение `Regex_hungary_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-294">Ключевое слово из `Keywords_hungary_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-295">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-295">Keywords</span></span>

<span data-ttu-id="18d72-296">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-296"></span></span>
|<span data-ttu-id="18d72-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-298">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-298">passport number</span></span>  <br/> <span data-ttu-id="18d72-299">Номер паспорта венгерский</span><span class="sxs-lookup"><span data-stu-id="18d72-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="18d72-300">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-300">passport no</span></span>  <br/> <span data-ttu-id="18d72-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="18d72-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="18d72-302">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="18d72-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="18d72-303">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-303">Format</span></span>

<span data-ttu-id="18d72-304">Два букв или цифр, а затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-305">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-305">Pattern</span></span>

<span data-ttu-id="18d72-306">Два букв или цифр, а затем семь цифр:</span><span class="sxs-lookup"><span data-stu-id="18d72-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="18d72-307">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="18d72-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="18d72-308">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="18d72-309">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-309">Checksum</span></span>

<span data-ttu-id="18d72-310">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-311">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-311">Definition</span></span>

<span data-ttu-id="18d72-312">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-313">Регулярное выражение `Regex_ireland_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-314">Ключевое слово из `Keywords_ireland_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-315">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-315">Keywords</span></span>

<span data-ttu-id="18d72-316">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-316"></span></span>
|<span data-ttu-id="18d72-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-318">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-318">passport number</span></span>  <br/> <span data-ttu-id="18d72-319">Номер паспорта Ирландский</span><span class="sxs-lookup"><span data-stu-id="18d72-319">irish passport number</span></span>  <br/> <span data-ttu-id="18d72-320">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-320">passport no</span></span>  <br/> <span data-ttu-id="18d72-321">PAS</span><span class="sxs-lookup"><span data-stu-id="18d72-321">pas</span></span>  <br/> <span data-ttu-id="18d72-322">passport</span><span class="sxs-lookup"><span data-stu-id="18d72-322">passport</span></span>  <br/> <span data-ttu-id="18d72-323">passeport</span><span class="sxs-lookup"><span data-stu-id="18d72-323">passeport</span></span>  <br/> <span data-ttu-id="18d72-324">passeport numero</span><span class="sxs-lookup"><span data-stu-id="18d72-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="18d72-325">Италия</span><span class="sxs-lookup"><span data-stu-id="18d72-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="18d72-326">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-326">Format</span></span>

<span data-ttu-id="18d72-327">Два букв или цифр, а затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-328">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-328">Pattern</span></span>

<span data-ttu-id="18d72-329">Два букв или цифр, а затем семь цифр:</span><span class="sxs-lookup"><span data-stu-id="18d72-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="18d72-330">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="18d72-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="18d72-331">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="18d72-332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-332">Checksum</span></span>

<span data-ttu-id="18d72-333">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="18d72-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-334">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-334">Definition</span></span>

<span data-ttu-id="18d72-335">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-336">Регулярное выражение `Regex_italy_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-337">Ключевое слово из `Keywords_italy_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-338">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-338">Keywords</span></span>

<span data-ttu-id="18d72-339">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-339"></span></span>
|<span data-ttu-id="18d72-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-341">Номер паспорта итальянский</span><span class="sxs-lookup"><span data-stu-id="18d72-341">italian passport number</span></span>  <br/> <span data-ttu-id="18d72-342">repubblica italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="18d72-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="18d72-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="18d72-343">passaporto</span></span>  <br/> <span data-ttu-id="18d72-344">passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="18d72-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="18d72-345">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-345">passport number</span></span>  <br/> <span data-ttu-id="18d72-346">italiana passaporto numero</span><span class="sxs-lookup"><span data-stu-id="18d72-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="18d72-347">passaporto numero</span><span class="sxs-lookup"><span data-stu-id="18d72-347">passaporto numero</span></span>  <br/> <span data-ttu-id="18d72-348">numéro passeport italien</span><span class="sxs-lookup"><span data-stu-id="18d72-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="18d72-349">numéro passeport</span><span class="sxs-lookup"><span data-stu-id="18d72-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="18d72-350">Латвия</span><span class="sxs-lookup"><span data-stu-id="18d72-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="18d72-351">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-351">Format</span></span>

<span data-ttu-id="18d72-352">Два букв или цифр, а затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-353">Pattern</span></span>

<span data-ttu-id="18d72-354">Два букв или цифр, а затем семь цифр:</span><span class="sxs-lookup"><span data-stu-id="18d72-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="18d72-355">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="18d72-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="18d72-356">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="18d72-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-357">Checksum</span></span>

<span data-ttu-id="18d72-358">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-359">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-359">Definition</span></span>

<span data-ttu-id="18d72-360">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-361">Регулярное выражение `Regex_latvia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-362">Ключевое слово из `Keywords_latvia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-363">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-363">Keywords</span></span>

<span data-ttu-id="18d72-364">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-364"></span></span>
|<span data-ttu-id="18d72-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-366">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-366">passport number</span></span>  <br/> <span data-ttu-id="18d72-367">Номер паспорта латышский</span><span class="sxs-lookup"><span data-stu-id="18d72-367">latvian passport number</span></span>  <br/> <span data-ttu-id="18d72-368">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-368">passport no</span></span>  <br/> <span data-ttu-id="18d72-369">pase numurs</span><span class="sxs-lookup"><span data-stu-id="18d72-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="18d72-370">Литва</span><span class="sxs-lookup"><span data-stu-id="18d72-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="18d72-371">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-371">Format</span></span>

<span data-ttu-id="18d72-372">Восемь цифр или символов без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-373">Pattern</span></span>

<span data-ttu-id="18d72-374">Восемь цифр или символов (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="18d72-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-375">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-375">Checksum</span></span>

<span data-ttu-id="18d72-376">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="18d72-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-377">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-377">Definition</span></span>

<span data-ttu-id="18d72-378">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-379">Регулярное выражение `Regex_lithuania_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-380">Ключевое слово из `Keywords_lithuania_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-381">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-381">Keywords</span></span>

<span data-ttu-id="18d72-382">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-382"></span></span>
|<span data-ttu-id="18d72-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-384">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-384">passport number</span></span>  <br/> <span data-ttu-id="18d72-385">Номер паспорта lithunian</span><span class="sxs-lookup"><span data-stu-id="18d72-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="18d72-386">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-386">passport no</span></span>  <br/> <span data-ttu-id="18d72-387">paso numeris</span><span class="sxs-lookup"><span data-stu-id="18d72-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="18d72-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="18d72-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="18d72-389">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-389">Format</span></span>

<span data-ttu-id="18d72-390">Восемь цифр или символов без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-391">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-391">Pattern</span></span>

<span data-ttu-id="18d72-392">Восемь цифр или символов (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="18d72-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-393">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-393">Checksum</span></span>

<span data-ttu-id="18d72-394">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-395">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-395">Definition</span></span>

<span data-ttu-id="18d72-396">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-397">Регулярное выражение `Regex_nation_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-398">Ключевое слово из `Keywords_nation_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-399">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-399">Keywords</span></span>

<span data-ttu-id="18d72-400">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-400"></span></span>
|<span data-ttu-id="18d72-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-402">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-402">passport number</span></span>  <br/> <span data-ttu-id="18d72-403">Номер паспорта латышский</span><span class="sxs-lookup"><span data-stu-id="18d72-403">latvian passport number</span></span>  <br/> <span data-ttu-id="18d72-404">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-404">passport no</span></span>  <br/> <span data-ttu-id="18d72-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="18d72-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="18d72-406">Мальта</span><span class="sxs-lookup"><span data-stu-id="18d72-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="18d72-407">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-407">Format</span></span>

<span data-ttu-id="18d72-408">Семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-409">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-409">Pattern</span></span>

 <span data-ttu-id="18d72-410">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="18d72-411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-411">Checksum</span></span>

<span data-ttu-id="18d72-412">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-413">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-413">Definition</span></span>

<span data-ttu-id="18d72-414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-415">Регулярное выражение `Regex_malta_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-416">Ключевое слово из `Keywords_malta_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-417">Keywords</span></span>

<span data-ttu-id="18d72-418">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-418"></span></span>
|<span data-ttu-id="18d72-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-420">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-420">passport number</span></span>  <br/> <span data-ttu-id="18d72-421">Номер паспорта maltese</span><span class="sxs-lookup"><span data-stu-id="18d72-421">maltese passport number</span></span>  <br/> <span data-ttu-id="18d72-422">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-422">passport no</span></span>  <br/> <span data-ttu-id="18d72-423">всего numru-passaport</span><span class="sxs-lookup"><span data-stu-id="18d72-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="18d72-424">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="18d72-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="18d72-425">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-425">Format</span></span>

<span data-ttu-id="18d72-426">Девять букв или цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-427">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-427">Pattern</span></span>

<span data-ttu-id="18d72-428">Девять букв или цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-429">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-429">Checksum</span></span>

<span data-ttu-id="18d72-430">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="18d72-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-431">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-431">Definition</span></span>

<span data-ttu-id="18d72-432">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-433">Регулярное выражение `Regex_netherlands_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-434">Ключевое слово из `Keywords_netherlands_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-435">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-435">Keywords</span></span>

<span data-ttu-id="18d72-436">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-436"></span></span>
|<span data-ttu-id="18d72-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-438">Номер паспорта голландский</span><span class="sxs-lookup"><span data-stu-id="18d72-438">dutch passport number</span></span>  <br/> <span data-ttu-id="18d72-439">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-439">passport number</span></span>  <br/> <span data-ttu-id="18d72-440">Номер паспорта Нидерланды</span><span class="sxs-lookup"><span data-stu-id="18d72-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="18d72-441">nederlanden paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="18d72-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="18d72-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="18d72-442">paspoort</span></span>  <br/> <span data-ttu-id="18d72-443">nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="18d72-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="18d72-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="18d72-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="18d72-445">Польша</span><span class="sxs-lookup"><span data-stu-id="18d72-445">Poland</span></span>

<span data-ttu-id="18d72-446">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта для Польши» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="18d72-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="18d72-447">Португалия</span><span class="sxs-lookup"><span data-stu-id="18d72-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="18d72-448">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-448">Format</span></span>

<span data-ttu-id="18d72-449">Один буквы, шести цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-450">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-450">Pattern</span></span>

<span data-ttu-id="18d72-451">Один буквы шести цифр:</span><span class="sxs-lookup"><span data-stu-id="18d72-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="18d72-452">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="18d72-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="18d72-453">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="18d72-454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-454">Checksum</span></span>

<span data-ttu-id="18d72-455">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-456">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-456">Definition</span></span>

<span data-ttu-id="18d72-457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-458">Регулярное выражение `Regex_portugal_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-459">Ключевое слово из `Keywords_portugal_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-460">Keywords</span></span>

<span data-ttu-id="18d72-461">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-461"></span></span>
|<span data-ttu-id="18d72-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-463">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-463">passport number</span></span>  <br/> <span data-ttu-id="18d72-464">Номер паспорта португальский</span><span class="sxs-lookup"><span data-stu-id="18d72-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="18d72-465">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-465">passport no</span></span>  <br/> <span data-ttu-id="18d72-466">Действие passaporte número</span><span class="sxs-lookup"><span data-stu-id="18d72-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="18d72-467">Румыния</span><span class="sxs-lookup"><span data-stu-id="18d72-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="18d72-468">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-468">Format</span></span>

<span data-ttu-id="18d72-469">Восемь или девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-470">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-470">Pattern</span></span>

<span data-ttu-id="18d72-471">Восемь или девяти цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-472">Checksum</span></span>

<span data-ttu-id="18d72-473">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-474">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-474">Definition</span></span>

<span data-ttu-id="18d72-475">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-476">Регулярное выражение `Regex_romania_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-477">Ключевое слово из `Keywords_romania_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-478">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-478">Keywords</span></span>

<span data-ttu-id="18d72-479">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-479"></span></span>
|<span data-ttu-id="18d72-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-481">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-481">passport number</span></span>  <br/> <span data-ttu-id="18d72-482">Номер паспорта румынской</span><span class="sxs-lookup"><span data-stu-id="18d72-482">romanian passport number</span></span>  <br/> <span data-ttu-id="18d72-483">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-483">passport no</span></span>  <br/> <span data-ttu-id="18d72-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="18d72-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="18d72-485">Словакия</span><span class="sxs-lookup"><span data-stu-id="18d72-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="18d72-486">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-486">Format</span></span>

<span data-ttu-id="18d72-487">Одной цифры или буквы, семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-488">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-488">Pattern</span></span>

<span data-ttu-id="18d72-489">Одной цифры или буквы (без учета регистра), семь цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="18d72-490">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-490">Checksum</span></span>

<span data-ttu-id="18d72-491">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-492">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-492">Definition</span></span>

<span data-ttu-id="18d72-493">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-494">Регулярное выражение `Regex_slovakia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-495">Ключевое слово из `Keywords_slovakia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-496">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-496">Keywords</span></span>

<span data-ttu-id="18d72-497">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-497"></span></span>
|<span data-ttu-id="18d72-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-499">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-499">passport number</span></span>  <br/> <span data-ttu-id="18d72-500">Номер паспорта словацкий</span><span class="sxs-lookup"><span data-stu-id="18d72-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="18d72-501">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-501">passport no</span></span>  <br/> <span data-ttu-id="18d72-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="18d72-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="18d72-503">Словения</span><span class="sxs-lookup"><span data-stu-id="18d72-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="18d72-504">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-504">Format</span></span>

<span data-ttu-id="18d72-505">Две буквы, затем семь знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-506">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-506">Pattern</span></span>

<span data-ttu-id="18d72-507">Две буквы, затем семь цифр:</span><span class="sxs-lookup"><span data-stu-id="18d72-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="18d72-508">Буква «P»</span><span class="sxs-lookup"><span data-stu-id="18d72-508">The letter "P"</span></span>
    
- <span data-ttu-id="18d72-509">Один прописная буква</span><span class="sxs-lookup"><span data-stu-id="18d72-509">One uppercase letter</span></span>
    
- <span data-ttu-id="18d72-510">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="18d72-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="18d72-511">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-511">Checksum</span></span>

<span data-ttu-id="18d72-512">Нет</span><span class="sxs-lookup"><span data-stu-id="18d72-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-513">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-513">Definition</span></span>

<span data-ttu-id="18d72-514">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-515">Регулярное выражение `Regex_slovenia_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-516">Ключевое слово из `Keywords_slovenia_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-517">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-517">Keywords</span></span>

<span data-ttu-id="18d72-518">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-518"></span></span>
|<span data-ttu-id="18d72-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-520">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-520">passport number</span></span>  <br/> <span data-ttu-id="18d72-521">Номер паспорта словенский</span><span class="sxs-lookup"><span data-stu-id="18d72-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="18d72-522">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-522">passport no</span></span>  <br/> <span data-ttu-id="18d72-523">Список a potnega številka</span><span class="sxs-lookup"><span data-stu-id="18d72-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="18d72-524">Испания</span><span class="sxs-lookup"><span data-stu-id="18d72-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="18d72-525">Формат</span><span class="sxs-lookup"><span data-stu-id="18d72-525">Format</span></span>

<span data-ttu-id="18d72-526">Сочетание восьми или девяти символов буквы и цифры без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="18d72-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="18d72-527">Шаблон</span><span class="sxs-lookup"><span data-stu-id="18d72-527">Pattern</span></span>

<span data-ttu-id="18d72-528">8 или 9 символ сочетание буквы и цифры:</span><span class="sxs-lookup"><span data-stu-id="18d72-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="18d72-529">Двух цифр или символов</span><span class="sxs-lookup"><span data-stu-id="18d72-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="18d72-530">Одну цифру или буква (необязательно)</span><span class="sxs-lookup"><span data-stu-id="18d72-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="18d72-531">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="18d72-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="18d72-532">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="18d72-532">Checksum</span></span>

<span data-ttu-id="18d72-533">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="18d72-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="18d72-534">Определение</span><span class="sxs-lookup"><span data-stu-id="18d72-534">Definition</span></span>

<span data-ttu-id="18d72-535">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="18d72-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="18d72-536">Регулярное выражение `Regex_spain_eu_passport_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="18d72-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="18d72-537">Ключевое слово из `Keywords_spain_eu_passport_number` найден.</span><span class="sxs-lookup"><span data-stu-id="18d72-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="18d72-538">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="18d72-538">Keywords</span></span>

<span data-ttu-id="18d72-539">| |</span><span class="sxs-lookup"><span data-stu-id="18d72-539"></span></span>
|<span data-ttu-id="18d72-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="18d72-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="18d72-541">passport</span><span class="sxs-lookup"><span data-stu-id="18d72-541">passport</span></span>  <br/> <span data-ttu-id="18d72-542">Испания паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-542">spain passport</span></span>  <br/> <span data-ttu-id="18d72-543">Книга паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-543">passport book</span></span>  <br/> <span data-ttu-id="18d72-544">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="18d72-544">passport number</span></span>  <br/> <span data-ttu-id="18d72-545">Passport не</span><span class="sxs-lookup"><span data-stu-id="18d72-545">passport no</span></span>  <br/> <span data-ttu-id="18d72-546">libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="18d72-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="18d72-547">número pasaporte</span><span class="sxs-lookup"><span data-stu-id="18d72-547">número pasaporte</span></span>  <br/> <span data-ttu-id="18d72-548">españa pasaporte</span><span class="sxs-lookup"><span data-stu-id="18d72-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="18d72-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="18d72-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="18d72-550">Швеция</span><span class="sxs-lookup"><span data-stu-id="18d72-550">Sweden</span></span>

<span data-ttu-id="18d72-551">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Швеция» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="18d72-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="18d72-552">(ВЕЛИКОБРИТАНИЯ)</span><span class="sxs-lookup"><span data-stu-id="18d72-552">UK</span></span>

<span data-ttu-id="18d72-p103">Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Великобритания США /» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="18d72-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18d72-555">См. также</span><span class="sxs-lookup"><span data-stu-id="18d72-555">See also</span></span>

[<span data-ttu-id="18d72-556">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="18d72-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

