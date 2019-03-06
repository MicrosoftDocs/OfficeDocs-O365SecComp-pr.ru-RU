---
title: Номер водительского удостоверения для драйвера ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации номера лицензии для драйвера ЕС. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: be9497c325866a670dff8d82b5170f4ca947c4ad
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410754"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="6fb6d-104">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="6fb6d-104">EU Driver's License Number</span></span>

<span data-ttu-id="6fb6d-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации номера лицензии для драйвера ЕС.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="6fb6d-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="6fb6d-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-108">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-108">Format</span></span>

<span data-ttu-id="6fb6d-109">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-110">Pattern</span></span>

<span data-ttu-id="6fb6d-111">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-112">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-112">Checksum</span></span>

<span data-ttu-id="6fb6d-113">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-114">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-114">Definition</span></span>

<span data-ttu-id="6fb6d-115">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-116">Регулярное выражение `Regex_austria_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-117">Найдено ключевое `Keywords_austria_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="6fb6d-118">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-118">Keywords</span></span>

<span data-ttu-id="6fb6d-119">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-119"></span></span>
|<span data-ttu-id="6fb6d-120">**Кэйвордс_аустриа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-121">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-121">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-122">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-122">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-123">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-123">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-124">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-124">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-125">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-125">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-126">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-127">driver's licence</span></span>  <br/> <span data-ttu-id="6fb6d-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-128">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-129">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-129">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-130">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="6fb6d-131">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-131">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-132">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-132">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-133">фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="6fb6d-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="6fb6d-134">фухрерсчеин Републик остерреич</span><span class="sxs-lookup"><span data-stu-id="6fb6d-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="6fb6d-135">Бельгия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-136">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-136">Format</span></span>

<span data-ttu-id="6fb6d-137">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-138">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-138">Pattern</span></span>

<span data-ttu-id="6fb6d-139">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-140">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-140">Checksum</span></span>

<span data-ttu-id="6fb6d-141">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-142">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-142">Definition</span></span>

<span data-ttu-id="6fb6d-143">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-144">Регулярное выражение `Regex_belgium_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-145">Найдено ключевое `Keywords_belgium_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6fb6d-146">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-146">Keywords</span></span>

<span data-ttu-id="6fb6d-147">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-147"></span></span>
|<span data-ttu-id="6fb6d-148">**Кэйвордс__белгиум_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-149">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-149">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-150">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-150">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-151">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-151">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-152">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-152">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-153">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-153">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-154">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-155">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-156">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-157">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-157">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-158">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-158">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-159">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-159">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-160">рижбевижс</span><span class="sxs-lookup"><span data-stu-id="6fb6d-160">rijbewijs</span></span>  <br/> <span data-ttu-id="6fb6d-161">рижбевижснуммер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="6fb6d-162">фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="6fb6d-163">фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="6fb6d-164">фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="6fb6d-165">фüхрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="6fb6d-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="6fb6d-166">фуехрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="6fb6d-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="6fb6d-167">фуехрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="6fb6d-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="6fb6d-168">Болгария</span><span class="sxs-lookup"><span data-stu-id="6fb6d-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-169">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-169">Format</span></span>

<span data-ttu-id="6fb6d-170">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-171">Pattern</span></span>

<span data-ttu-id="6fb6d-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-173">Checksum</span></span>

<span data-ttu-id="6fb6d-174">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-175">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-175">Definition</span></span>

<span data-ttu-id="6fb6d-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-177">Регулярное выражение `Regex_bulgaria_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-178">Найдено ключевое `Keywords_bulgaria_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="6fb6d-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-179">Keywords</span></span>

<span data-ttu-id="6fb6d-180">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-180"></span></span>
|<span data-ttu-id="6fb6d-181">**Кэйвордс_булгариа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-182">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-182">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-183">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-183">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-184">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-184">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-185">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-185">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-186">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-186">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-187">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-188">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-189">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-190">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-190">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-191">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-191">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-192">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-192">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-193">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-193">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-194">свидетелство за управление на МПС</span><span class="sxs-lookup"><span data-stu-id="6fb6d-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="6fb6d-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="6fb6d-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="6fb6d-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="6fb6d-196">сумпс</span></span>  <br/> <span data-ttu-id="6fb6d-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="6fb6d-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="6fb6d-198">Хорватия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-199">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-199">Format</span></span>

<span data-ttu-id="6fb6d-200">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-201">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-201">Pattern</span></span>

<span data-ttu-id="6fb6d-202">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-203">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-203">Checksum</span></span>

