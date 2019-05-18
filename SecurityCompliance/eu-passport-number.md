---
title: Номер паспорта ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС Passport Number. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: fa3be04dec0f71a2568e046abd6b0af3e20181c5
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152971"
---
# <a name="eu-passport-number"></a><span data-ttu-id="95628-104">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="95628-104">EU Passport Number</span></span>

<span data-ttu-id="95628-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС Passport Number.</span><span class="sxs-lookup"><span data-stu-id="95628-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="95628-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="95628-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="95628-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="95628-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="95628-108">Format</span><span class="sxs-lookup"><span data-stu-id="95628-108">Format</span></span>

<span data-ttu-id="95628-109">Одна буква, за которой следует необязательный пробел и семь цифр</span><span class="sxs-lookup"><span data-stu-id="95628-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-110">Pattern</span></span>

<span data-ttu-id="95628-111">Сочетание одной буквы, семи цифр и одного пробела:</span><span class="sxs-lookup"><span data-stu-id="95628-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="95628-112">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="95628-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="95628-113">Один пробел (необязательно)</span><span class="sxs-lookup"><span data-stu-id="95628-113">One space (optional)</span></span>
    
- <span data-ttu-id="95628-114">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95628-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-115">Checksum</span></span>

<span data-ttu-id="95628-116">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="95628-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-117">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-117">Definition</span></span>

<span data-ttu-id="95628-118">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-119">Регулярное выражение `Regex_austria_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-120">Найдено ключевое `Keywords_austria_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-121">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-121">Keywords</span></span>

<span data-ttu-id="95628-122">| |</span><span class="sxs-lookup"><span data-stu-id="95628-122"></span></span>
|<span data-ttu-id="95628-123">**Кэйвордс_аустриа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-124">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-124">passport number</span></span>  <br/> <span data-ttu-id="95628-125">Австрийский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="95628-125">austrian passport number</span></span>  <br/> <span data-ttu-id="95628-126">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-126">passport no</span></span>  <br/> <span data-ttu-id="95628-127">реисепасс</span><span class="sxs-lookup"><span data-stu-id="95628-127">reisepass</span></span>  <br/> <span data-ttu-id="95628-128">öстерреичисч реисепасс</span><span class="sxs-lookup"><span data-stu-id="95628-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="95628-129">Бельгия</span><span class="sxs-lookup"><span data-stu-id="95628-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="95628-130">Format</span><span class="sxs-lookup"><span data-stu-id="95628-130">Format</span></span>

<span data-ttu-id="95628-131">Две буквы, за которыми следуют шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-132">Pattern</span></span>

<span data-ttu-id="95628-133">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-134">Checksum</span></span>

<span data-ttu-id="95628-135">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="95628-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-136">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-136">Definition</span></span>

<span data-ttu-id="95628-137">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-138">Регулярное выражение `Regex_belgium_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-139">Найдено ключевое `Keywords_belgium_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-140">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-140">Keywords</span></span>

<span data-ttu-id="95628-141">| |</span><span class="sxs-lookup"><span data-stu-id="95628-141"></span></span>
|<span data-ttu-id="95628-142">**Кэйвордс_белгиум_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-143">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-143">passport number</span></span>  <br/> <span data-ttu-id="95628-144">Бельгийский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="95628-144">belgian passport number</span></span>  <br/> <span data-ttu-id="95628-145">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-145">passport no</span></span>  <br/> <span data-ttu-id="95628-146">паспурт</span><span class="sxs-lookup"><span data-stu-id="95628-146">paspoort</span></span>  <br/> <span data-ttu-id="95628-147">паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="95628-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="95628-148">реисепасс Кеин</span><span class="sxs-lookup"><span data-stu-id="95628-148">reisepass kein</span></span>  <br/> <span data-ttu-id="95628-149">реисепасс</span><span class="sxs-lookup"><span data-stu-id="95628-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="95628-150">Болгария</span><span class="sxs-lookup"><span data-stu-id="95628-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="95628-151">Format</span><span class="sxs-lookup"><span data-stu-id="95628-151">Format</span></span>

<span data-ttu-id="95628-152">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-153">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-153">Pattern</span></span>

 <span data-ttu-id="95628-154">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="95628-155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-155">Checksum</span></span>

<span data-ttu-id="95628-156">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-157">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-157">Definition</span></span>

