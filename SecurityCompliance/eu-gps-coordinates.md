---
title: Координаты GPS ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/14/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: fdf2aebc-d5a4-4138-b10f-4a81dd70415a
description: Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе описываются координаты GPS ЕС тип конфиденциальных данных.
ms.openlocfilehash: 89fb8420e479b9f793fc2be9aa3a9a9fd5741691
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534765"
---
# <a name="eu-gps-coordinates"></a><span data-ttu-id="1358f-104">Координаты GPS ЕС</span><span class="sxs-lookup"><span data-stu-id="1358f-104">EU GPS Coordinates</span></span>

<span data-ttu-id="1358f-p102">Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе описываются координаты GPS ЕС тип конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="1358f-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU GPS Coordinates sensitive information type.</span></span>
  
## <a name="austria"></a><span data-ttu-id="1358f-107">Австрия</span><span class="sxs-lookup"><span data-stu-id="1358f-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="1358f-108">Формат</span><span class="sxs-lookup"><span data-stu-id="1358f-108">Format</span></span>

<span data-ttu-id="1358f-109">Координаты для городов в Австрия — в диапазоне: широта из 46.526 48.816 и долгота из 9,6 для 16.945.</span><span class="sxs-lookup"><span data-stu-id="1358f-109">Coordinates for cities in Austria are in range: Latitude from 46.526 to 48.816 and longitude from 9.6 to 16.945.</span></span>
  
### <a name="pattern"></a><span data-ttu-id="1358f-110">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-110">Pattern</span></span>

<span data-ttu-id="1358f-111">Для каждого координат, сочетание до 6 цифр и десятичной запятой.</span><span class="sxs-lookup"><span data-stu-id="1358f-111">For each coordinate, combination of up to 6 digits and a decimal point.</span></span>
  
- <span data-ttu-id="1358f-112">До 6 символов</span><span class="sxs-lookup"><span data-stu-id="1358f-112">Up to 6 digits</span></span>
    
- <span data-ttu-id="1358f-113">Десятичный разделитель после первого или второго цифры.</span><span class="sxs-lookup"><span data-stu-id="1358f-113">A decimal point after first or second digit.</span></span>
    
### <a name="checksum"></a><span data-ttu-id="1358f-114">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-114">Checksum</span></span>

<span data-ttu-id="1358f-115">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-116">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-116">Definition</span></span>

<span data-ttu-id="1358f-117">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-118">Регулярное выражение `Regex_austria_eu_gps_data_1` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-118">The regular expression  `Regex_austria_eu_gps_data_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="1358f-119">Ключевое слово из `Keywords_austria_eu_gps_data` найден.</span><span class="sxs-lookup"><span data-stu-id="1358f-119">A keyword from  `Keywords_austria_eu_gps_data` is found.</span></span> 
    
<span data-ttu-id="1358f-120">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-120">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-121">Регулярное выражение `Regex_austria_eu_gps_data_1` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-121">The regular expression  `Regex_austria_eu_gps_data_1` finds content that matches the pattern.</span></span> 
    
<span data-ttu-id="1358f-122">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-122">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-123">Регулярное выражение `Regex_austria_eu_gps_data_2` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-123">The regular expression  `Regex_austria_eu_gps_data_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="1358f-124">Ключевое слово из `Keywords_austria_eu_gps_data` найден.</span><span class="sxs-lookup"><span data-stu-id="1358f-124">A keyword from  `Keywords_austria_eu_gps_data` is found.</span></span> 
    
<span data-ttu-id="1358f-125">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-125">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-126">Регулярное выражение `Regex_austria_eu_gps_data_2` находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-126">The regular expression  `Regex_austria_eu_gps_data_2` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_gps_data_1" />
          <Match idRef="Keywords_austria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_austria_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_gps_data_2" />
          <Match idRef="Keywords_austria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_austria_eu_gps_data_2" />
        </Pattern>

