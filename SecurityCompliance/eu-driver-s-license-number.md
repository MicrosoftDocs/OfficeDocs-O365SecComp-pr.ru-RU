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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255777"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="ab2df-104">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="ab2df-104">EU Driver's License Number</span></span>

<span data-ttu-id="ab2df-105">В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации номера лицензии для драйвера ЕС.</span><span class="sxs-lookup"><span data-stu-id="ab2df-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="ab2df-106">Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.</span><span class="sxs-lookup"><span data-stu-id="ab2df-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="ab2df-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="ab2df-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-108">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-108">Format</span></span>

<span data-ttu-id="ab2df-109">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-110">Pattern</span></span>

<span data-ttu-id="ab2df-111">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ab2df-112">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-112">Checksum</span></span>

<span data-ttu-id="ab2df-113">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-114">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-114">Definition</span></span>

<span data-ttu-id="ab2df-115">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-116">Регулярное выражение `Regex_austria_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-117">Найдено ключевое `Keywords_austria_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="ab2df-118">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-118">Keywords</span></span>

<span data-ttu-id="ab2df-119">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-119"></span></span>
|<span data-ttu-id="ab2df-120">**Кэйвордс_аустриа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-121">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-121">dl#</span></span>  <br/> <span data-ttu-id="ab2df-122">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-122">driver license</span></span>  <br/> <span data-ttu-id="ab2df-123">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-123">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-124">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-124">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-125">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-125">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-126">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-127">driver's licence</span></span>  <br/> <span data-ttu-id="ab2df-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-128">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-129">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-129">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-130">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="ab2df-131">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-131">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-132">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-132">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-133">фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="ab2df-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="ab2df-134">фухрерсчеин Републик остерреич</span><span class="sxs-lookup"><span data-stu-id="ab2df-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="ab2df-135">Бельгия</span><span class="sxs-lookup"><span data-stu-id="ab2df-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-136">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-136">Format</span></span>

<span data-ttu-id="ab2df-137">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-138">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-138">Pattern</span></span>

<span data-ttu-id="ab2df-139">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ab2df-140">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-140">Checksum</span></span>

<span data-ttu-id="ab2df-141">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-142">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-142">Definition</span></span>

<span data-ttu-id="ab2df-143">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-144">Регулярное выражение `Regex_belgium_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-145">Найдено ключевое `Keywords_belgium_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="ab2df-146">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-146">Keywords</span></span>

<span data-ttu-id="ab2df-147">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-147"></span></span>
|<span data-ttu-id="ab2df-148">**Кэйвордс__белгиум_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-149">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-149">dl#</span></span>  <br/> <span data-ttu-id="ab2df-150">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-150">driver license</span></span>  <br/> <span data-ttu-id="ab2df-151">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-151">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-152">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-152">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-153">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-153">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-154">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-155">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-156">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-157">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-157">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-158">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-158">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-159">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-159">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-160">рижбевижс</span><span class="sxs-lookup"><span data-stu-id="ab2df-160">rijbewijs</span></span>  <br/> <span data-ttu-id="ab2df-161">рижбевижснуммер</span><span class="sxs-lookup"><span data-stu-id="ab2df-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="ab2df-162">фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="ab2df-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="ab2df-163">фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="ab2df-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="ab2df-164">фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="ab2df-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="ab2df-165">фüхрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="ab2df-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="ab2df-166">фуехрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="ab2df-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="ab2df-167">фуехрерсчеин — НР</span><span class="sxs-lookup"><span data-stu-id="ab2df-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="ab2df-168">Болгария</span><span class="sxs-lookup"><span data-stu-id="ab2df-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-169">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-169">Format</span></span>

<span data-ttu-id="ab2df-170">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-171">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-171">Pattern</span></span>

<span data-ttu-id="ab2df-172">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ab2df-173">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-173">Checksum</span></span>

<span data-ttu-id="ab2df-174">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-175">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-175">Definition</span></span>

<span data-ttu-id="ab2df-176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-177">Регулярное выражение `Regex_bulgaria_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-178">Найдено ключевое `Keywords_bulgaria_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="ab2df-179">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-179">Keywords</span></span>

<span data-ttu-id="ab2df-180">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-180"></span></span>
|<span data-ttu-id="ab2df-181">**Кэйвордс_булгариа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-182">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-182">dl#</span></span>  <br/> <span data-ttu-id="ab2df-183">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-183">driver license</span></span>  <br/> <span data-ttu-id="ab2df-184">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-184">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-185">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-185">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-186">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-186">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-187">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-188">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-189">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-190">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-190">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-191">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-191">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-192">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-192">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-193">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-193">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-194">свидетелство за управление на МПС</span><span class="sxs-lookup"><span data-stu-id="ab2df-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="ab2df-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="ab2df-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="ab2df-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="ab2df-196">сумпс</span></span>  <br/> <span data-ttu-id="ab2df-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="ab2df-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="ab2df-198">Хорватия</span><span class="sxs-lookup"><span data-stu-id="ab2df-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-199">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-199">Format</span></span>

<span data-ttu-id="ab2df-200">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-201">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-201">Pattern</span></span>

