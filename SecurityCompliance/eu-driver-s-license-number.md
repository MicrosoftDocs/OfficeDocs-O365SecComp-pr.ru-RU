---
title: Номер водительского удостоверения для драйвера ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации номера лицензии для драйвера ЕС. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: f1a95ecbaf6b6d1ac189290dd6d076cfd91ab30f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152981"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="a2370-104">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="a2370-104">EU Driver's License Number</span></span>

<span data-ttu-id="a2370-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации номера лицензии для драйвера ЕС.</span><span class="sxs-lookup"><span data-stu-id="a2370-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="a2370-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="a2370-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="a2370-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="a2370-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="a2370-108">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-108">Format</span></span>

<span data-ttu-id="a2370-109">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-110">Pattern</span></span>

<span data-ttu-id="a2370-111">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2370-112">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-112">Checksum</span></span>

<span data-ttu-id="a2370-113">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-114">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-114">Definition</span></span>

<span data-ttu-id="a2370-115">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-116">Регулярное выражение `Regex_austria_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-117">Найдено ключевое `Keywords_austria_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2370-118">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-118">Keywords</span></span>

<span data-ttu-id="a2370-119">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-119"></span></span>
|<span data-ttu-id="a2370-120">**Кэйвордс_аустриа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-121">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-121">dl#</span></span>  <br/> <span data-ttu-id="a2370-122">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-122">driver license</span></span>  <br/> <span data-ttu-id="a2370-123">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-123">driver license number</span></span>  <br/> <span data-ttu-id="a2370-124">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-124">driver licence</span></span>  <br/> <span data-ttu-id="a2370-125">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-125">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-126">drivers license</span></span>  <br/> <span data-ttu-id="a2370-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="a2370-127">driver's licence</span></span>  <br/> <span data-ttu-id="a2370-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-128">driver's license</span></span>  <br/> <span data-ttu-id="a2370-129">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-129">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-130">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="a2370-131">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-131">driving license number</span></span>  <br/> <span data-ttu-id="a2370-132">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-132">dlno#</span></span>  <br/> <span data-ttu-id="a2370-133">фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="a2370-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="a2370-134">фухрерсчеин Републик остерреич</span><span class="sxs-lookup"><span data-stu-id="a2370-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="a2370-135">Бельгия</span><span class="sxs-lookup"><span data-stu-id="a2370-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="a2370-136">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-136">Format</span></span>

<span data-ttu-id="a2370-137">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-138">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-138">Pattern</span></span>

<span data-ttu-id="a2370-139">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2370-140">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-140">Checksum</span></span>

<span data-ttu-id="a2370-141">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-142">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-142">Definition</span></span>

<span data-ttu-id="a2370-143">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-144">Регулярное выражение `Regex_belgium_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-145">Найдено ключевое `Keywords_belgium_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2370-146">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-146">Keywords</span></span>

<span data-ttu-id="a2370-147">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-147"></span></span>
|<span data-ttu-id="a2370-148">**Кэйвордс__белгиум_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-149">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-149">dl#</span></span>  <br/> <span data-ttu-id="a2370-150">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-150">driver license</span></span>  <br/> <span data-ttu-id="a2370-151">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-151">driver license number</span></span>  <br/> <span data-ttu-id="a2370-152">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-152">driver licence</span></span>  <br/> <span data-ttu-id="a2370-153">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-153">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-154">drivers license</span></span>  <br/> <span data-ttu-id="a2370-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-155">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-156">driver's license</span></span>  <br/> <span data-ttu-id="a2370-157">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-157">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-158">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-158">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-159">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-159">dlno#</span></span>  <br/> <span data-ttu-id="a2370-160">рижбевижс</span><span class="sxs-lookup"><span data-stu-id="a2370-160">rijbewijs</span></span>  <br/> <span data-ttu-id="a2370-161">рижбевижснуммер</span><span class="sxs-lookup"><span data-stu-id="a2370-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="a2370-162">фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="a2370-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="a2370-163">фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="a2370-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="a2370-164">фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="a2370-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="a2370-165">фüхрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="a2370-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="a2370-166">фуехрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="a2370-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="a2370-167">фуехрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="a2370-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="a2370-168">Болгария</span><span class="sxs-lookup"><span data-stu-id="a2370-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="a2370-169">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-169">Format</span></span>

<span data-ttu-id="a2370-170">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-171">Pattern</span></span>

<span data-ttu-id="a2370-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2370-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-173">Checksum</span></span>

<span data-ttu-id="a2370-174">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-175">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-175">Definition</span></span>

<span data-ttu-id="a2370-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-177">Регулярное выражение `Regex_bulgaria_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-178">Найдено ключевое `Keywords_bulgaria_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="a2370-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-179">Keywords</span></span>

<span data-ttu-id="a2370-180">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-180"></span></span>
|<span data-ttu-id="a2370-181">**Кэйвордс_булгариа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-182">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-182">dl#</span></span>  <br/> <span data-ttu-id="a2370-183">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-183">driver license</span></span>  <br/> <span data-ttu-id="a2370-184">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-184">driver license number</span></span>  <br/> <span data-ttu-id="a2370-185">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-185">driver licence</span></span>  <br/> <span data-ttu-id="a2370-186">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-186">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-187">drivers license</span></span>  <br/> <span data-ttu-id="a2370-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-188">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-189">driver's license</span></span>  <br/> <span data-ttu-id="a2370-190">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-190">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-191">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-191">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-192">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-192">driving license number</span></span>  <br/> <span data-ttu-id="a2370-193">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-193">dlno#</span></span>  <br/> <span data-ttu-id="a2370-194">свидетелство за управление на МПС</span><span class="sxs-lookup"><span data-stu-id="a2370-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="a2370-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="a2370-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="a2370-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="a2370-196">сумпс</span></span>  <br/> <span data-ttu-id="a2370-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="a2370-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="a2370-198">Хорватия</span><span class="sxs-lookup"><span data-stu-id="a2370-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="a2370-199">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-199">Format</span></span>

