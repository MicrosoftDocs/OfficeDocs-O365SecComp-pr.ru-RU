---
title: Номер водительского удостоверения ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных номер водительского ЕС. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534810"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="dbd95-104">Номер водительского удостоверения ЕС</span><span class="sxs-lookup"><span data-stu-id="dbd95-104">EU Driver's License Number</span></span>

<span data-ttu-id="dbd95-p102">В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных номер водительского ЕС. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="dbd95-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="dbd95-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="dbd95-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-108">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-108">Format</span></span>

<span data-ttu-id="dbd95-109">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-110">Pattern</span></span>

<span data-ttu-id="dbd95-111">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dbd95-112">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-112">Checksum</span></span>

<span data-ttu-id="dbd95-113">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-114">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-114">Definition</span></span>

<span data-ttu-id="dbd95-115">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-116">Регулярное выражение `Regex_austria_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-117">Ключевое слово из `Keywords_austria_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="dbd95-118">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-118">Keywords</span></span>

<span data-ttu-id="dbd95-119">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-119"></span></span>
|<span data-ttu-id="dbd95-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-121">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-121">dl#</span></span>  <br/> <span data-ttu-id="dbd95-122">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-122">driver license</span></span>  <br/> <span data-ttu-id="dbd95-123">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-123">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-124">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-124">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-125">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-125">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-126">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-127">Лицензия водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-127">driver's licence</span></span>  <br/> <span data-ttu-id="dbd95-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-128">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-129">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-129">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-130">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="dbd95-131">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-131">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-132">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="dbd95-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="dbd95-134">fuhrerschein republik osterreich</span><span class="sxs-lookup"><span data-stu-id="dbd95-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="dbd95-135">Бельгия</span><span class="sxs-lookup"><span data-stu-id="dbd95-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-136">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-136">Format</span></span>

<span data-ttu-id="dbd95-137">10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-138">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-138">Pattern</span></span>

<span data-ttu-id="dbd95-139">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dbd95-140">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-140">Checksum</span></span>

<span data-ttu-id="dbd95-141">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-142">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-142">Definition</span></span>

<span data-ttu-id="dbd95-143">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-144">Регулярное выражение `Regex_belgium_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-145">Ключевое слово из `Keywords_belgium_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="dbd95-146">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-146">Keywords</span></span>

<span data-ttu-id="dbd95-147">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-147"></span></span>
|<span data-ttu-id="dbd95-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-149">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-149">dl#</span></span>  <br/> <span data-ttu-id="dbd95-150">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-150">driver license</span></span>  <br/> <span data-ttu-id="dbd95-151">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-151">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-152">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-152">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-153">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-153">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-154">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-155">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-156">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-157">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-157">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-158">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-158">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-159">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="dbd95-160">rijbewijs</span></span>  <br/> <span data-ttu-id="dbd95-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="dbd95-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="dbd95-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="dbd95-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="dbd95-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="dbd95-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="dbd95-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="dbd95-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="dbd95-165">führerschein-nr</span><span class="sxs-lookup"><span data-stu-id="dbd95-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="dbd95-166">fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="dbd95-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="dbd95-167">fuehrerschein-nr</span><span class="sxs-lookup"><span data-stu-id="dbd95-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="dbd95-168">Болгария</span><span class="sxs-lookup"><span data-stu-id="dbd95-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-169">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-169">Format</span></span>

<span data-ttu-id="dbd95-170">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-171">Pattern</span></span>

<span data-ttu-id="dbd95-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dbd95-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-173">Checksum</span></span>

<span data-ttu-id="dbd95-174">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-175">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-175">Definition</span></span>

<span data-ttu-id="dbd95-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-177">Регулярное выражение `Regex_bulgaria_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-178">Ключевое слово из `Keywords_bulgaria_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="dbd95-179">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-179">Keywords</span></span>

<span data-ttu-id="dbd95-180">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-180"></span></span>
|<span data-ttu-id="dbd95-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-182">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-182">dl#</span></span>  <br/> <span data-ttu-id="dbd95-183">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-183">driver license</span></span>  <br/> <span data-ttu-id="dbd95-184">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-184">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-185">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-185">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-186">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-186">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-187">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-188">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-189">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-190">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-190">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-191">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-191">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-192">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-192">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-193">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-194">УПРАВЛЕНИЕ НА СВИДЕТЕЛСТВО ЗА МПС</span><span class="sxs-lookup"><span data-stu-id="dbd95-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="dbd95-195">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО</span><span class="sxs-lookup"><span data-stu-id="dbd95-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="dbd95-196">СУМПС</span><span class="sxs-lookup"><span data-stu-id="dbd95-196">сумпс</span></span>  <br/> <span data-ttu-id="dbd95-197">ШОФЬОРСКА КНИЖКА</span><span class="sxs-lookup"><span data-stu-id="dbd95-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="dbd95-198">Хорватия</span><span class="sxs-lookup"><span data-stu-id="dbd95-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-199">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-199">Format</span></span>