<span data-ttu-id="ab2df-202">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ab2df-203">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-203">Checksum</span></span>

<span data-ttu-id="ab2df-204">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-205">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-205">Definition</span></span>

<span data-ttu-id="ab2df-206">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-207">Регулярное выражение `Regex_croatia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-208">Найдено ключевое `Keywords_croatia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="ab2df-209">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-209">Keywords</span></span>

<span data-ttu-id="ab2df-210">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-210"></span></span>
|<span data-ttu-id="ab2df-211">**Кэйвордс_кроатиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-212">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-212">dl#</span></span>  <br/> <span data-ttu-id="ab2df-213">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-213">driver license</span></span>  <br/> <span data-ttu-id="ab2df-214">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-214">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-215">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-215">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-216">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-216">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-217">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-218">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-219">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-220">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-220">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-221">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-221">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-222">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-222">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-223">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-223">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-224">возаčка дозвола</span><span class="sxs-lookup"><span data-stu-id="ab2df-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="ab2df-225">Кипр</span><span class="sxs-lookup"><span data-stu-id="ab2df-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-226">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-226">Format</span></span>

<span data-ttu-id="ab2df-227">12 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-228">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-228">Pattern</span></span>

<span data-ttu-id="ab2df-229">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ab2df-230">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-230">Checksum</span></span>

<span data-ttu-id="ab2df-231">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-232">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-232">Definition</span></span>

<span data-ttu-id="ab2df-233">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-234">Регулярное выражение `Regex_cyprus_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-235">Найдено ключевое `Keywords_cyprus_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-236">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-236">Keywords</span></span>

<span data-ttu-id="ab2df-237">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-237"></span></span>
|<span data-ttu-id="ab2df-238">**Кэйвордс_ципрус_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-239">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-239">dl#</span></span>  <br/> <span data-ttu-id="ab2df-240">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-240">driver license</span></span>  <br/> <span data-ttu-id="ab2df-241">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-241">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-242">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-242">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-243">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-243">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-244">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-245">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-246">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-246">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-247">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-247">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-248">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-248">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-249">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-249">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="ab2df-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="ab2df-251">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="ab2df-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-252">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-252">Format</span></span>

<span data-ttu-id="ab2df-253">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-254">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-254">Pattern</span></span>

<span data-ttu-id="ab2df-255">Восемь букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="ab2df-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="ab2df-256">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="ab2df-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="ab2df-257">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="ab2df-257">A space (optional)</span></span>
    
- <span data-ttu-id="ab2df-258">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-259">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-259">Checksum</span></span>

<span data-ttu-id="ab2df-260">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-261">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-261">Definition</span></span>

<span data-ttu-id="ab2df-262">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-263">Регулярное выражение `Regex_czech_republic_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-264">Найдено ключевое `Keywords_czech_republic_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="ab2df-265">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-265">Keywords</span></span>

<span data-ttu-id="ab2df-266">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-266"></span></span>
|<span data-ttu-id="ab2df-267">**Кэйвордс_кзеч_републик_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-268">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-268">dl#</span></span>  <br/> <span data-ttu-id="ab2df-269">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-269">driver license</span></span>  <br/> <span data-ttu-id="ab2df-270">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-270">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-271">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-271">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-272">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-272">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-273">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-274">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-275">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-276">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-276">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-277">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-277">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-278">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-278">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-279">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-279">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-280">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-280">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-281">řидиčскý прúказ</span><span class="sxs-lookup"><span data-stu-id="ab2df-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="ab2df-282">Дания</span><span class="sxs-lookup"><span data-stu-id="ab2df-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-283">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-283">Format</span></span>

<span data-ttu-id="ab2df-284">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-285">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-285">Pattern</span></span>

<span data-ttu-id="ab2df-286">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ab2df-287">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-287">Checksum</span></span>

<span data-ttu-id="ab2df-288">Да</span><span class="sxs-lookup"><span data-stu-id="ab2df-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-289">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-289">Definition</span></span>

<span data-ttu-id="ab2df-290">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-291">Регулярное выражение `Regex_denmark_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-292">Найдено ключевое `Keywords_denmark_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="ab2df-293">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-293">Keywords</span></span>

<span data-ttu-id="ab2df-294">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-294"></span></span>
|<span data-ttu-id="ab2df-295">**Кэйвордс_денмарк_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-296">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-296">dl#</span></span>  <br/> <span data-ttu-id="ab2df-297">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-297">driver license</span></span>  <br/> <span data-ttu-id="ab2df-298">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-298">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-299">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-299">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-300">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-300">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-301">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-302">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-303">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-304">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-304">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-305">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-305">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-306">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-306">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-307">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-307">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-308">кøрекорт</span><span class="sxs-lookup"><span data-stu-id="ab2df-308">kørekort</span></span>  <br/> <span data-ttu-id="ab2df-309">кøрекортнуммер</span><span class="sxs-lookup"><span data-stu-id="ab2df-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="ab2df-310">Эстония</span><span class="sxs-lookup"><span data-stu-id="ab2df-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-311">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-311">Format</span></span>

<span data-ttu-id="ab2df-312">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-313">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-313">Pattern</span></span>

