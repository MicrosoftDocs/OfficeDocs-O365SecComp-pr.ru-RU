---
title: Номер телефона ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1c90ca41-1681-46bf-8ad6-6bf4cec5c426
description: Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе описываются тип номера телефона ЕС конфиденциальных данных.
ms.openlocfilehash: 9dd878e3385312982f9f3a4927205e3ebb27aabb
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534920"
---
# <a name="eu-phone-number"></a><span data-ttu-id="76450-104">Номер телефона ЕС</span><span class="sxs-lookup"><span data-stu-id="76450-104">EU Phone Number</span></span>

<span data-ttu-id="76450-p102">Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе описываются тип номера телефона ЕС конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="76450-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="76450-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="76450-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="76450-108">Формат</span><span class="sxs-lookup"><span data-stu-id="76450-108">Format</span></span>

<span data-ttu-id="76450-109">Стандартная длина не</span><span class="sxs-lookup"><span data-stu-id="76450-109">No standard length</span></span>
  
### <a name="pattern"></a><span data-ttu-id="76450-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-110">Pattern</span></span>

- <span data-ttu-id="76450-111">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-111">Digits</span></span> 
    
- <span data-ttu-id="76450-112">Только номера мобильного телефона начинаются с цифры «6»</span><span class="sxs-lookup"><span data-stu-id="76450-112">Only mobile phone numbers begin with the digit "6"</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-113">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-113">Checksum</span></span>

<span data-ttu-id="76450-114">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-114">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-115">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-115">Definition</span></span>

<span data-ttu-id="76450-116">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-117">Регулярное выражение `Regex_austria_eu_telephone_number_1` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-117">The regular expression  `Regex_austria_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-118">Ключевое слово из `Keywords_austria_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-118">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-119">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-119">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-120">Регулярное выражение `Regex_austria_eu_telephone_number_2` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-120">The regular expression  `Regex_austria_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-121">Ключевое слово из `Keywords_austria_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-121">A keyword from  `Keywords_austria_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_1" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_telephone_number_2" />
          <Match idRef="Keywords_austria_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_austria_eu_formatted_telephone_number_2" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="76450-122">Бельгия</span><span class="sxs-lookup"><span data-stu-id="76450-122">Belgium</span></span>

### <a name="definition"></a><span data-ttu-id="76450-123">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-123">Definition</span></span>

<span data-ttu-id="76450-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-125">Регулярное выражение `Regex_belgium_eu_telephone_number_1` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-125">The regular expression  `Regex_belgium_eu_telephone_number_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-126">Ключевое слово из `Keywords_belgium_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-126">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-127">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-127">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-128">Регулярное выражение `Regex_belgium_eu_telephone_number_2` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-128">The regular expression  `Regex_belgium_eu_telephone_number_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-129">Ключевое слово из `Keywords_belgium_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-129">A keyword from  `Keywords_belgium_eu_telephone_number` is found.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_1" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_telephone_number_2" />
          <Match idRef="Keywords_belgium_eu_telephone_number" />
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_1" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_belgium_eu_formatted_telephone_number_2" />
          </Pattern></Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="76450-130">Болгария</span><span class="sxs-lookup"><span data-stu-id="76450-130">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-131">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-131">Pattern</span></span>

- <span data-ttu-id="76450-132">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-132">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-133">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-133">Checksum</span></span>

<span data-ttu-id="76450-134">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-134">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-135">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-135">Definition</span></span>

<span data-ttu-id="76450-136">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-137">Регулярное выражение `Regex_bulgaria_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-137">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-138">Ключевое слово из `Keywords_bulgaria_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-138">A keyword from  `Keywords_bulgaria_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-139">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-139">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-140">Регулярное выражение `Regex_bulgaria_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-140">The regular expression  `Regex_bulgaria_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_telephone_number" />
          <Match idRef="Keywords_bulgaria_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_bulgaria_eu_formatted_telephone_number" />
          </Pattern>
          
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="76450-141">Хорватия</span><span class="sxs-lookup"><span data-stu-id="76450-141">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-142">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-142">Pattern</span></span>