<span data-ttu-id="a2370-200">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-201">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-201">Pattern</span></span>

<span data-ttu-id="a2370-202">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2370-203">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-203">Checksum</span></span>

<span data-ttu-id="a2370-204">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-205">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-205">Definition</span></span>

<span data-ttu-id="a2370-206">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-207">Регулярное выражение `Regex_croatia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-208">Найдено ключевое `Keywords_croatia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2370-209">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-209">Keywords</span></span>

<span data-ttu-id="a2370-210">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-210"></span></span>
|<span data-ttu-id="a2370-211">**Кэйвордс_кроатиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-212">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-212">dl#</span></span>  <br/> <span data-ttu-id="a2370-213">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-213">driver license</span></span>  <br/> <span data-ttu-id="a2370-214">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-214">driver license number</span></span>  <br/> <span data-ttu-id="a2370-215">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-215">driver licence</span></span>  <br/> <span data-ttu-id="a2370-216">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-216">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-217">drivers license</span></span>  <br/> <span data-ttu-id="a2370-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-218">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-219">driver's license</span></span>  <br/> <span data-ttu-id="a2370-220">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-220">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-221">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-221">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-222">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-222">driving license number</span></span>  <br/> <span data-ttu-id="a2370-223">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-223">dlno#</span></span>  <br/> <span data-ttu-id="a2370-224">возаčка дозвола</span><span class="sxs-lookup"><span data-stu-id="a2370-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="a2370-225">Кипр</span><span class="sxs-lookup"><span data-stu-id="a2370-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="a2370-226">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-226">Format</span></span>

<span data-ttu-id="a2370-227">12 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-228">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-228">Pattern</span></span>

<span data-ttu-id="a2370-229">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2370-230">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-230">Checksum</span></span>

<span data-ttu-id="a2370-231">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-232">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-232">Definition</span></span>

<span data-ttu-id="a2370-233">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-234">Регулярное выражение `Regex_cyprus_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-235">Найдено ключевое `Keywords_cyprus_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-236">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-236">Keywords</span></span>

<span data-ttu-id="a2370-237">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-237"></span></span>
|<span data-ttu-id="a2370-238">**Кэйвордс_ципрус_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-239">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-239">dl#</span></span>  <br/> <span data-ttu-id="a2370-240">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-240">driver license</span></span>  <br/> <span data-ttu-id="a2370-241">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-241">driver license number</span></span>  <br/> <span data-ttu-id="a2370-242">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-242">driver licence</span></span>  <br/> <span data-ttu-id="a2370-243">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-243">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-244">drivers license</span></span>  <br/> <span data-ttu-id="a2370-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-245">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-246">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-246">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-247">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-247">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-248">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-248">driving license number</span></span>  <br/> <span data-ttu-id="a2370-249">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-249">dlno#</span></span>  <br/> <span data-ttu-id="a2370-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="a2370-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="a2370-251">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="a2370-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="a2370-252">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-252">Format</span></span>

<span data-ttu-id="a2370-253">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-254">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-254">Pattern</span></span>

<span data-ttu-id="a2370-255">Восемь букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="a2370-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="a2370-256">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="a2370-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="a2370-257">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="a2370-257">A space (optional)</span></span>
    
- <span data-ttu-id="a2370-258">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-259">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-259">Checksum</span></span>

<span data-ttu-id="a2370-260">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-261">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-261">Definition</span></span>

<span data-ttu-id="a2370-262">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-263">Регулярное выражение `Regex_czech_republic_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-264">Найдено ключевое `Keywords_czech_republic_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2370-265">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-265">Keywords</span></span>

<span data-ttu-id="a2370-266">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-266"></span></span>
|<span data-ttu-id="a2370-267">**Кэйвордс_кзеч_републик_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-268">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-268">dl#</span></span>  <br/> <span data-ttu-id="a2370-269">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-269">driver license</span></span>  <br/> <span data-ttu-id="a2370-270">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-270">driver license number</span></span>  <br/> <span data-ttu-id="a2370-271">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-271">driver licence</span></span>  <br/> <span data-ttu-id="a2370-272">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-272">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-273">drivers license</span></span>  <br/> <span data-ttu-id="a2370-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-274">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-275">driver's license</span></span>  <br/> <span data-ttu-id="a2370-276">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-276">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-277">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-277">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-278">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-278">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-279">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-279">driving license number</span></span>  <br/> <span data-ttu-id="a2370-280">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-280">dlno#</span></span>  <br/> <span data-ttu-id="a2370-281">řидиčскý прúказ</span><span class="sxs-lookup"><span data-stu-id="a2370-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="a2370-282">Дания</span><span class="sxs-lookup"><span data-stu-id="a2370-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="a2370-283">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-283">Format</span></span>

<span data-ttu-id="a2370-284">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-285">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-285">Pattern</span></span>

<span data-ttu-id="a2370-286">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2370-287">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-287">Checksum</span></span>

<span data-ttu-id="a2370-288">Да</span><span class="sxs-lookup"><span data-stu-id="a2370-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-289">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-289">Definition</span></span>

<span data-ttu-id="a2370-290">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-291">Регулярное выражение `Regex_denmark_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-292">Найдено ключевое `Keywords_denmark_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a2370-293">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-293">Keywords</span></span>

<span data-ttu-id="a2370-294">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-294"></span></span>
|<span data-ttu-id="a2370-295">**Кэйвордс_денмарк_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-296">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-296">dl#</span></span>  <br/> <span data-ttu-id="a2370-297">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-297">driver license</span></span>  <br/> <span data-ttu-id="a2370-298">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-298">driver license number</span></span>  <br/> <span data-ttu-id="a2370-299">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-299">driver licence</span></span>  <br/> <span data-ttu-id="a2370-300">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-300">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-301">drivers license</span></span>  <br/> <span data-ttu-id="a2370-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-302">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-303">driver's license</span></span>  <br/> <span data-ttu-id="a2370-304">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-304">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-305">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-305">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-306">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-306">driving license number</span></span>  <br/> <span data-ttu-id="a2370-307">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-307">dlno#</span></span>  <br/> <span data-ttu-id="a2370-308">кøрекорт</span><span class="sxs-lookup"><span data-stu-id="a2370-308">kørekort</span></span>  <br/> <span data-ttu-id="a2370-309">кøрекортнуммер</span><span class="sxs-lookup"><span data-stu-id="a2370-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="a2370-310">Эстония</span><span class="sxs-lookup"><span data-stu-id="a2370-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="a2370-311">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-311">Format</span></span>

