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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256827"
---
# <a name="eu-passport-number"></a><span data-ttu-id="53642-104">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="53642-104">EU Passport Number</span></span>

<span data-ttu-id="53642-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС Passport Number.</span><span class="sxs-lookup"><span data-stu-id="53642-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="53642-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="53642-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="53642-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="53642-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="53642-108">Format</span><span class="sxs-lookup"><span data-stu-id="53642-108">Format</span></span>

<span data-ttu-id="53642-109">Одна буква, за которой следует необязательный пробел и семь цифр</span><span class="sxs-lookup"><span data-stu-id="53642-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-110">Pattern</span></span>

<span data-ttu-id="53642-111">Сочетание одной буквы, семи цифр и одного пробела:</span><span class="sxs-lookup"><span data-stu-id="53642-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="53642-112">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="53642-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="53642-113">Один пробел (необязательно)</span><span class="sxs-lookup"><span data-stu-id="53642-113">One space (optional)</span></span>
    
- <span data-ttu-id="53642-114">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53642-115">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-115">Checksum</span></span>

<span data-ttu-id="53642-116">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="53642-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-117">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-117">Definition</span></span>

<span data-ttu-id="53642-118">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-119">Регулярное выражение `Regex_austria_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-120">Найдено ключевое `Keywords_austria_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-121">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-121">Keywords</span></span>

<span data-ttu-id="53642-122">| |</span><span class="sxs-lookup"><span data-stu-id="53642-122"></span></span>
|<span data-ttu-id="53642-123">**Кэйвордс_аустриа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-124">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-124">passport number</span></span>  <br/> <span data-ttu-id="53642-125">Австрийский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="53642-125">austrian passport number</span></span>  <br/> <span data-ttu-id="53642-126">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-126">passport no</span></span>  <br/> <span data-ttu-id="53642-127">реисепасс</span><span class="sxs-lookup"><span data-stu-id="53642-127">reisepass</span></span>  <br/> <span data-ttu-id="53642-128">öстерреичисч реисепасс</span><span class="sxs-lookup"><span data-stu-id="53642-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="53642-129">Бельгия</span><span class="sxs-lookup"><span data-stu-id="53642-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="53642-130">Format</span><span class="sxs-lookup"><span data-stu-id="53642-130">Format</span></span>

<span data-ttu-id="53642-131">Две буквы, за которыми следуют шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-132">Pattern</span></span>

<span data-ttu-id="53642-133">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-134">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-134">Checksum</span></span>

<span data-ttu-id="53642-135">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="53642-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-136">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-136">Definition</span></span>

<span data-ttu-id="53642-137">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-138">Регулярное выражение `Regex_belgium_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-139">Найдено ключевое `Keywords_belgium_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-140">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-140">Keywords</span></span>

<span data-ttu-id="53642-141">| |</span><span class="sxs-lookup"><span data-stu-id="53642-141"></span></span>
|<span data-ttu-id="53642-142">**Кэйвордс_белгиум_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-143">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-143">passport number</span></span>  <br/> <span data-ttu-id="53642-144">Бельгийский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="53642-144">belgian passport number</span></span>  <br/> <span data-ttu-id="53642-145">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-145">passport no</span></span>  <br/> <span data-ttu-id="53642-146">паспурт</span><span class="sxs-lookup"><span data-stu-id="53642-146">paspoort</span></span>  <br/> <span data-ttu-id="53642-147">паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="53642-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="53642-148">реисепасс Кеин</span><span class="sxs-lookup"><span data-stu-id="53642-148">reisepass kein</span></span>  <br/> <span data-ttu-id="53642-149">реисепасс</span><span class="sxs-lookup"><span data-stu-id="53642-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="53642-150">Болгария</span><span class="sxs-lookup"><span data-stu-id="53642-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="53642-151">Format</span><span class="sxs-lookup"><span data-stu-id="53642-151">Format</span></span>

<span data-ttu-id="53642-152">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-153">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-153">Pattern</span></span>

 <span data-ttu-id="53642-154">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="53642-155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-155">Checksum</span></span>

<span data-ttu-id="53642-156">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-157">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-157">Definition</span></span>

