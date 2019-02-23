---
title: Номер водительского удостоверения для драйвера ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации номера лицензии для драйвера ЕС. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: 86be7b52aed7581fd62ab595ac2c4b63ab33aab3
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217749"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="0cd13-104">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="0cd13-104">EU Driver's License Number</span></span>

<span data-ttu-id="0cd13-p102">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации номера лицензии для драйвера ЕС. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="0cd13-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="0cd13-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="0cd13-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-108">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-108">Format</span></span>

<span data-ttu-id="0cd13-109">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-110">Pattern</span></span>

<span data-ttu-id="0cd13-111">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0cd13-112">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-112">Checksum</span></span>

<span data-ttu-id="0cd13-113">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-114">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-114">Definition</span></span>

<span data-ttu-id="0cd13-115">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-116">Регулярное выражение `Regex_austria_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-117">Найдено ключевое `Keywords_austria_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="0cd13-118">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-118">Keywords</span></span>

<span data-ttu-id="0cd13-119">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-119"></span></span>
|<span data-ttu-id="0cd13-120">**Кэйвордс_аустриа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-121">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-121">dl#</span></span>  <br/> <span data-ttu-id="0cd13-122">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-122">driver license</span></span>  <br/> <span data-ttu-id="0cd13-123">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-123">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-124">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-124">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-125">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-125">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-126">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-127">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-127">driver's licence</span></span>  <br/> <span data-ttu-id="0cd13-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-128">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-129">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-129">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-130">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="0cd13-131">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-131">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-132">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-132">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-133">фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="0cd13-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="0cd13-134">фухрерсчеин Републик остерреич</span><span class="sxs-lookup"><span data-stu-id="0cd13-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="0cd13-135">Бельгия</span><span class="sxs-lookup"><span data-stu-id="0cd13-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-136">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-136">Format</span></span>

<span data-ttu-id="0cd13-137">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-138">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-138">Pattern</span></span>

<span data-ttu-id="0cd13-139">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0cd13-140">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-140">Checksum</span></span>

<span data-ttu-id="0cd13-141">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-142">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-142">Definition</span></span>

<span data-ttu-id="0cd13-143">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-144">Регулярное выражение `Regex_belgium_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-145">Найдено ключевое `Keywords_belgium_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="0cd13-146">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-146">Keywords</span></span>

<span data-ttu-id="0cd13-147">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-147"></span></span>
|<span data-ttu-id="0cd13-148">**Кэйвордс__белгиум_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-149">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-149">dl#</span></span>  <br/> <span data-ttu-id="0cd13-150">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-150">driver license</span></span>  <br/> <span data-ttu-id="0cd13-151">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-151">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-152">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-152">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-153">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-153">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-154">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-155">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-156">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-157">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-157">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-158">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-158">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-159">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-159">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-160">рижбевижс</span><span class="sxs-lookup"><span data-stu-id="0cd13-160">rijbewijs</span></span>  <br/> <span data-ttu-id="0cd13-161">рижбевижснуммер</span><span class="sxs-lookup"><span data-stu-id="0cd13-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="0cd13-162">фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="0cd13-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="0cd13-163">фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="0cd13-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="0cd13-164">фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="0cd13-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="0cd13-165">фüхрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="0cd13-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="0cd13-166">фуехрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="0cd13-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="0cd13-167">фуехрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="0cd13-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="0cd13-168">Болгария</span><span class="sxs-lookup"><span data-stu-id="0cd13-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-169">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-169">Format</span></span>

<span data-ttu-id="0cd13-170">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-171">Pattern</span></span>

<span data-ttu-id="0cd13-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0cd13-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-173">Checksum</span></span>

<span data-ttu-id="0cd13-174">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-175">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-175">Definition</span></span>

<span data-ttu-id="0cd13-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-177">Регулярное выражение `Regex_bulgaria_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-178">Найдено ключевое `Keywords_bulgaria_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="0cd13-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-179">Keywords</span></span>

<span data-ttu-id="0cd13-180">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-180"></span></span>
|<span data-ttu-id="0cd13-181">**Кэйвордс_булгариа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-182">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-182">dl#</span></span>  <br/> <span data-ttu-id="0cd13-183">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-183">driver license</span></span>  <br/> <span data-ttu-id="0cd13-184">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-184">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-185">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-185">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-186">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-186">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-187">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-188">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-189">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-190">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-190">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-191">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-191">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-192">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-192">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-193">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-193">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-194">свидетелство за управление на МПС</span><span class="sxs-lookup"><span data-stu-id="0cd13-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="0cd13-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="0cd13-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="0cd13-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="0cd13-196">сумпс</span></span>  <br/> <span data-ttu-id="0cd13-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="0cd13-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="0cd13-198">Хорватия</span><span class="sxs-lookup"><span data-stu-id="0cd13-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-199">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-199">Format</span></span>

<span data-ttu-id="0cd13-200">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-201">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-201">Pattern</span></span>