<span data-ttu-id="a2370-312">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-313">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-313">Pattern</span></span>

<span data-ttu-id="a2370-314">Две буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="a2370-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a2370-315">Буквы "ET" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="a2370-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a2370-316">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-317">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-317">Checksum</span></span>

<span data-ttu-id="a2370-318">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-319">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-319">Definition</span></span>

<span data-ttu-id="a2370-320">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-321">Регулярное выражение `Regex_estonia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-322">Найдено ключевое `Keywords_estonia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-323">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-323">Keywords</span></span>

<span data-ttu-id="a2370-324">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-324"></span></span>
|<span data-ttu-id="a2370-325">**Кэйвордс_естониа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-326">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-326">dl#</span></span>  <br/> <span data-ttu-id="a2370-327">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-327">driver license</span></span>  <br/> <span data-ttu-id="a2370-328">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-328">driver license number</span></span>  <br/> <span data-ttu-id="a2370-329">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-329">driver license number</span></span>  <br/> <span data-ttu-id="a2370-330">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-330">driver licence</span></span>  <br/> <span data-ttu-id="a2370-331">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-331">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-332">drivers license</span></span>  <br/> <span data-ttu-id="a2370-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-333">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-334">driver's license</span></span>  <br/> <span data-ttu-id="a2370-335">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-335">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-336">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-336">driving license number</span></span>  <br/> <span data-ttu-id="a2370-337">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-337">dlno#</span></span>  <br/> <span data-ttu-id="a2370-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a2370-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="a2370-339">Финляндия</span><span class="sxs-lookup"><span data-stu-id="a2370-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="a2370-340">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-340">Format</span></span>

<span data-ttu-id="a2370-341">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="a2370-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-342">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-342">Pattern</span></span>

<span data-ttu-id="a2370-343">10 цифр, содержащих дефис:</span><span class="sxs-lookup"><span data-stu-id="a2370-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a2370-344">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="a2370-344">Six digits</span></span> 
    
- <span data-ttu-id="a2370-345">дефис;</span><span class="sxs-lookup"><span data-stu-id="a2370-345">A hyphen</span></span>
    
-  <span data-ttu-id="a2370-346">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="a2370-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a2370-347">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-347">Checksum</span></span>

<span data-ttu-id="a2370-348">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-349">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-349">Definition</span></span>

<span data-ttu-id="a2370-350">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-351">Регулярное выражение `Regex_finland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-352">Найдено ключевое `Keywords_finland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-353">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-353">Keywords</span></span>

<span data-ttu-id="a2370-354">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-354"></span></span>
|<span data-ttu-id="a2370-355">**Кэйвордс_финланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-356">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-356">dl#</span></span>  <br/> <span data-ttu-id="a2370-357">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-357">driver license</span></span>  <br/> <span data-ttu-id="a2370-358">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-358">driver license number</span></span>  <br/> <span data-ttu-id="a2370-359">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-359">driver licence</span></span>  <br/> <span data-ttu-id="a2370-360">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-360">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-361">drivers license</span></span>  <br/> <span data-ttu-id="a2370-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-362">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-363">driver's license</span></span>  <br/> <span data-ttu-id="a2370-364">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-364">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-365">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-365">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-366">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-366">driving license number</span></span>  <br/> <span data-ttu-id="a2370-367">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-367">dlno#</span></span>  <br/> <span data-ttu-id="a2370-368">ажокортти</span><span class="sxs-lookup"><span data-stu-id="a2370-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="a2370-369">Франция</span><span class="sxs-lookup"><span data-stu-id="a2370-369">France</span></span>

<span data-ttu-id="a2370-370">Дополнительные сведения см. в разделе "номер водительского удостоверения для Франции" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a2370-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="a2370-371">Германия</span><span class="sxs-lookup"><span data-stu-id="a2370-371">Germany</span></span>

<span data-ttu-id="a2370-372">Дополнительные сведения можно найти в разделе "номер водительского удостоверения для немецкого драйвера" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a2370-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="a2370-373">Греция</span><span class="sxs-lookup"><span data-stu-id="a2370-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="a2370-374">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-374">Format</span></span>

<span data-ttu-id="a2370-375">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-376">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-376">Pattern</span></span>

 <span data-ttu-id="a2370-377">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a2370-378">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-378">Checksum</span></span>

<span data-ttu-id="a2370-379">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-380">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-380">Definition</span></span>

<span data-ttu-id="a2370-381">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-382">Регулярное выражение `Regex_greece_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-383">Найдено ключевое `Keywords_greece_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-384">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-384">Keywords</span></span>

<span data-ttu-id="a2370-385">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-385"></span></span>
|<span data-ttu-id="a2370-386">**Кэйвордс_грице_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-387">Файл</span><span class="sxs-lookup"><span data-stu-id="a2370-387">dlL#</span></span>  <br/> <span data-ttu-id="a2370-388">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-388">driver license</span></span>  <br/> <span data-ttu-id="a2370-389">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-389">driver license number</span></span>  <br/> <span data-ttu-id="a2370-390">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-390">driver licence</span></span>  <br/> <span data-ttu-id="a2370-391">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-391">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-392">drivers license</span></span>  <br/> <span data-ttu-id="a2370-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-393">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-394">driver's license</span></span>  <br/> <span data-ttu-id="a2370-395">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-395">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-396">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-396">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-397">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-397">driving license number</span></span>  <br/> <span data-ttu-id="a2370-398">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-398">dlno#</span></span>  <br/> <span data-ttu-id="a2370-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="a2370-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="a2370-400">Адеиа одигисис</span><span class="sxs-lookup"><span data-stu-id="a2370-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="a2370-401">Венгрия</span><span class="sxs-lookup"><span data-stu-id="a2370-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="a2370-402">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-402">Format</span></span>

<span data-ttu-id="a2370-403">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-404">Pattern</span></span>

<span data-ttu-id="a2370-405">Две буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="a2370-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a2370-406">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="a2370-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a2370-407">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-408">Checksum</span></span>

<span data-ttu-id="a2370-409">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-410">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-410">Definition</span></span>

<span data-ttu-id="a2370-411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-412">Регулярное выражение `Regex_hungary_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-413">Найдено ключевое `Keywords_hungary_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-414">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-414">Keywords</span></span>