<span data-ttu-id="95628-158">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-159">Регулярное выражение `Regex_bulgaria_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-160">Найдено ключевое `Keywords_bulgaria_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-161">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-161">Keywords</span></span>

<span data-ttu-id="95628-162">| |</span><span class="sxs-lookup"><span data-stu-id="95628-162"></span></span>
|<span data-ttu-id="95628-163">**Кэйвордс_булгариа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-164">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-164">passport number</span></span>  <br/> <span data-ttu-id="95628-165">номер паспорта для болгарского языка</span><span class="sxs-lookup"><span data-stu-id="95628-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="95628-166">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-166">passport no</span></span>  <br/> <span data-ttu-id="95628-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="95628-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="95628-168">Хорватия</span><span class="sxs-lookup"><span data-stu-id="95628-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="95628-169">Format</span><span class="sxs-lookup"><span data-stu-id="95628-169">Format</span></span>

<span data-ttu-id="95628-170">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-171">Pattern</span></span>

 <span data-ttu-id="95628-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="95628-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-173">Checksum</span></span>

<span data-ttu-id="95628-174">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-175">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-175">Definition</span></span>

<span data-ttu-id="95628-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-177">Регулярное выражение `Regex_croatia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-178">Найдено ключевое `Keywords_croatia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-179">Keywords</span></span>

<span data-ttu-id="95628-180">| |</span><span class="sxs-lookup"><span data-stu-id="95628-180"></span></span>
|<span data-ttu-id="95628-181">**Кэйвордс_кроатиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-182">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-182">passport number</span></span>  <br/> <span data-ttu-id="95628-183">номер паспорта для хорватского языка</span><span class="sxs-lookup"><span data-stu-id="95628-183">croatian passport number</span></span>  <br/> <span data-ttu-id="95628-184">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-184">passport no</span></span>  <br/> <span data-ttu-id="95628-185">Брож путовнице</span><span class="sxs-lookup"><span data-stu-id="95628-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="95628-186">Кипр</span><span class="sxs-lookup"><span data-stu-id="95628-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="95628-187">Format</span><span class="sxs-lookup"><span data-stu-id="95628-187">Format</span></span>

<span data-ttu-id="95628-188">Одна буква, за которой следуют 6-8 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-189">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-189">Pattern</span></span>

<span data-ttu-id="95628-190">Одна буква, за которой следуют шесть и восемь цифр</span><span class="sxs-lookup"><span data-stu-id="95628-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-191">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-191">Checksum</span></span>

<span data-ttu-id="95628-192">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-193">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-193">Definition</span></span>

<span data-ttu-id="95628-194">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-195">Регулярное выражение `Regex_cyprus_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-196">Найдено ключевое `Keywords_cyprus_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-197">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-197">Keywords</span></span>

<span data-ttu-id="95628-198">| |</span><span class="sxs-lookup"><span data-stu-id="95628-198"></span></span>
|<span data-ttu-id="95628-199">**Кэйвордс_ципрус_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-200">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-200">passport number</span></span>  <br/> <span data-ttu-id="95628-201">номер паспорта для Кипр</span><span class="sxs-lookup"><span data-stu-id="95628-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="95628-202">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-202">passport no</span></span>  <br/> <span data-ttu-id="95628-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="95628-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="95628-204">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="95628-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="95628-205">Format</span><span class="sxs-lookup"><span data-stu-id="95628-205">Format</span></span>

<span data-ttu-id="95628-206">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-207">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-207">Pattern</span></span>

<span data-ttu-id="95628-208">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-209">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-209">Checksum</span></span>

<span data-ttu-id="95628-210">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-211">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-211">Definition</span></span>

<span data-ttu-id="95628-212">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-213">Регулярное выражение `Regex_czech_republic_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-214">Найдено ключевое `Keywords_czech_republic_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-215">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-215">Keywords</span></span>

