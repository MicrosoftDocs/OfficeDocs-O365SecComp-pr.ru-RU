---
title: Номер мобильного телефона ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе описываются тип конфиденциальных данных ЕС номер мобильного телефона.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534752"
---
# <a name="eu-mobile-phone-number"></a><span data-ttu-id="46a7c-104">Номер мобильного телефона ЕС</span><span class="sxs-lookup"><span data-stu-id="46a7c-104">EU Mobile Phone Number</span></span>

<span data-ttu-id="46a7c-p102">Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе описываются тип конфиденциальных данных ЕС номер мобильного телефона.</span><span class="sxs-lookup"><span data-stu-id="46a7c-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU Mobile Phone Number sensitive information type.</span></span> 
  
## <a name="austria"></a><span data-ttu-id="46a7c-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="46a7c-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="46a7c-108">Формат</span><span class="sxs-lookup"><span data-stu-id="46a7c-108">Format</span></span>

<span data-ttu-id="46a7c-109">Цифры без стандартных длины</span><span class="sxs-lookup"><span data-stu-id="46a7c-109">Digits without standard lengths</span></span>
  
### <a name="pattern"></a><span data-ttu-id="46a7c-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-110">Pattern</span></span>

-  <span data-ttu-id="46a7c-111">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-111">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="46a7c-112">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-112">Definition</span></span>

<span data-ttu-id="46a7c-113">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-113">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-114">Регулярное выражение `Regex_austria_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-114">The regular expression  `Regex_austria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-115">Регулярное выражение `Regex_austria_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-115">The regular expression  `Regex_austria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-116">Ключевое слово из `Keywords_austria_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-116">A keyword from  `Keywords_austria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a><span data-ttu-id="46a7c-117">Бельгия</span><span class="sxs-lookup"><span data-stu-id="46a7c-117">Belgium</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-118">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-118">Pattern</span></span>

-  <span data-ttu-id="46a7c-119">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-119">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="46a7c-120">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-120">Definition</span></span>

<span data-ttu-id="46a7c-121">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-122">Регулярное выражение `Regex_belgium_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-122">The regular expression  `Regex_belgium_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-123">Регулярное выражение `Regex_belgium_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-123">The regular expression  `Regex_belgium_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-124">Ключевое слово из `Keywords_belgium_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-124">A keyword from  `Keywords_belgium_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="46a7c-125">Болгария</span><span class="sxs-lookup"><span data-stu-id="46a7c-125">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-126">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-126">Pattern</span></span>

-  <span data-ttu-id="46a7c-127">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-127">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="46a7c-128">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-128">Definition</span></span>

<span data-ttu-id="46a7c-129">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-129">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-130">Регулярное выражение `Regex_bulgaria_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-130">The regular expression  `Regex_bulgaria_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-131">Регулярное выражение `Regex_bulgaria_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-131">The regular expression  `Regex_bulgaria_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-132">Ключевое слово из `Keywords_bulgaria_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-132">A keyword from  `Keywords_bulgaria_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="46a7c-133">Хорватия</span><span class="sxs-lookup"><span data-stu-id="46a7c-133">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-134">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-134">Pattern</span></span>

-  <span data-ttu-id="46a7c-135">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-135">Digits</span></span> 
    
### <a name="definition"></a><span data-ttu-id="46a7c-136">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-136">Definition</span></span>

<span data-ttu-id="46a7c-137">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-138">Регулярное выражение `Regex_croatia_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-138">The regular expression  `Regex_croatia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-139">Регулярное выражение `Regex_croatia_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-139">The regular expression  `Regex_croatia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-140">Ключевое слово из `Keywords_croatia_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-140">A keyword from  `Keywords_croatia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a><span data-ttu-id="46a7c-141">Кипр</span><span class="sxs-lookup"><span data-stu-id="46a7c-141">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-142">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-142">Pattern</span></span>

-  <span data-ttu-id="46a7c-143">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-143">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-144">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-144">Checksum</span></span>

<span data-ttu-id="46a7c-145">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-145">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-146">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-146">Definition</span></span>

<span data-ttu-id="46a7c-147">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-148">Регулярное выражение `Regex_cyprus_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-148">The regular expression  `Regex_cyprus_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-149">Регулярное выражение `Regex_cyprus_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-149">The regular expression  `Regex_cyprus_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-150">Ключевое слово из `Keywords_cyprus_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-150">A keyword from  `Keywords_cyprus_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="46a7c-151">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="46a7c-151">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-152">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-152">Pattern</span></span>

