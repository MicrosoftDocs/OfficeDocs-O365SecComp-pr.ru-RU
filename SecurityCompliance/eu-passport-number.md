---
title: Номер паспорта ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС Passport Number. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: c46f683bd1baf651bcf13c1766dfff3cb953b341
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218269"
---
# <a name="eu-passport-number"></a><span data-ttu-id="8665f-104">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="8665f-104">EU Passport Number</span></span>

<span data-ttu-id="8665f-p102">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС Passport Number. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="8665f-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="8665f-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="8665f-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="8665f-108">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-108">Format</span></span>

<span data-ttu-id="8665f-109">Одна буква, за которой следует необязательный пробел и семь цифр</span><span class="sxs-lookup"><span data-stu-id="8665f-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-110">Pattern</span></span>

<span data-ttu-id="8665f-111">Сочетание одной буквы, семи цифр и одного пробела:</span><span class="sxs-lookup"><span data-stu-id="8665f-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="8665f-112">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="8665f-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="8665f-113">Один пробел (необязательно)</span><span class="sxs-lookup"><span data-stu-id="8665f-113">One space (optional)</span></span>
    
- <span data-ttu-id="8665f-114">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8665f-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-115">Checksum</span></span>

<span data-ttu-id="8665f-116">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8665f-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-117">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-117">Definition</span></span>

<span data-ttu-id="8665f-118">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-119">Регулярное выражение `Regex_austria_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-120">Найдено ключевое `Keywords_austria_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-121">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-121">Keywords</span></span>

<span data-ttu-id="8665f-122">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-122"></span></span>
|<span data-ttu-id="8665f-123">**Кэйвордс_аустриа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-124">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-124">passport number</span></span>  <br/> <span data-ttu-id="8665f-125">Австрийский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-125">austrian passport number</span></span>  <br/> <span data-ttu-id="8665f-126">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-126">passport no</span></span>  <br/> <span data-ttu-id="8665f-127">reisepass</span><span class="sxs-lookup"><span data-stu-id="8665f-127">reisepass</span></span>  <br/> <span data-ttu-id="8665f-128">öстерреичисч реисепасс</span><span class="sxs-lookup"><span data-stu-id="8665f-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="8665f-129">Бельгия</span><span class="sxs-lookup"><span data-stu-id="8665f-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="8665f-130">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-130">Format</span></span>

<span data-ttu-id="8665f-131">Две буквы, за которыми следуют шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-132">Pattern</span></span>

<span data-ttu-id="8665f-133">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-134">Checksum</span></span>

<span data-ttu-id="8665f-135">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8665f-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-136">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-136">Definition</span></span>

<span data-ttu-id="8665f-137">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-138">Регулярное выражение `Regex_belgium_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-139">Найдено ключевое `Keywords_belgium_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-140">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-140">Keywords</span></span>

<span data-ttu-id="8665f-141">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-141"></span></span>
|<span data-ttu-id="8665f-142">**Кэйвордс_белгиум_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-143">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-143">passport number</span></span>  <br/> <span data-ttu-id="8665f-144">Бельгийский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-144">belgian passport number</span></span>  <br/> <span data-ttu-id="8665f-145">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-145">passport no</span></span>  <br/> <span data-ttu-id="8665f-146">паспурт</span><span class="sxs-lookup"><span data-stu-id="8665f-146">paspoort</span></span>  <br/> <span data-ttu-id="8665f-147">паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="8665f-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="8665f-148">реисепасс Кеин</span><span class="sxs-lookup"><span data-stu-id="8665f-148">reisepass kein</span></span>  <br/> <span data-ttu-id="8665f-149">reisepass</span><span class="sxs-lookup"><span data-stu-id="8665f-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="8665f-150">Болгария</span><span class="sxs-lookup"><span data-stu-id="8665f-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="8665f-151">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-151">Format</span></span>

<span data-ttu-id="8665f-152">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-153">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-153">Pattern</span></span>

 <span data-ttu-id="8665f-154">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8665f-155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-155">Checksum</span></span>