<span data-ttu-id="6fb6d-204">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-205">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-205">Definition</span></span>

<span data-ttu-id="6fb6d-206">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-207">Регулярное выражение `Regex_croatia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-208">Найдено ключевое `Keywords_croatia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6fb6d-209">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-209">Keywords</span></span>

<span data-ttu-id="6fb6d-210">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-210"></span></span>
|<span data-ttu-id="6fb6d-211">**Кэйвордс_кроатиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-212">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-212">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-213">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-213">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-214">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-214">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-215">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-215">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-216">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-216">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-217">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-218">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-219">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-220">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-220">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-221">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-221">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-222">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-222">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-223">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-223">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-224">возаčка дозвола</span><span class="sxs-lookup"><span data-stu-id="6fb6d-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="6fb6d-225">Кипр</span><span class="sxs-lookup"><span data-stu-id="6fb6d-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-226">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-226">Format</span></span>

<span data-ttu-id="6fb6d-227">12 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-228">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-228">Pattern</span></span>

<span data-ttu-id="6fb6d-229">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-230">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-230">Checksum</span></span>

<span data-ttu-id="6fb6d-231">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-232">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-232">Definition</span></span>

<span data-ttu-id="6fb6d-233">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-234">Регулярное выражение `Regex_cyprus_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-235">Найдено ключевое `Keywords_cyprus_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-236">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-236">Keywords</span></span>

<span data-ttu-id="6fb6d-237">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-237"></span></span>
|<span data-ttu-id="6fb6d-238">**Кэйвордс_ципрус_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-239">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-239">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-240">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-240">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-241">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-241">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-242">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-242">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-243">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-243">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-244">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-245">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-246">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-246">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-247">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-247">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-248">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-248">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-249">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-249">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="6fb6d-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="6fb6d-251">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="6fb6d-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-252">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-252">Format</span></span>

<span data-ttu-id="6fb6d-253">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-254">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-254">Pattern</span></span>

<span data-ttu-id="6fb6d-255">Восемь букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="6fb6d-256">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="6fb6d-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="6fb6d-257">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="6fb6d-257">A space (optional)</span></span>
    
- <span data-ttu-id="6fb6d-258">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-259">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-259">Checksum</span></span>

<span data-ttu-id="6fb6d-260">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-261">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-261">Definition</span></span>

<span data-ttu-id="6fb6d-262">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-263">Регулярное выражение `Regex_czech_republic_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-264">Найдено ключевое `Keywords_czech_republic_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6fb6d-265">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-265">Keywords</span></span>

<span data-ttu-id="6fb6d-266">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-266"></span></span>
|<span data-ttu-id="6fb6d-267">**Кэйвордс_кзеч_републик_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-268">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-268">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-269">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-269">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-270">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-270">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-271">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-271">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-272">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-272">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-273">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-274">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-275">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-276">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-276">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-277">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-277">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-278">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-278">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-279">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-279">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-280">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-280">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-281">řидиčскý прúказ</span><span class="sxs-lookup"><span data-stu-id="6fb6d-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="6fb6d-282">Дания</span><span class="sxs-lookup"><span data-stu-id="6fb6d-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-283">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-283">Format</span></span>

<span data-ttu-id="6fb6d-284">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-285">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-285">Pattern</span></span>

<span data-ttu-id="6fb6d-286">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-287">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-287">Checksum</span></span>

<span data-ttu-id="6fb6d-288">Да</span><span class="sxs-lookup"><span data-stu-id="6fb6d-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-289">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-289">Definition</span></span>

<span data-ttu-id="6fb6d-290">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-291">Регулярное выражение `Regex_denmark_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-292">Найдено ключевое `Keywords_denmark_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="6fb6d-293">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-293">Keywords</span></span>

<span data-ttu-id="6fb6d-294">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-294"></span></span>
|<span data-ttu-id="6fb6d-295">**Кэйвордс_денмарк_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-296">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-296">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-297">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-297">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-298">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-298">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-299">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-299">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-300">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-300">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-301">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-302">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-303">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-304">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-304">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-305">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-305">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-306">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-306">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-307">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-307">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-308">кøрекорт</span><span class="sxs-lookup"><span data-stu-id="6fb6d-308">kørekort</span></span>  <br/> <span data-ttu-id="6fb6d-309">кøрекортнуммер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="6fb6d-310">Эстония</span><span class="sxs-lookup"><span data-stu-id="6fb6d-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-311">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-311">Format</span></span>

<span data-ttu-id="6fb6d-312">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-313">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-313">Pattern</span></span>