<span data-ttu-id="a2370-415">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-415"></span></span>
|<span data-ttu-id="a2370-416">**Кэйвордс_хунгари_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-417">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-417">dl#</span></span>  <br/> <span data-ttu-id="a2370-418">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-418">driver license</span></span>  <br/> <span data-ttu-id="a2370-419">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-419">driver license number</span></span>  <br/> <span data-ttu-id="a2370-420">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-420">driver licence</span></span>  <br/> <span data-ttu-id="a2370-421">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-421">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-422">drivers license</span></span>  <br/> <span data-ttu-id="a2370-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-423">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-424">driver's license</span></span>  <br/> <span data-ttu-id="a2370-425">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-425">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-426">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-426">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-427">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-427">driving license number</span></span>  <br/> <span data-ttu-id="a2370-428">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-428">dlno#</span></span>  <br/> <span data-ttu-id="a2370-429">везетои енжедели</span><span class="sxs-lookup"><span data-stu-id="a2370-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="a2370-430">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="a2370-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="a2370-431">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-431">Format</span></span>

<span data-ttu-id="a2370-432">Шесть цифр, за которыми следуют четыре буквы</span><span class="sxs-lookup"><span data-stu-id="a2370-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-433">Pattern</span></span>

<span data-ttu-id="a2370-434">Шесть цифр и четыре буквы:</span><span class="sxs-lookup"><span data-stu-id="a2370-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="a2370-435">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="a2370-435">Six digits</span></span>
    
- <span data-ttu-id="a2370-436">Четыре буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="a2370-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-437">Checksum</span></span>

<span data-ttu-id="a2370-438">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-439">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-439">Definition</span></span>

<span data-ttu-id="a2370-440">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-441">Регулярное выражение `Regex_ireland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-442">Найдено ключевое `Keywords_ireland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-443">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-443">Keywords</span></span>

<span data-ttu-id="a2370-444">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-444"></span></span>
|<span data-ttu-id="a2370-445">**Кэйвордс_иреланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-446">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-446">dl#</span></span>  <br/> <span data-ttu-id="a2370-447">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-447">driver license</span></span>  <br/> <span data-ttu-id="a2370-448">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-448">driver license number</span></span>  <br/> <span data-ttu-id="a2370-449">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-449">driver licence</span></span>  <br/> <span data-ttu-id="a2370-450">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-450">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-451">drivers license</span></span>  <br/> <span data-ttu-id="a2370-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-452">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-453">driver's license</span></span>  <br/> <span data-ttu-id="a2370-454">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-454">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-455">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-455">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-456">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-456">driving license number</span></span>  <br/> <span data-ttu-id="a2370-457">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-457">dlno#</span></span>  <br/> <span data-ttu-id="a2370-458">цеадúнас тиомáна</span><span class="sxs-lookup"><span data-stu-id="a2370-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="a2370-459">Италия</span><span class="sxs-lookup"><span data-stu-id="a2370-459">Italy</span></span>

<span data-ttu-id="a2370-460">Дополнительные сведения см. в разделе "номер водительского удостоверения для Италии" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a2370-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="a2370-461">Латвия</span><span class="sxs-lookup"><span data-stu-id="a2370-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="a2370-462">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-462">Format</span></span>

<span data-ttu-id="a2370-463">Три буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-464">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-464">Pattern</span></span>

<span data-ttu-id="a2370-465">Три буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="a2370-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="a2370-466">Три буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="a2370-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a2370-467">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-468">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-468">Checksum</span></span>

<span data-ttu-id="a2370-469">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-470">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-470">Definition</span></span>

<span data-ttu-id="a2370-471">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-472">Регулярное выражение `Regex_latvia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-473">Найдено ключевое `Keywords_latvia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-474">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-474">Keywords</span></span>

<span data-ttu-id="a2370-475">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-475"></span></span>
|<span data-ttu-id="a2370-476">**Кэйвордс_латвиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-477">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-477">dl#</span></span>  <br/> <span data-ttu-id="a2370-478">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-478">driver license</span></span>  <br/> <span data-ttu-id="a2370-479">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-479">driver license number</span></span>  <br/> <span data-ttu-id="a2370-480">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-480">driver licence</span></span>  <br/> <span data-ttu-id="a2370-481">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-481">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-482">drivers license</span></span>  <br/> <span data-ttu-id="a2370-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-483">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-484">driver's license</span></span>  <br/> <span data-ttu-id="a2370-485">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-485">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-486">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-486">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-487">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-487">driving license number</span></span>  <br/> <span data-ttu-id="a2370-488">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-488">dlno#</span></span>  <br/> <span data-ttu-id="a2370-489">аутовадīтāжа аплиекīба</span><span class="sxs-lookup"><span data-stu-id="a2370-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="a2370-490">Литва</span><span class="sxs-lookup"><span data-stu-id="a2370-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="a2370-491">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-491">Format</span></span>

<span data-ttu-id="a2370-492">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-493">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-493">Pattern</span></span>

 <span data-ttu-id="a2370-494">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a2370-495">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-495">Checksum</span></span>

<span data-ttu-id="a2370-496">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-497">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-497">Definition</span></span>