```

### <a name="keywords"></a><span data-ttu-id="1358f-127">Keywords</span><span class="sxs-lookup"><span data-stu-id="1358f-127">Keywords</span></span>

#### <a name="keywordsaustriaeugpsdata"></a><span data-ttu-id="1358f-128">Keywords_austria_eu_gps_data</span><span class="sxs-lookup"><span data-stu-id="1358f-128">Keywords_austria_eu_gps_data</span></span>

<span data-ttu-id="1358f-129">средство отслеживания GPS</span><span class="sxs-lookup"><span data-stu-id="1358f-129">gps tracker</span></span>
  
<span data-ttu-id="1358f-130">GPS-координаты</span><span class="sxs-lookup"><span data-stu-id="1358f-130">gps coordinates</span></span>
  
<span data-ttu-id="1358f-131">расположение</span><span class="sxs-lookup"><span data-stu-id="1358f-131">location</span></span>
  
<span data-ttu-id="1358f-132">карта</span><span class="sxs-lookup"><span data-stu-id="1358f-132">map</span></span>
  
<span data-ttu-id="1358f-133">Широта</span><span class="sxs-lookup"><span data-stu-id="1358f-133">latitude</span></span>
  
<span data-ttu-id="1358f-134">Долгота</span><span class="sxs-lookup"><span data-stu-id="1358f-134">longitude</span></span>
  
<span data-ttu-id="1358f-135">Средство отслеживания GPS</span><span class="sxs-lookup"><span data-stu-id="1358f-135">GPS-Tracker</span></span>
  
<span data-ttu-id="1358f-136">GPS-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="1358f-136">GPS-Koordinaten</span></span>
  
<span data-ttu-id="1358f-137">Standort Karte</span><span class="sxs-lookup"><span data-stu-id="1358f-137">Standort Karte</span></span>
  
<span data-ttu-id="1358f-138">Breitengrad</span><span class="sxs-lookup"><span data-stu-id="1358f-138">Breitengrad</span></span>
  
<span data-ttu-id="1358f-139">Längengrad</span><span class="sxs-lookup"><span data-stu-id="1358f-139">Längengrad</span></span>
  
## <a name="belgium"></a><span data-ttu-id="1358f-140">Бельгия</span><span class="sxs-lookup"><span data-stu-id="1358f-140">Belgium</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-141">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-141">Pattern</span></span>

-  <span data-ttu-id="1358f-142">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-142">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-143">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-143">Checksum</span></span>

<span data-ttu-id="1358f-144">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-145">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-145">Definition</span></span>

<span data-ttu-id="1358f-146">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-147">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-147">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-148">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-148">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75>">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_gps_data_1" />
          <Match idRef="Keywords_belgium_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
          <Match idRef="Keywords_belgium_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="1358f-149">Болгария</span><span class="sxs-lookup"><span data-stu-id="1358f-149">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-150">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-150">Pattern</span></span>

-  <span data-ttu-id="1358f-151">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-151">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-152">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-152">Checksum</span></span>

<span data-ttu-id="1358f-153">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-153">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-154">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-154">Definition</span></span>

<span data-ttu-id="1358f-155">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-155">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-156">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-156">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-157">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-157">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75>
</Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_1" />
          <Match idRef="Keywords_bulgaria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_2" />
          <Match idRef="Keywords_bulgaria_eu_gps_data" />
        </Pattern>
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="1358f-158">Хорватия</span><span class="sxs-lookup"><span data-stu-id="1358f-158">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-159">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-159">Pattern</span></span>

-  <span data-ttu-id="1358f-160">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-160">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-161">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-161">Checksum</span></span>

<span data-ttu-id="1358f-162">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-162">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-163">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-163">Definition</span></span>

<span data-ttu-id="1358f-164">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-164">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-165">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-165">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-166">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-166">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_gps_data_1" />
          <Match idRef="Keywords_croatia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_croatia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_gps_data_2" />
          <Match idRef="Keywords_croatia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_croatia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="cyprus"></a><span data-ttu-id="1358f-167">Кипр</span><span class="sxs-lookup"><span data-stu-id="1358f-167">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-168">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-168">Pattern</span></span>

-  <span data-ttu-id="1358f-169">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-169">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-170">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-170">Checksum</span></span>

<span data-ttu-id="1358f-171">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-171">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-172">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-172">Definition</span></span>

<span data-ttu-id="1358f-173">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-173">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-174">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-174">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-175">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-175">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_1" />
          <Match idRef="Keywords_cyprus_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_2" />
          <Match idRef="Keywords_cyprus_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="1358f-176">Чешская Республика</span><span class="sxs-lookup"><span data-stu-id="1358f-176">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-177">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-177">Pattern</span></span>

-  <span data-ttu-id="1358f-178">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-178">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-179">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-179">Checksum</span></span>

<span data-ttu-id="1358f-180">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-180">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-181">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-181">Definition</span></span>

<span data-ttu-id="1358f-182">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-182">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
<span data-ttu-id="1358f-183">Политика защиты от потери данных — это % уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости символов:</span><span class="sxs-lookup"><span data-stu-id="1358f-183">A DLP policy is % confident that it's detected this type of sensitive information if, within a proximity of characters:</span></span>
  
- <span data-ttu-id="1358f-184">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-184">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-185">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-185">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_1" />
          <Match idRef="Keywords_czech_republic_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_2" />
          <Match idRef="Keywords_czech_republic_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="denmark"></a><span data-ttu-id="1358f-186">Дания</span><span class="sxs-lookup"><span data-stu-id="1358f-186">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-187">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-187">Pattern</span></span>

-  <span data-ttu-id="1358f-188">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-188">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-189">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-189">Checksum</span></span>

<span data-ttu-id="1358f-190">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-190">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-191">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-191">Definition</span></span>

<span data-ttu-id="1358f-192">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-192">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-193">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-193">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-194">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-194">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_gps_data_1" />
          <Match idRef="Keywords_denmark_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_denmark_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_gps_data_2" />
          <Match idRef="Keywords_denmark_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_denmark_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="estonia"></a><span data-ttu-id="1358f-195">Эстония</span><span class="sxs-lookup"><span data-stu-id="1358f-195">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-196">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-196">Pattern</span></span>

-  <span data-ttu-id="1358f-197">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-197">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-198">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-198">Checksum</span></span>

<span data-ttu-id="1358f-199">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-199">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-200">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-200">Definition</span></span>

<span data-ttu-id="1358f-201">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-202">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-202">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-203">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-203">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_gps_data_1" />
          <Match idRef="Keywords_estonia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_estonia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_gps_data_2" />
          <Match idRef="Keywords_estonia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_estonia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="finland"></a><span data-ttu-id="1358f-204">Финляндия</span><span class="sxs-lookup"><span data-stu-id="1358f-204">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-205">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-205">Pattern</span></span>

-  <span data-ttu-id="1358f-206">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-206">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-207">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-207">Checksum</span></span>

<span data-ttu-id="1358f-208">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-208">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-209">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-209">Definition</span></span>

<span data-ttu-id="1358f-210">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-210">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-211">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-211">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-212">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-212">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_gps_data_1" />
          <Match idRef="Keywords_finland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_finland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_gps_data_2" />
          <Match idRef="Keywords_finland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_finland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="1358f-213">Франция</span><span class="sxs-lookup"><span data-stu-id="1358f-213">France</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-214">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-214">Pattern</span></span>

-  <span data-ttu-id="1358f-215">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-215">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-216">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-216">Checksum</span></span>

<span data-ttu-id="1358f-217">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-217">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-218">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-218">Definition</span></span>

<span data-ttu-id="1358f-219">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-219">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-220">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-220">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-221">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-221">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_gps_data_1" />
          <Match idRef="Keywords_france_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_france_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_gps_data_2" />
          <Match idRef="Keywords_france_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_france_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="germany"></a><span data-ttu-id="1358f-222">Германия</span><span class="sxs-lookup"><span data-stu-id="1358f-222">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-223">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-223">Pattern</span></span>

-  <span data-ttu-id="1358f-224">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-224">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-225">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-225">Checksum</span></span>

<span data-ttu-id="1358f-226">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-226">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-227">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-227">Definition</span></span>

<span data-ttu-id="1358f-228">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-228">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-229">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-229">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-230">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-230">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_gps_data_1" />
          <Match idRef="Keywords_germany_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_germany_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_gps_data_2" />
          <Match idRef="Keywords_germany_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_germany_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="greece"></a><span data-ttu-id="1358f-231">Греция</span><span class="sxs-lookup"><span data-stu-id="1358f-231">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-232">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-232">Pattern</span></span>

-  <span data-ttu-id="1358f-233">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-233">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-234">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-234">Checksum</span></span>

<span data-ttu-id="1358f-235">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-235">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-236">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-236">Definition</span></span>

<span data-ttu-id="1358f-237">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-237">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-238">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-238">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-239">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-239">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_gps_data_1" />
          <Match idRef="Keywords_greece_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_greece_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_gps_data_2" />
          <Match idRef="Keywords_greece_eu_gps_data" />
        </Pattern>
</Entity>
```