<span data-ttu-id="53642-158">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-159">Регулярное выражение `Regex_bulgaria_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-160">Найдено ключевое `Keywords_bulgaria_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-161">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-161">Keywords</span></span>

<span data-ttu-id="53642-162">| |</span><span class="sxs-lookup"><span data-stu-id="53642-162"></span></span>
|<span data-ttu-id="53642-163">**Кэйвордс_булгариа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-164">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-164">passport number</span></span>  <br/> <span data-ttu-id="53642-165">номер паспорта для болгарского языка</span><span class="sxs-lookup"><span data-stu-id="53642-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="53642-166">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-166">passport no</span></span>  <br/> <span data-ttu-id="53642-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="53642-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="53642-168">Хорватия</span><span class="sxs-lookup"><span data-stu-id="53642-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="53642-169">Format</span><span class="sxs-lookup"><span data-stu-id="53642-169">Format</span></span>

<span data-ttu-id="53642-170">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-171">Pattern</span></span>

 <span data-ttu-id="53642-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="53642-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-173">Checksum</span></span>

<span data-ttu-id="53642-174">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-175">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-175">Definition</span></span>

<span data-ttu-id="53642-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-177">Регулярное выражение `Regex_croatia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-178">Найдено ключевое `Keywords_croatia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-179">Keywords</span></span>

<span data-ttu-id="53642-180">| |</span><span class="sxs-lookup"><span data-stu-id="53642-180"></span></span>
|<span data-ttu-id="53642-181">**Кэйвордс_кроатиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-182">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-182">passport number</span></span>  <br/> <span data-ttu-id="53642-183">номер паспорта для хорватского языка</span><span class="sxs-lookup"><span data-stu-id="53642-183">croatian passport number</span></span>  <br/> <span data-ttu-id="53642-184">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-184">passport no</span></span>  <br/> <span data-ttu-id="53642-185">Брож путовнице</span><span class="sxs-lookup"><span data-stu-id="53642-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="53642-186">Кипр</span><span class="sxs-lookup"><span data-stu-id="53642-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="53642-187">Format</span><span class="sxs-lookup"><span data-stu-id="53642-187">Format</span></span>

<span data-ttu-id="53642-188">Одна буква, за которой следуют 6-8 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-189">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-189">Pattern</span></span>

<span data-ttu-id="53642-190">Одна буква, за которой следуют шесть и восемь цифр</span><span class="sxs-lookup"><span data-stu-id="53642-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-191">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-191">Checksum</span></span>

<span data-ttu-id="53642-192">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-193">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-193">Definition</span></span>

<span data-ttu-id="53642-194">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-195">Регулярное выражение `Regex_cyprus_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-196">Найдено ключевое `Keywords_cyprus_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-197">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-197">Keywords</span></span>

<span data-ttu-id="53642-198">| |</span><span class="sxs-lookup"><span data-stu-id="53642-198"></span></span>
|<span data-ttu-id="53642-199">**Кэйвордс_ципрус_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-200">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-200">passport number</span></span>  <br/> <span data-ttu-id="53642-201">номер паспорта для Кипр</span><span class="sxs-lookup"><span data-stu-id="53642-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="53642-202">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-202">passport no</span></span>  <br/> <span data-ttu-id="53642-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="53642-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="53642-204">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="53642-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="53642-205">Format</span><span class="sxs-lookup"><span data-stu-id="53642-205">Format</span></span>

<span data-ttu-id="53642-206">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-207">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-207">Pattern</span></span>

<span data-ttu-id="53642-208">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-209">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-209">Checksum</span></span>

<span data-ttu-id="53642-210">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-211">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-211">Definition</span></span>

<span data-ttu-id="53642-212">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-213">Регулярное выражение `Regex_czech_republic_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-214">Найдено ключевое `Keywords_czech_republic_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-215">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-215">Keywords</span></span>

<span data-ttu-id="53642-216">| |</span><span class="sxs-lookup"><span data-stu-id="53642-216"></span></span>
|<span data-ttu-id="53642-217">**Кэйвордс_кзеч_републик_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-218">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-218">passport number</span></span>  <br/> <span data-ttu-id="53642-219">номер паспорта для чешского языка</span><span class="sxs-lookup"><span data-stu-id="53642-219">czech passport number</span></span>  <br/> <span data-ttu-id="53642-220">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-220">passport no</span></span>  <br/> <span data-ttu-id="53642-221">цестовнí PAS</span><span class="sxs-lookup"><span data-stu-id="53642-221">cestovní pas</span></span>  <br/> <span data-ttu-id="53642-222">соответствующий</span><span class="sxs-lookup"><span data-stu-id="53642-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="53642-223">Дания</span><span class="sxs-lookup"><span data-stu-id="53642-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="53642-224">Format</span><span class="sxs-lookup"><span data-stu-id="53642-224">Format</span></span>