<span data-ttu-id="8665f-156">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-157">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-157">Definition</span></span>

<span data-ttu-id="8665f-158">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-159">Регулярное выражение `Regex_bulgaria_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-160">Найдено ключевое `Keywords_bulgaria_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-161">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-161">Keywords</span></span>

<span data-ttu-id="8665f-162">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-162"></span></span>
|<span data-ttu-id="8665f-163">**Кэйвордс_булгариа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-164">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-164">passport number</span></span>  <br/> <span data-ttu-id="8665f-165">номер паспорта для болгарского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="8665f-166">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-166">passport no</span></span>  <br/> <span data-ttu-id="8665f-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="8665f-168">Хорватия</span><span class="sxs-lookup"><span data-stu-id="8665f-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="8665f-169">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-169">Format</span></span>

<span data-ttu-id="8665f-170">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-171">Pattern</span></span>

 <span data-ttu-id="8665f-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8665f-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-173">Checksum</span></span>

<span data-ttu-id="8665f-174">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-175">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-175">Definition</span></span>

<span data-ttu-id="8665f-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-177">Регулярное выражение `Regex_croatia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-178">Найдено ключевое `Keywords_croatia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-179">Keywords</span></span>

<span data-ttu-id="8665f-180">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-180"></span></span>
|<span data-ttu-id="8665f-181">**Кэйвордс_кроатиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-182">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-182">passport number</span></span>  <br/> <span data-ttu-id="8665f-183">номер паспорта для хорватского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-183">croatian passport number</span></span>  <br/> <span data-ttu-id="8665f-184">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-184">passport no</span></span>  <br/> <span data-ttu-id="8665f-185">Брож путовнице</span><span class="sxs-lookup"><span data-stu-id="8665f-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="8665f-186">Кипр</span><span class="sxs-lookup"><span data-stu-id="8665f-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="8665f-187">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-187">Format</span></span>

<span data-ttu-id="8665f-188">Одна буква, за которой следуют 6-8 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-189">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-189">Pattern</span></span>

<span data-ttu-id="8665f-190">Одна буква, за которой следуют шесть и восемь цифр</span><span class="sxs-lookup"><span data-stu-id="8665f-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-191">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-191">Checksum</span></span>

<span data-ttu-id="8665f-192">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-193">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-193">Definition</span></span>

<span data-ttu-id="8665f-194">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-195">Регулярное выражение `Regex_cyprus_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-196">Найдено ключевое `Keywords_cyprus_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-197">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-197">Keywords</span></span>

<span data-ttu-id="8665f-198">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-198"></span></span>
|<span data-ttu-id="8665f-199">**Кэйвордс_ципрус_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-200">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-200">passport number</span></span>  <br/> <span data-ttu-id="8665f-201">номер паспорта для Кипр</span><span class="sxs-lookup"><span data-stu-id="8665f-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="8665f-202">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-202">passport no</span></span>  <br/> <span data-ttu-id="8665f-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="8665f-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="8665f-204">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="8665f-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="8665f-205">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-205">Format</span></span>

<span data-ttu-id="8665f-206">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-207">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-207">Pattern</span></span>

<span data-ttu-id="8665f-208">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-209">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-209">Checksum</span></span>

<span data-ttu-id="8665f-210">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-211">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-211">Definition</span></span>

<span data-ttu-id="8665f-212">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-213">Регулярное выражение `Regex_czech_republic_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-214">Найдено ключевое `Keywords_czech_republic_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-215">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-215">Keywords</span></span>

<span data-ttu-id="8665f-216">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-216"></span></span>
|<span data-ttu-id="8665f-217">**Кэйвордс_кзеч_републик_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-218">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-218">passport number</span></span>  <br/> <span data-ttu-id="8665f-219">номер паспорта для чешского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-219">czech passport number</span></span>  <br/> <span data-ttu-id="8665f-220">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-220">passport no</span></span>  <br/> <span data-ttu-id="8665f-221">цестовнí PAS</span><span class="sxs-lookup"><span data-stu-id="8665f-221">cestovní pas</span></span>  <br/> <span data-ttu-id="8665f-222">соответствующий</span><span class="sxs-lookup"><span data-stu-id="8665f-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="8665f-223">Дания</span><span class="sxs-lookup"><span data-stu-id="8665f-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="8665f-224">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-224">Format</span></span>