## <a name="hungary"></a><span data-ttu-id="1358f-240">Венгрия</span><span class="sxs-lookup"><span data-stu-id="1358f-240">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-241">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-241">Pattern</span></span>

-  <span data-ttu-id="1358f-242">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-242">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-243">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-243">Checksum</span></span>

<span data-ttu-id="1358f-244">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-244">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-245">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-245">Definition</span></span>

<span data-ttu-id="1358f-246">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-247">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-247">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-248">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-248">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_gps_data_1" />
          <Match idRef="Keywords_hungary_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_hungary_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_gps_data_2" />
          <Match idRef="Keywords_hungary_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_hungary_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="ireland"></a><span data-ttu-id="1358f-249">Ireland</span><span class="sxs-lookup"><span data-stu-id="1358f-249">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-250">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-250">Pattern</span></span>

-  <span data-ttu-id="1358f-251">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-251">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-252">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-252">Checksum</span></span>

<span data-ttu-id="1358f-253">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-253">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-254">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-254">Definition</span></span>

<span data-ttu-id="1358f-255">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-255">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-256">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-256">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-257">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-257">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_gps_data_1" />
          <Match idRef="Keywords_ireland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_ireland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_gps_data_2" />
          <Match idRef="Keywords_ireland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_ireland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="italy"></a><span data-ttu-id="1358f-258">Италия</span><span class="sxs-lookup"><span data-stu-id="1358f-258">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-259">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-259">Pattern</span></span>

