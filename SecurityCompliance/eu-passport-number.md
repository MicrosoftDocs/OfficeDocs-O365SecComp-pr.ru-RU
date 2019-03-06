---
title: Номер паспорта ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС Passport Number. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: 3ab92e87607f41cffa8c15f1179a4eef5369cb29
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410934"
---
# <a name="eu-passport-number"></a><span data-ttu-id="55da0-104">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="55da0-104">EU Passport Number</span></span>

<span data-ttu-id="55da0-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС Passport Number.</span><span class="sxs-lookup"><span data-stu-id="55da0-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="55da0-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="55da0-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="55da0-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="55da0-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="55da0-108">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-108">Format</span></span>

<span data-ttu-id="55da0-109">Одна буква, за которой следует необязательный пробел и семь цифр</span><span class="sxs-lookup"><span data-stu-id="55da0-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-110">Pattern</span></span>

<span data-ttu-id="55da0-111">Сочетание одной буквы, семи цифр и одного пробела:</span><span class="sxs-lookup"><span data-stu-id="55da0-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="55da0-112">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="55da0-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="55da0-113">Один пробел (необязательно)</span><span class="sxs-lookup"><span data-stu-id="55da0-113">One space (optional)</span></span>
    
- <span data-ttu-id="55da0-114">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="55da0-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-115">Checksum</span></span>

<span data-ttu-id="55da0-116">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="55da0-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-117">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-117">Definition</span></span>

<span data-ttu-id="55da0-118">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-119">Регулярное выражение `Regex_austria_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-120">Найдено ключевое `Keywords_austria_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-121">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-121">Keywords</span></span>

<span data-ttu-id="55da0-122">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-122"></span></span>
|<span data-ttu-id="55da0-123">**Кэйвордс_аустриа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-124">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-124">passport number</span></span>  <br/> <span data-ttu-id="55da0-125">Австрийский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="55da0-125">austrian passport number</span></span>  <br/> <span data-ttu-id="55da0-126">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-126">passport no</span></span>  <br/> <span data-ttu-id="55da0-127">реисепасс</span><span class="sxs-lookup"><span data-stu-id="55da0-127">reisepass</span></span>  <br/> <span data-ttu-id="55da0-128">öстерреичисч реисепасс</span><span class="sxs-lookup"><span data-stu-id="55da0-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="55da0-129">Бельгия</span><span class="sxs-lookup"><span data-stu-id="55da0-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="55da0-130">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-130">Format</span></span>

<span data-ttu-id="55da0-131">Две буквы, за которыми следуют шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-132">Pattern</span></span>

<span data-ttu-id="55da0-133">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-134">Checksum</span></span>

<span data-ttu-id="55da0-135">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="55da0-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-136">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-136">Definition</span></span>

<span data-ttu-id="55da0-137">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-138">Регулярное выражение `Regex_belgium_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-139">Найдено ключевое `Keywords_belgium_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-140">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-140">Keywords</span></span>

<span data-ttu-id="55da0-141">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-141"></span></span>
|<span data-ttu-id="55da0-142">**Кэйвордс_белгиум_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-143">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-143">passport number</span></span>  <br/> <span data-ttu-id="55da0-144">Бельгийский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="55da0-144">belgian passport number</span></span>  <br/> <span data-ttu-id="55da0-145">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-145">passport no</span></span>  <br/> <span data-ttu-id="55da0-146">паспурт</span><span class="sxs-lookup"><span data-stu-id="55da0-146">paspoort</span></span>  <br/> <span data-ttu-id="55da0-147">паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="55da0-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="55da0-148">реисепасс Кеин</span><span class="sxs-lookup"><span data-stu-id="55da0-148">reisepass kein</span></span>  <br/> <span data-ttu-id="55da0-149">реисепасс</span><span class="sxs-lookup"><span data-stu-id="55da0-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="55da0-150">Болгария</span><span class="sxs-lookup"><span data-stu-id="55da0-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="55da0-151">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-151">Format</span></span>

<span data-ttu-id="55da0-152">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-153">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-153">Pattern</span></span>

 <span data-ttu-id="55da0-154">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="55da0-155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-155">Checksum</span></span>