<span data-ttu-id="dbd95-200">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-201">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-201">Pattern</span></span>

<span data-ttu-id="dbd95-202">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dbd95-203">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-203">Checksum</span></span>

<span data-ttu-id="dbd95-204">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-205">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-205">Definition</span></span>

<span data-ttu-id="dbd95-206">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-207">Регулярное выражение `Regex_croatia_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-208">Ключевое слово из `Keywords_croatia_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="dbd95-209">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-209">Keywords</span></span>

<span data-ttu-id="dbd95-210">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-210"></span></span>
|<span data-ttu-id="dbd95-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-212">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-212">dl#</span></span>  <br/> <span data-ttu-id="dbd95-213">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-213">driver license</span></span>  <br/> <span data-ttu-id="dbd95-214">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-214">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-215">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-215">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-216">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-216">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-217">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-218">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-219">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-220">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-220">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-221">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-221">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-222">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-222">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-223">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="dbd95-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="dbd95-225">Кипр</span><span class="sxs-lookup"><span data-stu-id="dbd95-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-226">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-226">Format</span></span>

<span data-ttu-id="dbd95-227">12 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-228">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-228">Pattern</span></span>

<span data-ttu-id="dbd95-229">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dbd95-230">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-230">Checksum</span></span>

<span data-ttu-id="dbd95-231">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-232">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-232">Definition</span></span>

<span data-ttu-id="dbd95-233">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-234">Регулярное выражение `Regex_cyprus_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-235">Ключевое слово из `Keywords_cyprus_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-236">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-236">Keywords</span></span>

<span data-ttu-id="dbd95-237">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-237"></span></span>
|<span data-ttu-id="dbd95-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-239">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-239">dl#</span></span>  <br/> <span data-ttu-id="dbd95-240">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-240">driver license</span></span>  <br/> <span data-ttu-id="dbd95-241">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-241">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-242">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-242">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-243">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-243">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-244">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-245">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-246">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-246">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-247">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-247">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-248">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-248">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-249">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-250">ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="dbd95-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="dbd95-251">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="dbd95-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-252">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-252">Format</span></span>

<span data-ttu-id="dbd95-253">Две буквы, а затем шести цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-254">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-254">Pattern</span></span>

<span data-ttu-id="dbd95-255">8 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="dbd95-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="dbd95-256">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dbd95-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="dbd95-257">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="dbd95-257">A space (optional)</span></span>
    
- <span data-ttu-id="dbd95-258">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-259">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-259">Checksum</span></span>

<span data-ttu-id="dbd95-260">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-261">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-261">Definition</span></span>

<span data-ttu-id="dbd95-262">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-263">Регулярное выражение `Regex_czech_republic_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-264">Ключевое слово из `Keywords_czech_republic_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="dbd95-265">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-265">Keywords</span></span>

<span data-ttu-id="dbd95-266">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-266"></span></span>
|<span data-ttu-id="dbd95-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-268">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-268">dl#</span></span>  <br/> <span data-ttu-id="dbd95-269">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-269">driver license</span></span>  <br/> <span data-ttu-id="dbd95-270">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-270">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-271">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-271">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-272">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-272">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-273">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-274">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-275">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-276">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-276">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-277">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-277">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-278">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-278">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-279">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-279">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-280">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-281">Řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="dbd95-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="dbd95-282">Дания</span><span class="sxs-lookup"><span data-stu-id="dbd95-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-283">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-283">Format</span></span>

<span data-ttu-id="dbd95-284">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-285">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-285">Pattern</span></span>

<span data-ttu-id="dbd95-286">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dbd95-287">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-287">Checksum</span></span>

<span data-ttu-id="dbd95-288">Да</span><span class="sxs-lookup"><span data-stu-id="dbd95-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-289">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-289">Definition</span></span>

<span data-ttu-id="dbd95-290">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-291">Регулярное выражение `Regex_denmark_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-292">Ключевое слово из `Keywords_denmark_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="dbd95-293">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-293">Keywords</span></span>

<span data-ttu-id="dbd95-294">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-294"></span></span>
|<span data-ttu-id="dbd95-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-296">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-296">dl#</span></span>  <br/> <span data-ttu-id="dbd95-297">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-297">driver license</span></span>  <br/> <span data-ttu-id="dbd95-298">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-298">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-299">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-299">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-300">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-300">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-301">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-302">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-303">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-304">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-304">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-305">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-305">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-306">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-306">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-307">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="dbd95-308">kørekort</span></span>  <br/> <span data-ttu-id="dbd95-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="dbd95-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="dbd95-310">Эстония</span><span class="sxs-lookup"><span data-stu-id="dbd95-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-311">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-311">Format</span></span>