- <span data-ttu-id="76450-143">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-144">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-144">Checksum</span></span>

<span data-ttu-id="76450-145">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-146">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-146">Definition</span></span>

<span data-ttu-id="76450-147">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-148">Регулярное выражение `Regex_croatia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-148">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-149">Ключевое слово из `Keywords_croatia_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-149">A keyword from  `Keywords_croatia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-150">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-150">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-151">Регулярное выражение `Regex_croatia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-151">The regular expression  `Regex_croatia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_telephone_number" />
          <Match idRef="Keywords_croatia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_croatia_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="cyprus"></a><span data-ttu-id="76450-152">Кипр</span><span class="sxs-lookup"><span data-stu-id="76450-152">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-153">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-153">Pattern</span></span>

- <span data-ttu-id="76450-154">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-154">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-155">Checksum</span></span>

<span data-ttu-id="76450-156">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-156">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-157">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-157">Definition</span></span>

<span data-ttu-id="76450-158">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-159">Регулярное выражение `Regex_cyprus_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-159">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-160">Ключевое слово из `Keywords_cyprus_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-160">A keyword from  `Keywords_cyprus_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-161">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-161">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-162">Регулярное выражение `Regex_cyprus_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-162">The regular expression  `Regex_cyprus_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_telephone_number" />
          <Match idRef="Keywords_cyprus_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_cyprus_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="76450-163">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="76450-163">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-164">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-164">Pattern</span></span>

- <span data-ttu-id="76450-165">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-165">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-166">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-166">Checksum</span></span>

<span data-ttu-id="76450-167">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-167">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-168">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-168">Definition</span></span>

<span data-ttu-id="76450-169">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-169">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-170">Регулярное выражение `Regex_czech_republic_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-170">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-171">Ключевое слово из `Keywords_czech_republic_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-171">A keyword from  `Keywords_czech_republic_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-172">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-172">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-173">Регулярное выражение `Regex_czech_republic_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-173">The regular expression  `Regex_czech_republic_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_telephone_number" />
          <Match idRef="Keywords_czech_republic_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_czech_republic_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="denmark"></a><span data-ttu-id="76450-174">Дания</span><span class="sxs-lookup"><span data-stu-id="76450-174">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-175">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-175">Pattern</span></span>

- <span data-ttu-id="76450-176">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-176">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-177">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-177">Checksum</span></span>

<span data-ttu-id="76450-178">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-178">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-179">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-179">Definition</span></span>

<span data-ttu-id="76450-180">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-180">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-181">Регулярное выражение `Regex_denmark_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-181">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-182">Ключевое слово из `Keywords_denmark_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-182">A keyword from  `Keywords_denmark_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-183">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-183">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-184">Регулярное выражение `Regex_denmark_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-184">The regular expression  `Regex_denmark_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_telephone_number" />
          <Match idRef="Keywords_denmark_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_denmark_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="estonia"></a><span data-ttu-id="76450-185">Эстония</span><span class="sxs-lookup"><span data-stu-id="76450-185">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-186">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-186">Pattern</span></span>

- <span data-ttu-id="76450-187">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-187">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-188">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-188">Checksum</span></span>

<span data-ttu-id="76450-189">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-189">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-190">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-190">Definition</span></span>