<span data-ttu-id="55da0-156">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-157">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-157">Definition</span></span>

<span data-ttu-id="55da0-158">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-159">Регулярное выражение `Regex_bulgaria_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-160">Найдено ключевое `Keywords_bulgaria_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-161">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-161">Keywords</span></span>

<span data-ttu-id="55da0-162">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-162"></span></span>
|<span data-ttu-id="55da0-163">**Кэйвордс_булгариа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-164">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-164">passport number</span></span>  <br/> <span data-ttu-id="55da0-165">номер паспорта для болгарского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="55da0-166">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-166">passport no</span></span>  <br/> <span data-ttu-id="55da0-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="55da0-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="55da0-168">Хорватия</span><span class="sxs-lookup"><span data-stu-id="55da0-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="55da0-169">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-169">Format</span></span>

<span data-ttu-id="55da0-170">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-171">Pattern</span></span>

 <span data-ttu-id="55da0-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="55da0-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-173">Checksum</span></span>

<span data-ttu-id="55da0-174">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-175">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-175">Definition</span></span>

<span data-ttu-id="55da0-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-177">Регулярное выражение `Regex_croatia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-178">Найдено ключевое `Keywords_croatia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-179">Keywords</span></span>

<span data-ttu-id="55da0-180">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-180"></span></span>
|<span data-ttu-id="55da0-181">**Кэйвордс_кроатиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-182">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-182">passport number</span></span>  <br/> <span data-ttu-id="55da0-183">номер паспорта для хорватского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-183">croatian passport number</span></span>  <br/> <span data-ttu-id="55da0-184">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-184">passport no</span></span>  <br/> <span data-ttu-id="55da0-185">Брож путовнице</span><span class="sxs-lookup"><span data-stu-id="55da0-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="55da0-186">Кипр</span><span class="sxs-lookup"><span data-stu-id="55da0-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="55da0-187">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-187">Format</span></span>

<span data-ttu-id="55da0-188">Одна буква, за которой следуют 6-8 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-189">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-189">Pattern</span></span>

<span data-ttu-id="55da0-190">Одна буква, за которой следуют шесть и восемь цифр</span><span class="sxs-lookup"><span data-stu-id="55da0-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-191">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-191">Checksum</span></span>

<span data-ttu-id="55da0-192">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-193">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-193">Definition</span></span>

<span data-ttu-id="55da0-194">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-195">Регулярное выражение `Regex_cyprus_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-196">Найдено ключевое `Keywords_cyprus_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-197">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-197">Keywords</span></span>

<span data-ttu-id="55da0-198">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-198"></span></span>
|<span data-ttu-id="55da0-199">**Кэйвордс_ципрус_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-200">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-200">passport number</span></span>  <br/> <span data-ttu-id="55da0-201">номер паспорта для Кипр</span><span class="sxs-lookup"><span data-stu-id="55da0-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="55da0-202">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-202">passport no</span></span>  <br/> <span data-ttu-id="55da0-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="55da0-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="55da0-204">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="55da0-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="55da0-205">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-205">Format</span></span>

<span data-ttu-id="55da0-206">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-207">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-207">Pattern</span></span>

<span data-ttu-id="55da0-208">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-209">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-209">Checksum</span></span>

<span data-ttu-id="55da0-210">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-211">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-211">Definition</span></span>

<span data-ttu-id="55da0-212">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-213">Регулярное выражение `Regex_czech_republic_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-214">Найдено ключевое `Keywords_czech_republic_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-215">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-215">Keywords</span></span>

<span data-ttu-id="55da0-216">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-216"></span></span>
|<span data-ttu-id="55da0-217">**Кэйвордс_кзеч_републик_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-218">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-218">passport number</span></span>  <br/> <span data-ttu-id="55da0-219">номер паспорта для чешского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-219">czech passport number</span></span>  <br/> <span data-ttu-id="55da0-220">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-220">passport no</span></span>  <br/> <span data-ttu-id="55da0-221">цестовнí PAS</span><span class="sxs-lookup"><span data-stu-id="55da0-221">cestovní pas</span></span>  <br/> <span data-ttu-id="55da0-222">соответствующий</span><span class="sxs-lookup"><span data-stu-id="55da0-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="55da0-223">Дания</span><span class="sxs-lookup"><span data-stu-id="55da0-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="55da0-224">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-224">Format</span></span>