<span data-ttu-id="53642-225">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-226">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-226">Pattern</span></span>

 <span data-ttu-id="53642-227">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="53642-228">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-228">Checksum</span></span>

<span data-ttu-id="53642-229">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-230">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-230">Definition</span></span>

<span data-ttu-id="53642-231">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-232">Регулярное выражение `Regex_denmark_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-233">Найдено ключевое `Keywords_denmark_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-234">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-234">Keywords</span></span>

<span data-ttu-id="53642-235">| |</span><span class="sxs-lookup"><span data-stu-id="53642-235"></span></span>
|<span data-ttu-id="53642-236">**Кэйвордс_денмарк_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-237">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-237">passport number</span></span>  <br/> <span data-ttu-id="53642-238">номер паспорта для датского языка</span><span class="sxs-lookup"><span data-stu-id="53642-238">danish passport number</span></span>  <br/> <span data-ttu-id="53642-239">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-239">passport no</span></span>  <br/> <span data-ttu-id="53642-240">соответствующий</span><span class="sxs-lookup"><span data-stu-id="53642-240">pas</span></span>  <br/> <span data-ttu-id="53642-241">паснуммер</span><span class="sxs-lookup"><span data-stu-id="53642-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="53642-242">Эстония</span><span class="sxs-lookup"><span data-stu-id="53642-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="53642-243">Format</span><span class="sxs-lookup"><span data-stu-id="53642-243">Format</span></span>

<span data-ttu-id="53642-244">Одна буква, за которой следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-245">Pattern</span></span>

<span data-ttu-id="53642-246">Одна буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-247">Checksum</span></span>

<span data-ttu-id="53642-248">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-249">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-249">Definition</span></span>

<span data-ttu-id="53642-250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-251">Регулярное выражение `Regex_estonia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-252">Найдено ключевое `Keywords_estonia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-253">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-253">Keywords</span></span>

<span data-ttu-id="53642-254">| |</span><span class="sxs-lookup"><span data-stu-id="53642-254"></span></span>
|<span data-ttu-id="53642-255">**Кэйвордс_естониа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-256">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-256">passport number</span></span>  <br/> <span data-ttu-id="53642-257">номер паспорта для Эстонии</span><span class="sxs-lookup"><span data-stu-id="53642-257">estonian passport number</span></span>  <br/> <span data-ttu-id="53642-258">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-258">passport no</span></span>  <br/> <span data-ttu-id="53642-259">Исти коданику Pass</span><span class="sxs-lookup"><span data-stu-id="53642-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="53642-260">Финляндия</span><span class="sxs-lookup"><span data-stu-id="53642-260">Finland</span></span>

<span data-ttu-id="53642-261">Дополнительные сведения можно найти в разделе "Финляндия Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="53642-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="53642-262">Франция</span><span class="sxs-lookup"><span data-stu-id="53642-262">France</span></span>

<span data-ttu-id="53642-263">Дополнительные сведения можно найти в разделе "Франция Passport Number", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="53642-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="53642-264">Германия</span><span class="sxs-lookup"><span data-stu-id="53642-264">Germany</span></span>

<span data-ttu-id="53642-265">Дополнительные сведения можно найти в разделе "Германия Passport Number", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="53642-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="53642-266">Греция</span><span class="sxs-lookup"><span data-stu-id="53642-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="53642-267">Format</span><span class="sxs-lookup"><span data-stu-id="53642-267">Format</span></span>

<span data-ttu-id="53642-268">Две буквы, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-269">Pattern</span></span>

<span data-ttu-id="53642-270">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-271">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-271">Checksum</span></span>

<span data-ttu-id="53642-272">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-273">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-273">Definition</span></span>