<span data-ttu-id="a2370-498">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-499">Регулярное выражение `Regex_lithuania_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-500">Найдено ключевое `Keywords_lithuania_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-501">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-501">Keywords</span></span>

<span data-ttu-id="a2370-502">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-502"></span></span>
|<span data-ttu-id="a2370-503">**Кэйвордс_лисуаниа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-504">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-504">dl#</span></span>  <br/> <span data-ttu-id="a2370-505">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-505">driver license</span></span>  <br/> <span data-ttu-id="a2370-506">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-506">driver license number</span></span>  <br/> <span data-ttu-id="a2370-507">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-507">driver licence</span></span>  <br/> <span data-ttu-id="a2370-508">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-508">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-509">drivers license</span></span>  <br/> <span data-ttu-id="a2370-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-510">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-511">driver's license</span></span>  <br/> <span data-ttu-id="a2370-512">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-512">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-513">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-513">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-514">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-514">driving license number</span></span>  <br/> <span data-ttu-id="a2370-515">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-515">dlno#</span></span>  <br/> <span data-ttu-id="a2370-516">ваируотожо паžимėжимас</span><span class="sxs-lookup"><span data-stu-id="a2370-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="a2370-517">Луксембург</span><span class="sxs-lookup"><span data-stu-id="a2370-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="a2370-518">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-518">Format</span></span>

<span data-ttu-id="a2370-519">Шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-520">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-520">Pattern</span></span>

 <span data-ttu-id="a2370-521">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a2370-522">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-522">Checksum</span></span>

<span data-ttu-id="a2370-523">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-524">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-524">Definition</span></span>

<span data-ttu-id="a2370-525">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-526">Регулярное выражение `Regex_luxemburg_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-527">Найдено ключевое `Keywords_luxemburg_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-528">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-528">Keywords</span></span>

<span data-ttu-id="a2370-529">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-529"></span></span>
|<span data-ttu-id="a2370-530">**Кэйвордс_луксембург_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-531">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-531">dl#</span></span>  <br/> <span data-ttu-id="a2370-532">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-532">driver license</span></span>  <br/> <span data-ttu-id="a2370-533">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-533">driver license number</span></span>  <br/> <span data-ttu-id="a2370-534">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-534">driver licence</span></span>  <br/> <span data-ttu-id="a2370-535">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-535">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-536">drivers license</span></span>  <br/> <span data-ttu-id="a2370-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-537">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-538">driver's license</span></span>  <br/> <span data-ttu-id="a2370-539">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-539">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-540">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-540">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-541">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-541">driving license number</span></span>  <br/> <span data-ttu-id="a2370-542">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-542">dlno#</span></span>  <br/> <span data-ttu-id="a2370-543">фахрерлаубнис</span><span class="sxs-lookup"><span data-stu-id="a2370-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="a2370-544">Мальта</span><span class="sxs-lookup"><span data-stu-id="a2370-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="a2370-545">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-545">Format</span></span>

<span data-ttu-id="a2370-546">Сочетание двух символов и шести цифр в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="a2370-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-547">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-547">Pattern</span></span>

<span data-ttu-id="a2370-548">Сочетание двух символов и шести цифр:</span><span class="sxs-lookup"><span data-stu-id="a2370-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="a2370-549">Два символа (цифры или буквы без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="a2370-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="a2370-550">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="a2370-550">A space (optional)</span></span>
    
- <span data-ttu-id="a2370-551">три цифры; </span><span class="sxs-lookup"><span data-stu-id="a2370-551">Three digits</span></span>
    
- <span data-ttu-id="a2370-552">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="a2370-552">A space (optional)</span></span>
    
- <span data-ttu-id="a2370-553">Три цифры</span><span class="sxs-lookup"><span data-stu-id="a2370-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-554">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-554">Checksum</span></span>

<span data-ttu-id="a2370-555">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-556">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-556">Definition</span></span>

<span data-ttu-id="a2370-557">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-558">Регулярное выражение `Regex_malta_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-559">Найдено ключевое `Keywords_malta_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-560">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-560">Keywords</span></span>

<span data-ttu-id="a2370-561">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-561"></span></span>
|<span data-ttu-id="a2370-562">**Кэйвордс_малта_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-563">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-563">dl#</span></span>  <br/> <span data-ttu-id="a2370-564">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-564">driver license</span></span>  <br/> <span data-ttu-id="a2370-565">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-565">driver license number</span></span>  <br/> <span data-ttu-id="a2370-566">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-566">driver licence</span></span>  <br/> <span data-ttu-id="a2370-567">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-567">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-568">drivers license</span></span>  <br/> <span data-ttu-id="a2370-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-569">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-570">driver's license</span></span>  <br/> <span data-ttu-id="a2370-571">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-571">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-572">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-572">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-573">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-573">driving license number</span></span>  <br/> <span data-ttu-id="a2370-574">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-574">dlno#</span></span>  <br/> <span data-ttu-id="a2370-575">лиċензжаные зада Севкан</span><span class="sxs-lookup"><span data-stu-id="a2370-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="a2370-576">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="a2370-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="a2370-577">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-577">Format</span></span>

<span data-ttu-id="a2370-578">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-579">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-579">Pattern</span></span>

<span data-ttu-id="a2370-580">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2370-581">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-581">Checksum</span></span>

<span data-ttu-id="a2370-582">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-583">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-583">Definition</span></span>

<span data-ttu-id="a2370-584">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-585">Регулярное выражение `Regex_netherlands_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-586">Найдено ключевое `Keywords_netherlands_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-587">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-587">Keywords</span></span>

<span data-ttu-id="a2370-588">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-588"></span></span>
|<span data-ttu-id="a2370-589">**Кэйвордс_несерландс_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-590">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-590">dl#</span></span>  <br/> <span data-ttu-id="a2370-591">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-591">driver license</span></span>  <br/> <span data-ttu-id="a2370-592">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-592">driver license number</span></span>  <br/> <span data-ttu-id="a2370-593">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-593">driver licence</span></span>  <br/> <span data-ttu-id="a2370-594">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-594">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-595">drivers license</span></span>  <br/> <span data-ttu-id="a2370-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-596">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-597">driver's license</span></span>  <br/> <span data-ttu-id="a2370-598">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-598">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-599">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-599">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-600">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-600">driving license number</span></span>  <br/> <span data-ttu-id="a2370-601">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-601">dlno#</span></span>  <br/> <span data-ttu-id="a2370-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a2370-602">permis de conduire</span></span>  <br/> <span data-ttu-id="a2370-603">рижбевижс</span><span class="sxs-lookup"><span data-stu-id="a2370-603">rijbewijs</span></span>  <br/> <span data-ttu-id="a2370-604">рижбевижснуммер</span><span class="sxs-lookup"><span data-stu-id="a2370-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="a2370-605">Польша</span><span class="sxs-lookup"><span data-stu-id="a2370-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="a2370-606">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-606">Format</span></span>