-  <span data-ttu-id="46a7c-153">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-153">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-154">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-154">Checksum</span></span>

<span data-ttu-id="46a7c-155">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-155">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-156">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-156">Definition</span></span>

<span data-ttu-id="46a7c-157">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-157">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-158">Регулярное выражение `Regex_czech_republic_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-158">The regular expression  `Regex_czech_republic_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-159">Регулярное выражение `Regex_czech_republic_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-159">The regular expression  `Regex_czech_republic_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-160">Ключевое слово из `Keywords_czech_republic_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-160">A keyword from  `Keywords_czech_republic_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a><span data-ttu-id="46a7c-161">Дания</span><span class="sxs-lookup"><span data-stu-id="46a7c-161">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-162">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-162">Pattern</span></span>

-  <span data-ttu-id="46a7c-163">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-163">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-164">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-164">Checksum</span></span>

<span data-ttu-id="46a7c-165">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-165">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-166">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-166">Definition</span></span>

<span data-ttu-id="46a7c-167">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-167">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-168">Регулярное выражение `Regex_denmark_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-168">The regular expression  `Regex_denmark_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-169">Регулярное выражение `Regex_denmark_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-169">The regular expression  `Regex_denmark_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-170">Ключевое слово из `Keywords_denmark_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-170">A keyword from  `Keywords_denmark_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a><span data-ttu-id="46a7c-171">Эстония</span><span class="sxs-lookup"><span data-stu-id="46a7c-171">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-172">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-172">Pattern</span></span>

-  <span data-ttu-id="46a7c-173">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-173">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-174">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-174">Checksum</span></span>

<span data-ttu-id="46a7c-175">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-175">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-176">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-176">Definition</span></span>

<span data-ttu-id="46a7c-177">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-177">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-178">Регулярное выражение `Regex_estonia_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-178">The regular expression  `Regex_estonia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-179">Регулярное выражение `Regex_estonia_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-179">The regular expression  `Regex_estonia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-180">Ключевое слово из `Keywords_estonia_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-180">A keyword from  `Keywords_estonia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a><span data-ttu-id="46a7c-181">Финляндия</span><span class="sxs-lookup"><span data-stu-id="46a7c-181">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-182">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-182">Pattern</span></span>

-  <span data-ttu-id="46a7c-183">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-183">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-184">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-184">Checksum</span></span>

<span data-ttu-id="46a7c-185">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-185">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-186">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-186">Definition</span></span>

<span data-ttu-id="46a7c-187">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-187">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-188">Регулярное выражение `Regex_finland_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-188">The regular expression  `Regex_finland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-189">Регулярное выражение `Regex_finland_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-189">The regular expression  `Regex_finland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-190">Ключевое слово из `Keywords_finland_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-190">A keyword from  `Keywords_finland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="46a7c-191">Франция</span><span class="sxs-lookup"><span data-stu-id="46a7c-191">France</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-192">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-192">Pattern</span></span>

-  <span data-ttu-id="46a7c-193">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-193">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-194">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-194">Checksum</span></span>

<span data-ttu-id="46a7c-195">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-195">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-196">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-196">Definition</span></span>

<span data-ttu-id="46a7c-197">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-197">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-198">Регулярное выражение `Regex_france_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-198">The regular expression  `Regex_france_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-199">Регулярное выражение `Regex_france_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-199">The regular expression  `Regex_france_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-200">Ключевое слово из `Keywords_france_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-200">A keyword from  `Keywords_france_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a><span data-ttu-id="46a7c-201">Германия</span><span class="sxs-lookup"><span data-stu-id="46a7c-201">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-202">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-202">Pattern</span></span>

-  <span data-ttu-id="46a7c-203">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-203">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-204">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-204">Checksum</span></span>

<span data-ttu-id="46a7c-205">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-205">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-206">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-206">Definition</span></span>

<span data-ttu-id="46a7c-207">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-207">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-208">Регулярное выражение `Regex_germany_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-208">The regular expression  `Regex_germany_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-209">Регулярное выражение `Regex_germany_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-209">The regular expression  `Regex_germany_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-210">Ключевое слово из `Keywords_germany_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-210">A keyword from  `Keywords_germany_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a><span data-ttu-id="46a7c-211">Греция</span><span class="sxs-lookup"><span data-stu-id="46a7c-211">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-212">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-212">Pattern</span></span>