<span data-ttu-id="0cd13-202">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0cd13-203">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-203">Checksum</span></span>

<span data-ttu-id="0cd13-204">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-205">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-205">Definition</span></span>

<span data-ttu-id="0cd13-206">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-207">Регулярное выражение `Regex_croatia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-208">Найдено ключевое `Keywords_croatia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="0cd13-209">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-209">Keywords</span></span>

<span data-ttu-id="0cd13-210">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-210"></span></span>
|<span data-ttu-id="0cd13-211">**Кэйвордс_кроатиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-212">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-212">dl#</span></span>  <br/> <span data-ttu-id="0cd13-213">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-213">driver license</span></span>  <br/> <span data-ttu-id="0cd13-214">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-214">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-215">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-215">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-216">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-216">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-217">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-218">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-219">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-220">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-220">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-221">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-221">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-222">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-222">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-223">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-223">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-224">возаčка дозвола</span><span class="sxs-lookup"><span data-stu-id="0cd13-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="0cd13-225">Кипр</span><span class="sxs-lookup"><span data-stu-id="0cd13-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-226">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-226">Format</span></span>

<span data-ttu-id="0cd13-227">12 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-228">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-228">Pattern</span></span>

<span data-ttu-id="0cd13-229">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0cd13-230">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-230">Checksum</span></span>

<span data-ttu-id="0cd13-231">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-232">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-232">Definition</span></span>

<span data-ttu-id="0cd13-233">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-234">Регулярное выражение `Regex_cyprus_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-235">Найдено ключевое `Keywords_cyprus_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-236">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-236">Keywords</span></span>

<span data-ttu-id="0cd13-237">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-237"></span></span>
|<span data-ttu-id="0cd13-238">**Кэйвордс_ципрус_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-239">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-239">dl#</span></span>  <br/> <span data-ttu-id="0cd13-240">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-240">driver license</span></span>  <br/> <span data-ttu-id="0cd13-241">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-241">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-242">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-242">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-243">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-243">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-244">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-245">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-246">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-246">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-247">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-247">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-248">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-248">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-249">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-249">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="0cd13-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="0cd13-251">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="0cd13-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-252">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-252">Format</span></span>

<span data-ttu-id="0cd13-253">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-254">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-254">Pattern</span></span>

<span data-ttu-id="0cd13-255">Восемь букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="0cd13-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="0cd13-256">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0cd13-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="0cd13-257">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="0cd13-257">A space (optional)</span></span>
    
- <span data-ttu-id="0cd13-258">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-259">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-259">Checksum</span></span>

<span data-ttu-id="0cd13-260">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-261">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-261">Definition</span></span>

<span data-ttu-id="0cd13-262">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-263">Регулярное выражение `Regex_czech_republic_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-264">Найдено ключевое `Keywords_czech_republic_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="0cd13-265">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-265">Keywords</span></span>

<span data-ttu-id="0cd13-266">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-266"></span></span>
|<span data-ttu-id="0cd13-267">**Кэйвордс_кзеч_републик_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-268">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-268">dl#</span></span>  <br/> <span data-ttu-id="0cd13-269">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-269">driver license</span></span>  <br/> <span data-ttu-id="0cd13-270">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-270">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-271">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-271">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-272">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-272">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-273">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-274">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-275">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-276">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-276">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-277">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-277">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-278">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-278">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-279">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-279">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-280">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-280">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-281">řидиčскý прúказ</span><span class="sxs-lookup"><span data-stu-id="0cd13-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="0cd13-282">Дания</span><span class="sxs-lookup"><span data-stu-id="0cd13-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-283">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-283">Format</span></span>

<span data-ttu-id="0cd13-284">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-285">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-285">Pattern</span></span>

<span data-ttu-id="0cd13-286">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0cd13-287">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-287">Checksum</span></span>

<span data-ttu-id="0cd13-288">Да</span><span class="sxs-lookup"><span data-stu-id="0cd13-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-289">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-289">Definition</span></span>

<span data-ttu-id="0cd13-290">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-291">Регулярное выражение `Regex_denmark_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-292">Найдено ключевое `Keywords_denmark_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="0cd13-293">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-293">Keywords</span></span>

<span data-ttu-id="0cd13-294">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-294"></span></span>
|<span data-ttu-id="0cd13-295">**Кэйвордс_денмарк_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-296">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-296">dl#</span></span>  <br/> <span data-ttu-id="0cd13-297">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-297">driver license</span></span>  <br/> <span data-ttu-id="0cd13-298">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-298">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-299">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-299">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-300">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-300">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-301">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-302">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-303">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-304">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-304">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-305">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-305">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-306">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-306">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-307">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-307">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-308">кøрекорт</span><span class="sxs-lookup"><span data-stu-id="0cd13-308">kørekort</span></span>  <br/> <span data-ttu-id="0cd13-309">кøрекортнуммер</span><span class="sxs-lookup"><span data-stu-id="0cd13-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="0cd13-310">Эстония</span><span class="sxs-lookup"><span data-stu-id="0cd13-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-311">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-311">Format</span></span>