<span data-ttu-id="a2370-607">14 цифр, содержащих 2 косых черты.</span><span class="sxs-lookup"><span data-stu-id="a2370-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-608">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-608">Pattern</span></span>

<span data-ttu-id="a2370-609">14 цифр и 2 косых черт:</span><span class="sxs-lookup"><span data-stu-id="a2370-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="a2370-610">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="a2370-610">Five digits</span></span> 
    
- <span data-ttu-id="a2370-611">косая черта;</span><span class="sxs-lookup"><span data-stu-id="a2370-611">A forward slash</span></span>
    
- <span data-ttu-id="a2370-612">Две цифры</span><span class="sxs-lookup"><span data-stu-id="a2370-612">Two digits</span></span>
    
- <span data-ttu-id="a2370-613">косая черта;</span><span class="sxs-lookup"><span data-stu-id="a2370-613">A forward slash</span></span>
    
- <span data-ttu-id="a2370-614">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-615">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-615">Checksum</span></span>

<span data-ttu-id="a2370-616">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-617">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-617">Definition</span></span>

<span data-ttu-id="a2370-618">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-619">Регулярное выражение `Regex_poland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-620">Найдено ключевое `Keywords_poland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-621">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-621">Keywords</span></span>

<span data-ttu-id="a2370-622">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-622"></span></span>
|<span data-ttu-id="a2370-623">**Кэйвордс_поланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-624">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-624">dl#</span></span>  <br/> <span data-ttu-id="a2370-625">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-625">driver license</span></span>  <br/> <span data-ttu-id="a2370-626">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-626">driver license number</span></span>  <br/> <span data-ttu-id="a2370-627">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-627">driver licence</span></span>  <br/> <span data-ttu-id="a2370-628">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-628">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-629">drivers license</span></span>  <br/> <span data-ttu-id="a2370-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-630">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-631">driver's license</span></span>  <br/> <span data-ttu-id="a2370-632">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-632">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-633">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-633">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-634">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-634">driving license number</span></span>  <br/> <span data-ttu-id="a2370-635">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-635">dlno#</span></span>  <br/> <span data-ttu-id="a2370-636">право жазди</span><span class="sxs-lookup"><span data-stu-id="a2370-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="a2370-637">Португалия</span><span class="sxs-lookup"><span data-stu-id="a2370-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="a2370-638">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-638">Format</span></span>

<span data-ttu-id="a2370-639">Две буквы, за которыми следуют семь чисел в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="a2370-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-640">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-640">Pattern</span></span>

<span data-ttu-id="a2370-641">Две буквы, за которыми следуют семь цифр со специальными символами:</span><span class="sxs-lookup"><span data-stu-id="a2370-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="a2370-642">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="a2370-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a2370-643">дефис;</span><span class="sxs-lookup"><span data-stu-id="a2370-643">A hyphen</span></span>
    
- <span data-ttu-id="a2370-644">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="a2370-644">Six digits</span></span>
    
- <span data-ttu-id="a2370-645">Пробел</span><span class="sxs-lookup"><span data-stu-id="a2370-645">A space</span></span>
    
- <span data-ttu-id="a2370-646">одна цифра.</span><span class="sxs-lookup"><span data-stu-id="a2370-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-647">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-647">Checksum</span></span>

<span data-ttu-id="a2370-648">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-649">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-649">Definition</span></span>

<span data-ttu-id="a2370-650">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-651">Регулярное выражение `Regex_portugal_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-652">Найдено ключевое `Keywords_portugal_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-653">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-653">Keywords</span></span>

<span data-ttu-id="a2370-654">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-654"></span></span>
|<span data-ttu-id="a2370-655">**Кэйвордс_португал_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-656">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-656">dl#</span></span>  <br/> <span data-ttu-id="a2370-657">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-657">driver license</span></span>  <br/> <span data-ttu-id="a2370-658">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-658">driver license number</span></span>  <br/> <span data-ttu-id="a2370-659">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-659">driver licence</span></span>  <br/> <span data-ttu-id="a2370-660">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-660">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-661">drivers license</span></span>  <br/> <span data-ttu-id="a2370-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-662">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-663">driver's license</span></span>  <br/> <span data-ttu-id="a2370-664">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-664">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-665">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-665">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-666">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-666">driving license number</span></span>  <br/> <span data-ttu-id="a2370-667">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-667">dlno#</span></span>  <br/> <span data-ttu-id="a2370-668">картеира de моториста</span><span class="sxs-lookup"><span data-stu-id="a2370-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="a2370-669">Румыния</span><span class="sxs-lookup"><span data-stu-id="a2370-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="a2370-670">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-670">Format</span></span>

<span data-ttu-id="a2370-671">Один символ, за которым следуют восемь цифр</span><span class="sxs-lookup"><span data-stu-id="a2370-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-672">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-672">Pattern</span></span>

<span data-ttu-id="a2370-673">Один символ, за которым следуют восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="a2370-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="a2370-674">Одна буква (без учета регистра) или цифра</span><span class="sxs-lookup"><span data-stu-id="a2370-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="a2370-675">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-676">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-676">Checksum</span></span>

<span data-ttu-id="a2370-677">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-678">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-678">Definition</span></span>