<span data-ttu-id="55da0-225">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-226">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-226">Pattern</span></span>

 <span data-ttu-id="55da0-227">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="55da0-228">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-228">Checksum</span></span>

<span data-ttu-id="55da0-229">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-230">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-230">Definition</span></span>

<span data-ttu-id="55da0-231">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-232">Регулярное выражение `Regex_denmark_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-233">Найдено ключевое `Keywords_denmark_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-234">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-234">Keywords</span></span>

<span data-ttu-id="55da0-235">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-235"></span></span>
|<span data-ttu-id="55da0-236">**Кэйвордс_денмарк_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-237">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-237">passport number</span></span>  <br/> <span data-ttu-id="55da0-238">номер паспорта для датского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-238">danish passport number</span></span>  <br/> <span data-ttu-id="55da0-239">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-239">passport no</span></span>  <br/> <span data-ttu-id="55da0-240">соответствующий</span><span class="sxs-lookup"><span data-stu-id="55da0-240">pas</span></span>  <br/> <span data-ttu-id="55da0-241">паснуммер</span><span class="sxs-lookup"><span data-stu-id="55da0-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="55da0-242">Эстония</span><span class="sxs-lookup"><span data-stu-id="55da0-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="55da0-243">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-243">Format</span></span>

<span data-ttu-id="55da0-244">Одна буква, за которой следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-245">Pattern</span></span>

<span data-ttu-id="55da0-246">Одна буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-247">Checksum</span></span>

<span data-ttu-id="55da0-248">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-249">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-249">Definition</span></span>

<span data-ttu-id="55da0-250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-251">Регулярное выражение `Regex_estonia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-252">Найдено ключевое `Keywords_estonia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-253">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-253">Keywords</span></span>

<span data-ttu-id="55da0-254">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-254"></span></span>
|<span data-ttu-id="55da0-255">**Кэйвордс_естониа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-256">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-256">passport number</span></span>  <br/> <span data-ttu-id="55da0-257">номер паспорта для Эстонии</span><span class="sxs-lookup"><span data-stu-id="55da0-257">estonian passport number</span></span>  <br/> <span data-ttu-id="55da0-258">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-258">passport no</span></span>  <br/> <span data-ttu-id="55da0-259">Исти коданику Pass</span><span class="sxs-lookup"><span data-stu-id="55da0-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="55da0-260">Финляндия</span><span class="sxs-lookup"><span data-stu-id="55da0-260">Finland</span></span>

<span data-ttu-id="55da0-261">Дополнительные сведения можно найти в разделе "Финляндия Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="55da0-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="55da0-262">Франция</span><span class="sxs-lookup"><span data-stu-id="55da0-262">France</span></span>

<span data-ttu-id="55da0-263">Дополнительные сведения можно найти в разделе "Франция Passport Number", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="55da0-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="55da0-264">Германия</span><span class="sxs-lookup"><span data-stu-id="55da0-264">Germany</span></span>

<span data-ttu-id="55da0-265">Дополнительные сведения можно найти в разделе "Германия Passport Number", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="55da0-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="55da0-266">Греция</span><span class="sxs-lookup"><span data-stu-id="55da0-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="55da0-267">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-267">Format</span></span>

<span data-ttu-id="55da0-268">Две буквы, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-269">Pattern</span></span>

<span data-ttu-id="55da0-270">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-271">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-271">Checksum</span></span>

<span data-ttu-id="55da0-272">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-273">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-273">Definition</span></span>

<span data-ttu-id="55da0-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-275">Регулярное выражение `Regex_greece_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-276">Найдено ключевое `Keywords_greece_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-277">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-277">Keywords</span></span>