<span data-ttu-id="8665f-225">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-226">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-226">Pattern</span></span>

 <span data-ttu-id="8665f-227">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8665f-228">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-228">Checksum</span></span>

<span data-ttu-id="8665f-229">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-230">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-230">Definition</span></span>

<span data-ttu-id="8665f-231">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-232">Регулярное выражение `Regex_denmark_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-233">Найдено ключевое `Keywords_denmark_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-234">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-234">Keywords</span></span>

<span data-ttu-id="8665f-235">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-235"></span></span>
|<span data-ttu-id="8665f-236">**Кэйвордс_денмарк_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-237">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-237">passport number</span></span>  <br/> <span data-ttu-id="8665f-238">номер паспорта для датского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-238">danish passport number</span></span>  <br/> <span data-ttu-id="8665f-239">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-239">passport no</span></span>  <br/> <span data-ttu-id="8665f-240">соответствующий</span><span class="sxs-lookup"><span data-stu-id="8665f-240">pas</span></span>  <br/> <span data-ttu-id="8665f-241">паснуммер</span><span class="sxs-lookup"><span data-stu-id="8665f-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="8665f-242">Эстония</span><span class="sxs-lookup"><span data-stu-id="8665f-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="8665f-243">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-243">Format</span></span>

<span data-ttu-id="8665f-244">Одна буква, за которой следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-245">Pattern</span></span>

<span data-ttu-id="8665f-246">Одна буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-247">Checksum</span></span>

<span data-ttu-id="8665f-248">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-249">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-249">Definition</span></span>

<span data-ttu-id="8665f-250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-251">Регулярное выражение `Regex_estonia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-252">Найдено ключевое `Keywords_estonia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-253">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-253">Keywords</span></span>

<span data-ttu-id="8665f-254">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-254"></span></span>
|<span data-ttu-id="8665f-255">**Кэйвордс_естониа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-256">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-256">passport number</span></span>  <br/> <span data-ttu-id="8665f-257">номер паспорта для Эстонии</span><span class="sxs-lookup"><span data-stu-id="8665f-257">estonian passport number</span></span>  <br/> <span data-ttu-id="8665f-258">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-258">passport no</span></span>  <br/> <span data-ttu-id="8665f-259">Исти коданику Pass</span><span class="sxs-lookup"><span data-stu-id="8665f-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="8665f-260">Финляндия</span><span class="sxs-lookup"><span data-stu-id="8665f-260">Finland</span></span>

<span data-ttu-id="8665f-261">Дополнительные сведения можно найти в разделе "Финляндия Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8665f-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="8665f-262">Франция</span><span class="sxs-lookup"><span data-stu-id="8665f-262">France</span></span>

<span data-ttu-id="8665f-263">Дополнительные сведения можно найти в разделе "Франция Passport Number", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8665f-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="8665f-264">Германия</span><span class="sxs-lookup"><span data-stu-id="8665f-264">Germany</span></span>

<span data-ttu-id="8665f-265">Дополнительные сведения можно найти в разделе "Германия Passport Number", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8665f-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="8665f-266">Греция</span><span class="sxs-lookup"><span data-stu-id="8665f-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="8665f-267">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-267">Format</span></span>

<span data-ttu-id="8665f-268">Две буквы, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-269">Pattern</span></span>

<span data-ttu-id="8665f-270">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-271">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-271">Checksum</span></span>

<span data-ttu-id="8665f-272">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-273">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-273">Definition</span></span>

<span data-ttu-id="8665f-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-275">Регулярное выражение `Regex_greece_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-276">Найдено ключевое `Keywords_greece_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-277">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-277">Keywords</span></span>