-  <span data-ttu-id="1358f-260">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-260">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-261">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-261">Checksum</span></span>

<span data-ttu-id="1358f-262">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-262">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-263">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-263">Definition</span></span>

<span data-ttu-id="1358f-264">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-264">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-265">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-265">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-266">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-266">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_gps_data_1" />
          <Match idRef="Keywords_italy_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_italy_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_gps_data_2" />
          <Match idRef="Keywords_italy_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_italy_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="latvia"></a><span data-ttu-id="1358f-267">Латвия</span><span class="sxs-lookup"><span data-stu-id="1358f-267">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-268">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-268">Pattern</span></span>

-  <span data-ttu-id="1358f-269">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-269">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-270">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-270">Checksum</span></span>

<span data-ttu-id="1358f-271">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-271">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-272">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-272">Definition</span></span>

<span data-ttu-id="1358f-273">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-273">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-274">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-274">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-275">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-275">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_gps_data_1" />
          <Match idRef="Keywords_latvia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_latvia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_gps_data_2" />
          <Match idRef="Keywords_latvia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_latvia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="lithuania"></a><span data-ttu-id="1358f-276">Литва</span><span class="sxs-lookup"><span data-stu-id="1358f-276">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-277">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-277">Pattern</span></span>

-  <span data-ttu-id="1358f-278">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-278">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-279">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-279">Checksum</span></span>