-  <span data-ttu-id="46a7c-213">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-213">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-214">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-214">Checksum</span></span>

<span data-ttu-id="46a7c-215">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-215">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-216">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-216">Definition</span></span>

<span data-ttu-id="46a7c-217">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-217">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-218">Регулярное выражение `Regex_greece_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-218">The regular expression  `Regex_greece_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-219">Регулярное выражение `Regex_greece_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-219">The regular expression  `Regex_greece_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-220">Ключевое слово из `Keywords_greece_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-220">A keyword from  `Keywords_greece_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a><span data-ttu-id="46a7c-221">Венгрия</span><span class="sxs-lookup"><span data-stu-id="46a7c-221">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-222">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-222">Pattern</span></span>

-  <span data-ttu-id="46a7c-223">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-223">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-224">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-224">Checksum</span></span>

<span data-ttu-id="46a7c-225">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-225">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-226">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-226">Definition</span></span>

<span data-ttu-id="46a7c-227">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-227">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-228">Регулярное выражение `Regex_hungary_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-228">The regular expression  `Regex_hungary_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-229">Регулярное выражение `Regex_hungary_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-229">The regular expression  `Regex_hungary_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-230">Ключевое слово из `Keywords_hungary_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-230">A keyword from  `Keywords_hungary_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a><span data-ttu-id="46a7c-231">Ireland</span><span class="sxs-lookup"><span data-stu-id="46a7c-231">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-232">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-232">Pattern</span></span>

-  <span data-ttu-id="46a7c-233">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-233">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-234">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-234">Checksum</span></span>

<span data-ttu-id="46a7c-235">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-235">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-236">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-236">Definition</span></span>

<span data-ttu-id="46a7c-237">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-237">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-238">Регулярное выражение `Regex_ireland_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-238">The regular expression  `Regex_ireland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-239">Регулярное выражение `Regex_ireland_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-239">The regular expression  `Regex_ireland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-240">Ключевое слово из `Keywords_ireland_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-240">A keyword from  `Keywords_ireland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a><span data-ttu-id="46a7c-241">Италия</span><span class="sxs-lookup"><span data-stu-id="46a7c-241">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-242">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-242">Pattern</span></span>

-  <span data-ttu-id="46a7c-243">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-243">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-244">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-244">Checksum</span></span>

<span data-ttu-id="46a7c-245">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-245">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-246">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-246">Definition</span></span>

<span data-ttu-id="46a7c-247">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-247">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-248">Регулярное выражение `Regex_italy_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-248">The regular expression  `Regex_italy_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-249">Регулярное выражение `Regex_italy_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-249">The regular expression  `Regex_italy_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-250">Ключевое слово из `Keywords_italy_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-250">A keyword from  `Keywords_italy_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a><span data-ttu-id="46a7c-251">Латвия</span><span class="sxs-lookup"><span data-stu-id="46a7c-251">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-252">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-252">Pattern</span></span>

-  <span data-ttu-id="46a7c-253">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-253">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-254">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-254">Checksum</span></span>

<span data-ttu-id="46a7c-255">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-255">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-256">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-256">Definition</span></span>

<span data-ttu-id="46a7c-257">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-257">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-258">Регулярное выражение `Regex_latvia_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-258">The regular expression  `Regex_latvia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-259">Регулярное выражение `Regex_latvia_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-259">The regular expression  `Regex_latvia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-260">Ключевое слово из `Keywords_latvia_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-260">A keyword from  `Keywords_latvia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a><span data-ttu-id="46a7c-261">Литва</span><span class="sxs-lookup"><span data-stu-id="46a7c-261">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-262">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-262">Pattern</span></span>

-  <span data-ttu-id="46a7c-263">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-263">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-264">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-264">Checksum</span></span>

<span data-ttu-id="46a7c-265">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-265">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-266">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-266">Definition</span></span>

<span data-ttu-id="46a7c-267">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-267">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-268">Регулярное выражение `Regex_lithuania_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-268">The regular expression  `Regex_lithuania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-269">Регулярное выражение `Regex_lithuania_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-269">The regular expression  `Regex_lithuania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-270">Ключевое слово из `Keywords_lithuania_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-270">A keyword from  `Keywords_lithuania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="46a7c-271">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="46a7c-271">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-272">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-272">Pattern</span></span>