<span data-ttu-id="8665f-278">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-278"></span></span>
|<span data-ttu-id="8665f-279">**Кэйвордс_грице_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-280">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-280">passport number</span></span>  <br/> <span data-ttu-id="8665f-281">номер паспорта греческого алфавита</span><span class="sxs-lookup"><span data-stu-id="8665f-281">greek passport number</span></span>  <br/> <span data-ttu-id="8665f-282">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-282">passport no</span></span>  <br/> <span data-ttu-id="8665f-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="8665f-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="8665f-284">Венгрия</span><span class="sxs-lookup"><span data-stu-id="8665f-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="8665f-285">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-285">Format</span></span>

<span data-ttu-id="8665f-286">Две буквы, за которыми следуют шесть или семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-287">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-287">Pattern</span></span>

<span data-ttu-id="8665f-288">Две буквы, за которыми следуют шесть или семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-289">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-289">Checksum</span></span>

<span data-ttu-id="8665f-290">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-291">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-291">Definition</span></span>

<span data-ttu-id="8665f-292">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-293">Регулярное выражение `Regex_hungary_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-294">Найдено ключевое `Keywords_hungary_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-295">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-295">Keywords</span></span>

<span data-ttu-id="8665f-296">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-296"></span></span>
|<span data-ttu-id="8665f-297">**Кэйвордс_хунгари_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-298">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-298">passport number</span></span>  <br/> <span data-ttu-id="8665f-299">Венгерский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="8665f-300">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-300">passport no</span></span>  <br/> <span data-ttu-id="8665f-301">úтлевéл сзáма</span><span class="sxs-lookup"><span data-stu-id="8665f-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="8665f-302">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="8665f-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="8665f-303">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-303">Format</span></span>

<span data-ttu-id="8665f-304">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-305">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-305">Pattern</span></span>

<span data-ttu-id="8665f-306">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="8665f-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="8665f-307">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="8665f-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="8665f-308">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8665f-309">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-309">Checksum</span></span>

<span data-ttu-id="8665f-310">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-311">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-311">Definition</span></span>

<span data-ttu-id="8665f-312">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-313">Регулярное выражение `Regex_ireland_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-314">Найдено ключевое `Keywords_ireland_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-315">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-315">Keywords</span></span>

<span data-ttu-id="8665f-316">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-316"></span></span>
|<span data-ttu-id="8665f-317">**Кэйвордс_иреланд_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-318">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-318">passport number</span></span>  <br/> <span data-ttu-id="8665f-319">Ирландский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-319">irish passport number</span></span>  <br/> <span data-ttu-id="8665f-320">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-320">passport no</span></span>  <br/> <span data-ttu-id="8665f-321">соответствующий</span><span class="sxs-lookup"><span data-stu-id="8665f-321">pas</span></span>  <br/> <span data-ttu-id="8665f-322">passport</span><span class="sxs-lookup"><span data-stu-id="8665f-322">passport</span></span>  <br/> <span data-ttu-id="8665f-323">пассепорт</span><span class="sxs-lookup"><span data-stu-id="8665f-323">passeport</span></span>  <br/> <span data-ttu-id="8665f-324">пассепорт нумеро</span><span class="sxs-lookup"><span data-stu-id="8665f-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="8665f-325">Италия</span><span class="sxs-lookup"><span data-stu-id="8665f-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="8665f-326">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-326">Format</span></span>

<span data-ttu-id="8665f-327">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-328">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-328">Pattern</span></span>

<span data-ttu-id="8665f-329">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="8665f-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="8665f-330">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="8665f-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="8665f-331">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8665f-332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-332">Checksum</span></span>

<span data-ttu-id="8665f-333">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8665f-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-334">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-334">Definition</span></span>