<span data-ttu-id="55da0-278">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-278"></span></span>
|<span data-ttu-id="55da0-279">**Кэйвордс_грице_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-280">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-280">passport number</span></span>  <br/> <span data-ttu-id="55da0-281">номер паспорта греческого алфавита</span><span class="sxs-lookup"><span data-stu-id="55da0-281">greek passport number</span></span>  <br/> <span data-ttu-id="55da0-282">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-282">passport no</span></span>  <br/> <span data-ttu-id="55da0-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="55da0-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="55da0-284">Венгрия</span><span class="sxs-lookup"><span data-stu-id="55da0-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="55da0-285">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-285">Format</span></span>

<span data-ttu-id="55da0-286">Две буквы, за которыми следуют шесть или семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-287">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-287">Pattern</span></span>

<span data-ttu-id="55da0-288">Две буквы, за которыми следуют шесть или семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-289">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-289">Checksum</span></span>

<span data-ttu-id="55da0-290">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-291">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-291">Definition</span></span>

<span data-ttu-id="55da0-292">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-293">Регулярное выражение `Regex_hungary_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-294">Найдено ключевое `Keywords_hungary_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-295">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-295">Keywords</span></span>

<span data-ttu-id="55da0-296">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-296"></span></span>
|<span data-ttu-id="55da0-297">**Кэйвордс_хунгари_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-298">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-298">passport number</span></span>  <br/> <span data-ttu-id="55da0-299">Венгерский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="55da0-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="55da0-300">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-300">passport no</span></span>  <br/> <span data-ttu-id="55da0-301">úтлевéл сзáма</span><span class="sxs-lookup"><span data-stu-id="55da0-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="55da0-302">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="55da0-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="55da0-303">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-303">Format</span></span>

<span data-ttu-id="55da0-304">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-305">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-305">Pattern</span></span>

<span data-ttu-id="55da0-306">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="55da0-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="55da0-307">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="55da0-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="55da0-308">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="55da0-309">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-309">Checksum</span></span>

<span data-ttu-id="55da0-310">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-311">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-311">Definition</span></span>

<span data-ttu-id="55da0-312">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-313">Регулярное выражение `Regex_ireland_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-314">Найдено ключевое `Keywords_ireland_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-315">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-315">Keywords</span></span>

<span data-ttu-id="55da0-316">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-316"></span></span>
|<span data-ttu-id="55da0-317">**Кэйвордс_иреланд_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-318">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-318">passport number</span></span>  <br/> <span data-ttu-id="55da0-319">Ирландский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="55da0-319">irish passport number</span></span>  <br/> <span data-ttu-id="55da0-320">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-320">passport no</span></span>  <br/> <span data-ttu-id="55da0-321">соответствующий</span><span class="sxs-lookup"><span data-stu-id="55da0-321">pas</span></span>  <br/> <span data-ttu-id="55da0-322">службу</span><span class="sxs-lookup"><span data-stu-id="55da0-322">passport</span></span>  <br/> <span data-ttu-id="55da0-323">пассепорт</span><span class="sxs-lookup"><span data-stu-id="55da0-323">passeport</span></span>  <br/> <span data-ttu-id="55da0-324">пассепорт нумеро</span><span class="sxs-lookup"><span data-stu-id="55da0-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="55da0-325">Италия</span><span class="sxs-lookup"><span data-stu-id="55da0-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="55da0-326">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-326">Format</span></span>

<span data-ttu-id="55da0-327">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-328">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-328">Pattern</span></span>

<span data-ttu-id="55da0-329">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="55da0-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="55da0-330">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="55da0-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="55da0-331">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="55da0-332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-332">Checksum</span></span>

<span data-ttu-id="55da0-333">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="55da0-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-334">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-334">Definition</span></span>

