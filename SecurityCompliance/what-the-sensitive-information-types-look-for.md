---
title: Что позволяют искать типы конфиденциальной информации
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает в себя 80 типы конфиденциальной информации, готовые к использованию в политиках защиты от потери данных. В этом разделе перечислены все эти типы конфиденциальной информации и показывает, что политики защиты от потери данных выполняет поиск при обнаружении каждого типа.
ms.openlocfilehash: 4b083f80e02c80053b63ee897b2515a4505c16d9
ms.sourcegitcommit: 8c5a88433cff23c59b436260808cf3d91b06fdef
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/07/2018
ms.locfileid: "27194740"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="0b6c6-104">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="0b6c6-104">What the sensitive information types look for</span></span>

<span data-ttu-id="0b6c6-p102">Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе перечислены все эти типы конфиденциальной информации и показывает, что политики защиты от потери данных выполняет поиск при обнаружении каждого типа. Тип конфиденциальных данных определяется шаблон, который можно определить по регулярных выражений или функции. Кроме того подтверждающее свидетельств, таких как ключевые слова и контрольные можно использовать для определения типов конфиденциальной информации. Уровень надежности и близость также используются в процессе оценки.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="0b6c6-110">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="0b6c6-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-111">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-111">Format</span></span>

<span data-ttu-id="0b6c6-112">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-113">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-113">Pattern</span></span>

<span data-ttu-id="0b6c6-114">С форматированием</span><span class="sxs-lookup"><span data-stu-id="0b6c6-114">Formatted:</span></span>
- <span data-ttu-id="0b6c6-115">четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="0b6c6-116">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-116">A hyphen</span></span>
- <span data-ttu-id="0b6c6-117">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-117">Four digits</span></span>
- <span data-ttu-id="0b6c6-118">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-118">A hyphen</span></span>
- <span data-ttu-id="0b6c6-119">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="0b6c6-119">A digit</span></span>

<span data-ttu-id="0b6c6-120">Неформатированный: 9 последовательных цифр Приступая к работе с 0, 1, 2, 3, 6, 7 или 8</span><span class="sxs-lookup"><span data-stu-id="0b6c6-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="0b6c6-121">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-121">Checksum</span></span>

<span data-ttu-id="0b6c6-122">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-123">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-123">Definition</span></span>

<span data-ttu-id="0b6c6-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-125">функция Func_aba_routing находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-126">находится ключевое слово из Keyword_ABA_Routing.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="0b6c6-127">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="0b6c6-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="0b6c6-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="0b6c6-129">aba</span><span class="sxs-lookup"><span data-stu-id="0b6c6-129">aba</span></span>
- <span data-ttu-id="0b6c6-130">
aba#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-130">aba #</span></span>
- <span data-ttu-id="0b6c6-131">
aba routing #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-131">aba routing #</span></span>
- <span data-ttu-id="0b6c6-132">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="0b6c6-132">aba routing number</span></span>
- <span data-ttu-id="0b6c6-133">
aba#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-133">aba#</span></span>
- <span data-ttu-id="0b6c6-134">
abarouting#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-134">abarouting#</span></span>
- <span data-ttu-id="0b6c6-135">
aba number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-135">aba number</span></span>
- <span data-ttu-id="0b6c6-136">
abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="0b6c6-136">abaroutingnumber</span></span>
- <span data-ttu-id="0b6c6-137">
american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-137">american bank association routing #</span></span>
- <span data-ttu-id="0b6c6-138">
american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-138">american bank association routing number</span></span>
- <span data-ttu-id="0b6c6-139">
americanbankassociationrouting#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="0b6c6-140">
americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="0b6c6-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="0b6c6-141">
bank routing number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-141">bank routing number</span></span>
- <span data-ttu-id="0b6c6-142">
bankrouting#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-142">bankrouting#</span></span>
- <span data-ttu-id="0b6c6-143">
bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="0b6c6-143">bankroutingnumber</span></span>
- <span data-ttu-id="0b6c6-144">
routing transit number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-144">routing transit number</span></span>
- <span data-ttu-id="0b6c6-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="0b6c6-146">Номер внутреннего удостоверения личности для Аргентины (DNI)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-147">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-147">Format</span></span>

<span data-ttu-id="0b6c6-148">Восемь цифр, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-149">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-149">Pattern</span></span>

<span data-ttu-id="0b6c6-150">Восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-150">Eight digits:</span></span>
- <span data-ttu-id="0b6c6-151">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-151">Two digits</span></span>
- <span data-ttu-id="0b6c6-152">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-152">A period</span></span>
- <span data-ttu-id="0b6c6-153">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-153">Three digits</span></span>
- <span data-ttu-id="0b6c6-154">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-154">A period</span></span>
- <span data-ttu-id="0b6c6-155">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-156">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-156">Checksum</span></span>

<span data-ttu-id="0b6c6-157">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-158">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-158">Definition</span></span>

<span data-ttu-id="0b6c6-159">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-160">регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-161">находится ключевое слово из Keyword_argentina_national_id.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="0b6c6-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="0b6c6-164">Argentina National Identity number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="0b6c6-165">Идентификация</span><span class="sxs-lookup"><span data-stu-id="0b6c6-165">Identity</span></span> 
- <span data-ttu-id="0b6c6-166">Идентификация национальной идентификационной карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="0b6c6-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-167">DNI</span></span> 
- <span data-ttu-id="0b6c6-168">Сетевой Адаптер национальный реестра лиц</span><span class="sxs-lookup"><span data-stu-id="0b6c6-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="0b6c6-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="0b6c6-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="0b6c6-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-171">Identidad</span></span> 
- <span data-ttu-id="0b6c6-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="0b6c6-173">Номер банковского счета для Австралии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-174">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-174">Format</span></span>

<span data-ttu-id="0b6c6-175">6–10 цифр с номером филиала банка в штате или без него.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-176">Pattern</span></span>

<span data-ttu-id="0b6c6-p103">Номер учетной записи — 6 до 10 цифр. Номер филиала банка Австралия состояний:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="0b6c6-179">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-179">Three digits</span></span> 
- <span data-ttu-id="0b6c6-180">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-180">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-181">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-182">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-182">Checksum</span></span>

<span data-ttu-id="0b6c6-183">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-184">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-184">Definition</span></span>

<span data-ttu-id="0b6c6-185">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-186">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="0b6c6-187">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="0b6c6-188">регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="0b6c6-189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-190">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="0b6c6-191">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```
<!-- Australia Bank Account Number -->
<Entity id="74a54de9-2a30-4aa0-a8aa-3d9327fc07c7" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
        <Match idRef="Regex_australia_bank_account_number_bsb" />
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_bank_account_number" />
        <Match idRef="Keyword_australia_bank_account_number" />
  </Pattern>
 </Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="0b6c6-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="0b6c6-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="0b6c6-194">swift bank code</span></span>
- <span data-ttu-id="0b6c6-195">
correspondent bank</span><span class="sxs-lookup"><span data-stu-id="0b6c6-195">correspondent bank</span></span>
- <span data-ttu-id="0b6c6-196">
base currency</span><span class="sxs-lookup"><span data-stu-id="0b6c6-196">base currency</span></span>
- <span data-ttu-id="0b6c6-197">
usa account</span><span class="sxs-lookup"><span data-stu-id="0b6c6-197">usa account</span></span>
- <span data-ttu-id="0b6c6-198">
holder address</span><span class="sxs-lookup"><span data-stu-id="0b6c6-198">holder address</span></span>
- <span data-ttu-id="0b6c6-199">
bank address</span><span class="sxs-lookup"><span data-stu-id="0b6c6-199">bank address</span></span>
- <span data-ttu-id="0b6c6-200">
information account</span><span class="sxs-lookup"><span data-stu-id="0b6c6-200">information account</span></span>
- <span data-ttu-id="0b6c6-201">
fund transfers</span><span class="sxs-lookup"><span data-stu-id="0b6c6-201">fund transfers</span></span>
- <span data-ttu-id="0b6c6-202">
bank charges</span><span class="sxs-lookup"><span data-stu-id="0b6c6-202">bank charges</span></span>
- <span data-ttu-id="0b6c6-203">
bank details</span><span class="sxs-lookup"><span data-stu-id="0b6c6-203">bank details</span></span>
- <span data-ttu-id="0b6c6-204">
banking information</span><span class="sxs-lookup"><span data-stu-id="0b6c6-204">banking information</span></span>
- <span data-ttu-id="0b6c6-205">
full names</span><span class="sxs-lookup"><span data-stu-id="0b6c6-205">full names</span></span>
- <span data-ttu-id="0b6c6-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="0b6c6-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="0b6c6-207">Номер водительского удостоверения для Австралии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-208">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-208">Format</span></span>

<span data-ttu-id="0b6c6-209">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-210">Pattern</span></span>

<span data-ttu-id="0b6c6-211">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="0b6c6-212">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-213">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-213">Two digits</span></span> 
- <span data-ttu-id="0b6c6-214">пять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="0b6c6-215">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="0b6c6-215">OR</span></span>

- <span data-ttu-id="0b6c6-216">1–2 дополнительные буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-217">4–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-217">4-9 digits</span></span>

<span data-ttu-id="0b6c6-218">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="0b6c6-218">OR</span></span>

- <span data-ttu-id="0b6c6-219">девять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-220">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-220">Checksum</span></span>

<span data-ttu-id="0b6c6-221">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-222">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-222">Definition</span></span>

<span data-ttu-id="0b6c6-223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-224">регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-225">находится ключевое слово из Keyword_australia_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="0b6c6-226">ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```
<!-- Australia Drivers License Number -->
<Entity id="1cbbc8f5-9216-4392-9eb5-5ac2298d1356" patternsProximity="300" recommendedConfidence="75">
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_drivers_license_number" />
        <Match idRef="Keyword_australia_drivers_license_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_australia_drivers_license_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="0b6c6-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="0b6c6-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="0b6c6-229">international driving permits</span></span>
- <span data-ttu-id="0b6c6-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="0b6c6-230">australian automobile association</span></span>
- <span data-ttu-id="0b6c6-231">
international driving permit</span><span class="sxs-lookup"><span data-stu-id="0b6c6-231">international driving permit</span></span>
- <span data-ttu-id="0b6c6-232">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-232">DriverLicence</span></span>
- <span data-ttu-id="0b6c6-233">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-233">DriverLicences</span></span>
- <span data-ttu-id="0b6c6-234">Драйвер Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-234">Driver Lic</span></span>
- <span data-ttu-id="0b6c6-235">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-235">Driver Licence</span></span>
- <span data-ttu-id="0b6c6-236">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-236">Driver Licences</span></span>
- <span data-ttu-id="0b6c6-237">DriversLic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-237">DriversLic</span></span>
- <span data-ttu-id="0b6c6-238">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-238">DriversLicence</span></span>
- <span data-ttu-id="0b6c6-239">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-239">DriversLicences</span></span>
- <span data-ttu-id="0b6c6-240">Драйверы Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-240">Drivers Lic</span></span>
- <span data-ttu-id="0b6c6-241">Драйверы Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-241">Drivers Lics</span></span>
- <span data-ttu-id="0b6c6-242">Лицензия драйверы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-242">Drivers Licence</span></span>
- <span data-ttu-id="0b6c6-243">Число лицензий на драйверы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-243">Drivers Licences</span></span>
- <span data-ttu-id="0b6c6-244">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-244">Driver'Lic</span></span>
- <span data-ttu-id="0b6c6-245">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-245">Driver'Lics</span></span>
- <span data-ttu-id="0b6c6-246">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-246">Driver'Licence</span></span>
- <span data-ttu-id="0b6c6-247">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-247">Driver'Licences</span></span>
- <span data-ttu-id="0b6c6-248">Драйвер ' Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-248">Driver' Lic</span></span>
- <span data-ttu-id="0b6c6-249">Драйвер ' Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-249">Driver' Lics</span></span>
- <span data-ttu-id="0b6c6-250">Драйвер "лицензия</span><span class="sxs-lookup"><span data-stu-id="0b6c6-250">Driver' Licence</span></span>
- <span data-ttu-id="0b6c6-251">Драйвер "число лицензий на по</span><span class="sxs-lookup"><span data-stu-id="0b6c6-251">Driver' Licences</span></span>
- <span data-ttu-id="0b6c6-252">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-252">Driver'sLic</span></span>
- <span data-ttu-id="0b6c6-253">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-253">Driver'sLics</span></span>
- <span data-ttu-id="0b6c6-254">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-254">Driver'sLicence</span></span>
- <span data-ttu-id="0b6c6-255">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-255">Driver'sLicences</span></span>
- <span data-ttu-id="0b6c6-256">Lic драйвера</span><span class="sxs-lookup"><span data-stu-id="0b6c6-256">Driver's Lic</span></span>
- <span data-ttu-id="0b6c6-257">Lics драйвера</span><span class="sxs-lookup"><span data-stu-id="0b6c6-257">Driver's Lics</span></span>
- <span data-ttu-id="0b6c6-258">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-258">Driver's Licence</span></span>
- <span data-ttu-id="0b6c6-259">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-259">Driver's Licences</span></span>
- <span data-ttu-id="0b6c6-260">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-260">DriverLic#</span></span>
- <span data-ttu-id="0b6c6-261">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-261">DriverLics#</span></span>
- <span data-ttu-id="0b6c6-262">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-262">DriverLicence#</span></span>
- <span data-ttu-id="0b6c6-263">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-263">DriverLicences#</span></span>
- <span data-ttu-id="0b6c6-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-264">Driver Lic#</span></span>
- <span data-ttu-id="0b6c6-265">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-265">Driver Lics#</span></span>
- <span data-ttu-id="0b6c6-266">Драйвер лицензия #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-266">Driver Licence#</span></span>
- <span data-ttu-id="0b6c6-267">Драйвер число лицензий на #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-267">Driver Licences#</span></span>
- <span data-ttu-id="0b6c6-268">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-268">DriversLic#</span></span>
- <span data-ttu-id="0b6c6-269">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-269">DriversLics#</span></span>
- <span data-ttu-id="0b6c6-270">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-270">DriversLicence#</span></span>
- <span data-ttu-id="0b6c6-271">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-271">DriversLicences#</span></span>
- <span data-ttu-id="0b6c6-272">Драйверы Lic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-272">Drivers Lic#</span></span>
- <span data-ttu-id="0b6c6-273">Драйверы Lics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-273">Drivers Lics#</span></span>
- <span data-ttu-id="0b6c6-274">Драйверы лицензия #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-274">Drivers Licence#</span></span>
- <span data-ttu-id="0b6c6-275">Число лицензий на драйверы #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-275">Drivers Licences#</span></span>
- <span data-ttu-id="0b6c6-276">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-276">Driver'Lic#</span></span>
- <span data-ttu-id="0b6c6-277">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-277">Driver'Lics#</span></span>
- <span data-ttu-id="0b6c6-278">Driver' Licence#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-278">Driver'Licence#</span></span>
- <span data-ttu-id="0b6c6-279">Driver' Licences#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-279">Driver'Licences#</span></span>
- <span data-ttu-id="0b6c6-280">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-280">Driver' Lic#</span></span>
- <span data-ttu-id="0b6c6-281">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-281">Driver' Lics#</span></span>
- <span data-ttu-id="0b6c6-282">Драйвер "лицензия #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-282">Driver' Licence#</span></span>
- <span data-ttu-id="0b6c6-283">Драйвер "число лицензий на #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-283">Driver' Licences#</span></span>
- <span data-ttu-id="0b6c6-284">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-284">Driver'sLic#</span></span>
- <span data-ttu-id="0b6c6-285">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-285">Driver'sLics#</span></span>
- <span data-ttu-id="0b6c6-286">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-286">Driver'sLicence#</span></span>
- <span data-ttu-id="0b6c6-287">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-287">Driver'sLicences#</span></span>
- <span data-ttu-id="0b6c6-288">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-288">Driver's Lic#</span></span>
- <span data-ttu-id="0b6c6-289">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-289">Driver's Lics#</span></span>
- <span data-ttu-id="0b6c6-290">Лицензия водительского #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-290">Driver's Licence#</span></span>
- <span data-ttu-id="0b6c6-291">Число лицензий на водительского #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="0b6c6-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="0b6c6-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="0b6c6-293">aaa</span><span class="sxs-lookup"><span data-stu-id="0b6c6-293">aaa</span></span>
- <span data-ttu-id="0b6c6-294">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-294">DriverLicense</span></span>
- <span data-ttu-id="0b6c6-295">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-295">DriverLicenses</span></span>
- <span data-ttu-id="0b6c6-296">Драйвер лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-296">Driver License</span></span>
- <span data-ttu-id="0b6c6-297">Драйвер лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-297">Driver Licenses</span></span>
- <span data-ttu-id="0b6c6-298">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-298">DriversLicense</span></span>
- <span data-ttu-id="0b6c6-299">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-299">DriversLicenses</span></span>
- <span data-ttu-id="0b6c6-300">Драйверы лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-300">Drivers License</span></span>
- <span data-ttu-id="0b6c6-301">Драйверы лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-301">Drivers Licenses</span></span>
- <span data-ttu-id="0b6c6-302">Driver'License</span><span class="sxs-lookup"><span data-stu-id="0b6c6-302">Driver'License</span></span>
- <span data-ttu-id="0b6c6-303">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-303">Driver'Licenses</span></span>
- <span data-ttu-id="0b6c6-304">Драйвер "лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-304">Driver' License</span></span>
- <span data-ttu-id="0b6c6-305">Драйвер "лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-305">Driver' Licenses</span></span>
- <span data-ttu-id="0b6c6-306">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-306">Driver'sLicense</span></span>
- <span data-ttu-id="0b6c6-307">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-307">Driver'sLicenses</span></span>
- <span data-ttu-id="0b6c6-308">Водительского удостоверения для лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-308">Driver's License</span></span>
- <span data-ttu-id="0b6c6-309">Водительского удостоверения для лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-309">Driver's Licenses</span></span>
- <span data-ttu-id="0b6c6-310">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-310">DriverLicense#</span></span>
- <span data-ttu-id="0b6c6-311">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-311">DriverLicenses#</span></span>
- <span data-ttu-id="0b6c6-312">Драйвер лицензии #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-312">Driver License#</span></span>
- <span data-ttu-id="0b6c6-313">Драйвер лицензий #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-313">Driver Licenses#</span></span>
- <span data-ttu-id="0b6c6-314">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-314">DriversLicense#</span></span>
- <span data-ttu-id="0b6c6-315">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-315">DriversLicenses#</span></span>
- <span data-ttu-id="0b6c6-316">Драйверы лицензии #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-316">Drivers License#</span></span>
- <span data-ttu-id="0b6c6-317">Драйверы лицензий #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-317">Drivers Licenses#</span></span>
- <span data-ttu-id="0b6c6-318">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-318">Driver'License#</span></span>
- <span data-ttu-id="0b6c6-319">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-319">Driver'Licenses#</span></span>
- <span data-ttu-id="0b6c6-320">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-320">Driver' License#</span></span>
- <span data-ttu-id="0b6c6-321">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-321">Driver' Licenses#</span></span>
- <span data-ttu-id="0b6c6-322">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-322">Driver'sLicense#</span></span>
- <span data-ttu-id="0b6c6-323">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="0b6c6-324">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-324">Driver's License#</span></span>
- <span data-ttu-id="0b6c6-325">

Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="0b6c6-326">Номер карты медицинского страхования для Австралии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-327">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-327">Format</span></span>

<span data-ttu-id="0b6c6-328">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-329">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-329">Pattern</span></span>

<span data-ttu-id="0b6c6-330">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-330">10-11 digits:</span></span>
- <span data-ttu-id="0b6c6-331">Первая цифра находится в диапазоне 2–6.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="0b6c6-332">Девятая цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="0b6c6-333">Десятая цифра — цифра серии.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="0b6c6-334">Одиннадцатая цифра (необязательно) — индивидуальный номер.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-335">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-335">Checksum</span></span>

<span data-ttu-id="0b6c6-336">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-337">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-337">Definition</span></span>

<span data-ttu-id="0b6c6-338">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-339">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-340">находится ключевое слово из Keyword_Australia_Medical_Account_Number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="0b6c6-341">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-341">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-342">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-343">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-344">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-344">The checksum passes.</span></span>

```
  <!-- Australia Medical Account Number -->
<Entity id="104a99a0-3d3b-4542-a40d-ab0b9e1efe63" recommendedConfidence="85" patternsProximity="300">
    <Pattern confidenceLevel="95">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="1">
     <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
<Pattern confidenceLevel="85">
     <IdMatch idRef="Func_australian_medical_account_number"/>
     <Any minMatches="0" maxMatches="0">
  <Match idRef="Keyword_Australia_Medical_Account_Number"/>
     </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-345">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="0b6c6-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="0b6c6-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="0b6c6-347">bank account details</span></span>
- <span data-ttu-id="0b6c6-348">
medicare payments</span><span class="sxs-lookup"><span data-stu-id="0b6c6-348">medicare payments</span></span>
- <span data-ttu-id="0b6c6-349">
mortgage account</span><span class="sxs-lookup"><span data-stu-id="0b6c6-349">mortgage account</span></span>
- <span data-ttu-id="0b6c6-350">
bank payments</span><span class="sxs-lookup"><span data-stu-id="0b6c6-350">bank payments</span></span>
- <span data-ttu-id="0b6c6-351">
information branch</span><span class="sxs-lookup"><span data-stu-id="0b6c6-351">information branch</span></span>
- <span data-ttu-id="0b6c6-352">
credit card loan</span><span class="sxs-lookup"><span data-stu-id="0b6c6-352">credit card loan</span></span>
- <span data-ttu-id="0b6c6-353">
department of human services</span><span class="sxs-lookup"><span data-stu-id="0b6c6-353">department of human services</span></span>
- <span data-ttu-id="0b6c6-354">Локальная служба</span><span class="sxs-lookup"><span data-stu-id="0b6c6-354">local service</span></span>
- <span data-ttu-id="0b6c6-355">

medicare</span><span class="sxs-lookup"><span data-stu-id="0b6c6-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="0b6c6-356">Номер паспорта гражданина Австралии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-357">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-357">Format</span></span>

<span data-ttu-id="0b6c6-358">Буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-359">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-359">Pattern</span></span>

<span data-ttu-id="0b6c6-360">Буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-361">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-361">Checksum</span></span>

<span data-ttu-id="0b6c6-362">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-363">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-363">Definition</span></span>

<span data-ttu-id="0b6c6-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-365">регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-366">Ключевое слово из Keyword_passport или Keyword_australia_passport_number найти.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```
<!-- Australia Passport Number -->
<Entity id="29869db6-602d-4853-ab93-3484f905df50" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_australia_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_australia_passport_number" />
        </Any>
   </Pattern>
</Entity>   
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-367">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="0b6c6-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-368">Keyword_passport</span></span>

- <span data-ttu-id="0b6c6-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-369">Passport Number</span></span>
- <span data-ttu-id="0b6c6-370">
Passport No</span><span class="sxs-lookup"><span data-stu-id="0b6c6-370">Passport No</span></span>
- <span data-ttu-id="0b6c6-371">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-371">Passport #</span></span>
- <span data-ttu-id="0b6c6-372">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-372">Passport#</span></span>
- <span data-ttu-id="0b6c6-373">PassportID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-373">PassportID</span></span>
- <span data-ttu-id="0b6c6-374">Passportno
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-374">Passportno</span></span>
- <span data-ttu-id="0b6c6-375">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-375">passportnumber</span></span>
- <span data-ttu-id="0b6c6-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="0b6c6-376">パスポート</span></span>
- <span data-ttu-id="0b6c6-377">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-377">パスポート番号</span></span>
- <span data-ttu-id="0b6c6-378">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-378">パスポートのNum</span></span>
- <span data-ttu-id="0b6c6-379">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-379">パスポート ＃</span></span> 
- <span data-ttu-id="0b6c6-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-380">Numéro de passeport</span></span>
- <span data-ttu-id="0b6c6-381">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="0b6c6-381">Passeport n °</span></span>
- <span data-ttu-id="0b6c6-382">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-382">Passeport Non</span></span>
- <span data-ttu-id="0b6c6-383">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-383">Passeport #</span></span>
- <span data-ttu-id="0b6c6-384">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-384">Passeport#</span></span>
- <span data-ttu-id="0b6c6-385">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="0b6c6-385">PasseportNon</span></span>
- <span data-ttu-id="0b6c6-386">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="0b6c6-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="0b6c6-388">passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-388">passport</span></span>
- <span data-ttu-id="0b6c6-389">
passport details</span><span class="sxs-lookup"><span data-stu-id="0b6c6-389">passport details</span></span>
- <span data-ttu-id="0b6c6-390">
immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="0b6c6-390">immigration and citizenship</span></span>
- <span data-ttu-id="0b6c6-391">
commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="0b6c6-391">commonwealth of australia</span></span>
- <span data-ttu-id="0b6c6-392">
department of immigration</span><span class="sxs-lookup"><span data-stu-id="0b6c6-392">department of immigration</span></span>
- <span data-ttu-id="0b6c6-393">
residential address</span><span class="sxs-lookup"><span data-stu-id="0b6c6-393">residential address</span></span>
- <span data-ttu-id="0b6c6-394">
department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="0b6c6-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="0b6c6-395">visa
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-395">visa</span></span>
- <span data-ttu-id="0b6c6-396">
national identity card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-396">national identity card</span></span>
- <span data-ttu-id="0b6c6-397">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="0b6c6-397">passport number</span></span>
- <span data-ttu-id="0b6c6-398">
travel document</span><span class="sxs-lookup"><span data-stu-id="0b6c6-398">travel document</span></span>
- <span data-ttu-id="0b6c6-399">

issuing authority</span><span class="sxs-lookup"><span data-stu-id="0b6c6-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="0b6c6-400">Номер налогоплательщика для Австралии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-401">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-401">Format</span></span>

<span data-ttu-id="0b6c6-402">8–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-403">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-403">Pattern</span></span>

<span data-ttu-id="0b6c6-404">8–9 цифр, которые обычно разделены пробелами указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="0b6c6-405">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-405">Three digits</span></span> 
- <span data-ttu-id="0b6c6-406">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="0b6c6-406">An optional space</span></span> 
- <span data-ttu-id="0b6c6-407">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-407">Three digits</span></span> 
- <span data-ttu-id="0b6c6-408">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="0b6c6-408">An optional space</span></span> 
- <span data-ttu-id="0b6c6-409">2–3 цифры, причем последняя цифра — контрольная</span><span class="sxs-lookup"><span data-stu-id="0b6c6-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-410">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-410">Checksum</span></span>

<span data-ttu-id="0b6c6-411">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-412">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-412">Definition</span></span>

<span data-ttu-id="0b6c6-413">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-414">функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-415">ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="0b6c6-416">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-416">The checksum passes.</span></span>

```
    <!-- Australia Tax File Number -->
<Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
    
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_Australia_Tax_File_Number" />
          <Match idRef="Keyword_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="0b6c6-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="0b6c6-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-419">australian business number</span></span>
- <span data-ttu-id="0b6c6-420">
marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="0b6c6-420">marginal tax rate</span></span>
- <span data-ttu-id="0b6c6-421">
medicare levy</span><span class="sxs-lookup"><span data-stu-id="0b6c6-421">medicare levy</span></span>
- <span data-ttu-id="0b6c6-422">
portfolio number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-422">portfolio number</span></span>
- <span data-ttu-id="0b6c6-423">
service veterans</span><span class="sxs-lookup"><span data-stu-id="0b6c6-423">service veterans</span></span>
- <span data-ttu-id="0b6c6-424">
withholding tax</span><span class="sxs-lookup"><span data-stu-id="0b6c6-424">withholding tax</span></span>
- <span data-ttu-id="0b6c6-425">
individual tax return</span><span class="sxs-lookup"><span data-stu-id="0b6c6-425">individual tax return</span></span>
- <span data-ttu-id="0b6c6-426">

tax file number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="0b6c6-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="0b6c6-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="0b6c6-428">00000000</span><span class="sxs-lookup"><span data-stu-id="0b6c6-428">00000000</span></span>
- <span data-ttu-id="0b6c6-429">11111111</span><span class="sxs-lookup"><span data-stu-id="0b6c6-429">11111111</span></span>
- <span data-ttu-id="0b6c6-430">22222222</span><span class="sxs-lookup"><span data-stu-id="0b6c6-430">22222222</span></span>
- <span data-ttu-id="0b6c6-431">33333333</span><span class="sxs-lookup"><span data-stu-id="0b6c6-431">33333333</span></span>
- <span data-ttu-id="0b6c6-432">44444444</span><span class="sxs-lookup"><span data-stu-id="0b6c6-432">44444444</span></span>
- <span data-ttu-id="0b6c6-433">55555555</span><span class="sxs-lookup"><span data-stu-id="0b6c6-433">55555555</span></span>
- <span data-ttu-id="0b6c6-434">66666666</span><span class="sxs-lookup"><span data-stu-id="0b6c6-434">66666666</span></span>
- <span data-ttu-id="0b6c6-435">77777777</span><span class="sxs-lookup"><span data-stu-id="0b6c6-435">77777777</span></span>
- <span data-ttu-id="0b6c6-436">88888888</span><span class="sxs-lookup"><span data-stu-id="0b6c6-436">88888888</span></span>
- <span data-ttu-id="0b6c6-437">99999999 включительно</span><span class="sxs-lookup"><span data-stu-id="0b6c6-437">99999999</span></span>
- <span data-ttu-id="0b6c6-438">000000000</span><span class="sxs-lookup"><span data-stu-id="0b6c6-438">000000000</span></span>
- <span data-ttu-id="0b6c6-439">111111111</span><span class="sxs-lookup"><span data-stu-id="0b6c6-439">111111111</span></span>
- <span data-ttu-id="0b6c6-440">222222222</span><span class="sxs-lookup"><span data-stu-id="0b6c6-440">222222222</span></span>
- <span data-ttu-id="0b6c6-441">333333333</span><span class="sxs-lookup"><span data-stu-id="0b6c6-441">333333333</span></span>
- <span data-ttu-id="0b6c6-442">444444444</span><span class="sxs-lookup"><span data-stu-id="0b6c6-442">444444444</span></span>
- <span data-ttu-id="0b6c6-443">555555555</span><span class="sxs-lookup"><span data-stu-id="0b6c6-443">555555555</span></span>
- <span data-ttu-id="0b6c6-444">666666666</span><span class="sxs-lookup"><span data-stu-id="0b6c6-444">666666666</span></span>
- <span data-ttu-id="0b6c6-445">777777777</span><span class="sxs-lookup"><span data-stu-id="0b6c6-445">777777777</span></span>
- <span data-ttu-id="0b6c6-446">888888888</span><span class="sxs-lookup"><span data-stu-id="0b6c6-446">888888888</span></span>
- <span data-ttu-id="0b6c6-447">999999999</span><span class="sxs-lookup"><span data-stu-id="0b6c6-447">999999999</span></span>
- <span data-ttu-id="0b6c6-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="0b6c6-448">0000000000</span></span>
- <span data-ttu-id="0b6c6-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="0b6c6-449">1111111111</span></span>
- <span data-ttu-id="0b6c6-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="0b6c6-450">2222222222</span></span>
- <span data-ttu-id="0b6c6-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="0b6c6-451">3333333333</span></span>
- <span data-ttu-id="0b6c6-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="0b6c6-452">4444444444</span></span>
- <span data-ttu-id="0b6c6-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="0b6c6-453">5555555555</span></span>
- <span data-ttu-id="0b6c6-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="0b6c6-454">6666666666</span></span>
- <span data-ttu-id="0b6c6-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="0b6c6-455">7777777777</span></span>
- <span data-ttu-id="0b6c6-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="0b6c6-456">8888888888</span></span>
- <span data-ttu-id="0b6c6-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="0b6c6-457">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="0b6c6-458">Номер национального документа для Бельгии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-458">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-459">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-459">Format</span></span>

<span data-ttu-id="0b6c6-460">11 цифр, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-460">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-461">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-461">Pattern</span></span>

<span data-ttu-id="0b6c6-462">11 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-462">11 digits plus delimiters:</span></span>
- <span data-ttu-id="0b6c6-463">шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-463">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="0b6c6-464">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-464">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-465">три последовательные цифры (нечетные для мужчин, четные для женщин);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-465">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="0b6c6-466">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-466">A period</span></span> 
- <span data-ttu-id="0b6c6-467">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-467">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-468">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-468">Checksum</span></span>

<span data-ttu-id="0b6c6-469">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-469">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-470">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-470">Definition</span></span>

<span data-ttu-id="0b6c6-471">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-472">функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-472">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-473">находится ключевое слово из Keyword_belgium_national_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-473">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="0b6c6-474">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-474">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-475">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-475">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="0b6c6-476">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-476">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="0b6c6-477">Identity</span><span class="sxs-lookup"><span data-stu-id="0b6c6-477">Identity</span></span>
- <span data-ttu-id="0b6c6-478">Registration</span><span class="sxs-lookup"><span data-stu-id="0b6c6-478">Registration</span></span>
- <span data-ttu-id="0b6c6-479">Identification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-479">Identification</span></span> 
- <span data-ttu-id="0b6c6-480">ID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-480">ID</span></span> 
- <span data-ttu-id="0b6c6-481">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="0b6c6-481">Identiteitskaart</span></span>
- <span data-ttu-id="0b6c6-482">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-482">Registratie nummer</span></span> 
- <span data-ttu-id="0b6c6-483">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-483">Identificatie nummer</span></span> 
- <span data-ttu-id="0b6c6-484">Identiteit</span><span class="sxs-lookup"><span data-stu-id="0b6c6-484">Identiteit</span></span>
- <span data-ttu-id="0b6c6-485">Registratie</span><span class="sxs-lookup"><span data-stu-id="0b6c6-485">Registratie</span></span>
- <span data-ttu-id="0b6c6-486">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-486">Identificatie</span></span> 
- <span data-ttu-id="0b6c6-487">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-487">Carte d’identité</span></span> 
- <span data-ttu-id="0b6c6-488">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="0b6c6-488">numéro d'immatriculation</span></span>
- <span data-ttu-id="0b6c6-489">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-489">numéro d'identification</span></span>
- <span data-ttu-id="0b6c6-490">
identité
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-490">identité</span></span> 
- <span data-ttu-id="0b6c6-491">inscription
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-491">inscription</span></span> 
- <span data-ttu-id="0b6c6-492">Identifikation</span><span class="sxs-lookup"><span data-stu-id="0b6c6-492">Identifikation</span></span>
- <span data-ttu-id="0b6c6-493">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="0b6c6-493">Identifizierung</span></span>
- <span data-ttu-id="0b6c6-494">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-494">Identifikationsnummer</span></span>
- <span data-ttu-id="0b6c6-495">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="0b6c6-495">Personalausweis</span></span>
- <span data-ttu-id="0b6c6-496">Registrierung</span><span class="sxs-lookup"><span data-stu-id="0b6c6-496">Registrierung</span></span>
- <span data-ttu-id="0b6c6-497">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-497">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="0b6c6-498">Номер CPF для Бразилии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-498">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-499">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-499">Format</span></span>

<span data-ttu-id="0b6c6-500">11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-500">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-501">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-501">Pattern</span></span>

<span data-ttu-id="0b6c6-502">С форматированием</span><span class="sxs-lookup"><span data-stu-id="0b6c6-502">Formatted:</span></span>
- <span data-ttu-id="0b6c6-503">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-503">Three digits</span></span> 
- <span data-ttu-id="0b6c6-504">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-504">A period</span></span> 
- <span data-ttu-id="0b6c6-505">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-505">Three digits</span></span> 
- <span data-ttu-id="0b6c6-506">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-506">A period</span></span> 
- <span data-ttu-id="0b6c6-507">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-507">Three digits</span></span> 
- <span data-ttu-id="0b6c6-508">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-508">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-509">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-509">Two digits which are check digits</span></span>

<span data-ttu-id="0b6c6-510">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="0b6c6-510">Unformatted:</span></span>
- <span data-ttu-id="0b6c6-511">11 цифр, где две последние цифры — проверочные.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-511">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-512">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-512">Checksum</span></span>

<span data-ttu-id="0b6c6-513">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-514">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-514">Definition</span></span>

<span data-ttu-id="0b6c6-515">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-515">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-516">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-516">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-517">находится ключевое слово из Keyword_brazil_cpf;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-517">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="0b6c6-518">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-518">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-519">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-519">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-520">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-520">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-521">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-521">The checksum passes.</span></span>

```
<!-- Brazil CPF Number -->
<Entity id="78e09124-f2c3-4656-b32a-c1a132cd2711" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cpf"/>
     <Match idRef="Keyword_brazil_cpf"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cpf"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-522">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-522">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="0b6c6-523">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="0b6c6-523">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="0b6c6-524">CPF</span><span class="sxs-lookup"><span data-stu-id="0b6c6-524">CPF</span></span>