<span data-ttu-id="53642-274">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-275">Регулярное выражение `Regex_greece_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-276">Найдено ключевое `Keywords_greece_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-277">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-277">Keywords</span></span>

<span data-ttu-id="53642-278">| |</span><span class="sxs-lookup"><span data-stu-id="53642-278"></span></span>
|<span data-ttu-id="53642-279">**Кэйвордс_грице_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-280">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-280">passport number</span></span>  <br/> <span data-ttu-id="53642-281">номер паспорта греческого алфавита</span><span class="sxs-lookup"><span data-stu-id="53642-281">greek passport number</span></span>  <br/> <span data-ttu-id="53642-282">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-282">passport no</span></span>  <br/> <span data-ttu-id="53642-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="53642-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="53642-284">Венгрия</span><span class="sxs-lookup"><span data-stu-id="53642-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="53642-285">Format</span><span class="sxs-lookup"><span data-stu-id="53642-285">Format</span></span>

<span data-ttu-id="53642-286">Две буквы, за которыми следуют шесть или семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-287">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-287">Pattern</span></span>

<span data-ttu-id="53642-288">Две буквы, за которыми следуют шесть или семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-289">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-289">Checksum</span></span>

<span data-ttu-id="53642-290">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-291">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-291">Definition</span></span>

<span data-ttu-id="53642-292">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-293">Регулярное выражение `Regex_hungary_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-294">Найдено ключевое `Keywords_hungary_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-295">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-295">Keywords</span></span>

<span data-ttu-id="53642-296">| |</span><span class="sxs-lookup"><span data-stu-id="53642-296"></span></span>
|<span data-ttu-id="53642-297">**Кэйвордс_хунгари_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-298">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-298">passport number</span></span>  <br/> <span data-ttu-id="53642-299">Венгерский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="53642-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="53642-300">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-300">passport no</span></span>  <br/> <span data-ttu-id="53642-301">úтлевéл сзáма</span><span class="sxs-lookup"><span data-stu-id="53642-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="53642-302">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="53642-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="53642-303">Format</span><span class="sxs-lookup"><span data-stu-id="53642-303">Format</span></span>

<span data-ttu-id="53642-304">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-305">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-305">Pattern</span></span>

<span data-ttu-id="53642-306">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="53642-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="53642-307">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="53642-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="53642-308">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53642-309">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-309">Checksum</span></span>

<span data-ttu-id="53642-310">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-311">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-311">Definition</span></span>

<span data-ttu-id="53642-312">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-313">Регулярное выражение `Regex_ireland_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-314">Найдено ключевое `Keywords_ireland_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-315">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-315">Keywords</span></span>

<span data-ttu-id="53642-316">| |</span><span class="sxs-lookup"><span data-stu-id="53642-316"></span></span>
|<span data-ttu-id="53642-317">**Кэйвордс_иреланд_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-318">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-318">passport number</span></span>  <br/> <span data-ttu-id="53642-319">Ирландский номер паспорта</span><span class="sxs-lookup"><span data-stu-id="53642-319">irish passport number</span></span>  <br/> <span data-ttu-id="53642-320">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-320">passport no</span></span>  <br/> <span data-ttu-id="53642-321">соответствующий</span><span class="sxs-lookup"><span data-stu-id="53642-321">pas</span></span>  <br/> <span data-ttu-id="53642-322">службу</span><span class="sxs-lookup"><span data-stu-id="53642-322">passport</span></span>  <br/> <span data-ttu-id="53642-323">пассепорт</span><span class="sxs-lookup"><span data-stu-id="53642-323">passeport</span></span>  <br/> <span data-ttu-id="53642-324">пассепорт нумеро</span><span class="sxs-lookup"><span data-stu-id="53642-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="53642-325">Италия</span><span class="sxs-lookup"><span data-stu-id="53642-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="53642-326">Format</span><span class="sxs-lookup"><span data-stu-id="53642-326">Format</span></span>

<span data-ttu-id="53642-327">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-328">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-328">Pattern</span></span>

<span data-ttu-id="53642-329">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="53642-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="53642-330">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="53642-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="53642-331">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53642-332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-332">Checksum</span></span>

<span data-ttu-id="53642-333">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="53642-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-334">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-334">Definition</span></span>

<span data-ttu-id="53642-335">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-336">Регулярное выражение `Regex_italy_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-337">Найдено ключевое `Keywords_italy_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-338">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-338">Keywords</span></span>