-  <span data-ttu-id="46a7c-273">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-273">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-274">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-274">Checksum</span></span>

<span data-ttu-id="46a7c-275">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-275">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-276">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-276">Definition</span></span>

<span data-ttu-id="46a7c-277">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-277">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-278">Регулярное выражение `Regex_luxumburg_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-278">The regular expression  `Regex_luxumburg_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-279">Регулярное выражение `Regex_luxumburg_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-279">The regular expression  `Regex_luxumburg_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-280">Ключевое слово из `Keywords_luxumburg_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-280">A keyword from  `Keywords_luxumburg_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="46a7c-281">Мальта</span><span class="sxs-lookup"><span data-stu-id="46a7c-281">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-282">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-282">Pattern</span></span>

-  <span data-ttu-id="46a7c-283">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-283">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-284">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-284">Checksum</span></span>

<span data-ttu-id="46a7c-285">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-285">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-286">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-286">Definition</span></span>

<span data-ttu-id="46a7c-287">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-288">Регулярное выражение `Regex_malta_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-288">The regular expression  `Regex_malta_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-289">Регулярное выражение `Regex_malta_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-289">The regular expression  `Regex_malta_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-290">Ключевое слово из `Keywords_malta_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-290">A keyword from  `Keywords_malta_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="46a7c-291">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="46a7c-291">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-292">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-292">Pattern</span></span>

-  <span data-ttu-id="46a7c-293">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-293">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-294">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-294">Checksum</span></span>

<span data-ttu-id="46a7c-295">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-295">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-296">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-296">Definition</span></span>

<span data-ttu-id="46a7c-297">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-297">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-298">Регулярное выражение `Regex_netherlands_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-298">The regular expression  `Regex_netherlands_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-299">Регулярное выражение `Regex_netherlands_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-299">The regular expression  `Regex_netherlands_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-300">Ключевое слово из `Keywords_netherlands_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-300">A keyword from  `Keywords_netherlands_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="46a7c-301">Польша</span><span class="sxs-lookup"><span data-stu-id="46a7c-301">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-302">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-302">Pattern</span></span>

-  <span data-ttu-id="46a7c-303">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-303">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-304">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-304">Checksum</span></span>

<span data-ttu-id="46a7c-305">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-305">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-306">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-306">Definition</span></span>

<span data-ttu-id="46a7c-307">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-308">Регулярное выражение `Regex_poland_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-308">The regular expression  `Regex_poland_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-309">Регулярное выражение `Regex_poland_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-309">The regular expression  `Regex_poland_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-310">Ключевое слово из `Keywords_poland_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-310">A keyword from  `Keywords_poland_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="46a7c-311">Португалия</span><span class="sxs-lookup"><span data-stu-id="46a7c-311">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-312">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-312">Pattern</span></span>

-  <span data-ttu-id="46a7c-313">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-313">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-314">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-314">Checksum</span></span>

<span data-ttu-id="46a7c-315">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-315">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-316">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-316">Definition</span></span>

<span data-ttu-id="46a7c-317">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-317">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-318">Регулярное выражение `Regex_portugal_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-318">The regular expression  `Regex_portugal_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-319">Регулярное выражение `Regex_portugal_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-319">The regular expression  `Regex_portugal_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-320">Ключевое слово из `Keywords_portugal_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-320">A keyword from  `Keywords_portugal_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a><span data-ttu-id="46a7c-321">Румыния</span><span class="sxs-lookup"><span data-stu-id="46a7c-321">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-322">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-322">Pattern</span></span>

-  <span data-ttu-id="46a7c-323">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-323">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-324">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-324">Checksum</span></span>

<span data-ttu-id="46a7c-325">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-325">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-326">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-326">Definition</span></span>

<span data-ttu-id="46a7c-327">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-327">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-328">Регулярное выражение `Regex_romania_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-328">The regular expression  `Regex_romania_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-329">Регулярное выражение `Regex_romania_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-329">The regular expression  `Regex_romania_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-330">Ключевое слово из `Keywords_romania_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-330">A keyword from  `Keywords_romania_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="46a7c-331">Словакия</span><span class="sxs-lookup"><span data-stu-id="46a7c-331">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-332">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-332">Pattern</span></span>