<span data-ttu-id="0cd13-312">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-313">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-313">Pattern</span></span>

<span data-ttu-id="0cd13-314">Две буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="0cd13-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="0cd13-315">Буквы "ET" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0cd13-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="0cd13-316">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-317">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-317">Checksum</span></span>

<span data-ttu-id="0cd13-318">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-319">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-319">Definition</span></span>

<span data-ttu-id="0cd13-320">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-321">Регулярное выражение `Regex_estonia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-322">Найдено ключевое `Keywords_estonia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-323">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-323">Keywords</span></span>

<span data-ttu-id="0cd13-324">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-324"></span></span>
|<span data-ttu-id="0cd13-325">**Кэйвордс_естониа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-326">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-326">dl#</span></span>  <br/> <span data-ttu-id="0cd13-327">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-327">driver license</span></span>  <br/> <span data-ttu-id="0cd13-328">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-328">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-329">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-329">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-330">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-330">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-331">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-331">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-332">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-333">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-334">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-335">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-335">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-336">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-336">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-337">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-337">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="0cd13-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="0cd13-339">Финляндия</span><span class="sxs-lookup"><span data-stu-id="0cd13-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-340">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-340">Format</span></span>

<span data-ttu-id="0cd13-341">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="0cd13-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-342">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-342">Pattern</span></span>

<span data-ttu-id="0cd13-343">10 цифр, содержащих дефис:</span><span class="sxs-lookup"><span data-stu-id="0cd13-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="0cd13-344">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-344">Six digits</span></span> 
    
- <span data-ttu-id="0cd13-345">дефис;</span><span class="sxs-lookup"><span data-stu-id="0cd13-345">A hyphen</span></span>
    
-  <span data-ttu-id="0cd13-346">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0cd13-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="0cd13-347">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-347">Checksum</span></span>

<span data-ttu-id="0cd13-348">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-349">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-349">Definition</span></span>

<span data-ttu-id="0cd13-350">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-351">Регулярное выражение `Regex_finland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-352">Найдено ключевое `Keywords_finland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-353">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-353">Keywords</span></span>

<span data-ttu-id="0cd13-354">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-354"></span></span>
|<span data-ttu-id="0cd13-355">**Кэйвордс_финланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-356">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-356">dl#</span></span>  <br/> <span data-ttu-id="0cd13-357">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-357">driver license</span></span>  <br/> <span data-ttu-id="0cd13-358">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-358">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-359">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-359">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-360">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-360">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-361">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-362">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-363">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-364">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-364">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-365">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-365">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-366">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-366">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-367">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-367">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-368">ажокортти</span><span class="sxs-lookup"><span data-stu-id="0cd13-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="0cd13-369">Франция</span><span class="sxs-lookup"><span data-stu-id="0cd13-369">France</span></span>

<span data-ttu-id="0cd13-370">Дополнительные сведения см. в разделе "номер водительского удостоверения для Франции" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0cd13-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="0cd13-371">Германия</span><span class="sxs-lookup"><span data-stu-id="0cd13-371">Germany</span></span>

<span data-ttu-id="0cd13-372">Дополнительные сведения можно найти в разделе "номер водительского удостоверения для немецкого драйвера" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0cd13-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="0cd13-373">Греция</span><span class="sxs-lookup"><span data-stu-id="0cd13-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-374">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-374">Format</span></span>

<span data-ttu-id="0cd13-375">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-376">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-376">Pattern</span></span>

 <span data-ttu-id="0cd13-377">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0cd13-378">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-378">Checksum</span></span>

<span data-ttu-id="0cd13-379">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-380">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-380">Definition</span></span>

<span data-ttu-id="0cd13-381">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-382">Регулярное выражение `Regex_greece_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-383">Найдено ключевое `Keywords_greece_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-384">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-384">Keywords</span></span>

<span data-ttu-id="0cd13-385">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-385"></span></span>
|<span data-ttu-id="0cd13-386">**Кэйвордс_грице_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-387">Файл</span><span class="sxs-lookup"><span data-stu-id="0cd13-387">dlL#</span></span>  <br/> <span data-ttu-id="0cd13-388">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-388">driver license</span></span>  <br/> <span data-ttu-id="0cd13-389">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-389">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-390">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-390">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-391">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-391">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-392">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-393">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-394">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-395">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-395">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-396">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-396">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-397">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-397">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-398">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-398">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="0cd13-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="0cd13-400">Адеиа одигисис</span><span class="sxs-lookup"><span data-stu-id="0cd13-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="0cd13-401">Венгрия</span><span class="sxs-lookup"><span data-stu-id="0cd13-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-402">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-402">Format</span></span>

<span data-ttu-id="0cd13-403">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-404">Pattern</span></span>

<span data-ttu-id="0cd13-405">Две буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="0cd13-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="0cd13-406">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0cd13-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="0cd13-407">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-408">Checksum</span></span>

<span data-ttu-id="0cd13-409">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-410">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-410">Definition</span></span>

<span data-ttu-id="0cd13-411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-412">Регулярное выражение `Regex_hungary_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-413">Найдено ключевое `Keywords_hungary_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-414">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-414">Keywords</span></span>