<span data-ttu-id="95628-216">| |</span><span class="sxs-lookup"><span data-stu-id="95628-216"></span></span>
|<span data-ttu-id="95628-217">**Кэйвордс_кзеч_републик_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-218">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-218">passport number</span></span>  <br/> <span data-ttu-id="95628-219">номер паспорта для чешского языка</span><span class="sxs-lookup"><span data-stu-id="95628-219">czech passport number</span></span>  <br/> <span data-ttu-id="95628-220">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-220">passport no</span></span>  <br/> <span data-ttu-id="95628-221">цестовнí PAS</span><span class="sxs-lookup"><span data-stu-id="95628-221">cestovní pas</span></span>  <br/> <span data-ttu-id="95628-222">соответствующий</span><span class="sxs-lookup"><span data-stu-id="95628-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="95628-223">Дания</span><span class="sxs-lookup"><span data-stu-id="95628-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="95628-224">Format</span><span class="sxs-lookup"><span data-stu-id="95628-224">Format</span></span>

<span data-ttu-id="95628-225">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-226">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-226">Pattern</span></span>

 <span data-ttu-id="95628-227">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="95628-228">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-228">Checksum</span></span>

<span data-ttu-id="95628-229">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-230">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-230">Definition</span></span>

<span data-ttu-id="95628-231">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-232">Регулярное выражение `Regex_denmark_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-233">Найдено ключевое `Keywords_denmark_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-234">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-234">Keywords</span></span>

<span data-ttu-id="95628-235">| |</span><span class="sxs-lookup"><span data-stu-id="95628-235"></span></span>
|<span data-ttu-id="95628-236">**Кэйвордс_денмарк_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-237">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-237">passport number</span></span>  <br/> <span data-ttu-id="95628-238">номер паспорта для датского языка</span><span class="sxs-lookup"><span data-stu-id="95628-238">danish passport number</span></span>  <br/> <span data-ttu-id="95628-239">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-239">passport no</span></span>  <br/> <span data-ttu-id="95628-240">соответствующий</span><span class="sxs-lookup"><span data-stu-id="95628-240">pas</span></span>  <br/> <span data-ttu-id="95628-241">паснуммер</span><span class="sxs-lookup"><span data-stu-id="95628-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="95628-242">Эстония</span><span class="sxs-lookup"><span data-stu-id="95628-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="95628-243">Format</span><span class="sxs-lookup"><span data-stu-id="95628-243">Format</span></span>

<span data-ttu-id="95628-244">Одна буква, за которой следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-245">Pattern</span></span>

<span data-ttu-id="95628-246">Одна буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-247">Checksum</span></span>

<span data-ttu-id="95628-248">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-249">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-249">Definition</span></span>

<span data-ttu-id="95628-250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-251">Регулярное выражение `Regex_estonia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-252">Найдено ключевое `Keywords_estonia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-253">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-253">Keywords</span></span>

<span data-ttu-id="95628-254">| |</span><span class="sxs-lookup"><span data-stu-id="95628-254"></span></span>
|<span data-ttu-id="95628-255">**Кэйвордс_естониа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-256">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-256">passport number</span></span>  <br/> <span data-ttu-id="95628-257">номер паспорта для Эстонии</span><span class="sxs-lookup"><span data-stu-id="95628-257">estonian passport number</span></span>  <br/> <span data-ttu-id="95628-258">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-258">passport no</span></span>  <br/> <span data-ttu-id="95628-259">Исти коданику Pass</span><span class="sxs-lookup"><span data-stu-id="95628-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="95628-260">Финляндия</span><span class="sxs-lookup"><span data-stu-id="95628-260">Finland</span></span>

<span data-ttu-id="95628-261">Дополнительные сведения можно найти в разделе "Финляндия Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95628-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="95628-262">Франция</span><span class="sxs-lookup"><span data-stu-id="95628-262">France</span></span>

<span data-ttu-id="95628-263">Дополнительные сведения можно найти в разделе "Франция Passport Number", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95628-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="95628-264">Германия</span><span class="sxs-lookup"><span data-stu-id="95628-264">Germany</span></span>

<span data-ttu-id="95628-265">Дополнительные сведения можно найти в разделе "Германия Passport Number", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95628-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="95628-266">Греция</span><span class="sxs-lookup"><span data-stu-id="95628-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="95628-267">Format</span><span class="sxs-lookup"><span data-stu-id="95628-267">Format</span></span>

<span data-ttu-id="95628-268">Две буквы, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-269">Pattern</span></span>

<span data-ttu-id="95628-270">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-271">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-271">Checksum</span></span>

<span data-ttu-id="95628-272">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-273">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-273">Definition</span></span>

<span data-ttu-id="95628-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-275">Регулярное выражение `Regex_greece_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-276">Найдено ключевое `Keywords_greece_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-277">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-277">Keywords</span></span>