<span data-ttu-id="dbd95-312">Две буквы, а затем шести цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-313">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-313">Pattern</span></span>

<span data-ttu-id="dbd95-314">Две буквы и шести цифр:</span><span class="sxs-lookup"><span data-stu-id="dbd95-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="dbd95-315">Буквы «И» (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dbd95-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="dbd95-316">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-317">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-317">Checksum</span></span>

<span data-ttu-id="dbd95-318">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-319">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-319">Definition</span></span>

<span data-ttu-id="dbd95-320">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-321">Регулярное выражение `Regex_estonia_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-322">Ключевое слово из `Keywords_estonia_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-323">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-323">Keywords</span></span>

<span data-ttu-id="dbd95-324">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-324"></span></span>
|<span data-ttu-id="dbd95-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-326">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-326">dl#</span></span>  <br/> <span data-ttu-id="dbd95-327">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-327">driver license</span></span>  <br/> <span data-ttu-id="dbd95-328">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-328">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-329">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-329">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-330">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-330">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-331">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-331">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-332">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-333">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-334">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-335">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-335">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-336">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-336">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-337">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="dbd95-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="dbd95-339">Финляндия</span><span class="sxs-lookup"><span data-stu-id="dbd95-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-340">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-340">Format</span></span>

<span data-ttu-id="dbd95-341">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="dbd95-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-342">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-342">Pattern</span></span>

<span data-ttu-id="dbd95-343">10 цифр, содержащий дефис:</span><span class="sxs-lookup"><span data-stu-id="dbd95-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="dbd95-344">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-344">Six digits</span></span> 
    
- <span data-ttu-id="dbd95-345">дефис;</span><span class="sxs-lookup"><span data-stu-id="dbd95-345">A hyphen</span></span>
    
-  <span data-ttu-id="dbd95-346">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dbd95-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="dbd95-347">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-347">Checksum</span></span>

<span data-ttu-id="dbd95-348">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-349">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-349">Definition</span></span>

<span data-ttu-id="dbd95-350">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-351">Регулярное выражение `Regex_finland_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-352">Ключевое слово из `Keywords_finland_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-353">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-353">Keywords</span></span>

<span data-ttu-id="dbd95-354">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-354"></span></span>
|<span data-ttu-id="dbd95-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-356">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-356">dl#</span></span>  <br/> <span data-ttu-id="dbd95-357">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-357">driver license</span></span>  <br/> <span data-ttu-id="dbd95-358">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-358">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-359">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-359">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-360">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-360">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-361">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-362">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-363">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-364">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-364">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-365">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-365">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-366">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-366">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-367">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="dbd95-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="dbd95-369">Франция</span><span class="sxs-lookup"><span data-stu-id="dbd95-369">France</span></span>

<span data-ttu-id="dbd95-370">Для получения дополнительных сведений обратитесь к разделу «Номер водительского удостоверения Франция» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="dbd95-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="dbd95-371">Германия</span><span class="sxs-lookup"><span data-stu-id="dbd95-371">Germany</span></span>

<span data-ttu-id="dbd95-372">Для получения дополнительных сведений обратитесь к разделу «Немецкий номер водительского удостоверения» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="dbd95-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="dbd95-373">Греция</span><span class="sxs-lookup"><span data-stu-id="dbd95-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-374">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-374">Format</span></span>

<span data-ttu-id="dbd95-375">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-376">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-376">Pattern</span></span>

 <span data-ttu-id="dbd95-377">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="dbd95-378">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-378">Checksum</span></span>

<span data-ttu-id="dbd95-379">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-380">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-380">Definition</span></span>

<span data-ttu-id="dbd95-381">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-382">Регулярное выражение `Regex_greece_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-383">Ключевое слово из `Keywords_greece_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-384">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-384">Keywords</span></span>

<span data-ttu-id="dbd95-385">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-385"></span></span>
|<span data-ttu-id="dbd95-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-387">DLL-библиотека #</span><span class="sxs-lookup"><span data-stu-id="dbd95-387">dlL#</span></span>  <br/> <span data-ttu-id="dbd95-388">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-388">driver license</span></span>  <br/> <span data-ttu-id="dbd95-389">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-389">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-390">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-390">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-391">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-391">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-392">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-393">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-394">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-395">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-395">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-396">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-396">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-397">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-397">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-398">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-399">ΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="dbd95-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="dbd95-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="dbd95-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="dbd95-401">Венгрия</span><span class="sxs-lookup"><span data-stu-id="dbd95-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-402">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-402">Format</span></span>

<span data-ttu-id="dbd95-403">Две буквы, а затем шести цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-404">Pattern</span></span>

<span data-ttu-id="dbd95-405">Две буквы и шести цифр:</span><span class="sxs-lookup"><span data-stu-id="dbd95-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="dbd95-406">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dbd95-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="dbd95-407">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-408">Checksum</span></span>

<span data-ttu-id="dbd95-409">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-410">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-410">Definition</span></span>

<span data-ttu-id="dbd95-411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-412">Регулярное выражение `Regex_hungary_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-413">Ключевое слово из `Keywords_hungary_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-414">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-414">Keywords</span></span>