<span data-ttu-id="76450-191">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-191">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-192">Регулярное выражение `Regex_estonia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-192">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-193">Ключевое слово из `Keywords_estonia_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-193">A keyword from  `Keywords_estonia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-194">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-195">Регулярное выражение `Regex_estonia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-195">The regular expression  `Regex_estonia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_telephone_number" />
          <Match idRef="Keywords_estonia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_estonia_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="finland"></a><span data-ttu-id="76450-196">Финляндия</span><span class="sxs-lookup"><span data-stu-id="76450-196">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-197">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-197">Pattern</span></span>

- <span data-ttu-id="76450-198">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-198">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-199">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-199">Checksum</span></span>

<span data-ttu-id="76450-200">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-200">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-201">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-201">Definition</span></span>

<span data-ttu-id="76450-202">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-203">Регулярное выражение `Regex_finland_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-203">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-204">Ключевое слово из `Keywords_finland_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-204">A keyword from  `Keywords_finland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-205">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-205">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-206">Регулярное выражение `Regex_finland_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-206">The regular expression  `Regex_finland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_telephone_number" />
          <Match idRef="Keywords_finland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_finland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="76450-207">Франция</span><span class="sxs-lookup"><span data-stu-id="76450-207">France</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-208">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-208">Pattern</span></span>

- <span data-ttu-id="76450-209">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-209">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-210">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-210">Checksum</span></span>

<span data-ttu-id="76450-211">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-211">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-212">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-212">Definition</span></span>

<span data-ttu-id="76450-213">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-213">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-214">Регулярное выражение `Regex_france_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-214">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-215">Ключевое слово из `Keywords_france_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-215">A keyword from  `Keywords_france_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-216">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-216">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-217">Регулярное выражение `Regex_france_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-217">The regular expression  `Regex_france_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_telephone_number" />
          <Match idRef="Keywords_france_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_france_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="germany"></a><span data-ttu-id="76450-218">Германия</span><span class="sxs-lookup"><span data-stu-id="76450-218">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-219">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-219">Pattern</span></span>

- <span data-ttu-id="76450-220">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-220">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-221">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-221">Checksum</span></span>

<span data-ttu-id="76450-222">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-222">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-223">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-223">Definition</span></span>

<span data-ttu-id="76450-224">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-224">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-225">Регулярное выражение `Regex_germany_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-225">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-226">Ключевое слово из `Keywords_germany_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-226">A keyword from  `Keywords_germany_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-227">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-228">Регулярное выражение `Regex_germany_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-228">The regular expression  `Regex_germany_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_telephone_number" />
          <Match idRef="Keywords_germany_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_germany_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="greece"></a><span data-ttu-id="76450-229">Греция</span><span class="sxs-lookup"><span data-stu-id="76450-229">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-230">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-230">Pattern</span></span>

- <span data-ttu-id="76450-231">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-231">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-232">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-232">Checksum</span></span>

<span data-ttu-id="76450-233">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-233">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-234">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-234">Definition</span></span>

<span data-ttu-id="76450-235">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-235">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-236">Регулярное выражение `Regex_greece_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-236">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-237">Ключевое слово из `Keywords_greece_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-237">A keyword from  `Keywords_greece_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-238">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-238">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-239">Регулярное выражение `Regex_greece_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-239">The regular expression  `Regex_greece_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_telephone_number" />
          <Match idRef="Keywords_greece_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_greece_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="hungary"></a><span data-ttu-id="76450-240">Венгрия</span><span class="sxs-lookup"><span data-stu-id="76450-240">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-241">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-241">Pattern</span></span>

- <span data-ttu-id="76450-242">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-242">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-243">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-243">Checksum</span></span>

<span data-ttu-id="76450-244">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-244">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-245">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-245">Definition</span></span>

<span data-ttu-id="76450-246">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-247">Регулярное выражение `Regex_hungary_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-247">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-248">Ключевое слово из `Keywords_hungary_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-248">A keyword from  `Keywords_hungary_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-249">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-250">Регулярное выражение `Regex_hungary_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-250">The regular expression  `Regex_hungary_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_telephone_number" />
          <Match idRef="Keywords_hungary_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_hungary_eu_formatted_telephone_number" />
          </Pattern>
       </Entity>
```

## <a name="ireland"></a><span data-ttu-id="76450-251">Ireland</span><span class="sxs-lookup"><span data-stu-id="76450-251">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-252">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-252">Pattern</span></span>

- <span data-ttu-id="76450-253">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-254">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-254">Checksum</span></span>

<span data-ttu-id="76450-255">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-256">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-256">Definition</span></span>

<span data-ttu-id="76450-257">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-258">Регулярное выражение `Regex_ireland_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-258">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-259">Ключевое слово из `Keywords_ireland_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-259">A keyword from  `Keywords_ireland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-260">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-261">Регулярное выражение `Regex_ireland_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-261">The regular expression  `Regex_ireland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_telephone_number" />
          <Match idRef="Keywords_ireland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_ireland_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="italy"></a><span data-ttu-id="76450-262">Италия</span><span class="sxs-lookup"><span data-stu-id="76450-262">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-263">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-263">Pattern</span></span>