<span data-ttu-id="0cd13-415">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-415"></span></span>
|<span data-ttu-id="0cd13-416">**Кэйвордс_хунгари_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-417">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-417">dl#</span></span>  <br/> <span data-ttu-id="0cd13-418">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-418">driver license</span></span>  <br/> <span data-ttu-id="0cd13-419">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-419">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-420">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-420">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-421">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-421">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-422">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-423">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-424">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-425">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-425">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-426">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-426">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-427">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-427">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-428">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-428">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-429">везетои енжедели</span><span class="sxs-lookup"><span data-stu-id="0cd13-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="0cd13-430">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="0cd13-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-431">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-431">Format</span></span>

<span data-ttu-id="0cd13-432">Шесть цифр, за которыми следуют четыре буквы</span><span class="sxs-lookup"><span data-stu-id="0cd13-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-433">Pattern</span></span>

<span data-ttu-id="0cd13-434">Шесть цифр и четыре буквы:</span><span class="sxs-lookup"><span data-stu-id="0cd13-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="0cd13-435">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-435">Six digits</span></span>
    
- <span data-ttu-id="0cd13-436">Четыре буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0cd13-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-437">Checksum</span></span>

<span data-ttu-id="0cd13-438">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-439">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-439">Definition</span></span>

<span data-ttu-id="0cd13-440">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-441">Регулярное выражение `Regex_ireland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-442">Найдено ключевое `Keywords_ireland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-443">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-443">Keywords</span></span>

<span data-ttu-id="0cd13-444">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-444"></span></span>
|<span data-ttu-id="0cd13-445">**Кэйвордс_иреланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-446">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-446">dl#</span></span>  <br/> <span data-ttu-id="0cd13-447">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-447">driver license</span></span>  <br/> <span data-ttu-id="0cd13-448">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-448">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-449">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-449">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-450">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-450">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-451">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-452">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-453">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-454">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-454">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-455">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-455">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-456">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-456">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-457">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-457">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-458">цеадúнас тиомáна</span><span class="sxs-lookup"><span data-stu-id="0cd13-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="0cd13-459">Италия</span><span class="sxs-lookup"><span data-stu-id="0cd13-459">Italy</span></span>

<span data-ttu-id="0cd13-460">Дополнительные сведения см. в разделе "номер водительского удостоверения для Италии" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0cd13-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="0cd13-461">Латвия</span><span class="sxs-lookup"><span data-stu-id="0cd13-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-462">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-462">Format</span></span>

<span data-ttu-id="0cd13-463">Три буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-464">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-464">Pattern</span></span>

<span data-ttu-id="0cd13-465">Три буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="0cd13-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="0cd13-466">Три буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0cd13-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="0cd13-467">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-468">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-468">Checksum</span></span>

<span data-ttu-id="0cd13-469">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-470">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-470">Definition</span></span>

<span data-ttu-id="0cd13-471">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-472">Регулярное выражение `Regex_latvia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-473">Найдено ключевое `Keywords_latvia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-474">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-474">Keywords</span></span>

<span data-ttu-id="0cd13-475">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-475"></span></span>
|<span data-ttu-id="0cd13-476">**Кэйвордс_латвиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-477">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-477">dl#</span></span>  <br/> <span data-ttu-id="0cd13-478">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-478">driver license</span></span>  <br/> <span data-ttu-id="0cd13-479">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-479">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-480">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-480">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-481">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-481">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-482">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-483">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-484">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-485">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-485">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-486">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-486">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-487">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-487">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-488">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-488">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-489">аутовадīтāжа аплиекīба</span><span class="sxs-lookup"><span data-stu-id="0cd13-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="0cd13-490">Литва</span><span class="sxs-lookup"><span data-stu-id="0cd13-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-491">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-491">Format</span></span>

<span data-ttu-id="0cd13-492">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-493">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-493">Pattern</span></span>

 <span data-ttu-id="0cd13-494">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0cd13-495">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-495">Checksum</span></span>

<span data-ttu-id="0cd13-496">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-497">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-497">Definition</span></span>