<span data-ttu-id="95628-278">| |</span><span class="sxs-lookup"><span data-stu-id="95628-278"></span></span>
|<span data-ttu-id="95628-279">**Кэйвордс_грице_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-280">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-280">passport number</span></span>  <br/> <span data-ttu-id="95628-281">номер паспорта греческого алфавита</span><span class="sxs-lookup"><span data-stu-id="95628-281">greek passport number</span></span>  <br/> <span data-ttu-id="95628-282">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-282">passport no</span></span>  <br/> <span data-ttu-id="95628-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="95628-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="95628-284">Венгрия</span><span class="sxs-lookup"><span data-stu-id="95628-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="95628-285">Format</span><span class="sxs-lookup"><span data-stu-id="95628-285">Format</span></span>

<span data-ttu-id="95628-286">Две буквы, за которыми следуют шесть или семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-287">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-287">Pattern</span></span>

<span data-ttu-id="95628-288">Две буквы, за которыми следуют шесть или семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-289">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-289">Checksum</span></span>

<span data-ttu-id="95628-290">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-291">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-291">Definition</span></span>

<span data-ttu-id="95628-292">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-293">Регулярное выражение `Regex_hungary_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-294">Найдено ключевое `Keywords_hungary_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-295">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-295">Keywords</span></span>

<span data-ttu-id="95628-296">| |</span><span class="sxs-lookup"><span data-stu-id="95628-296"></span></span>
|<span data-ttu-id="95628-297">**Кэйвордс_хунгари_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-298">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-298">passport number</span></span>  <br/> <span data-ttu-id="95628-299">Венгерский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="95628-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="95628-300">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-300">passport no</span></span>  <br/> <span data-ttu-id="95628-301">úтлевéл сзáма</span><span class="sxs-lookup"><span data-stu-id="95628-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="95628-302">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="95628-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="95628-303">Format</span><span class="sxs-lookup"><span data-stu-id="95628-303">Format</span></span>

<span data-ttu-id="95628-304">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-305">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-305">Pattern</span></span>

<span data-ttu-id="95628-306">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="95628-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="95628-307">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="95628-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="95628-308">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95628-309">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-309">Checksum</span></span>

<span data-ttu-id="95628-310">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-311">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-311">Definition</span></span>

<span data-ttu-id="95628-312">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-313">Регулярное выражение `Regex_ireland_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-314">Найдено ключевое `Keywords_ireland_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-315">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-315">Keywords</span></span>

<span data-ttu-id="95628-316">| |</span><span class="sxs-lookup"><span data-stu-id="95628-316"></span></span>
|<span data-ttu-id="95628-317">**Кэйвордс_иреланд_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-318">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-318">passport number</span></span>  <br/> <span data-ttu-id="95628-319">Ирландский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="95628-319">irish passport number</span></span>  <br/> <span data-ttu-id="95628-320">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-320">passport no</span></span>  <br/> <span data-ttu-id="95628-321">соответствующий</span><span class="sxs-lookup"><span data-stu-id="95628-321">pas</span></span>  <br/> <span data-ttu-id="95628-322">службу</span><span class="sxs-lookup"><span data-stu-id="95628-322">passport</span></span>  <br/> <span data-ttu-id="95628-323">пассепорт</span><span class="sxs-lookup"><span data-stu-id="95628-323">passeport</span></span>  <br/> <span data-ttu-id="95628-324">пассепорт нумеро</span><span class="sxs-lookup"><span data-stu-id="95628-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="95628-325">Италия</span><span class="sxs-lookup"><span data-stu-id="95628-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="95628-326">Format</span><span class="sxs-lookup"><span data-stu-id="95628-326">Format</span></span>

<span data-ttu-id="95628-327">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-328">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-328">Pattern</span></span>

<span data-ttu-id="95628-329">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="95628-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="95628-330">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="95628-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="95628-331">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95628-332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-332">Checksum</span></span>

<span data-ttu-id="95628-333">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="95628-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-334">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-334">Definition</span></span>