- <span data-ttu-id="0b6c6-525">Identification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-525">Identification</span></span>
- <span data-ttu-id="0b6c6-526">Registration</span><span class="sxs-lookup"><span data-stu-id="0b6c6-526">Registration</span></span>
- <span data-ttu-id="0b6c6-527">Revenue</span><span class="sxs-lookup"><span data-stu-id="0b6c6-527">Revenue</span></span>
- <span data-ttu-id="0b6c6-528">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-528">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="0b6c6-529">Imposto
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-529">Imposto</span></span> 
- <span data-ttu-id="0b6c6-530">Identificação
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-530">Identificação</span></span> 
- <span data-ttu-id="0b6c6-531">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-531">Inscrição</span></span> 
- <span data-ttu-id="0b6c6-532">Receita

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-532">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="0b6c6-533">Номер юридического лица для Бразилии (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-533">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-534">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-534">Format</span></span>

<span data-ttu-id="0b6c6-535">14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-535">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-536">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-536">Pattern</span></span>
<span data-ttu-id="0b6c6-537">14 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-537">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="0b6c6-538">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-538">Two digits</span></span> 
- <span data-ttu-id="0b6c6-539">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-539">A period</span></span> 
- <span data-ttu-id="0b6c6-540">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-540">Three digits</span></span> 
- <span data-ttu-id="0b6c6-541">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-541">A period</span></span> 
- <span data-ttu-id="0b6c6-542">три цифры (эти первые восемь цифр — регистрационный номер);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-542">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="0b6c6-543">косая черта;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-543">A forward slash</span></span> 
- <span data-ttu-id="0b6c6-544">номер отделения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-544">Four-digit branch number</span></span> 
- <span data-ttu-id="0b6c6-545">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-545">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-546">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-546">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-547">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-547">Checksum</span></span>

<span data-ttu-id="0b6c6-548">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-549">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-549">Definition</span></span>

<span data-ttu-id="0b6c6-550">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-551">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-551">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-552">находится ключевое слово из Keyword_brazil_cnpj;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-552">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="0b6c6-553">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-553">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-554">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-554">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-555">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-555">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-556">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-556">The checksum passes.</span></span>

```
<!-- Brazil Legal Entity Number (CNPJ) -->
<Entity id="9b58b5cd-5e90-4df6-b34f-1ebcc88ceae4" recommendedConfidence="85" patternsProximity="300">
   <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_cnpj"/>
     <Match idRef="Keyword_brazil_cnpj"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_cnpj"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-557">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-557">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="0b6c6-558">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="0b6c6-558">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="0b6c6-559">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-559">CNPJ</span></span> 
- <span data-ttu-id="0b6c6-560">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="0b6c6-560">CNPJ/MF</span></span> 
- <span data-ttu-id="0b6c6-561">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-561">CNPJ-MF</span></span> 
- <span data-ttu-id="0b6c6-562">National Registry of Legal Entities
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-562">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="0b6c6-563">Taxpayers Registry
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-563">Taxpayers Registry</span></span> 
- <span data-ttu-id="0b6c6-564">Legal entity
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-564">Legal entity</span></span> 
- <span data-ttu-id="0b6c6-565">Legal entities
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-565">Legal entities</span></span> 
- <span data-ttu-id="0b6c6-566">Registration Status
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-566">Registration Status</span></span> 
- <span data-ttu-id="0b6c6-567">Business
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-567">Business</span></span> 
- <span data-ttu-id="0b6c6-568">Company</span><span class="sxs-lookup"><span data-stu-id="0b6c6-568">Company</span></span>
- <span data-ttu-id="0b6c6-569">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-569">CNPJ</span></span> 
- <span data-ttu-id="0b6c6-570">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-570">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="0b6c6-571">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-571">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="0b6c6-572">CGC
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-572">CGC</span></span> 
- <span data-ttu-id="0b6c6-573">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-573">Pessoa jurídica</span></span> 
- <span data-ttu-id="0b6c6-574">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-574">Pessoas jurídicas</span></span> 
- <span data-ttu-id="0b6c6-575">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-575">Situação cadastral</span></span> 
- <span data-ttu-id="0b6c6-576">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-576">Inscrição</span></span> 
- <span data-ttu-id="0b6c6-577">Empresa
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-577">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="0b6c6-578">	Номер внутреннего удостоверения личности для Бразилии (RG)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-578">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-579">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-579">Format</span></span>

<span data-ttu-id="0b6c6-580">Geral Registro (старый формат): девяти цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-580">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="0b6c6-581">Identidade де Registro (РИК) (новый формат): 11 разрядов</span><span class="sxs-lookup"><span data-stu-id="0b6c6-581">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-582">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-582">Pattern</span></span>

<span data-ttu-id="0b6c6-583">Registro Geral (старый формат):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-583">Registro Geral (old format):</span></span>
- <span data-ttu-id="0b6c6-584">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-584">Two digits</span></span> 
- <span data-ttu-id="0b6c6-585">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-585">A period</span></span> 
- <span data-ttu-id="0b6c6-586">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-586">Three digits</span></span> 
- <span data-ttu-id="0b6c6-587">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-587">A period</span></span> 
- <span data-ttu-id="0b6c6-588">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-588">Three digits</span></span> 
- <span data-ttu-id="0b6c6-589">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-589">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-590">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-590">One digit which is a check digit</span></span>

<span data-ttu-id="0b6c6-591">Identidade де Registro (РИК) (новый формат):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-591">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="0b6c6-592">10 цифр;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-592">10 digits</span></span> 
- <span data-ttu-id="0b6c6-593">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-593">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-594">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-594">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-595">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-595">Checksum</span></span>

<span data-ttu-id="0b6c6-596">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-596">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-597">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-597">Definition</span></span>

<span data-ttu-id="0b6c6-598">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-598">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-599">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-599">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-600">находится ключевое слово из Keyword_brazil_rg;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-600">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="0b6c6-601">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-601">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-602">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-602">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-603">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-603">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-604">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-604">The checksum passes.</span></span>

```
<!-- Brazil National ID Card (RG) -->
<Entity id="486de900-db70-41b3-a886-abdf25af119c" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_brazil_rg"/>
     <Match idRef="Keyword_brazil_rg"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_brazil_rg"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-605">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-605">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="0b6c6-606">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="0b6c6-606">Keyword_brazil_rg</span></span>