<span data-ttu-id="1358f-280">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-280">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-281">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-281">Definition</span></span>

<span data-ttu-id="1358f-282">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-283">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-283">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-284">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-284">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_1" />
          <Match idRef="Keywords_lithuania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_2" />
          <Match idRef="Keywords_lithuania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="1358f-285">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="1358f-285">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-286">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-286">Pattern</span></span>

-  <span data-ttu-id="1358f-287">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-287">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-288">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-288">Checksum</span></span>

<span data-ttu-id="1358f-289">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-289">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-290">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-290">Definition</span></span>

<span data-ttu-id="1358f-291">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-291">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-292">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-292">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-293">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-293">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_1" />
          <Match idRef="Keywords_luxemburg_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_2" />
          <Match idRef="Keywords_luxemburg_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="1358f-294">Мальта</span><span class="sxs-lookup"><span data-stu-id="1358f-294">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-295">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-295">Pattern</span></span>

-  <span data-ttu-id="1358f-296">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-296">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-297">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-297">Checksum</span></span>

<span data-ttu-id="1358f-298">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-298">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-299">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-299">Definition</span></span>

<span data-ttu-id="1358f-300">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-301">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-301">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-302">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-302">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_gps_data_1" />
          <Match idRef="Keywords_malta_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_gps_data_2" />
          <Match idRef="Keywords_malta_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="1358f-303">Нидерланды</span><span class="sxs-lookup"><span data-stu-id="1358f-303">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-304">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-304">Pattern</span></span>

-  <span data-ttu-id="1358f-305">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-305">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-306">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-306">Checksum</span></span>

<span data-ttu-id="1358f-307">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-307">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-308">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-308">Definition</span></span>

<span data-ttu-id="1358f-309">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-309">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-310">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-310">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-311">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-311">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_1" />
          <Match idRef="Keywords_netherlands_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_2" />
          <Match idRef="Keywords_netherlands_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="1358f-312">Польша</span><span class="sxs-lookup"><span data-stu-id="1358f-312">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-313">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-313">Pattern</span></span>

-  <span data-ttu-id="1358f-314">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-314">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-315">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-315">Checksum</span></span>

<span data-ttu-id="1358f-316">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-316">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-317">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-317">Definition</span></span>

<span data-ttu-id="1358f-318">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-318">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-319">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-319">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-320">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-320">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_gps_data_1" />
          <Match idRef="Keywords_poland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_poland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_gps_data_2" />
          <Match idRef="Keywords_poland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_poland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="1358f-321">Португалия</span><span class="sxs-lookup"><span data-stu-id="1358f-321">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-322">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-322">Pattern</span></span>

-  <span data-ttu-id="1358f-323">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-323">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-324">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-324">Checksum</span></span>

<span data-ttu-id="1358f-325">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-325">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-326">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-326">Definition</span></span>

<span data-ttu-id="1358f-327">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-327">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-328">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-328">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-329">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-329">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_gps_data_1" />
          <Match idRef="Keywords_portugal_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_portugal_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_gps_data_2" />
          <Match idRef="Keywords_portugal_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_portugal_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="romania"></a><span data-ttu-id="1358f-330">Румыния</span><span class="sxs-lookup"><span data-stu-id="1358f-330">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-331">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-331">Pattern</span></span>

-  <span data-ttu-id="1358f-332">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-332">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-333">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-333">Checksum</span></span>

<span data-ttu-id="1358f-334">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-334">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-335">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-335">Definition</span></span>