<span data-ttu-id="ab2df-314">Две буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="ab2df-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="ab2df-315">Буквы "ET" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="ab2df-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="ab2df-316">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-317">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-317">Checksum</span></span>

<span data-ttu-id="ab2df-318">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-319">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-319">Definition</span></span>

<span data-ttu-id="ab2df-320">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-321">Регулярное выражение `Regex_estonia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-322">Найдено ключевое `Keywords_estonia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-323">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-323">Keywords</span></span>

<span data-ttu-id="ab2df-324">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-324"></span></span>
|<span data-ttu-id="ab2df-325">**Кэйвордс_естониа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-326">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-326">dl#</span></span>  <br/> <span data-ttu-id="ab2df-327">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-327">driver license</span></span>  <br/> <span data-ttu-id="ab2df-328">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-328">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-329">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-329">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-330">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-330">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-331">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-331">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-332">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-333">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-334">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-335">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-335">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-336">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-336">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-337">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-337">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="ab2df-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="ab2df-339">Финляндия</span><span class="sxs-lookup"><span data-stu-id="ab2df-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-340">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-340">Format</span></span>

<span data-ttu-id="ab2df-341">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="ab2df-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-342">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-342">Pattern</span></span>

<span data-ttu-id="ab2df-343">10 цифр, содержащих дефис:</span><span class="sxs-lookup"><span data-stu-id="ab2df-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="ab2df-344">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="ab2df-344">Six digits</span></span> 
    
- <span data-ttu-id="ab2df-345">дефис;</span><span class="sxs-lookup"><span data-stu-id="ab2df-345">A hyphen</span></span>
    
-  <span data-ttu-id="ab2df-346">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="ab2df-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="ab2df-347">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-347">Checksum</span></span>

<span data-ttu-id="ab2df-348">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-349">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-349">Definition</span></span>

<span data-ttu-id="ab2df-350">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-351">Регулярное выражение `Regex_finland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-352">Найдено ключевое `Keywords_finland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-353">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-353">Keywords</span></span>

<span data-ttu-id="ab2df-354">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-354"></span></span>
|<span data-ttu-id="ab2df-355">**Кэйвордс_финланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-356">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-356">dl#</span></span>  <br/> <span data-ttu-id="ab2df-357">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-357">driver license</span></span>  <br/> <span data-ttu-id="ab2df-358">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-358">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-359">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-359">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-360">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-360">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-361">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-362">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-363">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-364">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-364">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-365">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-365">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-366">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-366">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-367">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-367">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-368">ажокортти</span><span class="sxs-lookup"><span data-stu-id="ab2df-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="ab2df-369">Франция</span><span class="sxs-lookup"><span data-stu-id="ab2df-369">France</span></span>

<span data-ttu-id="ab2df-370">Дополнительные сведения см. в разделе "номер водительского удостоверения для Франции" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="ab2df-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="ab2df-371">Германия</span><span class="sxs-lookup"><span data-stu-id="ab2df-371">Germany</span></span>

<span data-ttu-id="ab2df-372">Дополнительные сведения можно найти в разделе "номер водительского удостоверения для немецкого драйвера" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="ab2df-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="ab2df-373">Греция</span><span class="sxs-lookup"><span data-stu-id="ab2df-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-374">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-374">Format</span></span>

<span data-ttu-id="ab2df-375">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-376">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-376">Pattern</span></span>

 <span data-ttu-id="ab2df-377">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="ab2df-378">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-378">Checksum</span></span>

<span data-ttu-id="ab2df-379">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-380">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-380">Definition</span></span>

<span data-ttu-id="ab2df-381">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-382">Регулярное выражение `Regex_greece_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-383">Найдено ключевое `Keywords_greece_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-384">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-384">Keywords</span></span>

<span data-ttu-id="ab2df-385">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-385"></span></span>
|<span data-ttu-id="ab2df-386">**Кэйвордс_грице_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-387">Файл</span><span class="sxs-lookup"><span data-stu-id="ab2df-387">dlL#</span></span>  <br/> <span data-ttu-id="ab2df-388">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-388">driver license</span></span>  <br/> <span data-ttu-id="ab2df-389">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-389">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-390">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-390">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-391">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-391">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-392">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-393">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-394">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-395">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-395">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-396">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-396">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-397">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-397">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-398">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-398">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="ab2df-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="ab2df-400">Адеиа одигисис</span><span class="sxs-lookup"><span data-stu-id="ab2df-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="ab2df-401">Венгрия</span><span class="sxs-lookup"><span data-stu-id="ab2df-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-402">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-402">Format</span></span>

<span data-ttu-id="ab2df-403">Две буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-404">Pattern</span></span>

<span data-ttu-id="ab2df-405">Две буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="ab2df-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="ab2df-406">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="ab2df-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="ab2df-407">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-408">Checksum</span></span>

<span data-ttu-id="ab2df-409">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-410">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-410">Definition</span></span>

<span data-ttu-id="ab2df-411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-412">Регулярное выражение `Regex_hungary_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-413">Найдено ключевое `Keywords_hungary_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-414">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-414">Keywords</span></span>