<span data-ttu-id="55da0-335">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-336">Регулярное выражение `Regex_italy_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-337">Найдено ключевое `Keywords_italy_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-338">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-338">Keywords</span></span>

<span data-ttu-id="55da0-339">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-339"></span></span>
|<span data-ttu-id="55da0-340">**Кэйвордс_итали_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-341">номер паспорта для итальянского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-341">italian passport number</span></span>  <br/> <span data-ttu-id="55da0-342">Репубблика итальянский пассапорто</span><span class="sxs-lookup"><span data-stu-id="55da0-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="55da0-343">пассапорто</span><span class="sxs-lookup"><span data-stu-id="55da0-343">passaporto</span></span>  <br/> <span data-ttu-id="55da0-344">пассапорто итальянский</span><span class="sxs-lookup"><span data-stu-id="55da0-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="55da0-345">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-345">passport number</span></span>  <br/> <span data-ttu-id="55da0-346">Итальянский пассапорто нумеро</span><span class="sxs-lookup"><span data-stu-id="55da0-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="55da0-347">пассапорто нумеро</span><span class="sxs-lookup"><span data-stu-id="55da0-347">passaporto numero</span></span>  <br/> <span data-ttu-id="55da0-348">нумéро пассепорт италиен</span><span class="sxs-lookup"><span data-stu-id="55da0-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="55da0-349">нумéро пассепорт</span><span class="sxs-lookup"><span data-stu-id="55da0-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="55da0-350">Латвия</span><span class="sxs-lookup"><span data-stu-id="55da0-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="55da0-351">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-351">Format</span></span>

<span data-ttu-id="55da0-352">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-353">Pattern</span></span>

<span data-ttu-id="55da0-354">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="55da0-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="55da0-355">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="55da0-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="55da0-356">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="55da0-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-357">Checksum</span></span>

<span data-ttu-id="55da0-358">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-359">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-359">Definition</span></span>

<span data-ttu-id="55da0-360">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-361">Регулярное выражение `Regex_latvia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-362">Найдено ключевое `Keywords_latvia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-363">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-363">Keywords</span></span>

<span data-ttu-id="55da0-364">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-364"></span></span>
|<span data-ttu-id="55da0-365">**Кэйвордс_латвиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-366">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-366">passport number</span></span>  <br/> <span data-ttu-id="55da0-367">номер паспорта для Латвии</span><span class="sxs-lookup"><span data-stu-id="55da0-367">latvian passport number</span></span>  <br/> <span data-ttu-id="55da0-368">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-368">passport no</span></span>  <br/> <span data-ttu-id="55da0-369">ПАСЕ нумурс</span><span class="sxs-lookup"><span data-stu-id="55da0-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="55da0-370">Литва</span><span class="sxs-lookup"><span data-stu-id="55da0-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="55da0-371">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-371">Format</span></span>

<span data-ttu-id="55da0-372">Восемь цифр или букв без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-373">Pattern</span></span>

<span data-ttu-id="55da0-374">Восемь цифр или букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="55da0-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-375">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-375">Checksum</span></span>

<span data-ttu-id="55da0-376">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="55da0-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-377">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-377">Definition</span></span>

<span data-ttu-id="55da0-378">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-379">Регулярное выражение `Regex_lithuania_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-380">Найдено ключевое `Keywords_lithuania_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-381">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-381">Keywords</span></span>

<span data-ttu-id="55da0-382">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-382"></span></span>
|<span data-ttu-id="55da0-383">**Кэйвордс_лисуаниа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-384">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-384">passport number</span></span>  <br/> <span data-ttu-id="55da0-385">номер паспорта лисуниан</span><span class="sxs-lookup"><span data-stu-id="55da0-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="55da0-386">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-386">passport no</span></span>  <br/> <span data-ttu-id="55da0-387">Пасо нумерис</span><span class="sxs-lookup"><span data-stu-id="55da0-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="55da0-388">Луксембург</span><span class="sxs-lookup"><span data-stu-id="55da0-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="55da0-389">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-389">Format</span></span>

<span data-ttu-id="55da0-390">Восемь цифр или букв без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-391">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-391">Pattern</span></span>

<span data-ttu-id="55da0-392">Восемь цифр или букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="55da0-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-393">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-393">Checksum</span></span>

<span data-ttu-id="55da0-394">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-395">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-395">Definition</span></span>

<span data-ttu-id="55da0-396">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-397">Регулярное выражение `Regex_nation_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-398">Найдено ключевое `Keywords_nation_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-399">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-399">Keywords</span></span>