<span data-ttu-id="0b6c6-607">Cédula де identidade идентификационной карты национальный идентификатор для número de rregistro registro де Iidentidade registro geral (в этом ключевых слов с учетом регистра) RG РИК (в этом ключевых слов с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-607">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="0b6c6-608">Номер банковского счета для Канады</span><span class="sxs-lookup"><span data-stu-id="0b6c6-608">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-609">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-609">Format</span></span>

<span data-ttu-id="0b6c6-610">Семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-610">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-611">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-611">Pattern</span></span>

<span data-ttu-id="0b6c6-612">Номер банковского счета для Канады — семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-612">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="0b6c6-613">Транзитный номер банковского счета в Канаде имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-613">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="0b6c6-614">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-614">Five digits</span></span> 
- <span data-ttu-id="0b6c6-615">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-615">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-616">Три цифры или</span><span class="sxs-lookup"><span data-stu-id="0b6c6-616">Three digits OR</span></span>
- <span data-ttu-id="0b6c6-617">ноль "0";</span><span class="sxs-lookup"><span data-stu-id="0b6c6-617">A zero "0"</span></span> 
- <span data-ttu-id="0b6c6-618">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-618">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-619">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-619">Checksum</span></span>

<span data-ttu-id="0b6c6-620">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-620">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-621">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-621">Definition</span></span>

<span data-ttu-id="0b6c6-622">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-622">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-623">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-623">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-624">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-624">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="0b6c6-625">регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-625">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="0b6c6-626">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-627">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-627">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-628">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-628">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```
<!-- Canada Bank Account Number -->
<Entity id="552e814c-cb50-4d94-bbaa-bb1d1ffb34de" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
        <Match idRef="Regex_canada_bank_account_transit_number" />
   </Pattern>
   <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_bank_account_number" />
        <Match idRef="Keyword_canada_bank_account_number" />
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-629">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-629">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="0b6c6-630">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-630">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="0b6c6-631">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="0b6c6-631">canada savings bonds</span></span>
- <span data-ttu-id="0b6c6-632">
canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="0b6c6-632">canada revenue agency</span></span>
- <span data-ttu-id="0b6c6-633">
canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="0b6c6-633">canadian financial institution</span></span>
- <span data-ttu-id="0b6c6-634">
direct deposit form</span><span class="sxs-lookup"><span data-stu-id="0b6c6-634">direct deposit form</span></span>
- <span data-ttu-id="0b6c6-635">
canadian citizen</span><span class="sxs-lookup"><span data-stu-id="0b6c6-635">canadian citizen</span></span>
- <span data-ttu-id="0b6c6-636">
legal representative</span><span class="sxs-lookup"><span data-stu-id="0b6c6-636">legal representative</span></span>
- <span data-ttu-id="0b6c6-637">
notary public</span><span class="sxs-lookup"><span data-stu-id="0b6c6-637">notary public</span></span>
- <span data-ttu-id="0b6c6-638">
commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="0b6c6-638">commissioner for oaths</span></span>
- <span data-ttu-id="0b6c6-639">
child care benefit</span><span class="sxs-lookup"><span data-stu-id="0b6c6-639">child care benefit</span></span>
- <span data-ttu-id="0b6c6-640">
universal child care</span><span class="sxs-lookup"><span data-stu-id="0b6c6-640">universal child care</span></span>
- <span data-ttu-id="0b6c6-641">
canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="0b6c6-641">canada child tax benefit</span></span>
- <span data-ttu-id="0b6c6-642">
income tax benefit</span><span class="sxs-lookup"><span data-stu-id="0b6c6-642">income tax benefit</span></span>
- <span data-ttu-id="0b6c6-643">
harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="0b6c6-643">harmonized sales tax</span></span>
- <span data-ttu-id="0b6c6-644">social insurance number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-644">social insurance number</span></span>
- <span data-ttu-id="0b6c6-645">
income tax refund</span><span class="sxs-lookup"><span data-stu-id="0b6c6-645">income tax refund</span></span>
- <span data-ttu-id="0b6c6-646">
child tax benefit</span><span class="sxs-lookup"><span data-stu-id="0b6c6-646">child tax benefit</span></span>
- <span data-ttu-id="0b6c6-647">
territorial payments</span><span class="sxs-lookup"><span data-stu-id="0b6c6-647">territorial payments</span></span>
- <span data-ttu-id="0b6c6-648">
institution number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-648">institution number</span></span>
- <span data-ttu-id="0b6c6-649">
deposit request</span><span class="sxs-lookup"><span data-stu-id="0b6c6-649">deposit request</span></span>
- <span data-ttu-id="0b6c6-650">
banking information</span><span class="sxs-lookup"><span data-stu-id="0b6c6-650">banking information</span></span>
- <span data-ttu-id="0b6c6-651">

direct deposit</span><span class="sxs-lookup"><span data-stu-id="0b6c6-651">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="0b6c6-652">Номер водительского удостоверения для Канады</span><span class="sxs-lookup"><span data-stu-id="0b6c6-652">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-653">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-653">Format</span></span>

<span data-ttu-id="0b6c6-654">Зависит от провинции.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-654">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-655">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-655">Pattern</span></span>

<span data-ttu-id="0b6c6-656">Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-656">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-657">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-657">Checksum</span></span>

<span data-ttu-id="0b6c6-658">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-658">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-659">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-659">Definition</span></span>

<span data-ttu-id="0b6c6-660">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-660">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-661">функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-661">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-662">находится ключевое слово из Keyword_[province_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-662">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="0b6c6-663">находится ключевое слово из Keyword_canada_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-663">A keyword from Keyword_canada_drivers_license is found.</span></span>

```
<!-- Canada Driver's License Number -->
    <Entity id="37186abb-8e48-4800-ad3c-e3d1610b3db0" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_alberta_drivers_license_number" />
        <Match idRef="Keyword_alberta_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_british_columbia_drivers_license_number" />
        <Match idRef="Keyword_british_columbia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_manitoba_drivers_license_number" />
        <Match idRef="Keyword_manitoba_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_brunswick_drivers_license_number" />
        <Match idRef="Keyword_new_brunswick_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_newfoundland_labrador_drivers_license_number" />
        <Match idRef="Keyword_newfoundland_labrador_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_nova_scotia_drivers_license_number" />
        <Match idRef="Keyword_nova_scotia_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_ontario_drivers_license_number" />
        <Match idRef="Keyword_ontario_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_prince_edward_island_drivers_license_number" />
        <Match idRef="Keyword_prince_edward_island_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_quebec_drivers_license_number" />
        <Match idRef="Keyword_quebec_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_saskatchewan_drivers_license_number" />
        <Match idRef="Keyword_saskatchewan_drivers_license_name" />
        <Match idRef="Keyword_canada_drivers_license" />
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-664">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-664">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="0b6c6-665">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="0b6c6-665">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="0b6c6-666">Аббревиатура провинции, например AB.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-666">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="0b6c6-667">
Название провинции, например Альберта.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-667">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="0b6c6-668">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-668">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="0b6c6-669">DL</span><span class="sxs-lookup"><span data-stu-id="0b6c6-669">DL</span></span>
- <span data-ttu-id="0b6c6-670">DLS</span><span class="sxs-lookup"><span data-stu-id="0b6c6-670">DLS</span></span>
- <span data-ttu-id="0b6c6-671">CDL</span><span class="sxs-lookup"><span data-stu-id="0b6c6-671">CDL</span></span>
- <span data-ttu-id="0b6c6-672">CDLS</span><span class="sxs-lookup"><span data-stu-id="0b6c6-672">CDLS</span></span>
- <span data-ttu-id="0b6c6-673">DriverLic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-673">DriverLic</span></span>
- <span data-ttu-id="0b6c6-674">DriverLics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-674">DriverLics</span></span>
- <span data-ttu-id="0b6c6-675">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-675">DriverLicense</span></span>
- <span data-ttu-id="0b6c6-676">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-676">DriverLicenses</span></span>
- <span data-ttu-id="0b6c6-677">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-677">DriverLicence</span></span>
- <span data-ttu-id="0b6c6-678">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-678">DriverLicences</span></span>
- <span data-ttu-id="0b6c6-679">Драйвер Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-679">Driver Lic</span></span>
- <span data-ttu-id="0b6c6-680">Драйвер Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-680">Driver Lics</span></span>
- <span data-ttu-id="0b6c6-681">Драйвер лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-681">Driver License</span></span>
- <span data-ttu-id="0b6c6-682">Драйвер лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-682">Driver Licenses</span></span>
- <span data-ttu-id="0b6c6-683">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-683">Driver Licence</span></span>
- <span data-ttu-id="0b6c6-684">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-684">Driver Licences</span></span>
- <span data-ttu-id="0b6c6-685">DriversLic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-685">DriversLic</span></span>
- <span data-ttu-id="0b6c6-686">DriversLics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-686">DriversLics</span></span>
- <span data-ttu-id="0b6c6-687">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-687">DriversLicence</span></span>
- <span data-ttu-id="0b6c6-688">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-688">DriversLicences</span></span>
- <span data-ttu-id="0b6c6-689">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-689">DriversLicense</span></span>
- <span data-ttu-id="0b6c6-690">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-690">DriversLicenses</span></span>
- <span data-ttu-id="0b6c6-691">Драйверы Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-691">Drivers Lic</span></span>
- <span data-ttu-id="0b6c6-692">Драйверы Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-692">Drivers Lics</span></span>
- <span data-ttu-id="0b6c6-693">Драйверы лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-693">Drivers License</span></span>
- <span data-ttu-id="0b6c6-694">Драйверы лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-694">Drivers Licenses</span></span>
- <span data-ttu-id="0b6c6-695">Лицензия драйверы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-695">Drivers Licence</span></span>
- <span data-ttu-id="0b6c6-696">Число лицензий на драйверы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-696">Drivers Licences</span></span>
- <span data-ttu-id="0b6c6-697">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-697">Driver'Lic</span></span>
- <span data-ttu-id="0b6c6-698">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-698">Driver'Lics</span></span>
- <span data-ttu-id="0b6c6-699">Driver'License</span><span class="sxs-lookup"><span data-stu-id="0b6c6-699">Driver'License</span></span>
- <span data-ttu-id="0b6c6-700">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-700">Driver'Licenses</span></span>
- <span data-ttu-id="0b6c6-701">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-701">Driver'Licence</span></span>
- <span data-ttu-id="0b6c6-702">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-702">Driver'Licences</span></span>
- <span data-ttu-id="0b6c6-703">Драйвер ' Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-703">Driver' Lic</span></span>
- <span data-ttu-id="0b6c6-704">Драйвер ' Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-704">Driver' Lics</span></span>
- <span data-ttu-id="0b6c6-705">Драйвер "лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-705">Driver' License</span></span>
- <span data-ttu-id="0b6c6-706">Драйвер "лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-706">Driver' Licenses</span></span>
- <span data-ttu-id="0b6c6-707">Драйвер "лицензия</span><span class="sxs-lookup"><span data-stu-id="0b6c6-707">Driver' Licence</span></span>
- <span data-ttu-id="0b6c6-708">Драйвер "число лицензий на по</span><span class="sxs-lookup"><span data-stu-id="0b6c6-708">Driver' Licences</span></span>
- <span data-ttu-id="0b6c6-709">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-709">Driver'sLic</span></span>
- <span data-ttu-id="0b6c6-710">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-710">Driver'sLics</span></span>
- <span data-ttu-id="0b6c6-711">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-711">Driver'sLicense</span></span>
- <span data-ttu-id="0b6c6-712">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-712">Driver'sLicenses</span></span>
- <span data-ttu-id="0b6c6-713">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-713">Driver'sLicence</span></span>
- <span data-ttu-id="0b6c6-714">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-714">Driver'sLicences</span></span>
- <span data-ttu-id="0b6c6-715">Lic драйвера</span><span class="sxs-lookup"><span data-stu-id="0b6c6-715">Driver's Lic</span></span>
- <span data-ttu-id="0b6c6-716">Lics драйвера</span><span class="sxs-lookup"><span data-stu-id="0b6c6-716">Driver's Lics</span></span>
- <span data-ttu-id="0b6c6-717">Водительского удостоверения для лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-717">Driver's License</span></span>
- <span data-ttu-id="0b6c6-718">Водительского удостоверения для лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-718">Driver's Licenses</span></span>
- <span data-ttu-id="0b6c6-719">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-719">Driver's Licence</span></span>
- <span data-ttu-id="0b6c6-720">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-720">Driver's Licences</span></span>
- <span data-ttu-id="0b6c6-721">Conduire де Permis</span><span class="sxs-lookup"><span data-stu-id="0b6c6-721">Permis de Conduire</span></span>
- <span data-ttu-id="0b6c6-722">id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-722">id</span></span>
- <span data-ttu-id="0b6c6-723">идентификаторы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-723">ids</span></span>
- <span data-ttu-id="0b6c6-724">
idcard number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-724">idcard number</span></span>
- <span data-ttu-id="0b6c6-725">
idcard numbers</span><span class="sxs-lookup"><span data-stu-id="0b6c6-725">idcard numbers</span></span>
- <span data-ttu-id="0b6c6-726">
idcard#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-726">idcard #</span></span>
- <span data-ttu-id="0b6c6-727">
idcard #s</span><span class="sxs-lookup"><span data-stu-id="0b6c6-727">idcard #s</span></span>
- <span data-ttu-id="0b6c6-728">idcard карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-728">idcard card</span></span>
- <span data-ttu-id="0b6c6-729">idcard карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-729">idcard cards</span></span>
- <span data-ttu-id="0b6c6-730">idcard</span><span class="sxs-lookup"><span data-stu-id="0b6c6-730">idcard</span></span>
- <span data-ttu-id="0b6c6-731">identification number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-731">identification number</span></span>
- <span data-ttu-id="0b6c6-732">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-732">identification numbers</span></span>
- <span data-ttu-id="0b6c6-733">identification #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-733">identification #</span></span>
- <span data-ttu-id="0b6c6-734">
identification #s</span><span class="sxs-lookup"><span data-stu-id="0b6c6-734">identification #s</span></span>
- <span data-ttu-id="0b6c6-735">Идентификация карточки</span><span class="sxs-lookup"><span data-stu-id="0b6c6-735">identification card</span></span>
- <span data-ttu-id="0b6c6-736">Идентификация карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-736">identification cards</span></span>
- <span data-ttu-id="0b6c6-737">
identification
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-737">identification</span></span> 
- <span data-ttu-id="0b6c6-738">DL#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-738">DL#</span></span>
- <span data-ttu-id="0b6c6-739">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-739">DLS#</span></span> 
- <span data-ttu-id="0b6c6-740">CDL#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-740">CDL#</span></span> 
- <span data-ttu-id="0b6c6-741">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-741">CDLS#</span></span> 
- <span data-ttu-id="0b6c6-742">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-742">DriverLic#</span></span> 
- <span data-ttu-id="0b6c6-743">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-743">DriverLics#</span></span> 
- <span data-ttu-id="0b6c6-744">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-744">DriverLicense#</span></span> 
- <span data-ttu-id="0b6c6-745">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-745">DriverLicenses#</span></span> 
- <span data-ttu-id="0b6c6-746">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-746">DriverLicence#</span></span> 
- <span data-ttu-id="0b6c6-747">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-747">DriverLicences#</span></span> 
- <span data-ttu-id="0b6c6-748">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-748">Driver Lic#</span></span>
- <span data-ttu-id="0b6c6-749">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-749">Driver Lics#</span></span> 
- <span data-ttu-id="0b6c6-750">Драйвер лицензии #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-750">Driver License#</span></span> 
- <span data-ttu-id="0b6c6-751">Драйвер лицензий #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-751">Driver Licenses#</span></span> 
- <span data-ttu-id="0b6c6-752">Драйвер лицензии #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-752">Driver License#</span></span> 
- <span data-ttu-id="0b6c6-753">Драйвер число лицензий на #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-753">Driver Licences#</span></span> 
- <span data-ttu-id="0b6c6-754">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-754">DriversLic#</span></span> 
- <span data-ttu-id="0b6c6-755">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-755">DriversLics#</span></span> 
- <span data-ttu-id="0b6c6-756">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-756">DriversLicense#</span></span> 
- <span data-ttu-id="0b6c6-757">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-757">DriversLicenses#</span></span> 
- <span data-ttu-id="0b6c6-758">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-758">DriversLicence#</span></span> 
- <span data-ttu-id="0b6c6-759">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-759">DriversLicences#</span></span> 
- <span data-ttu-id="0b6c6-760">Драйверы Lic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-760">Drivers Lic#</span></span> 
- <span data-ttu-id="0b6c6-761">Драйверы Lics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-761">Drivers Lics#</span></span> 
- <span data-ttu-id="0b6c6-762">Драйверы лицензии #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-762">Drivers License#</span></span> 
- <span data-ttu-id="0b6c6-763">Драйверы лицензий #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-763">Drivers Licenses#</span></span> 
- <span data-ttu-id="0b6c6-764">Драйверы лицензия #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-764">Drivers Licence#</span></span> 
- <span data-ttu-id="0b6c6-765">Число лицензий на драйверы #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-765">Drivers Licences#</span></span> 
- <span data-ttu-id="0b6c6-766">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-766">Driver'Lic#</span></span> 
- <span data-ttu-id="0b6c6-767">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-767">Driver'Lics#</span></span> 
- <span data-ttu-id="0b6c6-768">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-768">Driver'License#</span></span> 
- <span data-ttu-id="0b6c6-769">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-769">Driver'Licenses#</span></span> 
- <span data-ttu-id="0b6c6-770">Driver' Licence#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-770">Driver'Licence#</span></span> 
- <span data-ttu-id="0b6c6-771">Driver' Licences#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-771">Driver'Licences#</span></span> 
- <span data-ttu-id="0b6c6-772">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-772">Driver' Lic#</span></span> 
- <span data-ttu-id="0b6c6-773">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-773">Driver' Lics#</span></span> 
- <span data-ttu-id="0b6c6-774">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-774">Driver' License#</span></span> 
- <span data-ttu-id="0b6c6-775">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-775">Driver' Licenses#</span></span> 
- <span data-ttu-id="0b6c6-776">Драйвер "лицензия #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-776">Driver' Licence#</span></span> 
- <span data-ttu-id="0b6c6-777">Драйвер "число лицензий на #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-777">Driver' Licences#</span></span> 
- <span data-ttu-id="0b6c6-778">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-778">Driver'sLic#</span></span> 
- <span data-ttu-id="0b6c6-779">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-779">Driver'sLics#</span></span> 
- <span data-ttu-id="0b6c6-780">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-780">Driver'sLicense#</span></span> 
- <span data-ttu-id="0b6c6-781">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-781">Driver'sLicenses#</span></span> 
- <span data-ttu-id="0b6c6-782">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-782">Driver'sLicence#</span></span> 
- <span data-ttu-id="0b6c6-783">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-783">Driver'sLicences#</span></span> 
- <span data-ttu-id="0b6c6-784">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-784">Driver's Lic#</span></span> 
- <span data-ttu-id="0b6c6-785">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-785">Driver's Lics#</span></span> 
- <span data-ttu-id="0b6c6-786">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-786">Driver's License#</span></span> 
- <span data-ttu-id="0b6c6-787">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-787">Driver's Licenses#</span></span> 
- <span data-ttu-id="0b6c6-788">Лицензия водительского #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-788">Driver's Licence#</span></span> 
- <span data-ttu-id="0b6c6-789">Число лицензий на водительского #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-789">Driver's Licences#</span></span> 
- <span data-ttu-id="0b6c6-790">Permis de Conduire #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-790">Permis de Conduire#</span></span> 
- <span data-ttu-id="0b6c6-791">Идентификатор #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-791">id#</span></span> 
- <span data-ttu-id="0b6c6-792">идентификаторы #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-792">ids#</span></span> 
- <span data-ttu-id="0b6c6-793">idcard card#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-793">idcard card#</span></span> 
- <span data-ttu-id="0b6c6-794">idcard cards#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-794">idcard cards#</span></span> 
- <span data-ttu-id="0b6c6-795">idcard#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-795">idcard#</span></span> 
- <span data-ttu-id="0b6c6-796">identification card#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-796">identification card#</span></span> 
- <span data-ttu-id="0b6c6-797">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-797">identification cards#</span></span> 
- <span data-ttu-id="0b6c6-798">identification #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-798">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="0b6c6-799">Номер службы здравоохранения для Канады</span><span class="sxs-lookup"><span data-stu-id="0b6c6-799">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-800">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-800">Format</span></span>

<span data-ttu-id="0b6c6-801">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-801">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-802">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-802">Pattern</span></span>

<span data-ttu-id="0b6c6-803">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-803">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-804">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-804">Checksum</span></span>

<span data-ttu-id="0b6c6-805">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-805">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-806">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-806">Definition</span></span>

<span data-ttu-id="0b6c6-807">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-807">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-808">регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-808">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-809">находится ключевое слово из Keyword_canada_health_service_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-809">A keyword from Keyword_canada_health_service_number is found.</span></span>

```
<!-- Canada Health Service Number -->
<Entity id="59c0bf39-7fab-482c-af25-00faa4384c94" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_health_service_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_health_service_number" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-810">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-810">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="0b6c6-811">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-811">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="0b6c6-812">personal health number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-812">personal health number</span></span>
- <span data-ttu-id="0b6c6-813">
patient information</span><span class="sxs-lookup"><span data-stu-id="0b6c6-813">patient information</span></span>
- <span data-ttu-id="0b6c6-814">работоспособность службы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-814">health services</span></span>
- <span data-ttu-id="0b6c6-815">
speciality services</span><span class="sxs-lookup"><span data-stu-id="0b6c6-815">speciality services</span></span>
- <span data-ttu-id="0b6c6-816">
automobile accident</span><span class="sxs-lookup"><span data-stu-id="0b6c6-816">automobile accident</span></span>
- <span data-ttu-id="0b6c6-817">
patient hospital</span><span class="sxs-lookup"><span data-stu-id="0b6c6-817">patient hospital</span></span>
- <span data-ttu-id="0b6c6-818">
psychiatrist</span><span class="sxs-lookup"><span data-stu-id="0b6c6-818">psychiatrist</span></span>
- <span data-ttu-id="0b6c6-819">
workers compensation</span><span class="sxs-lookup"><span data-stu-id="0b6c6-819">workers compensation</span></span>
- <span data-ttu-id="0b6c6-820">
disability</span><span class="sxs-lookup"><span data-stu-id="0b6c6-820">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="0b6c6-821">Номер паспорта гражданина Канады</span><span class="sxs-lookup"><span data-stu-id="0b6c6-821">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-822">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-822">Format</span></span>

<span data-ttu-id="0b6c6-823">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-823">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-824">Pattern</span></span>

<span data-ttu-id="0b6c6-825">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-825">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-826">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-826">Checksum</span></span>

<span data-ttu-id="0b6c6-827">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-827">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-828">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-828">Definition</span></span>

<span data-ttu-id="0b6c6-829">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-829">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-830">регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-830">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-831">Ключевое слово из Keyword_canada_passport_number или Keyword_passport найти.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-831">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

``` 
<!-- Canada Passport Number -->
<Entity id="14d0db8b-498a-43ed-9fca-f6097ae687eb" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_canada_passport_number" />
          <Match idRef="Keyword_passport" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-832">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-832">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="0b6c6-833">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-833">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="0b6c6-834">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="0b6c6-834">canadian citizenship</span></span>
- <span data-ttu-id="0b6c6-835">
canadian passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-835">canadian passport</span></span>
- <span data-ttu-id="0b6c6-836">
passport application</span><span class="sxs-lookup"><span data-stu-id="0b6c6-836">passport application</span></span>
- <span data-ttu-id="0b6c6-837">
passport photos</span><span class="sxs-lookup"><span data-stu-id="0b6c6-837">passport photos</span></span>
- <span data-ttu-id="0b6c6-838">
certified translator</span><span class="sxs-lookup"><span data-stu-id="0b6c6-838">certified translator</span></span>
- <span data-ttu-id="0b6c6-839">
canadian citizens</span><span class="sxs-lookup"><span data-stu-id="0b6c6-839">canadian citizens</span></span>
- <span data-ttu-id="0b6c6-840">
processing times</span><span class="sxs-lookup"><span data-stu-id="0b6c6-840">processing times</span></span>
- <span data-ttu-id="0b6c6-841">

renewal application</span><span class="sxs-lookup"><span data-stu-id="0b6c6-841">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="0b6c6-842">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-842">Keyword_passport</span></span>

- <span data-ttu-id="0b6c6-843">Passport Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-843">Passport Number</span></span>
- <span data-ttu-id="0b6c6-844">
Passport No</span><span class="sxs-lookup"><span data-stu-id="0b6c6-844">Passport No</span></span>
- <span data-ttu-id="0b6c6-845">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-845">Passport #</span></span>
- <span data-ttu-id="0b6c6-846">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-846">Passport#</span></span>
- <span data-ttu-id="0b6c6-847">PassportID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-847">PassportID</span></span>
- <span data-ttu-id="0b6c6-848">Passportno
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-848">Passportno</span></span>
- <span data-ttu-id="0b6c6-849">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-849">passportnumber</span></span>
- <span data-ttu-id="0b6c6-850">パスポート</span><span class="sxs-lookup"><span data-stu-id="0b6c6-850">パスポート</span></span>
- <span data-ttu-id="0b6c6-851">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-851">パスポート番号</span></span>
- <span data-ttu-id="0b6c6-852">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-852">パスポートのNum</span></span>
- <span data-ttu-id="0b6c6-853">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-853">パスポート＃</span></span>
- <span data-ttu-id="0b6c6-854">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-854">Numéro de passeport</span></span>
- <span data-ttu-id="0b6c6-855">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="0b6c6-855">Passeport n °</span></span>
- <span data-ttu-id="0b6c6-856">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-856">Passeport Non</span></span>
- <span data-ttu-id="0b6c6-857">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-857">Passeport #</span></span>
- <span data-ttu-id="0b6c6-858">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-858">Passeport#</span></span>
- <span data-ttu-id="0b6c6-859">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="0b6c6-859">PasseportNon</span></span>
- <span data-ttu-id="0b6c6-860">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="0b6c6-860">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="0b6c6-861">Персональный идентификационный номер службы здравоохранения для Канады (PHIN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-861">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-862">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-862">Format</span></span>

<span data-ttu-id="0b6c6-863">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-863">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-864">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-864">Pattern</span></span>

<span data-ttu-id="0b6c6-865">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-865">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-866">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-866">Checksum</span></span>

<span data-ttu-id="0b6c6-867">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-867">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-868">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-868">Definition</span></span>

<span data-ttu-id="0b6c6-p104">Политики защиты от потери данных — 75% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: регулярное выражение Regex_canada_phin находит контент, который соответствует шаблону. По крайней мере два ключевых слов из Keyword_canada_phin или Keyword_canada_provinces находятся...</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```
<!-- Canada PHIN -->
<Entity id="722e12ac-c89a-4ec8-a1b7-fea3469f89db" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_canada_phin" />
        <Any minMatches="2">
          <Match idRef="Keyword_canada_phin" />
          <Match idRef="Keyword_canada_provinces" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-871">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-871">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="0b6c6-872">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="0b6c6-872">Keyword_canada_phin</span></span>

- <span data-ttu-id="0b6c6-873">social insurance number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-873">social insurance number</span></span>
- <span data-ttu-id="0b6c6-874">
health information act</span><span class="sxs-lookup"><span data-stu-id="0b6c6-874">health information act</span></span>
- <span data-ttu-id="0b6c6-875">
income tax information</span><span class="sxs-lookup"><span data-stu-id="0b6c6-875">income tax information</span></span>
- <span data-ttu-id="0b6c6-876">
manitoba health</span><span class="sxs-lookup"><span data-stu-id="0b6c6-876">manitoba health</span></span>
- <span data-ttu-id="0b6c6-877">
health registration</span><span class="sxs-lookup"><span data-stu-id="0b6c6-877">health registration</span></span>
- <span data-ttu-id="0b6c6-878">
prescription purchases</span><span class="sxs-lookup"><span data-stu-id="0b6c6-878">prescription purchases</span></span>
- <span data-ttu-id="0b6c6-879">
benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="0b6c6-879">benefit eligibility</span></span>
- <span data-ttu-id="0b6c6-880">
personal health</span><span class="sxs-lookup"><span data-stu-id="0b6c6-880">personal health</span></span>
- <span data-ttu-id="0b6c6-881">
power of attorney</span><span class="sxs-lookup"><span data-stu-id="0b6c6-881">power of attorney</span></span>
- <span data-ttu-id="0b6c6-882">
registration number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-882">registration number</span></span>
- <span data-ttu-id="0b6c6-883">personal health number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-883">personal health number</span></span>
- <span data-ttu-id="0b6c6-884">
practitioner referral</span><span class="sxs-lookup"><span data-stu-id="0b6c6-884">practitioner referral</span></span>
- <span data-ttu-id="0b6c6-885">
wellness professional</span><span class="sxs-lookup"><span data-stu-id="0b6c6-885">wellness professional</span></span>
- <span data-ttu-id="0b6c6-886">
patient referral</span><span class="sxs-lookup"><span data-stu-id="0b6c6-886">patient referral</span></span>
- <span data-ttu-id="0b6c6-887">

health and wellness</span><span class="sxs-lookup"><span data-stu-id="0b6c6-887">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="0b6c6-888">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="0b6c6-888">Keyword_canada_provinces</span></span>

- <span data-ttu-id="0b6c6-889">Nunavut</span><span class="sxs-lookup"><span data-stu-id="0b6c6-889">Nunavut</span></span>
- <span data-ttu-id="0b6c6-890">
Quebec</span><span class="sxs-lookup"><span data-stu-id="0b6c6-890">Quebec</span></span>
- <span data-ttu-id="0b6c6-891">
Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="0b6c6-891">Northwest Territories</span></span>
- <span data-ttu-id="0b6c6-892">
Ontario</span><span class="sxs-lookup"><span data-stu-id="0b6c6-892">Ontario</span></span>
- <span data-ttu-id="0b6c6-893">
British Columbia</span><span class="sxs-lookup"><span data-stu-id="0b6c6-893">British Columbia</span></span>
- <span data-ttu-id="0b6c6-894">
Alberta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-894">Alberta</span></span>
- <span data-ttu-id="0b6c6-895">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="0b6c6-895">Saskatchewan</span></span>
- <span data-ttu-id="0b6c6-896">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="0b6c6-896">Manitoba</span></span>
- <span data-ttu-id="0b6c6-897">
Yukon</span><span class="sxs-lookup"><span data-stu-id="0b6c6-897">Yukon</span></span>
- <span data-ttu-id="0b6c6-898">
Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="0b6c6-898">Newfoundland and Labrador</span></span>
- <span data-ttu-id="0b6c6-899">
New Brunswick</span><span class="sxs-lookup"><span data-stu-id="0b6c6-899">New Brunswick</span></span>
- <span data-ttu-id="0b6c6-900">
Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="0b6c6-900">Nova Scotia</span></span>
- <span data-ttu-id="0b6c6-901">
Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="0b6c6-901">Prince Edward Island</span></span>
- <span data-ttu-id="0b6c6-902">Канада</span><span class="sxs-lookup"><span data-stu-id="0b6c6-902">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="0b6c6-903">Номер карты социального страхования для Канады</span><span class="sxs-lookup"><span data-stu-id="0b6c6-903">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-904">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-904">Format</span></span>

<span data-ttu-id="0b6c6-905">Девять цифр с необязательными дефисами или пробелами.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-905">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-906">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-906">Pattern</span></span>

<span data-ttu-id="0b6c6-907">С форматированием</span><span class="sxs-lookup"><span data-stu-id="0b6c6-907">Formatted:</span></span>
- <span data-ttu-id="0b6c6-908">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-908">Three digits</span></span> 
- <span data-ttu-id="0b6c6-909">дефис или пробел; </span><span class="sxs-lookup"><span data-stu-id="0b6c6-909">A hyphen or space</span></span> 
- <span data-ttu-id="0b6c6-910">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-910">Three digits</span></span> 
- <span data-ttu-id="0b6c6-911">дефис или пробел; </span><span class="sxs-lookup"><span data-stu-id="0b6c6-911">A hyphen or space</span></span> 
- <span data-ttu-id="0b6c6-912">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-912">Three digits</span></span>

<span data-ttu-id="0b6c6-913">Неформатированный: Девяти цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-913">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-914">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-914">Checksum</span></span>

<span data-ttu-id="0b6c6-915">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-915">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-916">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-916">Definition</span></span>

<span data-ttu-id="0b6c6-917">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-917">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-918">Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-918">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-919">Выполняются по меньшей мере два из таких условий:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-919">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="0b6c6-920">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-920">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="0b6c6-921">найдено ключевое слово из Keyword_sin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-921">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="0b6c6-922">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-922">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="0b6c6-923">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-923">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-924">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-924">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-925">функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-925">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-926">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-926">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="0b6c6-927">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-927">The checksum passes.</span></span>

```
<!-- Canada Social Insurance Number -->
<Entity id="a2f29c85-ecb8-4514-a610-364790c0773e" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_canadian_sin" />
        <Any minMatches="2">
          <Match idRef="Keyword_sin" />
          <Match idRef="Keyword_sin_collaborative" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_canadian_sin" />
        <Match idRef="Keyword_sin" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-928">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-928">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="0b6c6-929">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="0b6c6-929">Keyword_sin</span></span>

- <span data-ttu-id="0b6c6-930">sin</span><span class="sxs-lookup"><span data-stu-id="0b6c6-930">sin</span></span> 
- <span data-ttu-id="0b6c6-931">social insurance
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-931">social insurance</span></span> 
- <span data-ttu-id="0b6c6-932">numero d'assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-932">numero d'assurance sociale</span></span> 
- <span data-ttu-id="0b6c6-933">sins
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-933">sins</span></span> 
- <span data-ttu-id="0b6c6-934">SSN</span><span class="sxs-lookup"><span data-stu-id="0b6c6-934">ssn</span></span> 
- <span data-ttu-id="0b6c6-935">ssNS</span><span class="sxs-lookup"><span data-stu-id="0b6c6-935">ssns</span></span> 
- <span data-ttu-id="0b6c6-936">социального страхования</span><span class="sxs-lookup"><span data-stu-id="0b6c6-936">social security</span></span> 
- <span data-ttu-id="0b6c6-937">numero d'assurance social
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-937">numero d'assurance social</span></span> 
- <span data-ttu-id="0b6c6-938">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0b6c6-938">national identification number</span></span> 
- <span data-ttu-id="0b6c6-939">
national id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-939">national id</span></span> 
- <span data-ttu-id="0b6c6-940">sin#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-940">sin#</span></span> 
- <span data-ttu-id="0b6c6-941">soc ins
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-941">soc ins</span></span> 
- <span data-ttu-id="0b6c6-942">social ins
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-942">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="0b6c6-943">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="0b6c6-943">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="0b6c6-944">driver's license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-944">driver's license</span></span> 
- <span data-ttu-id="0b6c6-945">drivers license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-945">drivers license</span></span> 
- <span data-ttu-id="0b6c6-946">Лицензия водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="0b6c6-946">driver's licence</span></span> 
- <span data-ttu-id="0b6c6-947">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-947">drivers licence</span></span> 
- <span data-ttu-id="0b6c6-948">DOB
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-948">DOB</span></span> 
- <span data-ttu-id="0b6c6-949">Birthdate</span><span class="sxs-lookup"><span data-stu-id="0b6c6-949">Birthdate</span></span> 
- <span data-ttu-id="0b6c6-950">День рождения </span><span class="sxs-lookup"><span data-stu-id="0b6c6-950">Birthday</span></span> 
- <span data-ttu-id="0b6c6-951">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-951">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="0b6c6-952">	Номер удостоверения личности для Чили</span><span class="sxs-lookup"><span data-stu-id="0b6c6-952">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-953">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-953">Format</span></span>

<span data-ttu-id="0b6c6-954">7-8 цифр, а также разделители контрольный разряд или буква</span><span class="sxs-lookup"><span data-stu-id="0b6c6-954">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-955">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-955">Pattern</span></span>

<span data-ttu-id="0b6c6-956">7–8 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-956">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="0b6c6-957">1 или 2 цифры;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-957">1-2 digits</span></span> 
- <span data-ttu-id="0b6c6-958">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-958">A period</span></span> 
- <span data-ttu-id="0b6c6-959">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-959">Three digits</span></span> 
- <span data-ttu-id="0b6c6-960">точка;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-960">A period</span></span> 
- <span data-ttu-id="0b6c6-961">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-961">Three digits</span></span> 
- <span data-ttu-id="0b6c6-962">Тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-962">A dash</span></span> 
- <span data-ttu-id="0b6c6-963">одна цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-963">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-964">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-964">Checksum</span></span>

<span data-ttu-id="0b6c6-965">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-966">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-966">Definition</span></span>

<span data-ttu-id="0b6c6-967">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-967">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-968">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-968">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-969">находится ключевое слово из Keyword_chile_id_card;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-969">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="0b6c6-970">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-970">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-971">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-971">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-972">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-972">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-973">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-973">The checksum passes.</span></span>

```
<!-- Chile Identity Card Number -->
<Entity id="4e979794-49a0-407e-a0b9-2c536937b925" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_chile_id_card"/>
     <Match idRef="Keyword_chile_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_chile_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-974">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-974">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="0b6c6-975">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-975">Keyword_chile_id_card</span></span>

- <span data-ttu-id="0b6c6-976">National Identification Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-976">National Identification Number</span></span> 
- <span data-ttu-id="0b6c6-977">Identity card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-977">Identity card</span></span> 
- <span data-ttu-id="0b6c6-978">ID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-978">ID</span></span> 
- <span data-ttu-id="0b6c6-979">Identification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-979">Identification</span></span> 
- <span data-ttu-id="0b6c6-980">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-980">Rol Único Nacional</span></span> 
- <span data-ttu-id="0b6c6-981">ЗАПУСК</span><span class="sxs-lookup"><span data-stu-id="0b6c6-981">RUN</span></span> 
- <span data-ttu-id="0b6c6-982">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-982">Rol Único Tributario</span></span> 
- <span data-ttu-id="0b6c6-983">RUT
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-983">RUT</span></span> 
- <span data-ttu-id="0b6c6-984">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-984">Cédula de Identidad</span></span> 
- <span data-ttu-id="0b6c6-985">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-985">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="0b6c6-986">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-986">Tarjeta de identificación</span></span> 
- <span data-ttu-id="0b6c6-987">Identificación
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-987">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="0b6c6-988">	Номер удостоверения личности жителя Китая (КНР)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-988">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-989">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-989">Format</span></span>

<span data-ttu-id="0b6c6-990">18 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-990">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-991">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-991">Pattern</span></span>

<span data-ttu-id="0b6c6-992">18 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-992">18 digits:</span></span>
- <span data-ttu-id="0b6c6-993">шесть цифр — код адреса;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-993">Six digits which are an address code</span></span> 
- <span data-ttu-id="0b6c6-994">восемь цифр в виде ГГГГММДД — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-994">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="0b6c6-995">три цифры — серия карты;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-995">Three digits which are an order code</span></span> 
- <span data-ttu-id="0b6c6-996">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-996">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-997">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-997">Checksum</span></span>

<span data-ttu-id="0b6c6-998">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-998">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-999">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-999">Definition</span></span>

<span data-ttu-id="0b6c6-1000">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1000">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1001">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1001">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1002">находится ключевое слово из Keyword_china_resident_id;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1002">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="0b6c6-1003">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1003">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-1004">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1005">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1005">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1006">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1006">The checksum passes.</span></span>

```
<!-- China Resident Identity Card (PRC) Number -->
<Entity id="c92daa86-2d16-4871-901f-816b3f554fc1" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_china_resident_id"/>
     <Match idRef="Keyword_china_resident_id"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_china_resident_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1007">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1007">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="0b6c6-1008">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1008">Keyword_china_resident_id</span></span>

- <span data-ttu-id="0b6c6-1009">Resident Identity Card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1009">Resident Identity Card</span></span> 
- <span data-ttu-id="0b6c6-1010">PRC
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1010">PRC</span></span> 
- <span data-ttu-id="0b6c6-1011">National Identification Card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1011">National Identification Card</span></span> 
- <span data-ttu-id="0b6c6-1012">身份证 </span><span class="sxs-lookup"><span data-stu-id="0b6c6-1012">身份证</span></span> 
- <span data-ttu-id="0b6c6-1013">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="0b6c6-1013">居民 身份证</span></span> 
- <span data-ttu-id="0b6c6-1014">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1014">居民身份证</span></span> 
- <span data-ttu-id="0b6c6-1015">鉴定

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1015">鉴定</span></span> 
- <span data-ttu-id="0b6c6-1016">身分證 </span><span class="sxs-lookup"><span data-stu-id="0b6c6-1016">身分證</span></span> 
- <span data-ttu-id="0b6c6-1017">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1017">居民 身份證</span></span>
- <span data-ttu-id="0b6c6-1018">鑑定 </span><span class="sxs-lookup"><span data-stu-id="0b6c6-1018">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="0b6c6-1019">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1019">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1020">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1020">Format</span></span>

<span data-ttu-id="0b6c6-1021">16 цифр, которые могут иметь формат или неформатированные (dddddddddddddddd) и должно пройти проверку Luhn.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1021">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1022">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1022">Pattern</span></span>

<span data-ttu-id="0b6c6-1023">Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1023">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1024">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1024">Checksum</span></span>

<span data-ttu-id="0b6c6-1025">Да (рассчитывается по алгоритму Луна).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1025">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1026">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1026">Definition</span></span>

<span data-ttu-id="0b6c6-1027">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1027">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1028">Функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1028">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1029">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1029">One of the following is true:</span></span>
    - <span data-ttu-id="0b6c6-1030">найдено ключевое слово из Keyword_cc_verification;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1030">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="0b6c6-1031">найдено ключевое слово из Keyword_cc_name;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1031">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="0b6c6-1032">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1032">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="0b6c6-1033">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1033">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-1034">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1034">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1035">функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1035">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1036">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1036">The checksum passes.</span></span>

```
<!-- Credit Card Number -->
<Entity id="50842eb7-edc8-4019-85dd-5a5c1f2bb085" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_credit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_cc_verification" />
          <Match idRef="Keyword_cc_name" />
          <Match idRef="Func_expiration_date" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_credit_card" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1037">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1037">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="0b6c6-1038">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1038">Keyword_cc_verification</span></span>

- <span data-ttu-id="0b6c6-1039">card verification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1039">card verification</span></span>
- <span data-ttu-id="0b6c6-1040">card identification number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1040">card identification number</span></span>
- <span data-ttu-id="0b6c6-1041">cvn
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1041">cvn</span></span>
- <span data-ttu-id="0b6c6-1042">cid
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1042">cid</span></span>
- <span data-ttu-id="0b6c6-1043">cvc2</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1043">cvc2</span></span>
- <span data-ttu-id="0b6c6-1044">cvv2</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1044">cvv2</span></span>
- <span data-ttu-id="0b6c6-1045">pin block
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1045">pin block</span></span>
- <span data-ttu-id="0b6c6-1046">security code
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1046">security code</span></span>
- <span data-ttu-id="0b6c6-1047">security number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1047">security number</span></span>
- <span data-ttu-id="0b6c6-1048">security no
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1048">security no</span></span>
- <span data-ttu-id="0b6c6-1049">issue number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1049">issue number</span></span>
- <span data-ttu-id="0b6c6-1050">issue no
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1050">issue no</span></span>
- <span data-ttu-id="0b6c6-1051">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1051">cryptogramme</span></span>
- <span data-ttu-id="0b6c6-1052">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1052">numéro de sécurité</span></span>
- <span data-ttu-id="0b6c6-1053">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1053">numero de securite</span></span>
- <span data-ttu-id="0b6c6-1054">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1054">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="0b6c6-1055">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1055">kreditkartenprufnummer</span></span>
- <span data-ttu-id="0b6c6-1056">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1056">prüfziffer</span></span>
- <span data-ttu-id="0b6c6-1057">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1057">prufziffer</span></span>
- <span data-ttu-id="0b6c6-1058">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1058">sicherheits Kode</span></span>
- <span data-ttu-id="0b6c6-1059">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1059">sicherheitscode</span></span>
- <span data-ttu-id="0b6c6-1060">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1060">sicherheitsnummer</span></span>
- <span data-ttu-id="0b6c6-1061">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1061">verfalldatum</span></span>
- <span data-ttu-id="0b6c6-1062">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1062">codice di verifica</span></span>
- <span data-ttu-id="0b6c6-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p105">cod. sicurezza</span></span>
- <span data-ttu-id="0b6c6-1065">COD sicurezza</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1065">cod sicurezza</span></span>
- <span data-ttu-id="0b6c6-1066">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1066">n autorizzazione</span></span>
- <span data-ttu-id="0b6c6-1067">código
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1067">código</span></span>
- <span data-ttu-id="0b6c6-1068">codigo
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1068">codigo</span></span>
- <span data-ttu-id="0b6c6-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p106">cod. seg</span></span>
- <span data-ttu-id="0b6c6-1071">COD seg</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1071">cod seg</span></span>
- <span data-ttu-id="0b6c6-1072">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1072">código de segurança</span></span>
- <span data-ttu-id="0b6c6-1073">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1073">codigo de seguranca</span></span>
- <span data-ttu-id="0b6c6-1074">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1074">codigo de segurança</span></span>
- <span data-ttu-id="0b6c6-1075">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1075">código de seguranca</span></span>
- <span data-ttu-id="0b6c6-p107">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p107">cód. segurança</span></span>
- <span data-ttu-id="0b6c6-p108">COD. seguranca cod. segurança</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="0b6c6-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p109">cód. seguranca</span></span>
- <span data-ttu-id="0b6c6-1083">cód segurança</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1083">cód segurança</span></span>
- <span data-ttu-id="0b6c6-1084">решить seguranca cod segurança</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1084">cod seguranca cod segurança</span></span>
- <span data-ttu-id="0b6c6-1085">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1085">cód seguranca</span></span>
- <span data-ttu-id="0b6c6-1086">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1086">número de verificação</span></span>
- <span data-ttu-id="0b6c6-1087">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1087">numero de verificacao</span></span>
- <span data-ttu-id="0b6c6-1088">ablauf
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1088">ablauf</span></span>
- <span data-ttu-id="0b6c6-1089">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1089">gültig bis</span></span>
- <span data-ttu-id="0b6c6-1090">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1090">gültigkeitsdatum</span></span>
- <span data-ttu-id="0b6c6-1091">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1091">gultig bis</span></span>
- <span data-ttu-id="0b6c6-1092">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1092">gultigkeitsdatum</span></span>
- <span data-ttu-id="0b6c6-1093">scadenza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1093">scadenza</span></span>
- <span data-ttu-id="0b6c6-1094">data scad
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1094">data scad</span></span>
- <span data-ttu-id="0b6c6-1095">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1095">fecha de expiracion</span></span>
- <span data-ttu-id="0b6c6-1096">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1096">fecha de venc</span></span>
- <span data-ttu-id="0b6c6-1097">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1097">vencimiento</span></span>
- <span data-ttu-id="0b6c6-1098">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1098">válido hasta</span></span>
- <span data-ttu-id="0b6c6-1099">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1099">valido hasta</span></span>
- <span data-ttu-id="0b6c6-1100">vto
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1100">vto</span></span>
- <span data-ttu-id="0b6c6-1101">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1101">data de expiração</span></span>
- <span data-ttu-id="0b6c6-1102">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1102">data de expiracao</span></span>
- <span data-ttu-id="0b6c6-1103">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1103">data em que expira</span></span>
- <span data-ttu-id="0b6c6-1104">validade
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1104">validade</span></span>
- <span data-ttu-id="0b6c6-1105">valor
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1105">valor</span></span>
- <span data-ttu-id="0b6c6-1106">vencimento
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1106">vencimento</span></span>
- <span data-ttu-id="0b6c6-1107">Venc</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1107">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="0b6c6-1108">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1108">Keyword_cc_name</span></span>

- <span data-ttu-id="0b6c6-1109">amex</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1109">amex</span></span>
- <span data-ttu-id="0b6c6-1110">
american express</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1110">american express</span></span>
- <span data-ttu-id="0b6c6-1111">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1111">americanexpress</span></span>
- <span data-ttu-id="0b6c6-1112">Visa</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1112">Visa</span></span>
- <span data-ttu-id="0b6c6-1113">mastercard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1113">mastercard</span></span>
- <span data-ttu-id="0b6c6-1114">master card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1114">master card</span></span>
- <span data-ttu-id="0b6c6-1115">
mc
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1115">mc</span></span> 
- <span data-ttu-id="0b6c6-1116">mastercards</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1116">mastercards</span></span>
- <span data-ttu-id="0b6c6-1117">
master cards</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1117">master cards</span></span>
- <span data-ttu-id="0b6c6-1118">в diner клуба</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1118">diner's Club</span></span>
- <span data-ttu-id="0b6c6-1119">diners club
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1119">diners club</span></span>
- <span data-ttu-id="0b6c6-1120">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1120">dinersclub</span></span>
- <span data-ttu-id="0b6c6-1121">discover card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1121">discover card</span></span>
- <span data-ttu-id="0b6c6-1122">discovercard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1122">discovercard</span></span>
- <span data-ttu-id="0b6c6-1123">discover cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1123">discover cards</span></span>
- <span data-ttu-id="0b6c6-1124">JCB</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1124">JCB</span></span>
- <span data-ttu-id="0b6c6-1125">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1125">japanese card bureau</span></span>
- <span data-ttu-id="0b6c6-1126">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1126">carte blanche</span></span>
- <span data-ttu-id="0b6c6-1127">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1127">carteblanche</span></span>
- <span data-ttu-id="0b6c6-1128">credit card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1128">credit card</span></span>
- <span data-ttu-id="0b6c6-1129">CC #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1129">cc#</span></span>
- <span data-ttu-id="0b6c6-1130">cc #:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1130">cc#:</span></span>
- <span data-ttu-id="0b6c6-1131">
expiration date</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1131">expiration date</span></span>
- <span data-ttu-id="0b6c6-1132">exp date
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1132">exp date</span></span>
- <span data-ttu-id="0b6c6-1133">
expiry date</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1133">expiry date</span></span>
- <span data-ttu-id="0b6c6-1134">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1134">date d’expiration</span></span>
- <span data-ttu-id="0b6c6-1135">
date d'exp</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1135">date d'exp</span></span>
- <span data-ttu-id="0b6c6-1136">
date expiration</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1136">date expiration</span></span>
- <span data-ttu-id="0b6c6-1137">bank card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1137">bank card</span></span>
- <span data-ttu-id="0b6c6-1138">
bankcard</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1138">bankcard</span></span>
- <span data-ttu-id="0b6c6-1139">card number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1139">card number</span></span>
- <span data-ttu-id="0b6c6-1140">card num
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1140">card num</span></span>
- <span data-ttu-id="0b6c6-1141">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1141">cardnumber</span></span>
- <span data-ttu-id="0b6c6-1142">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1142">cardnumbers</span></span>
- <span data-ttu-id="0b6c6-1143">card numbers
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1143">card numbers</span></span>
- <span data-ttu-id="0b6c6-1144">creditcard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1144">creditcard</span></span>
- <span data-ttu-id="0b6c6-1145">credit cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1145">credit cards</span></span>
- <span data-ttu-id="0b6c6-1146">creditcards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1146">creditcards</span></span>
- <span data-ttu-id="0b6c6-1147">ccn
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1147">ccn</span></span>
- <span data-ttu-id="0b6c6-1148">card holder
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1148">card holder</span></span>
- <span data-ttu-id="0b6c6-1149">cardholder
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1149">cardholder</span></span>
- <span data-ttu-id="0b6c6-1150">card holders
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1150">card holders</span></span>
- <span data-ttu-id="0b6c6-1151">cardholders
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1151">cardholders</span></span>
- <span data-ttu-id="0b6c6-1152">check card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1152">check card</span></span>
- <span data-ttu-id="0b6c6-1153">checkcard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1153">checkcard</span></span>
- <span data-ttu-id="0b6c6-1154">check cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1154">check cards</span></span>
- <span data-ttu-id="0b6c6-1155">checkcards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1155">checkcards</span></span>
- <span data-ttu-id="0b6c6-1156">debit card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1156">debit card</span></span>
- <span data-ttu-id="0b6c6-1157">debitcard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1157">debitcard</span></span>
- <span data-ttu-id="0b6c6-1158">debit cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1158">debit cards</span></span>
- <span data-ttu-id="0b6c6-1159">debitcards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1159">debitcards</span></span>
- <span data-ttu-id="0b6c6-1160">atm card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1160">atm card</span></span>
- <span data-ttu-id="0b6c6-1161">atmcard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1161">atmcard</span></span>
- <span data-ttu-id="0b6c6-1162">atm cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1162">atm cards</span></span>
- <span data-ttu-id="0b6c6-1163">atmcards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1163">atmcards</span></span>
- <span data-ttu-id="0b6c6-1164">
enroute</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1164">enroute</span></span>
- <span data-ttu-id="0b6c6-1165">
en route</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1165">en route</span></span>
- <span data-ttu-id="0b6c6-1166">card type
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1166">card type</span></span>
- <span data-ttu-id="0b6c6-1167">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1167">carte bancaire</span></span>
- <span data-ttu-id="0b6c6-1168">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1168">carte de crédit</span></span>
- <span data-ttu-id="0b6c6-1169">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1169">carte de credit</span></span>
- <span data-ttu-id="0b6c6-1170">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1170">numéro de carte</span></span>
- <span data-ttu-id="0b6c6-1171">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1171">numero de carte</span></span>
- <span data-ttu-id="0b6c6-1172">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1172">nº de la carte</span></span>
- <span data-ttu-id="0b6c6-1173">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1173">nº de carte</span></span>
- <span data-ttu-id="0b6c6-1174">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1174">kreditkarte</span></span>
- <span data-ttu-id="0b6c6-1175">karte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1175">karte</span></span>
- <span data-ttu-id="0b6c6-1176">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1176">karteninhaber</span></span>
- <span data-ttu-id="0b6c6-1177">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1177">karteninhabers</span></span>
- <span data-ttu-id="0b6c6-1178">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1178">kreditkarteninhaber</span></span>
- <span data-ttu-id="0b6c6-1179">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1179">kreditkarteninstitut</span></span>
- <span data-ttu-id="0b6c6-1180">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1180">kreditkartentyp</span></span>
- <span data-ttu-id="0b6c6-1181">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1181">eigentümername</span></span>
- <span data-ttu-id="0b6c6-1182">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1182">kartennr</span></span> 
- <span data-ttu-id="0b6c6-1183">kartennummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1183">kartennummer</span></span>
- <span data-ttu-id="0b6c6-1184">
kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1184">kreditkartennummer</span></span>
- <span data-ttu-id="0b6c6-1185">kreditkarten nummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1185">kreditkarten-nummer</span></span>
- <span data-ttu-id="0b6c6-1186">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1186">carta di credito</span></span>
- <span data-ttu-id="0b6c6-1187">carta credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1187">carta credito</span></span>
- <span data-ttu-id="0b6c6-1188">carta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1188">carta</span></span>
- <span data-ttu-id="0b6c6-1189">n carta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1189">n carta</span></span>
- <span data-ttu-id="0b6c6-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p110">nr. carta</span></span>
- <span data-ttu-id="0b6c6-1192">nr carta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1192">nr carta</span></span>
- <span data-ttu-id="0b6c6-1193">numero carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1193">numero carta</span></span>
- <span data-ttu-id="0b6c6-1194">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1194">numero della carta</span></span>
- <span data-ttu-id="0b6c6-1195">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1195">numero di carta</span></span>
- <span data-ttu-id="0b6c6-1196">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1196">tarjeta credito</span></span>
- <span data-ttu-id="0b6c6-1197">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1197">tarjeta de credito</span></span>
- <span data-ttu-id="0b6c6-1198">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1198">tarjeta crédito</span></span>
- <span data-ttu-id="0b6c6-1199">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1199">tarjeta de crédito</span></span>
- <span data-ttu-id="0b6c6-1200">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1200">tarjeta de atm</span></span>
- <span data-ttu-id="0b6c6-1201">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1201">tarjeta atm</span></span>
- <span data-ttu-id="0b6c6-1202">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1202">tarjeta debito</span></span>
- <span data-ttu-id="0b6c6-1203">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1203">tarjeta de debito</span></span>
- <span data-ttu-id="0b6c6-1204">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1204">tarjeta débito</span></span>
- <span data-ttu-id="0b6c6-1205">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1205">tarjeta de débito</span></span>
- <span data-ttu-id="0b6c6-1206">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1206">nº de tarjeta</span></span>
- <span data-ttu-id="0b6c6-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p111">no. de tarjeta</span></span>
- <span data-ttu-id="0b6c6-1209">Не де tarjeta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1209">no de tarjeta</span></span>
- <span data-ttu-id="0b6c6-1210">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1210">numero de tarjeta</span></span>
- <span data-ttu-id="0b6c6-1211">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1211">número de tarjeta</span></span>
- <span data-ttu-id="0b6c6-1212">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1212">tarjeta no</span></span>
- <span data-ttu-id="0b6c6-1213">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1213">tarjetahabiente</span></span>
- <span data-ttu-id="0b6c6-1214">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1214">cartão de crédito</span></span>
- <span data-ttu-id="0b6c6-1215">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1215">cartão de credito</span></span>
- <span data-ttu-id="0b6c6-1216">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1216">cartao de crédito</span></span>
- <span data-ttu-id="0b6c6-1217">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1217">cartao de credito</span></span>
- <span data-ttu-id="0b6c6-1218">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1218">cartão de débito</span></span>
- <span data-ttu-id="0b6c6-1219">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1219">cartao de débito</span></span>
- <span data-ttu-id="0b6c6-1220">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1220">cartão de debito</span></span>
- <span data-ttu-id="0b6c6-1221">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1221">cartao de debito</span></span>
- <span data-ttu-id="0b6c6-1222">débito automático</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1222">débito automático</span></span>
- <span data-ttu-id="0b6c6-1223">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1223">debito automatico</span></span>
- <span data-ttu-id="0b6c6-1224">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1224">número do cartão</span></span>
- <span data-ttu-id="0b6c6-1225">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1225">numero do cartão</span></span> 
- <span data-ttu-id="0b6c6-1226">número do cartao</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1226">número do cartao</span></span>
- <span data-ttu-id="0b6c6-1227">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1227">numero do cartao</span></span>
- <span data-ttu-id="0b6c6-1228">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1228">número de cartão</span></span>
- <span data-ttu-id="0b6c6-1229">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1229">numero de cartão</span></span>
- <span data-ttu-id="0b6c6-1230">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1230">número de cartao</span></span>
- <span data-ttu-id="0b6c6-1231">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1231">numero de cartao</span></span>
- <span data-ttu-id="0b6c6-1232">Действие cartão nº</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1232">nº do cartão</span></span>
- <span data-ttu-id="0b6c6-1233">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1233">nº do cartao</span></span>
- <span data-ttu-id="0b6c6-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p112">nº. do cartão</span></span>
- <span data-ttu-id="0b6c6-1236">не cartão действие</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1236">no do cartão</span></span>
- <span data-ttu-id="0b6c6-1237">не cartao действие</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1237">no do cartao</span></span>
- <span data-ttu-id="0b6c6-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p113">no. do cartão</span></span>
- <span data-ttu-id="0b6c6-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="0b6c6-1242">	Номер удостоверения личности для Хорватии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1242">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1243">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1243">Format</span></span>

<span data-ttu-id="0b6c6-1244">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1245">Pattern</span></span>

<span data-ttu-id="0b6c6-1246">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1247">Checksum</span></span>

<span data-ttu-id="0b6c6-1248">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1248">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1249">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1249">Definition</span></span>

<span data-ttu-id="0b6c6-1250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1251">функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1251">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1252">находится ключевое слово из Keyword_croatia_id_card.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1252">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1253">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1253">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="0b6c6-1254">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1254">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="0b6c6-1255">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1255">Croatian identity card</span></span>
- <span data-ttu-id="0b6c6-1256">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1256">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="0b6c6-1257">	Индивидуальный идентификационный номер (OIB) для Хорватии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1257">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1258">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1258">Format</span></span>

<span data-ttu-id="0b6c6-1259">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1259">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1260">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1260">Pattern</span></span>

<span data-ttu-id="0b6c6-1261">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1261">11 digits:</span></span>
- <span data-ttu-id="0b6c6-1262">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1262">10 digits</span></span> 
- <span data-ttu-id="0b6c6-1263">Окончательный цифра — это цифра возврата в целях международных данных exchange, букв отдела Кадров добавляются предыдущих одиннадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1263">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1264">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1264">Checksum</span></span>

<span data-ttu-id="0b6c6-1265">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1265">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1266">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1266">Definition</span></span>

<span data-ttu-id="0b6c6-1267">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1267">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1268">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1268">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1269">находится ключевое слово из Keyword_croatia_oib_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1269">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="0b6c6-1270">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1270">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-1271">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1272">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1272">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1273">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1273">The checksum passes.</span></span>

```
<!-- Croatia Personal Identification (OIB) Number -->
<Entity id="31983b6d-db95-4eb2-a630-b44bd091968d" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_croatia_oib_number"/>
     <Match idRef="Keyword_croatia_oib_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_oib_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1274">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1274">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="0b6c6-1275">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1275">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="0b6c6-1276">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1276">Personal Identification Number</span></span>
- <span data-ttu-id="0b6c6-1277">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1277">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="0b6c6-1278">OIB
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1278">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="0b6c6-1279">Чешский личные номер</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1279">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1280">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1280">Format</span></span>

<span data-ttu-id="0b6c6-1281">Девяти цифр с необязательным косая черта (старый формат) 10 цифр и необязательные косая черта (новый формат)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1281">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1282">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1282">Pattern</span></span>

<span data-ttu-id="0b6c6-1283">Девяти цифр (старый формат):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1283">Nine digits (old format):</span></span>
- <span data-ttu-id="0b6c6-1284">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1284">Nine digits</span></span>

<span data-ttu-id="0b6c6-1285">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1285">OR</span></span>

- <span data-ttu-id="0b6c6-1286">Шести цифр, представляющих Дата рождения</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1286">Six digits that represent date of birth</span></span>
- <span data-ttu-id="0b6c6-1287">косая черта;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1287">A forward slash</span></span>
- <span data-ttu-id="0b6c6-1288">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1288">Three digits</span></span>

<span data-ttu-id="0b6c6-1289">10 цифр (новый формат):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1289">10 digits (new format):</span></span>
- <span data-ttu-id="0b6c6-1290">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1290">10 digits</span></span>

<span data-ttu-id="0b6c6-1291">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1291">OR</span></span>

- <span data-ttu-id="0b6c6-1292">Шести цифр, представляющих Дата рождения</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1292">Six digits that represent date of birth</span></span>
- <span data-ttu-id="0b6c6-1293">косая черта;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1293">A forward slash</span></span> 
- <span data-ttu-id="0b6c6-1294">Четыре цифры, где последнего цифра — это цифра проверки</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1294">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1295">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1295">Checksum</span></span>

<span data-ttu-id="0b6c6-1296">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1296">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1297">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1297">Definition</span></span>

<span data-ttu-id="0b6c6-p115">Политика защиты от потери данных — это 85% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: Func_czech_id_card поиска контента, который соответствует шаблону. Ключевое слово из Keyword_czech_id_card найти. Контрольная сумма передает.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="0b6c6-1301">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1301">Keywords</span></span>

- <span data-ttu-id="0b6c6-1302">Чешский личные номер</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1302">czech personal identity number</span></span>
- <span data-ttu-id="0b6c6-1303">Rodné číslo</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1303">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="0b6c6-1304">	Индивидуальный идентификационный номер для Дании</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1304">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1305">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1305">Format</span></span>

<span data-ttu-id="0b6c6-1306">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1306">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1307">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1307">Pattern</span></span>

<span data-ttu-id="0b6c6-1308">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1308">10 digits:</span></span>
- <span data-ttu-id="0b6c6-1309">шесть цифр в формате ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1309">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="0b6c6-1310">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1310">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-1311">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1311">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1312">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1312">Checksum</span></span>

<span data-ttu-id="0b6c6-1313">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1314">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1314">Definition</span></span>

<span data-ttu-id="0b6c6-p116">Политики защиты от потери данных — 75% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: регулярное выражение Regex_denmark_id находит контент, который соответствует шаблону. Ключевое слово из Keyword_denmark_id найти. Контрольная сумма передает.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1318">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1318">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="0b6c6-1319">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1319">Keyword_denmark_id</span></span>

- <span data-ttu-id="0b6c6-1320">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1320">Personal Identification Number</span></span>
- <span data-ttu-id="0b6c6-1321">CPR</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1321">CPR</span></span>
- <span data-ttu-id="0b6c6-1322">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1322">Det Centrale Personregister</span></span>
- <span data-ttu-id="0b6c6-1323">Personnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1323">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="0b6c6-1324">Номер Управления по борьбе с наркотиками США (DEA)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1324">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1325">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1325">Format</span></span>

<span data-ttu-id="0b6c6-1326">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1326">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1327">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1327">Pattern</span></span>

<span data-ttu-id="0b6c6-1328">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1328">Pattern must include all of the following:</span></span>
- <span data-ttu-id="0b6c6-1329">Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1329">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="0b6c6-1330">Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1330">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="0b6c6-1331">Семь цифр, последняя из которых — контрольная</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1331">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1332">Checksum</span></span>

<span data-ttu-id="0b6c6-1333">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1333">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1334">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1334">Definition</span></span>

<span data-ttu-id="0b6c6-1335">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1335">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1336">функция Func_dea_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1336">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1337">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1337">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1338">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1338">Keywords</span></span>

<span data-ttu-id="0b6c6-1339">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1339">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="0b6c6-1340">Номер банковской карты для ЕС</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1340">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1341">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1341">Format</span></span>

<span data-ttu-id="0b6c6-1342">16 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1342">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1343">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1343">Pattern</span></span>

<span data-ttu-id="0b6c6-1344">Очень сложный и надежный шаблон.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1344">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1345">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1345">Checksum</span></span>

<span data-ttu-id="0b6c6-1346">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1346">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1347">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1347">Definition</span></span>

<span data-ttu-id="0b6c6-1348">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1348">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1349">Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1349">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1350">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1350">At least one of the following is true:</span></span>
    - <span data-ttu-id="0b6c6-1351">найдено ключевое слово из Keyword_eu_debit_card;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1351">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="0b6c6-1352">найдено ключевое слово из Keyword_card_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1352">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="0b6c6-1353">найдено ключевое слово из Keyword_card_security_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1353">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="0b6c6-1354">найдено ключевое слово из Keyword_card_expiration_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1354">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="0b6c6-1355">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1355">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="0b6c6-1356">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1356">The checksum passes.</span></span>

```
    <!-- EU Debit Card Number -->
    <Entity id="0e9b3178-9678-47dd-a509-37222ca96b42" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_eu_debit_card" />
        <Any minMatches="1">
          <Match idRef="Keyword_eu_debit_card" />
          <Match idRef="Keyword_card_terms_dict" />
          <Match idRef="Keyword_card_security_terms_dict" />
          <Match idRef="Keyword_card_expiration_terms_dict" />
          <Match idRef="Func_expiration_date" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1357">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1357">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="0b6c6-1358">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1358">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="0b6c6-1359">Номер счета</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1359">account number</span></span> 
- <span data-ttu-id="0b6c6-1360">card number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1360">card number</span></span> 
- <span data-ttu-id="0b6c6-1361">card no.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1361">card no.</span></span> 
- <span data-ttu-id="0b6c6-1362">security number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1362">security number</span></span> 
- <span data-ttu-id="0b6c6-1363">CC #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1363">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="0b6c6-1364">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1364">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="0b6c6-1365">acct nbr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1365">acct nbr</span></span> 
- <span data-ttu-id="0b6c6-1366">acct num
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1366">acct num</span></span> 
- <span data-ttu-id="0b6c6-1367">acct no
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1367">acct no</span></span> 
- <span data-ttu-id="0b6c6-1368">american express
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1368">american express</span></span> 
- <span data-ttu-id="0b6c6-1369">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1369">americanexpress</span></span> 
- <span data-ttu-id="0b6c6-1370">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1370">americano espresso</span></span> 
- <span data-ttu-id="0b6c6-1371">amex</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1371">amex</span></span> 
- <span data-ttu-id="0b6c6-1372">atm card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1372">atm card</span></span> 
- <span data-ttu-id="0b6c6-1373">atm cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1373">atm cards</span></span> 
- <span data-ttu-id="0b6c6-1374">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1374">atm kaart</span></span> 
- <span data-ttu-id="0b6c6-1375">atmcard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1375">atmcard</span></span> 
- <span data-ttu-id="0b6c6-1376">atmcards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1376">atmcards</span></span> 
- <span data-ttu-id="0b6c6-1377">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1377">atmkaart</span></span> 
- <span data-ttu-id="0b6c6-1378">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1378">atmkaarten</span></span> 
- <span data-ttu-id="0b6c6-1379">bancontact
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1379">bancontact</span></span> 
- <span data-ttu-id="0b6c6-1380">bank card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1380">bank card</span></span> 
- <span data-ttu-id="0b6c6-1381">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1381">bankkaart</span></span> 
- <span data-ttu-id="0b6c6-1382">card holder
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1382">card holder</span></span> 
- <span data-ttu-id="0b6c6-1383">card holders
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1383">card holders</span></span> 
- <span data-ttu-id="0b6c6-1384">card num
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1384">card num</span></span> 
- <span data-ttu-id="0b6c6-1385">card number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1385">card number</span></span> 
- <span data-ttu-id="0b6c6-1386">card numbers
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1386">card numbers</span></span> 
- <span data-ttu-id="0b6c6-1387">card type
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1387">card type</span></span> 
- <span data-ttu-id="0b6c6-1388">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1388">cardano numerico</span></span> 
- <span data-ttu-id="0b6c6-1389">cardholder
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1389">cardholder</span></span> 
- <span data-ttu-id="0b6c6-1390">cardholders
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1390">cardholders</span></span> 
- <span data-ttu-id="0b6c6-1391">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1391">cardnumber</span></span> 
- <span data-ttu-id="0b6c6-1392">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1392">cardnumbers</span></span> 
- <span data-ttu-id="0b6c6-1393">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1393">carta bianca</span></span> 
- <span data-ttu-id="0b6c6-1394">carta credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1394">carta credito</span></span> 
- <span data-ttu-id="0b6c6-1395">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1395">carta di credito</span></span> 
- <span data-ttu-id="0b6c6-1396">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1396">cartao de credito</span></span> 
- <span data-ttu-id="0b6c6-1397">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1397">cartao de crédito</span></span> 
- <span data-ttu-id="0b6c6-1398">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1398">cartao de debito</span></span> 
- <span data-ttu-id="0b6c6-1399">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1399">cartao de débito</span></span> 
- <span data-ttu-id="0b6c6-1400">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1400">carte bancaire</span></span> 
- <span data-ttu-id="0b6c6-1401">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1401">carte blanche</span></span> 
- <span data-ttu-id="0b6c6-1402">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1402">carte bleue</span></span> 
- <span data-ttu-id="0b6c6-1403">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1403">carte de credit</span></span> 
- <span data-ttu-id="0b6c6-1404">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1404">carte de crédit</span></span> 
- <span data-ttu-id="0b6c6-1405">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1405">carte di credito</span></span> 
- <span data-ttu-id="0b6c6-1406">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1406">carteblanche</span></span> 
- <span data-ttu-id="0b6c6-1407">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1407">cartão de credito</span></span> 
- <span data-ttu-id="0b6c6-1408">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1408">cartão de crédito</span></span> 
- <span data-ttu-id="0b6c6-1409">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1409">cartão de debito</span></span> 
- <span data-ttu-id="0b6c6-1410">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1410">cartão de débito</span></span> 
- <span data-ttu-id="0b6c6-1411">cb
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1411">cb</span></span> 
- <span data-ttu-id="0b6c6-1412">ccn
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1412">ccn</span></span> 
- <span data-ttu-id="0b6c6-1413">check card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1413">check card</span></span> 
- <span data-ttu-id="0b6c6-1414">check cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1414">check cards</span></span> 
- <span data-ttu-id="0b6c6-1415">checkcard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1415">checkcard</span></span>
- <span data-ttu-id="0b6c6-1416">checkcards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1416">checkcards</span></span> 
- <span data-ttu-id="0b6c6-1417">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1417">chequekaart</span></span> 
- <span data-ttu-id="0b6c6-1418">cirrus
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1418">cirrus</span></span> 
- <span data-ttu-id="0b6c6-1419">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1419">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="0b6c6-1420">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1420">controlekaart</span></span> 
- <span data-ttu-id="0b6c6-1421">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1421">controlekaarten</span></span> 
- <span data-ttu-id="0b6c6-1422">credit card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1422">credit card</span></span> 
- <span data-ttu-id="0b6c6-1423">credit cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1423">credit cards</span></span> 
- <span data-ttu-id="0b6c6-1424">creditcard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1424">creditcard</span></span> 
- <span data-ttu-id="0b6c6-1425">creditcards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1425">creditcards</span></span> 
- <span data-ttu-id="0b6c6-1426">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1426">debetkaart</span></span> 
- <span data-ttu-id="0b6c6-1427">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1427">debetkaarten</span></span> 
- <span data-ttu-id="0b6c6-1428">debit card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1428">debit card</span></span> 
- <span data-ttu-id="0b6c6-1429">debit cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1429">debit cards</span></span> 
- <span data-ttu-id="0b6c6-1430">debitcard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1430">debitcard</span></span> 
- <span data-ttu-id="0b6c6-1431">debitcards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1431">debitcards</span></span> 
- <span data-ttu-id="0b6c6-1432">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1432">debito automatico</span></span> 
- <span data-ttu-id="0b6c6-1433">diners club
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1433">diners club</span></span> 
- <span data-ttu-id="0b6c6-1434">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1434">dinersclub</span></span> 
- <span data-ttu-id="0b6c6-1435">обнаружение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1435">discover</span></span> 
- <span data-ttu-id="0b6c6-1436">discover card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1436">discover card</span></span> 
- <span data-ttu-id="0b6c6-1437">discover cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1437">discover cards</span></span> 
- <span data-ttu-id="0b6c6-1438">discovercard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1438">discovercard</span></span> 
- <span data-ttu-id="0b6c6-1439">discovercards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1439">discovercards</span></span> 
- <span data-ttu-id="0b6c6-1440">débito automático</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1440">débito automático</span></span>
- <span data-ttu-id="0b6c6-1441">
edc
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1441">edc</span></span> 
- <span data-ttu-id="0b6c6-1442">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1442">eigentümername</span></span> 
- <span data-ttu-id="0b6c6-1443">european debit card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1443">european debit card</span></span> 
- <span data-ttu-id="0b6c6-1444">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1444">hoofdkaart</span></span> 
- <span data-ttu-id="0b6c6-1445">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1445">hoofdkaarten</span></span> 
- <span data-ttu-id="0b6c6-1446">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1446">in viaggio</span></span> 
- <span data-ttu-id="0b6c6-1447">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1447">japanese card bureau</span></span> 
- <span data-ttu-id="0b6c6-1448">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1448">japanse kaartdienst</span></span> 
- <span data-ttu-id="0b6c6-1449">jcb
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1449">jcb</span></span> 
- <span data-ttu-id="0b6c6-1450">kaart
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1450">kaart</span></span> 
- <span data-ttu-id="0b6c6-1451">kaart num
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1451">kaart num</span></span> 
- <span data-ttu-id="0b6c6-1452">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1452">kaartaantal</span></span> 
- <span data-ttu-id="0b6c6-1453">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1453">kaartaantallen</span></span> 
- <span data-ttu-id="0b6c6-1454">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1454">kaarthouder</span></span> 
- <span data-ttu-id="0b6c6-1455">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1455">kaarthouders</span></span> 
- <span data-ttu-id="0b6c6-1456">karte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1456">karte</span></span>  
- <span data-ttu-id="0b6c6-1457">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1457">karteninhaber</span></span> 
- <span data-ttu-id="0b6c6-1458">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1458">karteninhabers</span></span>
- <span data-ttu-id="0b6c6-1459">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1459">kartennr</span></span> 
- <span data-ttu-id="0b6c6-1460">kartennummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1460">kartennummer</span></span> 
- <span data-ttu-id="0b6c6-1461">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1461">kreditkarte</span></span> 
- <span data-ttu-id="0b6c6-1462">kreditkarten nummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1462">kreditkarten-nummer</span></span> 
- <span data-ttu-id="0b6c6-1463">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1463">kreditkarteninhaber</span></span> 
- <span data-ttu-id="0b6c6-1464">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1464">kreditkarteninstitut</span></span> 
- <span data-ttu-id="0b6c6-1465">kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1465">kreditkartennummer</span></span> 
- <span data-ttu-id="0b6c6-1466">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1466">kreditkartentyp</span></span> 
- <span data-ttu-id="0b6c6-1467">maestro
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1467">maestro</span></span> 
- <span data-ttu-id="0b6c6-1468">master card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1468">master card</span></span> 
- <span data-ttu-id="0b6c6-1469">master cards
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1469">master cards</span></span> 
- <span data-ttu-id="0b6c6-1470">mastercard
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1470">mastercard</span></span> 
- <span data-ttu-id="0b6c6-1471">mastercards</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1471">mastercards</span></span> 
- <span data-ttu-id="0b6c6-1472">mc</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1472">mc</span></span> 
- <span data-ttu-id="0b6c6-1473">mister cash
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1473">mister cash</span></span> 
- <span data-ttu-id="0b6c6-1474">n carta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1474">n carta</span></span> 
- <span data-ttu-id="0b6c6-1475">carta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1475">carta</span></span> 
- <span data-ttu-id="0b6c6-1476">Не де tarjeta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1476">no de tarjeta</span></span> 
- <span data-ttu-id="0b6c6-1477">не cartao действие</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1477">no do cartao</span></span> 
- <span data-ttu-id="0b6c6-1478">не cartão действие</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1478">no do cartão</span></span> 
- <span data-ttu-id="0b6c6-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="0b6c6-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p118">no. do cartao</span></span> 
- <span data-ttu-id="0b6c6-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p119">no. do cartão</span></span> 
- <span data-ttu-id="0b6c6-1485">nr carta</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1485">nr carta</span></span> 
- <span data-ttu-id="0b6c6-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p120">nr. carta</span></span> 
- <span data-ttu-id="0b6c6-1488">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1488">numeri di scheda</span></span> 
- <span data-ttu-id="0b6c6-1489">numero carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1489">numero carta</span></span> 
- <span data-ttu-id="0b6c6-1490">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1490">numero de cartao</span></span> 
- <span data-ttu-id="0b6c6-1491">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1491">numero de carte</span></span> 
- <span data-ttu-id="0b6c6-1492">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1492">numero de cartão</span></span> 
- <span data-ttu-id="0b6c6-1493">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1493">numero de tarjeta</span></span>
- <span data-ttu-id="0b6c6-1494">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1494">numero della carta</span></span> 
- <span data-ttu-id="0b6c6-1495">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1495">numero di carta</span></span> 
- <span data-ttu-id="0b6c6-1496">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1496">numero di scheda</span></span> 
- <span data-ttu-id="0b6c6-1497">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1497">numero do cartao</span></span> 
- <span data-ttu-id="0b6c6-1498">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1498">numero do cartão</span></span> 
- <span data-ttu-id="0b6c6-1499">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1499">numéro de carte</span></span> 
- <span data-ttu-id="0b6c6-1500">nº carta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1500">nº carta</span></span> 
- <span data-ttu-id="0b6c6-1501">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1501">nº de carte</span></span> 
- <span data-ttu-id="0b6c6-1502">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1502">nº de la carte</span></span> 
- <span data-ttu-id="0b6c6-1503">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1503">nº de tarjeta</span></span> 
- <span data-ttu-id="0b6c6-1504">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1504">nº do cartao</span></span> 
- <span data-ttu-id="0b6c6-1505">Действие cartão nº</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1505">nº do cartão</span></span> 
- <span data-ttu-id="0b6c6-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p121">nº. do cartão</span></span> 
- <span data-ttu-id="0b6c6-1508">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1508">número de cartao</span></span> 
- <span data-ttu-id="0b6c6-1509">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1509">número de cartão</span></span> 
- <span data-ttu-id="0b6c6-1510">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1510">número de tarjeta</span></span> 
- <span data-ttu-id="0b6c6-1511">número do cartao</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1511">número do cartao</span></span> 
- <span data-ttu-id="0b6c6-1512">scheda dell'assegno
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1512">scheda dell'assegno</span></span> 
- <span data-ttu-id="0b6c6-1513">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1513">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="0b6c6-1514">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1514">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="0b6c6-1515">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1515">scheda della banca</span></span> 
- <span data-ttu-id="0b6c6-1516">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1516">scheda di controllo</span></span> 
- <span data-ttu-id="0b6c6-1517">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1517">scheda di debito</span></span> 
- <span data-ttu-id="0b6c6-1518">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1518">scheda matrice</span></span> 
- <span data-ttu-id="0b6c6-1519">schede dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1519">schede dell'atmosfera</span></span> 
- <span data-ttu-id="0b6c6-1520">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1520">schede di controllo</span></span> 
- <span data-ttu-id="0b6c6-1521">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1521">schede di debito</span></span> 
- <span data-ttu-id="0b6c6-1522">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1522">schede matrici</span></span> 
- <span data-ttu-id="0b6c6-1523">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1523">scoprono la scheda</span></span> 
- <span data-ttu-id="0b6c6-1524">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1524">scoprono le schede</span></span> 
- <span data-ttu-id="0b6c6-1525">solo
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1525">solo</span></span> 
- <span data-ttu-id="0b6c6-1526">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1526">supporti di scheda</span></span> 
- <span data-ttu-id="0b6c6-1527">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1527">supporto di scheda</span></span> 
- <span data-ttu-id="0b6c6-1528">ключ</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1528">switch</span></span> 
- <span data-ttu-id="0b6c6-1529">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1529">tarjeta atm</span></span> 
- <span data-ttu-id="0b6c6-1530">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1530">tarjeta credito</span></span> 
- <span data-ttu-id="0b6c6-1531">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1531">tarjeta de atm</span></span> 
- <span data-ttu-id="0b6c6-1532">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1532">tarjeta de credito</span></span> 
- <span data-ttu-id="0b6c6-1533">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1533">tarjeta de debito</span></span> 
- <span data-ttu-id="0b6c6-1534">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1534">tarjeta debito</span></span> 
- <span data-ttu-id="0b6c6-1535">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1535">tarjeta no</span></span>
- <span data-ttu-id="0b6c6-1536">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1536">tarjetahabiente</span></span> 
- <span data-ttu-id="0b6c6-1537">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1537">tipo della scheda</span></span> 
- <span data-ttu-id="0b6c6-1538">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1538">ufficio giapponese della</span></span> 
- <span data-ttu-id="0b6c6-1539">scheda
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1539">scheda</span></span> 
- <span data-ttu-id="0b6c6-1540">v pay
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1540">v pay</span></span> 
- <span data-ttu-id="0b6c6-1541">v оплаты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1541">v-pay</span></span> 
- <span data-ttu-id="0b6c6-1542">visa
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1542">visa</span></span> 
- <span data-ttu-id="0b6c6-1543">visa plus
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1543">visa plus</span></span> 
- <span data-ttu-id="0b6c6-1544">visa electron
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1544">visa electron</span></span> 
- <span data-ttu-id="0b6c6-1545">visto
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1545">visto</span></span> 
- <span data-ttu-id="0b6c6-1546">visum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1546">visum</span></span> 
- <span data-ttu-id="0b6c6-1547">vpay
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1547">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="0b6c6-1548">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1548">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="0b6c6-1549">card identification number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1549">card identification number</span></span>
- <span data-ttu-id="0b6c6-1550">card verification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1550">card verification</span></span> 
- <span data-ttu-id="0b6c6-1551">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1551">cardi la verifica</span></span> 
- <span data-ttu-id="0b6c6-1552">cid
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1552">cid</span></span> 
- <span data-ttu-id="0b6c6-1553">COD seg</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1553">cod seg</span></span> 
- <span data-ttu-id="0b6c6-1554">COD seguranca</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1554">cod seguranca</span></span> 
- <span data-ttu-id="0b6c6-1555">COD segurança</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1555">cod segurança</span></span> 
- <span data-ttu-id="0b6c6-1556">COD sicurezza</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1556">cod sicurezza</span></span> 
- <span data-ttu-id="0b6c6-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p122">cod. seg</span></span> 
- <span data-ttu-id="0b6c6-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p123">cod. seguranca</span></span> 
- <span data-ttu-id="0b6c6-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p124">cod. segurança</span></span> 
- <span data-ttu-id="0b6c6-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="0b6c6-1565">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1565">codice di sicurezza</span></span> 
- <span data-ttu-id="0b6c6-1566">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1566">codice di verifica</span></span> 
- <span data-ttu-id="0b6c6-1567">codigo
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1567">codigo</span></span> 
- <span data-ttu-id="0b6c6-1568">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1568">codigo de seguranca</span></span> 
- <span data-ttu-id="0b6c6-1569">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1569">codigo de segurança</span></span> 
- <span data-ttu-id="0b6c6-1570">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1570">crittogramma</span></span> 
- <span data-ttu-id="0b6c6-1571">cryptogram
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1571">cryptogram</span></span> 
- <span data-ttu-id="0b6c6-1572">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1572">cryptogramme</span></span> 
- <span data-ttu-id="0b6c6-1573">CV2</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1573">cv2</span></span> 
- <span data-ttu-id="0b6c6-1574">cvc
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1574">cvc</span></span> 
- <span data-ttu-id="0b6c6-1575">cvc2</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1575">cvc2</span></span> 
- <span data-ttu-id="0b6c6-1576">cvn
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1576">cvn</span></span> 
- <span data-ttu-id="0b6c6-1577">cvv
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1577">cvv</span></span> 
- <span data-ttu-id="0b6c6-1578">cvv2</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1578">cvv2</span></span> 
- <span data-ttu-id="0b6c6-1579">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1579">cód seguranca</span></span> 
- <span data-ttu-id="0b6c6-1580">cód segurança</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1580">cód segurança</span></span> 
- <span data-ttu-id="0b6c6-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p126">cód. seguranca</span></span> 
- <span data-ttu-id="0b6c6-p127">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p127">cód. segurança</span></span> 
- <span data-ttu-id="0b6c6-1585">código
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1585">código</span></span> 
- <span data-ttu-id="0b6c6-1586">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1586">código de seguranca</span></span> 
- <span data-ttu-id="0b6c6-1587">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1587">código de segurança</span></span> 
- <span data-ttu-id="0b6c6-1588">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1588">de kaart controle</span></span> 
- <span data-ttu-id="0b6c6-1589">geeft nr uit
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1589">geeft nr uit</span></span> 
- <span data-ttu-id="0b6c6-1590">issue no
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1590">issue no</span></span> 
- <span data-ttu-id="0b6c6-1591">issue number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1591">issue number</span></span> 
- <span data-ttu-id="0b6c6-1592">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1592">kaartidentificatienummer</span></span> 
- <span data-ttu-id="0b6c6-1593">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1593">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="0b6c6-1594">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1594">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="0b6c6-1595">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1595">kwestieaantal</span></span> 
- <span data-ttu-id="0b6c6-p128">no. dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="0b6c6-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="0b6c6-1600">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1600">numero de securite</span></span> 
- <span data-ttu-id="0b6c6-1601">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1601">numero de verificacao</span></span> 
- <span data-ttu-id="0b6c6-1602">numero dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1602">numero dell'edizione</span></span> 
- <span data-ttu-id="0b6c6-1603">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1603">numero di identificazione della</span></span> 
- <span data-ttu-id="0b6c6-1604">scheda
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1604">scheda</span></span> 
- <span data-ttu-id="0b6c6-1605">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1605">numero di sicurezza</span></span> 
- <span data-ttu-id="0b6c6-1606">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1606">numero van veiligheid</span></span> 
- <span data-ttu-id="0b6c6-1607">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1607">numéro de sécurité</span></span> 
- <span data-ttu-id="0b6c6-1608">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1608">nº autorizzazione</span></span> 
- <span data-ttu-id="0b6c6-1609">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1609">número de verificação</span></span> 
- <span data-ttu-id="0b6c6-1610">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1610">perno il blocco</span></span> 
- <span data-ttu-id="0b6c6-1611">pin block
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1611">pin block</span></span> 
- <span data-ttu-id="0b6c6-1612">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1612">prufziffer</span></span> 
- <span data-ttu-id="0b6c6-1613">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1613">prüfziffer</span></span> 
- <span data-ttu-id="0b6c6-1614">security code
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1614">security code</span></span> 
- <span data-ttu-id="0b6c6-1615">security no
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1615">security no</span></span> 
- <span data-ttu-id="0b6c6-1616">security number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1616">security number</span></span> 
- <span data-ttu-id="0b6c6-1617">sicherheits kode
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1617">sicherheits kode</span></span> 
- <span data-ttu-id="0b6c6-1618">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1618">sicherheitscode</span></span> 
- <span data-ttu-id="0b6c6-1619">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1619">sicherheitsnummer</span></span> 
- <span data-ttu-id="0b6c6-1620">speldblok
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1620">speldblok</span></span> 
- <span data-ttu-id="0b6c6-1621">veiligheid nr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1621">veiligheid nr</span></span> 
- <span data-ttu-id="0b6c6-1622">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1622">veiligheidsaantal</span></span> 
- <span data-ttu-id="0b6c6-1623">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1623">veiligheidscode</span></span> 
- <span data-ttu-id="0b6c6-1624">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1624">veiligheidsnummer</span></span> 
- <span data-ttu-id="0b6c6-1625">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1625">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="0b6c6-1626">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1626">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="0b6c6-1627">ablauf
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1627">ablauf</span></span> 
- <span data-ttu-id="0b6c6-1628">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1628">data de expiracao</span></span> 
- <span data-ttu-id="0b6c6-1629">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1629">data de expiração</span></span> 
- <span data-ttu-id="0b6c6-1630">data del exp
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1630">data del exp</span></span> 
- <span data-ttu-id="0b6c6-1631">data di exp
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1631">data di exp</span></span> 
- <span data-ttu-id="0b6c6-1632">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1632">data di scadenza</span></span> 
- <span data-ttu-id="0b6c6-1633">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1633">data em que expira</span></span> 
- <span data-ttu-id="0b6c6-1634">data scad
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1634">data scad</span></span> 
- <span data-ttu-id="0b6c6-1635">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1635">data scadenza</span></span> 
- <span data-ttu-id="0b6c6-1636">date de validité
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1636">date de validité</span></span> 
- <span data-ttu-id="0b6c6-1637">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1637">datum afloop</span></span> 
- <span data-ttu-id="0b6c6-1638">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1638">datum van exp</span></span> 
- <span data-ttu-id="0b6c6-1639">de afloop
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1639">de afloop</span></span> 
- <span data-ttu-id="0b6c6-1640">espira
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1640">espira</span></span> 
- <span data-ttu-id="0b6c6-1641">espira
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1641">espira</span></span> 
- <span data-ttu-id="0b6c6-1642">exp date
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1642">exp date</span></span> 
- <span data-ttu-id="0b6c6-1643">exp datum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1643">exp datum</span></span> 
- <span data-ttu-id="0b6c6-1644">истечение срока действия</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1644">expiration</span></span> 
- <span data-ttu-id="0b6c6-1645">expire
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1645">expire</span></span> 
- <span data-ttu-id="0b6c6-1646">expires
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1646">expires</span></span> 
- <span data-ttu-id="0b6c6-1647">expiry
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1647">expiry</span></span> 
- <span data-ttu-id="0b6c6-1648">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1648">fecha de expiracion</span></span> 
- <span data-ttu-id="0b6c6-1649">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1649">fecha de venc</span></span> 
- <span data-ttu-id="0b6c6-1650">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1650">gultig bis</span></span> 
- <span data-ttu-id="0b6c6-1651">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1651">gultigkeitsdatum</span></span> 
- <span data-ttu-id="0b6c6-1652">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1652">gültig bis</span></span> 
- <span data-ttu-id="0b6c6-1653">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1653">gültigkeitsdatum</span></span> 
- <span data-ttu-id="0b6c6-1654">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1654">la scadenza</span></span> 
- <span data-ttu-id="0b6c6-1655">scadenza
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1655">scadenza</span></span> 
- <span data-ttu-id="0b6c6-1656">valable
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1656">valable</span></span> 
- <span data-ttu-id="0b6c6-1657">validade
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1657">validade</span></span> 
- <span data-ttu-id="0b6c6-1658">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1658">valido hasta</span></span> 
- <span data-ttu-id="0b6c6-1659">valor
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1659">valor</span></span> 
- <span data-ttu-id="0b6c6-1660">venc
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1660">venc</span></span> 
- <span data-ttu-id="0b6c6-1661">vencimento
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1661">vencimento</span></span> 
- <span data-ttu-id="0b6c6-1662">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1662">vencimiento</span></span> 
- <span data-ttu-id="0b6c6-1663">verloopt
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1663">verloopt</span></span> 
- <span data-ttu-id="0b6c6-1664">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1664">vervaldag</span></span> 
- <span data-ttu-id="0b6c6-1665">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1665">vervaldatum</span></span> 
- <span data-ttu-id="0b6c6-1666">vto
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1666">vto</span></span> 
- <span data-ttu-id="0b6c6-1667">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1667">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="0b6c6-1668">Номер водительского удостоверения ЕС</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1668">EU Driver's License Number</span></span>

<span data-ttu-id="0b6c6-1669">Для получения дополнительных сведений см [Тип конфиденциальных данных номер водительского удостоверения ЕС](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1669">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="0b6c6-1670">Национальный ЕС идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1670">EU National Identification Number</span></span>

<span data-ttu-id="0b6c6-1671">Для получения дополнительных сведений см [ЕС национальный идентификационный номер тип конфиденциальных данных](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1671">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="0b6c6-1672">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1672">EU Passport Number</span></span>

<span data-ttu-id="0b6c6-1673">Для получения дополнительных сведений см [номер паспорта ЕС тип конфиденциальных данных](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1673">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="0b6c6-1674">Страховой номер для ЕС или иметь эквивалентные права идентификатор</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1674">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="0b6c6-1675">Для получения дополнительных сведений, видеть [страховой номер для ЕС или эквивалентный идентификатор типа конфиденциальной информации](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1675">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="0b6c6-1676">Идентификационный номер налога ЕС</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1676">EU Tax Identification Number</span></span>

<span data-ttu-id="0b6c6-1677">Для получения дополнительных сведений см [идентификационный номер налога ЕС тип конфиденциальных данных](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1677">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="0b6c6-1678">Национальный идентификатор, Финляндия</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1678">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1679">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1679">Format</span></span>

<span data-ttu-id="0b6c6-1680">Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1680">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1681">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1681">Pattern</span></span>

<span data-ttu-id="0b6c6-1682">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1682">Pattern must include all of the following:</span></span>
- <span data-ttu-id="0b6c6-1683">Шесть цифр в формате ДДММГГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1683">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="0b6c6-1684">Маркер века (символы "-" и "+" или буква "a")</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1684">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="0b6c6-1685">Трехзначный личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1685">Three-digit personal identification number</span></span> 
- <span data-ttu-id="0b6c6-1686">Цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1686">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1687">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1687">Checksum</span></span>

<span data-ttu-id="0b6c6-1688">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1688">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1689">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1689">Definition</span></span>

<span data-ttu-id="0b6c6-1690">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1690">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1691">функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1691">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1692">находится ключевое слово из Keyword_finnish_national_id;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1692">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="0b6c6-1693">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1693">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1694">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1694">Keywords</span></span>

- <span data-ttu-id="0b6c6-1695">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1695">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="0b6c6-1696">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1696">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="0b6c6-1697">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1697">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="0b6c6-1698">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1698">Personbeteckning</span></span>
- <span data-ttu-id="0b6c6-1699">Personnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1699">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="0b6c6-1700">Номер паспорта для Финляндии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1700">Finland Passport Number</span></span>

<span data-ttu-id="0b6c6-p130">Форматирование сочетание девяти буквы и цифры сочетание шаблон девяти только буквы и цифры: два букв (без учета регистра) семь цифр контрольной суммой нет определения политики DLP — 75% уверены в том, что он обнаружил этот тип конфиденциальных данных, если в Близость 300 знаков: регулярное выражение Regex_finland_passport_number находит контент, который соответствует шаблону. Ключевое слово из Keyword_finland_passport_number найти. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> Passi Passport Keyword_finland_passport_number ключевых слов</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="0b6c6-1705">Номер водительского удостоверения для Франции</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1705">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1706">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1706">Format</span></span>

<span data-ttu-id="0b6c6-1707">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1707">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1708">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1708">Pattern</span></span>

<span data-ttu-id="0b6c6-1709">12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1709">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1710">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1710">Checksum</span></span>

<span data-ttu-id="0b6c6-1711">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1711">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1712">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1712">Definition</span></span>

<span data-ttu-id="0b6c6-1713">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1713">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1714">Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1714">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1715">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1715">At least one of the following is true:</span></span>
- <span data-ttu-id="0b6c6-1716">найдено ключевое слово из Keyword_french_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1716">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="0b6c6-1717">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1717">The function Func_eu_date finds a date in the right date format.</span></span>

```
<!-- France Driver's License Number -->
<Entity id="18e55a36-a01b-4b0f-943d-dc10282a1824" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_french_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_french_drivers_license" />
          <Match idRef="Func_eu_date" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1718">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1718">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="0b6c6-1719">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1719">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="0b6c6-1720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1720">drivers licence</span></span>
- <span data-ttu-id="0b6c6-1721">drivers license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1721">drivers license</span></span>
- <span data-ttu-id="0b6c6-1722">driving licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1722">driving licence</span></span>
- <span data-ttu-id="0b6c6-1723">управляющий лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1723">driving license</span></span>
- <span data-ttu-id="0b6c6-1724">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1724">permis de conduire</span></span>
- <span data-ttu-id="0b6c6-1725">
licence number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1725">licence number</span></span>
- <span data-ttu-id="0b6c6-1726">
license number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1726">license number</span></span>
- <span data-ttu-id="0b6c6-1727">
licence numbers</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1727">licence numbers</span></span>
- <span data-ttu-id="0b6c6-1728">

license numbers</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1728">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="0b6c6-1729">Номер внутреннего удостоверения личности для Франции (CNI)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1729">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1730">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1730">Format</span></span>

<span data-ttu-id="0b6c6-1731">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1731">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1732">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1732">Pattern</span></span>

<span data-ttu-id="0b6c6-1733">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1733">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1734">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1734">Checksum</span></span>

<span data-ttu-id="0b6c6-1735">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1735">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1736">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1736">Definition</span></span>

<span data-ttu-id="0b6c6-1737">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1737">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1738">регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1738">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1739">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1739">Keywords</span></span>

<span data-ttu-id="0b6c6-1740">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1740">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="0b6c6-1741">Номер паспорта гражданина Франции</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1741">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1742">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1742">Format</span></span>

<span data-ttu-id="0b6c6-1743">Девять цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1743">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1744">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1744">Pattern</span></span>

<span data-ttu-id="0b6c6-1745">Девять цифр и букв</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1745">Nine digits and letters:</span></span>
- <span data-ttu-id="0b6c6-1746">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1746">Two digits</span></span> 
- <span data-ttu-id="0b6c6-1747">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1747">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-1748">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1748">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1749">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1749">Checksum</span></span>

<span data-ttu-id="0b6c6-1750">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1750">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1751">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1751">Definition</span></span>

<span data-ttu-id="0b6c6-1752">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1752">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1753">функция Func_fr_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1753">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1754">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1754">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1755">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1755">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="0b6c6-1756">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1756">Keyword_passport</span></span>

- <span data-ttu-id="0b6c6-1757">Passport Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1757">Passport Number</span></span>
- <span data-ttu-id="0b6c6-1758">
Passport No</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1758">Passport No</span></span>
- <span data-ttu-id="0b6c6-1759">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1759">Passport #</span></span>
- <span data-ttu-id="0b6c6-1760">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1760">Passport#</span></span>
- <span data-ttu-id="0b6c6-1761">PassportID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1761">PassportID</span></span>
- <span data-ttu-id="0b6c6-1762">Passportno
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1762">Passportno</span></span>
- <span data-ttu-id="0b6c6-1763">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1763">passportnumber</span></span>
- <span data-ttu-id="0b6c6-1764">パスポート</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1764">パスポート</span></span>
- <span data-ttu-id="0b6c6-1765">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1765">パスポート番号</span></span>
- <span data-ttu-id="0b6c6-1766">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1766">パスポートのNum</span></span>
- <span data-ttu-id="0b6c6-1767">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1767">パスポート ＃</span></span> 
- <span data-ttu-id="0b6c6-1768">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1768">Numéro de passeport</span></span>
- <span data-ttu-id="0b6c6-1769">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1769">Passeport n °</span></span>
- <span data-ttu-id="0b6c6-1770">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1770">Passeport Non</span></span>
- <span data-ttu-id="0b6c6-1771">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1771">Passeport #</span></span>
- <span data-ttu-id="0b6c6-1772">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1772">Passeport#</span></span>
- <span data-ttu-id="0b6c6-1773">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1773">PasseportNon</span></span>
- <span data-ttu-id="0b6c6-1774">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1774">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="0b6c6-1775">Страховой номер для Франции (INSEE)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1775">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1776">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1776">Format</span></span>

<span data-ttu-id="0b6c6-1777">15 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1777">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1778">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1778">Pattern</span></span>

<span data-ttu-id="0b6c6-1779">Должен соответствовать одному из двух шаблонов:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1779">Must match one of two patterns:</span></span>
- <span data-ttu-id="0b6c6-1780">13 цифр, пробел, а затем две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1780">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="0b6c6-1781">или</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1781">or</span></span>
- <span data-ttu-id="0b6c6-1782">15 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1782">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1783">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1783">Checksum</span></span>

<span data-ttu-id="0b6c6-1784">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1784">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1785">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1785">Definition</span></span>

<span data-ttu-id="0b6c6-1786">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1786">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1787">Функция Func_french_insee или Func_fr_insee находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1787">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1788">находится ключевое слово из Keyword_fr_insee;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1788">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="0b6c6-1789">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1789">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-1790">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1790">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1791">Функция Func_french_insee или Func_fr_insee находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1791">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1792">ни одно ключевое слово из Keyword_fr_insee не находится;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1792">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="0b6c6-1793">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1793">The checksum passes.</span></span>

```
<!-- France INSEE -->
<Entity id="71f62b97-efe0-4aa1-aa49-e14de253619d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="95">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="1">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_french_insee" />
        <Match idRef="Func_fr_insee" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_fr_insee" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1794">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1794">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="0b6c6-1795">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1795">Keyword_fr_insee</span></span>

- <span data-ttu-id="0b6c6-1796">insee</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1796">insee</span></span>
- <span data-ttu-id="0b6c6-1797">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1797">securité sociale</span></span>
- <span data-ttu-id="0b6c6-1798">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1798">securite sociale</span></span>
- <span data-ttu-id="0b6c6-1799">
national id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1799">national id</span></span>
- <span data-ttu-id="0b6c6-1800">
national identification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1800">national identification</span></span>
- <span data-ttu-id="0b6c6-1801">
numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1801">numéro d'identité</span></span>
- <span data-ttu-id="0b6c6-1802">Нет d'identité</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1802">no d'identité</span></span>
- <span data-ttu-id="0b6c6-p131">
no. d'identité</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p131">no. d'identité</span></span>
- <span data-ttu-id="0b6c6-1805">
numero d'identite</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1805">numero d'identite</span></span>
- <span data-ttu-id="0b6c6-1806">не d'identite</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1806">no d'identite</span></span>
- <span data-ttu-id="0b6c6-p132">
no. d'identite</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p132">no. d'identite</span></span>
- <span data-ttu-id="0b6c6-1809">social security number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1809">social security number</span></span>
- <span data-ttu-id="0b6c6-1810">
social security code</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1810">social security code</span></span>
- <span data-ttu-id="0b6c6-1811">social insurance number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1811">social insurance number</span></span>
- <span data-ttu-id="0b6c6-1812">
le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1812">le numéro d'identification nationale</span></span>
- <span data-ttu-id="0b6c6-1813">
d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1813">d'identité nationale</span></span>
- <span data-ttu-id="0b6c6-1814">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1814">numéro de sécurité sociale</span></span>
- <span data-ttu-id="0b6c6-1815">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1815">le code de la sécurité sociale</span></span>
- <span data-ttu-id="0b6c6-1816">
numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1816">numéro d'assurance sociale</span></span>
- <span data-ttu-id="0b6c6-1817">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1817">numéro de sécu</span></span>
- <span data-ttu-id="0b6c6-1818">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1818">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="0b6c6-1819">Номер водительского удостоверения для Германии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1819">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1820">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1820">Format</span></span>

<span data-ttu-id="0b6c6-1821">Сочетание 11 цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1821">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1822">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1822">Pattern</span></span>

<span data-ttu-id="0b6c6-1823">11 цифр и букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1823">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="0b6c6-1824">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1824">A digit or letter</span></span> 
- <span data-ttu-id="0b6c6-1825">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1825">Two digits</span></span> 
- <span data-ttu-id="0b6c6-1826">Шесть цифр или букв</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1826">Six digits or letters</span></span> 
- <span data-ttu-id="0b6c6-1827">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1827">A digit</span></span> 
- <span data-ttu-id="0b6c6-1828">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1828">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1829">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1829">Checksum</span></span>

<span data-ttu-id="0b6c6-1830">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1830">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1831">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1831">Definition</span></span>

<span data-ttu-id="0b6c6-1832">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1833">Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1833">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1834">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1834">At least one of the following is true:</span></span>
    - <span data-ttu-id="0b6c6-1835">найдено ключевое слово из Keyword_german_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1835">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="0b6c6-1836">найдено ключевое слово из Keyword_german_drivers_license_collaborative;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1836">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="0b6c6-1837">найдено ключевое слово из Keyword_german_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1837">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="0b6c6-1838">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1838">The checksum passes.</span></span>

```
<!-- German Driver's License Number -->
<Entity id="91da9335-1edb-45b7-a95f-5fe41a16c63c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_drivers_license" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_drivers_license_number" />
          <Match idRef="Keyword_german_drivers_license_collaborative" />
          <Match idRef="Keyword_german_drivers_license" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1839">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1839">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="0b6c6-1840">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1840">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="0b6c6-1841">Führerschein</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1841">Führerschein</span></span>
- <span data-ttu-id="0b6c6-1842">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1842">Fuhrerschein</span></span>
- <span data-ttu-id="0b6c6-1843">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1843">Fuehrerschein</span></span>
- <span data-ttu-id="0b6c6-1844">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1844">Führerscheinnummer</span></span>
- <span data-ttu-id="0b6c6-1845">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1845">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="0b6c6-1846">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1846">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="0b6c6-1847">
Führerschein-
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1847">Führerschein-</span></span> 
- <span data-ttu-id="0b6c6-1848">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1848">Fuhrerschein-</span></span> 
- <span data-ttu-id="0b6c6-1849">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1849">Fuehrerschein-</span></span> 
- <span data-ttu-id="0b6c6-1850">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1850">FührerscheinnummerNr</span></span>
- <span data-ttu-id="0b6c6-1851">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1851">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="0b6c6-1852">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1852">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="0b6c6-1853">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1853">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="0b6c6-1854">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1854">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="0b6c6-1855">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1855">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="0b6c6-1856">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1856">Führerschein- Nr</span></span>
- <span data-ttu-id="0b6c6-1857">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1857">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="0b6c6-1858">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1858">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="0b6c6-1859">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1859">Führerschein- Klasse</span></span> 
- <span data-ttu-id="0b6c6-1860">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1860">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="0b6c6-1861">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1861">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="0b6c6-1862">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1862">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="0b6c6-1863">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1863">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="0b6c6-1864">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1864">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="0b6c6-1865">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1865">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="0b6c6-1866">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1866">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="0b6c6-1867">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1867">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="0b6c6-1868">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1868">Führerschein- Nr</span></span> 
- <span data-ttu-id="0b6c6-1869">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1869">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="0b6c6-1870">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1870">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="0b6c6-1871">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1871">Führerschein- Klasse</span></span> 
- <span data-ttu-id="0b6c6-1872">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1872">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="0b6c6-1873">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1873">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="0b6c6-1874">DL</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1874">DL</span></span> 
- <span data-ttu-id="0b6c6-1875">DLS</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1875">DLS</span></span>
- <span data-ttu-id="0b6c6-1876">
Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1876">Driv Lic</span></span> 
- <span data-ttu-id="0b6c6-1877">Driv Licen
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1877">Driv Licen</span></span> 
- <span data-ttu-id="0b6c6-1878">Driv License</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1878">Driv License</span></span>
- <span data-ttu-id="0b6c6-1879">
Driv Licenses
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1879">Driv Licenses</span></span> 
- <span data-ttu-id="0b6c6-1880">Driv Licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1880">Driv Licence</span></span> 
- <span data-ttu-id="0b6c6-1881">Driv Licences
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1881">Driv Licences</span></span> 
- <span data-ttu-id="0b6c6-1882">Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1882">Driv Lic</span></span> 
- <span data-ttu-id="0b6c6-1883">Driver Licen
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1883">Driver Licen</span></span> 
- <span data-ttu-id="0b6c6-1884">Драйвер лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1884">Driver License</span></span> 
- <span data-ttu-id="0b6c6-1885">Драйвер лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1885">Driver Licenses</span></span> 
- <span data-ttu-id="0b6c6-1886">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1886">Driver Licence</span></span> 
- <span data-ttu-id="0b6c6-1887">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1887">Driver Licences</span></span> 
- <span data-ttu-id="0b6c6-1888">Драйверы Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1888">Drivers Lic</span></span> 
- <span data-ttu-id="0b6c6-1889">Драйверы Licen</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1889">Drivers Licen</span></span> 
- <span data-ttu-id="0b6c6-1890">Драйверы лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1890">Drivers License</span></span> 
- <span data-ttu-id="0b6c6-1891">Драйверы лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1891">Drivers Licenses</span></span> 
- <span data-ttu-id="0b6c6-1892">Лицензия драйверы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1892">Drivers Licence</span></span> 
- <span data-ttu-id="0b6c6-1893">Число лицензий на драйверы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1893">Drivers Licences</span></span> 
- <span data-ttu-id="0b6c6-1894">Lic драйвера</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1894">Driver's Lic</span></span> 
- <span data-ttu-id="0b6c6-1895">Driver's Licen
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1895">Driver's Licen</span></span> 
- <span data-ttu-id="0b6c6-1896">Водительского удостоверения для лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1896">Driver's License</span></span> 
- <span data-ttu-id="0b6c6-1897">Водительского удостоверения для лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1897">Driver's Licenses</span></span> 
- <span data-ttu-id="0b6c6-1898">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1898">Driver's Licence</span></span> 
- <span data-ttu-id="0b6c6-1899">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1899">Driver's Licences</span></span> 
- <span data-ttu-id="0b6c6-1900">Driving Lic
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1900">Driving Lic</span></span> 
- <span data-ttu-id="0b6c6-1901">Driving Licen
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1901">Driving Licen</span></span> 
- <span data-ttu-id="0b6c6-1902">Driving License
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1902">Driving License</span></span> 
- <span data-ttu-id="0b6c6-1903">Driving Licenses
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1903">Driving Licenses</span></span> 
- <span data-ttu-id="0b6c6-1904">Driving Licence

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1904">Driving Licence</span></span> 
- <span data-ttu-id="0b6c6-1905">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1905">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="0b6c6-1906">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1906">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="0b6c6-1907">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1907">Nr-Führerschein</span></span> 
- <span data-ttu-id="0b6c6-1908">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1908">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="0b6c6-1909">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1909">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="0b6c6-1910">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1910">No-Führerschein</span></span> 
- <span data-ttu-id="0b6c6-1911">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1911">No-Fuhrerschein</span></span> 
- <span data-ttu-id="0b6c6-1912">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1912">No-Fuehrerschein</span></span> 
- <span data-ttu-id="0b6c6-1913">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1913">N-Führerschein</span></span> 
- <span data-ttu-id="0b6c6-1914">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1914">N-Fuhrerschein</span></span> 
- <span data-ttu-id="0b6c6-1915">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1915">N-Fuehrerschein</span></span>
- <span data-ttu-id="0b6c6-1916">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1916">Nr-Führerschein</span></span> 
- <span data-ttu-id="0b6c6-1917">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1917">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="0b6c6-1918">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1918">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="0b6c6-1919">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1919">No-Führerschein</span></span> 
- <span data-ttu-id="0b6c6-1920">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1920">No-Fuhrerschein</span></span> 
- <span data-ttu-id="0b6c6-1921">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1921">No-Fuehrerschein</span></span> 
- <span data-ttu-id="0b6c6-1922">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1922">N-Führerschein</span></span> 
- <span data-ttu-id="0b6c6-1923">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1923">N-Fuhrerschein</span></span> 
- <span data-ttu-id="0b6c6-1924">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1924">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="0b6c6-1925">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1925">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="0b6c6-1926">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1926">ausstellungsdatum</span></span>
- <span data-ttu-id="0b6c6-1927">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1927">ausstellungsort</span></span>
- <span data-ttu-id="0b6c6-1928">
ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1928">ausstellende behöde</span></span>
- <span data-ttu-id="0b6c6-1929">
ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1929">ausstellende behorde</span></span>
- <span data-ttu-id="0b6c6-1930">

ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1930">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="0b6c6-1931">Номер паспорта гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1931">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1932">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1932">Format</span></span>

<span data-ttu-id="0b6c6-1933">10 цифр или букв.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1933">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1934">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1934">Pattern</span></span>

<span data-ttu-id="0b6c6-1935">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1935">Pattern must include all of the following:</span></span>
- <span data-ttu-id="0b6c6-1936">Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1936">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="0b6c6-1937">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1937">Three digits</span></span> 
- <span data-ttu-id="0b6c6-1938">Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1938">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="0b6c6-1939">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1939">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1940">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1940">Checksum</span></span>

<span data-ttu-id="0b6c6-1941">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1941">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1942">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1942">Definition</span></span>

<span data-ttu-id="0b6c6-1943">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1943">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1944">функция Func_german_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1944">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1945">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1945">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="0b6c6-1946">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1946">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-1947">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1947">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1948">функция Func_german_passport_data находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1948">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1949">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1949">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="0b6c6-1950">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1950">The checksum passes.</span></span>

```
<!-- German Passport Number -->
<Entity id="2e3da144-d42b-47ed-b123-fbf78604e52c" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_german_passport" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_german_passport_data" />
        <Any minMatches="1">
          <Match idRef="Keyword_german_passport" />
          <Match idRef="Keyword_german_passport_collaborative" />
          <Match idRef="Keyword_german_passport_number" />
          <Match idRef="Keyword_german_passport1" />
          <Match idRef="Keyword_german_passport2" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1951">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1951">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="0b6c6-1952">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1952">Keyword_german_passport</span></span>

- <span data-ttu-id="0b6c6-1953">reisepass</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1953">reisepass</span></span>
- <span data-ttu-id="0b6c6-1954">
reisepasse</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1954">reisepasse</span></span>
- <span data-ttu-id="0b6c6-1955">
reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1955">reisepassnummer</span></span>
- <span data-ttu-id="0b6c6-1956">passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1956">passport</span></span>
- <span data-ttu-id="0b6c6-1957">

passports</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1957">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="0b6c6-1958">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1958">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="0b6c6-1959">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1959">geburtsdatum</span></span>
- <span data-ttu-id="0b6c6-1960">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1960">ausstellungsdatum</span></span>
- <span data-ttu-id="0b6c6-1961">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1961">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="0b6c6-1962">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1962">Keyword_german_passport_number</span></span>

<span data-ttu-id="0b6c6-1963">Не-Nr Reisepass-Reisepass</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1963">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="0b6c6-1964">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1964">Keyword_german_passport1</span></span>

<span data-ttu-id="0b6c6-1965">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1965">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="0b6c6-1966">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1966">Keyword_german_passport2</span></span>

<span data-ttu-id="0b6c6-1967">bnationalit.t</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1967">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="0b6c6-1968">Номер идентификационной карты гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1968">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1969">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1969">Format</span></span>

<span data-ttu-id="0b6c6-1970">Начиная с 1 ноября 2010 г.: девяти только буквы и цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1970">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="0b6c6-1971">От 1 апреля 1987 до 31 октября 2010:10 цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1971">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1972">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1972">Pattern</span></span>

<span data-ttu-id="0b6c6-1973">С 1 ноября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1973">Since 1 November 2010:</span></span>
- <span data-ttu-id="0b6c6-1974">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1974">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-1975">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1975">Eight digits</span></span>

<span data-ttu-id="0b6c6-1976">От 1 апреля 1987 до 31 октября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1976">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="0b6c6-1977">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1977">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-1978">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1978">Checksum</span></span>

<span data-ttu-id="0b6c6-1979">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1979">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-1980">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1980">Definition</span></span>

<span data-ttu-id="0b6c6-1981">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1981">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-1982">регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1982">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-1983">находится ключевое слово из Keyword_germany_id_card.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1983">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-1984">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1984">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="0b6c6-1985">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1985">Keyword_germany_id_card</span></span>

- <span data-ttu-id="0b6c6-1986">Identity Card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1986">Identity Card</span></span>
- <span data-ttu-id="0b6c6-1987">ID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1987">ID</span></span>
- <span data-ttu-id="0b6c6-1988">Identification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1988">Identification</span></span>
- <span data-ttu-id="0b6c6-1989">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1989">Personalausweis</span></span>
- <span data-ttu-id="0b6c6-1990">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1990">Identifizierungsnummer</span></span>
- <span data-ttu-id="0b6c6-1991">Ausweis</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1991">Ausweis</span></span>
- <span data-ttu-id="0b6c6-1992">Identifikation</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1992">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="0b6c6-1993">Номер внутреннего удостоверения личности для Греции</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1993">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-1994">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1994">Format</span></span>

<span data-ttu-id="0b6c6-1995">Сочетание 7–8 букв и чисел, а также тире.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1995">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-1996">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1996">Pattern</span></span>

<span data-ttu-id="0b6c6-1997">Семь букв и чисел (старый формат):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1997">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="0b6c6-1998">одна буква (любая буква греческого алфавита);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1998">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="0b6c6-1999">Тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-1999">A dash</span></span> 
- <span data-ttu-id="0b6c6-2000">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2000">Six digits</span></span>

<span data-ttu-id="0b6c6-2001">Восемь букв и чисел (новый формат):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2001">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="0b6c6-2002">две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2002">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="0b6c6-2003">Тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2003">A dash</span></span> 
- <span data-ttu-id="0b6c6-2004">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2004">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2005">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2005">Checksum</span></span>

<span data-ttu-id="0b6c6-2006">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2006">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2007">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2007">Definition</span></span>

<span data-ttu-id="0b6c6-2008">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2008">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2009">регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2009">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2010">находится ключевое слово из Keyword_greece_id_card.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2010">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2011">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2011">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="0b6c6-2012">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2012">Keyword_greece_id_card</span></span>

- <span data-ttu-id="0b6c6-2013">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2013">Greek identity Card</span></span>
- <span data-ttu-id="0b6c6-2014">Tautotita</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2014">Tautotita</span></span>
- <span data-ttu-id="0b6c6-2015">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2015">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="0b6c6-2016">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2016">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="0b6c6-2017">Номер удостоверения личности для Гонконга (HKID)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2017">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2018">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2018">Format</span></span>

<span data-ttu-id="0b6c6-2019">Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2019">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2020">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2020">Pattern</span></span>

<span data-ttu-id="0b6c6-2021">Сочетание 8–9 букв:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2021">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="0b6c6-2022">1–2 буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2022">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-2023">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2023">Six digits</span></span> 
- <span data-ttu-id="0b6c6-2024">последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2024">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2025">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2025">Checksum</span></span>

<span data-ttu-id="0b6c6-2026">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2026">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2027">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2027">Definition</span></span>

<span data-ttu-id="0b6c6-2028">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2028">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2029">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2029">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2030">находится ключевое слово из Keyword_hong_kong_id_card;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2030">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="0b6c6-2031">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2031">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-2032">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2032">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2033">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2033">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2034">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2034">The checksum passes.</span></span>

```
<!-- Hong Kong Identity Card (HKID) number -->
<Entity id="e63c28a7-ad29-4c17-a41a-3d2a0b70fd9c" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_hong_kong_id_card"/>
     <Match idRef="Keyword_hong_kong_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_hong_kong_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2035">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2035">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="0b6c6-2036">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2036">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="0b6c6-2037">Номер идентификационной карты (Гонконг)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2037">hong kong identity card</span></span>
- <span data-ttu-id="0b6c6-2038">HKIDC</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2038">HKIDC</span></span>
- <span data-ttu-id="0b6c6-2039">Карточка</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2039">id card</span></span>
- <span data-ttu-id="0b6c6-2040">identity card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2040">identity card</span></span>
- <span data-ttu-id="0b6c6-2041">hk идентификационной карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2041">hk identity card</span></span>
- <span data-ttu-id="0b6c6-2042">идентификатор (Гонконг)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2042">hong kong id</span></span>
- <span data-ttu-id="0b6c6-2043">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2043">香港身份證</span></span>
- <span data-ttu-id="0b6c6-2044">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2044">香港永久性居民身份證</span></span>
- <span data-ttu-id="0b6c6-2045">身份證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2045">身份證</span></span>
- <span data-ttu-id="0b6c6-2046">身份証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2046">身份証</span></span>
- <span data-ttu-id="0b6c6-2047">身分證 </span><span class="sxs-lookup"><span data-stu-id="0b6c6-2047">身分證</span></span>
- <span data-ttu-id="0b6c6-2048">身分証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2048">身分証</span></span>
- <span data-ttu-id="0b6c6-2049">香港身份証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2049">香港身份証</span></span>
- <span data-ttu-id="0b6c6-2050">香港身分證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2050">香港身分證</span></span>
- <span data-ttu-id="0b6c6-2051">香港身分証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2051">香港身分証</span></span>
- <span data-ttu-id="0b6c6-2052">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2052">香港身份證</span></span>
- <span data-ttu-id="0b6c6-2053">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2053">香港居民身份證</span></span>
- <span data-ttu-id="0b6c6-2054">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2054">香港居民身份証</span></span>
- <span data-ttu-id="0b6c6-2055">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2055">香港居民身分證</span></span>
- <span data-ttu-id="0b6c6-2056">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2056">香港居民身分証</span></span>
- <span data-ttu-id="0b6c6-2057">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2057">香港永久性居民身份証</span></span>
- <span data-ttu-id="0b6c6-2058">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2058">香港永久性居民身分證</span></span>
- <span data-ttu-id="0b6c6-2059">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2059">香港永久性居民身分証</span></span>
- <span data-ttu-id="0b6c6-2060">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2060">香港永久性居民身份證</span></span>
- <span data-ttu-id="0b6c6-2061">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2061">香港非永久性居民身份證</span></span>
- <span data-ttu-id="0b6c6-2062">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2062">香港非永久性居民身份証</span></span>
- <span data-ttu-id="0b6c6-2063">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2063">香港非永久性居民身分證</span></span>
- <span data-ttu-id="0b6c6-2064">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2064">香港非永久性居民身分証</span></span>
- <span data-ttu-id="0b6c6-2065">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2065">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="0b6c6-2066">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2066">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="0b6c6-2067">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2067">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="0b6c6-2068">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2068">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="0b6c6-2069">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2069">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="0b6c6-2070">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2070">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="0b6c6-2071">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2071">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="0b6c6-2072">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2072">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="0b6c6-2073">Идентификационный номер налогоплательщика для Индии (PAN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2073">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2074">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2074">Format</span></span>

<span data-ttu-id="0b6c6-2075">10 букв или цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2075">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2076">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2076">Pattern</span></span>

<span data-ttu-id="0b6c6-2077">10 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2077">10 letters or digits:</span></span>
- <span data-ttu-id="0b6c6-2078">пять букв (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2078">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-2079">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2079">Four digits</span></span> 
- <span data-ttu-id="0b6c6-2080">буква, которая является алфавитным проверочным символом.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2080">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2081">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2081">Checksum</span></span>

<span data-ttu-id="0b6c6-2082">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2083">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2083">Definition</span></span>

<span data-ttu-id="0b6c6-2084">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2084">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2085">регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2085">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2086">находится ключевое слово из Keyword_india_permanent_account_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2086">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="0b6c6-2087">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2087">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2088">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2088">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="0b6c6-2089">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2089">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="0b6c6-2090">Permanent Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2090">Permanent Account Number</span></span> 
- <span data-ttu-id="0b6c6-2091">PAN
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2091">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="0b6c6-2092">Индивидуальный идентификационный номер (Aadhaar) для Индии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2092">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2093">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2093">Format</span></span>

<span data-ttu-id="0b6c6-2094">12 цифр, содержащих необязательные пробелы или тире.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2094">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2095">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2095">Pattern</span></span>

<span data-ttu-id="0b6c6-2096">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2096">12 digits:</span></span>
- <span data-ttu-id="0b6c6-2097">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2097">Four digits</span></span> 
- <span data-ttu-id="0b6c6-2098">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2098">An optional space or dash</span></span> 
- <span data-ttu-id="0b6c6-2099">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2099">Four digits</span></span> 
- <span data-ttu-id="0b6c6-2100">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2100">An optional space or dash</span></span> 
- <span data-ttu-id="0b6c6-2101">последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2101">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2102">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2102">Checksum</span></span>

<span data-ttu-id="0b6c6-2103">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2103">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2104">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2104">Definition</span></span>

<span data-ttu-id="0b6c6-p133">Политика защиты от потери данных — это 85% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: Func_india_aadhaar поиска контента, который соответствует шаблону. Ключевое слово из Keyword_india_aadhar найти. Контрольная сумма передает. Политики защиты от потери данных — 75% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: Func_india_aadhaar поиска контента, который соответствует шаблону. Контрольная сумма передает. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="0b6c6-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="0b6c6-2111">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2111">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="0b6c6-2112">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2112">Keyword_india_aadhar</span></span>
- <span data-ttu-id="0b6c6-2113">Aadhar</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2113">Aadhar</span></span>
- <span data-ttu-id="0b6c6-2114">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2114">Aadhaar</span></span>
- <span data-ttu-id="0b6c6-2115">UID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2115">UID</span></span>
- <span data-ttu-id="0b6c6-2116">आधार</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2116">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="0b6c6-2117">Номер удостоверения личности (KTP) для Индонезии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2117">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2118">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2118">Format</span></span>

<span data-ttu-id="0b6c6-2119">16 цифр, содержащих необязательные точки.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2119">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2120">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2120">Pattern</span></span>

<span data-ttu-id="0b6c6-2121">16 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2121">16 digits:</span></span>
- <span data-ttu-id="0b6c6-2122">две цифры (код провинции);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2122">Two-digit province code</span></span> 
- <span data-ttu-id="0b6c6-2123">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2123">A period (optional)</span></span> 
- <span data-ttu-id="0b6c6-2124">две цифры (код округа или города);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2124">Two-digit regency or city code</span></span> 
- <span data-ttu-id="0b6c6-2125">две цифры (код района);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2125">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="0b6c6-2126">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2126">A period (optional)</span></span> 
- <span data-ttu-id="0b6c6-2127">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2127">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="0b6c6-2128">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2128">A period (optional)</span></span> 
- <span data-ttu-id="0b6c6-2129">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2129">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2130">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2130">Checksum</span></span>

<span data-ttu-id="0b6c6-2131">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2131">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2132">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2132">Definition</span></span>

<span data-ttu-id="0b6c6-2133">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2133">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2134">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2134">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2135">находится ключевое слово из Keyword_indonesia_id_card.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2135">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="0b6c6-2136">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2137">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2137">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

```
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2138">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2138">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="0b6c6-2139">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2139">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="0b6c6-2140">KTP</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2140">KTP</span></span>
- <span data-ttu-id="0b6c6-2141">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2141">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="0b6c6-2142">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2142">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="0b6c6-2143">Международный номер банковского счета (IBAN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2143">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2144">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2144">Format</span></span>

<span data-ttu-id="0b6c6-2145">Код страны (две буквы), а также проверочные цифры (две) и номер bban (до 30 символов)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2145">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2146">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2146">Pattern</span></span>

<span data-ttu-id="0b6c6-2147">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2147">Pattern must include all of the following:</span></span>

- <span data-ttu-id="0b6c6-2148">Двухбуквенный код страны</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2148">Two-letter country code</span></span>
- <span data-ttu-id="0b6c6-2149">Две проверочные цифры (после которых может следовать пробел) </span><span class="sxs-lookup"><span data-stu-id="0b6c6-2149">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="0b6c6-2150">1–7 групп из четырех букв или цифр (могут разделяться пробелами)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2150">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="0b6c6-2151">1–3 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2151">1-3 letters or digits</span></span>

<span data-ttu-id="0b6c6-p134">Формат для названия каждой из стран немного отличается. Тип конфиденциальной информации IBAN применяется к следующим 60 странам:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="0b6c6-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2155">Checksum</span></span>

<span data-ttu-id="0b6c6-2156">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2156">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2157">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2157">Definition</span></span>

<span data-ttu-id="0b6c6-2158">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2158">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2159">функция Func_iban находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2159">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2160">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2160">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2161">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2161">Keywords</span></span>

<span data-ttu-id="0b6c6-2162">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2162">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="0b6c6-2163">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2163">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2164">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2164">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="0b6c6-2165">IPv4:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2165">IPv4:</span></span>
<span data-ttu-id="0b6c6-2166">Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2166">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="0b6c6-2167">Протокол IPv6</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2167">IPv6:</span></span>
<span data-ttu-id="0b6c6-2168"> Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2168">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2169">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2169">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2170">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2170">Checksum</span></span>

<span data-ttu-id="0b6c6-2171">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2172">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2172">Definition</span></span>

<span data-ttu-id="0b6c6-2173">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2173">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2174">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2174">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2175">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2175">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="0b6c6-2176">В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2176">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2177">регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2177">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2178">находится ключевое слово из Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2178">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="0b6c6-2179">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2179">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2180">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2180">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2181">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2181">No keyword from Keyword_ipaddress is found.</span></span>

```
    <!-- IP Address -->
    <Entity id="1daa4ad5-e2dd-4ca4-a788-54722c09efb2" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv4_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="95">
        <IdMatch idRef="Regex_ipv6_address" />
        <Any minMatches="1">
          <Match idRef="Keyword_ipaddress" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2182">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2182">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="0b6c6-2183">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2183">Keyword_ipaddress</span></span>

- <span data-ttu-id="0b6c6-2184">IP (ключевое слово с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2184">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="0b6c6-2185">ip address
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2185">ip address</span></span> 
- <span data-ttu-id="0b6c6-2186">ip addresses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2186">ip addresses</span></span>
- <span data-ttu-id="0b6c6-2187">internet protocol</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2187">internet protocol</span></span>
- <span data-ttu-id="0b6c6-2188">
IP-כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2188">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="0b6c6-2189">Международные классификации болезней (ICD 10 см)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2189">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2190">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2190">Format</span></span>

<span data-ttu-id="0b6c6-2191">Словарь</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2191">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2192">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2192">Pattern</span></span>

<span data-ttu-id="0b6c6-2193">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2193">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2194">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2194">Checksum</span></span>

<span data-ttu-id="0b6c6-2195">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2195">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2196">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2196">Definition</span></span>

<span data-ttu-id="0b6c6-2197">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2197">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2198">Ключевое слово из Dictionary_icd_10_cm найти.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2198">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="0b6c6-2199">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2199">Keywords</span></span>

<span data-ttu-id="0b6c6-p135">Любой терминов из словаря Dictionary_icd_10_cm ключевое слово, которого выполняется на основе [International классификации болезней, версия одной десятой, клинических изменения (ICD 10 см)](https://go.microsoft.com/fwlink/?linkid=852604). Этот тип только поиск терминов, не страхования коды.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="0b6c6-2202">Международные классификации болезней (ICD 9 CM)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2202">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2203">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2203">Format</span></span>

<span data-ttu-id="0b6c6-2204">Словарь</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2204">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2205">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2205">Pattern</span></span>

<span data-ttu-id="0b6c6-2206">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2206">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2207">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2207">Checksum</span></span>

<span data-ttu-id="0b6c6-2208">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2208">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2209">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2209">Definition</span></span>

<span data-ttu-id="0b6c6-2210">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2210">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2211">Ключевое слово из Dictionary_icd_9_cm найти.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2211">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2212">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2212">Keywords</span></span>

<span data-ttu-id="0b6c6-p136">Любой терминов из словаря Dictionary_icd_9_cm ключевое слово, которого выполняется на основе [International классификации болезней, Revision девятая, клинических изменения (ICD 9 см)](https://go.microsoft.com/fwlink/?linkid=852605). Этот тип только поиск терминов, не страхования коды.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="0b6c6-2215">Индивидуальный социальный номер (PPS) для Ирландии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2215">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2216">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2216">Format</span></span>

<span data-ttu-id="0b6c6-2217">Использован старый формат (до 31 декабря 2012 г.):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2217">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="0b6c6-2218">семь цифр, за которыми следуют 1–2 буквы. </span><span class="sxs-lookup"><span data-stu-id="0b6c6-2218">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="0b6c6-2219">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2219">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="0b6c6-2220">семь цифр, за которыми следуют две буквы.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2220">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2221">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2221">Pattern</span></span>

<span data-ttu-id="0b6c6-2222">Использован старый формат (до 31 декабря 2012 г.):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2222">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="0b6c6-2223">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2223">Seven digits</span></span> 
- <span data-ttu-id="0b6c6-2224">1–2 буквы (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2224">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="0b6c6-2225">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2225">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="0b6c6-2226">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2226">Seven digits</span></span> 
- <span data-ttu-id="0b6c6-2227">буква (без учета регистра), которая является алфавитным проверочным символом;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2227">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="0b6c6-2228">буква "A" или "H" (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2228">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2229">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2229">Checksum</span></span>

<span data-ttu-id="0b6c6-2230">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2230">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2231">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2231">Definition</span></span>

<span data-ttu-id="0b6c6-2232">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2232">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2233">Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2233">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2234">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2234">One of the following is true:</span></span>
    - <span data-ttu-id="0b6c6-2235">найдено ключевое слово из Keyword_ireland_pps;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2235">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="0b6c6-2236">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2236">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="0b6c6-2237">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2237">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-2238">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2238">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2239">функция Func_ireland_pps находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2239">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2240">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2240">The checksum passes.</span></span>

```
<!-- Ireland Personal Public Service (PPS) Number -->
<Entity id="1cdb674d-c19a-4fcf-9f4b-7f56cc87345a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_ireland_pps"/>
     <Any minMatches="1">
  <Match idRef="Keyword_ireland_pps"/>
  <Match idRef="Func_eu_date"/>
     </Any>
  </Pattern>
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Func_ireland_pps"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2241">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2241">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="0b6c6-2242">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2242">Keyword_ireland_pps</span></span>

- <span data-ttu-id="0b6c6-2243">Personal Public Service Number 
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2243">Personal Public Service Number</span></span> 
- <span data-ttu-id="0b6c6-2244">PPS Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2244">PPS Number</span></span> 
- <span data-ttu-id="0b6c6-2245">PPS Num
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2245">PPS Num</span></span> 
- <span data-ttu-id="0b6c6-2246">PPS No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2246">PPS No.</span></span> 
- <span data-ttu-id="0b6c6-2247">PPS #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2247">PPS #</span></span> 
- <span data-ttu-id="0b6c6-2248">PPS #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2248">PPS#</span></span> 
- <span data-ttu-id="0b6c6-2249">PPSN
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2249">PPSN</span></span> 
- <span data-ttu-id="0b6c6-2250">Public Services Card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2250">Public Services Card</span></span> 
- <span data-ttu-id="0b6c6-2251">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2251">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="0b6c6-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="0b6c6-2254">PSP
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2254">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="0b6c6-2255">Номер банковского счета для Израиля</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2255">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2256">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2256">Format</span></span>

<span data-ttu-id="0b6c6-2257">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2257">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2258">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2258">Pattern</span></span>

<span data-ttu-id="0b6c6-2259">С форматированием</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2259">Formatted:</span></span>
- <span data-ttu-id="0b6c6-2260">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2260">Two digits</span></span> 
- <span data-ttu-id="0b6c6-2261">Тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2261">A dash</span></span> 
- <span data-ttu-id="0b6c6-2262">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2262">Three digits</span></span> 
- <span data-ttu-id="0b6c6-2263">Тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2263">A dash</span></span> 
- <span data-ttu-id="0b6c6-2264">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2264">Eight digits</span></span>

<span data-ttu-id="0b6c6-2265">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2265">Unformatted:</span></span>
- <span data-ttu-id="0b6c6-2266">	13 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2266">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2267">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2267">Checksum</span></span>

<span data-ttu-id="0b6c6-2268">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2269">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2269">Definition</span></span>

<span data-ttu-id="0b6c6-2270">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2271">регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2271">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2272">находится ключевое слово из Keyword_israel_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2272">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```
<!-- Israel Bank Account Number -->
<Entity id="7d08b2ff-a0b9-437f-957c-aeddbf9b2b25" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_israel_bank_account_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_israel_bank_account_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2273">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2273">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="0b6c6-2274">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2274">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="0b6c6-2275">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2275">Bank Account Number</span></span> 
- <span data-ttu-id="0b6c6-2276">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2276">Bank Account</span></span> 
- <span data-ttu-id="0b6c6-2277">Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2277">Account Number</span></span> 
- <span data-ttu-id="0b6c6-2278">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2278">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="0b6c6-2279">Национальный идентификатор для Израиля</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2279">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2280">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2280">Format</span></span>

<span data-ttu-id="0b6c6-2281">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2281">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2282">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2282">Pattern</span></span>

<span data-ttu-id="0b6c6-2283">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2283">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2284">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2284">Checksum</span></span>

<span data-ttu-id="0b6c6-2285">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2285">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2286">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2286">Definition</span></span>

<span data-ttu-id="0b6c6-2287">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2288">функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2288">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2289">находится ключевое слово из Keyword_Israel_National_ID;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2289">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="0b6c6-2290">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2290">The checksum passes.</span></span>

```
<!-- Israel National ID Number -->
<Entity id="e05881f5-1db1-418c-89aa-a3ac5c5277ee" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_israeli_national_id_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_Israel_National_ID" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2291">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2291">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="0b6c6-2292">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2292">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="0b6c6-2293">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2293">מספר זהות</span></span> 
- <span data-ttu-id="0b6c6-2294">National ID Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2294">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="0b6c6-2295">Номер водительского удостоверения для Италии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2295">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2296">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2296">Format</span></span>

<span data-ttu-id="0b6c6-2297">Сочетание из 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2297">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2298">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2298">Pattern</span></span>

- <span data-ttu-id="0b6c6-2299">Сочетание 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2299">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="0b6c6-2300">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2300">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-2301">Буква "A" или "V" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2301">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-2302">Семь букв (без учета регистра), цифр или символов подчеркивания</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2302">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="0b6c6-2303">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2303">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2304">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2304">Checksum</span></span>

<span data-ttu-id="0b6c6-2305">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2305">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2306">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2306">Definition</span></span>

<span data-ttu-id="0b6c6-2307">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2308">регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2308">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2309">находится ключевое слово из Keyword_italy_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2309">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```
<!-- Italy Driver's license Number -->
<Entity id="97d6244f-9157-41bd-8e0c-9d669a5c4d71" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_italy_drivers_license_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_italy_drivers_license_number" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2310">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2310">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="0b6c6-2311">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2311">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="0b6c6-2312">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2312">numero di patente di guida</span></span> 
- <span data-ttu-id="0b6c6-2313">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2313">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="0b6c6-2314">Номер банковского счета для Японии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2314">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2315">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2315">Format</span></span>

<span data-ttu-id="0b6c6-2316">Семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2316">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2317">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2317">Pattern</span></span>

<span data-ttu-id="0b6c6-2318">Номер банковского счета:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2318">Bank account number:</span></span>
- <span data-ttu-id="0b6c6-2319">семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2319">Seven or eight digits</span></span>
- <span data-ttu-id="0b6c6-2320">Код филиала для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2320">Bank account branch code:</span></span>
- <span data-ttu-id="0b6c6-2321">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2321">Four digits</span></span> 
- <span data-ttu-id="0b6c6-2322">Пробел или тире (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2322">A space or dash (optional)</span></span> 
- <span data-ttu-id="0b6c6-2323">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2323">Three digits</span></span>

<span data-ttu-id="0b6c6-2324">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2324">Checksum</span></span>

<span data-ttu-id="0b6c6-2325">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2325">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2326">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2326">Definition</span></span>

<span data-ttu-id="0b6c6-2327">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2327">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2328">Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2328">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2329">Находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2329">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="0b6c6-2330">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2330">One of the following is true:</span></span>
- <span data-ttu-id="0b6c6-2331">функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2331">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2332">найдено ключевое слово из Keyword_jp_bank_branch_code.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2332">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="0b6c6-2333">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2333">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2334">функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2334">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2335">находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2335">A keyword from Keyword_jp_bank_account is found.</span></span>

```
<!-- Japan Bank Account Number -->
<Entity id="d354f95b-96ee-4b80-80bc-4377312b55bc" patternsProximity="300" recommendedConfidence="75">
  <Version minEngineVersion="15.01.0131.000">
    <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_jp_bank_account" />
          <Match idRef="Keyword_jp_bank_account" />
          <Any minMatches="1">
            <Match idRef="Func_jp_bank_account_branch_code" />
            <Match idRef="Keyword_jp_bank_branch_code" />
          </Any>
      </Pattern>
  </Version>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_bank_account" />
        <Match idRef="Keyword_jp_bank_account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2336">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2336">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="0b6c6-2337">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2337">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="0b6c6-2338">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2338">Checking Account Number</span></span> 
- <span data-ttu-id="0b6c6-2339">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2339">Checking Account</span></span> 
- <span data-ttu-id="0b6c6-2340">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2340">Checking Account #</span></span> 
- <span data-ttu-id="0b6c6-2341">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2341">Checking Acct Number</span></span> 
- <span data-ttu-id="0b6c6-2342">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2342">Checking Acct #</span></span> 
- <span data-ttu-id="0b6c6-2343">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2343">Checking Acct No.</span></span> 
- <span data-ttu-id="0b6c6-2344">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2344">Checking Account No.</span></span> 
- <span data-ttu-id="0b6c6-2345">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2345">Bank Account Number</span></span> 
- <span data-ttu-id="0b6c6-2346">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2346">Bank Account</span></span> 
- <span data-ttu-id="0b6c6-2347">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2347">Bank Account #</span></span> 
- <span data-ttu-id="0b6c6-2348">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2348">Bank Acct Number</span></span> 
- <span data-ttu-id="0b6c6-2349">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2349">Bank Acct #</span></span> 
- <span data-ttu-id="0b6c6-2350">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2350">Bank Acct No.</span></span> 
- <span data-ttu-id="0b6c6-2351">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2351">Bank Account No.</span></span> 
- <span data-ttu-id="0b6c6-2352">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2352">Savings Account Number</span></span> 
- <span data-ttu-id="0b6c6-2353">Учетная запись экономии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2353">Savings Account</span></span> 
- <span data-ttu-id="0b6c6-2354">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2354">Savings Account #</span></span> 
- <span data-ttu-id="0b6c6-2355">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2355">Savings Acct Number</span></span> 
- <span data-ttu-id="0b6c6-2356">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2356">Savings Acct #</span></span> 
- <span data-ttu-id="0b6c6-2357">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2357">Savings Acct No.</span></span> 
- <span data-ttu-id="0b6c6-2358">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2358">Savings Account No.</span></span> 
- <span data-ttu-id="0b6c6-2359">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2359">Debit Account Number</span></span> 
- <span data-ttu-id="0b6c6-2360">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2360">Debit Account</span></span> 
- <span data-ttu-id="0b6c6-2361">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2361">Debit Account #</span></span> 
- <span data-ttu-id="0b6c6-2362">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2362">Debit Acct Number</span></span> 
- <span data-ttu-id="0b6c6-2363">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2363">Debit Acct #</span></span> 
- <span data-ttu-id="0b6c6-2364">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2364">Debit Acct No.</span></span> 
- <span data-ttu-id="0b6c6-2365">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2365">Debit Account No.</span></span> 
- <span data-ttu-id="0b6c6-2366">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2366">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="0b6c6-2367">＃アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2367">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="0b6c6-2368">＃勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2368">＃勘定の確認</span></span> 
- <span data-ttu-id="0b6c6-2369">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2369">勘定番号の確認</span></span> 
- <span data-ttu-id="0b6c6-2370">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2370">口座番号の確認</span></span> 
- <span data-ttu-id="0b6c6-2371">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2371">銀行口座番号</span></span> 
- <span data-ttu-id="0b6c6-2372">銀行口座</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2372">銀行口座</span></span> 
- <span data-ttu-id="0b6c6-2373">銀行口座＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2373">銀行口座＃</span></span> 
- <span data-ttu-id="0b6c6-2374">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2374">銀行の勘定番号</span></span> 
- <span data-ttu-id="0b6c6-2375">銀行のacct＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2375">銀行のacct＃</span></span> 
- <span data-ttu-id="0b6c6-2376">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2376">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="0b6c6-2377">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2377">銀行口座番号</span></span>
- <span data-ttu-id="0b6c6-2378">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2378">普通預金口座番号</span></span> 
- <span data-ttu-id="0b6c6-2379">預金口座
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2379">預金口座</span></span> 
- <span data-ttu-id="0b6c6-2380">貯蓄口座＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2380">貯蓄口座＃</span></span> 
- <span data-ttu-id="0b6c6-2381">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2381">貯蓄勘定の数</span></span> 
- <span data-ttu-id="0b6c6-2382">貯蓄勘定＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2382">貯蓄勘定＃</span></span> 
- <span data-ttu-id="0b6c6-2383">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2383">貯蓄勘定番号</span></span> 
- <span data-ttu-id="0b6c6-2384">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2384">普通預金口座番号</span></span> 
- <span data-ttu-id="0b6c6-2385">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2385">引き落とし口座番号</span></span> 
- <span data-ttu-id="0b6c6-2386">口座番号</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2386">口座番号</span></span> 
- <span data-ttu-id="0b6c6-2387">口座番号＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2387">口座番号＃</span></span> 
- <span data-ttu-id="0b6c6-2388">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2388">デビットのacct番号</span></span> 
- <span data-ttu-id="0b6c6-2389">デビット勘定＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2389">デビット勘定＃</span></span> 
- <span data-ttu-id="0b6c6-2390">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2390">デビットACCTの番号</span></span> 
- <span data-ttu-id="0b6c6-2391">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2391">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="0b6c6-2392">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2392">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="0b6c6-2393">Otemachi</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2393">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="0b6c6-2394">Номер водительского удостоверения для Японии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2394">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2395">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2395">Format</span></span>

<span data-ttu-id="0b6c6-2396">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2396">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2397">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2397">Pattern</span></span>

<span data-ttu-id="0b6c6-2398">12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2398">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2399">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2399">Checksum</span></span>

<span data-ttu-id="0b6c6-2400">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2400">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2401">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2401">Definition</span></span>

<span data-ttu-id="0b6c6-2402">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2402">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2403">функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2403">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2404">находится ключевое слово из Keyword_jp_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2404">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2405">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2405">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="0b6c6-2406">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2406">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="0b6c6-2407">dl#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2407">dl#</span></span> 
- <span data-ttu-id="0b6c6-2408">СПИСОК РАССЫЛКИ #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2408">DL＃</span></span> 
- <span data-ttu-id="0b6c6-2409">dls#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2409">dls#</span></span> 
- <span data-ttu-id="0b6c6-2410">СПИСКИ РАССЫЛКИ #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2410">DLS＃</span></span> 
- <span data-ttu-id="0b6c6-2411">driver license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2411">driver license</span></span> 
- <span data-ttu-id="0b6c6-2412">driver licenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2412">driver licenses</span></span> 
- <span data-ttu-id="0b6c6-2413">drivers license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2413">drivers license</span></span> 
- <span data-ttu-id="0b6c6-2414">driver's license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2414">driver's license</span></span> 
- <span data-ttu-id="0b6c6-2415">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2415">drivers licenses</span></span> 
- <span data-ttu-id="0b6c6-2416">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2416">driver's licenses</span></span> 
- <span data-ttu-id="0b6c6-2417">driving licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2417">driving licence</span></span> 
- <span data-ttu-id="0b6c6-2418">lic#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2418">lic#</span></span> 
- <span data-ttu-id="0b6c6-2419">LIC #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2419">LIC＃</span></span> 
- <span data-ttu-id="0b6c6-2420">lics#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2420">lics#</span></span> 
- <span data-ttu-id="0b6c6-2421">Код состояния</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2421">state id</span></span> 
- <span data-ttu-id="0b6c6-2422">state identification
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2422">state identification</span></span> 
- <span data-ttu-id="0b6c6-2423">state identification number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2423">state identification number</span></span> 
- <span data-ttu-id="0b6c6-2424">低所得国＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2424">低所得国＃</span></span> 
- <span data-ttu-id="0b6c6-2425">免許証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2425">免許証</span></span> 
- <span data-ttu-id="0b6c6-2426">状態ID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2426">状態ID</span></span>
- <span data-ttu-id="0b6c6-2427">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2427">状態の識別</span></span> 
- <span data-ttu-id="0b6c6-2428">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2428">状態の識別番号</span></span> 
- <span data-ttu-id="0b6c6-2429">運転免許</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2429">運転免許</span></span> 
- <span data-ttu-id="0b6c6-2430">運転免許証</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2430">運転免許証</span></span> 
- <span data-ttu-id="0b6c6-2431">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2431">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="0b6c6-2432">Номер паспорта гражданина Японии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2432">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2433">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2433">Format</span></span>

<span data-ttu-id="0b6c6-2434">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2434">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2435">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2435">Pattern</span></span>

<span data-ttu-id="0b6c6-2436">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2436">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2437">Checksum</span></span>

<span data-ttu-id="0b6c6-2438">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2438">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2439">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2439">Definition</span></span>

<span data-ttu-id="0b6c6-2440">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2441">функция Func_jp_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2441">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2442">находится ключевое слово из Keyword_jp_passport.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2442">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2443">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2443">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="0b6c6-2444">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2444">Keyword_jp_passport</span></span>

- <span data-ttu-id="0b6c6-2445">パスポート
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2445">パスポート</span></span> 
- <span data-ttu-id="0b6c6-2446">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2446">パスポート番号</span></span> 
- <span data-ttu-id="0b6c6-2447">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2447">パスポートのNum</span></span> 
- <span data-ttu-id="0b6c6-2448">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2448">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="0b6c6-2449">Номер регистрации резидента Японии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2449">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2450">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2450">Format</span></span>

<span data-ttu-id="0b6c6-2451">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2451">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2452">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2452">Pattern</span></span>

<span data-ttu-id="0b6c6-2453">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2453">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2454">Checksum</span></span>

<span data-ttu-id="0b6c6-2455">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2455">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2456">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2456">Definition</span></span>

<span data-ttu-id="0b6c6-2457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2458">функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2458">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2459">находится ключевое слово из Keyword_jp_resident_registration_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2459">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2460">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="0b6c6-2461">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2461">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="0b6c6-2462">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2462">Resident Registration Number</span></span>
- <span data-ttu-id="0b6c6-2463">Resident Register Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2463">Resident Register Number</span></span> 
- <span data-ttu-id="0b6c6-2464">Residents Basic Registry Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2464">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="0b6c6-2465">Resident Registration No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2465">Resident Registration No.</span></span> 
- <span data-ttu-id="0b6c6-2466">Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2466">Resident Register No.</span></span> 
- <span data-ttu-id="0b6c6-2467">Residents Basic Registry No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2467">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="0b6c6-2468">Basic Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2468">Basic Resident Register No.</span></span> 
- <span data-ttu-id="0b6c6-2469">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2469">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="0b6c6-2470">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2470">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="0b6c6-2471">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2471">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="0b6c6-2472">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2472">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="0b6c6-2473">Номер карты социального страхования для Японии (SIN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2473">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2474">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2474">Format</span></span>

<span data-ttu-id="0b6c6-2475">7–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2475">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2476">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2476">Pattern</span></span>

<span data-ttu-id="0b6c6-2477">7–12 цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2477">7-12 digits:</span></span>
- <span data-ttu-id="0b6c6-2478">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2478">Four digits</span></span> 
- <span data-ttu-id="0b6c6-2479">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2479">A hyphen (optional)</span></span> 
- <span data-ttu-id="0b6c6-2480">Шести цифр или</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2480">Six digits OR</span></span>
- <span data-ttu-id="0b6c6-2481">7–12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2481">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2482">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2482">Checksum</span></span>

<span data-ttu-id="0b6c6-2483">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2483">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2484">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2484">Definition</span></span>

<span data-ttu-id="0b6c6-2485">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2485">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2486">функция Func_jp_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2486">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2487">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2487">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="0b6c6-2488">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2488">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2489">функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2489">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2490">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2490">A keyword from Keyword_jp_sin is found.</span></span>

```
<!-- Japan Social Insurance Number -->
<Entity id="c840e719-0896-45bb-84fd-1ed5c95e45ff" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_jp_sin" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_sin_pre_1997" />
        <Match idRef="Keyword_jp_sin" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2491">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2491">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="0b6c6-2492">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2492">Keyword_jp_sin</span></span>

- <span data-ttu-id="0b6c6-2493">Social Insurance No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2493">Social Insurance No.</span></span> 
- <span data-ttu-id="0b6c6-2494">Social Insurance Num
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2494">Social Insurance Num</span></span> 
- <span data-ttu-id="0b6c6-2495">Social Insurance Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2495">Social Insurance Number</span></span> 
- <span data-ttu-id="0b6c6-2496">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2496">社会保険のテンキー</span></span> 
- <span data-ttu-id="0b6c6-2497">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2497">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="0b6c6-2498">Номер карты проживания японского языка</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2498">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2499">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2499">Format</span></span>

<span data-ttu-id="0b6c6-2500">12 только буквы и цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2500">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2501">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2501">Pattern</span></span>

<span data-ttu-id="0b6c6-2502">12 только буквы и цифры:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2502">12 letters and digits:</span></span>
- <span data-ttu-id="0b6c6-2503">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2503">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="0b6c6-2504">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2504">Eight digits</span></span> 
- <span data-ttu-id="0b6c6-2505">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2505">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2506">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2506">Checksum</span></span>

<span data-ttu-id="0b6c6-2507">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2507">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2508">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2508">Definition</span></span>

<span data-ttu-id="0b6c6-2509">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2509">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2510">Регулярное выражение Regex_jp_residence_card_number находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2510">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2511">Ключевое слово из Keyword_jp_residence_card_number найти.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2511">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2512">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2512">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="0b6c6-2513">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2513">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="0b6c6-2514">Номер карты проживания</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2514">Residence card number</span></span>
- <span data-ttu-id="0b6c6-2515">Проживания карточками нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2515">Residence card no</span></span>
- <span data-ttu-id="0b6c6-2516">Проживания карт #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2516">Residence card #</span></span>
- <span data-ttu-id="0b6c6-2517">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2517">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="0b6c6-2518">Номер удостоверения личности для Малайзии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2518">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2519">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2519">Format</span></span>

<span data-ttu-id="0b6c6-2520">12 цифр, содержащих необязательные дефисы.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2520">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2521">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2521">Pattern</span></span>

<span data-ttu-id="0b6c6-2522">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2522">12 digits:</span></span>
- <span data-ttu-id="0b6c6-2523">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2523">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="0b6c6-2524">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2524">A dash (optional)</span></span> 
- <span data-ttu-id="0b6c6-2525">код места рождения из двух букв;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2525">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="0b6c6-2526">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2526">A dash (optional)</span></span> 
- <span data-ttu-id="0b6c6-2527">три случайные цифры;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2527">Three random digits</span></span> 
- <span data-ttu-id="0b6c6-2528">код пола из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2528">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2529">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2529">Checksum</span></span>

<span data-ttu-id="0b6c6-2530">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2530">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2531">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2531">Definition</span></span>

<span data-ttu-id="0b6c6-2532">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2532">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2533">регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2533">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2534">находится ключевое слово из Keyword_malaysia_id_card_number.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2534">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2535">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2535">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="0b6c6-2536">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2536">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="0b6c6-2537">Карточка цифровой приложения</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2537">digital application card</span></span>
- <span data-ttu-id="0b6c6-2538">я / c</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2538">i/c</span></span>
- <span data-ttu-id="0b6c6-2539">я / c нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2539">i/c no</span></span>
- <span data-ttu-id="0b6c6-2540">IC</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2540">ic</span></span>
- <span data-ttu-id="0b6c6-2541">IC нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2541">ic no</span></span>
- <span data-ttu-id="0b6c6-2542">Карточка</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2542">id card</span></span>
- <span data-ttu-id="0b6c6-2543">Идентификация карточки</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2543">identification Card</span></span>
- <span data-ttu-id="0b6c6-2544">identity card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2544">identity card</span></span>
- <span data-ttu-id="0b6c6-2545">k/p</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2545">k/p</span></span>
- <span data-ttu-id="0b6c6-2546">k/p не</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2546">k/p no</span></span>
- <span data-ttu-id="0b6c6-2547">kad akuan diri</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2547">kad akuan diri</span></span>
- <span data-ttu-id="0b6c6-2548">цифровой aplikasi kad</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2548">kad aplikasi digital</span></span>
- <span data-ttu-id="0b6c6-2549">Малайзия pengenalan kad</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2549">kad pengenalan malaysia</span></span>
- <span data-ttu-id="0b6c6-2550">ключевого</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2550">kp</span></span>
- <span data-ttu-id="0b6c6-2551">ключевого нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2551">kp no</span></span>
- <span data-ttu-id="0b6c6-2552">mykad</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2552">mykad</span></span>
- <span data-ttu-id="0b6c6-2553">mykas</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2553">mykas</span></span>
- <span data-ttu-id="0b6c6-2554">mykid</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2554">mykid</span></span>
- <span data-ttu-id="0b6c6-2555">mypr</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2555">mypr</span></span>
- <span data-ttu-id="0b6c6-2556">mytentera</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2556">mytentera</span></span>
- <span data-ttu-id="0b6c6-2557">Малайзия идентификационной карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2557">malaysia identity card</span></span>
- <span data-ttu-id="0b6c6-2558">малазийскую идентификационной карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2558">malaysian identity card</span></span>
- <span data-ttu-id="0b6c6-2559">nric</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2559">nric</span></span>
- <span data-ttu-id="0b6c6-2560">Личная карточка идентификации</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2560">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="0b6c6-2561">Номер гражданской службы для Нидерландов (BSN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2561">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2562">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2562">Format</span></span>

<span data-ttu-id="0b6c6-2563">8–9 цифр, содержащих необязательные пробелы.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2563">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2564">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2564">Pattern</span></span>

<span data-ttu-id="0b6c6-2565">8–9 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2565">8-9 digits:</span></span>
- <span data-ttu-id="0b6c6-2566">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2566">Three digits</span></span> 
- <span data-ttu-id="0b6c6-2567">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="0b6c6-2567">A space (optional)</span></span> 
- <span data-ttu-id="0b6c6-2568">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2568">Three digits</span></span> 
- <span data-ttu-id="0b6c6-2569">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="0b6c6-2569">A space (optional)</span></span> 
- <span data-ttu-id="0b6c6-2570">2–3 цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2570">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2571">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2571">Checksum</span></span>

<span data-ttu-id="0b6c6-2572">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2572">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2573">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2573">Definition</span></span>

<span data-ttu-id="0b6c6-2574">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2574">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2575">функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2575">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2576">находится ключевое слово из Keyword_netherlands_bsn;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2576">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="0b6c6-2577">функция Func_eu_date2 находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2577">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="0b6c6-2578">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2578">The checksum passes.</span></span>

```
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2579">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2579">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="0b6c6-2580">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2580">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="0b6c6-2581">Citizen service number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2581">Citizen service number</span></span> 
- <span data-ttu-id="0b6c6-2582">BSN

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2582">BSN</span></span> 
- <span data-ttu-id="0b6c6-2583">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2583">Burgerservicenummer</span></span> 
- <span data-ttu-id="0b6c6-2584">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2584">Sofinummer</span></span> 
- <span data-ttu-id="0b6c6-2585">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2585">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="0b6c6-2586">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2586">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="0b6c6-2587">Номер министерства здравоохранения для Новой Зеландии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2587">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2588">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2588">Format</span></span>

<span data-ttu-id="0b6c6-2589">Три буквы, пробел (необязательно) и четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2589">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2590">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2590">Pattern</span></span>

<span data-ttu-id="0b6c6-2591">Три буквы (не регистр) четырех цифр пространства (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2591">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2592">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2592">Checksum</span></span>

<span data-ttu-id="0b6c6-2593">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2593">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2594">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2594">Definition</span></span>

<span data-ttu-id="0b6c6-2595">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2596">функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2596">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2597">находится ключевое слово из Keyword_nz_terms;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2597">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="0b6c6-2598">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2598">The checksum passes.</span></span>

```
<!-- New Zealand Health Number -->
<Entity id="2b71c1c8-d14e-4430-82dc-fd1ed6bf05c7" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_new_zealand_ministry_of_health_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_nz_terms" />
        </Any>
    </Pattern>
</Entity>
```

<span data-ttu-id="0b6c6-2599">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2599">Keywords</span></span>

<span data-ttu-id="0b6c6-2600">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2600">Keyword_nz_terms</span></span>

- <span data-ttu-id="0b6c6-2601">NHI
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2601">NHI</span></span> 
- <span data-ttu-id="0b6c6-2602">Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2602">New Zealand</span></span> 
- <span data-ttu-id="0b6c6-2603">Работоспособность</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2603">Health</span></span> 
- <span data-ttu-id="0b6c6-2604">treatment
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2604">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="0b6c6-2605">Идентификационный номер для Норвегии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2605">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2606">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2606">Format</span></span>

<span data-ttu-id="0b6c6-2607">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2607">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2608">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2608">Pattern</span></span>

<span data-ttu-id="0b6c6-2609">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2609">11 digits:</span></span>
- <span data-ttu-id="0b6c6-2610">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2610">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="0b6c6-2611">индивидуальный номер из трех цифр;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2611">Three-digit individual number</span></span> 
- <span data-ttu-id="0b6c6-2612">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2612">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2613">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2613">Checksum</span></span>

<span data-ttu-id="0b6c6-2614">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2614">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2615">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2615">Definition</span></span>

<span data-ttu-id="0b6c6-2616">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2616">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2617">функция Func_norway_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2617">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2618">находится ключевое слово из Keyword_norway_id_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2618">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="0b6c6-2619">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2619">The checksum passes.</span></span>
- <span data-ttu-id="0b6c6-2620">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2620">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2621">функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2621">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2622">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2622">The checksum passes.</span></span>

```
<!-- Norway Identification Number -->
<Entity id="d4c8a798-e9f2-4bd3-9652-500d24080fc3" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_norway_id_number"/>
     <Match idRef="Keyword_norway_id_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_norway_id_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2623">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2623">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="0b6c6-2624">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2624">Keyword_norway_id_number</span></span>

- <span data-ttu-id="0b6c6-2625">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2625">Personal identification number</span></span>
- <span data-ttu-id="0b6c6-2626">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2626">Norwegian ID Number</span></span>
- <span data-ttu-id="0b6c6-2627">ID Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2627">ID Number</span></span>
- <span data-ttu-id="0b6c6-2628">Identification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2628">Identification</span></span>
- <span data-ttu-id="0b6c6-2629">Personnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2629">Personnummer</span></span>
- <span data-ttu-id="0b6c6-2630">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2630">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="0b6c6-2631">Единый многофункциональный идентификационный номер для Филиппин</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2631">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2632">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2632">Format</span></span>

<span data-ttu-id="0b6c6-2633">12 цифр, разделенных дефисами.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2633">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2634">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2634">Pattern</span></span>

<span data-ttu-id="0b6c6-2635">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2635">12 digits:</span></span>
- <span data-ttu-id="0b6c6-2636">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2636">Four digits</span></span> 
- <span data-ttu-id="0b6c6-2637">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2637">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-2638">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2638">Seven digits</span></span> 
- <span data-ttu-id="0b6c6-2639">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2639">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-2640">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2640">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2641">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2641">Checksum</span></span>

<span data-ttu-id="0b6c6-2642">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2642">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2643">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2643">Definition</span></span>

<span data-ttu-id="0b6c6-2644">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2644">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2645">регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2645">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2646">находится ключевое слово из Keyword_philippines_id.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2646">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2647">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2647">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="0b6c6-2648">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2648">Keyword_philippines_id</span></span>

- <span data-ttu-id="0b6c6-2649">Unified Multi-Purpose ID
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2649">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="0b6c6-2650">UMID
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2650">UMID</span></span> 
- <span data-ttu-id="0b6c6-2651">Identity Card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2651">Identity Card</span></span> 
- <span data-ttu-id="0b6c6-2652">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2652">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="0b6c6-2653">Номер удостоверения личности для Польши</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2653">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2654">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2654">Format</span></span>

<span data-ttu-id="0b6c6-2655">Три буквы и шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2655">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2656">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2656">Pattern</span></span>

<span data-ttu-id="0b6c6-2657">Три буквы (без учета регистра), за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2657">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2658">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2658">Checksum</span></span>

<span data-ttu-id="0b6c6-2659">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2659">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2660">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2660">Definition</span></span>

<span data-ttu-id="0b6c6-p138">Политики защиты от потери данных — 75% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: Func_polish_national_id поиска контента, который соответствует шаблону. Ключевое слово из Keyword_polish_national_id_passport_number найти. Контрольная сумма передает.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2664">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2664">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="0b6c6-2665">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2665">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="0b6c6-2666">Dowód osobisty</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2666">Dowód osobisty</span></span>
- <span data-ttu-id="0b6c6-2667">Номер dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2667">Numer dowodu osobistego</span></span>
- <span data-ttu-id="0b6c6-2668">Nazwa я osobistego dowodu номер</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2668">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="0b6c6-2669">Nazwa я nr dowodu osobistego</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2669">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="0b6c6-2670">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2670">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="0b6c6-2671">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2671">Dowód Tożsamości</span></span>
- <span data-ttu-id="0b6c6-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p139">dow. os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="0b6c6-2674">Национальный идентификатор (PESEL), Польша</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2674">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2675">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2675">Format</span></span>

<span data-ttu-id="0b6c6-2676">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2676">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2677">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2677">Pattern</span></span>

<span data-ttu-id="0b6c6-2678">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2678">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2679">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2679">Checksum</span></span>

<span data-ttu-id="0b6c6-2680">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2680">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2681">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2681">Definition</span></span>

<span data-ttu-id="0b6c6-2682">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2682">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2683">функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2683">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2684">находится ключевое слово из Keyword_pesel_identification_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2684">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="0b6c6-2685">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2685">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2686">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2686">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="0b6c6-2687">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2687">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="0b6c6-2688">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2688">Nr PESEL</span></span>
- <span data-ttu-id="0b6c6-2689">PESEL</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2689">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="0b6c6-2690">Номер паспорта для Польши</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2690">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2691">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2691">Format</span></span>

<span data-ttu-id="0b6c6-2692">Две буквы и семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2692">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2693">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2693">Pattern</span></span>

<span data-ttu-id="0b6c6-2694">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2694">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2695">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2695">Checksum</span></span>

<span data-ttu-id="0b6c6-2696">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2696">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2697">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2697">Definition</span></span>

<span data-ttu-id="0b6c6-2698">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2698">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2699">функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2699">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2700">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2700">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="0b6c6-2701">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2701">The checksum passes.</span></span>

```
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2702">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2702">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="0b6c6-2703">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2703">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="0b6c6-2704">Номер paszportu</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2704">Numer paszportu</span></span>
- <span data-ttu-id="0b6c6-p140">Paszportu nr.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p140">Nr. Paszportu</span></span>
- <span data-ttu-id="0b6c6-2707">Paszport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2707">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="0b6c6-2708">Номер карты гражданина Португалии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2708">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2709">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2709">Format</span></span>

<span data-ttu-id="0b6c6-2710">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2710">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2711">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2711">Pattern</span></span>

<span data-ttu-id="0b6c6-2712">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2712">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2713">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2713">Checksum</span></span>

<span data-ttu-id="0b6c6-2714">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2714">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2715">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2715">Definition</span></span>

<span data-ttu-id="0b6c6-2716">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2716">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2717">регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2717">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2718">находится ключевое слово из Keyword_portugal_citizen_card.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2718">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2719">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2719">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="0b6c6-2720">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2720">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="0b6c6-2721">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2721">Citizen Card</span></span>
- <span data-ttu-id="0b6c6-2722">National ID Card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2722">National ID Card</span></span>
- <span data-ttu-id="0b6c6-2723">CC</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2723">CC</span></span>
- <span data-ttu-id="0b6c6-2724">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2724">Cartão de Cidadão</span></span>
- <span data-ttu-id="0b6c6-2725">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2725">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="0b6c6-2726">Национальный идентификатор для Саудовской Аравии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2726">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2727">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2727">Format</span></span>

<span data-ttu-id="0b6c6-2728">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2728">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2729">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2729">Pattern</span></span>

<span data-ttu-id="0b6c6-2730">10 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2730">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2731">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2731">Checksum</span></span>

<span data-ttu-id="0b6c6-2732">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2732">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2733">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2733">Definition</span></span>

<span data-ttu-id="0b6c6-2734">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2734">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2735">регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2735">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2736">находится ключевое слово из Keyword_saudi_arabia_national_id.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2736">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```
<!-- Saudi Arabia National ID -->
<Entity id="8c5a0ba8-404a-41a3-8871-746aa21ee6c0" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_saudi_arabia_national_id" />
        <Any minMatches="1">
          <Match idRef="Keyword_saudi_arabia_national_id" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2737">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2737">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="0b6c6-2738">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2738">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="0b6c6-2739">Identification Card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2739">Identification Card</span></span> 
- <span data-ttu-id="0b6c6-2740">I card number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2740">I card number</span></span> 
- <span data-ttu-id="0b6c6-2741">идентификатор</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2741">ID number</span></span> 
- <span data-ttu-id="0b6c6-2742">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2742">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="0b6c6-2743">Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2743">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2744">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2744">Format</span></span>

<span data-ttu-id="0b6c6-2745">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2745">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2746">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2746">Pattern</span></span>

- <span data-ttu-id="0b6c6-2747">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2747">Nine letters and digits:</span></span>
- <span data-ttu-id="0b6c6-2748">буква "F", "G", "S" или "T" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2748">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-2749">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2749">Seven digits</span></span> 
- <span data-ttu-id="0b6c6-2750">алфавитный проверочный символ.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2750">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2751">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2751">Checksum</span></span>

<span data-ttu-id="0b6c6-2752">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2752">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2753">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2753">Definition</span></span>

<span data-ttu-id="0b6c6-2754">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2754">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2755">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2755">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2756">находится ключевое слово из Keyword_singapore_nric;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2756">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="0b6c6-2757">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2757">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-2758">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2758">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2759">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2759">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2760">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2760">The checksum passes.</span></span>

```
<!-- Singapore National Registration Identity Card (NRIC) Number -->
<Entity id="cead390a-dd83-4856-9751-fb6dc98c34da" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_singapore_nric"/>
     <Match idRef="Keyword_singapore_nric"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_singapore_nric"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2761">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2761">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="0b6c6-2762">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2762">Keyword_singapore_nric</span></span>

- <span data-ttu-id="0b6c6-2763">National Registration Identity Card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2763">National Registration Identity Card</span></span> 
- <span data-ttu-id="0b6c6-2764">Identity Card Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2764">Identity Card Number</span></span> 
- <span data-ttu-id="0b6c6-2765">NRIC
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2765">NRIC</span></span> 
- <span data-ttu-id="0b6c6-2766">IC
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2766">IC</span></span> 
- <span data-ttu-id="0b6c6-2767">Foreign Identification Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2767">Foreign Identification Number</span></span> 
- <span data-ttu-id="0b6c6-2768">FIN
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2768">FIN</span></span> 
- <span data-ttu-id="0b6c6-2769">身份证 </span><span class="sxs-lookup"><span data-stu-id="0b6c6-2769">身份证</span></span> 
- <span data-ttu-id="0b6c6-2770">身份證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2770">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="0b6c6-2771">Идентификационный номер для Южной Африки</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2771">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2772">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2772">Format</span></span>

<span data-ttu-id="0b6c6-2773">13 цифр, которые могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2773">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2774">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2774">Pattern</span></span>

<span data-ttu-id="0b6c6-2775">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2775">13 digits:</span></span>
- <span data-ttu-id="0b6c6-2776">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2776">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="0b6c6-2777">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2777">Four digits</span></span> 
- <span data-ttu-id="0b6c6-2778">индикатор гражданства в виде одной цифры;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2778">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="0b6c6-2779">цифра "8" или "9";</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2779">The digit "8" or "9"</span></span> 
- <span data-ttu-id="0b6c6-2780">одна цифра (проверочная).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2780">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2781">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2781">Checksum</span></span>

<span data-ttu-id="0b6c6-2782">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2782">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2783">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2783">Definition</span></span>

<span data-ttu-id="0b6c6-2784">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2785">функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2785">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2786">находится ключевое слово из Keyword_south_africa_identification_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2786">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="0b6c6-2787">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2787">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2788">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2788">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="0b6c6-2789">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2789">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="0b6c6-2790">Identity card</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2790">Identity card</span></span>
- <span data-ttu-id="0b6c6-2791">ID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2791">ID</span></span>
- <span data-ttu-id="0b6c6-2792">Identification</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2792">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="0b6c6-2793">Регистрационный номер жителя Южной Кореи</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2793">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2794">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2794">Format</span></span>

<span data-ttu-id="0b6c6-2795">13 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2795">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2796">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2796">Pattern</span></span>

<span data-ttu-id="0b6c6-2797">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2797">13 digits:</span></span>
- <span data-ttu-id="0b6c6-2798">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2798">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="0b6c6-2799">дефис;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2799">A hyphen</span></span> 
- <span data-ttu-id="0b6c6-2800">одна цифра (определяет век и пол);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2800">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="0b6c6-2801">код региона рождения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2801">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="0b6c6-2802">одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2802">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="0b6c6-2803">проверочная цифра.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2803">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2804">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2804">Checksum</span></span>

<span data-ttu-id="0b6c6-2805">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2805">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2806">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2806">Definition</span></span>

<span data-ttu-id="0b6c6-2807">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2807">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2808">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2808">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2809">находится ключевое слово из Keyword_south_korea_resident_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2809">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="0b6c6-2810">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2810">The checksum passes.</span></span>

<span data-ttu-id="0b6c6-2811">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2811">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2812">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2812">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2813">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2813">The checksum passes.</span></span>

```
<!-- South Korea Resident Registration Number -->
<Entity id="5b802e18-ba80-44c4-bc83-bf2ad36ae36a" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_korea_resident_number"/>
     <Match idRef="Keyword_south_korea_resident_number"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_south_korea_resident_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2814">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2814">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="0b6c6-2815">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2815">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="0b6c6-2816">National ID card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2816">National ID card</span></span> 
- <span data-ttu-id="0b6c6-2817">Citizen's Registration Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2817">Citizen's Registration Number</span></span> 
- <span data-ttu-id="0b6c6-2818">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2818">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="0b6c6-2819">RRN
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2819">RRN</span></span> 
- <span data-ttu-id="0b6c6-2820">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2820">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="0b6c6-2821">Страховой номер для Испании (SSN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2821">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2822">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2822">Format</span></span>

<span data-ttu-id="0b6c6-2823">11–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2823">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2824">Pattern</span></span>

<span data-ttu-id="0b6c6-2825">цифры 11-12:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2825">11-12 digits:</span></span>
- <span data-ttu-id="0b6c6-2826">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2826">Two digits</span></span> 
- <span data-ttu-id="0b6c6-2827">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2827">A forward slash (optional)</span></span> 
- <span data-ttu-id="0b6c6-2828">7–8 цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2828">7-8 digits</span></span> 
- <span data-ttu-id="0b6c6-2829">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2829">A forward slash (optional)</span></span> 
- <span data-ttu-id="0b6c6-2830">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2830">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2831">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2831">Checksum</span></span>

<span data-ttu-id="0b6c6-2832">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2832">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2833">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2833">Definition</span></span>

<span data-ttu-id="0b6c6-2834">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2834">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2835">функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2835">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2836">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2836">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2837">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2837">Keywords</span></span>

<span data-ttu-id="0b6c6-2838">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2838">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="0b6c6-2839">Национальный идентификатор для Швеции</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2839">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2840">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2840">Format</span></span>

<span data-ttu-id="0b6c6-2841">10 или 12 цифр и дополнительный разделитель.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2841">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2842">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2842">Pattern</span></span>

<span data-ttu-id="0b6c6-2843">10 или 12 цифр с необязательным разделителем</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2843">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="0b6c6-2844">2–4 цифры (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2844">2-4 digits (optional)</span></span> 
- <span data-ttu-id="0b6c6-2845">Шесть цифр в формате даты ГГММДД.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2845">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="0b6c6-2846">Разделитель - или + (необязательно)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2846">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="0b6c6-2847">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2847">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2848">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2848">Checksum</span></span>

<span data-ttu-id="0b6c6-2849">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2849">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2850">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2850">Definition</span></span>

<span data-ttu-id="0b6c6-2851">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2851">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2852">функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2852">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2853">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2853">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2854">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2854">Keywords</span></span>

<span data-ttu-id="0b6c6-2855">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2855">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="0b6c6-2856">Номер паспорта гражданина Швеции</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2856">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2857">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2857">Format</span></span>

<span data-ttu-id="0b6c6-2858">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2858">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2859">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2859">Pattern</span></span>

<span data-ttu-id="0b6c6-2860">Восемь последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2860">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2861">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2861">Checksum</span></span>

<span data-ttu-id="0b6c6-2862">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2862">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2863">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2863">Definition</span></span>

<span data-ttu-id="0b6c6-2864">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2864">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2865">Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2865">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2866">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2866">One of the following is true:</span></span>
    - <span data-ttu-id="0b6c6-2867">найдено ключевое слово из Keyword_passport;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2867">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="0b6c6-2868">найдено ключевое слово из Keyword_sweden_passport.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2868">A keyword from Keyword_sweden_passport is found.</span></span>

```
<!-- Sweden Passport Number -->
<Entity id="ba4e7456-55a9-4d89-9140-c33673553526" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_sweden_passport_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_passport" />
          <Match idRef="Keyword_sweden_passport" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2869">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2869">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="0b6c6-2870">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2870">Keyword_sweden_passport</span></span>

- <span data-ttu-id="0b6c6-2871">visa requirements
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2871">visa requirements</span></span> 
- <span data-ttu-id="0b6c6-2872">Alien Registration Card
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2872">Alien Registration Card</span></span> 
- <span data-ttu-id="0b6c6-2873">Schengen visas
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2873">Schengen visas</span></span> 
- <span data-ttu-id="0b6c6-2874">Schengen visa
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2874">Schengen visa</span></span> 
- <span data-ttu-id="0b6c6-2875">Visa Processing
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2875">Visa Processing</span></span> 
- <span data-ttu-id="0b6c6-2876">Visa Type
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2876">Visa Type</span></span> 
- <span data-ttu-id="0b6c6-2877">Single Entry
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2877">Single Entry</span></span> 
- <span data-ttu-id="0b6c6-2878">Multiple Entry
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2878">Multiple Entry</span></span> 
- <span data-ttu-id="0b6c6-2879">G3 Processing Fees

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2879">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="0b6c6-2880">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2880">Keyword_passport</span></span>

- <span data-ttu-id="0b6c6-2881">Passport Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2881">Passport Number</span></span> 
- <span data-ttu-id="0b6c6-2882">
Passport No</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2882">Passport No</span></span> 
- <span data-ttu-id="0b6c6-2883">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2883">Passport #</span></span> 
- <span data-ttu-id="0b6c6-2884">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2884">Passport#</span></span> 
- <span data-ttu-id="0b6c6-2885">PassportID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2885">PassportID</span></span> 
- <span data-ttu-id="0b6c6-2886">Passportno
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2886">Passportno</span></span> 
- <span data-ttu-id="0b6c6-2887">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2887">passportnumber</span></span> 
- <span data-ttu-id="0b6c6-2888">パスポート</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2888">パスポート</span></span> 
- <span data-ttu-id="0b6c6-2889">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2889">パスポート番号</span></span> 
- <span data-ttu-id="0b6c6-2890">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2890">パスポートのNum</span></span> 
- <span data-ttu-id="0b6c6-2891">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2891">パスポート＃</span></span> 
- <span data-ttu-id="0b6c6-2892">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2892">Numéro de passeport</span></span> 
- <span data-ttu-id="0b6c6-2893">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2893">Passeport n °</span></span> 
- <span data-ttu-id="0b6c6-2894">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2894">Passeport Non</span></span> 
- <span data-ttu-id="0b6c6-2895">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2895">Passeport #</span></span> 
- <span data-ttu-id="0b6c6-2896">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2896">Passeport#</span></span> 
- <span data-ttu-id="0b6c6-2897">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2897">PasseportNon</span></span> 
- <span data-ttu-id="0b6c6-2898">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2898">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="0b6c6-2899">Код SWIFT</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2899">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2900">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2900">Format</span></span>

<span data-ttu-id="0b6c6-2901">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2901">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2902">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2902">Pattern</span></span>

<span data-ttu-id="0b6c6-2903">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2903">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="0b6c6-2904">Четырехбуквенный код банка (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2904">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-2905">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2905">An optional space</span></span> 
- <span data-ttu-id="0b6c6-2906">4–28 букв или цифр (основной номер банковского счета, BBAN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2906">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="0b6c6-2907">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2907">An optional space</span></span> 
- <span data-ttu-id="0b6c6-2908">1–3 буквы или цифры (оставшаяся часть BBAN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2908">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2909">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2909">Checksum</span></span>

<span data-ttu-id="0b6c6-2910">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2910">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2911">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2911">Definition</span></span>

<span data-ttu-id="0b6c6-2912">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2913">регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2913">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2914">находится ключевое слово из Keyword_swift.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2914">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2915">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2915">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="0b6c6-2916">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2916">Keyword_swift</span></span>

- <span data-ttu-id="0b6c6-2917">international organization for standardization 9362
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2917">international organization for standardization 9362</span></span> 
- <span data-ttu-id="0b6c6-2918">iso 9362
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2918">iso 9362</span></span> 
- <span data-ttu-id="0b6c6-2919">iso9362</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2919">iso9362</span></span> 
- <span data-ttu-id="0b6c6-2920">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2920">swift\#</span></span> 
- <span data-ttu-id="0b6c6-2921">swiftcode
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2921">swiftcode</span></span> 
- <span data-ttu-id="0b6c6-2922">swiftnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2922">swiftnumber</span></span> 
- <span data-ttu-id="0b6c6-2923">swiftroutingnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2923">swiftroutingnumber</span></span> 
- <span data-ttu-id="0b6c6-2924">код SWIFT</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2924">swift code</span></span> 
- <span data-ttu-id="0b6c6-2925">swift number #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2925">swift number #</span></span> 
- <span data-ttu-id="0b6c6-2926">swift routing number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2926">swift routing number</span></span> 
- <span data-ttu-id="0b6c6-2927">bic number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2927">bic number</span></span> 
- <span data-ttu-id="0b6c6-2928">bic code
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2928">bic code</span></span> 
- <span data-ttu-id="0b6c6-2929">БИК\#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2929">bic \#</span></span> 
- <span data-ttu-id="0b6c6-2930">БИК\#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2930">bic\#</span></span> 
- <span data-ttu-id="0b6c6-2931">bank identifier code
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2931">bank identifier code</span></span> 
- <span data-ttu-id="0b6c6-2932">標準化9362</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2932">標準化9362</span></span> 
- <span data-ttu-id="0b6c6-2933">迅速＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2933">迅速＃</span></span> 
- <span data-ttu-id="0b6c6-2934">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2934">SWIFTコード</span></span> 
- <span data-ttu-id="0b6c6-2935">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2935">SWIFT番号</span></span> 
- <span data-ttu-id="0b6c6-2936">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2936">迅速なルーティング番号</span></span> 
- <span data-ttu-id="0b6c6-2937">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2937">BIC番号</span></span> 
- <span data-ttu-id="0b6c6-2938">BICコード
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2938">BICコード</span></span> 
- <span data-ttu-id="0b6c6-2939">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2939">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="0b6c6-2940">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2940">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="0b6c6-2941">rapide\#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2941">rapide \#</span></span> 
- <span data-ttu-id="0b6c6-2942">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2942">code SWIFT</span></span> 
- <span data-ttu-id="0b6c6-2943">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2943">le numéro de swift</span></span> 
- <span data-ttu-id="0b6c6-2944">swift numéro d'acheminement
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2944">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="0b6c6-2945">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2945">le numéro BIC</span></span> 
- <span data-ttu-id="0b6c6-2946">\#БИК</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2946">\# BIC</span></span> 
- <span data-ttu-id="0b6c6-2947">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2947">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="0b6c6-2948">Национальный идентификатор, Тайвань</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2948">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2949">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2949">Format</span></span>

<span data-ttu-id="0b6c6-2950">Одна буква (английская), за которой следуют девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2950">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2951">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2951">Pattern</span></span>

<span data-ttu-id="0b6c6-2952">Один символ , за которым следуют девять цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2952">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="0b6c6-2953">Один символ (на английском языке, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2953">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-2954">Цифра 1 или 2</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2954">The digit "1" or "2"</span></span> 
- <span data-ttu-id="0b6c6-2955">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2955">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2956">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2956">Checksum</span></span>

<span data-ttu-id="0b6c6-2957">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2957">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2958">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2958">Definition</span></span>

<span data-ttu-id="0b6c6-2959">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2959">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2960">функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2960">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2961">находится ключевое слово из Keyword_taiwanese_national_id;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2961">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="0b6c6-2962">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2962">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2963">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2963">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="0b6c6-2964">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2964">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="0b6c6-2965">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2965">身份證字號</span></span> 
- <span data-ttu-id="0b6c6-2966">身份證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2966">身份證</span></span> 
- <span data-ttu-id="0b6c6-2967">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2967">身份證號碼</span></span> 
- <span data-ttu-id="0b6c6-2968">身份證號
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2968">身份證號</span></span> 
- <span data-ttu-id="0b6c6-2969">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2969">身分證字號</span></span> 
- <span data-ttu-id="0b6c6-2970">身分證 </span><span class="sxs-lookup"><span data-stu-id="0b6c6-2970">身分證</span></span> 
- <span data-ttu-id="0b6c6-2971">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2971">身分證號碼</span></span> 
- <span data-ttu-id="0b6c6-2972">身份證號
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2972">身份證號</span></span> 
- <span data-ttu-id="0b6c6-2973">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2973">身分證統一編號</span></span> 
- <span data-ttu-id="0b6c6-2974">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2974">國民身分證統一編號</span></span> 
- <span data-ttu-id="0b6c6-2975">簽名
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2975">簽名</span></span> 
- <span data-ttu-id="0b6c6-2976">蓋章
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2976">蓋章</span></span> 
- <span data-ttu-id="0b6c6-2977">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2977">簽名或蓋章</span></span> 
- <span data-ttu-id="0b6c6-2978">簽章</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2978">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="0b6c6-2979">	Номер паспорта гражданина Тайваня</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2979">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-2980">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2980">Format</span></span>

- <span data-ttu-id="0b6c6-2981">Номер паспорта Биометрическая: девяти цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2981">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="0b6c6-2982">Номер паспорта не Биометрическая: девяти цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2982">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-2983">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2983">Pattern</span></span>
<span data-ttu-id="0b6c6-2984">Номер паспорта Биометрическая:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2984">Biometric passport number:</span></span>
- <span data-ttu-id="0b6c6-2985">цифра "3";</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2985">The digit "3"</span></span> 
- <span data-ttu-id="0b6c6-2986">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2986">Eight digits</span></span>

<span data-ttu-id="0b6c6-2987">Номер паспорта Биометрическая без поддержки:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2987">Non-biometric passport number:</span></span>
- <span data-ttu-id="0b6c6-2988">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2988">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-2989">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2989">Checksum</span></span>

<span data-ttu-id="0b6c6-2990">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2990">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-2991">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2991">Definition</span></span>

<span data-ttu-id="0b6c6-2992">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2992">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-2993">регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2993">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-2994">находится ключевое слово из Keyword_taiwan_passport.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2994">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-2995">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2995">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="0b6c6-2996">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2996">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="0b6c6-2997">ROC passport number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2997">ROC passport number</span></span> 
- <span data-ttu-id="0b6c6-2998">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2998">Passport number</span></span> 
- <span data-ttu-id="0b6c6-2999">Passport не</span><span class="sxs-lookup"><span data-stu-id="0b6c6-2999">Passport no</span></span> 
- <span data-ttu-id="0b6c6-3000">Passport Num
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3000">Passport Num</span></span> 
- <span data-ttu-id="0b6c6-3001">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3001">Passport #</span></span> 
- <span data-ttu-id="0b6c6-3002">护照
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3002">护照</span></span> 
- <span data-ttu-id="0b6c6-3003">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3003">中華民國護照</span></span> 
- <span data-ttu-id="0b6c6-3004">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3004">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="0b6c6-3005">Номер удостоверения жителя Тайваня (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3005">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3006">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3006">Format</span></span>

<span data-ttu-id="0b6c6-3007">10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3007">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3008">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3008">Pattern</span></span>

<span data-ttu-id="0b6c6-3009">10 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3009">10 letters and digits:</span></span>
- <span data-ttu-id="0b6c6-3010">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3010">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="0b6c6-3011">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3011">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3012">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3012">Checksum</span></span>

<span data-ttu-id="0b6c6-3013">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3013">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3014">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3014">Definition</span></span>

<span data-ttu-id="0b6c6-3015">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3015">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3016">регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3016">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3017">находится ключевое слово из Keyword_taiwan_resident_certificate.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3017">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3018">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3018">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="0b6c6-3019">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3019">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="0b6c6-3020">Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3020">Resident Certificate</span></span> 
- <span data-ttu-id="0b6c6-3021">Резидентной Cert</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3021">Resident Cert</span></span> 
- <span data-ttu-id="0b6c6-3022">Resident Cert.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3022">Resident Cert.</span></span> 
- <span data-ttu-id="0b6c6-3023">Идентификация карточки</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3023">Identification card</span></span> 
- <span data-ttu-id="0b6c6-3024">Alien Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3024">Alien Resident Certificate</span></span> 
- <span data-ttu-id="0b6c6-3025">ARC
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3025">ARC</span></span> 
- <span data-ttu-id="0b6c6-3026">Taiwan Area Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3026">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="0b6c6-3027">TARC
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3027">TARC</span></span> 
- <span data-ttu-id="0b6c6-3028">居留證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3028">居留證</span></span> 
- <span data-ttu-id="0b6c6-3029">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3029">外僑居留證</span></span> 
- <span data-ttu-id="0b6c6-3030">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3030">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="0b6c6-3031">Тайский совокупности код</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3031">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3032">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3032">Format</span></span>

<span data-ttu-id="0b6c6-3033">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3033">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3034">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3034">Pattern</span></span>

<span data-ttu-id="0b6c6-3035">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3035">13 digits:</span></span>
- <span data-ttu-id="0b6c6-3036">Первая цифра не 0 или 9</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3036">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="0b6c6-3037">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3037">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3038">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3038">Checksum</span></span>

<span data-ttu-id="0b6c6-3039">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3039">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3040">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3040">Definition</span></span>

<span data-ttu-id="0b6c6-3041">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3041">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3042">Функция Func_Thai_Citizen_Id находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3042">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3043">Ключевое слово из Keyword_Thai_Citizen_Id найти.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3043">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="0b6c6-3044">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3044">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3045">Функция Func_Thai_Citizen_Id находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3045">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```
<!-- Thai Citizen ID -->
-<Entity id="44ca9e86-ead7-4c5d-884a-e2eaa401515e" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
      <Match idRef="Keyword_Thai_Citizen_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Thai_Citizen_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3046">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3046">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="0b6c6-3047">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3047">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="0b6c6-3048">ID Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3048">ID Number</span></span>
- <span data-ttu-id="0b6c6-3049">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3049">Identification Number</span></span>
- <span data-ttu-id="0b6c6-3050">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3050">บัตรประชาชน</span></span>
- <span data-ttu-id="0b6c6-3051">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3051">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="0b6c6-3052">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3052">บัตรประชาชน</span></span>
- <span data-ttu-id="0b6c6-3053">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3053">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="0b6c6-3054">Турецкий национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3054">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3055">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3055">Format</span></span>

<span data-ttu-id="0b6c6-3056">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3056">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3057">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3057">Pattern</span></span>

<span data-ttu-id="0b6c6-3058">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3058">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3059">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3059">Checksum</span></span>

<span data-ttu-id="0b6c6-3060">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3061">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3061">Definition</span></span>

<span data-ttu-id="0b6c6-3062">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3063">Функция Func_Turkish_National_Id находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3063">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3064">Ключевое слово из Keyword_Turkish_National_Id найти.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3064">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="0b6c6-3065">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3065">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3066">Функция Func_Turkish_National_Id находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3066">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```
<!-- Turkish National Identity -->
-<Entity id="fb621f20-3876-4cfc-acec-8c8e73ca32c7" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="85">
      <IdMatch idRef="Func_Turkish_National_Id"/>
      <Match idRef="Keyword_Turkish_National_Id"/>
   </Pattern>
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Func_Turkish_National_Id"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3067">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3067">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="0b6c6-3068">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3068">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="0b6c6-3069">No Kimlik ТРАД.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3069">TC Kimlik No</span></span>
- <span data-ttu-id="0b6c6-3070">Numarası Kimlik ТРАД.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3070">TC Kimlik numarası</span></span>
- <span data-ttu-id="0b6c6-3071">Vatandaşlık numarası</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3071">Vatandaşlık numarası</span></span>
- <span data-ttu-id="0b6c6-3072">Vatandaşlık нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3072">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="0b6c6-p141">Номер водительского удостоверения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3075">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3075">Format</span></span>

<span data-ttu-id="0b6c6-3076">Сочетание 18 букв и цифр в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3076">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3077">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3077">Pattern</span></span>

<span data-ttu-id="0b6c6-3078">18 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3078">18 letters and digits:</span></span>
- <span data-ttu-id="0b6c6-3079">Пять букв (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3079">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="0b6c6-3080">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3080">One digit</span></span> 
- <span data-ttu-id="0b6c6-3081">Пять цифр в формате даты ДДММГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3081">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="0b6c6-3082">Две буквы (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3082">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="0b6c6-3083">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3083">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3084">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3084">Checksum</span></span>

<span data-ttu-id="0b6c6-3085">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3085">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3086">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3086">Definition</span></span>

<span data-ttu-id="0b6c6-3087">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3087">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3088">функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3088">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3089">находится ключевое слово из Keyword_uk_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3089">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="0b6c6-3090">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3090">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3091">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3091">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="0b6c6-3092">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3092">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="0b6c6-3093">DVLA
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3093">DVLA</span></span> 
- <span data-ttu-id="0b6c6-3094">light vans
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3094">light vans</span></span> 
- <span data-ttu-id="0b6c6-3095">quadbikes
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3095">quadbikes</span></span> 
- <span data-ttu-id="0b6c6-3096">motor cars
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3096">motor cars</span></span> 
- <span data-ttu-id="0b6c6-3097">125cc</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3097">125cc</span></span> 
- <span data-ttu-id="0b6c6-3098">sidecar
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3098">sidecar</span></span> 
- <span data-ttu-id="0b6c6-3099">tricycles
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3099">tricycles</span></span> 
- <span data-ttu-id="0b6c6-3100">motorcycles
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3100">motorcycles</span></span> 
- <span data-ttu-id="0b6c6-3101">photocard licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3101">photocard licence</span></span> 
- <span data-ttu-id="0b6c6-3102">learner drivers
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3102">learner drivers</span></span> 
- <span data-ttu-id="0b6c6-3103">licence holder
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3103">licence holder</span></span> 
- <span data-ttu-id="0b6c6-3104">licence holders
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3104">licence holders</span></span> 
- <span data-ttu-id="0b6c6-3105">driving licences
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3105">driving licences</span></span> 
- <span data-ttu-id="0b6c6-3106">driving licence
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3106">driving licence</span></span> 
- <span data-ttu-id="0b6c6-3107">dual control car
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3107">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="0b6c6-p142">Регистрационный номер избирателя для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3110">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3110">Format</span></span>

<span data-ttu-id="0b6c6-3111">Две буквы, за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3111">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3112">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3112">Pattern</span></span>

<span data-ttu-id="0b6c6-3113">Две буквы (без учета регистра), за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3113">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3114">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3114">Checksum</span></span>

<span data-ttu-id="0b6c6-3115">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3115">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3116">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3116">Definition</span></span>

<span data-ttu-id="0b6c6-3117">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3118">регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3118">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3119">находится ключевое слово из Keyword_uk_electoral.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3119">A keyword from Keyword_uk_electoral is found.</span></span>

```
<!-- U.K. Electoral Number -->
<Entity id="a3eea206-dc0c-4f06-9e22-aa1be3059963" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_uk_electoral" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_electoral" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3120">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3120">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="0b6c6-3121">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3121">Keyword_uk_electoral</span></span>

- <span data-ttu-id="0b6c6-3122">council nomination
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3122">council nomination</span></span> 
- <span data-ttu-id="0b6c6-3123">nomination form
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3123">nomination form</span></span> 
- <span data-ttu-id="0b6c6-3124">electoral register

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3124">electoral register</span></span> 
- <span data-ttu-id="0b6c6-3125">electoral roll</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3125">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="0b6c6-p143">Номер национальной службы здравоохранения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3128">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3128">Format</span></span>

<span data-ttu-id="0b6c6-3129">10–17 цифр, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3129">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3130">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3130">Pattern</span></span>

<span data-ttu-id="0b6c6-3131">10-17 цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3131">10-17 digits:</span></span>
- <span data-ttu-id="0b6c6-3132">3 или 10 цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3132">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="0b6c6-3133">Пробел</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3133">A space</span></span> 
- <span data-ttu-id="0b6c6-3134">Три цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3134">Three digits</span></span> 
- <span data-ttu-id="0b6c6-3135">Пробел</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3135">A space</span></span> 
- <span data-ttu-id="0b6c6-3136">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3136">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3137">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3137">Checksum</span></span>

<span data-ttu-id="0b6c6-3138">Да</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3138">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3139">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3139">Definition</span></span>

<span data-ttu-id="0b6c6-3140">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3140">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3141">Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3141">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3142">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3142">One of the following is true:</span></span>
    - <span data-ttu-id="0b6c6-3143">найдено ключевое слово из Keyword_uk_nhs_number;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3143">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="0b6c6-3144">найдено ключевое слово из Keyword_uk_nhs_number1;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3144">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="0b6c6-3145">найдено ключевое слово из Keyword_uk_nhs_number_dob.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3145">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="0b6c6-3146">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3146">The checksum passes.</span></span>

```
<!-- U.K. NHS Number -->
<Entity id="3192014e-2a16-44e9-aa69-4b20375c9a78" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nhs_number" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nhs_number" />
          <Match idRef="Keyword_uk_nhs_number1" />
          <Match idRef="Keyword_uk_nhs_number_dob" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3147">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3147">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="0b6c6-3148">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3148">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="0b6c6-3149">national health service
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3149">national health service</span></span> 
- <span data-ttu-id="0b6c6-3150">nhs
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3150">nhs</span></span> 
- <span data-ttu-id="0b6c6-3151">health services authority

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3151">health services authority</span></span> 
- <span data-ttu-id="0b6c6-3152">health authority</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3152">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="0b6c6-3153">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3153">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="0b6c6-3154">patient id
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3154">patient id</span></span> 
- <span data-ttu-id="0b6c6-3155">patient identification
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3155">patient identification</span></span> 
- <span data-ttu-id="0b6c6-3156">patient no

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3156">patient no</span></span> 
- <span data-ttu-id="0b6c6-3157">patient number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3157">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="0b6c6-3158">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3158">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="0b6c6-3159">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3159">GP</span></span> 
- <span data-ttu-id="0b6c6-3160">DOB
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3160">DOB</span></span> 
- <span data-ttu-id="0b6c6-3161">D.O.B</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3161">D.O.B</span></span> 
- <span data-ttu-id="0b6c6-3162">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3162">Date of Birth</span></span> 
- <span data-ttu-id="0b6c6-3163">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3163">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="0b6c6-p144">Номер карты национального страхования для Соединенного Королевства (NINO)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3166">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3166">Format</span></span>

<span data-ttu-id="0b6c6-3167">7 или 9 символы, разделенных пробелами или тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3167">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3168">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3168">Pattern</span></span>

<span data-ttu-id="0b6c6-3169">Два возможных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3169">Two possible patterns:</span></span>

- <span data-ttu-id="0b6c6-3170">Две буквы (допустимый NINOs использовать только определенных символов в этом префикс, который проверяет этот шаблон; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3170">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="0b6c6-3171">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3171">Six digits</span></span>
- <span data-ttu-id="0b6c6-3172">Либо 'A', 'B', 'C', или имелся "(только для определенных символов в допускаются суффикс; не учитывают регистр, как префикс)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3172">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="0b6c6-3173">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3173">OR</span></span>

- <span data-ttu-id="0b6c6-3174">Два букв</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3174">Two letters</span></span>
- <span data-ttu-id="0b6c6-3175">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3175">A space or dash</span></span>
- <span data-ttu-id="0b6c6-3176">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3176">Two digits</span></span>
- <span data-ttu-id="0b6c6-3177">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3177">A space or dash</span></span>
- <span data-ttu-id="0b6c6-3178">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3178">Two digits</span></span>
- <span data-ttu-id="0b6c6-3179">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3179">A space or dash</span></span>
- <span data-ttu-id="0b6c6-3180">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3180">Two digits</span></span>
- <span data-ttu-id="0b6c6-3181">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3181">A space or dash</span></span>
- <span data-ttu-id="0b6c6-3182">Либо '', 'B', 'C', или имелся "</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3182">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3183">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3183">Checksum</span></span>

<span data-ttu-id="0b6c6-3184">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3185">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3185">Definition</span></span>

<span data-ttu-id="0b6c6-3186">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3186">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3187">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3187">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3188">находится ключевое слово из Keyword_uk_nino.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3188">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="0b6c6-3189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3190">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3190">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3191">ни одно ключевое слово из Keyword_uk_nino не находится.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3191">No keyword from Keyword_uk_nino is found.</span></span>

```
<!-- U.K. NINO -->
<Entity id="16c07343-c26f-49d2-a987-3daf717e94cc" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="1">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>    
     <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_nino" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_uk_nino" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3192">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="0b6c6-3193">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3193">Keyword_uk_nino</span></span>

- <span data-ttu-id="0b6c6-3194">national insurance number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3194">national insurance number</span></span> 
- <span data-ttu-id="0b6c6-3195">national insurance contributions
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3195">national insurance contributions</span></span> 
- <span data-ttu-id="0b6c6-3196">protection act
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3196">protection act</span></span> 
- <span data-ttu-id="0b6c6-3197">insurance
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3197">insurance</span></span> 
- <span data-ttu-id="0b6c6-3198">social security number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3198">social security number</span></span> 
- <span data-ttu-id="0b6c6-3199">insurance application
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3199">insurance application</span></span> 
- <span data-ttu-id="0b6c6-3200">medical application
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3200">medical application</span></span> 
- <span data-ttu-id="0b6c6-3201">social insurance
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3201">social insurance</span></span> 
- <span data-ttu-id="0b6c6-3202">medical attention
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3202">medical attention</span></span> 
- <span data-ttu-id="0b6c6-3203">социального страхования</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3203">social security</span></span> 
- <span data-ttu-id="0b6c6-3204">great britain
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3204">great britain</span></span> 
- <span data-ttu-id="0b6c6-3205">insurance
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3205">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="0b6c6-p145">Номер паспорта гражданина США и/или Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="0b6c6-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3208">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3208">Format</span></span>

<span data-ttu-id="0b6c6-3209">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3209">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3210">Pattern</span></span>

<span data-ttu-id="0b6c6-3211">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3211">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3212">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3212">Checksum</span></span>

<span data-ttu-id="0b6c6-3213">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3213">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3214">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3214">Definition</span></span>

<span data-ttu-id="0b6c6-3215">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3215">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3216">функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3216">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3217">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3217">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3218">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3218">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="0b6c6-3219">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3219">Keyword_passport</span></span>

- <span data-ttu-id="0b6c6-3220">Passport Number</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3220">Passport Number</span></span> 
- <span data-ttu-id="0b6c6-3221">
Passport No</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3221">Passport No</span></span> 
- <span data-ttu-id="0b6c6-3222">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3222">Passport #</span></span> 
- <span data-ttu-id="0b6c6-3223">Passport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3223">Passport#</span></span> 
- <span data-ttu-id="0b6c6-3224">PassportID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3224">PassportID</span></span> 
- <span data-ttu-id="0b6c6-3225">Passportno
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3225">Passportno</span></span> 
- <span data-ttu-id="0b6c6-3226">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3226">passportnumber</span></span> 
- <span data-ttu-id="0b6c6-3227">パスポート</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3227">パスポート</span></span> 
- <span data-ttu-id="0b6c6-3228">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3228">パスポート番号</span></span> 
- <span data-ttu-id="0b6c6-3229">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3229">パスポートのNum</span></span> 
- <span data-ttu-id="0b6c6-3230">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3230">パスポート＃</span></span> 
- <span data-ttu-id="0b6c6-3231">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3231">Numéro de passeport</span></span> 
- <span data-ttu-id="0b6c6-3232">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3232">Passeport n °</span></span> 
- <span data-ttu-id="0b6c6-3233">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3233">Passeport Non</span></span> 
- <span data-ttu-id="0b6c6-3234">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3234">Passeport #</span></span> 
- <span data-ttu-id="0b6c6-3235">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3235">Passeport#</span></span> 
- <span data-ttu-id="0b6c6-3236">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3236">PasseportNon</span></span> 
- <span data-ttu-id="0b6c6-3237">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3237">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="0b6c6-3238">Номер банковского счета для США</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3238">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3239">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3239">Format</span></span>

<span data-ttu-id="0b6c6-3240">8-17 цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3240">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3241">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3241">Pattern</span></span>

<span data-ttu-id="0b6c6-3242">8–17 последовательных цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3242">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3243">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3243">Checksum</span></span>

<span data-ttu-id="0b6c6-3244">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3244">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3245">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3245">Definition</span></span>

<span data-ttu-id="0b6c6-3246">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3247">регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3247">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3248">находится ключевое слово из Keyword_usa_Bank_Account.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3248">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3249">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3249">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="0b6c6-3250">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3250">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="0b6c6-3251">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3251">Checking Account Number</span></span> 
- <span data-ttu-id="0b6c6-3252">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3252">Checking Account</span></span> 
- <span data-ttu-id="0b6c6-3253">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3253">Checking Account #</span></span> 
- <span data-ttu-id="0b6c6-3254">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3254">Checking Acct Number</span></span> 
- <span data-ttu-id="0b6c6-3255">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3255">Checking Acct #</span></span> 
- <span data-ttu-id="0b6c6-3256">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3256">Checking Acct No.</span></span> 
- <span data-ttu-id="0b6c6-3257">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3257">Checking Account No.</span></span> 
- <span data-ttu-id="0b6c6-3258">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3258">Bank Account Number</span></span> 
- <span data-ttu-id="0b6c6-3259">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3259">Bank Account #</span></span> 
- <span data-ttu-id="0b6c6-3260">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3260">Bank Acct Number</span></span> 
- <span data-ttu-id="0b6c6-3261">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3261">Bank Acct #</span></span> 
- <span data-ttu-id="0b6c6-3262">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3262">Bank Acct No.</span></span> 
- <span data-ttu-id="0b6c6-3263">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3263">Bank Account No.</span></span> 
- <span data-ttu-id="0b6c6-3264">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3264">Savings Account Number</span></span> 
- <span data-ttu-id="0b6c6-3265">Savings Account.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3265">Savings Account.</span></span> 
- <span data-ttu-id="0b6c6-3266">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3266">Savings Account #</span></span> 
- <span data-ttu-id="0b6c6-3267">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3267">Savings Acct Number</span></span> 
- <span data-ttu-id="0b6c6-3268">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3268">Savings Acct #</span></span> 
- <span data-ttu-id="0b6c6-3269">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3269">Savings Acct No.</span></span> 
- <span data-ttu-id="0b6c6-3270">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3270">Savings Account No.</span></span> 
- <span data-ttu-id="0b6c6-3271">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3271">Debit Account Number</span></span> 
- <span data-ttu-id="0b6c6-3272">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3272">Debit Account</span></span> 
- <span data-ttu-id="0b6c6-3273">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3273">Debit Account #</span></span> 
- <span data-ttu-id="0b6c6-3274">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3274">Debit Acct Number</span></span> 
- <span data-ttu-id="0b6c6-3275">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3275">Debit Acct #</span></span> 
- <span data-ttu-id="0b6c6-3276">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3276">Debit Acct No.</span></span> 
- <span data-ttu-id="0b6c6-3277">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3277">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="0b6c6-3278">Номер водительского удостоверения для США</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3278">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3279">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3279">Format</span></span>

<span data-ttu-id="0b6c6-3280">Зависит от штата.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3280">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3281">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3281">Pattern</span></span>

<span data-ttu-id="0b6c6-3282">В зависимости от штата. Например, для Нью-Йорка:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3282">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="0b6c6-3283">Подойдут девять цифр в формате ццц ццц ццц.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3283">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="0b6c6-3284">Не подойдут девять цифр в формате ццццццццц.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3284">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3285">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3285">Checksum</span></span>

<span data-ttu-id="0b6c6-3286">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3287">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3287">Definition</span></span>

<span data-ttu-id="0b6c6-3288">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3289">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3289">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3290">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3290">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="0b6c6-3291">обнаружено ключевое слово из списка Keyword_us_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3291">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="0b6c6-3292">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3292">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3293">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3293">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3294">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3294">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="0b6c6-3295">находится ключевое слово из Keyword_us_drivers_license_abbreviations;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3295">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="0b6c6-3296">ни одно ключевое слово из Keyword_us_drivers_license не находится.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3296">No keyword from Keyword_us_drivers_license is found.</span></span>

```
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license" />
    </Pattern>
    <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_new_york_drivers_license_number" />
        <Match idRef="Keyword_new_york_drivers_license_name" />
        <Match idRef="Keyword_us_drivers_license_abbreviations" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_us_drivers_license" />
        </Any>
    </Pattern>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3297">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3297">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="0b6c6-3298">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3298">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="0b6c6-3299">DL</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3299">DL</span></span> 
- <span data-ttu-id="0b6c6-3300">DLS</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3300">DLS</span></span> 
- <span data-ttu-id="0b6c6-3301">CDL</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3301">CDL</span></span> 
- <span data-ttu-id="0b6c6-3302">CDLS</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3302">CDLS</span></span> 
- <span data-ttu-id="0b6c6-3303">ID</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3303">ID</span></span> 
- <span data-ttu-id="0b6c6-3304">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3304">IDs</span></span> 
- <span data-ttu-id="0b6c6-3305">DL#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3305">DL#</span></span> 
- <span data-ttu-id="0b6c6-3306">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3306">DLS#</span></span> 
- <span data-ttu-id="0b6c6-3307">CDL#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3307">CDL#</span></span> 
- <span data-ttu-id="0b6c6-3308">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3308">CDLS#</span></span> 
- <span data-ttu-id="0b6c6-3309">ID#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3309">ID#</span></span>
- <span data-ttu-id="0b6c6-3310">
IDs#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3310">IDs#</span></span> 
- <span data-ttu-id="0b6c6-3311">идентификатор</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3311">ID number</span></span> 
- <span data-ttu-id="0b6c6-3312">ID numbers
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3312">ID numbers</span></span> 
- <span data-ttu-id="0b6c6-3313">LIC</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3313">LIC</span></span> 
- <span data-ttu-id="0b6c6-3314">LIC#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3314">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="0b6c6-3315">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3315">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="0b6c6-3316">DriverLic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3316">DriverLic</span></span> 
- <span data-ttu-id="0b6c6-3317">DriverLics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3317">DriverLics</span></span> 
- <span data-ttu-id="0b6c6-3318">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3318">DriverLicense</span></span> 
- <span data-ttu-id="0b6c6-3319">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3319">DriverLicenses</span></span> 
- <span data-ttu-id="0b6c6-3320">Драйвер Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3320">Driver Lic</span></span> 
- <span data-ttu-id="0b6c6-3321">Драйвер Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3321">Driver Lics</span></span> 
- <span data-ttu-id="0b6c6-3322">Драйвер лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3322">Driver License</span></span> 
- <span data-ttu-id="0b6c6-3323">Драйвер лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3323">Driver Licenses</span></span> 
- <span data-ttu-id="0b6c6-3324">DriversLic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3324">DriversLic</span></span> 
- <span data-ttu-id="0b6c6-3325">DriversLics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3325">DriversLics</span></span> 
- <span data-ttu-id="0b6c6-3326">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3326">DriversLicense</span></span> 
- <span data-ttu-id="0b6c6-3327">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3327">DriversLicenses</span></span> 
- <span data-ttu-id="0b6c6-3328">Драйверы Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3328">Drivers Lic</span></span> 
- <span data-ttu-id="0b6c6-3329">Драйверы Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3329">Drivers Lics</span></span> 
- <span data-ttu-id="0b6c6-3330">Драйверы лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3330">Drivers License</span></span> 
- <span data-ttu-id="0b6c6-3331">Драйверы лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3331">Drivers Licenses</span></span> 
- <span data-ttu-id="0b6c6-3332">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3332">Driver'Lic</span></span> 
- <span data-ttu-id="0b6c6-3333">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3333">Driver'Lics</span></span> 
- <span data-ttu-id="0b6c6-3334">Driver'License</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3334">Driver'License</span></span> 
- <span data-ttu-id="0b6c6-3335">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3335">Driver'Licenses</span></span> 
- <span data-ttu-id="0b6c6-3336">Драйвер ' Lic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3336">Driver' Lic</span></span> 
- <span data-ttu-id="0b6c6-3337">Драйвер ' Lics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3337">Driver' Lics</span></span> 
- <span data-ttu-id="0b6c6-3338">Драйвер "лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3338">Driver' License</span></span> 
- <span data-ttu-id="0b6c6-3339">Драйвер "лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3339">Driver' Licenses</span></span>
- <span data-ttu-id="0b6c6-3340">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3340">Driver'sLic</span></span> 
- <span data-ttu-id="0b6c6-3341">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3341">Driver'sLics</span></span> 
- <span data-ttu-id="0b6c6-3342">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3342">Driver'sLicense</span></span> 
- <span data-ttu-id="0b6c6-3343">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3343">Driver'sLicenses</span></span> 
- <span data-ttu-id="0b6c6-3344">Lic драйвера</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3344">Driver's Lic</span></span> 
- <span data-ttu-id="0b6c6-3345">Lics драйвера</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3345">Driver's Lics</span></span> 
- <span data-ttu-id="0b6c6-3346">Водительского удостоверения для лицензии</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3346">Driver's License</span></span> 
- <span data-ttu-id="0b6c6-3347">Водительского удостоверения для лицензий</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3347">Driver's Licenses</span></span> 
- <span data-ttu-id="0b6c6-3348">identification number
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3348">identification number</span></span> 
- <span data-ttu-id="0b6c6-3349">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3349">identification numbers</span></span> 
- <span data-ttu-id="0b6c6-3350">identification #
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3350">identification #</span></span> 
- <span data-ttu-id="0b6c6-3351">Карточка</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3351">id card</span></span> 
- <span data-ttu-id="0b6c6-3352">Идентификатор карточки</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3352">id cards</span></span> 
- <span data-ttu-id="0b6c6-3353">Идентификация карточки</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3353">identification card</span></span> 
- <span data-ttu-id="0b6c6-3354">Идентификация карты</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3354">identification cards</span></span> 
- <span data-ttu-id="0b6c6-3355">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3355">DriverLic#</span></span> 
- <span data-ttu-id="0b6c6-3356">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3356">DriverLics#</span></span> 
- <span data-ttu-id="0b6c6-3357">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3357">DriverLicense#</span></span> 
- <span data-ttu-id="0b6c6-3358">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3358">DriverLicenses#</span></span> 
- <span data-ttu-id="0b6c6-3359">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3359">Driver Lic#</span></span> 
- <span data-ttu-id="0b6c6-3360">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3360">Driver Lics#</span></span> 
- <span data-ttu-id="0b6c6-3361">Драйвер лицензии #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3361">Driver License#</span></span> 
- <span data-ttu-id="0b6c6-3362">Драйвер лицензий #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3362">Driver Licenses#</span></span> 
- <span data-ttu-id="0b6c6-3363">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3363">DriversLic#</span></span> 
- <span data-ttu-id="0b6c6-3364">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3364">DriversLics#</span></span> 
- <span data-ttu-id="0b6c6-3365">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3365">DriversLicense#</span></span> 
- <span data-ttu-id="0b6c6-3366">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3366">DriversLicenses#</span></span> 
- <span data-ttu-id="0b6c6-3367">Драйверы Lic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3367">Drivers Lic#</span></span> 
- <span data-ttu-id="0b6c6-3368">Драйверы Lics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3368">Drivers Lics#</span></span> 
- <span data-ttu-id="0b6c6-3369">Драйверы лицензии #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3369">Drivers License#</span></span> 
- <span data-ttu-id="0b6c6-3370">Драйверы лицензий #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3370">Drivers Licenses#</span></span> 
- <span data-ttu-id="0b6c6-3371">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3371">Driver'Lic#</span></span> 
- <span data-ttu-id="0b6c6-3372">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3372">Driver'Lics#</span></span> 
- <span data-ttu-id="0b6c6-3373">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3373">Driver'License#</span></span> 
- <span data-ttu-id="0b6c6-3374">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3374">Driver'Licenses#</span></span> 
- <span data-ttu-id="0b6c6-3375">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3375">Driver' Lic#</span></span> 
- <span data-ttu-id="0b6c6-3376">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3376">Driver' Lics#</span></span> 
- <span data-ttu-id="0b6c6-3377">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3377">Driver' License#</span></span> 
- <span data-ttu-id="0b6c6-3378">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3378">Driver' Licenses#</span></span> 
- <span data-ttu-id="0b6c6-3379">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3379">Driver'sLic#</span></span> 
- <span data-ttu-id="0b6c6-3380">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3380">Driver'sLics#</span></span> 
- <span data-ttu-id="0b6c6-3381">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3381">Driver'sLicense#</span></span> 
- <span data-ttu-id="0b6c6-3382">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3382">Driver'sLicenses#</span></span> 
- <span data-ttu-id="0b6c6-3383">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3383">Driver's Lic#</span></span> 
- <span data-ttu-id="0b6c6-3384">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3384">Driver's Lics#</span></span> 
- <span data-ttu-id="0b6c6-3385">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3385">Driver's License#</span></span> 
- <span data-ttu-id="0b6c6-3386">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3386">Driver's Licenses#</span></span> 
- <span data-ttu-id="0b6c6-3387">Карточка #</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3387">id card#</span></span> 
- <span data-ttu-id="0b6c6-3388">id cards#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3388">id cards#</span></span> 
- <span data-ttu-id="0b6c6-3389">identification card#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3389">identification card#</span></span> 
- <span data-ttu-id="0b6c6-3390">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3390">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="0b6c6-3391">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3391">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="0b6c6-3392">Аббревиатура штата (например, NY)
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3392">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="0b6c6-3393">Название штата (например, New York)
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3393">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="0b6c6-3394">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3394">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3395">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3395">Format</span></span>

<span data-ttu-id="0b6c6-3396">Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3396">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3397">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3397">Pattern</span></span>

<span data-ttu-id="0b6c6-3398">С форматированием</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3398">Formatted:</span></span>
- <span data-ttu-id="0b6c6-3399">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3399">The digit "9"</span></span> 
- <span data-ttu-id="0b6c6-3400">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3400">Two digits</span></span> 
- <span data-ttu-id="0b6c6-3401">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3401">A space or dash</span></span> 
- <span data-ttu-id="0b6c6-3402">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3402">A "7" or "8"</span></span> 
- <span data-ttu-id="0b6c6-3403">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3403">A digit</span></span> 
- <span data-ttu-id="0b6c6-3404">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3404">A space, or dash</span></span> 
- <span data-ttu-id="0b6c6-3405">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3405">Four digits</span></span>

<span data-ttu-id="0b6c6-3406">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3406">Unformatted:</span></span>
- <span data-ttu-id="0b6c6-3407">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3407">The digit "9"</span></span> 
- <span data-ttu-id="0b6c6-3408">Две цифры</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3408">Two digits</span></span> 
- <span data-ttu-id="0b6c6-3409">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3409">A "7" or "8"</span></span> 
- <span data-ttu-id="0b6c6-3410">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3410">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3411">Checksum</span></span>

<span data-ttu-id="0b6c6-3412">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3412">No</span></span>

### <a name="definition"></a><span data-ttu-id="0b6c6-3413">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3413">Definition</span></span>

<span data-ttu-id="0b6c6-3414">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3415">Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3415">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3416">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3416">At least one of the following is true:</span></span>
    - <span data-ttu-id="0b6c6-3417">найдено ключевое слово из Keyword_itin;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3417">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="0b6c6-3418">функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3418">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="0b6c6-3419">функция Func_us_date находит дату в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3419">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="0b6c6-3420">найдено ключевое слово из Keyword_itin_collaborative.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3420">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="0b6c6-3421">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3421">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3422">Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3422">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3423">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3423">At least one of the following is true:</span></span>
    - <span data-ttu-id="0b6c6-3424">найдено ключевое слово из Keyword_itin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3424">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="0b6c6-3425">функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3425">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="0b6c6-3426">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3426">The function Func_us_date finds a date in the right date format.</span></span>

```
<!-- U.S. Individual Taxpayer Identification Number (ITIN) -->
<Entity id="e55e2a32-f92d-4985-a35d-a0b269eb687b" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_formatted_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
          <Match idRef="Keyword_itin_collaborative" />
        </Any>
    </Pattern>
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_itin" />
        <Match idRef="Keyword_itin" />
        <Any minMatches="1">
          <Match idRef="Keyword_itin_collaborative" />
          <Match idRef="Func_us_address" />
          <Match idRef="Func_us_date" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3427">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3427">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="0b6c6-3428">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3428">Keyword_itin</span></span>

- <span data-ttu-id="0b6c6-3429">taxpayer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3429">taxpayer</span></span> 
- <span data-ttu-id="0b6c6-3430">tax id
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3430">tax id</span></span> 
- <span data-ttu-id="0b6c6-3431">tax identification
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3431">tax identification</span></span> 
- <span data-ttu-id="0b6c6-3432">itin
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3432">itin</span></span> 
- <span data-ttu-id="0b6c6-3433">SSN</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3433">ssn</span></span> 
- <span data-ttu-id="0b6c6-3434">tin
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3434">tin</span></span> 
- <span data-ttu-id="0b6c6-3435">социального страхования</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3435">social security</span></span> 
- <span data-ttu-id="0b6c6-3436">tax payer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3436">tax payer</span></span> 
- <span data-ttu-id="0b6c6-3437">itins
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3437">itins</span></span> 
- <span data-ttu-id="0b6c6-3438">taxid

</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3438">taxid</span></span> 
- <span data-ttu-id="0b6c6-3439">individual taxpayer
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3439">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="0b6c6-3440">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3440">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="0b6c6-3441">License</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3441">License</span></span> 
- <span data-ttu-id="0b6c6-3442">DL</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3442">DL</span></span> 
- <span data-ttu-id="0b6c6-3443">DOB
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3443">DOB</span></span> 
- <span data-ttu-id="0b6c6-3444">Birthdate</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3444">Birthdate</span></span> 
- <span data-ttu-id="0b6c6-3445">День рождения </span><span class="sxs-lookup"><span data-stu-id="0b6c6-3445">Birthday</span></span> 
- <span data-ttu-id="0b6c6-3446">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3446">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="0b6c6-3447">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3447">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="0b6c6-3448">Формат</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3448">Format</span></span>

<span data-ttu-id="0b6c6-3449">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3449">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="0b6c6-3450">Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3450">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="0b6c6-3451">Шаблон</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3451">Pattern</span></span>

<span data-ttu-id="0b6c6-3452">Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3452">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="0b6c6-3453">Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3453">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="0b6c6-3454">Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3454">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="0b6c6-3455">Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3455">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="0b6c6-3456">Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3456">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="0b6c6-3457">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3457">Checksum</span></span>

<span data-ttu-id="0b6c6-3458">Нет</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3458">No</span></span>


### <a name="definition"></a><span data-ttu-id="0b6c6-3459">Определение</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3459">Definition</span></span>

<span data-ttu-id="0b6c6-3460">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3461">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3461">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3462">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3462">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="0b6c6-3463">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3464">Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3464">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3465">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3465">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="0b6c6-3466">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3467">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3467">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3468">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3468">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="0b6c6-3469">Функция Func_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3469">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="0b6c6-3470">Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3470">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="0b6c6-3471">Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3471">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="0b6c6-3472">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3472">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="0b6c6-3473">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3473">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

```
<!-- U.S. Social Security Number (SSN) -->
    <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="0b6c6-3474">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3474">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="0b6c6-3475">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3475">Keyword_ssn</span></span>

- <span data-ttu-id="0b6c6-3476">Social Security
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3476">Social Security</span></span> 
- <span data-ttu-id="0b6c6-3477">Social Security#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3477">Social Security#</span></span> 
- <span data-ttu-id="0b6c6-3478">Soc Sec
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3478">Soc Sec</span></span> 
- <span data-ttu-id="0b6c6-3479">SSN</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3479">SSN</span></span> 
- <span data-ttu-id="0b6c6-3480">SSNS
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3480">SSNS</span></span> 
- <span data-ttu-id="0b6c6-3481">SSN#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3481">SSN#</span></span> 
- <span data-ttu-id="0b6c6-3482">SS#
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3482">SS#</span></span> 
- <span data-ttu-id="0b6c6-3483">SSID
</span><span class="sxs-lookup"><span data-stu-id="0b6c6-3483">SSID</span></span> 
   