<span data-ttu-id="dbd95-415">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-415"></span></span>
|<span data-ttu-id="dbd95-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-417">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-417">dl#</span></span>  <br/> <span data-ttu-id="dbd95-418">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-418">driver license</span></span>  <br/> <span data-ttu-id="dbd95-419">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-419">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-420">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-420">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-421">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-421">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-422">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-423">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-424">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-425">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-425">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-426">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-426">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-427">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-427">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-428">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="dbd95-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="dbd95-430">Ireland</span><span class="sxs-lookup"><span data-stu-id="dbd95-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-431">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-431">Format</span></span>

<span data-ttu-id="dbd95-432">Шести цифр, а затем четырех букв</span><span class="sxs-lookup"><span data-stu-id="dbd95-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-433">Pattern</span></span>

<span data-ttu-id="dbd95-434">Шести цифр и четыре буквы:</span><span class="sxs-lookup"><span data-stu-id="dbd95-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="dbd95-435">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-435">Six digits</span></span>
    
- <span data-ttu-id="dbd95-436">Четыре буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dbd95-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-437">Checksum</span></span>

<span data-ttu-id="dbd95-438">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-439">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-439">Definition</span></span>

<span data-ttu-id="dbd95-440">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-441">Регулярное выражение `Regex_ireland_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-442">Ключевое слово из `Keywords_ireland_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-443">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-443">Keywords</span></span>

<span data-ttu-id="dbd95-444">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-444"></span></span>
|<span data-ttu-id="dbd95-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-446">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-446">dl#</span></span>  <br/> <span data-ttu-id="dbd95-447">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-447">driver license</span></span>  <br/> <span data-ttu-id="dbd95-448">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-448">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-449">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-449">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-450">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-450">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-451">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-452">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-453">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-454">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-454">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-455">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-455">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-456">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-456">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-457">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="dbd95-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="dbd95-459">Италия</span><span class="sxs-lookup"><span data-stu-id="dbd95-459">Italy</span></span>

<span data-ttu-id="dbd95-460">Для получения дополнительных сведений обратитесь к разделу «Номер водительского удостоверения Италия» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="dbd95-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="dbd95-461">Латвия</span><span class="sxs-lookup"><span data-stu-id="dbd95-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-462">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-462">Format</span></span>

<span data-ttu-id="dbd95-463">Три буквы, а затем шести цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-464">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-464">Pattern</span></span>

<span data-ttu-id="dbd95-465">Три буквы и шести цифр:</span><span class="sxs-lookup"><span data-stu-id="dbd95-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="dbd95-466">Три буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dbd95-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="dbd95-467">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-468">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-468">Checksum</span></span>

<span data-ttu-id="dbd95-469">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-470">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-470">Definition</span></span>

<span data-ttu-id="dbd95-471">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-472">Регулярное выражение `Regex_latvia_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-473">Ключевое слово из `Keywords_latvia_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-474">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-474">Keywords</span></span>

<span data-ttu-id="dbd95-475">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-475"></span></span>
|<span data-ttu-id="dbd95-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-477">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-477">dl#</span></span>  <br/> <span data-ttu-id="dbd95-478">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-478">driver license</span></span>  <br/> <span data-ttu-id="dbd95-479">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-479">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-480">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-480">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-481">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-481">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-482">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-483">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-484">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-485">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-485">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-486">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-486">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-487">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-487">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-488">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="dbd95-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="dbd95-490">Литва</span><span class="sxs-lookup"><span data-stu-id="dbd95-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-491">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-491">Format</span></span>

<span data-ttu-id="dbd95-492">Восьми знаков без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-493">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-493">Pattern</span></span>

 <span data-ttu-id="dbd95-494">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="dbd95-495">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-495">Checksum</span></span>

<span data-ttu-id="dbd95-496">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-497">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-497">Definition</span></span>

<span data-ttu-id="dbd95-498">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-499">Регулярное выражение `Regex_lithuania_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-500">Ключевое слово из `Keywords_lithuania_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-501">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-501">Keywords</span></span>

<span data-ttu-id="dbd95-502">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-502"></span></span>
|<span data-ttu-id="dbd95-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-504">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-504">dl#</span></span>  <br/> <span data-ttu-id="dbd95-505">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-505">driver license</span></span>  <br/> <span data-ttu-id="dbd95-506">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-506">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-507">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-507">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-508">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-508">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-509">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-510">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-511">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-512">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-512">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-513">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-513">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-514">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-514">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-515">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-516">vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="dbd95-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="dbd95-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="dbd95-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-518">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-518">Format</span></span>

<span data-ttu-id="dbd95-519">Шести цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-520">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-520">Pattern</span></span>

 <span data-ttu-id="dbd95-521">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="dbd95-522">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-522">Checksum</span></span>

<span data-ttu-id="dbd95-523">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-524">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-524">Definition</span></span>

<span data-ttu-id="dbd95-525">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-526">Регулярное выражение `Regex_luxemburg_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-527">Ключевое слово из `Keywords_luxemburg_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-528">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-528">Keywords</span></span>