<span data-ttu-id="0cd13-498">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-499">Регулярное выражение `Regex_lithuania_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-500">Найдено ключевое `Keywords_lithuania_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-501">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-501">Keywords</span></span>

<span data-ttu-id="0cd13-502">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-502"></span></span>
|<span data-ttu-id="0cd13-503">**Кэйвордс_лисуаниа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-504">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-504">dl#</span></span>  <br/> <span data-ttu-id="0cd13-505">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-505">driver license</span></span>  <br/> <span data-ttu-id="0cd13-506">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-506">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-507">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-507">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-508">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-508">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-509">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-510">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-511">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-512">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-512">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-513">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-513">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-514">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-514">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-515">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-515">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-516">ваируотожо паžимėжимас</span><span class="sxs-lookup"><span data-stu-id="0cd13-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="0cd13-517">Луксембург</span><span class="sxs-lookup"><span data-stu-id="0cd13-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-518">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-518">Format</span></span>

<span data-ttu-id="0cd13-519">Шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-520">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-520">Pattern</span></span>

 <span data-ttu-id="0cd13-521">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0cd13-522">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-522">Checksum</span></span>

<span data-ttu-id="0cd13-523">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-524">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-524">Definition</span></span>

<span data-ttu-id="0cd13-525">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-526">Регулярное выражение `Regex_luxemburg_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-527">Найдено ключевое `Keywords_luxemburg_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-528">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-528">Keywords</span></span>

<span data-ttu-id="0cd13-529">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-529"></span></span>
|<span data-ttu-id="0cd13-530">**Кэйвордс_луксембург_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-531">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-531">dl#</span></span>  <br/> <span data-ttu-id="0cd13-532">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-532">driver license</span></span>  <br/> <span data-ttu-id="0cd13-533">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-533">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-534">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-534">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-535">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-535">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-536">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-537">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-538">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-539">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-539">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-540">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-540">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-541">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-541">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-542">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-542">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-543">фахрерлаубнис</span><span class="sxs-lookup"><span data-stu-id="0cd13-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="0cd13-544">Мальта</span><span class="sxs-lookup"><span data-stu-id="0cd13-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-545">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-545">Format</span></span>

<span data-ttu-id="0cd13-546">Сочетание двух символов и шести цифр в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="0cd13-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-547">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-547">Pattern</span></span>

<span data-ttu-id="0cd13-548">Сочетание двух символов и шести цифр:</span><span class="sxs-lookup"><span data-stu-id="0cd13-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="0cd13-549">Два символа (цифры или буквы без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0cd13-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="0cd13-550">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="0cd13-550">A space (optional)</span></span>
    
- <span data-ttu-id="0cd13-551">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0cd13-551">Three digits</span></span>
    
- <span data-ttu-id="0cd13-552">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="0cd13-552">A space (optional)</span></span>
    
- <span data-ttu-id="0cd13-553">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0cd13-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-554">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-554">Checksum</span></span>

<span data-ttu-id="0cd13-555">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-556">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-556">Definition</span></span>

<span data-ttu-id="0cd13-557">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-558">Регулярное выражение `Regex_malta_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-559">Найдено ключевое `Keywords_malta_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-560">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-560">Keywords</span></span>

<span data-ttu-id="0cd13-561">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-561"></span></span>
|<span data-ttu-id="0cd13-562">**Кэйвордс_малта_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-563">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-563">dl#</span></span>  <br/> <span data-ttu-id="0cd13-564">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-564">driver license</span></span>  <br/> <span data-ttu-id="0cd13-565">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-565">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-566">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-566">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-567">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-567">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-568">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-569">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-570">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-571">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-571">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-572">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-572">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-573">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-573">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-574">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-574">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-575">лиċензжаные зада Севкан</span><span class="sxs-lookup"><span data-stu-id="0cd13-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="0cd13-576">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="0cd13-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-577">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-577">Format</span></span>

<span data-ttu-id="0cd13-578">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-579">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-579">Pattern</span></span>

<span data-ttu-id="0cd13-580">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0cd13-581">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-581">Checksum</span></span>

<span data-ttu-id="0cd13-582">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-583">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-583">Definition</span></span>

<span data-ttu-id="0cd13-584">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-585">Регулярное выражение `Regex_netherlands_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-586">Найдено ключевое `Keywords_netherlands_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-587">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-587">Keywords</span></span>

<span data-ttu-id="0cd13-588">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-588"></span></span>
|<span data-ttu-id="0cd13-589">**Кэйвордс_несерландс_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-590">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-590">dl#</span></span>  <br/> <span data-ttu-id="0cd13-591">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-591">driver license</span></span>  <br/> <span data-ttu-id="0cd13-592">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-592">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-593">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-593">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-594">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-594">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-595">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-596">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-597">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-598">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-598">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-599">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-599">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-600">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-600">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-601">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-601">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="0cd13-602">permis de conduire</span></span>  <br/> <span data-ttu-id="0cd13-603">рижбевижс</span><span class="sxs-lookup"><span data-stu-id="0cd13-603">rijbewijs</span></span>  <br/> <span data-ttu-id="0cd13-604">рижбевижснуммер</span><span class="sxs-lookup"><span data-stu-id="0cd13-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="0cd13-605">Польша</span><span class="sxs-lookup"><span data-stu-id="0cd13-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-606">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-606">Format</span></span>

<span data-ttu-id="0cd13-607">14 цифр, содержащих 2 косых черты.</span><span class="sxs-lookup"><span data-stu-id="0cd13-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-608">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-608">Pattern</span></span>