<span data-ttu-id="ab2df-415">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-415"></span></span>
|<span data-ttu-id="ab2df-416">**Кэйвордс_хунгари_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-417">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-417">dl#</span></span>  <br/> <span data-ttu-id="ab2df-418">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-418">driver license</span></span>  <br/> <span data-ttu-id="ab2df-419">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-419">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-420">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-420">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-421">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-421">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-422">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-423">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-424">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-425">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-425">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-426">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-426">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-427">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-427">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-428">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-428">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-429">везетои енжедели</span><span class="sxs-lookup"><span data-stu-id="ab2df-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="ab2df-430">Ireland (Ирландия)</span><span class="sxs-lookup"><span data-stu-id="ab2df-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-431">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-431">Format</span></span>

<span data-ttu-id="ab2df-432">Шесть цифр, за которыми следуют четыре буквы</span><span class="sxs-lookup"><span data-stu-id="ab2df-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-433">Pattern</span></span>

<span data-ttu-id="ab2df-434">Шесть цифр и четыре буквы:</span><span class="sxs-lookup"><span data-stu-id="ab2df-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="ab2df-435">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="ab2df-435">Six digits</span></span>
    
- <span data-ttu-id="ab2df-436">Четыре буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="ab2df-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-437">Checksum</span></span>

<span data-ttu-id="ab2df-438">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-439">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-439">Definition</span></span>

<span data-ttu-id="ab2df-440">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-441">Регулярное выражение `Regex_ireland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-442">Найдено ключевое `Keywords_ireland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-443">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-443">Keywords</span></span>

<span data-ttu-id="ab2df-444">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-444"></span></span>
|<span data-ttu-id="ab2df-445">**Кэйвордс_иреланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-446">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-446">dl#</span></span>  <br/> <span data-ttu-id="ab2df-447">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-447">driver license</span></span>  <br/> <span data-ttu-id="ab2df-448">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-448">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-449">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-449">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-450">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-450">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-451">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-452">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-453">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-454">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-454">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-455">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-455">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-456">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-456">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-457">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-457">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-458">цеадúнас тиомáна</span><span class="sxs-lookup"><span data-stu-id="ab2df-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="ab2df-459">Италия</span><span class="sxs-lookup"><span data-stu-id="ab2df-459">Italy</span></span>

<span data-ttu-id="ab2df-460">Дополнительные сведения см. в разделе "номер водительского удостоверения для Италии" [, который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="ab2df-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="ab2df-461">Латвия</span><span class="sxs-lookup"><span data-stu-id="ab2df-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-462">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-462">Format</span></span>

<span data-ttu-id="ab2df-463">Три буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-464">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-464">Pattern</span></span>

<span data-ttu-id="ab2df-465">Три буквы и шесть цифр:</span><span class="sxs-lookup"><span data-stu-id="ab2df-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="ab2df-466">Три буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="ab2df-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="ab2df-467">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-468">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-468">Checksum</span></span>

<span data-ttu-id="ab2df-469">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-470">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-470">Definition</span></span>

<span data-ttu-id="ab2df-471">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-472">Регулярное выражение `Regex_latvia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-473">Найдено ключевое `Keywords_latvia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-474">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-474">Keywords</span></span>

<span data-ttu-id="ab2df-475">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-475"></span></span>
|<span data-ttu-id="ab2df-476">**Кэйвордс_латвиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-477">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-477">dl#</span></span>  <br/> <span data-ttu-id="ab2df-478">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-478">driver license</span></span>  <br/> <span data-ttu-id="ab2df-479">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-479">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-480">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-480">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-481">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-481">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-482">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-483">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-484">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-485">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-485">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-486">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-486">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-487">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-487">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-488">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-488">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-489">аутовадīтāжа аплиекīба</span><span class="sxs-lookup"><span data-stu-id="ab2df-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="ab2df-490">Литва</span><span class="sxs-lookup"><span data-stu-id="ab2df-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-491">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-491">Format</span></span>

<span data-ttu-id="ab2df-492">Восемь цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-493">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-493">Pattern</span></span>

 <span data-ttu-id="ab2df-494">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="ab2df-495">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-495">Checksum</span></span>

<span data-ttu-id="ab2df-496">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-497">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-497">Definition</span></span>

<span data-ttu-id="ab2df-498">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-499">Регулярное выражение `Regex_lithuania_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-500">Найдено ключевое `Keywords_lithuania_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-501">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-501">Keywords</span></span>

<span data-ttu-id="ab2df-502">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-502"></span></span>
|<span data-ttu-id="ab2df-503">**Кэйвордс_лисуаниа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-504">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-504">dl#</span></span>  <br/> <span data-ttu-id="ab2df-505">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-505">driver license</span></span>  <br/> <span data-ttu-id="ab2df-506">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-506">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-507">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-507">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-508">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-508">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-509">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-510">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-511">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-512">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-512">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-513">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-513">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-514">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-514">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-515">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-515">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-516">ваируотожо паžимėжимас</span><span class="sxs-lookup"><span data-stu-id="ab2df-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="ab2df-517">Луксембург</span><span class="sxs-lookup"><span data-stu-id="ab2df-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-518">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-518">Format</span></span>

<span data-ttu-id="ab2df-519">Шесть цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-520">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-520">Pattern</span></span>

 <span data-ttu-id="ab2df-521">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="ab2df-522">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-522">Checksum</span></span>

<span data-ttu-id="ab2df-523">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-524">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-524">Definition</span></span>

<span data-ttu-id="ab2df-525">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-526">Регулярное выражение `Regex_luxemburg_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-527">Найдено ключевое `Keywords_luxemburg_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-528">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-528">Keywords</span></span>