<span data-ttu-id="dbd95-529">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-529"></span></span>
|<span data-ttu-id="dbd95-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-531">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-531">dl#</span></span>  <br/> <span data-ttu-id="dbd95-532">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-532">driver license</span></span>  <br/> <span data-ttu-id="dbd95-533">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-533">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-534">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-534">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-535">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-535">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-536">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-537">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-538">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-539">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-539">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-540">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-540">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-541">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-541">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-542">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="dbd95-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="dbd95-544">Мальта</span><span class="sxs-lookup"><span data-stu-id="dbd95-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-545">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-545">Format</span></span>

<span data-ttu-id="dbd95-546">Сочетание двух символов и шести цифр в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="dbd95-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-547">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-547">Pattern</span></span>

<span data-ttu-id="dbd95-548">Сочетание двух символов и шести цифр:</span><span class="sxs-lookup"><span data-stu-id="dbd95-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="dbd95-549">Два знаков (цифр или символов, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dbd95-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="dbd95-550">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="dbd95-550">A space (optional)</span></span>
    
- <span data-ttu-id="dbd95-551">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dbd95-551">Three digits</span></span>
    
- <span data-ttu-id="dbd95-552">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="dbd95-552">A space (optional)</span></span>
    
- <span data-ttu-id="dbd95-553">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dbd95-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-554">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-554">Checksum</span></span>

<span data-ttu-id="dbd95-555">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-556">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-556">Definition</span></span>

<span data-ttu-id="dbd95-557">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-558">Регулярное выражение `Regex_malta_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-559">Ключевое слово из `Keywords_malta_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-560">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-560">Keywords</span></span>

<span data-ttu-id="dbd95-561">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-561"></span></span>
|<span data-ttu-id="dbd95-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-563">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-563">dl#</span></span>  <br/> <span data-ttu-id="dbd95-564">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-564">driver license</span></span>  <br/> <span data-ttu-id="dbd95-565">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-565">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-566">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-566">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-567">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-567">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-568">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-569">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-570">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-571">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-571">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-572">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-572">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-573">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-573">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-574">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-575">liċenzja задач sewqan</span><span class="sxs-lookup"><span data-stu-id="dbd95-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="dbd95-576">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="dbd95-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-577">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-577">Format</span></span>

<span data-ttu-id="dbd95-578">10 цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-579">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-579">Pattern</span></span>

<span data-ttu-id="dbd95-580">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dbd95-581">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-581">Checksum</span></span>

<span data-ttu-id="dbd95-582">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-583">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-583">Definition</span></span>

<span data-ttu-id="dbd95-584">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-585">Регулярное выражение `Regex_netherlands_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-586">Ключевое слово из `Keywords_netherlands_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-587">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-587">Keywords</span></span>

<span data-ttu-id="dbd95-588">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-588"></span></span>
|<span data-ttu-id="dbd95-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-590">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-590">dl#</span></span>  <br/> <span data-ttu-id="dbd95-591">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-591">driver license</span></span>  <br/> <span data-ttu-id="dbd95-592">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-592">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-593">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-593">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-594">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-594">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-595">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-596">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-597">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-598">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-598">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-599">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-599">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-600">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-600">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-601">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="dbd95-602">permis de conduire</span></span>  <br/> <span data-ttu-id="dbd95-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="dbd95-603">rijbewijs</span></span>  <br/> <span data-ttu-id="dbd95-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="dbd95-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="dbd95-605">Польша</span><span class="sxs-lookup"><span data-stu-id="dbd95-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-606">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-606">Format</span></span>

<span data-ttu-id="dbd95-607">14 цифр, содержащий 2 косая черта</span><span class="sxs-lookup"><span data-stu-id="dbd95-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-608">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-608">Pattern</span></span>

<span data-ttu-id="dbd95-609">14 цифр и косая черта 2:</span><span class="sxs-lookup"><span data-stu-id="dbd95-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="dbd95-610">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-610">Five digits</span></span> 
    
- <span data-ttu-id="dbd95-611">косая черта;</span><span class="sxs-lookup"><span data-stu-id="dbd95-611">A forward slash</span></span>
    
- <span data-ttu-id="dbd95-612">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dbd95-612">Two digits</span></span>
    