<span data-ttu-id="95628-335">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-336">Регулярное выражение `Regex_italy_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-337">Найдено ключевое `Keywords_italy_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-338">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-338">Keywords</span></span>

<span data-ttu-id="95628-339">| |</span><span class="sxs-lookup"><span data-stu-id="95628-339"></span></span>
|<span data-ttu-id="95628-340">**Кэйвордс_итали_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-341">номер паспорта для итальянского языка</span><span class="sxs-lookup"><span data-stu-id="95628-341">italian passport number</span></span>  <br/> <span data-ttu-id="95628-342">Репубблика итальянский пассапорто</span><span class="sxs-lookup"><span data-stu-id="95628-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="95628-343">пассапорто</span><span class="sxs-lookup"><span data-stu-id="95628-343">passaporto</span></span>  <br/> <span data-ttu-id="95628-344">пассапорто итальянский</span><span class="sxs-lookup"><span data-stu-id="95628-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="95628-345">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-345">passport number</span></span>  <br/> <span data-ttu-id="95628-346">Итальянский пассапорто нумеро</span><span class="sxs-lookup"><span data-stu-id="95628-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="95628-347">пассапорто нумеро</span><span class="sxs-lookup"><span data-stu-id="95628-347">passaporto numero</span></span>  <br/> <span data-ttu-id="95628-348">нумéро пассепорт италиен</span><span class="sxs-lookup"><span data-stu-id="95628-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="95628-349">нумéро пассепорт</span><span class="sxs-lookup"><span data-stu-id="95628-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="95628-350">Латвия</span><span class="sxs-lookup"><span data-stu-id="95628-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="95628-351">Format</span><span class="sxs-lookup"><span data-stu-id="95628-351">Format</span></span>

<span data-ttu-id="95628-352">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-353">Pattern</span></span>

<span data-ttu-id="95628-354">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="95628-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="95628-355">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="95628-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="95628-356">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95628-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-357">Checksum</span></span>

<span data-ttu-id="95628-358">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-359">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-359">Definition</span></span>

<span data-ttu-id="95628-360">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-361">Регулярное выражение `Regex_latvia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-362">Найдено ключевое `Keywords_latvia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-363">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-363">Keywords</span></span>

<span data-ttu-id="95628-364">| |</span><span class="sxs-lookup"><span data-stu-id="95628-364"></span></span>
|<span data-ttu-id="95628-365">**Кэйвордс_латвиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-366">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-366">passport number</span></span>  <br/> <span data-ttu-id="95628-367">номер паспорта для Латвии</span><span class="sxs-lookup"><span data-stu-id="95628-367">latvian passport number</span></span>  <br/> <span data-ttu-id="95628-368">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-368">passport no</span></span>  <br/> <span data-ttu-id="95628-369">ПАСЕ нумурс</span><span class="sxs-lookup"><span data-stu-id="95628-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="95628-370">Литва</span><span class="sxs-lookup"><span data-stu-id="95628-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="95628-371">Format</span><span class="sxs-lookup"><span data-stu-id="95628-371">Format</span></span>

<span data-ttu-id="95628-372">Восемь цифр или букв без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-373">Pattern</span></span>

<span data-ttu-id="95628-374">Восемь цифр или букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="95628-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-375">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-375">Checksum</span></span>

<span data-ttu-id="95628-376">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="95628-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-377">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-377">Definition</span></span>

<span data-ttu-id="95628-378">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-379">Регулярное выражение `Regex_lithuania_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-380">Найдено ключевое `Keywords_lithuania_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-381">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-381">Keywords</span></span>

<span data-ttu-id="95628-382">| |</span><span class="sxs-lookup"><span data-stu-id="95628-382"></span></span>
|<span data-ttu-id="95628-383">**Кэйвордс_лисуаниа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-384">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-384">passport number</span></span>  <br/> <span data-ttu-id="95628-385">номер паспорта лисуниан</span><span class="sxs-lookup"><span data-stu-id="95628-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="95628-386">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-386">passport no</span></span>  <br/> <span data-ttu-id="95628-387">Пасо нумерис</span><span class="sxs-lookup"><span data-stu-id="95628-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="95628-388">Луксембург</span><span class="sxs-lookup"><span data-stu-id="95628-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="95628-389">Format</span><span class="sxs-lookup"><span data-stu-id="95628-389">Format</span></span>

<span data-ttu-id="95628-390">Восемь цифр или букв без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-391">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-391">Pattern</span></span>

<span data-ttu-id="95628-392">Восемь цифр или букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="95628-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-393">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-393">Checksum</span></span>

<span data-ttu-id="95628-394">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-395">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-395">Definition</span></span>

<span data-ttu-id="95628-396">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-397">Регулярное выражение `Regex_nation_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-398">Найдено ключевое `Keywords_nation_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-399">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-399">Keywords</span></span>