<span data-ttu-id="55da0-400">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-400"></span></span>
|<span data-ttu-id="55da0-401">**Кэйвордс_натион_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-402">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-402">passport number</span></span>  <br/> <span data-ttu-id="55da0-403">номер паспорта для Латвии</span><span class="sxs-lookup"><span data-stu-id="55da0-403">latvian passport number</span></span>  <br/> <span data-ttu-id="55da0-404">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-404">passport no</span></span>  <br/> <span data-ttu-id="55da0-405">пасснуммер</span><span class="sxs-lookup"><span data-stu-id="55da0-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="55da0-406">Мальта</span><span class="sxs-lookup"><span data-stu-id="55da0-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="55da0-407">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-407">Format</span></span>

<span data-ttu-id="55da0-408">Семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-409">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-409">Pattern</span></span>

 <span data-ttu-id="55da0-410">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="55da0-411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-411">Checksum</span></span>

<span data-ttu-id="55da0-412">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-413">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-413">Definition</span></span>

<span data-ttu-id="55da0-414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-415">Регулярное выражение `Regex_malta_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-416">Найдено ключевое `Keywords_malta_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-417">Keywords</span></span>

<span data-ttu-id="55da0-418">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-418"></span></span>
|<span data-ttu-id="55da0-419">**Кэйвордс_малта_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-420">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-420">passport number</span></span>  <br/> <span data-ttu-id="55da0-421">номер паспорта Мальтийский</span><span class="sxs-lookup"><span data-stu-id="55da0-421">maltese passport number</span></span>  <br/> <span data-ttu-id="55da0-422">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-422">passport no</span></span>  <br/> <span data-ttu-id="55da0-423">нумру Тал — пассапорт</span><span class="sxs-lookup"><span data-stu-id="55da0-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="55da0-424">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="55da0-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="55da0-425">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-425">Format</span></span>

<span data-ttu-id="55da0-426">Девять букв или цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-427">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-427">Pattern</span></span>

<span data-ttu-id="55da0-428">Девять букв или цифр;</span><span class="sxs-lookup"><span data-stu-id="55da0-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-429">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-429">Checksum</span></span>

<span data-ttu-id="55da0-430">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="55da0-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-431">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-431">Definition</span></span>

<span data-ttu-id="55da0-432">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-433">Регулярное выражение `Regex_netherlands_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-434">Найдено ключевое `Keywords_netherlands_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-435">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-435">Keywords</span></span>

<span data-ttu-id="55da0-436">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-436"></span></span>
|<span data-ttu-id="55da0-437">**Кэйвордс_несерландс_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-438">номер паспорта для нидерландского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-438">dutch passport number</span></span>  <br/> <span data-ttu-id="55da0-439">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-439">passport number</span></span>  <br/> <span data-ttu-id="55da0-440">номер паспорта Нидерландов</span><span class="sxs-lookup"><span data-stu-id="55da0-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="55da0-441">недерланден паспурт нуммер</span><span class="sxs-lookup"><span data-stu-id="55da0-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="55da0-442">паспурт</span><span class="sxs-lookup"><span data-stu-id="55da0-442">paspoort</span></span>  <br/> <span data-ttu-id="55da0-443">недерланден паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="55da0-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="55da0-444">паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="55da0-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="55da0-445">Польша</span><span class="sxs-lookup"><span data-stu-id="55da0-445">Poland</span></span>

<span data-ttu-id="55da0-446">Дополнительные сведения можно найти в разделе "Польша Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="55da0-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="55da0-447">Португалия</span><span class="sxs-lookup"><span data-stu-id="55da0-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="55da0-448">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-448">Format</span></span>

<span data-ttu-id="55da0-449">Одна буква, за которой следуют шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-450">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-450">Pattern</span></span>

<span data-ttu-id="55da0-451">Одна буква, за которой следуют шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="55da0-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="55da0-452">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="55da0-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="55da0-453">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="55da0-454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-454">Checksum</span></span>

<span data-ttu-id="55da0-455">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-456">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-456">Definition</span></span>

<span data-ttu-id="55da0-457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-458">Регулярное выражение `Regex_portugal_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-459">Найдено ключевое `Keywords_portugal_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-460">Keywords</span></span>