<span data-ttu-id="53642-339">| |</span><span class="sxs-lookup"><span data-stu-id="53642-339"></span></span>
|<span data-ttu-id="53642-340">**Кэйвордс_итали_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-341">номер паспорта для итальянского языка</span><span class="sxs-lookup"><span data-stu-id="53642-341">italian passport number</span></span>  <br/> <span data-ttu-id="53642-342">Репубблика итальянский пассапорто</span><span class="sxs-lookup"><span data-stu-id="53642-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="53642-343">пассапорто</span><span class="sxs-lookup"><span data-stu-id="53642-343">passaporto</span></span>  <br/> <span data-ttu-id="53642-344">пассапорто итальянский</span><span class="sxs-lookup"><span data-stu-id="53642-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="53642-345">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-345">passport number</span></span>  <br/> <span data-ttu-id="53642-346">Итальянский пассапорто нумеро</span><span class="sxs-lookup"><span data-stu-id="53642-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="53642-347">пассапорто нумеро</span><span class="sxs-lookup"><span data-stu-id="53642-347">passaporto numero</span></span>  <br/> <span data-ttu-id="53642-348">нумéро пассепорт италиен</span><span class="sxs-lookup"><span data-stu-id="53642-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="53642-349">нумéро пассепорт</span><span class="sxs-lookup"><span data-stu-id="53642-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="53642-350">Латвия</span><span class="sxs-lookup"><span data-stu-id="53642-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="53642-351">Format</span><span class="sxs-lookup"><span data-stu-id="53642-351">Format</span></span>

<span data-ttu-id="53642-352">Две буквы или цифры, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-353">Pattern</span></span>

<span data-ttu-id="53642-354">Две буквы или цифры, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="53642-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="53642-355">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="53642-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="53642-356">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53642-357">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-357">Checksum</span></span>

<span data-ttu-id="53642-358">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-359">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-359">Definition</span></span>

<span data-ttu-id="53642-360">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-361">Регулярное выражение `Regex_latvia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-362">Найдено ключевое `Keywords_latvia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-363">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-363">Keywords</span></span>

<span data-ttu-id="53642-364">| |</span><span class="sxs-lookup"><span data-stu-id="53642-364"></span></span>
|<span data-ttu-id="53642-365">**Кэйвордс_латвиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-366">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-366">passport number</span></span>  <br/> <span data-ttu-id="53642-367">номер паспорта для Латвии</span><span class="sxs-lookup"><span data-stu-id="53642-367">latvian passport number</span></span>  <br/> <span data-ttu-id="53642-368">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-368">passport no</span></span>  <br/> <span data-ttu-id="53642-369">ПАСЕ нумурс</span><span class="sxs-lookup"><span data-stu-id="53642-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="53642-370">Литва</span><span class="sxs-lookup"><span data-stu-id="53642-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="53642-371">Format</span><span class="sxs-lookup"><span data-stu-id="53642-371">Format</span></span>

<span data-ttu-id="53642-372">Восемь цифр или букв без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-373">Pattern</span></span>

<span data-ttu-id="53642-374">Восемь цифр или букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="53642-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-375">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-375">Checksum</span></span>

<span data-ttu-id="53642-376">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="53642-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-377">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-377">Definition</span></span>

<span data-ttu-id="53642-378">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-379">Регулярное выражение `Regex_lithuania_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-380">Найдено ключевое `Keywords_lithuania_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-381">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-381">Keywords</span></span>

<span data-ttu-id="53642-382">| |</span><span class="sxs-lookup"><span data-stu-id="53642-382"></span></span>
|<span data-ttu-id="53642-383">**Кэйвордс_лисуаниа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-384">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-384">passport number</span></span>  <br/> <span data-ttu-id="53642-385">номер паспорта лисуниан</span><span class="sxs-lookup"><span data-stu-id="53642-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="53642-386">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-386">passport no</span></span>  <br/> <span data-ttu-id="53642-387">Пасо нумерис</span><span class="sxs-lookup"><span data-stu-id="53642-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="53642-388">Луксембург</span><span class="sxs-lookup"><span data-stu-id="53642-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="53642-389">Format</span><span class="sxs-lookup"><span data-stu-id="53642-389">Format</span></span>

<span data-ttu-id="53642-390">Восемь цифр или букв без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-391">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-391">Pattern</span></span>

<span data-ttu-id="53642-392">Восемь цифр или букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="53642-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-393">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-393">Checksum</span></span>

<span data-ttu-id="53642-394">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-395">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-395">Definition</span></span>