<span data-ttu-id="ab2df-529">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-529"></span></span>
|<span data-ttu-id="ab2df-530">**Кэйвордс_луксембург_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-531">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-531">dl#</span></span>  <br/> <span data-ttu-id="ab2df-532">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-532">driver license</span></span>  <br/> <span data-ttu-id="ab2df-533">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-533">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-534">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-534">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-535">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-535">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-536">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-537">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-538">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-539">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-539">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-540">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-540">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-541">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-541">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-542">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-542">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-543">фахрерлаубнис</span><span class="sxs-lookup"><span data-stu-id="ab2df-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="ab2df-544">Мальта</span><span class="sxs-lookup"><span data-stu-id="ab2df-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-545">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-545">Format</span></span>

<span data-ttu-id="ab2df-546">Сочетание двух символов и шести цифр в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="ab2df-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-547">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-547">Pattern</span></span>

<span data-ttu-id="ab2df-548">Сочетание двух символов и шести цифр:</span><span class="sxs-lookup"><span data-stu-id="ab2df-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="ab2df-549">Два символа (цифры или буквы без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="ab2df-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="ab2df-550">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="ab2df-550">A space (optional)</span></span>
    
- <span data-ttu-id="ab2df-551">три цифры; </span><span class="sxs-lookup"><span data-stu-id="ab2df-551">Three digits</span></span>
    
- <span data-ttu-id="ab2df-552">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="ab2df-552">A space (optional)</span></span>
    
- <span data-ttu-id="ab2df-553">Три цифры</span><span class="sxs-lookup"><span data-stu-id="ab2df-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-554">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-554">Checksum</span></span>

<span data-ttu-id="ab2df-555">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-556">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-556">Definition</span></span>

<span data-ttu-id="ab2df-557">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-558">Регулярное выражение `Regex_malta_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-559">Найдено ключевое `Keywords_malta_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-560">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-560">Keywords</span></span>

<span data-ttu-id="ab2df-561">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-561"></span></span>
|<span data-ttu-id="ab2df-562">**Кэйвордс_малта_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-563">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-563">dl#</span></span>  <br/> <span data-ttu-id="ab2df-564">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-564">driver license</span></span>  <br/> <span data-ttu-id="ab2df-565">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-565">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-566">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-566">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-567">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-567">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-568">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-569">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-570">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-571">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-571">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-572">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-572">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-573">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-573">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-574">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-574">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-575">лиċензжаные зада Севкан</span><span class="sxs-lookup"><span data-stu-id="ab2df-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="ab2df-576">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="ab2df-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-577">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-577">Format</span></span>

<span data-ttu-id="ab2df-578">10 цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-579">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-579">Pattern</span></span>

<span data-ttu-id="ab2df-580">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ab2df-581">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-581">Checksum</span></span>

<span data-ttu-id="ab2df-582">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-583">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-583">Definition</span></span>

<span data-ttu-id="ab2df-584">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-585">Регулярное выражение `Regex_netherlands_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-586">Найдено ключевое `Keywords_netherlands_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-587">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-587">Keywords</span></span>

<span data-ttu-id="ab2df-588">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-588"></span></span>
|<span data-ttu-id="ab2df-589">**Кэйвордс_несерландс_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-590">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-590">dl#</span></span>  <br/> <span data-ttu-id="ab2df-591">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-591">driver license</span></span>  <br/> <span data-ttu-id="ab2df-592">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-592">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-593">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-593">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-594">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-594">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-595">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-596">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-597">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-598">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-598">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-599">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-599">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-600">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-600">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-601">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-601">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="ab2df-602">permis de conduire</span></span>  <br/> <span data-ttu-id="ab2df-603">рижбевижс</span><span class="sxs-lookup"><span data-stu-id="ab2df-603">rijbewijs</span></span>  <br/> <span data-ttu-id="ab2df-604">рижбевижснуммер</span><span class="sxs-lookup"><span data-stu-id="ab2df-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="ab2df-605">Польша</span><span class="sxs-lookup"><span data-stu-id="ab2df-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-606">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-606">Format</span></span>

<span data-ttu-id="ab2df-607">14 цифр, содержащих 2 косых черты.</span><span class="sxs-lookup"><span data-stu-id="ab2df-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-608">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-608">Pattern</span></span>

<span data-ttu-id="ab2df-609">14 цифр и 2 косых черт:</span><span class="sxs-lookup"><span data-stu-id="ab2df-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="ab2df-610">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="ab2df-610">Five digits</span></span> 
    
- <span data-ttu-id="ab2df-611">косая черта;</span><span class="sxs-lookup"><span data-stu-id="ab2df-611">A forward slash</span></span>
    
- <span data-ttu-id="ab2df-612">Две цифры</span><span class="sxs-lookup"><span data-stu-id="ab2df-612">Two digits</span></span>
    