-  <span data-ttu-id="46a7c-333">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-333">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-334">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-334">Checksum</span></span>

<span data-ttu-id="46a7c-335">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-335">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-336">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-336">Definition</span></span>

<span data-ttu-id="46a7c-337">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-337">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-338">Регулярное выражение `Regex_slovakia_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-338">The regular expression  `Regex_slovakia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-339">Регулярное выражение `Regex_slovakia_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-339">The regular expression  `Regex_slovakia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-340">Ключевое слово из `Keywords_slovakia_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-340">A keyword from  `Keywords_slovakia_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="46a7c-341">Словения</span><span class="sxs-lookup"><span data-stu-id="46a7c-341">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-342">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-342">Pattern</span></span>

-  <span data-ttu-id="46a7c-343">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-343">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-344">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-344">Checksum</span></span>

<span data-ttu-id="46a7c-345">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-345">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-346">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-346">Definition</span></span>

<span data-ttu-id="46a7c-347">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-347">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-348">Регулярное выражение `Regex_slovenia_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-348">The regular expression  `Regex_slovenia_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-349">Регулярное выражение `Regex_slovenia_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-349">The regular expression  `Regex_slovenia_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-350">Ключевое слово из `Keywords_slovenia_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-350">A keyword from  `Keywords_slovenia_eu_mobile_number` is found.</span></span> 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a><span data-ttu-id="46a7c-351">Испания</span><span class="sxs-lookup"><span data-stu-id="46a7c-351">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-352">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-352">Pattern</span></span>

-  <span data-ttu-id="46a7c-353">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-353">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-354">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-354">Checksum</span></span>

<span data-ttu-id="46a7c-355">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-355">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-356">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-356">Definition</span></span>

<span data-ttu-id="46a7c-357">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-357">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-358">Регулярное выражение `Regex_spain_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-358">The regular expression  `Regex_spain_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-359">Регулярное выражение `Regex_spain_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-359">The regular expression  `Regex_spain_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-360">Ключевое слово из `Keywords_spain_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-360">A keyword from  `Keywords_spain_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a><span data-ttu-id="46a7c-361">Швеция</span><span class="sxs-lookup"><span data-stu-id="46a7c-361">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-362">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-362">Pattern</span></span>

-  <span data-ttu-id="46a7c-363">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-363">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-364">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-364">Checksum</span></span>

<span data-ttu-id="46a7c-365">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-365">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-366">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-366">Definition</span></span>

<span data-ttu-id="46a7c-367">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-367">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-368">Регулярное выражение `Regex_sweden_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-368">The regular expression  `Regex_sweden_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-369">Регулярное выражение `Regex_sweden_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-369">The regular expression  `Regex_sweden_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-370">Ключевое слово из `Keywords_sweden_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-370">A keyword from  `Keywords_sweden_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a><span data-ttu-id="46a7c-371">(ВЕЛИКОБРИТАНИЯ)</span><span class="sxs-lookup"><span data-stu-id="46a7c-371">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="46a7c-372">Шаблон</span><span class="sxs-lookup"><span data-stu-id="46a7c-372">Pattern</span></span>

-  <span data-ttu-id="46a7c-373">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="46a7c-373">Digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="46a7c-374">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="46a7c-374">Checksum</span></span>

<span data-ttu-id="46a7c-375">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="46a7c-375">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="46a7c-376">Определение</span><span class="sxs-lookup"><span data-stu-id="46a7c-376">Definition</span></span>

<span data-ttu-id="46a7c-377">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="46a7c-377">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="46a7c-378">Регулярное выражение `Regex_uk_eu_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-378">The regular expression  `Regex_uk_eu_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-379">Регулярное выражение `Regex_uk_eu_formatted_mobile_number` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="46a7c-379">The regular expression  `Regex_uk_eu_formatted_mobile_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="46a7c-380">Ключевое слово из `Keywords_uk_eu_mobile_number` найден.</span><span class="sxs-lookup"><span data-stu-id="46a7c-380">A keyword from  `Keywords_uk_eu_mobile_number` is found.</span></span> 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="46a7c-381">См. также</span><span class="sxs-lookup"><span data-stu-id="46a7c-381">See also</span></span>

[<span data-ttu-id="46a7c-382">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="46a7c-382">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