<span data-ttu-id="55da0-461">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-461"></span></span>
|<span data-ttu-id="55da0-462">**Кэйвордс_португал_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-463">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-463">passport number</span></span>  <br/> <span data-ttu-id="55da0-464">номер паспорта для португальского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="55da0-465">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-465">passport no</span></span>  <br/> <span data-ttu-id="55da0-466">нúмеро Do пассапорте</span><span class="sxs-lookup"><span data-stu-id="55da0-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="55da0-467">Румыния</span><span class="sxs-lookup"><span data-stu-id="55da0-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="55da0-468">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-468">Format</span></span>

<span data-ttu-id="55da0-469">Восемь или девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-470">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-470">Pattern</span></span>

<span data-ttu-id="55da0-471">Восемь или девять цифр</span><span class="sxs-lookup"><span data-stu-id="55da0-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-472">Checksum</span></span>

<span data-ttu-id="55da0-473">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-474">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-474">Definition</span></span>

<span data-ttu-id="55da0-475">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-476">Регулярное выражение `Regex_romania_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-477">Найдено ключевое `Keywords_romania_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-478">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-478">Keywords</span></span>

<span data-ttu-id="55da0-479">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-479"></span></span>
|<span data-ttu-id="55da0-480">**Кэйвордс_романиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-481">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-481">passport number</span></span>  <br/> <span data-ttu-id="55da0-482">номер паспорта для румынского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-482">romanian passport number</span></span>  <br/> <span data-ttu-id="55da0-483">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-483">passport no</span></span>  <br/> <span data-ttu-id="55da0-484">нумăрул паșапортулуи</span><span class="sxs-lookup"><span data-stu-id="55da0-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="55da0-485">Словакия</span><span class="sxs-lookup"><span data-stu-id="55da0-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="55da0-486">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-486">Format</span></span>

<span data-ttu-id="55da0-487">Одна цифра или буква, за которой следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-488">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-488">Pattern</span></span>

<span data-ttu-id="55da0-489">Одна цифра или буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="55da0-490">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-490">Checksum</span></span>

<span data-ttu-id="55da0-491">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-492">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-492">Definition</span></span>

<span data-ttu-id="55da0-493">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-494">Регулярное выражение `Regex_slovakia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-495">Найдено ключевое `Keywords_slovakia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-496">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-496">Keywords</span></span>

<span data-ttu-id="55da0-497">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-497"></span></span>
|<span data-ttu-id="55da0-498">**Кэйвордс_словакиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-499">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-499">passport number</span></span>  <br/> <span data-ttu-id="55da0-500">номер паспорта словакиан</span><span class="sxs-lookup"><span data-stu-id="55da0-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="55da0-501">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-501">passport no</span></span>  <br/> <span data-ttu-id="55da0-502">číсло Пасу</span><span class="sxs-lookup"><span data-stu-id="55da0-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="55da0-503">Словения</span><span class="sxs-lookup"><span data-stu-id="55da0-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="55da0-504">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-504">Format</span></span>

<span data-ttu-id="55da0-505">Две буквы, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-506">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-506">Pattern</span></span>

<span data-ttu-id="55da0-507">Две буквы, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="55da0-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="55da0-508">Буква "P"</span><span class="sxs-lookup"><span data-stu-id="55da0-508">The letter "P"</span></span>
    
- <span data-ttu-id="55da0-509">Одна прописная буква</span><span class="sxs-lookup"><span data-stu-id="55da0-509">One uppercase letter</span></span>
    
- <span data-ttu-id="55da0-510">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="55da0-511">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-511">Checksum</span></span>

<span data-ttu-id="55da0-512">Нет</span><span class="sxs-lookup"><span data-stu-id="55da0-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-513">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-513">Definition</span></span>