- <span data-ttu-id="dbd95-613">косая черта;</span><span class="sxs-lookup"><span data-stu-id="dbd95-613">A forward slash</span></span>
    
- <span data-ttu-id="dbd95-614">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-615">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-615">Checksum</span></span>

<span data-ttu-id="dbd95-616">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-617">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-617">Definition</span></span>

<span data-ttu-id="dbd95-618">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-619">Регулярное выражение `Regex_poland_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-620">Ключевое слово из `Keywords_poland_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-621">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-621">Keywords</span></span>

<span data-ttu-id="dbd95-622">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-622"></span></span>
|<span data-ttu-id="dbd95-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-624">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-624">dl#</span></span>  <br/> <span data-ttu-id="dbd95-625">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-625">driver license</span></span>  <br/> <span data-ttu-id="dbd95-626">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-626">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-627">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-627">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-628">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-628">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-629">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-630">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-631">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-632">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-632">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-633">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-633">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-634">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-634">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-635">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-636">prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="dbd95-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="dbd95-637">Португалия</span><span class="sxs-lookup"><span data-stu-id="dbd95-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-638">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-638">Format</span></span>

<span data-ttu-id="dbd95-639">Две буквы, затем семь номеров в указанному шаблону</span><span class="sxs-lookup"><span data-stu-id="dbd95-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-640">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-640">Pattern</span></span>

<span data-ttu-id="dbd95-641">Две буквы, затем семь номеров с помощью специальных символов:</span><span class="sxs-lookup"><span data-stu-id="dbd95-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="dbd95-642">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dbd95-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="dbd95-643">дефис;</span><span class="sxs-lookup"><span data-stu-id="dbd95-643">A hyphen</span></span>
    
- <span data-ttu-id="dbd95-644">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-644">Six digits</span></span>
    
- <span data-ttu-id="dbd95-645">Пробел</span><span class="sxs-lookup"><span data-stu-id="dbd95-645">A space</span></span>
    
- <span data-ttu-id="dbd95-646">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="dbd95-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-647">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-647">Checksum</span></span>

<span data-ttu-id="dbd95-648">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-649">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-649">Definition</span></span>

<span data-ttu-id="dbd95-650">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-651">Регулярное выражение `Regex_portugal_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-652">Ключевое слово из `Keywords_portugal_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-653">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-653">Keywords</span></span>

<span data-ttu-id="dbd95-654">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-654"></span></span>
|<span data-ttu-id="dbd95-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-656">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-656">dl#</span></span>  <br/> <span data-ttu-id="dbd95-657">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-657">driver license</span></span>  <br/> <span data-ttu-id="dbd95-658">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-658">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-659">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-659">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-660">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-660">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-661">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-662">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-663">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-664">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-664">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-665">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-665">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-666">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-666">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-667">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-668">motorista де carteira</span><span class="sxs-lookup"><span data-stu-id="dbd95-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="dbd95-669">Румыния</span><span class="sxs-lookup"><span data-stu-id="dbd95-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-670">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-670">Format</span></span>

<span data-ttu-id="dbd95-671">Один символ, а затем восьми знаков</span><span class="sxs-lookup"><span data-stu-id="dbd95-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-672">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-672">Pattern</span></span>

<span data-ttu-id="dbd95-673">Один символ, а затем восьми знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="dbd95-674">Один (без учета регистра) букв или цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="dbd95-675">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-676">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-676">Checksum</span></span>

<span data-ttu-id="dbd95-677">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-678">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-678">Definition</span></span>

<span data-ttu-id="dbd95-679">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-680">Регулярное выражение `Regex_romania_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-681">Ключевое слово из `Keywords_romania_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-682">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-682">Keywords</span></span>

<span data-ttu-id="dbd95-683">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-683"></span></span>
|<span data-ttu-id="dbd95-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-685">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-685">dl#</span></span>  <br/> <span data-ttu-id="dbd95-686">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-686">driver license</span></span>  <br/> <span data-ttu-id="dbd95-687">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-687">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-688">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-688">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-689">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-689">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-690">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-691">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-692">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-693">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-693">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-694">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-694">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-695">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-695">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-696">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-697">conducere де permis</span><span class="sxs-lookup"><span data-stu-id="dbd95-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="dbd95-698">Словакия</span><span class="sxs-lookup"><span data-stu-id="dbd95-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-699">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-699">Format</span></span>

<span data-ttu-id="dbd95-700">Один символ, а затем семь цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-701">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-701">Pattern</span></span>

<span data-ttu-id="dbd95-702">Один символ, а затем семь цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="dbd95-703">Один (без учета регистра) букв или цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="dbd95-704">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="dbd95-705">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-705">Checksum</span></span>

<span data-ttu-id="dbd95-706">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-707">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-707">Definition</span></span>

<span data-ttu-id="dbd95-708">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-709">Регулярное выражение `Regex_slovakia_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-710">Ключевое слово из `Keywords_slovakia_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-711">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-711">Keywords</span></span>