- <span data-ttu-id="ab2df-613">косая черта;</span><span class="sxs-lookup"><span data-stu-id="ab2df-613">A forward slash</span></span>
    
- <span data-ttu-id="ab2df-614">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-615">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-615">Checksum</span></span>

<span data-ttu-id="ab2df-616">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-617">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-617">Definition</span></span>

<span data-ttu-id="ab2df-618">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-619">Регулярное выражение `Regex_poland_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-620">Найдено ключевое `Keywords_poland_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-621">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-621">Keywords</span></span>

<span data-ttu-id="ab2df-622">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-622"></span></span>
|<span data-ttu-id="ab2df-623">**Кэйвордс_поланд_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-624">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-624">dl#</span></span>  <br/> <span data-ttu-id="ab2df-625">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-625">driver license</span></span>  <br/> <span data-ttu-id="ab2df-626">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-626">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-627">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-627">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-628">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-628">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-629">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-630">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-631">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-632">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-632">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-633">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-633">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-634">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-634">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-635">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-635">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-636">право жазди</span><span class="sxs-lookup"><span data-stu-id="ab2df-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="ab2df-637">Португалия</span><span class="sxs-lookup"><span data-stu-id="ab2df-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-638">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-638">Format</span></span>

<span data-ttu-id="ab2df-639">Две буквы, за которыми следуют семь чисел в указанном шаблоне</span><span class="sxs-lookup"><span data-stu-id="ab2df-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-640">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-640">Pattern</span></span>

<span data-ttu-id="ab2df-641">Две буквы, за которыми следуют семь цифр со специальными символами:</span><span class="sxs-lookup"><span data-stu-id="ab2df-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="ab2df-642">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="ab2df-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="ab2df-643">дефис;</span><span class="sxs-lookup"><span data-stu-id="ab2df-643">A hyphen</span></span>
    
- <span data-ttu-id="ab2df-644">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="ab2df-644">Six digits</span></span>
    
- <span data-ttu-id="ab2df-645">Пробел</span><span class="sxs-lookup"><span data-stu-id="ab2df-645">A space</span></span>
    
- <span data-ttu-id="ab2df-646">одна цифра.</span><span class="sxs-lookup"><span data-stu-id="ab2df-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-647">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-647">Checksum</span></span>

<span data-ttu-id="ab2df-648">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-649">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-649">Definition</span></span>

<span data-ttu-id="ab2df-650">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-651">Регулярное выражение `Regex_portugal_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-652">Найдено ключевое `Keywords_portugal_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-653">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-653">Keywords</span></span>

<span data-ttu-id="ab2df-654">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-654"></span></span>
|<span data-ttu-id="ab2df-655">**Кэйвордс_португал_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-656">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-656">dl#</span></span>  <br/> <span data-ttu-id="ab2df-657">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-657">driver license</span></span>  <br/> <span data-ttu-id="ab2df-658">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-658">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-659">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-659">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-660">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-660">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-661">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-662">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-663">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-664">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-664">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-665">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-665">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-666">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-666">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-667">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-667">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-668">картеира de моториста</span><span class="sxs-lookup"><span data-stu-id="ab2df-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="ab2df-669">Румыния</span><span class="sxs-lookup"><span data-stu-id="ab2df-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-670">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-670">Format</span></span>

<span data-ttu-id="ab2df-671">Один символ, за которым следуют восемь цифр</span><span class="sxs-lookup"><span data-stu-id="ab2df-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-672">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-672">Pattern</span></span>

<span data-ttu-id="ab2df-673">Один символ, за которым следуют восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="ab2df-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="ab2df-674">Одна буква (без учета регистра) или цифра</span><span class="sxs-lookup"><span data-stu-id="ab2df-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="ab2df-675">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-676">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-676">Checksum</span></span>

<span data-ttu-id="ab2df-677">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-678">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-678">Definition</span></span>

<span data-ttu-id="ab2df-679">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-680">Регулярное выражение `Regex_romania_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-681">Найдено ключевое `Keywords_romania_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-682">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-682">Keywords</span></span>

<span data-ttu-id="ab2df-683">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-683"></span></span>
|<span data-ttu-id="ab2df-684">**Кэйвордс_романиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-685">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-685">dl#</span></span>  <br/> <span data-ttu-id="ab2df-686">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-686">driver license</span></span>  <br/> <span data-ttu-id="ab2df-687">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-687">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-688">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-688">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-689">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-689">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-690">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-691">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-692">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-693">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-693">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-694">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-694">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-695">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-695">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-696">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-696">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-697">разрешение de кондуцере</span><span class="sxs-lookup"><span data-stu-id="ab2df-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="ab2df-698">Словакия</span><span class="sxs-lookup"><span data-stu-id="ab2df-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-699">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-699">Format</span></span>

<span data-ttu-id="ab2df-700">Один символ, за которым следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-701">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-701">Pattern</span></span>

<span data-ttu-id="ab2df-702">Один символ, за которым следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="ab2df-703">Одна буква (без учета регистра) или цифра</span><span class="sxs-lookup"><span data-stu-id="ab2df-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="ab2df-704">семь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="ab2df-705">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-705">Checksum</span></span>

<span data-ttu-id="ab2df-706">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-707">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-707">Definition</span></span>

<span data-ttu-id="ab2df-708">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-709">Регулярное выражение `Regex_slovakia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-710">Найдено ключевое `Keywords_slovakia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-711">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-711">Keywords</span></span>