<span data-ttu-id="0cd13-609">14 цифр и 2 косых черт:</span><span class="sxs-lookup"><span data-stu-id="0cd13-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="0cd13-610">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-610">Five digits</span></span> 
    
- <span data-ttu-id="0cd13-611">косая черта;</span><span class="sxs-lookup"><span data-stu-id="0cd13-611">A forward slash</span></span>
    
- <span data-ttu-id="0cd13-612">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0cd13-612">Two digits</span></span>
    
- <span data-ttu-id="0cd13-613">косая черта;</span><span class="sxs-lookup"><span data-stu-id="0cd13-613">A forward slash</span></span>
    
- <span data-ttu-id="0cd13-614">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-615">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-615">Checksum</span></span>

<span data-ttu-id="0cd13-616">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-617">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-617">Definition</span></span>

<span data-ttu-id="0cd13-618">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-619">Регулярное выражение `Regex_poland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-620">Найдено ключевое `Keywords_poland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-621">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-621">Keywords</span></span>

<span data-ttu-id="0cd13-622">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-622"></span></span>
|<span data-ttu-id="0cd13-623">**Кэйвордс_поланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-624">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-624">dl#</span></span>  <br/> <span data-ttu-id="0cd13-625">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-625">driver license</span></span>  <br/> <span data-ttu-id="0cd13-626">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-626">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-627">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-627">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-628">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-628">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-629">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-630">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-631">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-632">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-632">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-633">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-633">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-634">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-634">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-635">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-635">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-636">право жазди</span><span class="sxs-lookup"><span data-stu-id="0cd13-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="0cd13-637">Португалия</span><span class="sxs-lookup"><span data-stu-id="0cd13-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-638">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-638">Format</span></span>

<span data-ttu-id="0cd13-639">Две буквы, за которыми следуют семь чисел в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="0cd13-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-640">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-640">Pattern</span></span>

<span data-ttu-id="0cd13-641">Две буквы, за которыми следуют семь цифр со специальными символами:</span><span class="sxs-lookup"><span data-stu-id="0cd13-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="0cd13-642">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0cd13-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="0cd13-643">дефис;</span><span class="sxs-lookup"><span data-stu-id="0cd13-643">A hyphen</span></span>
    
- <span data-ttu-id="0cd13-644">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-644">Six digits</span></span>
    
- <span data-ttu-id="0cd13-645">Пробел</span><span class="sxs-lookup"><span data-stu-id="0cd13-645">A space</span></span>
    
- <span data-ttu-id="0cd13-646">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="0cd13-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-647">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-647">Checksum</span></span>

<span data-ttu-id="0cd13-648">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-649">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-649">Definition</span></span>

<span data-ttu-id="0cd13-650">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-651">Регулярное выражение `Regex_portugal_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-652">Найдено ключевое `Keywords_portugal_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-653">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-653">Keywords</span></span>

<span data-ttu-id="0cd13-654">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-654"></span></span>
|<span data-ttu-id="0cd13-655">**Кэйвордс_португал_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-656">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-656">dl#</span></span>  <br/> <span data-ttu-id="0cd13-657">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-657">driver license</span></span>  <br/> <span data-ttu-id="0cd13-658">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-658">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-659">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-659">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-660">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-660">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-661">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-662">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-663">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-664">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-664">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-665">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-665">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-666">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-666">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-667">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-667">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-668">картеира de моториста</span><span class="sxs-lookup"><span data-stu-id="0cd13-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="0cd13-669">Румыния</span><span class="sxs-lookup"><span data-stu-id="0cd13-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-670">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-670">Format</span></span>

<span data-ttu-id="0cd13-671">Один символ, за которым следуют восемь цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-672">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-672">Pattern</span></span>

<span data-ttu-id="0cd13-673">Один символ, за которым следуют восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="0cd13-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="0cd13-674">Одна буква (без учета регистра) или цифра</span><span class="sxs-lookup"><span data-stu-id="0cd13-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="0cd13-675">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-676">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-676">Checksum</span></span>

<span data-ttu-id="0cd13-677">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-678">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-678">Definition</span></span>

<span data-ttu-id="0cd13-679">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-680">Регулярное выражение `Regex_romania_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-681">Найдено ключевое `Keywords_romania_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-682">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-682">Keywords</span></span>

<span data-ttu-id="0cd13-683">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-683"></span></span>
|<span data-ttu-id="0cd13-684">**Кэйвордс_романиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-685">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-685">dl#</span></span>  <br/> <span data-ttu-id="0cd13-686">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-686">driver license</span></span>  <br/> <span data-ttu-id="0cd13-687">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-687">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-688">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-688">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-689">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-689">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-690">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-691">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-692">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-693">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-693">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-694">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-694">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-695">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-695">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-696">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-696">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-697">разрешение de кондуцере</span><span class="sxs-lookup"><span data-stu-id="0cd13-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="0cd13-698">Словакия</span><span class="sxs-lookup"><span data-stu-id="0cd13-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-699">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-699">Format</span></span>

<span data-ttu-id="0cd13-700">Один символ, за которым следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-701">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-701">Pattern</span></span>

<span data-ttu-id="0cd13-702">Один символ, за которым следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="0cd13-703">Одна буква (без учета регистра) или цифра</span><span class="sxs-lookup"><span data-stu-id="0cd13-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="0cd13-704">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="0cd13-705">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-705">Checksum</span></span>

<span data-ttu-id="0cd13-706">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-707">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-707">Definition</span></span>

<span data-ttu-id="0cd13-708">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-709">Регулярное выражение `Regex_slovakia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-710">Найдено ключевое `Keywords_slovakia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-711">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-711">Keywords</span></span>