<span data-ttu-id="53642-396">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-397">Регулярное выражение `Regex_nation_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-398">Найдено ключевое `Keywords_nation_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-399">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-399">Keywords</span></span>

<span data-ttu-id="53642-400">| |</span><span class="sxs-lookup"><span data-stu-id="53642-400"></span></span>
|<span data-ttu-id="53642-401">**Кэйвордс_натион_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-402">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-402">passport number</span></span>  <br/> <span data-ttu-id="53642-403">номер паспорта для Латвии</span><span class="sxs-lookup"><span data-stu-id="53642-403">latvian passport number</span></span>  <br/> <span data-ttu-id="53642-404">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-404">passport no</span></span>  <br/> <span data-ttu-id="53642-405">пасснуммер</span><span class="sxs-lookup"><span data-stu-id="53642-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="53642-406">Мальта</span><span class="sxs-lookup"><span data-stu-id="53642-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="53642-407">Format</span><span class="sxs-lookup"><span data-stu-id="53642-407">Format</span></span>

<span data-ttu-id="53642-408">Семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-409">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-409">Pattern</span></span>

 <span data-ttu-id="53642-410">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="53642-411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-411">Checksum</span></span>

<span data-ttu-id="53642-412">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-413">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-413">Definition</span></span>

<span data-ttu-id="53642-414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-415">Регулярное выражение `Regex_malta_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-416">Найдено ключевое `Keywords_malta_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-417">Keywords</span></span>

<span data-ttu-id="53642-418">| |</span><span class="sxs-lookup"><span data-stu-id="53642-418"></span></span>
|<span data-ttu-id="53642-419">**Кэйвордс_малта_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-420">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-420">passport number</span></span>  <br/> <span data-ttu-id="53642-421">номер паспорта Мальтийский</span><span class="sxs-lookup"><span data-stu-id="53642-421">maltese passport number</span></span>  <br/> <span data-ttu-id="53642-422">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-422">passport no</span></span>  <br/> <span data-ttu-id="53642-423">нумру Тал — пассапорт</span><span class="sxs-lookup"><span data-stu-id="53642-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="53642-424">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="53642-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="53642-425">Format</span><span class="sxs-lookup"><span data-stu-id="53642-425">Format</span></span>

<span data-ttu-id="53642-426">Девять букв или цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-427">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-427">Pattern</span></span>

<span data-ttu-id="53642-428">Девять букв или цифр;</span><span class="sxs-lookup"><span data-stu-id="53642-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-429">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-429">Checksum</span></span>

<span data-ttu-id="53642-430">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="53642-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-431">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-431">Definition</span></span>

<span data-ttu-id="53642-432">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-433">Регулярное выражение `Regex_netherlands_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-434">Найдено ключевое `Keywords_netherlands_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-435">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-435">Keywords</span></span>

<span data-ttu-id="53642-436">| |</span><span class="sxs-lookup"><span data-stu-id="53642-436"></span></span>
|<span data-ttu-id="53642-437">**Кэйвордс_несерландс_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-438">номер паспорта для нидерландского языка</span><span class="sxs-lookup"><span data-stu-id="53642-438">dutch passport number</span></span>  <br/> <span data-ttu-id="53642-439">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-439">passport number</span></span>  <br/> <span data-ttu-id="53642-440">номер паспорта Нидерландов</span><span class="sxs-lookup"><span data-stu-id="53642-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="53642-441">недерланден паспурт нуммер</span><span class="sxs-lookup"><span data-stu-id="53642-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="53642-442">паспурт</span><span class="sxs-lookup"><span data-stu-id="53642-442">paspoort</span></span>  <br/> <span data-ttu-id="53642-443">недерланден паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="53642-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="53642-444">паспуртнуммер</span><span class="sxs-lookup"><span data-stu-id="53642-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="53642-445">Польша</span><span class="sxs-lookup"><span data-stu-id="53642-445">Poland</span></span>

<span data-ttu-id="53642-446">Дополнительные сведения можно найти в разделе "Польша Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="53642-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="53642-447">Португалия</span><span class="sxs-lookup"><span data-stu-id="53642-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="53642-448">Format</span><span class="sxs-lookup"><span data-stu-id="53642-448">Format</span></span>

<span data-ttu-id="53642-449">Одна буква, за которой следуют шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-450">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-450">Pattern</span></span>

<span data-ttu-id="53642-451">Одна буква, за которой следуют шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="53642-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="53642-452">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="53642-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="53642-453">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53642-454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-454">Checksum</span></span>

<span data-ttu-id="53642-455">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-456">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-456">Definition</span></span>

<span data-ttu-id="53642-457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-458">Регулярное выражение `Regex_portugal_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-459">Найдено ключевое `Keywords_portugal_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-460">Keywords</span></span>