<span data-ttu-id="8665f-335">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-336">Регулярное выражение `Regex_italy_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-337">Найдено ключевое `Keywords_italy_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-338">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-338">Keywords</span></span>

<span data-ttu-id="8665f-339">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-339"></span></span>
|<span data-ttu-id="8665f-340">**Кэйвордс_итали_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-341">номер паспорта для итальянского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-341">italian passport number</span></span>  <br/> <span data-ttu-id="8665f-342">Репубблика итальянский пассапорто</span><span class="sxs-lookup"><span data-stu-id="8665f-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="8665f-343">пассапорто</span><span class="sxs-lookup"><span data-stu-id="8665f-343">passaporto</span></span>  <br/> <span data-ttu-id="8665f-344">пассапорто итальянский</span><span class="sxs-lookup"><span data-stu-id="8665f-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="8665f-345">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-345">passport number</span></span>  <br/> <span data-ttu-id="8665f-346">Итальянский пассапорто нумеро</span><span class="sxs-lookup"><span data-stu-id="8665f-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="8665f-347">пассапорто нумеро</span><span class="sxs-lookup"><span data-stu-id="8665f-347">passaporto numero</span></span>  <br/> <span data-ttu-id="8665f-348">нумéро пассепорт италиен</span><span class="sxs-lookup"><span data-stu-id="8665f-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="8665f-349">нумéро пассепорт</span><span class="sxs-lookup"><span data-stu-id="8665f-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="8665f-350">Латвия</span><span class="sxs-lookup"><span data-stu-id="8665f-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="8665f-351">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-351">Format</span></span>

<span data-ttu-id="8665f-352">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-353">Pattern</span></span>

<span data-ttu-id="8665f-354">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="8665f-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="8665f-355">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="8665f-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="8665f-356">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8665f-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-357">Checksum</span></span>

<span data-ttu-id="8665f-358">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-359">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-359">Definition</span></span>

<span data-ttu-id="8665f-360">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-361">Регулярное выражение `Regex_latvia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-362">Найдено ключевое `Keywords_latvia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-363">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-363">Keywords</span></span>

<span data-ttu-id="8665f-364">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-364"></span></span>
|<span data-ttu-id="8665f-365">**Кэйвордс_латвиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-366">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-366">passport number</span></span>  <br/> <span data-ttu-id="8665f-367">номер паспорта для Латвии</span><span class="sxs-lookup"><span data-stu-id="8665f-367">latvian passport number</span></span>  <br/> <span data-ttu-id="8665f-368">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-368">passport no</span></span>  <br/> <span data-ttu-id="8665f-369">ПАСЕ нумурс</span><span class="sxs-lookup"><span data-stu-id="8665f-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="8665f-370">Литва</span><span class="sxs-lookup"><span data-stu-id="8665f-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="8665f-371">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-371">Format</span></span>

<span data-ttu-id="8665f-372">Восемь цифр или букв без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-373">Pattern</span></span>

<span data-ttu-id="8665f-374">Восемь цифр или букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="8665f-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-375">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-375">Checksum</span></span>

<span data-ttu-id="8665f-376">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8665f-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-377">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-377">Definition</span></span>

<span data-ttu-id="8665f-378">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-379">Регулярное выражение `Regex_lithuania_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-380">Найдено ключевое `Keywords_lithuania_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-381">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-381">Keywords</span></span>

<span data-ttu-id="8665f-382">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-382"></span></span>
|<span data-ttu-id="8665f-383">**Кэйвордс_лисуаниа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-384">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-384">passport number</span></span>  <br/> <span data-ttu-id="8665f-385">номер паспорта лисуниан</span><span class="sxs-lookup"><span data-stu-id="8665f-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="8665f-386">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-386">passport no</span></span>  <br/> <span data-ttu-id="8665f-387">Пасо нумерис</span><span class="sxs-lookup"><span data-stu-id="8665f-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="8665f-388">Луксембург</span><span class="sxs-lookup"><span data-stu-id="8665f-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="8665f-389">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-389">Format</span></span>

<span data-ttu-id="8665f-390">Восемь цифр или букв без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-391">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-391">Pattern</span></span>

<span data-ttu-id="8665f-392">Восемь цифр или букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="8665f-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-393">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-393">Checksum</span></span>

<span data-ttu-id="8665f-394">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-395">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-395">Definition</span></span>

<span data-ttu-id="8665f-396">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-397">Регулярное выражение `Regex_nation_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-398">Найдено ключевое `Keywords_nation_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-399">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-399">Keywords</span></span>