<span data-ttu-id="a2370-679">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-680">Регулярное выражение `Regex_romania_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-681">Найдено ключевое `Keywords_romania_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-682">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-682">Keywords</span></span>

<span data-ttu-id="a2370-683">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-683"></span></span>
|<span data-ttu-id="a2370-684">**Кэйвордс_романиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-685">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-685">dl#</span></span>  <br/> <span data-ttu-id="a2370-686">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-686">driver license</span></span>  <br/> <span data-ttu-id="a2370-687">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-687">driver license number</span></span>  <br/> <span data-ttu-id="a2370-688">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-688">driver licence</span></span>  <br/> <span data-ttu-id="a2370-689">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-689">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-690">drivers license</span></span>  <br/> <span data-ttu-id="a2370-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-691">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-692">driver's license</span></span>  <br/> <span data-ttu-id="a2370-693">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-693">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-694">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-694">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-695">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-695">driving license number</span></span>  <br/> <span data-ttu-id="a2370-696">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-696">dlno#</span></span>  <br/> <span data-ttu-id="a2370-697">разрешение de кондуцере</span><span class="sxs-lookup"><span data-stu-id="a2370-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="a2370-698">Словакия</span><span class="sxs-lookup"><span data-stu-id="a2370-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="a2370-699">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-699">Format</span></span>

<span data-ttu-id="a2370-700">Один символ, за которым следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-701">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-701">Pattern</span></span>

<span data-ttu-id="a2370-702">Один символ, за которым следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="a2370-703">Одна буква (без учета регистра) или цифра</span><span class="sxs-lookup"><span data-stu-id="a2370-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="a2370-704">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a2370-705">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-705">Checksum</span></span>

<span data-ttu-id="a2370-706">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-707">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-707">Definition</span></span>

<span data-ttu-id="a2370-708">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-709">Регулярное выражение `Regex_slovakia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-710">Найдено ключевое `Keywords_slovakia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-711">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-711">Keywords</span></span>

<span data-ttu-id="a2370-712">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-712"></span></span>
|<span data-ttu-id="a2370-713">**Кэйвордс_словакиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-714">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-714">dl#</span></span>  <br/> <span data-ttu-id="a2370-715">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-715">driver license</span></span>  <br/> <span data-ttu-id="a2370-716">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-716">driver license number</span></span>  <br/> <span data-ttu-id="a2370-717">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-717">driver licence</span></span>  <br/> <span data-ttu-id="a2370-718">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-718">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-719">drivers license</span></span>  <br/> <span data-ttu-id="a2370-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-720">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-721">driver's license</span></span>  <br/> <span data-ttu-id="a2370-722">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-722">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-723">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-723">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-724">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-724">driving license number</span></span>  <br/> <span data-ttu-id="a2370-725">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-725">dlno#</span></span>  <br/> <span data-ttu-id="a2370-726">водиčскý преуказ</span><span class="sxs-lookup"><span data-stu-id="a2370-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="a2370-727">Словения</span><span class="sxs-lookup"><span data-stu-id="a2370-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="a2370-728">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-728">Format</span></span>

<span data-ttu-id="a2370-729">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="a2370-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-730">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-730">Pattern</span></span>

<span data-ttu-id="a2370-731">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a2370-732">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-732">Checksum</span></span>

<span data-ttu-id="a2370-733">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-734">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-734">Definition</span></span>

<span data-ttu-id="a2370-735">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-736">Регулярное выражение `Regex_slovenia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-737">Найдено ключевое `Keywords_slovenia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-738">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-738">Keywords</span></span>

<span data-ttu-id="a2370-739">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-739"></span></span>
|<span data-ttu-id="a2370-740">**Кэйвордс_словениа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-741">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-741">dl#</span></span>  <br/> <span data-ttu-id="a2370-742">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-742">driver license</span></span>  <br/> <span data-ttu-id="a2370-743">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-743">driver license number</span></span>  <br/> <span data-ttu-id="a2370-744">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-744">driver licence</span></span>  <br/> <span data-ttu-id="a2370-745">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-745">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-746">drivers license</span></span>  <br/> <span data-ttu-id="a2370-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-747">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-748">driver's license</span></span>  <br/> <span data-ttu-id="a2370-749">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-749">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-750">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-750">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-751">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-751">driving license number</span></span>  <br/> <span data-ttu-id="a2370-752">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-752">dlno#</span></span>  <br/> <span data-ttu-id="a2370-753">возниšко доволженже</span><span class="sxs-lookup"><span data-stu-id="a2370-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="a2370-754">Испания</span><span class="sxs-lookup"><span data-stu-id="a2370-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="a2370-755">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-755">Format</span></span>

<span data-ttu-id="a2370-756">Восемь цифр, за которыми следует один символ</span><span class="sxs-lookup"><span data-stu-id="a2370-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-757">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-757">Pattern</span></span>

<span data-ttu-id="a2370-758">Восемь цифр, за которыми следует один символ:</span><span class="sxs-lookup"><span data-stu-id="a2370-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="a2370-759">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="a2370-759">Eight digits</span></span> 
    
- <span data-ttu-id="a2370-760">Одна цифра или буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="a2370-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-761">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-761">Checksum</span></span>

<span data-ttu-id="a2370-762">Да</span><span class="sxs-lookup"><span data-stu-id="a2370-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-763">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-763">Definition</span></span>

<span data-ttu-id="a2370-764">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-765">Функция `Func_spain_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-766">Найдено ключевое `Keywords_spain_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a2370-767">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-767">Keywords</span></span>