<span data-ttu-id="53642-461">| |</span><span class="sxs-lookup"><span data-stu-id="53642-461"></span></span>
|<span data-ttu-id="53642-462">**Кэйвордс_португал_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-463">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-463">passport number</span></span>  <br/> <span data-ttu-id="53642-464">номер паспорта для португальского языка</span><span class="sxs-lookup"><span data-stu-id="53642-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="53642-465">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-465">passport no</span></span>  <br/> <span data-ttu-id="53642-466">нúмеро Do пассапорте</span><span class="sxs-lookup"><span data-stu-id="53642-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="53642-467">Румыния</span><span class="sxs-lookup"><span data-stu-id="53642-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="53642-468">Format</span><span class="sxs-lookup"><span data-stu-id="53642-468">Format</span></span>

<span data-ttu-id="53642-469">Восемь или девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-470">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-470">Pattern</span></span>

<span data-ttu-id="53642-471">Восемь или девять цифр</span><span class="sxs-lookup"><span data-stu-id="53642-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-472">Checksum</span></span>

<span data-ttu-id="53642-473">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-474">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-474">Definition</span></span>

<span data-ttu-id="53642-475">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-476">Регулярное выражение `Regex_romania_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-477">Найдено ключевое `Keywords_romania_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-478">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-478">Keywords</span></span>

<span data-ttu-id="53642-479">| |</span><span class="sxs-lookup"><span data-stu-id="53642-479"></span></span>
|<span data-ttu-id="53642-480">**Кэйвордс_романиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-481">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-481">passport number</span></span>  <br/> <span data-ttu-id="53642-482">номер паспорта для румынского языка</span><span class="sxs-lookup"><span data-stu-id="53642-482">romanian passport number</span></span>  <br/> <span data-ttu-id="53642-483">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-483">passport no</span></span>  <br/> <span data-ttu-id="53642-484">нумăрул паșапортулуи</span><span class="sxs-lookup"><span data-stu-id="53642-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="53642-485">Словакия</span><span class="sxs-lookup"><span data-stu-id="53642-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="53642-486">Format</span><span class="sxs-lookup"><span data-stu-id="53642-486">Format</span></span>

<span data-ttu-id="53642-487">Одна цифра или буква, за которой следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-488">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-488">Pattern</span></span>

<span data-ttu-id="53642-489">Одна цифра или буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="53642-490">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-490">Checksum</span></span>

<span data-ttu-id="53642-491">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-492">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-492">Definition</span></span>

<span data-ttu-id="53642-493">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-494">Регулярное выражение `Regex_slovakia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-495">Найдено ключевое `Keywords_slovakia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-496">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-496">Keywords</span></span>

<span data-ttu-id="53642-497">| |</span><span class="sxs-lookup"><span data-stu-id="53642-497"></span></span>
|<span data-ttu-id="53642-498">**Кэйвордс_словакиа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-499">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-499">passport number</span></span>  <br/> <span data-ttu-id="53642-500">номер паспорта словакиан</span><span class="sxs-lookup"><span data-stu-id="53642-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="53642-501">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-501">passport no</span></span>  <br/> <span data-ttu-id="53642-502">číсло Пасу</span><span class="sxs-lookup"><span data-stu-id="53642-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="53642-503">Словения</span><span class="sxs-lookup"><span data-stu-id="53642-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="53642-504">Format</span><span class="sxs-lookup"><span data-stu-id="53642-504">Format</span></span>

<span data-ttu-id="53642-505">Две буквы, за которыми следуют семь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-506">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-506">Pattern</span></span>

<span data-ttu-id="53642-507">Две буквы, за которыми следуют семь цифр:</span><span class="sxs-lookup"><span data-stu-id="53642-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="53642-508">Буква "P"</span><span class="sxs-lookup"><span data-stu-id="53642-508">The letter "P"</span></span>
    
- <span data-ttu-id="53642-509">Одна прописная буква</span><span class="sxs-lookup"><span data-stu-id="53642-509">One uppercase letter</span></span>
    
- <span data-ttu-id="53642-510">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53642-511">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-511">Checksum</span></span>

<span data-ttu-id="53642-512">Нет</span><span class="sxs-lookup"><span data-stu-id="53642-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-513">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-513">Definition</span></span>