<span data-ttu-id="ab2df-712">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-712"></span></span>
|<span data-ttu-id="ab2df-713">**Кэйвордс_словакиа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-714">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-714">dl#</span></span>  <br/> <span data-ttu-id="ab2df-715">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-715">driver license</span></span>  <br/> <span data-ttu-id="ab2df-716">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-716">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-717">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-717">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-718">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-718">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-719">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-720">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-721">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-722">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-722">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-723">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-723">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-724">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-724">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-725">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-725">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-726">водиčскý преуказ</span><span class="sxs-lookup"><span data-stu-id="ab2df-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="ab2df-727">Словения</span><span class="sxs-lookup"><span data-stu-id="ab2df-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-728">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-728">Format</span></span>

<span data-ttu-id="ab2df-729">Девять цифр без пробелов и разделителей</span><span class="sxs-lookup"><span data-stu-id="ab2df-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-730">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-730">Pattern</span></span>

<span data-ttu-id="ab2df-731">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="ab2df-732">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-732">Checksum</span></span>

<span data-ttu-id="ab2df-733">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-734">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-734">Definition</span></span>

<span data-ttu-id="ab2df-735">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-736">Регулярное выражение `Regex_slovenia_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-737">Найдено ключевое `Keywords_slovenia_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-738">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-738">Keywords</span></span>

<span data-ttu-id="ab2df-739">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-739"></span></span>
|<span data-ttu-id="ab2df-740">**Кэйвордс_словениа_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-741">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-741">dl#</span></span>  <br/> <span data-ttu-id="ab2df-742">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-742">driver license</span></span>  <br/> <span data-ttu-id="ab2df-743">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-743">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-744">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-744">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-745">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-745">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-746">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-747">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-748">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-749">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-749">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-750">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-750">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-751">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-751">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-752">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-752">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-753">возниšко доволженже</span><span class="sxs-lookup"><span data-stu-id="ab2df-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="ab2df-754">Испания</span><span class="sxs-lookup"><span data-stu-id="ab2df-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-755">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-755">Format</span></span>

<span data-ttu-id="ab2df-756">Восемь цифр, за которыми следует один символ</span><span class="sxs-lookup"><span data-stu-id="ab2df-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-757">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-757">Pattern</span></span>

<span data-ttu-id="ab2df-758">Восемь цифр, за которыми следует один символ:</span><span class="sxs-lookup"><span data-stu-id="ab2df-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="ab2df-759">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="ab2df-759">Eight digits</span></span> 
    
- <span data-ttu-id="ab2df-760">Одна цифра или буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="ab2df-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-761">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-761">Checksum</span></span>

<span data-ttu-id="ab2df-762">Да</span><span class="sxs-lookup"><span data-stu-id="ab2df-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-763">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-763">Definition</span></span>

<span data-ttu-id="ab2df-764">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-765">Функция `Func_spain_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-766">Найдено ключевое `Keywords_spain_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="ab2df-767">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-767">Keywords</span></span>

<span data-ttu-id="ab2df-768">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-768"></span></span>
|<span data-ttu-id="ab2df-769">**Кэйвордс_спаин_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-770">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-770">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-771">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-771">dl#</span></span>  <br/> <span data-ttu-id="ab2df-772">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-772">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-773">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-773">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-774">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-774">driver license</span></span>  <br/> <span data-ttu-id="ab2df-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-775">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-776">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-777">driver's licence</span></span>  <br/> <span data-ttu-id="ab2df-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-778">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-779">driving licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-779">driving licence</span></span>  <br/> <span data-ttu-id="ab2df-780">driving license</span><span class="sxs-lookup"><span data-stu-id="ab2df-780">driving license</span></span>  <br/> <span data-ttu-id="ab2df-781">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-781">driver licence number</span></span>  <br/> <span data-ttu-id="ab2df-782">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-782">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-783">драйвер номер лицензии</span><span class="sxs-lookup"><span data-stu-id="ab2df-783">drivers licence number</span></span>  <br/> <span data-ttu-id="ab2df-784">номер лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="ab2df-784">drivers license number</span></span>  <br/> <span data-ttu-id="ab2df-785">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-785">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-786">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-786">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-787">номер водительской лицензии</span><span class="sxs-lookup"><span data-stu-id="ab2df-787">driving licence number</span></span>  <br/> <span data-ttu-id="ab2df-788">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-788">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-789">движущие разрешение</span><span class="sxs-lookup"><span data-stu-id="ab2df-789">driving permit</span></span>  <br/> <span data-ttu-id="ab2df-790">движущие число разрешений</span><span class="sxs-lookup"><span data-stu-id="ab2df-790">driving permit number</span></span>  <br/> <span data-ttu-id="ab2df-791">пермисо de кондукЦиóн</span><span class="sxs-lookup"><span data-stu-id="ab2df-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="ab2df-792">пермисо кондукЦиóн</span><span class="sxs-lookup"><span data-stu-id="ab2df-792">permiso conducción</span></span>  <br/> <span data-ttu-id="ab2df-793">нúмеро лиценЦиа кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="ab2df-794">нúмеро de карнет де кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="ab2df-795">нúмеро карнет кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="ab2df-796">лиценЦиа кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-796">licencia conducir</span></span>  <br/> <span data-ttu-id="ab2df-797">нúмеро de пермисо де кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="ab2df-798">нúмеро де пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="ab2df-799">нúмеро пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="ab2df-800">пермисо кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-800">permiso conducir</span></span>  <br/> <span data-ttu-id="ab2df-801">лиценЦиа de манежо</span><span class="sxs-lookup"><span data-stu-id="ab2df-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="ab2df-802">El карнет de кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="ab2df-803">Карнет кондуЦир</span><span class="sxs-lookup"><span data-stu-id="ab2df-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="ab2df-804">Швеция</span><span class="sxs-lookup"><span data-stu-id="ab2df-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="ab2df-805">Format</span><span class="sxs-lookup"><span data-stu-id="ab2df-805">Format</span></span>