<span data-ttu-id="0cd13-712">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-712"></span></span>
|<span data-ttu-id="0cd13-713">**Кэйвордс_словакиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-714">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-714">dl#</span></span>  <br/> <span data-ttu-id="0cd13-715">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-715">driver license</span></span>  <br/> <span data-ttu-id="0cd13-716">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-716">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-717">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-717">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-718">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-718">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-719">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-720">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-721">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-722">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-722">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-723">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-723">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-724">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-724">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-725">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-725">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-726">водиčскý преуказ</span><span class="sxs-lookup"><span data-stu-id="0cd13-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="0cd13-727">Словения</span><span class="sxs-lookup"><span data-stu-id="0cd13-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-728">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-728">Format</span></span>

<span data-ttu-id="0cd13-729">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="0cd13-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-730">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-730">Pattern</span></span>

<span data-ttu-id="0cd13-731">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0cd13-732">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-732">Checksum</span></span>

<span data-ttu-id="0cd13-733">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-734">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-734">Definition</span></span>

<span data-ttu-id="0cd13-735">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-736">Регулярное выражение `Regex_slovenia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-737">Найдено ключевое `Keywords_slovenia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-738">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-738">Keywords</span></span>

<span data-ttu-id="0cd13-739">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-739"></span></span>
|<span data-ttu-id="0cd13-740">**Кэйвордс_словениа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-741">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-741">dl#</span></span>  <br/> <span data-ttu-id="0cd13-742">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-742">driver license</span></span>  <br/> <span data-ttu-id="0cd13-743">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-743">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-744">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-744">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-745">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-745">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-746">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-747">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-748">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-749">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-749">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-750">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-750">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-751">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-751">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-752">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-752">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-753">возниšко доволженже</span><span class="sxs-lookup"><span data-stu-id="0cd13-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="0cd13-754">Испания</span><span class="sxs-lookup"><span data-stu-id="0cd13-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-755">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-755">Format</span></span>

<span data-ttu-id="0cd13-756">Восемь цифр, за которыми следует один символ</span><span class="sxs-lookup"><span data-stu-id="0cd13-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-757">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-757">Pattern</span></span>

<span data-ttu-id="0cd13-758">Восемь цифр, за которыми следует один символ:</span><span class="sxs-lookup"><span data-stu-id="0cd13-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="0cd13-759">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0cd13-759">Eight digits</span></span> 
    
- <span data-ttu-id="0cd13-760">Одна цифра или буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0cd13-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-761">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-761">Checksum</span></span>

<span data-ttu-id="0cd13-762">Да</span><span class="sxs-lookup"><span data-stu-id="0cd13-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-763">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-763">Definition</span></span>

<span data-ttu-id="0cd13-764">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-765">Функция `Func_spain_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-766">Найдено ключевое `Keywords_spain_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0cd13-767">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-767">Keywords</span></span>