<span data-ttu-id="53642-514">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-515">Регулярное выражение `Regex_slovenia_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-516">Найдено ключевое `Keywords_slovenia_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-517">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-517">Keywords</span></span>

<span data-ttu-id="53642-518">| |</span><span class="sxs-lookup"><span data-stu-id="53642-518"></span></span>
|<span data-ttu-id="53642-519">**Кэйвордс_словениа_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-520">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-520">passport number</span></span>  <br/> <span data-ttu-id="53642-521">номер паспорта для словенского языка</span><span class="sxs-lookup"><span data-stu-id="53642-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="53642-522">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-522">passport no</span></span>  <br/> <span data-ttu-id="53642-523">Список потнега šтевилка</span><span class="sxs-lookup"><span data-stu-id="53642-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="53642-524">Испания</span><span class="sxs-lookup"><span data-stu-id="53642-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="53642-525">Format</span><span class="sxs-lookup"><span data-stu-id="53642-525">Format</span></span>

<span data-ttu-id="53642-526">Сочетание букв и цифр из восьми или девяти символов без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="53642-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="53642-527">Шаблон</span><span class="sxs-lookup"><span data-stu-id="53642-527">Pattern</span></span>

<span data-ttu-id="53642-528">Сочетание букв и цифр из восьми или девяти символов:</span><span class="sxs-lookup"><span data-stu-id="53642-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="53642-529">Две цифры или буквы</span><span class="sxs-lookup"><span data-stu-id="53642-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="53642-530">Одна цифра или буква (необязательно)</span><span class="sxs-lookup"><span data-stu-id="53642-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="53642-531">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="53642-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="53642-532">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="53642-532">Checksum</span></span>

<span data-ttu-id="53642-533">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="53642-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="53642-534">Определение</span><span class="sxs-lookup"><span data-stu-id="53642-534">Definition</span></span>

<span data-ttu-id="53642-535">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="53642-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="53642-536">Регулярное выражение `Regex_spain_eu_passport_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="53642-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="53642-537">Найдено ключевое `Keywords_spain_eu_passport_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="53642-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="53642-538">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="53642-538">Keywords</span></span>

<span data-ttu-id="53642-539">| |</span><span class="sxs-lookup"><span data-stu-id="53642-539"></span></span>
|<span data-ttu-id="53642-540">**Кэйвордс_спаин_еу_пасспорт_нумбер**</span><span class="sxs-lookup"><span data-stu-id="53642-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="53642-541">службу</span><span class="sxs-lookup"><span data-stu-id="53642-541">passport</span></span>  <br/> <span data-ttu-id="53642-542">Служба Passport, Испания</span><span class="sxs-lookup"><span data-stu-id="53642-542">spain passport</span></span>  <br/> <span data-ttu-id="53642-543">Книга Passport</span><span class="sxs-lookup"><span data-stu-id="53642-543">passport book</span></span>  <br/> <span data-ttu-id="53642-544">passport number</span><span class="sxs-lookup"><span data-stu-id="53642-544">passport number</span></span>  <br/> <span data-ttu-id="53642-545">паспорт нет</span><span class="sxs-lookup"><span data-stu-id="53642-545">passport no</span></span>  <br/> <span data-ttu-id="53642-546">либрета пасапорте</span><span class="sxs-lookup"><span data-stu-id="53642-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="53642-547">нúмеро пасапорте</span><span class="sxs-lookup"><span data-stu-id="53642-547">número pasaporte</span></span>  <br/> <span data-ttu-id="53642-548">еспаñа пасапорте</span><span class="sxs-lookup"><span data-stu-id="53642-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="53642-549">пасапорте</span><span class="sxs-lookup"><span data-stu-id="53642-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="53642-550">Швеция</span><span class="sxs-lookup"><span data-stu-id="53642-550">Sweden</span></span>

<span data-ttu-id="53642-551">Дополнительные сведения можно найти в разделе "Швеции Passport Number", в котором [ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="53642-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="53642-552">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="53642-552">UK</span></span>

<span data-ttu-id="53642-553">Дополнительные сведения см. в разделе "США/Великобритания</span><span class="sxs-lookup"><span data-stu-id="53642-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="53642-554">Номер паспорта [, который ищет типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="53642-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53642-555">См. также</span><span class="sxs-lookup"><span data-stu-id="53642-555">See also</span></span>

[<span data-ttu-id="53642-556">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="53642-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