<span data-ttu-id="95628-400">| |</span><span class="sxs-lookup"><span data-stu-id="95628-400"></span></span>
|<span data-ttu-id="95628-401">**Кэйвордс_натион_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-402">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-402">passport number</span></span>  <br/> <span data-ttu-id="95628-403">номер паспорта для Латвии</span><span class="sxs-lookup"><span data-stu-id="95628-403">latvian passport number</span></span>  <br/> <span data-ttu-id="95628-404">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-404">passport no</span></span>  <br/> <span data-ttu-id="95628-405">пасснуммер</span><span class="sxs-lookup"><span data-stu-id="95628-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="95628-406">Мальта</span><span class="sxs-lookup"><span data-stu-id="95628-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="95628-407">Format</span><span class="sxs-lookup"><span data-stu-id="95628-407">Format</span></span>

<span data-ttu-id="95628-408">Семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-409">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-409">Pattern</span></span>

 <span data-ttu-id="95628-410">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="95628-411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-411">Checksum</span></span>

<span data-ttu-id="95628-412">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-413">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-413">Definition</span></span>

<span data-ttu-id="95628-414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-415">Регулярное выражение `Regex_malta_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-416">Найдено ключевое `Keywords_malta_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-417">Keywords</span></span>

<span data-ttu-id="95628-418">| |</span><span class="sxs-lookup"><span data-stu-id="95628-418"></span></span>
|<span data-ttu-id="95628-419">**Кэйвордс_малта_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-420">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-420">passport number</span></span>  <br/> <span data-ttu-id="95628-421">номер паспорта Мальтийский</span><span class="sxs-lookup"><span data-stu-id="95628-421">maltese passport number</span></span>  <br/> <span data-ttu-id="95628-422">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-422">passport no</span></span>  <br/> <span data-ttu-id="95628-423">нумру Тал — пассапорт</span><span class="sxs-lookup"><span data-stu-id="95628-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="95628-424">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="95628-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="95628-425">Format</span><span class="sxs-lookup"><span data-stu-id="95628-425">Format</span></span>

<span data-ttu-id="95628-426">Девять букв или цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-427">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-427">Pattern</span></span>

<span data-ttu-id="95628-428">Девять букв или цифр;</span><span class="sxs-lookup"><span data-stu-id="95628-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-429">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-429">Checksum</span></span>

<span data-ttu-id="95628-430">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="95628-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-431">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-431">Definition</span></span>

<span data-ttu-id="95628-432">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-433">Регулярное выражение `Regex_netherlands_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-434">Найдено ключевое `Keywords_netherlands_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-435">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-435">Keywords</span></span>

<span data-ttu-id="95628-436">| |</span><span class="sxs-lookup"><span data-stu-id="95628-436"></span></span>
|<span data-ttu-id="95628-437">**Кэйвордс_несерландс_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-438">номер паспорта для нидерландского языка</span><span class="sxs-lookup"><span data-stu-id="95628-438">dutch passport number</span></span>  <br/> <span data-ttu-id="95628-439">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-439">passport number</span></span>  <br/> <span data-ttu-id="95628-440">номер паспорта Нидерландов</span><span class="sxs-lookup"><span data-stu-id="95628-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="95628-441">недерланден паспурт нуммер</span><span class="sxs-lookup"><span data-stu-id="95628-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="95628-442">паспурт</span><span class="sxs-lookup"><span data-stu-id="95628-442">paspoort</span></span>  <br/> <span data-ttu-id="95628-443">недерланден паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="95628-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="95628-444">паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="95628-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="95628-445">Польша</span><span class="sxs-lookup"><span data-stu-id="95628-445">Poland</span></span>

<span data-ttu-id="95628-446">Дополнительные сведения можно найти в разделе "Польша Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95628-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="95628-447">Португалия</span><span class="sxs-lookup"><span data-stu-id="95628-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="95628-448">Format</span><span class="sxs-lookup"><span data-stu-id="95628-448">Format</span></span>

<span data-ttu-id="95628-449">Одна буква, за которой следуют шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-450">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-450">Pattern</span></span>

<span data-ttu-id="95628-451">Одна буква, за которой следуют шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="95628-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="95628-452">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="95628-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="95628-453">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95628-454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-454">Checksum</span></span>

<span data-ttu-id="95628-455">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-456">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-456">Definition</span></span>

<span data-ttu-id="95628-457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-458">Регулярное выражение `Regex_portugal_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-459">Найдено ключевое `Keywords_portugal_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-460">Keywords</span></span>