- <span data-ttu-id="76450-264">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-264">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-265">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-265">Checksum</span></span>

<span data-ttu-id="76450-266">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-266">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-267">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-267">Definition</span></span>

<span data-ttu-id="76450-268">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-268">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-269">Регулярное выражение `Regex_italy_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-269">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-270">Ключевое слово из `Keywords_italy_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-270">A keyword from  `Keywords_italy_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-271">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-272">Регулярное выражение `Regex_italy_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-272">The regular expression  `Regex_italy_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_telephone_number" />
          <Match idRef="Keywords_italy_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_italy_eu_formatted_telephone_number" />
          </Pattern>
         </Entity>
```

## <a name="latvia"></a><span data-ttu-id="76450-273">Латвия</span><span class="sxs-lookup"><span data-stu-id="76450-273">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-274">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-274">Pattern</span></span>

- <span data-ttu-id="76450-275">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-275">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-276">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-276">Checksum</span></span>

<span data-ttu-id="76450-277">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-277">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-278">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-278">Definition</span></span>

<span data-ttu-id="76450-279">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-279">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-280">Регулярное выражение `Regex_latvia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-280">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-281">Ключевое слово из `Keywords_latvia_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-281">A keyword from  `Keywords_latvia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-282">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-283">Регулярное выражение `Regex_latvia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-283">The regular expression  `Regex_latvia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_telephone_number" />
          <Match idRef="Keywords_latvia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_latvia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="lithuania"></a><span data-ttu-id="76450-284">Литва</span><span class="sxs-lookup"><span data-stu-id="76450-284">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-285">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-285">Pattern</span></span>

- <span data-ttu-id="76450-286">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-286">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-287">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-287">Checksum</span></span>

<span data-ttu-id="76450-288">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-288">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-289">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-289">Definition</span></span>

<span data-ttu-id="76450-290">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-291">Регулярное выражение `Regex_lithuania_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-291">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-292">Ключевое слово из `Keywords_lithuania_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-292">A keyword from  `Keywords_lithuania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-293">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-293">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-294">Регулярное выражение `Regex_lithuania_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-294">The regular expression  `Regex_lithuania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_telephone_number" />
          <Match idRef="Keywords_lithuania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_lithuania_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="76450-295">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="76450-295">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-296">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-296">Pattern</span></span>

- <span data-ttu-id="76450-297">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-297">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-298">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-298">Checksum</span></span>

<span data-ttu-id="76450-299">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-299">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-300">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-300">Definition</span></span>

<span data-ttu-id="76450-301">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-302">Регулярное выражение `Regex_luxemburg_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-302">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-303">Ключевое слово из `Keywords_luxemburg_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-303">A keyword from  `Keywords_luxemburg_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-304">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-304">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-305">Регулярное выражение `Regex_luxemburg_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-305">The regular expression  `Regex_luxemburg_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_telephone_number" />
          <Match idRef="Keywords_luxemburg_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_luxemburg_eu_formatted_telephone_number" />
                  </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="76450-306">Мальта</span><span class="sxs-lookup"><span data-stu-id="76450-306">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-307">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-307">Pattern</span></span>

- <span data-ttu-id="76450-308">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-308">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-309">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-309">Checksum</span></span>

<span data-ttu-id="76450-310">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-310">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-311">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-311">Definition</span></span>

<span data-ttu-id="76450-312">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-313">Регулярное выражение `Regex_malta_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-313">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-314">Ключевое слово из `Keywords_malta_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-314">A keyword from  `Keywords_malta_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-315">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-315">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-316">Регулярное выражение `Regex_malta_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-316">The regular expression  `Regex_malta_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_telephone_number" />
          <Match idRef="Keywords_malta_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_malta_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="76450-317">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="76450-317">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-318">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-318">Pattern</span></span>

- <span data-ttu-id="76450-319">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-319">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-320">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-320">Checksum</span></span>

<span data-ttu-id="76450-321">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-321">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-322">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-322">Definition</span></span>

<span data-ttu-id="76450-323">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-323">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-324">Регулярное выражение `Regex_netherlands_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-324">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-325">Ключевое слово из `Keywords_netherlands_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-325">A keyword from  `Keywords_netherlands_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-326">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-327">Регулярное выражение `Regex_netherlands_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-327">The regular expression  `Regex_netherlands_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_telephone_number" />
          <Match idRef="Keywords_netherlands_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_netherlands_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="76450-328">Польша</span><span class="sxs-lookup"><span data-stu-id="76450-328">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-329">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-329">Pattern</span></span>