<span data-ttu-id="8665f-400">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-400"></span></span>
|<span data-ttu-id="8665f-401">**Кэйвордс_натион_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-402">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-402">passport number</span></span>  <br/> <span data-ttu-id="8665f-403">номер паспорта для Латвии</span><span class="sxs-lookup"><span data-stu-id="8665f-403">latvian passport number</span></span>  <br/> <span data-ttu-id="8665f-404">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-404">passport no</span></span>  <br/> <span data-ttu-id="8665f-405">пасснуммер</span><span class="sxs-lookup"><span data-stu-id="8665f-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="8665f-406">Мальта</span><span class="sxs-lookup"><span data-stu-id="8665f-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="8665f-407">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-407">Format</span></span>

<span data-ttu-id="8665f-408">Семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-409">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-409">Pattern</span></span>

 <span data-ttu-id="8665f-410">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="8665f-411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-411">Checksum</span></span>

<span data-ttu-id="8665f-412">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-413">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-413">Definition</span></span>

<span data-ttu-id="8665f-414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-415">Регулярное выражение `Regex_malta_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-416">Найдено ключевое `Keywords_malta_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-417">Keywords</span></span>

<span data-ttu-id="8665f-418">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-418"></span></span>
|<span data-ttu-id="8665f-419">**Кэйвордс_малта_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-420">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-420">passport number</span></span>  <br/> <span data-ttu-id="8665f-421">номер паспорта Мальтийский</span><span class="sxs-lookup"><span data-stu-id="8665f-421">maltese passport number</span></span>  <br/> <span data-ttu-id="8665f-422">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-422">passport no</span></span>  <br/> <span data-ttu-id="8665f-423">нумру Тал — пассапорт</span><span class="sxs-lookup"><span data-stu-id="8665f-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="8665f-424">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="8665f-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="8665f-425">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-425">Format</span></span>

<span data-ttu-id="8665f-426">Девять букв или цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-427">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-427">Pattern</span></span>

<span data-ttu-id="8665f-428">Девять букв или цифр;</span><span class="sxs-lookup"><span data-stu-id="8665f-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-429">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-429">Checksum</span></span>

<span data-ttu-id="8665f-430">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8665f-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-431">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-431">Definition</span></span>

<span data-ttu-id="8665f-432">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-433">Регулярное выражение `Regex_netherlands_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-434">Найдено ключевое `Keywords_netherlands_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-435">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-435">Keywords</span></span>

<span data-ttu-id="8665f-436">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-436"></span></span>
|<span data-ttu-id="8665f-437">**Кэйвордс_несерландс_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-438">номер паспорта для нидерландского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-438">dutch passport number</span></span>  <br/> <span data-ttu-id="8665f-439">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-439">passport number</span></span>  <br/> <span data-ttu-id="8665f-440">номер паспорта Нидерландов</span><span class="sxs-lookup"><span data-stu-id="8665f-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="8665f-441">недерланден паспурт нуммер</span><span class="sxs-lookup"><span data-stu-id="8665f-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="8665f-442">паспурт</span><span class="sxs-lookup"><span data-stu-id="8665f-442">paspoort</span></span>  <br/> <span data-ttu-id="8665f-443">недерланден паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="8665f-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="8665f-444">паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="8665f-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="8665f-445">Польша</span><span class="sxs-lookup"><span data-stu-id="8665f-445">Poland</span></span>

<span data-ttu-id="8665f-446">Дополнительные сведения можно найти в разделе "Польша Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8665f-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="8665f-447">Португалия</span><span class="sxs-lookup"><span data-stu-id="8665f-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="8665f-448">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-448">Format</span></span>

<span data-ttu-id="8665f-449">Одна буква, за которой следуют шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-450">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-450">Pattern</span></span>

<span data-ttu-id="8665f-451">Одна буква, за которой следуют шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="8665f-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="8665f-452">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="8665f-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="8665f-453">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="8665f-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8665f-454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-454">Checksum</span></span>

<span data-ttu-id="8665f-455">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-456">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-456">Definition</span></span>

<span data-ttu-id="8665f-457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-458">Регулярное выражение `Regex_portugal_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-459">Найдено ключевое `Keywords_portugal_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-460">Keywords</span></span>