<span data-ttu-id="55da0-514">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-515">Регулярное выражение `Regex_slovenia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-516">Найдено ключевое `Keywords_slovenia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-517">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-517">Keywords</span></span>

<span data-ttu-id="55da0-518">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-518"></span></span>
|<span data-ttu-id="55da0-519">**Кэйвордс_словениа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-520">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-520">passport number</span></span>  <br/> <span data-ttu-id="55da0-521">номер паспорта для словенского языка</span><span class="sxs-lookup"><span data-stu-id="55da0-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="55da0-522">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-522">passport no</span></span>  <br/> <span data-ttu-id="55da0-523">Список потнега šтевилка</span><span class="sxs-lookup"><span data-stu-id="55da0-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="55da0-524">Испания</span><span class="sxs-lookup"><span data-stu-id="55da0-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="55da0-525">Format</span><span class="sxs-lookup"><span data-stu-id="55da0-525">Format</span></span>

<span data-ttu-id="55da0-526">Сочетание букв и цифр из восьми или девяти символов без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="55da0-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="55da0-527">Шаблон</span><span class="sxs-lookup"><span data-stu-id="55da0-527">Pattern</span></span>

<span data-ttu-id="55da0-528">Сочетание букв и цифр из восьми или девяти символов:</span><span class="sxs-lookup"><span data-stu-id="55da0-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="55da0-529">Две цифры или буквы</span><span class="sxs-lookup"><span data-stu-id="55da0-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="55da0-530">Одна цифра или буква (необязательно)</span><span class="sxs-lookup"><span data-stu-id="55da0-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="55da0-531">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="55da0-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="55da0-532">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="55da0-532">Checksum</span></span>

<span data-ttu-id="55da0-533">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="55da0-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="55da0-534">Определение</span><span class="sxs-lookup"><span data-stu-id="55da0-534">Definition</span></span>

<span data-ttu-id="55da0-535">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="55da0-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="55da0-536">Регулярное выражение `Regex_spain_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="55da0-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="55da0-537">Найдено ключевое `Keywords_spain_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="55da0-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="55da0-538">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="55da0-538">Keywords</span></span>

<span data-ttu-id="55da0-539">| |</span><span class="sxs-lookup"><span data-stu-id="55da0-539"></span></span>
|<span data-ttu-id="55da0-540">**Кэйвордс_спаин_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="55da0-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="55da0-541">службу</span><span class="sxs-lookup"><span data-stu-id="55da0-541">passport</span></span>  <br/> <span data-ttu-id="55da0-542">Служба Passport, Испания</span><span class="sxs-lookup"><span data-stu-id="55da0-542">spain passport</span></span>  <br/> <span data-ttu-id="55da0-543">Книга Passport</span><span class="sxs-lookup"><span data-stu-id="55da0-543">passport book</span></span>  <br/> <span data-ttu-id="55da0-544">passport number</span><span class="sxs-lookup"><span data-stu-id="55da0-544">passport number</span></span>  <br/> <span data-ttu-id="55da0-545">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="55da0-545">passport no</span></span>  <br/> <span data-ttu-id="55da0-546">либрета пасапорте</span><span class="sxs-lookup"><span data-stu-id="55da0-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="55da0-547">нúмеро пасапорте</span><span class="sxs-lookup"><span data-stu-id="55da0-547">número pasaporte</span></span>  <br/> <span data-ttu-id="55da0-548">еспаñа пасапорте</span><span class="sxs-lookup"><span data-stu-id="55da0-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="55da0-549">пасапорте</span><span class="sxs-lookup"><span data-stu-id="55da0-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="55da0-550">Швеция</span><span class="sxs-lookup"><span data-stu-id="55da0-550">Sweden</span></span>

<span data-ttu-id="55da0-551">Дополнительные сведения можно найти в разделе "Швеции Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="55da0-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="55da0-552">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="55da0-552">UK</span></span>

<span data-ttu-id="55da0-553">Дополнительные сведения см. в разделе "США/Великобритания</span><span class="sxs-lookup"><span data-stu-id="55da0-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="55da0-554">Номер паспорта [, который ищет типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="55da0-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55da0-555">См. также</span><span class="sxs-lookup"><span data-stu-id="55da0-555">See also</span></span>

[<span data-ttu-id="55da0-556">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="55da0-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