- <span data-ttu-id="76450-330">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-330">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-331">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-331">Checksum</span></span>

<span data-ttu-id="76450-332">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-332">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-333">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-333">Definition</span></span>

<span data-ttu-id="76450-334">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-334">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-335">Регулярное выражение `Regex_poland_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-335">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-336">Ключевое слово из `Keywords_poland_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-336">A keyword from  `Keywords_poland_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-337">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-338">Регулярное выражение `Regex_poland_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-338">The regular expression  `Regex_poland_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_telephone_number" />
          <Match idRef="Keywords_poland_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_poland_eu_formatted_telephone_number" />
             </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="76450-339">Португалия</span><span class="sxs-lookup"><span data-stu-id="76450-339">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-340">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-340">Pattern</span></span>

- <span data-ttu-id="76450-341">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-341">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-342">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-342">Checksum</span></span>

<span data-ttu-id="76450-343">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-343">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-344">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-344">Definition</span></span>

<span data-ttu-id="76450-345">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-345">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-346">Регулярное выражение `Regex_portugal_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-346">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-347">Ключевое слово из `Keywords_portugal_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-347">A keyword from  `Keywords_portugal_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-348">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-348">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-349">Регулярное выражение `Regex_portugal_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-349">The regular expression  `Regex_portugal_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_telephone_number" />
          <Match idRef="Keywords_portugal_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_portugal_eu_formatted_telephone_number" />
          </Pattern>
        </Entity>
```

## <a name="romania"></a><span data-ttu-id="76450-350">Румыния</span><span class="sxs-lookup"><span data-stu-id="76450-350">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-351">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-351">Pattern</span></span>

- <span data-ttu-id="76450-352">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-352">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-353">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-353">Checksum</span></span>

<span data-ttu-id="76450-354">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-354">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-355">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-355">Definition</span></span>

<span data-ttu-id="76450-356">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-356">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-357">Регулярное выражение `Regex_romania_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-357">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-358">Ключевое слово из `Keywords_romania_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-358">A keyword from  `Keywords_romania_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-359">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-359">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-360">Регулярное выражение `Regex_romania_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-360">The regular expression  `Regex_romania_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_telephone_number" />
          <Match idRef="Keywords_romania_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_romania_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="76450-361">Словакия</span><span class="sxs-lookup"><span data-stu-id="76450-361">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-362">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-362">Pattern</span></span>

- <span data-ttu-id="76450-363">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-364">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-364">Checksum</span></span>

<span data-ttu-id="76450-365">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-366">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-366">Definition</span></span>

<span data-ttu-id="76450-367">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-368">Регулярное выражение `Regex_slovakia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-368">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-369">Ключевое слово из `Keywords_slovakia_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-369">A keyword from  `Keywords_slovakia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-370">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-370">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-371">Регулярное выражение `Regex_slovakia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-371">The regular expression  `Regex_slovakia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_telephone_number" />
          <Match idRef="Keywords_slovakia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovakia_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="76450-372">Словения</span><span class="sxs-lookup"><span data-stu-id="76450-372">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-373">Pattern</span></span>