<span data-ttu-id="8665f-461">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-461"></span></span>
|<span data-ttu-id="8665f-462">**Кэйвордс_португал_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-463">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-463">passport number</span></span>  <br/> <span data-ttu-id="8665f-464">номер паспорта для португальского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="8665f-465">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-465">passport no</span></span>  <br/> <span data-ttu-id="8665f-466">нúмеро Do пассапорте</span><span class="sxs-lookup"><span data-stu-id="8665f-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="8665f-467">Румыния</span><span class="sxs-lookup"><span data-stu-id="8665f-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="8665f-468">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-468">Format</span></span>

<span data-ttu-id="8665f-469">Восемь или девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-470">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-470">Pattern</span></span>

<span data-ttu-id="8665f-471">Восемь или девять цифр</span><span class="sxs-lookup"><span data-stu-id="8665f-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-472">Checksum</span></span>

<span data-ttu-id="8665f-473">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-474">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-474">Definition</span></span>

<span data-ttu-id="8665f-475">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-476">Регулярное выражение `Regex_romania_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-477">Найдено ключевое `Keywords_romania_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-478">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-478">Keywords</span></span>

<span data-ttu-id="8665f-479">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-479"></span></span>
|<span data-ttu-id="8665f-480">**Кэйвордс_романиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-481">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-481">passport number</span></span>  <br/> <span data-ttu-id="8665f-482">номер паспорта для румынского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-482">romanian passport number</span></span>  <br/> <span data-ttu-id="8665f-483">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-483">passport no</span></span>  <br/> <span data-ttu-id="8665f-484">нумăрул паșапортулуи</span><span class="sxs-lookup"><span data-stu-id="8665f-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="8665f-485">Словакия</span><span class="sxs-lookup"><span data-stu-id="8665f-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="8665f-486">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-486">Format</span></span>

<span data-ttu-id="8665f-487">Одна цифра или буква, за которой следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-488">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-488">Pattern</span></span>

<span data-ttu-id="8665f-489">Одна цифра или буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="8665f-490">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-490">Checksum</span></span>

<span data-ttu-id="8665f-491">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-492">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-492">Definition</span></span>

<span data-ttu-id="8665f-493">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-494">Регулярное выражение `Regex_slovakia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-495">Найдено ключевое `Keywords_slovakia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-496">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-496">Keywords</span></span>

<span data-ttu-id="8665f-497">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-497"></span></span>
|<span data-ttu-id="8665f-498">**Кэйвордс_словакиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-499">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-499">passport number</span></span>  <br/> <span data-ttu-id="8665f-500">номер паспорта словакиан</span><span class="sxs-lookup"><span data-stu-id="8665f-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="8665f-501">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-501">passport no</span></span>  <br/> <span data-ttu-id="8665f-502">číсло Пасу</span><span class="sxs-lookup"><span data-stu-id="8665f-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="8665f-503">Словения</span><span class="sxs-lookup"><span data-stu-id="8665f-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="8665f-504">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-504">Format</span></span>

<span data-ttu-id="8665f-505">Две буквы, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-506">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-506">Pattern</span></span>

<span data-ttu-id="8665f-507">Две буквы, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="8665f-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="8665f-508">Буква "P"</span><span class="sxs-lookup"><span data-stu-id="8665f-508">The letter "P"</span></span>
    
- <span data-ttu-id="8665f-509">Одна прописная буква</span><span class="sxs-lookup"><span data-stu-id="8665f-509">One uppercase letter</span></span>
    
- <span data-ttu-id="8665f-510">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="8665f-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8665f-511">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-511">Checksum</span></span>

<span data-ttu-id="8665f-512">Нет</span><span class="sxs-lookup"><span data-stu-id="8665f-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-513">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-513">Definition</span></span>