<span data-ttu-id="ab2df-806">Десять цифр, содержащие дефис</span><span class="sxs-lookup"><span data-stu-id="ab2df-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="ab2df-807">Шаблон</span><span class="sxs-lookup"><span data-stu-id="ab2df-807">Pattern</span></span>

<span data-ttu-id="ab2df-808">Десять цифр, содержащих дефис:</span><span class="sxs-lookup"><span data-stu-id="ab2df-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="ab2df-809">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="ab2df-809">Six digits</span></span> 
    
- <span data-ttu-id="ab2df-810">дефис;</span><span class="sxs-lookup"><span data-stu-id="ab2df-810">A hyphen</span></span>
    
- <span data-ttu-id="ab2df-811">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="ab2df-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="ab2df-812">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="ab2df-812">Checksum</span></span>

<span data-ttu-id="ab2df-813">Нет</span><span class="sxs-lookup"><span data-stu-id="ab2df-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="ab2df-814">Определение</span><span class="sxs-lookup"><span data-stu-id="ab2df-814">Definition</span></span>

<span data-ttu-id="ab2df-815">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="ab2df-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="ab2df-816">Регулярное выражение `Regex_sweden_eu_driver's_license_number` находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="ab2df-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="ab2df-817">Найдено ключевое `Keywords_sweden_eu_driver's_license_number` слово FROM.</span><span class="sxs-lookup"><span data-stu-id="ab2df-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="ab2df-818">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="ab2df-818">Keywords</span></span>

<span data-ttu-id="ab2df-819">| |</span><span class="sxs-lookup"><span data-stu-id="ab2df-819"></span></span>
|<span data-ttu-id="ab2df-820">**Кэйвордс_сведен_еу_дривер'с_лиценсе_нумбер**</span><span class="sxs-lookup"><span data-stu-id="ab2df-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="ab2df-821">DL</span><span class="sxs-lookup"><span data-stu-id="ab2df-821">dl#</span></span>  <br/> <span data-ttu-id="ab2df-822">driver license</span><span class="sxs-lookup"><span data-stu-id="ab2df-822">driver license</span></span>  <br/> <span data-ttu-id="ab2df-823">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-823">driver license number</span></span>  <br/> <span data-ttu-id="ab2df-824">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-824">driver licence</span></span>  <br/> <span data-ttu-id="ab2df-825">Drivers лик.</span><span class="sxs-lookup"><span data-stu-id="ab2df-825">drivers lic.</span></span>  <br/> <span data-ttu-id="ab2df-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="ab2df-826">drivers license</span></span>  <br/> <span data-ttu-id="ab2df-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="ab2df-827">drivers licence</span></span>  <br/> <span data-ttu-id="ab2df-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="ab2df-828">driver's license</span></span>  <br/> <span data-ttu-id="ab2df-829">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-829">driver's license number</span></span>  <br/> <span data-ttu-id="ab2df-830">номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="ab2df-830">driver's licence number</span></span>  <br/> <span data-ttu-id="ab2df-831">номер водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="ab2df-831">driving license number</span></span>  <br/> <span data-ttu-id="ab2df-832">длно #</span><span class="sxs-lookup"><span data-stu-id="ab2df-832">dlno#</span></span>  <br/> <span data-ttu-id="ab2df-833">кöркорт</span><span class="sxs-lookup"><span data-stu-id="ab2df-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="ab2df-834">ВОЗМЕЩЕН</span><span class="sxs-lookup"><span data-stu-id="ab2df-834">UK</span></span>

<span data-ttu-id="ab2df-835">Дополнительные сведения см. в разделе "Великобритания</span><span class="sxs-lookup"><span data-stu-id="ab2df-835">For details, see the section "U.K.</span></span> <span data-ttu-id="ab2df-836">Номер водительского удостоверения, в [котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="ab2df-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ab2df-837">См. также</span><span class="sxs-lookup"><span data-stu-id="ab2df-837">See also</span></span>

[<span data-ttu-id="ab2df-838">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="ab2df-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