<span data-ttu-id="6fb6d-314">Две буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="6fb6d-315">Буквы "ET" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="6fb6d-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6fb6d-316">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-317">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-317">Checksum</span></span>

<span data-ttu-id="6fb6d-318">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-319">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-319">Definition</span></span>

<span data-ttu-id="6fb6d-320">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-321">Регулярное выражение `Regex_estonia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-322">Найдено ключевое `Keywords_estonia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-323">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-323">Keywords</span></span>

<span data-ttu-id="6fb6d-324">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-324"></span></span>
|<span data-ttu-id="6fb6d-325">**Кэйвордс_естониа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-326">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-326">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-327">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-327">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-328">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-328">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-329">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-329">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-330">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-330">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-331">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-331">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-332">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-333">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-334">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-335">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-335">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-336">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-336">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-337">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-337">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="6fb6d-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="6fb6d-339">Финляндия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-340">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-340">Format</span></span>

<span data-ttu-id="6fb6d-341">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-342">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-342">Pattern</span></span>

<span data-ttu-id="6fb6d-343">10 цифр, содержащих дефис:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="6fb6d-344">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="6fb6d-344">Six digits</span></span> 
    
- <span data-ttu-id="6fb6d-345">дефис;</span><span class="sxs-lookup"><span data-stu-id="6fb6d-345">A hyphen</span></span>
    
-  <span data-ttu-id="6fb6d-346">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="6fb6d-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-347">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-347">Checksum</span></span>

<span data-ttu-id="6fb6d-348">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-349">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-349">Definition</span></span>

<span data-ttu-id="6fb6d-350">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-351">Регулярное выражение `Regex_finland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-352">Найдено ключевое `Keywords_finland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-353">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-353">Keywords</span></span>

<span data-ttu-id="6fb6d-354">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-354"></span></span>
|<span data-ttu-id="6fb6d-355">**Кэйвордс_финланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-356">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-356">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-357">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-357">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-358">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-358">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-359">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-359">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-360">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-360">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-361">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-362">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-363">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-364">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-364">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-365">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-365">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-366">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-366">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-367">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-367">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-368">ажокортти</span><span class="sxs-lookup"><span data-stu-id="6fb6d-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="6fb6d-369">Франция</span><span class="sxs-lookup"><span data-stu-id="6fb6d-369">France</span></span>

<span data-ttu-id="6fb6d-370">Дополнительные сведения см. в разделе "номер водительского удостоверения для Франции" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="6fb6d-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="6fb6d-371">Германия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-371">Germany</span></span>

<span data-ttu-id="6fb6d-372">Дополнительные сведения можно найти в разделе "номер водительского удостоверения для немецкого драйвера" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="6fb6d-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="6fb6d-373">Греция</span><span class="sxs-lookup"><span data-stu-id="6fb6d-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-374">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-374">Format</span></span>

<span data-ttu-id="6fb6d-375">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-376">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-376">Pattern</span></span>

 <span data-ttu-id="6fb6d-377">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-378">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-378">Checksum</span></span>

<span data-ttu-id="6fb6d-379">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-380">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-380">Definition</span></span>

<span data-ttu-id="6fb6d-381">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-382">Регулярное выражение `Regex_greece_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-383">Найдено ключевое `Keywords_greece_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-384">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-384">Keywords</span></span>

<span data-ttu-id="6fb6d-385">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-385"></span></span>
|<span data-ttu-id="6fb6d-386">**Кэйвордс_грице_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-387">Файл</span><span class="sxs-lookup"><span data-stu-id="6fb6d-387">dlL#</span></span>  <br/> <span data-ttu-id="6fb6d-388">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-388">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-389">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-389">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-390">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-390">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-391">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-391">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-392">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-393">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-394">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-395">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-395">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-396">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-396">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-397">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-397">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-398">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-398">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="6fb6d-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="6fb6d-400">Адеиа одигисис</span><span class="sxs-lookup"><span data-stu-id="6fb6d-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="6fb6d-401">Венгрия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-402">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-402">Format</span></span>

<span data-ttu-id="6fb6d-403">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-404">Pattern</span></span>

<span data-ttu-id="6fb6d-405">Две буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="6fb6d-406">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="6fb6d-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6fb6d-407">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-408">Checksum</span></span>

<span data-ttu-id="6fb6d-409">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-410">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-410">Definition</span></span>

<span data-ttu-id="6fb6d-411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-412">Регулярное выражение `Regex_hungary_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-413">Найдено ключевое `Keywords_hungary_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-414">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-414">Keywords</span></span>