<span data-ttu-id="dbd95-712">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-712"></span></span>
|<span data-ttu-id="dbd95-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-714">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-714">dl#</span></span>  <br/> <span data-ttu-id="dbd95-715">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-715">driver license</span></span>  <br/> <span data-ttu-id="dbd95-716">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-716">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-717">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-717">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-718">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-718">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-719">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-720">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-721">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-722">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-722">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-723">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-723">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-724">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-724">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-725">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="dbd95-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="dbd95-727">Словения</span><span class="sxs-lookup"><span data-stu-id="dbd95-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-728">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-728">Format</span></span>

<span data-ttu-id="dbd95-729">Девяти цифр без пробелов и разделители</span><span class="sxs-lookup"><span data-stu-id="dbd95-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-730">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-730">Pattern</span></span>

<span data-ttu-id="dbd95-731">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="dbd95-732">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-732">Checksum</span></span>

<span data-ttu-id="dbd95-733">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-734">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-734">Definition</span></span>

<span data-ttu-id="dbd95-735">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-736">Регулярное выражение `Regex_slovenia_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-737">Ключевое слово из `Keywords_slovenia_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-738">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-738">Keywords</span></span>

<span data-ttu-id="dbd95-739">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-739"></span></span>
|<span data-ttu-id="dbd95-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-741">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-741">dl#</span></span>  <br/> <span data-ttu-id="dbd95-742">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-742">driver license</span></span>  <br/> <span data-ttu-id="dbd95-743">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-743">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-744">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-744">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-745">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-745">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-746">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-747">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-748">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-749">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-749">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-750">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-750">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-751">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-751">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-752">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="dbd95-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="dbd95-754">Испания</span><span class="sxs-lookup"><span data-stu-id="dbd95-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-755">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-755">Format</span></span>

<span data-ttu-id="dbd95-756">Восемь цифр, за которой следует один символ</span><span class="sxs-lookup"><span data-stu-id="dbd95-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-757">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-757">Pattern</span></span>

<span data-ttu-id="dbd95-758">Восемь цифр, за которой следует один символ:</span><span class="sxs-lookup"><span data-stu-id="dbd95-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="dbd95-759">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dbd95-759">Eight digits</span></span> 
    
- <span data-ttu-id="dbd95-760">Одну цифру или букву (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dbd95-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-761">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-761">Checksum</span></span>

<span data-ttu-id="dbd95-762">Да</span><span class="sxs-lookup"><span data-stu-id="dbd95-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-763">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-763">Definition</span></span>

<span data-ttu-id="dbd95-764">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-765">Функция `Func_spain_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-766">Ключевое слово из `Keywords_spain_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dbd95-767">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-767">Keywords</span></span>

<span data-ttu-id="dbd95-768">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-768"></span></span>
|<span data-ttu-id="dbd95-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-770">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-771">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-771">dl#</span></span>  <br/> <span data-ttu-id="dbd95-772">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-772">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-773">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-773">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-774">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-774">driver license</span></span>  <br/> <span data-ttu-id="dbd95-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-775">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-776">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-777">Лицензия водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-777">driver's licence</span></span>  <br/> <span data-ttu-id="dbd95-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-778">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-779">driving licence
</span><span class="sxs-lookup"><span data-stu-id="dbd95-779">driving licence</span></span>  <br/> <span data-ttu-id="dbd95-780">управляющий лицензии</span><span class="sxs-lookup"><span data-stu-id="dbd95-780">driving license</span></span>  <br/> <span data-ttu-id="dbd95-781">Номер лицензии драйвера</span><span class="sxs-lookup"><span data-stu-id="dbd95-781">driver licence number</span></span>  <br/> <span data-ttu-id="dbd95-782">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-782">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-783">драйверы лицензия номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-783">drivers licence number</span></span>  <br/> <span data-ttu-id="dbd95-784">Номер драйверы</span><span class="sxs-lookup"><span data-stu-id="dbd95-784">drivers license number</span></span>  <br/> <span data-ttu-id="dbd95-785">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-785">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-786">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-786">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-787">средство повышения лицензия номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-787">driving licence number</span></span>  <br/> <span data-ttu-id="dbd95-788">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-788">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-789">управляющий разрешения</span><span class="sxs-lookup"><span data-stu-id="dbd95-789">driving permit</span></span>  <br/> <span data-ttu-id="dbd95-790">управляющий номер разрешения</span><span class="sxs-lookup"><span data-stu-id="dbd95-790">driving permit number</span></span>  <br/> <span data-ttu-id="dbd95-791">conducción де permiso</span><span class="sxs-lookup"><span data-stu-id="dbd95-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="dbd95-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="dbd95-792">permiso conducción</span></span>  <br/> <span data-ttu-id="dbd95-793">número licencia conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="dbd95-794">número de carnet де conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="dbd95-795">número carnet conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="dbd95-796">licencia conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-796">licencia conducir</span></span>  <br/> <span data-ttu-id="dbd95-797">número de permiso де conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="dbd95-798">conducir permiso де número</span><span class="sxs-lookup"><span data-stu-id="dbd95-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="dbd95-799">número permiso conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="dbd95-800">permiso conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-800">permiso conducir</span></span>  <br/> <span data-ttu-id="dbd95-801">manejo де licencia</span><span class="sxs-lookup"><span data-stu-id="dbd95-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="dbd95-802">EL carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="dbd95-803">carnet conducir</span><span class="sxs-lookup"><span data-stu-id="dbd95-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="dbd95-804">Швеция</span><span class="sxs-lookup"><span data-stu-id="dbd95-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="dbd95-805">Формат</span><span class="sxs-lookup"><span data-stu-id="dbd95-805">Format</span></span>