<span data-ttu-id="0cd13-768">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-768"></span></span>
|<span data-ttu-id="0cd13-769">**Кэйвордс_спаин_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-770">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-770">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-771">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-771">dl#</span></span>  <br/> <span data-ttu-id="0cd13-772">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-772">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-773">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-773">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-774">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-774">driver license</span></span>  <br/> <span data-ttu-id="0cd13-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-775">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-776">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-777">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-777">driver's licence</span></span>  <br/> <span data-ttu-id="0cd13-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-778">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-779">driving licence
</span><span class="sxs-lookup"><span data-stu-id="0cd13-779">driving licence</span></span>  <br/> <span data-ttu-id="0cd13-780">Управление лицензией</span><span class="sxs-lookup"><span data-stu-id="0cd13-780">driving license</span></span>  <br/> <span data-ttu-id="0cd13-781">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-781">driver licence number</span></span>  <br/> <span data-ttu-id="0cd13-782">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-782">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-783">драйвер номер лицензии</span><span class="sxs-lookup"><span data-stu-id="0cd13-783">drivers licence number</span></span>  <br/> <span data-ttu-id="0cd13-784">номер лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="0cd13-784">drivers license number</span></span>  <br/> <span data-ttu-id="0cd13-785">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-785">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-786">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-786">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-787">номер водительской лицензии</span><span class="sxs-lookup"><span data-stu-id="0cd13-787">driving licence number</span></span>  <br/> <span data-ttu-id="0cd13-788">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-788">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-789">движущие разрешение</span><span class="sxs-lookup"><span data-stu-id="0cd13-789">driving permit</span></span>  <br/> <span data-ttu-id="0cd13-790">движущие число разрешений</span><span class="sxs-lookup"><span data-stu-id="0cd13-790">driving permit number</span></span>  <br/> <span data-ttu-id="0cd13-791">пермисо de кондукЦиóн</span><span class="sxs-lookup"><span data-stu-id="0cd13-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="0cd13-792">пермисо кондукЦиóн</span><span class="sxs-lookup"><span data-stu-id="0cd13-792">permiso conducción</span></span>  <br/> <span data-ttu-id="0cd13-793">нúмеро лиценЦиа кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="0cd13-794">нúмеро de карнет де кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="0cd13-795">нúмеро карнет кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="0cd13-796">лиценЦиа кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-796">licencia conducir</span></span>  <br/> <span data-ttu-id="0cd13-797">нúмеро de пермисо де кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="0cd13-798">нúмеро де пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="0cd13-799">нúмеро пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="0cd13-800">пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-800">permiso conducir</span></span>  <br/> <span data-ttu-id="0cd13-801">лиценЦиа de манежо</span><span class="sxs-lookup"><span data-stu-id="0cd13-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="0cd13-802">El карнет de кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="0cd13-803">Карнет кондуЦир</span><span class="sxs-lookup"><span data-stu-id="0cd13-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="0cd13-804">Швеция</span><span class="sxs-lookup"><span data-stu-id="0cd13-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="0cd13-805">Формат</span><span class="sxs-lookup"><span data-stu-id="0cd13-805">Format</span></span>

<span data-ttu-id="0cd13-806">Десять цифр, содержащие дефис</span><span class="sxs-lookup"><span data-stu-id="0cd13-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0cd13-807">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0cd13-807">Pattern</span></span>

<span data-ttu-id="0cd13-808">Десять цифр, содержащих дефис:</span><span class="sxs-lookup"><span data-stu-id="0cd13-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="0cd13-809">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0cd13-809">Six digits</span></span> 
    
- <span data-ttu-id="0cd13-810">дефис;</span><span class="sxs-lookup"><span data-stu-id="0cd13-810">A hyphen</span></span>
    
- <span data-ttu-id="0cd13-811">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0cd13-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0cd13-812">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0cd13-812">Checksum</span></span>

<span data-ttu-id="0cd13-813">Нет</span><span class="sxs-lookup"><span data-stu-id="0cd13-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="0cd13-814">Определение</span><span class="sxs-lookup"><span data-stu-id="0cd13-814">Definition</span></span>

<span data-ttu-id="0cd13-815">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0cd13-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0cd13-816">Регулярное выражение `Regex_sweden_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0cd13-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0cd13-817">Найдено ключевое `Keywords_sweden_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="0cd13-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="0cd13-818">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0cd13-818">Keywords</span></span>

<span data-ttu-id="0cd13-819">| |</span><span class="sxs-lookup"><span data-stu-id="0cd13-819"></span></span>
|<span data-ttu-id="0cd13-820">**Кэйвордс_сведен_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="0cd13-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="0cd13-821">dl#</span><span class="sxs-lookup"><span data-stu-id="0cd13-821">dl#</span></span>  <br/> <span data-ttu-id="0cd13-822">driver license</span><span class="sxs-lookup"><span data-stu-id="0cd13-822">driver license</span></span>  <br/> <span data-ttu-id="0cd13-823">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-823">driver license number</span></span>  <br/> <span data-ttu-id="0cd13-824">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-824">driver licence</span></span>  <br/> <span data-ttu-id="0cd13-825">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="0cd13-825">drivers lic.</span></span>  <br/> <span data-ttu-id="0cd13-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="0cd13-826">drivers license</span></span>  <br/> <span data-ttu-id="0cd13-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0cd13-827">drivers licence</span></span>  <br/> <span data-ttu-id="0cd13-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="0cd13-828">driver's license</span></span>  <br/> <span data-ttu-id="0cd13-829">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-829">driver's license number</span></span>  <br/> <span data-ttu-id="0cd13-830">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="0cd13-830">driver's licence number</span></span>  <br/> <span data-ttu-id="0cd13-831">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0cd13-831">driving license number</span></span>  <br/> <span data-ttu-id="0cd13-832">длно #</span><span class="sxs-lookup"><span data-stu-id="0cd13-832">dlno#</span></span>  <br/> <span data-ttu-id="0cd13-833">кöркорт</span><span class="sxs-lookup"><span data-stu-id="0cd13-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="0cd13-834">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="0cd13-834">UK</span></span>

<span data-ttu-id="0cd13-p103">Дополнительные сведения можно найти в разделе "номер водительского удостоверения для Великобритании" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0cd13-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0cd13-837">См. также</span><span class="sxs-lookup"><span data-stu-id="0cd13-837">See also</span></span>

[<span data-ttu-id="0cd13-838">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="0cd13-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