<span data-ttu-id="95628-461">| |</span><span class="sxs-lookup"><span data-stu-id="95628-461"></span></span>
|<span data-ttu-id="95628-462">**Кэйвордс_португал_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-463">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-463">passport number</span></span>  <br/> <span data-ttu-id="95628-464">номер паспорта для португальского языка</span><span class="sxs-lookup"><span data-stu-id="95628-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="95628-465">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-465">passport no</span></span>  <br/> <span data-ttu-id="95628-466">нúмеро Do пассапорте</span><span class="sxs-lookup"><span data-stu-id="95628-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="95628-467">Румыния</span><span class="sxs-lookup"><span data-stu-id="95628-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="95628-468">Format</span><span class="sxs-lookup"><span data-stu-id="95628-468">Format</span></span>

<span data-ttu-id="95628-469">Восемь или девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-470">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-470">Pattern</span></span>

<span data-ttu-id="95628-471">Восемь или девять цифр</span><span class="sxs-lookup"><span data-stu-id="95628-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-472">Checksum</span></span>

<span data-ttu-id="95628-473">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-474">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-474">Definition</span></span>

<span data-ttu-id="95628-475">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-476">Регулярное выражение `Regex_romania_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-477">Найдено ключевое `Keywords_romania_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-478">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-478">Keywords</span></span>

<span data-ttu-id="95628-479">| |</span><span class="sxs-lookup"><span data-stu-id="95628-479"></span></span>
|<span data-ttu-id="95628-480">**Кэйвордс_романиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-481">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-481">passport number</span></span>  <br/> <span data-ttu-id="95628-482">номер паспорта для румынского языка</span><span class="sxs-lookup"><span data-stu-id="95628-482">romanian passport number</span></span>  <br/> <span data-ttu-id="95628-483">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-483">passport no</span></span>  <br/> <span data-ttu-id="95628-484">нумăрул паșапортулуи</span><span class="sxs-lookup"><span data-stu-id="95628-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="95628-485">Словакия</span><span class="sxs-lookup"><span data-stu-id="95628-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="95628-486">Format</span><span class="sxs-lookup"><span data-stu-id="95628-486">Format</span></span>

<span data-ttu-id="95628-487">Одна цифра или буква, за которой следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-488">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-488">Pattern</span></span>

<span data-ttu-id="95628-489">Одна цифра или буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95628-490">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-490">Checksum</span></span>

<span data-ttu-id="95628-491">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-492">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-492">Definition</span></span>

<span data-ttu-id="95628-493">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-494">Регулярное выражение `Regex_slovakia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-495">Найдено ключевое `Keywords_slovakia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-496">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-496">Keywords</span></span>

<span data-ttu-id="95628-497">| |</span><span class="sxs-lookup"><span data-stu-id="95628-497"></span></span>
|<span data-ttu-id="95628-498">**Кэйвордс_словакиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-499">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-499">passport number</span></span>  <br/> <span data-ttu-id="95628-500">номер паспорта словакиан</span><span class="sxs-lookup"><span data-stu-id="95628-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="95628-501">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-501">passport no</span></span>  <br/> <span data-ttu-id="95628-502">číсло Пасу</span><span class="sxs-lookup"><span data-stu-id="95628-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="95628-503">Словения</span><span class="sxs-lookup"><span data-stu-id="95628-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="95628-504">Format</span><span class="sxs-lookup"><span data-stu-id="95628-504">Format</span></span>

<span data-ttu-id="95628-505">Две буквы, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-506">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-506">Pattern</span></span>

<span data-ttu-id="95628-507">Две буквы, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="95628-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="95628-508">Буква "P"</span><span class="sxs-lookup"><span data-stu-id="95628-508">The letter "P"</span></span>
    
- <span data-ttu-id="95628-509">Одна прописная буква</span><span class="sxs-lookup"><span data-stu-id="95628-509">One uppercase letter</span></span>
    
- <span data-ttu-id="95628-510">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95628-511">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-511">Checksum</span></span>