<span data-ttu-id="6fb6d-415">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-415"></span></span>
|<span data-ttu-id="6fb6d-416">**Кэйвордс_хунгари_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-417">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-417">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-418">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-418">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-419">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-419">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-420">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-420">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-421">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-421">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-422">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-423">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-424">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-425">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-425">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-426">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-426">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-427">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-427">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-428">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-428">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-429">везетои енжедели</span><span class="sxs-lookup"><span data-stu-id="6fb6d-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="6fb6d-430">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="6fb6d-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-431">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-431">Format</span></span>

<span data-ttu-id="6fb6d-432">Шесть цифр, за которыми следуют четыре буквы</span><span class="sxs-lookup"><span data-stu-id="6fb6d-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-433">Pattern</span></span>

<span data-ttu-id="6fb6d-434">Шесть цифр и четыре буквы:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="6fb6d-435">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="6fb6d-435">Six digits</span></span>
    
- <span data-ttu-id="6fb6d-436">Четыре буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="6fb6d-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-437">Checksum</span></span>

<span data-ttu-id="6fb6d-438">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-439">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-439">Definition</span></span>

<span data-ttu-id="6fb6d-440">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-441">Регулярное выражение `Regex_ireland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-442">Найдено ключевое `Keywords_ireland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-443">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-443">Keywords</span></span>

<span data-ttu-id="6fb6d-444">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-444"></span></span>
|<span data-ttu-id="6fb6d-445">**Кэйвордс_иреланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-446">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-446">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-447">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-447">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-448">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-448">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-449">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-449">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-450">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-450">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-451">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-452">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-453">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-454">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-454">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-455">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-455">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-456">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-456">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-457">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-457">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-458">цеадúнас тиомáна</span><span class="sxs-lookup"><span data-stu-id="6fb6d-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="6fb6d-459">Италия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-459">Italy</span></span>

<span data-ttu-id="6fb6d-460">Дополнительные сведения см. в разделе "номер водительского удостоверения для Италии" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="6fb6d-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="6fb6d-461">Латвия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-462">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-462">Format</span></span>

<span data-ttu-id="6fb6d-463">Три буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-464">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-464">Pattern</span></span>

<span data-ttu-id="6fb6d-465">Три буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="6fb6d-466">Три буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="6fb6d-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6fb6d-467">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-468">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-468">Checksum</span></span>

<span data-ttu-id="6fb6d-469">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-470">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-470">Definition</span></span>

<span data-ttu-id="6fb6d-471">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-472">Регулярное выражение `Regex_latvia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-473">Найдено ключевое `Keywords_latvia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-474">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-474">Keywords</span></span>

<span data-ttu-id="6fb6d-475">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-475"></span></span>
|<span data-ttu-id="6fb6d-476">**Кэйвордс_латвиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-477">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-477">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-478">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-478">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-479">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-479">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-480">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-480">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-481">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-481">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-482">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-483">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-484">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-485">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-485">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-486">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-486">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-487">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-487">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-488">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-488">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-489">аутовадīтāжа аплиекīба</span><span class="sxs-lookup"><span data-stu-id="6fb6d-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="6fb6d-490">Литва</span><span class="sxs-lookup"><span data-stu-id="6fb6d-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-491">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-491">Format</span></span>

<span data-ttu-id="6fb6d-492">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-493">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-493">Pattern</span></span>

 <span data-ttu-id="6fb6d-494">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-495">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-495">Checksum</span></span>

<span data-ttu-id="6fb6d-496">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-497">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-497">Definition</span></span>

<span data-ttu-id="6fb6d-498">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-499">Регулярное выражение `Regex_lithuania_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-500">Найдено ключевое `Keywords_lithuania_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-501">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-501">Keywords</span></span>

<span data-ttu-id="6fb6d-502">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-502"></span></span>
|<span data-ttu-id="6fb6d-503">**Кэйвордс_лисуаниа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-504">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-504">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-505">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-505">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-506">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-506">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-507">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-507">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-508">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-508">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-509">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-510">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-511">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-512">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-512">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-513">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-513">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-514">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-514">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-515">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-515">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-516">ваируотожо паžимėжимас</span><span class="sxs-lookup"><span data-stu-id="6fb6d-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="6fb6d-517">Луксембург</span><span class="sxs-lookup"><span data-stu-id="6fb6d-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-518">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-518">Format</span></span>

<span data-ttu-id="6fb6d-519">Шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-520">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-520">Pattern</span></span>

 <span data-ttu-id="6fb6d-521">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-522">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-522">Checksum</span></span>

<span data-ttu-id="6fb6d-523">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-524">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-524">Definition</span></span>

<span data-ttu-id="6fb6d-525">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-526">Регулярное выражение `Regex_luxemburg_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-527">Найдено ключевое `Keywords_luxemburg_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-528">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-528">Keywords</span></span>