<span data-ttu-id="1358f-336">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-336">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-337">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-337">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-338">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-338">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_gps_data_1" />
          <Match idRef="Keywords_romania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_romania_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_gps_data_2" />
          <Match idRef="Keywords_romania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_romania_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="1358f-339">Словакия</span><span class="sxs-lookup"><span data-stu-id="1358f-339">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-340">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-340">Pattern</span></span>

-  <span data-ttu-id="1358f-341">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-341">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-342">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-342">Checksum</span></span>

<span data-ttu-id="1358f-343">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-343">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-344">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-344">Definition</span></span>

<span data-ttu-id="1358f-345">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-345">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-346">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-346">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-347">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-347">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_1" />
          <Match idRef="Keywords_slovakia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_2" />
          <Match idRef="Keywords_slovakia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="1358f-348">Словения</span><span class="sxs-lookup"><span data-stu-id="1358f-348">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-349">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-349">Pattern</span></span>

-  <span data-ttu-id="1358f-350">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-350">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-351">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-351">Checksum</span></span>

<span data-ttu-id="1358f-352">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-352">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-353">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-353">Definition</span></span>

<span data-ttu-id="1358f-354">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-354">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-355">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-355">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-356">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-356">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_1" />
          <Match idRef="Keywords_slovenia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_2" />
          <Match idRef="Keywords_slovenia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="spain"></a><span data-ttu-id="1358f-357">Испания</span><span class="sxs-lookup"><span data-stu-id="1358f-357">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-358">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-358">Pattern</span></span>

-  <span data-ttu-id="1358f-359">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-359">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-360">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-360">Checksum</span></span>

<span data-ttu-id="1358f-361">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-361">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-362">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-362">Definition</span></span>

<span data-ttu-id="1358f-363">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-364">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-364">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-365">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-365">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_gps_data_1" />
          <Match idRef="Keywords_spain_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_spain_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_gps_data_2" />
          <Match idRef="Keywords_spain_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_spain_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="sweden"></a><span data-ttu-id="1358f-366">Швеция</span><span class="sxs-lookup"><span data-stu-id="1358f-366">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-367">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-367">Pattern</span></span>

-  <span data-ttu-id="1358f-368">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-368">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-369">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-369">Checksum</span></span>

<span data-ttu-id="1358f-370">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-370">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-371">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-371">Definition</span></span>

<span data-ttu-id="1358f-372">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-372">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-373">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-373">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-374">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-374">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_gps_data_1" />
          <Match idRef="Keywords_sweden_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_sweden_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_gps_data_2" />
          <Match idRef="Keywords_sweden_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_sweden_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="uk"></a><span data-ttu-id="1358f-375">(ВЕЛИКОБРИТАНИЯ)</span><span class="sxs-lookup"><span data-stu-id="1358f-375">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="1358f-376">Шаблон</span><span class="sxs-lookup"><span data-stu-id="1358f-376">Pattern</span></span>

-  <span data-ttu-id="1358f-377">Количество цифр</span><span class="sxs-lookup"><span data-stu-id="1358f-377">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="1358f-378">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="1358f-378">Checksum</span></span>

<span data-ttu-id="1358f-379">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="1358f-379">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="1358f-380">Определение</span><span class="sxs-lookup"><span data-stu-id="1358f-380">Definition</span></span>

<span data-ttu-id="1358f-381">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="1358f-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="1358f-382">Регулярное выражение находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="1358f-382">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="1358f-383">Ключевое слово из найти.</span><span class="sxs-lookup"><span data-stu-id="1358f-383">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_gps_data_1" />
          <Match idRef="Keywords_uk_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_uk_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_gps_data_2" />
          <Match idRef="Keywords_uk_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_uk_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="1358f-384">См. также</span><span class="sxs-lookup"><span data-stu-id="1358f-384">See also</span></span>

[<span data-ttu-id="1358f-385">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="1358f-385">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