<span data-ttu-id="8665f-514">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-515">Регулярное выражение `Regex_slovenia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-516">Найдено ключевое `Keywords_slovenia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-517">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-517">Keywords</span></span>

<span data-ttu-id="8665f-518">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-518"></span></span>
|<span data-ttu-id="8665f-519">**Кэйвордс_словениа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-520">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-520">passport number</span></span>  <br/> <span data-ttu-id="8665f-521">номер паспорта для словенского языка</span><span class="sxs-lookup"><span data-stu-id="8665f-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="8665f-522">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-522">passport no</span></span>  <br/> <span data-ttu-id="8665f-523">Список потнега šтевилка</span><span class="sxs-lookup"><span data-stu-id="8665f-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="8665f-524">Испания</span><span class="sxs-lookup"><span data-stu-id="8665f-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="8665f-525">Формат</span><span class="sxs-lookup"><span data-stu-id="8665f-525">Format</span></span>

<span data-ttu-id="8665f-526">Сочетание букв и цифр из восьми или девяти символов без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="8665f-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="8665f-527">Шаблон</span><span class="sxs-lookup"><span data-stu-id="8665f-527">Pattern</span></span>

<span data-ttu-id="8665f-528">Сочетание букв и цифр из восьми или девяти символов:</span><span class="sxs-lookup"><span data-stu-id="8665f-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="8665f-529">Две цифры или буквы</span><span class="sxs-lookup"><span data-stu-id="8665f-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="8665f-530">Одна цифра или буква (необязательно)</span><span class="sxs-lookup"><span data-stu-id="8665f-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="8665f-531">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="8665f-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="8665f-532">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="8665f-532">Checksum</span></span>

<span data-ttu-id="8665f-533">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="8665f-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="8665f-534">Определение</span><span class="sxs-lookup"><span data-stu-id="8665f-534">Definition</span></span>

<span data-ttu-id="8665f-535">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="8665f-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="8665f-536">Регулярное выражение `Regex_spain_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="8665f-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="8665f-537">Найдено ключевое `Keywords_spain_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="8665f-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="8665f-538">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="8665f-538">Keywords</span></span>

<span data-ttu-id="8665f-539">| |</span><span class="sxs-lookup"><span data-stu-id="8665f-539"></span></span>
|<span data-ttu-id="8665f-540">**Кэйвордс_спаин_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="8665f-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="8665f-541">passport</span><span class="sxs-lookup"><span data-stu-id="8665f-541">passport</span></span>  <br/> <span data-ttu-id="8665f-542">Служба Passport, Испания</span><span class="sxs-lookup"><span data-stu-id="8665f-542">spain passport</span></span>  <br/> <span data-ttu-id="8665f-543">Книга Passport</span><span class="sxs-lookup"><span data-stu-id="8665f-543">passport book</span></span>  <br/> <span data-ttu-id="8665f-544">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="8665f-544">passport number</span></span>  <br/> <span data-ttu-id="8665f-545">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="8665f-545">passport no</span></span>  <br/> <span data-ttu-id="8665f-546">либрета пасапорте</span><span class="sxs-lookup"><span data-stu-id="8665f-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="8665f-547">нúмеро пасапорте</span><span class="sxs-lookup"><span data-stu-id="8665f-547">número pasaporte</span></span>  <br/> <span data-ttu-id="8665f-548">еспаñа пасапорте</span><span class="sxs-lookup"><span data-stu-id="8665f-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="8665f-549">пасапорте</span><span class="sxs-lookup"><span data-stu-id="8665f-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="8665f-550">Швеция</span><span class="sxs-lookup"><span data-stu-id="8665f-550">Sweden</span></span>

<span data-ttu-id="8665f-551">Дополнительные сведения можно найти в разделе "Швеции Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8665f-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="8665f-552">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="8665f-552">UK</span></span>

<span data-ttu-id="8665f-p103">Дополнительные сведения можно найти в разделе "номер паспорта США/Великобритания", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="8665f-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8665f-555">См. также</span><span class="sxs-lookup"><span data-stu-id="8665f-555">See also</span></span>

[<span data-ttu-id="8665f-556">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="8665f-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