<span data-ttu-id="a2370-768">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-768"></span></span>
|<span data-ttu-id="a2370-769">**Кэйвордс_спаин_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-770">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-770">dlno#</span></span>  <br/> <span data-ttu-id="a2370-771">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-771">dl#</span></span>  <br/> <span data-ttu-id="a2370-772">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-772">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-773">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-773">driver licence</span></span>  <br/> <span data-ttu-id="a2370-774">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-774">driver license</span></span>  <br/> <span data-ttu-id="a2370-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-775">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-776">drivers license</span></span>  <br/> <span data-ttu-id="a2370-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="a2370-777">driver's licence</span></span>  <br/> <span data-ttu-id="a2370-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-778">driver's license</span></span>  <br/> <span data-ttu-id="a2370-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="a2370-779">driving licence</span></span>  <br/> <span data-ttu-id="a2370-780">driving license</span><span class="sxs-lookup"><span data-stu-id="a2370-780">driving license</span></span>  <br/> <span data-ttu-id="a2370-781">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-781">driver licence number</span></span>  <br/> <span data-ttu-id="a2370-782">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-782">driver license number</span></span>  <br/> <span data-ttu-id="a2370-783">драйвер номер лицензии</span><span class="sxs-lookup"><span data-stu-id="a2370-783">drivers licence number</span></span>  <br/> <span data-ttu-id="a2370-784">номер лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="a2370-784">drivers license number</span></span>  <br/> <span data-ttu-id="a2370-785">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-785">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-786">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-786">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-787">номер водительской лицензии</span><span class="sxs-lookup"><span data-stu-id="a2370-787">driving licence number</span></span>  <br/> <span data-ttu-id="a2370-788">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-788">driving license number</span></span>  <br/> <span data-ttu-id="a2370-789">движущие разрешение</span><span class="sxs-lookup"><span data-stu-id="a2370-789">driving permit</span></span>  <br/> <span data-ttu-id="a2370-790">движущие число разрешений</span><span class="sxs-lookup"><span data-stu-id="a2370-790">driving permit number</span></span>  <br/> <span data-ttu-id="a2370-791">пермисо de кондукЦиóн</span><span class="sxs-lookup"><span data-stu-id="a2370-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="a2370-792">пермисо кондукЦиóн</span><span class="sxs-lookup"><span data-stu-id="a2370-792">permiso conducción</span></span>  <br/> <span data-ttu-id="a2370-793">нúмеро лиценЦиа кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="a2370-794">нúмеро de карнет де кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="a2370-795">нúмеро карнет кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="a2370-796">лиценЦиа кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-796">licencia conducir</span></span>  <br/> <span data-ttu-id="a2370-797">нúмеро de пермисо де кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="a2370-798">нúмеро де пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="a2370-799">нúмеро пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="a2370-800">пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-800">permiso conducir</span></span>  <br/> <span data-ttu-id="a2370-801">лиценЦиа de манежо</span><span class="sxs-lookup"><span data-stu-id="a2370-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="a2370-802">El карнет de кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="a2370-803">Карнет кондуЦир</span><span class="sxs-lookup"><span data-stu-id="a2370-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="a2370-804">Швеция</span><span class="sxs-lookup"><span data-stu-id="a2370-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="a2370-805">Format</span><span class="sxs-lookup"><span data-stu-id="a2370-805">Format</span></span>

<span data-ttu-id="a2370-806">Десять цифр, содержащие дефис</span><span class="sxs-lookup"><span data-stu-id="a2370-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a2370-807">Шаблон</span><span class="sxs-lookup"><span data-stu-id="a2370-807">Pattern</span></span>

<span data-ttu-id="a2370-808">Десять цифр, содержащих дефис:</span><span class="sxs-lookup"><span data-stu-id="a2370-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a2370-809">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="a2370-809">Six digits</span></span> 
    
- <span data-ttu-id="a2370-810">дефис;</span><span class="sxs-lookup"><span data-stu-id="a2370-810">A hyphen</span></span>
    
- <span data-ttu-id="a2370-811">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="a2370-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a2370-812">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="a2370-812">Checksum</span></span>

<span data-ttu-id="a2370-813">Нет</span><span class="sxs-lookup"><span data-stu-id="a2370-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a2370-814">Определение</span><span class="sxs-lookup"><span data-stu-id="a2370-814">Definition</span></span>

<span data-ttu-id="a2370-815">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="a2370-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a2370-816">Регулярное выражение `Regex_sweden_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="a2370-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a2370-817">Найдено ключевое `Keywords_sweden_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="a2370-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="a2370-818">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="a2370-818">Keywords</span></span>

<span data-ttu-id="a2370-819">| |</span><span class="sxs-lookup"><span data-stu-id="a2370-819"></span></span>
|<span data-ttu-id="a2370-820">**Кэйвордс_сведен_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="a2370-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a2370-821">DL</span><span class="sxs-lookup"><span data-stu-id="a2370-821">dl#</span></span>  <br/> <span data-ttu-id="a2370-822">driver license</span><span class="sxs-lookup"><span data-stu-id="a2370-822">driver license</span></span>  <br/> <span data-ttu-id="a2370-823">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-823">driver license number</span></span>  <br/> <span data-ttu-id="a2370-824">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-824">driver licence</span></span>  <br/> <span data-ttu-id="a2370-825">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="a2370-825">drivers lic.</span></span>  <br/> <span data-ttu-id="a2370-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="a2370-826">drivers license</span></span>  <br/> <span data-ttu-id="a2370-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a2370-827">drivers licence</span></span>  <br/> <span data-ttu-id="a2370-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="a2370-828">driver's license</span></span>  <br/> <span data-ttu-id="a2370-829">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-829">driver's license number</span></span>  <br/> <span data-ttu-id="a2370-830">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="a2370-830">driver's licence number</span></span>  <br/> <span data-ttu-id="a2370-831">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="a2370-831">driving license number</span></span>  <br/> <span data-ttu-id="a2370-832">длно #</span><span class="sxs-lookup"><span data-stu-id="a2370-832">dlno#</span></span>  <br/> <span data-ttu-id="a2370-833">кöркорт</span><span class="sxs-lookup"><span data-stu-id="a2370-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="a2370-834">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="a2370-834">UK</span></span>

<span data-ttu-id="a2370-835">Дополнительные сведения см. в разделе "Великобритания</span><span class="sxs-lookup"><span data-stu-id="a2370-835">For details, see the section "U.K.</span></span> <span data-ttu-id="a2370-836">Номер водительского удостоверения, в [котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a2370-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2370-837">См. также</span><span class="sxs-lookup"><span data-stu-id="a2370-837">See also</span></span>

[<span data-ttu-id="a2370-838">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="a2370-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