<span data-ttu-id="dbd95-806">10 цифр, содержащий дефис</span><span class="sxs-lookup"><span data-stu-id="dbd95-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="dbd95-807">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dbd95-807">Pattern</span></span>

<span data-ttu-id="dbd95-808">10 цифр, содержащий дефис:</span><span class="sxs-lookup"><span data-stu-id="dbd95-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="dbd95-809">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dbd95-809">Six digits</span></span> 
    
- <span data-ttu-id="dbd95-810">дефис;</span><span class="sxs-lookup"><span data-stu-id="dbd95-810">A hyphen</span></span>
    
- <span data-ttu-id="dbd95-811">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dbd95-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="dbd95-812">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dbd95-812">Checksum</span></span>

<span data-ttu-id="dbd95-813">Нет</span><span class="sxs-lookup"><span data-stu-id="dbd95-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="dbd95-814">Определение</span><span class="sxs-lookup"><span data-stu-id="dbd95-814">Definition</span></span>

<span data-ttu-id="dbd95-815">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dbd95-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="dbd95-816">Регулярное выражение `Regex_sweden_eu_driver's_license_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dbd95-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="dbd95-817">Ключевое слово из `Keywords_sweden_eu_driver's_license_number` найден.</span><span class="sxs-lookup"><span data-stu-id="dbd95-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="dbd95-818">Keywords</span><span class="sxs-lookup"><span data-stu-id="dbd95-818">Keywords</span></span>

<span data-ttu-id="dbd95-819">| |</span><span class="sxs-lookup"><span data-stu-id="dbd95-819"></span></span>
|<span data-ttu-id="dbd95-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="dbd95-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="dbd95-821">dl#</span><span class="sxs-lookup"><span data-stu-id="dbd95-821">dl#</span></span>  <br/> <span data-ttu-id="dbd95-822">driver license</span><span class="sxs-lookup"><span data-stu-id="dbd95-822">driver license</span></span>  <br/> <span data-ttu-id="dbd95-823">драйвер номер</span><span class="sxs-lookup"><span data-stu-id="dbd95-823">driver license number</span></span>  <br/> <span data-ttu-id="dbd95-824">драйвер лицензия</span><span class="sxs-lookup"><span data-stu-id="dbd95-824">driver licence</span></span>  <br/> <span data-ttu-id="dbd95-825">драйверы lic.</span><span class="sxs-lookup"><span data-stu-id="dbd95-825">drivers lic.</span></span>  <br/> <span data-ttu-id="dbd95-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="dbd95-826">drivers license</span></span>  <br/> <span data-ttu-id="dbd95-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dbd95-827">drivers licence</span></span>  <br/> <span data-ttu-id="dbd95-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="dbd95-828">driver's license</span></span>  <br/> <span data-ttu-id="dbd95-829">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-829">driver's license number</span></span>  <br/> <span data-ttu-id="dbd95-830">номер водительского удостоверения для лицензирования</span><span class="sxs-lookup"><span data-stu-id="dbd95-830">driver's licence number</span></span>  <br/> <span data-ttu-id="dbd95-831">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dbd95-831">driving license number</span></span>  <br/> <span data-ttu-id="dbd95-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="dbd95-832">dlno#</span></span>  <br/> <span data-ttu-id="dbd95-833">körkort</span><span class="sxs-lookup"><span data-stu-id="dbd95-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="dbd95-834">(ВЕЛИКОБРИТАНИЯ)</span><span class="sxs-lookup"><span data-stu-id="dbd95-834">UK</span></span>

<span data-ttu-id="dbd95-p103">Для получения дополнительных сведений обратитесь к разделу «Номер водительского удостоверения Великобритания» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="dbd95-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dbd95-837">См. также</span><span class="sxs-lookup"><span data-stu-id="dbd95-837">See also</span></span>

[<span data-ttu-id="dbd95-838">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="dbd95-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