<span data-ttu-id="6fb6d-529">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-529"></span></span>
|<span data-ttu-id="6fb6d-530">**Кэйвордс_луксембург_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-531">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-531">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-532">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-532">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-533">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-533">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-534">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-534">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-535">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-535">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-536">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-537">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-538">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-539">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-539">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-540">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-540">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-541">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-541">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-542">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-542">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-543">фахрерлаубнис</span><span class="sxs-lookup"><span data-stu-id="6fb6d-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="6fb6d-544">Мальта</span><span class="sxs-lookup"><span data-stu-id="6fb6d-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-545">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-545">Format</span></span>

<span data-ttu-id="6fb6d-546">Сочетание двух символов и шести цифр в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="6fb6d-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-547">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-547">Pattern</span></span>

<span data-ttu-id="6fb6d-548">Сочетание двух символов и шести цифр:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="6fb6d-549">Два символа (цифры или буквы без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="6fb6d-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="6fb6d-550">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="6fb6d-550">A space (optional)</span></span>
    
- <span data-ttu-id="6fb6d-551">три цифры; </span><span class="sxs-lookup"><span data-stu-id="6fb6d-551">Three digits</span></span>
    
- <span data-ttu-id="6fb6d-552">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="6fb6d-552">A space (optional)</span></span>
    
- <span data-ttu-id="6fb6d-553">Три цифры</span><span class="sxs-lookup"><span data-stu-id="6fb6d-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-554">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-554">Checksum</span></span>

<span data-ttu-id="6fb6d-555">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-556">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-556">Definition</span></span>

<span data-ttu-id="6fb6d-557">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-558">Регулярное выражение `Regex_malta_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-559">Найдено ключевое `Keywords_malta_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-560">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-560">Keywords</span></span>

<span data-ttu-id="6fb6d-561">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-561"></span></span>
|<span data-ttu-id="6fb6d-562">**Кэйвордс_малта_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-563">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-563">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-564">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-564">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-565">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-565">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-566">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-566">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-567">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-567">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-568">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-569">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-570">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-571">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-571">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-572">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-572">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-573">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-573">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-574">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-574">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-575">лиċензжаные зада Севкан</span><span class="sxs-lookup"><span data-stu-id="6fb6d-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="6fb6d-576">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="6fb6d-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-577">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-577">Format</span></span>

<span data-ttu-id="6fb6d-578">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-579">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-579">Pattern</span></span>

<span data-ttu-id="6fb6d-580">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-581">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-581">Checksum</span></span>

<span data-ttu-id="6fb6d-582">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-583">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-583">Definition</span></span>

<span data-ttu-id="6fb6d-584">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-585">Регулярное выражение `Regex_netherlands_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-586">Найдено ключевое `Keywords_netherlands_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-587">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-587">Keywords</span></span>

<span data-ttu-id="6fb6d-588">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-588"></span></span>
|<span data-ttu-id="6fb6d-589">**Кэйвордс_несерландс_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-590">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-590">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-591">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-591">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-592">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-592">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-593">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-593">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-594">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-594">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-595">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-596">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-597">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-598">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-598">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-599">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-599">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-600">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-600">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-601">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-601">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="6fb6d-602">permis de conduire</span></span>  <br/> <span data-ttu-id="6fb6d-603">рижбевижс</span><span class="sxs-lookup"><span data-stu-id="6fb6d-603">rijbewijs</span></span>  <br/> <span data-ttu-id="6fb6d-604">рижбевижснуммер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="6fb6d-605">Польша</span><span class="sxs-lookup"><span data-stu-id="6fb6d-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-606">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-606">Format</span></span>

<span data-ttu-id="6fb6d-607">14 цифр, содержащих 2 косых черты.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-608">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-608">Pattern</span></span>

<span data-ttu-id="6fb6d-609">14 цифр и 2 косых черт:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="6fb6d-610">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="6fb6d-610">Five digits</span></span> 
    
- <span data-ttu-id="6fb6d-611">косая черта;</span><span class="sxs-lookup"><span data-stu-id="6fb6d-611">A forward slash</span></span>
    
- <span data-ttu-id="6fb6d-612">Две цифры</span><span class="sxs-lookup"><span data-stu-id="6fb6d-612">Two digits</span></span>
    
- <span data-ttu-id="6fb6d-613">косая черта;</span><span class="sxs-lookup"><span data-stu-id="6fb6d-613">A forward slash</span></span>
    
- <span data-ttu-id="6fb6d-614">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-615">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-615">Checksum</span></span>

<span data-ttu-id="6fb6d-616">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-617">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-617">Definition</span></span>

<span data-ttu-id="6fb6d-618">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-619">Регулярное выражение `Regex_poland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-620">Найдено ключевое `Keywords_poland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-621">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-621">Keywords</span></span>

<span data-ttu-id="6fb6d-622">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-622"></span></span>
|<span data-ttu-id="6fb6d-623">**Кэйвордс_поланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-624">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-624">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-625">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-625">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-626">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-626">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-627">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-627">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-628">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-628">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-629">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-630">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-631">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-632">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-632">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-633">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-633">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-634">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-634">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-635">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-635">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-636">право жазди</span><span class="sxs-lookup"><span data-stu-id="6fb6d-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="6fb6d-637">Португалия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-638">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-638">Format</span></span>

<span data-ttu-id="6fb6d-639">Две буквы, за которыми следуют семь чисел в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="6fb6d-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-640">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-640">Pattern</span></span>

<span data-ttu-id="6fb6d-641">Две буквы, за которыми следуют семь цифр со специальными символами:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="6fb6d-642">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="6fb6d-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="6fb6d-643">дефис;</span><span class="sxs-lookup"><span data-stu-id="6fb6d-643">A hyphen</span></span>
    
- <span data-ttu-id="6fb6d-644">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="6fb6d-644">Six digits</span></span>
    
- <span data-ttu-id="6fb6d-645">Пробел</span><span class="sxs-lookup"><span data-stu-id="6fb6d-645">A space</span></span>
    
- <span data-ttu-id="6fb6d-646">одна цифра.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-647">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-647">Checksum</span></span>

<span data-ttu-id="6fb6d-648">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-649">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-649">Definition</span></span>

<span data-ttu-id="6fb6d-650">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-651">Регулярное выражение `Regex_portugal_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-652">Найдено ключевое `Keywords_portugal_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-653">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-653">Keywords</span></span>

<span data-ttu-id="6fb6d-654">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-654"></span></span>
|<span data-ttu-id="6fb6d-655">**Кэйвордс_португал_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-656">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-656">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-657">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-657">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-658">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-658">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-659">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-659">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-660">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-660">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-661">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-662">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-663">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-664">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-664">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-665">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-665">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-666">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-666">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-667">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-667">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-668">картеира de моториста</span><span class="sxs-lookup"><span data-stu-id="6fb6d-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="6fb6d-669">Румыния</span><span class="sxs-lookup"><span data-stu-id="6fb6d-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-670">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-670">Format</span></span>

<span data-ttu-id="6fb6d-671">Один символ, за которым следуют восемь цифр</span><span class="sxs-lookup"><span data-stu-id="6fb6d-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-672">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-672">Pattern</span></span>

<span data-ttu-id="6fb6d-673">Один символ, за которым следуют восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="6fb6d-674">Одна буква (без учета регистра) или цифра</span><span class="sxs-lookup"><span data-stu-id="6fb6d-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="6fb6d-675">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-676">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-676">Checksum</span></span>

<span data-ttu-id="6fb6d-677">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-678">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-678">Definition</span></span>

<span data-ttu-id="6fb6d-679">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-680">Регулярное выражение `Regex_romania_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-681">Найдено ключевое `Keywords_romania_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-682">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-682">Keywords</span></span>

<span data-ttu-id="6fb6d-683">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-683"></span></span>
|<span data-ttu-id="6fb6d-684">**Кэйвордс_романиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-685">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-685">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-686">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-686">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-687">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-687">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-688">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-688">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-689">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-689">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-690">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-691">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-692">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-693">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-693">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-694">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-694">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-695">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-695">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-696">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-696">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-697">разрешение de кондуцере</span><span class="sxs-lookup"><span data-stu-id="6fb6d-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="6fb6d-698">Словакия</span><span class="sxs-lookup"><span data-stu-id="6fb6d-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-699">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-699">Format</span></span>

<span data-ttu-id="6fb6d-700">Один символ, за которым следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-701">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-701">Pattern</span></span>

<span data-ttu-id="6fb6d-702">Один символ, за которым следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="6fb6d-703">Одна буква (без учета регистра) или цифра</span><span class="sxs-lookup"><span data-stu-id="6fb6d-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="6fb6d-704">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-705">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-705">Checksum</span></span>

<span data-ttu-id="6fb6d-706">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-707">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-707">Definition</span></span>

<span data-ttu-id="6fb6d-708">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-709">Регулярное выражение `Regex_slovakia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-710">Найдено ключевое `Keywords_slovakia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-711">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-711">Keywords</span></span>

<span data-ttu-id="6fb6d-712">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-712"></span></span>
|<span data-ttu-id="6fb6d-713">**Кэйвордс_словакиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-714">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-714">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-715">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-715">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-716">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-716">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-717">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-717">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-718">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-718">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-719">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-720">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-721">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-722">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-722">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-723">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-723">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-724">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-724">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-725">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-725">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-726">водиčскý преуказ</span><span class="sxs-lookup"><span data-stu-id="6fb6d-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="6fb6d-727">Словения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-728">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-728">Format</span></span>

<span data-ttu-id="6fb6d-729">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="6fb6d-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-730">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-730">Pattern</span></span>

<span data-ttu-id="6fb6d-731">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="6fb6d-732">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-732">Checksum</span></span>

<span data-ttu-id="6fb6d-733">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-734">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-734">Definition</span></span>

<span data-ttu-id="6fb6d-735">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-736">Регулярное выражение `Regex_slovenia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-737">Найдено ключевое `Keywords_slovenia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-738">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-738">Keywords</span></span>

<span data-ttu-id="6fb6d-739">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-739"></span></span>
|<span data-ttu-id="6fb6d-740">**Кэйвордс_словениа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-741">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-741">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-742">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-742">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-743">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-743">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-744">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-744">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-745">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-745">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-746">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-747">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-748">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-749">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-749">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-750">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-750">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-751">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-751">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-752">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-752">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-753">возниšко доволженже</span><span class="sxs-lookup"><span data-stu-id="6fb6d-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="6fb6d-754">Испания</span><span class="sxs-lookup"><span data-stu-id="6fb6d-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-755">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-755">Format</span></span>

<span data-ttu-id="6fb6d-756">Восемь цифр, за которыми следует один символ</span><span class="sxs-lookup"><span data-stu-id="6fb6d-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-757">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-757">Pattern</span></span>

<span data-ttu-id="6fb6d-758">Восемь цифр, за которыми следует один символ:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="6fb6d-759">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-759">Eight digits</span></span> 
    
- <span data-ttu-id="6fb6d-760">Одна цифра или буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="6fb6d-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-761">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-761">Checksum</span></span>

<span data-ttu-id="6fb6d-762">Да</span><span class="sxs-lookup"><span data-stu-id="6fb6d-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-763">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-763">Definition</span></span>

<span data-ttu-id="6fb6d-764">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-765">Функция `Func_spain_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-766">Найдено ключевое `Keywords_spain_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-767">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-767">Keywords</span></span>

<span data-ttu-id="6fb6d-768">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-768"></span></span>
|<span data-ttu-id="6fb6d-769">**Кэйвордс_спаин_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-770">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-770">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-771">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-771">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-772">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-772">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-773">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-773">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-774">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-774">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-775">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-776">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-777">driver's licence</span></span>  <br/> <span data-ttu-id="6fb6d-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-778">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-779">driving licence</span></span>  <br/> <span data-ttu-id="6fb6d-780">driving license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-780">driving license</span></span>  <br/> <span data-ttu-id="6fb6d-781">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-781">driver licence number</span></span>  <br/> <span data-ttu-id="6fb6d-782">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-782">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-783">драйвер номер лицензии</span><span class="sxs-lookup"><span data-stu-id="6fb6d-783">drivers licence number</span></span>  <br/> <span data-ttu-id="6fb6d-784">номер лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="6fb6d-784">drivers license number</span></span>  <br/> <span data-ttu-id="6fb6d-785">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-785">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-786">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-786">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-787">номер водительской лицензии</span><span class="sxs-lookup"><span data-stu-id="6fb6d-787">driving licence number</span></span>  <br/> <span data-ttu-id="6fb6d-788">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-788">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-789">движущие разрешение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-789">driving permit</span></span>  <br/> <span data-ttu-id="6fb6d-790">движущие число разрешений</span><span class="sxs-lookup"><span data-stu-id="6fb6d-790">driving permit number</span></span>  <br/> <span data-ttu-id="6fb6d-791">пермисо de кондукЦиóн</span><span class="sxs-lookup"><span data-stu-id="6fb6d-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="6fb6d-792">пермисо кондукЦиóн</span><span class="sxs-lookup"><span data-stu-id="6fb6d-792">permiso conducción</span></span>  <br/> <span data-ttu-id="6fb6d-793">нúмеро лиценЦиа кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="6fb6d-794">нúмеро de карнет де кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="6fb6d-795">нúмеро карнет кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="6fb6d-796">лиценЦиа кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-796">licencia conducir</span></span>  <br/> <span data-ttu-id="6fb6d-797">нúмеро de пермисо де кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="6fb6d-798">нúмеро де пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="6fb6d-799">нúмеро пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="6fb6d-800">пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-800">permiso conducir</span></span>  <br/> <span data-ttu-id="6fb6d-801">лиценЦиа de манежо</span><span class="sxs-lookup"><span data-stu-id="6fb6d-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="6fb6d-802">El карнет de кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="6fb6d-803">Карнет кондуЦир</span><span class="sxs-lookup"><span data-stu-id="6fb6d-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="6fb6d-804">Швеция</span><span class="sxs-lookup"><span data-stu-id="6fb6d-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="6fb6d-805">Format</span><span class="sxs-lookup"><span data-stu-id="6fb6d-805">Format</span></span>

<span data-ttu-id="6fb6d-806">Десять цифр, содержащие дефис</span><span class="sxs-lookup"><span data-stu-id="6fb6d-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="6fb6d-807">Шаблон</span><span class="sxs-lookup"><span data-stu-id="6fb6d-807">Pattern</span></span>

<span data-ttu-id="6fb6d-808">Десять цифр, содержащих дефис:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="6fb6d-809">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="6fb6d-809">Six digits</span></span> 
    
- <span data-ttu-id="6fb6d-810">дефис;</span><span class="sxs-lookup"><span data-stu-id="6fb6d-810">A hyphen</span></span>
    
- <span data-ttu-id="6fb6d-811">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="6fb6d-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="6fb6d-812">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="6fb6d-812">Checksum</span></span>

<span data-ttu-id="6fb6d-813">Нет</span><span class="sxs-lookup"><span data-stu-id="6fb6d-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="6fb6d-814">Определение</span><span class="sxs-lookup"><span data-stu-id="6fb6d-814">Definition</span></span>

<span data-ttu-id="6fb6d-815">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="6fb6d-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="6fb6d-816">Регулярное выражение `Regex_sweden_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="6fb6d-817">Найдено ключевое `Keywords_sweden_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="6fb6d-818">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="6fb6d-818">Keywords</span></span>

<span data-ttu-id="6fb6d-819">| |</span><span class="sxs-lookup"><span data-stu-id="6fb6d-819"></span></span>
|<span data-ttu-id="6fb6d-820">**Кэйвордс_сведен_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="6fb6d-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="6fb6d-821">DL</span><span class="sxs-lookup"><span data-stu-id="6fb6d-821">dl#</span></span>  <br/> <span data-ttu-id="6fb6d-822">driver license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-822">driver license</span></span>  <br/> <span data-ttu-id="6fb6d-823">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-823">driver license number</span></span>  <br/> <span data-ttu-id="6fb6d-824">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-824">driver licence</span></span>  <br/> <span data-ttu-id="6fb6d-825">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="6fb6d-825">drivers lic.</span></span>  <br/> <span data-ttu-id="6fb6d-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-826">drivers license</span></span>  <br/> <span data-ttu-id="6fb6d-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="6fb6d-827">drivers licence</span></span>  <br/> <span data-ttu-id="6fb6d-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="6fb6d-828">driver's license</span></span>  <br/> <span data-ttu-id="6fb6d-829">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-829">driver's license number</span></span>  <br/> <span data-ttu-id="6fb6d-830">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="6fb6d-830">driver's licence number</span></span>  <br/> <span data-ttu-id="6fb6d-831">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="6fb6d-831">driving license number</span></span>  <br/> <span data-ttu-id="6fb6d-832">длно #</span><span class="sxs-lookup"><span data-stu-id="6fb6d-832">dlno#</span></span>  <br/> <span data-ttu-id="6fb6d-833">кöркорт</span><span class="sxs-lookup"><span data-stu-id="6fb6d-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="6fb6d-834">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="6fb6d-834">UK</span></span>

<span data-ttu-id="6fb6d-835">Дополнительные сведения см. в разделе "Великобритания</span><span class="sxs-lookup"><span data-stu-id="6fb6d-835">For details, see the section "U.K.</span></span> <span data-ttu-id="6fb6d-836">Номер водительского удостоверения, в [котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="6fb6d-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6fb6d-837">См. также</span><span class="sxs-lookup"><span data-stu-id="6fb6d-837">See also</span></span>

[<span data-ttu-id="6fb6d-838">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="6fb6d-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