<span data-ttu-id="95628-512">Нет</span><span class="sxs-lookup"><span data-stu-id="95628-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-513">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-513">Definition</span></span>

<span data-ttu-id="95628-514">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-515">Регулярное выражение `Regex_slovenia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-516">Найдено ключевое `Keywords_slovenia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-517">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-517">Keywords</span></span>

<span data-ttu-id="95628-518">| |</span><span class="sxs-lookup"><span data-stu-id="95628-518"></span></span>
|<span data-ttu-id="95628-519">**Кэйвордс_словениа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-520">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-520">passport number</span></span>  <br/> <span data-ttu-id="95628-521">номер паспорта для словенского языка</span><span class="sxs-lookup"><span data-stu-id="95628-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="95628-522">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-522">passport no</span></span>  <br/> <span data-ttu-id="95628-523">Список потнега šтевилка</span><span class="sxs-lookup"><span data-stu-id="95628-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="95628-524">Испания</span><span class="sxs-lookup"><span data-stu-id="95628-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="95628-525">Format</span><span class="sxs-lookup"><span data-stu-id="95628-525">Format</span></span>

<span data-ttu-id="95628-526">Сочетание букв и цифр из восьми или девяти символов без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="95628-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95628-527">Шаблон</span><span class="sxs-lookup"><span data-stu-id="95628-527">Pattern</span></span>

<span data-ttu-id="95628-528">Сочетание букв и цифр из восьми или девяти символов:</span><span class="sxs-lookup"><span data-stu-id="95628-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="95628-529">Две цифры или буквы</span><span class="sxs-lookup"><span data-stu-id="95628-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="95628-530">Одна цифра или буква (необязательно)</span><span class="sxs-lookup"><span data-stu-id="95628-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="95628-531">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="95628-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95628-532">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="95628-532">Checksum</span></span>

<span data-ttu-id="95628-533">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="95628-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95628-534">Определение</span><span class="sxs-lookup"><span data-stu-id="95628-534">Definition</span></span>

<span data-ttu-id="95628-535">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="95628-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95628-536">Регулярное выражение `Regex_spain_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="95628-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95628-537">Найдено ключевое `Keywords_spain_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="95628-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95628-538">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="95628-538">Keywords</span></span>

<span data-ttu-id="95628-539">| |</span><span class="sxs-lookup"><span data-stu-id="95628-539"></span></span>
|<span data-ttu-id="95628-540">**Кэйвордс_спаин_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="95628-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95628-541">службу</span><span class="sxs-lookup"><span data-stu-id="95628-541">passport</span></span>  <br/> <span data-ttu-id="95628-542">Служба Passport, Испания</span><span class="sxs-lookup"><span data-stu-id="95628-542">spain passport</span></span>  <br/> <span data-ttu-id="95628-543">Книга Passport</span><span class="sxs-lookup"><span data-stu-id="95628-543">passport book</span></span>  <br/> <span data-ttu-id="95628-544">passport number</span><span class="sxs-lookup"><span data-stu-id="95628-544">passport number</span></span>  <br/> <span data-ttu-id="95628-545">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="95628-545">passport no</span></span>  <br/> <span data-ttu-id="95628-546">либрета пасапорте</span><span class="sxs-lookup"><span data-stu-id="95628-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="95628-547">нúмеро пасапорте</span><span class="sxs-lookup"><span data-stu-id="95628-547">número pasaporte</span></span>  <br/> <span data-ttu-id="95628-548">еспаñа пасапорте</span><span class="sxs-lookup"><span data-stu-id="95628-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="95628-549">пасапорте</span><span class="sxs-lookup"><span data-stu-id="95628-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="95628-550">Швеция</span><span class="sxs-lookup"><span data-stu-id="95628-550">Sweden</span></span>

<span data-ttu-id="95628-551">Дополнительные сведения можно найти в разделе "Швеции Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95628-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="95628-552">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="95628-552">UK</span></span>

<span data-ttu-id="95628-553">Дополнительные сведения см. в разделе "США/Великобритания</span><span class="sxs-lookup"><span data-stu-id="95628-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="95628-554">Номер паспорта [, который ищет типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95628-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95628-555">См. также</span><span class="sxs-lookup"><span data-stu-id="95628-555">See also</span></span>

[<span data-ttu-id="95628-556">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="95628-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