- <span data-ttu-id="76450-374">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-374">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-375">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-375">Checksum</span></span>

<span data-ttu-id="76450-376">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-377">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-377">Definition</span></span>

<span data-ttu-id="76450-378">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-379">Регулярное выражение `Regex_slovenia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-379">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-380">Ключевое слово из `Keywords_slovenia_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-380">A keyword from  `Keywords_slovenia_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-381">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-382">Регулярное выражение `Regex_slovenia_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-382">The regular expression  `Regex_slovenia_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_telephone_number" />
          <Match idRef="Keywords_slovenia_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_slovenia_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="spain"></a><span data-ttu-id="76450-383">Испания</span><span class="sxs-lookup"><span data-stu-id="76450-383">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-384">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-384">Pattern</span></span>

- <span data-ttu-id="76450-385">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-385">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-386">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-386">Checksum</span></span>

<span data-ttu-id="76450-387">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-387">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-388">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-388">Definition</span></span>

<span data-ttu-id="76450-389">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-390">Регулярное выражение `Regex_spain_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-390">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-391">Ключевое слово из `Keywords_spain_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-391">A keyword from  `Keywords_spain_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-392">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-392">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-393">Регулярное выражение `Regex_spain_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-393">The regular expression  `Regex_spain_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_telephone_number" />
          <Match idRef="Keywords_spain_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_spain_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="sweden"></a><span data-ttu-id="76450-394">Швеция</span><span class="sxs-lookup"><span data-stu-id="76450-394">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-395">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-395">Pattern</span></span>

- <span data-ttu-id="76450-396">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-396">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-397">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-397">Checksum</span></span>

<span data-ttu-id="76450-398">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-398">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-399">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-399">Definition</span></span>

<span data-ttu-id="76450-400">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-400">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-401">Регулярное выражение `Regex_sweden_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-401">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-402">Ключевое слово из `Keywords_sweden_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-402">A keyword from  `Keywords_sweden_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-403">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-404">Регулярное выражение `Regex_sweden_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-404">The regular expression  `Regex_sweden_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_telephone_number" />
          <Match idRef="Keywords_sweden_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_sweden_eu_formatted_telephone_number" />
          </Pattern>
          </Entity>
```

## <a name="uk"></a><span data-ttu-id="76450-405">(ВЕЛИКОБРИТАНИЯ)</span><span class="sxs-lookup"><span data-stu-id="76450-405">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="76450-406">Шаблон</span><span class="sxs-lookup"><span data-stu-id="76450-406">Pattern</span></span>

- <span data-ttu-id="76450-407">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="76450-407">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="76450-408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="76450-408">Checksum</span></span>

<span data-ttu-id="76450-409">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="76450-409">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="76450-410">Определение</span><span class="sxs-lookup"><span data-stu-id="76450-410">Definition</span></span>

<span data-ttu-id="76450-411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-412">Регулярное выражение `Regex_uk_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-412">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="76450-413">Ключевое слово из `Keywords_uk_eu_telephone_number` найден.</span><span class="sxs-lookup"><span data-stu-id="76450-413">A keyword from  `Keywords_uk_eu_telephone_number` is found.</span></span> 
    
<span data-ttu-id="76450-414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="76450-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="76450-415">Регулярное выражение `Regex_uk_eu_telephone_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="76450-415">The regular expression  `Regex_uk_eu_telephone_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Telephone Number -->
<Entity id="eb367e90-d826-40aa-a338-a1fdb3a4d99b" patternsProximity="300" recommendedConfidence="75">
<!-- Loosely formatted patterns with mandatory corroborative evidence -->
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_telephone_number" />
          <Match idRef="Keywords_uk_eu_telephone_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
          <Pattern confidenceLevel="75">
            <IdMatch idRef="Regex_uk_eu_formatted_telephone_number" />
            </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="76450-416">См. также</span><span class="sxs-lookup"><span data-stu-id="76450-416">See also</span></span>

[<span data-ttu-id="76450-417">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="76450-417">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

